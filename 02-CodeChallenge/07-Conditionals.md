
# Month Name Printer

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

**Input:**

```
Enter the month number (1-12):
4
```

**Output:**

```
The name of month number 4 is April.
```

**Input:**

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