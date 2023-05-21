
### Step 01: Introducing Reference Types

**Question 60**

What is the purpose of reference variables in Java?

  * A. To store primitive values `Incorrect: Reference variables are used to store references to objects, not primitive values.`
  * B. To store objects on the Heap `Incorrect: Reference variables store references (addresses), not the actual objects.`
  * C. To store the memory location of an object `Correct: Reference variables store the memory location (reference) of an object.`【60†source】

**Question 61**

What is the main difference between reference types and primitive types in Java?

  * A. Primitive types are stored on the Stack, reference types on the Heap `Correct: Primitive types are stored on the Stack and reference types are stored on the Heap.`
  * B. Primitive types are stored on the Heap, reference types on the Stack `Incorrect: This is the opposite of the actual situation.`
  * C. Both are stored on the Heap `Incorrect: Primitive types are stored on the Stack, not on the Heap.`【61†source】

**Question 62**

In the following code snippet, where are the objects `jupiter` and `dog` stored?

```java
class Planet { ... }
Planet jupiter = new Planet();

class Animal { ... }
Animal dog = new Animal(12);
```

  * A. Stack `Incorrect: Objects are stored on the Heap in Java.`
  * B. Heap `Correct: Objects are stored on the Heap in Java.`
  * C. Both Stack and Heap `Incorrect: In Java, the Stack is used for storing method calls and primitive types, while the Heap is used for storing objects.`【62†source】

### Step 02: References: Usage And Puzzles

**Question 63**

What is the value of a reference variable that is not initialized by the programmer in Java?

  * A. 0 `Incorrect: 0 is a default value for numeric primitive types, not for reference types.`
  * B. Empty `Incorrect: Empty is not a default value for a reference variable.`
  * C. Null `Correct: If a reference variable is not initialized, its default value will be null.`【63†source】

**Question 64**

What happens when you compare two reference variables in Java?

  * A. It compares the values stored inside the referenced objects `Incorrect: By default, comparing two reference variables checks if they point to the same object, not the content of the objects.`
  * B. It compares the memory locations where the objects are stored `Correct: When you compare two reference variables, it checks whether they point to the same object, i.e., they have the same memory location.`
  * C. It compares the size of the objects `Incorrect: Java does not compare the size of the objects when comparing two reference variables.`【64†source】

**Question 65**

What happens when you assign one reference variable to another in Java?

  * A. It creates a copy of the entire referenced object `Incorrect: Assigning one reference variable to another does not copy the object, only the reference.`
  * B. It only copies the reference `Correct: When you assign one reference variable to another, it copies the reference, not the object. As a result, both variables point to the same object.`
  * C. It creates a new object with the same values as the referenced object `Incorrect: Assigning one reference variable to another does not create a new object.`【65†source】

### Step 03: Introducing String Quiz

**Question 66**

What is a string in Java?

  * A. A sequence of numbers `Incorrect: In Java, a string is not a sequence of numbers.`
  * B. A sequence of characters `Correct: In Java, a string is a sequence of characters.`
  * C. A sequence of symbols `Incorrect: In Java, a string is not a sequence of symbols, it is a sequence of characters.`【66†source】

**Question 67**

What is the output of the following code:

```java
String str = "Test";
System.out.println(str.charAt(2));
```

  * A. 'e' `Incorrect: The character at index 2 of the string "Test" is 's', not 'e'.`
  * B. 's' `Correct: The character at index 2 of the string "Test" is 's'.`
  * C. 'T' `Incorrect: The character at index 2 of the string "Test" is 's', not 'T'.`【67†source】

**Question 68**

What does the substring method of the String class return?

  * A. A sequence of numbers `Incorrect: The substring method returns a sequence of characters, not numbers.`
  * B. A sequence of characters `Correct: The substring method returns a sequence of characters from the original string.`
  * C. A sequence of symbols `Incorrect: The substring method returns a sequence of characters, not symbols.`【68†source】

### Step 04: Programming Exercise PE-01, And String Utilities

**Question 102**

