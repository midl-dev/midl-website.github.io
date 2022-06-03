---
layout: default
title: MIDL.dev - Tezos calculation
permalink: /tezos/figures/
---

# Calculation of rewards when baking with MIDL.dev

{% include _cryptocurrencies/tezos_table.md %}

Tezos Network has [at most 5.51%](https://tezos.gitlab.io/whitedoc/proof_of_stake.html?highlight=inflation#inflation) inflation. Because not everyone is online all the time, the true inflation value is lower. For this calculation, we assume 5% actual inflation.

When you bake on your own, this is what you make - 5% annually.

When leaving your XTZ on an exchange, you pay a 25% fee. So you make 3.75% annually.

When you become a public baker, your bond of 10,000 XTZ allows you to get at most 90,000 XTZ delegated to you.

We are making the assumption that:

* 70,000 XTZ are delegated to you
* you charge a 10% fee

Annually, you collect 5% of this 70,000 XTZ, and keep 10% of that amount, so you collect 0.5%, wihch is 3,500 XTZ in the first year - 3.5% of your balance. In addition to the 5% you make by solo baking, your assets grow by 8.5% annually.

Note that this assumes that you are able to collect delegations for your public baking service. This is your responsibility, and the actual amount delegated to you may be lower.
