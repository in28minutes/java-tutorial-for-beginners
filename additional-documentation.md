## Section 5: Introduction to Java Platform

#### **Group 1: Steps 01 and 07**
- **Step 01 - Overview Of Java Platform - An Introduction**
- **Step 07 - JDK vs JRE vs JVM**

**Why Grouped:**
Both steps provide an overview of Java, covering the foundational concepts of the platform, including bytecode, the Java Virtual Machine (JVM), and the distinctions between the JDK, JRE, and JVM.

### **Puzzle:** (OPTIONAL)
- Write a simple explanation of how Java achieves platform independence using bytecode and the JVM.

- Can you describe what happens from the moment you compile a Java program to when it is run on a specific operating system?

### **New Quiz Questions:**

1. **What is bytecode?**
   - A) Machine code for Windows
   - B) Code that runs directly on a CPU
   - C) An intermediate representation understood by the JVM (Answer: C)

2. **What does the JDK contain that the JRE does not?**
   - A) Debugging tools and the compiler (Answer: A)
   - B) The JVM
   - C) Java libraries

3. **Which component is responsible for converting bytecode to machine-specific instructions?**
   - A) JDK
   - B) JVM (Answer: B)
   - C) Compiler

### **Fun Fact:**
- **Did you know?** Java was originally developed by James Gosling at Sun Microsystems and was initially called "Oak" after an oak tree that stood outside Gosling's office. It was later renamed to "Java" after the Indonesian coffee.

---

#### **Group 2: Steps 02, 03, 04, 05, and 06**
- **Step 02 - Java Class and Object - First Look**
- **Step 03 - Create a Method in a Java Class**
- **Step 04 - Create and Compile Planet.java Class**
- **Step 05 - Run Planet Class with Java - Using a main method**
- **Step 06 - Play and Learn with Planet Class**

**Why Grouped:**
These steps introduce learners to creating a basic Java class (`Planet`), adding methods, compiling the code, running it with the `main()` method, and experimenting with the class. These topics flow logically as they guide learners through hands-on programming with Java.

### **Puzzle 1: Creating a Class and Objects**
- Create a class called `Planet` with a method `revolve()` that prints "Revolving around the sun." Instantiate two objects, `earth` and `mars`, and call the `revolve()` method for both objects.

**Code Snippet:**
```java
class Planet {
    void revolve() {
        System.out.println("Revolving around the sun.");
    }
}

public class Main {
    public static void main(String[] args) {
        Planet earth = new Planet();
        Planet mars = new Planet();
        earth.revolve();
        mars.revolve();
    }
}
```

**Expected Output:**
```
Revolving around the sun.
Revolving around the sun.
```

### **Puzzle 2: Add Properties to the Planet Class**
- Extend the `Planet` class to have two properties: `name` and `diameter`. Write a method `displayInfo()` that prints the name and diameter of the planet. Create instances for Earth and Mars with appropriate data.

**Code Snippet:**
```java
class Planet {
    String name;
    double diameter;

    Planet(String name, double diameter) {
        this.name = name;
        this.diameter = diameter;
    }

    void displayInfo() {
        System.out.println(name + " has a diameter of " + diameter + " kilometers.");
    }
}

public class Main {
    public static void main(String[] args) {
        Planet earth = new Planet("Earth", 12742);
        Planet mars = new Planet("Mars", 6779);
        earth.displayInfo();
        mars.displayInfo();
    }
}
```

**Expected Output:**
```
Earth has a diameter of 12742 kilometers.
Mars has a diameter of 6779 kilometers.
```

### **New Quiz Questions:**

1. **What is a Java class?**
   - A) A template for creating objects (Answer: A)
   - B) A block of code that runs methods
   - C) A part of the JVM

2. **How do you create an object in Java?**
   - A) Using the `new` keyword (Answer: A)
   - B) Using the `class` keyword
   - C) By declaring an array

3. **What is the purpose of the `main()` method?**
   - A) It compiles the program.
   - B) It is the entry point of the program (Answer: B).
   - C) It defines the class.

### **Fun Fact:**
- **Did you know?** The Java `main()` method is always `public static void main(String[] args)`, and if it's not written exactly like this, Java won't recognize it as the entry point of the program.

---

### Additional Coding Exercises:

### **Exercise 1: Create a "Device" Class with Multiple Methods and Compile It**

#### **Problem:**
Create a Java class called `Device` that represents different electronic devices. The class should:

- Have attributes for the `deviceName`, `brand`, and `powerStatus` (on/off).

- Implement methods:

  - `turnOn()` that prints "Device is turned ON."

  - `turnOff()` that prints "Device is turned OFF."

  - `showDetails()` that prints the device's name and brand.

- Create instances of the `Device` class for a few devices like "Smartphone", "Laptop", and "Tablet". Turn these devices on and off, and display their details.

Once you've created the class, follow these steps:

1. Save the file as `Device.java`.

2. Compile the file using `javac Device.java`.

3. Run the program using `java Device`.

#### **Code:**

```java
public class Device {
    // Attributes of the Device class
    String deviceName;
    String brand;
    boolean powerStatus;

    // Constructor to initialize the device
    public Device(String deviceName, String brand) {
        this.deviceName = deviceName;
        this.brand = brand;
        this.powerStatus = false; // default is off
    }

    // Method to turn on the device
    public void turnOn() {
        if (!powerStatus) {
            powerStatus = true;
            System.out.println(deviceName + " is turned ON.");
        } else {
            System.out.println(deviceName + " is already ON.");
        }
    }

    // Method to turn off the device
    public void turnOff() {
        if (powerStatus) {
            powerStatus = false;
            System.out.println(deviceName + " is turned OFF.");
        } else {
            System.out.println(deviceName + " is already OFF.");
        }
    }

    // Method to show details of the device
    public void showDetails() {
        System.out.println("Device Name: " + deviceName + ", Brand: " + brand);
    }

    // Main method to test the Device class
    public static void main(String[] args) {
        // Creating instances of Device class
        Device smartphone = new Device("Smartphone", "Samsung");
        Device laptop = new Device("Laptop", "Dell");
        Device tablet = new Device("Tablet", "Apple");

        // Turning devices on and showing details
        smartphone.turnOn();
        smartphone.showDetails();

        laptop.turnOn();
        laptop.showDetails();

        tablet.turnOn();
        tablet.showDetails();

        // Turning devices off
        smartphone.turnOff();
        laptop.turnOff();
        tablet.turnOff();
    }
}
```

#### **Explanation:**

**Attributes (deviceName, brand, powerStatus)**: These are the properties of the Device class that hold information about the device’s name, brand, and whether it’s ON or OFF.

**Constructor**: The constructor (`Device()`) initializes each object with a specific `deviceName` and `brand`, and sets the `powerStatus` to OFF by default.

**Methods**:
- `turnOn()`: Turns on the device by setting `powerStatus` to `true`.

- `turnOff()`: Turns off the device by setting `powerStatus` to `false`.

- `showDetails()`: Displays the device's name and brand.

**Main method**: This is where objects are created, methods are called, and the program is run.

#### **Steps to Compile and Run:**

1. Save the file as `Device.java`.

2. In the terminal, compile the code:

   ```
   javac Device.java
   ```

3. Run the code:

   ```
   java Device
   ```

#### **Output:**

```java
Smartphone is turned ON.
Device Name: Smartphone, Brand: Samsung
Laptop is turned ON.
Device Name: Laptop, Brand: Dell
Tablet is turned ON.
Device Name: Tablet, Brand: Apple
Smartphone is turned OFF.
Laptop is turned OFF.
Tablet is turned OFF.
```

---

### **Exercise 2: Create a "Game" Class with a Scoring System**

#### **Problem:**

Write a class called `Game` that models a simple game system. The class should:

- Have attributes for `gameName`, `maxScore`, and `currentScore`.

- Include methods to:

  - `startGame()` to initialize the game.

  - `playGame()` to increase the current score.

  - `endGame()` to print the game details and final score.

- Create instances for games like "Soccer", "Basketball", and "Tennis". Start each game, play to increase the score, and then end the game by displaying the final score.

#### Compile and run the program after saving the file.

#### **Code:**
```java
public class Game {
    // Attributes for the Game class
    String gameName;
    int maxScore;
    int currentScore;

    // Constructor to initialize the game
    public Game(String gameName, int maxScore) {
        this.gameName = gameName;
        this.maxScore = maxScore;
        this.currentScore = 0;
    }

    // Method to start the game
    public void startGame() {
        System.out.println("Starting the game: " + gameName);
        currentScore = 0; // Reset the score to 0
    }

    // Method to play the game and increase score
    public void playGame() {
        if (currentScore < maxScore) {
            currentScore += 10; // Increment score by 10
            System.out.println("Playing " + gameName + "... Current Score: " + currentScore);
        } else {
            System.out.println("Game Over! Maximum score reached.");
        }
    }

    // Method to end the game and show the final score
    public void endGame() {
        System.out.println("Ending the game: " + gameName + ". Final Score: " + currentScore);
    }

    // Main method to test the Game class
    public static void main(String[] args) {
        // Creating instances of Game class
        Game soccer = new Game("Soccer", 50);
        Game basketball = new Game("Basketball", 60);
        Game tennis = new Game("Tennis", 40);

        // Starting and playing games
        soccer.startGame();
        soccer.playGame();
        soccer.playGame();
        soccer.endGame();

        basketball.startGame();
        basketball.playGame();
        basketball.playGame();
        basketball.playGame();
        basketball.endGame();

        tennis.startGame();
        tennis.playGame();
        tennis.playGame();
        tennis.endGame();
    }
}
```

#### **Explanation:**

**Attributes (gameName, maxScore, currentScore)**: These hold the information about the name of the game, the maximum score limit, and the current score during the game.

**Constructor**: Initializes the game with the given `gameName` and `maxScore`, and sets the `currentScore` to 0 when the game starts.

**Methods**:

- `startGame()`: Starts the game and resets the score to 0.

- `playGame()`: Increases the score by 10 points. If the `maxScore` is reached, it prints a message indicating the game is over.

- `endGame()`: Prints the final score and ends the game.

**Main method**: Creates instances of Game, calls the methods to start, play, and end the game, and displays the final score.

#### **Steps to Compile and Run:**

1. Save the file as `Game.java`.

2. In the terminal, compile the code:

   ```
   javac Game.java
   ```

3. Run the code:

   ```
   java Game
   ```

#### **Output:**

```java
Starting the game: Soccer
Playing Soccer... Current Score: 10
Playing Soccer... Current Score: 20
Ending the game: Soccer. Final Score: 20
Starting the game: Basketball
Playing Basketball... Current Score: 10
Playing Basketball... Current Score: 20
Playing Basketball... Current Score: 30
Ending the game: Basketball. Final Score: 30
Starting the game: Tennis
Playing Tennis... Current Score: 10
Playing Tennis... Current Score: 20
Ending the game: Tennis. Final Score: 20
```

---

## Section 9: Introduction To Java Object Oriented Programming

#### **Group 1: Steps 01, 02, and 03**

- **Step 01 - Introduction to Object Oriented Programming - Basics**
- **Step 02 - Introduction to Object Oriented Programming - Terminology - Class, Object**
- **Step 03 - Introduction to Object Oriented Programming - Exercise - Online Shopping**

**Why Grouped**: These lectures provide an introduction to Object-Oriented Programming (OOP) concepts, including the basics, terminology, and a practical exercise on online shopping.

### **Puzzle: Define a Class for an Online Shopping Item**

**Problem:**
Create a class called `Item` that represents an item in an online shopping system.

- The `Item` class should have properties like `name`, `price`, and `quantity`.

- Write a method to display the details of the item, including the total cost (`price * quantity`).

**Explanation:**

1. **Define the Class and Properties:**  
   The `Item` class will have `name` (String), `price` (double), and `quantity` (int) properties.
   
   Example:
   ```java
   class Item {
       String name;
       double price;
       int quantity;
   }
   ```

2. **Constructor for Initialization:**  
   The constructor will initialize the values for these properties.
   
   Example:
   ```java
   Item(String name, double price, int quantity) {
       this.name = name;
       this.price = price;
       this.quantity = quantity;
   }
   ```

3. **Method to Display Item Details:**  
   A `displayItemDetails()` method will print the name, price, and total cost (price * quantity).
   
   Example:
   ```java
   void displayItemDetails() {
       double totalCost = price * quantity;
       System.out.println("Item: " + name + ", Price: " + price + ", Quantity: " + quantity + ", Total Cost: " + totalCost);
   }
   ```

4. **Create Objects and Call the Method:**  
   Create instances of `Item` and call `displayItemDetails()` to show details.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Item phone = new Item("Phone", 299.99, 2);
           phone.displayItemDetails();
       }
   }
   ```

**Output:**

```java
Item: Phone, Price: 299.99, Quantity: 2, Total Cost: 599.98
```

### **Existing Quiz Questions:**

1. **What is a class in Object Oriented Programming?**
   - A) An instance of an object
   - B) template for creating objects (Answer: B)
   - C) function to perform actions

2. **What are the two main components of an object in Object Oriented Programming?**
    - A) State and Behavior (Answer: A)
    - B) Template and Instance
    - C) Functions and Variables

### **New Quiz Questions:**

1. **What is the key concept behind Object-Oriented Programming (OOP)?**
   - A) Procedural coding
   - B) Organizing code around objects and classes (Answer: B)
   - C) Structured programming

2. **What does a class define in OOP?**
   - A) Only methods
   - B) Attributes and actions (Answer: B)
   - C) Objects

### **Fun Fact:**
- **Did you know?** Java is one of the most widely used Object-Oriented Programming languages, and OOP helps manage large and complex applications by organizing code into reusable objects.

---

#### **Group 2: Steps 04, 05, and 06**

- **Step 04 - Create Motor Bike Java Class and a couple of objects**
- **Step 05 - Exercise Solutions - Book class and Three instances**
- **Step 06 - Introducing State of an object with speed variable**

**Why Grouped**: These lectures cover practical exercises and examples (Motor Bike and Book classes), focusing on creating objects and introducing state with variables.


### **Puzzle 1: MotorBike Class with Speed**

**Problem:**
Create a class `MotorBike` with a variable `speed`. Write methods to get and set the speed.

- Create two objects: `ducati` and `honda`, with different speeds. Then, print out the speeds of both bikes.

**Explanation:**

1. **Define the Class:**  
   Define the `MotorBike` class with the `speed` property.
   
   Example:
   ```java
   class MotorBike {
       int speed;
   }
   ```

2. **Get and Set Methods:**  
   Write methods to get and set the speed.

   Example:
   ```java
   void setSpeed(int speed) {
       this.speed = speed;
   }
   
   int getSpeed() {
       return this.speed;
   }
   ```

3. **Create Objects and Set Speeds:**  
   Create two instances of `MotorBike` and set their speeds.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           MotorBike ducati = new MotorBike();
           MotorBike honda = new MotorBike();
           
           ducati.setSpeed(100);
           honda.setSpeed(80);
           
           System.out.println("Ducati speed: " + ducati.getSpeed());
           System.out.println("Honda speed: " + honda.getSpeed());
       }
   }
   ```

**Output:**

```java
Ducati speed: 100
Honda speed: 80
```

---

### **Puzzle 2: Create a Book Class and Instances**

**Problem:**
Create a class `Book` with attributes `title`, `author`, and `noOfCopies`. Write a method to display the book’s details.

- Create three instances: `Art of Computer Programming`, `Effective Java`, and `Clean Code`.

**Explanation:**

1. **Step 1: Define the Class and Attributes:**  
   The `Book` class will have `title`, `author`, and `noOfCopies`.

   Example:
   ```java
   class Book {
       String title;
       String author;
       int noOfCopies;
   }
   ```

2. **Step 2: Constructor and Method to Display Book Details:**  
   Add a constructor and a method to display details.

   Example:
   ```java
   Book(String title, String author, int noOfCopies) {
       this.title = title;
       this.author = author;
       this.noOfCopies = noOfCopies;
   }
   
   void displayBookDetails() {
       System.out.println(title + " by " + author + " has " + noOfCopies + " copies.");
   }
   ```

3. **Step 3: Create Objects and Display Details:**  
   Create three `Book` objects and display their details.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Book book1 = new Book("Art of Computer Programming", "Donald Knuth", 1000);
           Book book2 = new Book("Effective Java", "Joshua Bloch", 500);
           Book book3 = new Book("Clean Code", "Robert Martin", 300);
           
           book1.displayBookDetails();
           book2.displayBookDetails();
           book3.displayBookDetails();
       }
   }
   ```

**Output:**

```java
Art of Computer Programming by Donald Knuth has 1000 copies.
Effective Java by Joshua Bloch has 500 copies.
Clean Code by Robert Martin has 300 copies.
```

### **Existing Quiz Questions:**

1. **Which of the following methods in a class is the recommended approach to set the title attribute?**
    - A) setTitle(String title) (Answer: A)
    - B) getTitle()
    - C) setBook(String book)

2. **In a Java class, what is the purpose of a getter method?**
    - A) To modify the value of a private member variable
    - B) To access the value of a private member variable (Answer: B)

### **New Quiz Questions:**

1. **What does the `setSpeed()` method in the MotorBike class do?**
   - A) Sets the speed of the bike (Answer: A)
   - B) Starts the bike
   - C) Increases speed automatically

2. **What is the purpose of instance variables in OOP?**
   - A) To store state data for each object (Answer: A)
   - B) To execute methods
   - C) To call constructors

### **Fun Fact:**
- **Did you know?** Each object in Java has its own **state** (stored in instance variables) and **behavior** (defined by methods), which is why each `MotorBike` or `Book` object can have its own unique values.

---

#### **Group 3: Steps 07, 08, and 09**

- **Step 07 - Understanding basics of Encapsulation with Setter methods**
- **Step 08 - Exercises and Tips - Getters and Generating Getters and Setters with Eclipse**
- **Step 09 - Puzzles on this and initialization of member variables**

**Why Grouped**: These lectures introduce the concept of encapsulation and provide exercises and puzzles related to using getters and setters.

### **Puzzle: Encapsulation with Speed and Validation**

**Problem:**
Modify the `MotorBike` class to use **encapsulation**. Make the `speed` variable private and provide getter and setter methods. Ensure the setter method does not allow negative speeds.

**Explanation:**

1. **Encapsulate the Speed Property:**  
   Make the `speed` variable private.

   Example:
   ```java
   private int speed;
   ```

2. **Create Getters and Setters with Validation:**  
   Create getter and setter methods. The setter should only allow non-negative values for speed.

   Example:
   ```java
   void setSpeed(int speed) {
       if (speed >= 0) {
           this.speed = speed;
       }
   }
   
   int getSpeed() {
       return this.speed;
   }
   ```

3. **Create Objects and Test the Validation:**  
   Create `MotorBike` objects, set their speeds, and attempt to set a negative speed (which should be ignored).

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           MotorBike ducati = new MotorBike();
           ducati.setSpeed(100);
           ducati.setSpeed

           (-50); // This should be ignored
           
           System.out.println("Ducati speed: " + ducati.getSpeed()); // Output should be 100
       }
   }
   ```

**Output:**

```java
Ducati speed: 100
```

### **Existing Quiz Questions:**

1. **What is the purpose of private keyword in Java?**
    - A) To make a variable or method accessible only within the class (Answer: A)
    - B) To make a variable or method accessible outside the class
    - C) To make a variable or method static

2. **What is the main principle that is violated when an object directly accesses the state of another object without using any methods?**
    - A) Inheritance
    - B) Encapsulation (Answer: B)

### **New Quiz Questions:**

1. **What is encapsulation in Java?**
   - A) Hiding implementation details (Answer: A)
   - B) Making all variables public
   - C) Creating multiple objects

2. **What does the getter method do?**
   - A) Retrieves the value of a variable (Answer: A)
   - B) Changes the value of a variable
   - C) Deletes a variable

### **Fun Fact:**

- **Did you know?** Encapsulation is a way to protect data in a class by restricting direct access to it and using controlled methods (getters and setters) for modification.

---

#### **Group 4: Steps 10, 11, and 12**

- **Step 10 - First Advantage of Encapsulation**
- **Step 11 - Introduction to Encapsulation - Level 2**
- **Step 12 - Encapsulation Exercises - Better Validation and Book class**

**Why Grouped:** These steps explore **encapsulation** in more depth, focusing on its advantages and how better validation can be achieved by using it.

### **Puzzle 1: Book Class with Price Validation**

**Problem:**
Create a class `Book` with private properties `title`, `author`, and `price`. Use getter and setter methods to access these properties, but ensure the `price` cannot be negative.

- Create a few instances of the `Book` class and test the validation.

**Explanation:**

1. **Private Properties:**  
   Make the `title`, `author`, and `price` variables private to ensure encapsulation.

   Example:
   ```java
   class Book {
       private String title;
       private String author;
       private double price;
   }
   ```

2. **Getters and Setters with Validation:**  
   Write getter and setter methods. The setter for `price` will ensure that it does not accept negative values.

   Example:
   ```java
   void setPrice(double price) {
       if (price >= 0) {
           this.price = price;
       }
   }

   double getPrice() {
       return price;
   }
   ```

3. **Create and Test Book Objects:**  
   Create instances of the `Book` class and test setting the `price`. Try setting both valid and invalid prices to see the validation in action.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Book book1 = new Book();
           book1.setPrice(20);
           book1.setPrice(-5); // This should be ignored

           System.out.println("Book price: " + book1.getPrice()); // Should display 20
       }
   }
   ```

**Output:**

```java
Book price: 20.0
```

---

### **Puzzle 2: Better Validation with Book Class**

**Problem:**
Extend the `Book` class to add a new private property `numberOfPages`. 

- Add a setter for `numberOfPages` that ensures the value must be greater than zero.

- Create a few book instances and validate the number of pages.

**Explanation:**

1. **Add `numberOfPages` Property:**  
   Make `numberOfPages` private and ensure encapsulation.

   Example:
   ```java
   private int numberOfPages;
   ```

2. **Setter with Validation:**  
   The setter for `numberOfPages` will validate that the number must be greater than zero.

   Example:
   ```java
   void setNumberOfPages(int numberOfPages) {
       if (numberOfPages > 0) {
           this.numberOfPages = numberOfPages;
       }
   }

   int getNumberOfPages() {
       return numberOfPages;
   }
   ```

3. **Test Validation:**  
   Test the validation by creating instances of the `Book` class and setting valid and invalid values for `numberOfPages`.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Book book2 = new Book();
           book2.setNumberOfPages(100);
           book2.setNumberOfPages(-10); // This should be ignored

           System.out.println("Number of pages: " + book2.getNumberOfPages()); // Should display 100
       }
   }
   ```

**Output:**

```java
Number of pages: 100
```

### **Existing Quiz Questions:**

1. **What are the default values for object member variables when they are not explicitly initialized?**
    - A) null for reference types, true for boolean and the type's minimum value for numeric primitive types
    - B) null for reference types, false for boolean, and 0 for numeric primitive types (Answer: B)
    - C) The type's maximum value for primitive types, true for boolean and null for reference types

### **New Quiz Questions:**

1. **What is the main advantage of using encapsulation?**
   - A) Faster code execution
   - B) Better control over data validation (Answer: B)
   - C) More readable code

2. **What does a private variable mean in Java?**
   - A) The variable can only be accessed inside its class (Answer: A)
   - B) The variable can be accessed by other classes

### **Fun Fact:**

- **Did you know?** Encapsulation is one of the key principles of OOP and helps create **safe** and **modular** code by hiding the internal workings of classes and exposing only what is necessary.

---

#### **Group 5: Steps 13, 14, and 15**

- **Step 13 - Introduction to Abstraction**
- **Step 14 - Introduction to Java Constructors**
- **Step 15 - Introduction to Java Constructors - Exercises and Puzzles**

**Why Grouped:** These steps cover the concepts of **abstraction** and **constructors** in Java. There are exercises and puzzles related to constructors.

Sure! Here’s the updated version of the **Puzzle 1: Abstraction with Vehicle Class** example, following the correct approach for **inner classes** and abstract classes, as we've just fixed it.

### **Puzzle 1: Abstraction with Vehicle Class (Using Inner Classes)**

#### **Problem:**
Create an abstract class `Vehicle` with an abstract method `move()`. 

- Inside `Vehicle`, create two inner classes `Car` and `Bicycle` that extend `Vehicle` and provide their own implementation of `move()`.

#### **Explanation:**

1. **Abstract Class and Method:**
   - The `Vehicle` class is abstract and contains an abstract method `move()` that must be implemented by the inner classes.

   **Example:**
   ```java
   abstract class Vehicle {
       abstract void move();
   }
   ```

2. **Inner Classes Implementing the Abstract Method:**
   - Both `Car` and `Bicycle` are inner classes of `Vehicle`, and each implements the `move()` method in its own way.

   **Example:**
   ```java
   class Car extends Vehicle {
       void move() {
           System.out.println("Car is moving on the road.");
       }
   }

   class Bicycle extends Vehicle {
       void move() {
           System.out.println("Bicycle is pedaling on the street.");
       }
   }
   ```

3. **Test the Classes:**
   - To test these classes, create an anonymous instance of `Vehicle` and use it to instantiate the inner classes (`Car` and `Bicycle`). Then, call the `move()` methods on each instance.

   **Example:**
   ```java
   public class Main {
       public static void main(String[] args) {
           // Create an instance of the outer Vehicle class
           Vehicle vehicle = new Vehicle() {
               @Override
               void move() {
                   // This block is required but not used
               }
           };
           
           // Use the outer class instance to create inner class objects
           Vehicle.Car car = vehicle.new Car();
           Vehicle.Bicycle bicycle = vehicle.new Bicycle();

           // Call the move method on both inner class instances
           car.move();        // Output: Car is moving on the road.
           bicycle.move();    // Output: Bicycle is pedaling on the street.
       }
   }
   ```

4. **Output:**
   ```
   Car is moving on the road.
   Bicycle is pedaling on the street.
   ```

---

### **Puzzle 2: Constructor in a Person Class**

**Problem:**
Create a class `Person` with attributes `name` and `age`. Write a constructor that initializes these attributes.

- Create instances of `Person` and print the name and age.

**Explanation:**

1. **Class with Constructor:**  
   The `Person` class will have a constructor that initializes `name` and `age`.

   Example:
   ```java
   class Person {
       String name;
       int age;

       Person(String name, int age) {
           this.name = name;
           this.age = age;
       }
   }
   ```

2. **Create and Display `Person` Objects:**  
   Create two `Person` objects and display their details using the constructor.

   Example:
   ```java
   public class Main {
       public static void main(String[] args) {
           Person person1 = new Person("Alice", 25);
           Person person2 = new Person("Bob", 30);

           System.out.println(person1.name + " is " + person1.age + " years old.");
           System.out.println(person2.name + " is " + person2.age + " years old.");
       }
   }
   ```

**Output:**

```java
Alice is 25 years old.
Bob is 30 years old.
```

### **Existing Quiz Questions:**

1. **What is a constructor in Java?**
    - A) A special method that is called when an object of a class is created. (Answer: A)
    - B) A method that is used to destroy an object.

2. **How is a constructor invoked in Java?**
    - A) By calling the method directly
    - B) By using the new keyword to create an object of the class (Answer: B)
    - C) By declaring the constructor as static

### **New Quiz Questions:**

1. **What is the purpose of a constructor in Java?**
   - A) It defines an abstract method
   - B) It initializes an object when it is created (Answer: B)
   - C) It deletes the object

2. **What is abstraction in OOP?**
   - A) Hiding implementation details and exposing only essential features (Answer: A)
   - B) Creating multiple objects
   - C) Writing simple code

### **Fun Fact:**

- **Did you know?** **Abstraction** allows you to define **general behaviors** in a base class, while **specific behaviors** are left to subclasses. Constructors, on the other hand, help you initialize objects when they are created.

---

#### **Group 6: Step 16**

- **Step 16 - Introduction to Object Oriented Programming - Conclusion**

**Why Grouped:** This step wraps up the entire OOP section, summarizing the key concepts learned.

### **New Quiz Questions:**

1. **Which of the following is NOT one of the four pillars of OOP?**
   - A) Encapsulation
   - B) Abstraction
   - C) Compilation (Answer: C)

2. **What is polymorphism in OOP?**
   - A) The ability of one method to behave differently based on the object (Answer: A)
   - B) The inheritance of properties
   - C) Writing multiple methods

### **Fun Fact:**

- **Did you know?** The four pillars of OOP are designed to help developers **organize, structure, and manage complex code** by providing a framework that promotes flexibility, reusability, and scalability.

---

### Additional Coding Exercises:

### **Exercise 1: Create a "`GuessTheNumber`" Game**

#### **Problem:**

Create a class called `GuessTheNumber` that allows a player to guess a randomly generated number within a certain range. The class should:

- Have private attributes for the target number, the number of attempts, and a range (minimum and maximum numbers).

- Implement methods:

  - `startGame()` – to start the game and generate a random target number within the range.

  - `guess(int number)` – to accept a guess and provide feedback (too high, too low, or correct).

  - `displayResult()` – to display the total number of attempts made by the player.

The game ends when the player guesses the correct number.

#### **Code:**

```java
import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    // Private attributes of the GuessTheNumber class
    private int targetNumber;     // The random number to be guessed
    private int numberOfAttempts; // Number of attempts made by the player
    private int minRange;         // Minimum value of the range
    private int maxRange;         // Maximum value of the range

    // Constructor to initialize the game with a range
    public GuessTheNumber(int minRange, int maxRange) {
        this.minRange = minRange;
        this.maxRange = maxRange;
        this.numberOfAttempts = 0; // Initialize attempts to 0
    }

    // Method to start the game and generate a random number within the range
    public void startGame() {
        Random random = new Random();
        targetNumber = random.nextInt(maxRange - minRange + 1) + minRange;
        System.out.println("Game started! Try to guess the number between " + minRange + " and " + maxRange);
    }

    // Method to accept a guess and provide feedback
    public void guess(int number) {
        numberOfAttempts++; // Increment the number of attempts with each guess
        if (number == targetNumber) {
            System.out.println("Congratulations! You guessed the correct number.");
            displayResult();
        } else if (number < targetNumber) {
            System.out.println("Too low! Try again.");
        } else {
            System.out.println("Too high! Try again.");
        }
    }

    // Method to display the result (number of attempts made)
    public void displayResult() {
        System.out.println("You guessed the correct number in " + numberOfAttempts + " attempts.");
    }

    // Main method to test the GuessTheNumber game
    public static void main(String[] args) {
        // Create a Scanner to read input from the player
        Scanner scanner = new Scanner(System.in);

        // Create a GuessTheNumber object with a range between 1 and 10
        GuessTheNumber game = new GuessTheNumber(1, 10);

        // Start the game
        game.startGame();

        // Loop until the player guesses the correct number
        boolean correctGuess = false;
        while (!correctGuess) {
            System.out.print("Enter your guess: ");
            int playerGuess = scanner.nextInt();
            game.guess(playerGuess); // Call the guess method with the player's input

            if (playerGuess == game.targetNumber) {
                correctGuess = true; // Break the loop if the guess is correct
            }
        }

        // Close the scanner
        scanner.close();
    }
}
```

#### **Explanation:**

- The `GuessTheNumber` class encapsulates the game logic, including the randomly generated target number, the number of attempts, and the range.

- The constructor initializes the game by setting the range (`minRange`, `maxRange`) and resetting the attempt counter.

- The `startGame()` method generates a random number within the given range.

- The `guess(int number)` method accepts the player's guess, compares it to the target number, and provides feedback (too high, too low, or correct). It also increments the number of attempts.

- The game loop runs until the player guesses the correct number, at which point the game displays the result.

**Attributes (`targetNumber`, `numberOfAttempts`, `minRange`, `maxRange`):** These store the target number to guess, how many guesses the player has made, and the range within which the number is generated.

**Constructor:** Initializes the game's range and resets the attempt counter.

**Methods:**

  - `startGame()`: Randomly generates the target number and starts the game.

  - `guess(int number)`: Takes a guess and gives feedback (too high, too low, or correct).

  - `displayResult()`: Displays the number of attempts made once the player guesses correctly.

**Main method:** Sets up the game, takes input from the player, and loops until the correct guess is made.

#### **Steps to Run:**

1. Save the file as `GuessTheNumber.java`.

2. Compile using:

   ```
   javac GuessTheNumber.java
   ```

3. Run the program:

   ```
   java GuessTheNumber
   ```

#### **Output:**

```
Game started! Try to guess the number between 1 and 100
Enter your guess: 4
Too high! Try again.
Enter your guess: 1
Too low! Try again.
Enter your guess: 3
Congratulations! You guessed the correct number.
You guessed the correct number in 3 attempts.
```

---

### **Exercise 2: Rock, Paper, Scissors Game**

#### **Problem:**
Write a class called `RockPaperScissors` that allows the player to compete against the computer in a game of Rock, Paper, Scissors. The game should:

- Randomly generate the computer’s choice (rock, paper, or scissors).

- Accept the player’s choice.

- Compare the choices to determine the winner.

- Track the player's **wins**, **losses**, and **ties** over multiple rounds.

The game should allow the player to play multiple rounds and display the final score when the player chooses to stop.

#### **Code:**

```java
import java.util.Random;
import java.util.Scanner;

public class RockPaperScissors {
    // Attributes to track player's wins, losses, and ties
    private int wins;
    private int losses;
    private int ties;

    // Constructor to initialize the game with 0 wins, losses, and ties
    public RockPaperScissors() {
        wins = 0;
        losses = 0;
        ties = 0;
    }

    // Method to randomly generate the computer's choice
    public String getComputerChoice() {
        Random random = new Random();
        int choice = random.nextInt(3); // Generates a number between 0 and 2
        switch (choice) {
            case 0:
                return "rock";
            case 1:
                return "paper";
            case 2:
                return "scissors";
            default:
                return ""; // This should never happen
        }
    }

    // Method to determine the winner of a round
    public void playRound(String playerChoice, String computerChoice) {
        System.out.println("Computer chose: " + computerChoice);

        if (playerChoice.equals(computerChoice)) {
            System.out.println("It's a tie!");
            ties++;
        } else if (
            (playerChoice.equals("rock") && computerChoice.equals("scissors")) ||
            (playerChoice.equals("paper") && computerChoice.equals("rock")) ||
            (playerChoice.equals("scissors") && computerChoice.equals("paper"))
        ) {
            System.out.println("You win!");
            wins++;
        } else {
            System.out.println("You lose!");
            losses++;
        }
    }

    // Method to display the player's score
    public void displayScore() {
        System.out.println("Wins: " + wins + ", Losses: " + losses + ", Ties: " + ties);
    }

    // Main method to run the game
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        RockPaperScissors game = new RockPaperScissors();

        boolean keepPlaying = true;

        // Game loop for multiple rounds
        while (keepPlaying) {
            System.out.print("Enter your choice (rock, paper, or scissors): ");
            String playerChoice = scanner.nextLine().toLowerCase(); // Get player's choice and convert to lowercase

            // Validate player input
            if (!playerChoice.equals("rock") && !playerChoice.equals("paper") && !playerChoice.equals("scissors")) {
                System.out.println("Invalid choice. Please enter rock, paper, or scissors.");
                continue;
            }

            // Get computer's choice and play the round
            String computerChoice = game.getComputerChoice();
            game.playRound(playerChoice, computerChoice);

            // Ask if the player wants to play again
            System.out.print("Do you want to play again? (yes or no): ");
            String playAgain = scanner.nextLine().toLowerCase();

            if (!playAgain.equals("yes")) {
                keepPlaying = false; // End the game loop if the player says "no"
            }
        }

        // Display the final score after the game ends
        System.out.println("\nGame Over! Final Score:");
        game.displayScore();

        // Close the scanner
        scanner.close();
    }
}
```

#### **Explanation:**

