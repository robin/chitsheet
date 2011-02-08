--- 
hpricot: |-
  Element#css_path
  
   doc.at("div > div:nth(1)").css_path
     #=> "div > div:nth(1)" 
   doc.at("#header").css_path
     #=> "#header" 
  
  Element#xpath
  
   doc.at("div > div:nth(1)").xpath
     #=> "/div/div:eq(1)" 
   doc.at("#header").xpath
     #=> "//div[@id='header']" 
  
  Element#swap
  
   doc = Hpricot("That's my <b>spoon</b>, Tyler.")
   doc.at("b").swap("<i>fork</i>")
   doc.to_html
     #=> "That's my <i>fork</i>, Tyler." 
  
  Element#next_sibling, Element#previous_sibling
  
   (doc/:h3).each do |h3|
     while ele = h3.next_sibling
       ary << ele   # stuff away all the elements under the h3
     end
   end
  
  ###########################################
  
  elements = doc.search("a")
  elements = doc.search("a.class")
  elements = doc.search("a#ID")
  elements = doc.search("body > table > a")
  elements = doc.search("a[@href='http://hoodwink.d/']")
  element  = doc.at("a#ID") == doc.search("a#ID").first
  attribute = doc.at("body")['onload'] == doc.at("body")[:onload]
  elements = doc.search("table > a#ID") == (doc/"table > a#ID") == (doc/"table/a#ID") == (doc/:table/:a#ID)
