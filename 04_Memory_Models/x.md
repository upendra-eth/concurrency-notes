# 04_Memory_Models

## 01_Consistency_Models.md

### Consistency Models
Consistency models define the rules for how memory operations appear to execute in a concurrent system. They are critical for designing and understanding multi-threaded applications.

#### Key Consistency Models:
1. **Strict Consistency**:
   - Every read returns the most recent write, irrespective of thread.
   - Impractical in distributed systems due to latency.

2. **Sequential Consistency**:
   - Operations appear in the same order as programmed across all threads.
   - Easier to reason about but harder to implement efficiently.

3. **Causal Consistency**:
   - Preserves cause-effect relationships between writes.
   - Writes that are causally related appear in the same order for all threads.

4. **Eventual Consistency**:
   - Guarantees that all nodes converge to the same value eventually.
   - Common in distributed systems (e.g., NoSQL databases).

5. **Weak and Release Consistency**:
   - Allow more relaxed ordering for better performance.
   - Synchronization points ensure consistency (e.g., `lock` and `unlock`).

#### Trade-offs:
- **Performance vs Predictability**: Stricter models are easier to reason about but slower.
- **Use Case Dependence**: Choose a model based on application requirements (e.g., real-time systems vs distributed databases).

---

## 02_Shared_Memory.md

### Shared Memory
Shared memory is a concurrency model where threads or processes communicate by reading and writing to a common memory space.

#### Characteristics:
- Efficient communication with low overhead.
- Requires synchronization mechanisms to avoid conflicts (e.g., race conditions).

#### Benefits:
- Fast data sharing compared to message passing.
- Natural for applications requiring shared state (e.g., multi-threaded programs).

#### Challenges:
- **Synchronization Complexity**:
  - Requires mechanisms like mutexes, semaphores, and barriers.
- **Cache Coherence**:
  - Ensuring that changes in one thread's cache are visible to others.

#### Use Cases:
- Operating system kernels.
- High-performance computing (HPC) applications.

---

## 03_Cache_Coherency.md

### Cache Coherency
Cache coherence ensures that multiple copies of the same data in different caches are consistent. This is critical in multi-core systems where each core has its own cache.

#### Key Concepts:
1. **Coherence Protocols**:
   - Ensure that all caches see a consistent view of memory.
   - Common protocols:
     - **MESI (Modified, Exclusive, Shared, Invalid)**
     - **MOESI (Modified, Owned, Exclusive, Shared, Invalid)**

2. **Memory Barriers**:
   - Prevent reordering of memory operations for consistency.

#### Challenges:
- **False Sharing**:
  - Performance degradation when threads on different cores modify separate data in the same cache line.
- **Latency**:
  - Coherence protocols introduce overhead for maintaining consistency.

#### Solutions:
- Optimize data placement to minimize cache line contention.
- Use thread-local storage to reduce shared memory access.

#### Example:
Consider two cores accessing a shared variable:
1. Core 1 updates the variable.
2. Coherence protocol ensures that Core 2 sees the updated value immediately or invalidates its cached copy.

---