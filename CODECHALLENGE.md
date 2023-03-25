## Java Code Challenge

### Step 01: First Challenge : The Print-Multiplication-Table (PMT-Challenge)


#### Exercise 1: PMT Challenge Using For Loop

Using JShell, write a program to display the multiplication table for 7, with entries from 1 to 10 using a for loop.

###### Solution

Launch JShell and enter the following commands:


```
for(int i = 1; i <= 10; i++) {
    System.out.println("7 * " + i + " = " + (7*i));
}
``` 

Output:


```
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
7 * 4 = 28
7 * 5 = 35
7 * 6 = 42
7 * 7 = 49
7 * 8 = 56
7 * 9 = 63
7 * 10 = 70
``` 

#### Exercise 2: PMT Challenge Using While Loop

Using JShell, write a program to display the multiplication table for 3, with entries from 1 to 5 using a while loop.

###### Solution

Launch JShell and enter the following commands:


```
int i = 1;
while(i <= 5) {
    System.out.println("3 * " + i + " = " + (3*i));
    i++;
}
```

Output:


```
3 * 1 = 3
3 * 2 = 6
3 * 3 = 9
3 * 4 = 12
3 * 5 = 15
```


### Step 02: Introducing JShell


#### Exercise 1:

Create a JShell snippet that defines a variable `myNumber` with a value of 10, then use an expression to calculate and display the square of `myNumber`.

##### Solution:

```

jshell> int myNumber = 10;
myNumber ==> 10
 jshell> myNumber * myNumber
$1 ==> 100
```

#### Exercise 2:

Create a JShell snippet that defines a method called `isEven` that takes an integer argument `n` and returns a boolean value indicating whether `n` is even or not. Then, call the method with an integer value of your choice and display the result.

##### Solution:

```

jshell> boolean isEven(int n) {
   ...>     return n % 2 == 0;
   ...> }
|  created method isEven(int)

jshell> isEven(7)
$1 ==> false

jshell> isEven(12)
$2 ==> true
```



### Step 03: Welcome to Problem Solving


#### Java Coding Exercise 1

Using JShell, write a Java code snippet to calculate and print the result of multiplying 7 by 4.

##### Solution

```

jshell> int result = 7 * 4;
result ==> 28

jshell> System.out.println(result);
28
```

#### Java Coding Exercise 2

Using JShell, write a Java code snippet to print the multiplication table for 9, with entries from 1 to 5.

#####  Solution

```

jshell> for (int i = 1; i <= 5; i++) {
   ...>     int result = 9 * i;
   ...>     System.out.println("9 * " + i + " = " + result);
   ...> }
9 * 1 = 9
9 * 2 = 18
9 * 3 = 27
9 * 4 = 36
9 * 5 = 45
```

Note: The above solution uses a for loop to execute the code 5 times, once for each table entry, and prints the result of each calculation.



### Step 04: Introducing Expressions


#### Exercise 1: 
Write a Java program using JShell to calculate the area of a square with side length of 7 units. Use the appropriate Java operators and follow the steps below:

1.  Start JShell.
2.  Define a variable `sideLength` with a value of 7.
3.  Calculate the area of the square and store it in a variable called `area`.
4.  Print the value of `area`.
5.  Exit JShell.

##### Solution:

```

jshell> int sideLength = 7;
sideLength ==> 7
 jshell> int area = sideLength * sideLength;
area ==> 49
 jshell> System.out.println("Area of the square is: " + area);
Area of the square is: 49
 jshell> /exit
 ```

#### Exercise 2: 
Write a Java program using JShell to calculate the volume of a rectangular prism with length, width, and height of 4, 5, and 6 units respectively. Use the appropriate Java operators and follow the steps below:

1.  Start JShell.
2.  Define three variables `length`, `width`, and `height` with values of 4, 5, and 6 respectively.
3.  Calculate the volume of the rectangular prism and store it in a variable called `volume`.
4.  Print the value of `volume`.
5.  Exit JShell.

##### Solution:

