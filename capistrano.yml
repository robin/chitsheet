--- 
capistrano: "http://www.dizzy.co.uk/cheatsheets\n\
  This work is licensed under the Creative Commons\n\
  Attribution-NonCommercial-NoDerivs 2.0 License. To\n\
  view a copy of this license, visit\n\
  http://creativecommons.org/licenses/by-nc-nd/2.0/uk\n\n\n\
  ########## Shell Commands ##########\t\n\
  Installation:\n\
  $ gem install capistrano\n\n\
  Add your application to Capistrano (capify):\n\
  $ capify .\n\n\
  # NOTE: Rake access to capistrano is deprecated in Capistrano 1.3.\n\
  #       Use the 'cap' command instead.\n\n\
  Execute the setup task:\n\
  $ cap deploy:setup\n\n\
  Deploy your application:\n\
  $ cap deploy\n\n\
  Similar to deploy, but it runs the migrate task on the new release before\n\
  updating the symlink:\n\
  $ cap deploy:migrations\n\n\
  Rollback a release from production:\n\
  $ rake rollback\n\n\
  Deploy a particular revision from Subversion\n\
  $ cap deploy -s revision=1234\n\n\
  Execute the disable_web task:\n\
  $ rake remote_exec ACTION=disable_web \\\n\
  UNTIL=\"tomorrow morning\" \\\n\
  REASON=\"vital upgrade\"\n\n\
  Using the invoke task:\n\
  $ rake remote_exec ACTION=invoke \\\n\
  COMMAND=\"svn up /u/apps/flipper/current/app/views\" \\\n\
  ROLES=app\n\n\n\
  ########## Standard Tasks ##########\n\
  cleans up the releases directory, leaving the five most recent releases:\n\
  $ cap cleanup \n\n\
  used when deploying an application for the first time. Starts the\n\
  application\xE2\x80\x99s\n\
  spinner (via the spinner task) and then does a normal deploy:\n\
  $ cap cold_deploy \n\n\
  updates all the code on your server (via update_code and symlink\n\
  tasks), then restarts the FastCGI listeners on the application servers (via\n\
  the restart task):\n\
  $ cap deploy\n\n\
  prints the difference between what was last deployed, and what is\n\
  currently in your repository:\n\
  $ cap diff_from_last_deploy\n\n\
  puts up a static maintenance page that is displayed to visitors:\n\
  $ cap disable_web\n\n\
  removes the maintenance page:\n\
  $ cap enable_web\n\n\
  allows you to send commands directly:\n\
  $ cap invoke\n\n\
  changes to the directory of your current release (as indicated by the\n\
  current symlink), and runs rake RAILS_ENV=production migrate:\n\
  $ cap migrate\n\n\
  restarts all FastCGI listeners for your application by calling the reaper\n\
  command without arguments. Only executed on :app servers\n\
  $ cap restart\n\n\
  rolls your application back to the previously deployed version\n\
  determines the previous release , updates the current symlink to point\n\
  to that, and then deletes the latest release\n\
  $ cap rollback\n\n\
  Creates and chmods the directory tree properly:\n\
  $ cap setup\n\n\
  inspect the existing tasks and display them to standard out in\n\
  alphabetical order, along with their descriptions:\n\
  $ cap show_tasks\n\n\
  starts the spinner process for your application:\n\
  $ cap spinner\n\n\
  updates the current symlink to the latest deployed version of the code\n\
  $ cap symlink\n\n\
  Checks out your source code, deletes the log and public/system\n\
  directories in your new release, symlinks log to\n\
  #{shared_path}/log, symlinks public/system to #{shared_path}/system:\n\
  $ cap update_code\n\n\n\
  ########## config/deploy.rb ##########\n\
  *Defining Tasks\n\
  task :hello_world do\n  run \"echo Hello, $HOSTNAME\"\n\
  end\n\n\
  task :hello_world, :roles => [:db, :app] do\n  puts \"calling hello_world...\"\n  hello_world\n\
  end\n\n\
  *Transactions\n\
  task :cold_deploy do\n  transaction do\n    task_one_here\n    task_two_here\n  end\n  task_three_not_in_transaction\n\
  end\n\n\
  *Capturing output with run\n\
  run \"sudo ls -la\" do |channel, stream, data|\n  if data =~ /^Password:/\n    logger.info \"#{channel[:host]} asked for password\"\n    channel.send_data \"mypass\\n\"\n  end\n\
  end\n\n\
  buffer = render(:template => \n\
  <<EXAMPLE_TEMPLATE)\n  This template will be rendered replacing variables\n  <%= like_this_variable =>\n  with their values.\n\
  EXAMPLE_TEMPLATE\n\n\
  put buffer, \"path/to/save/file.txt\", :mode => 0755\n\n\
  * multi-stage\n\
  set :stages, %w(staging production testing) # [optional] defaults to\n\
  [development, test, staging?, production].\n\
  set :default_stage, \"testing\" # [optional] if omitted, cap aborts if you don't\n\
  specify in args\n\
  require 'capistrano/ext/multistage'\n\n\
  Stage-specific code in config/deploy/staging.rb and config/deploy/production.rb.\n\
  see: http://weblog.jamisbuck.org/2007/7/23/capistrano-multistage\n\n\
  *deploy.rb variables and their defaults\n\n\
  The name of your application. \n\
  :application\t(required)\t\n\n\
  The location of your code\xE2\x80\x99s scm repository\n\
  :repository\t(required)\t\n\n\
  The address of the server to use as a gateway. \n\
  :gateway\tnil\t\t\n\n\
  The name of the user to use when logging into the remote host(s).\n\
  :user\t\tcurrent_user\t\n\n\
  The password to use for logging into the remote host(s).\n\
  :password\tpassword\t\n\n\
  The root of the directory tree on the remote host(s) that the \n\
  application should be deployed to\n\
  :deploy_to\t\xE2\x80\x9C/u/apps/#{application}\xE2\x80\x9D\n\n\
  The directory under deploy_to that should contain each deployed revision.\n\
  :version_dir\treleases\t\n\n\
  The name to use (relative to deploy_to) for the symlink that points at \n\
  the current release\n\
  :current_dir\tcurrent\t\t\n\n\
  The name of the directory under deploy_to that will contain directories and\n\
  files to be shared between all releases.\n\
  :shared_dir\tshared\t\n\n\
  This specifies the revision you want to check out on the remote machines.\n\
  :revision\t(latest)\t\n\n\
  The source control module to use. \n\
  Current supported are :subversion, :cvs, :darcs\n\
  :scm\t\tsubversion\t\n\n\
  The location on the remote host of the source control executable.\n\
  :svn,:cvs,:darcs\n\n\
  The subversion operation to use when checking out code on the remote host. \n\
  Can be set to \xE2\x80\x9Cexport\xE2\x80\x9D\n\
  :checkout\t\"co\"\t\t\n\
  \t\t\t\t\n\
  Hash of additional options passed to the SSH connection routine.\n\
  This lets you set (among other things) a non-standard port to connect on:\n\
  (ssh_options[:port] = 2345)\n\
  :ssh_options\tHash.new\t\n\
  \t\t\t\t\n\
  Whether or not tasks that can use sudo, ought to use sudo. In a shared\n\
  environment, this is typically not desirable (or possible), and\n\
  in that case you should set this variable to false\n\
  :use_sudo\ttrue\t\t\n\n\
  Sets the path to sudo.\n\
  :sudo\t\t\t\t\n\n\
  variables are set via:\n\
  set :application, \"flipper\"\n\n\n\
  ########## Interactive Shell ##########\n      (requires capistrano-1.2.0)\n\
  Shell is essentially a SSH interface to your\n\
  servers, so you can run standard commands such \n\
  as 'ls' or 'cp' as well as Capistrano-specific ones.\n\n\
  Start the interactive Capistrano shell\n\
  $ cap -v shell\n\n\
  Execute Capistrano tasks\n\
  cap> !deploy\n\
  cap> !update_code symlink\n\
  cap> !setup deploy\n\
  cap> on app2.foo.com !setup\n\
  cap> with app,db !setup deploy"
