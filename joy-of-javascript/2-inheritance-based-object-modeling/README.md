# 2. Inheritance Based Object Modeling

## Chapter Overview

- Prototypal inheritance, constructor functions,
  and classes
- JavaScript’s property resolution mechanism
- The “prototypal inheritance” oxymoron
- Advantages and drawbacks of classes in
  JavaScript

## Intro

- JavaScript is a programming language where everything, except a few basics, is an object. Objects are essential in JavaScript, but they can also be difficult to understand and use correctly. Developers often struggle with creating prototype chains to relate different objects.
- Inheritance is a powerful pattern in code reuse, but it's not limited to just creating parent-child relationships.
- JavaScript's history includes attempts to make it look like Java, resulting in syntax that some purists don't like.
- Classes are a first-class citizen in JavaScript, and many developers prefer using them instead of direct prototype configuration because they're easier to use. However, it's essential to have a good understanding of how JavaScript's object system works.
- This chapter covers two patterns for modeling inheritance relationships: constructor functions and classes. Both patterns allow sharing data and behavior through prototype references and property resolution mechanisms.

## 2.1 Reviewing Prototypical Inheritance

- JavaScript is object-oriented, and it uses prototypes to enable objects to send messages to objects higher up in the hierarchy of interconnected objects, also known as inheritance.
- The Object.create() API is used to establish a prototype chain that links two or more objects. The prototype object can be manipulated at any time, and this feature allows developers to group common properties.
- The Object.create() API's second argument lets developers control how newly created object properties behave by configuring their properties.

### 2.1.1 Property Resolution Process

- how JavaScript's prototype mechanism and property lookup mechanism work together to implement object-oriented patterns in JavaScript.
- The internal reference `Prototype` is used to link objects, and the JavaScript engine looks for a property in the calling object and then in `Prototype`. If the property is not found, the process continues up the prototype chain until it reaches the empty object literal {}.
- The hidden proto property acts as a bridge that allows for traversal of the chain.
- Don't use proto directly in applications; Object.getPrototypeOf and Object.setPrototypeOf instead.
- Explore resources such as the book series You Don't Know JS to gain a deeper understanding of the nuances of manipulating object chains in JavaScript.

### 2.1.2 Differntial Inheritance

- Differential inheritance means that a derived object maintains references to the objects from which it is derived, which is common in prototypal languages. In JavaScript, this is called `Prototype`. In class-based inheritance, a derived object copies all the state and behavior from its own class, as well as all its derived classes. The key difference is copy versus link.
- differential inheritance is a way for objects to differentiate themselves from their parent object by adding new properties, while class-based inheritance copies all the properties and behaviors from its parent class.
- A hash value is a unique identifier for an object's state, and Object.setPrototypeOf can be used to differentiate a child object.

## 2.2 Constructor Functions

The constructor functions have been used for building objects in JavaScript for a long time, and they offer a scalable way to create many objects of the same shape. The section discusses advanced techniques related to the constructor function pattern.

### 2.2.1 Functions as Templates

- Using functions to build objects in JavaScript is a good design decision that makes your code less fragile and more maintainable.
- Constructor functions are a way to initialize objects populated with different data. By using functions, you can easily instantiate as many objects as you like.
- However, you need to call the function with the "new" keyword to ensure the context is initialized properly. The objects do not share references to any properties, and to fix this problem, you need to configure how prototype links are set up as new objects are created.

### 2.2.2 Sharing Properties by Using Constructors & Prototypes

- use of constructor functions in JavaScript to create objects and how the prototype property works to allow code sharing and reuse.
- The constructor function is a powerful way to create objects, but it requires more attention to detail than traditional object literals.
- The prototype property automatically creates an object that can be used to share code among instances. However, it is important to remember to use the new keyword when calling the constructor to ensure that the new object is created correctly.

## 2.3 Class Based Inheritance

- Classes make it easier to represent inheritance hierarchies and clean up the complex boilerplate code of constructor functions. JavaScript was an object-oriented language long before classes.
- The mental model of classes makes it simpler to represent inheritance hierarchies and helps with domain modeling in terms of inheritance. Classes were introduced to make inheritance modeling easier, especially for developers coming from class-oriented languages.
- The syntax of classes provides syntactical sugar over constructor functions that accomplish the same thing. JavaScript objects can access parent properties declared even after the child object was instantiated.
- Inherited properties from some base object are shared across all instances of child objects, which might lead to undesirable behavior.
- the ease with which classes allow you to set up the prototype chain.
