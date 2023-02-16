# If Expression

Condition code execution.

> **Syntax**  
> IfExpression:  
> if `<expression>` then (`<statement>`)\*  
> (elsif `<expression>` then (`<statement>`)\*)\*  
> end  

## Examples
```diatom
def test x =
    if x > 0 then
        println$('positive')
    elsif x == 0 then 
        println$('zero')
    else
        println$('negative')
    end
end

test$(1)
test$(0)
test$(-1)
```

