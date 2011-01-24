--- 
mysql_update: |-
  Name: 'UPDATE'
  Description:
  Syntax:
  Single-table syntax:
  
  UPDATE [LOW_PRIORITY] [IGNORE] tbl_name
      SET col_name1=expr1 [, col_name2=expr2 ...]
      [WHERE where_condition]
      [ORDER BY ...]
      [LIMIT row_count]
  
  Multiple-table syntax:
  
  UPDATE [LOW_PRIORITY] [IGNORE] table_references
      SET col_name1=expr1 [, col_name2=expr2 ...]
      [WHERE where_condition]
  
  For the single-table syntax, the UPDATE statement updates columns of
  existing rows in tbl_name with new values. The SET clause indicates
  which columns to modify and the values they should be given. The WHERE
  clause, if given, specifies the conditions that identify which rows to
  update. With no WHERE clause, all rows are updated. If the ORDER BY
  clause is specified, the rows are updated in the order that is
  specified. The LIMIT clause places a limit on the number of rows that
  can be updated.
  
  For the multiple-table syntax, UPDATE updates rows in each table named
  in table_references that satisfy the conditions. In this case, ORDER BY
  and LIMIT cannot be used.
  
  where_condition is an expression that evaluates to true for each row to
  be updated. It is specified as described in [HELP SELECT].
  
  The UPDATE statement supports the following modifiers:
  
  o If you use the LOW_PRIORITY keyword, execution of the UPDATE is
    delayed until no other clients are reading from the table. This
    affects only storage engines that use only table-level locking
    (MyISAM, MEMORY, MERGE).
  
  o If you use the IGNORE keyword, the update statement does not abort
    even if errors occur during the update. Rows for which duplicate-key
    conflicts occur are not updated. Rows for which columns are updated
    to values that would cause data conversion errors are updated to the
    closest valid values instead.
  
  
  URL: http://dev.mysql.com/doc/refman/5.0/en/update.html
