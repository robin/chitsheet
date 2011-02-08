--- 
git_collaboration: |-
  Restricted, shared git repo:
    $ mkdir repo.git
    $ cd repo.git
    $ git --bare init --shared
    $ touch git-daemon-export-ok
    $ git --bare fetch /git/git_repo_with_working master:master
  
  Now only developers with ssh access in the 'git' group (if you set it up that way) can pull / push / clone the repo.
