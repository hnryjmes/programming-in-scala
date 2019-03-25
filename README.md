# Programming in Scala

*Third Edition, by Martin Odersky, Lex Spoon, Bill Venners*

`Notes by Henry Cooksley`

### 1 A Scalable Language

"The language is so named because it was designed to grow with the demands of its users."

#### 1.1 A language that grows on you

"Scala has a set of convenient constructs that help you get started quickly and let you program in a pleasantly concise style."

Growing new types

"Scala is much more like a bazaar than a cathedral, in the sense that it is designed to be extended and adapted by the people programming in it."

"Instead, Scala allows users to grow and adapt the language in the directions they need by defining easy-to-use libraries that feel like native language support."

Growing new control constructs

"Actors are concurrency abstractions that can be implemented on top of threads."

"An actor can perform two basic operations, message send and receive."

"Even though the receive block may look and act very much like a built-in control construct, it is in fact a method defined in Akka's actors library."

"All in all, the actor model has turned out to be a very pleasant means for expressing concurrent and distributed computations."

#### 1.2 What makes Scala scalable?

"Scala goes further than all other well-known languages in fusing object-oriented and functional programming into a uniform language design."

"In fact the actor concept shown previously could not have been implemented without this unification of functions and objects."

Scala is object-oriented

"The great idea of object-oriented programming is to make these containers fully general, so that they can contain operations as well as data, and that they are themselves values that can be stored in other containers, or passed as parameters to operations."

"Traits are like interfaces in Java, but they can also have method implementations and even fields."

Scala is functional

"You can pass functions as arguments to other functions, return them as results from functions, or store them in variables."

"Functions that are first-class values provide a convenient means for abstracting over operations and creating new control structures."

"Immutable data structures are one of the cornerstones of functional programming."

"Functional languages encourage immutable data structures and referentially transparent methods."

#### 1.3 Why Scala?

Scala is compatible

"In fact, almost all Scala code makes heavy use of Java libraries, often without programmers being aware of this fact."

Scala is concise

"A more conservative estimate would be that a typical Scala program should have about half the number of lines of the same program written in Java."

Scala is high-level

"Scala helps you manage complexity by letting you raise the level of abstraction in the interfaces you design and use."

Scala is statically typed

"Starting from a system of nested class types much like Java's, it allows you to parameterize types with generics, to combine types using intersections, and to hide details of types using abstract types."

"These give a strong foundation for building and composing your own types, so that you can design interfaces that are at the same time safe and flexible to use."

Verifiable properties

"Although a static type system certainly cannot replace unit testing, it can reduce the number of unit tests needed by taking care of some properties that would otherwise need to be tested."

Safe refactorings

"A static type system provides a safety net that lets you make changes to a codebase with a high degree of confidence."

Documentation

"Static types are program documentation that is checked by the compiler for correctness."

"In fact, it's not uncommon for user code to have no explicit types at all."

#### 1.4 Scala's roots

"Scala's innovations come primarily from how its constructs are put together."

"For instance, its abstract types provide a more object-oriented alternative to generic types, its traits allow for flexible component assembly, and its extractors provide a representation-independent way to do pattern matching."

#### 1.5 Conclusion

"If you're coming to Scala from Java, the most challenging aspects of learning Scala may involve Scala's type system (which is richer than Java's) and its support for functional programming."

### 2 First Steps in Scala

Step 1. Learn to use the Scala interpreter

"The easiest way to get started with Scala is by using the Scala interpreter, an interactive “shell” for writing Scala expressions and programs."

Step 2. Define some variables

"Scala has two kinds of variables, vals and vars."

"Once initialized, a val can never be reassigned."

"A var can be reassigned throughout its lifetime."

"When the Scala interpreter (or compiler) can infer types, it is often best to let it do so rather than fill the code with unnecessary, explicit type annotations."

Step 3. Define some functions

"Function definitions start with def."

"In Java, the type of the value returned from a method is its return type."

"In Scala, that same concept is called result type."

"Scala's Unit type is similar to Java's void type; in fact, every void-returning method in Java is mapped to a Unit-returning method in Scala."

Step 4. Write some Scala scripts

Step 5. Loop with while; decide with if

