# Function Statement

Function statement declares a function and bind the name to that function in current scope.

> **Syntax**  
> FunctionStatement:  
> def `<identifier>``<identifier>`\* =  
> `<statement>`\*  
> end

## Examples
```diatom
def add3 a b c =
    a + b + c 
end

println$( add3$(1, 2, 3) )
```

