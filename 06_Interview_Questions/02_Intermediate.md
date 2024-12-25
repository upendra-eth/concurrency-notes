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
