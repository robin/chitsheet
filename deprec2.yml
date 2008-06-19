--- 
deprec2: "This is a copy of Chris Turners deprec2 howto (found here http://crackthenut.cracklabs.com/deprec2-your-slice/).  I'm adding it here because his site is down at the moment and I almost cried myself to sleep at the thought of losing it (thank you google cache)\r\n\
  \r\n\
  ------------------------------\r\n\
  \r\n\
  This is a summary of how we build our servers and deploy our Rails apps from Ubuntu with the the current pre-release version of deprec2 + capistrano2.\r\n\
  \r\n\
  We use Slicehost to host our Rails apps (highly recommended) and we use deprec + capistrano to build our slices and deploy our apps. Mike Bailey has been hard at work on deprec2, which builds on capistrano2 by Jamis Buck. Thank you to Mike and Jamis for making these great tools that make life easier.\r\n\
  \r\n\
  The machine I was deploying from here (my \xE2\x80\x9Cdevelopment\xE2\x80\x9D machine) is an Ubuntu Dapper slice with Ruby 1.8.6 and rubygems 1.0.1.\r\n\
  \r\n\
  The target machine here was a Slicehost slice with Ubuntu Gutsy.\r\n\
  \r\n\
  This will build the slice with Ruby 1.8.6 and latest rails (2.0.2 as of this writing) For serving up your app it installs mongrel+nginx (not apache - though it can easily be modified to use it)\r\n\
  \r\n\
  We use another remote machine to hold our source repositories and access those via the svn+ssh protocol. That is reflected in these instructions.\r\n\
  \r\n\
  Step 1 gets your development machine set up properly and is a one-time deal. You won\xE2\x80\x99t have to repeat it for each new slice you build/deploy to.\r\n\
  \r\n\
  Step 2 installs everything you\xE2\x80\x99ll need on your slice and deploys your app\r\n\
  \r\n\
  I wanted to get this posted sooner rather than later - it may be a bit terse - let me know if anything is confusing or inaccurate. I\xE2\x80\x99ll TRY to keep these instruction updated as deprec2 moves into full release and other things change.\r\n\
  Step 1 - Set Up The Machine You Are Deploying From (running Ubuntu in this case)\r\n\
  \r\n\
  This will make sure your development machine is set up the right way so that building your slice goes smoothly. You won\xE2\x80\x99t have to repeat this when you build/deploy to future slices.\r\n\
  1.1. Download the pre-release deprec2 gem\r\n\
  \r\n\
  Deprec 2.0 isn\xE2\x80\x99t quite released yet, but there is a pre-release gem available.\r\n\
  As of this writing it is at version 1.99-13. You can find it at deprec.org.\r\n\
  \r\n\
  The URL is almost guaranteed to change, but I\xE2\x80\x99ve been grabbing the gem by:\r\n\
  \r\n\
  wget http://www.deprec.org/attachment/wiki/WikiStart/deprec-1.99.13.gem?format=raw -O deprec-1.99.13.gem\r\n\
  \r\n\
  1.2. Install Deprec\r\n\
  \r\n\
  sudo gem install deprec-1.99.13.gem\r\n\
  \r\n\
  Make sure you run this command from the same directory where you downloaded the deprec gem to.\r\n\
  This will also install the latest version of capistrano, should you not already have it.\r\n\
  1.3. Install fastthread\r\n\
  \r\n\
  sudo gem install fastthread\r\n\
  \r\n\
  Fastthread is necessary if you are using Ruby 1.8.6 to avoid possible deadlocks when using capistrano (or so I hear)\r\n\
  1.4. Generate keys\r\n\
  \r\n\
  ssh-keygen -t rsa\r\n\
  \r\n\
  Accept the default name/location.\r\n\
  \r\n\
  Enter a passphrase if you wish.\r\n\
  \r\n\
  On my machine this creates my keys in /home/username/.ssh\r\n\
  1.5. Setup a directory we can use for holding slice config files\r\n\
  \r\n\
  This directory is not specific to any one rails project and once we set it up we can use\r\n\
  it in the future to do some of the initial setup for other slices we may build.\r\n\
  \r\n\
  From within /home/username:\r\n\
  \r\n\
  mkdir -p config_slices/config\r\n\
  \r\n\
  1.6. Create some files for Deprec/Capistrano\r\n\
  \r\n\
  Change to your config_slices directory and:\r\n\
  \r\n\
  depify .\r\n\
  \r\n\
  This creates:\r\n\
  ~/.caprc\r\n\
  ~/config_slices/Capfile\r\n\
  ~/config_slices/config/deploy.rb\r\n\
  \r\n\
  1.7. Edit your .caprc\r\n\
  \r\n\
  Open up ~/.caprc with a text editor\r\n\
  \r\n\
  Uncomment and update this line to point at the appropriate directory\r\n\
  \r\n\
  ssh_options[:keys] = %w(/path/to/your_home_dir/.ssh/id_rsa)\r\n\
  \r\n\
  like this on my machine:\r\n\
  \r\n\
  ssh_options[:keys] = %w(/home/username/.ssh/id_rsa)\r\n\
  \r\n\
  and uncomment these lines:\r\n\
  \r\n\
  ssh_options[:forward_agent] = ...\r\n\
  ssh_options[:paranoid] = ...\r\n\
  \r\n\
  1.8. Generate some config files locally that will be pushed out to your slice in a future step\r\n\
  \r\n\
  Make sure you are still in config_slices directory\r\n\
  \r\n\
  cap deprec:ssh:config_gen\r\n\
  \r\n\
  This step generates configuration files which will be used to configure the ssh client and server on the slice.\r\n\
  It also makes a directory to hold public keys for you and other users so deprec can find your keys and copy those out to the slice for you.\r\n\
  1.9. (optional) Make some changes to the sshd_config before you send it to the slice\r\n\
  \r\n\
  This step changes a couple settings in the the file that will be used to configure the slice\xE2\x80\x99s ssh server.\r\n\
  It will be more secure if you don\xE2\x80\x99t make either of these changes, but there is a chance you might find them to be useful.\r\n\
  \r\n\
  Edit ~/config_slices/config/ssh/etc/ssh/sshd_config\r\n\
  \r\n\
  If you still want to be able to ssh into your slice with a password (not only keys), change the line from\r\n\
  \r\n\
  PasswordAuthentication no\r\n\
  \r\n\
  to\r\n\
  \r\n\
  PasswordAuthentication yes\r\n\
  \r\n\
  If you still want to be able to ssh into your slice as root, change the line from\r\n\
  \r\n\
  PermitRootLogin no\r\n\
  \r\n\
  to\r\n\
  \r\n\
  PermitRootLogin yes\r\n\
  \r\n\
  1.10. Make some changes to the ssh_config before you send it to the slice\r\n\
  \r\n\
  This step changes a couple settings in the the file that will be used to configure the slice\xE2\x80\x99s ssh client.\r\n\
  This prevents the slice from getting a host key error when it uses ssh to check out your code from the svn repo.\r\n\
  \r\n\
  Edit ~/config_slices/config/ssh/etc/ssh/ssh_config\r\n\
  \r\n\
  Change:\r\n\
  \r\n\
  #StrictHostKeyChecking ask\r\n\
  \r\n\
  to\r\n\
  \r\n\
  StrictHostKeyChecking no\r\n\
  \r\n\
  1.11. Copy your public key to a place where deprec can find it\r\n\
  \r\n\
  cp ~/.ssh/id_rsa.pub ~/config_slices/config/ssh/authorized_keys/deploy_user\r\n\
  \r\n\
  Note: this copies and renames the file from id_rsa.pub to deploy_user\r\n\
  \r\n\
  You can put whatever you want for deploy_user - this will be the username we create on the slice later. I just use my last name. deprec makes it easy to add/manage additional users on the slice in the future - no need to have a single, dedicated \xE2\x80\x9Cdeploy\xE2\x80\x9D user.\r\n\
  1.12. Copy your public key out to your svn machine\r\n\
  \r\n\
  PUT SOMETHING HERE\r\n\
  \r\n\
  Step 2 - Set up your slice and deploy your app\r\n\
  \r\n\
  Now that our development machine is set up we can move on to dealing with our slice.\r\n\
  2.1. Create a new slice or rebuild one from SliceManager\r\n\
  \r\n\
  Note your slice\xE2\x80\x99s IP address and new root password.\r\n\
  2.2. Change the root password on the slice\r\n\
  \r\n\
  From within config_slices directory:\r\n\
  \r\n\
  cap deprec:users:passwd USER=root HOSTS=your.slice.ip.address\r\n\
  \r\n   1. You will be prompted for which user to change the password for - default is root, which is what we want - so just hit enter\r\n   2. You will be prompted for root\xE2\x80\x99s new password - type one in\r\n   3. You will be prompted for the slice\xE2\x80\x99s current root password - enter the password slicehost emailed you\r\n\
  \r\n\
  Your slice\xE2\x80\x99s root password has been changed.\r\n\
  2.3. Create a new user on the slice to do your deployment with\r\n\
  \r\n\
  From within config_slices directory:\r\n\
  \r\n\
  cap deprec:users:add USER=root HOSTS=your.slice.ip.address\r\n\
  \r\n   1. You will be prompted for a new username - enter whatever you used for deploy_user in step 1.11\r\n   2. You will be asked if this should be an admin account -> enter yes\r\n   3. It should tell you it has found the key you copied above (if not you named the key wrong or did not copy it to the correct place in 1.11) and ask if you want to copy it out to the slice - default is yes - so hit enter\r\n   4. You will be prompted for a new password for deploy_user -> enter one\r\n   5. You will be prompted for a password - enter your slice\xE2\x80\x99s new root password from previous step\r\n\
  \r\n\
  Your deploy_user has now been created on the slice and that users public key has been copied over.\r\n\
  2.4. (optional) Make sure your keys work and some stuff about ssh-agent\r\n\
  \r\n\
  At this point your user has been created on the slice and you should be able to ssh into the\r\n\
  slice from your development machine.\r\n\
  \r\n\
  If you want to make sure your keys are working properly:\r\n\
  \r\n\
  PLACEHOLDER:\r\n\
  \r\n\
  -test ssh into your slice with no password\r\n\
  \r\n\
  -instruction for running ssh-agent to eliminate passphrases and make sure key can get forwarded to svn if applicable\r\n\
  \r\n\
  -also test you can also ssh into your svn (if you use svn+ssh) - if not then add public key to authorized_keys on svn machine\r\n\
  2.5. Copy the ssh/sshd configs over to the slice\r\n\
  \r\n\
  From within config_slices directory:\r\n\
  \r\n\
  cap deprec:ssh:config USER=deploy_user HOSTS=my.slice.ip.address\r\n\
  \r\n\
  This configures the ssh client and server on the slice according to the config files we generated/edited in Step 1.\r\n\
  2.6. Setup your deploy.rb\r\n\
  \r\n\
  cd my_rails_project\r\n\
  depify .\r\n\
  \r\n\
  Edit my_rails_project/config/deploy.rb:\r\n\
  \r\n\
  If you do not keep database.yml under source control add this line at the top (after require \xE2\x80\x98deprec\xE2\x80\x99):\r\n\
  \r\n\
  set :database_yml_in_scm, false\r\n\
  \r\n\
  This will make sure that database.yml is symlinked from the shared/config dir (we\xE2\x80\x99ll create that file later)\r\n\
  If you keep database.yml in source control you should not put this line in.\r\n\
  \r\n\
  Now change the following lines to match your specifics:\r\n\
  \r\n\
  set :user, \"deploy_user\"\r\n\
  set :application, \"my_rails_project\"\r\n\
  set :repository,  \"svn+ssh://my_svn_useruser@my_svn/path_to/my_rails_project/trunk\"  #or whatever\r\n\
  set :domain, \"my.slice.ip.address\" #or domain name if you have that setup\r\n\
  role :app, domain\r\n\
  role :web, domain\r\n\
  role :db,  domain, :primary => true\r\n\
  \r\n\
  2.7. Install ruby/rails/mysql/mongrel/nginx and everything else you need on the slice\r\n\
  \r\n\
  From within my_rails_project directory:\r\n\
  \r\n\
  cap deprec:rails:install_rails_stack\r\n\
  \r\n\
  And you thought that would be hard\xE2\x80\xA6\r\n\
  This step saves you a LOT of work (thank you Mike Bailey)\r\n\
  It takes a little while, ~10 min when I ran it.\r\n\
  2.8. Run the initial deploy to get things configured\r\n\
  \r\n\
  From within my_rails_project directory:\r\n\
  \r\n\
  cap deploy:setup\r\n\
  cap deploy\r\n\
  \r\n\
  This sets up your application on the slice and does an initial check out from your svn.\r\n\
  2.9. Create database.yml on the slice if you don\xE2\x80\x99t keep it in source control\r\n\
  \r\n\
  Skip this step if database.yml is under source control.\r\n\
  \r\n\
  Add the following to my_rails_project/config/deploy.rb inside the namespace:deploy block\r\n\
  \r\n\
  db_params = {\r\n  \"adapter\"=>\"mysql\",\r\n  \"database\"=>\"#{application}_#{rails_env}\",\r\n  \"username\"=>\"root\",\r\n  \"password\"=>\"\",\r\n  \"host\"=>\"localhost\",\r\n  \"socket\"=>\"\"\r\n\
  }\r\n\
  \r\n\
  db_params.each do |param, default_val|\r\n  set \"db_#{param}\".to_sym,\r\n    lambda { Capistrano::CLI.ui.ask \"Enter database #{param}\" do |q| q.default=default_val end}\r\n\
  end\r\n\
  \r\n\
  task :my_generate_database_yml, :roles => :app do\r\n  database_configuration = \"#{rails_env}:\\n\"\r\n  db_params.each do |param, default_val|\r\n    val=self.send(\"db_#{param}\")\r\n    database_configuration<<\"  #{param}: #{val}\\n\"\r\n  end\r\n  run \"mkdir -p #{deploy_to}/#{shared_dir}/config\"\r\n  put database_configuration, \"#{deploy_to}/#{shared_dir}/config/database.yml\"\r\n\
  end\r\n\
  \r\n\
  Now run this task to create database.yml\r\n\
  \r\n\
  cap deploy:my_generate_database_yml\r\n\
  \r\n\
  Follow the prompts - this makes database.yml - the defaults are likely ok (just hit enter) at all of the prompts.\r\n\
  \r\n\
  2.10. Create the database and apply migrations\r\n\
  \r\n\
  Still from within my_rails_project directory:\r\n\
  \r\n\
  cap deprec:db:create\r\n\
  cap deprec:db:migrate\r\n\
  \r\n\
  This creates your database and applies your migrations.\r\n\
  \r\n\
  2.11. Restart mongrel+nginx\r\n\
  \r\n\
  Still from within my_rails_project directory:\r\n\
  \r\n\
  cap deprec:mongrel:restart\r\n\
  cap deprec:nginx:restart\r\n\
  \r\n\
  Now you should be able to point your browser at your slice and see your app running. Congrats!"
