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