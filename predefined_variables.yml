--- 
predefined_variables: |-
  $!
  The exception information message. raise sets this variable.
  
  $@
  The backtrace of the last exception, which is the array of the string that indicates the point where methods invoked from. The elements in the format like:
  
  "filename:line"
  or
  "filename:line:in `methodname'"
  (Mnemonic: where exception occurred at.)
  
  $&
  The string matched by the last successful pattern match in this scope, or nil if the last pattern match failed. (Mnemonic: like & in some editors.) This variable is read-only.
  
  $`
  The string preceding whatever was matched by the last successful pattern match in the current scope, or nil if the last pattern match failed. (Mnemonic: ` often precedes a quoted string.) This variable is read-only.
  
  $'
  The string following whatever was matched by the last successful pattern match in the current scope, or nil if the last pattern match failed. (Mnemonic: ' often follows a quoted string.)
  
  $+
  The last bracket matched by the last successful search pattern, or nil if the last pattern match failed. This is useful if you don't know which of a set of alternative patterns matched. (Mnemonic: be positive and forward looking.)
  
  $1, $2...
  Contains the subpattern from the corresponding set of parentheses in the last successful pattern matched, not counting patterns matched in nested blocks that have been exited already, or nil if the last pattern match failed. (Mnemonic: like \digit.) These variables are all read-only.
  
  $~
  The information about the last match in the current scope. Setting this variables affects the match variables like $&, $+, $1, $2.. etc. The nth subexpression can be retrieved by $~[nth]. (Mnemonic: ~ is for match.) This variable is locally scoped.
  
  $=
  The flag for case insensitive, nil by default. (Mnemonic: = is for comparison.)
  
  $/
  The input record separator, newline by default. Works like awk's RS variable. If it is set to nil, whole file will be read at once. (Mnemonic: / is used to delimit line boundaries when quoting poetry.)
  
  $\
  The output record separator for the print and IO#write. The default is nil. (Mnemonic: It's just like /, but it's what you get "back" from Ruby.)
  
  $,
  The output field separator for the print. Also, it is the default separator for Array#join. (Mnemonic: what is printed when there is a , in your print statement.)
  
  $;
  The default separator for String#split.
  
  $.
  The current input line number of the last file that was read.
  
  $<
  The virtual concatenation file of the files given by command line arguments, or stdin (in case no argument file supplied). $<.file returns the current filename. (Mnemonic: $< is a shell input source.)
  
  $>
  The default output for print, printf. $stdout by default. (Mnemonic: $> is for shell output.)
  
  $_
  The last input line of string by gets or readline. It is set to nil if gets/readline meet EOF. This variable is locally scoped. (Mnemonic: partly same as Perl.)
  
  $0
  Contains the name of the file containing the Ruby script being executed. On some operating systems assigning to $0 modifies the argument area that the ps(1) program sees. This is more useful as a way of indicating the current program state than it is for hiding the program you're running. (Mnemonic: same as sh and ksh.)
  
  $*
  Command line arguments given for the script. The options for Ruby interpreter are already removed. (Mnemonic: same as sh and ksh.)
  
  $$
  The process number of the Ruby running this script. (Mnemonic: same as shells.)
  
  $?
  The status of the last executed child process.
  
  $:
  The array contains the list of places to look for Ruby scripts and binary modules by load or require. It initially consists of the arguments to any -I command line switches, followed by the default Ruby library, probably "/usr/local/lib/ruby", followed by ".", to represent the current directory. (Mnemonic: colon is the separators for PATH environment variable.)
  
  $"
  The array contains the module names loaded by require. Used for prevent require from load modules twice. (Mnemonic: prevent files to be doubly quoted(loaded).)
  
  $DEBUG
  The status of the -d switch.
  
  $FILENAME
  Same as $<.filename.
  
  $LOAD_PATH
  The alias to the $:.
  
  $stdin
  The current standard input.
  
  $stdout
  The current standard output.
  
  $stderr
  The current standard error output.
  
  $VERBOSE
  The verbose flag, which is set by the -v switch to the Ruby interpreter.
  
  option variables
  The variables which names are in the form of $-?, where ? is the option character, are called option variables and contains the information about interpreter command line options.
  
  $-0
  The alias to the $/.
  
  $-a
  True if option -a is set. Read-only variable.
  
  $-d
  The alias to the $DEBUG.
  
  $-F
  The alias to the $;.
  
  $-i
  In in-place-edit mode, this variable holds the extention, otherwise nil. Can be assigned to enable (or disable) in-place-edit mode.
  
  $-I
  The alias to the $:.
  
  $-l
  True if option -lis set. Read-only variable.
  
  $-p
  True if option -pis set. Read-only variable.
  
  $-v
  The alias to the $VERBOSE.
  
  Taken from: http://www.ruby-doc.org/docs/ruby-doc-bundle/Manual/man-1.4/variable.html
