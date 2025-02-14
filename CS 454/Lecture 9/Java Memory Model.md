

The **JMM** defines how threads interact with memory and how changes made by one thread become visible to others.

In concurrent programming, multiple threads read/write shared memory. If we don't enforce proper [[synchronization]] they might see stale or inconsistent values.

