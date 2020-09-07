## TDD
### Test-Driven Development
## What is Test-Driven Development?
### Test-driven development (TDD) is a technique for ensuring that your code does what you think it does. It’s particularly relevant for JavaScript, with its cross-browser incompatibilities and hidden gotchas. With TDD, you express your intentions twice: once as a test, and once as production code. If the two approaches don’t match, your tests fail, and you’ve caught a bug.



## Inheritance and the prototype chain
### JavaScript objects are dynamic "bags" of properties (referred to as own properties). JavaScript objects have a link to a prototype object. When trying to access a property of an object, the property will not only be sought on the object but on the prototype of the object, the prototype of the prototype, and so on until either a property with a matching name is found or the end of the prototype chain is reached.

## This
### A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.

In most cases, the value of this is determined by how a function is called (runtime binding). It can't be set by assignment during execution, and it may be different each time the function is called. ES5 introduced the bind() method to set the value of a function's this regardless of how it's called, and ES2015 introduced arrow functions which don't provide their own this binding (it retains the this value of the enclosing lexical context).

# Classes
## Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 classalike semantics.
