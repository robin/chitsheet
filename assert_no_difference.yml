--- 
assert_no_difference: |-
  assert_no_difference -- an assertion for your testing suite
  
  Usage:
    assert_no_difference 'Model.count' do
      puts "blah"
    end
  
  Synonym for:
    assert_difference 'Model.count', 0 do
      puts "blah" #or any action that will NOT change the argument.
    end
  
  This is useful for when you are testing benign actions or, even better, when you have fail-safes that allow an action to be executed but do not actually affect the database.
  For instance, you've got an action that is protected by authentication and you don't want to broadcast its existance to anyone with lesser permissions.  If an unauthenticated
  use navigates to the action, just let them see nothing (render :nothing => true or something to that effect) and chug along without caring.
