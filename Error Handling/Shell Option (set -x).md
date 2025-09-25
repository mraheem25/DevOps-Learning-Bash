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
```

#### Explanation
- Script tries to run a command which doesn't exist - returning a non zero exit code. Set -e stops the script at line 7, which means the final echo command is not executed
