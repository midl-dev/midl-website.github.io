---
layout: default
img: signing-kit.jpeg
category: Services
title: MIDL.dev - The signing kit
permalink: /noncustodial-validator/
description: |
---
# The signing kit

<div style="padding-top:15px;"><img src="/img/services/signing-kit_bw.jpeg"/></div>-->

## Non-custodial service provider

At MIDL.dev, we help you stake your cryptocurrency. We are a non-custodial staking-as-a-service company, which means that you hold your keys.  
  
<span style="color:#fb9300"><b>We will never ask you for your keys.</b></span>

## How it works

A couple of Ledgers sharing the same secret seed are connected to a couple of Raspberry Pis. They are not too needy - they just need power and Internet most of the time. A battery and 4G connection is ready to take over when power and/on Internet connectivity fail. And they are fully redundant - if one fails, the other one takes over.

The signing operations are simple enough that the physical setup remains relatively low maintenance. You may have to upgrade the firmware on the Ledger once in a while, but that is it. Everything else, including protocol upgrades, is handled by us.

We ship you the signing computers, batteries and 4G-LTE dongles. Plug them in your closet, hidden behind the wi-fi router, or in a skunkworks collocation somewhere. They do not have to be in the same place either. For increased reliability, you may geographically distribute them.

When turned on, the devices securely establish a connection to our infrastructure. When your turn comes, an message is tunneled to the signer, which signs it. It is then sent back for our infrastructure to broadcast it to the network.

The signers themselves are being monitored, so if they ever loose power or Internet, you can expect a phone call from us.

The signer operating system is [fully open source and auditable](https://github.com/midl-dev/tezos-remote-signer-os).

## Optional - set up your own

Our remote signers are best-in-class - reliable, redundant, and secure. But if you want to set up your own, we can assist !

## Interested ?

Contact us at [hello@midl.dev](mailto:hello@midl.dev) to learn how we can help you stake your cryptocurrency, or just use the chat window below.
