--- 
zsh_bang: |-
  1   % ls /user/dir/file.c
  2   % which firefox
  3   % make
  4   % ./foo -f foo.conf
  5   % vi foo.c bar.c
  
  Getting stuff from the previous commands:
  1	Previous command:        % !!  -->% vi foo.c bar.c
  2	Previous command:        % !-1 -->% vi foo.c bar.c
  3	Second previous command: % !-2 -->% ./foo -f foo.conf
  
  Getting individual arguments:
  1	Last arg : % svn ci !$	       -->% svn ci bar.c
  2	All args : % svn ci !*	       -->% svn ci foo.c bar.c
  3	First arg: % svn ci !!:1       -->% svn ci foo.c
  
  Modifying commandlines
  1   Head:       % !ls:$:h            -->% /user/dir
  2   Tail:       % !ls:$:t            -->% file.c
  3   Rm Suffix:  % !ls:$:r            -->% /user/dir/file
  4   Substitute: % !ls:$:s/user/dude/ -->% /dude/dir/file.c
  
  Note: a bang expression can be expanded with the tab key
