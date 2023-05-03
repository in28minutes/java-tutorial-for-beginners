## Exercise 1: Vowel Extraction from a String

You are given a partial implementation of a `VowelPrinter` class. Your task is to complete the `isVowel` method and the `main` method to achieve the following functionality:

1.  Read a string input from the user.
2.  Iterate through the characters of the string using a `while` loop.
3.  Check if a character is a vowel (a, e, i, o, or u) using the `isVowel` method.
4.  Print the vowel characters in the order they appear in the input string.

### Input Format

-   A single line containing a string (1 <= |input| <= 1000) consisting of alphanumeric characters and spaces.

### Output Format

-   A single line containing the vowels from the input string in the order they appear.

### Instructions

1.  Implement the `isVowel` method to check if a given character is a vowel. Convert the character to lowercase and compare it to the vowel characters (a, e, i, o, or u).
    
2.  In the `main` method, read a string from the user using the `Scanner` object and store it in the `input` variable. Close the `Scanner` object after reading the input.
    
3.  Initialize an `index` variable with the value `0`.
    
4.  Use a `while` loop to iterate through the characters of the input string. The loop should continue until the `index` is equal to the length of the input string.
    
5.  Inside the loop, get the character at the current `index` of the input string using the `charAt` method.
    
6.  Check if the character is a vowel using the `isVowel` method. If it is a vowel, print the character.
    
7.  Increment the `index` variable by `1`.
    

Use the provided student code as a starting point, and complete the `isVowel` method and the `main` method according to the instructions.

### Example

Input:

```
Programming is fun!
```

Output:

```
oaiu
```

In the input string "Programming is fun!", the vowels are 'o', 'a', 'i', and 'u', which are printed in the order they appear.



## Hints

1.  In the `isVowel` method, use `Character.toLowerCase` to convert the input character to lowercase before comparing it to the vowel characters.
2.  To compare the character with vowel characters, use the logical OR operator (`||`) to check if the character is equal to any of the vowel characters (a, e, i, o, or u).
3.  In the `main` method, use the `Scanner` object to read the input string and close the scanner after reading the input.
4.  Create a `while` loop with the condition `index < input.length()`.
5.  Inside the loop, use the `charAt` method to get the character at the current index from the input string.
6.  Call the `isVowel` method to check if the character is a vowel, and print it if the method returns `true`.
7.  Increment the `index` variable by 1 to move to the next character in the input string.

## Solution Explanation

In this solution, we implement the `VowelPrinter` class by completing the `isVowel` method and the `main` method as follows:

1.  **Implement the `isVowel` method**: Convert the input character to lowercase using `Character.toLowerCase` and then check if the character is equal to any of the vowel characters (a, e, i, o, or u) using the logical OR operator (`||`).

```
public static boolean isVowel(char ch) {
    ch = Character.toLowerCase(ch);
    return ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u';
}
```

2.  **Read the input string**: In the `main` method, use a `Scanner` object to read the input string and store it in the `input` variable. Close the `Scanner` object after reading the input.

```
Scanner scanner = new Scanner(System.in); 
String input = scanner.nextLine();
scanner.close();
```

3.  **Initialize the index variable**: Create an `index` variable with the value `0`.

```
int index = 0;
```

4.  **Iterate through the characters**: Use a `while` loop with the condition `index < input.length()` to iterate through the characters of the input string.

```
while (index < input.length()) {
    // Loop body
}
```

5.  **Get the character**: Inside the loop, use the `charAt` method to get the character at the current index from the input string.

```
char ch = input.charAt(index);
```

6.  **Check if the character is a vowel**: Call the `isVowel` method to check if the character is a vowel. If the method returns `true`, print the character.

```
if (isVowel(ch)) {
    System.out.print(ch);
}
```

7.  **Increment the index**: Increment the `index` variable by 1 to move to the next character in the input string.

```
index++;
```

With these steps implemented, the `VowelPrinter` class is now complete. The program will read the input string and print the vowels in the order they appear.

**Full Solution Code :**

