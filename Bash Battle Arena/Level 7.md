## Task
- Write a script that sorts all .txt files in a directory by their size, from smallest to largest, and displays the sorted list.

## Solution
```bash
#!/bin/bash

directory="./BBA1-5/Arena"

if [[! -d $directory]]; then 
echo "Directory does not exist"
exit 1
fi

find "$directory" -type f -name "*.txt" -exec ls -lh {} + | sort -k 5,5 -h | awk '{ print $5, $9 }'
```
---

## Breakdown of line 15
- `find "$directory"`
  - Finding something in the Arena directory
- `-type f`
  - File type
- `"*.txt"`
  - All .txt file
- `-exec ls -lh {} +`
  - From the files found, list the contents in a list (-l) with the sizes in human-readable format
- `sort -k 5,5 -h`
  - Sort the the fifth column (-k 5,5) of the files received from the previous command based on human-readable format (-h)
- `awk '{ print $5, $9 }'`
  - `awk` assigns parameters repective to the column number
  - `'{ print $5, $9 }'` prints only the 5th and 9th column

