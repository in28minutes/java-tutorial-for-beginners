
# Exercise 2: Even Number Printer Calculator

  

## Instructions

#### Objective:

Complete the missing parts of the `EvenNumberPrinter` class in the `EvenNumberPrinterRunner` code file to implement the following methods:

-   `printEvenNumbers(int from, int to)`: Prints all even numbers in the range from `from` to `to` (inclusive), separated by a space.
-   `printEvenNumbers(int number)`: Prints all even numbers from 1 to the given number, separated by a space.
-   `printEvenNumbers()`: Prints all even numbers from 1 to 10 separated by a space.

#### Instructions:

1.  Implement the `printEvenNumbers(int from, int to)` method in the `EvenNumberPrinter` class:
    
    -   Use a for loop to iterate through the range of numbers from `from` to `to` (inclusive).
    -   Check if the current number is even using the modulo operator (i % 2 == 0).
    -   If the current number is even, print it using `System.out.printf(" %d", i)`.
2.  Implement the `printEvenNumbers(int number)` method in the `EvenNumberPrinter` class:
    
    -   Call the `printEvenNumbers(int from, int to)` method with `from` as 1 and `to` as the given `number`.
3.  Implement the `printEvenNumbers()` method in the `EvenNumberPrinter` class:
    
    -   Call the `printEvenNumbers(int from, int to)` method with `from` as 1 and `to` as 10.

#### Sample Input and Output:

Here are some sample inputs and their corresponding outputs to help you understand how the `EvenNumberPrinter` class should work:

1.  `evenNumberPrinter.printEvenNumbers(3, 12);`
    
    -   Output: `4 6 8 10 12`
2.  `evenNumberPrinter.printEvenNumbers(8);`
    
    -   Output: `2 4 6 8`
3.  `evenNumberPrinter.printEvenNumbers();`
    
    -   Output: `2 4 6 8 10`

These examples show the expected output when calling the different `printEvenNumbers` methods with various input values. Ensure that your implementation produces the correct output for each method. Note that the output should be separated by spaces, and there is no trailing or leading space.
  

## Hints

1. Use a `for` loop to iterate through the given range of numbers.

2. Use the modulo operator (`%`) to check if a number is even (i.e., if `number % 2 == 0`).

3. Use `System.out.printf()` to print the even numbers in each method.

  

## Solution Explanation

  
To implement the `EvenNumberPrinter` class, we need to complete the three methods: `printEvenNumbers(int from, int to)`, `printEvenNumbers(int number)`, and `printEvenNumbers()`.

### printEvenNumbers(int from, int to)

The `printEvenNumbers(int from, int to)` method should print all even numbers within the range `[from, to]` (inclusive). We can achieve this using a for loop to iterate through the range and an if statement to check if a number is even:

```
public static void printEvenNumbers(int from, int to) {
    for (int i = from; i <= to; i++) {
        if (i % 2 == 0) {
            System.out.printf(" %d", i);
        }
    }
}
```

### printEvenNumbers(int number)

The `printEvenNumbers(int number)` method should print all even numbers from 1 up to the given `number` (inclusive). We can use the previously defined `printEvenNumbers(int from, int to)` method to achieve this:

```
public static void printEvenNumbers(int number) {
    printEvenNumbers(1, number);
}
```

### printEvenNumbers()

The `printEvenNumbers()` method should print all even numbers up to 10 (inclusive). We can again use the `printEvenNumbers(int from, int to)` method for this:

```
public static void printEvenNumbers() {
    printEvenNumbers(1, 10);
}
```

### Testing the Solution

We can test the solution by calling each of the three methods with appropriate arguments in the `main` method:

```
public static void main(String[] args) {
    EvenNumberPrinter evenNumberPrinter = new EvenNumberPrinter();
    evenNumberPrinter.printEvenNumbers(3, 12); // Output: 4 6 8 10 12
    evenNumberPrinter.printEvenNumbers(8); // Output: 2 4 6 8
    evenNumberPrinter.printEvenNumbers(); // Output: 2 4 6 8 10
}
```

This completes the implementation of the `EvenNumberPrinter` class.

 

## Student File

**EvenNumberPrinterRunner.java**

```
public class EvenNumberPrinterRunner {

    public static class EvenNumberPrinter {
        
         public static void printEvenNumbers(int from, int to) {
            // Complete the code
        }
        
         public static void printEvenNumbers(int number) {
            // Complete the code
        }
        
        public static void printEvenNumbers() {
            // Complete the code
        }
       
    }

    public static void main(String[] args) {
        EvenNumberPrinter evenNumberPrinter = new EvenNumberPrinter();
        evenNumberPrinter.printEvenNumbers(3, 12);
        evenNumberPrinter.printEvenNumbers(8);
        evenNumberPrinter.printEvenNumbers();
        
        
    }
}

```

  
  

