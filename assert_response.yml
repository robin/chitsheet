--- 
assert_response: |-
  # 'cheat assertions' for the rest
  
  assert_response(type, message = nil)
  
  Asserts that the response is one of the following types:
  
      * :success - Status code was 200
      * :redirect - Status code was in the 300-399 range
      * :missing - Status code was 404
      * :error - Status code was in the 500-599 range
  
  You can also pass an explicit status number like assert_response(501) or its symbolic equivalent assert_response(:not_implemented). See ActionController::StatusCodes for a full list.
  
  Examples
  
    # assert that the response was a redirection
    assert_response :redirect
  
    # assert that the response code was status code 401 (unauthorized)
    assert_response 401
