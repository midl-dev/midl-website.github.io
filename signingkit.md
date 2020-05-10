---
layout: default
title: Midl.dev - The signing kit
---

At MIDL.dev, we help you stake your cryptocurrency. We are a non-custodial staking-as-a-service company, which means that you hold your keys. Here is how it works.

# The signing kit

A couple of Ledgers sharing the same secret seed are connected to a couple of Raspberry Pis. They are not too needy - they just need power and Internet most of the time. A battery and 4G connection is ready to take over when power and/on Internet connectivity fail. And they are fully redundant - if one fails, the other one takes over.

The signing operations are simple enough that the physical setup remains relatively low maintenance. You may have to upgrade the firmware on the Ledger once in a while, but that is it. Everything else, including protocol upgrades, is handled by us.

We ship you the signing computers, batteries and 4G-LTE dongles. Plug them in your closet, hidden behind the wi-fi router, or in a skunkworks collocation somewhere. They do not have to be in the same place either. For increased reliability, you may geographically distribute them.

When turned on, the devices securely establish a connection to our infrastructure. When your turn comes, an message is tunneled to the signer, which signs it. It is then sent back for our infrastructure to broadcast it to the network.

The signers themselves are being monitored, so if they ever loose power or Internet, you can expect a phone call from us.

The signer operating system is [fully open source and auditable](https://github.com/hodl-dot-farm/tezos-remote-signer-os).

## Interested ?

Contact us at [hello@midl.dev](mailto:hello@midl.dev) to learn how we can help you stake your cryptocurrency, or just use the chat window below.
