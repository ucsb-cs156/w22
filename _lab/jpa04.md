---
desc: "ArrayList, Sorting, Comparators, Lambdas"
assigned: 2020-11-02 17:00
due: 2020-11-09 23:00
layout: lab
num: jpa04
ready: true
course_org: https://github.com/ucsb-cs156-f20
starter_repo: https://github.com/ucsb-cs156-f20/STARTER-jpa04
gradescope: https://www.gradescope.com/courses/126922/assignments/814483
---

<style>


summary { 
   border: 4px solid green;
   padding: 1em;
   background-color: #ffe;
   margin-bottom: 1em;
}

details { 
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: auto;
  margin-right: auto;
  width: 80%;
  border: 4px solid blue;
  padding: 1em;
  }


</style>

This assignment is `jpa04`, i.e "Java Programming Assignment 04".

If you find typos or problems with the lab instructions, please report
them on the #typos channel on Slack

In this lab:

-   using `ArrayList`
-   sorting with Comparators
-   more practice with writing JUnit tests

# Preparation

Before starting this lab, you should understand how to use the built-in methods for sorting
in Java, which rely on an understanding of:

* interfaces
* `java.lang.Comparable`
* `java.util.Comparator`

These concepts are covered in these online exercises and videos:

* Exercises
  [ex14](https://ucsb-cs156.github.io/tutorials/student_ex14/) and
  [ex15](https://ucsb-cs156.github.io/tutorials/student_ex15/) on sorting by implementing
  `Comparable` and using `java.util.Collections.sort(arraylist)`;
* [Lecture Video from Tue 10/27 on Gauchocast](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=f8c552d7-1daa-4def-9daf-ac62002435a6) that goes with [ex14](https://ucsb-cs156.github.io/tutorials/student_ex14/) and
  [ex15](https://ucsb-cs156.github.io/tutorials/student_ex15/).

* Exercises
  [ex16](https://ucsb-cs156.github.io/tutorials/student_ex16/) and
  [ex17](https://ucsb-cs156.github.io/tutorials/student_ex17/) on sorting by implementing
  `Comparator` and using `arraylist.sort(comparator)`;
  
* Lecture Video from [Thu 10/29 on Gauchocast](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=76306c97-cb85-42c7-b484-ac6400feeaec) that goes with [ex16](https://ucsb-cs156.github.io/tutorials/student_ex16/) and
  [ex17](https://ucsb-cs156.github.io/tutorials/student_ex17/).


## Working in a pair?

You have the option to work in a pair on this assignment.

To set up a pair repo, see these instructions: [Pair Repo Setup](https://ucsb-cs156.github.io/topics/git_pair_repo/).

In addition:
* Read about [Strong Style Pairing](http://llewellynfalco.blogspot.com/2014/06/llewellyns-strong-style-pairing.html) and consider trying it.
* If you are working in aSwitch navigator/driver frequently and tradeoff who commits

If you are in your repo directory, and type `git log` at the command
line, you'll see a list of the commits for your repo.

Record that you are pairing on each commit message by putting the
initials of the pair partners at the start of the commit message.

E.g. If Selena Gomez is driving, and Justin Timberlake is
navigating, and you fixed a bug in your `getDanceMoves()` method, your
commit message should be `SG/JT fixed bug in getDanceMoves()`

We should see frequent switches between SG/JT and JT/SG.

When remote pairing, this means switching who is sharing their screen:
* The person driving pushes the repo.
* You switch who is sharing the screen
* Then, the other person pulls from the repo.

Step-by-Step
============

# Step 0: Set up your repo

When cloning your repo, be sure to use *only the ssh* links.
* Using the `https` link may result in an error when you try to push the to the repo,
  indicating that "a GitHub Action cannot be accessed from an OAuth login" or something like that.
* Using ssh instead of https gets around this problem.

You may work individually or as a pair on this lab.  However, if you work as a pair, please:
* Pair with someone from your same team, or at least, from your same
  discussion section.
* Remember to name the repo correctly, and also to add your pair on [Gradescope]({{page.gradescope}}) each time you submit

The starter code is in <{{page.starter_repo}}>.  Visit that page for the approrpiate URL to add the `starter` remote.

To add the starter as a remote, cd into the repo you cloned, then do:

<div>
<tt>git remote add starter {{page.starter_repo}} </tt>
</div>

Then do:
```
git checkout -b main
git pull starter main
git push origin main
```

That should get you set up with the starter code.


# Step 1: Copy code from your `jpa01` submission.

This lab builds on your `jpa01` submission.  In `jpa01`, there were two classes in the starter code, both inside the package `edu.ucsb.cs56.pconrad.menuitems`:


| Class Name | File Name |
|------------|-----------|
| `MenuItem` | `src/main/java/edu/ucsb/cs56/pconrad/menuitems/MenuItem.java` |
| `MenuItemTest` | `src/test/java/edu/ucsb/cs56/pconrad/menuitems/MenuItemTest.java` |


Your starter code for `jpa04` contains these same two files, but the "original" versions
from the `jpa01` starter.  You should copy your code for both `MenuItem.java` and `MenuItemTest.java` from your `jpa01` directory into the corresponding file in your new `jpa04` directory.

Note that there are also new classes `Menu.java` and `MenuTest.java`.  Leave these alone for now;
you'll be modfiying those as part of this programming assignment.

Commit the change to the files `MenuItem.java` and `MenuItemTest.java`. As you commit the change, consider the information below about **good commit messages**.

## Write a good commit message

As you commit the change, start now with the habit writing **meaningful commit messages**.  Starting from this assignment, you may be occasionally graded on a random sample of your commit messages, with the initial rubric consisting of these parts:

* Is the commit message accurate?
* Is the commit message understandable?
* Does it convey what changed and why?

A good commit message in this case would be something like this, where `xy` are your initials:

```
git commit -m "xy - replace MenuItem and MenuItemTest classes with solutions from jpa01"
```

## Reminder of Maven Commands

Here is a reminder about the commands you'll need as you work with the code. Try them out now.

| To do this | Type this command | Notes |
|-|-|-|
| compile the code | `mvn compile` | |
| reset everything | `mvn clean` | | 
| run the tests | `mvn test` | |
| generate a report of test coverage | `mvn test jacoco:report ` | Open the file `target/site/jacoco/index.html` in a browser to read the report |
| generate a jar file | `mvn package` | |
| generate a mutation test report | `mvn test org.pitest:pitest-maven:mutationCoverage` | Open the file <tt>target/pit-reports/<i>yyyymmddhhmm</i>/index.html</tt> to see the report; note that <tt><i>yyyymmddhhmm</i></tt> will be replaced by a date/timestamp. |


# Step 3: Look at the code for the `Menu.java` and `MenuTest.java`

There are two new classes in the `jpa04` code; they live in the same package as `MenuItem.java` and `MenuItemTest.java`:

* `Menu.java`: this is a class that encapsulates a collection of `MenuItem` objects that would represent the menu in a restaurant.   The suggestion is to implement this as an `ArrayList<MenuItem>`.
* `MenuTest.java`: this is a class to test the `Menu` class's methods.


Your job in this lab is to:

* Understand the tests in `MenuTest.java`
* Understand the stubs in `Menu.java`
* Add additional test cases to `MenuTest.java` for methods that don't have test cases
* Replace the stubs in `Menu.java` with correct implementations.

In addition, there are a few additional instructor test cases for the `MenuItem.java` class
that might catch bugs that the test suite for `jpa01` missed.  So if your code has those bugs,
you may need to do some additional work in the `MenuItem.java` class as well.


# Methods you need to implement in `Menu`:

* **`Menu` constructor**: You'll see that the `Menu` class has a constructor.  That constructor currently does nothing, but it should do is set the `menuitems` instance variable to refer to an empty `ArrayList<MenuItem>` object.

* **`lookup` method**:  You'll see that there is a `lookup` method.  This method should search the `ArrayList` for a `MenuItem` object with a name that matches the parameter passed in.  If one is found, return a reference to that `MenuItem`; otherwise, return `null`.

* **`csv` method**: You'll see that there is a `csv` method.  This method returns a `String` consisting of the entire contents of the menu, one line at a time, where each line represents one item in the menu.  The lines are separated by *newline* characters.  Since the *newline* character can be different on different systems, instead of using `'\n'`, we use the value of `System.lineSeparator();` which we store in a variable called `nl`.   (You can get a better idea of what `csv()` is supposed to do by looking at the test cases for it in `MenuTest.java`).

* **`sortByName` method**: The `sortByName` method sorts the `ArrayList` that is encapsulated inside the class so that the result of the `csv` method will be sorted by `name`.  You *should not* implement your own sort (i.e. DO NOT write your own insertion sort, bubble sort, etc.). You *should* use the techniques for sorting outlined during the lectures and exercises linked to at the start of this assignment.   You may choose to make this sort be the so-called *natural ordering* for `MenuItem`, or you may choose to create an instance of `java.lang.Comparator`, using any of the methods covered in the exercises; the implementation details are up to you.

* **`sortByCategoryThenName` method**: The `sortByCategoryThenName` sorts first by the category of the item, then within each category, the items are sorted by name.   One way to approach this is to build simple comparators for category and name, and then construct a composite comparator using the `thenComparing` method, as shown in ex17.


* **`sortByCategoryThenPriceDescendingThenByName` method**: This method is described in the comment
  in the source file:

  ```java
  /**
   * Put items in categories first, where the categories are in 
   * lexicographic order.  Then sort in order of descending price,
   * with most expensive items first, and least expensive items last.
   * Break ties of items within a category that have the same price
   * by putting them in lexicographic order.
   */
   ```

   This is certainly a case where creating simple comparators for category, name and price
   first, then using the `thenComparing` and `reversed` methods is likely the easiest
   approach.


## Checking the tests

To check the code against the tests that you've written, use:

* `mvn test`

To check your test coverage, use:

* `mvn clean test org.pitest:pitest-maven:mutationCoverage`

When you see that you are passing all of your own tests *and* killing off all the mutants,
you can try submitting to Gradescope.    The grade breakdown is:

* 32 points for tests for `MenuItem.java`
* 48 points for tests for `Menu.java`
* 20 points for mutation testing (i.e. your test suite kills all the mutants)

# Do I need to adjust the `CODECOV_TOKEN`?

For this lab, we are not checking that you've fixed the `CODECOV_TOKEN`.

You are encouraged to set that up, as it's good practice for future assignments, but
it is not a requirement in terms of your grade.

# End of description for {{page.num}}
