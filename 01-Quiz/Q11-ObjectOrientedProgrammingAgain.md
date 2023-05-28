## Step 01: Objects Revisited - State And Behavior


//What defines an object's state?
- a) Its methods
- b) Its behavior
- c) Its attributes

Answer: c

//What delivers messages to an object?
- a) Attributes
- b) Methods
 -c) Constructors

Answer: b

//What is the effect of behavior on an object's state?
- a) No effect
 -b) Positive effect
 -c) Negative effect

Answer: b` 

## Step 02: Managing class state

What corresponds to the state of a class?
- a) Member variables
- b) Methods
- c) Constructors

Answer: a

//What is the purpose of constructors in a class?
- a) To define behavior
 - b) To create objects
- c) To set attributes

Answer: b

//What is the purpose of the toString() method in a class?
- a) To define behavior
- b) To create objects
- c) To provide a string representation of the object's state

Answer: c

## Step 03: Augmenting Fan With Behavior



//What is the state attribute that needs to be exposed to change by Fan object users?
- a) make
- b) color
- c) isOn
- d) speed

Answer: c, d

//What is the purpose of the switchOn() and switchOff() methods in the Fan class?
- a) To toggle the isOn state attribute
- b) To toggle the speed state attribute
- c) To create a new Fan object

Answer: a

//What is the purpose of the setSpeed() method in the Fan class?
- a) To toggle the isOn state attribute
- b) To toggle the speed state attribute
- c) To create a new Fan object

Answer: b

## Step 04: Programming Exercise PE-OOP-01

//What are the state attributes of a Rectangle object?
- a) Length and width
- b) Height and width
- c) Length and breadth

Answer: a

//What is the purpose of the area() method in the Rectangle class?
- a) To calculate the perimeter of the rectangle
- b) To calculate the area of the rectangle
- c) To set the length of the rectangle

Answer: b

//What is the purpose of the perimeter() method in the Rectangle class?
- a) To calculate the perimeter of the rectangle
- b) To calculate the area of the rectangle
- c) To set the length of the rectangle

Answer: a


### Step 06: Understanding Object Composition

Question 1: What are the state attributes of the Fan class?

-   A) make, radius, color, isOn, speed
-   B) brand, diameter, hue, isRunning, velocity
-   C) manufacturer, size, tone, isActive, rate

Answer: A) make, radius, color, isOn, speed

Question 2: What is object composition?

-   A) Combining primitive types into a complex object
-   B) Creating multiple objects of the same type
-   C) Combining different objects to create a more complex object

Answer: C) Combining different objects to create a more complex object

Question 3: What is the purpose of constructors in object composition?

-   A) To create new objects of a class
-   B) To modify the state of an object
-   C) To add behaviors to an object

Answer: A) To create new objects of a class

### Step 07: Programming Exercise PE-OOP-02

Question 1: What are the attributes of the Book class?

-   A) Id, Name, Author
-   B) Title, Author, Description
-   C) Id, Title, Author

Answer: A) Id, Name, Author

Question 2: What is the purpose of the Review class?

-   A) To manage Books
-   B) To manage Authors
-   C) To manage reviews associated with a Book

Answer: C) To manage reviews associated with a Book

Question 3: What is the output of the following code?

```
Book book = new Book(123, "Object Oriented Programming With Java", "Ranga");
book.addReview(new Review(10, "Great Book", 4));
book.addReview(new Review(101, "Awesome", 5));
System.out.println(book);
```

-   A) Book-123, Object Oriented Programming With Java, Ranga, [(Review-10, Great Book", 4), (Review-101, Awesome, 5)]
-   B) Book-123, Object Oriented Programming With Java, Ranga, [(10, Great Book, 4), (101, Awesome, 5)]
-   C) Book-123, Object Oriented Programming With Java, Ranga, [(Review-10, Great Book", 5), (Review-101, Awesome, 4)]

Answer: A) Book-123, Object Oriented Programming With Java, Ranga, [(Review-10, Great Book", 4), (Review-101, Awesome, 5)]

### Step 07: The Need For Inheritance

Question 1: What is Inheritance in Object Oriented Programming?

-   A) A mechanism of code reuse
-   B) A mechanism to create new objects
-   C) A mechanism to modify existing objects

Answer: A) A mechanism of code reuse

Question 2: What is a superclass in Inheritance relationship?

-   A) A class that extends another class
-   B) A class that inherits from another class
-   C) A class that is neither extended nor inherited

Answer: B) A class that is inherited from another class

Question 3: How does a subclass access fields and methods of its superclass?

-   A) By using the keyword 'super'
-   B) By using the keyword 'this'
-   C) By using the keyword 'extends'

Answer: A) By using the keyword 'super'


### Step 09: Quiz

1.  What is the Object class in Java?

-   A. A user-defined class.
-   B. A package in Java system.
-   C. A built-in Java library class.

Answer: C

2.  Which methods of the Object class are available to objects of the Person class?

-   A. toString(), hashCode(), and notify().
-   B. setString(), setInt(), and notify().
-   C. toString(), getName(), and setEmail().

Answer: A

3.  What happens when the statement `System.out.println(person)` is executed in the StudentRunner.java file?

-   A. The `toString()` method of the Person class is called.
-   B. The `hashCode()` method of the Person class is called.
-   C. The `notify()` method of the Person class is called.

Answer: A


# Step 12: Constructors, And Calling super()

**Question 1**: What does the `super` keyword do in Java?  
a. Allows a subclass to access the attributes present in the superclass  
b. Creates a new instance of a superclass  
c. Allows a superclass to access the attributes present in the subclass

**Answer**: a. Allows a subclass to access the attributes present in the superclass

**Question 2**: What is the output of the `EmployeeRunner` class in Snippet-01?  
a. Employee Name: null, Email: null, Phone Number: null, Title: null, Employer: null, Employee Grade: , Salary: null  
b. Employee Name: Ranga, Email: [in28minutes@gmail.com](mailto:in28minutes@gmail.com), Phone Number: 123-456-7890, Title: Programmer Analyst, Employer: In28Minutes, Employee Grade: A, Salary: 50000.0000  
c. Error: super-class default constructor not found

**Answer**: b. Employee Name: Ranga, Email: [in28minutes@gmail.com](mailto:in28minutes@gmail.com), Phone Number: 123-456-7890, Title: Programmer Analyst, Employer: In28Minutes, Employee Grade: A, Salary: 50000.0000

**Question 3**: What is the output of the `EmployeeRunner` class in Snippet-10 after calling `setSalary()`?  
a. Employee Name: null, Email: null, Phone Number: null, Title: null, Employer: null, Employee Grade: , Salary: null  
b. Employee Name: Ranga, Email: [in28minutes@gmail.com](mailto:in28minutes@gmail.com), Phone Number: 123-456-7890, Title: Programmer Analyst, Employer: In28Minutes, Employee Grade: A, Salary: null  
c. Employee Name: Ranga, Email: [in28minutes@gmail.com](mailto:in28minutes@gmail.com), Phone Number: 123-456-7890, Title: Programmer Analyst, Employer: In28Minutes, Employee Grade: A, Salary: 50000.0000

**Answer**: c. Employee Name: Ranga, Email: [in28minutes@gmail.com](mailto:in28minutes@gmail.com), Phone Number: 123-456-7890, Title: Programmer Analyst, Employer: In28Minutes, Employee Grade: A, Salary: 50000.0000

# Step 13: Multiple Inheritance, Reference Variables And instanceof

**Question 1**: Can a Java class directly inherit from two or more classes?  
a. Yes  
b. No

**Answer**: b. No

**Question 2**: What is the output of the `Dog` object's `toString()` method in Snippet-02?  
a. Dog@23a6e47f  
b. Pet Groom  
c. null

**Answer**: a. Dog@23a6e47f

**Question 3**: What is the output of the `instanceof` operator when `pet instanceof String` is executed in Snippet-02?  
a. Pet cannot be converted to java.lang.String  
b. true  
c. false

**Answer**: a. Pet cannot be converted to java.lang.String

# Step 14: Introducing Abstract Classes. Here are three questions with answer options:

1.  What is an abstract method? 
- A) A method without any parameters 
- B) A method with a method definition 
- C) A method without a method definition 
 Answer: C
    
2.  Can an abstract class be instantiated? A) Yes B) No 
Answer: B
    
3.  What is a concrete class? 
- A) A class that can be instantiated 
- B) A class that cannot be instantiated 
- C) A class with a method definition 
Answer: A
    




## Step 14: Introducing Abstract Classes

1. What is an abstract method?
   A) A method without any parameters
   B) A method with a method definition
   C) A method without a method definition
   Answer: C

2. Can an abstract class be instantiated?
   A) Yes
   B) No
   Answer: B

3. What is a concrete class?
   A) A class that can be instantiated
   B) A class that cannot be instantiated
   C) A class with a method definition
   Answer: A`

