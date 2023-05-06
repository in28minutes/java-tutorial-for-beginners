## Step 01: The if and if-else Conditionals:

1.  What is the if statement used for? 
- a) To execute some code when a boolean condition is true 
- b) To execute some code when a boolean condition is false 
- c) To execute some code regardless of the boolean condition

Answer: a)

2.  What is the difference between if and if-else statements?  
- a) There is no difference, they do the same thing 
- b) If statement executes code only when the condition is true, whereas if-else statement executes code when the condition is false 
- c) If statement executes code only when the condition is false, whereas if-else statement executes code when the condition is true

Answer: b)

3.  What is the output of the following code snippet?

```
int i = 10;
if(i < 5) {
    System.out.println("i is less than 5");
} else if(i > 20) {
    System.out.println("i is greater than 20");
} else {
    System.out.println("i is between 5 and 20");
}
```
a) i is less than 5 
b) i is greater than 20 
c) i is between 5 and 20

Answer: c)



## Step 02: The if-else if-else Conditional:

1.  What is the purpose of the if-else if-else statement? 
- a) To execute some code when a boolean condition is true 
- b) To execute some code when multiple conditions are true 
- c) To execute some code when one and only one condition is true

Answer: c)

2.  What happens if multiple conditions in the if-else if-else statement evaluate to true?  
- a) All corresponding code blocks are executed 
- b) Only the first corresponding code block is executed 
- c) Only the last corresponding code block is executed

Answer: b)

3.  What is the output of the following code snippet?

```
int i = 15;
if(i < 5) {
    System.out.println("i is less than 5");
} else if(i > 20) {
    System.out.println("i is greater than 20");
} else if(i < 10) {
    System.out.println("i is less than 10");
} else {
    System.out.println("i is between 10 and 20");
}
```

- a) i is less than 5 
- b) i is greater than 20 
- c) i is less than 10 
- d) i is between 10 and 20

Answer: d)


## Step 03: Puzzles on if:

1.  What is the output of the following code snippet?

```
public static void puzzleOne() {
    int k = 15;
    if(k > 20) {
        System.out.println(1);
    } else if(k > 10) {
        System.out.println(2);
    } else if(k < 20) {
        System.out.println(3);
    } else {
        System.out.println(4);
    }
}
```
a) 1 
b) 2 
c) 3 
d) 4

Answer: b)

2.  What is the output of the following code snippet?

```
public static void puzzleTwo() {
    int l = 15;
    if(l < 20)
    System.out.println("l < 20");
    if(l > 20)
    System.out.println("l > 20");
    else
    System.out.println("Who Am I?");
}
```

a) l < 20 
b) l > 20 
c) Who Am I?

Answer: c)

3.  What is the output of the following code snippet?

```
public static void puzzleThree() {
    int m = 15;
    if(m > 20)
    if(m < 20)
    System.out.println("m >  20");	else
    System.out.println("Who Am I?");
}
```

a) m > 20 
b) Who Am I? 
c) Nothing is printed.

Answer: c)

4.  What is the output of the following code snippet?

```
int i = 0;
if(i) {
    System.out.println("i");
}
```

a) i 
b) Compiler Error 
c) Nothing is printed.

Answer: b)

5.  What is the output of the following code snippet?

```
public static void puzzleFive() {
    int number = 5;
    if(number < 0)
    number = number + 10;
    number++;
    System.out.println(number);
}
```

a) 4 
b) 5 
c) 6

Answer: c)


## Step 04: Reading User Input

1.  What is the purpose of using the Scanner class in Java? 
- a) To scan user input from the console 
- b) To read input from a file 
- c) To generate random numbers

Answer: a

2.  What do you need to pass as a parameter to the Scanner constructor? 
3. - a) System.in 
4. b) System.out 
5. c) System.error

Answer: a

3.  How do you read an integer input from the console using the Scanner class? 
- a) scanner.nextInt() 
- b) scanner.readInt() 
- c) scanner.getInt()

Answer: a


## Step : 5

Here are three multiple choice questions based on the step:

1.  What is the purpose of the following code snippet?

```
Scanner scanner = new Scanner(System.in);
```

a) To initialize the Scanner class 
b) To import the Scanner class 
c) To create an instance of the Scanner class

Answer: c) To create an instance of the Scanner class

2.  What does the following line of code do?

```
int number1 = Scanner.nextInt();
```

a) Imports the next integer from the keyboard 
b) Initializes the value of `number1` to the next integer from the keyboard 
c) Creates an instance of the `nextInt` method

