---
layout: default
title: Staking as a service
---

## What is staking

Proof of stake blockchains have inflation. Token holders must take action for their assets to grow: they must put them at stake on the network.

Let us go through the different options that a token holder has to do this today.

Alice is a token holder. She has overcome great pains, read documentation and chatted on staking forums, and has put a lot of time into deploying a validator node - a blockchain node that participates in consensus and generates blocks. She keeps the full extent of the rewards that the network allocates to her. But the network is self-governing, and frequent changes in the protocol requires constant upgrades to the infrastructure, so Alice has unwittingly committed to spend a significant amount of time in the long run to keep her operations up.

Proof of stake networks have taken this into account and have introduced the concept of delegation. This may be named differently (in Polkadot, it's called nomination) but it boils down to the same: a special network operation lets you delegate your tokens to a separate entity, called a delegate, baker, or validator depending on the network. This entity uses your state to participate in the network, and it is then responsible for sending rewards your way, taking a fee in the process. This fee can be substantial, especially if your token is worth more over time.

Some delegates are opaque entities, other are well-known cryptocurrency exchanges that take custody of your assets. Bob has his assets in one such exchange. He sleeps comfortably at night knowing that his assets are taken good care of. His portfolio is growing over time. One year from now, even if Bob has forgotten everything about this specific token, he can still transfer or exchange it using a familiar UI. But that peace of mind comes at a price - 25% of the gains.

Midl.dev introduces a third way, suitable for people who have enough assets that they wish they could cut the middleman and directly participate in the network - but not quite enough to mobilize the technological and human requirements to do so.

Charlene has been holding crypto for years and is comfortable being her own bank and store her coins on her Ledger™ hardware wallet. But she is annoyed by the 10% fee that her validator is taking.

Charlene now wants to participate directly in the network, produce blocks and endorsements, and participate in governanace. So Charlene gets in touch with the friendly team at midl.dev. They outfit her with a signing kit.

For a fixed monthly fee (in fiat), Charlene can sleep at night. She needs not worry about downtime, protocol upgrades, or network partitions. She knows that her funds are growing to the maximum extent possible.

This method is strictly non custodial. We do not control Charlene's funds. We procure the signing kit, but Charlene procures the Ledgers. She alone configures them and transfers her tokens to it.

In case of emergency, Charlene can even (proverbially) pull the plug from the signer device for her funds to instantly return to a cold state.

## Our experience

We have 10 years of experience managing infrastructure, and one year of experience baking Tezos with [Hodl.farm](https://hodl.farm). All our infrastructure is [open-source](https://github.com/hodl-dot-farm) and auditable.

Our approach is centered on two Fundamental Truths:

* the most reliable blockchain nodes run in the cloud. Cloud providers invest considerable amounts of time, money and brainpower on keeping the operations up. A home setup does not even come close to competing.
* not your keys, not your $FAVOURITE_TOKEN. While the cloud is great, do not put your keys in there ! The only acceptable storage for your key is a Hardware Security Module under your full, exclusive control.

Our own validator is the canonical deployment for the staking infrastructure. When rolling out new code, we always push it first to Hodl.farm before pushing it to our customer's infrastructure.

## The signer pattern

A digital currency has many moving parts. Nodes communicate using a peer to peer protocol. Self-contained execution engines run smart contracts. Finality gadgets dabble with byzantine consensus.

But a fundamental building block is public key cryptography. You, the token holder, own a full node. The full node preps a string of bits to broadcast to the network. You sign these bytes using your private key, and off they go.
The signing step is a simple process. Is it also the most critical in terms of operational security. Your keys need to be on a hot piece of silicon that takes unsigned strings and returns signed strings. Well architected blockchain ecosystems have come up with a dedicated daemon that does just that - signing.

This is how we conciliate the two Fundamental Truths: the bulk of the work is done in reliable, redundant, geographically distributed nodes in a cloud platform, but the critical signing operations are done on devies that you control !
