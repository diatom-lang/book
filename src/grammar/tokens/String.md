# String Literal

String literals are any characters surrounded by a pair of `"` or `'`. Any utf-8 characters may be included. To use special characters, you may put a `\` before that escape sequence. Here is a list of all escape sequence.

> **Syntax**  
> String:  
> ' ( \[^\\\\\] | EscapeSequence | \\\\' )\* '  
> | " ( \[^\\\\\] | EscapeSequence | \\\\" )\* "  
>  
> EscapeSequence:  
> \\\\x [0-7]{2}  
> | \\\\u [0-9a-fA-F]{4}  
> | \\\\U [0-9a-fA-F]{8}  
> | \\\\r | \\\\n | \\\\t | \\\\  

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
