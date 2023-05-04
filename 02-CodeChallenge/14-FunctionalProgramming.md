# Exercise 1: SimpleCalculator: Implementing Basic Arithmetic Operations Using Lambda Expressions and Functional Interfaces


## Problem Statement

You are given an incomplete `SimpleCalculator` class that aims to perform basic arithmetic operations (addition, subtraction, and multiplication) using lambda expressions and a functional interface named `Calculator`. Your task is to complete the missing parts of the code.

### Instructions

1.  Define the lambda expressions for the following arithmetic operations:
    
    -   Addition
    -   Subtraction
    -   Multiplication
2.  Implement the `performCalculation` method that takes a `Calculator` object, two integer values `a` and `b`, and returns the result of the calculation.
    

### Steps

1.  Define the lambda expression for the addition operation. Replace the `null` value with a lambda expression that takes two integers `a` and `b` and returns the sum of the two numbers.
    
2.  Define the lambda expression for the subtraction operation. Replace the `null` value with a lambda expression that takes two integers `a` and `b` and returns the result of `a - b`.
    
3.  Define the lambda expression for the multiplication operation. Replace the `null` value with a lambda expression that takes two integers `a` and `b` and returns the result of `a * b`.
    
4.  Implement the `performCalculation` method. This method should accept a `Calculator` object and two integers `a` and `b`. It should return the result of the calculation performed by the `Calculator` object on `a` and `b`.

## Hints

1.  Lambda expressions are anonymous functions that can be assigned to functional interfaces. To define a lambda expression, use the following syntax: `(parameter1, parameter2) -> expression`.
    
2.  For the addition operation, the lambda expression should add the two input parameters and return the result.
    
3.  For the subtraction operation, the lambda expression should subtract the second input parameter from the first and return the result.
    
4.  For the multiplication operation, the lambda expression should multiply the two input parameters and return the result.
    
5.  The `performCalculation` method should call the `calculate` method of the given `Calculator` object with the input integers `a` and `b` and return the result of the calculation.


## Solution Explanation

The solution involves defining lambda expressions for the arithmetic operations (addition, subtraction, and multiplication) and implementing the `performCalculation` method to use the `Calculator` functional interface.

Here's the complete solution code with explanations:

```
public class SimpleCalculator {

    @FunctionalInterface
    public interface Calculator {
        int calculate(int a, int b);
    }

    public static void main(String[] args) {
        // Define the lambda expression for the addition operation
        Calculator addition = (a, b) -> a + b;

        // Define the lambda expression for the subtraction operation
        Calculator subtraction = (a, b) -> a - b;

        // Define the lambda expression for the multiplication operation
        Calculator multiplication = (a, b) -> a * b;

        // Test the calculator functionality
        System.out.println("Addition: " + performCalculation(addition, 5, 3)); // Output: 8
        System.out.println("Subtraction: " + performCalculation(subtraction, 5, 3)); // Output: 2
        System.out.println("Multiplication: " + performCalculation(multiplication, 5, 3)); // Output: 15
    }

    // Implement the performCalculation method
    public static int performCalculation(Calculator calculator, int a, int b) {
        return calculator.calculate(a, b);
    }
}
```

1.  Define the lambda expressions for the arithmetic operations:
    
    -   `Calculator addition = (a, b) -> a + b;` - The addition operation takes two integers `a` and `b` as input and returns their sum.
    -   `Calculator subtraction = (a, b) -> a - b;` - The subtraction operation takes two integers `a` and `b` as input and returns the result of `a - b`.
    -   `Calculator multiplication = (a, b) -> a * b;` - The multiplication operation takes two integers `a` and `b` as input and returns the result of `a * b`.
2.  Implement the `performCalculation` method:
    
    -   `public static int performCalculation(Calculator calculator, int a, int b)` - This method takes a `Calculator` object and two integers `a` and `b` as input.
    -   `return calculator.calculate(a, b);` - The method calls the `calculate` method of the given `Calculator` object with the input integers `a` and `b` and returns the result of the calculation.

