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