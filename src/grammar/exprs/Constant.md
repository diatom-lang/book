# Constant values

Constant values or built in data structures. Diatom has `dictionary`, `set`, `tuple` and `list` as built in data structures.

> **Syntax**  
> ConstantExpression:  
> `<number>` | `<string>` | true | false | \\( \\)  
> | \\{ `<expression>`\* }  
> | \\{ : \\} | \\{ (`<expression>`:`<expression>`)\* \\}  
> | \\[ (`<expression>`)\* \\]  
> | `<identifier>`

## Examples

```diatom
0x123 -- numerical literal

"abc" -- string literal

true false -- boolean value

() -- unit type value
println$(())

-- list
println$([1, 2, 3], [])

-- Table
println$({key1 = 1, key2 = 'key'}, {})

-- tuple (Must contains at least two elements)
t1 = (1, 3, '?')
t2 = (1.2, (4, 5)) -- use parentheses for precedence
println$(t1, t2)
```