Step 6. Iterate with foreach and for

"Scala enables you to program imperatively, but as you get to know Scala better, you'll likely often find yourself programming in a more functional style."

"If a function literal consists of one statement that takes a single argument, you need not explicitly name and specify the argument."

Conclusion

### 3 Next Steps in Scala

"When you complete this chapter, you should have enough knowledge to enable you to start writing useful scripts in Scala."

Step 7. Parameterize arrays with types

"You parameterize an instance with values by passing objects to a constructor in parentheses."

"Scala doesn't technically have operator overloading, because it doesn't actually have operators in the traditional sense."

"Arrays are simply instances of classes like any other class in Scala."

"Scala achieves a conceptual simplicity by treating everything, from arrays to expressions, as objects with methods."

Step 8. Use lists

"One of the big ideas of the functional style of programming is that methods should not have side effects."

"Applying this functional philosophy to the world of objects means making objects immutable."

"Cons prepends a new element to the beginning of an existing list and returns the resulting list."

Step 9. Use tuples

Step 10. Use sets and maps

Step 11. Learn to recognize the functional style

"If the code contains no vars at all - i.e., it contains only vals - it is probably in a functional style."

Step 12. Read lines from a file

### 4 Classes and Objects

#### 4.1 Classes, field, and methods

"Fields are also known as instance variables, because every instance gets its own set of the variables."

#### 4.2 Semicolon inference

#### 4.3 Singleton objects

"As mentioned in Chapter 1, one way in which Scala is more object-oriented than Java is that classes in Scala cannot have static members."

"Instead, Scala has singleton objects."

"If you are a Java programmer, one way to think of singleton objects is as the home for any static methods you might have written in Java."

"One difference between classes and singleton objects is that singleton objects cannot take parameters, whereas classes can."

#### 4.4 A Scala application

#### 4.5 The App trait

#### 4.6 Conclusion

### 5 Basic Types and Operations

"If you're familiar with Java, you'll be glad to find that Java's basic types and operators have the same meaning in Scala."

#### 5.1 Some basic types

"Collectively, types Byte, Short, Int, Long, and Char are called integral types."

"The integral types plus Float and Double are called numeric types."

#### 5.2 Literals

Integral literals

"If an integer literal ends in an L or l, it is a Long; otherwise it is an Int."

Floating point literals

Character literals

"In addition to providing an explicit character between the single quotes, you can identify a character using its Unicode code point."

String literals

"You start and end a raw string with three double quotation marks in a row (""")."

Symbol literals

Boolean literals

#### 5.3 String interpolation

"Because the letter s immediately precedes the open quote, Scala will use the s string interpolator to process the literal."

#### 5.4 Operators are methods

"Operator notation is not limited to methods like + that look like operators in other languages." 

"You can use any method in operator notation."

#### 5.5 Arithmetic operations

#### 5.6 Relational and logical operations

#### 5.7 Bitwise operations

#### 5.8 Object equality

"In Java, you can use == to compare both primitive and reference types."

"On primitive types, Java's == compares value equality, as in Scala."

"On reference types, however, Java's == compares reference equality, which means the two variables point to the same object on the JVM's heap."

"Scala provides a facility for comparing reference equality, as well, under the name eq."

#### 5.9 Operator precedence and associativity

"No matter what associativity an operator has, however, its operands are always evaluated left to right."

#### 5.10 Rich wrappers

"All you need to know for now is that for each basic type described in this chapter, there is also a “rich wrapper” that provides several additional methods."

#### 5.11 Conclusion

### 6 Functional Objects

"In this chapter, the emphasis is on classes that define functional objects, or objects that do not have any mutable state."

#### 6.1 A specification for class Rational

"Compared to floating-point numbers, rational numbers have the advantage that fractions are represented exactly, without rounding or approximation."

#### 6.2 Constructing a Rational

"Immutable objects offer several advantages over mutable objects, and one potential disadvantage."

"First, immutable objects are often easier to reason about than mutable ones, because they do not have complex state spaces that change over time."

"Second, you can pass immutable objects around quite freely, whereas you may need to make defensive copies of mutable objects before passing them to other code."

"Third, there is no way for two threads concurrently accessing an immutable to corrupt its state once it has been properly constructed, because no thread can change the state of an immutable."

