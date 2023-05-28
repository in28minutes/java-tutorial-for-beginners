## Step 01: Concurrent Tasks: Extending Thread

### Question 1
What is the output of the following code snippet?

```java
public class ThreadBasicsRunner {
	public static void main(String[] args) {
		//Task1
		for(int i=101; i<=199; i++) {
			System.out.print(i + " ");
		}
		System.out.println("\nTask1 Done");

		//Task2
		for(int i=201; i<=299; i++) {
			System.out.print(i + " ");
		}

		System.out.println("\nTask2 Done");
		
		//Task3
		for(int i=301; i<=399; i++) {
			System.out.print(i + " ");			
		}
		System.out.println("\nTask3 Done");

		System.out.println("Main Done");
	}
}
```

A) 101 102 103 ... 199<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task1 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;201 202 203 ... 299<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task2 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;301 302 303 ... 399<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task3 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;Main Done

B) Task1 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task2 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task3 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;101 102 103 ... 199<br>
&nbsp;&nbsp;&nbsp;&nbsp;201 202 203 ... 299<br>
&nbsp;&nbsp;&nbsp;&nbsp;301 302 303 ... 399<br>
&nbsp;&nbsp;&nbsp;&nbsp;Main Done

C) 101 102 103 ... 199<br>
&nbsp;&nbsp;&nbsp;&nbsp;201 202 203 ... 299<br>
&nbsp;&nbsp;&nbsp;&nbsp;301 302 303 ... 399<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task1 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task2 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task3 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;Main Done

D) Main Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;101 102 103 ... 199<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task1 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;201 202 203 ... 299<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task2 Done<br>
&nbsp;&nbsp;&nbsp;&nbsp;301 302 303 ... 399<br>
&nbsp;&nbsp;&nbsp;&nbsp;Task3 Done

### Question 2
What is the purpose of the following code snippet?

```java
class Task1 extends Thread {
	public void run() {
		System.out.println("Task1 Started ");
		for(int i=101; i<=199; i++) {
			System.out.print(i + " ");
		}
		System.out.println("\nTask1 Done");
	}	
}
```

A) It creates a new thread called `Task1` and defines its execution logic within the `run` method.

B) It creates a new task called `Task1` that can be executed in parallel with other tasks.

C) It extends the `Thread` class and overrides the `start` method to perform the tasks defined in the `run` method.

D) It defines a separate class called `Task1` for organizing the code related to the task.

### Question 3
What is the difference between running a thread using `

start()` and directly calling the `run()` method?

A) There is no difference, both methods execute the thread's logic.

B) The `start()` method creates a new thread and invokes the `run()` method, while calling `run()` directly executes the method in the current thread.

C) The `start()` method is used for threads implemented with `Runnable`, while calling `run()` directly is used for threads extended from `Thread`.

D) The `start()` method allows passing arguments to the thread, while calling `run()` directly does not support passing arguments.

## Step 02: Concurrent Tasks - Implementing Runnable

### Question 1
What is the purpose of implementing the `Runnable` interface in Java?

A) It allows a class to be treated as a thread by extending the `Thread` class.

B) It provides a way to create multiple threads by implementing the `run()` method.

C) It allows a class to define its own execution logic without extending the `Thread` class.

D) It enables concurrent execution of tasks by implementing the `start()` method.

### Question 2
What is the difference between extending the `Thread` class and implementing the `Runnable` interface for creating threads?

A) There is no significant difference between the two approaches; both can be used interchangeably.

B) Extending the `Thread` class allows for simpler thread creation and execution compared to implementing `Runnable`.

C) Implementing the `Runnable` interface allows for better object-oriented design and code reusability compared to extending `Thread`.

D) Extending the `Thread` class provides better control over thread execution compared to implementing `Runnable`.

### Question 3
In the given code snippet, what is the purpose of the `Task2` class?

```java
class Task2 implements Runnable {
	@Override
	public void run() {
		System.out.println("Task2 Started ");
		for(int i=201; i<=299; i++) {
			System.out.print(i + " ");		
		}
		System.out.println("\nTask2 Done");
	}
}
```

A) It defines a new thread class that can be directly launched using the `start()` method.

B) It represents a sub-task that can be executed concurrently by implementing the `run()` method.

C) It extends the `Thread` class and overrides the `start()` method for task execution.

D) It encapsulates the logic for task execution and allows it to be executed by a separate thread.


## Step 03: The Thread Life-cycle

### Question 1
What is the initial state of a thread when it is created but its `start()` method hasn't been invoked?

A) RUNNING

B) RUNNABLE

C) BLOCKED/WAITING

D) NEW

### Question 2
When does a thread enter the TERMINATED/DEAD state?

A) After the execution of the `run()` method is completed.

B) After the `start()` method is invoked.

C) After the `join()` method is called on the thread.

D) After the thread is created using the `new` keyword.

