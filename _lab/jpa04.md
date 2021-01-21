---
desc: "Team Version: Deploying full stack app with Auth0 and Database"
assigned: 2021-01-20 12:30
due: 2021-01-28 23:59
github_org: ucsb-cs156-w21
layout: lab
num: jpa04
ready: true
---

This lab is a team-based lab; it is essentially the same lab as jpa03, but done at
the team level.


Detailed instructions are located in the lecture notes for 1/20/2021:
* <https://ucsb-cs156.github.io/w21/lectures/lect07/>


Check to make sure that:
* Your app is deployed on Heroku
* You can login and logout of the running app on Heroku successfully with your UCSB Google Account (i.e. your userid@ucsb.edu email address)
* You have a "green check" on GitHub for your repo, indicating that the tests are passing
* Codecov is configured correctly
* The README.md is modified correctly

At that point, one person from your team can submit on Gauchospace (on behalf of the entire team) using this link:

<https://gauchospace.ucsb.edu/courses/mod/assign/view.php?id=6022922&forceview=1>

Grading Rubric:


* A: (5 %) Inviting all team members to a shared Auth0 tenant (see note below)
* B: (5 %) Inviting all staff to your shared Auth0 tenant (see note below)
* C: (10 %) Setting up a shared Heroku app, and inviting all members of the group to it
* D: (10 %) Inviting all staff to your shared Heroku app.
* E: (10 %) Populate that Github repo with the starter code for jpa03
* F: (20 %) Configure the CI/CD pipeline, i.e. the repo level secrets for `CODECOV_TOKEN` and `TEST_PROPERTIES`
  - For full credit, repo should have green check   
  - If there are problems here, we'll give the team an opportunity to fix them.
* G: Do the setup steps to make the secrets for the app (i.e. create a `temp-credentials.txt` file),
     and then share the contents of that with your fellow team members via Slack DMs.
  - This step is not separately graded; the evidence of completion is when step H works.
* H: (30 %) The app is successfully deployed on Heroku
  - For full credit, all of the functions should work
  - This includes logging in/out, roles showing up properly, and saving "todo" items
  - We'll provide feedback on anything that doesn't work and give the teams an opportunity to fix it.
* J: (10 %) The links at the top of the README.md file are modified as indicated in the README.md template in the starter code.
