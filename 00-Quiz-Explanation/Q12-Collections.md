**Step 00: Collections Overview**

**Question 1: What are Collections in Java?**
- a) Collections is a package in Java `Incorrect: While there is a Collections class in Java, it is not a package.`
- b) Collections are in-built implementations available to support dynamic data structures in Java programs. `Correct: Collections in Java are data structures that hold objects and provide various operations on data including insertion, deletion, sorting, etc.`
- c) Collections are used to sort static data structures in Java programs. `Incorrect: Collections provide more than just sorting; they provide a variety of operations for managing groups of objects.`

**Question 2: What are some common collections?**
- a) List, Set, Queue, Map `Correct: These are some of the common interfaces in the Java Collections Framework.`
- b) Stack, Heap, Tree `Incorrect: These are data structures but not necessarily collection types in Java.`
- c) Graph, Queue, Hash Table `Incorrect: While Queue is a collection in Java, Graph and Hash Table aren't.`

**Question 3: What is List Interface used for?**
- a) List Interface is used to implement an ordered collection in Java programs. `Correct: List interface is used for collections that have a specific order and can contain duplicate elements.`
- b) List Interface is used to implement an unordered collection in Java programs. `Incorrect: Lists are ordered collections.`
- c) List Interface is used to implement a stack data structure in Java programs. `Incorrect: While a List could technically be used to implement a Stack, it is not its primary purpose.`

**Step 00: Comparator for ArrayList.sort()**

```java
package collections;
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Comparator;

public class StudentsCollectionRunner {
	public static void main(String[] args) {
		List<Student> students = List.of(new Student(1, "Ranga"),
										new Student(100, "Adam"),
										new Student(2, "Eve"));

		ArrayList<Student> studentsAl = new ArrayList<>(students);
		System.out.println(studentsAl);
		studentsAl.sort(new AscStudentComparator());
		System.out.println("Asc : " + studentsAl);			
		studentsAl.sort(new DescStudentComparator());
		System.out.println("Desc : " + studentsAl);
	}
}
```

**Question 1: What is the purpose of the StudentsCollectionRunner class?**
- a) To sort a list of students by their names `Incorrect: The class sorts students by their IDs, not names.`
- b) To sort a list of students by their IDs in ascending and descending order `Correct: The class uses comparators to sort a list of students by their IDs.`
- c) To create a new student object `Incorrect: Although new Student objects are created, the primary purpose is to sort them.`

**Question 2: What is the output of the following code?**

```java
ArrayList<Student> studentsAl = new ArrayList<>(students);
studentsAl.sort(new DescStudentComparator());
System.out.println("Desc : " + studentsAl);
```

- a) [100 Adam, 2 Eve, 1 Ranga] `Correct: The code sorts the Student objects in descending order of their IDs.`
- b) [1 Ranga, 2 Eve, 100 Adam] `Incorrect: This would be the output for ascending order sort, not descending.`
- c) [100 Adam, 1 Ranga, 2 Eve] `Incorrect: The order does not match the descending sort of IDs.`

**Question 3: Which interface is used to provide the custom sorting order for studentsAl?**
- a) Comparable `Incorrect: Comparable is used for natural ordering, not custom ordering.`
- b) Comparator `Correct: Comparator interface is used to define custom ordering.`
- c) Iterable `Incorrect: Iterable interface is not used for ordering.`

**Step 01: The Set interface**

**Question 1: How does the Java Set interface handle duplicates?**
- a) It stores all duplicate elements `Incorrect: Set interface doesn't allow duplicates.`
- b) It only stores the first occurrence of an element `Correct: In a Set, duplicate elements are not stored.`
- c) It throws an exception when duplicates are added `Incorrect: The Set interface doesn't throw exceptions when attempting to add duplicate elements

, it just ignores them.`

**Question 2: What does the equals method need to return for two objects to be considered equal and treated as duplicates by a Set implementation?**
- a) true `Correct: If equals method returns true, the objects are considered equal and treated as duplicates.`
- b) false `Incorrect: If equals method returns false, the objects are considered unequal.`
- c) It depends on the specific implementation `Incorrect: The equality check depends on the equals method returning true.`

**Question 3: What is one feature that is not provided by the Set interface?**
- a) Iteration over elements `Incorrect: The Set interface allows iteration over its elements.`
- b) Removing elements `Incorrect: The Set interface allows removing elements.`
- c) Positional element access `Correct: The Set interface does not support positional access like Lists do.`

**Step 02: Understanding Data Structures**
Hash Table
**Question 1: What is a hash table?**
- a) A table of sorted elements `Incorrect: Hash table is not about sorted elements.`
- b) A table of unique elements `Incorrect: While a Hash table does not allow duplicates, this description is too narrow.`
- c) A data structure that combines efficient element access and element insertion/deletion `Correct: A Hash table is a data structure that uses hash functions for efficient element access and operations.`

**Question 2: What is a bucket in a hash table?**
- a) A slot in the table where elements are inserted and chained together `Correct: In a hash table, a bucket is where elements with the same hash value are stored.`
- b) A subset of elements in the table that share the same hash value `Incorrect: It's not about subsets but about specific slots in the table.`
- c) A container used to store the hash function `Incorrect: A bucket doesn't store the hash function.`

