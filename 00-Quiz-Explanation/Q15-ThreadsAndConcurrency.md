**Step 01: Concurrent Tasks: Extending Thread**

**Question 1: What is the output of the following code snippet?**
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
- A) 101 102 103 ... 199
    Task1 Done
    201 202 203 ... 299
    Task2 Done
    301 302 303 ... 399
    Task3 Done
    Main Done
  - `Correct: The code runs in sequence, executing each task one after the other.`

- B) Task1 Done
    Task2 Done
    Task3 Done
    101 102 103 ... 199
    201 202 203 ... 299
    301 302 303 ... 399
    Main Done
  - `Incorrect: The code first executes the tasks and then prints "Task Done" statements.`

- C) 101 102 103 ... 199
    201 202 203 ... 299
    301 302 303 ... 399
    Task1 Done
    Task2 Done
    Task3 Done
    Main Done
  - `Incorrect: The code prints "Task Done" after each task is completed.`

- D) Main Done
    101 102 103 ... 199
    Task1 Done
    201 202 203 ... 299
    Task2 Done
    301 302 303 ... 399
    Task3 Done
  - `Incorrect: The code does not print "Main Done" until all tasks have completed.`

**Question 2: What is the purpose of the following code snippet?**
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
- A) It creates a new thread called Task1 and defines its execution logic within the run method.
  - `Correct: The Task1 class extends Thread, which means it is a new thread. The run method contains the logic to be executed when the thread starts.`

- B) It creates a new task called Task1 that can be executed in parallel with other tasks.
  - `Correct: Since Task1 is a thread, it can be executed in parallel with other tasks or threads.`

- C) It extends the Thread class and overrides the start method to perform the tasks defined in the run method.
  - `Incorrect: It doesn't override the start method but the run method.`

- D) It defines a separate class called Task1 for organizing the code related to the task.
  - `Incorrect: While it does create a separate class for the task, the main purpose is not just to organize code but to define a separate thread of execution.`

**Question 3: What is the difference between running a thread using `start()` and directly calling the `run()` method?**

- A) There is no difference, both methods execute the thread's logic.
  - `Incorrect: While both execute the thread's logic, start() creates a new thread of control, whereas run() doesn't.`

- B) The start() method creates a new thread and invokes the run() method, while calling run() directly executes the method in the current thread.
  - `Correct: Calling start() launches a new thread and then invokes run(), whereas calling run() directly just executes in the current thread without creating a new one.`

- C) The start() method is used for threads implemented with Runnable, while calling run() directly is used for threads extended from Thread.
  - `Incorrect: Both Runnable and Thread classes can use the start() method to start a new thread.`

- D) The start() method allows passing arguments to the thread, while calling run() directly does not support passing arguments.
  - `Incorrect: Neither start() nor run() support passing arguments directly. If needed, arguments should be passed via the constructor.`

**Step 02: Concurrent Tasks - Implementing Runnable**

**Question 1: What is the purpose of implementing the Runnable interface in Java?**

- A) It allows a class to be treated as a thread by extending the Thread class.
  - `Incorrect: The Runnable interface does not extend the Thread class.`

- B) It provides a way to create multiple threads by implementing the run() method.
  - `Incorrect: Implementing the run() method in Runnable does not directly create multiple threads, it only provides the task that can be assigned to a thread.`

- C) It allows a class to define its own execution logic without extending the Thread class.
  - `Correct: The Runnable interface enables a class to define the code to be executed in a thread (defined in the run() method) without requiring the class to extend the Thread class.`

- D) It enables concurrent execution of tasks by implementing the start() method.
  - `Incorrect: The Runnable interface only includes the run() method, not the start() method.`

**Question 2: What is the difference between extending the Thread class and implementing the Runnable interface for creating threads?**

- A) There is no significant difference between the two approaches; both can be used interchangeably.
  - `Incorrect: There are differences between the two approaches. Extending the Thread class might limit code reuse since Java doesn't support multiple inheritance. Implementing the Runnable interface is usually preferable.`

- B) Extending the Thread class allows for simpler thread creation and execution compared to implementing Runnable.
  - `Incorrect: While extending Thread may look simpler initially, implementing Runnable is often more flexible and promotes better design practices.`

- C) Implementing the Runnable interface allows for better object-oriented design and code reusability compared to extending Thread.
  - `Correct: Implementing Runnable is generally preferable as it doesn't require your class to inherit from Thread (allowing it to inherit from some other class if needed), and it allows the task (the Runnable) to be passed around and executed by different threads.`

- D) Extending the Thread class provides better control over thread execution compared to implementing Runnable.
  - `Incorrect: Both methods provide similar control over thread execution. Neither method inherently provides more control.`

**Question 3: In the given code snippet, what is the purpose of the Task2 class?**
```java
class Task2 implements Runnable {
	@Override
	public void run() {
		System.out.println("Task2 Started ");
		for(int i=201; i<=299; i++) {
			System.out.print(i + "

 ");		
		}
		System.out.println("\nTask2 Done");
	}
}
```
- A) It defines a new thread class that can be directly launched using the start() method.
  - `Incorrect: The Task2 class is not a Thread but a task that needs to be executed by a Thread. You can't call start() directly on a Runnable object.`

