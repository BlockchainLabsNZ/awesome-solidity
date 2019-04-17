# Check list of static analysis
This list aims to remind auditors of both common and rare issues of smart contract project. The resource is our previous project experience.

## Typical issues
* Gas costs can be reduced on specific conditions:
 - Using string in struct costs more gas than bytes32. See [example](https://github.com/BlockchainLabsNZ/mothership-sen/issues/3)
 - Unnecessary check. See [example](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/6)
 - Assigning a variable and return it can be combine to onle line. See [example](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/5)
 - Not assigning a global variable to a local variable. See [example](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/2) 
 - Uint256 can be used in replacement of uint8 to save gas. See [example](https://github.com/BlockchainLabsNZ/bankorus_contracts_audit/issues/2) and the [reason](https://ethereum.stackexchange.com/questions/3067/why-does-uint8-cost-more-gas-than-uint256)
* Whether all declared variables/modifiers/functions/events/files been used? See [example_1](https://github.com/BlockchainLabsNZ/zipper-contracts/issues/4), [example_2](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/13) 
* Whether log a event after critical behaviour like transfer/mint/burn/change owner, etc? See [example_1](https://github.com/BlockchainLabsNZ/zipper-contracts/issues/1), [example_2](https://github.com/BlockchainLabsNZ/staking-contracts-audit/issues/2)
* Prefer explicit declaration of variable types. See [example_1](https://github.com/BlockchainLabsNZ/staking-contracts-audit/issues/3), [example_2](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/9)
* Prefer explicit declaration of variables access modifiers. See [example](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/8)
* Alwayse use latest version of compiler. See [example](https://github.com/BlockchainLabsNZ/staking-contracts-audit/issues/1) 
* The declaration of pragma version should be at the top of the file, before any imports happen. See [example](https://github.com/BlockchainLabsNZ/staking-contracts-audit/issues/1)
* Enforce the use of specific solc version and the reasons. See [example_1](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/10), [example_2](https://github.com/BlockchainLabsNZ/leverj-contracts/issues/5) 
* Dead code should be removed. See [example](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/7)
* Consistent naming convention (normally CamelCase). See [example_1](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/4), [example_2](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/3)
* Make visibility explicitly declared on everything. See [example](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/1)
* Avoid magic numbers. See [example](https://github.com/BlockchainLabsNZ/bluzelle-contracts/issues/3)
* Comment needs updating to reflect code logic. See [example](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/11)
* Use .transfer instead of .send. See [example](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/10)
* Convention is to use capital letters for the token "symbol". See [example](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/6)
* Recommend using braces for single line if/for statement. See [example](https://github.com/BlockchainLabsNZ/etheal-contracts/issues/5). See [discussion](https://stackoverflow.com/questions/2125066/is-it-bad-practice-to-use-an-if-statement-without-brackets)
* Functions should throw an error instead of returning false. See [example](https://github.com/BlockchainLabsNZ/mobilego-contracts-audit/issues/1)
* Measure time milestones with timestamps, not block height. See [example](https://github.com/BlockchainLabsNZ/leverj-contracts/issues/6)
* Improve code readability by making use of solidity time uints. See [example](https://github.com/BlockchainLabsNZ/leverj-contracts/issues/8)
* The inheritance should be declared explicitly. See [example](https://github.com/BlockchainLabsNZ/poa-popa/issues/2)
* Repeated safety checks can be replaced by modifier. See [example](https://github.com/BlockchainLabsNZ/poa-popa/issues/1)
* Public variables and functions should have different names to aviod duplicate. See [example](https://github.com/BlockchainLabsNZ/LINA-TokenERC20/issues/2) 
* A function should return a result if its declaration says that. See [example](https://github.com/BlockchainLabsNZ/LINA-TokenERC20/issues/1)
* Favour require() over If() statements. See [example](https://github.com/BlockchainLabsNZ/mothership-sen/issues/1)



## Other issues
* [Unnecessary gas spent when avoiding double distribution](https://github.com/BlockchainLabsNZ/zipper-contracts/issues/2)
* [Inconsistent use of require and revert](https://github.com/BlockchainLabsNZ/wings-private-contracts/issues/13)
* [Inconsistency in variable types](https://github.com/BlockchainLabsNZ/synchrolife/issues/5)
* [Tokens are not automatically transferred to investors](https://github.com/BlockchainLabsNZ/gifto-contracts/issues/12)
* [Remove comment in Non-English and add ENG comments](https://github.com/BlockchainLabsNZ/LAToken-Contracts-Audit/issues/25)
* [Safemath should be used](https://github.com/BlockchainLabsNZ/leverj-contracts/issues/4)
