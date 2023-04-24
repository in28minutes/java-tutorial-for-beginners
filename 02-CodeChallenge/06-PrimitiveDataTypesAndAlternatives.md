
# Exercise 1: Calculating Average Speed of Formula 1 Cars in a Race using Java

  

  

## Instructions

### Problem Statement

In a Formula 1 race, there are 5 cars competing. The total distance traveled by all cars combined is 12,000 meters, and the total time taken by all cars is 720.5 seconds. Your task is to calculate the average speed of the cars in the race.

### Instructions

1.  Implement the `calculateAverageSpeed` method: 
- a. This method should take three parameters: `numberOfCars` (int), `totalDistance` (BigDecimal), and `totalTime` (BigDecimal). 
- b. Calculate the average distance by dividing the `totalDistance` by the `numberOfCars`. Set the scale to 2 and use BigDecimal.ROUND_HALF_UP for rounding. 
- c. Calculate the average time by dividing the `totalTime` by the `numberOfCars`. Set the scale to 2 and use BigDecimal.ROUND_HALF_UP for rounding. 
- d. Divide the average distance by the average time to get the average speed. Set the scale to 2 and use BigDecimal.ROUND_HALF_UP for rounding. 
- e. Return the calculated average speed (BigDecimal).
    
3.  In the `main` method: 
Call the `calculateAverageSpeed` method with the values `numberOfCars`, `totalDistance`, and `totalTime`. Store the result in a variable named `averageSpeed`.
    

#### Output:

**When you run the `Formula1RaceRunner` class with your code, you will get the following output:**

```
Average speed for the Formula 1 cars: 16.7 m/s

```

  

## Hints

Here are some short hints in markdown format:

1. Use the BigDecimal class for precise decimal calculations.
2. Divide the total distance by the total time to get the average speed of one car.
3. Divide the result by the number of cars to get the average speed of all the cars.
4. Use the ROUND_HALF_UP rounding mode to round the result according to standard mathematical rules.
5. Call the calculateAverageSpeed() method with the appropriate arguments to get the average speed of the cars.
6. Store the result of the calculateAverageSpeed() method in a variable named averageSpeed.
  



## Solution Explanation

#### Step 1: Define a method to calculate the average speed of the cars

The first step is to define a method to calculate the average speed of the cars. This method should take in the following three parameters:

-   `numberOfCars`: an integer representing the number of cars in the race
-   `totalDistance`: a BigDecimal representing the total distance covered by all the cars
-   `totalTime`: a BigDecimal representing the total time taken by all the cars

The method should return a BigDecimal representing the average speed of the cars. We can implement this method using the `BigDecimal.divide` method with a scale of 2 and rounding mode of `BigDecimal.ROUND_HALF_UP`.

Here's the code for the `calculateAverageSpeed` method:

```
static BigDecimal calculateAverageSpeed(int numberOfCars, BigDecimal totalDistance, BigDecimal totalTime) {
    BigDecimal averageDistance = totalDistance.divide(new BigDecimal(numberOfCars), 2, BigDecimal.ROUND_HALF_UP);
    BigDecimal averageTime = totalTime.divide(new BigDecimal(numberOfCars), 2, BigDecimal.ROUND_HALF_UP);

    return averageDistance.divide(averageTime, 2, BigDecimal.ROUND_HALF_UP);
}
```

#### Step 2: Call the `calculateAverageSpeed` method in the `main` method

The next step is to call the `calculateAverageSpeed` method in the `main` method and store the result in a variable named `averageSpeed`. We can then print out the average speed using the `System.out.println` method.

Here's the code for the `main` method:

```
public static void main(String[] args) {
    int numberOfCars = 5;
    BigDecimal totalDistance = new BigDecimal("12000"); // in meters
    BigDecimal totalTime = new BigDecimal("720.5"); // in seconds

    BigDecimal averageSpeed = calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

    System.out.println("Average speed for the Formula 1 cars: " + averageSpeed.setScale(1, BigDecimal.ROUND_HALF_UP) + " m/s");
}
```

#### Step 3: Output the result

The final step is to run the program and observe the output. The program should output the following:

```
Average speed for the Formula 1 cars: 16.7 m/s
```

And that's it!
 

## Student File

  

**Formula1RaceRunner.java**

  

