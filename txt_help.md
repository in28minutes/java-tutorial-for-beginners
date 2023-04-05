## Primitive Data Types

Earlier, we looked at basic Java types (including ```int```, ```double``` and ```boolean```), and got a little familiar with them.

We used literal values, declared variables and formed expressions using them. 

Java **primitive types** include:
* Integer Types
	* ```byte```
	* ```short```
	* ```int```
	* ```long```
* Floating-Point Types
	* ```float```
	* ```double```
* Character Type
	* ```char```
* Logical Type
	* ```boolean```

In this section, let's play with each of these types to understand them further.

### Step 01: The Integer Types

Integers are not much of a mystery, are they? They've been part of us since our school days, and we normally prefer them over other numbers (they scare us less!). 

Java supports them with ease, and we have coded quite a few examples using them, already. 

Java also has a **wrapper class** corresponding to each of them, which make their primitive versions more versatile. The wrapper classes we are talking about are:

* ```Byte```: for ```byte```
* ```Short```: matching ```short```
* ```Integer``` corresponding to ```int```
* ```Long```: about ```long```

Let's see how we can work with them.

##### Snippet-01 : Integer Sizes

Look at all the information these tiny classes hold for you! As they say, **_"fore-warned is fore-armed"_**. Depending on the data (range and size) your program handles, you decide which types to use, to store them.

```java

	jshell> Byte.SIZE
	$1 ==> 8
	jshell> Byte.BYTES
	$2 ==> 1
	jshell> Byte.MAX_VALUE
	$3 ==> 127
	jshell> Byte.MIN_VALUE
	$4 ==> -128
	jshell> Short.BYTES
	$5 ==> 2
	jshell> Integer.BYTES
	$6 ==> 4
	jshell> Long.BYTES
	$7 ==> 8
	jshell> Short.MAX_VALUE
	$8 ==> 32767
	jshell> Integer.MAX_VALUE
	$8 ==> 2147483647
	jshell> int i = 100000;
	i ==> 100000
	jshell> long l = 50000000000;
	| Error:
	| integer number too large: 50000000000
	| long l = 50000000000;
	|_________^
	jshell> long l = 50000000000l;
	l ==> 50000000000
	jshell>

```

#### Integer Type Conversions

Problems will (and should) arise if we attempt to store large data into smaller bins. The compiler warns the programmer about such issues by flagging errors. However, if the programmer is aware of the risks and intends to go ahead, **explicit casts** are her tools to push the code through.

Operations in the other direction (storing a smaller data value in a larger bin), is a piece of cake for the compiler. Such a conversion is called an **implicit cast**.

##### Snippet-02 : Integer Type Conversions 

Attempting to store a ```long``` value into an ```int``` variable will give us a compiler error. However, you can use an explicit cast, such as ```i = (int) l;```.

```java

	jshell> int i = 100000;
	i ==> 100000
	jshell> long l = 50000000000l;
	l ==> 50000000000
	jshell> i = l;
	| Error :
	| incompatible types: possible lossy conversion from long to int
	| i = l;
	|_____^
	jshell> i = (int) l;
	i ==> -1539607552
	jshell> l = i;
	l ==> -1539607552
	jshell>
	
```

**_The compiler is not responsible for the type-safety of this statement. The onus is on me, the programmer._**

Remember our earlier statement on possible incorrect program behavior? As you can see, a different value got stored in ```i```.

#### Summary

In this step, we:

* Explored the wrapper classes present for the primitive integer types
* Understood the different capacities and data ranges of these types
* Examined how to use explicit and implicit casts

### Step 02: Integer Representations, And Other Puzzles

In a decimal system, the allowed digits are ```0``` through ```9```. When a value of ```10``` is encountered, the number of digits increases by 1, and its representation is "```10```".

Those familiar with number systems would know that decimal is not the only system that computers understand. 

Other number systems that the Java language supports are **Octal** (Base-8) and **Hexadecimal** (Base-16). 

In an Octal system, the allowed digits are ```0``` through ```7```, and a value ```8``` is represented by "```010```". The leading ```0``` is added only to distinguish the octal format from the decimal one. 

