--- 
belongs_to: "Options for belongs_to\r\n\
  \r\n\
  :class_name - specify the class name of the association. Use it only if that name can\xE2\x80\x99t be inferred from the association name. So has_one :author will by default be linked to the Author class, but if the real class name is Person, you\xE2\x80\x99ll have to specify it with this option.\r\n\
  \r\n\
  :conditions - specify the conditions that the associated object must meet in order to be included as a \"WHERE\" sql fragment, such as \"authorized = 1\".\r\n\
  \r\n\
  :order - specify the order from which the associated object will be picked at the top. Specified as an \"ORDER BY\" sql fragment, such as \"last_name, first_name DESC\"\r\n\
  \r\n\
  :foreign_key - specify the foreign key used for the association. By default this is guessed to be the name of the associated class in lower-case and \"_id\" suffixed. So a Person class that makes a belongs_to association to a Boss class will use \"boss_id\" as the default foreign_key.\r\n\
  \r\n\
  :counter_cache - caches the number of belonging objects on the associate class through use of increment_counter and decrement_counter. The counter cache is incremented when an object of this class is created and decremented when it\xE2\x80\x99s destroyed. This requires that a column named \"#{table_name}_count\" (such as comments_count for a belonging Comment class) is used on the associate class (such as a Post class). You can also specify a custom counter cache column by given that name instead of a true/false value to this option (e.g., :counter_cache => :my_custom_counter.)\r\n\
  \r\n\
  :include - specify second-order associations that should be eager loaded when this object is loaded.\r\n\
  \r\n\
  :polymorphic - specify this association is a polymorphic association by passing true."
