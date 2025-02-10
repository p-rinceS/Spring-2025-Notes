


## no main() method

## App Structure
- Set of components
- Four kinds of components:
	- Activities
		- Components that manage the display of an app.
		- Responsible for painting the interface
	- [[Broadcast Receivers]]
		- Listeners
		- May or may not be running
		- If there are global listeners
			- For example: Battle Power is low
	- [[Content Providers]]
		- Shares persistent data among multiple apps
	- Services
		- Long running actions and background actions.

Components define methods the OD calls in response to user actions.
 > Activities define methods onCreate(), onStart(), onStop(), etc.
 > Services define methods onCreate(), onStartCommand(), onBind(), etc.

==*You have to strictly follow the rules of the Operating System when writing code.*==


 