```
jshell> int length = 4;
length ==> 4

jshell> int width = 5;
width ==> 5

jshell> int height = 6;
height ==> 6

jshell> int volume = length * width * height;
volume ==> 120

jshell> System.out.println("Volume of the rectangular prism is: " + volume);
Volume of the rectangular prism is: 120

jshell> /exit

```

### Step 05: Programming Exercise PE-1 (With Solutions)


####  Exercise 1

Write a JShell command to calculate the average of three integers: 10, 20, and 30.

##### Solution:

```
jshell> int num1 = 10;
jshell> int num2 = 20;
jshell> int num3 = 30;
jshell> int average = (num1 + num2 + num3) / 3;
jshell> average
average ==> 20
```

####  Exercise 2

Write a JShell command to convert a temperature of 75 degrees Fahrenheit to Celsius.

##### Solution:

```
jshell> double fahrenheit = 75.0;
jshell> double celsius = (fahrenheit - 32) * 5 / 9;
jshell> celsius
celsius ==> 23.88888888888889
```

Note: The formula to convert Fahrenheit to Celsius is: (°F - 32) * 5/9 = °C


###  Step 06: Operators

#### Exercise 1: Operator Practice

Write a Java program using JShell that takes two integers as input and prints their sum, difference, product, and quotient. Use appropriate operators to perform these operations.

#####  Solution

```
// Use JShell to declare variables and perform arithmetic operations
int num1 = 10;
int num2 = 5;

// Calculate and print sum, difference, product, and quotient
System.out.println("Sum: " + (num1 + num2));
System.out.println("Difference: " + (num1 - num2));
System.out.println("Product: " + (num1 * num2));
System.out.println("Quotient: " + (num1 / num2));
```

#### Exercise 2: Operator Precedence

Write a Java program using JShell that takes three integers as input and calculates the value of the following expression:

`(num1 + num2) * num3 / 2`

##### Solution

```
// Use JShell to declare variables and perform arithmetic operations
int num1 = 5;
int num2 = 10;
int num3 = 2;

// Calculate the value of the expression
int result = (num1 + num2) * num3 / 2;

// Print the result
System.out.println("Result: " + result);

```

Explanation:

-   First, the expressions inside the parentheses `(num1 + num2)` are evaluated, resulting in the sum of `num1` and `num2`.
-   Next, the result of the previous step is multiplied by `num3`, giving `(num1 + num2) * num3`.
-   Finally, the result of the previous step is divided by `2`, resulting in the final value of the expression.


### Step 07: Introducing Console Output


#### Exercise 1:

Challenge: Write a Java program that takes a user's name as input and greets the user by printing "Hello, [name]!" to the console using JShell.

##### Solution:

```
jshell> String name = "Alice";
name ==> "Alice"

jshell> System.out.println("Hello, " + name + "!");
Hello, Alice!
``` 

#### Exercise 2:

Challenge: Write a Java program that takes two numbers as input and prints their product in the format "[num1] * [num2] = [product]" to the console using JShell.

##### Solution:

```
jshell> int num1 = 5;
num1 ==> 5

jshell> int num2 = 3;
num2 ==> 3

jshell> int product = num1 * num2;
product ==> 15

jshell> System.out.println(num1 + " * " + num2 + " = " + product);
5 * 3 = 15
```




### Step 08: Programming Exercise PE-02



#### Exercise 1

Using JShell, write a program that prints out the message "Hello World" onto the console.

##### Solution

```
System.out.println("Hello World");
```

#### Syntax Revision

```
//Numeric and string literals
System.out.println("Hello World");

//Expressions
//There are no expressions in this code.

//Operators
//There are no operators in this code.

//Operands
//There are no operands in this code.

//Method calls
System.out.println();
```

#### Exercise 2

Using JShell, write a program that prints out the result of the expression 5 * 3, both as an expression and as the calculated value.

##### Solution

```
//Print the expression
System.out.println("5 * 3");

//Print the calculated value
System.out.println(5 * 3);
```

#### Syntax Revision

