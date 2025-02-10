


[[TypeScript]] supports Union and intersection types, this allows a variable to take multiple types (union).


These features allow it to handle multiple different types of data in a type-safe manner.

Example:


``` TypeScript
function printId(id:number | string){
	console.log(`ID: ${id}`);
}

printId("yooo"); // >> ID: yooo

printId("101"); // >> ID: 101

```

