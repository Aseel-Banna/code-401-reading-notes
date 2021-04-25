# Spring Boot and OAuth2

* There are several samples building on each other, adding new features at each step:

  * simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties (if you visit the home page, you will be automatically redirected to GitHub).

  * click: adds an explicit link that the user has to click to login.

  * logout: adds a logout link as well for authenticated users.

  * two-providers: adds a second login provider so the user can choose on the home page which one to use.

  * custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.

* Each app can be imported into an IDE.
* The apps all work on localhost:8080 because they’ll use OAuth 2.0 clients registered with GitHub and Google for that address.

* How to Single Sign On With GitHub
1. Creating a New Project
2. Add a Home Page
3. Securing the Application with GitHub and Spring Security to make the application secure.
4. Add a New GitHub app
5. Configure application.yml
6. Boot up the application

* You can use logout as an endpoint and CSRF Token in the Client.

Login with GitHub
1. Initial setup
2. Setting the redirect URI
3. Adding the Client Registration
4. Adding the Login Link

* The main theme running through all of the samples is authentication using an external OAuth 2.0 provider.
* All of the sample apps can be easily extended and re-configured for more specific use cases, usually with nothing more than a configuration file change. 