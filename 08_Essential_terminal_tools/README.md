# Section 8: Essential Terminal Tools

This section introduces important Linux concepts and tools that help you work efficiently with files, data streams, and command chaining.

## Topics Covered

### 1. Links & Inodes
- **Inodes**: Data structures that store metadata about files (permissions, size, timestamps) but not the file name.
- **Hard Links**:
  - Point directly to the same inode as the original file.
  - Created with: `ln file1 file2`
  - Deleting one link does not remove the file as long as another hard link exists.
- **Symbolic (Soft) Links**:
  - Pointers to the file name, not the inode.
  - Created with: `ln -s file1 link1`
  - Broken if the original file is deleted.

### 2. Input-Output Streams
- **Standard Input (stdin)**: Default input stream, usually the keyboard. (`fd 0`)
- **Standard Output (stdout)**: Default output stream, usually the terminal. (`fd 1`)
- **Standard Error (stderr)**: Default error message stream. (`fd 2`)
- **Redirection**:
  - Output to file: `command > file.txt`
  - Append output: `command >> file.txt`
  - Redirect stderr: `command 2> errors.txt`
  - Redirect both stdout and stderr: `command > output.txt 2>&1`

### 3. Pipeline
- **Definition**: Connects the output of one command to the input of another using the `|` operator.
- **Example**:
  ```bash
  cat file.txt | grep "error" | sort | uniq
