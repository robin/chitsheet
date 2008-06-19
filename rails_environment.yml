--- 
rails_environment: "Source: http://glu.ttono.us/articles/2006/05/22/configuring-rails-environments-the-cheat-sheet\n\n\
  = General Options =\n\
  For more detailed documentation, see the source code directly. \n\
  Each of these options should be prepended with config. when used with a Rails::Initializer do |config| block.\n\n\
  breakpoint_server\n    Whether or not to use the breakpoint server (boolean)\n\
  cache_classes\n    Whether or not classes should be cached (set to false if you want application classes to be reloaded on each request)\n\
  connection_adapters\n    The list of connection adapters to load.\n    By default, all connection adapters are loaded. You can set this to be just the adapter(s) you will use to reduce your application's load time.\n\
  controller_paths\n    The list of paths that should be searched for controllers.\n    Defaults to app/controllers and components.\n\
  database_configuration_file\n    The path to the database configuration file to use.\n    Defaults to config/database.yml.\n\
  frameworks\n    The list of rails framework components that should be loaded.\n    Defaults to :active_record, :action_controller, :action_view, :action_mailer, and :action_web_service.\n\
  load_paths\n    An array of additional paths to prepend to the load path.\n    By default, all app, lib, vendor and mock paths are included in this list.\n\
  log_level\n    The log level to use for the default Rails logger.\n    In production mode, this defaults to :info. In development mode, it defaults to :debug.\n\
  log_path\n    The path to the log file to use.\n    Defaults to log/#{environment}.log (e.g. log/development.log or log/production.log).\n\
  logger\n    The specific logger to use.\n    By default, a logger will be created and initialized using #log_path and #log_level, but a programmer may specifically set the logger to use via this accessor and it will be used directly.\n\
  view_path\n    The root of the application's views.\n    Defaults to app/views.\n\
  whiny_nils\n    Set to true if you want to be warned (noisily) when you try to invoke any method of nil. Set to false for the standard Ruby behavior.\n\
  plugin_paths\n    The path to the root of the plugins directory.\n    By default, it is in vendor/plugins.\n\n\n\
  = ActiveRecord Options =\n\
  Each of these options should be prepended with config.active_record. when used with a Rails::Initializer do |config| block.\n\n\
  primary_key_prefix_type\n    Accessor for the prefix type that will be prepended to every primary key column name. The options are :table_name and :table_name_with_underscore. If the first is specified, the Product class will look for \xE2\x80\x9Cproductid\xE2\x80\x9D instead of \xE2\x80\x9Cid\xE2\x80\x9D as the primary column. If the latter is specified, the Product class will look for \xE2\x80\x9Cproduct_id\xE2\x80\x9D instead of \xE2\x80\x9Cid\xE2\x80\x9D. Remember that this is a global setting for all Active Records.\n\
  table_name_prefix\n    The string to prepend to every table name.\n    By default, the prefix is an empty string\n\
  table_name_suffix\n    The same as table_name_prefix, but it appends the string to the table name.\n\
  pluralize_table_names\n    Indicates whether or not table names should be the pluralized versions of the corresponding class names.\n    Defaults to true.\n\
  colorize_logging\n    Should logs have ANSI color codes in logging statments?\n    Defaults to true\n\
  default_timezone\n    Determines whether to use Time.local (using :local) or Time.utc (using :utc) when pulling dates and times from the database.\n    Defaults to :local by default.\n\
  allow_concurrency\n    Determines whether or not to use a connection for each thread, or a single shared connection for all threads.\n    Defaults to false. Set to true if you're writing a threaded application.\n\
  generate_read_methods\n    Determines whether to speed up access by generating optimized reader methods to avoid expensive calls to method_missing when accessing attributes by name. You might want to set this to false in development mode, because the methods would be regenerated on each request.\n\
  schema_format\n    Specifies whether to dump the database in ruby or sql. It takes :ruby or :sql as options, and defaults to :ruby\n\n\n\
  = ActionController Options =\n\
  Each of these options should be prepended with config.action_controller. when used with a Rails::Initializer do |config| block.\n\n\
  view_controller_internals\n    Determines whether the view has access to controller internals @request, @response, @session, and @template.\n\
  assert_host\n    Prepends all the URL-generating helpers from AssetHelper (eg. image_tag)\n\
  consider_all_requests_local\n    All requests are considered local by default (true), so everyone will be exposed to detailed debugging screens on errors.\n    Defaults to true\n\
  debug_routes\n    Enable or disable the collection of failure information for RoutingErrors.\n    Defaults to true.\n\
  allow_concurrency\n    Controls whether the application is thread-safe.\n    Defaults to false.\n\
  param_parsers\n    Lets you register handlers wich will process the http body and add parameters to the @params hash.\n    Defaults to { Mime::XML => :xml_simple }\n\
  template_root\n    Sets the default template location. For example, a call to render(\"test/template\") will be converted to \"#{template_root}/test/template.rhtml\"\n\
  logger\n    Can be set to nil for no logging or a logger conforming to the interface of Log4r or the default Ruby 1.8+ Logger class.\n\
  ignore_missing_templates\n    Turn on ignore_missing_templates if you want to unit test actions without making the associated templates.\n\n\n\
  = ActionView Options =\n\
  Each of these options should be prepended with config.action_view. when used with a Rails::Initializer do |config| block.\n\n\
  cache_template_loading\n    Specify whether file modification times should be checked to see if a template needs recompilation\n\
  cache_template_extensions\n    Specify whether file extension lookup should be cached. Should be false for development environments.\n    Defaults to true.\n\
  local_assigns_support_string_keys\n    Specify whether local_assigns should be able to use string keys.\n    Defaults to true.\n    String keys are deprecated and will be removed shortly.\n\
  debug_rjs\n    Specify whether RJS responses should be wrapped in a try/catch block that alert()s the caught exception (and then re-raises it).\n    Defaults to false.\n\
  logger\n    Can be set to nil for no logging or a logger conforming to the interface of Log4r or the default Ruby 1.8+ Logger class.\n\n\n\
  = ActionMailer Options =\n\
  Each of these options should be prepended with config.action_mailer. when used with a Rails::Initializer do |config| block.\n\n\
  server_settings\n    A hash defining the server to be used for email.\n    Defaults to using a server localy on port 25 as such:\n\n    { :address        => \"localhost\", \n      :port           => 25, \n      :domain         => 'localhost.localdomain', \n      :user_name      => nil, \n      :password       => nil, \n      :authentication => nil }\n\n\
  raise_delivery_errors\n    Defaults to true\n\
  delivery_method\n    Defaults to :smtp\n\
  perform_deliveries\n    Defaults to true\n\
  default_charset\n    Defaults to \"utf-8\"\n\
  default_content_type\n    Defaults to \"text/plain\"\n\
  default_mime_version\n    Defaults to nil\n\
  default_implicit_parts_order\n    Defaults to %w[text/html text/enriched text/plain]"
