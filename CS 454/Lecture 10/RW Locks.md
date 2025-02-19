


Shared Counter


```java
int counter;

int read() {
	return counter
}

void synchronized inc() {
	counter += 1;
}
```


The counter cannot be observed to go back
but we can suffer from data races (visibility)

we need to make the counter [[volatile]] so other threads can see the changes to counter.



```java
int counter
Lock l;

int read() {
	return counter;

}

void inc() {

counter += 1;
}


```



This implementation will force them to wait for the read to finish and the n
```java
```java
int counter
Lock l;

int read() {
l.locK()
try {	return counter;}
finally {l.unlock();}

}

void inc() {
l.lock()
try {
counter += 1;
}
finally {l.unlock();}
}
```


## Readers-Writers Lock

Implementing Read-Write Locks
- Requires more sophisticated thread communication than we have seen
- We'll come back to this after the midterm
- You don't need to know how to build one to be able to use one


Who gets preference: Readers or Writers?
