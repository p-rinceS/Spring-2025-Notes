

Sometimes predefined adapters don't work well for your list items
- Grid view example: Arrange pictures in rows and columns
- Adapter must "squeeze" a set of image files into grid tiles


Defining your adapter, e.g., *MyAdapter*

1. Define MyAdapter to extend abstract superclass BaseAdapter
2. Define following methods (at least):
	- [[getView()]]
	- [[getItemId()]]
	- [[getCount()]]


## Predefined adapter hierarchy
- Interface Adapter which is a base class to define your own adapter
- Extend interface BaseAdapter
	- Already the base class for 
		- [[ArrayAdapter]]
		- SimpleAdapter
		- Abstract CursorAdapter
		- Abstract ResourceCursorAdapter


onCreate() method: Place resources in ArrayList\<integer\>
- Pass list to the adapter instance which will save the list in appropriate field
- Attach adapter to GridView 
- Define listener


Reminder of what an [[Intent]] is