# More set commands

### In addition to set -eux, there are more set commands which are commonly used. These include: set -o nounset; set -o errexit and set -o pipefail.
---
#### set -o nounset
- Similar to -u in that it helps you catch uninitialised variables
#### Example 
```bash
#!/bin/bash

set -o nounset

echo "The value of X is: $X"
```
The output is as follows:\
`./error_handling.sh: line 7: W: unbound variable`

---

#### set -o errexit, where errexit = erro exit
- Similar to -e in that it causes the shell to stop if any invoked command fails
#### Example
```bash
1 #!/bin/bash
2
3 set -o errexit
4
5 echo "This is a test"
6
7 non_existent_command       
8
9 echo "This is another test"    
```
#### The output is as follows:

```bash
./error_handling.sh: line 7: non_existent_command: command not found
```
---

#### set -o pipefail
- Causes a pipeline to return the exit status of the last command in the pipeline that exited with a non-zero command
- Useful when piping commands together
#### Example 
```bash
#!/bin/bash

set -o pipefail

cat non_existent_file | grep "something"
```
#### The output is as follows:

```bash
cat: non_existent_file: No such file or driectory
```
#### Explanation
- `grep` command is not executed as the pipeline fails at the `cat` command. This is because the file does not exist.

