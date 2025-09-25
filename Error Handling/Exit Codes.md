# Exit Codes

### Whenever a command or script ends, it returns an exit code to the system. Exit codes are numerical values that represent whether or not a command or script was executed successfully. 0 indicates success and 1 indicates an error.
---
#### To check the exit code of the last executed command, we can use `echo $?`
```bash
ls
echo $?   # Exit code = 0 (success)

nonexistent
echo $?   # Exit code = non-zero (error)
```
---

#### Example: Check if a binary is installed
```bash
1  #!/bin/bash
2
3  command -v git 2>/dev/null                         # Prints path of executable if it exists or silences output  
4
5  if [[ $? -ne 0 ]]; then                            # If exit code of line 3 is not equal to zero
6  echo "git is not installed. Please install git." 
7   exit 1
8  else
9   echo "git is installed."
10  fi
```
#### Understanding line 3
- `-v` asks `command` to print the path of the executable if it exists, which is `git` in this case
- `2>` redirects the standard error
- `/dev/null` acts as a blackhole that discards whatever is sent there
