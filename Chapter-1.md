# Introduction to C++ Programming

C++ is an extraordinary means for the human-to-machine interface. The method of coding for C++ was developed in 1979 by a man named Bjarne Stroustrup and is an extension of the C language developed at Bell Laboratories. This versatile language can be found not only in just computers but drones as well as robots. Understanding the C++ language is paramount today for those who will be working with the most modern technologies. A good foundational understanding of the manipulation and construction of this code can push future technicians a long way and help to increase the language’s boundaries into the future of all cutting-edge technology. In general, the basics of C++ can go a long way and will be used from the beginning to the end of a programmer's career. This section delineates those basics and gives simple explanations of how they work. 


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
 cout << “7 + 8 = “ << 7 + 8 << endl;
putting in comments:
cout << “7 + 8 = “ << 7 + 8 << endl; // prints: 7 + 8 = 15
-M.L. are structured as / * and * /.
   - Anything in between these symbols are ignored by the compiler

/*
	You can include comments that can
	occupy several lines. 
 */

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
1. As a reader, what comments are structured /* */ ?
2. What are whitespaces used for?
3. How can you tell if an identifier is illegal?

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
(6728, -67, 0, 78, 36782)
  - Positive integers do not need a + sign in front
  - No commas within integers (i.e 36, 765 is seen as 36 and 765)
‘bool’ Data Type
-Has only two values: true and false
  -called the logical (Boolean) values 
‘char’ Data Type
-Used to represent single characters (letters, number, and special symbols) on your keyboard
  - enclose each character within single quotation marks (i.e ‘A’, ‘b’, ‘+’)
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
1. What are the three categories for simple data types?
2. How many values does the ASCII and EBCDIC have each?
3. What is the definition of precision?

## Variables
We use variables to inform the compiler of the data that will be used in terms of our data types. When we declare a variable we give a statement specifying the data type and the name of the variable. 


-After you declare a variable it is important that you initialize it.


For example- 

int = y
y = 10


### Review Questions
1.) What are variables used for?


2.) What do you do after you declare a variable?

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
Expressions are fundamental in C++. Expressions allow you to manipulate data and perform different operations. Expressions are usually comprised of variables, operators, and constants which are to be evaluated.

- Example (a+b)-4

### Mixed Expressions
An expression that contains both floating-point numbers and integers is known as a mixed expression. It's important to note that there are rules when evaluating mixed expressions.

1.) The rule of precedence always applies when evaluating mixed expressions. Multiplication, division, and modulus operators must be evaluated before addition and subtraction.


2.) If an operator has both integer and floating-point, the result must be in floating-point form.

-An example of a mixed expression: 4 * 3 + 7 / 5 - 25.5 = -12.5
### Review Questions
1.) What is the first rule when evaluating a mixed expression?


2.) What is the order of precedence?
## Type Conversion (Casting)
Implicit Type Coercion: A value of one data type is automatically changed to another data type
To avoid implicit type coercion, C++ provides explicit type conversion through a ‘cast operator’- is called ‘type conversion’ or ‘type casting’
static_cast<dataTypeName> (expression)
- First, the expression is evaluated and then converted to value of the type specified by ‘dataTypeName’
- When converting a floating-point (decimal) number to an integer using the cast operator, you simply drop the decimal part of the floating-point number.
- You can also use cast operators to explicitly convert char data values into int data values and int data values into char data values.

### Review Questions
1. To avoid implict type coercion, what does C++ provide to an explicit type conversion?
2. What are some other ways you can use a cast operator?
3. What is another title for 'cast operator'?

## ```string``` Type
A string is simply a sequence of zero or more characters. The string type in C++ is robust and exhibits greater complexity than simple data types. Beyond offering the necessary storage space for strings, it encompasses a range of operations for string manipulation. 

-In C++, you will find strings inside quotation marks. 

-For example, “Example” is how you would see a string in C++. If you find a string with no characters, that is an “empty’ or “null” string. 
### Review Questions
1.) What do you put inside quotations in a string?

