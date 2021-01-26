---
desc: "Deploying Team Deployment of Legacy Code App (Course Search/LAs/Mapache)"
assigned: 2021-01-26 17:00
due: 2021-02-03 23:59
github_org: ucsb-cs156-w21
layout: lab
num: jpa05
ready: false
proj-ucsb-courses-search: https://github.com/ucsb-cs156-w21/proj-ucsb-courses-search
proj-ucsb-cs-las: https://github.com/ucsb-cs156-w21/proj-ucsb-cs-las
proj-mapache-search: https://github.com/ucsb-cs156-w21/proj-mapache-search
---

This lab is similar to jpa04, in that you will be working as a team to set up a deployment of a Spring/React full-stack web application.

Here's what's different:
* Instead of all students in the course deploying the *same* web app, this time you will be deploying the specific legacy code application that you'll be working with later, during the project phase of the course.
  - All 5pm teams will be deploying [proj-ucsb-courses-search]({{page.proj-ucsb-courses-search}})
  - Teams team-6pm-1, team-6pm-3 and team-7pm-1 will be deploying [proj-ucsb-courses-search]({{page.proj-ucsb-cs-las}})
  - Teams team-6pm-2, team-6pm-4 and team-7pm-2 will be deploying [proj-mapache-search]({{page.proj-mapache-search}})
* The setup instructions include all of the steps you did for jpa03/jpa04, except that:
  - You will not have to do the one-time setup step to connect your shared team Auth0 tenant to a Google OAuth client id and client secret, since that should already have been done for jpa04.
  - For all three projects, you'll have the additional step of configuring a URL for a MongoDB database
  - For proj-ucsb-courses-search, you'll have an additional step of configuring an API Key for the UCSB Developer API
  - For proj-mapache-search, you'll have the additional step of configuring a Slack Bot

# Why are we doing all of this

In order to be able to work on a full stack web application, you need to be able to:
* deploy that web application on your own machine&mdash;whether that's your CSIL account, or your own computer&mdash;so that you can test the effect of your code changes.
* deploy that web application on Heroku to make sure that it works in an environment similar to the one where it will run in production.

These setup steps, as you've already experienced, can be a little complex.  We are introducing them into the course early so that you get experience with them early. 
We don't want these steps to be the stumbling blocks when you are trying to deal with the actual code changes.

# OK, I get that, but what *are* all of these steps?

We can talk more about this in lecture, and I'm happy to... just ask.  But here's a quick run down.

* Auth0 is a "middleware" service for authentication.   It sits between your application and a service such as Google.  Having Auth0 in the middle makes it easier if/when we want to 
  switch authentication methods to, say, Facebook, GitHub, Twitter, LinkedIn, or any number of other companies that could be used for authentication instead of
  Google.
* The `secrets-localhost.properties` file is a file that is read by the Java code when your application starts up; it initializes values in various places in the application code.
  It *should not be checked into GitHub* because the information it contains could be used to compromise the security of your application.
* The `javascript/.env.local` file is read at the time your application starts up, and is used to initialize values in the front-end JavaScript code.  Like
  the `secrets-localhost.properties`, it should not be checked into GitHub (for the same reason).  This file is also used by the `setHerokuVar.py` script to
  initialize a few "Config Vars" on the Settings page of your Heroku app, values that are read into the front end JavaScript code when the application first
  starts up.
* The `secrets-localhost.properties` file is used by the `setHerokuVar.py` script to
  initialize the "config vars" called `SPRING_PROPERTIES` on the Settings page of your Heroku app.   
  These values are read by the Java code on Heroku when your application first starts up.

If you have more questions, ask in lecture, in office hours, or ask the TAs/LAs during section.
  
# Steps for jpa05

Steps 1 and 2 can be delegated to individual members of your team, and done in parallel with the remainder of the steps.


## Step 1: Give everyone on your team access to your Heroku app 

On your team's slack channel, you should find a message about your jpa05 Heroku app.  The name of the app will be something like this:

Examples:
* <https://dashboard.heroku.com/apps/cs156-w21-team-5pm-1-courses>
* <https://dashboard.heroku.com/apps/cs156-w21-team-6pm-1-las>
* <https://dashboard.heroku.com/apps/cs156-w21-team-7pm-2-mapache>

Some on your team was given admin access to the app.  Identify that person.  They should add everyone else on your team, using the 
email address that person uses to login to Heroku.

If that person is not available, there is an LA designated for your team.  Ask them, or one of the TAs, or the instructor, to add someone else from your team, and then *they* can add everyone else.

## Step 2: Give everyone on the staff access to your Heroku app

On the Slack, in the channel `#course-notes`, there is a list of the email addresses of the course staff.    Some of them already have access to your app, but the rest do not.  Please add the rest of them.

## Step 3: Clone the Repo assigned to your team.

This step should be done, eventually, by each member of the team individually.  For today, though, it is sufficient for one member of the team to do it,
preferably, sharing their screen with other members looking on and helping.

Identify the repo associated with your team:

 - All 5pm teams: <{{page.proj-ucsb-courses-search}}>
 - Teams team-6pm-1, team-6pm-3 and team-7pm-1 <{{page.proj-ucsb-cs-las}}>
 - Teams team-6pm-2, team-6pm-4 and team-7pm-2 <{{page.proj-mapache-search}}>

Clone this repo on your local machine, or in your CSIL account.
