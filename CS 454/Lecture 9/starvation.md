
Happens when a thread waits indefinitely because other threads keep taking priority. This can be avoided using a [[Queue Lock (CLH)]] which fairly gives threads a chance to grab the lock.


It usually occurs when system resources (CPU time, locks, etc.) are allocated unfairly. 


Starvation can be prevented using fair locks, fair resource allocation, or increasing priority of waiting locks.