```
import java.math.BigDecimal;

public class Formula1RaceRunner {
  
    // The method should return a BigDecimal representing the average speed of the cars.
    // Use the BigDecimal.divide method with a scale of 2 and rounding mode of BigDecimal.ROUND_HALF_UP.
    static BigDecimal calculateAverageSpeed(int numberOfCars, BigDecimal totalDistance, BigDecimal totalTime) {
        // Write your code here
    }

    public static void main(String[] args) {
        int numberOfCars = 5;
        BigDecimal totalDistance = new BigDecimal("12000"); // in meters
        BigDecimal totalTime = new BigDecimal("720.5"); // in seconds

        // TODO: Call the calculateAverageSpeed method and store the result in a variable named averageSpeed.
        BigDecimal averageSpeed;

        System.out.println("Average speed for the Formula 1 cars: " + averageSpeed.setScale(1, BigDecimal.ROUND_HALF_UP) + " m/s");
    }
}


```

  

  

## Solution File

  

**Formula1RaceRunner.java**

  

```
import java.math.BigDecimal;

public class Formula1RaceRunner {

    static BigDecimal calculateAverageSpeed(int numberOfCars, BigDecimal totalDistance, BigDecimal totalTime) {
        BigDecimal averageDistance = totalDistance.divide(new BigDecimal(numberOfCars), 2, BigDecimal.ROUND_HALF_UP);
        BigDecimal averageTime = totalTime.divide(new BigDecimal(numberOfCars), 2, BigDecimal.ROUND_HALF_UP);

        return averageDistance.divide(averageTime, 2, BigDecimal.ROUND_HALF_UP);
    }

    public static void main(String[] args) {
        int numberOfCars = 5;
        BigDecimal totalDistance = new BigDecimal("12000"); // in meters
        BigDecimal totalTime = new BigDecimal("720.5"); // in seconds

        BigDecimal averageSpeed = calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

        System.out.println("Average speed for the Formula 1 cars: " + averageSpeed.setScale(1, BigDecimal.ROUND_HALF_UP) + " m/s");
    }
}

```

  
  

## Evaluation File

 
**Evaluate.java**

  

```
// Evaluate.java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;
import com.udemy.ucp.IOHelper;
import com.udemy.ucp.EvaluationHelper;
import static org.junit.jupiter.api.Assertions.fail;
import java.lang.reflect.Method;

import java.math.BigDecimal;

public class Evaluate {

    Formula1RaceRunner runner = new Formula1RaceRunner();
    IOHelper helper = new IOHelper();

    EvaluationHelper evaluationHelper = new EvaluationHelper();


    @Test
    public void testFieldsAndMethods() {
        try {
            Method calculateAverageSpeedMethod = Formula1RaceRunner.class.getDeclaredMethod("calculateAverageSpeed", int.class, BigDecimal.class, BigDecimal.class);
        } catch (NoSuchMethodException e) {
            fail("'calculateAverageSpeed' method is not declared.");
        }

        try {
            Method mainMethod = Formula1RaceRunner.class.getDeclaredMethod("main", String[].class);
        } catch (NoSuchMethodException e) {
            fail("'main' method is not declared.");
        }
    }





    @Test
    public void testCalculateAverageSpeed() {
        int numberOfCars = 5;
        BigDecimal totalDistance = new BigDecimal("12000");
        BigDecimal totalTime = new BigDecimal("720.5");

        BigDecimal averageSpeed = runner.calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

        assertEquals(new BigDecimal("16.7"), averageSpeed.setScale(1, BigDecimal.ROUND_HALF_UP), "Average speed calculation is incorrect.");
    }

    @Test
    public void testMainMethod() {
        helper.resetStdOut(); // clean stdout
        Formula1RaceRunner.main(new String[] {});
        String actualOutput = helper.getOutput().trim(); // remove leading/trailing whitespaces
        assertEquals("Average speed for the Formula 1 cars: 16.7 m/s", actualOutput, "Output does not match the expected format.");
    }

}

```






# Exercise 2: Print First Nth Fibonacci Numbers with MyIntRunner

  

## Instructions

### Problem Statement

You are given an incomplete Java program called `MyIntRunner` that has a nested class `MyInt`. Your task is to complete the `MyInt` class by adding the required fields, constructor, and methods, following the provided solution code.

### Detailed Instructions

1.  Declare an instance variable `value` of type `int` in the `MyInt` class to store the value of the `MyInt` object.
    
2.  Create a constructor for the `MyInt` class that takes an `int` parameter, `value`. The constructor should initialize the `value` field of the `MyInt` object with the provided `value`.
    
3.  Implement the `printFirstNFibonacciNumbers()` method in the `MyInt` class. This method should print the first N Fibonacci numbers, where N is the `value` of the `MyInt` object.
    
    (i) Declare and initialize two variables, `a` and `b`, to store the first two Fibonacci numbers (0 and 1, respectively).
    
    (ii) Declare a variable `c` to store the sum of the two previous Fibonacci numbers.
    
    (iii) Use a loop to iterate from 1 to `value` (inclusive).
    
        -  (a) Print the current Fibonacci number (value of `a`). 
        -  (b) Calculate the sum of the two previous Fibonacci numbers (`a` and `b`) and store it in `c`.
        -  (c) Update the values of `a` and `b` for the next iteration: `a` should become `b` and `b` should become `c`.
    

