# Java Coding Exercises

## Section 7: Java Coding Exercises - Set 1

## Introduction To Java Coding Exercises

In this lecture, we explore the **Java Coding Exercises** feature offered by Udemy. This feature enables you to practice coding directly on the Udemy platform without the need for an IDE or setting up a development environment.

It is designed to make coding practice more accessible and user-friendly, especially for learners using laptops or desktop computers.

### Key Benefits of Udemy Coding Exercises

1. **No IDE Required**: You can code directly in your browser on the Udemy platform. This eliminates the need to set up complex development environments, making it easy to dive into practice.
   
2. **Automated Code Testing**: When you write code, Udemy automatically runs tests in the background to check the correctness of your code. You don't need to worry about writing your own test cases or setting up a main method to verify the solution.

3. **Guided Problem Solving**: 
   - Each coding exercise comes with clear instructions explaining the problem you need to solve.

   - There are **hints** to help guide you if you're stuck, and there are **solution explanations** if you need a more detailed breakdown of how to solve the exercise.

   - A **solution video** is also provided for many exercises, where you can watch the instructor solve the problem step by step.

4. **Practice-Oriented Learning**: The best way to learn programming is by solving problems and practicing continuously. The coding exercises help you do just that by providing immediate feedback on your solutions.

### How the Coding Interface Works

1. **Starting an Exercise**: When you begin a coding exercise, you will be presented with a coding interface that allows you to type your solution and run tests.
   
2. **Running Tests**: After typing your code, you can click the **"Run Tests"** button to run the tests provided for that exercise. The test results will show whether your solution passed or failed.
   
   - If a test fails, the interface provides detailed error messages. These messages help pinpoint issues, such as compilation errors or incorrect logic in your code.
   
3. **Compilation Errors**: If your code has syntax errors (e.g., missing return statements, parentheses), the platform will display the error details, including the exact line where the issue occurred.

4. **Hints and Solutions**: If you're struggling with an exercise:
   - You can click **"Hints"** after running the tests to get additional guidance.

   - If you're still stuck, the **"Solution Explanation"** becomes available, providing a detailed solution.

5. **Full-Screen Editor**: The interface allows you to expand the editor for a distraction-free coding experience by clicking **"Expand Editor"**.

6. **Error Handling**: The platform makes it easy to troubleshoot errors by showing clear and precise messages about any compilation issues or test failures.

### Step-by-Step Example

In one example exercise, you are asked to modify a method called `hello()` that currently returns `0`. The goal is to make the `hello()` method return `1` instead. Here’s how you solve it:

1. **Step 1**: Click **"Run Tests"** initially, and observe that the test fails because the method returns `0` instead of `1`.

2. **Step 2**: Modify the `hello()` method to return `1` instead of `0`, and click **"Run Tests"** again.

3. **Step 3**: Once the test passes, the exercise is complete.

### Advantages of Udemy Coding Exercises

- **Automated Solution Checking**: Your code is automatically checked by the provided tests. You don't need to manually run the program or print out results to verify correctness.
  
- **Practice Makes Perfect**: With over 40 coding exercises available, you’ll have ample opportunity to practice solving problems, which is essential for improving your programming skills.

- **Enhanced Documentation Skills**: Each coding exercise includes clear problem statements, allowing you to practice reading and interpreting requirements. This is a critical skill for working on real-world software projects.

- **Learn by Doing**: Coding exercises simulate real-world problem-solving scenarios, reinforcing your ability to code through hands-on practice.

### Best Practices for Using the Interface

1. **Take Your Time**: Coding exercises are meant to be a learning experience, so don’t rush through them. Carefully read the problem, try to solve it on your own, and use hints only when necessary.
   
2. **Avoid Copy-Pasting**: Write the code yourself to internalize the concepts. Avoid copying and pasting the solution directly, as typing out the solution helps reinforce your understanding.

3. **Review Solutions**: After solving an exercise, watch the accompanying **solution video** to see how the instructor approaches the problem. This can provide additional insights into better coding practices.

4. **Ask Questions**: If you encounter issues or need further clarification, use the **Q&A forum** to ask questions. Also, feel free to share your success stories or discuss any challenges you encountered.

---

## Solution Video For Coding Exercise: Print Hello World

In this exercise, you are tasked with creating a simple Java program that prints **Hello World** to the console. Let's walk through the solution step by step.

### Problem Description:
You need to write a Java program that outputs the message "Hello World" using the `System.out.println()` method in the main method.

### Step 1: Review the Initial Setup

- The initial code provided includes the **class declaration** and the **main method**.
- You need to add code inside the main method to print "Hello World."

```java
public class Exercise {
    public static void main(String[] args) {
        // Add code to print Hello World
    }
}
```

### Step 2: Add the Print Statement

To print the message "Hello World" in Java, you use `System.out.println()`. 

- The `System.out.println()` method prints a line of text to the console.
- It should be written inside the `main` method, and make sure to include the **semicolon (;)** at the end of the statement.

```java
public class Exercise {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

### Step 3: Running the Code

After writing the print statement, click **Run Tests** to check if the solution is correct. The test will check if "Hello World" is printed exactly as required.

If the code is correct, you'll see:

```
Passed 1 of 1 tests
```

### Common Mistakes

Here are a few common mistakes you might encounter:

1. **Missing Capital "S" in `System.out.println()`**:
   - If you accidentally use `system` with a lowercase "s", the program will not compile. Java is case-sensitive, and the correct syntax uses a capital "S" in `System`.

   Example of incorrect code:
   ```java
   system.out.println("Hello World");
   ```

   This will result in a compilation error:
   ```
   package system does not exist
   ```

2. **Missing Semicolon (`;`)**:
   - If you forget the semicolon at the end of the print statement, the compiler will throw an error. The semicolon is required to terminate the statement.

   Example of incorrect code:
   ```java
   System.out.println("Hello World")
   ```

   This will result in an error:
   ```
   semicolon expected
   ```

### Step 4: Correcting Errors

If you encounter any errors, the coding interface will display the line number and the error message, helping you identify and fix the issue. 

- **Error Message**: If you see an error message like `"package system does not exist"`, check if you have used a capital "S" in `System`.
- **Error Message**: `"semicolon expected"` means you need to add the missing semicolon at the end of the statement.

### Step 5: Final Test

Once you have corrected any mistakes, click **Run Tests** again. If everything is correct, the test will pass, and you'll have successfully completed the exercise.

This is a very simple exercise aimed at familiarizing you with the process of writing and running basic Java programs. Now that you have successfully completed it, you can move on to more challenging exercises.

---

## Solution Video For Coding Exercise: Time Converter

Let’s now walk through how I would solve the **Time Converter** coding exercise.

### Problem Description:
You’ve been given a partially implemented `TimeConverter` class. The goal is to complete two static methods:
1. **`convertHoursToMinutes(int hours)`**: This method takes an integer value representing hours and returns the equivalent value in minutes.
2. **`convertDaysToMinutes(int days)`**: This method takes an integer value representing days and returns the equivalent value in minutes.

Additionally, the problem specifies:
- For invalid cases (where days or hours are less than 0), the method should return **-1**.

### Step 1: Implement `convertHoursToMinutes`

Let’s start by focusing on the method that converts hours to minutes. The formula to convert hours to minutes is straightforward:
- **Minutes = Hours * 60**

However, before performing the calculation, we need to handle the invalid case where the input hours are negative.

Here’s the code:

```java
public static int convertHoursToMinutes(int hours) {
    if (hours < 0) {
        return -1; // Return -1 for invalid cases
    }
    return hours * 60; // Convert hours to minutes
}
```

### Step 2: Implement `convertDaysToMinutes`

Next, we’ll move on to the method that converts days to minutes. Since one day has 24 hours, and each hour has 60 minutes, we can multiply days by 24 and then by 60 to get the equivalent minutes. We also need to handle the case where the input days are negative.

Here’s the code:

```java
public static int convertDaysToMinutes(int days) {
    if (days < 0) {
        return -1; // Return -1 for invalid cases
    }
    return days * 24 * 60; // Convert days to minutes
}
```

### Step 3: Running the Tests

At this point, both methods are implemented, and we can now run the tests. Once you click **Run Tests**, you should see that all test cases pass successfully.

### Step 4: Optimization and Code Simplification

Now that the code is working, let’s look at how we can make it more concise without sacrificing readability.

In both methods, we calculate the result and return it immediately. Therefore, creating a local variable to store the result is unnecessary. Instead, we can return the result directly without storing it in a variable first.

Here’s the optimized code:

```java
public static int convertHoursToMinutes(int hours) {
    if (hours < 0) {
        return -1;
    }
    return hours * 60; // Directly return the calculated value
}

public static int convertDaysToMinutes(int days) {
    if (days < 0) {
        return -1;
    }
    return days * 24 * 60; // Directly return the calculated value
}
```

### Conclusion

With this optimized solution, both methods are concise and easy to read. The key takeaways from this exercise are:
- Handling invalid input conditions first to prevent unnecessary calculations.
- Simplifying the return logic by directly returning calculated values instead of using intermediate variables, which is more efficient when the calculation is straightforward.

Once you click **Run Tests** again, you should see that all test cases are still passing.

---

## Solution Video For Coding Exercise: Exam Result Checker

Let’s go through how I would solve the **Exam Result Checker** coding exercise.

### Problem Description:
You’ve been provided with a partially completed Java class named `ExamResult`, which has a method `isPass(int marks)`. The goal is to complete this method to determine if a student has passed or failed based on their marks.

#### Passing Criteria:
- A student is considered to have **passed** if their marks are **greater than 50**.
- A student is considered to have **failed** if their marks are **50 or less**.

### Step 1: Implementing the Logic

The problem is straightforward. We need to check if the provided marks are greater than 50, and return `true` for a pass, or `false` for a fail.

Here’s the initial implementation:

```java
public static boolean isPass(int marks) {
    if (marks > 50) {
        return true;  // Passed
    } else {
        return false; // Failed
    }
}
```

### Step 2: Running the Tests

Once you click **Run Tests**, you should see that all the test cases pass. These tests check various scenarios, such as:
- Marks below 50 (e.g., 49, 0).
- Marks exactly 50.
- Marks above 50 (e.g., 51, 100).
- Negative marks.

### Step 3: Optimization

The initial solution works fine, but it can be simplified further. Since the condition `marks > 50` already evaluates to a boolean (`true` or `false`), there’s no need for an `if-else` block.

We can directly return the result of the expression:

```java
public static boolean isPass(int marks) {
    return marks > 50;
}
```

This code is shorter, easier to read, and achieves the same functionality. The expression `marks > 50` will evaluate to `true` if the marks are greater than 50, and `false` otherwise.

### Step 4: Running Tests Again

Let’s click **Run Tests** again to verify the solution. All tests should pass successfully with this simplified version.

### Conclusion:

In this exercise, we learned how to:
- Use basic comparison operators to implement logic.
- Simplify code by returning boolean expressions directly.

---

## Solution Video For Coding Exercise: Sum of Squares of First N Numbers

Let’s walk through how I would solve the **Sum of Squares of First N Numbers** exercise.

### Problem Description:
You are given an integer `n`, and your task is to implement a method called `calculateSumOfSquares` in the class `SumOfSquares`. The method should calculate and return the sum of squares of all positive integers from 1 up to `n`. 

For example, if `n` is 3, the result should be:
\[ 1^2 + 2^2 + 3^2 = 14 \]

Additionally, if `n` is less than zero, the method should return `-1`.

### Step 1: Handling Invalid Input

The first step is to handle invalid input, where `n` is less than 0. In this case, we need to return `-1`.

```java
if (n < 0) {
    return -1;
}
```

### Step 2: Calculating the Sum of Squares

Now, if `n` is greater than or equal to zero, we need to compute the sum of squares. For this, we can loop from 1 to `n`, square each number, and add it to a sum variable.

We’ll declare a variable `sum` to store the total sum of squares. Since the sum can become large, I’ll use a `long` to avoid overflow.

Here's the code that implements this logic:

```java
long sum = 0;  // Initialize sum

for (int i = 1; i <= n; i++) {
    sum += i * i;  // Add the square of i to the sum
}

return sum;  // Return the total sum
```

### Step 3: Testing the Code

Let’s now run the tests to see if this works as expected. Once the code is implemented, run the test cases, and you should see that the results are successful.

### Debugging: Checking the Error

When running the tests, I initially encountered an issue. The expected result for `n = 5` was 55, but I was getting 125. This was because I mistakenly added the square of `n` instead of the square of `i` within the loop.

The correct statement should be:

```java
sum += i * i;
```

Once I corrected that, the tests passed successfully.

### Step 4: Final Code

Here is the final, correct implementation of the `calculateSumOfSquares` method:

```java
public static long calculateSumOfSquares(int n) {
    if (n < 0) {
        return -1;  // Handle invalid input
    }

    long sum = 0;  // Initialize sum

    for (int i = 1; i <= n; i++) {
        sum += i * i;  // Add the square of i to the sum
    }

    return sum;  // Return the total sum
}
```

### Step 5: Final Test

After fixing the logic, I ran the tests again, and they all passed successfully. The program now correctly calculates the sum of squares for any valid input `n` and handles invalid input (negative numbers) by returning `-1`.

### Conclusion:

In this exercise, we learned how to:
1. Loop from 1 to `n` and compute the sum of squares.
2. Handle edge cases such as negative inputs.
3. Debug and correct logic using print statements and careful analysis.

---

## Section 10: Java Coding Exercises - Set 2

## Solution Video For Coding Exercise - Inches to Object (Feet, Inches)

Let's walk through how to solve the **Inches to Object (Feet, Inches)** coding exercise.

### Problem Overview:
You need to complete the `Dimension` class, which represents a measurement in feet and inches. You're given a constructor that accepts an input in inches, and your task is to convert that value into feet and remaining inches.

### Requirements:
1. **Constructor**: The constructor takes a parameter `inches` and converts it to feet and inches.
   - If the input `inches` is less than zero, both feet and inches should be set to `-1`.
2. **Getters**: There are two getter methods:
   - `getFeet()` should return the feet value.
   - `getInches()` should return the remaining inches after conversion.

### Example:
If the input to the constructor is `25` inches:
- 12 inches = 1 foot, so 25 inches equals 2 feet and 1 inch (because 25 divided by 12 equals 2 feet, remainder 1 inch).
- For an invalid input, like `-1`, both feet and inches should be set to `-1`.

### Step 1: Implementing the Constructor

We start by implementing the constructor, where we need to:
- Convert inches to feet and inches.
- If the input inches are less than 0, set feet and inches to `-1`.

Here’s the code to handle the conversion:

```java
public Dimension(int inches) {
    if (inches < 0) {
        this.feet = -1;
        this.inches = -1;
    } else {
        this.feet = inches / 12;  // Convert inches to feet
        this.inches = inches % 12; // Get the remaining inches
    }
}
```

- **If `inches` is less than 0**: Set both `this.feet` and `this.inches` to `-1`.
- **Otherwise**: 
  - `inches / 12` gives the number of feet (integer division).
  - `inches % 12` gives the remainder (remaining inches).

### Step 2: Implementing the Getter Methods

Next, we need to implement the `getFeet()` and `getInches()` methods to return the values stored in the instance variables.

```java
public int getFeet() {
    return this.feet;
}

public int getInches() {
    return this.inches;
}
```

### Step 3: Running the Tests

Now that we've implemented the constructor and the getter methods, we can run the tests. 

Let’s see if the tests pass by running them.

### Debugging:
If we encounter an issue where the expected output for negative input (like `-1`) is incorrect, it’s likely because we didn’t properly set the member variables (`this.feet` and `this.inches`) to `-1`. This can be fixed by ensuring that we always refer to the member variables using `this`.

### Final Code:

```java
public class Dimension {
    private int feet;
    private int inches;

    public Dimension(int inches) {
        if (inches < 0) {
            this.feet = -1;
            this.inches = -1;
        } else {
            this.feet = inches / 12;  // Convert inches to feet
            this.inches = inches % 12; // Get the remaining inches
        }
    }

    public int getFeet() {
        return this.feet;
    }

    public int getInches() {
        return this.inches;
    }
}
```

### Step 4: Explanation

- **Integer Division (`/`)**: This gives the number of whole feet.
- **Modulo (`%`)**: This gives the remainder, which is the number of remaining inches.
- **Handling Negative Input**: If `inches` is less than zero, both feet and inches are set to `-1`, as per the requirement.

### Step 5: Conclusion

We’ve successfully implemented the `Dimension` class with the constructor and the getter methods. The tests should now pass, confirming that our implementation works for both valid and invalid inputs.

---

## Solution Video For Coding Exercise - Create a Square Class

Let’s go through the **Create a Square class** coding exercise.

### Problem Overview:
In this exercise, you need to implement a class called `Square`. The class models a geometric shape—a square—and handles operations like calculating the area and perimeter.

### Requirements:
1. **Constructor**: The `Square` class has one private instance variable, `side` (type `int`), which represents the length of the side of the square. The constructor takes an integer argument to initialize the `side` attribute.
2. **calculateArea Method**: 
   - This method calculates the area using the formula `side * side`.
   - If the `side` value is less than or equal to 0, the method should return `-1` to indicate invalid input.
3. **calculatePerimeter Method**:
   - This method calculates the perimeter using the formula `4 * side`.
   - Similarly, if the `side` value is less than or equal to 0, it should return `-1`.

### Step 1: Implement the Constructor

First, let’s implement the constructor to initialize the `side` variable. It will simply set the value passed in through the parameter.

```java
public class Square {
    private int side;

    public Square(int side) {
        this.side = side;
    }
}
```

The constructor takes an integer `side` as input and assigns it to the instance variable `side`.

### Step 2: Implement the `calculateArea` Method

The next step is to implement the method to calculate the area. Remember:
- If `side` is less than or equal to 0, return `-1`.
- Otherwise, return the area using the formula `side * side`.

```java
public int calculateArea() {
    if (side <= 0) {
        return -1;  // Return -1 for invalid side length
    }
    return side * side;  // Return the area (side * side)
}
```

### Step 3: Implement the `calculatePerimeter` Method

Now, let’s implement the method to calculate the perimeter. Similar to `calculateArea`, it must return `-1` if `side` is invalid and otherwise return `4 * side`.

```java
public int calculatePerimeter() {
    if (side <= 0) {
        return -1;  // Return -1 for invalid side length
    }
    return 4 * side;  // Return the perimeter (4 * side)
}
```

### Step 4: Running the Tests

Once the implementation is complete, we can run the tests to verify if everything is working correctly.

### Final Code:

```java
public class Square {
    private int side;

    public Square(int side) {
        this.side = side;
    }

    public int calculateArea() {
        if (side <= 0) {
            return -1;
        }
        return side * side;
    }

