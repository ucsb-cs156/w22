---
num: "Lecture 21"
lecture_date: 2020-11-19
desc: "Thursday: Forming Project Teams"
ready: true
5pm_url: https://github.com/ucsb-cs156-f20/proj-ucsb-courses-search/projects
6pm_url: https://github.com/ucsb-cs156-f20/proj-ucsb-cs-las/projects
7pm_url: https://github.com/ucsb-cs156-f20/proj-mapache-search/projects
---

<div style="display: none">
Show: http://ucsb-cs156.github.io/f20/lectures/lect21
</div>

Today we start work on the three projects for the course:

| Section | Project Repo |
|-|-|
| 5pm | <https://github.com/ucsb-cs156-f20/proj-ucsb-courses-search> |
| 6pm | <https://github.com/ucsb-cs156-f20/proj-ucsb-cs-las> |
| 7pm | <https://github.com/ucsb-cs156-f20/proj-mapache-search> |
{:.table .table-sm .table-striped .table-bordered}


Each of your teams has a Kanban board, shown in this table:

| | TA | LA | 5pm | 6pm | 7pm|
|-|-|-|-|-|-|
| a | Mara | Andrew | [F20-5pm-a]({{page.5pm_url}}/3) | [F20-6pm-a]({{page.6pm_url}}/3) <br/> public/member facing |  [F20-7pm-a]({{page.7pm_url}}/3)|
| b | Mara | Bryan  | [F20-5pm-b]({{page.5pm_url}}/4) | [F20-6pm-b]({{page.6pm_url}}/4) <br/> admin dashboard|  [F20-7pm-b]({{page.7pm_url}}/4)|
| c | Scott | Gabriel | [F20-5pm-c]({{page.5pm_url}}/5) | [F20-6pm-c]({{page.6pm_url}}/5) <br/> crud operations |  [F20-7pm-c]({{page.7pm_url}}/5)|
| d | Scott | Tanay | [F20-5pm-d]({{page.5pm_url}}/6) |[F20-6pm-d]({{page.6pm_url}}/6) <br/> course info |  [F20-7pm-d]({{page.7pm_url}}/6)|
{:.table .table-sm .table-striped .table-bordered}

In the "todo" column, on each of your pages, there is one issue that is labelled as an "Epic".   

This issue should remain in your "todo" column on your board throughout the remainder of the course.   You can refer to it to come up with the issues that you'll work on throughout the remainder of the quarter.


# Project Points

The project phase is worth 40% of your grade (see discussion from [Lecture 2](https://ucsb-cs156.github.io/f20/lectures/lect02/) and the newly updated [Syllabus](https://ucsb-cs156.github.io/f20/info/syllabus/)

In addition, we’ll be using peer evaluations through a tool called CATME to assess your individual contributions to the project’s success. The peer evaluation may apply a multiplier to your project grade, increasing it or decreasing it, per your team’s assessment of your contributions. It is important to be sure that you are meeting your committments to your team for a variety of reasons; your grade is among those.

Project points will be earned by contributing to one of the three open source legacy code projects. You’ll be assigned to a project team, and the project team will be assigned to a set of bug fixes and feature requests. This mirrors real world software development practice.

To earn a “perfect score” (100%) for this 20% component of your grade, your team needs to earn 100 project points. If you only earn 80, then an 80% will be recorded for that 20% of your grade.

Some assignments in the project category are worth more points, and some worth fewer.

If you accumulate more than 100 project points, up to 10 project points may be used to raise your final average in the class up to 2.0 points. (The points will be recorded as extra credit). (Each point raises your final course average by 0.2% ).

You may not earn more than 110 total project points–any points in excess of 110 will not count towards your grade (though you’ll probably learn a lot from having under taken the work to earn them.)

# Breakout room activity: turning epics into stories

Choose a leader/scribe.  The leader/scribe should share their screen (you may need the latest version of Zoom 5.3.1 to be able to share screens in breakout rooms.)

First, please ask each member of the team to put their "time zone" into the team's slack channel (both as an attendance check, and to collect this information).
(Time zone= Pacific, China, India, European, for example.  The notation UTC-8 or UTC+8 may be used also.)

What we will be doing today is turning our epics into stories.

We want to break up the epic into different stories, and get each story into a separate issue on the Kanban board.
This will help us be ready on Monday to start work on these stories.


A story is an issue on the Kanban board that has this format.

```
# User Story

As a ____ I can ____ so that ____

# Acceptance Criteria

- [ ] First thing that should be true when story is done.
- [ ] Second thing that should be true when story is done.
...

# Implementation Todos

Front end:

- [ ] First thing that must be done in the front end code.
- [ ] Second thing that must be done in the front end code.
...

Back end:

- [ ] First thing that must be done in the back end code.
- [ ] Second thing that must be done in the back end code.
...


Testing:

- [ ] Front end tests pass and there is adequate coverage
- [ ] Back end tests pass and there is adequate coverage
...
```

We'll talk about what goes into each of these placeholders in lecture, but here are some quick notes.

First, here's a concrete example of a user story that has all of these:
* <https://github.com/ucsb-cs156-f20/proj-mapache-search/issues/11>


* **User Story** is **REQUIRED** 
  - This is a brief statement, from a user's perspective, of who is going to use the new feature, what the new features allows them to do, and why it is important to then.
  - For more information on user stories, see: <https://ucsb-cs156.github.io/topics/user_stories/>
* **Acceptance Criteria** are **REQUIRED** 
  - The ACs are things that an end user should be able to observe in the application that are true when the story is finished.
  - As a whole, the ACs should define everything that needs to be true for the story to be *done* from an end user perspective.
  - They need to be clear and complete.
  - The most common problem with ACs is that they leave out things that are important; so be sure they are completely specified.
* **Implementation Todos** 
  - These are optional, but highly recommended.
  - They specify the steps the team needs to take to implement the story.
  - A common mistake is to put things that are implementation todos in the ACs.   ACs should be generally be *end user facing* and  generally should not include
    internal implementation details.
  - We can separate into front end, back end, and testing.


[Edit Page](https://github.com/ucsb-cs156/f20/edit/main/_lectures/lect21.md)
