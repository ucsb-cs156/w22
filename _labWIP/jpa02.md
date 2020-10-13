---
desc: Testing
assigned: 2020-10-13 14:00
due: 2020-10-19 23:00
layout: lab
num: jpa01
ready: false
signup_app: https://ucsb-cs-github-linker.herokuapp.com/
slack: https://ucsb-cs156-f20.slack.com
course_org: https://github.com/ucsb-cs156-f20
---

This assignment is `jpa01`, i.e "Java Programming Assignment 01".

If you find typos or problems with the lab instructions, please report
them on the #typos channel on Slack

In this lab:

-   using packages
-   writing your own JUnit tests
-   test coverage using Jacoco


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

You may work individually or as a pair on this lab.  However, if you work as a pair, please:
* Pair with someone from your same team, or at least, from your same
  discussion section.
* Remember to name the repo correctly, and also to add your pair on Gradescope each time you submit

The starter code is in <{{page.starter_repo}}>.  Visit that page for the approrpiate URL to add the `starter` remote.

To add the starter as a remote, cd into the repo you cloned, then do:

<div>
<tt>git remote add starter {{page.starter_repo}} </tt>
</div>

Then do:
```
git pull starter master
git push origin master
```

That should get you set up with the starter code.

# Step 1: Get oriented to packages

A few things to notice:

* Under `src`, there are two directory trees:
   * `src/main/java/edu/ucsb/cs56/pconrad/menuitems` contains regular Java classes.
   * `src/test/java/edu/ucsb/cs56/pconrad/menuitems` contains the test classes.

Don't change the package from `pconrad` to your name; the Gradescope autograder is looking for the code under the `edu.ucsb.cs56.pconrad.menuitems` package.
So each source file:

* must be under that directory path when it is compiled, and
* must have `package edu.ucsb.cs56.pconrad.menuitems;` as the first line in the file

Here are the commands you'll need as you work with the code. Try them out now.

| To do this | Type this command | Notes |
|-|-|-|
| compile the code | `mvn compile` | |
| reset everything | `mvn clean` | | 
| run the tests | `mvn test` | |
| generate a report of test coverage | `mvn test jacoco:report ` | Open the file `target/site/jacoco/index.html` in a browser to read the report |
| generate a jar file | `mvn package` | |


# Step 2: Start writing code to make tests pass

In this lab, you'll be implementing several methods of a class called `MenuItem` that represents
item on a restaurant Menu.

(There is a follow up lab in which we will add a `Menu` class that uses these menu items; but
we need to discuss sorting, `java.lang.Comparable`, `java.util.Comparator`,
and Java lambda expressions in lecture first before we get to that.)

A `MenuItem` represents an item on the menu of a restaurant.  It has three attributes:
* the menu item name, e.g. `"Small Poke Bowl"`
* the price, in cents (e.g an item that costs $1.49 is represented by the integer 149)
* a category such as `"Beverages"` or `"Poke Bowls"`


Note that the starter code:
* Has stubs for SOME of the needed methods, but NOT ALL of them
* Has unit tests for SOME of the needed methods, but NOT ALL of them

YOU WILL NEED TO WRITE SOME OF YOUR OWN TESTS.

So you'll need to do a bit more work than you may be used to.


I suggest that you work in this order:
* <b>First, Add stubs for all of the methods that don't have them yet.</b>  
   * Until you do this, you won't be able to run any of the instructor unit tests on Gradescope.
   * The reasons is that the instructor tests won't compile against your code unless and until you have those methods.
* <b>Then, try submitting on Gradescope</b>
   * At this point, you should have a clean compile for both the student and instructor code, though you won't be passing most of the unit tests.
* Then, one at a time, work on each method
   * If the method doesn't have a unit test yet, <b>write the test first and see it fail</b>.
   * Then make the test pass.
   * Then submit on Gradescope and see if the test for that method passes on Gradescope
   * Continue until all of your methods work.


