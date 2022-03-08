---
num: "Lecture 26"
lecture_date: 2022-03-07
desc: "Tue Discussion: Continue work on team04, more notes on PRs"
ready: true
---

# The PR boards (staff and students alike, review these)

It's important to keep the PR pipeline flowing.

So staff, please spend some time reviewing the status of PRs here.

Students, do likewise.

| PR List |
|---------|
| <https://github.com/ucsb-cs156-w22/team04-w22-5pm-courses/pulls> |
| <https://github.com/ucsb-cs156-w22/team04-w22-5pm-HappyCows/pulls> |
| <https://github.com/ucsb-cs156-w22/team04-w22-6pm-courses/pulls> |
| <https://github.com/ucsb-cs156-w22/team04-w22-6pm-HappyCows/pulls> |
| <https://github.com/ucsb-cs156-w22/team04-w22-7pm-courses/pulls> |
| <https://github.com/ucsb-cs156-w22/team04-w22-7pm-HappyCows/pulls> |
{:.table .table-sm .table-striped .table-bordered}




# Remember: sand vs. boulders

"It's easier to move sand through a pipe than boulders."

This saying is a metaphor for the fact that is is easier to code review, test, and merge small pull requests.

* They tend to have fewer merge conflicts.
* If/when they have merge conflicts, they are easier to resolve
* They are easier to test, because typically only a small number of things is changing at once

There may be a temptation to gather lots of features into one *giant* PR.  This is typically not a good idea.  There are exceptions, but even in those cases, there is a price to be paid:

* More likely to have merge conflicts
* Harder to resolve when they do happen
* Harder to test

But the biggest reason not to do this is that the whole idea of CI/CD is "Continuous Integration/Continuous Delivery".

* Continuous Integration means: integrating your changes into the default branch *continuously*
* Not all at once in a giant clump, at the tail end of the process
* But incrementally, in small pieces, over time.

One of the main reasons is that it helps you catch architectural conflicts early:

* Suppose team A and team B are heading in different, incompatible directions
* Example might include: different views on the methods/use of a class, a database table design, a set of routes, the props that a React component takes, or how a user interface will work.
* Integrating changes *early* helps you *find that out early* instead of later.
* Finding out sooner makes it easier to resolve the disagreement, and results in less "wasted effort".

# An important note about "updating from main"

Occasionally, you may see this on a PR.   

Staff  or fellow team members especially may see this when doing a code review. 
If you see this, it means that the main branch has moved on while your PR was waiting, 
so you need to incorporate those changes.  

Staff may click the indicated button when needed (and so can you):

<img width="1394" alt="image" src="https://user-images.githubusercontent.com/1119017/157315516-c2738816-3392-4dd8-a1d4-9bfdeb96f40e.png">

# That means you may need to `git pull origin branch-name` early and often

If you try to push to your branch and `git` complains, you might need to do:

```
git pull origin my-branch-name
```

That's always something you should do when starting work on a branch, even if you *think* you are the only one working
on that branch.  

If there's an open pull request, at any time, someone might update that branch from main.

Even if there isn't an open pull request, other folks on your team might have made some patch (e.g. because they saw a failing test)
so it's important to be sure your branch is up-to-date before pushing new code.
