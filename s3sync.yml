--- 
s3sync: |-
  S3SYNC
  ------
  
  s3sync.rb [options] <source> <destination>              version 1.1.4
    --help    -h          --verbose     -v     --dryrun    -n
    --ssl     -s          --recursive   -r     --delete
    --public-read -p      --expires="<exp>"    --cache-control="<cc>"
    --exclude="<regexp>"  --progress           --debug   -d           
  One of <source> or <destination> must be of S3 format, the other a local path.
  
  Examples: (using S3 bucket 'bucket' and prefix 'pre')
    Put the local etc directory itself into S3
          s3sync.rb  -r  /etc  bucket:pre
          (This will yield S3 keys named  pre/etc/...)
    Put the contents of the local /etc dir into S3, rename dir:
          s3sync.rb  -r  /etc/  bucket:pre/etcbackup
          (This will yield S3 keys named  pre/etcbackup/...)
    Put contents of S3 "directory" etc into local dir
          s3sync.rb  -r  bucket:pre/etc/  /root/etcrestore
          (This will yield local files at  /root/etcrestore/...)
    Put the contents of S3 "directory" etc into a local dir named etc
          s3sync.rb  -r  bucket:pre/etc  /root
          (This will yield local files at  /root/etc/...)
  
  
  S3CMD
  -----
  
  s3cmd.rb [options] <command> [arg(s)]           version 1.0.0
    --help    -h        --verbose     -v     --dryrun    -n
    --ssl     -s        --debug       -d
  
  Commands:
  s3cmd.rb  listbuckets  [headers]
  s3cmd.rb  createbucket|deletebucket  <bucket>  [headers]
  s3cmd.rb  list  <bucket>[:prefix]  [max/page]  [delimiter]  [headers]
  s3cmd.rb  delete  <bucket>:key  [headers]
  s3cmd.rb  deleteall  <bucket>[:prefix]  [headers]
  s3cmd.rb  get|put  <bucket>:key  <file>  [headers]
  
  Examples
  --------
  List all the buckets your account owns:
  	s3cmd.rb listbuckets
  
  Create a new bucket:
  	s3cmd.rb createbucket BucketName
  
  Delete an old bucket you don't want any more:
  	s3cmd.rb deletebucket BucketName
  	
  Find out what's in a bucket, 10 lines at a time:
  	s3cmd.rb list BucketName 10
  	
  Only look in a particular prefix:
  	s3cmd.rb list BucketName:startsWithThis
  	
  Look in the virtual "directory" named foo;
  lists sub-"directories" and keys that are at this level.
  Note that if you specify a delimiter you must specify a max before it.
  (until I make the options parsing smarter)
  	s3cmd.rb list BucketName:foo/  10  /
  
  Delete a key:
  	s3cmd.rb delete BucketName:AKey
  
  Delete all keys that match (like a combo between list and delete):
  	s3cmd.rb deleteall BucketName:SomePrefix
  	
  Only pretend you're going to delete all keys that match, but list them: 
  	s3cmd.rb  --dryrun  deleteall  BucketName:SomePrefix
  	
  Delete all keys in a bucket (leaving the bucket):
  	s3cmd.rb deleteall BucketName
  	
  Get a file from S3 and store it to a local file
  	s3cmd.rb get BucketName:TheFileOnS3.txt  ALocalFile.txt
  	
  Put a local file up to S3 
  Note we don't automatically set mime type, etc.
  NOTE that the order of the options doesn't change. S3 stays first!
  	s3cmd.rb put BucketName:TheFileOnS3.txt ALocalFile.txt
