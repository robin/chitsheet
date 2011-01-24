--- 
lucene_query_syntax: |-
  == Basics  
  
    term   - a single bare word
    phrase - "group of words surrounded by double quotes"
  
  == Operators
  
    All operators are in UPPERCASE. 
  
    AND - matches docs where both operands match
        * cheat AND sheet
        * cheat AND sheet AND "ruby gem"
  
    OR  - matches docs where either operands match
        * cheat OR sheet
        * cheat OR sheet OR "ruby gem"
  
    NOT - removes docs from result set that match the operand
        - the NOT operator MUST be used in conjuction with another
          operation
        * "cheat sheet" NOT lucene
  
  == Grouping
  
    Grouping is done with left and right parentheses ( ).
  
    - look for documents that have the words 'cheat' AND 'sheet'
      but not 'ruby' or 'rails'
  
    ( cheat AND sheet ) NOT ( ruby OR rails )
  
  
  == Proximity Search
  
    Apply a tilde '~N' to a phrase.  This finds documents where all
    the words in the phrase are within N words of each other.
  
    - find all documents where the words 'cheat' and 'sheet' are
      within 10 words of each other.
  
    "cheat sheet"~10