2.) What is the difference between a string and an equation?



## Assignment Statements, Input Statements
The principal objective of a C++ program is to execute calculations and manipulate data. Remember that data must be loaded into the main memory before manipulation. In this segment you will learn how to put data into the computer's memory. The process for storing data includes these two steps:
1. Instruct the computer to allocate memory.
2. Include statements in the program to put data into the allocated memory.

### Allocating Memory with Constants and Variables
In C++:
* When instructing a computer to allocate memory, you request storage space to hold your data.
* It's crucial to keep track of where you store the data and the name under which it is stored.
* Knowing the data type is valuable information as different data types are handled differently.
* Determining whether specific data needs to be "fixed" or can change throughout the program is essential.

Constants:
* Some data must remain constant throughout the program, such as conversion formulas that never change.
* Storing a fixed data type involves using the syntax ```const dataType identifier = value;```.
* This assigns a unique name to the statement, making it unchangeable.
* The data is stored in the computer's memory, ensuring it remains constant when needed again during the program's execution.

Variables
* In some programs, data needs to be changed during execution.
* As an example, an employee's salary changes over time and if you wanted to store them you would not store them as a constant but instead as a variable because it can be changed.
* The syntax for a variable would look like this, dataType identifier, identifier, ...;
* There are no written rules for naming variables or constants but for variables programmers normally use lower case letters, and uppercase letters for constants.

### Putting Data into Variables
In C++ there are two ways:
1. Use C++'s assignment statement.
2. Use input (read) statements.

### Assignment Statement
Syntax for assignment statement: variable = expression;
* The value of the expression and the data type of the variable should match.
* The expression is computed on the right side.
* The value is designated to the variable on the left side.

###  Saving and Using the Value of an Expression
Saving the value of an expression gives you the ability to use the value alone without having to use the entire expression.
There are three steps to saving the value of an expression.
1. Choose the correct data type and declare a variable.
2. Assign the value of the expression of the variable that was assigned.
3. Wherever the value is needed use the variable that was declared.

### Declaring and Initializing Variables
In C++ when declaring a variable it does not always automatically initialize it.
* Therefore you must initialize it manually because the computer does not warn us that the proper value is not assigned.
* This is an example of a statement that is declared and initialized seperately:
```cpp
int num1, num2;
char character;
double decimalNumber;

num1 = 25
num2 = 8
character = '@';
decimalNumber = 7.9;
```
* This is an example of a statement that is declared and initialized together:
```cpp
int num1 = 25, num2 = 8;
char character = '@';
double decimalNumber = 7.9;
```
* It is based on the programmer's preference or the classification of the program that determines whether or not the variables are initialized during their declaration.

### Input (Read) Statement
In C++ when putting data into variables you use ```cin``` and the operator ">>".
* The syntax for this is:
```cin >> variable >> variable ...;```

### Review Questions
Question 1.
When allocating memory in C++, what is a crucial aspect to keep in mind?

A. The value assigned to the memory allocation.

B. The size of the allocated memory.

C. Keeping track of where the data is stored and the name under which it is stored.

D. Using uppercase letters for variable names.

Question 2.
Which statement correctly describes storing a fixed data type in C++?

A. The syntax involves using const dataType identifier = value; and assigns a unique name to the statement.

B. The syntax involves using dataType identifier, identifier, ...; and allows the value to change during execution.

C. Constants must always be declared and initialized separately in C++.

D. Allocating memory for variables involves using the operator ">>".

Question 3.
What is the purpose of the assignment statement in C++?

A. To declare a variable.

B. To initialize a variable.

C. To allocate memory for constants.

D. To assign a value to a variable based on an expression.

Answers: 1. C 2. A 3. D.

## Increment and Decrement Operators
The increment and decrement are valuable tools in C++. By using ++, we can quickly increase the value of a variable by one and can use - - to decrease the value of a variable by one.

-Both increment and decrement operators come in two forms: pre and post-.

-The syntax for the increment operator is: Pre-increment: ++variable, Post-increment: variable++.

