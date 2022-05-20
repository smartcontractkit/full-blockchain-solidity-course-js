<!-- [YouTube Video](https://www.youtube.com/watch?v=M576WGiDBdQ) -->

<!-- <br/>
<p align="center">
<a href="https://www.youtube.com/watch?v=M576WGiDBdQ" target="_blank">
<img src="./img/youtube_thumbnail.jpeg" width="350" alt="Solidity, Blockchain, and Smart Contract Course – Beginner to Expert Python Tutorial">
</a>
</p>
<br/> -->

Welcome to the repository for the Ultimate Web3, Full Stack Solidity, and Smart Contract - Beginner to Expert Full Course | Javascript Edition FreeCodeCamp Course!

All code references have both a javascript and a typescript edition.

Recommended Testnet: Rinkeby

# [Testnet Faucets](https://faucets.chain.link)
Main Faucet: https://faucets.chain.link

Backup Faucet: https://rinkebyfaucet.com/

> ⚠️ All code associated with this course is for demo purposes only. They have not been audited and should not be considered production ready. Please use at your own risk. 

# Resources For This Course

### Questions

-   [Github Discussions](https://github.com/smartcontractkit/full-blockchain-solidity-course-py/discussions)
    -   Ask questions and chat about the course here!
-   [Stack Exchange Ethereum](https://ethereum.stackexchange.com/)
    -   Great place for asking technical questions about Ethereum
-   [StackOverflow](https://stackoverflow.com/)
    -   Great place for asking technical questions overall


# Table of Contents

- [Testnet Faucets](#testnet-faucets)
- [Resources For This Course](#resources-for-this-course)
    - [Questions](#questions)
- [Table of Contents](#table-of-contents)
<details>
<summary> <a href="#lesson-0-the-edge-of-the-rabbit-hole">Lesson 0: The Edge of the Rabbit Hole</a></summary>
<ol>
  <li>
  <a href="#welcome-to-the-course">Welcome to the course! </a>
  </li>
  <li>
  <a href="#best-practices">Best Practices </a>
  </li>
</ol>
</details>
<details>
<summary> <a href="#lesson-1-blockchain-basics"> Lesson 1: Blockchain Basics </a> </summary>
  <ol>
  <li>
  <a href="#what-is-a-blockchain-what-does-a-blockchain-do">What is a Blockchain? What does a blockchain do?</a>
  </li>
  </ol>
</details>
  - [The Purpose Of Smart Contracts](#the-purpose-of-smart-contracts)
  - [Other Blockchain Benefits](#other-blockchain-benefits)
  - [What have Smart Contracts done so far?](#what-have-smart-contracts-done-so-far)
  - [Making Your First Transaction](#making-your-first-transaction)
  - [Gas I: Introduction to Gas](#gas-i-introduction-to-gas)
  - [How Do Blockchains Work?](#how-do-blockchains-work)
  - [Signing Transactions](#signing-transactions)
  - [Gas II](#gas-ii)
  - [High-Level Blockchain Fundamentals](#high-level-blockchain-fundamentals)
- [Lesson 2: Welcome to Remix! Simple Storage](#lesson-2-welcome-to-remix-simple-storage)
  - [Introduction](#introduction)
  - [Setting Up Your First Contract](#setting-up-your-first-contract)
  - [Basic Solidity: Types](#basic-solidity-types)
  - [Basic Solidity: Functions](#basic-solidity-functions)
  - [Basic Solidity: Arrays & Structs](#basic-solidity-arrays--structs)
  - [Basic Solidity: Compiler Errors and Warnings](#basic-solidity-compiler-errors-and-warnings)
  - [Memory, Storage, Calldata (Intro)](#memory-storage-calldata-intro)
  - [Mappings](#mappings)
  - [Deploying your First Contract](#deploying-your-first-contract)
  - [The EVM & A Recap of Lesson 2](#the-evm--a-recap-of-lesson-2)
- [Lesson 3: Remix Storage Factory](#lesson-3-remix-storage-factory)
  - [Introduction](#introduction-1)
  - [Basic Solidity: Importing Contracts into other Contracts](#basic-solidity-importing-contracts-into-other-contracts)
  - [Basic Solidity: Interacting with other Contracts](#basic-solidity-interacting-with-other-contracts)
  - [Basic Solidity: Inheritance & Overrides](#basic-solidity-inheritance--overrides)
  - [Lesson 3 Recap](#lesson-3-recap)
- [Lesson 4: Remix Fund Me](#lesson-4-remix-fund-me)
  - [Introduction](#introduction-2)
  - [Sending ETH Through a Function & Reverts](#sending-eth-through-a-function--reverts)
  - [Chainlink & Oracles](#chainlink--oracles)
  - [Review of Sending ETH and working with Chainlink](#review-of-sending-eth-and-working-with-chainlink)
  - [Interfaces & Price Feeds](#interfaces--price-feeds)
  - [Importing from GitHub & NPM](#importing-from-github--npm)
  - [Floating Point Math in Solidtiy](#floating-point-math-in-solidtiy)
  - [Basic Solidity: Arrays & Structs II](#basic-solidity-arrays--structs-ii)
  - [Review of Interfacs, Importing from GitHub, & Math in Solidity](#review-of-interfacs-importing-from-github--math-in-solidity)
  - [Libraries](#libraries)
  - [SafeMath, Overflow Checking, and the "unchecked" keywork](#safemath-overflow-checking-and-the-unchecked-keywork)
  - [Basic Solidity: For Loop](#basic-solidity-for-loop)
  - [Basic Solidity: Resetting an Array](#basic-solidity-resetting-an-array)
  - [Sending ETH from a Contract](#sending-eth-from-a-contract)
  - [Basic Solidity: Constructor](#basic-solidity-constructor)
  - [Basic Solidity: Modifiers](#basic-solidity-modifiers)
  - [Testnet Demo](#testnet-demo)
  - [Advanced Solidity](#advanced-solidity)
    - [Immutable & Constant](#immutable--constant)
    - [Custom Errors](#custom-errors)
    - [Receive & Fallback Functions](#receive--fallback-functions)
  - [Lesson 4 Recap](#lesson-4-recap)
- [Lesson 5: Ethers.js Simple Storage](#lesson-5-ethersjs-simple-storage)
  - [Effective Debugging Strategies & Getting Help](#effective-debugging-strategies--getting-help)
    - [How to Debug Anything Video](#how-to-debug-anything-video)
  - [Installation & Setup](#installation--setup)
    - [Mac & Linux Setup](#mac--linux-setup)
    - [Windows Setup](#windows-setup)
    - [Gitpod](#gitpod)
  - [Local Development Introduction](#local-development-introduction)
    - [Optional Javascript Crash Courses](#optional-javascript-crash-courses)
  - [Tiny Javascript Refresher](#tiny-javascript-refresher)
  - [Asynchronous Programming in Javascript](#asynchronous-programming-in-javascript)
  - [Compiling our Solidity](#compiling-our-solidity)
  - [Ganache & Networks](#ganache--networks)
  - [Introduction to Ethers.js](#introduction-to-ethersjs)
    - [A Note on the await Keyword](#a-note-on-the-await-keyword)
  - [Adding Transaction Overrides](#adding-transaction-overrides)
  - [Transaction Receipts](#transaction-receipts)
  - [Sending a "raw" Transaction in Ethersjs](#sending-a-raw-transaction-in-ethersjs)
  - [Interacting with Contracts in Ethersjs](#interacting-with-contracts-in-ethersjs)
  - [Environment Variables](#environment-variables)
  - [Better Private Key Management](#better-private-key-management)
  - [Optional Prettier Formatting](#optional-prettier-formatting)
  - [Deploying to a Testnet or a Mainnet](#deploying-to-a-testnet-or-a-mainnet)
  - [Verifying on Block Explorers from the UI](#verifying-on-block-explorers-from-the-ui)
  - [Alchemy Dashboard & The Mempool](#alchemy-dashboard--the-mempool)
  - [Lesson 5 Recap](#lesson-5-recap)
    - [Typescript Ethers Simple Storage](#typescript-ethers-simple-storage)
- [Lesson 6: Hardhat Simple Storage](#lesson-6-hardhat-simple-storage)
  - [Introduction](#introduction-3)
  - [Hardhat Setup](#hardhat-setup)
    - [Troubleshooting Hardaht Setup](#troubleshooting-hardaht-setup)
  - [Hardhat Setup Continued](#hardhat-setup-continued)
  - [Deploying SimpleStorage from Hardhat](#deploying-simplestorage-from-hardhat)
  - [Networks in Hardhat](#networks-in-hardhat)
  - [Programatic Verification](#programatic-verification)
  - [Interacting with Contracts in Hardhat](#interacting-with-contracts-in-hardhat)
  - [Artifacts Troubleshooting](#artifacts-troubleshooting)
  - [Custom Hardhat Tasks](#custom-hardhat-tasks)
  - [Hardhat Localhost Node](#hardhat-localhost-node)
  - [The Hardhat Console](#the-hardhat-console)
  - [Hardhat Tests](#hardhat-tests)
  - [Hardhat Gas Reporter](#hardhat-gas-reporter)
  - [Solidity Coverage](#solidity-coverage)
  - [Hardhat Waffle](#hardhat-waffle)
  - [Lesson 6 Recap](#lesson-6-recap)
    - [Typescript Hardhat Simple Storage](#typescript-hardhat-simple-storage)
- [Lesson 7: Hardhat Fund Me](#lesson-7-hardhat-fund-me)
  - [Introduction](#introduction-4)
  - [Hardhat Setup - Fund Me](#hardhat-setup---fund-me)
  - [Linting](#linting)
  - [Hardhat Setup - Fund Me - Continued](#hardhat-setup---fund-me---continued)
  - [Importing from NPM](#importing-from-npm)
  - [Hardhat Deploy](#hardhat-deploy)
  - [Mocking](#mocking)
  - [Utils Folder](#utils-folder)
  - [Testnet Demo - Hardhat Fund Me](#testnet-demo---hardhat-fund-me)
  - [Solidity Style Guide](#solidity-style-guide)
  - [Testing Fund Me](#testing-fund-me)
  - [Breakpoints & Debugging](#breakpoints--debugging)
  - [Gas III:](#gas-iii)
  - [console.log & Debugging](#consolelog--debugging)
  - [Testing Fund Me II](#testing-fund-me-ii)
  - [Storage in Solidity](#storage-in-solidity)
  - [Gas Optimizations using Storage Knowledge](#gas-optimizations-using-storage-knowledge)
  - [Solidity Chainlink Style Guide](#solidity-chainlink-style-guide)
  - [Storage Review](#storage-review)
  - [Staging Tests](#staging-tests)
  - [Running Scripts on a Local Node](#running-scripts-on-a-local-node)
  - [Adding Scripts to your package.json](#adding-scripts-to-your-packagejson)
  - [Pushing to GitHub](#pushing-to-github)
  - [🐸🐦 Tweet Me (add your repo in)!](#-tweet-me-add-your-repo-in)
- [Lesson 8: HTML / Javascript Fund Me (Full Stack / Front End)](#lesson-8-html--javascript-fund-me-full-stack--front-end)
  - [Introduction](#introduction-5)
  - [How Websites work with Web3 Wallets](#how-websites-work-with-web3-wallets)
  - [HTML Setup](#html-setup)
  - [Connecting HTML to Metamask](#connecting-html-to-metamask)
  - [Javascript in it's own file](#javascript-in-its-own-file)
  - [ES6 vs Nodejs](#es6-vs-nodejs)
  - [Sending a transaction from a Website](#sending-a-transaction-from-a-website)
  - [Resetting an Account in Metamask](#resetting-an-account-in-metamask)
  - [Listening for Events and Completed Transactions](#listening-for-events-and-completed-transactions)
  - [Input Forms](#input-forms)
  - [Reading from the Blockchain](#reading-from-the-blockchain)
  - [Withdraw Function](#withdraw-function)
  - [Lesson 8 Recap](#lesson-8-recap)
    - [Optional Links:](#optional-links)
- [Lesson 9: Hardhat Smart Contract Lottery](#lesson-9-hardhat-smart-contract-lottery)
  - [Introduction](#introduction-6)
  - [Hardhat Setup - Smart Contract Lottery](#hardhat-setup---smart-contract-lottery)
  - [Raffle.sol Setup](#rafflesol-setup)
  - [Introduction to Events](#introduction-to-events)
  - [Events in Raffle.sol](#events-in-rafflesol)
  - [Introduction to Chainlink VRF](#introduction-to-chainlink-vrf)
    - [Sub-Lesson: Chainlink VRF](#sub-lesson-chainlink-vrf)
  - [Implementing Chainlink VRF - Introduction](#implementing-chainlink-vrf---introduction)
    - [Hardhat Shorthand](#hardhat-shorthand)
  - [Implementing Chainlink VRF - The Request](#implementing-chainlink-vrf---the-request)
  - [Implementing Chainlink VRF - The FulFill](#implementing-chainlink-vrf---the-fulfill)
    - [Modulo](#modulo)
  - [Introduction to Chainlink Keepers](#introduction-to-chainlink-keepers)
  - [Implementing Chainlink Keepers - checkUpkeep](#implementing-chainlink-keepers---checkupkeep)
    - [Enums](#enums)
  - [Implementing Chainlink Keepers - checkUpkeep continued](#implementing-chainlink-keepers---checkupkeep-continued)
  - [Implementing Chainlink Keepers - performUpkeep](#implementing-chainlink-keepers---performupkeep)
  - [Code Cleanup](#code-cleanup)
  - [Deploying Raffle.sol](#deploying-rafflesol)
    - [Mock Chainlink VRF Coordinator](#mock-chainlink-vrf-coordinator)
    - [Continued](#continued)
  - [Raffle.sol Unit Tests](#rafflesol-unit-tests)
    - [Testing Events & Chai Matchers](#testing-events--chai-matchers)
    - [Continued I](#continued-i)
  - [Hardhat Methods & Time Travel](#hardhat-methods--time-travel)
    - [Continued II](#continued-ii)
  - [Callstatic](#callstatic)
    - [Continued III](#continued-iii)
    - [Massive Promise Test](#massive-promise-test)
    - [Continued IV](#continued-iv)
  - [Raffle.sol Staging Tests](#rafflesol-staging-tests)
  - [Testing on a Testnet](#testing-on-a-testnet)
    - [Recommended LINK amounts for Rinkeby Staging Test:](#recommended-link-amounts-for-rinkeby-staging-test)
  - [Conclusion](#conclusion)
  - [Typescript - Smart Contract Lottery](#typescript---smart-contract-lottery)
- [Lesson 10: NextJS Smart Contract Lottery (Full Stack / Front End)](#lesson-10-nextjs-smart-contract-lottery-full-stack--front-end)
  - [Introduction](#introduction-7)
    - [Optional Sub-Lesson: Full Stack Development & Other Libraries](#optional-sub-lesson-full-stack-development--other-libraries)
  - [NextJS Setup](#nextjs-setup)
  - [Manual Header I](#manual-header-i)
    - [React Hooks](#react-hooks)
  - [Manual Header II](#manual-header-ii)
  - [useEffect Hook](#useeffect-hook)
  - [Local Storage](#local-storage)
  - [isWeb3EnabledLoading](#isweb3enabledloading)
  - [web3uikit](#web3uikit)
  - [Introduction to Calling Functions in Nextjs](#introduction-to-calling-functions-in-nextjs)
    - [Automatic Constant Value UI Updater](#automatic-constant-value-ui-updater)
    - [runContractFunction](#runcontractfunction)
  - [useState](#usestate)
  - [Calling Functions in NextJS](#calling-functions-in-nextjs)
  - [useNotification](#usenotification)
  - [Reading & Displaying Contract Data](#reading--displaying-contract-data)
  - [A Note about `onSuccess`](#a-note-about-onsuccess)
  - [A Challenge to You](#a-challenge-to-you)
  - [Tailwind & Styling](#tailwind--styling)
  - [Introduction to Hosting your Site](#introduction-to-hosting-your-site)
  - [IPFS](#ipfs)
  - [Hosting on IPFS](#hosting-on-ipfs)
  - [Hosting on IPFS & Filecoin using Fleek](#hosting-on-ipfs--filecoin-using-fleek)
  - [Filecoin Overview](#filecoin-overview)
  - [Lesson 10 Recap](#lesson-10-recap)
- [Lesson 11: Hardhat Starter Kit](#lesson-11-hardhat-starter-kit)
- [Lesson 12: Hardhat ERC20s](#lesson-12-hardhat-erc20s)
  - [What is an ERC? What is an EIP?](#what-is-an-erc-what-is-an-eip)
  - [What is an ERC20?](#what-is-an-erc20)
  - [Manually Creating an ERC20 Token](#manually-creating-an-erc20-token)
  - [Creating an ERC20 Token with Openzeppelin](#creating-an-erc20-token-with-openzeppelin)
  - [Lesson 12 Recap](#lesson-12-recap)
- [Lesson 13: Hardhat DeFi & Aave](#lesson-13-hardhat-defi--aave)
  - [What is DeFi?](#what-is-defi)
  - [What is Aave?](#what-is-aave)
  - [Programatic Borrowing & Lending](#programatic-borrowing--lending)
  - [WETH - Wrapped ETH](#weth---wrapped-eth)
  - [Forking Mainnet](#forking-mainnet)
  - [Depositing into Aave](#depositing-into-aave)
  - [Borrowing from Aave](#borrowing-from-aave)
  - [Repaying with Aave](#repaying-with-aave)
  - [Visualizing the Transactions](#visualizing-the-transactions)
  - [Lesson 13 Recap](#lesson-13-recap)
  - [Happy Bow-Tie Friday with Austin Griffith](#happy-bow-tie-friday-with-austin-griffith)
    - [More DeFi Learnings:](#more-defi-learnings)
- [Lesson 14: Hardhat NFTs (EVERYTHING you need to know about NFTs)](#lesson-14-hardhat-nfts-everything-you-need-to-know-about-nfts)
  - [What is an NFT?](#what-is-an-nft)
  - [Code Overview](#code-overview)
  - [Hardhat Setup](#hardhat-setup-1)
  - [Basic NFT](#basic-nft)
    - [Write Tests](#write-tests)
  - [Random IPFS NFT](#random-ipfs-nft)
    - [Mapping Chainlink VRF Requests](#mapping-chainlink-vrf-requests)
    - [Creating Rare NFTs](#creating-rare-nfts)
    - [Setting the NFT Image](#setting-the-nft-image)
    - [Setting an NFT Mint Price](#setting-an-nft-mint-price)
    - [Deploy Script](#deploy-script)
    - [Uploading Token Images with Pinata](#uploading-token-images-with-pinata)
    - [Uploading Token URIs (metadata) with Pinata](#uploading-token-uris-metadata-with-pinata)
    - [Deploying](#deploying)
    - [Tests](#tests)
  - [Dynamic SVG On-Chain NFT](#dynamic-svg-on-chain-nft)
    - [What is an SVG?](#what-is-an-svg)
    - [Initial Code](#initial-code)
    - [Base64 Encoding](#base64-encoding)
  - [Advanced: EVM Opcodes, Encoding, and Calling](#advanced-evm-opcodes-encoding-and-calling)
    - [abi.encode & abi.encodePacked](#abiencode--abiencodepacked)
    - [Introduction to Encoding Function Calls Directly](#introduction-to-encoding-function-calls-directly)
    - [Introduction to Encoding Function Calls Recap](#introduction-to-encoding-function-calls-recap)
    - [Encoding Function Calls Directly](#encoding-function-calls-directly)
    - [Creating an NFT TokenURI on-Chain](#creating-an-nft-tokenuri-on-chain)
    - [Making the NFT Dynamic](#making-the-nft-dynamic)
    - [Deploy Script](#deploy-script-1)
  - [Deploying the NFTs to a Testnet](#deploying-the-nfts-to-a-testnet)
  - [Lesson 14 Recap](#lesson-14-recap)
- [Lesson 15: NextJS NFT Marketplace (If you finish this lesson, you are a full-stack MONSTER!)](#lesson-15-nextjs-nft-marketplace-if-you-finish-this-lesson-you-are-a-full-stack-monster)
  - [Introduction](#introduction-8)
  - [Part I: NFT Marketplace Contracts](#part-i-nft-marketplace-contracts)
    - [Hardhat Setup](#hardhat-setup-2)
    - [NftMarketplace.sol](#nftmarketplacesol)
  - [Reentrancy](#reentrancy)
    - [NftMarketplace.sol - Continued](#nftmarketplacesol---continued)
    - [NftMarketplace.sol - Deploy Script](#nftmarketplacesol---deploy-script)
    - [NftMarketplace.sol - Tests](#nftmarketplacesol---tests)
    - [NftMarketplace.sol - Scripts](#nftmarketplacesol---scripts)
  - [Part II: Moralis Front End](#part-ii-moralis-front-end)
    - [What is Moralis?](#what-is-moralis)
    - [NextJS Setup](#nextjs-setup-1)
    - [Adding Tailwind](#adding-tailwind)
    - [Introduction to Indexing in Web3](#introduction-to-indexing-in-web3)
    - [Connecting Moralis to our Local Hardhat Node](#connecting-moralis-to-our-local-hardhat-node)
    - [Moralis Event Sync](#moralis-event-sync)
      - [Reset Local Chain](#reset-local-chain)
    - [Moralis Cloud Functions](#moralis-cloud-functions)
      - [Practice Resetting the Local Chain](#practice-resetting-the-local-chain)
    - [Moralis Cloud Functions II](#moralis-cloud-functions-ii)
    - [Querying the Moralis Database](#querying-the-moralis-database)
    - [Rendering the NFT Images](#rendering-the-nft-images)
    - [Update Listing Modal](#update-listing-modal)
    - [Buy NFT Listing](#buy-nft-listing)
    - [Listing NFTs for Sale](#listing-nfts-for-sale)
  - [Part III: TheGraph Front End](#part-iii-thegraph-front-end)
    - [Introduction](#introduction-9)
    - [What is The Graph?](#what-is-the-graph)
    - [Building a Subgraph](#building-a-subgraph)
    - [Deploying our Subgraph](#deploying-our-subgraph)
    - [Reading from The Graph](#reading-from-the-graph)
    - [Hosting our Dapp](#hosting-our-dapp)
- [Lesson 16: Hardhat Upgrades](#lesson-16-hardhat-upgrades)
  - [Upgradeable Smart Contracts Overview](#upgradeable-smart-contracts-overview)
  - [Types of Upgrades](#types-of-upgrades)
  - [Delegatecall](#delegatecall)
  - [Small Proxy Example](#small-proxy-example)
  - [Transparent Upgradeable Smart Contract](#transparent-upgradeable-smart-contract)
- [Lesson 17: Hardhat DAOs](#lesson-17-hardhat-daos)
  - [Introduction](#introduction-10)
  - [What is a DAO?](#what-is-a-dao)
  - [How to build a DAO](#how-to-build-a-dao)
- [Lesson 18: Security & Auditing](#lesson-18-security--auditing)
  - [Introduction](#introduction-11)
  - [Slither](#slither)
  - [Fuzzing and Eth Security Toolbox](#fuzzing-and-eth-security-toolbox)
  - [Closing Thoughts](#closing-thoughts)
- [Congratulations](#congratulations)
  - [Where do I go now?](#where-do-i-go-now)
    - [Learning More](#learning-more)
    - [Community](#community)
    - [Hackathons](#hackathons)


<!-- TODO: Add timestamps for lessons and sections -->
<!-- TODO: Add gitpod to all repos -->
<!-- TODO: Make sure Typescript is all set for all repos -->
<!-- TODO: Make sure all gitignores are looking good -->
<!-- TODO: Add dropdowns for the main table of contents -->
<!-- TODO: Add issues so that people know to go to discussions, and only make an issue if the class has an issue -->
<!-- TODO: Make sure all tests don't use async functions in the describe block -->
<!-- TODO: Make sure all tests use `async function(){}` syntax instead of anon functions -->
<!-- TODO: Add `Special Guest: <name>` for all guests (and also Matt for his UI help!) -->

# Lesson 0: The Edge of the Rabbit Hole
## Welcome to the course! 
*[0:00]()*
## Best Practices 
*[4:24]()*

# Lesson 1: Blockchain Basics
*[8:28]()*

## What is a Blockchain? What does a blockchain do? 
-   [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)
    -   [Satoshi Nakamoto](https://en.wikipedia.org/wiki/Satoshi_Nakamoto)
-   [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/)
    -   [Vitalik Buterin](https://en.wikipedia.org/wiki/Vitalik_Buterin)
-   [What is a Smart Contract?](https://chain.link/education/smart-contracts)
-   [Nick Szabo](https://en.wikipedia.org/wiki/Nick_Szabo)
-   [Hybrid Smart Contracts](https://blog.chain.link/hybrid-smart-contracts-explained/)
-   [Blockchain Oracles](https://betterprogramming.pub/what-is-a-blockchain-oracle-f5ccab8dbd72?source=friends_link&sk=d921a38466df8a9176ed8dd767d8c77d)
-   [Terminology](https://connect.comptia.org/content/articles/blockchain-terminology)
-   [Web3](https://en.wikipedia.org/wiki/Web3)
-   [What is a blockchain](https://www.investopedia.com/terms/b/blockchain.asp)

## The Purpose Of Smart Contracts
- [Original Video](https://www.youtube.com/watch?v=_JeRq7Gwj5Y&feature=youtu.be)
🦬 [My ETH Denver Talk](https://www.youtube.com/watch?v=06hXCX_jj2E)
🍔 [McDonalds Scandal](https://www.chicagotribune.com/sns-mcdonalds-story.html)
⛓ [More on the evolution of agreements](https://www.youtube.com/watch?v=ufVyX7JDCgg)
✍️ [What is a Smart Contract?](https://www.youtube.com/watch?v=ZE2HxTmxfrI)
🧱 [How does a blockchain work?](https://www.youtube.com/watch?v=SSo_EIwHSd4)
🔮 [Chainlink & Oracles](https://www.youtube.com/watch?v=tIUHQ7sDoaU)

## Other Blockchain Benefits
- [Decentralized]()
- [Transparency & Flexibility]()
- [Speed & Efficiency]()
- [Security & Immutability]()
- [Counterparty Risk Removal]()
- [Trust Minimized Agreements]()

## What have Smart Contracts done so far? 
- [DeFi]()
  - [Defi Llama]()
  - [Why DeFi is Important]()
- [DAOs]()
- [NFTs]()

## Making Your First Transaction
-   [Metamask Download Link](https://metamask.io/)
    -   [What is a Private Key?]()
    -   [What is a Secret Phrase?]()
-   [Etherscan](https://etherscan.io/)
-   [Rinkeby Etherscan](https://rinkeby.etherscan.io/)
-   [Kovan Etherscan](https://kovan.etherscan.io/)
-   Rinkeby Faucet (Check the [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#rinkeby))
    -   NOTE: The Chainlink documentation always has the most up to date faucets on their [link token contracts page](https://docs.chain.link/docs/link-token-contracts/#rinkeby). If the faucet above is broken, check the chainlink documentation for the most up to date faucet.
-   OR, use the [Kovan ETH Faucet](https://faucets.chain.link/), just be sure to swap your metamask to kovan!

## Gas I: Introduction to Gas
-   [Gas and Gas Fees](https://ethereum.org/en/developers/docs/gas/)
-   [Wei, Gwei, and Ether Converter](https://eth-converter.com/)
-   [ETH Gas Station](https://ethgasstation.info/)

## How Do Blockchains Work?
- [What is a hash?]()
- [Blockchain Demo](https://andersbrownworth.com/blockchain/)
- [Summary]()

## Signing Transactions
-   [Public / Private Keys](https://andersbrownworth.com/blockchain/public-private-keys/keys)
-   [Layer 2 and Rollups](https://ethereum.org/en/developers/docs/scaling/layer-2-rollups/)
-   [Decentralized Blockchain Oracles](https://blog.chain.link/what-is-the-blockchain-oracle-problem/)

## Gas II
-   [Block Rewards](https://www.investopedia.com/terms/b/block-reward.asp)
-   Advanced Gas
    -   [EIP 1559](https://www.youtube.com/watch?v=MGemhK9t44Q)
    -   GWEI, WEI, and ETH
        -   [ETH Converter](https://eth-converter.com/)
-   [Gas II Summary]()
-   [Run Your Own Ethereum Node](https://geth.ethereum.org/docs/getting-started)

## High-Level Blockchain Fundamentals
-   [Consensus](https://wiki.polkadot.network/docs/learn-consensus)
-   [Proof of Stake](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/)
-   [Proof of Work](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/)
-   [Nakamoto Consensus](https://blockonomi.com/nakamoto-consensus/)
-   [Ethereum 2 (the merge)](https://ethereum.org/en/eth2/)

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed Blockchain Basics! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

# Lesson 2: [Welcome to Remix! Simple Storage](https://github.com/PatrickAlphaC/simple-storage-fcc)

💻 Code: https://github.com/PatrickAlphaC/simple-storage-fcc

## Introduction
- [Remix](https://remix.ethereum.org/)
- [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.6/index.html)

## Setting Up Your First Contract
-   Versioning
-   Take notes in your code!
-   [What is a software license](https://snyk.io/learn/what-is-a-software-license/)
-   SPDX License
-   Compiling
-   Contract Declaration

## Basic Solidity: Types
-   [Types & Declaring Variables](https://docs.soliditylang.org/en/v0.8.13/)
    -   `uint256`, `int256`, `bool`, `string`, `address`, `bytes32`
    -   [Solidity Types](https://docs.soliditylang.org/en/latest/types.html)
    -   [Bits and Bytes](https://www.youtube.com/watch?v=Dnd28lQHquU)
-   Default Initializations
-   Comments

## Basic Solidity: Functions
-   Functions
-   Deploying a Contract
    -   Smart Contracts have addresses just like our wallets
-   Calling a public state-changing Function
-   [Visibility](https://docs.soliditylang.org/en/v0.7.3/contracts.html#visibility-and-getters)
-   Gas III | An example
-   Scope
-   View & Pure Functions

## Basic Solidity: Arrays & Structs
-   Structs
-   Intro to Storage
-   Arrays 
-   Dynamic & Fixed Sized
-   `push` array function


## Basic Solidity: Compiler Errors and Warnings
- Yellow: Warnings are Ok
- Red: Errors are not Ok

## Memory, Storage, Calldata (Intro)
- 6 Places you can store and access data
  - calldata
  - memory
  - storage
  - code
  - logs
  - stack

## Mappings
- [Mappings]()

## Deploying your First Contract
-   A testnet or mainnet
-   Connecting Metamask
-   [Find a faucet here](https://docs.chain.link/docs/link-token-contracts/#rinkeby)
-   See the faucets at the top of this readme!
-   Interacting with Deployed Contracts

## The EVM & A Recap of Lesson 2
-   The EVM

# Lesson 3: Remix Storage Factory

💻 Code: https://github.com/PatrickAlphaC/storage-factory-fcc

## Introduction
- [Factory Pattern]()

## Basic Solidity: Importing Contracts into other Contracts
- [Composibility]()
- [Solidity new keyword]()
- [Importing Code in solidity]()

## Basic Solidity: Interacting with other Contracts
- To interact, you always need: ABI + Address
- [ABI]()
- [Compilation Details]()

## Basic Solidity: Inheritance & Overrides
- [Inheritance]() 
- [Override Keyword]()
- [Virtual Keyword]()

## Lesson 3 Recap

# Lesson 4: Remix Fund Me

💻 Code: https://github.com/PatrickAlphaC/fund-me-fcc

## Introduction

## Sending ETH Through a Function & Reverts
- [Value Field of a transaction]()
- [Fields in a Transaction]()
- [More on v,r,s]()
- [payable]()
- [msg.value]()
  - [Other global keywords]()
- [require]()
- [revert]()

## Chainlink & Oracles
- [What is a blockchain oracle?](https://chain.link/education/blockchain-oracles)
- [What is the oracle problem?]()
- [Chainlink](https://chain.link/)
- [Chainlink Price Feeds (Data Feeds)](https://docs.chain.link/docs/get-the-latest-price/)
  - [data.chain.link](https://data.chain.link/)
- [Chainlink VRF](https://docs.chain.link/docs/chainlink-vrf/)
- [Chainlink Keepers](https://docs.chain.link/docs/chainlink-keepers/introduction/)
- [Chainlink API Calls](https://docs.chain.link/docs/request-and-receive-data/)
- [Importing Tokens into your Metamask]()
- [Request and Receive Chainlink Model]()

## Review of Sending ETH and working with Chainlink 

## Interfaces & Price Feeds
- [Chainlink Price Feeds (Data Feeds)](https://docs.chain.link/docs/get-the-latest-price/)
- [Chainlink GitHub](https://github.com/smartcontractkit/chainlink) 
- [Interface]()

## Importing from GitHub & NPM
- [Chainlink NPM Package](https://www.npmjs.com/package/@chainlink/contracts)

## Floating Point Math in Solidtiy
- [tuple]()
- [Floating Point Numbers in Solidity]()
- [Type Casting]()
- [Gas Estimation Failed]()

## Basic Solidity: Arrays & Structs II
- [msg.sender]()

## Review of Interfacs, Importing from GitHub, & Math in Solidity

## Libraries
- [Library](https://docs.soliditylang.org/en/v0.8.14/contracts.html?highlight=library#libraries)
- [Solidity-by-example Library](https://solidity-by-example.org/library)

## SafeMath, Overflow Checking, and the "unchecked" keywork
- [Openzeppelin Safemath](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/math/SafeMath.sol)
- [unchecked vs. checked](https://docs.soliditylang.org/en/v0.8.0/control-structures.html#checked-or-unchecked-arithmetic)

## Basic Solidity: For Loop
- [For Loop](https://solidity-by-example.org/loop)
- `/* */` is another way to make comments

## Basic Solidity: Resetting an Array

## Sending ETH from a Contract
- [Transfer, Send, Call](https://solidity-by-example.org/sending-ether/)
- [this keyword]()

## Basic Solidity: Constructor
- [Constructor]()

## Basic Solidity: Modifiers
- [Double equals]()
- [Modifier](https://solidity-by-example.org/function-modifier)

## Testnet Demo
- [Disconnecting Metamask]()
- [Gas Estimation Failed]()

## Advanced Solidity 
### Immutable & Constant
- [Immutable]()
- [Constant]()
- [Current ETH Gas Prices]()
- Don't stress about gas optimizations! (yet)
- [Naming Conventions]()

### Custom Errors
- [Custom Errors Introduction](https://blog.soliditylang.org/2021/04/21/custom-errors/)

### Receive & Fallback Functions
- [Solidity Docs Special Functions](https://docs.soliditylang.org/en/v0.8.14/contracts.html?highlight=fallback#special-functions)
- [Fallback](https://solidity-by-example.org/fallback)
- [Receive](https://docs.soliditylang.org/en/v0.8.14/contracts.html?highlight=fallback#receive-ether-function)

## Lesson 4 Recap

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed Solidity Basics! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

# Lesson 5: Ethers.js Simple Storage

💻 Code: https://github.com/PatrickAlphaC/ethers-simple-storage-fcc

🧪 [Alchemy: https://alchemy.com/?a=673c802981](https://alchemy.com/?a=673c802981)

## Effective Debugging Strategies & Getting Help
1. Tinker and isolate problem
   1. For this course, take at LEAST 15 minutes to figure out a bug.
2. Google / Web Search the Exact problem
   1. Go to this GitHub Repo / Discussions
3. Ask a question on a Forum like Stack Exchange Ethereum or Stack Overflow
   1. Format your questions!!
   2. Use [Markdown]()

### How to Debug Anything Video
- [Patrick's Original Video]()

## Installation & Setup
-   [Visual Studio Code](https://code.visualstudio.com/)
    - [Crash Course](https://www.youtube.com/watch?v=WPqXP_kLzpo)
- [NodeJS](https://nodejs.org/en/)
- [VSCode Keybindings](https://code.visualstudio.com/docs/getstarted/keybindings)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [What is a terminal?](https://code.visualstudio.com/docs/editor/integrated-terminal)

### Mac & Linux Setup

### Windows Setup
- [WSL](https://docs.microsoft.com/en-us/windows/wsl/install)
  - When working in WSL, use Linux commands instead of Windows commands
- [TroubleShooting](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting)
- `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash`

> ⚠️ Please use Gitpod as an absolute last resort
### Gitpod
- [Gitpod]()
  - **If using this, NEVER share a private key with real money on Gitpod**
  - Ideally you figure out the MacOS, Linux, or Windows install though

## Local Development Introduction
- `CMD + K` or `CTRL + K` clears the terminal
- `mkdir ethers-simple-storage-fcc`
- `code .` to open VSCode in a new VSCode window
### Optional Javascript Crash Courses
  - [NodeJS Course](https://www.youtube.com/watch?v=RLtyhwFtXQA)
  - [Javascript Course](https://www.youtube.com/watch?v=jS4aFq5-91M)
- Import your `SimpleStorage.sol`
- [Solidity + Hardhat VSCode Extension]()

- Format your solidity code with: 
```
    "[solidity]": {
        "editor.defaultFormatter": "NomicFoundation.hardhat-solidity"
    },
    "[javascript]":{
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    }
```
In your `.vscode/settings.json` file.
- [Prettier Extension](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
## Tiny Javascript Refresher
- [Javascript Tips]()
## Asynchronous Programming in Javascript
- [Asynchronous Programming](https://www.bmc.com/blogs/asynchronous-programming/)
- [async keyword](https://www.w3schools.com/JS//js_async.asp)
- [Promise in Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- [await keyword](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
## Compiling our Solidity
- [Yarn Install](https://yarnpkg.com/getting-started/install)
- [solc-js](https://github.com/ethereum/solc-js)
  - `yarn add solc@0.8.7-fixed`
- [yarn scripts]()
## Ganache & Networks
- [Ganache](https://trufflesuite.com/ganache/)
- [Networks in Metamask]()
- [RPC URL]()
- [Geth](https://github.com/ethereum/go-ethereum)
- [JSON RPC Spec Playground](https://playground.open-rpc.org/?schemaUrl=https://raw.githubusercontent.com/ethereum/execution-apis/assembled-spec/openrpc.json&uiSchema%5BappBar%5D%5Bui:splitView%5D=false&uiSchema%5BappBar%5D%5Bui:input%5D=false&uiSchema%5BappBar%5D%5Bui:examplesDropdown%5D=false)
## Introduction to Ethers.js
- [Ethers.js](https://docs.ethers.io/v5/getting-started/)
- [prettier-plugin-solidity](https://github.com/prettier-solidity/prettier-plugin-solidity)
### A Note on the await Keyword
## Adding Transaction Overrides
## Transaction Receipts
## Sending a "raw" Transaction in Ethersjs
## Interacting with Contracts in Ethersjs
- [EVM Decompiler](https://ethervm.io/decompile)
- [BigNumber]()
## Environment Variables
- [dotenv](https://www.npmjs.com/package/dotenv)
- [.gitignore]()
## Better Private Key Management
- [wallet.encrypt](https://docs.ethers.io/v5/api/signer/#Wallet-encrypt)
- [THE .ENV PLEDGE](https://github.com/smartcontractkit/full-blockchain-solidity-course-js/discussions/5)
## Optional Prettier Formatting
- [Prettier](https://prettier.io/docs/en/index.html)
- [Best README Template](https://github.com/othneildrew/Best-README-Template)
## Deploying to a Testnet or a Mainnet
- [Alchemy](https://alchemy.com/?a=673c802981)
- [Getting your private key from Metamask]()
- `CTRL + C` stops any terminal command
## Verifying on Block Explorers from the UI
## Alchemy Dashboard & The Mempool
- [Special Guest Albert]()
- [Mempool](https://ethereum.org/en/developers/tutorials/sending-transactions-using-web3-and-alchemy/#see-your-transaction-in-the-mempool)
## Lesson 5 Recap
### Typescript Ethers Simple Storage

# Lesson 6: Hardhat Simple Storage

💻 Code: https://github.com/PatrickAlphaC/hardhat-simple-storage-fcc

## Introduction
## Hardhat Setup
- [Hardhat Documentation](https://hardhat.org/)
- [DevDependencies vs Dependencies](https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies)
- [@ Sign node modules](https://stackoverflow.com/questions/36667258/what-is-the-meaning-of-the-at-prefix-on-npm-packages)

### Troubleshooting Hardaht Setup
## Hardhat Setup Continued
## Deploying SimpleStorage from Hardhat
## Networks in Hardhat
- [The Hardhat Network](https://hardhat.org/hardhat-network/)
- [Hardhat configuration](https://hardhat.org/config/#configuration)
- [Chain ID List](https://chainlist.org/)
## Programatic Verification
- [Etherscan Verify Tutorial](https://docs.etherscan.io/tutorials/verifying-contracts-programmatically)
- [Etherscan Docs](https://docs.etherscan.io/)
- [Hardhat-Etherscan](https://hardhat.org/plugins/nomiclabs-hardhat-etherscan.html)
- [Etherscan API Keys](https://info.etherscan.com/api-keys/)
- [Javascript == vs ===](https://stackoverflow.com/questions/359494/which-equals-operator-vs-should-be-used-in-javascript-comparisons)
## Interacting with Contracts in Hardhat
## Artifacts Troubleshooting
## Custom Hardhat Tasks
- [Hardhat Tasks](https://hardhat.org/guides/create-task.html)
- [Javascript Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_funct ions)
## Hardhat Localhost Node
## The Hardhat Console
- [Hardhat Console](https://hardhat.org/guides/hardhat-console.html)
## Hardhat Tests
- [Hardhat Tests](https://hardhat.org/tutorial/testing-contracts.html#_5-testing-contracts)
- [Mocha Style Tests](https://mochajs.org/)
- [Chai](https://www.npmjs.com/package/chai)
- [Waffle Tests](https://ethereum-waffle.readthedocs.io/en/latest/)
## Hardhat Gas Reporter
- [Hardhat Gas Reporter](https://www.npmjs.com/package/hardhat-gas-reporter)
- [Coinmarketcap API](https://coinmarketcap.com/api/)
## Solidity Coverage
- [Solidity Coverage](https://github.com/sc-forks/solidity-coverage)
## Hardhat Waffle
- [Hardhat-Waffle](https://npm.io/package/@nomiclabs/hardhat-waffle)
## Lesson 6 Recap
### Typescript Hardhat Simple Storage
- [Typechain](https://github.com/dethcrypto/TypeChain)

```
yarn add --dev @typechain/ethers-v5 @typechain/hardhat @types/chai @types/node @types/mocha ts-node typechain typescript
```

# Lesson 7: Hardhat Fund Me

💻 Code: https://github.com/PatrickAlphaC/hardhat-fund-me-fcc

## Introduction
## Hardhat Setup - Fund Me
## Linting
- [Eslint](https://eslint.org/)
- [Solhint](https://github.com/protofire/solhint)
- [Linting Code](https://www.perforce.com/blog/qac/what-lint-code-and-why-linting-important)
## Hardhat Setup - Fund Me - Continued
## Importing from NPM
- [@chainlink/contracts](https://www.npmjs.com/package/@chainlink/contracts)
## Hardhat Deploy
- [Hardhat Deploy](https://github.com/wighawag/hardhat-deploy)
## Mocking
- [Mocking](https://stackoverflow.com/questions/2665812/what-is-mocking)
- [Aave Github](https://github.com/aave/aave-v3-core)
- [Chainlink Github](https://github.com/smartcontractkit/chainlink)
- [Multiple Versions of Solidity]()
- [Tags in hardhat]()
## Utils Folder
## Testnet Demo - Hardhat Fund Me
- [Hardhat Deploy Block Confirmations]()
## Solidity Style Guide
- [Style Guide](https://docs.soliditylang.org/en/v0.8.13/style-guide.html)
- [NatSpec](https://docs.soliditylang.org/en/v0.8.13/natspec-format.html#natspec)
## Testing Fund Me
- [Unit Testing](https://en.wikipedia.org/wiki/Unit_testing)
- [Hardhat Deploy Fixtures]()
- [ethers.getContract]()
- [expect]()
- [ethers.utils.parseUnits]()
- [Waffle Chai Matchers](https://ethereum-waffle.readthedocs.io/en/latest/matchers.html)
## Breakpoints & Debugging
- [VSCode Breakpoints]()
## Gas III: 
- [Transaction Receipt]()
## console.log & Debugging
- [Hardhat console.log](https://hardhat.org/hardhat-network/reference/#console-log)
## Testing Fund Me II
## Storage in Solidity
- [Storage Layout](https://docs.soliditylang.org/en/v0.8.13/internals/layout_in_storage.html)
- [Purpose of the memory keyword](https://stackoverflow.com/questions/33839154/in-ethereum-solidity-what-is-the-purpose-of-the-memory-keyword)
- [getStorageAt]()
## Gas Optimizations using Storage Knowledge
- [Opcodes](https://ethereum.org/en/developers/docs/evm/opcodes/)
- [Opcodes by Gas](https://github.com/crytic/evm-opcodes)
- [Opcodes by Gas](https://evm.codes/)
- Append `s_` to storage variables
- Append `i_` to immutable variables
- Caps lock and underscore constant variables
## Solidity Chainlink Style Guide
- [Chainlink Solidity Style Guide]()
## Storage Review
## Staging Tests
- [Ternary](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)
## Running Scripts on a Local Node
## Adding Scripts to your package.json
## Pushing to GitHub
- [Github Quickstart](https://docs.github.com/en/get-started/quickstart)
- [What is Git?](https://www.git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F)
- [The quickstart that we follow in the video](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git)
- [Learn about git and GitHub](https://www.youtube.com/watch?v=RGOj5yH7evk)
## 🐸🐦 [Tweet Me (add your repo in)!](https://twitter.com/intent/tweet?text=I%20just%20made%20my%20first%20Smart%20Contract%20repo%20using%20@solidity_lang,%20@HardhatHQ,%20@chainlink,%20@AlchemyPlatform,%20and%20more!%0a%0aThanks%20@PatrickAlphaC!!)

# Lesson 8: HTML / Javascript Fund Me (Full Stack / Front End)

💻 Code: https://github.com/PatrickAlphaC/html-fund-me-fcc

## Introduction
## How Websites work with Web3 Wallets
- [OHow to Connect your Smart Contracts to Metamask](https://www.youtube.com/watch?v=pdsYCkUWrgQ)
  - 💻 Code from Video: https://github.com/PatrickAlphaC/full-stack-web3-metamask-connectors
  - ✍️ Article from Video: https://betterprogramming.pub/everything-you-need-to-know-about-fullstack-web3-94c0f1b18019?sk=a2764bcbdae98bf05e1052931de77982
## HTML Setup
- Live Server: ExtensionID: ritwickdey.LiveServer
## Connecting HTML to Metamask
- [Metamask Docs](https://docs.metamask.io/guide/)
## Javascript in it's own file
## ES6 vs Nodejs
- [ES6 vs Nodesjs](https://stackoverflow.com/questions/31354559/using-node-js-require-vs-es6-import-export#31367852)
- [Ethers docs for web browser](https://docs.ethers.io/v5/getting-started/#getting-started--importing--web-browser)
- [module vs text/javascript](https://stackoverflow.com/questions/51418964/script-type-text-javascript-vs-script-type-module)
## Sending a transaction from a Website
- [Web3Provider](https://docs.ethers.io/v5/api/providers/other/#Web3Provider)
- [Adding a network to metamask]()
- [Importing a private key to metamask]()
## Resetting an Account in Metamask
```
MetaMask - RPC Error:
[ethjs-query] while formatting ouputs from RPC '{"value":{"code":-32603,"data":{"code":-32000,"message":"Nonce too high. Expected nonce to be 2 but got 4. Note that transactions can't be queued when automining."}}}'
```
## Listening for Events and Completed Transactions
- [provider.once](https://docs.ethers.io/v5/api/providers/provider/#Provider-once)
- [Anonymous function](https://www.geeksforgeeks.org/javascript-anonymous-functions/)
- [Javascript Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
## Input Forms
## Reading from the Blockchain
## Withdraw Function
## Lesson 8 Recap
### Optional Links:
- [Browserify](https://browserify.org/)
- [Watchify](https://www.npmjs.com/package/watchify)

# Lesson 9: Hardhat Smart Contract Lottery

💻 Code: https://github.com/PatrickAlphaC/hardhat-smartcontract-lottery-fcc

## Introduction
## Hardhat Setup - Smart Contract Lottery
- Install dependencies:
```bash
yarn add --dev @nomiclabs/hardhat-ethers@npm:hardhat-deploy-ethers ethers @nomiclabs/hardhat-etherscan @nomiclabs/hardhat-waffle chai ethereum-waffle hardhat hardhat-contract-sizer hardhat-deploy hardhat-gas-reporter prettier prettier-plugin-solidity solhint solidity-coverage dotenv
```
## Raffle.sol Setup
- [Custom Errors in Solidity](https://blog.soliditylang.org/2021/04/21/custom-errors/)
## Introduction to Events
- [Events and Logging](https://www.youtube.com/watch?v=KDYJC85eS5M)
- [Events & Logging Video](https://www.youtube.com/watch?v=KDYJC85eS5M)
- [Events & Logging in Hardhat](https://github.com/PatrickAlphaC/hardhat-events-logs)
## Events in Raffle.sol
## Introduction to Chainlink VRF
### Sub-Lesson: Chainlink VRF
> - [Chainlink VRFv2 Docs](https://docs.chain.link/docs/get-a-random-number/)
> - [Chainlink VRFv2 Walkthrough](https://www.youtube.com/watch?v=rdJ5d8j1RCg)
> - [Chainlink Contracts](https://github.com/smartcontractkit/chainlink/blob/develop/contracts/src/v0.8/VRFConsumerBase.sol)
## Implementing Chainlink VRF - Introduction
### Hardhat Shorthand
- [Hardhat Shorthand](https://hardhat.org/guides/shorthand.html)
## Implementing Chainlink VRF - The Request
## Implementing Chainlink VRF - The FulFill
### Modulo
- [Modulo](https://docs.soliditylang.org/en/v0.8.13/types.html?highlight=modulo#modulo)
## Introduction to Chainlink Keepers
- [Chainlink Keepers Docs](https://docs.chain.link/docs/chainlink-keepers/introduction/)
- [Chainlink Keepers Walkthrough](https://www.youtube.com/watch?v=-Wkw5JVQGUo)
## Implementing Chainlink Keepers - checkUpkeep
### Enums
- [Enum](https://docs.soliditylang.org/en/v0.8.13/structure-of-a-contract.html?highlight=enum#enum-types)
## Implementing Chainlink Keepers - checkUpkeep continued
- [block.timestamp]()
## Implementing Chainlink Keepers - performUpkeep
## Code Cleanup
## Deploying Raffle.sol
### Mock Chainlink VRF Coordinator
### Continued
- [LINK Token]()
## Raffle.sol Unit Tests
- We use `async function` in the describe blocks at the start, but we correctly take them out later. 
### Testing Events & Chai Matchers
- [Emit Chai Matcher](https://ethereum-waffle.readthedocs.io/en/latest/matchers.html#emitting-events)
### Continued I
## Hardhat Methods & Time Travel
- [Make Hardhat do whatever you want it to](https://hardhat.org/hardhat-network/reference/)
- [Special debugging hardhat methods](https://hardhat.org/hardhat-network/reference/#special-testing-debugging-methods)
### Continued II
## Callstatic
- [Callstatic]()
### Continued III
### Massive Promise Test
### Continued IV
## Raffle.sol Staging Tests
## Testing on a Testnet
### Recommended LINK amounts for Rinkeby Staging Test:
- Chainlink VRF: 2 LINK
- Chainlink Keepers: 8 LINK
## Conclusion
## Typescript - Smart Contract Lottery

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed Hardhat Basics! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

# Lesson 10: NextJS Smart Contract Lottery (Full Stack / Front End)

💻 Code: https://github.com/PatrickAlphaC/nextjs-smartcontract-lottery-fcc

⚡️⚡️ Live Demo IPFS: ipfs://QmXwACyjcS8tL7UkYwimpqMqW9sKzSHUjE4uSZBSyQVuEH

⚡️⚡️ Live Demo Fleek: https://fancy-dream-3458.on.fleek.co/

## Introduction
We move into using [NextJS](https://nextjs.org/) for our front end. NextJS is a [React framework](https://reactjs.org/) for building websites. 

### Optional Sub-Lesson: Full Stack Development & Other Libraries
- [6 Ways to connect your dapp to a wallet](https://www.youtube.com/watch?v=pdsYCkUWrgQ)
- [NextJS Crash Course](https://www.youtube.com/watch?v=mTz0GXj8NN0)
- Other React libraries:
  - [Web3React](https://github.com/NoahZinsmeister/web3-react)
  - [wagmi](https://github.com/tmm/wagmi)
  - [react-moralis](https://www.npmjs.com/package/react-moralis)
  - [useDapp](https://github.com/TrueFiEng/useDApp)
  - [Web3Modal](https://github.com/Web3Modal/web3modal)
  - [useMetamask](https://github.com/mdtanrikulu/use-metamask)
- Other Full Stack Web3 Templates
  - [scaffold-eth](https://github.com/scaffold-eth/scaffold-eth)
  - [ethereum-boilerplate](https://github.com/ethereum-boilerplate/ethereum-boilerplate)
  - [create-eth-app](https://github.com/paulrberg/create-eth-app)
- [React being quite popular](https://insights.stackoverflow.com/survey/2021#section-most-popular-technologies-web-frameworks)
- [Why use react?](https://www.freecodecamp.org/news/why-use-react-for-web-development/)

## NextJS Setup
- [NextJS Documentation](https://nextjs.org/learn/basics/create-nextjs-app)
- [NextJS Minimal Ethers Example For Lottery](https://github.com/PatrickAlphaC/nextjs-ethers-introduction)

```
yarn create next-app .
```
## Manual Header I
- [What is a component?](https://www.w3schools.com/react/react_components.asp)
- [jsx]()
- [Moralis](https://moralis.io/)
- [React Moralis](https://github.com/MoralisWeb3/react-moralis)
### React Hooks
- [What is a react hook?](https://reactjs.org/docs/hooks-overview.html)
## Manual Header II
## useEffect Hook
- [useEffect Hook](https://reactjs.org/docs/hooks-effect.html)
- [More on useEffect](https://blog.logrocket.com/guide-to-react-useeffect-hook/)
- [React Context]()
  - [useEffect Firing Twice](https://stackoverflow.com/questions/60618844/react-hooks-useeffect-is-called-twice-even-if-an-empty-array-is-used-as-an-ar)
## Local Storage
- [Local Storage]()
## isWeb3EnabledLoading
## web3uikit
- [web3uikit](https://github.com/web3ui/web3uikit)
- [web3uikit interactive docs](https://web3ui.github.io/web3uikit/?path=/story/1-web3-blockie--custom-seed)
- [web3uikit connect button](https://web3ui.github.io/web3uikit/?path=/story/1-web3-connectbutton--default)
## Introduction to Calling Functions in Nextjs
- [useWeb3Contract]()
### Automatic Constant Value UI Updater
- [ethers.utils.FormatTypes]()
### runContractFunction
- [Moralis Provider]()
- [useMoralis]()
- [parseInt]()
## useState
- [useState Hook](https://reactjs.org/docs/hooks-state.html)
## Calling Functions in NextJS
## useNotification
- Add `onError` to all your `runContractFunction` calls
## Reading & Displaying Contract Data
## A Note about `onSuccess`
- `onSuccess` just checks to see if MetaMask sends the transaction, not 
## A Challenge to You
## Tailwind & Styling
- [Learn CSS](https://www.w3schools.com/css/)
- [Tailwindcss](https://tailwindcss.com/)
- [PostCSS Extension](https://marketplace.visualstudio.com/items?itemName=csstools.postcss)
- [Tailwind Extension](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)
- [Install Tailwind into NextJS](https://tailwindcss.com/docs/guides/nextjs)
## Introduction to Hosting your Site
- [Vercel]()
- [Moralis]()
- [Netilfy]()
- [IPFS](https://ipfs.io/)
## IPFS
- [What is IPFS](https://www.youtube.com/watch?v=5Uj6uR3fp-U)
- [IPFS](https://ipfs.io/)
## Hosting on IPFS
- [IPFS Companion](https://chrome.google.com/webstore/detail/ipfs-companion/nibjojkomfdiaoajekhjakgkdhaomnch)
- [Brave Browser](https://brave.com/)
- `yarn build && yarn next export`
## Hosting on IPFS & Filecoin using Fleek
- [Fleek](https://fleek.co/)
## Filecoin Overview
- [IPFS URL of Ally's Video](ipfs://bafybeiasd6oxqiefoxgtskrokomexnb4zcq3fhwlcbyplx2paw65zmq2du)
## Lesson 10 Recap

# Lesson 11: Hardhat Starter Kit

💻 Code: https://github.com/smartcontractkit/hardhat-starter-kit

# Lesson 12: Hardhat ERC20s

💻 Code: https://github.com/PatrickAlphaC/hardhat-erc20-fcc

## What is an ERC? What is an EIP?
- [What is an EIP?](https://eips.ethereum.org/)
- [EIPs codebase](https://github.com/ethereum/EIPs)
## What is an ERC20?
- [Video (using brownie/python)](https://youtu.be/8rpir_ZSK1g?t=39)
- [EIP-20](https://eips.ethereum.org/EIPS/eip-20)
- [ERC-677](https://github.com/ethereum/EIPs/issues/677)
- [EIP-777](https://eips.ethereum.org/EIPS/eip-777)
## Manually Creating an ERC20 Token
## Creating an ERC20 Token with Openzeppelin
- [Openzeppelin](https://openzeppelin.com/)
- [Openzeppelin Contracts](https://github.com/OpenZeppelin/openzeppelin-contracts)
- [Solmate (Openzeppelin alternative)](https://github.com/Rari-Capital/solmate)
## Lesson 12 Recap

# Lesson 13: Hardhat DeFi & Aave

💻 Code: https://github.com/PatrickAlphaC/hardhat-defi-fcc

## What is DeFi?
- [What is DeFi?](https://chain.link/education/defi)
- [DefiLlama](https://defillama.com/)
## What is Aave?
- [Aave](https://aave.com/)
- [My Previous Aave Video on Shorting Assets](https://www.youtube.com/watch?v=TmNGAvI-RUA)
## Programatic Borrowing & Lending
- [DAI](https://makerdao.com/en/)
- [Uniswap](https://app.uniswap.org/)
## WETH - Wrapped ETH
- [WETH Token Rinkeby Etherscan](https://rinkeby.etherscan.io/token/0xc778417e063141139fce010982780140aa0cd5ab#writeContract)
- [WETH Token Mainnet](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2)
## Forking Mainnet
- [Mainnet Forking](https://hardhat.org/hardhat-network/guides/mainnet-forking.html)
## Depositing into Aave
- [Aave V2 Docs](https://docs.aave.com/developers/v/2.0/)
- [Aave NPM](https://www.npmjs.com/package/@aave/protocol-v2)
## Borrowing from Aave
- [Aave Borrowing FAQs](https://docs.aave.com/faq/borrowing)
- [Health Factor](https://docs.aave.com/faq/borrowing#what-is-the-health-factor)
- [Aave Risk Parameters](https://docs.aave.com/risk/asset-risk/risk-parameters)
## Repaying with Aave 
## Visualizing the Transactions
- [aTokens](https://docs.aave.com/developers/v/1.0/developing-on-aave/the-protocol/atokens)
## Lesson 13 Recap
## Happy Bow-Tie Friday with Austin Griffith
- [Austin Griffith](https://twitter.com/austingriffith)!
- [Speed Run Ethereum](https://speedrunethereum.com/) 
### More DeFi Learnings: 
- [Speed Run Ethereum](https://speedrunethereum.com/)
- [Defi-Minimal](https://github.com/smartcontractkit/defi-minimal/tree/main/contracts)
- [Defi Dad](https://www.youtube.com/channel/UCatItl6C7wJp9txFMbXbSTg)


# Lesson 14: Hardhat NFTs (EVERYTHING you need to know about NFTs)

💻 Code: https://github.com/PatrickAlphaC/hardhat-nft-fcc

## What is an NFT? 
- [Video](https://www.youtube.com/watch?v=9yuHz6g_P50)
- [Optional: All on Chain SVG NFT](https://www.youtube.com/watch?v=9oERTH9Bkw0)
- [EIP-721]()
## Code Overview
- [Opensea Testnet]()
## Hardhat Setup
## Basic NFT
### Write Tests 
- [Openzeppelin NFT](https://docs.openzeppelin.com/contracts/4.x/)
## Random IPFS NFT
### Mapping Chainlink VRF Requests
### Creating Rare NFTs
### Setting the NFT Image
### Setting an NFT Mint Price
### Deploy Script
### Uploading Token Images with Pinata
- [Pinata](https://pinata.cloud)
- [nft.storage](https://nft.storage)
- [Pinata NPM]()
- [Pinata Docs]()
### Uploading Token URIs (metadata) with Pinata
### Deploying
### Tests
## Dynamic SVG On-Chain NFT
- [Patrick's Original Video]()
### What is an SVG?
- [SVG Tutorial](https://www.w3schools.com/graphics/svg_intro.asp)
  - [On-Chain SVG Example](https://opensea.io/assets/matic/0x291ff90b9c410f56e047599bfee6b585c0c484d7/2)
### Initial Code  
### Base64 Encoding
- [Base64 Encoding](https://en.wikipedia.org/wiki/Base64)
  - [Example Encoder](https://base64.guru/converter/encode/image/svg)
- [base64-sol]()
## Advanced: EVM Opcodes, Encoding, and Calling
### abi.encode & abi.encodePacked
- [abi.encode]()
- [abi.encodePacked]()
Thanks to [Alex Roan](https://twitter.com/alexroan) for his help on this session!
- [Example Contract Creation Transaction](https://rinkeby.etherscan.io/tx/0x924f592458b0e37ee17024f9c826b97697455cd97f6946b802bc42296e77ae43)
What REALLY is the ABI?
- [EVM Opcodes](https://www.evm.codes/)
- [More EVM Opcodes](https://github.com/crytic/evm-opcodes)
- [Solidity Cheatsheet](https://docs.soliditylang.org/en/v0.8.13/cheatsheet.html?highlight=encodewithsignature)
- [abi.encode vs abi.encodePacked](https://ethereum.stackexchange.com/questions/91826/why-are-there-two-methods-encoding-arguments-abi-encode-and-abi-encodepacked)
### Introduction to Encoding Function Calls Directly
### Introduction to Encoding Function Calls Recap
### Encoding Function Calls Directly
- [Function Selector]()
- [Function Signature]() 
### Creating an NFT TokenURI on-Chain
### Making the NFT Dynamic
### Deploy Script
## Deploying the NFTs to a Testnet
## Lesson 14 Recap


Extra credit:
  - [Deconstructing Solidity](https://blog.openzeppelin.com/deconstructing-a-solidity-contract-part-ii-creation-vs-runtime-6b9d60ecb44c/)
  - [Knowing and controlling your Smart Contract Address](https://www.youtube.com/watch?v=RxL_1AfV7N4)
  - [From Solidity to byte code](https://www.youtube.com/watch?v=RxL_1AfV7N4)

# Lesson 15: NextJS NFT Marketplace (If you finish this lesson, you are a full-stack MONSTER!)

💻 Code: 
 - Backend (Contracts): https://github.com/PatrickAlphaC/hardhat-nft-marketplace-fcc
 - Frontend (Moralis Indexer): https://github.com/PatrickAlphaC/nextjs-nft-marketplace-moralis-fcc
 - Frontend (TheGraph Indexer): https://github.com/PatrickAlphaC/nextjs-nft-marketplace-thegraph-fcc    
   - The Graph: https://github.com/PatrickAlphaC/graph-nft-marketplace-fcc  

Special thanks to [Matt]() for help with this section. 

## Introduction
- [Opensea]()
- [Artion](https://github.com/Fantom-foundation/Artion-Contracts)
## Part I: NFT Marketplace Contracts
### Hardhat Setup
### NftMarketplace.sol
- [Pull Over Push]()
## Reentrancy
- [Reentrancy](https://solidity-by-example.org/hacks/re-entrancy)
- [Rekt.news](https://rekt.news/leaderboard/)
- [Openzeppelin NonReentrant]()
### NftMarketplace.sol - Continued
### NftMarketplace.sol - Deploy Script
### NftMarketplace.sol - Tests
### NftMarketplace.sol - Scripts

## Part II: Moralis Front End
### What is Moralis?
- [Special Guest Ivan]()
### NextJS Setup
- [Link NextJS](https://nextjs.org/docs/api-reference/next/link)
### Adding Tailwind
- [Tailwind with NextJS](https://tailwindcss.com/docs/guides/nextjs)
### Introduction to Indexing in Web3
- [TheGraph]()
- [Moralis](https://moralis.io/)
### Connecting Moralis to our Local Hardhat Node
- [NextJS Environment Variables](https://nextjs.org/docs/basic-features/environment-variables)
- [Reverse Proxy FRP](https://github.com/fatedier/frp/releases)
  - [Docs](https://docs.moralis.io/moralis-dapp/web3/setting-up-ganache)
  - [Trouble Shooting](https://docs.moralis.io/faq#frpc)
- [Moralis Forum](https://forum.moralis.io/)
- [Moralis Admin CLI](https://docs.moralis.io/moralis-dapp/tools/moralis-admin-cli)
### Moralis Event Sync
- [Moralis Add Event Sync From Code](https://docs.moralis.io/moralis-dapp/connect-the-sdk/connect-using-node#add-new-event-sync-from-code)
#### Reset Local Chain
### Moralis Cloud Functions
- [Moralis Cloud Functions](https://docs.moralis.io/moralis-dapp/cloud-code/cloud-functions)
- [Moralis Logging](https://docs.moralis.io/moralis-dapp/tools/moralis-admin-cli#get-logs)
- [Hardhat Network Reference](https://hardhat.org/hardhat-network/reference/)
- Moralis Database only confirms a transaction with a block confirmation - so we need to move blocks on our hardhat local node. 
- [Moralis Triggers]()
#### Practice Resetting the Local Chain
### Moralis Cloud Functions II
### Querying the Moralis Database
- [Moralis Queries](https://docs.moralis.io/moralis-dapp/database/queries)
### Rendering the NFT Images
- [useNFTBalance]()
- [fetch]()
- [next/image]()
### Update Listing Modal
### Buy NFT Listing
### Listing NFTs for Sale
- [web3uikit Form]()

## Part III: TheGraph Front End
### Introduction
### What is The Graph? 
- [Special Guest Nader Dabit]()
### Building a Subgraph
- [Example Subgraphs]()
- [The Graph Studio]()
- [GraphQL VSCode Extension]()
- [GraphQL](https://graphql.org/)
### Deploying our Subgraph
- [GraphQL Queries](https://www.tutorialspoint.com/graphql/graphql_query.htm)
### Reading from The Graph
- [@apollo/client](https://www.npmjs.com/package/@apollo/client)
- [gql]()
- [The Graph Docs](https://thegraph.com/docs/en/)
### Hosting our Dapp
- [Hosting on Moralis](https://moralis.io/how-to-host-a-dapp-dapp-hosting-explained/)
- [Vercel]()
- [Netilfy]()

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed Front End Basics! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

# Lesson 16: Hardhat Upgrades

💻 Code: https://github.com/PatrickAlphaC/hardhat-upgrades-fcc

## Upgradeable Smart Contracts Overview
- [Optional Video](https://www.youtube.com/watch?v=bdXJmWajZRY)
- [Links from Video]
## Types of Upgrades
1.  Parameter
2.  Social Migrate
3.  Proxy
    1.  Proxy Gotchas
        1. [Function Collisions]()
        2. [Storage Collisions]()
    2.  [Metamorphic Upgrades](https://github.com/PatrickAlphaC/hardhat-metamorphic-upgrades-fcc)
    3.  [Transparent]()
    4.  [UUPS]()
    5.  [Diamond]()
## Delegatecall
- [delegatecall (solidity-by-example)](https://solidity-by-example.org/delegatecall)
- [Yul](https://docs.soliditylang.org/en/latest/yul.html)
## Small Proxy Example
- [EIP 1967](https://eips.ethereum.org/EIPS/eip-1967)
## Transparent Upgradeable Smart Contract 
- [Hardhat-deploy Proxies](https://github.com/wighawag/hardhat-deploy#deploying-and-upgrading-proxies)
- [Openzeppelin Upgrades Plugin](https://docs.openzeppelin.com/upgrades-plugins/1.x/)
  - [Openzeppelin upgrades tutorial](https://forum.openzeppelin.com/t/openzeppelin-upgrades-step-by-step-tutorial-for-hardhat/3580)
- [hardhat deploy upgrades examples](https://github.com/wighawag/template-ethereum-contracts/tree/examples/openzeppelin-proxies/deploy)


# Lesson 17: Hardhat DAOs

⬆️ Up-to-date code: https://github.com/PatrickAlphaC/dao-template

💻 Code from video: https://github.com/PatrickAlphaC/hardhat-dao-fcc

## Introduction
## What is a DAO?
- [What is a DAO?](https://www.youtube.com/watch?v=X_QKZzd68ro)
## How to build a DAO
- [How to build a DAO](https://www.youtube.com/watch?v=AhJtmUqhAqg)
- [That's Patrick]()
- [PY Code](https://github.com/brownie-mix/dao-mix)
- [Python Video](https://www.youtube.com/watch?v=rD8AxZ_wBA4)
- [Openzeppelin Governance](https://docs.openzeppelin.com/contracts/4.x/api/governance)
- [Compound Governance](https://compound.finance/governance)
- [Contract Wizard](https://docs.openzeppelin.com/contracts/4.x/wizard)
- [CastVoteBySig](https://forum.openzeppelin.com/t/what-is-votecastbysig/17069/2)

# Lesson 18: Security & Auditing

💻 Code: https://github.com/PatrickAlphaC/hardhat-security-fcc

## Introduction
- [Readiness Guide](https://learn.openzeppelin.com/security-audits/readiness-guide)
## Slither
- [Install python](https://www.python.org/downloads/)
- [Slither](https://github.com/crytic/slither#how-to-install)
- [solc-select](https://github.com/crytic/solc-select)
- [Fuzz testing](https://en.wikipedia.org/wiki/Fuzzing)
## Fuzzing and Eth Security Toolbox
- [Echidna](https://github.com/crytic/echidna)
- [Docker Install](https://docs.docker.com/get-docker/)
- [Eth-Security-ToolBox](https://github.com/trailofbits/eth-security-toolbox)
## Closing Thoughts
-   [Best Practices](https://consensys.github.io/smart-contract-best-practices/)
-   [Attacks](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
    -   [Oracle Attacks](https://hackernoon.com/how-dollar100m-got-stolen-from-defi-in-2021-price-oracle-manipulation-and-flash-loan-attacks-explained-3n6q33r1)
    -   [Re-entrancy Attacks](https://quantstamp.com/blog/what-is-a-re-entrancy-attack)
-   [Damn Vulnerable Defi](https://www.damnvulnerabledefi.xyz/)
-   [Ethernaut](https://ethernaut.openzeppelin.com/)
-   Some Auditors:
    -   [OpenZeppelin](https://openzeppelin.com/)
    -   [SigmaPrime](https://sigmaprime.io/)
    -   [Trail of Bits](https://www.trailofbits.com/)

# Congratulations

🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 Completed The Course! 🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊🎊 

## Where do I go now?

### Learning More

-   [CryptoZombies](https://cryptozombies.io/)
-   [Patrick Collins](https://www.youtube.com/channel/UCn-3f8tw_E1jZvhuHatROwA)
-   [Dapp University](https://www.youtube.com/channel/UCY0xL8V6NzzFcwzHCgB8orQ)
-   [ChainShot](https://www.chainshot.com/courses)
-   [Ivan on Tech](https://academy.ivanontech.com/)
-   [Cami]()
-   [Albert]()
-   [Ally]()
-   [Eat the Blocks](https://www.youtube.com/channel/UCZM8XQjNOyG2ElPpEUtNasA)
-   [Austin Griffith](https://www.youtube.com/channel/UC_HI2i2peo1A-STdG22GFsA)
-   [Nader Dabit](https://www.youtube.com/user/boyindasouth)
-   [Ethereum.org](https://ethereum.org/en/)

### Community

-   [Twitter](https://twitter.com/PatrickAlphaC)
-   [Hardhat Discord](https://discord.gg/9zk7snTfWe)
-   [Chainlink Discord](https://discord.gg/2YHSAey)
-   [Ethereum Discord](https://ethereum.org/en/)
-   [Reddit ethdev](https://www.reddit.com/r/ethdev/)

### Hackathons

-   [CL Hackathon](https://chain.link/hackathon)
-   [ETH Global](https://ethglobal.co/)
-   [ETH India](https://twitter.com/ETHIndiaco)

Be sure to check out project grant programs!

And make today an amazing day!