```
//Numeric and string literals
System.out.println("5 * 3");

//Expressions
System.out.println(5 * 3);

//Operators
//The * operator is used to multiply 5 and 3.

//Operands
//The operands in this code are 5 and 3.

//Method calls
System.out.println();
```



### Step 09: Solutions to PE-02

#### Exercise 1

Create a program in JShell that displays the sum of 2 and 3.

**Solution:**


```
jshell> int sum = 2 + 3;
sum ==> 5
jshell> System.out.println("The sum of 2 and 3 is: " + sum);
The sum of 2 and 3 is: 5
``` 

#### Exercise 2

Create a program in JShell that converts a temperature from Celsius to Fahrenheit. The formula for converting Celsius to Fahrenheit is F = (C * 1.8) + 32.

**Solution:**

```
jshell> double celsius = 20.0;
celsius ==> 20.0
jshell> double fahrenheit = (celsius * 1.8) + 32;
fahrenheit ==> 68.0
jshell> System.out.println(celsius + " degrees Celsius is equal to " + fahrenheit + " degrees Fahrenheit.");
20.0 degrees Celsius is equal to 68.0 degrees Fahrenheit.
```


### Step 10: Whitespace, Case sensitiveness and Escape Characters

#### Exercise 1: Whitespace Counter

Write a program that takes a string input and counts the number of whitespace characters in it. Use JShell to test your program with the following inputs:

Input 1:


`"The quick brown fox jumps over the lazy dog."` 

Expected Output 1:

`8` 

Input 2:

`"Java  Programming  is  Fun!"` 

Expected Output 2:

`6` 

##### Solution:



```
int whitespaceCount = 0;
String input = "The quick brown fox jumps over the lazy dog.";
for (int i = 0; i < input.length(); i++) {
    if (Character.isWhitespace(input.charAt(i))) {
        whitespaceCount++;
    }
}
System.out.println(whitespaceCount);
```

#### Exercise 2: Escape Sequence Example

Write a program that uses escape sequences to print the following message exactly as shown below:


`Java is a "programming" language.` 

Use JShell to test your program.

##### Solution:


```
System.out.println("Java is a \"programming\" language.");
```


### Step 11: More On Method Calls


#### Exercise 1: JShell Math Practice

Create a program using JShell that does the following:

1.  Generates a random integer between 1 and 10 inclusive using the Math.random() method.
2.  Prints out the random integer.
3.  Calculates the square root of the random integer using the Math.sqrt() method.
4.  Prints out the square root.

##### Solution:

```
jshell> int randomNum = (int)(Math.random() * 10 + 1)
randomNum ==> 6

jshell> double sqrtNum = Math.sqrt(randomNum)
sqrtNum ==> 2.449489742783178

jshell> System.out.println("Random integer: " + randomNum);
Random integer: 6

jshell> System.out.println("Square root of random integer: " + sqrtNum);
Square root of random integer: 2.449489742783178
```

#### Exercise 2: Max of Three Numbers

Create a program using JShell that finds the maximum of three numbers using the Math.max() method.

1.  Declare three integer variables and assign them values.
2.  Call the Math.max() method with the three variables as parameters.
3.  Print out the result.

##### Solution:

```
jshell> int num1 = 10;
num1 ==> 10

jshell> int num2 = 15;
num2 ==> 15

jshell> int num3 = 8;
num3 ==> 8

jshell> int maxNum = Math.max(Math.max(num1, num2), num3);
maxNum ==> 15

jshell> System.out.println("Maximum of " + num1 + ", " + num2 + ", and " + num3 + " is: " + maxNum);
Maximum of 10, 15, and 8 is: 15
```



### Step 12: More Formatted Output


####  Exercise 1: 
Create a Java program using JShell to print the following multiplication table on the console:

1 * 1 = 1 1 * 2 = 2 1 * 3 = 3 ... 1 * 10 = 10

##### Solution 1:

```
// Using JShell to print multiplication table for 1
for (int i = 1; i <= 10; i++) {
    System.out.printf("1 * %d = %d%n", i, 1 * i);
}
```
Output:

```
1 * 1 = 1
1 * 2 = 2
1 * 3 = 3
1 * 4 = 4
1 * 5 = 5
1 * 6 = 6
1 * 7 = 7
1 * 8 = 8
1 * 9 = 9
1 * 10 = 10
```

Explanation: The for loop iterates from 1 to 10, and for each iteration, it uses the printf method to print the multiplication table for 1. The `%d` format specifier is used to print the value of the loop variable `i`, and `%n` is used to print a newline character.

#### Exercise 2: 
Create a Java program using JShell to print the following output on the console:

3.5 + 2.8 + 1.9 = 8.2

##### Solution 2:

```
// Using JShell to print the sum of three decimal numbers
double a = 3.5;
double b = 2.8;
double c = 1.9;
double sum = a + b + c;
System.out.printf("%.1f + %.1f + %.1f = %.1f%n", a, b, c, sum);
```

Output:

```
3.5 + 2.8 + 1.9 = 8.2
```

Explanation: The program declares three double variables `a`, `b`, and `c`, and initializes them with the values 3.5, 2.8, and 1.9 respectively. It then calculates the sum of these variables and stores it in the `sum` variable. Finally, it uses the printf method to print the output with one decimal point using the `%f` format specifier and the `%.1f` modifier. `%n` is used to print a newline character.


### Step 13: Introducing Variables


#### Exercise 1: Simple Variable Assignment

In this exercise, you will use JShell to create a variable and assign a value to it. You will then modify the value of the variable and print out the new value.

1.  Open up JShell in your command prompt or terminal.
2.  Define an integer variable named "number" and assign it a value of 5.
3.  Print out the value of the "number" variable.
4.  Change the value of the "number" variable to 10.
5.  Print out the new value of the "number" variable.

##### Solution:

1.  Open up JShell in your command prompt or terminal.
    
2.  Define an integer variable named "number" and assign it a value of 5.
    

```
jshell> int number = 5
number ==> 5
```

3.  Print out the value of the "number" variable.

```
jshell> System.out.println(number)
5
```

4.  Change the value of the "number" variable to 10.

```
jshell> number = 10
number ==> 10
```

5.  Print out the new value of the "number" variable.

```
jshell> System.out.println(number)
10
```

#### Exercise 2: Multiplication Table with Variables

In this exercise, you will use JShell to create a multiplication table using variables. You will define a variable "i" and use it to print out the multiplication table for the number 5.

1.  Open up JShell in your command prompt or terminal.
2.  Define an integer variable named "i" and assign it a value of 1.
3.  Print out the multiplication table for the number 5 using the "i" variable.
4.  Change the value of the "i" variable to 2 and print out the corresponding multiplication table.
5.  Repeat step 4 for the values of "i" from 3 to 10.

##### Solution:

1.  Open up JShell in your command prompt or terminal.
    
2.  Define an integer variable named "i" and assign it a value of 1.
    

```
jshell> int i = 1
i ==> 1
```

3.  Print out the multiplication table for the number 5 using the "i" variable.

```
jshell> System.out.printf("%d * %d = %d\n", 5, i, 5*i)
5 * 1 = 5
```

4.  Change the value of the "i" variable to 2 and print out the corresponding multiplication table.

```
jshell> i = 2
i ==> 2
jshell> System.out.printf("%d * %d = %d\n", 5, i, 5*i)
5 * 2 = 10
```

5.  Repeat step 4 for the values of "i" from 3 to 10.

```
jshell> i = 3
i ==> 3
jshell> System.out.printf("%d * %d = %d\n", 5, i, 5*i)
5 * 3 = 15

jshell> i = 4
i ==> 4
jshell> System.out.printf("%d * %d = %d\n", 5, i, 5*i)
5 * 4 = 20

jshell> i = 5
i ==> 5
jshell> System.out.printf("%d * %d = %d\n", 5, i, 5*i)
5 * 5 = 25

jshell> i = 6
i ==> 6
jshell> System.out.printf("%d * %d = %d
```




