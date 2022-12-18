# Loop Statement

There are three types of loops in diatom:
 - `loop`: infinite loop
 - `until`: loop until a break condition is met
 - `for`: loop through an Iterator

> **Syntax**  
> LoopStatement:  
> loop `<statement>`\* end  
> | until `<expression>` do `<statement>`\* end  
> | for `<expression>` in `<expression>` do  
>   `<statement>`\*  
>   end

## Examples
```diatom
a = 0

loop 
    if a > 5 then
        break
    else 
        a = a + 1
    end
end

until a > 5 do
    a = a + 1
end

for i,v in (1..10).iter$().enumerate$() do
    a = a + i + v*a
end
```
