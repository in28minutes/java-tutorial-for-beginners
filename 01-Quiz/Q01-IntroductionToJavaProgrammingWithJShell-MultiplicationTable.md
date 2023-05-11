## Introduction to Programming with Print-Multiplication-Table - MCQ

## Step 02: Introducing JShell

----------

1.  What does JShell stand for? 
    a. JavaShell  
    b. JavaScriptShell  
    c. JupyterShell

**Answer: a. JavaShell**

JShell stands for Java Shell.

Introduced in Java 9, JShell is a Read-Eval-Print Loop (REPL) tool that allows developers to run Java statements and expressions interactively in the console without having to wrap them in classes or methods. This is particularly useful for testing small bits of code, learning new features, or prototyping.

To explain why the other options are incorrect:

b. JavaScriptShell - This is not accurate because JShell is a feature of Java, not JavaScript. These are two different programming languages with distinct features and use cases.

c. JupyterShell - This option is not correct either. Jupyter is a separate open-source project that provides a web-based interactive computing environment for multiple programming languages, including Python, Julia, and R. It has no direct connection with Java or JShell.

----------

2.  What is the purpose of JShell? 
    a. To create graphical user interfaces  
    b. To evaluate and execute Java code and provide immediate results  
    c. To debug Java code

**Answer: b. To evaluate and execute Java code and provide immediate results**
JShell is designed to evaluate and execute Java code and provide immediate results. This is a feature known as a Read-Eval-Print Loop (REPL), which is common in scripting languages but was introduced in Java with the release of Java 9.

To further explain:

a. To create graphical user interfaces - While Java is indeed used to create graphical user interfaces (GUIs), this is not the primary purpose of JShell. GUI creation in Java typically involves using libraries such as Swing or JavaFX, not JShell.

b. To evaluate and execute Java code and provide immediate results - This is the correct answer. JShell allows developers to input Java code directly and see results immediately, without needing to compile or run a full program. This makes JShell a useful tool for testing snippets of code, learning new features of the language, or prototyping.

c. To debug Java code - While you could potentially use JShell to test and debug small snippets of code, this is not its primary function. Traditional debugging usually involves tools that can step through code, inspect variable values, set breakpoints, and so on. JShell is more of an interactive console for running code and seeing immediate results.
----------

3.  What command can be used to exit JShell? 
    a. /end  
    b. /exit  
    c. /quit

**Answer: b. /exit**
The command to exit JShell is indeed /exit.

Here's a breakdown of each option:

a. /end - This is not a valid command in JShell. JShell doesn't recognize this command and will give you an error if you try to use it.

b. /exit - This is the correct answer. Using the /exit command in JShell will terminate the session and return you to your system's command line.

c. /quit - This is not a valid command in JShell. Similar to /end, JShell doesn't recognize this command and will give you an error if you try to use it.

It's worth noting that JShell also supports a variety of other slash commands (/) for various functions. For instance, /help will provide a list of all available commands and /list will show you all the code you've entered during your current JShell session.

## Step 03: Welcome to Problem Solving


1.  What is the problem solving technique used in this step?
    
    -   a) Reverse Engineering
    -   b) Subdivision
    -   c) Deductive Reasoning
    -   Answer: b) Subdivision

The correct answer is indeed b) Subdivision.

Here's the explanation for each option:

a) Reverse Engineering - This is a process where you start with a finished product and then work backward to understand how it was made. This method is often used in software engineering to understand the source code of a program when the source code is not available. In the context of the question, reverse engineering does not apply.

b) Subdivision - This is the correct answer. In problem-solving, subdivision is a technique where a complex problem is broken down into smaller, more manageable parts. This is a common technique in programming and is often used to simplify the process of writing code. In the context of the multiplication table program, subdivision is used to break down the complex problem of generating a multiplication table into simpler tasks like iterating over numbers and printing individual rows of the table.