### Step 14: Programming Exercise PE-03 (With solution)



#### Exercise 1: JShell Basics

1.  Open JShell and declare an integer variable called `myNum` with a value of 10.
2.  Print the value of `myNum`.
3.  Change the value of `myNum` to 15 and print it again.

##### Solution to Exercise 1:

```
jshell> int myNum = 10;
myNum ==> 10
 jshell> System.out.println(myNum);
10
 jshell> myNum = 15;
myNum ==> 15
 jshell> System.out.println(myNum);
15
```

#### Exercise 2: Looping with JShell

1.  Use a for loop to print the numbers from 1 to 10.
2.  Create a new variable called `sum` and initialize it to 0.
3.  Use a for loop to add the numbers from 1 to 10 to `sum`.
4.  Print the value of `sum`.

##### Solution to Exercise 2:

```
jshell> for (int i = 1; i <= 10; i++) {
   ...>     System.out.println(i);
   ...> }
1
2
3
4
5
6
7
8
9
10

jshell> int sum = 0;
sum ==> 0

jshell> for (int i = 1; i <= 10; i++) {
   ...>     sum += i;
   ...> }

jshell> System.out.println(sum);
55
```


### Step 15: Using Variables

#### Java Coding Exercise 1

Write a Java program using JShell to declare an integer variable called "age" and assign it a value of 25. Then, print the value of "age" on the console.

##### Solution:

```
jshell> int age = 25;
age ==> 25

jshell> System.out.println(age);
25
```

#### Java Coding Exercise 2

Write a Java program using JShell to declare two variables, "name" and "age". Assign your name to the variable "name" and your age to the variable "age". Then, print the values of both variables on the console in the following format: "My name is [name] and I am [age] years old."

##### Solution:

```
jshell> String name = "John Doe";
name ==> "John Doe"

jshell> int age = 30;
age ==> 30

jshell> System.out.println("My name is " + name + " and I am " + age + " years old.");
My name is John Doe and I am 30 years old.
```



### Step 16: Variables: Behind-The-Scenes



#### Exercise 1

Create a JShell program that declares three variables of type `int`, initializes the first two variables with integer values, and assigns the sum of the first two variables to the third variable.

##### Solution

```
`// Declare three variables and assign values to the first two variables
jshell> int num1 = 10;
num1 ==> 10
jshell> int num2 = 20;
num2 ==> 20

// Assign the sum of the first two variables to the third variable
jshell> int sum = num1 + num2;
sum ==> 30

// Verify that the third variable has the correct value
jshell> sum
sum ==> 30
```

#### Exercise 2

Create a JShell program that declares two variables of type `double`, initializes the first variable with a double value, and assigns the sum of the first variable and a second double value to the second variable.

##### Solution

```
// Declare two variables of type double and initialize the first variable with a double value
jshell> double num1 = 3.14;
num1 ==> 3.14

// Assign the sum of the first variable and a second double value to the second variable
jshell> double num2 = num1 + 2.0;
num2 ==> 5.14

// Verify that the second variable has the correct value
jshell> num2
num2 ==> 5.14
```



### Step 17: Naming Variables


#### Exercise 1

Create a variable of type `int` in JShell with the following requirements:

1.  The variable name should start with a letter.
2.  The variable name should be in CamelCase.
3.  The variable name should be descriptive.

**Solution:**

```
jshell> int numberOfStudents
numberOfStudents ==> 0
```

#### Exercise 2

Create a variable of type `String` in JShell with the following requirements:

1.  The variable name should contain an underscore.
2.  The variable name should be descriptive.

**Solution:**

```
jshell> String student_name
student_name ==> null
```



### Step 18: Introducing Primitive Types

#### Exercise 1: Using JShell to Perform Arithmetic Operations on Primitive Types

**Problem:**

In this exercise, you will use JShell to perform arithmetic operations on various primitive types in Java. Perform the following operations and observe the results:

1.  Add two `int` values.
2.  Multiply two `float` values.
3.  Divide a `double` value by an `int` value.
4.  Find the remainder when a `long` value is divided by an `int` value.

**Solution:**

Open JShell and execute the following commands:

```
int a = 15;
int b = 25;
int sum = a + b;
System.out.println("The sum of a and b is: " + sum);

