--- 
regexp: |-
  A regexp's form is written /pattern/modifiers where "pattern" is the regular expression itself, and "modifiers" are a series of characters indicating various options.
  
  (see an alternate/more complete cheat-sheet with 'cheat regex')
  
  /i makes match case insensitive.
  /m makes the dot match newlines.
  /o causes any #{...} substitutions in a particular regex literal to be performed just once, the first time it is evaluated. Otherwise, the substitutions will be performed every time the literal generates a Regexp object.
  
  [] 	range specification (e.g., [a-z] means a letter in the range a to z)
  \w 	letter or digit; same as [0-9A-Za-z]
  \W 	neither letter or digit
  \s 	space character; same as [ \t\n\r\f]
  \S 	non-space character
  \d 	digit character; same as [0-9]
  \D 	non-digit character
  \b 	backspace (0x08) (only if in a range specification)
  \b 	word boundary (if not in a range specification)
  \B 	non-word boundary
  * 	zero or more repetitions of the preceding
  + 	one or more repetitions of the preceding
  {m,n} 	at least m and at most n repetitions of the preceding
  ? 	at most one repetition of the preceding; same as {0,1}
  | 	either preceding or next expression may match
  () 	grouping
  
  print "success" if subject =~ /regex/
  
  result = subject.gsub(/before/, "after")
  
  myarray = mystring.scan(/delimiter/)
