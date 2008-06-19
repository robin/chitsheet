--- 
ditz: |-
  Ditz is a simple, light-weight distributed issue tracker designed to work with
  distributed version control systems like darcs and git. Ditz maintains an issue database file on disk, written in a line-based and human-editable format. This file is kept under version control, alongside project code.  Changes in issue state is handled by version control like code change: included as part of a commit, merged with changes from other developers, conflict-resolved in the standard manner, etc.
  
  Ditz provides a simple, console-based interface for creating and updating the
  issue database file, and some rudimentary HTML generation capabilities for producing world-readable status pages. It offers no central public method of
  bug submission.
  
  == SYNOPSIS
  
  # set up project. creates the bugs.yaml file.
  1. ditz init
  2. ditz add-release
  
  # add an issue
  3. ditz add
  
  # where am i?
  4. ditz status
  5. ditz todo
  
  # do work
  6. write code
  7. ditz close <issue-id>
  8. commit
  9. goto 3
  
  # finished!
  10. ditz release <release-name>
