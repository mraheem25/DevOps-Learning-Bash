## Task
- Write a script that accepts a filename as an argument and prints the number of lines in that file. If no filename is provided, display a message saying 'No file provided'.

## Solution 1
```bash
#!/bin/bash
 
if [[ $# -eq 0 ]]; then           # If no. arguments passed is equal to zero
    echo "No file provided"
    exit 1
fi

if [[ ! -f $1 ]]; then            # If argument passed is not a file  
    echo "File does not exist"
    exit 1
fi

file_linecount=$(wc -l < "$1")    
echo "Number of lines in the file: "$file_linecount""
```

---

## Solution 2
```bash
#!/bin/bash

if [[ -z $1 ]]; then              # If argument passed is a null string (zero length)
    echo "No file provided"
    exit 1
fi

if [[ ! -f $1 ]]; then            # If argument passed is not a file  
    echo "File does not exist"
    exit 1
fi

file_linecount=$(wc -l < "$1")
echo "Number of lines in the file: "$file_linecount""
```
