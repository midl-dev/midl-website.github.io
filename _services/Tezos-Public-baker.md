---
layout: default
title: Staking-as-a-service - Tezos public baker
subTitle: How it works
permalink: /tezos-public-baker/
---

## Staking-as-a-service solution for public baker

### Who should become a public baker?

You have already established yourself as a baker. Now you would like to further benefit from the baking operation and maximize your earnings by collecting delegation fees. 

### How it works

You publish your Tezos baking address so Tezos delegators may delegate to you. You define your fee rate.

We maintain full nodes, as well as baking and endorsing daemons for you. Your tezos key is on a Ledger that you control. You install and run the [Tezos baking app]("https://github.com/obsidiansystems/ledger-app-tezos") and connect it to the signer. When it is your turn to bake/endorse, our infrastructure will send a signing request to your signer.

<b>The signer</b> is a Raspberry Pi with battery backup, an alternative 4G connection, and a hot spare that you may place in a different location.

In addition to your baking address, you maintain a payout address. This payout address must be replenished frequently by you.

We run a payout bot that pays your delegates every cycle from the payout address.

We run a website publication mechanism so your delegates can check their contribution and their most recent payouts just by entering their address on your website.

<b>You remain a full custodian of your keys throughout the whole process.</b>