- **Attributes:**
  - `wins`, `losses`, `ties`: These variables track the player's performance over multiple rounds.
  
- **Methods:**
  - `getComputerChoice()`: Generates a random choice for the computer (either "rock", "paper", or "scissors").

  - `playRound()`: Compares the player's choice and the computer's choice, determines the winner, and updates the scores (wins, losses, ties).

  - `displayScore()`: Displays the total number of wins, losses, and ties after the game ends.

- **Main Method:** 

  - The game runs in a loop, allowing the player to play multiple rounds. The loop continues until the player chooses to stop.

  - The player's input is validated to ensure it's either "rock", "paper", or "scissors".

  - After each round, the player is asked if they want to play again.

#### **Steps to Run:**

1. Save the file as `RockPaperScissors.java`.

2. Compile using:

   ```
   javac RockPaperScissors.java
   ```

3. Run the program:

   ```
   java RockPaperScissors
   ```

#### **Output:**

```java
Enter your choice (rock, paper, or scissors): rock
Computer chose: paper
You lose!
Do you want to play again? (yes or no): yes

Enter your choice (rock, paper, or scissors): scissors
Computer chose: paper
You win!
Do you want to play again? (yes or no): no

Game Over! Final Score:
Wins: 1, Losses: 1, Ties: 0
```

---

### **Exercise 3: Math Quiz Challenge**

#### **Problem:**
Create a game where the player is presented with random math problems (addition, subtraction, multiplication, or division).

The player must solve as many problems as possible within a time limit (e.g., 10 seconds). The game tracks the player's score based on correct answers.

### **Code:**

```java
import java.util.Random;
import java.util.Scanner;
import java.util.Timer;
import java.util.TimerTask;

public class MathQuizChallenge {
    private static int score = 0; // Keeps track of the player's score
    private static boolean timeUp = false; // Keeps track of whether the time is up

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.println("Welcome to the Math Quiz Challenge!");
        System.out.println("Solve as many math problems as you can within 10 seconds.");
        System.out.println("Press Enter to start...");
        scanner.nextLine(); // Wait for the player to press Enter

        // Start the timer for 10 seconds
        Timer timer = new Timer();
        timer.schedule(new TimerTask() {
            @Override
            public void run() {
                timeUp = true;
                System.out.println("\nTime's up!");
            }
        }, 10000); // Timer set for 10 seconds

        // Main game loop
        while (!timeUp) {
            // Generate random numbers and a random operation
            int num1 = random.nextInt(10) + 1; // Random number between 1 and 10
            int num2 = random.nextInt(10) + 1; // Random number between 1 and 10
            int operator = random.nextInt(4);  // 0 for +, 1 for -, 2 for *, 3 for /

            String operation = "";
            int correctAnswer = 0;

            switch (operator) {
                case 0:
                    operation = "+";
                    correctAnswer = num1 + num2;
                    break;
                case 1:
                    operation = "-";
                    correctAnswer = num1 - num2;
                    break;
                case 2:
                    operation = "*";
                    correctAnswer = num1 * num2;
                    break;
                case 3:
                    operation = "/";
                    // Ensure that num2 is not zero to avoid division by zero
                    if (num2 == 0) num2 = 1;
                    correctAnswer = num1 / num2;
                    break;
            }

            // Display the math problem to the player
            System.out.print(num1 + " " + operation + " " + num2 + " = ");

            // Check if time has run out before accepting input
            if (scanner.hasNextInt() && !timeUp) {
                int playerAnswer = scanner.nextInt(); // Get the player's answer

                // Check if the player's answer is correct
                if (playerAnswer == correctAnswer) {
                    System.out.println("Correct!");
                    score++;
                } else {
                    System.out.println("Wrong. The correct answer was " + correctAnswer);
                }
            } else {
                break; // Exit the loop if the time is up or no valid input is provided
            }
        }

        // Print the final score after the game loop ends
        System.out.println("\nYour final score is: " + score);

        // Close the scanner
        scanner.close();
    }
}
```

### **Explanation:**

1. **Attributes:**

   - `score`: This variable tracks the number of correct answers the player gives.

   - `timeUp`: This boolean tracks whether the 30-second timer has ended, signaling that the game is over.

2. **Main Method:**

   - **Timer**: A `Timer` is used to count down 30 seconds. Once the time is up, the game stops, and no more problems are presented to the player.

   - **Random Math Problem Generation**: The game randomly generates two numbers (`num1` and `num2`) and selects a random operation (`+`, `-`, `*`, `/`) for the player to solve. 

   - **Game Loop**: The game keeps running until the timer expires. The player's answers are compared to the correct answers, and their score is updated accordingly.

3. **Game Flow:**

   - The player presses **Enter** to start.

   - Math problems are generated one by one, and the player inputs their answer.

   - The game provides feedback for each answer (correct or wrong).

   - After 30 seconds, the game ends, and the player's final score is displayed.

### **Steps to Run:**

1. Save the file as `MathQuizChallenge.java`.

2. Compile the program:

   ```
   javac MathQuizChallenge.java
   ```

3. Run the program:

   ```
   java MathQuizChallenge
   ```

### **Output:**

```java
Welcome to the Math Quiz Challenge!
Solve as many math problems as you can within 10 seconds.
Press Enter to start...

3 + 7 = 10
Correct!
6 * 5 = 30
Correct!
8 / 2 = 4
Correct!
4 - 9 = -5
Correct!
2 * 2 = 5
Wrong. The correct answer was 4
7 + 8 = 15
Correct!

Time's up!
Your final score is: 5
```

### **Possible Enhancements:**

1. **Different Levels:** Adding difficulty levels (easy, medium, hard) where the range of numbers or types of operations becomes more challenging.

2. **Scoring System:** Award more points for solving harder problems (e.g., multiplication and division).

3. **High Score Tracker:** Storing the player's highest score and display it at the end of each game.

---

## Section 11: Primitive Data Types And Alternatives in Java Programming

#### **Group 1: Integer Data Types (Steps 01, 02, 03)**

- **Step 01: Basics about Java Integer Data Types - Casting, Operators and More**
- **Step 02: Java Integer Data Types - Puzzles - Octal, Hexadecimal, Post and Pre Increment**
- **Step 03: Java Integer Data Types - Exercises - BiNumber - add, multiply and double**

**Why Grouped**: These steps focus on integer data types, including the basics, puzzles on number systems (octal, hexadecimal), and exercises with operations on integers (like adding, multiplying, and doubling).



### **Puzzle 1: Octal and Hexadecimal Conversion**
**Problem:** Convert the following values into decimal:
1. Octal value `010` (Hint: Base 8)
2. Hexadecimal value `0xA2` (Hint: Base 16)

**Answer:**
1. Octal `010` = Decimal `8`
2. Hexadecimal `0xA2` = Decimal `162`

### **Puzzle 2: Pre and Post-Increment Operators**
**Problem:** Predict the output of the following code based on the discussion of pre- and post-increment:
```java
int x = 5;
int y = ++x;
System.out.println(x);  // ?
System.out.println(y);  // ?
```

**Answer:**  
- `x = 6`
- `y = 6`

### **Existing Quiz Questions:**

1. Which of these wrapper classes corresponds to the 'int' primitive type in Java?

    - A) Byte
    - B) Integer (Answer: B)
    - C) Short

2. What is the maximum value of a 'short' data type in Java?

    - A) 127
    - B) 32767 (Answer: B)
    - C) 2147483647

3. Which of the following is the correct representation for the value 16 in a hexadecimal system?

    - A) 0x10 (Answer: A)
    - B) 010
    - C) 0х16

### **New Quiz Questions:**

1. What is the difference between pre-increment and post-increment in Java?

    - A) Pre-increment uses the value first, then increments
    - B) Post-increment increments the value first, then uses it
    - C) Pre-increment increments the value before using it in the expression (Answer: C)

2. How are octal and hexadecimal numbers represented in Java?

    - A) Octal with `0` and Hexadecimal with `0x` (Answer: A)
    - B) Both with `0`
    - C) Octal with `x` and Hexadecimal with `h`

### **Fun Fact:**
- **Fun Fact:** The Java platform supports number systems like binary, octal, decimal, and hexadecimal, which are often used in low-level programming.

---

#### **Group 2: (Steps 04, 05, 06, 07)**

- Step 04: Java Floating Point Data Types - Casting, Conversion and Accuracy
- Step 05: Introduction to BigDecimal Java Class
- Step 06: BigDecimal Puzzles - Adding Integers
- Step 07: BigDecimal Exercises - Simple Interest Calculation

**Why Grouped**: These steps focus on floating-point numbers and BigDecimal, covering topics like accuracy with floating-point numbers, casting, conversion, and calculations using the BigDecimal class.

### **Puzzle 1: Floating Point Precision**

**Problem:** Why does the following code print `false`?
```java
double a = 0.1;
double b = 0.2;
System.out.println((a + b) == 0.3);  // Why is this false?
```

**Answer:** Floating-point numbers are not represented exactly in binary, which results in imprecision. The sum of `a` and `b` is slightly off from `0.3`.

### **Puzzle 2: BigDecimal Addition**

**Problem:** What is the output of the following code?
```java
BigDecimal a = new BigDecimal("0.1");
BigDecimal b = new BigDecimal("0.2");
BigDecimal result = a.add(b);
System.out.println(result);
```
**Answer:** The output is `0.3`. This ties into the importance of using `BigDecimal` for financial or precise calculations.

### **Existing Quiz Questions:**

1. What is the default type for floating-point literals in Java?

    - A) float
    - B) double (Answer: B)
1. How can you create a float literal in Java?

    - A) float f = 34.5;
    - B) float f = 34.5f; (Answer: B)

2. What is the main reason for using the BigDecimal data type in Java?

    - A) To represent floating-point numbers with higher precision (Answer: A)
    - B) To perform faster calculations
    - C) To store large integer values

3. What is the best way to construct a BigDecimal object to achieve high precision?

    - A) Using double literals
    - B) Using String literals (Answer: B)

4. Which of the following methods can be used for arithmetic operations on BigDecimal objects?

    - A) add()
    - B) multiply()
    - C) subtract()
    - D) All of the above (Answer: D)

### **New Quiz Questions:**

1. What is the main benefit of using the `BigDecimal` class over floating-point data types?

    - A) It is faster
    - B) It allows better precision for large and exact calculations (Answer: B)
    - C) It uses less memory

2. Why does floating-point arithmetic sometimes produce unexpected results?

    - A) Because Java is not accurate enough
    - B) Because certain numbers cannot be represented exactly in binary (Answer: B)
    - C) Because the computer runs out of memory

### **Fun Fact:**
- **Fun Fact:** The Java `BigDecimal` class was introduced to handle precise decimal calculations, which are critical in applications like banking or scientific computing.

---

#### **Group 3: Boolean Data Types (Steps 08, 09)**

- Step 08: Java Boolean Data Type - Relational and Logical Operators
- Step 09: Java Boolean Data Type - Puzzles - Short Circuit Operators

**Why Grouped**: These steps introduce Boolean data types and the use of logical and relational operators, including puzzles on short-circuit operators.

### **Puzzle 1: Short-Circuit Operators**
**Problem:** What is the output of the following code?
```java
int i = 10, j = 20;
if (j > 25 && i++ > 5) {
    System.out.println(i);
}
```
**Answer:** The output will be `10`, because the first condition (`j > 25`) is false, so the second part (`i++ > 5`) is not evaluated due to short-circuiting.

### **Puzzle 2: Boolean Comparison**
**Problem:** Predict the output of this code:
```java
int x = 5;
boolean result = (x > 3) && (x < 10);
System.out.println(result);  // ?
```
**Answer:** The output is `true` because both conditions are satisfied (`x` is greater than 3 and less than 10).

### **Existing Quiz Questions:**

1. Which of the following operators is a logical operator in Java?

    - A) `>`
    - B) `&&` (Answer: B)
    - C) `<=`

### **New Quiz Questions:**

1. What is a short-circuit operator in Java?

    - A) An operator that always evaluates both conditions
    - B) An operator that stops evaluating once the result is determined (Answer: B)
    - C) An operator used for short expressions

2. What is the difference between `&&` and `&` operators?

    - A) `&&` evaluates both sides of the condition
    - B) `&` is used only for numbers
    - C) `&&` short-circuits, and `&` evaluates both sides even if the first condition is false (Answer: C)


### **Fun Fact:**

- **Fun Fact:** Boolean algebra was developed by George Boole in the mid-1800s, and it forms the foundation of logic gates and decision-making in programming.

---

#### **Group 4: Character Data Types (Steps 10, 11, 12, 13)**

- Step 10: Java Character Data Type char - Representation and Conversion
- Step 11: Java char Data Type - Exercises 1 - isVowel
- Step 12: Java char Data Type - Exercises 2 - isDigit
- Step 13: Java char Data Type - Exercises 3 - isConsonant, List Upper Case and Lower Case

**Why Grouped**: These steps focus on the char data type, including exercises that involve checking characters (vowel, digit, consonant), as well as representation and conversion of characters in Java.

### **Puzzle 1: isVowel Method**
**Problem:** Write a method that checks if a character is a vowel.
```java
public static boolean isVowel(char c) {
    c = Character.toLowerCase(c);
    return (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u');
}
```
**Test Case:**
```java
System.out.println(isVowel('A'));  // true
System.out.println(isVowel('b'));  // false
```

### **Puzzle 2: isDigit Method**
**Problem:** Write a method to check if a character is a digit.
```java
public static boolean isDigit(char c) {
    return Character.isDigit(c);
}
```
**Test Case:**
```java
System.out.println(isDigit('5'));  // true
System.out.println(isDigit('a'));  // false
```

### **New Quiz Questions:**

1. What is the difference between a character literal and a string literal in Java?

    - A) A character literal is enclosed in single quotes, and a string literal in double quotes (Answer: A)
    - B) There is no difference
    - C) A character literal is used for numbers

2. How can you convert a char to its uppercase equivalent?

    - A) Use the `Character.toUpperCase(char)` method (Answer: A)
    - B) Add `32` to the `char` value
    - C) Use `String.toUpperCase()`

### **Fun Fact:**

- **Fun Fact:** Java uses the Unicode character set, which can represent characters from nearly every writing system in the world, allowing over 65,000 characters to be represented in the `char` data type.

---

#### **Group 5: Primitive Data Types in Depth (Step 14)**

- Step 14: Primitive Data Types in Depth - Conclusion
  
**Why Grouped**: This is the conclusion of the entire section, summarizing the key points about primitive data types in Java.

#### **New Quiz Question:**

1. Why are primitive data types used in Java?
    - A) They are more efficient and use less memory (Answer: A)
    - B) They are easier to use than objects
    - C) They do not need to be initialized

### **Fun Fact:**

- **Fun Fact:** Java has 8 primitive data types: `byte`, `short`, `int`, `long`, `float`, `double`, `boolean`, and `char`.

---

### Additional Coding Exercises

### **Exercise 1: Currency Converter Using BigDecimal**

#### **Description:**
This exercise is a simple **currency converter** that uses the `BigDecimal` class to perform precise conversions between different currencies. It teaches the importance of using `BigDecimal` for financial applications where precision matters.

#### **Code:**
```java
import java.math.BigDecimal;
import java.math.RoundingMode;
import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Exchange rates
        BigDecimal usdToEur = new BigDecimal("0.85");  // 1 USD = 0.85 EUR
        BigDecimal usdToGbp = new BigDecimal("0.75");  // 1 USD = 0.75 GBP

        // Input amount in USD
        System.out.print("Enter amount in USD: ");
        BigDecimal amountInUsd = scanner.nextBigDecimal();

        // Convert to EUR and GBP
        BigDecimal amountInEur = amountInUsd.multiply(usdToEur).setScale(2, RoundingMode.HALF_UP);
        BigDecimal amountInGbp = amountInUsd.multiply(usdToGbp).setScale(2, RoundingMode.HALF_UP);

        // Display results
        System.out.println("Amount in EUR: " + amountInEur);
        System.out.println("Amount in GBP: " + amountInGbp);

        scanner.close();
    }
}
```

#### **Output:**
```
Enter amount in USD: 100
Amount in EUR: 85.00
Amount in GBP: 75.00
```

---

### **Exercise 2: Guess the Character Game**

#### **Description:**
This is a **character guessing game** where the player has to guess whether the randomly selected character is a vowel or consonant. It reinforces working with the `char` primitive type.

#### **Code:**
```java
import java.util.Scanner;
import java.util.Random;

public class GuessTheCharacterGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        // List of random characters to guess from
        char[] letters = {'a', 'e', 'i', 'o', 'u', 'b', 'c', 'd', 'f', 'g'};
        char selectedChar = letters[random.nextInt(letters.length)];

        // Prompt user to guess
        System.out.println("Guess if the character is a vowel or consonant.");
        System.out.print("Character: " + selectedChar + " (Type 'vowel' or 'consonant'): ");
        String guess = scanner.next().toLowerCase();

        // Check if the character is a vowel
        boolean isVowel = selectedChar == 'a' || selectedChar == 'e' || selectedChar == 'i' || selectedChar == 'o' || selectedChar == 'u';

        // Compare player's guess with the correct answer
        if ((isVowel && guess.equals("vowel")) || (!isVowel && guess.equals("consonant"))) {
            System.out.println("Correct! " + selectedChar + " is a " + (isVowel ? "vowel." : "consonant."));
        } else {
            System.out.println("Wrong! " + selectedChar + " is a " + (isVowel ? "vowel." : "consonant."));
        }

        scanner.close();
    }
}
```

#### **Output:**
```
Guess if the character is a vowel or consonant.
Character: o (Type 'vowel' or 'consonant'): vowel
Correct! o is a vowel.
```

---

### **Exercise 3: Temperature Conversion Game**

#### **Description:**

In this game, the player must convert a randomly generated temperature from Celsius, Fahrenheit, or Kelvin to the desired unit. The game helps players understand **primitive types** like `float` and `double`, and practice **casting** between data types when needed.

---

### **Code:**

```java
import java.util.Scanner;
import java.util.Random;

public class TemperatureConversionGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        // Introduction
        System.out.println("Welcome to the Temperature Conversion Game!");
        System.out.println("You will be asked to convert temperatures between Celsius, Fahrenheit, and Kelvin.");
        System.out.println("Try to get as many correct answers as possible!");

        // Keep track of score
        int score = 0;

        // Game loop
        for (int i = 0; i < 5; i++) {  // Play 5 rounds
            // Generate random temperature and unit
            float temperature = random.nextInt(100) + random.nextFloat();  // Random temperature between 0 and 100
            int unit = random.nextInt(3);  // 0 = Celsius, 1 = Fahrenheit, 2 = Kelvin
            String originalUnit = "";
            String targetUnit = "";

            switch (unit) {
                case 0:
                    originalUnit = "Celsius";
                    targetUnit = "Fahrenheit";
                    System.out.printf("Convert %.2f degrees Celsius to Fahrenheit: ", temperature);
                    break;
                case 1:
                    originalUnit = "Fahrenheit";
                    targetUnit = "Celsius";
                    System.out.printf("Convert %.2f degrees Fahrenheit to Celsius: ", temperature);
                    break;
                case 2:
                    originalUnit = "Kelvin";
                    targetUnit = "Celsius";
                    System.out.printf("Convert %.2f Kelvin to Celsius: ", temperature);
                    break;
            }

            // Player's answer
            float playerAnswer = scanner.nextFloat();

            // Correct answer calculation
            float correctAnswer = 0;
            switch (unit) {
                case 0:  // Celsius to Fahrenheit
                    correctAnswer = (temperature * 9 / 5) + 32;
                    break;
                case 1:  // Fahrenheit to Celsius
                    correctAnswer = (temperature - 32) * 5 / 9;
                    break;
                case 2:  // Kelvin to Celsius
                    correctAnswer = temperature - 273.15f;
                    break;
            }

            // Check if player's answer is close enough (allow for small precision errors)
            if (Math.abs(playerAnswer - correctAnswer) < 0.1) {
                System.out.println("Correct!");
                score++;
            } else {
                System.out.printf("Wrong! The correct answer was %.2f %s.%n", correctAnswer, targetUnit);
            }
        }

        // Game over - Show final score
        System.out.println("Game over! Your final score is: " + score + " out of 5.");

        scanner.close();
    }
}
```

### **Output:**

```
Welcome to the Temperature Conversion Game!
You will be asked to convert temperatures between Celsius, Fahrenheit, and Kelvin.
Try to get as many correct answers as possible!

Convert 45.72 degrees Celsius to Fahrenheit: 113.5
Correct!

Convert 78.34 degrees Fahrenheit to Celsius: 25.5
Wrong! The correct answer was 25.74 Celsius.

Convert 294.12 Kelvin to Celsius: 20.9
Correct!

Convert 12.59 degrees Celsius to Fahrenheit: 54.0
Wrong! The correct answer was 54.66 Fahrenheit.

Convert 103.12 degrees Fahrenheit to Celsius: 39.5
Correct!

Game over! Your final score is: 3 out of 5.
```

---

## Section 12: Conditionals in Java Programming

#### **Group 1: (Steps 01, 02, 03)**

- **Step 01:** Introduction to If Else Statement
- **Step 02:** Introduction to Nested If Else
- **Step 03:** If Else Statement - Puzzles

**Why Grouped:** These steps introduce **basic if-else** and **nested if-else** structures and how to handle multiple conditions.

### **Puzzle 1: Fix the Block Structure**
**Problem:** Write an if-else statement to check if a number is positive or negative.
```java
int number = -5;
if (number > 0) {
    System.out.println("Positive");
} else {
    System.out.println("Negative");
}
```

### **Puzzle 2: Nested If-Else Example**
**Problem:** Modify the code to add a check for zero and print "Zero" if the number is zero.
```java
int number = 0;
if (number > 0) {
    System.out.println("Positive");
} else if (number < 0) {
    System.out.println("Negative");
} else {
    System.out.println("Zero");
}
```

### **Existing Quiz Questions:**

1. What is the output of the following code snippet?

```java
int i = 10;
if(i < 5) {
    System.out.println("i is less than 5");
} else if(i > 20) {
    System.out.println("i is greater than 20");
} else {
    System.out.println("i is between 5 and 20");
}
```

- A) i is less than 5
- B) i is greater than 20
- C) i is between 5 and 20 (Answer: C)

2. What is the output of the following code snippet?

```java
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

- A) i is less than 5
- B) i is greater than 20
- C) i is less than 10
- D) i is between 10 and 20 (Answer: D)

3. What is the output of the following code snippet?

```java
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

- A) 1
- B) 2 (Answer: B)
- C) 3
- D) 4

4. What is the output of the following code snippet?

```java
int i = 0;
if(i) {
    System.out.println("i");
}
```

- A) i
- B) Compiler Error (Answer: B)
- C) Nothing is printed.

### **New Quiz Questions:**

1. **What is the purpose of the `else` block in Java?**
   - A) It executes if the `if` condition is true.
   - B) It executes if the `if` condition is false. (Answer: B)
   - C) It checks another condition.

2. **What happens if an assignment operator (`=`) is used instead of a comparison operator (`==`) in an if condition?**
   - A) It causes a syntax error.
   - B) The value is assigned, and the if condition might always be true. (Answer: B)
   - C) It causes a runtime error.

#### **Fun Fact:**
- **Fun Fact:** In older languages like C, if conditions could accept integers as "true" or "false." However, in Java, conditions must explicitly return a boolean, improving clarity.

---

#### **Group 2: (Steps 04, 05, 06)**

- **Step 04:** If Else Problem - How to get User Input in Java?
- **Step 05:** If Else Problem - How to get number 2 and choice from user?
- **Step 06:** If Else Problem - Implementing with Nested If Else

**Why Grouped:** These steps focus on interacting with the user via the **Scanner class** to get input and use conditional logic to solve user-driven problems, like making a basic calculator.

### **Puzzle 1: Implement a Simple Calculator**
**Problem:** Write a program that asks the user to enter two numbers and choose an operation (addition, subtraction). Based on the user's choice, perform the operation using nested if-else.
```java
Scanner scanner = new Scanner(System.in);
System.out.print("Enter first number: ");
int num1 = scanner.nextInt();
System.out.print("Enter second number: ");
int num2 = scanner.nextInt();
System.out.print("Enter choice (1 for addition, 2 for subtraction): ");
int choice = scanner.nextInt();

if (choice == 1) {
    System.out.println("Result: " + (num1 + num2));
} else if (choice == 2) {
    System.out.println("Result: " + (num1 - num2));
} else {
    System.out.println("Invalid choice");
}
```

### **Puzzle 2: Get User's Age and Check if Adult**
**Problem:** Write a program that gets the user’s age and prints whether the user is an adult (age >= 18) or not.
```java
Scanner scanner = new Scanner(System.in);
System.out.print("Enter your age: ");
int age = scanner.nextInt();

if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are not an adult.");
}
```

### **Existing Quiz Questions:**

1. What is the purpose of using the Scanner class in Java?

    - A) To read/scan user input from the console (Answer: A)
    - B) To read input from a file
    - C) To generate random numbers

2.	How do you read an integer input from the console using the Scanner class?

    - A) scanner.nextInt() (Answer: A)
    - B) scanner.readInt()
    - C) scanner.getint()

### **New Quiz Questions:**

1. **Which of the following is used to get user input in Java?**
   - A) `Scanner` (Answer: A)
   - B) `BufferedReader`
   - C) `System.out`

2. **What would happen if you forget to close the `Scanner` object?**
   - A) The program will crash.
   - B) Resources may not be released properly. (Answer: B)
   - C) The input will not work.

### **Fun Fact:**
- **Fun Fact:** The `Scanner` class is not only for reading user input but can also read from files and other input sources, making it very versatile.

---

#### **Group 3: (Steps 07, 08, 09)**

- **Step 07:** Java Switch Statement - An Introduction
- **Step 08:** Java Switch Statement - Puzzles - Default, Break and Fall Through
- **Step 09:** Java Switch Statement - Exercises - isWeekDay, nameOfMonth, nameOfDay

**Why Grouped:** These steps cover the **switch statement**, how it compares to if-else, common pitfalls (e.g., forgetting the break statement), and exercises that apply switch to real-world problems like determining days of the week or months of the year.

### **Puzzle 1: Switch on Days of the Week**
**Problem:** Write a switch statement that takes a number (1-7) and prints the corresponding day of the week.
```java
int day = 3;
switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    case 4:
        System.out.println("Thursday");
        break;
    case 5:
        System.out.println("Friday");
        break;
    case 6:
        System.out.println("Saturday");
        break;
    case 7:
        System.out.println("Sunday");
        break;
    default:
        System.out.println("Invalid day");
}
```

### **Puzzle 2: Name of the Month**
**Problem:** Write a switch statement that takes an integer (1-12) and prints the corresponding month.
```java
int month = 5;
switch (month) {
    case 1:
        System.out.println("January");
        break;
    case 2:
        System.out.println("February");
        break;
    case 3:
        System.out.println("March");
        break;
    case 4:
        System.out.println("April");
        break;
    case 5:
        System.out.println("May");
        break;
    // Continue for other months...
    default:
        System.out.println("Invalid month");
}
```

### **Existing Quiz Questions:**

1.	What is the purpose of the break statement in a switch statement in Java?

    - A) To break out of the switch after a successful match (Answer: A)
    - B) To continue to the next case in the switch
    - C) To stop the execution of the program

### **New Quiz Questions:**

1. **What happens if you forget to include a `break` statement in a switch case?**
   - A) Only the matching case is executed.
   - B) All the cases below the matching case are executed (fall-through). (Answer: B)
   - C) It causes a runtime error.

2. **Which data types can be used in a switch statement?**
   - A) `int`, `char`, `String`, `enum` (Answer: A)
   - B) `float`, `double`
   - C) `boolean`

#### **Fun Fact:**
- **Fun Fact:** Java switch statements used to only work with `int` and `char` types, but starting with Java 7, they were expanded to support `String` and `enum`.

---

#### **Group 4: Ternary Operator (Step 10)**

- **Step 10:** Java Ternary Operation - An Introduction

**Why Grouped:** This step explains the **ternary operator** as a shorthand form of if-else for simple conditions.

### **Puzzle: Use the Ternary Operator**
**Problem:** Rewrite the following if-else statement using the ternary operator:
```java
if (age >= 18) {
    result = "Adult";
} else {
    result = "Not Adult";
}
```

**Answer:**
```java
result = (age >= 18) ? "Adult" : "Not Adult";
```

### **Existing Quiz Question:**

1. What is the return type of both expressions in the ternary operator ?: in Java?

    - A) They CAN be different types.
    - B) They MUST be different types.
    - C) They MUST be the same type. (Answer: C)

### **New Quiz Question:**

1. **What is the purpose of the ternary operator in Java?**
   - A) To perform simple if-else conditions in a single line. (Answer: A)
   - B) To replace the switch statement.
   - C) To perform bitwise operations.

### **Fun Fact:**
- **Fun Fact:** The ternary operator is one of the few operators in Java that takes three operands: a condition, a true result, and a false result.

---

#### **Group 5: Conclusion (Step 11)**

- **Step 11:** Conditionals with Java - Conclusion

**Why Grouped:** This is the **conclusion**, summarizing the key takeaways from conditionals in Java.

### **New Quiz Question:**

1. **What is the main benefit of using switch over if-else in certain situations?**
   - A) It is easier to read when there are multiple conditions to check. (Answer: A)
   - B) It is faster in all cases.
   - C) It uses less memory.

---

### Additional Coding Exercises

### **Exercise 1: Simple Calculator Using Nested If-Else**

#### **Description:**
Write a program that simulates a basic calculator. The program should:
1. Prompt the user to enter two numbers.
2. Ask the user to choose an operation: add, subtract, multiply, divide.
3. Use **nested if-else** statements to perform the correct operation.
4. Handle division by zero cases and show appropriate error messages.

#### **Code:**
```java
import java.util.Scanner;

public class SimpleCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get user inputs
        System.out.print("Enter first number: ");
        double num1 = scanner.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = scanner.nextDouble();

        System.out.println("Choose operation: 1) Add 2) Subtract 3) Multiply 4) Divide");
        int choice = scanner.nextInt();

        double result = 0;
        boolean validOperation = true;

        // Use nested if-else for operations
        if (choice == 1) {
            result = num1 + num2;
        } else if (choice == 2) {
            result = num1 - num2;
        } else if (choice == 3) {
            result = num1 * num2;
        } else if (choice == 4) {
            if (num2 != 0) {
                result = num1 / num2;
            } else {
                System.out.println("Error: Division by zero is not allowed.");
                validOperation = false;
            }
        } else {
            System.out.println("Invalid operation selected.");
            validOperation = false;
        }

        // Print result if the operation is valid
        if (validOperation) {
            System.out.println("Result: " + result);
        }

        scanner.close();
    }
}
```

#### **Output:**

```java
Enter first number: 10
Enter second number: 5
Choose operation: 1) Add 2) Subtract 3) Multiply 4) Divide
3
Result: 50.0
```

---

### **Exercise 2: Day of the Week Checker Using Switch**

#### **Description:**
Create a program that takes an integer input (1-7) from the user and displays the corresponding day of the week (1 = Sunday, 2 = Monday, ..., 7 = Saturday).

Use a **switch statement** to implement this. Include error handling for invalid inputs (numbers outside 1-7).

#### **Code:**
```java
import java.util.Scanner;

public class DayOfWeekChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user to enter a number between 1 and 7
        System.out.print("Enter a number (1-7) to get the day of the week: ");
        int dayNumber = scanner.nextInt();

        // Use switch to check the day of the week
        switch (dayNumber) {
            case 1:
                System.out.println("Sunday");
                break;
            case 2:
                System.out.println("Monday");
                break;
            case 3:
                System.out.println("Tuesday");
                break;
            case 4:
                System.out.println("Wednesday");
                break;
            case 5:
                System.out.println("Thursday");
                break;
            case 6:
                System.out.println("Friday");
                break;
            case 7:
                System.out.println("Saturday");
                break;
            default:
                System.out.println("Invalid input. Please enter a number between 1 and 7.");
        }

        scanner.close();
    }
}
```

#### **Output:**
```java
Enter a number (1-7) to get the day of the week: 3
Tuesday
```

---

### **Exercise 3: Guess the Number Game (Game Exercise)**

#### **Description:**
Create a **Guess the Number** game where:
1. The computer randomly selects a number between 1 and 100.
2. The user tries to guess the number.
3. The program provides feedback on whether the guess is too high, too low, or correct.
4. Use **if-else** and **while loops** to implement this game.

#### **Code:**
```java
import java.util.Scanner;
import java.util.Random;

public class GuessTheNumberGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        // Computer randomly picks a number between 1 and 100
        int secretNumber = random.nextInt(100) + 1;
        int userGuess = 0;
        int attempts = 0;

        System.out.println("Welcome to the Guess the Number Game!");
        System.out.println("Try to guess the number between 1 and 100.");

        // Game loop
        while (userGuess != secretNumber) {
            System.out.print("Enter your guess: ");
            userGuess = scanner.nextInt();
            attempts++;

            // Provide feedback
            if (userGuess < secretNumber) {
                System.out.println("Too low! Try again.");
            } else if (userGuess > secretNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
            }
        }

        scanner.close();
    }
}
```

#### **Output:**
```java
Welcome to the Guess the Number Game!
Try to guess the number between 1 and 100.
Enter your guess: 50
Too high! Try again.
Enter your guess: 25
Too low! Try again.
Enter your guess: 37
Congratulations! You guessed the number in 3 attempts.
```

---

### **Exercise 4: "Guess the Animal" Game**

#### **Description:**

In this game:
- The computer "thinks" of an animal.

- The player asks **yes** or **no** questions to figure out which animal it is.

- The player continues asking questions until they correctly guess the animal.

- We'll use **if-else statements** to simulate the computer's responses and guide the player toward the right answer.

### **Code:**

```java
import java.util.Scanner;

public class GuessTheAnimal {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String animal = "elephant";  // The animal the computer is thinking of

        System.out.println("Welcome to the 'Guess the Animal' game!");
        System.out.println("I am thinking of an animal. Ask yes/no questions to guess which one!");

        // Game loop
        boolean guessedCorrectly = false;
        while (!guessedCorrectly) {
            System.out.println("\nAsk a yes/no question: ");
            String question = scanner.nextLine().toLowerCase();

            // Use if-else statements to simulate the computer's responses based on the question
            if (question.contains("mammal")) {
                System.out.println("Yes, it's a mammal.");
            } else if (question.contains("large")) {
                System.out.println("Yes, it's large.");
            } else if (question.contains("four legs")) {
                System.out.println("Yes, it has four legs.");
            } else if (question.contains("trunk")) {
                System.out.println("Yes, it has a trunk.");
            } else if (question.contains("africa")) {
                System.out.println("Yes, it lives in Africa.");
            } else if (question.contains("elephant")) {
                System.out.println("Congratulations! You guessed it. It's an elephant!");
                guessedCorrectly = true;
            } else {
                System.out.println("I don't know the answer to that.");
            }
        }

        scanner.close();
        System.out.println("Thanks for playing 'Guess the Animal'!");
    }
}
```

### **Output:**

```java
Welcome to the 'Guess the Animal' game!
I am thinking of an animal. Ask yes/no questions to guess which one!

Ask a yes/no question:
Is it a mammal?
Yes, it's a mammal.

Ask a yes/no question:
Does it have a trunk?
Yes, it has a trunk.

Ask a yes/no question:
Is it an elephant?
Congratulations! You guessed it. It's an elephant!
Thanks for playing 'Guess the Animal'!
```

---

## Section 14: Loops in Java Programming

#### **Group 1: (Steps 01, 02, 03, 04)**

- **Step 01:** Java For Loop - Syntax and Puzzles
- **Step 02:** Java For Loop - Exercises Overview and First Exercise Prime Numbers
- **Step 03:** Java For Loop - Exercise - Sum Upto N Numbers and Sum of Divisors
- **Step 04:** Java For Loop - Exercise - Print a Number Triangle

