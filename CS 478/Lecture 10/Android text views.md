


Specific Type of [View](views)

Root of heirarchy is class **TextView**

- Not editable by default; change with android:inputType="text" or use subsclass *EditText*

Rich API allows user to define fonts, colors, sizes, backgrounds for text box.

### Key methods:

getText() --- Returns a CharSequence
setText(String someString) --- Overloaded, use with String arg.


Declaring a TextView in XML

```xml
<TextView android:id = "@+id/text2"
		  android:layout_width = "wrap_content" 
		  android:layout_height = "wrap_content"
		  android:text = "This is a text view!" /> 

```

Imagine the above was wrapped in a `<LinearLayout> ... </LinearLayout>`



### TextView's Heirarchy

- CompoundButtons - ([[Abstract Class]] )button subclass with "unchecked" and "checked" states (implements Checkable interface and toggle() method)
-