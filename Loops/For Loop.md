# For Loops
### For loops allow you to iterate over a sequence of values and perform repetitive tasks. They are a powerful tool for automating operations and processing data. For loops enable you to repeat a block of code for a specific number of iterations.

#### Structure
```bash
#!/bin/bash

for variable in sequence
do
  #Code block to be executed
done
```
---

#### Basic Example
```bash
#!/bin/bash

for (( i=1; i<=3; i++))      # Initialise variable i by setting it to 1; our sequence; increase value of i by 1 for each iteration
do
  echo "Number: $i"          # Print for each element in the sequence that the variable i takes on
done
```
The output is as follows:\
`Number: 1`\
`Number: 2`\
`Number: 3`

---

#### Array example
``` bash
fruits=("apple" "banana" "pear")    # Assigning an array with 3 items to the variable fruits

for fruit in "${#fruits[@]}"        # Loop iterates over each element in the array
do
    echo "Fruits: $fruit"           # Print the fruit for all array elements                      
done
```

The output is as follows:\
`Fruit: apple`\
`Fruit: banana`\
`Fruit: pear`

