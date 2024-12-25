### Advanced Interview Questions
These questions focus on complex concurrency scenarios and advanced concepts.

#### Questions:
1. **What is the actor model? How does it differ from traditional thread-based concurrency?**
   - The actor model encapsulates state and behavior within actors, communicating via messages. It avoids shared state, unlike traditional threads.

2. **Explain weak and release consistency in memory models.**
   - Weak consistency allows operations to appear out of order unless explicitly synchronized. Release consistency synchronizes at specific points (e.g., locking).

3. **What is false sharing? How can it be mitigated?**
   - False sharing occurs when threads modify variables in the same cache line, causing performance degradation. Mitigate it by aligning variables to separate cache lines.

4. **How would you implement a thread-safe singleton?**
   - Use double-checked locking with proper memory barriers or language constructs like `synchronized` or `std::call_once` (C++).

5. **Describe a scenario where livelock might occur and how to resolve it.**
   - Livelock happens when threads continuously respond to each other without making progress. Resolve it by introducing randomness or breaking symmetry in responses.
