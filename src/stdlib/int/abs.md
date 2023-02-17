# Int::abs 

Calculate absolute value of an integer.  
Note that absolute value of `Int::MIN` will always cause an **overflow** which will return `Int::MIN`.

### Type
```haskell
abs :: Int -> Int
```

### Examples
```diatom
println$( (-10).abs$() )
println$( Int::MIN.abs$() )
```
