# Android Fundamentals

* There are languages that are using to implement Android app such as, kotlin, java and c++.
* APK is an Android package that archives file with an .apk suffix that will be used with Android SDK to compile the code.
* One APK file contains all the contents of an Android app and is the file that Android-powered devices use to install the app.
* An Android app can be protected by:
  * The Android operating system
  * Permissions that the system sets for all the files in an app so that only the user ID assigned to that app can access them.
  * Virtual machine (VM).

* The Android system implements the principle of least privilege: 
  * Each app can access only to the components that it requires to do its work to complete the work of the app, which means that the app cannot access any parts of the system even if it has a permission.

  * It is possible to share data from one app to another:

* There are four different types of app components:
  * Activities: each page of the app that the user can use and interact with.
  * Services: component that are used to perform operations.
  * Broadcast receivers: component deliver events to the app outside of a regular user flow and allowing the app to respond to system-wide broadcast announcements. 
  * Content providers: manage data that you can store. 

* Each activity has its onCreate() method and it will execute when the activity starts, so there is no main() method.
* Intent object can be used to move between activities by using startActivity() method or other methods. 
* You can use the JobScheduler class to schedule actions. 
* sendBroadcast(), sendOrderedBroadcast(), or sendStickyBroadcast() are methods are used to initiate a broadcast.
* You can perform a query to a content provider by calling query() on a ContentResolver.

* AndroidManifest.xml is a file that has the configuration of the app such as:
  * User permissions.
  * The API Level required by the app.
  * Hardware and software features.
  * API libraries the app needs to be linked to API.
 
* Every resource in your Android project has an Id that is defined by SDK build tools.
* The qualifier is a short string that you include in the name of your resource directories in order to define the device configuration for which those resources should be used.
