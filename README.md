# Awesome Solidity ![Awesome](../master/banner.png?raw=true)

# Contributing

Please read our contribution guidelines first. [Contributors](https://github.com/BlockchainLabsNZ/awesome-solidity/graphs/contributors) are our favourite people, but we also love you readers too, thank you!

✨ Index ✨
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
  - [Other](#other)
- [Tools](#tools)
  - [Testing tools](#testing-tools)
  

## Getting Started

* [Ethereum Natural Specification Format](https://github.com/ethereum/wiki/wiki/Ethereum-Natural-Specification-Format)
* [ERC20 Token Standard](https://theethereum.wiki/w/index.php/ERC20_Token_Standard) - The ERC20 token standard describes the functions and events that an Ethereum token contract has to implement.
* [ERC Token Standards for Dummies, Like Me](https://decentral.market/2018/03/04/erc-token-standards-for-dummies-like-me/) - ERC20, ERC223, ERC827, ERC721 short review with major points and concerns.
* Solidity CRUD operations – [part1](https://bitbucket.org/rhitchens2/soliditycrud/src/master/docs/solidityCRUD-pt1.pdf), [part2](https://bitbucket.org/rhitchens2/soliditycrud/src/master/docs/solidityCRUD-pt2.pdf)
* [Airdrops](https://blog.ricmoo.com/merkle-air-drops-e6406945584d)

	### Typical Business logic
	
	* [Tokens](logic/tokens.md)
	* Wallets<!--](logic/wallets.md)-->
	* Crowd sale<!--](logic/sale.md)-->
	* Distribution/Exchange<!--](logic/distribution-and-exchange.md)-->
	* Vesting/Locking<!--](logic/vesting.md)-->

	### Short answers to some questions

	* ["Indexed" keyword / filtering logs](https://ethereum.stackexchange.com/questions/8658/what-does-the-indexed-keyword-do#8659)
	* [Execution of Fallback function with more 2300 gas](https://ethereum.stackexchange.com/questions/11237/execution-of-fallback-function-with-more-2300-gas)

<br>



## Concepts

* [Blockchain Oracles, Explained](https://cointelegraph.com/explained/blockchain-oracles-explained)
* [ABI](https://github.com/ethereum/wiki/wiki/Ethereum-Contract-ABI)
* [Upgradable contracts](https://blog.indorse.io/ethereum-upgradeable-smart-contract-strategies-456350d0557c) - check the reference section also
* [Keccak256](https://www.slideshare.net/RajeevVerma14/keccakpptx)
* [Random numbers](https://ethereum.stackexchange.com/questions/191/how-can-i-securely-generate-a-random-number-in-my-smart-contract)
* [Off-Chain Whitelist with On-Chain Verification for Ethereum Smart Contracts](https://medium.com/@PhABC/off-chain-whitelist-with-on-chain-verification-for-ethereum-smart-contracts-1563ca4b8f11)
* [Velocity of Tokens](https://medium.com/newtown-partners/velocity-of-tokens-26b313303b77)

<br>


## Best practices

### Security

* [Ethereum Smart Contract Security Best Practices (Consensys) ](https://consensys.github.io/smart-contract-best-practices/)
* [Exceptions on overflow](https://github.com/ethereum/solidity/issues/796#issuecomment-253578925)
* [Known attacks](http://ethereum-contract-security-techniques-and-tips.readthedocs.io/en/latest/known_attacks/)

### Gas spending

* [How to write an optimized (gas-cost) smart contract?](https://ethereum.stackexchange.com/questions/28813/how-to-write-an-optimized-gas-cost-smart-contract/28818)
* [Gas Costs from Yellow paper](https://docs.google.com/spreadsheets/d/1n6mRqkBz3iWcOlRem_mO09GtSKEKrAsfO7Frgx18pNU/edit#gid=0)
* [Under-Optimized Smart Contracts Devour Your Money](https://arxiv.org/pdf/1703.03994.pdf) (.pdf)
* [public vs external](https://ethereum.stackexchange.com/questions/19380/external-vs-public-best-practices?answertab=active#tab-top) - latter is twice cheaper (496 vs 261)

### Other

- [Style Guide](http://solidity.readthedocs.io/en/develop/style-guide.html#function-declaration) - Follow the style guide to make solidity codes layout look pretty

<br>


<br>


## Libraries

## Best Practice

- [OpenZeppelin Contracts](https://github.com/OpenZeppelin/zeppelin-solidity) - A framework to build secure smart contracts on Ethereum.
- [SafeMath](https://github.com/OpenZeppelin/zeppelin-solidity/blob/master/contracts/math/SafeMath.sol) - Safely perform mathematical operations.

## MulstiSig Wallets

- [Gnosis MultiSig](https://github.com/gnosis/MultiSigWallet) - Popular multisig deployed by the likes of District0x, Golem, Aragon, Bancor, and more..

## Smart Contract Examples

## Tokens

- [OpenZeppelin Base Tokens](https://github.com/OpenZeppelin/zeppelin-solidity/tree/master/contracts/token) - Collection of basic token skeletons to extend.
- [MiniMe Token](https://github.com/Giveth/minime) - The MiniMeToken contract is a standard ERC20 token with extra functionality.

## Crowd Sales

- [Status.im Crowdsale](https://github.com/status-im/status-network-token/tree/master/contracts) - Crowdsale contracts from Status.

If you need more help, check out [Ethereum StackExchange](https://ethereum.stackexchange.com)

## Dev-tools

- [Solidity-scripts](https://github.com/matt-lough/solidity-scripts) - List of Scripts created by us for use when auditing

- [Solidity Function Profiler](https://github.com/EricR/sol-function-profiler) -  Analysis report of function signatures, visibility, return values, and modifiers.

## Tutorials

- [Crypto Zombies](https://cryptozombies.io/) - Great for a complete beginner to learn Solidity

## Known Vulnerabilities

The following is a list of known vulnerabilities that should be considered when writing and auditing smart contracts.
