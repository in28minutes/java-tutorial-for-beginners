
## Exercise 1: Implementing Encapsulation Techniques in the VideoGame Class Part 1

  

## Instructions


**Instructions**

**Task 1: Implement VideoGame class attributes**

In the given `VideoGameRunner` class, add the following attributes to the `VideoGame` class:

-   `title` of type `String`
    
-   `numberOfCopies` of type `int`
    

**Task 2: Implement methods for VideoGame class**

Implement the following methods for the `VideoGame` class:

-   `setTitle(String gameTitle)`: Sets the title of the video game.
    
-   `getTitle()`: Returns the title of the video game.
    
-   `setNumberOfCopies(int numberOfCopies)`: Sets the number of copies if the provided number is greater than or equal to 0.
    
-   `getNumberOfCopies()`: Returns the number of copies.
    

**Task 3: Test the VideoGame class in the main method**

In the `main` method of the `VideoGameRunner` class, do the following:

1.  Create three instances of the `VideoGame` class and set their titles as follows:
    
    -   Create an instance named `rdr2` and set its title to "Red Dead Redemption 2".
        
    -   Create an instance named `tw3` and set its title to "The Witcher 3".
        
    -   Create an instance named `botw` and set its title to "Breath of the Wild".
        
2.  Set the number of copies for each video game instance as follows:
    
    -   Set the number of copies for `rdr2` to 5.
        
    -   Set the number of copies for `tw3` to 8.
        
    -   Set the number of copies for `botw` to 10.
        
3.  After setting the number of copies for each video game instance, print the title and number of copies for each video game instance using the following format:
    
 ```
 System.out.println(videoGameInstance.getTitle() + " - Number of copies: " + videoGameInstance.getNumberOfCopies());
```
        

**The output should look like:**

  
```
Red Dead Redemption 2 - Number of copies: 5
The Witcher 3 - Number of copies: 8
Breath of the Wild - Number of copies: 10
```

## Hints

1.  Task 1 requires you to add the attributes `title` and `numberOfCopies` to the `VideoGame` class. To do this, you need to declare these attributes as private instance variables in the `VideoGame` class.
    
2.  Task 2 requires you to implement four methods in the `VideoGame` class: `setTitle(String gameTitle)`, `getTitle()`, `setNumberOfCopies(int numberOfCopies)`, and `getNumberOfCopies()`. Remember to use appropriate access modifiers and parameter types for each method.
    
3.  For Task 3, start by creating three instances of the `VideoGame` class: `rdr2`, `tw3`, and `botw`. Then use the `setTitle(String gameTitle)` method to set the title of each instance, and use the `setNumberOfCopies(int numberOfCopies)` method to set the number of copies for each instance.
    
4.  After setting the number of copies for each instance, use the `getTitle()` and `getNumberOfCopies()` methods to print the title and number of copies for each instance using the format shown in the problem statement.
    

I hope these hints help you complete the exercise!
  

## Solution Explanation

In this problem, we need to implement a VideoGame class and test it in the main method of the VideoGameRunner class.

**Task 1: Implement VideoGame class attributes**

In the VideoGame class, we need to add two attributes: `title` of type `String` and `numberOfCopies` of type `int`.

```
public class VideoGame {
    private String title;
    private int numberOfCopies;
}
```

**Task 2: Implement methods for VideoGame class**

In the VideoGame class, we need to implement four methods: `setTitle`, `getTitle`, `setNumberOfCopies`, and `getNumberOfCopies`.

`setTitle(String gameTitle)`: Sets the title of the video game.

```
public void setTitle(String gameTitle) {
    title = gameTitle;
}
```

`getTitle()`: Returns the title of the video game.

```
public String getTitle() {
    return title;
}
```

`setNumberOfCopies(int numberOfCopies)`: Sets the number of copies if the provided number is greater than or equal to 0.

