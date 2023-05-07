## Step 00: Collections Overview

//Question 1
//What are Collections in Java?
a) Collections is a package in Java
**b) Collections are in-built implementations available to support dynamic data structures in Java programs.**
c) Collections are used to sort static data structures in Java programs.

//Question 2
//What are some common collections?
**a) List, Set, Queue, Map**
b) Stack, Heap, Tree
c) Graph, Queue, Hash Table

//Question 3
//What is List Interface used for?
**a) List Interface is used to implement an ordered collection in Java programs.**
b) List Interface is used to implement an unordered collection in Java programs.
c) List Interface is used to implement a stack data structure in Java programs.


## Step 00: Comparator for ArrayList.sort()

```
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

**Question 1:** What is the purpose of the `StudentsCollectionRunner` class?

-   A) To sort a list of students by their names
-   B) To sort a list of students by their IDs in ascending and descending order
-   C) To create a new student object

**Answer:** B) To sort a list of students by their IDs in ascending and descending order

**Question 2:** What is the output of the following code?

```
ArrayList<Student> studentsAl = new ArrayList<>(students);
studentsAl.sort(new DescStudentComparator());
System.out.println("Desc : " + studentsAl);
```

-   A) [100 Adam, 2 Eve, 1 Ranga]
-   B) [1 Ranga, 2 Eve, 100 Adam]
-   C) [100 Adam, 1 Ranga, 2 Eve]

**Answer:** A) [100 Adam, 2 Eve, 1 Ranga]

**Question 3:** Which interface is used to provide the custom sorting order for `studentsAl`?

-   A) `Comparable`
-   B) `Comparator`
-   C) `Iterable`

**Answer:** B) `Comparator`

## Step 01: The Set interface

Mathematically, a set is a collection of unique items. Similarly, the Java Set interface also specifies a contract for collections having unique elements.

If object1.equals(object2) returns true, then only one of object1 and object2 have a place in a Set implementation. There is no positional element access provided by the Set implementations.

**Question 1:** How does the Java Set interface handle duplicates?

-   A) It stores all duplicate elements
-   B) It only stores the first occurrence of an element
-   C) It throws an exception when duplicates are added

**Answer:** B) It only stores the first occurrence of an element

**Question 2:** What does the `equals` method need to return for two objects to be considered equal and treated as duplicates by a Set implementation?

-   A) `true`
-   B) `false`
-   C) It depends on the specific implementation

**Answer:** A) `true`

**Question 3:** What is one feature that is not provided by the Set interface?

-   A) Iteration over elements
-   B) Removing elements
-   C) Positional element access

**Answer:** C) Positional element access

## Step 02: Understanding Data Structures

### Hash Table

**Question 1:** What is a hash table?

-   A) A table of sorted elements
-   B) A table of unique elements
-   C) A data structure that combines efficient element access and element insertion/deletion

**Answer:** C) A data structure that combines efficient element access and element insertion/deletion

**Question 2:** What is a bucket in a hash table?

-   **A) A slot in the table where elements are inserted and chained together**
-   B) A subset of elements in the table that share the same hash value 
-   C) A container used to store the hash function


# Step 17: PriorityQueue

```
Queue queue = new PriorityQueue<>();
queue.addAll(List.of("Apple", "Zebra", "Monkey", "Cat"));
```

1.  What is the output of `queue.poll()` after adding the elements to the PriorityQueue?
    
    -   A. "Apple"
    -   B. "Zebra"
    -   C. "Cat"
    -   D. "Monkey"
    
    Answer: A
    
2.  What is the default ordering of elements in a PriorityQueue?
    
    -   A. Descending order
    -   B. Ascending order based on natural order
    -   C. Insertion order
    -   D. Random order
    
    Answer: B
    
3.  What is the output of `queue.poll()` after executing `queue.poll()` three times?
    
    -   A. "Cat"
    -   B. "Monkey"
    -   C. "Zebra"
    -   D. null
    
    Answer: D
    

# Step 18: Custom Priority PriorityQueue

```
Queue<String> queue = new PriorityQueue<>(new StringLengthComparator());
queue.addAll(List.of("Zebra", "Monkey", "Cat"));
```

1.  What is the output of `queue.poll()` after adding the elements to the PriorityQueue?
    
    -   A. "Zebra"
    -   B. "Monkey"
    -   C. "Cat"
    -   D. null
    
    Answer: C
    
2.  What interface must be implemented to specify a custom priority order in a PriorityQueue?
    
    -   A. Comparable<T>
    -   B. Comparator<T>
    -   C. PriorityQueue<T>
    -   D. Queue<T>
    
    Answer: B
    
3.  What is the output of the following code snippet after executing `queue.poll()` three times?
    

```
Queue<String> queue = new PriorityQueue<>(new StringLengthComparator());
queue.addAll(List.of("Zebra", "Monkey", "Cat"));
queue.poll();
queue.poll();
queue.poll();
queue.poll();
```

-   A. null
-   B. "Cat"
-   C. "Monkey"
-   D. "Zebra"

Answer: D

# Step 19: Basic Map Operations

```
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
```

1.  What is the size of `map`?
    
    -   A. 3
    -   B. 4
    -   C. 5
    -   D. 6
    
    Answer: A
    
2.  What is the value associated with the key "Z" in `map`?
    
    -   A. 3
    -   B. 5
    -   C. 10
    -   D. null
    
    Answer: C
    
3.  What is the output of `map.containsValue(4)`?
    
    -   A. true
    -   B. false
    -   C. compilation error
    -   D. runtime error
    
    Answer: B
    

# Step 20: Mutable Maps

```
Map<String, Integer> map = Map.of("A", 3, "B", 5, "Z", 10);
Map<String, Integer> hashMap = new HashMap<>(map);
```

1.  What is the output of `hashMap.put("F", 5)`?
    
    -   A. 5
    -   B. null
    -   C. "F"
    -   D. compilation error
    
    Answer: B
    


## Step 21: Map Implementations

```
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