In a Hexadecimal system, the allowed digits are ```0``` through ```9```, followed by ```a``` through ```f``` (or ```A``` through ```F```). A value of ```16``` is represented by "```0x10```". Here, a leading ```0x``` is added to help the compiler recognize Hexa decimal representation.

Let's see how Java supports these three number systems.

##### Snippet-01 : Storing Octal and Hexadecimal in Integer types

There are no number-system specific integer types in Java! The same ```int``` type is used to store decimal, octal and hexadecimal values. 

If we adhere to to number system conventions about valid digits and understand the compiler hints, we get no surprises.

```java

	jshell> int eight = 010;
	eight ==> 8
	jshell> int sixteen = 0x10;
	sixteen ==> 16
	jshell> int fifteen = 0xf;
	fifteen ==> 15
	jshell> int eight = 08;//8 is invalid octal digit
	| Error:
	| integer number too large : 08
	| int eight = 08;
	|___________^
	jshell> int big = 0xbbaacc;
	big ==> 12298956
	jshell>

```

##### Snippet-02 : More Integer Type-casting

There are two kinds of assignments:
* Literal-to-variable assignment: With ```short s = 123456;```, the data is clearly out of range (this is known at compile-time). The compiler flags an error.
* Variable-to-variable assignment:  Consider ```sh = in;```. The value stored in ```int in``` at that stage was ```4567```, which is well within the range of the ```short``` type. The compiler chooses not to take chances and flags an error. This can again be preempted with a explicit cast `sh = (short) in`.


```java

	jshell> byte b = 128;
	| Error:
	| incompatible types: possible lossy conversion from int to byte
	| byte b = 128;
	|_________^--^
	jshell> short s = 123456;
	| Error:
	| incompatible types: possible lossy conversion from int to short
	| short s = 123456;
	|__________^-------^
	jshell> short sh = 3456;
	sh ==> 3456
	jshell> int in = 4567;
	in ==> 3456
	jshell> sh = in;
	| Error:
	| incompatible types: possible lossy conversion from int to short
	| sh = in;
	|______^
	jshell> sh = (short) in;
	sh ==> 4567
	jshell> int num = sh;
	num ==> 4567
	jshell>

```

#### Built-In Operators For Integer Types

We already had a glimpse of arithmetic operators for the integer types:
* ```+```
* ```-```
* ```*```
* ```/```
* ```%```
* ```++``` (both prefix and post-fix increment)
* ```--``` (both prefix and post-fix increment)

The increment and decrement operators are an interesting case, as they are actually short-hands for multiple statements. When we use their prefix and post-fix versions, we need to look out for side-effects.

##### Snippet-03 : Increment & Decrement Operators

With post-fix increment, such as in ```int j = i++;```, the increment takes place *after* the assignment is done. ```j``` gets the value before increment.
```java

	jshell> int i = 10;
	i ==> 10
	jshell> int j = i++;
	j ==> 10
	jshell> i
	i ==> 11
```

When prefix increment is involved, as with ```int n = ++m;```, the increment is carried out *before* the assignment. ```n``` gets the value after increment.

```java
	jshell> int m = 10;
	m ==> 10
	jshell> int n = ++m;
	n ==> 11
	jshell> m
	m ==> 11
```

With post-fix decrement, as with ```int l = k--;```, the decrement occurs *after* the assignment is done. As far as prefix decrement is concerned, such as in ```int q = --p;```, the decrement is performed *before* the assignment.

```java
	jshell> int k = 10;
	k ==> 10
	jshell> int l = k--;
	l ==> 10
	jshell> k
	k ==> 9
	jshell> int p = 10;
	p ==> 10
	jshell> int q = --p;
	q ==> 9
	jshell> p
	p ==> 9
	jshell>

```

#### Summary:

In this step, we:

* Looked at the number-systems supported in Java for integers
* Examined how prefix and post-fix versions work for increment and decrement operators

- - -	
### Step 03: Classroom Exercise CE-01 (With Solutions)

#### Exercise Set

1. Create a Java ```class``` ```BiNumber``` that stores a pair of integers, and has the following functionality:

	* Can be created by passing its initial two numbers to store
	* Must Support Addition and Multiplication operations on the stored integers
	* An operation to double the values of both numbers
	* Operations to access each number individually
	
In short, we must be able to write code like this in the ```main``` method of  our runner class:

