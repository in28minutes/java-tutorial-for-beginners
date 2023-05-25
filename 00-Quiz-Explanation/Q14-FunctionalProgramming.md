**Step 01: Introducing Functional Programming**

**Question 1: What is the purpose of functional programming?**

- A) To loop around a list and print its content.
  - `Incorrect: While functional programming can certainly accomplish this task, it isn't the purpose of functional programming.`

- B) To focus on the "how" of programming.
  - `Incorrect: Functional programming focuses more on the "what" rather than the "how" of programming.`

- C) To focus on the "what" of programming.
  - `Correct: Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. It is a declarative type of programming style that focuses on "what" to solve rather than "how" to solve.`

**Question 2: What is the output of the following code?**

- A) Apple, Banana, Cat, Dog
  - `Correct: The for-each loop iterates over each element in the list, and prints each element to the console. Therefore, all the elements in the list are printed.`

- B) Apple
  - `Incorrect: Although "Apple" is the first element in the list, the loop iterates over the entire list, not just the first element.`

- C) Banana, Cat, Dog
  - `Incorrect: The loop iterates over the entire list, so "Apple" will be printed as well.`

**Question 3: How does functional programming differ from the approach shown in Snippet-01?**

- A) It allows us to loop around a list.
  - `Incorrect: Both functional programming and the traditional approach can loop around a list.`

- B) It focuses on the "what" of programming.
  - `Correct: Functional programming is a declarative style of programming that emphasizes the "what" of programming (what you want to achieve) instead of the "how" (how the computer should do it). The traditional approach shown in Snippet-01, on the other hand, focuses more on the "how".`

- C) It accesses individual elements of a list.
  - `Incorrect: Both functional programming and the traditional approach can access individual elements of a list.`

**Step 02: Looping Through A List**

**Question 1: What does the following code do?**

- A) Prints the list of numbers.
  - `Correct: The forEach() method is applied to each element in the stream, and for each element, System.out.println(elem) is executed, which prints the element.`

- B) Filters the stream based on some logic.
  - `Incorrect: The code doesn't apply any filter to the stream. If there were a filter() method call, it would filter the stream.`

- C) Passes a function as a method argument.
  - `Correct: The lambda expression (elem -> System.out.println(elem)) is essentially a function that is passed as an argument to the forEach() method. Therefore, this statement is also correct.`

**Question 2: What is the purpose of using a lambda expression in the code?**

- A) To iterate over the list.
  - `Incorrect: While it's true that the lambda expression is used in the context of iteration, it's not used to perform the iteration itself.`

- B) To filter the stream elements.
  - `Incorrect: The lambda expression in this case doesn't perform any filtering. It's used to execute a function (printing) for each element.`

- C) To execute a function for each element.
  - `Correct: The lambda expression represents a function that is executed for each element in the stream.`

**Question

 3: What is the output of the following code?**

- A) 1, 7, 9
  - `Correct: The filter() method filters the stream so that only the numbers that are odd (num % 2 == 1) remain. Therefore, 1, 7, and 9 are printed.`

- B) 4
  - `Incorrect: The number 4 is even and is filtered out by the filter() method.`

- C) 1, 4, 7, 9
  - `Incorrect: The filter() method filters out the even number (4), so it's not printed.`


**Step 03: Filtering Results**

**Question 1: What is the purpose of the filter() method?**

- A) To loop around a list and print its content.
  - `Incorrect: The filter() method does not print its content nor iterate over the list, it applies a Predicate (a function returning a boolean) on each element and filters those which return true.`

- B) To filter the stream elements based on some logic.
  - `Correct: The filter() method applies a Predicate to each element of the stream and filters (keeps) those for which the Predicate returns true.`

- C) To focus on the "what" of programming.
  - `Incorrect: While functional programming as a whole focuses on the "what", the filter() method specifically applies a condition to filter elements from a stream.`

**Question 2: What is the output of the following code?**

- A) Apple, Bat, Cat, Dog
  - `Incorrect: The filter() method is used to keep only the elements that end with "at", so "Apple" and "Dog" are not printed.`

- B) Bat, Cat
  - `Correct: The filter() method is used to keep only the elements that end with "at", so "Bat" and "Cat" are printed.`

