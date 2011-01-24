--- 
svn: |-
  Creating a new repository:
    mkdir /path/to/new/dir
    svnadmin create /path/to/new/dir
  Starting svnserve:
  	svnserve --daemon --root /path/to/new/repository
  Importing project into svn repo:
    $ svn import -m "Wibble initial import" svn://olio/wibble/trunk
  Creating directory in svn repo:
    $ svn mkdir -m "Create tags directory" svn://olio/wibble/tags
  Branching:
    $ svn copy http://svn.example.com/repos/calc/trunk \
             http://svn.example.com/repos/calc/branches/my-calc-branch \
        -m "Creating a private branch of /calc/trunk."
    Committed revision 341.
  
  Diff / Merge:
   $ svn diff -rHEAD filename # changes in repository
   $ svn diff -rPREV:BASE filename # most recent change
   $ svn diff -r 343:344 http://svn.example.com/repos/calc/trunk
   $ svn merge -r 343:344 http://svn.example.com/repos/calc/trunk
   U  integer.c
   $ svn status
   M  integer.c
  
  Rollback:
    $ svn merge -r 100:99 .
    $ svn commit -m "Rollback to revision 99"
    Committed revision 101.
  
  Make a patch against the rails source:
    (in /vendor/rails/) $ svn diff > your_patch_name.diff
  
  Edit a dir's ignores:
   $ svn propedit svn:ignore your_dir_name
  Set a dir's ignores:
   $ svn propset svn:ignore "ignore1 ignore2" your_dir_name
  
  Switch a working copy to another URL
   $ svn switch --relocate http://server1:/svn/trunk/ http://server2/svn/trunk/ .
  
  Add all unversioned files in your working copy
   $ svn add --force .
  
  See all local changes live in a terminal
   $ watch 'svn st --ignore-externals|grep -v ^X'
  
  Find all new files, or unversioned files
   $ svn status | grep "^\?" | awk "{print \$2}"
  
  Find all changes, ignoring unversioned files
   $ svn status -uv 2>/dev/null | egrep "^([^\? ]|       \*)"
   (There are 7 spaces before the \*, which don't show up on some browsers)
  
  Set up externals dependency
    $svn propset svn:externals "dataacccess svn://olio/dataaccess/trunk" maitai
  	$svn commit -m "Added dataaccess project as an external"
  
  Log:
   $ svn log -v filename
   $ svn log -r6 filename
   $ svn log --stop-on-copy
  
  File statuses:
   C  - Conflict
   G  - Merged our changes with update (locally)
   U  - Updated a file
   UU - Update to file AND properties
   M  - Modified
   A  - Added
   D  - Deleted
  
  Resolve Conflicts:
   $ cp Number.txt.mine Number.txt; svn resolved Number.txt
   $ svn revert Number.txt
  
  Additional Commands:
   $ svn add --non-recursive directory_name
   $ svn co -r7 url directory
   $ svn propedit svn:ignore *.bak
