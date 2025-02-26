
# UNIX Architecture

There are two main structures in UNIX: **Internal** and **External**.

---

## Internal Structure

### Kernel
The **Kernel** is the core component of the UNIX operating system. It is loaded into memory when the system is booted and communicates directly with the hardware. On many UNIX systems, the kernel is represented by the file `/boot/vmlinuz`.

**Key Functions of the Kernel**  
1. **Driver Management**  
   - Manages all device drivers.  
   - Any new hardware connected to the system interacts with the hardware through the kernel.

2. **Process Management**  
   - Responsible for creating (forking) child processes to handle multitasking and multiple users.  
   - For example, when the application Oracle is started, an initial (parent) process is created; as multiple users connect, the kernel spawns child processes for each user to handle their requests.

3. **Memory Management**  
   - Swaps memory pages between RAM and HDD using the **Least Recently Used (LRU)** algorithm.  
   - Applications that are not being used frequently are swapped from RAM to the hard drive, and brought back to RAM as needed.

4. **File Management**  
   - Treats everything in UNIX as files and folders, organizing them in a tree-like structure called the file system.  

   **Types of Files in UNIX**  
   - **Ordinary Files**: Store user data or program instructions.  
   - **Directories**: Act as “folders” to store and organize files.  
   - **Special Files**: Control access to specific hardware devices (e.g., CD-ROMs, Ethernet adapters). These are typically located in the `/dev` directory.

### Shell
The **Shell** is the command interpreter that provides an interface between the user and the kernel. It checks the syntax and semantics of UNIX commands.  

- There is **one kernel** but potentially **multiple shells**, one for each logged-in user.  
- Common shells include:  
  - `sh` (Bourne shell)  
  - `csh` (C shell)  
  - `ksh` (Korn shell)  
  - `bash` (Bash shell)  

To find out which shell you are currently using, run:

```bash
echo $SHELL
```

---
