

# Exercise 1: Month Name Printer

## Problem Statement

You are tasked with implementing a Java program that takes an integer input representing the month number (1-12) and prints the corresponding month name.

### Instructions

1.  **TODO:** Implement the `getMonthName()` method which takes an integer `monthNumber` as a parameter and returns the corresponding month name as a string. If the given `monthNumber` is invalid (not in the range of 1-12), the method should return `null`.
    
2.  **TODO:** In the `main()` method, prompt the user to enter the month number (1-12). Call the `getMonthName()` method with the entered month number as an argument and store the result in a variable named `monthName`.
    
3.  **TODO:** Use an `if-else` statement to check if the `monthName` is `null`. If it is, print "Invalid month number entered." If it's not `null`, print "The name of month number [monthNumber] is [monthName]."
    

### Input Format

The input is a single integer `monthNumber` (1 ≤ monthNumber ≤ 12).

```
4
```

### Output Format

The output is a single line with the month name corresponding to the given `monthNumber`. If the `monthNumber` is invalid, the output is "Invalid month number entered."

```
The name of month number 4 is April.
```

### Example

**Input 1:**

```
Enter the month number (1-12):
4
```

**Output:**

```
The name of month number 4 is April.
```

**Input 2:**

```
Enter the month number (1-12):
0
```

**Output:**

```
Invalid month number entered.
```


## Hints

1.  Use a `switch` statement inside the `getMonthName()` method to map the `monthNumber` to its corresponding month name.
    
2.  Use a `Scanner` object to read user input in the `main()` method.
    
3.  After calling the `getMonthName()` method, use an `if-else` statement to check if the returned value is `null` or a valid month name.
    
4.  Print the appropriate message based on the value of the `monthName` variable.


## Answer Explanation

To implement the Month Name Printer program, follow these steps:

1.  Use a `switch` statement inside the `getMonthName()` method to map the `monthNumber` to its corresponding month name.
2.  Use a `Scanner` object to read user input in the `main()` method.
3.  After calling the `getMonthName()` method, use an `if-else` statement to check if the returned value is `null` or a valid month name.
4.  Print the appropriate message based on the value of the `monthName` variable.

Here's the complete code for the Month Name Printer program:


```
import java.util.Scanner;

public class MonthNamePrinter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the month number (1-12):");
        int monthNumber = scanner.nextInt();

        String monthName = getMonthName(monthNumber);

        if (monthName == null) {
            System.out.println("Invalid month number entered.");
        } else {
            System.out.println("The name of month number " + monthNumber + " is " + monthName + ".");
        }
    }

    public static String getMonthName(int monthNumber) {
        switch (monthNumber) {
            case 1: return "January";
            case 2: return "February";
            case 3: return "March";
            case 4: return "April";
            case 5: return "May";
            case 6: return "June";
            case 7: return "July";
            case 8: return "August";
            case 9: return "September";
            case 10: return "October";
            case 11: return "November";
            case 12: return "December";
            default: return null;
        }
    }
}
```

In this implementation, the `getMonthName()` method uses a `switch` statement to map the input `monthNumber` to its corresponding month name. If the input is invalid (not between 1 and 12), the method returns `null`.

The `main()` method uses a `Scanner` object to read the month number from the user, calls the `getMonthName()` method, and checks if the returned value is `null` or a valid month name. If the value is `null`, the program prints "Invalid month number entered." If the value is a valid month name, the program prints "The name of month number [monthNumber] is [monthName]."






## Student File

  

  

**MonthNamePrinter.java**

  

  

```

import java.util.Scanner;

public class MonthNamePrinter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the month number (1-12):");
        int monthNumber = scanner.nextInt();

        // TODO: Call the getMonthName method with monthNumber as the argument
        String monthName = null; // Replace 'null' with the method call

        if (monthName == null) {
            System.out.println("Invalid month number entered.");
        } else {
            System.out.println("The name of month number " + monthNumber + " is " + monthName + ".");
        }
    }

    // TODO: Complete the getMonthName method
    public static String getMonthName(int monthNumber) {
        // Implement the method to return the correct month name based on the given month number
        // You can use a switch statement to determine the month name
        return null; // Replace 'null' with your implementation
    }
}


```

  

  

  

