# User and Group Management in Linux

In this session, we’ll explore how to manage users and groups in Linux. User and group management is a critical skill for system administrators, as it ensures proper access control and security on a Linux system. By the end of this session, you’ll be able to create, modify, and delete users and groups, as well as assign permissions effectively.

---

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
   -m: Creates a home directory for the user.
   -s /bin/bash: Sets the default shell to Bash.
  ```
  Set a password for the user:
```bash
sudo passwd alice
```

Verify the user creation:
```bash
id alice
```

---

## Step 2: Modify a User

Change the user’s full name:
```bash
sudo usermod -c "Alice Smith" alice
```

Change the user’s shell to `sh`:
```bash
sudo usermod -s /bin/sh alice
```

Lock the user account:
```bash
sudo usermod -L alice
```

Unlock the user account:
```bash
sudo usermod -U alice
```

---

## Step 3: Delete a User

Delete the user **and** their home directory:
```bash
sudo userdel -r alice
```
- **-r**: Removes the user’s home directory and mail spool.

---

## Step 4: Create and Manage Groups

Create a new group:
```bash
sudo groupadd developers
```

Add a user to the group:
```bash
sudo usermod -aG developers alice
```
- **-aG**: Appends the user to the group without removing them from other groups.

Verify the group membership:
```bash
groups alice
```

Remove a user from the group:
```bash
sudo gpasswd -d alice developers
```

Delete the group:
```bash
sudo groupdel developers
```

---

## Best Practices and Common Pitfalls

### Best Practices
- **Use Strong Passwords**: Always set strong passwords for user accounts.
- **Limit Sudo Access**: Only grant sudo privileges to trusted users.
- **Use Groups for Permission Management**: Assign permissions to groups instead of individual users for easier management.

### Common Pitfalls
- **Deleting the Wrong User**: Double-check before deleting a user, especially the `root` user.
- **Forgetting to Remove Home Directories**: Use `userdel -r` to remove home directories when deleting users.
- **Overusing Sudo**: Avoid running commands as root unless absolutely necessary.
```