### Output Format

The output of the program should be the first N Fibonacci numbers, where N is the `value` of the `MyInt` object, each on a new line.

### Example

For a `MyInt` object with a `value` of 10, the output should be:

```
0
1
1
2
3
5
8
13
21
34
```


## Hints

1.  Use the `public` keyword to declare the instance variable `value` and the constructor of the `MyInt` class.
    
2.  Initialize the `value` field of the `MyInt` object in the constructor using `this.value = value`.
    
3.  To declare the `printFirstNFibonacciNumbers()` method, use the `public` keyword followed by the `void` return type.
    
4.  Use a `for` loop to iterate from 1 to `value` (inclusive).
    
5.  Inside the loop, print the current Fibonacci number using `System.out.println(a)`.
    
6.  Update the Fibonacci numbers using `c = a + b`, `a = b`, and `b = c` inside the loop.

##  Solution Explanation

The solution involves completing the `MyInt` class by adding the required fields, constructor, and methods. Let's go through the solution step by step:

1.  Declare the instance variable `value` of type `int` in the `MyInt` class:
    
    ```
    public int value;
    ```
    
2.  Create a constructor for the `MyInt` class that takes an `int` parameter, `value`. The constructor should initialize the `value` field of the `MyInt` object with the provided `value`:
    
   ```
   public MyInt(int value) {
        this.value = value;
    }
   ```
    
3.  Implement the `printFirstNFibonacciNumbers()` method in the `MyInt` class:
    
    ```public void printFirstNFibonacciNumbers() {
        // (i) Declare and initialize variables to store the first two Fibonacci numbers
        int a = 0, b = 1;
    
        // (ii) Declare a variable to store the sum of the two previous Fibonacci numbers
        int c;
    
        // (iii) Use a loop to iterate from 1 to value (inclusive)
        for (int i = 1; i <= value; i++) {
            // (a) Print the current Fibonacci number
            System.out.println(a);
    
            // (b) Calculate the sum of the two previous Fibonacci numbers and store it in c
            c = a + b;
    
            // (c) Update the values of a and b for the next iteration
            a = b;
            b = c;
        }
    }
    ```
    

Now, the `MyInt` class is complete with the required fields, constructor, and methods. The `MyIntRunner` class, with the completed `MyInt` class, will print the first N Fibonacci numbers, where N is the `value` of the `MyInt` object.

Here's the final solution code:

```
public class MyIntRunner {
    public static void main(String[] args) {
        // Create a MyInt object with a value of 10
        MyInt myInt = new MyInt(10);

        // Call the printFirstNFibonacciNumbers method on the myInt object
        myInt.printFirstNFibonacciNumbers();
    }

    static class MyInt {
        // Declare an instance variable to store the value
        public int value;

        // Constructor to initialize the value of the MyInt object
        public MyInt(int value) {
            this.value = value;
        }
        
        // Method to print the first N Fibonacci numbers, where N is the value of the MyInt object
        public void printFirstNFibonacciNumbers() {
            // Declare and initialize variables to store the first two Fibonacci numbers
            int a = 0, b = 1;

            // Declare a variable to store the sum of the two previous Fibonacci numbers
            int c;

            // Loop from 1 to value (inclusive)
            for (int i = 1; i <= value; i++) {
                // Print the current Fibonacci number
                System.out.println(a);

                // Calculate the sum of the two previous Fibonacci numbers
                c = a + b;

                // Update the values of a and b for the next iteration
                a = b;
                b = c;
            }
        }
    }
}
```


## Student File

  

**MyIntRunner.java**

  

```
public class MyIntRunner {
    public static void main(String[] args) {
        // Create a MyInt object with a value of 10
        MyInt myInt = new MyInt(10);

        // Call the printFirstNFibonacciNumbers method on the myInt object
        myInt.printFirstNFibonacciNumbers();
    }

    static class MyInt {
        // Declare an instance variable to store the value

        // Constructor to initialize the value of the MyInt object

        // Method to print the first N Fibonacci numbers, where N is the value of the MyInt object
        public void printFirstNFibonacciNumbers() {
            // TODO: Declare and initialize variables to store the first two Fibonacci numbers

            // TODO: Declare a variable to store the sum of the two previous Fibonacci numbers

            // TODO: Loop from 1 to value (inclusive)

                // TODO: Print the current Fibonacci number

                // TODO: Calculate the sum of the two previous Fibonacci numbers

                // TODO: Update the values of the two Fibonacci number variables for the next iteration
        }
    }
}



```

  

  

