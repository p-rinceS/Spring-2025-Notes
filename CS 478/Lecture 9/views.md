
*View* is the root of UI-element class hierarchy.
Each **view instance** is associated with rectangular portion of display


Main responsibilities of *View* and it's subclasses
- Know how to draw instances
- Knowing instance position in the window displaying instance
- Intercepting + responding to user interactions (e.g. button press)
- Container views only: adding/accessing/removing children views.


A view is a subclass of Java root class *Object*

 -> TextView
 -> ImageView
 -> KeyboardView
 -> ProgressBar
 -> ViewGroup
	 - Set of views ([[composite pattern]])
	 - Subclasses include most layouts (LinearLayout, RelativeLayout, DrawerLayout, etc.)

