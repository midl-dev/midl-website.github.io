---
layout: post
title: Should I delegate or bake?
date:  2020-05-26 07:00:00 +0800
category: tezos
subTitle: 
permalink: /bake-or-delegate/
---

**"Should I delegate or bake?"** This is the question that all tezos token holders sooner or later ask themselves.

The answer is - it depends. Tezos protocol has been designed to reward token holders as long as they participate in the network whether actively or passively. The list of questions below can help you narrow down the solution which is the most applicable to your situation.

We assume that you are familiar with the basics of baking operation on [Tezos network](https://tezos.com/get-started/#bake-validate-basics). If not, Tezos website provides a detailed overview of the protocol. 


<b>Do I have a sufficient amount of XTZ to bake?</b>

In order to bake, one needs to hold a minimum of 1 roll of XTZ, which equates to 8000 tokens. Anything below this amount means you can only delegate. 

<b>Do I have too many XTZ, which makes it difficult to find a baker with sufficient capacity?</b>

It's a good problem to have. However, recently there have been several threads on different crypto-channels where a baker was trying to reach out to its delegate who delegated more XTZ than a baker has capacity for. Over-delegation is a real problem that bakers are grappling with. In most circumstances baking is usually a better option for token holders with a large amount of XTZ. 

<b>Do you plan to hold XTZ for a long period of time to justify setting up a baking infrastructure?</b> 

If you plan to exit the network sooner than later, it might not be worthwhile to spend time and efforts to spin off the whole infrastructure to set up a baking operation. On the other hand, if you believe in the future of the network (we certainly do) and prefer to hold the tokens for the foreseeable future, it might be wise to consider baking as an alternative to delegation.

<b>Do you have sufficient knowledge and willingness to invest your time to learn all the technical nitty-gritty of Tezos protocol and infrastructure?</b> 

If you are a nerd like we are, you might find it entertaining to spend your evenings on reading through white papers and documentation. This is only the beginning, however. Once you finally know how to set up and operate a baking operation, you need to maintain it. The protocol is actively being improved, which means ongoing upgrades and maintenance. 

<b>Do you want to take advantage of earning rather than paying delegation fees?</b>

Only a baker can become a delegator (a.k.a. a public baker) and earn rewards in terms of delegation fees. It of course depends on your staking capacity and its utilization. The more capacity you have, the more lucrative a public baker offering is. Not only you earn additional rewards, you provide a platform for smaller token holders to participate in the network. This essentially creates a positive feedback loop that drives improvements to the network. The better network performs and the more it engages the public, the higher value you can expect from your tokens.

<b>Do you want to participate in on-chain governance?</b>

As a baker you can participate in governing the protocol and ensure that you have a say in the proposed protocol amendments. 

<b>How much are you willing to spend on building a reliable infrastructure for baking?</b> 

A reliable infrastructure, such as a cloud platform, is a great solution and is exactly what we use and recommend. However, it costs money. You need to do your research and select the right cost-efficient platform for your baking operation. Additionally, baking is not a risk-free activity. Tezos protocol has built-in protection mechanism to prevent malicious activity, such as double-baking and double-endorsing. Such that a baker may have the security bond slashed for the cycle in which abnormal behavior occurred. 

<b>How much XTZ do I need for baking to be more cost-efficient than delegation?</b> 

Below are several examples that compare rewards and costs between delegation and baking. 

<i><b>Note</b>: below analysis of final rewards is based on the 10% delegation fee vs baking with MIDL.dev infrastructure solution.</i> 
<i>If you plan to set-up your own baking infrastructure, the costs will vary based on your individual setup. They will usually be higher than that of MIDL.dev.</i>
<i>Additionally, the rewards amount can be higher or smaller based on XTZ to USD exchange rate, actual delegation fee and public baker's capacity utilization.</i>

<i><b>Inflation rate</b>:Tezos Network has [at most 5.51%](https://tezos.gitlab.io/whitedoc/proof_of_stake.html?highlight=inflation#inflation) inflation. Because not everyone is online all the time, the true inflation value is lower. For this calculation, we assume 5% actual inflation.
When you bake on your own, this is what you make - 5% annually.</i>

<div style="padding-top:15px"></div>
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTQXp79GiUhXYmlc_PYcAjdf1d7eZ2cKArT7BZalg9auem-aJtNnnRuKDRWcPvkOmJuwcNk6dShcxL4/pubhtml?gid=1643664373&amp;single=true&amp;widget=false&amp;headers=false&amp;chrome=false" width="700" height="720"></iframe>

#### Delegation tips
* Select your baker platform based on its efficiency and fee structure
* Review payouts history of the baker to ensure that payouts are consistent
* Ensure your baker offers a communication/support channel
* Confirm whether a baker has sufficient staking capacity

There are a number of websites that provide a valuable metrics for public bakers:

[Tezos-nodes](https://tezos-nodes.com/)

[Baking-bad](https://baking-bad.org/)

<i>Some metrics might not be 100% accurate or apply to all bakers.
For instance, [Hodl.farm](https://hodl.farm) processes payouts in advance to give its delegates peace of mind that they will always receive their rewards. Currently, there is no payout metric that reflects this model on the rating websites.</i> 