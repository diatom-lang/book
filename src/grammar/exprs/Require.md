# Require Expression (Not Implemented)

Diatom allows to import another file with require expression. This expression will return a module contains all variables after executing that file. This expression does not introduce any variables to global scope.

> **Syntax**
> RequireExpression:  
> require `<string literal>`

Note that the string literal must be in `a.b.c` or `a` form. There may not be characters except `[a-zA-Z0-9_\\-\\.]`.

## Examples
```diatom
util = require "myModule.util"
lib = require "lib"
```
