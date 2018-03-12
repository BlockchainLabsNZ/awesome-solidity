# Upgradable contracts

<br>

## Importing data from another contract
If you need access the same data from different contact you need to think in advance.

### Original contract

```
pragma solidity ^0.4.18;

contract upgradableContactDataController {
    
  address public addr;
    
  struct Structure { 
      address addr;
      uint num;
  }
  
  Structure public _struct;
  
  function asdf() public {
      _struct.addr = 0x123;
      _struct.num = 12;
  }
  
  function getStruct() public view returns(address, uint) {
      return(_struct.addr, _struct.num);
  }
  
}
```

### Interface contract

```
pragma solidity ^0.4.18;

contract DataInterface {
    
    struct Structure { 
      address addr;
      uint num;
    }    

    Structure public _struct;

    function getAddress() view public returns(address, uint) {
        return (_struct.addr, _struct.num);
    }
}
```

### New contract

```
pragma solidity ^0.4.18;

import "./DataInterface.sol";

contract newContractDataController is DataInterface {
  function foo(address _contract) public view {
    address _addr;
    uint _num;
    (_addr, _num) = DataInterface(_contract).getAddress();
  }
}

```


<br>
