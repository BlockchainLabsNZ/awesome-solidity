# Testing errors and how to fix them

This is a list of error messages when running testing tools, and the methods of how to deal with them. You can contribute to the list, or talk to Bruce if you have any problem.
Most of errors and solutions been encountered and fixed under environment below:
* Environment
    - Operation system: Windows 10
    - testRPC version: v6.1.0 (ganache-core: 2.1.0)
    - coverage-solidity version: 
    - Node.js version: 8.9.0
If your contribution is totally different with this condition (e.g. only encountered on Linux system), label it.

## Coverage-solidity
### Exceeds block gas limit
* Error message
```
Error: Error: Exceeds block gas limit
    at StateManager.queueTransaction (C:\Users\ryu98\AppData\Roaming\npm\node_modules\ethereumjs-testrpc\build\cli.node.js:90571:21)
    ...
Cleaning up...
Event trace could not be read.
Error: ENOENT: no such file or directory, open 'D:\Blockchain-Solidity\etheal-contracts2\allFiredEvents'
Exiting without generating coverage...
```
* Method to fix
When you start your testRPC, run this script instead of simply "testrpc"
```
testrpc --gasLimit 0xfffffffffff
```
That sets up your block gas limit. You can raise it up if that number cannot satisfy your test.

### Export/import failure
* Error message
```
(function (exports, require, module, __filename, __dirname) { export default async promise => {...}
                                                              ^^^^^^
SyntaxError: Unexpected token export
```
* Method to fix
The reason we've got this error is because `export/import` is not standard js syntax. You either use babel.js to compile to standard JavaScript (if you know how) or change
```
export default async promise => {...}
```
to
```
module.exports = async function (promise) {...}
``` 
Similar issue when it comes to `import`. Change
```
import assertRevert from './helpers/assertRevert';
```
to
```
const assertRevert = require('./helpers/assertRevert');
```
 will fix the problem.

### Increase balance of testrpc accounts
* Error message
```
 sender doesn't have enough funds to send tx. The upfront cost is: 1759218604441500000000000 and the sender's account only has: 100000000000000000000
```
* Method to fix
Balances of accounts are too low. When you run testrpc, adding more balances to each account will fix the problem. In command line, it could looks like this:
```
node_modules/.bin/testrpc-sc --gasLimit 0xfffffffffff --gasPrice 1 --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501200,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501201,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501202,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501203,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501204,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501205,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501206,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501207,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501208,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF --account=0x2bdd21761a483f71054e14f5b827213567971c676928d9a1808cbfa4b7501209,0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF
```

### Out of gas due to high gas price
* Error message
```
VM Exception while processing transaction: out of gas
```
* Method to fix
gas price maybe too high and run out the ether in your account. Set it to 1 in the truffle.js file. It could look like this:
```
module.exports = {
  networks: {
    development: {
      host: "127.0.0.1",
      port: 8545,
      gas: 0xfffffffffff, // <-- Use this high block gas limit 
      gasPrice: 0x01,     // <-- Use this low gas price
      network_id: "*" 
    }
  },
...etc...
};
```

### Missing allFiredEvents
* Error message
```
Event trace could not be read.
Error: ENOENT: no such file or directory, open 'D:\Blockchain-Solidity\bankorus_pre\allFiredEvents'
Exiting without generating coverage...
```
* Method to fix
Need a file called allFiredEvents in the folder for logging event. You can create an empty one manually.
