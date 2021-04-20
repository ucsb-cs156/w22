---
num: "Lecture 10"
lecture_date: 2021-04-20
desc: "Tue Discussion: Team Standup for team01, work on team01"
ready: true
---

# Short Version

* Do your team standup (each member of team puts update on Slack channel, then discuss)
* Update PRs so that red X's become green checks (you can do this with instructions below)
* Code Review your PRs (and get code reviews from staff)
* **Important** Test your code through the swagger-ui also!
  * It is NOT ENOUGH to just test with the automated tests
  * You should ALSO test with the swagger-ui endpoint to make sure that you see real results coming back 
  * The staff will be testing each team's implementation that way ALSO, and you will lose points if your implementation doesn't *actually* work.
  * If you don't understand what this means, ask for help from staff.
* Merge your PRs
* When all PRs merged:
  1. Deploy your main branch on your team's Heroku app for team01 (see table of links below)
  2. Make sure that it actually works, using the `swagger-ui` endpoint.
  3. Then **each team member** should submit from main branch on Gradescope separately.  You should at that point get 100% on Gradescope.
  4. Then, **one team member** should submit on behalf of whole team on Gauchospace.

Then, and only then, you are all done with [team01](https://ucsb-cs156.github.io/s21/lab/team01/).

# See the announcement on `#annoucements` about GitHub Actions

> We have a solution for the CI/CD runs that were failing.  We have deployed a few "self-hosted" CI/CD servers.     You have two options.   We encourage you to use option 2.
> * Option 1: Just go ahead as if nothing has happened, but your jobs will sometimes work and sometimes you'll get the "billing error".   When you get the biling error, just click "Rerun All Jobs".   Repeat every 2-3 minutes you get a passing test, or a "real" error.
> * Option 2: Edit the file .github/workflows/maven.yml and make these changes:
>   1. Change the line 8 from `runs-on: ubuntu-latest` to `runs-on: self-hosted`
>   2. Delete lines 21-27; that is, remove these lines:
>      ```yml
>            - name: Pitest
>              run: mvn test org.pitest:pitest-maven:mutationCoverage
>            - name: Upload Pitest to Artifacts
>              uses: actions/upload-artifact@v2
>              with:
>                name: pitest-mutation-testing
>                path: target/pit-reports/**/*     
>  
>      ```
>   With those two changes, you should not experience the billing problem anymore, and your runs will complete much faster.

There is a video on Gauchocast (~12 minutes) about how to deal with the red X's and get them 
to turn into green checks:

<iframe src="https://gauchocast.hosted.panopto.com/Panopto/Pages/Embed.aspx?id=609d5ff5-46b7-47ad-96c0-ad1001067e49&autoplay=false&offerviewer=true&showtitle=true&showbrand=false&start=0&interactivity=all" height="405" width="720" style="border: 1px solid #464646;" allowfullscreen allow="autoplay">
</iframe>

* <https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=609d5ff5-46b7-47ad-96c0-ad1001067e49>

# Standup (P06)

We'll do a standup just like we did last Wednesday, and yesterday:

1. When you get to your breakout rooms, one person will share their screen, and point at the Slack channel for the team.
2. Start a two minute timer (if you type `two minute timer` into Google, it will bring up one on the search results directly, or  there are lots of fun countdown timers on YouTube as well.)
3. During the two minutes, each person types into the Slack channel their standup summary:
   - What stage of [team01](https://ucsb-cs156.github.io/s21/lab/team01/) are you on? Mention the number (2.0 through 2.9), but
     also describe it in words.
   - What are you planning to do next
   - What blockers (if any) do you have (answer could be "none")
4. After the two minutes, go through and have each person unmute themselves 
   and share their status update out loud.  **Make a note of any blockers in the team's slack channel**
5. Once everyone has shared, standup, per se, is over.  But now, *deal with the blockers* if any.  
   - This may be a longer discussion, and it might be one where the whole team doesn't need to particpate.
   - For example, it might be two team members going into a separate breakout room to discuss the solution to a problem.

A particular "blocker" is if the team members has made their pull request 
and is waiting for a code review, and for their PR to be merged.  

There is now a video on Gauchocast about how to do code reviews:

<iframe src="https://gauchocast.hosted.panopto.com/Panopto/Pages/Embed.aspx?id=30125bc2-25c7-48ee-9b3c-ad10010bdf47&autoplay=false&offerviewer=true&showtitle=true&showbrand=false&start=0&interactivity=all" height="405" width="720" style="border: 1px solid #464646;" allowfullscreen allow="autoplay">
</iframe>

* <https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=30125bc2-25c7-48ee-9b3c-ad10010bdf47>
 
