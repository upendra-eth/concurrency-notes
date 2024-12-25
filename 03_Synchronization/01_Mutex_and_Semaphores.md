### Mutex and Semaphores
Synchronization mechanisms like mutexes and semaphores help control access to shared resources in concurrent programming.

#### Mutex (Mutual Exclusion):
- Ensures that only one thread accesses a critical section at a time.
- **Key Characteristics**:
  - Binary lock (locked/unlocked).
  - Ownership: Only the thread that locks it can unlock it.
- **Use Cases**:
  - Protecting shared variables.
  - Preventing race conditions.

#### Semaphore:
- A synchronization primitive that allows access to a resource by a limited number of threads.
- **Key Characteristics**:
  - Can have a count > 1 (unlike mutex).
  - Two types: Binary (like mutex) and Counting.
- **Use Cases**:
  - Controlling access to a pool of resources (e.g., database connections).

#### Differences:
| Feature       | Mutex              | Semaphore          |
|---------------|--------------------|--------------------|
| Count         | 1 (binary)         | 1 or more          |
| Ownership     | Yes                | No                 |
| Use           | Mutual exclusion   | Resource limiting  |
