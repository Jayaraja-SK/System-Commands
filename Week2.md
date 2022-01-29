# WEEK-2

### COMMANDS

- `more file_name` = Similar to less but shows progress and exits automatically on reaching End of File
- `cat file_name` = Displays all contents of file
	* `cat > file_name` = Create new file and add contents to it. If file already exists, then overwrite with new contents
	* `cat >> file_name` = Append contents to existing file. If file doesn't exists, then create new file and add the contents
- `head file_name` = Displays 1st 10 lines of file
	* `head -n x file_name` = Displays 1st x no. of lines
- `tail file_name` = Displays last 10 lines of file
	* `tail -n x file_name` = Displays last x no. of lines
- `wc file_name` = No. of lines, word and byte count of file
	* `wc -l file_name` = No. of lines in file
- `which cmd_name` = Location of command
- `whatis cmd_name` = Brief description of command
- `apropos keyword` = List of cmd_names and their brief descriptions which has the matching keyword given in the command. Equivalent to `man -k`
- `info` = List of all available commands along with manual
- `alias new_cmd='cmd'` = Creates a new command (Eg. `alias ll='ls -l'`)
	* `alias` = List of all aliases
	* `unalias new_cmd` = Removes the alias
- `type cmd`
- `ln -s old_file new_file` = Soft link for original file (Different Inode no.'s)
- `ln old_file new_file` = Hard link for original file (Same Inode no.'s)
- `stat file_name` = File size, Time stamp and no. of blocks
- `du file_name` = File size
	* `du -h file_name` = File size in human-readable form
- `cat /proc/version` = Similar to `uname -a`
- `cat /proc/meminfo` = Similar to `free`
- `cat /proc/partitions` = Similar to `df -h`
- `echo hello, world` = Prints "hello, world" to screen
	* `echo "hello,      world"` = Prints with spaces. If no quotes, then more than one space would be treated as one space
	* `echo "hello, '` = Asks for input until matching quote is found
	* `echo $HOSTNAME` = Displays the shell-var. Also, `echo "$HOSTNAME"` can be used
	* `echo '$HOSTNAME'`= Displays the string - "$HOSTNAME" rather than the var.
	* `echo "\$HOSTNAME"` = Displays "$HOSTNAME"
	* `echo {a..z}` = Displays all character from a to z, separated by space
	* `echo *` = List all files in current direc.
- `printenv` = Displays all available shell variables
	* `printenv VAR` = Displays value of the var. (No need of "$" symbol)
- `env` = Displays all available shell variables
- `set` = Make changes to shell env. var.
- `ps` = Snapshot of current running processes
	* `ps --forest` = Shows which parent process has started a child process
	* `ps -ef` = Processes running in O.S.
	* `ps -A` = Display info. about other user's proc.
	* `ps -d` = Similar to `ps -A`, but excludes session loaders
	* `ps -a` = Display info. about other user's proc. including own
	* `ps -t` = Display info. about proc. attached to specified terminal devices
	* `ps -r` = Sort by current C.P.U. usage
	* `ps -p` = Display info. about proc. which match specified pid
- `history` = List of all commands runned previously
	* `!number` = Repeat the command once again from history by using the number
- `bc` = Starts a calculator (Terminate using Ctrl+D)



### SHELL VARIABLES

- `$HOME` = Home direc.
- `$USERNAME` = Name of current user
- `$HOSTNAME` = Name of host
- `$PWD` = Current working direc.
- `$PATH` = Displays all path var.
- `$USER` = Username associated with current session
- `$0` = Name of shell
- `$$` = Process I.D. of shell
- `$?` = Return code of previously run program
- `$-` = Flags set in bash shell


### PROGRAM EXIT CODES

##### Note: Exit code lies between [0,255]. If not in range, then find exit code modulo 256

- `0` = Success
- `1` = Failure
- `2` = Misuse
- `126` = Command cannot be executed
- `127` = Command not found
- `130` = Process killed using Ctrl-C
- `137` = Process killed using kill -9 p_id


### FLAGS SET IN BASH

- `h` = Locate and hash cmd's
- `B` = Brace expansion enabled
- `i` = Interative mode
- `m` = Job control enabled
- `H` = Style history substitution enabled
- `s` = Commands read from stdin
- `c` = Commands read from arguments


### PROCESS MANAGEMENT

- `sleep x` = Terminal gets suspended for x seconds (No control)
	* `sleep x &` = Run the process for x seconds in background
- `coproc sleep x` = Process runs in background and control is not lost
- `kill` = Kills all the processes
	* `kill -9 process_id` = Killing the given process
- `fg` = Brings the process running in background to foreground (Ctrl-Z to stop) (Shell built-in)
- `jobs` = Lists out the processes that are currently running
- `top` = Lists out the process that's occupying more space


### RUN MULTIPLE COMMANDS

- `cmd_1 ; cmd_2 ; cmd_3` = Output is printed on consecutive lines
- `cmd_1 ; cmd_2 ; cmd_3;`