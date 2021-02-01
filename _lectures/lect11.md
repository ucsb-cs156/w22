---
num: "Lecture 11"
lecture_date: 2021-02-01
desc: "Mon Lecture: jpa05, and discovery on the three apps"
ready: false
projects:
 - team: team-5pm-1
   repo: proj-ucsb-courses-search
   short: courses
 - team: team-5pm-2
   repo: proj-ucsb-courses-search
   short: courses
 - team: team-5pm-3
   repo: proj-ucsb-courses-search
   short: courses
 - team: team-5pm-4
   repo: proj-ucsb-courses-search
   short: courses
 - team: team-6pm-1
   repo: proj-ucsb-cs-las
   short: las
 - team: team-6pm-2
   repo: proj-mapache-search
   short: mapache
 - team: team-6pm-3
   repo: proj-ucsb-cs-las
   short: las
 - team: team-6pm-4
   repo: proj-mapache-search
   short: mapache
 - team: team-7pm-1
   repo: proj-ucsb-cs-las
   short: las
 - team: team-7pm-2
   repo: proj-mapache-search
   short: mapache
---

Our aim for today is to finish up jpa05; that is, for each group to have it's Heroku app (at the link below) deployed.  

The following things should be true:
* The page loads and presents a login button
* The login button allows you to login with your UCSB email address (Google Account)
* When the page loads, and you are logged in, on the Profile page, the badge shows your role ( `Admin`, `Member`, `Guest`) rather than the text `Loading Role...`).
  - Debugging this can be challenging.  Here is a start at some hints about this <https://ucsb-cs156.github.io/topics/legacy_code_roles/>.

There are additional things that should be true for each of the three apps; we'll cover those individually.

Here is a list of links to the teams and their apps:

| Team | App Name/Link to Repo | Deployed App | Heroku Dashboard |
|------|--------------|------------------|
{% for p in page.projects %} | {{p.team}} | [{{p.repo}}](https://github.com/ucsb-cs156-w21/{{p.repo}}){:target="_blank"} | [Running App](https://cs156-w21-{{p.team}}-{{p.short}}.herokuapp.com){:target="_blank"} | [Heroku Dashboard](https://dashboard.heroku.com/apps/cs156-w21-{{p.team}}-{{p.short}}){:target="_blank"} |
{% endfor %}{:.table .table-sm .table-striped .table-bordered}

For UCSB Courses Search:
* You should be able to search for courses on the main Courses Search page, and see results come up (at least in JSON format)

For UCSB CS LAs:
* 

For Mapache Search:
* You should be able to see content when you use the features that look at the Slack Channels and Slack Users
* You should be able to do Google Searches and see search results come back in JSON format
* You should be able to issue `/mapache` slack commands from your team's test slack workspace.

# Then, the 01.27 exercise

# In your team repo

Recall that each of you has a team repo for notes:

| 5pm | 6pm | 7pm |
|-----|-----|-----|
| [team-5pm-1-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-1-NOTES) | [team-6pm-1-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-1-NOTES) | [team-7pm-1-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-1-NOTES)  |
| [team-5pm-2-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-2-NOTES) | [team-6pm-2-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-2-NOTES) | [team-7pm-2-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-2-NOTES)  |
| [team-5pm-3-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-3-NOTES) | [team-6pm-3-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-3-NOTES) | [team-7pm-3-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-3-NOTES)  |
| [team-5pm-4-NOTES](https://github.com/ucsb-cs156-w21/team-5pm-4-NOTES) | [team-6pm-4-NOTES](https://github.com/ucsb-cs156-w21/team-6pm-4-NOTES) | [team-7pm-4-NOTES](https://github.com/ucsb-cs156-w21/team-7pm-4-NOTES)  |
{:.table .table-sm .table-striped .table-bordered}

In this repo, please create a new directory `01.27` and a `README.md` in that directory, as shown in this image:

![create 01.27/README.md](../lect10/create-readme.png)

In the README.md file, put a link to your jpa05 deployment.  No special syntax is needed in GitHub Flavored Markdown to get a URL to be a link:

```
Our jpa05 deployment is here: https://cs156-w21-team-5pm-1-courses.herokuapp.com/
```

Under the `01.27` directory, each of the team members should create a file with their first name followed by `.md`, e.g. `Amy.md`, `Brian.md`, `Chris.md`, etc.

Now: 
* Explore the app.   
* In your `Chris.md` file, make lists of:
  - Bugs
  - Feature suggestions
  - Improvments to the User Interface

Here is a guide to GitHub Flavored Markdown syntax: <https://guides.github.com/features/mastering-markdown/>

Do this individually first.  

Then have a group discussion about what you found, and assemble your suggestions together in one document, in the `01.27/README.md` file.

Then: 
* Read about User Stories, here: <https://ucsb-cs156.github.io/topics/user_stories/>
  * Then, for each of the feature suggestions or UX improvements, rewrite it as a user story
  * Be sure it is in the form "As a _  I can _ so that _"
    - Note the different roles for your app: Admin, Member, Guest.
    - Specify: "User" when it doesn't matter
    - Specify: "Logged in User" vs. "Logged out User" when it matters.
* Read about Acceptance Criteria here: https://ucsb-cs156.github.io/topics/agile_acceptance_criteria/
  * Then, for each of the user stories, add acceptance criteria

For examples, see the closed issue for each of the three repos:


  

