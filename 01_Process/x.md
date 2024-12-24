# 01_Process

## 01_Process_Concurrency.md

### Process Concurrency Overview
Concurrency in operating systems refers to the ability to execute multiple processes simultaneously. This improves resource utilization and system responsiveness. Processes are independent programs that are executed by the operating system.

#### Key Concepts:
- **Concurrency vs Parallelism**:
  - Concurrency: Multiple tasks making progress simultaneously.
  - Parallelism: Multiple tasks running at the same instant on different cores.
- **Process State**: Each process transitions between states: `Ready`, `Running`, and `Waiting`.

#### Benefits of Process Concurrency:
- Better CPU utilization.
- Faster response times.
- Simplifies program design by breaking tasks into smaller processes.

---

## 02_Kernel_Routines.md

### Kernel Routines for Process Management
The kernel plays a pivotal role in managing process concurrency. It ensures that processes execute smoothly without conflicts.

#### Key Functions of Kernel Routines:
1. **Process Creation and Termination**:
   - System calls like `fork()` and `exec()`.
   - Cleaning up resources on termination.
2. **Process Scheduling**:
   - Allocating CPU time to processes.
   - Balancing priorities using algorithms (Round Robin, Priority Scheduling).
3. **Interrupt Handling**:
   - Managing hardware/software interrupts.
   - Ensuring process execution is not disrupted.
4. **Inter-Process Communication (IPC):**
   - Mechanisms like pipes, message queues, and shared memory.

---

## 03_Context_Switch.md

### Context Switching
Context switching occurs when the CPU switches from executing one process to another. This is a core mechanism in achieving process concurrency.

#### Steps in a Context Switch:
1. Save the current process state (registers, program counter, etc.) to its Process Control Block (PCB).
2. Load the state of the next process from its PCB.

#### Key Metrics:
- **Context Switch Time**: Overhead time taken to switch between processes.
- **Frequency**: More frequent switches may lead to inefficiencies.

#### Benefits and Challenges:
- Ensures fair CPU usage among processes.
- Adds overhead due to saving/loading process states.

---

## 04_Process_Control_Block.md

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
