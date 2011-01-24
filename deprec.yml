--- 
deprec: |-
  Deprec is a collection of automated deployment,recipes written in ruby, for setting up production ready rails servers.
  
  Known to support: Ubuntu 7,10, 8,04
  
  ALL commands are performed on the CLIENT.
  
  ##To Install (performed once):
  sudo gem install deprec                     # installs what you need
  cap show_tasks                              # should now include deprec tasks
  
  ##To deploy your app to a fresh slice:
  
  cd your_rails_app
  depify .
  # Edit config/deploy.rb
  cap deprec:rails:install_stack
  
  # WARNING! Don't run the following command if you are using
  # a shared database server that has already been installed.
  cap deprec:db:install 
  
  cap deploy:setup
  cap deploy
  cap deploy:migrate
  
  Derived from: http://www.deprec.org/
  More help: http://topfunky.com/clients/peepcode/free-episodes
