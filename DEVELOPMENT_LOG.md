# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID
**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes


---

## Your Development Log:

### Entry 1 -  [March 27, 2026, 10:00 AM]
**What I did:** Forked the repository and set up my student ID
**Details:**
-Created GitHub account using my university email
-Forked the CPU scheduler starter repository
-Located line 92 and changed the student ID to 445052513
-Compiled the program using javac and ran it successfully
-Reviewed the initial output to understand the basic structure
**Challenges:** The program compiled but I didn't fully understand what the output was showing

**Solution:** I ran the program multiple times and compared outputs to see patterns in the scheduling

**Time spent:** 45 minutes

---

### Entry 2 -  [March 27, 2026, 2:30 PM]
**What I did:** Studied the Round-Robin scheduling algorithm and analyzed program output
**Details:**
-Reviewed course notes on Round-Robin scheduling
-Ran the program 5 times to observe patterns
-Focused on understanding how processes move through the ready queue
-Noticed that processes with burst time longer than quantum were being re-queued
-Identified P1 as a good example to track through the simulation

**Challenges:**The output was cluttered and it was difficult to track individual processes

**Solution:** I decided to improve the print statements to make the output clearer

**Time spent:** 1 hour 

---

### Entry 3 - [March 28, 2026, 11:00 AM]
**What I did:** Enhanced print statements to improve output clarity
**Details:**
-Modified the print statements to show remaining burst time after each quantum
-Added clear indicators when processes were re-added to the ready queue
-Added visual progress bars to show percentage of completion
-Ensured the ready queue display was clearly formatted after each context switch
-Recompiled and ran the program to test the improvements

**Challenges:** Had to carefully identify which variables to print without breaking existing functionality

**Solution:** I traced through the code to understand where burst time was updated, then added print statements at those key points

**Time spent:** 1 hour 30 minutes
---

### Entry 4 -[March 28, 2026, 4:00 PM]
**What I did:** Traced P1 through the complete thread lifecycle
**Details:**
-Used the improved output to track P1 from creation to termination
-Identified each state transition: New → Runnable → Running → Runnable → Running → Terminated
-Documented how P1 was preempted after its first quantum with 429ms remaining
-Observed P1 being re-added to the end of the ready queue after preemption
-Noted P1's final execution where it completed its remaining burst time

**Challenges:** Understanding why P1's waiting time was calculated as 35750ms

**Solution:** I reviewed the code to understand how waiting time is accumulated when a process is in the ready queue

**Time spent:** 1 hour 15 minutes



---

### Entry 5 - [March 28, 2026, 9:30 AM]
**What I did:** Compared ready queue behavior across all processes and completed analysis
**Details:**
-Analyzed how P7 and P9 were re-queued multiple times due to their long burst times
-Counted total context switches (16) from the output
-Compared waiting times between processes: P9 had the longest waiting time (46186ms)
-Documented the Round-Robin pattern where processes cycle through the queue fairly
-Completed all assignment questions with references to the program output

**Challenges:** Explaining the difference between Waiting state and Runnable state in the thread lifecycle

**Solution:** I realized that in this simulation, processes never enter a Waiting state because there are no I/O operations or synchronization blocks

**Time spent:** 1 hour
---

### Entry 6 - [March 30, 2026, 1:00 PM]
**What I did:** Wrote the development log and reviewed all answers
**Details:**
-Compiled all observations into the development log entries
-Verified that each answer referenced specific output examples
-Ensured all 4 questions were answered with 3-5 sentences minimum
-Reviewed the summary section to reflect key learnings and areas for improvement
-Double-checked that student ID (445052513) appears correctly throughout

**Challenges:** Ensuring the answers were concise while still demonstrating understanding

**Solution:** I focused on using specific examples from the output rather than generic explanations

**Time spent:** 45 minutes

---

## Summary

**Total time spent on assignment**:Approximately 12 hours and 15 minutes 

**Most challenging part**:Recognizing the states of the thread lifecycle and elucidating why this simulation does not experience the Waiting state. After going over the course notes and following P1 through the output, I realized that Waiting necessitates blocking on I/O or synchronization. At first, I mistook the Runnable state for Waiting.

**Most interesting learning**: observing the program's output to see how Round-Robin scheduling really functions in practice. Compared to reading about it in theory, the visual depiction of the ready queue shifting after each context flip made the idea much more understandable. I found it very interesting to observe how processes with lengthy burst periods, such as P7 and P9, repeatedly went through the queue.

**What I would do differently next time**:  I would begin by making the print statements better at the beginning of the procedure. I first squandered time attempting to decipher ambiguous output. I could have finished the analysis more quickly if I had improved the logging from the start. To better understand the performance indicators, I would also make a basic table to record the start, end, and waiting times of each process.
