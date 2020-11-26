---
layout: post
title: Ethereum 2.0 Remote Signing with MIDL.dev
date:  2020-11-25 07:00:00 +0800
category: 
tag: Ethereum
---

This is part 2 of the Ethereum 2.0 [key management post](https://midl.dev/2020/11/16/eth-2-key-management/)

### Remote signer powered by MIDL.dev

When you opt to running a remote signer, you keep complete control of your validation key. For this reason, you must spin up a virtual machine with the remote signer on a cloud platform that you fully control yourself. Not to worry, our solution makes it simple to do so.

Our remote signer solution is a [Digital Ocean Basic Droplet](https://www.digitalocean.com/pricing/) costing $10/mo.

When you are ready, we give you a shell command to deploy a Digital Ocean VM with [custom user-data](https://www.digitalocean.com/blog/automating-application-deployments-with-user-data/). The VM comes online and automatically sets itself up as a remote signer.

Your public and private validation keys are passed to the virtual machine as environment variables. We give you instructions to extract these keys from your validator keystore that you generated during onboarding.

The Droplet is configured with a [Cloud Firewall](https://www.digitalocean.com/docs/networking/firewalls/how-to/manage-droplets/) to only accept inbound signing connections and ssh connections using a key pair. It has a [static IP address](https://www.digitalocean.com/community/questions/will-my-droplet-have-a-static-ip).

The connection from the validator setup to the remote signer is TLS encrypted and the firewall is additionall restricted to the IP range of the validator setup for additional security.

MIDL.dev monitoring infrastructure verifies that the signer is operational by periodically sending HTTP keepalives and sends a Slack message to the operator if there is an issue with the signing VM.

The remote signer runtime is based on the [remote-signer-ts project from EthPOS](https://github.com/ethpos/remote-signer-ts). It supports any number of keys.

If the VM needs to be upgraded to support additional keys or a new version of the sofware, the same procedure can be applied again, in coordination with MIDL.dev in case the IP address of the virtual machine changes.
