## Step 01: Introducing Functional Programming

**Question 1:** What is the purpose of functional programming?

- A) To loop around a list and print its content.
- B) To focus on the "how" of programming.
- C) To focus on the "what" of programming.

**Question 2:** What is the output of the following code?

```java
List<String> list = List.of("Apple", "Banana", "Cat", "Dog");
for(String str:list) {
    System.out.println(str);
}
```

- A) Apple, Banana, Cat, Dog
- B) Apple
- C) Banana, Cat, Dog

**Question 3:** How does functional programming differ from the approach shown in Snippet-01?

- A) It allows us to loop around a list.
- B) It focuses on the "what" of programming.
- C) It accesses individual elements of a list.

## Step 02: Looping Through A List

**Question 1:** What does the following code do?

```java
List<Integer> list = List.of(1, 4, 7, 9);
list.stream().forEach(elem -> System.out.println(elem));
```

- A) Prints the list of numbers.
- B) Filters the stream based on some logic.
- C) Passes a function as a method argument.

**Question 2:** What is the purpose of using a lambda expression in the code?

- A) To iterate over the list.
- B) To filter the stream elements.
- C) To execute a function for each element.

**Question 3:** What is the output of the following code?

```java
List<Integer> list = List.of(1, 4, 7, 9);
list.stream().filter(num -> num%2 == 1).forEach(elem -> System.out.println(elem));
```

- A) 1, 7, 9
- B) 4
- C) 1, 4, 7, 9

## Step 03: Filtering Results

**Question 1:** What is the purpose of the `filter()` method?

- A) To loop around a list and print its content.
- B) To filter the stream elements based on some logic.
- C) To focus on the "what" of programming.

**Question 2:** What is the output of the following code?

```java
List<String> list = List.of("Apple", "Bat", "Cat", "Dog");
list.stream()
    .filter(elem -> elem.endsWith("at"))
    .forEach(element -> System.out.println(element));
```

- A) Apple, Bat, Cat, Dog
- B) Bat, Cat
- C) Cat

**Question 3:** How would you filter the list of numbers to print only the even numbers?

- A) `list.stream().filter(num -> num%2 == 0)`
- B) `list.stream().filter(num -> num%2 == 1)`
- C) `list.stream().filter(num -> num%2 == 2)`

## Step 05: Streams - Aggregated Results

**Question 1:** What is the purpose of the `reduce()` method in functional programming?

- A) To loop around a list and print its content.
- B) To filter the stream elements based on some logic.
- C) To aggregate data into a single result.

**Question 2:** What is the output of the following code?

```java
List<Integer> numbers = List.of(4, 6, 8, 13, 3, 15);
int sum = numbers.stream()
                 .reduce(0, (num1, num2) -> num1 + num2);
System.out.println(sum);
```

- A) 49
- B) 31
- C) 34

**Question 3:** How does the `reduce()` method work in the given code?

- A) It adds all the numbers in the list.
- B) It filters the even numbers in the list.
- C) It applies a lambda expression to aggregate the numbers.

## Step 06: Functional Programming v Structured Programming

**Question 1:** What is the difference between Structured Programming (SP) and Functional Programming (FP) in terms of mutations?

- A) SP involves mutations, while FP avoids mutations.
- B) SP doesn't involve mutations, while FP allows mutations.
- C) Both SP and FP involve mutations.

**Question 2:** How does SP differ from FP in terms of specifying the computation?

- A) SP specifies both what to do and how to do it.
- B) FP specifies what to do, but not how to do it.
- C) Both SP and FP specify what to do and how to do it.

**Question 3:** Which method in the given code follows the Functional Programming (FP) approach?

- A) `basicSum()`
- B) `fpSum()`
- C) Both `basicSum()` and `fpSum()`

## Step 07: Some FP Terminology

**Question 1:** What is a lambda expression in functional programming?

- A) A method that performs a specific computation.
- B) A sequence of elements in a stream.
- C) A concise way to represent a function or behavior.

**Question 2:** How is a lambda expression different from a regular method?

- A) A lambda expression cannot have multiple lines of code.
- B) A lambda expression cannot take any parameters.
- C) A lambda expression is a more concise representation of a method.

**Question 3:** What are intermediate operations and terminal operations in streams?

- A) Intermediate operations produce a single result, while terminal operations produce another stream of elements.
- B) Intermediate operations take a stream and return a single result, while terminal operations take a stream and produce another stream of elements.
- C) Intermediate operations modify the stream, while terminal operations produce a single result or a collection of objects.



## Step 08: Intermediate Stream Operations

**Question 1:** What is the purpose of the `sorted()` method in stream operations?

- A) To filter the stream elements based on some logic.
- B) To preserve the elements in natural sorted order.
- C) To compute new results from the input stream elements.

**Question 2:** What is the purpose of the `distinct()` method in stream operations?

- A) To sort the stream elements in ascending order.
- B) To return only the unique elements of the input stream.
- C) To compute the square of each element in the input stream.

**Question 3:** What is the output of the following code?

```java
List<Integer> numbers = List.of(3, 5, 3, 213, 45, 5, 7);
numbers.stream().distinct().sorted().forEach(elem -> System.out.println(elem));
```

- A) 3, 5, 7, 45, 213
- B) 3, 5, 213, 45, 7
- C) 3, 3, 5, 5, 7, 45, 213

## Step 09: Programming Exercise FP-PE-01

**Question 1:** What is the purpose of the `map()` method in the `printFPSquares()` method?

- A) To filter the stream elements based on some logic.
- B) To preserve the elements in natural sorted order.
- C) To compute the square of each element in the input stream.

**Question 2:** How would you modify the `printLowerCases()` method to print all the strings in lowercase?

- A) Use the `map()` method with a lambda expression to convert each string to lowercase.
- B) Use the `filter()` method with a lambda expression to filter out lowercase strings.
- C) Use the `sorted()` method with a lambda expression to sort the strings in lowercase order.

**Question 3:** How does the `printLengths()` method calculate the length of each string?

- A) It uses the `filter()` method with a lambda expression to filter out strings based on their length.
- B) It uses the `sorted()` method with a lambda expression to sort the strings based on their length.
- C) It uses the `map()` method with a lambda expression to transform each string into its length.

## Step 10: Terminal Operations

**Question 1:** What does the `reduce()` method do in terminal operations?

- A) It sorts the stream elements in ascending order.
- B) It returns a single result by combining the elements of the stream.
- C) It returns only the unique elements of the input stream.

**Question 2:** How does the `max()` method differ from `reduce()` in the given code?

- A) `max()` returns the maximum element from the stream, while `reduce()` combines all the elements into a single result.
- B) `max()` sorts the stream elements in ascending order, while `reduce()` sorts them in descending order.
- C) `max()` applies a lambda expression to compute a single result, while `reduce()` applies a different lambda expression.

**Question 3:** What is the purpose of the `Optional` type in stream operations?

- A) To provide an alternative result when the stream is empty.
- B) To handle null values in the stream elements.
- C) To convert the stream into a collection.


## Step 11: More Stream Operations

**Question 1:** What is the output of the following code?

```java
List<Integer> numbers = List.of(23, 12, 34, 53);
List<Integer> evens = numbers.stream()
                             .filter(n -> n%2==0)
                             .collect(Collectors.toList());
System.out.println(evens);
```

- A) [23, 12, 34, 53]
- B) [12, 34]
- C) [23, 53]

**Question 2:** How would you modify the code to create a list of the odd numbers from the `numbers` list?

- A) Change the condition in the lambda expression to `n%2==1`.
- B) Replace `filter()` with `sorted()` method.
- C) Use `map()` instead of `filter()`.

**Question 3:** What is the purpose of the `collect()` method in stream operations?

- A) To compute a single result by combining the elements of the stream.
- B) To convert the stream into a collection or other data structure.
- C) To filter the stream elements based on some logic.

## Step 12: The Optional<T> class

**Question 1:** What does the `Optional<T>` class represent in stream operations?

- A) It represents a nullable result from a terminal stream operation.
- B) It represents an intermediate stream operation.
- C) It represents a lambda expression in functional programming.

**Question 2:** How can you check if an `Optional<T>` object contains a valid result?

- A) By calling the `get()` method on the object.
- B) By invoking the `isPresent()` method on the object.
- C) By using the `orElse()` method with a default value.

**Question 3:** What does the `orElse()` method do in the context of `Optional<T>`?

- A) It returns the maximum element from the stream.
- B) It handles exceptions during stream operations.
- C) It provides a default value if the result is empty.

## Step 13: Functional Interfaces: Predicate

**Question 1:** What is a functional interface in Java?

- A) An interface that contains only one abstract method.
- B) An interface that can be used to define lambda expressions.
- C) An interface that represents a logical condition or test.

**Question 2:** What is the purpose of the `Predicate<T>` interface in stream operations?

- A) It is used to collect the elements of a stream into a list.
- B) It is used to filter elements based on a logical condition.
- C) It is used to calculate a single result from a stream.

**Question 3:** How can you use a lambda expression to implement a `Predicate`?

- A) By overriding the `test()` method in the `Predicate` interface.
- B) By implementing the `Predicate` interface directly in a class.
- C) By calling the `filter()` method with a lambda expression as an argument.



## Step 14: Functional Interfaces: Consumer

**Question 1:** What is the purpose of the `Consumer<S>` interface in stream operations?

- A) It is used to filter elements based on a logical condition.
- B) It is used to perform an action on each element of the stream.
- C) It is used to transform the elements of the stream.

**Question 2:** How can you implement a custom `Consumer` interface?

- A) By overriding the `test()` method in the `Consumer` interface.
- B) By implementing the `Consumer` interface directly in a class.
- C) By using a lambda expression as an argument to the `forEach()` method.

**Question 3:** What does the `accept()` method of the `Consumer` interface do?

- A) It applies a transformation to the input element.
- B) It performs an action on the input element.
- C) It filters the input element based on a condition.

## Step 15: More Functional Interfaces

**Question 1:** What is the purpose of the `map()` operation in stream operations?

- A) It is used to filter the elements of a stream based on a condition.
- B) It is used to transform the elements of a stream using a lambda expression.
- C) It is used to combine the elements of a stream into a single result.

**Question 2:** What is the signature of the `map()` operation in the `Stream` interface?

- A) `<R> Stream<R> map(Function<? super T, ? extends R> mapper)`
- B) `<T> Stream<T> map(Predicate<T> predicate)`
- C) `<S> Stream<S> map(Consumer<? super S> action)`

**Question 3:** What is the purpose of the `apply()` method in the `Function` interface?

- A) It performs an action on the input element.
- B) It filters the input element based on a condition.
- C) It applies a transformation to the input element.

## Step 16: Introducing Method References

**Question 1:** What is a method reference in Java?

- A) It is a reference to a static method or an instance method.
- B) It is a reference to a lambda expression.
- C) It is a reference to a functional interface.

**Question 2:** How can you use a method reference to replace a lambda expression?

- A) By using the `apply()` method of a functional interface.
- B) By overriding the `accept()` method of a functional interface.
- C) By referring to the method directly using the `::` operator.

**Question 3:** How can you use a method reference to call an instance method?

- A) By specifying the class name followed by the method name.
- B) By using the `apply()` method of a functional interface.
- C) By using the `::` operator followed by the method name.


