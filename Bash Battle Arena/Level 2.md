## Task
- Create a script that outputs the numbers 1 to 10, one number per line.

## Solution 1
```bash
#!/bin/bash

for ((i=1; i<=10; i++))
do 
    echo "Number $i"
done
```

## Solution 2
```bash
#!/bin/bash

for i in {1..10}
do
    echo $i
done
```
