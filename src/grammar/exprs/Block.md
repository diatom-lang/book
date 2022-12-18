# Block Expression

Multiple statements can be grouped as a block. A block also has its own scope.

> **Syntax**  
> BlockExpression:  
> begin ( `<statement>` )\* end

## Examples
```diatom
begin
    a = 1
    if a > 0 then
        return 0
    else 
        return 1
    end
end
```