- C) Cat
  - `Incorrect: Both "Bat" and "Cat" end with "at", so both are printed.`

**Question 3: How would you filter the list of numbers to print only the even numbers?**

- A) list.stream().filter(num -> num%2 == 0)
  - `Correct: This lambda expression checks if a number is even (the remainder of the division by 2 is 0), so it filters the even numbers.`

- B) list.stream().filter(num -> num%2 == 1)
  - `Incorrect: This lambda expression checks if a number is odd (the remainder of the division by 2 is 1), so it filters the odd numbers.`

- C) list.stream().filter(num -> num%2 == 2)
  - `Incorrect: The remainder of the division of any number by 2 can only be 0 or 1, never 2, so this filter would not match any number.`

**Step 05: Streams - Aggregated Results**

**Question 1: What is the purpose of the reduce() method in functional programming?**

- A) To loop around a list and print its content.
  - `Incorrect: The reduce() method is not for printing content or looping around a list, but for aggregating the elements of a stream into a single result.`

- B) To filter the stream elements based on some logic.
  - `Incorrect: The reduce() method is not for filtering elements, but for aggregating them into a single result.`

- C) To aggregate data into a single result.
  - `Correct: The reduce() method is used to perform an operation that combines all elements of a stream into a single result.`

**Question 2: What is the output of the following code?**

- A) 49
  - `Correct: The reduce() method applies a lambda expression that adds together all numbers in the list, and their sum is 49.`

- B) 31
  - `Incorrect: The sum of the numbers in the list is 49, not 31.`

- C) 34
  - `Incorrect: The sum of the numbers in the list is 49, not 34.`

**Question 3: How does the reduce() method work in the given code?**

- A) It adds all

 the numbers in the list.
  - `Correct: The reduce() method applies a lambda expression that sums the numbers. It starts with the initial value (0), then adds each element of the stream.`

- B) It filters the even numbers in the list.
  - `Incorrect: The reduce() method does not filter elements, it aggregates them into a single result.`

- C) It applies a lambda expression to aggregate the numbers.
  - `Correct: The reduce() method indeed uses a lambda expression (num1, num2) -> num1 + num2, which sums the numbers, to aggregate the elements of the stream.`



**Step 06: Functional Programming v Structured Programming**

**Question 1: What is the difference between Structured Programming (SP) and Functional Programming (FP) in terms of mutations?**

- A) SP involves mutations, while FP avoids mutations.
  - `Correct: Structured programming often involves changing the state or mutating variables, while functional programming tends to avoid mutations and promotes immutability.`

- B) SP doesn't involve mutations, while FP allows mutations.
  - `Incorrect: Structured programming often involves mutating variables, while functional programming promotes immutability and avoids mutation.`

- C) Both SP and FP involve mutations.
  - `Incorrect: Functional programming discourages mutation and promotes immutability, while structured programming may involve mutation.`

**Question 2: How does SP differ from FP in terms of specifying the computation?**

- A) SP specifies both what to do and how to do it.
  - `Correct: Structured programming often focuses on the steps to achieve the result (the "how"), in addition to the result itself (the "what").`

- B) FP specifies what to do, but not how to do it.
  - `Correct: Functional programming focuses on the desired result (the "what"), and not on the steps to achieve it (the "how").`

- C) Both SP and FP specify what to do and how to do it.
  - `Incorrect: While structured programming often specifies both the "what" and the "how", functional programming typically focuses on the "what".`

**Question 3: Which method in the given code follows the Functional Programming (FP) approach?**

Without seeing the given code, I can't answer this question definitively. However, assuming that `basicSum()` follows a structured programming approach and `fpSum()` follows a functional programming approach, the correct answer would be:

- B) fpSum()

**Step 07: Some FP Terminology**

**Question 1: What is a lambda expression in functional programming?**

- A) A method that performs a specific computation.
  - `Incorrect: While a lambda expression can represent a function that performs a specific computation, it's not the same as a method. Methods have a name and are defined inside classes, while lambda expressions are anonymous and can be passed as arguments.`

- B) A sequence of elements in a stream.
  - `Incorrect: A lambda expression is not a sequence of elements in a stream, it's a function or a piece of behavior that can be passed as an argument.`

