

The value of `this` is determined dynamically



`call()`
	Invokes a function immediately and allows you to specify the value of `this` and pass arguments individually
	Example:
		`func.call(thisArg, arg1, arg2, ...)`
		
```JavaScript
function greet(greeting) {
	console.log(`${greeting}, my name is ${this.name}`);
}

const person = { name: 'Alice' };

greet.call(person, 'Hello'); // Output: Hello, my name is Alice
		```




`apply()`
	Similar to call() but it takes arguments as an array
	`func.apply(thisArg, [argsArray])`
	
``` JavaScript
function greet(greeting, punctuation) {
	console.log(`${greeting}, my name is ${this.name}{$punctuation}`);
}

const person = {name: "Bob"};

greet.apply(person, ["Hello", "!"]);
```



`bind()`
	Returns a new function where `this` is permanently bound to the provided value, allows the function to be called later with the desired `this`
	`const boundFunction = func.bind(thisArg, arg1, arg2, ...)`

``` JavaScript
function greet(greeting){
	console.log(`${greeting}, my name is ${this.name}`);
}

const person = {name: "Prince"}

const boundGreet = greet.bind(person);

boundGreet('hey');

//outputs: hey, my name is Prince

```


| Method    | Execution                                             | Arguments                   | Use Case                                                                                         |
| --------- | ----------------------------------------------------- | --------------------------- | ------------------------------------------------------------------------------------------------ |
| `call()`  | Executes immediately                                  | Passed individually         | Use when you need to invoke the function right away and set `this`                               |
| `apply()` | Executes immediately                                  | Passed as an array          | Same as `call()`, but useful when arguments are already in an array                              |
| `bind()`  | Returns a new function (does not execute immediately) | Passed individually or none | Use when you want to create a new function with `this` bound and possibly some pre-set arguments |

