# assert

Assert an expression. 

Accept a single **bool** as argument. If the value is false then it will **panic**.

#### Example
```diatom
a = (1..).take(6).collect()
assert(a.len() == 6)
```
