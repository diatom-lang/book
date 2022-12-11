# Statement

Statements are chunk of code that always return `nil` except if it is an expression itself.

## 1 Flow Control

`return`, `break` and `continue` are three keywords used as flow control statements. `return` may optioinally take an argument.

Examples:
```diatom
def f ()
    a = 1
    if a > 3 then
        return true -- return a value
    end
    return -- Return nothing (nil)
end

for i in 1..10 do
    if i < 5 then
        continue
    else 
        break
    end
end

```

## 2 Loop

There are three types of loops in diatom:
 - `loop`: infinite loop
 - `until`: loop until a break condition is met
 - `for`: loop through an Iterator

 The syntaxes are:
 - `loop`: `loop` + `<body>` + `end`
 - `until`: `until` + `<condition>` + `do` + `body` + `end`
 - `for`: `for` + `<variables>` + `in` + `<iterator>` + `do` + `<body>` + `end`

Examples:
```diatom
a = 0

loop 
    if a > 5 then
        break
    else 
        a = a + 1
    end
end

until a > 5 do
    a = a + 1
end

for i,v in (1..10).iter$().enumerate$() do
    a = a + i + v*a
end
    
```

## 3 Class

Work in progress...
