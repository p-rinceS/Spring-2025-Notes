


[[TypeScript]] allows for type assertions to override inferred types.


This is useful in scenarios where you’re certain of a type but TypeScript can’t determine it automatically.


``` typescript

let somevalue = "unknown value";

let strLength: number = (somevalue as string). length;
```