## Solution File

  

  

**MonthNamePrinter.java**

  

  

```

import java.util.Scanner;

public class MonthNamePrinter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the month number (1-12):");
        int monthNumber = scanner.nextInt();

        String monthName = getMonthName(monthNumber);

        if (monthName == null) {
            System.out.println("Invalid month number entered.");
        } else {
            System.out.println("The name of month number " + monthNumber + " is " + monthName + ".");
        }
    }

    public static String getMonthName(int monthNumber) {
        switch (monthNumber) {
            case 1: return "January";
            case 2: return "February";
            case 3: return "March";
            case 4: return "April";
            case 5: return "May";
            case 6: return "June";
            case 7: return "July";
            case 8: return "August";
            case 9: return "September";
            case 10: return "October";
            case 11: return "November";
            case 12: return "December";
            default: return null;
        }
    }
}

```

  

  

## Evaluation File

  

**Evaluate.java**

  

  

```

import org.junit.jupiter.api.Test;

import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.*;

class Evaluate {
    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @Test
    void testGetMonthName() {
        LOGGER.info("Testing getMonthName() method...");
        assertEquals("January", MonthNamePrinter.getMonthName(1), "Month number 1 should return January");
        assertEquals("February", MonthNamePrinter.getMonthName(2), "Month number 2 should return February");
        assertEquals("March", MonthNamePrinter.getMonthName(3), "Month number 3 should return March");
        assertEquals("April", MonthNamePrinter.getMonthName(4), "Month number 4 should return April");
        assertEquals("May", MonthNamePrinter.getMonthName(5), "Month number 5 should return May");
        assertEquals("June", MonthNamePrinter.getMonthName(6), "Month number 6 should return June");
        assertEquals("July", MonthNamePrinter.getMonthName(7), "Month number 7 should return July");
        assertEquals("August", MonthNamePrinter.getMonthName(8), "Month number 8 should return August");
        assertEquals("September", MonthNamePrinter.getMonthName(9), "Month number 9 should return September");
        assertEquals("October", MonthNamePrinter.getMonthName(10), "Month number 10 should return October");
        assertEquals("November", MonthNamePrinter.getMonthName(11), "Month number 11 should return November");
        assertEquals("December", MonthNamePrinter.getMonthName(12), "Month number 12 should return December");
        assertNull(MonthNamePrinter.getMonthName(0), "Month number 0 should return null");
        assertNull(MonthNamePrinter.getMonthName(13), "Month number 13 should return null");
    }
}


```




# Exercise 2: Udemy Course Access Exercise

## Problem Statement

You are given the task of implementing a simple console application in Java that checks if a user is logged in and enrolled in the "in28Minutes" course on Udemy. The application should prompt the user to input their login and enrollment status and then display a response based on the input.

### Instructions

Complete the following tasks in the `UdemyCourseAccess` class:

-   **TODO 1**: Create a new `Scanner` object to read input from the console.
-   **TODO 2**: Prompt the user to enter their login status (1 for yes, 0 for no) and store the input in the `loggedIn` variable.
-   **TODO 3**: Prompt the user to enter their enrollment status (1 for yes, 0 for no) and store the input in the `enrolled` variable.
-   **TODO 4**: Call the `processUserInput` method with the `loggedIn` and `enrolled` values, and store the result in the `response` variable.
-   **TODO 5**: Print the response to the console.
-   **TODO 6**: Close the scanner to avoid resource leaks.
-   **TODO 7**: Implement the `processUserInput` method that takes `loggedIn` and `enrolled` as parameters and returns a `String` response.

In the `processUserInput` method, implement the following logic:

-   **TODO 8**: Check if the user is logged in (`loggedIn` == 1).
-   **TODO 9**: If logged in, check if the user is enrolled in the "in28Minutes" course (`enrolled` == 1).
-   **TODO 10**: If enrolled, return the welcome message: `"Welcome to the in28Minutes Course!"`.
-   **TODO 11**: If not enrolled, return a message asking the user to enroll: `"Please enroll in the in28Minutes course."`.
-   **TODO 12**: If not logged in, return a message asking the user to log in: `"Please log in to Udemy."`.