What does the indexOf() method in the String class do?

  * A. Returns the position of a character in a string `Correct but not the complete answer: The indexOf() method does return the position of the first occurrence of a specified character in a string.`
  * B. Returns the starting position of a substring in a string `Correct but not the complete answer: The indexOf() method does return the position of the first occurrence of a specified substring in a string.`
  * C. Both of the above `Correct: The indexOf() method can return the position of a character or a substring in a string.`
  * D. None of the above `Incorrect: The indexOf() method does perform the functions stated in option C.`【102†source】

**Question 103**

How does the endsWith() method determine if a string ends with a given suffix?

  * A. It returns the position of the last occurrence of the suffix in the string `Incorrect: The endsWith() method does not return a position.`
  * B. It returns true if the string ends with the given suffix, false otherwise `Correct: The endsWith() method checks if a string ends with the specified suffix and returns a boolean result.`
  * C. It returns false if the string ends with the given suffix, true otherwise `Incorrect: The endsWith() method returns true if the string ends with the specified suffix, not false.`
  * D. None of the above `Incorrect: The endsWith() method does perform the function stated in option B.`【103†source】

**Question 104**

When using the equals() method, what is the result if the string is identical to the argument?

  * A. Returns true `Correct: The equals() method compares the string to the argument and returns true if they are identical.`
  * B. Returns false `Incorrect: The equals() method returns false if the strings are not identical, not if they are.`
  * C. Returns the position of the first occurrence of the argument in the string `Incorrect: The equals() method does not return a position.`
  * D. None of the above `Incorrect: The equals() method does perform the function stated in option A.`【104†source】

### Step 05: String Immutability

**Question 72**

What is the meaning of the word "immutable"?

  * A. Changeable `Incorrect: "Immutable" means unchangeable.`
  * B. Unchangeable `Correct: "Immutable" means unchangeable.`
  * C. Mutable `Incorrect: "Mutable" is the opposite of "immutable". It means changeable.`【72†source】

**Question 73**

Can the value of a string object be changed after it is created?

  * A. Yes `Incorrect: String objects are immutable in Java, meaning their value cannot be changed once created.`
  * B. No `Correct: String objects are immutable in Java, meaning their value cannot be changed once created.`【73†source】

**Question 74**

What does the method concat() do

 in Java?

  * A. Changes the original string by appending another string `Incorrect: The concat() method does not change the original string; instead, it returns a new string.`
  * B. Returns a new string resulting from appending another string to the original string `Correct: The concat() method returns a new string that is the result of appending the specified string to the end of the original string.`
  * C. Replaces the original string with a new string `Incorrect: The concat() method does not replace the original string; it returns a new string.`【74†source】

**Question 75**

What is String Pool in Java?

  * A. A pool of methods for the String class `Incorrect: The String Pool is a pool of literal strings, not methods.`
  * B. A pool of literal strings stored in the heap memory `Correct: The String Pool in Java is a pool of literal strings stored in the heap memory.`
  * C. A pool of references to the String objects `Incorrect: The String Pool is a pool of literal strings, not references to String objects.`【75†source】


### Step 05: String Immutability Continued

**Question 76**

What happens to the original string object when the method toUpperCase() is used on it?

  * A. The original string object is changed to upper case `Incorrect: In Java, strings are immutable. The toUpperCase() method returns a new string.`
  * B. The original string object remains unchanged, a new string object is returned with the changed value `Correct: The toUpperCase() method does not change the original string; it returns a new string.`【76†source】

**Question 77**

What is the output of the following code:

```java
String str = "in28Minutes";
str = str.concat(" is awesome");
System.out.println(str);
```

  * A. "in28Minutes is awesome" `Correct: The concat() method appends the given string to the end of the original string and the result is stored in 'str'.`
  * B. "in28Minutes" `Incorrect: The concat() method appends the given string to the end of the original string.`
  * C. "in28Minutes is awesome" and "in28Minutes" `Incorrect: The System.out.println() method will print only one string - the value of 'str'.`【77†source】

### Step 06: More String Utilities

**Question 78**

What is the result of the following code:

```java
int i = 20;
System.out.println("Value is " + i + 20);
```

  * A. Value is 40 `Incorrect: In this case, 'i + 20' will not perform integer addition because of string concatenation, and will result in '2020'.`
  * B. Value is 2020 `Correct: The "+" operator in this context is used for string concatenation, not numerical addition.`
  * C. Value is 2040 `Incorrect: The "+" operator in this context is used for string concatenation, not numerical addition.`【78†source】

