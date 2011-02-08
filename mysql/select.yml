--- 
mysql_select: |-
  EXPORT TO CSV [http://forums.mysql.com/read.php?79,11324,13062#msg-13062]
  
  SELECT a,b,a+b INTO OUTFILE '/tmp/result.text'
  FIELDS TERMINATED BY ',' OPTIONALLY ENCLOSED BY '"'
  LINES TERMINATED BY '\n'
  FROM test_table;
  
  
  # Find null or empty values
  SELECT * FROM  `sti_stories` WHERE i_am IS NULL OR i_am =  ''
