

Design Pattern

- Manage incompatible interfaces between classes
	- For example, a wall plug in Europe has a different socket than in the US.
	- You put an adaptor in the middle and takes your plug and converts it to a design appropriate for European wall outlets.

![[Adapter Design Pattern Image.png]]

Sidesteps incompatibilities between interfaces and classes.


A adaptor maps the calls from an interface to a call that the Adaptee an understand so that it can understand the request.

Adaptee is a given, all requests usually end up there.