**Why Grouped**: These steps focus on the for loop structure, including its syntax and various exercises, such as checking prime numbers, calculating sums, and printing number patterns.

### **Puzzle 1: Prime Number Checker**
   - Write a program to check if a number is prime using a **for loop**.
   
   **Solution:**
   ```java
   int number = 17;
   boolean isPrime = true;
   
   for (int i = 2; i <= number / 2; i++) {
       if (number % i == 0) {
           isPrime = false;
           break;
       }
   }
   
   if (isPrime) {
       System.out.println(number + " is a prime number.");
   } else {
       System.out.println(number + " is not a prime number.");
   }
   ```

### **Puzzle 2: Sum of Divisors**

   - Write a program that uses a **for loop** to find the sum of all divisors of a number excluding 1 and the number itself.
   
   **Solution:**
   ```java
   int number = 12;
   int sum = 0;
   
   for (int i = 2; i < number; i++) {
       if (number % i == 0) {
           sum += i;
       }
   }
   
   System.out.println("Sum of divisors of " + number + " is: " + sum);
   ```

### **New Quiz Questions:**

1. **What is the correct syntax of a `for` loop in Java?**
   - A) `for(initialization; condition; update) { statement }` (Answer: A)
   - B) `for(condition; initialization; update)`
   - C) `for(initialization condition update)`

2. **What will the following code print?**
   ```java
   for (int i = 0; i < 3; i++) {
       System.out.print(i + " ");
   }
   ```
   - A) `0 1 2 ` (Answer: A)
   - B) `0 1 2 3`
   - C) `1 2 3`

### **Fun Fact:**
- **Fun Fact:** The **for loop** can be completely empty (`for(;;)`) and still function as an infinite loop.

---

#### **Group 2: (Steps 05, 06)**

- **Step 05:** While Loop in Java - An Introduction
- **Step 06:** While Loop - Exercises - Cubes and Squares upto limit

**Why Grouped**: These steps introduce the while loop, explaining its syntax and providing exercises that calculate cubes and squares within a given limit.

### **Puzzle 1: Print Squares Using While Loop**
   - Write a program that prints squares of numbers up to a given limit using a **while loop**.
   
   **Solution:**
   ```java
   int limit = 20;
   int number = 1;
   
   while (number * number <= limit) {
       System.out.println(number * number);
       number++;
   }
   ```

### **Puzzle 2: Sum of Even Numbers Using While Loop**
   - Write a program to find the sum of even numbers up to a limit using a **while loop**.
   
   **Solution:**
   ```java
   int limit = 10;
   int sum = 0;
   int number = 1;
   
   while (number <= limit) {
       if (number % 2 == 0) {
           sum += number;
       }
       number++;
   }
   
   System.out.println("Sum of even numbers: " + sum);
   ```

### **New Quiz Questions:**

1. **Which of the following is true about a `while` loop?**
   - A) It may not execute even once if the condition is false initially. (Answer: A)
   - B) It always executes at least once.
   - C) It is used for counting loops.

2. **What is the output of the following code?**
   ```java
   int i = 0;
   while (i < 3) {
       System.out.println(i);
       i++;
   }
   ```
   - A) 0 1 2 (Answer: A)
   - B) 1 2 3
   - C) 0 1 2 3

### **Fun Fact:**
- **Fun Fact:** The **while loop** is used when the number of iterations is unknown and determined by a condition.

---

### **Group 3: (Steps 07, 08)**

- **Step 07:** Do While Loop in Java - An Introduction
- **Step 08:** Do While Loop in Java - An Example - Cube while user enters positive numbers

**Why Grouped**: These steps focus on the do-while loop, its syntax, and a practical example where the loop continues based on user input.

### **Puzzle 1: Cube Calculator with Do-While Loop**
   - Write a program that asks the user for a number and prints the cube of the number. Continue until the user enters a negative number.
   
   **Solution:**
   ```java
   Scanner scanner = new Scanner(System.in);
   int number;
   
   do {
       System.out.print("Enter a number: ");
       number = scanner.nextInt();
       if (number >= 0) {
           System.out.println("Cube: " + (number * number * number));
       }
   } while (number >= 0);
   
   System.out.println("Program ended.");
   ```

### **Puzzle 2: Guess the Number Using Do-While**
   - Write a program that keeps asking the user to guess a number until they guess correctly using a **do-while loop**.

   **Solution:**
   ```java
   Scanner scanner = new Scanner(System.in);
   int secretNumber = 7;
   int guess;
   
   do {
       System.out.print("Guess the number: ");
       guess = scanner.nextInt();
       if (guess != secretNumber) {
           System.out.println("Try again.");
       }
   } while (guess != secretNumber);
   
   System.out.println("You guessed it!");
   ```

### **New Quiz Questions:**

1. **What is the key difference between a `while` and a `do-while` loop?**
   - A) `while` checks the condition first, `do-while` checks it after. (Answer: A)
   - B) Both execute at least once.
   - C) They are identical.

2. **Which of the following scenarios best suits a `do-while` loop?**
   - A) Executing a loop when the number of iterations is known beforehand.
   - B) Ensuring the loop body executes at least once. (Answer: B)
   - C) Looping based on a counter.

### **Fun Fact:**
- **Fun Fact:** The **do-while loop** is often used when the code inside the loop needs to be executed at least once before any condition is checked.

---

### **Group 4: Break, Continue, and Loop Selection (Steps 09, 10)**

- **Step 09:** Introduction to Break and Continue
- **Step 10:** Selecting Loop in Java - For vs While vs Do While

**Why Grouped**: These steps explain break and continue statements and compare the different types of loops, helping learners understand when to use each loop.

### **Puzzle 1: Break a Loop**
   - Write a program that prints numbers from 1 to 10 but stops when it reaches 5 using the `break` statement.
   
   **Solution:**
   ```java
   for (int i = 1; i <= 10; i++) {
       if (i == 5) {
           break;
       }
       System.out.println(i);
   }
   ```

### **Puzzle 2: Continue in a Loop**
   - Write a program that prints numbers from 1 to 10 but skips the number 5 using the `continue` statement.

   **Solution:**
   ```java
   for (int i = 1; i <= 10; i++) {
       if (i == 5) {
           continue;
       }
       System.out.println(i);
   }
   ```

### **New Quiz Questions:**

1. **What does the `break` statement do in a loop?**
   - A) Exits the loop immediately. (Answer: A)
   - B) Skips to the next iteration.
   - C) Continues the loop.

2. **What is the difference between a `continue` and a `break` statement?**
   - A) `continue` skips the rest of the loop body and proceeds to the next iteration, while `break` exits the loop entirely. (Answer: A)
   - B) They both exit the loop.
   - C) Both skip to the next iteration.

### **Fun Fact:**
- **Fun Fact:** Using **break** and **continue** can make code harder to understand, so it’s often recommended to avoid them when possible.

---

### Additional Coding Exercises

### **Exercise 1: Prime Number Finder with Break and Continue**
**Objective:** Write a program that finds and prints prime numbers between 1 and a user-defined limit using a **for loop**.

The program should break the loop if the prime count reaches a specific number (e.g., stop after finding 5 primes) and use **continue** to skip non-prime numbers.

**Code:**
```java
import java.util.Scanner;

public class PrimeNumberFinder {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a limit: ");
        int limit = scanner.nextInt();
        System.out.print("Enter the number of primes to find: ");
        int primeCount = scanner.nextInt();

        int count = 0;
        for (int i = 2; i <= limit; i++) {
            if (!isPrime(i)) {
                continue; // Skip non-prime numbers
            }
            System.out.println(i + " is a prime number.");
            count++;
            if (count == primeCount) {
                break; // Stop after finding the required number of primes
            }
        }
    }

    private static boolean isPrime(int number) {
        for (int i = 2; i <= number / 2; i++) {
            if (number % i == 0) {
                return false;
            }
        }
        return true;
    }
}
```

**Output:**
```java
Enter a limit: 20
Enter the number of primes to find: 5
2 is a prime number.
3 is a prime number.
5 is a prime number.
7 is a prime number.
11 is a prime number.
```

---

### **Exercise 2: Sum of Odd Numbers Using While Loop**
**Objective:** Create a program that calculates the sum of all odd numbers between 1 and a user-defined number using a **while loop**.

**Code:**
```java
import java.util.Scanner;

public class SumOfOddNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the limit: ");
        int limit = scanner.nextInt();
        
        int number = 1;
        int sum = 0;
        
        while (number <= limit) {
            if (number % 2 != 0) { // Check if the number is odd
                sum += number;
            }
            number++;
        }
        
        System.out.println("Sum of odd numbers up to " + limit + " is: " + sum);
    }
}
```
  
**Output:**
```
Enter the limit: 10
Sum of odd numbers up to 10 is: 25
```

---

### **Exercise 3: Guess the Number with Do-While Loop**
**Objective:** Write a guessing game where the computer selects a random number between 1 and 100, and the player has to guess the number.

The game continues until the correct number is guessed, using a **do-while loop**.

**Code:**
```java
import java.util.Scanner;

public class GuessTheNumberGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int secretNumber = (int) (Math.random() * 100 + 1);
        int guess;
        
        System.out.println("Guess the number between 1 and 100!");

        do {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            
            if (guess < secretNumber) {
                System.out.println("Too low! Try again.");
            } else if (guess > secretNumber) {
                System.out.println("Too high! Try again.");
            }
        } while (guess != secretNumber);
        
        System.out.println("Congratulations! You guessed the number: " + secretNumber);
    }
}
```

**Output:**
```java
Guess the number between 1 and 100!
Enter your guess: 50
Too low! Try again.
Enter your guess: 75
Too high! Try again.
Enter your guess: 63
Congratulations! You guessed the number: 63
```

---

### **Exercise 4 (Game): Multiplication Quiz Using For Loop**
**Objective:** Create a simple multiplication quiz game where the player answers a series of multiplication problems. The game should provide feedback and calculate the score at the end.

**Code:**
```java
import java.util.Scanner;

public class MultiplicationQuizGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int score = 0;
        
        for (int i = 1; i <= 5; i++) {
            int num1 = (int) (Math.random() * 10 + 1);
            int num2 = (int) (Math.random() * 10 + 1);
            
            System.out.print("Question " + i + ": What is " + num1 + " * " + num2 + "? ");
            int answer = scanner.nextInt();
            
            if (answer == num1 * num2) {
                System.out.println("Correct!");
                score++;
            } else {
                System.out.println("Wrong! The correct answer is " + (num1 * num2));
            }
        }
        
        System.out.println("Your final score is: " + score + "/5");
    }
}
```

**Output:**
```java
Question 1: What is 3 * 7? 21
Correct!
Question 2: What is 5 * 6? 30
Correct!
...
Your final score is: 4/5
```

---

## Section 16: Reference Types in Java Programming

#### **Group 1: Steps 01, 02 – Introduction to Reference Types and Memory**
- **Step 01:** Reference Types - How are they stored in Memory?
- **Step 02:** Java Reference Types - Puzzles

**Why Grouped**: These steps focus on how reference types are stored in memory and introduce puzzles to test learners' understanding.

### **Puzzle 1: What is stored in reference variables?**
   - Given the code snippet:
   ```java
   Animal dog = new Animal(12);
   Animal cat = new Animal(15);
   ```
   What is actually stored in `dog` and `cat`?

   **Answer:**
   - `dog` and `cat` store the memory addresses (references) of the actual `Animal` objects in the heap, not the values themselves.

### **Puzzle 2: What happens when reference variables are copied?**
   - If you set `nothing = cat;` and modify `nothing.id = 10;`, what happens to `cat.id`?

   **Answer:**
   - `cat.id` also becomes `10` because `nothing` and `cat` are both pointing to the same object in memory.


### Existing Quiz Questions:

1.	What is the purpose of reference variables in Java?

    - A) To store primitive values
    - B) To store objects on the Heap
    - C) To store the memory location of an object (Answer: C)

2.	What is the value of a reference variable that is not initialized by the programmer in Java?

    - A) 0
    - B) Empty
    - C) Null (Answer: C)

3.	What happens when you compare two reference variables in Java?

    - A) It compares the values stored inside the referenced objects.
    - B) It compares the memory locations where the objects are stored. (Answer: B)
    - C) It compares the size of the objects.

4.	What happens when you assign one reference variable to another in Java?

    - A) It creates a copy of the entire referenced object.
    - B) It only copies the reference. (Answer: B)
    - C) It creates a new object with the same values as the referenced object.

### New Quiz Questions:

1. **How are reference types stored in memory in Java?**

    - A) By storing the value directly
    - B) By storing a reference to the value (Answer: B)
    - C) By storing both the value and the reference

2. **What does the == operator compare for reference types?**

    - A) The memory reference (Answer: A)
    - B) The actual value
    - C) The type of object

### Fun Fact: 

In Java, strings are stored in a string pool for memory optimization, meaning identical string literals can share the same memory reference.

---

#### **Group 2: Steps 03, 04, 05, 06, 07 – String Class and String Handling**
- **Step 03:** String class - Introduction and Exercise - Print each word and char
- **Step 04:** String class - Exercise Solution and Some More Important Methods
- **Step 05:** Understanding String is Immutable and String Concat, Upper Case, Lower Case
- **Step 06:** String Concatenation and Join, Replace Methods
- **Step 07:** Java String Alternatives - StringBuffer and StringBuilder

**Why Grouped**: These steps explore the String class, its immutability, key methods for manipulating strings, and introduce StringBuffer and StringBuilder for mutable string handling.

### **Puzzle 1: Print Each Word in a String**
   - Write a program to print each word and character of the string "Java is awesome" on a new line.
   
   **Code:**
   ```java
   String sentence = "Java is awesome";
   String[] words = sentence.split(" ");
   for (String word : words) {
       System.out.println("Word: " + word);
       for (char c : word.toCharArray()) {
           System.out.println("Character: " + c);
       }
   }
   ```
   **Output**
```
Word: Java
Character: J
Character: a
Character: v
Character: a
Word: is
Character: i
Character: s
Word: awesome
Character: a
Character: w
Character: e
Character: s
Character: o
Character: m
Character: e
```


### **Puzzle 2: Compare `StringBuilder` and `StringBuffer`**
   - Write code that demonstrates the performance difference between **StringBuilder** and **StringBuffer** for appending multiple strings.

   **Code:**
   ```java
   StringBuilder sb = new StringBuilder();
   long startTime = System.nanoTime();
   for (int i = 0; i < 10000; i++) {
       sb.append("Java");
   }
   long endTime = System.nanoTime();
   System.out.println("StringBuilder time: " + (endTime - startTime) + " ns");

   StringBuffer sbf = new StringBuffer();
   startTime = System.nanoTime();
   for (int i = 0; i < 10000; i++) {
       sbf.append("Java");
   }
   endTime = System.nanoTime();
   System.out.println("StringBuffer time: " + (endTime - startTime) + " ns");
   ```

**Output**

```java
StringBuilder time: 260000 ns
StringBuffer time: 340000 ns
```

### Existing Quiz Questions:

1. What is the output of the following code:

```java
String str = "Test";
System.out.println(str.charAt(2));
```

- A) e'
- B) s (Answer: B)
- C) T

2.	What is the meaning of the word “immutable”?

    - A) Changeable
    - B) Unchangeable (Answer: B)

3.	What is the difference between StringBuffer and StringBuilder?

    - A) StringBuffer is thread-safe while StringBuilder is not (Answer: A)
    - B) StringBuilder is thread-safe while StringBuffer is not
    - C) Both StringBuffer and StringBuilder are thread-safe


### New Quiz Questions:

1. **What is the main difference between StringBuilder and StringBuffer?**

    - A) StringBuilder is synchronized, StringBuffer is not
    - B) StringBuffer is synchronized, StringBuilder is not (Answer: B)
    - C) Both are synchronized

2. **Why are strings immutable in Java?**

    - A) To make strings more efficient for memory management (Answer: A)
    - B) To make strings changeable
    - C) To make strings thread-safe

### Fun Fact:

String immutability in Java ensures that strings can be shared safely between multiple threads without worrying about data corruption.

---

#### **Group 3: Steps 08, 09, 10 – Wrapper Classes**
- **Step 08:** Java Wrapper Classes - An Introduction - Why and What?
- **Step 09:** Java Wrapper Classes - Creation - Constructor and valueOf
- **Step 10:** Java Wrapper Classes - Auto Boxing and a Few Wrapper Constants

**Why Grouped**: These steps introduce wrapper classes, their usage, creation, and the concept of auto-boxing in Java.

### **Puzzle 1: Create a Wrapper Object**
   - Write code that demonstrates how to create a wrapper object using both the `new` keyword and the `valueOf` method.
   
   **Code:**
   ```java
   Integer integer1 = new Integer(5);
   Integer integer2 = Integer.valueOf(5);
   System.out.println(integer1 == integer2); // false, because different objects
   ```
**Output**

```java
false
```

### **Puzzle 2: Explore Wrapper Class Constants**
   - Use the **Integer.MAX_VALUE** and **Integer.MIN_VALUE** constants to print the maximum and minimum integer values.

   **Code:**
   ```java
   System.out.println("Max int value: " + Integer.MAX_VALUE);
   System.out.println("Min int value: " + Integer.MIN_VALUE);
   ```

**Output**

```java
Max int value: 2147483647
Min int value: -2147483648
```

### Existing Quiz Questions:

1. Which of these statements about creating Wrapper objects is TRUE?

    - A) new and valueOf() both create new objects every time.
    - B) There is no difference
    - C) new creates a new object every time, but valueOf() tries to reuse existing objects with the same value.
    - D) valueOf() creates a new object every time, but new reuses existing objects with the same value.

### New Quiz Questions:

1. **What is auto-boxing in Java?**

    - A) Automatically converting a primitive type to its corresponding wrapper class (Answer: A)
    - B) Automatically converting a wrapper class to a primitive type
    - C) Boxing multiple classes together

2. **Which of the following is a valid wrapper class in Java?**

    - A) Integer (Answer: A)
    - B) intWrapper
    - C) Primitive
  
### Fun Fact:

Java automatically converts between primitives and their wrapper class equivalents thanks to auto-boxing and unboxing, reducing the need for manual conversion.

---

#### **Group 4: Steps 11, 12, 13 – Java Dates**
- **Step 11:** Java Dates - Introduction to LocalDate, LocalTime and LocalDateTime
- **Step 12:** Java Dates - Exploring LocalDate - Creation and Methods to play with Dates
- **Step 13:** Java Dates - Exploring LocalDate - Comparing Dates and Creating Specific Dates

**Why Grouped**: These steps focus on Java's date and time classes and explain how to work with LocalDate, LocalTime, and LocalDateTime.

### **Puzzle 1: Print Current Date and Time**
   - Write a program to print the current date, time, and date-time using **LocalDate**, **LocalTime**, and **LocalDateTime**.

   **Code:**
   ```java
   import java.time.LocalDate;
   import java.time.LocalTime;
   import java.time.LocalDateTime;

   public class DateTimeExample {
       public static void main(String[] args) {
           LocalDate date = LocalDate.now();
           LocalTime time = LocalTime.now();
           LocalDateTime dateTime = LocalDateTime.now();
           System.out.println("Current Date: " + date);
           System.out.println("Current Time: " + time);
           System.out.println("Current DateTime: " + dateTime);
       }
   }
   ```

**Output**

```java
Current Date: 2024-10-22
Current Time: 14:35:45.234
Current DateTime: 2024-10-22T14:35:45.234
```


### **Puzzle 2: Create and Compare Dates**
   - Write a program that creates two **LocalDate** objects and compares them.

   **Answer:**
   ```java
   import java.time.LocalDate;

   public class DateComparison {
       public static void main(String[] args) {
           LocalDate date1 = LocalDate.of(2020, 5, 15);
           LocalDate date2 = LocalDate.of(2023, 8, 10);
           System.out.println("Is date1 before date2? " + date1.isBefore(date2));
       }
   }
   ```

**Output**

```java
Is date1 before date2? true
```

### New Quiz Questions:

1. **Which class is used to represent a date in Java 8?**

    - A) Date
    - B) LocalDate (Answer: B)
    - C) DateTime

2. **How do you get the current date in Java 8?**

    - A) LocalDate.now() (Answer: A)
    - B) System.currentDate()
    - C) Date.new()

### Fun Fact:

Java's LocalDate and LocalDateTime classes introduced in Java 8 provide an immutable and thread-safe way to handle date and time information.

---

#### **Group 5: Step 14 – Conclusion of Reference Types**
- **Step 14:** Java Reference Types - Conclusion

**Why Grouped**: This is the conclusion of the Reference Types section, summarizing everything covered.

### **Fun Fact:**

Java introduced the **LocalDate** and **LocalDateTime** classes in **Java 8**, improving the handling of dates and times by making them thread-safe and immutable, unlike the older `java.util.Date` class.

---

### Additional Coding Exercises

### **Exercise 1: Creating and Managing Animals in a Zoo**
**Description:** Create a system for managing animals in a zoo. Each animal has an ID, name, and type (e.g., Mammal, Bird, Reptile).

Use a `Map<String, Animal>` to store animals, where the key is the animal's name and the value is an `Animal` object. Implement functions to add animals, display all animals, and find an animal by name.

**Code :**
```java
import java.util.HashMap;
import java.util.Map;

class Animal {
    private int id;
    private String name;
    private String type;

    public Animal(int id, String name, String type) {
        this.id = id;
        this.name = name;
        this.type = type;
    }

    public String getName() {
        return name;
    }

    public String getType() {
        return type;
    }

    @Override
    public String toString() {
        return "Animal[ID=" + id + ", Name=" + name + ", Type=" + type + "]";
    }
}

public class Zoo {
    private Map<String, Animal> animals = new HashMap<>();

    public void addAnimal(Animal animal) {
        animals.put(animal.getName(), animal);
    }

    public void displayAnimals() {
        for (Animal animal : animals.values()) {
            System.out.println(animal);
        }
    }

    public Animal findAnimalByName(String name) {
        return animals.get(name);
    }

    public static void main(String[] args) {
        Zoo zoo = new Zoo();
        zoo.addAnimal(new Animal(1, "Lion", "Mammal"));
        zoo.addAnimal(new Animal(2, "Parrot", "Bird"));
        zoo.addAnimal(new Animal(3, "Crocodile", "Reptile"));

        zoo.displayAnimals();

        Animal animal = zoo.findAnimalByName("Parrot");
        System.out.println("Found Animal: " + animal);
    }
}
```

**Output:**
```java
Animal[ID=1, Name=Lion, Type=Mammal]
Animal[ID=2, Name=Parrot, Type=Bird]
Animal[ID=3, Name=Crocodile, Type=Reptile]
Found Animal: Animal[ID=2, Name=Parrot, Type=Bird]
```

---

### **Exercise 2: Word Frequency Counter using Strings**
**Description:** Write a program that takes a paragraph as input and calculates the frequency of each word in the paragraph. Ignore case sensitivity and punctuation.

**Code:**
```java
import java.util.HashMap;
import java.util.Map;

public class WordFrequencyCounter {
    public static void main(String[] args) {
        String paragraph = "Java is awesome. Java is versatile. Java is widely used.";
        String[] words = paragraph.toLowerCase().replaceAll("[^a-z ]", "").split(" ");

        Map<String, Integer> wordCount = new HashMap<>();
        for (String word : words) {
            wordCount.put(word, wordCount.getOrDefault(word, 0) + 1);
        }

        for (Map.Entry<String, Integer> entry : wordCount.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

**Output:**
```java
java: 3
is: 3
awesome: 1
versatile: 1
widely: 1
used: 1
```

---

### **Exercise 3: Wrapper Class Challenge – Finding Maximum Integer**
**Description:** Create a program that reads a list of integers (as strings) and determines the maximum value using wrapper classes.

The input should be handled as strings and converted to integers using `Integer.parseInt()`.

**Code:**
```java
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class MaxIntegerFinder {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<String> inputs = new ArrayList<>();

        System.out.println("Enter integers (type 'done' to stop):");
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("done")) {
                break;
            }
            inputs.add(input);
        }

        int max = Integer.MIN_VALUE;
        for (String input : inputs) {
            int number = Integer.parseInt(input);
            if (number > max) {
                max = number;
            }
        }

        System.out.println("The maximum number is: " + max);
    }
}
```

**Output:**
```java
Enter integers (type 'done' to stop):
5
12
7
19
done
The maximum number is: 19
```

---

### **Exercise 4 (Game): "Guess the Animal" Game**
**Description:** Create a simple "Guess the Animal" game where the player thinks of an animal, and the program tries to guess it by asking yes/no questions.

Use an `ArrayList<String>` to store a small set of animals, and the program eliminates options based on user responses.

**Code Snippet:**
```java
import java.util.ArrayList;
import java.util.Scanner;

public class GuessTheAnimalGame {
    public static void main(String[] args) {
        ArrayList<String> animals = new ArrayList<>();
        animals.add("Lion");
        animals.add("Elephant");
        animals.add("Eagle");
        animals.add("Shark");

        Scanner scanner = new Scanner(System.in);

        System.out.println("Think of an animal from this list: Lion, Elephant, Eagle, Shark.");
        System.out.println("I will try to guess it by asking yes/no questions.");

        String guessedAnimal = null;

        for (String animal : animals) {
            System.out.println("Is it a " + animal + "? (yes/no)");
            String answer = scanner.nextLine();

            if (answer.equalsIgnoreCase("yes")) {
                guessedAnimal = animal;
                break;
            }
        }

        if (guessedAnimal != null) {
            System.out.println("I guessed it! The animal is a " + guessedAnimal + "!");
        } else {
            System.out.println("I couldn't guess the animal.");
        }
    }
}
```

**Output:**
```
Think of an animal from this list: Lion, Elephant, Eagle, Shark.
I will try to guess it by asking yes/no questions.
Is it a Lion? (yes/no)
no
Is it an Elephant? (yes/no)
yes
I guessed it! The animal is a Elephant!
```

---

## Arrays and ArrayLists in Java Programming

#### **Group 1: Steps 01, 02, 03, 04 – Basics of Arrays and Array Manipulation**
- **Step 01**: Understanding the need and Basics about an Array
- **Step 02**: Java Arrays - Creating and Accessing Values - Introduction
- **Step 03**: Java Arrays - Puzzles - Arrays of Objects, Primitive Data Types, toString
- **Step 04**: Java Arrays - Compare, Sort and Fill

**Why grouped:** Basics of Arrays and Array Manipulation: Focuses on introducing arrays, accessing values, performing operations, and basic manipulations like sorting and filling.

### 1. **Puzzle: Calculate the Sum of Array Elements**
   - Write a program to calculate the sum of elements in an integer array. Given an array of integers, find the total sum using a loop.
   ```java
   int[] numbers = {10, 20, 30, 40};
   int sum = 0;
   for (int num : numbers) {
       sum += num;
   }
   System.out.println("Total sum: " + sum);
   ```
   **Output:**
   ```
   Total sum: 100
   ```

### 2. **Puzzle: Sorting an Array of Strings**
   - Given an array of strings, use the `Arrays.sort()` method to arrange them in alphabetical order. Test it with a set of words.
   ```java
   String[] words = {"banana", "apple", "cherry", "date"};
   Arrays.sort(words);
   System.out.println(Arrays.toString(words));
   ```
   **Output:**
   ```
   [apple, banana, cherry, date]
   ```

### **Existing Quiz Questions:**

1.	Why do we use arrays?

    - A) To store different types of data
    - B) To store similar types of data in a structured and organized manner. (Answer: B)
    - C) To store data in an unorganized manner.

2.	What is the purpose of enhanced for loop in arrays?

    - A) Stores elements in the array.
    - B) Accesses elements from the array.
    - C) Iterate through all elements in the array with very simple syntax (Answer: C)

3.	How can we access elements from an array?

    - A) By using the indexing operator, [] (Answer: A)
    - B) By using the length property of the array.

4.	What is the length property in arrays used for?

    - A) To find the number of elements in an array. (Answer: A)
    - B) To find the value of an element in an array.

5.	What is the value of an array element of type int when it is NOT initialized?

    - A) Null
    - B) False
    - C) 0 (Answer: C)

6.	What is the purpose of the method Arrays.fill?

    - A) To compare two arrays
    - B) To fill an array with a specified value (Answer: B)
    - C) To perform an in-position sorting of elements
    - D) To store zero or more number of elements in an array

7.	What is the output of the following code?

```java
  int[] marks = new int[5];
  Arrays.fill(marks, 100);
  System.out.println(marks);
```

- A) [100,100,100,100,100] (Answer: A)
- B) [0,0,0,0,0]

8. What is the result of the following code?

```java
int []
array1 = {1, 2, 3};
int []
array2 = {1, 2, 3};
System.out.println(Arrays.equals(array1, array2));
```

- A) false
- B) true (Answer: B)

### **New Quiz Questions:**


1. What is the primary advantage of using an array?
   - **A)** It allows storing different data types.
   - **B)** It allows storing multiple values of the same data type. **(Answer: B)**
   - **C)** It automatically resizes itself.

2. Which of these is the correct syntax to create an array in Java?
   - **A)** `int[] numbers = new int[5];` **(Answer: A)**
   - **B)** `int numbers[5];`
   - **C)** `int numbers = new int(5);`

3. What will happen if you try to access an element outside the bounds of an array?
   - **A)** The program will compile with a warning.
   - **B)** An `ArrayIndexOutOfBoundsException` will be thrown. **(Answer: B)**
   - **C)** The program will ignore the out-of-bound access.

### **Fun Fact:**
- **Arrays in Ancient Programming:** Arrays were first formally introduced in the FORTRAN language in the 1950s and have since become fundamental in almost every programming language.

---

#### **Group 2: Steps 05, 06, 07, 08, 09 – Array Exercises and Variable Arguments**
- **Step 05**: Java Arrays - Exercise - Create Student Class - Part 1 - Total and Average
- **Step 06**: Java Arrays - Exercise - Create Student Class - Part 2 - Maximum and Minimum
- **Step 07**: Introduction to Variable Arguments - Need
- **Step 08**: Introduction to Variable Arguments - Basics
- **Step 09**: Introduction to Variable Arguments - Enhancing Student Class

**Why grouped:** Array Exercises and Variable Arguments: Covers exercises using arrays in a Student class, including calculations like total, average, maximum, minimum, and an introduction to variable arguments to enhance flexibility.

### 1. **Puzzle: Calculating the Average Score**
   - Create an array of scores and write a method to calculate the average score. Use variable arguments to allow flexibility in the number of scores passed.
   ```java
   public class AverageScore {
       public static double calculateAverage(int... scores) {
           int sum = 0;
           for (int score : scores) {
               sum += score;
           }
           return (double) sum / scores.length;
       }

       public static void main(String[] args) {
           System.out.println("Average Score: " + calculateAverage(85, 90, 78, 92));
       }
   }
   ```
   **Output:**
   ```
   Average Score: 86.25
   ```

### 2. **Puzzle: Finding Maximum and Minimum Marks**
   - Write a `Student` class with an array of marks. Create methods to calculate the maximum and minimum marks.
   ```java
   class Student {
       int[] marks = {88, 74, 96, 85, 91};

       public int getMaxMark() {
           int max = marks[0];
           for (int mark : marks) {
               if (mark > max) max = mark;
           }
           return max;
       }

       public int getMinMark() {
           int min = marks[0];
           for (int mark : marks) {
               if (mark < min) min = mark;
           }
           return min;
       }
   }

   public class Main {
       public static void main(String[] args) {
           Student student = new Student();
           System.out.println("Max Mark: " + student.getMaxMark());
           System.out.println("Min Mark: " + student.getMinMark());
       }
   }
   ```
   **Output:**
   ```
   Max Mark: 96
   Min Mark: 74
   ```

### **Existing Quiz Questions:**

1.	Where should the variable arguments list be placed in the list of arguments passed to a function?

    - A) At the beginning
    - B) In the middle
    - C) At the end (Answer: C)

2.	Which of these is an example of a variable argument method?

    - A) public int getNumberOfMarks()
    - B) public int[] getMarks()
    - C) public Student(String name, int... marks) (Answer: C)

3.	What happens if you pass the wrong data type to a variable argument method?

    - A) The Java compiler will throw an error. (Answer: A)
    - B) The program will run, but with unexpected results.
    - C) The program will crash.


### **New Quiz Questions:**

1. What is the benefit of using variable arguments in a method?
   - **A)** It allows a method to accept a variable number of parameters. **(Answer: A)**
   - **B)** It restricts the method to accept only integers.
   - **C)** It simplifies the method to accept arrays only.

2. When using `variable arguments`, which of the following is correct?
   - **A)** Variable arguments can be placed anywhere in the parameter list.
   - **B)** Variable arguments must be the last parameter. **(Answer: B)**
   - **C)** Variable arguments must be the first parameter.

### **Fun Fact:**
- **Variable Arguments in Java 5:** Variable arguments (varargs) were introduced in Java 5 to simplify working with methods that accept an unknown number of parameters, a feature influenced by languages like Python.

---

#### **Group 3: Steps 10, 11, 12 – Arrays of Objects and Limitations**
- **Step 10**: Java Arrays - Using Person Objects and String Elements with Exercises
- **Step 11**: Java String Arrays - Exercise Solutions - Print Day of Week with Most Occurrences
- **Step 12**: Adding and Removing Marks - Problem with Arrays

**Why grouped:** Arrays of Objects and Limitations: Delves into handling arrays of objects (e.g., Person), string array exercises, and discusses the limitations of arrays, such as fixed size.

### 1. **Puzzle: Identify Longest Day of the Week**
   - Create an array of the days of the week and identify the day with the most characters.
   ```java
   String[] daysOfWeek = {"Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"};
   String longestDay = "";
   for (String day : daysOfWeek) {
       if (day.length() > longestDay.length()) {
           longestDay = day;
       }
   }
   System.out.println("Longest day: " + longestDay);
   ```
   **Output:**
   ```
   Longest day: Wednesday
   ```

### 2. **Puzzle: Reversing Days of the Week**
   - Print the days of the week in reverse order.
   ```java
   for (int i = daysOfWeek.length - 1; i >= 0; i--) {
       System.out.println(daysOfWeek[i]);
   }
   ```
   **Output:**
   ```
   Saturday
   Friday
   Thursday
   Wednesday
   Tuesday
   Monday
   Sunday
   ```

### **Existing Quiz Questions:**

1.	When creating an array of objects, what does the array hold?

    - A) The actual objects themselves
    - B) Copies of the objects
    - C) References to the created objects (Answer: C)

2.	Why is it difficult to add or remove elements in an array?

    - A) Because the size of an array is fixed (Answer: A)
    - B) Because arrays are only for primitive types
    - C) Because arrays cannot store non-homogeneous types

### **New Quiz Questions:**

1. What will be the default value for unassigned elements in an array of integers?
   - **A)** `null`
   - **B)** `0` **(Answer: B)**
   - **C)** `undefined`

2. Which exception is thrown if you try to access an invalid index in an array?
   - **A)** `NullPointerException`
   - **B)** `IndexOutOfBoundsException` **(Answer: B)**
   - **C)** `ArrayIndexOutOfBoundsException`

### **Fun Fact:**
- **Fixed-Size Array Limitation:** In many programming languages, including Java, arrays have a fixed size, which led to the development of dynamic data structures like ArrayLists.

---

#### **Group 4: Steps 13, 14, 15, 16 – ArrayList Basics and Student Class Refactoring**
- **Step 13**: First Look at ArrayList - An Introduction
- **Step 14**: First Look at ArrayList - Refactoring Student Class to use ArrayList
- **Step 15**: First Look at ArrayList - Enhancing Student Class with Add and Remove
- **Step 16**: Introduction to Array and ArrayList - Conclusion

**Why grouped:** ArrayList Basics and Student Class Refactoring: Introduces ArrayLists, refactors the Student class to use ArrayLists instead of arrays, and explores enhanced functionality like adding and removing elements.

### 1. **Puzzle: Manage a List of Favorite Books**
   - Create an ArrayList to store your favorite books. Add, remove, and display books using ArrayList methods.
   ```java
   ArrayList<String> books = new ArrayList<>();
   books.add("The Hobbit");
   books.add("1984");
   books.add("To Kill a Mockingbird");
   books.remove("1984");
   System.out.println(books);
   ```
   **Output:**
   ```
   [The Hobbit, To Kill a Mockingbird]
   ```

### 2. **Puzzle: Convert an Array to an ArrayList**
   - Convert an array of integers into an ArrayList and find the sum of its elements.
   ```java
   Integer[] array = {5, 10, 15, 20};
   ArrayList<Integer> list = new ArrayList<>(Arrays.asList(array));
   int sum = 0;
   for (int num : list) {
       sum += num;
   }
   System.out.println("Sum: " + sum);
   ```
   **Output:**
   ```
   Sum: 50
   ```

### **Existing Quiz Questions:**

1.	What is the main advantage of ArrayList over arrays?

    - A) Arrays can store only primitive types
    - B) ArrayList provides operations to add and remove elements (Answer: B)
    - C) ArrayList has a fixed size

2.	How do you remove an element from an ArrayList?

    - A) Using the remove() method (Answer: A)
    - B) Using the delete() method
    - C) Using the clear() method

3.	What method can be used to find the maximum value in an ArrayList?

    - A) Collections.max() (Answer: A)
    - B) ArrayList.max()
    - C) ArrayList.getMaximum()

### **New Quiz Questions:**

1. Which method is used to add an element to an ArrayList?
   - **A)** `put()`
   - **B)** `add()` **(Answer: B)**
   - **C)** `insert()`

2. How can you initialize an ArrayList with values?
   - **A)** `new ArrayList(Arrays.asList(values))` **(Answer: A)**
   - **B)** `ArrayList(values)`
   - **C)** `new ArrayList{values}`

### **Fun Fact:**
- **ArrayLists in Java Collections:** The ArrayList in Java is part of the Collections Framework and provides a dynamic alternative to arrays, allowing resizing, addition, and removal of elements at any point.

---

### Additional Coding Exercises

### **Exercise 1: Student Gradebook with ArrayList**

**Description**: Create a `Gradebook` class where students’ names and their respective grades are stored in an ArrayList. The program should allow adding new students with grades, updating grades, and removing students.

This exercise reinforces ArrayList operations, such as adding, updating, and removing elements.

**Code**:

```java
import java.util.ArrayList;

