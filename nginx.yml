--- 
nginx: |-
  If you want Nginx to always use the "Host" header as you would for virtual hosting, you can use _ as server_name as of 0.6.x. However there is a better way which I recommend. Use the following directives to use host header instead of server_name:
  optimize_server_names off;
  server_name_in_redirect off;
  
  Signals
  -------
  
  TERM (15), INT (1)  Terminate the server immediately
  QUIT (3)            Stop the server
  HUP (1)             Configuration changes, start new workers, graceful stop of
                      old workers
  USR1                Reopen log files
  USR2                Upgrade the server executable
  WINCH               Graceful Stop (parent process advise the children to exit)
