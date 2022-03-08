---
num: "Lecture 26"
lecture_date: 2022-03-07
desc: "Tue Discussion: Continue work on team04, more notes on PRs"
ready: true
---

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