## Solution File

**EvenNumberPrinterRunner.java**

```
public class EvenNumberPrinterRunner {

    public static class EvenNumberPrinter {

        public static void printEvenNumbers(int from, int to) {
            for (int i = from; i <= to; i++) {
                if (i % 2 == 0) {
                    System.out.printf(" %d", i);
                }
            }
        }

        public static void printEvenNumbers(int number) {
            printEvenNumbers(1, number);
        }

        public static void printEvenNumbers() {
            printEvenNumbers(1, 10);
        }
    }

    public static void main(String[] args) {
        EvenNumberPrinter evenNumberPrinter = new EvenNumberPrinter();
        evenNumberPrinter.printEvenNumbers(3, 12);
        evenNumberPrinter.printEvenNumbers(8);
        evenNumberPrinter.printEvenNumbers();
    }
}
```

    

## Evaluation File

**Evaluate.java**

```
import com.udemy.ucp.IOHelper;
import org.junit.jupiter.api.Test;
import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {

    IOHelper helper = new IOHelper();
    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void testPrintEvenNumbers() {
        helper.resetStdOut(); // clean stdout
        EvenNumberPrinterRunner.EvenNumberPrinter.printEvenNumbers();
        String expectedOutput = " 2 4 6 8 10";
        String actualOutput = helper.getOutput();
        LOGGER.info("Expected Output: " + expectedOutput);
        LOGGER.info("Your output: " + actualOutput);
        assertEquals(expectedOutput, actualOutput, "Even numbers from 1 to 10 are not printed correctly.");
       
    }

    @Test
    public void testPrintEvenNumbersWithNumber() {
        helper.resetStdOut(); // clean stdout
        EvenNumberPrinterRunner.EvenNumberPrinter.printEvenNumbers(8);
        String expectedOutput = " 2 4 6 8";
        String actualOutput = helper.getOutput();
        LOGGER.info("Expected Output: " + expectedOutput);
        LOGGER.info("Your output: " + actualOutput);
        assertEquals(expectedOutput, actualOutput, "Even numbers from 1 to 8 are not printed correctly.");
        
    }

    @Test
    public void testPrintEvenNumbersWithRange() {
        helper.resetStdOut(); // clean stdout
        EvenNumberPrinterRunner.EvenNumberPrinter.printEvenNumbers(3, 12);
        String expectedOutput = " 4 6 8 10 12";
        String actualOutput = helper.getOutput();
        LOGGER.info("Expected Output: " + expectedOutput);
        LOGGER.info("Your output: " + actualOutput);
        assertEquals(expectedOutput, actualOutput, "Even numbers from 3 to 12 are not printed correctly.");
        
    }
}

```



































<!---
### Exercise 1:  Factorial Calculator : Implement a Factorial Calculator in Java

#### Instructions


**Task:**

Complete the missing parts of the `FactorialCalculator` class.

Implement the `print(int number)` and `print(int from, int to)` methods to print the factorial of the given number and the factorials of numbers in the given range, respectively.

Use the provided `calculateFactorial` method to calculate factorials.

**Steps:**

1.  Implement the `print(int number)` method:
    -   Use `System.out.printf()` to print the formatted output.
    -   Call `calculateFactorial(number)` to get the factorial of the given number.
2.  Implement the `print(int from, int to)` method:
    -   Use a for loop to iterate through the range of numbers from `from` to `to`.
    -   Call the `print(number)` method for each number in the range.

#### Hints

1.  For the `print(int number)` method, you can use `System.out.printf()` to print the formatted output. Use `calculateFactorial(number)` to get the factorial.
    
2.  For the `print(int from, int to)` method, use a for loop to iterate through the range of numbers and call `print(number)` method for each number in the range.

#### Solution Explanation

The solution implements the missing methods in the `FactorialCalculator` class.

1.  In the `print(int number)` method, we use `System.out.printf()` to print the formatted output with the factorial of the given number calculated using `calculateFactorial(number)`.

```
public static void print(int number) {
    System.out.printf("Factorial of %d is: %d", number, calculateFactorial(number)).println();
}
```

2.  In the `print(int from, int to)` method, we use a for loop to iterate through the range of numbers and call the `print(number)` method for each number in the range.

```
public static void print(int from, int to) {
    for (int i = from; i <= to; i++) {
        System.out.printf("Factorial of %d is: %d", i, calculateFactorial(i)).println();
    }
}
```

