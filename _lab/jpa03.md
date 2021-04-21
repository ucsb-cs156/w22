---
desc: "Deploying full stack app with Auth0 and Database"
assigned: 2021-04-21 17:00
due: 2021-04-27 23:00
gauchospace_url: https://gauchospace.ucsb.edu/courses/mod/assign/view.php?id=6976145&forceview=1
github_org: ucsb-cs156-s21
layout: lab
num: jpa03
ready: true
starter: https://github.com/ucsb-cs156-s21/STARTER-jpa03
---

{% include drop_down_style.html %}


This is an **individual** lab on the topic of deploying
Java web apps that use OAuth and Databases, using Heroku.

You may cooperate with one or more pair partners from your team to help in debugging and understanding the lab, but each person should complete the lab separately for themselves.

# Preliminaries

We assume that you already created a Heroku account for `jpa02`.

We also assume that you are familiar with the material in `jpa02`
concerning the following items; consult jpa02 if you find
while doing the lab that you need a refresher on any of these:

* Running a Spring Boot app on localhost on port 8080
* Connecting to a server on `localhost:8080` and dealing
  with the issues that arise if that server is running on CSIL
* Creating a new app on Heroku
* Connecting an app on Heroku to a GitHub repo, and deploying
  a branch of that repo on Heroku
* Configuring *Secrets* in a Github repo.

Also, if you are working on your own machine, you need the same
software that was needed for `jpa02`, namely:

* Java 11
* Maven
* git
* Heroku CLI

See guides for installing these on your machine at the links shown:

* Windows: <https://ucsb-cs156.github.io/topics/windows/>
* MacOS: <https://ucsb-cs156.github.io/topics/macos/>

# Step 1: Understanding what we are trying to do

## What are we trying to accomplish in this lab?

This lab, similar to `jpa02` has no programming; just like
 `jpa02` the task is simply to deploy an app on localhost
 and on Heroku.  This time, however, instead of a simple
`Hello World` type app, the app you are deploying is a full-stack
web app with:

* A front-end built in React (under the directory `./javascript`) as in `jspa01`
* A back-end built in Spring Boot (the code for this is under the directory `./src`, plus the `pom.xml` at the top level
* Auth0 integration; this allows the app to have a "login/logout" feature based on Google Accounts (e.g. your UCSB Google Account)
* An SQL database, which runs using H2 (an in-memory database) on localhost, and using Postgres when running on Heroku.

The reason we are doing this lab is that before you can
work on a full-stack legacy code webapp, you need to know how to 
deploy such an app, i.e. get it running.

There are quite a few configuration steps that are needed,
and we want to get you used to those before we start
introducing the coding challenges as well.

# Step 2: Create your repo

You should already have a repo under the course organization 
<tt>{{page.github_org}}</tt> called 
<tt>{{page.num}}-<i>githubid</i></tt>
created for you by the staff, where <tt><i>github</i></tt> 
is your github id.

If not, create one for yourself following that naming convention;
it should initially be private, and empty (no `README`, license or
`.gitignore`.)

Clone that repo somewhere and cd into it.


Then add this remote:

<tt>git remote add starter {{page.starter}}</tt>

That sets up `starter` as a remote with the code from this github repo: <{{page.starter}}>

Then do:

```
git checkout -b main
git pull starter main
git push origin main
```

# Step 3: Configure your app as documented in the README.md

The next step is to read through the [README.md]({{starter}}/blob/main/README.md)
and configure your app as indicated there.

This includes configuration for Auth0, and GitHub Actions
(the `CODECOV_TOKEN`).

The Auth0 configuration step includes copying some files
with `.SAMPLE` to files that are of the same name *without*
the `.SAMPLE` extension. Those files (the ones without the `.SAMPLE` extension) contain *secrets* so
they should *not* be committed to GitHub. 

The instruction to configure this app for OAuth are linked to from
the `README.md` in the starter repo itself, so will not repeat
them here.  Follow those instructions (which may, in turn, refer
you to instruction inside the `doc` folder of the repo.)

These instructions include setting up an account with `Auth0`; you
should be able to do so on a "free plan"; at no time should
you need to enter a credit card for activities needed in this
course.

## About Auth0

Auth0 is a third-party service that helps application
developers add OAuth support to their application.

OAuth is a protocol that allows you to delegate the login/logout
functionality (user authentication) to a third party such as
Google, Facebook, GitHub, Twitter, etc.  If you've ever used
a website that allows you to "Login with Google" or "Login With Facebook", then chances are good that app was built using OAuth.

Indeed, you've already encountered two examples of GitHub OAuth earlier in the course:
* when you used your GitHub account to log into the <https://ucsb-cs-github-linker.herokuapp.com>
* when you used your GitHub account to log into <https://codecov.io>

## Follow the instructions in the README

The instructions in the README include instructions
for deploying to both localhost, and to Heroku.  Follow those
instructions, consulting the material below and the
material in jpa02 as needed, until you have the application
working on both localhost and Heroku.

You should follow the `SETUP-FULL.md` version of the
instructions the first time, since they include
steps you need to establish your:
* Auth0 account
* Auth0 tenant
* Google client id/client secret for your Auth0 tenant

You'll be following this sequence of instructions many
times during this course.  As you get more comfortable
with it, you'll be able to follow the `SETUP-QUICKSTART.md`
version.

## Also set up the GitHub Actions secrets

In the file `docs/github-actions-secrets.md` there are instructions for configuring
GitHub Actions so that it runs the tests for both the JavaScript and Java code in the repo.

You should follow these instructions to get the CI/CD pipeline set up so that
you have a green check, and not a red X, on the main branch of your repo.

## Reminder about running your webapp on `localhost`

To get a spring boot app running on `localhost`, generally
we need to do the following:

* Perform any necessary configuration of secrets, e.g.
  in the `loc
* First, use `mvn compile` to make sure that the code compiles.

  * If you get the error about `JAVA_HOME` not being defined
    correctly, you may need this command:
    ```
    export JAVA_HOME=/usr/lib/jvm/java-11-openjdk
    ```
* Next, try `mvn test` to be sure that the test cases pass.
* Then, try `mvn spring-boot:run`.  This should start up a web
  server on port 8080 running on `localhost`

  The `mvn spring-boot:run` command is a shortcut that is provided for us to be able to run the jar file.  It does pretty much the same thing as 
  if we ran the `.jar` file and specified the class containing our `main` on the command line.


When the app is up and running, try logging in with your
UCSB Google Account.  You should then be able to create, edit
and delete todo items.

Note that at this point, each time you start up the app,
the database is recreated *from scratch* in memory.  We use
an in-memory database called H2 when running on localhost;
this saves you a lot of trouble with having to configure
a database on CSIL or on your own machine.

When we migrate to Heroku in the later steps of this lab,
we'll be using a "real" database, one where what is stored
remains even when the app is shut down.

# Step 4: Create a new Heroku App using the Heroku CLI

In this step, we'll deploy our Spring Boot application to the public internet using Heroku.

As part of the setup instructions, you likely already set up a Heroku application
with the name <tt>{{page.num}}-<i>ucsbnetid</i></tt>.

You should now be able to link this app to your repo and deploy the `main` branch,
provided you did all the other setup steps correctly.

# What if it doesn't work?

If it doesn't work, consult the troubleshooting steps in `jpa02` and try them before asking a mentor, TA, or instructor for help.


# Step 5: Adding links to repo in the README.md

Edit your README.md. You'll find some TODO items inside indicating what edits you need to make.

All quarter long, we want you to develop the habit of adjusting the  README.md in your repo to include a link to your repo.

The link to your repo may seem redundant, but it helps your mentors, TAs and instructors; when you submit your work for grading to either Gradescope or Gauchospace, having those links handy really helps us navigate through your assignments quickly to evaluate them and assign grades.

# Step 6: Submitting your work for grading

When you have a running web app, visit <{{page.gauchospace_url}}> and make a submission.

In the text area, enter something like this, substituting your repo name and your Heroku app name:

<div style="font-family:monospace;">
repo name: https://github.com/{{page.org}}/{{page.num}}-chrislee123<br><br>
on heroku: https://{{page.num}}-chrislee123.herokuapp.com<br>
</div>

Then, **and this is super important**, please make both of those URLs **clickable urls**.

The instructions for doing so are here: <https://ucsb-cs156.github.io/topics/gauchospace_clickable_urls/>


# Grading Rubric:

* (20 pts) Basic Logistics
  - Having a repo with the correct name in the correct organization with the starter code for this lab
  - There is a post on Gauchospace that has the correct content
  - The links on Gauchospace are clickable links (to make it easier to test your app)
  - README has a link to your repo.
* (20 pts) Having a running web app at <tt>https://{{page.num}}-<i>ucsbnetid</i>.herokuapp.com</tt>
* (30 pts) Running web app has the ability to login through a Google Account, and create, edit and delete TODOs.
* (30 pts) GitHub Actions runs correctly and there is a green check (not a red X) on your main branch
  - To get this part working, you need to be sure that the `CODECOV_TOKEN` and `TEST_PROPERTIES` are configured
    correctly.


