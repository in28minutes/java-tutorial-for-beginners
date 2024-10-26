# Missing Info in Lectures From Github Repo

## Section 3: Introduction to Java Programming with Jshell using Multiplication Table

### Step 10 - Printing output to console with Java - Puzzles:

### Whitespace is ignored by the compiler when used around numeric expressions.

```java
	jshell> System.out.println(24 * 60 * 60)
	86400
	jshell> System.out.println(24    *    60    *    60)
	86400
	jshell>
```
---
### Step 14 - Introduction to Variables in Java - Exercises and Puzzles

### Let's consider another example:

```java
	jshell> int number = "Hello World"
	| Error:
	| incompatible types: java.lang.String cannot be converted to int
	| int number = "Hello World"
	|_____________^--------------^
	jshell>
```

- number is an int variable, and we are trying to store a String value "Hello World". Not allowed.

---

### Step 16 - How are variables stored in memory?

### An assignment to a constant literal is not allowed.

```java
	jshell> 20 = var
	| Error:
	| unexpected type
	| required : variable
	| found : value
	| 20 = var
	| ^^

	jshell>
```

---

### Additional Coding Exercises:

### Programming Exercise 1: Multiplication Table for Any Number

Objective: Allow the user to input any number and display its multiplication table from 1 to 10.

#### Instructions:

- Write a program that prompts the user to enter a number.
- Use a loop to display the multiplication table for the entered number from 1 to 10.
- Format the output using System.out.printf() for clean display.

#### Sample Code:

```java
import java.util.Scanner;

public class MultiplicationTable {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Prompt user for input
        System.out.print("Enter a number to display its multiplication table: ");
        int number = scanner.nextInt();
        
        // Display multiplication table for the entered number
        System.out.println("Multiplication Table for " + number + ":");
        for (int i = 1; i <= 10; i++) {
            System.out.printf("%d * %d = %d%n", number, i, number * i);
        }
        
        scanner.close();
    }
}
```

#### Expected Output:

```java
Enter a number to display its multiplication table: 7
Multiplication Table for 7:
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

---

### Programming Exercise 2: Even Numbers Table

Objective: Generate and print the multiplication table for all even numbers between 2 and 10.

#### Instructions:

- Write a program that generates the multiplication table for all even numbers between 2 and 10.
- Use nested loops to calculate and display each table.
- Format the output using System.out.printf() for clean display.

#### Sample Code:

```java
public class EvenMultiplicationTable {
    public static void main(String[] args) {
        System.out.println("Multiplication Tables for Even Numbers (2 to 10):");
        
        // Loop through even numbers from 2 to 10
        for (int number = 2; number <= 10; number += 2) {
            System.out.printf("Multiplication Table for %d:%n", number);
            for (int i = 1; i <= 10; i++) {
                System.out.printf("%d * %d = %d%n", number, i, number * i);
            }
            System.out.println();  // Print a blank line for better readability
        }
    }
}
```

#### Expected Output:

```java
Multiplication Tables for Even Numbers (2 to 10):
Multiplication Table for 2:
2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
2 * 6 = 12
2 * 7 = 14
2 * 8 = 16
2 * 9 = 18
2 * 10 = 20

Multiplication Table for 4:
4 * 1 = 4
4 * 2 = 8
4 * 3 = 12
4 * 4 = 16
4 * 5 = 20
4 * 6 = 24
4 * 7 = 28
4 * 8 = 32
4 * 9 = 36
4 * 10 = 40

... (and so on for 6, 8, and 10)
```

---

## Section 4: Introduction to Java Method with Multiplication Table

### Step 04 - Introduction to Java Methods - Arguments and Parameters

### Snippet-5 : Parameter type mismatch

- Java is a strongly typed language, with strict rules laid out for type compatibility. We saw that with variables, and how they play out with expressions and assignments.

- The same type compatibility rules are enforced by the compiler, when it needs to match the arguments from method calls with method definition.

```java
	jshell> sayHelloWorld("value")
	| Error:
	| incompatible types: java.lang.String cannot be converted to int
	| sayHelloWorld("value")
	|               ^-----^
	jshell> sayHelloWorld(4.5)
	| Error:
	| incompatible types: possibly lossy conversion from double to int
	| sayHelloWorld(4.5)
	|               ^-^
	jshell>
```

---

### Step 06 - Introduction to Java Method Arguments - Puzzles and Tips

#### Overview

In this step, we will learn about **method arguments** in Java. This includes understanding the difference between **parameters** and **arguments**, as well as some common mistakes that beginners often make when working with methods.

Methods are essential in Java programming because they allow us to reuse blocks of code by passing values to them.

Let's explore a few puzzles that will help solidify your understanding of how method arguments work.

### Puzzle 1: What Happens When No Argument is Passed?

Imagine we have a method called `sayHelloWorld` that expects an integer as a parameter. What happens if we don’t pass any argument to the method?

**Scenario**:

```java
sayHelloWorld(); // No argument passed
```

**Result**:

```
Error: actual and formal argument lists differ in length
```

**Explanation**:

- This error occurs because the method definition requires **one argument**.

- If we call the method without any arguments (i.e., an empty pair of parentheses `()`), the program throws an error.

- The error message says that the **actual** number of arguments (0) is different from the **expected** number of arguments (1). 

To fix this error, we need to pass exactly one argument that matches the type expected by the method.

### Puzzle 2: Passing a String Instead of an Integer

What if we try to pass a **string** to the `sayHelloWorld` method that expects an integer? Will that work?

**Scenario**:

```java
sayHelloWorld("Hello"); // Passing a string
```

**Result**:

```
Error: incompatible types
```

**Explanation**:

- The method expects an **integer** (like `4` or `10`), but we are trying to pass a **string** (like `"Hello"`).

- In Java, you cannot pass a value of the wrong type to a method. In this case, the types don't match—an `int` was expected, but a `String` was provided.

- This causes the error. 

To fix it, we need to pass a number that is compatible with the method’s parameter type (i.e., an integer).

### Puzzle 3: Passing a Decimal (Double) Instead of an Integer

What happens if we pass a **decimal number** (also known as a double) instead of an integer?

**Scenario**:

```java
sayHelloWorld(4.5); // Passing a double
```

**Result**:

```
Error: incompatible types
```

**Explanation**:

- Even though `4.5` is a number, it's a **double** (a number with a decimal), not an **integer** (whole number).

- Since the method is designed to accept an integer, passing a double will result in an error.

- Java is strict about matching the types exactly. 

To fix this, we need to pass a whole number (e.g., `4`) that matches the `int` type expected by the method.

### Key Tip: Understanding Parameters vs. Arguments

#### What is a Parameter?

A **parameter** is the name of the variable that appears in the method’s definition. It's like a placeholder. When defining a method, we use parameters to tell the method what kind of data it will accept.

**Example**:

```java
public void sayHelloWorld(int noOfTimes) {
    // noOfTimes is the parameter
}
```

In this example, `noOfTimes` is the parameter that holds the value passed to the method.

#### What is an Argument?

An **argument** is the actual value that we pass to the method when we call it. The argument is what fills in the placeholder defined by the parameter.

When you pass a value to the method, that value becomes the argument.

**Example**:

```java
sayHelloWorld(4); // 4 is the argument
```

In this example, `4` is the argument that we pass to the method.

The method takes the argument and uses it in place of the parameter `noOfTimes`.

#### Example Code:

```java
public void sayHelloWorld(int noOfTimes) {
    for (int i = 0; i < noOfTimes; i++) {
        System.out.println("Hello World");
    }
}

// Method call
sayHelloWorld(4);  // Passing 4 as the argument
```

**Explanation**:

- In the method definition: `int noOfTimes` is the **parameter**.

- When we call the method with `sayHelloWorld(4);`, the value `4` is the **argument**.

In this case, `noOfTimes` takes on the value of the argument (`4`), so the method prints "Hello World" four times.

---

### Additional Coding Exercises:

### Exercise 1: Multiplication Table Generator

**Objective**: Create a method that prints the multiplication table for any number, up to a specified range.

**Explanation**:
In this exercise, you’ll write a method that accepts two arguments:

`number`: The number for which the multiplication table is to be printed.

`range`: The number of rows in the multiplication table (i.e., how far the table goes).

For example, calling `generateMultiplicationTable(7, 12);` would print the multiplication table of 7 up to 12.

#### Code:

```java
public class MultiplicationTable {
    public static void generateMultiplicationTable(int number, int range) {
        for (int i = 1; i <= range; i++) {
            System.out.printf("%d * %d = %d%n", number, i, number * i);
        }
    }

    public static void main(String[] args) {
        generateMultiplicationTable(7, 12);  // Example: prints multiplication table of 7 up to 12
    }
}
```

#### Output:

```java
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
...
7 * 12 = 84
```

This exercise tests your ability to work with loops, method arguments, and formatted output.

---

### Exercise 2: Reusable Print Statements

**Objective**: Create a method that prints a custom message a specific number of times.

**Explanation**:
In this exercise, you’ll write a method that takes two arguments:

`message`: A string message to print.

`times`: The number of times to print the message.

This allows you to reuse the method to print any message, as many times as desired.

#### Code:

```java
public class PrintMessageExample {
    // Method to print a custom message a specific number of times
    public static void printCustomMessage(String message, int times) {
        for (int i = 1; i <= times; i++) {
            System.out.println(message);
        }
    }

    public static void main(String[] args) {
        // Example usage of the method
        printCustomMessage("Java is fun!", 5);  // Prints the message 5 times
    }
}
```

#### Output:

```java
Java is fun!
Java is fun!
Java is fun!
Java is fun!
Java is fun!
```

This exercise reinforces how to use method arguments to allow for flexibility in method behavior, as well as loop control for repeated tasks.

---

## Section 5: Introduction to Java Platform

> No content for this section

---

## Section 6: Introduction to Eclipse - First Java Programming Project

### Additional Coding Exercises:

### **Exercise 1: Creating and Debugging a Java Class in Eclipse**

**Objective**: Practice creating a Java class in Eclipse, running it, and using the Debug mode to examine its behavior.

#### Tasks:

1. **Create a Java class** named `Calculator` with the following methods:

   - `add(int a, int b)`: Returns the sum of `a` and `b`.

   - `subtract(int a, int b)`: Returns the result of `a - b`.
   - `multiply(int a, int b)`: Returns the result of `a * b`.
   - `divide(int a, int b)`: Returns the result of `a / b`. Ensure you handle division by zero.

2. **Add a `main()` method** to the class where you create an instance of `Calculator` and call each of the methods with some example values. Print the results of each operation.

3. **Run the class** using Eclipse’s "Run as --> Java Application" option to see the results in the console.

4. **Set breakpoints** in each of the methods (`add`, `subtract`, `multiply`, `divide`) and debug the program using Eclipse’s Debug mode.

At each breakpoint, inspect the values of the variables and step through the program execution.

#### Code:
```java
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
    
    public int subtract(int a, int b) {
        return a - b;
    }
    
    public int multiply(int a, int b) {
        return a * b;
    }
    
    public int divide(int a, int b) {
        if (b == 0) {
            System.out.println("Error: Division by zero");
            return 0;
        }
        return a / b;
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println("Addition: " + calc.add(10, 5));
        System.out.println("Subtraction: " + calc.subtract(10, 5));
        System.out.println("Multiplication: " + calc.multiply(10, 5));
        System.out.println("Division: " + calc.divide(10, 0));
    }
}
```

#### Expected Outcome:

- Learners will gain hands-on experience creating and running Java classes in Eclipse.

- They will also learn how to set breakpoints, step through code, and inspect variables using Eclipse’s Debug mode.

---

### **Exercise 2: Using Eclipse to Refactor and Organize Code into Packages**

**Objective**: Practice organizing Java classes into packages, using Eclipse's refactoring tools, and running a program with multiple classes.

#### Tasks:

1. **Create a new Java project** in Eclipse and organize your code into packages:

   - Create a package called `math.operations`.

   - Inside `math.operations`, create two classes:
     - `Addition`: A class with a method `add(int a, int b)` that returns the sum of two integers.

     - `Multiplication`: A class with a method `multiply(int a, int b)` that returns the product of two integers.

2. **Create a separate package** called `main` and inside it, create a class named `MathRunner` with the `main()` method.

   - The `MathRunner` class should import the `Addition` and `Multiplication` classes from the `math.operations` package.

   - In the `main()` method, create instances of `Addition` and `Multiplication` and call their methods, printing the results.

3. **Use Eclipse’s Refactoring tools** to rename one of the classes (e.g., rename `Addition` to `Sum`). Ensure the code updates correctly throughout the project.

4. **Run the program** using "Run as --> Java Application" and observe the output.

#### Code:

**Addition.java (in `math.operations`)**:
```java
package math.operations;

public class Addition {
    public int add(int a, int b) {
        return a + b;
    }
}
```

**Multiplication.java (in `math.operations`)**:
```java
package math.operations;

public class Multiplication {
    public int multiply(int a, int b) {
        return a * b;
    }
}
```

**MathRunner.java (in `main`)**:
```java
package main;

import math.operations.Addition;
import math.operations.Multiplication;

public class MathRunner {
    public static void main(String[] args) {
        Addition add = new Addition();
        Multiplication multiply = new Multiplication();
        
        System.out.println("Sum: " + add.add(10, 5));
        System.out.println("Product: " + multiply.multiply(10, 5));
    }
}
```

#### Expected Outcome:

- Learners will practice using packages to organize classes and gain familiarity with Eclipse’s refactoring tools.

- They will also understand how to import classes from different packages and run multi-class programs in Eclipse.

---

## Section 9: Introduction To Java Object Oriented Programming

> No content for this section

---

## Section 11: Primitive Data Types And Alternatives in Java Programming

### Additional Coding Exercises

### **Exercise 1: Number System Converter**

**Objective**: Practice working with different number systems (decimal, octal, and hexadecimal) and integer type conversions in Java.

#### Tasks:

1. **Create a class `NumberSystemConverter`** that has the following functionalities:

   - Convert a decimal number to its binary, octal, and hexadecimal representations.

   - Convert an octal or hexadecimal number (input as a string) back to decimal.
   
2. **Add methods** to the `NumberSystemConverter` class:
   - `toBinary(int number)`: Converts a decimal number to its binary representation.

   - `toOctal(int number)`: Converts a decimal number to its octal representation.

   - `toHexadecimal(int number)`: Converts a decimal number to its hexadecimal representation.

   - `fromOctal(String octal)`: Converts an octal number (as a string) back to decimal.

   - `fromHexadecimal(String hex)`: Converts a hexadecimal number (as a string) back to decimal.
   
3. **Create a `main()` method** to test these methods by converting values between different number systems.

#### Code:

**NumberSystemConverter.java**:

```java
public class NumberSystemConverter {
    public String toBinary(int number) {
        return Integer.toBinaryString(number);
    }

    public String toOctal(int number) {
        return Integer.toOctalString(number);
    }

    public String toHexadecimal(int number) {
        return Integer.toHexString(number);
    }

    public int fromOctal(String octal) {
        return Integer.parseInt(octal, 8);
    }

