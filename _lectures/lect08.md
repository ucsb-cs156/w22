---
num: "Lecture 08"
lecture_date: 2022-01-24
desc: "Mon Lecture: Intro to JavaScript / React"
ready: true
cra_custom: https://github.com/ucsb-cs156-w22/demo-cra-customized
---

# Announcements

* Conrad's office hours will be 3:30-4:30pm today instead of 2pm-3pm as usual.
* This means they will overlap a bit with Andrew's.  
* We might use breakout rooms to manage this.

# Return to in-person instruction

* We'll be in SH 1431 starting next Monday


# Remote options during in-person instruction

There are several important points I want to convey.  I'm numbering them so that if you have questions about any of these, you can refer to them by number.

1. I will be complying with the University's requirement that I offer CMPSC 156 as an in-person class starting on January 31st.
2. This course does have required synchronous participation requirements.
3. I never, ever, want any student or staff member to feel pressured to come to class in person during a time that they:
   - feel sick, and would not be comfortable in a classroom
   - are concerned that they may be contagious and would spread infecton (Covid-19 or anything else, cold, flu, etc.) to others.
   - are experiencing other life-circumstances that would make in-person attendance excessively burdensome
4. Accordingly, I will offer 
   - simultaneous live zoom, and recordings for all direct instruction from the course staff
   - zoom office hours by me and course staff
5. I will also be inviting, suggesting, strongly encouraging all teams to make their group meetings during class and outside of class
   "zoom friendly", i.e. conduct them in hybrid fashion where needed to allow team members to participate remotely.

This last point is the one that requires some reflection and discussion on your part.

So I'm going to ask you, in your breakout rooms today to make a post saying:

* I prefer to come in person to SH1431 for lecture / discussion (except in circumstances where I myself may be sick)
* I prefer to work from home over Zoom at all times
* I am unsure, and would like the ability to decide later.

Then, to discuss in your teams whether you are comfortable with making space for one another to participate in a hybrid fashion.

If so, please record that decision in your team's chat room.

If there is not a consensus on that, please record that there is not a consensus on allowing for hybrid, so that I can follow up as needed.

Note that there are several cases:
1. Teams that are comfortable with hybrid, and will likely be hybrid during every class (i.e. at least some team members are likely
   to just stay remote most or all of the time.)
2. Teams that are comfortable with hybrid, but where it will likely only be used in the case of an unexpected illness; all team
   members prefer in-person and intend to be in-person except when remote is necessary due to illness.
3. Teams where the team cannot reach consensus on being ok with hybrid team meetings, and thus there is no-continency plan for
   participation of someone if they are sick.
4. Possibly other cases I haven't thought of.

Cases 1 and 2 are fine.  Case 3, I honestly am not sure what to do about; we'll just have to handle that if/when it arises.  (Case 4, by definition, I cannot plan for in advance.)
  
# Treating One Another With Grace And Kindness

One of the most important lessons any of us can learn is to treat one another with grace and kindness.

I hope that this idea appeals to you intuitively.  But in case not:
* This isn't necessarily just mushy psychobabble.
* If you can build  a culture of grace, kindness and respect in a software team, or at a company, 
  it can be a real *strategic advantage* from a business standpoint.
* Employees will be more loyal, there is less turnover, and staff are more productive.

So, I'd like to apply that general principle to this specific situation:

Note that there may be cases where "I prefer to work from home" is actually a way of
referring to a required accomodation for a documented reason while maintaining confidentiality.

Ideally:
* For privacy reasons, it should be up to individual students to either self-disclose or not self-disclose about required accomodations.
* The nature of group work in this course makes that tricky.   In a course where students interact only with the instructional staff,
  and not with one another, maintaining that confidentiality is a lot easier.

So: 
* This could be a difficult uncomfortable conversation.  
* But it doesn't have to be.
* Let's see if we we can show grace and patience with one another.

I would like to invite you all, out of respect for your fellow classmates to:

* If someone expresses a "preference" to work from home over Zoom at all times, to make space for the possibility that this 
  might be a face-saving way to avoid disclosure of private information (i.e. that they
  have a required-by-law remote instruction accomodation, but that they would simply
  prefer not to disclose this.)
