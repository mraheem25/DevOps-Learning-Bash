## Task
- Write a script that takes two numbers as input from the user
- Performs basic arithmetic operations (addition, subtraction, multiplication, and division)
- Displays all the answers of those operations in the terminal.

## Solution
```bash
#!/bin/bash

basic_arithmetic() {
    if [ $# -eq 0 ]; then
        echo "Enter 2 numbers"
        read numbers
    else 
        num1=$1 
        num2=$2

    if [[ ! $num1 =~ ^[0-9]+$ ]] || [[ ! $num2 =~ ^[0-9]+$ ]]; then
       echo "Input is invalid, please enter a number."
       return 1
    fi

 addition=$((num1 + num2))
 subtraction=$((num1 - num2))
 multiplication=$((num1 * num2))

    if [[ $num1 -eq 0 ]] || [[ $num2 -eq 0 ]]; then
       echo "Cannot divide by zero."
    else
       division=$((num1 / num2))
    fi
    
    fi

 echo "The sum of the two number is $addition"
 echo "Subtracting the second from the first number gives $subtraction"
 echo "Multiplying the two numbers gives $multiplication"
 echo "Dividining the first number by the second number gives $division"
}

basic_arithmetic 0 10
```
