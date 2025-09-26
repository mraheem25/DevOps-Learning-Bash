## Task
- Create a script that copies all .txt files from a specified directory to a backup directory. If the backup directory doesn’t exist, the script should create it first. 

## Solution
```bash
#!/bin/bash

mkdir "specified_directory"
touch ./"specified_directory"/{file1.txt,file2.txt}   # Added for the saKe of running the example

if [[ ! -d "backup_directory" ]]; then
    mkdir "backup_directory"
    cp "./"specified_directory"/"*.txt"" "./backup_directory"
else
    cp "./"specified_directory"/"*.txt"" "./backup_directory"
fi
```
