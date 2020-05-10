---
layout: cryptos
img: Tezos_logo.png
status: Available now
category: Services
title: Midl.dev - Tezos
subTitle: Become a baker.<br/>Maximize your earnings.
staker: Become a baker
short_title: tezos
crypto_name: Tezos
permalink: /tezos/
order_number: 2
description: | 
---

# Bake your Tezos with Midl.dev

Tezos bakers and exchanges take fees. Instead, we can help you be a baker and keep the rewards to yourself!

{% include _cryptocurrencies/tezos_table.md %}

[How did we calculate this ?](/tezos/figures/)

All we take is a monthly fee - in fiat currency - to manage your infrastructure.

## You hold the keys

We are a non-custodial staking-as-a-service offering.

We provide you with a signing device - a small computer. Connect your Ledger device to it, keep it online - we take care of the rest.

This is secure. The hardware wallet remains in your possession - we can not access your funds.

We eat our own dog food. We have one year of experience staking Tezos on our own baking service -  [Hodl.farm](hodl.farm). All our infrastructure is open-source.

## Offerings

| Solo baker                              | Public baker                            |
|-----------------------------------------|-----------------------------------------|
| Secure, distributed baking nodes        | Secure, distributed baking nodes        |
| Signing kit (redundant signing devices) | Signing kit (redundant signing devices) |
|                                         | Payout engine                           |
|                                         | Website template for payout lookup      |

### Solo baker

You own a few rolls. Instead of delegating them to a baker, you become a delegator. You bake and endose blocks occasionally, and the generated rewards go to your account.

You may also group with a few friends and split the rewards between yourselves.

We maintain full nodes, as well as baking and endorsing daemons for you. Your tezos key is on a Ledger that you control. Install and run the [Tezos baking app](https://github.com/obsidiansystems/ledger-app-tezos) and connect it to the signer. When it is your turn to bake/endorse, our infrastrucure will send a signing request to your signer.

The signer is a Raspberry Pi with battery backup, an alternative 4G connection, and a hot spare that you may place in a different location.

### Public baker

In addition to the solo baker setup described above, you also publish your Tezos baking address so Tezos delegators may delegate to you.

In addition to your baking address, you maintain a payout address. This payout address must be replenished frequently by you.

We run a payout bot that pays your delegates every cycle from the payout address.

We run a website publication mechanism so your delegates can check their contribution and their most recent payouts just by entering their address on your website.
