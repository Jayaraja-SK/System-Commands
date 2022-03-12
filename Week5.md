# WEEK-5

### COMMANDS

- `./filename` = Command to execute a script file
- `#!/bin/bash` = Header file for bash-script
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
- For Loop
	```	for var in list
		do
			commands
		done
	
	```