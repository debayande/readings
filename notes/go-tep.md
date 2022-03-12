# Go in Three Easy Pieces

🎬 Greisemer, Robert. 2012. [Go In Three Easy Pieces](https://docs.microsoft.com/en-us/events/lang-next-2012/go-in-three-easy-pieces). Lang.NEXT 2012. Redmond, WA.

## Notes

* Declarations use a cleaned-up Pascal style
    - `// keyword name [type] [initial value]`
* Statements use a cleaned-up C style
    - No semicolons needed
* Object-orientation
    - Methods without classes (?)
    - Interfaces without hierarchies (?)
    - Code reuse without inheritance (?)
* Concurrency and communication
    - Built into the language; no external libraries needed
    - Support for concurrency comes with "batteries included"
* Exception handling
    - Functions with multiple return values
    - `defer` for deferring function invocation
    - No `try...catch`
* Static dispatch (?)
* A method is a function with a receiver (?)
* Methods can be attached to any type
* There is no need for a class (there are no classes); one can just define methods as and when they 
become necessary
* Explicit casts are needed — numeric types do not exhibit implicit conversions
* An interface is a type that defines a set of methods
* A type that implements all methods of an interface is said to implement the interface
* All types implement the empty interface, `interface{}`
* Dynamic dispatch (?)
* A value of a type that implements an interface can be assigned to a variable of that interface 
type
* Typically, interfaces are small (1-3 methods)
* Pervasive use of key interfaces in the standard library makes it easy to chain APIs together
* Interfaces are often introduced ad-hoc, and after the fact
* There's no explicit hierarchy and thus no need to design one
*

## Concepts

### Managed vs. native code
### Dynamic vs. static dispatch

When code involves polymorphism, there needs to be a mechanism to determine which specific version 
is actually run. This is called "dispatch". There are two major forms of dispatch: static and 
dynamic dispatch.
