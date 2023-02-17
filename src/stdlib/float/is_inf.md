# Float::is\_inf

Test if a `Float` is positive or negative infinity.

### Type
```haskell
is_inf :: Float -> Bool
```

### Examples
```diatom
println$( Float::INF.is_inf$() )
println$( Float::NEG_INF.is_inf$() )
println$( 1.2345.is_inf$() )
```

