# Android Fundamentals

* Android apps can be written using Kotlin, Java, and C++ languages.
* APK is an Android package that archives file with an .apk suffix that will be used with Android SDK to compile the code.
* One APK file contains all the contents of an Android app and is the file that Android-powered devices use to install the app.
* There is a security sandbox for each Android app that is protected by:
  * The Android operating system
  * Permissions that the system sets for all the files in an app so that only the user ID assigned to that app can access them.
  * Virtual machine (VM).
* The Android system implements the principle of least privilege: 
  * Each app, by default, has access only to the components that it requires to do its work and no more.
  * This creates a very secure environment in which an app cannot access parts of the system for which it is not given permission.
  * However, there are ways for an app to share data with other apps and for an app to access system services:
     * It's possible to arrange for two apps to share the same Linux user ID, in which case they are able to access each other's files. 
     * An app can request permission to access device data such as the device's location, camera, and Bluetooth connection.
* There are four different types of app components:
  * Activities: are the entry point for interacting with the user
  An activity facilitates the following key interactions between system and app:
    * Keeping track of what the user currently cares about (what is on screen) to ensure that the system keeps running the process that is hosting the activity.
    * Knowing that previously used processes contain things the user may return to (stopped activities), and thus more highly prioritize keeping those processes around.
    * Helping the app handle having its process killed so the user can return to activities with their previous state restored.
    * Providing a way for apps to implement user flows between each other, and for the system to coordinate these flows.
  * Services: are the component that runs in the background to perform long-running operations or to perform work for remote processes.
  * Broadcast receivers: are the component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements. 
  * Content providers: manage a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access. 

* Android apps don't have a single entry point (there's no main() function). 
* Because the system runs each app in a separate process with file permissions that restrict access to other apps, your app cannot directly activate a component from another app.
* An intent is created with an Intent object, which defines a message to activate either a specific component (explicit intent) or a specific type of component (implicit intent).
* For broadcast receivers, the intent simply defines the announcement being broadcast. For example, a broadcast to indicate the device battery is low includes only a known action string that indicates battery is low.
* You can start an activity or give it something new to do by passing an Intent to startActivity() or startActivityForResult()
* You can use the JobScheduler class to schedule actions. 
* You can initiate a broadcast by passing an Intent to methods such as sendBroadcast(), sendOrderedBroadcast(), or sendStickyBroadcast().
* You can perform a query to a content provider by calling query() on a ContentResolver.

* AndroidManifest.xml can be used to:
  * Identify any user permissions the app requires, such as Internet access or read-access to the user's contacts.
  * Declare the minimum API Level required by the app, based on which APIs the app uses.
  * Declare hardware and software features used or required by the app, such as a camera, bluetooth services, or a multitouch screen.
  * Declare API libraries the app needs to be linked against (other than the Android framework APIs), such as the Google Maps library.

* An Android app is composed of more than just code—it requires resources that are separate from the source code, such as images, audio files, and anything relating to the visual presentation of the app. 
* For every resource that you include in your Android project, the SDK build tools define a unique integer ID, which you can use to reference the resource from your app code or from other resources defined in XML.
* One of the most important aspects of providing resources separate from your source code is the ability to provide alternative resources for different device configurations.
* The qualifier is a short string that you include in the name of your resource directories in order to define the device configuration for which those resources should be used.
