--- 
cap_bare: |-
  Please keep this sheet clean and simple.   Long winded discussions should be in cheat capistrano.
  
  * multi-stage   (http://weblog.jamisbuck.org/2007/7/23/capistrano-multistage)
  set :stages, %w(staging production testing) # [optional] defaults to [development, test, staging?, production].
  set :default_stage, "testing" # [optional] if omitted, cap aborts if you don't specify in args
  require 'capistrano/ext/multistage'
  
  Stage-specific code: config/deploy/staging.rb, etc.
