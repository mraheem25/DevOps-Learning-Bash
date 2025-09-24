# Variables

### Variables allow you to store and manipulate data. In Bash, variables are like containers that can hold the following data: strings, arrays and numbers

Creating a variable
- Assign a value `"Hello World"` to the variable `greet` using the assignment operator `=`
  - Note that there are no spaces either side of the assignment operator
- e.g. string ==> `greeting="Hello World"`
- e.g. number ==> `count=20`
- e.g. array ==> `fruits=("apple" "banana" "pear")`

Accessing a variable
- Prefix the variable name with $
- Print value of variable by executing the following commands:
- e.g. string ==> `echo $greeting`
- e.g. number ==> `echo $count`
- e.g. array ==> `echo ${fruits[index]}`, where index=0,1 and 2 for apple,banana and pear respectively
  - format for accessing a variable is `${array[index]}`

Variable interpolation
- Using variables within strings to create a dynamic output
- `name="Ahmed"`\
  `echo "Hello $name"`
