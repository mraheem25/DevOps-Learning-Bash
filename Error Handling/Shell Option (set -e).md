# Shell Option (set -e)

### Set -e is an option inluded at the start of a script with the purpose of stopping the script from executing when a non zero exit code is returned.

#### Example
```bash
1 #!/bin/bash
2
3 set -e
4
5 echo "Before the script"
6
7 non_existent_command        # Intentionally included a fake command
8
9 echo "After the script"    
```
#### The output is as follows:

```bash
./error_handling.sh: line 7: non_existent_command: command not found
```

#### Explanation
- Script tries to run a command which doesn't exist - returning a non zero exit code. Set -e stops the script at line 7, which means the final echo command is not executed
