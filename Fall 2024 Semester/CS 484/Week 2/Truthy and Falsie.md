

Truthy/Falsie are values considered true or false in Boolean context.

Using == vs. ===

=== (Triple Equal)
	Checks for strict equality

== (Double Equal)
	Checks for Truthiness or Falsieness

e.g.

```
const a = 0
const b = ""


a == b
> true

a === b
> false

```