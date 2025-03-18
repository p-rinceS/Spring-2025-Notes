

1) Which operations can potentially violate property Progress 5, and what steps did you take to avoid that?
	- The operations that can potentially violate the property of avoiding deadlocks are boardBus, transferTickets, useTickets, and expireTickets. The steps we took to ensure this property holds was to create a ordering of locks. In the transfer tickets method locks are acquired in a order based on Bus IDs. We also use Fine-Grained Locks and separate these locks for different resources to reduce areas where we could have contention. We also used synchronized blocks to maintain consistency in the useTickets and expireTickets the status updates are synchronized on the depot Solution.



2) How do you ensure concurrent progress on operations that get the contents of the same bus (Progress 1. Concurrent getTickets operations should all make progress in parallel.)?
	* We allow concurrent getTickets operations by using ReadWriteLock which would let multiple threads aquire the read lock concurrently to allow parallel progress when reading the status and when writing to the bus contents it will acquire the write lock. We also use fine grained locking here to make sure that the read lock is only held for the time it is reading the bus contents.


3) How do you ensure linearizability when adding tickets to a bus and when using/expiring tickets (Linearizability 1 and 4)?
	-  To ensure linearizability when adding tickets we use locks to synchronize access to shared resources. For example when we go to the boardBus methods the adding to tickets to a bus is atomic and consistent. It uses a lock to synchronize access to the bus and ensures a happens before relationship where we are checking the status of the bus before adding them on the bus. So either all of the tickets are added or none at all. The use tickets and expire tickets are also atomic and use synchronized blocks where they are synchronized on the DepotSolution. The status of each ticket is checked before making any changes to make sure it's consistent.


4) (Bonus) How did you ensure that nonLinearStatus performs as described in this document?
	Faster Execution: nonLinearStatus avoids synchronization, making it faster than getStatus, which uses a synchronized block.
	Correctness Properties: While nonLinearStatus may not guarantee linearizability, it still provides a snapshot of the ticket's status, which can be useful in scenarios where strict consistency is not required.
	Linearizability 1 and 4: These properties may not hold for nonLinearStatus because it does not ensure atomicity and consistency across multiple threads