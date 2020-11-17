---
layout: post
title: Ethereum 2.0 Key management
date:  2020-10-17 07:00:00 +0800
category: 
tag: Ethereum
---

After you send your Ethereum 2.0 tokens to the Deposit Contract, you will take possession of two cryptographic keys:

* the withdrawal key or "seed" consists of 12 english words and should be stored offline, written down on paper,
* the validation key, necessary to stake and participate in consensus.

So, when you are using the [Ethereum 2.0 staking service from MIDL.dev](/ethereum), how does cryptographic signature of the validation messages work?

The withdrawal key or "seed" remains yours and yours alone. This key will allow you to withdraw your Eth2 funds once transfers are enabled. As a non-custodial staking provider, we do not need this key and will never ask you for it.

As for the valiadtion key, there are two solutions, and it is basically up to you on which one you feel comfortable with.

## Validation key handoff

This is the simplest solution, suitable for validators who want peace of mind and a fully managed solution.

* you hand us off the validation key using a secure channel, it is kept in our infrastructure using security best practices
* we validate for you
* in a later phase of Ethereum 2.0 rollout, transfers are enabled. At this point, you are able to transfer funds and rotate the keys.

In our opinion, this is non-custodial since the withdrawal key remains in your possession. Only this key allows you to eventually move assets to a different address.

### Handoff risks

Validation key handoff may not be the choice solution for everyone. 

During phase zero, the protocol does not support rotation of the validation key attached to a withdrawal key, much to our regret. Therefore, by handing off your validation keys to someone, you expose yourself to the following risks:

* if you engage with several different staking providers during phase zero, and hand off your keys to both, you need to coordinate to ensure that both are not validating at the same time, which is a protocol offense that may result in loss of funds
* the provider may accidentally perform a voluntary exit from the validator set. This is an irreversible operation and will prevent you from earning more rewards until transfers are enabled.

We mitigate these risks by:

* performing due diligence to ensure proper validation operation
* contractually committing to destroying our copy of the validation key upon termination of our engagement with you

## Remote signer powered by MIDL.dev

If you would rather keep the validation key under your full exclusive control, we have a solution.

We assist you in setting up a virtual machine acting as remote signer in a cloud provider. This virtual machine is in your full control, in a cloud provider for which only you have the credentials.

Our infrastructure operates full nodes and validators. When it is your turn to validate, we send a signing request to your virtual machine using a secure channel. The virtual machine replies with the signed message. During this process, the validation key never leaves the virtual machine.

Our virtual machine base image comes with the software preinstalled, all you have to do is spin it up and inject your key. This is a simple process that requires minimal knowledge of command line interface.

The advantages of this approach are twofold:

* you retain the capability to grant or revoke access to the signing VM
* your VM will only sign operations needed for validation. It will refuse to sign anything else (i.e. voluntary exit)

### Remote signer risks

The remote signer is under your full and exclusive control. If it goes offline for any reason, we are unable to validate for you.

Also, running a VM in a cloud provider incurs additional cost. You are responsible for handling timely payments to the cloud provider.

## Conclusion

Ethereum 2.0 is an experimenal protocol. It will mature over time: key rotation will be enabled, and hardware security module support will be added. For the time being, we will be working with you to better suit your expertise and comfort.

**Validation key handoff** is a good solution if you want peace of mind and are willing to work with us until the network matures.

**Remote signer powered by MIDL.dev** is great if you want to retain full control over both your keys while still enjoying a quality of service only attainable with a dedicated staking infrastructure company.

We are a boutique validation service and we will be diligently working with you to set up a staking solution that suits your needs.
