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
