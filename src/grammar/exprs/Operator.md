# Operator Expressions

For operators and precedences, see [_Operators_].

> **Syntax**  
> OperatorExpression:  
> `<prefix>` `<expression>`  
> | `<expression>` `<infix>` `<expression>`  
> | `<expression>` `<postfix>`

## Examples
```diatom
a = 1
a // 10
Just${1}
[1 2 3]$[2] -- 2
[1 2 3 4].len$()
1,2,3 -- tuple
```

[_Operators_]: ../Tokens.md