- C) A concise way to represent a function or behavior.
  - `Correct: A lambda expression is a concise representation of a function, which can be used where a function is expected as an argument.`

**Question 2: How is a lambda expression different from a regular method?**

- A) A lambda expression cannot have multiple lines of code.
  - `Incorrect: Lambda expressions can indeed have multiple lines of code, if enclosed in braces. However, they are usually used for short, concise pieces of functionality.`

- B) A lambda expression cannot take any parameters.
  - `Incorrect: Lambda expressions can take parameters, just like regular methods.`

- C) A lambda expression is a more concise representation of a method.
  - `Correct: A lambda expression is indeed a more concise representation of a function or method, often used for passing behaviors as arguments.`

**Question 3: What are intermediate operations and terminal operations in streams?**

- A) Intermediate operations produce a single result, while terminal operations produce another stream of elements.
  - `Incorrect: Intermediate operations produce another stream, while terminal operations produce a single result or a collection.`

- B) Intermediate operations

 take a stream and return a single result, while terminal operations take a stream and produce another stream of elements.
  - `Incorrect: This is reversed. Intermediate operations produce another stream, while terminal operations produce a single result or a collection.`

- C) Intermediate operations modify the stream, while terminal operations produce a single result or a collection of objects.
  - `Correct: Intermediate operations like filter() and map() transform the stream, while terminal operations like collect(), reduce(), or forEach() produce a single result or a collection, or have a side effect like printing to the console.`

**Step 08: Intermediate Stream Operations**

**Question 1: What is the purpose of the sorted() method in stream operations?**

- A) To filter the stream elements based on some logic.
  - `Incorrect: The sorted() method does not filter elements. It sorts them in natural order.`

- B) To preserve the elements in natural sorted order.
  - `Correct: The sorted() method returns a stream consisting of the elements of the original stream, sorted in their natural order.`

- C) To compute new results from the input stream elements.
  - `Incorrect: The sorted() method does not compute new results, it sorts the elements in their natural order.`

**Question 2: What is the purpose of the distinct() method in stream operations?**

- A) To sort the stream elements in ascending order.
  - `Incorrect: The distinct() method does not sort elements, it eliminates duplicates.`

- B) To return only the unique elements of the input stream.
  - `Correct: The distinct() method returns a stream consisting of the unique elements of the original stream.`

- C) To compute the square of each element in the input stream.
  - `Incorrect: The distinct() method does not compute squares, it eliminates duplicates.`

**Question 3: What is the output of the following code?**

- A) 3, 5, 7, 45, 213
  - `Correct: This is the output of the code. The distinct() method removes duplicates, and sorted() orders the unique numbers.`

- B) 3, 5, 213, 45, 7
  - `Incorrect: The numbers are not correctly sorted in this option.`

- C) 3, 3, 5, 5, 7, 45, 213
  - `Incorrect: This option does not remove duplicates as distinct() would.`



**Step 09: Programming Exercise FP-PE-01**

**Question 1: What is the purpose of the map() method in the printFPSquares() method?**

- A) To filter the stream elements based on some logic.
  - `Incorrect: The map() method doesn't filter elements, it transforms them. It takes a function as an argument and applies it to each element of the stream, producing a new stream.`

- B) To preserve the elements in natural sorted order.
  - `Incorrect: The map() method doesn't sort elements. It transforms each element in the stream according to a function.`

- C) To compute the square of each element in the input stream.
  - `Correct: In this context, the map() method is being used to transform each number in the stream to its square.`

**Question 2: How would you modify the printLowerCases() method to print all the strings in lowercase?**

- A) Use the map() method with a lambda expression to convert each string to lowercase.
  - `Correct: This is the right approach. By using map() method with a lambda expression String::toLowerCase, we can transform each string in the stream to its lowercase equivalent.`

- B) Use the filter() method with a lambda expression to filter out lowercase strings.
  - `Incorrect: The filter() method is used to select elements from the stream that satisfy a certain condition, not to transform elements.`

- C) Use the sorted() method with a lambda expression to sort the strings in lowercase order.
  - `Incorrect: The sorted() method is used to sort elements in the stream, not to transform them.`

