## Task 
- Write a script that:
  1. Creates a directory
  2. Navigates into it
  3. Creates a file inside it
  4. Writes some text to the file
  5. Then displays the contents of the file.

## Solution
```bash
#!/bin/bash

mkdir -p operations_directory
cd operations_directory

fileops_function () {
    local filename=$1
    local file_contents=$2

    echo "file_contents" >> "$filename"
}

fileops_function "file_operations.txt" "Trial text directed to file_operations.txt"

cat "file_operations.txt"
```
