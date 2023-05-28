**Step 1: The Integer Types**

**Question 1: Which of the following wrapper classes corresponds to the int primitive type in Java?**

- A) Byte `Incorrect: Byte corresponds to the byte primitive type, not int.`
- B) Integer `Correct: Integer is the wrapper class for the int primitive type in Java.`
- C) Short `Incorrect: Short corresponds to the short primitive type, not int.`

**Question 2: What is the maximum value of a short data type in Java?**

- A) 127 `Incorrect: 127 is the maximum value for a byte, not short.`
- B) 32767 `Correct: 32767 is indeed the maximum value a short can take in Java.`
- C) 2147483647 `Incorrect: This is the maximum value for int, not short.`

**Question 3: What type of cast is used to store a smaller data value in a larger data type variable?**

- A) Implicit cast `Correct: Java will automatically perform an implicit cast when storing a smaller data type in a larger one.`
- B) Explicit cast `Incorrect: Explicit casting is used when we want to convert a larger type to a smaller one, potentially losing information.`

**Step 2: Integer Representations, And Other Puzzles**

**Question 1: What are the three number systems supported by Java for integers?**

- A) Decimal, Octal, and Binary `Incorrect: Java supports Decimal, Octal, Binary and also Hexadecimal.`
- B) Decimal, Octal, and Hexadecimal `Correct: Java supports these three number systems as well as binary.`
- C) Decimal, Binary, and Hexadecimal `Correct: Java indeed supports these three number systems.`

**Question 2: Which of the following is the correct representation for the value 16 in a hexadecimal system?**

- A) 0x10 `Correct: 0x prefix denotes hexadecimal in Java, and 10 is 16 in hexadecimal.`
- B) 010 `Incorrect: The 0 prefix is for octal numbers in Java, not hexadecimal.`
- C) 0x16 `Incorrect: 0x16 represents 22 in decimal, not 16.`

**Question 3: What is the difference between prefix and post-fix increment operators in Java?**

- A) Prefix increment takes place before the assignment, and post-fix increment takes place after the assignment. `Correct: In prefix, the value is incremented first then used whereas in postfix the value is used then incremented.`
- B) Prefix increment takes place after the assignment, and post-fix increment takes place before the assignment. `Incorrect: It's the other way around. Prefix increment occurs before assignment and post-fix increment after assignment.`
- C) There is no difference between prefix and post-fix increment operators in Java. `Incorrect: The order of operations differs between the two.`

**Step 3: Classroom Exercise CE-01 (With Solutions)**

**Question 1: What is the purpose of the BiNumber class?**

- A) To store a single integer and perform basic arithmetic operations `Incorrect: BiNumber is designed to store and operate on a pair of numbers, not a single integer.`
- B) To store a pair of integers and perform basic arithmetic operations `Correct: The BiNumber class is designed to store two numbers and perform operations on them.`
- C) To store a list of integers and perform basic arithmetic operations `Incorrect: BiNumber class is not intended for storing a list of integers.`

**Question 2: Which method is used to double the values of both numbers in a BiNumber object?**

- A)

 double() `Incorrect: There's no double() method in the BiNumber class.`
- B) doubleNumbers() `Correct: The doubleNumbers() method doubles the values of both numbers in the BiNumber object.`
- C) doubleValue() `Incorrect: The doubleValue() method is not used to double the numbers in the BiNumber class.`

**Question 3: What will be the output of the following code snippet?**

```java
BiNumber numbers = new BiNumber(4, 5);
System.out.println(numbers.add());
numbers.doubleValue();
System.out.println(numbers.getNumber1());
System.out.println(numbers.getNumber2());
```

- A) 9, 8, 10 `Correct: The add() method returns the sum of the numbers (4+5=9). The doubleValue() method doubles the values (4*2=8 and 5*2=10).`
- B) 9, 8, 5 `Incorrect: The second number is also doubled by the doubleValue() method, it should be 10 not 5.`
- C) 9, 4, 5 `Incorrect: The doubleValue() method doubles the values of both numbers.`

**Step 5: Floating-Point Types**

**Question 1: What is the default type for floating-point literals in Java?**

- A) float `Incorrect: In Java, floating-point literals are by default considered double.`
- B) double `Correct: Double is indeed the default data type for floating-point literals in Java.`

**Question 2: How can you create a float literal?**

- A) float f = 34.5 `Incorrect: This will lead to a compilation error as 34.5 is a double literal by default. A suffix of 'f' or 'F' is needed to make it a float literal.`
- B) float f = 34.5f; `Correct: This is the correct way to create a float literal in Java. The 'f' suffix indicates a float literal.`
- C) float f = (float)34.5 `Correct: Explicitly casting a double literal to a float will also work, but the 'f' suffix is generally preferred.`

**Question 3: Which type of casting is needed to convert a double value to a float value?**

- A) Implicit casting `Incorrect: Implicit casting is used when we convert a smaller type to a larger one.`
- B) Explicit casting `Correct: When converting a larger type to a smaller one, such as double to float, explicit casting is needed.`

