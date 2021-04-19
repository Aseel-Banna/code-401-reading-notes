# Related Resources and Integration Testing

#### One-to-One Relationship
- The Data Model using @OneToOne
- The @RestResource annotation is optional and can be used to customize the endpoint.
- The Repositories extending the CrudRepository interface
- Creating the Associations so, we can establish the relationship by using one of the association resources.


#### One-to-Many Relationship
- The Data Model using @OneToMany

#### Many-to-Many Relationship
- The Data Model using @ManyToMany

#### Testing the Endpoints With TestRestTemplate
Define @Test method that saves objects by making POST requests to the collection resources. Then it saves the relationship with a PUT request to the association resource and verifies that it has been established with a GET request to the same resource.

## Integration Testing in Spring
- We will need junit-jupiter-engine, junit-jupiter-api, and Spring test dependencies.
- Enable Spring in Tests with JUnit 5 by adding the @ExtendWith annotation to our test classes and specifying the extension class to load.
- We also need the @ContextConfiguration annotation to load the context configuration and bootstrap the context that our test will use.
- The WebApplicationContext Object which provides a web application configuration. It loads all the application beans and controllers into the context.
- Mocking Web Context Beans encapsulates all web application beans and makes them available for testing.
- Also, send GET and POST requests with variations of parameter passing and how to verify the HTTP response status, header, and content.
