# Introduction to C++ Programming

## Objectives
Upon finishing this chapter, students will have the capability to:
1. Identify basic components of a C++ program, including functions, special symbols, and identifiers
2. Classify simple data types and use them in assignment statements
3. Use arithmetic operators, precedence, and expressions
4. Create assignment and input statements and the use of variables within statements.
5. Differentiate between type conversion and type casting
6. Develop output results using output statements
7. Identify syntax errors and debugging techniques
8. Write a basic C++ program

## Introduction

## Basic Elements
C++ program is a collection of one or more subprograms—called functions (collection of statements, and when activated, it accomplishes something)
- ‘Predefined’ or ‘standard’ functions are already written and provided in the system
Every C++ program has a function called ‘main’, even if the program has one function
The programming language consists of its own special symbols, words, and syntax rules (tell of statements are accepted or not in the program)
- Semantic rules: determines the meaning of the instructions

### Comments
Identifies the author, date it was written, an explanation of the program and meanings of key statements
- For the readers, not compiler
Two types of comments: single-line and multiple-line comments
-S.L. begin with / / and can be placed anywhere in the line
   - Anything after / / is ignored by the compiler
-M.L. are structured as / * and * /.
   - Anything in between these symbols are ignored by the compiler

### Special Symbols
Token: smallest individual unit of a program
 - Divided into special symbols, word symbols and identifiers
    - Mathematical symbols (+), (-), (*), (/)
    - English grammar (.), (;), (?), (,)
    - Tokens: nothing can go in between these characters (<=, !=, ==, >=)

### Recieved Words (Keywords)
Letters that make up a reserved word are always lowercase (i.e, int, float, double, char, etc.)
 - Each is considered to be a single symbol
     *Cannot be used for anything other than their intended use*

### Identifiers
Names of things that appear in programs, such as variables, constants, and functions
- Some are predefined (can be redefined), others are defined by the user
-  ex. ‘cout’ is a predefined identifier, ‘length’ is a user-defined identifier
Can only be made up of letters, digits, and the underscore character
C++ is case sensitive, number and NUMBER are considered different
To tell if an identifier is illegal, it cannot have any spaces, numbers, or special characters 

### Whitespaces
Whitespaces include blacks, tabs, and newline characters
- Used to separate special symbols, reserved words, and identifiers

### Review Questions

## Data Types
C++ has three data type categories: Simple data type, Structures data type, and Pointers

### Simple Data Types
Considered the building block of structured data type
Three categories of simple data: Intergral, Floating Point, and Enumeration
Integral: Deals with integers, or numbers without a decimal part
- Classifications: char, shirt, int, long, bool, unsigned charm unsigned short, unsigned int, unsigned long, long long, unsigned long
  - These data types represents the values associated with it
Floating point: Deals with decimal numbers
Enumeration: User-defined data type
‘int’ Data Type
-Integers in mathematics
  - Positive integers do not need a + sign in front
  - No commas within integers (i.e 36, 765 is seen as 36 and 765)
‘bool’ Data Type
-Has only two values: true and false
  -called the logical (Boolean) values 
