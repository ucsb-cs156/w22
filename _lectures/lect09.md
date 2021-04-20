---
num: "Lecture 09"
lecture_date: 2021-04-19
desc: "Mon Lecture: Update on CI/CD pipeline for team01, plus intro to JS"
ready: true
---

<iframe src="https://gauchocast.hosted.panopto.com/Panopto/Pages/Embed.aspx?id=2e42c01a-2d3d-4f11-b29b-ad100112c1bc&autoplay=false&offerviewer=true&showtitle=true&showbrand=false&start=0&interactivity=all" height="405" width="720" style="border: 1px solid #464646;" allowfullscreen allow="autoplay">
</iframe>

* <https://gauchocast.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=2e42c01a-2d3d-4f11-b29b-ad100112c1bc>

# Problem with the CI/CD pipeline (GitHub Actions)

This lecture was supposed to start introducing React, and we did a little bit of that, but
only about 15-20 minutes rather than the planned 30-45 minutes.   That will get pushed off
to Wednesday, or possibly even later.  

Instead, we focused on a small unplanned crisis: the fact that all of the GitHub Actions runs
for team01 were failing due to us running out of "free minutes" for GitHub Actions runs
on private repos in our org.

This led to a discussion of how GitHub Actions works.    

(Though this wasn't covered in lecture, later in the day we announced the workaround on
the slack `#announcements` channel:

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

# Standup (P05)

Today's particpation activity (P05) involves the following (pretty much identical to P04
that we did last Monday):

1. When you get to your breakout rooms, one person will share their screen, and point at the Slack channel for the team.
2. Start a two minute timer (if you type `two minute timer` into Google, it will bring up one on the search results directly, or  there are lots of fun countdown timers on YouTube as well.)
3. During the two minutes, each person types into the Slack channel their standup summary:
   - What stage of [team01](https://ucsb-cs156.github.io/s21/lab/team01/) are you on? Mention the number (2.0 through 2.9), but
     also describe it in words.
   - What are you planning to do next
   - What blockers (if any) do you have (answer could be "none")
4. After the two minutes, go through and have each person unmute themselves and share their status update out loud.  This may
   seem redundant, but there's a purpose:
   - It's an opportunity for the team to focus on each person's sharing one at a time, and...
   - ... more importantly to respond to each person's sharing.
   - If there are blockers that can't be dealt with immmediately, make a note to deal with them after standup.
5. Once everyone has shared, standup, per se, is over.  But now, *deal with the blockers* if any.  
   - This may be a longer discussion, and it might be one where the whole team doesn't need to particpate.
   - For example, it might be two team members going into a separate breakout room to discuss the solution to a problem.

A particular "blocker" is if the team members has made their pull request and is waiting for a code review, and for their PR to be merged.  We'll discuss that one next if time permits; if not, we'll return to it on Monday.

 
