## Task
- Write a script that checks if a file exists and prints a message indicating whether it exists or not. If it exists, the script should also check if the file is readable, writable, or executable. 

##Solution
```bash
#!/bin/bash

if [[ ! -f "$FILE" ]]; then
    echo "File does not exist."
    return 1
else
    echo "File exists."
    
if [[ -r "$FILE" ]]; then
    echo "File has readable permissions"
else
    echo "File doesn't have readable permissions."
    fi 
    
if [[ -w "$FILE" ]]; then
    echo "File has readable permissions"
else
    echo "File doesn't have readable permissions."
    fi 
    
if [[ -x "$FILE" ]]; then
    echo "File has executable permissions"
else
    echo "File doesn't have executable permissions."
    fi

fi
```
