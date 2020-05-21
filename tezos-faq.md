---
layout: default
title: Midl.dev - Tezos - Frequently asked questions
---

## Tezos Frequently asked questions

**Q: Since you have access to the signer, can't you just sign whatever you want over it and drain the bond from the baker account?**

A: Our remote signer only works with keys stored in a Ledger Nano S, and the baking app on. Ledger Tezos baking app will [only sign baking and endorsement operations](https://github.com/obsidiansystems/ledger-app-tezos#using-the-tezos-baking-application-nano-s-only). So while we have full access to the remote signer, we can't drain the account.

We also support customers setting up their own remote signers, in that case, we will ensure that they filter by transaction type.

**Q: The tezos-signer natively supports authentication using a keypair - why not use this and avoid the ssh tunnel?**

A: The remote signer setup "just works" from anywhere including NATted environments. And when the primary internet connection fails, the [4G LTE dongle takes over](https://github.com/hodl-dot-farm/tezos-remote-signer-os/blob/master/tezos-remote-signer/templates/usr/bin/isp_failover). On the other end, the ssh server endpoint is a hostname pointing to a [cloud load balancer](https://github.com/midl-dev/tezos-on-gke/blob/master/tezos-baker/tezos-remote-signer-forwarder.yaml#L5-L12). So originating the connection from the remote signer is the better choice for a highly reliable signer. You just plug it in and it "phones home".

The second reason is that the remote signer is fully managed by us (OS upgrades, upgrades of the signer software itself) so we need access to more than the signer protocol, namely ssh login and monitoring endpoints. They all go through the tunnel.

**Q: How is failover between the two signers managed? Is it automatic or manual?**

A: automatic with haproxy

**Q: Why not run the entire baking operation from the remote signer ? Why use cloud instances ?**

A: As Tezos evolves continuously, the requirements of running a full node tend to grow. For example, the introduction of Sapling zero-knowledge smart contracts in protocol 007 is likely to hike the CPU and/or RAM required. Also, the size of the blockchain may outgrow storage capabilities of the node.

On the other hand, the remote signer's requirements are tiny, so rolling out new hardware will be rare. The cloud is able to autoscale so that the baking operations will never be impacted by an increase in computing requirements.

**Q: Is there a centralization concern if too many bakers use MIDL.dev ?**

A: Having several baking nodes managed by a single entity increases centralization. Specifically, there is risk of us accidentally or maliciously knocking off a large section of the Tezos network. However:

* the accidental risk can be mitigated by good engineering practices: leveraging multi-cloud, having several management contexts for several nodes
* the malicious risk should be put in perspective: if the model we are proposing is successful, it will likely be emulated, which will reduce the centralization risk.

There are a lot of XTZ holders today using custodial solutions for lack of technical ability to bake. These holders switching to a non-custodial service like ours is a decentralization win: users can independently vote for governance proposals and it reduces the size of large custodians' own stake in the network.
