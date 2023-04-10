
# ## Exercise 1: Implementing Encapsulation Techniques in the VideoGame Class

  

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
        // Complete the code
    }

    public static void main(String[] args) {
       
       // VideoGame rdr2 = new VideoGame();
       // rdr2.setTitle("Red Dead Redemption 2");
       // rdr2.setNumberOfCopies(5);
       // Complete the code 

        

       // System.out.println(rdr2.getTitle() + " - Number of copies: " + rdr2.getNumberOfCopies());
       // Complete the code
  
  
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

            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredField("title") != null, "Field title is not declared in VideoGame class.");
            assertTrue(VideoGameRunner.VideoGame.class.getDeclaredField("numberOfCopies") != null, "Field numberOfCopies is not declared in VideoGame class.");
        } catch (NoSuchMethodException | NoSuchFieldException e) {
            LOGGER.severe("Error: " + e.getMessage());
        }
    }

    @Test
    public void testMainMethod() {
        helper.resetStdOut(); // clean stdout
        VideoGameRunner.main(new String[]{});
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
    VideoGameRunner.main(new String[]{});
    String actualOutput = helper.getOutput();
    assertTrue(actualOutput.contains("Red Dead Redemption 2 - Number of copies: 5"), "Output does not contain expected string: Red Dead Redemption 2 - Number of copies: 5");
    }

   @Test
   public void testTw3Output() {
   helper.resetStdOut(); // clean stdout
   VideoGameRunner.main(new String[]{});
   String actualOutput = helper.getOutput();
   assertTrue(actualOutput.contains("The Witcher 3 - Number of copies: 8"), "Output does not contain expected string: The Witcher 3 - Number of copies: 8");
   }

   @Test
   public void testBotwOutput() {
   helper.resetStdOut(); // clean stdout
   VideoGameRunner.main(new String[]{});
   String actualOutput = helper.getOutput();
   assertTrue(actualOutput.contains("Breath of the Wild - Number of copies: 10"), "Output does not contain expected string: Breath of the Wild - Number of copies: 10");
   }
}

```