By using lambda expressions and the functional interface `Calculator`, the solution provides a simple way to perform basic arithmetic operations with a flexible and reusable design.


## Student File

```
public class SimpleCalculator {

    @FunctionalInterface
    public interface Calculator {
        int calculate(int a, int b);
    }

    public static void main(String[] args) {
        // TODO: Define the lambda expression for the addition operation
        Calculator addition = null;

        // TODO: Define the lambda expression for the subtraction operation
        Calculator subtraction = null;

        // TODO: Define the lambda expression for the multiplication operation
        Calculator multiplication = null;

        // Test the calculator functionality
        System.out.println("Addition: " + performCalculation(addition, 5, 3)); // Output: 8
        System.out.println("Subtraction: " + performCalculation(subtraction, 5, 3)); // Output: 2
        System.out.println("Multiplication: " + performCalculation(multiplication, 5, 3)); // Output: 15
    }

    // TODO: Implement the performCalculation method
    public static int performCalculation(Calculator calculator, int a, int b) {
        return 0;
    }
}


```

## Solution File

```
public class SimpleCalculator {

    @FunctionalInterface
    public interface Calculator {
        int calculate(int a, int b);
    }

    public static void main(String[] args) {
        // Define the lambda expression for the addition operation
        Calculator addition = (a, b) -> a + b;

        // Define the lambda expression for the subtraction operation
        Calculator subtraction = (a, b) -> a - b;

        // Define the lambda expression for the multiplication operation
        Calculator multiplication = (a, b) -> a * b;

        // Test the calculator functionality
        System.out.println("Addition: " + performCalculation(addition, 5, 3)); // Output: 8
        System.out.println("Subtraction: " + performCalculation(subtraction, 5, 3)); // Output: 2
        System.out.println("Multiplication: " + performCalculation(multiplication, 5, 3)); // Output: 15
    }

    // Implement the performCalculation method
    public static int performCalculation(Calculator calculator, int a, int b) {
        return calculator.calculate(a, b);
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
    public void test_addition() {
        SimpleCalculator.Calculator addition = (a, b) -> a + b;
        int result = SimpleCalculator.performCalculation(addition, 5, 3);
        logger.info("Addition test: expected output: 8, actual output: " + result);
        assertEquals(8, result, "Addition test failed");
    }

    @Test
    public void test_subtraction() {
        SimpleCalculator.Calculator subtraction = (a, b) -> a - b;
        int result = SimpleCalculator.performCalculation(subtraction, 5, 3);
        logger.info("Subtraction test: expected output: 2, actual output: " + result);
        assertEquals(2, result, "Subtraction test failed");
    }

    @Test
    public void test_multiplication() {
        SimpleCalculator.Calculator multiplication = (a, b) -> a * b;
        int result = SimpleCalculator.performCalculation(multiplication, 5, 3);
        logger.info("Multiplication test: expected output: 15, actual output: " + result);
        assertEquals(15, result, "Multiplication test failed");
    }
}
```






# Exercise 2: COVID-19 Symptom Filter using Java Streams

## Problem Statement

You are tasked with creating a simple program to filter and display a list of COVID-19 symptoms. Given a list of symptoms with their names and a boolean flag indicating whether they are related to COVID-19, you must implement the following functionalities:

1.  Filter the list of symptoms to only include those that are COVID-19 symptoms.
2.  Print the COVID-19 symptoms.

### Instructions and Steps

1.  In the `main` method, use the `stream()` method and the `filter()` function to filter the list of symptoms to only include those that are COVID-19 symptoms. The `filter()` function should use the `isCovidSymptom()` method from the `Symptom` class to determine if a symptom is related to COVID-19.
2.  After filtering the symptoms, use the `collect()` method to collect the filtered symptoms into a new `List<Symptom>` object named `covidSymptoms`.
3.  To print the COVID-19 symptoms, use the `forEach()` method on the `covidSymptoms` list. Inside the `forEach()` method, use a lambda expression to print the name of each symptom using the `getName()` method from the `Symptom` class.

### Example

Input:

