- [Ahead-of-time compilation](#ahead-of-time-compilation)
- [Just-in-time compilation](#just-in-time-compilation)
- [Pure function](#pure-function)
- [REST API](#rest-api)
- [Hash function](#hash-function)
- [Time & Space Complexity](#time--space-complexity)
- [What is a Headless CMS?](#what-is-a-headless-cms)


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

### REST API
A REST API is an application programming interface that conforms to the constraints of REST architectural style and allows for interaction with RESTful web services. REST stands for representational state transfer.
REST is a set of architectural constraints, not a protocol or a standard. When a client request is made via a RESTful API, it transfers a representation of the state of the resource to the requester or endpoint. This information, or representation, is delivered in one of several formats via HTTP: JSON, HTML, XLT, or plain text. JSON is the most generally popular file format to use because it's language-agnostic.
Something else to keep in mind: Headers and parameters are also important in the HTTP methods of a RESTful API, as they contain important identifier information as to the request's metadata, authorization, uniform resource identifier(URI), caching, cookies and more. There are request headers and response headers, each with their own HTTP connection information and status codes.

In order for an API to be considered RESTful, it has to confirm to these criteria:
- `Client-server architecture`: The client-server design pattern enforces the principle of `separation of concerns`: separating the user interface concenrs from data storage concerns.
- `Statelessness`: In computing, a stateless protocol is a communication protocol in which no session information is retained by the receiver, usually a server. No client information is stored between get requests and each request is separate and unconnected.
- `Cacheability`: As on the World Wide Web, clients and intermediaries can cache responses. Responses must define themselves as either cacheable or non-cacheable. Well-managed caching partially or completely eliminates some client-server interactionis, further improving scalability and performance.
- `Layered system`: A layered system is a system in which components are grouped in a hierarchical arragement, such that lower layers provide functions and services that support the functions and servies of higher layers. If a proxy or load balancer is placed between the client and server, it won't affect their communications, and there won't be a need to update the client or server code.
- `Uniform interface`: A uniform interface between components so that information is transferred in a standardized form instead of specific to an application's needs.
- `Code on demand`: the ability to send exectuable code from the server to the client when requested, extending client functionality.

### Hash function
A hash function is any function that can be used to map data of arbitrary size to fixed-size values. The values returned by a hash function are called hash values.
Hash functions and their associated hash tables are used in data storage and retrieval applications to access data in a small and nearly constant time per retrieval.
A good hash function satisfies two basic properties: 
- It should be very fast to compute; 
- It should minimize duplication of output values (collisions)


### Time & Space Complexity
`Time complexity` is the computational complexity that describes the amount of computer time it takes to run an algorithm. The time complexity is commonly expressed using big O notation.

`Space complexity` of an algorithm or a computer program is the amount of memory space required to solve an instance of the computational problem as a function of characteristics of the input. It is the memory required by an algorithm until it executes completely.



### What is a Headless CMS?
A headless CMS is a content management system that separates where content is stored (the “body”) from where it is presented (the “head“). You can store the content in your headless CMS and then send it to display anywhere – offering a lot more flexibility as to how it's presented in different places. The “head” relates to where your content ends up, and the “body” is where your content is stored and authored.
