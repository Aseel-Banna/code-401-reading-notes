# Kinesis & Analytics

* The Analytics category enables you to collect analytics data for your App.
* The Analytics category comes with built-in support for Amazon Pinpoint and Amazon Kinesis 
* To set up analytics backend:
  * CLI: amplify add analytics
  * Then push using amplify push
  * Then add the dependencies:
     * implementation 'com.amplifyframework:aws-analytics-pinpoint:1.17.8'
     * implementation 'com.amplifyframework:aws-auth-cognito:1.17.8'
  * To initialize the Amplify Auth and Analytics categories you call Amplify.addPlugin() in onCreate() method.
  * To record an event, create an AnalyticsEvent and call Amplify.Analytics.recordEvent() to send it
  * From the terminal run the following command. Navigate to the Analytics tab, and then choose View in Pinpoint.
     * amplify console analytics<br>

[Set up Analytics backend](https://docs.amplify.aws/lib/analytics/getting-started/q/platform/android)

