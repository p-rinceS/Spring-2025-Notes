


[[Control Flow Hijacking]]
[[Writing Shell Code]]


[[Week 3 - Secure Computer Systems]]


Invoking Programs
	- Invoking external commmands from inside a program
		- Use the system() library function.

```C
int main() {
	system("ls");
}
```

Invoking Programs: Unsafe Approach
	**Problem**: Some part of the data becomes code (command name)



Let's say we pass a formatted string  to a variable called command and pass it as a parameter to system()

```C
int main() {

sprintf("%s %s") ...
system(command);
}
```


```C
system("cat aa/bin/sh");
```


## Invoking Programs Safely:

Using [[execve()]]


[[Principle of Isolation]]
[[Principle of Least Privilege]]


## [[Environment Variables]]
- Set of dynamic named values



Attacks via [[Dynamic Linker]]: Case Study

- Program calls sleep function which is dynamically linked
```C
int main()
{
sleep(1);// sleep for one second
return 0;
}
```

Another sleep() function can be implemented called:

```C
void sleep(int s)
{
	printf("not sleeping");
}
```

[[LD_PRELOAD]] is a file that contains lists of libraries that the linker searches first, and it can be edited by Users, it allows them to control the outcome of the linking process.

If the program was a SetUID program it may lead to security breaches


Countermeasures
	- Normal-User Process
	- Privileged Process
		- Conducts privileged operations for users
		- service approach



