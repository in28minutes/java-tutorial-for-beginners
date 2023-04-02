
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

    }

    public static void main(String[] args) {
        // VideoGame rdr2 = new VideoGame();
        //  rdr2.setTitle("Red Dead Redemption 2");
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
        videoGame = new VideoGameRunner.VideoGame();
    }

    @Test
    public void testSetTitleAndGetTitle() {
        LOGGER.info("Running testSetTitleAndGetTitle...");
        videoGame.setTitle("Test Game");
        assertEquals("Test Game", videoGame.getTitle());
    }

    @Test
    public void testSetNumberOfCopiesAndGetNumberOfCopies() {
        LOGGER.info("Running testSetNumberOfCopiesAndGetNumberOfCopies...");
        videoGame.setNumberOfCopies(10);
        assertEquals(10, videoGame.getNumberOfCopies());
    }

    @Test
    public void testIncreaseCopies() {
        LOGGER.info("Running testIncreaseCopies...");
        videoGame.setNumberOfCopies(5);
        videoGame.increaseCopies(5);
        assertEquals(10, videoGame.getNumberOfCopies());
    }

    @Test
    public void testDecreaseCopies() {
        LOGGER.info("Running testDecreaseCopies...");
        videoGame.setNumberOfCopies(10);
        videoGame.decreaseCopies(5);
        assertEquals(5, videoGame.getNumberOfCopies());
    }
}
```