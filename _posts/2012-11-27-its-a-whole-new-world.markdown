---
layout: post
title:  "It's a whole new world"
date:   2012-11-27 12:23:47
excerpt: "An Ubuntu converts review of the awesome new [Elementary OS](http://elementaryos.org)."
categories: blog
---

### My thoughts on a week with elementary OS.
I've been an Ubuntu user for 7 years now, but I hate what it's become. I really, really hate it. For a year I've had to contend with only being able to boot my PC using the boot loader on an old Mac OSX "hackintosh" CD after the upgrade to 11.10 ruined my hard disks boot partition beyond repair (I devoted a full two weeks to fixing it at one point, it will not work). I haven't had a properly working third monitor since my foray into Linux began.

I'm not one of those people who was disgusted at the appearance of Unity. I think the idea is brilliant, but it's so poorly executed it's put me off the whole Ubuntu ecosystem. It runs like a hippo in quicksand, and because of my third monitor I'm forced to use unity 2d, which is even worse, and it was recently announced that unity 2d will no longer be supported in future versions. The speed is a huge issue for me. My desktop machine has 6 cores and 16GB of RAM - even under windows it’s capable of running anything you can throw at it - but with unity in either 2d or 3d mode, even the simplest task takes an age to complete.

I haven't switched to another OS yet, simply because I haven't found another distribution that offers the same no nonsense ease of use that made me originally choose Ubuntu for everyday use. My desperation even caused me to go so far as to attempt to build my own distribution, but lack of time and knowledge meant that this idea was soon discarded.

This week the team at elementary released Luna beta 1, and it seemed like a good time to set aside a partition and see if it could replace Ubuntu as my OS of choice. After a week of getting used to the UI, and setting up my usual applications and settings I have to say I'm thoroughly impressed. I'll outline some of the most important points (for me) below:

#### Speed
**It’s quick**. By god it's quick. As a small comparison, I created a small php test page to pull in 1000 rows from a local mysql database and echo the results to the browser. Admittedly, under elementary I'm using nginx, rather than apache2 under Ubuntu (as I could never get nginx working), but other than that the setup is identical. Under Ubuntu the page load would take 3-4 secs on average. In elementary, it takes <250ms. This is a huge difference, which makes for a much faster development workflow.

Part of this speed increase is due to much lower RAM usage. This is evident when using large images in gimp. I regularly work with 3-4GB multi-layered images. Having one of these open in Ubuntu meant that using the PC for anything else at the same time was impossible. Now I can comfortably work on 3 or 4 at once, and still have multiple tabs in chrome, rhythmbox and an IDE open, and everything still works perfectly.

#### UI
I've complained before about the insistence of OSes on developing new and markedly different user interfaces - such as unity or metro in windows - without concentrating on the small details that have provided annoyance in every version of modern OSes. A prime example is the standard three window controls, positioned next to reach other in one corner. I bet you've never even noticed a problem with this system, as no one has ever challenged it, but how many times have you accidentally closed an important document whilst aiming for the maximise/minimise buttons? Elementary has a solution, close on the left, maximise on the right, a simple change that makes a lot of sense, and removes any chance of inaccuracy.

Another example is the changes to the file browser. You can now single click to open files and folders instead of double click, and each icon has a small plus sign attached to it to allow you to select multiple files, without the need to hold the CTRL key. Again, a small change which makes for a much more intuitive user experience.

Using ALT+TAB to switch between windows is a joy. Rather than displaying a row of icons, all windows fade away, leaving only the selected one visible, and then all restore with the selected window on top when ALT is released. The window of choice is much easier to identify this way, particularly if you have multiple instances of the same program open.

The Applications menu is another huge improvement over Unity and Gnome, giving a simple view of the applications installed on the system without any of the unnecessary rubbish added to the menu by other OSes.

Hot corners are included in Ubuntu, but due to the terrible performance any use of animated features becomes a burden under heavy use. In elementary everything is smooth, and works as designed.

All of the default applications feature excellent user interfaces, keeping things lightweight and concentrating on quality rather than quantity of features. A commendable choice by the design team, and it has made elementary incredibly easy to use.

#### Plank
Plank is a huge breath of fresh air. It's exactly what unity should have been, instead of the behemoth it is today. It has icons, you click on them to open programs; it doesn't need to do anything else, and as a result startup and login time is massively reduced, because you don't have to wait for the system to load countless features that you'll never use.

#### Geary
Geary is the first linux email application I’ve even considered using over the Gmail web interface, and will more than likely use it as my main email client. It reads and sends emails, and shares the conversation view of the web interface. I have no need for custom labels or rules, and by omitting these and a number of other rarely used features the application is a joy to use.

#### Noise
I haven’t been able to test Noise, as the application crashes as soon as I try to import any music. I’m told that an update is in the pipeline so we’ll have to wait and see how that pans out. That said, the interface looks good, with the same simplicity as the rest of the OS, so I’m looking forward to being able to test it properly.

#### Midori
For casual browsing Midori is an excellent choice. It’s fast, simple and conforms to web standards. As a web developer I still need to use chrome due to a number of browser extensions I use, but when I’m not working I find myself jumping to Midori so that I can get to the information I want without any distractions. The RAM usage is also much lower than in chrome, firefox or opera.

#### Install and boot time
Install was quick, easy and seamless. Elementary shares Ubuntu’s installer, and admittedly it is one feature which Canonical got right, so it was a good decision to keep it in here.

Boot time is much quicker than Ubuntu or windows, due to the lightweight nature of the operating system and the desktop environment, there simply isn’t as much to load.

#### A few niggles
The third monitor is still a no-go for me, but this is largely down to the poor drivers Nvidia is still putting out for linux. One day, someone will finally work out a way to fix this.

Hot corners only apply to the primary screen, rather than the desktop as a whole. I’m not sure if this is a bug or a feature, but if the two monitors you use are the same size only two of the hot corners are useable.

Custom shortcuts don’t currently stay pinned to the dock through the right click menu in Plank, disappearing when the application is closed. They can be added by modifying the configuration file though.

#### Conclusion
All in all, for a week old beta, it’s a huge step in the right direction. There are still bugs to iron out, but given the quality of work by the team so far, I’m confident that elementary will be as near to flawless as possible by final release. In fact, it’s so much better than Ubuntu already that I am now intending to use it as my production OS, whilst I patiently await the final release.

If you are an Ubuntu user, I urge you to head to [elementaryos.org](http://elementaryos.org) and download a copy of Luna Beta 1 to try out. I think you’ll be pleasantly surprised.