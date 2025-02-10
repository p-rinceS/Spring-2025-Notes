
(This is a guide not a tutorial!)


Dynamic Typing:
	JS is loosely typed: No need to declare a variable type.
	Runtime Type Change: Variable types can be changed during execution
		Example:
		`let variable = num`
			`$typeof(variable)`
				`>number`
		`variable = "hey, whats up!"`
			`$typeof(variable)`
				`>string`

Functions as First-Class Citizens
	- [[Assign to Variables]]
	- [[Higher-Order Functions]]
	- [[Arrow Functions]]
		- e.g. 
``` JavaScript
const greet = () => "Hello";
const run = (fn) => fn();
run(greet)
```
This is a valid example of using functions as variables, passing functions as parameters, and how a function uses arrows.

Scoping and Hoisting
	*Function-Scoped*: [['var' variables]]
	*Block-Scoped*: [['let' variables.]]
	*Hoisting*: variables are 'hoisted' to the top of their scope.

`this` keyword
	Contextual: Depends on how the function is called.
	[[Bind, Apply, Call]]: Methods to control `this`
[[Truthy and Falsie]]


Event Loop & Concurrency Model
	[[Single-Threaded]]
	[[Event Loop]]
	[[Callback Queue]]
		e.g.
```		JavaScript
setTimeout(() => console.log("Hi), 0) 
		console.log("Bye")

>> "Bye" "Hi"
	
```
		


[[Event-Driven Programming]]

Asynchronous Programming
	Callbacks: Early method for async programming
	Promises: Improved way to handle async operations
	`async/await`: modern async handling

```JavaScript
async function fetchData() {
	const data = await fetch('some-api.com');
}

// await said implicitly, go to sleep, and after this fetch to some-api is done then callback will happen and run whatever the next line will be in the function

// cons: hard to debug
// pro: very cool

```


The DOM
	Select Elements: `querySelector`, `getElementById`, etc.
	Modify Content: Changing HTML or CSS
	Window and Document: Not available in Node.js

``` JavaScript
document.querySelector('.class').innerHTML = "hello";
```


ES6+ Features
	[[Arrow Functions]]
	Destructuring
		Easily extract properties from objects
	Template Literals
		String interpolation
String Mode
	Catching Errors
		- Easier debugging
	Prevent Mistakes
		- Stops, or throws errors, for common JS pitfalls.
e.g.
``` JavaScript
"use strict";

x = 3.14; // this will cause an errror (no 'let' or 'var')
```



Runtimes
	Browser
		Executes JS on the Web
	Node.js
		Server-side JS
	Differences
		Filesystem access, global variables like `window`.


9/3/24 (In Lecture)
[[Closure]]
[[Callback Hell]]


[[Promises]]:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise