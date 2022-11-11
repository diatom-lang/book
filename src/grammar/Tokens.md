# Tokens and Literals

When you program is passed to the interpreter, it will first be analyzed by the `Lexer` which will breaks the source code into tokens and then feeds them to the `Parser`.

## 1. Overview of All Kinds of Tokens

- `Numeric`   : A 64-bits signed integer or floating point number.
- `String`    : A string literal.
- `Keywords`  : Keywords defined by grammar.
- `Identifier`: Identifier for variables.
- `Operator`  : Operators.

## 2. Details of Lexer Implementation
### 2.1 Numeric Literal

|Literals\*|Example|Exponentiation|
|:---|:---|:---|
|Decimal integer|`123_456`|N/A|
|Hex integer|`0xff1`|N/A|
|Octal integer|`0o72`|N/A|
|Binary integer|`0b1111_0100`|N/A|
|Floating point|`12.23e-5`|Optional|

\*: All number literals allow _ as a visual separator: `1_234.0E+18`  
\*: All characters are case insensitive.

### 2.2 String Literal

String literals are any characters surrounded by a pair of `"` or `'`. Any utf-8 characters may be included. To use special characters, you may put a `\` before that escape sequence. Here is a list of all escape sequence.

|Escapes| Character|
|:---|:---|
|`\\`| backslash|
|`\r`|Newline|
|`\n`|Carriage return|
|`\t`| Tab|
|`\x41`|7 bit character code (exactly 2 hex numbers\*)|
|`\u00E9`|16bit unicode escape(exactly 4 hex numbers\*)|
|`\U000000E9`|16bit unicode escape(exactly 8 hex numbers\*)|

\*: All hex numbers ignore case. 

### 2.3 Keywords

Work in progress...

### 2.4 Identifier

A valid identifier is a sequence of characters that satisfies the following conditions:
- The sequence must not start with `'0'..'9'`.
- The sequence must not contains whitespace characters, namely `' ', '\r', '\n', '\t'` .
- The sequence must not contains any ascii symbols like `?#$@%...` .
- Unicode characters may be used. For example, `🐱🐶` is valid identifier.

### 2.5 Operators

Work in progress...
