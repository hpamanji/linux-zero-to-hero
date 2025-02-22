# User and Group Management in Linux

In this session, we’ll explore how to manage users and groups in Linux. User and group management is a critical skill for system administrators, as it ensures proper access control and security on a Linux system. By the end of this session, you’ll be able to create, modify, and delete users and groups, as well as assign permissions effectively.

---

## Theory

### What are Users and Groups?
- **Users**: Every person or process that interacts with a Linux system has a user account. Each user has a unique identifier (UID) and a home directory.
- **Groups**: Groups are collections of users. They simplify permission management by allowing you to assign permissions to multiple users at once.

### Key Concepts
- **Root User**: The superuser with full administrative privileges (UID 0).
- **Regular Users**: Standard users with limited privileges (UIDs starting from 1000).
- **System Users**: Users created for system processes and services (UIDs between 1 and 999).

### Important Files
- `/etc/passwd`: Stores user account information.
- `/etc/shadow`: Stores encrypted passwords and password-related information.
- `/etc/group`: Stores group information.
- `/etc/sudoers`: Defines which users can run commands as root.

---

## Hands-On Lab: Managing Users and Groups

### Objective
Learn how to create, modify, and delete users and groups.

---

### Step 1: Create a New User
1. Open the terminal.
2. Use the `useradd` command to create a new user:
   ```bash
   sudo useradd -m -s /bin/bash alice