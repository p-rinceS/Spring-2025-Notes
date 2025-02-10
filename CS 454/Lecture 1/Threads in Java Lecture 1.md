## Option 1:

1) Extend the thread class
2) Override the run method


Can start threads by creating a thread and using the start() method


```Java

Thread t = new myThread().start();
```

Pros: Easy to reuse code to start many threads.
Cons: Interferes with class inheritance



## Option 2:
	Implement interface java.lang.Runnable

```Java
public classMyRunnable implements Runnable {
	public void run() { ...}
}
```

## Option 3: 

Anonymous inner clsas

Cons: cannot reuse code

## Option 4:
[[Java 8+ Lambdas]]

``` Java
new Thread (() -> { ... })
```



Join vs Stop

[[`Thread.Join()`]] allows us to wait for a thread.
[[`Thread.Interrupt()`]] does not stop a thread
`Thread.Stop()` does stop a thread but it's not good practice
	When using thread.stop(), it is not good because it can result in hanging if you start two threads and stops one of them. Is **deprecated**

We need to implement extra logic to make threads return from their function.


### Java Keyword: Synchronize

The `synchronized` keyword will


Thread.stop is Deprecated because stopping a thread causes it to unlock all the monitors that it has locked

Safely stopping threads

1) We need a flag
2) We need to check if stop is true
3) Between checks we need to do whatever we want the thread to do.
4) We set Stop flag to true to stop the thread. (need a new stop flag per thread to handle multiple stops at different times.
Threads inside a CPU:
	Threads live in general purpose registers that our compiler uses for us to do some computation


## [[Hyper-Threading]]

- Duplicated number of registers

Sometimes the overhead of one thread waiting for the other, it can be less efficient
Which is why the threads running concurrently it is better


[[NUMA Topology]]


Symmetric Multi Processing (SMP) :


Granularity of a Cache:
	1 word (has 32-64 bits)
	Few Words(2, 8 words)


[[Cache Coherence]]


Locking a thread is an atomic instruction, the more atomic instructions I have, the slower you make your entire programming.
The more Cache Coherence traffic you have, the slower everyone gets.

[[Mesi Protocol]]
