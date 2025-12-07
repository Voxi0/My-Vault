**Tags: #programming #os**
A complicated piece of software that manages a computer's hardware and software resources while also providing common services for other programs.

It's basically a software layer that allows computer programs to interact with the hardware resources easily in a relatively portable manner.

The core part of an operating system is the [[Kernel]] but there are various other parts as well that are also important e.g. the [[Bootloader]].
## Types of Operating Systems
In the modern day and age, single-user multitasking operating systems are widely used for general-purpose computing. But there are various other types of operating systems as well.
### Single-User Single-Tasking
Allows a user to run one task at a time.
#### Pros
- Improved efficiency and performance as all available hardware resources are used for one specific task leading to faster execution and better user experience.
- Increased reliability as the likelihood of system crashes or conflicts is significantly reduced making it suitable for critical systems that requires constant uptime and stability.
- Reduced attack surface leading to better security as it's less susceptible to malware and other security threats making it a perfect fit for systems that handles sensitive data or operate in environments where security is key.
- Has a much more simpler design compared to multi-tasking operating systems meaning there's less places for things to go wrong and making it easier for the developers to work on it.
#### Cons
- Lacks multitasking capabilities which is inconvenient for users when they need to switch between multiple applications or perform concurrent activities making it less suitable for general-purpose computing where multitasking is essential.
- Since it's dedicated to running a single task, unused system resources remain idle resulting in potential waste.
### Single-User Multi-Tasking
Allows a user to run multiple tasks concurrently.
#### Pros
- Capable of running multiple tasks at the same time without slowing down the system which is more convenient for users when they need to switch between multiple applications or perform concurrent activities.
- Utilizes system resources better as tasks can be executed in parallel therefore making better use of the CPU and memory.
#### Cons
- Uses more system memory.
- Has a much more complex design compared to single-tasking operating systems meaning there's more places for things to go wrong and making it harder for the developers to work on it.
- Reduced reliability and higher chance of performance issues if system resources aren't managed properly unless efficient scheduling algorithms and resource management techniques are in place leading to resource contention, bottlenecks, slowdowns and system crashes or conflicts.
### Real-Time
Specialized operating system focusing on ensuring that critical tasks are executed on time reliably. These are typically used where timing is critical e.g. defence systems.
#### Types of Real-Time Operating Systems
- **Hard:** Guarantees that critical tasks are completed within a strict time frame. Examples include air traffic control systems and medical imaging systems.
- **Soft:** Provides some flexibility in timing, suitable for applications like multimedia systems.
- **Firm:** Missing a deadline can have consequences, but not as severe as in hard real-time systems. Examples include certain multimedia applications.
#### Pros
- Manages memory allocation efficiently and effectively.
- Designed to be highly reliable and error free.
- Efficient use of devices and systems leading to higher output as it utilizes the hardware resources to the maximum.
#### Cons
- Can only handle a few tasks simultaneously in order to maintain high reliability.
- Requires complex algorithms for scheduling and task management.
- May be resource intensive.