    public int calculatePerimeter() {
        if (side <= 0) {
            return -1;
        }
        return 4 * side;
    }
}
```

### Step 5: Explanation

- **Constructor**: Initializes the `side` variable.
- **calculateArea**: Validates the `side` value and returns `-1` for invalid input or the calculated area (`side * side`).
- **calculatePerimeter**: Validates the `side` value and returns `-1` for invalid input or the calculated perimeter (`4 * side`).

### Step 6: Conclusion

All the tests should pass, confirming that your implementation is correct. This was a straightforward exercise where you learned to create a class with a constructor and simple methods to perform calculations, including handling invalid inputs.

---

## Solution Video For Coding Exercise - Create a Point Class with 2D Coordinates

Let’s go through the **Create a Point class with 2D coordinates** coding exercise.

### Problem Overview:
In this exercise, you need to complete the implementation of a `Point` class in Java. The `Point` class represents a point in two-dimensional space with x and y coordinates. You are given a partial implementation, and you need to finish the methods `move` and `distanceTo`.

### Requirements:
1. **move(dx, dy)**:
   - This method adjusts the current position of the point by adding `dx` to `x` and `dy` to `y`.
   - Example: If the point is at (3, 4) and `move(1, 2)` is called, the new coordinates should be (4, 6).

2. **distanceTo(other)**:
   - This method calculates and returns the Euclidean distance between the current point and another point, which is passed as a parameter.
   - Formula: 
     \[
     d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
     \]
   - Example: If the point is (3, 4) and the other point is (6, 8), the Euclidean distance should be 5.

### Step 1: Implement the `move` Method

Let’s start by implementing the `move` method. This method modifies the current point by adjusting its x and y coordinates based on `dx` and `dy`.

```java
public void move(int dx, int dy) {
    this.x += dx;
    this.y += dy;
}
```

Here, we simply add `dx` to the current x-coordinate and `dy` to the current y-coordinate.

### Step 2: Implement the `distanceTo` Method

Next, we’ll implement the `distanceTo` method, which calculates the Euclidean distance between two points. We will use the distance formula:
\[
d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
\]

```java
public double distanceTo(Point other) {
    int diffX = this.x - other.x;
    int diffY = this.y - other.y;
    return Math.sqrt(diffX * diffX + diffY * diffY);
}
```

- **diffX**: The difference between the x-coordinates of the two points.
- **diffY**: The difference between the y-coordinates of the two points.
- We then calculate the square of `diffX` and `diffY`, sum them up, and return the square root of the result using `Math.sqrt()`.

### Step 3: Run Tests

Let’s now run the tests to see if everything works as expected.

### Final Code:

```java
public class Point {
    private int x;
    private int y;

    public Point(int x, int y) {
        this.x = x;
        this.y = y;
    }

    public int getX() {
        return x;
    }

    public int getY() {
        return y;
    }

    public void move(int dx, int dy) {
        this.x += dx;
        this.y += dy;
    }

    public double distanceTo(Point other) {
        int diffX = this.x - other.x;
        int diffY = this.y - other.y;
        return Math.sqrt(diffX * diffX + diffY * diffY);
    }
}
```

### Step 4: Explanation

- **Constructor**: Initializes the x and y coordinates.
- **move(dx, dy)**: Adjusts the point’s position by adding `dx` to `x` and `dy` to `y`.
- **distanceTo(Point other)**: Uses the Euclidean distance formula to calculate the distance between the current point and another point.

### Step 5: Conclusion

All the tests should now pass, indicating that the implementation is correct. This exercise gave you hands-on practice with manipulating object properties and applying mathematical formulas.

---

## Solution Video For Coding Exercise - RGB Color Class

In this exercise, we’re going to implement the **RGB Color Class**, a fun and practical problem that involves manipulating color values.

### Problem Overview:
In the **RGB** (Red, Green, Blue) color model, each color is a combination of the three primary colors—red, green, and blue—each with an intensity value ranging from 0 to 255. This exercise requires us to complete an **RGB Color** class, where:
- You have fields for red, green, and blue values.
- You need to implement getter methods for these values.
- You need to implement a method that **inverts** the color by subtracting each color component from 255.

### Requirements:
1. **Constructor**: 
   - Takes three integer arguments representing the red, green, and blue values and initializes the instance variables.
   
2. **Getter Methods**: 
   - `getRed()`: Returns the red component.
   - `getGreen()`: Returns the green component.
   - `getBlue()`: Returns the blue component.
   
3. **invert()**:
   - Inverts the color by subtracting the current values of red, green, and blue from 255.

### Example:
If you create an RGB object like `new RGBColor(255, 0, 0)`, calling `color.invert()` should change the color to (0, 255, 255).

### Step 1: Implement the Constructor

The first step is to complete the constructor, which initializes the `red`, `green`, and `blue` values using the passed arguments.

```java
public RGBColor(int red, int green, int blue) {
    this.red = red;
    this.green = green;
    this.blue = blue;
}
```

### Step 2: Implement the Getter Methods

Next, we implement the getter methods to return the values of red, green, and blue.

```java
public int getRed() {
    return this.red;
}

public int getGreen() {
    return this.green;
}

public int getBlue() {
    return this.blue;
}
```

These methods will simply return the corresponding color component.

### Step 3: Implement the `invert()` Method

In the `invert()` method, we need to change each color component to its complement by subtracting the current value from 255.

```java
public void invert() {
    this.red = 255 - this.red;
    this.green = 255 - this.green;
    this.blue = 255 - this.blue;
}
```

For example:
- If `red` is 255, the new `red` value will be `255 - 255 = 0`.
- If `green` is 0, the new `green` value will be `255 - 0 = 255`.
- The same logic applies to `blue`.

### Step 4: Test the Code

Now that we have implemented the constructor, getter methods, and the `invert()` method, let's run the tests to ensure everything works correctly.

### Full Code Implementation:

```java
public class RGBColor {
    private int red;
    private int green;
    private int blue;

    public RGBColor(int red, int green, int blue) {
        this.red = red;
        this.green = green;
        this.blue = blue;
    }

    public int getRed() {
        return red;
    }

    public int getGreen() {
        return green;
    }

    public int getBlue() {
        return blue;
    }

    public void invert() {
        this.red = 255 - this.red;
        this.green = 255 - this.green;
        this.blue = 255 - this.blue;
    }
}
```

### Step 5: Explanation

- **Constructor**: Initializes the `red`, `green`, and `blue` values.
- **getRed(), getGreen(), getBlue()**: Simple getter methods to return the current values of the red, green, and blue color components.
- **invert()**: Inverts the color by subtracting each color component from 255.

### Step 6: Conclusion

After running the tests, everything should pass successfully. This exercise was a great introduction to object-oriented principles, getter methods, and basic operations on class fields.

---

## Section 13: Java Coding Exercises - Set 3

## Solution Video For Coding Exercise - Is Valid Triangle

I hope you had a chance to attempt the **Is Valid Triangle** exercise. If not, give it a try before diving into the solution, as practicing the problem on your own will help you understand it better.

### Problem Overview:

In this exercise, you are provided with three integer inputs that represent the angles of a triangle: `angle1`, `angle2`, and `angle3`. You need to implement a method named **`isValidTriangle`**, which checks whether these three angles form a valid triangle.

### Conditions for a Valid Triangle:
1. **All angles must be positive integers** (greater than 0).
2. **The sum of the three angles must equal 180 degrees**.

If both conditions are satisfied, the method should return **true**, indicating the angles form a valid triangle. Otherwise, it should return **false**.

### Step 1: Validate the Angles

The first step is to check whether each of the angles is a positive integer. If any of the angles is less than or equal to 0, we return **false** because a valid triangle cannot have non-positive angles.

```java
if (angle1 <= 0 || angle2 <= 0 || angle3 <= 0) {
    return false;
}
```

### Step 2: Check if the Sum of the Angles Equals 180

After validating the angles, the next step is to check if the sum of the three angles equals 180 degrees. If the sum is not equal to 180, the triangle is invalid, so we return **false**. If it is exactly 180, we return **true**.

```java
int sumOfAngles = angle1 + angle2 + angle3;
return sumOfAngles == 180;
```

### Full Code Implementation:

Here's the full implementation of the `isValidTriangle` method:

```java
public class TriangleValidator {
    
    public static boolean isValidTriangle(int angle1, int angle2, int angle3) {
        // Step 1: Check if all angles are positive
        if (angle1 <= 0 || angle2 <= 0 || angle3 <= 0) {
            return false;
        }

        // Step 2: Check if the sum of angles equals 180 degrees
        int sumOfAngles = angle1 + angle2 + angle3;
        return sumOfAngles == 180;
    }
}
```

### Explanation:

1. **Validate the Angles**: We check if any of the angles is less than or equal to zero using the condition `angle1 <= 0 || angle2 <= 0 || angle3 <= 0`. If this condition is true, we return **false** because a valid triangle requires all angles to be positive.
  
2. **Check the Sum of Angles**: We calculate the sum of the angles using `int sumOfAngles = angle1 + angle2 + angle3`. If the sum equals 180, we return **true**, otherwise, **false**.

### Step 3: Test the Code

Let's now run the tests to ensure the solution works correctly.

- **Test Case 1**: `isValidTriangle(60, 60, 60)` → **true** (Equilateral triangle)
- **Test Case 2**: `isValidTriangle(90, 45, 45)` → **true** (Right-angled triangle)
- **Test Case 3**: `isValidTriangle(0, 90, 90)` → **false** (Invalid, zero angle)
- **Test Case 4**: `isValidTriangle(90, 90, 10)` → **false** (Sum is not 180)

All tests should pass successfully!

### Conclusion:

This was a simple yet practical exercise where we learned to validate inputs and apply conditions to solve a problem. We ensured the angles were positive and checked whether their sum equaled 180 degrees to determine if the inputs formed a valid triangle.

---

## Solution Video For Coding Exercise - Is Right Angled Triangle

I hope you had a chance to try the "Is Right Angled Triangle" exercise. If you haven’t, take a moment to work through it before jumping into the solution. Practicing on your own will help solidify your understanding.

### Problem Overview:

You are given three integer inputs representing the lengths of the sides of a triangle: `side1`, `side2`, and `side3`. Your task is to complete the `isRightAngled` method, which determines whether the triangle formed by these sides is a **right-angled triangle**. The method should return `true` if it is a right-angled triangle and `false` otherwise.

### Approach:

To determine if a triangle is a right-angled triangle, we can use the **Pythagorean Theorem**.

Where the **hypotenuse** is the longest side of the triangle. 

### Step 1: Check Validity of Side Lengths

First, we ensure that all side lengths are greater than zero. If any side is less than or equal to zero, it’s not a valid triangle, so we return `false`.

```java
if (side1 <= 0 || side2 <= 0 || side3 <= 0) {
    return false;
}
```

### Step 2: Check the Pythagorean Theorem

Next, we use the Pythagorean Theorem to check whether the triangle is right-angled. There are three possible configurations for the hypotenuse (longest side), so we check each possibility:

1. **Hypotenuse = side3**: Check if \((side1)^2 + (side2)^2 = (side3)^2\)
2. **Hypotenuse = side2**: Check if \((side1)^2 + (side3)^2 = (side2)^2\)
3. **Hypotenuse = side1**: Check if \((side2)^2 + (side3)^2 = (side1)^2\)

If any of these conditions hold true, we return `true`. If none of them hold, we return `false`.

### Full Code Implementation:

```java
public class TriangleValidator {
    
    public static boolean isRightAngled(int side1, int side2, int side3) {
        // Step 1: Validate that all sides are positive
        if (side1 <= 0 || side2 <= 0 || side3 <= 0) {
            return false;
        }

        // Step 2: Check if any combination of sides satisfies the Pythagorean theorem
        if (side1 * side1 + side2 * side2 == side3 * side3 ||
            side2 * side2 + side3 * side3 == side1 * side1 ||
            side3 * side3 + side1 * side1 == side2 * side2) {
            return true;
        }

        // If none of the conditions hold, it's not a right-angled triangle
        return false;
    }
}
```

### Explanation:

1. **Side Validation**: We start by checking if any of the side lengths are zero or negative. If so, we return `false` because it's not a valid triangle.
  
2. **Pythagorean Theorem Check**: We check all three possible configurations for the hypotenuse:
   - Hypotenuse = `side3`: \((side1)^2 + (side2)^2 = (side3)^2\)
   - Hypotenuse = `side2`: \((side1)^2 + (side3)^2 = (side2)^2\)
   - Hypotenuse = `side1`: \((side2)^2 + (side3)^2 = (side1)^2\)
   
   If any of these conditions are met, we return `true`. If none are met, the triangle is not right-angled, so we return `false`.

### Step 3: Test the Code

Let’s test the solution with different inputs:

- **Test Case 1**: `isRightAngled(3, 4, 5)` → **true** (Pythagorean triplet)
- **Test Case 2**: `isRightAngled(5, 12, 13)` → **true** (Pythagorean triplet)
- **Test Case 3**: `isRightAngled(1, 2, 3)` → **false** (Not a valid triangle)
- **Test Case 4**: `isRightAngled(6, 8, 10)` → **true** (Pythagorean triplet)
- **Test Case 5**: `isRightAngled(0, 4, 5)` → **false** (Invalid side length)

### Conclusion:

This was a great exercise to reinforce our understanding of the Pythagorean Theorem and to practice condition-based logic. By checking multiple configurations for the hypotenuse, we ensure our method works for any input.

---

## Solution Video For Coding Exercise - Is Leap Year

I hope you've had the opportunity to try out the "Is Leap Year" exercise. If you haven't yet, pause here, give it a shot, and then come back to check out the solution. This will reinforce your learning and help you get comfortable with logical conditions and control structures.

### Problem Overview:

In this exercise, you're tasked with determining whether a given year is a leap year based on a set of rules. The method `isLeapYear` takes an integer representing the year, and it should return `true` if the year is a leap year and `false` otherwise.

### Rules for Identifying a Leap Year:

1. **Divisibility by 4**: A year is a leap year if it is divisible by 4.
2. **Divisibility by 100**: If a year is divisible by 100, it is **not** a leap year, unless...
3. **Divisibility by 400**: If a year is divisible by 400, it **is** a leap year (overriding the divisibility by 100 rule).

### Example Breakdown:

- **2041**: Not divisible by 4, so it is **not** a leap year.
- **2048**: Divisible by 4, and not divisible by 100, so it **is** a leap year.
- **2000**: Divisible by 4 and 100, but also divisible by 400, so it **is** a leap year.
- **2100**: Divisible by 4 and 100, but **not** divisible by 400, so it is **not** a leap year.

Now, let's implement this logic step by step in the `isLeapYear` method.

### Step-by-Step Solution:

### Step 1: Handling the Edge Case (Year ≤ 0)

The Gregorian calendar does not have a year 0 or negative years, so we first check whether the year is less than or equal to zero. If so, we return `false` immediately.

```java
if (year <= 0) {
    return false;
}
```

### Step 2: Check if Year is Divisible by 4

If the year is not divisible by 4, it cannot be a leap year.

```java
if (year % 4 != 0) {
    return false;
}
```

### Step 3: Handling Years Divisible by 100

If the year is divisible by 4, we next check whether it is divisible by 100. If the year is divisible by 100 but **not** divisible by 400, it is not a leap year.

```java
if (year % 100 == 0 && year % 400 != 0) {
    return false;
}
```

### Step 4: If None of the Above, It's a Leap Year

If all the previous conditions fail, the year is a leap year.

```java
return true;
```

### Full Code Implementation:

```java
public class LeapYearChecker {
    
    public static boolean isLeapYear(int year) {
        // Step 1: Check for invalid year
        if (year <= 0) {
            return false;
        }
        
        // Step 2: Check if the year is divisible by 4
        if (year % 4 != 0) {
            return false;
        }
        
        // Step 3: Check if the year is divisible by 100 but not by 400
        if (year % 100 == 0 && year % 400 != 0) {
            return false;
        }
        
        // If none of the above conditions match, it's a leap year
        return true;
    }
}
```

### Explanation of the Code:

1. **Year Validation**: We first check if the year is less than or equal to zero. If it is, we return `false` because such a year is not valid in the Gregorian calendar.
  
2. **Divisibility by 4**: If the year is not divisible by 4, it is not a leap year, so we return `false`.

3. **Divisibility by 100**: If the year is divisible by both 100 and 4, we check if it is divisible by 400. If it’s not divisible by 400, it is not a leap year, so we return `false`.

4. **Leap Year**: If none of the previous conditions match, it means the year is a leap year, and we return `true`.

### Testing the Solution:

Let’s test the solution with different inputs:

- **Year 2041**: Not divisible by 4 → **false**
- **Year 2048**: Divisible by 4 and not divisible by 100 → **true**
- **Year 2000**: Divisible by 4, 100, and 400 → **true**
- **Year 2100**: Divisible by 4 and 100 but not 400 → **false**
- **Year 0**: Invalid year → **false**

### Conclusion:

This exercise was a good demonstration of using multiple logical conditions to solve a real-world problem like determining leap years. Handling special cases (like divisibility rules and invalid years) is crucial for creating robust solutions.

---

## Solution Video For Coding Exercise - Is Perfect Number

It's time to solve another coding exercise, and this one is called **Is Perfect Number**. Let’s walk through the problem and its solution step by step.

### Problem Overview:

In this exercise, you are tasked with implementing a method in the `PerfectNumberChecker` class that checks whether a given number is a **perfect number**.

### What is a Perfect Number?

A perfect number is a positive integer that is equal to the sum of all its positive divisors, **excluding itself**. For example:
- **6** is a perfect number because its divisors (excluding itself) are 1, 2, and 3, and 1 + 2 + 3 = 6.
- **28** is a perfect number because its divisors (excluding itself) are 1, 2, 4, 7, and 14, and 1 + 2 + 4 + 7 + 14 = 28.

### Task:
The method should return `true` if the number is a perfect number and `false` otherwise.

### Additional Instructions:
- A perfect number is always a **positive integer**.
- If the number is less than or equal to zero, return `false` immediately.

### Plan:

1. First, check if the number is less than or equal to zero. If so, return `false`.
2. Loop through all numbers from 1 to `number - 1`, checking for divisors.
3. Sum up all divisors.
4. If the sum of divisors equals the original number, return `true`. Otherwise, return `false`.

### Step-by-Step Solution:

### Step 1: Validate Input

We start by checking if the number is less than or equal to zero. If that's the case, we know it's not a perfect number.

```java
if (number <= 0) {
    return false;
}
```

### Step 2: Loop to Find Divisors

We need to loop through numbers from 1 to `number - 1` and check if each number is a divisor of the given number. We use the modulo (`%`) operator to find the divisors.

```java
int sum = 0;
for (int i = 1; i < number; i++) {
    if (number % i == 0) {
        sum += i;
    }
}
```

Here, for each divisor `i` (where `number % i == 0`), we add `i` to the `sum`.

### Step 3: Check if the Sum Equals the Original Number

At the end of the loop, if the sum of the divisors is equal to the original number, it's a perfect number.

```java
return sum == number;
```

### Full Code Implementation:

```java
public class PerfectNumberChecker {

