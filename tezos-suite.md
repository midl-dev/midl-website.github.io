---
layout: default
title: MIDL.dev - Staking as a service
subTitle: Tezos suite
---

# Tezos suite by MIDL.dev

MIDL.dev maintains the following open-source software projects to make it easy to deploy a baking setup:

* [Tezos-on-GKE](https://github.com/midl-dev/tezos-on-gke): deploys a secure baker setup in Google Kubernetes Engine in just one command
* [Tezos-remote-signer-OS](https://github.com/midl-dev/tezos-remote-signer-os): operating system for a secure, highly available Tezos remote signer setup
* [Tezos-auxiliary-cluster](https://github.com/midl-dev/tezos-auxiliary-cluster): a toolkit for public bakers: monitors baking operations, issues payouts, and generates a dynamic baking website
* [Tezos-snapshot-generator](https://github.com/midl-dev/tezos-snapshot-generator): a snapshot engine that periodically generates Tezos snapshots and makes them available.

## Documentation

The documentation for the Tezos suite can be found [here](https://tezos-docs.midl.dev).

## Architecture

The best known baking tool, [Kiln](https://gitlab.com/obsidian.systems/kiln), is a complete solution for home baking, to be installed on physical hardware. Tezos-on-GKE, in contrast, outsources most of the computing to the cloud, increasing reliability and decreasing the operating burden of the baking operations.

Signing operations on a hardware wallet is best kept in hardware under the baker's control. We provide a hardened remote signer OS that allows you to securely connect to the cloud setup and sign baking and endorsing operations.

Since the signing operations are of paramount importance, a separate Kubernetes cluster with separate authentication credentials takes care of the auxiliary operations such as payout and monitoring.

These three projects, taken together, allow you to deploy a secure, best-practices baking operation.

The setup supports Tezos mainnet as well as Carthagenet and future test networks.

## Roadmap

We are the recipients of a [Tezos foundation grant](https://tezos.foundation/grants/) for this project. As part of this, we will:

* improve baking operation uptime by deploying an active-active baking setup with a Kubernetes operator
* increase awareness of the tool by writing documentation, writing articles and interacting with the community of users
