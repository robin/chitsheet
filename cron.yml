--- 
cron: |-
  To edit the crontab of the current user:
  $ crontab -e
  
  To display the crontab of the current user:
  $ crontab -l 
  
  To remove the crontab of the current user:
  $ crontab -r
  
  Basic file format:
  
  *     *   *   *    *  command to be executed
  -     -    -    -    -
  |     |     |     |     |
  |     |     |     |     +----- day of week (0 - 6) (Sunday=0)
  |     |     |     +------- month (1 - 12)
  |     |     +--------- day of month (1 - 31)
  |     +----------- hour (0 - 23)
  +------------- min (0 - 59)
  
  Expressions
  
  1,2,3   list of several values (comma-separated)
  1-3     list of consecutive values (dash)
  */2     step value (every N)
  
  Examples
  
  * 12 10-16/2 * * backup.sh
  * 12 10,12,14,16 * * backup.sh
  
  Runs backup.sh at noon on the 10th, 12th, 14th, and 16th of each month
  
  */15 9-17 * * * connection.test
  
  Runs connection.test every 15 mins between the hours or 9am and 5pm
  
  Notes:
   * Doesn't load your bash.rc.  
   * Different Path.
   * Use full, absolute paths.
   * Sends email with output from each run (only way to debug).  sSMTP is simple emailer.
   * Logs to syslog (only indicates that entry was run, no output).
