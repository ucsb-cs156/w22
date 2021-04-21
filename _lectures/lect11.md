---
num: "Lecture 10"
lecture_date: 2021-04-20
desc: "Wed Lecture: Team Standup for team01, work on team01--if done, work on jpa03"
ready: true
---

# Make a post on your team's channel

Either:
* `Team is DONE with team01` OR
* `Team is NOT DONE with team01`

# If your team is NOT DONE with team01

I think this is 7 of the 12 teams.

* Do a team standup
* Work together as a team to finish team01
* More detailed instructions below (identical to yesterdays from discussion)

Deadline is 11pm Friday night.   
 
# If team is done with team01

I think this is 5 of the 12 teams.

* Do a quick "informal" retro (your P07 participation activity for today)
  - Have a team discussion organized around "stop/start/continue".
  - First, on the slack channel, *each& person take 2 minutes to write
    - What went well and what could be improved
    - More specifically, what should you stop doing, start doing, and/or continue doing
    - Each person try to come up with at least one thing in each of those categories
  - Then discuss
* Then, start working on [jpa03](https://ucsb-cs156.github.io/s21/lab/jpa03/)
  - New individual lab on setting up a Spring Boot application that uses Authentication
  - No programming, just configuration.  Its more of the "Ops" side of what the trendy kids are calling "DevOps".
* You might all be able to get it completely finished in the 75 minutes of lecture today!
* BUT after you do your retro, if you really, really need to work on something else, that's fine 
  - But post in the slack channel so we'll know that you were here, and that you are now gone. :-)


# Reviewing the team01 instructions from yesterday

* Do your team standup (each member of team puts update on Slack channel, then discuss)
* Update PRs so that red X's become green checks (you can do this with instructions below)
* Code Review your PRs (and get code reviews from staff)
* **Important** Test your code through the swagger-ui also!
  * It is NOT ENOUGH to just test with the automated tests
  * You should ALSO test with the swagger-ui endpoint to make sure that you see real results coming back 
  * The staff will be testing each team's implementation that way ALSO, and you will lose points if your implementation doesn't *actually* work.
  * If you don't understand what this means, ask for help from staff.
* Merge your PRs
* When all PRs merged:
  1. Deploy your main branch on your team's Heroku app for team01 (see table of links below)
  2. Make sure that it actually works, using the `swagger-ui` endpoint.
  3. Then **each team member** should submit from main branch on Gradescope separately.  You should at that point get 100% on Gradescope.
  4. Then, **one team member** should submit on behalf of whole team on Gauchospace.

Then, and only then, you are all done with [team01](https://ucsb-cs156.github.io/s21/lab/team01/).

Heroku Dashboard:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-s21-5pm-1-team01](https://dashboard.heroku.com/apps/cs156-s21-5pm-1-team01)|[cs156-s21-6pm-1-team01](https://dashboard.heroku.com/apps/cs156-s21-6pm-1-team01)|[cs156-s21-7pm-1-team01](https://dashboard.heroku.com/apps/cs156-s21-7pm-1-team01)|
|[cs156-s21-5pm-2-team01](https://dashboard.heroku.com/apps/cs156-s21-5pm-2-team01)|[cs156-s21-6pm-2-team01](https://dashboard.heroku.com/apps/cs156-s21-6pm-2-team01)|[cs156-s21-7pm-2-team01](https://dashboard.heroku.com/apps/cs156-s21-7pm-2-team01)|
|[cs156-s21-5pm-3-team01](https://dashboard.heroku.com/apps/cs156-s21-5pm-3-team01)|[cs156-s21-6pm-3-team01](https://dashboard.heroku.com/apps/cs156-s21-6pm-3-team01)|[cs156-s21-7pm-3-team01](https://dashboard.heroku.com/apps/cs156-s21-7pm-3-team01)|
|[cs156-s21-5pm-4-team01](https://dashboard.heroku.com/apps/cs156-s21-5pm-4-team01)|[cs156-s21-6pm-4-team01](https://dashboard.heroku.com/apps/cs156-s21-6pm-4-team01)|[cs156-s21-7pm-4-team01](https://dashboard.heroku.com/apps/cs156-s21-7pm-4-team01)|
{:.table .table-sm .table-striped .table-bordered}

Running App:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-s21-5pm-1-team01](https://cs156-s21-5pm-1-team01.herokuapp.com)|[cs156-s21-6pm-1-team01](https://cs156-s21-6pm-1-team01.herokuapp.com)|[cs156-s21-7pm-1-team01](https://cs156-s21-7pm-1-team01.herokuapp.com)|
|[cs156-s21-5pm-2-team01](https://cs156-s21-5pm-2-team01.herokuapp.com)|[cs156-s21-6pm-2-team01](https://cs156-s21-6pm-2-team01.herokuapp.com)|[cs156-s21-7pm-2-team01](https://cs156-s21-7pm-2-team01.herokuapp.com)|
|[cs156-s21-5pm-3-team01](https://cs156-s21-5pm-3-team01.herokuapp.com)|[cs156-s21-6pm-3-team01](https://cs156-s21-6pm-3-team01.herokuapp.com)|[cs156-s21-7pm-3-team01](https://cs156-s21-7pm-3-team01.herokuapp.com)|
|[cs156-s21-5pm-4-team01](https://cs156-s21-5pm-4-team01.herokuapp.com)|[cs156-s21-6pm-4-team01](https://cs156-s21-6pm-4-team01.herokuapp.com)|[cs156-s21-7pm-4-team01](https://cs156-s21-7pm-4-team01.herokuapp.com)|
{:.table .table-sm .table-striped .table-bordered}
