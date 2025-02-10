

[[TypeScript]] has powerful type inference capabilities, even though you can explicitly declare your types.


This means the compiler can often determine the type of a variable based on the value assigned to it 



``` typescript

let x = 10; // typescript infers x is a number
x = "hello"; // error because type 'string' is not assignable to type 'number'
```


