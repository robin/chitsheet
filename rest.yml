--- 
rest: |-
  Resource Routes (in config/routes.rb)
    Simple
     map.resources :users, :sessions 
  
    Nested
      map.resources :teams do |teams| 
        teams.resources :players 
      end 
  
    Customized
      map.resources :articles, 
                    :collection  => {:sort => :put}, 
                    :member      => {:deactivate => :delete}, 
                    :new         => {:preview => :post}, 
                    :controller  => 'articles', 
                    :singular    => 'article', 
                    :path_prefix => '/book/:book_id', 
                    :name_prefix => 'book_' 
  
    Including the default route (/:controller/:action/:id) will allow any verb to
    access any action. This is usually not what you want, so you should probably 
    delete it from routes.rb 
  
  | Standard Methods       | Verb   | Path          | Action  |
  |------------------------|--------|---------------|---------|
  |       plural_path      | GET    | /teams        | index   |
  |     singular_path(id)  | GET    | /teams/1      | show    |
  | new_singular_path      | GET    | /teams/new    | new     |
  |       plural_path      | POST   | /teams        | create  |
  | edit_singular_path(id) | GET    | /teams/1;edit | edit    |
  |      singular_path(id) | PUT    | /teams/1      | update  |
  |      singular_path(id) | DELETE | /teams/1      | destroy |
  
    Each method also has a counterpart ending in _url that includes the protocol,
    domain, and port. There is also a hash_for_ version of each method that 
    returns a hash instead of a string.
  
  | Formats in the URL                         | Path                  |
  |--------------------------------------------|-----------------------|
  | formatted_plural_path(:xml)                | /teams.xml            |
  | formatted_singular_path(id, :rss)          | /teams.1.rss          |
  | formatted_players_path(@team, :atom)       | /teams/1/players.atom |
  | formatted_player_path(@team, @player, :js) | /teams/1/players/5.js |
  | formatted_player_path(:team_id => 1,       | /teams/1/players/5.js |
  |               id => 5, :format => :js)     |                       |
  
    Any URL-generating method can take a hash of options instead of bare 
    arguments. This is the only way to generate a URL with extra querystring 
    params.
  
  button_to "Destroy", 
            team_path(@team), 
            :confirm => "Are you sure?", 
            :method => :delete 
  
  link_to "Destroy", 
          team_path(@team), 
          :confirm => "Are you sure?", 
          :method => :delete
  
  link_to_remote "Destroy", 
                 :url => team_path(@team), 
                 :confirm => "Are you sure?", 
                 :method => :delete
  
  form_for :team, 
           @team, 
           :url => team_path(@team), 
           :html => { 
             :method => :put 
           } do |f| ... 
  
  | Nested Resources            | Path                        |
  |-----------------------------|-----------------------------|
  | players_path(@team)         | /teams/:team_id/players     |
  |                             | /teams/1/players            |
  | player_path(@team, @player) | /teams/:team_id/players/:id |
  |                             | /teams/1/players/5          |
  
    Nested resources must be defined in routes.rb. See above for an example.
  
  Useful Plugins
  * Beast Forum (an app built with RESTful design) 
      http://svn.techno-weenie.net/projects/beast/trunk/
  * RESTFUL Authentication Plugin 
      http://svn.techno-weenie.net/projects/plugins/restful_authentication/
  * Simply Helpful Plugin 
      http://dev.rubyonrails.org/svn/rails/plugins/simply_helpful/
  
  respond_to { |wants| 
    wants.all | .text | .html | .js | .ics | .xml | .rss | .atom | .yaml 
  }
  
  Add New MIME types (in config/initializers/mime.rb)
    Mime::Type.register "image/jpg", :jpg
    Mime::Type.register "application/vnd.visa+xml", :visa
  
    Types listed here can be used in a respond_to block and as a forced format 
    extension at the end of urls.
  
  Scaffold Resource Generator
    ./script/generate scaffold
                      Episode
                      title:string
                      description:text
                      program_id:integer
  
    Use a singular word for the model/resource name. The other arguments will be 
    used to pre-populate the database migration and fields in view templates.
  
  Mostly from http://peepcode.com/articles/2006/10/08/restful-rails
