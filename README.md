# Awesome Solidity

![Awesome](awesome_solidity_logo.jpg)

#### Contributing

[Contributors](https://github.com/BlockchainLabsNZ/awesome-solidity/graphs/contributors) are our favourite people, but we also love you readers too, thank you!


✨ **Index** ✨

* [Getting Started](#getting-started)
* [Vulnerabilities](#vulnerabilities)
* [Best practices](#best-practices)
* [Libraries](#libraries)
* [Code Examples](#code-and-patterns-examples)
* [Tools](#tools)
* [Dapps development](#dapps-development)

<br>

## Getting Started

* [The Hitchhiker's Guide to Smart Contracts](https://blog.zeppelin.solutions/the-hitchhikers-guide-to-smart-contracts-in-ethereum-848f08001f05)
* Solidity CRUD operations – [part1](https://bitbucket.org/rhitchens2/soliditycrud/src/master/docs/solidityCRUD-pt1.pdf), [part2](https://bitbucket.org/rhitchens2/soliditycrud/src/master/docs/solidityCRUD-pt2.pdf)
* [Airdrops](https://blog.ricmoo.com/merkle-air-drops-e6406945584d)
- [Note of setting up testing environment](https://github.com/BlockchainLabsNZ/awesome-solidity/blob/master/Note_of_setting_up_testing_environment.md) – A note of how to set up testing environment and avoid annoying errors (on Windows10). Including a few regular tools: testrpc, truffle, mocha.js,truffle flattener, gas-reporter, coveralls, sol-function-profiler, Parity

	### Concepts

	* [Blockchain Oracles, Explained](https://cointelegraph.com/explained/blockchain-oracles-explained)
	* [ABI](https://github.com/ethereum/wiki/wiki/Ethereum-Contract-ABI)
	* [Keccak256](https://www.slideshare.net/RajeevVerma14/keccakpptx)
	* [Web 3.0 Explained](https://www.youtube.com/watch?v=aPVmd7SyKfQ)
	* [Random numbers](https://ethereum.stackexchange.com/questions/191/how-can-i-securely-generate-a-random-number-in-my-smart-contract)
	* [Velocity of Tokens](https://medium.com/newtown-partners/velocity-of-tokens-26b313303b77)


	### Tutorials

	* [CryptoZombies: Learn to Code Ethereum DApps By Building Your Own Game](https://cryptozombies.io)
	* [Ethernaut - Smart Contract Hacking Game](https://ethernaut.zeppelin.solutions/)
	* [Hack This Contract Game](http://hackthiscontract.io/)
	* [What's Solidity?](https://www.youtube.com/channel/UCaWes1eWQ9TbzA695gl_PtA/videos) – Youtube tutorials
	* [Building a fully decentralized User profile app on Ethereum and IPFS](https://medium.com/@sebinatx/building-a-fully-decentralized-user-profile-dapp-on-ethereum-and-ipfs-e55afac35718)
	* [Ethereum and Solidity: The Complete Developer's Guide](https://www.udemy.com/ethereum-and-solidity-the-complete-developers-guide/learn/v4/overview) – Udemy course
	* [Become a Blockchain Developer with Ethereum and Solidity](https://www.udemy.com/getting-started-with-ethereum-solidity-development/learn/v4/content) – Udemy course
	* [Creating your own DAO based on Aragon framework](https://medium.com/@joselfgaray/dao-workshop-testnet-b406380894a6)
	* [Test Driven Development for Solidity](https://michalzalecki.com/ethereum-test-driven-introduction-to-solidity/)


	### Short answers to some questions

	* ["Indexed" keyword / filtering logs](https://ethereum.stackexchange.com/questions/8658/what-does-the-indexed-keyword-do#8659)
	* [Execution of Fallback function with more 2300 gas](https://ethereum.stackexchange.com/questions/11237/execution-of-fallback-function-with-more-2300-gas)

	### Typical Business logic

	* [Tokens](logic/tokens.md)
	* Wallets<!--](logic/wallets.md)-->
	* Crowd sale<!--](logic/sale.md)-->
	* Distribution/Exchange<!--](logic/distribution-and-exchange.md)-->
	* Vesting/Locking<!--](logic/vesting.md)-->

	### News

	* [ICO Alert](https://www.icoalert.com/) – upcoming ICOs
	* [Dappradar](https://dappradar.com) – list of new dapps

	### Blogs

	* [ConsenSys](https://medium.com/@ConsenSys)
	* [Sarah Baker Mills](https://medium.com/@starsoup7) – Design director @Consensys
	* [David Rugendyke](https://medium.com/@darcius) – Rocket Pool developer
	* [Alex Sherbuck](https://medium.com/@alexsherbuck) – market news and hacks observation
	* [Matthew Di Ferrante](https://medium.com/@matthewdif) – Founder @ ZK Labs
	* [Philippe Castonguay](https://medium.com/@PhABC)



<br>

## Vulnerabilities

* Consensys: [known attacks](http://ethereum-contract-security-techniques-and-tips.readthedocs.io/en/latest/known_attacks/) (updates are irregular)
* Honey Pots: [1](https://medium.com/@gerhard.wagner/the-phenomena-of-smart-contract-honeypots-755c1f943f7b),
[2](https://medium.com/@alexsherbuck/dissecting-an-ethereum-honey-pot-7102d7def5e0), [3](https://medium.com/@jsanjuas/an-analysis-of-a-couple-ethereum-honeypot-contracts-5c07c95b0a8d)

	### Known hacks
	* [Integer Overflow (i.e., proxyOverflow Bug)](http://telegra.ph/Integer-Overflow-ie-proxyOverflow-Bug-Found-in-Multiple-ERC20-Smart-Contracts-04-25) – Found in Multiple ERC20 Smart Contracts
	* [The DAO Hack](http://hackingdistributed.com/2016/06/18/analysis-of-the-dao-exploit/)
	* [Parity Wallet Hack](https://medium.freecodecamp.org/a-hacker-stole-31m-of-ether-how-it-happened-and-what-it-means-for-ethereum-9e5dc29e33ce)
	* [Parity Wallet Hack II](https://hackernoon.com/parity-wallet-hack-2-electric-boogaloo-e493f2365303)
	* [How $800K Evaporated from PoWH Ponzi](https://blog.goodaudience.com/how-800k-evaporated-from-the-powh-coin-ponzi-scheme-overnight-1b025c33b530)

<br>

## Best practices

### Security

* [Ethereum Smart Contract Security Best Practices (Consensys) ](https://consensys.github.io/smart-contract-best-practices/)
* [Exceptions on overflow](https://github.com/ethereum/solidity/issues/796#issuecomment-253578925)

### Gas spending

* [How to write an optimized (gas-cost) smart contract?](https://ethereum.stackexchange.com/questions/28813/how-to-write-an-optimized-gas-cost-smart-contract/28818)
* [Gas Costs from Yellow paper](https://docs.google.com/spreadsheets/d/1n6mRqkBz3iWcOlRem_mO09GtSKEKrAsfO7Frgx18pNU/edit#gid=0)
* [Under-Optimized Smart Contracts Devour Your Money](https://arxiv.org/pdf/1703.03994.pdf) (.pdf)
* [public vs external](https://ethereum.stackexchange.com/questions/19380/external-vs-public-best-practices?answertab=active#tab-top) – latter is twice cheaper (496 vs 261)

### Common design principles

* [Off-Chain Whitelist with On-Chain Verification for Ethereum Smart Contracts](https://medium.com/@PhABC/off-chain-whitelist-with-on-chain-verification-for-ethereum-smart-contracts-1563ca4b8f11)
* [Library Driven Development in Solidity](https://blog.aragon.one/library-driven-development-in-solidity-2bebcaf88736), and [SOLDOC#Libraries](https://solidity.readthedocs.io/en/develop/contracts.html#libraries)
* [Reversing Ethereum Smart Contracts](https://arvanaghi.com/blog/reversing-ethereum-smart-contracts/) – smart contract reverse engineering
* [A Crash Course for Mechanism Design](https://medium.com/blockchannel/a-crash-course-in-mechanism-design-for-cryptoeconomic-applications-a9f06ab6a976)

### ERCs

* [ERC20 Token Standard](https://theethereum.wiki/w/index.php/ERC20_Token_Standard) – The ERC20 token standard describes the functions and events that an Ethereum token contract has to implement.
* [The Anatomy of ERC20](https://medium.com/blockchannel/the-anatomy-of-erc20-c9e5c5ff1d02)
* [ERC223 Token Standard](https://github.com/ethereum/EIPs/issues/223) – contracts with safety methods that allow return tokens sent accidentally to the contract address.
* [ERC Token Standards for Dummies, Like Me](https://decentral.market/2018/03/04/erc-token-standards-for-dummies-like-me/) – ERC20, ERC223, ERC827, ERC721 short review with major points and concerns.
* [Walking Through the ERC721 Full Implementation
](https://medium.com/blockchannel/walking-through-the-erc721-full-implementation-72ad72735f3c)
* [ERC827](https://github.com/ethereum/EIPs/issues/827) – ERC827 token. Transfers/approvals with calls.
* [ERC875](https://github.com/ethereum/EIPs/issues/875) - ERC875 for non fungible tokens and simple atomic swaps

### EIPs
* [Ethereum Natural Specification Format](https://github.com/ethereum/wiki/wiki/Ethereum-Natural-Specification-Format)
* [EIP821](https://github.com/ethereum/EIPs/issues/821) – EIP (not ERC) 821. Contracts for Non Fungible Tokens (NFTs).
* [A New Advanced Token Standard](https://github.com/ethereum/EIPs/issues/777) – Contract defines operators to send tokens on behalf of another address – contract or regular account.

### Other

* [Style Guide](http://solidity.readthedocs.io/en/develop/style-guide.html#function-declaration) – Follow the style guide to make solidity codes layout look pretty
* [Upgradable contracts](upgradable-contracts.md)




<br>

## Libraries

### Standard contracts

- [OpenZeppelin Contracts](https://github.com/OpenZeppelin/zeppelin-solidity) – A framework to build secure smart contracts on Ethereum.
- [OpenZeppelin Base Tokens](https://github.com/OpenZeppelin/zeppelin-solidity/tree/master/contracts/token) – Collection of basic token skeletons to extend.
- [MiniMe Token](https://github.com/Giveth/minime) – The MiniMeToken contract is a standard ERC20 token with extra functionality.
- [Gnosis MultiSig](https://github.com/gnosis/MultiSigWallet) – Popular multisig deployed by the likes of District0x, Golem, andon, Bancor, and more..
- [Status.im Crowdsale](https://github.com/status-im/status-network-token/tree/master/contracts) – Crowdsale contracts from Status.

### Utils

- [SafeMath](https://github.com/OpenZeppelin/zeppelin-solidity/blob/master/contracts/math/SafeMath.sol) – Safely perform mathematical operations.
- [Solidity String Utils](https://github.com/Arachnid/solidity-stringutils) (use with care).
- [Easily Send Many Tokens to Many Addresses](https://github.com/poanetwork/multisender)
- [BytesHelper](https://github.com/izqui/keybase-ethereum-registry/blob/rocksolid/contracts/BytesHelper.sol) - library to deal with bytes32


<br>

## Code and patterns examples

- [Bitwise Operations and Bit Manipulation in Solidity, Ethereum](https://medium.com/@imolfar/bitwise-operations-and-bit-manipulation-in-solidity-ethereum-1751f3d2e216)
- [Upgradable contracts](examples/upgradable-contracts.md) – example
- [Solidity Security Exploits](https://github.com/tenthirtyone/weaponized_math): Re-Entrancy, Denial of Service - Gas, Denial of Service - Revert, Force Ether - selfdestruct, Storage Allocation Exploit, Underflow / Overflow, Re-Entrancy Honey Pot, Function Call Honey Pot. [Explanations here](https://medium.com/@alexsherbuck/two-ways-to-force-ether-into-a-contract-1543c1311c56)
- [Not so smart contracts](https://github.com/trailofbits/not-so-smart-contracts) – Another examples of known vulnerabilities
- [Changing contract storage from inside of the Library](examples/libraries.md#changing-contract-storage-from-inside-of-the-library)
- [Emitting events from the Library](examples/libraries.md#emitting-events-from-the-library)
- Chai.js, [BDD approach in testing](http://www.chaijs.com/api/bdd/)
- [Memory vs Storage & How to initialize an array inside a struct](https://medium.com/loom-network/ethereum-solidity-memory-vs-storage-how-to-initialize-an-array-inside-a-struct-184baf6aa2eb)



<br>

## Tools

### Testing tools

- [Truffle](https://github.com/trufflesuite/truffle) – Truffle is a development environment, testing framework and asset pipeline for Ethereum, aiming to make life as an Ethereum developer easier.
- [TestRPC](https://github.com/ethereumjs/testrpc) – Fast Ethereum RPC client for testing and development.
- [Solidity Function Profiler](https://github.com/EricR/sol-function-profiler) -  Analysis report of function signatures, visibility, return values, and modifiers.

### Development tools

- [Docker images](https://hub.docker.com/r/nzblabs/) / [Audit repo](https://github.com/BlockchainLabsNZ/audit-env) - Solidity testing environment from us (Blockchain Labs, NZ)
- [11 Best Ethereum Development Tools](https://hackernoon.com/11-best-ethereum-development-tools-to-grow-your-stack-e782fd7156ab)
- [Solidity Doc generator](https://github.com/matt-lough/solidity-docstring-generator) – from Matt Lough
- [Solidity syntax highlighting on Github](https://medium.com/@danielque/psa-how-to-fix-githubs-syntax-highlighting-for-solidity-4e9867c540b6) – howto

### Online services

- [Ethereum gas station](https://www.ethgasstation.info)
- [Ethereum unit converter](https://etherconverter.online)


<br>

## Dapps development

Helpful information about Dapps.

* [Web3 Design principles](https://medium.com/@lyricalpolymath/web3-design-principles-f21db2f240c1) – development Dapps
* [Blockchain Design Principles](https://medium.com/design-ibm/blockchain-design-principles-599c5c067b6e)
* [How to create a DApp using Truffle, Oraclize, ethereum-bridge and Webpack](https://medium.com/coinmonks/how-to-create-a-dapp-using-truffle-oraclize-ethereum-bridge-and-webpack-9cb84b8f6bcb)
* [Create Blockchain Dapp with Ethereum and VueJS](https://www.danielefavi.com/create-your-blockchain-dapp-with-ethereum-and-vuejs-part-1/)
* []()

	### Design

	* [Designing for the blockchain](https://hackernoon.com/designing-for-the-blockchain-launching-an-ethereum-smart-contract-app-3a972615731c)
	* [How to make a user-friendly Ethereum dApp
](https://blog.hellobloom.io/how-to-make-a-user-friendly-ethereum-dapp-5a7e5ea6df22)

<br>

