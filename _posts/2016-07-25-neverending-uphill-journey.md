---
title: A Neverending Uphill Journey
layout: post
summary: The journey to understand the "full stack" never ends--it just gets more and more complex as layers of abstraction are added and then eventually solidify.  And that's ok. 

---

The advancements brought about by the [DevOps](https://www.youtube.com/watch?v=o7-IuYS0iSE) culture movement in the past 6+ years are nothing short of a computing renaissance, and the pace isn't slowing.  Where one or two tools used to exist to administer large numbers of systems, there is now an entire industry of open-source and commercially backed software built by many talented teams and individuals that can solve nearly every problem.  What I've noticed, though, is that the scope of knowledge needed to fully understand each layer has exploded with that growth.

For me, that's an odd feeling.  Until recently, I've felt like I had a solid grasp on all the layers.  Somewhere in the past 2 years or so, I started noticing that concepts and frameworks have become so abstract and divorced from the actual resources that I no longer was able to just watch/listen to a talk at a conference and have a really good idea of what's going on.  I've often had to spin up a [vagrant](https://vagrantup.com) box or [cloudformation template](https://aws.amazon.com/cloudformation) and read a readme in [Github](https://github.com) just to be able to truly grok what that project is doing.  In addition, you really have to be working with some of these technologies to be able to appreciate the new capabilities as they are released.

As a long time user of [AWS](https://aws.amazon.com), I've always wanted my own private AWS region to practice against.  However, installing [Openstack](https://www.openstack.org) in the [Folsom](https://www.openstack.org/software/folsom/)/[Grizzly](https://www.openstack.org/software/grizzly) era wasn't exactly straightforward.  But all these companies are using Openstack and/or [Docker](https://www.docker.com) to great effect.  Some on bare metal, some in public clouds, and some doing both.  Every conference seems to advance the state of the art by leaps and bounds, and I want to keep up despite not working for a unicorn with massive scaling problems necessitating novel solutions to those problems.

So, when I was able to get my hands on some decently powerful lab hardware, it sort of clicked.  I'm going to make my way up the stack building a private cloud capable of running both VMs and Docker frameworked workloads.  Maybe even going hybrid with AWS.  Of course, I'll document things along the way.

## Project Goals ##

1. To build a private cloud stack capable of running various workloads and testing new projects published by the community quickly.
2. To learn what it actually takes to manage all layers of the "full stack" using a balance of best practice and budget.
3. To apply my background in InfoSec to see if there are any issues or room for contribution.
4. To give back to the community (that I owe my career) by sharing all code and documentation publicly.

## Hardware ##

* 3 x 2012 Mac Minis
* 1 x 2008 Mac Pro
* 2 x 20?? Dell servers
* 3 x 20?? SuperMicro servers
* 1 x Zotac Mini PC
* 1 x 4 port Pfsense firewall PC
* 1 x Dell Powerconnect 2816 Gb switch

## Roadmap ##

#### MaaS ####
A lifecycle system to manage the provisioning and re-provisioning of hardware to a known-good, starting state.

* [MaaS Part 1 - PXE booting PCs and Netbooting Macs]({% post_url 2016-07-26-maas-1 %})
* [MaaS Part 2 - Centos 7 and Kickstart Installation]({% post_url 2016-07-26-maas-2 %})
* [MaaS Part 3 - Remaining Issues]({% post_url 2016-07-26-maas-3 %})
* [MaaS Part 4 - A Revised Approach]({% post_url 2016-07-28-maas-4 %})

#### P/CaaS ####
While not technically a P/CaaS, running frameworks like Kubernetes and/or DC/OS/Mesos/Marathon and/or Docker Swarm.

* [CaaS Part 1 - Kubernetes on Centos 7.x Bare Metal]({% post_url 2016-11-15-caas-1 %})
* [Installing Kubernetes on Baremetal via CoreOS Tectonic with Grub Booting]({% post_url 2017-08-02-coreos-matchbox %})

#### SaaS ####
Given a VM or Docker-based workload option, I want to explore various CI/CD operational models and testing frameworks using the latest automation workflows for delivering apps.

* TBD

## Next Steps ##
Probably hybrid cloud across all providers, probably exploring ubiquitous computing, probably getting ahead of myself again.  I'll leave this one TBD, too.
