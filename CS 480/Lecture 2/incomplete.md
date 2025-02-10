

Can be modeled by adding a special null value to each domain to encode that the value of the attribute is unknown or not applicable.


```json
Student = {
(null, John, null)
}
```


Adding incompleteness significantly increases the complexity of operations.

-- Non trivial questions 
		For example, what should 3 == null equate to.
			False