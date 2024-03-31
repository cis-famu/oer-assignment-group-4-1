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

## Predefined Functions

### Review Questions

## User-Defined Functions

### Review Questions

## Value-Returning Functions

### Syntax: Value-Returning Function

### Syntax: Formal Parameter List

### Function Call

### Syntax: Actual Parameter List

### return Statement

### Syntax: return Statement

### Function Prototype

### Syntax: Function Prototype

### Value-Returning Functions: Some Peculiarities

### More Examples of Value-Returning Functions

### Flow of Compilation and Execution

### Review Questions

## Void Functions

### Review Questions

## Value Parameters

Pretend you've got a box. Whatever you put in this box, can change, but the original thing you put in stays the same. Now, imagine a toy car. You put this toy car into the magic box. Inside the box, you decide to change the color of the toy car to red. When you take the car out of the box, it's red, but the original toy car you put in remains the same color it was before. In C++, when we use something called value parameters, it's like using that magic box. When you pass information (like a number or a word) to a function, it's as if you're putting it in the magic box. The function can work with a copy of this information, just like changing the color of the toy car inside the box. So, let's say you have a function called " paintCar " in your C++ program. This function changes the color of a car. When you call this function with the color "blue", it's like putting "blue" in the magic box. Inside the function, it changes the color to "red". But when you take the car (or the value) out of the function, the original "blue" color remains unchanged. Value parameters in C++ let us work with data without messing up the original values. It's like using that box to make changes without affecting the original car. Value parameters in C++ allow you to work with data inside a function without modifying the original values passed as arguments. It's like using a temporary copy or model to make changes without affecting the original object. This is useful when you want to perform operations on the data within the function's scope while keeping the original data intact.

void paintCar(string carColor) {
    carColor = "Red"; // Changes the color inside the function
}

string color = "Blue";
paintCar(color);



### Review Questions

1) If you have a function called "paintCar" that changes the color of a car and you call it with the color "blue", what will be the color of the car outside the function?

2) Explain why, in C++, when you pass information to a function using value parameters, the original data remains unchanged.

3) True or False: Changes made to a value parameter inside a function affect the original argument variable in the calling code.

4) How does the use of value parameters contribute to code safety and prevent unintended side effects?

5) If you have a function called "paintCar" that changes the color of a car and you call it with the color "blue", what will be the color of the car outside the function?

## Reference Variables as Parameters

### Review Questions

## Value and Reference Parameters and Memory Allocation

### Review Questions

## Reference and Parameters and Value-Returning Functions

### Review Questions

## Scope of an Identifier

In C++, the place where an identifier can be used is called its scope. There are 3 kinds of scopes:

Global Scope: If an identifier is declared outside of any functions or classes, it has a global scope and can be used anywhere in the program.

Local Scope: If an identifier is declared inside a function or a group of code, it has local scope. It can only be used inside that function or group of code. As soon as that function or group of code finishes, the identifier is eliminated and cannot be used anymore.

Class Scope: If an identifier is declared inside a class (but not in one of its methods), it has class scope. It can be used by all methods inside that class.

Example:
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
    // cout << classVar << endl; // error: cannot access classVar
}

### Review Questions

## Global Variables, Named Constants, and Side Effects

### Review Questions

## Static and Automatic Variables

### Review Questions

## Debugging: Using Drivers and Stubs

### Review Questions

## Function Overloading: An Introduction

### Review Questions

## Functions with Default Parameters

### Review Questions

## Summary

## Key Terms

## Programming Exercise

## References

This chapter's editor was ...
