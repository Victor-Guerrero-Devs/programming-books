# Chapter 1: JavaScript Reloaded

## Introduction

- when creating something new, the biggest question is how to structure your code
- although frameworks take care of that for the most part, you still need to create structure in vanilla JS, especially w/
  business-domain logic
- this book will teach you this as well as other features in JS
- it will also teach how to write JS well

## 1.1 Evolving JavaScript

- not much is discussed beside the evolution of JS
- anyway, the four major themes of this book will be covered starting now

## 1.2 Objects

- objects are memory references that point to another location in memory
- object literals are fine for one of a kind object
- classes if you need objects with the same properties and methods

## 1.3 Functions

- Functions drive the state of an application and implement its business logic.
- They can be thought of in two ways: as a group of statements that execute together in a procedural or imperative mindset, or as immutable computations assembled like Lego bricks in functional programming.
- Functional programming can simplify complex programs and make code more maintainable and declarative, using techniques such as decomposition, composition, and higher-order functions. The chapter on functional programming teaches enough to significantly affect day-to-day coding, and the use of functions can abstract any kind of logic to create a pipeline of information.
- JavaScript's pipeline operator and Algebraic Data Types (ADTs) can be used for data transformation and validation.
- The pipeline operator allows chaining of functions in a UNIX-like manner, while ADTs provide a way to abstract over if/else logic with an expression.
- Functors and monads are introduced as objects that behave like functions and can be used for data transformation.

## 1.4 Code

- ESM standardizes how code is shared and is platform agnostic
- this is the import/export module that replaced CommonJS, made by NodeJS
- easy for bundlers to pack into one file
- easy to write module code
- easy to implement separation of concerns

## 1.5 Data

- JavaScript is used for handling data of various shapes and sizes arriving synchronously or asynchronously from anywhere.
- Promises simplify reasoning about asynchronous code, allowing for composable chains of sequential logic to solve complex problems involving asynchronous data sources.
- Async generators allow for potentially infinite sequences of data over time, and Observables can handle all data types with a consistent computing model, making them attractive to framework and library authors.
- Observables are composable and can be used to process data synchronously or asynchronously, making them a powerful tool for modern software development.
- with the JS feature of higher order functions, managing data becomes easy
