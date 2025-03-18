

#### Wait 
- Must be called holding the object's monitor (i.e., inside synchronized)
- Does not execute until another thread notifies the same object.
- ==Releases the monitor==
	

#### Notify 
- Must be called holding the object's monitor.
- Notifies one thread waiting.

#### Wait (after notify)
- Resumes execution
- ==Grabs the object monitor==




