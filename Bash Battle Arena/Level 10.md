## Task
- Write a script that:
  1. Creates a directory called Arena_Boss.
  2. Creates 5 text files inside the directory, named file1.txt to file5.txt.
  3. Generates a random number of lines (between 10 and 20) in each file.
  4. Sorts these files by their size and displays the list.
  5. Checks if any of the files contain the word 'Victory', and if found, moves the file to a directory called Victory_Archive.

## Solution 1
```bash
#!/bin/bash

mkdir "Arena_boss"
touch ./"Arena_boss"/{file1.txt,file2.txt,file3.txt,file4.txt,file5.txt}
cd "Arena_boss"
files=("file1.txt" "file2.txt" "file3.txt" "file4.txt" "file5.txt")

for file in "${files[@]}"
do 
lines=$((RANDOM%11 +10))
for l in $(seq 1 $lines)
    do  echo "This is line $l" >> "$file"
done
done

find "." -type f -name *.txt -exec ls -lh {} + | sort -k 5,5 -h 

mkdir -p Victory_Archive
for file in Arena_boss/*txt
do
  if grep -q "Victory" "$file"; then
  mv "$file" Victory_Archive/
  echo "$file contains 'Victory' and has been moved to Victory_Archive.'
fi
done

```
---

## Solution 2
```bash
#!/bin/bash

mkdir Arena_Boss

for i in {1..5}
do
    FILE="Arena_Boss/file$i.txt"
    LINES=$((RANDOM % 11 + 10))
    for j in $(seq 1 $LINES)
    do
        echo "This is line $j" >> "$FILE"
    done
done

echo "Files sorted by size:"
find Arena_Boss -type f -exec ls -lh {} + | sort -k 5,5 -h


mkdir -p Victory_Archive
for FILE in Arena_Boss/*.txt
do
    if grep -q "Victory" "$FILE"; then
        mv "$FILE" Victory_Archive/
        echo "$FILE contains 'Victory' and has been moved to Victory_Archive."
    fi
done
```