**Question 79**

What is the result of the following code:

```java
String.join(",", "2", "3", "4");
```

  * A. "2,3,4" `Correct: The join() method concatenates the given strings with a comma as a delimiter.`
  * B. "23,4" `Incorrect: The join() method concatenates all the given strings with a comma as a delimiter.`
  * C. "234" `Incorrect: The join() method concatenates the given strings with a comma as a delimiter.`【79†source】

**Question 80**

What is the result of the following code:

```java
"abcd".replace("ab", "xyz");
```

  * A. "xyzcd" `Correct: The replace() method replaces all occurrences of the first argument with the second argument in the string.`
  * B. "xyzabcd" `Incorrect: The replace() method does not append the replacement at the start of the string.`
  * C. "abcdxyz" `Incorrect: The replace() method does not append the replacement at the end of the string.`【80†source】

### Step 07: Storing mutable text

**Question 81**

What is the difference between StringBuffer and StringBuilder?

  * A. StringBuffer is mutable while StringBuilder is immutable `Incorrect: Both StringBuffer and StringBuilder are mutable.`
  * B. StringBuilder is mutable while StringBuffer is immutable `Incorrect: Both StringBuffer and StringBuilder are mutable.`
  * C. Both StringBuffer and StringBuilder are immutable `Incorrect: Both StringBuffer and StringBuilder are mutable.`【81†source】

**Question 82**

What is the main advantage

 of using StringBuilder over StringBuffer?

  * A. StringBuilder is thread-safe `Incorrect: StringBuffer is thread-safe, not StringBuilder.`
  * B. StringBuilder offers better performance in both execution-time and memory usage `Correct: Because StringBuilder is not thread-safe, it doesn't have the overhead of synchronization, which makes it faster and more efficient than StringBuffer.`
  * C. StringBuilder is a built-in class in Java `Incorrect: Both StringBuffer and StringBuilder are built-in classes in Java.`【82†source】

**Question 83**

Can we modify a string literal using StringBuffer?

  * A. Yes, we can modify a string literal using StringBuffer `Incorrect: String literals are immutable in Java, so they cannot be modified by StringBuffer or any other class.`
  * B. No, we cannot modify a string literal using StringBuffer `Correct: String literals are immutable in Java, so they cannot be modified.`
  * C. It depends on the situation `Incorrect: String literals are always immutable in Java, regardless of the situation.`【83†source】

### Step 08: Introducing Wrapper Classes

**Question 84**

What is the purpose of using Wrapper Classes in Java?

  * A. To access type information about the corresponding primitive type `Incorrect: Wrapper classes in Java are primarily used to convert primitive data types into objects.`
  * B. To promote primitive data to an object reference type `Correct: Wrapper classes in Java are used to convert primitive data types into objects. This is often necessary because certain Java collections can only handle objects and not primitive types.`
  * C. To move primitive type data around data structures `Incorrect: While it's true that wrapper classes can help move primitive data around in object-oriented data structures, their primary purpose is to convert primitive types into objects.`【84†source】

**Question 85**

What is Auto-Boxing in Java?

  * A. The process of promoting primitive data to an object reference type `Incorrect: Auto-boxing is the automatic conversion that the Java compiler makes between the primitive types and their corresponding object wrapper classes.`
  * B. The process of converting an object reference type to a primitive data type `Incorrect: This process is known as unboxing, not auto-boxing.`
  * C. The process of converting a primitive data type to an object reference type `Correct: Auto-boxing is the automatic conversion of primitive types to their corresponding object wrapper classes.`【85†source】

**Question 86**

Can we modify the value of a wrapper class once it is assigned?

  * A. Yes, we can modify the value of a wrapper class `Incorrect: Once a value has been assigned to a wrapper class, it cannot be changed.`
  * B. No, the value of a wrapper class is immutable `Correct: Once a value has been assigned to a wrapper class, it cannot be changed. This is because all wrapper classes in Java are immutable.`
  * C. It depends on the type of wrapper class being used. `Incorrect: All wrapper classes in Java are immutable, regardless of the type.`【86†source】

### Step 09: Creating Wrapper Objects

**Question 87**

What are Wrapper Classes in Java?

  * A. Classes that provide a mechanism to convert primitive data types into objects `Correct: This is one of the main functions of wrapper classes in Java.`
  * B. Classes that provide a mechanism to convert objects into primitive data types `Correct: This is one of the main functions of wrapper classes in Java. They allow us to "unwrap" the value of an object into a primitive type through a process known as unboxing.`
  * C. Both of the above `Correct: Wrapper classes in Java both convert primitive data types

 into objects (known as boxing), and provide a mechanism to convert objects into primitive data types (known as unboxing).`
  * D. None of the above `Incorrect: Wrapper classes in Java serve both of the functions listed above.`【87†source】

**Question 88**

What is the difference between creating a Wrapper object using 'new' and 'valueOf()'?

  * A. There is no difference `Incorrect: There is a significant difference between these two methods.`
  * B. 'new' creates a new object every time, whereas 'valueOf()' reuses existing objects with the same value `Correct: The 'new' keyword always creates a new object, while 'valueOf()' may return a cached object for certain ranges of values (particularly small integers).`
  * C. 'new' reuses existing objects with the same value, whereas 'valueOf()' creates a new object every time `Incorrect: It is 'valueOf()' that may reuse objects, not 'new'.`
  * D. None of the above `Incorrect: The correct answer is option B.`【88†source】

**Question 89**

Are Wrapper Classes mutable in Java?

  * A. Yes `Incorrect: Wrapper classes in Java are immutable.`
  * B. No `Correct: Once a value has been assigned to a wrapper class, it cannot be changed.`
  * C. Depends on the implementation `Incorrect: All wrapper classes in Java are immutable, regardless of the implementation.`
  * D. None of the above `Incorrect: The correct answer is option B.`【89†source】

### Step 10: Auto-Boxing, And Some Wrapper Constants

**Question 90**

What is Auto-Boxing in Java?

  * A. A feature that provides new functionality to the Java language `Incorrect: While it is true that auto-boxing was a new feature introduced in Java 5, it is not the definition of auto-boxing.`
  * B. A mechanism to make code more readable `Incorrect: While auto-boxing can make code more readable, that is not its primary function.`
  * C. A mechanism to upgrade a primitive data type to its corresponding object type `Correct: Auto-boxing is the automatic conversion of primitive types to their corresponding object wrapper classes.`
  * D. None of the above `Incorrect: The correct answer is option C.`【90†source】

**Question 91**

What is the mechanism used by Auto-Boxing in Java?

  * A. It uses the 'new' operator to create new objects every time `Incorrect: Auto-boxing uses the valueOf() method, not the new operator.`
  * B. It uses the 'valueOf()' method to create objects `Correct: Auto-boxing uses the valueOf() method to create an instance of the wrapper class for the corresponding primitive type.`
  * C. It uses the 'toString()' method to create objects `Incorrect: The toString() method is used to convert an object to a string, not to create new objects.`
  * D. None of the above `Incorrect: The correct answer is option B.`【91†source】

**Question 92**

Are there any constants available on Wrapper Classes in Java to check the size and range of values they can store?

  * A. No `Incorrect: Each wrapper class does indeed contain constants that represent the minimum and maximum values that can be stored.`
  * B. Yes `Correct: Each wrapper class contains constants MIN_VALUE and MAX_VALUE that represent the minimum and maximum values that can be stored in an object of that type.`
  * C. Depends on the implementation `Incorrect: All standard wrapper classes in Java contain these constants.`
  * D.

 None of the above `Incorrect: The correct answer is option B.`【92†source】

### Step 11: The Java Date API Quiz

**Question 93**

What is the main purpose of the Java Date API?

  * a. To perform arithmetic operations on date and time objects `Incorrect: While the Java Date API does allow arithmetic operations on date and time objects, this is not its main purpose.`
  * b. To provide an interface for date and time classes `Incorrect: The Java Date API provides more than just an interface; it provides a full implementation for handling date and time.`
  * c. To provide a framework for date and time classes `Correct: The Java Date API is a framework that provides classes for handling date and time in a way that is both easier to understand and more accurate than using just the Date class.`
  * d. To provide a library for date and time classes `Incorrect: While the Java Date API can be considered a library, the most accurate description is that it is a framework.`【93†source】

**Question 94**

