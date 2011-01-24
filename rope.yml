--- 
rope: |-
  # updated as of Ruby Reports 0.6.1
  
  rope is a simple tool that comes with Ruport that will drop a directory structure for you and generate some boilerplate code / config files. To try it out, just type rope myprojname on the command line.
  
  Once you do this, you should see something like this:
  
  bash-3.1$ ls my_proj_name/
  Rakefile  app  config  data  log  output  sql  templates  test  util
  
  This has given you a rake file, a simple config file(config/ruport_config.rb), hooks for Ruport's logging system, and a two simple applications.
  build.rb
  
  The first is util/build.rb . This will eventually enable generating all sorts of components for Ruport, but right now can be used to generate report files.
  
  Example:
  
  ruby util/build.rb report my_report
  
  Now when you run rake test, you'll see something like this:
  
  
    1) Failure:
  test_flunk(TestMyReport) [./test/test_my_report.rb:9]:
  Write your real tests here or in any test/test_* file.
  
  So you have a test already for your report, and your report file has been stowed in app/reports, waiting for you to begin working on it. This has put in the necessary boilerplate to set up a Ruport Report, hooked into the default configuration file, and enabled logging to work out of the box.
  
  sql_exec.rb
  
  you can point this script at an SQL file and run it. This will respond by printing the results as text to STDOUT. This is a good way to check that your configuration file is hooked up properly and also a way to check if any query files you have are working. You can also provide SQL on STDIN, if that is helpful to you.
