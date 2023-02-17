# Float::NAN

Not a Number (NaN).

The value of this depends on Rust version and platform.

> **[Description from Rust's std](https://doc.rust-lang.org/std/primitive.f64.html#associatedconstant.NAN)**  
> Note that IEEE 754 doesn’t define just a single NaN value; a plethora of bit patterns are considered to be NaN. Furthermore, the standard makes a difference between a “signaling” and a “quiet” NaN, and allows inspecting its “payload” (the unspecified bits in the bit pattern). This constant isn’t guaranteed to equal to any specific NaN bitpattern, and the stability of its representation over Rust versions and target platforms isn’t guaranteed.

### Type
```haskell
NAN :: Float
```

### Examples
```diatom
println$( Float::NAN )
println$( Float::NAN.is_nan$() )
```

