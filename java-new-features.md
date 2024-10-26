# Section 34: Java New Features - Java 10 to Java 16

## Step 01 - Understanding Java Versions: A 10,000 Feet Overview

Java has undergone numerous changes since its inception, with new releases now arriving every six months.

In this step, we will cover the key Java versions, their release timelines, and the new approach to versioning that Oracle has adopted in recent years.

This will provide a high-level understanding of Java’s evolution and the versioning system.

### Early Java Versions

The first version of Java was released as **JDK 1.0** in **January 1996**, marking the beginning of what would become one of the most widely used programming languages.

Subsequent versions included JDK 2, 3, and 4. However, a major release came in **September 2004** with **J2SE 5.0**.

### Key Milestones (1996 - 2004):

- **JDK 1.0**: Released in January 1996.

- **J2SE 5.0**: Released in September 2004. This marked the fifth release of Java in eight years.

### Java SE 8 - A Landmark Release

The most significant release, according to many, is **Java SE 8**, which was released in **March 2014**. This version brought **functional programming** to Java and introduced important features such as:

- **Lambda Expressions**

- **Streams API**

- **Method References**

These features made Java SE 8 a transformative release, enabling developers to write more expressive and functional-style code.

Before Java SE 8, functional programming was not possible in Java.

### Transition to Time-based Releases

Starting with **Java SE 9** in **September 2017**, Oracle introduced a shift in the way new versions of Java were released. Between **2004** and **2017**, Java saw only four major releases, from **Java SE 5** to **Java SE 9**. However, this pace would soon change.

From **Java SE 10** (released in **March 2018**), Oracle adopted a **time-based release versioning model**.

This new approach ensures a **new release every six months**. Instead of waiting for specific features to be ready, each release includes whatever features are completed within the six-month timeframe.

### Recent Java Versions (2018 - 2021)

With this shift, Java has seen a dramatic increase in the number of releases. Some of the key releases are:

- **Java SE 10**: Released in March 2018.

- **Java SE 11**: Released in September 2018 (a **long-term support** or LTS release).

- **Java SE 12**: Released in March 2019.

- **Java SE 13**: Released in September 2019.

- **Java SE 14**: Released in March 2020.

- **Java SE 15**: Released in September 2020.

- **Java SE 16**: Released in March 2021.

In just three years (March 2018 to March 2021), there were six new Java releases. 

### Long-Term Support (LTS) Versions

Oracle now offers **long-term support (LTS)** versions every three years. These LTS versions are recommended for use in production environments because they come with extended support and stability guarantees. 

- **Java SE 11** is the most recent LTS release.

- The next LTS version will be **Java SE 17**.

---

## Step 02 - Understanding Java New Features: An Overview

Java has introduced numerous features across various versions, each bringing new capabilities that enhance the language.

In this step, we'll review some of the most important features introduced in older and newer versions of Java, providing a broad overview of how the language has evolved.

### Key Features from Earlier Releases

### J2SE 5.0 (Released in 2004)

**J2SE 5.0** is a significant release that introduced several important language features, including:

- **Enhanced For Loop**: Simplifies iterating through collections.

- **Generics**: Introduced type safety for collections and other types.

- **Enums**: Added support for enumerated types.

- **Autoboxing/Unboxing**: Automatic conversion between primitives and their corresponding wrapper classes.

These features laid the foundation for modern Java programming.

### Java SE 8 (Released in March 2014)

**Java SE 8** is arguably the most important Java release to date because it introduced **functional programming** to the language, significantly changing how Java applications are written. Some key features include:

- **Lambda Expressions**: Enable writing concise anonymous functions.

- **Streams API**: Provide a powerful way to perform functional-style operations on collections of data.

- **Method References**: Simplify the use of lambda expressions by referencing existing methods.

- **Static Methods in Interfaces**: Allowed defining static methods within interfaces.

Java SE 8 revolutionized the language by introducing these functional programming constructs, making code more concise, readable, and expressive.

### Java SE 9 (Released in September 2017)

**Java SE 9** introduced a significant architectural improvement to Java:

- **Modularization**: The JDK was broken into smaller modules, allowing developers to create modularized applications. This improves both scalability and maintainability.
  
We'll explore modularization in more depth in a later step.

### Java SE 10 (Released in March 2018)

**Java SE 10** brought the concept of **local variable type inference**:

- **Local Variable Type Inference**: By using the `var` keyword, Java can infer the type of local variables.

- This reduces the need for explicit type declarations, making code cleaner and less verbose, especially when dealing with complex types.

### Java SE 14 (Released in March 2020)

**Java SE 14** introduced **switch expressions**:

- **Switch Expressions**: In addition to being used as a statement, switch can now be used as an expression, allowing you to return values from switch constructs directly. This results in cleaner and more functional code.

We'll dive deeper into switch expressions in a later step.

### Java SE 15 (Released in September 2020)

**Java SE 15** introduced a new feature for working with multi-line strings:

- **Text Blocks**: Allow you to write multi-line string literals in a more readable and maintainable way.

- This is especially useful for strings that contain special characters, quotes, or span multiple lines.

### Java SE 16 (Released in March 2021)

**Java SE 16** introduced **record classes**, a new way to create data-carrying classes (also known as Java beans):

- **Record Classes**: Provide a concise syntax for creating immutable data classes. With records, you no longer need to manually write getters, setters, constructors, `toString()`, `hashCode()`, and `equals()` methods.

- Instead, you can define all of this with just a few lines of code.

This greatly simplifies the creation of simple data-holding classes.

### Performance Improvements Across Versions

- Each new version of Java typically includes various performance improvements, especially in the area of **garbage collection**.

- As programs create and discard objects, Java uses garbage collection algorithms to reclaim memory.

- Across different Java versions, these algorithms have been continuously optimized for better performance and efficiency.

---

## Step 03 - Getting Started with Java Modularization

In this step, we will explore an important feature introduced in **Java 9**—**Java modularization**.

Modularization brings several improvements, such as the ability to create modularized applications and the modularization of the JDK itself.

This step will provide an overview of these concepts, focusing on how modularization can make Java programs more efficient, organized, and easier to manage.

### Why Modularization?

Before **Java 9**, the **JDK** came bundled in a large jar file known as **RT.jar** (Runtime Jar).

Over time, as new features were added to Java, the size of RT.jar grew significantly, reaching over **60 MB** by Java 8.

This jar contained all the classes and libraries needed for Java programs, regardless of whether an application needed them or not.

- For example, if a program did not use any **SQL** features, it still had to carry around the **java.sql** library.