Answer: b) Initializes the value of `number1` to the next integer from the keyboard

3.  What does the following code snippet do?

```
System.out.println("Your Inputs Are:");
System.out.println("Number1: " + number1);
System.out.println("Number2: " + number2);
System.out.println("Choice: " + choice);
```

a) Imports the values of `number1`, `number2`, and `choice` from the keyboard 
b) Writes the values of `number1`, `number2`, and `choice` to the console 
c) Initializes the values of `number1`, `number2`, and `choice`

Answer: b) Writes the values of `number1`, `number2`, and `choice` to the console

# Step 06: Menu-Challenge - Reading Input, Computing Result, Displaying Output

## Quiz

1.  What is the purpose of the if-else-else if statement in the code? 
- a. To check for 4 favorable conditions 
- b. To handle invalid operation choice 
- c. To handle both favorable conditions and invalid operation choice 
- d. None of the above

Answer: c. To handle both favorable conditions and invalid operation choice

2.  What does the statement "System.out.println("Result = " + (number1 + number2));" do in the code? 
- a. Prints the sum of number1 and number2 
- b. Prints the difference of number1 and number2 
- c. Prints the product of number1 and number2 
- d. Prints the quotient of number1 and number2

Answer: a. Prints the sum of number1 and number2

3.  What is the output when choice is 5? 
- a. Result = 55 
- b. Invalid Operation 
- c. Number1: 25 
- d. Number2: 35

Answer: b. Invalid Operation

## Step 07: Introducing switch

### Quiz 1

Which of the following is NOT true about a switch statement in Java?

A) A switch statement is used to test multiple conditions

B) The default clause is executed when none of the cases match

C) The switch statement can handle the default possibility

D) The switch statement is used to test only one condition

Answer: D

### Quiz 2

What is the purpose of the break statement in a switch statement in Java?

A) To break out of the switch after a successful match

B) To continue to the next case in the switch

C) To stop the execution of the program

D) To continue to the default clause in the switch

Answer: A

### Quiz 3

What will the following code snippet output in Java?

```
int number = 2;
switch(number) {
	case 1:
		System.out.println(1);			
	case 2:
		System.out.println(2);
	case 3:
		System.out.println(3);
	default:
		System.out.println("default");
}
```

A) 1

B) 2

C) 3

D) 1, 2, 3, default

Answer: D


## Step 09: Comparing The if Family, And switch

### Quiz

1.  What type of conditions can be evaluated using an if-family conditional? 
- a. Only boolean conditions 
- b. Only integer values 
- c. Both boolean and integer values 
- d. None of the above
    
    Correct Answer: a. Only boolean conditions
    
2.  What is the advantage of using a switch conditional over an if-family conditional? 
- a. More readable and compact 
- b. Can be used to check for only integer values 
- c. More strict rules 
- d. More versatile
    
    Correct Answer: a. More readable and compact
    
3.  What is the disadvantage of using a switch conditional over an if-family conditional?  -
- a. Can lead to subtle errors in the program 
- b. More versatile 
- c. Can only check for boolean conditions 
- d. Not as strict as if-family conditional
    
    Correct Answer: a. Can lead to subtle errors in the program



## Step 10: Programming Exercise PE-03

### Question 1

What is the name of the day represented by the number `3` in the `determineNameOfDay` method?

A. Monday 
B. Tuesday 
C. Wednesday 
D. Thursday

Correct answer: C. Wednesday

### Question 2

What is the name of the month represented by the number `9` in the `determinenameofMonth` method?

A. January 
B. February 
C. March 
D. September

Correct answer: D. September

### Question 3

Is the day represented by the number `1` considered to be a week day in the `isWeekDay` method?

A. Yes 
B. No

Correct answer: A. Yes


## Step 12: Introducing ?:, The Ternary Operator

#### Question 1:

What is the purpose of the ternary operator ?: in Java?

A. To perform addition of two operands 
B. To perform subtraction of two operands 
**C. To perform conditional operations**

#### Question 2:

What should be the return type of both expressions in the ternary operator ?: in Java?

A. Both expressions can return any type of value 
B. Both expressions should return different types of value 
**C. Both expressions should return values of the same type**

#### Question 3:

What is the syntax of the ternary operator ?: in Java?

A. result = (expression-if-condition-true ? condition : expression:if-condition-false); 
B. result = (expression-if-condition-false ? condition : expression-if-condition-true); 
**C. result = (condition ? expression-if-condition-true : expression-if-condition-false);**