```
List<Symptom> symptoms = Arrays.asList(
    new Symptom("Fever", true),
    new Symptom("Dry Cough", true),
    new Symptom("Tiredness", true),
    new Symptom("Sore Throat", false),
    new Symptom("Headache", false),
    new Symptom("Loss of Taste or Smell", true),
    new Symptom("Difficulty Breathing", true)
);
```

Output:

```
COVID-19 Symptoms:
Fever
Dry Cough
Tiredness
Loss of Taste or Smell
Difficulty Breathing
```


## Hints

1.  Use the `stream()` method on the `symptoms` list to create a stream of symptoms.
2.  Apply the `filter()` function on the stream, and pass the `Symptom::isCovidSymptom` method reference as a predicate to filter COVID-19 symptoms.
3.  Collect the filtered symptoms into a new list using the `collect()` method and `Collectors.toList()` as an argument.
4.  Iterate over the `covidSymptoms` list using the `forEach()` method.
5.  Inside the `forEach()` method, use a lambda expression to print the name of each symptom using the `getName()` method from the `Symptom` class.


## Solution Explanation

In this solution, we'll use Java Streams to filter the list of symptoms and display only the COVID-19 related symptoms.

1.  First, we create a stream of symptoms using the `stream()` method on the `symptoms` list.

```
symptoms.stream()
```

2.  Next, we apply the `filter()` function on the stream, and pass the `Symptom::isCovidSymptom` method reference as a predicate to filter COVID-19 symptoms.

```
symptoms.stream()
    .filter(Symptom::isCovidSymptom)
``` 

3.  We then collect the filtered symptoms into a new list using the `collect()` method and `Collectors.toList()` as an argument.

```
List<Symptom> covidSymptoms = symptoms.stream()
    .filter(Symptom::isCovidSymptom)
    .collect(Collectors.toList());
 ```

4.  To print the COVID-19 symptoms, we iterate over the `covidSymptoms` list using the `forEach()` method.

```
covidSymptoms.forEach(symptom -> System.out.println(symptom.getName()));
```

5.  Inside the `forEach()` method, we use a lambda expression to print the name of each symptom using the `getName()` method from the `Symptom` class.


**Complete Solution:**

```
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class CovidSymptomChecker {
    public static void main(String[] args) {
        List<Symptom> symptoms = Arrays.asList(
            new Symptom("Fever", true),
            new Symptom("Dry Cough", true),
            new Symptom("Tiredness", true),
            new Symptom("Sore Throat", false),
            new Symptom("Headache", false),
            new Symptom("Loss of Taste or Smell", true),
            new Symptom("Difficulty Breathing", true)
        );

        List<Symptom> covidSymptoms = symptoms.stream()
            .filter(Symptom::isCovidSymptom)
            .collect(Collectors.toList());

        System.out.println("COVID-19 Symptoms:");
        covidSymptoms.forEach(symptom -> System.out.println(symptom.getName()));
    }

    public static class Symptom {
        private String name;
        private boolean isCovidSymptom;

        public Symptom(String name, boolean isCovidSymptom) {
            this.name = name;
            this.isCovidSymptom = isCovidSymptom;
        }

        public String getName() {
            return name;
        }

        public boolean isCovidSymptom() {
            return isCovidSymptom;
        }
    }
}
```

This code will output the following:

```
COVID-19 Symptoms:
Fever
Dry Cough
Tiredness
Loss of Taste or Smell
Difficulty Breathing
```


## Student File

```
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class CovidSymptomChecker {
    public static void main(String[] args) {
        List<Symptom> symptoms = Arrays.asList(
            new Symptom("Fever", true),
            new Symptom("Dry Cough", true),
            new Symptom("Tiredness", true),
            new Symptom("Sore Throat", false),
            new Symptom("Headache", false),
            new Symptom("Loss of Taste or Smell", true),
            new Symptom("Difficulty Breathing", true)
        );

        // TODO: Filter the list of symptoms to only include those that are COVID-19 symptoms
        List<Symptom> covidSymptoms = null;

        System.out.println("COVID-19 Symptoms:");
        // TODO: Print the COVID-19 symptoms
    }

    public static class Symptom {
        private String name;
        private boolean isCovidSymptom;

        public Symptom(String name, boolean isCovidSymptom) {
            this.name = name;
            this.isCovidSymptom = isCovidSymptom;
        }

        public String getName() {
            return name;
        }

        public boolean isCovidSymptom() {
            return isCovidSymptom;
        }
    }
}

```


