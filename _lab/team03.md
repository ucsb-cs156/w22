---
desc: "Team Project: Spring Boot Backend, part 2 (authenticated CRUD)"
assigned: 2022-02-15 12:30
due: 2022-02-22 23:59
github_org: ucsb-cs156-w22
layout: lab
num: team03
ready: false
---

# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET

In this team project, our starter code has a full frontend and backend.  Our main focus is the frontend, but we also introduce one new backend element: working with MongoDB
databases.

* Creating support for a MongoDB collection with `@Document` and `@Repository` with `MongoRepository`
* Creating React components and pages in a site that was piloted with the [Create React App](https://create-react-app.dev/) script
* Using [Storybook.js](https://storybook.js.org/) to visualize, catalog, document, and interactively test React components
* Implementing React components for tables using [React Table](https://react-table.tanstack.com/)
* Implementing React components for forms using [React Hook Form](https://react-hook-form.com/)
* Interacting with the backend using the custom hooks `useBackend` and `useBackendMutation`, each of which is wrapped around
  methods from [Axios](https://axios-http.com/) and [React Query](https://react-query.tanstack.com/)
* Using Toast notifications from [React Toastify](https://fkhadra.github.io/react-toastify/introduction/)
* Writing units tests for React components using [Jest](https://jestjs.io/), [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/), [Axios Mock Adapter](https://www.npmjs.com/package/axios-mock-adapter)
* Using `npm run coverage` to use the coverage features of [Jest](https://jestjs.io/) to check Javascript test coverage
* Using `npx stryker run` to use [Stryker Mutator](https://stryker-mutator.io/docs/stryker-js/introduction)  to do mutation testing of a JavaScript test suite

That's a lot!  The thing is, this is typical of professional level full-stack web projects:
* There are so many moving parts, each with its own complex documentation.
* It is typically not feasible (given time constraints) to do a complete deep dive into each of them.
* It is an important skill to be able to discern when "copy/paste/adapt" is the right strategy, and when to do a deeper dive to try to understand what is going on.
* It is also an important skill to know *when* to ask for help, and *how* to ask for help.  That may be one of the most important skills you learn in this course.


In addition, we'll practice further with a few concepts we've seen before:
- Set up of the documentation repos, the `-docs` and `-docs-qa` repos
  - This will be more meaningful now because the Storybook pages published in these repos will become part of our workflow.
  - The scripts to set these up have also be greatly improved over the ones from jpa03 and team02.
- Working with pull requests, and GitHub actions scripts (aka CI/CD).
- Working with a Kanban board and GitHub issues.

# Getting Started

Here's how that will play out in detail:
1. Someone on your team will navigate to the team's `team03-teamname` repo.
2. Under "Projects" create a legacy project (Kanban board, not the Beta Project), with columns: `Todo`, `In Progress`, `In Review`, `Done`
3. Then, you'll pull in the starter code from STARTER-team03 in the usual way:
   ```
   git remote add starter url-of-STARTER-repo-goes-here
   git checkout -b main
   git pull starter main
   git push origin main
   ```
4. Then, as in team02, there is a GitHub actions script which you can manually trigger that should populate your Kanban board with the issues under the `/issues` subdirectory.
5. Then, as in team02, you'll assign those tasks to members of the team, moving them into the "In Progress" as each task is assigned.  
   - You may assign tasks either to individuals, pairs, or even larger groups (so-called "mobs", as in [*Mob Programming*](https://en.wikipedia.org/wiki/Mob_programming))
   - But be sure that if you assign a task to more than one person, that each member of the pair or mob is legitimately committed to contributing to working on the task, and committed to getting it finished.
6. Once a pull request is complete for a given task, you move it into the `In Review` column
   - At this stage, you seek a code review from a member of the team that was not involved in the coding.
   - If it was a true "all-team mob", than it's fine to get a code review from someone that participated, but this is rare.
   - Also, at this stage, if the PR is not "green on CI", meaning that all of the GitHub actions scripts show green checks, this is when you 
     should address that, before merging the pull request.
7. Only when the PR is merged does the issue get moved into the done column.

## What you'll do: Content/Product

From a high-level standpoint, you'll be doing these things:

Set up Tasks:

* Setting up Google OAuth for your project
* Setting up a MongoDB instance for your project
* Setting up a Repo with qa and prod deployments on Heroku
* Configuring the documentation repos
* Configuring Codecov

Coding Tasks:
* Adding CRUD operations for University Subreddits, and UCSB Subjects (we'll leave off UCSB Requirements)
* Copying your the EarthquakeQueryService and EarthquakeQueryServiceTests from your team01 project into team03
* Adding classes that model the JSON retrieved by the EarthquakeQueryService, with a Document class representing the `Feature` level in this JSON.
* Setting up a MongoDB collection for Features documents that represent individual earthquakes.
* Setting up an Earthquakes menu with three options: 
  - Retrieve Earthquakes (Admin only: this will use the EarthquakeQueryService to get all earthquakes that are within a specified distance from Storke Tower, and that are at least a specified magnitude, and store them in the MongoDB collection)
  - Purge Earthquakes (Admin only: this will delete all Earthquakes in the collection)
  - List Earthquakes (All Users: this will list all Earthquakes in the collection) 
* Full test coverage for all of that

# A reminder about open source

Note that this assignment is open source.

The repos are public *on purpose*.
* You are encouraged to consult with one another within and across teams where it helps
  your learning.
* That does not mean that you can cheat by just copying code from another team.
* You are *not* permitted to just look at another team's code, even though you "can".
* It does mean that you should try to solve the problems as best you can, but you may 
  consult with members of other teams as you work.  In that context, you may look at 
  other team's code.

This isn't hard.   You all *know* when you are are looking at other team's work to
try to learn, versus when you are just looking at it as a shortcut to learning.

I'm trusting you to do the right thing.   This is practice for when, later on, you are
all working on different assignments.

