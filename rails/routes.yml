--- 
rails_routes: |-
  http://api.rubyonrails.com/classes/ActionController/Routing.html
  
  TEST/UNIT:
  
  assert_routing: lets you test whether or not the route properly resolves into options.
  
   def test_movie_route_properly_splits
    opts = {:controller => "plugin", :action => "checkout", :id => "2"}
    assert_routing "plugin/checkout/2", opts
   end
  
  
  assert_recognizes:  tests that an URL breaks into parameters properly.
  
   def test_route_has_options
    opts = {:controller => "plugin", :action => "show", :id => "12"}
    assert_recognizes opts, "/plugins/show/12"
   end
  
  
  In tests you can simply pass the URL or named route to get or post.
   def send_to_jail
     get '/jail'
     assert_response :success
     assert_template "jail/front"
   end
  
   def goes_to_login
     get login_url
     #...
   end
  
  ---- 
   RSPEC:
  
   it "index should be landing page for companies" do
      route_for(:controller => "companies", :action => "index").should == '/companies'
   end
  
   it "should be landing page for companies" do
      params_for('/companies').should == {:controller => "companies", :action => "index"}
   end
  
   specify "{:controller => 'sessions', :action => 'new'} from GET /login" do 
      params_from("/login", :method => :get).should == {:controller => "sessions", :action => "new"} 
   end