**Question 3: How does the printLengths() method calculate the length of each string?**

- A) It uses the filter() method with a lambda expression to filter out strings based on their length.
  - `Incorrect: The filter() method is not involved in calculating the length of the strings. It is used for selecting elements from a stream that satisfy a certain condition.`

- B) It uses the sorted() method with a lambda expression to sort the strings based on their length.
  - `Incorrect: The sorted() method is not involved in calculating the length of the strings. It's used to sort elements in a stream.`

- C) It uses the map() method with a lambda expression to transform each string into its length.
  - `Correct: The map() method is being used to transform each string in the stream to its length.`

**Step 10: Terminal Operations**

**Question 1: What does the reduce() method do in terminal operations?**

- A) It sorts the stream elements in ascending order.
  - `Incorrect: The reduce() method doesn't sort elements, it combines them into a single result according to a provided binary operator.`

- B) It returns a single result by combining the elements of the stream.
  - `Correct: The reduce() method takes a binary operator and uses it to combine the elements of the stream into a single result.`

- C) It returns only the unique elements of the input stream.
  - `Incorrect: The reduce() method doesn't filter out unique elements. It combines all elements of a stream into a single result.`

**Question 2: How does the max() method differ from reduce() in the given code?**

- A) max() returns the maximum element from the stream, while reduce() combines all the elements into a single result.
  - `Correct: The max() method returns the maximum element according to a provided comparator, while the reduce() method combines all elements into a single result using a provided binary operator.`

- B) max() sorts the stream

 elements in ascending order, while reduce() sorts them in descending order.
  - `Incorrect: Neither max() nor reduce() sort elements. max() finds the maximum element, and reduce() combines all elements into a single result.`

- C) max() applies a lambda expression to compute a single result, while reduce() applies a different lambda expression.
  - `Partly Correct: Both methods can work with lambda expressions, but they serve different purposes. max() finds the maximum element, and reduce() combines elements.`

**Question 3: What is the purpose of the Optional type in stream operations?**

- A) To provide an alternative result when the stream is empty.
  - `Correct: Optional is a container that can contain a non-null value or be empty. It's used in stream operations to avoid NullPointerException and to express that a result may not exist (for example, finding a maximum in an empty list).`

- B) To handle null values in the stream elements.
  - `Incorrect: Optional is not designed to handle null values within the stream elements. It's more about expressing the absence of a result.`

- C) To convert the stream into a collection.
  - `Incorrect: Optional is not used for converting streams into collections. It's used to represent a value that might be null.`

**Step 11: More Stream Operations**

**Question 1: What is the output of the following code?**

- A) [23, 12, 34, 53]
  - `Incorrect: This option includes all numbers, not just the even ones.`

- B) [12, 34]
  - `Correct: The code filters out the even numbers (12 and 34) from the input list.`

- C) [23, 53]
  - `Incorrect: This option includes the odd numbers from the list, not the even ones.`

**Question 2: How would you modify the code to create a list of the odd numbers from the numbers list?**

- A) Change the condition in the lambda expression to n%2==1.
  - `Correct: Changing the condition in the filter method to n%2==1 will select the odd numbers.`

- B) Replace filter() with sorted() method.
  - `Incorrect: The sorted() method sorts elements but doesn't filter them.`

- C) Use map() instead of filter().
  - `Incorrect: The map() method transforms elements but doesn't filter them.`

**Question 3: What is the purpose of the collect() method in stream operations?**

- A) To compute a single result by combining the elements of the stream.
  - `Incorrect: While collect() can be used to produce a single result (such as counting elements), its primary purpose is to transform the stream into a different form, often a collection.`

- B) To convert the stream into a collection or other data structure.
  - `Correct: The collect() method is a terminal operation that transforms the elements of the stream into a different form, often a collection (like a List, Set, or Map).`

- C) To filter the stream elements based on some logic.
  - `Incorrect: The collect() method doesn't filter elements. It's a terminal operation used to collect the elements of a stream into a collection or other data structure. Filtering is usually done before the collect() method, using the filter() method.`



**Step 12: The Optional class**

**Question 1: What does the Optional<T> class represent in stream operations?**

