---
desc: "Team Project: Spring Boot Backend, part 1 (unauthenticated RESTFul APIs)"
assigned: 2021-04-13 17:00
due: 2021-04-21 23:59
github_org: ucsb-cs156-s21
layout: lab
num: team01
ready: false
starter: https://github.com/ucsb-cs156-s21/STARTER-team01
---


# NOTE: THIS IS STILL A WORK IN PROGRESS... COME BACK LATER (it isn't ready for you to start work yet.)

This is a team programming assignment.  Each team has it's own repo to complete this assignment, and
you will work as a team.

Here are the links to the repos:

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[team01-s21-5pm-1](https://github.com/ucsb-cs156-s21/team01-s21-5pm-1)|[team01-s21-6pm-1](https://github.com/ucsb-cs156-s21/team01-s21-6pm-1)|[team01-s21-7pm-1](https://github.com/ucsb-cs156-s21/team01-s21-7pm-1)|
|[team01-s21-5pm-2](https://github.com/ucsb-cs156-s21/team01-s21-5pm-2)|[team01-s21-6pm-2](https://github.com/ucsb-cs156-s21/team01-s21-6pm-2)|[team01-s21-7pm-2](https://github.com/ucsb-cs156-s21/team01-s21-7pm-2)|
|[team01-s21-5pm-3](https://github.com/ucsb-cs156-s21/team01-s21-5pm-3)|[team01-s21-6pm-3](https://github.com/ucsb-cs156-s21/team01-s21-6pm-3)|[team01-s21-7pm-3](https://github.com/ucsb-cs156-s21/team01-s21-7pm-3)|
|[team01-s21-5pm-4](https://github.com/ucsb-cs156-s21/team01-s21-5pm-4)|[team01-s21-6pm-4](https://github.com/ucsb-cs156-s21/team01-s21-6pm-4)|[team01-s21-7pm-4](https://github.com/ucsb-cs156-s21/team01-s21-7pm-4)|
{:.table .table-sm .table-striped .table-bordered}

# Step 1: Pull in Starter Code

One member of the team, it doesn't matter who, should pull in the starter code.

I suggest you do this in your breakout room, with the whole team watching, and the team member that is doing the work
sharing their screen.

That member should:
1. Clone the team's repo
2. Add a remote for the starter code, which is here: <{{page.starter}}>
3. Checkout the main branch (`git checkout -b main`)
4. Pull from the starter remote (`git pull starter main`)
5. Push to the origin repo (`git push origin main`)

# Step 2: Deploy the repo, as is, to Heroku

A member of your team should:

1. Visit the Heroku Dashboard, and create a Heroku app with the name `cs156-s21-5pm-1-team01`, substituting in your team number in place of `5pm-1`.
2. On the deploy screen, link your Heroku app to your team's repo, and deploy the main branch.
3. When the app is deployed, you should be able to navigate to the link below for your team, and launch the application.

| 5pm | 6pm | 7pm|
|-----|-----|----|
|[cs156-s21-5pm-1-team01](https://cs156-s21-5pm-1-team01.herokuapp.com)|[cs156-s21-6pm-1-team01](https://cs156-s21-6pm-1-team01.herokuapp.com)|[cs156-s21-7pm-1-team01](https://cs156-s21-7pm-1-team01.herokuapp.com)|
|[cs156-s21-5pm-2-team01](https://cs156-s21-5pm-2-team01.herokuapp.com)|[cs156-s21-6pm-2-team01](https://cs156-s21-6pm-2-team01.herokuapp.com)|[cs156-s21-7pm-2-team01](https://cs156-s21-7pm-2-team01.herokuapp.com)|
|[cs156-s21-5pm-3-team01](https://cs156-s21-5pm-3-team01.herokuapp.com)|[cs156-s21-6pm-3-team01](https://cs156-s21-6pm-3-team01.herokuapp.com)|[cs156-s21-7pm-3-team01](https://cs156-s21-7pm-3-team01.herokuapp.com)|
|[cs156-s21-5pm-4-team01](https://cs156-s21-5pm-4-team01.herokuapp.com)|[cs156-s21-6pm-4-team01](https://cs156-s21-6pm-4-team01.herokuapp.com)|[cs156-s21-7pm-4-team01](https://cs156-s21-7pm-4-team01.herokuapp.com)|
{:.table .table-sm .table-striped .table-bordered}

The result of visiting the home page of the app in the browser should be something like this:
   
```json
{"api-documentation":"http://localhost:8080/swagger-ui/","greeting":"Greetings from Spring Boot","repo":"https://github.com/ucsb-cs156-s21/STARTER-team01","team":["Andrew L.","Bryan T.","Calvin J.","Jacqui M.","Mara D.","Max L.","Phill C.","Wade V."]}
```
   
It might also be nicely formatted, depending on whether you have any browser extensions installed for processing JSON:
```json
{
  api-documentation: "https://starter-team01.herokuapp.com/swagger-ui/",
  greeting: "Greetings from Spring Boot",
  repo: "https://github.com/ucsb-cs156-s21/STARTER-team01",
  team: [
    "Andrew L.",
    "Bryan T.",
    "Calvin J.",
    "Jacqui M.",
    "Mara D.",
    "Max L.",
    "Phill C.",
    "Wade V."
  ]
}
```

3. This step is a part of participation assignment (P04), in class on Monday 04/11/2021. 

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
   
4. This step is also part of participation assignment (P04), in class on Monday 04/11/2021. 

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
   
   
   
 
 
 # Special Instructions for the RedditQueryService
 
The Reddit Query service will work just like the other services, except that you may get frequent errors 
of the form `429 Too Many Requests` as described in [this Stack Overflow post](https://stackoverflow.com/questions/30992791/http-429-too-many-requests-when-accessing-a-reddit-json-page-only-once-using-ja).   The fix is to add this line of code,
which you should customize with your reddit id (put it in place of `cgaucho`).

```java
   headers.set("User-Agent","spring-boot:cs156-team01:s21 (by /u/cgaucho)")
```

This goes immediately after these lines of code, which you'll find in the example services:

```java
   HttpHeaders headers = new HttpHeaders();
   headers.setAccept(List.of(MediaType.APPLICATION_JSON));
   headers.setContentType(MediaType.APPLICATION_JSON);
```



