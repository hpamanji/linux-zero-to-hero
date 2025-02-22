## Session 3 : Working with Text Files

### Text Editors
- **nano**: A simple, beginner-friendly text editor.
- **vim**: A powerful, advanced text editor (steep learning curve but worth it).

### Common Commands
- `cat`: Display the contents of a file.
- `more/less`: View files page by page.
- `head/tail`: Display the beginning or end of a file.
- `grep`: Search for text within files.
- `>` and `>>`: Redirect output to a file (overwrite or append).

---

### Hands-On Lab: Text File Manipulation

**Objective: Learn how to create, edit, and manipulate text files.**

### Steps

1. **Create a new file:**
   ```bash
   nano myfile.txt
   ```
   Add some text, then save and exit (Ctrl+O, Enter, Ctrl+X).

2. **View the file contents:**
   ```bash
   cat myfile.txt
   ```

3. **Search for a specific word:**
   ```bash
   grep "hello" myfile.txt
   ```

4. **Append text to the file:**
   ```bash
   echo "This is a new line" >> myfile.txt
   ```

5. **View the last few lines of the file:**
   ```bash
   tail myfile.txt
   ```

---

## Best Practices and Common Issues

### Best Practices
- **Use Tab Completion**: Save time by pressing Tab to auto-complete file names and commands.
- **Keep Your System Updated**: Regularly update your Linux system to patch security vulnerabilities.
- **Backup Important Files**: Always keep backups of critical data.

### Common Issues
- **Running Commands as Root**: Avoid using `sudo` unless necessary. Misusing root privileges can break your system.
- **Deleting Files Carelessly**: Double-check before using `rm -rf`. There’s no recycle bin in the terminal!
- **Ignoring Error Messages**: Always read error messages carefully. They often contain clues to fix the issue.

