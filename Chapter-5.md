# Intoduction to Chapter 5

## Objectives
Upon completion of this unit, students will be able to:

1. Describe predefined and user-defined functions
2. Identify value-returning functions, including actual and formal parameters
3. Construct and use a value-returning, user-defined function in a program
4. Identify function prototypes
5. Use void functions in a program
6. Distinguish between value and reference parameters
7. Compare and contrast local and global identifiers
8. Use static variables
9. Debug programs using drivers and stubs
10. Research function overloading
11. Use functions with default parameters

## Introduction

Functions are like powerful tools that help you break down complex problems into smaller, more manageable steps. They can perform specific tasks, reuse code efficiently, and improve the program. In this section, you'll gain a foundation in working with functions in C++. Think of functions as building blocks. By breaking down your program into smaller, reusable functions, you're laying a strong foundation for well-structured, efficient, and maintainable C++ code.

## Predefined Functions
Using predefined functions in C++ is beneficial when you need to reuse certain values. This allows you to not have to build everything from scratch each time you need it.

Some examples of mathematical predefined functions are ```pow(x,y), sqrt(x), and floor(x).```

First off to use predefined functions in a program you must first include the header file that contains the functions' specification using the include statement.

As an example if you wanted to use the floor(x) function you would have to use the #include <cmath> header.

### Review Questions
1. Which of the following is a benefit of using predefined functions in C++?
   A) They allow you to reuse certain values without building everything from scratch.
   B) They require you to write all the code for tasks yourself.
   C) They slow down the execution of the program.
   D) They increase the complexity of the code.

2. Which of the following is NOT an example of a mathematical predefined function in C++?
   A) pow(x, y)
   B) sqrt(x)
   C) log(x)
   D) floor(x)

3. True or False: To use predefined functions in a C++ program, you must include the header file that contains the functions' specification using the include statement.
   A) True
   B) False

Answers- 1. A, 2. C, 3. A.

## User-Defined Functions
There are two types of User-Defined Functions:
    Value-returning functions: with these functions you give it a value and it gives you back something in return.
    Void functions: you tell it to do something and it does it but you do not get anything back.
    
### Review Questions
1. What is the main difference between value-returning functions and void functions?
   A) Value-returning functions return a value of a specific data type, while void functions do not return any value.
   B) Value-returning functions do not have a return type, while void functions return a specific data type.
   C) Value-returning functions do not use a return statement, while void functions use a return statement to return a value.

2. If a function returns the sum of two numbers, what type of function is it likely to be?
   A) Value-returning function
   B) Void function
   C) Conditional function

3. True or False: Void functions can't perform any calculations or operations, they can only print output to the screen.
   A) True
   B) False

Answers- 1. A, 2. A, 3. B.

## Value-Returning Functions
The proper syntax for value-returning functions includes:
    Formal parameters: a variable declared in the function heading.
    Actual parameters: a variable or expression listed in a call to a function.

### Syntax: Value-Returning Function
An example:
```
int add(int a, int b) {
        return a + b;
}
```

### Syntax: Formal Parameter List
An example:

```
int addNumbers(int num1, int num2);
```

### Function Call
Syntax example:
``` int sum = addNumbers(a,b);```

### Syntax: Actual Parameter List
An example:
```void greetUser(string name, int age)```

### Review Questions
1. What is the purpose of value-returning functions in C++?
   A) To perform calculations and return a result to the caller.
   B) To print messages to the console.
   C) To declare variables within a function.

2. What is the proper syntax for defining a value-returning function in C++?
   A) ```void functionName(int param1, int param2) { }```
   B) ```int functionName(int param1, int param2) { }```
   C) ```functionName(int param1, int param2) { }```

3. In the function call `int result = add(3, 5);`, what are the actual parameters?
   A) `result`
   B) `3` and `5`
   C) `add` and `(3, 5)`

Answers- 1. A, 2. B, 3. B.

## Void Functions
* A void function does not have a data type.
* In a void function you can use the return statement without any value.

### Review Questions
1. True or False: A void function does not have a return type.
   - A) True
   - B) False

2. What is the purpose of using the return statement in a void function?
   - A) To return a value to the caller.
   - B) To exit the function and return control to the caller without returning any value.
   - C) To print output to the console.

3. Which of the following best describes a void function?
   - A) A function that performs calculations and returns a result.
   - B) A function that does not return any value.
   - C) A function that has a void data type.

Answers- 1. A, 2. B, 3. B.

## Value Parameters