c) Deductive Reasoning - This is a process of reasoning from one or more general statements to reach a logically certain conclusion. While this is a valuable problem-solving skill, it's not the primary technique being employed in this situation. The task of creating a multiplication table is more about systematically applying a set of rules (i.e., the multiplication operation) to a range of inputs, rather than drawing conclusions from general principles.



2.  What is the result of 5 * 3?
    
    -   a) 8
    -   b) 10
    -   c) 15
    -   Answer: c) 15

The correct answer is indeed c) 15.

Here's the explanation:

Multiplication is one of the basic operations in arithmetic. When you multiply 5 by 3, you are essentially adding 5 three times.

So, 5 * 3 = 5 + 5 + 5 = 15

Therefore, the result of 5 times 3 is 15, making option c) the correct answer.

3.  How many times do we repeat the calculation in this step?
    
    -   a) 5 times
    -   b) 10 times
    -   c) 15 times
    -   Answer: b) 10 times



## Step 04: Introducing Expressions

1.  What is the result of 5 * 3?
    
    -   a) 8
    -   b) 10
    -   c) 15
    -   Answer: c) 15
2.  What are the operands in the expression 5 * 3?
    
    -   a) 5, 3
    -   b) 5
    -   c) 3
    -   Answer: a) 5, 3

The correct answer is a) 5, 3.

In the expression 5 * 3, 5 and 3 are the operands. In general, an operand in programming and mathematics is a term of a mathematical operation that takes part in the operation.

In this case, the operation is multiplication (*), and the two numbers (5 and 3) that are being multiplied are the operands. So, the numbers 5 and 3 are the values on which the multiplication operation is performed. Hence, the answer is a) 5, 3.

3.  What is the modulo operator in Java?
    
    -   a) *
    -   b) %
    -   c) +
    -   Answer: b) %

The correct answer is b) %.

In Java, the modulo operator is represented by the percentage symbol (%). This operator returns the remainder of a division operation. For example, if you divide 10 by 3, the remainder is 1. So, in Java, the expression 10 % 3 would yield the result 1.

This operator is useful for many programming tasks such as determining if a number is even or odd (a number is even if it's divisible by 2 with no remainder, so num % 2 would be 0), or wrapping values within a certain range (like getting the remainder of a division by the size of an array to always get a valid index).

Therefore, the modulo operator in Java is % (option b).

## Step 05: Programming Exercise PE-1 (With Solutions)

1.  Write an expression to calculate the number of minutes in a day.
    
    -   a) 24 * 60
    -   b) 60 + 24
    -   c) 60 * 24
    -   Answer: c) 60 * 24
2.  Write an expression to calculate the number of seconds in a day.
    
    -   a) 24 * 60 * 60
    -   b) 60 + 60 + 24
    -   c) 60 * 60 * 24
    -   Answer: c) 60 * 60 * 24



## Step 06: Operators

1.  Which of the following is a valid operator in Java?
    
    -   a) **
    -   b) $
    -   c) *
    -   Answer: c) *
2.  What is the result of 5 / 2 in Java?
    
    -   a) 2
    -   b) 2.0
    -   c) 2.5
    -   Answer: a) 2
3.  What is the order of sub-expression evaluation in the expression 5 + 5 * 6?
    
    -   a) 5 + 5, then 10 * 6
    -   b) 5 * 6, then 5 + 30
    -   c) Depends on operand types
    -   Answer: b) 5 * 6, then 5 + 30
4.  How can parentheses be used to group parts of an expression?
    
    -   a) They have no effect on the evaluation of an expression
    -   b) They are used to specify the order of sub-expression evaluation
    -   c) They are used to introduce new operators
    -   Answer: b) They are used to specify the order of sub-expression evaluation


## Step 07: Introducing Console Output

1.  Which built-in Java method displays text on the console?
    
    -   a) System.out.print()
    -   b) System.out.display()
    -   c) System.out.println()
    -   Answer: c) System.out.println()
2.  What is a String literal in Java?
    
    -   a) A sequence of numbers
    -   b) A piece of text with numeric characters
    -   c) A keyword used for control flow
    -   Answer: b) A piece of text with numeric characters
