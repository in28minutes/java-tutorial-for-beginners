# Section 31: Java Tips

## Java Tip 01 - Imports and Static Imports

In this tip, we revisited the concept of **imports** and explored the use of **static imports** in Java.

We discussed how to import classes and packages, when imports happen automatically, and how to make your code cleaner and more concise using static imports.

### 1. Default Imports in Java

Some packages in Java are **imported by default**, meaning you do not need to manually import them.

One such package is `java.lang`, which contains essential classes like `String`, `System`, and `Math`.

#### Example:

```java
String str = "Hello, World!";
// No need to import java.lang.String; it's automatically available.
```

#### Key Point:

- **`java.lang`** is imported automatically by the Java compiler.

- No need to explicitly import classes from `java.lang`, such as `String` or `System`.

### 2. Regular Imports

For classes not part of `java.lang`, you need to explicitly **import** them.

This ensures that your program has access to specific classes from other packages, such as `java.util`, `java.io`, etc.

#### Example:

```java
import java.math.BigDecimal;

BigDecimal value = new BigDecimal("123.45");
```

#### Best Practice:

- **Avoid wildcard imports** (e.g., `import java.util.*`). Instead, import specific classes to improve readability and avoid unnecessary imports.
  
  ```java
  import java.util.List;   // Good
  import java.util.*;      // Not recommended
  ```

### 3. Static Imports

**Static imports** allow you to import static members (methods or variables) from a class, so you can access them directly without needing to reference the class name each time.

### 3.1 Static Import of Variables

A common use case is with `System.out`. Normally, you would write `System.out.println()`, but with static imports, you can simplify this to `out.println()`.

#### Example:

```java
import static java.lang.System.out;

public class StaticImportExample {
    public static void main(String[] args) {
        out.println("Static Imports are useful!");
    }
}
```

### 3.2 Static Import of Methods

You can also statically import methods, such as `Collections.sort()`, so you don’t need to reference the class name repeatedly.

#### Example:

```java
import static java.util.Collections.sort;
import java.util.ArrayList;
import java.util.List;

public class StaticImportExample {
    public static void main(String[] args) {
        List<Integer> numbers = new ArrayList<>();
        numbers.add(3);
        numbers.add(1);
        numbers.add(2);

        sort(numbers);  // No need to write Collections.sort(numbers)
        System.out.println(numbers);
    }
}
```

#### When to Use Static Imports:

- Use **static imports** when you are frequently calling static methods or accessing static variables in a class.

- Avoid overusing static imports as they can reduce code clarity by hiding the class origin of methods and variables.

---

## Java Tip 02 - Blocks

In this tip, we explore **blocks** in Java, which are a fundamental part of controlling flow in programs. Blocks are used in structures like **if statements**, **loops**, and methods.

In this lesson, we dive deeper into blocks, best practices for using them, and some tips on how variables behave within blocks.

### What are Blocks?

A **block** in Java is a section of code enclosed within curly braces `{}`. Blocks define a **scope** where variables and logic can be declared and executed.

### Types of Blocks:

- **Method Block**: Encloses the body of a method.

- **Code Block**: A generic block of code enclosed by curly braces, which can be used anywhere.

- **If Block / Loop Block**: A block used to define the statements executed within an `if`, `for`, `while`, or other conditional structures.

### Example of Blocks

### 1. **If Block**

In conditional statements like `if`, a block is used to group the statements that will be executed if the condition is true.

```java
if (3 > 2) {
    System.out.println("3 > 2");  // This is an if block
}
```

### 2. **Else Block**

An `else` block can be added after an `if` block to handle the false condition.

```java
if (3 > 5) {
    System.out.println("This won't be printed.");
} else {
    System.out.println("This is printed because 3 is not greater than 5.");
}
```

### 3. **Best Practice for Blocks**

It is considered **bad practice** to omit curly braces when defining blocks, even if the block contains only one statement. Not using braces can lead to errors or misunderstandings, especially when adding more code later.

#### Example of Bad Practice:

```java
if (3 > 2) 
    System.out.println("3 > 2");
    System.out.println("This is always printed, not part of the if block!"); // Misleading
```

#### Good Practice:

```java
if (3 > 2) {
    System.out.println("3 > 2");
    System.out.println("This is part of the if block.");
}
```

### Standalone Blocks

Blocks do not always need to be associated with a control structure like `if` or `for`. You can create **standalone blocks** to limit the scope of variables, for example.

```java
{
    int i = 10;
    System.out.println("Value inside block: " + i);
}
// Outside the block, variable 'i' is not accessible
System.out.println(i);  // This would cause a compilation error
```

#### Key Point:

- Variables declared inside a block are **local** to that block and cannot be accessed outside of it.

### Variable Scope in Blocks

A variable declared inside a block is **limited to that block's scope**. Once you exit the block, the variable is no longer accessible.

```java
{
    int x = 5;
    System.out.println("x inside block: " + x);
}
// x is not accessible here
System.out.println(x);  // Compilation error: x cannot be resolved to a variable
```

Always use curly braces `{}` to define blocks, even when writing simple one-line conditional statements, as it helps avoid mistakes and makes the code more maintainable.

Understanding blocks and their scope is essential for writing clear and bug-free code.

---

## Java Tip 03 - `equals()` Method

In this tip, we explore the **`equals()` method** in Java, which is used to compare objects for equality. By default, the `equals()` method only checks if two objects refer to the same memory location (i.e., they are the same object).

However, we can override this behavior to provide a more meaningful comparison, such as comparing object values (like IDs). In this tip, we will see how to override `equals()` in a custom class.

### Default Behavior of `equals()` Method

The default implementation of `equals()` is provided by the **`Object` class** in Java. It compares whether two references point to the **same object in memory**.

#### Example:

```java
Client c1 = new Client(1);
Client c2 = new Client(1);

System.out.println(c1.equals(c2));  // Output: false
```

- Even though `c1` and `c2` have the same `id` (1), the default `equals()` method returns **false** because `c1` and `c2` refer to different objects in memory.
  
- If you compare `c1.equals(c1)`, it would return **true** because both references point to the same object.

#### Key Point:

- The default `equals()` method compares **object references**, not object content.

### Overriding `equals()` Method

To compare the **content** of objects (such as comparing two `Client` objects based on their `id`), we need to **override** the `equals()` method.

#### Example Class `Client`:

```java
class Client {
    private int id;

    public Client(int id) {
        this.id = id;
    }

    @Override
    public boolean equals(Object that) {
        if (this == that) return true;  // If both references point to the same object
        if (that == null) return false;  // If the other object is null, return false
        if (getClass() != that.getClass()) return false;  // Ensure both objects are of the same class
        
        Client otherClient = (Client) that;  // Cast the Object to Client
        return this.id == otherClient.id;  // Compare based on id
    }
}
```

#### Explanation:

- **`this == that`**: If both references point to the same object, return `true`.

- **`that == null`**: If the other object is `null`, return `false`.

- **`getClass() != that.getClass()`**: If the objects are of different classes, return `false`.

- **Cast `Object` to `Client`**: Cast the object to the `Client` type for comparison.

- **Compare `id` values**: If the `id` values of both `Client` objects are the same, return `true`.

#### Example of Using Overridden `equals()`:

```java
Client c1 = new Client(1);
Client c2 = new Client(1);

System.out.println(c1.equals(c2));  // Output: true
```

- Now, `c1.equals(c2)` returns **true** because both `Client` objects have the same `id`.

### Why Do We Also Generate `hashCode()`?

- Whenever you override the `equals()` method, it is recommended to also override the **`hashCode()`** method. The `hashCode()` method ensures that objects that are considered equal (according to `equals()`) return the same hash code.

- The **`hashCode()`** method plays an important role when objects are used in **hash-based collections** like `HashMap`, `HashSet`, etc. We will discuss the `hashCode()` method in detail in the next tip.

By overriding `equals()`, you can provide more meaningful comparisons between objects, such as checking if two `Client` objects with the same `id` are considered equal.

---

## Java Tip 04 - `hashCode()` Method

In this tip, we explore the **`hashCode()` method** in Java and its importance, particularly when working with **hash-based collections** such as `HashMap` and `HashSet`.

We also explain why `hashCode()` is usually implemented alongside the `equals()` method and the essential properties that a good `hashCode()` function must follow.

### Why is `hashCode()` Important?

The **`hashCode()` method** is crucial for the efficiency of **hash-based collections** such as `HashMap`, `HashSet`, and `Hashtable`.

These collections use **buckets** to store objects, and an object's **hash code** determines which bucket it will be placed in.

### How HashMap Works:

1. A **hash function** (which uses the object's `hashCode()`) computes an integer value that helps decide the bucket where the object should be placed.

2. The **goal** of a good `hashCode()` implementation is to **distribute objects evenly** across all buckets to avoid collisions and ensure efficient lookups.

#### Example of `hashCode()` and `HashMap`:

```java
Map<Client, String> clientMap = new HashMap<>();
Client c1 = new Client(1);
Client c2 = new Client(1);

clientMap.put(c1, "Client 1");
clientMap.put(c2, "Client 2");

// If equals and hashCode are properly implemented, c1 and c2 will be treated as equal
System.out.println(clientMap.size());  // Output: 1 (if equals and hashCode are correctly implemented)
```

- In the example above, **c1** and **c2** have the same `id`. If `equals()` and `hashCode()` are correctly implemented, both objects should hash to the same bucket and be considered **equal**, so the map size remains 1.

### Properties of a Good `hashCode()` Implementation

To ensure correctness and efficiency in hash-based collections, the **`hashCode()` method** must follow these two key properties:

### 1. **Consistent with `equals()`**

- If two objects are **equal** according to the `equals()` method, then their **`hashCode()` values must also be equal**.
  
### 2. **Stable `hashCode()` Value**

- The **hash code** of an object should remain **consistent** as long as the object's state (used in `equals()`) does not change.

- The **`hashCode()` value** should not change over time unless a field used in `equals()` is modified.

#### Example of a `hashCode()` Implementation:

```java
class Client {
    private int id;

    public Client(int id) {
        this.id = id;
    }

    @Override
    public boolean equals(Object that) {
        if (this == that) return true;
        if (that == null || getClass() != that.getClass()) return false;
        Client client = (Client) that;
        return id == client.id;
    }

    @Override
    public int hashCode() {
        return Integer.hashCode(id);  // hash code based on the 'id'
    }
}
```

#### Key Points:

- **`equals()` and `hashCode()` must work together**: If two objects are equal, they **must** have the same hash code.

- A poor `hashCode()` implementation can lead to inefficient data storage and lookups in hash-based collections (e.g., all objects ending up in the same bucket).

### Why `hashCode()` and `equals()` are Implemented Together

In Java, **`hashCode()` and `equals()`** are often implemented together because they serve complementary roles in ensuring the correct behavior of collections like `HashMap` and `HashSet`. 

- **`equals()`**: Defines object equality based on content (e.g., `id`).

- **`hashCode()`**: Determines the bucket where an object should be stored in hash-based collections.

Java tools like Eclipse offer a combined option to generate both **`hashCode()` and `equals()`** at the same time to ensure consistency and correctness.

---

## Java Tip 05 - Class Access Modifiers: `public` and `default`

In this tip, we explore **class-level access modifiers** in Java. Access modifiers help control the visibility of classes, methods, and variables, promoting **encapsulation**.

The primary focus here is on two access modifiers: **`public`** and **`default`** (also known as package-private), and their impact on class accessibility across different packages.

### Access Modifiers Overview

Java provides four access modifiers:

- **`public`**: Accessible from anywhere.

- **`protected`**: Limited to subclasses and the package (not applicable to classes).

- **`default`** (no modifier): Accessible only within the same package.

- **`private`**: Restricted to the enclosing class (not applicable to classes).

In this tip, we focus on **class-level modifiers** and discuss the use of **`public`** and **`default`**.

### 1. `public` Access Modifier

When a class is marked as **`public`**, it is **accessible from anywhere**—including different packages. This is the most permissive access level.

#### Example:

```java
// In package1
package com.in28minutes.tips.access.package1;

public class ClassAccessModifiers {
    // Class content here
}
```

#### Usage in Another Package:

```java
// In package2
package com.in28minutes.tips.access.package2;

import com.in28minutes.tips.access.package1.ClassAccessModifiers;

public class ClassAccessModifiersRunnerInOtherPackage {
    public static void main(String[] args) {
        ClassAccessModifiers c = new ClassAccessModifiers();  // Accessible since it is public
    }
}
```

#### Key Point:

- A **`public` class** can be accessed from **any package**. It allows other packages to create instances of this class or call its methods.

### 2. `default` (Package-Private) Access Modifier

When no access modifier is specified, the class is said to have **`default` access**, meaning it is only accessible **within the same package**.

This is also known as **package-private** visibility.

#### Example:

```java
// In package1
package com.in28minutes.tips.access.package1;

class ClassAccessModifiers {
    // No public modifier, so this class has default (package-private) access
}
```

#### Trying to Use `default` Class in Another Package:

```java
// In package2
package com.in28minutes.tips.access.package2;

import com.in28minutes.tips.access.package1.ClassAccessModifiers;  // Compilation Error

public class ClassAccessModifiersRunnerInOtherPackage {
    public static void main(String[] args) {
        ClassAccessModifiers c = new ClassAccessModifiers();  // Not accessible outside package1
    }
}
```

#### Key Point:

- A **`default` class** (without an access modifier) is **only accessible within the same package**. It **cannot** be accessed from outside the package.

### Important Rules for Class-Level Access Modifiers

1. **`public` and `default`** are the only access modifiers allowed on a class.

2. **`protected`** and **`private`** cannot be applied to top-level classes. These modifiers are used for methods, fields, and inner classes but not for classes themselves.

#### Example of Invalid Modifiers for Classes:

```java
protected class MyClass {   // Compilation Error: Cannot use protected with classes
    // Class content here
}

private class MyClass {     // Compilation Error: Cannot use private with classes
    // Class content here
}
```

Additionally, we learned that **`protected`** and **`private`** cannot be applied to top-level classes.

The choice of access modifier depends on how much visibility you want to grant to other parts of your code. Encapsulation is a key principle, and selecting the right modifier helps control access to classes effectively.

---

## Java Tip 06 - Method Access Modifiers: `public`, `protected`, `private`, and `default`

In this tip, we explore **method-level access modifiers** in Java. Access modifiers control the visibility of methods within classes, packages, and subclasses, helping to enforce encapsulation.

Java provides four main access modifiers for methods: **`public`**, **`protected`**, **`private`**, and **`default`** (package-private). We will discuss how these modifiers affect method accessibility from the **same class**, **same package**, **subclasses**, and **different packages**.

### Overview of Method Access Modifiers

### 1. **`public`**

- A **`public` method** is accessible **everywhere**—within the same class, package, different packages, and even subclasses.
  
### 2. **`protected`**

- A **`protected` method** is accessible within the **same package** and **subclasses** (even if they are in different packages).
  
### 3. **`private`**

- A **`private` method** is accessible **only within the class** where it is defined. It cannot be accessed from outside the class, even by subclasses.

### 4. **`default`** (package-private)

- When no modifier is specified, a method has **`default`** (also called package-private) access. Such methods are accessible only within the **same package**.

### Example: Method Access Modifiers

We create a class `ExampleClass` with methods of different access modifiers:

```java
package com.in28minutes.tips.access.package1;

public class ExampleClass {
    public void publicMethod() {
        System.out.println("Public method");
    }

    protected void protectedMethod() {
        System.out.println("Protected method");
    }

    void defaultMethod() {
        System.out.println("Default method");
    }

    private void privateMethod() {
        System.out.println("Private method");
    }
}
```

### 1. Access within the **same class**

All methods—**public**, **protected**, **default**, and **private**—can be accessed within the same class.

```java
public class ExampleClass {
    public static void main(String[] args) {
        ExampleClass example = new ExampleClass();
        example.publicMethod();    // Accessible
        example.protectedMethod(); // Accessible
        example.defaultMethod();   // Accessible
        example.privateMethod();   // Accessible
    }
}
```

### 2. Access within the **same package**

In a different class within the same package, you can access **public**, **protected**, and **default** methods. However, **private** methods are not accessible.

```java
package com.in28minutes.tips.access.package1;

public class MethodAccessRunner {
    public static void main(String[] args) {
        ExampleClass example = new ExampleClass();
        example.publicMethod();    // Accessible
        example.protectedMethod(); // Accessible
        example.defaultMethod();   // Accessible
        example.privateMethod();   // Not Accessible - Compilation Error
    }
}
```

### 3. Access from a **different package**

When accessing methods from a different package, only **public** methods are accessible unless the class is extended (for `protected` methods).

```java
package com.in28minutes.tips.access.package2;

import com.in28minutes.tips.access.package1.ExampleClass;

public class MethodAccessRunnerInDifferentPackage {
    public static void main(String[] args) {
        ExampleClass example = new ExampleClass();
        example.publicMethod();    // Accessible
        example.protectedMethod(); // Not Accessible - Compilation Error
        example.defaultMethod();   // Not Accessible - Compilation Error
        example.privateMethod();   // Not Accessible - Compilation Error
    }
}
```

### 4. Access in a **subclass in a different package**

In a subclass from a different package, only **public** and **protected** methods are accessible.

```java
package com.in28minutes.tips.access.package2;

import com.in28minutes.tips.access.package1.ExampleClass;

public class SubClass extends ExampleClass {
    public void testMethods() {
        publicMethod();    // Accessible
        protectedMethod(); // Accessible
        defaultMethod();   // Not Accessible - Compilation Error
        privateMethod();   // Not Accessible - Compilation Error
    }
}
```

### Summary of Access Levels for Methods

| Modifier  | Same Class | Same Package | Subclass (Same Package) | Subclass (Different Package) | Different Package |
|-----------|------------|--------------|-------------------------|------------------------------|-------------------|
| `public`  | Yes        | Yes          | Yes                     | Yes                          | Yes               |
| `protected`| Yes       | Yes          | Yes                     | Yes                          | No                |
| `default` | Yes        | Yes          | Yes                     | No                           | No                |
| `private` | Yes        | No           | No                      | No                           | No                |

---

### Best Practices

1. **Use `public`** when you want your method to be accessible from anywhere.
2. **Use `protected`** for methods that should only be accessible within the same package or subclasses.
3. **Use `private`** for methods that should only be accessible within the same class.
4. **Avoid `default`** unless package-level access is explicitly required.

### Important Note:
- **Variables** follow the same access rules as methods, but it’s generally best practice to keep variables `private` and provide controlled access through methods.

Choosing the right access modifier is crucial for **encapsulation** and helps maintain clear and organized code. Be mindful of how you expose methods in your classes and use the appropriate modifier to control access.

---

# Java Tip 07 - Final Classes and Final Methods

In this tip, we explore the **`final` non-access modifier** in Java. The `final` keyword can be applied to both **classes** and **methods**.

When used, it prevents classes from being extended and methods from being overridden. In this tip, we will cover the purpose of `final` on both classes and methods, its impact on inheritance, and when you might want to use it.

### 1. Final Classes

A **`final class`** cannot be extended or subclassed. Once a class is marked as `final`, no other class can inherit from it. This is useful when you want to prevent modification or extension of the behavior of the class.

#### Syntax:

```java
final class FinalClass {
    // Class content here
}
```

#### Example:

```java
final class FinalClass {
    // Some code here
}

class SomeClass extends FinalClass {  // Compilation error: Cannot subclass a final class
    // This class will cause a compilation error
}
```

### Why Use Final Classes?

Java provides several **final classes** to prevent modification and ensure that certain classes behave predictably. For example:
- **`String`** and **wrapper classes** like `Integer`, `Long`, etc., are marked as `final`. This ensures that no one can modify or extend these classes to alter their behavior, which is important for maintaining the integrity of core Java features like hashing and memory management.

#### Example: String Class

```java
// String is final, meaning it cannot be extended
final class String {
    // Class content here
}
```

#### Key Point:
- A **final class** is used when you want to prevent extension and modification of a class's behavior.
- Examples include core Java classes like `String`, `Integer`, `Long`, etc.

### 2. Final Methods

A **`final method`** cannot be overridden by subclasses. If you want to prevent a method from being overridden in any subclass, you can declare it as `final`.

### Syntax:

```java
class SomeClass {
    public final void doSomething() {
        // Method content here
    }
}
```

#### Example:

```java
class SomeClass {
    public final void doSomething() {
        System.out.println("This method is final.");
    }
}

class ExtendingClass extends SomeClass {
    @Override
    public void doSomething() {  // Compilation error: Cannot override a final method
        // This will cause a compilation error
    }
}
```

### Why Use Final Methods?

You might use `final` on a method when you want to **prevent subclasses from changing the implementation** of that method. This ensures that the method behaves consistently across all subclasses and prevents any potential errors that might occur due to overriding.

#### Example: Enforcing a Method's Logic

Consider a scenario where you have a template method that defines a specific sequence of actions, and you don't want subclasses to modify that sequence:

```java
class Recipe {
    public final void execute() {
        getReady();
        doTheDish();
        cleanup();
    }

    void getReady() { /* Subclass can implement */ }
    void doTheDish() { /* Subclass can implement */ }
    void cleanup() { /* Subclass can implement */ }
}
```

In this example, the `execute()` method is **final** because you don't want subclasses to change the order of the steps in the recipe, while allowing subclasses to define how each step is implemented.

Use the `final` keyword when you want to **protect the integrity** of a class or method by preventing inheritance or modification. This is especially important in cases where modifying behavior could lead to errors or inconsistencies in the system.

---

## Java Tip 08 - Final Variables and Final Arguments

In this tip, we explore the concept of **`final` variables** and **`final` arguments** in Java.

The `final` keyword can be applied to variables and method arguments to ensure that their values can only be assigned once, making them **immutable**. This practice promotes better coding standards and helps in writing more predictable and maintainable code.

### 1. Final Variables

A **`final` variable** is a variable that can only be assigned a value **once**. Once a value has been assigned, it cannot be changed throughout the program. This makes the variable **immutable** after its initial assignment.

#### Syntax:

```java
final int i = 5;
```

#### Example:

```java
public class FinalVariablesExample {
    public static void main(String[] args) {
        final int i = 5;  // i is assigned the value 5
        i = 7;  // Compilation Error: Cannot assign a value to final variable i
    }
}
```

- **Without `final`**: A regular variable's value can be changed multiple times.

- **With `final`**: The variable's value can only be assigned once. Any attempt to change it results in a **compilation error**.

#### Key Point:

- A `final` variable **must** be initialized either at the time of declaration or later in the constructor, but it can only be assigned **once**.

### 2. Final Arguments

A **`final` argument** is a method parameter that cannot be modified inside the method body. Once a method is called, the argument’s value is set and cannot be changed.

#### Syntax:

```java
public void doSomething(final int arg) {
    // arg is a final argument and cannot be modified
}
```

#### Example:

```java
public class FinalArgumentsExample {
    public void doSomething(final int arg) {
        arg = 10;  // Compilation Error: Cannot assign a value to final parameter arg
    }
}
```

- **Without `final`**: You can modify the argument inside the method body, although this is generally not considered a good practice.

- **With `final`**: The argument becomes **immutable** and cannot be reassigned a new value within the method.

#### Key Point:
- Making method arguments `final` ensures that they **remain unchanged** throughout the method, making the method more predictable and easier to understand.

### When to Use `final`?

The **`final` modifier** is typically recommended for both **variables** and **method arguments** to promote **immutability**. Immutable variables make code easier to understand and maintain because their values remain consistent once assigned.

### Advantages of Using `final`:

- **Immutability**: Once a value is assigned, it cannot change, leading to more predictable behavior.

- **Code Readability**: By marking variables and arguments as `final`, it becomes clear to others that these values should not and cannot be changed.

- **Coding Standards**: Many coding standards recommend using `final` wherever possible. Some organizations may flag variables that are not marked as `final` as coding violations.

### Best Practice:
- While it may not be practical to make every variable `final`, you should strive to make **most variables and arguments final** when their values do not need to change. This results in cleaner and more maintainable code.

---

## Java Tip 09 - Why Do We Need Static Variables?

In this tip, we explore the concept of **static variables** in Java. Static variables, unlike instance variables, are shared across all instances of a class.

This makes them useful when you need a common value or state that is shared across all objects of a class. We will look at a practical example to understand the need for static variables.

### What Are Static Variables?

A **static variable** belongs to the **class** rather than to individual instances (objects) of the class. This means that **only one copy** of the static variable is shared among all instances of that class. In contrast, instance variables are unique to each object.

#### Syntax:

```java
class ClassName {
    static int staticVariable;
}
```

#### Example: Player Class with Static Variable

Consider the following example where we track the number of `Player` instances created:

```java
class Player {
    private String name;
    private static int count = 0;  // Static variable shared across all instances

    public Player(String name) {
        this.name = name;
        count++;  // Increment count every time a Player object is created
    }

    public static int getCount() {
        return count;
    }
}
```

#### Example Usage:

```java
public class StaticModifierRunner {
    public static void main(String[] args) {
        Player player1 = new Player("Ronaldo");
        Player player2 = new Player("Federer");

        System.out.println(Player.getCount());  // Output: 2
    }
}
```

#### Key Points:

- **`count` is a static variable**: It is shared among all instances of the `Player` class.

- Each time a new `Player` is created, the `count` variable is incremented.

- The **`getCount()`** method is also static, meaning it can be accessed using the class name (`Player.getCount()`), without needing to instantiate an object.

### Why Do We Need Static Variables?

Static variables are useful when you need **shared data** or a **common state** across all instances of a class. In the example above, the `count` variable tracks how many players have been created across all instances of the `Player` class.

#### Without Static Variable:

```java
class Player {
    private String name;
    private int count = 0;  // Instance variable

    public Player(String name) {
        this.name = name;
        count++;
    }

    public int getCount() {
        return count;
    }
}
```

In this case, each `Player` object has its own `count` variable, and the value of `count` will be reset for every instance. This means:

- `player1.getCount()` will return `1`.

- `player2.getCount()` will also return `1` (not the desired behavior).

#### With Static Variable:

By making the `count` variable **static**, the value is shared across all `Player` objects. This allows us to track the total number of `Player` objects created.

### Key Characteristics of Static Variables

1. **Shared Across Instances**:
   - A static variable is shared across all instances of a class.
   - All objects of the class refer to the same static variable.

2. **Memory Management**:
   - A static variable is stored in a common memory location that is created when the class is loaded.
   - Static variables are initialized only once, at the start of the program's execution, and persist throughout the program.

3. **Accessed via Class Name**:
   - Static variables can be accessed using the class name (e.g., `ClassName.staticVariable`), making it clear that they are shared among all instances.

### When to Use Static Variables

Use static variables when:
- You need to maintain **shared state** or data across all instances of a class.
- The value should remain consistent across all objects (e.g., a counter tracking how many instances of a class have been created).

In this tip, we learned about the importance of **static variables** and how they differ from instance variables. Static variables are useful when you need a **single shared instance** of a variable across all objects of a class, such as tracking the total number of objects created.

---

## Java Tip 09 - Why Do We Need Static Methods?

In this tip, we explore the concept of **static methods** in Java. Static methods belong to the **class** rather than any specific instance of the class, which allows them to be called without creating an object.

Static methods are commonly used when a method performs an operation that is **not dependent on instance-specific data** but rather on class-level or static data. 

We will explore why static methods are useful, especially when working with static variables.

### Why Do We Need Static Methods?

#### Context:
In the previous tip, we discussed **static variables**, which are shared across all instances of a class. When a method only operates on static variables, it is logical to make that method **static**. Static methods are useful because:

- They can be accessed **without needing an instance** of the class.

- They operate on **class-level data** rather than instance-level data.

#### Example: Player Class with Static Method

Consider the following example where we track the number of `Player` instances created. We make the `getCount()` method static because it operates on the static `count` variable, which is shared across all `Player` objects.

```java
class Player {
    private String name;
    private static int count = 0;  // Shared between all instances

    public Player(String name) {
        this.name = name;
        count++;  // Increment the shared count when a new player is created
    }

    // Static method to access the static count variable
    public static int getCount() {
        return count;
    }
}
```

#### Example Usage:

```java
public class StaticModifierRunner {
    public static void main(String[] args) {
        Player player1 = new Player("Ronaldo");
        Player player2 = new Player("Federer");

        // Calling static method using the class name
        System.out.println(Player.getCount());  // Output: 2
    }
}
```

### Why Use Static Methods?

- **Shared Access**: Since `count` is shared among all instances of the `Player` class, the method that accesses it, `getCount()`, should also be shared. This is achieved by making the method static.

- **Class-Level Operations**: Static methods allow you to perform operations related to the **class** itself rather than individual objects. In this case, `Player.getCount()` is a class-level operation.

### Static Methods vs Instance Methods

- **Static Methods**:
  - Can be called using the **class name** (e.g., `Player.getCount()`).
  - Do not depend on any instance-specific data.
  - Operate on **static data** (e.g., static variables).

- **Instance Methods**:
  - Must be called using an **instance of the class** (e.g., `player1.getName()`).
  - Can access both **instance-specific** and **static data**.

#### Example:

```java
Player player1 = new Player("Ronaldo");

// Calling instance method
player1.getName();  // Instance method, needs an object

// Calling static method
Player.getCount();  // Static method, can be called with class name
```

Even though it's possible to call a static method using an instance (e.g., `player1.getCount()`), it's **not recommended**. The preferred approach is to call static methods using the **class name**, making it clear that the method belongs to the class, not the instance.

### Key Characteristics of Static Methods

1. **Belong to the Class**:
   - Static methods are associated with the **class itself** rather than any instance.
   - They can be called using the **class name** (e.g., `Player.getCount()`).

2. **Access Only Static Data**:
   - Static methods can only operate on **static variables** or other static methods.
   - They **cannot** access instance variables or instance methods directly.

3. **Common Use Cases**:
   - Utility functions like `Math.max()`, `Collections.sort()`, and factory methods such as `List.of()` and `Map.of()`.
   - Operations that do not depend on instance-specific data.

In this tip, we learned about the importance of **static methods** and why they are useful when dealing with **class-level data** such as static variables.

Static methods can be called without creating an instance of the class, making them perfect for operations that do not depend on instance-specific data.

---

## Java Tip 10 - Static Methods Cannot Use Instance Methods or Variables

In this tip, we explore an important rule about **static methods** in Java: **static methods cannot access instance methods or variables**. This rule stems from the fact that static methods belong to the **class itself**, not to any particular object instance.

On the other hand, instance methods and variables belong to individual objects. In this tip, we will break down why this limitation exists and how it impacts the way you write static methods.

### Static Methods vs Instance Methods

- **Static Methods**:
  - Belong to the **class** itself and can be called without creating an object.
  - Can only access **static variables** and other **static methods**.
  
- **Instance Methods**:
  - Belong to a specific **instance** of a class and can access both **instance variables** (specific to an object) and **static variables** (shared across all objects).

#### Example: Player Class with Static and Instance Methods

Let's continue using the `Player` class from the previous examples, but this time, we'll focus on how static methods and instance methods interact with variables and methods.

```java
class Player {
    private String name;  // Instance variable
    private static int count = 0;  // Static variable

    public Player(String name) {
        this.name = name;
        count++;  // Increment shared count for every new Player object
    }

    // Static method that returns the total count of players
    public static int getCount() {
        return count;
    }

    // Instance method that returns the name of the player
    public String getName() {
        return name;
    }
}
```

### Static Methods Cannot Access Instance Variables or Methods

A **static method** operates at the class level and does not have access to object-specific data, such as **instance variables** or **instance methods**. This is because static methods do not require an instance of the class to be called.

#### Example of What You **Cannot** Do:

```java
public static void getPlayerInfo() {
    System.out.println(name);  // Compilation error: Cannot make a static reference to a non-static field 'name'
}
```

- **Why does this fail?**
  - The variable `name` is an **instance variable**, meaning it belongs to a specific object of the `Player` class.
  - The static method `getPlayerInfo()` belongs to the class itself, and there is no specific object instance to provide the `name` value for.
  
#### What You **Can** Do:

Static methods can only access **static variables** or call other **static methods**.

```java
public static void printPlayerCount() {
    System.out.println(getCount());  // Allowed: static method accessing static method
}
```

#### Instance Methods Can Access Both Static and Instance Data

In contrast, **instance methods** can access both instance variables and static variables. Since instance methods are called on an object, they can access object-specific data as well as class-level data.

```java
public void printDetails() {
    System.out.println("Player: " + getName());  // Allowed: instance method accessing instance variable
    System.out.println("Total Players: " + getCount());  // Allowed: instance method accessing static method
}
```

### Key Rules for Static Methods

1. **Static methods can only access static variables**:
   - Static variables belong to the class and are shared across all instances, so static methods can access them directly.
   - Example:
     ```java
     public static int getCount() {
         return count;  // Allowed: accessing static variable
     }
     ```

2. **Static methods can only call static methods**:
   - Since static methods do not have an associated instance, they cannot call instance methods.
   - Example:
     ```java
     public static void showCount() {
         getCount();  // Allowed: static method accessing another static method
     }
     ```

3. **Instance methods can access both static and instance data**:
   - Instance methods are tied to a specific object, so they can access both instance variables (specific to that object) and static variables (shared by all objects).
   - Example:
     ```java
     public void printNameAndCount() {
         System.out.println("Name: " + name);  // Accessing instance variable
         System.out.println("Count: " + getCount());  // Accessing static variable
     }
     ```

### Why This Limitation Exists

The main reason for this limitation is that **static methods** are not tied to any particular object. They are called on the class itself, and since there is no specific object associated with a static method, there is no instance data (such as instance variables or instance methods) available for the static method to access.

On the other hand, **instance methods** are always tied to an object, so they have access to both the object-specific data (instance variables) and class-level data (static variables).

---

## Java Tip 11 - `public static final` - Constants

In this tip, we explore the **`public static final`** combination in Java, which is used to define **constants**. Constants are values that do not change throughout the execution of a program.

Java makes extensive use of constants in its core classes, and understanding how and why to use them helps in writing more readable and maintainable code.

We will also discuss the importance of using **`public static final`** for clarity and reusability in programs.

### What is `public static final`?

The `public static final` combination has three components:
- **`public`**: The constant can be accessed from anywhere.
- **`static`**: The constant belongs to the class itself and not to any specific instance. This means there is only one copy of the constant shared among all instances of the class.
- **`final`**: The value cannot be changed once initialized. The constant is immutable.

#### Syntax:

```java
public static final <type> CONSTANT_NAME = <value>;
```

#### Example:

```java
public class ConstantsExample {
    public static final int SECONDS_IN_MINUTE = 60;
    public static final int MINUTES_IN_HOUR = 60;
    public static final int HOURS_IN_DAY = 24;

    public static final int SECONDS_IN_DAY = SECONDS_IN_MINUTE * MINUTES_IN_HOUR * HOURS_IN_DAY;
}
```

### Why Use `public static final`?

1. **Clarity and Readability**:
   - Using constants makes the code **self-explanatory**. Rather than hardcoding values, constants give meaningful names to values, making the code easier to understand.
   - Example:
     ```java
     int secondsInDay = 60 * 60 * 24;  // Hard to understand what these numbers represent
     ```
     vs
     ```java
     int secondsInDay = SECONDS_IN_MINUTE * MINUTES_IN_HOUR * HOURS_IN_DAY;  // Clear and understandable
     ```

2. **Reusability**:
   - Once a constant is declared as `public static final`, it can be accessed from anywhere in the program.
   - Example:
     ```java
     System.out.println(ConstantsExample.SECONDS_IN_DAY);  // Accessing the constant from another class
     ```

3. **Immutability**:
   - Since the value is marked as `final`, it cannot be changed after it is initialized. This ensures **consistency** throughout the application.

### Example: Using Constants

Let’s consider a real-world example where we calculate the number of seconds in a day.

#### Without Constants:

```java
public class TimeCalculator {
    public static void main(String[] args) {
        int secondsInDay = 60 * 60 * 24;  // Hardcoded values
        System.out.println("Seconds in a day: " + secondsInDay);
    }
}
```

This works, but it's not immediately clear what the numbers represent. Now, let's rewrite it using `public static final` constants.

#### With `public static final` Constants:

```java
public class ConstantsExample {
    public static final int SECONDS_IN_MINUTE = 60;
    public static final int MINUTES_IN_HOUR = 60;
    public static final int HOURS_IN_DAY = 24;

    public static final int SECONDS_IN_DAY = SECONDS_IN_MINUTE * MINUTES_IN_HOUR * HOURS_IN_DAY;
}

public class TimeCalculator {
    public static void main(String[] args) {
        System.out.println("Seconds in a day: " + ConstantsExample.SECONDS_IN_DAY);  // Using constants
    }
}
```

By using constants, the code becomes more **understandable** and **maintainable**.

### Real-World Use of `public static final` in Java

Java makes extensive use of `public static final` for constants in core libraries. For example:

1. **`Integer.MIN_VALUE` and `Integer.MAX_VALUE`**:
   - In the `Integer` class, constants like `MIN_VALUE` and `MAX_VALUE` represent the minimum and maximum values an `int` can hold.
   - Example:
     ```java
     System.out.println("Min value of int: " + Integer.MIN_VALUE);
     System.out.println("Max value of int: " + Integer.MAX_VALUE);
     ```

2. **Other APIs Using `public static final`**:
   - Many classes in the Java API, such as `Collections`, `Arrays`, and `Math`, define constants using `public static final` to make their values accessible globally without allowing modification.

### Benefits of Using Constants

- **Prevents Magic Numbers**:
  - Magic numbers are hardcoded numbers that appear in code without context. Using constants replaces these magic numbers with meaningful names.
  - Example:
    ```java
    public static final int DAYS_IN_WEEK = 7;
    ```

- **Easier Maintenance**:
  - If you need to update the value of a constant (e.g., a configuration setting), you only need to change it in one place, and the change will propagate across the entire codebase.

- **Improved Code Understanding**:
  - Constants make the intent of the code clearer to others who read it, reducing the learning curve and improving maintainability.

In this tip, we explored the use of **`public static final`** to define constants. Using constants helps make your code more readable, maintainable, and error-free.

They provide a clear way to define values that should remain unchanged throughout the program. Java heavily uses constants in its core libraries, and you should also make use of this pattern when writing your programs.

---

## Java Tip 12 - Nested Classes: Inner Class vs Static Nested Class

In this tip, we explore **Nested Classes** in Java, focusing on the differences between **Inner Classes** and **Static Nested Classes**. 

Nested classes are defined within another class, and depending on whether they are static or not, they behave differently. Understanding when and how to use these different types of nested classes helps in writing more modular and organized code.

### What Are Nested Classes?

A **Nested Class** is any class that is defined inside another class. There are two types of nested classes in Java:
1. **Inner Class**: A non-static nested class.
2. **Static Nested Class**: A nested class marked with the `static` keyword.

#### Example:

```java
public class OuterClass {
    class InnerClass {
        // Inner class (non-static nested class)
    }

    static class StaticNestedClass {
        // Static nested class
    }
}
```

### Inner Class vs Static Nested Class

### 1. Inner Class (Non-Static Nested Class)

An **Inner Class** is a class that is nested within another class and **cannot exist independently** of the enclosing class. It requires an instance of the outer class to be created.

#### Key Characteristics:
- An instance of an Inner Class can only be created if an instance of the **enclosing (outer) class** exists.
- An Inner Class **can access** the instance variables and methods of the enclosing class.

#### Example of Inner Class:

```java
public class OuterClass {
    private int outerValue = 10;

    class InnerClass {
        public void display() {
            System.out.println("Outer class value: " + outerValue);  // Access outer class's instance variable
        }
    }
}
```

To create an instance of `InnerClass`, you must first create an instance of `OuterClass`:

```java
OuterClass outer = new OuterClass();
OuterClass.InnerClass inner = outer.new InnerClass();
inner.display();  // Output: Outer class value: 10
```

### 2. Static Nested Class

A **Static Nested Class** is a nested class marked with the `static` keyword. Unlike inner classes, a static nested class **can exist independently** of an instance of the outer class. It behaves more like a top-level class but is still logically grouped with its enclosing class.

#### Key Characteristics:
- A Static Nested Class **can be instantiated without creating an instance** of the enclosing class.
- It **cannot access** the instance variables or instance methods of the enclosing class directly.

#### Example of Static Nested Class:

```java
public class OuterClass {
    private int outerValue = 10;

    static class StaticNestedClass {
        public void display() {
            // System.out.println(outerValue);  // Error: Cannot access non-static outer class members
            System.out.println("Static nested class.");
        }
    }
}
```

To create an instance of `StaticNestedClass`, you don't need an instance of `OuterClass`:

```java
OuterClass.StaticNestedClass staticNested = new OuterClass.StaticNestedClass();
staticNested.display();  // Output: Static nested class.
```

### Differences Between Inner Class and Static Nested Class

| Feature                        | Inner Class                                | Static Nested Class                         |
|---------------------------------|--------------------------------------------|--------------------------------------------|
| **Keyword**                     | No `static` keyword                        | Declared with `static` keyword             |
| **Requires Outer Class Instance** | Yes                                       | No                                         |
| **Access to Outer Class Members** | Can access all instance variables and methods of the outer class | Cannot access instance variables or methods of the outer class |
| **Instantiation**               | Requires an instance of the outer class    | Can be instantiated independently of the outer class |
| **Use Case**                    | When you need a tight coupling between the inner class and the outer class | When the nested class is more loosely related to the outer class and does not depend on instance data |

### Code Example: Inner Class vs Static Nested Class

```java
public class NestedClassRunner {
    private int outerValue = 42;

    // Inner Class (Non-Static Nested Class)
    class InnerClass {
        public void display() {
            System.out.println("Inner class can access outerValue: " + outerValue);  // Access instance variable
        }
    }

    // Static Nested Class
    static class StaticNestedClass {
        public void display() {
            // Cannot access outerValue directly
            System.out.println("Static nested class.");
        }
    }

    public static void main(String[] args) {
        // Creating an instance of Inner Class
        NestedClassRunner outer = new NestedClassRunner();
        NestedClassRunner.InnerClass inner = outer.new InnerClass();
        inner.display();  // Output: Inner class can access outerValue: 42

        // Creating an instance of Static Nested Class
        NestedClassRunner.StaticNestedClass staticNested = new NestedClassRunner.StaticNestedClass();
        staticNested.display();  // Output: Static nested class.
    }
}
```

---

## Java Tip 13 - Anonymous Classes

In this tip, we explore the concept of **Anonymous Classes** in Java. An anonymous class is a **class without a name** and is typically used when you need to override a method or implement an interface on the spot, without creating a separate named class.

Anonymous classes are useful when the implementation is only required for a short scope and won't be reused elsewhere.

### What Is an Anonymous Class?

An **anonymous class** in Java is a type of **inner class** that is created **without a class name**. It is used to instantiate classes or interfaces inline, often to provide custom implementations for methods without the need for a full class declaration.

### Syntax:

```java
new <interface-or-class>() {
    // Method implementations
};
```

Anonymous classes are often used when:
- You need to provide a quick implementation of an interface or class.
- The implementation is short and specific to a particular use case.
- You do not plan to reuse the implementation elsewhere in the code.

### Example: Sorting a List with an Anonymous Comparator

Let's consider sorting a list of strings by their length. Normally, you would use a `Comparator` to define the custom sorting logic.

#### Regular Comparator Implementation:

```java
import java.util.*;

public class LengthComparator implements Comparator<String> {
    @Override
    public int compare(String str1, String str2) {
        return Integer.compare(str1.length(), str2.length());
    }
}
```

To use this `LengthComparator`:

```java
List<String> animals = new ArrayList<>(List.of("Ant", "Cat", "Ball", "Elephant"));
Collections.sort(animals, new LengthComparator());
System.out.println(animals);  // Output: [Ant, Cat, Ball, Elephant]
```

### Using an Anonymous Class:

Instead of creating a separate `LengthComparator` class, you can implement the `Comparator` interface directly using an **anonymous class**.

```java
List<String> animals = new ArrayList<>(List.of("Ant", "Cat", "Ball", "Elephant"));

Collections.sort(animals, new Comparator<String>() {
    @Override
    public int compare(String str1, String str2) {
        return Integer.compare(str1.length(), str2.length());
    }
});

System.out.println(animals);  // Output: [Ant, Cat, Ball, Elephant]
```

In this example:
- We use the `new Comparator<String>() { ... }` syntax to create an anonymous class that implements the `Comparator` interface.
- There is no need to define a separate named class (`LengthComparator`), and the comparator is defined and used in the same place.

### Why Use Anonymous Classes?

1. **Convenience**: You can provide an implementation directly at the point where it's needed, without cluttering your code with unnecessary class declarations.
2. **Encapsulation**: If the implementation is only required for a specific use case and won't be reused, it can be kept hidden within the scope where it's relevant.
3. **Reduce Boilerplate**: It simplifies the code when a full class declaration is not required.

However, use anonymous classes sparingly, as they can make your code harder to maintain and understand if overused or applied inappropriately.

### Key Points About Anonymous Classes

1. **No Name**: An anonymous class does not have a class name. The instance of the class is created immediately after the class definition.
   
2. **Implements an Interface or Extends a Class**: An anonymous class must either implement an interface or extend a class.

3. **One-Time Use**: Anonymous classes are typically used for one-time use cases where you don't need to reuse the implementation elsewhere.

4. **Access to Variables**: Anonymous classes can access local variables of the enclosing method, but only if the variables are declared `final` or effectively final.

#### Example:

```java
int base = 5;

Collections.sort(animals, new Comparator<String>() {
    @Override
    public int compare(String str1, String str2) {
        // Anonymous class can access local variable 'base'
        return Integer.compare(str1.length() + base, str2.length() + base);
    }
});
```

In this case, the anonymous class can access the `base` variable because it is effectively final.

### Use Cases of Anonymous Classes

1. **Event Listeners**: Often used in UI programming (e.g., handling button clicks).
   
2. **Comparators**: As shown in the example, anonymous classes are frequently used when you need to implement custom sorting logic.

3. **Runnable Implementations**: For providing quick implementations of the `Runnable` interface when starting threads.

#### Example: Runnable with Anonymous Class

```java
new Thread(new Runnable() {
    @Override
    public void run() {
        System.out.println("Thread is running");
    }
}).start();
```

In this case, we use an anonymous class to provide a `Runnable` implementation directly.

### Anonymous Classes vs Lambda Expressions

Anonymous classes and **lambda expressions** both allow for concise implementations of interfaces with a single method (functional interfaces).

However, lambda expressions are more concise and are preferred in most cases where functional programming is supported.

#### Example: Lambda vs Anonymous Class for Comparator

#### Anonymous Class:
```java
Collections.sort(animals, new Comparator<String>() {
    @Override
    public int compare(String str1, String str2) {
        return Integer.compare(str1.length(), str2.length());
    }
});
```

#### Lambda Expression:
```java
Collections.sort(animals, (str1, str2) -> Integer.compare(str1.length(), str2.length()));
```

The lambda expression is more concise and achieves the same result.

---

## Java Tip 14 - Why Enum and Enum Basics: `ordinal` and `values`

In this tip, we explore **Enums** in Java, short for **Enumerations**. Enums are a special type of class that represent a fixed set of constants.

They are useful when you need to define a variable that can only take one out of a small set of possible values, such as days of the week, seasons, or directions.

This tip covers:
- What an enum is.
- How to define and use enums.
- Utility methods like `ordinal()` and `values()`.

### Why Use Enums?

Enums help restrict variables to predefined constants. For example, if you are representing the seasons of the year, you can use `String` to represent them, but it would not prevent someone from assigning invalid values like `"Garbage"`.

Using enums enforces the valid set of values, ensuring that only allowed values can be used.

#### Example with String (Problematic):

```java
String season = "Summer";  // This is fine.
season = "Garbage";        // This is not valid, but there is no restriction.
```

#### Example with Enum (Correct Approach):

```java
enum Season {
    WINTER, SPRING, SUMMER, FALL;
}

// Now, season can only have one of the valid values defined in the enum.
Season season = Season.WINTER;
```

### Defining and Using Enums

Enums in Java are defined similarly to a class but use the `enum` keyword. Inside the enum, you list the allowed values (known as constants).

#### Defining an Enum:

```java
public enum Season {
    WINTER, SPRING, SUMMER, FALL;
}
```

#### Using Enums:

```java
Season currentSeason = Season.SUMMER;
System.out.println(currentSeason);  // Output: SUMMER
```

By using enums, you restrict the variable to only accept predefined values (`WINTER`, `SPRING`, `SUMMER`, and `FALL`).

### Utility Methods for Enums

Java enums come with built-in utility methods that make them easier to work with.

### 1. `valueOf(String name)`

The `valueOf` method returns the enum constant of the specified string name, but it must exactly match the name of one of the constants in the enum (case-sensitive).

#### Example:

```java
Season season1 = Season.valueOf("WINTER");
System.out.println(season1);  // Output: WINTER
```

If you pass an invalid string or incorrect case (e.g., `"winter"`), it will throw an exception:
```java
// Throws java.lang.IllegalArgumentException
Season season2 = Season.valueOf("winter");  // Case-sensitive!
```

### 2. `ordinal()`

The `ordinal` method returns the **position** of the enum constant in the enum declaration, starting from `0`.

#### Example:

```java
System.out.println(Season.WINTER.ordinal());  // Output: 0
System.out.println(Season.SPRING.ordinal());  // Output: 1
```

#### Important Note:
Avoid using `ordinal()` to store enum values in a database because if the order of enum constants changes in the future, it will break the integrity of your data. Always store enums by name rather than ordinal.

### 3. `values()`

The `values` method returns an array of all the constants in the enum, which allows you to iterate over the enum constants.

#### Example:

```java
Season[] allSeasons = Season.values();
System.out.println(Arrays.toString(allSeasons));  
// Output: [WINTER, SPRING, SUMMER, FALL]
```

This method is useful for looping over all possible values of the enum.

### Example: Using Enum with Methods

Let's put everything together in an example:

```java
import java.util.Arrays;

public class EnumRunner {
    public enum Season {
        WINTER, SPRING, SUMMER, FALL;
    }

    public static void main(String[] args) {
        // Assigning an enum constant
        Season currentSeason = Season.SUMMER;
        System.out.println("Current season: " + currentSeason);

        // Using valueOf to convert a string to an enum constant
        Season season1 = Season.valueOf("WINTER");
        System.out.println("Season from valueOf: " + season1);

        // Using ordinal to get the position of enum constants
        System.out.println("WINTER ordinal: " + Season.WINTER.ordinal());
        System.out.println("SPRING ordinal: " + Season.SPRING.ordinal());

        // Using values() to list all enum constants
        Season[] allSeasons = Season.values();
        System.out.println("All seasons: " + Arrays.toString(allSeasons));
    }
}
```

#### Output:

```java
Current season: SUMMER
Season from valueOf: WINTER
WINTER ordinal: 0
SPRING ordinal: 1
All seasons: [WINTER, SPRING, SUMMER, FALL]
```

### Key Points to Remember

1. **Enums provide a way to restrict variables** to predefined constants, improving code safety and readability.
   
2. **Enums can be used like classes**: they can have fields, methods, and constructors, though we only covered the basics here.
   
3. **`ordinal()`**: Returns the position of the enum constant in its declaration (starting from 0).
   
4. **`values()`**: Returns all constants in the enum as an array.
   
5. **`valueOf(String name)`**: Converts a string into the corresponding enum constant, but the string must exactly match the constant's name (case-sensitive).

Enums are a powerful tool in Java that allow you to represent a fixed set of constants in a type-safe manner.

They help make your code more robust and easier to maintain by limiting the possible values a variable can take.

In this tip, we discussed the basics of enums, focusing on utility methods like `ordinal()` and `values()`. In the next tip, we'll dive deeper into enums and explore how you can assign custom values to them.

---

## Java Tip 15 - Enum: Constructor, Variables, and Methods

In this tip, we will dive deeper into **Enums** in Java and explore how they can have **constructors**, **variables**, and **methods**. We will also look at how to assign custom values to enum constants, which can be useful for storing them in a database.

This helps to overcome the limitation of using `ordinal()` for database storage, as the ordinal can change if the order of enum constants is modified.

### Why Avoid `ordinal()` for Storing Enums in Databases?

As discussed earlier, using `ordinal()` for storing enums in a database is risky because `ordinal()` depends on the position of the enum constant in the declaration. If the order of the enum constants changes, the ordinal values will also change, causing inconsistency in the stored data.

The solution is to assign **custom values** to enum constants and use these values for database storage.

### Enum Constructor, Variables, and Methods

Enums in Java can have:
- **Instance variables** to hold data specific to each enum constant.
- **Constructors** to initialize these instance variables.
- **Methods** to access or manipulate the values.

#### Defining Enums with Custom Values

To assign custom values to enum constants, we need to define a constructor in the enum and pass the value to it.

#### Example:

```java
public enum Season {
    WINTER(1), SPRING(4), SUMMER(2), FALL(3);

    // Enum instance variable
    private int value;

    // Private constructor
    private Season(int value) {
        this.value = value;
    }

    // Getter for the value
    public int getValue() {
        return value;
    }
}
```

#### Key Points:
1. **Enum Constructor**: The constructor is private because enum constants are predefined, and no external class should instantiate enum objects.
2. **Instance Variable**: Each enum constant holds a specific value (e.g., `WINTER(1)` assigns the value `1` to `WINTER`).
3. **Getter Method**: A public getter method `getValue()` is provided to retrieve the assigned value.

### Accessing Enum Values

Once the enum constants have been defined with custom values, you can access these values using the getter method.

#### Example:

```java
public class EnumRunner {
    public static void main(String[] args) {
        // Accessing enum values and custom assigned values
        Season season = Season.SPRING;
        System.out.println("Season: " + season);
        System.out.println("Value of " + season + ": " + season.getValue());
        
        // Printing all enum values and their custom values
        for (Season s : Season.values()) {
            System.out.println(s + " has value: " + s.getValue());
        }
    }
}
```

#### Output:

```
Season: SPRING
Value of SPRING: 4
WINTER has value: 1
SPRING has value: 4
SUMMER has value: 2
FALL has value: 3
```

### Changing the Position of Enum Constants

If you change the order of the enum constants, the `ordinal()` will change, but the custom values assigned will remain the same.

#### Example: Changing the Position of Constants

```java
public enum Season {
    WINTER(1), SUMMER(2), FALL(3), SPRING(4);  // SPRING is now last
}
```

Even though the ordinal of `SPRING` will now be `3`, its value will still be `4`:

```java
System.out.println(Season.SPRING.ordinal());  // Output: 3
System.out.println(Season.SPRING.getValue()); // Output: 4
```

This ensures that custom values remain consistent, even when the enum constants' positions change.

### Enum Methods

Enums can also have methods just like regular classes. In our example, we used a **getter method** `getValue()` to return the custom value of the enum constant. This allows us to expose values without exposing the internal logic or data structure of the enum.

#### Example: Custom Methods in Enums

```java
public enum Season {
    WINTER(1), SPRING(4), SUMMER(2), FALL(3);

    private int value;

    private Season(int value) {
        this.value = value;
    }

    public int getValue() {
        return value;
    }

    // Custom method to check if the season is warm
    public boolean isWarm() {
        return this == SUMMER || this == SPRING;
    }
}
```

Now you can call the custom method on the enum constants:

```java
System.out.println(Season.SUMMER.isWarm());  // Output: true
System.out.println(Season.WINTER.isWarm());  // Output: false
```

Enums in Java are much more than just a list of constants. They can have variables, constructors, and methods, allowing them to model more complex behaviors and data.

By assigning custom values to enums and using methods to access them, you can make your code more robust and adaptable, especially when working with databases.

---

## Java Tip 16 - A Quick Look at Built-in Enums: `Month` and `DayOfWeek`

In the previous tips, we discussed the basics of **Enums** and how to create and use them. Enums are often used when you need a variable to have only a predefined set of values.

In this tip, we will explore some of the **built-in enums** in Java, specifically focusing on `DayOfWeek` and `Month`, which are part of the `java.time` package introduced in Java 8.

### Moving Enums to Their Own Class Files

Enums can be defined as their own independent class files. This allows them to be organized like other Java classes.

#### Example:

```java
public enum Season {
    WINTER, SPRING, SUMMER, FALL;
}
```

Instead of defining this enum inside another class, it can be placed in its own `.java` file as a public enum, allowing other classes to access it more easily.

### Built-in Enums in Java: `DayOfWeek` and `Month`

Java provides several built-in enums as part of its API. Two of the most commonly used enums are:

### 1. `DayOfWeek` (java.time.DayOfWeek)

The `DayOfWeek` enum represents the days of the week, starting from Monday and going up to Sunday. This enum is part of the `java.time` package, which provides comprehensive support for date and time in Java.

#### Example:

```java
import java.time.DayOfWeek;

public class EnumRunner {
    public static void main(String[] args) {
        DayOfWeek today = DayOfWeek.MONDAY;
        System.out.println("Today is: " + today);

        // Looping through all days of the week
        for (DayOfWeek day : DayOfWeek.values()) {
            System.out.println("Day: " + day + " Ordinal: " + day.ordinal());
        }
    }
}
```

#### Output:

```java
Today is: MONDAY
Day: MONDAY Ordinal: 0
Day: TUESDAY Ordinal: 1
Day: WEDNESDAY Ordinal: 2
Day: THURSDAY Ordinal: 3
Day: FRIDAY Ordinal: 4
Day: SATURDAY Ordinal: 5
Day: SUNDAY Ordinal: 6
```

### 2. `Month` (java.time.Month)

The `Month` enum represents the twelve months of the year, starting from January (`1`) to December (`12`). Like `DayOfWeek`, `Month` is part of the `java.time` package.

#### Example:

```java
import java.time.Month;

public class EnumRunner {
    public static void main(String[] args) {
        Month currentMonth = Month.JANUARY;
        System.out.println("Current month is: " + currentMonth);

        // Looping through all months of the year
        for (Month month : Month.values()) {
            System.out.println("Month: " + month + " Ordinal: " + month.ordinal());
        }

        // Getting a Month by its number (1 for January, 12 for December)
        Month monthByNumber = Month.of(3);
        System.out.println("Month for number 3: " + monthByNumber);
    }
}
```

#### Output:

```
Current month is: JANUARY
Month: JANUARY Ordinal: 0
Month: FEBRUARY Ordinal: 1
Month: MARCH Ordinal: 2
Month: APRIL Ordinal: 3
Month: MAY Ordinal: 4
Month: JUNE Ordinal: 5
Month: JULY Ordinal: 6
Month: AUGUST Ordinal: 7
Month: SEPTEMBER Ordinal: 8
Month: OCTOBER Ordinal: 9
Month: NOVEMBER Ordinal: 10
Month: DECEMBER Ordinal: 11
Month for number 3: MARCH
```

#### Key Methods of `Month` Enum:

- `Month.of(int monthNumber)`: Returns the `Month` corresponding to the number passed (e.g., `Month.of(3)` returns `MARCH`).
- `Month.values()`: Returns all the `Month` values in an array.

### Primitive Obsession and Why You Should Use Enums

Many developers often default to using primitive types like `String` or `int` to represent specific values, such as days of the week or months. This is known as **primitive obsession**, and it can lead to errors and poor code readability.

For example, storing the day of the week as a `String` or `int` can easily result in invalid values being assigned.

#### Example of Primitive Obsession:

```java
String day = "Monday";   // Correct
String day = "Funday";   // Invalid, but no compile-time check
```

Using enums helps prevent this issue by providing a fixed set of values that can be assigned, ensuring type safety and reducing the possibility of errors.

#### Example with Enum (Correct Approach):

```java
DayOfWeek day = DayOfWeek.MONDAY;   // Correct
// DayOfWeek day = "Funday";       // Invalid, compile-time error
```

Enums also improve the readability of your code by making it clear what kind of values are expected, and they are much easier to maintain and extend.

In this tip, we explored some of the **built-in enums** in Java, specifically focusing on `DayOfWeek` and `Month`.

These enums are part of the `java.time` package and are used to represent days of the week and months of the year, respectively.

When you're working with values that have a predefined set of constants, such as days, months, or directions, consider using enums to make your code cleaner, more maintainable, and less error-prone.

---