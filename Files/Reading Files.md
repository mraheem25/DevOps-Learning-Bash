# Reading Files
### Reading files allows us to access and extract valuable information from different types of files. Files can be read using redirection or by executing the cat command and processing the contents line by line.

#### Example of how to read files using redirection
```bash
1  #!/bin/bash
2
3  read_file() {
4  local file_path=$1
5 
6   while IFS= read -r line; do
7     echo "$line"
8   done < "$file_path"
9  }
10
11 read_file "./log.txt"
```
### Explanation

#### Line 6
- `IFS` (Interrnal Field Separator) ensures leading and trailing whitespace characters are preserved
- Use `read` command to read each line of the file
-  `-r` prevents backslashes being interpreted as escape characters
#### Line 8
- We are passing in the file path
