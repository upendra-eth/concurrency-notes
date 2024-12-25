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
