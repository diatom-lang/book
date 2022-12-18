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

Here is a list of all current keywords.
```markdown
where until end if then else elsif case in for do
assert return break continue loop class def begin
```

### 2.4 Identifier

A valid identifier is a sequence of characters that satisfies the following conditions:
- The sequence must not start with `'0'..'9'`.
- The sequence must not contains whitespace characters, namely `' ', '\r', '\n', '\t'` .
- The sequence must not contains any ascii symbols like `?#$@%...` .
- Unicode characters may be used. For example, `🐱🐶` is valid identifier.

### 2.5 Operators

Here is a list of all operators.

|Operator|Meaning|Example| Precedence (left and right) |
|:---|:---|:---|:---|
|.| access member | `list.len$()` | 21,22 |
|not| logic not | `not false` | 19(prefix) |
|$()| function call | `f$()` | 20(postfix) |
|$[]| index array| `list$[0]`| 20(postfix) |
|${}| data constructor | `Just${1}`| 20(postfix) |
|**| power | `2**3` | 17,18 |
|*| multiply | `2*3` | 15,16 |
|//| integer division  | `7//3` | 15,16 |
|/| division | `7/3` | 15,16 |
|%| modular | `5%2` | 15,16 |
|+| addiction | `1+2`| 13,14 |
|-| subtract or negative value | `1-2` `-2` | 101(prefix) 13,14(infix)|
|>| greater than | `5>4` | 11,12 |
|>=| greater than or equal to | `4>=3` | 11,12 |
|<| less than | `2<6` | 11,12 |
|<=| less than or equal to | `5<=5` | 11,12 |
|==| equal to | `3==3` | 11,12 |
|<>| not equal to | `5<>4` | 11,12 |
|and| logic and | `true and false` | 9, 10|
|or| logic or | `true or false` | 7,8 |
|..| range | `1..10`| 5,6 |
|,| create a tuple | `1,2,3` | 3,4 |
|=| assign value to variable | `a=5`| 2,1|
|:| N/A | N/A | N/A |

