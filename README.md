# CheatSheet-Go
This is a Repository for a cheatsheet for Golang in englisch

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
+ '+' :  Addition
+ '-' :  Subtraction
+ '*' :  Multiplication
+ '/' :  Division
+ '%' :  Modulus
---
### Comparison Operators: Used to compare values
+ '==' : Equal to
+ '!=' : Not equal to
+ '<'  : Less than
+ '<=' : Less than or equal to
+ '>'  : Greater than
+ '>=' : Greater than or equal to
---
### Logical:
+ '&&' : Logical AND
+ '||' : Logical OR
+ '!'  : Logical NOT
---
### Bitwise:
+ '&' :  Bitwise AND
+ '|' :  Bitwise OR
+ '^' :  Bitwise XOR (exclusive OR)
+ '&^' :  Bit clear (AND NOT)
+ '<<' :  Left shift
+ '>>' :  Right shift
---
### Assignment: Used to assign values to variables
+ '='   :  Simple assignment
+ '+='  :  Addition assignment
+ '-='  :  Subtraction assignment
+ '*='  :  Multiplication assignment
+ '/='  :  Division assignment
+ '%='  :  Remainder assignment
+ '<<=' :  Left shift assignment
+ '>>=' :  Right shift assignment
+ '&='  :  Bitwise AND assignment
+ '|='  :  Bitwise OR assignment
+ '^='  :  Bitwise XOR assignment
+ '&^=' :  Bit clear assignment
---
### Unary Operators: Operate on a single operand.
+ '+'   : Unary plus (sign)
+ '-'   : Unary minus (negation)
+ '++'  : Increment
+ '--'  : Decrement
+ '!'   : Logical NOT
---
### Other Operators:
+ '.'   : Struct field access
+ '[]'  : Slice, array indexing
+ '()'  : Function call, grouping expressions
+ ':'   : Used in declarations, switch cases, and composite literals
+ '...' : Variadic arguments, slice unpacking
+ ','   : Separator in function arguments, composite literals, and more
---
The Next thing you need to know are Variables and how to use them,

there are many types of Variables in Go 

## Variables in Go
- Normal
- Signed
- Unsigned

### Normal Variables in Go
These are you're typical Variables that also exist in many other Languages
- 'byte'    :  Is a Variable that represents a range of 0 to 255. Can also use as a Ascii Letter
- 'int'     : The Range of the int in Go is defined with the architecture of the you're Computer you using either 32bit or 64bit
- 'float32' : Is a Varaible that is used for a single decimal Number like 1.5769
- 'float64' : Is a larger Variable than float32
- 'rune'    : Is for a Unicode Code Point Letter or symbole like Chinese letters or the German Ä Ü Ö
- 'string'  : Is a Variable where you can save Sentences and not just a letter or Symbole
- 'bool'    : Is a Variable for Logical Operation it saves 'true' or 'false'
- 'Complex64' : Is a Variable for Complex numbers
- 'Complex128': Is a Larger Variable than Complex64
---
### Signed Variables in Go
These are Variables that can go in the minus area of Numbers 

Normaly when you write the Variables in the Above list, these are then normally signed
- 'int8'  : It has a range of -128 to 127
- 'int16' : It has a range of -32768 to 32767
- 'int32' : It has a range of -2147483648 to 2147483647
- 'int64' : It has a range of -9223372036854775808 to 9223372036854775807

### Unsigned Variables in Go
These are the Variables that can not go into the minus area

but these Variables have a greater range in the Plus range
- 'uint8'   : It has a range of 0 to 255
- 'uint16'  : It has a range of 0 to 65535
- 'uint32'  : It has a range of 0 to 4294967295
- 'uint64'  : It has a range of 0 to 18446744073709551615
- 'uintptr' : An unsigned integer type that is large enough to store the uninterpreted bits of a pointer value.
---
## How to declare and initialize Variables
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
var a, b = 6, "Hello" //without the type
a,b,c,d := 10,'P',10.1,'Ü' // These are also only localy available
```
---
## How to use the Variables
You know how to declare and initialize variables but what can you do 
with them now
You can do basicly anything with them with the operators
```go
var a int = 6
b := 5
c := a+b //By the way it is 11
```
---
## How to delete Variables or anything else in code
Golang is a good languange that does not allow variables or anything else
to be not used in code. You can not declare a variable and never use them 
you just can not. But if you wanna delete them there is the Garbage collection
it is your garbage man. Golang knows when a variable is not used anymore and 
deletes them.
---
 ## Pointers 
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
## Array
Arrays are the best example for a variable that stores a definit amount of
variables of the same type
```go
//you declare a array with var <name> [n]<type>
var arr [6]int
//you can initialize an array like this
var arr [5]int =  [5]int{1, 2, 3, 4, 5} // Yes you need to write [n]<type>{value} i don't know why
arr := [5]int{1, 2, 3, 4, 5} // Short form for declare an array with values
fmt.Println(arr[0]) // it is 1
// When you want to save more variables than n you need to use a slice
```
---
## Slice
Slices are a flexible array that can grow or shrink as needed.
```go
var numbers []int  // Declares an empty slice of integers
fruits := []string{"apple", "banana", "orange"}  // Slice with initial values short form
fmt.Println(fruits[0]) // it is apple

