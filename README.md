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