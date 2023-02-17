# List::iter

Get an iterator of this list.
### Type
```haskell
iter :: [a] -> Iter a
```

### Examples
```diatom
iter = [1, 2, 3].iter$()
println$( iter.__next$().value )
```

