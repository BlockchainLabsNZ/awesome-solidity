# Libraries

### Changing contract storage from inside of the Library


```
library CounterLib {
    struct Counter { uint i; }

    function incremented(Counter storage self) returns (uint) {
        return ++self.i;
    }
}

contract CounterContract {
    using CounterLib for CounterLib.Counter;

    CounterLib.Counter counter;

    function increment() returns (uint) {
        return counter.incremented();
    }
}
```

more details on it here: [Library driven development](https://blog.aragon.one/library-driven-development-in-solidity-2bebcaf88736)

<br>

### Emitting events from the Library


```
library EventEmitterLib {
    function emit(string s) {
        Emit(s);
    }
    
    event Emit(string s);
}

contract EventEmitterContract {
    using EventEmitterLib for string;
    
    function emit(string s) {
        s.emit();
    }
    
    event Emit(string s);
}
``` 

more details on it here: [Library driven development](https://blog.aragon.one/library-driven-development-in-solidity-2bebcaf88736)