- **Java 9** solved this issue by breaking the JDK into **modules**.

### Modularizing the JDK

In **Java 9**, the JDK was divided into multiple **modules**.

A module is a self-contained unit of code that has a well-defined interface and clearly declared dependencies on other modules.

This means that when building an application, you no longer need the entire JDK; you can choose only the modules your application needs.

Let's explore this with an example.

### Listing Available Modules

To see the available modules in your current JDK version, use the following command:

```bash
java --list-modules
```

This command lists all the modules in your JDK. For example, you will see:

- **java.base**: The base module required for all Java programs.

- **java.logging**: Contains logging functionality.

- **java.sql**: Contains JDBC classes for database access.

- **java.xml**: Provides XML processing functionality.

You will also see **JDK-specific modules**, such as:

- **jdk.compiler**: For compiling Java code.

- **jdk.jshell**: For using the **JShell** tool.

The JDK is now divided into these modules, allowing you to include only what is needed for your specific application, making it lighter and more efficient.

### Modular Dependencies

Modules often have dependencies on each other. For example:

- **java.sql** depends on **java.base**.

- **java.logging** might also depend on **java.base**.

You can explore the dependencies of a module using this command:

```bash
java -Djava.sql
```

This command will show that **java.sql** requires **java.base** as a dependency.

### Exporting Packages

Modules can specify which of their **packages** are available to other modules.

For example, **java.sql** might export certain packages to make them accessible to other modules, but it can keep some internal packages hidden to improve encapsulation.

In the next step, we will explore how to modularize a sample Java application, comparing the traditional approach with the new modular approach enabled by Java 9.

---

## Step 04 - Java Modularization - 01 - Building Service and Consumer

In this step, we will build a simple Java application without worrying about modularization or splitting it into different JAR files.

Later, we will modularize it to demonstrate the benefits and differences modularization brings to the application.

Our goal is to set up a basic sorting utility and a consumer to use it.

### Step-by-Step Process

### 1. Creating the Java Project

1. **Create a New Java Project:**

   - Go to `File > New > Java Project`.

   - Name the project **modularization-1** and **combined** (everything combined in one place).

   - **Important:** Uncheck "Create module-info.java file" as we are not worrying about modularization yet.

   - Click **Finish**.

### 2. Building the Sorting Utility

Next, we will build a simple sorting utility that allows us to sort a list of names.

2. **Create a New Class:**

   - Class Name: **MySortingUtil**

   - Package: `com.in28minutes.sorting.util`

   - The class will contain a method `sort()` that accepts a list of names and returns it sorted (for now, we return the list as-is).

   ```java
   package com.in28minutes.sorting.util;

   import java.util.List;

   public class MySortingUtil {
       public List<String> sort(List<String> names) {
           // BubbleSort implementation goes here (for now, return names as-is)
           BubbleSort bubbleSort = new BubbleSort();
           return bubbleSort.sort(names);
       }
   }
   ```

3. **Create the BubbleSort Class:**

   - We will implement a simple **BubbleSort** class in a new package.

   ```java
   package com.in28minutes.sorting.algorithm;

   import java.util.List;

   public class BubbleSort {
       public List<String> sort(List<String> names) {
           // Return names as-is for now
           return names;
       }
   }
   ```

   - This class provides flexibility to switch to a different sorting algorithm later (e.g., QuickSort).

### 3. Creating the Consumer

Now, let's create a **consumer** class that will use the sorting utility.

4. **Create a New Class:**

   - Class Name: **MySortingUtilConsumer**

   - Package: `com.in28minutes.consumer`

   - This class contains the `main()` method and uses the sorting utility to sort a list of names.

   ```java
   package com.in28minutes.consumer;

   import com.in28minutes.sorting.util.MySortingUtil;
   import java.util.List;
   import java.util.logging.Logger;

   public class MySortingUtilConsumer {
       private static final Logger logger = Logger.getLogger(MySortingUtilConsumer.class.getName());

       public static void main(String[] args) {
           MySortingUtil util = new MySortingUtil();
           List<String> sorted = util.sort(List.of("Ranga", "Ravi", "Sathish", "Adam", "Eve"));
           logger.info(sorted.toString());
       }
   }
   ```

### 4. Logging the Output

- Instead of printing output using `System.out.println()`, we use **java.util.logging.Logger** to log the results of the sorted list.

```java
private static final Logger logger = Logger.getLogger(MySortingUtilConsumer.class.getName());
```

- The logger logs the sorted list:
  
```java
logger.info(sorted.toString());
```

### 5. Running the Application

