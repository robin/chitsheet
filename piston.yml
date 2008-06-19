--- 
piston: |-
  Piston (http://piston.rubyforge.org/usage.html) is a tool for keeping bits and pieces of your Subversion repository in sync with a remote repository. Like svn:externals, but better. How?
  
  With Piston, you import a remote repository and check it into your local repository. You can then go nuts modifying it or periodically sync it up with its remote origin using piston update.
  
  All of the examples use the vendor/rails directory. But piston works on any directory that you would use svn:externals with (IE Other plugin directories).
  
  Note that for some commands to work you must first commit the imported files into your repository.
  
  Install:
    gem install piston -y
  
  Import:
    piston import http://dev.rubyonrails.org/svn/rails/trunk vendor/rails
  
  Update:
    piston update vendor/rails
  
  Lock (doesn't allow updates):
    piston lock vendor/rails
  
  Unlock:
    piston unlock vendor/rails
  
  Status:
    piston status vendor/rails
