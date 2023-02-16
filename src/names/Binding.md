# Binding and Closure

## Assignment Rules

All **primitive types** in diatom are unboxed and will be **passed by value**. This includes

- Unit
- Int
- Float
- Bool
- String

```diatom
i = 1
alias = i
alias = 2

println$('i =', i)
println$('alias =', alias)
```

**Lists, tuples and tables** are stored in heap. Thus these value shall be **passed by reference**. External functions and closures also follow this rule.

```diatom
l = [1, 2]
alias = l

alias.append$(3)

println$('l =', l)
println$('alias =', alias)
```

## Closure

Closure may capture variables which is not by value but directly aliases the variable. The captures are still effective even if variables go out of scope.

```diatom
-- declare variable x1 & x2
x1 = () x2 = ()
f = 
    fn = begin
        a = 1
        -- x1 captures `a`
        x1 = 
            fn = a
        -- x2 also captures `a`
        x2 = 
            fn x = begin 
                a = x
            end
    end
-- initialize x1 & x2 
f$()

-- modify `a` (decalred in `f`) which has
-- already go out of scope via `x2`
x2$(10)

-- `a` captured by x1 is also modified
println$(x1$())
```
