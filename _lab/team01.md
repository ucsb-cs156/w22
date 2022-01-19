---
desc: "Team Project: Spring Boot Backend, part 1 (unauthenticated RESTFul APIs)"
assigned: 2022-01-18 17:00
due: 2022-01-25 23:59
github_org: ucsb-cs156-w22
layout: lab
num: team01
ready: true
gradescope: https://www.gradescope.com/courses/342053/assignments/1766517/
starter: https://github.com/ucsb-cs156-w22/STARTER-team01
gauchospace: https://gauchospace.ucsb.edu/courses/mod/assign/view.php?id=775822&forceview=1
qxx: w22
participation_activity_num: p04
participation_activity_date: "Tuesday 01/18/2022"
---



# First team programming assignment: Spring Backend, and working with APIs

This is a team programming assignment.  Each team has it's own repo to complete this assignment, and
you will work as a team.


# What are we building?

You are building a Spring Boot webapp that *only has a backend*.  The front end code will built in a later team project.

We will use a tool called *Swagger-ui* that:
* builds a temporary front-end that can be used by developers to test the backend.
* provides a way for programmers to automatically build documentation for their backend.

If you want to see an example of what the working web app should look like, you can visit this site:

* <https://team01-w22-solution.herokuapp.com/>

This is an exercise in working with three kinds of APIs as explained in [this short article on APIs](https://ucsb-cs156.github.io/topics/apis/)

The starter code you are given contains three "controllers", each of which implements a separate backend API:

* The Java class [`EarthquakesController`](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/controllers/EarthquakesController.java) implements an API endpoint that provides information about earthquakes within a given distance from Storke Tower, that have a magnitude that is greater than or equal to some minimum specified.
* The Java class [`CountryCodeController`](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/controllers/CountryCodeController.java) implements an API endpoint that, given the name of a country, provides information about that country, including a list of latitude and longitude points that mark the outline of that country.
* The Java class [`CollegeSubredditsController`] provides an endpoint that gives a list of subreddits on the social networking site Reddit.com that correspond to various colleges and universities.   This endpoint doesn't need any input.

These three controllers, in turn, rely on three Java classes that each provide a "service".  The service provided, in each case, is a method `getJSON(p1,p2,...)` that may or may not take parameters.  The parameters are the ones that were input to each of the controllers 
* the [`EarthquakeQueryService`](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/EarthquakeQueryService.java) implements `getJSON(String distance, String minMag)` which is used by the `EarthquakesController`.
* the [`CountryCodeQueryService`](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/CountryCodeQueryService.java) implements `getJSON(String country)` which is used by the `CountryCodeController`
* the [`CollegeSubredditQueryService`](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/CollegeSubredditQueryService.java) implements `getJSON()` (with no parameters) which is used by the `CollegeSubredditsController`

For each of these controller / service pairs, there are also tests:

| Controller  | Controller Test | Service  | Service Test |
|-|-|-|-|
| `EarthquakesController` | `EarthquakesControllerTest` | `EarthquakeQueryService` | `EarthquakeQueryServiceTest` |
| `CountryCodeController` | `CountryCodeControllerTest` | `CountryCodeQueryService` | `CountryCodeQueryServiceTest` |
| `CollegeSubredditsController` | `CollegeSubredditsControllerTest` | `CollegeSubredditQueryService` | `CollegeSubredditQueryServiceTest` |


So you are given those twelve classes.   Your job, as a team, is to implement 24 more classes (4 each), i.e. one row of the following table:

| Controller  | Controller Test | Service  | Service Test |
|-|-|-|-|
| `LocationController` | `LocationControllerTest` | `LocationQueryService` | `LocationQueryServiceTest` |
| `PublicHolidaysController` | `PublicHolidaysControllerTest` | `PublicHolidayQueryService` | `PublicHolidayQueryServiceTest` |
| `RedditController` | `RedditControllerTest` | `RedditQueryService` | `RedditQueryServiceTest` |
| `TidesController` | `TidesControllerTest` | `TidesQueryService` | `TidesQueryServiceTest` |
| `UniversityController` | `UniversityControllerTest` | `UniversityQueryService` | `UniversityQueryServiceTest` |
| `ZipCodeController` | `ZipCodeControllerTest` | `ZipCodeQueryService` | `ZipCodeQueryServiceTest` |

You can see what those services will look like in Swagger by looking at this example of the finished app running:

* <https://team01-w22-solution.herokuapp.com/>

That will also give you an idea of what the documentaiton should look like when you've put in all the proper values for the various annotations (the things
that start with `@` in the code.)