float c = 3.5f;
float d = 2.0f;
float product = c * d;
System.out.println("The product of c and d is: " + product);

double e = 30.0;
int f = 4;
double division = e / f;
System.out.println("The result of dividing e by f is: " + division);

long g = 10000000000L;
int h = 7;
long remainder = g % h;
System.out.println("The remainder when g is divided by h is: " + remainder);
```

#### Exercise 2: Comparing Primitive Types in JShell

**Problem:**

In this exercise, you will use JShell to compare various primitive types in Java. Compare the following pairs of values and determine if they are equal:

1.  Two `int` values.
2.  Two `float` values.
3.  Two `double` values.
4.  Two `char` values.

**Solution:**

Open JShell and execute the following commands:

```
int i1 = 42;
int i2 = 42;
boolean intsEqual = (i1 == i2);
System.out.println("Are i1 and i2 equal? " + intsEqual);

float f1 = 3.14f;
float f2 = 3.14f;
boolean floatsEqual = (f1 == f2);
System.out.println("Are f1 and f2 equal? " + floatsEqual);

double d1 = 25.678;
double d2 = 25.678;
boolean doublesEqual = (d1 == d2);
System.out.println("Are d1 and d2 equal? " + doublesEqual);

char c1 = 'A';
char c2 = 'A';
boolean charsEqual = (c1 == c2);
System.out.println("Are c1 and c2 equal? " + charsEqual);
```

These exercises will help you gain hands-on experience with primitive types and their operations in Java using JShell.


### Step 19: Choosing A Data Type


#### Exercise 1: Calculating average temperature

**Problem:**

Write a program in JShell to calculate the average temperature of a week. Store the daily temperatures in an array, and then calculate and display the average temperature.

**Solution:**

```
// Initialize the array with daily temperatures (in Celsius)
double[] dailyTemperatures = {20.5, 22.3, 18.9, 19.6, 21.4, 23.7, 20.1};

// Calculate the sum of temperatures
double sumTemperatures = 0;
for (int i = 0; i < dailyTemperatures.length; i++) {
    sumTemperatures += dailyTemperatures[i];
}

// Calculate the average temperature
double averageTemperature = sumTemperatures / dailyTemperatures.length;

// Display the average temperature
System.out.println("The average temperature for the week is: " + averageTemperature);
```

#### Exercise 2: Determining leap years

**Problem:**

Write a program in JShell to determine if a given year is a leap year or not. A leap year is a year that is exactly divisible by 4, except for years that are exactly divisible by 100. However, years that are exactly divisible by 400 are also considered leap years.

**Solution:**

```
// Define a year to check if it's a leap year
int year = 2024;

// Determine if the year is a leap year
boolean isLeapYear = (year % 4 == 0) && (year % 100 != 0) || (year % 400 == 0);

// Display the result
if (isLeapYear) {
    System.out.println(year + " is a leap year.");
} else {
    System.out.println(year + " is not a leap year.");
}
```




### Step 20: The Assignment Operator =




#### Exercise 1: Increment and Decrement Counter

**Problem**

Write a Java program using JShell to demonstrate the use of increment and decrement operations on a counter variable `counter`. Follow these steps:

1.  Initialize `counter` with 0.
2.  Increment `counter` by 5.
3.  Decrement `counter` by 2.

**Solution**

```
jshell> int counter = 0;
counter ==> 0

jshell> counter = counter + 5;
counter ==> 5

jshell> counter = counter - 2;
counter ==> 3

jshell> counter;
counter ==> 3
```

#### Exercise 2: Calculate the power of a number using increments

**Problem**

Write a Java program using JShell to calculate the power of a number `base` raised to an exponent `exponent`. Do this using increments and a loop.

**Solution**

```
jshell> int base = 2;
base ==> 2

