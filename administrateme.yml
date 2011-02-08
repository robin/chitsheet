--- 
administrateme: |-
  administrate_me: A Rails plugin to provide support for common administration functions. http://github.com/insignia/administrate_me
  
  $   ruby script/plugin install git://github.com/insignia/administrate_me
  
  Copying asset files to the current project:
  $ rake admin:import_files
  
  Defining modules (tabs) for the app:
  
  class ApplicationController < ActionController::Base
    # Main definitions
    set_module :products
    set_module :categories
    # Setting modules by request
    def modules
      set_module :users if current_user.has_role?('admin')
    end
  end
  
  Making a controller work with administrate_me interfase:
  class Products < ApplicationController
    administrate_me do |a|
      a.search :name
    end
  end
  
  Generating view files for restful controller/model:
  $ ruby script/generate admin_view <controller-name>
  
  See README file for a step-by-step tutorial to the most basic app using this plugin.
