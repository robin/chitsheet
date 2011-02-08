--- 
shoes: |-
  ## 
  # General Stuff
  stack do  # fills width 100%
    contents
  end
  
  stack :width => x, :margin-left => x do
    contents
  end
  
  button "label" do
    event
  end
  
  alert 'string'
  text 'string'
  background rgb(1, 1, 1), :top => 50, :right => 0, :width => 55
  image 'static/blah.png', :top => 0, :left => 0 # also jpegs and gifs
  
  keypress do |k|
    # keys may be strings or symbols
  end
  
  
  ##
  # Colors
   rgb(1.0, 1.0, 1.0)     # white
   rgb(0xFF, 0xFF, 0xFF)  # white
   rgb(255, 255, 255)     # white
   gray(1.0)              # white
   gray(0xFF)             # white
   gray(255)              # white
   Color.parse("#FFFFFF") # white
   Color.parse("#FFF")    # white
   Color.parse("rgb(255, 255, 255)")
  
   rgb(0.1, 0.1, 0.7)     # blue
   rgb(0.1, 0.7, 0.2, 0.5) # green (50% transparent)
   gray(255, 0.5)         # white (50% transparent)
  
  The color can be passed into `background`, `fill` and `stroke`.
  
  
  ##
  # Controls
  
  # dropdown with One and Two as options
  list = list_box :items => %w(One Two) 
  
  # text field
  text = edit_line
  
  # text box
  body = edit_box 
  body.text = 'default value'
  
  Shoes.p box.text # print to debug value of text box
  
  # other controls: progress
  
  
  ##
  # API Extracted from ruby.c [ http://pastie.caboo.se/90140 ]
  cAnim
    remove
  cBackground
    remove
  cButton
    remove
  cCanvas
    after
    animate
    append
    arrow
    background
    before
    button
    clear
    click
    clipboard
    clipboard=
    contents
    curve_to
    edit_box
    edit_line
    fill
    flow
    goto
    gray
    height
    hide
    image
    imagesize
    keypress
    line
    line_to
    list_box
    motion
    mouse
    move_to
    nofill
    nostroke
    oval
    path
    pop
    prepend
    progress
    push
    quit
    rect
    release
    remove
    reset
    rgb
    rotate
    scale
    show
    skew
    stack
    star
    stroke
    strokewidth
    text
    toggle
    transform
    translate
    width
  cColor
    to_s
  cEditBox
    remove
    text
    text=
  cEditLine
    remove
    text
    text=
  cImage
    remove
  cListBox
    remove
    text
  cPath
    move
    remove
  cProgress
    remove
  cTextClass
    cursor
    cursor=
    remove
    replace
    to_s
  rb_mKernel
    alert
    ask
    ask_color
    ask_open_file
    ask_save_file
    confirm
