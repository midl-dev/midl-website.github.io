## The team

### Nicolas Ochem - founder

Nicolas has 10 years experience managing cloud and on-prem infrastructure, and was most recently working at Rigetti Computing, a quantum computing company.

[LinkedIn Profile](https://www.linkedin.com/in/nicolasochem/)

### Oksana Protsukha - founder

Oksana has 10 year experience in the fintech industry and was most recently working at Tesla.

[LinkedIn Profile](https://www.linkedin.com/in/oksanaprotsukha/)

## Our experience

We have 10 years of building and managing reliable systems, and one year of experience baking Tezos with [Hodl.farm](https://hodl.farm). All our infrastructure is [open-source](https://github.com/hodl-dot-farm) and auditable.

Our approach is centered on two Fundamental Truths:

* the most reliable blockchain nodes run in the cloud. Cloud providers invest considerable amounts of time, money and brainpower on keeping the operations up. A home setup does not even come close to competing.
* not your keys, not your $FAVOURITE_TOKEN. While the cloud is great, do not put your keys in there ! The only acceptable storage for your key is a Hardware Security Module under your full, exclusive control.

Our own validator is the canonical deployment for the staking infrastructure. When rolling out new code, we always push it first to Hodl.farm before pushing it to our customer's infrastructure.

## Our method

A digital currency has many moving parts, but a core process is cryptographic signing.

The signing process is simple. Is it also the most critical in terms of operational security. Your keys need to be on a hot piece of silicon that takes unsigned strings and returns signed strings. Well architected blockchain ecosystems have come up with a dedicated daemon that does just that - signing.

We conciliate the two Fundamental Truths by separating signing from everything else: the bulk of the work is done in reliable, redundant, geographically distributed nodes in a cloud platform, but the critical signing operations are done on devices that you control ! That makes us a fully non-custodial service.
