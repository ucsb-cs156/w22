---
num: "Lecture 14"
lecture_date: 2021-04-28
desc: "Wed Lecture: Intro to JavaScript/React, and the team02 project"
ready: true
---

We'll be in "straight lecture mode" again today with no participation grade.

While you are encouraged to participate synchronously, it is acceptable to 
just watch the video later if you are in a time zone where sleep is a better alternative, 
or if you are just juggling other responsibilities.

We have two upcoming team activities planned for next week, so please plan on synchronous participation then:

* A team assignment where you work as a team on front-end code in JavaScript/React that goes with the 
  backend you built in team01.  This will be similar to the team01 assignment, but on the JavaScript/React side. 
  Today's lecture is prep for that.
  
* A separate team assignment where you get your first experience with the legacy code project 
  that you'll be working with in the second half of the course.  

I had anticipated that we'd be starting the legacy code deployment today, but it came to light from students' 
experiences with jpa03 that there were some improvements we could make to the process so that things would go more smoothly.   
So, I think it's worth waiting until next week to get those improvements into the code base.

# What we are building in team02

The team02 assignment is still under development, but here's a preview of the app (in its current state):

* <https://staff-team02-dev.herokuapp.com/>

As you can see, we still have access to the "Swagger" interface directly to the backend endpoints, but we also have some nicer interfaces intended for human
users.  

There is also a Storybook for the React components for the app here, where we can see what each looks like indepdenntly:

* <https://ucsb-cs156-s21.github.io/STAFF-team02-dev-docs/storybook/>

And a QA version here, where you can see the storybook for the most recently pushed PR:

* <https://ucsb-cs156-s21.github.io/STAFF-team02-dev-docs-qa/storybook/>

# What is a React component?

A react component is a unit of JavaScript code (actually JSX code, which is a blend of JavaScript and HTML) that represents a part of a web user interface.

It can be en entire page, or part of a page.

We keep components that are full pages under:

* `javascript/src/main/pages`

And those that are parts of pages under:

* `javascript/src/main/components`

There are tests for both under:

* `javascript/src/test/components`
* `javascript/src/test/pages`

And there is also something called a "Storybook" where you can see each of these components in isolation (from other components, and from the backend):

* <https://ucsb-cs156-s21.github.io/STAFF-team02-dev-docs/storybook/>

# Plain old JavaScript code.

Let's look at some plain old javascript code and the code that is used to test it:

* Look at: `javascript/src/main/utils/arrayUtils.js` and  `javascript/src/main/utils/minMax_NoStryker.js` 
* Look at: `javascript/src/test/utils/arrayUtils.js` and  `javascript/src/test/utils/minMax_NoStryker.js` 

# Overall structure

Under `javascript`

* Most of what we will deal with is under `javascript/src`
* We may also need to know about the `package.json` occasionally and the `package-lock.json`

Under `javascript/src` we find:
* `fixtures`
* `main`
* `stories`
* `test`
* Other misc files:
  - `index.css`   
  - `index.js`
  - `logo.svg`
  - `serviceWorker.js`
  - `setupTests.js`

Under `main`
* `assests`
* `components`
* `pages`
* `utils`
* `App.css`
* `App.js`
