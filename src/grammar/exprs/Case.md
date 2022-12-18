# Case Expression

Case expression is used to perform pattern matching.

> **Syntax**  
> CaseExpression:  
> case `<expression>` of  
> ( `<pattern>` ( if `<expression>` )? => `<expression>` )\*   
> end  
> 
> Pattern: 
> `<pattern>` \\| `<pattern>`  
> | `<pattern>` , `<pattern>`  
> | `<constructor>` $ \\{ `<variable>`\* \\}  
> | `<constant>`  
> | `<identifier>` @ `<pattern>`  
> | \\( `<pattern>` \\)
> 
> Priority: `()` > `@` > `,` > `|`


## Examples
```diatom
case Just${1} of 
    x @(Just${1} | Just${_}) => true
    Nothing => false
end
```
