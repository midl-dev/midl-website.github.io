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

{% include _cryptocurrencies/service_types_table.md %}

<div style="padding-top:50px;" id="solobaker"></div>
  

### Solo baker

You own a few rolls. Instead of delegating them to a baker, you become a baker. You bake and endorse blocks occasionally, and the generated rewards go to your account.

You may also group with a few friends and split the rewards between yourselves.

We maintain full nodes, as well as baking and endorsing daemons for you. Your tezos key is on a Ledger that you control. You install and run the [Tezos baking app]("https://github.com/obsidiansystems/ledger-app-tezos") and connect it to the signer. When it is your turn to bake/endorse, our infrastructure will send a signing request to your signer.

**The signer** is a Raspberry Pi with battery backup, an alternative 4G connection, and a hot spare that you may place in a different location.

<b>You remain a full custodian of your keys throughout the whole process.</b>

<div style="padding-top:50px;" id="publicbaker"></div>

  
### Public baker

To further benefit from the baking operation, you also publish your Tezos baking address so Tezos delegators may delegate to you and set a flat fee %.

In addition to your baking address, you maintain a payout address. This payout address must be replenished frequently by you.

We run a payout bot that pays your delegates every cycle from the payout address.

We run a website publication mechanism so your delegates can check their contribution and their most recent payouts just by entering their address on your website.

<b>You remain a full custodian of your keys throughout the whole process.</b>