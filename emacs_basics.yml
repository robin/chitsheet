--- 
emacs_basics: |-
  Commands to Manipulate Files
  
  C-x C-f    find-file.
  C-x C-s    save-buffer. Save.
  C-x s      save-some-buffers. Save All.
  
  
  Commands to Manipulate Buffers
  
  C-x b      switch-to-buffer.
  C-x C-b    list-buffers. 
  C-x k      kill-buffer. Asks to save if modified. 
  C-x C-q    vc-toggle-read-only. Toggle read-only <-> read-write. If the file
             under version control, it will check the file out for you. 
  
  
  Commands to Manipulate Windows
  
  C-v        scroll-up. 
  M-v        scroll-down.
  C-x o      other-window. Switch to another window.
  C-x 1      delete-other-windows. Deletes all other windows except the current
             one.
  C-x 0      delete-window. Deletes just the current window.
  C-x 2      split-window-vertically. Splits the current window in two,
             vertically.
  C-x 3      split-window-horizontally. Splits the current window in two,
             horizontally.
  C-M-v      scroll-other-window. Just like C-v, but scrolls the other window.
  
  
  Infinite Undo with Redo
  
  C-_        undo. (Also C-x u and C-/)
  
  
  Motion and Objects
  
  C-f      forward-char. Moves forward (to the right) over a character.
  C-b      backward-char. Moves backward (to the left) over a character.
  M-f      forward-word. Moves forward over a word.
  M-b      backward-word. Moves backward over a word.
  C-n      next-line. Moves down to the next line.
  C-p      previous-line. Moves up to the previous line.
  C-a      beginning-of-line. Moves to the beginning of the current line.
  C-e      end-of-line. Moves to the end of the current line.
  M-a      backward-sentence. Moves to the beginning of the current sentence.
  M-e      forward-sentence. Moves to the end of the current sentence.
  M-{      backward-paragraph. Move to the beginning of the current paragraph.
  M-}      forward-paragraph. Move to the end of the current paragraph.
  C-x [    backward-page. Moves to the beginning of the current page.
  C-x ]    forward-page. Moves to the end of the current page.
  M-<      beginning-of-buffer. Moves to the beginning of the buffer.
  M->      end-of-buffer. Moves to the end of the buffer.
  C-M-f    forward-sexp. Move forward one 'balanced expression'.
  C-M-b    backward-sexp. Move backward one 'balanced expression'.
  
  
  Regions
  
  Regions are areas of text that you select to operate on. Operations can
  including killing / deleting, copying, re-indenting, counting lines,
  etc. Normally, you select a region by placing a 'mark' at one end-point of the
  region you want, and moving the point (or cursor) to the other end before
  invoking the command you want.
  
  C-SPC    set-mark-command. Places a mark at the current point or cursor
           position.
  C-x C-x  exchange-point-and-mark. Move between the current position and the
           mark.
  C-x h    mark-whole-buffer. Mark the entire buffer.
  C-M-SPC  mark-sexp. Mark the expression following the point.
  
  
  Copying, Deleting, Killing and Yanking
  
  Deletion means to remove text from the buffer without saving it.  Killing
  means to save the removed text, so that it can be yanked back later someplace
  else.
  
  C-d            delete-char. Deletes the character to the right of (under, if
  	       the cursor is a block that covers a character) the cursor. 
  DEL or C-?     delete-backward-char. Deletes the character to the left of the
                 cursor. 
  C-y            yank. Yanks text, inserting whatever text you killed last.
  C-w            kill-region. Kills the region of text between the point and the
                 cursor.
  M-w            kill-ring-save. Save the region as if killed, but don't kill
                 it. AKA Copy.
  C-M-w          append-next-kill. If the next command kills text, append it to
                 the last thing killed instead of replaceing it.
  M-d            kill-word. Kills to the end of the word to the right of the
                 cursor (forward). 
  M-DEL          backward-kill-word. Kills to the beginning of the word to the
                 left of the cursor (backward). 
  C-k            kill-line. Kills to the end of the current line.
  C-u 0 C-k      kill-line. Kills to the beginning of the current line.
  C-u -1 C-k     kill-line. Kills to the beginning of the current line, and
                 previous newline character.
  M-k            kill-sentence. Kills to the end of the current sentence.
  C-u -1 M-k     kill-sentence. Kills to the beginning of the current sentence.
  C-M-k          kill-sexp. Kills the sexp after the cursor.
  C-u -1 C-M-k   kill-sexp. Kills the sexp before the cursor.
  
  
  Help
  
  C-h a   command-apropos.  List commands matching the given name or regexp.
  C-h f   describe-function.  Show documentation on the given function.
  C-h v   describe-variable.  Show documentation on the given variable.
  C-h c   describe-key-briefly.  Name the function bound to the given key
          sequence.
  C-h k   describe-key.  Show documentation for the function bound to the given
          key sequence.
  C-h w   where-is.      Show key sequences bound to the given command name.
  C-h m   describe-mode. Documentation on the current major mode.
  C-h l   view-lossage.  Show the last 100 keystrokes.
  
  C-h after any prefix key will display all available shortcuts under that prefix.
  
  From http://www.lib.uchicago.edu/keith/tcl-course/emacs-tutorial.html
