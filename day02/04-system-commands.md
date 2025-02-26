## 2. Basic System Information

### 2.1 **uname**
- **Purpose**: Displays basic system information.  
- **Examples**:  
  - `uname -a` – Shows all system details (kernel name, version, architecture, etc.).

### 2.2 **arch**
- **Purpose**: Displays the system architecture.  
- **Examples**:  
  - `arch`  
    - `i686` indicates a 32-bit system.  
    - `x86_64` indicates a 64-bit system.

### 2.3 **clear**
- **Purpose**: Clears the terminal screen.  
- **Shortcut**: `Ctrl + L` is often equivalent to `clear`.

### 2.4 **date**
- **Purpose**: Displays or manipulates the current system date and time.  
- **Examples**:  
  - `date +%A` – Displays the full weekday name (e.g., *Tuesday*).  
  - `date +%F` – Displays the date in `YYYY-MM-DD` format (e.g., *2014-05-27*).

### 2.5 **tty**
- **Purpose**: Shows the terminal type you are currently using.  
- **Examples**:  
  - `tty` – Might display something like `/dev/pts/2` (pseudo-terminal for GUI).

### 2.6 **hostname**
- **Purpose**: Displays the system’s hostname.  
- **Examples**:  
  - `hostname > output.txt` – Redirects the hostname to a file.

### 2.7 **env / echo $SHELL**
- **Purpose**: Check environment variables or the current shell.  
- **Examples**:  
  - `echo $SHELL` – Shows which shell you are using.

