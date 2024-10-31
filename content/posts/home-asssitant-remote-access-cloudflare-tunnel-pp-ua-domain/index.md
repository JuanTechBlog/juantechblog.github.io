---
title: "How to Access Home Assistant Remotely."
description: "Step-by-step guides to get a .PP.UA domain, set up Cloudfalre as your nameserver, configure Cloudflare Tunnel, install Cloudflare Tunnel docker client and configure Home Assistant."
date: "2024-08-24"
tags: ["Home Assistant", "Cloudflare", ".PP.UA domain", "Docker", "Docker Compose"]
draft: false
ShowToc: true
cover:
    image: 
    alt: ""
    caption: ""
    relative: true
---

## Intro
This is the method that I use for remote access to my Home Assistant.

We take advantage of the free Cloudflare Tunnel feature to connect our local service—Home Assistant without expose our external IP.

The diagram below from [Cloudflare](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/) shows how the Cloudflare Tunnel works:

![How an HTTP request reaches a private application connected with Cloudflare Tunnel](https://developers.cloudflare.com/_astro/handshake.eh3a-Ml1_ZvgY0m.webp)

We will go through the steps to register a domain, switch the domain's nameserver to Cloudflare, set up the Cloudflare Tunnel, install the cloudflared client using Docker Compose, and configure Home Assistant

### :stop_sign: Disclaimer

Before proceed, I think you should know the risk. 

Register a .PP.UA will expose your information when someone look up on the whois record. I recommand to use fake name, home address and temporary email. But they need a functional phone number for verification. We can use a virtual phone number for that. It's quite hard to get a virtual phone number in Malaysia. 

Also, we need to bind our credit/debit card with it. I suggest using a virtual credit/debit card for that.


## Get a Domain from nic.au








### c