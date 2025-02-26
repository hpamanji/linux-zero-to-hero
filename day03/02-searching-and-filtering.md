## 8. Searching and Filtering

### 8.1 **grep** / **egrep**
- **Purpose**: Searches for a matching pattern in a file.  
- **Examples**:  
  - `grep -i "liux" greptest` – Case-insensitive search for “liux”.  
  - `grep -v "root" /etc/passwd` – Invert match (display lines **not** matching “root”).  
  - `grep "^liux" greptest` – Match lines beginning with “liux”.  
  - `grep "OS$" greptest` – Match lines ending with “OS”.  
  - `egrep "root|venky" /etc/passwd` – Search multiple patterns.

### 8.2 **find**
- **Purpose**: Searches for files or directories in a hierarchy.  
- **Examples**:  
  - `find / -name "passwd"` – Search for “passwd” from the root directory.  
  - `find /opt -empty -type f` – Find empty files under `/opt`.  
  - `find /opt -perm 777 -exec ls -l {} \;` – Run `ls -l` on each file found with permission `777`.  
  - `-name`, `-iname`, `-type`, `-user`, `-perm`, `-exec`, `-size`, `-mtime`, `-atime`, etc.

### 8.3 **locate**
- **Purpose**: Quickly find files using a pre-built database (updated via `updatedb`).  
- **Examples**:  
  - `locate Indhu.txt` – Search for “Indhu.txt” in the DB.  
  - `locate sethu` – Search for “sethu” in the DB.

### 8.4 **cut**
- **Purpose**: Cuts out columns or characters from a file.  
- **Examples**:  
  - `cut -c1 filename` – Output only the first character of each line.  
  - `cut -d ' ' -f3-6 filename` – Use space as a delimiter and output fields 3 to 6.

### 8.5 **diff**
- **Purpose**: Compares two files line by line.  
- **Examples**:  
  - `diff difftest1.txt difftest2.txt` – Shows differences between the two files.
