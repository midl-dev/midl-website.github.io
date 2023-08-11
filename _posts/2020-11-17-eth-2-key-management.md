---
layout: post
title: Ethereum 2.0 Key management with MIDL.dev
date:  2020-11-17 07:00:00 +0800
category: 
tag: Ethereum
---

After you send your Eth1 tokens to the Deposit Contract, you will take possession of two cryptographic keys:

* the withdrawal key or "seed" consists of 24 english words and it should be stored offline, written down on paper,
* the validation key, necessary to stake and participate in consensus.

## Withdrawal key

When using the [Ethereum 2.0 staking service from MIDL.dev](/ethereum/), the withdrawal key or “seed” remains yours and yours alone. Withdrawal key will allow you to withdraw or transfer your Eth2 funds once transfers are enabled. As a non-custodial staking provider, we do not need this key and will never ask you for it.

## Validation key

Validation key is required to participate in the network validation activities. This key does not have access to withdraw or transfer your funds. 

There are two solutions to manage validation key. You can choose the one you are most comfortable with.

### Solution 1 - Validation key handoff

This is the simplest solution, suitable for validators who want peace of mind and a fully managed solution.

* you hand us off the validation key using a secure channel (such as Signal expiring messages);
* it is kept in our infrastructure using security best practices (Kubernetes Secrets, 2-factor authentication);
* we validate for you;
* in a later phase of Ethereum 2.0 rollout, transfers are enabled. At this point, you are able to transfer funds and rotate the keys.

This is a non-custodial service: the withdrawal key remains in your possession. Only this key allows you to eventually withdraw or transfer assets to a different address.

<h3><i class="fa fa-exclamation" aria-hidden="true" style="color:#FB9300"></i> Handoff risks</h3>

Validation key handoff may not be the choice solution for everyone. 

During phase zero, the protocol does not support rotation of the validation key attached to a withdrawal key, much to our regret. Therefore, by handing off your validation key(s) to someone, you expose yourself to the following risks:

* if you engage with several different staking providers during phase zero, and hand off your keys to both, you need to coordinate to ensure that both are not validating at the same time. Double validation is a protocol offense that may result in loss of funds.
* anyone in possession of the validation key may perform a voluntary exit from the validator set. This is an irreversible operation and will prevent you from earning more rewards until transfers are enabled.

We mitigate these risks by:

* running reliable, secure, always-on staking infrastructure;
* contractually committing to destroying our copy of the validation key(s) upon termination of our engagement with you.

### Solution 2 - Remote signer powered by MIDL.dev

If you would rather keep the validation key under your exclusive control, we have a solution.

We assist you in setting up a virtual machine acting as remote signer in a cloud provider. This virtual machine is in your full control, in a cloud provider for which only you have the credentials.

Our infrastructure operates full nodes and validators. When it is your turn to validate, we send a signing request to your virtual machine using a secure channel. The virtual machine replies with the signed message. During this process, the validation key never leaves your virtual machine.

Our virtual machine base image comes with the software preinstalled, all you have to do is spin it up and inject your key. This is a simple process that requires minimal knowledge of command line interface.

The advantages of this approach are twofold:

* you retain the capability to grant or revoke access to the signing VM
* your VM will only accept sign operations needed for validation. It will refuse to sign anything else (i.e. voluntary exit)

<h3><i class="fa fa-exclamation" aria-hidden="true" style="color:#FB9300"></i> Remote signer risks</h3>

The remote signer is under your full and exclusive control. If it goes offline for any reason, we are unable to validate for you.

Also, running a VM in a cloud provider incurs additional cost. You are responsible for handling timely payments to the cloud provider.

## Conclusion

Ethereum 2.0 is an experimental protocol. It will mature over time: key rotation will be enabled, and hardware security module support will be added. For the time being, we offer two solutions, for you to pick based on your expertise and comfort level.

**Validation key handoff** is a good solution if you want peace of mind and are willing to work with us until the network matures.

**Remote signer powered by MIDL.dev** is a good solution if you want to retain full control over both your keys while still enjoying a quality of service only attainable with a dedicated staking infrastructure company.

We are a boutique validation service and we will diligently work with you to set up a staking solution that suits your needs.
