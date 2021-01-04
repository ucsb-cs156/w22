---
num: "Lecture 21"
lecture_date: 2020-11-19
desc: "Monday: Understanding our teams' epics"
ready: true
5pm_url: https://github.com/ucsb-cs156-f20/proj-ucsb-courses-search/projects
6pm_url: https://github.com/ucsb-cs156-f20/proj-ucsb-cs-las/projects
7pm_url: https://github.com/ucsb-cs156-f20/proj-mapache-search/projects
---

<div style="display: none">
Show: http://ucsb-cs156.github.io/f20/lectures/lect21
</div>

Last Thursday, each team was assigned an epic from one of these three legacy code projects:

| Section | Project Repo |
|-|-|
| 5pm | <https://github.com/ucsb-cs156-f20/proj-ucsb-courses-search> |
| 6pm | <https://github.com/ucsb-cs156-f20/proj-ucsb-cs-las> |
| 7pm | <https://github.com/ucsb-cs156-f20/proj-mapache-search> |
{:.table .table-sm .table-striped .table-bordered}


Each of your teams has a Kanban board, shown in this table:

| | TA | LA | 5pm | 6pm | 7pm|
|-|-|-|-|-|-|
| a | Mara | Andrew | [F20-5pm-a]({{page.5pm_url}}/3) <br/> Searches | [F20-6pm-a]({{page.6pm_url}}/3) <br/> public/member facing |  [F20-7pm-a]({{page.7pm_url}}/3) <br /> Search by user, summarize message data by user|
| b | Mara | Bryan  | [F20-5pm-b]({{page.5pm_url}}/4) <br/> Personal Schedule | [F20-6pm-b]({{page.6pm_url}}/4) <br/> admin dashboard|  [F20-7pm-b]({{page.7pm_url}}/4) <br/> Slack Bot |
| c | Scott | Gabriel | [F20-5pm-c]({{page.5pm_url}}/5) <br/> Department Statistics | [F20-6pm-c]({{page.6pm_url}}/5) <br/> crud operations |  [F20-7pm-c]({{page.7pm_url}}/5) <br/>  Message Display Improvements|
| d | Scott | Tanay | [F20-5pm-d]({{page.5pm_url}}/6)<br/> Basic Course Search UX + CSV |[F20-6pm-d]({{page.6pm_url}}/6) <br/> course info |  [F20-7pm-d]({{page.7pm_url}}/6) <br/> Custom Search via Google|
{:.table .table-sm .table-striped .table-bordered}

In the "planning" column, on each of your pages, there is one issue that is labelled as an "Epic".   

This issue should remain in your "planning" column on your board throughout the remainder of the course.   You can refer to it to come up with the issues that you'll work on throughout the remainder of the quarter.

Each of your teams has a Kanban board, shown in this table:

| | TA | LA | 5pm | 6pm | 7pm|
|-|-|-|-|-|-|
| a | Mara | Andrew | [F20-5pm-a]({{page.5pm_url}}/3) <br/> Searches | [F20-6pm-a]({{page.6pm_url}}/3) <br/> public/member facing |  [F20-7pm-a]({{page.7pm_url}}/3) <br /> Search by user, summarize message data by user|
| b | Mara | Bryan  | [F20-5pm-b]({{page.5pm_url}}/4) <br/> Personal Schedule | [F20-6pm-b]({{page.6pm_url}}/4) <br/> admin dashboard|  [F20-7pm-b]({{page.7pm_url}}/4) <br/> Slack Bot |
| c | Scott | Gabriel | [F20-5pm-c]({{page.5pm_url}}/5) <br/> Department Statistics | [F20-6pm-c]({{page.6pm_url}}/5) <br/> crud operations |  [F20-7pm-c]({{page.7pm_url}}/5) <br/>  Message Display Improvements|
| d | Scott | Tanay | [F20-5pm-d]({{page.5pm_url}}/6)<br/> Basic Course Search UX + CSV |[F20-6pm-d]({{page.6pm_url}}/6) <br/> course info |  [F20-7pm-d]({{page.7pm_url}}/6) <br/> Custom Search via Google|
{:.table .table-sm .table-striped .table-bordered}

Each of these Kanban boards should have these columns:

| Planning | Todo | In Progress | In Review | Done |
|-|-|-|-|-|
| Your teams epic, and issues in the planning stages | Issues that are fully ready for someone on the team to pick up and work on | Issues that someone on the team is currently actively working on | Issues for which there is a pull request ready for review or being reviewed | Issues where the PR has been merged to `main`|
{:.table .table-sm .table-striped .table-bordered}

