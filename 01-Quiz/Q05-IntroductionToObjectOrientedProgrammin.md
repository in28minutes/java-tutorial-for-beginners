## Step 1

**Question 1:** What is a class in Object Oriented Programming?

- A. An instance of an object 
- B. A template for creating objects 
- C. A function to perform actions

_Answer: B_

**Question 2:** What are the two main components of an object in Object Oriented Programming?

- A. State and Behavior 
- B. Template and Instance 
- C. Functions and Variables

_Answer: A_

## Step 4, 5, 6, 7

**Question 3:** Which of the following methods in a class sets the title attribute?

- A. `setTitle(String bookTitle)` 
- B. `getTitle()` 
- C. `setBook(String title)`

_Answer: A_

**Question 4:** In a class representing a vehicle, what is the purpose of the `this` keyword when used within a method?

- A. To access a static variable 
- B. To differentiate between a member variable and a method argument with the same name 
- C. To call a method within the same class

_Answer: B_

**Question 5:** What is the primary purpose of using access modifiers such as `public` and `private` in Object-Oriented Programming?

- A. To make code more readable 
- B. To control what external objects can access within a given object 
- C. To define the scope of a variable

_Answer: B_

**Question 6:** What is the purpose of `private` keyword in Java?

- A. To make a variable or method accessible only within the class 
- B. To make a variable or method accessible outside the class 
- C. To make a variable or method static

_Answer: A_

**Question 7:** What are the methods used to access and modify private member variables in a class?

- A. Public methods 
- B. Getter and Setter methods 
- C. Static methods

_Answer: B_

**Question 8:** What is the main principle that is violated when an object directly accesses the state of another object without using any methods?

- A. Inheritance 
- B. Encapsulation 
- C. Polymorphism

_Answer: B_

**Question 9:** In a Java class, what is the purpose of a getter method?

- A. To modify the value of a private member variable 
- B. To access the value of a private member variable 
- C. To perform a calculation with a private member variable

_Answer: B_

**Question 10:** Which of the following best describes the concept of state in Object-Oriented Programming?

- A. The condition of an object at a given time, represented by member variables 
- B. The actions an object can perform, represented by methods 
- C. The relationship between two objects

_Answer: A_

**Question 11:** What is the primary reason for using a getter method in a Java class?

- A. To ensure that an object's member variables are accessed according to the encapsulation principle 
- B. To define a new method that performs a calculation with an object's member variables 
- C. To initialize an object's member variables with default values

_Answer: A_

**Question 12:** Which of the following correctly defines a getter method for a private member variable `name` in a Java class?

- A.

```
public String getName() {
  return name;
}
```

- B.

```
public void getName(String newName) {
  name = newName;
}
```

- C.

```
public String getName(String name) {
  return this.name;
}
```

_Answer: A_

## Step 8,9 

**Question 13:** What is the primary purpose of a getter method?

- A. To modify the value of an object's private member variable 
- B. To allow controlled access to an object's private member variable 
- C. To set a default value for an object's private member variable

_Answer: B_

**Question 14:** Consider the following code snippet. What will be the output?

MotorBike.java

```
public class MotorBike {
  private int speed;

  public int getSpeed() {
    return speed;
  }
}
```

MotorBikeRunner.java

```
public class MotorBikeRunner {
  public static void main(String[] args) {
    MotorBike bike = new MotorBike();
    System.out.println("Current Bike Speed is : " + bike.getSpeed());
  }
}
```

- A. The code will not compile because the speed variable is not initialized 
- B. The output will be: `Current Bike Speed is : 0` 
- C. The output will be: `Current Bike Speed is : null`

_Answer: B_

**Question 15:** What are the default values for object member variables when they are not explicitly initialized?

- A. `null` for reference types, and the type's minimum value for primitive types 
- B. `null` for reference types, and 0 for primitive types 
- C. The type's maximum value for primitive types, and `null` for reference types

_Answer: B_

## Step 10, 11

#### Question 16

What is one of the advantages of encapsulation in Object-Oriented Programming? - A. Code Reuse 
- B. Code Compression 
- C. Code Simplification

**Answer: A. Code Reuse**

#### Question 17

In the given example, which method is responsible for setting the speed of a MotorBike object while ensuring it is not negative? 
- A. setSpeed() 
- B. increaseSpeed() 
- C. decreaseSpeed()

**Answer: A. setSpeed()**

#### Question 18

How can code duplication be reduced when implementing validation checks for the `increaseSpeed()` and `decreaseSpeed()` methods? 
- A. By using separate validation checks for each method 
- B. By calling the `setSpeed()` method with appropriate parameters inside both methods 
- C. By using a global validation check

**Answer: B. By calling the `setSpeed()` method with appropriate parameters inside both methods**

#### Question 19

What is the purpose of encapsulation in the context of protecting an object's state? 
- A. To prevent other objects from directly accessing the object's state 
- B. To allow other objects to directly access the object's state 
- C. To create a new object with the same state as the original object

**Answer: A. To prevent other objects from directly accessing the object's state**

#### Question 20

In the given example, which method is used to start the MotorBike? 
- A. begin() 
- B. start() 
- C. initiate()

**Answer: B. start()**

## Step 13

**Question 21: What is the purpose of a constructor in a Java class?**

- a) To create an instance of the class with the specified initial state 
- b) To perform calculations on the class variables 
- c) To modify the state of an object after it has been created 
- d) To destroy an object when it is no longer needed

**Answer: a) To create an instance of the class with the specified initial state**

**Question 6: What is a default constructor in Java?**

- a) A constructor that is automatically provided by the compiler if no other constructors are defined 
- b) A constructor with a single argument 
- c) A constructor that takes an unlimited number of arguments 
- d) A constructor that initializes all instance variables to their default values

**Answer: a) A constructor that is automatically provided by the compiler if no other constructors are defined**