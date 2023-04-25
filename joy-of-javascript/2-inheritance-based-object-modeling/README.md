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
