
# Exercise 2: Calculating Average Speed of Formula 1 Cars in a Race using Java

  

  

## Instructions

### Problem Statement:

You have been tasked with creating a Java program that calculates the average speed of a group of Formula 1 cars during a race, taking into account their total distance covered and the time taken for each car. Your program should use the following primitive data types: int, long, float, and double.

### Instructions:

1.  Create a Java class called `Formula1RaceRunner`.
2.  Define a method named `calculateAverageSpeed` that takes three parameters:
    -   an `int` named `numberOfCars`, representing the number of Formula 1 cars in the race
    -   a `long` named `totalDistance`, representing the total distance covered by all cars in meters
    -   a `float` named `totalTime`, representing the total time taken by all cars in seconds
3.  In the `calculateAverageSpeed` method, calculate the average distance covered by each car by dividing the total distance by the number of cars.
4.  Calculate the average time taken by each car by dividing the total time by the number of cars.
5.  Calculate the average speed by dividing the average distance by the average time. Return the result as a `double`.
6.  Create a `main` method in the `Formula1RaceRunner` class.
7.  In the `main` method, define variables for the number of cars, total distance, and total time. Assign appropriate values to these variables.
8.  Call the `calculateAverageSpeed` method with the defined variables as arguments and store the result in a `double` variable named `averageSpeed`.
9.  Print the `averageSpeed` to the console, formatted to one decimal place.

By following these instructions, you will create a Java program that calculates the average speed of a group of Formula 1 cars during a race, considering their total distance covered and the time taken for each car, using the requested primitive data types.

#### Output:

**When you run the `Formula1RaceRunner` class with your code, you will get the following output:**

```
Average speed for the Formula 1 cars: 16.7 m/s
```

This output shows the calculated average speed for the Formula 1 cars during the race, considering their total distance covered and the time taken for each car. The result is formatted to one decimal place.
  

## Hints

Here are the hints:

1.  **Hint 1**: Create a `Formula1RaceRunner` class and define a method named `calculateAverageSpeed` that takes three parameters - `numberOfCars`, `totalDistance`, and `totalTime`.
2.  **Hint 2**: Calculate `averageDistance` by dividing `totalDistance` by `numberOfCars`. Calculate `averageTime` by dividing `totalTime` by `numberOfCars`.
3.  **Hint 3**: Calculate the `averageSpeed` by dividing `averageDistance` by `averageTime`. Return the result as a `double`.
4.  **Hint 4**: Create a `main` method in the `Formula1RaceRunner` class. Define variables for the `numberOfCars`, `totalDistance`, and `totalTime`. Assign appropriate values to these variables.
5.  **Hint 5**: Call the `calculateAverageSpeed` method with the defined variables as arguments and store the result in a `double` variable named `averageSpeed`.
6.  **Hint 6**: Print the `averageSpeed` to the console, formatted to one decimal place using `System.out.printf()`.  
  



## Solution Explanation
Here is the solution explanation with code in Markdown format:

To solve this problem, we'll create a Java class called `Formula1RaceRunner` that calculates the average speed of a group of Formula 1 cars during a race, considering their total distance covered and the time taken for each car.

**Step 1**: Create a method named `calculateAverageSpeed` in the `Formula1RaceRunner` class:

```
static double calculateAverageSpeed(int numberOfCars, long totalDistance, float totalTime) {
    // .....
}
```

This method takes three parameters: `numberOfCars` (an integer), `totalDistance` (a long), and `totalTime` (a float).

**Step 2**: Calculate the average distance and average time:

```
double averageDistance = (double) totalDistance / numberOfCars;
double averageTime = totalTime / numberOfCars;
```

We divide the total distance by the number of cars to get the average distance. Similarly, we divide the total time by the number of cars to get the average time.

**Step 3**: Calculate and return the average speed:

```
return averageDistance / averageTime;
```

To calculate the average speed, we divide the average distance by the average time.

**Step 4**: Create the `main` method in the `Formula1RaceRunner` class:

```
public static void main(String[] args) {
    // ...
}
```

**Step 5**: Define the variables for the number of cars, total distance, and total time, and assign appropriate values to them:

```
int numberOfCars = 5;
long totalDistance = 12000; // in meters
float totalTime = 720.5f; // in seconds
```

**Step 6**: Call the `calculateAverageSpeed` method with the defined variables as arguments and store the result in a `double` variable named `averageSpeed`:

```
double averageSpeed = calculateAverageSpeed(numberOfCars, totalDistance, totalTime);
```

**Step 7**: Print the `averageSpeed` to the console, formatted to one decimal place using `System.out.printf()`:

```
System.out.printf("Average speed for the Formula 1 cars: %.1f m/s\n", averageSpeed);
```

The complete `Formula1RaceRunner` class should look like this:

```
public class Formula1RaceRunner {

    static double calculateAverageSpeed(int numberOfCars, long totalDistance, float totalTime) {
        double averageDistance = (double) totalDistance / numberOfCars;
        double averageTime = totalTime / numberOfCars;

        return averageDistance / averageTime;
    }

    public static void main(String[] args) {
        int numberOfCars = 5;
        long totalDistance = 12000; // in meters
        float totalTime = 720.5f; // in seconds

        double averageSpeed = calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

        System.out.printf("Average speed for the Formula 1 cars: %.1f m/s\n", averageSpeed);
    }
}
```

When you run this Java program, it calculates the average speed of the Formula 1 cars during the race and prints the result:

```
Average speed for the Formula 1 cars: 16.7 m/s
```
  

## Student File

  

**Formula1RaceRunner.java**

  

```
public class Formula1RaceRunner {
    
    static double calculateAverageSpeed(int numberOfCars, long totalDistance, float totalTime) {
        // Complete the code
    }

    public static void main(String[] args) {
        int numberOfCars = 5;
        long totalDistance = 12000; // in meters
        float totalTime = 720.5f; // in seconds

        // Complete the code
        double averageSpeed;

        System.out.printf("Average speed for the Formula 1 cars: %.1f m/s\n", averageSpeed);
    }
}

```

  

  

## Solution File

  

**Formula1RaceRunner.java**

  

```
public class Formula1RaceRunner {

    static double calculateAverageSpeed(int numberOfCars, long totalDistance, float totalTime) {
        double averageDistance = (double) totalDistance / numberOfCars;
        double averageTime = totalTime / numberOfCars;

        return averageDistance / averageTime;
    }

    public static void main(String[] args) {
        int numberOfCars = 5;
        long totalDistance = 12000; // in meters
        float totalTime = 720.5f; // in seconds

        double averageSpeed = calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

        System.out.printf("Average speed for the Formula 1 cars: %.1f m/s\n", averageSpeed);
    }
}

```

  
  

## Evaluation File

 
**Evaluate.java**

  

```
import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;
import java.util.logging.Logger;
import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {

    private Formula1RaceRunner formula1RaceRunner;
    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @BeforeEach
    public void setUp() {
        formula1RaceRunner = new Formula1RaceRunner();
    }

    @Test
    public void testCalculateAverageSpeed() {
        LOGGER.info("Running testCalculateAverageSpeed...");

        int numberOfCars = 5;
        long totalDistance = 12000; // in meters
        float totalTime = 720.5f; // in seconds

        double expectedAverageSpeed = 16.7;

        double actualAverageSpeed = Formula1RaceRunner.calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

        assertEquals(expectedAverageSpeed, actualAverageSpeed, 0.1, "The average speed calculation is not correct");
    }
}

```