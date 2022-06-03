---
layout: default
title: MIDL.dev - The team
---

# The team

### Nicolas Ochem - founder

Nicolas has 10 years experience managing cloud and on-prem infrastructure, and was most recently working at Rigetti Computing, a quantum computing company.

<img src="/img/midl-nico.jpeg"/>

[LinkedIn Profile](https://www.linkedin.com/in/nicolasochem/)

### Oksana Protsukha - founder

Oksana has 10 years experience in the fintech industry and was most recently working at Tesla.

<img src="/img/midl-oksana.jpeg"/>

[LinkedIn Profile](https://www.linkedin.com/in/oksanaprotsukha/)

### Chao Zhang - Engineer

Chao has 8 years experience of cloud and on-premise infra management along with software development, was most recently working at Nokia.

<img src="/img/midl-chao.jpeg"/>

[LinkedIn Profile](https://www.linkedin.com/in/chao-zhang-0326/)

### Xavier Rondé-Oustau - General Counsel

### Join us

We are always looking to grow the team. [Contact us](mailto:hello@midl.dev)

## Our experience

We have 10 years of experience building and managing reliable systems, and one year operating a Tezos baker. All our infrastructure is [open-source](https://github.com/midl-dev) and auditable.

Our approach is centered on two fundamental ideas:

* the most reliable blockchain nodes run in the cloud. Cloud providers invest considerable amounts of time, money and brainpower on keeping the operations up. A home setup does not even come close to competing.
* not your keys, not your $FAVOURITE_TOKEN. The cloud is very capable, but **do not put your keys in there!** The only acceptable storage for your key is a Hardware Security Module under your full, exclusive control.

## Our method

A digital currency has many moving parts, but a core process is cryptographic signing.

The signing process is simple. Is it also the most critical in terms of operational security. Your keys need to be on a hot piece of silicon that takes unsigned strings and returns signed strings. Well architected blockchain ecosystems have come up with a dedicated daemon that does just that - signing.

We conciliate the two fundamental ideas by separating signing from everything else: the bulk of the work is done in reliable, redundant, geographically distributed nodes in a cloud platform, but the critical signing operations are done on devices that you control. That makes us a fully non-custodial service.

We eat our own dog food. Our staking operation is the canary deployment for the staking infrastructure. When rolling out new code, we always push it first to to our baker before pushing it to our customers.