    public static boolean isPerfectNumber(int number) {
        // Step 1: Handle the case where the number is less than or equal to 0
        if (number <= 0) {
            return false;
        }

        // Step 2: Find divisors and calculate their sum
        int sum = 0;
        for (int i = 1; i < number; i++) {
            if (number % i == 0) {
                sum += i;  // Add divisor to sum
            }
        }

        // Step 3: Check if the sum of divisors equals the original number
        return sum == number;
    }
}
```

### Explanation of the Code:

1. **Input Validation**: We first check if the number is less than or equal to zero. Since a perfect number must be positive, we return `false` in this case.
  
2. **Finding Divisors**: We loop through all numbers from 1 to `number - 1`. For each number `i` that divides `number` evenly (i.e., `number % i == 0`), we add `i` to the `sum`.

3. **Returning the Result**: After calculating the sum of divisors, we compare it with the original number. If they are equal, the number is a perfect number, and we return `true`. Otherwise, we return `false`.

### Testing the Solution:

Let’s test the solution with different inputs:

- **6**: Divisors are 1, 2, 3, and 1 + 2 + 3 = 6 → **true** (Perfect number).
- **28**: Divisors are 1, 2, 4, 7, 14, and 1 + 2 + 4 + 7 + 14 = 28 → **true** (Perfect number).
- **12**: Divisors are 1, 2, 3, 4, 6, and 1 + 2 + 3 + 4 + 6 = 16 → **false** (Not a perfect number).
- **0**: Not a valid number for checking a perfect number → **false**.

### Conclusion:

In this exercise, we implemented a method to determine if a number is a perfect number by:
1. Validating the input.
2. Summing the divisors of the number (excluding the number itself).
3. Returning `true` if the sum equals the original number, otherwise `false`.

---

## Solution Video For Coding Exercise - Student Grades A to F based on Marks

In this exercise, we will write a program that assigns a grade (A to F) to a student based on their marks. Let's walk through the problem step by step and solve it.

### Problem Overview:

You're tasked with implementing the functionality of a `Student` class that calculates and assigns the student's grade based on the provided marks.

### Grading Criteria:

- **Marks >= 90**: Grade A
- **Marks >= 80**: Grade B
- **Marks >= 70**: Grade C
- **Marks >= 60**: Grade D
- **Marks >= 50**: Grade E
- **Marks < 50**: Grade F
- If the marks are less than 0 or greater than 100, return 'X' to indicate invalid marks.

### Steps to Solve:

1. **Constructor**: We will initialize the student's marks using the constructor.
2. **Assign Grade Method**: We will implement the logic to assign grades based on the criteria mentioned above.

### Step-by-Step Solution:

### Step 1: Constructor

We start by implementing the constructor to initialize the `marks` instance variable.

```java
public class Student {
    int marks;

    // Constructor
    public Student(int marks) {
        this.marks = marks;
    }
}
```

Here, the constructor initializes the `marks` with the value passed as an argument.

### Step 2: Assign Grade Logic

Now, let's implement the `assignGrade` method that returns the appropriate grade based on the marks.

#### 2.1: Invalid Marks Case

First, we check if the marks are invalid. Marks must be between 0 and 100. If the marks are outside this range, we return 'X'.

```java
if (marks > 100 || marks < 0) {
    return 'X';  // Invalid marks
}
```

#### 2.2: Grade A to F

Next, we implement the grading logic based on the marks ranges:

- If marks are greater than or equal to 90, return 'A'.
- If marks are greater than or equal to 80, return 'B'.
- If marks are greater than or equal to 70, return 'C'.
- If marks are greater than or equal to 60, return 'D'.
- If marks are greater than or equal to 50, return 'E'.
- Otherwise, return 'F' (for marks less than 50).

Here’s the code:

```java
public char assignGrade() {
    if (marks > 100 || marks < 0) {
        return 'X';  // Invalid marks
    }
    if (marks >= 90) {
        return 'A';
    }
    if (marks >= 80) {
        return 'B';
    }
    if (marks >= 70) {
        return 'C';
    }
    if (marks >= 60) {
        return 'D';
    }
    if (marks >= 50) {
        return 'E';
    }
    return 'F';  // Marks less than 50
}
```

### Full Code Implementation:

```java
public class Student {
    int marks;

    // Constructor
    public Student(int marks) {
        this.marks = marks;
    }

    // Method to assign grade based on marks
    public char assignGrade() {
        if (marks > 100 || marks < 0) {
            return 'X';  // Invalid marks
        }
        if (marks >= 90) {
            return 'A';
        }
        if (marks >= 80) {
            return 'B';
        }
        if (marks >= 70) {
            return 'C';
        }
        if (marks >= 60) {
            return 'D';
        }
        if (marks >= 50) {
            return 'E';
        }
        return 'F';  // Marks less than 50
    }
}
```

### Explanation:

1. **Input Validation**: We first check if the marks are valid. Marks should be between 0 and 100. If the marks are not within this range, we return 'X' for invalid input.
  
2. **Grading Logic**: 
   - We check the conditions in descending order from the highest grade (A) to the lowest grade (F). 
   - Each condition is evaluated in sequence, and the correct grade is returned based on the marks range.
  
3. **Efficiency**: The program checks each condition one at a time, returning the appropriate grade as soon as the condition is met. If no condition is met, it returns 'F' for marks less than 50.

### Testing the Solution:

Let’s test the solution with various inputs:

- **Marks = 95**: Should return 'A'.
- **Marks = 85**: Should return 'B'.
- **Marks = 75**: Should return 'C'.
- **Marks = 65**: Should return 'D'.
- **Marks = 55**: Should return 'E'.
- **Marks = 45**: Should return 'F'.
- **Marks = -10**: Should return 'X' (invalid input).
- **Marks = 105**: Should return 'X' (invalid input).

### Running the Tests:

After implementing the solution, we run the test cases, and the solution successfully passes all of them.

- Test for grade 'A', 'B', 'C', 'D', 'E', 'F', and invalid grade 'X'.
- All the tests pass successfully.

### Conclusion:

In this exercise, we implemented a `Student` class that assigns grades to students based on their marks. We handled various conditions for valid and invalid marks and used simple if-statements to determine the correct grade. 

---

## Solution Video For Coding Exercise - Weather Advisor

In this exercise, we're going to implement a class that provides advice on what to wear based on the current temperature. Let's go over the problem step by step.

### Problem Overview:

You are tasked with implementing a method called `provideWeatherAdvisory` inside the `WeatherAdvisor` class. The method takes a temperature as input and returns a string containing advice on what to wear based on the given temperature.

### Temperature Ranges and Corresponding Advice:

- **Temperature < 0**: Return `"It's freezing! Stay inside!"`
- **Temperature between 0 and 10 (inclusive)**: Return `"It's cold! Bundle up."`
- **Temperature between 11 and 20 (inclusive)**: Return `"It's cool! A light jacket will do."`
- **Temperature > 20**: Return `"It's warm! Enjoy the day."`

### Step-by-Step Solution:

### Step 1: Skeleton Code

The provided skeleton includes the method signature and the task is to fill in the logic for determining the appropriate weather advice based on the temperature. 

We have the method:
```java
public class WeatherAdvisor {
    public String provideWeatherAdvisory(int temperature) {
        // TODO: Implement the logic here
    }
}
```

### Step 2: Implementing the Logic

We will write conditional statements to check the temperature and return the appropriate advice.

1. **Temperature less than 0**: We return `"It's freezing! Stay inside!"`
2. **Temperature between 0 and 10 (inclusive)**: We return `"It's cold! Bundle up."`
3. **Temperature between 11 and 20 (inclusive)**: We return `"It's cool! A light jacket will do."`
4. **Temperature greater than 20**: We return `"It's warm! Enjoy the day."`

Here’s the implementation:

```java
public class WeatherAdvisor {
    public String provideWeatherAdvisory(int temperature) {
        if (temperature < 0) {
            return "It's freezing! Stay inside!";
        } 
        if (temperature <= 10) {
            return "It's cold! Bundle up.";
        } 
        if (temperature <= 20) {
            return "It's cool! A light jacket will do.";
        }
        return "It's warm! Enjoy the day.";
    }
}
```

### Explanation:

- **First Condition**: If the temperature is less than 0, we return `"It's freezing! Stay inside!"`
- **Second Condition**: If the temperature is between 0 and 10 (inclusive), we return `"It's cold! Bundle up."`
- **Third Condition**: If the temperature is between 11 and 20 (inclusive), we return `"It's cool! A light jacket will do."`
- **Final Condition**: If the temperature is greater than 20, we return `"It's warm! Enjoy the day."`

### Step 3: Optimizing the Code

We can simplify the code by removing the unnecessary `else` statements. Since each `if` block either returns a value or continues to the next condition, there is no need for the `else`.

Here’s the optimized version:

```java
public class WeatherAdvisor {
    public String provideWeatherAdvisory(int temperature) {
        if (temperature < 0) {
            return "It's freezing! Stay inside!";
        }
        if (temperature <= 10) {
            return "It's cold! Bundle up.";
        }
        if (temperature <= 20) {
            return "It's cool! A light jacket will do.";
        }
        return "It's warm! Enjoy the day.";
    }
}
```

### Testing the Solution:

Let’s test the solution with a few inputs:

- **Temperature = -5**: Should return `"It's freezing! Stay inside!"`
- **Temperature = 5**: Should return `"It's cold! Bundle up."`
- **Temperature = 15**: Should return `"It's cool! A light jacket will do."`
- **Temperature = 25**: Should return `"It's warm! Enjoy the day."`

### Running the Tests:

After running the tests, all the test cases pass successfully.

### Conclusion:

In this exercise, we successfully implemented a `WeatherAdvisor` class that provides advice based on the temperature. The conditions were straightforward, and we optimized the code for readability and simplicity.

---

## Solution Video For Coding Exercise - Switch with Char: Is a Vowel or Not

Let's dive into another exercise—this time, it's about using a **switch statement** with a `char` type to determine whether a character is a vowel or not. We're going to implement a method inside the `MyChar` class that checks if the given character is a vowel (either uppercase or lowercase).

### Problem Overview:

We need to implement the method `isVowel` in the `MyChar` class. This method accepts a character as input and returns `true` if the character is a vowel (`A`, `E`, `I`, `O`, `U`—both uppercase and lowercase) and `false` otherwise.

### Step-by-Step Solution:

### Step 1: Skeleton Code

The provided skeleton contains the following:

```java
public class MyChar {
    public boolean isVowel(char ch) {
        switch (ch) {
            // TODO: Implement the switch cases
        }
        return false;
    }
}
```

Our task is to implement the switch cases for the vowels (both lowercase and uppercase) inside the `isVowel` method.

### Step 2: Implementing the Switch Statement

To start, we'll write a switch statement that checks for both lowercase (`a`, `e`, `i`, `o`, `u`) and uppercase (`A`, `E`, `I`, `O`, `U`) vowels. If the character matches any of these cases, we return `true`; otherwise, we return `false`.

Here’s how we can start:

```java
public class MyChar {
    public boolean isVowel(char ch) {
        switch (ch) {
            case 'a':
            case 'e':
            case 'i':
            case 'o':
            case 'u':
            case 'A':
            case 'E':
            case 'I':
            case 'O':
            case 'U':
                return true;
            default:
                return false;
        }
    }
}
```

### Explanation:

- **Case 'a'**: If the input character is lowercase `a`, it returns `true`.
- We handle other vowels (`e`, `i`, `o`, `u` and their uppercase counterparts) in the same way by listing them in the switch cases.
- **Default**: If the character does not match any of the vowels, we return `false`.

### Step 3: Test and Run

Let’s test the solution with a few characters:

- Input: `'A'` should return `true`.
- Input: `'b'` should return `false`.
- Input: `'E'` should return `true`.
- Input: `'F'` should return `false`.

### Running the Tests:

All test cases should pass successfully.

### Step 4: Code Optimization

We can further simplify the code. Since multiple cases in our switch statement return the same value (`true` for vowels), we can leverage **fall-through** behavior. Instead of writing a return statement for each vowel, we group them together like this:

```java
public class MyChar {
    public boolean isVowel(char ch) {
        switch (ch) {
            case 'a', 'e', 'i', 'o', 'u':
            case 'A', 'E', 'I', 'O', 'U':
                return true;
            default:
                return false;
        }
    }
}
```

### Explanation of the Optimization:

- We combined all the lowercase vowels into a single case: `'a', 'e', 'i', 'o', 'u'`.
- Similarly, we combined all the uppercase vowels into one line: `'A', 'E', 'I', 'O', 'U'`.
- The `switch` statement now directly returns `true` for any of these cases and `false` for everything else.

### Final Code:

```java
public class MyChar {
    public boolean isVowel(char ch) {
        switch (ch) {
            case 'a', 'e', 'i', 'o', 'u':
            case 'A', 'E', 'I', 'O', 'U':
                return true;
            default:
                return false;
        }
    }
}
```

### Conclusion:

We successfully implemented the method to check whether a character is a vowel using a `switch` statement, and optimized the code to handle multiple cases efficiently. All test cases pass, and the code is easy to read and maintain.

---

## Section 15: Java Coding Exercises - Set 4

## Solution Video For Coding Exercise - Calculate Factorial Of a Number

Welcome back! In this exercise, we will calculate the factorial of a given number using Java. This is a common coding problem, and the logic behind it is straightforward once we understand the concept of a factorial.

### Problem Overview:

A **factorial** of a non-negative integer `N`, denoted as `N!`, is the product of all positive integers less than or equal to `N`. For example:

- `4! = 4 * 3 * 2 * 1 = 24`
- `3! = 3 * 2 * 1 = 6`
- `2! = 2 * 1 = 2`
- `1! = 1`

If the input is **negative**, we are required to return `-1` as factorials are not defined for negative numbers.

### Step-by-Step Solution:

### Step 1: Understanding the Skeleton

We have a class called `FactorialCalculator` with a method `calculateFactorial` that accepts an integer `number` as input. Our job is to implement this method to compute the factorial or return `-1` if the input is negative.

Here’s the starting skeleton code:

```java
public class FactorialCalculator {
    public int calculateFactorial(int number) {
        // TODO: Implement the method to calculate factorial
        return -1;
    }
}
```

### Step 2: Add Input Validation for Negative Numbers

The first thing we need to do is handle invalid input. If the number is negative, the method should return `-1`. This can be done with a simple `if` check:

```java
if (number < 0) {
    return -1;
}
```

### Step 3: Initialize a Variable for the Factorial Calculation

Next, we initialize a variable `factorial` with a value of `1`. This variable will store the result of the factorial as we multiply values from 2 up to `number`. Initializing it as `1` ensures that any number multiplied by it will retain its value (since multiplying by zero would result in zero, which is incorrect for factorials).

```java
int factorial = 1;
```

### Step 4: Loop to Calculate the Factorial

We now need to loop through all the numbers from `2` to `number`, multiplying them together and storing the result in the `factorial` variable. Here's how we can do that:

```java
for (int i = 2; i <= number; i++) {
    factorial *= i;
}
```

### Step 5: Return the Final Result

Finally, after the loop finishes, we return the `factorial` variable, which contains the calculated factorial of the input number.

```java
return factorial;
```

### Complete Code:

Here is the complete implementation of the `calculateFactorial` method:

```java
public class FactorialCalculator {
    public int calculateFactorial(int number) {
        if (number < 0) {
            return -1;
        }
        
        int factorial = 1;
        
        for (int i = 2; i <= number; i++) {
            factorial *= i;
        }
        
        return factorial;
    }
}
```

### Step 6: Test the Code

Let’s run the code with some test cases:

- Input: `4` should return `24` (since `4! = 4 * 3 * 2 * 1 = 24`)
- Input: `3` should return `6` (since `3! = 3 * 2 * 1 = 6`)
- Input: `2` should return `2`
- Input: `1` should return `1`
- Input: `0` should return `1` (since `0!` is defined as `1`)
- Input: `-5` should return `-1` (invalid input)

### Run the Tests:

After running the tests, all of them pass successfully. The code correctly handles positive numbers and the special case of negative input.

### Conclusion:

In this solution, we started by validating the input and then used a simple loop to calculate the factorial of a given number. The logic was straightforward—multiplying all integers from `2` to `number` to compute the factorial.

---

## Solution Video For Coding Exercise - Find Last Digit Of A Number

In this coding exercise, we are going to implement a method that retrieves the last digit of a given number. This exercise is simple, but it forms the basis for more complex tasks, so it's important to get it right.

### Problem Overview

We are tasked with completing the implementation of the `NumberUtils` class in Java, where we need to write a method to find the last digit of a number. Here are the specific rules:

1. **For positive numbers**, return the last digit.
   - Example: For `2345`, the last digit is `5`.
   - For `90`, the last digit is `0`.
2. **For zero**, return `0` as the last digit.
   - Example: For `0`, the last digit is `0`.
3. **For negative numbers**, return `-1` to indicate that we do not handle negative inputs.
   - Example: For `-67`, return `-1`.

### Step-by-Step Approach

### Step 1: Check for Negative Numbers

The first step is to handle negative inputs. If the number is negative, we need to return `-1` immediately. We can easily do this with an `if` condition:

```java
if (number < 0) {
    return -1;
}
```

### Step 2: Find the Last Digit

For non-negative numbers, we can find the last digit using the **modulo operation**. The expression `number % 10` gives us the remainder when the number is divided by 10, which is exactly the last digit.

For example:
- `2345 % 10` gives `5`
- `90 % 10` gives `0`
- `9 % 10` gives `9`

Thus, to get the last digit, we simply return `number % 10`.

### Complete Code

Here is the complete implementation of the `findLastDigit` method in the `NumberUtils` class:

```java
public class NumberUtils {
    public int findLastDigit(int number) {
        if (number < 0) {
            return -1;
        }
        return number % 10;
    }
}
```

### Step 3: Test the Code

Let’s walk through a few test cases to ensure our solution works:

1. **Positive Number (Example: 1234):**
   - The last digit of `1234` is `4`, so the method should return `4`.
2. **Number Ending in Zero (Example: 90):**
   - The last digit of `90` is `0`, so the method should return `0`.
3. **Single Digit Number (Example: 9):**
   - The last digit of `9` is `9`, so the method should return `9`.
4. **Zero (Example: 0):**
   - The last digit of `0` is `0`, so the method should return `0`.
5. **Negative Number (Example: -67):**
   - The input is negative, so the method should return `-1`.

### Run the Tests

After running the tests, all of them pass successfully, meaning our solution is correct.

### Conclusion

In this exercise, we learned how to find the last digit of a number using the modulo operator and handled different cases like negative numbers and zero. This simple exercise forms the foundation for more complex operations.

---

## Solution Video For Coding Exercise - Find Number of Digits in a Number

In this exercise, we're going to find the number of digits in a given number. This is a fundamental programming problem, and it’s great practice to improve your logic-building skills.

### Problem Overview

The task is to complete the implementation of a method that calculates the number of digits in a given integer.

- For **positive numbers**, return the total number of digits.
  - Example: For `12345`, the number of digits is `5`.
  - For `90`, the number of digits is `2`.
- For **zero**, return `1`. Even though it's zero, it's considered to have one digit.
  - Example: For `0`, the number of digits is `1`.
- For **negative numbers**, return `-1`. In this problem, we're not counting the digits for negative numbers.

### Step-by-Step Solution

Let's break down the steps needed to solve this problem:

### Step 1: Handle Edge Cases First

The first thing we want to do is handle the special cases for **zero** and **negative numbers**. The logic is simple:
- If the number is **negative**, we return `-1`.
- If the number is **zero**, we return `1`.

This is how we can implement the initial conditions:

```java
if (number < 0) {
    return -1;
}

