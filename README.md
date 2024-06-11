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
---
### How to declare and initialize Variables
You need to declare variables in Go so that you can use them, remember that if you write the Variable name in caps
it is public else it is private
```go
// declaring
// You can declare a variable with var <name> <type>
var a int
var b rune
var a,b,c,d int

//You can also declare a variable with const <name> <typer>
// But you can't change the variable anymore
const a int
const b rune

//Initializing
// You can do it with the declaring type
var a int = 6
const a rune = 'A'
a := 2 //It is only local available

// You can also initialize many variables in the same line
var a, b, c ,d ,e int = 1, 2, 3, 4, 5
var a, b = 6, "Hello" without the type
a,b,c,d := 10,'P',10.1,'Ü' // These are also only localy available
```
---
### How to use the Variables
You know how to declare and initialize variables but what can you do 
with them now
You can do basicly anything with them with the operators
```go
var a int = 6
b := 5
c := a+b //By the way it is 11
```
---
 ### Pointers 
 In Golang and for example c there is something like a pointer 
 they are used so that you don't need to declare a variable
 anytime you want to use a a value of another variable 
```go
//declaring a pointer
var a int = 42  // Regular variable with value 42
var ptr *int    // Pointer variable to store an int address
ptr = &a        // Assign the address of 'a' to the pointer 'ptr'

//dereferencing Pointers
value := *ptr  // Dereference 'ptr' to get the value stored at its address (which is 42)
fmt.Println(value) // Output: 42

//modifying Values through Pointers
*ptr = 100    // Modify the value stored at the address pointed to by 'ptr' (which is 'a')
fmt.Println(a)  // Output: 100 (original variable 'a' is now modified)
```

