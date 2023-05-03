# Exercise 1: Pyramid Star Pattern Exercise 

## Problem Statement

In this exercise, you will complete a Java program to print a pyramid star pattern. The program has an incomplete function `printPyramidStarPattern()` that takes an integer `n` as an input, which represents the number of rows in the pyramid. Your task is to complete the function so that it prints a pyramid pattern with `n` rows using asterisks (*) and spaces.

### Instructions

1.  Complete the `printPyramidStarPattern(int n)` method inside the `PyramidStarPattern` class. This method should take an integer `n` as its parameter and print a pyramid pattern with `n` rows using asterisks (*) and spaces.
2.  In the `printPyramidStarPattern()` method, use nested loops to print the pyramid pattern.
    -   In the outer loop, iterate from `1` to `n` inclusive.
    -   In the first inner loop, print spaces. The number of spaces to print is equal to `n - i`, where `i` is the current iteration of the outer loop.
    -   In the second inner loop, print asterisks. The number of asterisks to print is equal to `(2 * i) - 1`.
    -   After printing the spaces and asterisks, move to the next line.

### Example Output

For an input of `5`, the output should look like this:

```
    *
   ***
  *****
 *******
*********
```

The main method and the variable initialization have already been provided for you. Complete the `printPyramidStarPattern()` method to produce the correct output for the given input. Good luck!


## Hints

1.  Use nested loops to construct the pyramid pattern. The outer loop iterates through each row, while the inner loops print spaces and asterisks.
    
2.  In the outer loop, start with `i = 1` and iterate up to `n` inclusive, where `n` is the number of rows.
    
3.  In the first inner loop, start with `j = 1` and iterate up to `n - i` inclusive. In each iteration, print a space character (`" "`).
    
4.  In the second inner loop, start with `k = 1` and iterate up to `(2 * i) - 1` inclusive. In each iteration, print an asterisk (`"*"`).
    
5.  After the inner loops have finished, use `System.out.println();` to move to the next line before the next iteration of the outer loop.
    

Remember to use the provided student code as a starting point, and complete the `printPyramidStarPattern()` method to produce the correct output.


## Answer Explanation

To complete the `printPyramidStarPattern()` method, we need to use nested loops to print spaces and asterisks in the correct order to form a pyramid pattern.

Here is the complete code with an explanation:

```
public class PyramidStarPattern {
    // Method to print a pyramid pattern with n rows
    public static void printPyramidStarPattern(int n) {
        // Iterate through each row, where i is the current row number
        for (int i = 1; i <= n; i++) {
            // Print spaces before the asterisks in the current row
            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }
            // Print asterisks in the current row
            for (int k = 1; k <= (2 * i) - 1; k++) {
                System.out.print("*");
            }
            // Move to the next line for the next row
            System.out.println();
        }
    }

    // Main method to run the program
    public static void main(String[] args) {
        // Set the fixed number of rows for the pyramid
        int myPyramid = 5;
        // Call the printPyramidStarPattern method with the specified number of rows
        printPyramidStarPattern(myPyramid);
    }
}

```

1.  The outer loop iterates from `1` to `n` inclusive, where `n` is the number of rows in the pyramid. In each iteration, the value of `i` represents the current row number.
    
2.  In the first inner loop, we print spaces. We iterate from `1` to `n - i` inclusive. In each iteration, we print a space character (`" "`). This creates the necessary spacing to the left of the pyramid.
    
3.  In the second inner loop, we print asterisks. We iterate from `1` to `(2 * i) - 1` inclusive. In each iteration, we print an asterisk (`"*"`). This forms the actual shape of the pyramid with increasing numbers of asterisks in each row.
    
4.  After the inner loops have finished, we use `System.out.println();` to move to the next line before the next iteration of the outer loop. This creates a new row for the next set of spaces and asterisks.
    

When the program is run, it will print the pyramid pattern with the specified number of rows (in this case, `5`).


## Student File

```
public class PyramidStarPattern {
    // Method to print the pyramid star pattern
    public static void printPyramidStarPattern(int n) {
        // TODO: Use nested loops to print the pyramid pattern
        // Outer loop: iterate through each row
        // First inner loop: print spaces (n - i spaces for row i)
        // Second inner loop: print asterisks ((2 * i) - 1 asterisks for row i)
        // After inner loops: move to the next line
    }

    // Main method to run the program
    public static void main(String[] args) {
        int myPyramid = 5; // Set the fixed number of rows for the pyramid
        // Call the printPyramidStarPattern method to print the pyramid pattern
        printPyramidStarPattern(myPyramid);
    }
}

```


## Solution File

