# 06_Interview_Questions

## 01_Basic.md

### Basic Interview Questions
These questions focus on fundamental concurrency concepts and are typically asked to assess foundational understanding.

#### Questions:
1. **What is concurrency? How is it different from parallelism?**
   - Concurrency is the ability to manage multiple tasks simultaneously. Parallelism involves executing tasks simultaneously.

2. **What is a process? How does it differ from a thread?**
   - A process is an independent program in execution, with its own memory space. Threads share the memory space of their parent process.

3. **What are race conditions? How can they be avoided?**
   - Race conditions occur when multiple threads access shared data simultaneously, causing unpredictable results. Avoid them using locks or atomic operations.

4. **What is a critical section?**
   - A critical section is a code block that must be executed by only one thread at a time.

5. **What is context switching?**
   - Context switching is the process of saving a thread or process state and restoring another. It enables multitasking but introduces overhead.

---

## 02_Intermediate.md

### Intermediate Interview Questions
These questions delve into synchronization mechanisms and threading intricacies.

#### Questions:
1. **Explain the difference between a mutex and a semaphore.**
   - Mutex is a binary lock for mutual exclusion. Semaphore allows multiple threads to access a resource up to a limit.

2. **What are condition variables? How are they used?**
   - Condition variables enable threads to wait for specific conditions before proceeding. Used with mutexes for signaling between threads.

3. **What is a deadlock? How can it be prevented?**
   - Deadlock occurs when threads are blocked indefinitely, waiting for resources held by each other. Prevent it by avoiding circular waits or using resource ordering.

4. **What is thread safety? How do you ensure it?**
   - Thread safety ensures shared data is accessed predictably. Achieve it using synchronization, immutability, or thread-local storage.

5. **Describe the producer-consumer problem and its solution.**
   - A producer generates data, and a consumer processes it. Solve it using shared buffers with synchronization tools like semaphores or condition variables.

---

## 03_Advanced.md

### Advanced Interview Questions
These questions focus on complex concurrency scenarios and advanced concepts.

#### Questions:
1. **What is the actor model? How does it differ from traditional thread-based concurrency?**
   - The actor model encapsulates state and behavior within actors, communicating via messages. It avoids shared state, unlike traditional threads.

2. **Explain weak and release consistency in memory models.**
   - Weak consistency allows operations to appear out of order unless explicitly synchronized. Release consistency synchronizes at specific points (e.g., locking).

3. **What is false sharing? How can it be mitigated?**
   - False sharing occurs when threads modify variables in the same cache line, causing performance degradation. Mitigate it by aligning variables to separate cache lines.

4. **How would you implement a thread-safe singleton?**
   - Use double-checked locking with proper memory barriers or language constructs like `synchronized` or `std::call_once` (C++).

5. **Describe a scenario where livelock might occur and how to resolve it.**
   - Livelock happens when threads continuously respond to each other without making progress. Resolve it by introducing randomness or breaking symmetry in responses.

---