```
public void setNumberOfCopies(int numberOfCopies) {
    if (numberOfCopies >= 0) {
        this.numberOfCopies = numberOfCopies;
    }
}` 
```

`getNumberOfCopies()`: Returns the number of copies.

```
public int getNumberOfCopies() {
    return numberOfCopies;
}
```

**Task 3: Test the VideoGame class in the main method**

In the main method of the VideoGameRunner class, we need to create three instances of the VideoGame class and set their titles. Then, we need to set the number of copies for each video game instance and print the title and number of copies for each video game instance.

```
public static void main(String[] args) {
    VideoGame rdr2 = new VideoGame();
    rdr2.setTitle("Red Dead Redemption 2");
    rdr2.setNumberOfCopies(5);

    VideoGame tw3 = new VideoGame();
    tw3.setTitle("The Witcher 3");
    tw3.setNumberOfCopies(8);

    VideoGame botw = new VideoGame();
    botw.setTitle("Breath of the Wild");
    botw.setNumberOfCopies(10);

    System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
    System.out.println(tw3.getTitle() + " - Number of copies: " + tw3.getNumberOfCopies());
    System.out.println(botw.getTitle() + " - Number of copies: " + botw.getNumberOfCopies());
}
```

The above code creates three VideoGame instances `rdr2`, `tw3`, and `botw`. Then, it sets the titles and number of copies for each instance. Finally, it prints the title and number of copies for each video game instance.

The output of the above code is:

```
Red Dead Redemption 2 - Number of copies: 5
The Witcher 3 - Number of copies: 8
Breath of the Wild - Number of copies: 10
```

This output matches the expected output mentioned in the problem statement.
 

## Student File

**VideoGameRunner.java**

```
public class VideoGameRunner {

    static class VideoGame {
        // Add two private attributes: title (type: String) and numberOfCopies (type: int)

        // Implement setTitle method: public void setTitle(String gameTitle)

        // Implement getTitle method: public String getTitle()

        // Implement setNumberOfCopies method: public void setNumberOfCopies(int numberOfCopies) with a condition to check if numberOfCopies is greater than or equal to 0

        // Implement getNumberOfCopies method: public int getNumberOfCopies()
    }

    public static void main(String[] args) {
        // Create a VideoGame instance called rdr2 and set its title to "Red Dead Redemption 2"
        // Set the number of copies for rdr2 to 5
        // VideoGame rdr2 = new VideoGame();
        // rdr2.setTitle("Red Dead Redemption 2");
        // rdr2.setNumberOfCopies(5);

        // Create a VideoGame instance called tw3 and set its title to "The Witcher 3"
        // Set the number of copies for tw3 to 8

        // Create a VideoGame instance called botw and set its title to "Breath of the Wild"
        // Set the number of copies for botw to 10

        // Print the title and number of copies for each instance in the format: "Title - Number of copies: X"
        // System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
    }
}

```

  
  

## Solution File

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
    }

    public static void main(String[] args) {
        VideoGame rdr2 = new VideoGame();
        rdr2.setTitle("Red Dead Redemption 2");
        rdr2.setNumberOfCopies(5);

        VideoGame tw3 = new VideoGame();
        tw3.setTitle("The Witcher 3");
        tw3.setNumberOfCopies(8);

        VideoGame botw = new VideoGame();
        botw.setTitle("Breath of the Wild");
        botw.setNumberOfCopies(10);

        System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
        System.out.println(tw3.getTitle() + " - Number of copies: " + tw3.getNumberOfCopies());
        System.out.println(botw.getTitle() + " - Number of copies: " + botw.getNumberOfCopies());
    }
}

```

    

## Evaluation File

**Evaluate.java**

