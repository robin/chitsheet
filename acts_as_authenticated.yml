--- 
acts_as_authenticated: "See: http://technoweenie.stikipad.com/plugins/show/User+Authentication\r\n\
  \r\n\
  Install:\r\n\
  >> ruby script/plugin source http://svn.techno-weenie.net/projects/plugins\r\n\
  >> ruby script/plugin install acts_as_authenticated\r\n\
  \r\n\
  Generate:\r\n\
  >> ruby script/generate authenticated user account\r\n\
  >> rake db:migrate\r\n\
  \r\n\
  To require logins for all actions, use this in your controllers:\r\n  before_filter :login_required\r\n\
  \r\n\
  To require logins for specific actions, use this in your controllers:\r\n  before_filter :login_required, :only => [ :edit, :update ]\r\n\
  \r\n\
  To skip this in a subclassed controller:\r\n  skip_before_filter :login_required\r\n\
  \r\n\
  Here are other available methods for your views and controllers:\r\n    * logged_in? \xE2\x80\x93 Returns true if the user is currently logged in.\r\n    * current_user \xE2\x80\x93 Returns an instance of the currently logged in user.\r\n\
  \r\n\
  You can override the #protect? method in your controller to only protect certain actions:\r\n\
  \r\n  # don't protect the login and the about method\r\n  def protect?(action)\r\n    if ['login', 'about'].include?(action)\r\n       return false\r\n    else\r\n       return true\r\n    end\r\n  end\r\n\
  \r\n\
  You can also override #authorized? in your controller to restrict the actions based on the user:\r\n\
  \r\n  # only allow nonbobs\r\n  def authorized?(user)\r\n    user.login != \"bob\" \r\n  end"
