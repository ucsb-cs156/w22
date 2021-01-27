---
num: "Lecture 10"
lecture_date: 2021-01-25
desc: "Wed Lecture: Teamwork, part 1, jpa05 continuation, Exploration of legacy app"
ready: true
---


# Overview
* Recap of last night
* Discussion of team work, and 15 minute writing exercise
* Work in Breakout Groups
  - Discussion of teamwork
  - Work on jpa04/jpa05
  - Start on exploring the legacy code app

# Last Night recap

Last night in discussion section was oriented around this assignment: <https://ucsb-cs156.github.io/w21/lab/jpa05/>

Teams worked in breakout rooms on getting started on it, and getting as far as possible on it.

A few cleanup items:
* _Everyone_ please join one of these three slack channels as appropriate:
  - All 5pm section students: `#proj-ucsb-courses-search`
  - 6pm/7pm odd numbered teams: `#proj-ucsb-cs-las`
  - 6pm/7pm even numbered teams: `#proj-mapache-search`

Announcements by project:
* `proj-ucsb-courses-search` seems to be ok... two groups have finished.
* `proj-ucsb-cs-las` should be ok, but let us know if you are running into challenges
* `proj-mapache-search`: Check the `#proj-mapache-search` channel for updates on 
   - How to get the Google Search API Key
   - Progress towards setting up the Slack Slash Command Token
   Also, please join the separate slack workspaces for testing.   Today, I'll make sure that one student from each group gets admin privileges and then can then
   add all of the other team members.
   
Questions about jpa04/jpa05?


# Teamwork is Challenging

* You've probably had good experiences with teams, and also not so good experiences with teams
* You've probably had, perhaps some of each, in this class already too!

If your team experience so far has been "less than ideal":
* That's something to pay attention to...
* But let me try to set your mind at ease.

We are going to be talking a lot about teamwork in this course.   

And having already had some "less than ideal" experiences may actually be a good thing.

* When we talk about teamwork, it helps to have some concrete experiences to relate that to.
* Otherwise, it might seem like a very abstract, uninteresting, theoretical discussion.

# Most real world software development is a team effort

Most software is too large and too complex to be produced or maintained by a single individual.

Teamwork is essential to success.

* Some aspects of teamwork are fairly universal
* Some aspects are specific/contextual to software development

We'll talk about about in this course.

# What is a Team?

From [an article by Jim Sisson](https://www.bizjournals.com/bizjournals/how-to/growth-strategies/2013/06/the-difference-between-a-group-and-a.html), emphasis and formatting added:

"What is the difference between a group of employees and a team?"

* "A group is a collection of individuals who coordinate their individual efforts."
* "On the other hand, a *team* is a group of people who *share a common team purpose* and a *number of challenging goals*."

"Members of the team are *mutually committed to the goals and to each other*." 

"This mutual commitment also creates *joint accountability* which creates a *strong bond* and a strong *motivation to perform*."

# Teams don't just happen: The Tuckman Stages

* As the instructor of the course, I've put you in *groups*.
* We've called those groups "teams".
* But, are they teams yet?

A Psychologist named Bruce Tuckman studied what happens with both successful and unsuccessful teams.  His data revealed a set of common stages that teams go through,
which are now known as the "Tuckman Stages":

1. Forming
2. Norming
3. Storming
4. Performing

Later, a fifth stage was added: (5) Adjourning, to describe what happens after a team is finished with its work and no longer working together 
(i.e. what will happen to these ten teams in Mid-March when this course is over.)

More information is available here: <https://en.wikipedia.org/wiki/Tuckman%27s_stages_of_group_development>

Let's take 7 minutes to read the first four stages, and then 8 minutes to complete the exercise linked to below (two multiple choice questions, one short answer.)

# What stage is your team at?

Let's take a moment to read about these, and then do some writing about that.

[This exercise](https://docs.google.com/forms/d/e/1FAIpQLSfnEPhVCGnb4rD4zlNmSTu-fiHFjcQW867VIHT_JOyUAd8scg/viewform?usp=sf_link) counts 
towards your course participation grade.

# In your breakout rooms

* Have each person share on the team slack channel where they think the team is (just write the name of the stage as a single post; you don't have to write the entire explanation).
* Then, invite each person to share (out loud) what they think the team's next steps should be towards both:
  - finishing jpa04 and jpa05
  - making progress on the Tuckman stages, if needed
* Then, work together to finish jpa04 and/or jpa05
* When finished with jpa04/jpa05, there is one more team activity to start (see below)

# In your team repo

Recall that each of you has a team repo for notes:

| 5pm | 6pm | 7pm |
|-----|-----|-----|
| [team-5pm-1-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-1-NOTES) | [team-6pm-1-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-1-NOTES) | [team-7pm-1-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-1-NOTES)  |
| [team-5pm-2-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-2-NOTES) | [team-6pm-2-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-2-NOTES) | [team-7pm-2-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-2-NOTES)  |
| [team-5pm-3-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-3-NOTES) | [team-6pm-3-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-3-NOTES) | [team-7pm-3-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-3-NOTES)  |
| [team-5pm-4-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-4-NOTES) | [team-6pm-4-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-4-NOTES) | [team-7pm-4-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-4-NOTES)  |
{:.table .table-sm .table-striped .table-bordered}

In this repo, please create a new directory `01.27` and a `README.md` in that directory, as shown in this image:

![create 01.27/README.md](create-readme.png)

In the README.md file, put a link to your jpa05 deployment.  No special syntax is needed in GitHub Flavored Markdown to get a URL to be a link:

```
Our jpa05 deployment is here: https://cs156-w21-team-5pm-1-courses.herokuapp.com/
```

Under the `01.27` directory, each of the team members should create a file with their first name followed by `.md`, e.g. `Amy.md`, `Brian.md`, `Chris.md`, etc.

Now: 
* Explore the app.   
* In your `Chris.md` file, make lists of:
  - Bugs
  - Feature suggestions
  - Improvments to the User Interface

Here is a guide to GitHub Flavored Markdown syntax: <https://guides.github.com/features/mastering-markdown/>

Do this individually first.  Then have a group discussion about what you found, and assemble your suggestions together in one document, in the `01.27/README.md` file.