```
import com.udemy.ucp.IOHelper;

import com.udemy.ucp.EvaluationHelper;

import org.junit.jupiter.api.Test;

import java.util.logging.Logger;

import static org.junit.jupiter.api.Assertions.assertEquals;

import static org.junit.jupiter.api.Assertions.assertTrue;

import static org.junit.jupiter.api.Assertions.fail;



public class Evaluate {



    IOHelper helper = new IOHelper();

    EvaluationHelper evaluationHelper = new EvaluationHelper();

    VideoGameRunner.VideoGame videoGame = new VideoGameRunner.VideoGame();



    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());



    @Test

    public void testMainMethod() {

        helper.resetStdOut(); // clean stdout

        VideoGameRunner.main(new String[] {});

        String actualOutput = helper.getOutput();

        String refinedActualOutput = helper.getOutput().replace("\n", " ");



        String expectedOutput = "Red Dead Redemption 2 - Number of copies: 5\n" +

            "The Witcher 3 - Number of copies: 8\n" +

            "Breath of the Wild - Number of copies: 10\n";

        LOGGER.info("Expected Output: " + expectedOutput);

        LOGGER.info("Actual Output: " + actualOutput);

        assertEquals(expectedOutput, actualOutput, "Output does not match the expected value. Please check user logs for more detailed view. Expected: Red Dead Redemption 2 - Number of copies: 5 " +

            "The Witcher 3 - Number of copies: 8 " +

            "Breath of the Wild - Number of copies: 10 " + ", actual: " + refinedActualOutput);

    }

    @Test

    public void testRdr2Output() {

        helper.resetStdOut(); // clean stdout

        VideoGameRunner.main(new String[] {});

        String actualOutput = helper.getOutput();

        assertTrue(actualOutput.contains("Red Dead Redemption 2 - Number of copies: 5"), "Output does not contain expected string: Red Dead Redemption 2 - Number of copies: 5");

    }



    @Test

    public void testTw3Output() {

        helper.resetStdOut(); // clean stdout

        VideoGameRunner.main(new String[] {});

        String actualOutput = helper.getOutput();

        assertTrue(actualOutput.contains("The Witcher 3 - Number of copies: 8"), "Output does not contain expected string: The Witcher 3 - Number of copies: 8");

    }



    @Test

    public void testBotwOutput() {

        helper.resetStdOut(); // clean stdout

        VideoGameRunner.main(new String[] {});

        String actualOutput = helper.getOutput();

        assertTrue(actualOutput.contains("Breath of the Wild - Number of copies: 10"), "Output does not contain expected string: Breath of the Wild - Number of copies: 10");

    }

    @Test

    public void testFieldsAndMethods() {

        if (!evaluationHelper.isFieldDeclared(videoGame, "title", String.class)) {

            fail("'title' field is not declared.");

        }

        if (!evaluationHelper.isFieldDeclared(videoGame, "numberOfCopies", int.class)) {

            fail("'numberOfCopies' field is not declared.");

        }

        if (!evaluationHelper.isMethodDeclared(videoGame, "setTitle", String.class)) {

            fail("'setTitle' method is not declared.");

        }

        if (!evaluationHelper.isMethodDeclared(videoGame, "getTitle")) {

            fail("'getTitle' method is not declared.");

        }

        if (!evaluationHelper.isMethodDeclared(videoGame, "setNumberOfCopies", int.class)) {

            fail("'setNumberOfCopies' method is not declared.");

        }

        if (!evaluationHelper.isMethodDeclared(videoGame, "getNumberOfCopies")) {

            fail("'getNumberOfCopies' method is not declared.");

        }

    }

}

```







## Exercise 2: Implementing Encapsulation Techniques in the VideoGame Class Part 2

  

## Instructions


You are asked to implement methods for the `VideoGame` class and perform some operations in the `main` method of the `VideoGameRunner` class.

### Task 1: Implement methods for VideoGame class

Implement the following methods for the `VideoGame` class:

1.  `increaseCopies(int howMuch)`: Increases the number of copies of the video game instance by the provided integer value, only if the value is greater than 0.
    
2.  `decreaseCopies(int howMuch)`: Decreases the number of copies of the video game instance by the provided integer value, only if the value is greater than 0 and the resulting value is not negative. If the resulting value is negative, then the `numberOfCopies` attribute is set to 0.
    

### Task 2: Perform operations in the main method of VideoGameRunner class

In the `main` method of the `VideoGameRunner` class, do the following:

1.  Increase the number of copies for each video game instance as follows:
    
    -   Increase the number of copies for `rdr2` by 12.
    -   Increase the number of copies for `tw3` by 18.
    -   Increase the number of copies for `botw` by 24.
2.  After increasing the number of copies for each video game instance, print the title and number of copies for each video game instance using the following format:
    
    ```
    System.out.println(videoGameInstance.getTitle() + " - Number of copies after increasing copies : " + videoGameInstance.getNumberOfCopies());
    ```
    
