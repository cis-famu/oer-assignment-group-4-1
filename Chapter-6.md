# Introduction to Chapter 6

## Objectives

## Introduction

## Enumeration Type
The three things needed to use an enumeration type are:
1. A name for the data type.
2. A set of values for the data type.
3. A set of operations on the values.

The syntax is as follows:
``` enum class Weekday {
         MONDAY,
         TUESDAY
         WEDNESDAY
         THURSDAY
         FRIDAY
}; ```

The days of the week in this example are considered the enumerators.

### Declaring Variables and Assignment
The syntax for declaring variables of this type is:

``` Weekday day = Weekday::MONDAY; ```

We declared "day" of type "Weekday" and assigned the value "Weekday::MONDAY"

### Operations on Enumeration Types
* With enumeration types math operations are not allowed.
* In order to do them while using enumeration types you must use the cast operator.

### Review Questions
1. The three things needed to use an enumeration type are a name for the data type, a set of values for the data type, and a set of operations on the values.

  A. True
  B. False

2. Which of the following is the correct syntax for declaring a variable of the `Weekday` enum type and assigning it the value `MONDAY`?
  
   A. `Weekday day = Weekday.MONDAY;`
   B. `Weekday day = MONDAY;`
   C. `Weekday::MONDAY day;`


3. Math operations on enumeration types are allowed directly without any restrictions.
  
   A. True
   B. False

Answers - 1. A, 2. C, 3. B.

## Namespaces

### Review Questions

## ```string```Type

### Additional ```string``` Operations

### Review Questions

## Summary

## Key Terms
1. enumeration type- a user-defined simple data type.
2. enumerators- an identifier used in an enumeration type.
3. anonymous type- a data type in which you directly specify values in the variable declaration with no type name.
4. array subscript operator- used to access an individual character within a string by specifying the character’s position within the square brackets.

## Programming Exercises

## References

This chapters editor was (...).
