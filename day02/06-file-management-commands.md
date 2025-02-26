## 4. Viewing & Editing File Contents

### 4.1 **cat**
- **Purpose**: Concatenate or display files.  
- **Examples**:  
  - `cat <file_name>` – Show file content.  
  - `cat > <new_file>` – Create a new file with typed input (end with `Ctrl + D`).  
  - `cat >> <file_name>` – Append to an existing file.  
  - `cat -n <file_name>` – Display file content with line numbers.

### 4.2 **more** / **less**
- **Purpose**: Paginated viewing of long files.  
- **Examples**:  
  - `more <file_name>` – Scroll line-by-line (`Enter`) or page-by-page (`Space`), quit with `q`.  
  - `less <file_name>` – Similar to `more` but allows backward/forward scrolling (`b`/`Space`).

### 4.3 **head** / **tail**
- **Purpose**: View the beginning or end of a file.  
- **Examples**:  
  - `head -n 3 <file_name>` – Show the first 3 lines.  
  - `tail -n 3 <file_name>` – Show the last 3 lines.

### 4.4 **vi / vim** (Text Editor)
- **Purpose**: A command-mode editor with various modes.  
- **Key Modes**:
  1. **Insert Mode**: Insert or append text.  
     - `i`, `I`, `a`, `A`, `o`, `O`  
  2. **Command Mode**:  
     - `:w` – Save, `:q` – Quit, `:wq` – Save & Quit, `:q!` – Force quit.  
     - `:set nu` – Show line numbers, `:set nonu` – Hide line numbers.  
  3. **Extended Commands** (Esc + ...):  
     - `dd` – Delete line, `yy` – Yank (copy) line, `p` – Paste.  
     - `r` – Replace a character, `R` – Overwrite mode.  
     - `:1,$s/cat/dog/g` – Replace all instances of “cat” with “dog” throughout the file.