```
import java.util.Scanner;

public class VowelPrinter {

    public static boolean isVowel(char ch) {
        // Convert the input character to lowercase
        ch = Character.toLowerCase(ch);
        // Check if the character is a vowel (a, e, i, o, or u) and return the result
        return ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u';
    }

    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner scanner = new Scanner(System.in); 
        // Read the input string from the user
        String input = scanner.nextLine();
        // Close the scanner object
        scanner.close();
        // Initialize an index variable with the value 0
        int index = 0;
        
        // Use a while loop to iterate through the characters of the input string
        while (index < input.length()) {
            // Get the character at the current index from the input string
            char ch = input.charAt(index);
            // Check if the character is a vowel using the isVowel method
            if (isVowel(ch)) {
                // If the character is a vowel, print it
                System.out.print(ch);
            }
            // Increment the index variable by 1 to move to the next character
            index++;
        }
    }
}

```

## Student File

```

import java.util.Scanner;

public class VowelPrinter {

    public static boolean isVowel(char ch) {
        // TODO: Convert the input character to lowercase
        // TODO: Check if the character is a vowel (a, e, i, o, or u)
        // TODO: Return true if the character is a vowel, otherwise return false
    }

    public static void main(String[] args) {
        // Create a Scanner object to read input from the user
        Scanner scanner = new Scanner(System.in); 
        // Read the input string from the user
        String input = scanner.nextLine();
        // Close the scanner object
        scanner.close();
        // Initialize an index variable with the value 0
        int index = 0;
        
        // TODO: Use a while loop to iterate through the characters of the input string
        // TODO: Inside the loop, get the character at the current index
        // TODO: Check if the character is a vowel using the isVowel method
        // TODO: If the character is a vowel, print it
        // TODO: Increment the index variable by 1
    }
}


```

## Solution File

```

    import java.util.Scanner;

    public class VowelPrinter {

        public static boolean isVowel(char ch) {
            ch = Character.toLowerCase(ch);
            return ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u';
        }

        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in); 
            String input = scanner.nextLine();
            scanner.close();
            int index = 0;
            while (index < input.length()) {
                char ch = input.charAt(index);
                if (isVowel(ch)) {
                    System.out.print(ch);
                }
                index++;
            }
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
import java.io.PrintStream;
import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {

    private final ByteArrayOutputStream outContent = new ByteArrayOutputStream();
    private final PrintStream originalOut = System.out;
    private final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @BeforeEach
    public void setUpStreams() {
        System.setOut(new PrintStream(outContent));
    }

    @AfterEach
    public void restoreStreams() {
        System.setOut(originalOut);
    }

    @Test
    public void test_vowel_printer_empty_string() {
        System.setIn(new ByteArrayInputStream("\n".getBytes()));
        VowelPrinter.main(new String[]{});
        String actualOutput = outContent.toString().trim();
        String expectedOutput = "";
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
        assertEquals(expectedOutput, actualOutput, "Should return empty string for empty input");
    }

    @Test
    public void test_vowel_printer_no_vowels() {
        System.setIn(new ByteArrayInputStream("xyz\n".getBytes()));
        VowelPrinter.main(new String[]{});
        String actualOutput = outContent.toString().trim();
        String expectedOutput = "";
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
        assertEquals(expectedOutput, actualOutput, "Should return empty string for input with no vowels");
    }

    @Test
    public void test_vowel_printer_all_vowels() {
        System.setIn(new ByteArrayInputStream("aeiou\n".getBytes()));
        VowelPrinter.main(new String[]{});
        String actualOutput = outContent.toString().trim();
        String expectedOutput = "aeiou";
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
        assertEquals(expectedOutput, actualOutput, "Should return all vowels for input with all vowels");
    }

    @Test
    public void test_vowel_printer_mixed_input() {
        System.setIn(new ByteArrayInputStream("Hello World\n".getBytes()));
        VowelPrinter.main(new String[]{});
        String actualOutput = outContent.toString().trim();
        String expectedOutput = "eoo";
        logger.info("Actual Output: " + actualOutput);
        logger.info("Expected Output: " + expectedOutput);
        assertEquals(expectedOutput, actualOutput, "Should return all vowels in the input string");
    }
}


```






# Exercise 2 : Age Calculator using Java's LocalDate and Period classes

## Problem Statement

In this exercise, you are required to implement an `AgeCalculator` class that calculates a person's age based on their date of birth and the current date. The date of birth should be entered by the user in the format `YYYY-MM-DD`. You need to complete the `calculateAge` method.