# The Repos you will work in

Here are the links to the repos:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[team01-{{page.qxx}}-5pm-1](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-1)|[team01-{{page.qxx}}-6pm-1](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-1)|[team01-{{page.qxx}}-7pm-1](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-1)|
|[team01-{{page.qxx}}-5pm-2](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-2)|[team01-{{page.qxx}}-6pm-2](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-2)|[team01-{{page.qxx}}-7pm-2](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-2)|
|[team01-{{page.qxx}}-5pm-3](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-3)|[team01-{{page.qxx}}-6pm-3](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-3)|[team01-{{page.qxx}}-7pm-3](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-3)|
|[team01-{{page.qxx}}-5pm-4](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-4)|[team01-{{page.qxx}}-6pm-4](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-6pm-4)|[team01-{{page.qxx}}-7pm-4](https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-7pm-4)|
{:.table .table-sm .table-striped .table-bordered}

You will get two grades for this assignment:
* You'll get an autograded grade via Gradescope
* You'll also get a manual grade via Gauchospace; the manual grade will check that you've done
  a reasonable job of documenting your work.

# Part 1: Team divides up the work

[This video (10:53)](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=15d5a190-f7b2-4bbd-92e2-ae2101874844) walks you through the steps of Part 1. 

# Step 1.1: Pull in Starter Code

One member of the team, it doesn't matter who, should pull in the starter code.

I suggest you do this in your breakout room, with the whole team watching, and the team member that is doing the work
sharing their screen.

That member should:
1. Clone the team's repo
2. Add a remote for the starter code, which is here: <{{page.starter}}>
3. Checkout the main branch (`git checkout -b main`)
4. Pull from the starter remote (`git pull starter main`)
5. Push to the origin repo (`git push origin main`)

# Step 1.2: Deploy the repo, as is, to Heroku

A member of your team should:

1. Visit the Heroku Dashboard, and create a Heroku app with the name <tt>cs156-{{page.qxx}}-5pm-1-team01</tt>, substituting in your team number in place of `5pm-1`.
2. On the deploy screen, link your Heroku app to your team's repo, and deploy the main branch.
3. When the app is deployed, you should be able to navigate to the link below for your team, and launch the application.

Heroku Dashboard:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-{{page.qxx}}-5pm-1-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-1-team01)|[cs156-{{page.qxx}}-6pm-1-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-1-team01)|[cs156-{{page.qxx}}-7pm-1-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-1-team01)|
|[cs156-{{page.qxx}}-5pm-2-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-2-team01)|[cs156-{{page.qxx}}-6pm-2-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-2-team01)|[cs156-{{page.qxx}}-7pm-2-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-2-team01)|
|[cs156-{{page.qxx}}-5pm-3-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-3-team01)|[cs156-{{page.qxx}}-6pm-3-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-3-team01)|[cs156-{{page.qxx}}-7pm-3-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-3-team01)|
|[cs156-{{page.qxx}}-5pm-4-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-4-team01)|[cs156-{{page.qxx}}-6pm-4-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-4-team01)|[cs156-{{page.qxx}}-7pm-4-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-4-team01)|
{:.table .table-sm .table-striped .table-bordered}

