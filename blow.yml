--- 
blow: |-
  #!/usr/bin/env ruby
  require 'open-uri'
  unless $*.empty?
  eval(open("http://balloon.hobix.com/#{$*.shift}").read) rescue puts "** balloon not found"
  else
  puts "Usage: blow <script-name>"
  end