    public int fromHexadecimal(String hex) {
        return Integer.parseInt(hex, 16);
    }
}
```

**NumberSystemConverterRunner.java**:

```java
public class NumberSystemConverterRunner {
    public static void main(String[] args) {
        NumberSystemConverter converter = new NumberSystemConverter();

        // Decimal to Binary, Octal, Hexadecimal
        int decimal = 255;
        System.out.println("Binary of 255: " + converter.toBinary(decimal));
        System.out.println("Octal of 255: " + converter.toOctal(decimal));
        System.out.println("Hexadecimal of 255: " + converter.toHexadecimal(decimal));

        // Octal and Hexadecimal back to Decimal
        String octal = "377";
        String hex = "FF";
        System.out.println("Octal 377 to Decimal: " + converter.fromOctal(octal));
        System.out.println("Hexadecimal FF to Decimal: " + converter.fromHexadecimal(hex));
    }
}
```

#### Output:

```java
Binary of 255: 11111111
Octal of 255: 377
Hexadecimal of 255: ff
Octal 377 to Decimal: 255
Hexadecimal FF to Decimal: 255
```

**Explanation**:

- The binary representation of 255 is 11111111.

- The octal representation of 255 is 377.

- The hexadecimal representation of 255 is ff.

- The octal number 377 is equivalent to 255 in decimal.

- The hexadecimal number FF is also equivalent to 255 in decimal.

#### Expected Outcome:

- Learners will gain a better understanding of how Java handles different number systems.

- They will practice working with **string parsing** and **integer conversion** functions in Java.
  
---

### **Exercise 2: Simple Interest Calculator Using `BigDecimal`**

**Objective**: Practice handling precise floating-point calculations using `BigDecimal`.

#### Tasks:

1. **Create a class `SimpleInterestCalculator`** that performs a simple interest calculation using `BigDecimal`.

   - The class should accept a principal amount and interest rate as `String` inputs.

   - It should calculate the total value after a given number of years using the formula:  
     `Total Amount = Principal + (Principal * Interest * Number of Years)`
   
2. **Add methods** to the `SimpleInterestCalculator` class:

   - `calculateTotalValue(int years)`: Calculates the total value after the given number of years.

3. **Create a `main()` method** to test the interest calculation with various inputs.

#### Code:

**SimpleInterestCalculator.java**:

```java
import java.math.BigDecimal;

public class SimpleInterestCalculator {
    private BigDecimal principal;
    private BigDecimal interestRate;

    public SimpleInterestCalculator(String principal, String interestRate) {
        this.principal = new BigDecimal(principal);
        this.interestRate = new BigDecimal(interestRate).divide(new BigDecimal("100"));
    }

    public BigDecimal calculateTotalValue(int years) {
        BigDecimal totalInterest = principal.multiply(interestRate).multiply(new BigDecimal(years));
        return principal.add(totalInterest);
    }
}
```

**SimpleInterestCalculatorRunner.java**:

```java
public class SimpleInterestCalculatorRunner {
    public static void main(String[] args) {
        SimpleInterestCalculator calculator = new SimpleInterestCalculator("5000", "5");
        BigDecimal totalValue = calculator.calculateTotalValue(3);
        System.out.println("Total Amount after 3 years: " + totalValue);
    }
}
```

#### Output:

```java
Total Amount after 3 years: 5750.00
```

**Explanation**:

- The principal amount is `5000`.

- The interest rate is 5%, which, over 3 years, results in a total interest of `750` (`5000 * 0.05 * 3`).
Therefore, the total amount after 3 years is `5750`.


#### Expected Outcome:

- Learners will reinforce the use of the `BigDecimal` class for accurate floating-point arithmetic.

- They will explore handling **precise calculations**, which is particularly useful in financial applications.

---

## Section 12: Conditionals in Java Programming

### Step 09: Comparing The if Family, And switch

Let's compare and contrast these two approaches, to gain some experience on how to choose a conditional.

First comes an example using the if-else if-else statement.

#### Snippet-01 : Formatted Output Using if

#### OperatorChoiceRunner.java

```java
	package com.in28minutes.ifstatement.examples;

	public class OperatorChoiceRunner {
		public static void main(String[] args) {
			OperatorChoice opChoice = new OperatorChoice(5, 2, 1);
			opChoice.operate();
		}
	}
```
#### OperatorChoice.java

```java
	package com.in28minutes.ifstatement.examples;

	public class OperatorChoice {
		private int number1;
		private int number2;
		private int choice;
		
		public OperatorChoice(int number1, int number2, int choice) {
			this.number1 = number1;		
			this.number2= number2;
			this.choice = choice;
		}

		public void operate() {
			System.out.printf("number1 : %d", number1).println();
			System.out.printf("number2 : %d", number2).println();
			System.out.printf("choice : %d", choice).println();
			
			if(choice == 1) {
				System.out.printf("result : %d", number1 + number2).println();
			} else if(choice == 2) {
				System.out.printf("result : %d", number1 - number2).println();
			} else if(choice == 3) {
				System.out.printf("result : %d", number1 * number2).println();
			} else if(choice == 4) {
				System.out.printf("result : %d", number1 / number2).println();
			} else {
				System.out.println("Invalid Operation");
			}
		}
	}
```

#### Console Output

```java
number1 : 5

number2 : 2

choice : 1

result : 7
```

Next in line, is an example involving a switch.

#### Snippet-02 : Formatted Output Using switch

#### OperatorChoiceRunner.java

```java
	package com.in28minutes.ifstatement.examples;

	public class OperatorChoiceRunner {
		public static void main(String[] args) {
			OperatorChoice opChoice = new OperatorChoice(5, 2, 1);
			opChoice.operateUsingSwitch();
		}
	}
```

#### OperatorChoice.java

```java

	package com.in28minutes.ifstatement.examples;

	public class OperatorChoice {
		private int number1;
		private int number2;
		private int choice;

		public OperatorChoice(int number1, int number2, int choice) {
			this.number1 = number1;
			this.number2= number2;
			this.choice = choice;
		}

		public void operateUsingSwitch() {
			System.out.printf("number1 : %d", number1).println();
			System.out.printf("number2 : %d", number2).println();
			System.out.printf("choice : %d", choice).println();

			switch(choice) {
				case 1: System.out.printf("result : %d", number1 + number2).println(); 
					break;
				case 2: System.out.printf("result : %d", number1 - number2).println(); 
					break;
				case 3: System.out.printf("result : %d", number1 * number2).println(); 
					break;				
				case 4: System.out.printf("result : %d", number1 / number2).println(); 
					break;
				default: System.out.printf("result : %d", number1 + number2).println(); 
					break;
			}
		}
	}
```

#### Console Output

```java
number1 : 5

number2 : 2

choice : 1

result : 7
```

#### Summary

In this step, we:

- Observed that the same conditional code could be written using an if-family conditional, or the switch.

- Learned that an if family conditional is difficult to get wrong, as the rules for it are very strict. It can be used to evaluate only boolean conditions. But it is verbose, and often less readable.

- Came to know that a switch conditional can be used to check for only integer values. It is very compact, and very readable.

- However, the relative order of case clauses and default are not fixed, and the usage of break is optional. This can lead to subtle errors in your program.

---

### Additional Coding Exercises:

### **Exercise 1: Grade Evaluator Using if-else and switch**

**Objective**: Create a Java program that evaluates a student's grade based on their score and gives feedback using both `if-else` and `switch` statements.

#### Task:

1. Create a class `GradeEvaluator` that performs the following:

   - **If-else version**: Takes an integer input (score between 0 and 100) and prints the corresponding letter grade using `if-else if` logic:

     - 90-100: Grade A

     - 80-89: Grade B

     - 70-79: Grade C

     - 60-69: Grade D

     - 0-59: Grade F

   - **Switch version**: Using integer division, create a `switch` version to achieve the same result. (For example, dividing the score by 10 simplifies the range logic.)

2. Add a method to print feedback for each grade:

   - A: "Excellent work!"

   - B: "Good job!"

   - C: "You passed."

   - D: "Barely passed."

   - F: "Failed. Try again."

#### Code:

**GradeEvaluator.java**:

```java
public class GradeEvaluator {

    // if-else version
    public void evaluateGradeIfElse(int score) {
        if (score >= 90 && score <= 100) {
            System.out.println("Grade A - Excellent work!");
        } else if (score >= 80 && score < 90) {
            System.out.println("Grade B - Good job!");
        } else if (score >= 70 && score < 80) {
            System.out.println("Grade C - You passed.");
        } else if (score >= 60 && score < 70) {
            System.out.println("Grade D - Barely passed.");
        } else if (score >= 0 && score < 60) {
            System.out.println("Grade F - Failed. Try again.");
        } else {
            System.out.println("Invalid score.");
        }
    }

    // switch version
    public void evaluateGradeSwitch(int score) {
        switch (score / 10) {
            case 10:
            case 9:
                System.out.println("Grade A - Excellent work!");
                break;
            case 8:
                System.out.println("Grade B - Good job!");
                break;
            case 7:
                System.out.println("Grade C - You passed.");
                break;
            case 6:
                System.out.println("Grade D - Barely passed.");
                break;
            default:
                System.out.println("Grade F - Failed. Try again.");
        }
    }
}
```

**GradeEvaluatorRunner.java**:

```java
public class GradeEvaluatorRunner {
    public static void main(String[] args) {
        GradeEvaluator evaluator = new GradeEvaluator();

        // Test with different scores
        System.out.println("Using if-else:");
        evaluator.evaluateGradeIfElse(85);

        System.out.println("Using switch:");
        evaluator.evaluateGradeSwitch(72);
    }
}
```

Input (in `GradeEvaluatorRunner.java`):

```java
evaluator.evaluateGradeIfElse(85);
evaluator.evaluateGradeSwitch(72);
```

**Output**:

```java
Using if-else:
Grade B - Good job!

Using switch:
Grade C - You passed.
```

**Explanation**:

- For the if-else evaluation with an input of 85, the output is "Grade B - Good job!" because 85 falls in the 80-89 range, which corresponds to a B grade.

- For the switch evaluation with an input of 72, the output is "Grade C - You passed." because 72 falls in the 70-79 range, which corresponds to a C grade.

#### Expected Outcome:

- Learners will understand how to use both `if-else` and `switch` to handle conditional branching.

- They'll see how range logic can be simplified with integer division for `switch` cases.

---

### **Exercise 2: Tax Bracket Calculator Using Ternary Operator**

**Objective**: Use the ternary operator to calculate and print tax brackets based on income.

#### Task:

1. Create a class `TaxBracketCalculator` that:

   - Takes an integer input representing annual income and calculates the applicable tax rate using the ternary operator.

   - Tax Brackets:

     - Income > 100,000: 30% tax

     - Income between 50,001 and 100,000: 20% tax

     - Income between 30,001 and 50,000: 10% tax

     - Income ≤ 30,000: 5% tax
     
2. Add methods:

   - `calculateTaxRate`: Returns the tax rate as a percentage.

   - `calculateTax`: Returns the total tax amount (income * tax rate).

#### Code:

**TaxBracketCalculator.java**:

```java
public class TaxBracketCalculator {

    // Calculate tax rate using the ternary operator
    public double calculateTaxRate(int income) {
        return (income > 100000) ? 0.30 :
               (income > 50000) ? 0.20 :
               (income > 30000) ? 0.10 : 0.05;
    }

    // Calculate total tax based on income
    public double calculateTax(int income) {
        double taxRate = calculateTaxRate(income);
        return income * taxRate;
    }
}
```

**TaxBracketCalculatorRunner.java**:

```java
public class TaxBracketCalculatorRunner {
    public static void main(String[] args) {
        TaxBracketCalculator calculator = new TaxBracketCalculator();

        int income = 75000;
        double taxRate = calculator.calculateTaxRate(income);
        double tax = calculator.calculateTax(income);

        System.out.println("Income: $" + income);
        System.out.println("Tax Rate: " + (taxRate * 100) + "%");
        System.out.println("Tax Amount: $" + tax);
    }
}
```

#### Input (in `TaxBracketCalculatorRunner.java`):

```java
int income = 75000;
```

#### Output:

```java
Income: $75000
Tax Rate: 20.0%
Tax Amount: $15000.0
```

**Explanation**:

- With an income of $75,000, the program calculates the tax rate as 20%, which applies to incomes between $50,001 and $100,000.

- The tax amount is calculated as 75,000 * 0.20 = 15,000, so the tax to be paid is $15,000.

#### Expected Outcome:

- Learners will explore using the ternary operator for compact conditional logic.

- They'll practice calculating tax rates and amounts based on given inputs.

---

## Section 14: Loops in Java Programming

### Step 02 - Java For Loop - Exercises Overview and First Exercise Prime Numbers

#### Overview

In this step, we are going to explore several exercises that use **for loops** in Java.

We will work with a custom class called `MyNumber` to perform tasks such as checking if a number is **prime**, finding the **sum of numbers up to N**, calculating the **sum of divisors**, and printing a **number triangle**.

### Exercises Overview

Here are the main exercises we will be solving:

1. **Prime Number Check**: Write a method to check whether a number is a prime number.

2. **Sum Up to N**: Write a method to find the sum of all numbers from 1 up to N.

3. **Sum of Divisors**: Write a method to calculate the sum of divisors of a number, excluding 1 and the number itself.

4. **Print a Number Triangle**: Print a right-angled triangle with numbers based on the given input.

### Exercise 1: Checking if a Number is Prime

A **prime number** is a number greater than 1 that is only divisible by 1 and itself. For example:

- **5** is a prime number because it is only divisible by 1 and 5.

- **6** is not prime because it is divisible by 1, 2, 3, and 6.

#### Solution:

We will create a class called `MyNumber`, and inside this class, we will define a method `isPrime()` to determine if a given number is prime. Let's break down the steps:

1. **Class Creation**: 

    - First, we create a new class called `MyNumber`.

    - We define a constructor that accepts a number, and this number is stored as an instance variable.

2. **Method Creation**: 

    - We create a method `isPrime()` that returns a boolean value (`true` if the number is prime, `false` if it is not).

    - The method will check if the number is divisible by any number between 2 and the number minus 1.

    - If the number is divisible by any of these numbers, it is not prime.

#### Code:

```java
// Class definition
public class MyNumber {
    private int number;

    // Constructor to initialize the number
    public MyNumber(int number) {
        this.number = number;
    }

