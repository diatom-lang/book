# Identifier

> **Syntax**  
> Identifier:  [_a-zA-Z][_0-9a-zA-Z]\*  
>   
> **Note**: Unicode identifier is allowed but discouraged.

A valid identifier is a sequence of characters that satisfies the following conditions:
- The sequence must not start with `'0'..'9'`.
- The sequence must not contains whitespace characters, namely `' ', '\r', '\n', '\t'` .
- The sequence must not contains any ascii symbols like `?#$@%...` .
- Unicode characters may be used. For example, `🐱🐶` is valid identifier.
