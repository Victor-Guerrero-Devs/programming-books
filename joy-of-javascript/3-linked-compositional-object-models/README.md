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
