## Step 01: The Need For Array Quiz

1.  Why do we need arrays? 
- a. To store different types of data. 
- b. To store similar types of data. 
- c. To store data in an unorganized manner.
    
    **b. To store similar types of data.**
    
2.  What is the use of indexing operator, ‘[]’ in arrays? a. To access elements from the array. b. To store elements in the array. c. To change the elements in the array.
    
    **a. To access elements from the array.**
    
3.  What is the purpose of enhanced for loop in arrays? 
- a. To store elements in the array. 
- b. To access elements from the array. 
- c. To iterate through all elements in the array.
    
    **c. To iterate through all elements in the array.**
    

## Step 02: Storing and Accessing Array Values Quiz

1.  What is the purpose of using the new operator in arrays? a. To initialize an array with specific values. b. To create an array with a specific size. c. To assign values to an array.
    
    **b. To create an array with a specific size.**
    
2.  How can we access elements from an array? 
- a. By using the indexing operator, ‘[]’. 
- b. By using the length property of the array. 
- c. By using the for loop.
    
    **a. By using the indexing operator, ‘[]’.**
    
3.  What is the length property in arrays used for? 
- a. To find the size of an array. 
- b. To find the number of elements in an array. 
- c. To find the value of an element in an array.
    
    **b. To find the number of elements in an array.**
    

## Step 04: Array Initialization, Data Types and Exceptions Quiz

1.  What is the value of an array element of type int when it is not initialized? 
- a. Null 
- b. False 
- c. 0
    
    **c. 0**
    
2.  What is the value of an array element of type boolean when it is not initialized? 
- a. Null 
- b. False 
- c. 0
    
    **b. False**
    
3.  What is the declaration part of an array definition not allowed to include? 
- a. The type of elements stored in the array. 
- b. The dimension of the array. 
- c. The name of the array.
    
    **b. The dimension of the array.**
    


## Step 05: Array Utilities Quiz

1.  What is the purpose of the method `Arrays.fill`? 
- a. To compare two arrays 
- b. To fill an array with a specified value 
- c. To perform an in-position sorting of elements 
- d. To store zero or more number of elements in an array
    
    **Answer: b. To fill an array with a specified value**
    
3.  What is the output of the following code?
    
    ```
    int[] marks = new int[5];
    Arrays.fill(marks, 100);
    System.out.println(marks);
    ```
    
  - a. [100,100,100,100,100] 
  - b. [0,0,0,0,0] 
  - c. 100,100,100,100,100 
  - d. I@6c49835d
    
    **Answer: a. [100,100,100,100,100]**
    
4.  What is the result of the following code?
    
```
  int[] array1 = {1, 2, 3};
    int[] array2 = {1, 2, 3};
    Arrays.equals(array1, array2);
```
    
    - a. false 
    - b. true 
    - c. [1,2,3] 
    - d. I@6c49835d
    
    **Answer: b. true**

# Step 06: Classroom Exercise CE-AA-02

Create a multiple-choice quiz based on the concepts taught in this step:

**Question 1:** Which of the following utility methods can be used to get the total number of marks of a `Student` object?

-   A) `getNumberOfmarks()`
-   B) `getTotalSumOfMarks()`
-   C) `getAverageMarks()`

**Answer:** A) `getNumberOfmarks()`

**Question 2:** Which of the following is an implementation of the `Student` class as an array?

-   A) `Student student = new Student(name, list-of-marks);`
-   B) `int[] marks = {99, 98, 100};`
-   C) `BigDecimal average = student.getAverageMarks();`

**Answer:** B) `int[] marks = {99, 98, 100};`

**Question 3:** Which of the following utility methods can be used to get the maximum mark of a `Student` object?

-   A) `getNumberOfmarks()`
-   B) `getMaximumMark()`
-   C) `getMinimumMark()`

**Answer:** B) `getMaximumMark()`

# Step 08: Variable Arguments - The Basics

Create a multiple-choice quiz based on the concepts taught in this step:

**Question 1:** What is the critical part when creating a method which can accept a variable number of arguments?

-   A) The `int` data type
-   B) The `...` symbol
-   C) The `Arrays.toString()` method

**Answer:** B) The `...` symbol

**Question 2:** What is the output of the following code snippet?

```
class Something {
  public void doSomething(int... values) {
    System.out.println(Arrays.toString(values));
  }
}
Something thing = new Something();
thing.doSomething(1, 2, 3);
```

-   A) `[1, 2]`
-   B) `[1, 2, 3]`
-   C) `1 2 3`

**Answer:** B) `[1, 2, 3]`

**Question 3:** Where should the variable arguments list be placed in the parameter list passed to a method?

