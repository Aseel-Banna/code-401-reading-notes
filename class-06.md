# Object-Oriented Programming Concepts

### Classes
- Classes are created to hold all mutual attributes and then objects are created.
- When we have many individual objects that shared same kind, classes need to be implemented.
- The objects will be instances from the original class.
- Classes can contain methods related to the objects and the instance of the class can access these methods.

### Objects
* All real world objects have state and behavior.
* State can be something related to them but static like their names, colors, ...etc.
* Behavior can be something related to them but dynamic like their functionality.
* An object stores its state in fields which are variables and access their behavior by methods.
* Data Encapsulation: to hide internal state and requiring all interaction to be performed through an object's methods.
* The advantages of using objects:
  * Modularity: Once object created, it can be easily passed around inside the system.
  * Information-hiding: Object's methods, the details of its internal implementation remain hidden from the outside world.
  * Code re-use: Allows developers to implement,test or debug complex, task-specific objects, which you can then trust to run in your own code.

### Inheritance 
- When different kinds of objects often have a certain amount in common with each other, we used inheritance.
- We have a class, called parent class, and it has all mutual attributes, and when we want to create an class that has the same attribute or methods and some other different attribute or methods, we can use the parent class by extend it in the new class, which is called child class.
- The child class can access all attributes in the parent class.

### Interface
- To hide certain details and only show the important details of an object, interfaces are used. 
- To implement this interface, the name of your class would change, and you'd use the implements keyword in the class declaration instead of extends.
- Implementing an interface allows a class to become more formal about the behavior it promises to provide
- Interfaces form a contract between the class and the outside world, and this contract is enforced at build time by the compiler.
- If your class claims to implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile.

### Package
- ***Package***: is a group of similar types of classes and interfaces.
- Packages are helpful because software written in the Java programming language can be composed of hundreds or thousands of individual classes.
- The Java platform provides an enormous class library (a set of packages) suitable for use in your own applications, which is called Application Programming Interface or API.


