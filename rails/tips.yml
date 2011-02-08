--- 
rails_tips: |-
  * Store sessions in the database.
  * Use a custom configuration file for passwords and API keys instead of storing them in your Subversion repository. I use YAML and mirror the style of database.yml.
  * Use constants where needed. Instead of repeating strings like the address of your customer service reply email, set it once in a constant (in environment.rb or the appropriate environment file) and use that throughout your application.
  * Keep time in UTC. A no brainer, and easy to do.
  * Don't loop through ActiveRecord models inside other models. Use eager loading if you need to work with multiple associated models. Better yet, write a custom SQL query and let the database do the work for you.
  * Beware of binary fields. By default, all fields are returned with queries, including the full contents of any binary fields. Use :select to pull out only the fields you need.
  * Write tables to cache data for reports that span months and years. It.s much faster than re-generating a year.s worth of reports every time a page is loaded.
  * Create a table with a list of country names. By default, Rails uses strings for selects and lists of countries, which doesn.t work well for reporting or database consistency between models.
  * Avoid bloated controllers. Instead of piling actions into a controller, limit yourself to 10 actions per controller, then rethink your design.
  * Keep your controllers and views skinny. In general, most of your code should be in your models, not your controllers or views.
  * Don't store objects in the session. Use integers or short strings if necessary, then pull the appropriate object out of the database for the duration of a single request.
  * Avoid heavy response processing. Can you mark a record as needing to be processed, then use a cron job or a messaging server to do the long-running work? BackgroundRB is also an option. (I use this technique for filtering SPAM comments on this blog).
  * Use ar_mailer to queue bulk emails instead of sending them during the Rails response cycle.
  * Monitor your servers with the exception_notification plugin, munin, monit, or other tools.
  * Don't cut costs on hardware. You.ll quickly lose the money you thought you were saving if your developers have to spend even one day a month on unexpected server maintenance due to poor backups or cheap hardware.
  * Test-drive your development.
  
  * Use database indexes to speed up queries. Rails only indexes primary keys, so you.ll have to find the spots that need more attention.
  * Profile your code. The ruby-prof gem and plugin helped me make an application three times faster with only minimal changes to the code.
  * Minimize graphic-related dependencies. If your application only needs to make a few thumbnails, don.t waste memory by importing large graphics libraries. Look at mini-magick or image_science for lightweight thumbnailing.
  * Avoid excessive repeated rendering of small partials.
  * Use CSS instead of inline tags to apply selective styling.
  * Don't use ActiveRecord.s serialize option to store large objects in database fields.
  * Use attr_protected :fieldname in models to keep database fields from being manipulated from forms (or from any calls to Model.update_attributes(params[:model])).
  * Use Ruby classes and inheritance to refactor repeated controller code.
  * Use unobtrusive Javascripting techniques to separate behavior from markup.
  * Package self-sufficient classes and modules as plugins or RubyGems.
  * Cache frequently accessed data and rendered content where possible.
  * Write custom Test::Unit assertions or rSpec matchers to help with debugging test suite errors.
  * Rotate the Rails and Mongrel logfiles using the logrotate daemon on Linux.
  * Build a reliable backup system.
  * Automate deployment and maintenance with Capistrano or Vlad.
  * Keep method bodies short. If a method is more than 10 lines long, it.s time to break it down and refactor.
  * Run flog to determine overly complex methods and clases.
  * Don't use too many conditionals. Take advantage of case statements and Ruby objects to filter instead of multiply-nested if statements.
  * Don't be too clever. Ruby has great metaprogramming features, but they are easy to overuse (such as eval and method_missing).
  * Become familiar with the most popular plugins. Instead of re-implementing the wheel, save yourself some time by using well tested, popular plugins.
