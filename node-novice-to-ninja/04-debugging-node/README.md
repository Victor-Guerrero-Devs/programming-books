# 04. How to debug Node.JS Scripts

## Why Learn Debugging?

- software development is complex
- eventually you will run into a bug
- some far more serious than others, e.g. one that ccan wipe everything on your hardrive
- therefore, it is good to be prepared

## What is Debugging?

- fixing software defects
- often easy like adding a missing semi-colon
- the main issue is when it takes hours trying to find the bug
- thankfully node has great tools for tracking down bugs

## Preventing bugs

1. use a good IDE that underlines errors

2. use a linter (VSC you can just use an extension instead of fancy CLI)

`npm i eslint -g`

`npm eslint index.js`

3. Use source countrol so you can save programs from being irredemable

4. Use an issue-tracking system like Jira, FogBugz, or Bugzilla which are basically journals for identifying bugs and the progress of fixing them.

5. use test driven development (TDD) which is when you test if a function does what it is supposed to before even writing it
