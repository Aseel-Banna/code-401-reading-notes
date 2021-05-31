# Cognito

* Amplify auth has a built-in support for Amazon Cognito
* Set up amplify auth:
  * Add this CLI `amplify add auth`
  * Enter the following when prompted:
    ? Do you want to use the default authentication and security configuration?</br>
    `Default configuration`</br>
    ? How do you want users to be able to sign in?</br>
    `Username`</br>
    ? Do you want to configure advanced settings?</br>
    `No, I am done.`</br>
  * Then enter this CLI `amplify push`
  * As usual, we have to add dependencies for our app to get libraries:
     * Add `implementation 'com.amplifyframework:aws-auth-cognito:1.17.4'` in dependencies part in build-gradle file
     * Add these two lines, to include the Auth plugin.
        `Amplify.addPlugin(new AWSCognitoAuthPlugin());`</br>
        `Amplify.configure(getApplicationContext());`</br>
     * Add this code in your onCreate method in MainActivity to make sure that your app is running: </br>
        `Amplify.Auth.fetchAuthSession(`
            ` result -> Log.i("AmplifyQuickstart", result.toString()),`
            ` error -> Log.e("AmplifyQuickstart", error.toString()));`
     * Then you have to set your username, password, ...etc.
* Every user has his/her own username and password, you can use this code to register a user:
  `AuthSignUpOptions options = AuthSignUpOptions.builder()`
  `  .userAttribute(AuthUserAttributeKey.email(), "my@email.com")`
   ` .build();`
`Amplify.Auth.signUp("username", "Password123", options,`
  `  result -> Log.i("AuthQuickStart", "Result: " + result.toString()),`
   ` error -> Log.e("AuthQuickStart", "Sign up failed", error)`
`);`

* These line of codes use to confirm the sign up operation
 `Amplify.Auth.confirmSignUp(`
   ` "username",`
   ` "the code you received via email",`
   ` result -> Log.i("AuthQuickstart", result.isSignUpComplete() ? "Confirm signUp succeeded" : "Confirm sign up not complete"),`
    `error -> Log.e("AuthQuickstart", error.toString())`
`);`

* If the operation is succeed, this will be shown in the console window
* These line of codes use to confirm the sign in operation
`Amplify.Auth.signIn(`
    `"username",`
    ` "password",`
   ` result -> Log.i("AuthQuickstart", result.isSignInComplete() ? "Sign in succeeded" : "Sign in not complete"),`
   ` error -> Log.e("AuthQuickstart", error.toString())`
`);`
* If the operation is succeed, this will be shown in the console window too.

