


Cannot be solved by Transient communication
Interrupts

It can be solved by One-bit shared variables (flags) that can be read or written.

A piece of code that "locks" a block of code, preventing other threads from accessing it until the lock is "unlocked" is called a ==mutex== (short for "mutual exclusion").

Formal Definition:

a "mutex" (mutual exclusion) is a specific implementation of a lock that guarantees only one thread can hold the lock at a time, essentially providing exclusive access to a shared resource