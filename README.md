# ChainVIN

## Decentralized Vehicle Passport

ChainVIN is a decentralized application (dApp) designed to create an immutable and transparent history of vehicles using blockchain technology.

The goal of the project is to reduce fraud in the used car market by storing important vehicle records on-chain, where they cannot be secretly modified or deleted.

The application allows vehicle owners, verified service centers, and future buyers to interact with a trusted decentralized vehicle history system.

---

# Problem

The used vehicle market suffers from multiple trust-related problems:

- Mileage rollback fraud
- Hidden accidents
- Fake service history
- Manipulated ownership records
- Centralized databases that can be altered

Today buyers often rely on centralized services or the honesty of sellers. Important records may be missing, manipulated, or inaccessible.

ChainVIN solves this problem by using blockchain technology to create permanent and verifiable vehicle records.

---

# Solution

ChainVIN provides a decentralized vehicle passport where:

- Vehicle owners can register vehicles
- Verified service centers can add maintenance and inspection records
- Vehicle ownership transfers are stored on-chain
- Buyers can verify vehicle history transparently
- Suspicious mileage rollback attempts are automatically detected

Each important event in the lifecycle of a vehicle becomes immutable and publicly verifiable.

---

# Features

## Vehicle Registration
Vehicle owners can register a vehicle on-chain using a VIN hash.

## Verified Service Centers
Only approved and verified service centers can create official service records.

## Service History
Maintenance, inspections, mileage updates, and accident records are permanently stored on the blockchain.

## Ownership Transfers
Vehicle ownership changes are recorded transparently.

## Mileage Fraud Detection
The smart contract automatically detects suspicious mileage decreases that may indicate odometer fraud.

## Evidence Storage
IPFS hashes can be attached to service records for:
- repair documents
- inspection reports
- accident evidence
- dashcam footage

---

# Architecture Overview

The project consists of:

## Smart Contracts
Written in Solidity and deployed on an EVM-compatible blockchain.

Responsibilities:
- vehicle registry
- access control
- service verification
- ownership management
- fraud detection
- immutable record storage

## Frontend Application
A React-based web application connected to MetaMask.

Users can:
- connect wallets
- register vehicles
- view vehicle history
- add service records
- transfer ownership

## Storage
Sensitive or large files are stored off-chain using IPFS, while their hashes are stored on-chain for integrity verification.

---

# Technology Stack

## Blockchain
- Solidity
- Hardhat
- OpenZeppelin

## Frontend
- React
- TailwindCSS
- wagmi
- ethers.js

## Storage
- IPFS

## Network
- Base Sepolia Testnet

---

# Smart Contract Overview

The smart contract manages:

- vehicle registration
- service center verification
- service record creation
- vehicle ownership transfers
- suspicious mileage detection

Important entities:

## Vehicle
Stores:
- VIN hash
- model
- year
- current owner
- last known mileage

## ServiceRecord
Stores:
- record type
- mileage
- timestamp
- service center
- IPFS/document hash
- suspicious status

---

# Security Considerations

The project implements multiple security mechanisms:

- Access control using verified service centers
- Ownership validation
- Immutable service history
- Fraud detection logic
- Restricted administrative actions

OpenZeppelin's Ownable contract is used for admin permissions.

---

# Example Workflow

1. Vehicle owner registers a car
2. Admin verifies service centers
3. Service center adds maintenance records
4. Vehicle ownership can be transferred
5. Buyers can inspect full transparent history

---

# Why Blockchain?

Blockchain is used because vehicle history requires:

- immutability
- transparency
- tamper resistance
- decentralized trust
- verifiable ownership history

A centralized database could be modified or manipulated, while blockchain guarantees integrity of records.

---

# Future Improvements

Possible future extensions include:

- decentralized insurance integration
- NFT-based ownership certificates
- service center reputation system
- EV battery health tracking
- DAO governance for service verification
- integration with IoT vehicle devices
- decentralized vehicle marketplace

---

# Testing

The project includes unit tests for:

- vehicle registration
- duplicate VIN prevention
- service center verification
- service record creation
- unauthorized access rejection
- ownership transfers
- mileage rollback detection

---

# AI Usage

Generative AI tools such as ChatGPT were used during:
- brainstorming
- architecture planning
- smart contract development
- frontend planning
- documentation writing

All code and design decisions were reviewed and understood by the authors.

---

# What We Learned

During development we learned:
- Solidity smart contract development
- blockchain architecture design
- decentralized application workflows
- smart contract testing
- wallet integration
- blockchain-based access control
- decentralized trust mechanisms

---

# Conclusion

ChainVIN demonstrates how blockchain technology can solve real-world trust problems in the automotive market.

By creating a decentralized and immutable vehicle passport, the project improves transparency, reduces fraud, and provides buyers with trustworthy vehicle history information.

The project combines practical usefulness with decentralized architecture and shows how blockchain can be applied beyond cryptocurrencies and speculative applications.
