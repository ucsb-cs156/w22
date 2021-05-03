---
desc: "Team Project: Front End: Javascript, React, Jest, Stryker"
assigned: 2021-05-03 12:30
due: 2021-05-12 11:59
github_org: ucsb-cs156-s21
layout: lab
num: team02
ready: false
gradescope: TBD
starter: https://github.com/ucsb-cs156-s21/STARTER-team02
gauchospace: https://gauchospace.ucsb.edu/courses/mod/assign/view.php?id=TBD
---

# NOT READY YET
# NOT READY YET
# NOT READY YET

Please don't start until the staff indicates that this is ready to start and the notices above are removed.

# Second team programming assignment: Front End coding with Javascript, React, Jest

This is a team programming assignment.  Each team has it's own repo to complete this assignment, and
you will work as a team.

Here are the links to the repos:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[team01-s21-5pm-1](https://github.com/ucsb-cs156-s21/team01-s21-5pm-1)|[team01-s21-6pm-1](https://github.com/ucsb-cs156-s21/team01-s21-6pm-1)|[team01-s21-7pm-1](https://github.com/ucsb-cs156-s21/team01-s21-7pm-1)|
|[team01-s21-5pm-2](https://github.com/ucsb-cs156-s21/team01-s21-5pm-2)|[team01-s21-6pm-2](https://github.com/ucsb-cs156-s21/team01-s21-6pm-2)|[team01-s21-7pm-2](https://github.com/ucsb-cs156-s21/team01-s21-7pm-2)|
|[team01-s21-5pm-3](https://github.com/ucsb-cs156-s21/team01-s21-5pm-3)|[team01-s21-6pm-3](https://github.com/ucsb-cs156-s21/team01-s21-6pm-3)|[team01-s21-7pm-3](https://github.com/ucsb-cs156-s21/team01-s21-7pm-3)|
|[team01-s21-5pm-4](https://github.com/ucsb-cs156-s21/team01-s21-5pm-4)|[team01-s21-6pm-4](https://github.com/ucsb-cs156-s21/team01-s21-6pm-4)|[team01-s21-7pm-4](https://github.com/ucsb-cs156-s21/team01-s21-7pm-4)|
{:.table .table-sm .table-striped .table-bordered}


# Part 1: Team divides up the work

# Step 1.1: Pull in Starter Code

One member of the team, it doesn't matter who, should pull in the starter code.

I suggest you do this in your breakout room, with the whole team watching, and the team member that is doing the work
sharing their screen.

That member should:
1. Clone the team's repo
2. Add a remote for the starter code, which is here: <{{page.starter}}>
3. Checkout the main branch (`git checkout -b main`)
4. Pull from the starter remote (`git pull starter main`)
5. Push to the origin repo (`git push origin main`)

# Step 1.2: Deploy the repo, as is, to Heroku

A member of your team should:

1. Visit the Heroku Dashboard, and create a Heroku app with the name `cs156-s21-5pm-1-team01`, substituting in your team number in place of `5pm-1`.
2. On the deploy screen, link your Heroku app to your team's repo, and deploy the main branch.
3. When the app is deployed, you should be able to navigate to the link below for your team, and launch the application.

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

The result of visiting the home page of the app in the browser should be something like this:
   
```json
{"api-documentation":"http://localhost:8080/swagger-ui/","greeting":"Greetings from Spring Boot","repo":"https://github.com/ucsb-cs156-s21/STARTER-team01","team":["Andrew L.","Bryan T.","Calvin J.","Jacqui M.","Mara D.","Max L.","Phill C.","Wade V."]}
```
   
It might also be nicely formatted, depending on whether you have any browser extensions installed for processing JSON:
```json
{
  api-documentation: "https://starter-team01.herokuapp.com/swagger-ui/",
  greeting: "Greetings from Spring Boot",
  repo: "https://github.com/ucsb-cs156-s21/STARTER-team01",
  team: [
    "Andrew L.",
    "Bryan T.",
    "Calvin J.",
    "Jacqui M.",
    "Mara D.",
    "Max L.",
    "Phill C.",
    "Wade V."
  ]
}
```

At a later step (Step 3.2) you'll customize this with links for your team and with the names of your team members.  But we're getting ahead of ourselves.

# Step 1.3: Give team and staff access to your Heroku Deployment

Please visit the `Access` tab of the Heroku Dashboard for your deployed app.

Add each of the members of your team.

Then also add the assigned LA and TA for your team.   
* You can find their names here: `https://ucsb-cs156.github.io/s21/info/teams/`
* To get the email that you should use for Heroku, dm them on the slack.
* Then add `phtcon@ucsb.edu`, the instructor for the course.


# Step 1.4: Divide up the six controllers among your team

This step is a part of participation assignment (P04), in class on Monday 04/11/2021. 

Now in the README.md, towards the top, there is a place where you need to divide up the work among the team 
members.  There are six services, and six matching controllers that you need to implement and write tests
for; divide these up so that each team member is assigned to at least one of these.
   
Find the table that looks like this, and fill it in, dividing the work among the team members.
   
There are six service/controller pairs: you need to go into your team's slack channel and claim one:
   
* Location look up (enter a string, get back locations in the world along with their latitude/longitude)
* Look up public holidays (enter a year and a country code), get back public holidays
* Reddit query (enter a subreddit name, get back recent reddit posts; whomever does this one needs to have 
     a reddit account.)
* Tides query (enter a start and end date, and a station id, get back high and low tides during that period)
* University query (enter part of a university name, get back all matching universities)
* Zip Code query (enter a zip code, get back information about that zip code).

Each member of the team is responsible for implementing one of these services, the matching controller, and
the tests that go along with them.

**NOTE: to get the participation grade for today's discussion seciton, you MUST actually post in the team slack channel
which of the six you are claiming.  If you are not present in discussion, you might get assigned one of these by your team.
But you only get the particpation grade if you were actually in discussion as evidenced by your post to the Slack.**

# Step 1.5: Document the division in your README.md file

This step is also part of participation assignment (P04), in class on Monday 04/11/2021. 

In the README, there is a table that looks like this.  Someone on the team should fill in the first two columns 
of the table with the name of the team members that will implement each of the services.  

On teams with fewer than six members, after each person has done one, whoever finishes first can help the
team by completing the unfinished one.  *However, each team member must contribute at least one of the services*
*and controllers, with commits and pull requests in their name.*


```
|   Name    | GitHub Id |  Service                    | Controller                |
|-----------|-----------|-----------------------------|---------------------------| 
|           |           | `LocationQueryService`      | `LocationController`      |   
|           |           | `PublicHolidayQueryService` | `PublicHolidayController` |   
|           |           | `RedditQueryService`        | `RedditController`        |   
|           |           | `TidesQueryService`         | `TidesController`         |   
|           |           | `UniversityQueryService`    | `UniversityController`    |
|           |           | `ZipCodeQueryService`       | `ZipCodeController`       |
```
   
Note that after you add the names, the lines might not line up in the source code.  Don't worry; the table will still look fine as a formatted table.  

Example: notice the wavy lines...

```
|   Name    | GitHub Id |  Service                    | Controller                |
|-----------|-----------|-----------------------------|---------------------------| 
|           |           | `LocationQueryService`      | `LocationController`      |   
| Bryan T.  | btk5h     | `PublicHolidayQueryService` | `PublicHolidayController` |   
| Wade V.   | WadeVaresio | `RedditQueryService`        | `RedditController`        |   
| Jacqui M. | JacquelineMai | `TidesQueryService`         | `TidesController`         |   
|           |           | `UniversityQueryService`    | `UniversityController`    |
| Mara D.   | mara-downing | `ZipCodeQueryService`       | `ZipCodeController`       |
```
   
Then notice the rendered table looks fine:


|   Name    | GitHub Id |  Service                    | Controller                |
|-----------|-----------|-----------------------------|---------------------------| 
|           |           | `LocationQueryService`      | `LocationController`      |   
| Bryan T.  | btk5h     | `PublicHolidayQueryService` | `PublicHolidayController` |   
| Wade V.   | WadeVaresio | `RedditQueryService`        | `RedditController`        |   
| Jacqui M. | JacquelineMai | `TidesQueryService`         | `TidesController`         |   
|           |           | `UniversityQueryService`    | `UniversityController`    |
| Mara D.   | mara-downing | `ZipCodeQueryService`       | `ZipCodeController`       |
{:.table .table-sm .table-striped .table-bordered}
