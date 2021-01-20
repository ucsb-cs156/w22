---
num: "Lecture 7"
lecture_date: 2021-01-20
desc: "Wed Lecture: "
ready: false
---


Note: Discuss working on CSIL vs. working on your local machine.


# In your Breakout Groups: start on jpa04

The assignment jpa04 is essentially the same as jpa03, except you are doing it _as a team_.  This sets up some of the infrastructure and skills you'll need for working on the legacy code projects later in the course.

There are eight distinct jobs (A-H) that you should divide among the members of your group (see list below).
Instructions for each of these follows later in these notes.

Choose a facilitator for today's discussion; that person should share their screen and bring
up the team slack channel in Zoom.

Divide up the first six items, A-H, among the members of the group that are present.  Note the names of any group members that are absent.

**Make a post in your team's zoom channel indicating which team members is assigned to each of the tasks A-F**

_If you have fewer than 6 members_, just assign the first 4 or 5 tasks from among A-F initially.

Then as team members finish with a task, you should each make a post indicating that in the team's slack channel, and then take on the *next* task in the list.

The goal is to try to get through all of these during today's lecture; though if that
proves unfeasible, you should at least get through the first six steps (A-F).

Note that there are multiple jobs here, and more than there are group members.  
So everyone present should take responsibility for at least
one of them.  But after that, you can pair on some of these.

* A: Inviting all team members to a shared Auth0 tenant (see note below)
* B: Inviting all staff to your shared Auth0 tenant (see note below)
* C: Setting up a shared Heroku app, and inviting all members of the group to it
* D: Inviting all staff to your shared Heroku app.
* E: Setting up a shared Github Repo for your team
* F: Populate that Github repo with the starter code for jpa03
* G: Do the setup steps to make the secrets for the app (i.e. create a `temp-credentials.txt` file),
     and then share the contents of that in your team's channel.
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
this task.   Post on the team slack channel that you are finished, and assign yourself the next task that needs
to be completed.  If all tasks have been assigned, pair with someone that is still working on theirs.

## Setting up a shared Heroku app

Now, one member of your team should log into Heroku and set up a shared Heroku app with the following name, substituting in your team name as appropriate:

* `jpa03-w21-team-5pm-1`





## Deploying the jpa03 code to Auth0
