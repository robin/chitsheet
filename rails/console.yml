--- 
rails_console: |-
  Reloading the Console Environment:
  >> reload!
  >> Dispatcher.reset_application!   # (outdated)
  
  Load and execute a Ruby script:
  >> load "the_file_name.rb"
  
  Using app object:
  >> app.get '/stories/10002'
  => 200
  >> app.assigns(:story)
  => #<Story:0x24aad0c ... >
  >> app.path
  => "/stories/10002" 
  >> app.reset!
  => nil
  
  Using helpers methods:
  >> helper.pluralize 2, "story" 
  => "2 stories"
  
  Clear the console:
  ctrl + l or Command + k (Mac)
  
  How-to Examine Routes:
  rs = ActionController::Routing::Routes
  puts rs.routes
  rs.recognize_path "/session"
  rs.generate :controller => "users", :action => "edit", :id => "4"
  
  Print as YAML
  >> y @something
  
  Grep available methods between model objects:
  >> p = Post.new # in this case there's a corresponding Comments model too
  >> y p.methods.grep(/commen/).sort
  --- 
  - autosave_associated_records_for_comments
  - comment_ids
  - comment_ids=
  - comments
  - comments=
  ...
  ...
  etc.
  
  Start in a sandbox (any modifications you make to the database will be rolled back on exit)
  $ ./script/console -s
  
  See also:
  
  $ cheat console
