# Introduction to Chapter 3

## Objectives
Upon completion of this unit, students will be able to:

Identify and use control structures
Identify logical and relational operators, how they work, and order of precedence
Distinguish the relationship of relational operators and simple data types
Identify how to form and evaluate logical (Boolean) expressions
Use one-way and/or two-way selection syntax
Utilize pseudocode to develop, test, and debug a program
Demonstrate a switch statement in a program
Identify how to avoid bugs
Use the assert function to terminate a program

## Chapter Introduction

## Control Structures

Control structures allow for C++ code to perform conditional tasks. These conditional tasks are contained in what are called “control structures”. There are three types of Control Structures in C++, they are the sequence structure, the selection structure, and the loop structure. 

*Sequence Structure: Execute instructions step by step.
The sequence structure presents a serial list (one after another) of tasks for the code to perform to completion. The sequence structure exists as the most fundamental form of control structure, this type of structure is present in its most basic form as the “hello world” program example.
#include <iostream>
using namespace std;
int main(){
#include <iostream>

    cout << "Hello World!";
    return 0;
}

This control structure is how normal code is read as it's compiled.

*Selection Structure: Make decisions based on conditions.
In selection control structures, conditional statements are the parts of the code that do tasks based on whether a specific condition provided by the code equates to true or false. 



#include <iostream>
using namespace std; 
int main() {
    int x = 10;

   
    if (x > 5) {
    cout << "x is greater than 5" << endl;
    }

    return 0;
}

Output: x is greater than 5

*Loop Structure: Repeat tasks until a condition is met.
Like in the previous example with the switch statements, loop statements can be written a single time, allowing a programmer to perform many tasks using less direct input. This code is written in a way that it replays forever “in a loop”, or terminates when a set condition is seen as true or false.

#include <iostream>
using namespace std; 
int main() {
    
    for (int i = 1; i <= 5; i++) {
    cout << i << endl;
    }

    return 0;
}

The output: 
1
2
3
4
5






### SELECTION: ```if``` AND ```if...else```
Logical expression: an expression that evaluates to ‘true’ or ‘false’
- i. e. 8 is greater than 3, is true: 8 > 3.
- Relational Operators: == equal to, != not equal to, < less than, <= less than or equal to, > greater than, >= greater than or equal to

### Relational Operators and Simple Data Types
You can use realtional operators with all three simple data types

- 8 < 15, (8 is less than 15), true
- 6 != 6 (6 is not equal to 6), false
- 2.5 > 5.8 (2.5 is greater than 5.8), false
- 5.9 <= 7.5 (5.9 is less than or equal to 7.5), true
- 7 <= 10.4, 7 is less than or equal to 10.4), true

### Comparing Characters
For ‘char’ values, the realtional operators ‘true’ or ‘false’ depends on the collating sequence
- 32 < 97, and the ASCII value ‘ ‘ is 32 and the ASCII value of ‘a’ is 97, ‘ ‘ < ‘a’ is true
- Other values: ‘R’ > ’T’ is false. ‘+’ < ‘*’ is false, ‘A’ <= ‘a’ is true
However, different data types may produce unpredictable results
- 8 < ‘5’, 8 is compared with the collating sequence of ‘5’, which is 53, which makes this evaluation ‘true’
When C++ evaluates a logical expression, it returns an integer value of 1 if ture; it returns an integer value of 0. Any nonzero value is treated as true
In C++, there are two selections, or branch control structures: if statements and the switch structure

### One-Way Selection
One-way selections are incorporated using the ‘if’ statement
- Syntax:
- if (expression)
-    (statement)
Expression (decision maker). Statement (action statement).
- The ‘expression’ is usually a logical expression. If the value of the ‘expression’ is true, the ‘statement’ executes. If the ‘expression’ is false, vice versa.
Ex. 
- if (score >= 60)
-    (grade = ‘P’;)
- Forgetting parentheses around the logical expression, and putting a semicolon after the ‘expression’ will create a semantic error.

