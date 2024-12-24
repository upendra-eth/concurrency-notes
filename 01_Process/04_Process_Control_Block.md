### Process Control Block (PCB)
The Process Control Block is a data structure maintained by the operating system to store process information.

#### Components of PCB:
1. **Process Identification**:
   - Process ID (PID) to uniquely identify each process.
2. **CPU State**:
   - Register values, program counter, etc.
3. **Memory Management Information**:
   - Base and limit registers, page tables.
4. **Scheduling Information**:
   - Priority, time slice information.
5. **I/O Status**:
   - Open file descriptors, I/O devices in use.

#### Role of PCB in Context Switching:
- Acts as a "bookmark" for each process.
- Enables the kernel to pause and resume processes efficiently.
