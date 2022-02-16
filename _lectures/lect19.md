---
num: "Lecture 19"
lecture_date: 2022-02-16
desc: "Wed Lecture: team03"
ready: false
---

Our course meeting on 02/16 is a pure work session on [team03](https://ucsb-cs156.github.io/w22/lab/team03/).

Here are some notes that were put on the Slack before the work session:

# Start with Standup

We'll invite you to start with a "standup meeting" on team03

Please post a written update in the slack channel along with your verbal update

* What have you gotten done since yesterday (if anything)
* What are you working on now (and with whom, if you are pairing),
* Are there any blockers (.e.g things you are stuck on, things you are waiting for from others) 
* What do you think you might have done by next standup

# Plan for standup outside of class

Since we don't have lecture on Monday (University Holiday: "Presidents Day"), the "next standup" is not until next Tuesday, six days from now.

While I can't really "require" you do this, I want to strongly encourage you to *schedule at least one standup between now and next Tuesday* at a time convenient to the team.

Ideally, this would be a synchronous meeting, either in person or on zoom as you see fit.

But, if you can't find a time to do that synchronously, then consider an "asynchronous" standup where, for example, sometime on Friday between 9am and 5pm, each of you posts a "standup update" on your Slack channel.

# Other notes

## Finish up any unfinished setup tasks today in lecture if possible

* Ideally, the team completed all of the setup tasks last night, so that everyone on the team can bring up the application on localhost.
* Ideally, every team has a working prod and qa instance on Heroku.
* **Please add links to the Heroku apps (the working prod and qa instance) at the top of the README of your main team03 repo** along with the links to the prod and qa storybook sites.
* Be sure that every member of the team can log in cloud.mongodb.com and see your database instance.
* Be sure that every member of the team can access the prod and qa instances of the Heroku app.
* Try doing CRUD operations through Swagger on the `students` collection to make sure that the MongoDB instance is working properly.  Consider looking at the MongoDB web interface to see that you can see the database records there (in addition to seeing them through Swagger.)

## Be sure that your team processes are working well

* When you finish an issue and get it into the state where it needs a code review (a CR), consider posting that fact on your Team's slack channel.  
* Be sure to be generous with offering code reviews to other members of your team; you'll need them to CR your PRs too.
* There is a guide here for how to do CRs:  https://ucsb-cs156.github.io/topics/code_reviews/
* Remember to move the cards on the Kanban board as things move from Todo to In Progress to In Review to Done.
* Once you get a card to the "Code Review" stage, try to pick up an new issue for the "In Progress" column as soon as possible.  It's a sign of a good working team that at all times, every team member is working on at least one issue.
* At the same time, don't let CRs' pile up in the "In Review" column.  Another sign of a good team is a good "flow" of work through the pipeline, not letting things pile up in any one column (other than the "Done" column.