### Two-Way Selection
- Two-way selection involves the ‘if-else’ statement
Syntax:
- if (expression)
-    (statement1)
- else
-    (statement2)
- In a two-way selection, if the value of the expression is true, statement1 executes. If the value of the expression is false, statement2 executes
Ex.
- if (hours (hours > 40.0)
-    (wages = 40.0 * rate + 1.5 * rate * (hours - 40.0);
- else
-    (wages = hours * rate;)
- If a semicolon is placed after the ‘expression’ and before ‘statement1’, it creates a syntax error

### ```int``` Data Type and Logical (Boolean) Expressions
- Nonzero values are treated as true
ex.
- int legalAge;
- (int age;)
- AND THE ASSIGNMENT STATEMENT
- (legalAge = 21;)
- If regarding legalAge as a logical variable, the value of legalAge is true.

- ex2.
- (legalAge = (age >= 21);)
- The value 1 to legalAge if the value of age is greater than or equal to 21. The statememt assigns the value of age is less than 21.

### ```bool``` Data Type and Logical (Boolean) Expressions
- 'bool', 'true', and 'false' are reserved words
- The identifier ‘true’ has the value 1, and ‘false’ has the value 0
ex.
- bool legalAge;
- int age;
- THE STATEMENT
- legalAge = true; (sets the value of legalAge to true)
- legal = (age >= 21);
- This assigns the value true to legalAge if the value of age is greater than or equal to 21. This statement assigns the value false to legalAge if the value of age is less than 21

### Logical (Boolean) Operators and Logical Expressions
The evaluation of a single relational operator
- ex. weight and height are double variables
(weight > 180 and height < 6.0)
- ! not (unary)
- && and (binary)
- | | or (binary)

The ! operator (not)
- When ! true, this means false 
- When ! false, this means true
- ex. ! (‘A’ > ‘B’), true, becuase ‘A’ > ‘B’ is false

The && operator (and)
- ex1 && ex2 is true if both expressions are true, otherwise it is false
- ex. (24 >= 35) && (‘A’ < ‘B’), false, because (24 >= 35) is false, (‘A’ < ‘B’) is true, and false && true is false.

The | | operator (or)
- ex1 | | ex2 is true if and only if at least one is true, otherwise it is false
- ex. (‘A’ <= ‘a’) | | (7 != 7), true, because (‘A’ <= ‘a’) is true, and (7 != 7) is false. true | | false is true.

### Order of Precedence
(11 > 5 | | 6 < 15 && 7 >= 8)
- This logical expression yields different results, depending on whether || or && is evaluated first. If || is evaluated first, the expression evaluates to false. If && is evaluated first, the expression evaluates to true.
- !, +,- (unary operators),      first
- *, /, % ,                      second
- +, - ,                          third
- <, <=, =>, > ,                  fourth
- ==, != ,                       fifth
- && ,                           sixth
- | | ,                          seventh
- = (assignment operator) ,      last

- Using the precedence rules in an expression, relational and logical operators are evaluated from left to right
- You can use parentheses into an expression to clarify its meaning and also to override the precedence of operators

### Review Questions
1. What are the six relational operators?
2. What is wrong with this syntax?
if (expression);
    statement1;
else
     statement2;
3. What is the Order of Precedence of the operators?

## Relational Operators and the ```string``` Type
Relational Operatores include
    * Equal to (==)
    * Not equal to (!=)
    * Greater than (>)
    * Less than (<)
    * Greater than or equal to (>=)
    * Less than or equal to (<=)
These are used to return a boolean value like (```true``` or ```false```)
When comparing strings in C++ you are going letter by letter until you find a deviation.

### Compund (Block of) Statements
The ```if...else``` structure only allows you control over one statement at a time.
For more complex statements you can use a compound statement.
The syntax is 
``` {
        statement_1
        statement_2
        .
        .
        .
        statement_n
    }
```

### Review Questions
1. Relational operators in C++ include "Not equal to" (!=).

A) True
B) False