"Fourth, immutable objects make safe hash table keys."

"The main disadvantage of immutable objects is that they sometimes require that a large object graph be copied, whereas an update could be done in its place."

#### 6.3 Reimplementing the toString method

#### 6.4 Checking preconditions

"One of the benefits of object-oriented programming is that it allows you to encapsulate data inside objects so that you can ensure the data is valid throughout its lifetime."

#### 6.5 Adding fields

#### 6.6 Self references

#### 6.7 Auxiliary constructors

"In Scala, constructors other than the primary constructor are called auxiliary constructors."

"In Scala, every auxiliary constructor must invoke another constructor of the same class as its first action."

"The invoked constructor is either the primary constructor (as in the Rational example), or another auxiliary constructor that comes textually before the calling constructor."

"The primary constructor is thus the single point of entry of a class."

#### 6.8 Private fields and methods

#### 6.9 Defining operators

#### 6.10 Identifiers in Scala

"An alphanumeric identifier starts with a letter or underscore, which can be followed by further letters, digits, or underscores."

"In Java, the convention is to give constants names that are all upper case, with underscores separating the words, such as MAX_VALUE or PI."

"In Scala, the convention is merely that the first character should be upper case."

#### 6.11 Method overloading

#### 6.12 Implicit conversions

#### 6.13 A word of caution

#### 6.14 Conclusion

### 7 Built-in Control Structures

"The only control structures are if, while, for, try, match, and function calls."

"This is the approach taken by functional languages, where programs are viewed as computing a value, thus the components of a program should also compute values."

#### 7.1 If expressions

"Look for opportunities to use vals."

"They can make your code both easier to read and easier to refactor."

#### 7.2 While loops

"Scala includes the while loop nonetheless because sometimes an imperative solution can be more readable, especially to programmers with a predominantly imperative background."

#### 7.3 For expressions

Iteration through collections

Filtering

Nested iteration

Mid-stream variable bindings

Producing a new collection

#### 7.4 Exception handling with try expressions

Throwing exceptions

"Technically, an exception throw as type Nothing."

Catching exceptions

The finally clause

Yielding a value

#### 7.5 Match expressions

"The most significant difference from Java's switch, however, may be that match expressions result in a value."

#### 7.6 Living without break and continue

"Scala leaves out these commands because they do not mesh well with function literals, a feature described in the next chapter."

"The simplest approach is to replace every continue by an if and every break by a boolean variable."

#### 7.7 Variable scope

"One difference between Java and Scala is that Scala allows you to define variables of the same name in different scopes."

#### 7.8 Refactoring imperative-style code

#### 7.9 Conclusion

### 8 Functions and Closures

"Besides methods, which are functions that are members of some object, there are also functions nested within functions, function literals, and function values."

#### 8.1 Methods

#### 8.2 Local functions

"Just like local variables, such local functions are visible only in their enclosing block."

#### 8.3 First-class functions

"A function literal is compiled into a class that when instantiated at runtime is a function value."

"Thus the distinction between function literals and values is that function literals exist in the source code, whereas function values exist as objects at runtime."

"Function values are objects, so you can store them in variables if you like."

"They are functions, too, so you can invoke them using the usual parentheses function-call notation."

#### 8.4 Short forms of function literals

#### 8.5 Placeholder syntax

"You can think of the underscore as a “blank” in the expression that needs to be “filled in.”"

"This blank will be filled in with an argument to the function each time the function is invoked."

#### 8.6 Partially applied functions

"For example, rather than writing println(_), you could write println _."

"A partially applied function is an expression in which you don't supply all of the arguments needed by the function."

"This apply method, defined in the class generated automatically by the Scala compiler from the expression sum _, simply forwards those three missing parameters to sum, and returns the result."

#### 8.7 Closures

"Scala's syntax for partially applied functions highlights a difference in the design trade-offs of Scala and classical functional languages, such as Haskell or ML."

"In these languages, partially applied functions are considered the normal case."

"The function value (the object) that's created at runtime from this function literal is called a closure."

#### 8.8 Special function call forms

Repeated parameters

"Scala allows you to indicate that the last parameter to a function may be repeated."

