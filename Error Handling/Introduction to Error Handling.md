# Introduction to Error Handling

### Error handling is about taking measures proactively to prevent you script from crashing or exhibiting unexpected behaviour. Error handling allows you to detect the problem and display a useful error message. 

#### Example without error handling
```bash
#!/bin/bash

num1=10
num2=0
result=$(( num1 / num2 ))
echo "Result is $result"
```

Without the error handling, the script would crash and output `The results is:`\

#### Same Example with error handling
```bash
#!/bin/bash

num1=10
num2=0

if [ $num2 -eq 0 ]; then
  echo "Error: Division by zero is not allowed."
  exit 1
fi

result=$(( num1 / num2 ))
echo "The result is: $result"
```
With error handling, an error message would be displayed - `Error: Division by zero is not allowed.`
