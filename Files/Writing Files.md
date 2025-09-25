# Writing Files

### Writing files allow us to create, store and modify information in various formats. 

#### Example of writing files using redirection
```bash
#!/bin/bash

write_to_file() {
  local file_path=$1
  local data=$2

  # Overwrite file contents
  echo "$data" > "$file_path"
}

write_to_file "read.txt" "Hello World"
```

#### The output is as follows
- `Hello World`

--- 

#### Example of writing files by appending
```bash
#!/bin/bash

write_to_file() {
  local file_path=$1
  local data=$2

  # Overwrite file contents
  echo "$data" >> "$file_path"
}

write_to_file "read.txt" "Hello"
```

#### The output is as follows
- `Hello World`\
  `Hello`

---

#### Key Operators
- `>` redirects contents of one file to another. The contents of the existing file will overwritten.
- `>>` appends the contents of one file to another withour overwriting the contents of the existing file.
