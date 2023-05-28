### Question 1

What is a class in Object Oriented Programming?

  * A) An instance of an object. `Incorrect: An instance of a class is an object, not the class itself`.
  * B) A template for creating objects. `Correct: A class in Object Oriented Programming is a blueprint or template for creating objects`.
  * C) A function to perform actions. `Incorrect: Functions (methods in Java) can be part of a class, but they are not the definition of a class`【23†source】.

### Question 2

What are the two main components of an object in Object Oriented Programming?

  * A) State and Behavior. `Correct: An object in Object Oriented Programming consists of state (represented by attributes or properties) and behavior (represented by methods)`.
  * B) Template and Instance. `Incorrect: These terms relate to the concept of classes and objects, but they are not the components of an object`.
  * C) Functions and Variables. `Incorrect: While objects can contain variables (fields) and functions (methods), in the context of Object-Oriented Programming they are usually referred to as state (fields) and behavior (methods)`【24†source】.

### Question 3

Which of the following methods in a class sets the title attribute?

  * A) setTitle(String bookTitle). `Correct: This method follows the common naming convention for a setter method, which is used to set the value of a field`.
  * B) getTitle(). `Incorrect: This method is typically a getter method, used to retrieve the value of a field, not to set it`.
  * C) setBook(String title). `Incorrect: While the method name implies it could set some information related to a book, it's not clear that it sets the title`【25†source】.

### Question 4

In a class representing a vehicle, what is the purpose of the this keyword when used within a method?

  * A) To access a static variable. `Incorrect: The this keyword is used to refer to the current instance of a class, not to access static variables`.
  * B) To differentiate between a member variable and a method argument with the same name. `Correct: The this keyword is often used in this context to avoid confusion or name clashes between a field (member variable) and a parameter`.
  * C) To call a method within the same class. `Incorrect: While this can be used to call a method within the same class, its primary function is to reference the current object instance`【26†source】.

### Question 5

What is the primary purpose of using access modifiers such as public and private in Object-Oriented Programming?

  * A) To make code more readable. `Incorrect: While good use of access modifiers can make code more readable by clearly indicating which parts of the code are intended for external access, this is not their primary purpose`.
  * B) To control what external objects can access within a given object. `Correct: Access modifiers are primarily used to control the level of access other objects have to an object's fields and methods`.
  * C) To define the scope of a variable. `Incorrect: Access modifiers do influence scope, but their primary function is to control access, not to define scope`【27†source】.

### Question 6

What is the purpose of private keyword in Java?

  * A) To make a variable or method accessible only within the class. `Correct: The private access modifier restricts access to the field or method to the class in which it is declared`.
  * B) To make a variable or method accessible outside the class. `Incorrect: The private keyword makes a variable or method less accessible, not more. A public keyword would make a variable or method accessible outside the class`.
  * C) To make a variable or method static. `Incorrect: The keyword for making a variable or method static is static, not private`【28†source】.

### Question 7

What are the methods used to access and modify private member variables in a class?

  * A) Public methods. `Incorrect: While technically correct, since getter and setter methods are usually public, this is too broad of a term`.
  * B) Getter and Setter methods. `Correct: Getter and Setter methods are specifically used to access and modify private member variables in a class`.
  * C) Static methods. `Incorrect: While static methods can access and modify static variables, they are not typically used to access and modify instance variables`【29†source】.

### Question 8

What is the main principle that is violated when an object directly accesses the state of another object without using any methods?

  * A) Inheritance. `Incorrect: Inheritance is a principle that allows a class to inherit fields and methods from another class. It is not related to the direct access of another object's state`.
  * B) Encapsulation. `Correct: Encapsulation is the principle that an object's state should be accessed and modified through its methods, not directly`.
  * C) Polymorphism. `Incorrect: Polymorphism is a principle that allows a method to behave differently depending on the object that it is acting upon. It is not related to the direct access of another object's state`【30†source】.

### Question 9

In a Java class, what is the purpose of a getter method?

  * A) To modify the value of a private member variable. `Incorrect: A getter method is used to access or retrieve the value of a private member variable, not to modify it`.
  * B) To access the value of a private member variable. `Correct: A getter method's purpose is to access or retrieve the value of a private member variable`.
  * C) To perform a calculation with a private member variable. `Incorrect: While a getter method might be used as part of a calculation, its primary purpose is to retrieve the value of a variable, not to perform calculations`【31†source】.

### Question 10

Which of the following best describes the concept of state in Object-Oriented Programming?

  * A) The condition of an object at a given time, represented by member variables. `Correct: In Object-Oriented Programming, the state of an object is the data it contains at any given moment, represented by its member variables`.
  * B) The actions an object can perform, represented by methods. `Incorrect: This describes behavior, not state`.
  * C) The relationship between two objects. `Incorrect: While relationships between objects are a significant aspect of OOP, they don't define the state of an individual object`【32†source】.

### Question 11