-The syntax of the decrement operator is Pre-decrement: --variable, Post-decrement: variable–.

The difference between having the increment or decrement come before or after comes into play when used in an expression. For example,  
z is an int variable. If ++z is used in our expression, z will first be incremented by one, and then its new value will be used. However, if z++ is used in our expression, first the value of z will be used, followed by an increment of 1.

### Review Questions

## Output
In C++ to display output onto the standard output device use ```cout``` and the operator "<<"
* The syntax is:
``` cout << expression or manipulator << expression or mainpulator...;```
To use cin and cout in a program you have to include a specific header file. 

### Review Questions
Question 1.
How do you display output onto the standard output device in C++ using cout?

A. cout >> expression or manipulator >> expression or manipulator...;

B. cout << expression or manipulator << expression or manipulator...;

C. cin << expression or manipulator << expression or manipulator...;

D. cin >> expression or manipulator >> expression or manipulator...;

Question 2.
What is the correct syntax for using cout to display multiple expressions or manipulators in C++?

A. cout = expression or manipulator = expression or manipulator...;

B. cout -> expression or manipulator -> expression or manipulator...;

C. cout << expression or manipulator << expression or manipulator...;

D. cout :: expression or manipulator :: expression or manipulator...;

Question 3.
Which header file needs to be included to use cin and cout in a C++ program?

A. <iostream>

B. <stdio.h>

C. <math.h>

D. <cstdlib>

Answers: 1. B 2. C 3. A.

## Preprocessor Directives
C++ programming involves a particular and concise set of operations, and the crucial functions and symbols required for running a C++ program are encapsulated within different libraries. Each library is identified by a name and associated with a header file. Preprocessor directives play a critical role and are executed by the preprocessor program.

-Preprocessor directives, which are initiated with a # symbol, guide the preprocessor without needing a semicolon at the end of the commands. You would use the syntax #include <HeaderFileName> if you wanted to have a header file included.

-Preprocessor commands will always be processed before the program is sent through the compiler.

-An example would be #include <iostream>.

### ```namespace``` and Using ```cin``` and ```cout``` in a Program
In C++, we can use namespaces to organize our codes into separate, smarter units. We can view namespaces as containers that hold identities (functions, variables, etc.) which makes sure they don't clash with other namespaces.


For example,
std::cout << "This is the example namespace print function." << std::endl;


In C++, Cin and Cout are used for respective input and output operations.


Cin is short for "Console Input". This allows the user to input data into the computer.


In this example, we can get an integer input.


std::cin >> number;


Cout is short for "Console Output". We use Cout to display output onto the console. 


In this example, we use cout to display "Hello, World".


std::cout << "Hello, World!" << std::endl;


### Using the ```string``` Data Type in a Program

### Review Questions

## Creating a C++ Program
Creating a C++ program for beginners:

A good compiler is required for creating and running a C++ program. The use of such a program will help you to create, edit, and run the code you wish to use. What is a compiler? A compiler interfaces the C++ coding with the computer by translating your code into machine language, allowing the computer to understand and interpret your instructions. 

A well-known example of a simple code for beginners is the “Hello World” C++ program. This program is simple to run and use.

Once you have your compiler and saved a new file as a C++ type with a .cpp file extension, begin the code on line 1 with the #include(space)<iostream>. Skip a line and begin with int(space)main() skip another space and place a right-facing bracket {. Skip two more spaces and begin with cout(space)<< “hello, world” <<(space)std::endl; after the endl; tag line skip to another line and type return(space)0;. For the last piece skip one more line and type a left-facing bracket }. This will conclude the code building part of the page, all that is left is to run the program through the compiler and the result should output “hello world”. Your code should look something like this: 




```
#include <iostream>
Int main()
{

cout<< “hello world” << std::endl;
	


return 0;
}
```

After running this program you should see “hello world”.




### Review Questions

## Debugging: Understanding and Fixing Syntax Errors

### Review Questions