Pretend you've got a box. Whatever you put in this box, can change, but the original thing you put in stays the same. Now, imagine a toy car. You put this toy car into the box. Inside the box, you decide to change the color of the toy car to red. When you take the car out of the box, it's red, but the original toy car you put in remains the same color it was before. In C++, when we use something called value parameters, it's like using that magic box. When you pass information (like a number or a word) to a function, it's as if you're putting it in the magic box. The function can work with a copy of this information, just like changing the color of the toy car inside the box. So, let's say you have a function called " paintCar " in your C++ program. This function changes the color of a car. When you call this function with the color "blue", it's like putting "blue" in the magic box. Inside the function, it changes the color to "red". But when you take the car (or the value) out of the function, the original "blue" color remains unchanged. Value parameters in C++ let us work with data without messing up the original values. It's like using that box to make changes without affecting the original car. Value parameters in C++ allow you to work with data inside a function without modifying the original values passed as arguments. It's like using a temporary copy or model to make changes without affecting the original object. This is useful when you want to perform operations on the data within the function's scope while keeping the original data intact.
```
void paintCar(string carColor) {
    carColor = "Red"; // Changes the color inside the function
}

string color = "Blue";
paintCar(color);
```


### Review Questions

1) If you have a function called "paintCar" that changes the color of a car and you call it with the color "blue", what will be the color of the car outside the function?

2) Explain why, in C++, when you pass information to a function using value parameters, the original data remains unchanged.

3) True or False: Changes made to a value parameter inside a function affect the original argument variable in the calling code.

4) How does the use of value parameters contribute to code safety and prevent unintended side effects?

5) If you have a function called "paintCar" that changes the color of a car and you call it with the color "blue", what will be the color of the car outside the function?

## Reference Variables as Parameters

A reference parameter is a reference to the memory location of a variable. When parameters are passed by reference, a new storage location is not created for these parameters. Instead, the reference parameters directly represent the same memory location as the actual arguments (variables) supplied to the function. When you pass an argument by reference, you're not creating a copy of the variable's value. The reference parameter essentially becomes an alias or alternative name for the original variable, referring to the exact same memory address. Any modifications made to the reference parameter within the function will directly affect the original argument variable in the calling code, since they are both pointing to the same memory location. Unlike value parameters, where changes to the parameter inside the function have no effect on the original argument, reference parameters provide a way to modify the original variable's value through the function. This is because the reference parameter and the argument variable share the same underlying memory location, rather than having separate copies. By passing parameters by reference, you can avoid the overhead of creating a copy of the variable, which can be beneficial when working with large objects or data structures. It also allows functions to modify the original argument variables, which is useful when you need to return multiple values or update complex data structures. In C++, you can pass arguments to functions either by value or by reference. When you pass an argument by reference, you're passing the memory address of the variable rather than a copy of its value.

The syntax for declaring a reference parameter is to use the & symbol before the parameter's type:

```
void updateValue(int& x) {
    x = 10; // Modifies the original argument variable
}

int main() {
    int a = 5;
    updateValue(a); // Passing a by reference
    cout << "Value of a: " << a << endl; // Output: Value of a: 10
    return 0;
}
```
In this example, the function updateValue takes a reference parameter x. When we call updateValue(a), we're passing the memory address of a to the function. Inside updateValue, any changes made to x are actually modifying the original variable a in the calling code.

### Review Questions

1) True or False: When passing an argument by reference, a new memory location is created for the parameter.

2) True or False: Reference parameters can be used to return multiple values from a function.

3) In what situations would you prefer to use reference parameters over value parameters, or vice versa?

4) What is the advantage of using reference parameters when working with large objects or data structures?

5) When passing an argument by reference, is a new memory location created for the parameter or not? Explain.

## Value and Reference Parameters and Memory Allocation

In C++ there are two types of function parameters: value parameters and reference parameters.Value parameters are used to pass information into a function. When you pass an argument to a function by value, a copy of the argument's value is created and passed to the function's parameter variable. Any changes made to the parameter variable inside the function do not affect the original argument variable in the calling code.
Value Parameters (Pass by Value) in C++:

When you pass an argument to a function as a value parameter in C++, a new copy of the argument's value is created in memory. Any changes made to the parameter inside the function will not affect the original variable passed as an argument.

Example:
```
void incrementValue(int x) {
    x++; // x is a copy of the argument's value
    // Changes to x won't affect the original variable
}

int main() {
    int a = 5;
    incrementValue(a); // Passing a as a value parameter
    cout << a; // Output: 5 (a is not modified)
    return 0;
}
```
In this example, the incrementValue function creates a copy of the value of a (which is 5) and stores it in the parameter x. Incrementing x within the function does not affect the original variable a in the main function.

Reference Parameters (Pass by Reference) in C++:

When you pass an argument to a function as a reference parameter in C++, you're passing a reference (or an alias) to the original variable's memory location. Any changes made to the parameter inside the function will affect the original variable passed as an argument.

