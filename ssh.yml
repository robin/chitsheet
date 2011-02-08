--- 
ssh: |-
  Authenticating via key pair (password-less)
  
  connecting from client to server (all command lines are run from the client)
  
   create the key pair (ALWAYS give a strong password)
    $ ssh-keygen
  
   create the key pair (DSA)
    $ ssh-keygen -t dsa -b 1024 
  
   authorize client's key with server
    $ cat ~/.ssh/id_rsa.pub | ssh user@server \
          'mkdir ~/.ssh; touch ~/.ssh/authorized_keys;
           chmod a=,u=Xrw -R ~/.ssh;
           cat - >> ~/.ssh/authorized_keys'
  
  After that, you should be able to login to server using the password that you used to encrypt your private key.  If you password protected your private key (strongly recommended), then you should run ssh-agent within your session, and then add the key to the agent:
  
   see if ssh-agent is running (some systems start it up by default)
    $ ps `echo $SSH_AGENT_PID`
  
   if ssh-agent isn't running
    $ eval `ssh-agent`
   or find a way to run it when your login session starts
  
   add your key to the agent
    $ ssh-add
  
  After that, you should not need to type the password again during this session.
  
  See http://uwstopia.nl/blog/2006/08/password-hell-gdm-ssh-gnome-keyring to make ssh-add unnecessary.
  
  
  SSH Tunnels
  
  Basic:
  $ ssh -fN -L localport:destination:destport user@remotehost
  
  Reverse:
  $ ssh -fN -R remoteport:localhost:localport user@remotehost
  
  Reverse, bound to all interfaces on remotehost:
  $ ssh -fN -R *:remoteport:localhost:localport user@remotehost
  (this requires "GatewayPorts yes" to be set in sshd_config on remotehost)
  
  Examples:
  
  To allow anonymous access to mongrel on localhost, without network-level port forwarding:
  $ ssh -fN -R *:8080:localhost:3000 user@remotehost
  Any requests to http://remotehost:8080 will be forwarded to localhost 3000.
