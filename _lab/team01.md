---
desc: "Team Project: Spring Boot Backend, part 1 (unauthenticated RESTFul APIs)"
assigned: 2021-04-13 17:00
due: 2021-04-21 23:59
github_org: ucsb-cs156-s21
layout: lab
num: team01
ready: false
starter: https://github.com/ucsb-cs156-s21/STARTER-team01
---


# NOTE: THIS IS STILL A WORK IN PROGRESS... COME BACK LATER (it isn't ready for you to start work yet.)

This is a team programming assignment.  Each team has it's own repo to complete this assignment, and
you will work as a team.

Here are the links to the repos:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[team01-s21-5pm-1](https://github.com/ucsb-cs156-s21/team01-s21-5pm-1)|[team01-s21-6pm-1](https://github.com/ucsb-cs156-s21/team01-s21-6pm-1)|[team01-s21-7pm-1](https://github.com/ucsb-cs156-s21/team01-s21-7pm-1)|
|[team01-s21-5pm-2](https://github.com/ucsb-cs156-s21/team01-s21-5pm-2)|[team01-s21-6pm-2](https://github.com/ucsb-cs156-s21/team01-s21-6pm-2)|[team01-s21-7pm-2](https://github.com/ucsb-cs156-s21/team01-s21-7pm-2)|
|[team01-s21-5pm-3](https://github.com/ucsb-cs156-s21/team01-s21-5pm-3)|[team01-s21-6pm-3](https://github.com/ucsb-cs156-s21/team01-s21-6pm-3)|[team01-s21-7pm-3](https://github.com/ucsb-cs156-s21/team01-s21-7pm-3)|
|[team01-s21-5pm-4](https://github.com/ucsb-cs156-s21/team01-s21-5pm-4)|[team01-s21-6pm-4](https://github.com/ucsb-cs156-s21/team01-s21-6pm-4)|[team01-s21-7pm-4](https://github.com/ucsb-cs156-s21/team01-s21-7pm-4)|
{:.table .table-sm .table-striped .table-bordered}

# Step 1: Pull in Starter Code

One member of the team, it doesn't matter who, should pull in the starter code.

I suggest you do this in your breakout room, with the whole team watching, and the team member that is doing the work
sharing their screen.

That member should:
1. Clone the team's repo
2. Add a remote for the starter code, which is here: <{{page.starter}}>
3. Checkout the main branch (`git checkout -b main`)
4. Pull from the starter remote (`git pull starter main`)
5. Push to the origin repo (`git push origin main`)

# Step 2: Deploy the repo, as is, to Heroku

A member of your team should:

1. Visit the Heroku Dashboard, and create a Heroku app with the name `cs156-s21-5pm-1-team01`, substituting in your team number in place of `5pm-1`.
2. On the deploy screen, link your Heroku app to your team's repo, and deploy the main branch.
3. When the app is deployed, you should be able to navigate to the link below for your team, and launch the application.

   The result of visiting the home page of the app in the browser should be something like this:
   
   ```json
   ```
   
   It might also be nicely formatted, depending on whether you have any browser extensions installed for processing JSON:
   ```json
   ```

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-s21-5pm-1-team01](https://cs156-s21-5pm-1-team01.herokuapp.com)|[cs156-s21-6pm-1-team01](https://cs156-s21-6pm-1-team01.herokuapp.com)|[cs156-s21-7pm-1-team01](https://cs156-s21-7pm-1-team01.herokuapp.com)|
|[cs156-s21-5pm-2-team01](https://cs156-s21-5pm-2-team01.herokuapp.com)|[cs156-s21-6pm-2-team01](https://cs156-s21-6pm-2-team01.herokuapp.com)|[cs156-s21-7pm-2-team01](https://cs156-s21-7pm-2-team01.herokuapp.com)|
|[cs156-s21-5pm-3-team01](https://cs156-s21-5pm-3-team01.herokuapp.com)|[cs156-s21-6pm-3-team01](https://cs156-s21-6pm-3-team01.herokuapp.com)|[cs156-s21-7pm-3-team01](https://cs156-s21-7pm-3-team01.herokuapp.com)|
|[cs156-s21-5pm-4-team01](https://cs156-s21-5pm-4-team01.herokuapp.com)|[cs156-s21-6pm-4-team01](https://cs156-s21-6pm-4-team01.herokuapp.com)|[cs156-s21-7pm-4-team01](https://cs156-s21-7pm-4-team01.herokuapp.com)|
{:.table .table-sm .table-striped .table-bordered}
