--- 
history: |-
  Your history:
  
      % which firefox
      % make
      % ./foo -f foo.conf
      % vi foo.c bar.c
  
  Getting stuff from the last command:
  
      Full line:     % !!            becomes:   % vi foo.c bar.c
      Last arg :     % svn ci !$     becomes:   % svn ci bar.c
      All args :     % svn ci !*     becomes:   % svn ci foo.c bar.c
      First arg:     % svn ci !!:1   becomes:   % svn ci foo.c
  
  Accessing commandlines by pattern:
  
      Full line:     % !./f          becomes:   % ./foo -f foo.conf
      Full line:     % vi `!whi`     becomes:   % vi `which firefox`
      Last arg :     % vi !./f:$     becomes:   % vi foo.conf
      All args :     % ./bar !./f:*  becomes:   % ./bar -f foo.conf
      First arg:     % svn ci !vi:1  becomes:   % svn ci foo.c
