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
