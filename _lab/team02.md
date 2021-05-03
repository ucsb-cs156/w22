---
desc: "Team Project: Front End: Javascript, React, Jest, Stryker"
assigned: 2021-05-03 12:30
due: 2021-05-12 11:59
github_org: ucsb-cs156-s21
layout: lab
num: team02
ready: false
gradescope: TBD
starter: https://github.com/ucsb-cs156-s21/STARTER-team02
gauchospace: https://gauchospace.ucsb.edu/courses/mod/assign/view.php?id=TBD
---

# NOT READY YET
# NOT READY YET
# NOT READY YET

Please don't start until the staff indicates that this is ready to start and the notices above are removed.

# Second team programming assignment: Front End coding with Javascript, React, Jest

This is a team programming assignment.  Each team has it's own repo to complete this assignment, and
you will work as a team.

Here are the links to the repos:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[team02-s21-5pm-1](https://github.com/ucsb-cs156-s21/team02-s21-5pm-1)|[team02-s21-6pm-1](https://github.com/ucsb-cs156-s21/team02-s21-6pm-1)|[team02-s21-7pm-1](https://github.com/ucsb-cs156-s21/team02-s21-7pm-1)|
|[team02-s21-5pm-2](https://github.com/ucsb-cs156-s21/team02-s21-5pm-2)|[team02-s21-6pm-2](https://github.com/ucsb-cs156-s21/team02-s21-6pm-2)|[team02-s21-7pm-2](https://github.com/ucsb-cs156-s21/team02-s21-7pm-2)|
|[team02-s21-5pm-3](https://github.com/ucsb-cs156-s21/team02-s21-5pm-3)|[team02-s21-6pm-3](https://github.com/ucsb-cs156-s21/team02-s21-6pm-3)|[team02-s21-7pm-3](https://github.com/ucsb-cs156-s21/team02-s21-7pm-3)|
|[team02-s21-5pm-4](https://github.com/ucsb-cs156-s21/team02-s21-5pm-4)|[team02-s21-6pm-4](https://github.com/ucsb-cs156-s21/team02-s21-6pm-4)|[team02-s21-7pm-4](https://github.com/ucsb-cs156-s21/team02-s21-7pm-4)|
{:.table .table-sm .table-striped .table-bordered}


# Part 1: Team divides up the work

The first few steps here are identical to the ones that you did for
team01, and will be similar to skills you'll need for the legacy
code phase of the course.

The steps in Part 1 are part of participation assignment (P04), in class on Monday 05/03/2021. 

# Step 1.0: Divide up the Part 1 Tasks

In your breakout room:

1. Choose one member of the team should to share 
   their screen and bring up the team's slack channel.
2. Each team member is asked to make a post to let the
   team know they are participating; 
   this might be a simple greeting to the team (e.g. `Hey there team!`).
   
   You need to know how many folks are here, because the tasks you 
   are dividing up are ones you'll be completing during class.

3. Now, divide up the following list of tasks among the team members.
   These are to be done during class today.   Post to the slack channel
   who is doing what.  You can pair up on a tasks if needed; but
   each person should be assigned to at least one task, and each task
   needs to be covered.

   These can be done more-or-less in parallel; there are a few 
   small dependencies (such as the fact that if you deploy the
   Heroku app when the repo is still empty, nothing will happen),
   but you can definitely start on each of them at the same time.

   1. Cloning initial code repo, and populating with starter code.
   2. Setting up Heroku deployment for team02 app and deploying code
      to it.
   3. Setting up team and staff permissions on the Heroku repo.
   4. Setting up GitHub Pages repo `docs` for storybook.
   5. Setting up GitHub Pages repo `docs-qa` for storybook.
   6. Setting up Kanban board for team.

   The rest of Part 1 describes each of these tasks one-by-one.
   After dividing up the tasks, get started on them.  When each
   one is finished, report that on the team's slack channel,
   and check in on other team members to help with their tasks.

   You can stay all in the team's main zoom breakout room, or if it helps, you can divide across multiple breakout rooms; either way, stay in touch with your team using the team's slack channel.




# Step 1.1: Pull in Starter Code

One member of the team, it doesn't matter who (but for practice, I suggest that it be someone different that who did it for `team01`), should clone the team's repo on their machine, pull in the starter code
(as outlined below).

I suggest you do this in your breakout room, with the whole team watching, and the team member that is doing the work
sharing their screen.

That member should:
1. Clone the team's repo
2. Add a remote for the starter code, which is here: <{{page.starter}}>
3. Checkout the main branch (`git checkout -b main`)
4. Pull from the starter remote (`git pull starter main`)
5. Push to the origin repo (`git push origin main`)

# Step 1.2: Deploy the repo, as is, to Heroku

A member of your team should:

1. Visit the Heroku Dashboard, and create a Heroku app with the name `cs156-s21-5pm-1-team02`, substituting in your team number in place of `5pm-1`.   Since each user on the Heroku "free plan" is limited to 5 apps, it would be helpful if this were someone other than the team member
that created this for `team01`.
2. On the deploy screen, link your Heroku app to your team's repo, and deploy the main branch.
3. When the app is deployed, you should be able to navigate to the link below for your team, and launch the application.

Heroku Dashboard:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-s21-5pm-1-team02](https://dashboard.heroku.com/apps/cs156-s21-5pm-1-team02)|[cs156-s21-6pm-1-team02](https://dashboard.heroku.com/apps/cs156-s21-6pm-1-team02)|[cs156-s21-7pm-1-team02](https://dashboard.heroku.com/apps/cs156-s21-7pm-1-team02)|
|[cs156-s21-5pm-2-team02](https://dashboard.heroku.com/apps/cs156-s21-5pm-2-team02)|[cs156-s21-6pm-2-team02](https://dashboard.heroku.com/apps/cs156-s21-6pm-2-team02)|[cs156-s21-7pm-2-team02](https://dashboard.heroku.com/apps/cs156-s21-7pm-2-team02)|
|[cs156-s21-5pm-3-team02](https://dashboard.heroku.com/apps/cs156-s21-5pm-3-team02)|[cs156-s21-6pm-3-team02](https://dashboard.heroku.com/apps/cs156-s21-6pm-3-team02)|[cs156-s21-7pm-3-team02](https://dashboard.heroku.com/apps/cs156-s21-7pm-3-team02)|
|[cs156-s21-5pm-4-team02](https://dashboard.heroku.com/apps/cs156-s21-5pm-4-team02)|[cs156-s21-6pm-4-team02](https://dashboard.heroku.com/apps/cs156-s21-6pm-4-team02)|[cs156-s21-7pm-4-team02](https://dashboard.heroku.com/apps/cs156-s21-7pm-4-team02)|
{:.table .table-sm .table-striped .table-bordered}

Running App:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-s21-5pm-1-team02](https://cs156-s21-5pm-1-team02.herokuapp.com)|[cs156-s21-6pm-1-team02](https://cs156-s21-6pm-1-team02.herokuapp.com)|[cs156-s21-7pm-1-team02](https://cs156-s21-7pm-1-team02.herokuapp.com)|
|[cs156-s21-5pm-2-team02](https://cs156-s21-5pm-2-team02.herokuapp.com)|[cs156-s21-6pm-2-team02](https://cs156-s21-6pm-2-team02.herokuapp.com)|[cs156-s21-7pm-2-team02](https://cs156-s21-7pm-2-team02.herokuapp.com)|
|[cs156-s21-5pm-3-team02](https://cs156-s21-5pm-3-team02.herokuapp.com)|[cs156-s21-6pm-3-team02](https://cs156-s21-6pm-3-team02.herokuapp.com)|[cs156-s21-7pm-3-team02](https://cs156-s21-7pm-3-team02.herokuapp.com)|
|[cs156-s21-5pm-4-team02](https://cs156-s21-5pm-4-team02.herokuapp.com)|[cs156-s21-6pm-4-team02](https://cs156-s21-6pm-4-team02.herokuapp.com)|[cs156-s21-7pm-4-team02](https://cs156-s21-7pm-4-team02.herokuapp.com)|
{:.table .table-sm .table-striped .table-bordered}

The result of visiting the home page of the app in the browser should be something like this:

![home page screenshot](team02-start-home-page.png)


# Step 1.3: Give team and staff access to your Heroku Deployment

Please visit the `Access` tab of the Heroku Dashboard for your deployed app.

Add each of the members of your team.

Then also add the assigned LA and TA for your team.   
* You can find their names here: `https://ucsb-cs156.github.io/s21/info/teams/`
* To get the email that you should use for Heroku, dm them on the slack.
* Then add `phtcon@ucsb.edu`, the instructor for the course.


# Step 1.4: Setting up GitHub Pages repo `docs` for storybook.

TODO: Write these instructions

# Step 1.5: Setting up GitHub Pages repo `docs-qa` for storybook.

TODO: Write these instructions

# Step 1.6: Create a Kanban board for your team.

TODO: Write these instructions
