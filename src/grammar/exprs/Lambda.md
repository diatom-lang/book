# Lambda Expression

Lambda expression is used as an anonymous function.

> **Syntax**  
> LambdaExpression:  
> fn ( `<identifier>` )\* = `<expression>`

Examples:
```diatom
-- lambda takes a single expression
add3 = 
    fn a b c = a + b + c
println$( add3$(1, 2, 3) )

-- To use multiple expression/statements
-- Group them in a block expression
(fn x = begin
    loop 
        if x == 0 then
            break
        else 
            x = x//2
        end
    end
    println$('loop finished')
end) $(Int::MAX) -- Directly call lambda
```

