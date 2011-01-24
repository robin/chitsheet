--- 
zsh_param: |-
  TBC
  
  ${name}			Value
  ${+name}		Set?
  ${name:+word}	Set and non-null? Yes = 'word'.
  ${name:-word}	Set and non-null? Yes = value. No = 'word'
  ${name:=word}	Unset or null? Yes = 'word'. No = value.
  ${name::=word}	Set 'name' to 'word'. Then sub value.
  ${name:?word}	Set and non-null? Yes = value. No = print 'word' and exit from shell.
  ${name#pat}		
  ${name##pat}
  
  If the pattern matches the beginning of the value of name, then substitute the value of name with the matched portion deleted; otherwise, just substitute the value of name. In the first form, the smallest matching pattern is preferred; in the second form, the largest matching pattern is preferred. If name is an array and the substitution is not quoted or the @ flag or the name[@] syntax is used, matching is performed on each array elements separately.
  
  	${name%pattern}
  
  	${name%%pattern}
  
  If the pattern matches the end of the value of name, then substitute the value of name with the matched portion deleted; otherwise, just substitute the value of name. In the first form, the smallest matching pattern is preferred; in the second form, the largest matching pattern is preferred. If name is an array and the substitution is not quoted or the @ flag or the name[@] syntax is used, matching is performed on each array elements separately.
  
  	${name:#pattern}
  
  If the pattern matches the value of name, then substitute the empty string; otherwise, just substitute the value of name. If name is an array and the substitution is not quoted or the @ flag or the name[@] syntax is used, matching is performed on each array elements separately, and the matched array elements are removed (use the M flag to remove the non-matched elements).
  
  	${#spec}
  
  If spec is one of the above substitutions, substitute the length in characters of the result instead of the result itself. If spec is an array expression, substitute the number of elements of the result.
  
  	${^spec}
  
  Turn on the value of the RC_EXPAND_PARAM option for the evaluation of spec; if the ^ is doubled, turn it off. When this option is set, array expansions of the form `foo${xx}bar', where the parameter `xx' is set to `(a b c)', are substituted with `fooabar foobbar foocbar' instead of the default `fooa b cbar'.
  
  	${=spec}
  
  Turn on the value of the SH_WORD_SPLIT option for the evaluation of spec; if the = is doubled, turn it off. When this option is set, parameter values are split into separate words using IFS as a delimiter before substitution. This is done by default in most other shells.
  
  	${~spec}
  
  Turn on the value of the GLOB_SUBST option for the evaluation of spec; if the ~ is doubled, turn it off. When this option is set, any pattern characters resulting from the substitution become eligible for file expansion and filename generation.
  
  If the colon is omitted from one of the above expressions containing a colon, then the shell only checks whether name is set or not, not whether it is null.
  
  
  If a ${...} type parameter expression or a $(...) type command substitution is used in place of name above, it is substituted first and the result is used as it were the value of name.
  
  
  If the opening brace is directly followed by an opening parenthesis the string up to the matching closing parenthesis will be taken as a list of flags. Where arguments are valid, any character, or the matching pairs (...), {...}, [...], or <...>, may be used in place of the colon as delimiters. The following flags are supported:
