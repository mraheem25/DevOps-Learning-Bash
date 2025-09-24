# Arithmetic Expansion

## Bash allows mathematical calculations to be formed using the following notation `$((calculation))`. Calculations can be performed by accessing variables or passing paarmeters.

#### Arithmetic Expansion with variables
`#!/bin/bash`\
`length=5`\
`width=8`\
`area=$((length * width))`\
`perimeter=$((2*(length + width)))`\
`echo "The area is $area"`\
`echo "The perimeter is $perimeter"`

#### Arithmetic Expansion with parameters
User runs `./my_script.sh 5 10`\
`#!/bin/bash`\
`length="$1"`\
`width="$2"`\
`area=$((length * width))`\
`perimeter=$((2*(length + width)))`\
`echo "The area is $area"`\
`echo "The perimeter is $perimeter"`
