--- 
radrails_ruby: |-
  -- RadRails Ruby Cheat Sheet -- 
  all
  all? { |${e}| ${cursor} }
  
  am
  alias_method :${new_name}, :${old_name}
  
  any
  any? { |${e}| ${cursor} }
  
  app
  if __FILE__ == $$PROGRAM_NAME
  	${cursor}
  end
  
  Array
  Array.new(${10}) { |${i}|${cursor} }
  
  art
  assert_redirected_to :action => "${index}"
  
  as
  assert(${test}, "${message}")
  
  asa
  assert(${var} = assigns(:${var}), "@${var} should be defined")
  
  ase
  assert_equal(${expected}, ${actual})
  
  asid
  assert_in_delta(${expected_float}, ${actual_float}, ${20})
  
  asio
  assert_instance_of(${ExpectedClass}, ${actual_instance})
  
  asko
  assert_kind_of(${ExpectedKind}, ${actual_instance})
  
  asm
  assert_match(/${expected_pattern}/, ${actual_string})
  
  asn
  assert_nil(${instance})
  
  asne
  assert_not_equal(${unexpected}, ${actual})
  
  asnm
  assert_no_match(/${unexpected_pattern}/, ${actual_string})
  
  asnn
  assert_not_nil(${instance})
  
  asnnv
  assert_not_nil(${var} = assigns(:${var}))
  
  asnr
  assert_nothing_raised(${Exception}) { ${cursor} }
  
  asns
  assert_not_same(${unexpected}, ${actual})
  
  asnt
  assert_nothing_thrown { ${cursor} }
  
  aso
  assert_operator(${left}, :${operator}, ${right})
  
  asr
  assert_raise(${Exception}) { ${cursor} }
  
  asrdt
  assert_redirected_to(${path}, '${message}')
  
  asre
  assert_response :${success}
  
  asrt
  assert_respond_to(${object}, :${method})
  
  ass
  assert_same(${expected}, ${actual})
  
  ass
  assert_send([${object}, :${message}, ${args}])
  
  ast
  assert_throws(:${expected}) { ${cursor} }
  
  b
  =begin rdoc
  	${cursor}
  =end
  
  begin
  begin
  	${paste}
  rescue ${Exception} => ${e}
  	${cursor}
  end
  
  
  bm
  TESTS = ${10_000}
  Benchmark.bmbm(${10}) do |results|
    ${cursor}
  end
  
  bt
  belongs_to :${object}
  
  btf
  belongs_to :${object}, :class_name => '${class_name}', :foreign_key => :${foreign_key}
  
  case
  case ${object}
  when ${condition}
  	${cursor}
  end
  
  cl
  classify { |${e}| ${cursor} }
  
  cla
  class ${ClassName} < DelegateClass(${ParentClass})
  	def initialize${1}
  		super(${del_obj})
  		
  		${cursor}
  	end
  	
  	
  end
  
  cla
  class ${ClassName} < ${ParentClass}
  	def initialize${1}
  		${cursor}
  	end
  	
  	
  end
  
  cla
  class ${ClassName} < Struct.new(:${attr_names})
  	def initialize(*args)
  		super
  		
  		${cursor}
  	end
  	
  	
  end
  
  cla
  class ${ClassName}
  	${cursor}
  end
  
  cla
  class ${ClassName}
  	def initialize${1}
  		${cursor}
  	end
  	
  	
  end
  
  cla
  class << ${self}
  	${cursor}
  end
  
  cla
  class ${BlankSlate}
  	instance_methods.each { |meth| undef_method(meth) unless meth =~ /\A__/ }
  	
  	def initialize${var}
  		@${delegate} = ${delegate_object}
  		
  		${cursor}
  	end
  	
  	def method_missing(meth, *args, &block)
  		@${delegate}.send(meth, *args, &block)
  	end
  	
  	
  end
  
  clafn
  split("::").inject(Object) { |par, const| par.const_get(const) }
  
  class
  class ${ClassName}
  	${cursor}
  end
  
  col
  collect { |${e}| ${cursor} }
  
  collect
  collect { |${element}| ${element}.${cursor} }
  
  Comp
  include Comparable
  
  def <=>(other)
  	${cursor}
  end
  
  dee
  Marshal.load(Marshal.dump(${obj_to_copy}))
  
  def
  def ${method_name}
  	${cursor}
  end
  
  defd
  def_delegator :${del_obj}, :${del_meth}, :${new_name}
  
  defds
  def_delegators :${del_obj}, :${del_methods}
  
  deff
  def ${method_name}
  	${cursor}
  end
  
  defs
  def self.${class_method_name}
  	${cursor}
  end
  
  deft
  def test_${case_name}
  	${cursor}
  end
  
  deli
  delete_if { |${e}| ${cursor} }
  
  det
  detect { |${e}| ${cursor} }
  
  Dir
  Dir.glob(${glob}) { |${file}| ${cursor} }
  
  do
  do
  	${cursor}
  end
  
  doo
  do |${object}|
  	${cursor}
  end
  
  dow
  downto(${0}) { |${n}|${cursor} }
  
  ea
  each { |${e}| ${cursor} }
  
  eab
  each_byte { |${byte}| ${cursor} }
  
  eac
  each_char { |${chr}| ${cursor} }
  
  eac
  each_cons(${2}) { |${group}| ${cursor} }
  
  each
  each { |${element}| ${element}.${cursor} }
  
  each_with_index
  each_with_index { |${element}, ${idx}| ${element}.${cursor} }
  
  eai
  each_index { |${i}| ${cursor} }
  
  eak
  each_key { |${key}| ${cursor} }
  
  eal
  each_line${1} { |${line}| ${cursor} }
  
  eap
  each_pair { |${name}, ${val}| ${cursor} }
  
  eas
  each_slice(${2}) { |${group}| ${cursor} }
  
  eav
  each_value { |${val}| ${cursor} }
  
  eawi
  each_with_index { |${e}, ${i}| ${cursor} }
  
  elsif
  elsif ${condition}
  	${cursor}
  
  Enum
  include Enumerable
  
  def each(&block)
  	${cursor}
  end
  
  fet
  fetch(${name}) { |${key}|${cursor} }
  
  fil
  fill(${range}) { |${i}|${cursor} }
  
  File
  File.foreach(${file}) { |${line}| ${cursor} }
  
  fin
  find { |${e}| ${cursor} }
  
  fina
  find_all { |${e}| ${cursor} }
  
  fl
  flunk("${message}")
  
  flao
  inject(Array.new) { |${arr}, ${a}| ${arr}.push(*${a}) }
  
  flash
  flash[:${notice}] = "${Successfully}"${cursor}
  
  forin
  for ${element} in ${collection}
  	${element}.${cursor}
  end
  
  Forw
  extend Forwardable
  
  gre
  grep(${pattern}) { |${match}| ${cursor} }
  
  gsu
  gsub(/${pattern}/) { |${match}|${cursor} }
  
  habtm
  has_and_belongs_to_many :${object}
  
  Hash
  Hash.new { |${hash}, ${key}| ${hash}[${key}] = ${cursor} }
  
  hm
  has_many :${models}
  
  hmf
  has_many :${models}, :class_name => '${class_name}', :foreign_key => :${foreign_key}
  
  hmt
  has_many :${models}, :through => :${join_models}
  
  ho
  has_one :${model}
  
  hof
  has_one :${model}, :class_name => '${class_name}', :foreign_key => :${foreign_key}
  
  hp
  :${key} => ${value}
  
  if
  if ${condition}
  	${cursor}
  end
  
  ife
  if ${condition}
  	${2}
  else
  	${3}
  end
  
  inj
  inject(${init}) { |${mem}, ${var}| ${cursor} }
  
  inject
  inject(${object}) { |${injection}, ${element}| ${4} }${cursor}
  
  lam
  lambda { |${args}|${cursor} }
  
  log
  logger.debug "${message}"${cursor}
  
  loge
  logger.error "${message}"${cursor}
  
  logf
  logger.fatal "${message}"${cursor}
  
  logi
  logger.info "${message}"${cursor}
  
  logw
  logger.warn "${message}"${cursor}
  
  mac
  add_column :${table}, :${column}, :${string}
  
  map
  map { |${e}| ${cursor} }
  
  mapwi
  enum_with_index.map { |${e}, ${i}| ${cursor} }
  
  max
  max { |a, b| ${cursor} }
  
  mcc
  t.column :${title}, :${string}${cursor}
  
  mccc
  t.column :${title}, :${string}
  mccc${cursor}
  
  mct
  create_table :${table} do |t|
      ${cursor}
  end
  
  Md
  File.open(${dump}, "w") { |${file}| Marshal.dump(${obj}, ${file}) }
  
  mdt
  drop_table :${table}
  ${cursor}
  
  min
  min { |a, b| ${cursor} }
  
  Ml
  File.open(${dump}) { |${file}| Marshal.load(${file}) }
  
  mm
  def method_missing(meth, *args, &block)
  	${cursor}
  end
  
  mnc
  rename_column :${column}, :${new_column}
  
  mnt
  rename_table :${table}, :${new_name}${cursor}
  
  mod
  module ${ModuleName}
  	module ClassMethods
  		${cursor}
  	end
  	
  	extend ClassMethods
  	
  	def self.included(receiver)
  		receiver.extend(ClassMethods)
  	end
  	
  	
  end
  
  mod
  module ${ModuleName}
  	${cursor}
  end
  
  mod
  module ${ModuleName}
  	module_function
  	
  	${cursor}
  end
  
  mrc
  remove_column :${table}, :${column}
  
  ope
  open(${pipe}) { |${io}| ${cursor} }
  
  opt
  opts.on( "-${o}", "--${option}"${1},
           "${description}" ) do |${opt}|
  	${cursor}
  end
  
  optp
  require "optparse"
  require "ostruct"
  
  options = OpenStruct.new(${default})
  
  ARGV.options do |opts|
  	opts.banner = "Usage:  #{File.basename($$PROGRAM_NAME)}  [OPTIONS]${1}"
  	
  	opts.separator ""
  	opts.separator "Specific Options:"
  	
  	${cursor}
  	
  	opts.separator "Common Options:"
  	
  	opts.on( "-h", "--help",
  	         "Show this message." ) do
  		puts opts
  		exit
  	end
  	
  	begin
  		opts.parse!
  	rescue
  		puts opts
  		exit
  	end
  end
  
  
  par
  partition { |${e}| ${cursor} }
  
  params
  params[:${id}]
  
  patfh
  File.join(File.dirname(__FILE__), *%w[${here}])
  
  Pn
  PStore.new(${file_name})
  
  ra
  render :action => "${action}"
  
  ral
  render :action => "${action}", :layout => "${layoutname}"
  
  ran
  sort_by { rand }
  
  rb
  #!/usr/bin/env ruby -w
  
  
  
  rcea
  render_component :action => "${index}"
  
  rcec
  render_component :controller => "${items}"
  
  rceca
  render_component :controller => "${items}", :action => "${index}"
  
  rdb
  RAILS_DEFAULT_LOGGER.debug "${message}"${cursor}
  
  rea
  redirect_to :action => "${index}"
  
  reai
  redirect_to :action => "${show}", :id => ${item}
  
  rec
  redirect_to :controller => "${items}"
  
  reca
  redirect_to :controller => "${items}", :action => "${list}"
  
  recai
  redirect_to :controller => "${items}", :action => "${show}", :id => ${item}
  
  rej
  reject { |${e}| ${cursor} }
  
  reject
  reject { |${element}| ${element}.${cursor} }
  
  rep
  results.report("${name}:") { TESTS.times { ${cursor} } }
  
  req
  require "${cursor}"
  
  reve
  reverse_each { |${e}| ${cursor} }
  
  rf
  render(:file => "${filepath}")
  
  rfu
  render(:file => "${filepath}", :use_full_path => ${false})
  
  ri
  render(:inline => "${hello}")
  
  ril
  render(:inline => "${hello}", :locals => { ${name} => "${value}"${4} })
  
  rit
  render(:inline => "${hello}", :type => ${rxml})
  
  rl
  render(:layout => "${layoutname}")
  
  rn
  render(:nothing => ${true})
  
  rns
  render(:nothing => ${true}, :status => ${401})
  
  ro
  attr_reader :${attr_names}
  
  rp
  render(:partial => "${item}")
  
  rpc
  render(:partial => "${item}", :collection => ${items})
  
  rpl
  render(:partial => "${item}", :locals => { :${name} => ${value} })
  
  rpo
  render(:partial => "${item}", :object => ${object})
  
  rps
  render(:partial => "${item}", :status => ${500})
  
  rt
  render(:text => "${render}")
  
  rtl
  render(:text => "${render}", :layout => "${layoutname}")
  
  rtlt
  render(:text => "${render}", :layout => ${true})
  
  rts
  render(:text => "${render}", :status => ${401})
  
  rw
  attr_accessor :${attr_names}
  
  sca
  scan(/${pattern}/) { |${match}| ${cursor} }
  
  sel
  select { |${e}| ${cursor} }
  
  select
  select { |${element}| ${element}.${2} }${cursor}
  
  session
  session[:${User}]
  
  sin
  class << self; self end
  
  sor
  sort { |a, b| ${cursor} }
  
  sorb
  sort_by { |${e}| ${cursor} }
  
  ste
  step(${2}) { |${n}|${cursor} }
  
  sub
  sub(/${pattern}/) { |${match}|${cursor} }
  
  tc
  require "test/unit"
  
  require "${library_file_name}"
  
  class Test${amp} < Test::Unit::TestCase
  	def test_${case_name}
  		${cursor}
  	end
  end
  
  tim
  times { |${n}|${cursor} }
  
  tra
  transaction${1} { ${cursor} }
  
  ts
  require "test/unit"
  
  require "tc_${test_case_file}"
  require "tc_${test_case_file}"
  
  
  uni
  ARGF.each_line${1} do |${line}|
  	${cursor}
  end
  
  unless
  unless ${condition}
  	${cursor}
  end
  
  until
  until ${condition}
  	${cursor}
  end
  
  upt
  upto(${0}) { |${n}|${cursor} }
  
  usai
  if ARGV.${1}
    puts "Usage:  #{$$PROGRAM_NAME} ${ARGS_GO_HERE}"
    exit
  end
  
  usau
  unless ARGV.${1}
    puts "Usage:  #{$$PROGRAM_NAME} ${ARGS_GO_HERE}"
    exit
  end
  
  va
  validates_associated :${attribute}
  
  vc
  validates_confirmation_of :${attribute}
  
  ve
  validates_exclusion_of :${attribute}
  
  verify
  verify :only => [:${1}], :session => :user, :params => :id, :redirect_to => {:action => '${index}'}
  
  
  verify
  verify :only => [:${1}], :method => :post, :render => {:status => 500, :text => "use HTTP-POST"}
  
  
  vl
  validates_length_of :${attribute}, :within => ${20}
  
  vp
  validates_presence_of :${attribute}
  
  vpif
  validates_presence_of :${attribute}, :if => proc { |obj| ${condition} }}
  
  vu
  validates_uniqueness_of :${attribute}
  
  when
  when ${condition}
  	${cursor}
  
  while
  while ${condition}
  	${cursor}
  end
  
  wo
  attr_writer :${attr_names}
  
  Yd
  File.open(${yaml}, "w") { |${file}| YAML.dump(${obj}, ${file}) }
  
  yields
   :yields: ${arguments}
  
  Yl
  File.open(${yaml}) { |${file}| YAML.load(${file}) }
  
  zip
  zip(${enums}) { |${row}| ${cursor} }