```
void incrementReference(int& x) {
    x++; // x is a reference to the original variable
    // Changes to x will affect the original variable
}

int main() {
    int a = 5;
    incrementReference(a); // Passing a as a reference parameter
    cout << a; // Output: 6 (a is modified)
    return 0;
}
```
The incrementReference function takes a reference to the original variable a using the int& syntax. When x is incremented within the function, it modifies the value stored at the memory location of a in the main function.

Memory Allocation in C++:

Value Parameters: A new memory location is allocated for the copy of the argument's value, separate from the original variable's memory location.
Reference Parameters: No new memory is allocated; the parameter refers to the same memory location as the original variable. The choice between value and reference parameters in C++ depends on the desired behavior of the function and whether you want to modify the original variable or work with a copy of its value. Value parameters are typically used when you don't want the function to modify the original variable, while reference parameters are used when you want the function to modify the original variable directly.
It's important to note that in C++, when you pass an object (such as a class instance) as a value parameter, a copy constructor is called to create a new copy of the object. Similarly, when you pass an object as a reference parameter, no new copy is created, and the function operates on the original object.


### Review Questions

1) What are the two types of function parameters in C++?

2) When would you choose to use value parameters over reference parameters in C++?

3) Explain the concept of pass by value and pass by reference in C++.

4) Compare and contrast the behavior of value parameters and reference parameters when passed to a function.

5) What happens to the original variable when it's passed as a value parameter to a function?

## Reference and Parameters and Value-Returning Functions

In C++ functions are tools that let you break down complex tasks into manageable steps. These functions often need information to work with, which is provided through parameters. There are two main ways to pass this information:
Value Parameters: By default, functions receive arguments as value parameters. This means a copy of the argument's value is created and passed to the function. Any changes the function makes to this copy do not affect the original variable. Think of it like giving the function a photocopy of your document - it can work with the copy, but the original remains untouched.
Reference Parameters: When you need a function to directly modify the original variable, you can use reference parameters. These parameters are declared with an ampersand (&) before their type. When you pass a variable by reference, the function essentially gets a special nickname (the reference) that points directly to the original variable. Any changes made through this reference will affect the original variable. Imagine handing the function the actual document itself, not just a copy.


### Review Questions

1) What are the two main ways to pass information (arguments) to functions in C++?

2) When might you want to use a value parameter instead of a reference parameter?

3) Efficiency: How does passing large objects by value vs. reference affect program efficiency?

4) Write a short code snippet demonstrating how to pass a variable by reference to a function.

5) Analogy: How is passing a value parameter similar to making a photocopy?

## Scope of an Identifier

In C++, the place where an identifier can be used is called its scope. There are 3 kinds of scopes:

Global Scope: If an identifier is declared outside of any functions or classes, it has a global scope and can be used anywhere in the program.

Local Scope: If an identifier is declared inside a function or a group of code, it has local scope. It can only be used inside that function or group of code. As soon as that function or group of code finishes, the identifier is eliminated and cannot be used anymore.

Class Scope: If an identifier is declared inside a class (but not in one of its methods), it has class scope. It can be used by all methods inside that class.

Example:
```
#include <iostream> // global scope
using namespace std;
int globalVar = 10; // global scope
class MyClass {
    int classVar; // class scope
 void myMethod() {
        int localVar = 5; // local scope
        cout << localVar << endl; // can access localVar
        cout << classVar << endl; // can access classVar
        cout << globalVar << endl; // can access globalVar
    }
};
int main() {
    int localVar = 20; // local scope
    cout << localVar << endl; // can access localVar
    cout << globalVar << endl; // can access globalVar
    }
```
### Review Questions

## Global Variables, Named Constants, and Side Effects
In C++, a var that's declared outside of all functions and classes is called a global var. This kind of var can be used everywhere in your code. Even though it may seem convenient, having global vars can cause issues because any part of your code can modify them. This can make it tricky to pinpoint where the value of a global var is being changed if you're trying to troubleshoot your code.

Named constants are special kinds of variables that can't be changed once they're set. This helps you keep a specific value in your code that you don't want to alter accidentally. To create a named constant, you can use the keyword const.

In C++, a side effect is when a function or process alters some part of the program's status beyond its own boundaries. It might be tweaking a global value, modifying a document, or even showing information to the consumer. Even though side effects oftentimes prove beneficial, particularly when addressing a database or presenting data to a client, they may complicate the code's comprehensibility and fixing, particularly when the ramifications aren't promptly documented or are unanticipated.

### Review Questions

1.) Describe named constants.

2.) What is the process of a side effect?

## Static and Automatic Variables

