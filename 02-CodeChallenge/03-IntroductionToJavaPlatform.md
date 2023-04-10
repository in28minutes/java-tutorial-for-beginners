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
import com.udemy.ucp.IOHelper;

public class Evaluate {
    Exercise ex = new Exercise();
    IOHelper helper = new IOHelper();
    
    @Test
    public void testHelloWorld() {
        helper.resetStdOut(); // clean stdout
        Exercise.main(null);
        assertEquals("Hello World\n", helper.getOutput(), "The output should be 'Hello World'");
    }
}

```

<!---

### Exercise 2:  Printing a Message with the Exercise Class

#### Instructions

**Task**

Your task is to create a Java class called `**Exercise**` that includes a method called `**exerciseComplete**` which prints the message "I have completed the exercise" to the console. You will also need to create a `**main**` method that creates an instance of the `**Exercise**` class and calls the `**exerciseComplete**` method on this instance. The purpose of this exercise is to help you gain experience in creating classes, methods, and console output in Java.

**Steps**

Follow these steps to complete the exercise:

1.  Open your preferred text editor or IDE and create a new file named `**Exercise.java**`.
    
2.  Inside the `**Exercise**` class, create a method called `**exerciseComplete**` that takes no arguments and returns void.
    
3.  Inside the `**exerciseComplete**` method, use the `**System.out.println()**` statement to print the message "I have completed the exercise" to the console.
    
4.  Inside the `**Exercise**` class, create a `**main**` method that takes no arguments and returns void.
    
5.  Inside the `**main**` method, create a new instance of the `**Exercise**` class using the `**new**` keyword and store it in a variable.
    
6.  Call the `**exerciseComplete**` method on the instance of the `**Exercise**` class using the dot notation.
    
7.  Run the code and ensure that the message "I have completed the exercise" is printed to the console.

#### Hints
Create a file named `**Exercise.java**` with the following instructions:

1.  Create a class called `**Exercise**`.
    
2.  Inside the class, create a method called `**exerciseComplete**` that prints the message "I have completed the exercise" to the console using the `**System.out.println()**` statement.
    
3.  Inside the class, create a `**main**` method that creates a new instance of the `**Exercise**` class and calls the `**exerciseComplete**` method on this instance.
    
4.  Save the file and run the program to ensure that the message "I have completed the exercise" is printed to the console.

#### Solution Explanation

The goal of this exercise is to create a Java class called `**Exercise**` that includes a method called `**exerciseComplete**` that prints the message "I have completed the exercise" to the console, and a `**main**` method that creates an instance of the `**Exercise**` class and calls the `**exerciseComplete**` method on this instance. Here's an implementation of the solution:

```
public class Exercise {
    public void exerciseComplete() {
        System.out.println("I have completed the exercise");
    }

    public static void main(String[] args) {
        Exercise myExercise = new Exercise();
        myExercise.exerciseComplete();
    }
}
```

The `**Exercise**` class defines a method called `**exerciseComplete**` that prints the message "I have completed the exercise" to the console using the `**System.out.println()**` statement. The class also defines a `**main**` method that creates a new instance of the `**Exercise**` class using the `**new**` keyword and stores it in a variable called `**myExercise**`. Finally, the `**main**` method calls the `**exerciseComplete**` method on the `**myExercise**` instance using the dot notation.

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
    void exerciseComplete() {
        System.out.println("I have completed the exercise");
    }

    public static void main(String[] args) {
        Exercise myExercise = new Exercise();
        myExercise.exerciseComplete();
    }
}

```

#### Evaluation File
**Evaluate.java**
```
import static org.junit.jupiter.api.Assertions.*;
import org.junit.jupiter.api.Test;
import java.io.ByteArrayOutputStream;
import java.io.PrintStream;

public class Evaluate {
    @Test
    public void testExerciseOutput() {
        // Redirect output to a ByteArrayOutputStream
        ByteArrayOutputStream outputStream = new ByteArrayOutputStream();
        PrintStream printStream = new PrintStream(outputStream);
        System.setOut(printStream);
        
        // Create an instance of the Exercise class and call the exerciseComplete method
        Exercise exercise = new Exercise();
        exercise.exerciseComplete();
        
        // Verify that the output contains the message "I have completed the exercise"
        String output = outputStream.toString();
        assertEquals("I have completed the exercise\n", output);
    }
}
```

--->