    // Method to check if the number is prime
    public boolean isPrime() {
        // Guard condition for numbers less than 2 (which are not prime)
        if (number < 2) {
            return false;
        }

        // Loop to check divisibility from 2 to number-1
        for (int i = 2; i < number; i++) {
            if (number % i == 0) {
                return false; // If divisible, it is not prime
            }
        }

        return true; // If no divisors, it's prime
    }
}
```

**Explanation**:

- **Constructor**: Initializes the number passed as input.

- `isPrime()` method:

- First, it checks for numbers less than 2, which are not prime.

- Then, it checks divisibility using a for loop from 2 to the number minus 1. If the number is divisible by any value, it returns false (not prime).

- Otherwise, it returns true (prime).

**Guard Condition**:

A Guard Condition is used to handle special cases at the beginning of the method. In this case:

Numbers less than 2 (negative numbers, 0, 1) are not prime, so we return false for them right away.

---

### Step 03 - Java For Loop - Exercise - Sum Upto N Numbers and Sum of Divisors

#### Overview

In this lesson, we will continue working with the `MyNumber` class and implement two new methods:

1. `sumUptoN()`: This method will calculate the sum of all numbers from 1 to N.

2. `sumOfDivisors()`: This method will calculate the sum of divisors of a given number, excluding 1 and the number itself.

Both methods will use the **for loop** to iterate through numbers and perform the required calculations.

### Exercise 1: Sum Up to N

#### Problem Description:

Given a number `N`, the task is to calculate the sum of all integers from `1` to `N`. For example:
- If `N = 6`, the sum would be `1 + 2 + 3 + 4 + 5 + 6 = 21`.

### Solution Approach:

To calculate the sum, we need to iterate through all numbers from 1 to `N` and keep adding them together.

### Code:

```java
public class MyNumber {
    private int number;

    // Constructor to initialize the number
    public MyNumber(int number) {
        this.number = number;
    }

    // Method to calculate sum up to N
    public int sumUptoN() {
        int sum = 0; // Initialize sum to 0

        // Loop from 1 to the number
        for (int i = 1; i <= number; i++) {
            sum = sum + i; // Add the current value of i to sum
        }

        return sum; // Return the final sum
    }
}
```

**Explanation**:

- **Looping through 1 to N**: We start from 1 and go up to number (N). On each iteration, we add the current value (i) to sum.

- **Sum variable**: This variable is initialized to 0 and will store the running total. As we loop through the numbers, we keep adding to sum.


#### Here’s how to use the sumUptoN() method in the main program:

```java
public class MyNumberRunner {
    public static void main(String[] args) {
        MyNumber number = new MyNumber(6); // Creating an instance with the number 6
        int sum = number.sumUptoN(); // Calculating sum up to 6
        System.out.println("Sum up to N: " + sum); // Output: 21
    }
}
```

#### Output:

```java
Sum up to N: 21
```

- For N = 6, the loop goes through 1, 2, 3, 4, 5, 6 and keeps adding these numbers to sum.

- At the end of the loop, the total sum is 21.

### Exercise 2: Sum of Divisors

Given a number N, the task is to calculate the sum of all divisors of N, excluding 1 and the number itself. For example:

If N = 6, its divisors are 1, 2, 3, 6. Excluding 1 and 6, the sum of divisors is 2 + 3 = 5.

If N = 9, its divisors are 1, 3, 9. Excluding 1 and 9, the sum of divisors is 3.

#### Solution Approach:

To calculate the sum of divisors, we need to:

- Loop through all numbers from 2 to N-1.

- Check if each number divides N without a remainder.

- If it does, add it to the sum.

#### Code:

```java
public class MyNumber {
    private int number;

    // Constructor to initialize the number
    public MyNumber(int number) {
        this.number = number;
    }

    // Method to calculate sum of divisors
    public int sumOfDivisors() {
        int sum = 0; // Initialize sum to 0

        // Loop from 2 to number - 1
        for (int i = 2; i < number; i++) {
            if (number % i == 0) { // Check if i is a divisor of number
                sum = sum + i; // Add i to sum if it's a divisor
            }
        }

        return sum; // Return the final sum
    }
}
```

**Explanation**:

- Looping through 2 to N-1: We check every number between 2 and number - 1 to see if it's a divisor of number.

- Checking divisibility: We use the modulus operator % to check if the remainder is zero. If number % i == 0, then i is a divisor.

- Sum of divisors: We only add i to the sum if it's a divisor.

#### Here’s how to use the sumOfDivisors() method in the main program:

```java
public class MyNumberRunner {
    public static void main(String[] args) {
        MyNumber number = new MyNumber(6); // Creating an instance with the number 6
        int sum = number.sumOfDivisors(); // Calculating sum of divisors for 6
        System.out.println("Sum of divisors: " + sum); // Output: 5

        number = new MyNumber(9); // Creating an instance with the number 9
        sum = number.sumOfDivisors(); // Calculating sum of divisors for 9
        System.out.println("Sum of divisors: " + sum); // Output: 3
    }
}
```

#### Output:

```java
Sum of divisors: 5
Sum of divisors: 3
```

- For N = 6, the divisors are 1, 2, 3, 6. Excluding 1 and 6, the remaining divisors are 2 and 3. Their sum is 5.

- For N = 9, the divisors are 1, 3, 9. Excluding 1 and 9, the only remaining divisor is 3. So, the sum is 3.

---

### Step 04 - Java For Loop - Exercise - Print a Number Triangle

#### Overview

In this exercise, we will focus on printing a **number triangle** using **nested loops** in Java.

The goal is to print a triangle pattern where each row contains increasing numbers up to the input value.

This exercise demonstrates how to use a **for loop** inside another **for loop** (loop within a loop) to achieve this triangular pattern.

#### Problem Description:

Given an input `N`, we need to print a **number triangle** where:

- The first row contains the number `1`.

- The second row contains the numbers `1 2`.

- The third row contains `1 2 3`, and so on, until the last row contains numbers from `1` to `N`.

#### Solution Approach:

To print this triangle, we will use **two for loops**:

1. The outer loop controls the rows (i.e., how many lines we print).

2. The inner loop prints the numbers in each row, from 1 up to the current row number.

### Code:

```java
public class MyNumber {
    private int number;

    // Constructor to initialize the number
    public MyNumber(int number) {
        this.number = number;
    }

    // Method to print a number triangle
    public void printANumberTriangle() {
        // Outer loop to control the number of rows
        for (int i = 1; i <= number; i++) {
            // Inner loop to print numbers for each row
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " "); // Print number with a space
            }
            System.out.println(); // Print a new line after each row
        }
    }
}
```

**Explanation**:

- Outer loop (i loop): This loop runs from 1 to number (i.e., the total number of rows). It controls the number of rows to be printed.

- Inner loop (j loop): For each row i, this loop runs from 1 to i. It prints numbers from 1 up to the current value of i.

- `System.out.print()`: This is used to print numbers on the same line with a space.

- `System.out.println()`: This adds a new line after each row, so that the next set of numbers starts on the next line.

#### Here’s how to use the `printANumberTriangle()` method in the main program:

```java
public class MyNumberRunner {
    public static void main(String[] args) {
        MyNumber number = new MyNumber(5); // Create an instance with the number 5
        number.printANumberTriangle(); // Print the number triangle
    }
}
```

**Output**:

```java
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```

- For N = 5, the outer loop runs 5 times, once for each row.
For each iteration of the outer loop, the inner loop prints numbers from 1 up to the current row number (i).

- After printing each row, `System.out.println()` is used to move to the next line.

---

### Step 05 - While Loop in Java - An Introduction

#### Overview

In this lesson, we will explore the **while loop** in Java, a type of loop that executes a block of code repeatedly as long as a specified condition is true.

We will cover the syntax of the while loop, compare it to the **if statement**, and highlight some common mistakes like infinite loops.

By the end, you'll understand how the while loop works and its differences from other loops like the for loop.

### What is a While Loop?

- The **while loop** is a control flow statement that allows you to repeat a block of code as long as the condition is true.

- It is similar to the `if` statement in its syntax, but unlike `if`, which executes the block only once, the while loop will execute the block repeatedly until the condition becomes false.

### Syntax of the While Loop:

```java
while (condition) {
    // Code to be executed while the condition is true
}
```

- The condition is evaluated before each iteration of the loop.

- If the condition is true, the block of code inside the loop is executed.

- If the condition is false, the loop stops.

**Problem**:

We want to print the numbers from 0 to 4 using a while loop.

#### Code:

```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int i = 0; // Initialize i

        // While loop: repeat as long as i is less than 5
        while (i < 5) {
            System.out.println(i); // Print the current value of i
            i++; // Increment i after each loop iteration
        }
    }
}
```

**Explanation**:

- The variable i is initialized to 0.

- The condition (i < 5) is checked before each iteration. As long as i is less than 5, the loop will continue.

- Inside the loop, System.out.println(i) prints the current value of i.

- After each iteration, i is incremented by 1 using i++.

- The loop will stop once i reaches 5.

**Output**:

```java
0
1
2
3
4
```

### Key Difference Between if and while

The syntax of the while loop looks similar to an if statement, but the key difference is that:

An if statement runs the code only once if the condition is true.

A while loop runs the code multiple times as long as the condition remains true.

**Example comparison**:

```java
int i = 0;

// If statement
if (i < 5) {
    System.out.println("i is less than 5"); // Runs only once if condition is true
}

// While loop
while (i < 5) {
    System.out.println(i); // Runs multiple times while i is less than 5
    i++; // Increment i
}
```

### Common Mistakes - What is an Infinite Loop?

- An infinite loop occurs when the condition in a while loop never becomes false.

- This can happen if we forget to modify the condition within the loop. For example, if we forget to increment the value of i, the loop will continue forever because i will never reach the limit that makes the condition false.

#### Example of an Infinite Loop:

```java
int i = 0;

// Infinite loop: i is never incremented, so the condition is always true
while (i < 5) {
    System.out.println(i);
    // i++ is missing, so i never changes
}
```

- In this case, the loop will print 0 infinitely because the condition i < 5 is always true, and i never gets incremented.

- To stop the loop, we would need to add i++ inside the loop to ensure that i eventually reaches 5 and the condition becomes false.

### Problem:

What happens if the initial value of i is set to a value greater than or equal to the loop condition?

#### Code:

```java
int i = 6; // Initialize i to 6

while (i < 5) {
    System.out.println(i);
    i++; // This will not be executed
}
```

**Explanation**:

- Here, the initial value of i is 6, and the condition is (i < 5).

- Since the condition is false at the start, the loop will not run at all.

- No output will be produced.

**Output**:

```java
(nothing is printed)
```

#### Example: Starting with a Negative Value

### Problem:

If we start with a negative value for i, how does the while loop behave?

#### Code:

```java
int i = -2;

while (i < 5) {
    System.out.println(i);
    i++; // Increment i
}
```

**Explanation**:

- The variable i starts at -2.

- The condition (i < 5) is true initially, so the loop begins and continues until i reaches 5.

- During each iteration, the current value of i is printed, and then i is incremented.

**Output**:

```java
-2
-1
0
1
2
3
4
```

Make sure to increment the value of i (or modify the condition in some way) inside the loop to prevent infinite loops.

---

### Step 06 - While Loop - Exercises - Cubes and Squares upto limit

#### Overview

In this lesson, we will explore two exercises using the **while loop**:

1. Printing the **squares** of numbers up to a specified limit.

2. Printing the **cubes** of numbers up to a specified limit.

We will use the **while loop** in scenarios where we don't know in advance how many iterations we need. The loop will continue running until the square or cube of the number exceeds the limit.

### Problem 1: Print Squares Up to a Limit

#### Problem Description:

We want to print the squares of numbers starting from 1, but only as long as the square is less than the given **limit**.

For example:

- If the limit is `30`, the output should be: `1, 4, 9, 16, 25` (since 36 exceeds the limit).

#### Solution Approach:

We will use a **while loop** to iterate through the numbers, calculate their squares, and print the square only if it is less than the limit.

#### Code:

```java
public class WhileNumberPlayer {
    private int limit;

    // Constructor to initialize the limit
    public WhileNumberPlayer(int limit) {
        this.limit = limit;
    }

    // Method to print squares up to the limit
    public void printSquaresUptoLimit() {
        int i = 1; // Initialize i to 1

        // While loop: Repeat as long as i * i is less than the limit
        while (i * i < limit) {
            System.out.print(i * i + " "); // Print the square of i
            i++; // Increment i after each iteration
        }
        System.out.println(); // Move to the next line after printing all squares
    }
}
```

**Explanation**:

- **Constructor**: The limit is passed when creating an instance of WhileNumberPlayer.

- `printSquaresUptoLimit()` method:
We initialize i to 1 and start a while loop that continues as long as i * i (the square of i) is less than the limit.

- Inside the loop, we print the square of i and increment i by 1.

- The loop stops when the square of i exceeds the limit.

```java
public class WhileNumberPlayerRunner {
    public static void main(String[] args) {
        WhileNumberPlayer player = new WhileNumberPlayer(30); // Limit is 30
        player.printSquaresUptoLimit(); // Output squares up to 30
    }
}
```

**Output**:

```java
1 4 9 16 25
```

### Problem 2: Print Cubes Up to a Limit

#### Problem Description:

We want to print the cubes of numbers starting from 1, but only as long as the cube is less than the given limit. For example:

If the limit is 90, the output should be: 1, 8, 27, 64 (since 125 exceeds the limit).

#### Solution Approach:

We will use a similar approach as the squares exercise, but this time, we will calculate the cubes of the numbers and stop when the cube exceeds the limit.

#### Code:

```java
public class WhileNumberPlayer {
    private int limit;

    // Constructor to initialize the limit
    public WhileNumberPlayer(int limit) {
        this.limit = limit;
    }

    // Method to print cubes up to the limit
    public void printCubesUptoLimit() {
        int i = 1; // Initialize i to 1

        // While loop: Repeat as long as i * i * i is less than the limit
        while (i * i * i < limit) {
            System.out.print(i * i * i + " "); // Print the cube of i
            i++; // Increment i after each iteration
        }
        System.out.println(); // Move to the next line after printing all cubes
    }
}
```

**Explanation**:

- `printCubesUptoLimit()` method:
We initialize i to 1 and start a while loop that continues as long as i * i * i (the cube of i) is less than the limit.

- Inside the loop, we print the cube of i and increment i by 1.

- The loop stops when the cube of i exceeds the limit.

```java
public class WhileNumberPlayerRunner {
    public static void main(String[] args) {
        WhileNumberPlayer player = new WhileNumberPlayer(90); // Limit is 90
        player.printCubesUptoLimit(); // Output cubes up to 90
    }
}
```

#### Output:

```java
1 8 27 64
```

---

### Step 07 - Do While Loop in Java - An Introduction

In this lecture, we will explore the **do-while loop** in Java.

In the previous lesson, we discussed the **while loop**, which executes as long as a condition is true.

Now, we will learn about the do-while loop, its syntax, and when to use it.

### Syntax of a Do-While Loop

The syntax of a do-while loop is very similar to the while loop. However, the key difference is the placement of the condition check.

In a **do-while loop**, the condition is checked at the end of the loop rather than at the beginning.

#### Example:

```java
int i = 1; // Initialize i with value 1
do {
    System.out.println(i); // Print the value of i
    i++; // Increment i by 1
} while (i < 5); // Condition check after the loop body
```

- In this example, the loop will print numbers from **1** to **4**. When `i` becomes **5**, the condition `(i < 5)` will fail, and the loop will stop.

#### Output:

```java
1
2
3
4
```

### Difference Between `while` and `do-while` Loops

- In a **while loop**, the condition is checked **before** the execution of the loop body.

- In a **do-while loop**, the condition is checked **after** the execution of the loop body, which guarantees that the code inside the loop is executed **at least once**, even if the condition is false.

#### Example with a While Loop:

```java
int i = 10;
while (i < 5) {
    System.out.println(i); // This code will never execute
    i++;
}
```

- In this case, since the initial value of `i` is **10** (which is greater than 5), the condition `(i < 5)` is false from the start, so the loop body is **never executed**.

#### Output:

```
(no output)
```

#### Example with a Do-While Loop:

```java
int i = 10;
do {
    System.out.println(i); // This code will execute once
    i++;
} while (i < 5);
```

- In this case, even though `i = 10` (which is greater than 5), the **do-while loop** will still execute **once** because the condition is checked **after** the loop body.

#### Output:

```
10
```

### When to Use a Do-While Loop

You should use a **do-while loop** in situations where you want the code inside the loop to be executed at least once, regardless of whether the condition is true or not.

For all other cases, where you only want to execute the loop based on the condition, a **while loop** is recommended.

---

### Step 08 - Do While Loop in Java - An Example - Cube while user enters positive numbers

In this lecture, we will implement an example using the **do-while loop** to repeatedly ask the user for a number, compute its cube, and stop when the user enters a negative number.

### Problem Statement

We want to design a program that performs the following steps:

1. Ask the user to enter a number.

2. Print the cube of the number.

3. Repeat steps 1 and 2 until the user enters a negative number.

4. When a negative number is entered, print a farewell message and exit the loop.

#### Example Interaction:

```java
Enter a number: 5
Cube is 125
Enter a number: 3
Cube is 27
Enter a number: -1
Thank you! Have Fun!
```

### Solution Implementation

The solution is implemented using a **do-while loop** to ensure that the program asks for a number at least once, even if the user enters a negative number at the beginning.

#### Code:

```java
import java.util.Scanner;

