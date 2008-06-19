--- 
sake: |-
  ***************************************************************************
  Sake - system-wide Rake.
  For more information: http://errtheblog.com/posts/60-sake-bomb
  
  $ sudo gem install sake
  
  ***************************************************************************
  ** Auto Completion Of Sake Tasks
  ***************************************************************************
  bash: complete -W "$(sake -T | awk {'print $2'})" sake
  z: function sake_task_list { reply=(`sake -T | awk '{ print $2 }'); } 
     compctl -K sake_task_list sake
  
  ***************************************************************************
  ** Pastie (http://drnicwilliams.com/2007/06/28/pastie-paradise/)
  ***************************************************************************
  $ sake -i http://pastie.caboo.se/73801.txt
  $ sake -T
  $ sake pastie:send
    # Sends STDIN or FILE=file to Pastie;
    # USAGE: cat some_code.rb | sake pastie:send
    # OR:    sake pastie:send FILE=some_code.rb
  
  On OSX, you can get the url for your new pastie in the clipboard using pbcopy:
  $ cat some_code.rb | sake pastie:send | pbcopy
  
  Want to send a patch to someone via pastie?
  $ svn diff | sake pastie:send | pbcopy
  
  ***************************************************************************
  ** Load up any RubyGem into an editor from cache.
  ***************************************************************************
  To Install:
  $ sake -i http://pastie.org/76167.txt
  
  Example:
  $ sake gems:find activerecord | xargs mate
  ***************************************************************************
