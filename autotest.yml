--- 
autotest: |-
  Autotest continuously scans the files in your project for changes and runs the appropriate tests. Test failures are run until they have all passed. Then the full test suite is run to ensure that nothing else was inadvertantly broken.
  
  If you want Autotest to start over from the top, hit ^C once. If you want Autotest to quit, hit ^C twice.
  
  To use Autotest with Rails:
  
  $ sudo gem install ZenTest
  $ cd /path/to/railsapp/
  $ autotest
  
  Plugins:
  
  Plugins are available by creating a .autotest file either in your project root or in your home directory. You can then write event handlers in the form of:
  
    Autotest.add_hook hook_name { |autotest| ... }
  
  The available hooks are: initialize, run, run_command, ran_command,
  
    red, green, all_good, reset, interrupt, and quit.
  
  See example_dot_autotest.rb for more details.
  
  Naming:
  
  Autotest uses a simple naming scheme to figure out how to map implementation files to test files following the Test::Unit naming scheme.
  
      * Test files must be stored in test/
      * Test files names must start with test_
      * Test class names must start with Test
      * Implementation files must be stored in lib/
      * Implementation files must match up with a test file named test_.*implementation.rb
  
  Strategy:
  
     1. Find all files and associate them from impl <-> test.
     2. Run all tests.
     3. Scan for failures.
     4. Detect changes in ANY (ruby?. file, rerun all failures + changed files.
     5. Until 0 defects, goto 3.
     6. When 0 defects, goto 2.
  
  Exclusions:
  
    Autotest.add_hook :initialize do |at|
      at.add_exception(coverage)
      at.add_exception(vendor)
    end
