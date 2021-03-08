---
num: "Lecture 25"
lecture_date: 2021-03-03
desc: "Wed Lecture"
ready: true
---

# Running Backend and Front end Separately

This is best if you:
* Are working on changes in *either* the backend *or* the front end, but not both
* Want to have "hot refresh" of the front end code, i.e. it changes the behavior in the app as soon as you change the code (not need to "restart")
* Want to speed up the cycle time (since restarts affect *only* backend, or *only* frontend, but not both.)
 
# How to do it 
 
* Run backend in one terminal window with `mvn spring-boot:run -Dskip.npm`
  * The `-Dskip.npm` means: don't do the front end set up stuff
* Run frontend in a separate terminal window with:
  * `cd javascript`
  * `npm start`
* Then, access the application on `localhost:3000` instead of `localhost:8080`
  * There will still be a version on `localhost:8080`, but it wont update 

If you are working on CSIl and forwarding ports, you may need to forward both port 8080 and port 3000.

# Other general items:

* Running the whole app: `mvn spring-boot:run`

Backend Tests:

* Run only the backend tests `mvn test  -Dskip.npm` 
* Run only the backend tests, but recompile everything first: `mvn clean test  -Dskip.npm` 
* Run only the backend code coverage: `mvn test jacoco:report -Dskip.npm` 
* Run only the backend code coverage, but recompile everything first: `mvn clean test jacoco:report -Dskip.npm` 
* Look for code coverage reports in `target/site/jacoco/index.html`

Front end Tests:

* `cd javascript; npm test`
* `cd javascript; npm run coverage`
  * it is meaningless unless all tests run with `npm test` pass
  * look for coverage report in `javascript/coverage/lcov-reports/index.html` or something like that (TODO check link)

