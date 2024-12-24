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