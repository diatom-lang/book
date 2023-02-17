# Float::int

Cast a `Float` to `Int` type by truncating.

### Type
```haskell
int :: Float -> Int
```

### Examples
```diatom
println$( 1.7.int$() )
println$( 1.2.int$() )
println$( (-1.7).int$() )
println$( (-1.2).int$() )
```

