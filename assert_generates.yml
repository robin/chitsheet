--- 
assert_generates: |
  # 'cheat assertions' for the rest
  
  assert_generates(expected_path, options, defaults={}, extras = {}, message=nil)
  
  Asserts that the provided options can be used to generate the provided path. This is the inverse of assert_recognizes. The extras parameter is used to tell the request the names and values of additional request parameters that would be in a query string. The message parameter allows you to specify a custom error message for assertion failures.
  
  The defaults parameter is unused.
  
  Examples
  
    # Asserts that the default action is generated for a route with no action
    assert_generates("/items", :controller => "items", :action => "index")
  
    # Tests that the list action is properly routed
    assert_generates("/items/list", :controller => "items", :action => "list")
  
    # Tests the generation of a route with a parameter
    assert_generates("/items/list/1", { :controller => "items", :action => "list", :id => "1" })
  
    # Asserts that the generated route gives us our custom route
    assert_generates "changesets/12", { :controller => 'scm', :action => 'show_diff', :revision => "12" }