2. Relational operators in C++ return:

A) Strings
B) Integers
C) Booleans
D) Floats

3. Compound statements in C++ are used to execute multiple statements together within a single block.

A) True
B) False

Answers- 1. True, 2. C, 3. True

## Using Pseudocode to Develop, Test, and Debug a Program
Pseudocode is the method of using C++ and informal C++ language to help develop a program. Pseudocode allows you to create an outline for your code, which can help you see the applicable structure.


Example:


If... Y>X then Y is Larger. Else... X is larger. In C++ this would look like....


#include <iostream>
using namespace std;
int main()
{
if Y>X}


### Review Questions
Why do we utililize psuedo code?

## ```switch```Structures
In C++, we can use selection structures to make decisions in our programs.** **1. The "if" and "if...else" statements:** * These statements allow us to evaluate a logical expression to determine which block of code to execute. * We can use the "if" statement when we only have one block of code to execute based on a condition. * We use the "if...else" statement when we have two blocks of code to execute based on a condition. **2. The switch structure:** * This structure doesn't require evaluating a logical expression. * It allows the computer to choose from multiple options based on a given variable. * The "switch" statement checks the value of a variable and executes the code associated with that value.


### Avoiding Bugs by Avoiding Partially Understood Concepts and Techniques (Revisited)

### Review Questions
1.) What is the purpose of switch structures?

2.) How can we use switch structures?
## Terminating a Program with the ```assert``` Function
The assert function is built in C++ to help address what we may face in the process of programming development. The assertion function will allow us to execute our programs with grace and give the user an error message indicating the type of error and the location within the program it occurred.


Example,


int main() {
    int divisor = 0;
    
    // Using assert to check if divisor is not zero
    assert(divisor != 0);
    
    int dividend = 10;
    int result = dividend / divisor; // This line will cause a division by zero error if divisor is 0

    std::cout << "Result: " << result << std::endl;

    return 0;
}

### Review Questions
1.)What is the purpose of the Assert function?


2.) How can one use the assert function to prevent you from having errors?
## Chapter Summary

## Key Terms
1. logical (Boolean) expressions- an expression that has a value of either true or false.
2. Decision maker- the expression in an if statement which determines whether to execute the statement that follows it.
3. Action statement- the statement following the expression in an if statement.
4. logical (Boolean) values- ```true``` and ```false```.
5. Logical (Boolean) operators- operators that enable you to combine logical expressions.
6. Associativity- the order in which operators are grouped and evaluated.
7. Compound statement- consists of a sequence of statements enclosed in curly braces, { and }.
8. Nested- when one control statement is located within another.
9. Pairing an ```else``` with an ```if```- the rule stating that an else statement is associated with the most recent incomplete if statement.
10. Short-circuit evaluation- A process in which the computer evaluates a logical expression from left to right and stops as soon as the final value of the expression is known.
11. Conditional operator- a ternary operator written as “?:”; the three arguments explain what the condition is, what the result will be if the condition is true, and what the result will be if the condition is false.
12. Conditional expression- an expression that uses a conditional operator.
13. Pseudocode- an informal mixture of C++ and ordinary language used to design an outline of a logical solution to a problem.
14. Switch structure- gives the computer the power to choose from among many alternatives.

## Programming Exercises
1.) Create a Psuedocode for a program that gets a number from the user ranging from 1-10, adds the number by 1, and displays the new number to the user.
2.) Compare and contrast the = and == in C++.

3.) Write a C++ program that takes input from the user for their math score on a test and calculates the inputted grade based on the following grading scale:

A: Score >= 90
B: 80 <= Score < 90
C: 70 <= Score < 80
D: 60 <= Score < 70
F: Score < 60

## References
Malik, D. S. (2018). C++ Programming: From problem analysis to program design (8th ed.). Cengage Learning.

Chatgpt. ChatGPT. (2024). https://chat.openai.com/


This Chapter's editor was...(Put Name Here)
