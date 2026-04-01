# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[process is an independent program execution unit with its own dedicated memory space whereas a thread is a smaller lightweight unit of execution that exists within a process and shares its resources
 we used threads because they share the same memory space which allows for faster communication and  lower creation overhead compared to separate processes Using threads in the SchedulerSimulation.java class is more efficient for simulating CPU scheduling because all process objects need to be managed within a single shared queue and map]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[n Round-Robin scheduling if a process does not finish within its assigned time quantum it is interrupted and moved back to the end of the ready queue This ensures fairness because it prevents any single long-running process from monopolizing the CPU and allows other processes a chance to execute]

Example from my output:
```
[ P6 yields CPU for context switch
]
```

**Explanation of example:**
[process P1 had a remaining time of 4352ms which is greater than the time quantum of 4000ms Because it could not finish within its time  the scheduler interrupted its execution and displayed the yield message and moved it to the back of the ready queue to allow other processes ( P2) to run

]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle]

1. **New**: [p1 is in the New state when the Process object is instantiated and the Thread object is created but not yet started ]

2. **Runnable**: [P1 becomes Runnable after the addProcessToQueue method is called and the process enters the ready queue]  

3. **Running**: [P1 enters the Running state when the scheduler calls Thread.start(), and the run() method begins executing on the CPU ]

4. **Waiting**: [ P1 enter a Waiting or Timed Waiting state during its execution if Thread.sleep() is called to simulate processing time ]

5. **Terminated**: [P1 enters the Terminated state once its remainingTime reaches zero and the run() method complete ]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [ Web Server  ]

**Description**: 
[A web server handling multiple simultaneous HTTP requests from different users ]

**Why Round-Robin works well here**: 
[ because It ensures responsiveness by giving each user request a small time slice preventing a large file download from blocking other users simple page requests]

### Example 2: [ Multimedia Player ]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[ It provides predictability and fairness ensuring that the audio thread and video thread b get regular CPU time to maintain synchronization without lagging  ]

---

## Summary

**Key concepts I understood through these questions:**
1. thread 
2. process
3. round robin scheduling

**Concepts I need to study more:**
1. round robin scheduling
2. threads
