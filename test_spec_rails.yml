--- 
test_spec_rails: |-
  test/spec/rails by Per "Tuxie" Wigren <per.wigren@gmail.com>
  
  http://svn.techno-weenie.net/projects/plugins/test_spec_on_rails/
  
  This plugin contain some helpers to test your Rails app using test/spec.
  
  There's also a rake treat at: http://require.errtheblog.com/plugins/wiki/TestSpecRails
  
  Installation
  ------------
   * Install test/spec: gem install test-spec
   * Install test/spec/rails
   * require 'test/spec/rails' in your test_helper.rb
  
  
  Model validation
  ----------------
    @user.should.validate
    @user.should.not.validate
    or:
    @user.should.be.validated
    @user.should.not.be.validated
  
  
  Redirection
  -----------
    response.should.be.redirected           # assert_response :redirect
    response.should.redirect foo_url(@foo)  # assert_redirected_to foo_url(@foo)
    should.redirect_to :action => 'show'    # because "response" is optional
  
    It's aliased as redirect, redirect_to, redirected and redirected_to
  
  
  Output verification
  -------------------
    Wrapper for assert_select:
  
    get :show
    page.should.select "form#user_form"             # require the output to have a <form id="user_form">
  
    page.should.select "form#user_form" do |form|
      form.should.select "input[type=submit]"       # the user_form must include a <input type="submit">
    end
  
  
  HTTP Status
  -----------
    Wrapper for assert_response:
  
    status.should.be :success
    status.should.be 200
  
  
  Which template was rendered?
  ----------------------------
    Wrapper for assert_template:
  
    template.should.be "foo/show.rhtml"
  
  
  URL testing
  -----------
    get :show, :user_id => 1
    url.should.be "/users/1"
    url.should.be :controller => "users", :action => "show", :user_id => 1
  
  
  Setup controller for testing + example usage
  --------------------------------------------
    context "A guest" do
      use_controller FooController
  
      specify "isn't allowed to foo" do
        post :create, :foo => 'bar'
        flash[:error].should.not.be.blank
        response.should.redirect :controller => 'front', :action => 'show'
        assigns(:foo).errors.on(:bar).should.not.be.blank
        assigns(:foo).should.not.validate
        follow_redirect
        page.should.select "#errors", :text => /#{flash[:error]}/
      end
    end
  
    context "Tuxie" do
      setup do
        use_controller FooController
        login_as :tuxie
      end
  
      specify "may foo" do
        post :create, :foo => 'bar'
        flash[:notice].should.not.be.blank
        assigns(:foo).errors.should.be.empty
        assigns(:foo).should.validate
        should.redirect_to :action => 'show'
        follow_redirect
        page.should.select "#notice", :text => /#{flash[:notice]}/
      end
    end
  
  
  Misc
  ----
  
    page, response and request are just aliases for self (the TestCase) so the 
    following are functionally identical:
  
    page.should.redirect
    response.should.redirect
    request.should.redirect
  
    output, body, html and xhtml return @response.body so the following lines 
    are identical:
  
    output.should.match /foo/
    html.should.match /foo/
    xhtml.should.match /foo/
    body.should.match /foo/
  
    If an object respond to #should_equal, that method will be used instead 
    of assert_equal when using foo.should.equal(bar) or foo.should.be(bar)
    foo.should.not.equal and foo.should.not.be look for #should_not_equal
