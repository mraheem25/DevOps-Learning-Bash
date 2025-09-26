## Task
- Create a directory named `Arena` and then inside it, create three files: `warrior.txt`, `mage.txt`, and `archer.txt`. List the contents of the `Arena` directory.

## Solution 1
```bash
#!/bin/bash

mkdir Arena
touch ./Arena/{warrior.txt,mage.txt,archer.txt}
ls Arena
```

---

## Solution 2
```bash
#!/bin/bash

mkdir Arena
cd Arena
touch warrior.txt mage.txt archer.txt
ls
```
