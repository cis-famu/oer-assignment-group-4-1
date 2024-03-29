\# Intoduction to Chapter 4

## Objectives

## Introduction

Repetition in coding includes the various types of loops used in c++ coding: while loops, for loops, do-while loops, and if-else statements are helpful for many user prompts programs for menus, counting from arrays, as well as a vast multitude of other uses and purposes. Switch statements, using break and continue statements, help regulate the order and efficiency of the coded loops. The skills built in these sections are major cornerstones of high organizational coding. 

## Why is repetition needed?
-Repetition in C++ allows the user to execute code multiple times, which makes programs more concise and easier to maintain. There's different types of Loops, like for, while, and do-while, which provide the user a level of flexibility in controlling repetition based on various requirements and conditions.

### Review Questions

1.) Why is EOF important?

2.) Explain why repetition is important in C++?

## while Looping (Repetition) Structure

### Case 1: Counter-Controlled while Loops

-A counter-controlled while loop is a type of loop in C++ that repeats a block of code a certain number of times. It's controlled by a counter variable that keeps track of how many times the loop has run. 

EX. 

#include <iostream>
using namespace std;
int main() {
    int counter = 0;
    while (counter < 5) {
        cout << "Counter: " << counter << endl;
        counter++;
    }
    return 0;
}

### Case 2: Sentinel-Controlled while Loops

A sentinel-controlled while loop is a type of loop in programming that repeats a block of code until a specific “sentinel" value is encountered. The sentinel value acts as a signal to stop the loop and exit. A sentinel-controlled while loop is a powerful construct that allows your program to perform tasks until a specific signal (the sentinel value) is received; at this point, the loop terminates repeatedly.


EX

#include <iostream>
using namespace std;
int main() {
    int number;
    cout << "Enter numbers (enter -1 to exit): ";
    cin >> number;
    while (number != -1) {
        std::cout << "You entered: " << number << std::endl;
        std::cin >> number;
    }
    cout << "Exiting loop." << std::endl;
    return 0;
}


### Case 3: Flag-Controlled while Loops

A flag-controlled while loop in C++ is a loop that repeats a block of code as long as a specific condition remains true. Unlike a regular while loop where the condition directly determines whether the loop continues, in a flag-controlled while loop, the loop is controlled by a boolean flag variable.

EX.

#include <iostream>
using namespace std;

int main() {
    bool flag = true;
    int count = 0;
    while (flag) {
        cout << "Count: " << count << endl;
        count++;
        if (count == 5) {
            flag = false; // Set flag to false to exit the loop
        }
    }
    cout << "Exiting loop." << endl;
    return 0;
}

### eof Function

The End of File function in C++ checks whether the (EOF) has been reached on an input stream. It returns true if the end-of-file indicator associated with the stream is set and false otherwise. It is often used with input operations, especially in loops reading from files.

#include <iostream>
#include <fstream>

int main() {
    ifstream file("example.txt");
    char ch;
    while (!file.eof()) {
        file.get(ch);
        cout << ch;
    }
    file.close();
    return 0;
}


### Review Questions
1. Which type of loop in C++ repeats a block of code a certain number of times based on a counter variable?
a) Sentinel-controlled while loop
b) Flag-controlled while loop
c) Counter-controlled while loop
d) eof function loop

2. What type of loop in programming repeats a block of code until a specific "sentinel" value is encountered?
a) Counter-controlled while loop
b) Flag-controlled while loop
c) Sentinel-controlled while loop
d) eof function loop

3. In a flag-controlled while loop, what controls whether the loop continues or not?
a) The counter variable
b) The sentinel value
c) A boolean flag variable
d) The eof function

Answers 1. C, 2. C, 3. C

## for Looping (Repetition) Structure
The for loop in C++ is a versatile control flow construct designed to repeat a block of code a specific number of times. It comprises three key components: initialization, condition evaluation, and update. The loop begins with initialization, where a loop control variable is typically initialized and executed only once at the loop's outset. Subsequently, the condition is evaluated; if true, the code block within the loop executes, allowing for various C++ operations like variable declarations, calculations, and function calls. Following code execution, the loop control variable is updated, commonly incremented or decremented. The loop then returns to the condition evaluation step, repeating the process until the condition becomes false, thereby terminating the loop. 




