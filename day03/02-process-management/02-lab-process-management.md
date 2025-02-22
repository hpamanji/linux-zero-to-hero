## Session 02 : Process Management in Linux

In this session, we’ll explore how to manage processes in Linux. 

Processes are running instances of programs, and managing them is a critical skill for system administrators and developers. By the end of this session, you’ll be able to monitor, control, and troubleshoot processes effectively.

---

### What is a Process?

A process is an instance of a running program. Each process has a unique Process ID (PID) and consumes system resources like CPU, memory, and I/O.

### Key Concepts
- **Foreground Processes**: Processes that run in the terminal and require user interaction.
- **Background Processes**: Processes that run independently of the terminal.
- **Parent and Child Processes**: Processes can spawn other processes, creating a parent-child relationship.
- **Daemons**: Background processes that provide system services (e.g., `sshd`, `httpd`).

### Common Commands
- `ps`: Display information about running processes.
- `top`: Display real-time system statistics and process information.
- `htop`: An interactive version of `top` (requires installation).
- `kill`: Terminate a process by PID.
- `pkill`: Terminate a process by name.
- `nice` and `renice`: Adjust process priority.

---

### Managing Processes

*Objective : Learn how to monitor, control, and troubleshoot processes.*

#### Step 1: View Running Processes

1. **Use `ps` to display processes:**
   ```bash
   ps
   ```

2. **Display all processes for the current user:**
   ```bash
   ps -u $USER
   ```

3. **Display all processes on the system:**
   ```bash
   ps aux
   ```

---

#### Step 2: Monitor Processes in Real-Time

- **Use `top` to monitor processes:**
  ```bash
  top
  ```
  Press `q` to exit.

- **Use `htop` (if installed):**
  ```bash
  htop
  ```

- **Install `htop` if necessary:**
  ```bash
  sudo apt install htop   # Debian-based systems
  sudo yum install htop   # Red Hat-based systems
  ```

---

#### Step 3: Terminate a Process

1. **Find the PID of a process** using `ps` or `top`:
   ```bash
   ps aux | grep vim
   ```

2. **Terminate the process** using `kill`:
   ```bash
   kill <PID>
   ```

3. **Forcefully terminate a process**:
   ```bash
   kill -9 <PID>
   ```

4. **Terminate a process by name** using `pkill`:
   ```bash
   pkill vim
   ```

---

#### Step 4: Adjust Process Priority

- **Start a process with a custom priority** using `nice`:
  ```bash
  nice -n 10 vim
  ```
  Lower values mean higher priority (range: -20 to 19).

- **Change the priority of a running process** using `renice`:
  ```bash
  renice -n 5 -p <PID>
  ```

---

### Best Practices and Common Pitfalls

#### Best Practices
- **Monitor System Resources**: Use `top` or `htop` to monitor CPU, memory, and I/O usage.
- **Terminate Processes Carefully**: Avoid using `kill -9` unless absolutely necessary.
- **Adjust Priorities Wisely**: Use `nice` and `renice` to prioritize critical processes.

#### Common Pitfalls
- **Killing the Wrong Process**: Double-check the PID before terminating a process.
- **Ignoring Resource Usage**: Failing to monitor resource usage can lead to system slowdowns or crashes.
- **Overusing `kill -9`**: Forcefully terminating processes can lead to data loss or corruption.
```