**Step 17: PriorityQueue**
```java
Queue queue = new PriorityQueue<>();
queue.addAll(List.of("Apple", "Zebra", "Monkey", "Cat"));
```

**Question 1: What is the output of queue.poll() after adding the elements to the PriorityQueue?**
- a) "Apple" `Correct: The PriorityQueue follows natural ordering, so the first element to be polled would be "Apple".`
- b) "Zebra" `Incorrect: "Zebra" is not the first element in natural ordering.`
- c) "Cat" `Incorrect: "Cat" is not the first element in natural ordering.`
- d) "Monkey" `Incorrect: "Monkey" is not the first element in natural ordering.`

**Question 2: What is the default ordering of elements in a PriorityQueue?**
- a) Descending order `Incorrect: The default ordering is not descending.`
- b) Ascending order based on natural order `Correct: PriorityQueue orders elements in their natural ordering by default.`
- c) Insertion order `Incorrect: PriorityQueue does not maintain insertion order.`
- d) Random order `Incorrect: PriorityQueue does not use a random order.`

**Question 3: What is the output of queue.poll() after executing queue.poll() three times?**
- a) "Cat" `Incorrect: "Cat" would have already been removed after the second poll.`
- b) "Monkey" `Incorrect: "Monkey" would have already been removed after the third poll.`
- c) "Zebra" `Incorrect: "Zebra" is not the fourth element in the queue.`
- d) null `Correct: After polling three times, the fourth poll would return null because the queue is empty.`



**Step 18: Custom Priority PriorityQueue**

```java
Queue<String> queue = new PriorityQueue<>(new StringLengthComparator());
queue.addAll(List.of("Zebra", "Monkey", "Cat"));
```

**Question 1: What is the output of queue.poll() after adding the elements to the PriorityQueue?**
- a) "Zebra" `Incorrect: With the custom comparator, "Zebra" is not the shortest string.`
- b) "Monkey" `Incorrect: With the custom comparator, "Monkey" is not the shortest string.`
- c) "Cat" `Correct: With the custom comparator sorting by string length, "Cat" is the shortest and therefore polled first.`
- d) null `Incorrect: The queue is not empty at this point.`

**Question 2: What interface must be implemented to specify a custom priority order in a PriorityQueue?**
- a) Comparable `Incorrect: Comparable is used for natural ordering, not custom ordering.`
- b) Comparator `Correct: Comparator interface is used to define custom ordering.`
- c) PriorityQueue `Incorrect: PriorityQueue is a class, not an interface for custom ordering.`
- d) Queue `Incorrect: Queue is a broader interface, not specifically for custom ordering.`

**Question 3: What is the output of the following code snippet after executing queue.poll() three times?**
```java
Queue<String> queue = new PriorityQueue<>(new StringLengthComparator());
queue.addAll(List.of("Zebra", "Monkey", "Cat"));
queue.poll();
queue.poll();
queue.poll();
queue.poll();
```

- a) null `Correct: After polling three times, the fourth poll would return null because the queue is empty.`
- b) "Cat" `Incorrect: "Cat" would have already been removed after the first poll.`
- c) "Monkey" `Incorrect: "Monkey" would have already been removed after the second poll.`
- d) "Zebra" `Incorrect: "Zebra" would have already been removed after the third poll.`

**Step 19: Basic Map Operations**
```java
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
```

**Question 1: What is the size of map?**
- A. 3 `Correct: The map contains three key-value pairs, hence the size is 3.`
- B. 4 `Incorrect: The map only has three key-value pairs.`
- C. 5 `Incorrect: The map only has three key-value pairs.`
- D. 6 `Incorrect: The map only has three key-value pairs.`

**Question 2: What is the value associated with the key "Z" in map?**
- A. 3 `Incorrect: The value associated with the key "Z" is 10.`
- B. 5 `Incorrect: The value associated with the key "Z" is 10.`
- C. 10 `Correct: The key "Z" is associated with the value 10.`
- D. null `Incorrect: There is a value associated with the key "Z".`

**Question 3: What is the output of map.containsValue(4)?**
- A. true `Incorrect: The map does not contain the value 4.`
- B. false `Correct: The map does not contain the value 4.`
- C. compilation error `Incorrect: The method call is valid and will not result in a compilation error.`
- D. runtime error `Incorrect: The method call is valid and will not result in a runtime error.`

**Step 20: Mutable Maps**
```java
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
Map<String, Integer> hashMap = new HashMap<>(map);
```

**Question 1: What is the output of hashMap.put("F", 5)?**
- A. 5 `Incorrect: The put() method returns the previous value associated with the key, or null if there was no mapping for the key.`
- B. null `Correct: There was no previous mapping for the key "F".`
- C. "F" `Incorrect: The put() method does not return the key.`
- D. compilation error `Incorrect: The code is valid and will not result in a compilation error.`

**Step 21: Map Implementations**

