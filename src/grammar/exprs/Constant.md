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

-- list
[]
[ 1 2 3 ]

-- set
{}
{ 1 2 3 }

-- dictionary
{:}
{ "key1": 1 "key2": 2 "key3": 3 }

-- tuple (Must contains at least two elements)
a,b,c
a,(b,c) -- use parentheses for precedence
```