### Question 3
Which of the following states is a thread in when it is ready to be executed but not currently running?

A) RUNNING

B) RUNNABLE

C) BLOCKED/WAITING

D) NEW

## Step 04: Thread Priorities

### Question 1
What is the range of thread priorities in Java?

A) 1 to 100

B) 1 to 1000

C) 1 to 10

D) 0 to 10

### Question 2
What is the default priority assigned to a thread in Java?

A) 1

B) 5

C) 10

D) 0

### Question 3
What method is used to change the priority of a thread in Java?

A) `setPriority(int)`

B) `changePriority(int)`

C) `updatePriority(int)`

D) `modifyPriority(int)`

## Step 05: Communicating Threads

### Question 1
What is the purpose of the `join()` method in Java?

A) It pauses the execution of a thread until it is explicitly resumed.

B) It sets the priority of a thread to the highest level.

C) It allows one thread to wait for the completion of another thread.

D) It terminates a thread and frees up system resources.

### Question 2
In the given code snippet, when will the execution of Task3 begin?

```java
task1.join();
task2Thread.join();

System.out.print("\nTask3 Kicked Off\n");
for(int i=301; i<=399; i++) {
    System.out.print(i + " ");
}
```

A) After Task1 starts

B) After Task2 starts

C) After Task1 and Task2 complete

D) Before Task1 and Task2 start

### Question 3
What is the purpose of using the `join()` method on threads?

A) To synchronize the execution of multiple threads.

B) To pause the execution of a thread temporarily.

C) To terminate a thread.

D) To change the priority of a thread.


## Step 07: Thread Utilities

### Question 1
What is the purpose of the `sleep()` method in Java?

A) It pauses the execution of a thread for a specified number of milliseconds.

B) It terminates a thread and frees up system resources.

C) It changes the priority of a thread.

D) It allows one thread to wait for the completion of another thread.

### Question 2
Which method is used to request the thread scheduler to execute some other thread?

A) `wait()`

B) `join()`

C) `sleep()`

D) `yield()`

## Step 08: Drawbacks of earlier approaches

### Question 1
What is a drawback of using the Thread class or Runnable interface for managing threads?

A) No fine-grained control over thread execution.

B) Difficult to maintain when managing multiple threads.

C) No way to get the result from a sub-task.

D) All of the above.

### Question 2
Which of the following methods is NOT a part of the Thread class for synchronization?

A) `start()`

B) `join()`

C) `sleep()`

D) `wait()`

## Step 09: Introducing ExecutorService

### Question 1
What is the ExecutorService used for in Java?

A) To synchronize the execution of multiple threads.

B) To pause the execution of a thread temporarily.

C) To manage and control the execution of threads.

D) To terminate a thread and free up system resources.

### Question 2
Which method is used to create a single-threaded ExecutorService?

A) `newSingleThreadExecutor()`

B) `newFixedThreadPool()`

C) `newCachedThreadPool()`

D) `newScheduledThreadPool()`



## Step 10: Executor - Customizing Number Of Threads

### Question 1
Which method is used to create a fixed-size thread pool with a specified number of threads?

A) `newSingleThreadExecutor()`

B) `newFixedThreadPool()`

C) `newCachedThreadPool()`

D) `newScheduledThreadPool()`

### Question 2
What happens if more tasks are submitted to an ExecutorService than the number of threads in the thread pool?

A) The additional tasks are queued and executed when a thread becomes available.

B) The additional tasks are discarded and not executed.

C) The ExecutorService automatically adds more threads to the thread pool to accommodate the tasks.

D) The additional tasks cause an exception to be thrown.

### Question 3
Which of the following statements is true about the ExecutorService?

A) It allows for fine-grained control over the execution of threads.

B) It is used to pause the execution of a thread temporarily.

C) It is used to manage and control the execution of threads.

D) It is used to terminate a thread and free up system resources.


## Step 11: ExecutorService: Returning Values From Tasks

### Question 1
Which interface is used to create sub-tasks that return a result?

A) `Thread`

B) `Runnable`

C) `Callable<T>`

D) `ExecutorService`

### Question 2
What method is used to submit a `Callable` task to an `ExecutorService` and obtain a `Future` object representing the task's result?

A) `execute()`

B) `submit()`

C) `invokeAll()`

D) `invokeAny()`

### Question 3
How can you retrieve the result of a `Callable` task from a `Future` object?

A) Using the `get()` method of the `Future` object

B) Using the `run()` method of the `Callable` task

C) Using the `call()` method of the `Callable` task

D) Using the `result()` method of the `Future` object

## Step 12: Executor - Wait Only For The Fastest Task

### Question 1
What method of `ExecutorService` can be used to wait for the result of the fastest completed task from a collection of `Callable` tasks?

A) `execute()`

B) `submit()`

C) `invokeAll()`

D) `invokeAny()`



