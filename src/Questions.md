# Java Multithreading & Concurrency — 60 Questions

Target: Java interviews · 2–4 years experience · Fundamentals to advanced

## Level 1 — Thread Fundamentals
### Questions 1–10 · Thread lifecycle, execution and core concepts
    1. What is the difference between a process and a thread? Explain with a Java example.
    2. What are the different ways to create a thread in Java? Compare extending Thread with implementing Runnable.
    3. What is the difference between calling start() and calling run() directly?
    4. Explain the Java thread lifecycle and the states defined in Thread.State.
    5. What is the difference between Thread.sleep() and Thread.yield()?
    6. What does Thread.join() do, and how can it coordinate execution between two threads?
    7. What are daemon threads? How do they differ from user threads?
    8. What is thread priority in Java, and why should program correctness not depend on it?
    9. What happens when an uncaught exception occurs inside a thread? How can it be handled?
    10. What is thread interruption? Explain interrupt(), isInterrupted(), and Thread.interrupted().

## Level 2 — Synchronization and Thread Safety
### Questions 11–20 · Shared state, monitors and memory visibility
    11. What is a race condition? Demonstrate it using a shared counter accessed by multiple threads.
    12. What is a critical section, and how does synchronized protect it?
    13. What is the difference between synchronizing an instance method and a static method?
    14. What is the difference between a synchronized method and a synchronized block?
    15. What is object-level locking, and how does Java's intrinsic monitor work?
    16. What is reentrancy in Java synchronization? Demonstrate why a thread can reacquire a lock it already owns.
    17. What is the Java Memory Model (JMM), and why does it matter for concurrent programs?
    18. What does volatile guarantee, and why does it not make compound operations such as count++ atomic?
    19. What is the happens-before relationship? Explain it using synchronization and volatile variables.
    20. What makes a class thread-safe? Explain immutability, confinement, and synchronization as different strategies. 

## Level 3 — Coordination, Deadlocks and Locking
### Questions 21–30 · Coordination mechanisms and lock behavior
    21. What is the difference between wait(), notify(), and notifyAll()? Why must wait() usually be called inside a loop?
    22. Why must wait(), notify(), and notifyAll() be called while holding the object's monitor?
    23. What is the difference between wait() and sleep() regarding lock ownership?
    24. What is a deadlock? Write a Java example involving two locks and explain how to prevent it.
    25. What are livelock and starvation, and how do they differ from deadlock?
    26. What is ReentrantLock, and when would you choose it over synchronized?
    27. Explain tryLock(), timed lock acquisition, and interruptible locking.
    28. What is ReadWriteLock, and when can it outperform a regular exclusive lock?
    29. What is Condition, and how does it provide multiple wait sets for a single lock?
    30. What are optimistic and pessimistic locking strategies? Explain how StampedLock supports optimistic reads and the precautions required when validating them.
## Level 4 — Executor Framework and Thread Pools
### Questions 31–40 · Task execution, futures and resource management
    31. Why use ExecutorService instead of manually creating a new thread for every task?
    32. Compare execute() and submit(). How are task exceptions handled differently?
    33. What is the difference between Callable and Runnable?
    34. What is a Future, and how do get(), cancel(), and isDone() work?
    35. Compare shutdown() and shutdownNow(). How should an executor be shut down gracefully?
    36. What is a thread pool? Explain core pool size, maximum pool size, and keep-alive time in ThreadPoolExecutor.
    37. How does the work queue influence thread-pool behavior? Compare bounded and unbounded queues.
    38. What is RejectedExecutionHandler? Explain the built-in rejection policies and when rejection occurs.
    39. What is ScheduledExecutorService, and how do fixed-rate and fixed-delay scheduling differ?
    40. How do you size a thread pool for CPU-bound versus I/O-bound workloads? What measurements should guide the choice?

## Level 5 — Concurrent Collections and Atomic Operations
### Questions 41–50 · Scalable data structures and non-blocking techniques
    41. What is the difference between HashMap, Collections.synchronizedMap(), and ConcurrentHashMap under concurrent access?
    42. How does ConcurrentHashMap support concurrent operations, and why is it not simply one globally synchronized map?
    43. What are weakly consistent iterators, and how do they differ from fail-fast iterators?
    44. Compare ArrayList, Vector, and CopyOnWriteArrayList for concurrent read-heavy workloads.
    45. Compare BlockingQueue, ArrayBlockingQueue, and LinkedBlockingQueue. When would you use each?
    46. How would you implement a producer-consumer system using BlockingQueue without manually coordinating wait() and notify()?
    47. What are atomic classes such as AtomicInteger and AtomicReference, and how do compare-and-set operations work?
    48. What is the difference between AtomicInteger, synchronized, and LongAdder for maintaining a frequently updated counter?
    49. What is the ABA problem in lock-free algorithms, and how can AtomicStampedReference help address it?
    50. What is ConcurrentLinkedQueue, and how does a non-blocking queue differ from a blocking queue?
## Level 6 — Advanced Concurrency and Practical Problems
### Questions 51–60 · CompletableFuture, coordination utilities and design
    51. What is CompletableFuture, and how does it differ from Future?
    52. Explain thenApply(), thenCompose(), and thenCombine() with examples of dependent and independent asynchronous tasks.
    53. What is the difference between thenApply() and thenApplyAsync()? Which executor runs each continuation?
    54. How do you handle exceptions in CompletableFuture using exceptionally(), handle(), and whenComplete()?
    55. What are CountDownLatch, CyclicBarrier, and Phaser? Compare their coordination models and suitable use cases.
    56. What is Semaphore, and how can it limit concurrent access to a resource such as an external API?
    57. How would you implement a thread-safe singleton using the initialization-on-demand holder idiom, and why is double-checked locking dependent on volatile?
    58. Design a bounded producer-consumer pipeline with multiple producers and consumers, graceful shutdown, and failure handling.
    59. Design a concurrent task-processing service that limits parallel requests, applies timeouts, handles failures, and avoids unbounded queue growth.
    60. A Spring Boot API becomes slow under concurrent load. How would you investigate thread-pool exhaustion, lock contention, blocked threads, and excessive task queuing?

