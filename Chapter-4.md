# Intoduction to Chapter 4

## Objectives

## Introduction

## Why is repetition needed?

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

### Review Questions

## do... while Looping (Repetition) Structure

### Choosing the Right Looping Structure

### Review Questions

## break and continue Statements

### Review Questions

## Nested Control Structures

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
