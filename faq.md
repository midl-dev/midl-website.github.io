---
layout: default
title: Midl.dev - Frequently asked questions
---

## Frequently asked questions

**Q: If many staking nodes share the same infrastructure, does that constitute a centralization risk ?**

A: All our customer nodes are deployed on separate accounts and we do not perform automated operations across several of them at once to reduce the risk of impacting the network.

**Q: Raspberry Pis are so inexpensive. Are they reliable ? Aren't they toys ?**

A: These credit-card sized computers are mass produced from reliable chip vendors, and have tiny requirements in terms of power and cooling. So they are in fact more reliable than traditional server blades, and can survive in the toughest conditions.

**Q: Is staking in the cloud a centralization risk ?**

A: We are running nodes in the cloud because it is more reliable than on-premises solutions. When a lot of stakers are hosting their nodes in a single cloud provider, downtime of the provider impacts the network. However, we are leveraging kubernetes which is a cloud-agnostic solution, so we are able to leverage multi-cloud when needed to mitigate that risk.

**Q: Do you support my favourite cryptocurrency ? Do you support other hardware security modules ?**

A: Please get in touch.

**Q: We do not want our staking infrastructure in a public cloud. Will you support my private cloud/my on-prem infrastructure ?**

A: Please get in touch.

**Q: Can you steal my money ?**

A: No. We do have remote access to the signer device to perform occasional upgrades, but the signer device does not have access to the keys. The keys exist only on the Ledger (that you control) and on the paper backup mnemonic which you should take precious good care of. All we can do is sign specific messages to participate in consensus.

**Q: I keep the signers at home. Do you have remote access to my home network ?**

A: We do not need access to your home network. We can guide you through configuring your home network to segregate the signers in their own VLAN so they can not access the rest of your network.

**Q: What does MIDL stand for ?**

A: Managed Infrastructure for Distributed Ledgers
