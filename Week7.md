# WEEK-7

### COMMANDS

- `#!/usr/bin/sed -f` = Header for SED
- Actions
	* `p` - Print pattern space
	* `d` = Delete pattern space
	* `s` = Substitute using regex match (`s/pattern/replacement/g`)
	* `=` = Print current input line no.
	* `i` = Insert above current line
	* `a` = Append below current line
	* `c` = Change current line
	* `:label` = Specify location of label for branch command
	* `blabel` = Branch unconditionally to label
- `sed -e "" file_name` = Print file contents when nothing is specified
- `sed -n -e "" file_name` = Don't print anything in default
- `sed -n -e "5p" file_name` = Print only 5th line
- `sed -n -e '5!p' file_name` = Skip 5th line
- `sed -n -e '$!p' file_name` = Don't print last line
- `sed -n -e '5,8p' file_name` = Print 5th to 8th line
- `sed -n -e '=; 5,8p' file_name` = Print 5th to 8th line along with all lines no.'s
- `sed -n -e '5,8{=;p}' file_name` = Print 5th to 8th line along with corresponding line no.'s
- `sed -n -e '1~3p' file_name` = From 1st line, print lines by skipping 3 lines
- `sed -n -e '/microsoft/p'` = Lines matching `microsoft` would be printed
- `sed -n -e '/microsoft/+2p' file_name` = Lines matching `microsoft` would be printed, along with 2 lines after each match
- `sed -e '5d' file_name` = Delete 5th line
- `sed -e '5,8d' file_name` = Delete 5th to 8th line
- `sed -e '$d' file_name` = Delete last line
- `sed -e '/microsoft/d'` = Lines matching `microsoft` would be deleted
- `sed -e 's/microsoft/Microsoft/g'` = Lines matching `microsoft` would be replaced with given word
- `sed -e '1s/microsoft/Microsoft/g'` = Only 1st line with `microsoft` would be replaced with given word
- `sed -e '1,5s/microsoft/Microsoft/g'` = 1st line to 5th line with `microsoft` would be replaced with given word
- `sed -E -e '3,6s/^L[[:digit:]]+ //g'` = 3rd line to 6th line will be replaced with none, matching the extended grep
- `sed -E -e '3,/symbolic/s/^L[[:digit:]]+ //g'` = 3rd line to line with symbolic will be replaced with none, matching the extended grep
- `sed -E -e '1~3s/^L[[:digit:]]+ //g'` = Every 3rd line from 1st line until last will be replaced with none, matching the extended grep
- `sed -E -e '/text/,/video/s/^L[[:digit:]]+ //g'` = From line with word `text` to line with `video` will be replaced with none, matching the extended grep 
- `sed -e '1i -----header-----'` = Inserts an header at 1st line
- `sed -e '1i -----header-----' -e '$a -----footer-----'` = Inserts an header at 1st line and footer after last line
- `sed -e '/microsoft/i -----header-----'` = Inserts an header at all lines that has the word `microsoft`
- `sed -e '1~5i ---break---'` = Insert a line after every 5 lines starting from 1st line
- `sed -e '/microsoft/c -----change-----'` = Change the lines that has the word `microsoft`