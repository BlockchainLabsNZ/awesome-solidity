# Awesome Solidity ![Awesome](https://raw.githubusercontent.com/BlockchainLabsNZ/awesome-solidity/master/banner.png)

# Contributing

Please read our contribution guidelines first. [Contributors](https://github.com/BlockchainLabsNZ/awesome-solidity/graphs/contributors) are our favourite people, but we also love you readers too, thank you!

- [Getting Started](#getting-started)
- [Concepts](#concepts)
- [Best practices](#best-practices)
- [Libraries](#libraries)
  - [Standards](#standards)
  - [MultiSig Wallets](#multisig-wallets)
  - [Tokens](#tokens)
  - [Crowd sales](#crowd-sales)
- [Code Examples](#code-examples)
  - [Tokens](#tokens)
  - [Crowd Sales](#crowd-sales)
- [Tools](#tools)
  - [Testing tools](#testing-tools)
  

## Getting Started

* [Ethereum Natural Specification Format](https://github.com/ethereum/wiki/wiki/Ethereum-Natural-Specification-Format)
* [ERC20 Token Standard](https://theethereum.wiki/w/index.php/ERC20_Token_Standard) - The ERC20 token standard describes the functions and events that an Ethereum token contract has to implement.

<br>



## Concepts

* [Blockchain Oracles, Explained](https://cointelegraph.com/explained/blockchain-oracles-explained)
* [ABI](https://github.com/ethereum/wiki/wiki/Ethereum-Contract-ABI)


<br>


## Best practices

### Security

* [Ethereum Smart Contract Security Best Practices (Consensys) ](https://consensys.github.io/smart-contract-best-practices/)
* [Exceptions on overflow](https://github.com/ethereum/solidity/issues/796#issuecomment-253578925)
* [Know attacks](http://ethereum-contract-security-techniques-and-tips.readthedocs.io/en/latest/known_attacks/)

### Gas spending
* [How to write an optimized (gas-cost) smart contract?](https://ethereum.stackexchange.com/questions/28813/how-to-write-an-optimized-gas-cost-smart-contract/28818)
* [Gas Costs from Yellow paper](https://docs.google.com/spreadsheets/d/1n6mRqkBz3iWcOlRem_mO09GtSKEKrAsfO7Frgx18pNU/edit#gid=0)
* [Under-Optimized Smart Contracts Devour Your Money](https://arxiv.org/pdf/1703.03994.pdf) (.pdf)


<br>

## Libraries

### Standards

- [OpenZeppelin Contracts](https://github.com/OpenZeppelin/zeppelin-solidity) - A framework to build secure smart contracts on Ethereum.
- [SafeMath](https://github.com/OpenZeppelin/zeppelin-solidity/blob/master/contracts/math/SafeMath.sol) - Safely perform mathematical operations.
- [Style Guide](http://solidity.readthedocs.io/en/develop/style-guide.html#function-declaration) - Follow the style guide to make solidity codes layout look pretty

### MulstiSig Wallets

- [Gnosis MultiSig](https://github.com/gnosis/MultiSigWallet) - Popular multisig deployed by the likes of District0x, Golem, Aragon, Bancor, and more..

### Tokens

- [OpenZeppelin Base Tokens](https://github.com/OpenZeppelin/zeppelin-solidity/tree/master/contracts/token) - Collection of basic token skeletons to extend.
- [MiniMe Token](https://github.com/Giveth/minime) - The MiniMeToken contract is a standard ERC20 token with extra functionality.

### Crowd Sales

- [Status.im Crowdsale](https://github.com/status-im/status-network-token/tree/master/contracts) - Crowdsale contracts from Status.

If you need more help, check out [Ethereum StackExchange](https://ethereum.stackexchange.com)


<br>



## Code and patterns examples
links to the code

### Test Templates



<br>

## Tools

### Testing tools

- [Truffle](https://github.com/trufflesuite/truffle) - Truffle is a development environment, testing framework and asset pipeline for Ethereum, aiming to make life as an Ethereum developer easier.
- [TestRPC](https://github.com/ethereumjs/testrpc) - Fast Ethereum RPC client for testing and development.
- [Note of setting up testing environment](https://github.com/BlockchainLabsNZ/awesome-solidity/blob/master/Note_of_setting_up_testing_environment.md) - A note of how to set up testing environment and avoid annoying errors (on Windows10). Including a few regular tools: testrpc, truffle, mocha.js,truffle flattener, gas-reporter, coveralls, sol-function-profiler, Parity