-   A) At the beginning
-   B) In the middle
-   C) At the end

**Answer:** C) At the end

# Step 09: Variable Argument Methods For Student

Create a multiple-choice quiz based on the concepts taught in this step:

**Question 1:** Which of the following is an example of a variable argument method in the `Student` class?

-   A) `public int getNumberOfMarks()`
-   B) `public int[] getMarks()`
-   C) `public Student(String name, int... marks)`

**Answer:** C) `public Student(String name, int... marks)`

**Question 2:** What is the output of the following code snippet?

```
Student student = new Student("Ranga", 97, 98, 100);
System.out.println(student.getNumberOfMarks());
```

-   A) `3`
-   B) `97, 98, 100`
-   C) `295`

**Answer:** A) `3`

**Question 3:** What happens if you pass the wrong data type to a variable argument method?

-   A) The Java compiler will throw an error.
-   B) The program will run, but with unexpected results.
-   C) The program will crash.

**Answer:** A) The Java compiler will throw an error.

# Step 10: Arrays - Some Puzzles And Exercises

Create a multiple-choice quiz based on the concepts taught in this step:

**Question 1:** When creating an array of objects, what does the array hold?

-   A) The actual objects themselves
-   B) Copies of the objects
-   C) References to the created objects

**Answer:** C) References to the created objects

**Question 2:** What is the output of the following code snippet?

```
Person[] persons = new Person[3];
persons[0] = new Person();
persons[2] = new Person();
System.out.println(persons[1]);
```

-   A) `null`
-   B) An error will be thrown
-   C) A memory address

**Answer:** A) `null`

**Question 3:** What is the output of the following code snippet?

```
String[] textValues = {"Apple", "Ball", "Cat"};
System.out.println(textValues[2].charAt(0));
```

-   A) `A`
-   B) `B`
-   C) `C`

**Answer:** C) `C`

### Step 11: Problems With Arrays

Question 1: Why is it difficult to add or remove elements in an array?

-   A) Because the size of an array is fixed
-   B) Because arrays are only for primitive types
-   C) Because arrays cannot store non-homogeneous types

Answer: A

Question 2: How can we add an element to an array?

-   A) By increasing the size of the array dynamically
-   B) By decreasing the size of the array dynamically
-   C) By converting the array to an ArrayList

Answer: A

Question 3: What is the drawback of adding or removing elements from an array?

-   A) It can cause an ArrayIndexOutOfBoundsException
-   B) It can be very inefficient
-   C) It can cause a NullPointerException

Answer: B

### Step 12: Introducing ArrayList

Question 1: What is the main advantage of ArrayList over arrays?

-   A) ArrayList can store only primitive types
-   B) ArrayList provides operations to add and remove elements
-   C) ArrayList has a fixed size

Answer: B

Question 2: How do you remove an element from an ArrayList?

-   A) Using the remove() method
-   B) Using the delete() method
-   C) Using the clear() method

Answer: A

Question 3: What is the warning message displayed when adding non-homogeneous types to an ArrayList?

-   A) "Type safety: The method add(Object) belongs to the raw type ArrayList. References to generic type ArrayList<E> should be parameterized."
-   B) "Unchecked call to add(E) as a member of the raw type java.util.ArrayList"
-   C) "Type mismatch: cannot convert from int to String"

Answer: B

### Step 13: Refactoring Student To Use ArrayList

Question 1: How can we create an ArrayList that can hold only String values?

-   A) ArrayList<String> items = new ArrayList<String>()
-   B) ArrayList items = new ArrayList<String>()
-   C) ArrayList<String> items = new ArrayList()

Answer: A

Question 2: What method can be used to find the maximum value in an ArrayList?

-   A) Collections.max()
-   B) ArrayList.max()
-   C) ArrayList.getMaximum()

Answer: A

Question 3: How can we add a mark to a Student using ArrayList?

-   A) Using the addMark() method
-   B) Using the add() method of ArrayList
-   C) Using the add() method of the Student class

Answer: A

### Step 14: Enhancing Student Further

Question 1: How can we remove a mark from a Student using ArrayList?

-   A) Using the remove() method of ArrayList
-   B) Using the removeMark() method
-   C) Using the delete() method of ArrayList

Answer: B

Question 2: What is the output of `System.out.println(student)` in the main method of Step 14?

-   A) Ranga[97,98,100]
-   B) Ranga[97,98,100,35]
-   C) Ranga[97,100,35]

Answer: C

Question 3: How can we find the minimum value in an ArrayList?

-   A) Collections.min()
-   B) ArrayList.minimum()
-   C) ArrayList.getMin()

Answer: A