```
public class PyramidStarPattern {
    // Method to print a pyramid pattern with n rows
    public static void printPyramidStarPattern(int n) {
        // Iterate through each row, where i is the current row number
        for (int i = 1; i <= n; i++) {
            // Print spaces before the asterisks in the current row
            for (int j = 1; j <= n - i; j++) {
                System.out.print(" ");
            }
            // Print asterisks in the current row
            for (int k = 1; k <= (2 * i) - 1; k++) {
                System.out.print("*");
            }
            // Move to the next line for the next row
            System.out.println();
        }
    }

    // Main method to run the program
    public static void main(String[] args) {
        // Set the fixed number of rows for the pyramid
        int myPyramid = 5;
        // Call the printPyramidStarPattern method with the specified number of rows
        printPyramidStarPattern(myPyramid);
    }
}

```

## Evaluation File

```
import org.junit.jupiter.api.AfterEach;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

import java.io.ByteArrayOutputStream;
import java.io.PrintStream;
import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {
    private final ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
    private final PrintStream originalOut = System.out;
    private final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @BeforeEach
    public void setUpStreams() {
        System.setOut(new PrintStream(outputStream));
    }

    @AfterEach
    public void restoreStreams() {
        System.setOut(originalOut);
    }

    @Test
    public void test_print_pyramid_with_1_row() {
        PyramidStarPattern.printPyramidStarPattern(1);
        String expected = "*\n";
        String actual = outputStream.toString();
        logger.info("Expected output: \n" + expected);
        logger.info("Actual output: \n" + actual);
        assertEquals(expected, actual, "Should print a pyramid with 1 row");
    }

    @Test
    public void test_print_pyramid_with_3_rows() {
        PyramidStarPattern.printPyramidStarPattern(3);
        String expected = "  *\n ***\n*****\n";
        String actual = outputStream.toString();
        logger.info("Expected output: \n" + expected);
        logger.info("Actual output: \n" + actual);
        assertEquals(expected, actual, "Should print a pyramid with 3 rows");
    }

    @Test
    public void test_print_pyramid_with_5_rows() {
        PyramidStarPattern.printPyramidStarPattern(5);
        String expected = "    *\n   ***\n  *****\n *******\n*********\n";
        String actual = outputStream.toString();
        logger.info("Expected output: \n" + expected);
        logger.info("Actual output: \n" + actual);
        assertEquals(expected, actual, "Should print a pyramid with 5 rows");
    }
}
```





# Exercise 2: Simple Calculator Exercise 

## Problem Statement

In this exercise, you will complete a Java program that acts as a simple calculator. The calculator allows users to perform addition and subtraction. The program contains a `printMenu()` method to display the available operations, and an incomplete `main` method where you need to implement the calculator's functionality.

### Instructions

1.  Complete the `main` method inside the `SimpleCalculator` class using a `do-while` loop. The loop should continue executing until the user chooses to exit (option `3`).
    
2.  Inside the `do-while` loop, call the `printMenu()` method to display the available operations.
    
3.  Read the user's choice using `scanner.nextInt()` and store it in the `choice` variable.
    
4.  Use conditional statements (`if-else`) to perform the selected operation:
    
    -   If `choice` is `1`, perform addition:
        -   Prompt the user with `System.out.print("Enter the first number: ");`
        -   Read the first number from the user using `scanner.nextInt()`.
        -   Prompt the user with `System.out.print("Enter the second number: ");`
        -   Read the second number from the user using `scanner.nextInt()`.
        -   Add the two numbers together and print the result using `System.out.println("The result is: " + sum);`
    -   If `choice` is `2`, perform subtraction:
        -   Prompt the user with `System.out.print("Enter the first number: ");`
        -   Read the first number from the user using `scanner.nextInt()`.
        -   Prompt the user with `System.out.print("Enter the second number: ");`
        -   Read the second number from the user using `scanner.nextInt()`.
        -   Subtract the second number from the first number and print the result using `System.out.println("The result is: " + difference);`
    -   If `choice` is `3`, exit the loop and print a goodbye message using `System.out.println("Thank you for using Simple Calculator. Goodbye!");`
    -   If the `choice` is any other value, print an error message indicating an invalid choice using `System.out.println("Invalid choice. Please try again.");`
5.  The loop should continue executing until the user selects option `3` (Exit). After the loop, close the `Scanner` object using `scanner.close()`.
    

### Example Output

A sample interaction with the calculator should look like this:

```
Welcome to Simple Calculator!
Please choose an operation:
1. Addition
2. Subtraction
3. Exit
Enter your choice: 1
Enter the first number: 5
Enter the second number: 3
The result is: 8

Welcome to Simple Calculator!
Please choose an operation:
1. Addition
2. Subtraction
3. Exit
Enter your choice: 2
Enter the first number: 10
Enter the second number: 4
The result is: 6

Welcome to Simple Calculator!
Please choose an operation:
1. Addition
2. Subtraction
3. Exit
Enter your choice: 3
Thank you for using Simple Calculator. Goodbye!
```

