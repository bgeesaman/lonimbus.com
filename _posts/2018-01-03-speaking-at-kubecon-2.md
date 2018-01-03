---
layout: post
title:  "Speaking at KubeCon 2017 - Part 2 - Research"
date:   2018-01-03 8:55:07 -0500
permalink: speaking-at-kubecon-2017-part-2-research
categories: kubernetes kubecon speaking
---

Having performed a good portion of the research and validation prior to being accepted as a form of passing the time, I'll admit I let the scope creep a bit too far.

##### Post Series Navigation:

* [Part 1 - The CFP Submission]({% post_url 2018-01-03-speaking-at-kubecon-1 %})
* [Part 2 - Research]({% post_url 2018-01-03-speaking-at-kubecon-2 %})
* [Part 3 - First Run]({% post_url 2018-01-03-speaking-at-kubecon-3 %})
* [Part 4 - The Talk]({% post_url 2018-01-03-speaking-at-kubecon-4 %})
* [The Recorded Talk](https://www.youtube.com/watch?v=vTgQLzeBfRU)
* [The Final Slides](http://goo.gl/TNRxtd)

## How I Approached the Problem

My search for a Kubernetes installer or managed service that shared my desired set of default security capabilities and settings hardened out-of-the-box took much longer than I had anticipated.  It was a very time consuming journey, but that arduous process fraught with tedium brought the perspective and expertise over time that I needed to feel confident during the talk.

After manually discovering, installing, configuring, testing/prodding, and destroying a dozen or so tools/services, I was able to come up with a set of possible attacks stemming from configuration issues that were common to most of them.

It was then that I realized that many of the installers had released updates in that short window of time, forever locking those findings to those versions.

I needed a tool to help me solve the problem of being able to easily acquire and install newer versions of an installer's release while also being able to go back and re-assess an older release several months later reliably.

[KubeATF](https://github.com/bgeesaman/kubeatf) was hacked together late at night using the tools I knew best: bash and Ansible.  It attempts to be a simple CRUD interface for spinning up, validating, and destroying clusters with repeatable results.  While it may not be useful outside this context, I think it was worth sharing in the interest of being completely transparent about my assessment approach in case anyone disagreed with it.

## Reaching Out to the Community

When I reached out directly to the folks at [Heptio](https://heptio.com), [kops](https://github.com/kubernetes/kops), and [kube-aws](https://github.com/kubernetes-incubator/kube-aws), I got very positive responses to what I was highlighting.  Instead of ignoring, downplaying, or outright dismissing me, I was asked to help them ensure they accurately captured the issues.  This provided all the validation I needed to know that this work was not only useful -- it was openly welcomed.

Disclosing to a couple of the bigger named providers was much more formal and drawn out, but it certainly wasn't a negative experience.  Thankfully, all of my issues identified were already on their radar and on track for resolution.  

## Scope Creep

The months between acceptance and actually presenting were longer than I expected, so I became somewhat of a connoisseur of installers.  It was a pretty standard process to take one and make it work inside ```kubeatf```, so I could assess them against my criteria from start to finish in under 3 hrs.  In hindsight, I went overboard a bit, but it did make for a more comprehensive looking results graph.

I also spent some time making a plugin for [Heptio's Sonobuoy](https://github.com/heptio/sonobuoy) tool called [bulkhead](https://github.com/bgeesaman/sonobuoy-plugin-bulkhead) in the attempt to perform some level of assessment against the CIS Kubernetes Benchmark by dropping in Aqua Security's [kube-bench](https://github.com/aquasecurity/kube-bench) tool.  This really could have been an entire talk topic itself, so I released it in its initial format with plans on working on it again in the future.

##### Post Series Navigation:

* [Part 1 - The CFP Submission]({% post_url 2018-01-03-speaking-at-kubecon-1 %})
* [Part 2 - Research]({% post_url 2018-01-03-speaking-at-kubecon-2 %})
* [Part 3 - First Run]({% post_url 2018-01-03-speaking-at-kubecon-3 %})
* [Part 4 - The Talk]({% post_url 2018-01-03-speaking-at-kubecon-4 %})
* [The Recorded Talk](https://www.youtube.com/watch?v=vTgQLzeBfRU)
* [The Final Slides](http://goo.gl/TNRxtd)