### Instructions

1.  Import the `LocalDate` and `Period` classes from the `java.time` package.
2.  Complete the `calculateAge` method by implementing the logic to calculate a person's age based on their date of birth and the current date.
    -   Use the `LocalDate.parse()` method to convert the birthDate string into a LocalDate object.
    -   Check if the currentDate is before the date of birth using the `isBefore()` method. If it is, return -1 to indicate an error.
    -   Check if the date of birth is before a specific date (e.g., `1900-01-01`). If it is, return -1 to indicate an error.
    -   Use the `Period.between()` method to calculate the difference between the date of birth and the current date in years.
    -   Return the calculated age.

### Input Format

-   A string representing the user's date of birth in the format `YYYY-MM-DD`.

### Output Format

-   If the input is invalid, print an error message: "Invalid input. Please enter a valid date in the format YYYY-MM-DD."
-   If the input is valid, print the person's age: "Your age is: X", where X is the calculated age.

**Note**: Make sure to mention the `Period.between()`, `isBefore()`, and `LocalDate.parse()` methods in the instructions, as the student is not familiar with these methods.

### Example

**Input:**

```
Please enter your date of birth in YYYY-MM-DD format: 2000-05-01
```

**Output:**

```
Your age is: 23
```

**Explanation:** In this example, the user has entered their date of birth as `2000-05-01`. The current date is assumed to be `2023-05-03`. The difference between these two dates in years is 23 years. Hence, the output is "Your age is: 23".


## Hints

1.  Use `LocalDate.parse()` method to convert the birthDate string into a LocalDate object.
2.  Use `isBefore()` method to check if one date is before another date.
3.  Use `Period.between()` method to calculate the difference between two dates in years.
4.  Make sure to return -1 in case of invalid input (e.g., when the date of birth is in the future or before a specific date such as `1900-01-01`).
5.  In the `main` method, the code to read input, calculate the current date, and call the `calculateAge` method is already provided.

## Solution Explanation

Here is the step-by-step explanation of the solution:

1.  In the `calculateAge` method, first, we check if the `birthDate` string is null or empty. If it is, we return -1 to indicate an error.
    
    ```
    if (birthDate == null || birthDate.isEmpty()) {
        return -1;
    }
    ```
    
2.  Convert the `birthDate` string into a `LocalDate` object using the `LocalDate.parse()` method.
    
   ```
   LocalDate dob = LocalDate.parse(birthDate);
   ```
    
3.  Check if the `currentDate` is before the date of birth using the `isBefore()` method. If it is, return -1 to indicate an error.
    
   ```
   if (currentDate.isBefore(dob)) {
        return -1;
    }
```
    
4.  Check if the date of birth is before a specific date (e.g., `1900-01-01`). If it is, return -1 to indicate an error.
    
    ```
    if (dob.isBefore(LocalDate.of(1900, 1, 1))) {
        return -1;
    }
    ```
    
5.  Use the `Period.between()` method to calculate the difference between the date of birth and the current date in years.
    
   ```
   return Period.between(dob, currentDate).getYears();
   ```
    

The `main` method is already provided in the student code. It takes care of reading the input, calculating the current date, calling the `calculateAge` method, and printing the age or an error message based on the calculated age.

#### Here's the Full Solution Code:

```
import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;

public class AgeCalculator {

    public static int calculateAge(String birthDate, LocalDate currentDate) {
        // Check if birthDate is null or empty
        if (birthDate == null || birthDate.isEmpty()) {
            return -1;
        }
        
        // Convert birthDate string to LocalDate object
        LocalDate dob = LocalDate.parse(birthDate);
        
        // Check if currentDate is before the date of birth
        if (currentDate.isBefore(dob)) {
            return -1;
        }
        
        // Check if the date of birth is before a specific date (e.g., 1900-01-01)
        if (dob.isBefore(LocalDate.of(1900, 1, 1))) {
            return -1;
        }

        // Calculate the difference between dob and currentDate in years using Period.between() method
        return Period.between(dob, currentDate).getYears();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Please enter your date of birth in YYYY-MM-DD format: ");
        String birthDate = scanner.nextLine();
        scanner.close();

        // Get the current date
        LocalDate currentDate = LocalDate.now();
        
        // Calculate the age using the calculateAge method
        int age = calculateAge(birthDate, currentDate);
        
        // Print the age or an error message if age is negative
        if (age < 0) {
            System.out.println("Invalid input. Please enter a valid date in the format YYYY-MM-DD.");
        } else {
            System.out.println("Your age is: " + age);
        }
    }
}
```

