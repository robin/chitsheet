--- 
rails_plugin_creation: |-
  require 'active_record'
  
  module Foo
    module Acts #:nodoc:
      module Fox #:nodoc:
  
        def self.included(mod)
          mod.extend(ClassMethods)
        end
  
        # declare the class level helper methods which
        # will load the relevant instance methods
        # defined below when invoked
        module ClassMethods
          def acts_as_fox
            class_eval do
              extend Foo::Acts::Fox::SingletonMethods
            end
            include Foo::Acts::Fox::InstanceMethods
          end
        end
  
        # Adds a catch_chickens class method which finds
        # all records which have a 'chickens' field set
        # to true.
        module SingletonMethods
          def catch_chickens
            find(:all, :conditions => ['chickens = ?', true])
          end
          # etc...
        end
  
        # Adds instance methods.
        module InstanceMethods
          def eat_chicken
            puts "Fox with ID #{self.id} just ate a chicken" 
          end
        end
  
      end
    end
  end
  
  # reopen ActiveRecord and include all the above to make
  # them available to all our models if they want it
  
  ActiveRecord::Base.class_eval do
    include Foo::Acts::Fox
  end
