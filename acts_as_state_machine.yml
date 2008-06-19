--- 
acts_as_state_machine: |-
  == Example
  
  class Order < ActiveRecord::Base
    acts_as_state_machine :initial => :opened
  
    state :opened
    state :closed, :enter => Proc.new {|o| Mailer.send_notice(o)}
    state :returned
  
    event :close do
      transitions :to => :closed, :from => :opened
    end
  
    event :return do
      transitions :to => :returned, :from => :closed
    end
  end
  
  o = Order.create
  o.close! # notice is sent by mailer
  o.return!