After implementing the above tasks, the application should correctly display the appropriate response based on the user's input.


### Output Format

The output is a single string based on the user's input.

-   If the user is logged in and enrolled in the course, the output is: `"Welcome to the in28Minutes Course!"`.
-   If the user is logged in but not enrolled, the output is: `"Please enroll in the in28Minutes course."`.
-   If the user is not logged in, the output is: `"Please log in to Udemy."`.

**Example:**

```
Welcome to the in28Minutes Course!
```

or

```
Please enroll in the in28Minutes course.
```

or

```
Please log in to Udemy.
```


## Hints

1.  Use a `Scanner` object to read input from the console.
2.  Prompt the user to input their login and enrollment status using `nextInt()`.
3.  Call the `processUserInput` method and store the result in a variable.
4.  Print the result to the console.
5.  Close the `Scanner` object.
6.  Implement the `processUserInput` method with the given parameters.
7.  Use conditional statements (`if`, `else`) to determine the appropriate response.
8.  Return the corresponding response string based on the user's input.


## Solution Explanation

We will implement the `UdemyCourseAccess` class, which will prompt the user for their login and enrollment status, process the input, and display the appropriate response. The `processUserInput` method will contain the logic to determine the response based on the input.

Here's a step-by-step explanation of the solution:

1.  Create a `Scanner` object to read input from the console.

```
Scanner scanner = new Scanner(System.in);
```

2.  Prompt the user to enter their login status and store the input in the `loggedIn` variable.

```
System.out.print("Are you logged in? (1 for yes, 0 for no): ");
int loggedIn = scanner.nextInt();
```

3.  Prompt the user to enter their enrollment status and store the input in the `enrolled` variable.

```
System.out.print("Are you enrolled in the in28Minutes course? (1 for yes, 0 for no): ");
int enrolled = scanner.nextInt();
```

4.  Call the `processUserInput` method with the `loggedIn` and `enrolled` values, and store the result in the `response` variable.

```
String response = processUserInput(loggedIn, enrolled);
```

5.  Print the response to the console.

```
System.out.println(response);
```

6.  Close the `Scanner` object to avoid resource leaks.

```
scanner.close();
``` 

7.  Implement the `processUserInput` method that takes `loggedIn` and `enrolled` as parameters and returns a `String` response.

```
public static String processUserInput(int loggedIn, int enrolled) {
```

8.  Use conditional statements (`if`, `else`) to determine the appropriate response.

```
if (loggedIn == 1) {
    if (enrolled == 1) {
        return "Welcome to the in28Minutes Course!";
    } else {
        return "Please enroll in the in28Minutes course.";
    }
} else {
    return "Please log in to Udemy.";
}
```

The complete `UdemyCourseAccess` class will look like this:

```
import java.util.Scanner;

public class UdemyCourseAccess {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Are you logged in? (1 for yes, 0 for no): ");
        int loggedIn = scanner.nextInt();

        System.out.print("Are you enrolled in the in28Minutes course? (1 for yes, 0 for no): ");
        int enrolled = scanner.nextInt();

        String response = processUserInput(loggedIn, enrolled);
        System.out.println(response);

        scanner.close();
    }

    public static String processUserInput(int loggedIn, int enrolled) {
        if (loggedIn == 1) {
            if (enrolled == 1) {
                return "Welcome to the in28Minutes Course!";
            } else {
                return "Please enroll in the in28Minutes course.";
            }
        } else {
            return "Please log in to Udemy.";
        }
    }
}
```

This solution will correctly display the appropriate response based on the user's input for login and enrollment status.




## Student File

  

  

  

**UdemyCourseAccess.java**

  

  

  

