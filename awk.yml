--- 
awk: |-
  Useful awk programs are often short, just a line or two. Here is a collection
  of useful, short programs to get you started. Some of these programs contain
  constructs that haven't been covered yet. The description of the program will
  give you a good idea of what is going on, but please read the rest of the
  manual to become an awk expert!
  
  awk '{ if (NF > max) max = NF }
       END { print max }'
      This program prints the maximum number of fields on any input line. 
  awk 'length($0) > 80'
      This program prints every line longer than 80 characters. The sole rule has a relational expression as its pattern, and has no action (so the default action, printing the record, is used). 
  awk 'NF > 0'
      This program prints every line that has at least one field. This is an easy way to delete blank lines from a file (or rather, to create a new file similar to the old file but from which the blank lines have been deleted). 
  awk '{ if (NF > 0) print }'
      This program also prints every line that has at least one field. Here we allow the rule to match every line, then decide in the action whether to print. 
  awk 'BEGIN { for (i = 1; i <= 7; i++)
                 print int(101 * rand()) }'
      This program prints 7 random numbers from 0 to 100, inclusive. 
  ls -l files | awk '{ x += $4 } ; END { print "total bytes: " x }'
      This program prints the total number of bytes used by files. 
  expand file | awk '{ if (x < length()) x = length() }
                    END { print "maximum line length is " x }'
      This program prints the maximum line length of file. The input is piped through the expand program to change tabs into spaces, so the widths compared are actually the right-margin columns. 
  awk 'BEGIN { FS = ":" }
       { print $1 | "sort" }' /etc/passwd
      This program prints a sorted list of the login names of all users. 
  awk '{ nlines++ }
       END { print nlines }'
      This programs counts lines in a file. 
  awk 'END { print NR }'
      This program also counts lines in a file, but lets awk do the work. 
  awk '{ print NR, $0 }'
      This program adds line numbers to all its input files, similar to `cat -n'.
  awk -F "\"*,\"*" '{print $3}' file.csv
      CSV parsing, prints 3rd field
