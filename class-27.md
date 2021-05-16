# Intents, Activities, and SharedPreferences

* A task is a collection of activities.
* The activities are starting when the user opens the application until he/she finishes the using of the app.
* The moving between activities pushed into back stack.
* Once the user finished a certain task, it is popped from the stack.
* If the user continues to press back button, it will back to the previous activity until it reaches the home page or main activity with dropping each activity from stack.
* If the user is in the home page and presses back, so all activities will be dropped from the back stack and at the end the task will be no longer exists.
* User can use multi apps. If the user is in an app and then press the home button, the activity will be paused until the user closes it or return to it. And user can open another app during this journey, and it works as I mentioned before.
* The activities in stack are last-in first-out.
* Activity can be declared in a manifest file by specifying how the activity should associate with tasks when it starts.
* Also, using Intent and startActivity() can be used to declare an activity too.
* The launchMode attribute in a manifest file specifies an instruction on how the activity should be launched into a task.
* launchMode Values:
  * standard (the default mode):  The activity can be instantiated multiple times, each instance can belong to different tasks, and one task can have multiple instances.
  * singleTop: If an instance of the activity already exists at the top of the current task, the system routes the intent to that instance through a call to its onNewIntent() method, rather than creating a new instance of the activity. 
  * singleTask: The system creates a new task and instantiates the activity at the root of the new task. 
  * singleInstance: The system creates a new task and instantiates the activity at the root of the new task, but the system doesn't launch any other activities into the task holding the instance.

* The flags you can use to modify the default behavior when starting a new activity are:
  * FLAG_ACTIVITY_NEW_TASK
  * FLAG_ACTIVITY_SINGLE_TOP
  * FLAG_ACTIVITY_CLEAR_TOP

* The taskAffinity attribute takes a string value, which must be unique from the default package name declared in the <manifest> element, because the system uses that name to identify the default task affinity for the app.
* If the user leaves a task for a long time, the system clears the task of all activities except the root activity. 
* You can set up an activity as the entry point for a task by giving it an intent filter with "android.intent.action.MAIN" as the specified action and "android.intent.category.LAUNCHER" as the specified category.


## Save key-value data
* If you want to save values you should use SharedPreferences.
* Calling one of these methods creates a SharedPreferences:
  * getSharedPreferences(): it is used if you need multiple shared preference files identified by name, and you can call this from any Context in your app.
  * getPreferences(): ypu can use this method from an Activity if you need to use only one shared preference file for the activity. 
* To write to a shared preferences file, create a SharedPreferences.Editor by calling edit() on your SharedPreferences.

