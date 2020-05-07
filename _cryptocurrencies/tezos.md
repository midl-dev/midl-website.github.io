---
layout: cryptos
img: Tezos_logo.png
status: Available now
logosize: 100px
category: Services
title: Midl.dev - Tezos
subTitle: Don't delegate.<br/>Bake.
short_title: tezos
description: | 
---

# Bake your Tezos with Midl.dev

Tezos bakers and exchanges take fees. With Midl.dev, be a delegate instead and keep all the rewards to yourself !

We have one year of experience staking Tezos on [Hodl.farm](hodl.farm) and all our infrastructure is open-source.

Our offerings are:

## Solo baker

You own a few rolls. Instead of delegating them to a baker, you become a delegator. You bake and endose blocks occasionally, and the generated rewards go to your account.

You may also group with a few friends and split the rewards between yourselves.

We maintain full nodes, as well as baking and endorsing daemons for you. Your tezos key is on a Ledger that you control. Install and run the [Tezos baking app](https://github.com/obsidiansystems/ledger-app-tezos) and connect it to the signer. When it is your turn to bake/endorse, our infrastrucure will send a signing request to your signer.

The signer is a Raspberry Pi with battery backup, an alternative 4G connection, and a hot spare that you may place in a different location.

## Public baker

In addition to the solo baker setup described above, you also publish your Tezos baking address so Tezos delegators may delegate to you.

In addition to your baking address, you maintain a payout address. This payout address must be replenished frequently by you.

We run a payout bot that pays your delegates every cycle from the payout address.

We run a website publication mechanism so your delegates can check their contribution and their most recent payouts just by entering their address on your website.
