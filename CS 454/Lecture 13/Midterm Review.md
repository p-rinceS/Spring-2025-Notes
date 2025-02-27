
Safety
- A safe lock is one where no two threads can ever get the lock.
- It is not possible to transfer more than the balance of the account.
- The sum of the balance between the two accounts remains constant.

Liveness
- All transfer methods eventually succeed or fail.


Properties of [[Mutual Exclusion]]

If two threads want the lock, the second thread can only get the lock after the first one has released the lock.


Deadlock freedom:
If a thread calls lock and never returns from the lock it is only if other threads are always getting the lock.

Bad things will happen if we call [[thread.stop()]]. It is deprecated, if we want threads to stop we need to utilize a flag and check whether or not that flag is set


[[linearizable]]


What is sequentially consistency?
Whatever we observe in program order in one thread is observed by all threads.

A happens before relationship means that:
if two actions ordered by a happens before relationship

If one action a happens before another action b.
Everything ordered before b happens before a