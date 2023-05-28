**Step 1: Introducing Exceptions**

**Question 1: What is an exception in Java?**
- A) An error that occurs during the execution of a program.
  - `Correct: An exception in Java is an event that occurs during the execution of a program that disrupts the normal flow of instructions.`

- B) A condition that indicates the successful completion of a program.
  - `Incorrect: An exception doesn't indicate the successful completion of a program. Instead, it represents an error or unusual condition.`

- C) A statement that is used to handle errors in a program.
  - `Incorrect: An exception itself is not a statement used to handle errors. It's an event that occurs during the execution of a program.`

**Question 2: Which of the following is an example of an exception?**
- A) A program running out of memory.
- B) A division by zero error.
- C) Both A and B.
  - `Correct: Both running out of memory and division by zero can cause exceptions in Java.`

**Question 3: What happens if an exception is not handled in a program?**
- A) The program continues running normally.
  - `Incorrect: If an exception is not handled, it will cause the program to terminate abruptly, not continue running normally.`

- B) The program terminates abruptly and an error message is displayed.
  - `Correct: If an exception is not handled in a program, it will cause the program to terminate abruptly and an error message will be displayed.`

- C) The program enters a loop until the exception is resolved.
  - `Incorrect: An unhandled exception causes the program to terminate abruptly, not enter a loop.`

**Step 2: Handling An Exception**

**Question 1: How can you handle an exception in Java?**
- A) By using the try-catch block.
  - `Correct: In Java, exceptions can be handled using try-catch blocks.`

- B) By using the if-else statement.
  - `Incorrect: if-else statements are used for decision making, not exception handling.`

- C) By using the throw keyword.
  - `Incorrect: The throw keyword is used to manually throw an exception, not to handle it.`

**Question 2: What is the purpose of the catch block in a try-catch block?**
- A) To define the code that may throw an exception.
  - `Incorrect: The code that may throw an exception is placed in the try block, not the catch block.`

- B) To handle the exception and provide an alternative code path.
  - `Correct: The catch block is used to handle the exception and provide an alternative code path when an exception occurs.`

- C) To specify the type of exception to be caught.
  - `Correct: In the declaration of a catch block, you specify the type of exception it can catch.`

**Question 3: What happens if an exception is caught in a catch block?**
- A) The program continues running normally after the catch block.
  - `Correct: If an exception is caught in a catch block, the program will continue running normally after the catch block.`

- B) The program terminates abruptly and an error message is displayed.
  - `Incorrect: If an exception is caught in a catch block, the program doesn't terminate abruptly.`

- C) The program enters a loop until the exception is resolved.
  - `Incorrect: The program doesn't enter a loop when an exception is caught.`

**Step 3: The Exception Hierarchy**

**Question 1: What is the root class of the Java exception hierarchy?**
- A) RuntimeException


  - `Incorrect: RuntimeException is a subclass of Exception, not the root class of the exception hierarchy.`

- B) Exception
  - `Incorrect: Exception is a subclass of Throwable, not the root class of the exception hierarchy.`

- C) Throwable
  - `Correct: The Throwable class is the superclass of all errors and exceptions in Java. It's the root of the exception hierarchy.`

**Question 2: Which of the following is true about the exception hierarchy in Java?**
- A) All exceptions in Java are subclasses of Exception.
  - `Incorrect: Not all exceptions in Java are subclasses of Exception. Error is a direct subclass of Throwable.`

- B) NullPointerException is a subclass of RuntimeException.
  - `Correct: NullPointerException is a subclass of RuntimeException.`

- C) Both A and B.
  - `Incorrect: Only B is correct.`

**Question 3: Why is it important to understand the exception hierarchy in Java?**
- A) It helps in determining the type of exception to catch.
  - `Correct: Understanding the exception hierarchy can help in determining which exceptions can be caught by a specific catch block.`

- B) It provides a way to handle different types of exceptions in a program.
  - `Correct: Understanding the exception hierarchy can help in handling different types of exceptions in a program.`

- C) Both A and B.
  - `Correct: Both A and B are valid reasons for understanding the exception hierarchy.`

**Step 4: The Need For finally**

**Question 1: What happens if a resource is not properly released in a program?**
- A) The program continues running normally.
  - `Incorrect: If a resource is not properly released, it may cause resource leaks and other issues in the program.`

- B) The program terminates abruptly and an error message is displayed.
  - `Incorrect: A program does not necessarily terminate abruptly if a resource isn't properly released, though it could lead to problems.`