- A) It represents a nullable result from a terminal stream operation.
  - `Correct: Optional<T> is a container object which may or may not contain a non-null value. It is used to represent the result of a computation that might return a value or might not (like when you're looking for the maximum of an empty list).`

- B) It represents an intermediate stream operation.
  - `Incorrect: Optional<T> doesn't represent an operation, it's a class used to represent the result of a computation that may or may not produce a result.`

- C) It represents a lambda expression in functional programming.
  - `Incorrect: Optional<T> doesn't represent a lambda expression, it's a class used to encapsulate a result that might be present or not.`

**Question 2: How can you check if an Optional<T> object contains a valid result?**

- A) By calling the get() method on the object.
  - `Incorrect: While the get() method can be used to obtain the value contained within an Optional, it's not a safe way to check for a value because it will throw a NoSuchElementException if the Optional is empty.`

- B) By invoking the isPresent() method on the object.
  - `Correct: The isPresent() method can be used to check if an Optional contains a value.`

- C) By using the orElse() method with a default value.
  - `Incorrect: The orElse() method is used to provide a default value when the Optional is empty, but it's not used to check if an Optional contains a value.`

**Question 3: What does the orElse() method do in the context of Optional<T>?**

- A) It returns the maximum element from the stream.
  - `Incorrect: The orElse() method provides a default value to return when the Optional is empty. It has nothing to do with finding the maximum value.`

- B) It handles exceptions during stream operations.
  - `Incorrect: While it does prevent a NoSuchElementException from being thrown when the Optional is empty, the orElse() method primarily serves to provide a default value.`

- C) It provides a default value if the result is empty.
  - `Correct: The orElse() method returns the value in the Optional if it's present, otherwise it returns a default value that is provided as an argument.`

  
**Step 13: Functional Interfaces: Predicate**

**Question 1: What is a functional interface in Java?**

- A) An interface that contains only one abstract method.
  - `Correct: A functional interface in Java is an interface that contains exactly one abstract method.`

- B) An interface that can be used to define lambda expressions.
  - `Correct: Functional interfaces can be used as targets for lambda expressions and method references.`

- C) An interface that represents a logical condition or test.
  - `Incorrect: This describes the Predicate functional interface specifically, but not functional interfaces in general.`

**Question 2: What is the purpose of the Predicate<T> interface in stream operations?**

- A) It is used to collect the elements of a stream into a list.
  - `Incorrect: Predicate<T> is used in operations like filter(), which select elements based on a condition, not to collect elements.`

- B) It is used to filter elements based on a logical condition.
  - `Correct: Predicate<T> is used to create a condition that returns true or false. In the context of stream operations, it is used for methods like filter().`

- C) It is used to

 calculate a single result from a stream.
  - `Incorrect: Predicate<T> is used to evaluate conditions, not to combine or calculate results.`

**Question 3: How can you use a lambda expression to implement a Predicate?**

- A) By overriding the test() method in the Predicate interface.
  - `Incorrect: In a sense, using a lambda expression does implicitly "override" the test() method, but you do not explicitly override methods when using lambda expressions.`

- B) By implementing the Predicate interface directly in a class.
  - `Incorrect: While you can do this, it's not an example of using a lambda expression.`

- C) By calling the filter() method with a lambda expression as an argument.
  - `Correct: The filter() method takes a Predicate as an argument. This is often supplied as a lambda expression.`

**Step 14: Functional Interfaces: Consumer**

**Question 1: What is the purpose of the Consumer<S> interface in stream operations?**

- A) It is used to filter elements based on a logical condition.
  - `Incorrect: The Consumer<S> interface is not used for filtering elements, it is used for performing an action on each element of a stream.`

- B) It is used to perform an action on each element of the stream.
  - `Correct: The Consumer<S> interface is used to define an operation that takes one input argument and returns no result. It is used in the context of stream operations to perform an action on each element.`

- C) It is used to transform the elements of the stream.
  - `Incorrect: The Consumer<S> interface is not used for transforming elements, it is used for performing an action on each element.`

**Question 2: How can you implement a custom Consumer interface?**

- A) By overriding the test() method in the Consumer interface.
  - `Incorrect: The Consumer interface does not have a test() method to override. It has an accept() method.`

