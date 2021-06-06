# Intent Filters

* Intent filter is a property that used in your app to allow other apps use a feature of your app.
* It is added in the manifest file if you want to use it
* When your app is installed on a device, the system identifies your intent filters and adds the information to an internal catalog of intents supported by all installed apps. 
* To add an intent filter, you have to specify the following:
  * Action: it is a string that handle the name of the action that should be performed.
  * Data: describe the data in your intent.
  * Category: characterize the activity handling the intent.

* In order to decide what action to take in your activity, you can read the Intent that was used to start it.
