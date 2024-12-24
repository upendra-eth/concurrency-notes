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
