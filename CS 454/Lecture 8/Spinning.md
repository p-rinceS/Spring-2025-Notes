

In our class example, we see threads stuck in a while loop that does nothing, this is essentially spinning until it sees that a lock is not occupied by another thread to use it for itself.

 low level programming pattern whereby a thread will repeatedly check for some condition being met without being suspended.