- B) By implementing the Consumer interface directly in a class.
  - `Correct: You can create a class that implements the Consumer interface and overrides the accept() method. However, it is often easier and more concise to use a lambda expression.`

- C) By using a lambda expression as an argument to the forEach() method.
  - `Correct: The forEach() method in the Stream interface takes a Consumer as an argument. This is often supplied as a lambda expression, which defines the action to be performed on each element.`

**Question 3: What does the accept() method of the Consumer interface do?**

- A) It applies a transformation to the input element.
  - `Incorrect: The accept() method performs an action on its input. It does not return a value, so it cannot transform the input.`

- B) It performs an action on the input element.
  - `Correct: The accept() method of the Consumer interface takes an argument and performs an operation on it. It doesn't return a result.`

- C) It filters the input element based on a condition.
  - `Incorrect: The accept() method performs an action on its input. It doesn't return a boolean value, so it can't filter based on a condition.`

  
  **Step 15: More Functional Interfaces**

**Question 1: What is the purpose of the map() operation in stream operations?**

- A) It is used to filter the elements of a stream based on a condition.
  - `Incorrect: The map() operation is used to transform elements in a stream, not to filter them.`

- B) It is used to transform the elements of a stream using a lambda expression.
  - `Correct: The map() operation applies a function to each element in a stream and produces a new stream with the transformed elements.`

- C) It is used to combine the elements of a stream into a single result.
  - `Incorrect: The map() operation transforms elements but doesn't combine them into a single result. That role is fulfilled by operations like reduce().`

**Question 2: What is the signature of the map() operation in the Stream interface?**

- A) <R> Stream<R> map(Function<? super T, ? extends R> mapper)
  - `Correct: The map() method in the Stream interface takes a Function as a parameter, which is applied to each element in the stream, and it returns a new Stream with the results.`

- B) <T> Stream<T> map(Predicate<T> predicate)
  - `Incorrect: The map() method doesn't take a Predicate as a parameter. It takes a Function.`

- C) <S> Stream<S> map(Consumer<? super S> action)
  - `Incorrect: The map() method doesn't take a Consumer as a parameter. It takes a Function.`

**Question 3: What is the purpose of the apply() method in the Function interface?**

- A) It performs an action on the input element.
  - `Incorrect: The apply() method applies a transformation to the input element, but it doesn't just perform an action on it; it produces a result.`

- B) It filters the input element based on a condition.
  - `Incorrect: The apply() method doesn't filter elements based on a condition. It applies a transformation to its input.`

- C) It applies a transformation to the input element.
  - `Correct: The apply() method of the Function interface takes an argument and applies a function to it, producing a result.`

**Step 16: Introducing Method References**

**Question 1: What is a method reference in Java?**

- A) It is a reference to a static method or an instance method.
  - `Correct: A method reference can refer to a static method, an instance method of a particular object, an instance method of an arbitrary object of a particular type, or a constructor.`

- B) It is a reference to a lambda expression.
  - `Incorrect: A method reference is an alternative syntax to a lambda expression for expressing instances of functional interfaces, but it's not a reference to a lambda expression.`

- C) It is a reference to a functional interface.
  - `Incorrect: A method reference isn't a reference to a functional interface. It's a shorthand notation for a lambda expression that calls a specific method.`

**Question 2: How can you use a method reference to replace a lambda expression?**

- A) By using the apply() method of a functional interface.
  - `Incorrect: The apply() method is a method of the Function interface, not a means to use a method reference.`

- B) By overriding the accept() method of a functional interface.
  - `Incorrect: Overriding the accept() method is a way to implement the Consumer interface, not to use a method reference.`

- C) By referring to the method directly using the :: operator.
  - `

Correct: The :: operator is used to create a method reference. This can be used to replace a lambda expression that calls a specific method.`

**Question 3: How can you use a method reference to call an instance method?**

- A) By specifying the class name followed by the method name.
  - `Incorrect: To reference an instance method, you generally need to use the :: operator and the name of the method, without the class name.`

- B) By using the apply() method of a functional interface.
  - `Incorrect: The apply() method is part of the Function interface, not a way to use a method reference.`

- C) By using the :: operator followed by the method name.
  - `Correct: To reference an instance method, you can use the :: operator followed by the method name.`
