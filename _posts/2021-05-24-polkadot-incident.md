#Polkadot validator went offline

Due to a [memory issue on v0.9.2](https://github.com/paritytech/substrate/pull/8892), the Polkadot chain halted at 11:30 UTC on May 24th, 2021. Parity issues an emergency announcement to downgrade to 0.8.30.

We see that our polkadot nodes have stopped syncing and a restart does not help.

## Setup

The polkadot deployment is done with terraform and Google Cloud Build. We use a custom entrypoint shell called [`push_containers`](https://github.com/midl-dev/polkadot-k8s/blob/master/terraform/k8s.tf#L1-L35). A custom container is built on top of the polkadot container version passed as parameter, with the entrypoint script injected and some extra packages like `jq` and `xxd` added.

We perform the downgrade, by passing version v0.8.30 to the [terraform module variable](https://github.com/midl-dev/polkadot-k8s/blob/master/terraform/variables.tf#L39-L42) responsible for MIDL polkadot deployments, however we observe that after deployment is complete, the polkadot version is still v0.9.2.

We verified that the image pull policy of the statefulset was set to `always` and that at each pod restart, the right image digest would indeed be pulled.

We then attempted several things:

* bypass the string replacement logic in the dockerfile template by hardcoding the version, to no avail,
* bypass cloud build by building locally from dev machine and pushing, to no avail,
* bypass tag selection of the image
* rebuild all containers for all polkadot nodes, to test whether improper isolation between namespaces may be causing this

Meanwhile, the epoch went over and the validator was marked offline.

## Root cause

The custom container Dockerfile contains an `apt-get upgrade` instruction which upgrades the container to v0.9.2 despite the original container having version v0.8.30. Therefore, despite the origin container being set to the right version, the final one always has the latest released version.

We removed the apt-get upgrade instruction and the pipeline now behaves as expected. We then redeclared the validate intention of the nominator at 17:55 UTC on May 24th, 2021.

Commit of the fix: https://github.com/midl-dev/polkadot-k8s/commit/05364f80e21636094d3e39283b546b649dce4ef2

## Analysis / next steps

A couple of weeks ago we noticed that the container version was not always set as expected based on the config, but we did not take further action.

We have been following a policy of rebuilding containers to inject entrypoints. In hindsight, it appears safer to always use the origin containers whenever possible, and inject the entrypoint with a configmap, because:

* it speeds up upgrade/downgrade operations
* it makes it easier to debug which container version we are running

We will be doing that moving forwards.
