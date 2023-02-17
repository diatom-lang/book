# Meta Table

A meta table is just a normal table can contains any keys.

Meta table is used to abstract a common behavior among multiple tables. It can **ONLY** be set at **the creation of a table**. After that you can not set a new meta table or get current meta table out.

Modify meta table from a table is also limited due to assign to table keys will not be resolved to meta table.

This example will **NOT** work.
```diatom
table = {}

meta = {
    my_method = 
        fn x = x + 1
}

table <- meta
```
