# Piping 

### Piping allows us to pass the output of one command as an input to another. Piping can be used within functions and can store the output in a variable for later use. Piping enables you to build data processing pipelines in your script.

---

#### Example of using piping to count files in a directory 
```bash
#!/bin/bash

get_file_count() {
    local directory="$1"
    local file_count

    file_count=$(ls "directory" | wc -l)                    # $(...) is command substitution and lets us store the output as a varibale. 
                                                            # The command lists the files and then counts the number of lines 
    echo "Number of files in $directory: $file_count"
}
get_file_count "./"                                          # Current directory as a parameter
```

The output would be as follows:\
`Number of files in ./: 5`

---


#### Example of using piping to search for a term
```bash
#!/bin/bash

search_logs() {
  local search_term=$1

  grep "$search_term" log.txt | awk '{ print $2 }'  # Looking for the lines that contain "error" in log.txt
                                                    # We want to extract and print the second ($2) columns
}

search_logs "error"                                 # Call the function, searching for "error"
```
The output would be as follows:\
`12:05:12`\
`12:12:36`

