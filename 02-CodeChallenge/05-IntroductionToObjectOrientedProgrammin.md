## Exercise 1: Implementing Encapsulation Techniques in the VideoGame Class

  

### Instructions

#### Task 1: Implement VideoGame class attributes

1.  In the given `VideoGameRunner` class, add the following attributes to the `VideoGame` class:
    -   `title` of type `String`
    -   `numberOfCopies` of type `int`

#### Task 2: Implement methods for VideoGame class

1.  Implement the following methods for the `VideoGame` class:
    -   `setTitle(String gameTitle)`: Sets the title of the video game.
    -   `getTitle()`: Returns the title of the video game.
    -   `setNumberOfCopies(int numberOfCopies)`: Sets the number of copies if the provided number is greater than or equal to 0.
    -   `getNumberOfCopies()`: Returns the number of copies.
    -   `increaseCopies(int howMuch)`: Increases the number of copies by the given amount.
    -   `decreaseCopies(int howMuch)`: Decreases the number of copies by the given amount but ensures that the number of copies does not go below 0.  
  

#### Task 3: Test the VideoGame class in the main method

1.  In the `main` method of the `VideoGameRunner` class, create three instances of the `VideoGame` class and set their titles as follows:
    
    -   Create an instance named `rdr2` and set its title to "Red Dead Redemption 2".
    -   Create an instance named `tw3` and set its title to "The Witcher 3".
    -   Create an instance named `botw` and set its title to "Breath of the Wild".
2.  Print the titles of the three video game instances (`rdr2`, `tw3`, and `botw`).
    
3.  Increase the number of copies for each video game instance as follows:
    
    -   Increase the number of copies for `rdr2` by 12.
    -   Increase the number of copies for `tw3` by 18.
    -   Increase the number of copies for `botw` by 24.
4.  Decrease the number of copies for each video game instance as follows:
    
    -   Decrease the number of copies for `rdr2` by 6.
    -   Decrease the number of copies for `tw3` by 12.
    -   Decrease the number of copies for `botw` by 18.
5.  Print the number of copies for each video game instance (`rdr2`, `tw3`, and `botw`).

  

### Hints

#### Task 1: Implement VideoGame class attributes

**Hint 1:** To add attributes to a class, declare them within the class using the appropriate data type.

**Hint 2:** You need to add two attributes: a `String` for the `title` and an `int` for the `numberOfCopies`.

#### Task 2: Implement methods for VideoGame class

**Hint 1:** To create a method, use the following syntax: `access_modifier return_type methodName(parameters) { /* method body */ }`.

**Hint 2:** For example, the `setTitle` method should have a `void` return type and a single `String` parameter.

**Hint 3:** To set the number of copies only if the provided number is greater than or equal to 0, use an `if` statement in the `setNumberOfCopies` method.

**Hint 4:** The `increaseCopies` and `decreaseCopies` methods should use the `setNumberOfCopies` method to update the `numberOfCopies` attribute.

#### Task 3: Test the VideoGame class in the main method

**Hint 1:** To create an instance of a class, use the `new` keyword followed by the class name and parentheses.

**Hint 2:** To call a method on an instance of a class, use the dot (.) operator followed by the method name and its arguments.

**Hint 3:** Use `System.out.println()` to print the titles and number of copies for each video game instance.
  

### Solution Explanation


The given problem code is incomplete and needs to be modified to include the necessary attributes and methods in the `VideoGame` class. Below is the step-by-step explanation of the solution code.

#### Task 1: Implement VideoGame class attributes

We start by adding the required attributes `title` and `numberOfCopies` to the `VideoGame` class.

```
private String title;
private int numberOfCopies;
```

#### Task 2: Implement methods for VideoGame class

Next, we implement the required methods for the `VideoGame` class.

1.  Set and get methods for `title` attribute:

```
public void setTitle(String gameTitle) {
    title = gameTitle;
}

public String getTitle() {
    return title;
}
```

2.  Set and get methods for `numberOfCopies` attribute with a condition to ensure the number of copies is non-negative:

```
public void setNumberOfCopies(int numberOfCopies) {
    if (numberOfCopies >= 0) {
        this.numberOfCopies = numberOfCopies;
    }
}

public int getNumberOfCopies() {
    return numberOfCopies;
}
```

3.  Methods to increase and decrease the number of copies:

```
public void increaseCopies(int howMuch) {
    setNumberOfCopies(numberOfCopies + howMuch);
}

public void decreaseCopies(int howMuch) {
    setNumberOfCopies(numberOfCopies - howMuch);
}
```

#### Task 3: Test the VideoGame class in the main method

Finally, we test the `VideoGame` class in the `main` method by creating instances, setting titles, increasing and decreasing the number of copies, and printing their titles and number of copies.

```
public static void main(String[] args) {
    VideoGame rdr2 = new VideoGame();
    rdr2.setTitle("Red Dead Redemption 2");
    VideoGame tw3 = new VideoGame();
    tw3.setTitle("The Witcher 3");
    VideoGame botw = new VideoGame();
    botw.setTitle("Breath of the Wild");

    System.out.println(rdr2.getTitle());
    System.out.println(tw3.getTitle());
    System.out.println(botw.getTitle());

    rdr2.increaseCopies(12);
    tw3.increaseCopies(18);
    botw.increaseCopies(24);
    rdr2.decreaseCopies(6);
    tw3.decreaseCopies(12);
    botw.decreaseCopies(18);

    System.out.println(rdr2.getNumberOfCopies());
    System.out.println(tw3.getNumberOfCopies());
    System.out.println(botw.getNumberOfCopies());
}
```

This solution code demonstrates the proper implementation of encapsulation techniques and completes the `VideoGame` class as required by the problem statement.

### Student File

**VideoGameRunner.java**

```

public class VideoGameRunner {

    static class VideoGame {
     // Complete the code
    }

    public static void main(String[] args) {
        // VideoGame rdr2 = new VideoGame();
        //  rdr2.setTitle("Red Dead Redemption 2");
         // Complete the code
    }
}

```

  
  

### Solution File

**VideoGameRunner.java**

```
public class VideoGameRunner {

    static class VideoGame {
        private String title;
        private int numberOfCopies;

        public void setTitle(String gameTitle) {
            title = gameTitle;
        }

        public String getTitle() {
            return title;
        }

        public void setNumberOfCopies(int numberOfCopies) {
            if (numberOfCopies >= 0) {
                this.numberOfCopies = numberOfCopies;
            }
        }

        public int getNumberOfCopies() {
            return numberOfCopies;
        }

        public void increaseCopies(int howMuch) {
            setNumberOfCopies(numberOfCopies + howMuch);
        }

        public void decreaseCopies(int howMuch) {
            setNumberOfCopies(numberOfCopies - howMuch);
        }
    }

    public static void main(String[] args) {
        VideoGame rdr2 = new VideoGame();
        rdr2.setTitle("Red Dead Redemption 2");
        VideoGame tw3 = new VideoGame();
        tw3.setTitle("The Witcher 3");
        VideoGame botw = new VideoGame();
        botw.setTitle("Breath of the Wild");

        System.out.println(rdr2.getTitle());
        System.out.println(tw3.getTitle());
        System.out.println(botw.getTitle());

        rdr2.increaseCopies(12);
        tw3.increaseCopies(18);
        botw.increaseCopies(24);
        rdr2.decreaseCopies(6);
        tw3.decreaseCopies(12);
        botw.decreaseCopies(18);

        System.out.println(rdr2.getNumberOfCopies());
        System.out.println(tw3.getNumberOfCopies());
        System.out.println(botw.getNumberOfCopies());
    }
}

```


### Evaluation File

**Evaluate.java**

