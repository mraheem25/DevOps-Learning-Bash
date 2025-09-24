# While loop
### While loops allow you to repeatedly execute a block of code as long as a certain condition remains true. They are a powerful tool used to automate tasks and iterate over data. The condition is checked before each iteration is made.

#### Structure
```bash
#!/bin/bash

while [ condition ]
do
  #code block to be executed
done
```
---
#### Basic Example
```bash
#!/bin/bash
count=1
while [ $count -le 3 ]
do
  echo "Count: $count"
  ((count++))
done
```
The output is as follows:\
`Count: 1`\
`Count: 2`\
`Count: 3`

---

#### Array example
``` bash
fruits=("apple" "banana" "pear")           # Assigning an array with 3 items to the variable fruits
index=0                                    # Start with index 0 (apple)

while [ $index -lt ${#fruits[@]} ]          # Loop runs as long as $index < no. elements in the array
do
    echo "Fruits: ${fruits[$index]}"       # Continuously print the fruit at the current index until condition is false
    ((index++))                            # Increase value of index by 1 for each iteration
done
```

The output is as follows:\
`Fruit: apple`\
`Fruit: banana`\
`Fruit: pear`