What is the primary reason for using a getter method in a Java class?

  * A) To ensure that an object's member variables are accessed according to the encapsulation principle. `Correct: Getter methods are used to provide access to an object's data while still maintaining the principles of encapsulation`.
  * B) To define a new method that performs a calculation with an object's member variables. `Incorrect: While a getter method can be used as part of a calculation, that's not the primary reason to use one`.
  * C) To initialize an object's member variables with default values. `Incorrect: Initialization of member variables is usually done in constructors or with direct assignment, not with getter methods`【33†source】.

### Question 12

Which of the following correctly defines a getter method for a private member variable name in a Java class?

  * A) `Correct: This is the conventional way to define a getter method in Java. It's public, has a return type matching the variable type, and returns the private variable`.

```java
public String getName() {
  return name;
}
```
-   B) `Incorrect: This seems to be a setter method rather than a getter method, as it takes a parameter and assigns it to the variable`.

```java
public void getName(String newName) {
  name = newName;
}
```

-   C) `Incorrect: This method signature includes a parameter, which is unusual for a getter method. Additionally, it might create confusion between the method parameter and the class field`.

```java
public String getName(String name) {
  return this.name;
}
```

【34†source】.

### Question 13

What is the primary purpose of a getter method?

-   A) To modify the value of an object's private member variable. `Incorrect: Getter methods are used to access or return the value of a private member variable, not to modify it`.
-   B) To allow controlled access to an object's private member variable. `Correct: The primary purpose of a getter method is to provide controlled access to an object's private member variable`.
-   C) To set a default value for an object's private member variable. `Incorrect: Default values for an object's private member variables are usually set in a constructor or at the time of variable declaration, not in a getter method`【35†source】.

### Question 14

Consider the following code snippet. What will be the output?

```java 
public class MotorBike {
  private int speed;

  public int getSpeed() {
    return speed;
  }
}

public class MotorBikeRunner {
  public static void main(String[] args) {
    MotorBike bike = new MotorBike();
    System.out.println("Current Bike Speed is : " + bike.getSpeed());
  }
}
```

-   A) The code will not compile because the speed variable is not initialized. `Incorrect: In Java, instance variables are automatically initialized to a default value if not explicitly initialized. For integer variables, this default value is 0`.
-   B) The output will be: Current Bike Speed is : 0. `Correct: Since the speed variable is not explicitly initialized, its value is set to the default value of 0`.
-   C) The output will be: Current Bike Speed is : null. `Incorrect: Null is the default value for object references and not for primitive types like int`【36†source】.

### Question 15

What are the default values for object member variables when they are not explicitly initialized?

-   A) null for reference types, and the type's minimum value for primitive types. `Incorrect: While reference types are initialized to null, primitive types are not initialized to their minimum value`.
-   B) null for reference types, and 0 for primitive types. `Correct: Reference types are initialized to null and primitive types like int, char, float, boolean etc., are initialized to 0, '\u0000', 0.0f, and false respectively`.
-   C) The type's maximum value for primitive types, and null for reference types. `Incorrect: Primitive types are not initialized to their maximum value`【37†source】.

### Question 16

What is one of the advantages of encapsulation in Object-Oriented Programming?

-   A) Code Reuse. `Incorrect: Code reuse is associated more with inheritance and polymorphism than with encapsulation`.
-   B) Code Compression. `Incorrect: Encapsulation does not inherently lead to code compression`.
-   C) Code Simplification. `Correct: Encapsulation simplifies code by hiding its complexity. It allows the encapsulating object to change its internal implementation without affecting the code that uses the object`【38†source】.
### Question 17

In the given example, which method is responsible for setting the speed of a MotorBike object while ensuring it is not negative?

-   A) setSpeed(). `Correct: The setSpeed() method is typically responsible for setting the speed of a MotorBike object. It can include validation to ensure the speed is not negative`.
-   B) increaseSpeed(). `Incorrect: The increaseSpeed() method might increase the speed of the MotorBike object, but it is not responsible for directly setting the speed`.
-   C) decreaseSpeed(). `Incorrect: The decreaseSpeed() method might decrease the speed of the MotorBike object, but it is not responsible for directly setting the speed`【39†source】.

### Question 18

How can code duplication be reduced when implementing validation checks for the increaseSpeed() and decreaseSpeed() methods?

-   A) By using separate validation checks for each method. `Incorrect: Using separate validation checks for each method would actually lead to code duplication`.
-   B) By calling the setSpeed() method with appropriate parameters inside both methods. `Correct: By calling the setSpeed() method (which could contain the necessary validation checks) from within the increaseSpeed() and decreaseSpeed() methods, we can reuse the validation logic and thus reduce code duplication`.
-   C) By using a global validation check. `Incorrect: Using a global validation check can be problematic as it may not apply universally to all situations and can lead to code coupling`【40†source】.

### Question 19

What is the purpose of encapsulation in the context of protecting an object's state?

