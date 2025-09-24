## Introduction to Bash Scripting

### Why should you learn Bash?
**- Automate tasks to save you time from repetitive actions, which also boosts efficiency**

**- Manage systems by being able to handle files, install software and make system configurations**
 
#### Bash
- Command line tool allowing you to interact with your computer

#### Bash Script
- File containing commands you want your computer to execute automatically

#### Shebang Line (1st line) => #!/bin/bash
- #! is referred to as the shebang and tells the system that this file is a set of commands to be fed to the command interpreter specified
- /bin/bash is the pathname, which is the path to the program that interprets the commands in the script
  - Program can be a shell or programming language

## Writing and executing a script
- The script needs to be created using `touch` and entered into by using `vim`. The `vim` command can be used on its own as it will also create the file if it doesn't already exist
  - `vim script_name.sh`
- In the first line specify the command interepreter to be used, which is bash in this case
  - `#!/bin/bash`
- The script needs executable permissions
  - `chmod +x script_name.sh`
- To run the script the following commands can be used `bash`, `sh`, `./`
  - `./script_name.sh`

