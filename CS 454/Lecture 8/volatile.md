

Java keyword that can be added to fields

```java
class C {
	volatile int;
}
	```
****
A **<font color="#f79646">write</font>** to a *volatile* field [[happens-before]] every subsequent <font color="#9bbb59">read</font> of that *volatile* field.
	- Read/read does not happen before
	- Write/write does not happen **before**


The volatile keyword in java ensures that the value is always read from and written to main memory rather than the thread's LOCAL cache.

Therefore the volatile keyword makes the variable's value visible across multiple threads



