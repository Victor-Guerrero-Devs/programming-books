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
