### Step 01: Objects Revisited - State And Behavior

**Question 1: What defines an object's state?**

- A. Its methods `Incorrect: Methods define the behavior of an object, not its state.`
- B. Its behavior `Incorrect: Behavior is how an object acts, but it doesn't define its state.`
- C. Its attributes `Correct: The state of an object is determined by its attributes or properties.`

**Question 2: What delivers messages to an object?**

- A. Attributes `Incorrect: Attributes don't deliver messages; they store state information.`
- B. Methods `Correct: Methods are used to send messages to an object to perform certain actions.`
- C. Constructors `Incorrect: Constructors are used to initialize an object, not to send messages.`

**Question 3: What is the effect of behavior on an object's state?**

- A. No effect `Incorrect: Behavior, defined by methods, can affect an object's state.`
- B. Positive effect `Incorrect: The term "positive effect" is not precise in this context.`
- C. Negative effect `Incorrect: The term "negative effect" is not precise in this context.`

### Step 02: Managing class state

**Question 1: What corresponds to the state of a class?**

- A. Member variables `Correct: Member variables hold the state of an object of a class.`
- B. Methods `Incorrect: Methods define the behavior of the objects, not their state.`
- C. Constructors `Incorrect: Constructors are used to initialize an object, not to define its state.`

**Question 2: What is the purpose of constructors in a class?**

- A. To define behavior `Incorrect: Constructors are used to initialize an object, not to define its behavior.`
- B. To create objects `Correct: Constructors are used to create and initialize objects of a class.`
- C. To set attributes `Incorrect: Although constructors can be used to set attribute values, their primary purpose is to create objects.`

**Question 3: What is the purpose of the toString() method in a class?**

- A. To define behavior `Incorrect: The toString() method does not define behavior.`
- B. To create objects `Incorrect: The toString() method is used to provide a String representation of an object, not to create objects.`
- C. To provide a string representation of the object's state `Correct: The toString() method provides a string representation of an object's state.`

### Step 03: Augmenting Fan With Behavior

**Question 1: What is the state attribute that needs to be exposed to change by Fan object users?**

- A. make `Incorrect: "make" is not typically changed by users.`
- B. color `Incorrect: "color" is not typically changed by users.`
- C. isOn `Correct: Users need to be able to change whether the fan is on or off.`
- D. speed `Correct: Users need to be able to change the speed of the fan.`

**Question 2: What is the purpose of the switchOn() and switchOff() methods in the Fan class?**

- A. To toggle the isOn state attribute `Correct: These methods are used to change the "isOn" state attribute of a Fan object.`
- B. To toggle the speed state attribute `Incorrect: These methods don't directly change the speed state attribute.`
- C. To create a new Fan object `Incorrect: These methods are used to modify the state of an existing Fan object, not to create a new one.`

**Question 3: What is the

 purpose of the setSpeed() method in the Fan class?**

- A. To toggle the isOn state attribute `Incorrect: This method doesn't change the "isOn" state attribute.`
- B. To toggle the speed state attribute `Correct: This method is used to set the speed of the Fan.`
- C. To create a new Fan object `Incorrect: This method is used to modify the state of an existing Fan object, not to create a new one.`


**Step 04: Programming Exercise PE-OOP-01**

**Question 1: What are the state attributes of a Rectangle object?**
- A. Length and width `Correct: A rectangle is defined by its length and width.`
- B. Height and width `Incorrect: Height is not typically a characteristic used to define a rectangle.`
- C. Length and breadth `Incorrect: The term "breadth" is less commonly used to describe a rectangle's dimensions.`

**Question 2: What is the purpose of the area() method in the Rectangle class?**
- A. To calculate the perimeter of the rectangle `Incorrect: The area() method calculates the area, not the perimeter.`
- B. To calculate the area of the rectangle `Correct: The area() method calculates the area of a rectangle.`
- C. To set the length of the rectangle `Incorrect: The area() method doesn't set any attribute; it calculates a value.`

**Question 3: What is the purpose of the perimeter() method in the Rectangle class?**
- A. To calculate the perimeter of the rectangle `Correct: The perimeter() method calculates the perimeter of a rectangle.`
- B. To calculate the area of the rectangle `Incorrect: The perimeter() method calculates the perimeter, not the area.`
- C. To set the length of the rectangle `Incorrect: The perimeter() method doesn't set any attribute; it calculates a value.`

**Step 06: Understanding Object Composition**

**Question 1: What are the state attributes of the Fan class?**
- A) make, radius, color, isOn, speed `Correct: These are the attributes that define the state of a Fan object.`
- B) brand, diameter, hue, isRunning, velocity `Incorrect: These attributes may define similar features, but the specific names differ from those in the Fan class.`
- C) manufacturer, size, tone, isActive, rate `Incorrect: These attributes may define similar features, but the specific names differ from those in the Fan class.`

