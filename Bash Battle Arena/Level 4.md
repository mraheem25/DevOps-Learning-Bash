## Task
- Create a script that copies all `.txt` files from the `Arena` directory to a new directory called `Backup`

## Solution 1
```bash
#!/bin/bash

mkdir Backup
cd Arena
files=(*.txt)

for file in "${files[@]}"
do
    cp "$file" "../Backup"
done
```

# Solution 2
```bash
#!/bin/bash

mkdir -p Backup          
cp Arena/*.txt Backup/
```
---

## Note
- `-p` with `mkdir` creates the directory if it doesn't already exist - preventing erros from occurring
- `*` is referred to as a wildcard and matches all the files in a directory
- Solution 1 only works as I already knew there `.txt` files in Arena. If no `.txt` files were present, an error would pop up saying `cp: *.txt: No such file or directory`. This means `*.txt` would be treated as a string.
  - I could modify my script by addding an if statement to see if the file exits if I was unsure.
- Solution 2 is the better option as if no `.txt` files exist, the command runs with no arguemnts and will fail gracefully. 
