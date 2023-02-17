# Tuple

A tuple of items, useful in multiple return or anonymous tables.  
Access tuple items via `.` operator and a `Int` literal.

### Examples
```diatom
def multi_ret x y =
    (x, y)
end

tuple = multi_ret$(1, 3)
println$( tuple )
println$( tuple.0 )

tuple.0 = 'changed'
println$( tuple.0 )
```