**Question 2: What is object composition?**
- A) Combining primitive types into a complex object `Incorrect: While this is a form of composition, it's not specific to object composition in OOP.`
- B) Creating multiple objects of the same type `Incorrect: This doesn't define object composition.`
- C) Combining different objects to create a more complex object `Correct: Object composition involves using different objects to build more complex ones.`

**Question 3: What is the purpose of constructors in object composition?**
- A) To create new objects of a class `Correct: Constructors are used to create and initialize new objects.`
- B) To modify the state of an object `Incorrect: Constructors initialize an object's state, not modify it after creation.`
- C) To add behaviors to an object `Incorrect: While constructors can assign methods, their main purpose is to create and initialize new objects.`

**Step 07: Programming Exercise PE-OOP-02**

**Question 1: What are the attributes of the Book class?**
- A) Id, Name, Author `Correct: These are the attributes that define the state of a Book object.`
- B) Title, Author, Description `Incorrect: While these could be valid attributes for a Book, they do not match the provided Book class structure.`
- C) Id, Title, Author `Incorrect: While these could be valid attributes for a Book, they do not match the provided Book class structure.`

**Question 2: What is the purpose of the Review class?**
- A) To manage Books `Incorrect: The Review class is meant to manage reviews, not

 books.`
- B) To manage Authors `Incorrect: The Review class is meant to manage reviews, not authors.`
- C) To manage reviews associated with a Book `Correct: The Review class is used to manage and associate reviews with a Book.`

**Question 3: What is the output of the following code?**

```java
Book book = new Book(123, "Object Oriented Programming With Java", "Ranga");
book.addReview(new Review(10, "Great Book", 4));
book.addReview(new Review(101, "Awesome", 5));
System.out.println(book);
```

- A) Book-123, Object Oriented Programming With Java, Ranga, [(Review-10, Great Book", 4), (Review-101, Awesome, 5)] `Correct: This is the expected output based on the provided code.`
- B) Book-123, Object Oriented Programming With Java, Ranga, [(10, Great Book, 4), (101, Awesome, 5)] `Incorrect: The output format includes the word "Review-" before the review IDs.`
- C) Book-123, Object Oriented Programming With Java, Ranga, [(Review-10, Great Book", 5), (Review-101, Awesome, 4)] `Incorrect: The review ratings do not match those given in the code.`

**Step 07: The Need For Inheritance**

**Question 1: What is Inheritance in Object Oriented Programming?**
- A) A mechanism of code reuse `Correct: Inheritance allows the reuse of code from one class in another.`
- B) A mechanism to create new objects `Incorrect: While inheritance can be part of creating new objects, it primarily refers to code reuse between classes.`
- C) A mechanism to modify existing objects `Incorrect: Inheritance involves classes and their relationships, not modifying existing objects.`

**Question 2: What is a superclass in Inheritance relationship?**
- A) A class that extends another class `Incorrect: A superclass is the class that gets extended, not the one that does the extending.`
- B) A class that inherits from another class `Incorrect: A superclass is the class that is inherited from, not the class that does the inheriting.`
- C) A class that is neither extended nor inherited `Incorrect: In the context of inheritance, a superclass is a class that is inherited from.`

**Question 3: How does a subclass access fields and methods of its superclass?**
- A) By using the keyword 'super' `Correct: In Java, the 'super' keyword is used to refer to the superclass of the current object.`
- B) By using the keyword 'this' `Incorrect: The 'this' keyword refers to the current object, not its superclass.`
- C) By using the keyword 'extends' `Incorrect: The 'extends' keyword is used to establish an inheritance relationship, not to access superclass members.`

**Step 12: Constructors, And Calling super()**

**Question 1: What does the super keyword do in Java?**
- a. Allows a subclass to access the attributes present in the superclass `Correct: The super keyword in Java is used to refer to the immediate parent class instance variable.`
- b. Creates a new instance of a superclass `Incorrect: The super keyword does not create new instances; it refers to the superclass.`
- c. Allows a superclass to access the attributes present in the subclass `Incorrect: The super keyword is used in the context of a subclass referring to its superclass, not the other way around.`

**Step 13: Multiple Inheritance, Reference Variables And instanceof**

**Question 1: Can a Java class directly inherit from two or more classes?**
- a. Yes `Incorrect: Java doesn't support multiple inheritance directly due to the "Diamond Problem".`
- b. No `Correct: A class in Java can directly inherit from only one class.`

**Question 2: What is the output of the Dog object's toString() method in Snippet-02?**
- a. Dog@23a6e47f `Correct: If not overridden, the toString() method returns the class name followed by the "@" sign and the unsigned hexadecimal representation of the hash code of the object.`
- b. Pet Groom `Incorrect: The output of toString() wouldn't be a string literal unless explicitly defined in the Dog class.`
- c. null `Incorrect: The toString() method will not return null unless explicitly defined to do so.`

