--- 
permalink_fu: |-
  Install:
  >> ./script/plugin install http://svn.techno-weenie.net/projects/plugins/permalink_fu/
  >> piston import http://svn.techno-weenie.net/projects/plugins/permalink_fu/
  
  Modify table:
  >> ./script/generate migration add_permalink_to_article
  >> add_column :designers, :permalink, :string
  
  Model:
  
  class Article < ActiveRecord::Base
          # title is the field name you want to convert to a permalink
          has_permalink :title 
          # you can also specifiy a different permalink field in your database by giving a second paramater
          # has_permalink :title, :my_permalink_field
  
          # we now add the to_param method which Rails's routing uses
          def to_param
                permalink
          end         
  end
  
  Convert old titles to permalinks:
  >> Article.find(:all).each(&:save)
  
  Hackish find(id):
  >> @article = Article.find_by_permalink(params[:id])
  
  # in your route file
  map.connect 'article/:permalink', :controller => 'article', :action => 'view'
  # in your views when linking
  link_to "View #{article.title}", {:controller => 'designer', :action => 'view', :permalink => article.permalink}
  # then in your controller you can use
  @article = Article.find_by_permalink(params[:permalink])
  
  Reference: http://www.seoonrails.com/even-better-looking-urls-with-permalink_fu
