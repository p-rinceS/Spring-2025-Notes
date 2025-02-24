
Question Notes:

1. How does your implementation ensure Property 3 (happens-before)? 
		My implementation ensures a happens-before relationship because of the use of the Atomic variables allows the state of the lock at any moment to be visible to all threads running. This allows other threads to know when a lock is locked and have to wait for an unlock to happen before being able to grab the lock. I've also implemented the highest precision sleep function as shown in class to force the thread to wait to try to see if the lock is unlocked.

2. Explain if your implementation is fair, starvation-free, or neither. See Property 2.
		 My implementation is not fair or starvation free, fairness implies that the threads trying to get the lock will get it in order of attempts, but since this is not a queue lock there is no order. And because we force the thread to spin, we don't guarantee that the thread will get the lock by waiting longer. However the implementation Is deadlock free, in this implementation when a lock is unlocked, some thread will try to grab it via the compareAndSet method.

3. Explain why your implementation of isReentered is as fast as possible.
			My implementation of isReentered is as fast as possible because it's a simple comparison on if the thread has entered the lock more than once. We also are reading from an Atomic Integer, and this does not require any sort of synchronization to be calculated. It is lock free.

4. Describe 2 steps you took to improve the performance of your implementation locking mechanisms under contention.
		 I used the highest precision sleep implementation shown in class to use an exponential back off mechanism. So instead of instantly retrying the thread's wait time will double to give the thread that is currently holding the lock to finish it's block of code.
		 The second step I took was to utilize an atomicInteger to count the number of reentries a thread attempts on a lock to avoid using unnecessary synchronization.  And because this 