class Gradebook {
    private ArrayList<String> students;
    private ArrayList<Integer> grades;

    public Gradebook() {
        students = new ArrayList<>();
        grades = new ArrayList<>();
    }

    public void addStudent(String name, int grade) {
        students.add(name);
        grades.add(grade);
    }

    public void updateGrade(String name, int newGrade) {
        int index = students.indexOf(name);
        if (index != -1) {
            grades.set(index, newGrade);
            System.out.println("Updated grade for " + name);
        } else {
            System.out.println("Student not found.");
        }
    }

    public void removeStudent(String name) {
        int index = students.indexOf(name);
        if (index != -1) {
            students.remove(index);
            grades.remove(index);
            System.out.println("Removed " + name + " from gradebook.");
        } else {
            System.out.println("Student not found.");
        }
    }

    public void display() {
        System.out.println("\nGradebook:");
        for (int i = 0; i < students.size(); i++) {
            System.out.println(students.get(i) + ": " + grades.get(i));
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Gradebook gradebook = new Gradebook();
        gradebook.addStudent("Alice", 88);
        gradebook.addStudent("Bob", 92);
        gradebook.addStudent("Charlie", 76);
        
        gradebook.display();

        gradebook.updateGrade("Alice", 90);
        gradebook.display();

        gradebook.removeStudent("Bob");
        gradebook.display();
    }
}
```

**Output**:

```
Gradebook:
Alice: 88
Bob: 92
Charlie: 76

Updated grade for Alice

Gradebook:
Alice: 90
Bob: 92
Charlie: 76

Removed Bob from gradebook.

Gradebook:
Alice: 90
Charlie: 76
```

---

### **Exercise 2: Dynamic Inventory System with Arrays**

**Description**: Implement an inventory system for a store using arrays to store product names and quantities. Allow the user to add new items, update item quantities, and view the inventory.

This exercise enhances skills in accessing and updating array elements.

**Code**:

```java
import java.util.Arrays;

class Inventory {
    private String[] products;
    private int[] quantities;
    private int size;

    public Inventory(int capacity) {
        products = new String[capacity];
        quantities = new int[capacity];
        size = 0;
    }

    public void addProduct(String product, int quantity) {
        if (size < products.length) {
            products[size] = product;
            quantities[size] = quantity;
            size++;
        } else {
            System.out.println("Inventory full! Cannot add more products.");
        }
    }

    public void updateQuantity(String product, int quantity) {
        for (int i = 0; i < size; i++) {
            if (products[i].equals(product)) {
                quantities[i] = quantity;
                System.out.println("Updated quantity for " + product);
                return;
            }
        }
        System.out.println("Product not found in inventory.");
    }

    public void displayInventory() {
        System.out.println("\nInventory:");
        for (int i = 0; i < size; i++) {
            System.out.println(products[i] + ": " + quantities[i] + " units");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Inventory inventory = new Inventory(5);

        inventory.addProduct("Apple", 50);
        inventory.addProduct("Banana", 30);
        inventory.displayInventory();

        inventory.updateQuantity("Apple", 70);
        inventory.displayInventory();
    }
}
```

**Output**:

```
Inventory:
Apple: 50 units
Banana: 30 units

Updated quantity for Apple

Inventory:
Apple: 70 units
Banana: 30 units
```

---

### **Exercise 3: Rock-Paper-Scissors Game**

**Description**: Develop a simple Rock-Paper-Scissors game where the player competes against the computer. Use an array to store the game choices.

This exercise focuses on comparing values within arrays.

**Code**:

```java
import java.util.Random;
import java.util.Scanner;

public class RockPaperScissors {
    public static void main(String[] args) {
        String[] choices = {"Rock", "Paper", "Scissors"};
        Random random = new Random();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Let's play Rock, Paper, Scissors!");
        System.out.println("Enter Rock, Paper, or Scissors:");

        String userChoice = scanner.nextLine();
        String computerChoice = choices[random.nextInt(3)];

        System.out.println("Computer chose: " + computerChoice);

        if (userChoice.equalsIgnoreCase(computerChoice)) {
            System.out.println("It's a tie!");
        } else if ((userChoice.equalsIgnoreCase("Rock") && computerChoice.equals("Scissors")) ||
                   (userChoice.equalsIgnoreCase("Paper") && computerChoice.equals("Rock")) ||
                   (userChoice.equalsIgnoreCase("Scissors") && computerChoice.equals("Paper"))) {
            System.out.println("You win!");
        } else {
            System.out.println("Computer wins!");
        }
        scanner.close();
    }
}
```

**Output**:

```
Let's play Rock, Paper, Scissors!
Enter Rock, Paper, or Scissors:
Rock
Computer chose: Scissors
You win!
```

---

### **Exercise 4: Temperature Conversion Tracker (ArrayList)**

**Description**: Design a program that tracks temperature conversions. It accepts temperatures in Celsius and converts them to Fahrenheit, storing each conversion in an ArrayList.

This exercise emphasizes using ArrayList for dynamic storage and retrieval.

**Code**:

```java
import java.util.ArrayList;
import java.util.Scanner;

class TemperatureConversion {
    private ArrayList<Double> celsiusTemps;
    private ArrayList<Double> fahrenheitTemps;

    public TemperatureConversion() {
        celsiusTemps = new ArrayList<>();
        fahrenheitTemps = new ArrayList<>();
    }

    public void addTemperature(double celsius) {
        double fahrenheit = celsius * 9/5 + 32;
        celsiusTemps.add(celsius);
        fahrenheitTemps.add(fahrenheit);
    }

    public void displayConversions() {
        System.out.println("\nTemperature Conversions:");
        for (int i = 0; i < celsiusTemps.size(); i++) {
            System.out.println(celsiusTemps.get(i) + "°C = " + fahrenheitTemps.get(i) + "°F");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        TemperatureConversion converter = new TemperatureConversion();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter temperatures in Celsius to convert to Fahrenheit (type 'done' to finish):");

        while (true) {
            String input = scanner.nextLine();
            if (input.equalsIgnoreCase("done")) {
                break;
            }
            try {
                double celsius = Double.parseDouble(input);
                converter.addTemperature(celsius);
            } catch (NumberFormatException e) {
                System.out.println("Invalid input. Please enter a numeric value.");
            }
        }

        converter.displayConversions();
        scanner.close();
    }
}
```

**Output**:

```
Enter temperatures in Celsius to convert to Fahrenheit (type 'done' to finish):
25
100
done

Temperature Conversions:
25.0°C = 77.0°F
100.0°C = 212.0°F
```

---

### **Exercise 5: Word Scramble Game**

**Description**: Create a word scramble game where the program presents a scrambled version of a word, and the player has to guess the original word.

Use an array to store a list of words, and shuffle the letters of a word randomly each time it’s presented.

**Code**:

```java
import java.util.Arrays;
import java.util.Collections;
import java.util.List;
import java.util.Scanner;

public class WordScrambleGame {
    public static void main(String[] args) {
        String[] words = {"java", "array", "list", "object", "method"};
        Scanner scanner = new Scanner(System.in);

        for (String word : words) {
            String scrambledWord = scrambleWord(word);
            System.out.println("Guess the word: " + scrambledWord);
            
            String guess = scanner.nextLine();
            if (guess.equalsIgnoreCase(word)) {
                System.out.println("Correct!");
            } else {
                System.out.println("Incorrect. The word was: " + word);
            }
        }
        System.out.println("Game over!");
        scanner.close();
    }

    public static String scrambleWord(String word) {
        List<String> letters = Arrays.asList(word.split(""));
        Collections.shuffle(letters);
        return String.join("", letters);
    }
}
```

**Output**:
```
Guess the word: jvaa
java
Correct!

Guess the word: btjeco
object
Correct!

Guess the word: htomed
method
Correct!

Game over!
```

---

### **Exercise 6: Number Memory Game**

**Description**: Develop a memory game where the program presents a sequence of numbers that the player must memorize. After a short delay, the numbers are hidden, and the player must input them in the correct order.

Use an ArrayList to store the sequence, and increase the length of the sequence as the player progresses.

**Code**:

```java
import java.util.ArrayList;
import java.util.Random;
import java.util.Scanner;
import java.util.concurrent.TimeUnit;

public class NumberMemoryGame {
    public static void main(String[] args) throws InterruptedException {
        ArrayList<Integer> sequence = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int level = 1;
        boolean playing = true;

        System.out.println("Welcome to the Number Memory Game!");

        while (playing) {
            // Generate a new number and add it to the sequence
            sequence.add(random.nextInt(10)); // Numbers 0-9
            System.out.print("Memorize this sequence: ");

            // Display the sequence to the player
            for (int num : sequence) {
                System.out.print(num + " ");
            }
            System.out.println();

            // Wait 3 seconds before clearing the screen
            TimeUnit.SECONDS.sleep(3);
            System.out.print("\033[H\033[2J"); // Clear console screen (may vary by environment)
            System.out.flush();

            System.out.println("Enter the sequence:");
            ArrayList<Integer> playerSequence = new ArrayList<>();

            // Get the player's input
            for (int i = 0; i < sequence.size(); i++) {
                playerSequence.add(scanner.nextInt());
            }

            // Check if the player's input matches the sequence
            if (playerSequence.equals(sequence)) {
                System.out.println("Correct! Moving to the next level.");
                level++;
            } else {
                System.out.println("Incorrect sequence. Game over! You reached level " + level + ".");
                playing = false;
            }
        }
        scanner.close();
    }
}
```

**Output**:
```
Welcome to the Number Memory Game!
Memorize this sequence: 7 2 

Enter the sequence:
7 2
Correct! Moving to the next level.

Memorize this sequence: 7 2 4 

Enter the sequence:
7 2 4
Correct! Moving to the next level.

Memorize this sequence: 7 2 4 9

Incorrect sequence. Game over! You reached level 3.
```

---

## Section 20: Java - Oriented Programming Again

### **Group 1: Steps 01, 02, and 03 – Basics of Designing a Class and Behavior**

- **Step 01 - Basics of Designing a Class - Class, Object, State, and Behavior**
- **Step 02 - OOPS Example - Fan Class - Deciding State and Constructors**
- **Step 03 - OOPS Example - Fan Class - Deciding Behavior with Methods**

**Why grouped**: These steps provide a foundational overview of object-oriented concepts like class, object, state, and behavior, and apply these to design the `Fan` class. This group covers the basics of constructing a class, establishing its state, and defining methods for behavior.

### 1. **Puzzle: Creating a Fan Class**
   - Create a simple `Fan` class with attributes `speed`, `isOn`, and `color`. Write methods to turn the fan on, change speed, and turn it off.
   ```java
   class Fan {
       private int speed;
       private boolean isOn;
       private String color;

       public Fan(String color) {
           this.speed = 0;
           this.isOn = false;
           this.color = color;
       }

       public void turnOn() {
           isOn = true;
           speed = 1;
           System.out.println("Fan is on.");
       }

       public void changeSpeed(int newSpeed) {
           if (isOn) {
               speed = newSpeed;
               System.out.println("Fan speed changed to " + speed);
           } else {
               System.out.println("Turn the fan on first.");
           }
       }

       public void turnOff() {
           isOn = false;
           speed = 0;
           System.out.println("Fan is off.");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Fan fan = new Fan("Blue");
           fan.turnOn();
           fan.changeSpeed(3);
           fan.turnOff();
       }
   }
   ```
   **Output:**
   ```
   Fan is on.
   Fan speed changed to 3
   Fan is off.
   ```

### **Existing Quiz Questions:**

1.	What are used to send instructions/messages to an object?

    - A) Attributes
    - B) Methods (Answer: B)
    - C) Constructors

2.	What corresponds to the state of an object?

    - A) Member variables (Answer: A)
    - B) Methods
    - C) Constructors

3.	What is the purpose of constructors in a class?

    - A) To define behavior
    - B) To create objects (Answer: B)


### **New Quiz Questions:**

1. **What is the purpose of defining a constructor in a class?**
   - A) To provide an alternate name for the class
   - B) To initialize object state when created **(Answer: B)**
   - C) To define the class’s default behavior

2. **What does an object represent in OOP?**
   - A) An instance of a class with specific state and behavior **(Answer: A)**
   - B) A blueprint for creating classes
   - C) A set of rules for program structure

### **Fun Fact:**
- **Fun Fact:** The term "object" in OOP comes from real-life objects, as OOP was designed to mimic the way humans perceive entities with attributes and actions.

---

### **Group 2: Steps 04, 05, and 06 – Object Composition and Class Exercises**

- **Step 04 - OOPS Exercise - Rectangle Class**
- **Step 05 - Understanding Object Composition with Customer Address Example**
- **Step 06 - Understanding Object Composition - An Exercise - Books and Reviews**

**Why grouped**: This set delves into more practical exercises in class design, focusing on the `Rectangle` class and understanding object composition. These exercises introduce how classes can hold other classes as components, enhancing understanding of composite relationships in OOP.

### 1. **Puzzle: Rectangle Area and Perimeter Calculator**
   - Write a `Rectangle` class with `width` and `height` attributes. Create methods to calculate the area and perimeter.
   ```java
   class Rectangle {
       private int width;
       private int height;

       public Rectangle(int width, int height) {
           this.width = width;
           this.height = height;
       }

       public int area() {
           return width * height;
       }

       public int perimeter() {
           return 2 * (width + height);
       }
   }

   public class Main {
       public static void main(String[] args) {
           Rectangle rectangle = new Rectangle(5, 7);
           System.out.println("Area: " + rectangle.area());
           System.out.println("Perimeter: " + rectangle.perimeter());
       }
   }
   ```
   **Output:**
   ```
   Area: 35
   Perimeter: 24
   ```

### 2. **Puzzle: Book and Review Composition**
   - Design a `Book` class with a list of `Review` objects. Each review should have a reviewer name and text. Demonstrate adding reviews and displaying book details with reviews.
   ```java
   import java.util.ArrayList;

   class Review {
       private String reviewer;
       private String text;

       public Review(String reviewer, String text) {
           this.reviewer = reviewer;
           this.text = text;
       }

       public String toString() {
           return reviewer + ": " + text;
       }
   }

   class Book {
       private String title;
       private ArrayList<Review> reviews;

       public Book(String title) {
           this.title = title;
           this.reviews = new ArrayList<>();
       }

       public void addReview(String reviewer, String text) {
           reviews.add(new Review(reviewer, text));
       }

       public void showBook() {
           System.out.println("Title: " + title);
           for (Review review : reviews) {
               System.out.println(review);
           }
       }
   }

   public class Main {
       public static void main(String[] args) {
           Book book = new Book("Java Programming");
           book.addReview("Alice", "Great book for beginners!");
           book.addReview("Bob", "Comprehensive and well-written.");
           book.showBook();
       }
   }
   ```
   **Output:**
   ```
   Title: Java Programming
   Alice: Great book for beginners!
   Bob: Comprehensive and well-written.
   ```

### **New Quiz Questions:**

1. **What is object composition in OOP?**
   - A) Inheriting properties from another class
   - B) Using other objects as fields within a class **(Answer: B)**
   - C) Overriding methods in a class

2. **What is the purpose of the `ArrayList` in the Book and Review example?**
   - A) To store a dynamic list of reviews for a book **(Answer: A)**
   - B) To provide faster access to reviews
   - C) To create a fixed list of reviews

### **Fun Fact:**
- **Fun Fact:** Object composition is sometimes preferred over inheritance in OOP because it allows for more flexible relationships between objects.

---

### **Group 3: Steps 07, 08, and 09 – Understanding Inheritance**

- **Step 07 - Understanding Inheritance - Why do we need it?**
- **Step 08 - Object is at the Top of the Inheritance Hierarchy**
- **Step 09 - Inheritance and Overriding - with toString() method**

**Why grouped**: These steps explore the concept of inheritance, including why it is useful, the role of the Object superclass, and how to override methods. Together, they establish the fundamentals of inheritance and demonstrate how subclasses inherit and customize behavior from their superclass.

### 1. **Puzzle: Override `toString` Method**
   - Create a `Person` superclass with attributes `name` and `age`, and a `toString()` method. Subclass it with `Student` and override `toString` to include the grade level.
   ```java
   class Person {
       protected String name;
       protected int age;

       public Person(String name, int age) {
           this.name = name;
           this.age = age;
       }

       public String toString() {
           return "Person[name=" + name + ", age=" + age + "]";
       }
   }

   class Student extends Person {
       private String grade;

       public Student(String name, int age, String grade) {
           super(name, age);
           this.grade = grade;
       }

       public String toString() {
           return "Student[name=" + name + ", age=" + age + ", grade=" + grade + "]";
       }
   }

   public class Main {
       public static void main(String[] args) {
           Student student = new Student("Alice", 20, "Sophomore");
           System.out.println(student);
       }
   }
   ```
   **Output:**
   ```
   Student[name=Alice, age=20, grade=Sophomore]
   ```

### **Existing Quiz Questions:**

1.	What is Inheritance in Object Oriented Programming?

    - A) A mechanism of code reuse (Answer: A)
    - B) A mechanism to create new objects
    - C) A mechanism to modify existing objects

2.	What is the Object class in Java?

    - A) A user-defined class.
    - B) A package in Java system.
    - C) A built-in Java library class. (Answer: C)

3.	Which methods of the Object class are available to objects of other Java classes?

    - A) toString(), hashCodel(), and notify() (Answer: A)
    - B) setString(), and setint()
    - C) getName(), and setEmail()

4.	What happens when the statement System.out.println(person) is executed with an object person?

    - A) The 'toString() method of the Person class is called. (Answer: A)
    - B) The 'hashCode()' method of the Person class is called.
    - C) The 'notify() ' method of the Person class is called.

5.	Can a Java class directly inherit from two or more classes?

    - A) Yes
    - B) No (Answer: B)

6. What is the purpose of the toString() method in a class?

    - A) To define behavior.
    - B) To create objects.
    - C) To provide a String representation of an object. (Answer: C)

### **New Quiz Questions:**

1. **What is the purpose of overriding a method?**
   - A) To replace a superclass method with a subclass-specific implementation **(Answer: A)**
   - B) To call a superclass method
   - C) To rename a superclass method

2. **What is the top class in Java’s inheritance hierarchy?**
   - A) `Object` **(Answer: A)**
   - B) `Class`
   - C) `Hierarchy`

### **Fun Fact:**
- **Fun Fact:** Every Java class is a descendant of `Object`, making `Object` the ancestor of all Java classes.

---

### **Group 4: Steps 10, 11, and 12 – Advanced Inheritance Concepts**

- **Step 10 - Java Inheritance - Exercise - Student and Employee Classes**
- **Step 11 - Java Inheritance - Default Constructors and super() method call**
- **Step 12 - Java Inheritance - Puzzles - Multiple Inheritance, Reference Variables**

**Why grouped**: This group focuses on practical applications of inheritance through exercises on constructing subclasses (`Student` and `Employee`) and understanding constructors, super calls, and reference variables. The puzzles add depth by tackling complex scenarios like multiple inheritance and referencing.

### 1. **Puzzle: Implementing Inheritance with Constructors**
   - Create a `Person` superclass with `name` and `age` attributes, and use a constructor to initialize them. Extend it with an `Employee` class that includes an `employeeId` attribute and demonstrates the use of `super()` to call the superclass constructor.
   ```java
   class Person {
       protected String name;
       protected int age;

       public Person(String name, int age) {
           this.name = name;
           this.age = age;
       }
   }

   class Employee extends Person {
       private int employeeId;

       public Employee(String name, int age, int employeeId) {
           super(name, age); // Calling the superclass constructor
           this.employeeId = employeeId;
       }

       public void display() {
           System.out.println("Name: " + name + ", Age: " + age + ", Employee ID: " + employeeId);
       }
   }

   public class Main {
       public static void main(String[] args) {
           Employee employee = new Employee("John Doe", 30, 1023);
           employee.display();
       }
   }
   ```
   **Output:**
   ```
   Name: John Doe, Age: 30, Employee ID: 1023
   ```

### 2. **Puzzle: Understanding Reference Variables and Inheritance**
   - Given a superclass reference variable pointing to a subclass object, demonstrate how methods are called based on the object’s actual type.
   ```java
   class Animal {
       public void makeSound() {
           System.out.println("Animal sound");
       }
   }

   class Dog extends Animal {
       @Override
       public void makeSound() {
           System.out.println("Bark");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Animal myDog = new Dog();
           myDog.makeSound(); // Expected to print "Bark"
       }
   }
   ```
   **Output:**
   ```
   Bark
   ```

### **New Quiz Questions:**

1. **What does the `super` keyword do in a subclass?**
   - A) Calls a method in the subclass
   - B) Calls a constructor or method in the superclass **(Answer: B)**
   - C) Creates a new instance of the superclass

2. **When using a superclass reference to hold a subclass object, which methods are called?**
   - A) Superclass methods only
   - B) Subclass methods if overridden **(Answer: B)**
   - C) Only default methods

### **Fun Fact:**
- **Fun Fact:** Java does not support multiple inheritance to avoid the “diamond problem,” where a class could inherit conflicting methods from two parent classes.

---

### **Group 5: Steps 13, 14, and 15 – Abstract Classes and Methods**

- **Step 13 - Java Abstract Class - Introduction**
- **Step 14 - Java Abstract Class - First Example - Creating Recipes with Template Method**
- **Step 15 - Java Abstract Class - Puzzles**

**Why grouped**: This group introduces abstract classes and their use cases, emphasizing the flexibility they offer in class hierarchies. These steps cover the basics of defining abstract methods, their role in subclasses, and related puzzles to reinforce the concept.

### 1. **Puzzle: Create an Abstract `Appliance` Class with a `turnOn` Method**
   - Define an abstract `Appliance` class with an abstract method `turnOn()` and a concrete `plugIn()` method. Create a `WashingMachine` subclass that implements `turnOn`.
   ```java
   abstract class Appliance {
       public void plugIn() {
           System.out.println("Appliance plugged in.");
       }

       public abstract void turnOn();
   }

   class WashingMachine extends Appliance {
       @Override
       public void turnOn() {
           System.out.println("Washing machine is now running.");
       }
   }

   public class Main {
       public static void main(String[] args) {
           WashingMachine washer = new WashingMachine();
           washer.plugIn();
           washer.turnOn();
       }
   }
   ```
   **Output:**
   ```
   Appliance plugged in.
   Washing machine is now running.
   ```

### 2. **Puzzle: Implementing a Recipe Template with an Abstract Class**
   - Design an abstract `Recipe` class with a `prepare` method. Create a `PastaRecipe` class that provides details for making pasta.
   ```java
   abstract class Recipe {
       public void prepareRecipe() {
           boilWater();
           addIngredients();
           serve();
       }

       private void boilWater() {
           System.out.println("Boiling water...");
       }

       public abstract void addIngredients();

       private void serve() {
           System.out.println("Serving the dish.");
       }
   }

   class PastaRecipe extends Recipe {
       @Override
       public void addIngredients() {
           System.out.println("Adding pasta and sauce.");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Recipe pasta = new PastaRecipe();
           pasta.prepareRecipe();
       }
   }
   ```
   **Output:**
   ```
   Boiling water...
   Adding pasta and sauce.
   Serving the dish.
   ```

### **Existing Quiz Questions:**

1.	What is an abstract method?

    - A) A method without any parameters
    - B) A method with a method definition
    - C) A method without a method definition (Answer: C)

2.	Can an abstract class be instantiated?

    - A) Yes
    - B) No (Answer: B)

3.	What are the advantages of using an abstract class to create a recipe hierarchy?

    - A) Allows for the flexibility and customization of recipes.
    - B) Allows for the common structure of recipes to be maintained.
    - C) Allows for the creation of multiple recipe types easily.
    - D) All of the above (Answer: D)

4.	Which design pattern is used in the recipe hierarchy example?

    - A) Observer pattern
    - B) Decorator pattern
    - C) Template method pattern (Answer: C)

5.	Can an abstract class have member variables?

    - A) Yes (Answer: A)
    - B) No

6.	Can an abstract class have non-abstract methods?

    - A) Yes (Answer: A)
    - B) No

### **New Quiz Questions:**

1. **What is the purpose of an abstract class?**
   - A) To provide partial implementation for subclasses **(Answer: A)**
   - B) To define a full implementation for all subclasses
   - C) To be instantiated directly

2. **Which of the following statements about abstract methods is true?**
   - A) Abstract methods must have a body
   - B) Abstract methods do not have a body and must be implemented by subclasses **(Answer: B)**
   - C) Abstract methods can be overridden by any class

### **Fun Fact:**
- **Fun Fact:** The Template Method design pattern, often implemented with abstract classes, helps create a predefined sequence of steps for subclasses to follow with custom implementations.

---

### **Group 6: Steps 16, 17, 18, 19, 20, and 21 – Interfaces and Polymorphism**

- **Step 16 - Java Interface - Example 1 - Gaming Console - How to think about Interfaces**
- **Step 17 - Java Interface - Example 2 - Complex Algorithm - API defined by externals**
- **Step 18 - Java Interface - Puzzles - Unimplemented methods, Abstract Classes, Variability**
- **Step 19 - Java Interface vs Abstract Class - A Comparison**
- **Step 20 - Java Interface Flyable and Abstract Class Animal - An Exercise**
- **Step 21 - Polymorphism - An introduction**

**Why grouped**: This final group dives into interfaces, exploring their usage, differences from abstract classes, and application in polymorphism. By comparing interfaces with abstract classes, it builds a comprehensive understanding of interface-based design and the flexibility of polymorphic behaviors in OOP.

### 1. **Puzzle: Define a Gaming Console Interface**
   - Create an interface `GamingConsole` with methods `start()`, `stop()`, and `reset()`. Implement it in a `PlayStation` class.
   ```java
   interface GamingConsole {
       void start();
       void stop();
       void reset();
   }

   class PlayStation implements GamingConsole {
       public void start() {
           System.out.println("PlayStation starting...");
       }

       public void stop() {
           System.out.println("PlayStation stopping...");
       }

       public void reset() {
           System.out.println("PlayStation resetting...");
       }
   }

   public class Main {
       public static void main(String[] args) {
           GamingConsole ps = new PlayStation();
           ps.start();
           ps.reset();
           ps.stop();
       }
   }
   ```
   **Output:**
   ```
   PlayStation starting...
   PlayStation resetting...
   PlayStation stopping...
   ```

### 2. **Puzzle: Implementing a Flyable Interface with Polymorphism**
   - Create an interface `Flyable` with a `fly()` method. Implement `Flyable` in `Bird` and `Airplane` classes and demonstrate polymorphism by using a `Flyable` reference.
   ```java
   interface Flyable {
       void fly();
   }

   class Bird implements Flyable {
       public void fly() {
           System.out.println("Bird is flying.");
       }
   }

   class Airplane implements Flyable {
       public void fly() {
           System.out.println("Airplane is flying.");
       }
   }

   public class Main {
       public static void main(String[] args) {
           Flyable bird = new Bird();
           Flyable airplane = new Airplane();

           bird.fly();
           airplane.fly();
       }
   }
   ```
   **Output:**
   ```
   Bird is flying.
   Airplane is flying.
   ```

---

### **Existing Quiz Questions:**

1.	Who provides the implementation of methods declared in an interface?

    - A) The implementing classes (Answer: A)
    - B) The super class of the interface

### **New Quiz Questions:**

1. **Which keyword is used to implement an interface?**
   - A) `extends`
   - B) `implements` **(Answer: B)**
   - C) `inherit`

2. **What is polymorphism in Java?**
   - A) The ability for a method to take many forms **(Answer: A)**
   - B) Using multiple classes in a project
   - C) A process of encapsulation

### **Fun Fact:**
- **Fun Fact:** Java allows multiple inheritance of interfaces, making it easier to compose behaviors without the complications of multiple inheritance from classes.

---

### Additional Coding Exercises

### Exercise 1: “Library Management System” – Class and Object Composition
**Description**: Develop a simple library system to manage books, authors, and reviews. This exercise will reinforce object composition, constructors, and `toString()` method usage.

**Requirements**:
- Create a `Book` class with `title`, `author`, and a list of `Review` objects.
- Implement methods to add reviews and display book details.
- Include an `Author` class that’s part of the `Book` class composition.

**Code**:
```java
import java.util.ArrayList;
import java.util.List;

class Author {
    private String name;
    private String nationality;

    public Author(String name, String nationality) {
        this.name = name;
        this.nationality = nationality;
    }

    public String getName() {
        return name;
    }

    public String getNationality() {
        return nationality;
    }

    @Override
    public String toString() {
        return "Author: " + name + ", Nationality: " + nationality;
    }
}

class Review {
    private int rating;
    private String comment;

    public Review(int rating, String comment) {
        this.rating = rating;
        this.comment = comment;
    }

    @Override
    public String toString() {
        return "Rating: " + rating + "/5, Comment: " + comment;
    }
}

class Book {
    private String title;
    private Author author;
    private List<Review> reviews;

    public Book(String title, Author author) {
        this.title = title;
        this.author = author;
        this.reviews = new ArrayList<>();
    }

    public void addReview(Review review) {
        reviews.add(review);
    }

    public void displayBookInfo() {
        System.out.println("Title: " + title);
        System.out.println(author);
        System.out.println("Reviews:");
        for (Review review : reviews) {
            System.out.println("- " + review);
        }
    }
}

public class LibraryManager {
    public static void main(String[] args) {
        Author author = new Author("George Orwell", "British");
        Book book = new Book("1984", author);

        book.addReview(new Review(5, "A timeless classic."));
        book.addReview(new Review(4, "Thought-provoking and profound."));

        book.displayBookInfo();
    }
}
```

**Output**:
```
Title: 1984
Author: George Orwell, Nationality: British
Reviews:
- Rating: 5/5, Comment: A timeless classic.
- Rating: 4/5, Comment: Thought-provoking and profound.
```

---

### Exercise 2: “Zoo Animals” – Using Inheritance and Polymorphism
**Description**: Create a `Zoo` class with different types of animals, demonstrating polymorphism and method overriding.

**Requirements**:
- Create an abstract `Animal` class with a `sound()` method.
- Develop subclasses `Lion`, `Elephant`, and `Monkey` that override `sound()`.
- Use polymorphism to store animals in a list and call their `sound()` methods.

**Code**:
```java
import java.util.ArrayList;
import java.util.List;

abstract class Animal {
    abstract void sound();
}

class Lion extends Animal {
    @Override
    void sound() {
        System.out.println("Lion: Roar!");
    }
}

class Elephant extends Animal {
    @Override
    void sound() {
        System.out.println("Elephant: Trumpet!");
    }
}

class Monkey extends Animal {
    @Override
    void sound() {
        System.out.println("Monkey: Ooh-ooh!");
    }
}

public class Zoo {
    public static void main(String[] args) {
        List<Animal> animals = new ArrayList<>();
        animals.add(new Lion());
        animals.add(new Elephant());
        animals.add(new Monkey());

        System.out.println("Zoo Animals Sound:");
        for (Animal animal : animals) {
            animal.sound();
        }
    }
}
```

**Output**:
```
Zoo Animals Sound:
Lion: Roar!
Elephant: Trumpet!
Monkey: Ooh-ooh!
```

---

### Exercise 3: “Recipe Book” – Abstract Class Template
**Description**: Implement a recipe management system with an abstract class to define different recipes, showcasing abstract methods.

**Requirements**:
- Define an abstract class `Recipe` with methods `prepareIngredients()`, `cook()`, and `serve()`.
- Create `PastaRecipe` and `SaladRecipe` classes that extend `Recipe` and implement these methods.

**Code**:
```java
abstract class Recipe {
    abstract void prepareIngredients();
    abstract void cook();
    abstract void serve();

    public final void makeRecipe() {
        prepareIngredients();
        cook();
        serve();
    }
}

class PastaRecipe extends Recipe {
    @Override
    void prepareIngredients() {
        System.out.println("Preparing pasta, tomatoes, and cheese.");
    }

    @Override
    void cook() {
        System.out.println("Boiling pasta and cooking sauce.");
    }

    @Override
    void serve() {
        System.out.println("Serving pasta on a plate.");
    }
}

class SaladRecipe extends Recipe {
    @Override
    void prepareIngredients() {
        System.out.println("Chopping lettuce, tomatoes, and cucumbers.");
    }

    @Override
    void cook() {
        System.out.println("Mixing all ingredients.");
    }

    @Override
    void serve() {
        System.out.println("Serving salad in a bowl.");
    }
}

public class RecipeBook {
    public static void main(String[] args) {
        Recipe pasta = new PastaRecipe();
        Recipe salad = new SaladRecipe();

        System.out.println("Making Pasta:");
        pasta.makeRecipe();
        System.out.println("\nMaking Salad:");
        salad.makeRecipe();
    }
}
```

**Output**:
```
Making Pasta:
Preparing pasta, tomatoes, and cheese.
Boiling pasta and cooking sauce.
Serving pasta on a plate.

Making Salad:
Chopping lettuce, tomatoes, and cucumbers.
Mixing all ingredients.
Serving salad in a bowl.
```

---

### Exercise 4: “Guess the Animal” Game – Using Interface and Polymorphism
**Description**: Build a guessing game where the user is given hints to guess the animal. This will utilize interfaces and reinforce object-oriented design.

**Requirements**:
- Create an interface `AnimalHint` with a method `hint()`.
- Implement classes for different animals (`LionHint`, `ElephantHint`, etc.), each providing unique hints.
- Allow the user to guess based on the hints provided.

**Code**:
```java
import java.util.Scanner;

interface AnimalHint {
    void hint();
    String getAnswer();
}

class LionHint implements AnimalHint {
    public void hint() {
        System.out.println("I am the king of the jungle. Who am I?");
    }

