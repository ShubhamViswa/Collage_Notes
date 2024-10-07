### Processes

#### Process Concept  [Click to watch Video](https://youtu.be/B0Uq9Mjz4gM?si=2q6QIv4VGOeCINhC&t=38)

A **process** is a program in execution, consisting of the program code, current activity (represented by the value of the Program Counter), and a set of resources (memory, I/O devices, etc.) allocated to it. Processes are essential for multitasking and resource management.

#### Process Scheduling  [Click to watch Video](https://youtu.be/2h3eWaPx8SA?si=BE-Oz0eKQPMkVWqF&t=36)

**Process scheduling** is the method by which the operating system decides which processes run at a given time. The scheduler selects a process from the ready queue and allocates the CPU to it.

#### Operations on Processes  [Click to watch Video](https://youtu.be/pSW9d3Oaie8?si=DwL-HOEd1lWujEqx)

The operating system manages processes through various operations:
- **Creation:** Creating a new process (forking).
- **[Termination](https://youtu.be/SFc3jt8t5rU?si=fzQVTtNgnkh6eBjt):** Ending a process (exit).
- **Suspension and Resumption:** Suspending a process and resuming it later.


---

### CPU Scheduling

#### Basic Concepts  [Click to watch Video](https://youtu.be/EWkQl0n0w5M?si=pRNwH4R4iLcvBfF3&t=170)

**CPU Scheduling** refers to the method used to allocate the CPU to different processes. Effective scheduling increases CPU utilization and system responsiveness.

**Important Points for Exam:**
- CPU scheduler is part of the operating system.
- Importance of efficient CPU scheduling.

#### Scheduling Criteria [Click to watch Video](https://youtu.be/bWHFY8-rL5I?si=Iu2mgO-VXbuvTvXd)

Common criteria for evaluating scheduling algorithms include:
- **CPU Utilization:** Percentage of time the CPU is busy.
- **Throughput:** Number of processes completed per time unit.
- **Turnaround Time:** Total time taken from submission to completion.
- **Waiting Time:** Total time a process spends waiting in the ready queue.
- **Response Time:** Time from submission of a request to the first response.


#### Scheduling Algorithms

1. **[First-Come, First-Served (FCFS)](https://youtu.be/7DoP1L9nAAs?si=9F5o5tk2dYV7Vqfh):** Processes are scheduled in the order they arrive.
2. **[Shortest Job Next (SJN)](https://youtu.be/t0g9b3SJECg?si=YUdQ8eZEpnYMpzrO):** The process with the smallest execution time is scheduled next.
3. **[Priority Scheduling](https://youtu.be/yKD3pcFvGmY?si=G5M8DkfkAhtin-lk):** Processes are scheduled based on priority. Higher priority processes are executed first.
4. **[Round Robin (RR)](https://youtu.be/YzBBJYfwdi8?si=cyeR5eVCtqV9sRIL):** Each process is assigned a time slice and scheduled in a circular order.
5. **[Multilevel Queue Scheduling](https://youtu.be/fvkSXMZaBNY?si=E8c87eq8uvUjRIrw):** Multiple queues with different scheduling algorithms for each.


#### Multiple-Processor Scheduling

In **multiple-processor scheduling**, multiple CPUs or cores execute processes simultaneously. Key considerations include load balancing, ensuring all CPUs are utilized efficiently, and dealing with process affinity.


---

### Process Synchronization

#### Background

**Process synchronization** is crucial in multi-threaded and multi-process environments to ensure that processes can operate concurrently without conflicts when accessing shared resources.


#### The Critical-Section Problem

The **critical-section problem** arises when multiple processes access and manipulate shared data concurrently, leading to inconsistency. A critical section is a portion of code where the shared resource is accessed.


#### Synchronization Hardware

Some modern architectures provide hardware support for synchronization, such as:
- **Test-and-Set**: Atomically test a variable and set it.
- **Compare-and-Swap**: Compare the value of a variable to a given value and swap it with a new value if they are equal.


#### Semaphores

A **semaphore** is a synchronization primitive that can be used to control access to a shared resource. It can be:
- **Binary Semaphore:** Can take values 0 or 1.
- **Counting Semaphore:** Can take non-negative integer values.


#### Classical Problems of Synchronization

Several classic synchronization problems include:
1. **Producer-Consumer Problem:** A problem involving two processes that share a common buffer.
2. **Dining Philosophers Problem:** A problem that illustrates synchronization issues and resource allocation.
3. **Readers-Writers Problem:** A problem focusing on shared data access by readers and writers.


---

### Important Questions for Exam:

1. Define a process and explain its components.
2. What is the difference between process states? Explain context switching.
3. Discuss the various CPU scheduling algorithms and their advantages and disadvantages.
4. Explain the criteria used to evaluate scheduling algorithms.
5. What is the critical-section problem? List the conditions for a solution.
6. Describe semaphores and their role in process synchronization.
7. Explain the producer-consumer problem and a potential solution.
8. What are the differences between binary and counting semaphores?
9. Discuss the importance of synchronization in operating systems.
10. What is multiple-processor scheduling, and what are the key challenges associated with it?

### Summary for Exam:

1. Processes - Definition, States, Scheduling.
2. CPU Scheduling - Algorithms, Criteria, Multiple-Processor Scheduling.
3. Process Synchronization - Background, Critical-Section Problem, Semaphores, Classical Problems.
