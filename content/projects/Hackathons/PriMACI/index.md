---
title: "PriMACI"
date: 2024-05-26
author: "Tobias Rothmann, Aleksandre Kandelaki"
description: "The coordinator of MACI in a Multi-Party Computation (MPC) setting"
---

# MP-SPDZ protocol for PriMaci

Implemented the [coordinator](https://maci.pse.dev/docs/core-concepts/coordinator-processing) of [MACI](https://maci.pse.dev/docs/introduction) in a Multi-Party Computation (MPC) setting.

We run the coordinator as a multi-party computation. 
The coordinator's task is essentially to decrypt all valid votes, sum them up, and reveal the result without revealing the individual votes.
Therefore we implement the cryptographic primitives used by the coordinator in an MPC circuit. 

Firstly, we implement the [BabyJubJub](https://iden3-docs.readthedocs.io/en/latest/_downloads/33717d75ab84e11313cc0d8a090b636f/Baby-Jubjub.pdf) Elliptic Curve over which MACI conducts the cryptography.
Secondly, we implement an extension of the [Poseidon Hash function](https://eprint.iacr.org/2019/458.pdf), namely the [Poseidon Encryption Scheme](https://maci.pse.dev/docs/core-concepts/hashing-and-encryption), that is used by MACI for vote encryption (we implement only the decryption function in the MPC circuit, as we do not need encryption within the circuit).