    public String getAnswer() {
        return "Lion";
    }
}

class ElephantHint implements AnimalHint {
    public void hint() {
        System.out.println("I have a long trunk. Who am I?");
    }

    public String getAnswer() {
        return "Elephant";
    }
}

public class GuessTheAnimalGame {
    public static void main(String[] args) {
        AnimalHint[] animals = { new LionHint(), new ElephantHint() };
        Scanner scanner = new Scanner(System.in);

        for (AnimalHint animal : animals) {
            animal.hint();
            System.out.print("Your Guess: ");
            String guess = scanner.nextLine();

            if (guess.equalsIgnoreCase(animal.getAnswer())) {
                System.out.println("Correct!");
            } else {
                System.out.println("Wrong! The answer was " + animal.getAnswer());
            }
        }

        scanner.close();
    }
}
```

**Output**:
```
I am the king of the jungle. Who am I?
Your Guess: Tiger
Wrong! The answer was Lion
I have a long trunk. Who am I?
Your Guess: Elephant
Correct!
```

---

### **Exercise 5: “Battle Game” – Using Polymorphism and Inheritance**
**Description**: Create a battle game where players have different characters, each with unique abilities. This exercise reinforces polymorphism, method overriding, and class inheritance.

**Requirements**:
- Create a superclass `Character` with `name` and `attack()` method.
- Define subclasses `Warrior`, `Mage`, and `Archer`, each overriding the `attack()` method with unique behaviors.
- Simulate a battle by allowing characters to attack each other.

**Code**:
```java
abstract class Character {
    protected String name;

    public Character(String name) {
        this.name = name;
    }

    public abstract void attack();
}

class Warrior extends Character {
    public Warrior(String name) {
        super(name);
    }

    @Override
    public void attack() {
        System.out.println(name + " attacks with a sword!");
    }
}

class Mage extends Character {
    public Mage(String name) {
        super(name);
    }

    @Override
    public void attack() {
        System.out.println(name + " casts a fireball!");
    }
}

class Archer extends Character {
    public Archer(String name) {
        super(name);
    }

    @Override
    public void attack() {
        System.out.println(name + " shoots an arrow!");
    }
}

public class BattleGame {
    public static void main(String[] args) {
        Character warrior = new Warrior("Thor");
        Character mage = new Mage("Merlin");
        Character archer = new Archer("Robin");

        System.out.println("Battle Begins!");
        warrior.attack();
        mage.attack();
        archer.attack();
    }
}
```

**Output**:
```
Battle Begins!
Thor attacks with a sword!
Merlin casts a fireball!
Robin shoots an arrow!
```

---

### **Exercise 6: “Quiz Master” Game – Interface with Question Types**
**Description**: Create a quiz game where each question has a different type, like multiple choice and true/false. This exercise reinforces interface design and polymorphism.

**Requirements**:
- Create an interface `Question` with a `displayQuestion()` and `checkAnswer()` methods.
- Implement `MultipleChoiceQuestion` and `TrueFalseQuestion` classes.
- Test the quiz by presenting questions and validating answers.

**Code**:
```java
import java.util.Scanner;

interface Question {
    void displayQuestion();
    boolean checkAnswer(String answer);
}

class MultipleChoiceQuestion implements Question {
    private String question;
    private String[] options;
    private String correctAnswer;

    public MultipleChoiceQuestion(String question, String[] options, String correctAnswer) {
        this.question = question;
        this.options = options;
        this.correctAnswer = correctAnswer;
    }

    @Override
    public void displayQuestion() {
        System.out.println(question);
        for (int i = 0; i < options.length; i++) {
            System.out.println((i + 1) + ": " + options[i]);
        }
    }

    @Override
    public boolean checkAnswer(String answer) {
        return options[Integer.parseInt(answer) - 1].equals(correctAnswer);
    }
}

class TrueFalseQuestion implements Question {
    private String question;
    private boolean correctAnswer;

    public TrueFalseQuestion(String question, boolean correctAnswer) {
        this.question = question;
        this.correctAnswer = correctAnswer;
    }

    @Override
    public void displayQuestion() {
        System.out.println(question + " (true/false)");
    }

    @Override
    public boolean checkAnswer(String answer) {
        return Boolean.parseBoolean(answer) == correctAnswer;
    }
}

public class QuizMasterGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Question[] quiz = {
            new MultipleChoiceQuestion("What is the capital of France?", new String[]{"Berlin", "Paris", "Rome", "Madrid"}, "Paris"),
            new TrueFalseQuestion("The earth is flat.", false)
        };

        for (Question question : quiz) {
            question.displayQuestion();
            System.out.print("Your Answer: ");
            String answer = scanner.nextLine();
            if (question.checkAnswer(answer)) {
                System.out.println("Correct!");
            } else {
                System.out.println("Incorrect.");
            }
            System.out.println();
        }

        scanner.close();
    }
}
```

**Output**:
```
What is the capital of France?
1: Berlin
2: Paris
3: Rome
4: Madrid
Your Answer: 2
Correct!

The earth is flat. (true/false)
Your Answer: false
Correct!
```

---

### **Exercise 7: “Racing Game” – Abstract Class with Interfaces**
**Description**: Create a racing game where players can choose vehicles with different speeds and fuel capacities. This exercise uses an abstract class and interfaces to demonstrate polymorphism and encapsulation.

**Requirements**:
- Create an abstract class `Vehicle` with a `drive()` method and attributes like `speed` and `fuel`.
- Implement an interface `Refuelable` to add fuel to vehicles.
- Define `Car` and `Bike` classes extending `Vehicle` and implementing `Refuelable`.

**Code**:
```java
interface Refuelable {
    void refuel(int fuelAmount);
}

abstract class Vehicle implements Refuelable {
    protected String name;
    protected int speed;
    protected int fuel;

    public Vehicle(String name, int speed, int fuel) {
        this.name = name;
        this.speed = speed;
        this.fuel = fuel;
    }

    public void drive() {
        if (fuel > 0) {
            fuel--;
            System.out.println(name + " is driving at " + speed + " km/h. Fuel left: " + fuel);
        } else {
            System.out.println(name + " is out of fuel!");
        }
    }

    @Override
    public abstract void refuel(int fuelAmount);
}

class Car extends Vehicle {
    public Car(String name, int speed, int fuel) {
        super(name, speed, fuel);
    }

    @Override
    public void refuel(int fuelAmount) {
        fuel += fuelAmount;
        System.out.println(name + " refueled with " + fuelAmount + " liters. Total fuel: " + fuel);
    }
}

class Bike extends Vehicle {
    public Bike(String name, int speed, int fuel) {
        super(name, speed, fuel);
    }

    @Override
    public void refuel(int fuelAmount) {
        fuel += fuelAmount;
        System.out.println(name + " refueled with " + fuelAmount + " liters. Total fuel: " + fuel);
    }
}

public class RacingGame {
    public static void main(String[] args) {
        Vehicle car = new Car("Ferrari", 150, 5);
        Vehicle bike = new Bike("Ducati", 100, 3);

        System.out.println("Race Start!");
        car.drive();
        car.drive();
        car.refuel(2);
        car.drive();

        bike.drive();
        bike.refuel(1);
        bike.drive();
    }
}
```

**Output**:
```
Race Start!
Ferrari is driving at 150 km/h. Fuel left: 4
Ferrari is driving at 150 km/h. Fuel left: 3
Ferrari refueled with 2 liters. Total fuel: 5
Ferrari is driving at 150 km/h. Fuel left: 4

Ducati is driving at 100 km/h. Fuel left: 2
Ducati refueled with 1 liters. Total fuel: 3
Ducati is driving at 100 km/h. Fuel left: 2
```

---

## Section 22: Collections in Java Programming

#### **Group 1: Steps 1–6 – Basics of Collections and List Interface**

- **Step 01**: Java Collections - Section Overview with Need for Collections
- **Step 02**: List Interface - Introduction - Position is King
- **Step 03**: List Interface - Immutability and Introduction of Implementations - ArrayList
- **Step 04**: List Interface Implementations - ArrayList vs LinkedList
- **Step 05**: List Interface Implementations - ArrayList vs Vector
- **Step 06**: List Interface - Methods to add, remove, and change elements and lists

**Why Grouped:** This group covers the basics of the Collections framework, introduces the `List` interface, and explores its different implementations, such as `ArrayList`, `LinkedList`, and `Vector`. Basic operations on lists like adding, removing, and modifying elements are also discussed.

#### **Puzzles**

1. **Puzzle: Working with ArrayList Basics**  
   - **Problem**: Create an ArrayList of integers, add integers from 1 to 10, replace the element at index 5 with 50, and remove the element at index 3.
   ```java
   import java.util.ArrayList;

   public class ArrayListPuzzle {
       public static void main(String[] args) {
           ArrayList<Integer> numbers = new ArrayList<>();
           for (int i = 1; i <= 10; i++) {
               numbers.add(i);
           }
           numbers.set(5, 50); // Replaces element at index 5
           numbers.remove(3);  // Removes element at index 3
           System.out.println(numbers);
       }
   }
   ```
   **Output**: `[1, 2, 3, 5, 50, 7, 8, 9, 10]`

2. **Puzzle: Using LinkedList**  
   - **Problem**: Create a LinkedList of strings representing tasks for a day. Add "Breakfast" and "Exercise" at the beginning, "Work" and "Lunch" in the middle, and remove "Exercise."
   ```java
   import java.util.LinkedList;

   public class LinkedListPuzzle {
       public static void main(String[] args) {
           LinkedList<String> tasks = new LinkedList<>();
           tasks.add("Breakfast");
           tasks.add("Exercise");
           tasks.add("Work");
           tasks.add(2, "Lunch"); // Insert in the middle
           tasks.remove("Exercise");
           System.out.println(tasks);
       }
   }
   ```
   **Output**: `[Breakfast, Lunch, Work]`

### **Existing Quiz Questions**

1.	What is List Interface used for?

   - A) To implement an ordered collection in Java programs. (Answer: A)
   - B) o implement an unordered collection in Java programs.
   - C) To implement a stack data structure in Java programs.

### **New Quiz Questions**

1. **Which of the following interfaces allows duplicate elements in Java?**
   - A) `Set`
   - B) `Map`
   - C) `List` **(Answer: C)**

2. **Which class in Java is synchronized by default?**
   - A) `ArrayList`
   - B) `LinkedList`
   - C) `Vector` **(Answer: C)**

3. **What is the primary difference between `ArrayList` and `LinkedList`?**
   - A) `ArrayList` is slower for insertions at the beginning **(Answer: A)**
   - B) `LinkedList` does not allow null elements
   - C) `ArrayList` does not allow duplicate elements

### **Fun Fact**
- **Did you know?** The Collections Framework was first introduced in Java 1.2, standardizing data structures like `List`, `Set`, and `Map`.

---

#### **Group 2: Steps 7–12 – List Operations and Iteration Techniques**

- **Step 07**: List and ArrayList - Iterating around elements
- **Step 08**: List and ArrayList - Choosing iteration approach for printing and deleting
- **Step 09**: List and ArrayList - Puzzles - Type Safety and Removing Integers
- **Step 10**: List and ArrayList - Sorting - Introduction to Collections sort static
- **Step 11**: List and ArrayList - Sorting - Implementing Comparable Interface in Students
- **Step 12**: List and ArrayList - Sorting - Providing Flexibility by implementing Comparator

**Why Grouped:** This group delves into various list operations, including iteration techniques, removing elements, sorting, and understanding type safety. It includes both `Comparable` and `Comparator` interfaces for customized sorting.

---

#### **Puzzles**

1. **Puzzle: Removing Even Numbers**  
   - **Problem**: Create an ArrayList of numbers from 1 to 20 and remove all even numbers using an iterator.
   ```java
   import java.util.ArrayList;
   import java.util.Iterator;

   public class RemoveEvenNumbers {
       public static void main(String[] args) {
           ArrayList<Integer> numbers = new ArrayList<>();
           for (int i = 1; i <= 20; i++) {
               numbers.add(i);
           }
           Iterator<Integer> iterator = numbers.iterator();
           while (iterator.hasNext()) {
               if (iterator.next() % 2 == 0) {
                   iterator.remove();
               }
           }
           System.out.println(numbers);
       }
   }
   ```
   **Output**: `[1, 3, 5, 7, 9, 11, 13, 15, 17, 19]`


### **New Quiz Questions**

1. **Which method removes elements safely while iterating in Java?**
   - A) `ArrayList.remove()`
   - B) `Iterator.remove()` **(Answer: B)**
   - C) `List.removeAll()`

2. **What’s the primary use of the `Comparable` interface?**
   - A) To allow custom comparison in sorting **(Answer: A)**
   - B) To provide default comparison
   - C) To iterate over elements in reverse

### **Fun Fact**
- **Fun Fact:** Java allows both `Comparable` and `Comparator` for sorting. `Comparable` is for natural ordering, while `Comparator` enables custom sorting!

---

#### **Group 3: Steps 13–17 – Sets and Uniqueness**

- **Step 13**: List and ArrayList - A Summary
- **Step 14**: Set Interface - Introduction - No Duplication
- **Step 15**: Understanding Data Structures - Array, LinkedList and Hashing
- **Step 16**: Understanding Data Structures - Tree - Sorted Order
- **Step 17**: Set Interface - Hands on - HashSet, LinkedHashSet, and TreeSet

**Why Grouped:** This group introduces `Set` interfaces and implementations like `HashSet`, `LinkedHashSet`, and `TreeSet`, emphasizing the uniqueness constraint and different types of ordering.

#### **Puzzles**

1. **Puzzle: Unique Student IDs**  
   - **Problem**: Create a `HashSet` of integers representing student IDs. Add duplicates and see if they’re automatically removed.
   ```java
   import java.util.HashSet;

   public class StudentIDs {
       public static void main(String[] args) {
           HashSet<Integer> ids = new HashSet<>();
           ids.add(101);
           ids.add(102);
           ids.add(103);
           ids.add(101); // Duplicate
           System.out.println(ids);
       }
   }
   ```
   **Output**: `[101, 102, 103]`

---

### **Existing Quiz Questions**

1.	How does Java Set handle duplicate elements?

    - A) Stores all duplicate elements.
    - B) Stores the first occurrence of an element. (Answer: B)
    - C) Throws an exception when duplicates are added.

2.	What does the ‘equals’ method need to return for two objects to be considered equal and treated as duplicates?

    - A) true (Answer: A)
    - B) false

### **New Quiz Questions**

1. **Which implementation of `Set` maintains insertion order?**
   - A) `HashSet`
   - B) `LinkedHashSet` **(Answer: B)**
   - C) `TreeSet`

2. **What property does `HashSet` ensure?**
   - A) Elements are sorted
   - B) Elements are unique **(Answer: B)**
   - C) Elements are duplicated

### **Fun Fact**
- **Fun Fact:** Hashing is a unique process used in `HashSet` to organize data for efficient retrieval, even with large sets!

---

#### **Group 4: Steps 18–22 – Advanced Set Operations and Introduction to Queues**

- **Step 18**: Set Interface - Exercise - Find Unique Characters in a List
- **Step 19**: TreeSet - Methods from NavigableSet - floor, lower, upper, subSet, headSet
- **Step 20**: Queue Interface - Process Elements in Order
- **Step 21**: Introduction to PriorityQueue - Basic Methods and Customized Priority
- **Step 22**: Map Interface - An Introduction - Key and Value

**Why Grouped:** This group extends the `Set` operations and dives into `Queue` concepts, including priority and order in processing. It introduces `PriorityQueue` and basic `Map` functionalities.

#### **Puzzles**

1. **Puzzle: Task Prioritization with PriorityQueue**  
   - **Problem**: Create a `PriorityQueue` for tasks with different priorities and display them in order of priority.
   ```java
   import java.util.PriorityQueue;

   public class TaskPriority {
       public static void main(String[] args) {
           PriorityQueue<String> tasks = new PriorityQueue<>();
           tasks.add("Complete project");
           tasks.add("Buy groceries");
           tasks.add("Go for a run");
           tasks.add("Read a book");
           while (!tasks.isEmpty()) {
               System.out.println(tasks.poll());
           }
       }
   }
   ```
   **Output**:
   ```
   Buy groceries
   Complete project
   Go for a run
   Read a book
   ```

### **New Quiz Questions**

1. **What is the primary benefit of a PriorityQueue?**
   - A) It maintains insertion order
   - B) It processes elements by priority **(Answer: B)**
   - C) It duplicates elements

2. **Which method retrieves the first element in a PriorityQueue without removing it?**
   - A) `poll()`
   - B) `peek()` **(Answer: B)**
   - C) `pop()`

---

### **Fun Fact**
- **Fun Fact:** Java’s `PriorityQueue` is used in scheduling systems to manage tasks in order of importance or urgency!

---

#### **Group 5: Steps 23–27 – Map Implementations and Advanced Operations**

- **Step 23**: Map Interface - Implementations - `HashMap`, `HashTable`, `LinkedHashMap`, and `TreeMap`
- **Step 24**: Map Interface - Basic Operations
- **Step 25**: Map Interface - Comparison - `HashMap` vs `LinkedHashMap` vs `TreeMap`
- **Step 26**: Map Interface - Exercise - Count occurrences of characters and words
- **Step 27**: `TreeMap` - Methods from `NavigableMap` - `floorKey`, `higherKey`, `firstEntry`, `lastEntry`

**Why Grouped:** This group dives into different implementations of the `Map` interface (`HashMap`, `LinkedHashMap`, `TreeMap`, `Hashtable`) and their basic operations, as well as specific methods from `NavigableMap` to access elements by key. Exercises explore counting occurrences and performing advanced operations with `TreeMap`.

#### **Puzzles**

1. **Puzzle: Count Character Frequency in a String**  
   - **Problem**: Use a `HashMap` to count the occurrences of each character in the string "Programming".
   ```java
   import java.util.HashMap;

   public class CharFrequency {
       public static void main(String[] args) {
           String text = "Programming";
           HashMap<Character, Integer> frequencyMap = new HashMap<>();

           for (char c : text.toCharArray()) {
               frequencyMap.put(c, frequencyMap.getOrDefault(c, 0) + 1);
           }
           System.out.println(frequencyMap);
       }
   }
   ```
   **Output**: `{P=1, r=2, o=1, g=2, a=1, m=2, i=1, n=1}`

2. **Puzzle: Find Word Frequency in a Sentence**  
   - **Problem**: Using a `HashMap`, count the number of occurrences of each word in the sentence "Java is great and Java is versatile".
   ```java
   import java.util.HashMap;

   public class WordFrequency {
       public static void main(String[] args) {
           String text = "Java is great and Java is versatile";
           String[] words = text.split(" ");
           HashMap<String, Integer> wordMap = new HashMap<>();

           for (String word : words) {
               wordMap.put(word, wordMap.getOrDefault(word, 0) + 1);
           }
           System.out.println(wordMap);
       }
   }
   ```
   **Output**: `{Java=2, is=2, great=1, and=1, versatile=1}`

3. **Puzzle: Working with TreeMap - NavigableMap Methods**  
   - **Problem**: Using a `TreeMap`, add a few country-population pairs and use `floorKey`, `higherKey`, `firstEntry`, and `lastEntry` methods to query the data.
   ```java
   import java.util.TreeMap;

   public class CountryPopulation {
       public static void main(String[] args) {
           TreeMap<String, Integer> countries = new TreeMap<>();
           countries.put("USA", 331000000);
           countries.put("India", 1380000000);
           countries.put("China", 1440000000);
           countries.put("Brazil", 213000000);

           System.out.println("Countries in TreeMap: " + countries);
           System.out.println("Country with population <= India: " + countries.floorKey("India"));
           System.out.println("Country with population > India: " + countries.higherKey("India"));
           System.out.println("First entry: " + countries.firstEntry());
           System.out.println("Last entry: " + countries.lastEntry());
       }
   }
   ```
   **Output**:
   ```
   Countries in TreeMap: {Brazil=213000000, China=1440000000, India=1380000000, USA=331000000}
   Country with population <= India: India
   Country with population > India: USA
   First entry: Brazil=213000000
   Last entry: USA=331000000
   ```

### **Existing Quiz Questions**

1.	What is the size of this ‘map’?

```java
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
```

- A) 3 (Answer: A)
- B) 4
- C) 6

2. What is the value associated with the key “Z” in ‘map’?

```java
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
```

- A) 3
- B) null
- C) 10 (Answer: C)

3. What is the output of ‘map.containsValue(4)’?

```java
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
```

- A) true
- B) false (Answer: B)

4.	Which of the following map implementations maintains natural sorted order of the keys?

- A) HashMap
- B) LinkedHashMap
- C) TreeMap (Answer: C)

5.	Which of the following map implementations does not guarantee the order of stored elements?

- A) HashMap (Answer: A)
- B) LinkedHashMap

6.	Which of the following map implementations maintains insertion order of elements?

- A) HashMap
- B) LinkedHashMap (Answer: B)
- C) TreeMap

7.	What is the output of the following code?

```java
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
map.put("D", 4);
System.out.println(map.size());
```

- A) 3
- B) 4
- C) Compilation error (Answer: C)

8.	What is the output of the following code?

```java
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
System.out.println(map.keySet());
```

- A) ["A", "B", "C"] (Answer: A)
- B) [1, 2, 3]
- C) ["A"], ['"B"], ["C"]

9.	Which interface provides a contract to implement collections of elements in the form of (key, value) pairs?

- A) List
- B) Set
- C) Map (Answer: C)

10.	What is the main difference between a HashMap and a TreeMap?

- A) HashMap stores elements in natural sorted order while TreeMap is unordered.
- B) HashMap maintains insertion order while TreeMap is unsorted.
- C) HashMap and TreeMap are both unordered and unsorted.
- D) HashMap is based on a hash table while TreeMap is stored in a tree data structure and maintains natural sorted order. (Answer: D)

### **New Quiz Questions**

1. **What is a primary difference between `HashMap` and `TreeMap`?**
   - A) `TreeMap` allows duplicate keys
   - B) `HashMap` is sorted by keys
   - C) `TreeMap` is sorted by keys **(Answer: C)**

2. **Which of the following guarantees insertion order?**
   - A) `HashMap`
   - B) `LinkedHashMap` **(Answer: B)**
   - C) `TreeMap`

3. **What does the `getOrDefault` method do in a `Map`?**
   - A) Inserts a default value in the map
   - B) Returns the value for a key or a default value if key isn’t present **(Answer: B)**
   - C) Returns the key’s default hash code

4. **What does the `floorKey` method in `TreeMap` do?**
   - A) Finds the largest key less than or equal to the given key **(Answer: A)**
   - B) Finds the smallest key greater than or equal to the given key
   - C) Finds the first key in the map

### **Fun Fact**
- **Fun Fact:** `TreeMap` is implemented as a Red-Black Tree, which is a balanced binary tree structure, allowing efficient data retrieval and ordering by key.

---

#### **Group 6: Step 28 – Java Collections Conclusion and Tips**

- **Step 28**: Java Collections - Conclusion with Three Tips

**Why Grouped:** This step wraps up the Java Collections section, summarizing key takeaways and offering tips for effective usage of collections in Java.

### **New Quiz Questions**

1. **Which collection type would you choose for fast retrieval by key?**
   - A) `Set`
   - B) `Map` **(Answer: B)**
   - C) `List`

2. **What should you consider when choosing between `ArrayList` and `LinkedList`?**
   - A) Sorting requirements
   - B) Frequency of additions and deletions **(Answer: B)**
   - C) Duplicate handling

3. **Which data structure is typically used for implementing priority queues?**
   - A) Linked List
   - B) Array
   - C) Heap **(Answer: C)**

### **Fun Fact**
- **Fun Fact:** Java Collections Framework has been optimized over many versions of Java, with each collection having a unique purpose based on efficiency, order, and flexibility.

---

### Additional Coding Exercises

### Exercise 1: Word Frequency Counter
**Description:** Count the frequency of each word in a given paragraph.
  
```java
import java.util.HashMap;
import java.util.Map;

public class WordFrequencyCounter {
    public static void main(String[] args) {
        String paragraph = "Java is fun. Java is powerful. Java is also popular!";
        String[] words = paragraph.toLowerCase().replaceAll("[^a-z ]", "").split(" ");
        
        Map<String, Integer> wordCount = new HashMap<>();

        for (String word : words) {
            if (word.length() >= 3) {
                wordCount.put(word, wordCount.getOrDefault(word, 0) + 1);
            }
        }
        
        System.out.println("Word Frequencies: " + wordCount);
    }
}
```

**Output:**
```
Word Frequencies: {java=3, fun=1, powerful=1, also=1, popular=1}
```

---

### Exercise 2: Grade Book with LinkedList
**Description:** Implement a simple grade book using a `LinkedList`.

```java
import java.util.LinkedList;

public class GradeBook {
    public static void main(String[] args) {
        LinkedList<Integer> grades = new LinkedList<>();
        
        grades.add(85);
        grades.add(92);
        grades.add(76);
        grades.add(88);
        
        System.out.println("Grades: " + grades);
        
        grades.removeFirstOccurrence(76);
        System.out.println("Grades after removal: " + grades);
        
        System.out.println("Contains 92? " + grades.contains(92));
    }
}
```

**Output:**
```
Grades: [85, 92, 76, 88]
Grades after removal: [85, 92, 88]
Contains 92? true
```

---

### Exercise 3: High Scores Tracker with TreeMap
**Description:** Use a `TreeMap` to maintain high scores sorted by score in descending order.

```java
import java.util.TreeMap;

public class HighScoresTracker {
    public static void main(String[] args) {
        TreeMap<Integer, String> highScores = new TreeMap<>((a, b) -> b - a); 
        
        highScores.put(95, "Alice");
        highScores.put(85, "Bob");
        highScores.put(100, "Cindy");
        
        System.out.println("High Scores: " + highScores);
        
        System.out.println("Top Score: " + highScores.firstEntry());
    }
}
```

**Output:**
```
High Scores: {100=Cindy, 95=Alice, 85=Bob}
Top Score: 100=Cindy
```

---

### Exercise 4: Fruit Market Inventory Game (ArrayList & Set)
**Description:** Simulate a market inventory system, showing unique fruit items.

```java
import java.util.ArrayList;
import java.util.HashSet;

public class FruitMarketInventory {
    public static void main(String[] args) {
        ArrayList<String> fruits = new ArrayList<>();
        
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Apple");
        fruits.add("Orange");
        System.out.println("Fruit Inventory: " + fruits);

        HashSet<String> uniqueFruits = new HashSet<>(fruits);
        System.out.println("Unique Fruits: " + uniqueFruits);
    }
}
```

**Output:**
```
Fruit Inventory: [Apple, Banana, Apple, Orange]
Unique Fruits: [Apple, Banana, Orange]
```

---

### **Exercise 5: “Student Attendance Tracker”**
**Description:** Create a program that tracks student attendance using a `HashMap`. Each student has a name and a count of attended classes.

**Requirements:**
- The program should allow adding students and incrementing their attendance.
- The attendance should be displayed at the end in descending order of attendance.

**Code:**
```java
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;
import java.util.TreeMap;
import java.util.Comparator;

public class AttendanceTracker {
    public static void main(String[] args) {
        Map<String, Integer> attendanceMap = new HashMap<>();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Student Attendance Tracker:");
        System.out.println("Commands: add [name], present [name], display, exit");

        while (true) {
            System.out.print("Enter command: ");
            String input = scanner.nextLine();
            String[] command = input.split(" ");

            if (command[0].equalsIgnoreCase("add")) {
                String name = command[1];
                attendanceMap.put(name, 0);
                System.out.println("Added student: " + name);

            } else if (command[0].equalsIgnoreCase("present")) {
                String name = command[1];
                attendanceMap.put(name, attendanceMap.getOrDefault(name, 0) + 1);
                System.out.println("Marked present: " + name);

            } else if (command[0].equalsIgnoreCase("display")) {
                System.out.println("Attendance Summary:");
                attendanceMap.entrySet()
                        .stream()
                        .sorted(Map.Entry.comparingByValue(Comparator.reverseOrder()))
                        .forEach(entry -> System.out.println(entry.getKey() + ": " + entry.getValue()));
            } else if (command[0].equalsIgnoreCase("exit")) {
                break;
            }
        }
        scanner.close();
    }
}
```

**Output:**
```
Commands: add [name], present [name], display, exit
Enter command: add Alice
Added student: Alice
Enter command: present Alice
Marked present: Alice
Enter command: display
Attendance Summary:
Alice: 1
```

---

### **Exercise 6: “Classroom Game - Guess the Word”**
**Description:** Create a game where students guess words. Each word guessed correctly is removed from a list, and the player’s score is tracked.

**Requirements:**
- A predefined list of words.
- A score counter for correct guesses.
- The game ends when all words are guessed or a user types “exit.”

**Code:**
```java
import java.util.ArrayList;
import java.util.Scanner;

public class GuessTheWordGame {
    public static void main(String[] args) {
        ArrayList<String> words = new ArrayList<>();
        words.add("Java");
        words.add("Collections");
        words.add("HashMap");
        words.add("ArrayList");

        int score = 0;
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to Guess the Word Game!");
        System.out.println("Type 'exit' to quit.");

        while (!words.isEmpty()) {
            System.out.print("Guess a word: ");
            String guess = scanner.nextLine();

            if (guess.equalsIgnoreCase("exit")) break;

            if (words.contains(guess)) {
                words.remove(guess);
                score++;
                System.out.println("Correct! Your score: " + score);
            } else {
                System.out.println("Incorrect! Try again.");
            }
        }

        System.out.println("Game Over! Final Score: " + score);
        scanner.close();
    }
}
```

**Output:**
```
Welcome to Guess the Word Game!
Guess a word: Java
Correct! Your score: 1
Guess a word: HashMap
Correct! Your score: 2
Game Over! Final Score: 2
```

---

### **Exercise 7: “Zoo Animal Counter” - Using Sets and Maps**
**Description:** Simulate a zoo animal tracker. This program will keep track of unique animals and their counts as they enter or leave the zoo.

**Requirements:**
- Use a `HashSet` to track unique animal species.
- Use a `HashMap` to count the number of animals of each species.
- Display all animals in the zoo with their counts.

**Code:**
```java
import java.util.HashMap;
import java.util.HashSet;
import java.util.Map;
import java.util.Scanner;

public class ZooAnimalTracker {
    public static void main(String[] args) {
        HashSet<String> animalSpecies = new HashSet<>();
        Map<String, Integer> animalCount = new HashMap<>();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Zoo Animal Tracker:");
        System.out.println("Commands: add [species], remove [species], display, exit");

        while (true) {
            System.out.print("Enter command: ");
            String[] command = scanner.nextLine().split(" ");

            if (command[0].equalsIgnoreCase("add")) {
                String species = command[1];
                animalSpecies.add(species);
                animalCount.put(species, animalCount.getOrDefault(species, 0) + 1);
                System.out.println("Added " + species);

            } else if (command[0].equalsIgnoreCase("remove")) {
                String species = command[1];
                if (animalCount.getOrDefault(species, 0) > 0) {
                    animalCount.put(species, animalCount.get(species) - 1);
                    if (animalCount.get(species) == 0) {
                        animalSpecies.remove(species);
                    }
                    System.out.println("Removed one " + species);
                } else {
                    System.out.println("No such species in the zoo.");
                }

            } else if (command[0].equalsIgnoreCase("display")) {
                System.out.println("Animals in the zoo:");
                animalCount.forEach((species, count) -> System.out.println(species + ": " + count));
            } else if (command[0].equalsIgnoreCase("exit")) {
                break;
            }
        }
        scanner.close();
    }
}
```

**Output:**
```
Commands: add [species], remove [species], display, exit
Enter command: add Lion
Added Lion
Enter command: add Elephant
Added Elephant
Enter command: display
Animals in the zoo:
Lion: 1
Elephant: 1
```

---

### **Exercise 8: “Library Book Borrowing System” - Using Map and Queue**
**Description:** Build a library system that allows users to borrow books. Each book is represented by a title and the borrower’s name.

**Requirements:**
- Use a `HashMap` to store book titles and borrowers.
- Allow checking out and returning books.
- Track a queue of borrowers for each book.

**Code:**
```java
import java.util.HashMap;
import java.util.LinkedList;
import java.util.Map;
import java.util.Queue;
import java.util.Scanner;

public class LibrarySystem {
    public static void main(String[] args) {
        Map<String, Queue<String>> bookBorrowers = new HashMap<>();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Library Book Borrowing System:");
        System.out.println("Commands: borrow [book] [name], return [book], queue [book], exit");

        while (true) {
            System.out.print("Enter command: ");
            String[] command = scanner.nextLine().split(" ");

            if (command[0].equalsIgnoreCase("borrow")) {
                String book = command[1];
                String name = command[2];
                bookBorrowers.putIfAbsent(book, new LinkedList<>());
                Queue<String> queue = bookBorrowers.get(book);

                if (queue.isEmpty()) {
                    System.out.println(name + " borrowed " + book);
                } else {
                    queue.offer(name);
                    System.out.println(name + " added to the waiting list for " + book);
                }
            } else if (command[0].equalsIgnoreCase("return")) {
                String book = command[1];
                Queue<String> queue = bookBorrowers.get(book);
                
                if (!queue.isEmpty()) {
                    String nextBorrower = queue.poll();
                    System.out.println(nextBorrower + " can now borrow " + book);
                } else {
                    System.out.println("No one is in line for " + book);
                }
            } else if (command[0].equalsIgnoreCase("queue")) {
                String book = command[1];
                System.out.println("Waiting list for " + book + ": " + bookBorrowers.getOrDefault(book, new

 LinkedList<>()));
            } else if (command[0].equalsIgnoreCase("exit")) {
                break;
            }
        }
        scanner.close();
    }
}
```

**Output:**
```
Commands: borrow [book] [name], return [book], queue [book], exit
Enter command: borrow Java101 Alice
Alice borrowed Java101
Enter command: borrow Java101 Bob
Bob added to the waiting list for Java101
Enter command: queue Java101
Waiting list for Java101: [Bob]
```

--- 

## Section 24: Generics in Java Programming

#### **Group 1: Steps 1–2 – Introduction and Implementing Generics**

- **Step 01**: Introduction to Generics - Why do we need Generics?
- **Step 02**: Implementing Generics for the Custom List

**Why Grouped:** These steps introduce the concept of generics and why they’re essential in Java. Step 2 transitions to practical implementation, applying generics to a custom list class, allowing it to work with any data type.

#### **Puzzles**

1. **Puzzle: Create a Custom List with Generics**
   - **Problem:** Modify a `MyCustomList` class to store elements of any type and add a `get(int index)` method to retrieve an element by its index.
   
   **Code:**
   ```java
   import java.util.ArrayList;

   class MyCustomList<T> {
       private ArrayList<T> list = new ArrayList<>();

       public void addElement(T element) {
           list.add(element);
       }

       public T getElement(int index) {
           return list.get(index);
       }

       @Override
       public String toString() {
           return list.toString();
       }
   }

   public class GenericsPuzzle {
       public static void main(String[] args) {
           MyCustomList<String> stringList = new MyCustomList<>();
           stringList.addElement("Hello");
           stringList.addElement("Generics");
           System.out.println("String List: " + stringList);

           MyCustomList<Integer> intList = new MyCustomList<>();
           intList.addElement(10);
           intList.addElement(20);
           System.out.println("Integer List: " + intList);
       }
   }
   ```
   **Output:**
   ```
   String List: [Hello, Generics]
   Integer List: [10, 20]
   ```

2. **Puzzle: Implement a Generic `addElement` and `removeElement` Method**
   - **Problem:** Extend `MyCustomList` with methods to add and remove elements dynamically.
   
   **Code:**
   ```java
   class MyCustomList<T> {
       private ArrayList<T> list = new ArrayList<>();

