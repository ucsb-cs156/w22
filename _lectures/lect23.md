---
num: "Lecture 23"
lecture_date: 2022-03-01
desc: "Tue Discussion: work on team04"
ready: true
---


Today:

# Standup on team04

* Always start with a standup meeting
* Keep updates short—if you haven't had time to start anything yet, just say so
* But if you have gotten started, it will be helpful to bring everyone up to speed on what you've done so far.

# Sprint Planning (at a minimum, do this)

Some teams have already created a Kanban board.  For those that didn't, I  created them.  Links are in the table below.

Today, at a minimum, before your discussion section is over, please aim to:
* At a minimum, create the columns `Todo`, `In Progress`, `In Review`, `Done` on your team's board.
* We suggest that you consider splitting the `In Review` column into two columns:
  - `Team Review`: Stories/Issues/PRs that are ready for the *team* to review
  - `Staff Review`: Stories/Issues/PRs that are ready for the *staff* to review.
  This should make it easier to determine where the PRs/Issues are in the process, and who needs to take action to move things along. (Thanks Kevin H. for this suggestion.)
* Create at least a few issues in your repo 
  - NOTE that since you SHARE a repo with another team, your "Issues" column is shared with that team.
  - You can find sample issues under the `/issues` directory in your team's repo, under `epic01`, `epic02`, `epic03`, or `epic04`
  - Unlike in previous assignments, it is now *your team's responsibility* to create the Issue in GitHub, and "groom" it (i.e. add Acceptance Criteria)
  - For grooming of issues, TA Kevin Heffernan suggests this resource (about an 8 minute read): <https://www.productplan.com/glossary/backlog-grooming/>
* Make sure that each team member is assigned to at least one in-progress issue

That's the minimum bar for today's discussion section.  If you have time to do more, some suggesitons appear below the table of Kanban boards.   There are also a few reminders.

| Team | Repo | Kanban Board | 
|------|------|---------------|
| w22-5pm-1 | <https://github.com/ucsb-cs156-w22/team04-w22-5pm-courses> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-5pm-courses/projects/1) |
| w22-5pm-2 | <https://github.com/ucsb-cs156-w22/team04-w22-5pm-courses> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-5pm-courses/projects/2) |
| w22-5pm-3 | <https://github.com/ucsb-cs156-w22/team04-w22-5pm-HappyCows> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-5pm-HappyCows/projects/1) |
| w22-5pm-4 | <https://github.com/ucsb-cs156-w22/team04-w22-5pm-HappyCows> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-5pm-HappyCows/projects/2) |
| w22-6pm-1 | <https://github.com/ucsb-cs156-w22/team04-w22-6pm-courses> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-6pm-courses/projects/1) |
| w22-6pm-2 | <https://github.com/ucsb-cs156-w22/team04-w22-6pm-courses> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-6pm-courses/projects/2) |
| w22-6pm-3 | <https://github.com/ucsb-cs156-w22/team04-w22-6pm-HappyCows> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-6pm-HappyCows/projects/1) |
| w22-6pm-4 | <https://github.com/ucsb-cs156-w22/team04-w22-6pm-HappyCows> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-6pm-HappyCows/projects/2) |
| w22-7pm-1 | <https://github.com/ucsb-cs156-w22/team04-w22-7pm-courses> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-7pm-courses/projects/1) |
| w22-7pm-2 | <https://github.com/ucsb-cs156-w22/team04-w22-7pm-courses> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-7pm-courses/projects/2) |
| w22-7pm-3 | <https://github.com/ucsb-cs156-w22/team04-w22-7pm-HappyCows> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-7pm-HappyCows/projects/1) |
| w22-7pm-4 | <https://github.com/ucsb-cs156-w22/team04-w22-7pm-HappyCows> | [Kanban](https://github.com/ucsb-cs156-w22/team04-w22-7pm-HappyCows/projects/2) |
{:.table .table-sm .table-striped .table-bordered}


# Some reminders

* Unlike in previous team exercises, you do not have full admin control over the repo.
* In particular, you do not have access to push or merge directly into the default (`main`) branch.
  - It is not universal, but pretty common in industry that devs don't have direct access to push to `master`/`main`
  - Instead, there is a "process" that you have to go through to get stuff merged into `master`/`main`
* The process in this project is also the way you earn points.
* Each team shares a grade for the project, out of 100.
* You may earn up to 110 points; extra 10 count as extra credit (2.5% of course grade, max).
* What you need before a PR can be merged:
  - Linked to an issue
  - Issue is groomed with Acceptance Criteria
  - All Acceptance criteria are met
  - PR has good description
  - All CI/CD checks pass, including mutation testing
  - Approving code review from member of team that didn't work on the issue
  - Approving code review from a staff member

# You may need to rebase on main often

You are now working in a repo where more than just your own team is working.

This increases the chance for merge conflicts.

This means that you should rebase on main early and often.

The complexity of rebasing on main can range dramatically:
* In some cases, super easy!
* In others, mind-bogglingly hard

It isn't possible to write a full guide for every possible permutation of what can happen.  But we'll provide a guide to the simple cases,
and then encourage you to reach out for help if and when the complex ones arise.


# If you have time to do more than the minimum

Here are some things to do if you have time to go beyond the minimum

1. Get your qa deployments are set up.   See Slack discussion in either [`#help-proj-courses-search`](https://ucsb-cs156-w22.slack.com/archives/C0350JFKJPM/p1646172077158749) or [#help-proj-happycows](https://ucsb-cs156-w22.slack.com/archives/C034XMDFSER/p1646172600790119)
2. Make sure you can clone the repo and get it up and running on localhost.  The discussion at the previous link has some hints about reusuing your OAuth credentials.
3. Talk with the staff about the "big picture" of your sprint.   
   - That is, try to understand what it is you are trying to build.  
   - What is in scope, and what is out of scope? 
   - What does the end user want/need from this feature?
   - For courses search, Prof. Conrad, Andrew, Pranav are the ones most familiar with the app
   - For Happy Cows, Seth, Kevin, Bryan Z are the best sources
   - Bryan T is equally familiar with both.

# Some high level observations

Courses Search and Happy Cows are in vary different stages of development

For, Courses Search, this is our third major version of the app: some of the staff have been working on it for over two years now, and we really know the features very well, inside and out.

For Happy Cows, we are at a much earlier stage.  Some of the dev team (Conrad, Bryan T, and Seth V) did some maintenance programming on an earlier version of the app, and then started on a re-write using this tech stack in S21.  But we didn't very far, and there are still many things that are still being defined.

Thie means you'll have very different experiences, with different tradeoffs.

Courses Search will be a more straightforward path; the user/customer/product manager has a much clearer idea of what they want, and the staff has a pretty clear idea how to build that.

Happy Cows will be less straightforward. There is less clarity about what the finished product should look like, or the best way to get there.

You may think that this means that Courses Search folks are the more fortunate ones.  I'd suggest, though, that the experience of the Happy Cows folks is much more authentic and typical of real world coding.  They may have the better learning experience.

