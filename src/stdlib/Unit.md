# Unit (primitive type)

A tuple with 0 items, has only one possible value `()`. This value is implicitly returned if no return value is provided.

### Type
```haskell
() :: ()
```

### Examples
```diatom
def ret_unit = end

println$( ret_unit$() )

value = begin
    -- statement always return ()
    loop 
        break
    end
end

println$(value)
```