- B) It represents a sub-task that can be executed concurrently by implementing the run() method.
  - `Correct: The Task2 class implements Runnable and can be passed to a Thread to execute concurrently.`

- C) It extends the Thread class and overrides the start() method for task execution.
  - `Incorrect: Task2 implements Runnable, it does not extend Thread and does not override the start() method.`

- D) It encapsulates the logic for task execution and allows it to be executed by a separate thread.
  - `Correct: The Task2 class encapsulates a task that can be run by a separate thread.`


**Step 03: The Thread Life-cycle**

**Question 1: What is the initial state of a thread when it is created but its start() method hasn't been invoked?**

- A) RUNNING
  - `Incorrect: A new thread is not in the RUNNING state until the start() method has been invoked.`

- B) RUNNABLE
  - `Incorrect: A new thread is not in the RUNNABLE state until the start() method has been invoked.`

- C) BLOCKED/WAITING
  - `Incorrect: A new thread is not in the BLOCKED/WAITING state initially. It can only enter this state during its execution when it is waiting for a resource.`

- D) NEW
  - `Correct: A new thread is in the NEW state when it is created and before its start() method is invoked.`

**Question 2: When does a thread enter the TERMINATED/DEAD state?**

- A) After the execution of the run() method is completed.
  - `Correct: A thread enters the TERMINATED state after its run() method has completed.`

- B) After the start() method is invoked.
  - `Incorrect: Invoking the start() method initiates the thread execution, it does not terminate it.`

- C) After the join() method is called on the thread.
  - `Incorrect: The join() method makes the current thread to wait until the thread on which join() is called finishes its execution. It does not terminate the thread.`

- D) After the thread is created using the new keyword.
  - `Incorrect: Creating a thread using the new keyword puts the thread in the NEW state, not the TERMINATED state.`

**Question 3: Which of the following states is a thread in when it is ready to be executed but not currently running?**

- A) RUNNING
  - `Incorrect: If a thread is in the RUNNING state, it is currently being executed.`

- B) RUNNABLE
  - `Correct: A thread is in the RUNNABLE state when it is ready to run and is awaiting the CPU's attention.`

- C) BLOCKED/WAITING
  - `Incorrect: A thread is in the BLOCKED/WAITING state when it is waiting for a resource (like a lock) to become available. It is not ready to run.`

- D) NEW
  - `Incorrect: A thread is in the NEW state after it is created but before it is started. It is not yet ready to run.`

**Step 04: Thread Priorities**

**Question 1: What is the range of thread priorities in Java?**

- A) 1 to 100
  - `Incorrect: In Java, the range of thread priorities is 1 to 10, not 1 to 100.`

- B) 1 to 1000
  - `Incorrect: In Java, the range of thread priorities is 1 to 10, not 1 to 1000.`

- C) 1 to 10
  - `Correct: In Java, thread priorities range from 1 to 10.`

- D) 0 to 10
  - `Incorrect: In Java, the minimum thread priority is 1, not 0.`

**Question 2: What is the default priority assigned to a thread in Java?**

- A) 1
  - `Incorrect: The default priority assigned to a thread in Java is 5, not 1.`

- B) 5
  - `Correct: The default priority assigned to a thread in Java is 5.`

- C) 10
  - `Incorrect: The maximum priority that can be assigned to a thread in Java is 10, but it's not the default priority.`

- D) 0
  - `Incorrect: The minimum priority that can be assigned to a thread in Java is 1, not 0.`

**Question 3: What method is used to change the priority of a thread in Java?**

- A) setPriority(int)
  - `Correct: The setPriority(int) method is used to set the priority of a thread in Java.`

- B) changePriority(int)
  - `Incorrect: There's no method called changePriority(int) in Java's Thread class.`

- C) updatePriority(int)
  - `Incorrect: There's no method called updatePriority(int) in Java's Thread class.`

- D) modifyPriority(int)
  - `Incorrect: There's no method called modifyPriority(int) in Java's Thread class.`



**Step 05: Communicating Threads**

**Question 1: What is the purpose of the join() method in Java?**

- A) It pauses the execution of a thread until it is explicitly resumed.
  - `Incorrect: The join() method doesn't pause the thread on which it is invoked. It makes the calling thread to wait until the thread on which join() is called finishes its execution.`

- B) It sets the priority of a thread to the highest level.
  - `Incorrect: The join() method doesn't affect thread priorities.`

- C) It allows one thread to wait for the completion of another thread.
  - `Correct: The join() method allows a thread to wait until the thread on which join() is called completes its execution.`

- D) It terminates a thread and frees up system resources.
  - `Incorrect: The join() method doesn't terminate threads.`

**Question 2: In the given code snippet, when will the execution of Task3 begin?**

- A) After Task1 starts
  - `Incorrect: Task3 doesn't start just after Task1 starts. It starts after Task1 and Task2 both complete, because of the join() methods.`

