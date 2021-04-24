# Spring Security Architecture

- Authentication: Who are you
- Authorization: What are you allowed to do
- Spring Security has an architecture that is designed to separate authentication from authorization and has strategies and extension points for both.
- AuthenticationException is a runtime exception and it is usually handled by an application in a generic way, depending on the style or purpose of the application. User code is not normally expected to catch and handle it. 
- Spring Security provides some configuration helpers to quickly get common authentication manager features set up in your application.
- Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters, so it is helpful to first look at the role of Filters generally. 
- The client sends a request to the application, and the container decides which filters and which servlet apply to it based on the path of the request URI.
- One servlet can handle a single request, but filters form a chain, so they are ordered. 
- A filter can veto the rest of the chain if it wants to handle the request itself.
- A filter can also modify the request or the response used in the downstream filters and servlet.
- If you use the Spring Boot Actuator for management endpoints, you probably want them to be secure, and, by default, they are.
- As soon as you add the Actuator to a secure application, you get an additional filter chain that applies only to the actuator endpoints. 
- If you want your application security rules to apply to the actuator endpoints, you can add a filter chain that is ordered earlier than the actuator one and that has a request matcher that includes all actuator endpoints.