* If anyone does disclose that they have a required work from home accomodation, that you treat this as confidential,
  discuss it only within your team, and then only when absolutely necessary for a work-related reason 
  (not just as a matter of "conversation").
* Make space for the fact that some students may feel that in-person instruction is
  what they are paying for, and what they have a right to expect
* Make space for the fact that some students, despite not meeting any strict criteria
  for required accomodations for medical/disability reasons, may nevertheless have
  good reasons for wanting/needing to work from home.

Then, as a team, discuss if you are comfortable making space for one another's preferences.

My hope is that there will be harmony, and a recognition of 

# Checking in about the status of team01


Each person please make a post in the team slack; you can copy paste this text, and then change the `y/n` to either `y` or `n`:

```
* y/n: Started coding
* y/n: Controller/Service working in Swagger on localhost
* y/n: Tests passing on localhost
* y/n: Instructor tests for my controller/service passing on Gradescope
* y/n: Mutation testing 25/25 on Gradescope
* y/n: Pull request made
* y/n: Pull request code reviewed by another team member
* y/n: Pull request merged
```

In addition, please make a post describing any blockers/questions/problems you may have with completing your part of the project
before the deadline, or state, "no blockers".

Then:

* Handle any code reviews that need work
* Merge any PRs that are ready to merge
* Delegate the task of the Home Controller to someone on the team (i.e. editing the names in the home controller, and the test 
  for the home controller).
* Delegate the task of submitting the team submission on Gauchospace.
  - One suggestion is to do this live during your breakout room session either today, Tuesday during section, or Wednesday
* Check the team submission on Gauchospace.


# Introduction to JavaScript and React

We may not get to this today.  But if we do:

Create React App 
* <https://create-react-app.dev/> describes a script that can be used to create a React app.
  ```
  npx create-react-app my-app
  cd my-app
  npm start
  ```
* If there's time, I'll demonstrate the script live, or you can just try it yourself
* You can also look at <https://github.com/ucsb-cs156-w22/demo-cra-plain>
* The app created is already a `git` repo (but not a GitHub repo)

To make a Create React App repo into a GitHub repo
* Create an empty repo 
  - to keep things sane, I suggest using the same name as what you put on the command line after `npx create-react-app`, e.g. `my-app`
* Copy the ssh url for the repo
* cd into the directory
* Enter these commands to set up a remote called `origin`, and then push the contents to GitHub
  ```
  git remote add origin ssh-url-of-the-repo
  git checkout -b main
  git push origin main
  ```
  
# Customized Version of Create React App

I am working on a customzied version of Create React App here:
* <https://github.com/ucsb-cs156-w22/demo-cra-customized>

I started with a plain vanilla create react app.  I then proceeded by a series of PRs to customize it in 
various ways for use in CMPSC 156.

You can find a full list of [merged PRs at this link](https://github.com/ucsb-cs156-w22/demo-cra-customized/pulls?q=is%3Apr+is%3Amerged), but here
is a list of what's been done so far as of the time of this lecture:

| Pull Request | Description |
|--------------|-------------|
| [pull/1]({{page.cra_custom}}/pull/1) | move everything into frontend directory |
| [pull/2]({{page.cra_custom}}/pull/2) | create directory structure |
| [pull/3]({{page.cra_custom}}/pull/3) | add github actions script for frontend-tests  |
| [pull/4]({{page.cra_custom}}/pull/4) | add bootstrap and a basic layout, some example componets/pages, tests  |
| [pull/5]({{page.cra_custom}}/pull/5) | add storybook  |
| [pull/6]({{page.cra_custom}}/pull/6) | refine QA storybook GitHub workflow to support multiple QA storybook branches  |
| [pull/7]({{page.cra_custom}}/pull/7) | modify workflow for production docs to include putting in the index.md file  |
{:.table .table-sm .table-striped .table-bordered}

In Progress:
* Adding in Stryker mutation testing
* Add ESLint and a Github actions script for it.


  
