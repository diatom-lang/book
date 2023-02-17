# Method Call

If a table's entry or its meta table's entry is a closure, it is possible to call this closure as a **method** or **member function**. 

A method will implicitly pass the caller itself as the first parameter.
```diatom
def my_add self x =
    self.value + x
end

MyInt = { 
    my_add = my_add
}

my_int = { value = 1, my_add2 = my_add } <- MyInt
println$( my_int.my_add$(10) )
println$( my_int.my_add2$(10) )
```

Sometimes you may want to call a static method by not passing the caller, in which case you can use `::` operator instead of `.`. It is also recommended to use static value such as `Int::MAX` with `::` instead of `Int.MAX`.

```diatom
def my_add self x =
    self.value + x
end

MyInt = { 
    my_add = my_add
}

my_int = { value = 1, my_add2 = my_add } <- MyInt
println$( MyInt::my_add$( my_int, 10 ) )
```
