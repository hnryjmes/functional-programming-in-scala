# Functional Programming in Scala

*by Paul Chiusano, Rúnar Bjarnason*

`Notes by Henry Cooksley`

### Foreword

"Scala is an impure functional programming language in that it admits impure as well as pure functions, and in that it does not try to distinguish between these categories by using different syntax or giving them different types."

"Side effects such as mutation, I/O, or use of exceptions are not ruled out, and they can indeed come in quite handy sometimes, be it for reasons of interoperability, efficiency, or convenience."

## 1 Introduction to functional programming

"We begin this book with a radical premise - that we will restrict ourselves to constructing programs using only pure functions with no side effects such as reading from files or mutating memory."

### 1 What is functional programming?

"The answer is that functional programming is a restriction on how we write programs, but not on what programs we can express."

"Because of their modularity, pure functions are easier to test, reuse, parallelize, generalize, and reason about."

#### 1.1 The benefits of FP: a simple example

##### 1.1.1 A program with side effects

##### 1.1.2 A functional solution: removing the side effects

"Here we've separated the concern of creating a charge from the processing or interpretation of that charge."

#### 1.2 Exactly what is a (pure) function?

"A function f with input type A and output type B (written in Scala as a single type: A => B, pronounced “A to B” or “A arrow B”) is a computation that relates every value a of type A to exactly one value b of type B such that b is determined solely by the value of a."

"In other words, a function has no observable effect on the execution of the program other than to compute a result given its inputs; we say that it has no side effects."

"Procedure is often used to refer to some parameterized chunk of code that may have side effects."

"This is all it means for an expression to be referentially transparent - in any program, the expression can be replaced by its result without changing the meaning of the program."

#### 1.3 Referential transparency, purity, and the substitution model

"Modular programs consist of components that can be understood and reused independently of the whole, such that the meaning of the whole depends only on the meaning of the components and the rules governing their composition; that is, they are composable."

#### 1.4 Summary

### 2 Getting started with functional programming in Scala

"We'll discuss how to write loops using tail recursive functions, and we'll introduce higher-order functions (HOFs)."

"HOFs are functions that take other functions as arguments and may themselves return functions as their output."

#### 2.1 Introducing Scala the language: an example

"We'll sometimes refer to the part of a declaration that goes before the equals sign as the right-hand side or definition."

"Usually a return type of Unit is a hint that the method has a side effect."

#### 2.2 Running our program

#### 2.3 Modules, objects, and namespaces

#### 2.4 Higher-order functions: passing functions to functions

##### 2.4.1 A short detour: writing loops functionally

"In functional programming, we tend to use very short variable names, even one-letter names."

"This is usually because HOFs are so general that they have no opinion on what the argument should actually do."

#### 2.5 Polymorphic functions: abstracting over types

"So far we've defined only monomorphic functions, or functions that operate on only one type of data."

"Often, and especially when writing HOFs, we want to write code that works for any type it's given."

"We're using the term polymorphism in a slightly different way than you might be used to if you're familiar with object-oriented programming, where that term usually connotes some form of subtyping or inheritance relationship."

"The kind of polymorphism we're using here is sometimes called parametric polymorphism."

##### 2.5.1 An example of a polymorphic function

"This is an example of a polymorphic function, sometimes called a generic function."

"We're abstracting over the type of the array and the function used for searching it."

##### 2.5.2 Calling HOFs with anonymous functions

"When we define a function literal, what is actually being defined in Scala is an object with a method called apply."

#### 2.6 Following types to implementations

#### 2.7 Summary

### 3 Functional data structures