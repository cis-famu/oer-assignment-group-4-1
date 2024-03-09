\# Intoduction to Chapter 4

## Objectives

## Introduction

Repetition in coding includes the various types of loops used c++ coding, while loops, for loops, do-while loops, and if-else statements are useful for many user prompts programs for menus, counting from arrays, as well as a vast multitude of other uses and purposes. Switch statements, using break and continue statements help to regulate the order and efficiency of the loops being coded. The skills built in these sections are major cornerstones of high organizational coding. 

## Why is repetition needed?
Repetition in C++ allows the user to execute code multiple times, which makes programs more concise and easier to maintain. There's different types of Loops like for, while, and do-while, which provide the user a level of flexibility in controlling repetition based on various requirements and conditions.

### Review Questions

## while Looping (Repetition) Structure

### Designing while Loops

### Case 1: Counter-Controlled while Loops

### Case 2: Sentinel-Controlled while Loops

### Case 3: Flag-Controlled while Loops

### eof Function

### More on Expressions in while Statements

### Review Questions

## for Looping (Repetition) Structure

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

### Choosing the Right Looping Structure

### Review Questions

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

## Summary

## Key Terms

## Programming Exercise

## References

This Chapter's editor was...(Put Name Here)
