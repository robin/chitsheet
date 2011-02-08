--- 
selenium_on_rails: "See: http://www.openqa.org/selenium-on-rails/\r\n\
  \r\n\
  $ rake test:acceptance\r\n\
  \r\n\
  Installation:\r\n   1. Install Selenium on Rails: script/plugin install http://svn.openqa.org/svn/selenium-on-rails/selenium-on-rails\r\n   2. If you\xE2\x80\x98re on Windows, gem install win32-open3\r\n   3. If the RedCloth gem is available the Selenese test cases can use it for better markup.\r\n   4. Run the Rakefile in the plugin\xE2\x80\x98s directory to run the tests in order to see that everything works. (If RedCloth isn\xE2\x80\x98t installed a few tests will fail since they assume RedCloth is installed.)\r\n   5. Create a test case: script/generate selenium login\r\n   6. Start the server: script/server -e test\r\n   7. Point your browser to localhost:3000/selenium\r\n   8. If everything works as expected you should see the Selenium test runner. The north east frame contains all your test cases (just one for now), and the north frame contains your test case.\r\n\
  \r\n\
  FORMATS\r\n\
  The test cases can be written in a number of formats. Which one you choose is a matter of taste. You can generate your test files by running script/generate selenium or by creating them manually in your /test/selenium directory.\r\n\
  \r\n\
  Selenese, .sel:\r\n\
  Wiki Table.  SeleniumIDE makes it super easy to record test and edit them.\r\n |open|/selenium/setup|\r\n |open|/|\r\n |goBack|\r\n\
  \r\n\
  RSelenese, .rsel:\r\n setup :fixtures => :all\r\n open '/'\r\n assert_title 'Home'\r\n ('a'..'z').each {|c| open :controller => 'user', :action => 'create', :name => c }\r\n\
  \r\n\
  See SeleniumOnRails::TestBuilder for available commands: http://svn.openqa.org/fisheye/browse/~raw,r=1000/selenium-on-rails/selenium-on-rails/doc/classes/SeleniumOnRails/TestBuilder.html\r\n\
  \r\n\
  HTML/RHTML:\r\n\
  Use Tables.\r\n\
  \r\n\
  PARTIAL test cases:\r\n  filename has to start with an underscore (#_login.rsel)\r\n\
  \r\n |includePartial|login|name=John Doe|password=eoD nhoJ|\r\n\
  \r\n include_partial 'login', :name => 'Jane Doe', :password => 'Jane Doe'.reverse\r\n\
  \r\n <%= render :partial => 'login', :locals => {:name = 'Joe Schmo', :password => 'Joe Schmo'.reverse} %>"
