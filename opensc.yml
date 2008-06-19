--- 
opensc: |-
  OpenSC summary cheat sheet
  
  These hints are from: http://www.mayrhofer.eu.org/Default.aspx?pageindex=6&pageid=78
  I take no credit for Rene's work!
  
  To get reader numbers for other commands:
  	opensc-tool -l 
  
  "Formatting" a card with PKCS#15 structures:
  	pkcs15-init -r 1 --erase-card --create-pkcs15 --no-so-pin --label 'rmayrhofer' 
  
  Defining a new PIN:
  	pkcs15-init -r 1 --store-pin --label 'rmayrhofer PIN' --auth-id 01
  
  Generating a new keypair on the card:
  	pkcs15-init -r 1 --generate-key 'rsa/1024' --auth-id 01 --label 'test key 1' --public-key-label 'public test key 1' --split-key
  
  Importing an existing keypair and corresponding X.509 certificate:
  	pkcs15-init -r 1 --store-private-key gibraltar/CA/private/styx.key --id 45 --auth-id 01 --label 'test key 2 for IPSec' --split-key
  	pkcs15-init -r 1 --store-certificate gibraltar/CA/styx.pem --id 45 --auth-id 01 --label 'public test certificate 2 for IPSec'
  
  Importing a PKCS#12 file containing the certificate and private key:
  	pkcs15-init -r 1 --store-private-key gibraltar/CA/private/styx.p12 --format PKCS12 --id 45 --auth-id 01 --label 'test key 2 for IPSec' --split-key
  
  Listing PINs that can be used (or are already used) for protecting keys:
  	pkcs15-tool --reader 1 --list-keys
  
  Listing private and corresponding public keys:
  	pkcs15-tool --reader 1 --list-keys
  	pkcs15-tool --reader 1 --list-public-keys
  
  Listing X.509 certificates stored on the card:
  	pkcs15-tool --reader 1 --list-certificates
  
  Querying a key and output in ssh format:
   pkcs15-tool --reader 1 --read-ssh-key 45
   ssh-keygen -D 1
