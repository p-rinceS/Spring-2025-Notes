




### Assignment 2 Hints
All locks are [[linearizable]]


In assignment two you need to make sure there is a point where the lock is completely unlocked.


Returning from the lock means -> "We got the lock"
- Method lock should block for as long as needed
- Keep in mind that a thread may fail to get the lock many times in a row

Due this Saturday at 5pm.

### Midterm:
March 4:
	(In person, during class)
	Midterm topics & sample midterm solved in class next week



### Recap
[[Fast Path]]
[[Java Memory Model]]


Fast Path Queue Lock
- CAS(F_U, F_L) -> will return F_U if we get the lock

[[TASLock]] 


### Types of Java Locks

- Monitor of most objects in java will never be used.
- The hash-code of most objects will also never be used.

- Consequence for the common case
	- Optimize for either lock or hash-code



### Lock usage frequency

1. No lock is used for an object
2. Locking an unlocked object
3. ...



We know a object is not locked if it has a 1 or 0, epoch is used to keep track of reentered locks.