## Program Style and Form
An agreed-upon form of style helps other programmers to understand and decipher code that is written by other programmers. The styles of C++ include the LLVM Coding Standards, ISO C++ Core Guidelines, Microsoft C++ Coding Standards, Airbnb C++ Style Guide, Qt Coding Style, Mozilla C++ Portability Guide, BOOST C++ Coding Standards, Embedded C++ Coding Standards, and the Your Team/Project's Custom Style. The style and forms of standards are dependent on the project and scope of the work being produced. 
### Syntax

### Use of Blanks
Blanks allow for the separation of numbers and words from symbols for a clearer understanding. Blanks should not be put into identifiers or reserved words like nullptr, operator, or, or_eq, private, protected, public, register, reinterpret_cast, requires, etc.



### Use of Semicolons, Brackets, and Commas
Semicolons terminate statements and or lines an example of this is the std::endl; or the return 0;. Curly brackets enclose the main body of a C++ program. Regular brackets “()” separate certain functions from the rest of the code and help determine the accuracy of mathematical statements. An example of this is the statement 3 + 8 * 9 this statement reads entirely different when it's written as (3 + 8) * 9. Commas can separate items in an initializer of a constructor, declarations in a struct or class, different statements in a single line as well as a myriad of other uses. 



### Semantics
Semantics in C++ and language are used to determine the meanings of statements coded in C++, semantics can change the meaning of certain C++ statements depending on what is being phrased in the code. An example can be made with the commands “double” and “float” being used in a program that requires an accurate numerical value. Float numbers will always be less precise than numbers using the double command and could change the output accuracy of a program using these commands.

### Naming Identifiers
Naming identifiers can be very important to the readability and clarity of C++ statements. If my named identifier is coded as studentsperteacher it may be less understandable than an identifier named students_per_teacher. This can give more clarity to the author of the code as well as those reading such an identifier in the future.

### Prompt Lines
Prompt lines help the user of the program understand what actions are to be taken. An example of a prompt line could be “Please enter today's temperature, integers only then press enter”. This prompt line tells the user to enter an integer and press the enter key, thereby giving the user an inkling of what the program needs to do to interact with the program legally. Without a command prompt, the user wouldn’t understand how to interact with the program.

### Documentation
Documentation in C++ refers to the notes a good coder will leave behind within the code. Leaving instructions or reasonings behind withing the code will help to clarify what the code is doing or being used for. “//This phrase most often will appear green in the program.” Anything written after the // will not be used for program instructions and its only purpose will be to inform and label parts of the code visible to the author and those viewing the code directly and serve no other purpose.

### Form and Style
This follows how a C++ code is spaced and formatted. Like a run-on sentence in English, the spelling may be correct but following what the coder is writing may be more difficult. Indentations can identify which parts of the code do what as well as blank spaces and skipping lines. An IDE can help with structuring code and making it easier to follow.





### Review Questions

-How can the use of blanks improve the readability of code in C++?

-What is a prompt line and what does it do?

-What is one way to improve the naming identifier "milesperhour"?

## Chapter Summary

