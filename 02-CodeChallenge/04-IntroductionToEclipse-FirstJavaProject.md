### Exercise 2:  Factorial Calculator : Implement a Factorial Calculator in Java

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
