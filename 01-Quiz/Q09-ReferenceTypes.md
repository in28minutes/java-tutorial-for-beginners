## Step 01: Introducing Reference Types

**Question 1**

What is the purpose of reference variables in Java?

A. To store primitive values 
B. To store objects on the Heap 
C. To store the memory location of an object

**Answer: C**

**Question 2**

What is the main difference between reference types and primitive types in Java?

A. Primitive types are stored on the Stack, reference types on the Heap B. Primitive types are stored on the Heap, reference types on the Stack C. Both are stored on the Heap

**Answer: A**

**Question 3**

In the following code snippet, where are the objects `jupiter` and `dog` stored?

```
class Planet { ... }
Planet jupiter = new Planet();
jupiter ==> Planet@31a5c39e

class Animal { ... }
Animal dog = new Animal(12);
dog ==> Animal@27c20538
```

A. Stack 
B. Heap 
C. Both Stack and Heap

**Answer: B**


## Step 02: References: Usage And Puzzles

### Question 1

What is the value of a reference variable that is not initialized by the programmer in Java?

A. 0 
B. Empty 
C. Null

Answer: C. Null

### Question 2

What happens when you compare two reference variables in Java?

A. It compares the values stored inside the referenced objects. 
B. It compares the memory locations where the objects are stored. 
C. It compares the size of the objects.

Answer: B. It compares the memory locations where the objects are stored.

### Question 3

What happens when you assign one reference variable to another in Java?

A. It creates a copy of the entire referenced object. 
B. It only copies the reference. 
C. It creates a new object with the same values as the referenced object.

Answer: B. It only copies the reference.


## Step 03: Introducing String Quiz

### Question 1

What is a string in Java?

A. A sequence of numbers 
**B. A sequence of characters** 
C. A sequence of symbols

### Question 2

What is the output of the following code:

```
String str = "Test";
System.out.println(str.charAt(2));
```

A. 'e' 
**B. 's'** 
C. 'T'

### Question 3

What does the substring method of the String class return?

A. A sequence of numbers 
**B. A sequence of characters** 
C. A sequence of symbols

### Correct answers

1.  B. A sequence of characters
2.  B. 's'
3.  B. A sequence of characters

## Step 04: Programming Exercise PE-01, And String Utilities

### Quiz

1.  What does the `indexOf()` method in the String class do? 
2. A. Returns the position of a character in a string. 
3. B. Returns the starting position of a substring in a string. 
4. C. Both of the above. 
5. D. None of the above.
    
    **Answer:** C. Both of the above.
    
6.  How does the `endsWith()` method determine if a string ends with a given suffix? 
- A. It returns the position of the last occurrence of the suffix in the string. 
- B. It returns true if the string ends with the given suffix, false otherwise. 
- C. It returns false if the string ends with the given suffix, true otherwise. 
- D. None of the above.
    
    **Answer:** B. It returns true if the string ends with the given suffix, false otherwise.
    
7.  When using the `equals()` method, what is the result if the string is identical to the argument? 
- A. Returns true. 
- B. Returns false. 
- C. Returns the position of the first occurrence of the argument in the string. 
- D. None of the above.
    
    **Answer:** A. Returns true.

## Step 05: String Immutability

1.  What is the meaning of the word "immutable"? 
 - A. Changeable 
 - **B. Unchangeable** 
 - C. Mutable
    
2.  Can the value of a string object be changed after it is created? 
- A. Yes 
- **B. No**
    
3.  What does the method `concat()` do? 
- A. Changes the original value of a string object 
- **B. Returns a new string object by joining the contents of two string objects** 
- C. Trims a string object
    
4.  What happens to the original string object when the method `toUpperCase()` is used on it? 
- A. The original string object is changed to upper case 
- **B. The original string object remains unchanged, a new string object is returned with the changed value**
    
6.  What is the output of the following code:
    

```
String str = "in28Minutes";
str = str.concat(" is awesome");
```

- **A. "in28Minutes is awesome"** 
- B. "in28Minutes" 
- C. "in28Minutes is awesome" and "in28Minutes"

## Step 06: More String Utilities

Q1. What is the result of the following code:

```
int i = 20;
System.out.println("Value is " + i + 20);
```

 - A. Value is 40 
 - B. Value is 2020 
 - **C. Value is 2040**

Q2. What is the result of the following code:

```
String.join(",", "2", "3", "4");
```

 - **A. "2,3,4"** 
 - B. "23,4" 
 - C. "234"

Q3. What is the result of the following code:

```
"abcd".replace("ab", "xyz");
```

 - **A. "xyzcd"** 
 - B. "xyzabcd" 
 - C. "abcdxyz"




## Step 07: Storing mutable text

Question 1: What is the difference between StringBuffer and StringBuilder?

- A. StringBuffer is mutable while StringBuilder is immutable
- B. StringBuilder is mutable while StringBuffer is immutable
- C. Both StringBuffer and StringBuilder are immutable

Answer: B. StringBuilder is mutable while StringBuffer is immutable

Question 2: What is the main advantage of using StringBuilder over StringBuffer?

A. StringBuilder is thread-safe
B. StringBuilder offers better performance in both execution-time and memory usage
C. StringBuilder is a built-in class in Java

Answer: B. StringBuilder offers better performance in both execution-time and memory usage

Question 3: Can we modify a string literal using StringBuffer?

A. Yes, we can modify a string literal using StringBuffer
B. No, we cannot modify a string literal using StringBuffer
C. It depends on the situation

Answer: B. No, we cannot modify a string literal using StringBuffer




## Step 08: Introducing Wrapper Classes

Question 1: What is the purpose of using Wrapper Classes in Java?

A. To access type information about the corresponding primitive type 
B. To promote primitive data to an object reference type 
C. To move primitive type data around data structures

Answer: B. To promote primitive data to an object reference type

Question 2: What is Auto-Boxing in Java?

A. The process of promoting primitive data to an object reference type 
B. The process of converting an object reference type to a primitive data type 
C. The process of converting a primitive data type to an object reference type

Answer: C. The process of converting a primitive data type to an object reference type

Question 3: Can we modify the value of a wrapper class once it is assigned?

A. Yes, we can modify the value of a wrapper class 
B. No, the value of a wrapper class is immutable 
C. It depends on the type of wrapper class being used.

Answer: B. No, the value of a wrapper class is immutable



## Step 09: Creating Wrapper Objects


1. What are Wrapper Classes in Java?
- A. Classes that provide a mechanism to convert primitive data types into objects
- B. Classes that provide a mechanism to convert objects into primitive data types
- C. Both of the above
- D. None of the above
**Answer: C. Both of the above**

2. What is the difference between creating a Wrapper object using 'new' and 'valueOf()'?
- A. There is no difference
- B. 'new' creates a new object every time, whereas 'valueOf()' reuses existing objects with the same value
- C. 'new' reuses existing objects with the same value, whereas 'valueOf()' creates a new object every time
- D. None of the above
**Answer: B. 'new' creates a new object every time, whereas 'valueOf()' reuses existing objects with the same value**

3. Are Wrapper Classes mutable in Java?
- A. Yes
- B. No
- C. Depends on the implementation
- D. None of the above
**Answer: B. No**

    


## Step 10: Auto-Boxing, And Some Wrapper Constants

1.  What is Auto-Boxing in Java? 
- A. A feature that provides new functionality to the Java language 
- B. A mechanism to make code more readable 
- **C. A mechanism to upgrade a primitive data type to its corresponding object type**
- D. None of the above
    
2.  What is the mechanism used by Auto-Boxing in Java? 
- A. It uses the 'new' operator to create new objects every time 
- **B. It uses the 'valueOf()' method to create objects**
- C. It uses the 'toString()' method to create objects 
- D. None of the above
    
3.  Are there any constants available on Wrapper Classes in Java to check the size and range of values they can store? 
- A. No 
- **B. Yes**
- C. Depends on the implementation 
- D. None of the above


## Step 11: The Java Date API Quiz

1.  What is the main purpose of the Java Date API? 
- a. To perform arithmetic operations on date and time objects 
- b. To provide an interface for date and time classes 
- c. To provide a framework for date and time classes 
- d. To provide a library for date and time classes
    
    Answer: b
    
2.  What is the main difference between LocalDate, LocalTime, and LocalDateTime? 
- a. They are used for different purposes 
- b. They are different classes in Java 
- c. They are used to represent different values for date and time 
- d. They are used for different date and time formats
    
    Answer: c
    
3.  What is the difference between the `LocalDate.now()` and `LocalDate.of()` methods in the Java Date API? 
- a. `LocalDate.now()` returns the current date and time, while `LocalDate.of()` returns a specific date and time 
- b. `LocalDate.now()` returns the current date, while `LocalDate.of()` returns a specific date 
- c. `LocalDate.now()` returns the current time, while `LocalDate.of()` returns a specific time 
- d. `LocalDate.now()` returns a date and time object, while `LocalDate.of()` returns a date object
    
    Answer: b
    

## Step 12: Playing With java.time.LocalDate Quiz

1.  What information can you retrieve from a LocalDate object? 
- a. Date information such as Day/Month/Year and related attributes 
- b. Time information such as Hour/Minute/Second and related attributes 
- c. Both date and time information 
- d. None of the above
    
    Answer: a
    
3.  Are LocalDate, LocalTime, and LocalDateTime objects mutable? a. Yes b. No
    
    Answer: b
    
4.  What is the result of the following code snippet?
    

```
LocalDate today = LocalDate.now();
LocalDate tomorrow = today.plusDays(1);
System.out.println(today.isBefore(tomorrow));
```

a. True
b. False
c. Error

Answer: a

## Step 13: Comparing LocalDate Objects Quiz

1.  What is the purpose of the `isBefore()` and `isAfter()` methods in the Java Date API? 
- a. To compare the order of two LocalDate objects 
- b. To determine if a LocalDate object is earlier or later than a specific date 
- c. To compare the value of two LocalDate objects 
- d. To determine if a LocalDate object is equal to a specific date
    
    Answer: a
    
3.  What is the result of the following code snippet?
    

```
LocalDate today = LocalDate.now();
LocalDate yesterday = LocalDate.of(2018, 01, 31);
System.out.println(today.isAfter(yesterday));
```

a. True
b. False
c. Error

Answer: a

3. Can you compare LocalTime and LocalDateTime objects using the `isBefore()` and `isAfter()` methods? 
- a. Yes 
- b. No



`Answer: a`