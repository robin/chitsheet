--- 
prototype: "Utility Methods:\r\n\
  \r\n\
  $(id | element) -> HTMLElement\r\n\
  $((id | element)...) -> [HTMLElement...]\r\n\
  If provided with a string, returns the element in the document with matching ID; otherwise returns the passed element. Takes in an arbitrary number of arguments. All elements returned by the function are extended with Prototype DOM extensions.\r\n\
  \r\n\
  $$(cssRule...) -> [HTMLElement...]\r\n\
  Takes an arbitrary number of CSS selectors (strings) and returns a document-order array of extended DOM elements that match any of them.\r\n\
  \r\n\
  $A(iterable) -> actualArray\r\n\
  Accepts an array-like collection (anything with numeric indices) and returns its equivalent as an actual Array object. This method is a convenience alias of Array.from, but is the preferred way of casting to an Array.\r\n\
  \r\n\
  $F(element) -> value\r\n\
  Returns the value of a form control. This is a convenience alias of Form.Element.getValue. Refer to it for full details.\r\n\
  \r\n\
  $H([obj]) -> Hash\r\n\
  Creates a Hash (which is synonymous to \xE2\x80\x9Cmap\xE2\x80\x9D or \xE2\x80\x9Cassociative array\xE2\x80\x9D for our purposes). A convenience wrapper around the Hash constructor, with a safeguard that lets you pass an existing Hash object and get it back untouched (instead of uselessly cloning it).\r\n\
  \r\n\
  $R(start, end[, exclusive = false]) -> ObjectRange\r\n\
  Creates a new ObjectRange object. This method is a convenience wrapper around the ObjectRange constructor, but $R is the preferred alias.\r\n\
  \r\n\
  $w(String) -> Array\r\n\
  Splits a string into an Array, treating all whitespace as delimiters. Equivalent to Ruby's %w{foo bar} or Perl's qw(foo bar).\r\n\
  \r\n\
  \r\n\
  \r\n\
  Element\r\n\
  \r\n\
  new Element(tagName[, attributes])\r\n\
  var a = new Element('a', { 'class': 'foo', href: '/foo.html' }).update(\"Next page\");\r\n\
  Constructor creates new element.\r\n\
  \r\n\
  absolutize(element) -> HTMLElement\r\n\
  Turns element into an absolutely-positioned element without changing its position in the page layout.\r\n\
  \r\n\
  addClassName(element, className) -> HTMLElement \r\n\
  Adds a CSS class to element.\r\n\
  \r\n\
  addMethods([methods])\r\n\
  addMethods(tagName, methods)\r\n\
  Takes a hash of methods and makes them available as methods of extended elements and of the Element object. The second usage form is for targeting a specific HTML element.\r\n\
  \r\n\
  Element.adjacent(element[, selectors...]) -> [HTMLElement...]\r\n\
  someElement.adjacent([selectors...]) -> [HTMLElement...]\r\n\
  Finds all siblings of the current element that match the given selector(s).\r\n\
  \r\n\
  ancestors(element) -> [HTMLElement...]\r\n\
  Collects all of element\xE2\x80\x99s ancestors and returns them as an array of extended elements.\r\n\
  \r\n\
  childElements(element) -> [HTMLElement...]\r\n\
  Collects all of the element's children and returns them as an array of extended elements.\r\n\
  \r\n\
  cleanWhitespace(element) -> HTMLElement\r\n\
  Removes all of element's text nodes which contain only whitespace. Returns element.\r\n\
  \r\n\
  clonePosition(element, source[, options]) -> HTMLElement\r\n\
  Clones the position and/or dimensions of source onto element as defined by the optional argument options.\r\n\
  \r\n\
  cumulativeOffset(element) -> [Number, Number] also accessible as { left: Number, top: Number }\r\n\
  Returns the offsets of element from the top left corner of the document.\r\n\
  \r\n\
  cumulativeScrollOffset(element) -> [Number, Number] also accessible as { left: Number, top: Number }\r\n\
  Calculates the cumulative scroll offset of an element in nested scrolling containers.\r\n\
  \r\n\
  descendantOf(element, ancestor) -> Boolean \r\n\
  Checks if element is a descendant of ancestor.\r\n\
  \r\n\
  descendants(element) -> [HTMLElement...]\r\n\
  Collects all of element\xE2\x80\x99s descendants and returns them as an array of extended elements.\r\n\
  \r\n\
  down(element[, cssRule][, index = 0]) -> HTMLElement | undefined\r\n\
  Returns element\xE2\x80\x99s first descendant (or the n-th descendant if index is specified) that matches cssRule. If no cssRule is provided, all descendants are considered. If no descendant matches these criteria, undefined is returned.\r\n\
  \r\n\
  empty(element) -> Boolean\r\n\
  Tests whether element is empty (i.e. contains only whitespace).\r\n\
  \r\n\
  extend(element)\r\n\
  Extends element with all of the methods contained in Element.Methods and Element.Methods.Simulated. If element is an input, textarea or select tag, it will also be extended with the methods from Form.Element.Methods. If it is a form tag, it will also be extended with Form.Methods.\r\n\
  \r\n\
  fire(eventName[, memo]) -> Event\r\n\
  Fires a custom event with the current element as its target.\r\n\
  \r\n\
  firstDescendant(element) -> HTMLElement\r\n\
  Returns the first child that is an element. This is opposed to firstChild DOM property which will return any node (whitespace in most usual cases).\r\n\
  \r\n\
  getDimensions(element) -> {height: Number, width: Number}\r\n\
  Finds the computed width and height of element and returns them as key/value pairs of an object.\r\n\
  \r\n\
  getHeight(element) -> Number\r\n\
  Finds and returns the computed height of element.\r\n\
  \r\n\
  getOffsetParent(element) -> HTMLElement\r\n\
  Returns element\xE2\x80\x99s closest positioned ancestor. If none is found, the body element is returned.\r\n\
  \r\n\
  getStyle(element, property) -> String | null\r\n\
  Returns the given CSS property value of element. property can be specified in either of its CSS or camelized form.\r\n\
  \r\n\
  getWidth(element) -> Number\r\n\
  Finds and returns the computed width of element.\r\n\
  \r\n\
  hasClassName(element, className) -> Boolean\r\n\
  Checks whether element has the given CSS className.\r\n\
  \r\n\
  hide(element) -> HTMLElement\r\n\
  Hides and returns element.\r\n\
  \r\n\
  identify(element) -> id\r\n\
  returns element\xE2\x80\x99s id attribute if it exists, or sets and returns a unique, auto-generated id.\r\n\
  \r\n\
  insert(element, { position: content }) -> HTMLElement\r\n\
  insert(element, content) -> HTMLElement\r\n\
  Inserts content before, after, at the top of, or at the bottom of element, as specified by the position property of the second argument. If the second argument is the content itself, insert will append it to element.\r\n\
  inspect\r\n\
  \r\n\
  inspect(element) -> String\r\n\
  Returns the debug-oriented string representation of element.\r\n\
  \r\n\
  makeClipping(element) -> HTMLElement\r\n\
  Simulates the poorly supported CSS clip property by setting element's overflow value to 'hidden'. Returns element.\r\n\
  \r\n\
  makePositioned(element) -> HTMLElement\r\n\
  Allows for the easy creation of CSS containing block by setting element's CSS position to 'relative' if its initial position is either 'static' or undefined. Returns element.\r\n\
  \r\n\
  match(element, selector) -> Boolean\r\n\
  Checks if element matches the given CSS selector.\r\n\
  \r\n\
  next(element[, cssRule][, index = 0]) -> HTMLElement | undefined\r\n\
  Returns element\xE2\x80\x99s following sibling (or the index\xE2\x80\x99th one, if index is specified) that matches cssRule. If no cssRule is provided, all following siblings are considered. If no following sibling matches these criteria, undefined is returned.\r\n\
  \r\n\
  nextSiblings(element) -> [HTMLElement...]\r\n\
  Collects all of element\xE2\x80\x99s next siblings and returns them as an array of extended elements.\r\n\
  \r\n\
  Element.observe(element, eventName, handler) -> HTMLElement\r\n\
  someElement.observe(eventName, handler) -> HTMLElement\r\n\
  Registers an event handler on element and returns element.\r\n\
  \r\n\
  positionedOffset(element) -> [Number, Number] also accessible as { left: Number, top: Number }\r\n\
  Returns element\xE2\x80\x99s offset relative to its closest positioned ancestor (the element that would be returned by Element#getOffsetParent).\r\n\
  \r\n\
  previous(element[, cssRule][, index = 0]) -> HTMLElement | undefined\r\n\
  Returns element's previous sibling (or the index'th one, if index is specified) that matches cssRule. If no cssRule is provided, all previous siblings are considered. If no previous sibling matches these criteria, undefined is returned.\r\n\
  \r\n\
  previousSiblings(element) -> [HTMLElement...]\r\n\
  Collects all of element\xE2\x80\x99s previous siblings and returns them as an array of extended elements.\r\n\
  \r\n\
  readAttribute(element, attribute) -> String | null\r\n\
  Returns the value of element's attribute or null if attribute has not been specified.\r\n\
  \r\n\
  recursivelyCollect(element, property) -> [HTMLElement...]\r\n\
  Recursively collects elements whose relationship is specified by property. property has to be a property (a method won\xE2\x80\x99t do!) of element that points to a single DOM node. Returns an array of extended elements.\r\n\
  \r\n\
  relativize(element) -> HTMLElement\r\n\
  Turns element into an relatively-positioned element without changing its position in the page layout.\r\n\
  \r\n\
  remove(element) -> HTMLElement\r\n\
  Completely removes element from the document and returns it.\r\n\
  \r\n\
  removeClassName(element, className) -> HTMLElement\r\n\
  Removes element\xE2\x80\x99s CSS className and returns element.\r\n\
  \r\n\
  replace(element[, html]) -> HTMLElement\r\n\
  Replaces element by the content of the html argument and returns the removed element.\r\n\
  \r\n\
  scrollTo(element) -> HTMLElement\r\n\
  Scrolls the window so that element appears at the top of the viewport. Returns element.\r\n\
  \r\n\
  select(element, selector...) -> [HTMLElement...]\r\n\
  Takes an arbitrary number of CSS selectors (strings) and returns an array of extended descendants of element that match any of them.\r\n\
  \r\n\
  Element.setOpacity(element, opacity) -> [HTMLElement...]\r\n\
  someElement.setOpacity(opacity) -> [HTMLElement...]\r\n\
  Sets the visual opacity of an element while working around inconsistencies in various browsers. The opacity argument should be a floating point number, where the value of 0 is fully transparent and 1 is fully opaque.\r\n\
  \r\n\
  setStyle(element, styles) -> HTMLElement\r\n\
  Modifies element\xE2\x80\x99s CSS style properties. Styles are passed as a hash of property-value pairs in which the properties are specified in their camelized form.\r\n\
  \r\n\
  show(element) -> HTMLElement\r\n\
  Displays and returns element.\r\n\
  \r\n\
  siblings(element) -> [HTMLElement...]\r\n\
  Collects all of element\xE2\x80\x99s siblings and returns them as an array of extended elements.\r\n\
  \r\n\
  stopObserving(element, eventName, handler) -> HTMLElement\r\n\
  Unregisters handler and returns element.\r\n\
  \r\n\
  toggle(element) -> HTMLElement\r\n\
  Toggles the visibility of element.\r\n\
  \r\n\
  toggleClassName(element, className) -> HTMLElement\r\n\
  Toggles element\xE2\x80\x99s CSS className and returns element.\r\n\
  \r\n\
  undoClipping(element) -> HTMLElement\r\n\
  Sets element\xE2\x80\x99s CSS overflow property back to the value it had before Element.makeClipping() was applied. Returns element.\r\n\
  \r\n\
  undoPositioned(element) -> HTMLElement\r\n\
  Sets element back to the state it was before Element.makePositioned was applied to it. Returns element.\r\n\
  \r\n\
  up(element, [cssRule][, index = 0]) -> HTMLElement | undefined\r\n\
  Returns element\xE2\x80\x99s first ancestor (or the index\xE2\x80\x99th ancestor, if index is specified) that matches cssRule. If no cssRule is provided, all ancestors are considered. If no ancestor matches these criteria, undefined is returned.\r\n\
  \r\n\
  update(element[, newContent]) -> HTMLElement\r\n\
  Replaces the content of element with the provided newContent argument and returns element.\r\n\
  \r\n\
  viewportOffset(element) -> [Number, Number] also accessible as { left: Number, top: Number }\r\n\
  Returns the X/Y coordinates of element relative to the viewport.\r\n\
  \r\n\
  visible(element) -> Boolean\r\n\
  Returns a Boolean indicating whether or not element is visible (i.e. whether its inline style property is set to \"display: none;\").\r\n\
  \r\n\
  Element.wrap(element, wrapper[, attributes]) -> HTMLElement\r\n\
  someElement.wrap(wrapper[, attributes]) -> HTMLElement\r\n\
  Wraps an element inside another, then returns the wrapper.\r\n\
  \r\n\
  writeAttribute(element, attribute[, value = true]) -> HTMLElement\r\n\
  writeAttribute(element, attributes) -> HTMLElement\r\n\
  Adds, specifies or removes attributes passed as either a hash or a name/value pair.\r\n\
  \r\n\
  \r\n \t \r\n\
  Form Functions\t \r\n\
  \r\n\
  $F(fieldname);\r\n  Return the value of the form element, whether it is a text input, textarea, select box or checkbox. If it is a checkbox, it will return undefined if unchecked. Radio groups dont work.\r\n\
  Form.getElements(formID);\r\n  Returns an array of all the form elements for form formID\r\n\
  Form.serialize(formID);\r\n  Returns a formatted URL containing all the elements in the form, similar to &field=value&field2=othervalue\r\n\
  Form.focusFirstElement(formID);\t\r\n  Will set focus on the first form element.\r\n\
  \r\n \t \r\n\
  Exception Handling\t \r\n\
  \r\n\
  Try.these(\r\n       function(){  \r\n            // errors \r\n       }, \r\n       function(){\r\n            // other stuff\r\n       }\r\n\
  );\r\n  Allows you to execute the second function if the first one fails. \r\n  Kinda like try/catch, except it doesn't make any sense.\r\n\
  \r\n                       \t \r\n\
  Ajax\r\n\
  \r\n\
  function ajaxMe( theUrl, data ){\r\n   var ajaxRequest = new Ajax.Request(\r\n     theUrl,{method: post, parameters: data, onComplete: theResponse});\r\n\
  }\r\n\
  \r\n\
  function theResponse(origRequest){\r\n    alert(origRequest.responseText);\r\n\
  }\r\n\
  \r\n\
  Classes\r\n\
  \r\n\
  var Butter = Class.create({\r\n  initialize: function(brand) {\r\n    this.brand = brand;\r\n    this.melted = false;\r\n  },\r\n  melt: function() {\r\n    this.melted = true;\r\n  }\r\n\
  })\r\n\
  var parkay = new Butter('Parkay');\r\n\
  \r\n  Prototype gives you a way to create classes. If you want, you\r\n  can define an initialize function that will be called when\r\n  instances of the class are created."
