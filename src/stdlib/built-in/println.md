# println

Print anything to output buffer (usually is managed by host program). It may accepts **any amount** and **any kind of parameters**. Will **NOT** run into infinite loop if data to be printed is cycled.

If output buffer can not be written (such as tcp stream is closed), it will **panic**.

#### Example
```diatom
table = { ref = () }
table.ref = table

println(table, 1, "asm", false, 1.234, ())
```
