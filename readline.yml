--- 
readline: "keyboard shortcuts: \n\n\
  Moving around\n\n\
  Ctrl-a  Move the cursor   \xE2\x87\xA4 to the start of the line\n\
  Ctrl-e  Move the cursor   \xE2\x87\xA5 to the end of the line\n\n\
  Alt-b Move the cursor one word  \xE2\x87\xA6 to the left\n\
  Alt-f Move the cursor one word  \xE2\x87\xA8 to the right\n\
  Ctrl-x-x Move the cursor    \xE2\x87\xA4\xE2\x87\xA5 to the start, and to the end again\n\n\
  Cut, copy and paste\n\n\
  Ctrl-u  Delete everything  \xE2\x87\xA4 from the cursor back to the line start\n\
  Ctrl-k  Delete  everything  \xE2\x87\xA5 from the cursor to the end of the line\n\
  Alt-d   Delete  word  \xE2\x87\xA8 untill before the next word boundary\n\
  Ctrl-w  Delete  word  \xE2\x87\xA6 untill after the previous word boundary\n\
  Ctrl-y Yank/Paste  prev. killed text at the cursor position\n\n\
  Undo\n\n\
  Ctrl-_ \n\
  Ctrl+-  Undo the last editing command; you can undo all the way back to an empty line\n\n\
  History\n\n\
  Ctrl-p  Move in history one line  \xE2\x87\xA7 before this line\n\
  Ctrl-n  Move in history one line  \xE2\x87\xA9 after this line\n\
  Alt-> Move in history all the lines \xE2\x87\xA9 to the line currently being entered\n\
  Ctrl-r  Incrementally search the line history \xE2\x87\xA7 backwardly\n\
  Ctrl-s  Incrementally search the line history \xE2\x87\xA9 forwardly\n\
  Ctrl-J  End an incremental search\n\
  Ctrl-G  Abort an incremental search and restore the original line\n\n\n\n\
  ==============================================================================\n\n\
  Integrate readline into a ruby program:\n\n\
  require 'readline'\n\n\
  while line = Readline.readline('> ', history = true)\n  break if line =~ /^(quit|exit)$/\n  puts \"You typed: #{line.inspect}\"\n\
  end\n\
  puts \"Bye!\"\n\n\
  # completion\n\n\
  require 'abbrev'\n\n\
  Completors = %w[hello world of nifty_completion]\n\n\
  Readline.completion_proc = lambda{|tok| Completors.abbrev[tok] }"
