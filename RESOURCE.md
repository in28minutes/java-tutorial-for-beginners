# Java Multiple Choice Quiz & Code Challenge

# Step 01: First Challenge : The Print-Multiplication-Table (PMT-Challenge)

1.  What is the objective of the PMT-Challenge?
    
    a. To write a program that prints out a multiplication table for 10, with entries from 1 to 5.
    
    b. To write a program that prints out a multiplication table for 5, with entries from 1 to 10.
    
    c. To write a program that prints out a multiplication table for 5, with entries from 1 to 5.
    
    **Answer: b**
    
2.  What is JShell?
    
    a. A tool for creating and managing databases in Java.
    
    b. A tool for interactive Java programming, allowing you to experiment with Java code and test snippets of code.
    
    c. A tool for creating and managing user interfaces in Java.
    
    **Answer: b**
    
3.  Which Java concept is used to execute a set of statements repeatedly?
    
    a. Conditionals
    
    b. Methods
    
    c. Loops
    
    **Answer: c**



## Exercise 1: PMT Challenge Using For Loop

Using JShell, write a program to display the multiplication table for 7, with entries from 1 to 10 using a for loop.

### Solution

Launch JShell and enter the following commands:

javaCopy code

`for(int i = 1; i <= 10; i++) {
    System.out.println("7 * " + i + " = " + (7*i));
}` 

Output:

Copy code

`7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
7 * 4 = 28
7 * 5 = 35
7 * 6 = 42
7 * 7 = 49
7 * 8 = 56
7 * 9 = 63
7 * 10 = 70` 

## Exercise 2: PMT Challenge Using While Loop

Using JShell, write a program to display the multiplication table for 3, with entries from 1 to 5 using a while loop.

### Solution

Launch JShell and enter the following commands:

javaCopy code

`int i = 1;
while(i <= 5) {
    System.out.println("3 * " + i + " = " + (3*i));
    i++;
}` 

Output:

Copy code

`3 * 1 = 3
3 * 2 = 6
3 * 3 = 9
3 * 4 = 12
3 * 5 = 15`