**Question 3: What is the output of the instanceof operator when pet instanceof String is executed in Snippet-02?**
- a. Pet cannot be converted to java.lang.String `Correct: The 'instanceof' operator in Java is used to test whether an object is an instance of a specific class or not. In this case, 'pet' is not a String.`
- b. true `Incorrect: The pet is not an instance of String.`
- c. false `Incorrect: It throws a compile-time error because 'pet' can't be compared with 'String'.`

**Step 14: Introducing Abstract Classes**

**Question 1: What is an abstract method?**
- A) A method without any parameters `Incorrect: Abstract methods are defined by lack of implementation, not lack of parameters.`
- B) A method with a method definition `Incorrect: Abstract methods lack a method definition.`
- C) A method without a method definition `Correct: Abstract methods in Java are declared without a body.`

**Question 2: Can an abstract class be instantiated?**
- A) Yes `Incorrect: Abstract classes in Java cannot be instantiated.`
- B) No `Correct: Abstract classes can't be instantiated directly; they can only be subclassed.`

**Question 3: What is a concrete class?**
- A) A class that can be instantiated `Correct: A concrete class is a class that can be instantiated.`
- B) A class that cannot be instantiated `Incorrect: A concrete class, unlike an abstract class, can be instantiated.`
- C) A class with a method definition `Incorrect: While a concrete class does have defined methods, it's primarily characterized by its ability to be instantiated.`

**Step 15: Abstract Classes - Design Aspects**

**Question 1: What is the purpose of an abstract class?**
- A) To provide implementation for all its methods `Incorrect: Abstract classes don't provide full implementation; they contain one or more abstract methods.`
- B) To declare methods without providing implementation `Correct: Abstract classes declare methods without providing their implementation.`
- C) To create a hierarchy of classes `Incorrect: While abstract classes do play a role in class hierarchies, their primary purpose is to declare methods without providing implementation.`

**Question 2: What is the advantage of using an abstract class to create a recipe hierarchy?**
- A) It allows for the order of steps to be defined `Incorrect: The order of steps is not inherently defined by using an abstract class.`
- B) It allows for the implementation of each step to be defined by the sub-classes `Correct: Abstract classes allow subclasses to provide specific implementations of abstract methods.`
- C) It allows for the creation of multiple

 recipe types easily `Incorrect: While it might be true, the main advantage is in the encapsulation of a general process structure while enabling specific step implementations.`

**Question 3: Which design pattern is used in the recipe hierarchy example?**
- A) Observer pattern `Incorrect: The observer pattern is a design pattern where an object maintains a list of dependents and notifies them of any changes. It's not used here.`
- B) Decorator pattern `Incorrect: The decorator pattern allows behavior to be added to an individual object, either statically or dynamically, without affecting the behavior of other objects from the same class. It's not used here.`
- C) Template method pattern `Correct: The template method pattern is a behavioral design pattern that defines the program skeleton in an operation but defers some steps to subclasses.`

**Step 16: Abstract Classes - Puzzles**

**Question 1: Can an abstract class be created without any abstract member methods?**
- A) Yes `Correct: Abstract classes can exist without abstract methods. They can't be instantiated, but they can include actual method implementations.`
- B) No `Incorrect: It's not required for an abstract class to have abstract methods, although it's common.`

**Question 2: Can an abstract class have member variables?**
- A) Yes `Correct: Abstract classes can have member variables like any other classes.`
- B) No `Incorrect: Abstract classes, like any other class, can have member variables.`

**Question 3: Can an abstract class have non-abstract methods?**
- A) Yes `Correct: Abstract classes can have both abstract and non-abstract methods.`
- B) No `Incorrect: Abstract classes can include fully implemented (non-abstract) methods.`

**Step 17: Introducing Interfaces**

**Question 1: What is an interface in Java?**
- A) A class that provides implementation for all its methods `Incorrect: Interfaces do not provide implementation for any methods, only their signatures.`
- B) A class that declares methods without providing implementation `Incorrect: While interfaces do declare methods without implementation, they are not classes.`
- C) A class that cannot be instantiated but can be implemented by other classes `Correct: An interface can't be instantiated, but other classes can implement it to define the methods.`

**Question 2: Who provides the implementation of methods declared in an interface?**
- A) The interface itself `Incorrect: Interfaces in Java do not provide implementation for methods.`
- B) The implementing classes `Correct: The classes implementing the interface provide the method implementation.`
- C) The superclass of the interface `Incorrect: Interfaces do not have superclasses. Method implementation is provided by the classes implementing the interface.`

