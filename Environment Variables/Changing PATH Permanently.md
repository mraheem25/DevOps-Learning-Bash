# Changing PATH Permanently

#### The PATH environnment variable is a system variable that specifies the directories where the shell should look for executable files. To make our scripts and binaries available systemwide, we can add our own directories to the PATH environment variable.

#### Note:
- Changes made to the PATH EV made in the terminal are temporary and are lost when the shell session ends
- To make the changes permanent, we need to add the changes to the .zshrc file or .bashrc file.

---

#### Process of how to change the PATH EV permanently

1. Create a new directory from the terminal
   - `mkdir my_scripts`
2. Create a file you would like to access anywhere from the system
   - `vim my_scripts/hello_world.sh`
3. Add desired contents to the script
   - ```bash
     #!/bin/bash
     echo "Hello World"
     ```
4. Save and exit script
   - `:wq!`
5. Make script executable
   - `chmod +x my_scripts/hello_world.sh`
6. Add directory to the PATH EV and append to the .zshrc file or .bashrc file
   - `echo 'export PATH="$PATH:~/my-scripts"' >> ~/.zshrc`
7. Reoload .zshrc file to reflect changes made
   - `source .zshrc`
8. Run file from anywhere
   - `cd Desktop`
   - `hello_world.sh`
9. Contents of file will print on terminal
    - `Hello World`
  



