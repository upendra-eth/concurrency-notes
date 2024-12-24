# 03_Synchronization

## 01_Mutex_and_Semaphores.md

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

---

## 02_Monitors_and_Condition_Variables.md

### Monitors and Condition Variables
Monitors and condition variables provide high-level synchronization mechanisms for thread communication.

#### Monitors:
- A monitor is a high-level abstraction for mutual exclusion and synchronization.
- **Key Features**:
  - Encapsulates shared resources.
  - Only one thread can execute a monitor function at a time.

#### Condition Variables:
- Used within monitors to allow threads to wait for specific conditions.
- **Key Operations**:
  - `wait()`: A thread releases the lock and waits for a condition.
  - `signal()`: Wakes up one waiting thread.
  - `broadcast()`: Wakes up all waiting threads.

#### Example Use Case:
A producer-consumer problem where the producer waits if the buffer is full, and the consumer waits if the buffer is empty.

---

## 03_Deadlocks.md

### Deadlocks
A deadlock occurs when two or more threads are blocked forever, each waiting for the other to release a resource.

#### Necessary Conditions for Deadlock:
1. **Mutual Exclusion**: Only one thread can hold a resource at a time.
2. **Hold and Wait**: Threads holding resources wait for additional ones.
3. **No Preemption**: Resources cannot be forcibly taken.
4. **Circular Wait**: A circular chain of threads holding and waiting for resources.

#### Deadlock Prevention:
- Avoid one or more of the necessary conditions.
- **Techniques**:
  - Allocate all resources at once.
  - Impose a resource acquisition order.

#### Deadlock Detection and Recovery:
- Use algorithms to detect cycles in resource allocation graphs.
- Preempt resources or terminate threads to break the cycle.

---

## 04_LiveLock_and_Starvation.md

### Livelock and Starvation
Livelock and starvation are issues related to synchronization that hinder thread progress.

#### Livelock:
- Threads keep changing states in response to each other but cannot proceed.
- **Example**: Two threads repeatedly yielding to each other.

#### Starvation:
- A thread waits indefinitely for resources due to scheduling priorities.
- **Example**: A low-priority thread blocked by high-priority threads.

#### Solutions:
- **For Livelock**:
  - Use randomized backoff or other strategies to break repetitive behavior.
- **For Starvation**:
  - Use fair scheduling algorithms (e.g., First Come First Serve, Round Robin).
  - Implement aging to gradually increase the priority of waiting threads.