3.  Decrease the number of copies for each video game instance as follows:
    
    -   Decrease the number of copies for `rdr2` by 6.
    -   Decrease the number of copies for `tw3` by 12.
    -   Decrease the number of copies for `botw` by 18.
4.  After decreasing the number of copies for each video game instance, print the title and number of copies for each video game instance using the following format:
    
   ```
   System.out.println(videoGameInstance.getTitle() + " - Number of copies after decreasing copies : " + videoGameInstance.getNumberOfCopies());
   ```
    

The output should look like this:

```
Red Dead Redemption 2 - Number of copies: 5
The Witcher 3 - Number of copies: 8
Breath of the Wild - Number of copies: 10
Red Dead Redemption 2 - Number of copies after increasing copies : 17
The Witcher 3 - Number of copies after increasing copies : 26
Breath of the Wild - Number of copies after increasing copies : 34
Red Dead Redemption 2 - Number of copies after decreasing copies : 11
The Witcher 3 - Number of copies after decreasing copies : 14
Breath of the Wild - Number of copies after decreasing copies : 16
```

## Hints


1.  **Hint 1**: To implement the `increaseCopies()` method, first create a public method with the signature `public void increaseCopies(int howMuch)`. Inside the method, check if `howMuch` is greater than 0, and if it is, add `howMuch` to `numberOfCopies`.
    
2.  **Hint 2**: To implement the `decreaseCopies()` method, first create a public method with the signature `public void decreaseCopies(int howMuch)`. Inside the method, check if `howMuch` is greater than 0 and if the result of `numberOfCopies - howMuch` is greater than or equal to 0. If both conditions are true, subtract `howMuch` from `numberOfCopies`. If the resulting value is negative, set `numberOfCopies` to 0.
    
3.  **Hint 3**: After implementing the `increaseCopies()` and `decreaseCopies()` methods, use them to increase and decrease the number of copies for each video game instance, as specified in the instructions.
    
4.  **Hint 4**: To print the updated number of copies after increasing and decreasing the copies, use the given format `System.out.println(videoGameInstance.getTitle() + " - Number of copies after (increasing/decreasing) copies : " + videoGameInstance.getNumberOfCopies());` after calling the respective methods.
  

## Solution Explanation


The solution to this task can be broken down into two parts: implementing the `increaseCopies` and `decreaseCopies` methods for the `VideoGame` class, and then calling these methods in the `main` method of the `VideoGameRunner` class as instructed.

### Implementing the increaseCopies and decreaseCopies methods

First, we need to implement the `increaseCopies` and `decreaseCopies` methods inside the `VideoGame` class:

```
public void increaseCopies(int howMuch) {
    if (howMuch > 0) {
        numberOfCopies += howMuch;
    }
}

public void decreaseCopies(int howMuch) {
    if (howMuch > 0 && numberOfCopies >= howMuch) {
        numberOfCopies -= howMuch;
    } else {
        numberOfCopies = 0;
    }
}
```

In the `increaseCopies` method, we check if the provided integer value `howMuch` is greater than 0. If it is, we increase the `numberOfCopies` attribute by `howMuch`.

In the `decreaseCopies` method, we again check if the provided integer value `howMuch` is greater than 0, and also if the `numberOfCopies` attribute is greater than or equal to `howMuch`. If both conditions are satisfied, we decrease the `numberOfCopies` attribute by `howMuch`. Otherwise, we set the `numberOfCopies` attribute to 0.

### Calling the increaseCopies and decreaseCopies methods in the main method

Next, we need to call the `increaseCopies` and `decreaseCopies` methods for each video game instance as instructed, and print the number of copies after each operation:

```
// Increase the number of copies
rdr2.increaseCopies(12);
tw3.increaseCopies(18);
botw.increaseCopies(24);

// Print number of copies after increasing copies
System.out.println(rdr2.getTitle() + " - Number of copies after increasing copies : " + rdr2.getNumberOfCopies());
System.out.println(tw3.getTitle() + " - Number of copies after increasing copies : " + tw3.getNumberOfCopies());
System.out.println(botw.getTitle() + " - Number of copies after increasing copies : " + botw.getNumberOfCopies());

// Decrease the number of copies
rdr2.decreaseCopies(6);
tw3.decreaseCopies(12);
botw.decreaseCopies(18);

// Print number of copies after decreasing copies
System.out.println(rdr2.getTitle() + " - Number of copies after decreasing copies : " + rdr2.getNumberOfCopies());
System.out.println(tw3.getTitle() + " - Number of copies after decreasing copies : " + tw3.getNumberOfCopies());
System.out.println(botw.getTitle() + " - Number of copies after decreasing copies : " + botw.getNumberOfCopies());
```

