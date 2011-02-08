--- 
ruby_globals: |-
  Exceptions
    $!	 latest error message
    $@	 location of error
  
  IO
    $_	 string last read by gets
    $/	 input record separator
    $\	 output record separator
    $<	 concatenation stream of files given on input, or $stdin
    $>     default output for print functions, defaults to $stdout
    $FILENAME current input file from $< (i.e. $<.filename)
    $stdin standard input stream
    $stdout standard output stream
    $stderr standard error stream
    
  Processes
    $.	 line number last read by interpreter
    $0	 the name of the ruby script file
    $*	 the command line arguments
    $$	 interpreter's process ID
    $?	 exit status of last executed child process
  
  Regular Expressions
    $~	 the last regexp match on thread, as a MatchData
    $&	 string last matched by regexp		    (i.e. $~.string)
    $`	 the string before last match		    (i.e. $~.pre_match)
    $'	 the string after the last match	    (i.e. $~.post_match)
    $+	 the contents of the last matched group	    (i.e. $~[-1])
    $n	 the <n>th group in the last match, e.g. $1 (i.e. $~[n])
    $=	 Deprecated. false (default) indicates case insensive matching by default
  
  Misc
    $,	 default separator for Array.join (nil default == none)
    $;     default separator for String.split (string or regex, nil default = whitespace)
    $:	 load path for scripts/binaries when using require
    $"     all loaded scripts by require
    $LOAD_PATH same as $:
    $DEBUG status of debug / -d switch
    $VERBOSE status of verbose / -v switch
  
    $-0
  
  based on: 
    http://www.ruby-doc.org/docs/UsersGuide/rg/globalvars.html 
    http://www.zenspider.com/Languages/Ruby/QuickRef.html
