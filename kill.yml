--- 
kill: |-
  Signals you can send with kill:
  
  Name     Num   Action    Description
  
  0          0   n/a       exit code indicates if a signal may be sent
  ALRM      14   exit
  HUP        1   exit
  INT        2   exit
  KILL       9   exit      this signal may not be blocked
  PIPE      13   exit
  POLL           exit
  PROF           exit
  TERM      15   exit
  USR1           exit
  USR2           exit
  VTALRM         exit
  STKFLT         exit      may not be implemented
  PWR            ignore    may exit on some systems
  WINCH          ignore
  CHLD           ignore
  URG            ignore
  TSTP           stop      may interact with the shell
  TTIN           stop      may interact with the shell
  TTOU           stop      may interact with the shell
  STOP           stop      this signal may not be blocked
  CONT           restart   continue if stopped, otherwise ignore
  ABRT       6   core
  FPE        8   core
  ILL        4   core
  QUIT       3   core
  SEGV      11   core
  TRAP       5   core
  SYS            core      may not be implemented
  EMT            core      may not be implemented
  BUS            core      core dump may fail
  XCPU           core      core dump may fail
  XFSZ           core      core dump may fail
  
  Taken from the kill man page on Linux.
  
  (According to Larry Wall, avoid kill -9.  Instead try 15 and wait a couple seconds, then 2 then 1 to allow the proces a chance to end clenaly.)
