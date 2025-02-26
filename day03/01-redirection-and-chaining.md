## 6. Redirection and Command Chaining

### 6.1 Redirection
- **Purpose**: Change where the output of a command goes (standard output vs. file).  
- **Examples**:  
  - `>` – Overwrite a file. (e.g., `uname -a > output.txt`)  
  - `>>` – Append to a file. (e.g., `ls -ltr >> output.txt`)

### 6.2 Piping (`|`)
- **Purpose**: Send the output of one command as input to another command.  
- **Examples**:  
  - `cat /etc/passwd | wc` – Count lines, words, and characters of `/etc/passwd`.  
  - `ls -ltr | more` – View the `ls -ltr` output page by page.

### 6.3 Command Chaining (`;`, `&&`, `||`)
- **`;`** – Execute commands sequentially, regardless of success/failure.  
- **`&&`** – Execute the next command only if the previous one succeeded.  
- **`||`** – Execute the next command only if the previous one **failed**.
