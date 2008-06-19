--- 
htaccess4: "Enable Directory Browsing\r\n\
  \r\n\
  Options +Indexes\r\n\
  ## block a few types of files from showing\r\n\
  IndexIgnore *.wmv *.mp4 *.avi\r\n\
  Disable Directory Browsing\r\n\
  \r\n\
  Options All -Indexes\r\n\
  Customize Error Messages\r\n\
  \r\n\
  ErrorDocument 403 /forbidden.html\r\n\
  ErrorDocument 404 /notfound.html\r\n\
  ErrorDocument 500 /servererror.html\r\n\
  Get SSI working with HTML/SHTML\r\n\
  \r\n\
  AddType text/html .html\r\n\
  AddType text/html .shtml\r\n\
  AddHandler server-parsed .html\r\n\
  AddHandler server-parsed .shtml\r\n\
  # AddHandler server-parsed .htm\r\n\
  Change Default Page (order is followed!)\r\n\
  \r\n\
  DirectoryIndex myhome.htm index.htm index.php\r\n\
  Block Users from accessing the site\r\n\
  \r\n\
  <limit GET POST PUT>\r\n\
  order deny,allow\r\n\
  deny from 202.54.122.33\r\n\
  deny from 8.70.44.53\r\n\
  deny from .spammers.com\r\n\
  allow from all\r\n\
  </limit>\r\n\
  Allow only LAN users\r\n\
  \r\n\
  order deny,allow\r\n\
  deny from all\r\n\
  allow from 192.168.0.0/24\r\n\
  Redirect Visitors to New Page/Directory\r\n\
  \r\n\
  Redirect oldpage.html http://www.domainname.com/newpage.html\r\n\
  Redirect /olddir http://www.domainname.com/newdir/\r\n\
  Block site from specific referrers\r\n\
  \r\n\
  RewriteEngine on\r\n\
  RewriteCond %{HTTP_REFERER} site-to-block\\.com [NC]\r\n\
  RewriteCond %{HTTP_REFERER} site-to-block-2\\.com [NC]\r\n\
  RewriteRule .* - [F]\r\n\
  Block Hot Linking/Bandwidth hogging\r\n\
  \r\n\
  RewriteEngine on\r\n\
  RewriteCond %{HTTP_REFERER} !^$\r\n\
  RewriteCond %{HTTP_REFERER} !^http://(www\\.)?mydomain.com/.*$ [NC]\r\n\
  RewriteRule \\.(gif|jpg)$ - [F]\r\n\
  Want to show a \xE2\x80\x9CStealing is Bad\xE2\x80\x9D message too?\r\n\
  \r\n\
  Add this below the Hot Link Blocking code:\r\n\
  \r\n\
  RewriteRule \\.(gif|jpg)$ http://www.mydomain.com/dontsteal.gif [R,L]\r\n\
  Stop .htaccess (or any other file) from being viewed\r\n\
  \r\n\
  <files file-name>\r\n\
  order allow,deny\r\n\
  deny from all\r\n\
  </files>\r\n\
  Avoid the 500 Error\r\n\
  \r\n\
  # Avoid 500 error by passing charset\r\n\
  AddDefaultCharset utf-8\r\n\
  Grant CGI Access in a directory\r\n\
  \r\n\
  Options +ExecCGI\r\n\
  AddHandler cgi-script cgi pl\r\n\
  # To enable all scripts in a directory use the following\r\n\
  # SetHandler cgi-script\r\n\
  Password Protecting Directories\r\n\
  \r\n\
  Use the .htaccess Password Generator and follow the brief instructions!\r\n\
  \r\n\
  Change Script Extensions\r\n\
  \r\n\
  AddType application/x-httpd-php .gne\r\n\
  gne will now be treated as PHP files! Similarly, x-httpd-cgi for CGI files, etc.\r\n\
  \r\n\
  Use MD5 Digests\r\n\
  \r\n\
  Performance may take a hit but if thats not a problem, this is a nice option to turn on.\r\n\
  \r\n\
  ContentDigest On\r\n\
  The CheckSpelling Directive\r\n\
  \r\n\
  From Jens Meiert: CheckSpelling corrects simple spelling errors (for example, if someone forgets a letter or if any character is just wrong). Just add CheckSpelling On to your htaccess file.\r\n\
  \r\n\
  The ContentDigest Directive\r\n\
  \r\n\
  As the Apache core features documentation says: \xE2\x80\x9CThis directive enables the generation of Content-MD5 headers as defined in RFC1864 respectively RFC2068. The Content-MD5 header provides an end-to-end message integrity check (MIC) of the entity-body. A proxy or client may check this header for detecting accidental modification of the entity-body in transit.\r\n\
  \r\n\
  Note that this can cause performance problems on your server since the message digest is computed on every request (the values are not cached). Content-MD5 is only sent for documents served by the core, and not by any module. For example, SSI documents, output from CGI scripts, and byte range responses do not have this header.\xE2\x80\x9D\r\n\
  \r\n\
  To turn this on, just add ContentDigest On.\r\n\
  \r\n\
  Save Bandwidth\r\n\
  \r\n\
  # Only if you use PHP\r\n\
  <ifmodule mod_php4.c>\r\n\
  php_value zlib.output_compression 16386\r\n\
  </ifmodule>\r\n\
  Turn off magic_quotes_gpc\r\n\
  \r\n\
  # Only if you use PHP\r\n\
  <ifmodule mod_php4.c>\r\n\
  php_flag magic_quotes_gpc off\r\n\
  </ifmodule>"
