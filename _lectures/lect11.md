---
num: "Lecture 11"
lecture_date: 2022-01-25
desc: "Mon Lecture: First in-person class for CMPSC 156 in W22 in SH1431"
ready: false
---


# Table Assignment

| Section | Team 1 | Team 2 | Team 3 | Team 4|
|---------|--------|--------|--------|-------|
| 5pm     |  1     |  2     | 3      |  4    |
| 6pm     |  5     |  6     |  7     |   8   |
| 7pm     |  9     |  10    |  11    |   13  |
{:.table .table-sm .table-striped .table-bordered}

# Topics


## How to get the logs for a Heroku app

Through the web interface:

<img src="https://user-images.githubusercontent.com/1119017/151609450-0a75b593-ef27-4d8a-85ea-42912ce99c43.png" alt="Heroku Dashboard Logs Menu Item" width="300" />

At command line (with Heroku CLI installed):

The `-a application-name` is the application name, e.g. for `demo-spring-react-example-v2qa.herokuapp.com`, use this:

```
heroku logs -a demo-spring-react-example-v2qa --tail
```

The `--tail` allows you to see the log go by in real time as it is produced.

## How to run just one test file using Maven

For example, to run only the tests in the file `ApiControllerTests.java`

```
mvn test -Dtest=ApiControllerTests
```