jshell> int exponent = 3;
exponent ==> 3

jshell> int result = 1;
result ==> 1

jshell> for (int i = 0; i < exponent; i++) {
   ...>   result = result * base;
   ...> }
jshell> result;
result ==> 8
```



### Step 21: Assignment Puzzles, and PMT-Challenge revisited



#### Exercise 1: Pre- and Post- Increment and Decrement with JShell

**Problem:**

Using JShell, create a variable called `count` and initialize it with the value `10`. Then, apply pre- and post-increment and pre- and post-decrement operators. Print the value of the `count` variable after each operation to observe the differences.

**Solution:**

```
jshell> int count = 10
count ==> 10

jshell> ++count
$1 ==> 11

jshell> count
count ==> 11

jshell> count++
$2 ==> 11

jshell> count
count ==> 12

jshell> --count
$3 ==> 11

jshell> count
count ==> 11

jshell> count--
$4 ==> 11

jshell> count
count ==> 10
```

#### Exercise 2: Compound Assignment Operators with JShell

**Problem:**

Using JShell, create a variable called `value` and initialize it with the value `8`. Apply various compound assignment operators on `value` and print its value after each operation.

**Solution:**

```
jshell> int value = 8
value ==> 8

jshell> value += 4
$1 ==> 12

jshell> value
value ==> 12

jshell> value -= 2
$2 ==> 10

jshell> value
value ==> 10

jshell> value *= 3
$3 ==> 30

jshell> value
value ==> 30

jshell> value /= 2
$4 ==> 15

jshell> value
value ==> 15

jshell> value %= 4
$5 ==> 3

jshell> value
value ==> 3
```




### Step 22: Some  `JShell`  Usage Tips

#### Exercise 1

#### Problem

Write a short program in JShell to calculate the area of a rectangle using the given length and width. Use JShell internal variables to store the results of your calculations. Finally, print the area of the rectangle.

##### Solution

1.  Open JShell by typing `jshell` in your command prompt or terminal.
2.  Enter the following commands one by one in JShell:

```
int length = 10
int width = 5
int area = length * width
System.out.println("Area of the rectangle: " + area)
```

3.  You should see the output: `Area of the rectangle: 50`

#### Exercise 2

#### Problem

Create a simple program in JShell to add two numbers and print their sum. Then, use JShell shortcuts to modify the previous input and calculate the sum of two different numbers.

##### Solution

1.  Open JShell by typing `jshell` in your command prompt or terminal.
2.  Enter the following commands one by one in JShell:

```
int num1 = 3
int num2 = 7
int sum = num1 + num2
System.out.println("Sum of the numbers: " + sum)
```

3.  You should see the output: `Sum of the numbers: 10`
4.  Now, use the up-arrow key to navigate back to the `int num1 = 3` line and modify the value of `num1`:

```
int num1 = 5
```

5.  Use the up-arrow key again to navigate back to the `int num2 = 7` line and modify the value of `num2`:

```
int num2 = 9
```

6.  Finally, use the up-arrow key to navigate back to the `int sum = num1 + num2` and `System.out.println("Sum of the numbers: " + sum)` lines to re-execute them.
7.  You should now see the output: `Sum of the numbers: 14`




### Step 23: Introducing Conditionals - the if



#### Exercise 1: Check if a Number is Even

**Problem**: Write a Java program using JShell that checks if a given number is even or odd. If the number is even, print "The number is even", otherwise print "The number is odd".

**Solution**:

```
int number = 10;

if (number % 2 == 0) {
    System.out.println("The number is even");
} else {
    System.out.println("The number is odd");
}
``` 

#### Exercise 2: Compare Two Numbers

**Problem**: Write a Java program using JShell that takes two integer values as input and compares them. If the first number is greater than the second number, print "The first number is greater than the second number". 

**Solution**:

```
int num1 = 15;
int num2 = 7;

