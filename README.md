## Counter on Celo Sepolia

<img width="1470" height="956" alt="Screenshot 2025-10-29 at 1 53 12 PM" src="https://github.com/user-attachments/assets/65d7c5a1-190f-456a-8e0f-0801b9faf5da" />


### Project Description
This repository contains a simple, production-ready setup for deploying a Solidity smart contract (a basic Counter) to the Celo Sepolia testnet using Hardhat. It’s tailored to be beginner-friendly while keeping a clean structure for real-world use.

### What it does
The contract exposes a minimal on-chain counter with functions to increment, decrement (with a safety check so it never goes below zero), and read the current count. The included Hardhat scripts compile and deploy the contract to the Celo Sepolia network.

### Features
- Simple `Counter` smart contract
- Hardhat configuration for Celo Sepolia
- One-command deployment script
- Environment-variable driven private key and RPC management
- Clean project structure suitable for extension

### Deployed Smart Contract Link: https://celo-sepolia.blockscout.com/address/0x521928d722209AEDE2B2518FA98D7b467Dc52f89

### Use this code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract Counter {
    uint256 public count;

    function increment() public {
        count += 1;
    }

    function decrement() public {
        require(count > 0, "Count cannot be less than zero");
        count -= 1;
    }

    function getCount() public view returns (uint256) {
        return count;
    }
}

---

If you find this helpful, consider starring the repo and extending the contract or scripts to suit your needs (e.g., verification, CI/CD, or a frontend dapp). Happy building on Celo!


# Celo-Contract
