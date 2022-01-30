---
desc: "Team Project: Spring Boot Backend, part 2 (authenticated CRUD)"
assigned: 2022-01-31 12:30
due: 2022-02-08 23:59
github_org: ucsb-cs156-w22
layout: lab
num: team02
ready: true
gradescope: https://www.gradescope.com/courses/342053
starter: https://github.com/ucsb-cs156-w22/STARTER-team02
gauchospace: https://gauchospace.ucsb.edu/courses/mod/assign/view.php?id=TBD&forceview=1
qxx: w22
participation_activity_num: p05
participation_activity_date: "Monday 01/31/2022"
---


# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET

In this team project, our starter code has a full frontend and backend, however we are still focusing only on the backend part, learning these new concepts:

* Creating SQL database tables using `@Entity` and `@Repository`
* Using the Lombok annotations: `@Data`, `@NoArgsConstructor`, `@Builder`, etc.
* Implementing controller routes for CRUD operations (Created, Read, Update, Destroy)
* Writing unit tests for controller CRUD operations, including the use of:
  - Spring `MockMvc`
  - Mockito methods for creating mocks of repositories and services (`when`, `verify)
  - the idea of "dependency injection"

In addition, we'll practice further with a few concepts that we touched on in `jpa03`, but may not have fully fleshed out:
- Set up of the documentation repos, the `-docs` and `-docs-qa` repos
- Working with pull requests, and GitHub actions scripts
- Working with code coverage and mutation testing

Finally, we'll start practicing with a *Kanban Board*, which is a basic tool used by many software development organizations.
- Every organization has some approach to what is called the *Software Design Life Cycle* or *SDLC*
- Some organizations adopt a formal framework such as *Agile* or *Scrum*
- Others use a more informal or hybrid approach, choosing bits and pieces from various frameworks, keeping what works, and setting aside what doesn't.
- I put myself in that category, embracing a core principle from Agile: *Inspect and Adapt*.
- More on that later.

# What you'll do

From a process standpoint, you are working with a Kanban board.
- A Kanban board is a "visualization of work in progress"
- It typically has, at a minimum, three columns labelled "todo", "in progress", "done".  
- Additional columns may be added if there are additional stages such as 
  - column(s) for todo items that are being saved for a future time (e.g. `Future`, `Icebox`, `Backburner`)
  - column(s) for review stages between in-progress and done such as `In Review`, `QA`)
  - column(s) beyond `Done`, e.g. for `Deployed to Production`
- If you've ever worked with a Trello board, it's a similar idea.
- Originally, a Kanban board was a corkboard, and each item was an index card pinned to it with a thumbtack.
- These days, they are mostly online tools.

Here's how that will play out in detail:
1. You'll start by claming your team's `team02-teamname` repo, and setting up a Kanban board for it.
2. Next, you'll create a Kanban board with columns: `Todo`, `In Progress`, `In Review`, `Done`
3. You'll then populate the `Todo` column with a set of tasks, which are called *Issues* in the GitHub implementation of Kanban.
4. You'll then assign those tasks to members of the team, moving them into the "In Progress" as each task is assigned.  
   - You may assign tasks either to individuals, pairs, or even larger groups (so-called "mobs", as in [*Mob Programming*](https://en.wikipedia.org/wiki/Mob_programming)
   - But be sure that if you assign a task to more than one person, that each member of the pair or mob is legitimately committed to contributing to working on the task, and committed to getting it finished.
5. Once a pull request is complete for a given task, you move it into the `In Review` column
   - At this stage, you seek a code review from a member of the team that was not involved in the coding.
   - If it was a true "all-team mob", than it's fine to get a code review from someone that participated, but this is rare.
   - Also, at this stage, if the PR is not "green on CI", meaning that all of the GitHub actions scripts show green checks, this is when you 
     should address that, before merging the pull request.
6. Only when the PR is merged does the issue get moved into the done column.
