--- 
association_methods: |-
  Singular associations (one-to-one)
  
                                    |            |  belongs_to  |
  generated methods                 | belongs_to | :polymorphic | has_one
  ----------------------------------+------------+--------------+---------
  #other                            |     X      |      X       |    X
  #other=(other)                    |     X      |      X       |    X
  #build_other(attributes={})       |     X      |              |    X
  #create_other(attributes={})      |     X      |              |    X
  #other.create!(attributes={})     |            |              |    X
  #other.nil?                       |     X      |      X       |    
  
  Collection associations (one-to-many / many-to-many)
  
                                    |       |          | has_many
  generated methods                 | habtm | has_many | :through  
  ----------------------------------+-------+----------+----------
  #others                           |   X   |    X     |    X
  #others=(other,other,...)         |   X   |    X     |    
  #other_ids                        |   X   |    X     |    
  #other_ids=(id,id,...)            |   X   |    X     |    
  #others<<                         |   X   |    X     |    X
  #others.push                      |   X   |    X     |    X
  #others.concat                    |   X   |    X     |    X
  #others.build(attributes={})      |   X   |    X     |    X
  #others.create(attributes={})     |   X   |    X     |    
  #others.create!(attributes={})    |   X   |    X     |    X
  #others.size                      |   X   |    X     |    
  #others.length                    |   X   |    X     |    
  #others.count                     |       |    X     |    
  #others.sum(args*,&block)         |   X   |    X     |    X
  #others.empty?                    |   X   |    X     |    
  #others.clear                     |   X   |    X     |    
  #others.delete(other,other,...)   |   X   |    X     |    X
  #others.delete_all                |   X   |    X     |    
  #others.destroy_all               |   X   |    X     |    
  #others.find(*args)               |   X   |    X     |    X
  #others.find_first                |   X   |          |    
  #others.uniq                      |   X   |    X     |    
  #others.reset                     |   X   |    X     |    X
