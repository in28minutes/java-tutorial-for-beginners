### Step 01 : Defining A Simple Method 
### Step 02: Exercise-Set PE-01

### Exercise 1

1.  Launch JShell
2.  Define a method named `printHello` that prints the string "Hello" to the console.
3.  Call the `printHello` method.
4.  Exit JShell using `/exit` command.

#### Solution 1

1. Launch JShell

2. Define a method named `printHello` that prints the string "Hello" to the console:

```
jshell> void printHello() {
   ...> System.out.println("Hello");
   ...> }
```

3. Call the `printHello` method:

```
jshell> printHello();
Hello
```

4. Exit JShell using `/exit` command:
```
jshell> /exit
```

### Exercise 2

1.  Launch JShell
2.  Define a method named `printNumbers` that prints the numbers 1 to 5 to the console, each on a new line.
3.  Call the `printNumbers` method.
4.  Exit JShell using `/exit` command.

### Solution 2

1. Launch JShell

2. Define a method named `printNumbers` that prints the numbers 1 to 5 to the console, each on a new line:

```
jshell> void printNumbers() {
   ...> for (int i = 1; i <= 5; i++) {
   ...> System.out.println(i);
   ...> }
   ...> }
   ```

3. Call the `printNumbers` method:
```
jshell> printNumbers();
1
2
3
4
5
```

4. Exit JShell using `/exit` command:
```
jshell> /exit
```



### Step 03: Editing A Method Definition (Jshell Tips)





#### Exercise 1: Editing a Method Definition in JShell

1.  Launch JShell.
2.  Define a method called `printMessage` that prints the message "Hello, World!" to the console.
3.  Call the `printMessage` method to verify that it works.
4.  Modify the `printMessage` method so that it prints a different message.
5.  Call the `printMessage` method again to verify that it now prints the new message.
6.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.

```
jshell>
```

2.  Define a method called `printMessage` that prints the message "Hello, World!" to the console.

```
jshell> void printMessage() {
   ...>   System.out.println("Hello, World!");
   ...> }
   ```

3.  Call the `printMessage` method to verify that it works.

```
jshell> printMessage();
Hello, World!
```

4.  Modify the `printMessage` method so that it prints a different message.

```
jshell> void printMessage() {
   ...>   System.out.println("Goodbye, World!");
   ...> }
   ```

5.  Call the `printMessage` method again to verify that it now prints the new message.

```
jshell> printMessage();
Goodbye, World!
```

6.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```




#### Exercise 2: Editing A Method Definition in JShell

1.  Launch JShell.
2.  Define a method called `greet` that prints the message "Welcome to JShell!" to the console.
3.  Call the `greet` method.
4.  Edit the `greet` method to print "Hello, JShell!" to the console instead.
5.  Call the `greet` method again to verify that it has been updated.
6.  Exit JShell using the `/exit` command.

##### Solution

1.  Launch JShell.
    
2.  Define a method called `greet` that prints the message "Welcome to JShell!" to the console.
    

```
jshell> void greet() {
   ...>     System.out.println("Welcome to JShell!");
   ...> }
   ```

3.  Call the `greet` method.

```
jshell> greet();
Welcome to JShell!
```

4.  Edit the `greet` method to print "Hello, JShell!" to the console instead.

```
jshell> /edit greet
```

This will open the method definition in an external editor. Replace the line that prints "Welcome to JShell!" with the following line:

```
System.out.println("Hello, JShell!");
```

Save the changes and close the editor.

5.  Call the `greet` method again to verify that it has been updated.

```
jshell> greet();
Hello, JShell!
```

6.  Exit JShell using the `/exit` command.

```
jshell> /exit
|  Goodbye
```