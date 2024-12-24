### Thread Basics
A thread is the smallest unit of execution within a process. Threads within the same process share memory and resources but execute independently.

#### Key Characteristics:
- **Shared Resources**: Threads share code, data, and files of the process.
- **Independent Execution**: Each thread has its own program counter, stack, and registers.

#### Advantages of Threads:
- Efficient resource utilization.
- Faster context switches compared to processes.
- Simplifies implementation of parallel tasks.

#### Use Cases:
- Multi-tasking applications (e.g., web servers handling multiple requests).
- Real-time systems requiring concurrency.