public class DoWhileRepeatedQuestionRunner {
    public static void main(String[] args) {
        // Create a scanner object to read input
        Scanner scanner = new Scanner(System.in);

        // Variable to store the number entered by the user
        int number = 0;

        // Do-while loop to repeatedly ask for a number and print its cube
        do {
            System.out.print("Enter a number: ");  // Prompt the user for input
            number = scanner.nextInt();  // Read the number

            if (number >= 0) {
                // Print the cube of the number if it's non-negative
                System.out.println("Cube is " + (number * number * number));
            }
        } while (number >= 0);  // Continue the loop as long as the number is non-negative

        // Print a farewell message when the loop ends
        System.out.println("Thank you! Have Fun!");
    }
}
```

### Explanation:

1. **Scanner Class**: We use the `Scanner` class to read input from the user.

    - `Scanner scanner = new Scanner(System.in);`

    - This creates a scanner object that reads input from the console.

2. **Loop Logic**: 

    - The program starts by asking the user to enter a number using `System.out.print("Enter a number: ")`.

    - The entered number is then stored in the `number` variable using `number = scanner.nextInt();`.

    - If the number is non-negative, the cube of the number is calculated and printed using `System.out.println("Cube is " + (number * number * number));`.

    - The **do-while loop** ensures that the prompt and cube calculation occur at least once, even if the user enters a negative number immediately.
    
3. **Loop Termination**:

    - The loop continues until the user enters a negative number, at which point the loop ends, and the program prints the message `"Thank you! Have Fun!"`.

#### Output Example

#### Scenario 1 - User Enters Positive Numbers:

```java
Enter a number: 12
Cube is 1728
Enter a number: 6
Cube is 216
Enter a number: 2
Cube is 8
Enter a number: -1
Thank you! Have Fun!
```

#### Scenario 2 - User Enters Zero:

```java
Enter a number: 0
Cube is 0
Enter a number: -1
Thank you! Have Fun!
```

### Key Points

- The **do-while loop** is used because we need to ensure that the prompt for input is displayed at least once.

- We use the `Scanner` class to handle user input from the console.

- The loop continues as long as the user enters a non-negative number. Once a negative number is entered, the program terminates with a farewell message.

---

### Step 09 - Introduction to Break and Continue

In this lecture, we are introduced to two important statements used in loops: **`break`** and **`continue`**.

These statements allow you to control the flow of loops in a precise manner, either by breaking out of the loop entirely or skipping certain iterations.

### The `break` Statement

The **`break`** statement is used to exit a loop prematurely. When a `break` statement is encountered, the loop stops executing, and the control is transferred to the statement following the loop.

### Example 1 - Using `break` in a `for` Loop

```java
for (int i = 1; i <= 10; i++) {
    if (i == 5) break;
    System.out.print(i + " ");  // Print numbers in a single line with space
}
```

#### Output:

```java
1 2 3 4
```

- In this example, the loop starts printing numbers from **1**.

- When `i` becomes **5**, the condition `if (i == 5)` is met, and the `break` statement is executed.

- The loop exits, and the numbers **5** to **10** are not printed.

### The `continue` Statement

The **`continue`** statement skips the rest of the current loop iteration and moves to the next iteration.

Unlike `break`, it doesn't exit the loop but skips the code that comes after it for the current iteration.

### Example 2 - Using `continue` in a `for` Loop

```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) continue;
    System.out.print(i + " ");
}
```

#### Output:

```java
1 3 5 7 9
```

- In this example, the loop prints only odd numbers.

- The condition `if (i % 2 == 0)` checks if `i` is even. If the condition is true, the `continue` statement is executed, and the current iteration is skipped.

- As a result, even numbers **2, 4, 6, 8, 10** are skipped, and only the odd numbers are printed.

### Differences Between `break` and `continue`

- **`break`**: When a `break` is executed, it **completely exits** the loop, and the control is passed to the next statement outside the loop.

- **`continue`**: When a `continue` is executed, it **skips the rest of the current iteration** and moves on to the next iteration of the loop.

### Exercise - Printing Even Numbers

Let's create a program to print only the even numbers from 1 to 10 using the `continue` statement.

### Example 3 - Printing Even Numbers with `continue`

```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 != 0) continue;  // Skip odd numbers
    System.out.print(i + " ");
}
```

#### Output:

```java
2 4 6 8 10
```

- The condition `if (i % 2 != 0)` checks if `i` is odd. If it is, the `continue` statement is executed, skipping the odd numbers.

- Only the even numbers **2, 4, 6, 8, 10** are printed.

While **`break`** and **`continue`** can be useful, they can also make loops harder to understand.

It is generally a good idea to minimize their use in loops unless absolutely necessary, as they can introduce complexity in program flow.

---

### Step 10 - Selecting Loop in Java - For vs While vs Do While

In this lecture, we review how to select the right loop to use in Java. We have learned about three types of loops: **For**, **While**, and **Do While**.

The decision of which loop to use depends on the situation and the problem being solved.

This lecture covers how to choose between these loops based on specific conditions.

### Key Considerations for Selecting a Loop

### 1. Do You Know How Many Times the Loop Will Run?

- If you know the exact number of times the loop should execute, such as `i` times or `n/2` times, the **For loop** is the best choice.
  
  **Example**: 

  ```java
  for (int i = 0; i < 5; i++) {
      System.out.println(i);
  }
  ```

- In many situations, you may **not** know how many times the loop will run. For example, if you're processing user input until a specific condition is met (e.g., user enters a negative number), you should use a **While** or **Do While** loop.

### 2. Should the Code in the Loop Be Executed at Least Once?

- If you need to ensure that the code in the loop executes **at least once**, regardless of whether the condition is true initially, you should use a **Do While** loop.

  **Example**: 

  ```java
  int number;
  do {
      System.out.println("Enter a number:");
      number = scanner.nextInt();
  } while (number >= 0);
  ```

- If the condition should be checked before the loop executes, you should use a **While loop**.

  **Example**: 

  ```java
  int number = 1;
  while (number >= 0) {
      System.out.println("Enter a number:");
      number = scanner.nextInt();
  }
  ```

### Example Scenario: Menu-Driven Program

Consider a scenario where we have a menu that allows the user to enter two numbers and perform operations like addition, subtraction, multiplication, etc.

In the previous section, the program exited after one operation.

However, if we want to keep showing the menu until the user selects an "Exit" option, which loop should we use?

#### **Choosing the Right Loop**:

1. **Do we know how many times the operations will be executed at the start?**
   - **No**. The number of operations is unknown, so the **For loop** is excluded.

2. **Should the code in the loop be executed at least once?**
   - **Yes**. We want the user to see the menu at least once. Therefore, the best choice is the **Do While loop**.

### Example Code for Menu Loop:

```java
int choice;
do {
    System.out.println("Menu:");
    System.out.println("1. Add");
    System.out.println("2. Subtract");
    System.out.println("3. Multiply");
    System.out.println("4. Divide");
    System.out.println("5. Exit");
    System.out.print("Enter your choice: ");
    choice = scanner.nextInt();

    // Perform operations based on the user's choice
    switch (choice) {
        case 1:
            // Add numbers
            break;
        case 2:
            // Subtract numbers
            break;
        case 3:
            // Multiply numbers
            break;
        case 4:
            // Divide numbers
            break;
        case 5:
            System.out.println("Exiting the program.");
            break;
        default:
            System.out.println("Invalid choice, please try again.");
    }
} while (choice != 5);
```

- In this scenario, we use a **Do While** loop to ensure that the menu is displayed at least once, and the loop continues to execute until the user chooses to exit (i.e., selects option **5**).

---

### Additional Coding Exercises:

### Exercise 1: Calculating the Sum of Even Numbers
**Objective:** Write a Java program that uses a `for` loop to calculate the sum of all even numbers from 1 to a given number `n`.

**Task:**
1. Create a class called `SumOfEvenNumbers`.

2. Implement a method `calculateEvenSum(int n)` that:
   - Takes an integer `n` as input.
   - Iterates through all numbers from 1 to `n` using a `for` loop.
   - Checks if each number is even (`number % 2 == 0`).
   - If the number is even, add it to the `sum` variable.

3. Print the total sum after the loop completes.

**Code:**

```java
public class SumOfEvenNumbers {
    public void calculateEvenSum(int n) {
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                sum += i;
            }
        }
        System.out.println("The sum of even numbers from 1 to " + n + " is: " + sum);
    }
}

public class SumOfEvenNumbersRunner {
    public static void main(String[] args) {
        SumOfEvenNumbers calculator = new SumOfEvenNumbers();
        calculator.calculateEvenSum(10); // Test with n = 10
    }
}
```

**Output:**

```java
The sum of even numbers from 1 to 10 is: 30
```

**Explanation:**
- The program calculates the sum of even numbers from 1 to 10. It checks if each number is even using `i % 2 == 0` and adds it to the sum.

- By the end of the loop, the sum of even numbers (2, 4, 6, 8, 10) is `30`.

### Exercise 2: Displaying Multiplication Table
**Objective:** Write a Java program that displays the multiplication table of a number using a `while` loop.

**Task:**
1. Create a class called `MultiplicationTable`.

2. Implement a method `printTable(int number)` that:
   - Takes an integer `number` as input.
   - Uses a `while` loop to print the multiplication table for the given number from `1` to `10`.

3. Ensure that each line displays the result of multiplying the input number by values from 1 to 10.

**Code:**

```java
public class MultiplicationTable {
    public void printTable(int number) {
        int i = 1;
        while (i <= 10) {
            System.out.println(number + " x " + i + " = " + (number * i));
            i++;
        }
    }
}

public class MultiplicationTableRunner {
    public static void main(String[] args) {
        MultiplicationTable table = new MultiplicationTable();
        table.printTable(5); // Test with number = 5
    }
}
```

**Output:**

```java
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

**Explanation:**
- The program uses a `while` loop to print the multiplication table for the number `5`. It starts with `i = 1` and continues until `i` reaches `10`.

- It prints each line in the format `"number x i = result"`, incrementing `i` in each iteration.

---

## Section 16: Reference Types in Java Programming

### Step 14 - Java Reference Types - Conclusion

In this section, we explored the concept of **reference types** in Java and how they differ from **primitive types**.

This was an in-depth look at reference variables, memory storage, initialization, and how assignment and equality work with them.

We also discussed built-in reference types in Java, focusing specifically on the **String class**, its alternatives, and **wrapper classes**.

### 1. Difference Between Reference and Primitive Types

- **Primitive Types**: Simple data types such as `int`, `char`, `boolean`, etc.

- **Reference Types**: Objects that refer to memory addresses where the data is stored, such as instances of classes (e.g., `String`, `Array`).

### 2. Built-in Reference Types in Java

#### a. The **String Class**

- **String** is a commonly used reference type in Java. We examined how strings are stored in memory and the way they behave in terms of assignment and equality.
  
#### b. **StringBuilder** and **StringBuffer**

- These two classes provide alternatives to `String` when mutable strings are needed. We discussed:

  - **StringBuilder**: Faster but not thread-safe.

  - **StringBuffer**: Thread-safe but slower due to synchronization.

### 3. Wrapper Classes

Java has **eight wrapper classes**, each corresponding to one of the eight primitive types:

- **Byte**, **Short**, **Integer**, **Long**
- **Float**, **Double**
- **Character**
- **Boolean**

#### Why Wrapper Classes?
- Wrapper classes allow primitives to be used in contexts that require objects, such as collections (`ArrayList`, `HashMap`).
- They provide utility methods, like converting between strings and numbers.

### 4. Date and Time API: `LocalDate`, `LocalDateTime`, and `LocalTime`
- Java’s new date and time API provides methods to manipulate date and time easily.
  
#### Example Methods:

- **LocalDate**: Retrieve and manipulate dates.
  
  ```java
  LocalDate today = LocalDate.now();
  LocalDate futureDate = today.plusDays(10);
  ```

- **LocalDateTime**: Combine date and time.

  ```java
  LocalDateTime dateTime = LocalDateTime.now();
  ```

- **LocalTime**: Manipulate only the time part of the date.

  ```java
  LocalTime time = LocalTime.now();
  ```

#### Common Methods:
- **Leap year check**: `isLeapYear()`
- **Length of month/year**: `lengthOfMonth()`, `lengthOfYear()`
- **Add/Subtract time**: `plusDays()`, `minusMonths()`

### Importance of Exploring APIs

This section also highlighted the importance of **exploring built-in APIs** in Java.

Although it may seem tedious at times, understanding what is available allows you to effectively use Java's powerful libraries.

Knowing which methods exist in APIs like `String`, `Wrapper Classes`, and `LocalDate` helps in building efficient programs.

### Additional Coding Exercises:

### Exercise 1: Wrapper Class Conversion

**Objective:** Understand and demonstrate the use of Java wrapper classes by converting primitive types to their corresponding wrapper classes and performing operations on them.

**Instructions:**

1. **Declare Primitive Variables:** Start by declaring three primitive variables: an `int`, a `double`, and a `boolean`.

2. **Convert to Wrapper Classes:** Use the appropriate wrapper classes (`Integer`, `Double`, and `Boolean`) to convert these primitive variables.
3. **Print Wrapper Values:** Print the values of the wrapper objects to see how they represent the primitive values.
4. **Convert Back to Primitive Types:** Demonstrate the conversion back to primitive types using the methods `intValue()`, `doubleValue()`, and `booleanValue()`.
5. **Print Results:** Finally, print the results after converting back to the primitive types.