With these methods implemented, the `FactorialCalculator` class is complete and ready to be used in the `main` method to print factorials of individual numbers and ranges.


#### Student File
**FactorialCalculatorRunner.java**
```
public class FactorialCalculatorRunner {

    public static class FactorialCalculator {
        public static void print() {
            for (int i = 1; i <= 10; i++) {
                System.out.printf("Factorial of %d is: %d", i, calculateFactorial(i)).println();
            }
        }

        public static void print(int number) {
            // Complete the code
        }

        public static void print(int from, int to) {
            // Complete the code
        }

        private static long calculateFactorial(int number) {
            long factorial = 1;
            for (int i = 1; i <= number; i++) {
                factorial *= i;
            }
            return factorial;
        }
    }

    public static void main(String[] args) {
        FactorialCalculator factorialCalculator= new FactorialCalculator();
        factorialCalculator.print();
        factorialCalculator.print(8);
        factorialCalculator.print(3, 6);
    }
}


```


#### Solution File
**FactorialCalculatorRunner.java**
```
public class FactorialCalculatorRunner {

    public static class FactorialCalculator {
        public static void print() {
            for (int i = 1; i <= 10; i++) {
                System.out.printf("Factorial of %d is: %d", i, calculateFactorial(i)).println();
            }
        }

        public static void print(int number) {
            System.out.printf("Factorial of %d is: %d", number, calculateFactorial(number)).println();
        }

        public static void print(int from, int to) {
            for (int i = from; i <= to; i++) {
                System.out.printf("Factorial of %d is: %d", i, calculateFactorial(i)).println();
            }
        }

        private static long calculateFactorial(int number) {
            long factorial = 1;
            for (int i = 1; i <= number; i++) {
                factorial *= i;
            }
            return factorial;
        }
    }

    public static void main(String[] args) {
        FactorialCalculator factorialCalculator= new FactorialCalculator();
        factorialCalculator.print();
        factorialCalculator.print(8);
        factorialCalculator.print(3, 6);
    }
}
```



#### Evaluation File
**Evaluate.java**
```
import org.junit.jupiter.api.Test;
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

import java.io.ByteArrayOutputStream;
import java.io.PrintStream;

public class Evaluate {
    @Test
    public void testMainMethod() {
        PrintStream originalOut = System.out;
        ByteArrayOutputStream baos = new ByteArrayOutputStream();
        System.setOut(new PrintStream(baos));

        FactorialCalculatorRunner.main(null);

        System.setOut(originalOut);
        String capturedOutput = baos.toString();

        String lineSeparator = System.lineSeparator();
        String expectedOutput = "Factorial of 1 is: 1" + lineSeparator +
                                 "Factorial of 2 is: 2" + lineSeparator +
                                 "Factorial of 3 is: 6" + lineSeparator +
                                 "Factorial of 4 is: 24" + lineSeparator +
                                 "Factorial of 5 is: 120" + lineSeparator +
                                 "Factorial of 6 is: 720" + lineSeparator +
                                 "Factorial of 7 is: 5040" + lineSeparator +
                                 "Factorial of 8 is: 40320" + lineSeparator +
                                 "Factorial of 9 is: 362880" + lineSeparator +
                                 "Factorial of 10 is: 3628800" + lineSeparator +
                                 "Factorial of 8 is: 40320" + lineSeparator +
                                 "Factorial of 3 is: 6" + lineSeparator +
                                 "Factorial of 4 is: 24" + lineSeparator +
                                 "Factorial of 5 is: 120" + lineSeparator +
                                 "Factorial of 6 is: 720" + lineSeparator;

        assertEquals(expectedOutput, capturedOutput);
    }
}


```







### Exercise 2:  Even Number Printer  Calculator

#### Instructions


**Task:**

Complete the missing parts of the `EvenNumberPrinter` class to implement the following methods:

1.  `printEvenNumbers()`: Prints all even numbers from 1 to 10.
2.  `printEvenNumbers(int number)`: Prints all even numbers from 1 to `number`.
3.  `printEvenNumbers(int from, int to)`: Prints all even numbers in the range `from` to `to` (inclusive).

**Steps:**

1.  Implement the `printEvenNumbers()` method:
    -   Call the `printEvenNumbers(int from, int to)` method with `from` as 1 and `to` as 10.
2.  Implement the `printEvenNumbers(int number)` method:
    -   Call the `printEvenNumbers(int from, int to)` method with `from` as 1 and `to` as `number`.
3.  Implement the `printEvenNumbers(int from, int to)` method:
    -   Use a for loop to iterate through the range of numbers from `from` to `to` (inclusive).
    -   Check if the current number is even using the modulo operator (`i % 2 == 0`).
    -   If the current number is even, print it using `System.out.println(i)`.

