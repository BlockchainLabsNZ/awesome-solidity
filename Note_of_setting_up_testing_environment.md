# Note of setting up testing environment

This list is created and maintained by Bruce Li. It is based on Windows 10. This is not a spelling-out tutorial but more like a reminder or note to share. This list is about tools below:

* [testrpc](#testrpc)
* [Truffle](#truffle)
* [Mocha.js](#mocha)
* [Chai.js](#chai)
* [Truffle flattener](#truffle-flattener)
* [eth-gas-reporter](#eth-gas-reporter)
* [travis](#travis)
* [Coveralls](#coveralls)
* [sol-function-profiler](#sol-function-profiler)
* [Parity](#parity)

## testrpc

* Installation:  npm install -g ethereumjs-testrpc
* run it: testrpc
* sometimes, you have to run test with gas limit like this:
```
testrpc -i 666 --gasLimit 6721975
```
* we usually put it in json-package.json file like this：
```
"scripts": {
    "testrpc": "testrpc -i 666 --gasLimit 6721975",
and then npm run testrpc.
```

## Truffle

Truffle is solidity compile and deployment helper
* (If you using windows cmd, you have to add .cmd right after truffle. But if you are using PowerShell, or Mac and Linux, there is no that problem)
* install: npm install -g truffle
* init the app: truffle.cmd init
* hop into project folder and start to compile
* compile: truffle.cmd compile 
* before migrate, remember to config your truffle.js file:
```
module.exports = {
   networks: {
   development: {
   host: "localhost",
   port: 8545,
   network_id: "*" // Match any network id
  }
 }
}; 
```
* and you need to config the file in migrations folder:
```
//1_initial_migration.js
const Migrations = artifacts.require('Migrations')

module.exports = function(deployer) {
    deployer.deploy(Migrations)
}
```
* then migrate to EVM:  truffle.cmd migrate

## Mocha

Mocha is the default truffle testing tool [Website](https://mochajs.org/) 
Fast and automatically create test :
```
truffle.cmd create test projectName;
```
## Chai
Chai is the default test framework. [syntax guidance](http://chaijs.com/guide/styles/#assert)

## Truffle flattener 
to automatically make the contracts that need to be deployed combine together.
* Precondition: make sure your truffle.js installed locally, otherwise flattener cannot work properly.
```
npm install truffle-flattener -g
```
(Note: you have to install flattener globally or it wouldn’t work)


## eth-gas-reporter
* Requires mocha
```
npm install -g mocha
```

* If your Truffle installed globally:
```
npm install -g eth-gas-reporter
```

* If your Truffle installed locally (ProTip: If global installation doesn’t work, this would do the trick)
```
npm install --save-dev eth-gas-reporter
```

* Configeration
```
//truffle.js
module.exports = {
  networks: {
    ...etc...
  },
  //add below lines in the file, or it wouldn't run gas-report
  mocha: {
    reporter: 'eth-gas-reporter',
    reporterOptions : {
      currency: 'CHF',
      gasPrice: 21
    }
  }
};
```

* To run the gas-report:
```
truffle test
```
(actually, it runs with mocha.js. So, this is how you run mocha.js)

## travis 
(To be continued...)

## Coveralls
You need to do some configuration manually so that it can run on Windows 10
* Install:
```
npm install --save-dev solidity-coverage
```
* Create a file named `.solcover.js” with “module.exports = { norpc: true }` inside
* Run testRPC with:
```
node_modules\.bin\testrpc-sc --port 8555
```
* Open new command line and run
```
./node_modules/.bin/solidity-coverage
```

## sol-function-profiler
This tool is used to generate work paper
* Hop in the profiler folder and run:
```
node index.js <file name with path to the file>
```
for example: 
```
node index.js D:\Blockchain-Solidity\mothership-sen\contracts\Distribution.sol
```

<br>

If you want to generate work paper for the whole folder, use Matt’s sh script:
* Clone repo from https://github.com/matt-lough/solidity-scripts
* Hop in the folder and run bash command line
* In (git) bash, type and run: `./run_profiler`, then it asks you the target folder path. Enter and then run. 
For example: ` ../mothership-sen/contracts/ ` (don't miss the slash at the end of the path)
* All results go to work_paper.MD in solidity-scripts folder. If you are using this script repeatedly, make sure you have backup the previous report 


## Parity
It default links to Main net. Want to switch network to kovan? 
```
path/to/file/parity.exe  --chain kovan --no-persistent-txqueue
```
