# List

A dynamic array that can contains any items.

```diatom
-- Create an empty list
list = []
println$(list)

-- List with a single item
list = [1]
println$(list)

-- List with multiple items
list = [1, 'string', false]
println$(list)
```

### Type
```haskell
List :: [a]
```

### Meta Table

`List` type's meta table is stored in variable named `List`.

```diatom
l = [1, 2, 3]
List::append$(l, 4)
println$(l)
```

### Index

List may by index by `Int` type. Both **postive** and **negative** will work.

```diatom
l = [1, 2, 3, 4]
println$( l$[0], l$[3] )
println$( l$[-4], l$[-1] )
```

### Iterate

List can be used in `for` loop or as an iterator.

```diatom
-- for loop
for i in [1, 2, 3] do
    print$(i, '')
end
println$('\n')

-- get an iterator
list = [1, 2, 3]
iterator = list.iter$()
println$( iterator.__next$() )
println$( iterator.__next$() )
println$( iterator.__next$() )
println$( iterator.__next$() is Option::None )
println$(list)
```



