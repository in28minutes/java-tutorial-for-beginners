### Exercise 1  Print Hello World

#### Instructions
In this exercise, you are required to write a Java program that prints the message "Hello World" to the console. Your program should contain a `**main**` method that prints this message using the `**System.out.println()**` statement.

Before attempting this exercise, learners should have a basic understanding of Java programming concepts, including syntax and the use of the `**System.out.println()**` statement. Learners should also be familiar with setting up and running Java programs using a command line interface or an integrated development environment (IDE).

#### Hints
-   Use the `**System.out.println()**` statement to print the message "Hello World"
    
-   Remember to use quotation marks to indicate that the text is a string

#### Solution Explanation
Here is an example of a possible solution:

  
```
public class Exercise {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

The code above creates a class called `**Exercise**` with a `**main**` method that prints the string "Hello World" to the console using the `**System.out.println()**` statement.

The key concept used in this solution is the `**System.out.println()**` statement, which is used to print text to the console. In this case, we pass the string "Hello World" as an argument to the statement to print the message to the console.

When learners run the program, they should see the message "Hello World" printed to the console.

#### Student File
**Exercise.java**
```
public class Exercise {

}
```

#### Solution File
**Exercise.java**
```
public class Exercise {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

#### Evaluation File
**Evaluate.java**
```
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.assertEquals;
import java.io.ByteArrayOutputStream;
import java.io.PrintStream;

public class Evaluate {
    
    @Test
    public void testExerciseOutput() {
        // Redirect output to a ByteArrayOutputStream
        ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
        PrintStream printStream = new PrintStream(outputStream);
        System.setOut(printStream);
        
        // Call the main method of the Exercise class
        Exercise.main(null);
        
        // Verify that the output contains the message "Hello World"
        String output = outputStream.toString();
        assertEquals("Hello World\n", output);
    }
}
```
