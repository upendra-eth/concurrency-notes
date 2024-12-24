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