# 3. Linked Compositional Object Models

## Overview

- Understanding the Objects Linked to Other
  Objects (OLOO) pattern of behavior delegation
  with linked objects
- Combining classes with mixins for concatenative
  dynamic extension
- Using Object.assign and the spread operator to
  build new objects

## Intro

- Chapter 2 showed how inheritance helps with making re-usable code
- This chapter focuses on two new techniques to achieve the same goal without using inheritance.
- The first technique is called Objects Linked to Other Objects (OLOO) and relies on Object.create to link objects together. This pattern simplifies the complicated prototype jargon and allows you to view your objects as peers that delegate to one another.
- The second approach involves using mixins, which capture a small set of behavior to create a richer model. Mixins allow you to integrate independent pieces of behavior and data into a single object, similar to using @mixins in CSS preprocessors

## 3.1 Types of Object Links

- In JavaScript, there are two ways to associate objects: implicitly and explicitly. Implicit association is not visible in the code and is done through the internal `Prototype` reference, allowing one object to delegate behavior to another. This is the fundamental method of accessing properties and behavior in prototype-based languages and is used by all object construction patterns. Explicit association is done through a property known directly by name. Both methods allow one object to send messages to another.
- Implicit links are the best to delegate behavior

## 3.2 OLOO Pattern

- The OLOO pattern presented by Kyle Simpson in his book series You Don't Know JS changes our mindset when it comes to visualizing parent-child relationships among objects.
- OLOO's view of differential inheritance is different from the mental model of classes in that it considers objects peers that link together and delegate functionality by passing messages to each other.
- OLOO keeps the good parts of the language while throwing away the deceiving class-based design and the complex prototype configuration of the constructor function pattern. OLOO still uses the `Prototype`, but that mechanism is cleverly hidden behind Object.create and provides a much simpler userland model for designing objects. In OLOO, initialization and construction are separated as two different steps.
- The pattern resembles the Builder pattern used in object-oriented design. The reliance in prototypal inheritance is much more controlled and less exposed. The pattern is presented in simple and complex scenarios.

## 3.3 Object.assign()

- used for the following: copy the properties of one object onto another with a new reference, create a new object that derives its properties from 2 objects, or to update the properties of one object with another's
