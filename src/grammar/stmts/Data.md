# Data Type Statement

Keyword `data` is used to create custom data types.
> **Syntax**  
> DataStatement:  
> data `<identifier>` =  
> ( `<identifier>` ( `<identifier>` )\* )+  
> `<FunctionStatement>`\*  
> end

## Examples
```diatom
-- Data with multiple variants
data Maybe =
    Just x    -- Create a constructor called 'Just' with a member called 'x'
    | Nothing -- Create a constructor called 'Nothing' with no member

    -- followed by member functions
    def is_just(self) = 
        case self of
            Just${_} => true
            _ => false
        end
    end
end

-- Call constructors
-- with named parameters
Just${x: 1}
-- without names
Just${1}

-- Data Constructor may have the same name as the data type
data Circle = Circle r end
data Rect = Rect x y
    def area(self) = 
        self.x * self.y
    end
end

Circle${1}
Rect${ 10 20 }
```
