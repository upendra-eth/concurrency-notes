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