Running App:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-{{page.qxx}}-5pm-1-team01](https://cs156-{{page.qxx}}-5pm-1-team01.herokuapp.com)|[cs156-{{page.qxx}}-6pm-1-team01](https://cs156-{{page.qxx}}-6pm-1-team01.herokuapp.com)|[cs156-{{page.qxx}}-7pm-1-team01](https://cs156-{{page.qxx}}-7pm-1-team01.herokuapp.com)|
|[cs156-{{page.qxx}}-5pm-2-team01](https://cs156-{{page.qxx}}-5pm-2-team01.herokuapp.com)|[cs156-{{page.qxx}}-6pm-2-team01](https://cs156-{{page.qxx}}-6pm-2-team01.herokuapp.com)|[cs156-{{page.qxx}}-7pm-2-team01](https://cs156-{{page.qxx}}-7pm-2-team01.herokuapp.com)|
|[cs156-{{page.qxx}}-5pm-3-team01](https://cs156-{{page.qxx}}-5pm-3-team01.herokuapp.com)|[cs156-{{page.qxx}}-6pm-3-team01](https://cs156-{{page.qxx}}-6pm-3-team01.herokuapp.com)|[cs156-{{page.qxx}}-7pm-3-team01](https://cs156-{{page.qxx}}-7pm-3-team01.herokuapp.com)|
|[cs156-{{page.qxx}}-5pm-4-team01](https://cs156-{{page.qxx}}-5pm-4-team01.herokuapp.com)|[cs156-{{page.qxx}}-6pm-4-team01](https://cs156-{{page.qxx}}-6pm-4-team01.herokuapp.com)|[cs156-{{page.qxx}}-7pm-4-team01](https://cs156-{{page.qxx}}-7pm-4-team01.herokuapp.com)|
{:.table .table-sm .table-striped .table-bordered}

The result of visiting the home page of the app in the browser should be something like this:
   
```json
{"api-documentation":"http://localhost:8080/swagger-ui/","greeting":"Greetings from Spring Boot","repo":"https://github.com/ucsb-cs156-w22/STARTER-team01","team":["Andrew L.","Bryan T.","Calvin J.","Jacqui M.","Mara D.","Max L.","Phill C.","Wade V."]}
```
   
It might also be nicely formatted, depending on whether you have any browser extensions installed for processing JSON:
```json
{
  api-documentation: "https://starter-team01.herokuapp.com/swagger-ui/",
  greeting: "Greetings from Spring Boot",
  repo: "https://github.com/ucsb-cs156-w22/STARTER-team01",
  team: [
    "Andrew L.",
    "Bryan T.",
    "Bryan Z.",
    "Kevin H.",
    "Phill C.",
    "Pranav M.",
    "Seth V."
  ]
}
```

At a later step (Step 3.2) you'll customize this with links for your team and with the names of your team members.  But we're getting ahead of ourselves.

# Step 1.3: Give team and staff access to your Heroku Deployment

Please visit the `Access` tab of the Heroku Dashboard for your deployed app.

Add each of the members of your team.

Then also add the assigned LA and TA for your team.   
* You can find their names here: <tt>https://ucsb-cs156.github.io/{{page.qxx}}/info/teams/</tt>
* To get the email that you should use for Heroku, dm them on the slack.
* Then add `phtcon@ucsb.edu`, the instructor for the course.


# Step 1.4: Divide up the six controllers among your team

This step is a part of participation assignment ({{page.participation_activity_num}}), in class on {{page.particpation_activity_date}}}. 

Now in the README.md, towards the top, there is a place where you need to divide up the work among the team 
members.  There are six services, and six matching controllers that you need to implement and write tests
for; divide these up so that each team member is assigned to at least one of these.
   
Find the table that looks like this, and fill it in, dividing the work among the team members.
   
There are six service/controller pairs: you need to go into your team's slack channel and claim one:
   
* Location look up (enter a string, get back locations in the world along with their latitude/longitude)
* Look up public holidays (enter a year and a country code), get back public holidays
* Reddit query (enter a subreddit name, get back recent reddit posts; whomever does this one needs to have 
     a reddit account.)
* Tides query (enter a start and end date, and a station id, get back high and low tides during that period)
* University query (enter part of a university name, get back all matching universities)
* Zip Code query (enter a zip code, get back information about that zip code).

Each member of the team is responsible for implementing one of these services, the matching controller, and
the tests that go along with them.

**NOTE: to get the participation grade for today's discussion seciton, you MUST actually post in the team slack channel
which of the six you are claiming.  If you are not present in discussion, you might get assigned one of these by your team.
But you only get the particpation grade if you were actually in discussion as evidenced by your post to the Slack.**

# Step 1.5: Document the division in your README.md file

This step is also part of participation assignment ({{page.participation_activity_num}}), in class on {{page.participation_activity_date}}. 

In the README, there is a table that looks like this.  Someone on the team should fill in the first two columns 
of the table with the name of the team members that will implement each of the services.  

On teams with fewer than six members, after each person has done one, whoever finishes first can help the
team by completing the unfinished one.  *However, each team member must contribute at least one of the services*
*and controllers, with commits and pull requests in their name.*


```
|   Name    | GitHub Id |  Service                    | Controller                |
|-----------|-----------|-----------------------------|---------------------------| 
|           |           | `LocationQueryService`      | `LocationController`      |   
|           |           | `PublicHolidayQueryService` | `PublicHolidayController` |   
|           |           | `RedditQueryService`        | `RedditController`        |   
|           |           | `TidesQueryService`         | `TidesController`         |   
|           |           | `UniversityQueryService`    | `UniversityController`    |
|           |           | `ZipCodeQueryService`       | `ZipCodeController`       |
```
   
Note that after you add the names, the lines might not line up in the source code.  Don't worry; the table will still look fine as a formatted table.  

Example: notice the wavy lines...

```
|   Name    | GitHub Id |  Service                    | Controller                |
|-----------|-----------|-----------------------------|---------------------------| 
|           |           | `LocationQueryService`      | `LocationController`      |   
| Bryan T.  | btk5h     | `PublicHolidayQueryService` | `PublicHolidayController` |   
| Wade V.   | WadeVaresio | `RedditQueryService`        | `RedditController`        |   
| Jacqui M. | JacquelineMai | `TidesQueryService`         | `TidesController`         |   
|           |           | `UniversityQueryService`    | `UniversityController`    |
| Mara D.   | mara-downing | `ZipCodeQueryService`       | `ZipCodeController`       |
```
   
Then notice the rendered table looks fine:


|   Name    | GitHub Id |  Service                    | Controller                |
|-----------|-----------|-----------------------------|---------------------------| 
|           |           | `LocationQueryService`      | `LocationController`      |   
| Bryan T.  | btk5h     | `PublicHolidayQueryService` | `PublicHolidayController` |   
| Wade V.   | WadeVaresio | `RedditQueryService`        | `RedditController`        |   
| Jacqui M. | JacquelineMai | `TidesQueryService`         | `TidesController`         |   
|           |           | `UniversityQueryService`    | `UniversityController`    |
| Mara D.   | mara-downing | `ZipCodeQueryService`       | `ZipCodeController`       |
{:.table .table-sm .table-striped .table-bordered}

   
# Part 2: Work as an individual on your service

In this part of the lab, you work as an individual, on your part.  You may get help from other team members&mdash;in fact you are strongly encouraged to do so!  Pairing on this is a great idea!  But, you should be doing the commits and pull requests from your github account so that you and your team gets credit.

Videos:
* [This video (20:30)](https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=15d5a190-f7b2-4bbd-92e2-ae2101874844) walks you through steps 2.1 through 2.4 (note that step 2.2 is done out of order with the other two, but it's still there in the video.)
* There isn't a video for steps 2.5 and 2.6 yet, but there will be soon.

## Step 2.0: Optional, but recommended: install VSCode extension for Lombok

This step is optional, but highly recommended.  If you like, you may come back and do this later
as the need arises.

In this lab, we'll be using a package called Lombok. Lombok makes many things easier, 
by writing boring "cookie-cutter" (also known as "boilerplate") code for you!   However this can cause VSCode to
get confused; VSCode says: "dude, you don't have getters and setters!" or "your variable `log` is undefined!"

To help VSCode not be confused, look under VSCode Extensions, and install this one:

* <https://marketplace.visualstudio.com/items?itemName=GabrielBB.vscode-lombok>


## Step 2.1: Clone the repo to your own machine (or CSIL account)

Clone the team's repo to your own machine or CSIL account, with `git clone repo-url`, then cd into the repo and open it up in your editor (we suggest VSCode).

Then try running `mvn spring-boot:run` and opening up the server on <http://localhost:8080>.

Try navigating to <http://localhost:8080/swagger-ui/> and trying out the various APIs.

Then when you are ready to start coding, we'll move on to Step 2.2.

## Step 2.2: Create a new branch

First come up with a branch name, using this convention: `Firstname-Servicename`, for example:
* If your name is Chris, and you are working on the `PublicHolidayService`, call your branch `Chris-PublicHoliday`
* If your name is Taylor, and you are working on the `ZipCodeService`, call your branch `Taylor-ZipCode`

To create your branch, cd into your cloned repo, and use this command:

```
git checkout main
git pull origin main
git checkout -b Chris-PublicHoliday`
```

This creates a new branch `Chris-PublicHoliday` that is branched off a fresh copy of the main branch.

You'll do all of your work in this branch, and when you are done, you'll do a *Pull Request* to get your code into the `main` branch.  

* *Note that using this workflow is a required part of the assignment*.   
* We are practicing a workflow (the GitHub feature-branch/pull-request workflow) that will become super important later in the course, and even more important when you work on real world projects.

## Step 2.3: Implement the Service you were assigned

Now, in the directory `src/main/java/edu/ucsb/cs156/spring/backenddemo/services`, you should find the "stub" for the service that you are asked to create.  

Each of these services provides a method `getJSON` (which may or may not have parameters, depending on the specifics of the service.)  This `getJSON` method encapsulates a web request to another web application that is our source of information.
Our backend is going to aggregate information from many sources and then, eventually, make it all available to a front-end user interface.

Each of these service works roughly the same as the example `EarthquakeQueryService` or the `CountryCodeQueryService`, so use those services as templates for how to write yours.   
* The `EarthquakeQueryService` and `CountryCodeQueryService` are both provided for you as examples.  Please read over them; we'll also go over them in lecture.  
* The `CollegeSubredditQueryService` is also provided for you, but it works a bit differently; it uses a CSV file as it's data source rather than a JSON web service.  So don't use that as a model for your services. We'll discuss that one in lecture and how it differs from the others.

Now, open up the stub file for your service, and start adding code based on what you see in the two example services.

The first piece of information you need is a value for the endpoint, which is in the table below.

| Service                     | Endpoint | 
|-----------------------------|----------|
| `LocationController`       | `https://nominatim.openstreetmap.org/search/{location}?format=json` |
| `PublicHolidayQueryService` | `https://date.nager.at/api/v2/publicholidays/{year}/{countryCode}` |
| `RedditQueryService`        | `https://www.reddit.com/r/{subreddit}.json` |
| `TidesQueryService`         | `https://api.tidesandcurrents.noaa.gov/api/prod/datagetter?application=ucsb-cs156&begin_date={beginDate}&end_date={endDate}&station={station}&product=predictions&datum=mllw&units=english&time_zone=lst_ldt&interval=hilo&format=json` |
| `UniversityQueryService`    | `http://universities.hipolabs.com/search?name={name}` |
| `ZipCodeQueryService`       | `http://api.zippopotam.us/us/{zipcode}` |
{:.table .table-sm .table-striped .table-bordered}

You will also need some additional documentation about the parameters.  You can find this on the swagger-ui
pages of staff solution, here:
* <https://staff-team01-solution.herokuapp.com/swagger-ui/>

NOTE: The `EarthquakeQueryService` (along with the test for it) has two hard coded parameters in addition to the ones that 
are exposed through the api (i.e. `minMag` for minimum magnitude, and `distance` (for distance in km from Storke Tower).   We 
could have chosen to make those parameters that the user of the API could supply.  And indeed, it would feasible (though 
it isn't part of this assignment) to implement a separate service that allows the user to supply those, or to make 
the lat/long of Storke Tower the default if and only if the user doesn't supply values for those.

But, the bottom line is that *none of the other services you are implementing needs latitude and longitude, especially not that of Storke Tower,
in the implementation.*   So those should not appear in your code for anything other than the `EarthquakeQueryService` and the 
`EarthquakeQueryServiceTests`.   Some might say that the `EarthquakeQueryService` is therefore a bad example for you to work from&mdash;I choose to
think of it differently; it's an example that forces you to really think about what's going on, and what parameters you should retain, vs. which ones
you should not retain.

Additionally, there are some special instructions for the `RedditQueryService` near the bottom of this web page.

As you work on your service, make commits frequently, with meaningful commit messages. 
* Use your initials at the start of your commit message (e.g. `cg` for "Chris Gaucho")
* Separate your initials from your message with a hyphen
* Your message should describe what you did

Examples:

* `git commit -m "cg - added service to get information on zip codes"`
* `git commit -m "cg - correct typo in endpoint url for zip code service"`

Having meaningful commit messages is a component of your grade for this assignment, so please do put some thought into what you write.

As you make commits, push them to your branch, for example:

```
git push origin Chris-Zipcode
```

A few handy commands:
* `git status` shows what branch you are on, among other things
* `git branch -a` shows all current branches
* `git fetch` updates information about branches by pulling new branch names from GitHub

When you're done implementing the first draft, the next step is to write the test for your service

## Step 2.4: Implement the test for the service you were assigned

In the directory `src/test/java/edu/ucsb/cs156/spring/backenddemo/controllers` you will find tests for the three sample services.  Use these as a model to write a test for your service.

We'll go over the code for these tests in lecture.

Run the tests by running `mvn test` and then check the test coverage with `mvn test jacoco:report`

When that test passes, we'll build the controller and the controller test so that you can try out your service.

## Step 2.5: Implement the controller for the service

In a Spring Boot application, a controller class is one that implements backend endpoints (i.e. provides a web service
on a URL).   You will now implement a controller so that users of your app (in practice, typically, the front end code)
can access the information provided by your service. 

The documentation at the staff solution to the lab <https://staff-team01-solution.herokuapp.com/swagger-ui/> shows the urls of the endpoints you'll be implementing; they 
are also shown in this table:


|  Controller                | Endpoint     |
|----------------------------|--------------|
|  `LocationController`      | `/api/locations/get` |  
|  `PublicHolidayController` | `/api/publicholidays/get` |  
|  `RedditController`        | `/api/reddit/get` |  
|  `TidesController`         | `/api/tides/get` |  
|  `UniversityController`    | `/api/university/get` |
|  `ZipCodeController`       | `/api/zipcode/get` |
{:.table .table-sm .table-striped .table-bordered}


You'll see additional information in the Swagger-ui that is provided by annotations such as these found in the `EarthquakesController`

* `@Api(description="Earthquake info from USGS")`
* `@ApiOperation(value = "Get earthquakes a certain distance from UCSB's Storke Tower", notes = "JSON return format documented here: https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php")`
* `@ApiParam("distance in km, e.g. 100")`

Please:
* Take note of how those are used in the `EarthquakesController`
* Note the similar information that appears in the Swagger-ui interface of the staff solution here: <https://staff-team01-solution.herokuapp.com/swagger-ui/> 
* Add these annotations in the appropriate places in your own Controller so that the documentation matches that of the staff solution.  This is another component of your grade for this assignment.

To check if your controller endpoint is operational, you can run:

```
mvn spring-boot:run
```

And then visit the `/swagger-ui/` endpoint.  You should then be able to test your service interactively.

When it appears to be working, make a commit, and then we'll move on to the coding part for the individual phase: writing a test for your controller.

## Step 2.6: Write the controller test

In the directory: `src/test/java/edu/ucsb/cs156/spring/backenddemo/controllers` you'll find example controller tests.

Using those as a model, implement a controller test for your controller.

Run the tests by running `mvn test` and then check the test coverage with `mvn test jacoco:report`

## Step 2.7: Write the service test

In the directory: `src/test/java/edu/ucsb/cs156/spring/backenddemo/services` you'll find example  tests for the services

Using those as a model, implement a test for your new service.

Run the tests by running `mvn test` and then check the test coverage with `mvn test jacoco:report`

When you have good coverage for both your service and your controller, you are ready for the final stage of part 2.


## Step 2.8: Make a Pull Request

* Navigate to your repo on the GitHub website
* Go to the Pull Requests tab
* Click to create a new pull request
  - the `base` branch should be `main` (this is where your code will be "pulled into")
  - the `compare` branch should be your feature branch, e.g. `Chris-Zipcode`
  - for the title, put in something like "Add ZipCode Service and Controller"
* For the PR description, enter something like this 

  ```
  In this PR, we add an endpoint `/api/zipcode/get` that can be used to get information
  about the location of a particular zipcode.  
  ```
* Then, once the PR is created, add your team members as code reviewers
* Do not merge your own PR.  You should wait until another member of your team has code reviewed it, 
  and then they can do the merge.
  

## Step 2.9: Try submitting your branch on Gradescope

Now, go to the [team01 assignment on Gradescope]({{page.gradescope}}) and submit from the team's repo, and from your branch (`Name-Topic`) rather than the `main` branch (there's a drop down where you can select the branch) to see
if the tests pertaining to your service/controller are passing.  Don't worry (for now) about the other tests for the moment; just try to get the tests for your own service/controller to pass.

# Part 3: Back to the team 

## Step 3.1: Review and merge the PRs

Now, as a team, look at one another's PRs.  You should be able to do a code review (we'll demonstrate how that works in lecture), and approve the PR with the comment `LGTM` (`Looks Good To Me`, or `Let's Get This Merged`).
* Note that "commenting LGTM" is not the same as doing an "Approving Code Review" with the comment `LGTM`.  You need the latter.
* It's also a good idea to try it out. Here are three ways:
  - You can check out the branch, then run `mvn spring-boot:run` to test the code.
  - You can also deploy the branch in the PR to Heroku and try it there.
  - Finally, you can try submitting that branch to Gradescope and see if it passes it's tests
* When the *team* is satisfied with the code for one of the branches, you can merge that branch into main by clicking the "Merge" button on the PR.



## Step 3.2: Customize the `HomeController`

Now, someone on the team should make a branch, `YourName-HomeController` (e.g. `Alex-HomeController`), and
update the code in `HomeController` so that:

* instead of a list of the staff names, there is a list of the names of the people on your team that contributed to this repo
* instead of a link to <tt>https://github.com/ucsb-cs156-{{page.qxx}}/STARTER-team01</tt>, there is a link to your team's private repo (e.g. <tt>https://github.com/ucsb-cs156-{{page.qxx}}/team01-{{page.qxx}}-5pm-1</tt>

Make these changes, test them, and then make a PR for this, and merge it.

## Step 3.3: Finish the changes to the README.md

Now, someone else on the team should make a  branch, `YourName-READMEFixes` (e.g. `Alex-READMEFixes`), and
update README.md, so that all of the places that say "TODO" are replaced with the appropriate content.

When items 3.1, 3.2, and 3.3 are done, and all of the PRs are merged, you are ready to submit for your team on Gauchospace.


# Part 4: Submission

## Step 4.1  Each team member must submit individually from the main branch on Gradescope

Deploy your repos main branch on your team's shared Heroku deployment.  Here's the dashboard link:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-{{page.qxx}}-5pm-1-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-1-team01)|[cs156-{{page.qxx}}-6pm-1-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-1-team01)|[cs156-{{page.qxx}}-7pm-1-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-1-team01)|
|[cs156-{{page.qxx}}-5pm-2-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-2-team01)|[cs156-{{page.qxx}}-6pm-2-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-2-team01)|[cs156-{{page.qxx}}-7pm-2-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-2-team01)|
|[cs156-{{page.qxx}}-5pm-3-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-3-team01)|[cs156-{{page.qxx}}-6pm-3-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-3-team01)|[cs156-{{page.qxx}}-7pm-3-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-3-team01)|
|[cs156-{{page.qxx}}-5pm-4-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-5pm-4-team01)|[cs156-{{page.qxx}}-6pm-4-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-6pm-4-team01)|[cs156-{{page.qxx}}-7pm-4-team01](https://dashboard.heroku.com/apps/cs156-{{page.qxx}}-7pm-4-team01)|
{:.table .table-sm .table-striped .table-bordered}

Double check that:
* the running app shows your team members names (i.e. that Step 3.2 above was done correctly)
* that each of the other controllers works properly and returns good results (check this by interactively testing through the swagger-ui interface)

## Step 4.2  Each team member must submit individually from the main branch on Gradescope

Once all of the PRs for the team are merged, *each* team member should find [assignment team01 on Gradscope]({{page.gradescope}}), submit from the team's repo, and the `main` branch on Gradescope.  The main branch should now contain all team member's work.

*Do not simply assume that your team will submit on your behalf*.

To help promote both team and individual accountability, I am asking each team member to submit the team's work to Gradescope separately, after all of the PR's are merged.

I would like to see which team members are actually in touch with their teams and engaged with the process&mdash;hopefully that's everyone.   This mutual team accountability will be an important skill during the project phase of the course, which is worth 40% of your course grade, so we are practicing it with a programming assignment now (which is a "lower stakes" part of your course grade.)

## Step 4.3  One team member can submit on Gauchospace on behalf of the team

You will get one grade for this assignment out of 100 points based on the Gradescope autograder.

In addition, you'll get a separate grade after a staff member does a manual inspection of your running app.
To signal that you are ready for that, please submit a link to your team's repo Gauchospace in the place marked team01-links:

* [team01-links]({{page.gauchospace}})

For this grade item (`team01-links`), you will get a separate manually assigned grade (on Gauchospace) based on these items:
* Is your app deployed on Heroku?
* Is the swagger-ui documented using all of the appropriate annotations (e.g. `@Api`, `@ApiOperation` and `@ApiParam`)
* Do the endpoints actually work?
* Is the `HomeController` updated with the repo name and members of the team?
* Did the team use the Pull Request process, with code reviews to get all code merged?
* Are commit messages meaningful?
* Did each team member contribute at least one PR (i.e. the commits and PR are done under their github id?)

You may want to go over this list as a team before submitting on Gauchospace.

   
 # Special Instructions for the RedditQueryService
 
The Reddit Query service will work just like the other services, except that you may get frequent errors 
of the form `429 Too Many Requests` as described in [this Stack Overflow post](https://stackoverflow.com/questions/30992791/http-429-too-many-requests-when-accessing-a-reddit-json-page-only-once-using-ja).   The fix is to add this line of code,
which you should customize with your reddit id (put it in place of `cgaucho`).

```java
   headers.set("User-Agent","spring-boot:cs156-team01:s22 (by /u/cgaucho)")
```

This goes immediately after these lines of code, which you'll find in the example services:

```java
   HttpHeaders headers = new HttpHeaders();
   headers.setAccept(List.of(MediaType.APPLICATION_JSON));
   headers.setContentType(MediaType.APPLICATION_JSON);
```