**Step 6: Introducing BigDecimal**

**Question 1: What is the main reason for using the BigDecimal data type in Java?**

- A) To represent floating-point numbers with higher precision `Correct: BigDecimal allows us to represent floating-point numbers with almost arbitrary precision, making it a good choice for financial and monetary calculations.`
- B) To perform faster calculations `Incorrect: BigDecimal computations are generally slower than primitive types due to the higher precision and object overhead.`
- C) To store large integer values `Incorrect: Although BigDecimal can indeed store large numbers, its primary purpose is to offer precise floating-point computations.`

**Question 2: What is the best way to construct a BigDecimal object to achieve high precision?**

- A) Using integer literals `Incorrect: Although you can construct a BigDecimal with an integer literal, for high precision you should prefer string literals.`
- B) Using double literals `Incorrect: This can introduce rounding errors because of the binary representation of double literals. It's not the preferred way for high precision.`
- C) Using string literals `Correct: Constructing BigDecimal objects using string literals is the preferred way when high precision is required.`

**Question 3: What is the main characteristic of BigDecimal objects?**

- A) Mutable `Incorrect: BigDecimal objects are immutable, which means their value

 cannot be changed once created.`
- B) Immutable `Correct: Indeed, BigDecimal objects are immutable.`
- C) Synchronized `Incorrect: Synchronization isn't a characteristic of BigDecimal. It's a concept related to multi-threading.`

**Step 6: BigDecimal Operations**

**Question 1: Which of the following methods can be used for arithmetic operations on BigDecimal objects?**

- A) add() `This method is used for addition operations on BigDecimal objects.`
- B) multiply() `This method is used for multiplication operations on BigDecimal objects.`
- C) subtract() `This method is used for subtraction operations on BigDecimal objects.`
- D) All of the above `Correct: All these methods can be used for arithmetic operations on BigDecimal objects.`

**Question 2: Can you perform arithmetic operations directly between a BigDecimal object and a primitive data type, like an int or a double?**

- A) Yes `Incorrect: You cannot directly perform arithmetic operations between a BigDecimal object and a primitive data type.`
- B) No `Correct: You need to convert the primitive to a BigDecimal first.`

**Question 3: How can you perform an arithmetic operation between a BigDecimal object and a primitive int value?**

- A) Convert the int to a BigDecimal using BigDecimal.valueOf() `Correct: This is the best way to convert a primitive int to a BigDecimal for arithmetic operations.`
- B) Use a type cast to convert the int to a BigDecimal `Incorrect: You can't use casting to convert a primitive to a BigDecimal.`
- C) Perform the operation directly as the BigDecimal class automatically handles primitive types `Incorrect: The BigDecimal class doesn't automatically handle arithmetic with primitives.`

**Step 8: boolean, Relational and Logical Operators**

**Question 1: Which of the following operators is a logical operator in Java?**

- A) > `Incorrect: '>' is a relational operator, not a logical operator.`
- B) && `Correct: '&&' is a logical AND operator. It returns true if both operands are true.`
- C) <= `Incorrect: '<=' is a relational operator, not a logical operator.`

**Question 2: Given the following code snippet, what will be the value of result?**
```java
  int a = 10;
    int b = 5;
    boolean result = (a > b) && (a < 2 * b);
```

- A) true `Correct: Since both conditions (a > b and a < 2 * b) are true, the result will be true.`
- B) false `Incorrect: Given the values of a and b, the result of the boolean expression is true.`

**Question 3: What will the following expression evaluate to?**

```java
boolean x = true;
boolean y = false;
boolean z = !(x || y);
```

- A) true `Incorrect: Since 'x' is true, 'x || y' is also true. The negation of true is false.`
- B) false `Correct: The expression '(x || y)' is true, so the negation of this expression is false.`

**Step 10: Character Types**

**Question 1: What is the Unicode representation of the double quotation mark?**

- A) \u0021 `Incorrect: \u0021 is the Unicode representation for the exclamation mark (!).`
- B) \u0022 `Correct: \u0022 is the Unicode representation for the double quotation mark (").`
- C) \u0023 `Incorrect: \u0023 is the Unicode representation for the number sign (#).`

**Question 2: What data type in Java is used to store Unicode characters?**

- A) String `Incorrect: Although a String can contain Unicode characters, the data type specifically designed to store a single Unicode character is char.`
- B) char `Correct: The char data type in Java is used to store a single Unicode character.`
-

 C) byte `Incorrect: Although a byte can represent a character in some encodings, the char data type is specifically designed for this purpose in Java.`

**Question 3: What will the following code print out?**

- A) The character 'a' `Incorrect: The code will print the character corresponding to the Unicode value 0x0041, which is 'A'.`
- B) The character 'A' `Correct: The Unicode value 0x0041 corresponds to the character 'A'.`
- C) The number 65 `Incorrect: The code will print the character corresponding to the Unicode value 0x0041, not the value itself.`
