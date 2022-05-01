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
- [Lesson 0: The Edge of the Rabbit Hole](#lesson-0-the-edge-of-the-rabbit-hole)
- [Lesson 1: Blockchain Basics](#lesson-1-blockchain-basics)
  - [What is a Blockchain?](#what-is-a-blockchain)
  - [Making Your First Transaction](#making-your-first-transaction)
  - [How Do Blockchains Work?](#how-do-blockchains-work)
    - [Consensus](#consensus)
- [Lesson 2: Welcome to Remix! Simple Storage](#lesson-2-welcome-to-remix-simple-storage)
    - [Everything in this section can be read about in the Solidity Documentation](#everything-in-this-section-can-be-read-about-in-the-solidity-documentation)
    - [Remix](#remix)
    - [Basic Solidity](#basic-solidity)
    - [Deploying to a "Live" network](#deploying-to-a-live-network)
- [Lesson 3: Remix Storage Factory](#lesson-3-remix-storage-factory)
- [Lesson 4: Remix Fund Me](#lesson-4-remix-fund-me)
- [Lesson 5: Ethers.js Simple Storage](#lesson-5-ethersjs-simple-storage)
  - [Installation & Setup!](#installation--setup)
- [Lesson 6: Hardhat Simple Storage](#lesson-6-hardhat-simple-storage)
- [Lesson 7: Hardhat Fund Me](#lesson-7-hardhat-fund-me)
- [Lesson 8: HTML / Javascript Fund Me (Full Stack / Front End)](#lesson-8-html--javascript-fund-me-full-stack--front-end)
- [Lesson 9: Hardhat Smart Contract Lottery](#lesson-9-hardhat-smart-contract-lottery)
    - [Sub-Lesson: Events & Logging](#sub-lesson-events--logging)
    - [Sub-Lesson: Chainlink VRF](#sub-lesson-chainlink-vrf)
    - [Sub-Lesson: Chainlink Keepers](#sub-lesson-chainlink-keepers)
    - [Recommended LINK amounts for Rinkeby Staging Test:](#recommended-link-amounts-for-rinkeby-staging-test)
- [Lesson 10: NextJS Smart Contract Lottery (Full Stack / Front End)](#lesson-10-nextjs-smart-contract-lottery-full-stack--front-end)
    - [Optional Sub-Lesson: Full Stack Development & Other Libraries](#optional-sub-lesson-full-stack-development--other-libraries)
    - [The Rest of this Lesson](#the-rest-of-this-lesson)
- [Lesson 11: Hardhat Starter Kit](#lesson-11-hardhat-starter-kit)
- [Lesson 12: Hardhat ERC20s](#lesson-12-hardhat-erc20s)
    - [Sub-Lesson: What is an ERC20?](#sub-lesson-what-is-an-erc20)
    - [Rest of the Lesson](#rest-of-the-lesson)
- [Lesson 13: Hardhat DeFi & Aave](#lesson-13-hardhat-defi--aave)
- [Lesson 14: Hardhat NFTs (EVERYTHING you need to know about NFTs)](#lesson-14-hardhat-nfts-everything-you-need-to-know-about-nfts)
    - [Sublesson: What is an NFT?](#sublesson-what-is-an-nft)
    - [Hardhat NFTs Part 1](#hardhat-nfts-part-1)
    - [Sublesson: EVM Opcodes, Encoding, and Calling](#sublesson-evm-opcodes-encoding-and-calling)
- [Lesson 15: NextJS NFT Marketplace (If you finish this lesson, you are a full-stack MONSTER!)](#lesson-15-nextjs-nft-marketplace-if-you-finish-this-lesson-you-are-a-full-stack-monster)
    - [TheGraph](#thegraph)
- [Lesson 16: Hardhat Upgrades](#lesson-16-hardhat-upgrades)
  - [Types of Upgrades](#types-of-upgrades)
- [Lesson 17: Hardhat DAOs](#lesson-17-hardhat-daos)
- [Lesson 18: Security & Auditing](#lesson-18-security--auditing)
  - [Where do I go now?](#where-do-i-go-now)
    - [Learning More](#learning-more)
    - [Community](#community)
    - [Hackathons](#hackathons)

# Lesson 0: The Edge of the Rabbit Hole

-   Welcome to the course!
-   Why do you want to embark on this journey?
-   Best Practices

# Lesson 1: Blockchain Basics

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
-   Advanced Gas
    -   [EIP 1559](https://www.youtube.com/watch?v=MGemhK9t44Q)
    -   GWEI, WEI, and ETH
        -   [ETH Converter](https://eth-converter.com/)
-   [Run Your Own Ethereum Node](https://geth.ethereum.org/docs/getting-started)

### Consensus

-   [Consensus](https://wiki.polkadot.network/docs/learn-consensus)
-   [Proof of Stake](https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/)
-   [Proof of Work](https://ethereum.org/en/developers/docs/consensus-mechanisms/pow/)
-   [Nakamoto Consensus](https://blockonomi.com/nakamoto-consensus/)
-   [Ethereum 2 (the merge)](https://ethereum.org/en/eth2/)

# Lesson 2: [Welcome to Remix! Simple Storage](https://github.com/PatrickAlphaC/simple-storage-fcc)

💻 Code: https://github.com/PatrickAlphaC/simple-storage-fcc

### Everything in this section can be read about in the [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.6/index.html)

### [Remix](https://remix.ethereum.org/)

### Basic Solidity

-   Versioning
-   Compiling
-   Contract Declaration
-   [Types & Declaring Variables](https://docs.soliditylang.org/en/v0.8.13/)
    -   `uint256`, `int256`, `bool`, `string`, `address`, `bytes32`
    -   [Bits and Bytes](https://www.youtube.com/watch?v=Dnd28lQHquU)
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

# Lesson 3: Remix Storage Factory

💻 Code: https://github.com/PatrickAlphaC/storage-factory-fcc

# Lesson 4: Remix Fund Me

💻 Code: https://github.com/PatrickAlphaC/fund-me-fcc

-   [Transfer, Send, Call](https://solidity-by-example.org/sending-ether/)

# Lesson 5: Ethers.js Simple Storage

## Installation & Setup!

-   [Visual Studio Code](https://code.visualstudio.com/)
    - [Crash Course](https://www.youtube.com/watch?v=WPqXP_kLzpo)
- [NodeJS](https://nodejs.org/en/)
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Windows Only:
- [WSL](https://docs.microsoft.com/en-us/windows/wsl/install)
- [TroubleShooting](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting)

💻 Code: https://github.com/PatrickAlphaC/ethers-simple-storage-fcc

- [NodeJS Course](https://www.youtube.com/watch?v=RLtyhwFtXQA)
- [Javascript Course](https://www.youtube.com/watch?v=jS4aFq5-91M)
- Format your solidity code with: 
```
    "[solidity]": {
        "editor.defaultFormatter": "NomicFoundation.hardhat-solidity"
    },
```
In your `.vscode/settings.json` file.
- [Yarn](https://yarnpkg.com/getting-started/install)
- [Ganache](https://trufflesuite.com/ganache/)
- [EthersJS](https://docs.ethers.io/v5/getting-started/)
- [prettier-plugin-solidity](https://github.com/prettier-solidity/prettier-plugin-solidity)
- [Alchemy](https://alchemy.com/?a=673c802981)

More information:
- [JSON RPC Spec](https://playground.open-rpc.org/?schemaUrl=https://raw.githubusercontent.com/ethereum/execution-apis/assembled-spec/openrpc.json&uiSchema%5BappBar%5D%5Bui:splitView%5D=false&uiSchema%5BappBar%5D%5Bui:input%5D=false&uiSchema%5BappBar%5D%5Bui:examplesDropdown%5D=false)

# Lesson 6: Hardhat Simple Storage

💻 Code: https://github.com/PatrickAlphaC/hardhat-simple-storage-fcc

- [Hardhat Documentation](https://hardhat.org/)
- [DevDependencies vs Dependencies](https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies)
- [@ Sign node modules](https://stackoverflow.com/questions/36667258/what-is-the-meaning-of-the-at-prefix-on-npm-packages)
- [Chain ID List](https://chainlist.org/)
- [Etherscan Verify Tutorial](https://docs.etherscan.io/tutorials/verifying-contracts-programmatically)
- [Javascript == vs ===](https://stackoverflow.com/questions/359494/which-equals-operator-vs-should-be-used-in-javascript-comparisons)
- [Hardhat Gas Reporter](https://www.npmjs.com/package/hardhat-gas-reporter)
- [Coinmarketcap API](https://coinmarketcap.com/api/)
- [Best README Template](https://github.com/othneildrew/Best-README-Template)
- [Hardhat-Waffle](https://npm.io/package/@nomiclabs/hardhat-waffle)

Typescript:
- [Typechain](https://github.com/dethcrypto/TypeChain)
```
yarn add --dev @typechain/ethers-v5 @typechain/hardhat @types/chai @types/node @types/mocha ts-node typechain typescript
```

# Lesson 7: Hardhat Fund Me

💻 Code: https://github.com/PatrickAlphaC/hardhat-fund-me-fcc

- [Eslint](https://eslint.org/)
- [Solhint](https://github.com/protofire/solhint)
- [Linting Code](https://www.perforce.com/blog/qac/what-lint-code-and-why-linting-important)
- [Hardhat Deploy](https://github.com/wighawag/hardhat-deploy)
- [Mocking](https://stackoverflow.com/questions/2665812/what-is-mocking)
- [Aave Github](https://github.com/aave/aave-v3-core)
- [Chainlink Github](https://github.com/smartcontractkit/chainlink)
- [Style Guide](https://docs.soliditylang.org/en/v0.8.13/style-guide.html)
- [NatSpec](https://docs.soliditylang.org/en/v0.8.13/natspec-format.html#natspec)
- [Unit Testing](https://en.wikipedia.org/wiki/Unit_testing)
- [Waffle Chai Matchers](https://ethereum-waffle.readthedocs.io/en/latest/matchers.html)
- [Storage Layout](https://docs.soliditylang.org/en/v0.8.13/internals/layout_in_storage.html)
- [Purpose of the memory keyword](https://stackoverflow.com/questions/33839154/in-ethereum-solidity-what-is-the-purpose-of-the-memory-keyword)
- [Opcodes by Gas](https://github.com/crytic/evm-opcodes)
- [Ternary](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)
- [Github Quickstart](https://docs.github.com/en/get-started/quickstart)
  - [The quickstart that we follow in the video](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git)
  - [Learn about git and GitHub](https://www.youtube.com/watch?v=RGOj5yH7evk)

# Lesson 8: HTML / Javascript Fund Me (Full Stack / Front End)

💻 Code: https://github.com/PatrickAlphaC/html-fund-me-fcc

- Live Server: ExtensionID: ritwickdey.LiveServer
- [Metamask Docs](https://docs.metamask.io/guide/)
- [Web3Provider](https://docs.ethers.io/v5/api/providers/other/#Web3Provider)
- [Browserify](https://browserify.org/)
- [Watchify](https://www.npmjs.com/package/watchify)
- [Javascript Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

# Lesson 9: Hardhat Smart Contract Lottery

💻 Code: https://github.com/PatrickAlphaC/hardhat-smartcontract-lottery-fcc

- Install dependencies:
```bash
yarn add --dev @nomiclabs/hardhat-ethers@npm:hardhat-deploy-ethers ethers @nomiclabs/hardhat-etherscan @nomiclabs/hardhat-waffle chai ethereum-waffle hardhat hardhat-contract-sizer hardhat-deploy hardhat-gas-reporter prettier prettier-plugin-solidity solhint solidity-coverage dotenv
```
- [Custom Errors in Solidity](https://blog.soliditylang.org/2021/04/21/custom-errors/)
### Sub-Lesson: Events & Logging
  - [Events & Logging Video](https://www.youtube.com/watch?v=KDYJC85eS5M)
  - [Events & Logging in Hardhat](https://github.com/PatrickAlphaC/hardhat-events-logs)
### Sub-Lesson: Chainlink VRF
> - [Chainlink VRFv2 Docs](https://docs.chain.link/docs/get-a-random-number/)

> - [Chainlink VRFv2 Walkthrough](https://www.youtube.com/watch?v=rdJ5d8j1RCg)

> - [Chainlink Contracts](https://github.com/smartcontractkit/chainlink/blob/develop/contracts/src/v0.8/VRFConsumerBase.sol)

- [Modulo](https://docs.soliditylang.org/en/v0.8.13/types.html?highlight=modulo#modulo)
### Sub-Lesson: Chainlink Keepers

- [Chainlink Keepers Docs](https://docs.chain.link/docs/chainlink-keepers/introduction/)
  - [Chainlink Keepers Walkthrough](https://www.youtube.com/watch?v=-Wkw5JVQGUo)
- [Enum](https://docs.soliditylang.org/en/v0.8.13/structure-of-a-contract.html?highlight=enum#enum-types)
- [Emit Chai Matcher](https://ethereum-waffle.readthedocs.io/en/latest/matchers.html#emitting-events)
- [Make Hardhat do whatever you want it to](https://hardhat.org/hardhat-network/reference/)
- [Special debugging hardhat methods](https://hardhat.org/hardhat-network/reference/#special-testing-debugging-methods)


### Recommended LINK amounts for Rinkeby Staging Test:
- Chainlink VRF: 2 LINK
- Chainlink Keepers: 8 LINK

# Lesson 10: NextJS Smart Contract Lottery (Full Stack / Front End)

💻 Code: https://github.com/PatrickAlphaC/nextjs-smartcontract-lottery-fcc
⚡️⚡️ Live Demo IPFS: ipfs://QmXwACyjcS8tL7UkYwimpqMqW9sKzSHUjE4uSZBSyQVuEH
⚡️⚡️ Live Demo Fleek: https://fancy-dream-3458.on.fleek.co/

We moving into using [NextJS](https://nextjs.org/) for our front end. NextJS is a [React framework](https://reactjs.org/) for building websites. 

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

### The Rest of this Lesson
- [NextJS Documentation](https://nextjs.org/learn/basics/create-nextjs-app)
- [NextJS Minimal Ethers Example For Lottery](https://github.com/PatrickAlphaC/nextjs-ethers-introduction)

```
yarn create next-app .
```
- [What is a component?](https://www.w3schools.com/react/react_components.asp)
- [What is a react hook?](https://reactjs.org/docs/hooks-overview.html)
- [useEffect Hook](https://reactjs.org/docs/hooks-effect.html)
- [More on useEffect](https://blog.logrocket.com/guide-to-react-useeffect-hook/)
- [useState Hook](https://reactjs.org/docs/hooks-state.html)
- [Learn CSS](https://www.w3schools.com/css/)
- [Tailwindcss](https://tailwindcss.com/)
- [Install Tailwind into NextJS](https://tailwindcss.com/docs/guides/nextjs)
- [What is IPFS](https://www.youtube.com/watch?v=5Uj6uR3fp-U)

    1. call, staticcall, delegatecall
    2. send, transfer, call

- [IPFS](https://ipfs.io/)
- [Fleek](https://fleek.co/)

# Lesson 11: Hardhat Starter Kit

💻 Code: https://github.com/smartcontractkit/hardhat-starter-kit

# Lesson 12: Hardhat ERC20s

💻 Code: https://github.com/PatrickAlphaC/hardhat-erc20-fcc

### Sub-Lesson: What is an ERC20? 
- [Video (using brownie/python)](https://youtu.be/8rpir_ZSK1g?t=39)
- [What is an EIP?](https://eips.ethereum.org/)
- [EIPs codebase](https://github.com/ethereum/EIPs)
- [EIP-20](https://eips.ethereum.org/EIPS/eip-20)
- [ERC-677](https://github.com/ethereum/EIPs/issues/677)
- [EIP-777](https://eips.ethereum.org/EIPS/eip-777)

### Rest of the Lesson
- [Openzeppelin](https://openzeppelin.com/)
- [Openzeppelin Contracts](https://github.com/OpenZeppelin/openzeppelin-contracts)
- [Solmate (Openzeppelin alternative)](https://github.com/Rari-Capital/solmate)

# Lesson 13: Hardhat DeFi & Aave

💻 Code: https://github.com/PatrickAlphaC/hardhat-defi-fcc

- [What is DeFi?](https://chain.link/education/defi)
- [DefiLlama](https://defillama.com/)
- [WETH Token Rinkeby Etherscan](https://rinkeby.etherscan.io/token/0xc778417e063141139fce010982780140aa0cd5ab#writeContract)
- [Aave V2 Docs](https://docs.aave.com/developers/v/2.0/)
- [DAI](https://makerdao.com/en/)
- [Uniswap](https://app.uniswap.org/)
- [WETH Token Mainnet](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2)
- [Aave Risk Parameters](https://docs.aave.com/risk/asset-risk/risk-parameters)

More DeFi Learnings: 
- [Speed Run Ethereum](https://speedrunethereum.com/)
- [Defi-Minimal](https://github.com/smartcontractkit/defi-minimal/tree/main/contracts)
- [Defi Dad](https://www.youtube.com/channel/UCatItl6C7wJp9txFMbXbSTg)
-   5 minute speedrun ethereum ft. [Austin Griffith](https://twitter.com/austingriffith)!



# Lesson 14: Hardhat NFTs (EVERYTHING you need to know about NFTs)

💻 Code: https://github.com/PatrickAlphaC/hardhat-nft-fcc

### Sublesson: What is an NFT? 
- [Video](https://www.youtube.com/watch?v=9yuHz6g_P50)
- [Optional: All on Chain SVG NFT](https://www.youtube.com/watch?v=9oERTH9Bkw0)

### Hardhat NFTs Part 1
- [Openzeppelin NFT](https://docs.openzeppelin.com/contracts/4.x/)
- [SVG Tutorial](https://www.w3schools.com/graphics/svg_intro.asp)
  - [On-Chain SVG Example](https://opensea.io/assets/matic/0x291ff90b9c410f56e047599bfee6b585c0c484d7/2)
- [Base64 Encoding](https://en.wikipedia.org/wiki/Base64)
  - [Example Encoder](https://base64.guru/converter/encode/image/svg)

### Sublesson: EVM Opcodes, Encoding, and Calling
Thanks to [Alex Roan](https://twitter.com/alexroan) for his help on this session!
- [Example Contract Creation Transaction](https://rinkeby.etherscan.io/tx/0x924f592458b0e37ee17024f9c826b97697455cd97f6946b802bc42296e77ae43)
What REALLY is the ABI?
  - [EVM Opcodes](https://www.evm.codes/)
  - [More EVM Opcodes](https://github.com/crytic/evm-opcodes)
  - [Solidity Cheatsheet](https://docs.soliditylang.org/en/v0.8.13/cheatsheet.html?highlight=encodewithsignature)
  - [abi.encode vs abi.encodePacked](https://ethereum.stackexchange.com/questions/91826/why-are-there-two-methods-encoding-arguments-abi-encode-and-abi-encodepacked)

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

- [Artion](https://github.com/Fantom-foundation/Artion-Contracts)
- [Reentrancy](https://solidity-by-example.org/hacks/re-entrancy)
- [Rekt.news](https://rekt.news/leaderboard/)
- [Link NextJS](https://nextjs.org/docs/api-reference/next/link)
- [Tailwind with NextJS](https://tailwindcss.com/docs/guides/nextjs)
- [Moralis](https://moralis.io/)
- [NextJS Environment Variables](https://nextjs.org/docs/basic-features/environment-variables)
- [Reverse Proxy FRP](https://github.com/fatedier/frp/releases)
  - [Docs](https://docs.moralis.io/moralis-dapp/web3/setting-up-ganache)
  - [Trouble Shooting](https://docs.moralis.io/faq#frpc)
- [Moralis Forum](https://forum.moralis.io/)
- [Moralis Admin CLI](https://docs.moralis.io/moralis-dapp/tools/moralis-admin-cli)
- [Moralis Add Event Sync From Code](https://docs.moralis.io/moralis-dapp/connect-the-sdk/connect-using-node#add-new-event-sync-from-code)
- [Moralis Cloud Functions](https://docs.moralis.io/moralis-dapp/cloud-code/cloud-functions)
- [Moralis Logging](https://docs.moralis.io/moralis-dapp/tools/moralis-admin-cli#get-logs)
- [Hardhat Network Reference](https://hardhat.org/hardhat-network/reference/)
- [Moralis Queries](https://docs.moralis.io/moralis-dapp/database/queries)

### TheGraph
- [GraphQL](https://graphql.org/)
- [GraphQL Queries](https://www.tutorialspoint.com/graphql/graphql_query.htm)
- [@apollo/client](https://www.npmjs.com/package/@apollo/client)
- [Hosting on Moralis](https://moralis.io/how-to-host-a-dapp-dapp-hosting-explained/)
- [TheGraph Docs](https://thegraph.com/docs/en/)

    1. Using Moralis
    2. Using Graph Protocol

# Lesson 16: Hardhat Upgrades

💻 Code: https://github.com/PatrickAlphaC/hardhat-upgrades-fcc

- [Optional Video](https://www.youtube.com/watch?v=bdXJmWajZRY)
## Types of Upgrades
1.  Parameter
2.  Social Migrate
3.  Proxy
    1.  [Metamorphic Upgrades](https://github.com/PatrickAlphaC/hardhat-metamorphic-upgrades-fcc)
        1. Collisions
        2. [opcodes](https://etherscan.io/opcode-tool)
    2.  Transparent
    3.  UUPS
    4.  Diamond
- [delegatecall (solidity-by-example)](https://solidity-by-example.org/delegatecall)
- [Yul](https://docs.soliditylang.org/en/latest/yul.html)
- [EIP 1967](https://eips.ethereum.org/EIPS/eip-1967)
- [Hardhat-deploy Proxies](https://github.com/wighawag/hardhat-deploy#deploying-and-upgrading-proxies)
- [Openzeppelin Upgrades Plugin](https://docs.openzeppelin.com/upgrades-plugins/1.x/)
  - [Openzeppelin upgrades tutorial](https://forum.openzeppelin.com/t/openzeppelin-upgrades-step-by-step-tutorial-for-hardhat/3580)
- [hardhat deploy upgrades examples](https://github.com/wighawag/template-ethereum-contracts/tree/examples/openzeppelin-proxies/deploy)


# Lesson 17: Hardhat DAOs

⬆️ Up-to-date code: https://github.com/PatrickAlphaC/dao-template
💻 Code from video: https://github.com/PatrickAlphaC/hardhat-dao-fcc

- [PY Code](https://github.com/brownie-mix/dao-mix)
- [Python Video](https://www.youtube.com/watch?v=rD8AxZ_wBA4)
- [Openzeppelin Governance](https://docs.openzeppelin.com/contracts/4.x/api/governance)
- [Compound Governance](https://compound.finance/governance)
- [Contract Wizard](https://docs.openzeppelin.com/contracts/4.x/wizard)
- [CastVoteBySig](https://forum.openzeppelin.com/t/what-is-votecastbysig/17069/2)

# Lesson 18: Security & Auditing

💻 Code: https://github.com/PatrickAlphaC/hardhat-security-fcc

    1. Reentrancy
    2. Flash Loans Attacks
    3. Top Tools

-   [Best Practices](https://consensys.github.io/smart-contract-best-practices/)
-   [Attacks](https://consensys.github.io/smart-contract-best-practices/known_attacks/)
    -   [Oracle Attacks](https://hackernoon.com/how-dollar100m-got-stolen-from-defi-in-2021-price-oracle-manipulation-and-flash-loan-attacks-explained-3n6q33r1)
    -   [Re-entrancy Attacks](https://quantstamp.com/blog/what-is-a-re-entrancy-attack)
-   [Damn Vulnerable Defi](https://www.damnvulnerabledefi.xyz/)
-   [Ethernaut](https://ethernaut.openzeppelin.com/)
-   Some Auditors
    -   [OpenZeppelin](https://openzeppelin.com/)
    -   [SigmaPrime](https://sigmaprime.io/)
    -   [Trail of Bits](https://www.trailofbits.com/)

## Where do I go now?

### Learning More

-   [CryptoZombies](https://cryptozombies.io/)
-   [Patrick Collins](https://www.youtube.com/channel/UCn-3f8tw_E1jZvhuHatROwA)
-   [Dapp University](https://www.youtube.com/channel/UCY0xL8V6NzzFcwzHCgB8orQ)
-   [ChainShot](https://www.chainshot.com/courses)
-   [Ivan on Tech](https://academy.ivanontech.com/)
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
8. TODO: Explain EIP-1559 at some point... maybe after blockchain explainer, but before coding.

optional JS seciton? 
Async, Arrow functions, yarn 