Named arguments

Default parameter values

#### 8.9 Tail recursion

"Functions like approximate, which call themselves as their last action, are called tail recursive."

"The Scala compiler detects tail recursion and replaces it with a jump back to the beginning of the function, after updating the function parameters with the new values."

Tracing tail-recursive functions

"A tail-recursive function will not build a new stack frame for each call; all calls will execute in a single frame.

Limits of tail recursion

"The use of tail recursion in Scala is fairly limited because the JVM instruction set makes implementing more advanced forms of tail recursion very difficult."

#### 8.10 Conclusion

"In addition to methods, Scala provides local functions, function literals, and function values."

"In addition to normal function calls, Scala provides partially applied functions and functions with repeated parameters."

### 9 Control Abstraction

#### 9.1 Reducing code duplication

"One benefit of higher-order functions is they enable you to create control abstractions that allow you to reduce code duplication."

#### 9.2 Simplifying client code

#### 9.3 Currying

"A curried function is applied to multiple argument lists, instead of just one."

#### 9.4 Writing new control structures

#### 9.5 By-name parameters

#### 9.6 Conclusion

"You can use functions within your code to factor out common control patterns, and you can take advantage of higher-order functions in the Scala library to reuse control patterns that are common across all programmers' code."

### 10 Composition and inheritance

"Composition means one class holds a reference to another, using the referenced class to help it fulfill its mission."

"Inheritance is the superclass/subclass relationship."

#### 10.1 A two-dimensional layout library

"Such composing operators are also often called combinators because they combine elements of some domain into new elements."

#### 10.2 Abstract classes

#### 10.3 Defining parameterless methods

"The recommended convention is to use a parameterless method whenever there are no parameters and the method accesses mutable state only by reading fields of the containing object (in particular, it does not change mutable state)."

#### 10.4 Extending classes

#### 10.5 Overriding methods and fields

#### 10.6 Defining parametric fields

#### 10.7 Invoking superclass constructors

#### 10.8 Using override modifiers

"These “accidental overrides” are the most common manifestation of what is called the “fragile base class” problem."

"The problem is that if you add new members to base classes (which we usually call superclasses) in a class hierarchy, you risk breaking client code."

#### 10.9 Polymorphism and dynamic binding

#### 10.10 Declaring final members

#### 10.11 Using composition and inheritance

#### 10.12 Implementing above, beside, and toString

#### 10.13 Defining a factory object

"An advantage of this approach is that object creation can be centralized and the details of how objects are represented with classes can be hidden."

#### 10.14 Heighten and widen

#### 10.15 Putting it all together

#### 10.16 Conclusion

"Among others, you encountered abstract classes, inheritance and subtyping, class hierarchies, parametric fields, and method overriding."

### 11 Scala's Hierarchy

"In Scala, every class inherits from a common superclass named Any."

"Because every class is a subclass of Any, the methods defined in Any are “universal” methods: they may be invoked on any object."

"Scala also defines some interesting classes at the bottom of the hierarchy, Null and Nothing, which essentially act as common subclasses."

#### 11.1 Scala's class hierarchy

#### 11.2 How primitives are implemented

"In fact, Scala stores integers in the same way as Java - as 32-bit words."

#### 11.3 Bottom types

#### 11.4 Defining your own value classes

#### 11.5 Conclusion

### 12 Traits

"A trait encapsulates method and field definitions, which can then be reused by mixing them into classes."

"Unlike class inheritance, in which each class must inherit from just one superclass, a class can mix in any number of traits."

#### 12.1 How traits work

#### 12.2 Thin versus rich interfaces

"A rich interface has many methods, which make it convenient for the caller."

"A thin interface, on the other hand, has fewer methods, and thus is easier on the implementers."

#### 12.3 Example: Rectangular objects

#### 12.4 The Ordered trait

#### 12.5 Traits as stackable modifications

#### 12.6 Why not multiple inheritance?

"When you instantiate a class with new, Scala takes the class, and all of its inherited classes and traits, and puts them in a single, linear order."

#### 12.7 To trait or not to trait?

"If the behavior will not be reused, then make it a concrete class."

"If it might be reused in multiple, unrelated classes, make it a trait."