**Code:**

```java
public class WrapperClassExample {
    public static void main(String[] args) {
        // Step 1: Declare primitive variables
        int primitiveInt = 25; // Integer primitive
        double primitiveDouble = 10.5; // Double primitive
        boolean primitiveBoolean = true; // Boolean primitive

        // Step 2: Convert to wrapper classes
        Integer wrapperInt = Integer.valueOf(primitiveInt); // Wrapper for Integer
        Double wrapperDouble = Double.valueOf(primitiveDouble); // Wrapper for Double
        Boolean wrapperBoolean = Boolean.valueOf(primitiveBoolean); // Wrapper for Boolean

        // Step 3: Print wrapper values
        System.out.println("Primitive int value: " + primitiveInt); // Output: 25
        System.out.println("Wrapper Integer value: " + wrapperInt); // Output: 25
        System.out.println("Converted back to primitive: " + wrapperInt.intValue()); // Output: 25

        System.out.println("Primitive double value: " + primitiveDouble); // Output: 10.5
        System.out.println("Wrapper Double value: " + wrapperDouble); // Output: 10.5
        System.out.println("Converted back to primitive: " + wrapperDouble.doubleValue()); // Output: 10.5

        System.out.println("Primitive boolean value: " + primitiveBoolean); // Output: true
        System.out.println("Wrapper Boolean value: " + wrapperBoolean); // Output: true
        System.out.println("Converted back to primitive: " + wrapperBoolean.booleanValue()); // Output: true
    }
}
```

**Sample Output:**

```java
Primitive int value: 25
Wrapper Integer value: 25
Converted back to primitive: 25

Primitive double value: 10.5
Wrapper Double value: 10.5
Converted back to primitive: 10.5

Primitive boolean value: true
Wrapper Boolean value: true
Converted back to primitive: true
```

**Explanation:**

- **Primitive Types:** Java has primitive types such as `int`, `double`, and `boolean`. These types store simple values.

- **Wrapper Classes:** Each primitive type has a corresponding wrapper class (e.g., `Integer` for `int`, `Double` for `double`, and `Boolean` for `boolean`). These classes allow us to treat primitive types as objects.
- **Conversion:** We can convert a primitive type to its corresponding wrapper class using the `valueOf()` method. Similarly, we can convert a wrapper class back to a primitive type using methods like `intValue()`, `doubleValue()`, and `booleanValue()`.

### Exercise 2: Date Manipulation

**Objective:** Use the Java Date API to manipulate dates, check for leap years, and understand how to work with date objects.

**Instructions:**

1. **Get the Current Date:** Use `LocalDate.now()` to retrieve the current date.

2. **Print the Current Date:** Output the current date to the console.
3. **Add Days to the Current Date:** Use the `plusDays()` method to add 30 days to the current date and print the new date.
4. **Check for Leap Year:** Use the `isLeapYear()` method to determine if the current year is a leap year and print the result.
5. **Get Length of the Current Month:** Use the `lengthOfMonth()` method to find the number of days in the current month and print this value.

**Code:**

```java
import java.time.LocalDate;

public class DateManipulationExample {
    public static void main(String[] args) {
        // Step 1: Get the current date
        LocalDate currentDate = LocalDate.now();
        System.out.println("Current Date: " + currentDate); // Output: e.g., 2023-10-17

        // Step 2: Add 30 days
        LocalDate newDate = currentDate.plusDays(30);
        System.out.println("Date after adding 30 days: " + newDate); // Output: e.g., 2023-11-16

        // Step 3: Check if the current year is a leap year
        boolean isLeapYear = currentDate.isLeapYear();
        System.out.println("Is this year a leap year? " + isLeapYear); // Output: true or false

        // Step 4: Get the length of the current month
        int lengthOfMonth = currentDate.lengthOfMonth();
        System.out.println("Length of the current month: " + lengthOfMonth); // Output: 31 (for October)
    }
}
```

**Sample Output:**

```java
Current Date: 2023-10-17
Date after adding 30 days: 2023-11-16
Is this year a leap year? false
Length of the current month: 31
```

**Explanation:**

- **LocalDate Class:** The `LocalDate` class represents a date without time-zone information. It is part of the `java.time` package introduced in Java 8.

- **Current Date:** We retrieve the current date using `LocalDate.now()`, which provides an easy way to get today's date.
- **Date Manipulation:** The `plusDays()` method allows us to add a specified number of days to a date.
- **Leap Year Check:** The `isLeapYear()` method helps determine if the current year has 366 days instead of the usual 365.
- **Length of Month:** The `lengthOfMonth()` method returns the number of days in the month of the date, which is useful for calendar calculations.

---

## Section 18: Arrays and ArrayLists in Java Programming

### Step 01 - Understanding the need and Basics about an Array

You can use an index to find the specific element from the array. It is done by using the indexing operator, '[]'.

The expression marks[0] maps to the first array element stored at index 0 of the array marks.

```java
jshell> marks[0]
$20 ==> 75

jshell> marks[1]
$21 ==> 60

jshell> marks[2]
$22 ==> 56
```

---

### Step 16 - Introduction to Array and ArrayList - Conclusion

In this section, we were introduced to the concepts of **Arrays** and **ArrayLists** in Java.

These data structures allow us to store and manipulate collections of data efficiently.

We learned why arrays are necessary for handling data of the same type and the limitations that led us to explore **ArrayLists** as a more flexible alternative.

### 1. **Arrays**: The Basics

- Arrays allow you to store **multiple elements** of the same type in a single variable.

- We explored several operations that can be performed using arrays, such as:
  - Storing and accessing a collection of values (e.g., marks).

  - **Sum**, **maximum**, **minimum**, and **average** of marks.

### 2. Limitations of Arrays

- **Fixed Size**: Once an array is created, its size cannot be changed.

- **Adding and Removing Elements**: Inserting or removing elements in arrays can be cumbersome and inefficient because arrays have a fixed size.

### 3. **ArrayList**: A More Flexible Alternative
- Unlike arrays, **ArrayLists** are dynamic and can grow or shrink in size as needed.

- We introduced basic operations such as adding and removing elements using ArrayLists.

### 4. ArrayList and the Java Collections Framework

- ArrayList is part of the **Java Collections Framework**.

- While this section introduced the basic usage of ArrayLists, more advanced concepts related to collections will be discussed in a future section.

### Additional Coding Exercises:

### **Exercise 1: Array Operations**

**Objective:** Understand and demonstrate basic operations with Java arrays, including creation, initialization, and simple calculations.

**Instructions:**

1. Create an array of integers to store daily temperatures for a week.
   
2. Initialize the array with sample temperature values.
3. Calculate and print the average temperature for the week.
4. Find and print the highest and lowest temperatures.
5. Print all the temperatures stored in the array.

**Code:**

```java
public class WeeklyTemperatureArray {
    public static void main(String[] args) {
        // Step 1: Create an array for daily temperatures
        int[] temperatures = new int[7];

        // Step 2: Initialize the array with sample values
        temperatures[0] = 28; // Monday
        temperatures[1] = 30; // Tuesday
        temperatures[2] = 27; // Wednesday
        temperatures[3] = 29; // Thursday
        temperatures[4] = 31; // Friday
        temperatures[5] = 32; // Saturday
        temperatures[6] = 30; // Sunday

        // Step 3: Calculate average temperature
        int sum = 0;
        for (int temp : temperatures) {
            sum += temp;
        }
        double average = (double) sum / temperatures.length;

        // Step 4: Find highest and lowest temperatures
        int highest = temperatures[0];
        int lowest = temperatures[0];
        for (int i = 1; i < temperatures.length; i++) {
            if (temperatures[i] > highest) {
                highest = temperatures[i];
            }
            if (temperatures[i] < lowest) {
                lowest = temperatures[i];
            }
        }

        // Step 5: Print results
        System.out.println("Daily Temperatures:");
        for (int i = 0; i < temperatures.length; i++) {
            System.out.println("Day " + (i + 1) + ": " + temperatures[i] + "°C");
        }
        System.out.println("Average Temperature: " + average + "°C");
        System.out.println("Highest Temperature: " + highest + "°C");
        System.out.println("Lowest Temperature: " + lowest + "°C");
    }
}
```

**Output:**

```java
Daily Temperatures:
Day 1: 28°C
Day 2: 30°C
Day 3: 27°C
Day 4: 29°C
Day 5: 31°C
Day 6: 32°C
Day 7: 30°C
Average Temperature: 29.571428571428573°C
Highest Temperature: 32°C
Lowest Temperature: 27°C
```

**Explanation:**

- We create an array of integers to store temperatures for each day of the week.

- We use array indexing to initialize and access elements.
- We use a for-each loop to calculate the sum of temperatures.
- We use a traditional for loop to find the highest and lowest temperatures.
- The length of the array is used to calculate the average and iterate through all elements.

### **Exercise 2: ArrayList Operations**

**Objective:** Understand and demonstrate basic operations with Java ArrayList, including adding elements, removing elements, and iterating through the list.

**Instructions:**

1. Create an ArrayList to store a list of fruits.

2. Add several fruit names to the list.
3. Print the initial list of fruits.
4. Remove a fruit from the list.
5. Add a new fruit to the list.
6. Check if a specific fruit is in the list.
7. Print the final list of fruits and the total number of fruits.

**Code:**

```java
import java.util.ArrayList;

public class FruitListArrayList {
    public static void main(String[] args) {
        // Step 1: Create an ArrayList for fruits
        ArrayList<String> fruits = new ArrayList<>();

        // Step 2: Add fruits to the list
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");
        fruits.add("Mango");

        // Step 3: Print initial list
        System.out.println("Initial fruit list:");
        printFruits(fruits);

        // Step 4: Remove a fruit
        fruits.remove("Banana");
        System.out.println("\nAfter removing Banana:");
        printFruits(fruits);

        // Step 5: Add a new fruit
        fruits.add("Grapes");
        System.out.println("\nAfter adding Grapes:");
        printFruits(fruits);

        // Step 6: Check if a fruit is in the list
        String fruitToCheck = "Mango";
        if (fruits.contains(fruitToCheck)) {
            System.out.println("\n" + fruitToCheck + " is in the list.");
        } else {
            System.out.println("\n" + fruitToCheck + " is not in the list.");
        }

        // Step 7: Print final list and count
        System.out.println("\nFinal fruit list:");
        printFruits(fruits);
        System.out.println("Total number of fruits: " + fruits.size());
    }

    // Helper method to print fruits
    private static void printFruits(ArrayList<String> fruits) {
        for (String fruit : fruits) {
            System.out.println("- " + fruit);
        }
    }
}
```

**Output:**

```java
Initial fruit list:
- Apple
- Banana
- Orange
- Mango

After removing Banana:
- Apple
- Orange
- Mango

After adding Grapes:
- Apple
- Orange
- Mango
- Grapes

Mango is in the list.

Final fruit list:
- Apple
- Orange
- Mango
- Grapes
Total number of fruits: 4
```

**Explanation:**

- We use ArrayList to create a dynamic list of fruits.
  
- The `add()` method is used to add elements to the ArrayList.
- The `remove()` method is used to remove an element from the ArrayList.
- The `contains()` method checks if an element is present in the ArrayList.
- The `size()` method returns the number of elements in the ArrayList.
- We use a for-each loop to iterate through the ArrayList and print its contents.

---

## Section 20: Java - Oriented Programming Again

### Step 20 - Java Interface Flyable and Abstract Class Animal - An Exercise

In this exercise, we will practice implementing both an **interface** and an **abstract class** in Java.

We will focus on how interfaces represent common actions across different objects and how abstract classes provide a base for shared functionality.

### Exercise 1: Interface `Flyable`

We want to create an interface called **Flyable**, which represents the action of flying. This interface will be implemented by two classes: **Bird** and **Aeroplane**, which have different methods of flying.

### Steps:

1. Create the interface `Flyable` with a method `void fly()`.

2. Implement the interface in two classes:

   - **Bird**: The `fly()` method should print `"with wings"`.

   - **Aeroplane**: The `fly()` method should print `"with fuel"`.

3. In the `FlyableRunner` class, create an array of `Flyable` objects (`new Bird()` and `new Aeroplane()`).

4. Loop through the array and call the `fly()` method for each object.

#### Code:

```java
// Flyable Interface
interface Flyable {
    void fly();
}

// Bird class implementing Flyable
class Bird implements Flyable {
    @Override
    public void fly() {
        System.out.println("with wings");
    }
}

// Aeroplane class implementing Flyable
class Aeroplane implements Flyable {
    @Override
    public void fly() {
        System.out.println("with fuel");
    }
}

// Runner class to test the interface
public class FlyableRunner {
    public static void main(String[] args) {
        // Creating an array of Flyable objects
        Flyable[] flyingObjects = { new Bird(), new Aeroplane() };

        // Looping through the array and invoking fly() on each object
        for (Flyable object : flyingObjects) {
            object.fly();
        }
    }
}
```

#### Output:

```java
with wings
with fuel
```

#### Explanation:

- The interface **Flyable** declares a common method `fly()`.

- The classes **Bird** and **Aeroplane** implement the `fly()` method with their respective flying mechanisms.

- In the `FlyableRunner`, we loop through the array of `Flyable` objects and invoke the `fly()` method on both `Bird` and `Aeroplane`.

### Exercise 2: Abstract Class `Animal`

We want to create an abstract class called **Animal**, which has an abstract method `void bark()`.

Two concrete classes, **Dog** and **Cat**, will extend this abstract class and provide their own implementations of the `bark()` method.

### Steps:

1. Create an abstract class `Animal` with an abstract method `void bark()`.

2. Implement two classes:

   - **Dog**: The `bark()` method should print `"Bow Bow"`.

   - **Cat**: The `bark()` method should print `"Meow Meow"`.

3. In the `AnimalRunner` class, create an array of `Animal` objects (`new Dog()` and `new Cat()`).

4. Loop through the array and call the `bark()` method for each object.

#### Code:

```java
// Abstract class Animal
abstract class Animal {
    abstract void bark();
}

// Dog class extending Animal
class Dog extends Animal {
    @Override
    public void bark() {
        System.out.println("Bow Bow");
    }
}

// Cat class extending Animal
class Cat extends Animal {
    @Override
    public void bark() {
        System.out.println("Meow Meow");
    }
}

// Runner class to test the abstract class
public class AnimalRunner {
    public static void main(String[] args) {
        // Creating an array of Animal objects
        Animal[] animals = { new Dog(), new Cat() };

        // Looping through the array and invoking bark() on each object
        for (Animal animal : animals) {
            animal.bark();
        }
    }
}
```

#### Output:

```java
Bow Bow
Meow Meow
```

#### Explanation:

- The abstract class **Animal** defines the abstract method `bark()`.

- The **Dog** and **Cat** classes implement the `bark()` method with their own sounds.

- In the `AnimalRunner`, we loop through the array of `Animal` objects and invoke the `bark()` method on both `Dog` and `Cat`.

---

### Step 21 - Polymorphism - An introduction

