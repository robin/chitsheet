--- 
rdoc: |-
  rdoc:
  
  Normal Paragraph text
    def indented_text()
      # is treated as code -- not reformatted
    end
  
  Lists:
    * This is a list element
    - This is one too.
    1. This one will be numbered
    [label] item description,
            can be continued at same
            indent level
    label::
      or start the description on the following line
      and continue at the same indent level
  
  ----------------------------------------------------------------------
  Three or more hyphens make a horizontal rule on the page
  
  Styling:
    = Level One Heading
    == Level Two Heading
    _italic_::                  _word_ or <em>text</em>
    *bold*::                    *word* or <b>text</b>
    +typewriter+::              +word+ or <tt>text</tt>
  
  Auto hyperlinked:
   MyClass
   my_class.rb
   def my_method; end;
   #my_method
   http:, mailto:, ftp:, www.
   link: (to local filesystem relative to --op)
   (urls to images are rendered as inline image tags)
   label[url] (uses label as hyperlink text)
   {multi word label}[url] (uses label as hyperlink text)
  
  Ruby:
  
    ClassNames, source_files.rb and either method_name_having_an_underscore
    or #methodnamewithhash are hyperlinked to their documentation.
  
    :title:The title for the document.
  
    # documenting this function
    #--
    # this will not appear in the docs (shhh....)
    #++
    # this will appear (hi!)
    def foo() # :nodoc:
      # this function won't appear in the docs
    end
