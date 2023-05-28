## Step 1: Introducing Exceptions

**Question 1:** What is an exception in Java?

- A) An error that occurs during the execution of a program.
- B) A condition that indicates the successful completion of a program.
- C) A statement that is used to handle errors in a program.

**Question 2:** Which of the following is an example of an exception?

- A) A program running out of memory.
- B) A division by zero error.
- C) Both A and B.

**Question 3:** What happens if an exception is not handled in a program?

- A) The program continues running normally.
- B) The program terminates abruptly and an error message is displayed.
- C) The program enters a loop until the exception is resolved.

## Step 2: Handling An Exception

**Question 1:** How can you handle an exception in Java?

- A) By using the `try-catch` block.
- B) By using the `if-else` statement.
- C) By using the `throw` keyword.

**Question 2:** What is the purpose of the `catch` block in a `try-catch` block?

- A) To define the code that may throw an exception.
- B) To handle the exception and provide an alternative code path.
- C) To specify the type of exception to be caught.

**Question 3:** What happens if an exception is caught in a `catch` block?

- A) The program continues running normally after the `catch` block.
- B) The program terminates abruptly and an error message is displayed.
- C) The program enters a loop until the exception is resolved.



## Step 3: The Exception Hierarchy

**Question 1:** What is the root class of the Java exception hierarchy?

- A) `RuntimeException`
- B) `Exception`
- C) `Throwable`

**Question 2:** Which of the following is true about the exception hierarchy in Java?

- A) All exceptions in Java are subclasses of `Exception`.
- B) `NullPointerException` is a subclass of `RuntimeException`.
- C) Both A and B.

**Question 3:** Why is it important to understand the exception hierarchy in Java?

- A) It helps in determining the type of exception to catch.
- B) It provides a way to handle different types of exceptions in a program.
- C) Both A and B.

## Step 4: The Need For `finally`

**Question 1:** What happens if a resource is not properly released in a program?

- A) The program continues running normally.
- B) The program terminates abruptly and an error message is displayed.
- C) The resource remains in use and may cause issues in the program.

**Question 2:** How can you ensure that a resource is always released, even if an exception occurs?

- A) By using the `try-catch` block.
- B) By using the `finally` block.
- C) By using the `throw` keyword.

**Question 3:** When is the code inside the `finally` block executed?

- A) Only when an exception occurs.
- B) Only when there is no exception.
- C) Whether an exception occurs or not.


## Step 5: Programming Puzzles - PP-01

**Puzzle-01:** Would the `finally` clause be executed if the statement `//str = "Hello";` remains as-is?

- A) Yes
- B) No

**Puzzle-02:** When will code in a `finally` clause not get executed?

- A) When an exception occurs in the `try` block.
- B) When an exception occurs in the `catch` block.
- C) When an exception occurs in preceding statements within the same `finally` clause.
- D) When there is a JVM crash.

**Puzzle-03:** Will the following code, a `try-finally` without a `catch`, compile?

- A) Yes
- B) No

**Puzzle-04:** Will the following code, a `try` without a `catch` or a `finally`, compile?

- A) Yes
- B) No

## Step 6: Handling Exceptions: Do We Have A Choice?

**Question 1:** What is the purpose of the `throws` keyword in Java?

- A) To handle an exception within a method using a `try-catch` block.
- B) To declare that a method may throw a specific type of exception.
- C) To indicate that an exception has occurred in a method.

**Question 2:** What are the two ways to manage "Checked" exceptions in Java?

- A) Handling with a `try-catch` block and using the `throws` specification.
- B) Handling with a `try-finally` block and using the `throws` specification.
- C) Handling with a `catch` block and using the `throws` specification.
- D) Handling with a `try-catch-finally` block and using the `throws` specification.

## Step 8: The Java Exception Hierarchy

**Question 1:** Which exception class is at the root of the Java exception hierarchy?

- A) `Error`
- B) `Exception`
- C) `InterruptedException`
- D) `RuntimeException`

**Question 2:** Which category of exceptions are unchecked exceptions?

- A) `RuntimeException` and its sub-classes
- B) All sub-classes of `Exception` excluding `RuntimeException`
- C) `InterruptedException` and its sub-classes
- D) All sub-classes of `Error`

**Question 3:** Which category of exceptions are checked exceptions?

- A) `RuntimeException` and its sub-classes
- B) All sub-classes of `Exception` excluding `RuntimeException`
- C) `InterruptedException` and its sub-classes
- D) All sub-classes of `Error`

## Step 9: Throwing an Exception

**Question 1:** What is the purpose of throwing an exception in Java?

- A) To handle an exceptional condition in the code.
- B) To indicate that a method cannot be executed due to an exceptional condition.
- C) To terminate the program abruptly.
- D) To provide debugging information to the programmer.

**Question 2:** Which keyword is used to throw an exception in Java?

- A) `catch`
- B) `throw`
- C) `try`
- D) `finally`

**Question 3:** When should a checked exception be declared in a method signature?

- A) When the method handles the checked exception using a `try-catch` block.
- B) When the method may throw the checked exception during execution.
- C) When the method does not handle the checked exception.
- D) When the method is a sub-class of `RuntimeException`.

## Step 10: Throwing A Custom Exception

**Question 1:** What is the benefit of throwing a custom exception in Java?

- A) It allows you to handle exceptional conditions specific to your code.
- B) It provides a way to terminate the program abruptly.
- C) It simplifies the exception handling process.
- D) It improves the performance of the code.

**Question 2:** Which type of exception will a custom exception become if it inherits from a checked exception class?

- A) Checked exception
- B) Unchecked exception
- C) RuntimeException
- D) Error

**Question 3:** Which type of exception will a custom exception become if it inherits from an unchecked exception class?

- A) Checked exception
- B) Unchecked exception
- C) RuntimeException
- D) Error

## Step 11: Introducing try-With-Resources

**Question 1:** What is the purpose of the try-with-resources statement in Java?

- A) To handle exceptions in a try-catch-finally block.
- B) To automatically manage resources that implement the `AutoCloseable` interface.
- C) To terminate the program abruptly.
- D) To provide debugging information to the programmer.

**Question 2:** Which interface must a resource implement to be compatible with try-with-resources?

- A) `Closeable`
- B) `AutoCloseable`
- C) `Resource`
- D) `Disposable`

**Question 3:** What is the benefit of using try-with-resources over manually closing the resource?

- A) It simplifies the exception handling process.
- B) It ensures that the resource is always closed, even in case of exceptions.
- C) It improves the performance of the code.
- D) It allows the resource to be reused in multiple try-catch blocks.

## Step 12: Programming Puzzle Set PP_02

**Puzzle-01:**
Does the following program handle the exception thrown?

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
- B) No

**Puzzle-02:**
Does the following code compile?

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
- B) No

**Puzzle-03:**
Does the following code compile?

```java
try {

} catch (IOException | SQLException ex) {
    ex.printStackTrace();
}
```

- A) Yes
- B) No
