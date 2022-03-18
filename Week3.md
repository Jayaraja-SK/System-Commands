# WEEK-3

### COMMANDS

- `cmd_1 ; cmd_2 ; cmd_3` = Execute cmd's one after other
- `cmd_1 && cmd_2` = 2nd cmd. is executed only if 1st cmd. is succeeded
- `cmd_1 || cmd_2` = 2nd cmd. is executed only if 1st cmd. is un-successful
- `myvar="value string"` = Creating a var. (No space near "=")
- `export myvar` = Make it available for shell (Also, `declare -x myvar` can be used)
- `echo $myvar` = Displaying var. (Also, `echo ${myvar`})
- `unset myvar` = Removing value of var.
- `[[ -v myvar ]]; echo $?` = 0 - Success (Var. is set), 1- Failure (Var. is not set)
- `[[ -z ${myvar} ]]; echo $?` = 0 - Success (Var. is not set), 1- Failure (Var. is set)
- `echo ${myvar:-"default"}` = If var. is set, display its value, else display "default"
- `echo ${myvar:="default"}` = If var. is set, display its value, else set "default" as its value and display
- `echo ${myvar:+"default"}` = If var. is set, then set "default" as its new value and display its value, else don't display anything
- `echo ${!H*}` = List of names of shell starting with H
- `echo ${#myvar}` = Length of var.
- `echo ${myvar:x:y}` = Display y characters of string by skipping 1st x characters
- `echo ${myvar#pattern}` = Remove matching prefix pattern once
- `echo ${myvar##pattern}` = Remove matching prefix pattern max. times
- `echo ${myvar%pattern}` = Remove matching suffix pattern once
- `echo ${myvar%%pattern}` = Remove matching suffix pattern max. times
- `echo ${myvar/pattern/string}` = Replace matching pattern once
- `echo ${myvar//pattern/string}` = Replace matching pattern max. times
- `echo ${myvar/#pattern/string}` = Replace matching pattern at beg.
- `echo ${myvar/%pattern/string}` = Replace matching pattern at end
- `echo ${myvar,}` = Change 1st char. to lower case
- `echo ${myvar,,}` = Change all char's to lower case
- `echo ${myvar^}` = Change 1st char. to upper case
- `echo ${myvar^^}` = Change all char's to upper case
- `declare -i myvar` = Only integers assigned
- `declare -l myvar` = Only lower case char's assigned
- `declare -u myvar` = Only upper case char's assigned
- `declare -r myvar` = Var. is only read only. Once declared, cannot be un-done
- `declare +i myvar` = Integer restriction removed
- `declare +l myvar` = Lower case char's restriction removed
- `declare +u myvar` = Upper case char's restriction removed
- `declare -a arr` = Declaring an array
	* `$arr[0]="string"` = Assigning
	* `echo ${arr[0]}` = Displaying value at 0th index
	* `echo ${#arr[@]}` = No. of elements in arr.
	* `echo ${!arr[@]}` = Display all indices used
	* `echo ${arr[@]}` = Display all elements in arr.
	* `arr+=("value")` = Append an element to end of arr
	* `unset arr[0]` = Removing
- `declare -A hash` = Declaring an associative arr.
	* `hash["a"]="value" = Assigning a value to a key`
	* `echo ${hash["a"]}` = Value of given key
	* `echo ${#hash[@]}` = No. of elements
	* `echo ${!hash[@]}` = Keys used
	* `echo ${hash[@]}` = Display values of all elements
	* `unset hash["a"]` = Delete element with given key



### REDIRECTIONS

- `0` = stdin
- `1` = stdout
- `2` = stderr
- `cmd > file1`
	* keyboard - stdin
	* stdout - file1
	* stderr - display
- `cmd >> file1`
	* keyboard - stdin
	* stdout - file1
	* stderr - display
- `cmd 2> file1`
	* keyboard - stdin
	* stdout - display
	* stderr - file1
- `cmd > file1 2>file2`
	* keyboard - stdin
	* stdout - file1
	* stderr - file2
- `cmd < file1`
	* file1 - stdin
	* stdout - display
	* stderr - display
- `cmd > file1 2>&1`
	* keyboard - stdin
	* stdout - file1
	* stderr - file1
- `cmd_1 | cmd_2`
	* keyboard - stdin for cmd_1
	* stdout of cmd_1 - stdin for cmd_2
	* stderr of cmd_1 - display
	* stdout of cmd_2 - display
	* stderr of cmd_1 - display
- `cmd_1 | cmd_2 > file1`
	* keyboard - stdin for cmd_1
	* stdout of cmd_1 - stdin for cmd_2
	* stderr of cmd_1 - display
	* stdout of cmd_2 - file1
	* stderr of cmd_1 - display
- `cmd > file1 2> /dev/null`
	* keyboard - stdin
	* stdout - file1
	* stderr - /dev/null
- `cmd_1 | tee file1`
	* keyboard - stdin for cmd_1
	* stdout of cmd_1 - stdin for cmd_2
	* stderr of cmd_1 - display
	* stdout of cmd_2 - file1 and display
	* stderr of cmd_1 - display