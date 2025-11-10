# Distributed ECDSA Signing – Contributions by Hava Haviv

This repository is a fork of [Emmanuel Meloul's fork of Bitcoin Core](https://github.com/Emelloul98/bitcoin) that includes my contributions to a **distributed threshold ECDSA signing system**.

> ⚠️ Note: The commits I made are visible in Emmanuel's repository. This fork mainly serves to showcase my work and contributions.

## Overview

I contributed code that enables **secure, collaborative signing** using **t-of-n threshold signatures** and **Shamir’s Secret Sharing**, integrated into Bitcoin Core's RPC interface.

## Features

- **Threshold ECDSA Signing** – Secure t-of-n partial signatures.  
- **Bitcoin Core Integration** – Works in `regtest` mode for testing transaction signing and broadcasting.  
- **Distributed Storage Simulation** – SQLite-based distributed key storage.  
- **PyQt5 UI** – Wallet selection, participant checkboxes, transaction creation, real-time logging.  
- **Configurable Thresholds** – Set t-of-n signing dynamically in the UI.

## Key Contributions

- **RPC Commands for Threshold Signing**:
  - `setsigninggroup`: set participant ports for the signing group.
  - `setthreshold`: define t-of-n threshold values.
  - `reconstructsecret`: reconstruct the distributed private key from participant shares.

- **DistributedSigner Module**:
  - Generates polynomial coefficients for secret sharing.
  - Sends and retrieves partial secrets to/from participants.
  - Aggregates partial signatures into a full ECDSA signature.
  - Ensures reconstructed secrets match the public key.
  - Robust logging and input validation.

## References

For the full history of my commits and the original codebase, see [Emmanuel Meloul's repository](https://github.com/Emelloul98/bitcoin).
