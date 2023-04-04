## Step 1,2

### Question 1

What does the `void` keyword indicate in a method definition?

- A) The method returns an integer value 
- B) The method does not return any value 
- C) The method returns a boolean value

**Answer:** B) The method does not return any value

### Question 2

What is the correct way to call a method named `sayHelloWorldTwice`?

- A) sayHelloWorldTwice 
- B) sayHelloWorldTwice() 
- C) sayHelloWorldTwice();

**Answer:** B) sayHelloWorldTwice()

### Question 3

Which of the following statements is true about method definitions and method calls?

- A) Defining a method automatically executes its statement body 
- B) Defining a method and invoking it are the same thing 
- C) Defining and invoking methods are two different steps

**Answer:** C) Defining and invoking methods are two different steps


### Question 4

What is the correct syntax for defining a method that prints "Hello World"?

- A) void printHelloWorld() { System.out.println("Hello World"); } 
- B) printHelloWorld() { System.out.println("Hello World"); } 
- C) void printHelloWorld { System.out.println("Hello World"); }

**Answer:** A) void printHelloWorld() { System.out.println("Hello World"); }

### Question 5

Which of these method names follows the same naming rules as variable names?

- A) 1stMethod 
- B) method_one 
- C) first-Method

**Answer:** B) method_one

## Step 3

### Question 6

Which command lists the methods defined in the current JShell session?

- A) /methods 
- B) /list 
- C) /edit

**Answer:** A) /methods

### Question 7

What does the /edit command do in JShell?

- A) Lists the code of the specified method 
- B) Allows you to modify the method definition in a separate editor window 
- C) Saves the session method definitions to a file

**Answer:** B) Allows you to modify the method definition in a separate editor window


## Step 4, 5

### Question 8

What is the correct syntax for defining a method with an argument?

- A) void methodName(ArgType argName) { method-body } 
- B) methodName(ArgType argName) { method-body } 
- C) methodName(ArgType argName) { method-body; }

**Answer:** A) void methodName(ArgType argName) { method-body }

### Question 9

Which method definition correctly prints all integers from 1 to n (inclusive), where n is an argument?

- A)

```
void printNumbers(int n) {
  for (int i = 1; i <= n; i++) {
    System.out.println(i);
  }
}
```

- B)

```
void printNumbers(int n) {
  for (int i = 1; i < n; i++) {
    System.out.println(i);
  }
}
```
- C)

```
void printNumbers(int n) {
  for (int i = 0; i < n; i++) {
    System.out.println(i);
  }
}
```

**Answer:** A)

```
void printNumbers(int n) {
  for (int i = 1; i <= n; i++) {
    System.out.println(i);
  }
}
```

### Question 10

What would happen if you try to call the method `sayHelloWorld` with a string argument, when the method is defined to accept an integer argument?

- A) The program will compile and run without any errors 
- B) The program will throw a runtime error 
- C) The program will fail to compile due to incompatible types

**Answer:** C) The program will fail to compile due to incompatible types

## Step 8, 9

### Question 11

What is method overloading in Java?

- A) The ability to have multiple methods with the same name in a class, but with different types of arguments 
- B) The ability to have multiple methods with the same name and the same types of arguments in a class 
- C) The ability to have a single method with an arbitrary number of arguments

**Answer:** A) The ability to have multiple methods with the same name in a class, but with different types of arguments

### Question 12

Consider the following two method definitions:

```
void printName(String firstName, String lastName) {
  System.out.println(firstName + " " + lastName);
}

void printName(String firstName, String middleName, String lastName) {
  System.out.println(firstName + " " + middleName + " " + lastName);
}
```

Which of the following statements are true?

- A) The two methods are overloaded methods 
- B) The two methods have the same name and different number of arguments 
- C) The two methods have the same name and the same types of arguments

**Answer:** A) The two methods are overloaded methods and B) The two methods have the same name and different number of arguments

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

- A) The output will be

```
3
6
```

- B) The output will be

```
3
5
```

- C) The code will not compile due to method overloading

**Answer:** A) The output will be

```
3
6
```

### Question 14

Which of the following statements is true about methods with multiple arguments in Java?

- A) A method can only accept up to 2 arguments 
- B) A method can accept any number of arguments, but they must be of the same type 
- C) A method can accept any number of arguments, and they can be of different types

**Answer:** C) A method can accept any number of arguments, and they can be of different types

### Question 15

What is the main purpose of method overloading in Java?

- A) To reduce code duplication by allowing methods with the same name but different arguments 
- B) To allow a method to return different types of values based on the input arguments 
- C) To create multiple methods with the same name and the same number of arguments, but with different implementation

**Answer:** A) To reduce code duplication by allowing methods with the same name but different arguments


## Step 10

**Question 16 :** What is the purpose of a return statement in a method?

- A. To end the execution of the method 
- B. To return the result of a computation to the calling code 
- C. To print the output of the method

_Answer: B_

**Question 17 :** What is the benefit of using a return mechanism in a method?

- A. It allows the method to print the result of the computation 
- B. It enables sharing computed results with other code and methods, and improves breaking down a problem into sub-problems 
- C. It simplifies the syntax of the method

_Answer: B_