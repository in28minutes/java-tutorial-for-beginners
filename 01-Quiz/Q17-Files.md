## File Operations Quiz

**Question 1:**

Which package provides utility classes and interfaces to interact with the native file system in Java?

A) `java.io`
B) `java.nio.file`
C) `java.util`
D) `java.lang`

**Question 2:**

What does the following code do?

```java
Files.list(Paths.get(".")).forEach(System.out::println);
```

A) Lists all the files and directories in the current directory
B) Prints the contents of a specific file
C) Lists the contents of a specified directory
D) Throws an exception

**Question 3:**

What does the `Paths.get()` method return?

A) The absolute path of a file or directory
B) The name of a file or directory
C) The path of a file or directory relative to the current directory
D) The parent directory of a file or directory

**Question 4:**

What is the difference between `Files.list()` and `Files.walk()`?

A) `Files.list()` lists only regular files, while `Files.walk()` recursively traverses directories
B) `Files.list()` traverses directories up to a specified depth, while `Files.walk()` lists all files and directories
C) `Files.list()` is used to list files, while `Files.walk()` is used to walk through directories
D) There is no difference, they can be used interchangeably

**Question 5:**

What does the following code do?

```java
Files.walk(currentDirectory, 4).filter(path -> String.valueOf(path).contains(".java")).forEach(System.out::println);
```

A) Lists all files and directories up to a depth of 4, filtering only Java files
B) Lists all Java files in the current directory and its subdirectories up to a depth of 4
C) Throws an exception
D) Filters all files and directories with names containing ".java"

**Question 6:**

What is the purpose of the `Files.readAllLines()` method?

A) It reads the content of a file as a single string
B) It reads the content of a file line by line and returns a list of strings
C) It reads the content of a file as bytes
D) It reads the content of a file character by character

**Question 7:**

What does the following code do?

```java
Files.lines(pathFileToRead).map(String::toLowerCase).forEach(System.out::println);
```

A) Converts the content of a file to lowercase and prints it
B) Prints the content of a file as lowercase characters
C) Throws an exception
D) Converts the content of a file to lowercase and returns it as a list of strings

**Question 8:**

What is the purpose of the `Files.write()` method?

A) It reads the content of a file
B) It appends new content to a file
C) It writes data to a file
D) It deletes a file

**Question 9:**

What does the following code do?

```java
List<String> list = List.of("Apple", "Boy", "Cat", "Dog", "Elephant");
Files.write(pathFileToWrite, list);
```

A) Creates a new file with the specified list of strings as its content
B) Writes the list of strings to an existing file
C) Deletes the file specified by `pathFileToWrite`
D) Prints the list of strings to the console

**Question 10:**

Which class provides methods for reading and writing files in Java?

A) `Path`
B) `File`
C) `Files`
D) `Scanner`
