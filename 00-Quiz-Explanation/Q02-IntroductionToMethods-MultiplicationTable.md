### Question 1

  

What does the `void` keyword indicate in a method definition?

  

* A) The method returns an integer value. `Incorrect: void` means no return type, not integer.

* B) The method does not return any value. `Correct: void` means the method does not return any value.

* C) The method returns a boolean value. `Incorrect: void` means no return type, not boolean【5†source】.

  

### Question 2

  

What is the correct way to call a method named `sayHelloWorldTwice`?

  

* A) sayHelloWorldTwice. `Incorrect: Method calls in Java require parentheses, even if no arguments are being passed`.

* B) sayHelloWorldTwice(). `Correct: This is the correct syntax to call a method in Java`.

* C) sayHelloWorldTwice(); `Incorrect: While this is valid in a statement context, it's not the correct way to just refer to a method call`【6†source】.

  

### Question 3

  

Which of the following statements is true about method definitions and method calls?

  

* A) Defining a method automatically executes its statement body. `Incorrect: Defining a method does not execute its body`.

* B) Defining a method and invoking it are the same thing. `Incorrect: Defining a method is different from invoking it`.

* C) Defining and invoking methods are two different steps. `Correct: In Java, a method must first be defined and then invoked for the code in the method to execute`【7†source】.

  

### Question 4

  

What is the correct syntax for defining a method that prints "Hello World"?

  

* A) void printHelloWorld() { System.out.println("Hello World"); }. `Correct: This is the correct syntax for defining a method in Java`.

* B) printHelloWorld() { System.out.println("Hello World"); }. `Incorrect: Java methods require a return type, in this case, 'void' is missing`.

* C) void printHelloWorld { System.out.println("Hello World"); }. `Incorrect: Parentheses are required after the method name to indicate it's a method`【8†source】.

  

### Question 5

  

Which of these method names follows the same naming rules as variable names?

  

* A) 1stMethod. `Incorrect: Variable names cannot start with a number`.

* B) method_one. `Correct: This follows the Java naming rules, can contain alphanumeric characters and underscores, and cannot start with a number`.

* C) first-Method. `Incorrect: Hyphens are not allowed in Java method names`【9†source】.

  

### Question 6

  

Which command lists the methods defined in the current JShell session?

  

* A) /methods. `Correct: This command lists the methods defined in the current JShell session`.

* B) /list. `Incorrect: This command lists the statements entered during the current JShell session`.

* C) /edit. `Incorrect: This command opens a method definition in a separate editor window`【10†source】.

  

### Question 7

  

What does the /edit command do in JShell?

  

* A) Lists the code of the specified method. `Incorrect: This is not the function of the /edit command`.

* B) Allows you to modify the method definition in a separate editor window. `Correct: The /edit command opens the definition of a method in a separate editor window for modification`.

* C) Saves the session method definitions to a file. ``Incorrect: This is the functionality of the /save command, not /edit`【11†source】.

  

### Question 8

  

What is the correct syntax for defining a method with an argument?

  

* A) void methodName(ArgType argName) { method-body }. `Correct: This is the correct syntax to define a method with arguments in Java`.

* B) methodName(ArgType argName) { method-body }. `Incorrect: Java methods require a return type`.

* C) methodName(ArgType argName) { method-body; }. `Incorrect: The semicolon at the end is not necessary and the return type is missing`【12†source】.

  

### Question 9

  

Which method definition correctly prints all integers from 1 to n (inclusive), where n is an argument?

  

* A)

  

void printNumbers(int n) {

for (int i = 1; i <= n; i++) {

System.out.println(i);

}

}

`Correct: This method correctly prints all integers from 1 to n`【13†source】.

  

### Question 10

  

What would happen if you try to call the method `sayHelloWorld` with a string argument, when the method is defined to accept an integer argument?

  

* A) The program will compile and run without any errors. `Incorrect: The method call will fail to compile due to incompatible types`.

* B) The program will throw a runtime error. `Incorrect: The error will occur at compile time, not runtime`.

* C) The program will fail to compile due to incompatible types. `Correct: Java is statically-typed, meaning the type of each variable and expression is checked at compile time`【14†source】.

  


``### Question 11

What is method overloading in Java?

 * A) The ability to have multiple methods with the same name in a class, but with different types of arguments. `Correct: Method overloading allows multiple methods with the same name but different parameter lists in a class`.
 * B) The ability to have multiple methods with the same name and the same types of arguments in a class. `Incorrect: Methods with the same name and argument types are considered duplicates and will result in a compilation error`.
 * C) The ability to have a single method with an arbitrary number of arguments. `Incorrect: This describes varargs, not method overloading`【16†source】.

### Question 12

Consider the following two method definitions:

```java
void printName(String firstName, String lastName) {
  System.out.println(firstName + " " + lastName);
}