if (number == 0) {
    return 1;
}
```

### Step 2: Calculate the Number of Digits for Positive Numbers

For positive numbers, we can use **integer division** to determine the number of digits. The idea is simple:
- Keep dividing the number by `10` until the number becomes zero.
- Each time you divide by `10`, you count how many times you are able to divide. This will give the total number of digits.

For example:
- Start with `12345`. Divide by `10` -> `1234`.
- Divide by `10` again -> `123`.
- Continue dividing until the number becomes zero.
- The number of divisions corresponds to the number of digits.

### Step 3: Implement the Loop

We will use a `while` loop to keep dividing the number by `10` until it becomes zero. For each division, we increment a counter:

```java
int numberOfDigits = 0;
while (number > 0) {
    number = number / 10;   // Integer division
    numberOfDigits++;
}
```

### Complete Code

Here is the complete implementation of the `getNumberOfDigits` method in the `NumberUtils` class:

```java
public class NumberUtils {
    public int getNumberOfDigits(int number) {
        if (number < 0) {
            return -1;  // Negative numbers return -1
        }
        
        if (number == 0) {
            return 1;  // Zero is considered to have one digit
        }
        
        int numberOfDigits = 0;
        
        // Divide the number by 10 until it becomes 0, counting how many times
        while (number > 0) {
            number = number / 10;
            numberOfDigits++;
        }
        
        return numberOfDigits;
    }
}
```

### Step 4: Test the Solution

Let’s go through a few test cases to ensure the solution works:

1. **Positive Number (Example: 12345):**
   - The number of digits is `5`.
2. **Number Ending in Zero (Example: 90):**
   - The number of digits is `2`.
3. **Zero (Example: 0):**
   - The number of digits is `1`.
4. **Negative Number (Example: -123):**
   - Since the number is negative, the output should be `-1`.

### Run the Tests

After running the tests, all of them pass successfully, which confirms that the solution works for all edge cases.

### Conclusion

In this exercise, we learned how to find the number of digits in a given number using integer division. We also handled special cases like zero and negative numbers.

---

## Solution Video For Coding Exercise - Calculate Sum of Digits of a Number

In this exercise, we are tasked with calculating the sum of the digits of a number. This is a common programming challenge that is similar to the exercise where we counted the number of digits in a number.

### Problem Overview

In this problem, you need to complete the implementation of the `NumberUtils` class in Java by writing a method called `getSumOfDigits`. This method should:

- **Return -1** if the input number is negative.
- **Return 0** if the input number is 0.
- For **positive numbers**, calculate and return the sum of its digits.

### Examples:
- For `1234`, the output should be `1 + 2 + 3 + 4 = 10`.
- For `90`, the output should be `9 + 0 = 9`.
- For `-45` (a negative number), the output should be `-1`.

### Approach

Let's break down how we can solve this problem step by step.

### Step 1: Handle Special Cases
We first handle the edge cases:
- If the number is **negative**, return `-1`.
- If the number is **zero**, return `0`.

### Step 2: Calculate the Sum of Digits
For positive numbers, we need to extract each digit and sum them. Here's how:
- Use the modulo operator (`%`) to get the last digit of the number.
- Add the last digit to the sum.
- Use integer division (`/`) by 10 to remove the last digit from the number.
- Repeat the process until the number becomes zero.

### Step 3: Loop Until the Number Becomes Zero
We will use a `while` loop to keep extracting digits and adding them until the number becomes zero.

### Implementation

Let's go ahead and implement the solution.

```java
public class NumberUtils {
    public int getSumOfDigits(int number) {
        // Step 1: Handle special cases
        if (number < 0) {
            return -1;
        }
        
        if (number == 0) {
            return 0;
        }
        
        // Step 2: Initialize sum of digits
        int sumOfDigits = 0;
        
        // Step 3: Extract digits and calculate the sum
        while (number > 0) {
            int digit = number % 10;       // Get the last digit
            sumOfDigits += digit;          // Add the digit to the sum
            number = number / 10;          // Remove the last digit from the number
        }
        
        // Step 4: Return the calculated sum
        return sumOfDigits;
    }
}
```

### How the Code Works

### Example 1: Input `1234`
- The initial number is `1234`.
- In the first iteration: `1234 % 10 = 4`, so the sum becomes `0 + 4 = 4`. Then, `1234 / 10 = 123`.
- In the second iteration: `123 % 10 = 3`, so the sum becomes `4 + 3 = 7`. Then, `123 / 10 = 12`.
- In the third iteration: `12 % 10 = 2`, so the sum becomes `7 + 2 = 9`. Then, `12 / 10 = 1`.
- In the fourth iteration: `1 % 10 = 1`, so the sum becomes `9 + 1 = 10`. Then, `1 / 10 = 0`, and the loop ends.

The final sum is `10`.

### Example 2: Input `90`
- The initial number is `90`.
- First iteration: `90 % 10 = 0`, so the sum becomes `0 + 0 = 0`. Then, `90 / 10 = 9`.
- Second iteration: `9 % 10 = 9`, so the sum becomes `0 + 9 = 9`. Then, `9 / 10 = 0`, and the loop ends.

The final sum is `9`.

### Example 3: Input `-45`
- The number is negative, so the method returns `-1` immediately without any further calculation.

### Test the Solution

We can test this solution with various test cases to ensure it works for all edge cases:

1. **Positive Number**: `1234` → Output: `10`.
2. **Single Digit**: `9` → Output: `9`.
3. **Zero**: `0` → Output: `0`.
4. **Negative Number**: `-45` → Output: `-1`.

### Run the Tests

After running the tests, all of them passed successfully:

- 15 test cases, including edge cases like `0`, negative numbers, and different positive numbers, were tested.
- The solution passed all the tests.

### Conclusion

In this exercise, we learned how to calculate the sum of the digits of a number by using a simple loop with the modulo and division operations. We also handled special cases for zero and negative numbers.

---

## Solution Video For Coding Exercise - Reverse a Number

In this problem, we will be working on reversing a number.

### Problem Overview

You are tasked with completing the method `reverseNumber` in the `NumberUtils` class. This method takes an integer as input and returns the reversed version of the number. Here are the specific rules:

- If the input number is **0**, the method should return `0`.
- If the input number is **negative**, the method should return `-1`.
- For any positive number, the method should return the reversed number.

### Examples:
- Input: `123` → Output: `321`
- Input: `5497` → Output: `7945`
- Input: `-456` → Output: `-1`
- Input: `0` → Output: `0`

Now that we understand the requirements, let's get started!

### Approach

### Step 1: Handle Edge Cases
We need to handle two specific edge cases first:
1. If the number is **negative**, return `-1`.
2. If the number is **zero**, return `0`.

### Step 2: Reversing the Number
To reverse a number:
1. Extract the digits starting from the rightmost one. We can do this by using the modulo operator (`% 10`).
2. Keep adding the digits to a new number, adjusting the position of each new digit by multiplying the previous result by 10.
3. Continue until all the digits have been extracted.

### Step 3: Return the Reversed Number
Once all digits are processed, return the reversed number.

### Code Implementation

Let's break down how to implement this in Java.

```java
public class NumberUtils {
    public int reverseNumber(int number) {
        // Step 1: Handle edge cases
        if (number < 0) {
            return -1; // Negative number returns -1
        }
        if (number == 0) {
            return 0; // Zero returns zero
        }

        // Step 2: Initialize variables
        int reversedNumber = 0;
        while (number > 0) {
            int digit = number % 10;            // Extract the last digit
            reversedNumber = reversedNumber * 10 + digit; // Add the digit to the reversed number
            number = number / 10;               // Remove the last digit
        }

        // Step 3: Return the reversed number
        return reversedNumber;
    }
}
```

### Explanation:

1. **Edge Case Handling**: 
   - If the number is negative, we return `-1` immediately.
   - If the number is `0`, we return `0` immediately.
   
2. **Reversing Logic**:
   - We initialize `reversedNumber` to `0`.
   - We loop through the digits of the number using `number % 10` to get the last digit.
   - We then multiply the current `reversedNumber` by `10` and add the digit to it.
   - Finally, we remove the last digit from the original number by dividing it by `10`.
   
3. **Return**: 
   - After the loop, we return the `reversedNumber` containing the reversed digits.

### Test Example

Let's go through an example:

### Input: `456`
- Initial number: `456`
- First iteration: 
  - `digit = 456 % 10 = 6`
  - `reversedNumber = 0 * 10 + 6 = 6`
  - `number = 456 / 10 = 45`
- Second iteration: 
  - `digit = 45 % 10 = 5`
  - `reversedNumber = 6 * 10 + 5 = 65`
  - `number = 45 / 10 = 4`
- Third iteration:
  - `digit = 4 % 10 = 4`
  - `reversedNumber = 65 * 10 + 4 = 654`
  - `number = 4 / 10 = 0`

At this point, the number becomes `0`, so the loop terminates and we return the `reversedNumber`, which is `654`.

### Input: `5497`
- Reversed result: `7945`

### Input: `-456`
- Reversed result: `-1` (since it's negative).

### Input: `0`
- Reversed result: `0`.

### Testing the Solution

After implementing the solution, I ran several tests, including edge cases like `0`, negative numbers, and multi-digit numbers.

The solution successfully passed all test cases:
- **Input**: `1234` → **Output**: `4321`
- **Input**: `1000` → **Output**: `1`
- **Input**: `0` → **Output**: `0`
- **Input**: `-45` → **Output**: `-1`
- **Input**: `56789` → **Output**: `98765`

### Conclusion

In this exercise, we learned how to reverse a number by extracting digits one by one and constructing the reversed number. We also handled special cases for negative numbers and zero. This is a fundamental problem that demonstrates how we can manipulate digits of a number using arithmetic operations.

---

## Solution Video For Coding Exercise - LCM Of A Number

In this coding exercise, we’ll be tackling a problem where you need to calculate the **Least Common Multiple (LCM)** of two numbers. 

### Problem Overview

We are given a class `BiNumber` with two integer attributes, `number1` and `number2`. Our task is to implement a method `calculateLCM` that computes the least common multiple of `number1` and `number2`.

### Rules:
1. If **either** number is negative, the method should return `-1`.
2. If **either** number is zero, the method should return `0`.
3. Otherwise, calculate the LCM using the logic described below.

### What is LCM?

The **Least Common Multiple (LCM)** of two numbers is the smallest positive integer that is divisible by both numbers. For example:
- **LCM(6, 8)** = 24 (since 24 is divisible by both 6 and 8, and is the smallest such number).
- **LCM(5, 10)** = 10 (since 10 is divisible by both 5 and 10).

### Special Conditions:
- If **either** number is negative, return `-1`.
- If **either** number is zero, return `0`.

### Approach

### Step 1: Handle Edge Cases
We first check:
1. If either `number1` or `number2` is negative, return `-1`.
2. If either number is zero, return `0`.

### Step 2: Calculate LCM
To compute the LCM:
1. Use the formula:
   \[
   \text{LCM}(a, b) = \frac{|a \times b|}{\text{GCD}(a, b)}
   \]
   where **GCD** is the **Greatest Common Divisor**.
   
   - For example, LCM(6, 8) = \(\frac{6 \times 8}{\text{GCD}(6, 8)} = \frac{48}{2} = 24\).

### Step 3: Implement the Solution

We'll use the built-in method to find the GCD of two numbers and use it in the formula for calculating LCM.

### Code Implementation

```java
public class BiNumber {
    private int number1;
    private int number2;

    // Constructor
    public BiNumber(int number1, int number2) {
        this.number1 = number1;
        this.number2 = number2;
    }

    // Getters for number1 and number2
    public int getNumber1() {
        return number1;
    }

    public int getNumber2() {
        return number2;
    }

    // Method to calculate LCM
    public int calculateLCM() {
        // Step 1: Handle edge cases
        if (number1 < 0 || number2 < 0) {
            return -1;  // Return -1 if either number is negative
        }
        if (number1 == 0 || number2 == 0) {
            return 0;  // Return 0 if either number is zero
        }

        // Step 2: Calculate LCM using the formula
        int gcd = findGCD(number1, number2);  // Find GCD of the two numbers
        int lcm = Math.abs(number1 * number2) / gcd;  // Calculate LCM using the formula

        return lcm;  // Return the LCM
    }

