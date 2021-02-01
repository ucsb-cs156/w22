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