### Step 15: Abstract Classes - Design Aspects

**Question 1:** What is the purpose of an abstract class?

-   A) To provide implementation for all its methods
-   B) To declare methods without providing implementation
-   C) To create a hierarchy of classes

**Answer:** B) To declare methods without providing implementation

**Question 2:** What is the advantage of using an abstract class to create a recipe hierarchy?

-   A) It allows for the order of steps to be defined
-   B) It allows for the implementation of each step to be defined by the sub-classes
-   C) It allows for the creation of multiple recipe types easily

**Answer:** B) It allows for the implementation of each step to be defined by the sub-classes

**Question 3:** Which design pattern is used in the recipe hierarchy example?

-   A) Observer pattern
-   B) Decorator pattern
-   C) Template method pattern

**Answer:** C) Template method pattern

### Step 16: Abstract Classes - Puzzles

**Question 1:** Can an abstract class be created without any abstract member methods?

-   A) Yes
-   B) No

**Answer:** A) Yes

**Question 2:** Can an abstract class have member variables?

-   A) Yes
-   B) No

**Answer:** A) Yes

**Question 3:** Can an abstract class have non-abstract methods?

-   A) Yes
-   B) No

**Answer:** A) Yes

### Step 17: Introducing Interfaces

**Question 1:** What is an interface in Java?

