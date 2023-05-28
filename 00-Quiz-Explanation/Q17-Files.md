**Question 89: Which package provides utility classes and interfaces to interact with the native file system in Java?**
- A) java.io
  - `Incorrect: While the java.io package does provide classes for file handling, it does not directly interact with the native file system.`
- B) java.nio.file
  - `Correct: The java.nio.file package provides classes that offer a comprehensive model for file I/O and for accessing the default file system.`
- C) java.util
  - `Incorrect: The java.util package does not provide classes for file handling. It mainly contains the collections framework, date and time facilities, random-number generator, and other utility classes.`
- D) java.lang
  - `Incorrect: The java.lang package does not provide classes for file handling. It provides classes that are fundamental to the design of the Java programming language.`

**Question 90: What does the following code do?**
```java
Files.list(Paths.get(".")).forEach(System.out::println);
```
- A) Lists all the files and directories in the current directory
  - `Correct: This line of code uses the java.nio.file API to list all the files and directories in the current directory and print them to the console.`
- B) Prints the contents of a specific file
  - `Incorrect: This code does not print the contents of any file, it prints the paths of the files and directories in the current directory.`
- C) Lists the contents of a specified directory
  - `Incorrect: The specified directory is ".", which means the current directory.`
- D) Throws an exception
  - `Incorrect: This code won't necessarily throw an exception unless there's a problem accessing the file system.`

**Question 91: What does the Paths.get() method return?**
- A) The absolute path of a file or directory
  - `Incorrect: Paths.get() can return either a relative path or an absolute path, depending on the argument passed to it.`
- B) The name of a file or directory
  - `Incorrect: Paths.get() returns a Path object, which represents a path in the file system, not just the name of a file or directory.`
- C) The path of a file or directory relative to the current directory
  - `Incorrect: Paths.get() can return either a relative path or an absolute path, depending on the argument passed to it.`
- D) The parent directory of a file or directory
  - `Incorrect: Paths.get() returns a Path object, which represents a path in the file system. It does not specifically return the parent directory of a file or directory.`

**Question 92: What is the difference between Files.list() and Files.walk()?**
- A) Files.list() lists only regular files, while Files.walk() recursively traverses directories
  - `Correct: Files.list() lists all the files and directories in a directory but does not recurse into subdirectories. Files.walk() does the same, but it also recursively traverses directories.`
- B) Files.list() traverses directories up to a specified depth, while Files.walk() lists all files and directories
  - `Incorrect: Files.list() does not traverse directories at all, it only lists the files and directories in the specified directory. Files.walk() is the method that can traverse directories up to a specified depth.`
- C) Files.list() is used to list files, while Files.walk() is used to walk through directories
  - `Incorrect: Both Files.list() and Files.walk() can be used to list files and directories. The difference is that Files.walk() also recursively traverses directories.`
- D) There is no difference, they

 can be used interchangeably
  - `Incorrect: There is a significant difference between Files.list() and Files.walk(), as explained in the answer to option (A).`

**Question 93: What does the following code do?**
```java
Files.walk(currentDirectory, 4).filter(path -> String.valueOf(path).contains(".java")).forEach(System.out::println);
```
- A) Lists all files and directories up to a depth of 4, filtering only Java files
  - `Incorrect: This code does not list all files and directories up to a depth of 4. It only lists those files that have ".java" in their path.`
- B) Lists all Java files in the current directory and its subdirectories up to a depth of 4
  - `Correct: This code lists all files in the current directory and its subdirectories up to a depth of 4, but only those that have ".java" in their path are printed to the console.`
- C) Throws an exception
  - `Incorrect: This code won't necessarily throw an exception unless there's a problem accessing the file system.`
- D) Filters all files and directories with names containing ".java"
  - `Incorrect: The code filters and lists files with names containing ".java" only up to a depth of 4 in the directory hierarchy.`

**Question 94: What is the purpose of the Files.readAllLines() method?**
- A) It reads the content of a file as a single string
  - `Incorrect: Files.readAllLines() reads all lines from a file and returns a List of strings, with each string being one line in the file.`
- B) It reads the content of a file line by line and returns a list of strings
  - `Correct: This method reads all lines from a file and returns a List of strings, with each string being one line in the file.`
- C) It reads the content of a file as bytes
  - `Incorrect: This method reads the content of a file as lines of text, not as bytes.`
- D) It reads the content of a file character by character
  - `Incorrect: This method reads the content of a file as lines of text, not character by character.`

**Question 95: What does the following code do?**
```java
Files.lines(pathFileToRead).map(String::toLowerCase).forEach(System.out::println);
```
- A) Converts the content of a file to lowercase and prints it
  - `Correct: This line of code reads all lines from the file specified by pathFileToRead, converts each line to lowercase, and then prints each line to the console.`
- B) Prints the content of a file as lowercase characters
  - `Incorrect: The code does not print the content as individual lowercase characters, but it does print the lines after converting them to lowercase.`
- C) Throws an exception
  - `Incorrect: This code won't necessarily throw an exception unless there's a problem accessing the file system.`
- D) Converts the content of a file to lowercase and returns it as a list of strings
  - `Incorrect: The code does not return anything. It prints the lines after converting them to lowercase.`

**Question 96: What is the purpose of the Files.write() method?**
- A) It reads the content of a file
  - `Incorrect: The Files.write() method is used to write to a file, not to read its content.`
- B) It appends new content to a file
  - `Incorrect: The Files.write() method overwrites the existing content of a file by default. If you want to

 append content to a file, you need to pass an additional argument to the method.`
- C) It writes data to a file
  - `Correct: The Files.write() method is used to write byte or character data to a file.`
- D) It deletes a file
  - `Incorrect: The Files.write() method is not used to delete files. There is a separate method, Files.delete(), for that purpose.`

**Question 97: What does the following code do?**
```java
List<String> list = List.of("Apple", "Boy", "Cat", "Dog", "Elephant");
Files.write(pathFileToWrite, list);
```
- A) Creates a new file with the specified list of strings as its content
  - `Correct: If the file specified by pathFileToWrite does not exist, this code will create a new file with the contents of the list. If the file already exists, this code will overwrite the existing content of the file with the contents of the list.`
- B) Writes the list of strings to an existing file
  - `Incorrect: While the code does write the list of strings to the file specified by pathFileToWrite, it does not require the file to exist beforehand. If the file does not exist, the code will create it.`
- C) Deletes the file specified by pathFileToWrite
  - `Incorrect: This code does not delete any files.`
- D) Prints the list of strings to the console
  - `Incorrect: This code writes the list of strings to a file, not to the console.`

**Question 98: Which class provides methods for reading and writing files in Java?**
- A) Path
  - `Incorrect: The Path interface in the java.nio.file package represents a path in the file system, but it does not provide methods for reading and writing files.`
- B) File
  - `Incorrect: The File class in the java.io package provides methods for working with files and directories, but the methods for reading and writing files are provided by the java.nio.file.Files class in modern Java.`
- C) Files
  - `Correct: The java.nio.file.Files class provides static methods for reading and writing files.`
- D) Scanner
  - `Incorrect: The Scanner class in the java.util package is used for parsing text from various sources including files, but it is not the primary class for reading and writing files in Java.`
