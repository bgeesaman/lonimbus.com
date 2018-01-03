---
layout: post
title:  "Speaking at KubeCon 2017 - Part 1 - The CFP Submission"
date:   2018-01-03 8:54:07 -0500
permalink: speaking-at-kubecon-2017-part-1-the-cfp-submission
categories: kubernetes kubecon speaking
---

In this four part blog series on my journey to speaking at KubeCon 2017, I want to share the knowledge that I have learned in the hopes that it encourages others in the community to muster the courage and confidence to bring their own unique experiences to light.

##### Post Series Navigation:

* [Part 1 - The CFP Submission]({% post_url 2018-01-03-speaking-at-kubecon-1 %})
* [Part 2 - Research]({% post_url 2018-01-03-speaking-at-kubecon-2 %})
* [Part 3 - First Run]({% post_url 2018-01-03-speaking-at-kubecon-3 %})
* [Part 4 - The Talk]({% post_url 2018-01-03-speaking-at-kubecon-4 %})
* [The Recorded Talk](https://www.youtube.com/watch?v=vTgQLzeBfRU)
* [The Final Slides](http://goo.gl/TNRxtd)

## The Desire to Speak

I've been in the InfoSec space for some time, and I've attended a decent range of conferences as an attendee or vendor in all of them.  In some cases, I've given presentations to decent sized audiences as a Sales Engineer, but it wasn't a topic of passion.  The preparation process and execution was excellent practice, though, and it definitely removed my fear of public speaking.

So, it seems I was always prepared *mechanically* to do it.  I just needed the right mix of topic, expertise, and timing.  I knew I could execute on it if I just found the right "thing" to speak about. 

## Choosing the Topic

When the project at work I was working on hit a major milestone, I had a chance to think about what we accomplished leveraging Kubernetes.  I reflected on the fact that in the middle of our project, KubeCon 2016 videos were released.  I distinctly remember saying to myself, "Wow, what a treasure trove!" and I immediately linked several videos to colleagues with a *must watch* tag.  In the back of my mind, I sort of had this notion that I owed the community something in return.

That reflection led to thinking about a deep dive technical overview of what we built, how we built it, and what we learned as something to potentially submit.  Everybody loves deep dives, right?  All the hype gets peeled back, and the harsh realities and trade-offs of production come to light.  What better way to give back to the system administrators and implementors?

While I was listing some of the challenges that we had to solve or work around, I realized that most of them were related to hardening our Kubernetes cluster for our use case.  The defaults were pretty wide open, and we spent a lot of time "closing the door and locking it" so to speak.

As I made some notes for each item on the list of security hardening steps we took, I decided to look at some of the other projects in the community that installed Kubernetes to see if they already had these covered.  As in, "maybe the installer we picked just had these as the defaults" and we needed to use another installer next time around.  I began a quest of sorts to find "the one" Kubernetes installation or managed service that embodied and enforced the "internally secure components and isolated workload" opinions that I shared.  However, after looking at about 9 or 10, the pattern had emerged.

The community had to know what I saw.  I felt morally and ethically compelled to share this information, because I'd wager a good percentage of production clusters in the wild were essentially one small vulnerability from cluster takeover or cloud account compromise.

I set out to contact every single project and/or service I looked at to let them know what I was finding, and in that process, I met an uncharacteristically welcoming and friendly community.  Every single one of them responded to my writeups.  Every single one thanked me.  Most kept in touch over the months leading up to KubeCon.  To say that it was a positive culture difference from the InfoSec world would be an understatement.

## Writing the CFP Submission

I suppose I was fortunate that I had this knowledge before writing the CFP submission.  It certainly made it easier to write.  But CFP submissions aren't judged solely on technical merit.  Having never written one before, I decided that mimicking the tone and delivery of prior successful abstract and bios was my best bet.

So, I hit up the CNCF Youtube page, sorted by "most popular", and pulled the abstracts and bios of about two dozen of the best technical videos and tried to find a few that sounded like something I'd write, but better.  After surgically creating my franken-bio-stract, I had a decent start.

Looking at the CFP submission form, though, there was an extra field to the effect of "How would your talk benefit the community?".  I'll admit, this fantastic question threw me for a loop.  "Yeah, how would I maximize this talk and the supporting data in terms of the contribution to others?" I remember saying to a good friend.

## Peer Review

It's my firm belief that the 4 conversations I had prior to submitting were what shaped it into something worthy of selection.  Answering for questions like "who is your audience, and why would they care?" and "what are you doing to fix these issues?" made me realize my talk was missing a key goal: "What can I show the audience that is better today than 4 months ago when I found and disclosed these issues?"

Once I asked the right question of myself, I had the right answer to the community benefit section.  My goals became:

* Demonstrate what is feasible and possible in terms of potential attack vectors
* Disclose those issues to the community in a responsible way early
* Determine the best methods of prevention for each attack
* Work really hard to have fixes already in place or clear guidance on how to prevent them before the talk
* Present the issues with those fixes to the public/audience in clear and objective manner

[Hacking and Hardening Kubernetes Clusters by Example](https://www.youtube.com/watch?v=vTgQLzeBfRU) wasn't the greatest title, but it got to the point of the talk decently enough.  After writing and re-writing it about 6 times, I finally submitted it once I was convinced "I simply can't make it any better without making it worse".  

## The Waiting Game

And then, the wait.  Submissions were due on August 21st, but the overwhelming number of submissions led to a form of DoS attack on the committee that made the selection take a few weeks longer than anticipated.

The only way to take my mind off of the waiting was to decide that I was going to do the talk regardless of acceptance to KubeCon, so just set out to do the work as if I was.

When the acceptance email came, I was awash with relief.  I had spent a lot of personal time and racked up some decent cloud bills doing the legwork, and I was happy to know the plan was coming together.  The next day, though, I was overcome with deep, deep feelings of Imposter Syndrome.  I felt this sudden weight of pressure to live up to some imaginary bar of the excellence of all previous KubeCon talks, the desire not to let the committee regret their choice because so many good folks had theirs rejected, and the thought that maybe I wasn't "expert" enough to deliver this topic properly.

While I can't say I completely overcame those feelings, sharing that I had them with several members of the community helped me achieve some perspective.  I'll admit they were the constant driver to keep going and to produce the best possible body of work I could on the topic.

##### Post Series Navigation:

* [Part 1 - The CFP Submission]({% post_url 2018-01-03-speaking-at-kubecon-1 %})
* [Part 2 - Research]({% post_url 2018-01-03-speaking-at-kubecon-2 %})
* [Part 3 - First Run]({% post_url 2018-01-03-speaking-at-kubecon-3 %})
* [Part 4 - The Talk]({% post_url 2018-01-03-speaking-at-kubecon-4 %})
* [The Recorded Talk](https://www.youtube.com/watch?v=vTgQLzeBfRU)
* [The Final Slides](http://goo.gl/TNRxtd)