Let me say this again, because I've assigned this lab a few times now,
and each time, students fail to read this important instruction:

**YOU MUST WRITE STUBS FOR ALL METHODS** before any of the Gradescope
tests will work.  Until you write stubs for all methods, the code will
**FAIL TO COMPILE** on Gradescope, and no tests will pass.

# Details about methods of MenuItem

The constructor has the signature:
```
public MenuItem(String name,
                int priceInCents,
                String category)
```

Here are the instance methods you'll need to implement for `MenuItem`

| Modifier and Type	| Method | Description |
|-|-|
|String	| getCategory() | Returns the category of the menu item |
|String	| getName() | Returns the name of the menu item |
|String	| getPrice() | Returns the price, formatted as a string with a $.
|String	| getPrice(int width) | Returns the price, formatted as a string with a $, right justified in a field with the specified width. |
| int	| getPriceInCents() | get the price in cents only |
| String	| toString() | return a string in csv format, in the order name,price,cateogry. <br> For example: `"Small Poke Bowl,1049,Poke Bowls"`<br>In this case, the price is unformatted; just an integer number of cents. |


# Step 3: Learning about Test Coverage

Now, did you really write unit tests for all of your code? Let's check!

We can automatically compute "test case coverage", using a tool call JaCoCo (Java Code Coverage).

Read these short articles about test coverage before moving to step 4:
* <https://ucsb-cs56.github.io/topics/testing/>
* <https://ucsb-cs56.github.io/topics/testing_jacoco_reports/>

Once you've looked over those, it's time to check your test coverage, which
we'll do in Step 4.

# Step 4: Checking Test Case Coverage

Be sure that you've added your pair partner to your submissions on Gauchospace


Then, check your test coverage!

There are two ways to do it: locally, or using codecov.  Use whichever way is eeasier for you.

## Checking Test Case Coverage Locally.

* Run: `mvn test jacoco:report`
* Then, open the file `target/site/jacoco/index.html` in a browser.
   * *How* you go about that depends a lot on your setup.
   * You may be able to navigate to that file and just double click on it
     to open it.
   * On Mac, you can use `open target/site/jacoco/index.html`.

## Checking Test Case Coverage via Codecov

If your main branch shows green (i.e. all tests pass), then you should
be able to see the code coverage on Codecov.io by visiting
* <https://codecov.io/gh/ucsb-cs156-f20/REPO-NAME-HERE>

If your code is on another branch
* <https://codecov.io/gh/ucsb-cs156-f20/REPO-NAME-HERE/branch/BRANCH-NAME-HERE>


# How to read the test coverage reports

* If any line of code is red, that means it is not tested at all&mdash;it is being missed by *line coverage*
* If a line of code is yellow, it means there are multiple ways to execute the line.
   * it may have an if/else, or a boolean expression involving `&&` or `||`, and thus there are multiple paths through the code (multiple branches).  
   * Yellow means it is being missed by *branch coverage*; some branches are covered, and others are not.   
   * Think about the multiple paths through the code and be sure your tests are coverage all of them.

# Step 5: Try to get as close to 100% coverage as you can

Keep reworking your code until you get as close as you can to 100% test coverage.

As we'll discuss in lecture, 100% coverage isn't always necessary or
even desirable, but in this case you should be able to get there, or
at least pretty close.

One method that it's definitely ok to not have test coverage for (in
this particular project) is the `public static void main(String []
args)` method; that method is only there as a placeholder, and
contributes nothing to the correctness of the code.  If it did, we'd
need to consider writing tests for it (and that is possible, though a
little awkward.)

Try to get as close to 100% test coverage as you can.   In a later
lab, we'll be revisiting this code with a test technique called
"mutation testing" that will really give your test suite a workout.

# Step 6: Before final submission on Gradescope

* Make sure that your README.md file has your github id(s) and name(s) (Both if you worked as a pair.)

# End of description for {{page.num}}
