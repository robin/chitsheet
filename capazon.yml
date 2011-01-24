--- 
capazon: |-
  Capistrano tasks to manage Amazon EC2 Images. Requires Capistrano 2.x
  http://capazon.rubyforge.org/, http://www.capify.org/
  
  gem install capazon
  
  Edit your your config/deploy.rb:
  
          require 'capazon'
  
          #AWS login info
          set :aws_access_key_id, 'XXX'
          set :aws_secret_access_key, 'X'
  
          # Name of the keypair used to spawn and connect to the Amazon EC2 Instance
          # Defaults to one created by the setup_keypair task
          set :aws_keypair_name, "#{application}-capazon"
  
          # Path to the private key for the Amazon EC2 Instance mentioned above
          # Detaults to one created by setup_keypair task
          set :aws_private_key_path, "#{Dir.pwd}/#{aws_keypair_name}-key"
  
          #defaults to an ubuntu image
          #set :aws_ami_id, "ami-e4b6538d"
  
          #defaults to, um, default
          #set :aws_security_group, "default"
