# Exercise 1: SimpleCalculator: Implementing Basic Arithmetic Operations Using Lambda Expressions and Functional Interfaces


## Problem Statement

You are given an incomplete `SimpleCalculator` class that aims to perform basic arithmetic operations (addition, subtraction, and multiplication) using lambda expressions and a functional interface named `Calculator`. Your task is to complete the missing parts of the code.

### Instructions

1.  Define the lambda expressions for the following arithmetic operations:
    
    -   Addition
    -   Subtraction
    -   Multiplication
2.  Implement the `performCalculation` method that takes a `Calculator` object, two integer values `a` and `b`, and returns the result of the calculation.
    

### Steps

1.  Define the lambda expression for the addition operation. Replace the `null` value with a lambda expression that takes two integers `a` and `b` and returns the sum of the two numbers.
    
2.  Define the lambda expression for the subtraction operation. Replace the `null` value with a lambda expression that takes two integers `a` and `b` and returns the result of `a - b`.
    
3.  Define the lambda expression for the multiplication operation. Replace the `null` value with a lambda expression that takes two integers `a` and `b` and returns the result of `a * b`.
    
4.  Implement the `performCalculation` method. This method should accept a `Calculator` object and two integers `a` and `b`. It should return the result of the calculation performed by the `Calculator` object on `a` and `b`.

## Hints

1.  Lambda expressions are anonymous functions that can be assigned to functional interfaces. To define a lambda expression, use the following syntax: `(parameter1, parameter2) -> expression`.
    
2.  For the addition operation, the lambda expression should add the two input parameters and return the result.
    
3.  For the subtraction operation, the lambda expression should subtract the second input parameter from the first and return the result.
    
4.  For the multiplication operation, the lambda expression should multiply the two input parameters and return the result.
    
5.  The `performCalculation` method should call the `calculate` method of the given `Calculator` object with the input integers `a` and `b` and return the result of the calculation.


## Solution Explanation

The solution involves defining lambda expressions for the arithmetic operations (addition, subtraction, and multiplication) and implementing the `performCalculation` method to use the `Calculator` functional interface.

Here's the complete solution code with explanations:

```
public class SimpleCalculator {

    @FunctionalInterface
    public interface Calculator {
        int calculate(int a, int b);
    }

    public static void main(String[] args) {
        // Define the lambda expression for the addition operation
        Calculator addition = (a, b) -> a + b;

        // Define the lambda expression for the subtraction operation
        Calculator subtraction = (a, b) -> a - b;

        // Define the lambda expression for the multiplication operation
        Calculator multiplication = (a, b) -> a * b;

        // Test the calculator functionality
        System.out.println("Addition: " + performCalculation(addition, 5, 3)); // Output: 8
        System.out.println("Subtraction: " + performCalculation(subtraction, 5, 3)); // Output: 2
        System.out.println("Multiplication: " + performCalculation(multiplication, 5, 3)); // Output: 15
    }

    // Implement the performCalculation method
    public static int performCalculation(Calculator calculator, int a, int b) {
        return calculator.calculate(a, b);
    }
}
```

1.  Define the lambda expressions for the arithmetic operations:
    
    -   `Calculator addition = (a, b) -> a + b;` - The addition operation takes two integers `a` and `b` as input and returns their sum.
    -   `Calculator subtraction = (a, b) -> a - b;` - The subtraction operation takes two integers `a` and `b` as input and returns the result of `a - b`.
    -   `Calculator multiplication = (a, b) -> a * b;` - The multiplication operation takes two integers `a` and `b` as input and returns the result of `a * b`.
2.  Implement the `performCalculation` method:
    
    -   `public static int performCalculation(Calculator calculator, int a, int b)` - This method takes a `Calculator` object and two integers `a` and `b` as input.
    -   `return calculator.calculate(a, b);` - The method calls the `calculate` method of the given `Calculator` object with the input integers `a` and `b` and returns the result of the calculation.

By using lambda expressions and the functional interface `Calculator`, the solution provides a simple way to perform basic arithmetic operations with a flexible and reusable design.


## Student File

```
public class SimpleCalculator {

    @FunctionalInterface
    public interface Calculator {
        int calculate(int a, int b);
    }

    public static void main(String[] args) {
        // TODO: Define the lambda expression for the addition operation
        Calculator addition = null;

        // TODO: Define the lambda expression for the subtraction operation
        Calculator subtraction = null;

        // TODO: Define the lambda expression for the multiplication operation
        Calculator multiplication = null;

        // Test the calculator functionality
        System.out.println("Addition: " + performCalculation(addition, 5, 3)); // Output: 8
        System.out.println("Subtraction: " + performCalculation(subtraction, 5, 3)); // Output: 2
        System.out.println("Multiplication: " + performCalculation(multiplication, 5, 3)); // Output: 15
    }

    // TODO: Implement the performCalculation method
    public static int performCalculation(Calculator calculator, int a, int b) {
        return 0;
    }
}


```

## Solution File

```
public class SimpleCalculator {

    @FunctionalInterface
    public interface Calculator {
        int calculate(int a, int b);
    }

    public static void main(String[] args) {
        // Define the lambda expression for the addition operation
        Calculator addition = (a, b) -> a + b;

        // Define the lambda expression for the subtraction operation
        Calculator subtraction = (a, b) -> a - b;

        // Define the lambda expression for the multiplication operation
        Calculator multiplication = (a, b) -> a * b;

        // Test the calculator functionality
        System.out.println("Addition: " + performCalculation(addition, 5, 3)); // Output: 8
        System.out.println("Subtraction: " + performCalculation(subtraction, 5, 3)); // Output: 2
        System.out.println("Multiplication: " + performCalculation(multiplication, 5, 3)); // Output: 15
    }

    // Implement the performCalculation method
    public static int performCalculation(Calculator calculator, int a, int b) {
        return calculator.calculate(a, b);
    }
}

```

## Evaluation File

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;
import java.util.logging.Logger;

public class Evaluate {
    private static final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void test_addition() {
        SimpleCalculator.Calculator addition = (a, b) -> a + b;
        int result = SimpleCalculator.performCalculation(addition, 5, 3);
        logger.info("Addition test: expected output: 8, actual output: " + result);
        assertEquals(8, result, "Addition test failed");
    }

    @Test
    public void test_subtraction() {
        SimpleCalculator.Calculator subtraction = (a, b) -> a - b;
        int result = SimpleCalculator.performCalculation(subtraction, 5, 3);
        logger.info("Subtraction test: expected output: 2, actual output: " + result);
        assertEquals(2, result, "Subtraction test failed");
    }

    @Test
    public void test_multiplication() {
        SimpleCalculator.Calculator multiplication = (a, b) -> a * b;
        int result = SimpleCalculator.performCalculation(multiplication, 5, 3);
        logger.info("Multiplication test: expected output: 15, actual output: " + result);
        assertEquals(15, result, "Multiplication test failed");
    }
}
```