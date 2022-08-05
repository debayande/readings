    * Discussions first started in late 2007.
* Spec first drafted in March 2008.
* Initially generated C.
* Once spec arose, the compiler was re-written to generate native code.
* First `hello_world.go`:
```
package main

func main() int {
    print "Hello, world!\n";
    return 0;
}
```
* Then:
```
package main

func main() int {
    print "Hello, world\n";
}
```
* Then, print became a function and not a primitive:
```
package main

func main() {
    print("Hello, world!\n");
}
```
* Then:
```
package main

import "fmt"

func main() {
    fmt.printf("Hello, world!\n");
}
```
* Then came "uppercase for export" (casification):
```
package main

import "fmt"

func main() {
    fmt.Printf("Hello, world!\n");
}
```
* Today, no semicolons:
```
package main

import "fmt"

func main() {
    fmt.Printf("Hello, world!\n")
}
```
* Some languages that influenced and informed th design of Go include C, Pascal, Modula 2, Oberon 
2, CSP, Occam, Newsqueak, Limbo, Alef, BCPL, Smalltalk, APL. Plus good and bad lessons gleaned from 
C++, C#, Java, JavaScript, LISP, Python, Scala...
* The package `main`
    - One place where the legacy of C shows through
    - `main` package, `main` function ⟹ the root of the initialisation tree
* `import`
    - ⟹ mechanism to load a package
    - Implemented by the compiler, not by a text processor (preprocessor)
    - Imports a package, not a set of identifiers
* `fmt`
    - The package path is just a string, not a list of identifiers
    - Allows the language to avoid defining what it means — thus keeping things adaptable; also 
        allows for future growth
    - Always wanted URLs to be an option
* `func`
    - A keyword that introduces functions; allows for easy parsing (important for function literals 
        or closures)
* 