## Solution File

```

import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class CovidSymptomChecker {
    public static void main(String[] args) {
        List<Symptom> symptoms = Arrays.asList(
            new Symptom("Fever", true),
            new Symptom("Dry Cough", true),
            new Symptom("Tiredness", true),
            new Symptom("Sore Throat", false),
            new Symptom("Headache", false),
            new Symptom("Loss of Taste or Smell", true),
            new Symptom("Difficulty Breathing", true)
        );

        List<Symptom> covidSymptoms = symptoms.stream()
            .filter(Symptom::isCovidSymptom)
            .collect(Collectors.toList());

        System.out.println("COVID-19 Symptoms:");
        covidSymptoms.forEach(symptom -> System.out.println(symptom.getName()));
    }

    public static class Symptom {
        private String name;
        private boolean isCovidSymptom;

        public Symptom(String name, boolean isCovidSymptom) {
            this.name = name;
            this.isCovidSymptom = isCovidSymptom;
        }

        public String getName() {
            return name;
        }

        public boolean isCovidSymptom() {
            return isCovidSymptom;
        }
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
import java.util.Arrays;
import java.util.List;
import java.util.logging.Logger;
import java.util.stream.Collectors;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {
    private static final Logger logger = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void test_covid_symptoms() {
        List<CovidSymptomChecker.Symptom> symptoms = Arrays.asList(
            new CovidSymptomChecker.Symptom("Fever", true),
            new CovidSymptomChecker.Symptom("Dry Cough", true),
            new CovidSymptomChecker.Symptom("Tiredness", true),
            new CovidSymptomChecker.Symptom("Sore Throat", false),
            new CovidSymptomChecker.Symptom("Headache", false),
            new CovidSymptomChecker.Symptom("Loss of Taste or Smell", true),
            new CovidSymptomChecker.Symptom("Difficulty Breathing", true)
        );

        List<CovidSymptomChecker.Symptom> covidSymptoms = symptoms.stream()
            .filter(CovidSymptomChecker.Symptom::isCovidSymptom)
            .collect(Collectors.toList());

        List<String> expected = Arrays.asList("Fever", "Dry Cough", "Tiredness", "Loss of Taste or Smell", "Difficulty Breathing");
        List<String> actual = covidSymptoms.stream().map(CovidSymptomChecker.Symptom::getName).collect(Collectors.toList());

        logger.info("Expected output: " + expected);
        logger.info("Actual output: " + actual);
        
        assertEquals(expected, actual, "Should return the correct list of COVID-19 symptoms");
    }

    private final ByteArrayOutputStream outContent = new ByteArrayOutputStream();
    private final PrintStream originalOut = System.out;

    @BeforeEach
    public void setUpStreams() {
        System.setOut(new PrintStream(outContent));
    }

    @AfterEach
    public void restoreStreams() {
        System.setOut(originalOut);
    }

    @Test
    public void test_covid_symptoms_output() {
        CovidSymptomChecker.main(new String[]{});

        String expectedOutput = "COVID-19 Symptoms:" + System.lineSeparator()
            + "Fever" + System.lineSeparator()
            + "Dry Cough" + System.lineSeparator()
            + "Tiredness" + System.lineSeparator()
            + "Loss of Taste or Smell" + System.lineSeparator()
            + "Difficulty Breathing" + System.lineSeparator();

        logger.info("Expected printed output: " + expectedOutput.replace(System.lineSeparator(), "\\n"));
        logger.info("Actual printed output: " + outContent.toString().replace(System.lineSeparator(), "\\n"));

        assertEquals(expectedOutput, outContent.toString(), "Should print the correct list of COVID-19 symptoms");
    }
}

```