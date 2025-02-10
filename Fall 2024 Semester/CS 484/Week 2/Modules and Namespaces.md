[[TypeScript]]


TS supports ES6 modules 

allows code to be organized into separate files with clearly defined imports and exports
([[Separation of Concerns]])


Namespaces can be used to group related code together under a common name.
	- Prevents global scope pollution

Example:
	imagine a file named mathUtils.ts

``` TypeScript
export function add(a:number, b:number): number{
	return a + b;
}

import {add} from './mathUtils';
console.log(add(5,3)); // >> 8
```


