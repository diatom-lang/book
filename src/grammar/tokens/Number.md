# Numeric Literal

> **Syntax**  
> Number:  
> ( \[ 0 \] \[ Xx \] \[ \_0-9a-fA-F ]+)  
> |( \[ 0 \] \[ Bb \] [ \_0-1 ]+)  
> |( \[ 0 \] \[ Oo \] [ \_0-7 ]+)  
> |( \[ 0-9 \] [ \_0-9 ]\* ( \\.[ \_0-9 ]+ ){0,1} ( \[ Ee \] [ \\+\\- ]{0,1} [ 0-9_ ]\* ){0, 1} )

|Literals\*|Example|Exponentiation|
|:---|:---|:---|
|Decimal integer|`123_456`|N/A|
|Hex integer|`0xff1`|N/A|
|Octal integer|`0o72`|N/A|
|Binary integer|`0b1111_0100`|N/A|
|Floating point|`12.23e-5`|Optional|

\*: All number literals allow _ as a visual separator: `1_234.0E+18`  
\*: All characters are case insensitive.
