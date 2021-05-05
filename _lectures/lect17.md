---
num: "Lecture 17"
lecture_date: 2021-05-05
desc: "Wed Lecture: continue team03"
ready: false
up: ✅ 
down: ❌
sep: 🔸
---

See: <https://ucsb-cs156.github.io/s21/lab/team03/>

Here's the status as of 10am this morning:

When teams are done, the following Heroku applications should be
up and running:

| Section | Team 1 | Team 2 | Team 3 | Team 4 |
|---------|--------|--------|--------|--------|
| 5pm | {{page.up}}[App](https://cs156-s21-team-5pm-1-courses.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-5pm-1-courses) | {{page.up}}[App](https://cs156-s21-team-5pm-2-courses.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-5pm-2-courses) | {{page.down}}[App](https://cs156-s21-team-5pm-3-courses.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-5pm-3-courses) | {{page.down}}[App](https://cs156-s21-team-5pm-4-courses.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-5pm-4-courses) | 
| 6pm | {{page.down}}[App](https://cs156-s21-team-6pm-1-las.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-6pm-1-las) | {{page.down}}[App](https://cs156-s21-team-6pm-2-las.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-6pm-2-las) | {{page.up}}[App](https://cs156-s21-team-6pm-3-las.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-6pm-3-las) | {{page.down}}[App](https://cs156-s21-team-6pm-4-las.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-6pm-4-las) | 
| 7pm | {{page.down}}[App](https://cs156-s21-team-7pm-1-mapache.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-7pm-1-mapache) | {{page.down}}[App](https://cs156-s21-team-7pm-2-mapache.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-7pm-2-mapache) | {{page.down}}[App](https://cs156-s21-team-7pm-3-mapache.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-7pm-3-mapache) | {{page.down}}[App](https://cs156-s21-team-7pm-4-mapache.herokuapp.com){{page.sep}}[Dashboard](https://dashboard.heroku.com/apps/cs156-s21-team-7pm-4-mapache) | 
{:.table .table-sm .table-striped .table-bordered}

I'd like to see all of those as {{page.up}} by the end of class today, so that you can start your next team activity: getting to know your legacy code app as an end user, and as an admin.

To be clear: the {{page.down}} marks are all on pages that *have not yet even attempted* to deploy the app on Heroku.  So let's briefly go over is required to get the app up on Heroku:

* You need to have set the `SPRING_PROPERTIES` environment variable by:
  - putting appropriate values into `secrets-heroku.properties` (that can be a detailed process)
  - running the script `./setHerokuEnvVars.py --app your-app-name-here`

  Here's how you see if you have `SPRING_PROPERTIES` set at all (this doesn't verify that you have correct values, but if it doesn't show up, it's 
  definitely *not* going to work:
  
   ![Checking SPRING_PROPERTIES](checking_spring_properties.gif)

* You have to actually hit the deploy button: it looks like this

  ![Deploying on Heroku](deploying_on_heroku.gif)

    
# What is a *qa deployment* of an app?

We speak of a *deployment* or *instance* of an app as a separate instance of the app running somewhere.

These app instances, one per team, are intended to be *quality assurance (qa)* deployments. 

They are to be used for testing out changes to the app so that you can be "assured" 
that they improve the "quality", before doing a pull request to merge them into the `main` branch.

# Are these instances fully separate, or do they share any data in common?

Usually, these separate instances work from separate databases; this is necessary and appropriate when
the app has read/write access to the databases.

In a few cases, they apps all share a common database; this is typically possible when the database is read only,
and the database schema (the way in which the information is structured), is not changing much, or at all:
  
Here are the details:
- For all three apps, all SQL tables are individual to each app deployment; none are shared across deployments. The only shared databases are MongoDB databases.
- For `proj-ucsb-courses-search`, all deployments use the same read-only MongoDB database that stores old course
  information.  Our schema matches that used by the ucsb developer api for course info, so it doesn't 
  change except where their API changes, which is rarely, if at all.  The course staff run scripts to update
  the data in this database. 
- For `proj-ucsb-cs-las`, the MongoDB database is read/write (for storing user logins) and is specific to 
  each deployment of the app.
- For `proj-mapache-search`, deployments for a particular quarter share a common database with information
  about the Slack workspace for that instance of CMPSC 156.    The schema matches the Slack workspace
  data export format, which changes rarely, if at all.   The course staff run scripts to update
  the data in this database.

# Getting to know your team's legacy code app

The team's qa apps can also be used to get to know the app's features, *especially the admin only features*.

You can get to know the legacy code apps as user to *some extent*, by using the three production versions:
* <https://proj-ucsb-courses-search.herokuapp.com>
* <https://proj-ucsb-cs-las.herokuapp.com>
* <https://proj-mapache-search.herokuapp.com>

However, each of the apps has "admin only" features that you need to be an administrator to access.  We generally don't give admin access on the production apps to students in the class, so to test admin features, you need to have your own instance of the app.

# Deploying Apps on Heroku: Linking requires Admin access to the repo

To deploy an  app on Heroku, the Heroku app needs to be linked to the repo by someone that has "admin" access to the repo.   This is why we created these Heroku apps on behalf of each team.   

Sometimes, teams may need an additional Heroku instance of their app.  
Here are some workarounds:

* Create a Heroku app, add one of the staff as a collaborator, and have the *staff member* do the initial
  linking of the repo to the Heroku app (the staff member can, because they have admin rights to the repo).
  After that, you can deploy the app as often as you like.   This would allow the team to have as many
  qa instances of the app on Heroku as you have slots for on your Heroku plan.
  
* Fork your own copy of the legacy code app, one in which you have full admin rights.  "Forking", in this case,
  refers to a specific GitHub feature where you can have a separate app on GitHub, with a separate owner,
  but that it linked back to the main repo.   You can do pull requests between forks of the same repo.
  
  Since you can do pull requests across forks, this would probably still be compatible with the workflows
  for the course.  However, managing forked copies of repos introduces an 
  extra layer of complexity, and offers no known advantages other than the ability to deploy on Heroku, so
  we've avoided it thus far.  
  (Some extra complications include setting up repo level Secrets for the CI/CD workflows, integration with Codecov, etc.)
