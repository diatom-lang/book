# Bool (primitive type)

Boolean value, can be either `true` or `false`.
`if` and `until` statement requires condition must return a bool value.

### Type
```haskell
Bool :: Bool
```

### Examples
This example will **NOT** work.
```diatom
if 0 then
    println$(' 0 is not false ')
end
```
