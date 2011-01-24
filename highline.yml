--- 
highline: "##############################################################################\r\n\
  agree( yes_or_no_question, character = nil )           # return boolean \r\n\
  ask( question, answer_type = String ) {|question| ...} # string by default\r\n\
  choose( *items, &details )                             # string\r\n\
  list( items, mode = :rows, option = nil )              # string\r\n   # Other modes available :columns_across , :columns_down and :inline\r\n\
  ##############################################################################\r\n                     ##  FROM THE HIGHLINE RDOC  ##\r\n\
  Basic usage:\r\n\
  \r\n  ask(\"Company?  \") { |q| q.default = \"none\" }\r\n\
  \r\n\
  Validation:\r\n\
  \r\n  ask(\"Age?  \", Integer) { |q| q.in = 0..105 }\r\n  ask(\"Name?  (last, first)  \") { |q| q.validate = /\\A\\w+, ?\\w+\\Z/ }\r\n\
  \r\n\
  Type conversion for answers:\r\n\
  \r\n  ask(\"Birthday?  \", Date)\r\n  ask(\"Interests?  (comma sep list)  \", lambda { |str| str.split(/,\\s*/) })\r\n\
  \r\n\
  Reading passwords:\r\n\
  \r\n  ask(\"Enter your password:  \") { |q| q.echo = false }\r\n  ask(\"Enter your password:  \") { |q| q.echo = \"x\" }\r\n\
  \r\n\
  ERb based output (with HighLine\xE2\x80\x99s ANSI color tools):\r\n\
  \r\n  say(\"This should be <%= color('bold', BOLD) %>!\")\r\n\
  \r\n\
  Menus:\r\n\
  \r\n  choose do |menu|\r\n    menu.prompt = \"Please choose your favorite programming language?  \"\r\n\
  \r\n    menu.choice(:ruby) { say(\"Good choice!\") }\r\n    menu.choices(:python, :perl) { say(\"Not from around here, are you?\") }\r\n  end"
