



You have an array of flags
which will be pointed to by a next attribute, and it will be <font color="#f79646">incremented</font> as [[threads]] get their turn.

![[Array_Lock_IMG.png]]

Each thread will get a unique number and that number will go up by one.



```java
class ALock implements Lock {
	 boolean[] flags={true,false,...,false};
	 AtomicInteger next = new AtomicInteger(0);
	 ThreadLocal<Integer> mySlot; 
}
```



[[ThreadLocals]] in java


ALock implementation
```java
class ALock implements Lock {
	 boolean[] flags={true,false,...,false};
	 AtomicInteger next = new AtomicInteger(0);
	 ThreadLocal<Integer> mySlot;
	 void lock() {
		 mySlot = next.getAndIncrement();
		 while (!flags[mySlot]) {};
		 flags[mySlot] = false;
	 }
	 void unlock() {
		 flags[(mySlot+1)] = true;
	 } 
 }
```


This doesn't work because it violates the [[Java Memory Model]]. There are no [[volatile]]s here.

If we assume that every flag in the boolean flags array is volatile, it would still not work because of TAS-like performance. 