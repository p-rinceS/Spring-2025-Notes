


Concurrent programming with Lists


# List [[Invariant]]s

#### Properties
1. The list contains two sentinel nodes
2. The tail sentinel is reachable from head sentinel
3. List is sorted
4. The list doesn't contain duplicates


e.g., An empty list already satisfies these properties



# Sequential List Set





### [[Coarse-Grained Locking]]

This implementation is linearizable and thread-safe.
	The only issue is it is slow when many threads are running.




### [[Fine-Grained Lock]]