```
import java.util.Scanner;

public class UdemyCourseAccess {

    public static void main(String[] args) {
        // TODO: 1. Create a new Scanner object to read input from the console.
        

        // TODO: 2. Prompt the user to enter their login status, and store the input in the loggedIn variable.
        System.out.print("Are you logged in? (1 for yes, 0 for no): ");
        int loggedIn; 

        // TODO: 3. Prompt the user to enter their enrollment status, and store the input in the enrolled variable.
        System.out.print("Are you enrolled in the in28Minutes course? (1 for yes, 0 for no): ");
        int enrolled;

        // TODO: 4. Call the processUserInput method with the loggedIn and enrolled values, and store the result in the response variable.
        String response;

        // TODO: 5. Print the response to the console.
        System.out.println(response);

        // TODO: 6. Close the scanner to avoid resource leaks.
        
    }

    // 7. Implement the processUserInput method that takes loggedIn and enrolled as parameters and returns a String response.
    public static String processUserInput(int loggedIn, int enrolled) {
        // TODO: Implement the logic to return the appropriate response based on loggedIn and enrolled values.
        
        // 8. Check if the user is logged in (loggedIn == 1).

            // 9. If logged in, check if the user is enrolled in the in28Minutes course (enrolled == 1).

                // 10. If enrolled, return the welcome message.

                // 11. If not enrolled, return a message asking the user to enroll.

        // 12. If not logged in, return a message asking the user to log in.
        
        return ""; // Replace this line with your logic.
    }
}

```

  

  

  

  

## Solution File

  

  

  

**UdemyCourseAccess.java**
  

```
import java.util.Scanner;

public class UdemyCourseAccess {

    public static void main(String[] args) {
        // 1. Create a new Scanner object to read input from the console.
        Scanner scanner = new Scanner(System.in);

        // 2. Prompt the user to enter their login status, and store the input in the loggedIn variable.
        System.out.print("Are you logged in? (1 for yes, 0 for no): ");
        int loggedIn = scanner.nextInt();

        // 3. Prompt the user to enter their enrollment status, and store the input in the enrolled variable.
        System.out.print("Are you enrolled in the in28Minutes course? (1 for yes, 0 for no): ");
        int enrolled = scanner.nextInt();

        // 4. Call the processUserInput method with the loggedIn and enrolled values, and store the result in the response variable.
        String response = processUserInput(loggedIn, enrolled);

        // 5. Print the response to the console.
        System.out.println(response);

        // 6. Close the scanner to avoid resource leaks.
        scanner.close();
    }

    // 7. Implement the processUserInput method that takes loggedIn and enrolled as parameters and returns a String response.
    public static String processUserInput(int loggedIn, int enrolled) {
        // 8. Check if the user is logged in (loggedIn == 1).
        if (loggedIn == 1) {
            // 9. If logged in, check if the user is enrolled in the in28Minutes course (enrolled == 1).
            if (enrolled == 1) {
                // 10. If enrolled, return the welcome message.
                return "Welcome to the in28Minutes Course!";
            } else {
                // 11. If not enrolled, return a message asking the user to enroll.
                return "Please enroll in the in28Minutes course.";
            }
        } else {
            // 12. If not logged in, return a message asking the user to log in.
            return "Please log in to Udemy.";
        }
    }
}


```

  

  

  

## Evaluation File

  

  

**Evaluate.java**

  

  

  

```

import org.junit.jupiter.api.Test;
import java.util.logging.Logger;
import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {

    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void testLoggedInAndEnrolled() {
        String expected = "Welcome to the in28Minutes Course!";
        String actual = UdemyCourseAccess.processUserInput(1, 1);
        LOGGER.info("Expected: " + expected + ", Actual: " + actual);
        assertEquals(expected, actual, "Failed: Logged in and enrolled test");
    }

    @Test
    public void testLoggedInNotEnrolled() {
        String expected = "Please enroll in the in28Minutes course.";
        String actual = UdemyCourseAccess.processUserInput(1, 0);
        LOGGER.info("Expected: " + expected + ", Actual: " + actual);
        assertEquals(expected, actual, "Failed: Logged in but not enrolled test");
    }

    @Test
    public void testNotLoggedIn() {
        String expected = "Please log in to Udemy.";
        String actual = UdemyCourseAccess.processUserInput(0, 0);
        LOGGER.info("Expected: " + expected + ", Actual: " + actual);
        assertEquals(expected, actual, "Failed: Not logged in test");
    }
}

```
=======

