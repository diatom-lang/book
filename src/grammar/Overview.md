# Grammar

This chapter is about the grammar of diatom.

## General Grammar Rules

Diatom's grammar is design around the following concept in mind:
 - **No delimiter**: Statements and Expressions does not require `newline` or `;` to be separated from each other. That means `a = 1 b = 2` is a perfectly fine line of code.
 - **Fewer Punctuations**: Diatom significantly reduces the need of redundant punctuations like `() {}` pairs. Blocks uses keywords instead of `{}` and tuples does not need to be surrounded by `()`. Instead just write `a,b` is enough to make a tuple. `[1 2 3]` is a good list in diatom, no comma is required or allowed.
 - **Format independent syntax**: Diatom does not use so called significant whitespace in its grammar. You are free to format you code without changing its meanings. To prevent unintended behaviors, most of the grammar requires some kind of terminator like `if ... then ... end` so user will not accidentally write to wrong scopes.
 - **Expression based**: Every expression( including block ) has a return value. Simply put an expression at the end of the block will automatically return its value. For example, `fn x = x + 1` will just return `x + 1`, no `return` is needed.
