## Counter on Celo Sepolia

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

### Deployed Smart Contract Link: 004e637d997edcd42c1164c5f8d3e87630e75219393cf9f0171b79c904586a58

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


