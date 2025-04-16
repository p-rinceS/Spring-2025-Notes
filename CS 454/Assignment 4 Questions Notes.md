
1) How do you avoid busy-waiting in your implementation'
	We avoid busy-waiting in this implementation by using the wait-notify. getAction method in BusSolution uses wait to pause the thread and when the action linked list is empty instead of busy waiting in a while loop. When a new action is added with the submitAction method,  we use notifyAll() to unpause the waiting threads. We also combine the results in some of our operations like transferTickets and getTicketsAsync to limit the amount that the threads wait. Instead of constantly waiting for the threads every time we are submitting an action, it will all happen concurrently and will only wait once.

2) Is it correct to modify bus.contents using an operation that does not create an inter-thread happens-before relationship with reading it? Why?

	**No, it is not correct to modify `bus.contents` using an operation that does not create an inter-thread happens-before relationship before reading it.**  
	This is because without a happens-before relationship, there is **no guarantee that a thread reading `bus.contents` will see the most recent updates made by another thread**. You can see how we did this in our solution by looking at the submitAction and getAction methods which have synchronized blocks to make sure that modifications to the actions list is visible When a thread adds an action to the list it will establish happens before relationship with any next thread that reads from the list.

3) How do you ensure that a failing transfer operation does not result in tickets being lost?
	 We do the same combining of results similar to how we do this in getTicketsAsync() and in the introductory video. We have a retry system in place which is the while loop and if the move out or move in operations fail we will retry until the tickets are either properly moved into the correct bus or transferred back to it's original bus. This implementation also handles every possible outcome of the move out and move in operations this will make sure that tickets are either fully transferred, or moved back to it's original bus.
36:12