In this lecture, we explore an important concept in object-oriented programming: **Polymorphism**.

Polymorphism allows objects of different types to be treated as instances of the same class or interface, enabling the same code to execute different behavior depending on the object.

### Example 1: Polymorphism with Interfaces

Let's start with an example where we use an interface called `GamingConsole`.

We will create two classes, **MarioGame** and **ChessGame**, that implement the same interface but have different behaviors.

#### Steps:

1. Create an interface **GamingConsole** with a method `void play()`.

2. Implement the interface in two classes:

   - **MarioGame**: Implements `play()` method with Mario game-specific behavior.

   - **ChessGame**: Implements `play()` method with Chess game-specific behavior.

3. Create an array of type `GamingConsole` to store objects of both `MarioGame` and `ChessGame`.

4. Loop through the array and call the `play()` method for each object.

#### Code:

```java
// GamingConsole Interface
interface GamingConsole {
    void play();
}

// MarioGame class implementing GamingConsole
class MarioGame implements GamingConsole {
    @Override
    public void play() {
        System.out.println("Jump, Goes into hole, Go forward");
    }
}

// ChessGame class implementing GamingConsole
class ChessGame implements GamingConsole {
    @Override
    public void play() {
        System.out.println("Move piece up, down, left, right");
    }
}

// Runner class to test polymorphism with interfaces
public class GameRunner {
    public static void main(String[] args) {
        // Creating an array of GamingConsole objects
        GamingConsole[] games = { new MarioGame(), new ChessGame() };

        // Looping through the array and invoking play() on each object
        for (GamingConsole game : games) {
            game.play();
        }
    }
}
```

#### Output:

```java
Jump, Goes into hole, Go forward
Move piece up, down, left, right
```

#### Explanation:

- The interface **GamingConsole** declares a common method `play()`.

- Both **MarioGame** and **ChessGame** provide different implementations of the `play()` method.

- The `GameRunner` class loops through the array of `GamingConsole` objects and invokes `play()` on each one, executing different behavior depending on the object (`MarioGame` or `ChessGame`).

### Example 2: Polymorphism with Abstract Classes

Polymorphism can also be achieved through **abstract classes**.

Let's create an abstract class called `Animal` with an abstract method `void bark()`, and then create two concrete classes, **Dog** and **Cat**, that extend the abstract class.

#### Steps:

1. Create an abstract class **Animal** with an abstract method `void bark()`.

2. Implement two classes:

   - **Dog**: Implements the `bark()` method with `"Bow Bow"`.

   - **Cat**: Implements the `bark()` method with `"Meow Meow"`.

3. Create an array of type `Animal` to store objects of both `Dog` and `Cat`.

4. Loop through the array and call the `bark()` method for each object.

#### Code:

```java
// Abstract class Animal
abstract class Animal {
    abstract void bark();
}

// Dog class extending Animal
class Dog extends Animal {
    @Override
    public void bark() {
        System.out.println("Bow Bow");
    }
}

// Cat class extending Animal
class Cat extends Animal {
    @Override
    public void bark() {
        System.out.println("Meow Meow");
    }
}

// Runner class to test polymorphism with abstract classes
public class AnimalRunner {
    public static void main(String[] args) {
        // Creating an array of Animal objects
        Animal[] animals = { new Cat(), new Dog() };

        // Looping through the array and invoking bark() on each object
        for (Animal animal : animals) {
            animal.bark();
        }
    }
}
```

#### Output:

```java
Meow Meow
Bow Bow
```

#### Explanation:

- The abstract class **Animal** defines the abstract method `bark()`.

- The **Dog** and **Cat** classes provide different implementations of the `bark()` method.

- The `AnimalRunner` class loops through the array of `Animal` objects and invokes `bark()` on each one, resulting in different behavior based on the actual object (`Cat` or `Dog`).

### What is Polymorphism?

- **Polymorphism** allows the same method to exhibit different behavior based on the object it is called on.

- This enables us to write more flexible and maintainable code by using common interfaces or base classes, while still allowing individual objects to define their specific behavior.

### Additional Coding Exercises:

### Exercise 1: Polymorphism with a Shape Interface

**Objective:** Understand polymorphism by creating a `Shape` interface and implementing it in various shape classes.

#### Implementation
In this exercise, we will create an interface named `Shape` with a method `draw()`. We will implement this interface in two classes, `Circle` and `Square`, each providing its own implementation of the `draw()` method. We will then create a main class to demonstrate how polymorphism allows us to treat different shapes uniformly.

#### Code

1. **Create the `Shape` interface:**
   ```java
   // Shape.java
   public interface Shape {
       void draw(); // Method to draw the shape
   }
   ```

2. **Implement the `Shape` interface in the `Circle` class:**
   ```java
   // Circle.java
   public class Circle implements Shape {
       @Override
       public void draw() {
           System.out.println("Drawing a Circle");
       }
   }
   ```

3. **Implement the `Shape` interface in the `Square` class:**
   ```java
   // Square.java
   public class Square implements Shape {
       @Override
       public void draw() {
           System.out.println("Drawing a Square");
       }
   }
   ```

4. **Write a main class to demonstrate polymorphism:**
   ```java
   // Main.java
   public class Main {
       public static void main(String[] args) {
           // Creating an array of Shape references
           Shape[] shapes = new Shape[2];
           
           // Instantiating Circle and Square
           shapes[0] = new Circle();
           shapes[1] = new Square();
           
           // Iterating through the shapes array and calling draw method
           for (Shape shape : shapes) {
               shape.draw(); // Dynamic method dispatch
           }
       }
   }
   ```

#### Output
```
Drawing a Circle
Drawing a Square
```

#### Explanation

- In this exercise, we defined an interface called `Shape`, which declares a method `draw()`. The `Circle` and `Square` classes implement this interface and provide their specific implementations of the `draw()` method. 

- In the `Main` class, we created an array of `Shape` references and instantiated objects of `Circle` and `Square`. By iterating through the array and calling the `draw()` method, we demonstrated polymorphism.

- This allows us to call the same method on different types of objects, showcasing dynamic method dispatch—where the method that gets executed is determined at runtime based on the actual object type.

### Exercise 2: Method Overloading in a Calculator Class

**Objective:** Practice method overloading by creating a `Calculator` class with overloaded methods for addition.

#### Implementation

In this exercise, we will implement a `Calculator` class that has multiple `add` methods. Each method will have a different signature, allowing it to handle various types and numbers of parameters.

This will demonstrate how method overloading enables a class to perform similar operations in different ways.

#### Code

1. **Create the `Calculator` class:**
   ```java
   // Calculator.java
   public class Calculator {
       
       // Method to add two integers
       public int add(int a, int b) {
           return a + b;
       }
       
       // Method to add three integers
       public int add(int a, int b, int c) {
           return a + b + c;
       }
       
       // Method to add two double values
       public double add(double a, double b) {
           return a + b;
       }
   }
   ```

2. **Write a main class to test the `Calculator` class:**
   ```java
   // Main.java
   public class Main {
       public static void main(String[] args) {
           Calculator calculator = new Calculator();
           
           // Testing the add methods
           int sum1 = calculator.add(5, 10); // Adding two integers
           int sum2 = calculator.add(5, 10, 15); // Adding three integers
           double sum3 = calculator.add(5.5, 10.5); // Adding two double values
           
           // Printing results
           System.out.println("Sum of 5 and 10 is: " + sum1); // Output: 15
           System.out.println("Sum of 5, 10, and 15 is: " + sum2); // Output: 30
           System.out.println("Sum of 5.5 and 10.5 is: " + sum3); // Output: 16.0
       }
   }
   ```

#### Output

```java
Sum of 5 and 10 is: 15
Sum of 5, 10, and 15 is: 30
Sum of 5.5 and 10.5 is: 16.0
```

#### Explanation

In this exercise, we created a `Calculator` class that demonstrates method overloading, a core concept in OOP. The `add()` method is overloaded to handle different types and numbers of parameters:

- **Two integers:** Adds two integers and returns the result.

- **Three integers:** Adds three integers, showcasing the flexibility of method overloading.

- **Two doubles:** Adds two double values, illustrating that methods can be differentiated by parameter types.

In the `Main` class, we instantiated the `Calculator` and tested the overloaded methods, demonstrating that Java can determine which method to call based on the method signature at compile time. This enhances code readability and allows multiple operations to be performed seamlessly.

---

## Section 22: Collections in Java Programming


### Additional Coding Exercises:

### **Exercise 1: Set Operations**

**Problem Statement:**  
Given a list of integers:
```java
List<Integer> numbers = List.of(5, 10, 5, 20, 10, 15);
```
1. Display unique integers using a `HashSet`.

2. Display these integers in insertion order using a `LinkedHashSet`.

3. Display these integers in sorted order using a `TreeSet`.

**Solution:**

```java
import java.util.*;

public class SetOperations {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(5, 10, 5, 20, 10, 15);

        // Using HashSet to display unique integers (order is not guaranteed)
        Set<Integer> hashSet = new HashSet<>(numbers);
        System.out.println("HashSet (Unique, Unordered): " + hashSet);

        // Using LinkedHashSet to maintain insertion order
        Set<Integer> linkedHashSet = new LinkedHashSet<>(numbers);
        System.out.println("LinkedHashSet (Insertion Order): " + linkedHashSet);

        // Using TreeSet to display integers in sorted order
        Set<Integer> treeSet = new TreeSet<>(numbers);
        System.out.println("TreeSet (Sorted Order): " + treeSet);
    }
}
```

**Output:**

```java
HashSet (Unique, Unordered): [20, 5, 10, 15]
LinkedHashSet (Insertion Order): [5, 10, 20, 15]
TreeSet (Sorted Order): [5, 10, 15, 20]
```

**Explanation:**
- The `HashSet` removes duplicates but does not maintain any order.

- The `LinkedHashSet` preserves the insertion order.

- The `TreeSet` stores elements in natural (sorted) order.

### **Exercise 2: Queue Operations with Custom Comparator**

**Problem Statement:**  

Create a `PriorityQueue` with the following strings:

```java
List<String> words = List.of("Elephant", "Dog", "Cat", "Giraffe", "Mouse");
```
1. Add these words into a `PriorityQueue` and display them in natural (alphabetical) order.

2. Use a custom comparator to sort the words by length, and display them in ascending order of length.

**Solution:**

```java
import java.util.*;

public class PriorityQueueOperations {
    public static void main(String[] args) {
        List<String> words = List.of("Elephant", "Dog", "Cat", "Giraffe", "Mouse");

        // PriorityQueue with natural ordering (alphabetical order)
        PriorityQueue<String> alphabeticalQueue = new PriorityQueue<>(words);
        System.out.println("PriorityQueue (Alphabetical Order):");
        while (!alphabeticalQueue.isEmpty()) {
            System.out.println(alphabeticalQueue.poll());
        }

        // PriorityQueue with custom comparator for length-based ordering
        PriorityQueue<String> lengthQueue = new PriorityQueue<>(Comparator.comparingInt(String::length));
        lengthQueue.addAll(words);
        System.out.println("\nPriorityQueue (Length Order):");
        while (!lengthQueue.isEmpty()) {
            System.out.println(lengthQueue.poll());
        }
    }
}
```

**Output:**

```java
PriorityQueue (Alphabetical Order):
Cat
Dog
Elephant
Giraffe
Mouse

PriorityQueue (Length Order):
Cat
Dog
Mouse
Giraffe
Elephant
```

**Explanation:**

- The first `PriorityQueue` sorts words alphabetically by default.

- The second `PriorityQueue` uses a custom comparator to sort words based on their length (`String::length`).

---

## Section 24: Generics in Java Programming

### Additional Coding Exercises:

### Exercise 1: Implement a Size Method

**Task:** Add a method named `size` to the `MyCustomList` class that returns the number of elements currently in the list.

#### Explanation:

1. **Purpose:** This method allows users to determine how many elements are present in the custom list.

2. **Return Type:** The method returns an integer representing the size of the list.

3. **Implementation Steps:**
   - Use the `size()` method from the underlying `ArrayList` to retrieve the count of elements.
   - Ensure that the method is accessible and adheres to generics.

#### Code:

**MyCustomList.java**
```java
package com.in28minutes.generics;

import java.util.ArrayList;

public class MyCustomList<T> {
    ArrayList<T> list = new ArrayList<>();

    // Method to add an element
    public void addElement(T element) {
        list.add(element);
    }

    // Method to remove an element
    public void removeElement(T element) {
        list.remove(element);
    }

    // Method to get an element at a specific index
    public T get(int index) {
        return list.get(index);
    }

    // Method to return the size of the list
    public int size() {
        return list.size(); // Returns the current number of elements in the list
    }

    // Override toString() for better representation
    @Override
    public String toString() {
        return list.toString(); // Returns a string representation of the list
    }
}
```

**GenericsRunner.java**
```java
package com.in28minutes.generics;

public class GenericsRunner {
    public static void main(String[] args) {
        MyCustomList<String> list = new MyCustomList<>();
        list.addElement("Element-1");
        list.addElement("Element-2");
        System.out.println("Size of list: " + list.size()); // Expected output: 2

        MyCustomList<Integer> list2 = new MyCustomList<>();
        list2.addElement(Integer.valueOf(5));
        list2.addElement(Integer.valueOf(9));
        System.out.println("Size of list2: " + list2.size()); // Expected output: 2
    }
}
```

#### Output:

```java
Size of list: 2
Size of list2: 2
```

### Exercise 2: Implement a Clear Method

**Task:** Add a method named `clear` to the `MyCustomList` class that removes all elements from the list.

#### Explanation:
1. **Purpose:** This method allows users to empty the custom list of all its elements.

2. **Return Type:** The method returns void since it modifies the list in place.

3. **Implementation Steps:**
   - Use the `clear()` method from the underlying `ArrayList` to remove all elements.
   - Ensure the method is accessible and performs the action effectively.

#### Code:

**MyCustomList.java**
```java
package com.in28minutes.generics;

import java.util.ArrayList;

public class MyCustomList<T> {
    ArrayList<T> list = new ArrayList<>();

    // Method to add an element
    public void addElement(T element) {
        list.add(element);
    }

    // Method to remove an element
    public void removeElement(T element) {
        list.remove(element);
    }

    // Method to get an element at a specific index
    public T get(int index) {
        return list.get(index);
    }

    // Method to return the size of the list
    public int size() {
        return list.size(); // Returns the current number of elements in the list
    }

    // Method to clear all elements from the list
    public void clear() {
        list.clear(); // Clears the entire list
    }

    // Override toString() for better representation
    @Override
    public String toString() {
        return list.toString(); // Returns a string representation of the list
    }
}
```

**GenericsRunner.java**
```java
package com.in28minutes.generics;

public class GenericsRunner {
    public static void main(String[] args) {
        MyCustomList<String> list = new MyCustomList<>();
        list.addElement("Element-1");
        list.addElement("Element-2");
        System.out.println("List before clear: " + list); // Expected output: [Element-1, Element-2]
        list.clear(); // Clearing the list
        System.out.println("List after clear: " + list); // Expected output: []
    }
}
```

