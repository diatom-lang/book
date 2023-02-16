# Operators

> **Syntax**:
> Operator:  
> `<singular operator>`  
> | $ \\( `<expression>`\* \\)  
> | $ \\[ `<expression>`\* \\]  
> | $ \\{ (`<expression>`\*) | (`<identifier>` : `<expression>`)\* \\}

Here is a list of all operators.

|Operator|Meaning|Example| Precedence (left and right) |
|:---|:---|:---|:---|
|.| access member | `[1,2].len$()` | 23,24 |
|::| access member | `List::len$([1,2])` | 23,24 |
|<-| set meta-table | `{} <- MetaTable` | 21,22 |
|not| logic not | `not false` | 19 (prefix) |
|$()| function call | `f$()` | 20 (postfix) |
|$[]| index array| `list$[0]`| 20 (postfix) |
|${}| data constructor | `Just${1}`| 20 (postfix) |
|\*\*| power | `2**3` | 17,18 |
|\*| multiply | `2*3` | 15,16 |
|//| integer division  | `7//3` | 15,16 |
|/| division | `7/3` | 15,16 |
|%| modular | `5%2` | 15,16 |
|+| addiction | `1+2`| 13,14 |
|-| subtract or negative value | `1-2` `-2` | 19 (prefix) 13,14 (infix)|
|>| greater than | `5>4` | 11,12 |
|>=| greater than or equal to | `4>=3` | 11,12 |
|<| less than | `2<6` | 11,12 |
|<=| less than or equal to | `5<=5` | 11,12 |
|==| equal to | `3==3` | 11,12 |
|is| compare reference | `{} is []` | 11,12 |
|<>| not equal to | `5<>4` | 11,12 |
|and| logic and | `true and false` | 9, 10|
|or| logic or | `true or false` | 7,8 |
|..| range | `1..10`| 5,6 |
|,| create a tuple | `1,2,3` | 1,2 |
|=| assign value to variable | `a=5`| 4,3|

