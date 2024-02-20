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

### Review Questions

## ```switch```Structures

### Avoiding Bugs by Avoiding Partially Understood Concepts and Techniques (Revisited)

### Review Questions

## Terminating a Program with the ```assert``` Function

### Review Questions

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

## References