3.  How do you print the exact text "Hello World" on the console using System.out.println()?
    
    -   a) System.out.println("Hello World")
    -   b) System.out.println(Hello World)
    -   c) System.out.print("Hello World")
    -   Answer: a) System.out.println("Hello World")
4.  Can you pass a mathematical expression like 5 * 3 = 15 as an argument to System.out.println() in Java?
    
    -   a) Yes, it will evaluate the expression and print the result
    -   b) No, it will throw an error
    -   Answer: b) No, it will throw an error

## Step 08: Programming Exercise PE-02
## Step 09: Solutions to PE-02
Question 1: What is the output of the following code?

```
System.out.println("Hello World");
```
a) HelloWorld
b) Hello World
c) "Hello World" 

Answer: b) Hello World

Question 2: What is the output of the following code?

```
System.out.println("5 * 3");
```
a) 5 * 3
b) 15
c) "5 * 3"

Answer: a) 5 * 3

Question 3: What is the output of the following code?

```
System.out.println(5 * 3);
```
a) 5 * 3
b) 15
c) "15"


Answer: b) 15

Question 4: What is the output of the following code?

```
System.out.println(60 * 60 * 24);
```
a) 86400
b) 86400.0
c) "86400"

Answer: a) 86400



## Step 10: Whitespace, Case Sensitiveness and Escape Characters

1.  What does whitespace refer to in Java?

-   a) Any sequence of continuous digits.
-   b) Any sequence of continuous space, tab or newline characters.
-   c) Any sequence of continuous special symbols.

Answer: b) Any sequence of continuous space, tab or newline characters.

2.  Why is it important to use the correct case when calling pre-defined Java elements?

-   a) Because Java is case-sensitive, and using the incorrect case will result in an error.
-   b) Because Java is case-insensitive, and using the incorrect case will result in an error.
-   c) Because Java is not case-sensitive, and using the incorrect case will not result in an error.

Answer: a) Because Java is case-sensitive, and using the incorrect case will result in an error.

3.  What is the escape sequence for inserting a tab in a string literal?

-   a) \n
-   b) \t
-   c) \b

Answer: b) \t


## Step 11: More On Method Calls

1.  What is the purpose of parentheses in method calls?
    
    -   a) They are optional and can be left out
    -   b) They are used to separate individual parameters with a comma
    -   c) They enclose all the parameters and are a necessary part of the syntax
    -   **Answer: c**
2.  What does the Math.random() method do?
    
    -   a) It prints a random integer between 0 and 1
    -   b) It prints a random real number between 0 and 1
    -   c) It returns the maximum of two given numbers
    -   **Answer: b**
3.  What does the Math.min() method return?
    
    -   a) The maximum of two given numbers
    -   b) The minimum of two given numbers
    -   c) The sum of two given numbers
    -   **Answer: b**


## Step 12: More Formatted Output

1.  Which method can accept a variable number of arguments? 
- a) System.out.println() 
- b) System.out.printf() 
- c) Math.min()

Answer: b) System.out.printf()

2.  Which of the following is a predefined literal used as a format specifier in printf() to format data of type int? 
- a) %f 
- b) %d 
- c) %s

Answer: b) %d

3.  What will be the output of the following code?

```
System.out.printf("%d + %d + %d = %d", 3, 4, 5, 3 + 4 + 5).println();
```

- a) 3 + 4 + 5 = 12 
- b) 3 4 5 = 12 
- c) 3 + 4 = 7

Answer: a) 3 + 4 + 5 = 12


## Step 13: Introducing Variables

1.  What is a variable in Java? 
 - a) A method to print calculated values 
 - b) A keyword to reserve memory for data 
 - c) A character to represent symbols in a string

Answer: b)

2.  How can we change the value of a variable? 
- a) Using the System.out.printf() method 
- b) By calling a method with a different argument 
- c) By assigning a new value to it using the assignment operator =

