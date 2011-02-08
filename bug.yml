--- 
bug: |-
  validate - define it with a custom validation to run on all saves 
  
  validate_on_create - define it with a custom validation to run on all creates
  
  validate_on_update - define it with a custom validation to run on all updates
  
  All validation helpers can take :if, :on, and :message unless otherwise stated.
  
  validates_acceptance_of(:attribute, :value) - validates that the gived attribute is set to "1" or the passed value.  Does not have to be a database attribute.
  
  validates_associated(*attributes) - validates whether the associated object or objects are all valid themselves. works with any kind of association.  does not take message
  
  validates_confirmation_of(:attribute) - validates that attributename_confirmation is equal to the attribute.  The confirmation variable does not need to be in the database
  
  validates_exclusion_of(:attribute, :if) - validates that the value of the specified attribute is not in a particular enumerable object specified by the :if argument
  
  validates_format_of(:attribute, :with) - validates whether the value of the specified attribute is of the correct form by matching it against the regular expression provided in the :with argument
  
  validates_inclusion_of(:attribute, :if) - validates that the value of the specified attribute is in a particular enumerable object specified by the :if argument
  
  validates_length_of(:attribute, *options) - validates that the specified attribute matches the length restrictions supplied. only one option can be used at a time.  options: maximum, minimum, is, within, in, allow_nil. message options: too_long, too_short, wrong_length
  
  validates_numericality_of(:attribute) - validates whether the value of the specified attribute is numeric by trying to convert it to a float with Kernel.Float (if integer is false) or applying it to the regular expression /^[+\-]?\d+$/ (if integer is set to true). options: allow_nil, only_integer
  
  validates_presence_of(:atrribute) - validates that the specified attributes are not blank (as defined by Object#blank?)
  
  validates_uniqueness_of(:attribute) = calidates whether the value of the specified attributes are unique across the system. options: scope (one or more columns by which to limit the scope of the uniquness constraint_
