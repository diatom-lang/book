# Scope

Diatom use lexical scope. That means all names are resolved according lexical context.

## Variable Declaration

Diatom does not require variable to be declared before using. Variable is automatically declared the first time it is assigned with a value.

## Variable Shadowing 

Diatom disallows local variable to shadow outside ones. Names will always be resolved to outside ones if available. This is also applied to function parameters. They must not be the same name as a outside variable.

For example,
```diatom
a = []

def f() =
    a.push$(2)
end

f$()
```
`a` will have value `[2]` after execution.

## Local Scope

The following grammars enable local scope:
- Block: `begin` ... `end`
- Function: `def` ... `end`
- Lambda: `fn`

Variable declared in local scope is not available in outside scopes.
