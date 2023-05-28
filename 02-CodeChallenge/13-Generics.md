# Exercise 1: Implementing and Using a Generic Pair Class

## Problem Statement

In this exercise, you need to complete the implementation of a simple generic class called `GenericPair` that can store a pair of objects with different types. You will also use this class to create instances and print the pairs.

You have been given an incomplete code file, and your task is to fill in the missing parts of the code.

### Instructions

1.  Complete the constructor of the `GenericPair` class by assigning the constructor arguments to the corresponding instance variables.
2.  Implement the `getKey()` method that returns the `key` instance variable.
3.  Implement the `getValue()` method that returns the `value` instance variable.

### Example Usage

After completing the code, the `GenericPair` class should be used as follows:

```
GenericPair<String, Integer> pair1 = new GenericPair<>("One", 1);
System.out.println("Key: " + pair1.getKey() + ", Value: " + pair1.getValue());
// Output: Key: One, Value: 1

GenericPair<Integer, Double> pair2 = new GenericPair<>(2, 2.0);
System.out.println("Key: " + pair2.getKey() + ", Value: " + pair2.getValue()); 
// Output: Key: 2, Value: 2.0
```

After the student completes the implementation, the example output should look like this:

```
Key: One, Value: 1
Key: 2, Value: 2.0
```

## Hints

1.  **Constructor**: Assign the constructor arguments to the instance variables `key` and `value` in the `GenericPair` class.

```
this.key = key;
this.value = value;
```

2.  **getKey() method**: Return the `key` instance variable.


`return key;` 

3.  **getValue() method**: Return the `value` instance variable.


`return value;`

## Solution Explanation

The solution involves completing the implementation of the `GenericPair` class, which is a generic class that stores a pair of objects with different types. The class has two type parameters `K` and `V`, and two private instance variables called `key` and `value` of type `K` and `V` respectively.

1.  **Constructor**: The constructor takes two arguments, one of type `K` and another of type `V`. These arguments need to be assigned to the instance variables `key` and `value`. To do this, we use the `this` keyword, which refers to the current instance of the class:

```
this.key = key;
this.value = value;
```

2.  **getKey() method**: This method should return the `key` instance variable. It has a return type of `K` to match the type of the `key` instance variable:

`return key;` 

3.  **getValue() method**: This method should return the `value` instance variable. It has a return type of `V` to match the type of the `value` instance variable:

`return value;` 

After completing these steps, the `GenericPair` class can be used to store and retrieve pairs of objects with different types, as demonstrated in the example usage.


**Full Solution Code :**
```
public class GenericPairTest {
    public static void main(String[] args) {
        // Create a GenericPair object with String and Integer types
        GenericPair<String, Integer> pair1 = new GenericPair<>("One", 1);
        // Print the key and value of the pair1 object
        System.out.println("Key: " + pair1.getKey() + ", Value: " + pair1.getValue());
        // Output: Key: One, Value: 1

        // Create a GenericPair object with Integer and Double types
        GenericPair<Integer, Double> pair2 = new GenericPair<>(2, 2.0);
        // Print the key and value of the pair2 object
        System.out.println("Key: " + pair2.getKey() + ", Value: " + pair2.getValue());
        // Output: Key: 2, Value: 2.0
    }

    public static class GenericPair<K, V> {
        // Instance variables to store the key and value
        private K key;
        private V value;

        // Constructor to initialize the key and value
        public GenericPair(K key, V value) {
            this.key = key;
            this.value = value;
        }

        // Method to get the key
        public K getKey() {
            return key;
        }

        // Method to get the value
        public V getValue() {
            return value;
        }
    }
}

```

## Student Code File

```
public class GenericPairTest {
    public static void main(String[] args) {
        GenericPair<String, Integer> pair1 = new GenericPair<>("One", 1);
        System.out.println("Key: " + pair1.getKey() + ", Value: " + pair1.getValue());        
        // Output: Key: One, Value: 1

        GenericPair<Integer, Double> pair2 = new GenericPair<>(2, 2.0);
        System.out.println("Key: " + pair2.getKey() + ", Value: " + pair2.getValue()); 
        // Output: Key: 2, Value: 2.0
    }

    public static class GenericPair<K, V> {
        private K key;
        private V value;

        public GenericPair(K key, V value) {
            // TODO: Assign the key and value to the instance variables

        }

        public K getKey() {
            // TODO: Return the key
        }

        public V getValue() {
            // TODO: Return the value
        }
    }
}

```


## Solution File

```

public class GenericPairTest {
    public static void main(String[] args) {
        GenericPair<String, Integer> pair1 = new GenericPair<>("One", 1);
        System.out.println("Key: " + pair1.getKey() + ", Value: " + pair1.getValue());        
        // Output: Key: One, Value: 1

        GenericPair<Integer, Double> pair2 = new GenericPair<>(2, 2.0);
        System.out.println("Key: " + pair2.getKey() + ", Value: " + pair2.getValue()); 
       // Output: Key: 2, Value: 2.0
    }

    public static class GenericPair<K, V> {
        private K key;
        private V value;

        public GenericPair(K key, V value) {
            this.key = key;
            this.value = value;
        }

        public K getKey() {
            return key;
        }

        public V getValue() {
            return value;
        }
    }
}

```

## Evaluation File

```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;

import java.util.logging.Logger;

public class Evaluate {
    private static final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void test_generic_pair_string_integer(){
        GenericPairTest.GenericPair<String, Integer> pair = new GenericPairTest.GenericPair<>("One", 1);
        logger.info("Expected Key: One, Actual Key: " + pair.getKey());
        logger.info("Expected Value: 1, Actual Value: " + pair.getValue());
        assertEquals("One", pair.getKey(), "Key should be One");
        assertEquals(1, pair.getValue(), "Value should be 1");
    }

    @Test
    public void test_generic_pair_integer_double(){
        GenericPairTest.GenericPair<Integer, Double> pair = new GenericPairTest.GenericPair<>(2, 2.0);
        logger.info("Expected Key: 2, Actual Key: " + pair.getKey());
        logger.info("Expected Value: 2.0, Actual Value: " + pair.getValue());
        assertEquals(2, pair.getKey(), "Key should be 2");
        assertEquals(2.0, pair.getValue(), "Value should be 2.0");
    }
}
```