       public void addElement(T element) {
           list.add(element);
       }

       public void removeElement(T element) {
           list.remove(element);
       }

       @Override
       public String toString() {
           return list.toString();
       }
   }

   public class GenericsTest {
       public static void main(String[] args) {
           MyCustomList<Double> doubleList = new MyCustomList<>();
           doubleList.addElement(3.14);
           doubleList.addElement(2.71);
           System.out.println("Before removal: " + doubleList);
           
           doubleList.removeElement(2.71);
           System.out.println("After removal: " + doubleList);
       }
   }
   ```
   **Output:**
   ```
   Before removal: [3.14, 2.71]
   After removal: [3.14]
   ```

#### **New Quiz Questions**

1. **What is the purpose of generics in Java?**
   - A) To restrict classes to specific data types
   - B) To allow classes to work with different data types **(Answer: B)**
   - C) To enhance security

2. **What symbol is used to denote a generic type?**
   - A) `<T>` **(Answer: A)**
   - B) `[G]`
   - C) `{T}`

### **Fun Fact**
- **Fun Fact:** The concept of generics was introduced in Java 5 to add more type safety and reduce casting errors.

---

#### **Group 2: Step 3 – Extending Custom List with Generic Return Method**

- **Step 03**: Extending Custom List with a Generic Return Method

**Why Grouped:** This step builds on the previous custom list by adding a generic return method, showcasing the flexibility of generics in method return types.

#### **Puzzle**

1. **Puzzle: Adding a Generic `getElement` Method**
   - **Problem:** Create a generic `getElement(int index)` method to return the element at a specific index.
   
   **Code:**
   ```java
   class MyCustomList<T> {
       private ArrayList<T> list = new ArrayList<>();

       public void addElement(T element) {
           list.add(element);
       }

       public T getElement(int index) {
           return list.get(index);
       }

       @Override
       public String toString() {
           return list.toString();
       }
   }

   public class GenericsReturnPuzzle {
       public static void main(String[] args) {
           MyCustomList<String> words = new MyCustomList<>();
           words.addElement("Java");
           words.addElement("Programming");

           System.out.println("First word: " + words.getElement(0));
       }
   }
   ```
   **Output:**
   ```
   First word: Java
   ```

### **New Quiz Question**

1. **How can a generic return type be defined in a method?**
   - A) By adding `<T>` before the return type **(Answer: A)**
   - B) By using the `Object` class as the return type
   - C) By returning an `ArrayList`

### **Fun Fact**
- **Fun Fact:** Generics add type safety without impacting runtime performance, as they are implemented through "type erasure."

---

#### **Group 3: Step 4 – Restrictions with Extends and Generic Methods**

- **Step 04**: Generics Puzzles - Restrictions with extends and Generic Methods

**Why Grouped:** This step explores restrictions in generics using `extends`, limiting types to subclasses of a specific class, which helps enforce consistency and prevent runtime errors.

#### **Puzzle**

1. **Puzzle: Restricting Types in a Generic List**
   - **Problem:** Create a `NumericList` that accepts only numbers (Integer, Double, etc.) and can return the average of all numbers.
   
   **Code:**
   ```java
   import java.util.ArrayList;

   class NumericList<T extends Number> {
       private ArrayList<T> list = new ArrayList<>();

       public void addNumber(T number) {
           list.add(number);
       }

       public double getAverage() {
           double sum = 0.0;
           for (T number : list) {
               sum += number.doubleValue();
           }
           return sum / list.size();
       }
   }

   public class GenericsRestriction {
       public static void main(String[] args) {
           NumericList<Integer> numbers = new NumericList<>();
           numbers.addNumber(10);
           numbers.addNumber(20);
           numbers.addNumber(30);

           System.out.println("Average: " + numbers.getAverage());
       }
   }
   ```
   **Output:**
   ```
   Average: 20.0
   ```

### **New Quiz Question**

1. **Which of the following restricts a generic type to subtypes of `Number`?**
   - A) `<T super Number>`
   - B) `<T extends Number>` **(Answer: B)**
   - C) `<T implements Number>`

### **Fun Fact**
- **Fun Fact:** `extends` in generics can apply to both classes and interfaces, allowing flexible restrictions.

---

#### **Group 4: Step 5 – WildCards with Upper and Lower Bound**

- **Step 05**: Generics and WildCards - Upper Bound and Lower Bound

**Why Grouped:** This step introduces wildcards with `extends` (upper bound) and `super` (lower bound), showcasing flexible boundaries in method arguments.

---

#### **Puzzle**

1. **Puzzle: Summing Numbers with Upper Bounded Wildcard**
   - **Problem:** Create a method that sums any list of numbers using an upper bounded wildcard (`? extends Number`).
   
   **Code:**
   ```java
   import java.util.List;

   public class SumNumbers {
       public static double sumOfNumbers(List<? extends Number> numbers) {
           double sum = 0.0;
           for (Number number : numbers) {
               sum += number.doubleValue();
           }
           return sum;
       }

       public static void main(String[] args) {
           List<Integer> intList = List.of(1, 2, 3, 4);
           List<Double> doubleList = List.of(1.5, 2.5, 3.5);

           System.out.println("Sum of integers: " + sumOfNumbers(intList));
           System.out.println("Sum of doubles: " + sumOfNumbers(doubleList));
       }
   }
   ```
   **Output:**
   ```
   Sum of integers: 10.0
   Sum of doubles: 7.5
   ```

### **New Quiz Question**

1. **Which wildcard allows accepting a list of any subtype of `Number`?**
   - A) `<? super Number>`
   - B) `<? extends Number>` **(Answer: B)**
   - C) `<T>`

### **Fun Fact**
- **Fun Fact:** Wildcards make generics more flexible, allowing methods to work with various subclasses or superclasses without modifying the class itself.

---

### Additional Coidng Exercises

### **Exercise 1: Custom Stack with Generics**

**Description:** Create a custom `Stack` class using generics. This class should allow pushing elements to the top, popping elements from the top, and viewing the top element.

**Code:**
```java
import java.util.ArrayList;

class CustomStack<T> {
    private ArrayList<T> stack = new ArrayList<>();

    public void push(T element) {
        stack.add(element);
    }

    public T pop() {
        if (!stack.isEmpty()) {
            return stack.remove(stack.size() - 1);
        }
        return null; // Or throw an exception
    }

    public T peek() {
        if (!stack.isEmpty()) {
            return stack.get(stack.size() - 1);
        }
        return null;
    }

    @Override
    public String toString() {
        return stack.toString();
    }
}

public class StackGenericsTest {
    public static void main(String[] args) {
        CustomStack<String> stringStack = new CustomStack<>();
        stringStack.push("Java");
        stringStack.push("Generics");
        System.out.println("Stack after pushes: " + stringStack);

        System.out.println("Peek: " + stringStack.peek());
        System.out.println("Pop: " + stringStack.pop());
        System.out.println("Stack after pop: " + stringStack);
    }
}
```

**Output:**
```
Stack after pushes: [Java, Generics]
Peek: Generics
Pop: Generics
Stack after pop: [Java]
```

---

### **Exercise 2: Pair Finder with Upper Bounds**

**Description:** Create a generic method to find and display all pairs from a list of numbers (e.g., `Integer`, `Double`) that sum up to a given target value.

**Code:**
```java
import java.util.ArrayList;
import java.util.List;

public class PairFinder {
    public static <T extends Number> void findPairs(List<T> list, double targetSum) {
        for (int i = 0; i < list.size(); i++) {
            for (int j = i + 1; j < list.size(); j++) {
                if (list.get(i).doubleValue() + list.get(j).doubleValue() == targetSum) {
                    System.out.println("Pair found: " + list.get(i) + ", " + list.get(j));
                }
            }
        }
    }

    public static void main(String[] args) {
        List<Integer> intList = List.of(2, 4, 6, 8, 10);
        System.out.println("Finding pairs that sum to 10:");
        findPairs(intList, 10);

        List<Double> doubleList = List.of(1.5, 3.5, 5.0, 6.5);
        System.out.println("Finding pairs that sum to 7.0:");
        findPairs(doubleList, 7.0);
    }
}
```

**Output:**
```
Finding pairs that sum to 10:
Pair found: 2, 8
Pair found: 4, 6
Finding pairs that sum to 7.0:
Pair found: 1.5, 5.5
```

---

### **Exercise 3: “Flashcard Quiz” Game using Generics**

**Description:** Create a flashcard quiz game where each flashcard has a question (String) and an answer (generic). This will allow different types of answers, such as `Integer`, `Double`, or `String`.

**Code:**
```java
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

class Flashcard<T> {
    private String question;
    private T answer;

    public Flashcard(String question, T answer) {
        this.question = question;
        this.answer = answer;
    }

    public String getQuestion() {
        return question;
    }

    public T getAnswer() {
        return answer;
    }
}

public class FlashcardQuiz {
    public static void main(String[] args) {
        Map<Flashcard<?>, String> flashcards = new HashMap<>();
        flashcards.put(new Flashcard<>("What is 5 + 5?", 10), "Integer");
        flashcards.put(new Flashcard<>("Name of this programming language?", "Java"), "String");
        flashcards.put(new Flashcard<>("Square root of 49?", 7.0), "Double");

        Scanner scanner = new Scanner(System.in);
        int score = 0;

        for (Map.Entry<Flashcard<?>, String> entry : flashcards.entrySet()) {
            Flashcard<?> card = entry.getKey();
            System.out.println(card.getQuestion());
            System.out.print("Answer: ");
            String userAnswer = scanner.nextLine();

            if (String.valueOf(card.getAnswer()).equalsIgnoreCase(userAnswer)) {
                System.out.println("Correct!");
                score++;
            } else {
                System.out.println("Incorrect. Correct answer: " + card.getAnswer());
            }
        }

        System.out.println("Quiz over! Your score: " + score + "/" + flashcards.size());
    }
}
```

**Output:**
```
What is 5 + 5?
Answer: 10
Correct!
Name of this programming language?
Answer: Java
Correct!
Quiz over! Your score: 2/2
```

---

### **Exercise 4: Generic Max Finder Game with Bounds**

**Description:** Create a game that finds the maximum number from a list. The list should support `Integer`, `Double`, or `Float` types using upper bounds.

**Code:**
```java
import java.util.List;

public class MaxFinderGame {
    public static <T extends Number & Comparable<T>> T findMax(List<T> list) {
        if (list.isEmpty()) {
            return null;
        }

        T max = list.get(0);
        for (T element : list) {
            if (element.compareTo(max) > 0) {
                max = element;
            }
        }
        return max;
    }

    public static void main(String[] args) {
        List<Integer> intList = List.of(10, 30, 20, 50);
        System.out.println("Max in Integer list: " + findMax(intList));

        List<Double> doubleList = List.of(1.5, 3.5, 2.5, 6.5);
        System.out.println("Max in Double list: " + findMax(doubleList));
    }
}
```

**Output:**
```
Max in Integer list: 50
Max in Double list: 6.5
```

---

## Section 25: Introduction to Functional Programming in Java

#### **Group 1: Steps 1–3 - Introduction and Basic Functions as Parameters**

- **Step 01**: Introduction to Functional Programming - Functions are First-Class Citizens
- **Step 02**: Functional Programming - First Example with Function as Parameter
- **Step 03**: Functional Programming - Exercise - Loop a List of Numbers

**Why Grouped:** This group covers fundamental concepts, introducing functions as first-class citizens and demonstrating how functions can be passed as parameters in Java.

#### **Puzzles**

1. **Puzzle:** Create a function that accepts a list of integers and returns a list with each element incremented by 2.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.stream.Collectors;

     public class IncrementByTwo {
         public static List<Integer> increment(List<Integer> numbers) {
             return numbers.stream().map(n -> n + 2).collect(Collectors.toList());
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(1, 2, 3);
             System.out.println(increment(numbers)); // Output: [3, 4, 5]
         }
     }
     ```
   - **Output:** `[3, 4, 5]`

2. **Puzzle:** Create a function that takes a list and applies a lambda to double each number.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.stream.Collectors;

     public class DoubleNumbers {
         public static List<Integer> doubleElements(List<Integer> numbers) {
             return numbers.stream().map(n -> n * 2).collect(Collectors.toList());
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(4, 5, 6);
             System.out.println(doubleElements(numbers)); // Output: [8, 10, 12]
         }
     }
     ```
   - **Output:** `[8, 10, 12]`

### **Existing Quiz Questions**

1. What is a functional interface in Java?

    - A) An interface that contains only one abstract method.
    - B) An interface that can be implemented using a lambda expression.
    - C) An interface that can be used to represent a function.
    - D) All of the above. (Answer: D)

2. How is a lambda expression different from a regular method?

    - A) Lambda expressions are anonymous, while regular methods have names.
    - B) Lambda expressions are concise, while regular methods can be multiple lines of code.
    - C) Lambda expressions are type-inferred, while regular methods must explicitly specify their types.
    - D) All of the above. (Answer: D)

### **New Quiz Questions**

1. **What does it mean for functions to be "first-class citizens" in functional programming?**
   - A) Functions can be passed as arguments, returned as values, and assigned to variables **(Answer: A)**
   - B) Functions can only be called in classes
   - C) Functions cannot return values

2. **How would you loop through a list of numbers in functional programming?**
   - A) Using a traditional `for` loop
   - B) Using `forEach` with a lambda expression **(Answer: B)**
   - C) Using only recursive functions

### **Fun Fact**
Java introduced lambda expressions and functional programming concepts in Java 8 to make code more readable and concise.

---

#### **Group 2: Steps 4–6 - Filtering and Summing Lists**

- **Step 04**: Functional Programming - Filtering - Exercises to print odd and even numbers
- **Step 05**: Functional Programming - Collect - Sum of Numbers in a List
- **Step 06**: Functional Programming vs Structural Programming - A Quick Comparison

**Why Grouped:** These steps cover filtering operations, collecting data into lists, and comparing functional programming with traditional structural programming.

#### **Puzzles**

1. **Puzzle:** Write a function to filter out even numbers and return only odd numbers from a list.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.stream.Collectors;

     public class OddNumbersOnly {
         public static List<Integer> filterOdds(List<Integer> numbers) {
             return numbers.stream().filter(n -> n % 2 != 0).collect(Collectors.toList());
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(1, 2, 3, 4, 5);
             System.out.println(filterOdds(numbers)); // Output: [1, 3, 5]
         }
     }
     ```
   - **Output:** `[1, 3, 5]`

2. **Puzzle:** Implement a function that sums all the even numbers in a list.
   - **Solution Code:**
     ```java
     import java.util.List;

     public class SumEvenNumbers {
         public static int sumEven(List<Integer> numbers) {
             return numbers.stream().filter(n -> n % 2 == 0).mapToInt(Integer::intValue).sum();
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(1, 2, 3, 4, 5);
             System.out.println(sumEven(numbers)); // Output: 6
         }
     }
     ```
   - **Output:** `6`

### **Existing Quiz Questions**

1. What is the purpose of the filter method?

    - A) To filter the elements of a stream based on a predicate. (Answer: A)
    - B) To sort the elements of a stream.
    - C) To map the elements of a stream to a new type.
    - D) To reduce the elements of a stream to a single value.

2. How would you filter the list of numbers to contain only even numbers?

```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9);
```

- A) numbers.stream().filter(num -> num%2 == 0) (Answer: A)
- B) numbers.stream().filter(num -> num%2 ==1)
- C) numbers.stream().filter(num -> num%2 == 2)

### **New Quiz Questions**

1. **What is the purpose of the `filter` method in streams?**
   - A) To filter out elements based on a condition **(Answer: A)**
   - B) To loop through a list
   - C) To sort elements

2. **How would you sum elements in a list using streams?**
   - A) `list.stream().reduce(Integer::sum)`
   - B) `list.stream().mapToInt(Integer::intValue).sum()` **(Answer: B)**
   - C) `list.stream().average()`

### **Fun Fact**
Functional programming encourages immutability and avoids side effects, making programs easier to reason about and debug.

---

#### **Group 3: Steps 7–10 - Intermediate Stream Operations and Lambda Expressions**

- **Step 07**: Functional Programming Terminology - Lambda Expression, Stream and Operators
- **Step 08**: Stream Intermediate Operations - Sort, Distinct, Filter and Map
- **Step 09**: Stream Intermediate Operations - Exercises - Squares of First 10, Map
- **Step 10**: Stream Terminal Operations - `max` operation with Comparator

**Why Grouped:** These steps introduce various stream operations, including sorting, distinct elements, filtering, and working with lambda expressions for more complex stream manipulations.

#### **Puzzles**

1. **Puzzle:** Implement a function to return distinct squares of numbers from a list.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.stream.Collectors;

     public class DistinctSquares {
         public static List<Integer> squareDistinct(List<Integer> numbers) {
             return numbers.stream().map(n -> n * n).distinct().collect(Collectors.toList());
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(2, 3, 2, 4);
             System.out.println(squareDistinct(numbers)); // Output: [4, 9, 16]
         }
     }
     ```
   - **Output:** `[4, 9, 16]`

2. **Puzzle:** Write a function to find the maximum element in a list using streams.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.Comparator;

     public class MaxElement {
         public static int findMax(List<Integer> numbers) {
             return numbers.stream().max(Comparator.naturalOrder()).orElseThrow();
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(3, 7, 2, 9, 5);
             System.out.println(findMax(numbers)); // Output: 9
         }
     }
     ```
   - **Output:** `9`

### **Existing Quiz Questions**

1. What is the purpose of the distinct method in stream operations?

    - A) To remove duplicate elements from a stream. (Answer: A)
    - B) To sort the elements of a stream.
    - C) To map the elements of a stream to a new type.
    - D) To reduce the elements of a stream to a single value.

2. What is the purpose of the map() operation in stream operations?

    - A) To apply a function to each element in a stream and produce a new stream with the results. (Answer: A)
    - B) To filter the elements of a stream based on a predicate.
    - C) To sort the elements of a stream.
    - D) To reduce the elements of a stream to a single value.

3. What are intermediate operations and terminal operations in streams?

    - A) Intermediate operations return a new stream, while terminal operations produce a result or side-effect.
    - B) Intermediate operations can be chained together, while terminal operations cannot be chained together.
    - C) Both are true (Answer: C)

### **New Quiz Questions**

1. **What does the `map` method do in a stream?**
   - A) Loops over elements
   - B) Transforms each element **(Answer: B)**
   - C) Filters elements

2. **Which stream operation is terminal?**
   - A) map
   - B) filter
   - C) collect **(Answer: C)**

#### **Fun Fact**
Streams provide a high-level abstraction for processing collections, allowing developers to work with data in a more functional style.

---

#### **Group 4: Steps 11–18 - Optional Class, Functional Interfaces, and Method References**

- **Step 11**: Stream Terminal Operations - `min`, collect to List
- **Step 12**: Optional class in Java - An Introduction
- **Step 13**: Functional Interfaces - Implement Predicate Interface
- **Step 14**: Functional Interfaces - Implement Consumer Interface
- **Step 15**: Functional Interfaces - Implement Function Interface
- **Step 16**: Simplify Functional Programming with Method References
- **Step 17**: Functions are First-Class Citizens
- **Step 18**: Introduction to Functional Programming - Conclusion

**Why Grouped:** This group dives deeper into advanced functional programming concepts, such as functional interfaces, optional values, and method references, providing a well-rounded conclusion to the section.

#### **Puzzles**

1. **Puzzle:** Implement a function that returns the minimum of a list using streams.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.Comparator;

     public class MinElement {
         public static int findMin(List<Integer> numbers) {
             return numbers.stream().min(Comparator.naturalOrder()).orElseThrow();
         }

         public static void main(String[] args) {
             List<Integer> numbers = List.of(5, 3, 9, 2);
             System.out.println(findMin(numbers)); // Output: 2
         }
     }


     ```
   - **Output:** `2`

2. **Puzzle:** Create a function that uses the `Predicate` functional interface to filter words with length greater than 4.
   - **Solution Code:**
     ```java
     import java.util.List;
     import java.util.function.Predicate;
     import java.util.stream.Collectors;

     public class FilterWords {
         public static List<String> filterByLength(List<String> words, Predicate<String> condition) {
             return words.stream().filter(condition).collect(Collectors.toList());
         }

         public static void main(String[] args) {
             List<String> words = List.of("Java", "Stream", "API", "Functional", "Programming");
             System.out.println(filterByLength(words, word -> word.length() > 4)); // Output: [Stream, Functional, Programming]
         }
     }
     ```
   - **Output:** `[Stream, Functional, Programming]`

### **Existing Quiz Questions**

1. What does the Optional < T > class represent in stream operations?

- A) A container object that may or may not contain a value.
- B) A way to represent null values in stream operations.
- C) A way to avoid NullPointerExceptions in stream operations.
- D) All of the above. (Answer: D)

2. What is the purpose of the reduce method in functional programming?

- A) To filter the elements of a stream based on a predicate.
- B) To sort the elements of a stream.
- C) To map the elements of a stream to a new type.
- D) To reduce the elements of a stream to a single value. (Answer: D)

3. What is the output of the following code?

```java
List<Integer> list = List.of(1, 4, 7, 9);
list.stream().filter(num -> num%2 == 1).forEach(elem -> System.out.println(elem));
```

- A) 1, 7,9 (Annswer: A)
- B) 4
- C) 1, 4, 7, 9

4. What is the output of the following code?

```java
List<Integer> numbers = List.of(4, 6, 8, 13, 3, 15);
int sum = numbers.stream()
                 .reduce(0, (num1, num2) -> num1 + num2);
System.out.println(sum);
```

- A) 49 (Answer: A)
- B) 31
- C) 34

### **New Quiz Questions**

1. **What does `Optional` represent in Java?**
   - A) A mandatory value
   - B) A container for nullable values **(Answer: B)**
   - C) A required integer

2. **What does `Predicate` interface represent?**
   - A) A function that returns a boolean **(Answer: A)**
   - B) A void method
   - C) A mathematical formula

---

### Additional Coding Exercises

### Exercise 1: **Inventory Management System**

**Description**: In this exercise, you will create a small inventory management system that uses functional programming to manage a list of products. Implement filtering, mapping, and reducing operations to manage inventory and calculate the total value of in-stock items.

1. **Instructions**:
   - Define a `Product` class with properties `String name`, `double price`, and `boolean inStock`.
   - Create a list of `Product` instances, with varying prices and stock status.
   - Use functional programming to:
     - Filter products that are in stock.
     - Calculate and display the total value of the inventory for in-stock items.
     - Map and print product names in uppercase.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   class Product {
       String name;
       double price;
       boolean inStock;

       public Product(String name, double price, boolean inStock) {
           this.name = name;
           this.price = price;
           this.inStock = inStock;
       }

       public String getName() {
           return name;
       }

       public double getPrice() {
           return price;
       }

       public boolean isInStock() {
           return inStock;
       }
   }

   public class InventoryManager {
       public static void main(String[] args) {
           List<Product> products = List.of(
               new Product("Laptop", 1200.50, true),
               new Product("Mouse", 25.75, false),
               new Product("Keyboard", 75.25, true),
               new Product("Monitor", 300.00, true)
           );

           // Filter in-stock products and calculate total value
           double totalValue = products.stream()
               .filter(Product::isInStock)
               .mapToDouble(Product::getPrice)
               .sum();

           System.out.println("Total value of in-stock items: $" + totalValue);

           // Map product names to uppercase
           System.out.println("Product names in uppercase:");
           products.stream()
               .map(product -> product.getName().toUpperCase())
               .forEach(System.out::println);
       }
   }
   ```
3. **Output**:
   ```
   Total value of in-stock items: $1575.75
   Product names in uppercase:
   LAPTOP
   MOUSE
   KEYBOARD
   MONITOR
   ```

---

### Exercise 2: **Student Grades Analyzer**

**Description**: Create a program that analyzes a list of students’ grades. Using functional programming, find students with grades above a certain threshold, calculate the average grade, and display the highest grade in the class.

1. **Instructions**:
   - Define a `Student` class with properties `String name` and `double grade`.
   - Generate a list of students with random grades.
   - Use streams to:
     - Filter and print students with grades above 70.
     - Calculate the class average.
     - Find the student with the highest grade.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   class Student {
       String name;
       double grade;

       public Student(String name, double grade) {
           this.name = name;
           this.grade = grade;
       }

       public String getName() {
           return name;
       }

       public double getGrade() {
           return grade;
       }
   }

   public class StudentAnalyzer {
       public static void main(String[] args) {
           List<Student> students = List.of(
               new Student("Alice", 85.5),
               new Student("Bob", 62.0),
               new Student("Charlie", 91.5),
               new Student("Diana", 76.5)
           );

           System.out.println("Students with grades above 70:");
           students.stream()
               .filter(s -> s.getGrade() > 70)
               .forEach(s -> System.out.println(s.getName()));

           double averageGrade = students.stream()
               .mapToDouble(Student::getGrade)
               .average()
               .orElse(0.0);
           System.out.println("Class average: " + averageGrade);

           Student topStudent = students.stream()
               .max(Comparator.comparingDouble(Student::getGrade))
               .orElse(null);
           if (topStudent != null) {
               System.out.println("Top student: " + topStudent.getName() + " with grade " + topStudent.getGrade());
           }
       }
   }
   ```
3. **Output**:
   ```
   Students with grades above 70:
   Alice
   Charlie
   Diana
   Class average: 78.875
   Top student: Charlie with grade 91.5
   ```

---

### Exercise 3: **“Guess the Number” Game with Hints**

**Description**: Create a functional programming-based guessing game where the computer randomly picks a number between 1 and 100, and the player must guess it. The program should give hints like "too high" or "too low."

1. **Instructions**:
   - Generate a random number.
   - Allow the player to input guesses and provide hints until they guess correctly.
   - Count attempts and print the final score.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   public class GuessTheNumberGame {
       public static void main(String[] args) {
           int numberToGuess = new Random().nextInt(100) + 1;
           Scanner scanner = new Scanner(System.in);
           System.out.println("Welcome to the 'Guess the Number' Game!");
           System.out.println("I'm thinking of a number between 1 and 100. Try to guess it!");

           Stream.generate(() -> scanner.nextInt())
               .map(guess -> {
                   if (guess < numberToGuess) return "Too low!";
                   else if (guess > numberToGuess) return "Too high!";
                   else return "Correct!";
               })
               .peek(System.out::println)
               .anyMatch(response -> response.equals("Correct!"));

           System.out.println("You guessed the correct number! Congratulations!");
       }
   }
   ```
3. **Output**:
   ```
   Welcome to the 'Guess the Number' Game!
   I'm thinking of a number between 1 and 100. Try to guess it!
   (Player input: 50)
   Too low!
   (Player input: 75)
   Too high!
   ...
   Correct!
   ```

---

### Exercise 4: **Word Frequency Counter**

**Description**: Implement a program that calculates the frequency of each word in a given sentence. This exercise will use functional programming to process a sentence into words, map word counts, and print the results.

1. **Instructions**:
   - Take a sentence input from the user.
   - Split the sentence into words.
   - Count occurrences of each word using streams.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   public class WordFrequencyCounter {
       public static void main(String[] args) {
           Scanner scanner = new Scanner(System.in);
           System.out.println("Enter a sentence:");
           String sentence = scanner.nextLine().toLowerCase();

           Map<String, Long> wordFrequency = Arrays.stream(sentence.split(" "))
               .collect(Collectors.groupingBy(word -> word, Collectors.counting()));

           System.out.println("Word Frequency:");
           wordFrequency.forEach((word, count) -> System.out.println(word + ": " + count));
       }
   }
   ```
3. **Output**:
   ```
   Enter a sentence:
   (User input: "Java is fun and Java is powerful")
   Word Frequency:
   java: 2
   is: 2
   fun: 1
   and: 1
   powerful: 1
   ```

---

### **Exercise 5: Vocabulary Builder**

**Description**: Create a vocabulary builder program that takes a list of words and counts occurrences of each word length. This is useful for building vocabulary by focusing on different word lengths.

1. **Instructions**:
   - Accept a list of words.
   - Count and display the frequency of each word length (e.g., 3-letter words, 4-letter words, etc.).
   - Use streams to group by word length and count occurrences.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   public class VocabularyBuilder {
       public static void main(String[] args) {
           List<String> words = List.of("apple", "orange", "cat", "elephant", "dog", "pear", "zebra", "owl");

           Map<Integer, Long> lengthFrequency = words.stream()
               .collect(Collectors.groupingBy(String::length, Collectors.counting()));

           System.out.println("Word Length Frequency:");
           lengthFrequency.forEach((length, count) -> System.out.println(length + "-letter words: " + count));
       }
   }
   ```
3. **Output**:
   ```
   Word Length Frequency:
   5-letter words: 2
   6-letter words: 1
   3-letter words: 3
   7-letter words: 1
   8-letter words: 1
   ```

---

### **Exercise 6: Movie Rating Aggregator**

**Description**: Implement a movie rating aggregator that takes a list of movies with ratings and calculates the average rating for each genre. This will help reinforce the use of streams to group and aggregate data.

