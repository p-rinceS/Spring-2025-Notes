Superset of [[JavaScript]]

Compiles down to plain JavaScript, makes it compatible with existing JavaScript codebases.


Adds optional [[static typing]], not an entirely different language from JavaScript.



[[tsx]] makes transpiling code on server side easy.


## **Why is TS different than JS?

adds [[static typing]] to JavaScript, allows us to define variable types explicitly. Helps catch type-related errors at compile-time.

``` TypeScript

let x: number = 5
x = "Hello" // will cause error, type 'string' is not assignable to type 'number'
```

- Interfaces and Type Aliases
	- Typescript allows the defining of [[interfaces]] and type aliases to describe the structure of objects and functions.
``` TypeScript
interface User{
name:string;
age:number;
}

let user:User = {
	name = 'Alice';
	age = 42;

}

```


- [[Classes and Inheritance]]
	- Typescript builds on [[JavaScript]]'s prototype-based inheritance

- [[Generics]]
- [[Union and Intersection Types]]
- [[Type Inference]]
- [[Enums]]
- [[Type Assertions]]
- [[Modules and Namespaces]]
- 
- Advanced Types
	- Mapped Types
	- Conditional Types
	- Utility Types
		# Example:

``` TypeScript
type ReadOnly<T> = {
	readonly [P in keyof T]: T[P];
}

interface User {
	name: string;
	age: number;
}

let user: Readonly<User> = {
	name: "Alice",
	age: 42
};

// user.age = 30; // Error: cannot assign 'age' because it is a read-only property 
```