Complete the `main` method in the provided student code, following the solution code to implement the calculator's functionality. Ensure that you include the specific print statements as described in the instructions. Good luck!


## Hints

1.  Use a `do-while` loop to keep the calculator running until the user selects option `3` (Exit).
    
2.  Call the `printMenu()` method at the beginning of each iteration of the `do-while` loop to display the available operations.
    
3.  Use `scanner.nextInt()` to read the user's choice and store it in the `choice` variable.
    
4.  Use `if-else` statements to handle the user's choice:
    
    -   For addition (choice `1`), read two numbers and print their sum.
    -   For subtraction (choice `2`), read two numbers and print their difference.
    -   For exit (choice `3`), print a goodbye message and exit the loop.
    -   For an invalid choice, print an error message.
5.  Remember to close the `Scanner` object after the `do-while` loop using `scanner.close()`.
    

Use the provided student code as a starting point, and complete the `main` method to implement the calculator's functionality.


### Solution Explanation

To complete the `main` method inside the `SimpleCalculator` class, follow these steps:

1.  Wrap the calculator's functionality in a `do-while` loop that continues executing until the user selects option `3` (Exit).

```
do {
    // Calculator functionality will go here
} while (choice != 3);
```

2.  Inside the `do-while` loop, call the `printMenu()` method to display the available operations, and read the user's choice using `scanner.nextInt()`.

```
printMenu();
choice = scanner.nextInt();
```
3.  Use an `if-else` statement to perform the selected operation based on the user's choice:

```
if (choice == 1) {
    // Addition
} else if (choice == 2) {
    // Subtraction
} else if (choice == 3) {
    // Exit
} else {
    // Invalid choice
}
```

4.  Complete the `if-else` branches for addition, subtraction, and invalid choice:
    
    -   For addition (choice `1`), read two numbers from the user, add them together, and print the result.
    
```
System.out.print("Enter the first number: ");
    int num1 = scanner.nextInt();
    System.out.print("Enter the second number: ");
    int num2 = scanner.nextInt();
    int sum = num1 + num2;
    System.out.println("The result is: " + sum);
```
    
   -   For subtraction (choice `2`), read two numbers from the user, subtract the second number from the first number, and print the result.
    
 ```
    System.out.print("Enter the first number: ");
    int num1 = scanner.nextInt();
    System.out.print("Enter the second number: ");
    int num2 = scanner.nextInt();
    int difference = num1 - num2;
    System.out.println("The result is: " + difference);
````
    
   -   For exit (choice `3`), print a goodbye message.
    
   ```
   System.out.println("Thank you for using Simple Calculator. Goodbye!");
```
    
   -   For an invalid choice, print an error message.
    
    
    System.out.println("Invalid choice. Please try again.");
    
    
5.  After the `do-while` loop, close the `Scanner` object using `scanner.close()`.
    

Here is the complete `main` method with all the steps implemented:

```
import java.util.Scanner;

public class SimpleCalculator {

    // Print menu to display available operations
    public static void printMenu() {
        System.out.println("Welcome to Simple Calculator!");
        System.out.println("Please choose an operation:");
        System.out.println("1. Addition");
        System.out.println("2. Subtraction");
        System.out.println("3. Exit");
        System.out.print("Enter your choice: ");
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Initialize the Scanner object
        int choice; // Declare a variable to store the user's choice

        do {
            printMenu(); // Display the available operations
            choice = scanner.nextInt(); // Read the user's choice

            if (choice == 1) {
                // Perform addition
                System.out.print("Enter the first number: ");
                int num1 = scanner.nextInt();
                System.out.print("Enter the second number: ");
                int num2 = scanner.nextInt();
                int sum = num1 + num2;
                System.out.println("The result is: " + sum);
            } else if (choice == 2) {
                // Perform subtraction
                System.out.print("Enter the first number: ");
                int num1 = scanner.nextInt();
                System.out.print("Enter the second number: ");
                int num2 = scanner.nextInt();
                int difference = num1 - num2;
                System.out.println("The result is: " + difference);
            } else if (choice == 3) {
                // Exit the calculator
                System.out.println("Thank you for using Simple Calculator. Goodbye!");
            } else {
                // Handle invalid choice
                System.out.println("Invalid choice. Please try again.");
            }

        } while (choice != 3); // Continue executing until the user selects option 3 (Exit)

        scanner.close(); // Close the Scanner object
    }
}

```
With these steps implemented, the `SimpleCalculator` class is now complete. The calculator will continue running until the user selects option `3` (Exit), allowing them to perform addition and subtraction operations repeatedly. The specific print statements for each operation ensure clear communication with the user.


## Student File

```

