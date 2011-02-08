--- 
string: |-
  Ruby 1.8 String Literal
  
  Delimiters:
    'singlequote'    "doublequote" 
    %q/single/       %Q!double!    
    %q<single>       %Q(double)    
                     %{double}     
  
  Heredoc:
  
  Following a << you can specify a string or an identifier to terminate the string literal, and all lines following the current line up to the terminator are the value of the string. If the terminator is quoted, the type of quotes determines the type of the line-oriented string literal. Notice there must be no space between << and the terminator.
  
  If the - placed before the delimiter, then all leading whitespcae characters (tabs or spaces) are stripped from input lines and the line containing delimiter. This allows here-documents within scripts to be indented in a natural fashion.
  
  print <<EOF
  The price is #{$Price}.
  EOF
  
  print <<"EOF";			# same as above
  The price is #{$Price}.
  EOF
  
  print <<`EOC`			# execute commands
  echo hi there
  echo lo there
  EOC
  
  print <<"foo", <<"bar"	# you can stack them
  I said foo.
  foo
  I said bar.
  bar
  
  myfunc(<<"THIS", 23, <<'THAT')
  Here's a line
  or two.
  THIS
  and here's another.
  THAT
  
  Escapes (double-quote):
  
  |----+-----+---------------------+------+-----|
  | E  | ASC | Name(s)             |  Hex | Dec |
  |----+-----+---------------------+------+-----|
  | \a | BEL | bell, alert         | 0x07 |   7 |
  | \b | BS  | backspace           | 0x08 |   8 |
  | \e | ESC | escape              | 0x1b |  27 |
  | \f | NP  | formfeed, newpage   | 0x0c |  12 |
  | \n | NL  | linefeed, newline   | 0x0a |  10 |
  | \r | CR  | carriage return     | 0x0d |  13 |
  | \s | SP  | space               | 0x20 |  32 |
  | \t | HT  | tab, horizontal tab | 0x09 |   9 |
  | \v | VT  | vertical tab        | 0x0b |  11 |
  |----+-----+---------------------+------+-----|
  
  |---------+------------------|
  | Format  | Translation      |
  |---------+------------------|
  | \nnn    | Octal nnn        |
  | \xnn    | Hexadecimal 0xnn |
  | \cx     | Control-x        |   Control-x == (?x & 0b10011111)
  | \C-x    | Control-x        |
  | \M-x    | Meta-x           |   Meta-x == (?x | 0b10000000)
  | \M-\C-x | Meta-control-x   | 
  | \x      | x                |
  | #{expr} | Value of expr    |
  |---------+------------------|
  
  Escapes (single-quote)
  
  |----+-----+--------------+------+-----|
  | E  | ASC | Name         |  Hex | Dec |
  |----+-----+--------------+------+-----|
  | \' | '   | single-quote | 0x27 |  39 |
  | \\ | \   | backslash    | 0x5c |  92 |
  |----+-----+--------------+------+-----|