What is the main difference between LocalDate, LocalTime, and LocalDateTime?

  * a. They are used for different purposes `Incorrect: While these classes are used for different purposes, the key difference is what they represent.`
  * b. They are different classes in Java `Incorrect: While this is technically true, it doesn't describe the functional differences between these classes.`
  * c. They are used to represent different values for date and time `Correct: LocalDate represents a date (year, month, day), LocalTime represents a time (hour, minute, second, nanosecond), and LocalDateTime represents both a date and a time.`
  * d. They are used for different date and time formats `Incorrect: While these classes can be used to format dates and times in different ways, the key difference is what they represent.`【94†source】

**Question 95**

What is the difference between the LocalDate.now() and LocalDate.of() methods in the Java Date API?

  * a. LocalDate.now() returns the current date and time, while LocalDate.of() returns a specific date and time `Incorrect: LocalDate.now() returns the current date, not the current date and time.`
  * b. LocalDate.now() returns the current date, while LocalDate.of() returns a specific date `Correct: LocalDate.now() returns the current date, and LocalDate.of() can be used to create a LocalDate object for a specific date.`
  * c. LocalDate.now() returns the current time, while LocalDate.of() returns a specific time `Incorrect: LocalDate objects do not contain time information.`
  * d. LocalDate.now() returns a date and time object, while LocalDate.of() returns a date object `Incorrect: Both methods return LocalDate objects, which contain only date information.`【95†source】

### Step 12: Playing With java.time.LocalDate Quiz

**Question 96**

What information can you retrieve from a LocalDate object?

  * a. Date information such as Day/Month/Year and related attributes `Correct: LocalDate objects contain date information and related attributes, but do not contain any time information.`
  * b. Time information such as Hour/Minute/Second and related attributes `Incorrect: LocalDate objects do not contain any time information.`
  * c. Both date and time information `Incorrect: LocalDate objects contain only date information, not time information.`
  * d. None of the above `Incorrect: The correct answer is option A.`【96†source】

**Question 97**

Are LocalDate, LocalTime, and LocalDateTime objects mutable?

  * a. Yes `Incorrect: Objects of these classes are immutable.`
  * b. No `Correct: Objects of LocalDate, LocalTime, and LocalDateTime are immutable. Once created, their

 state cannot be changed.`【97†source】

**Question 98**

What is the result of the following code snippet?

```java
LocalDate today = LocalDate.now();
LocalDate tomorrow = today.plusDays(1);
System.out.println(today.isBefore(tomorrow));
```

  * a. True `Correct: The method `isBefore()` returns true because the date `tomorrow` is after `today`.`
  * b. False `Incorrect: The correct answer is true.`
  * c. Error `Incorrect: The code will not result in an error.`【98†source】

### Step 13: Comparing LocalDate Objects Quiz

**Question 99**

What is the purpose of the isBefore() and isAfter() methods in the Java Date API?

  * a. To compare the order of two LocalDate objects `Correct: The `isBefore()` and `isAfter()` methods are used to determine if one LocalDate is before or after another, respectively.`
  * b. To determine if a LocalDate object is earlier or later than a specific date `Incorrect: While this can be a result of using these methods, it's not the purpose. Their purpose is to compare two LocalDate objects.`
  * c. To compare the value of two LocalDate objects `Incorrect: These methods do not compare the value of two LocalDate objects. They check the order of the dates.`
  * d. To determine if a LocalDate object is equal to a specific date `Incorrect: For equality checks, the `isEqual()` method should be used.`【99†source】

**Question 100**

What is the result of the following code snippet?

```java
LocalDate today = LocalDate.now();
LocalDate yesterday = LocalDate.of(2018, 01, 31);
System.out.println(today.isAfter(yesterday));
```

  * a. True `Correct: Unless this code is run on January 31, 2018, `today` will be after `yesterday`, and so `isAfter()` will return true.`
  * b. False `Incorrect: Unless this code is run on January 31, 2018, the method `isAfter()` will return true.`
  * c. Error `Incorrect: The code will not result in an error.`【100†source】

**Question 101**

Can you compare LocalTime and LocalDateTime objects using the isBefore() and isAfter() methods?

  * a. Yes `Correct: The `isBefore()` and `isAfter()` methods are available in both LocalTime and LocalDateTime classes.`
  * b. No `Incorrect: The correct answer is yes.`【101†source】