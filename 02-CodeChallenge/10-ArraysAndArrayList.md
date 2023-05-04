# Exercise 1: Merging Two Integer Arrays

## Problem Statement

You are given two integer arrays. Your task is to implement a program that merges these two arrays into a single array while preserving the order of the elements from the input arrays. The program should use the `mergeArrays` method to merge the input arrays.

### Instructions

1.  Read the size and elements of the first array from the user.
2.  Read the size and elements of the second array from the user.
3.  Implement the `mergeArrays` method that takes two integer arrays as input and returns a new integer array containing all the elements of both input arrays. The elements in the returned array should preserve their order from the input arrays.
4.  Call the `mergeArrays` method with the input arrays and store the result in a variable called `mergedArray`.
5.  Print the merged array.

### Input

-   The size of the first array (1 <= size1 <= 10^3)
-   The elements of the first array (-10^3 <= array1[i] <= 10^3)
-   The size of the second array (1 <= size2 <= 10^3)
-   The elements of the second array (-10^3 <= array2[i] <= 10^3)

### Output

-   The merged array containing all the elements from both input arrays, preserving their order.

### Example

Input:

```
Enter the size of the first array: 3
Enter the elements of the first array:
1 2 3
Enter the size of the second array: 4
Enter the elements of the second array:
4 5 6 7
```

Output:

```
Merged array: [1, 2, 3, 4, 5, 6, 7]
```

## Hints

**Hint 1:** Start by initializing the merged array with the combined length of both input arrays.

**Hint 2:** Use two separate loops or a single loop with two indices to iterate over both input arrays and copy their elements into the merged array.

**Hint 3:** Keep track of the index in the merged array, and update it after adding an element from one of the input arrays.

**Hint 4:** Be sure to return the merged array at the end of the `mergeArrays` method.


## Solution Explanation

In the provided solution, we implement the `mergeArrays` method to merge two given integer arrays, preserving the order of their elements. Here's a step-by-step explanation of the solution:

1.  We first create a new `mergedArray` with the combined length of both input arrays: `int[] mergedArray = new int[array1.length + array2.length];`

```
public static int[] mergeArrays(int[] array1, int[] array2) {
    int[] mergedArray = new int[array1.length + array2.length];
    // ...
}
```
2.  Next, we initialize an index variable `i` to keep track of the position in the merged array.

```
public static int[] mergeArrays(int[] array1, int[] array2) {
    int[] mergedArray = new int[array1.length + array2.length];
    int i = 0;
    // ...
}
```
3.  We use a `for` loop to iterate over the first input array (`array1`) and copy its elements into the merged array. We increment the index `i` after adding each element.

```
public static int[] mergeArrays(int[] array1, int[] array2) {
    int[] mergedArray = new int[array1.length + array2.length];
    int i = 0;

    for (int element : array1) {
        mergedArray[i++] = element;
    }
    // ...
}
```

4.  Similarly, we use another `for` loop to iterate over the second input array (`array2`) and copy its elements into the merged array, again incrementing the index `i` after adding each element.

```
public static int[] mergeArrays(int[] array1, int[] array2) {
    int[] mergedArray = new int[array1.length + array2.length];
    int i = 0;

    for (int element : array1) {
        mergedArray[i++] = element;
    }

    for (int element : array2) {
        mergedArray[i++] = element;
    }
    // ...
}
```

5.  Finally, we return the `mergedArray` containing all the elements from both input arrays.

```
public static int[] mergeArrays(int[] array1, int[] array2) {
    int[] mergedArray = new int[array1.length + array2.length];
    int i = 0;

    for (int element : array1) {
        mergedArray[i++] = element;
    }

    for (int element : array2) {
        mergedArray[i++] = element;
    }

    return mergedArray;
}
```

This solution successfully merges the two input arrays while maintaining the order of their elements.


**Full Solution Code:**
```
import java.util.Arrays;
import java.util.Scanner;

public class MergeArrays {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the size of the first array: ");
        int size1 = scanner.nextInt();
        int[] array1 = new int[size1];

        System.out.println("Enter the elements of the first array: ");
        for (int i = 0; i < size1; i++) {
            array1[i] = scanner.nextInt();
        }

        System.out.print("Enter the size of the second array: ");
        int size2 = scanner.nextInt();
        int[] array2 = new int[size2];

        System.out.println("Enter the elements of the second array: ");
        for (int i = 0; i < size2; i++) {
            array2[i] = scanner.nextInt();
        }

        int[] mergedArray = mergeArrays(array1, array2);

        System.out.println("Merged array: " + Arrays.toString(mergedArray));

        scanner.close();
    }

    // Merges two integer arrays into one array while preserving their order
    public static int[] mergeArrays(int[] array1, int[] array2) {
        // Create a new array with the combined length of both input arrays
        int[] mergedArray = new int[array1.length + array2.length];

        // Initialize an index variable to keep track of the position in the merged array
        int i = 0;

        // Iterate over the first input array and copy its elements into the merged array
        for (int element : array1) {
            mergedArray[i++] = element;
        }

        // Iterate over the second input array and copy its elements into the merged array
        for (int element : array2) {
            mergedArray[i++] = element;
        }

        // Return the merged array containing all the elements from both input arrays
        return mergedArray;
    }
}

```

