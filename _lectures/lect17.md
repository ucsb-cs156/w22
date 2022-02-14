---
num: "Lecture 17"
lecture_date: 2022-02-14
desc: "Mon Lecture: Front End "
ready: true
---


# Today's Plan: Straight lecture on frontend code

We'll tackle this Epic: 
* <https://github.com/ucsb-cs156-w22/demo-spring-react-example-v2/issues/84>

That includes:
* Expanding into issues
* Grooming the issues
* Actually doing as much of the coding as we can fit into 75 minutes

The coding will involve mostly frontend skills, things we haven't done in an assignment before (but will be part of your next assignment.)

Your next team03 assignment will involve:
* Building CRUD operations for two of the three tables you added in team02 
* Adding Document and Collection objects for a MongoDB database
* Adding backend operations for list and create for a MongoDB dataset
* Adding frontend list and create for the MongoDB dataset (that's what today's lecture illustrates)

Here's a copy/paste of what the epic looked like before we started lecture (note that it might evolve as we groom the issues):

# The Epic (as it looked before we started)

In this Epic, we will add frontend support for listing and creating Students.

There isn't backend support yet for Edit and Delete, so we'll concentrate on just these two for now.

As with UCSBDate, we'll allow 
* No access for users not logged in
* Read only access for Users
* Read/Write access for Admins

We can use the UCSBDate components and pages as a model to follow.

- [ ] Add Students menu that shows up only when logged in; has only one item for regular users (List) and two items for Admin users (List and Create).   Goes to placeholder pages StudentIndexPage and StudentsCreatePage 
- [ ] Make a reusable StudentsTable component. 
- [ ] Incorporate StudentsTable component into StudentsIndexPage
- [ ] Make a reusable StudentForm component
- [ ] Incorporate into StudentsCreatePage

At each stage, make sure there is good test coverage.

 
# Tech Tip: `npx stryker run` on a single file

Running mutation testing on the entire code base can take a long time.  If you know that all of the surviving mutants are in a single file (typically the one you just added), it's wasteful to run mutation testing on the entire code base each time.

Fortunately, you don't have to.  

Suppose your mutation testing report looks like this:

![image](https://user-images.githubusercontent.com/1119017/153695047-f1b777aa-8be9-4a04-bb80-06055d534cd9.png)

Clearly all of the problems are in a single file, `src/main/components/UCSBDates/UCSBDateForm.js`

Here's how you can run  mutation testing on just that one file:

```text
npx stryker run -m src/main/components/UCSBDates/UCSBDateForm.js
```

In this particular case, the mutation testing ran in 19 seconds on the one file, vs. 68 seconds on the entire code base.


