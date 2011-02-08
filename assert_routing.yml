--- 
assert_routing: |-
  # 'cheat assertions' for the rest
  
  assert_routing(path, options, defaults={}, extras={}, message=nil)
  
  Asserts that path and options match both ways; in other words, it verifies that path generates options and then that options generates path. This essentially combines assert_recognizes and assert_generates into one step.
  
  The extras hash allows you to specify options that would normally be provided as a query string to the action. The message parameter allows you to specify a custom error message to display upon failure.
  
  Examples
  
   # Assert a basic route: a controller with the default action (index)
   assert_routing('/home', :controller => 'home', :action => 'index')
  
   # Test a route generated with a specific controller, action, and parameter (id)
   assert_routing('/entries/show/23', :controller => 'entries', :action => 'show', id => 23)
  
   # Assert a basic route (controller + default action), with an error message if it fails
   assert_routing('/store', { :controller => 'store', :action => 'index' }, {}, {}, 'Route for store index not generated properly')
  
   # Tests a route, providing a defaults hash
   assert_routing 'controller/action/9', {:id => "9", :item => "square"}, {:controller => "controller", :action => "action"}, {}, {:item => "square"}