We first increase the number of copies for each video game instance by calling the `increaseCopies` method with the specified values (12 for `rdr2`, 18 for `tw3`, and 24 for `botw`). Then, we print the number of copies after increasing copies using the provided format.

Next, we decrease the number of copies for each video game instance by calling the `decreaseCopies` method with the specified values (6 for `rdr2`, 12 for `tw3`, and 18 for `botw`). Finally, we print the number of copies after decreasing copies using the provided format.

After incorporating these changes, the main method of the `VideoGameRunner` class should look like this:

```
public static void main(String[] args) {
    VideoGame rdr2 = new VideoGame();
    rdr2.setTitle("Red Dead Redemption 2");
    rdr2.setNumberOfCopies(5);

    VideoGame tw3 = new VideoGame();
    tw3.setTitle("The Witcher 3");
    tw3.setNumberOfCopies(8);

    VideoGame botw = new VideoGame();
    botw.setTitle("Breath of the Wild");
    botw.setNumberOfCopies(10);

    System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
    System.out.println(tw3.getTitle() + " - Number of copies: " + tw3.getNumberOfCopies());
    System.out.println(botw.getTitle() + " - Number of copies: " + botw.getNumberOfCopies());

    // Increase the number of copies
    rdr2.increaseCopies(12);
    tw3.increaseCopies(18);
    botw.increaseCopies(24);

    // Print number of copies after increasing copies
    System.out.println(rdr2.getTitle() + " - Number of copies after increasing copies : " + rdr2.getNumberOfCopies());
    System.out.println(tw3.getTitle() + " - Number of copies after increasing copies : " + tw3.getNumberOfCopies());
    System.out.println(botw.getTitle() + " - Number of copies after increasing copies : " + botw.getNumberOfCopies());

    // Decrease the number of copies
    rdr2.decreaseCopies(6);
    tw3.decreaseCopies(12);
    botw.decreaseCopies(18);

    // Print number of copies after decreasing copies
    System.out.println(rdr2.getTitle() + " - Number of copies after decreasing copies : " + rdr2.getNumberOfCopies());
    System.out.println(tw3.getTitle() + " - Number of copies after decreasing copies : " + tw3.getNumberOfCopies());
    System.out.println(botw.getTitle() + " - Number of copies after decreasing copies : " + botw.getNumberOfCopies());
}
```

When executed, this code will produce the expected output:

```
Red Dead Redemption 2 - Number of copies: 5
The Witcher 3 - Number of copies: 8
Breath of the Wild - Number of copies: 10
Red Dead Redemption 2 - Number of copies after increasing copies : 17
The Witcher 3 - Number of copies after increasing copies : 26
Breath of the Wild - Number of copies after increasing copies : 34
Red Dead Redemption 2 - Number of copies after decreasing copies : 11
The Witcher 3 - Number of copies after decreasing copies : 14
Breath of the Wild - Number of copies after decreasing copies : 16` 
```

This solution implements the required methods for the `VideoGame` class and demonstrates their functionality within the `main` method of the `VideoGameRunner` class.
 

## Student File

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
        
        // TODO: Implement the increaseCopies() and decreaseCopies() methods for the VideoGame class

    }

    public static void main(String[] args) {
        VideoGame rdr2 = new VideoGame();
        rdr2.setTitle("Red Dead Redemption 2");
        rdr2.setNumberOfCopies(5);

        VideoGame tw3 = new VideoGame();
        tw3.setTitle("The Witcher 3");
        tw3.setNumberOfCopies(8);

        VideoGame botw = new VideoGame();
        botw.setTitle("Breath of the Wild");
        botw.setNumberOfCopies(10);

        // Print initial number of copies for each video game
        System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
        System.out.println(tw3.getTitle() + " - Number of copies: " + tw3.getNumberOfCopies());
        System.out.println(botw.getTitle() + " - Number of copies: " + botw.getNumberOfCopies());
        
        // TODO: Increase the number of copies for each video game instance and print the updated number of copies
        
        rdr2.increaseCopies(12);
        
        // TODO: Print the updated number of copies for rdr2 after increasing copies
        
        System.out.println(rdr2.getTitle() + " - Number of copies after increasing copies : " + rdr2.getNumberOfCopies());
        
        // TODO: Decrease the number of copies for each video game instance and print the updated number of copies
        
        rdr2.decreaseCopies(6);
        
        // TODO: Print the updated number of copies for rdr2 after decreasing copies
        System.out.println(rdr2.getTitle() + " - Number of copies after decreasing copies : " + rdr2.getNumberOfCopies());
    }
}

```

  
  