```java
HashMap<String, Integer> hashMap = new HashMap<>();
hashMap.put("Z", 5);
hashMap.put("A", 15);
hashMap.put("F", 25);
hashMap.put("L", 250);
hashMap // {A=15, F=25, Z=5, L=250}

LinkedHashMap<String, Integer> linkedHashMap = new LinkedHashMap<>();
linkedHashMap.put("Z", 5);
linkedHashMap.put("A", 15);
linkedHashMap.put("F", 25);
linkedHashMap.put("L", 250);
linkedHashMap // {Z=5, A=15, F=25, L=250}

TreeMap<String, Integer> treeMap = new TreeMap<>();
treeMap.put("Z", 5);
treeMap.put("A", 15);
treeMap.put("F", 25);
treeMap.put("L", 250);
treeMap // {A=15, F=25, L=250, Z=5}
```

**Question 1: Which of the following map implementations maintains natural sorted order of the keys?**
- A. HashMap `Incorrect: HashMap does not maintain a natural sorted order.`
- B. LinkedHashMap `Incorrect: LinkedHashMap maintains the order of insertion, not natural sorted order.`
- C. TreeMap `Correct: TreeMap maintains a natural sorted order.`

**Question 2: Which of the following map implementations does not guarantee the order of stored elements?**
- A. HashMap `Correct: HashMap does not maintain any specific order.`
- B. LinkedHashMap `Incorrect: LinkedHashMap maintains the order of insertion.`
- C. TreeMap `Incorrect: TreeMap maintains a natural sorted order.`

**Question 3: Which of the following map implementations maintains insertion order of elements?**
- A. HashMap `Incorrect: HashMap does not maintain any specific order.`
- B. LinkedHashMap `Correct: LinkedHashMap maintains the order of insertion.`
- C. TreeMap `Incorrect: TreeMap maintains a natural sorted order, not the order of insertion.`

**Step 22: Basic Map Operations**

```java
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
map // {Z=10, A=3, B=5}
map.get("Z") // 10
map.get("A") // 3
map.get("C") // null
map.size() // 3
map.isEmpty() // false
map.containsKey("A") // true
map.containsKey("F") // false
map.containsValue(3) // true
map.containsValue(4) // false
map.keySet() // [Z, A, B]
map.values() // [10, 3, 5]
```

**Question 1: What is the output of the following code?**
```java
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
map.put("D", 4);
System.out.println(map.size());
```

- A. 3 `Incorrect: The map is immutable, the put() operation would result in a compilation error.`
- B. 4 `Incorrect: The map is immutable, the put() operation would result in a compilation error.`
- C. 5 `Incorrect: The map is immutable, the put() operation would result in a compilation error.`
- D. Compilation error `Correct: Map created with Map.of() is immutable, any modification attempts would result in a compilation

 error.`

**Question 2: What is the output of the following code?**
```java
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
System.out.println(map.containsValue(2));
```
- A. true `Correct: The map does contain the value 2.`
- B. false `Incorrect: The map contains the value 2.`
- C. Compilation error `Incorrect: The code is valid and will not result in a compilation error.`

**Question 3: What is the output of the following code?**
```java
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
System.out.println(map.keySet());
```
- A. ["A", "B", "C"] `Correct: The map contains the keys "A", "B", and "C".`
- B. [1, 2, 3] `Incorrect: keySet() returns a set of keys, not values.`
- C. ["A"], ["B"], ["C"] `Incorrect: keySet() returns a single set, not separate sets for each key.`
- D. Compilation error `Incorrect: The code is valid and will not result in a compilation error.`

**Step 23: Sorting Collections**

**Question 1: Which data structure always maintains the natural sorted order of its elements?**
- a) HashSet `Incorrect: HashSet does not maintain any specific order.`
- b) LinkedHashMap `Incorrect: LinkedHashMap maintains insertion order, not natural sorted order.`
- c) TreeMap `Correct: TreeMap maintains a natural sorted order of its keys.`
- d) PriorityQueue `Incorrect: PriorityQueue maintains a natural order but not necessarily sorted.`

**Question 2: Which interface provides a contract to implement collections of elements in the form of (key, value) pairs?**
- a) List `Incorrect: List represents an ordered collection (also known as a sequence).`
- b) Set `Incorrect: Set is a collection that cannot contain duplicate elements.`
- c) Queue `Incorrect: Queue typically orders elements in a FIFO (first-in-first-out) manner.`
- d) Map `Correct: Map is an object that maps keys to values. A map cannot contain duplicate keys.`

**Question 3: What is the main difference between a HashMap and a TreeMap?**
- a) HashMap stores elements in natural sorted order while TreeMap is unordered. `Incorrect: It's the other way around. TreeMap maintains natural sorted order, while HashMap is unordered.`
- b) HashMap maintains insertion order while TreeMap is unsorted. `Incorrect: LinkedHashMap maintains insertion order, not HashMap. TreeMap is sorted.`
- c) HashMap and TreeMap are both unordered and unsorted. `Incorrect: HashMap is unordered, but TreeMap is ordered and sorted.`
- d) HashMap is based on a hash table while TreeMap is stored in a tree data structure and maintains natural sorted order. `Correct: HashMap uses hashing principle and TreeMap internally uses Red-Black tree to maintain the natural sorted order.`
