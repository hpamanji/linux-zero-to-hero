# External Structure

## File System Hierarchy

In UNIX, the **file system hierarchy** represents the external structure. Files and directories are arranged in a tree-like form, originating from the **root (`/`)** directory.

---
### Visual Representation

---

### Accessing Local and Remote Machines

- **Local Machine**:  
  - Press `Ctrl + Alt + F1` through `F6` to switch to **CUI mode** (command-line interface).  
  - Press `Ctrl + Alt + F7` to switch to **GUI mode** (graphical interface).

- **Remote Machine**:  
  - Use commands like `ssh`, `telnet`, `rlogin`, `rsync`, or FTP utilities to connect to remote systems.

---

## Key Directories and Their Purposes

### `/` (Root)
- Parent directory for all other directories; referred to as the **root** directory.  
- Analogous to **`C:\`** on Windows.

### `/root`
- Home directory for the **root user** (superuser).  
- Provides the working environment for administrative tasks.  
- Similar to **`C:\Documents and Settings\Administrator`** on Windows.

### `/home`
- Home directory for **regular users** (everyone other than root).  
- Similar to **`C:\Documents and Settings\username`** on Windows.

### `/boot`
- Contains **bootable files** for UNIX:
  - `vmlinuz` (the kernel)
  - `initrd` (Initial RAM Disk)
  - **GRUB** (Grand Unified Bootloader)
  - Other boot configuration files (e.g., `boot.ini`)

### `/etc`
- Houses **configuration files**:
  - `/etc/passwd` (user information)
  - `/etc/resolv.conf` (DNS configuration)
  - `/etc/dhcpd.conf` (DHCP server configuration)
- Comparable to **`C:\Windows\System32\drivers`** in Windows.

### `/usr`
- The default location for **software installations** (UNIX-sharable resources).  
- Similar to **`C:\Program Files`** on Windows.

### `/opt`
- An **optional directory** for `/usr`.  
- Stores **third-party software**.  
- Also analogous to **`C:\Program Files`** in Windows.

### `/bin`
- Contains **binary files** (programs) used by **all** users.

### `/sbin`
- Contains **system binary files**, which are typically used only by the **superuser** (root).

### `/dev`
- Contains **device files** representing hardware components:
  - `/dev/hda` (hard disk)
  - `/dev/cdrom` (CD-ROM drive)

### `/proc`
- A **virtual directory** that contains information about running processes.  
- Files here are not permanent; they change dynamically:
  - `/proc/meminfo` (RAM information)
  - `/proc/cpuinfo` (CPU information)

### `/var`
- Stores **variable data** such as **log files** and **mail**:
  - `/var/spool/mail` (mail storage)

### `/mnt`
- The default **mount point** for external partitions or drives.  
- Typically empty until something is manually mounted here.

### `/lib`
- Contains **library files** used by the operating system.  
- **Drivers** facilitate kernel-to-hardware communication, whereas **libraries** facilitate application-to-kernel communication.

---

By understanding these directories and their purposes, users can effectively navigate and manage the external structure of a UNIX-based system.