Answer: c)

3.  How can we use variables to simplify code? 
- a) By defining a new method 
- b) By storing the output of a method in a variable 
- c) By assigning changing values to a variable and using it in a statement

Answer: c)


## Step 15: Using Variables Quiz

1.  Why is it important to declare variables before using them in a Java program?
    
    -   a) It makes the code look more organized
    -   b) It ensures that the variables have values assigned to them
    -   c) It avoids errors due to uninitialized variables
    
    Answer: c
    
2.  In Java, every variable must be declared with a __________.
    
    -   a) keyword
    -   b) value
    -   c) type
    
    Answer: c
    
3.  What happens when you try to store a double value into an integer variable?
    
    -   a) It is allowed without any issues
    -   b) An error is generated as the types are incompatible
    -   c) The value is automatically rounded up to the nearest integer
    
    Answer: b



## Step 16: Variables: Behind-The-Scenes

1.  What is the process of giving a value to a variable during its declaration called? 
- A) Assignment 
- B) Initialization 
- C) Declaration 
Answer: B
    
2.  What happens when a variable's initial value is another variable previously defined? 
- A) The initial value of the first variable is lost 
- B) The value of the second variable is lost 
- C) The value stored in the first variable's slot is copied to the second variable's slot 
Answer: C
    
3.  Which of the following is not allowed in variable assignment? 
- A) From a literal value to a variable, having compatible types 
- B) From a variable to another variable, of compatible types 
- C) Assignment to a constant literal 
Answer: C


# Step 17: Naming Variables

1.  Which of the following characters is allowed in a variable name in Java?

- A) # 
- B) $ 
- C) % 
- D) !

**Answer: B)** The special character `$` is allowed in a variable name in Java.

2.  Which of the following variable names is not allowed in Java?

- A) _score 
- B) 3goals 
- C) yellowCard 
- D) goals3

**Answer: B)** A variable name cannot start with a numerical digit [0-9].

3.  Which of the following is a recommended naming convention for variables in Java?

- A) start variable names with uppercase letters 
- B) use long variable names to make your code more expressive 
- C) use CamelCase for variable names with multiple words 
- D) use special characters like ! or % in variable names

**Answer: C)** In Java, it is recommended to use CamelCase when we have multiple words in variable name.



## Step 18: Java Primitive Types Quiz

1.  Which of the following is NOT an integral value primitive type in Java? 
- a) byte 
- b) short 
- c) float

Answer: c) float

2.  What is the default type for floating type values in Java with size 64 bits? 
- a) double 
- b) float 
- c) int

Answer: a) double

3.  What is the correct way to store a single character symbol in a char variable in Java? 
- a) within double quotes "" 
- b) within parentheses () 
- c) within single quotes ''

Answer: c) within single quotes ''


## Step 19: Choosing A Data Type Quiz

1.  Which data type is best for storing the number of goals scored by a team in a football match?

a) Byte 
b) Short 
c) Long

Answer: b) Short

2.  Which data type is best for storing the average rainfall in a month?

a) Int 
b) Float 
c) Double

Answer: c) Double

3.  Which data type is best for storing the grade of a student in a class?

a) Int 
b) Char 
c) Float

Answer: b) Char



## Step 20: Assignment Operator Quiz

1.  What is the assignment operator in Java?

-   a) ==
-   b) =
-   c) +

Answer: b) =

2.  What is the output of the following code: `int x = 5; x = x + 3;`

-   a) 3
-   b) 8
-   c) 5

Answer: b) 8

3.  What is the result of the following code: `int y = 10; y = y - 2; y = y - 3;`

-   a) 3
-   b) 10
-   c) 5

Answer: c) 5




## Step 21: Java Operators

1.  What is the difference between prefix and postfix versions of increment and decrement operators? 
- a) There is no difference between prefix and postfix versions. 
- b) Prefix version returns the updated value while postfix returns the original value. 
- c) Postfix version returns the updated value while prefix returns the original value.

