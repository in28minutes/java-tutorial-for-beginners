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


### Step 08: Methods With Arguments, And Overloading

#### Exercise 1: Method Overloading

1.  Launch JShell
2.  Create a Java method called `printNumber` that takes an integer argument and prints it to the console.
3.  Overload the `printNumber` method with another method that takes a double argument and prints it to the console.
4.  Overload the `printNumber` method with another method that takes a string argument and prints it to the console.
5.  Call each of the `printNumber` methods with an appropriate argument.
6.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
2.  Create a Java method called `printNumber` that takes an integer argument and prints it to the console:

```
jshell> void printNumber(int num) {
   ...> System.out.println("The number is: " + num);
   ...> }
   ```

3.  Overload the `printNumber` method with another method that takes a double argument and prints it to the console:

```
jshell> void printNumber(double num) {
   ...> System.out.println("The number is: " + num);
   ...> }
   ```

4.  Overload the `printNumber` method with another method that takes a string argument and prints it to the console:

```
jshell> void printNumber(String str) {
   ...> System.out.println("The string is: " + str);
   ...> }
   ```

5.  Call each of the `printNumber` methods with an appropriate argument:

```
jshell> printNumber(10);
The number is: 10

jshell> printNumber(10.5);
The number is: 10.5

jshell> printNumber("Hello World");
The string is: Hello World
```

6.  Exit JShell using the `/exit` command:

```
jshell> /exit
|  Goodbye
```

#### Exercise: 2

1.  Launch JShell
2.  Define a method called `printHelloWorld()` that prints the message "Hello, World!" to the console.
3.  Define an overloaded method called `printHelloWorld(int number)` that prints the message "Hello, World!" to the console `number` times.
4.  Call the `printHelloWorld()` method.
5.  Call the `printHelloWorld(int number)` method with `number` equal to 3.
6.  Exit JShell using the `/exit` command.

##### Solution:

1.  Launch JShell
2.  Define a method called `printHelloWorld()` that prints the message "Hello, World!" to the console.

```
void printHelloWorld() {
    System.out.println("Hello, World!");
}
```

3.  Define an overloaded method called `printHelloWorld(int number)` that prints the message "Hello, World!" to the console `number` times.

```
void printHelloWorld(int number) {
    for (int i = 0; i < number; i++) {
        System.out.println("Hello, World!");
    }
}
```

4.  Call the `printHelloWorld()` method.

```
printHelloWorld();
```

Output:

```
Hello, World!
```

5.  Call the `printHelloWorld(int number)` method with `number` equal to 3.

```
printHelloWorld(3);
```

Output:

```
Hello, World!
Hello, World!
Hello, World!
```

6.  Exit JShell using the `/exit` command.

```
/exit
| Goodbye
```



### Step 09: Methods With Multiple Arguments

#### Exercise 1: Methods with Multiple Arguments in JShell

1.  Launch JShell.
2.  Define a method called `calculateSum` that takes in two `int` arguments and calculates and prints their sum.
3.  Define another method called `calculateAverage` that takes in three `double` arguments and calculates and prints their average.
4.  Call the `calculateSum` method with two `int` arguments.
5.  Call the `calculateAverage` method with three `double` arguments.
6.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
    
2.  Define a method called `calculateSum` that takes in two `int` arguments and calculates and prints their sum.
    

```
jshell> void calculateSum(int num1, int num2) {
   ...>     int sum = num1 + num2;
   ...>     System.out.println("The sum of " + num1 + " and " + num2 + " is " + sum);
   ...> }
   ```

3.  Define another method called `calculateAverage` that takes in three `double` arguments and calculates and prints their average.

```
jshell> void calculateAverage(double num1, double num2, double num3) {
   ...>     double avg = (num1 + num2 + num3) / 3.0;
   ...>     System.out.println("The average of " + num1 + ", " + num2 + ", and " + num3 + " is " + avg);
   ...> }
   ```

4.  Call the `calculateSum` method with two `int` arguments.

```
jshell> calculateSum(5, 7);
The sum of 5 and 7 is 12
```

5.  Call the `calculateAverage` method with three `double` arguments.

```
jshell> calculateAverage(3.5, 6.8, 9.1);
The average of 3.5, 6.8, and 9.1 is 6.466666666666666
```

6.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```


#### Exercise 2

Problem: Write a method called `printMessage` that takes a string message and an integer count as parameters, and prints the message count times to the console. Then, call the `printMessage` method with a string message of your choice and an integer count of your choice.

Solution:

```
1. Launch JShell
2. Define a method called `printMessage` that takes a string message and an integer count as parameters, and prints the message count times to the console:
   jshell> void printMessage(String message, int count) {
              for (int i = 1; i <= count; i++) {
                  System.out.println(message);
              }
          }
3. Call the `printMessage` method with a string message of your choice and an integer count of your choice:
   jshell> printMessage("Hello, world!", 3)
   Hello, world!
   Hello, world!
   Hello, world!
4. Exit JShell using the `/exit` command.
```

Note: In this example, the `printMessage` method takes two parameters - a string message and an integer count. Inside the method, we use a for loop to print the message count times to the console. Finally, we call the `printMessage` method with the string message "Hello, world!" and the integer count 3.



### Step 10: Returning From A Method

#### Exercise 1

Write a method called `calculateSum` that takes two integer parameters and returns their sum. Then, call the `calculateSum` method with two integer arguments of your choice and print the result to the console.

Solution:

1.  Launch JShell.
2.  Define a method called `calculateSum` that takes two integer parameters and returns their sum:
    
```
jshell> int calculateSum(int a, int b) {
               return a + b;
           }
```
    
3.  Call the `calculateSum` method with two integer arguments of your choice and print the result to the console:
    
```
jshell> int result = calculateSum(5, 7);
           System.out.println(result); 
```
    Output: `12`
4.  Exit JShell using the `/exit` command.

Note: In this example, we define a method called `calculateSum` that takes two integer parameters `a` and `b`. Inside the method, we return the sum of `a` and `b`. Finally, we call the `calculateSum` method with two integer arguments `5` and `7` and store the result in a variable named `result`. Then we print the `result` variable to the console using the `System.out.println()` method.



#### Exercise 2

Write a method called `sumNumbers` that takes an integer `n` as a parameter and returns the sum of the first `n` natural numbers.

Solution:

1.  Launch JShell.
2.  Define a method called `sumNumbers` that takes an integer `n` as a parameter and returns the sum of the first `n` natural numbers:
    
```
jshell> int sumNumbers(int n) {
               int sum = 0;
               for (int i = 1; i <= n; i++) {
                   sum += i;
               }
               return sum;
           }
```
    
3.  Call the `sumNumbers` method with an integer `n` of your choice:
    
```
jshell> sumNumbers(10)
    $1 ==> 55
```
    
4.  Exit JShell using the `/exit` command.

Note: In this example, the `sumNumbers` method takes an integer `n` as a parameter and returns the sum of the first `n` natural numbers using a for loop. We call the `sumNumbers` method with an integer `n` of 10 and it returns the sum of the first 10 natural numbers, which is 55.