-   A) To prevent other objects from directly accessing the object's state. `Correct: Encapsulation is a principle of Object-Oriented Programming that helps protect an object's state by hiding its data (fields) and providing methods for data access and manipulation`.
-   B) To allow other objects to directly access the object's state. `Incorrect: Encapsulation does not allow other objects to directly access the object's state, instead, it provides controlled access via methods`.
-   C) To create a new object with the same state as the original object. `Incorrect: Encapsulation does not deal with creating new objects with the same state as existing ones`【41†source】.

### Question 20

In the given example, which method is used to start the MotorBike?

-   A) begin(). `Incorrect: The method name to start the MotorBike is not given in the question. However, in conventional programming practice, methods such as "start" or "run" are often used`.
-   B) start(). `Correct: In common practice, the method to start a MotorBike or similar objects could be named "start"`.
-   C) initiate(). `Incorrect: Although "initiate" could be a valid method name, it's not as commonly used as "start"`【42†source】.

### Question 22

What is the purpose of a constructor in a Java class?

-   a) To create an instance of the class with the specified initial state. `Correct: A constructor in Java is used to create an instance of a class and can initialize the state of the object`.
-   b) To perform calculations on the class variables. `Incorrect: While constructors can contain code that performs calculations, this is not their primary purpose`.
-   c) To modify the state of an object after it has been created. `Incorrect: Constructors are used to initialize an object when it is created, not to modify its state after creation`.
-   d) To destroy an object when it is no longer needed. `Incorrect: In Java, destruction of objects is managed by the Garbage Collector, not by constructors`【43†source】.

### Question 6

What is a default constructor in Java?

-   a) A constructor that is automatically provided by the compiler if no other constructors are defined. `Correct: If no constructors are defined in a Java class, the compiler automatically provides a default constructor with no arguments`.
-   b) A constructor with a single argument. `Incorrect: The number of arguments has no bearing on whether a constructor is considered default`.
-   c) A constructor that takes an unlimited number of arguments. `Incorrect: A default constructor does not take an unlimited number of arguments, it takes no arguments`.
-   d) A constructor that initializes all instance variables to their default values. `Incorrect: While a default constructor can be used to initialize variables, its defining feature is that it is provided by the compiler when no other constructors are defined`【44†source】.

### Question 23

What is a constructor in Java?

-   a) A special method with the same name as the class. `Correct: A constructor is a special method in a class, with the same name as the class`.
-   b) A method that returns a value. `Incorrect: Constructors do not return a value`.
-   c) A method that can be called directly. `Incorrect: Constructors are not called directly; they are called when an instance of the class is created using the new keyword`.
-   d) A method that can only accept zero arguments. `Incorrect: Constructors can take any number of arguments, including zero`【45†source】.

### Question 24

How is a constructor invoked in Java?

-   a) By calling the method directly. `Incorrect: Constructors are not called directly, they are invoked when an instance of the class is created`.
-   b) By using the new keyword while creating an object of the class. `Correct: Constructors are invoked using the new keyword when an object of the class is created`.
-   c) By declaring the constructor as static. `Incorrect: Static methods belong to the class, not the instance of the class. Constructors are not static and cannot be declared as such`.
-   d) By using the this keyword while creating an object of the class. `Incorrect: The this keyword refers to the current instance of the class and is not used to invoke a constructor`【46†source】.

### Question 25

Can a constructor accept multiple arguments in Java?

-   a) No, a constructor can only accept zero or one argument. `Incorrect: A constructor in Java can accept any number of arguments`.
-   b) Yes, a constructor can accept multiple arguments. `Correct: A constructor in Java can accept multiple arguments`.
-   c) Only the default constructor can accept multiple arguments. `Incorrect: The default constructor does not take any arguments`.
-   d) It depends on the access modifiers of the constructor. `Incorrect: The number of arguments a constructor can take does not depend on its access modifiers`【47†source】.

### Question 26

What is a default constructor in Java?

-   a) A constructor that accepts no arguments. `Correct: A default constructor is a no-argument constructor`.
-   b) A constructor that is defined by the programmer. `Incorrect: A default constructor is provided by the compiler if no constructor is defined by the programmer`.
-   c) A constructor that is generated by the compiler when no constructor is defined. `Correct: If no constructor is defined in the class, the Java compiler automatically provides a default constructor`.
-   d) A constructor that is called automatically when an object is created. `Incorrect: While all constructors are invoked when an object is created, not all are default constructors`【48†source】.

### Question 27

What happens when a class has no constructor defined in Java?

-   a) The code fails to compile. `Incorrect: If a class in Java does not have a constructor defined, the code will still compile`.
-   b) A default constructor is generated by the compiler. `Correct: If no constructor is explicitly defined in a Java class, the compiler automatically generates a default constructor`.
-   c) The code compiles and runs without any issues. `Incorrect: While the code would still compile and could run without issues, this answer is misleading because it does not mention the automatic generation of a default constructor`.
-   d) The class cannot be instantiated. `Incorrect: Even if a constructor is not defined, a class can still be instantiated using the default constructor`【49†source】.