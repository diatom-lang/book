# Lambda Expression

Lambda expression is used as an anonymous function.

> **Syntax**  
> LambdaExpression:  
> fn ( `<identifier>` )\* = `<expression>`

Examples:
```diatom
fn x y z = x + y + z

-- To use multiple expression/statements
-- Group them in a block expression
fn x y = begin
    if x > 10 then
        return y
    end
    until x > 10 do
        y = y + x
        x = x + 1
    end
    y
end
```