## Student File

```
import java.util.Arrays;
import java.util.Scanner;

public class MergeArrays {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the size of the first array: ");
        int size1 = scanner.nextInt();
        int[] array1 = new int[size1];

        System.out.println("Enter the elements of the first array: ");
        for (int i = 0; i < size1; i++) {
            array1[i] = scanner.nextInt();
        }

        System.out.print("Enter the size of the second array: ");
        int size2 = scanner.nextInt();
        int[] array2 = new int[size2];

        System.out.println("Enter the elements of the second array: ");
        for (int i = 0; i < size2; i++) {
            array2[i] = scanner.nextInt();
        }

        int[] mergedArray = mergeArrays(array1, array2);

        System.out.println("Merged array: " + Arrays.toString(mergedArray));

        scanner.close();
    }
    
    // TODO: Implement the mergeArrays method that takes two integer arrays as input
    // TODO: The method should return a new integer array containing all the elements of both input arrays
    // TODO: The elements in the returned array should preserve their order from the input arrays
    public static int[] mergeArrays(int[] array1, int[] array2) {
        // You should create a new array with the combined length of both input arrays
        // Then, iterate over the first input array and copy its elements into the new merged array
        // Next, iterate over the second input array and copy its elements into the merged array
        // Finally, return the merged array containing all the elements from both input arrays
    }
}

```

## Solution File

```

import java.util.Arrays;
import java.util.Scanner;

public class MergeArrays {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the size of the first array: ");
        int size1 = scanner.nextInt();
        int[] array1 = new int[size1];

        System.out.println("Enter the elements of the first array: ");
        for (int i = 0; i < size1; i++) {
            array1[i] = scanner.nextInt();
        }

        System.out.print("Enter the size of the second array: ");
        int size2 = scanner.nextInt();
        int[] array2 = new int[size2];

        System.out.println("Enter the elements of the second array: ");
        for (int i = 0; i < size2; i++) {
            array2[i] = scanner.nextInt();
        }

        int[] mergedArray = mergeArrays(array1, array2);

        System.out.println("Merged array: " + Arrays.toString(mergedArray));

        scanner.close();
    }

    public static int[] mergeArrays(int[] array1, int[] array2) {
        int[] mergedArray = new int[array1.length + array2.length];

        int i = 0;

        for (int element : array1) {
            mergedArray[i++] = element;
        }

        for (int element : array2) {
            mergedArray[i++] = element;
        }

        return mergedArray;
    }
}


```

## Evaluation File

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertArrayEquals;

import java.util.Arrays;
import java.util.logging.Logger;

public class Evaluate {

    private final static Logger logger = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void test_merge_empty_arrays() {
        int[] array1 = {};
        int[] array2 = {};
        int[] expected = {};
        int[] actual = MergeArrays.mergeArrays(array1, array2);
        logger.info("Expected: " + Arrays.toString(expected) + ", Actual: " + Arrays.toString(actual));
        assertArrayEquals(expected, actual, "Should return an empty array when both input arrays are empty");
    }

    @Test
    public void test_merge_one_empty_array() {
        int[] array1 = {1, 2, 3};
        int[] array2 = {};
        int[] expected = {1, 2, 3};
        int[] actual = MergeArrays.mergeArrays(array1, array2);
        logger.info("Expected: " + Arrays.toString(expected) + ", Actual: " + Arrays.toString(actual));
        assertArrayEquals(expected, actual, "Should return the non-empty array when one input array is empty");
    }

    @Test
    public void test_merge_arrays() {
        int[] array1 = {1, 3, 5};
        int[] array2 = {2, 4, 6};
        int[] expected = {1, 3, 5, 2, 4, 6};
        int[] actual = MergeArrays.mergeArrays(array1, array2);
        logger.info("Expected: " + Arrays.toString(expected) + ", Actual: " + Arrays.toString(actual));
        assertArrayEquals(expected, actual, "Should merge two arrays in ascending order");
    }

    @Test
    public void test_merge_arrays_with_duplicates() {
        int[] array1 = {1, 3, 5, 5, 7};
        int[] array2 = {2, 4, 5, 6, 8};
        int[] expected = {1, 3, 5, 5, 7, 2, 4, 5, 6, 8};
        int[] actual = MergeArrays.mergeArrays(array1, array2);
        logger.info("Expected: " + Arrays.toString(expected) + ", Actual: " + Arrays.toString(actual));
        assertArrayEquals(expected, actual, "Should merge two arrays in ascending order and include duplicates");
    }
}


```