
Turn array into list
	- Retain fairness / FIFO order 
	- Small, constant overhead per thread


Ensures fairness in concurrent programming by maintaining a queue of threads or processes waiting for a lock. 

When a thread requests a lock that is held by another thread or process it is placed in a queue and waits for it's turn. This prevents [[starvation]].



Queue Lock Initial State

``` mermaid
flowchart TD
tail --> A
```


[[Compare And Swap]]:
 - If successful returns OLD value
 - if unsuccessful, returns NEW value.

Queue Lock Release



[[Queue Lock (CLH)]] violates the [[Java Memory Model]] because the JMM doesn't guarentee that one thread's updates are immediately visible to other threads unless explicit memory synchronization like volatile or synchronized are used.



## CLH Queue Pros & Cons

Good:
	Lock releases only affect one thread.
	Fair
	Small constant-size space
Bad:
	Does not work on[[ NUMA Machines]]
	Speed: Acquiring lock requires allocating memory.

