
[[TypeScript]]'s Generics allow you to create reusable components that can work with any datatype


Provide a way to create functions, classes, or interfaces that can operate on a variety of types while still being type-safe

Example:

``` TypeScript

function identity<T>(arg:T): T{
	return arg;
}

let num = identity<number>(5);
let str = identity<string>("hello");

// very cool
```



