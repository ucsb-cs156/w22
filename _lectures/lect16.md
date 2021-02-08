---
num: "Lecture 16"
lecture_date: 2021-02-10
desc: "Wed Lecture: Continuation of Mon lect, with focus today on React"
ready: true
---

# A few things from last time

I was mistaken about Google restricting us to only UCSB users in our OAuth apps.

If you would like to try testing with non-ucsb gmails, to check whether the 'guest' role works properly, you can do so by:

* Navigate to <https://console.developers.google.com/apis/credentials/consent> and select the appropriate project.
* Click where it says "User Type", and you can select either Internal or External.  

  If you select External, and "in production", then you'll be able to login with non-UCSB Google Addresses.
  
  Previously I thought doing that triggered a need for review from Google.  But apparently, you don't have to 
  get your app approved by Google as long as you don't:
  - add more than 10 domains
  - upload a logo
  - ask for sensitive scopes

Then, you can log into your app with non-UCSB Google email addresses.  Sometimes this is useful for testing, since you can make those
accounts have differnet privileges from your UCSB email address.

Please note that you are not *required* to do this.  It's just an option you have if you find it useful.

# A question/comment from a student:

Last time, after class, a student asked this in chat:

> These projects just seem crazy for me.  How did the instructor team manage to create those full-stack projects? The idea of being familiar with multiple languages, databases, and linking them together sounds overwhelming.

Let's discuss that a bit!

# May I delete my jpa02 from Heroku to make space?

Yes!  And we'll let you know when you may delete jpa03 as well

