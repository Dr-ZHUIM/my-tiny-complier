# Study for the-super-tiny-compiler

Today, I find a repo called [the-super-tiny-compiler](https://github.com/jamiebuilds/the-super-tiny-compiler) which intends to teach how to understand a compiler and create one.

To follow it, I will try to accomplish this work and sometime later I can try to make a markdown plugin for vite but not like the official version.

## Goal

We need to convert a lisp-like function call into a C-like function call.

maybe look like this:

| raw math perfermance | LISP                     | C                       |
| -------------------- | ------------------------ | ----------------------- |
| 2 + 2                | `(add 2 2) `             | `add(2,2)`              |
| 4 - 2                | `(subtract 4 2)`         | `subtract(4,2)`         |
| 2 + (4 - 2)          | `(add 2 (subtract 4 2))` | `add(2, subtract(4,2))` |

## A Composition of A Compiler

Most compiler breaks down into three parts: Parsing, Transfromation and Code Generation. 

1. **Parsing** is taking raw code and turning it into a more abstract representation of the code. 
2. **Transfromation** takes the abstract representation and manipulates to do whatever the compiler wants it do.
3. **Code Generation** takes the transfromed representation of the code and turns it into new code.

## Parsing

Parsing typically has two phases: Lexical Analysis and Syntactic Analysis.

