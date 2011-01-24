--- 
git_usage: |-
  Some common git usage
  ---------------------
  
  To ignore certain files:
  $ echo "log/*.log" >> .gitignore
  $ echo "tmp/**/*" >> .gitignore
  $ git add .
  $ git commit -m "Add files"
  
  To add .gitignore files to all empty directories recursively from your current directory:
  $find . \( -type d -empty \) -and \( -not -regex ./\.git.* \) -exec touch {}/.gitignore \;
  
  
  To create a public repository:
  $ mkdir someapp.git
  $ cd someapp.git
  $ git --bare init
  $ git-update-server-info
  
  Add public repository as a remote:
  $ git remote add origin ssh://myserver.com/var/git/myapp.git
  $ git push
  
  Track the Remote Branch
  [branch "master"]
  	remote = origin
  	merge = refs/heads/master
  
  To pull from someone else's repository:
  # # Create a local branch
  $ git checkout some_working_branch
  # # Add the person's repository as a remote
  $ git remote add foos_remote git://someurl/
  # # Fetch her branch into yours
  $ git checkout -b foos_remote/her_branch
  # # Pull the changes into your local branch
  $ git pull foos_remote her_branch
  
  Submodule support:
  $ git submodule add [git-url] [path to local project dir]
  $ git submodule init
  # thereafter
  $ git submodule update
