# Chapter 2 Input/Output

## Objectives
Upon completion of this chapter, students will be able to:

1. Identify input and output streams
2. Read data from the standard input device
3. Define the use predefined functions in a program
4. Describe input stream functions get, ignore, putback, and peek
5. Write data to the standard output device
6. Use manipulators in a program to format output
7. Perform input and output operations using the string data type
8. Distinguish how to use debug logic errors

## Introduction

## I/O Streams and Standard I/O Devices
Stream: a sequence of characters from the source to the destination
- input (istream / cin): sequence of characters to an input device
- output (ostream / cout): sequence of characters to an output device

### cin and the Extraction Operator >>
The extraction operator >> is binary and thus takes two operands
- The left-side must be an input stream, like cin, and the right side is a variable
General syntax: cin >> variable >> variable
ex. cin >> payRate >> hoursWorked, there is no difference between the inputs
cin >> payRate
cin >> hoursWorked

….

### Review Questions
1. True or False. The operator >> skips all whitespace.
2. What is one input stream variable that is used with the operator >>?
3. True or False. The operator >> does not read digits of numbers, including the decimal point for floating-point variables.

## Using Predefined Functions in a program
In Chapter 1 we learned that a function is a block of code that only runs when called.
  * an example of a function is ```main``` this function is used to execute autimatically when you run a program.
  * another example of a function is ```pow``` which is the power function it is used to calculate $`x^y`$ in a program.
      * you would use ```pow``` like this pow(2.0, 3.0) = $`2.0^3.^0`$ = 8.0.
      * The numbers x and y that are used in this function are called arguments or parameters of a function.
      * The parameters are 2.0 and 3.0
  * an expression such as pow (2.0, 3.0) is called a function call.
    * a function call in C++ is an expression containing the function name followed by the function call operator, ().

### cin and get Function
The variable ```cin``` is used to get user input.
 * cin is predefined to read data from the program with the extraction operator (>>)
The get function is used to read a string or text line it includes the whitespaces.
 *

### cin and ignore Function

### The putback and peek Functions

### The Dot Notation between I/O Stream Variables and I/O Functions: A Precaution

### Review Questions

## Input Failure

### The clear Function

### Review Questions

## Output and Formatting Output

### setprecision Manipulator
setprecision: controls the output of floating-point numbers
General syntax: setprecision(n)
- ’n’ is the number decimal places
- to use the manipulator, you must put #include <iomanip>

### fixed Manipulator
sets the output of floating-point numbers in a fixed decimal format on the standard output device: ‘cout << fixed;’
- to disable the manipulator, you put ‘cout.unsetf(ios::fixed);
    - this turns the number to default
scientific: output floating-point numbers in scientific format

### showpoint Manipulator
used to show the decimal point and trailing zeros
format: ‘cout << showpoint’
The output of a floating-point number in a fixed decimal format with the decimal point and trailing zeros: ‘cout << fixed << showpoint;’

### C++ 14 Digit Seperator
Use single-quote character ‘
Example: the number 87523872918 will be represented as 87’523’872’918

### set w
output of the next value of an expression in a specific number of columns
format: setw(n)
- either a string or a number
ex. if the number of columns are 8, and the output requires only four columns, the first fout columns are left blank
- if the number of columns specified is less than the number of columns required by the output, the output automatically expands to the required number of columns; the output is not truncated 
ex. i fx is an ‘int; variable, this statement ‘cout << setw(5) << x << endl;’ outputs the value of x in five columns

  -have to include, #include <iomanip> to use the manipulator

### Review Questions
1 . What does the the output setw(n) do?
2. Which manipulator controls the output of floating-point numbers?
3. To disable the the fixed manipulator, what do you use?

## Additional Output Formatting Tools

### setfill Manipulator

### left and right Manipulators

### Review Questions

## Input/Output and the stringType

### Review Questions

## Debugging: Understanding Logic Errors and Debugging with cout Statements

### Review Questions

## File Input/Output

### Review Questions

## Chapter Summary

## Key Terms

## Programming Exercises

## References
