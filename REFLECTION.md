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

**Your Answer:Building high-performance server-side applications, like a backend API that must manage thousands of concurrent user requests, is a direct application of the concepts I learned here. I can make sure that every user receives a prompt answer without any one request stopping the system as a whole by utilizing a thread pool and a fair scheduling method. I can also use different threads for rendering, AI logic, and physics calculations when developing games. This guarantees that even in cases when the background calculations are very intricate or time-consuming, the game will maintain a high frame rate and remain responsive to player inputs.**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:Building high-performance server-side apps that manage thousands of concurrent requests is a straightforward application of the multithreading ideas I have mastered. By using a thread pool and an effective scheduling algorithm, it is ensured that no single "heavy" request would prevent the system from responding quickly to any user. Multithreading is also necessary in game development to keep the graphics and user interface threads apart from complex physics and AI computations. A professional user experience depends on the game maintaining a high frame rate and remaining responsive to player inputs, both of which are ensured by this design.**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?

[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
