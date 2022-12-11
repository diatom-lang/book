# Expressions

Diatom is an expression based language, which means almost everything is an expression. Here is a list of all current expressions and their grammar.

## 1 Arithmetic Expressions

Arithmetic expressions are expression combined by an infix or prefix or postfix operator.

```diatom
 a = (1+3)**3
 a = a // 10
 a

```

## 2 Function declaration

Function declaration contains `def` + `name(optional)` + `( <parameters> )` + `body` + `(optional) where <binds>` + `end`. This expression always return the function it self.

Note: If the name is omitted, then it is considered as a lambda expression.

Examples:
```diatom
def f(a b c)
    a + b + c 
end

def f ()
    g$()
where
    g: def () 1 end
end

```

## 3 If expression

`If` expression contains `if` + `<condition>` + `then` + `<body>` + `(optional) elsif <condition> then <body>` + `(optional) else <body>` + `end`. This expression returns the last expression of body's value.

Examples:
```diatom
if true then
    1
end 

a = 5

if a > 5 then 
    1
elsif a > 4 then 
    -1
else 
    0
end

```

## 4 Block

Multiple statements can be grouped as a block. A block also has its own scope.

Examples:
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

## 5 Built in Data Structure

Diatom has `dictionary`, `set`, `tuple` and `list` as built in data structures.

Note: No comma required or allowed as separator in all data structures. Except for `tuple`, `tuple` is created by `,` operator and does not require parentheses.

Examples:
```diatom
-- list
[]
[ 1 2 3 ]

-- set
{}
{ 1 2 3 }

-- dictionary
{:}
{ "key1": 1 "key2": 2 "key3": 3 }

-- tuple (Must contains at least two elements)
a,b,c
a,(b,c) -- use parentheses for precedence

```

## 6 Constant values

The following values are considered as expressions.

```diatom
0x123 -- numerical literal

"abc" -- string literal

true false -- boolean value

nil

```
