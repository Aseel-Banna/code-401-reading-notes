# API (GRAPHQL)

* Serverless: it is a cloud computing execution model that could manage the distribution and the providing of severs.
* Using cloud providers in serverless make a lot of money
![img](https://hackernoon.com/hn-images/1*t4O4UXpdG68MQboNKC6bBw.jpeg)

### Traditional vs. Serverless Architecture
![img](https://hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg)

* The benefits of using serverless:
  * It is reduce cost
  * Setting up environments are easy

* The disadvantages of using serverless:
  * you cannot directly access APIs through the usual IP, because serverless functions are accessed only as private APIs. 
  * unusable for applications that have variable execution times
  

* If your context's of project is simple use serverless, else use traditional architecture.
* Faas is an implementing for serverless that can use to deploy individual functions or a piece of business logic.

* Principles of FaaS:
  * Complete management of servers
  * Invocation based billing
  * Event-driven and instantaneously scalable

* With Serverless, everything is stateless

The serverless app
![img](https://hackernoon.com/hn-images/1*TIrjN7EjLUVJmJ6YvHR7Dg.png)


## AWS Amplify
* AWS Amplify is a set of tools and services that can be used to build a scalable full-stack apps.
### AWS Amplify Advantages
  * the project can be connected to backend easily.
  * deploy static web apps in a few clicks
  * easily manage app content outside the AWS console

## Add relationships between types
* To define relationship between models, we have to use @connection
* many-to-many relationship can be defined using two one-to-many relations, an @key, and a joining @model.
* fields argument is used to queried by to get connected objects.
* A Has One @connection can only reference the primary index of a model
* Set the limit argument to define the number of nested objects, which is by default 100.