In C++, a var that keeps its worth between function calls is called static. It's initialized only once and its memory is secured when the program begins, then released once the program ends. Static vars can be created inside a function (only accessible within that func), or outside a function (accessible within the whole file).


In C++ automatic variables are the type of variable. They are generated upon entering a block, such, as a function. Are removed when exiting that block. Their values do not carry over between function invocations. If you forget to set a variable it contains data (whatever was stored in that memory spot previously).

Example:

void someFunction() {
    static int staticVar = 0; // This is a static variable
    staticVar++;
    cout << staticVar << endl;
}

int main() {
    someFunction(); // This will print 1
    someFunction(); // This will print 2
    return 0;
}


### Review Questions

1. What is the difference between static and automatic variables?

2. What happens when you don't initialize an automatic variable?

## Debugging: Using Drivers and Stubs

When dealing with systems pinpointing and addressing issues can sometimes be challenging. This is where the roles of drivers and stubs prove to be useful.

Drivers; Acting as a mediator a driver consists of code that invokes a module or function undergoing testing. It supplies test data to the module or function. Showcases the resulting output. Drivers are utilized in situations where testing a module at a level's necessary but the higher level module that calls it has not yet been developed. In scenarios the driver emulates the behavior of the higher level module.

Stubs; On the other hand, a stub serves as a placeholder—a pseudo module or function that is invoked by the module under examination. Stubs are employed when testing involves modules that call upon lower-level modules or functions that're still, in development. Here the stub imitates the functionality of these lower-level modules by furnishing outputs.

### Review Questions

## Function Overloading: An Introduction

In C++ function overloading allows you to create functions, with names but varying parameters. These parameters may vary in terms of quantity, type or sequence. When you invoke the function the compiler decides which one to use based on the arguments you pass. This concept is a form of polymorphism, which's fundamental, in object oriented programming.

### Review Questions

## Functions with Default Parameters

In C++ you have the option to set default values, for parameters within a function. This indicates that if you invoke the function without giving a value for that parameter the default value will be utilized. This feature proves handy when you aim to establish a default action, for a function while granting the caller the ability to alter that action if desired.

### Review Questions

## Summary

Have you ever attempted to put together a giant puzzle? Functions in C++ are like dividing that puzzle into smaller pieces. Each piece completes a tiny part of the bigger picture, making the entire puzzle less daunting. Similarly, functions break down complex programming problems into manageable steps. Each function focuses on a specific task, like calculating an area or displaying a menu. By putting these "function pieces" together, you build well-structured C++ programs

## Key Terms
1. modules- another name for a function.
2. parameters- an identifier in a function header, which acts within the function as a regular local variable; a parameter may be formal or actual.
3. function header- includes the name of the function, the number of parameters if any, the data type of each parameter, and the data type of the value returned by the function.
4. body- the code within the function required to accomplish the task.
5. definition- includes the name of the function, a listing of the parameters if any, the data type of each parameter, the data type of the value returned by the function, and the code required to accomplish the task.
6. formal parameter- a variable declared in the function heading.
7. actual parameters- a variable or expression listed in a call to a function.
8. data type- the return type of a value-returning function.
9. return type- the data type of the value that the function returns; also called the data type of a function.
10. local declaration- a declaration of a variable within a block of code for use only within that block.
11. function prototypes- a function heading without the body of the function.
12. value parameters- A formal parameter that receives a copy of the content of the corresponding actual parameter.
13. reference parameters- a formal parameter that receives the location (memory address) of the corresponding actual parameter.
14. local variables- variables declared in the body of a function (or block) for use only within that function (or block).
15. scope- refers to where an identifier is accessible (visible) in a program.
16. Local identifier- an identifier declared within a function (or block).
17. Global identifier- an identifier declared outside of every function definition.
18. nested block- a block declared within another block.
19. external variable- a global variable declared within a function using the extern reserved word; the keyword extern indicates that the variable is declared elsewhere.
20. automatic variable- a variable for which memory is allocated at block entry and deallocated at block exit.
21. driver- a program that tests a function.
22. function overloading- creating several functions with the same name but different formal parameter lists.
23. different formal parameter lists- when two or more functions with the same name have a different number of formal parameters, or if they have the same number of parameters, the data type of the parameters differs in at least one position.

## Programming Exercise

## References

OpenAI. (2024, April 30). https://openai.com/  

C++ programming language. C++ Basics - C++ Programming Tutorial. (n.d.). https://www3.ntu.edu.sg/home/ehchua/programming/cpp/cp1_basics.html 

Malik, D. S. (2018). C++ Programming: From problem analysis to program design (8th ed.). Cengage Learning.


This chapter's editor was ...