## Solution File

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
          if (howMuch > 0) {
         numberOfCopies += howMuch;
        }
    }

    public void decreaseCopies(int howMuch) {
    if (howMuch > 0 && numberOfCopies >= howMuch) {
        numberOfCopies -= howMuch;
    } else {
        numberOfCopies = 0;
    }
       }

    }

    public static void main(String[] args) {
        VideoGame rdr2 = new VideoGame();
        rdr2.setTitle("Red Dead Redemption 2");
        rdr2.setNumberOfCopies(5);

        VideoGame tw3 = new VideoGame();
        tw3.setTitle("The Witcher 3");
        tw3.setNumberOfCopies(8);

        VideoGame botw = new VideoGame();
        botw.setTitle("Breath of the Wild");
        botw.setNumberOfCopies(10);

        System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
        System.out.println(tw3.getTitle() + " - Number of copies: " + tw3.getNumberOfCopies());
        System.out.println(botw.getTitle() + " - Number of copies: " + botw.getNumberOfCopies());
        
        
        rdr2.increaseCopies(12);
        tw3.increaseCopies(18);
        botw.increaseCopies(24);
        
        System.out.println(rdr2.getTitle() + " - Number of copies after increasing copies : " + rdr2.getNumberOfCopies());
        System.out.println(tw3.getTitle() + " - Number of copies after increasing copies : " + tw3.getNumberOfCopies());
        System.out.println(botw.getTitle() + " - Number of copies after increasing copies : " + botw.getNumberOfCopies());
        
        rdr2.decreaseCopies(6);
        tw3.decreaseCopies(12);
        botw.decreaseCopies(18);
        
        System.out.println(rdr2.getTitle() + " - Number of copies after decreasing copies : " + rdr2.getNumberOfCopies());
        System.out.println(tw3.getTitle() + " - Number of copies after decreasing copies : " + tw3.getNumberOfCopies());
        System.out.println(botw.getTitle() + " - Number of copies after decreasing copies : " + botw.getNumberOfCopies());
    }
}

```

    

## Evaluation File

**Evaluate.java**

```
import com.udemy.ucp.IOHelper;
import org.junit.jupiter.api.Test;
import java.util.logging.Logger;
import static org.junit.jupiter.api.Assertions.assertEquals;
import static org.junit.jupiter.api.Assertions.assertTrue;

public class Evaluate {

    IOHelper helper = new IOHelper();
    private static final Logger LOGGER = Logger.getLogger(Evaluate.class.getName());

    @Test
    public void testSetAndGetMethods() {
        try {
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredMethod("setTitle", String.class) != null, "Method setTitle is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredMethod("getTitle") != null, "Method getTitle is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredMethod("setNumberOfCopies", int.class) != null, "Method setNumberOfCopies is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredMethod("getNumberOfCopies") != null, "Method getNumberOfCopies is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredMethod("increaseCopies", int.class) != null, "Method increaseCopies is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredMethod("decreaseCopies", int.class) != null, "Method decreaseCopies is not declared in VideoGame class.");

            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredField("title") != null, "Field title is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredField("numberOfCopies") != null, "Field numberOfCopies is not declared in VideoGame class.");
        } catch (NoSuchMethodException | NoSuchFieldException e) {
            LOGGER.severe("Error: " + e.getMessage());
        }
    }

