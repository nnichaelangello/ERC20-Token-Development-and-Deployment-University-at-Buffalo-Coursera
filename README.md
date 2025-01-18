# ERC-20 Token Development and Deployment

## Overview
This project is part of the **Programming Assignment: Tokens and Tokenization** course offered by the University at Buffalo. The goal of this project is to develop, deploy, and interact with an ERC-20 token on the Ethereum blockchain. ERC-20 is a standard for creating fungible tokens on the Ethereum network, widely used for cryptocurrencies, utility tokens, and more.

This repository contains the Solidity smart contract code for the ERC-20 token, along with instructions for deploying and interacting with the token using Remix IDE and the Sepolia Testnet.

---

## Table of Contents
1. [What is ERC-20?](#what-is-erc-20)
2. [Project Objectives](#project-objectives)
3. [Features of the ERC-20 Token](#features-of-the-erc-20-token)
4. [Technologies Used](#technologies-used)
5. [Steps to Deploy and Interact with the Token](#steps-to-deploy-and-interact-with-the-token)
6. [Simulation Output](#simulation-output)
   - [Contract Deployment](#contract-deployment)
   - [Checking Token Balance](#checking-token-balance)
   - [Transferring Tokens](#transferring-tokens)
   - [Minting New Tokens](#minting-new-tokens)
   - [Querying Token Details](#querying-token-details)
7. [Key Learnings](#key-learnings)
8. [Resources](#resources)

---

## What is ERC-20?
ERC-20 is a technical standard used for creating and issuing smart contracts on the Ethereum blockchain. It defines a set of rules that Ethereum-based tokens must follow, ensuring compatibility across the ecosystem. These rules include:
- Transferring tokens from one account to another.
- Getting the current token balance of an account.
- Approving and spending tokens on behalf of another account.

ERC-20 tokens are widely used for:
- Cryptocurrencies (e.g., stablecoins like USDT).
- Utility tokens (e.g., access to a platform or service).
- Governance tokens (e.g., voting rights in decentralized organizations).

---

## Project Objectives
The main objectives of this project are:
1. **Understand the ERC-20 Standard**: Learn the core functions and events defined by the ERC-20 standard.
2. **Develop a Custom ERC-20 Token**: Write a Solidity smart contract that implements the ERC-20 standard.
3. **Deploy the Token on Sepolia Testnet**: Use Remix IDE and Metamask to deploy the token on the Ethereum test network.
4. **Interact with the Token**: Test the token's functionality, including transferring tokens, checking balances, and minting new tokens.

---

## Features of the ERC-20 Token
The ERC-20 token developed in this project includes the following features:
- **Name and Symbol**: The token has a customizable name and symbol (e.g., `ERC20Token` and `ERC20`).
- **Total Supply**: The total supply of tokens is defined during deployment and can be minted further if needed.
- **Balance Tracking**: The contract tracks the balance of each address holding the token.
- **Transfer Function**: Allows users to transfer tokens to another address.
- **Approval and TransferFrom**: Enables delegated transfers, where one address can spend tokens on behalf of another.
- **Minting**: The contract owner can mint new tokens (for demonstration purposes).

---

## Technologies Used
- **Solidity**: The programming language used to write the smart contract.
- **Remix IDE**: An online development environment for writing, compiling, and deploying smart contracts.
- **Metamask**: A cryptocurrency wallet used to interact with the Ethereum blockchain.
- **Sepolia Testnet**: A test network for Ethereum, used for deploying and testing the token without using real ETH.
- **Ethereum**: The blockchain platform on which the token is deployed.

---

## Steps to Deploy and Interact with the Token

### Step 1: Set Up the Environment
1. Install [Metamask](https://metamask.io/) and create a wallet.
2. Switch to the **Sepolia Testnet** in Metamask.
3. Obtain Sepolia ETH from a faucet (e.g., [Sepolia Faucet](https://sepoliafaucet.com/)).

### Step 2: Write the Smart Contract
1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a new file named `ERC20Token.sol`.
3. Copy and paste the Solidity code provided in this repository into the file.

### Step 3: Compile the Contract
1. Go to the **Solidity Compiler** tab in Remix.
2. Select the compiler version `0.8.20`.
3. Click **Compile ERC20Token.sol**.

### Step 4: Deploy the Contract
1. Go to the **Deploy & Run Transactions** tab.
2. Select **Injected Provider - Metamask** as the environment.
3. Enter the token name, symbol, and initial supply (in Wei) in the constructor fields.
4. Click **Transact** and confirm the transaction in Metamask.

### Step 5: Interact with the Token
1. Use the deployed contract's functions in Remix to:
   - Check balances (`balanceOf`).
   - Transfer tokens (`transfer`).
   - Approve and transfer tokens on behalf of another address (`approve` and `transferFrom`).
   - Mint new tokens (`mint`).

---

## Simulation Output

### Contract Deployment
Output from deploying the ERC-20 token contract:
```
view on etherscan
[block:7519567 txIndex:13]
from: 0x76e...ab63d
to: ERC20Token.(constructor)
value: 0 wei
data: 0x608...00000
logs: 0
hash: 0x4d7...c76f3
```

---

### Checking Token Balance
Output from checking the token balance of an address:
```
call to ERC20Token.balanceOf
call
[call]
from: 0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d
to: ERC20Token.balanceOf(address)
data: 0x70a...def12
```

---

### Transferring Tokens
Output from transferring tokens to another address:
```
transact to ERC20Token.transfer pending ... 
view on etherscan
[block:7519572 txIndex:37]
from: 0x76e...ab63d
to: ERC20Token.transfer(address,uint256) 0x002...239cc
value: 0 wei
data: 0xa90...00064
logs: 1
hash: 0x89c...dd9bf
```

---

### Minting New Tokens
Output from minting new tokens:
```
transact to ERC20Token.mint pending ... 
view on etherscan
[block:7519574 txIndex:29]
from: 0x76e...ab63d
to: ERC20Token.mint(uint256) 0x002...239cc
value: 0 wei
data: 0xa07...0000a
logs: 1
hash: 0x5ab...5622e
```

---

### Querying Token Details
Output from querying token details (decimals, name, symbol, and total supply):
```
call to ERC20Token.decimals
call
[call]
from: 0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d
to: ERC20Token.decimals()
data: 0x313...ce567

call to ERC20Token.name
call
[call]
from: 0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d
to: ERC20Token.name()
data: 0x06f...dde03

call to ERC20Token.symbol
call
[call]
from: 0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d
to: ERC20Token.symbol()
data: 0x95d...89b41

call to ERC20Token.totalSupply
call
[call]
from: 0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d
to: ERC20Token.totalSupply()
data: 0x181...60ddd

from: 0x76E6d4Ca3d593eE429cFB6dD46ed75bA65bab63d
to: ERC20Token.totalSupply() 0x002f37447f6aFf59d543A7E7b2e4a57fc4B239cC
input: 0x181...60ddd
output: 00000000000000000000002111941661492392424223200
decoded input: {}
decoded output: {
    "0": "uint256: 1000010000000000000000000"
}
logs: []
raw logs: []
```

---

## Key Learnings
- **Smart Contract Development**: Gained hands-on experience in writing and deploying smart contracts using Solidity.
- **ERC-20 Standard**: Learned the core functions and events required by the ERC-20 standard.
- **Blockchain Interaction**: Understood how to interact with the Ethereum blockchain using tools like Remix IDE and Metamask.
- **Testnet Deployment**: Practiced deploying and testing smart contracts on a test network (Sepolia) without using real funds.

---

## Resources
- [Solidity Documentation](https://soliditylang.org/docs/)
- [Remix IDE](https://remix.ethereum.org/)
- [Metamask](https://metamask.io/)
- [Sepolia Faucet](https://sepoliafaucet.com/)
- [ERC-20 Token Standard](https://eips.ethereum.org/EIPS/eip-20)

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- **University at Buffalo** for providing the course materials and assignment.
- **Coursera** for hosting the course.
- **Ethereum Foundation** for developing the tools and standards used in this project.
```
