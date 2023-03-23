## Java Multiple Choice Quiz & Code Challenge

### Step 01: First Challenge : The Print-Multiplication-Table (PMT-Challenge)


#### Exercise 1: PMT Challenge Using For Loop

Using JShell, write a program to display the multiplication table for 7, with entries from 1 to 10 using a for loop.

###### Solution

Launch JShell and enter the following commands:


```
for(int i = 1; i <= 10; i++) {
    System.out.println("7 * " + i + " = " + (7*i));
}
``` 

Output:


```
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
7 * 4 = 28
7 * 5 = 35
7 * 6 = 42
7 * 7 = 49
7 * 8 = 56
7 * 9 = 63
7 * 10 = 70
``` 

#### Exercise 2: PMT Challenge Using While Loop

Using JShell, write a program to display the multiplication table for 3, with entries from 1 to 5 using a while loop.

###### Solution

Launch JShell and enter the following commands:


```
int i = 1;
while(i <= 5) {
    System.out.println("3 * " + i + " = " + (3*i));
    i++;
}
```

Output:


```
3 * 1 = 3
3 * 2 = 6
3 * 3 = 9
3 * 4 = 12
3 * 5 = 15
```


### Step 02: Introducing JShell


#### Exercise 1:

Create a JShell snippet that defines a variable `myNumber` with a value of 10, then use an expression to calculate and display the square of `myNumber`.

##### Solution:

```

jshell> int myNumber = 10;
myNumber ==> 10
 jshell> myNumber * myNumber
$1 ==> 100
```

#### Exercise 2:

Create a JShell snippet that defines a method called `isEven` that takes an integer argument `n` and returns a boolean value indicating whether `n` is even or not. Then, call the method with an integer value of your choice and display the result.

##### Solution:

```

jshell> boolean isEven(int n) {
   ...>     return n % 2 == 0;
   ...> }
|  created method isEven(int)

jshell> isEven(7)
$1 ==> false

jshell> isEven(12)
$2 ==> true
```



### Step 03: Welcome to Problem Solving


#### Java Coding Exercise 1

Using JShell, write a Java code snippet to calculate and print the result of multiplying 7 by 4.

##### Solution

```

jshell> int result = 7 * 4;
result ==> 28

jshell> System.out.println(result);
28
```

#### Java Coding Exercise 2

Using JShell, write a Java code snippet to print the multiplication table for 9, with entries from 1 to 5.

#####  Solution

```

jshell> for (int i = 1; i <= 5; i++) {
   ...>     int result = 9 * i;
   ...>     System.out.println("9 * " + i + " = " + result);
   ...> }
9 * 1 = 9
9 * 2 = 18
9 * 3 = 27
9 * 4 = 36
9 * 5 = 45
```

Note: The above solution uses a for loop to execute the code 5 times, once for each table entry, and prints the result of each calculation.