#### Output:
```
List before clear: [Element-1, Element-2]
List after clear: []
```

---

## Section 25: Introduction to Functional Programming in Java

### Step 12 - Optional class in Java - An Introduction

In an earlier section, we wrote and ran the following code:

```java
	jshell> List.of(23, 12, 34, 53).stream().max((n1, n2) -> Integer.compare(n1, n2));
	Optional[53]
	jshell>
```

In order to get the result in a form you would appreciate, we modified this code to look like:

```java
jshell> List.of(23, 12, 34, 53).stream().max((n1, n2) -> Integer.compare(n1, n2)).get();
53
jshell>
```

`max()` is a stream operation, that needs to consume a stream. It is possible that the input stream is empty. In that case, the maximum value would be null. It is undesirable in FP to encounter an exception during a stream operation.

It is extremely inelegant if we are asked to handle an exception in an FP code pipeline.

---

### Step 18 - Introduction to Functional Programming - Conclusion

In this section, we explored the basics of **functional programming** in Java, a powerful paradigm that allows developers to write more concise, readable, and maintainable code.

We introduced the concept of **functions as first-class citizens**, enabling the storage of functions in variables, passing functions to methods, and returning functions from methods.

This opens new opportunities for programming, especially when working with data in a more declarative way.

### 1. **Functions as First-Class Citizens**

- In functional programming, functions can be treated like any other variable or object. You can:

  - Store functions in variables.

  - Pass functions as arguments to methods.

  - Return functions as values from methods.

This flexibility allows developers to build more modular and reusable code by separating **what** to do from **how** to do it.

### 2. **Imperative vs Declarative Programming**

We contrasted two different programming styles:

- **Imperative Programming**: You specify **how** to do something step-by-step.

  - For example, summing a list of numbers involves explicitly creating a variable to store the sum, looping through the numbers, and adding each one.
  
  ```java
  int sum = 0;
  for (int number : numbers) {
      sum += number;
  }
  ```

- **Declarative Programming**: You focus on **what** to do rather than how to do it.

  - Functional programming allows you to express the same logic at a higher level. For instance, summing a list of numbers using **streams** can be written declaratively.

  ```java
  int sum = numbers.stream().reduce(0, Integer::sum);
  ```

### 3. **Benefits of Functional Programming**

- **Code Simplicity**: Functional programming simplifies logic by allowing you to write cleaner, more readable code without the need for explicit state management or mutation.

- **Higher Abstraction**: With functional programming, you can operate at a **higher level of abstraction**, focusing on what the code should do instead of how to implement it.

- **Immutability**: Functional programming encourages avoiding **mutation**, leading to fewer side effects and more predictable code behavior.

### Challenges of Adopting Functional Programming

Functional programming can feel unfamiliar and complex, particularly for programmers accustomed to **imperative** and **object-oriented** paradigms.

The functional approach is often less intuitive, especially when working with constructs like **streams** and **lambda expressions** for the first time.

### Additional Coding Exercises:

### Exercise 1: Race Condition Simulation

**Objective:** Demonstrate a race condition by implementing a simple counter increment using multiple threads.

#### Explanation:
In this exercise, we will create a counter that multiple threads will increment. Due to the lack of synchronization, we expect to observe inconsistencies in the final counter value, demonstrating a race condition.

#### Instructions:
1. Create a class named `RaceConditionDemo`.

2. Declare a static variable `counter` initialized to `0`.
3. Implement a method `incrementCounter()` that increments the `counter` variable.
4. Create multiple threads that will call the `incrementCounter()` method.
5. Run the threads and print the final value of the `counter` after all threads have finished executing.

#### Code:

```java
public class RaceConditionDemo {
    static int counter = 0; // Shared counter variable

    // Method to increment the counter
    public static void incrementCounter() {
        counter++; // Incrementing the counter
    }

    public static void main(String[] args) throws InterruptedException {
        Thread[] threads = new Thread[10]; // Array to hold threads

        // Creating and starting 10 threads
        for (int i = 0; i < 10; i++) {
            threads[i] = new Thread(() -> {
                for (int j = 0; j < 1000; j++) { // Each thread increments 1000 times
                    incrementCounter();
                }
            });
            threads[i].start(); // Start each thread
        }

        // Waiting for all threads to finish
        for (Thread thread : threads) {
            thread.join();
        }

        // Printing the final value of the counter
        System.out.println("Final counter value (without synchronization): " + counter);
    }
}
```

####  Output:

You may not always see the expected output of `10000` due to the race condition. For example, you might see:
```
Final counter value (without synchronization): 9995
```

This exercise shows how concurrent modifications to shared resources can lead to unexpected results due to race conditions.

### Exercise 2: Thread Safety with Synchronized Block

**Objective:** Fix the race condition in the previous exercise by using a synchronized block.

#### Explanation:
In this exercise, we will modify the `incrementCounter()` method to include synchronization. This will ensure that only one thread can execute the method at a time, preventing race conditions.

#### Instructions:
1. Modify the `incrementCounter()` method to use the `synchronized` keyword.

2. Run the threads again and print the final value of the `counter` after all threads have finished executing.

#### Code:

```java
public class ThreadSafeDemo {
    static int counter = 0; // Shared counter variable

    // Synchronized method to increment the counter
    public synchronized static void incrementCounter() {
        counter++; // Incrementing the counter safely
    }

    public static void main(String[] args) throws InterruptedException {
        Thread[] threads = new Thread[10]; // Array to hold threads

        // Creating and starting 10 threads
        for (int i = 0; i < 10; i++) {
            threads[i] = new Thread(() -> {
                for (int j = 0; j < 1000; j++) { // Each thread increments 1000 times
                    incrementCounter();
                }
            });
            threads[i].start(); // Start each thread
        }

        // Waiting for all threads to finish
        for (Thread thread : threads) {
            thread.join();
        }

        // Printing the final value of the counter
        System.out.println("Final counter value (with synchronization): " + counter);
    }
}
```

#### Output:

With the use of synchronization, the output should consistently be `10000`, for example:

```java
Final counter value (with synchronization): 10000
```

This exercise illustrates how synchronization can prevent race conditions in multithreaded applications, ensuring thread safety when accessing shared resources.

---

## Section 27: Introduction to Threads And Concurrency in Java

### Step 08 - Need for Controlling the Execution of Threads

Drawbacks of earlier approaches

We saw few of the methods for synchronization in the Thread class

- `start()`
- `join()`
- `sleep()`
- `wait()`

#### Above approaches have a few drawbacks:

No Fine-Grained Control: Suppose, for instance , we want Task3 to run after any one of Task1 or Task2 is done.

#### How do we do it?

- **Difficult to maintain**: Imagine managing 5-10 threads with code written in earlier examples. It would become very difficult to maintain.

- **NO Sub-Task Return Mechanism**: With the Thread class or the Runnable interface, there is no way to get the result from a sub-task.

---

### Step 14 - Threads and MultiThreading - Conclusion

In this section, we explored the concept of **MultiThreading** in Java. 

We began by learning how to create threads, manage their execution, and handle communication between them.

We also introduced the **ExecutorService** to simplify the process of managing multiple threads.

This section provided a comprehensive overview of the key features Java offers for multithreading.

### 1. Creating Threads in Java

We learned two primary ways to create a thread in Java:

- **Extending the Thread class**: Create a new class that extends `Thread` and overrides the `run()` method.

- **Implementing the Runnable interface**: Create a class that implements `Runnable` and pass it to a `Thread` object.

### 2. Thread States and Management

We explored the different **states** a thread can be in:

- **New**
- **Runnable**
- **Blocked/Waiting**
- **Timed Waiting**
- **Terminated**

We also looked at:

- **Thread priorities**: How to set different priorities for threads.

- **Waiting for threads**: Techniques like `join()` to wait for threads to complete their execution.

- **Thread communication**: Methods such as `wait()`, `notify()`, and `notifyAll()` to synchronize threads.

### 3. ExecutorService

Managing multiple threads manually can become complex. 

- **ExecutorService** simplifies this by handling the creation and management of threads efficiently.

- We discussed how **ExecutorService** allows us to control how many threads are used to process tasks, providing a more scalable and efficient solution.

### 4. Handling Results with `Future`

We learned how to retrieve results from a thread using **Future**. By calling the `get()` method on a `Future` object, we can wait for the result of a task and retrieve it once the task is completed.

### 5. `invokeAll()` and `invokeAny()`

- **`invokeAll()`**: Executes multiple tasks concurrently and waits for **all** tasks to complete before proceeding.

- **`invokeAny()`**: Executes multiple tasks concurrently and returns the result of the **first** completed task, canceling the remaining tasks.

### Additional Coding Exercises:

### Exercise 1: Synchronizing Multiple Tasks

**Objective:** Create a Java program that uses threads to execute three tasks. Task 1 and Task 2 should run in parallel, and Task 3 should start only after both Task 1 and Task 2 have completed.

**Instructions:**

1. Define three tasks: `Task1`, `Task2`, and `Task3`. 

   - **Task1** should print numbers from 1 to 10.

   - **Task2** should print letters from 'A' to 'J'.
   - **Task3** should print "All tasks completed!" after Task 1 and Task 2 are done.

2. In the `main` method, start `Task1` and `Task2`, and use the `join()` method to ensure that `Task3` executes only after both `Task1` and `Task2` are finished.

**Code:**

```java
class Task1 extends Thread {
    public void run() {
        for (int i = 1; i <= 10; i++) {
            System.out.print(i + " ");
        }
        System.out.println("\nTask1 Done");
    }
}

class Task2 extends Thread {
    public void run() {
        for (char c = 'A'; c <= 'J'; c++) {
            System.out.print(c + " ");
        }
        System.out.println("\nTask2 Done");
    }
}

class Task3 {
    public void execute() {
        System.out.println("All tasks completed!");
    }
}

public class SynchronizationExample {
    public static void main(String[] args) throws InterruptedException {
        Task1 task1 = new Task1();
        Task2 task2 = new Task2();
        
        task1.start();
        task2.start();
        
        task1.join();
        task2.join();
        
        Task3 task3 = new Task3();
        task3.execute();
    }
}
```

**Output:**

```java
1 2 3 4 5 6 7 8 9 10 
Task1 Done
A B C D E F G H I J 
Task2 Done
All tasks completed!
```

### Exercise 2: Using ExecutorService for Parallel Execution

**Objective:** Create a Java program that uses `ExecutorService` to manage multiple tasks running in parallel. All tasks should print their identifiers (e.g., Task 1, Task 2, etc.) and indicate when they are done.

**Instructions:**

1. Define a `Runnable` task that takes a task identifier (e.g., Task 1, Task 2) and prints a message indicating when it starts and when it is done.

2. Create an `ExecutorService` with a fixed thread pool of 3.
3. Submit multiple tasks (at least 5) to the executor service and observe how they run concurrently.
4. After submitting the tasks, call `shutdown()` on the executor service to stop accepting new tasks and wait for previously submitted tasks to complete.

**Code:**

```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

class PrintTask implements Runnable {
    private final String taskName;

    public PrintTask(String taskName) {
        this.taskName = taskName;
    }

    public void run() {
        System.out.println(taskName + " started.");
        try {
            Thread.sleep(1000); // Simulate work
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }
        System.out.println(taskName + " done.");
    }
}

public class ExecutorServiceExample {
    public static void main(String[] args) {
        ExecutorService executorService = Executors.newFixedThreadPool(3);
        
        for (int i = 1; i <= 5; i++) {
            executorService.execute(new PrintTask("Task " + i));
        }
        
        executorService.shutdown();
    }
}
```

**Output:**

```java
Task 1 started.
Task 2 started.
Task 3 started.
Task 4 started.
Task 5 started.
Task 1 done.
Task 2 done.
Task 3 done.
Task 4 done.
Task 5 done.
```

---

## Section 28: Introduction to Exception Handling in Java

### Step 01 - Introduction to Exception Handling - Your Thought Process during Exceptions

#### Snippet-1 : Exception Condition

ExceptionHandlingRunner.java

```java

	package com.in28minutes.exceptionhandling;
	
	public class ExceptionHandlingRunner {
		public static void main(String[] args) {
			callMethod();
			System.out.println("callMethod Done");		
		}

		static void callMethod() {
			String str = null;
			int len = str.length();
			System.out.println("String Length Done");
		}		
	}	
```

#### Console Output

```java
java.lang.NullPointerException

Exception in thread "main" java.lang.NullPointerException

at com.in28minutes.exceptionhandling.ExceptionHandlingRunner.callMethod (ExceptionHandlingRunner.java:8)

at com.in28minutes.exceptionhandling.ExceptionHandlingRunner.main (ExceptionHandlingRunner.java:4)
```


#### Snippet-01 Explained

A java.lang.NullPointerException is thrown by the Java run-time when we called length() on the null reference.

If an exception is not handled in the entire call chain, including main, the exception is thrown out and the program terminates.

System.out.println() statements after the exception are never executed.

The runtime prints the call stack trace onto the console.

For instance, consider this simple class Test:

```java
	public class Test {
		public static void main(String[] args) {
			callOne();
		}

		public static void callOne() {
			callTwo();
		}

		public static void callTwo() {
			callThree();
		}

		public static void callThree() {
			String name;
			System.out.println("This name is %d characters long", name.length());
		}
	}
```

However, the code name.length() used in callThree() caused a NullPointerException to be thrown.

However, this is not handled, and the console coughs up the following display:

```java
Exception in thread "main" java.lang.NullPointerException

at Test.callThree(Test.java:13)

at Test.callTwo(Test.java:9)

at Test.callOne(Test.java:6)

at Test.main(Test.java:3)
```

This is nothing but a call trace of the stack, frozen in time.

---

### Step 14 - Exception Handling - Conclusion with Best Practices

In this section, we covered **exception handling** in Java, focusing on best practices derived from extensive real-world experience.

Effective exception handling is crucial for building robust applications. This conclusion summarizes key practices that can help in writing better exception handling code.

### Best Practices for Exception Handling

### 1. **Never Hide Exceptions**

- Always log the full **stack trace** of an exception. The stack trace provides invaluable information about where the exception occurred, which is crucial for debugging.

- Avoid catching an exception and failing to provide the necessary information for someone to trace the problem later.

### 2. **Do Not Use Exceptions for Flow Control**

- Avoid using exceptions as a substitute for regular conditional logic (e.g., `if-else` statements).

- Exceptions are meant to handle **error conditions**, not to control the flow of a program.

- Exception handling is expensive in terms of resources. Using it as a flow control mechanism can degrade performance.

### 3. **Consider the End User**

- Always think about what the **end user** sees when an exception occurs. 

- The user should see a **friendly error message** that indicates what went wrong and what they can do about it, if possible.

- End users should not see technical details such as stack traces. These are meant for the **support team** or **developers**.

### 4. **Think About the Support Team**

- When handling exceptions, ensure you log enough **information** for the support team to debug the issue.

- Logs should provide the **context**, stack trace, and any relevant details that can help the support team reproduce and fix the issue.

### 5. **Consider the Calling Method**

- When throwing exceptions, think about what the **calling method** can do with the exception.

