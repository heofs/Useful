# Bash Scripting

## For loops
```bash
#!/bin/bash

array=("1" "2" 3)

for i in ${array[@]}; do
	echo $i
done

array="5 6 7"
for i in ${array}; do
	echo $i
done
```

## If-Else
```bash
#!/bin/bash

test="hi my name is Steve"

if echo ${test} | grep hi > /dev/null; then
	echo variable test contains the word 'hi'
else
	echo variable test does not contain the word 'hi'
fi

if [ -n "${test}" ]; then
	echo "variable 'test' is not empty"
fi

if [ -z "${test}" ]; then
	echo "variable is empty"
fi
```

## Print directory
```bash
#!/bin/bash

output=$(ls)							# Puts output of ls into variable
for i in ${output}; do
    if [[ -d $i ]]; then
        echo -e $i "\t is a directory."
    fi
    if [[ -f $i ]]; then
        echo -e $i "\t is a file."
    fi
	
done
```
