- [Ahead-of-time compilation](#ahead-of-time-compilation)
- [Just-in-time compilation](#just-in-time-compilation)
- [Pure function](#pure-function)

### Ahead-of-time compilation
In computer science, ahead-of-time compilation (AOT compilation) is the act of compiling an (often) higher-level programming language into an (often) lower-level language before execution of a program, usually at build-time, to reduce the amount of work needed to be performed at run time.
Most often, it is associated with the act of compiling a higher-level programming language such as C or C++, or an intermediate representation such as Java bytecode or .NET Framework Common Intermediate Language (CIL) code, into a native (system-dependent) machine code so that the resulting binary file can execute natively, just like a standard native compiler.
When being used in this specific context, it's often seen as an opposite of just-in-time (JIT) compiling.

### Just-in-time compilation
In computing, just-in-time (JIT) compilation (also dynamic translation or run-time compilation) is a way of executing computer code that involves compilation during execution of a program (at run time) rather than before execution.
This may consist of source code translation but is more commonly bytecode translation to machine code, which is then executed directly. 
A system implementing a JIT compiler typically continuously analyses the code being executed and identifies parts of the code where the speedup gained from compilation or recompilation would outweigh the overhead of compiling that code.

### Pure function
In computer programming, a pure function is a function that has the following properties.
-	The function return values that are identical for identical arguments
-	The function application has no side effects (no mutation of local static variables, non-local variables, mutable reference arguments or input/output streams)