- **Run the Application**:

  - Right-click the project and select `Run As > Java Application`.

  - The console should display the following output (since we haven't implemented actual sorting yet, the list is returned as-is):

    ```java
    Ranga, Ravi, Sathish, Adam, Eve
    ```

In this step, we built the basic structure of the sorting utility and its consumer.

The sorting utility uses a BubbleSort class, while the consumer sorts a list of names and logs the results.

In the following steps, we will split this project into different JARs and explore the modularization process.

---

## Step 05 - Java Modularization - 02 - Splitting Service and Consumer into JARs

In this step, we continue setting up our problem in preparation for Java modularization.

We'll demonstrate how to split a service and a consumer into separate JARs.

The challenge here is that without proper modularization, consumers can bypass intended APIs and directly access underlying implementation classes (like sorting algorithms), which may not be desirable. We will explore how to address this problem.

### Step-by-Step Process

### 1. Scenario Setup

Let’s assume we have two teams working on different parts of our project:

- **Team 1:** Implements the sorting algorithms and utility (service).

- **Team 2:** Implements the consumer that should use the sorting utility.

However, if both the service and consumer exist in the same project, a consumer developer might bypass the sorting utility and directly use the sorting algorithm (e.g., `BubbleSort`).

This is not the intended usage, as changes to the sorting utility might not propagate correctly.

### 2. Demonstrating the Problem

1. **Create a Direct Consumer:**

   - Copy the existing `MySortingUtilConsumer` class.

   - Create a new class called `DirectConsumer`, which uses the `BubbleSort` algorithm directly, bypassing the `MySortingUtil`.

   ```java
   package com.in28minutes.consumer;

   import com.in28minutes.sorting.algorithm.BubbleSort;
   import java.util.List;
   import java.util.logging.Logger;

   public class DirectConsumer {
       private static final Logger logger = Logger.getLogger(DirectConsumer.class.getName());

       public static void main(String[] args) {
           BubbleSort bubbleSort = new BubbleSort();
           List<String> sorted = bubbleSort.sort(List.of("Ranga", "Ravi", "Sathish", "Adam", "Eve"));
           logger.info(sorted.toString());
       }
   }
   ```

   - **Problem:** The `DirectConsumer` class can access and use `BubbleSort` directly instead of using `MySortingUtil`.
   
   - If the sorting algorithm is updated in `MySortingUtil`, the `DirectConsumer` class will not benefit from the change.

### Splitting into Separate JARs

To address this issue, we will now split the project into two separate JARs:

- **Service JAR:** Contains the sorting algorithms and utility.

- **Consumer JAR:** Contains the consumers that use the service JAR.

### 3. Creating the Service JAR Project

1. **Create a New Java Project:**

   - Go to `File > New > Java Project`.

   - Name the project **modularization-2-service-jar**.

   - **Important:** Uncheck "Create module-info.java" as we are not yet implementing modularization.

   - Click **Finish**.

2. **Move Sorting Classes to Service JAR:**

   - Move the `com.in28minutes.sorting.algorithm` and `com.in28minutes.sorting.util` packages to the **modularization-2-service-jar** project.

### 4. Creating the Consumer JAR Project

1. **Create a New Java Project:**

   - Go to `File > New > Java Project`.

   - Name the project **modularization-3-consumer-jar**.

   - Uncheck "Create module-info.java".

   - Click **Finish**.

2. **Move Consumer Classes to Consumer JAR:**

   - Move the `com.in28minutes.consumer` package to the **modularization-3-consumer-jar** project.

### 5. Configuring Dependencies Between JARs

To allow the **consumer JAR** to access the classes in the **service JAR**, we need to add the service JAR to the classpath of the consumer JAR:

1. **Add Service JAR to Consumer JAR's Classpath:**

   - Right-click the **modularization-3-consumer-jar** project and select **Properties**.

   - Go to **Java Build Path** > **Projects**.

   - Click **Add** and select **modularization-2-service-jar**.

   - Click **Apply and Close**.

   This will allow the consumer project to reference the sorting utility and algorithms from the service JAR.

### 6. Running the Application

Now that the projects are split into separate JARs, we can test them:

1. **Run MySortingUtilConsumer:**

   - Right-click **MySortingUtilConsumer** and select `Run As > Java Application`.

   - You should see the following output in the console:

   ```java
   [Ranga, Ravi, Sathish, Adam, Eve]
   ```

2. **Run DirectConsumer:**

   - Similarly, right-click **DirectConsumer** and select `Run As > Java Application`.

   - You will see the same output, showing that the direct use of `BubbleSort` still works.

In the next step, we will introduce modularization and see how it can help prevent the direct use of implementation classes like `BubbleSort`.

---

## Step 06 - Java Modularization - 03 - Splitting Service and Consumer into Modules

In this step, we take our service and consumer projects and split them into proper Java modules.

We’ll explore the benefits modularization brings in terms of encapsulation and access control.

Unlike the Classpath approach, Java modularization allows for fine-grained control over which parts of a module are exposed to other modules.

### Step-by-Step Process

### 1. Creating the Service Module

1. **Create a New Java Project:**

   - Go to `File > New > Java Project`.

   - Name the project **modularization-4-service-module**.

   - Ensure **Create module-info.java** is checked.

   - Click **Finish**.

2. **Define the Module Name:**

   - You will be prompted to name the module. Name it `com.in28minutes.service.provider`.

   - This creates a `module-info.java` file, which defines the module and its dependencies.

3. **Understanding the module-info.java File:**

   - The `module-info.java` file defines the module's metadata, such as the module's name and the packages it exports to other modules.

### 2. Creating the Consumer Module

1. **Create Another New Java Project:**

   - Go to `File > New > Java Project`.

   - Name the project **modularization-5-consumer-module**.

   - Ensure **Create module-info.java** is checked.

   - Click **Finish**.

2. **Define the Consumer Module Name:**

   - Name the module `com.in28minutes.consumer`.

   - This creates another `module-info.java` file for the consumer module.

### 3. Moving Code to the Modules

1. **Copy the Code for the Service:**

   - Copy the `com.in28minutes.sorting.algorithm` and `com.in28minutes.sorting.util` packages from the **modularization-2-service-jar** to **modularization-4-service-module**.

2. **Copy the Code for the Consumer:**

   - Copy the `com.in28minutes.consumer` package from **modularization-3-consumer-jar** to **modularization-5-consumer-module**.

### 4. Setting Up Dependencies Between Modules

1. **Fix Compilation Errors:**

   - After copying the code, you'll notice compilation errors in the consumer module because it depends on the service module.

2. **Declare the Service Module Dependency:**

   - In the consumer module’s `module-info.java` file, add the following line to specify the dependency:

     ```java
     requires com.in28minutes.service.provider;
     ```

   - This tells the consumer module that it requires the service provider module to function.

3. **Resolve the Module Dependency:**

   - Right-click on the **modularization-5-consumer-module** project and select **Properties**.

   - Go to **Java Build Path** > **Projects** > **Modulepath**.

   - Add **modularization-4-service-module** to the Modulepath.

   - Click **Apply and Close**.

   This resolves the compilation error in the consumer module as it now knows where to find the required service module.

### 5. Handling External Dependencies (Logging)

1. **Resolve Java Logging Dependency:**

   - The consumer module uses the `java.util.logging.Logger` class, which belongs to the `java.logging` module.

   - In the consumer module’s `module-info.java` file, add:

     ```java
     requires java.logging;
     ```

2. **Apply the Fix:**

   - This can be done manually, or you can use the Quick Fix feature in the IDE when it prompts you to add the required module.

### 6. Controlling Access with Exports

1. **Control Which Packages Are Exported:**

   - By default, the consumer module cannot access any classes from the service module unless they are explicitly exported.

   - In the **service module's** `module-info.java`, export only the `com.in28minutes.sorting.util` package:

     ```java
     exports com.in28minutes.sorting.util;
     ```

2. **Test the Changes:**

   - You will see that the `MySortingUtilConsumer` compiles and runs fine since it uses the exported `MySortingUtil` class.

   - However, `DirectConsumer` now fails to compile because it tries to access the `BubbleSort` class, which is in the `com.in28minutes.sorting.algorithm` package and is not exported.

### 7. Additional Control Over Access

1. **If You Want to Export More Packages:**

   - You can export the `com.in28minutes.sorting.algorithm` package as well by modifying the service module’s `module-info.java`:

     ```java
     exports com.in28minutes.sorting.algorithm;
     ```

   - This will allow both the `MySortingUtilConsumer` and `DirectConsumer` to compile and run successfully.

- Java modularization provides a much-needed level of encapsulation that is not available with the traditional Classpath approach.

- By explicitly declaring which packages are exported, we can control what parts of a module are accessible to other modules.

- This allows us to prevent unintended use of implementation classes (like `BubbleSort`) and ensure that consumers use the intended API (like `MySortingUtil`).

In the next steps, we will explore more features of modularization and continue refining our understanding of how modules can enhance code organization and maintenance.

---

## Step 07 - Java Modularization - 04 - A Quick Review

In this step, let's quickly review some key concepts about Java modularization that we’ve covered so far.

We'll revisit the module descriptor file (`module-info.java`), its components, and the benefits of modularization.

### Key Concepts of Java Modularization

### 1. **Module Descriptor (`module-info.java`)**

   - The `module-info.java` file defines metadata for the module.

   - It contains the essential declarations, such as:

     - **Requires**: Declares dependencies on other modules.

     - **Exports**: Specifies which packages are exposed to other modules.

### 2. **Requires Statement**

   - The `requires` keyword specifies which modules your module depends on to work.

   - Example:

     ```java
     requires java.logging;
     requires com.in28minutes.service.provider;
     ```

   - In the **consumer module**, we specified that it requires `java.logging` (for logging purposes) and `com.in28minutes.service.provider` (for accessing the service module).

### 3. **Transitive Requires**

   - You can use the `requires transitive` keyword to propagate module dependencies to consumers of your module.

   - Example:

     ```java
     requires transitive java.logging;
     ```

   - If a module declares a transitive dependency, then any module that depends on this module will automatically have access to the transitive dependency (`java.logging` in this case).

### 4. **Exports Statement**

   - The `exports` keyword is used to specify which packages can be accessed by other modules.

   - In the **service module**, we exported only the utility package:

     ```java
     exports com.in28minutes.sorting.util;
     ```

   - This ensures that only the utility package can be accessed by other modules, while keeping other packages (like the algorithm package) hidden.

### 5. **Opening Packages for Reflection**

   - Starting with Java 9, reflection access is controlled.

   - By default, reflection cannot access private types or members unless you explicitly allow it.

   - You can open specific packages to certain modules for reflection using the `opens` keyword:

     ```java
     opens com.in28minutes.sorting.util to specific.module;
     ```

   - This restricts reflection only to the specified package and module.

### Advantages of Java Modularization

### 1. **Compile-Time Checks**
   - Modularization provides **compile-time checks** for module dependencies.

   - If a required module is missing in the Modulepath, the compilation will fail, ensuring that all necessary modules are available.

### 2. **Improved Encapsulation**

   - Modules allow for **better encapsulation** of code.

   - Unlike the Classpath approach, you can control which parts of your module are visible to other modules using `exports`.

   - Only classes and packages explicitly exported are accessible by other modules, helping maintain tighter control over your module’s internal structure.

### 3. **Smaller Java Runtime**

   - With Java modularization, you can create a **smaller runtime** by choosing only the modules you need.

   - For example, if your program requires logging, you explicitly include `java.logging`. If not, it is excluded, leading to a more lightweight runtime.

In this quick review, we looked at how the `module-info.java` file helps define dependencies and control access within modules.

We also covered the benefits of modularization, such as compile-time checks, improved encapsulation, and the ability to create a smaller Java runtime.

---

## Step 08 - Exploring New Java API - List, Set, and Map - copyOf Methods

In this step, we will explore new methods introduced in Java 10 that allow us to create unmodifiable collections from existing ones.

These methods—`copyOf`—are available in the `List`, `Set`, and `Map` interfaces.

We'll see how these methods can help you create immutable collections easily, and when and why to use them.

### Setting Up the Project

1. **Create a New Java Project:**

   - Project Name: `JavaNewAPIFeatures`

   - Make sure to select the latest execution environment.

   - Uncheck the option to create `module-info.java`.

2. **Create a New Class:**

   - Class Name: `CopyOfAPI`

   - Package: `com.in28minutes.api.a`

   - Add a `main` method to this class.

### The `copyOf` Methods in Java 10+

### What is `copyOf`?

The `copyOf` method is a utility added in Java 10 that allows you to create an **unmodifiable collection** from an existing collection. It's available for:

- `List`

- `Set`

- `Map`

**Key Features:**

- The `copyOf` method creates an **unmodifiable** version of the collection passed to it.

- The collection must not contain `null` values.

- If the collection is already unmodifiable, `copyOf` will return the same collection, avoiding unnecessary copying.

### Example - Creating Unmodifiable Collections

### Using `List.copyOf`

1. **Create a Modifiable List:**

   ```java
   List<String> names = new ArrayList<>();
   names.add("Ranga");
   names.add("Ravi");
   names.add("John");
   ```

2. **Pass List to a Method that Modifies It:**

   ```java
   public static void doNotChangeNames(List<String> names) {
       names.add("Adam"); // Trying to modify the list
   }
   ```

3. **Without `copyOf` Method:**

   If we pass the list `names` directly, the method `doNotChangeNames` can modify it, which may not be desirable:

   ```java
   doNotChangeNames(names); // This will modify the list
   System.out.println(names); // Output: [Ranga, Ravi, John, Adam]
   ```

4. **Using `List.copyOf` for Immutability:**

   To prevent changes to the list, we use `List.copyOf` to create an immutable copy:

   ```java
   List<String> copyOfNames = List.copyOf(names);
   doNotChangeNames(copyOfNames); // This will throw an exception
   ```

   - Output:

     ```
     Exception in thread "main" java.lang.UnsupportedOperationException: Immutable collection
     ```

### The `copyOf` Methods for `Set` and `Map`

- **`Set.copyOf`** works the same way as `List.copyOf`, creating an unmodifiable `Set`.

- **`Map.copyOf`** allows you to create an immutable `Map` from an existing one.

### Benefits of `copyOf`

1. **Immutability:**
   - Ensures that no one can modify a collection after it is passed around, preserving data integrity.
   
2. **Efficiency:**
   - If the collection is already immutable, `copyOf` returns the same collection without creating a new copy.

In this step, we explored the `copyOf` methods introduced in Java 10 for `List`, `Set`, and `Map`.

These methods allow you to create immutable collections from modifiable ones, providing a simple way to enforce immutability in your code.

This is especially useful when you want to protect collections from being modified after passing them to external methods.

---

## Step 09 - Exploring New Java API - Files - `readString` and `writeString` Methods

In this step, we'll explore two important file-handling methods introduced in **Java 11**: `Files.readString` and `Files.writeString`. 

These methods simplify the process of reading and writing string data to and from files.

We'll go through examples of reading a file into a string, modifying its content, and writing the modified content back to a new file.

### Setting Up the Project

1. **Create a New Class:**

   - Class Name: `FileReadWriteRunner`

   - Package: `com.in28minutes.api.b`

   - Add a `main` method.

2. **Create a Resource Folder and File:**

   - **Folder:** `resources`

   - **File:** `sample.txt` (with content: "sample line 2 line 3")

### Using `Files.readString` to Read a File

1. **Create a Path Object:**

   ```java
   Path path = Paths.get("./resources/sample.txt");
   ```

2. **Use `Files.readString` to Read the File Content:**

   ```java
   String fileContent = Files.readString(path);
   ```

3. **Handle Exceptions:**

   Since file operations can throw an `IOException`, make sure to either catch the exception or add a `throws IOException` to your `main` method.

4. **Print File Content:**

   ```java
   System.out.println(fileContent);
   ```

5. **Output:**

   ```
   sample
   line two
   line three
   ```

### Modifying and Writing Content Using `Files.writeString`

1. **Modify the Content:**

   Let's replace the word "line" with "lines":

   ```java
   String newFileContent = fileContent.replace("line", "lines");
   ```

2. **Write the Modified Content to a New File:**

   ```java
   Path newFilePath = Paths.get("./resources/sample-new.txt");
   Files.writeString(newFilePath, newFileContent);
   ```

3. **Check the New File:**

   After running the program, a new file `sample-new.txt` should be created with the updated content:

   ```
   sample
   lines two
   lines three
   ```

### Key Points about `readString` and `writeString`

1. **`Files.readString`:**

   - Introduced in **Java 11**.

   - Allows reading the entire content of a file as a string.

   - Uses `UTF-8` encoding by default but can accept other encodings as an optional parameter.

2. **`Files.writeString`:**

   - Also introduced in **Java 11**.

   - Makes writing a string to a file easy by specifying the target `Path` and the content string.

   - Can overwrite an existing file or create a new one if it doesn't exist.

In this step, we explored two utility methods introduced in **JDK 11**: `Files.readString` and `Files.writeString`.

These methods simplify file operations by allowing us to easily read from and write strings to files.

They reduce boilerplate code and provide more straightforward handling of file I/O in Java.

---

## Step 10 - Exploring New Java API - `Predicate.not` Method

In this step, we will explore the `Predicate.not` method, introduced in **JDK 11**.

This method allows you to easily negate a predicate, making your functional programming code more readable and concise.

We will also compare this new method with the traditional approach of using the `negate` method.

### Setting Up the Example

1. **Create a New Class:**

   - Class Name: `PredicateNotRunner`

   - Package: `com.in28minutes.api.c`

   - Add a `main` method.

2. **Create a List of Integers:**

   ```java
   List<Integer> numbers = List.of(3, 4, 7, 10, 88, 99);
   ```

3. **Define a Predicate for Even Numbers:**

   ```java
   Predicate<Integer> evenNumberPredicate = number -> number % 2 == 0;
   ```

4. **Filter Even Numbers Using the Predicate:**

   ```java
   numbers.stream()
          .filter(evenNumberPredicate)
          .forEach(System.out::println);
   ```

   This will print the even numbers from the list.

### Negating the Predicate

1. **Using the `negate()` Method:**

   - To filter out the odd numbers, you can negate the predicate:

     ```java
     numbers.stream()
            .filter(evenNumberPredicate.negate())
            .forEach(System.out::println);
     ```

   - Output: 

     ```
     3
     7
     99
     ```

### Using `Predicate.not` Method

1. **Define a Method Reference for Even Numbers:**

   ```java
   public static boolean isEven(Integer number) {
       return number % 2 == 0;
   }
   ```

2. **Filter Using a Method Reference:**

   ```java
   numbers.stream()
          .filter(PredicateNotRunner::isEven)
          .forEach(System.out::println);
   ```

   This will print the even numbers: `4, 10, 88`.

3. **Negating the Method Reference with `Predicate.not`:**

   - If you want to filter the odd numbers using a method reference, use the `Predicate.not` method:

     ```java
     numbers.stream()
            .filter(Predicate.not(PredicateNotRunner::isEven))
            .forEach(System.out::println);
     ```

   - Output:

     ```
     3
     7
     99
     ```

### Key Points about `Predicate.not`

1. **`Predicate.not`:**

   - Introduced in **Java 11**.

   - Simplifies the process of negating predicates, especially useful when working with method references.

   - More readable and concise compared to the traditional `negate()` method.

2. **Usage with Method References:**

   - The `Predicate.not` method is particularly handy when you are using method references and need to negate the predicate.

In this step, we explored the **`Predicate.not`** method introduced in **JDK 11**.

This method helps negate predicates in a more readable way, especially when working with method references.

It enhances the functional programming capabilities in Java by making it easier to work with conditions and filters.

---

## Step 11 - Exploring New Java API - String Utility Methods

In this step, we will explore several new **String API** methods introduced in recent versions of Java.

These methods improve the way you handle strings and simplify common tasks such as checking for blank strings, trimming whitespace, splitting lines, transforming strings, and formatting them.

We'll also take a look at the **helpful NullPointerException** messages introduced in JDK 14, which add more context to null pointer exceptions, making debugging easier.

### 1. Checking for Blank Strings

### **`isBlank()`** Method (Introduced in Java 11)

- **Purpose**: Checks whether a string is blank (empty or contains only whitespace).
  
```java
String str = " ";
System.out.println(str.isBlank()); // true
```

The `isBlank()` method will return `true` if the string is either empty or only contains white space characters.

### 2. Trimming Strings

### **`strip()`**, **`stripLeading()`**, and **`stripTrailing()`** Methods (Introduced in Java 11)

- **Purpose**: Removes leading and/or trailing whitespaces.
  
```java
String str = "   left   right   ";
System.out.println(str.strip());         // "left   right"
System.out.println(str.stripLeading());  // "left   right   "
System.out.println(str.stripTrailing()); // "   left   right"
```

- **`strip()`** removes leading and trailing whitespaces.

- **`stripLeading()`** removes only leading whitespaces.

- **`stripTrailing()`** removes only trailing whitespaces.

### 3. Breaking String into Lines

### **`lines()`** Method (Introduced in Java 11)

- **Purpose**: Breaks a string into multiple lines (returns a `Stream<String>`).
  
```java
String multiLineString = "Line1\nLine2\nLine3";
multiLineString.lines().forEach(System.out::println);
```

This will split the string by line terminators and print each line separately.

### 4. String Transformation

### **`transform()`** Method (Introduced in Java 12)

- **Purpose**: Allows transforming a string by passing it to a function (lambda expression).

```java
String str = "UPPERCASE";
String result = str.transform(s -> s.substring(2));
System.out.println(result); // "PERCASE"
```

The `transform()` method allows you to apply any function to the string, enabling flexible string manipulations.

### 5. Formatting Strings

### **`formatted()`** Method (Introduced in Java 13)

- **Purpose**: Formats a string using placeholders, similar to `String.format()`.

```java
String formattedStr = "My name is %s and I am %d years old.".formatted("Ranga", 25);
System.out.println(formattedStr); 

// Output: "My name is Ranga and I am 25 years old."
```

The `formatted()` method is an alternative to `String.format()` and simplifies formatting.

### 6. Helpful NullPointerException Messages

### **Enhanced NullPointerException** (Introduced in Java 14)

- **Purpose**: Provides more context in NullPointerException messages, making it easier to debug.

```java
String str = null;
str.isBlank(); // This will throw a NullPointerException with detailed message
```

- **Error Message Example**:
  
  ```
  Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.isBlank()" because "str" is null
  ```

With Java 14+, this enhanced message will specify **what exactly** is null, providing more detailed context.

These methods simplify common string manipulation tasks, making your code more concise and readable.

We also saw how debugging has been made easier with enhanced null pointer exception messages.

---

## Step 12 - Exploring Java New Features - Local Variable Type Inference

In this step, we will explore an important feature introduced in **Java 10**, called **local variable type inference**.

This feature allows the **Java compiler to infer the type of local variables**, reducing the need to explicitly declare types, especially when dealing with complex type declarations.

We'll see how this feature simplifies variable declaration while maintaining type safety. The **`var`** keyword plays a key role in this feature.

### 1. What is Local Variable Type Inference?

Local variable type inference allows the compiler to infer the type of a local variable based on the initializer (the expression on the right-hand side of the assignment).

For example:

```java
// Without type inference:
List<String> names = List.of("John", "Adam");

// With type inference (using var):
var names = List.of("John", "Adam");
```

Here, **`var`** tells the compiler to infer the type from the assigned value (`List<String>`). This reduces boilerplate code and can be especially useful when dealing with complex types.

### 2. Example of Type Inference

Let's take a more complex example of nested lists:

```java
// List of List of Strings without type inference:
List<List<String>> namesList = List.of(names1, names2);

// With type inference:
var namesList = List.of(names1, names2);
```

Even though the type (`List<List<String>>`) is complex, **`var`** allows the compiler to infer the correct type, making the code cleaner and easier to read.

### 3. Type Safety with `var`

Even though you use **`var`**, type safety is not compromised. The compiler still checks the types at **compile time**.

For example:

```java
var names = List.of("John", "Adam");

// You can still perform valid operations on the list:
names.stream().forEach(System.out::println);

// If you attempt an invalid operation, you'll get a compile-time error:
names.streamOne(); // Error: streamOne() is not a valid method for List<String>
```

The type is inferred based on the right-hand side, and any invalid operations will result in a compile-time error, ensuring type safety.

### 4. Using `var` in Loops

You can also use **`var`** in loops, simplifying variable declaration within loop constructs.

### Example:

```java
// Standard for-loop
for (var i = 0; i < 10; i++) {
    System.out.println(i);
}

// Enhanced for-loop with type inference:
for (var name : names) {
    System.out.println(name);
}
```

In both examples, **`var`** allows the compiler to infer the type of the loop variables.

### 5. Restrictions on `var`

#### 1. **Cannot be assigned `null`**:

You cannot assign `null` to a variable declared with **`var`**, because the compiler cannot infer the type from `null`.

```java
var str = null; // Compile-time error: Cannot infer type for variable initialized to null
```

#### 2. **Not a keyword**:

**`var`** is not a keyword in Java, which means you can still use **`var`** as an identifier for variable or method names (although this is discouraged).

```java
var var = "This is valid, but not recommended.";
System.out.println(var);
```

### 6. Use `var` Wisely

While **`var`** can simplify code, using it inappropriately can make code harder to understand.

For example, if variable names are not descriptive enough, it becomes unclear what the inferred type is.

#### Bad Example:

```java
var x = List.of("John", "Adam"); // Not clear what `x` is
```

#### Good Example:

```java
var namesList = List.of("John", "Adam"); // Clearer and descriptive variable name
```

### 7. Improving Readability with `var`

Type inference is particularly helpful in improving readability in situations where you have **chained method calls** or **complex expressions**.

#### Example:

```java
var filteredNames = List.of("Ranga", "Ravi", "Adam")
                       .stream()
                       .filter(name -> name.length() < 5)
                       .collect(Collectors.toList());

filteredNames.forEach(System.out::println);
```

In this example, **`var`** improves readability by letting the developer focus on the logic rather than the exact type of the variable.

### 8. `var` in Final Variables

You can also declare **final** variables using **`var`**, but by default, **`var`** variables are **not final**. To make a **`var`** variable immutable, you need to explicitly declare it as **final**.

```java
final var immutableNames = List.of("John", "Adam");
```

In this step, we explored the **local variable type inference** feature introduced in Java 10, which allows the use of the **`var`** keyword for variable declarations.

---

## Step 13 - Exploring Java New Features - Switch Expression

In this step, we explore **Switch Expressions**, a feature introduced in **JDK 14**.

While Java has long supported the traditional **Switch Statement**, the **Switch Expression** offers a more concise and flexible syntax that enhances readability and eliminates common issues such as fall-through behavior.

**Switch Expression** was initially released as a preview feature in **JDK 12** and **JDK 13**, and it was finalized as a standard feature in **JDK 14**.

### 1. Traditional Switch Statement

Let's first revisit a traditional **Switch Statement**, where we map an integer (0-6) to the corresponding day of the week.

#### Example:

```java
public static String findDayOfWeek(int day) {
    String dayOfWeek = "";
    
    switch (day) {
        case 0:
            dayOfWeek = "Sunday";
            break;
        case 1:
            dayOfWeek = "Monday";
            break;
        case 2:
            dayOfWeek = "Tuesday";
            break;
        case 3:
            dayOfWeek = "Wednesday";
            break;
        case 4:
            dayOfWeek = "Thursday";
            break;
        case 5:
            dayOfWeek = "Friday";
            break;
        case 6:
            dayOfWeek = "Saturday";
            break;
        default:
            throw new IllegalArgumentException("Invalid day: " + day);
    }
    
    return dayOfWeek;
}
```

### Key Observations:

- **Break statements** are necessary to prevent **fall-through** behavior.

- The code involves a lot of boilerplate with repetitive assignments.

- If we forget a break, it can lead to subtle bugs where one case flows into another.

### 2. Simplifying with Switch Expressions

With **Switch Expressions**, we can eliminate these issues and write cleaner, more concise code.

#### Example:

```java
public static String findDayOfWeekWithSwitchExpression(int day) {
    return switch (day) {
        case 0 -> "Sunday";
        case 1 -> "Monday";
        case 2 -> "Tuesday";
        case 3 -> "Wednesday";
        case 4 -> "Thursday";
        case 5 -> "Friday";
        case 6 -> "Saturday";
        default -> throw new IllegalArgumentException("Invalid day: " + day);
    };
}
```

### Key Benefits:

- **No break statements**: Each case returns a value using the `->` (lambda-style) syntax.

- **No fall-through**: Each case is evaluated independently.

- The **Switch Expression** is concise and avoids unnecessary local variables.

- **Returns a value** directly, making the switch itself an expression, not just a statement.

### 3. Handling Complex Logic with Switch Expressions

Sometimes, the logic inside a case might be more complex, involving multiple statements. In this case, we can use **braces** to group the logic and return the final value using the **`yield`** keyword.

### Example:

```java
public static String findDayWithComplexLogic(int day) {
    return switch (day) {
        case 0 -> {
            System.out.println("Executing complex logic for Sunday");
            yield "Sunday";
        }
        case 1 -> "Monday";
        case 2 -> "Tuesday";
        default -> throw new IllegalArgumentException("Invalid day: " + day);
    };
}
```

### Key Features:

- When using **braces** to handle complex logic, use **`yield`** to return the value.

- No need for a **semicolon** after the switch expression in cases where braces are used.

### 4. No Fall-Through in Switch Expressions

One of the critical advantages of **Switch Expressions** is that **fall-through behavior is completely eliminated**. Each case is **mutually exclusive**, and there is no need for **break** statements.

In the example below, there is no risk that evaluating one case will inadvertently flow into another:

```java
return switch (day) {
    case 0 -> "Sunday";  // Directly returns "Sunday"
    case 1 -> "Monday";  // Directly returns "Monday"
    // No risk of fall-through
};
```

- This makes the code more predictable and prevents common errors associated with forgetting to include `break` statements.

Switch Expressions provide a **simplified**, **concise**, and **safe** way to work with conditional logic in Java.

By eliminating fall-through behavior and allowing **return values** directly from the switch, it makes code more readable and less error-prone.

In this step, we explored how to transform traditional switch statements into switch expressions and looked at how **`yield`** can be used for more complex logic within switch cases.

---

## Step 14 - Exploring Java New Features - Text Blocks

In this step, we explore **Text Blocks**, a feature introduced in **JDK 15**. Text blocks provide a simpler way to work with multi-line strings in Java, improving readability and maintainability.

Before text blocks, creating complex multi-line strings often involved using escape sequences, making the code harder to read and maintain. Text blocks simplify this by allowing multi-line strings to be written more naturally.

Text blocks were introduced as a **preview feature** in **JDK 13** and **JDK 14**, and were made a standard feature in **JDK 15**.

### 1. The Problem with Traditional String Handling

When working with traditional string literals, especially multi-line strings or strings with special characters, the code can become cluttered with escape sequences (`\n`, `\"`, etc.).

#### Example (Without Text Blocks):

```java
System.out.println("\"First Line\"\nSecond Line\nThird Line");
```

This approach is hard to read, as it uses escape sequences for quotes and newlines.

### 2. Introduction to Text Blocks

**Text Blocks** simplify working with multi-line strings. They allow you to define a string using three double quotes (`"""`), making it easier to write and read large blocks of text, such as JSON, HTML, or SQL.

#### Example (With Text Blocks):

```java
System.out.println("""
        "name": "John",
         age: 30,
        city: "New York"""
      );
```

#### Key Benefits:

- No need for escape sequences for quotes.

- Multi-line strings are easier to read and maintain.

- Leading and trailing spaces are automatically handled.

### 3. Creating Text Blocks

Let's create a text block to see how it works in practice.

```java
String textBlock = """
    Line 1
    Line 2
    Line 3
    """;
```

#### Key Points:

- Text blocks start and end with three double quotes (`"""`).

- The content inside the block is treated as-is, including newlines.

- You can use `System.out.print` to print the content of the text block:
  
```java
System.out.print(textBlock);
```

This will output:

```java
Line 1
Line 2
Line 3
```

### Removing Trailing Newlines:

If you don’t want a newline at the end, place the closing quotes (`"""`) immediately after the last line:

```java
String textBlock = """
    Line 1
    Line 2
    Line 3""";
```

This removes the extra newline at the end.

### 4. Handling Indentation

Text blocks automatically handle indentation. The first non-whitespace character on each line is treated as the left margin, and any whitespace to the left of this margin is ignored for all lines.

For example:

```java
String indentedBlock = """
        Line 1
        Line 2
        Line 3
    """;
```

Even though each line is indented, the printed output will not contain this indentation.

### Custom Line Indentation:

If you want specific lines to be indented, simply add spaces or tabs to those lines:

```java
String indentedBlock = """
    Line 1
        Line 2 (indented)
    Line 3
    """;
```

Output:

```java
Line 1
    Line 2 (indented)
Line 3
```

### 5. Double Quotes Inside Text Blocks

Text blocks also allow you to use double quotes without escaping them. For example:

```java
String quoteExample = """
    He said, "Hello!"
    """;
```

There is no need to escape the quotes.

### 6. Text Blocks and String Operations

You can use text blocks wherever you would use normal strings. This includes performing operations such as string formatting.

### Example (Using `formatted` method):

```java
String template = """
    Name: %s
    Age: %d
    """;
String formatted = template.formatted("John", 25);
System.out.print(formatted);
```

This will output:

```java
Name: John
Age: 25
```

#### Example (Combining with String Methods):

You can also chain other string methods, such as `replace` or `toUpperCase`:

```java
String block = """
    Hello, World!
    """.toUpperCase();
```

### 7. Restrictions and Best Practices

- **Line Break Requirement**: After the opening three quotes (`"""`), there must be a line break. You cannot define a text block all on one line.
  
    **Invalid Example**:
    ```java
    String invalid = """Hello""";
    ```

    **Valid Example**:
    ```java
    String valid = """
    Hello
    """;
    ```

- **Automatic Alignment**: If there is consistent leading whitespace in all lines, it is automatically removed.

- **Trailing Whitespace**: Any trailing whitespace is also stripped. If you want to preserve trailing whitespace, it must be explicitly added.

#### Best Practice:

```java
String block = """
    Line 1
    Line 2
    Line 3
    """;
```

This formatting makes it clear that the string is a multi-line block.

### 8. Text Blocks for Templates

Text blocks can be particularly useful for creating templates such as HTML or SQL queries.

### Example (HTML Template):

```java
String htmlTemplate = """
    <html>
        <head>
            <title>%s</title>
        </head>
        <body>
            <h1>%s</h1>
        </body>
    </html>
    """.formatted("My Page", "Welcome to My Page!");
```

This makes it easy to create dynamic content by formatting the template with actual values.

In this step, we explored how to create and work with text blocks, including handling formatting, indentation, and embedding values using `formatted`.

---

## Step 15 - Exploring Java New Features - Records

In this step, we explore **records**, a feature introduced in **JDK 14** as a preview and made a standard feature in **JDK 16**.

Records are a special kind of Java class that eliminate the need for boilerplate code. They automatically generate:

- **Constructors**

- **Public accessor methods** (getters)

- **equals()**

- **hashCode()**

- **toString()**

Records are primarily used for classes that are simple data carriers, also known as **data transfer objects (DTOs)** or **POJOs**.

### 1. Traditional Java Class: The Problem

In traditional Java programming, creating a simple class with member variables often requires a lot of repetitive code. For example, a typical `Employee` class might look like this:

```java
public class Employee {
    private String name;
    private String email;
    private String phoneNumber;

    public Employee(String name, String email, String phoneNumber) {
        this.name = name;
        this.email = email;
        this.phoneNumber = phoneNumber;
    }

    public String getName() { return name; }
    public String getEmail() { return email; }
    public String getPhoneNumber() { return phoneNumber; }

    @Override
    public String toString() {
        return "Employee{name='" + name + "', email='" + email + "', phoneNumber='" + phoneNumber + "'}";
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (!(o instanceof Employee)) return false;
        Employee employee = (Employee) o;
        return name.equals(employee.name) &&
                email.equals(employee.email) &&
                phoneNumber.equals(employee.phoneNumber);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, email, phoneNumber);
    }
}
```

This class defines fields, constructors, getters, `toString()`, `equals()`, and `hashCode()` methods. For each new class, we repeat this boilerplate code.

### 2. Introducing Records

**Records** eliminate this boilerplate by automatically generating constructors, getters, `toString()`, `equals()`, and `hashCode()`.

#### Example:

```java
public record Person(String name, String email, String phoneNumber) { }
```

This single line of code defines a class that:

- Has three fields: `name`, `email`, and `phoneNumber`

- Automatically provides:

  - A constructor

  - Getters (`name()`, `email()`, and `phoneNumber()`)
  
  - `toString()`, `equals()`, and `hashCode()`

#### Creating a Record Instance:

```java
Person person = new Person("Ranga", "ranga@in28minutes.com", "1234567890");
System.out.println(person);
```

The output:
```
Person[name=Ranga, email=ranga@in28minutes.com, phoneNumber=1234567890]
```

### 3. Accessor Methods

Records automatically generate **public accessor methods** for each field. These methods are named after the field.

#### Example:

```java
System.out.println(person.name());         // Prints: Ranga
System.out.println(person.email());        // Prints: ranga@in28minutes.com
System.out.println(person.phoneNumber());  // Prints: 1234567890
```

### 4. Equality and Hashcode

Records automatically implement `equals()` and `hashCode()` based on all their fields. Two records are considered equal if all their fields are equal.

### Example:

```java
Person person1 = new Person("Ranga", "ranga@in28minutes.com", "1234567890");
Person person2 = new Person("Ranga", "ranga@in28minutes.com", "1234567890");

System.out.println(person1.equals(person2)); // Prints: true
```

### 5. Custom Constructors and Validations

You can also define custom constructors and validations inside records.

#### Example (Custom Constructor with Validation):

```java
public record Person(String name, String email, String phoneNumber) {
    public Person {
        if (name == null || name.isEmpty()) {
            throw new IllegalArgumentException("Name cannot be null or empty");
        }
    }
}
```

Here, the constructor checks that the `name` is not null or empty. If the validation fails, an `IllegalArgumentException` is thrown.

### Compact Constructors:
Java also allows **compact constructors** for records, where you don’t need to explicitly assign fields to `this`:

```java
public record Person(String name, String email, String phoneNumber) {
    public Person {
        if (name == null || name.isEmpty()) {
            throw new IllegalArgumentException("Name cannot be null or empty");
        }
    }
}
```

This compact constructor automatically assigns `name`, `email`, and `phoneNumber` without requiring explicit assignments like `this.name = name`.

### 6. Restrictions in Records

While records simplify a lot of work, they come with certain restrictions:

- **No additional instance variables**: You cannot add additional fields other than the ones defined in the record header.

- **No mutable fields**: Fields in records are final, which means records are immutable by default.

- **Custom methods**: You can add additional methods, but you cannot add mutable fields or instance initializers.

#### Allowed Example:

```java
public record Person(String name, String email, String phoneNumber) {
    public String uppercaseName() {
        return name.toUpperCase();
    }
}
```

#### Not Allowed Example:

```java
public record Person(String name, String email, String phoneNumber) {
    private int age; // Not allowed
}
```

### 7. Static Fields and Methods in Records

You **can** add static fields and methods to records.

### Example:
```java
public record Person(String name, String email, String phoneNumber) {
    public static String species = "Homo sapiens";

    public static String getSpecies() {
        return species;
    }
}
```

### 8. Benefits of Records

- **Less boilerplate**: Records automatically generate much of the repetitive code, making the class definition cleaner and easier to read.

- **Immutable by default**: Records are inherently immutable, making them safe for concurrent programming.

- **Well-defined equality**: The `equals()` and `hashCode()` methods are based on the fields, which makes comparisons straightforward.

In this step, we explored **records**, a feature introduced in **JDK 16** that simplifies class creation by eliminating boilerplate code for constructors, getters, `toString()`, `equals()`, and `hashCode()`. 

---
