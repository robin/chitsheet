--- 
zsh_rename: |-
  # Renaming files with Zsh
  
  
  ### Numerical prefix:
  $  i=1; for j in *; do mv $j $i.$j; ((i++)); done
    	 
  $  i=1; for f in *; do mv $f $(echo $i| awk '{ printf("%03d", $0)}').$f; ((i++)); done
  
  $  integer i=0; for f in *; do mv $f $[i+=1].$f; done
  
  
  ### Rename all files from name.mp3 to Name.mp3:
  $  zmv `([a-z])(*).mp3` `${(C)1}$2.mp3`	
  
  ### Capitalize file
  $  zmv '([a-z])(*).pdf' '${(C)1}$2.pdf'
  
  ### Replaces spaces with underlines
  $  zmv '* *' '$f:gs/ /_'
  
  ### FOO to foo
  $  for i in *(.); mv $i ${i:l}
  
  ### Rename pic1.jpg to pic0001.jpg ...
  $  zmv 'pic(*).jpg' 'pic${(1:4::0:)1}.jpg'
  $  zmv '(**/)pic(*).jpg' '$1/pic1:4::0:)2}.jpg'  # recursive
  
  ### Remove spaces from filenames
  $  for a in ./**/*\ *(Dod); do mv $a ${a:h}/${a:t:gs/ /_}; done
  
  ### Substitute r for l
  
  		s/l/r[/]
  
  Unless preceded immediately by a g, with no colon between, the substitution is done only for the first string that matches l. For arrays and filename expansion, this applies to each word of the expanded text. 
  
  The left-hand side of substitutions are not regular expressions, but character strings. 
  
  Any character can be used as the delimiter in place of '/'. A backslash quotes the delimiter character.
  
  The character '&', in the right-hand-side r, is replaced by the text from the left-hand-side l. The '&' can be quoted with a backslash. 
  
  [See Zshlovers for more]
