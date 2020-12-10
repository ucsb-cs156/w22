---
num: "Lecture 29"
lecture_date: 2020-12-10
desc: "Thursday: Course Wrap Up, planning for the demo"
ready: true
5pm_url: https://github.com/ucsb-cs156-f20/proj-ucsb-courses-search/projects
6pm_url: https://github.com/ucsb-cs156-f20/proj-ucsb-cs-las/projects
7pm_url: https://github.com/ucsb-cs156-f20/proj-mapache-search/projects
---

# Thank you for your patience and hard work

This course has been really challenging for all of us:
* All of the students
* All of the staff (TA/LAs/and the instructor)

I hope the struggle was worth it.

A reminder to complete online course evaluations before the deadline, which I think is sometime tomorrow (Friday 12/10/2020).

# Where things stand

* Three teams are done!
* Six teams are close to done; they just need to finish the steps of getting their PRs across the finish line:
  - Getting tests to pass
  - Fixing merge conflicts✱
  - Getting team members to do a first code review
  - Making sure the PR has a good description✱✱
* Three teams needed some extra time, and have been given an extension on getting PRs in until midnight tonight.


Notes:

✱ Fixing merge conflicts isn't necessarily a "one and done" situation.  As new code is merged into `main`, new merge conflicts that were not there before may arise. Often those
  arise because of code from **your own team** that got merged into main.   So keep an eye on your PRs.

  The same thing can happen with tests; tests that didn't fail before can start failing as code is merged to main, and you rebase on main.    So know that it isn't
  a "one and done" proposition.   You have to keep iterating until your PR gets merged.

✱✱ The **description** doesn't have to be super long.  But it should be more than just "fixed issue #30".   It should give the reader an idea, from a
user perspective, on what changed in the app.  It is helpful to note:
- What navigation does the user need to do in order to see the change?  I.e. what menu, what page, what sequence of actions?
- One way to do this is to use "before" and "after" screen shots or even better, animated gifs.  
  - The tool [Licecap](https://www.cockos.com/licecap/) which is free and open-source, and available for Windows and Mac can make animated gifs really easily that you can just drag into your description.
  - Example: [Before and after on ucsb-courses-search PR 76](https://github.com/ucsb-cs156-f20/proj-ucsb-courses-search/pull/76)
  - Example: [Before and after on mapache-search PR 64](https://github.com/ucsb-cs156-f20/proj-mapache-search/pull/64)
