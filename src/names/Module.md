# Module

Diatom can load external diatom source code files as modules.

## Search Path

Search path is a set of paths where diatom compiler looking for possible modules. There are several ways to add search path.
 - Relative path: When parsing a file, the file's directory is automatically added to search path and takes the highest priority.
 - Other search path: Search path can also be specified by host.
 - Console: Diatom Console will add current work directory to search path.

## Resolve Rule

Module string like "a.b.c" will be resolved to `<search path>/a/b/c.dm` or `<search path>/a/b/c/mod.dm`. Diatom will always search module according to priority and immediately return when the first module matched is found.

Diatom will only execute a module once and use cached value when the same module is loaded.

## Access Module Members

Require expression will return a module. All variables declared in the module file will be a member of the module and be accessed via `.` operator.

```diatom 
-- lib.dm
version = "0.1.1"

def sum (x y z) =
    x + y + z
end

-- main.dm
lib = require "lib"
lib.version
lib.sum$( 1 2 3 )
```
