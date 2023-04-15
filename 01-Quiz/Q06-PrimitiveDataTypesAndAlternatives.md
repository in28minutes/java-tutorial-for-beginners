
### Step 01: The Integer Types

**Question 1:** Which of the following wrapper classes corresponds to the `int` primitive type in Java?

1.  Byte
2.  Integer
3.  Short

**Answer:** `2. Integer`

**Question 2:** What is the maximum value of a `short` data type in Java?

1.  127
2.  32767
3.  2147483647

**Answer:** `2. 32767`

**Question 3:** What type of cast is used to store a smaller data value in a larger data type variable?

1.  Implicit cast
2.  Explicit cast

**Answer:** `1. Implicit cast`

### Step 02: Integer Representations, And Other Puzzles

**Question 1**

What are the three number systems supported by Java for integers?

1.  Decimal, Octal, and Binary
2.  Decimal, Octal, and Hexadecimal
3.  Decimal, Binary, and Hexadecimal

**Answer:** 2. Decimal, Octal, and Hexadecimal

**Question 2**

Which of the following is the correct representation for the value 16 in a hexadecimal system?

1.  0x10
2.  010
3.  0x16

**Answer:** 1. 0x10

**Question 3**

What is the difference between prefix and post-fix increment operators in Java?

1.  Prefix increment takes place before the assignment, and post-fix increment takes place after the assignment.
2.  Prefix increment takes place after the assignment, and post-fix increment takes place before the assignment.
3.  There is no difference between prefix and post-fix increment operators in Java.

**Answer:** 1. Prefix increment takes place before the assignment, and post-fix increment takes place after the assignment.

### Step 03: Classroom Exercise CE-01 (With Solutions)


**Question 1: What is the purpose of the `BiNumber` class?**

- A) To store a single integer and perform basic arithmetic operations 
- B) **To store a pair of integers and perform basic arithmetic operations** 
- C) To store a list of integers and perform basic arithmetic operations

**Question 2: Which method is used to double the values of both numbers in a `BiNumber` object?**

- A) `double()` 
- B) `doubleNumbers()` 
- C) **`doubleValue()`**

**Question 3: What will be the output of the following code snippet?**

```
BiNumber numbers = new BiNumber(4, 5);
System.out.println(numbers.add());
numbers.doubleValue();
System.out.println(numbers.getNumber1());
System.out.println(numbers.getNumber2());
```

- A) 9, 8, 10 
- B) **9, 8, 5** 
- C) 9, 4, 5


### Step 05: Floating-Point Types

#### Question 1

What is the default type for floating-point literals in Java?

- A) float 
- **B) double**

#### Question 2

How can you create a float literal?

- A) float f = 34.5 
- **B) float f = 34.5f;** 
- C) float f = (float)34.5

#### Question 3

Which type of casting is needed to convert a double value to a float value?

- A) Implicit casting 
- **B) Explicit casting**


### Step 06: Introducing BigDecimal



**Question 1:** What is the main reason for using the BigDecimal data type in Java?

1.  To represent floating-point numbers with higher precision
2.  To perform faster calculations
3.  To store large integer values

_Answer: 1. To represent floating-point numbers with higher precision_

**Question 2:** What is the best way to construct a BigDecimal object to achieve high precision?

1.  Using integer literals
2.  Using double literals
3.  Using string literals

_Answer: 3. Using string literals_

**Question 3:** What is the main characteristic of BigDecimal objects?

1.  Mutable
2.  Immutable
3.  Synchronized

_Answer: 2. Immutable_


### Step 06: BigDecimal Operations

1.  Which of the following methods can be used for arithmetic operations on BigDecimal objects?
    
    - a. `add()` 
    - b. `multiply()` 
    - c. `subtract()` 
    - d. All of the above
    

**Answer: d. All of the above**

2.  Can you perform arithmetic operations directly between a BigDecimal object and a primitive data type, like an int or a double?
    
    - a. Yes 
    - b. No
    

**Answer: b. No**

3.  How can you perform an arithmetic operation between a BigDecimal object and a primitive int value?
    
    - a. Convert the int to a BigDecimal using `BigDecimal.valueOf()` 
    - b. Use a type cast to convert the int to a BigDecimal 
    - c. Perform the operation directly as the BigDecimal class automatically handles primitive types
    

**Answer: a. Convert the int to a BigDecimal using `BigDecimal.valueOf()`**


### Step 08: boolean, Relational and Logical Operators

1.  Which of the following operators is a logical operator in Java?
    
    - a) `>` 
    - b) `&&` 
    - c) `<=`
    
    **Answer: b) `&&`**
    
2.  Given the following code snippet, what will be the value of `result`?
    
```
  int a = 10;
    int b = 5;
    boolean result = (a > b) && (a < 2 * b);
```
    
   - a) `true` 
   - b) `false`
    
   **Answer: a) `true`**
    
3.  What will the following expression evaluate to?
    
    ```
    boolean x = true;
    boolean y = false;
    boolean z = !(x || y);
    ```
    
    - a) `true` 
    - b) `false`
    
    **Answer: b) `false`**


 ### Step 10: Character Types


### Question 1

What is the Unicode representation of the double quotation mark?

1.  `\u0021`
2.  `\u0022`
3.  `\u0023`

**Answer:** 2. `\u0022`

### Question 2

What data type in Java is used to store Unicode characters?

1.  String
2.  char
3.  int

**Answer:** 2. char

### Question 3

What happens when you perform the following operation in Java: `char cn = 65;`?

1.  A character with a Unicode value of 65 is stored in the variable `cn`.
2.  An integer value of 65 is stored in the variable `cn`.
3.  A compilation error occurs.

**Answer:** 1. A character with a Unicode value of 65 is stored in the variable `cn`.   