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
C++ program is a collection of one or more subprograms—called functions (collection of statements, and when activated, it accomplishes something
- ‘Predefined’ or ‘standard’ functions are already written and provided in the system
Every C++ program has a function called ‘main’, even if the program has one function
The programming language consists of its own special symbols, words, and syntax rules (tell of statements are accepted or not in the program)
- Semantic rules: determines the meaning of the instructions

### Comments
Comments can be used to identify the author, date it was written, an explanation of the program and meanings of key statements
- For the readers, not compiler
Two types of comments: single-line and multiple-line comments
-S.L. begin with / / and can be placed anywhere in the line
   - Anything after / / is ignored by the compiler
-M.L. are structured as / * and * /.
   - Anything in between these symbols are ignored by the compiler

### Special Symbols
Token: smallest individual unit of a program
 - Divided into special symbols, word symbols and identifiers
    - Mathematical symbols (+, -, *, /)
    - English grammar (. , ; , ?, ,)
    - Tokens: nothing can go in between these characters (<=, !=, ==, >=)

### Recieved Words (Keywords)
Letters that make up a reserved word are always lowercase (i.e, int, float, double, char, etc.)
 - Each is considered to be a single symbol
     *Cannot be used for anything other than their intended use*

### Identifiers
Identifiers: names of things that appear in programs, such as variables, constants, and functions
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

### Floating-Point Data Types

### Review Questions

## Variables
Implicit Type Coercion: A value of one data type is automatically changed to another data type
To avoid implicit type coercion, C++ provides explicit type conversion through a ‘cast operator’- is called ‘type conversion’ or ‘type casting’
- First, the expression is evaluated and then converted to value of the type specified by ‘dataTypeName’
- When converting a floating-point (decimal) number to an integer using the cast operator, you simply drop the decimal part of the floating-point number.
- (few examples for 2.6)
- You can also use cast operators to explicitly convert char data values into int data values and int data values into char data values.

### Review Questions

## Arithmetic Operators, Operator Precedence, and Expressions

### Order Precedence

### Expressions

### Mixed Expressions

### Review Questions

## Type Conversion (Casting)

### Review Questions

## string Type

### Review Questions

## Assignment Statements, Input Statements
The principal objective of a C++ program is to execute calculations and manipulate data. Remember that data must be loaded into the main memory before manipulation. In this segment you will learn how to put data into the computer's memory. The process for storing data includes these two steps:
1. Instruct the computer to allocate memory.
2. Include statements in the program to put data into the allocated memory.

### Allocating Memory with Constants and Variables
In C++:
-When instructing a computer to allocate memory, you request storage space to hold your data.
-It's crucial to keep track of where you store the data and the name under which it is stored.
-Knowing the data type is valuable information as different data types are handled differently.
-Determining whether specific data needs to be "fixed" or can change throughout the program is essential.
Constants:
-Some data must remain constant throughout the program, such as conversion formulas that never change.
-Storing a fixed data type involves using the syntax 'const dataType identifier = value;.'
-This assigns a unique name to the statement, making it unchangeable.
-The data is stored in the computer's memory, ensuring it remains constant when needed again during the program's execution.
Variables
-In some programs, data needs to be changed during execution.
-As an example, an employee's salary changes over time and if you wanted to store them you would not store them as a constant but instead as a variable because it can be changed.
-The syntax for a variable would look like this, dataType identifier, identifier, ...;
-There are no written rules for naming variables or constants but for variables programmers normally use lower case letters, and uppercase letters for constants.

### Putting Data into Variables
In C++ there are two ways:
1. Use C++'s assignment statement.
2. Use input (read) statements.

### Assignment Statement
Syntax for assignment statement: variable = expression;


###  Saving and Using the Value of an Expression

### Declaring and Initializing Variables

### Input (Read) Statement

### Variable Initialization

### Review Questions

## Increment and Decrement Operators

### Review Questions

## Output

### Review Questions

## Preprocessor Directives
Not all 
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
  