**Question 3: How can an interface be used to enforce a contract for its implementors?**
- A) By providing default implementations for its methods `Incorrect: While interfaces can provide default methods, the primary means of enforcing a contract is by declaring methods without providing implementation.`
- B) By declaring methods without providing implementation `Correct: Interfaces enforce a contract by declaring methods without providing implementation. The implementing classes are obliged to provide the implementation.`
- C) By creating a hierarchy of interfaces `Incorrect: While interfaces can inherit from other interfaces, the primary way they enforce a contract is by declaring methods without implementation.`

**Step 18: Using Interfaces To Design APIs**

**Question 1: Which of the following is not a way to ensure compatibility between teams working on different parts of an application?**
- a) Define an interface for the external team to implement `Incorrect: Defining interfaces is indeed a good way to ensure compatibility, as it sets the expectations for method signatures

.`
- b) Work on the parts of the application simultaneously `Incorrect: Working simultaneously doesn't inherently ensure compatibility; clear contracts and communication do.`
- c) Define an algorithm for the external team to implement directly into the application `Correct: This approach does not ensure compatibility as it lacks a defined contract for how components should interact.`

**Question 2: What is the purpose of defining an interface between two teams working on different parts of an application?**
- a) To allow teams to work independently without worrying about compatibility issues `Incorrect: While interfaces allow teams to work independently, they primarily serve to define a contract between the two teams.`
- b) To define a contract between the two teams `Correct: Interfaces provide a defined contract of methods, which facilitates the independent work of different teams on separate components.`
- c) To ensure that both teams use the same programming language `Incorrect: An interface doesn't enforce the use of a specific programming language, it's about defining the methods that classes implementing it should have.`

**Question 3: Which of the following is an implementation of the ComplexAlgorithm interface?**
- a) OneComplexAlgorithm `Incorrect: Without more context, we can't confirm if "OneComplexAlgorithm" is an implementation of the ComplexAlgorithm interface.`
- b) ActualComplexAlgorithm `Incorrect: Without more context, we can't confirm if "ActualComplexAlgorithm" is an implementation of the ComplexAlgorithm interface.`
- c) Both a and b `Correct: Assuming that both "OneComplexAlgorithm" and "ActualComplexAlgorithm" implement the ComplexAlgorithm interface.`

**Step 19: Interfaces - Puzzles And Interesting Facts**

**Question 1: Which of the following is true about interfaces in Java?**
- a) An interface can be extended by another interface `Correct: Interfaces can extend one or more other interfaces.`
- b) An implementation of an interface needs to implement all methods declared in the interface and its super interfaces `Incorrect: While an implementation class generally needs to implement all methods of an interface, if the class is abstract, it doesn't have to implement all methods.`
- c) Interfaces can have member variables `Incorrect: Interfaces can have constants (static final variables) but not regular member variables.`

**Question 2: Which of the following is not a way to provide a default implementation for a method in an interface?**
- a) Include the keyword "default" in the method signature `Incorrect: This is indeed one way to provide a default method in an interface.`
- b) Provide a body for the method in the interface definition `Incorrect: This is another way to provide a default method in an interface.`
- c) Override the method in the implementation class `Correct: Overriding the method in the implementation class is not providing a default implementation. It's providing a class-specific implementation.`

**Question 3: Why is providing default method implementations useful in building and extending frameworks?**
- a) It allows for a new method to be added to an interface without breaking the implementation classes `Correct: Default methods enable new functionality to be added to the interfaces of libraries and ensure binary compatibility with code written for older versions of those interfaces.`
- b) It ensures that all implementation classes have the same behavior for the default method `Incorrect: While this might happen, the main purpose is to allow extension without breaking existing implementations.`
- c) It reduces the amount of code needed to implement the interface `Incorrect: The amount of code is not necessarily reduced as the default method can still be overridden.`

**Step 20: abstract class And interface : A Comparison**

**Question 1: Which of the following is a primary use case for an interface?**
- a) Generalizing behavior by

 defining a set of methods that a class must implement `Correct: This is indeed a primary use case for interfaces.`
- b) Providing default implementations for methods `Incorrect: While interfaces can provide default method implementations, it's not their primary use case.`
- c) Defining member variables `Incorrect: Interfaces in Java can't define member variables (only constants).`

**Question 2: Which of the following is a primary use case for an abstract class?**
- a) Providing partial implementation for a class `Correct: This is a primary use case for abstract classes. They allow for the definition of both abstract and non-abstract methods.`
- b) Defining a contract for methods that a class must implement `Incorrect: This is a primary use case for interfaces, not abstract classes.`
- c) Extending multiple classes `Incorrect: In Java, a class (including abstract class) can't extend multiple classes directly.`

**Question 3: Which of the following can be instantiated?**
- a) An interface `Incorrect: Interfaces cannot be instantiated.`
- b) An abstract class `Incorrect: Abstract classes cannot be instantiated.`
- c) A concrete class `Correct: A concrete class, unlike interfaces or abstract classes, can be instantiated.`