# CheatSheet-Go
This is a Repository for a cheatsheet for go in englisch

First things first is **how to write a comment**
```go
// for one Line comment
/* For more than one line comment*/
```

The other importent first thing to know are Operators in Go

This is a list of all the Operator types in Go and what they're are

## Operators in Go
The Operators in Go are 
- Arithmetic
- Comparison
- Logical
- Bitwise
- Assignment
- Unary
- Other
---
### Arithmetic 
+ '+' == Addition
+ '-' == Subtraction
+ '*' == Multiplication
+ '/' == Division
+ '%' == Modulus
---
### Comparison Operators: Used to compare values
+ '==' == Equal to
+ '!=' == Not equal to
+ '<' == Less than
+ '<=' == Less than or equal to
+ '>' == Greater than
+ '>=' == Greater than or equal to
---
### Logical:
+ '&&' == Logical AND
+ '||' == Logical OR
+ '!' == Logical NOT
---
### Bitwise:
+ '&' ==  Bitwise AND
+ '|' ==  Bitwise OR
+ '^' == Bitwise XOR (exclusive OR)
+ '&^' ==  Bit clear (AND NOT)
+ '<<' ==  Left shift
+ '>>' ==  Right shift
---
### Assignment: Used to assign values to variables
+ '=' ==  Simple assignment
+ '+=' ==  Addition assignment
+ '-=' ==  Subtraction assignment
+ '*=' ==  Multiplication assignment
+ '/=' ==  Division assignment
+ '%=' ==  Remainder assignment
+ '<<=' ==  Left shift assignment
+ '>>=' ==  Right shift assignment
+ '&=' ==  Bitwise AND assignment
+ '|=' == Bitwise OR assignment
+ '^=' == Bitwise XOR assignment
+ '&^=' == Bit clear assignment
---
### Unary Operators: Operate on a single operand.
+ '+' == Unary plus (sign)
+ '-' == Unary minus (negation)
+ '++' == Increment
+ '--' == Decrement
+ '!' == Logical NOT
---
### Other Operators:
+ '.' == Struct field access
+ '[]' == Slice, array indexing
+ '()' == Function call, grouping expressions
+ ':' == Used in declarations, switch cases, and composite literals
+ '...' == Variadic arguments, slice unpacking
+ ',' == Separator in function arguments, composite literals, and more
---
The Next thing you need to know are Variables and how to use them,

there are many types of Variables in Go 

## Variables in Go
- Normal
- Signed
- Unsigned

### Normal Variables in Go
These are you're typical Variables that also exist in many other Languages
- 'byte' == Is a Variable that represents a range of 0 to 255. Can also use as a Ascii Letter
- 'int' == The Range of the int in Go is defined with the architecture of the you're Computer you using either 32bit or 64bit
- 'float32' == Is a Varaible that is used for a single decimal Number like 1.5769
- 'float64' == Is a larger Variable than float32
- 'rune' == Is for a Unicode Code Point Letter or symbole like Chinese letters or the German Ä Ü Ö
- 'string' == Is a Variable where you can save Sentences and not just a letter or Symbole
- 'bool' == Is a Variable for Logical Operation it saves 'true' or 'false'
- 'Complex64' == Is a Variable for Complex numbers
- 'Complex128' == Is a Larger Variable than Complex64
---
### Signed Variables in Go
These are Variables that can go in the minus area of Numbers 

Normaly when you write the Variables in the Above list, these are then normally signed
- 'int8' == It has a range of -128 to 127
- 'int16' == It has a range of -32768 to 32767
- 'int32' == It has a range of -2147483648 to 2147483647
- 'int64' == It has a range of -9223372036854775808 to 9223372036854775807

### Unsigned Variables in Go
These are the Variables that can not go into the minus area

but these Variables have a greater range in the Plus range
- 'uint8' == It has a range of 0 to 255
- 'uint16' == It has a range of 0 to 65535
- 'uint32' == It has a range of 0 to 4294967295
- 'uint64' == It has a range of 0 to 18446744073709551615
- 'uintptr' == An unsigned integer type that is large enough to store the uninterpreted bits of a pointer value.



