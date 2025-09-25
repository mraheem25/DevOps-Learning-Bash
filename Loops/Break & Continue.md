# Break & Continue

### Break and continue are two essential control statements that rpovide additional control within for and while loops. These control statements allow you to interrupt or skip iterations based on specific conditions.

---

#### Break
- Immediately exits the inner most looop it's placed in regardless of the loops condition

#### Example of break used in a for loop
```bash
#!/bin/bash

for (( i=1; i<=5; i++ ))
do
  if [ $i -eq 3 ]      # If the value of i=3
  then
      break            # Ends the loop prematurely
  fi
echo "Number: $i"
done

```
The output is as follows:\
`Number: 1`\
`Number: 2`

---

#### Continue
- Allows you to skip the rest of the current iteration and move on to the next iteration of the loop
  
#### Example of continue used in a for loop
```bash
#!/bin/bash

for (( i=1; i<=5; i++ ))
do
  if [ $i -eq 3 ]      # If the value of i=3
  then
      continue         # i=3 is skipped
  fi
echo "Number: $i"
done

```
The output is as follows:\
`Number: 1`\
`Number: 2`\
`Number: 4`\
`Number: 5`









