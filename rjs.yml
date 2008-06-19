--- 
rjs: "<<(javascript)\r\n\
  Writes raw JavaScript to the page.\r\n\
  \r\n\
  [](id)\r\n  Returns a element reference by finding it through id in the DOM. This element can then be used for further method calls. Examples:\r\n    page['blank_slate']                  # => $('blank_slate');\r\n    page['blank_slate'].show             # => $('blank_slate').show();\r\n    page['blank_slate'].show('first').up # => $('blank_slate').show('first').up();\r\n\
  \r\n\
  alert(message)\r\n  Displays an alert dialog with the given message.\r\n\
  \r\n\
  assign(variable, value)\r\n  Assigns the JavaScript variable the given value.\r\n\
  \r\n\
  call(function, *arguments, &block)\r\n  Calls the JavaScript function, optionally with the given arguments.\r\n  If a block is given, the block will be passed to a new JavaScriptGenerator; the resulting JavaScript code will then be wrapped inside function() { \xE2\x80\xA6 } and passed as the called function\xE2\x80\x98s final argument.\r\n\
  \r\n\
  delay(seconds = 1) {|| ...}\r\n  Executes the content of the block after a delay of seconds. Example:\r\n    page.delay(20) do\r\n      page.visual_effect :fade, 'notice'\r\n    end\r\n\
  \r\n\
  draggable(id, options = {})\r\n  Creates a script.aculo.us draggable element. See ActionView::Helpers::ScriptaculousHelper for more information.\r\n\
  \r\n\
  drop_receiving(id, options = {})\r\n  Creates a script.aculo.us drop receiving element. See ActionView::Helpers::ScriptaculousHelper for more information.\r\n\
  \r\n\
  hide(*ids)\r\n  Hides the visible DOM elements with the given ids.\r\n\
  \r\n\
  insert_html(position, id, *options_for_render)\r\n  Inserts HTML at the specified position relative to the DOM element identified by the given id.\r\n  position may be one of:\r\n  :top:\tHTML is inserted inside the element, before the element\xE2\x80\x98s existing content.\r\n  :bottom:\tHTML is inserted inside the element, after the element\xE2\x80\x98s existing content.\r\n  :before:\tHTML is inserted immediately preceeding the element.\r\n  :after:\tHTML is inserted immediately following the element.\r\n  options_for_render may be either a string of HTML to insert, or a hash of options to be passed to ActionView::Base#render. For example:\r\n    # Insert the rendered 'navigation' partial just before the DOM\r\n    # element with ID 'content'.\r\n    insert_html :before, 'content', :partial => 'navigation'\r\n\
  \r\n    # Add a list item to the bottom of the <ul> with ID 'list'.\r\n    insert_html :bottom, 'list', '<li>Last item</li>'\r\n\
  \r\n\
  literal(code)\r\n  Returns an object whose to_json evaluates to code. Use this to pass a literal JavaScript expression as an argument to another JavaScriptGenerator method.\r\n\
  \r\n\
  redirect_to(location)\r\n  Redirects the browser to the given location, in the same form as url_for.\r\n\
  \r\n\
  remove(*ids)\r\n  Removes the DOM elements with the given ids from the page.\r\n\
  \r\n\
  replace(id, *options_for_render)\r\n  Replaces the \"outer HTML\" (i.e., the entire element, not just its contents) of the DOM element with the given id.\r\n  options_for_render may be either a string of HTML to insert, or a hash of options to be passed to ActionView::Base#render. For example:\r\n    # Replace the DOM element having ID 'person-45' with the\r\n    # 'person' partial for the appropriate object.\r\n    replace 'person-45', :partial => 'person', :object => @person\r\n  This allows the same partial that is used for the insert_html to be also used for the input to replace without resorting to the use of wrapper elements.\r\n  Examples:\r\n    <div id=\"people\">\r\n      <%= render :partial => 'person', :collection => @people %>\r\n    </div>\r\n\
  \r\n    # Insert a new person\r\n    page.insert_html :bottom, :partial => 'person', :object => @person\r\n\
  \r\n    # Replace an existing person\r\n    page.replace 'person_45', :partial => 'person', :object => @person\r\n\
  \r\n\
  replace_html(id, *options_for_render)\r\n  Replaces the inner HTML of the DOM element with the given id.\r\n  options_for_render may be either a string of HTML to insert, or a hash of options to be passed to ActionView::Base#render. For example:\r\n    # Replace the HTML of the DOM element having ID 'person-45' with the\r\n    # 'person' partial for the appropriate object.\r\n    replace_html 'person-45', :partial => 'person', :object => @person\r\n\
  \r\n\
  select(pattern)\r\n  Returns a collection reference by finding it through a CSS pattern in the DOM. This collection can then be used for further method calls. Examples:\r\n    page.select('p')                      # => $$('p');\r\n    page.select('p.welcome b').first      # => $$('p.welcome b').first();\r\n    page.select('p.welcome b').first.hide # => $$('p.welcome b').first().hide();\r\n  You can also use prototype enumerations with the collection. Observe:\r\n    page.select('#items li').each do |value|\r\n      value.hide\r\n    end\r\n    # => $$('#items li').each(function(value) { value.hide(); });\r\n  Though you can call the block param anything you want, they are always rendered in the javascript as \xE2\x80\x98value, index.\xE2\x80\x99 Other enumerations, like collect() return the last statement:\r\n    page.select('#items li').collect('hidden') do |item|\r\n      item.hide\r\n    end\r\n    # => var hidden = $$('#items li').collect(function(value, index) { return value.hide(); });\r\n\
  \r\n\
  show(*ids)\r\n  Shows hidden DOM elements with the given ids.\r\n\
  \r\n\
  sortable(id, options = {})\r\n  Creates a script.aculo.us sortable element. Useful to recreate sortable elements after items get added or deleted. See ActionView::Helpers::ScriptaculousHelper for more information.\r\n\
  \r\n\
  toggle(*ids)\r\n  Toggles the visibility of the DOM elements with the given ids.\r\n\
  \r\n\
  visual_effect(name, id = nil, options = {})\r\n  Starts a script.aculo.us visual effect. See ActionView::Helpers::ScriptaculousHelper for more information."
