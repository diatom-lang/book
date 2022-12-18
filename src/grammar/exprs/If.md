# If Expression

Condition code execution.

> **Syntax**  
> IfExpression:  
> if `<expression>` then (`<statement>`)\*  
> (elsif `<expression>` then (`<statement>`)\*)\*  
> end  

## Examples
```diatom
if true then
    1
end 

a = 5

if a > 5 then 
    1
elsif a > 4 then 
    -1
else 
    0
end
```