I hope this helps! Let me know if you have any questions.


## Student File

```
import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;

public class AgeCalculator {

    public static int calculateAge(String birthDate, LocalDate currentDate) {
        // Write your code to calculate the age based on the birthDate and currentDate
        // You can use the Period.between() method to calculate the difference between two dates in years
        // Return -1 if the input is invalid
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Please enter your date of birth in YYYY-MM-DD format: ");
        String birthDate = scanner.nextLine();
        scanner.close();

        // Get the current date
        LocalDate currentDate = LocalDate.now();
        
        // Call the calculateAge method to calculate the age
        int age = calculateAge(birthDate, currentDate);
        
        // Print the age or an error message if age is negative
        if (age < 0) {
            System.out.println("Invalid input. Please enter a valid date in the format YYYY-MM-DD.");
        } else {
            System.out.println("Your age is: " + age);
        }
    }
}

```

## Solution code

```

   
import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;

public class AgeCalculator {

    public static int calculateAge(String birthDate, LocalDate currentDate) {
        if (birthDate == null || birthDate.isEmpty()) {
            return -1;
        }
        
        LocalDate dob = LocalDate.parse(birthDate);
        
        
        if (currentDate.isBefore(dob)) {
            return -1;
        }
        
        if (dob.isBefore(LocalDate.of(1900, 1, 1))) {
            return -1;
        }

        
        return Period.between(dob, currentDate).getYears();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Please enter your date of birth in YYYY-MM-DD format: ");
        String birthDate = scanner.nextLine();
        scanner.close();

        LocalDate currentDate = LocalDate.now();
        
        int age = calculateAge(birthDate, currentDate);
        
        if (age < 0) {
            System.out.println("Invalid input. Please enter a valid date in the format YYYY-MM-DD.");
        } else {
            System.out.println("Your age is: " + age);
        }
    }
}



```

## Evaluation File

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;
import static org.junit.jupiter.api.Assertions.assertNotEquals;
import java.time.LocalDate;
import java.util.logging.Logger;

public class Evaluate {
private final Logger logger = Logger.getLogger(Evaluate.class.getName());

@Test
public void test_valid_input(){
    LocalDate currentDate = LocalDate.of(2022, 10, 1);
    int age = AgeCalculator.calculateAge("2000-01-01", currentDate);
    assertEquals(22, age, "Should return correct age for valid input");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: " + 22);
}

@Test
public void test_invalid_input(){
    LocalDate currentDate = LocalDate.of(2022, 10, 1);
    int age = AgeCalculator.calculateAge("", currentDate);
    assertEquals(-1, age, "Should return -1 for empty input");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: " + -1);

    age = AgeCalculator.calculateAge(null, currentDate);
    assertEquals(-1, age, "Should return -1 for null input");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: " + -1);

    LocalDate futureDate = LocalDate.of(1999, 2, 1);
    age = AgeCalculator.calculateAge("2000-01-01", futureDate);
    assertEquals(-1, age, "Should return -1 for future date input");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: " + -1);
}

@Test
public void test_edge_cases(){
    LocalDate currentDate = LocalDate.of(2022, 10, 1);
    int age = AgeCalculator.calculateAge("2000-10-01", currentDate);
    assertEquals(22, age, "Should return correct age for edge case input (same birth date and current date)");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: " + 22);
    
    age = AgeCalculator.calculateAge("1900-01-01", currentDate);
    assertEquals(122, age, "Should return correct age for edge case input (very old birth date)");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: 122");

    age = AgeCalculator.calculateAge("1901-01-01", currentDate);
    assertEquals(121, age, "Should return correct age for edge case input (after 1900-01-01)");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: 121");

    age = AgeCalculator.calculateAge("1899-12-31", currentDate);
    assertEquals(-1, age, "Should not return correct age for edge case input (very old birth date)");
    logger.info("Actual Output: " + age);
    logger.info("Expected Output: -1");
    }
}

```