    @Test
    public void testMainMethod() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[] {});
        String actualOutput = helper.getOutput().trim(); // remove leading/trailing whitespaces
        String[] lines = actualOutput.split("\n"); // split by line

        // check each line to match expected format
        assertEquals("Red Dead Redemption 2 - Number of copies: 5", lines[0]);
        assertEquals("The Witcher 3 - Number of copies: 8", lines[1]);
        assertEquals("Breath of the Wild - Number of copies: 10", lines[2]);
        assertTrue(lines[3].startsWith("Red Dead Redemption 2 - Number of copies after increasing copies : "));
        assertTrue(lines[4].startsWith("The Witcher 3 - Number of copies after increasing copies : "));
        assertTrue(lines[5].startsWith("Breath of the Wild - Number of copies after increasing copies : "));
        assertTrue(lines[6].startsWith("Red Dead Redemption 2 - Number of copies after decreasing copies : "));
        assertTrue(lines[7].startsWith("The Witcher 3 - Number of copies after decreasing copies : "));
        assertTrue(lines[8].startsWith("Breath of the Wild - Number of copies after decreasing copies : "));
    }


    @Test
    public void testRdr2Output() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[] {});
        String actualOutput = helper.getOutput();
        assertTrue(actualOutput.contains("Red Dead Redemption 2 - Number of copies: 5"), "Output does not contain expected string: Red Dead Redemption 2 - Number of copies: 5");
    }

    @Test
    public void testTw3Output() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[] {});
        String actualOutput = helper.getOutput();
        assertTrue(actualOutput.contains("The Witcher 3 - Number of copies: 8"), "Output does not contain expected string: The Witcher 3 - Number of copies: 8");
    }

    @Test
    public void testBotwOutput() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[] {});
        String actualOutput = helper.getOutput();
        assertTrue(actualOutput.contains("Breath of the Wild - Number of copies: 10"), "Output does not contain expected string: Breath of the Wild - Number of copies: 10");
    }

    @Test
    public void testIncreaseCopies() {
        VideoGameRunner.VideoGame game = new VideoGameRunner.VideoGame();
        game.setNumberOfCopies(10);
        game.increaseCopies(5);
        assertEquals(15, game.getNumberOfCopies(), "Number of copies did not increase by the expected amount.");
    }

    @Test
    public void testDecreaseCopies() {
        VideoGameRunner.VideoGame game = new VideoGameRunner.VideoGame();
        game.setNumberOfCopies(10);
        game.decreaseCopies(5);
        assertEquals(5, game.getNumberOfCopies(), "Number of copies did not decrease by the expected amount.");
    }

    @Test
    public void testIncreaseCopiesOutput() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[] {});
        String actualOutput = helper.getOutput();
        assertTrue(actualOutput.contains("Red Dead Redemption 2 - Number of copies after increasing copies : 17"), "Output does not contain expected string: Red Dead Redemption 2 - Number of copies after increasing copies : 17");
        assertTrue(actualOutput.contains("The Witcher 3 - Number of copies after increasing copies : 26"), "Output does not contain expected string: The Witcher 3 - Number of copies after increasing copies : 26");
        assertTrue(actualOutput.contains("Breath of the Wild - Number of copies after increasing copies : 34"), "Output does not contain expected string: Breath of the Wild - Number of copies after increasing copies : 34");
    }

    @Test
    public void testDecreaseCopiesOutput() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[] {});
        String actualOutput = helper.getOutput();
        assertTrue(actualOutput.contains("Red Dead Redemption 2 - Number of copies after decreasing copies : 11"), "Output does not contain expected string: Red Dead Redemption 2 - Number of copies after decreasing copies : 11");
        assertTrue(actualOutput.contains("The Witcher 3 - Number of copies after decreasing copies : 14"), "Output does not contain expected string: The Witcher 3 - Number of copies after decreasing copies : 14");
        assertTrue(actualOutput.contains("Breath of the Wild - Number of copies after decreasing copies : 16"), "Output does not contain expected string: Breath of the Wild - Number of copies after decreasing copies : 16");
    }
}
```