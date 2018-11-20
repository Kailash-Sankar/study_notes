# Javascript

#### Foundation
- ECMAscript
- ES6

#### Concepts
- Mutable vs Immutable
- Hoisting - moving declarations to the top of the current scope
- Module pattern
- lexical scope
- Property shadowing
- First class functions and Higher order functions

#### Topics
* Primitives
  - undefined, null, boolean, string and number
* Array
	 - arr1.push(arr2) this will push arr2 as a single element in to arr1
   - reverse gives a reference and also reverse the array it's called on
   - slice accepts negative indices, arr1.slice(-1);
* Object
	- creating objects
		- object literal {}
		- new Object()
		- object constructor
		- object.create(anotherObj) | no constructor
		- built-in's
	- characteristics
		- objects cannot be compared
		- objects are mutable
		- call by reference
	- operations
		- for (prop in obj) - enumerable => object + prototype chain
		- object.keys(obj)
		- Object.getOwnPropertyNames(obj)
		- delete obj.prop
	- property attributes: Object.defineProperty()
		- value, enumerable, configurable, and writable
	- prototype
* Function
  - hoisting
  - self invoking, anonymous
  - object properties
  	- arguments arrary, arguments.length
  - missing parameters are set as undefined
  - call by value expect for objects
  - invoking and this
  	- function, func(a,b)
  	- method, obj.func(a,b)
  	- function constructor, new func(a,b)
  	- call, func.call(obj,a,b);
  	- apply, func.apply(obj,[a,b]);
  	- bind, bind a context with a function
* Closure
	- global and local scope
	- wihout var keyword variables become global
	- allows function to have a private global variables
	- function has access to parent scope even when parent function has closed
	- closure is the combination of a function and the lexical environment within which that function was declared.
	- private scope
	- closures on loops can go wrong
* Promise
	- A promise can only succeed or fail once
	- If a promise has succeeded or failed and you later add a success/failure callback, the correct callback will be called, even though the event took place earlier.
  - fulfilled: The action relating to the promise succeeded
  - rejected: The action relating to the promise failed
  - pending: Hasn't fulfilled or rejected yet
  - settled: Has fulfilled or rejected
* Inheritance
  - classical inheritance
  - prototype inheritance
* Regex
* Error handling
* Util
  - function.toString()
  - global window object
  - Timers - setTimeout, setInterval, clearInterval
* DOM
  - document.forms[1] or document.forms["myForm"] or document.forms.myForm.
  - Custom events
  - Bubbling
  - document.ready: called when page DOM is ready for code to execute, before images
  - document.onload: called when all content is loaded - images, scripts.
* Iterators and Generators
* Gotchas
  - == and ====
  - hasOwnProperty
  - getters and setters
  - this
  - variables created without var keyword
  - let keyword
  - yield keyword
  - null is an object
  - scope of var variable is entire enclosing function
  - enclose entire code in a block to create a closure and a private namespace
  - strict mode
  - numbers in javascript are treated with floating point precision
  - bind
  - observers
* More
  - contentTypes and dataTypes in ajax call
  - callback hell
  - promise vs callback
  - continue and break statements
  - type casting, output of 1 + 3 + '3'
  - check if a variable is undefined, typeof(x)
  - namespaces in JavaScript

#### Links
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain
* https://github.com/leonardomso/33-js-concepts
