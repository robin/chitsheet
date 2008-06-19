--- 
linux_network_boot: |-
  Network booting and installation of Ubuntu Linux
  
  
  mount -t iso9660 -o loop ubuntu.iso /var/www/ubuntu
  ln -s /var/www/ubuntu /tftboot
  
  in /etc/dhcpd3/dhcpd.conf
  
  ping-check = 1;
  filename = "ubuntu/install/netboot/pxelinux.0";
  subnet 192.168.1.0
  netmask 255.255.255.0 {
  range 192.168.1.10 192.168.1.254;
  }
  
  install atftp
  run atftpd as:
  
  killall inetd
  atftpd --daemon --no-fork --bind-address 192.168.1.1 /var/www/
  
  - make sure one of the interfaces (eth0, eth1 etc.) is bound to 192.168.1.1
  - make sure apache is running}
