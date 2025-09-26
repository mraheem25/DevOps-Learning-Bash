## Task
- Combine what has been learn from levels 1-4 by writing a script that:
  1. Creates a directory names 'Battlefield'
  2. Inside Battlefield, create files named knight.txt, sorcerer.txt, and rogue.txt.
  3. Check if knight.txt exists; if it does, move it to a new directory called Archive.
  4. List the contents of both Battlefield and Archive.
 
## Solution 
```bash
#!/bin/bash

mkdir Battlefield
touch ./Battlefield/{"knight.txt",sorcer.txt,rogue.txt}

if [[ -f "./Battlefield/knight.txt" ]]; then
    mkdir Archive
    mv "./Battlefield/knight.txt" "./Archive"
    echo "knight.txt has been moved to Archive"
else
    echo "Knight.txt does not exist"
fi

Battlefield_contents=$(ls "Battlefield")
Archive_contents=$(ls "Archive")
echo " The contents of Battlefield are $Battlefield_contents"
echo " The contents of Archive are $Archive_contents"
```
