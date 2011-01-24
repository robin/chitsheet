--- 
assert_recognizes: |-
  # 'cheat assertions' for the rest
  
  assert_recognizes(expected_options, path, extras={}, message=nil)
  
  Asserts that the routing of the given path was handled correctly and that the parsed options (given in the expected_options hash) match path. Basically, it asserts that Rails recognizes the route given by expected_options.
  
  Pass a hash in the second argument (path) to specify the request method. This is useful for routes requiring a specific HTTP method. The hash should contain a :path with the incoming request path and a :method containing the required HTTP verb.
  
    # assert that POSTing to /items will call the create action on ItemsController
    assert_recognizes({:controller => 'items', :action => 'create'}, {:path => 'items', :method => :post})
  
  You can also pass in extras with a hash containing URL parameters that would normally be in the query string. This can be used to assert that values in the query string string will end up in the params hash correctly. To test query strings you must use the extras argument, appending the query string on the path directly will not work. For example:
  
    # assert that a path of '/items/list/1?view=print' returns the correct options
    assert_recognizes({:controller => 'items', :action => 'list', :id => '1', :view => 'print'}, 'items/list/1', { :view => "print" })
  
  The message parameter allows you to pass in an error message that is displayed upon failure.
  Examples
  
    # Check the default route (i.e., the index action)
    assert_recognizes({:controller => 'items', :action => 'index'}, 'items')
  
    # Test a specific action
    assert_recognizes({:controller => 'items', :action => 'list'}, 'items/list')
  
    # Test an action with a parameter
    assert_recognizes({:controller => 'items', :action => 'destroy', :id => '1'}, 'items/destroy/1')
  
    # Test a custom route
    assert_recognizes({:controller => 'items', :action => 'show', :id => '1'}, 'view/item1')
  
    # Check a Simply RESTful generated route
    assert_recognizes(list_items_url, 'items/list')