```

import org.junit.jupiter.api.BeforeEach;
import org.junit.jupiter.api.Test;

import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.assertEquals;

public class Evaluate {

    private VideoGameRunner.VideoGame videoGame;
    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @BeforeEach
    public void setUp() {
        LOGGER.info("Setting up a new VideoGame instance for the tests...");
        videoGame = new VideoGameRunner.VideoGame();
    }

    @Test
    public void testSetTitleAndGetTitle() {
        LOGGER.info("Running testSetTitleAndGetTitle...");
        String testTitle = "Test Game";
        LOGGER.info("Setting title to: " + testTitle);
        videoGame.setTitle(testTitle);
        LOGGER.info("Getting the title and checking if it matches the expected value...");
        assertEquals(testTitle, videoGame.getTitle());
        LOGGER.info("testSetTitleAndGetTitle passed.");
    }

    @Test
    public void testSetNumberOfCopiesAndGetNumberOfCopies() {
        LOGGER.info("Running testSetNumberOfCopiesAndGetNumberOfCopies...");
        int testCopies = 10;
        LOGGER.info("Setting number of copies to: " + testCopies);
        videoGame.setNumberOfCopies(testCopies);
        LOGGER.info("Getting the number of copies and checking if it matches the expected value...");
        assertEquals(testCopies, videoGame.getNumberOfCopies());
        LOGGER.info("testSetNumberOfCopiesAndGetNumberOfCopies passed.");
    }

    @Test
    public void testIncreaseCopies() {
        LOGGER.info("Running testIncreaseCopies...");
        int initialCopies = 5;
        int increaseCopiesBy = 5;
        LOGGER.info("Setting initial number of copies to: " + initialCopies);
        videoGame.setNumberOfCopies(initialCopies);
        LOGGER.info("Increasing number of copies by: " + increaseCopiesBy);
        videoGame.increaseCopies(increaseCopiesBy);
        LOGGER.info("Getting the number of copies and checking if it matches the expected value...");
        assertEquals(initialCopies + increaseCopiesBy, videoGame.getNumberOfCopies());
        LOGGER.info("testIncreaseCopies passed.");
    }

    @Test
    public void testDecreaseCopies() {
        LOGGER.info("Running testDecreaseCopies...");
        int initialCopies = 10;
        int decreaseCopiesBy = 5;
        LOGGER.info("Setting initial number of copies to: " + initialCopies);
        videoGame.setNumberOfCopies(initialCopies);
        LOGGER.info("Decreasing number of copies by: " + decreaseCopiesBy);
        videoGame.decreaseCopies(decreaseCopiesBy);
        LOGGER.info("Getting the number of copies and checking if it matches the expected value...");
        assertEquals(initialCopies - decreaseCopiesBy, videoGame.getNumberOfCopies());
        LOGGER.info("testDecreaseCopies passed.");
    }
}

```






## Exercise 2: Implementing Vehicle Engine Control and Speed Tracking

  

### Instructions


#### Objective

In this exercise, you are asked to complete the implementation of a simple `Vehicle` class and a `VehicleRunner` class that demonstrates its usage.

#### Instructions

1.  Complete the implementation of the `Vehicle` class inside the `VehicleRunner` class. The `Vehicle` class should have the following properties:
    
    -   `speed`: An integer representing the speed of the vehicle.
    -   `type`: A string representing the type of the vehicle, e.g., "Car", "Truck", "Bike".
2.  Implement two constructors for the `Vehicle` class:
    
    -   A constructor that takes two parameters: `speed` and `type`. The `speed` should be set only if the value is greater than 0. Otherwise, the default speed should be 10. The `type` should always be set.
    -   A default constructor that sets the `speed` to 10 and the `type` to "Bike".
3.  Implement the following methods for the `Vehicle` class:
    
    -   `startEngine()`: This method should print "Engine started!".
    -   `stopEngine()`: This method should print "Engine stopped!" and set the `speed` to 0.
    -   `getSpeed()`: This method should return the current `speed` of the vehicle.
    -   `getType()`: This method should return the current `type` of the vehicle.
4.  In the `main()` method of the `VehicleRunner` class, create three `Vehicle` instances with different speed and type values:
    
    -   `car`: Speed 30, Type "Car".
    -   `truck`: Speed 20, Type "Truck".
    -   `bike`: Default constructor.
5.  Start the engine of all three vehicles and print their initial speed and type.
    
6.  Stop the engine of all three vehicles and print their final speed.
    

#### Example

Below is an example of the incomplete code provided to the student:

```
public class VehicleRunner {
    public static class Vehicle {
        // Write your code
    }
    
    public static void main(String[] args) {
       // Vehicle car = new Vehicle(30, "Car");
       // Write your code
    }
}
```

After completing the exercise, the output should look like this:
```
Engine started!
Engine started!
Engine started!
Earlier Car Speed is : 30, Type: Car
Earlier Truck Speed is : 20, Type: Truck
Earlier Bike Speed is : 10, Type: Bike
Engine stopped!
Engine stopped!
Engine stopped!
Stopped Car Speed is : 0
Stopped Truck Speed is : 0
Stopped Bike Speed is : 0
```


### Hints


Here are some hints for completing the given incomplete exercise code:

1.  Inside the `Vehicle` class, you need to declare two instance variables:
    
    -   `speed` of type `int`
    -   `type` of type `String`