1. **Instructions**:
   - Define a `Movie` class with `String title`, `String genre`, and `double rating`.
   - Create a list of `Movie` instances.
   - Use functional programming to:
     - Group movies by genre.
     - Calculate and display the average rating for each genre.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   class Movie {
       String title;
       String genre;
       double rating;

       public Movie(String title, String genre, double rating) {
           this.title = title;
           this.genre = genre;
           this.rating = rating;
       }

       public String getGenre() {
           return genre;
       }

       public double getRating() {
           return rating;
       }
   }

   public class MovieRatingAggregator {
       public static void main(String[] args) {
           List<Movie> movies = List.of(
               new Movie("Inception", "Sci-Fi", 9.0),
               new Movie("Interstellar", "Sci-Fi", 8.5),
               new Movie("The Matrix", "Sci-Fi", 8.7),
               new Movie("The Godfather", "Crime", 9.2),
               new Movie("Goodfellas", "Crime", 8.7),
               new Movie("Pulp Fiction", "Drama", 8.9)
           );

           Map<String, Double> averageRatings = movies.stream()
               .collect(Collectors.groupingBy(Movie::getGenre, Collectors.averagingDouble(Movie::getRating)));

           System.out.println("Average Ratings by Genre:");
           averageRatings.forEach((genre, avgRating) -> System.out.println(genre + ": " + avgRating));
       }
   }
   ```
3. **Output**:
   ```
   Average Ratings by Genre:
   Sci-Fi: 8.733333333333333
   Crime: 8.95
   Drama: 8.9
   ```

---

### **Exercise 7: Language Translation Quiz Game**

**Description**: Create a language translation quiz game where users must translate words from English to another language. This exercise uses functional programming to shuffle words and verify answers.

1. **Instructions**:
   - Create a `Map` of English words and their corresponding translations.
   - Randomly select words for the quiz.
   - Check if the player’s translation matches the correct answer.

2. **Code**:
   ```java
   import java.util.*;
   import java.util.stream.*;

   public class LanguageTranslationQuiz {
       public static void main(String[] args) {
           Map<String, String> translations = Map.of(
               "hello", "hola",
               "world", "mundo",
               "apple", "manzana",
               "car", "coche",
               "book", "libro"
           );

           List<String> words = new ArrayList<>(translations.keySet());
           Collections.shuffle(words);
           Scanner scanner = new Scanner(System.in);
           int score = 0;

           System.out.println("Translate the following words into Spanish:");

           for (String word : words.stream().limit(3).collect(Collectors.toList())) {
               System.out.print("Translate '" + word + "': ");
               String answer = scanner.nextLine();
               if (translations.get(word).equalsIgnoreCase(answer)) {
                   System.out.println("Correct!");
                   score++;
               } else {
                   System.out.println("Incorrect! The correct answer is: " + translations.get(word));
               }
           }

           System.out.println("Your score: " + score + "/" + 3);
       }
   }
   ```
3. **Output**:
   ```
   Translate the following words into Spanish:
   Translate 'hello': hola
   Correct!
   Translate 'car': coche
   Correct!
   Translate 'apple': fruta
   Incorrect! The correct answer is: manzana
   Your score: 2/3
   ```

---

## Section 27: Introduction to Threads And Concurrency in Java

#### **Group 1: Steps 01-03 - Introduction and Basic Thread Creation**

   - **Why Grouped**: These steps introduce the need for threads, creating a thread by extending the `Thread` class, and implementing `Runnable`.

#### **Puzzles**

**Puzzle 1**: Create a `Task` class that extends `Thread` and prints numbers from 1 to 50.

   **Code**:
   ```java
   class Task extends Thread {
       @Override
       public void run() {
           for (int i = 1; i <= 50; i++) {
               System.out.println("Task printing: " + i);
           }
       }
   }

   public class TaskExample {
       public static void main(String[] args) {
           Task task = new Task();
           task.start();
       }
   }
   ```
   **Output**:
   ```
   Task printing: 1
   Task printing: 2
   ...
   Task printing: 50
   ```

**Puzzle 2**: Implement a `Runnable` that counts down from 100 to 1 with a delay.

   **Code**:
   ```java
   class Countdown implements Runnable {
       @Override
       public void run() {
           for (int i = 100; i >= 1; i--) {
               System.out.println("Countdown: " + i);
               try {
                   Thread.sleep(100); // Pauses for 0.1 seconds
               } catch (InterruptedException e) {
                   e.printStackTrace();
               }
           }
       }
   }

   public class CountdownExample {
       public static void main(String[] args) {
           Thread countdownThread = new Thread(new Countdown());
           countdownThread.start();
       }
   }
   ```
   **Output**:
   ```
   Countdown: 100
   Countdown: 99
   ...
   Countdown: 1
   ```

### **Existing Quiz Questions**

1. **What is the purpose of implementing the `Runnable` interface in Java?**

- A) To create a class that can be executed by a thread. (Answer: A)
- B) To create a class that can throw checked exceptions.
- C) To create a class that can be used in a try-catch block.

2. **What is a drawback of using the `Thread` class or `Runnable` interface for managing threads?**

- A) No fine-grained control over thread execution.
- B) Difficult to maintain when managing multiple threads.
- C) No way to get the result from a sub-task.
- D) All of the above. (Answer: D)

### **New Quiz Questions**

1. **What are the two main ways to create a thread in Java?**
   - A) Using `Thread` and `Runnable` **(Answer)**
   - B) Using `Callable` and `Runnable`
   - C) Using `Runnable` and `Executor`

2. **What is the purpose of the `start()` method in a thread?**
   - A) To begin executing the thread **(Answer)**
   - B) To initialize thread variables
   - C) To set thread priority

### **Fun Fact**

- **Did you know?** Threads allow Java applications to handle multiple tasks simultaneously, introduced as early as Java’s initial release in 1995.

---

#### **Group 2: Steps 04-06 - Thread States, Priorities, and Communication with join()**

   - **Why Grouped**: These steps discuss thread states, setting thread priorities, and using the `join()` method for communication.

#### **Puzzles**

**Puzzle 1**: Run two threads (`Task1` and `Task2`) in sequence using `join()`.

   **Code**:
   ```java
   class Task1 extends Thread {
       public void run() {
           System.out.println("Task1 started.");
           try { Thread.sleep(500); } catch (InterruptedException e) {}
           System.out.println("Task1 completed.");
       }
   }

   class Task2 extends Thread {
       public void run() {
           System.out.println("Task2 started.");
           try { Thread.sleep(500); } catch (InterruptedException e) {}
           System.out.println("Task2 completed.");
       }
   }

   public class SequentialThreads {
       public static void main(String[] args) throws InterruptedException {
           Task1 task1 = new Task1();
           Task2 task2 = new Task2();
           task1.start();
           task1.join(); // Ensure Task2 starts only after Task1 completes
           task2.start();
       }
   }
   ```
   **Output**:
   ```
   Task1 started.
   Task1 completed.
   Task2 started.
   Task2 completed.
   ```

**Puzzle 2**: Assign `MAX_PRIORITY` to `Task1` and `MIN_PRIORITY` to `Task2`.

   **Code**:
   ```java
   class TaskPriorityExample extends Thread {
       private String name;

       public TaskPriorityExample(String name) {
           this.name = name;
       }

       public void run() {
           System.out.println(name + " started with priority " + getPriority());
           try { Thread.sleep(100); } catch (InterruptedException e) {}
           System.out.println(name + " completed.");
       }
   }

   public class PriorityExample {
       public static void main(String[] args) {
           TaskPriorityExample task1 = new TaskPriorityExample("Task1");
           TaskPriorityExample task2 = new TaskPriorityExample("Task2");
           task1.setPriority(Thread.MAX_PRIORITY);
           task2.setPriority(Thread.MIN_PRIORITY);
           task1.start();
           task2.start();
       }
   }
   ```
   **Output**:
   ```
   Task1 started with priority 10
   Task1 completed.
   Task2 started with priority 1
   Task2 completed.
   ```

### **Existing Quiz Questions**

1. **Which of the following states is a thread in when it is ready to be executed but not currently running?**

- A) RUNNING
- B) RUNNABLE (Answer: B)
- C) BLOCKED/WAITING

2. **What is the range of thread priorities in Java?**

- A) 1 to 100
- B) 1 to 1000
- C) 1 to 10 (Answer: C)

3. **What is the default priority assigned to a thread in Java?**

- A) 1
- B) 5 (Answer: B)
- C) 10
- D) 0

4. **What is the purpose of the `join()` method in Java?**

- A) It pauses the execution of a thread until it is explicitly resumed.
- B) It sets the priority of a thread to the highest level.
- C) It allows one thread to wait for the completion of another thread. (Answer: C)
- D) It terminates a thread and frees up system resources.

### **New Quiz Questions**

1. **What does `join()` do in a thread?**
   - A) Pauses the thread until another completes **(Answer)**
   - B) Combines two threads into one
   - C) Duplicates the thread

2. **What are the five thread states in Java?**
   - A) New, Runnable, Running, Blocked, Terminated **(Answer)**
   - B) Waiting, Active, Suspended, Terminated, Runnable
   - C) Initialized, Running, Blocked, Suspended, Terminated

### **Fun Fact**

- **Did you know?** Thread priority is only a “hint” to the Java scheduler and doesn’t guarantee priority order.

---

#### **Group 3: Steps 07-08 - Thread Control with sleep, yield, and synchronized**

   - **Why Grouped**: These steps introduce methods like `sleep` and `yield`, as well as synchronization to control thread execution.

#### **Puzzles**

**Puzzle 1**: Create two threads that increment a shared counter variable. Use `synchronized` to avoid data inconsistencies.

   **Code**:
   ```java
   class Counter {
       private int count = 0;

       public synchronized void increment() {
           count++;
       }

       public int getCount() {
           return count;
       }
   }

   class IncrementTask extends Thread {
       private Counter counter;

       public IncrementTask(Counter counter) {
           this.counter = counter;
       }

       public void run() {
           for (int i = 0; i < 100; i++) {
               counter.increment();
           }
       }
   }

   public class SynchronizedCounterExample {
       public static void main(String[] args) throws InterruptedException {
           Counter counter = new Counter();
           IncrementTask task1 = new IncrementTask(counter);
           IncrementTask task2 = new IncrementTask(counter);
           task1.start();
           task2.start();
           task1.join();
           task2.join();
           System.out.println("Final counter value: " + counter.getCount());
       }
   }
   ```
   **Output**:
   ```
   Final counter value: 200
   ```

**Puzzle 2**: Use `Thread.sleep(500)` to add a delay.

   **Code**:
   ```java
   class SleepTask extends Thread {
       public void run() {
           System.out.println("Processing...");
           try {
               Thread.sleep(500);
           } catch (InterruptedException e) {
               e.printStackTrace();
           }
           System.out.println("Processing continued...");
       }
   }

   public class SleepExample {
       public static void main(String[] args) {
           SleepTask task = new SleepTask();
           task.start();
       }
   }
   ```
   **Output**:
   ```
   Processing...
   [Pauses for 0.5 seconds]
   Processing continued...
   ```

### **New Quiz Questions**

1. **What does the `synchronized` keyword do?**
   - A) Ensures only one thread accesses a block of code at a time **(Answer)**
   - B) Pauses the thread
   - C) Sets thread priority

2. **What is the purpose of `Thread.sleep()`?**
   - A) To permanently stop the thread
   - B) To pause the thread **(Answer)**
   - C) To synchronize the thread

### **Fun Fact**

- **Did you know?** The `synchronized` keyword prevents race conditions by allowing only one thread to execute a synchronized method at a time.

---

#### **Group 4: Steps 09-14 - Advanced Thread Control with ExecutorService**

   - **Why Grouped**: These steps cover the `ExecutorService`, including `invokeAll` and `invokeAny` methods.

#### **Puzzles**

**Puzzle 1**: Use `invokeAll` to execute multiple tasks and retrieve their results.

   **Code**:
   ```java
   import java.util.*;
   import java.util.concurrent.*;

   class SimpleTask implements Callable<String> {
       private String name;

       public SimpleTask(String name) {
           this.name = name;
       }

       public String call() {
           return name + " completed";
       }
   }

   public class InvokeAllExample {
       public static void main(String[] args) throws InterruptedException, ExecutionException {
           ExecutorService executor = Executors.newFixedThreadPool(3);
           List<Callable<String>> tasks = List.of(
               new

 SimpleTask("Task 1"),
               new SimpleTask("Task 2"),
               new SimpleTask("Task 3")
           );

           List<Future<String>> results = executor.invokeAll(tasks);
           for (Future<String> result : results) {
               System.out.println(result.get());
           }
           executor.shutdown();
       }
   }
   ```
   **Output**:
   ```
   Task 1 completed
   Task 2 completed
   Task 3 completed
   ```

**Puzzle 2**: Use `invokeAny` to execute multiple tasks and get the result of the fastest.

   **Code**:
   ```java
   import java.util.*;
   import java.util.concurrent.*;

   public class InvokeAnyExample {
       public static void main(String[] args) throws ExecutionException, InterruptedException {
           ExecutorService executor = Executors.newFixedThreadPool(3);
           List<Callable<String>> tasks = List.of(
               () -> { Thread.sleep(200); return "Task 1 completed"; },
               () -> { Thread.sleep(100); return "Task 2 completed"; },
               () -> { Thread.sleep(300); return "Task 3 completed"; }
           );

           String result = executor.invokeAny(tasks);
           System.out.println("Fastest task result: " + result);
           executor.shutdown();
       }
   }
   ```
   **Output**:
   ```
   Fastest task result: Task 2 completed
   ```

### **Existing Quiz Questions**

1. **Which method is used to create an `ExecutorService` with just one thread?**

- A) ExecutorService.newSingleThreadExecutor() (Answer: A)
- B) ExecutorService.newFixedThreadPool()
- C) ExecutorService.newCachedThreadPool()
- D) ExecutorService.newScheduledThreadPool()

2. **Which method is used to create a thread pool with a specified number of threads?**

- A) ExecutorService.newSingleThreadExecutor()
- B) ExecutorService.newFixedThreadPool() (Answer: B)
- C) ExecutorService.newCachedThreadPool()
- D) ExecutorService.newScheduledThreadPool()

3. **What happens if more tasks are submitted to an `ExecutorService` than the number of threads in the pool?**

- A) The additional tasks are queued and executed when a thread becomes available. (Answer: A)
- B) The additional tasks are discarded and not executed.
- C) The Executor Service automatically adds more threads to the thread pool to accommodate the tasks.

4. **Which interface is used to create sub-tasks that return a result?**

- A) Thread
- B) Runnable
- C) Callable < T > (Answer: C)
- D) ExecutorService

5. **What method of `ExecutorService` can be used to wait for the result of the fastest completed task from a group of tasks?**

- A) execute()
- B) submit()
- C) invokeAll()
- D) invokeAny() (Answer: D)

### **New Quiz Questions**

1. **What is the purpose of the `Future` object in `ExecutorService`?**
   - A) Holds a promise of a result for an asynchronous task **(Answer)**
   - B) Pauses a task
   - C) Sets task priority

2. **How does `invokeAny()` differ from `invokeAll()` in an `ExecutorService`?**
   - A) `invokeAny()` returns the first completed task result, `invokeAll()` waits for all tasks to complete **(Answer)**
   - B) Both wait for all tasks to complete
   - C) Both return a list of results

### **Fun Fact**

- **Did you know?** Java’s `Future` class allows you to cancel tasks and check their completion status, adding a layer of control to concurrency handling.

---

### Additional Coding Exercises

### **Exercise 1: Task Scheduler Game**
**Description**: Create a simple game using threads to schedule and execute tasks in sequence and parallel. In this game, each task simulates a game level, and players must complete each level (task) to progress to the next level.

**Code**:
```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

class GameLevel implements Runnable {
    private final String levelName;

    public GameLevel(String levelName) {
        this.levelName = levelName;
    }

    @Override
    public void run() {
        System.out.println(levelName + " has started.");
        try {
            Thread.sleep(1000); // Simulate level execution time
        } catch (InterruptedException e) {
            System.out.println("Interrupted: " + levelName);
        }
        System.out.println(levelName + " has finished.");
    }
}

public class TaskSchedulerGame {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(3);
        System.out.println("Game has started!");

        // Add levels
        executor.execute(new GameLevel("Level 1"));
        executor.execute(new GameLevel("Level 2"));
        executor.execute(new GameLevel("Level 3"));

        executor.shutdown();
    }
}
```

**Output**:
```
Game has started!
Level 1 has started.
Level 1 has finished.
Level 2 has started.
Level 2 has finished.
Level 3 has started.
Level 3 has finished.
```

---

### **Exercise 2: Multi-Task File Downloader**
**Description**: Simulate downloading files using multiple threads. Each thread represents a file download task, and `ExecutorService` manages simultaneous downloads.

**Code**:
```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
import java.util.concurrent.TimeUnit;

class FileDownload implements Runnable {
    private final String fileName;

    public FileDownload(String fileName) {
        this.fileName = fileName;
    }

    @Override
    public void run() {
        System.out.println("Starting download of " + fileName);
        try {
            Thread.sleep(2000); // Simulating download time
        } catch (InterruptedException e) {
            System.out.println("Download interrupted for: " + fileName);
        }
        System.out.println("Completed download of " + fileName);
    }
}

public class FileDownloader {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(3);

        executor.execute(new FileDownload("File1.zip"));
        executor.execute(new FileDownload("File2.zip"));
        executor.execute(new FileDownload("File3.zip"));
        executor.execute(new FileDownload("File4.zip"));
        executor.execute(new FileDownload("File5.zip"));

        executor.shutdown();
        try {
            executor.awaitTermination(10, TimeUnit.SECONDS);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```

**Output**:
```
Starting download of File1.zip
Starting download of File2.zip
Starting download of File3.zip
Completed download of File1.zip
Starting download of File4.zip
Completed download of File2.zip
Starting download of File5.zip
...
```

---

### **Exercise 3: Quiz Timer Challenge**
**Description**: Develop a timer-based quiz game where each question has a time limit. If the user doesn’t answer within the time, the thread will automatically terminate and move to the next question.

**Code**:
```java
import java.util.Scanner;
import java.util.concurrent.*;

class QuizQuestion implements Callable<String> {
    private final String question;

    public QuizQuestion(String question) {
        this.question = question;
    }

    @Override
    public String call() throws Exception {
        System.out.println(question);
        Scanner scanner = new Scanner(System.in);
        return scanner.nextLine();
    }
}

public class QuizTimerChallenge {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newSingleThreadExecutor();
        String[] questions = {"What is the capital of France?", "2 + 2?", "What is Java?"};
        int score = 0;

        for (String question : questions) {
            Future<String> future = executor.submit(new QuizQuestion(question));

            try {
                String answer = future.get(5, TimeUnit.SECONDS); // 5-second timer for each question
                System.out.println("Answer: " + answer);
                score++;
            } catch (TimeoutException e) {
                System.out.println("Time's up!");
            } catch (Exception e) {
                e.printStackTrace();
            }
        }

        executor.shutdown();
        System.out.println("Final score: " + score + "/" + questions.length);
    }
}
```

**Output**:
```
What is the capital of France?
[User input or "Time's up!" if exceeded]
2 + 2?
[User input or "Time's up!" if exceeded]
Final score: X/3
```

---

### **Exercise 4: “Fastest Response” Task Game**
**Description**: Using `invokeAny`, create a game where multiple threads perform a simulated task, and the first to complete is the “winner.” This demonstrates competitive parallel execution.

**Code**:
```java
import java.util.concurrent.*;

class TaskChallenge implements Callable<String> {
    private final String taskName;

    public TaskChallenge(String taskName) {
        this.taskName = taskName;
    }

    @Override
    public String call() throws InterruptedException {
        int time = (int) (Math.random() * 3000);
        Thread.sleep(time);
        return taskName + " finished in " + time + " ms";
    }
}

public class FastestTaskGame {
    public static void main(String[] args) throws InterruptedException, ExecutionException {
        ExecutorService executor = Executors.newFixedThreadPool(3);

        System.out.println("Starting the Fastest Task Game...");
        String result = executor.invokeAny(
            List.of(new TaskChallenge("Task A"), new TaskChallenge("Task B"), new TaskChallenge("Task C"))
        );

        System.out.println("Fastest task: " + result);
        executor.shutdown();
    }
}
```

**Output**:
```
Starting the Fastest Task Game...
Fastest task: Task B finished in 912 ms
```

---

### **Exercise 5: Multiplayer Chat Simulation**

**Description**: Create a multiplayer chat simulation where each player represents a `Runnable` task. Messages are sent at random intervals, and the program displays each message in real-time.

1. **Instructions**:
   - Define a `Player` class implementing `Runnable`, simulating random message sends.
   - Use `ExecutorService` to handle multiple players (threads).
   - Randomly delay messages to simulate real-time chat.

2. **Code**:
   ```java
   import java.util.Random;
   import java.util.concurrent.ExecutorService;
   import java.util.concurrent.Executors;
   import java.util.concurrent.TimeUnit;

   class Player implements Runnable {
       private final String name;

       public Player(String name) {
           this.name = name;
       }

       @Override
       public void run() {
           String[] messages = {
               "Hello!", "How’s it going?", "Anyone here?", 
               "I’m ready to play!", "Good game!", "Let’s win!"
           };
           Random random = new Random();

           for (int i = 0; i < 5; i++) {
               try {
                   Thread.sleep(random.nextInt(2000)); // Random delay for message
                   System.out.println(name + ": " + messages[random.nextInt(messages.length)]);
               } catch (InterruptedException e) {
                   System.out.println(name + " left the chat.");
               }
           }
       }
   }

   public class MultiplayerChatSimulation {
       public static void main(String[] args) {
           ExecutorService chatService = Executors.newFixedThreadPool(3);

           System.out.println("Chat simulation started...");

           chatService.execute(new Player("Player1"));
           chatService.execute(new Player("Player2"));
           chatService.execute(new Player("Player3"));

           chatService.shutdown();
           try {
               chatService.awaitTermination(10, TimeUnit.SECONDS);
           } catch (InterruptedException e) {
               e.printStackTrace();
           }

           System.out.println("Chat simulation ended.");
       }
   }
   ```

3. **Output**:
   ```
   Chat simulation started...
   Player1: Hello!
   Player2: I’m ready to play!
   Player3: How’s it going?
   Player1: Good game!
   ...
   Chat simulation ended.
   ```

---

### **Exercise 6: Airport Runway Simulation**

**Description**: Simulate an airport runway with multiple planes requesting permission to take off. Only one plane can use the runway at a time, and planes must wait for their turn.

1. **Instructions**:
   - Define a `Plane` class implementing `Runnable`, representing a plane waiting to take off.
   - Use a `synchronized` method to control runway access.
   - Implement a `takeOff()` method where each plane attempts to use the runway sequentially.

2. **Code**:
   ```java
   class Runway {
       public synchronized void takeOff(String planeName) {
           System.out.println(planeName + " is taking off...");
           try {
               Thread.sleep(2000); // Simulate take-off time
           } catch (InterruptedException e) {
               System.out.println(planeName + " take-off interrupted.");
           }
           System.out.println(planeName + " has successfully taken off.");
       }
   }

   class Plane implements Runnable {
       private final String planeName;
       private final Runway runway;

       public Plane(String planeName, Runway runway) {
           this.planeName = planeName;
           this.runway = runway;
       }

       @Override
       public void run() {
           System.out.println(planeName + " is ready to take off.");
           runway.takeOff(planeName);
       }
   }

   public class AirportSimulation {
       public static void main(String[] args) {
           Runway runway = new Runway();
           Thread plane1 = new Thread(new Plane("Plane A", runway));
           Thread plane2 = new Thread(new Plane("Plane B", runway));
           Thread plane3 = new Thread(new Plane("Plane C", runway));

           plane1.start();
           plane2.start();
           plane3.start();
       }
   }
   ```

3. **Output**:
   ```
   Plane A is ready to take off.
   Plane A is taking off...
   Plane B is ready to take off.
   Plane C is ready to take off.
   Plane A has successfully taken off.
   Plane B is taking off...
   ...
   ```

---

### **Exercise 7: Race Simulation with Threads**

**Description**: Create a race simulation where multiple runners (threads) compete to finish first. Each runner moves forward in random increments, and the race ends when one runner reaches the finish line.

1. **Instructions**:
   - Define a `Runner` class implementing `Runnable`, with each runner advancing at a random speed.
   - Use a `volatile` flag to signal when the race ends.
   - Track each runner’s position, and declare a winner when the first runner crosses the finish line.

2. **Code**:
   ```java
   import java.util.Random;
   import java.util.concurrent.ExecutorService;
   import java.util.concurrent.Executors;
   import java.util.concurrent.TimeUnit;

   class Runner implements Runnable {
       private static volatile boolean raceOver = false;
       private final String name;
       private static final int FINISH_LINE = 100;

       public Runner(String name) {
           this.name = name;
       }

       @Override
       public void run() {
           Random random = new Random();
           int position = 0;

           while (!raceOver && position < FINISH_LINE) {
               position += random.nextInt(10) + 1; // Move forward by 1-10 units
               System.out.println(name + " ran to position: " + position);
               try {
                   Thread.sleep(100);
               } catch (InterruptedException e) {
                   e.printStackTrace();
               }
           }

           if (!raceOver && position >= FINISH_LINE) {
               raceOver = true;
               System.out.println(name + " wins the race!");
           }
       }
   }

   public class RaceSimulation {
       public static void main(String[] args) {
           ExecutorService race = Executors.newFixedThreadPool(3);
           System.out.println("Race has started!");

           race.execute(new Runner("Runner 1"));
           race.execute(new Runner("Runner 2"));
           race.execute(new Runner("Runner 3"));

           race.shutdown();
           try {
               race.awaitTermination(5, TimeUnit.SECONDS);
           } catch (InterruptedException e) {
               e.printStackTrace();
           }
       }
   }
   ```

3. **Output**:
   ```
   Race has started!
   Runner 1 ran to position: 5
   Runner 2 ran to position: 7
   Runner 3 ran to position: 3
   Runner 1 ran to position: 15
   ...
   Runner 2 wins the race!
   ```

---

## Section 28: Introduction to Exception Handling in Java

#### **Group 1: Basics of Exception Handling and Thought Process (Steps 1-3)**
   - **Why Grouped**: These steps introduce core concepts of exception handling, including understanding the stack trace, and basic error handling using `try` and `catch`.

#### **Puzzles**

**Puzzle 1**: **Simulating a NullPointerException**
   - **Problem**: Create a program that intentionally causes a `NullPointerException` by accessing a method on a `null` object. Use a `try-catch` block to handle the exception.
   - **Code**:
     ```java
     public class NullPointerExample {
         public static void main(String[] args) {
             try {
                 String str = null;
                 System.out.println(str.length());
             } catch (NullPointerException e) {
                 System.out.println("Caught a NullPointerException: " + e.getMessage());
             }
         }
     }
     ```
   - **Output**:
     ```
     Caught a NullPointerException: null
     ```

**Puzzle 2**: **Exception Flow Up the Call Stack**
   - **Problem**: Write methods `methodA`, `methodB`, and `methodC`, where `methodC` throws an exception, and `methodA` catches it. Observe the flow of the exception up the call stack.
   - **Code**:
     ```java
     public class ExceptionFlow {
         public static void main(String[] args) {
             try {
                 methodA();
             } catch (Exception e) {
                 System.out.println("Exception caught in main: " + e.getMessage());
             }
         }

         static void methodA() throws Exception {
             methodB();
         }

         static void methodB() throws Exception {
             methodC();
         }

         static void methodC() throws Exception {
             throw new Exception("Exception from methodC");
         }
     }
     ```
   - **Output**:
     ```
     Exception caught in main: Exception from methodC
     ```

### **Existing Quiz Questions**

1. **What is an exception in Java?**

- A) A condition that indicates the successful completion of a program
- B) A statement that is used to handle errors in a program
- C) An event that occurs during the execution of a program and disrupts the normal flow of instructions (Answer: C)

2. **Which of the following is an example of an exception?**

- A) A program running out of memory.
- B) A division by zero error.
- C) Both A and B. ( Answer: C)

3. **What happens if an exception is not handled in a program?**

- A) The program continues running normally.
- B) The program terminates abruptly. (Answer: B)
- C) The program enters a loop until the exception is resolved.

4. **How can you handle an exception in Java?**

- A) By using the try-catch block. (Answer: A)
- B) By using the if-else statement.
- C) By using the throw keyword.

5. **What is the purpose of the `catch` block in a try-catch block?**

- A) To define the code that may throw an exception.
- B) To write code to handle the exception. (Answer: B)

6. **What happens if an exception is caught in a catch block?**

- A) The program continues running normally after the catch block. (Answer: A)
- B) The program terminates abruptly and an error message is displayed.
- C) The program enters a loop until the exception is resolved.

### **New Quiz Questions**

1. **What is the purpose of the `try` and `catch` blocks in Java?**
   - A) To store multiple variables
   - B) To handle exceptions and prevent program crashes **(Answer)**
   - C) To declare variables as final

2. **Which method is used to print a detailed stack trace of an exception in Java?**
   - A) `e.printStackTrace()` **(Answer)**
   - B) `System.out.println(e)`
   - C) `e.toString()`

### **Fun Fact**
- **Did you know?** Java’s exception handling system was inspired by Ada, a language used in real-time, high-stakes applications like aviation software, emphasizing safety and reliability.

---

#### **Group 2: Exception Hierarchy, Matching, and Catching (Steps 4-6)**
   - **Why Grouped**: This set explains the structure of exception types in Java, discusses the exception hierarchy, and covers the significance of `finally` blocks.

#### **Puzzles**

**Puzzle 1**: **Multiple Catch Blocks**
   - **Problem**: Write a program using multiple `catch` blocks for `NullPointerException` and `ArrayIndexOutOfBoundsException`. Test by triggering each exception and observe the handling mechanism.
   - **Code**:
     ```java
     public class MultipleCatchExample {
         public static void main(String[] args) {
             try {
                 String[] arr = null;
                 System.out.println(arr[1]);
             } catch (NullPointerException e) {
                 System.out.println("Caught NullPointerException");
             } catch (ArrayIndexOutOfBoundsException e) {
                 System.out.println("Caught ArrayIndexOutOfBoundsException");
             }
         }
     }
     ```
   - **Output**:
     ```
     Caught NullPointerException
     ```

**Puzzle 2**: **Using finally for Resource Cleanup**
   - **Problem**: Demonstrate the use of `finally` to close a resource, regardless of whether an exception is thrown or not.
   - **Code**:
     ```java
     import java.io.FileReader;
     import java.io.IOException;

     public class FinallyExample {
         public static void main(String[] args) {
             FileReader reader = null;
             try {
                 reader = new FileReader("test.txt");
                 System.out.println("File opened successfully.");
             } catch (IOException e) {
                 System.out.println("File not found.");
             } finally {
                 try {
                     if (reader != null) reader.close();
                     System.out.println("File closed.");
                 } catch (IOException e) {
                     e.printStackTrace();
                 }
             }
         }
     }
     ```
   - **Output**:
     ```
     File not found.
     File closed.
     ```

### **Existing Quiz Questions**

1. **What is the root class of the Java exception hierarchy?**

- A) RuntimeException
- B) Exception
- C) Throwable (Answer: C)

2. **Which of the following is true about the exception hierarchy in Java?**

- A) All exceptions in Java are subclasses of Exception.
- B) NullPointerException is a subclass of RuntimeException.
- C) Both A and B. (Answer: C)

3. **How can you ensure that a resource is always released, even if an exception occurs?**

- A) By using the try-catch block.
- B) By using the finally block. (Answer: B)
- C) By using the throw keyword.

4. **When is the code inside the `finally` block executed?**

- A) Only when an exception occurs.
- B) Only when there is no exception.
- C) Whether an exception occurs or not. (Answer: C)

### **New Quiz Questions**

1. **What is the purpose of the `finally` block?**
   - A) To execute code regardless of an exception occurrence **(Answer)**
   - B) To handle checked exceptions only
   - C) To ignore runtime exceptions

2. **When should you use multiple catch blocks?**
   - A) When catching different types of exceptions **(Answer)**
   - B) When trying to avoid all exceptions
   - C) To always catch unchecked exceptions

### **Fun Fact**
- **Did you know?** The `finally` block always executes after the `try-catch` sequence, making it an ideal spot for resource cleanup tasks.

---

#### **Group 3: Checked vs. Unchecked Exceptions (Steps 7-8)**
   - **Why Grouped**: This group explores checked and unchecked exceptions, clarifying their differences and the specific handling requirements in Java.

#### **Puzzles**

**Puzzle 1**: **Checked Exception Simulation with Thread.sleep()**
   - **Problem**: Use `Thread.sleep()` to trigger a checked `InterruptedException` and handle it properly.
   - **Code**:
     ```java
     public class CheckedExceptionExample {
         public static void main(String[] args) {
             try {
                 riskyMethod();
             } catch (InterruptedException e) {
                 System.out.println("Caught InterruptedException: " + e.getMessage());
             }
         }

         static void riskyMethod() throws InterruptedException {
             Thread.sleep(1000);
         }
     }
     ```
   - **Output**:
     ```
     (After 1 second delay)
     Caught InterruptedException: sleep interrupted
     ```

**Puzzle 2**: **Unchecked Exception Simulation**
   - **Problem**: Trigger a `RuntimeException` in the same program, and observe that it doesn’t need to be explicitly caught.
   - **Code**:
     ```java
     public class UncheckedExceptionExample {
         public static void main(String[] args) {
             throw new RuntimeException("Unchecked exception example");
         }
     }
     ```
   - **Output**:
     ```
     Exception in thread "main" java.lang.RuntimeException: Unchecked exception example
     ```

### **Existing Quiz Questions**

1. **Which category of exceptions are unchecked exceptions?**

- A) RuntimeException and its sub-classes (Answer: A)
- B) All sub-classes of Exception excluding RuntimeException
- C) InterruptedException and its sub-classes

2. **Which category of exceptions are checked exceptions?**

- A) RuntimeException and its sub-classes
- B) All sub-classes of Exception excluding RuntimeException and subclasses of RuntimeException (Answer: B)
- C) InterruptedException and its sub-classes

### **New Quiz Questions**

1. **Which of these exceptions must be handled by the programmer?**
   - A) `NullPointerException`
   - B) `IOException` **(Answer)**
   - C) `ArithmeticException`

2. **What keyword is used to propagate a checked exception up the call chain?**
   - A) `catch`
   - B) `throws` **(Answer)**
   - C) `return`

### **Fun Fact**
- **Did you know?** In Java, checked exceptions must be either caught or declared in the method signature, whereas unchecked exceptions are optional to catch.

---

#### **Group 4: Throwing Exceptions and Custom Exceptions (Steps 9-11)**
   - **Why Grouped**: This group covers throwing standard exceptions, creating custom exceptions, and their usage.

#### **Puzzles**

**Puzzle 1**: **Throwing a Custom Exception**
   - **Problem**: Create a custom `InvalidCurrencyException` and throw it when currencies don’t match in a currency conversion method.
   - **Code**:
     ```java
     class InvalidCurrencyException extends Exception {
         public InvalidCurrencyException(String message) {
             super(message);
         }
     }

     public class CustomExceptionDemo {
         public static void main(String[] args) {
             try {
                 checkCurrency("USD", "EUR");
             } catch (InvalidCurrencyException e) {
                 System.out.println("Caught custom exception: " + e.getMessage());
             }
         }

         static void checkCurrency(String currency1, String currency2) throws InvalidCurrencyException {
             if (!currency1.equals(currency2)) {
                 throw new InvalidCurrencyException("Currencies do not match!");
             }
         }
     }
     ```
   - **Output**:
     ```
     Caught custom exception: Currencies do not match!
     ```

### **Existing Quiz Questions**

1. **What is the purpose of the `throws` keyword in Java?**

- A) To handle an exception within a method using a try-catch block.
- B) To declare that a method may throw a specific type of exception. (Answer: B)
- C) To indicate that an exception has occurred in a method.

2. **What is the benefit of throwing a custom exception in Java?**

- A) It allows you to provide more specific information about the error that occurred.
- B) It allows you to create your own exception hierarchy.
- C) It allows you to catch and handle the exception in a more specific way.
- D) All of the above. (Answer: D)

### **New Quiz Questions**

1. **When should you throw a custom exception?**
   - A) To indicate a specific error not covered by standard exceptions **(Answer)**
   - B) To print error messages to the console
   - C) To declare variables as constant

### **Fun Fact**
- **Did you know?** Custom exceptions can make your code easier to understand and debug, as they communicate specific issues more clearly than generic exceptions.

---

#### **Group 5: Best Practices in Exception Handling (Steps 12-14)**
   - **Why Grouped**: This final group emphasizes best practices, including using try-with-resources and avoiding unnecessary exception handling.

#### **Puzzles**

**Puzzle 1**: **Try-with-Resources Example**
   - **Problem**: Use a try-with-resources

 statement to automatically close a file reader resource.
   - **Code**:
     ```java
     import java.io.BufferedReader;
     import java.io.FileReader;
     import java.io.IOException;

     public class TryWithResourcesExample {
         public static void main(String[] args) {
             try (BufferedReader reader = new BufferedReader(new FileReader("example.txt"))) {
                 System.out.println("File content: " + reader.readLine());
             } catch (IOException e) {
                 System.out.println("Exception while reading file: " + e.getMessage());
             }
         }
     }
     ```
   - **Output**:
     ```
     Exception while reading file: example.txt (No such file or directory)
     ```

### **Existing Quiz Questions**

1. **Which interface must a resource implement to be compatible with try-with-resources?**

- A) Closeable
- B) AutoCloseable (Answer: B)
- C) Resource
- D) Disposable

2. **What is the purpose of the try-with-resources statement in Java?**

- A) To handle exceptions in a try-catch-finally block.
- B) To automatically manage resources that implement the AutoCloseable interface. (Answer: B)
- C) To terminate the program abruptly.

### **New Quiz Questions**

1. **What is the purpose of try-with-resources?**
   - A) Automatically closes resources **(Answer)**
   - B) Reduces memory allocation
   - C) Optimizes CPU usage

2. **What will happen if an exception is not caught in Java?**
   - A) The program terminates **(Answer)**
   - B) The exception is ignored
   - C) The JVM handles it automatically

### **Fun Fact**
- **Did you know?** The `try-with-resources` statement, introduced in Java 7, simplifies resource management and reduces potential memory leaks by auto-closing resources.

--- 

### Additional Coding Exercises

### **Exercise 1: Bank Account Simulation with Custom Exception Handling**

**Description**: Create a `BankAccount` class where users can withdraw funds. Implement a custom exception `InsufficientFundsException` to handle scenarios where a withdrawal amount exceeds the account balance.

**Code**:

```java
class InsufficientFundsException extends Exception {
    public InsufficientFundsException(String message) {
        super(message);
    }
}

class BankAccount {
    private double balance;

    public BankAccount(double balance) {
        this.balance = balance;
    }

    public void withdraw(double amount) throws InsufficientFundsException {
        if (amount > balance) {
            throw new InsufficientFundsException("Insufficient funds. Balance: " + balance);
        }
        balance -= amount;
        System.out.println("Withdrawal successful! Remaining Balance: " + balance);
    }

    public double getBalance() {
        return balance;
    }
}

public class Main {
    public static void main(String[] args) {
        BankAccount account = new BankAccount(500);
        try {
            account.withdraw(100); // Should succeed
            account.withdraw(600); // Should throw InsufficientFundsException
        } catch (InsufficientFundsException e) {
            System.out.println("Exception: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- `InsufficientFundsException` is a custom exception that inherits from `Exception`.
- If the withdrawal amount exceeds the balance, `InsufficientFundsException` is thrown with a message.
- The `catch` block handles the custom exception and outputs the error message.

**Output**:
```plaintext
Withdrawal successful! Remaining Balance: 400.0
Exception: Insufficient funds. Balance: 400.0
```

---

### **Exercise 2: Online Shopping Cart with Checked Exceptions**

**Description**: Implement an online shopping cart system where each `Product` has a limited stock. Create a custom `OutOfStockException` to manage inventory.

**Code**:

```java
class OutOfStockException extends Exception {
    public OutOfStockException(String message) {
        super(message);
    }
}

class Product {
    private String name;
    private int stock;

    public Product(String name, int stock) {
        this.name = name;
        this.stock = stock;
    }

    public void purchase(int quantity) throws OutOfStockException {
        if (quantity > stock) {
            throw new OutOfStockException("Insufficient stock for product: " + name);
        }
        stock -= quantity;
        System.out.println("Purchased " + quantity + " of " + name + ". Stock left: " + stock);
    }

    public int getStock() {
        return stock;
    }
}

public class Main {
    public static void main(String[] args) {
        Product product = new Product("Laptop", 5);
        try {
            product.purchase(2); // Successful purchase
            product.purchase(4); // Will throw OutOfStockException
        } catch (OutOfStockException e) {
            System.out.println("Exception: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- `OutOfStockException` is thrown if the quantity requested is greater than the stock.
- The `catch` block outputs the exception message.

**Output**:
```plaintext
Purchased 2 of Laptop. Stock left: 3
Exception: Insufficient stock for product: Laptop
```

---

### **Exercise 3: File Handling with `try-with-resources`**

**Description**: Implement a file reading operation using `try-with-resources`. The program should handle exceptions gracefully and ensure the file is closed automatically.

**Code**:

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class FileReadExample {
    public static void main(String[] args) {
        String filePath = "sample.txt";
        
        try (BufferedReader reader = new BufferedReader(new FileReader(filePath))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            System.out.println("Error reading file: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- `try-with-resources` ensures that the file is automatically closed after the operation.
- The `catch` block handles `IOException`, displaying an error message if file reading fails.

**Output** (If `sample.txt` contains "Hello World!"):
```plaintext
Hello World!
```

---

### **Exercise 4: Guess the Number Game with Exception Handling**

**Description**: Create a number-guessing game where players try to guess a randomly generated number. Handle invalid inputs (e.g., non-integer inputs) using exception handling.

**Code**:

```java
import java.util.InputMismatchException;
import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        Random random = new Random();
        int targetNumber = random.nextInt(100) + 1;
        Scanner scanner = new Scanner(System.in);
        int attempts = 0;
        boolean guessedCorrectly = false;

        System.out.println("Guess the number between 1 and 100!");

        while (!guessedCorrectly) {
            System.out.print("Enter your guess: ");
            try {
                int guess = scanner.nextInt();
                attempts++;
                if (guess == targetNumber) {
                    System.out.println("Congratulations! You've guessed the number in " + attempts + " attempts.");
                    guessedCorrectly = true;
                } else if (guess < targetNumber) {
                    System.out.println("Too low! Try again.");
                } else {
                    System.out.println("Too high! Try again.");
                }
            } catch (InputMismatchException e) {
                System.out.println("Invalid input! Please enter a valid number.");
                scanner.next(); // Clear invalid input
            }
        }
        scanner.close();
    }
}
```

**Explanation**:
- `InputMismatchException` is handled to manage non-integer inputs.
- If the guess is too high or low, feedback is provided, allowing the player to continue guessing until they succeed.

**Output** (example):
```plaintext
Guess the number between 1 and 100!
Enter your guess: abc
Invalid input! Please enter a valid number.
Enter your guess: 50
Too high! Try again.
Enter your guess: 25
Congratulations! You've guessed the number in 2 attempts.
```

---

### **Exercise 5: Library Management System with Book Reservation**

**Description**: Design a Library Management System where users can reserve books. If a book is already reserved, throw a custom `BookNotAvailableException`. Implement exception handling to manage book reservation and return.

**Code**:

```java
class BookNotAvailableException extends Exception {
    public BookNotAvailableException(String message) {
        super(message);
    }
}

class Book {
    private String title;
    private boolean isReserved;

    public Book(String title) {
        this.title = title;
        this.isReserved = false;
    }

    public void reserve() throws BookNotAvailableException {
        if (isReserved) {
            throw new BookNotAvailableException("Book '" + title + "' is already reserved.");
        }
        isReserved = true;
        System.out.println("Book '" + title + "' reserved successfully.");
    }

    public void returnBook() {
        isReserved = false;
        System.out.println("Book '" + title + "' returned.");
    }
}

public class LibrarySystem {
    public static void main(String[] args) {
        Book book = new Book("Java Programming");

        try {
            book.reserve();
            book.reserve(); // Attempt to reserve again, should throw exception
        } catch (BookNotAvailableException e) {
            System.out.println("Exception: " + e.getMessage());
        } finally {
            book.returnBook(); // Ensure the book is returned
        }
    }
}
```

**Explanation**:
- `BookNotAvailableException` is a custom exception triggered when a reserved book is attempted to be reserved again.
- The `finally` block ensures the book is returned after the reservation process, releasing the reservation regardless of the exception.

**Output**:
```plaintext
Book 'Java Programming' reserved successfully.
Exception: Book 'Java Programming' is already reserved.
Book 'Java Programming' returned.
```

---

### **Exercise 6: Quiz Competition with Time-Limited Questions**

**Description**: Create a quiz application where each question has a time limit. If the user fails to answer within the specified time, throw a `TimeLimitExceededException`.

**Code**:

```java
import java.util.Scanner;
import java.util.concurrent.*;

class TimeLimitExceededException extends Exception {
    public TimeLimitExceededException(String message) {
        super(message);
    }
}

class QuizGame {
    private final ExecutorService executor = Executors.newSingleThreadExecutor();

    public String askQuestion(String question, int timeLimit) throws TimeLimitExceededException {
        Callable<String> task = () -> {
            Scanner scanner = new Scanner(System.in);
            System.out.println(question);
            return scanner.nextLine();
        };

        try {
            Future<String> future = executor.submit(task);
            return future.get(timeLimit, TimeUnit.SECONDS);
        } catch (TimeoutException e) {
            throw new TimeLimitExceededException("Time limit exceeded for this question!");
        } catch (Exception e) {
            return "An error occurred.";
        }
    }

    public void endQuiz() {
        executor.shutdown();
    }
}

public class QuizCompetition {
    public static void main(String[] args) {
        QuizGame quizGame = new QuizGame();

        try {
            String answer = quizGame.askQuestion("What is the capital of France?", 5);
            System.out.println("Your answer: " + answer);
        } catch (TimeLimitExceededException e) {
            System.out.println("Exception: " + e.getMessage());
        } finally {
            quizGame.endQuiz();
        }
    }
}
```

**Explanation**:
- `TimeLimitExceededException` is thrown if the user fails to respond within the allowed time.
- The `ExecutorService` manages the task, allowing a time-bound input mechanism.

**Output** (if the user exceeds the time limit):
```plaintext
What is the capital of France?
Exception: Time limit exceeded for this question!
```

---

### **Exercise 7: Online Banking System with Multi-Level Exception Handling**

**Description**: Build an online banking simulation with funds transfer and balance check operations. If a user tries to transfer an amount greater than their balance, throw an `InsufficientFundsException`. If a negative amount is entered for transfer, throw an `InvalidAmountException`.

**Code**:

```java
class InsufficientFundsException extends Exception {
    public InsufficientFundsException(String message) {
        super(message);
    }
}

class InvalidAmountException extends Exception {
    public InvalidAmountException(String message) {
        super(message);
    }
}

class Account {
    private String accountHolder;
    private double balance;

    public Account(String accountHolder, double balance) {
        this.accountHolder = accountHolder;
        this.balance = balance;
    }

    public void transferFunds(double amount) throws InsufficientFundsException, InvalidAmountException {
        if (amount <= 0) {
            throw new InvalidAmountException("Transfer amount must be positive.");
        }
        if (amount > balance) {
            throw new InsufficientFundsException("Insufficient funds. Available balance: " + balance);
        }
        balance -= amount;
        System.out.println("Transferred " + amount + ". Remaining balance: " + balance);
    }

    public double getBalance() {
        return balance;
    }
}

public class BankingSystem {
    public static void main(String[] args) {
        Account account = new Account("Alice", 500);

        try {
            account.transferFunds(200); // Successful transfer
            account.transferFunds(-50); // Will throw InvalidAmountException
            account.transferFunds(400); // Will throw InsufficientFundsException
        } catch (InsufficientFundsException | InvalidAmountException e) {
            System.out.println("Exception: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- `InvalidAmountException` is thrown if the transfer amount is non-positive.
- `InsufficientFundsException` is thrown if the transfer amount exceeds the balance.
- The `catch` block manages both exceptions using a multi-catch statement.

**Output**:
```plaintext
Transferred 200.0. Remaining balance: 300.0
Exception: Transfer amount must be positive.
Exception: Insufficient funds. Available balance: 300.0
```

---

## Section 29: Files and Directories in Java

#### **Group 1: Listing Files and Directories (Steps 1-2)**
   - **Why Grouped**: This group introduces methods for listing and filtering files in a directory. It covers both single-level file listing with `Files.list()` and recursive listing with `Files.walk()`.

#### **Puzzles**

**Puzzle 1**: **List All Files in a Directory**
   - **Problem**: Write a program that lists all files and folders in a specified directory.
   - **Code**:
     ```java
     import java.nio.file.Files;
     import java.nio.file.Path;
     import java.nio.file.Paths;
     import java.io.IOException;

     public class ListFiles {
         public static void main(String[] args) {
             try {
                 Files.list(Paths.get("."))
                     .forEach(System.out::println);
             } catch (IOException e) {
                 System.out.println("Error listing files: " + e.getMessage());
             }
         }
     }
     ```
   - **Output**:
     ```
     ./.classpath
     ./.project
     ./src
     ./bin
     ./resources
     ```

**Puzzle 2**: **Recursive Directory Listing with Filtering**
   - **Problem**: List all `.java` files within a directory recursively.
   - **Code**:
     ```java
     import java.nio.file.*;
     import java.io.IOException;

     public class ListJavaFiles {
         public static void main(String[] args) {
             try {
                 Files.walk(Paths.get("."))
                      .filter(path -> path.toString().endsWith(".java"))
                      .forEach(System.out::println);
             } catch (IOException e) {
                 System.out.println("Error: " + e.getMessage());
             }
         }
     }
     ```
   - **Output**:
     ```
     ./src/Main.java
     ./src/Utils.java
     ./tests/TestMain.java
     ```

### **New Quiz Questions**

1. **Which method is used to list files in a directory in Java?**
   - A) `Files.readAllLines()`
   - B) `Files.list()` **(Answer)**
   - C) `Files.lines()`

2. **What method allows recursive listing of files in Java?**
   - A) `Files.walk()` **(Answer)**
   - B) `Files.find()`
   - C) `Files.lines()`

### **Fun Fact**

- **Did you know?** The `Files.walk()` method allows for depth-first traversal of a file tree, providing developers an efficient way to navigate large directory structures.

---

#### **Group 2: Reading and Writing Files (Steps 3-4)**
   - **Why Grouped**: This group focuses on file content operations, covering reading and writing methods with `Files.readAllLines()`, `Files.lines()`, and `Files.write()`.

#### **Puzzles**

**Puzzle 1**: **Read from a File and Print Each Line**
   - **Problem**: Write a program to read all lines from a file and print each line to the console.
   - **Code**:
     ```java
     import java.nio.file.*;
     import java.io.IOException;
     import java.util.List;

     public class ReadFileExample {
         public static void main(String[] args) {
             Path path = Paths.get("resources/data.txt");
             try {
                 List<String> lines = Files.readAllLines(path);
                 lines.forEach(System.out::println);
             } catch (IOException e) {
                 System.out.println("Error reading file: " + e.getMessage());
             }
         }
     }
     ```
   - **Output** (assuming `data.txt` contains "Hello World!" and "Java is great!"):
     ```
     Hello, World!
     Java is great!
     ```

**Puzzle 2**: **Write Content to a File**
   - **Problem**: Create a list of strings and write each string to a file.
   - **Code**:
     ```java
     import java.nio.file.*;
     import java.io.IOException;
     import java.util.List;

     public class WriteToFile {
         public static void main(String[] args) {
             Path path = Paths.get("resources/output.txt");
             List<String> content = List.of("Java", "Python", "C++");
             try {
                 Files.write(path, content);
                 System.out.println("Content written to file.");
             } catch (IOException e) {
                 System.out.println("Error writing to file: " + e.getMessage());
             }
         }
     }
     ```
   - **Output**:
     ```
     Content written to file.
     ```

### **New Quiz Questions**

1. **Which method reads all lines of a file at once?**
   - A) `Files.lines()`
   - B) `Files.readAllLines()` **(Answer)**
   - C) `Files.walk()`

2. **Which method is best for reading large files line-by-line in Java?**
   - A) `Files.readAllLines()`
   - B) `Files.write()`
   - C) `Files.lines()` **(Answer)**

3. **What does the `Files.write()` method do?**
   - A) Reads content from a file
   - B) Writes content to a file **(Answer)**
   - C) Lists files in a directory

### **Fun Fact**

- **Did you know?** The `Files.lines()` method allows reading large files line-by-line, making it highly efficient for big data applications and minimizing memory use.

---

#### **Group 3: Conclusion and Best Practices (Step 5)**
   - **Why Grouped**: This group summarizes the best practices for handling files, especially when managing large files, using functional programming concepts like `map` and `filter` with file streams.

#### **Puzzles**

**Puzzle 1**: **Use Stream API to Count Lines in a File**
   - **Problem**: Count the number of lines in a file using `Files.lines()` and display the result.
   - **Code**:
     ```java
     import java.nio.file.*;
     import java.io.IOException;

     public class CountLinesInFile {
         public static void main(String[] args) {
             Path path = Paths.get("resources/sample.txt");
             try {
                 long lineCount = Files.lines(path).count();
                 System.out.println("Total lines: " + lineCount);
             } catch (IOException e) {
                 System.out.println("Error reading file: " + e.getMessage());
             }
         }
     }
     ```
   - **Output** (if `sample.txt` contains 3 lines):
     ```
     Total lines: 3
     ```

**Puzzle 2**: **File Copy with Best Practices**
   - **Problem**: Copy content from one file to another, demonstrating best practices.
   - **Code**:
     ```java
     import java.nio.file.*;
     import java.io.IOException;

     public class FileCopyExample {
         public static void main(String[] args) {
             Path source = Paths.get("resources/source.txt");
             Path destination = Paths.get("resources/destination.txt");

             try {
                 Files.copy(source, destination, StandardCopyOption.REPLACE_EXISTING);
                 System.out.println("File copied successfully.");
             } catch (IOException e) {
                 System.out.println("Error copying file: " + e.getMessage());
             }
         }
     }
     ```
   - **Output**:
     ```
     File copied successfully.
     ```

### **New Quiz Questions**

1. **Which class is used to handle file paths in Java’s NIO package?**
   - A) `Paths` **(Answer)**
   - B) `FileReader`
   - C) `FileInputStream`

2. **What is a recommended best practice when handling large files in Java?**
   - A) Load the entire file into memory
   - B) Use `Files.lines()` to read line-by-line **(Answer)**
   - C) Avoid using streams for large files

3. **How does `Files.copy()` behave if the destination file already exists and `REPLACE_EXISTING` is not specified?**
   - A) It will overwrite the file
   - B) It will throw an `IOException` **(Answer)**
   - C) It will append content to the file

### **Fun Fact**

- **Did you know?** The `StandardCopyOption.REPLACE_EXISTING` option allows developers to specify whether they want to overwrite an existing file, providing control over file copy operations and reducing potential errors.

---

### Additional Coding Exercises

### **Exercise 1: File Directory Explorer with Filtering and Sorting**

**Description**: Create a program that explores a directory, lists all `.txt` files in a specified directory, and sorts them by their last modified date in descending order.

**Code**:

```java
import java.nio.file.*;
import java.io.IOException;
import java.nio.file.attribute.BasicFileAttributes;
import java.util.Comparator;
import java.util.stream.Stream;

public class DirectoryExplorer {
    public static void main(String[] args) {
        Path path = Paths.get("resources"); // specify the directory path

        try (Stream<Path> stream = Files.list(path)) {
            stream.filter(p -> p.toString().endsWith(".txt"))
                  .sorted((p1, p2) -> {
                      try {
                          BasicFileAttributes attr1 = Files.readAttributes(p1, BasicFileAttributes.class);
                          BasicFileAttributes attr2 = Files.readAttributes(p2, BasicFileAttributes.class);
                          return attr2.lastModifiedTime().compareTo(attr1.lastModifiedTime());
                      } catch (IOException e) {
                          return 0;
                      }
                  })
                  .forEach(System.out::println);
        } catch (IOException e) {
            System.out.println("Error accessing directory: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- Filters files with `.txt` extension.
- Sorts the files by last modified date in descending order.
- Outputs the sorted list of `.txt` files to the console.

**Output**:
```plaintext
resources/report.txt
resources/log.txt
resources/notes.txt
```

---

### **Exercise 2: File Word Counter**

**Description**: Develop a program that reads a file and counts the occurrences of each word, ignoring case sensitivity.

**Code**:

```java
import java.nio.file.*;
import java.io.IOException;
import java.util.HashMap;
import java.util.Map;
import java.util.stream.Stream;

public class WordCounter {
    public static void main(String[] args) {
        Path path = Paths.get("resources/sample.txt"); // specify the file path

        Map<String, Integer> wordCount = new HashMap<>();

        try (Stream<String> lines = Files.lines(path)) {
            lines.forEach(line -> {
                String[] words = line.toLowerCase().split("\\W+");
                for (String word : words) {
                    if (word.isEmpty()) continue;
                    wordCount.put(word, wordCount.getOrDefault(word, 0) + 1);
                }
            });

            wordCount.forEach((word, count) -> System.out.println(word + ": " + count));
        } catch (IOException e) {
            System.out.println("Error reading file: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- Reads a text file and splits each line into words, converting them to lowercase.
- Counts occurrences of each word and stores them in a `Map`.
- Displays each word and its frequency in the console.

**Output**:
```plaintext
java: 3
programming: 2
language: 1
```

---

### **Exercise 3: File Search Game**

**Description**: Create a file search game where users try to guess the name of a file that exists in a directory. The program hints if their guesses are close by showing the files alphabetically near the guessed name.

**Code**:

```java
import java.nio.file.*;
import java.io.IOException;
import java.util.List;
import java.util.Scanner;
import java.util.stream.Collectors;
import java.util.stream.Stream;

public class FileGuessGame {
    public static void main(String[] args) {
        Path path = Paths.get("resources");
        Scanner scanner = new Scanner(System.in);
        
        try (Stream<Path> stream = Files.list(path)) {
            List<String> fileNames = stream.map(p -> p.getFileName().toString())
                                           .sorted()
                                           .collect(Collectors.toList());

            System.out.println("Guess the name of a file in the directory (hint: type 'list' to see all files).");
            String guess;
            
            while (true) {
                System.out.print("Enter your guess: ");
                guess = scanner.nextLine().trim();
                
                if (guess.equalsIgnoreCase("list")) {
                    fileNames.forEach(System.out::println);
                    continue;
                }

                if (fileNames.contains(guess)) {
                    System.out.println("Correct! The file exists in the directory.");
                    break;
                } else {
                    System.out.println("Incorrect. Here are some close matches:");
                    fileNames.stream()
                             .filter(name -> name.compareTo(guess) > 0)
                             .limit(3)
                             .forEach(System.out::println);
                }
            }
        } catch (IOException e) {
            System.out.println("Error accessing directory: " + e.getMessage());
        }
        
        scanner.close();
    }
}
```

**Explanation**:
- Lists files in a directory and allows the user to guess file names.
- Provides hints by displaying a few file names alphabetically near the incorrect guess.

**Output**:
```plaintext
Guess the name of a file in the directory (hint: type 'list' to see all files).
Enter your guess: sample.txt
Incorrect. Here are some close matches:
summary.txt
test.txt
```

---

### **Exercise 4: Directory Size Calculator with Progress Display**

**Description**: Write a program that calculates the total size of all files in a directory. Display progress by printing each file’s size as it is calculated.

**Code**:

```java
import java.nio.file.*;
import java.io.IOException;
import java.nio.file.attribute.BasicFileAttributes;
import java.util.stream.Stream;

public class DirectorySizeCalculator {
    public static void main(String[] args) {
        Path path = Paths.get("resources"); // specify directory

        try (Stream<Path> stream = Files.walk(path)) {
            long totalSize = stream.filter(Files::isRegularFile)
                                   .mapToLong(p -> {
                                       try {
                                           long size = Files.size(p);
                                           System.out.println("File: " + p + " Size: " + size + " bytes");
                                           return size;
                                       } catch (IOException e) {
                                           System.out.println("Error reading file: " + p);
                                           return 0L;
                                       }
                                   })
                                   .sum();
            
            System.out.println("Total Directory Size: " + totalSize + " bytes");
        } catch (IOException e) {
            System.out.println("Error accessing directory: " + e.getMessage());
        }
    }
}
```

**Explanation**:
- Recursively traverses a directory and calculates the size of each file.
- Outputs each file’s size as it’s processed, then displays the total directory size.

**Output**:
```plaintext
File: resources/sample1.txt Size: 256 bytes
File: resources/sample2.txt Size: 512 bytes
File: resources/sample3.txt Size: 128 bytes
Total Directory Size: 896 bytes
```

---

## Section 30: More Concurrency with Concurrent Collections and Atomic Operations

#### **Group 1: Basics of Synchronization and Locks (Steps 1-3)**
   - **Why Grouped**: This group introduces the essentials of synchronization with `synchronized` and its limitations, and progresses to using `ReentrantLock` for more efficient thread management.

#### **Puzzles**

**Puzzle 1**: **Synchronized Counter Example**
   - **Problem**: Implement a thread-safe counter using the `synchronized` keyword.
   - **Code**:
     ```java
     class Counter {
         private int count = 0;

         public synchronized void increment() {
             count++;
         }

         public synchronized int getCount() {
             return count;
         }
     }

     public class SynchronizedCounter {
         public static void main(String[] args) throws InterruptedException {
             Counter counter = new Counter();

             Runnable task = () -> {
                 for (int i = 0; i < 1000; i++) {
                     counter.increment();
                 }
             };

             Thread thread1 = new Thread(task);
             Thread thread2 = new Thread(task);

             thread1.start();
             thread2.start();

             thread1.join();
             thread2.join();

             System.out.println("Final Count: " + counter.getCount());
         }
     }
     ```
   - **Output**:
     ```plaintext
     Final Count: 2000
     ```

**Puzzle 2**: **ReentrantLock with Two Counters**
   - **Problem**: Use `ReentrantLock` to manage synchronization with two separate counters.
   - **Code**:
     ```java
     import java.util.concurrent.locks.ReentrantLock;

     class DualCounter {
         private int counter1 = 0;
         private int counter2 = 0;
         private final ReentrantLock lock1 = new ReentrantLock();
         private final ReentrantLock lock2 = new ReentrantLock();

         public void incrementCounter1() {
             lock1.lock();
             try {
                 counter1++;
             } finally {
                 lock1.unlock();
             }
         }

         public void incrementCounter2() {
             lock2.lock();
             try {
                 counter2++;
             } finally {
                 lock2.unlock();
             }
         }

         public int getCounter1() {
             return counter1;
         }

         public int getCounter2() {
             return counter2;
         }
     }

     public class ReentrantLockExample {
         public static void main(String[] args) throws InterruptedException {
             DualCounter dualCounter = new DualCounter();
             Runnable task1 = dualCounter::incrementCounter1;
             Runnable task2 = dualCounter::incrementCounter2;

             Thread t1 = new Thread(task1);
             Thread t2 = new Thread(task2);
             t1.start();
             t2.start();

             t1.join();
             t2.join();

             System.out.println("Counter1: " + dualCounter.getCounter1());
             System.out.println("Counter2: " + dualCounter.getCounter2());
         }
     }
     ```
   - **Output**:
     ```plaintext
     Counter1: 1
     Counter2: 1
     ```

#### **New Quiz Questions**

1. **Which of the following ensures thread safety for a single method?**
   - A) `volatile`
   - B) `synchronized` **(Answer)**
   - C) `final`

2. **What is a primary limitation of `synchronized` for concurrent methods?**
   - A) Too much concurrency
   - B) Only one thread can execute at a time per object instance **(Answer)**
   - C) Locks only local variables

#### **Fun Fact**

- **Did you know?** Reentrant locks allow the same thread to acquire a lock multiple times without getting stuck. This ability to re-enter is especially useful in recursive calls and complex threading operations.

---

#### **Group 2: Atomic Classes and Concurrent Collections (Steps 4-7)**

   - **Why Grouped**: This group introduces atomic classes like `AtomicInteger` for atomic operations, and `ConcurrentHashMap` for concurrent access to collections with built-in thread safety and regional locking for optimized performance.

#### **Puzzles**

**Puzzle 1**: **Atomic Integer Counter**
   - **Problem**: Implement a thread-safe counter using `AtomicInteger`.
   - **Code**:
     ```java
     import java.util.concurrent.atomic.AtomicInteger;

     class AtomicCounter {
         private AtomicInteger count = new AtomicInteger(0);

         public void increment() {
             count.incrementAndGet();
         }

         public int getCount() {
             return count.get();
         }
     }

     public class AtomicCounterExample {
         public static void main(String[] args) throws InterruptedException {
             AtomicCounter counter = new AtomicCounter();
             Runnable task = counter::increment;

             Thread thread1 = new Thread(task);
             Thread thread2 = new Thread(task);
             thread1.start();
             thread2.start();

             thread1.join();
             thread2.join();

             System.out.println("Final Count: " + counter.getCount());
         }
     }
     ```
   - **Output**:
     ```plaintext
     Final Count: 2
     ```

**Puzzle 2**: **ConcurrentHashMap Character Counter**
   - **Problem**: Use `ConcurrentHashMap` to count occurrences of each character in a string.
   - **Code**:
     ```java
     import java.util.concurrent.ConcurrentHashMap;

     public class ConcurrentCharacterCounter {
         public static void main(String[] args) {
             ConcurrentHashMap<Character, Integer> counter = new ConcurrentHashMap<>();
             String text = "Hello World";

             for (char c : text.toCharArray()) {
                 counter.merge(c, 1, Integer::sum);
             }

             counter.forEach((key, value) -> System.out.println(key + ": " + value));
         }
     }
     ```
   - **Output**:
     ```plaintext
     H: 1
     e: 1
     l: 3
     o: 2
     W: 1
     r: 1
     d: 1
     ```

#### **New uiz Questions**

1. **What class is used to handle atomic integer operations?**
   - A) `Integer`
   - B) `AtomicInteger` **(Answer)**
   - C) `ConcurrentInteger`

2. **Which class provides a thread-safe alternative to `HashMap`?**
   - A) `Hashtable`
   - B) `ConcurrentHashMap` **(Answer)**
   - C) `HashMap`

#### **Fun Fact**

- **Did you know?** `ConcurrentHashMap` employs a segmented locking mechanism, allowing different threads to access distinct regions of the map simultaneously, significantly boosting performance in concurrent environments.

---

#### **Group 3: CopyOnWrite Collections (Step 8)**
   - **Why Grouped**: This group discusses `CopyOnWriteArrayList` and `CopyOnWriteArraySet`, optimized for situations where reads heavily outweigh writes. These collections copy data on each write operation.

#### **Puzzles**

**Puzzle 1**: **CopyOnWriteArrayList Example**
   - **Problem**: Demonstrate how `CopyOnWriteArrayList` allows concurrent reads and occasional writes without affecting other threads.
   - **Code**:
     ```java
     import java.util.List;
     import java.util.concurrent.CopyOnWriteArrayList;

     public class CopyOnWriteExample {
         public static void main(String[] args) {
             List<String> list = new CopyOnWriteArrayList<>(List.of("A", "B", "C"));

             // Reading elements
             for (String s : list) {
                 System.out.println("Reading: " + s);
             }

             // Adding a new element
             list.add("D");

             // Reading elements again
             for (String s : list) {
                 System.out.println("Reading after adding: " + s);
             }
         }
     }
     ```
   - **Output**:
     ```plaintext
     Reading: A
     Reading: B
     Reading: C
     Reading after adding: A
     Reading after adding: B
     Reading after adding: C
     Reading after adding: D
     ```

#### **New Quiz Questions**

1. **Which class is optimized for high reads and low writes?**
   - A) `ArrayList`
   - B) `CopyOnWriteArrayList` **(Answer)**
   - C) `LinkedList`

2. **What happens in a `CopyOnWriteArrayList` when an element is modified?**
   - A) The list is replaced with a new copy **(Answer)**
   - B) The modification is ignored
   - C) It throws an exception

#### **Fun Fact**

- **Did you know?** `CopyOnWriteArrayList` is particularly useful in read-heavy scenarios like cache implementations or applications where data is infrequently updated but frequently read by multiple threads.

---

#### **Group 4: Conclusion and Best Practices (Step 9)**
   - **Why Grouped**: This step provides a wrap-up of best practices for using concurrent collections and atomic operations effectively, emphasizing scenarios and recommendations for choosing the right data structure for optimal performance.

#### **Puzzles**

**Puzzle 1**: **AtomicBoolean for Task Management**
   - **Problem**: Use `AtomicBoolean` to manage a shared resource between threads.
   - **Code**:
     ```java
     import java.util.concurrent.atomic.AtomicBoolean;

     class SharedTask {
         private AtomicBoolean isRunning = new Atomic

Boolean(false);

         public void startTask() {
             if (isRunning.compareAndSet(false, true)) {
                 System.out.println("Task started by " + Thread.currentThread().getName());
             } else {
                 System.out.println("Task already running!");
             }
         }
     }

     public class AtomicBooleanExample {
         public static void main(String[] args) {
             SharedTask task = new SharedTask();

             Runnable taskRunner = task::startTask;

             Thread t1 = new Thread(taskRunner, "Thread-1");
             Thread t2 = new Thread(taskRunner, "Thread-2");
             
             t1.start();
             t2.start();
         }
     }
     ```
   - **Output**:
     ```plaintext
     Task started by Thread-1
     Task already running!
     ```

#### **New Quiz Questions**

1. **What class provides atomic operations for a boolean value?**
   - A) `AtomicBoolean` **(Answer)**
   - B) `AtomicBooleanValue`
   - C) `AtomicFlag`

2. **Which of these is recommended when many threads perform frequent reads but few writes?**
   - A) `ConcurrentHashMap`
   - B) `CopyOnWriteArrayList` **(Answer)**
   - C) `ArrayList`

#### **Fun Fact**

- **Did you know?** Atomic classes, like `AtomicBoolean`, allow multiple threads to safely manage shared flags, making them ideal for controlling tasks and managing shared resources.

---

### Additional Coding Exercises

### **Exercise 1: Concurrent Auction System Simulation**

**Description**: 
Create a simulation of an online auction system where multiple bidders place bids on items simultaneously. Use `ConcurrentHashMap` to store the items and their current highest bids and simulate concurrency by using multiple threads to represent bidders.

**Code**:
```java
import java.util.concurrent.ConcurrentHashMap;
import java.util.concurrent.ThreadLocalRandom;

class Auction {
    private final ConcurrentHashMap<String, Integer> itemBids = new ConcurrentHashMap<>();

    public Auction(String... items) {
        for (String item : items) {
            itemBids.put(item, 0);
        }
    }

    public void placeBid(String item, int bidAmount) {
        itemBids.merge(item, bidAmount, Math::max);  // Only keeps highest bid
    }

    public void displayResults() {
        itemBids.forEach((item, highestBid) -> System.out.println(item + " highest bid: " + highestBid));
    }
}

public class AuctionSimulation {
    public static void main(String[] args) throws InterruptedException {
        Auction auction = new Auction("Laptop", "Smartphone", "Tablet");

        Runnable bidder = () -> {
            for (int i = 0; i < 10; i++) {
                String item = switch (ThreadLocalRandom.current().nextInt(3)) {
                    case 0 -> "Laptop";
                    case 1 -> "Smartphone";
                    default -> "Tablet";
                };
                int bidAmount = ThreadLocalRandom.current().nextInt(100, 1000);
                auction.placeBid(item, bidAmount);
                System.out.println(Thread.currentThread().getName() + " placed a bid of " + bidAmount + " on " + item);
            }
        };

        Thread bidder1 = new Thread(bidder);
        Thread bidder2 = new Thread(bidder);
        Thread bidder3 = new Thread(bidder);

        bidder1.start();
        bidder2.start();
        bidder3.start();

        bidder1.join();
        bidder2.join();
        bidder3.join();

        System.out.println("\nAuction Results:");
        auction.displayResults();
    }
}
```

**Output**:
```plaintext
Thread-0 placed a bid of 450 on Smartphone
Thread-0 placed a bid of 320 on Laptop
Thread-1 placed a bid of 650 on Tablet
Thread-2 placed a bid of 750 on Laptop
...
Auction Results:
Laptop highest bid: 750
Smartphone highest bid: 450
Tablet highest bid: 650
```

---

### **Exercise 2: Atomic Integer Game - Hit Counter**

**Description**: 
Implement a game where players hit a target, and the total hits are counted using `AtomicInteger`. This ensures thread-safe counting, even if multiple players hit the target simultaneously. Each thread represents a player attempting to hit the target.

**Code**:
```java
import java.util.concurrent.atomic.AtomicInteger;

class TargetGame {
    private final AtomicInteger hitCount = new AtomicInteger(0);

    public void hit() {
        hitCount.incrementAndGet();
    }

    public int getHits() {
        return hitCount.get();
    }
}

public class HitCounterGame {
    public static void main(String[] args) throws InterruptedException {
        TargetGame game = new TargetGame();

        Runnable player = () -> {
            for (int i = 0; i < 100; i++) {
                game.hit();
                System.out.println(Thread.currentThread().getName() + " hit the target.");
            }
        };

        Thread player1 = new Thread(player);
        Thread player2 = new Thread(player);
        Thread player3 = new Thread(player);

        player1.start();
        player2.start();
        player3.start();

        player1.join();
        player2.join();
        player3.join();

        System.out.println("\nTotal Hits: " + game.getHits());
    }
}
```

**Output**:
```plaintext
Thread-0 hit the target.
Thread-1 hit the target.
Thread-2 hit the target.
...
Total Hits: 300
```

---

### **Exercise 3: Thread-Safe Chat Room with CopyOnWriteArrayList**

**Description**:
Simulate a chat room where users can join and send messages concurrently. Use `CopyOnWriteArrayList` to store messages and allow multiple threads to simulate concurrent messaging.

**Code**:
```java
import java.util.List;
import java.util.concurrent.CopyOnWriteArrayList;

class ChatRoom {
    private final List<String> messages = new CopyOnWriteArrayList<>();

    public void postMessage(String message) {
        messages.add(message);
    }

    public void displayMessages() {
        messages.forEach(System.out::println);
    }
}

public class ChatRoomSimulation {
    public static void main(String[] args) throws InterruptedException {
        ChatRoom chatRoom = new ChatRoom();

        Runnable user = () -> {
            for (int i = 0; i < 5; i++) {
                String message = Thread.currentThread().getName() + " says hello " + i;
                chatRoom.postMessage(message);
                System.out.println(Thread.currentThread().getName() + " posted: " + message);
            }
        };

        Thread user1 = new Thread(user);
        Thread user2 = new Thread(user);
        Thread user3 = new Thread(user);

        user1.start();
        user2.start();
        user3.start();

        user1.join();
        user2.join();
        user3.join();

        System.out.println("\nChat Room Messages:");
        chatRoom.displayMessages();
    }
}
```

**Output**:
```plaintext
Thread-0 posted: Thread-0 says hello 0
Thread-1 posted: Thread-1 says hello 0
Thread-2 posted: Thread-2 says hello 0
...
Chat Room Messages:
Thread-0 says hello 0
Thread-0 says hello 1
Thread-1 says hello 0
Thread-2 says hello 0
Thread-1 says hello 1
Thread-2 says hello 1
```

---

### **Exercise 4: Multi-threaded Bank Account System Using Locks**

**Description**:
Simulate a bank account system where multiple users try to deposit and withdraw money concurrently. Use `ReentrantLock` to ensure transactions are safely handled without overlapping.

**Code**:
```java
import java.util.concurrent.locks.ReentrantLock;

class BankAccount {
    private double balance;
    private final ReentrantLock lock = new ReentrantLock();

    public BankAccount(double initialBalance) {
        this.balance = initialBalance;
    }

    public void deposit(double amount) {
        lock.lock();
        try {
            balance += amount;
            System.out.println(Thread.currentThread().getName() + " deposited " + amount + ". New Balance: " + balance);
        } finally {
            lock.unlock();
        }
    }

    public void withdraw(double amount) {
        lock.lock();
        try {
            if (balance >= amount) {
                balance -= amount;
                System.out.println(Thread.currentThread().getName() + " withdrew " + amount + ". New Balance: " + balance);
            } else {
                System.out.println(Thread.currentThread().getName() + " tried to withdraw " + amount + " but insufficient funds.");
            }
        } finally {
            lock.unlock();
        }
    }

    public double getBalance() {
        return balance;
    }
}

public class BankAccountSimulation {
    public static void main(String[] args) throws InterruptedException {
        BankAccount account = new BankAccount(500);

        Runnable depositTask = () -> {
            for (int i = 0; i < 3; i++) {
                account.deposit(100);
            }
        };

        Runnable withdrawTask = () -> {
            for (int i = 0; i < 3; i++) {
                account.withdraw(50);
            }
        };

        Thread thread1 = new Thread(depositTask);
        Thread thread2 = new Thread(withdrawTask);
        Thread thread3 = new Thread(depositTask);

        thread1.start();
        thread2.start();
        thread3.start();

        thread1.join();
        thread2.join();
        thread3.join();

        System.out.println("\nFinal Balance: " + account.getBalance());
    }
}
```

**Output**:
```plaintext
Thread-0 deposited 100. New Balance: 600.0
Thread-1 withdrew 50. New Balance: 550.0
Thread-2 deposited 100. New Balance: 650.0
...
Final Balance: 800.0
```

---

> End of this document - Last updated 18:46 10/26