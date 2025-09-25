# Shell Option (set -x)

### Set -x prints each command that will be executed to the terminal before it is executed - allowing you to follow the flow of the script more easily.

#### Example
```bash
1 #!/bin/bash
2
3 set -x
4
5 echo "Starting the script"
6 X=10
7 Y=20
8 Z=$((X + Y))
9 echo "The value of Z is: $Z"
10 set +x
11 echo "After the script"   
```
#### The output is as follows:

```bash
+ echo 'Starting the script'
Starting the script
+ X=10
+ Y=20
+ Z=30
+ echo 'The value of Z is: 30'
The value of Z is: 30
+ set +x
After the script
```

#### Explanation
- Until set +x, each command is printed before execution, which allows you to understand what the script is doing at each step
- set +x disables debugging and only allows debugging for the portion of script above. This results in the final echo command not being stated before its execution.
