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

***Click here to watch the video -->***
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

---
## 3. Memory Management Techniques

Several techniques are used by the OS to allocate and manage memory efficiently:

### a) Partitioning
- **Fixed Partitioning**: Memory is divided into fixed-size partitions. Each partition holds one process. However, this can lead to wasted space (**internal fragmentation**) if a process doesn't fully use its partition.
- **Dynamic Partitioning**: Memory is divided into partitions dynamically based on process needs. This helps reduce internal fragmentation but may lead to **external fragmentation**, where free memory is split into small, non-contiguous blocks.

### b) Paging
- **Paging** is a technique that divides memory into fixed-size blocks called pages. Physical memory (RAM) is divided into **page frames**, and the OS maps virtual memory addresses to physical memory using **page tables**.
  - Paging reduces external fragmentation.
  - It allows processes to use non-contiguous memory blocks, which simplifies memory allocation.

### c) Segmentation
- **Segmentation** divides memory into variable-sized segments based on logical divisions, such as code, data, and stack. Each segment has its own **base** and **limit address**. Unlike paging, which focuses on physical memory, segmentation deals with the logical view of memory. It allows more flexibility but may suffer from **external fragmentation**.

### d) Virtual Memory
- **Virtual memory** allows processes to run as if they have more RAM than is physically available. The OS uses paging or segmentation to map parts of processes into secondary storage (such as a hard drive) and loads them into RAM when needed. This provides several benefits:
  - Enables multitasking by giving each process its own virtual address space.
  - Facilitates **swapping**, where parts of memory can be temporarily moved to secondary storage when RAM is full.
  - Handles large applications that require more memory than available physical RAM.

---
### Swapping [Swapping Video](https://youtu.be/Kow9tovzVd4?si=-dMsJkFMR-ggGMH9&t=23)

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
