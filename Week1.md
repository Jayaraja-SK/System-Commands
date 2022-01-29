# WEEK-1

### COMMANDS

- `pwd`  = Present working direc.
- `ls` = List all file name in pwd
	* `ls -a` = Also lists hidden files
	* `ls -l` = Long format
	* `ls -i` = Inode no. of files (Entry in filesystem table and unique for different files. If same, then they're hard-link)
	* `ls -li` = Inode no. and Long format (Also, `ls -l -i` can be used)
- `ps` = List of proc. running
- `uname` = Name of O.S.
- `whoami` = Username
- `clear` = Clear screen (Ctrl+L)
- `exit` = Close terminal (Ctrl+D)
- `man cmd_name` = Manual
	* `man option_no cmd_name` = Only the particular section of the manual for the cmd is displayed
- `cd` = Home direc.
	* `cd ..` = Parent direc.
	* `cd ~` = Home direc.
	* `cd -` = Previous working direc.
	* `cd path_name` = Go directly to the direc. by specifying path
	* `cd direc_name` = Go to sub-direc. present in pwd
- `date` = Date and time
	* `date -R` = E-Mail communication time
- `cal` = Calendar of current month
	* `cal month year` = Calendar of given month and year (Eg. month - aug or Aug or 8, year = 2012)
	* `ncal` = Different orientation
- `free` = Stats. of machine (Amount of memory available)
	* `free -h` = Stats. in human readable form
- `groups` = Groups to which current user belongs to
- `chmod option filename` = Change permission for a file
	* `chmod g-w filename` = Remove write permission for the file
	* `chmod u+x filename` = Give executable permission for user for the file
	* `chmod o-r filename` = Remove read permission for other users for the file
	* `chmod 700 filename` = Give all permissions to user and remove all permissions for group and others
- `touch filename` = Create an empty file if it doesn't exists
- `cp old_filename new_filename` = Copy contents of one file to a new file
- `mv path_of_file new_path` = Move file from one direc. to another
- `mv old_filename new_filename` = Rename file (Use "" to use more than two words for file name)
- `rm filename` = Remove file
	* `rm -i filename` = Ask user to remove file or not (Interactive  mode)
- `mkdir` = Create a directory
- `rmdir` = Remove an empty directory
- `less filename` = Display only the 1st few lines of a file (Click "q" to leave)


### OUTPUT OF ls -l

- `drwxr-xr-x 5 steve steve 12288 Dec 20 10:00 Document` = FileType|OwnerPermission|GroupPermission|OtherPermission|NumberOfHardLinks|Owner|Group|Size|LastModifiedTimeStamp|FileName 

- FILE TYPES
	* `-` = Regular file
	* `d` = Directory
	* `l` = Symbolic link
	* `c` = Char. file
	* `b` = Block file
	* `s` = Socket file
	* `p` = Named pipe

- FILE PERMISSIONS
	* `rwx` = 7
	* `rw-` = 6
	* `r-x` = 5
	* `r--` = 4
	* `-wx` = 3
	* `-w-` = 2
	* `--x` = 1




### FILE SYSTEM HIERARCHY

- `/`
	* `sbin` = Essential system binaries
	* `media` = Mount points for removable devices
	* `bin` = Essential cmd. binaries
	* `etc` = Host specific system config.
		* `apt`
	* `home`
		* `user`
	* `tmp` = Temporary files
	* `usr` = Secondary hierarchy
		* `bin` = User commands
		* `sbin` = Non-vital system binaries
		* `share` = Arch. dependent data
		* `include` = Header files of C programs
		* `src` = Source code
		* `lib` = Libraries
	* `lib` = Essential shared lib. and kernel modules
	* `var` = Variable data
		* `cache` = App. cache data
		* `lock` = Lock files
		* `log` = Log files and direc.
		* `run` = Data relevant to running proc.
		* `tmp` = Temp. files preserved b/w reboots
		* `lib` = Var. state info
		* `local` = Var. data for /usr/local
	* `mnt`  = Mount points
	* `opt` = Add-on application software packages
	* `boot` = Static files of device loader
	* `srv` = Data for services
