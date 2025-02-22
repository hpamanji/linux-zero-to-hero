## Session 02 :  Linux Command Line Basics

In this session, we’ll dive into the fundamentals of the Linux command line interface (CLI). The command line is a powerful tool that allows you to interact with your Linux system efficiently. By the end of this session, you’ll be comfortable navigating the file system, running basic commands, and understanding how to use the CLI effectively.

---

### What is the Command Line?
The command line is a text-based interface where you can type commands to perform tasks on your Linux system. It’s faster and more powerful than graphical interfaces for many tasks, especially in server environments.

### Key Concepts
- **Shell**: The program that interprets your commands (e.g., Bash, Zsh).
- **Terminal**: The application that provides access to the shell.
- **Commands**: Instructions you type to perform specific tasks.

### Basic Commands
- `pwd`: Print the current working directory.
- `ls`: List files and directories.
- `cd`: Change directory.
- `mkdir`: Create a new directory.
- `rm`: Remove files or directories.
- `cp`: Copy files or directories.
- `mv`: Move or rename files or directories.
- `touch`: Create an empty file or update the timestamp of an existing file.

---

### Hands-On Lab: Navigating the File System

**Objective : Practice basic commands to navigate and manage files.**

---

#### Step 1: Explore the File System

1. Open the terminal.

2. **Use `pwd` to see your current directory:**
   ```bash
   pwd
   ```

3. **Use `ls` to list files and directories in the current directory:**
   ```bash
   ls
   ```

4. **Use `ls -l` to display detailed information:**
   ```bash
   ls -l
   ```

5. **Use `ls -a` to show hidden files (files starting with a dot):**
   ```bash
   ls -a
   ```

---

#### Step 2: Change Directories

1. **Navigate to your home directory:**
   ```bash
   cd ~
   ```

2. **Navigate to the root directory:**
   ```bash
   cd /
   ```

3. **Go back to the previous directory:**
   ```bash
   cd -
   ```

---

#### Step 3: Create and Manage Files and Directories

1. **Create a new directory:**
   ```bash
   mkdir my_project
   ```

2. **Navigate into the directory:**
   ```bash
   cd my_project
   ```

3. **Create a new file:**
   ```bash
   touch hello.txt
   ```

4. **List the contents of the directory:**
   ```bash
   ls
   ```

5. **Copy the file:**
   ```bash
   cp hello.txt hello_backup.txt
   ```

6. **Rename the file:**
   ```bash
   mv hello.txt greeting.txt
   ```

7. **Delete the file:**
   ```bash
   rm greeting.txt
   ```

---

### Best Practices and Common Isues

#### Best Practices
- **Use Tab Completion**: Save time by pressing Tab to auto-complete file names and commands.
- **Double-Check Commands**: Especially when using `rm` or `sudo`.
- **Organize Files**: Use meaningful directory structures to keep your files organized.

#### Common Issues
- **Deleting Files Carelessly**: Double-check before using `rm -rf`. There’s no recycle bin in the terminal!
- **Ignoring Error Messages**: Always read error messages carefully. They often contain clues to fix the issue.
- **Overusing Sudo**: Avoid running commands as root unless absolutely necessary.
