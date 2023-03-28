### Step 01 : Defining A Simple Method 
### Step 02: Exercise-Set PE-01

### Exercise 1

1.  Launch JShell
2.  Define a method named `printHello` that prints the string "Hello" to the console.
3.  Call the `printHello` method.
4.  Exit JShell using `/exit` command.

#### Solution 1

1. Launch JShell

2. Define a method named `printHello` that prints the string "Hello" to the console:

```
jshell> void printHello() {
   ...> System.out.println("Hello");
   ...> }
```

3. Call the `printHello` method:

```
jshell> printHello();
Hello
```

4. Exit JShell using `/exit` command:
```
jshell> /exit
```

### Exercise 2

1.  Launch JShell
2.  Define a method named `printNumbers` that prints the numbers 1 to 5 to the console, each on a new line.
3.  Call the `printNumbers` method.
4.  Exit JShell using `/exit` command.

### Solution 2

1. Launch JShell

2. Define a method named `printNumbers` that prints the numbers 1 to 5 to the console, each on a new line:

```
jshell> void printNumbers() {
   ...> for (int i = 1; i <= 5; i++) {
   ...> System.out.println(i);
   ...> }
   ...> }
   ```

3. Call the `printNumbers` method:
```
jshell> printNumbers();
1
2
3
4
5
```

4. Exit JShell using `/exit` command:
```
jshell> /exit
```



### Step 03: Editing A Method Definition (Jshell Tips)





#### Exercise 1: Editing a Method Definition in JShell

1.  Launch JShell.
2.  Define a method called `printMessage` that prints the message "Hello, World!" to the console.
3.  Call the `printMessage` method to verify that it works.
4.  Modify the `printMessage` method so that it prints a different message.
5.  Call the `printMessage` method again to verify that it now prints the new message.
6.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.

```
jshell>
```

2.  Define a method called `printMessage` that prints the message "Hello, World!" to the console.

```
jshell> void printMessage() {
   ...>   System.out.println("Hello, World!");
   ...> }
   ```

3.  Call the `printMessage` method to verify that it works.

```
jshell> printMessage();
Hello, World!
```

4.  Modify the `printMessage` method so that it prints a different message.

```
jshell> void printMessage() {
   ...>   System.out.println("Goodbye, World!");
   ...> }
   ```

5.  Call the `printMessage` method again to verify that it now prints the new message.

```
jshell> printMessage();
Goodbye, World!
```

6.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```




#### Exercise 2: Editing A Method Definition in JShell

1.  Launch JShell.
2.  Define a method called `greet` that prints the message "Welcome to JShell!" to the console.
3.  Call the `greet` method.
4.  Edit the `greet` method to print "Hello, JShell!" to the console instead.
5.  Call the `greet` method again to verify that it has been updated.
6.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
    
2.  Define a method called `greet` that prints the message "Welcome to JShell!" to the console.
    

```
jshell> void greet() {
   ...>     System.out.println("Welcome to JShell!");
   ...> }
   ```

3.  Call the `greet` method.

```
jshell> greet();
Welcome to JShell!
```

4.  Edit the `greet` method to print "Hello, JShell!" to the console instead.

```
jshell> /edit greet
```

This will open the method definition in an external editor. Replace the line that prints "Welcome to JShell!" with the following line:

```
System.out.println("Hello, JShell!");
```

Save the changes and close the editor.

5.  Call the `greet` method again to verify that it has been updated.

```
jshell> greet();
Hello, JShell!
```

6.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```



### Step 04: Methods with Arguments
### Step 05: Exercise Set PE-02 (With Solutions)



#### Exercise 1: Creating and Calling a Method with a Single Argument

1.  Launch JShell.
2.  Define a method called `printTwice` that takes in a `String` parameter and prints it twice to the console, with a space in between.
3.  Call the `printTwice` method with the argument `"Hello"`.
4.  Call the `printTwice` method with the argument `"Java"`.
5.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
    
2.  Define the `printTwice` method with a `String` parameter:
    
 ```
 jshell> void printTwice(String message) {
       ...> System.out.println(message + " " + message);
       ...> }
 ```
    
3.  Call the `printTwice` method with the argument `"Hello"`:
    
```
jshell> printTwice("Hello");
    Hello Hello
```
    
4.  Call the `printTwice` method with the argument `"Java"`:
    
  ```
  jshell> printTwice("Java");
    Java Java
```
    
5.  Exit JShell using the `/exit` command:
    
```
 jshell> /exit
    |  Goodbye
```
    

#### Exercise 2: Simple Method with an Integer Parameter

