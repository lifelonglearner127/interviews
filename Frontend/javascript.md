- [Explain Hoisting in javascript](#explain-hoisting-in-javascript)
- [Difference between == and === operators](#difference-between--and--operators)
- [Difference between var and let keyword in javascript](#difference-between-var-and-let-keyword-in-javascript)
- [Explain Implicit Type Coercion in Javascript](#explain-implicit-type-coercion-in-javascript)
- [Explain Passed by value and passed by reference](#explain-passed-by-value-and-passed-by-reference)
- [Explain call(), apply() and bind() methods](#explain-call-apply-and-bind-methods)
- [What are callbacks?](#what-are-callbacks)
- [What are arrow functions?](#what-are-arrow-functions)
- [What do you mean by prototype design pattern?](#what-do-you-mean-by-prototype-design-pattern)
- [What is the use of promises in javascript?](#what-is-the-use-of-promises-in-javascript)
- [What is memoization?](#what-is-memoization)

### Explain Hoisting in javascript
Hoisting is a Javascript mechanism where all the variables, function declarations and classes are moved to the top of their scope before code execution.
JavaScript only hoists declarations, not initialisation.
To avoid hoisting, you can run javascript in strict mode by using “use strict” on top of the code.

### Difference between == and === operators
Both are comparison operators. The difference between both the operators is that `==` is used to compare values whereas `===` is used to compare both values and types.

### Explain Implicit Type Coercion in Javascript
Implicit type coercion in javascript is the automatic conversion of value from one data type to another. It takes place when the operands of an expression are of different data types.
- String coercion
- Boolean Coercion
- Equality Coercion

### Explain Passed by value and passed by reference
In JavaScript, primitive data types are passed by value and non-primitive data types are passed by reference.

### Explain Higher Order Functions in Javascript
Higher-order function is a function that accepts another function as an argument or returns a function as a return value or both.

### Explain call(), apply() and bind() methods

### Difference between var and let keyword in javascript
- The keyword `Var` has function scope. Anywhere in the function, the variable specified using var is accessible but in `let` the scope of a variable declared with the `let` keyword is limited to the block in which it is declared. 
- `var` declares a variable that will be hoisted but `let` declares a variable that will not be hoisted.

### What are callbacks?
A callback is a function that will be executed after another function gets executed. In javascript, functions are treated as first-class citizens, they can be used as an argument of another function, can be returned by another function, and can be used as a property of an object.

### What are arrow functions?
Arrow functions were introduced in the ES6 version of javascript. They provide us with a new and shorter syntax for declaring functions, but it is limited and can't be used in all situations.
- Arrow functions don't have their own bindings to `this`, `arguments` or `super`, and should not be used as methods.
- Arrow functions aren't suitable for `call`, `apply` and `bind` methods, which generally rely on establishing a scope.
- Arrow functions cannot be used as constructors.
- Arrow functions cannot use yield, within its body.


### What do you mean by prototype design pattern?
### What is the use of promises in javascript?
Promises are used to handle asynchronous operations in Javacript. Before promises, callbacks were used to handle asynchronous operations. But due to the limited functionality of callbacks, using multiple callbacks to handle asynchronous code can lead to unmanageable code.

Promise object has four states:
- `Pending`: Initial state of promise. This state represents that the promise has neither been fulfilled nor been rejected, it is in the pending state.
- `Fulfilled`:  This state represents that the promise has been fulfilled, meaning the async operation is completed.
- `Rejected`: This state represents that the promise has been rejected for some reason, meaning the async operation has failed.
- `Settled`:  This state represents that the promise has been either rejected or fulfilled.

A promise is created using the Promise constructor which takes in a callback with two parameters, `resolve` and `reject` respectively.
- `resolve` is a function that will be called when the async operation has been successfully completed.
- `reject` is a function that will be called, when the async operation fails or if some error occurs.

We can consume any promise by attaching `then()` and `catch()` methods to the consumer.
- `then()` method is used to access the result when the promise is fulfilled.
- `catch()` method is used to access the result/error when the promise is rejected.

### What is memoization?
Memoization is a programming technique which attempts to increase a function’s performance by caching its previously computed results. If the parameter of that function is not changed, the cached version of the function is returned.
Computing the result with the same parameter, again and again, is not a big deal in case of the function is light-weight.
But imagine if the function does some heavy-duty work, then, computing the result again and again with the same parameter will lead to wastage of time.
This is where memoization comes in. By using memoization we can store(cache) the computed results based on the parameters. If the same parameter is used again while invoking the function, instead of computing the result, we directly return the stored (cached) value.