#include <iostream>

using namespace std;
 int main(){

/* condition is i beginning at zero is incremented until it is less than or equal to 25 */
for (int i = 0; i <= 25; i++) {

/* each increment of i is printed to screen on a new line as long as the value condition is true */    
  cout << i << endl;
}

return 0;
 }



### Review Questions
1. What are the three key components of a for loop in C++?
   a) Initialization, condition evaluation, and sentinel value
   b) Initialization, loop variable update, and sentinel value
   c) Initialization, condition evaluation, and loop variable update
   d) Initialization, condition evaluation, and loop termination

2. In a for loop, when does the initialization step occur?
   a) Before the condition evaluation
   b) After the condition evaluation
   c) After the loop variable update
   d) Before the loop termination

3. What happens during the loop variable update step in a for loop?
   a) The loop control variable is reset to its initial value
   b) The loop control variable is incremented or decremented
   c) The loop terminates
   d) The loop control variable is compared with the sentinel value

Answers 1. C, 2. A, 3. B 

## do... while Looping (Repetition) Structure 

A Do-while loop will execute at least once, then it will test if the while condition is true and continue to loop until it's not. If the initial condition is not met the loop will stop. Do-while loops are good for user validation in menus and escape or default exit inputs. A while loop is also known as a posttest loop because it evaluates after running at least once and possesses an exit condition. 

#include <iostream> 
using namespace std; 
  
int main() 
{ 
    /* Initialization expression i starts at zero */ 
    int i = 0; 
  
    do { 
        /* Loop body*/ 
        cout << "Next loop" << endl; 
  
        /* Update expression */
        i++; 
  
    } 
    /* Test expression */
    while (i < 10); /* Number of loops repeated until i increments to 10 */
  
    return 0; 
}


### Review Questions

What goes first in a do-while loop, the condition or the code?

What is aonther name for the do-while loop?

What is a use for the do-while loop?

How many times will the code in a do while code run initially?


## break and continue Statements

Break and Continue statements can help to regulate the loop process by either ending the loop or allowing it to continue running, also known as ‘jump statements’. Continue statements allow code within the loop to continue looping and break statements allow if certain conditions are met the loop statement to be terminated. Break statements can work in three types of loops: simple loops, nested loops, and infinite loops. In nested loops, break statements will terminate in the innermost loop.

#include <iostream>
#include <cmath>
using namespace std;

int main(){
    int num1, num2, num3, num4, num5, avg;  /* Declare variables*/

    
    do{
        cout << "Enter five numbers" << endl;   //Prompts user to enter 5 numbers.
        cin >> num1 >> num2 >> num3 >> num4 >> num5;    // 5 numbers 

        avg = (num1 + num2 + num3 + num4 + num5)/5;

        
        /*If number is even, continue*/
        if(avg % 2 == 0){
            cout << "EVEN" << endl;
            continue; 
        }
        /*If number is odd break*/ 
        else if(avg % 2 == 1)
        {
            cout << "ODD" << endl;
            break;
        }
    /*Loops until break statement*/    
    }while(1);

    return 0;
}



### Review Questions

What is another name for break and continue statements?

What does a break statement do?

What does a continue statement do?

What loops can break statements be used in?

T/F A break statement in a nested loop will terminate the outer loopfunction?


## Nested Control Structures

Nested Control Structures
Nested loops are loops within loops that execute based on a conditional statement. The inner loop once its condition has been met allows continuation of the outer loop. An example of this could be a do-while loop, wherein a prompt is displayed to the user asking for a character input. This process only continues once the correct input has been made. There is an if-else statement buried within the do-while structure that reports to the user whether or not the correct input has been typed. If for instance, an integer or any non-alphabetical character is input the program will print to the screen “Invalid option”, this will send the user back to the default prompt. The ELSE part of the statement terminates the loop by either outputting “Good job!”  or nothing is output because the user typed ‘Q’.


#include <iostream>
#include <cmath>
using namespace std;

