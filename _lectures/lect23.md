---
num: "Lecture 23"
lecture_date: 2021-05-19
desc: "Wed Lecture: "
ready: false
---


# Tradoffs: Quick Win, vs Maintainability

A case study: https://github.com/ucsb-cs156-s21/proj-ucsb-courses-search/pull/292

Tradeoff:
* Can get the italics quickly by just modifying a few lines of code
  - Upside: quick, easy to understand
  - Downside: But the code might become hard to read, understand, maintain
* Alternative: put a css class on the elements that marks them as "sections"
  - Set the style for all sections in one place.
  - Downside: will take longer to do

Bottom line: for the short term
* Sometimes the quick win is the better way to go
  - Team morale
  - Getting something in front of the customers for feedback
  - Competiton (in a real world settting), and avoiding churn
* Sometime the more maintainable solution is the better way to go
  - If there isn't a pressing need
  

It's a good idea though, when you do the "quick win" to have a concrete plan for refacoring.
* Quick wins can accumulate into tech debt

As Bryan points out:

> I think something we might want to make more clear to the students is that they will be expected to refactor/rewrite existing code in some cases, and that the code already present in the codebase isn't necessarily the best example of good design


This is absolutely true, and it's also going to be true of real world software development settings.


# The default plan today, with one addition


Plan for lecture today: same as section yesterday, after a short discussion in the main room.  Plus one twist : each team make a post on the project channel describing PRs done, and those in progress/planned.