//Do you wanna know why slices are called slices because you can slice them
citrusFruits := fruits[1:3] 
fmt.Println(citrusFruits[0:2]) // it is banana orange
```
## Struct
Structs are your own data types it consist of variables or other structs
If you write the first letter of a struct in Uppercase it is visible in every file
If you write the first letter of a struct in Lowercase it is only visible in the file where the 
struct in declared
```go
type person struct {
  Name string
  Age int
  City string
}
alice := person{}
var alice person  // Declare a variable of type Person
var alice person = {Name : "Alice",Age : 16,City : "a"} //Declare with Values
alice.Name = "Alice" //add values after declaring
alice.Age = 30
alice.City = "New York"
fmt.Println(alice.City)

// There is also embedded struct that just means that a struct is in a struct
type Animal struct {
    Name string
}
// Dog struct embedded in Animal
type Dog struct {
    Animal // Embedded struct
    Breed  string
}
dog := Dog{
    Animal: Animal{Name: "Buddy"},
    Breed:  "Labrador",
}
```
---
## Function
Function are code blocks for specific task
Same as structs first letter decides if it is visible or not
```go
func functionName(parameters) (returnValues) {
  // Function body containing code to be executed
  return returnValue1, returnValue2, ... // Optional return values
}
///////////////////////////////////////////////////////////////////
type Vec3d struct(Datatyp){
	(variablen Namen) + Datentyp
}
func add(Variables) Vec3d{
	sum := Vec3d
	return sum
}
func add()(int32,int32)// Two returns{
	return 22,22
}
///Named Return in einer func:
func (v *Vec3d) add(rhs Vec3d) Vec3d{// add is a Methode for a struct
	sum := Vec3d{}
}
/// There are also variadic funtion. They are used when you want to give many variables of a
///type to a function
func sum(numbers ...int) int {
    total := 0
    for _, num := range numbers {
        total += num
    }
    return total
}
func main() {
    // Calling sum function with different number of arguments
    fmt.Println(sum(1, 2, 3))        // Output: 6
    fmt.Println(sum(1, 2, 3, 4, 5))  // Output: 15
    fmt.Println(sum(10))             // Output: 10
    fmt.Println(sum())               // Output: 0 (no arguments provided)
}
```
## Controle structures
there are many controle structures in golang
- if
- switch

### if 
These are used if you want to compare some variables
```go
///Normal if
if x > 10 {
    fmt.Println("x is bigger 10")
}else if x == 10 {
    fmt.Println("x is equals 10")
}else {
    fmt.Println("x is 10 or smaller")
}

///If wih a statment:
if y := x * 2; y > 10 {
    fmt.Println("y is bigger than 10")
}
```
---
### Switch
These are used for many if in one structure
```go
///Switch without statment:
switch day:= 3 {
case 1:
    fmt.Println("Monday")
 fallthrough // it also goes in the next case i don`t know why you use this it is not needed
case 2:
    fmt.Println("Thursday")
case 3:
    fmt.Println("Wensday")
default:
    fmt.Println("error")
}

//Switch with statment:
x := 3
switch{
case x > 10:
    fmt.Println("x is bigger than 10")
case x == 10:
    fmt.Println("x equals 10")
default:
    fmt.Println("x is lower than 10")
}
```
------
## Loops
There are only one type of loop, it is 'For' but it can be convertet in many other types
-for
-while
-infinite
-foreach
```go
/// Basic for loop
// It goes from 0 to 10 
for i := 0; i < 10; i++ {
    fmt.Println(i)
}

/// for as a while loop
i := 0
for i < 10 {
    fmt.Println(i)
    i++
}

/// infinite for
for {
    fmt.Println("infinite-loop")
}

/// for as foreach loop
numbers := []int{1, 2, 3, 4, 5}
for index, value := range numbers {
    fmt.Printf("Index: %d, Wert: %d\n", index,value)
}
```
These are the thinks to terminate the loop early

Break:
The break statement ends the current loop immediately and continues with the code after the loop.

Continue:
The continue statement skips the remaining statements in the current iteration and continues with the next iteration.

Return:
If the loop is in a function, a return statement can end the function (and therefore the loop) completely.

Labels:
The you can declare labels, labels are used for when you want to end many for in one statment
```go
func main() {
OuterLoop: //label
    for i := 0; i < 3; i++ {
        for j := 0; j < 3; j++ {
            if i == 1 && j == 1 {
                break OuterLoop // end all for loops
            }
            fmt.Printf("i = %d, j = %d\n", i, j)
        }
    }
}
```
