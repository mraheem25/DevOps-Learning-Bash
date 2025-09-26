## Task
- Write a script that checks if a file named `hero.txt` exists in the `Arena` directory. If it does, print `Hero found!`; otherwise, print `Hero missing!`.

## Solution
```bash
#!/bin/bash

if [[ -f "Arena/hero.txt" ]]; then
echo "Hero.txt exists in Arena"
else
echo "Hero.txt does not exist in Arena"
fi
```
