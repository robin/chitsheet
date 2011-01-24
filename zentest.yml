--- 
zentest: |-
  gem install ZenTest
  
  # autotest
  
  $ autotest [options]
  
  options:
          -h
          -help           You're looking at it.
  
          -v              Be verbose. Prints files that autotest doesn't know how to map to tests.
  
          -q              Be more quiet.
  
          -f              Fast start. Doesn't initially run tests at start.
  
  # Rails testing
  
  require 'test/rails'
  
  ## assertions
  
  assert_empty []
  assert_in_epsilon a, b, 0.5
  assert_include [a, b, c], a
  assert_includes [a, b, c], a  # just syntactical sugar
  deny false
  deny_empty [1, 2, 3]
  deny_equal 1, 2               # alias for assert_not_equal
  deny_include [a, b, c], d
  deny_includes [a, b, c], d    # just syntactical sugar
  deny_nil []                   # alias for assert_not_nil
