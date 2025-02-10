


```
console.log(a);
{ // meaningless block
	var a = 5;
}

>> undefined
```


===


```
var a

console.log(a)
{
a = 5
}

>> undefined
```


Both will return undefined because 'a' gets hoisted up to the top.

If we change it to let then it will be blocked inside of that meaningless scope, and console.log() will not know what 'a' is.