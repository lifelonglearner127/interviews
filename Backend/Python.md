- [What is Python? What are the benefits of using Python](#what-is-python-what-are-the-benefits-of-using-python)
- [What is a dynamically typed language?](#what-is-a-dynamically-typed-language)
- [What is an Interpreted language?](#what-is-an-interpreted-language)
- [What is Pep8 and why is it important?](#what-is-pep8-and-why-is-it-important)
- [What is Scope in Python?](#what-is-scope-in-python)
- [How is memory managed in Python?](#how-is-memory-managed-in-python)
- [What are decorators in Python?](#what-are-decorators-in-python)
- [What is pickling and unpickling?](#what-is-pickling-and-unpickling)
- [What are iterators in Python?](#what-are-decorators-in-python)
- [What are generators in Python?](#)

### What is Python? What are the benefits of using Python
### What is a dynamically typed language?
### What is an Interpreted language?
### What is Pep8 and why is it important?
PEP stands for Python Enhancement Proposal.
A PEP is an official design document providing information to the Python community, or describing a new feature for Python or its processes.
PEP 8 is especially important since it documents the style guidelines for Python Code.
Apparently contributing to the Python open-source community requires you to follow these style guidelines sincerely and strictly.

### What is Scope in Python?

### How is memory managed in Python?
Memory management in Python involves a private heap containing all Python objects and data structures.
The management of this private heap is ensured internally by the Python memory manager.
The Python memory manager has different components which deal with various dynamic storage management aspects, like sharing, segmentation, preallocation or caching.

At the lowest level, a raw memory allocator ensures that there is enough room in the private heap for storing all Python-related data by interacting with the memory manager of the operating system.
On top of the raw memory allocator, several object-specific allocators operate on the same heap and implement distinct memory management policies adapted to the peculiarities of every object type.
For example, integer objects are managed differently within the heap than strings, tuples or dictionaries because integers imply different storage requirements and speed/space tradeoffs.
The Python memory manager thus delegates some of the work to the object-specific allocators, but ensures that the latter operate within the bounds of the private heap.

It is important to understand that the management of the Python heap is performed by the interpreter itself and that the user has no control over it, even if they regularly manipulate object pointers to memory blocks inside that heap.
The allocation of heap space for Python objects and other internal buffers is performed on demand by the Python memory manager through the Python/C API functions.

### What are decorators in Python?
Decorators in Python are essentially functions that add functionality to an existing function without changing the structure of the function itself.
Functions in Python are first-class object, which means that functions can be passed around and used as arguments.
This is a fundamental concept to understand Python decorators.
Decorators are usually called before the definition of a function you want to decorate.

### What is pickling and unpickling?
Pickle in Python is primarily used in serializing and deserializing a Python object structure.

**Pickling** is the process of converting a Python object into a byte stream to store it in a file/database, maintain program state across sessions, or transport data over the network.
**Unpickling** is the complete inverse of pickling. It deserializes the byte stream to recreate the objects stored in the file and loads the object to memory.

### What are iterators in Python?
An iterator is an object that contains a countable number of values.
An iterator is an object that can be iterated upon, meaning that you can traverse through all the values.
Technically, in Python, an iterator is an object which implements the iterator protocol, which consist of the methods __iter__() and __next__().
Lists, tuples, dictionaries, and sets are all iterable objects.
