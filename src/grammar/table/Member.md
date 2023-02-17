# Member Resolution

Operator `.` and `::` are used to access member of a table.  
Diatom interpreter will looks up table entries first, if failed then it will try to look up the table's meta table entries.

```diatom
meta_table = {meta_key = 2}
-- Create a table with meta table
table = {key1 = 0, key2 = 1} <- meta_table

println$('table.key1 =', table.key1)
println$('table.meta_key =', table.meta_key)
```

However, assign to a table will **NOT** be resolved to meta table. In which case will create a new key inside this table.
```diatom
meta_table = {meta_key = 2}
-- Create a table with meta table
table = {key1 = 0, key2 = 1} <- meta_table

table.meta_key = 3

println$('table.meta_key =', table.meta_key)
println$('meta_table.meta_key =', meta_table.meta_key)
```
