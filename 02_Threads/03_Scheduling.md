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