1.  Launch JShell.
2.  Define a method called `doubleNumber` that takes an `int` parameter called `num`. The method should print the result of doubling `num` to the console using `System.out.println()`.
3.  Call the `doubleNumber` method with the argument `5`.
4.  Call the `doubleNumber` method with the argument `-3`.
5.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
2.  Define a method called `doubleNumber` that takes an `int` parameter called `num`. The method should print the result of doubling `num` to the console using `System.out.println()`:

```
jshell> void doubleNumber(int num) {
   ...> System.out.println("Double of " + num + " is " + (num * 2));
   ...> }
   ```

3.  Call the `doubleNumber` method with the argument `5`:

```
jshell> doubleNumber(5);
Double of 5 is 10
```

4.  Call the `doubleNumber` method with the argument `-3`:

```
jshell> doubleNumber(-3);
Double of -3 is -6
```

5.  Exit JShell using the `/exit` command:

```
jshell> /exit
|  Goodbye
```


### Step 07:  _PMT-Challenge_  Revisited (And Some Puzzles)

#### Exercise 1: Printing a Multiplication Table with a Method in JShell

1.  Launch JShell.
2.  Define a method called `printMultiplicationTable` that takes an `int` parameter called `number`. The method should print the multiplication table of the given number up to 10. Each line of the table should be printed in the format `number * i = result`, where `i` is the number being multiplied by `number`, and `result` is the product of the multiplication.
3.  Call the `printMultiplicationTable` method with the argument `5`.
4.  Call the `printMultiplicationTable` method with the argument `9`.
5.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
2.  Define a method called `printMultiplicationTable` that takes an `int` parameter called `number`. The method should print the multiplication table of the given number up to 10. Each line of the table should be printed in the format `number * i = result`, where `i` is the number being multiplied by `number`, and `result` is the product of the multiplication.

```
jshell> void printMultiplicationTable(int number) {
   ...>     for (int i = 1; i <= 10; i++) {
   ...>         System.out.printf("%d * %d = %d\n", number, i, number * i);
   ...>     }
   ...> }
   ```

3.  Call the `printMultiplicationTable` method with the argument `5`.

```
jshell> printMultiplicationTable(5);
5 * 1 = 5
5 * 2 = 10
5 * 3 = 15
5 * 4 = 20
5 * 5 = 25
5 * 6 = 30
5 * 7 = 35
5 * 8 = 40
5 * 9 = 45
5 * 10 = 50
```

4.  Call the `printMultiplicationTable` method with the argument `9`.

```
jshell> printMultiplicationTable(9);
9 * 1 = 9
9 * 2 = 18
9 * 3 = 27
9 * 4 = 36
9 * 5 = 45
9 * 6 = 54
9 * 7 = 63
9 * 8 = 72
9 * 9 = 81
9 * 10 = 90
```

5.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```


#### Exercise 2: Printing Even Numbers using a Method with a Parameter

1.  Launch JShell.
2.  Define a method called `printEvenNumber` that takes an integer parameter.
3.  In the method, use a for loop to iterate from 1 to the parameter value.
4.  Within the loop, use an `if` statement to check if the current number is even.
5.  If the number is even, print it to the console using `System.out.println()`.
6.  Call the `printEvenNumber` method with the argument `10`.
7.  Call the `printEvenNumber` method again with the argument `20`.
8.  Exit JShell using the `/exit` command.

#### Solution

1.  Launch JShell.

```
$ jshell
|  Welcome to JShell -- Version 11.0.10
|  For an introduction type: /help intro
```

2.  Define a method called `printEvenNumber` that takes an integer parameter.

```
jshell> void printEvenNumber(int number) {
   ...> }
   ```

3.  In the method, use a for loop to iterate from 1 to the parameter value.

```
jshell> void printEvenNumber(int number) {
   ...>     for (int i = 1; i <= number; i++) {
   ...>     }
   ...> }
   ```

4.  Within the loop, use an `if` statement to check if the current number is even.

```
jshell> void printEvenNumber(int number) {
   ...>     for (int i = 1; i <= number; i++) {
   ...>         if (i % 2 == 0) {
   ...>         }
   ...>     }
   ...> }
   ```

5.  If the number is even, print it to the console using `System.out.println()`.

```
jshell> void printEvenNumber(int number) {
   ...>     for (int i = 1; i <= number; i++) {
   ...>         if (i % 2 == 0) {
   ...>             System.out.println(i);
   ...>         }
   ...>     }
   ...> }
   ```

6.  Call the `printEvenNumber` method with an integer parameter `10`.

```
jshell> printEvenNumber(10);
2
4
6
8
10
```

7.  Call the `printEvenNumber` method again with a different integer parameter `20`.

```
jshell> printEvenNumber(20);
2
4
6
8
10
12
14
16
18
20
```

8.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```


