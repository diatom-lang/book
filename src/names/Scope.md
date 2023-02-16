# Scope

Diatom use lexical scope. That means all names are resolved according lexical context.

## Variable Declaration

Diatom does not require variable to be declared before using. Variable is automatically declared the first time it is assigned with a value.

## Variable Shadowing 

Diatom disallows local variable to shadow outside ones. Names will always be resolved to outside ones if available. This is also applied to function parameters. They must not be the same name as a outside variable.

For example,
```diatom
a = 1
def f x =
    a = x
end
f$(2)

println$('a =', a)
```
`a` will have value `2` after execution.

## Local Scope

The following grammars enable local scope:
- Block: `begin` ... `end`
- Function: `def` ... `end`
- Lambda: `fn`
- Loop/For: `loop` ... `end`, `for` ... `end`, `until` .. `do` ... `end`

Variable declared in local scope is not available in outside scopes.

The following code will **NOT** work.
```diatom
begin
    a = 10
end
println$(a)
```
