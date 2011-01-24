--- 
watir_ie: |-
  Watir
  *Load the Watir library
    require 'watir'
  
  *Open Internet Explorer at the specified URL
    $browser = Watir::IE.start("http://google.com")
    $browser = Watir::IE.start "http://google.com"
  
  *Attach to an existing browser, raising an exception if it isn't found
    $browser = Watir::IE.attach(:url, "http://www.google.com")
    $browser = Watir::IE.attach(:title, "Google")
  
  *Attach to an existing browser, returning nil if it isn't found
    $browser = Watir::IE.find(:title, "Google") 
    $browser = Watir::IE.find(:url, "http://www.google.com")
  
  *Speed up execution (or use the "-b" command line switch)
    $browser.speed = :fast
  
  *Close the browser
    $browser.close
  
  *Access an Element
    Text box or text area
      t = $browser.text_field(:name, "username")
    Button
      b = $browser.button(:value, "Click Here")
    Drop down list
      d = $browser.select_list(:name, "month")
    Check box
      c = $browser.checkbox(:name, "enabled")
    Radio button
      r = $browser.radio(:name, "payment type")
    Form
      f = $browser.form(:name, "address")
      f = $browser.form(:action, "submit")
    Link
      l = $browser.link(:url, "http://google.com")
    Table cell in a table (2nd row, 1st column)
      td = $browser.table(:name, 'recent_records')[2][1]
  	
  *Manipulate the Element
    Click a button or link
  	b.click
  	l.click
    Enter text in a text box
  	t.set("mickey mouse")
  	t.set "mickey mouse"
    Enter multiple lines in a multi-line text box
      t.set("line 1\nline2")
      t.set "line 1\nline2"
    Set radio button or check box
      c.set
      r.set
    Clear an element
      t.clear
  	c.clear
  	r.clear
    Select an option in a drop down list
  	d.select("Hey!")
  	d.select "Hey!"
    Clear a drop down list
      d.clearSelection
    Submit a form
      f.submit
    Flash any element (useful from the watir-console)
      e.flash
  
  *Check the Contents
    Return the html of the page or any element
  	$browser.html
  	e.html
    Return the text of the page or any element
  	$browser.text
  	e.text
    Return the title of the document
  	$browser.title
    Return true if the specified text appears on the page
  	$browser.text.include? 'llama'
    Return the contents of a table as an array
      $browser.table(:id, 'recent_records').to_a
