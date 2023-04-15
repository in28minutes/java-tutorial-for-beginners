
# Exercise 2: Calculating Average Speed of Formula 1 Cars in a Race using Java

  

  

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