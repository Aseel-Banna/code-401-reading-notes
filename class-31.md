# Android Tests

* Espresso is used to test Android UI.
* Espresso tests are fast.
* Message queue has to be empty to run onView() method. Also, while the program is testing, the AsyncTask must have no instance to execute tasks.
* To use Espresso in testing, there are packages that should be used in the program:
  * espresso-core
  * espresso-web 
  * espresso-idling-resource
  * espresso-contrib
  * espresso-intents
  * espresso-remote

* To ease testing, there is a tool to record the teat scenario instead of writing code, it is called ***Espresso Test Recorder***, it is used Espresso Testing framework to write the test code.
* [How to record a test?](https://youtu.be/JRkDVvB106k)
* To use the tes recorder, turn off animations on your test device, because it might lead to unexpected results.
* [Set up the recorder](https://developer.android.com/training/testing/ui-testing/espresso-testing#setup)
* UI interactions and assertions are the main components of Espresso Test Recorder.
* [How to record UI interactions](https://developer.android.com/studio/test/espresso-test-recorder#record-ui-interactions)
* The assertion in tests can be text is, exists or does not exist.
* [add an assertion to your test](https://developer.android.com/studio/test/espresso-test-recorder#add-assertions-to-verify-ui-elements)
* Creating an assertion does not avoid you from interacting with your app.
* [How to save test record](https://developer.android.com/studio/test/espresso-test-recorder#save-a-recording)
* [How to run a record](https://developer.android.com/studio/test/espresso-test-recorder#run-an-espresso-test-locally)  