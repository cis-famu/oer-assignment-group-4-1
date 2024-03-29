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

In this chapter, importance is placed on the manipulation of input/output data. Understanding how to debug a program, reading and writing to and from other programs or data, clearing input/output error codes the definition of a function, as well as a multitude of other functions.

## I/O Streams and Standard I/O Devices
Stream: a sequence of characters from the source to the destination
- input (istream / cin): sequence of characters to an input device
- output (ostream / cout): sequence of characters to an output device

### cin and the Extraction Operator >>
The extraction operator >> is binary and thus takes two operands
- Skips all whitespace characters
- The left-side must be an input stream, like cin, and the right side is a variable
General syntax: cin >> variable >> variable
- ex. cin >> payRate >> hoursWorked, there is no difference between the inputs
 - cin >> payRate
 -  cin >> hoursWorked
- The >> operator when reading the ‘char’ variable, it only finds and stores the next character
- To read into an ‘int’ or ‘double’ variable, it only stops when a whitespace or a character other than a digit is found

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
 * when you use the variable cin and the function get together the syntax is ```cin.get(..);```

### cin and ignore Function
When wanting to process only a portion of data use the stream function ```ignore```.
 * the syntax for using the function ignore is ```cin.ignore(...);```.
   You can set how many character you want to be ignore in a line using this function.

### The putback and peek Functions
The stream function ```putback``` lets you put the last character taken from the inout stream by the get function back into the input stream.
 * the syntax for the putback function is ```istreamVar.putback(..);```.
The stream function peek looks into the input stream and lets you know what the next character is without getting rid of it from the input stream.
 * the syntax for the peek function is ```ch = istreamVar.peek();```.

### The Dot Notation between I/O Stream Variables and I/O Functions: A Precaution
It is important to keep the dot in between identifiers to prevent error codes.

### Review Questions
1. What is a function in programming, and how is it utilized?

     A) A variable that stores user input.
     B) A block of code that runs automatically when a program starts.
     C) A function is not used in programming.
     D) A loop that iterates through code.

2. Explain the role of cin and the get function in C++ for user input.

     A) cin is used for string manipulation, and get is for numerical input.
     B) cin is for output, and get is for input.
     C) cin is a variable for user input, and get reads a string or text line with whitespaces.
     D) cin and get cannot be used together.

3. Describe the functionalities of the putback and peek functions in I/O streams. 

     A) putback stores the last character, and peek removes the next character.
     B) putback puts the last character back into the stream, and peek checks the next character without removing it.
     C) Both putback and peek remove characters from the stream.
     D) putback is used for user input, and peek is for output.
Answers- 1. B, 2. C, 3. B.

## Input Failure

### The clear Function

The clear function – A .clear() function removes all previously assigned values from a set or a string. This will destroy every value and the set container will carry no values or 0, this can allow for the creation of a new set with entirely new variables. The .clear() function can also clear the error state when std::cin fails to interpret the input, and allow the program to bypass the error state. 

std::cin.clear();
std::cin.ignore(std::Macguffin<std::streamsize>::max(), '\n');

 


### Review Questions

What function can be used to clear std::cin errors in a stream?

What does the .clear() function do to the characters of a set?

What type of errors does the the .clearfunction bypass?

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
In terms of the setw manipulator, the requested number of columns is greater than the actual amount needed for the expression. Since the output
is right justified, the unused columns on the left are left as blank spaces. Output stream variables can use the setfilll manipulator to fill the unused spaces.

Ex.

cout << setfill ('x') << setw (10);

### left and right Manipulators
The left and right manipulators are used for the justification in C++, allowing for respective left and right formatting.


-You can use the the unsetf function to disable these manipulators.

Ex. 


cout.width(6);   
  cout << left << n << '\n'; 
### Review Questions
1.) Why do we use the setfill manipulator?

2.) What are left and right manipulators?

## Input/Output and the stringType

Input/output string and the string type-
First things first, to use any string command remember to #include <string> so you can use the commands from the string library. A string is a group of characters, which could be letters numbers, or text. The input variable “cin” and the extraction operator “>>” can read a word with no spaces into a string variable the extraction operator can’t for example read both a first and last name in this scenario. If for example the name being entered is John Smith, only “John” will be extracted from the statement since there is a space between John and Smith.

Example:

#include <iostream>
#include <string>

using namespace std;

int main(){

string name;

cout << "type your name: ";

cin >> name;

cout << name << endl;



return 0;
}

This code allows the variable “name” to be assigned to what is typed into the prompt. This assignment of the typed characters into the name prompt will only accept the first unbroken line of characters typed and output the first string of characters. If there's a space for say, a last name entered, it will not be recognized. This is okay for simple data entry but for a total name containing spaces the code will need the getline function. In this new example, the getline function is used to recognize and output the full name with spaces.
#include <iostream>
#include <string>

int main() {



    std::string fullName;

    std::cout << "Type your first and last name: ";
    
    std::getline(std::cin, fullName);

    std::cout << fullName << std::endl;

   
   
   
    return 0;
}

 
Both the string and getline commands can be used to store any character information but have different capabilities, it is important to choose the most appropriate type for each individual situation.




### Review Questions

What library is necessary for the use of the string or getline functions? 

What type of information can be manipulated with the string and getline functions?

True/false – String can store information with spaces included?


## Debugging: Understanding Logic Errors and Debugging with cout Statements
There is a difference between syntax errors which are found by the compiler, and logical errors which are not usually detected by the compiler.