-   A) A class that provides implementation for all its methods
-   B) A class that declares methods without providing implementation
-   C) A class that cannot be instantiated but can be implemented by other classes

**Answer:** C) A class that cannot be instantiated but can be implemented by other classes

**Question 2:** Who provides the implementation of methods declared in an interface?

-   A) The interface itself
-   B) The implementing classes
-   C) The superclass of the interface

**Answer:** B) The implementing classes

**Question 3:** How can an interface be used to enforce a contract for its implementors?

-   A) By providing default implementations for its methods
-   B) By declaring methods without providing implementation
-   C) By creating a hierarchy of interfaces

**Answer:** B) By declaring methods without providing implementation


### Step 18: Using Interfaces To Design APIs

Which of the following is not a way to ensure compatibility between teams working on different parts of an application?

- a) Define an interface for the external team to implement 
- b) Work on the parts of the application simultaneously 
- c) Define an algorithm for the external team to implement directly into the application

Answer: c

----------

What is the purpose of defining an interface between two teams working on different parts of an application?

- a) To allow teams to work independently without worrying about compatibility issues 
- b) To define a contract between the two teams 
- c) To ensure that both teams use the same programming language

Answer: b

----------

Which of the following is an implementation of the ComplexAlgorithm interface?

- a) OneComplexAlgorithm 
- b) ActualComplexAlgorithm 
- c) Both a and b

Answer: b

### Step 19: Interfaces - Puzzles And Interesting Facts

Which of the following is true about interfaces in Java?

- a) An interface can be extended by another interface 
- b) An implementation of an interface needs to implement all methods declared in the interface and its super interfaces 
- c) Interfaces can have member variables

Answer: a

----------

Which of the following is not a way to provide a default implementation for a method in an interface?

- a) Include the keyword "default" in the method signature 
- b) Provide a body for the method in the interface definition 
- c) Override the method in the implementation class

Answer: c

----------

Why is providing default method implementations useful in building and extending frameworks?

- a) It allows for a new method to be added to an interface without breaking the implementation classes 
- b) It ensures that all implementation classes have the same behavior for the default method 
- c) It reduces the amount of code needed to implement the interface

Answer: a

### Step 20: abstract class And interface : A Comparison

Which of the following is a primary use case for an interface?

- a) Generalizing behavior by creating a super class 
- b) Defining a contract between two software components 
- c) Implementing multiple interfaces in a single class

Answer: b

----------

Which of the following is a syntactical difference between an interface and an abstract class?

- a) An interface can have member variable declarations, but an abstract class cannot 
- b) An abstract class can have private methods, but an interface cannot have any methods declared as private 
- c) An interface can extend multiple interfaces, but an abstract class can only extend one class or abstract class

Answer: c

----------

What is the purpose of creating an abstract class?

- a) To define a contract between two software components 
- b) To generalize behavior by creating a super class 
- c) To provide a default implementation for a method in an interface

Answer: b
