# Introduction to UNIX

## Multiuser System
UNIX is a multiprogramming system, permitting multiple users to run separate jobs simultaneously. The CPU, memory, and hard disk are shared between users.  

- The system splits a unit of time into several segments, allocating each segment to a different user.  
- At any given moment, the system runs a job for a single user; when that user’s allotted time expires, the job is put on hold, and the system moves on to the next job.

## Multitasking System
A single user can also run multiple tasks concurrently in a multitasking environment.  

- One job can run in the foreground while the rest run in the background.  
- For example, you might edit one file while simultaneously printing another.  
- Multiple jobs can be handled in parallel, giving the illusion of simultaneous execution.

## Building-Block Approach
UNIX commands are designed to perform simple, specific tasks. A powerful feature of UNIX is the ability to chain commands together:

- Using the pipe symbol (`|`), the output of one command can be fed directly into another command.  
- This allows you to build complex functionalities from smaller, single-purpose commands.

## UNIX Toolkit
While the **kernel** itself is relatively minimal, UNIX provides a wide array of tools to meet various needs:

- **General-purpose tools**  
- **Text manipulation utilities**  
- **Compilers & interpreters**  
- **Network applications**  
- **System administration tools**  

You also have a choice of different shells. With each release of UNIX, new tools are added while older ones may be modified or removed.

## Programming Facility
UNIX offers robust features for programmers:

- **Shell scripting** (e.g., the Bourne shell, Bash) and **awk** provide programming environments.  
- They include control structures, loops, and variables, making them powerful programming languages in their own right.
- Shell scripts can invoke multiple commands together to form complex logics. Awk can be used for generating reports.

