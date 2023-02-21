# unreachable

Cause panic if executed. Useful to mark unreachable codes.

```diatom 
def my_func =
    if false then
        unreachable()
    end
end

my_func()
println('success')
```
