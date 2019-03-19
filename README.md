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