#### Hints


1.  Use a `for` loop to iterate through the given range of numbers.
2.  Use the modulo operator (`%`) to check if a number is even (i.e., if `number % 2 == 0`).
3.  Use `System.out.println()` to print the even numbers in each method.

#### Solution Explanation

The solution implements the `EvenNumberPrinter` class with three methods for printing even numbers.

1.  `printEvenNumbers()`: This method prints even numbers from 1 to 10 by calling the `printEvenNumbers(int from, int to)` method with arguments 1 and 10.

```
public static void printEvenNumbers() {
    printEvenNumbers(1, 10);
}
```

2.  `printEvenNumbers(int number)`: This method prints even numbers from 1 to the given number by calling the `printEvenNumbers(int from, int to)` method with arguments 1 and `number`.

```
public static void printEvenNumbers(int number) {
    printEvenNumbers(1, number);
}
```

3.  `printEvenNumbers(int from, int to)`: This method iterates through the range `from` to `to` using a `for` loop and prints the even numbers using the `System.out.println()` method.

```
public static void printEvenNumbers(int from, int to) {
    for (int i = from; i <= to; i++) {
        if (i % 2 == 0) {
            System.out.println(i);
        }
    }
}
```

The main method calls these three methods to demonstrate their functionality:

```
public static void main(String[] args) {
    EvenNumberPrinter evenNumberPrinter = new EvenNumberPrinter();
    evenNumberPrinter.printEvenNumbers();
    evenNumberPrinter.printEvenNumbers(8);
    evenNumberPrinter.printEvenNumbers(3, 12);
}
```


#### Student File
**EvenNumberPrinterRunner.java**
```
public class EvenNumberPrinterRunner {

    public static class EvenNumberPrinter {
        public static void printEvenNumbers() {
            // Complete the code
        }

        public static void printEvenNumbers(int number) {
            // Complete the code
        }

        public static void printEvenNumbers(int from, int to) {
            // Complete the code
        }
    }

    public static void main(String[] args) {
        EvenNumberPrinter evenNumberPrinter = new EvenNumberPrinter();
        evenNumberPrinter.printEvenNumbers();
        evenNumberPrinter.printEvenNumbers(8);
        evenNumberPrinter.printEvenNumbers(3, 12);
    }
}



```


#### Solution File
**EvenNumberPrinterRunner.java**
```
public class EvenNumberPrinterRunner {

    public static class EvenNumberPrinter {
        public static void printEvenNumbers() {
            printEvenNumbers(1, 10);
        }

        public static void printEvenNumbers(int number) {
            printEvenNumbers(1, number);
        }

        public static void printEvenNumbers(int from, int to) {
            for (int i = from; i <= to; i++) {
                if (i % 2 == 0) {
                    System.out.println(i);
                }
            }
        }
    }

    public static void main(String[] args) {
        EvenNumberPrinter evenNumberPrinter = new EvenNumberPrinter();
        evenNumberPrinter.printEvenNumbers();
        evenNumberPrinter.printEvenNumbers(8);
        evenNumberPrinter.printEvenNumbers(3, 12);
    }
}

```



#### Evaluation File
**Evaluate.java**
```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

import java.io.ByteArrayOutputStream;
import java.io.PrintStream;

public class Evaluate {

    @Test
    public void testEvenNumbersMethods() {
        PrintStream originalOut = System.out;
        ByteArrayOutputStream baos = new ByteArrayOutputStream();
        System.setOut(new PrintStream(baos));

        EvenNumberPrinterRunner.EvenNumberPrinter.printEvenNumbers();
        EvenNumberPrinterRunner.EvenNumberPrinter.printEvenNumbers(8);
        EvenNumberPrinterRunner.EvenNumberPrinter.printEvenNumbers(3, 12);

        System.setOut(originalOut);
        String capturedOutput = baos.toString();

        String lineSeparator = System.lineSeparator();
        String expectedOutput = "2" + lineSeparator +
                                 "4" + lineSeparator +
                                 "6" + lineSeparator +
                                 "8" + lineSeparator +
                                 "10" + lineSeparator +
                                 "2" + lineSeparator +
                                 "4" + lineSeparator +
                                 "6" + lineSeparator +
                                 "8" + lineSeparator +
                                 "4" + lineSeparator +
                                 "6" + lineSeparator +
                                 "8" + lineSeparator +
                                 "10" + lineSeparator +
                                 "12" + lineSeparator;

        assertEquals(expectedOutput, capturedOutput);
    }
}


```


--->