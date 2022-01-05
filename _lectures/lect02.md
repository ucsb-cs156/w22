---
num: "Lecture 02"
lecture_date: 2022-01-05
desc: "Code Coverage and Mutation Testing (jpa01)"
ready: false
---

# Programming Assignments

* [jpa00](https://ucsb-cs156.github.io/w22/lab/jpa00/) - Simple Java Hello World (using Maven, Java 17)
* [jpa01](https://ucsb-cs156.github.io/w22/lab/jpa01/) - Java OOP, Unit Testing (Junit 5), Code Coverage (Jacoco), Mutation Testing (pitest)
* [jpa02](https://ucsb-cs156.github.io/w22/lab/jpa02/) - Deploying Spring Boot Hello World on Heroku

See Gradescope for due dates.

Both jpa00 and jpa02 are self-explanatory, and don't involve much other than following directions.  

jpa01, on the other hand, requires some thought, and involves learning some new concepts.

So let's dig in.

# Today: preparation for jpa01

Today, we'll discuss:

* Maven
* JUnit
* Jacoco (Code coverage) 
* Mutation Testing

as background for [jpa01](https://ucsb-cs156.github.io/w22/lab/jpa01/).

Today will be an exception to the usual way the course works, in that we may end up using the entire time for a more "traditional lecture"; there's a lot
of ground to cover with these four topics.

We'll use a series of tutorials that are available here, all based on a  simple Java class callled `Student`
* <https://ucsb-cs156.github.io/tutorials/>

You are encouraged to work through tutorials 01 through 09 on your own at a pace suitable for you; our tour in lecture today will be super fast, as we have a lot to cover.

So if you are left a little bewildered, if it all comes too much too fast, don't worry.  Just let as much sink it as can sink in, then go back through it on your own.

# Overview

* If you know what  `make` and `Makefile`s do for C/C++ programming, that's a good starting point for understanding the role of Maven in Java programming.
  - Note that it's not a perfect analogy; make is imperative and tied to Unix commands,
    while Maven is declarative and platform independent
  - Maven also incorporates a package manager which plain vanilla `make` does not.

* JUnit is a framework for unit testing: writing tests that can be run to test your code.
  - Unit testing is foundational for modern software development
  - Unit testing means testing one unit (e.g. a single method) at a time.
  - Typically, other kinds of testing, such as integration testing and end-to-end testing
    are built on top of a unit test framework.
  - It allows us to build an "automated test suite" that runs every time we make a change
    to our code.

* Jacoco: is Java Code Coverage.
  - It allows us to check whether every line of code is covered by at least one test.
  - This is a "good start" for measuring the quality of a test suite
  - But it's possible to cheat, and get 100% test coverage while doing little to no meaningful
    testing.  

* Pitest is a Mutation Testing framework for Java
  - It is a better way of evaluating the quality of a test suite.
  - The idea: start with the assumption that your code is correct.
  - Then, create "mutant" versions of yoru code that are assumed to contain bugs
  - See whether your test suite "kills off all the mutants" (i.e. detects that they have bugs).
  - If any mutants survive, you might have a problem with your test suite, or your code.

The rest of the lecture will be demonstrating these ideas using the Student tutorial.  