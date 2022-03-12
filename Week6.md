# WEEK-6

### COMMANDS

- `let a=$1+5` = Assignment (Also, `let "a = $1 +5"`)
- `b=$[ $a + 10 ]` = Assignment
- `b=$( expr $a + 20 )` = Assignment
- `b=$(( $a + 10 ))` = Assignment
- `(( b++ ))` = Incrmenting
- `shift` = Shift command line arguments by one left
- `break 2` = Break out of outer loop
- Expr commands
	* `a | b` = Return a if neither argument is null or 0, else return b
	* `a & b` = Return a if neither argument is null or 0, else return 0
	* `[[ $1 =~ $2 ]]` = $1 not equal to $2
	* `$( expr length "$str" )` = Length of string
	* `$( expr substr "$str" n m )` = Sub-string from index n of length m
- Heredoc Feature (Can also have ABC instead of EOF)
	```
	a=2.5
	b=3.2
	c=4
	d=$(bc -l << EOF
	scale = 5
	($a+$b)^$c
	EOF
	)
	
	```
- `#!/bin/usr/gawk -f` = Header for AWK scripts
- Format
	```
	BEGIN{

	}
	{

	}
	END{

	}
	
	```

- AWK Built-in Variables
	* `ARGC` = No. of arguments supplied
	* `ARGV` = Array of cmd. line arguments
	* `ENVIRON` = Associative array of env. var.
	* `FILENAME` = Current filename being processed
	* `FNR` = Record no. being processed, relative to current file
	* `FS` = Field separator
	* `NF` = No. of fields
	* `NR` = No. of records
	* `OFMT` = Output format for no.'s
	* `OFS` = Output field separator
	* `ORS` = Output record separator
	* `RS` = Record separator
	* `$0` = All fields of record
	* `$n` = nth field of record