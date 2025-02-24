Messaging object that allows one app component ([[activity]], service, or [[Broadcast Receivers]]) to request an action from another component


Acts as away to communicate between different parts of the app.


An [[intent extra]] is extra data for the intent.
The format of this data consists of key value pairs.


### Structure of an Intent
##### Primary pieces of an intent are:

<font color="#c0504d">Action</font>: The general action to be performed such as:
- ACTION_VIEW
- ACTION_EDIT
- ACTION_MAIN
- ...
<font color="#c0504d">Data</font>: 
- The data to be operated on such as a person record in contacts database, expressed as a `Uri`.


