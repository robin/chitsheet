--- 
bash_scripting: |-
  -z "string"   	 String has zero length
  -n "string" 	String has non-zero length
  
  Note
  
  To check whether a variable is set and not blank, use -n "${BLAH}" rather than -n $BLAH. The latter will cause problems in some situations if the variable is unset. 
  
  Integer Comparison in bash
  
  The general form of integer comparisons is int1 -operator int2. The following are available:
  Operator 	Purpose
  -eq 	Integer equality
  -ne 	Integer inequality
  -lt 	Integer less than
  -le 	Integer less than or equal to
  -gt 	Integer greater than
  -ge 	Integer greater than or equal to
  File Tests in bash
  
  The general form of a file test is -operator "filename". The following are available (lifted from man bash):
  Operator 	Purpose
  -a file 	Exists (use -e instead)
  -b file 	Exists and is a block special file
  -c file 	Exists and is a character special file
  -d file 	Exists and is a directory
  -e file 	Exists
  -f file 	Exists and is a regular file
  -g file 	Exists and is set-group-id
  -h file 	Exists and is a symbolic link
  -k file 	Exists and its sticky bit is set
  -p file 	Exists and is a named pipe (FIFO)
  -r file 	Exists and is readable
  -s file 	Exists and has a size greater than zero
  -t fd 	        Descriptor fd is open and refers to a terminal
  -u file 	Exists and its set-user-id bit is set
  -w file 	Exists and is writable
  -x file 	Exists and is executable
  -O file 	Exists and is owned by the effective user id
  -G file 	Exists and is owned by the effective group id
  -L file 	Exists and is a symbolic link
  -S file 	Exists and is a socket
  -N file 	Exists and has been modified since it was last read
  File Comparison in bash
  
  The general form of a file comparison is "file1" -operator "file2". The following are available (lifted from man bash):
  Operator 	Purpose
  file1 -nt file2 	file1 is newer (according to modification date) than file2, or if file1 exists and file2 does not.
  file1 -ot file2 	file1 is older than file2, or if file2 exists and file1 does not.
  file1 -ef file2 	file1 and file2 refer to the same device and inode numbers.
  Boolean Algebra in bash
  
  There are constructs available for boolean algebra ('and', 'or' and 'not'). These are used outside of the [[ ]] blocks. For operator precedence, use ( ).
  Construct 	Effect
  first || second 	first or second (short circuit)
  first && second 	first and second (short circuit)
  ! condition 	not condition
  
  Note
  
  These will also sometimes work inside [[ ]] constructs, and using ! before a test is fairly common. [[ ! -foo ]] && bar is fine. However, there are catches -- [[ -f foo && bar ]] will not work properly, since commands cannot be run inside [[ ]] blocks.
  
  Inside [ ] blocks, several -test style boolean operators are available. These should be avoided in favour of [[ ]] and the above operators.
  
  To download files that have zero-padded filenames (bob002.jpg etc. in this example):
  
  for i in `seq -f "%03g" 1 100`; do wget http://www.example.com/bob$i.jpg; done
  
  Change the seq formatting options for more or less padding.
  
  Arrays in bash:
  
  zombies=(bob tom)
  zombies[10]='helen'
   
  echo 'zombie 0 is' ${zombies[0]}
  #zombie 0 is bob
   
  for name in ${zombies[@]}
  do
    echo $name 'is a zombie'
  done
  #bob is a zombie
  #tom is a zombie
  #helen is a zombie
   
  for (( i=0; i < ${#zombies[@]}; i++ ))
  do
    echo 'zombie' $i 'is' ${zombies[$i]}
  done
  #zombie 0 is bob
  #zombie 1 is tom
  #zombie 3 is