"If you want to inherit from it in Java code, use an abstract class."

"If you plan to distribute it in compiled form, and you expect outside groups to write classes inheriting from it, you might lean towards using an abstract class."

"If you still do not know, after considering the above, then start by making it as a trait."

#### 12.8 Conclusion

"Traits do not merely support the idioms described in this chapter; they are a fundamental unit of code that is reusable through inheritance."

### 13 Packages and Imports

"One way to minimize coupling is to write in a modular style."

#### 13.1 Putting code in packages

#### 13.2 Concise access to related code

#### 13.3 Imports

"The first of these corresponds to Java's single type import and the second to Java's on-demand import."

"For one, imports in Scala can appear anywhere, not just at the beginning of a compilation unit."

#### 13.4 Implicit imports

#### 13.5 Access modifiers

Private members

Protected members

Public members

Scope of members

"Marking a member private[this] is a guarantee that it will not be seen from other objects of the same class."

Visibility and companion objects

#### 13.6 Package objects

"Package objects are frequently used to hold package-wide type aliases and implicit conversions."

#### 13.7 Conclusion

### 14 Assertions and Tests

#### 14.1 Assertions

"The expression assert(condition) throws an AssertionError if condition does not hold."

"The expression assert(condition, explanation) tests condition and, if it does not hold, throws an AssertionError that contains the given explanation."

#### 14.2 Testing in Scala

#### 14.3 Informative failure reports

#### 14.4 Tests as specifications

"In the behavior-driven development (BDD) testing style, the emphasis is on writing human-readable specifications of the expected behavior of code and accompanying tests that verify the code has the specified behavior."

"One of the big ideas of BDD is that tests can be used to facilitate communication between the people who decide what a software system should do, the people who implement the software, and the people who determine whether the software is finished and working."

#### 14.5 Property-based testing

#### 14.6 Organizing and running tests

#### 14.7 Conclusion

### 15 Case Classes and Pattern Matching

"This chapter introduces case classes and pattern matching, twin constructs that support you when writing regular, non-encapsulated data structures."

"These two constructs are particularly helpful for tree-like recursive data."

"If you have programmed in a functional language before, then you will probably recognize pattern matching."

"But case classes will be new to you."

"Case classes are Scala's way to allow pattern matching on objects without requiring a large amount of boilerplate."

#### 15.1 A simple example

"To keep things simple, we'll concentrate on arithmetic expressions consisting of variables, numbers, and unary and binary operations."

Case classes

"Using the modifier makes the Scala compiler add some syntactic conveniences to your class."

"First, it adds a factory method with the name of the class."

"The second syntactic convenience is that all arguments in the parameter list of a case class implicitly get a val prefix, so they are maintained as fields"

"Third, the compiler adds “natural” implementations of methods toString, hashCode, and equals to your class."

"They will print, hash, and compare a whole tree consisting of the class and (recursively) all its arguments."

"Finally, the compiler adds a copy method to your class for making modified copies."

Pattern matching

"A pattern match includes a sequence of alternatives, each starting with the keyword case."

"Each alternative includes a pattern and one or more expressions, which will be evaluated if the pattern matches."

"An arrow symbol => separates the pattern from the expressions."

"A match expression is evaluated by trying each of the patterns in the order they are written."

match compared to switch

"Match expressions can be seen as a generalization of Java-style switches."

"A Java-style switch can be naturally expressed as a match expression, where each pattern is a constant and the last pattern may be a wildcard (which represents the default case of the switch)."

"First, match is an expression in Scala (i.e., it always results in a value)."

"Second, Scala's alternative expressions never “fall through” into the next case."

"Third, if none of the patterns match, an expression named MatchError is thrown."

"This means you always have to make sure that all cases are covered, even if it means adding a default case where there's nothing to do."

#### 15.2 Kinds of patterns

"Since the syntax of patterns is so transparent, the main thing to pay attention to is just what kinds of patterns are possible."

Wildcard patterns

"The wildcard pattern (_) matches any object whatsoever."

Constant patterns

"Any literal may be used as a constant."

Variable patterns

"But unlike a wildcard, Scala binds the variable to whatever the object is."

"You can then use this variable to act on the object further."

