--- 
darcs: |-
  Creating a new repository:
    $ mkdir ProjectDirectory
    $ cd ProjectDirectory
    $ darcs init
  
  Creating a new repository for an existing project:
    $ cd ExistingProject
    $ darcs init
    $ darcs add -r *
    $ darcs record -m "Initial import of ExistingProject."
  
  Status:
    $ darcs whatsnew -l
  
  Committing changes:
    $ darcs record
  
  Creating a patch for a darcs repository:
    $ darcs send http://gnufoo.org/darcs/physics2d; # Sends the maintainer an email
    $ darcs send -o patch.diff http://gnufoo.org/darcs/physics2d; # Creates a patch file
  
  Creating a patch for a non-darcs repository:
    $ darcs changes --last 2; # Make sure you're picking up the right patches.
    $ darcs diff -u --last 2 > patch.diff;
  
  Rollback:
    $ darcs unrecord
  
  Making a new copy of a repository (you can treat it like a branch):
    $ darcs get ProjectDirectory RadicalRefactor
    $ cd RadicalRefactor; # Go nuts!
  
  Checking out from an external repository:
    $ darcs get http://gnufoo.org/darcs/dynamorph
  
  Creating a tarball:
    $ darcs dist
  
  Exposing repository to the web (just copy up to your webspace; no server needed):
    $ tar cfz ProjectDirectory.tgz ProjectDirectory
    $ scp ProjectDirectory.tgz yourhost.org:your/web/directory
    Now people can grab your repository with: 
    $ darcs get http://yourhost.org:your/web/directory/ProjectDirectory
  
  Updating your repository on the web:
    $ cd dynamorph-local
    $ darcs push gnufoo.org:www/darcs/dynamorph; # uses scp to copy (requires darcs on the other machine)
