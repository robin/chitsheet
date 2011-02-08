--- 
callbacks: |-
  Regular callbacks in ActiveRecord::Base:
  
    1. before_validation
    2. before_validation_on_create
    3. after_validation
    4. after_validation_on_create
    5. before_save
    6. before_create
    7. after_create
    8. after_save
    9. before_destroy
    10. after_destroy
  
  Usage:
  
    Define a method:
  
      class Foo < ActiveRecord::Base
        def before_create
          # your code here
        end
      end
  
   Invoke callback with a name of a method:
  
      class Foo < ActiveRecord::Base
        before_create :do_stuff
      protected
        def do_stuff
          # your code here
        end
      end
  
    Invoke callback with a block:
  
      class Foo < ActiveRecord::Base
        before_create do
          def do_stuff
            # your code here
          end
        end
      end
  
  Exceptions:
  
    1. after_find
    2. after_initialize 
  
  Usage:
  
    Define a method:
  
      class Foo < ActiveRecord::Base
        def after_find
          do_stuff
        end
      end