Constructor patterns

"It consists of a name (BinOp) and then a number of patterns within parentheses: "+", e, and Number(0)."

"Assuming the name designates a case class, such a pattern means to first check that the constructor parameters of the object match the extra patterns supplied."

Sequence patterns

"You can match against sequence types, like List or Array, just like you match against case classes."

Tuple patterns

Typed patterns

Type erasure

"Scala uses the erasure model of generics, just like Java does."

"This means that no information about type arguments is maintained at runtime."

"The only exception to the erasure rule is arrays, because they are handled specially in Java as well as Scala."

Variable binding

"This gives you a variable-binding pattern, which means the pattern is to perform the pattern match as normal, and if the pattern succeeds, set the variable to the matched object just as with a simple variable pattern."

#### 15.3 Pattern guards

"A pattern guard comes after a pattern and starts with an if."

"If a pattern guard is present, the match succeeds only if the guard evaluates to true."

#### 15.4 Pattern overlaps

#### 15.5 Sealed classes

"What do you do if there is no default?"

"The alternative is to make the superclass of your case classes sealed."

"If you write a hierarchy of classes intended to be pattern matched, you should consider sealing them."

#### 15.6 The Option type

"The Option type is used frequently in Scala programs."

"Compare this to the dominant idiom in Java of using null to indicate no value."

"If a variable is allowed to be null, then you must remember to check it for null every time you use it."

"When you forget to check, you open the possibility that a NullPointerException may result at runtime."

"This approach to optional values has several advantages over Java's."

"But most importantly, that programming error described earlier of using a variable that may be null without first checking it for null becomes a type error in Scala."

"If a variable is of type Option[String] and you try to use it as a String, your Scala program will not compile."

#### 15.7 Patterns everywhere

Patterns in variable definitions

Case sequences as partial functions

"A sequence of cases (i.e., alternatives) in curly braces can be used anywhere a function literal can be used."

"Essentially, a case sequence is a function literal, only more general."

"Instead of having a single entry point and list of parameters, a case sequence has multiple entry points, each with their own list of parameters."

"In general, you should try to work with complete functions whenever possible, because using partial functions allows for runtime errors that the compiler cannot help you with."

Patterns in for expressions

#### 15.8 A larger example

#### 15.9 Conclusion

"In this chapter, you learned about Scala's case classes and pattern matching in detail."

"By using them, you can take advantage of several concise idioms not normally available in object-oriented languages."

### 16 Working with Lists

#### 16.1 List literals

"First, lists are immutable."

"That is, elements of a list cannot be changed by assignment."

"Second, lists have a recursive structure (i.e. a linked list), whereas arrays are flat."

#### 16.2 The List type

"Like arrays, lists are homogenous: the elements of a list all have the same type."

#### 16.3 Constructing lists

"All lists are built from two fundamental building blocks, Mil and :: (pronounced “cons”)."

"Nil represents the empty list."

"The infix operator, ::, expresses list extension at the front."

"That is, x :: xs represents a list whose first element is x, followed by (the elements of) list xs."

#### 16.4 Basic operations on lists

"As an example of how lists can be processed, consider sorting the elements of a list of numbers into ascending order."

"One simple way to do so is insertion sort, which works as follows: To sort a non-empty list x :: xs, sort the remainder xs and insert the first element x at the right position in the result."

#### 16.5 List patterns

"List patterns correspond one-by-one to list expressions."

"Often, pattern matching over lists is clearer than decomposing them with methods, so pattern matching should be a part of your list processing toolbox."

#### 16.6 First-order methods on class List

"A method is first-order if it does not take any functions as arguments."

"The result of xs ::: ys is a new list that contains all the elements of xs, followed by all the elements of ys."

The Divide and Conquer principle

"Many algorithms over lists first split an input list into simpler cases using a pattern match."

"The most common pattern match over lists simply distinguishes an empty from a non-empty list."

Taking the length of a list: length

"On lists, unlike arrays, length is a relatively expensive operation."

"That's why it's not a good idea to replace a test such as xs.isEmpty by xs.length == 0."

Accessing the end of a list: init and last

Reversing lists: reverse

"If at some point in the computation an algorithm demands frequent accesses to the end of a list, it's sometimes better to reverse the list first and work with the result instead."

