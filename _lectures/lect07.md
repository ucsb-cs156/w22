---
num: "Lecture 7"
lecture_date: 2021-01-20
desc: "Wed Lecture: Team deployment of jpa03 (jpa04)"
ready: false
done: "Post on the team slack channel that you are finished, and assign yourself the next task that needs
to be completed.  If all tasks have been assigned, pair with someone that is still working on theirs."
---

Note: Discuss working on CSIL vs. working on your local machine.

# In your Breakout Groups: start on jpa04

The assignment jpa04 is essentially the same as jpa03, except you are doing it _as a team_.  This sets up some of the infrastructure and skills you'll need for working on the legacy code projects later in the course.

There are nine distinct jobs (A-I) that you should divide among the members of your group (see list below).
Instructions for each of these follows later in these notes.

Choose a facilitator for today's discussion; that person should share their screen and bring
up the team slack channel in Zoom.

Let n be the number of group members that are present today in lecture; e.g. n may be 4, 5 or 6.
Divide up the first n tasks from the items A-H, among the members of the group that are present.  
Note the names of any group members that are absent.

**Make a post in your team's zoom channel indicating which team members is assigned to each of the first n tasks,
and any group members that are absent**

Example:
```
For team-4pm-1 (not a real team)
* A: Kelsey
* B: Jody
* C: Lane
* D: Morgan

Absent today: Grayson
```

Then as team members finish with a task, you should each make a post indicating that in the team's slack channel, and then take on the *next* task in the list.  

Example:
```
Jody: I'm done with B.  I'm taking on E.
```

The goal is to try to get through all of these during today's lecture; though if that
proves unfeasible, you should at least get through the first five steps (A-E).  The rest
can be done between now and Monday.

* A: Inviting all team members to a shared Auth0 tenant (see note below)
* B: Inviting all staff to your shared Auth0 tenant (see note below)
* C: Setting up a shared Heroku app, and inviting all members of the group to it
* D: Inviting all staff to your shared Heroku app.
* E: Populate that Github repo with the starter code for jpa03
* F: Configure the CI/CD pipeline, i.e. the repo level secrets for `CODECOV_TOKEN` and `TEST_PROPERTIES`

* G: Do the setup steps to make the secrets for the app (i.e. create a `temp-credentials.txt` file),
     and then share the contents of that with your fellow team members via Slack DMs.
* H: Deploy the app first on localhost, then on the team's shared Heroku deployment.

NOTE on items (A) and (B): 

* Two members of your team should have emails inviting them to a shared Auth0 tenant for your team. Find out which of these group members are present; one of them should be assigned to jobs "A" and "B".
* If no-one has such emails, ask for help on the `#help-lecture-discussion` channel on Slack; one of the staff will invite one of the members of your group.


## (A,B) Inviting Additional members to Auth0 Shared Tenant

Two members of your group shoudl have an invitation to a shared auth0 tenant with a name such as:
* `cs156-w21-team-5pm-1`

First task is to accept your own invitation.

Next, switch tenants to the team tenant (there is a "Switch Tenant" option in the menu at the upper right of the Auth0.com dashboard, where your login name is.)

Then, from the same menu, choose the "Invite Admin" feature to invite the other admins.

The person with job "A" should get the `@ucsb.edu` email addresses of all of the other team members.

The person with job "B" should get the `@ucsb.edu` email addresses of all of the staff; these are posted in the `#class-notes` channel on the course Slack.

When you have finished inviting all of the other members of your team (A) or the staff (B), you are done with
this task. {{page.done}}

## (C) Setting up a shared Heroku app

Now, one member of your team should log into Heroku and set up a shared Heroku app with the following name, substituting in your team name as appropriate:

* `jpa03-w21-team-5pm-1`

Then, go to the tab for `Access` 
* the url will be something like <https://dashboard.heroku.com/apps/jpa03-w21-team-5pm-1/access> but your team name in place of `team-5pm-1`

Add the `@ucsb.edu` emails of each of your fellow team members.

When you've done that, task C is complete. {{page.done}}


## (D) Inviting all staff to your shared Heroku app.

Visit your team's shared heroku app, `jpa03-w21-team-5pm-1`.

Then, go to the tab for `Access` 
* the url will be something like <https://dashboard.heroku.com/apps/jpa03-w21-team-5pm-1/access> but your team name in place of `team-5pm-1`

