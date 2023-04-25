

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

## Output Format

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


