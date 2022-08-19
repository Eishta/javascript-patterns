# javascript-patterns

#### What is a pattern?
Design patterns are commonly used solutions to common software development problems.

#### Anti-pattern 
Like changing the Object prototype is an anti-pattern. It will affect all the object in your code

#### Categories
1. Creational design patterns
* * This patterns deal with object creation on a more optimized way than the basic object creation. 
2. Structural design patterns
* * These patterns work with relations between objects. They guarantee that if a system’s part change, nothing else has to change with it.
3. Behavioral design patterns
* * This kind of pattern acknowledge, implement and improve communication between objects of the system.
4. Concurrency design patterns
* * When you are dealing with multi threading programming these are the patterns that you will want to use.
5. Architectural design patterns
* * Design patterns that are used on the system’s architecture, like MVC or MVVM.

##### Creational 
1. Constructor 
* * allows to create objects using Classes  with constructors 
* * also can be created using constructor functions
* * make use of the prototype property to add the methods to be shared among all object instances

2. Module 
* * makes use of closures to encapsulate the private and public properties
* * only a public API is returned, keeping everything else within the closure private.
* * utilizes an immediately-invoked function expression where object is returned
* * makes use of import and export to use the public keys in different modules
* * The greatest utility of this pattern is to make a clear separation between the public and private parts of an object.

3. Singleton
* * when we need only one instanse like a DB connection

4. Prototype
* *  useful way to share properties among many objects of the same type
* *  Instead of creating a duplicate of the property each time, we can simply add the property to the prototype, since all instances have access to the prototype object.
* * if not found in its own prototype, it goes through the prototype chain to find the property 

5. Factory
* * function that returns a new object without using new keyword
* * this function is not a constructor nor a class
* * when we want to create multiple small objects with same config
* * these objects can be modified after creation

6. Abstract Factory pattern
* * allows us to produce families of related objects without specifying concrete classes
* * like a factory of automobiles => car, truck, motorcycle can be created
* * we have a single function to be called to get a new object of any of these types 
* * we use switch to match the type and return the object of that type of automobile

7. Builder Pattern
* *  create objects in "steps".
* *  we separate the creation of properties and methods into different entities.
* * we can create an object and apply to it only the "steps" we need, which is a more flexible approach.
* * all the objects may not have all the functions attached to them 

##### Structural
1. Adapter
* * allows two objects with incompatible interfaces to interact with each other.
* * Example:- XML response from one API needs to be sent to API that consumes JSON, we need to adapt the XML to JSON first 

2. Decorator 
* *  lets you attach new behaviors to objects by placing them inside wrapper objects that contain the behaviors.
* * Like HOCs in React.js

3. Facade
* *  provides a simplified interface to a library, a framework, or any other complex set of classes.
* * like React, or MUI , or map, reduce, filter functions which use for loop under the hood.

4. Proxy 
* * pattern provides a substitute or placeholder for another object.
* *  The idea is to control access to the original object, performing some kind of action before or after the request gets to the actual original object.
* * example -> middlewears, ExpressJs is used to build node js APIs


##### Behavioural 
1. Chain of Responsibility 
* * passes requests along a chain of handlers. Each handler decides either to process the request or to pass it to the next handler in the chain.
* * render function renders the UI , another function calls and api , that data is passd to another handler to sort , and then this data is rendered on UI 

2. Iterator Pattern
* * used to traverse elements of a collection
* * for, forEach, for...of, for...in, map, reduce, filter, and so on
* * an iterator can be a function that return two functions => hasNext() and next()

3. Observer Pattern
* *  lets you define a subscription mechanism to notify multiple objects about any events that happen to the object they’re observing.
* * useEffect can be good example



<details>
  <summary>How Pub Sub is different from Observer?</summary>
  
  1. Observer
     * Synchronous
     * Tightly coupled - subject knows the observers observing its state
  2. PubSub
     * Asynchronous behaviour
     * Pub and Sub are loosly coupled - they both are not aware about each others existance also
</details>