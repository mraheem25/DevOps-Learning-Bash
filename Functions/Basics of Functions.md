# Basics of Functions
### Functions allow us to turn our code into modules - improving script organisation and enhancing reusability. Functions are like miniprograms in our bash script. They encapsulate a set of instructions that can be called and executed whenever needed.

---

#### Structure
```bash
#!/bin/bash

function_name() {
    #Block of code to be executed
}

```

---

Functions can also accept parameters - making them more felxible.

#### Example of a function using parameters

```bash
#!/bin/bash

greet_person() {        # Creating a new function
local name="$1"         # Setting a local variable and assigning it to the first parameter passed
echo "Hello $name"
}

greet_person "Alice"    # Invoking function
```
The output would be as follows:\
`Hello Alice`
