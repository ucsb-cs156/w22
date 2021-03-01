---
num: "Lecture 23"
lecture_date: 2021-03-01
desc: "Mon Lecture"
ready: true
---

# Due Dates

* Final Presentations:  Tuesday, March 16, 2021 12:00 PM - 3:00 PM
* Deadline for all PRs: Noon, Wednesday 3/10 

After that, you may continue to make changes to 
* Get tests to pass
* Address code review issues
* Address merge conflicts 
* Address bugs found during code review

You may not, however:
* Do substantial new development
* Start new issues

# Pull Requests

* <https://ucsb-cs156.github.io/topics/pull_requests/>

# Live Demos and Exploratory Testing

* on qa site?
* on team site?

# Localhost setup

# Making Progress

* If you run out of stories?

# Git commands

Any questions on that?

Concepts:
* branch
* remote
* rebase
* merge

Diagram... 

Commands

* git reset
* git pull --rebase origin main
* git push origin branch -f 

# General Skills

* Front end vs. Back end
  * Front end is all under `javascript` and in JavaScript
  * Back end is all under `src` (at top level) and in Java
  * How do they work together?
  * What is the DOM?
  * What is a RESTful API?

* `mvn spring-boot:run`
* `mvn clean test jacoco:report -Dskip.npm` 
  * vs `mvn test jacoco:report -Dskip.npm`
  * look in `target/site/jacoco/index.html`
* Running back end and front end separately: `mvn spring-boot:run -Dskip.npm`  plus `cd javascript; npm start`
  * then look at localhost:3000 instead of localhost:8080 for live hot refresh of front end code
  * If backend isn't running, you may get errors in this setup
  * If running on CSIL, you may have to forward both ports 8080 and 3000 separately...
* `cd javascript; npm test`
* `cd javascript; npm run coverage`
  * it is meaningless unless all tests run with `npm test` pass
  * look for coverage report in `javascript/coverage/lcov-reports/index.html` or something like that (TODO check link)

For testing:
* looking at examples from projects

# Other

* Setting up React Dev Tools
* Docker