## Solution File

  

**MyIntRunner.java**

  

```
public class MyIntRunner {
    public static void main(String[] args) {
        // Create a MyInt object with a value of 10
        MyInt myInt = new MyInt(10);

        // Call the printFirstNFibonacciNumbers method on the myInt object
        myInt.printFirstNFibonacciNumbers();
    }

    static class MyInt {
        // Declare an instance variable to store the value
        public int value;

        // Constructor to initialize the value of the MyInt object
        public MyInt(int value) {
            this.value = value;
        }
        

        // Method to print the first N Fibonacci numbers, where N is the value of the MyInt object
        public void printFirstNFibonacciNumbers() {
            // Declare and initialize variables to store the first two Fibonacci numbers
            int a = 0, b = 1;

            // Declare a variable to store the sum of the two previous Fibonacci numbers
            int c;

            // Loop from 1 to value (inclusive)
            for (int i = 1; i <= value; i++) {
                // Print the current Fibonacci number
                System.out.println(a);

                // Calculate the sum of the two previous Fibonacci numbers
                c = a + b;

                // Update the values of a and b for the next iteration
                a = b;
                b = c;
            }
        }
    }
}

```

  
  

## Evaluation File

 
**Evaluate.java**

  

```
// Evaluate.java
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.AfterEach;
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;
import static org.junit.jupiter.api.Assertions.assertTrue;
import java.io.ByteArrayOutputStream;
import java.io.PrintStream;
import java.util.logging.Logger;
import java.util.logging.Level;
import java.lang.reflect.Field;
import java.lang.reflect.Method;

public class Evaluate {

    private final ByteArrayOutputStream outContent = new ByteArrayOutputStream();
    private final PrintStream originalOut = System.out;
    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @BeforeEach
    public void setUpStreams() {
        System.setOut(new PrintStream(outContent));
    }

    // Other tests...
    @Test
    public void testPrintFirstNFibonacciNumbers() {
        MyIntRunner.MyInt myInt = new MyIntRunner.MyInt(10);
        myInt.printFirstNFibonacciNumbers();

        String expectedOutput = "0" + System.lineSeparator() +
                                "1" + System.lineSeparator() +
                                "1" + System.lineSeparator() +
                                "2" + System.lineSeparator() +
                                "3" + System.lineSeparator() +
                                "5" + System.lineSeparator() +
                                "8" + System.lineSeparator() +
                                "13" + System.lineSeparator() +
                                "21" + System.lineSeparator() +
                                "34" + System.lineSeparator();
        String actualOutput = outContent.toString();
        LOGGER.log(Level.INFO, "Expected Output: " + expectedOutput);
        LOGGER.log(Level.INFO, "Actual Output: " + actualOutput);
        assertEquals(expectedOutput, actualOutput, "MyInt.printFirstNFibonacciNumbers() should print the first N Fibonacci numbers correctly");
    }

    @Test
    public void testFieldsAndMethods() {
        // Check if the 'value' field is declared
        try {
            Field valueField = MyIntRunner.MyInt.class.getDeclaredField("value");
            assertEquals(int.class, valueField.getType(), "MyInt.value field should be of type int");
        } catch (NoSuchFieldException e) {
            LOGGER.log(Level.SEVERE, "MyInt.value field is missing", e);
            assertTrue(false, "MyInt.value field should be declared");
        }

        // Check if the constructor is declared
        try {
            MyIntRunner.MyInt.class.getDeclaredConstructor(int.class);
            assertTrue(true, "MyInt constructor should be declared");
        } catch (NoSuchMethodException e) {
            LOGGER.log(Level.SEVERE, "MyInt constructor is missing", e);
            assertTrue(false, "MyInt constructor should be declared");
        }

        // Check if the 'printFirstNFibonacciNumbers()' method is declared
        try {
            Method printFirstNFibonacciNumbersMethod = MyIntRunner.MyInt.class.getDeclaredMethod("printFirstNFibonacciNumbers");
            assertEquals(void.class, printFirstNFibonacciNumbersMethod.getReturnType(), "MyInt.printFirstNFibonacciNumbers() method should have void return type");
        } catch (NoSuchMethodException e) {
            LOGGER.log(Level.SEVERE, "MyInt.printFirstNFibonacciNumbers() method is missing", e);
            assertTrue(false, "MyInt.printFirstNFibonacciNumbers() method should be declared");
        }
    }

    @AfterEach
    public void restoreStreams() {
        System.setOut(originalOut);
    }
}


```