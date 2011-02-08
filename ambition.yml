--- 
ambition: |-
  Query#to_sql
  >> User.select { |m| m.name == 'jon' }.to_sql
  => "SELECT * FROM users WHERE users.name = 'jon'"
  
  Query#to_hash
  >> User.select { |m| m.name == 'jon' }.to_hash
  => {:conditions=>"users.name = 'jon'"}
  
  Equality
  
  User.select { |m| m.name == 'jon' }
  User.select { |m| m.name != 'jon' }
  User.select { |m| m.name == 'jon' && m.age == 21 }
  User.select { |m| (m.name == 'jon' || m.name == 'rick') && m.age == 21 }
  
  Associations
  
  User.select { |u| u.email == 'chris@ozmm.org' && u.profile.name == 'chris wanstrath' }.map(&:title)
  
  Comparisons
  
  User.select { |m| m.age < 21 }.to_sql
  User.select { |m| [1, 2, 3, 4].include? m.id }
  
  LIKE and REGEXP
  
  User.select { |m| m.name =~ 'chri%' }
  User.select { |m| m.name !~ 'chris' }
  User.select { |m| !(m.name =~ 'chris') }
  User.select { |m| m.name =~ /chris/ }
  
  Detect
  
  User.detect { |m| m.name == 'chris' }
  
  Limits
  
  User.select { |m| m.name == 'jon' }.first
  User.select { |m| m.name == 'jon' }.first(5)
  User.select { |m| m.name == 'jon' }[10, 20]
  User.select { |m| m.name == 'jon' }[10..20]
  
  Sort
  
  User.select { |m| m.name == 'jon' }.sort_by { |m| m.name }
  User.select { |m| m.name == 'jon' }.sort_by { |m| [ m.name,  -m.age ] }
  User.select { |m| m.name == 'jon' }.sort_by { |m| -m.profiles.title }
  User.select { |m| m.name == 'jon' }.sort_by { rand }
  
  Count
  
  User.select { |m| m.name == 'jon' }.size
  
  Other
  
  
  User.any? { |m| m.name == 'jon' }
  User.all? { |m| m.name == 'jon' }
  User.select { |m| m.name == 'jon' }.empty?
  User.select { |m| m.name.downcase =~ 'jon%' }.to_sql
