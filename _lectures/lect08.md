---
num: "Lecture 08"
lecture_date: 2021-04-13
desc: "Wed Lecture: testing aspect of team01, mocking/stubbing in Java (Mockito), code reviews and PRs"
ready: true
---

Today we'll look at the testing aspect of the project <https://ucsb-cs156.github.io/s21/lab/team01/>

We'll discuss the goal with of *unit testing* of isolating the *unit under test* so that we test only the code inside that
unit (i.e. a single method), by mocking and stubbing dependencies.

This relates to the concept of *dependency injection*, which we'll also discuss.

# Dependency Injection

For testing purposes, you want dependencies to be loose rather than strict.

Example of `EarthquakeController` depending on `EarthquakeQueryService`:
- Suppose the correctness of module A depends on the correctness of module B
- Specific example: The `EarthquakeController` depends on the `EarthquakeQueryService` doing it's job properly
- For testing *just the code* in the `EarthquakeController`, you want to temporarily set up a situation where the
  specific features of the `EarthquakeQueryService` that the  `EarthquakeController` depends on are *mocked*.
- That is, you hard code an alternative implementation of the `EarthquakeQueryService` that knows just how to 
  take a specific input, and provide a specific return value from the  `EarthquakeQueryService`.
- That allows you to test the service in isolation.

Example of  `EarthquakeQueryService` depending on an external API (the one from the US Geological Survey):
- Suppose the correctness of module A depends on the correctness of an external service,
  one that isn't even provided by code that we wrote!
- Specific example: The `EarthquakeQueryService` depends on the API provided by the US Geological Survey
- The code for your `EarthquakeQueryService` could be *100% correct*, but if the USGS web server is down,
  the `EarthquakeQueryService` won't perform correctly.
- Plus, the data returned by the  `EarthquakeQueryService` can change over time; even for past earthquakes!  From time to time,
  the USGS gets new data readings and updates data for past earthquakes.  So there is no way to be *sure* when we 
  write a test what the "correct" answer should be.  How can we test such a service?
- Solution: for testing *just the code* in the `EarthquakeQueryService`, you want to temporarily set up a situation where the
  interaction with the external API is *mocked*.  Instead of doing a real call to the USGS server, we set up a "fake"
  server that is expecting a certain URL to be requested, and will return a certain fake value.
- We then can check that when we pass in particular parameters, the service does indeed call out to the specific URL,
  and that the value returned by the URL is processed in the way we expect and returned from the service.
  
  
# Pros/Cons of Mocking and Stubbing  
 
Mocking and Stubbing is a widely used practice in the software industry, and definitely is an important thing to know about.

We also acknowledge that it has its limitations, and its critics:

Some pros:
* Good isolation of tests; you can test each component by itself
* In order to be able to test in this way, you do need to keep each module small, which promotes some good software engineering practices:
  - Single Responsibility Principle: each module should have "just one job" (sometimes expressed as "one reason to change").
  - Modules should depend on one other "loosely" through well defined APIs, rather than depending on internal details.

Some cons:
* Tests written in this way can be *brittle* meaning that they break frequently when changes to the code are made.
* This is because they often depend on internal details of the code; ideally tests should depend on external behavior only,
  and not on internal implementation details.
* Some feel that this level of testing doesn't sufficiently get at the *big picture*, i.e. "does the app really work"? They 
  prefer *integration tests* that check the behavior of the app as a "black box", i.e. test that only work through the 
  RESTful API, or the user interface of the app.
  
 This brings us to a concept call the testing pyramid.  The following diagram is copied from the article [The Practical Test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html)
 by Martin Fowler, which I encourage you to read if you are interested in this topic.  The diagram itself is attributed
 to Mike Cohn:
 
 
 
 Martin Fowler discusses the pros/cons of various types of testing, and of the test pyramid concept itself, but arrives
 at two big-picture take aways that represent something like the mainstream consensus, though individual opinions will vary:
 
1. Write tests with different granularity
2. The more high-level you get the fewer tests you should have

Point 1 says that it's useful to write:
* unit tests that isolate components
* integration tests that check whether components work together
* end-to-end (e2e) tests that actually interact with your application from start to finish, automating the exact steps a real user
  of your app would take (whether that user is a human being, or another computer program)
  
Point 2 says that as we move up this pyramid, there will likely be fewer tests
* lots of unit tests, ideally ones that cover all or most of your functionality
* some integration tests
* just a few e2e tests 

The reasoning behind point 2 is that lower in the pyramid, the tests are:
* the lower you are in the pyramid, the faster the tests are to write, and the faster they run
* the higher you are in the pyramid, the more time consuming the tests are to write, and the slower they run

I would also acknowledge that:
* the lower you are in the pyramid, the less value there is to each individual test
* the higher you are in the pyramid, the more value there is to each individual test

  
