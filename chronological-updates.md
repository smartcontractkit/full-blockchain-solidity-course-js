# Chronological Updates

This file will contain all updates to sections. 

# Lesson 5
## Windows, WSL, & Ganache
- Per [this question](https://github.com/smartcontractkit/full-blockchain-solidity-course-js/discussions/34#discussioncomment-2846436), if you're using WSL, for the ganache UI you'll have to use a different endpoint. 

You have 4 options to fix this:
1. Use the WSL endpoint on the ganache UI (this sometimes doesn't work)
2. Use `ganache` from the command line
3. Use `ganache-cli` from the command line (not recommended)
4. Just use `hardhat` from the command line (you'll have to use hardhat at some point anyways!)

### Using the WSL Endpoint
On the Ganache UI, you can select a different hostname and connect to whatever IP you see. In the example below, you'd connect to `172.24.224.1`

![img](./img/ganache-windows.png)

You can also try to edit it by:

1. Inside Ganache in the top-right corner tap on the gear icon (settings).
2. Then in the server tab, change the HOSTNAME and select 0.0.0.0 - All Interfaces.
3. Now replace your RPC Server URL inside the code with this latest URL that will be something like: HTTP://0.0.0.0.7545. Recheck this from Ganache.

### Using `ganache`

```
yarn global add ganache
ganache
```

Keep this running in it's own terminal, and use the endpoint it gives you. To kill it, press `CTRL` + `C`.

[See the discussion here](https://github.com/smartcontractkit/full-blockchain-solidity-course-js/discussions/34)

### Using `ganache-cli` from the command line.
Or, optionally, you can install `ganache-cli` [as this user did](https://github.com/smartcontractkit/full-blockchain-solidity-course-js/discussions/39#discussioncomment-2854165).

```
yarn global add ganache-cli
ganache-cli
```

Keep this running in it's own terminal, and use the endpoint it gives you. To kill it, press `CTRL` + `C`.

### Using `hardhat`

[See the discussion here](https://github.com/smartcontractkit/full-blockchain-solidity-course-js/discussions/90#discussioncomment-2871657)

```
yarn add --dev hardhat
yarn hardhat
```

Then select the `Create an empty hardhat.config.js`

Then run:

```
yarn hardhat node
```

Keep this running in it's own terminal, and use the endpoint it gives you. To kill it, press `CTRL` + `C`.


--------

# Lesson 9

## Keepers Not Kicking Off Troubleshooting

If your keepers are not kicking off, run through this checklist to find out why. 

1. Double check the subscription ID in your contract
2. Double check the subscription is funded with enough LINK 
3. Is `checkUpkeep` returning true?  
4. Can you call `performUpkeep` yourself? (If you can't the keeper can't!)

# Lesson 15

## Metamask Troubleshooting while using Gitpod

- Remember if you are using gitpod then you cannot connect your local hardhat node with metamask. To resolve this you can use vs code or testnets instead of local node.
