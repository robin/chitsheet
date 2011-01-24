--- 
assert_no_tag: |
  # 'cheat assertions' for the rest
  
  assert_no_tag(*opts)
  
  Identical to assert_tag, but asserts that a matching tag does not exist. (See assert_tag for a full discussion of the syntax.)
  
  Examples
  
    # Assert that there is not a "div" containing a "p"
    assert_no_tag :tag => "div", :descendant => { :tag => "p" }
  
    # Assert that an unordered list is empty
    assert_no_tag :tag => "ul", :descendant => { :tag => "li" }
  
    # Assert that there is not a "p" tag with between 1 to 3 "img" tags
    # as immediate children
    assert_no_tag :tag => "p",
               :children => { :count => 1..3, :only => { :tag => "img" } }

