--- 
assert_redirected_to: |-
  # 'cheat assertions' for the rest
  
  assert_redirected_to(options = {}, message=nil)
  
  Assert that the redirection options passed in match those of the redirect called in the latest action. This match can be partial, such that assert_redirected_to(:controller => "weblog") will also match the redirection of redirect_to(:controller => "weblog", :action => "show") and so on.
  
  Examples
  
    # assert that the redirection was to the "index" action on the WeblogController
    assert_redirected_to :controller => "weblog", :action => "index"
  
    # assert that the redirection was to the named route login_url
    assert_redirected_to login_url
