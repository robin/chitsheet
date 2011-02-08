--- 
git_buildpackage: |-
  Importing
  ---------
  
  git import-dsc <package>.dsc
  
  Updating
  --------
  
  git import-orig -u <version> <source>.tar.gz
  
  Releasing
  ---------
  
  git dch --release
  git dch --snapshot
  git dch --snapshot --auto
  
  Building
  --------
  
  git buildpackage --git-ignore-new
  git buildpackage --git-tag
  
  Creating
  --------
  
  $ mkdir package-0.1
  $ cd package-0.1
  $ git init
  
  $ git import-orig -u 0.1 ../package-0.1.tar.gz
  $ dh_make