- If there is nothing meaningful that the calling method can do, consider making the exception a **RuntimeException** (unchecked).

- **Checked exceptions** should only be used when the caller can potentially handle the exception meaningfully.

### 6. **Use Global Exception Handling**

- Ensure that your application has a **global exception handler** to catch any uncaught exceptions.

- For example, in a console application, make sure the main method handles all exceptions gracefully.

- In web applications, implement a global exception handler to catch and handle all exceptions centrally, ensuring that no technical details are exposed to the end user.

### Additional Coding Exercises:

### Exercise 1: Exception Handling in Currency Addition

**Objective:** Implement exception handling when trying to add two amounts of different currencies. Use both checked and unchecked exceptions.

**Instructions:**

1. Create a class `CurrencyMismatchException` that extends `RuntimeException`.

2. Create a class `Amount` with the following:
   - Fields: `String currency` and `int amount`.
   - A method `add(Amount that)` that:
     - Throws `CurrencyMismatchException` if the currencies do not match.
     - Adds the amounts if the currencies match.
  
3. Create a class `CurrencyTest` with a `main` method that:
   - Instantiates two `Amount` objects with different currencies.
   - Calls the `add()` method and handles the exception by printing a meaningful message.

**Code:**

```java
// CurrencyMismatchException.java
public class CurrencyMismatchException extends RuntimeException {
    public CurrencyMismatchException(String message) {
        super(message);
    }
}

// Amount.java
public class Amount {
    private String currency;
    private int amount;

    public Amount(String currency, int amount) {
        this.currency = currency;
        this.amount = amount;
    }

    public String getCurrency() {
        return currency;
    }

    public int getAmount() {
        return amount;
    }

    public Amount add(Amount that) {
        if (!this.currency.equals(that.currency)) {
            throw new CurrencyMismatchException("Currency mismatch: Cannot add " + this.amount + " " + this.currency + " and " + that.amount + " " + that.currency);
        }
        return new Amount(this.currency, this.amount + that.amount);
    }
}

// CurrencyTest.java
public class CurrencyTest {
    public static void main(String[] args) {
        Amount usdAmount = new Amount("USD", 10);
        Amount eurAmount = new Amount("EUR", 20);
        
        try {
            Amount totalAmount = usdAmount.add(eurAmount);
            System.out.println("Total Amount: " + totalAmount.getAmount() + " " + totalAmount.getCurrency());
        } catch (CurrencyMismatchException e) {
            System.out.println(e.getMessage());
        }
    }
}
```

**Output:**

```java
Currency mismatch: Cannot add 10 USD and 20 EUR
```

### Exercise 2: Throwing Custom Exceptions

**Objective:** Create and use a custom checked exception when trying to add two amounts of different currencies.

**Instructions:**
1. Define a class `CurrencyMismatchException` that extends `Exception`.

2. Create a class `Amount` with the following:
   - Fields: `String currency` and `int amount`.
   - A method `add(Amount that)` that:
     - Throws `CurrencyMismatchException` if the currencies do not match.
     - Adds the amounts if they match.
  
3. Create a class `AmountTester` with a `main` method that:
   - Instantiates two `Amount` objects with different currencies.
   - Calls the `add()` method and handles the `CurrencyMismatchException` with a try-catch block.
   - Prints a stack trace of the exception.

**Code:**

```java
// CurrencyMismatchException.java
public class CurrencyMismatchException extends Exception {
    public CurrencyMismatchException(String message) {
        super(message);
    }
}

// Amount.java
public class Amount {
    private String currency;
    private int amount;

    public Amount(String currency, int amount) {
        this.currency = currency;
        this.amount = amount;
    }

    public String getCurrency() {
        return currency;
    }

    public int getAmount() {
        return amount;
    }

    public Amount add(Amount that) throws CurrencyMismatchException {
        if (!this.currency.equals(that.currency)) {
            throw new CurrencyMismatchException("Currencies Don't Match: " + this.currency + " & " + that.currency);
        }
        return new Amount(this.currency, this.amount + that.amount);
    }
}

// AmountTester.java
public class AmountTester {
    public static void main(String[] args) {
        Amount usdAmount = new Amount("USD", 10);
        Amount eurAmount = new Amount("EUR", 20);
        
        try {
            Amount totalAmount = usdAmount.add(eurAmount);
            System.out.println("Total Amount: " + totalAmount.getAmount() + " " + totalAmount.getCurrency());
        } catch (CurrencyMismatchException e) {
            e.printStackTrace();
        }
    }
}
```

**Output:**

```java
Exception in thread "main" CurrencyMismatchException: Currencies Don't Match: USD & EUR
	at Amount.add(Amount.java:12)
	at AmountTester.main(AmountTester.java:15)
```

---

## Section 29: Files and Directories in Java

### Step 05 - Files - Conclusion

In this section, we explored various operations related to **files and directories** in Java.

We focused on modern file handling techniques using features introduced in Java 7 and Java 8, specifically from the **Java New I/O (NIO)** package.

This section provided a practical overview of how to interact with files efficiently using the latest APIs and functional programming techniques.

### 1. **Listing Files in a Directory**

- We started by learning how to **list files** within a specific directory. 

- We also explored how to **recursively** traverse through all files in nested directories.

- Filtering files based on attributes, such as file type or size, was demonstrated.

### 2. **Finding Files with Filters**

- We used the **Find()** method to apply filters when searching for files. 

- These filters allowed us to search based on attributes like whether the path is a directory, file size, etc.

### 3. **Reading File Content**

- We learned how to **read the content** of a file using `readAllLines()`. However, for large files, this approach can be inefficient as it loads all lines into memory.

- We introduced the more efficient **Files.lines()** method, which returns a **Stream** of lines, allowing for efficient processing of large files with operations like `map()` and `filter()`.

### 4. **Writing to a File**

- We also covered how to **write content** to a file, demonstrating how to take data and save it to a file efficiently.

### Java NIO and Functional Programming Features

This section primarily used features introduced in **Java 7 (NIO)** and **Java 8**:

- **Java NIO (New I/O)** package (`java.nio.file`), which provides better scalability and functionality for file operations.

- **Streams**: We used `Files.lines()` to read large files as streams.

- **Lambda expressions** and **Predicates**: These functional programming techniques were utilized for filtering and processing file content efficiently.

### Additional Coding Exercises:

### Exercise 1: Count Lines in a File

### Objective:
Write a Java program that reads a text file and counts the total number of lines in it. This exercise helps understand how to read files and perform operations on the data.

#### File: `LineCountRunner.java`

```java
package com.in28minutes.files;

import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.io.IOException;

public class LineCountRunner {
    public static void main(String[] args) throws IOException {
        // Specify the path of the file to read
        Path pathFileToRead = Paths.get("./resources/data.txt");

        // Use Files.lines to create a stream of lines from the file
        long lineCount = Files.lines(pathFileToRead).count();

        // Output the total number of lines
        System.out.println("Total number of lines: " + lineCount);
    }
}
```

#### Explanation:
- **Package Declaration**: The class is part of the `com.in28minutes.files` package.

- **Imports**: The program imports necessary classes from the `java.nio.file` and `java.io` packages to handle file operations.
- **Path Creation**: The `Paths.get` method is used to create a `Path` object representing the file `data.txt`.
- **Line Counting**: The `Files.lines` method reads all lines from the file as a stream, and the `count()` method counts the number of lines in that stream.
- **Output**: The result is printed to the console.

#### Output:

```java
Total number of lines: 5
```

### Exercise 2: Append Text to a File

#### Objective:
Write a Java program that appends a line of text to an existing text file. This exercise demonstrates how to modify files by adding content.

#### File: `FileAppendRunner.java`

```java
package com.in28minutes.files;

import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.io.IOException;
import java.util.List;

public class FileAppendRunner {
    public static void main(String[] args) throws IOException {
        // Specify the path of the file to append to
        Path pathFileToAppend = Paths.get("./resources/data.txt");

        // Create a list of new lines to append
        List<String> newLines = List.of("Dog", "Elephant");

        // Use Files.write with StandardOpenOption.APPEND to add new lines to the file
        Files.write(pathFileToAppend, newLines, java.nio.file.StandardOpenOption.APPEND);

        // Output confirmation message
        System.out.println("New lines appended to the file.");
    }
}
```

#### Explanation:

- **Package Declaration**: The class is part of the `com.in28minutes.files` package.

- **Imports**: The program imports necessary classes from the `java.nio.file` and `java.io` packages.

- **Path Creation**: The `Paths.get` method is used to create a `Path` object representing the file `data.txt`.

- **New Lines Creation**: A list of new lines (`Dog` and `Elephant`) is created using `List.of()`.

- **Appending Lines**: The `Files.write` method is called with the `StandardOpenOption.APPEND` option, which appends the new lines to the existing content in the file.

- **Output**: A confirmation message is printed to the console.


```java
New lines appended to the file.
```

---

## Section 30: More Concurrency with Concurrent Collections and Atomic Operations

### Step 09 - Conclusion

In this section, we explored the concept of **concurrency** in Java.

The focus was on understanding how to manage shared resources in a multithreaded environment while ensuring thread safety.

We covered a range of tools and techniques, starting with `synchronized` blocks, moving to locks, and then exploring more advanced concurrency utilities like **Atomic classes** and **Concurrent Collections**.

### 1. **Synchronized Blocks**

- We began by using the `synchronized` keyword to control access to shared resources. 

- While synchronization ensures thread safety, we discussed the **disadvantages** such as performance overhead due to contention between threads.

### 2. **BiCounter with Locks**

- To address the limitations of `synchronized`, we introduced the concept of **locks**.

- We implemented a **BiCounter** using `Lock` objects, which provided more fine-grained control over synchronization, allowing greater flexibility.

### 3. **Atomic Classes**

- We explored **AtomicInteger**, which provides **atomic operations** without the need for explicit locking.

- These atomic classes internally use low-level synchronization, ensuring thread safety for operations like `incrementAndGet()`, `compareAndSet()`, etc.

- Other atomic classes such as **AtomicLong** were also introduced for handling atomic operations on long data types.

### 4. **Concurrent Collections**

We moved from atomic classes to exploring **concurrent collections**, which provide built-in thread-safe implementations of commonly used collections.

#### a. **ConcurrentMap and ConcurrentHashMap**

- We looked at **ConcurrentHashMap**, a thread-safe version of `HashMap` that splits the map into regions (segments), each of which can be locked independently, promoting higher concurrency.

- This reduces contention and enhances **performance** when multiple threads access the map simultaneously.

- We also explored **atomic operations** on concurrent collections, like `computeIfAbsent()`.

#### b. **CopyOnWriteArrayList**

- **CopyOnWriteArrayList** is another concurrent collection designed for scenarios with **many reads and few writes**.

- It synchronizes only during write operations by creating a new copy of the list whenever a modification is made. This avoids the need to lock during read operations, improving performance for read-heavy workloads.

### Additional Coding Exercises:

### Exercise 1: Implementing a Thread-Safe Counter

**Objective**: Create a thread-safe counter using the `synchronized` keyword.

#### Instructions:
1. Create a class `ThreadSafeCounter` with the following:
   - A private integer variable `counter`.
   - A method `increment()` that increases `counter` by 1.
   - A method `getCounter()` that returns the current value of `counter`.

2. Create a `Main` class to test `ThreadSafeCounter`:
   - Create multiple threads that call the `increment()` method.
   - After all threads have finished executing, print the final value of the counter.

#### Solution:

```java
class ThreadSafeCounter {
    private int counter = 0;

    public synchronized void increment() {
        counter++;
    }

    public synchronized int getCounter() {
        return counter;
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        ThreadSafeCounter counter = new ThreadSafeCounter();
        Thread[] threads = new Thread[10];

        for (int i = 0; i < 10; i++) {
            threads[i] = new Thread(() -> {
                for (int j = 0; j < 1000; j++) {
                    counter.increment();
                }
            });
            threads[i].start();
        }

        for (Thread thread : threads) {
            thread.join();
        }

        System.out.println("Final counter value: " + counter.getCounter());
    }
}
```

#### Explanation:

- **ThreadSafeCounter Class**: 
  - It has a private integer variable `counter` initialized to 0.
  - The `increment()` method is synchronized to ensure that only one thread can execute it at a time, preventing race conditions.
  - The `getCounter()` method is also synchronized to provide the current value of `counter` safely.

- **Main Class**:
  - We create an array of 10 threads, each of which increments the counter 1000 times.
  - The `join()` method is used to wait for all threads to finish execution before printing the final counter value.

#### Output:

```java
Final counter value: 10000
```

### Exercise 2: Using `ConcurrentHashMap`

**Objective**: Create a simple word frequency counter using `ConcurrentHashMap`.

#### Instructions:

1. Create a class `WordFrequencyCounter` with the following:
   - A `ConcurrentHashMap<String, Integer>` to store words and their frequencies.
   - A method `addWord(String word)` that increments the count for the word in the map.
   - A method `getFrequency(String word)` that returns the frequency of the word.

2. Create a `Main` class to test `WordFrequencyCounter`:

   - Create multiple threads that add words to the counter.
   - After all threads have finished executing, print the frequencies of specific words.

#### Solution:
```java
import java.util.concurrent.ConcurrentHashMap;

class WordFrequencyCounter {
    private ConcurrentHashMap<String, Integer> wordCounts = new ConcurrentHashMap<>();

    public void addWord(String word) {
        wordCounts.merge(word, 1, Integer::sum);
    }

    public int getFrequency(String word) {
        return wordCounts.getOrDefault(word, 0);
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        WordFrequencyCounter counter = new WordFrequencyCounter();
        String[] words = {"apple", "banana", "apple", "orange", "banana", "banana"};

        Thread[] threads = new Thread[words.length];

        for (int i = 0; i < words.length; i++) {
            final String word = words[i];
            threads[i] = new Thread(() -> {
                counter.addWord(word);
            });
            threads[i].start();
        }

        for (Thread thread : threads) {
            thread.join();
        }

        System.out.println("Frequency of 'apple': " + counter.getFrequency("apple"));
        System.out.println("Frequency of 'banana': " + counter.getFrequency("banana"));
        System.out.println("Frequency of 'orange': " + counter.getFrequency("orange"));
    }
}
```

#### Explanation:

- **WordFrequencyCounter Class**: 
  
  - It uses `ConcurrentHashMap` to store word frequencies, allowing multiple threads to safely modify it concurrently.
  
  - The `addWord(String word)` method uses the `merge` function to increment the count of a word or add it if it doesn't exist.
  - The `getFrequency(String word)` method retrieves the frequency of a word, returning 0 if the word is not found.

- **Main Class**:
  - We create an array of strings with words. Multiple threads are created to add words concurrently.

  - The `join()` method is used to wait for all threads to finish before printing the frequencies.

#### Output:
```
Frequency of 'apple': 2
Frequency of 'banana': 3
Frequency of 'orange': 1
```

---

## Section 31: Java Tips

> **Note**: Section-31 info here.

---

## Section 34: Java New Features - Java 10 to Java 16

> **Note**: Section-34 info here.

---