These Kanban boards started with one card on them, in the TODO column, representing an Epic.

Each team was asked to:
* add a "planning" column at the far left of the Kanban board
* drag the epic card into this planning column
* turn that epic into a series of stories (first as cards, then as issues)
* as/when the stories have sufficient detail on them to be ready to work on, drag those into the TODO column.

# Reviewing from Thursday

* There is a template (see last Thursday's lecture notes) for an issue
* That template has these parts (explained in last Thursday's lecture notes)
  - User Story
  - Acceptance Criteria
  - Implementation Todos for front end, back end and testing

# Tasks for today: 

1. Set up a shared Auth0 tenant
2. Getting your team's repo running on Localhost
3. Getting your team's repo running on your team's private Heroku deployment
4. Understanding the stories that the team will get started on

Your task today (and continuing into tomorrow's lecture as needed) is work as a team to 
- decide what stories you will start on first
- assign each person on the team to exactly one story (in some cases in pairs, or mobs (see [Mob Programming](https://en.wikipedia.org/wiki/Mob_programming))
- work to understand exactly what you'll need to do to implement the story at a high level

By "understand at a high level", what I mean is exploring questions such as these:
- Are you working in the front end, back end, or both?
- What existing files would you likely be touching?  
- What new source code files would you be creating?
- What is the role of each of those source code files?
- What non-programming tasks (e.g. setting up Auth0, MongoDB, Heroku) would be involved in your story?
  
  
# What about coding?

My guess is that many teams wont be ready to start coding in earnest until after Tuesday, or perhaps even until the Monday after Thanksgiving Break.

The deadline, by the way, for final pull requests to be ready to review is midnight on Wednesday Dec 9.  In the final lecture on Thursday Dec 10, we'll 
be doing only code reviews and testing.

The final exam slot on Tuesday, December 15, 2020 4:00 PM - 7:00 PM will be for demos:

* 4pm - 5pm, proj-ucsb-courses-search (normally 5pm section)
  - 4:05-4:15: team-5pm-a
  - 4:15-4:25: team-5pm-b
  - 4:25-4:35: team-5pm-c
  - 4:35-4:45: team-5pm-d
  - 4:45-4:50  wrap up
  - 4:50-5:00  break (or overflow time if needed).
* 5pm - 6pm, proj-ucsb-cs-las (normally 6pm section)
  - Divided in a similar manner
* 6pm - 7pm, proj-mapache-search (normally 7pm section)
  - Divided in a similar manner

Anyway, back to coding: if/when you do start coding, please note that you should do it in this manner:

1. **ALWAYS START BY CREATING A BRANCH**.  You should not be making changes directly to `main`.
   
   To create a fresh branch off of main, do this:
   * `git fetch` (to update the cloned local repos information about each branch)
   * `git checkout main` ( to get yourself on the main branch; you'll create a new branch from `main`)
   * `git pull origin main` ( to update `main` to the latest before you start).
   * Create a new branch, following this naming convention: `git checkout -b `6pm-b-NewThingWeAreDoing`
 
   That naming convention is <tt><i>section</i>-<i>team</i>-<i>description</i></tt> where:
   *  <tt><i>section</i></tt> is `5pm`, `6pm` or `7pm`
   *  <tt><i>team</i></tt> is `a`, `b`, `c`, or `d`, and
   *  <tt><i>description</i></tt> is a camel, snake or kebab case very short description (no spaces or special chars) of the new feature you are implementing, e.g. `crud-for-courses`, `slack-bot-mapache-command`, `search-by-ge`, etc.

   It may not be clear right now why having a branch naming convention is important.  It will become more clear as you begin working and 
   need to coordinate with  members of your team and other teams on merging pull requests, and resolving merge conflicts.  Being able to see
   at a glance where a given pull request is coming from and what it's trying to accomplish is quite handy.
   
2. Work on the branch.   Do all your commits to that branch, and push it frequently

   * `git add filename1 filename2 filename3`
   * `git commit -m "xy - what you changed and why"`  (xy are your initials; make it xy/ab/jk if multiple team members are involved)
   * `git push origin 6pm-b-NewThingWeAreDoing`  (push changes to your branch)

3. When you are done, do a pull request to the `main` branch



   
[Edit Page](https://github.com/ucsb-cs156/f20/edit/main/_lectures/lect21.md)