```java

	BiNumber numbers = new BiNumber(2, 3);
	System.out.println(numbers.add());
	System.out.println(numbers.multiply());
	numbers.double();
	System.out.println(numbers.getNumber1());
	System.out.println(numbers.getNumber2());

```

#### Solution to CE-01

**_BiNumber.java_**

```java

	package com.in28minutes.primitive.datatypes;
	
	public class BiNumber {
		private int number1;
		private int number2;

		public BiNumber(int number1, int number2) {
			this.number1 = number1;
			this.number2 = number2;
		}

		public int add() {
			return number1 + number2;
		}

		public int multiply() {
			return number1 * number2;
		}

		public void doubleValue() {
			number1 *= 2;
			number2 *= 2;
		}

		public int getNumber1() {`
			return number1;
		}

		public int getNumber2() {
			return number2;
		}

		public void setNumber1(int number1) {
			this.number1 = number1;
		}

		public void setNumber2(int number2) {
			this.number2 = number2;
		}
	}

```

**_BiNumberRunner.java_**

```java

	package com.in28minutes.primitive.datatypes;

	public class BiNumberRunner {
		public static void main(String[] args) {
			BiNumber numbers = new BiNumber(2, 3);
			System.out.println(numbers.add());
			System.out.println(numbers.multiply());
			numbers.doubleValue();
			System.out.println(numbers.getNumber1());
			System.out.println(numbers.getNumber2());
		}
	}

```

**_Console Output_**

_5_

_6_

_4_

_6_

### Step 05: Floating-Point Types

You would recall there are two types in Java to support floating-point numbers:
* ```double```: The default type for floating-point literals, with a capacity of 8 bytes
* ```float```: A narrower, less precise representation for floating-point data. It has a capacity of 4 bytes.

Let's quickly refresh what we know, with a few code snippets.

##### Snippet-01 : double and float

Default floating point type in Java is `double`. A ```float``` literal must be accompanied with a trailing ```f``` or ```F```.


```java

	jshell> float f = 34.5;
	| Error:
	| incomaptible types: possible lossy conversion from double to float
	| float f = 34.5;
	|_________^---^
	jshell> float f = 34.5f;
	f ==> 34.5
	jshell> float fl = 34.5F;
	fl ==> 34.5
	jshell> double d = 34.5678;
	d ==> 34.5678
	jshell> float flo = d;
	| Error:
	| incomaptible types: possible lossy conversion from double to float
	| float flo = d;
	|__________^
	jshell> float flo = (float) d;
	flo ==> 34.567
	jshell>

```

##### Snippet-02 : Operators for type double

You can use operators `++`, `--` and `%` on double. 

```java

jshell> double dbl = 34.5678;
dbl ==> 34.5678

jshell> dbl++
$3 ==> 34.5678

jshell> dbl
dbl ==> 35.5678

jshell> dbl--
dbl ==> 35.5678
jshell> dbl % 5
dbl ==> 4.567799999999998
```

You would need an explicit cast to convert a float to an integer value `int i = (int)f`.

```java
	jshell> float f = 34.5678f;
	f ==> 34.5678
	jshell> int i = f;
	| Error:
	| incomaptible types: possible lossy conversion from float to int
	| int i = f;
	|_______^
	jshell> int i = (int)f;
	i ==> 34
	jshell> float fl = i;
	fl ==> 34.0
	jshell>

```
#### Summary

In this step, we:

* Saw how we create literals and variables of the floating-point types
* Understood the differences between ```double``` and ```float```

### Step 06: Introducing BigDecimal

Compact though they are, ```double``` and ```float``` are not very precise representations of floating-point numbers. 

In fact, they are not used in computations that require high degrees for accuracy, such as scientific experiments and financial applications. The next example shows you why.


```java

	jshell> 34.56789876 + 34.2234
	$1 ==> 68.79129875999999
```

The literal expression ```34.56789876 + 34.2234``` should evaluate to ```68.79129876```. Above addition is not really accurate.

This is due to a flaw in floating-point representations, used in the ```double``` and ```float``` types.

The ```BigDecimal``` class was introduced in Java to tide over these problems.

Accuracy of ```BigDecimal``` representation is retained only when ```String``` literals are used to build it.



```java

	jshell> BigDecimal number1 = new BigDecimal("34.56789876");
	number1 ==> 34.56789876
	jshell> BigDecimal number2 = new BigDecimal("34.2234");
	number2 ==> 34.2234_
