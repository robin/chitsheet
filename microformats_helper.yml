--- 
microformats_helper: |-
  hAtom
  
  <% render_hfeed(options?) do ... end %>
  <% render_hentry(id, options?) do ... end %>
  
    Render ol with class hfeed, or li with the class hentry and id. Options passed to HTML element.
  
  <%= hentry_title(title?, options?) { ... } %>
  <%= hentry_content(content?, options?) { ... } %>
  
    Returns header with class entry-title, or element with class entry-content. Content pass as argument or returned from block, options passed to wrapping element. Use :level to specify header level (default 2), :tag to specify content element (default p).
  
  Other
  
  <%= hcard(values) %>
  
    :fn           Formal name
    :given-name   Given name (alternative to :fn)
    :family-name  Family name (alternative to :fn)
    :url          URL of person/entity (results in link)
    :photo        URL of photo, or hash of options for img tag
    :html         Options to pass to wrapper element
  
  <%= Time.microformat(type, format?) { ... } %>
  
    Formats time using the date/time pattern, returns abbr element. First argument is date/time type (e.g. :published). Human formatted: using second argument (see strftime), result of block, or self.to_s.
