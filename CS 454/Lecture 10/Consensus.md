

### Atomic Instructions

1. Volatile
2. AtomicBoolean.getAndSet
3. AtomicInteger.getAndIncrement
4. AtomicReference.compareAndSwap


Which one is more powerful

2, 3 are equal and more powerful than 1 and less than 4.



### Consensus Problem
1) Each thread proposes one value
2) All threads comunicate
3) All threads decide
	- The same vlaue
	- Can be any of the values
	- Must be one of the proposed values



### Why consensus matters
- Most problems when developing a concurrent algorithm can boil down to consensus.
- Important to understand the limitations of consensus
	- What do we need to achieve consensus between 2 
- We can measure relative power of synchronization primitives