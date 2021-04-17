# Spring MVC
- When you use Spring MVC application, @Controller classes are responsible for preparing a model map with data and selecting a view to be rendered.
- It allows you to complete abstraction of the view technology.

#### How it works?
1. Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes by using addAttributes method. 
2. Return ModelAndView with model attributes included.
3. Expose common attributes via methods annotated with @ModelAttribute.
4. messages attribute is added to the model and it will be available in Thymeleaf views.
5. These model attributes (or context variables in Thymeleaf jargon) can be accessed with the following syntax: ${attributeName}, where attributeName in our case is messages.


* ***Spring EL (Spring Expression Language)*** is a language that supports querying and manipulating an object graph at runtime.


Request Parameters:
1. Request parameters can be easily accessed in Thymeleaf views, and they can be passed from the client to server.
2. @Controller sends a redirect with a request parameter.

Session attributes:
Session attributes can be accessed by using #session, that gives you direct access to the javax.servlet.http.HttpSession object.

ServletContext attributes
The ServletContext attributes are shared between requests and sessions. In order to access ServletContext attributes in Thymeleaf you can use the #servletContext.

Spring beans
Thymeleaf allows accessing beans registered at the Spring Application Context with the @beanName syntax.

