
[[Singleton]] class uses private, static field to hold unique instance.

Singleton constructors declared private to prevent instance creation by clients.


Class defines public, static method getInstance() which either returns an existing instance or creates it if there isn't one.

Clients obtain instance with expression Singleton.getInstance().



![[Pasted image 20250122132055.png]]