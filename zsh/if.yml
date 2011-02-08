--- 
zsh_if: |-
  if [[ $foo = '' ]]; then
  	print The parameter foo is empty
  fi
  
  # see also -z below
  
  if [[ biriyana = b* ]]; then		
  	print Word begins with a b
  fi
  # quote the term to avoid pattern matching (not regexp, btw)
  
  
  # Numbers
  if [[ $number -gt 3 ]]; then
  if [[ $number -lt 3 ]]; then
  if (( $number > 3 )); then
  if (( 3 )); then	
  
  # Files
  if [[ file1 -nt file2 ]]; then		# newer than
  if [[ file1 -ot file2 ]]; then		# older than
  if [[ file1 -ef file2 ]]; then		# same file
  
  # Variables
  if [[ -z "$var is blah; test fails" ]]; then		# zero length?
  if [[ -n "$var is blah; test passes" ]]; then		# non-zero length?
  
  -a file
  # true if file exists.
  
  -b file
  # true if file exists and is a block special file.
  
  -c file
  # # true if file exists and is a character special file.
  
  -d file
  # #true if file exists and is a directory.
  
  -e file
  # true if file exists.
  
  -f file
  # true if file exists and is a regular file.
  
  -g file
  # true if file exists and has its setgid bit set.
  
  -h file
  # true if file exists and is a symbolic link.
  
  -k file
  # true if file exists and has its sticky bit set.
  
  -n string
  # true if length of string is non-zero.
  
  -o option
  # true if option named option is on. option may be a single character, in which case it is a single letter option name. (See 15.1 Specifying Options.)
  
  -p file
  # true if file exists and is a FIFO special file (named pipe).
  
  -r file
  # true if file exists and is readable by current process.
  
  -s file
  # true if file exists and has size greater than zero.
  
  -t fd
  # true if file descriptor number fd is open and associated with a terminal device. (note: fd is not optional)
  
  -u file
  # true if file exists and has its setuid bit set.
  
  -w file
  # true if file exists and is writable by current process.
  
  -x file
  # true if file exists and is executable by current process. If file exists and is a directory, then the current process has permission to search in the directory.
  
  -z string
  # true if length of string is zero.
  
  -L file
  # true if file exists and is a symbolic link.
  
  -O file
  # true if file exists and is owned by the effective user ID of this process.
  
  -G file
  # true if file exists and its group matches the effective group ID of this process.
  
  -S file
  # true if file exists and is a socket.
  
  -N file
  # true if file exists and its access time is not newer than its modification time.
  
  file1 -nt file2
  # true if file1 exists and is newer than file2.
  
  file1 -ot file2
  # true if file1 exists and is older than file2.
  
  file1 -ef file2
  # true if file1 and file2 exist and refer to the same file.
  
  string = pattern
  string == pattern
  # true if string matches pattern. The `==' form is the preferred one. The `=' form is for backward compatibility and should be considered obsolete.
  
  string != pattern
  # true if string does not match pattern.
  
  string1 < string2
  # true if string1 comes before string2 based on ASCII value of their characters.
  
  string1 > string2
  # true if string1 comes after string2 based on ASCII value of their characters.
  
  exp1 -eq exp2
  # true if exp1 is numerically equal to exp2.
  
  exp1 -ne exp2
  # true if exp1 is numerically not equal to exp2.
  
  exp1 -lt exp2
  # true if exp1 is numerically less than exp2.
  
  exp1 -gt exp2
  # true if exp1 is numerically greater than exp2.
  
  exp1 -le exp2
  # true if exp1 is numerically less than or equal to exp2.
  
  exp1 -ge exp2
  # true if exp1 is numerically greater than or equal to exp2.
  
  ( exp )
  # true if exp is true.
  
  ! exp
  # true if exp is false.
  
  exp1 && exp2
  # true if exp1 and exp2 are both true.
  
  exp1 || exp2
  # true if either exp1 or exp2 is true.
  
  
  # NB Arrays get treated as words separated by spaces.
  
  TBC