Answer: b) Prefix version returns the updated value while postfix returns the original value.

2.  What is the compound assignment operator used for? 
- a) To assign a new value to a variable. 
- b) To combine the = with a numeric operator. 
- c) To compare two values.

Answer: b) To combine the = with a numeric operator.

3.  What does the expression i %= 2 mean?  
- a) Add 2 to the value of i and store the result back into i. 
- b) Divide i by 2, and store the result back into i. 
- c) Divide i by 2, and store the remainder back into i.

Answer: c) Divide i by 2, and store the remainder back into i.



# Step 23: Introducing Conditionals - the if

1.  Which is the correct comparison operator in Java?

-   =
-   ==

Answer: ==

2.  What is the structure of an if statement in Java?

-   if {condition} (statement);
-   if {statement} (condition);
-   if (condition) {statement};

Answer: if (condition) {statement};

3.  What is the output of the following code:

```
int a = 5;
int b = 10;
if (a > b) {
  System.out.println("a is greater than b");
} else {
  System.out.println("b is greater than a");
}
```

-   a is greater than b
-   b is greater than a

Answer: b is greater than a




## Step 26:  `if`  Statement again

1.  What is the output of the following code snippet?

```
int x = 7;
if (x < 10) {
    System.out.println("x is less than 10");
}
else {
    System.out.println("x is greater than or equal to 10");
}
```

A. x is less than 10 
B. x is greater than or equal to 10 
C. Compiler Error

Answer: A

2.  What happens when we don't use statement blocks with if conditional?

A. The condition statement only controls the execution of the first statement. 
B. The condition statement controls the execution of all the statements. 
C. The code will not compile.

Answer: A

3.  What is the benefit of using statement blocks with if conditionals?

A. Improves code readability 
B. Increases the number of statements that can be executed conditionally 
C. Improves program efficiency

Answer: A



## Step 27: Introducing Loops: The  `for`  Statement

1.  What does a for loop iterate over? 
- a) a fixed number of iterations 
- b) an infinite number of times 
- c) a variable number of times **Answer: c**
    
2.  What is the syntax of a for loop? 
- a) for (initialization; update; condition) 
- b) for (update; condition; initialization) 
- c) for (condition; initialization; update) **Answer: a**
    


# Step 28-29

1.  What is the output of the following code snippet?

```
for (int i=0; i<=10; i++) {
    System.out.printf("%d * %d = %d", 6, i, 6*i).println();
}
```

a. Multiplication table of 6 
b. Multiplication table of 10 
c. Multiplication table of 7

**Answer: a. Multiplication table of 6**

2.  What is the output of the following code snippet?

```
for (int i=1; i<=10; i++) {
    System.out.printf(i*i).println();
}
```

a. The squares of integers from 1 to 10 
b. The squares of first 10 even integers 
c. The squares of first 10 odd integers

**Answer: a. The squares of integers from 1 to 10**

3.  What is the output of the following code snippet?

```
for (int i=10; i>0; i--) {
    System.out.printf(i).println();
}
```

a. The integers from 10 to 1 
b. The integers from 1 to 10 
c. The squares of integers from 1 to 10 in reverse order

**Answer: a. The integers from 10 to 1**



## Step 30: Puzzling You With  `for`

#### 1. Which of the following is true about the for loop construct in Java?

-   A) All components of the for loop are required.
-   B) Only the condition component of the for loop is optional.
-   C) All components of the for loop are optional.

Answer: C) All components of the for loop are optional.

#### 2. What happens if the condition component of a for loop is left empty?

-   A) The loop continues indefinitely until stopped externally.
-   B) The loop exits immediately without executing any statements.
-   C) The loop executes once and exits immediately.

Answer: A) The loop continues indefinitely until stopped externally.

#### 3. What is the output of the following code snippet?

```
int i = 1;
for (; i <= 10; i++);
System.out.println(i);
```

-   A) 1
-   B) 10
-   C) 11

Answer: C) 11