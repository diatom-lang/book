# Expressions

Diatom is an expression based language, which means almost everything is an expression. Here is a list of all current expressions and their grammar.

## 1 Arithmetic Expressions

Arithmetic expressions are expression combined by an infix or prefix or postfix operator.

```diatom
a = 1
a // 10
Just${1}
[1 2 3]$[2] -- 2
[1 2 3 4].len$()
1,2,3 -- tuple

```

## 2 Lambda Expression

Lambda expression contains `fn` + `<parameters>` + `=` + `<expression>`. Parameters are separated by space.

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

() -- unit type value

```

## 7 Case Expression

Case expression is used to perform pattern matching.

The grammar is `case` + `<expression>` + `of` + `<pattern> (if <guard expression>)? => <expression>`\* + `end`.

Pattern can be 
- Or form: `<pattern> | <pattern>`
- Tuple: `<pattern> , <pattern>`
- Match data: `<constructor>${ <variable> <variable> ... }`
- Constant Literal: `1 "str" true ...`
- Bind: `<variable name> @ pattern`

Priority: `()` > `@` > `,` > `|`
Examples:
```diatom
case Just${1} of 
    x @(Just${1} | Just${_}) => true
    Nothing => false
end

```
