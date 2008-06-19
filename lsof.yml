--- 
lsof: |-
  lsof -i
   -- Show all connections
  
  lsof -iTCP
   -- Show only TCP connections (works the same for UDP)
  
  lsof -i :22
   -- -i :port shows all networking related to a given port
  
  lsof -i@192.168.1.5
   -- To show connections to a specific host, use @host
  
  lsof -i@192.168.1.5:22
   -- Show connections based on the host and the port using @host:port
  
  lsof -i| grep LISTEN
   -- Grepping for "LISTEN" shows what ports your system is waiting for connections on
  
  lsof -i| grep ESTABLISHED
   -- Grepping for "ESTABLISHED" shows current active connections
  
  lsof -u ecable
   -- Show what a given user has open using -u
  
  lsof -c syslog-ng
   -- See what files and network connections a command is using with -c
  
  lsof /var/log/messages
   -- Pointing to a file shows what's interacting with that file
  
  lsof -p 10075
   -- The -p switch lets you see what a given process ID has open, which is good for learning more about unknown processes
  
  lsof -t -c Mail
   -- The -t option returns just a PID
  
  lsof -a -u ecable -i @1.1.1.1
   -- Using-a allows you to combine search terms, so the query below says, "show me everything running as daniel connected to 1.1.1.1"
  
  kill -HUP `lsof -t -c sshd`
   -- Using the -t and -c options together you can HUP processes
  
  kill -9 `lsof -t -u daniel`
   -- You can also use the -t with -u to kill everything a user has open
  
  lsof +L1
   -- lsof +L1 shows you all open files that have a link count less than 1, often indicative of a cracker trying to hide something
