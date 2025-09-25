# Shell Option (set -u)

### Set -u is an option which forces the bash script to stop if it encounters an unitialised variable. this could help prevent scenarios where missing data could lead to incorrect results or unexpected behaviour.

#### Example
```bash
1 #!/bin/bash
2
3 set -u
4
5 X=10
6 Y=20
7 Z=$((X + Y + W))
8 echo "Z equals: $Z"    
```
#### The output is as follows:

```bash
./error_handling.sh: line 7: W: unbound variable
```

#### Explanation
- Z is dependant on X, Y and W but W has not been initialised. Therefore, we have an error message regarding W.
