

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