Add the `@ucsb.edu` emails of each of the course staff. these are posted in the `#class-notes` channel on the course Slack.

When you've done that, task D is complete. {{page.done}}

## (E) Populate your team's shared Github repo with the starter code for jpa03

There should already be a repo for your team (substitute your team's name in place of `team-5pm-1`, and everyone
on your team should have access to it. (If that's not the case, check in with the staff)

* <https://github.com/ucsb-cs156-w21/jpa03-team-5pm-1>

Follow the instructions from <https://ucsb-cs156.github.io/w21/lab/jpa03/> to clone this repo,
and then populate it with the starter code for jpa03.

When you've done that, task E is complete. {{page.done}}

## (F) Configure the CI/CD pipeline, i.e. the repo level secrets for `CODECOV_TOKEN` and `TEST_PROPERTIES`

This step depends on step E being completed first, i.e. the repo needs to exist.

Follow the instructions in the file `docs/github-actions-secrets.md` to set up the secrets for
`CODECOV_TOKEN` and `TEST_PROPERTIES` for the repo, so that it passes it's CI/CD tests, i.e. gets a green
check on Github.

When you've done that, task F is complete. {{page.done}}


## (G) Do the setup steps to make the secrets for the app (i.e. create a `temp-credentials.txt` file), and then share the contents of that in your team's channel.

By the time someone takes this on, there are likely multiple team members available

This step is the most complex one, and one where it is _very helpful to pair, or "mob"_
* Note: [mob programming]() is similar to pair programming, but with 3 or more people
* Fun fact: your instructor, Prof. Conrad, was unsuccessful on his first two attempts at following this process,
  and was only successfully when he paired with one of the course staff, Bryan.    Bryan have to do much
  except watch: just the fact that he was watching, caused Prof. Conrad to pay more attention to detail,
  and get things right.   So I _highly recommend_ pairing, not just from theory, but real lived experience.

This step involves going through the setup instructions (the `docs/SETUP-FULL.md` version) from your
repo to generate a `temp-credentials.txt` file.  That file *should not be committed to the repo*!  

It is in the `.gitignore` for a reason: the client id and client secret it contains is a security risk if it
leaks.

Instead, share it among your team using Slack DMs (direct messages).  That information can then be used
by any team members to complete step H.

When you've done that, task G is complete. {{page.done}}

## (H) Deploy the app first on localhost, then on the team's shared Heroku deployment.

This step depends on step G being completed first, i.e. you need the `temp-credentials.txt` file information
to complete it.

Everyone on the team should eventually do the first part (i.e. getting the app running on localhost).
That involves only 
* cloning the repo
* setting up the `secrets-localhost.properties` and `javascript/.env.local` file using the information in the `temp-credentials.txt` file, and the instructions in `docs/SETUP-QUICKSTART.md` 

One member of the team, though, needs to go through the process of setting up the application on the teams's shared jpa03 Heroku application and deploying the main branch.

When that is done, the team is done with it's responsibilities for this lab.

This will be written up as jpa04, a grade that is part of the "programming assignment" portion of your grade, 
but which is assigned at the team level.

Grading rubric:

* A: (10 %) Inviting all team members to a shared Auth0 tenant (see note below)
* B: (10 %) Inviting all staff to your shared Auth0 tenant (see note below)
* C: (10 %) Setting up a shared Heroku app, and inviting all members of the group to it
* D: (10 %) Inviting all staff to your shared Heroku app.
* E: (10 %) Populate that Github repo with the starter code for jpa03
* F: (20 %) Configure the CI/CD pipeline, i.e. the repo level secrets for `CODECOV_TOKEN` and `TEST_PROPERTIES`
  - For full credit, repo should have green check   
  - If there are problems here, we'll give the team an opportunity to fix them.
* G: Do the setup steps to make the secrets for the app (i.e. create a `temp-credentials.txt` file),
     and then share the contents of that with your fellow team members via Slack DMs.
  - This step is not separately graded; the evidence of completion is when step H works.
* H: (30 %) The app is successfully deployed on Heroku
  - For full credit, all of the functions should work
  - This includes logging in/out, roles showing up properly, and saving "todo" items
  - We'll provide feedback on anything that doesn't work and give the teams an opportunity to fix it.
  
