# gramfi-web3-authenticator
Technical documentation and design for the GramFi Web3 Authenticator and authorization system on BNB Smart Chain.

# GramFi Web3 Authenticator

This repository contains the technical design and architecture documentation for the **GramFi Web3 Authenticator**, a device-based authorization system for ERC-20 and native token transfers on **BNB Smart Chain**.

## Overview

The GramFi Web3 Authenticator is designed to provide secure, time-bound authorization for on-chain actions without requiring users or developers to manage complex wallet or signing infrastructure. The authenticator runs on the user’s own device and acts as a cryptographic approval layer for sensitive actions such as token transfers, approvals, and authentication events.

This system is intended to be developer-friendly infrastructure that can be integrated into Web3 and hybrid Web2/Web3 applications.

## Core Components

- **Web3 Authenticator Application**
  - Runs on a user-controlled device (mobile phone, wearable, tablet)
  - Generates cryptographic approvals for ERC-20 and native BNB transfers
  - Supports time-bound and intent-specific authorization

- **Authorization Request Flow**
  - Applications generate a transfer or action request
  - Requests are routed to the user’s authenticator
  - The user explicitly approves or rejects the request
  - Approved requests produce a signed payload for on-chain submission

- **BNB Smart Chain Integration**
  - Native BNB transfers
  - ERC-20 token transfers, including Binance-Peg USDC
  - Non-custodial by design

- **NFC / QR Identifier Support (Planned)**
  - Physical cards or QR codes act only as identifiers
  - No private keys or signing material stored on cards
  - All authorization occurs through the Web3 Authenticator

## Security Model

- Private keys remain on the user’s device
- No custodial components
- Explicit user approval required for every action
- Time-bound approvals reduce replay risk

## Status

This documentation is an active work in progress and will be expanded during the BNB Chain grant evaluation phase to include detailed flows, threat modeling, and implementation milestones.

## Related Project

- **GramFi.io** — Non-custodial Web3 wallet and payments application
