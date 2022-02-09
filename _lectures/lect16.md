---
num: "Lecture 16"
lecture_date: 2022-02-07
desc: "Wed Lecture: Retrospectives, Work on Frontend"
ready: true
---


# Tech Tip: ESLint

When working on the frontend code, there is a GitHub actions script that will run a program called `eslint` against your JavaScript/ECMAScript code (the `es` in `eslint` stands for
ECMAScript.)

This is what it looks like when it fails:


<img alt="ESlint fails" src="https://user-images.githubusercontent.com/1119017/153115905-5a6b0360-95fb-429b-8e28-6f31229621aa.png" width="800" />

What `eslint` does is to check your code for certain style issues, including:
* Indentation
* Variables that are declared by never used

You can check what the eslint problems are by running `npx eslint .` inside the `frontend` directory.  Here's a sample run:

```text
pconrad@Phillips-MacBook-Pro frontend % npx eslint .

/Users/pconrad/github/ucsb-cs156-w22/demo-spring-react-example-v2/frontend/src/tests/components/OurTable.test.js
  1:38  error  'within' is defined but never used. Allowed unused vars must match /^_/u  no-unused-vars

/Users/pconrad/github/ucsb-cs156-w22/demo-spring-react-example-v2/frontend/src/tests/components/Users/UsersTable.test.js
  1:18  error  'waitFor' is defined but never used. Allowed unused vars must match /^_/u                  no-unused-vars
  4:10  error  'getFirstSmallestLargest' is defined but never used. Allowed unused vars must match /^_/u  no-unused-vars
  5:8   error  'userEvent' is defined but never used. Allowed unused vars must match /^_/u                no-unused-vars

✖ 4 problems (4 errors, 0 warnings)

pconrad@Phillips-MacBook-Pro frontend % 
```

In this case, all of the errors are about variables that are defined by never used.  The typical way to resolve this is to simply delete the definitions of those variables.

In rare cases, there may be a legitimate reason that you are keeping the variable around.  In this case, you may change the name of the variable to one that starts
with an underscore, e.g. change `foo` to `_foo`.  This is a convention for unused variables.

Once you've addressed all of the problems, the `eslint` CI/CD script should give you a green check.

If you run `npx eslint .` and get back no output, that means you are good to go:

```text
pconrad@Phillips-MacBook-Pro frontend % npx eslint .                              
pconrad@Phillips-MacBook-Pro frontend % 
```
