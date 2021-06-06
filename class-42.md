# Locations 
* There is a Google Play service that allow you to request the last known location of the user's device.
* Google Play is using APIs to provide location suh as ***The Fused Location Provider***.
* The fused location provider benefits: 
  * It manages the underlying location technology.
  * It provides a simple API so that you can specify requirements at a high level.
  * It also optimizes the device's use of battery power.

* Steps for creating location service client:
  * Set up Google Play services: Download and install the Google Play services component via the SDK Manager and add the library to your project. 
  [Setting Up Google Play Services](https://developer.android.com/google/play-services/setup)
  * Specify app permissions: The app must request location permissions.
  [Request Location Permissions](https://developer.android.com/training/location/permissions)
  * Create location services client: Create an instance of the Fused Location Provider Client
  [Create location services client](https://developer.android.com/training/location/retrieve-current#play-services)
  * Get the last known location: 
  [Get the last known location](https://developer.android.com/training/location/retrieve-current#last-known)
    * The location object may be null in the following situations:
       * Location is turned off in the device settings.
       * The device never recorded its location.
       * Google Play services on the device has restarted.
  * Maintain a current best estimate
  [Maintain a current best estimate](https://developer.android.com/training/location/retrieve-current#BestEstimate)