# 🤗 Welcome CONTRIBUTOR

This is a document about coding guidelines and processes. These topics reflect the way SolidOS stack contributors work.

Table of content:

- [🤗 Welcome CONTRIBUTOR](#-welcome-contributor)
  - [General rules](#general-rules)
  - [Documenting your code](#documenting-your-code)
    - [General comments](#general-comments)
    - [Adding a TODO](#adding-a-todo)
  - [Refactoring code](#refactoring-code)
    - [Conversion to TypeScript](#conversion-to-typescript)
  - [Windows developers](#windows-developers)

## General rules

- In any given branch/PR, there should be no more than a couple files modified. In general, try to stick to one, though you may need two for testing — one for the test, and one for the code you are testing.
- Name branch as you want.
- include **WIP** in the title of the PR if you want a review.

## Documenting your code

### General comments

In general, if the code is clean, it is easy to understand the algorithm, but sometimes it may make sense to include comments to explain or give an example.

Comment blocks look like this:

```js
/**
 * comments
 * more comments
 */
   doSomething()
 ```

 One-line comments look like this:

 ```js
  // comments
  doSomething()
 ```

### Adding a TODO

An example of when you need a TODO is when you refactor code. There may be times you run across code that cannot be easily changed or that may be better suited for an alternate branch. In this case you can:

1. Create a follow-up issue
2. Document the code with a comment such as that shown below
   `/* @@ TODO [comment about what needs to be done and/or why it is a problem]. See [link to issue]`

## Refactoring code

### Conversion to TypeScript

One of the long-term goals of the SolidOS stack is to convert the code in TypeScript.

Steps:

1. Rename file to `.ts`
2. Add types to public methods (if this is difficult, you can add the `any` type and add comments as described above to indicate it needs further work)
3. Add a comment that the file was previously javascript
4. No Logic changes; only minor refactoring
5. PR is reviewed by at least one other engineer and merged to `main` branch
6. Write unit tests
7. Write examples
8. Refactor
9. Re-Test

## Windows developers

Notes: Single quotes can't be used in scripts on Windows; need to use `\"` instead.
Builds must be run using `bash`, because of `sh` command.