- B) After Task2 starts
  - `Incorrect: Task3 doesn't start just after Task2 starts. It starts after Task1 and Task2 both complete, because of the join() methods.`

- C) After Task1 and Task2 complete
  - `Correct: The join() methods on task1 and task2Thread make the main thread (which is executing Task3) to wait until both Task1 and Task2 complete.`

- D) Before Task1 and Task2 start
  - `Incorrect: Task3 starts after Task1 and Task2 both complete.`

**Question 3: What is the purpose of using the join() method on threads?**

- A) To synchronize the execution of multiple threads.
  - `Correct: The join() method is used to synchronize the execution of threads by making one thread wait until another thread completes its execution.`

- B) To pause the execution of a thread temporarily.
  - `Incorrect: The join() method doesn't pause the thread on which it is invoked. It makes the calling thread to wait until the thread on which join() is called finishes its execution.`

- C) To terminate a thread.
  - `Incorrect: The join() method doesn't terminate threads.`

- D) To change the priority of a thread.
  - `Incorrect: The join() method doesn't affect thread priorities.`

**Step 07: Thread Utilities**

**Question 1: What is the purpose of the sleep() method in Java?**

- A) It pauses the execution of a thread for a specified number of milliseconds.
  - `Correct: The sleep() method pauses the execution of the current thread for a specified number of milliseconds.`

- B) It terminates a thread and frees up system resources.
  - `Incorrect: The sleep() method doesn't terminate threads.`

- C) It changes the priority of a thread.
  - `Incorrect: The sleep() method doesn't affect thread priorities.`

- D) It allows one thread to wait for the completion of another thread.
  - `Incorrect: The sleep() method doesn't make the current thread wait for another thread to complete.`

**Question 2: Which method is used to request the thread scheduler to execute some other thread?**

- A) wait()
  - `Incorrect: The wait() method causes the current thread to wait until another thread invokes the notify() or notifyAll() method for this object.`

- B) join()
  - `Incorrect: The join

() method makes the current thread to wait until the thread on which it is called completes its execution.`

- C) sleep()
  - `Incorrect: The sleep() method causes the currently executing thread to sleep (temporarily cease execution) for the specified number of milliseconds.`

- D) yield()
  - `Correct: The yield() method gives a hint to the thread scheduler that the current thread is willing to yield its current use of a processor. The scheduler is free to ignore this hint.`



**Step 08: Drawbacks of earlier approaches**

**Question 1: What is a drawback of using the Thread class or Runnable interface for managing threads?**

- A) No fine-grained control over thread execution.
  - `Partially Correct: The Thread class and Runnable interface do not provide advanced features for managing threads, like thread pooling, scheduling, etc.`

- B) Difficult to maintain when managing multiple threads.
  - `Partially Correct: Managing a large number of threads using only Thread class and Runnable interface can become complex.`

- C) No way to get the result from a sub-task.
  - `Partially Correct: Thread class and Runnable interface do not provide an easy mechanism to return results from threads.`

- D) All of the above.
  - `Correct: All the options describe limitations of using the Thread class or Runnable interface for managing threads.`

**Question 2: Which of the following methods is NOT a part of the Thread class for synchronization?**

- A) start()
  - `Incorrect: The start() method is part of the Thread class.`

- B) join()
  - `Incorrect: The join() method is part of the Thread class.`

- C) sleep()
  - `Incorrect: The sleep() method is part of the Thread class.`

- D) wait()
  - `Correct: The wait() method is part of the Object class, not the Thread class. It is used for inter-thread communication, not specifically for synchronization.`

**Step 09: Introducing ExecutorService**

**Question 1: What is the ExecutorService used for in Java?**

- A) To synchronize the execution of multiple threads.
  - `Incorrect: While ExecutorService can be used in scenarios where you need to synchronize tasks, its primary purpose is not synchronization.`

- B) To pause the execution of a thread temporarily.
  - `Incorrect: The ExecutorService interface does not provide methods to pause a thread.`

- C) To manage and control the execution of threads.
  - `Correct: ExecutorService is used to manage and control thread execution. It provides methods to manage end-of-life scenarios for threads and also provides methods for producing future results, and so on.`

- D) To terminate a thread and free up system resources.
  - `Partially Correct: ExecutorService provides methods to shut down the executor and thus terminate threads. However, its main purpose is to control and manage thread execution, not only to terminate threads.`

**Question 2: Which method is used to create a single-threaded ExecutorService?**

- A) newSingleThreadExecutor()
  - `Correct: The newSingleThreadExecutor() method creates an ExecutorService that uses a single worker thread operating off an unbounded queue.`

- B) newFixedThreadPool()
  - `Incorrect: The newFixedThreadPool() method creates a thread pool that reuses a fixed number of threads.`

- C) newCachedThreadPool()
  - `Incorrect: The newCachedThreadPool() method creates a thread pool that creates new threads as needed, but will reuse previously constructed threads when they are available.`

- D) newScheduledThreadPool()
  - `Incorrect: The newScheduledThreadPool() method creates a thread pool that can schedule commands to run after a given delay, or to execute periodically.`


