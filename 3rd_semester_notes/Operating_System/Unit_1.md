### Operating System (OS) - Introduction

An **Operating System (OS)** is system software that manages hardware and software resources in a computer system and provides services to programs. It acts as an intermediary between users and the hardware. Without an OS, the hardware is difficult to use and manage. Some major roles of an OS are:
- Managing hardware resources like CPU, memory, and I/O devices.
- Providing a user interface.
- Managing files and directories.
- Facilitating the execution of programs.

**Important Points for Exam:**
- Functions of an OS: Process management, Memory management, File system management, I/O system management.
- Types of OS: Batch OS, Time-sharing OS, Distributed OS, Real-time OS, etc.

---

### Simple Batch Systems

In **Simple Batch Systems**, users submit their jobs to the computer, and the OS batches the jobs together to process them sequentially. There's no user interaction once a job starts. The OS keeps the CPU busy by reducing idle time between tasks.
- **Advantage:** Increased CPU utilization.
- **Disadvantage:** Lack of interactivity with users.

**Important Points for Exam:**
- Concept of batching jobs.
- No user interaction after submission.
- Limited resource utilization strategies.

![Batch Operating System Diagram](https://files.prepinsta.com/2023/06/Batch-Operating-System.webp)

---

### Multi-programmed Batch Systems

**Multi-programming** allows the OS to load several programs in memory and execute them concurrently. When one job is waiting for I/O, the CPU can switch to another job, ensuring better utilization of the system.
- **Advantage:** Improved CPU utilization compared to single batch systems.
- **Disadvantage:** Requires more sophisticated memory and process management.

**Important Points for Exam:**
- Concept of multiple jobs sharing CPU time.
- Role of CPU scheduling in multi-programming.
- Memory management strategies in multi-programming.

![Multi-programmed Batch Systems](https://cdn1.byjus.com/wp-content/uploads/2022/08/word-image-4.png)

---

### Time-Sharing Systems

**Time-sharing systems** are an extension of multi-programming where the CPU executes multiple jobs by rapidly switching between them, giving the illusion that the system is dedicated to each user. Each job is allocated a time slice.
- **Advantage:** Interactive system where multiple users can work simultaneously.
- **Disadvantage:** Requires efficient scheduling and resource management.

**Important Points for Exam:**
- Concept of time slices.
- CPU scheduling algorithms used in time-sharing.
- Multi-user support.

![Time-Sharing System](https://cdn1.byjus.com/wp-content/uploads/2022/08/word-image-13.png)
---

### Personal-Computer Systems

**Personal-Computer (PC) Systems** are designed for individual users. They have less sophisticated operating systems compared to large systems but provide sufficient services for personal use.
- Example: Windows, macOS, Linux distributions.

**Important Points for Exam:**
- Characteristics of PC systems.
- Comparison with large systems like mainframes.

---

### Parallel Systems

**Parallel systems** have multiple processors working together to perform tasks. These processors can either share memory or have separate memory, and work on different parts of a problem simultaneously.
- **Advantage:** Increased processing power and speed.
- **Disadvantage:** Complexity in managing synchronization and memory access.

**Important Points for Exam:**
- Difference between parallel and distributed systems.
- Shared memory vs distributed memory.

  [![Learning React](https://img.youtube.com/vi/dGcsHMXbSOA/0.jpg)](https://youtu.be/pPFBgN2XSTY?si=RrbzKP7bQ0PVYQ-r)

<iframe width="560" height="315" src="https://www.youtube.com/embed/dGcsHMXbSOA" 
frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

[Parallel vs Distributed Operating System](https://youtu.be/pPFBgN2XSTY?si=RrbzKP7bQ0PVYQ-r)
---

### Distributed Systems

**Distributed systems** consist of multiple computers working together, appearing to users as a single coherent system. Resources are shared, and communication is required between machines.

 Each machine has a piece of the distributed OS installed to allow them to communicate. Because they must deal with a variety of networking protocols, distributed Operating Systems are far more sophisticated, massive, and complex than network Operating Systems.

- **Advantage:** Scalability and fault tolerance.
- **Disadvantage:** Complexity in communication and synchronization.

**Important Points for Exam:**
- Key characteristics of distributed systems.
- Importance of resource sharing and fault tolerance.

![Distributed System](https://cdn1.byjus.com/wp-content/uploads/2022/08/word-image-14.png)
---

### Real-Time Systems

**Real-time systems** provide immediate processing and responses, ensuring tasks are completed within specific time constraints. Real-time systems are used in critical environments like embedded systems, medical devices, and aircraft.
- **Hard real-time:** Tasks must be completed within strict deadlines.
- **Soft real-time:** Some delays are acceptable.

**Important Points for Exam:**
- Difference between hard and soft real-time systems.
- Real-time constraints and examples.

---

## Memory Management

### Background

**Memory management** involves managing the computer's memory hierarchy (primary memory and secondary storage). The OS is responsible for allocating and deallocating memory to processes.

---

### Logical vs Physical Address Space

- **Logical Address:** Address generated by the CPU.
- **Physical Address:** Actual address in the memory unit.
The OS translates logical addresses to physical addresses using a **Memory Management Unit (MMU)**.

**Important Points for Exam:**
- Difference between logical and physical addresses.
- Role of MMU.

---

### Swapping

**Swapping** is a memory management technique where processes are swapped between main memory and secondary storage to free up memory for active processes.

---

### Contiguous Allocation

In **Contiguous Allocation**, each process is assigned a single continuous block of memory. This approach is simple but can lead to fragmentation issues.

---

### Paging

**Paging** divides memory into fixed-sized blocks called **pages** and **frames**. The process's logical address space is divided into pages, and these are mapped to physical memory frames.
- **Advantage:** Avoids external fragmentation.

---

### Segmentation

**Segmentation** divides memory into variable-sized segments based on the program's logical divisions (e.g., code, data). Each segment is mapped to memory.

---

## Virtual Memory

### Demand Paging

In **Demand Paging**, pages are loaded into memory only when they are required. This reduces memory load but requires a mechanism to handle page faults (when a page is not in memory).

---

### Page Replacement Algorithms

When memory is full, **Page Replacement Algorithms** decide which page to replace. Some common algorithms are:
- **FIFO (First In, First Out)**
- **LRU (Least Recently Used)**
- **Optimal Page Replacement**

---

### Thrashing

**Thrashing** occurs when a system spends more time swapping pages in and out of memory than executing processes. It results in significant performance degradation.

---

### Important Questions for Exam:

1. What are the main functions of an operating system?
2. Compare simple batch systems with multi-programmed batch systems.
3. Explain time-sharing systems and how they differ from batch systems.
4. Describe parallel and distributed systems. What are the key differences?
5. Explain the concept of logical and physical addresses. How does the OS handle memory translation?
6. What is paging, and how does it help in memory management?
7. Compare contiguous allocation with segmentation and paging.
8. What is demand paging, and how does it differ from regular paging?
9. Explain different page replacement algorithms (FIFO, LRU, Optimal).
10. What is thrashing, and how can it be minimized?

### Summary for Exam:

1. Operating Systems - Types (Batch, Multi-programmed, Time-sharing, etc.)
2. Memory Management - Address Spaces, Paging, Segmentation
3. Virtual Memory - Page Replacement Algorithms, Thrashing