void printName(String firstName, String middleName, String lastName) {
  System.out.println(firstName + " " + middleName + " " + lastName);
}
```

Which of the following statements are true?

-   A) The two methods are overloaded methods. `Correct: These methods have the same name but different parameters, which is a feature of method overloading`.
-   B) The two methods have the same name and different number of arguments. `Correct: These methods indeed have the same name but different number of arguments`.
-   C) The two methods have the same name and the same types of arguments. `Incorrect: While they have the same types of arguments, the number of arguments is different, so this statement is false`【17†source】.

### Question 13

What will the following code snippet output?

```
void sum(int a, int b) {
  System.out.println(a + b);
}

void sum(int a, int b, int c) {
  System.out.println(a + b + c);
}

sum(1, 2);
sum(1, 2, 3);
```

-   A) The output will be 3 6. `Correct: The first call to sum uses the two-parameter version, while the second call uses the three-parameter version`.
-   B) The output will be 3 5. `Incorrect: The second call to sum(1,2,3) would yield 6, not 5`.
-   C) The code will not compile due to method overloading. `Incorrect: Method overloading is a valid concept in Java, and this code would compile and run correctly`【18†source】.

### Question 14

Which of the following statements is true about methods with multiple arguments in Java?

-   A) A method can only accept up to 2 arguments. `Incorrect: A method in Java can accept any number of arguments`.
-   B) A method can accept any number of arguments, but they must be of the same type. `Incorrect: A method can accept arguments of different types`.
-   C) A method can accept any number of arguments, and they can be of different types. `Correct: In Java, a method can accept any number of arguments, and these arguments can be of different types`【19†source】.

### Question 15

What is the main purpose of method overloading in Java?

-   A) To reduce code duplication by allowing methods with the same name but different arguments. `Correct: One of the benefits of method overloading is that it allows the same method name to be used with different parameters`.
-   B) To allow a method to return different types of values based on the input arguments. `Incorrect: Method overloading does not affect the return type of a method`.
-   C) To create multiple methods with the same name and the same number of arguments, but with different implementation. `Incorrect: The methods would need to have different parameter lists to be considered overloaded`【20†source】.

### Question 16

What is the purpose of a return statement in a method?

-   A) To end the execution of the method. `Incorrect: While a return statement does end the execution of a method, its main purpose is to return the result of a computation to the calling code`.
-   B) To return the result of a computation to the calling code. `Correct: The primary purpose of the return statement in a method is to return the result of a computation to the calling code`.
-   C) To print the output of the method. `Incorrect: Printing the output is the job of the System.out.println() method, not the return statement`【21†source】.

### Question 17

What is the benefit of using a return mechanism in a method?

-   A) It allows the method to print the result of the computation. `Incorrect: Printing is not the job of the return statement, rather it returns the result to the calling code`.
-   B) It enables sharing computed results with other code and methods, and improves breaking down a problem into sub-problems. `Correct: The return mechanism enables the reuse of computed results in other parts of the code`.
-   C) It simplifies the syntax of the method. `Incorrect: While the use of return can make a method more readable, it does not necessarily simplify the syntax`【22†source】.