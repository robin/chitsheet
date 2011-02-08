--- 
zsh_glob: |-
  **/* 	Picks out all files and directories, recursively.
  ***/*	Ditto, following symlinks
  *	Any string, including the null string.
  ?	Any character.
  [...]	Any of the enclosed characters. Ranges of characters can be specified by separating two characters by a -.
  [^...]	Inverse
  [!...]	Inverse
  <x-y>	Any number in the range x to y, inclusive. Either can be omitted.
  ^x	Anything except the pattern x.
  x|y	Either x or y.
  
  x#	Zero or more occurrences of the pattern x.
  x##	One or more occurrences of the pattern x.
  
  (.) 	Files only
  (/)     Directories only
  (@)     Symlinks only
  (x)     Executables only
  (r)     Readable files only
  (w)     Writable files only
  (W)     World-writable files
  (U)     Owned by you
  		
  	dos2unix **/*~*.(gif|png|jpg)(.)     # ~ excludes
  		
  	dos2unix (#i)**/*~*.(gif|png|jpg)(.) # case-insensitive
  
  	ls =bob	                    # Lists file anywhere in $PATH
  
  	ls **/some_file             # Lists file under current directory   
  	zargs -- **/*(.) -- ls -l   # Ditto