-You can use cout statements to help you debug by printing key values and expressions.


Ex. 


#include <iostream>

int main() {
    int num1, num2;
    
    // Input
    std::cout << "Enter the first number: ";
    std::cin >> num1;
    
    std::cout << "Enter the second number: ";
    std::cin >> num2;

    // Calculation of average (with a logic error)
    int average = num1 + num2 / 2;

    // Output
    std::cout << "The average is: " << average << std::endl;

    return 0;
}


#include <iostream>

int main() {
    int num1, num2;
    
    // Input
    std::cout << "Enter the first number: ";
    std::cin >> num1;
    
    std::cout << "Enter the second number: ";
    std::cin >> num2;

    // Debugging cout statements
    std::cout << "Debugging: num1 = " << num1 << ", num2 = " << num2 << std::endl;

    // Calculation of average (with a logic error)
    int average = num1 + num2 / 2;

    // Debugging cout statement
    std::cout << "Debugging: Incorrect average calculation = " << average << std::endl;

    // Output
    std::cout << "The average is: " << average << std::endl;

    return 0;
}
### Review Questions
1.) What is the difference between a logical error and a syntax error?


2.) How does the statement help us with debugging logical errors?

## File Input/Output
To obtain data from other input devices you can use the file I/O to read data or write data to a file.
 * to use this you have to include the header ```#include <fstream>```
 * under this header are two data types called ```ifstream``` and ```ofstream```.
 * ```ifstream``` means input file stream.
 * ```ofstream``` means output file stream.
 * You have to declare variables called file stream variables.
 * Then you must associate these file variables with the proper I/O sources.
 * Finally close the files.
 * The proper syntax to declare the I/O sources is ```ifstream inData; ofstream outData;```
 * The proper syntax to open the files is ```inData.open(".."); outData.open("..");```
 * The proper syntax to close the files is ```inData.close(); outData.close();```

### Review Questions
1. What is the purpose of the #include <fstream> statement in C++?

      A) It includes a fundamental file management library.
      B) It is used for numerical calculations.
      C) It is only necessary for graphical interfaces.
      D) It is not relevant to file I/O operations.
  
2. Which data types are associated with input and output file streams in C++ file I/O operations?

      A) ```ifstream``` and ```ofstream```
      B) ```int``` and ```float```
      C) ```string``` and ```char```
      D) ```cin``` and ```cout```

3. What is the correct sequence of steps for performing file I/O in C++, from declaring file stream variables to closing the files?

      A) Declare, open, associate, close
      B) Open, declare, associate, close
      C) Close, declare, open, associate
      D) Declare, associate, open, close
   
Answers. 1. A, 2. A, 3. A.

## Chapter Summary 

The operations of input and output or i/o is the most basic part of coding. Understanding these basic principles will accelerate your understanding of C++ and give you the capability to efficiently handle data. Output can be displayed, imparting ability to user interface, the hanling and manipulation of data from external and internal files through the string or the getline function and a wide array of functions and capabilities.  

## Key Terms
1. Stream- a sequence of characters from the source to the destination.
2. Input stream- a sequence of characters from an input device to the computer.
3. Output stream- a sequence of characters from the computer to an output device.
4. Common input- the variable cin is named after this.
5. Common output- the variable cout is named after this.
6. Input stream variables- variables of the type istream.
7. Output stream variables- variables of the type ostream.
8. Stream variables- either an input stream variable or an output stream variable.
9. Input failure- a situation in which a program either fails to compile, or yields incorrect results, because the input data does not match the corresponding variables in the program.
10. istream member functions- functions that are associated with the data type istream.
11. Stream member functions- I/O functions such as get.
12. Predefined functions- functions that are already defined in C++.
13. Arguments- values that are passed in a function call in the parentheses after the name of the function.
14. Function call- an expression that transfers control from the main function to the first statement in the body of the function, such as pow(2,3).
15. Dot notation- notation in which a dot separates the input stream variable name from the member, or function name.
16. Member access operator- the dot operator in C++.
17. Fail state- the state an input stream enters after input failure in which all further I/O statements using that stream are ignored.
18. Parameterized stream manipulators- manipulators with parameters.
19. File- an area in secondary storage used to hold information.
20. File stream variables- user-declared variables including ifstream and ofstream used for input and output.
21. Opening the files- associating a file stream variable with an input/output source.

## Programming Exercises
1.)Create a C++ program that gets the user's name as input using cin and then outputs a welcoming greeting. Please use the cout statement to display the greeting you create.


2.)Write a C++ program that defines a function called multiply, which would take two integer parameters, multiply them, and returns the result. In the main function, take two integers as input from the user, then call the multiply function, and print the result.


3.) Explain what a stream is and provide examples of input and output streams.

## References

Malik, D. S. (2018). C++ programming: From problem analysis to program design (8th ed.). Cengage Learning. 

Chatgpt. ChatGPT. (2024). https://chat.openai.com/ 

Academy, V. (2020, September 13). User input string in C++ | C++ tutorial for Beginners. YouTube. https://www.youtube.com/watch?v=i4BeY77jWWg 

Academy, V. (2020, September 13). User input string in C++ | C++ tutorial for Beginners. YouTube. https://www.youtube.com/watch?v=i4BeY77jWWg 

Yaossg, U. (2017, December 16). C++ reference. cppreference.com. https://en.cppreference.com/w/cpp 

Learn to code. W3Schools Online Web Tutorials. (n.d.). https://www.w3schools.com/ 

This Chapter's editor is Christopher Thaxton.
