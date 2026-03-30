# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**
A thread is a smaller unit of execution within a process, whereas a process is a whole program operating independently with its own memory and resources. The ability for multiple threads to coexist and share memory within a single process speeds up communication. The overhead of producing threads is lower than that of creating distinct processes. Because all simulated processes required to be managed by a single scheduler and shared ready queue, threads were a better fit for this job. This improved the Round-Robin simulation's efficiency and brought it closer to Java's CPU scheduling demonstration.
[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
When a process does not finish within its allocated time quantum, it is preempted and moved back to the end of the ready queue to wait for its next turn. This is clearly shown in my program output with process P1, which had a total burst time of 4429ms. When P1 executed for the first time, it received the full time quantum of 4000ms, but still had 429ms of remaining burst time, so it was re-added to the ready queue. Similarly, process P7 with burst time 8594ms was re-queued multiple times, appearing in the ready queue after each incomplete quantum until its remaining time reached zero

Example from my output:
▶ P1 executing quantum [4000ms]
⚡ Quantum progress: [███████████████] 100%
⏸ P1 completed quantum 4000ms │ Overall progress: [██████████████████░░] 90% Remaining time: 429ms
↻ P1 yields CPU for context switch
➕ P1 added to ready queue │ Burst time: 4429ms|priority:4
┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P3 → P4 → P5 → P6 → P7 → P8 → P9 → P10 → P1]
└───────────────────────────────────────────────────────────────────────────────
**Explanation of example:**
[Explain what's happening in the output snippet you pasted]
In this output snippet, P1 is shown executing for the full time quantum of 4000ms. After completing its quantum, the program checks the remaining burst time and finds 429ms left, meaning the process did not finish. The scheduler then performs a context switch, and P1 is immediately added back to the end of the ready queue as indicated by the "➕ P1 added to ready queue" message. The updated ready queue display shows P1 now positioned at the end, after P10, demonstrating the Round-Robin behavior where processes cycle through the queue and each gets a fair turn.
---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**
1-**New:** P1 enters the New state when it is first created at the beginning of the simulation before being added to the ready queue. This occurs when the program initializes all processes, as shown in the output where "➕ P1 added to ready queue" appears after the initial creation phase.

2-**Runnable:** P1 becomes Runnable when it is placed into the ready queue, waiting for CPU access. In the output, this happens initially when P1 is first added to the queue, and again each time it is re-queued after being preempted, such as when the output shows "➕ P1 added to ready queue" with the queue displaying P1 at the end waiting for its next turn.

3-**Running:** P1 is in the Running state when the scheduler selects it from the ready queue and begins execution. The output clearly shows this when "▶ P1 executing quantum [4000ms]" appears for its first execution, and later "▶ P1 executing quantum [429ms]" for its final execution where it completes its remaining burst time.

4-**Waiting:** P1 does not enter a Waiting state in this simulation because Round-Robin scheduling uses preemption based on time quantum expiration rather than blocking for external events. The process simply alternates between Runnable and Running states until completion, as there are no I/O operations or synchronization mechanisms in this implementation that would cause it to wait.

5-**Terminated:** P1 enters the Terminated state after its final execution when its remaining burst time reaches zero. The output shows this when "✓ P1 finished execution!" appears after executing its final quantum of 429ms, at which point P1 is removed from the ready queue and no longer participates in scheduling.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1:Online Gaming Servers
**Description**: 
Multiplayer online games handle thousands of players simultaneously, each sending and receiving game state updates, player movements, and actions. The game server uses multiple threads to process all this data in real-time.

**Why Round-Robin works well here**: 
Round-Robin scheduling ensures that all connected players receive equal CPU attention, preventing any single player from experiencing lag while others play smoothly. This fairness is essential for competitive gaming where every player needs consistent response times to maintain fair gameplay and a positive user experience.
### Example 2: Multimedia Streaming Applications
**Description**: 
Description: Applications like YouTube or Spotify need to simultaneously download data from servers, buffer content, decode audio/video, and update the user interface. Each of these tasks runs on separate threads to provide seamless playback.
**Why Round-Robin works well here**: 
Round-Robin scheduling allows the application to allocate CPU time fairly between downloading, decoding, and UI threads, ensuring smooth playback without interruptions. The regular time slices prevent the UI from freezing while content is buffering, and keep audio/video playback stable without stuttering or skipping.
---

## Summary
1.Thread vs Process: Threads share memory and are lightweight, making them ideal for simulations like CPU scheduling.
2.Round-Robin Mechanism: Processes that don't finish within their time quantum are re-queued at the end, ensuring fairness.
3.Thread Lifecycle: I traced P1 through New, Runnable, Running, and Terminated states, understanding when each occurs.
**Key concepts I understood through these questions:**
1.Context Switching Overhead: How to determine the optimal time quantum that balances responsiveness with efficiency.
2.Priority Scheduling: How priority-based scheduling can be combined with Round-Robin to improve performance for important processes.