int main(){
    char letter;
    
    do{
        cout << "Please enter a letter | Q = Quit" << endl; //Prompts user to enter a letter.
        cin >> letter;  //Extracts user input from standard input stream

        if(!isalpha(letter)){   //Sentinel-terminted if statement. If char letter is not alphabetic
            cout << "Invalid option" << endl;   //Prints out error statement if condition is true
        }else{                  
            cout << "Good Job!" << endl;    //Prints out success statement
            letter = 'Q';   //Sets letter to the while loop's conditional statement, terminating the loop.
        }
    }while( letter =! 'Q' );    //Sentinal-terminated while loop. If letter is equal to 'Q'

    return 0;
}



### Review Questions

What are nested control structures?

How are nested control structures executed?

What kind of loops usually are on the outside of these control structures?

What kinds of loops can be on the inside of nested control structures?

How many loops can be contained within the outer loop?


## Avoiding Bugs by Avoiding Patches
Software Patch: a piece of code written on top of another piece of code that is intended to fix a bug in the original code
<br>
In the file, here is the data stored:<br>
87 78 83 94<br>
23 89 92 70<br>
92 78 34 56<br>
The objective for this program is to find the sum of the numbers in each line.
<br>
**Program:**<br>
int main()<br>
{<br>
        ifstream infile;<br>
        int i;<br>
        int j;<br>
        int sum;<br>
        int num;<br>
        infile.open("Ch5_LoopWithBugsData.txt");<br>
        for(i=1; i<=4; i++)<br>
        {<br>
            sum=0;<br>
            for (j=1; j<= 4; j++)<br>
            {<br>
                infile>>num;<br>
                cout<<num<<" ";<br>
                sum=sum+num;<br>
            }<br>
            cout<<"sum= "<<sum<<endl;<br>
        }<br>
}<br>
<br>
Sample Run:<br>
87 78 83 94 sum = 342<br>
23 89 92 70 sum = 274<br>
92 78 34 56 sum = 260<br>
56 56 56 56 sum = 224<br>
<br>
In the sample, it is clear that there is a problem because the output contains four lines instead of three, and 56 is repeated four times.

In the program below, a software patch is added to manually cut off the unwanted fourth line:<br>
int main()<br>
{<br>
        ifstream infile;<br>
        int i;<br>
        int j;<br>
        int sum;<br>
        int num;<br>
        infile.open("Ch5_LoopWithBugsData.txt");<br>
        for(i=1; i<=4; i++)<br>
        {<br>
            sum=0;<br>
            if (i != 4) //software patch<br>
            {<br>
                for (j=1; j<= 4; j++)<br>
                {<br>
                    infile>>num;<br>
                    cout<<num<<" ";<br>
                    sum=sum+num;<br>
                }<br>
                cout<<"sum= "<<sum<<endl;<br>
            }<br>
        }<br>
}<br>
<br>
Sample Run (2):<br>
87 78 83 94 sum = 342<br>
23 89 92 70 sum = 274<br>
92 78 34 56 sum = 260<br>
<br>
- Now, the program is working. However this shows that the program is executing extra statements. Adding the software patch did elimate the symptom, but is a poor programming practice.

- This problem can be eliminated by correctly setting the values of the loop control variable. The values assigned to loop control variable i are 1, 2, 3, and 4. This is an example of the loop executing one too many/few times.
<br>
Rewritten code:<br>
{<br>
        for (i=1; i<=3; i++)<br>
        {<br>
            sum=0;<br>
            for (j=1; j<=4; j++)<br>
            {<br>
                infile>>num;<br>
                cout<<num<<" ";<br>
                sum=sum+num;<br>
            }<br>
            cout<<"sum= "<<sum<<endl;<br>
        }<br>
        return 0;<br>
}<br>

### Review Questions
1. What does a software patch aim to do in programming?
   a) Optimize code for better performance
   b) Introduce new features into existing code
   c) Fix a bug in the original code
   d) Enhance code readability

2. What was the problem with the initial program that required the addition of a software patch?
   a) The code had syntax errors
   b) The loop control variable was not properly managed
   c) The file couldn't be opened for reading
   d) The output formatting was incorrect

3. How was the issue resolved without adding a software patch in the rewritten code?
   a) By introducing new variables
   b) By correctly setting the values of the loop control variable
   c) By changing the file reading mechanism
   d) By modifying the output display format

Answers 1. C, 2. B, 3. B

## Debugging Loops
Most times, the complier will identify errors, like syntax errors. If there are logical errors, we have to personally look for them.

