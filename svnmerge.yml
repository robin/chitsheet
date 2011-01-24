--- 
svnmerge: |-
  Development Branch:
  
    Prepare branch
  
    $ svn co <branch url> branch
    $ cd branch
    $ svnmerge.py init
    $ svn ci -F svnmerge-commit-message.txt
    $ rm svnmerge-commit-message.txt
  
    Merge branch
  
    $ svnmerge.py merge
  
    See available changes
  
    $ svnmerge.py avail               # show only the revision numbers
    $ svnmerge.py avail --log         # show logs of the revisions
    $ svnmerge.py avail --diff        # show diffs of the revisions
  
  Merging Back To Trunk:
  
    Prepare trunk
  
    $ svn co <trunk url> trunk
    $ cd trunk
    $ svnmerge.py init <branch url>
    $ svn ci -F svnmerge-commit-message.txt
    $ rm svnmerge-commit-message.txt
  
    Merge trunk
  
    $ svnmerge.py merge --bidirectional  # merges all changes back into trunk
  
    Quit working with branch
  
    $ svnmerge.py uninit
    $ svn ci -F svnmerge-commit-message.txt
  
  
  
  More information at: http://www.orcaware.com/svn/wiki/Svnmerge.py
