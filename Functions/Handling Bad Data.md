# Handling Bad Data

### Bad data is invalid or unexpected user input(s) that can cause errors or undesired behavious in our scripts.

#### How can we validate user input within functions?
- Use conditional statements to check validity of input

#### Example of validating input 
```bash
#!/bin/bash

validate_age() {
    local age=$1

    if [[ ! $age =~ ^[0-9]+$ ]]; then                          # if the input age is not a numeric value
        echo "Invalid age. Please provide a numeric value."    
        return 1                                               # non-zero exit code suggests we have encountered an error
    fi

    if (( age < 18 )); then
        echo "Sorry, you must be 18 years old at least."
        return 1
    fi

    echo "Congratulations! You are eligible."
    return 0                                                   # exit code of 0 means there are no errors and conditions have been met
}

echo "Please enter your age"
read user_age                                                  # Assigning user input to variable user_age

validate_age "$user_age"                                       # Executing our validate_age function with user_age as a parameter
exit_code=$?                                                   # $? is referred to as the exit status variable and holds the exit status of a command, function or script itself
                                                                  
if (( exit_code != 0 )); then                                  # Conditional checking if our exit code is zero or non-zero
    echo "Input Validation failed."
fi

```