- C) The resource remains in use and may cause issues in the program.
  - `Correct: If a resource is not properly released, it remains in use and can cause issues like resource leaks.`

**Question 2: How can you ensure that a resource is always released, even if an exception occurs?**
- A) By using the try-catch block.
  - `Incorrect: While a try-catch block can be used to handle exceptions, it doesn't ensure that resources are always released.`

- B) By using the finally block.
  - `Correct: The finally block is used to place important code that must be processed regardless of whether an exception is thrown or not. It's typically used for cleanup tasks such as closing database connections, I/O streams, etc.`

- C) By using the throw keyword.
  - `Incorrect: The throw keyword is used to manually throw an exception, not to ensure that resources are always released.`

**Question 3: When is the code inside the finally block executed?**
- A) Only when an exception occurs.
  - `Incorrect: The finally block is executed regardless of whether an exception occurs.`

- B) Only when there is no exception.
  - `Incorrect: The finally block is executed regardless of whether an exception occurs.`

- C) Whether an exception occurs or not.
  - `Correct: The finally block is always executed, whether an exception occurs or not.`

**Step 5: Programming Puzzles - PP-01**

*Puzzle-01: Would the finally clause be executed if the statement //str = "Hello"; remains as-is?*
- A) Yes
  - `Correct: The finally block is always executed, regardless of what code

 is commented out.`

- B) No
  - `Incorrect: The finally block is always executed, whether there's an exception or not.`

*Puzzle-02: When will code in a finally clause not get executed?*
- A) When an exception occurs in the try block.
  - `Incorrect: Even if an exception occurs in the try block, the finally block will still be executed.`

- B) When an exception occurs in the catch block.
  - `Incorrect: Even if an exception occurs in the catch block, the finally block will still be executed.`

- C) When an exception occurs in preceding statements within the same finally clause.
  - `Incorrect: If an exception occurs in the finally block, the rest of the block may not be executed, but this depends on the specific scenario and is not generally true.`

- D) When there is a JVM crash.
  - `Correct: If the JVM crashes or if the system exits (either by calling System.exit or by a system-wide issue), the finally block may not execute.`

*Puzzle-03: Will the following code, a try-finally without a catch, compile?*
- A) Yes
  - `Correct: In Java, you can use a try block without a catch block as long as you include a finally block.`

- B) No
  - `Incorrect: A try-finally block without a catch block will compile in Java.`

*Puzzle-04: Will the following code, a try without a catch or a finally, compile?*
- A) Yes
  - `Incorrect: A try block must be followed by either a catch block, a finally block, or both.`

- B) No
  - `Correct: In Java, a try block must be followed by either a catch block, a finally block, or both.`

**Step 6: Handling Exceptions: Do We Have A Choice?**

**Question 1: What is the purpose of the throws keyword in Java?**
- A) To handle an exception within a method using a try-catch block.
  - `Incorrect: The throws keyword does not handle exceptions; it declares that a method might throw exceptions.`

- B) To declare that a method may throw a specific type of exception.
  - `Correct: The throws keyword is used in method signatures to declare that the method may throw the specified exceptions.`

- C) To indicate that an exception has occurred in a method.
  - `Incorrect: The throw keyword is used to indicate that an exception has occurred, not the throws keyword.`

**Question 2: What are the two ways to manage "Checked" exceptions in Java?**
- A) Handling with a try-catch block and using the throws specification.
  - `Correct: Checked exceptions in Java can be managed either by handling them with a try-catch block or by using the throws specification in the method declaration.`

- B) Handling with a try-finally block and using the throws specification.
  - `Incorrect: While a try-finally block can ensure a block of code is always executed, it does not handle exceptions.`

- C) Handling with a catch block and using the throws specification.
  - `Incorrect: A catch block is part of a try-catch structure for handling exceptions, but it does not stand alone.`

- D) Handling with a try-catch-finally block and using the throws specification.
  - `Correct: Checked exceptions in Java can be managed either by handling them with a try-catch-finally block or by using the throws specification in the method declaration.`
  
  **Step 8: The Java Exception Hierarchy**

**Question 1: Which exception class is at the root of the Java exception hierarchy?**
- A) Error
  - `Incorrect: While Error is a subclass of Throwable, it is not the root of the Java exception hierarchy.`

- B) Exception
  - `Incorrect: While Exception is a subclass of Throwable, it is not the root of the Java exception hierarchy.`

- C) InterruptedException
  - `Incorrect: InterruptedException is a subclass of Exception, and it is not the root of the Java exception hierarchy.`

