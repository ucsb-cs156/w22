---
desc: "Team Project: React Frontend for CRUD, MongoDB Backend"
assigned: 2022-02-15 12:30
due: 2022-02-22 23:59
github_org: ucsb-cs156-w22
layout: lab
num: team03
ready: false
---

# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET
# NOT READY YET

In this team project, our starter code has a full frontend and backend.  Our main focus is the frontend, but we also introduce one new backend element: working with MongoDB
databases.

* Creating support for a MongoDB collection with `@Document` and `@Repository` with `MongoRepository`
* Creating React components and pages in a site that was piloted with the [Create React App](https://create-react-app.dev/) script
* Using [Storybook.js](https://storybook.js.org/) to visualize, catalog, document, and interactively test React components
* Implementing React components for tables using [React Table](https://react-table.tanstack.com/)
* Implementing React components for forms using [React Hook Form](https://react-hook-form.com/)
* Interacting with the backend using the custom hooks `useBackend` and `useBackendMutation`, each of which is wrapped around
  methods from [Axios](https://axios-http.com/) and [React Query](https://react-query.tanstack.com/)
* Using Toast notifications from [React Toastify](https://fkhadra.github.io/react-toastify/introduction/)
* Writing units tests for React components using [Jest](https://jestjs.io/), [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/), [Axios Mock Adapter](https://www.npmjs.com/package/axios-mock-adapter)
* Using `npm run coverage` to use the coverage features of [Jest](https://jestjs.io/) to check Javascript test coverage
* Using `npx stryker run` to use [Stryker Mutator](https://stryker-mutator.io/docs/stryker-js/introduction)  to do mutation testing of a JavaScript test suite

That's a lot!  The thing is, this is typical of professional level full-stack web projects:
* There are so many moving parts, each with its own complex documentation.
* It is typically not feasible (given time constraints) to do a complete deep dive into each of them.
* It is an important skill to be able to discern when "copy/paste/adapt" is the right strategy, and when to do a deeper dive to try to understand what is going on.
* It is also an important skill to know *when* to ask for help, and *how* to ask for help.  That may be one of the most important skills you learn in this course.


In addition, we'll practice further with a few concepts we've seen before:
- Set up of the documentation repos, the `-docs` and `-docs-qa` repos
  - This will be more meaningful now because the Storybook pages published in these repos will become part of our workflow.
  - The scripts to set these up have also be greatly improved over the ones from jpa03 and team02.
- Working with pull requests, and GitHub actions scripts (aka CI/CD).
- Working with a Kanban board and GitHub issues.

# Getting Started

Here's how that will play out in detail:
1. Someone on your team will navigate to the team's `team03-teamname` repo.
2. Under "Projects" create a legacy project (Kanban board, not the Beta Project), with columns: `Todo`, `In Progress`, `In Review`, `Done`
3. Then, you'll pull in the starter code from STARTER-team03 in the usual way:
   ```
   git remote add starter url-of-STARTER-repo-goes-here
   git checkout -b main
   git pull starter main
   git push origin main
   ```
4. Then, as in team02, there is a GitHub actions script which you can manually trigger that should populate your Kanban board with the issues under the `/issues` subdirectory.
   - You may need to first enable GitHub Actions, and you may also need to enable issue if they are not enabled on the Repo.
   - To enable Issue, go under Settings, then the General Tab, the scroll down to Features:
     <img width="747" alt="image" src="https://user-images.githubusercontent.com/1119017/154173897-16539bd5-c07a-4ae8-9911-a401fe51ed59.png">

6. Then, as in team02, you'll assign those tasks to members of the team, moving them into the "In Progress" as each task is assigned.  
   - You may assign tasks either to individuals, pairs, or even larger groups (so-called "mobs", as in [*Mob Programming*](https://en.wikipedia.org/wiki/Mob_programming))
   - But be sure that if you assign a task to more than one person, that each member of the pair or mob is legitimately committed to contributing to working on the task, and committed to getting it finished.
7. Once a pull request is complete for a given task, you move it into the `In Review` column
   - At this stage, you seek a code review from a member of the team that was not involved in the coding.
   - If it was a true "all-team mob", than it's fine to get a code review from someone that participated, but this is rare.
   - Also, at this stage, if the PR is not "green on CI", meaning that all of the GitHub actions scripts show green checks, this is when you 
     should address that, before merging the pull request.
7. Only when the PR is merged does the issue get moved into the done column.

## What you'll do: Content/Product

From a high-level standpoint, you'll be doing these things:

Set up Tasks:

* Setting up Google OAuth for your project
* Setting up a MongoDB instance for your project
* Setting up a Repo with qa and prod deployments on Heroku
* Configuring the documentation repos
* Configuring Codecov

Coding Tasks:
* Adding CRUD operations for University Subreddits, and UCSB Subjects (we'll leave off UCSB Requirements)
* Copying your the [EarthquakeQueryService](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/main/java/edu/ucsb/cs156/spring/backenddemo/services/EarthquakeQueryService.java) and [EarthquakeQueryServiceTests](https://github.com/ucsb-cs156-w22/STARTER-TEAM01/blob/main/src/test/java/edu/ucsb/cs156/spring/backenddemo/services/EarthquakeQueryServiceTests.java) from the [team01](https://ucsb-cs156.github.io/w22/lab/team01/) project into your team03 repo.
* Adding classes that model the JSON retrieved by the EarthquakeQueryService, with a Document class representing the `Feature` level in this JSON.
* Setting up a MongoDB collection for Features documents that represent individual earthquakes.
* Setting up an Earthquakes menu with three options: 
  - Retrieve Earthquakes (Admin only: this will use the EarthquakeQueryService to get all earthquakes that are within a specified distance from Storke Tower, and that are at least a specified magnitude, and store them in the MongoDB collection)
  - Purge Earthquakes (Admin only: this will delete all Earthquakes in the collection)
  - List Earthquakes (All Users: this will list all Earthquakes in the collection) 
* Full test coverage for all of that

# More about MongoDB

To learn more about MongoDB, you can read these three articles, which also reference code that is part of the starter repo
for this project.   They should be read in this order, but the third article is the one that is most relevant to this project.

* [MongoDB: New Database](https://ucsb-cs156.github.io/topics/mongodb_new_database/)—Setting up a new database on cloud.mongodb.com
* [MongoDB: Spring Boot - Basic Collection](https://ucsb-cs156.github.io/topics/mongodb_spring_boot_basic_collection/)—Accessing a MongoDB collection from Spring Boot
* [MongoDB: Spring Boot - Nested Document](https://ucsb-cs156.github.io/topics/mongodb_spring_boot_nested_collection/)—Creating a document class for nested JSON

The third article describes how to set up Java classes for a nested collection, which is precisely the problem that is being posed here.  
The [US Geological Survey API for Earthquakes](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) that we used in [team01](https://ucsb-cs156.github.io/w22/lab/team01/), has this structure (I've edited this to show only two earthquakes instead of the 18 that 
were returned by this query, in order to keep this shorter; sorry, it's still quite long.)

```json
{
    "type": "FeatureCollection",
    "metadata": {
        "generated": 1644953348000,
        "url": "https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&minmagnitude=2.0&maxradiuskm=100&latitude=34.4140&longitude=-119.8489",
        "title": "USGS Earthquakes",
        "status": 200,
        "api": "1.13.2",
        "count": 2
    },
    "features": [
        {
            "type": "Feature",
            "properties": {
                "mag": 2.16,
                "place": "10km ESE of Ojai, CA",
                "time": 1644571919000,
                "updated": 1644648614363,
                "tz": null,
                "url": "https://earthquake.usgs.gov/earthquakes/eventpage/ci40182864",
                "detail": "https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=ci40182864&format=geojson",
                "felt": 1,
                "cdi": 2,
                "mmi": null,
                "alert": null,
                "status": "reviewed",
                "tsunami": 0,
                "sig": 72,
                "net": "ci",
                "code": "40182864",
                "ids": ",ci40182864,",
                "sources": ",ci,",
                "types": ",dyfi,focal-mechanism,nearby-cities,origin,phase-data,scitech-link,",
                "nst": 72,
                "dmin": 0.01068,
                "rms": 0.3,
                "gap": 40,
                "magType": "ml",
                "type": "earthquake",
                "title": "M 2.2 - 10km ESE of Ojai, CA"
            },
            "geometry": {
                "type": "Point",
                "coordinates": [
                    -119.1321667,
                    34.4271667,
                    16.08
                ]
            },
            "id": "ci40182864"
        },
        {
            "type": "Feature",
            "properties": {
                "mag": 2.64,
                "place": "10km NW of Santa Paula, CA",
                "time": 1644539746380,
                "updated": 1644905608040,
                "tz": null,
                "url": "https://earthquake.usgs.gov/earthquakes/eventpage/ci40182600",
                "detail": "https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=ci40182600&format=geojson",
                "felt": 41,
                "cdi": 4.5,
                "mmi": null,
                "alert": null,
                "status": "reviewed",
                "tsunami": 0,
                "sig": 126,
                "net": "ci",
                "code": "40182600",
                "ids": ",ci40182600,us7000gjva,",
                "sources": ",ci,us,",
                "types": ",dyfi,focal-mechanism,nearby-cities,origin,phase-data,scitech-link,",
                "nst": 86,
                "dmin": 0.01655,
                "rms": 0.32,
                "gap": 27,
                "magType": "ml",
                "type": "earthquake",
                "title": "M 2.6 - 10km NW of Santa Paula, CA"
            },
            "geometry": {
                "type": "Point",
                "coordinates": [
                    -119.1346667,
                    34.4205,
                    16.29
                ]
            },
            "id": "ci40182600"
        }
    ],
    "bbox": [
        -120.6706667,
        33.9791667,
        -0.05,
        -118.9346667,
        35.0601667,
        18.74
    ]
}
```

To summarize the "shape" of this JSON, we have essentially four objects:

* `FeatureCollection`
* `Metadata`
* `Feature`
* `FeatureProperties`

We could also optionally set up classes for 

Each of these will be set up as a Java class using the [Lombok](https://ucsb-cs156.github.io/topics/lombok/) `@Data` annotation which automatically sets up setters and getters for each of the private fields.   The `@NoArgConstructor` and `@Builder` annotationsa are also useful (as explained in the documentation above.)  

A `FeatureCollection`, which is the top level object, has these fields.  
 
```java
    private String type;
    private Metadata metadata;
    private List<Feature> features;
```

It could also have a `bbox` field of type `List<Double>`, but we can leave that out. (If you've read the three tutorials above, you may recall that we do not have to represent every field in the JSON in our Java objects; we only need to represent the parts of the JSON that we are interested in retrieving, storing, and displaying&mdash;though, this requires us to configure the `ObjectMapper` object (typically the variable is `mapper` to set  `DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES` to `false`:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
```

A `Metadata` object looks like this in JSON.  This time, I won't give you the Java code, but you can see that it would simply be `private String` fields for everything here except for the `count`, which would be a `private int`.   

```json
 "metadata": {
        "generated": 1644953348000,
        "url": "https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&minmagnitude=2.0&maxradiuskm=100&latitude=34.4140&longitude=-119.8489",
        "title": "USGS Earthquakes",
        "status": 200,
        "api": "1.13.2",
        "count": 2
    },
```

A `Feature` object would look like this:

```java
   private String type;
   private FeatureProperties properties;
   private String id;
```

It could also contain a `private Geometry geometry` object, which might look like this, but I think we can leave that out.

```java
  private String type
  private List<Double> coordinates; 
```

With that, and the example of the `RedditPosts` in the sample code, my hope is that you can figure out how to set up appropriate classes under the `documents` package to represent the JSON objects returned by the USGS (which are a special case of a format called [GeoJSON](https://geojson.org/), along with a class under `collections` to represent the MongoDB collection. 

# A reminder about open source

Note that this assignment is open source.

The repos are public *on purpose*.
* You are encouraged to consult with one another within and across teams where it helps
  your learning.
* That does not mean that you can cheat by just copying code from another team.
* You are *not* permitted to just look at another team's code, even though you "can".
* It does mean that you should try to solve the problems as best you can, but you may 
  consult with members of other teams as you work.  In that context, you may look at 
  other team's code.

This isn't hard.   You all *know* when you are are looking at other team's work to
try to learn, versus when you are just looking at it as a shortcut to learning.

I'm trusting you to do the right thing.   This is practice for when, later on, you are
all working on different assignments.

