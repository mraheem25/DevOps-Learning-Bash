# If Statements

## If statements allow you to introduce decision making logic into your scripts. They allow you to evaluate conditions and execute different code blocks based on the result of the statement.

#### Structure 
```bash
#!/bin/bash
if [ condition ]
then
  #execute code block if condition is true
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

#### Example of numeric operator

```bash
age=20
if [ $age -gt 18 ]
then
    echo "You are an adult"
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
