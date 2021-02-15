# AQA---CS-A-Level
AQA Computer Science A-Level Revision Notes

# Advanced Fundamentals of Computer Science using the AQA syllabus. Adapted from physicsandmathtutor.com

# Programming

## Data Types

### Data Type = is defined by the values it can take or the operations which can be performed on it.

It is possible to store one piece of data using various data types - must decide which is best suited. i.e. Age can be str or int.

      - Integer = 6, -1, 0
      - Float = 34.53453 , -3242.234234
      - Boolean = True / False
      - Character = 'm'
      - String = 'hello world'
      - Date / Time = Available in all most all languages to assist with the storing of dates and times.
      - Pointer / Reference = Declare a variable that can be used to 'point' to a physical address in memory.
      - Records = Composed of related data of various other data types. It is divied into names fields. Think of a record as a row from a table.
      - Arrays = (Same as lists for Python) ['Dave', 'John', 'William']

### User-defined Data Types

Built-in data types are useful, but often limiting. Languages allow you to construct your own complex user-defined data types.

## Programming Concepts

      - Variable declaration = Creating a variable for the first time, giving it a name (and sometimes a data type).
                               This alllocates a portion of computer memory to the variable.
      - Constant declaration = Same as variable declaration, but this value is constant i.e. won't change when program is running.
      
      - Assignment           = Giving a constant a variable or a value.
      - Iteration            = Repeating an instruction (can be definite or indefinite).
      - Selection            = Comparing values and then choosing an action based on those values.
      - Subroutine           = A named block of code containing a set of instructions designed to perform a frequently used operation.
      
### Definite and indefinite iteration

Process of repeating a block of code. Examples of this are for and while loops.

      - Definite             =  Type of iteration in which the number of repetitions required is known before the loop starts.
      - Indefinite           =  Type of iteration in which the number of repetitions required is not known before the loop starts.

```
for i in range(60):
  print(i)
```

```
a = 1

while a == 1:
    b = input("Enter your name\n")
    print('Hi, ', b, 'This is an infinite loop!!')
```
### Nested Structures

Selection strucutures and iteration structures can be nested. i.e. one strucutre is placed within another structure - easily identified by indentation (easier for humans to read)

```
for i in range(10):
    if i < 5:
        print('Hello numbers <5')
    else:
        if i == 6:
            print('6 is boring :(')
        else:
            print('bigger numbers are cool')
```

## Arithmetic Operations

       - Addition = 2 + 2 
       - Subtraction = 4 - 2
       - Multiplication = 4 * 2
       - Float Division = 8 / 4
       - Integer Division = 12 \ 8 or 12 DIV 8
       - Modulo (remainder) = 12 % 8
       - Exponentiation = 2**6
       - Rounding = "{0:.2sf}".format(float_number)
       - Truncation = removing all numbers after the decimal point (do not round)
      
 ## Relational Operations
 
       - Equal to: 12 = 12
       - Not equal to: 16 != 23
       - Less than: 3 < 5
       - Greater than: 5 > 3
       - Less than or equal to: x <= 5
       - Greater than or equal to: x >= 5

## Boolean Operations

### A Boolean data type is one whose value can only ever be true or false (1 or 0)

      NOT - Opposite of a Boolean value i.e. NOT 1 = 0
      AND - The product of 2 Boolean values i.e. 1 AND 1 = 1 ... 0 AND 1 = 0
      OR  - The sum of 2 Boolean values i.e. 1 OR 0 = 1 ... 1 OR 1 = 1 (= 2 but cant have 'more' true with this logic)
      XOR - True if strictly one of two values is true i.e. 1 XOR 1 = 0 ... 1 XOR 0 = 1
    
## Constants and Variables

Constants are useful if a value is required multiple times through code - it only has to be updated once.
They also make code easier to understand as we assign a name to a particular constant rather than just doing random stuff with an unnamed number throughout code.

## String-handling Operations

