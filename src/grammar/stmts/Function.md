# Function Statement

Function statement declares a function and bind the name to that function in current scope.

> **Syntax**  
> FunctionStatement:  
> def `<identifier>` \\( `<identifier>`\* \\) =  
> `<statement>`\*  
> end

## Examples
```diatom
def f(a b c) =
    a + b + c 
end

def f () =
    g$(x)
where
    g = fn x = x.upper$()
    x = "str"
end
```