Prefixes and suffixes: drop, take, and splitAt

Element selection: apply and indices

Flattening a list of lists: flatten

Zipping lists: zip and unzip

Displaying lists: toString and mkString

Converting lists: iterator, toArray, copyToArray

Example: Merge sort

"The insertion sort presented earlier is concise to write, but it is not very efficient."

"Its average complexity is proportional to the square of the length of the input list."

"Merge sort works as follows: First, if the list has zero or one elements, it is already sorted, so the list can be returned unchanged."

"Longer lists are split into two sub-lists, each containing about half the elements of the original list."

#### 16.7 Higher-order methods on class List

"Some examples are: transforming every element of a list in some way, verifying whether a property holds for all elements of a list, extracting from a list elements satisfying a certain criterion, or combining the elements of a list using some operator."

Mapping over lists: map, flatMap and foreach

"The operation xs map f takes as operands a list xs of type List[T] and a function f of type T => U."

"It returns the list that results from applying the function f to each list element in xs."

"The flatMap operator is similar to map, but it takes a function returning a list of elements as its right operand."

"Unlike map and flatMap, however, foreach takes a procedure (a function with result type Unit) as right operand."

"The result of the operation itself is again Unit; no list of results is assembled."

Filtering lists: filter, partition, find, takeWhile, dropWhile, and span

"The partition method is like filter but returns a pair of lists."

"One list contains all elements for which the predicate is true, while the other contains all elements for which the predicate is false."

Folding lists: /: and :\

"A fold left operation “(z /: xs)(op)” involves three objects: a start value z, a list xs, and a binary operation op."

"The result of the fold is op applied between successive elements of the list prefixed by z."

"For associative operations, fold left and fold right are equivalent, but there might be a difference in efficiency."

Example: List reversal using fold

Sorting lists: sortWith

#### 16.8 Methods of the List object

Creating lists from their elements: List.apply

Creating a range of numbers: List.range

Creating uniform lists: List.fill

Tabulating a function: List.tabulate

Concatenating multiple lists: List.concat

#### 16.9 Processing multiple lists together

#### 16.10 Understanding Scala's type inference algorithm

#### 16.11 Conclusion

### 17 Working with Other Collections

#### 17.1 Sequences

Lists

"This combination of features might sound odd, but they hit a sweet spot that works well for many algorithms."

"The fast addition and removal of initial elements means that pattern matching works well, as described in Chapter 15."

Arrays

List buffers

Array buffers

Strings (via StringOps)

#### 17.2 Sets and maps

Using sets

"The key characteristic of sets is that they will ensure that at most one of each object, as determined by ==, will be contained in the set at any one time."

Using maps

"Maps let you associate a value with each element of a set."

Default sets and maps

Sorted sets and maps

#### 17.3 Selecting mutable versus immutable collections

"When in doubt, it is better to start with an immutable collection and change it later, if you need to, because immutable collections can be easier to reason about than mutable ones."

#### 17.4 Initializing collections

Converting to an array or list

Converting between mutable and immutable sets and maps

#### 17.5 Tuples

#### 17.6 Conclusion

### 18 Mutable Objects

"Such mutable objects often come up naturally when you want to model objects in the real world that change over time."

#### 18.1 What makes an object mutable?

#### 18.2 Reassignable variables and properties

"In Scala, every var that is a non-private member of some object implicitly defines a getter and a setter method with it."

#### 18.3 Case study: Discrete event simulation

"This example is taken from the classic textbook Structure and Interpretation of Computer Programs by Abelson and Sussman." 

"What's different here is that the implementation language is Scala instead of Scheme, and that the various aspects of the example are structures into four software layers: one for the simulation framework, another for the basic circuit simulation package, a third for a library of user-defined circuits, and the last layer for each simulated circuit itself."

#### 18.4 A language for digital circuits

#### 18.5 The Simulation API

#### 18.6 Circuit Simulation

The Wire class

The inverter method

The andGate and orGate methods

Simulation output

Running the simulator

#### 18.7 Conclusion

"Higher-order functions were used in the simulation framework to execute actions at specified points in simulated time."

### 19 Type Parameterization

