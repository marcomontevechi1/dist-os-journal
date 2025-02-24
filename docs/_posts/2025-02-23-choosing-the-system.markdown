---
layout: post
title:  "Choosing the system"
date:   2025-02-23
categories: OS
---

1. [Overview](#overview)
2. [Manufacturer Provided System](#manufacturer-system)
3. [Distributed options](#dist-options)
4. [Another option: hadoop](#hadoop)

A scorched land of weird systems awaits...

## Overview <a name="overview"></a>

I want to operate several computers in a transparent way, that is: to use them as much as a single system as I can.
I want this to be a learning opportunity: how will the filesystem behave? RAM allocation and usage? Performance? etc.

## Manufacturer system (not distributed) <a name="manufacturer-system"></a>

For starters, the Odroid N2+ manufacturer provides a simple ubuntu server system which can be downloaded [from here](https://wiki.odroid.com/odroid-n2/odroid-n2). Of course, this has nothing to do with a distributed system but It's good to get to know your hardware. The images can be flashed into an SD card with balena etcher. For some reason I couldn't make Startup Disk Creator understand the images (I think it only understands .iso).

A quick experimenting phase with it showed this is an ubuntu server like any other. Nothing new here, you can use apt at will, configure systemd services etc.

![odroid2 experimenting]({{ site.baseurl }}/assets/odroid2.GIF)

## Distributed options <a name="dist-options"></a>

The [Single-System Image wikipedia page](https://en.wikipedia.org/wiki/Single_system_image) is a good place to start. Besides having a nice explanation for the main features of a distributed system, it has a nice table with common systems and which of each feature they implement.

The [distributed operational system wikipedia page](https://en.wikipedia.org/wiki/Distributed_operating_system), on the other hand, has a good history and conceptual discussions. It also has weird phrases seemingly written by someone who likes fancy words:

> (...) the exceptional degree of inherent complexity could easily render the entire system an anathema to any user (...)

"Anathema" is a fancy word. I like this one.

> (...) These design and development considerations are critical and unforgiving. (...)

Getting eerie and ominous...

Anyway, after reading a bit and trying to stick to open source solutions I realized the most interesting options were:

- OpenSSI - Open source, implements everything except process checkpoint, latest release by 2010;
- Inferno - Open source, doesn't implement much functionalities but is more actively developed;
- Plan9 - Same as Inferno;
- TidalScale - Closed source but had the most recent release date.

I had a series of unfortunate discoveries:

- OpenSSI is basically dead. It supports up to Debian 5 or something. Too old for me.
- TidalScale is basically a product and I would have to pay. Unacceptable. 😤
- Inferno seemed interesting, but also looked old and with scattered sources. Seems like could be worth trying.
- The original plan9 project was abandoned and forked into 9front - an alternative with currently active development.
  9Front has official releases and a manual clearly written by non-neurotypical people. Parts of its
  charm include:
  - A manual topic called "Help", followed by the word "NO." and the next topic;
  - A topic called "Frequently questioned answers";
  - A release from 2024 called "DO NOT INSTALL";
  - A [section from source code"](https://git.9front.org/plan9front/pyhg/HEAD/info.html) called "snake oil(???);
  - An [active subreddit](https://www.reddit.com/r/plan9/) full of people willing to help you;
  - A cute bunny mascot called glenda.

<p align="center">
  <img src="{{ site.baseurl }}/assets/glenda.jpg" />
</p>

I think it's pretty clear which system I chose.

## Another option: hadoop <a name="hadoop"></a>

[Apache Hadoop](https://hadoop.apache.org) is not a distributed operational system, but more of a framework for distributed software development
and server management, if I understand it correctly.
Nevertheless, it seems to have more usage in modern contexts and to be much more of a useful learning
opportunity than plan9/9front itself.

It provides a distributed filesystem, task trackers and schedulers, fault tolerance mechanisms... etc.

So when all else is done and I finally come to the unavoidable conclusion that I don't want to stick with
9front on my day-to-day life, I might use the cluster to experiment with hadoop and see where I go.

It also has a cute elephant mascot, although he seems either a bit tired or old. Well, a lot to manage for him, I guess.

<p align="center">
  <img src="{{ site.baseurl }}/assets/hadoop-logo.jpg" />
</p>