    // Helper method to find the GCD (Greatest Common Divisor)
    private int findGCD(int a, int b) {
        // Use the Euclidean algorithm to find GCD
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;  // Return the GCD
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - If either number is less than zero, we return `-1`.
   - If either number is zero, we return `0`.

2. **GCD Calculation**:
   - The **Greatest Common Divisor (GCD)** is calculated using the **Euclidean algorithm**. This algorithm uses a simple loop where we replace the larger number with the remainder of the division between the two numbers until one of them becomes zero.
   
3. **LCM Calculation**:
   - Using the formula \(\text{LCM}(a, b) = \frac{|a \times b|}{\text{GCD}(a, b)}\), we compute the LCM.

4. **Return the Result**:
   - Finally, the method returns the calculated LCM.

### Test Example

### Example 1: LCM(6, 8)
- **GCD** of 6 and 8 is 2.
- **LCM** is \(\frac{6 \times 8}{2} = 24\).
- **Output**: 24.

### Example 2: LCM(5, 10)
- **GCD** of 5 and 10 is 5.
- **LCM** is \(\frac{5 \times 10}{5} = 10\).
- **Output**: 10.

### Example 3: LCM(0, 8)
- **Output**: 0 (since one of the numbers is zero).

### Example 4: LCM(-5, 10)
- **Output**: -1 (since one of the numbers is negative).

### Testing the Solution

After implementing the solution, I ran tests for a variety of inputs, including edge cases for zero and negative numbers.

All tests passed successfully:
- **Input**: `6, 8` → **Output**: `24`
- **Input**: `5, 10` → **Output**: `10`
- **Input**: `0, 8` → **Output**: `0`
- **Input**: `-5, 10` → **Output**: `-1`

### Conclusion

In this exercise, we learned how to calculate the **Least Common Multiple (LCM)** of two numbers. We used the formula involving the **Greatest Common Divisor (GCD)** to compute the LCM efficiently. Additionally, we handled special cases for negative and zero values.

---

## Solution Video For Coding Exercise - GCD of a Number

In this coding exercise, we’ll be solving the problem of finding the **Greatest Common Divisor (GCD)** of two numbers.

### Problem Overview

You are given a class `BiNumber` with two integer attributes, `number1` and `number2`. The task is to complete the method `calculateGCD` that calculates the GCD of `number1` and `number2`.

### What is GCD?

The **Greatest Common Divisor (GCD)** of two numbers is the largest number that divides both numbers without leaving a remainder.

For example:
- **GCD(48, 18)** = 6 (since 6 is the largest number that divides both 48 and 18).
- **GCD(56, 98)** = 14.

### Edge Cases:
1. If **either** number is zero, return `0`.
2. If **either** number is negative, return `1`.
3. If both numbers are equal, return `number1` or `number2`, as their GCD is the number itself.

### Approach

### Step 1: Handle Edge Cases
We first handle the following:
1. If either number is zero, return `0`.
2. If either number is negative, return `1`.
3. If both numbers are equal, return one of them, as the GCD of two equal numbers is the number itself.

### Step 2: Calculate GCD
To calculate the GCD, we can use the **Euclidean algorithm**:
1. The GCD of two numbers `a` and `b` can be found by replacing `a` with `b` and `b` with `a % b`, and repeating the process until `b` becomes zero.
2. When `b` becomes zero, `a` will hold the GCD.

### Step 3: Implement the Solution

### Code Implementation

```java
public class BiNumber {
    private int number1;
    private int number2;

    // Constructor
    public BiNumber(int number1, int number2) {
        this.number1 = number1;
        this.number2 = number2;
    }

    // Getters for number1 and number2
    public int getNumber1() {
        return number1;
    }

    public int getNumber2() {
        return number2;
    }

    // Method to calculate GCD
    public int calculateGCD() {
        // Step 1: Handle edge cases
        if (number1 == 0 || number2 == 0) {
            return 0;  // GCD with zero is zero
        }
        if (number1 < 0 || number2 < 0) {
            return 1;  // GCD for negative numbers is 1
        }
        if (number1 == number2) {
            return number1;  // GCD of equal numbers is the number itself
        }

        // Step 2: Use Euclidean algorithm to calculate GCD
        int a = number1;
        int b = number2;

        // Euclidean algorithm: keep replacing a with b, and b with a % b, until b becomes zero
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }

        return a;  // GCD is stored in a
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - If either `number1` or `number2` is zero, return `0`.
   - If either number is negative, return `1`.
   - If the two numbers are equal, return either one, as the GCD of two equal numbers is the number itself.

2. **Euclidean Algorithm**:
   - We use the **Euclidean algorithm** to efficiently compute the GCD. The process involves repeatedly replacing the larger number with the remainder of the division between the two numbers, until one of the numbers becomes zero. The GCD will be the last non-zero number.

3. **Return the Result**:
   - Finally, the method returns the computed GCD.

### Test Example

### Example 1: GCD(48, 18)
- Step-by-step:
  - \( 48 \mod 18 = 12 \)
  - \( 18 \mod 12 = 6 \)
  - \( 12 \mod 6 = 0 \)
- **GCD** is 6.

### Example 2: GCD(56, 98)
- Step-by-step:
  - \( 98 \mod 56 = 42 \)
  - \( 56 \mod 42 = 14 \)
  - \( 42 \mod 14 = 0 \)
- **GCD** is 14.

### Example 3: GCD(0, 8)
- **Output**: 0 (since one of the numbers is zero).

### Example 4: GCD(-5, 10)
- **Output**: 1 (since one of the numbers is negative).

### Testing the Solution

After implementing the solution, I ran tests for various inputs, including edge cases for zero and negative numbers.

All tests passed successfully:
- **Input**: `48, 18` → **Output**: `6`
- **Input**: `56, 98` → **Output**: `14`
- **Input**: `0, 8` → **Output**: `0`
- **Input**: `-5, 10` → **Output**: `1`

### Conclusion

In this exercise, we learned how to efficiently compute the **Greatest Common Divisor (GCD)** of two numbers using the **Euclidean algorithm**. This approach is efficient and handles edge cases such as zero and negative numbers.

---

## Section 17: Java Coding Exercises - Set 5

## Solution Video For Coding Exercise - Count Uppercase Letters in a String

Welcome to the solution for the coding exercise: **Count Uppercase Letters in a String**.

### Problem Overview

Your task is to complete a Java method called `countUppercaseLetters` in the `StringMagic` class. This method takes a string as input and returns the number of uppercase letters in that string. 

### Edge Cases:
- If the string is **empty**, the method should return `0`.
- If the string **does not contain any uppercase letters**, the method should return `0`.

### Example:
- Input: `"Hello WORld"` 
  - Uppercase letters: `H`, `W`, `O`, `R`, `L`.
  - **Output**: `5`.

### Approach

### Step 1: Handle Edge Cases
We will first check if the string is `null` to avoid any `NullPointerException`. If the string is `null`, we return `-1` as an indicator of an invalid input. 

Next, we handle an empty string. If the string is empty, we return `0` since there are no characters to check.

### Step 2: Loop Through the String
We will iterate through the string character by character and check if each character is uppercase using the `Character.isUpperCase()` method.

### Step 3: Count Uppercase Letters
For each uppercase letter we encounter, we will increment a counter. Finally, we return the count of uppercase letters.

### Code Implementation

```java
public class StringMagic {
    
    // Method to count uppercase letters in a string
    public int countUppercaseLetters(String str) {
        // Step 1: Handle null case
        if (str == null) {
            return -1;  // Return -1 for invalid input (null)
        }

        // Step 2: Initialize counter for uppercase letters
        int count = 0;

        // Step 3: Loop through the string and check for uppercase letters
        for (int i = 0; i < str.length(); i++) {
            // Get character at current index
            char currentChar = str.charAt(i);

            // Step 4: Check if the character is uppercase
            if (Character.isUpperCase(currentChar)) {
                count++;  // Increment count if the character is uppercase
            }
        }

        // Step 5: Return the total count of uppercase letters
        return count;
    }
}
```

### Explanation:
1. **Null Check**:
   - We first check if the input string is `null`. If it is, we return `-1` as an indicator of invalid input.
   
2. **Count Initialization**:
   - We initialize a counter `count` to `0` which will keep track of the number of uppercase letters found in the string.
   
3. **Loop Through the String**:
   - We loop through the string using `for (int i = 0; i < str.length(); i++)`.
   - For each character, we use `str.charAt(i)` to get the character at the current index.
   
4. **Uppercase Check**:
   - We use `Character.isUpperCase(currentChar)` to check if the character is uppercase. If it is, we increment the counter.

5. **Return the Count**:
   - Once the loop completes, we return the count of uppercase letters.

### Test Example

### Example 1: Input - "Hello WORld"
- Uppercase letters: `H`, `W`, `O`, `R`, `L`.
- **Output**: 5.

### Example 2: Input - "this is all lowercase"
- No uppercase letters.
- **Output**: 0.

### Example 3: Input - "THIS IS ALL UPPERCASE"
- Uppercase letters: `T`, `H`, `I`, `S`, `I`, `S`, `A`, `L`, `L`, `U`, `P`, `P`, `E`, `R`, `C`, `A`, `S`, `E`.
- **Output**: 18.

### Example 4: Input - ""
- An empty string.
- **Output**: 0.

### Example 5: Input - null
- Input is null.
- **Output**: -1.

### Testing the Solution

Once the implementation was complete, I ran the test cases to ensure that all edge cases and normal scenarios were handled properly. All the tests passed successfully:
- **Input**: `"Hello WORld"` → **Output**: `5`
- **Input**: `"this is all lowercase"` → **Output**: `0`
- **Input**: `"THIS IS ALL UPPERCASE"` → **Output**: `18`
- **Input**: `""` → **Output**: `0`
- **Input**: `null` → **Output**: `-1`

### Conclusion

In this exercise, we learned how to count the number of uppercase letters in a string by iterating through it and using the `Character.isUpperCase()` method to detect uppercase characters. We also ensured proper handling of edge cases such as null and empty strings.

---

## Solution Video For Coding Exercise - Does a String have Two Consecutive Characters?

We'll walk through the solution for the coding exercise: **Does a String have two consecutive identical characters?**

### Problem Overview

Your task is to implement a method called `hasConsecutiveDuplicates` in the `StringMagic` class. This method will check if the input string contains two consecutive identical characters. The method should return `true` if such a pair exists and `false` otherwise.

### Example:
- Input: `"Hello"` 
  - Output: `true` (because of the consecutive `LL`)
- Input: `"World"`
  - Output: `false`
- Input: `""` (empty string)
  - Output: `false`

### Edge Cases:
- **Empty string**: Should return `false`.
- **Single character**: Should return `false`.
- **Multiple identical consecutive characters**: Should return `true`.

### Approach

### Step 1: Handle Edge Cases
We need to make sure we account for edge cases:
- If the string is `null`, we could handle it by returning `false` or `-1` depending on the situation.
- For an **empty string** or a **single character**, it is clear that there cannot be consecutive identical characters, so we return `false`.

### Step 2: Loop Through the String
We'll iterate through the string using a loop and check pairs of characters:
- Compare the character at index `i` with the character at index `i + 1`.
- If they are identical, return `true`.
- If no such pair is found, return `false`.

### Step 3: Prevent Index Out-of-Bounds Errors
Since we're checking the character at `i + 1`, we need to ensure that our loop doesn't go past the second-last character of the string. We'll loop only from `0` to `length - 2` to avoid out-of-bounds errors.

### Code Implementation

```java
public class StringMagic {
    
    // Method to check if a string has consecutive identical characters
    public boolean hasConsecutiveDuplicates(String str) {
        // Step 1: Handle edge cases for null or very short strings
        if (str == null || str.length() < 2) {
            return false; // Cannot have consecutive characters
        }

        // Step 2: Loop through the string, comparing each character with the next
        for (int i = 0; i < str.length() - 1; i++) {
            // Get the current character and the next character
            char currentChar = str.charAt(i);
            char nextChar = str.charAt(i + 1);

            // Step 3: Check if consecutive characters are identical
            if (currentChar == nextChar) {
                return true; // Found consecutive identical characters
            }
        }

        // Step 4: If no consecutive duplicates are found, return false
        return false;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - If the string is `null` or has a length less than `2`, there can be no consecutive identical characters, so we return `false` in these cases.

2. **Looping Through the String**:
   - We loop through the string, stopping at `str.length() - 2` to compare pairs of characters (`i` and `i + 1`).
   - For each iteration, we compare the character at index `i` with the character at `i + 1`.
   
3. **Return the Result**:
   - If we find consecutive identical characters, we return `true`.
   - If the loop completes without finding any, we return `false`.

### Test Example

### Example 1: Input - `"Hello"`
- Consecutive identical characters: `"LL"`
- **Output**: `true`

### Example 2: Input - `"World"`
- No consecutive identical characters.
- **Output**: `false`

### Example 3: Input - `""` (empty string)
- **Output**: `false`

### Example 4: Input - `"A"`
- **Output**: `false`

### Example 5: Input - `"AABBC"`
- Consecutive identical characters: `"AA"` and `"BB"`.
- **Output**: `true`

### Testing the Solution

Once the implementation was done, I ran the test cases to ensure that everything was handled correctly. Here are the results:
- **Input**: `"Hello"` → **Output**: `true`
- **Input**: `"World"` → **Output**: `false`
- **Input**: `""` → **Output**: `false`
- **Input**: `"A"` → **Output**: `false`
- **Input**: `"AABBC"` → **Output**: `true`

All edge cases and normal cases were covered, and the implementation passed successfully.

### Conclusion

In this exercise, we learned how to check for consecutive identical characters in a string by looping through the string and comparing adjacent characters. We also handled edge cases like empty strings and single-character strings, where consecutive characters are impossible.

---

## Solution Video For Coding Exercise - Rightmost Digit in a String

In this video, we will solve the coding exercise **"Rightmost Digit in a String"**. Let's walk through the problem and the solution step by step.

### Problem Overview

Your task is to complete the method `getRightmostDigit` in the `StringMagic` class. This method should take a string as an argument and return the **rightmost digit** in the string. If the string contains no digits, the method should return `-1`.

### Example:

- **Input**: `"I bought 5 apples, 4 bananas, and 3 oranges"`
  - **Output**: `3` (as `3` is the rightmost digit)
  
- **Input**: `"No numbers here!"`
  - **Output**: `-1` (since there are no digits)

### Edge Cases:

- **Empty string**: Should return `-1`.
- **String without digits**: Should return `-1`.

### Tools:
We can utilize helpful methods from the `Character` class:
- `Character.isDigit(char c)`: This method checks if a character is a digit (0–9).
- `Character.getNumericValue(char c)`: This converts a digit character into its numeric value.

### Plan

1. **Edge Case Handling**: First, check if the string is `null` or empty. If it is, return `-1`.
2. **Loop Through the String**: We will scan the string **from right to left** so that the first digit we find will be the rightmost one.
3. **Check Each Character**: For each character in the string, check if it's a digit using `Character.isDigit`. Once we find the rightmost digit, return its numeric value using `Character.getNumericValue`.
4. **Return -1 if No Digits Found**: If the loop completes and no digit is found, return `-1`.

### Code Implementation

```java
public class StringMagic {
    
    public int getRightmostDigit(String str) {
        // Step 1: Handle edge cases for null or empty string
        if (str == null || str.isEmpty()) {
            return -1;  // Return -1 for null or empty strings
        }

        // Step 2: Loop through the string from right to left
        int length = str.length();
        for (int i = length - 1; i >= 0; i--) {
            char ch = str.charAt(i);  // Get the character at index i
            
            // Step 3: Check if the character is a digit
            if (Character.isDigit(ch)) {
                // Step 4: Return the numeric value of the digit
                return Character.getNumericValue(ch);
            }
        }

        // Step 5: If no digit is found, return -1
        return -1;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - We check if the string is `null` or empty and return `-1` in these cases.

2. **Looping Through the String**:
   - We start at the last index (`length - 1`) and move towards the first character (`i >= 0`).
   - For each character, we check if it is a digit using `Character.isDigit(ch)`.

3. **Return the Rightmost Digit**:
   - If we find a digit, we immediately return its numeric value using `Character.getNumericValue(ch)`.

4. **Return -1 if No Digits Found**:
   - If the loop completes and no digits are found, we return `-1`.

### Test Cases

### Example 1:
- **Input**: `"I bought 5 apples, 4 bananas, and 3 oranges"`
- **Output**: `3` (rightmost digit)

### Example 2:
- **Input**: `"No numbers here!"`
- **Output**: `-1` (no digits)

### Example 3:
- **Input**: `""` (empty string)
- **Output**: `-1` (empty string)

### Example 4:
- **Input**: `"Number is 1000"`
- **Output**: `0` (rightmost digit is `0`)

### Conclusion

This exercise helped us to practice string manipulation and working with characters in Java. We used a simple technique to loop from the rightmost character to the left, identifying and returning the rightmost digit. If no digits were found, we returned `-1`.

---

## Section 19: Java Coding Exercises - Set 6

## Solution Video For Coding Exercise - Is There a Greater Element

Welcome back! In this video, we are going to solve the coding exercise **"Is There a Greater Element?"** Let's walk through the problem and the solution step by step.

### Problem Overview

You are tasked with completing the method `doesHaveElementGreaterThan()` in the `ArrayMagic` class. This method accepts an integer array and a number as inputs. Your goal is to check whether the array contains any element that is greater than the provided number.

### Example:

- **Input**: `array = {1, 2, 3, 4, 5}`, `number = 3`
  - **Output**: `true` (since 4 and 5 are greater than 3)

- **Input**: `array = {1, 2, 3}`, `number = 4`
  - **Output**: `false` (since no element is greater than 4)

### Edge Case:

- If the array is empty, the method should return `false` because there are no elements in the array.

### Plan

1. **Edge Case Handling**: First, check if the array is empty (`length == 0`). If it is, return `false`.
2. **Loop Through the Array**: Traverse through each element in the array.
3. **Check If Any Element is Greater**: For each element, check if it is greater than the provided number. If you find such an element, return `true` immediately.
4. **Return False if No Greater Element Found**: If the loop completes and no element is greater than the number, return `false`.

### Code Implementation

```java
public class ArrayMagic {
    
    public boolean doesHaveElementGreaterThan(int[] array, int number) {
        // Step 1: Edge case - if array is empty, return false
        if (array.length == 0) {
            return false;
        }

        // Step 2: Loop through the array
        for (int value : array) {
            // Step 3: Check if any element is greater than the given number
            if (value > number) {
                return true;  // Return true immediately if found
            }
        }

        // Step 4: If no element is greater than the number, return false
        return false;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - We check if the array is empty (`array.length == 0`). If it is, we return `false` because no element exists that could be greater than the given number.

2. **Loop Through the Array**:
   - We use a **for-each** loop to iterate over each element of the array.

3. **Check If Any Element is Greater**:
   - For each element, we compare it with the given number. If we find any element that is greater, we immediately return `true`.

4. **Return False if No Greater Element is Found**:
   - If we finish looping through the entire array and find no element that is greater, we return `false`.

### Test Cases

### Example 1:
- **Input**: `array = {1, 2, 3, 4, 5}`, `number = 3`
- **Output**: `true` (since 4 and 5 are greater than 3)

### Example 2:
- **Input**: `array = {1, 2, 3}`, `number = 4`
- **Output**: `false` (since no element is greater than 4)

### Example 3:
- **Input**: `array = {}`, `number = 10` (empty array)
- **Output**: `false`

### Example 4:
- **Input**: `array = {10, 9, 8}`, `number = 9`
- **Output**: `true` (since 10 is greater than 9)

### Conclusion

This was a simple but important exercise to practice looping through arrays and using conditionals. We learned how to handle edge cases such as an empty array, and how to terminate a loop early when a condition is satisfied (i.e., when we find an element greater than the given number).

---

## Solution Video For Coding Exercise - Find Second Largest Element

In this video, we'll solve the exercise **"Find Second Largest Element"**. Let's break down the problem and walk through the solution step by step.

### Problem Overview

You're tasked with completing the method `findSecondLargestElement()` in the `ArrayMagic` class. This method accepts an integer array as input and returns the **second largest element** from the array. If there are fewer than two distinct elements in the array, the method should return `-1`.

### Example 1:

- **Input**: `array = {9, 7, 9}`
  - **Output**: `7` (The largest element is 9, but we want the second largest, which is 7)

### Example 2:

- **Input**: `array = {1, 1, 1, 1}`
  - **Output**: `-1` (All elements are the same, so there's no second largest element)

### Example 3:

- **Input**: `array = {5}`
  - **Output**: `-1` (There’s only one element, so no second largest element exists)

### Plan

1. **Edge Case Handling**: Check if the array has fewer than two elements. If it does, return `-1`.
2. **Find Largest and Second Largest**: 
   - Traverse through the array and keep track of both the largest and second largest elements.
   - If a new largest element is found, update both the largest and second largest elements.
   - If the current element is not the largest but is greater than the current second largest, update the second largest.
3. **Return Second Largest or `-1`**: If no valid second largest element is found, return `-1`.

### Code Implementation

```java
public class ArrayMagic {

    public int findSecondLargestElement(int[] array) {
        // Step 1: Edge case - if array has fewer than two elements, return -1
        if (array.length < 2) {
            return -1;
        }

        // Step 2: Initialize variables for largest and second largest elements
        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;

        // Step 3: Traverse the array
        for (int value : array) {
            // If we find a new largest element
            if (value > largest) {
                // Update second largest before largest
                secondLargest = largest;
                largest = value;
            } 
            // If the current value is not equal to the largest but greater than second largest
            else if (value > secondLargest && value != largest) {
                secondLargest = value;
            }
        }

        // Step 4: If second largest is still MIN_VALUE, it means there was no valid second largest
        return (secondLargest == Integer.MIN_VALUE) ? -1 : secondLargest;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - We check if the array has fewer than two elements (`array.length < 2`). If it does, return `-1` because it's impossible to have a second largest element.

2. **Track Largest and Second Largest**:
   - We initialize two variables, `largest` and `secondLargest`, to `Integer.MIN_VALUE`. This helps to ensure any number in the array will be larger than the initial values.
   - As we loop through the array:
     - If we encounter a number larger than the current `largest`, we update `secondLargest` to be the previous `largest`, then update `largest` to the current number.
     - If the number is not the largest but is larger than `secondLargest` and different from `largest`, we update `secondLargest`.

3. **Final Check**:
   - After the loop, if `secondLargest` is still `Integer.MIN_VALUE`, it means we did not find a valid second largest element, so we return `-1`. Otherwise, we return the value of `secondLargest`.

### Test Cases

### Example 1:
- **Input**: `array = {9, 7, 9}`
- **Output**: `7`

### Example 2:
- **Input**: `array = {1, 1, 1, 1}`
- **Output**: `-1`

### Example 3:
- **Input**: `array = {5}`
- **Output**: `-1`

### Example 4:
- **Input**: `array = {4, 6, 1, 2, 6}`
- **Output**: `4` (6 is the largest, so 4 is the second largest)

### Conclusion

This exercise involved finding the second largest element from an array, which required careful handling of edge cases and keeping track of two values simultaneously (largest and second largest). We ensured that if the array doesn’t have a second largest element, we return `-1`.

---

## Solution Video For Coding Exercise - Are Sum of Arrays Equal

In this video, we’ll be solving the exercise **"Are Sum of Arrays Equal?"**. In this task, you’re required to compare the sum of two integer arrays and determine if their sums are equal.

### Problem Overview

You are given two integer arrays, `array1` and `array2`, inside a class called `BiArray`. Your task is to implement a method that:

1. Calculates the sum of each array.
2. Compares the sums and returns `true` if they are equal, or `false` otherwise.

We also need to implement a helper method to calculate the sum of the elements in an array.

### Example 1:

- **Input**:
  - `array1 = {1, 2}`
  - `array2 = {4, -2, 1}`
- **Output**: `true` (Both arrays sum to 3)

### Example 2:

- **Input**:
  - `array1 = {5, 10, 15}`
  - `array2 = {1, 9, 20}`
- **Output**: `true` (Both arrays sum to 30)

### Example 3:

- **Input**:
  - `array1 = {-1, -1, -1}`
  - `array2 = {-2, 1}`
- **Output**: `false` (One sums to -3, the other to -1)

### Plan

1. **Helper Method**: Create a method `calculateSum()` that computes the sum of an array.
   - Initialize a `sum` variable to zero.
   - Use a **for-each loop** to iterate through each element of the array and add it to `sum`.
   - Return the final value of `sum`.
   
2. **Comparison Method**: Implement the method `areSumsEqual()`:
   - Call `calculateSum()` for both arrays.
   - Compare the sums and return `true` if they are equal, otherwise return `false`.

### Code Implementation

```java
public class BiArray {

    // Method to calculate the sum of elements in an array
    public int calculateSum(int[] array) {
        int sum = 0;  // Initialize sum to zero
        
        // Use an enhanced for loop to sum all elements in the array
        for (int element : array) {
            sum += element;  // Add each element to sum
        }
        
        return sum;  // Return the calculated sum
    }

    // Method to compare sums of two arrays and check if they are equal
    public boolean areSumsEqual(int[] array1, int[] array2) {
        // Calculate the sum of both arrays using calculateSum()
        int sum1 = calculateSum(array1);
        int sum2 = calculateSum(array2);
        
        // Return true if the sums are equal, otherwise return false
        return sum1 == sum2;
    }
}
```

### Explanation:

1. **`calculateSum()` Method**:
   - We initialize `sum` to zero.
   - We loop through each element of the array, adding it to `sum`.
   - After processing all elements, we return the value of `sum`.

2. **`areSumsEqual()` Method**:
   - We call `calculateSum()` for both `array1` and `array2` to get their sums.
   - We compare the two sums using `==` (equality operator).
   - If the sums are equal, we return `true`. Otherwise, we return `false`.

### Test Cases

### Example 1:
- **Input**: `array1 = {1, 2}`, `array2 = {4, -2, 1}`
- **Output**: `true` (Both arrays sum to 3)

### Example 2:
- **Input**: `array1 = {5, 10, 15}`, `array2 = {1, 9, 20}`
- **Output**: `true` (Both arrays sum to 30)

### Example 3:
- **Input**: `array1 = {-1, -1, -1}`, `array2 = {-2, 1}`
- **Output**: `false` (Sums are -3 and -1, respectively)

### Conclusion

In this exercise, we successfully implemented a method to compare the sum of two arrays. By breaking down the problem into smaller pieces, we were able to:
- Create a helper method `calculateSum()` that focuses solely on calculating the sum of an array.
- Implement the `areSumsEqual()` method to compare the two sums and return whether they are equal.

This approach ensures clean, readable code with well-defined responsibilities for each method.

---

## Solution Video For Coding Exercise - Check if an Array is Sorted

In this exercise, we’re going to solve the problem **“Check if an Array is Sorted.”** 

### Problem Overview

You are given an incomplete Java method called `isSorted` inside a class called `ArrayMagic`. The method takes an array of integers as input and should return `true` if the array is sorted in ascending order, or `false` if it is not.

### Example:

- **Input**: `[1, 2, 3, 4]`
  - **Output**: `true` (Array is sorted in ascending order)
  
- **Input**: `[5, 4, 3, 2, 1]`
  - **Output**: `false` (Array is sorted in descending order, not ascending)

### Edge Cases:
- An empty array or an array with only one element is considered sorted, so the method should return `true` in those cases.
- The array may contain negative numbers, zero, or duplicate elements.

### Plan

We’ll break the problem down into the following steps:

1. **Edge Case**:
   - If the array length is 0 or 1, it’s already sorted. We return `true` immediately in these cases.

2. **Loop through the Array**:
   - For each element, compare it to the next element.
   - If at any point, the next element is smaller than the current one, return `false` because the array is not sorted in ascending order.
   - If we loop through all elements and don’t find any violations, return `true` since the array is sorted.

### Code Implementation

```java
public class ArrayMagic {

    // Method to check if the array is sorted in ascending order
    public boolean isSorted(int[] array) {
        // Edge case: If the array has 0 or 1 element, it's considered sorted
        if (array.length <= 1) {
            return true;
        }

        // Loop through the array from the start to the second last element
        for (int i = 0; i < array.length - 1; i++) {
            // If the current element is greater than the next element, return false
            if (array[i] > array[i + 1]) {
                return false;
            }
        }

        // If we get through the entire array without finding a problem, it's sorted
        return true;
    }
}
```

### Explanation:

1. **Edge Case**:
   - If the array is empty or has just one element, it is trivially sorted. So, we return `true` for arrays with length 0 or 1.

2. **Loop through the Array**:
   - We use a traditional `for` loop starting from the first element to the second-to-last element (`array.length - 1`).
   - At each iteration, we compare the current element (`array[i]`) with the next element (`array[i + 1]`).
   - If we find any element where the next element is smaller than the current element, we return `false`.
   - If no such pair is found, we return `true` at the end.

### Test Cases

### Example 1:
- **Input**: `[1, 2, 3, 4]`
  - **Output**: `true` (Array is sorted)

### Example 2:
- **Input**: `[5, 4, 3, 2, 1]`
  - **Output**: `false` (Array is sorted in descending order)

### Example 3:
- **Input**: `[1, 3, 2, 4]`
  - **Output**: `false` (Array is not sorted)

### Example 4:
- **Input**: `[-1, 0, 1, 2]`
  - **Output**: `true` (Array with negative and positive numbers is sorted)

### Example 5:
- **Input**: `[]` (Empty array)
  - **Output**: `true` (Empty array is considered sorted)

### Conclusion

In this solution, we efficiently check if an array is sorted by comparing each element with its next neighbor. If any element is found to be greater than the next, we know the array is not sorted, and we can return `false` immediately. If we get through all the comparisons without issues, we return `true`.

---

## Solution Video For Coding Exercise - Reverse an Array

In this coding exercise, we’ll be solving the problem **“Reverse an Array.”** 

### Problem Overview

You are required to complete a method called `reversedArray` inside a class `ArrayMagic`. This method takes an array as input and returns a new array where the elements are in reverse order.

### Example:

- **Input**: `[1, 2, 3, 4]`
  - **Output**: `[4, 3, 2, 1]`

- **Input**: `[5, -10, 15, -20]`
  - **Output**: `[-20, 15, -10, 5]`

### Edge Cases:
- If the input array is empty, return an empty array.
- If the input array contains one element, return that array as is (since it is already reversed).

### Plan

We’ll implement the solution by using the following steps:

1. **Edge Cases**:
   - If the array is empty or contains only one element, return the array as is.

2. **Two-Pointer Approach**:
   - We’ll use two pointers: one starting at the beginning of the array (`start`) and one at the end of the array (`end`).
   - Swap the elements at the `start` and `end` positions.
   - Increment the `start` pointer and decrement the `end` pointer, and continue swapping until `start` is greater than or equal to `end`.

### Code Implementation

```java
public class ArrayMagic {

    // Method to reverse the array
    public int[] reversedArray(int[] array) {
        // Edge case: if the array is empty or has one element, return it as is
        if (array.length <= 1) {
            return array;
        }

        // Two pointers for the start and end of the array
        int start = 0;
        int end = array.length - 1;
        
        // Create a new array to hold the reversed elements
        int[] reversedArray = new int[array.length];

        // Loop through the array, swapping elements from the start and end
        while (start <= end) {
            // Swap the elements at start and end
            reversedArray[start] = array[end];
            reversedArray[end] = array[start];
            // Move the pointers
            start++;
            end--;
        }

        // Return the reversed array
        return reversedArray;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - If the array has a length of `0` or `1`, we directly return the input array because it is either empty or already reversed.

2. **Two-Pointer Technique**:
   - We initialize two pointers: `start` at the beginning (`0`) and `end` at the last index (`array.length - 1`).
   - In each iteration, we swap the elements at these positions and then move the `start` pointer to the right and the `end` pointer to the left.
   - We stop when `start` exceeds `end`, which means the entire array has been reversed.

3. **Swapping Elements**:
   - As we go through the array, the first element is swapped with the last, the second element with the second-last, and so on, until the array is fully reversed.

### Test Cases

### Example 1:
- **Input**: `[1, 2, 3, 4]`
  - **Output**: `[4, 3, 2, 1]`

### Example 2:
- **Input**: `[5, -10, 15, -20]`
  - **Output**: `[-20, 15, -10, 5]`

### Example 3:
- **Input**: `[]` (Empty array)
  - **Output**: `[]` (Empty array)

### Example 4:
- **Input**: `[10]`
  - **Output**: `[10]` (Single element remains unchanged)

### Conclusion

In this solution, we used the two-pointer technique to reverse an array efficiently. By swapping the elements from both ends and moving towards the center, we can reverse the array in `O(n)` time complexity where `n` is the length of the array.

---

## Solution Video For Coding Exercise - Return Factors Of A Number in an ArrayList

In this exercise, we’ll tackle the problem of **finding factors of a number** and returning them in an `ArrayList`.

### Problem Overview

You are tasked with completing a Java method that returns all the factors of a given integer in an `ArrayList`. The method is part of a class named `NumberMagic`. The factors of a number are defined as the numbers that divide the given number without leaving a remainder. The output must include both 1 and the number itself.

### Example:
- **Input**: `6`
  - **Output**: `[1, 2, 3, 6]`
  
- **Input**: `12`
  - **Output**: `[1, 2, 3, 4, 6, 12]`
  
- **Input**: `15`
  - **Output**: `[1, 3, 5, 15]`

### Edge Cases:
- If the input number is `0` or negative, return an empty list.

### Plan

Here’s the step-by-step breakdown of the approach:

1. **Edge Case Handling**:
   - If the input number is `0` or less, return an empty `ArrayList` because factors do not apply in these cases.

2. **Finding Factors**:
   - Loop through all numbers starting from `1` up to the input number.
   - Check if the current number divides the input number perfectly (i.e., no remainder).
   - If it does, add it to the `ArrayList`.

3. **Return Result**:
   - After the loop, return the `ArrayList` containing all factors.

### Code Implementation

```java
import java.util.ArrayList;
import java.util.List;

public class NumberMagic {

    // Method to return the factors of a number
    public List<Integer> determineFactors(int number) {
        // Edge case: if the number is less than or equal to zero, return an empty list
        List<Integer> factors = new ArrayList<>();
        if (number <= 0) {
            return factors;
        }

        // Loop from 1 to the number itself to find all factors
        for (int i = 1; i <= number; i++) {
            // If the number is divisible by i, it's a factor
            if (number % i == 0) {
                factors.add(i);
            }
        }

        // Return the list of factors
        return factors;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - We first check if the input number is less than or equal to zero. If true, we return an empty `ArrayList` as there are no valid factors for such numbers.

2. **Finding Factors**:
   - We use a `for` loop to iterate from `1` up to the input number.
   - For each iteration, we check if the number is divisible by the current value of `i` (i.e., `number % i == 0`).
   - If it divides evenly, we add `i` to the `factors` list.

3. **Returning the List**:
   - After collecting all factors, we return the `factors` list.

### Test Cases

### Example 1:
- **Input**: `6`
  - **Output**: `[1, 2, 3, 6]`
  - **Explanation**: The factors of 6 are 1, 2, 3, and 6.

### Example 2:
- **Input**: `12`
  - **Output**: `[1, 2, 3, 4, 6, 12]`
  - **Explanation**: The factors of 12 are 1, 2, 3, 4, 6, and 12.

### Example 3:
- **Input**: `0`
  - **Output**: `[]`
  - **Explanation**: Since 0 has no factors, we return an empty list.

### Example 4:
- **Input**: `-5`
  - **Output**: `[]`
  - **Explanation**: Negative numbers do not have factors, so an empty list is returned.

### Example 5:
- **Input**: `15`
  - **Output**: `[1, 3, 5, 15]`
  - **Explanation**: The factors of 15 are 1, 3, 5, and 15.

### Conclusion

In this solution, we implemented a method to find the factors of a number and return them in an `ArrayList`. By checking for edge cases and iterating through potential factors, we can efficiently solve this problem.

---

## Solution Video For Coding Exercise - Return ArrayList with Multiples of a Number

In this exercise, we’ll solve the problem of returning an `ArrayList` containing multiples of a given number up to a specified limit.

### Problem Overview

You are tasked with completing a method named `determineMultiples` inside the `NumberMagic` class. This method takes two inputs: 
1. `number` - the number whose multiples you want to find.
2. `limit` - the upper bound, meaning the multiples should be less than this value.

The goal is to return a list of multiples of the given number that are less than the limit.

### Examples:
- **Input**: `number = 3`, `limit = 20`
  - **Output**: `[3, 6, 9, 12, 15, 18]`
  
- **Input**: `number = 5`, `limit = 1`
  - **Output**: `[]` (No multiples of 5 are less than 1)

### Edge Cases:
- If either the number or the limit is less than or equal to `0`, return an empty list.
- The multiples list should include all multiples of the number, but they must be less than the given limit.

### Plan

Here’s the breakdown of the approach:

1. **Edge Case Handling**:
   - If the `number` or `limit` is less than or equal to `0`, return an empty `ArrayList` since no valid multiples exist.

2. **Generating Multiples**:
   - Start from `1` and generate multiples of the `number` by multiplying it with a counter (`i`).
   - Keep adding these multiples to the list until the multiple exceeds the `limit`.

3. **Return Result**:
   - Once all valid multiples are generated, return the `ArrayList`.

### Code Implementation

```java
import java.util.ArrayList;
import java.util.List;

public class NumberMagic {

    // Method to return the multiples of a number less than a limit
    public List<Integer> determineMultiples(int number, int limit) {
        // Create an empty list to store the multiples
        List<Integer> multiples = new ArrayList<>();
        
        // Edge case: if the number or limit is less than or equal to 0, return an empty list
        if (number <= 0 || limit <= 0) {
            return multiples;
        }
        
        // Loop to generate multiples of the number
        for (int i = 1; number * i < limit; i++) {
            multiples.add(number * i);  // Add each valid multiple to the list
        }
        
        // Return the list of multiples
        return multiples;
    }
}
```

### Explanation:

1. **Edge Case Handling**:
   - If either the `number` or `limit` is less than or equal to `0`, we return an empty `ArrayList` because no valid multiples exist in such cases.

2. **Generating Multiples**:
   - We use a `for` loop where `i` starts at `1` and increments by `1` on each iteration. We multiply `number * i` and check if the result is less than the `limit`.
   - If the product is less than the `limit`, we add it to the `multiples` list.
   - The loop continues until the product exceeds the `limit`.

3. **Returning the List**:
   - After generating all valid multiples, the `multiples` list is returned.

### Test Cases

### Example 1:
- **Input**: `number = 3`, `limit = 20`
  - **Output**: `[3, 6, 9, 12, 15, 18]`
  - **Explanation**: The multiples of 3 that are less than 20 are 3, 6, 9, 12, 15, and 18.

### Example 2:
- **Input**: `number = 5`, `limit = 1`
  - **Output**: `[]`
  - **Explanation**: There are no multiples of 5 that are less than 1.

### Example 3:
- **Input**: `number = 7`, `limit = 50`
  - **Output**: `[7, 14, 21, 28, 35, 42, 49]`
  - **Explanation**: The multiples of 7 less than 50 are 7, 14, 21, 28, 35, 42, and 49.

### Example 4:
- **Input**: `number = 10`, `limit = 100`
  - **Output**: `[10, 20, 30, 40, 50, 60, 70, 80, 90]`
  - **Explanation**: The multiples of 10 less than 100 are 10, 20, 30, 40, 50, 60, 70, 80, and 90.

### Example 5:
- **Input**: `number = -3`, `limit = 20`
  - **Output**: `[]`
  - **Explanation**: Since the number is negative, the output is an empty list.

### Conclusion

In this solution, we implemented a method that finds multiples of a number up to a given limit and returns them in an `ArrayList`. We handled edge cases like negative numbers and limits, and ensured that the correct multiples were included in the output list. 

---

## Section 21: Java Coding Exercises - Set 7

## Solution Video For Coding Exercise - Arithmetic Operations

In this exercise, we’ll solve a simple problem that involves performing basic arithmetic operations using interfaces in Java. The goal is to implement addition, subtraction, and division operations using the `Operation` interface.

### Problem Overview

You are provided with an `Operation` interface that contains a method `perform(int x, int y)`, and your task is to create classes that implement this interface for the following operations:
1. **Addition**: Add two numbers and return the result.
2. **Subtraction**: Subtract the second number from the first and return the result.
3. **Division**: Divide the first number by the second, but handle the edge case where division by zero occurs. If the second number (`y`) is zero, return `-1`.

### Edge Case:
- For the division operation, you need to check if the divisor (`y`) is zero. If it is, return `-1` instead of throwing an exception.

### Approach

1. **Operation Interface**:
   - The `Operation` interface has an abstract method `perform(int x, int y)`. This will be implemented by the `Add`, `Subtract`, and `Divide` classes.

2. **Add Class**:
   - This class will implement the `perform` method and return the sum of `x` and `y`.

3. **Subtract Class**:
   - This class will implement the `perform` method and return the result of `x - y`.

4. **Divide Class**:
   - This class will implement the `perform` method. It will check if `y` is zero. If `y` is zero, return `-1`; otherwise, return `x / y`.

### Code Implementation

```java
// Define the Operation interface
interface Operation {
    // Abstract method to perform the operation
    int perform(int x, int y);
}

// Implement the Add class
class Add implements Operation {
    // Implement the perform method to add two numbers
    public int perform(int x, int y) {
        return x + y;
    }
}

// Implement the Subtract class
class Subtract implements Operation {
    // Implement the perform method to subtract two numbers
    public int perform(int x, int y) {
        return x - y;
    }
}

// Implement the Divide class
class Divide implements Operation {
    // Implement the perform method to divide two numbers
    // Handle the edge case of division by zero
    public int perform(int x, int y) {
        if (y == 0) {
            return -1;  // Return -1 if trying to divide by zero
        }
        return x / y;
    }
}
```

### Explanation:

1. **Operation Interface**:
   - The `Operation` interface defines an abstract method `perform(int x, int y)` that each operation class must implement.

2. **Add Class**:
   - This class implements the `Operation` interface and provides a concrete implementation for the `perform` method, which simply adds `x` and `y`.

3. **Subtract Class**:
   - This class also implements the `Operation` interface and provides the subtraction logic in the `perform` method.

4. **Divide Class**:
   - In this class, before performing the division, we check if the divisor `y` is zero. If it is, we return `-1` to handle division by zero. Otherwise, we return the result of `x / y`.

### Example Walkthrough:

1. **Addition Example**:
   - **Input**: `Add.perform(5, 3)`
   - **Output**: `8`
   - **Explanation**: The `Add` class's `perform` method simply returns `5 + 3`, which is `8`.

2. **Subtraction Example**:
   - **Input**: `Subtract.perform(10, 4)`
   - **Output**: `6`
   - **Explanation**: The `Subtract` class's `perform` method returns `10 - 4`, which is `6`.

3. **Division Example**:
   - **Input**: `Divide.perform(10, 2)`
   - **Output**: `5`
   - **Explanation**: The `Divide` class checks if `y` is zero (it isn’t), so it performs the division `10 / 2` and returns `5`.

4. **Division by Zero Example**:
   - **Input**: `Divide.perform(10, 0)`
   - **Output**: `-1`
   - **Explanation**: Since `y` is `0`, the `Divide` class returns `-1` to handle the division by zero case.

### Test Cases

### Example 1: Addition
- **Input**: `Add.perform(7, 5)`
  - **Output**: `12`
  - **Explanation**: Adds `7 + 5`.

### Example 2: Subtraction
- **Input**: `Subtract.perform(15, 8)`
  - **Output**: `7`
  - **Explanation**: Subtracts `15 - 8`.

### Example 3: Division
- **Input**: `Divide.perform(20, 5)`
  - **Output**: `4`
  - **Explanation**: Divides `20 / 5`.

### Example 4: Division by Zero
- **Input**: `Divide.perform(10, 0)`
  - **Output**: `-1`
  - **Explanation**: Handles division by zero by returning `-1`.

### Conclusion

In this exercise, we implemented three basic arithmetic operations: addition, subtraction, and division using an interface in Java. The division operation had an edge case where we handled division by zero by returning `-1`. This is a simple demonstration of how interfaces can be used to create flexible, reusable code for different mathematical operations.

---

## Solution Video For Coding Exercise - Shapes and Area

In this coding exercise, we will explore abstract classes and inheritance in Java. Specifically, we are tasked with creating subclasses for different shapes and implementing methods to calculate their area.

### Problem Overview

You are provided with an abstract class `Shape` that includes an abstract method `calculateArea()`. Your task is to create two subclasses, `Circle` and `Rectangle`, that extend `Shape`. Each subclass must implement the `calculateArea()` method to compute the area for that specific shape. The shapes must calculate their areas as follows:
- **Circle**: The area is calculated using the formula: \( \pi \times r^2 \), where `r` is the radius of the circle.
- **Rectangle**: The area is calculated using the formula: \( \text{length} \times \text{width} \).

### Key Requirements:
1. **Circle Class**:
   - A `Circle` must have a private `radius` attribute.
   - It must implement the `calculateArea()` method, which uses the formula \( \pi \times r^2 \).
2. **Rectangle Class**:
   - A `Rectangle` must have `length` and `width` attributes.
   - It must implement the `calculateArea()` method using the formula \( \text{length} \times \text{width} \).
3. **Edge Cases**:
   - The values for the radius, length, and width are always positive. You don’t need to handle negative or zero values.

### Steps to Implement

### 1. Abstract Class `Shape`
The `Shape` class is abstract, and it has an abstract method `calculateArea()` that each subclass must implement.

```java
abstract class Shape {
    private String name;
    
    public Shape(String name) {
        this.name = name;
    }
    
    public String getName() {
        return name;
    }
    
    public abstract double calculateArea();
}
```

### 2. Circle Class
The `Circle` class extends `Shape` and implements the `calculateArea()` method using the formula \( \pi \times r^2 \).

```java
class Circle extends Shape {
    private double radius;
    
    public Circle(String name, double radius) {
        super(name);  // Call the superclass constructor to set the name
        this.radius = radius;
    }
    
    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
    
    public double getRadius() {
        return radius;
    }
}
```

- **Constructor**: The constructor takes a `name` and a `radius`, setting the name using the superclass's constructor (`super()`).
- **calculateArea()**: The area is calculated using \( \pi \times r^2 \) and returned.

### 3. Rectangle Class
The `Rectangle` class extends `Shape` and implements the `calculateArea()` method using the formula \( \text{length} \times \text{width} \).

```java
class Rectangle extends Shape {
    private double length;
    private double width;
    
    public Rectangle(String name, double length, double width) {
        super(name);  // Call the superclass constructor to set the name
        this.length = length;
        this.width = width;
    }
    
    @Override
    public double calculateArea() {
        return length * width;
    }
    
    public double getLength() {
        return length;
    }
    
    public double getWidth() {
        return width;
    }
}
```

- **Constructor**: The constructor accepts a `name`, `length`, and `width`, and initializes these values.
- **calculateArea()**: The area is calculated using \( \text{length} \times \text{width} \).

### Test Cases

### Example 1: Circle
- **Input**: `Circle("Circle A", 5)`
- **Expected Output**: Area is \( \pi \times 5^2 = 78.54 \)

### Example 2: Rectangle
- **Input**: `Rectangle("Rectangle A", 10, 5)`
- **Expected Output**: Area is \( 10 \times 5 = 50 \)

### Example 3: Circle with Large Radius
- **Input**: `Circle("Circle B", 10)`
- **Expected Output**: Area is \( \pi \times 10^2 = 314.16 \)

### Example 4: Rectangle with Equal Length and Width
- **Input**: `Rectangle("Square A", 5, 5)`
- **Expected Output**: Area is \( 5 \times 5 = 25 \)

### Conclusion

In this exercise, we used abstract classes and inheritance to create specific shape classes like `Circle` and `Rectangle`. By extending the abstract `Shape` class, we were able to provide concrete implementations of the `calculateArea()` method for each shape. This approach allows us to define common behavior in the abstract class while delegating the implementation details to each subclass.

---

## Section 23: Java Coding Exercises - Set 8

## Solution Video For Coding Exercise - Anagram Checker

In this exercise, we are tasked with determining whether two strings are anagrams of each other. Let's dive into the details of how we solve this problem.

### Problem Overview

You are given two strings, `str1` and `str2`. Your task is to determine if these two strings are anagrams. 

### What is an Anagram?

An anagram is a word or phrase formed by rearranging the letters of another word or phrase, using all the original letters exactly once. For example:
- "listen" is an anagram of "silent"
- "hello" is an anagram of "olelh"

### Requirements:
1. The method should return **true** if `str1` and `str2` are anagrams.
2. The comparison should be **case insensitive**.
3. If either `str1` or `str2` is **null**, the method should return **false**.
4. If the lengths of the two strings are not the same, the method should return **false**.

### Steps to Implement

### 1. Edge Case Handling
We need to handle some edge cases upfront:
- If either `str1` or `str2` is **null**, return **false**.
- If the lengths of the two strings are not equal, return **false**.

```java
if (str1 == null || str2 == null) {
    return false;
}

if (str1.length() != str2.length()) {
    return false;
}
```

### 2. Convert Strings to Lowercase
Since we need to ignore the case, we should convert both strings to lowercase before further processing. This ensures that case differences do not affect the anagram comparison.

```java
String lowercaseStr1 = str1.toLowerCase();
String lowercaseStr2 = str2.toLowerCase();
```

### 3. Convert Strings to Character Arrays
Once the strings are converted to lowercase, the next step is to break them down into character arrays. This allows us to manipulate and compare the characters easily.

```java
char[] charArray1 = lowercaseStr1.toCharArray();
char[] charArray2 = lowercaseStr2.toCharArray();
```

### 4. Sort the Character Arrays
We can now sort both character arrays. If two strings are anagrams, sorting their characters will result in identical arrays.

```java
Arrays.sort(charArray1);
Arrays.sort(charArray2);
```

### 5. Compare the Sorted Arrays
Finally, we use `Arrays.equals()` to compare the two sorted arrays. If they are equal, the strings are anagrams.

```java
return Arrays.equals(charArray1, charArray2);
```

### Complete Solution

Here is the complete implementation of the `areAnagrams` method:

```java
public boolean areAnagrams(String str1, String str2) {
    // Step 1: Handle null values and unequal lengths
    if (str1 == null || str2 == null) {
        return false;
    }

    if (str1.length() != str2.length()) {
        return false;
    }

    // Step 2: Convert both strings to lowercase
    String lowercaseStr1 = str1.toLowerCase();
    String lowercaseStr2 = str2.toLowerCase();

    // Step 3: Convert strings to character arrays
    char[] charArray1 = lowercaseStr1.toCharArray();
    char[] charArray2 = lowercaseStr2.toCharArray();

    // Step 4: Sort the character arrays
    Arrays.sort(charArray1);
    Arrays.sort(charArray2);

    // Step 5: Compare the sorted arrays
    return Arrays.equals(charArray1, charArray2);
}
```

### 6. Run Tests

Let's run the tests to ensure everything is working as expected. The solution should pass various test cases, including:
- Anagrams with different letter cases.
- Anagrams with single characters.
- Strings of different lengths (which should return **false**).
- Null inputs (which should return **false**).

When we run the tests, the solution should pass all of them successfully!

### Conclusion

In this exercise, we implemented a simple and efficient approach to check if two strings are anagrams by:
1. Handling edge cases (null values and unequal lengths).
2. Converting strings to lowercase for case-insensitive comparison.
3. Sorting the characters of both strings.
4. Comparing the sorted arrays to determine if the strings are anagrams.

This approach efficiently solves the problem while being easy to understand and maintain.

---

## Solution Video For Coding Exercise - Is Hexadecimal String?

In this exercise, we will check whether a given string is a valid hexadecimal string. Let’s go through the steps needed to implement this.

### Problem Overview

You are given a class `MyString` with a string variable `str` and two methods: `isHexadecimalChar` and `isHexadecimal`. You need to complete these two methods to check if a character or a string is a valid hexadecimal.

### What is a Hexadecimal String?
A string is considered a valid hexadecimal if it contains:
- Digits **0-9**.
- Letters **A-F** (uppercase or lowercase).

So, the string can have both uppercase and lowercase characters, but no characters outside this range are allowed. For example:
- **"123F"** is a valid hexadecimal string.
- **"1G2H"** is **not** a valid hexadecimal string because it contains letters outside the A-F range.

### Task Breakdown

1. **isHexadecimalChar(char ch)**: This method should return true if the character is a valid hexadecimal character (`0-9`, `a-f`, `A-F`).
2. **isHexadecimal(String str)**: This method should return true if the entire string is a valid hexadecimal string, false otherwise.

### Step-by-Step Solution

### 1. Implementing `isHexadecimalChar`
The goal of this method is to check if a given character is either a digit or a valid hexadecimal letter (A-F or a-f).

```java
public boolean isHexadecimalChar(char ch) {
    return (ch >= 'a' && ch <= 'f') || (ch >= 'A' && ch <= 'F');
}
```

Here, we check if the character falls between 'a' and 'f' (lowercase) or 'A' and 'F' (uppercase). If it does, it’s a valid hexadecimal letter.

### 2. Implementing `isHexadecimal`
In this method, we need to check whether the entire string is composed of valid hexadecimal characters.

#### Step-by-step plan:
- Handle edge cases: If the string is null or empty, return false.
- Convert the string to a character array and iterate through each character.
- For each character, check if it is either a digit or a valid hexadecimal letter using `Character.isDigit` and `isHexadecimalChar`.
- If we encounter an invalid character, return false.
- If all characters are valid, return true.

```java
public boolean isHexadecimal(String str) {
    // Edge case: check for null or empty string
    if (str == null || str.equals("")) {
        return false;
    }

    // Loop through the characters of the string
    for (char ch : str.toCharArray()) {
        // Check if it's neither a hexadecimal char nor a digit
        if (!isHexadecimalChar(ch) && !Character.isDigit(ch)) {
            return false;  // Invalid character found
        }
    }

    return true;  // All characters are valid
}
```

### Detailed Explanation:

1. **Edge Case Handling**: 
   - We first check if the string is null or empty. If it is, the string is not valid, so we return false.
   
2. **Iterate through the Characters**:
   - We convert the string into a character array using `str.toCharArray()` and then use a `for-each` loop to iterate through each character.

3. **Character Validation**:
   - For each character, we check if it’s a valid hexadecimal character using `isHexadecimalChar`.
   - We also check if the character is a digit using `Character.isDigit(ch)`.

4. **Return the Result**:
   - If any character is not a valid hexadecimal character or digit, we return false.
   - If the loop completes without finding any invalid characters, we return true.

### Full Code Solution:

```java
public class MyString {
    public boolean isHexadecimalChar(char ch) {
        return (ch >= 'a' && ch <= 'f') || (ch >= 'A' && ch <= 'F');
    }

    public boolean isHexadecimal(String str) {
        // Edge case: null or empty string
        if (str == null || str.equals("")) {
            return false;
        }

        // Check each character
        for (char ch : str.toCharArray()) {
            if (!isHexadecimalChar(ch) && !Character.isDigit(ch)) {
                return false;  // Invalid character found
            }
        }

        return true;  // All characters are valid
    }
}
```

### 3. Run Tests
Let’s now run the tests and ensure that everything works as expected. The solution should pass various test cases, including:
- Valid hexadecimal strings with uppercase and lowercase letters.
- Strings with invalid characters.
- Edge cases like null and empty strings.

When we run the tests, all 16 test cases should pass successfully!

### Conclusion

In this exercise, we implemented a method to check whether a string is a valid hexadecimal string by:
1. Handling edge cases (null and empty strings).
2. Using `isHexadecimalChar` to check if each character is a valid hexadecimal character.
3. Using a loop to iterate through each character in the string and validate it.

This solution is simple and efficient.

---

## Solution Video For Coding Exercise - Word Reverser

In this exercise, we are going to reverse the individual words in a sentence while maintaining the original order of the words. Let’s go step-by-step through the solution.

### Problem Overview

You need to write a method called `reverseWords` inside a `StringMagic` class. This method will take a sentence as input and return a string in which each word in the sentence is reversed, but the order of the words remains the same.

### Example:
- Input: `"Hello world"`
- Output: `"olleH dlrow"`

So, in this example:
- The word "Hello" is reversed to "olleH."
- The word "world" is reversed to "dlrow."
- The order of the words remains the same.

### Edge Conditions:
- If the input is null, return `"Invalid"`.
- If the input is an empty string, return an empty string.

### Step-by-Step Solution

### 1. Handle Edge Cases

The first step is to handle the edge cases where the input string is either `null` or empty:
- If the input is `null`, return `"Invalid"`.
- If the input is an empty string, return an empty string.

### 2. Split the Sentence into Words

To reverse each word, we need to split the sentence into individual words. We can use the `split()` method in Java with space (`" "`) as the delimiter.

### 3. Reverse Each Word

Once we have each word, we reverse it using `StringBuilder`. The `StringBuilder` class in Java has a built-in method `reverse()` that can reverse the sequence of characters in a string.

### 4. Construct the Final Result

After reversing each word, append it to a `StringBuilder` and add a space between words. At the end, you may have an extra space, which you can remove using the `trim()` method.

### Full Code Solution

```java
public class StringMagic {

    public String reverseWords(String sentence) {
        // Step 1: Handle edge cases for null and empty string
        if (sentence == null) {
            return "Invalid";
        }
        if (sentence.equals("")) {
            return "";
        }

        // Step 2: Split the sentence into words
        String[] words = sentence.split(" ");
        StringBuilder reversedSentence = new StringBuilder();

        // Step 3: Reverse each word and append it to the result
        for (String word : words) {
            StringBuilder reversedWord = new StringBuilder(word).reverse();
            reversedSentence.append(reversedWord).append(" ");
        }

        // Step 4: Return the reversed sentence, trimming the extra space at the end
        return reversedSentence.toString().trim();
    }
}
```

### Explanation:

1. **Handling Edge Cases**:
   - We check if the sentence is `null`, and if so, we return `"Invalid"`.
   - If the sentence is an empty string, we return an empty string directly.

2. **Splitting the Sentence**:
   - We use `split(" ")` to split the sentence into words based on spaces. This creates an array of words.

3. **Reversing Each Word**:
   - We loop through each word in the array, reverse it using `StringBuilder.reverse()`, and append the reversed word to `reversedSentence`.

4. **Trimming the Result**:
   - Since we add a space after each word, the last word will also have a trailing space. We use `trim()` to remove the extra space at the end.

### Running the Tests

Now let’s run the tests and verify the output:
- For input `"Hello world"`, the output will be `"olleH dlrow"`.
- For input `"Java is fun"`, the output will be `"avaJ si nuf"`.
- For null input, it will return `"Invalid"`.
- For an empty string, it will return an empty string.

All tests should pass successfully!

### Conclusion

In this exercise, we implemented a method to reverse the individual words of a sentence while keeping the word order intact. We used:
1. String splitting to break the sentence into words.
2. StringBuilder to reverse the characters of each word.
3. Proper handling of edge cases like null and empty strings.

This approach is both simple and efficient.

---

## Section 26: Java Coding Exercises - Set 9

## Solution Video For Coding Exercise - Filter Odd Numbers

In this coding exercise, we will use functional programming in Java to filter out odd numbers from a list of integers. Let's dive into the details of this exercise and see how we can implement it using the **Java Stream API**.

### Problem Overview

You are given a list of integers, and your task is to filter out **only the odd numbers** from this list using the Java Stream API. The order of the numbers in the output list should be the same as the order in the input list.

### Input:
- A list of integers that may contain positive, negative, and zero values.
- The list may also be empty.

### Output:
- A list of integers containing only odd numbers from the input list, in the same order.

### Example:
1. **Input:** `[1, 2, 3, 4, 5]`  
   **Output:** `[1, 3, 5]`

2. **Input:** `[6, 7, 8, 9, 10]`  
   **Output:** `[7, 9]`

3. **Input:** `[-3, -2, -1, 0, 1, 2, 3]`  
   **Output:** `[-3, -1, 1, 3]`

### Approach

We will make use of the **Java Stream API** to solve this problem. The steps are as follows:
1. Convert the input list into a stream.
2. Use a **filter** to keep only the odd numbers.
3. Collect the filtered numbers back into a list.

### Edge Cases:
- If the input list is empty, return an empty list.
- Handle negative numbers and zero appropriately.

### Step-by-Step Implementation

### Step 1: Convert the List to a Stream
We start by converting the list of numbers into a stream using the `.stream()` method.

### Step 2: Filter Odd Numbers
We use the `.filter()` method with a lambda expression to filter out only the odd numbers. We check if a number is odd using the modulus operator (`n % 2 != 0`). This works for both positive and negative numbers:
- An odd number will have a remainder that is not zero when divided by 2.
  
### Step 3: Collect the Filtered Numbers
Finally, we use the `.collect()` method to collect the filtered odd numbers into a list using `Collectors.toList()`.

### Full Code Implementation

```java
import java.util.List;
import java.util.stream.Collectors;

public class NumberMagic {

    public List<Integer> filterOddNumbers(List<Integer> numbers) {
        // Convert the list to a stream, filter the odd numbers, collect them back into a list
        return numbers.stream()
                      .filter(n -> n % 2 != 0) // Filtering odd numbers
                      .collect(Collectors.toList()); // Collecting the filtered stream back to a list
    }
}
```

### Explanation:

1. **Stream Conversion:**  
   `numbers.stream()` converts the list of integers into a stream.
   
2. **Filter Condition:**  
   `.filter(n -> n % 2 != 0)` filters the stream, keeping only numbers where `n % 2` is not zero, i.e., odd numbers.
   
3. **Collecting the Results:**  
   `.collect(Collectors.toList())` collects the filtered numbers into a new list and returns it.

### Edge Case with Negative Numbers

In the initial solution, we filtered numbers by checking if `n % 2 == 1`, but this condition failed for negative odd numbers (e.g., `-3 % 2` gives `-1` instead of `1`). By changing the condition to `n % 2 != 0`, we handle both positive and negative odd numbers correctly.

### Running the Tests

Let’s run some test cases:
- **Input:** `[1, 2, 3, 4, 5]`  
  **Output:** `[1, 3, 5]`
  
- **Input:** `[-3, -2, -1, 0, 1, 2, 3]`  
  **Output:** `[-3, -1, 1, 3]`
  
- **Input:** `[6, 7, 8, 9, 10]`  
  **Output:** `[7, 9]`

All the test cases should pass successfully!

### Conclusion

In this exercise, we used **Java Streams** to filter out odd numbers from a list. We learned how to:
- Convert a list into a stream.
- Use the `.filter()` method with a lambda expression to filter out elements.
- Collect the filtered elements back into a list using `.collect(Collectors.toList())`.

This approach is clean, simple, and leverages the power of functional programming in Java.

---

## Solution Video For Coding Exercise - Get Cubes of First N Numbers

In this task, we're going to generate the cubes of the first N natural numbers using Java Streams. Let’s go step by step and solve the problem.

### Problem Overview

You’re given an integer `N`, and your task is to generate a list of cubes of the first `N` natural numbers. For example:
- If `N = 5`, the output should be `[1, 8, 27, 64, 125]`.
- If `N = 3`, the output should be `[1, 8, 27]`.
- If `N = 0`, the output should be an empty list.

### Input:
- A single integer `N`, where `N >= 0`.

### Output:
- A list of integers representing the cubes of the first `N` natural numbers.

### Example:
1. **Input:** `N = 5`  
   **Output:** `[1, 8, 27, 64, 125]`
   
2. **Input:** `N = 3`  
   **Output:** `[1, 8, 27]`
   
3. **Input:** `N = 0`  
   **Output:** `[]`

### Approach

We will utilize **Java Streams** and functional programming to solve this problem. The key steps are:
1. **Generate a sequence of numbers from 1 to N.**
2. **Map each number to its cube.**
3. **Convert the stream of cubes into a list.**

### Key Functions:
- **IntStream.rangeClosed(1, N)**: Generates a sequence of integers from `1` to `N`. We use `rangeClosed(1, N)` to include both the start and the end points.
- **map(number -> number * number * number)**: Maps each number in the stream to its cube.
- **boxed()**: Converts an `IntStream` into a `Stream<Integer>`, which is needed to collect the results into a list.
- **collect(Collectors.toList())**: Collects the stream into a list.

### Step-by-Step Implementation

### Step 1: Generate a Sequence of Numbers
We use `IntStream.rangeClosed(1, N)` to generate numbers from 1 to N. This ensures that we get the first N natural numbers.

### Step 2: Map Each Number to Its Cube
We then use the `.map()` function to take each number and calculate its cube using the expression `number * number * number`.

### Step 3: Collect the Cubes into a List
To convert the stream of cubes into a list, we use `.boxed()` followed by `.collect(Collectors.toList())`.

### Full Code Implementation

```java
import java.util.List;
import java.util.stream.Collectors;
import java.util.stream.IntStream;

public class FunctionalProgrammingMagic {

    public List<Integer> getCubesOfFirstNNumbers(int N) {
        // Generate a stream of numbers from 1 to N, map each to its cube, and collect into a list
        return IntStream.rangeClosed(1, N)
                        .map(number -> number * number * number)  // Cubing each number
                        .boxed()  // Convert IntStream to Stream<Integer>
                        .collect(Collectors.toList());  // Collect to List
    }
}
```

### Explanation:

1. **Stream Generation:**  
   `IntStream.rangeClosed(1, N)` generates a sequence of numbers from 1 to N.
   
2. **Mapping to Cubes:**  
   `.map(number -> number * number * number)` computes the cube of each number.
   
3. **Collecting the Result:**  
   `.boxed()` converts the `IntStream` into a `Stream<Integer>`, and `.collect(Collectors.toList())` collects the cubes into a list.

### Edge Case:
- If `N = 0`, `IntStream.rangeClosed(1, 0)` will result in an empty stream, so an empty list will be returned.

### Running the Tests

Let’s run the solution against some test cases:
- **Input:** `N = 5`  
  **Output:** `[1, 8, 27, 64, 125]`
  
- **Input:** `N = 3`  
  **Output:** `[1, 8, 27]`
  
- **Input:** `N = 0`  
  **Output:** `[]`

All tests should pass successfully!

### Conclusion

In this exercise, we used functional programming in Java to solve the problem of generating cubes of the first N natural numbers. We learned how to:
- Use **IntStream** to generate sequences of numbers.
- Use the **map()** function to transform each number in the stream.
- Collect the transformed numbers into a list using **Collectors.toList()**.

This approach is clean, efficient, and makes good use of Java's Stream API.

---

## Solution Video For Coding Exercise - Length of Course Names

Welcome back to another coding exercise solution! In this task, we are working on functional programming in Java, specifically focusing on getting the length of course names.

### Problem Overview

You need to complete a method called `getCourseNameCharacterCount` that takes in a list of course names and returns a list of integers representing the character count for each course name.

### Input:
- A list of strings, where each string is a course name (e.g., "Math", "English").
- The input can also be `null` or an empty list.

### Output:
- A list of integers representing the length of each course name in the same order.
- If the input is `null` or empty, return an empty list.

### Examples:

1. **Input:** `["Math", "English", "History", "Physics"]`  
   **Output:** `[4, 7, 7, 7]`  
   Explanation:  
   - "Math" has 4 characters.
   - "English" has 7 characters.
   - "History" has 7 characters.
   - "Physics" has 7 characters.

2. **Input:** `[]`  
   **Output:** `[]`

3. **Input:** `null`  
   **Output:** `[]`

### Approach

We'll break this down into a simple, step-by-step solution using **Java Streams**:
1. **Handle Edge Cases**: If the input list is `null`, we should return an empty list.
2. **Stream Processing**: 
   - Convert the list of course names into a stream.
   - Use the `.map()` function to transform each course name into its length.
   - Collect the transformed data back into a list.
3. **Return the Result**.

### Key Functions:
- **courses.stream()**: Converts the list of course names into a stream for processing.
- **map(String::length)**: Transforms each course name into its length using a method reference.
- **collect(Collectors.toList())**: Collects the resulting stream into a list.

### Full Code Implementation

```java
import java.util.List;
import java.util.stream.Collectors;

public class FunctionalProgrammingMagic {

    public List<Integer> getCourseNameCharacterCount(List<String> courses) {
        // Edge case: If courses is null, return an empty list
        if (courses == null) {
            return List.of();
        }

        // Convert the list into a stream, map each course name to its length, and collect into a list
        return courses.stream()
                      .map(String::length)  // Map each course to its character count
                      .collect(Collectors.toList());  // Collect into a list
    }
}
```

### Explanation:

1. **Handle Edge Case for Null Input**:  
   We check if the input list is `null`. If it is, we return an empty list using `List.of()`.

2. **Stream Processing**:  
   - `courses.stream()` converts the list into a stream.
   - `.map(String::length)` applies a method reference that calculates the length of each course name.
   - `.collect(Collectors.toList())` collects the results into a list of integers.

### Edge Cases:
- **Null Input**: If `courses` is `null`, return an empty list.
- **Empty List**: If `courses` is an empty list, return an empty list.

### Running the Tests

Let’s test the solution with the provided examples:
1. **Input:** `["Math", "English", "History", "Physics"]`  
   **Output:** `[4, 7, 7, 7]`
   
2. **Input:** `[]`  
   **Output:** `[]`
   
3. **Input:** `null`  
   **Output:** `[]`

All test cases should pass successfully!

### Conclusion

In this exercise, we demonstrated how to use Java's **Stream API** to process a list of strings and return a list of their lengths. This approach is clean, concise, and makes great use of functional programming techniques in Java.

---

## Solution Video For Coding Exercise - Sum of Squares

This exercise is about functional programming, where we’ll calculate the sum of squares of integers in a list using Java Streams.

### Problem Overview

You need to implement a function called `sumOfSquares` that takes a list of integers as input and returns the sum of the squares of these integers.

### Key Considerations:
- If the input list is `null`, return `0`.
- If the input list is empty, return `0`.
- Each integer in the list should be squared, and then all the squares should be summed up.
- The result should be returned as a `long`.

### Examples:

1. **Input:** `[1, 2, 3]`  
   **Output:** `14`  
   Explanation:  
   \( 1^2 + 2^2 + 3^2 = 1 + 4 + 9 = 14 \)

2. **Input:** `[]`  
   **Output:** `0`

3. **Input:** `null`  
   **Output:** `0`

### Approach

We will break down the solution into the following steps:
1. **Handle Edge Cases**: If the input list is `null` or empty, return `0`.
2. **Use Java Streams**: 
   - Convert the list to a stream.
   - Use the `mapToLong()` function to square each integer and ensure the result is a `long`.
   - Use the `sum()` function to sum all the squared values.
3. **Return the Result**: The result should be a `long` value representing the sum of squares.

### Key Functions:
- **numbers.stream()**: Converts the list of integers into a stream for processing.
- **mapToLong()**: Maps each integer to its square as a `long` value.
- **sum()**: Calculates the sum of the squared values in the stream.

### Full Code Implementation

```java
import java.util.List;

public class FunctionalProgrammingMagic {

    public long sumOfSquares(List<Integer> numbers) {
        // Handle edge case: If the list is null, return 0
        if (numbers == null) {
            return 0L;
        }

        // Convert the list into a stream, map each number to its square, and sum the results
        return numbers.stream()
                      .mapToLong(number -> (long) number * number)  // Square each number
                      .sum();  // Sum the squares
    }
}
```

### Explanation:

1. **Edge Case for Null Input**:  
   If the `numbers` list is `null`, we return `0L` (long `0`).

2. **Stream Processing**:  
   - `numbers.stream()` converts the list into a stream.
   - `.mapToLong(number -> (long) number * number)` squares each number, making sure the result is a `long` to avoid overflow issues.
   - `.sum()` sums all the squared values together.

3. **Return Result**: The sum of squares is returned as a `long`.

### Edge Cases:
- **Null Input**: If `numbers` is `null`, return `0`.
- **Empty List**: If `numbers` is an empty list, return `0`.

### Running the Tests

Let’s test the solution with the provided examples:
1. **Input:** `[1, 2, 3]`  
   **Output:** `14`
   
2. **Input:** `[]`  
   **Output:** `0`
   
3. **Input:** `null`  
   **Output:** `0`

All tests should pass successfully!

### Conclusion

In this exercise, we used **Java Streams** to efficiently calculate the sum of squares of a list of integers. This approach is concise, uses functional programming techniques, and handles edge cases like `null` and empty input lists.

---

## Solution Video For Coding Exercise - Find Max Even Number

Welcome back to another coding exercise solution! In this exercise, we are tasked with finding the **maximum even number** from a list of integers using Java Streams. Let's break down the problem and how we can approach it.

### Problem Overview

You are given a list of integers, and your task is to complete the function `findMaxEvenNumber`, which returns the maximum even number from the list. However, if the list:
- Is `null`
- Is empty
- Contains only odd numbers

In these cases, the function should return `0`.

### Examples:
1. **Input:** `[3, 5, 12, 78, 13]`  
   **Output:** `78`  
   Explanation: 78 is the largest even number.

2. **Input:** `[1, 3, 5]`  
   **Output:** `0`  
   Explanation: There are no even numbers in the list.

3. **Input:** `[]`  
   **Output:** `0`  
   Explanation: The list is empty.

4. **Input:** `null`  
   **Output:** `0`  
   Explanation: The list is null.

### Approach

We can solve this problem using Java Streams by following these steps:

1. **Handle the Edge Case for `null` List**: If the list is `null`, immediately return `0`.
2. **Stream the List**: Use the `stream()` function to convert the list into a stream for further processing.
3. **Filter Even Numbers**: Use the `filter()` method to extract only the even numbers.
4. **Find the Maximum**: Use the `max()` method to find the largest even number.
5. **Handle the Optional Result**: Since there may not be any even numbers, the `max()` function returns an `Optional`. We can use the `orElse()` method to return `0` if no even numbers are found.

### Code Implementation

Here’s the code that implements the solution:

```java
import java.util.List;
import java.util.Optional;

public class FunctionalProgrammingMagic {

    public int findMaxEvenNumber(List<Integer> numbers) {
        // Edge case: if the list is null, return 0
        if (numbers == null) {
            return 0;
        }

        // Stream the list, filter even numbers, and find the maximum
        Optional<Integer> maxEven = numbers.stream()
            .filter(number -> number % 2 == 0)  // Filter only even numbers
            .max(Integer::compare);             // Find the maximum even number

        // Return the maximum even number, or 0 if no even numbers are found
        return maxEven.orElse(0);
    }
}
```

### Detailed Explanation:

1. **Check for `null` Input**:  
   If the list `numbers` is `null`, we immediately return `0`.

2. **Streaming and Filtering**:  
   - `numbers.stream()` converts the list into a stream.
   - `.filter(number -> number % 2 == 0)` filters out all odd numbers, leaving only the even numbers.

3. **Finding the Maximum**:  
   - `.max(Integer::compare)` finds the maximum even number by comparing the filtered even numbers.

4. **Handling Optional Result**:  
   - The `max()` function returns an `Optional<Integer>` because there might not be any even numbers in the list.
   - `.orElse(0)` returns the value of the `Optional` if it exists; otherwise, it returns `0`.

### Edge Cases:
- **Null List**: If the input list is `null`, return `0`.
- **Empty List**: If the input list is empty, return `0`.
- **All Odd Numbers**: If there are no even numbers in the list, return `0`.

### Running the Tests

Let’s test the solution with a few examples:

1. **Input:** `[3, 5, 12, 78, 13]`  
   **Output:** `78`

2. **Input:** `[1, 3, 5]`  
   **Output:** `0`

3. **Input:** `[]`  
   **Output:** `0`

4. **Input:** `null`  
   **Output:** `0`

All test cases should pass successfully!

### Conclusion

In this exercise, we used **Java Streams** to filter and find the maximum even number from a list of integers. We made sure to handle cases where the input list could be `null`, empty, or contain only odd numbers.

---

## Section 32: Java Coding Exercises - Set 10

## Solution Video For Coding Exercise - Enum Direction

Welcome to another coding exercise solution! This time, we're working with **Enums** and implementing logic for **Direction** in Java. Let’s dive into the problem and break it down step-by-step.

### Problem Overview

In this task, you are given an enumeration called `Direction`, representing the four cardinal directions:
- **North**
- **South**
- **East**
- **West**

The goal is to implement two methods:
1. **left()**: Returns the direction to the left of the current direction.
2. **right()**: Returns the direction to the right of the current direction.

Enums are useful for representing a restricted set of values, such as directions, and they make it easier to work with constant values like these.

### Example Behavior:
1. **Left of North** is **West**.
2. **Right of North** is **East**.
3. **Left of West** is **South**.
4. **Right of West** is **North**.

### Approach

We’ll implement the `left()` and `right()` methods for the `Direction` enum to correctly return the appropriate direction when turning left or right.

### Enum Structure:
- **Enum Name:** `Direction`
- **Values:** `NORTH`, `SOUTH`, `EAST`, `WEST`
- **Methods:** 
  - `left()`: Returns the direction to the left.
  - `right()`: Returns the direction to the right.

### Key Concepts:
- **Enums:** Enums are great for representing a fixed set of constants, like cardinal directions.
- **Switch Statements:** We'll use switch statements to handle the different direction cases.
- **Circular Logic:** The direction sequence is circular, meaning that left of `NORTH` is `WEST`, and right of `WEST` is `NORTH`.

### Enum Code Implementation:

```java
public enum Direction {
    NORTH("North"),
    SOUTH("South"),
    EAST("East"),
    WEST("West");

    private final String name;

    Direction(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    // Method to return the direction to the left
    public Direction left() {
        switch (this) {
            case NORTH:
                return WEST;
            case WEST:
                return SOUTH;
            case SOUTH:
                return EAST;
            case EAST:
                return NORTH;
            default:
                throw new IllegalArgumentException("Invalid Direction");
        }
    }

    // Method to return the direction to the right
    public Direction right() {
        switch (this) {
            case NORTH:
                return EAST;
            case EAST:
                return SOUTH;
            case SOUTH:
                return WEST;
            case WEST:
                return NORTH;
            default:
                throw new IllegalArgumentException("Invalid Direction");
        }
    }
}
```

### Breakdown of the Code:

1. **Enum Values**:  
   We define four constants: `NORTH`, `SOUTH`, `EAST`, and `WEST`. Each has an associated `name` (for display purposes), which is passed via the constructor and stored in the `name` field.

2. **left() Method**:
   - This method determines which direction is to the left of the current direction.
   - We use a `switch` statement to check the current direction and return the appropriate direction.
   - For example, `left()` of `NORTH` is `WEST`, and `left()` of `WEST` is `SOUTH`.

3. **right() Method**:
   - This method determines which direction is to the right of the current direction.
   - Similarly, we use a `switch` statement here.
   - For example, `right()` of `NORTH` is `EAST`, and `right()` of `EAST` is `SOUTH`.

4. **Error Handling**:
   - We include a `default` case in both switch statements to throw an `IllegalArgumentException` in case an invalid direction is encountered (though this shouldn't happen with a fixed set of enum values).

### Running the Tests

Let's test the solution with a few examples:

1. **Left of NORTH:**
   - **Input:** `NORTH.left()`
   - **Output:** `WEST`

2. **Right of NORTH:**
   - **Input:** `NORTH.right()`
   - **Output:** `EAST`

3. **Left of WEST:**
   - **Input:** `WEST.left()`
   - **Output:** `SOUTH`

4. **Right of WEST:**
   - **Input:** `WEST.right()`
   - **Output:** `NORTH`

All test cases should pass successfully!

### Conclusion

In this exercise, we implemented an **Enum** to represent cardinal directions and added methods to determine the direction to the left and right. This solution showcases the power of enums for representing fixed sets of constants and how we can implement custom logic in enum classes.

---

## Solution Video For Coding Exercise - Enum Day Of The Week

Welcome back to another solution video for a coding exercise! This time, we are working with **Enums** to handle the days of the week. Let's dive into how we can effectively implement methods in an Enum to solve this problem.

### Problem Overview

In this task, you are given an incomplete `DaysOfWeek` enum, representing all seven days of the week:
- **Monday**
- **Tuesday**
- **Wednesday**
- **Thursday**
- **Friday**
- **Saturday**
- **Sunday**

The goal is to implement the following methods:

1. **getName()**: Returns the name of the day.
2. **isWeekday()**: Returns true if the day is a weekday (Monday through Friday) and false otherwise.
3. **isHoliday()**: Returns true if the day is a holiday (Saturday and Sunday).

### Example Behavior:
1. For **Tuesday**:
   - `getName()` should return **"Tuesday"**
   - `isWeekday()` should return **true**
   - `isHoliday()` should return **false**
   
2. For **Saturday**:
   - `getName()` should return **"Saturday"**
   - `isWeekday()` should return **false**
   - `isHoliday()` should return **true**

### Approach

We'll implement these methods step-by-step using the enum structure, which allows us to represent a restricted set of constant values (the days of the week). Enums also allow us to associate custom behavior (methods) with each value.

### Enum Code Implementation

```java
public enum DaysOfWeek {
    MONDAY("Monday"),
    TUESDAY("Tuesday"),
    WEDNESDAY("Wednesday"),
    THURSDAY("Thursday"),
    FRIDAY("Friday"),
    SATURDAY("Saturday"),
    SUNDAY("Sunday");

    private final String name;

    // Constructor to initialize the day name
    DaysOfWeek(String name) {
        this.name = name;
    }

    // Method to return the name of the day
    public String getName() {
        return this.name;
    }

    // Method to check if the day is a weekday
    public boolean isWeekday() {
        return this != SATURDAY && this != SUNDAY;
    }

    // Method to check if the day is a holiday
    public boolean isHoliday() {
        return !isWeekday();
    }
}
```

### Breakdown of the Code

1. **Enum Values**:  
   We define all seven days of the week, each associated with a string name (e.g., `"Monday"`, `"Tuesday"`, etc.).

2. **Constructor**:  
   The constructor takes the name of the day as an argument and assigns it to the `name` field. This allows each enum constant (day) to store its respective name.

3. **getName() Method**:
   - This method simply returns the `name` field, which holds the name of the day.
   - For example, calling `TUESDAY.getName()` will return `"Tuesday"`.

4. **isWeekday() Method**:
   - This method checks if the current day is a weekday (Monday through Friday).
   - If the day is not **Saturday** or **Sunday**, we return true (it's a weekday). Otherwise, we return false.

5. **isHoliday() Method**:
   - This method checks if the current day is a holiday.
   - We simply return the opposite of `isWeekday()`. If it's not a weekday, then it's a holiday.

### Alternative Approaches

- **Using a `switch` statement**:  
   Instead of using conditional checks, we could use a switch statement for checking whether a day is a weekday or a holiday. For example:

   ```java
   public boolean isWeekday() {
       switch (this) {
           case SATURDAY:
           case SUNDAY:
               return false;
           default:
               return true;
       }
   }
   ```

- **Manual Conditions**:  
   Instead of checking for weekdays using a single condition (`this != SATURDAY && this != SUNDAY`), we could use multiple `if` statements or switch cases, but the current approach is cleaner and easier to maintain.

### Running the Tests

Let's test the solution with a few examples:

1. **For Tuesday**:
   - `getName()` returns **"Tuesday"**
   - `isWeekday()` returns **true**
   - `isHoliday()` returns **false**

2. **For Saturday**:
   - `getName()` returns **"Saturday"**
   - `isWeekday()` returns **false**
   - `isHoliday()` returns **true**

All tests should pass successfully!

### Conclusion

In this exercise, we learned how to work with **Enums** in Java to represent a fixed set of values (days of the week) and associate custom methods to those values. By using Enums, we can create clean, organized code that handles specific scenarios with a predefined set of constants.

---

> End of coding exercises!