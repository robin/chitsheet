--- 
sti: |-
  Single Table Inheritance
  
  class CreateSTI < ActiveRecord::Migration
    def self.up
      create_table "statuses" do |t|
        t.column :type, :string # You need this!
        t.column :invoice_id, :integer
        t.column :employee_id, :integer
        t.column :created_at, :datetime
      end
    end
  
    def self.down
      drop_table "statuses"
    end
  end
  
  class Status < ActiveRecord::Base
    #superclass
  end
  
  class Invoiced < Status
    #subclass
    belongs_to :invoice
  end
  
  class Employeed < Status
    #subclass
    belongs_to :employee, :class_name => "Person", :foreign_key => 'employee_id'
  end
  
  Fixtures for a STI model must go in the fixture file for the
  superclass.
  
  To find out what class an instance of the superclass use
  @instance.class or you can use the value of the type column
  from other systems that do not go through AR.
  
  If you cannot use type (radio button helper has problems
  with it) define the new column in your superclass model
  like this:
  def self.inheritance_column
   'role' 
  end
