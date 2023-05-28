
# Exercise 1: Finding Duplicate Characters in a String using HashMap in Java

## Problem Statement

The given code defines a class `DuplicateCharFinder` which contains a method `findDuplicateChars()` to find the duplicate characters in a given input string using a `HashMap`. However, the method `findDuplicateChars()` is incomplete and needs to be implemented.

### Instructions

Please complete the implementation of the `findDuplicateChars()` method in the `DuplicateCharFinder` class.

1.  Iterate through the characters of the input string and add characters to the `charCountMap` with their counts.
2.  Iterate through the `charCountMap` and add characters with count > 1 to the `duplicateCharMap`.
3.  Return the `HashMap` object containing only duplicate characters.

### Steps to complete the implementation

1.  Initialize two `HashMap` objects: `charCountMap` and `duplicateCharMap`.
2.  Iterate through the characters of the input string using a for-each loop:
    -   If the `charCountMap` contains the character, increment its count in the map.
    -   If the `charCountMap` does not contain the character, add it to the map with a count of 1.
3.  Iterate through the `charCountMap` using a for-each loop:
    -   If the count of a character in the `charCountMap` is greater than 1, add it to the `duplicateCharMap` with its count.
4.  Return the `duplicateCharMap`.


### Example

**Input:**

```
Enter a string: programming
```

**Output:**

```
Duplicate characters in the input string:
r: 2
g: 2
m: 2
```

**Input:**

```
Enter a string: hello world
```

**Output:**

```
Duplicate characters in the input string:
l: 3
o: 2
```


## Hints

1.  To find duplicate characters in a string, you need to keep track of the count of each character.
2.  Use a `HashMap` to store the characters and their counts.
3.  Iterate through the characters of the input string and add them to the `HashMap`.
4.  While adding the characters to the `HashMap`, check if the character is already present in the map or not. If it's present, increment the count. If it's not present, add the character to the map with a count of 1.
5.  After adding all the characters to the `HashMap`, iterate through the map and add only those characters to a new `HashMap` which have a count greater than 1.
6.  Return the new `HashMap` containing only the duplicate characters.
7.  Use a Scanner object to read the input string from the user.
8.  Handle the case when no duplicate characters are found in the input string.



## Solution Explanation

The given problem requires us to find duplicate characters in a string. We can solve this problem using a `HashMap` to store the characters and their counts.

We first initialize two `HashMap` objects: `charCountMap` and `duplicateCharMap`. We then iterate through the characters of the input string and add them to the `charCountMap`. While adding the characters, we check if the character is already present in the `charCountMap` or not. If it's present, we increment the count of the character. If it's not present, we add the character to the `charCountMap` with a count of 1.

Once we have added all the characters to the `charCountMap`, we iterate through the map and add only those characters to the `duplicateCharMap` which have a count greater than 1. Finally, we return the `duplicateCharMap` which contains only the duplicate characters.

In the `main()` method, we use a `Scanner` object to read the input string from the user. We then call the `findDuplicateChars()` method and store the result in the `resultMap`. We then iterate through the `resultMap` and print the duplicate characters along with their counts. If no duplicate characters are found in the input string, we print a message saying "No duplicate characters found."

Here's the complete code solution:

```
import java.util.HashMap;
import java.util.Map.Entry;
import java.util.Scanner;

public class DuplicateCharFinder {

    public static HashMap<Character, Integer> findDuplicateChars(String input) {
        HashMap<Character, Integer> charCountMap = new HashMap<>();
        HashMap<Character, Integer> duplicateCharMap = new HashMap<>();

        // Iterate through the characters of the input string and add them to the charCountMap
        for (char c : input.toCharArray()) {
            if (charCountMap.containsKey(c)) {
                charCountMap.put(c, charCountMap.get(c) + 1);
            } else {
                charCountMap.put(c, 1);
            }
        }

        // Iterate through the charCountMap and add only the duplicate characters to the duplicateCharMap
        for (Entry<Character, Integer> entry : charCountMap.entrySet()) {
            if (entry.getValue() > 1) {
                duplicateCharMap.put(entry.getKey(), entry.getValue());
            }
        }

        // Return the HashMap object containing only duplicate characters
        return duplicateCharMap;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String input = scanner.nextLine();

        // Call the findDuplicateChars method and store the result in a HashMap
        HashMap<Character, Integer> resultMap = findDuplicateChars(input);

        // Print the duplicate characters along with their counts
        System.out.println("Duplicate characters in the input string:");
        boolean hasDuplicate = false;
        for (Entry<Character, Integer> entry : resultMap.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
            hasDuplicate = true;
        }

        // Handle the case when no duplicate characters are found in the input string
        if (!hasDuplicate) {
            System.out.println("No duplicate characters found.");
        }

        scanner.close();
    }
}
```


