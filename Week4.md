# WEEK-4


### SOFTWARE MANAGEMENT

##### NEED FOR PACKAGE MANAGER
- Tools for installing, updating, deleting and managing a software


##### PACKAGE TYPES
- `package`
	* `RPM`
		* `Red Hat`
			* `CentOs`
			* `Fedora`
			* `Oracle Linux`
		* `SUSE Enterprise Linux`
			* `openSUSE`
	* `DEB`
		* `Debian`
			* `Ubuntu`
				* `Mint`
			* `Knoppix`


### COMMANDS

- `lsb_release -a` = Type of O.S.
- `apt-cache pkgnames` = List all packages
- `apt-cache search keyword` = Search packages w.r.t.keyword
- `apt-cache show -a package` = Display package records of a package
- `/etc/apt` = Folder - sources.list.d, File - sources.list
	* `apt-get update` = Sync. package overview files
	* `apt-get upgrade` = Upgrade all installed packages
	* `apt-get install package` = Install a package
	* `apt-get reinstall package` = Re-install a package
	* `apt-get autoremove` = Remove packages that were automatically installed to satisfy a dependency
	* `apt-get clean` = Clean local repo. of retrieved packages
	* `apt-get remove` = Remove package
	* `apt-get purge package` = Remove package files from system
- `/var/lib/dpkg` = Folder - info, File - arch, available and status
	* `dpkg -l pattern` = List all packages whose name match the pattern
	* `dpkg -L package` = List installed files that came from packages
	* `dpkg -s package` = Report status of package
	* `dpkg -S pattern` = Search installed packages for a file
	* Uninstalling packages using `dpkg` is not recommended
- `grep pattern filename` = Pattern from given file
	* `cmd | grep pattern`
	* `.` = Any single character except null or newline
	* `grep -E pattern filename` = Extended grep
	* `*` = Zero or more characters
	* `^` = Beginning of line
	* `$` = End of line
	* `\` = Esc. special char.
	* `\b` = Word boundary (Empty Space)
	* `[]` = Any of char's in range or negation of char's in range
	* `\{n,m\}` = Atleast n times and utmost m times
	* `\( \)` = Grouping of reg. exp.
- `egrep pattern filename` = Extended grep
	* `{n,m}` = Range of occur. of preceding pattern atleasr n times and utmost m times
	* `+` = One or more of preceding char.
	* `?` = Zero or more of preceding char.
	* `()` = Grouping of expression
	* `|` = Logical OR over patterns
- Character classes
	* `[[:print:]]` = Printable
	* `[[:alnum:]]` = Alpha-numeric
	* `[[:alpha:]]` = Alphabetic
	* `[[:lower:]]` = Lower case
	* `[[:upper:]]` = Upper case
	* `[[:digit:]]` = Decimal digits
	* `[[:blank:]]` = Space/Tab
	* `[[:space:]]` = Whitespace
	* `[[:punct:]]` = Punctuation
	* `[[:cntrl:]]` = Control char's
	* `[[:graph:]]` = Non-space
	* `[[:xdigit:]]` = Hexa-decimal
- `cut -c 1-3 filename` = 1st three char's of a line
	* `cut -c -3 filename` = 1st three char's of a line
	* `cut -d " " -f 1-3` = 1st three fields of a file


### PACKAGE PRIORITIES

- `required` = Essential for proper functioning of system
- `important` = Provides functionality that enables system to run well
- `standard` = Included in system installation
- `optional` = Can omit if there is un-sufficient storage
- `extra` = Can conflict with packages with higher priority and install only if needed


### CHECKSUMS (TO VERIFY PACKAGE AUTHENTICITY)

- `md5sum` - 128 bit
- `SHA1` - 160 bit
- `SHA256` - 256 bit