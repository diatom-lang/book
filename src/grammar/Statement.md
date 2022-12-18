# Statement

Statements are chunk of code that always return `nil` except if it is an expression itself.

## 1. Flow Control

`return`, `break` and `continue` are three keywords used as flow control statements. `return` may optioinally take an argument.

Examples:
```diatom
def f () = 
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

## 2. Loop

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

## 3. Function Declaration

Function declaration contains `def <name> ( <parameters> ) =` + `body` + `(optional) where <binds>` + `end`. 

Examples:
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

## 4. Custom Data Type

Keyword `data` is used to create custom data types.
Grammar: `data <name> = <constructor1> <variables> | <constructor1> <variables> | ...` + `<member functions>` + `end`.

Examples:
```diatom
-- Data with multiple variants
data Maybe =
    Just x    -- Create a constructor called 'Just' with a member called 'x'
    | Nothing -- Create a constructor called 'Nothing' with no member

    -- followed by member functions
    def is_just(self) = 
        case self of
            Just${_} => true
            _ => false
        end
    end
end

-- Call constructors
-- with named parameters
Just${x: 1}
-- without names
Just${1}

-- Data Constructor may have the same name as the data type
data Circle = Circle r end
data Rect = Rect x y
    def area(self) = 
        x * y
    end
end

```