## Student File

```
import java.util.HashMap;
import java.util.Map.Entry;
import java.util.Scanner;

public class DuplicateCharFinder {

    public static HashMap<Character, Integer> findDuplicateChars(String input) {
        HashMap<Character, Integer> charCountMap = new HashMap<>();
        HashMap<Character, Integer> duplicateCharMap = new HashMap<>();

        // TODO: Write your code

        // Return the HashMap object containing only duplicate characters
        return duplicateCharMap;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String input = scanner.nextLine();

        // Call the findDuplicateChars method and store the result in a HashMap
        HashMap<Character, Integer> resultMap = findDuplicateChars(input);

        // Print the duplicate characters along with their counts
        System.out.println("Duplicate characters in the input string:");
        boolean hasDuplicate = false;
        for (Entry<Character, Integer> entry : resultMap.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
            hasDuplicate = true;
        }

        // Handle the case when no duplicate characters are found in the input string
        if (!hasDuplicate) {
            System.out.println("No duplicate characters found.");
        }

        scanner.close();
    }
}

```


## Solution File

```
import java.util.HashMap;
import java.util.Map.Entry;
import java.util.Scanner;

public class DuplicateCharFinder {

    public static HashMap<Character, Integer> findDuplicateChars(String input) {
        HashMap<Character, Integer> charCountMap = new HashMap<>();
        HashMap<Character, Integer> duplicateCharMap = new HashMap<>();

        // Iterate through the characters of the input string and add them to the charCountMap
        for (char c : input.toCharArray()) {
            if (charCountMap.containsKey(c)) {
                charCountMap.put(c, charCountMap.get(c) + 1);
            } else {
                charCountMap.put(c, 1);
            }
        }

        // Iterate through the charCountMap and add only the duplicate characters to the duplicateCharMap
        for (Entry<Character, Integer> entry : charCountMap.entrySet()) {
            if (entry.getValue() > 1) {
                duplicateCharMap.put(entry.getKey(), entry.getValue());
            }
        }

        // Return the HashMap object containing only duplicate characters
        return duplicateCharMap;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a string: ");
        String input = scanner.nextLine();

        // Call the findDuplicateChars method and store the result in a HashMap
        HashMap<Character, Integer> resultMap = findDuplicateChars(input);

        // Print the duplicate characters along with their counts
        System.out.println("Duplicate characters in the input string:");
        boolean hasDuplicate = false;
        for (Entry<Character, Integer> entry : resultMap.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
            hasDuplicate = true;
        }

        // Handle the case when no duplicate characters are found in the input string
        if (!hasDuplicate) {
            System.out.println("No duplicate characters found.");
        }

        scanner.close();
    }
}

```


## Evaluation File

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;
import java.util.HashMap;
import java.util.logging.Logger;

public class Evaluate {

    private static final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void test_find_duplicate_chars_with_duplicates() {
        String input = "hello world";
        HashMap<Character, Integer> expected = new HashMap<>();
        expected.put('l', 3);
        expected.put('o', 2);
        HashMap<Character, Integer> actual = DuplicateCharFinder.findDuplicateChars(input);
        logger.info("Expected: " + expected + ", Actual: " + actual);
        assertEquals(expected, actual, "Should return the correct duplicate characters and their counts");
    }

    @Test
    public void test_find_duplicate_chars_without_duplicates() {
        String input = "abcdefg";
        HashMap<Character, Integer> expected = new HashMap<>();
        HashMap<Character, Integer> actual = DuplicateCharFinder.findDuplicateChars(input);
        logger.info("Expected: " + expected + ", Actual: " + actual);
        assertEquals(expected, actual, "Should return an empty HashMap when there are no duplicate characters");
    }

    @Test
    public void test_find_duplicate_chars_with_empty_input() {
        String input = "";
        HashMap<Character, Integer> expected = new HashMap<>();
        HashMap<Character, Integer> actual = DuplicateCharFinder.findDuplicateChars(input);
        logger.info("Expected: " + expected + ", Actual: " + actual);
        assertEquals(expected, actual, "Should return an empty HashMap when the input string is empty");
    }
}

```