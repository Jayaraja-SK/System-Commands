# WEEK-5

### COMMANDS

- `./filename` = Command to execute a script file
- `#!/bin/bash` = Header for bash-script
- Display Output
	* `echo "My name is $var"`
	* `printf "My name is %s\n" $var`
- `read var` = Read a variable
- Shell Script Arguments
	* `$0` - Name of shell program
	* `$#` - No. of arguments passed
	* `$1` - 1st argument (Also, `${1}`)
	* `$*` - All arguments at once (Also, `$@`)
	* `"$*"` - All arguments as a single string
	* `"$@"` - All arguments as separate string
- `var=$(cmd)` = Command is executed and substituted in the variable (Also, var=`cmd`)
- `IFS = ' '` = Default input field separator
- `var=$(($var1+$var2))` = Evaluate a expression and assignment

- For Loop
	```	
	for var in list
	do
		commands
	done
	
	```

	```	
	for ((var=0;var<10;var++))
	do
		commands
	done
	
	```


- If Loop
	```
	if condition
	then
		commands
	fi	
	
	```

	```
	if condition; then
		commands
	fi	
	
	```

	```
	if condition
	then
		commands
	elif condition
	then
		commands
	else
		commands
	fi	
	
	```

- While Loop
	```
	while condition
	do
		commands
	done
	
	```


- Case Statement
	```
	case var in
	pattern1)
		commands
		;;
	pattern2)
		commands
		;;
	pattern3)
		commands
		;;
	esac
	
	```

- Numeric Comparisons
	* `$n1 -eq $n2` = Check if n1 equals n2
	* `$n1 -ge $n2` = Check if n1 is greater than or equal to n2
	* `$n1 -gt $n2` = Check if n1 is greater than n2
	* `$n1 -le $n2`
	* `$n1 -lt $n2`
	* `$n1 -ne $n2` = n1 not equals to n2

- String Comparisons (Eg. (($# !=2 )))
	* `$str1 = $str2` = Check if str1 equals str2
	* `$str1 != $str2` = Check if str1 not equals str2
	* `$str1 < $str2` = Check if str1 is less than str2
	* `$str1 > $str2`
	* `-n $str1` = Check if length of str1 is not zero
	* `-z $str1` = Check if length of str1 is zero

- Unary file Comparisons (Eg. [ -w $1 ])
	* `-e file` = Check if file exists
	* `-d file` = Check if File is directory
	* `-f file` = Check if File exists and is a file
	* `-r file` = Check if File exists and has read permission
	* `-w file`
	* `-x file`
	* `-O file` = File exists and is owned by current user
	* `-G file` = Check if file exists and default group is same as that of current user

- Binary File Comparisons
	* `file1 -nt file2` = Check if file1 is newer than file2
	* `file1 -ot file2` = Check if file1 is older than file2