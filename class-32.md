# Serverless and Amplify

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

## GraphQL
* The GraphQL Transform used to help you quickly create backend for web and mobile applications on AWS.
* GraphQL Schema Definition Language (SDL) is used to define application’s data model 
* The library handles converting SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data model.
[See this documentation](https://docs.amplify.aws/cli/graphql-transformer/overview#create-a-graphql-api)
