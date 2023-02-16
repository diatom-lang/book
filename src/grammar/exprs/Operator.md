# Operator Expressions

For operators and precedences, see [_Operators_].

> **Syntax**  
> OperatorExpression:  
> `<prefix>` `<expression>`  
> | `<expression>` `<infix>` `<expression>`  
> | `<expression>` `<postfix>`

## Examples
```diatom
a = 12345

println$(
    a // 3,
    a > 12344,
    a + 5,
    a ** 4,
    a - -2,
    a.float$(),
    a / Float::INF
)
```

[_Operators_]: ../Tokens.md

