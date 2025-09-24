# If Statements, Else/Elif 

### If statements allow you to introduce decision making logic into your scripts. They allow you to evaluate conditions and execute different code blocks based on the result of the statement.
### Else clauses provide an alternative code block to be executed when the condition from the if statement is false. Elif allows us to add another condition if the first condition is false.

#### If Structure 
```bash
#!/bin/bash
if [ condition ]
then
  #execute code block if condition is true
fi
```
#### Else Structure 
```bash
#!/bin/bash
if [ condition ]
then
  #execute code block if condition is true
else
  #execute code block if condition is false
fi
```
#### Elif Structure 
```bash
#!/bin/bash
if [ 1st condition ]
then
  #execute code block if condition is true
elif [ 2nd condition ]
  #execute code block if condition is true
else
  #execute code block if both condition are false
fi
```
---

The following types of operators allow you to compare values and determine if a conditon is true or not:
- Numeric operators
- Logical operators
- String operators

---

#### Numeric operators
              
| Operator |          Meaning         |                      
| -------- | ------------------------ |                                
|  `-eq`   | equal to                 |               
|  `-ne`   | not equal to             |                
|  `-gt`   | greater than             |                
|  `-lt`   | less than                |
|  `-ge`   | greater than or equal to |
|  `-le`   | less than or equal to    |

#### Logical Operators

| Operator |                  Meaning                |                      
| -------- | --------------------------------------- |                                
| `&&`     |     AND - if both conditions are true   |               
|    II    |     OR  - if either condition is true   | 

#### String Operators

| Operator |        Meaning        |
| -------- | --------------------- |
|   `==`   | Strings are equal     |
|   `!=`   | Strings aren't equal  |

---

#### Example of numeric operator (If statement)

```bash
age=20
if [ $age -gt 18 ]
then
    echo "You are an adult"
fi
```
#### Example of numeric operator (Elif)

```bash
grade=85
if [ $grade -ge 90 ] 
then
    echo "Excellent"
elif [ $score -ge 80 ]
then
    echo "Well Done"
else
    echo "Better luck next time"
fi
```

#### Example of logical operator

```bash
grade=95
if [ $grade -ge 90 ] && [ $grade -le 100 ]
then
    echo "Excellent"
fi
```

#### Example of string operator

```bash
name="Raheem"
if [ "$name" == "Raheem" ]
then
    echo "Hello Raheem"
fi
```
