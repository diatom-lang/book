# Int (primitive type)

An platform independent 64-bit signed integer type, guaranteed to be **wrapped** if **overflow happens**.

### Meta table
`Int` type's meta table is stored in variable named `Int`.

### Examples
```diatom
println$( Int::MAX )
println$( Int::abs$(-10) )
```

