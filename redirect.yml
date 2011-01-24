--- 
redirect: |-
  # Send contents of file to command
  $ command < file	
  
  # Redirect Stderr twice		
  $ command 2> file2 > file1 2>&1	
  
  # Text to Stdin (command)
  $ command << 'text'				
  
  # Redirect both Stdout and Stderr to file
  $ command > file 2>&1		
  
  # Redirect Stdout to one file and Stderr to another
  $ command > file1 2> file2	
  
  # Pipe Stdout and Stderr to another process	
  $ command 2>&1 | command2			
  
  $ less <(gzip -cd foo.gz)
  $ gzip -cd foo.gz && less foo
  
  # Redirect an error
  $ echo An Error >&2 2>&1 | sed -e 's/A/I/'
  
  # Duplicate output
  $ command | tee file1 > file2
