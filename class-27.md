# Intents, Activities, and SharedPreferences

* A task is a collection of activities.
* The activities are stored in a back-stack. When a user starts to use an app, the activities are starting and push the current activity to the stack. Once the user finishes using the activity and moves to another one, the current activity will be popped from the stack and the new one will be pushed into the stack.
* If the user continues to press back button, it will continue backing to the previous activity until it reaches the home page or main activity with dropping each activity from stack.
* When the user is in the home page, the stack has only the home activity. Once the user presses back button, the home activity will be dropped from the back stack and at the end the task will be no longer exists.
* User can use multi apps in same time. If the user is in an app and then press the home button, the activity will be paused until the user closes it or return to it. If the user open another app during this journey, another stack will be declared to holds the new activity and the previous one will be paused.  
* lunchMode attribute gives instruction how the app is running.

* launchMode Values:
  * standard (the default mode).
  * singleTop. 
  * singleTask. 
  * singleInstance.

* The flags you can use to modify the default behavior when starting a new activity are:
  * FLAG_ACTIVITY_NEW_TASK
  * FLAG_ACTIVITY_SINGLE_TOP
  * FLAG_ACTIVITY_CLEAR_TOP

* In manifest file, you can decide which activity should be the first one to execute when the app is running.


## Save key-value data
* SharedPreferences is one of the ways that is used to save data.
* Calling one of these methods creates a SharedPreferences:
  * getSharedPreferences(): that it is used if you need multiple shared preference files identified by name.
  * getPreferences(): that is used if you need to use only one shared preference file for the activity. 
* To write to a shared preferences file, create a SharedPreferences.Editor by calling edit() on your SharedPreferences.

