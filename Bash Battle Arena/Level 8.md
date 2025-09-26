## Task
- Create a script that searches for a specific word or phrase across all .log files in a directory and outputs the names of the files that contain the word or phrase.

## Solution
```bash
#!/bin/bash

directory="Arena"
specific="Word"

if [[ ! -d $directory ]]; then 
echo "Directory does not exist"
exit 1
fi

grep -l "$specific" "$directory"/*.log
```
---

## Breakdown of line 16
- `grep`
  - search for
- `-l`
  - files with matches
- `"specific"`
  - of a specific word
- `"$directory"/*.log`
  - for all log files in the specified directory
