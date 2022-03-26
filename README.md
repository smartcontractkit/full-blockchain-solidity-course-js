<!-- [YouTube Video](https://www.youtube.com/watch?v=M576WGiDBdQ) -->

<!-- <br/>
<p align="center">
<a href="https://www.youtube.com/watch?v=M576WGiDBdQ" target="_blank">
<img src="./img/youtube_thumbnail.jpeg" width="350" alt="Solidity, Blockchain, and Smart Contract Course – Beginner to Expert Python Tutorial">
</a>
</p>
<br/> -->

Welcome to the repository for the Ultimate Solidity, Blockchain, and Smart Contract - Beginner to Expert Full Course | Javascript Edition FreeCodeCamp course!

All code references have both a javascript and a typescript edition.

Recommended Testnet: Rinkeby
Testnet Faucets: https://faucets.chain.link

# Resources For This Course

### Questions

-   [Github Discussions](https://github.com/smartcontractkit/full-blockchain-solidity-course-py/discussions)
    -   Ask questions and chat about the course here!
-   [Stack Exchange Ethereum](https://ethereum.stackexchange.com/)
    -   Great place for asking technical questions about Ethereum
-   [StackOverflow](https://stackoverflow.com/)
    -   Great place for asking technical questions overall

# Table of Contents

- [Resources For This Course](#resources-for-this-course)
    - [Questions](#questions)
- [Table of Contents](#table-of-contents)
- [Lesson 0: Welcome To Blockchain](#lesson-0-welcome-to-blockchain)
  - [What is a Blockchain?](#what-is-a-blockchain)
  - [Making Your First Transaction](#making-your-first-transaction)
  - [How Do Blockchains Work?](#how-do-blockchains-work)
    - [Consensus](#consensus)
- [Lesson 1: Welcome to Remix! Simple Storage](#lesson-1-welcome-to-remix-simple-storage)
    - [Everything in this section can be read about in the Solidity Documentation](#everything-in-this-section-can-be-read-about-in-the-solidity-documentation)
    - [Remix](#remix)
    - [Basic Solidity](#basic-solidity)
    - [Deploying to a "Live" network](#deploying-to-a-live-network)
- [Lesson 2: Storage Factory](#lesson-2-storage-factory)
    - [Inheritance, Factory Pattern, and Interacting with External Contracts](#inheritance-factory-pattern-and-interacting-with-external-contracts)
- [Lesson 3: Fund Me](#lesson-3-fund-me)
    - [Payable, msg.sender, msg.value, Units of Measure](#payable-msgsender-msgvalue-units-of-measure)
    - [Chainlink Oracles](#chainlink-oracles)
    - [Importing from NPM and Advanced Solidity](#importing-from-npm-and-advanced-solidity)
- [Lesson 4: Web3.js Simple Storage](#lesson-4-web3js-simple-storage)
    - [Installing VSCode, Python, and Web3](#installing-vscode-python-and-web3)
    - [Our First Python Script with Web3.js - Deploying a Contract](#our-first-python-script-with-web3js---deploying-a-contract)
    - [Interacting with Our Contract in Javascript & Web3.js](#interacting-with-our-contract-in-javascript--web3js)
- [Lesson 5: Hardhat Simple Storage](#lesson-5-hardhat-simple-storage)
    - [Hardhat Introduction](#hardhat-introduction)
    - [Installing Hardhat](#installing-hardhat)
    - [Testing Basics](#testing-basics)
    - [[Hardhat console]](#hardhat-console)
- [Lesson 6: Hardhat Fund Me](#lesson-6-hardhat-fund-me)
    - [Introduction](#introduction)
    - [Dependencies, Deploying, and Networks](#dependencies-deploying-and-networks)
    - [Funding and Withdrawing Javascript Scripts](#funding-and-withdrawing-javascript-scripts)
    - [Testing across networks](#testing-across-networks)
    - [Git](#git)
- [Lesson 7: SmartContract Lottery](#lesson-7-smartcontract-lottery)
    - [Introduction](#introduction-1)
    - [`Lottery.sol`](#lotterysol)
- [Lesson 8: Full Stack Introduction](#lesson-8-full-stack-introduction)
- [Lesson 9: Full Stack Lottery](#lesson-9-full-stack-lottery)
- [Lesson 10: Hardhat Starter Kit](#lesson-10-hardhat-starter-kit)
- [Lesson 11: ERC20s, EIPs, and Token Standards](#lesson-11-erc20s-eips-and-token-standards)
- [Lesson 12: Defi & Aave](#lesson-12-defi--aave)
    - [Defi Intro](#defi-intro)
- [Lesson 13: NFTs](#lesson-13-nfts)
- [Lesson 14: NFT Marketplace](#lesson-14-nft-marketplace)
- [Lesson 15: Upgrades](#lesson-15-upgrades)
- [Lesson 16 [DAOs]](#lesson-16-daos)
- [Lesson 17 [Security]](#lesson-17-security)
  - [Where do I go now?](#where-do-i-go-now)
    - [Learning More](#learning-more)
    - [Community](#community)
    - [Hackathons](#hackathons)

# Lesson 0: Welcome To Blockchain

## What is a Blockchain?

-   [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)
-   [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/)
-   [Hybrid Smart Contracts](https://blog.chain.link/hybrid-smart-contracts-explained/)
-   [Blockchain Oracles](https://betterprogramming.pub/what-is-a-blockchain-oracle-f5ccab8dbd72?source=friends_link&sk=d921a38466df8a9176ed8dd767d8c77d)
-   [What is a blockchain](https://www.investopedia.com/terms/b/blockchain.asp)

## Making Your First Transaction

-   [Metamask](https://metamask.io/)
-   [Etherscan](https://etherscan.io/)
-   [Rinkeby Etherscan](https://rinkeby.etherscan.io/)
-   [Kovan Etherscan](https://kovan.etherscan.io/)
-   Rinkeby Faucet (Check the [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#rinkeby))
    -   NOTE: The Chainlink documentation always has the most up to date faucets on their [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#rinkeby). If the faucet above is broken, check the chainlink documentation for the most up to date faucet.
-   OR, use the [Kovan ETH Faucet](https://faucets.chain.link/), just be sure to swap your metamask to kovan!
-   [Gas and Gas Fees](https://ethereum.org/en/developers/docs/gas/)
-   [Wei, Gwei, and Ether Converter](https://eth-converter.com/)
-   [ETH Gas Station](https://ethgasstation.info/)

## How Do Blockchains Work?

-   [Blockchain Demo](https://andersbrownworth.com/blockchain/)
-   [Public / Private Keys](https://andersbrownworth.com/blockchain/public-private-keys/keys)
-   [Layer 2 and Rollups](https://ethereum.org/en/developers/docs/scaling/layer-2-rollups/)
-   [Decentralized Blockchain Oracles](https://blog.chain.link/what-is-the-blockchain-oracle-problem/)
-   [Block Rewards](https://www.investopedia.com/terms/b/block-reward.asp)
-   [Run Your Own Ethereum Node](https://geth.ethereum.org/docs/getting-started)

### Consensus

-   [Consensus](https://wiki.polkadot.network/docs/learn-consensus)
-   [Proof of Stake](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/)
-   [Proof of Work](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/)
-   [Nakamoto Consensus](https://blockonomi.com/nakamoto-consensus/)
-   [Ethereum 2 (the merge)](https://ethereum.org/en/eth2/)

# Lesson 1: [Welcome to Remix! Simple Storage](https://github.com/PatrickAlphaC/simple_storage)

💻 Code: https://github.com/PatrickAlphaC/simple_storage

### Everything in this section can be read about in the [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.6/index.html)

### [Remix](https://remix.ethereum.org/)

### Basic Solidity

-   Versioning
-   Compiling
-   Contract Declaration
-   [Types & Declaring Variables](https://docs.soliditylang.org/en/v0.8.6/types.html)
    -   `uint256`, `int256`, `bool`, `string`, `address`, `bytes32`
-   Default Initializations
-   Comments
-   Functions
-   Deploying a Contract
-   Calling a public state-changing Function
-   [Visibility](https://docs.soliditylang.org/en/v0.7.3/contracts.html#visibility-and-getters)
-   Scope
-   View & Pure Functions
-   Structs
-   Intro to Storage
-   Arrays - Dynamic & Fixed sized
-   Compiler Errors and Warnings
-   Memory, storage, calldata
-   Mappings
-   SPDX License
-   Recap

### Deploying to a "Live" network

-   A testnet or mainnet
-   [Find a faucet here](https://docs.chain.link/docs/link-token-contracts/#rinkeby)
-   Connecting Metamask
-   Interacting with Deployed Contracts
-   The EVM

# Lesson 2: [Storage Factory](https://github.com/PatrickAlphaC/storage_factory)

💻 Code: https://github.com/PatrickAlphaC/storage_factory

### Inheritance, Factory Pattern, and Interacting with External Contracts

-   Factory Pattern
-   Imports
-   Deploy a Contract From a Contract
-   Interact With a Deployed Contract
-   Recap

# Lesson 3: [Fund Me](https://github.com/PatrickAlphaC/fund_me)

💻 Code: https://github.com/PatrickAlphaC/fund_me

### Payable, msg.sender, msg.value, Units of Measure

-   Payable
-   [Wei/Gwei/Eth Converter](https://eth-converter.com/)
-   msg.sender & msg.value

### Chainlink Oracles

-   Decentralized Oracle Network Chainlink
    -   Blockchains can't make API calls
    -   Centralized Nodes are Points of Failure
-   [data.chain.link](https://data.chain.link/)
-   Getting External Data with Chainlink Oracles
    -   [Chainlink](https://docs.chain.link/)
    -   [Faucets and Contract Addresses](https://docs.chain.link/docs/link-token-contracts/)
        -   [Kovan](https://docs.chain.link/docs/link-token-contracts/#kovan)
    -   [Getting Price Information](https://docs.chain.link/docs/get-the-latest-price/)

### Importing from NPM and Advanced Solidity

-   Decimals/Floating Point Numbers in Solidity
-   latestRoundData
-   Importing from NPM in Remix
-   Interfaces
    -   Introduction to ABIs
-   [Getting Price Feed Addresses](https://docs.chain.link/docs/reference-contracts/)
-   getPrice
-   Tuples
    -   Unused Tuple Variables
-   Matching Units (WEI/GWEI/ETH)
-   getConversionRate
-   Matching Units (Continued)
-   SafeMath & Integer Overflow
    -   using keyword
    -   [Libraries](https://docs.soliditylang.org/en/v0.8.6/contracts.html#libraries)
    -   SafeMath PSA
-   Setting a Threshold
-   Require
-   Revert
-   Withdraw Function
-   Transfer
-   Balance
-   this
-   Contract Owners
-   Constructor
-   ==
-   Modifiers
-   Resetting
-   for loop
-   Array Length
-   Forcing a Transaction
-   Recap

# Lesson 4: [Web3.js Simple Storage]()

💻 Code:

### Installing VSCode, Python, and Web3

-   [Developer Bootcamp Setup Instructions (metamask, vscode, python, nodejs..)](https://chain.link/bootcamp/brownie-setup-instructions)
-   [VSCode](https://code.visualstudio.com/download)
-   [VSCode Crash Course](https://www.youtube.com/watch?v=WPqXP_kLzpo)
-   Extensions
-   Short Cuts:
    -   [VSCode Shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings)
    -   [VSCode MacOS Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
-   [Python](https://www.python.org/downloads/)
    -   Install Troubleshooting
-   Terminal
-   Making a directory/Folder
-   Opening the folder up with VSCode
-   Creating a new file
-   Syntax Highlights
-   Remember to save!
-   Setting linting compile version
-   VSCode Solidity Settings
    -   Formatting & Format on Save
    -   Solidity Prettier
    -   [Python Black](https://pypi.org/project/black/)
    -   [pip](https://pypi.org/project/pip/)

### Our First Python Script with Web3.js - Deploying a Contract

-   Reading our solidity file
-   Running a Python Script in the Terminal
-   [MaxOS Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
-   [Windows Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
-   [Linux Shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)
-   Compiling in Python
-   [py-solc-x](https://pypi.org/project/py-solc-x/)
    -   compile_standard
-   Colorized Brackets
-   JSON ABI
-   Saving Compiled Code
-   Formatting JSON

### Interacting with Our Contract in Javascript & Web3.js

# Lesson 5: [Hardhat Simple Storage]()

### Hardhat Introduction

### Installing Hardhat

### Testing Basics

### [Hardhat console]

-   `brownie console`

# Lesson 6: [Hardhat Fund Me]()

### Introduction

-   Setup

### Dependencies, Deploying, and Networks

### Funding and Withdrawing Javascript Scripts

### Testing across networks

### Git

-   Tweet it out!

# Lesson 7: SmartContract Lottery

💻 Code:

### Introduction

-   Add a `README.md`
-   Defining the project
-   Is it decentralized?

### `Lottery.sol`

# Lesson 8: Full Stack Introduction

# Lesson 9: Full Stack Lottery

# Lesson 10: [Hardhat Starter Kit](https://github.com/smartcontractkit/hardhat-starter-kit)

💻 Code: https://github.com/smartcontractkit/hardhat-starter-kit

# Lesson 11: [ERC20s, EIPs, and Token Standards]()

💻 Code:

-

# Lesson 12: [Defi & Aave]()

💻 Code:

### Defi Intro

-   [Defipulse](https://defipulse.com/)
-   [Defillama](https://defillama.com/)
-   [Aave Testnet Site](https://testnet.aave.com/)
-   [Paraswap](https://paraswap.io/)
-   Decentralized Exchange

# Lesson 13: [NFTs]()

💻 Code

# Lesson 14: NFT Marketplace

# Lesson 15: [Upgrades](https://github.com/PatrickAlphaC/upgrades-mix)

💻 Code: https://github.com/PatrickAlphaC/upgrades-mix

# Lesson 16 [DAOs]

# Lesson 17 [Security]

<!-- # Closing and Summary
## Security
- [Best Practices](https://consensys.github.io/smart-contract-best-practices/)
- [Attacks](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
  - [Oracle Attacks](https://hackernoon.com/how-dollar100m-got-stolen-from-defi-in-2021-price-oracle-manipulation-and-flash-loan-attacks-explained-3n6q33r1)
  - [Re-entrancy Attacks](https://quantstamp.com/blog/what-is-a-re-entrancy-attack)
- [Damn Vulnerable Defi](https://www.damnvulnerabledefi.xyz/)
- [Ethernaut](https://ethernaut.openzeppelin.com/)
- Some Auditors
  - [OpenZeppelin](https://openzeppelin.com/)
  - [SigmaPrime](https://sigmaprime.io/)
  - [Trail of Bits](https://www.trailofbits.com/) -->

## Where do I go now?

### Learning More

-   [CryptoZombies](https://cryptozombies.io/)
-   [Dapp University](https://www.youtube.com/channel/UCY0xL8V6NzzFcwzHCgB8orQ)
-   [ChainShot](https://www.chainshot.com/courses)
-   [Ivan on Tech](https://academy.ivanontech.com/)
-   [Eat the Blocks](https://www.youtube.com/channel/UCZM8XQjNOyG2ElPpEUtNasA)
-   [Patrick Collins](https://www.youtube.com/channel/UCn-3f8tw_E1jZvhuHatROwA)
-   [Austin Griffith](https://www.youtube.com/channel/UC_HI2i2peo1A-STdG22GFsA)
-   [Nader Dabit](https://www.youtube.com/user/boyindasouth)
-   [Ethereum.org](https://ethereum.org/en/)

### Community

-   Twitter
-   [Brownie Discord](https://discord.gg/9zk7snTfWe)
-   [Ethereum Discord](https://ethereum.org/en/)
-   [Chainlink Discord](https://discord.gg/2YHSAey)
-   [Reddit ethdev](https://www.reddit.com/r/ethdev/)

### Hackathons

-   [CL Hackathon](https://chain.link/hackathon)
-   [ETH Global](https://ethglobal.co/)
-   [ETH India](https://twitter.com/ETHIndiaco)

Be sure to check out project grant programs!

And make today an amazing day!

Improvements from the Python edition:

1. Videos are split into 2 -> 15 minute sections
2. Javascript & Typescript edition of code
3. Deeper explainer of:
    1. Stackoverflow
    2. Stack Exchange ETH
    3. How to ask good questions & get help
4. Aave lesson improvements
5. Fundme lesson improvements
6. Not using sleep to wait for tx to complete
7. Front end stuff
