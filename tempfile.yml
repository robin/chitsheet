--- 
tempfile: |-
  require 'tempfile'
  
  tf = Tempfile.new 'prefix'
  tf.write File.read("template")
  tf.close
  
  system(ENV['VISUAL'], tf.path)
  
  tf.open
  edited = tf.read
