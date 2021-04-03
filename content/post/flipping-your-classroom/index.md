---
title: 'How to Flip Your Classroom'
author: Mattox Beckman
date: '2021-03-27'
slug: how-to-flip-your-classroom
categories: ["teaching"]
tags: []
header:
  caption: ''
  image: ''
---

I frequently get asked how I went about flipping my classroom, so I decided to write it up here.  I'm going to assume
you already think a flipped classroom is a good idea and that you want to do this.  Perhaps I'll advocate for it in
another post.  For today I'm going to document what I do in hopes that others find it useful.  Let me know if you use
any of this, or have suggestions.

## The Equipment I Use

I had to get three things to set all this up.

First, I got a USB Microphone.  You can test the microphone on your computer, but most people find that theirs is not
very good.  I got the  [Blue Yeti USB Microphone](https://www.bluemic.com/en-us/products/yeti/) in 2013, and
that model is still for sale.  It has several capture modes; I usually use one called *cardioid* which is somewhat
directional.  This does a good job of capturing my voice while not capturing the sound of the computer fan if it happens
to come on during the recording.

For video capture and editing, I use [Camtasia](https://www.techsmith.com/video-editor.html) on a Windows machine
to record my video.  I'm a linux person, so for me to *actually get a windows machine just to run this software*
is saying something.  I load up my slides, select the window with Camtasia, and start recording.  It seems that
best practice is to *not* record your "talking head," otherwise students will watch you instead of looking at the slides.
This is good news: simply recording your voice over the slides is all you need.
 
Once you are done with the recording you can edit out mistakes and clicking sounds from advancing the slides.

Finally, I use [Amazon S3](https://s3.console.aws.amazon.com/s3/) to host the video file.  I export the video as an MP4 in a 16x9 aspect ratio.
Hosting this way is not expensive, and Amazon often gives out credits for educators.

## The Workflow

In brief, here is what my workflow looks like:
  - Write the slides and the transcript
  - Record myself narrating the slides.
  - Post-process the video and export it
  - Upload to Amazon 

Creating a video for a flipped lecture is a bit different from giving a lecture to a live audience.  The thing that surprises
most people is how short the videos will be.  Eight to 10 minutes is about as long as you want them!  You can have more than
one video for a class session if need to though.  The reason the videos will be so short is that you can be much more efficient
in your delivery.  Nobody is interrupting you to ask questions, you aren't looking at your slide and thinking about what to
say next.  Only the final product makes it to the recording.  Also, students are not likely to want to pay attention more that
that length of time for a single video.

### Writing the Transcript

WHen I give a talk, I usually do not have a word-for-word script in mind.  I come with a higher level idea of what I want to say,
and rely on the slides to prompt me what to talk about next.  The process of writing the slides is where I would have decided what
to say at a particular moment.  In a live lecture, this has worked well.  For recording videos, this has not worked as well.

What I do for a new lecture is to write the slides and the transcript of your lecture simultaneously.  As I write the slide, I
imagine what I would say to a live audience, and write that down.  I typically use the markdown format, which has the advantage
that it's easy to post to my website later, since I use [Hugo](https://gohugo.io) as my static site generator.

When it comes time to record, I move my slides to the windows machine and start Camtasia.  I usually have another computer or a
tablet with the transcript on it.

This next part is important: if you simply read the transcript, it will sound terrible.  You will have to voice-act the transcript.
You should not do this when you are tired.  I also find that I need to start a few times and restart to "warm up" for the performance.
Once you have a good flow going, I advise you not to stop for mistakes.  If you make a mistake, pause for a few seconds and then
start that section again, while still recording.  When you are doing post-production you will see the gap and know that it needs
attention.

### Post Production

You will do two things in this part.  First, you are cleaning up background noise (clicking sounds from advancing the slides)
and your own mistakes ("umms", sentences that you redid, and, for me, my microphone seems very able to pick up the sound of me
swallowing).

The other thing is to place annotations in the slides.  Camtasia has annotations that let you draw lines around
parts you are talking about, highlighting, and callouts for extra text.  The callouts can be helpful if you need to correct a
small mistake in the slides quickly.  The first time I recorded slides, the main complain students had was that they could
not tell what line of code I was talking about, and asked that I would highlight them in the slides somehow.

### Uploading

If you are using Hugo or some other static site generator, create a layout or shortcode to automate as much as you can.
Mine takes the slug (filename) and title, and knows where to find the corresponding mp4 file on AWS.  There's also a flag
that says if I have a transcript for that lecture.

## Final Thoughts

It is a huge amount of work to set this up.  I have found that students seem to do better with the videos; they can watch
when it's best for them, and they can replay something they didn't quite catch.  Some things to keep in mind:

  - Once the videos are set up, you will find yourself starting to forget what was in them after a few semesters.  Make
    a habit of rereading the slides and transcripts as you go through the semester.

  - Students who are new to this format will not always understand that they are expected to pay close attention to the
    videos.  You can't learn how to perform lambda calculus reductions from a video you are playing in the background
    while you are washing the dishes, but some students will try that and complain.  It's probably best to have a
    "how to get the most out of this course" section on your course website.

  - Correcting mistakes... I'm not sure if there is an efficient way to do this.  Often I find it quickest to re-record
    the whole video, but I suspect that just means I'm missing something.

