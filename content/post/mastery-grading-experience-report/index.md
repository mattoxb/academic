---
title: 'Mastery Grading - an Experience Report'
author: Mattox Beckman
date: '2021-07-07'
slug: mastery-grading-experience-report
categories: ["teaching"]
tags: []
header:
  caption: ''
  image: ''
---

I recently read Linda Nilson's book on Specifications Grading, and wanted to try that in my course.  It turns out that
I implemented Mastery Grading, not Specifications Grading, but the two are similar.

The basic idea is that we get away from a points-based economy for calculating grades, and instead use a series of mastery
areas.  The grade is then based on how many mastery areas the student completes.  Here are the steps I took, and some lessons
I learned along the way.

## Step 1 -- Determine the mastery areas

The first step was to decide on 20 mastery areas. For CS 421 I called them "Learning Modules" (which instantly got abbreviated
as "LMs").  For example, the first LM was called "Recursion".   Each LM then had some "Outcomes",  usually four of them.
Each outcome was worth a certain number of points, and I made the total number of points sum to 10.

Once you have these, you decide how you are going to measure these. Each assessment in the course would contribute
points to one or more outcomes.  So, for the Recursion LM, the first outcome was to write a recursive function over integers,
in direct style.  There was a homework assignment available on the web (we called these "activities") that would give 1 point,
and an exam question that would give another point to this outcome.  So, a student would have to do both the activity and the
exam to get the points for the outcome.

One of the features of mastery learning is that the assessments are all-or-nothing.  Since this was my first time trying it,
I set a threshold of 80% for a problem to count.  If the student got at least 80% of the points, they got credit for the assessment,
otherwise they got nothing.  (In practice, getting *just* 80% is hard; typically scores were either 100% or something lower than
50%.)  Similarly, to get credit for the learning module, the student needed 8 of the 10 outcome points.

To balance the all-or-nothing nature of the course, students had multiple attempts at the activity, typically one week of time.
They could keep trying the assessment until they got it right.  This, by the way, is why what I was doing was not specifications
grading; in specs grading, students start off with a certain number of token, and have to spend one in order to redo an assessment.
Since everything was computer graded, I just let students keep practicing until they got it --- allowing retakes is free for me.

I'm not sure if I will try a token-based system in the future or not; it would cause students to be more careful up front, but
with a class size of over 300 students, this could be a lot to manage.

## Lesson 1 -- A lot of stuff wasn't getting measured before!

I was surprised to discover that many of the outcomes I listed had no assessments attached to them at all.  I think this is typical
in a course; when writing an exam you cannot ask about *everything* you want students to learn, but now that I was requiring them
to demonstrate mastery of all these outcomes, I had to develop assessments to do so.  That was a lot of work, but now that I have them
written it should be simple to implement in the future.

## Lesson 2 -- Communication is key!

This was the first course my students ever had that used mastery grading. Reactions varied quite a bit, but most
students liked knowing precisely what they needed to study. It took me a few attempts to discover how to communicate
each student's progress in fulfilling outcomes, and letting students know which assessments fulfilled them.  The end result looked
something like a spreadsheet.  I used a Postgres database with a front-end written in Haskell to keep track of the grades and report
them to the students.  Putting that together also was a lot of work.

## Benefits

Students could fulfill their outcomes and learning modules on the midterms, activities, and machine problems.  The final exam then
functioned as a "second chance" exam they could take to retry fulfilling an outcome if they had missed it on the midterm.  This made
the final exam effectively optional.  If they only needed points for one last LM, they could do that question by itself and skip the
rest of the final.  Students liked that this scheme greatly reduced stress.

The other benefit was that I only got one single email the whole semester where a student was point-grubbing for partial credit.  Once
I told them that going from 60% to 65% on the assignment would have no effect at all they let it go, and presumably studied the problem
so they would get it right on the final.  Now the student is learning the material and not counting out points!

## Next Time

Things I might change for next time.... I will try to have a single web page with the LMs, outcomes, and corresponding assessments as a single
source of truth for the grades.  I had tried to use the database to generate this, but it was significantly more work to keep it updated than
I expected.  Using a hand-edited web site would be more direct.

I might try using tokens for retakes, but I'm not sure if that makes much sense in this course, since restricting assignments would actually
be more work than just leaving them open.

I will probably move the assessment threshold to 100% instead of 80%.  The original 80% was a buffer, and no longer seems necessary
to me.

In conclusion, I think this was a huge success, and will definitely grade this way from now on.  It's a lot of work getting it set up, but
now if a student says they got an A in my class, I can confidently say what that means.
