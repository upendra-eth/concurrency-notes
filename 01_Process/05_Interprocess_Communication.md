## 01_Interprocess_Communication.md

### Interprocess Communication (IPC)
Interprocess Communication allows processes to exchange data and synchronize actions.

#### Key IPC Mechanisms:
1. **Pipes**:
   - Used for unidirectional communication between processes.
   - Types:
     - Anonymous Pipes: Limited to parent-child process communication.
     - Named Pipes: Allow communication between unrelated processes.

2. **Message Queues**:
   - A queue that stores messages for communication between processes.
   - Benefits:
     - Decouples senders and receivers.
     - Supports asynchronous communication.

3. **Shared Memory**:
   - Processes share a region of memory for direct access.
   - Fast but requires synchronization mechanisms.

4. **Sockets**:
   - Enables communication over a network or locally.
   - Supports bidirectional communication.

5. **Signals**:
   - Used to notify a process of events like termination or interrupts.

#### Types of IPC:
1. **Local IPC**:
   - Communication occurs between processes on the same system.
   - Mechanisms: Shared memory, message queues, named pipes.

2. **Remote IPC**:
   - Communication happens between processes on different systems.
   - Mechanisms: Sockets, RPC.

3. **Synchronous IPC**:
   - Sender waits for the receiver to acknowledge or process the message.
   - Example: Blocking message queues.

4. **Asynchronous IPC**:
   - Sender continues execution without waiting for the receiver.
   - Example: Non-blocking sockets.


#### Use Cases:
- File system operations.
- Network protocols.

---

### Interview Questions:
1. **What is IPC? Why is it needed?**
   - IPC allows processes to communicate and share data, enabling modular and efficient system design.

2. **Explain the difference between message queues and shared memory.**
   - Message queues decouple communication but introduce overhead. Shared memory is fast but requires explicit synchronization.

3. **What are named pipes? How do they differ from anonymous pipes?**
   - Named pipes allow unrelated processes to communicate, unlike anonymous pipes.

4. **What are signals in IPC? Provide an example.**
   - Signals notify processes of events like `SIGINT` for interrupts.

---


### Remote Procedure Call (RPC)
RPC is a communication paradigm where a process executes a procedure on a remote server as if it were local.

#### Key Concepts:
1. **Stubs**:
   - Client and server stubs handle communication details.

2. **Serialization**:
   - Converts data into a transmittable format (e.g., JSON, Protocol Buffers).

3. **Transport Protocols**:
   - Underlying protocols like HTTP, gRPC, or TCP handle message delivery.

#### Benefits:
- Simplifies distributed system development.
- Abstracts networking details from developers.

#### Challenges:
- Network reliability and latency.
- Error handling (e.g., retries, timeouts).

---

### Interview Questions:
1. **What is RPC? How does it differ from IPC?**
   - RPC enables communication between processes on different machines, while IPC is limited to local processes.

2. **Explain the role of stubs in RPC.**
   - Stubs abstract serialization and communication, enabling seamless procedure calls.

3. **What are the common protocols used for RPC?**
   - HTTP, gRPC, and TCP.

4. **What are the challenges of implementing RPC?**
   - Handling network failures, serialization overhead, and ensuring security.

---