## Key Terms
1. Computer Program- a sequence of statements whose objective is to accomplish a task.
2. Programming- the process of planning and creating a program.
3. Function- a collection of statements; when activated, or executed, it accomplishes something.
4. Predefined- a function that is already written and provided as part of the system.
5. Programming Language- a set of rules, symbols, and special words.
6. Syntax Rules- tell you which statements (instructions) are legal or valid.
7. Semantic Rules- determine the meaning of the instructions.
8. Token- The smallest individual unit of a program written in any language.
9. Keywords- a reserved word.
10. Identifiers- a C++ identifier consists of letters, digits, and the underscore character (_); it must begin with a letter or underscore.
11. Data Types- a set of values together with a set of operations.
12. Integral- a data type that deals with integers, or numbers, without a decimal part.
13. Floating Point- a data type that deals with decimal numbers.
14. Enumeration- a user-defined data type.
15. Collating Sequence- a predefined ordering for the characters in a set.
16. Floating Point Notation- a form of scientific notation used to represent real numbers.
17. Float- The data type float is used in C++ to represent any decimal number between -3.4 * 10^38 and 3.4 * 10^38 . The memory allocated for a value of the float data type is four bytes.
18. Double- The data type double is used in C++ to represent any decimal number between -1.7 * 10^308 and 1.7 * 10^308. The memory allocated for a value of the double data type is eight bytes.
19. Precision- the maximum number of significant digits.
20. Double Precision- values of type double.
21. Arithemtic Expressions- an expression constructed using arithmetic operators and numbers.
22. Operands- numbers appearing in an arithmetic expression.
23. Unary Operators- An operator that has only one operand.
24. Binary Operators- an operator that has two operands.
25. Associativity- the associativity of arithmetic operators is said to be from left to right.
26. Character Arithmetic- arithmetic operation on char data.
27. Integral expressions- an expression in which all operands are integers.
28. Floating-point (decimal) expressions- an expression in which all operands in the expression are floating-point numbers.
29. Mixed expressions- an expression that has operands of different data types.
30. Implicit type coercion- when a value of one data type is automatically changed to another data type.
31. Cast operator- also known as type conversion or type casting - used to explicitly convert one data type to another data type.
32. String- a sequence of zero or more characters.
33. Null- a string containing no characters.
34. Named Constant- a memory location whose content is not allowed to change during program execution.
35. Variable- A memory location whose content may change during program execution.
36. Simple- a data type where the variable or named constant of that type can store only one value at a time.
37. Initialized- the first time a value is placed in the variable.
38. Assignment operator- =; assigns whatever is on the right side to the variable on the left side.
39. Walk-through- Tracing values through a sequence.
40. Input (read)- a statement that places data into variables using cin and >>.
41. Increment Operators- ++; increases the value of a variable by 1.
42. Decrement Operators- --; decreases the value of a variable by 1.
43. Pre-increment- has the syntax ++variable.
44. Post-increment- has the syntax variable++.
45. Pre-decrement- has the syntax --variable.
46. Post-decrement- has the syntax variable--.
47. Output Statement- an output on the standard output device via cout and <<.
48. Preprocessor- a program that carries out preprocessor directives.
49. Source code- the preprocessor directives and the program statements constitute the C++ source code.
50. Source code file- The file containing the source code.
51. Heading- The first line of the function main.
52. Declaration statements- statements that are used to declare things, such as variables.
53. Executable statements- statements that perform calculations, manipulate data, create output, accept input, and so on.
54. Statement Terminator- The semicolon.
55. Semantics- The set of rules that gives meaning to a language.
56. Self documenting- The identifiers in the second set of statements.
57. Prompt lines- executable statements that inform the user what to do.
58. Compound assignment statements- statements that are used to write simple assignment statements in a more concise notation.

## Programming Exercises

## References
  MindTap - Cengage Learning, ng.cengage.com/static/nb/ui/evo/index.html?snapshotId=3814784. Accessed 23 Jan. 2024. 

Priya, U. (2023, December 27). Use of Semicolon in Programming languages. Coding ninjas studio. https://www.codingninjas.com/studio/library/use-of-semicolon-in-programming-languages 

Nath, S. (2020, February 26). How to write the first C++ program?. Tutorialspoint. https://www.tutorialspoint.com/How-to-write-the-first-cplusplus-program 

Goyal, S. (2023, April 17). The history of C++ (with timeline infographic) // unstop. The History Of C++ (With Timeline Infographic) // Unstop. https://unstop.com/blog/history-of-cpp 

Hock-Chuan, C. (2013, June). C++ programming language. C++ Basics - C++ Programming Tutorial. https://www3.ntu.edu.sg/home/ehchua/programming/cpp/cp1_basics.html

Chatgpt - openai聊天. (2024, January 18). https://chat.openai.com/auth/login

Mark K. Jowett, Ph. D. (n.d.). Introduction. Basic C++ Elements. https://www.cs.fsu.edu/~cop3014p/lectures/ch2/index.html 
