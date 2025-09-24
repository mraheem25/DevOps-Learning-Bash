# Parameters

## Parameters allow user input from the command line to be passed to the bash script for execution - enabling you to customise the behaviour of your script.

Parameters must be placed after the script name as followed:
- `#!/bin/bash`\
  `echo "Parameter 1: $1"`\
  `echo "Parameter 2: $2"`\
  `echo "Parameter 3: $3"`\
  `echo "All Parameters: $@` 
- $ grabs the value of the parameter passed when we run the script
- $@ allows us to access all the parameters passed to the script

The user input for the example above could be as follows:
- `./my_script.sh Hi Hello Hey`
- Note that parameters must have spaces between them

This would print
- `Parameter 1: Hi`\
  `Parameter 2: Hello`\
  `Parameter 3: Hey`\
  `All Parameters: Hi Hello Hey`
