--- 
chmod: |-
  chmod: a Unix utility for managing file permissions
  
  Modes can be expressed in octal or human-readable:
  
                            Description | Octal  | Human-readable
      ----------------------------------+--------+---------------
                         Set user write | 200    | u=w
      Set user rwx, group and others rx | 755    | u=rwx,go=rx
                         Add group read | -      | g+w
                     Remove all execute | 111    | a-x
       Set user rws, everyone else none | 4700   | u=rwxs,go-rwx
                        Add user sticky | -      | u+s
                       Add group sticky | -      | g+s
  Octal
  -----
  With three-digit octal notation, each numeral represents a different component of the permission set: user class, group class, and "others" class respectively.
  
  Each of these digits is the sum of its component bits. As a result, specific bits add to the sum as it is represented by a numeral:
  
   * The read bit adds 4 to its total,
   * The write bit adds 2 to its total,
   * The execute bit adds 1 to its total.
  
  Examples
  --------
  
  "-rwxr-xr-x" would be represented as 755 in three-digit octal.
  "-rw-rw-r--" would be represented as 664 in three-digit octal.
  "-r-x------" would be represented as 500 in three-digit octal.
  
  Example: Make foo u=rwx and go=rx:
    $ chmod u=rwx,go=rx foo
  
  Example: Make foo u=rwx and go=rx (in octal):
    $ chmod 755 foo
  
  Example: Find all subdirectories, put them in 'mygroup', make them group sticky:
    $ find . -type d -exec chgrp mygroup \{\} \;
    $ find . -type d -exec chmod g+s \{\} \;
