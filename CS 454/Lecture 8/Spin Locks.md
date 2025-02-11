


### [[Mutual Exclusion]]

What to do if you cannot get a cannot get a lock?

1) Keep Trying
	1) AKA [[Spinning]] or Busy-waiting
2) Give up the CPU until lock is ready


If we were were using a uniprocessor system:
3) Give up the CPU until the lock is ready
	1) AKA Yield


### [[Spin Locks]]

One thread will have the lock and the other two will keep spinning until they get the lock.


### Sequential Bottlenecks

```cpp
Lock l;
int c = 0;
// N threads
// Each thread does:
for (int i = 0 ; i < 10_000_000/N ; i++) {
	 l.lock();
	 c += 1; // Single Threaded
	 l.unlock();
}
```


We shouldn't see our performance get worse since it's a [[Single-Threaded]] process.

Our lock will suffer from **[[contention]]**.


Increments per second (higher is better)
Time to Increment (lower is better)


```cpp

class BooleanLock {
	 boolean state = false;
	 void lock() {
	 while (state) {}
		 state = true;
	 }
	 void unlock() {
		 state = false;
 }
}
```


$T1 \longrightarrow T2$

$T1 \longrightarrow T2$


This won't work because state needs to be [[volatile]].
but making it volatile won't help us because it because we run into the same problem where two threads get the [[lock]]
