--- 
rubyio: |-
  ruby: send('method', arg)
    io: perform("slot", arg)
  
  ruby: respond_to? 'method'
    io: hasSlot("slot")
  
  ruby: object.something if object.respond_to? :something
    io: object ?something
  
  ruby: methods
    io: slotNames
  
  ruby: method_missing
    io: forward
  
  ruby: inspect
    io: slotSummary
  
  ruby: puts method(:blah).to_ruby
    io: getSlot("blah") code print
  
  ruby: extend Module
    io: appendProto(Module clone)
  
  ruby: require 'file'
    io: doFile('file.io')
  
  ruby: dudes.map { |dude| dude.name }
    io: dudes map(dude, dude name)
  
  ruby: dudes.map(&:name)
    io: dudes map(name)
  
  ruby: longest = tasks.map { |task| task.name.size }.max 
    io: longest := tasks map(name size) max
  
  ruby: dudes.each { |dude| puts " #{dude.name}" }
    io: dudes foreach(dude, writeln(" ", dude name))
  
  ruby: dudes.each_with_index { |dude,i| puts " #{dude.name}" }
    io: dudes foreach(i, dude, writeln(" ", dude name))
  
  ruby: dudes.select { |dude| dude.age < 32 }
    io: dudes select(dude, dude age < 32)        
  
  ruby: dudes.select { |dude| dude.age < 32 }
    io: dudes select(age < 32)