- D) RuntimeException
  - `Incorrect: RuntimeException is a subclass of Exception, and it is not the root of the Java exception hierarchy.`

The correct answer is `Throwable`. This is the superclass of all errors and exceptions in the Java language.

**Question 2: Which category of exceptions are unchecked exceptions?**
- A) RuntimeException and its sub-classes
  - `Correct: RuntimeException and its subclasses are unchecked exceptions in Java.`

- B) All sub-classes of Exception excluding RuntimeException
  - `Incorrect: This category includes checked exceptions, not unchecked exceptions.`

- C) InterruptedException and its sub-classes
  - `Incorrect: InterruptedException is a checked exception, not an unchecked exception.`

- D) All sub-classes of Error
  - `Correct: All subclasses of Error are also considered unchecked exceptions.`

**Question 3: Which category of exceptions are checked exceptions?**
- A) RuntimeException and its sub-classes
  - `Incorrect: RuntimeException and its subclasses are unchecked exceptions, not checked exceptions.`

- B) All sub-classes of Exception excluding RuntimeException
  - `Correct: All subclasses of Exception excluding RuntimeException are checked exceptions.`

- C) InterruptedException and its sub-classes
  - `Correct: InterruptedException is a checked exception.`

- D) All sub-classes of Error
  - `Incorrect: All subclasses of Error are unchecked exceptions, not checked exceptions.`

**Step 9: Throwing an Exception**

**Question 1: What is the purpose of throwing an exception in Java?**
- A) To handle an exceptional condition in the code.
  - `Incorrect: Throwing an exception is a way of indicating an exceptional condition, not handling it.`

- B) To indicate that a method cannot be executed due to an exceptional condition.
  - `Correct: Exceptions are thrown to indicate that a method cannot continue execution due to an exceptional condition.`

- C) To terminate the program abruptly.
  - `Incorrect: While an unhandled exception can cause a program to terminate abruptly, the primary purpose of throwing an exception is to indicate an exceptional condition.`

- D) To provide debugging information to the programmer.
  - `Correct: When an exception is thrown, it can carry information about the error, which can aid in debugging.`

**Question 2: Which keyword is used to throw an exception in Java?**
- A) catch
  - `Incorrect: The catch keyword is used to handle exceptions, not to throw them.`

- B) throw
  - `Correct: The throw keyword is used to throw an exception.`

- C) try
  - `Incorrect: The try keyword is used to enclose a block of code in which an exception might occur.`

- D) finally
  - `Incorrect: The finally keyword is used to enclose a block of code that must be executed regardless of whether an exception occurs.`

**Question 3: When should a checked exception be declared in a method signature?**
- A) When the method handles the checked exception using a try-catch block.
  - `Incorrect: If the method handles the checked exception

, it doesn't need to declare it.`

- B) When the method may throw the checked exception during execution.
  - `Correct: If a method might throw a checked exception, it should declare that in its method signature.`

- C) When the method does not handle the checked exception.
  - `Correct: If a method does not handle a checked exception, it must declare it in its method signature.`

- D) When the method is a sub-class of RuntimeException.
  - `Incorrect: The RuntimeException and its subclasses are unchecked exceptions, so they do not need to be declared in a method signature.`
  
  
  **Step 10: Throwing A Custom Exception**

**Question 1: What is the benefit of throwing a custom exception in Java?**
- A) It allows you to handle exceptional conditions specific to your code.
  - `Correct: Custom exceptions can be used to handle specific conditions that aren't covered by the standard Java exceptions.`

- B) It provides a way to terminate the program abruptly.
  - `Incorrect: The primary purpose of throwing a custom exception isn't to terminate the program abruptly, but to signal specific exceptional conditions in your code.`

- C) It simplifies the exception handling process.
  - `Correct: Custom exceptions can help simplify exception handling by providing more specific exceptions that are easier to handle in a meaningful way.`

- D) It improves the performance of the code.
  - `Incorrect: The creation of custom exceptions doesn't generally improve the performance of the code.`

**Question 2: Which type of exception will a custom exception become if it inherits from a checked exception class?**
- A) Checked exception
  - `Correct: If a custom exception inherits from a checked exception, it will be a checked exception.`

- B) Unchecked exception
  - `Incorrect: Inheriting from a checked exception will not make the custom exception unchecked.`

- C) RuntimeException
  - `Incorrect: RuntimeException is a type of unchecked exception.`

- D) Error
  - `Incorrect: Error is not a type of exception.`

