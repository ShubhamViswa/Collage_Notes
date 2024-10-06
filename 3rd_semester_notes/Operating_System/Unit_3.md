
### Deadlocks

#### System Model

A **deadlock** is a situation in a multiprogramming environment where two or more processes cannot proceed because each is waiting for the other to release resources. To model a system's behavior with respect to deadlocks, we consider:
- **Resources:** These can be hardware (CPU, memory) or software resources (files, data).
- **Processes:** These request and use resources.
- **Resource Allocation Graph (RAG):** A graphical representation of the allocation of resources to processes. Nodes represent processes and resources, while edges represent requests and allocations.

**Important Points for Exam:**
- Definition of a deadlock.
- System model components: processes and resources.
- Resource Allocation Graph and its significance in detecting deadlocks.

---

#### Deadlock Characterization

Deadlocks can be characterized by four necessary conditions that must hold simultaneously for a deadlock to occur:
1. **Mutual Exclusion:** At least one resource must be held in a non-shareable mode; only one process can use the resource at a time.
2. **Hold and Wait:** A process holding at least one resource is waiting to acquire additional resources that are currently being held by other processes.
3. **No Preemption:** Resources cannot be forcibly taken from a process; they must be released voluntarily.
4. **Circular Wait:** A set of processes exists such that each process is waiting for a resource held by the next process in the set.

**Important Points for Exam:**
- Define and explain each of the four conditions for deadlock.
- Explain how the combination of these conditions leads to a deadlock situation.

---

#### Methods for Handling Deadlocks

There are several strategies to handle deadlocks in a system:

1. **Deadlock Prevention:** Modify the system so that at least one of the four conditions cannot hold. This can be done through:
   - Eliminating mutual exclusion by using shareable resources.
   - Preventing hold and wait by requiring processes to request all required resources at once.
   - Allowing preemption by taking resources from processes.
   - Avoiding circular wait by imposing an ordering on resource types.

2. **Deadlock Avoidance:** The system dynamically examines the state of resource allocation to ensure that a circular wait condition cannot occur. The most common algorithm is the **Banker’s Algorithm**, which checks resource allocation before proceeding to allocate resources to ensure safety.

3. **Deadlock Detection:** The system periodically checks for deadlocks by constructing a wait-for graph. If the graph contains a cycle, a deadlock exists. 

4. **Recovery from Deadlock:** Once a deadlock is detected, the system must recover from it. Recovery methods include:
   - **Process Termination:** Killing one or more processes involved in the deadlock.
   - **Resource Preemption:** Temporarily taking resources away from one or more processes.

**Important Points for Exam:**
- Compare and contrast deadlock prevention, avoidance, detection, and recovery.
- Explain the Banker’s Algorithm and how it helps in deadlock avoidance.
- Discuss methods of recovering from deadlocks.

---

### Important Questions for Exam:

1. What is a deadlock? Describe the system model used to analyze deadlocks.
2. List and explain the four conditions necessary for a deadlock to occur.
3. Compare and contrast deadlock prevention and deadlock avoidance.
4. Explain the Banker’s Algorithm and how it can be used to avoid deadlocks.
5. Describe the process of deadlock detection and how the system can check for deadlocks.
6. What are the different strategies for recovering from a deadlock?
7. Discuss the significance of resource allocation graphs in deadlock management.
8. Explain how mutual exclusion can lead to deadlocks in a system.
9. Describe the hold and wait condition and its implications for resource allocation.
10. How can the operating system implement preemption to avoid deadlocks?

### Summary for Exam:

1. Deadlocks - Definition, System Model, and Resource Allocation Graph.
2. Deadlock Characterization - Four necessary conditions.
3. Methods for Handling Deadlocks - Prevention, Avoidance, Detection, and Recovery.
4. Banker’s Algorithm - Safe and unsafe states in resource allocation.
