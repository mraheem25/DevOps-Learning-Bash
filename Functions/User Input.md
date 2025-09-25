# User Input

#### User input allows our scripts to interact with users - making them more responsive. We can use the read command to capture the user's input and/or pass parameters as a form of input

---
### Example of accepting user input with read command

```bash
#!/bin/bash

greet_user() {
  echo "What is your name?"    # Prints on terminal to prompt user to enter their name
  read name                    # Stores the user input in the variable name
  echo "Hello, $name"          # Prints the greeting based on the user input
}

greet_user
```

---

### Example of combining parameters and user input

```bash
#!/bin/bash

greet() {
  local name
  if [ $# -eq 0 ]; then           # If the no. arguments passed = 0
    echo "What is your name?"
    read name                     
  else
    name=$1                       # If no. parameters is not equal to 0, then store the first parameter in the variable name
  fi

  echo "Hello, $name"
}

greet                             # Invkoking function which will prompt the user to enter their name
greet "Alice"                     # Skips the prompt and Alice is assigend to the variable name - printing "Hello Alice"                 
```




