--- 
cpio: |-
  create an archive:
  
  touch .timestamp
  
  (edit some files)
  
  find . -newer .timestamp -print | cpio -oaBcv > ~/new-files.cpio
  
    - or -
  
  find . -newer .timestamp -print | cpio -oaBcv | gzip > ~/new-files.cpio.gz
