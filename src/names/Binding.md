# Binding and Capture

## !Discussion Required!
Diatom will always capture variable by reference unless they are primitive types or string.

These types are considered as immutable so that they will not be accidentally modified.
This includes:
 - Int 
 - Float 
 - Boolean
 - String
 - Unit ( It only has one possible value anyway. )


 **Note**: In the future version of diatom, this behavior will be applied to all instance of `Immutable` class.
