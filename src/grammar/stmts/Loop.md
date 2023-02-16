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
println$(a)

a = 0
until a > 5 do
    a = a + 1
end
println$(a)

a = 0
for _ in 0..6 do
    a = a + 1
end
println$(a)
```