‘char’ Data Type
-Used to represent single characters (letters, number, and special symbols) on your keyboard
  - enclose each character within single quotation marks (i.e ‘A’, ‘b’, ‘+’
The most common character data sets are the American Standard Code for Information Interchange (ASCII) and Extended Binary-Coded Decimal Interchange Code (EBCDIC)
- ASCII has 128 values, while the EBCDIC has 256 values and was created by IBM

### Floating-Point Data Types
A form of scientific notation
- The letter E stands for exponent (i.e: ‘0.0000453’ would be ‘4.530000E-5’ in C++ Floating-Point Notation)
Three data types: float, double, and long double
- On most new compilers, double and long double are considered the same thing
The maximum and minimum values of the data types ‘float’ and ‘double’ are system dependent
-Other than set values, the other different between these two data types are the maximum value of significant figures
  -In float values is six or seven
  -In double, values is 15
Precision: maximum number of significant digits
- Sometimes float values are called single precision, and values of type double are called double precision

### Review Questions

## Variables

### Review Questions

## Arithmetic Operators, Operator Precedence, and Expressions
Arithmetic operators in C++ include + (Addition), - (Subtration), *(Multiplication), / (Division) and % (modulus).

-Arithmetic operators are used for integral and floating-point data types.

Operands are the numbers within an expression are referred to as operands.

### Order Precedence
Arithmetic operators follow a specific order of precedence.

Precedence Hierarchy:

Multiplication (*), Division (/), and Modulus (%) have a higher precedence than Addition (+) and Subtraction (-).

-Execution Sequence:

Operations with the same precedence are performed from left to right.

### Expressions

### Mixed Expressions

### Review Questions

## Type Conversion (Casting)
Implicit Type Coercion: A value of one data type is automatically changed to another data type
To avoid implicit type coercion, C++ provides explicit type conversion through a ‘cast operator’- is called ‘type conversion’ or ‘type casting’
- First, the expression is evaluated and then converted to value of the type specified by ‘dataTypeName’
- When converting a floating-point (decimal) number to an integer using the cast operator, you simply drop the decimal part of the floating-point number.
- *****(few examples for 2.6)******
- You can also use cast operators to explicitly convert char data values into int data values and int data values into char data values.

### Review Questions

## string Type
A string is simply a sequence of zero or more characters. The string type in C++ is robust and exhibits greater complexity than simple data types. Beyond offering the necessary storage space for strings, it encompasses a range of operations for string manipulation. 

-In C++, you will find strings inside quotation marks. 

-For example, “Example” is how you would see a string in C++. If you find a string with no characters, that is an “empty’ or “null” string. 
### Review Questions

## Assignment Statements, Input Statements
The principal objective of a C++ program is to execute calculations and manipulate data. Remember that data must be loaded into the main memory before manipulation. In this segment you will learn how to put data into the computer's memory. The process for storing data includes these two steps:
1. Instruct the computer to allocate memory.
2. Include statements in the program to put data into the allocated memory.

### Allocating Memory with Constants and Variables
When you tell a computer to allocate memory, you ask for storage space to hold your data. It would be best if you kept up with where you store the data and which name it is under. Knowing the data type is also valuable information. Depending on the data type, you will handle them differently. You also need to determine whether or not you need to have specific data “fixed" or if it can change throughout the program.

In C++, some data must remain the same throughout the program. An example is a conversion formula that must stay the same because that is a fact that never changes, like how a foot is always 12 inches. When storing a fixed data type, you will use the syntax 'const dataType identifier = value;.’ This gives the statement a unique name, which renders it unchanging. Now, it is stored in the computer’s memory, so when needed again, the computer uses that same data, eliminating the risk of it changing while the program runs.

### Putting Data into Variables

### Assignment Statement

###  Saving and Using the Value of an Expression

### Declaring and Initializing Variables

### Input (Read) Statement

### Variable Initialization

### Review Questions

## Increment and Decrement Operators
The increment and decrement are valuable tools in C++. By using ++, we can quickly increase the value of a variable by one and can use - - to decrease the value of a variable by one.

-Both increment and decrement operators come in two forms: pre and post-.

-The syntax for the increment operator is: Pre-increment: ++variable, Post-increment: variable++.

-The syntax of the decrement operator is Pre-decrement: --variable, Post-decrement: variable–.

The difference between having the increment or decrement come before or after comes into play when used in an expression. For example,  
z is an int variable. If ++z is used in our expression, z will first be incremented by one, and then its new value will be used. However, if z++ is used in our expression, first the value of z will be used, followed by an increment of 1.

### Review Questions

## Output

### Review Questions

## Preprocessor Directives
C++ programming involves a particular and concise set of operations, and the crucial functions and symbols required for running a C++ program are encapsulated within different libraries. Each library is identified by a name and associated with a header file. Preprocessor directives play a critical role and are executed by the preprocessor program.

-Preprocessor directives, which are initiated with a # symbol, guide the preprocessor without needing a semicolon at the end of the commands. You would use the syntax #include <HeaderFileName> if you wanted to have a header file included.

-Preprocessor commands will always be processed before the program is sent through the compiler.

-An example would be #include <iostream>.

### namespace and Using cin and cout in a Program

### Using the string Data Type in a Program

### Review Questions

## Creating a C++ Program

### Review Questions

## Debugging: Understanding and Fixing Syntax Errors

### Review Questions

## Program Style and Form

### Syntax

### Use of Blanks

### Use of Semicolons, Brackets, and Commas

### Semantics

### Naming Identifiers

### Prompt Lines

### Documentation

### Form and Style

### Review Questions

## Chapter Summary

## Key Terms

## Programming Exercises

## References
  