### Question 1

Which of the following map implementations maintains natural sorted order of the keys?

A. HashMap 
B. LinkedHashMap 
C. TreeMap

Answer: C

### Question 2

Which of the following map implementations does not guarantee the order of stored elements?

A. HashMap 
B. LinkedHashMap 
C. TreeMap

Answer: A

### Question 3

Which of the following map implementations maintains insertion order of elements?

A. HashMap 
B. LinkedHashMap 
C. TreeMap

Answer: B

## Step 22: Basic Map Operations

```
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

### Question 1

What is the output of the following code?

```
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
map.put("D", 4);
System.out.println(map.size());
```

A. 3 
B. 4 
C. 5 
D. Compilation error

Answer: D (Map.of() method creates an immutable map, hence put() operation cannot be performed)

### Question 2

What is the output of the following code?

```
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
System.out.println(map.containsValue(2));
```

A. true 
B. false 
C. Compilation error

Answer: A

### Question 3

What is the output of the following code?

```
Map<String, Integer> map = Map.of("A", 1, "B", 2, "C", 3);
System.out.println(map.keySet());
```

A. ["A", "B", "C"] 
B. [1, 2, 3] 
C. ["A"], ["B"], ["C"] 
D. Compilation error

Answer: A

## Step 23: Sorting Collections

Question 1: Which data structure always maintains the natural sorted order of its elements? 
a) HashSet 
b) LinkedHashMap 
c) TreeMap 
d) PriorityQueue

Answer: c) TreeMap

Question 2: Which interface provides a contract to implement collections of elements in the form of (key, value) pairs? 
a) List 
b) Set 
c) Queue 
d) Map

Answer: d) Map

Question 3: What is the main difference between a HashMap and a TreeMap? 
a) HashMap stores elements in natural sorted order while TreeMap is unordered. 
b) HashMap maintains insertion order while TreeMap is unsorted. 
c) HashMap and TreeMap are both unordered and unsorted. 
d) HashMap is based on a hash table while TreeMap is stored in a tree data structure and maintains natural sorted order.

Answer: d) HashMap is based on a hash table while TreeMap is stored in a tree data structure and maintains natural sorted order.