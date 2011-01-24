--- 
scala: |-
  * Collection of Notes about Scala Programming Language *
  
  * The basics
  
  ** How to read from STDIN: Source.fromInputStream(System.in)
  
  * Data types
  
  * Control structures and Logical expressions
  ** About Case expressions :
     You can use '|' to combine various case options.
  ** You can't use break or continute, use boolean variables in place.
  
  * Function and methods
  ** When passing arguments to a method, you should enclose the argument in () if
     they also explicitly specify type.
  ** You should always use = to define methods.
  ** You can use somewhat ugly () to return Unit from a method.
  ** backend_connection? is a invalid method name, while backend_conneciton_?
     isn't.
  ** For using variadic functions, one should specify type with a * suffix.
     def helloWorld(arg: Int*) = { }
     One can use Any* for generic types.
  ** Scala compiler won't do type inference for function calls and hence type
     must be specified while defining the functions.
  
  ** The equals sign that precedes the body of a function hints that in
     the functional world view, a function defines an expression that results in a
     value.
  
  ** Partial Applied Functions :
  ** A method name that ends with ":" is applied right to left and hence a:::b
     will apply as b.:::(a)
  ** When you are invoking a method that takes tuples as parameters, you should
     surround it with additional parenthesis. For example:
  
     Following invocation won't pass a tuple.
       tSet += ("Air","Tel")
  
     But if you have to pass a tuple:
       tSet.takesTuple(("Air","Tel"))
  ** 1 -> "lol" will return a two element tuple. The mechanism which allows us to
     invoke -> on any object is called implicits in scala.
  
  ** One gotcha to watch out for is that whenever you leave off the equals sign
     before the body of a method, its result type will definitely be Unit.
  
  ** When you are using Method chaining, you should always put the operator at
     the end.
  
  * Classes and Object Orientation
  ** When you use Method overloading, you must specify return type clearly.
  ** When a class inherits another class, default constructor is generally
     automatically invoked, and you need not do any extra work for that.
  
  ** The parameters passed to a class for construction become private val fields
     for the class.
  
  ** In java uninitialized fields of a class are initialized to default values
     such as null,0 or false depending on their type if no value is provided for
     them in class definition.
     We can achieve the same effect in scala, by using:
  
        var x: Int = _
  
  ** When a Singleton shares same name with the class template its called
     companion object for the class.  You must define class and its companion
     object in the same file.
  ** one can use keyword 'require' in class definition for asserting arguments
     passed while instantiating the object. For example:
       class Rational(n: Int,d: Int) {
         require(d != 0)
         override def toString = n + "/" + d
       }
  ** In scala, in body on any auxiliary constructor, first method call should be
     of, another constructor of the same class. Called constructor can be primary
     contructor or another auxiliary constructor which comes textually before
     current contructor.  This rule is enforced because in Scala only primary
     contructor can invoke superclass constructors.
  
  * Case class and Pattern Matching
  ** Since, case classes come predefined with their Factories for object
     creation, you don't need to call new on them, but you must use () for
     creating objects, even if case class constructor doesn't accept any
     parameters.
  
  * Functional Programming Primitives
  
  * Language Specific Miscellenany
  ** Use split with care.
  ** Scala operator precedence table:
     nfix (least to highest precedence)
  
     |
     ^
     &
     < >
     = !
     :
     + -
     * / %
     ~
  
     Postfix (unary_)
  
     +
     -
     !
     ~
  
     Operators ending with colon (:) are right-associative.
  
  * Concurrent Programming Concepts
  
  * Scala Collection Classes
  ** HashMaps and TreeMaps are based on RedBlackTrees and you often don't need
     them for a simple hash type of functionality.
  ** Another simple and easy to use data structure is Map.
     scala> val map = scala.collection.mutable.Map[String,Int]()
     map: scala.collection.mutable.Map[String,Int] = Map()
  
     scala> map("Hello") = 1
  
     scala> map("World") = 2
  
     scala> map.contains("Hello")
     res39: Boolean = true
  ** If you are looking for 'join' method in scala, use mkString in place of join.
  
  * Scala Type System
  
  ** In scala value assigned to a variable created with val can't be changed, but
     often in the interpreter its possible. The behaviour of interpretor is
     confusing.
  
  ** In scala, a val can be reassigned to some other value by defining the value
     in  a new scope. For example, following code won't compile:
  
     val a = 1
     val a = 2
     println(a)
  
     But following code will compile:
  
     val a = 1
     {
       val a = 2
       println(a)
     }
     println(a)
  
     In this case an inner variable is said to "shadow" an outer variable.
  
  * Language Tools
  
  ** To compile a scala file
     scalac HelloWorld.scala
  
  ** Compile scala file to different location:
     By default scalac generates the class files to the same location as the
     corresponding source files.
     You may specify a different output directory using the -d option.
  
     scalac -d classes HelloWorld.scala
  
  ** To run a compiled scala file
     scala HelloWorld
  
  * UnAnswered Questions:
  ** What are those link and unlink methods in Actor class.
     link and unlink are generally used to link Actors so as one actor can
     monitor and vice-versa.
  ** How to globally identify an Actor without defining it as a singleton.
