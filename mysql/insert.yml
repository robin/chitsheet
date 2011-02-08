--- 
mysql_insert: |-
  Name: 'INSERT'
  Description:
  Syntax:
  INSERT [LOW_PRIORITY | DELAYED | HIGH_PRIORITY] [IGNORE]
      [INTO] tbl_name [(col_name,...)]
      VALUES ({expr | DEFAULT},...),(...),...
      [ ON DUPLICATE KEY UPDATE col_name=expr, ... ]
  
  Or:
  
  INSERT [LOW_PRIORITY | DELAYED | HIGH_PRIORITY] [IGNORE]
      [INTO] tbl_name
      SET col_name={expr | DEFAULT}, ...
      [ ON DUPLICATE KEY UPDATE col_name=expr, ... ]
  
  Or:
  
  INSERT [LOW_PRIORITY | HIGH_PRIORITY] [IGNORE]
      [INTO] tbl_name [(col_name,...)]
      SELECT ...
      [ ON DUPLICATE KEY UPDATE col_name=expr, ... ]
  
  INSERT inserts new rows into an existing table. The INSERT ... VALUES
  and INSERT ... SET forms of the statement insert rows based on
  explicitly specified values. The INSERT ... SELECT form inserts rows
  selected from another table or tables. INSERT ... SELECT is discussed
  further in [HELP INSERT SELECT].
  
  URL: http://dev.mysql.com/doc/refman/5.0/en/insert.html
