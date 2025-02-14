

A **NUMA** machine is a type of multiprocessor system where memory access time depends on memory location relative to the processor.


Spinning on remote memory is very slow 
Spinning on local memory is very fast

### Locks for NUMA Machines

MCS Lock
	- Modified Queue lock that ensures we only spin in local memory
	- Described in detail in the book
		- (Out of the scope of the course)
	- CLH Queue lock is not perfect
		- 