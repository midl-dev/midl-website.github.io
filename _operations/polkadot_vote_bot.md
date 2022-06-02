---
layout: default
img: Polkadot_logo.png
status: Available now
category: Services
title: Midl.dev - Polkadot/Kusama Vote Bot
subTitle: Automated governance votes for your validator.
staker: 
short_title: 
crypto_name: Polkadot
permalink: /polkadot-vote-bot/
description: | 
---

<h2>Polkadot and Kusama Vote Bot by MIDL.dev</h2>
<h3>Onboard your validator for automated referenda votes</h3>
<p>Polkadot and Kusama use on-chain <a href="https://polkassembly.io" target="_blank">governance</a> and validators and nominators alike are expected to regularly vote in referenda put forth by the council. But it can be tedious to constantly watch for them.</p>
<p>Our service relieves you of the task of regularly logging in to the Polkadot/Kusama UI to vote in outstanding referenda.</p>
<p>Our votes are <a href="https://github.com/midl-dev/dotsama-votes" target="_blank">publicly documented</a> and you can always override them if you disagree.</p>
<p>We also provide an <a href="/polkadot-automated-payouts"> automated payout service</a> for your validator.</p>

<h4>Subscribe to automated governance votes for your Kusama validator for US$14.99 per month</h4>
<p>First, register our vote bot as governance proxy for your account. Its address is 
<a href="https://kusama.subscan.io/account/HhhJ5buaF8ZWSMBBSG2AmjY66caSomrzJyFH4CZkGoWNyYc" target="_blank"><code>HhhJ5buaF8ZWSMBBSG2AmjY66caSomrzJyFH4CZkGoWNyYc</code></a>. Then subscribe to the automated service.</p>
{% include _cryptocurrencies/kusama_votebot_table.md %}
<h4>Subscribe to automated governance votes for your Polkadot validator for US$29.99 per month</h4>
<p>First, register our vote bot as governance proxy for your account. Its address is <a href="https://polkadot.subscan.io/account/1LP7WM89gNvGqYwQKyf7W8nLssZDr447SNG2KFSze9zKZwh" target="_blank"><code>1LP7WM89gNvGqYwQKyf7W8nLssZDr447SNG2KFSze9zKZwh</code></a>. Then subscribe to the automated service.</p>
{% include _cryptocurrencies/polkadot_votebot_table.md %}

<h3>Frequently asked questions</h3>
<h4>Who is this service for?</h4>
<ul><li><b>Validators</b> who want to show good stewardship of the ecosystem to attract nominations,</li>
<li><b>Nominators</b> who want to actively contribute in governance.</li>
</ul>
<h4>Is it safe?</h4>
<p>In order for us to vote on your behalf, you need to give us the power to do so. Polkadot/Kusama has a concept of proxy accounts. You need to configure our vote bot as your Governance proxy.</p>
<p>This is a perfectly safe thing to do: the protocol ensures that you delegate voting rights to us and nothing else. Specifically we are not able to transfer any balance out of the account.</p>
<h4>How to set up a Governance proxy?</h4>
<p><b>Step 1:</b> In the "Developer/Extrinsics" page of the Polkadot-JS UI, select your validator and submit the extrinsic "proxy/addProxy()":</p>
<p><img src="/img/services/votebot/00.png" width="600px"/></p>
<p><b>Step 2:</b> Copy MIDL.dev vote bot address above in the "delegate" field and select "Governance" as proxy type, "0" as delay. Validate. Approve on your Ledger device (you need it connected).</p>
<p><img src="/img/services/votebot/01.png" width="600px"/></p>
<p>Be careful! Only configure our address as Governance proxy and nothing else. If you give us too many proxy powers, we will get in touch to remediate this.</p>
<p><b>Step 3:</b> Verify that the blue Proxy icon appears on the left.</p>
<p><img src="/img/services/votebot/02.png" width="600px"/></p>
<h4>What service level do you offer?</h4>
<p>We will vote for every referendum before it ends. This or your money back!</p>
<h4>How do you decide what to vote?</h4>
<p>We have good technical knowledge of the ecosystem and have made several meaningful contributions to it. We stay informed about the evolution of the Polkadot and Kusama chains and vote for what we believe will bring a better outcome for the ecosystem and maximize their long-term value.</p>
<p><a href="https://github.com/midl-dev/dotsama-votes" target="_blank">We document our votes</a> in a public Github repository. Our bot only votes for a given referendum if your account has not voted yet. If you disagree with us, you can always override by voting without the proxy.</p>
<h4>How do I unsubscribe from the vote bot service?</h4>
<p>Send an email to <a href="mailto:hello@midl.dev">hello@midl.dev</a>.</p>
<h4>What are the terms and conditions?</h4>
<p>Unless required by applicable law or agreed to in writing, MIDLDEV OÜ provides a service on an “AS IS” BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied, including, without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A PARTICULAR PURPOSE. You are solely responsible for determining the appropriateness of using our services.</p>
