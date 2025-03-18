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



##### Formal Def

- An intent is a messaging object which tells us what kind of actions need to be performed. The intent's most significant use is the launching of an [[activity]]. An intent is a passive data structure holding an abstract description of an action to be performed.