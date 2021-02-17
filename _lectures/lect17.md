---
num: "Lecture 17"
lecture_date: 2021-02-16
desc: "Tue Discussion: Starting on the Legacy Code Projects"
ready: true
courses_url: https://github.com/ucsb-cs156-w21/proj-ucsb-courses-search
las_url: https://github.com/ucsb-cs156-w21/proj-ucsb-cs-las
mapache_url: https://github.com/ucsb-cs156-w21/proj-mapache-search
courses_prod: https://proj-ucsb-courses-search.herokuapp.com
las_prod: https://proj-ucsb-cs-las.herokuapp.com
mapache_prod: https://proj-mapache-search.herokuapp.com
courses_qa: https://proj-ucsb-courses-search-qa.herokuapp.com
las_qa: https://proj-ucsb-cs-las-qa.herokuapp.com
mapache_qa: https://proj-mapache-search-qa.herokuapp.com
team_5pm_1_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-courses-search/projects/9
team_5pm_2_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-courses-search/projects/10
team_5pm_3_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-courses-search/projects/11
team_5pm_4_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-courses-search/projects/12
team_6pm_1_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-cs-las/projects/15
team_6pm_3_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-cs-las/projects/14
team_7pm_1_kanban: https://github.com/ucsb-cs156-w21/proj-ucsb-cs-las/projects/13
team_6pm_2_kanban: https://github.com/ucsb-cs156-w21/proj-mapache-search/projects/11
team_6pm_4_kanban: https://github.com/ucsb-cs156-w21/proj-mapache-search/projects/10
team_7pm_2_kanban: https://github.com/ucsb-cs156-w21/proj-mapache-search/projects/9
---


# Kanban Boards

Each of your teams now has a Kanban board.  This Kanban board is the status of your work for the rest of the quarter.

It has five columns as shown here:

| Planning | Todo | In Progress | In Review | Done |
|-|-|-|-|-|
| Your teams epic, and issues in the planning stages | Issues that are fully ready for someone on the team to pick up and work on | Issues that someone on the team is currently actively working on | Issues for which there is a pull request ready for review or being reviewed | Issues where the PR has been merged to `main`|
{:.table .table-sm .table-striped .table-bordered}

The staff has created some "issues" for you to work on, currently in the "Planning" column.

Issues start in the planning column, and stay there until the team has looked over them and decided they are ready to be picked up by a team member.

Then they go to to the "Todo" column.

Issues in "todo" can be picked up by any team member, or pair, or "mob" (three or more team members.)

When they are picked up, you assign yourself to the issue and move it to the "In Progress" column.

At that point, you create a branch of the repo, and you start working on the issue in that branch.

e.g. if you are on team `team-5pm-3` and your story is to fix the footer, you might decide to call your branch `5pm-3-fixFooter`.

```
git clone ssh-url-of-repo-goes-here
cd repo-name
git checkout main
git checkout -b 5pm-3-fixFooter
```

*PLEASE ALWAYS* prefix your branch name with the name of your team (e.g. `5pm-3`, `7pm-1`).

Then make a comment on the issue with the branch name.

Then start working on the issue.  

# Write meaningful commit messages! 

Your team will be graded on a random sample of its commit messages.  So please hold one another accountable for writing good ones.

Here's some advice: <https://ucsb-cs156.github.io/topics/git_commit_messages/>

# `git push origin branch-name`

You are no longer pushing to `main`.  You are pushing to your branch name, and then you'll do a Pull Request.

We'll talk more about pull requests in lecture tomorrow.