A string is a collecetion of characters - they have various functions applied to them

      - Length = Returns the number of characters within a specified string.
      - Position = Returns the position of a specified character within a string. 
      - Substring = Given a starting position and a length, returns a portion of a string.
            IAM is a substring of WILLIAM starting with position 4 and of length 3!
      - Concatenation = Joining two or more strings together, forming a new, longer string. 
      - Character to character code = Returning the character code which corresponds to a specified character.
      - Character code to character = Returning the character represented by a given character code.
      - String to integer and vice versa.
      - String to float and vice versa.
      - Date / time to string and vice versa.
 
 ## Random Numbers
 
 High-level programming languages have the ability to generate random numbers - in python you can import random then do random.random()
 
```
import random

for i in range(10):
    if i < 10:
        print(random.random())
print()
```

## Exception Handling

When error occurs in program an 'exception' is thrown - caused by i.e. wrong data type, divide by zero, non-existent variable etc.

If exception has been thrown, the computer has to handle the exception to avoid crashing -- the following occurs:
      - Pausing execution
      - Saving the current volatile state of the program on the system stack
      - Running a section of code called a catch block
            This code will prevent the program from crashing and may inform the user of the error.
            
Once error has been handled, the program uses the system stack to restore its pervious state before resuming execution.

## Subroutines

A named block of code containing a set of instructions used to perform a frequently used operation.
      - Reduces repitition, therefore, more compact and easier to read.
Both functions and prodcedures are types of subrouting - can be called writing their name in program statement.
      Both can return a value, functions are required to, procedures may not!

### Parameters of Subroutines

Parameters are used to pass data between subroutines within programs - specified within brackers at subrouting call, they hold pieces of information that the subroutine
requires to run.

      Pseudocode example:
      
      Length <-- USERINPUT
      Width  <-- USERINPUT
      OUTPUT CalculateArea(Length, Width)
      
      SUBROUTINE CalculateArea(x, y)
            RETURN x * y
      ENDSUBROUTINE
The subroutine takes 2 parameters, Length and Width
      The actual value passed by a parameter is called an argument. If a rectangle with sides of height 4 and width 6 was input into CalculateArea, 
      the parameters Length and Width would have arguments 4 and 6 respectively.
      
## Local vs Global Variables

Local variables can only be accessed from the subroutine within which it is declared. 
      Only exist in computer memory when their parent subroutine is executing. - more memory efficient way of storing data compled to globals

Global variables can be accessed from any part of a program - exist in memory for the entire duration of program execution. 

They can both be given the same identifier but this is bad practise - if local varialbe is changed, the global will remain the same.

## Stack frames in subroutine calls

Used to store:

      - return addresses
      - parameters
      - local variables

for each subroutine call that occurs during program execution.

Nesting = A subroutine calls another.

When this nesting occurs, each subroutine call will be 'pushed' onto the computer's call stack in the form of a stack frame (before code is executed).
When the nested subroutine finishes executing, the stack frame is 'popped' from the call stack - the computer uses the information to return to execution 
of the previous subroutine.

PLEASE SEE EXAMPLE VIDEO FOR FULL EXPLANATION OF CALL STACK AND POPPING.

## Recursive Techniques

A recursive subroutine is one which is defined in terms of iteself. 
i.e. somewhere in the recursive subroutine, there is a call to the subroutine itself.

Recursive subroutines must have a stopping condition (aka base case) - this must be met at some point in the execution of the program.
      - If an algorithm calls itself but doesn't have a base case, it will never terminate, causing a stack overflow as more and more stack frames are 
        pushed onto the call stack. 
      
See pseudocode example:
```
      SUBROUTINE Factorial(value)
            IF value = 0 THEN
                  RETURN 1
            ELSE
                  RETURN value * Factorial(value - 1)
            ENDIF
      ENDSUBROUTINE
```
BASE CASE IS WHEN value = 0 ; In this case algorithm doesn't use recursion to return result.  

When a problem can be solved using recursion, it can also be solved using iteration.
      Iterative solutions are easier to program while recursive solutions can be more compact in code.