2.  Create a constructor for the `Vehicle` class that takes two parameters:
    
    -   `int speed`
    -   `String type` Inside the constructor, initialize the instance variables with the given parameters.
3.  Create a default constructor for the `Vehicle` class. In this constructor, set default values for the instance variables:
    
    -   Set `speed` to `10`
    -   Set `type` to `"Bike"`
4.  Add a method `startEngine()` to the `Vehicle` class that prints "Engine started!" when called.
    
5.  Add a method `stopEngine()` to the `Vehicle` class that prints "Engine stopped!" when called and sets the `speed` of the vehicle to `0`.
    
6.  Create getter methods for the `speed` and `type` instance variables in the `Vehicle` class:
    
    -   `public int getSpeed()`
    -   `public String getType()`
7.  In the `main` method of the `VehicleRunner` class, create three instances of the `Vehicle` class:
    
    -   `Vehicle car = new Vehicle(30, "Car");`
    -   `Vehicle truck = new Vehicle(20, "Truck");`
    -   `Vehicle bike = new Vehicle();`
8.  Start the engine of each vehicle by calling the `startEngine()` method on each instance.
    
9.  Print the initial speed and type of each vehicle by calling the `getSpeed()` and `getType()` methods.
    
10.  Stop the engine of each vehicle by calling the `stopEngine()` method on each instance.
    
11.  Print the final speed of each vehicle after stopping the engine by calling the `getSpeed()` method.
  

### Solution Explanation



In this exercise, we're asked to complete the given incomplete `VehicleRunner` class by implementing the `Vehicle` class, its methods, and then creating instances of the `Vehicle` class in the `main` method. Here's the step-by-step explanation of the solution:

### Implementing the Vehicle class

1.  First, we declare two instance variables for the `Vehicle` class:
    -   `speed` of type `int`
    -   `type` of type `String`

```
private int speed;
private String type;
```

2.  Next, we create a constructor for the `Vehicle` class that takes two parameters:
    -   `int speed`
    -   `String type` Inside the constructor, we initialize the instance variables with the given parameters.

```
public Vehicle(int speed, String type) {
    if (speed > 0) {
        this.speed = speed;
    }
    this.type = type;
}
```

3.  We then create a default constructor for the `Vehicle` class. In this constructor, we set default values for the instance variables:
    -   Set `speed` to `10`
    -   Set `type` to `"Bike"`

```
public Vehicle() {
    this.speed = 10;
    this.type = "Bike";
}
```

4.  We add a method `startEngine()` to the `Vehicle` class that prints "Engine started!" when called.

```
public void startEngine() {
    System.out.println("Engine started!");
}
```

5.  We add another method `stopEngine()` to the `Vehicle` class that prints "Engine stopped!" when called and sets the `speed` of the vehicle to `0`.

```
public void stopEngine() {
    System.out.println("Engine stopped!");
    this.speed = 0;
}
```

6.  We create getter methods for the `speed` and `type` instance variables in the `Vehicle` class:
    -   `public int getSpeed()`
    -   `public String getType()`

```
public int getSpeed() {
    return speed;
}

public String getType() {
    return type;
}
```

### Creating instances and calling methods in the main method

7.  In the `main` method of the `VehicleRunner` class, we create three instances of the `Vehicle` class:

```
Vehicle car = new Vehicle(30, "Car");
Vehicle truck = new Vehicle(20, "Truck");
Vehicle bike = new Vehicle();
```

8.  We start the engine of each vehicle by calling the `startEngine()` method on each instance:

```
car.startEngine();
truck.startEngine();
bike.startEngine();
```

9.  We print the initial speed and type of each vehicle by calling the `getSpeed()` and `getType()` methods:

```
System.out.println("Earlier Car Speed is : " + car.getSpeed() + ", Type: " + car.getType());
System.out.println("Earlier Truck Speed is : " + truck.getSpeed() + ", Type: " + truck.getType());
System.out.println("Earlier Bike Speed is : " + bike.getSpeed() + ", Type: " + bike.getType());
```

10.  We stop the engine of each vehicle by calling the `stopEngine()` method on each instance:

```
car.stopEngine();
truck.stopEngine();
bike.stopEngine();
```

11.  Finally, we print the final speed of each vehicle after stopping the engine by calling the `getSpeed()` method:

```
System.out.println("Stopped Car Speed is : " + car.getSpeed());
System.out.println("Stopped Truck Speed is : " + truck.getSpeed());
System.out.println("Stopped Bike Speed is : " + bike.getSpeed());
```

With this, we have successfully completed the implementation of the `VehicleRunner` class and its inner `Vehicle` class.

### Student File

**VehicleRunner.java**

```

public class VehicleRunner {
    public static class Vehicle {
        // Write your code
    }
    
    public static void main(String[] args) {
       // Vehicle car = new Vehicle(30, "Car");
       // Write your code
    }

   
}
```

  
  

### Solution File

**VehicleRunner.java**

```
public class VehicleRunner {
    public static class Vehicle {
        private int speed;
        private String type;

        public Vehicle(int speed, String type) {
            if (speed > 0) {
                this.speed = speed;
            }
            this.type = type;
        }

        public Vehicle() {
            this.speed = 10;
            this.type = "Bike";
        }

        public void startEngine() {
            System.out.println("Engine started!");
        }

        public void stopEngine() {
            System.out.println("Engine stopped!");
            this.speed = 0;
        }

        public int getSpeed() {
            return speed;
        }

        public String getType() {
            return type;
        }
    }
    
    public static void main(String[] args) {
        Vehicle car = new Vehicle(30, "Car");
        Vehicle truck = new Vehicle(20, "Truck");
        Vehicle bike = new Vehicle();

        car.startEngine();
        truck.startEngine();
        bike.startEngine();

        System.out.println("Earlier Car Speed is : " + car.getSpeed() + ", Type: " + car.getType());
        System.out.println("Earlier Truck Speed is : " + truck.getSpeed() + ", Type: " + truck.getType());
        System.out.println("Earlier Bike Speed is : " + bike.getSpeed() + ", Type: " + bike.getType());

        car.stopEngine();
        truck.stopEngine();
        bike.stopEngine();

        System.out.println("Stopped Car Speed is : " + car.getSpeed());
        System.out.println("Stopped Truck Speed is : " + truck.getSpeed());
        System.out.println("Stopped Bike Speed is : " + bike.getSpeed());
    }

   
}

```


### Evaluation File

**Evaluate.java**

```

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class Evaluate {
    @Test
    public void testStartEngine() {
        VehicleRunner.Vehicle car = new VehicleRunner.Vehicle(30, "Car");
        VehicleRunner.Vehicle truck = new VehicleRunner.Vehicle(20, "Truck");
        VehicleRunner.Vehicle bike = new VehicleRunner.Vehicle();

        car.startEngine();
        truck.startEngine();
        bike.startEngine();

        System.out.println("Car Speed after starting engine: " + car.getSpeed());
        System.out.println("Truck Speed after starting engine: " + truck.getSpeed());
        System.out.println("Bike Speed after starting engine: " + bike.getSpeed());

        assertEquals(30, car.getSpeed());
        assertEquals(20, truck.getSpeed());
        assertEquals(10, bike.getSpeed());
    }

    @Test
    public void testStopEngine() {
        VehicleRunner.Vehicle car = new VehicleRunner.Vehicle(30, "Car");
        VehicleRunner.Vehicle truck = new VehicleRunner.Vehicle(20, "Truck");
        VehicleRunner.Vehicle bike = new VehicleRunner.Vehicle();

        car.startEngine();
        truck.startEngine();
        bike.startEngine();

        car.stopEngine();
        truck.stopEngine();
        bike.stopEngine();

        System.out.println("Car Speed after stopping engine: " + car.getSpeed());
        System.out.println("Truck Speed after stopping engine: " + truck.getSpeed());
        System.out.println("Bike Speed after stopping engine: " + bike.getSpeed());

        assertEquals(0, car.getSpeed());
        assertEquals(0, truck.getSpeed());
        assertEquals(0, bike.getSpeed());
    }

    @Test
    public void testGetType() {
        VehicleRunner.Vehicle car = new VehicleRunner.Vehicle(30, "Car");
        VehicleRunner.Vehicle truck = new VehicleRunner.Vehicle(20, "Truck");
        VehicleRunner.Vehicle bike = new VehicleRunner.Vehicle();

        System.out.println("Car type: " + car.getType());
        System.out.println("Truck type: " + truck.getType());
        System.out.println("Bike type: " + bike.getType());

        assertEquals("Car", car.getType());
        assertEquals("Truck", truck.getType());
        assertEquals("Bike", bike.getType());
    }
}


```