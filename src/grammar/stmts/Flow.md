# Flow Control Statement

These statement alters execution flow in a function or a lambda expression.

> **Syntax**  
> FlowStatement:  
> break  
> | continue  
> | return `<expression>`?

## Examples
```diatom
def f a = 
    if a > 3 then
        return true -- return a value
    end
    return -- Return nothing (Unit)
end

println$( f$(5), f$(-1) )

for i in 1..10 do
    if i < 5 then
        print$(i, '')
        continue
    else 
        println$('Break: i =', i)
        break
    end
end
```
