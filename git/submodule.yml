--- 
git_submodule: "** Adding a submodule to a superproject.\r\n\
  \r\n\
  git submodule add <repository>\r\n  Add the given repository as a submodule to the current git project.\r\n\
  \r\n\
  ** After cloning the superproject, the submodule directories will exist, but they will be empty.\r\n\
  \r\n\
  git submodule status\r\n  Show the status of the submodules.\r\n\
  \r\n\
  ** Actually pulling down the submodules is a two-step process.\r\n\
  \r\n\
  git submodule init\r\n\
  \r\n\
  git submodule update\r\n\
  \r\n\
  ** Gotcha: submodules do not checkout master by default, it checks out a specific commit relative to the superproject (somewhat like a tag).  To do any work, make sure you checkout master or another branch.\r\n\
  \r\n\
  $ cd my_submodule\r\n\
  $ git branch\r\n\
  * (no branch)\r\n  master\r\n\
  $ git checkout master\r\n\
  \r\n\
  ** Gotcha: when publishing (pushing) make sure you publish the submodule changes first, followed by the superproject.  Otherwise others will have problems cloning the repository.\r\n\
  \r\n\
  $ git commit -m \"Updated the my_submodule from within the superproject.\"\r\n\
  $ git push\r\n\
  $ cd ..\r\n\
  $ git add my_submodule\r\n\
  $ git commit -m \"Updated my_submodule.\"\r\n\
  $ git push\r\n\
  \r\n\
  ** Changing submodules URL\r\n\
  \r\n    * Fork/create your own version of the submodule in question\r\n    * Remove references to the existing submodule in .git/config, .gitmodules and nuke the submodule directory\r\n    * Commit\r\n    * Add the new submodule URL\r\n    * Commit\r\n    * Make changes in your submodule\r\n    * Commit changes in the submodule (not the parent project)\r\n    * Commit the changes in the parent project (otherwise you\xE2\x80\x99ll only get the old version of the submodule in future pulls)\r\n    * Enjoy the hair you didn\xE2\x80\x99t have to rip from your scalp\r\n"
