# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?
**Your Answer:I now have a thorough understanding of how multithreading facilitates concurrency in contemporary software thanks to this project. I discovered that controlling threads involves more than just beginning them; it also entails closely monitoring their lifecycle, state transitions, and data sharing, such as the remainingTime variable. Seeing how "Context Switching" actually functions in code—saving the state of one task and switching to the next—was the most unexpected aspect. I now see that computers wouldn't be able to manage several programs at once without effective thread scheduling, and everything would seem sluggish and sequential.**
[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:The Java "Thread Reuse" restriction, which prohibits restarting a thread after it has completed its run() method, was the most challenging obstacle I encountered. A process in a Round-Robin simulation has to run, pause, and then restart at a later time, which appeared difficult with just one thread object. In order to fix this, each time the Process object re-entered the Ready Queue, I had to create a new Thread instance for it. In order to ensure that the "State" of the process—such as its remaining burst time—was maintained across several thread instances, I had to properly map threads to their corresponding process data using a HashMap.**

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:I resolved the difficulties by methodically analyzing the code, concentrating on one process at a time—particularly P1—and closely monitoring its progression from execution to the ready queue and ultimately to termination. I enhanced the print statements to clearly display the executed time quantum, remaining burst time, and when a process was re-added to the queue after running the program several times and seeing the recurring Round-Robin scheduling pattern. In order to better relate the theory to the behavior of the code, I also went over the Java thread lifecycle from my course notes. The reasoning became much evident when the output was compared to the queue operations in the code. The best option for clearing up the issue was this systematic tracing methodology.**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:In real-world systems like web browsers, where different threads manage rendering, loading images, playing videos, and reacting to user clicks simultaneously, multithreading is frequently utilized. While another thread downloads data in the background, one thread in mobile apps keeps the user interface responsive. To handle physics calculations, player input, and network connection simultaneously, online games use multithreading. My understanding of how equitable scheduling techniques like Round-Robin maintain tasks' responsiveness and balance has improved as a result of this project. In contemporary software systems, thread management generally enhances user experience and performance.**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?
Since these ideas are crucial for creating bigger and safer multithreaded systems, I would like to learn more about thread synchronization, race situations, semaphores, mutex locks, and deadlock prevention.
[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?
I am now confident in my comprehension of ready queue behavior, scheduler flow, lifecycle states, and thread generation. I still need to work on more advanced synchronization and concurrency debugging skills, though.
[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
