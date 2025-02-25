---
layout: post
title:  "Getting started with plan9front"
date:   2025-02-25
categories: OS
---

> "Do not go gentle into the command line\
> Old syntaxes should burn and rave at close of day\
> Rage, rage against users of plan9
> 
> Though wise devs at Bell Labs thought 'no UN*X-like!'\
> Because their thoughts had forked no lightning, they\
> Do not go gentle into the system plan9"
>
> \- Dylan Thomas, after experimenting with plan9 for the first time.

1. [Charming documentation](#docs)
2. [Images, installing and experimenting](#2)
3. [Spinning up the VM - plan9 and the radical search for spiritual freedom](#3)

# Charming documentation <a name="docs"></a>

If you want to have a good time, feel free to explore [their weird documentation](https://git.9front.org)
or specifically [their charming manual](https://fqa.9front.org) containing phrases such as "ACHTUNG!
Information provided by this document is UNOFFICIAL and may be outdated or just plain WRONG. Use your brain. NO REFUNDS."
or topics such as "Is plan9 a cult run by scam artists?".

# Images, installing and experimenting <a name="2"></a>

Out-of-the-box I noticed their [release page](https://9front.org/releases/2025/01/19/0/) show images for i386, amd64,
arm64, honeycomb raspberry pi's and reform. I didn't know the reform and honeycomb boards until today.

Of course, if I have the determination to it, I will need to port the system to the Odroidn2+ board since it's not available
oout-of-the-box. It seems [someone](https://github.com/adventuresin9/9front-rk3568) already started some job for Odroid M1,
but it's still not clear to me what can be repurposed from that, if anything at all.

For now, I downloaded both the .iso and .qcow files from release "THIS TIME DEFINITELY" from 2025 and started spinning up a VM.
Just to get to know how the system looks like.

# Spinning up the VM - plan9 and the radical search for spiritual freedom <a name="3"></a>

To be continued... (it's late and I'm tired) \
Continuing: (I'm still tired but it's another day today)

So, turns out 9front virtual machines are radically searching for liberation of the physical constraints that bind us all into this world
by refusing to leave the [guru meditation state](https://forums.virtualbox.org/viewtopic.php?t=109347) when booted through Virtual Box.

When I encountered this in the past it was always because of some failure to correctly virtualize the machine's resources, but no changes to RAM, CPU, etc. configuration would fix this in this case and searching in VirtualBox forums revealed that having success here is not usual.

It's not supposed to be a surprise: the [documentation](https://9p.io/wiki/plan9/virtual_machines/index.html) recommends qemu.

So:

    qemu-system-x86_64 -boot d -cdrom 9front-10931.amd64.iso -m 2048

Spwaned me a nice non-permanent system where I could go through the [installation procedure](https://fqa.9front.org/fqa4.html) and all.

A good quick start guide for the installation can be found [here](https://thorjhanson.com/blog/20220324-9front-in-qemu).

![plan9 VM]({{ site.baseurl }}/assets/plan9.GIF)

After you have your lovely machine running, a good list of UNIX-like commands translation to plan9 can be found [here](https://9p.io/wiki/plan9/Unix_to_Plan_9_command_translation/index.html).