Using an algorithm, it is important to make sure it works properly.
- Algorithms that are a simple sequential flow or contains a branch, it can be hand-traced or use the debugger, if any that is provided by IDE.
- Loops are harder to debug. The correctness of a loop can be verified by using loop invariants
Ex. Let 'p' be a loop invariant and 'q' be the (logical) expression in a loop statement. Then 'p' && 'q' remains true before each iteration of the loop and 'p' && not(q) is true after the loop termination

**COMMON ERRORS**<br>
- If a loop turns to be an infinite loop, the error is most likely in the logical expression that controls the execution of the loop

- If you have reversed an inequality, an assignment statement symbol appears in place of the equality operator
- If && appears in place of | |
- If the loop changes the values of variables, you can print the values of the variables before and/or after each iteration or you can use your IDE’s debugger, if any, and watch the values of variables during each iteration.

### Review Questions
Review Questions:

1. How can the correctness of a loop be verified using loop invariants?
   a) By checking if the loop executes a specific number of times
   b) By ensuring that the loop terminates
   c) By verifying that a logical expression remains true before each iteration and after loop termination
   d) By counting the number of iterations manually

2. What is a common error if a loop becomes an infinite loop?
   a) Syntax error in the loop initialization
   b) Logical expression controlling the loop execution
   c) Incorrect loop variable update
   d) Missing semicolon at the end of the loop

3. When debugging loops, what can be helpful in tracking the values of variables during each iteration?
   a) Using loop invariants
   b) Hand-tracing the loop
   c) Printing the values of variables before and/or after each iteration
   d) Checking for syntax errors in the loop body

Answers 1. C, 2. B, 3. C
## Summary


Understanding core concepts about control structures and repetition in C++ gives the coder foundational tools including conditional statements, looping structures, and switch statements. These skills are essential for directing the program flow and creating efficient usable code. By obtaining these skills, programmers gain the ability to make decisions, repeat actions, and manage control flow effectively, thus allowing a greater capability to write complex though maintainable programs in C++.


## Key Terms
1. decision maker- an expression in an if statement, which determines whether to execute the statement that follows it.
2. infinite loop- a loop that continues to execute endlessly.
3. loop control variable- a variable that controls the end of the loop.
4. counter-controlled while loop - a while loop that is used when you know how many items of data are to be read; the loop will continue until the condition designated by the counter is met or evaluates to false.
5. flag-controlled while loop- uses a Boolean variable to control the execution of the loop.
6. end-of-file (EOF)-controlled while loop- a while loop that stops when it reaches the end of the input file.
7. Fibonacci number- a number in the Fibonacci sequence.
8. Fibonacci sequence- an= an-1+an-2
9. for loop- used to simplify the writing of counter-controlled loops; consists of an initialization statement, the loop condition, and the update statement.
10. nesting- a process that involves putting one control structure inside another.
11. divisor- suppose that m and n are integers and m is nonzero. Then m is called a divisor of n if n=mt for some integer t; that is, when m divides n, the remainder is 0.

## Programming Exercise
1.) Write a program that prints numbers from 1 to 10 using a counter-controlled while loop.

2.) Write a program that outputs even numbers from 2 to 20 using a flag-controlled while loop.

3.) Write a program that prompts the user to enter numbers until they enter 0. After each input, print the sum of all entered numbers.

## References

Chatgpt. ChatGPT. (2024).  https://chat.openai.com/

From <https://github.com/cis-famu/oer-assignment-group-4-1/blob/main/Chapter-3.md> 

Malik, D. S. (2018). C++ Programming: From problem analysis to program design (8th ed.). Cengage Learning.

From <https://github.com/cis-famu/oer-assignment-group-4-1/blob/main/Chapter-3.md> 

Hanansani. (2024, January 29). Mastering loops in C++: A comprehensive guide. Medium. https://medium.com/@hanansani2002/mastering-loops-in-c-a-comprehensive-guide-15a621de10c8 

C++ for loop. (n.d.-a). https://www.w3schools.com/cpp/cpp_for_loop.asp 

GfG. (2023, December 26). C++ loops. GeeksforGeeks. https://www.geeksforgeeks.org/cpp-loops/ 

C++ while and do...while loop. Programiz. (n.d.). https://www.programiz.com/cpp-programming/do-while-loop  



This Chapter's editor was...(Briana Harvey)