```

A ```BigDecimal``` type can be used to create only **immutable** objects. The values in an *immutable* object cannot be changed after creation. 

You can see that the value of number1 is not changed on executing `number1.add(number2)`. To get the result of the sum, we create a new variable `sum`.

```java
	jshell> number1.add(number2);
	$2 ==> 68.79129876
	jshell> number1
	number1 ==> 34.56789876
	jshell> BigDecimal sum = number1.add(number2);
	sum ==> 68.79129876
```

#### Summary

In this step, we:

* Learned that ```double``` and ```float``` are not very precise data types
* Were introduced to the ```BigDecimal``` built-in data type
* Understood that ```BigDecimal``` is immutable
* Saw that accuracy is best achieved when you construct ```BigDecimal``` data using string literals 

### Step 06: BigDecimal Operations

Let's look at a few other operations defined in the ```BigDecimal``` class.

##### Snippet-01: Arithmetic Operations

All BigDecimal operations support only BigDecimal operands.

```java

	jshell> BigDecimal number1 = new BigDecimal("11.5");
	number1 ==> 34.56789876
	jshell> BigDecimal number2 = new BigDecimal("23.45678");
	number2 ==> 23.45678
	jshell> number1.add(number2);
	$1 ==> 34.95678
```

```BigDecimal``` does not jell well with primitive types.

```java
	jshell> int i = 5;
	i ==> 5
	jshell> number1.add(i);
	| Error:
	| incompatible types: int cannot be converted to java.math.BigDecimal
	| number1.add(i);
	|_____________^
```

We can add, multiple, divide or subtract `BigDecimal` values.

```java
	jshell> number1.add(new BigDecimal(i));
	$2 ==> 16.5
	jshell> number1.multiply(new BigDecimal(i));
	$3 ==> 67.5
	jshell> number1.divide(new BigDecimal(100));
	$4 ==> 0.115
	jshell>

```

#### Summary

In this step, we:

* Explored the ```BigDecimal``` methods for doing some basic arithmetic
* Found that ```BigDecimal``` has constructors accepting most basic Java numeric types

### Step 07: Classroom Exercise CE-02

#### Exercise-Set

Write a Program that does a Simple Interest computation for a Principal amount. Recall that the formula for such a calculation is:

`Total amount (TA) = Principal Amount (PA) + ( PA * Simple Interest (SI) Rate * Duration In Years (N))`

In essence, write a ```SimpleInterestCalculator``` ```class``` that can be used in the following manner:

```java

	SimpleInterestCalculator calculator = new SimpleInterestCalculator("4500.00", "7.5");
	BigDecimal totalValue = calculator.calculateTotalValue(5); //5 year duration
	System.out.println(totalValue);

