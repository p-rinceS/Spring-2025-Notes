

```java

class TASlock {
	AtomicBoolean state = new AtomicBoolean(false);
	void lock() {
		while(!state.getAndSet()){
			
		}
	}
	void unlock() {
		state.set(false);
	}

}
```


This "works" meaning it allows one thread to get a lock at a time, but it is useless synchronized [[threads]] 


This is our basic lock that works currently.

## Space complexity
- Very small memory footprint
- N threads require only O(1) space.
	- Filter/bakery required O(n) space


```cpp
class TTASlock {
	 AtomicBoolean state = new AtomicBoolean(false);
	 void lock() {
		 while (true) {
			 while (state.get()) {}
			 
			 if (state.getAndSet(true)) return;
	 }
}

```

## Test-and-Test-and-Set [[lock]]


* NOTE: linter will complain about the while loop but it works.

- This causes each cache to loop through their own local cache. And as soon as the test & set lock gets released then everyone will try and get the lock and then they will spin in that loop again.

#### This makes things better but it can still be improved upon

* To make it faster we make it slow on purpose.

- We need to detect [[contention]]

If the lock looks free and the thread fails to get it, it means there is a lot of contention.



### [[Exponential Backoff]]


```java
public class Backoff implements Lock {
	 public void lock() {
		 int delay = MIN_DELAY;
			 while (true) {
				 while (state.get()) {}
				 if (!lock.getAndSet(true))
					 return;
				 sleep(random() % delay);
				 if (delay < MAX_DELAY)
					 delay = 2 * delay;
			}
		}
	}
```


Backoff locks are **good**
**PROS**:
- They are easy to implement, beats TTAS lock & gets closer to ideal.
**CONS**:
- Must choose parameters carefully
- Not portable across different platforms.
- Not fair [[Fairness]]
- One thread may [[starve]].