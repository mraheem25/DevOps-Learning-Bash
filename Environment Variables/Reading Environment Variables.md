# Reading Environment Variables

### Environment variables (EV) allow us to store and retrieve important information in our bash script
### EV's provide a way to store settings and system configurations that our system can access when needed
### EV's must be written in capitals and can be accessed by appending the variable with `$`

---

#### Example of reading environment variables
```bash
#!/bin/bash

echo "Home directory: $HOME"
echo "Current user: $USER"
echo "Operating system type: $OSTYPE"
```

The output would be as follows:
```bash
Home directory: /Users/raheem
Current user: raheem
Operating system type: darwin21
```

---


#### Example of assigning environment variables to local variables
```bash
#!/bin/bash

my_home="$HOME"
my_user="$USER"
my_OS="$OSTYPE"

echo "Home directory: $my_home"
echo "Current user: $my_user"
echo "Operating system type: $my_OS"
```

The output would be as follows:
```bash
Home directory: /Users/raheem
Current user: raheem
Operating system type: darwin21
```