```

#### Solution To CE-02

**_SimpleInterestCalculatorRunner.java_**

```java

	package com.in28minutes.primitive.datatypes;
	import java.math.BigDecimal;

	public class SimpleInterestCalculatorRunner {
		public static void main(String[] args) {
			SimpleInterestCalculator calculator = new SimpleInterestCalculator("4500.00", 7.5");
			BigDecimal totalValue = calculator.calculateTotalValue(5); //5 year duration
			System.out.println(totalValue);
		}
	}

```

**_SimpleInterestCalculator.java_**

```java

	package com.in28minutes.primitive.datatypes;
	import java.math.BigDecimal;

	public class SimpleInterestCalculatorRunner {
		BigDecimal principal;
		BigDecimal interest;

		public SimpleInterestCalculator(String principal, String interest) {
			this.principal = new BigDecimal(principal);
			this.interest = new BigDecimal(interest).divide(new BigDecimal(100));
		}

		public BigDecimal calculateTotalValue(int noOfYears)
			//Total Value = Principal  + Principal * Interest* Years
			BigDecimal totalValue = prinipal.add(principal.multiply(interest).multiply(new BigDecimal(noOfYears)));
			return totalValue;`
		}	
}

```

**_Console Output:_**

_6187.50000_

#### Tip: The ```import``` Statement

The Java ```import``` statement is Required in each source file that uses a ```class``` from another ```package```. Hence, both **_SimpleInterestCalculator.java_** (```class``` definition) and **_SimpleInterestCalculatorRunner.java_** (runner ```class``` definition) need to import ```class``` ```java.math.BigDecimal```.

```package java.lang.*``` is imported by default. 

The ```.*``` suffix indicates that all classes in the ```package``` ```java.lang``` are being imported.

#### Summary

In this step, we:

* Used ```BigDecimal``` values in a stand-alone Java program
* Learnt how to make use of built-in Java packages, through the ```import``` statement 

### Step 08: ```boolean```, Relational and Logical Operators

The Java ```boolean	``` data type is one that holds only one of two values: ```true``` or ```false```. Both labels are case-sensitive. We have seen examples of built-in comparison operators, such as ```==```, ```!=``` and ```>```, that evaluate expressions to  give us ```boolean``` results. Let us do a quick recap of some of these.

##### Snippet-01 : Relational Operators : Recap

Relational Operators are used mainly for comparison. They accept operands of non-```boolean``` primitive data types, and return a ```boolean``` value.

```java

	jshell> int i = 7;
	i ==> 7
	jshell> i > 7;
	$1 ==> false
	jshell> i >= 7;
	$2 ==> true
	jshell> i < 7;
	$3 ==> false
	jshell> i <= 7;
	$4 ==> true
	jshell> i == 7;
	$5 ==> true
	jshell> i == 8;
	$6 ==> false
	jshell>
	
```

#### Logical Operators

Java also has logical operators that are used in expressions. Logical operators expect ```boolean``` operands. Expressions involving these are used for forming ```boolean``` conditions in code, including within  ```if```, ```for``` and ```while``` statements.  The prominent logical operators are:

* ```&&``` : logical **AND**
* ```||``` : **OR**
* ```!``` : **NOT**

Let's learn how we use them in our code.

##### Snippet-02 : Logical Operators

We would want to find if `i` is between `15` and `25`.  An expression `i >= 15 && i <= 25` can be used. Details below.

```java

	jshell> int i = 17;
	i ==> 17
	jshell> i >= 15
	$1 ==> true
	jshell> i <= 25
	$2 ==> true
	jshell> i >= 15 && i <= 25
	$3 ==> true
	jshell> i == 30;
	i ==> 30
	jshell> i >= 15 && i <= 25
	$4 ==> false
	jshell> i == 5;
	i ==> 30
	jshell> i >= 15 && i <= 25
	$5 ==> false
```

An expression with```&&``` evaluates to ```true``` only if **both** its ```boolean``` operands evaluate to ```true```.

```java
	jshell> true && true
	$6 ==> true
	jshell> true && false
	$7 ==> false
	jshell> false && true
	$8 ==> false
	jshell> false && false
	$9 ==> false
	jshell>

```

##### Snippet-02 Explained

The next example helps us visualize truth tables for the prominent logical operators.

```java

	jshell> true || true
	$1 ==> true
	jshell> true || false
	$2 ==> true
	jshell> false || true
	$3 ==> true
	jshell> false || false
	$4 ==> false
	jshell> true ^ true
	$5 ==> false
	jshell> true ^ false
	$6 ==> true
	jshell> false ^ true
	$7 ==> true
	jshell> false ^ false
	$8 ==> false
	jshell> !true
	$9 ==> false
	jshell> !false
	$10 ==> true
	jshell> int x = 6;
	x ==> 6
	jshell> !(x > 7)
	$11 ==> true
	jshell>

```

#### Summary

In this step, we:

* We're introduced to the ```boolean``` primitive type
* Understood where logical operators are used in Java programs
* Explored the truth-tables of commonly used logical operators

### Step 09: Short-Circuit Evaluation (With Puzzles)

Consider code below. The expression ```j > 15 && i++ > 5``` evaluates to ```false``` as expected. `j>15` is `false` as `j` has a value of `15`. 


```java

	jshell> int j = 15;
	j ==> 15
	jshell> int i = 10;
	i ==> 10
	jshell> j > 15 && i++ > 5
	$1 ==> false
	jshell> j
	j ==> 15
	jshell> i
	i ==> 10
```

You can also observe that the value of i remains unchanged `10`.  

Why? Because ```i++ > 5``` was not even evaluated.
Why? `&&` is lazy. It saw that `j > 15` is false. Irrespective of the result of second expression, the result of this `&&` would be false. So, it does NOT evaluate the second expression.

***A more detailed explanation***

The expression ```j > 15 && i++ > 5``` was scanned from left to right. As the first operand to ```&&``` evaluated to ```false```, the compiler got lazy. `&&` avoids evaluating expressions that don't affect the final result. The optimization has a name: **Short-Circuit Evaluation**, also called **lazy evaluation**.


The logical operator ```&``` is another version of the logical **AND** operation, that does away with lazy evaluation. 

Both operands to ```&``` are always evaluated. 

```java

	jshell> j > 15 & i++ > 5
	$1 ==> false
	jshell> j
	j ==> 15
	jshell> i
	i ==> 11
	jshell>

```

Similarly, the logical **OR** operator also has two versions: 
* The ```||``` operator we saw earlier. This exhibits lazy evaluation.
* The ```|``` operator, without lazy evaluation.

It is bad programming practice for our code to depend on the compiler's lazy evaluation. It makes code less readable, and can hide difficult-to-fix software bugs. It obviously adds to the code maintenance burden, so don't do it unless you like being in your peers' bad books.        

#### Summary

In this step, we:

* Examined conditions involving logical operators, that had lazy evaluation
* Observed that the lazy evaluation depends on the operator's truth-table
* Saw versions of the operators without lazy evaluation
* Learned that code depending on lazy-evaluation, is less readable 

### Step 10: Character Types
 
Earlier, we explored how we could store basic keyboard characters(called **ascii-code** characters), such as:
* Upper-Case and lower-case letters (A-Z, a-z)
* Numeric characters (0-9)
* Punctuation and other special characters (such as ',', '$', '{', etc.)

Turns out Java supports a much larger family of character encoding sets, called **Unicode**. All Unicode characters can be input to, understood and processed by, as well as output from your code. 

##### Snippet-01 : Unicode characters

Not all Unicode characters can be input from your keyboard. But Java allows you to  handle their values from your code, if you deal correctly with their format.

```java 
 
	jshell> char ch = '"';
	ch ==> '"'
	jshell> char c = '\u0022';
	c ==> '"'
```

Integer values can be stored in ```char``` variables. If the value is within a meaningful range, it also corresponds to the **ascii** value of a keyboard character. 

```java
	jshell> char cn = 65;
	cn ==> 'A'
```

Integer arithmetic can be performed on `char` data.

```java
	jshell> cn++
	$1 ==> 'A'
	jshell> cn
	$2 ==> 'B'
	jshell> ++cn
	$3 ==> 'C'
	jshell> cn + 5
	$4 ==> 72
	jshell> cn
	cn ==> 'C'
	jshell> (int)cn
	cn ==> 67
	jshell>

```


#### Summary

In this step, we:

* Were introduced the the ```char``` data type
* Learned that Unicode takes the character set beyond your keyboard
* An ascii character is ```char``` value, encoded by an integer value

### Step 11: Programming Exercise PE-02

#### Exercise Set

1. Write a Java class ```MyChar``` that is a special type of ```char```. An object of type ```MyChar``` is created round an input ```char``` data element, and has operations that do the following:
	* Check if the input character is a:
		* Numeric Digit
		* Letter of the Alphabet
		* Vowel (Either upper-case or lower-case)
		* Consonant (Either upper-case or lower-case) NOTE: A letter is a consonant if not a vowel
	* Print all the letters of the Alphabet in
		* Upper-Case
		* Lower-Case

In Essence, a runner ```class``` for ```MyChar``` would have its ```main``` method run code similar to:

```java

	MyChar myChar = new MyChar('c');
	System.out.println(myChar.isDigit());
	System.out.println(myChar.isAlphabet());
	System.out.println(myChar.isVowel());
	System.out.println(myChar.isConsonant());
	myChar.printLowerCaseAlphabets();
	myChar.printUpperCaseAlphabets();

```

### Step 12: Solution To PE-02, Part 1 - ```isVowel()```

**_MyCharRunner.java_**

```java

	package com.in28minutes.primitive.datatypes;

	public class MyCharRunner {
		public static void main(String[] args) {
			MyChar myChar = new MyChar('c');
			System.out.println(myChar.isVowel());
		}
	}

```

**_MyChar.java_**

```java

	package com.in28minutes.primitive.datatypes;
	
	public class MyChar {
		private char ch;
		
		public MyChar(char ch) {
			this.ch = ch;
		}

		public boolean isVowel() {
			if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
				return true;
			} 
			if(ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
				return true;
			}
			return false;
		}
	}

```

**_Console Output_** :

_false_

### Step 13: Solution To PE-02, Part 2 - ```isDigit()```

**_MyCharRunner.java_**

```java

	package com.in28minutes.primitive.datatypes;

	public class MyCharRunner {
		public static void main(String[] args) {
			MyChar myChar = new MyChar('c');
			System.out.println(myChar.isDigit());
			System.out.println(myChar.isVowel());
		}
	}

```

**_MyChar.java_**

```java

	package com.in28minutes.primitive.datatypes;

	public class MyChar {
		private char ch;

		public MyChar(char ch) {
			this.ch = ch;
		}

		public boolean isVowel() {
			if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
				return true;
			} 

			if(ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
				return true;
			}
			return false;
		}

		public boolean isDigit() {
			if(ch >= 48 && ch <= 57) {
				return true;
			}
			return false;
		}

}

```

**_Console Output_** :

_false_

_false_

### Step 14: Solution To PE-02, Part 3 - Other Methods

**_MyCharRunner.java_**

```java

	package com.in28minutes.primitive.datatypes;
	
	public class MyCharRunner {
		public static void main(String[] args) {
			MyChar myChar = new MyChar('c');
			System.out.println(myChar.isDigit());
			System.out.println(myChar.isAlphabet());
			System.out.println(myChar.isVowel());
			System.out.println(myChar.isConsonant());
			myChar.printLowerCaseAlphabets();
			myChar.printUpperCaseAlphabets();
		}
	}

```

**_MyChar.java_**

```java

	package com.in28minutes.primitive.datatypes;

	public class MyChar {
		private char ch;
		
		public MyChar(char ch) {
			this.ch = ch;
		}

		public boolean isVowel() {
			if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
				return true;
			} 
			if(ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
				return true;
			}
			return false;
		}

		public boolean isConsonant() {
			if(isAlphabet() && !(isVowel())) {
				return true;
			}
			return false;
		}

		public boolean isDigit() {
			if(ch >= 48 && ch <= 57) {
				return true;
			}
			return false;
		}

		public boolean isAlphabet() {
			if(ch >= 97 && ch <= 122) {
				return true;
			}
			if(ch >= 65 && ch <= 90) {
				return true;
			}
			return false;
		}

		public void printLowerCaseAlphabets() {
			for(char ch='a'; ch <= 'z'; ch++) {
				System.out.println(ch);
			}
		}

		public void printUpperCaseAlphabets() {
			for(char ch='A'; ch <= 'Z'; ch++) {
				System.out.println(ch);
			}
		}
	}

```

**_Console Output_** :

_false_

_true_

_false_

_true_

a

b

c

d

e

f

g

h

i

j

k

l

m

n

o

p

q

r

s

t

u

v

w

x

y

z

A

B

C

D

E

F

G

H

I

J

K

L

M

N

O

P

Q

R

S

T

U

V

W

X

Y

Z

### Step 15: The Primitive Types - A Review

In this section, we built on our knowledge of the primitive Java types. 

* We first got familiar with built-in wrappers for the integer types, that store useful type information. 
* Going from the integer to the floating-point types, we examined type compatibility, and how the compiler warns you about common pitfalls. We used explicit casts to force type conversions, and learned that implicit type conversions are quite common.
* We moved on to the ```BigDecimal``` class, a floating-point type with greater precision and accuracy. 
* Next in line was ```boolean```, where we built on what we know of logical expressions. We focused on the logical operators, more so on short-circuit evaluation of their expressions. 
* We saw how dependency on side-effects, and on lazy evaluation, is not a good programming practice.
* Finally, we got to the ```char``` type, and were pleasantly surprised to know, that the keyboard is not the limit.
