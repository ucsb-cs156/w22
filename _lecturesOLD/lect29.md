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

# CATME Survey

* A new CATME survey will open up on Friday--**shorter** than the last one.  (I've eliminated several of the longer questions.)  
* There will then be one more at the very end of the course,  even shorter than the previous ones.

Each of these counts as a participation grade.

# Where things stand

* Three teams are done!
* Six teams are close to done; they just need to finish the steps of getting their PRs across the finish line:
  - Getting tests to pass
  - Fixing merge conflicts✱
  - Getting team members to do a first code review
  - Making sure the PR has a good description✱✱
* Three teams needed some extra time, and have been given an extension on getting PRs in until midnight tonight.


## Notes:

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

# Grades

# Final Course Grades

(Repeated from syllabus)

Your grade will be made up of activities from the following categories:

* (We still have some of these to enter) Participation Grades (10%) - Each participation grade will be out of 100 points.  The grade for 10/01 is an example of this category.
  
  Particpation grades may vary: some are individual, some are team, and some (like 10/01) may be a combination of the two that adds up to 100.
  
  The lowest three participation grades will be dropped; accordingly, if you need to miss a lecture every now and then because of illness,
  internet problems, etc., it shouldn't affect your grade unless it becomes a persistent problem (in which case you should speak to the instructor as soon as possible about your situation.)

  This is also where filling out the CATME surveys, and your final presentation comes in.
  
* (COMPLETE) Homeworks / Quizzes (20 %) - These will be administered through Gradescope.  
  Some questions will be graded by hand (e.g. short answer/essay type questions), while others might be autograded
  (e.g. multiple choice, fill in the blank, true/false questions.)  These will typically be based on assigned readings.
  We will drop only the lowest two grades from this category.
  
* (COMPLETE) Auto-Graded Programming assignments (30 %) - jpa00 is an example of these programming assignments.  None of these will be dropped; you are
  responsible for all of them.   This may include individual assignments (such as jpa00), pair assignments, and/or team assignments.

* Project Grade (40%) - Your project grade will be based on your contributions during the Project phase of the course.   We'll discuss that 
  further in a few weeks, but there are details on the syllabus if you want to check them out.

  In addition, we'll be using peer evaluations through a tool called CATME to assess your individual contributions to the project's success.
  The peer evaluation may apply a multiplier to your project grade, increasing it or decreasing it, per your team's assessment 
  of your contributions.   It is important to be sure that you are meeting your committments to your team for a variety of reasons; your
  grade is among those.

To convert final averages to letter grades, a standard 10 point scale will be used, with the upper and lower ends of each range as +/- grades, except
for A+ grades, see below.  There is no "rounding up"; a grade of 86.9999 is a B and a grade of 87.0000 is a B+.

A+ grades: These may be awarded to the very best performing students in the class—but the cutoff for A+ grades will be determined at the end of the course at the discretion of the instructor (there is no pre-determined cutoff---an average of 97 or more doesn't guarantee you an A+ grade.)

# Final Presentation

You may do it live, or you may do it pre-recorded via Video (uploaded to YouTube or Vimeo, or any other video sharing service.).

Here's a tutorial [video on making demo videos from CS48 S20](https://youtu.be/k0Je8ASh4jo) (Video inception)

Based on the experience of CS48 students, **pre-recording is strongly recommended**.  You will *know for sure* in advance whether the
demo is successful, and whether or not you've hit the target length of 5-10 minutes.

Your video should be 5 to 10 minutes long, and cover these points:

* First, mention the names of the members of the team, and introduce the person narrating the video.  
  - It is ok if all the team members appear in the video.  It is also ok if only one person narrates the video on behalf of the team.
* Second, go through each of the features that your team worked on that were merged into `main`
  - Only demo the features that were merged into `main`
  - Focus in this part of the video on demoing the features from a *user perspective*, not on the technical details of how they were implemented.
* Next, if there is time remaining to reach the 5-10 minute mark, you may briefly cover any technical and/or non-technical challenges your team faced
  - You don't have to cover everything.  
  - You don't really even have to include this part if your demo already hits the 5-10 minute range.
  - If you do include this part, focus on the items that you think would be interesting to the audience (fellow students in CS156 F20, and the staff of CS156 F20). 
  - Possible items to include
    - Particularly interesting technical details of what you had to write in the code
    - Challenges in testing
    - Challenges in team communication and organization, and what you did to overcome those
* Optional: at the end, if you like, you may thank anyone that was particularly helpful to the team from the staff (TAs and LAs, or students from other teams). 
  - Please don't include thanks to me (Prof. Conrad) in the video; I don't want this to be an exercise in brown-nosing.
  - If you do want to express gratitude, feel free to share your thoughts with me on the Slack, by email, etc.  


  In the video, please:
* mention the names of the members of the team
* demo (by demonstrating in the app) each of the features your team completed that was merged into the `main` branch.

The demo should start by covering each of the features that you implemented 
