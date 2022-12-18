# Flow Control Statement

These statement alters execution flow in a function or a lambda expression.

> **Syntax**  
> FlowStatement:  
> break  
> | continue  
> | return `<expression>`?

## Examples
```diatom
def f () = 
    a = 1
    if a > 3 then
        return true -- return a value
    end
    return -- Return nothing (nil)
end

for i in 1..10 do
    if i < 5 then
        continue
    else 
        break
    end
end
```