**Question 3: Which type of exception will a custom exception become if it inherits from an unchecked exception class?**
- A) Checked exception
  - `Incorrect: If a custom exception inherits from an unchecked exception, it will be an unchecked exception.`

- B) Unchecked exception
  - `Correct: If a custom exception inherits from an unchecked exception, it will be an unchecked exception.`

- C) RuntimeException
  - `Correct: If a custom exception inherits from RuntimeException, it will be an unchecked exception as RuntimeException is a type of unchecked exception.`

- D) Error
  - `Incorrect: Error is not a type of exception.`

**Step 11: Introducing try-With-Resources**

**Question 1: What is the purpose of the try-with-resources statement in Java?**
- A) To handle exceptions in a try-catch-finally block.
  - `Incorrect: While try-with-resources can be used with a try-catch-finally block, its primary purpose is to automatically manage resources.`

- B) To automatically manage resources that implement the AutoCloseable interface.
  - `Correct: The primary purpose of try-with-resources is to automatically close resources that implement the AutoCloseable interface.`

- C) To terminate the program abruptly.
  - `Incorrect: The purpose of try-with-resources is not to terminate the program abruptly.`

- D) To provide debugging information to the programmer.
  - `Incorrect: The purpose of try-with-resources is not to provide debugging information, but to automatically manage resources.`

**Question 2: Which interface must a resource implement to be compatible with try-with-resources?**
- A) Closeable
  - `Correct: Resources that implement the Closeable interface, which extends AutoCloseable, can be used with try-with-resources.`

- B) AutoCloseable
  - `Correct: Resources that implement the AutoCloseable interface can be used with try-with-resources.`

- C) Resource
  - `Incorrect: There is no Resource interface in Java.`

- D) Disposable
  - `Incorrect: There is no Disposable interface in Java.`

**Question 3: What is the benefit of using try-with-resources over manually closing the resource?**
- A

) It simplifies the exception handling process.
  - `Correct: Using try-with-resources can simplify exception handling by automatically closing resources, thus avoiding potential resource leaks.`

- B) It ensures that the resource is always closed, even in case of exceptions.
  - `Correct: The try-with-resources statement ensures that each resource is closed at the end of the statement, even if an exception is thrown.`

- C) It improves the performance of the code.
  - `Incorrect: Using try-with-resources doesn't directly improve the performance of the code.`

- D) It allows the resource to be reused in multiple try-catch blocks.
  - `Incorrect: The primary benefit of try-with-resources is automatic resource management, not reusability in multiple try-catch blocks.`
  
  
**Step 12: Programming Puzzle Set PP_02**

**Puzzle-01: Does the following program handle the exception thrown?**
```java
try {
    AmountAdder.addAmounts(new Amount("RUPEE", 5), new Amount("RUPEE", 5));
    String str = null;
    str.toString();
} catch (CurrenciesDoNotMatchException ex) {
    ex.printStackTrace();
}
```
- A) Yes
  - `Incorrect: This program can handle `CurrenciesDoNotMatchException` but it doesn't handle `NullPointerException` which will be thrown when attempting to invoke `toString()` on a null string.`

- B) No
  - `Correct: Although `CurrenciesDoNotMatchException` is handled, the code will throw a `NullPointerException` when `str.toString();` is executed, and that exception isn't handled.`

**Puzzle-02: Does the following code compile?**
```java
try {
    AmountAdder.addAmounts(new Amount("RUPEE", 5), new Amount("RUPEE", 5));
    String str = null;
    str.toString();
} catch (Exception e) {
    e.printStackTrace();
} catch (CurrenciesDoNotMatchException ex) {
    ex.printStackTrace();
}
```
- A) Yes
  - `Incorrect: This code will not compile because the catch block for the superclass Exception is before the catch block for the subclass CurrenciesDoNotMatchException. In Java, catch blocks for more specific exception types must come before those for more general types.`

- B) No
  - `Correct: The code doesn't compile because the catch blocks are in the wrong order. The catch block for Exception (which is a superclass of all exceptions) should come after all other more specific exception catch blocks.`

**Puzzle-03: Does the following code compile?**
```java
try {

} catch (IOException | SQLException ex) {
    ex.printStackTrace();
}
```
- A) Yes
  - `Correct: The code does compile. Since Java 7, you can catch multiple exception types in a single catch block using this syntax.`

- B) No
  - `Incorrect: The code does compile. The `IOException` and `SQLException` are being caught in a single catch block, which is a valid syntax in Java.`
  
  
