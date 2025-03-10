---
title: "PrivatePOAP"
date: 2021-09-18
author: "Shouvik Gosh, Tobias Krug, Tobias Rothmann, Marc Sinner, Valentin Hartig"
description: "SuiSeal: Your Solution to Combat Counterfeits"
---

## Concept
[POAPs](https://poap.xyz) are a trend that gained large traction in the last couple of years of the crypto scene developments. These days, many events and booths on events allow visitors to mint a POAP in recognition of their presence. While that motivates people to move around and collect those NFTs, it also results in privacy related problems.

Overall, we see three dimensions of potential issues:
1. Link of identity and location based on people's Ethereum wallet address - possibly linked with ENS, UD or Twitter - and POAPs that indicate where they were at a certain point.
1. Link of relationships, based on POAPs' timestamp property, which allows to determine the likelihood of people to have a real-life relationship
1. Learning and forging profiles of identities based on POAP collection analytics and dusting attacks on publicly known Ethereum wallet addresses

## Design
The Private POAP PoC implements a four-step user-flow:
1. Initialize a HD wallet based on the BIP39 standard
1. Derive wallets by incrementing the Path property; determine empty Ethereum wallets with a POAP count of 0
   - [Dune Query](https://dune.com/queries/1279140)
1. Mint POAP via POAP API
   - [Claim GET](https://documentation.poap.tech/reference/getactionsclaim-qr-2) and [Claim POST](https://documentation.poap.tech/reference/postactionsclaim-qr-2)
1. Display POAP Collection based on used Ethereum wallet list
   - [Dune Query](https://dune.com/queries/1279140)

**Built with ❤ by**

<img style="width: 158px; height: 79px;" src="tbc-logo.png" />