import java.util.Scanner;

public class SimpleCalculator {

    // Print menu to display available operations
    public static void printMenu() {
        System.out.println("Welcome to Simple Calculator!");
        System.out.println("Please choose an operation:");
        System.out.println("1. Addition");
        System.out.println("2. Subtraction");
        System.out.println("3. Exit");
        System.out.print("Enter your choice: ");
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Initialize the Scanner object
        int choice; // Declare a variable to store the user's choice

        // Implement the calculator functionality in a do-while loop
        // The loop should continue until the user chooses to exit (option 3)
        // Your code will go here

        scanner.close(); // Close the Scanner object
    }
}


```


## Solution File

```
import java.util.Scanner;

public class SimpleCalculator {

    // Print menu to display available operations
    public static void printMenu() {
        System.out.println("Welcome to Simple Calculator!");
        System.out.println("Please choose an operation:");
        System.out.println("1. Addition");
        System.out.println("2. Subtraction");
        System.out.println("3. Exit");
        System.out.print("Enter your choice: ");
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Initialize the Scanner object
        int choice; // Declare a variable to store the user's choice

        do {
            printMenu(); // Display the available operations
            choice = scanner.nextInt(); // Read the user's choice

            if (choice == 1) {
                // Perform addition
                System.out.print("Enter the first number: ");
                int num1 = scanner.nextInt();
                System.out.print("Enter the second number: ");
                int num2 = scanner.nextInt();
                int sum = num1 + num2;
                System.out.println("The result is: " + sum);
            } else if (choice == 2) {
                // Perform subtraction
                System.out.print("Enter the first number: ");
                int num1 = scanner.nextInt();
                System.out.print("Enter the second number: ");
                int num2 = scanner.nextInt();
                int difference = num1 - num2;
                System.out.println("The result is: " + difference);
            } else if (choice == 3) {
                // Exit the calculator
                System.out.println("Thank you for using Simple Calculator. Goodbye!");
            } else {
                // Handle invalid choice
                System.out.println("Invalid choice. Please try again.");
            }

        } while (choice != 3); // Continue executing until the user selects option 3 (Exit)

        scanner.close(); // Close the Scanner object
    }
}


```


## Evaluation File

```

import org.junit.jupiter.api.AfterEach;
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
import java.io.InputStream;
import java.io.PrintStream;
import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {
    private final ByteArrayOutputStream outContent = new ByteArrayOutputStream();
    private final PrintStream originalOut = System.out;
    private static final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @BeforeEach
    public void setUpStreams() {
        System.setOut(new PrintStream(outContent));
    }

    @AfterEach
    public void restoreStreams() {
        System.setOut(originalOut);
    }

    @Test
    public void test_addition() {
        String input = "1\n5\n3\n3\n";
        InputStream in = new ByteArrayInputStream(input.getBytes());
        System.setIn(in);

        SimpleCalculator.main(new String[]{});

        String actualOutput = outContent.toString();
        String expectedOutput = "Welcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Enter the first number: Enter the second number: The result is: 8\nWelcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Thank you for using Simple Calculator. Goodbye!\n";
        assertEquals(expectedOutput, actualOutput);
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
    }

    @Test
    public void test_subtraction() {
        String input = "2\n5\n3\n3\n";
        InputStream in = new ByteArrayInputStream(input.getBytes());
        System.setIn(in);

        SimpleCalculator.main(new String[]{});

        String actualOutput = outContent.toString();
        String expectedOutput = "Welcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Enter the first number: Enter the second number: The result is: 2\nWelcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Thank you for using Simple Calculator. Goodbye!\n";
        assertEquals(expectedOutput, actualOutput);
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
    }

    @Test
    public void test_invalid_choice() {
        String input = "4\n3\n";
        InputStream in = new ByteArrayInputStream(input.getBytes());
        System.setIn(in);

        SimpleCalculator.main(new String[]{});

        String actualOutput = outContent.toString();
        String expectedOutput = "Welcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Invalid choice. Please try again.\nWelcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Thank you for using Simple Calculator. Goodbye!\n";
        assertEquals(expectedOutput, actualOutput);
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
    }

    @Test
    public void test_exit() {
        String input = "3\n";
        InputStream in = new ByteArrayInputStream(input.getBytes());
        System.setIn(in);

        SimpleCalculator.main(new String[]{});

        String actualOutput = outContent.toString();
        String expectedOutput = "Welcome to Simple Calculator!\nPlease choose an operation:\n1. Addition\n2. Subtraction\n3. Exit\nEnter your choice: Thank you for using Simple Calculator. Goodbye!\n";
        assertEquals(expectedOutput, actualOutput);
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
    }
}


```




