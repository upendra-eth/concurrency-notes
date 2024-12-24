# 02_Threads

## 01_Thread_Basics.md

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

---

## 02_User_vs_Kernel_Threads.md

### User Threads vs Kernel Threads
Threads can be implemented at the user level or the kernel level. Each approach has its pros and cons.

#### User Threads:
- **Managed by**: User-level libraries.
- **Advantages**:
  - Lightweight and fast.
  - No kernel involvement for thread management.
- **Disadvantages**:
  - Cannot leverage multiple cores directly.
  - Entire process blocks if one thread performs a blocking operation.

#### Kernel Threads:
- **Managed by**: Operating system kernel.
- **Advantages**:
  - Directly supported by the OS.
  - Allows true parallel execution on multi-core processors.
- **Disadvantages**:
  - Slower due to kernel overhead.
  - More resource-intensive.

#### Hybrid Models:
Some systems use a combination of user and kernel threads, mapping multiple user threads to kernel threads.

---

## 03_Scheduling.md

### Thread Scheduling
Thread scheduling determines which thread gets CPU time and for how long. It can be preemptive or non-preemptive.

#### Preemptive Scheduling:
- Threads are assigned CPU time based on priority or time slices.
- Example: Round-robin, priority scheduling.

#### Non-preemptive Scheduling:
- Threads voluntarily yield the CPU.
- Example: Cooperative scheduling.

#### Common Scheduling Algorithms:
1. **Round-Robin (RR):**
   - Equal time slices for each thread.
   - Simple and fair.
2. **Priority Scheduling:**
   - Higher-priority threads execute first.
   - Risk of starvation for low-priority threads.
3. **Multilevel Queue Scheduling:**
   - Threads are grouped into priority queues.
   - Different algorithms are applied within and between queues.

---

## 04_Thread_Safety.md

### Thread Safety
Thread safety ensures that shared data and resources are accessed in a controlled manner, preventing conflicts and inconsistencies.

#### Common Issues:
- **Race Conditions**:
  - Multiple threads accessing shared data simultaneously.
  - Outcome depends on execution order.
- **Deadlocks**:
  - Two or more threads waiting indefinitely for resources held by each other.
- **Starvation**:
  - Threads unable to proceed due to resource unavailability.

#### Techniques for Ensuring Thread Safety:
1. **Synchronization Mechanisms**:
   - Mutexes, semaphores, and monitors.
2. **Thread-safe Libraries**:
   - Use libraries with built-in synchronization.
3. **Immutability**:
   - Avoid modifying shared data after creation.
4. **Atomic Operations**:
   - Use atomic instructions for small, critical operations.

#### Best Practices:
- Minimize shared resources.
- Use fine-grained locks.
- Prefer thread-local storage when possible.
