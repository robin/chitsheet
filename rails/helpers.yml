--- 
rails_helpers: |-
  ApplicationController helpers in views 
  (putting the methods in ApplicationHelper only makes them available to views,
  if you need them in controllers AND views, define them in ApplicationController
  and use the helper_method method)
  in ApplicationController: 
    helper_method :method_name1, :method_name2, :so_on_and_so_forth
  
  View Helpers in Controllers or Models
  (might make you feel dirty, but if you need to you'll get over it)
  1. make a module in /lib:
    "shared.rb"
    --
    module Shared
      def shared_help
        SharedHelper.instance
      end
  	  
      class SharedHelper
        include Singleton
        include ActionView::Helpers::TextHelper
        include ActionView::Helpers::UrlHelper
        include ActionView::Helpers::DateHelper
        include ActionView::Helpers::TagHelper
        include ActionView::Helpers::NumberHelper
        # and whatever else you need ...
      end
    end
  	
  2. include the module in a Controller or Model:
  include Shared
  
  3. call your view helpers like 'shared_help.method', i.e.:
  shared_help.mail_to(email_addr)
  
  Another way to do it, using a class instead of a module:
     1. # create a new file inside lib/ and call it helpers.rb
     2. # paste the following:
     3.  
     4. def help
     5.  Helper.instance
     6. end
     7.  
     8. class Helper
     9.  include Singleton
    11.  include ActionView::Helpers::DateHelper
    12.  include ActionView::Helpers::TextHelper
    13. end
    14.  
    15. # then in any model or controller:
    16. require 'lib/helpers'
    17.  
    18. # to use:
    19. # help.name_of_helper
    20. # EX: help.pluralize 10, "person"
  
  View helpers in email templates
  use the helper method in your mailer class, like:
  class Notifier < ActionMailer::Base
    helper :application
    # ... your mailer methods
  end