if (num1 > num2) {
    System.out.println("The first number is greater than the second number");
```




### Step 24: Programming Exercise PE-04

#### Exercise 1: JShell Arithmetic Comparison

In this exercise, you will use JShell to create four integer variables a, b, c, and d, and compare the sums of a + b and c + d.

#### Problem

1.  Start a JShell session.
2.  Declare four integer variables a, b, c, and d, and initialize them with any integer values.
3.  Write an if statement to print if the sum of a and b is greater than the sum of c and d.

##### Solution

```
`// Start JShell
$ jshell

// Declare and initialize four integer variables
jshell> int a = 10;
a ==> 10

jshell> int b = 20;
b ==> 20

jshell> int c = 5;
c ==> 5

jshell> int d = 15;
d ==> 15

// Write an if statement to compare the sums and print the result
jshell> if (a + b > c + d) {
   ...>     System.out.println("The sum of a and b is greater than the sum of c and d.");
   ...> }
The sum of a and b is greater than the sum of c and d.
```

#### Exercise 2: JShell Triangle Angle Check

In this exercise, you will use JShell to check if three given angles can form a triangle.

#### Problem

1.  Start a JShell session if you haven't already.
2.  Declare three integer variables angle1, angle2, and angle3, and initialize them with any integer values.
3.  Write an if statement to check if the sum of angle1, angle2, and angle3 equals 180 degrees. If so, print that the angles can form a triangle; otherwise, print that the angles cannot form a triangle.

##### Solution

```
// Start JShell if not already open
$ jshell

// Declare and initialize three integer variables for the angles
jshell> int angle1 = 60;
angle1 ==> 60

jshell> int angle2 = 60;
angle2 ==> 60

jshell> int angle3 = 60;
angle3 ==> 60

// Write an if statement to check if the angles can form a triangle
jshell> if (angle1 + angle2 + angle3 == 180) {
   ...>     System.out.println("The angles can form a triangle.");
   ...> } else {
   ...>     System.out.println("The angles cannot form a triangle.");
   ...> }
The angles can form a triangle.
```






### Step 26: if Statement again
#### Exercise 1

**Problem Statement:**

Create a JShell script that assigns a value to an integer `x` and checks if `x` is equal to 10. If `x` is equal to 10, print "x is equal to 10" and "x is even". If `x` is not equal to 10, print "x is not equal to 10".

**Solution:**

```
jshell> int x = 10;
jshell> if (x == 10) {
   ...> System.out.println("x is equal to 10");
   ...> System.out.println("x is even");
   ...> } else {
   ...> System.out.println("x is not equal to 10");
   ...> }
   ```

#### Exercise 2

**Problem Statement:**

Create a JShell script that assigns a value to an integer `y` and checks if `y` is greater than 15. If `y` is greater than 15, print "y is greater than 15" and "y is a large number". If `y` is not greater than 15, print "y is not greater than 15".

**Solution:**

```
jshell> int y = 20;
jshell> if (y > 15) {
   ...> System.out.println("y is greater than 15");
   ...> System.out.println("y is a large number");
   ...> } else {
   ...> System.out.println("y is not greater than 15");
   ...> }
```


### Step 27: Introducing Loops: The  `for`  Statement

#### Exercise 1: Printing Even Numbers

**Problem:** Write a Java code snippet in JShell that uses a `for` loop to print the even numbers from 2 to 20.

**Solution:**

```
jshell> for (int i = 2; i <= 20; i += 2) {
...>     System.out.println(i);
...> }
```

**Output:**

```
2
4
6
8
10
12
14
16
18
20
```

#### Exercise 2: Sum of Natural Numbers

**Problem:** Write a Java code snippet in JShell that uses a `for` loop to find the sum of the first 15 natural numbers.

**Solution:**

```
jshell> int sum = 0;
sum ==> 0
jshell> for (int i = 1; i <= 15; i++) {
...>     sum += i;
...> }
jshell> System.out.println("Sum of first 15 natural numbers: " + sum);
```

**Output:**

```
Sum of first 15 natural numbers: 120
```
