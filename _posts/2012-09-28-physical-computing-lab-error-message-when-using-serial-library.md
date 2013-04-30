---
title: 'Physical Computing Week 4 Lab: Error message in Processing when using serial library?'
author: Nick
layout: post
dsq_thread_id:
  - 863229960
categories:
  - PComp
---
#

A few people have mentioned that they got an error message in Processing when doing the serial communication lab.  You may get it if you haven’t used Processing for serial communication on your computer before.  It requires you to open the terminal and enter two [sudo][1] commands.

 [1]: http://en.wikipedia.org/wiki/Sudo

Here’s the important part of it (the instructions you’ll need to follow):

> To use the serial library, first open
> Applications -> Utilities -> Terminal.app
> and enter the following:
> sudo mkdir -p /var/lock
> sudo chmod 777 /var/lock

You’ll also get a prompt to enter your system password to authorize the changes.  Once you do this, restart processing and you should be good to go.

Also to note:
Depending on your operating system and the configuration of your computer, the serial ports may appear in a different order than the example in the lab.  Make sure you’re selecting the port that your Arduino in on.

 