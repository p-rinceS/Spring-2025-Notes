
Part of the operating environment in which a process runs
Affects the way that a running process will behave
Introduced in Unix and adopted by Microsoft Windows 


Example PATH variable
			- When a program is executed, the shell process will use the environment variable to find where the program is if the full path is not provided.


## How to access Environment Variables


the command `env` will list every environment variable
Ways to call [[execve()]] using environment variables


There is a global environment variable call 
`extern char** environ`

![[Pasted image 20240903160425.png]]


Why do we need environment variables?
	- 

Attack Surface on Environment Variables
	- hidden usage of environment variables is dangerous
	- Since users can set environment variables, they become part of the attack surface on setUID programs.


