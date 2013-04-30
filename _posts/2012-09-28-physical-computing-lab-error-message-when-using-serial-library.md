---
title: 'Physical Computing Week 4 Lab: Error message in Processing when using serial library?'
author: Nick
layout: post
dsq_thread_id:
  - 863229960
categories:
  - PComp
---
<p>A few people have mentioned that they got an error message in Processing when doing the serial communication lab.  You may get it if you haven&#8217;t used Processing for serial communication on your computer before.  It requires you to open the terminal and enter two <a href="http://en.wikipedia.org/wiki/Sudo">sudo</a> commands.</p>
<p>Here&#8217;s the important part of it (the instructions you&#8217;ll need to follow):</p>
<blockquote><p>To use the serial library, first open<br />
Applications -&gt; Utilities -&gt; Terminal.app<br />
and enter the following:<br />
sudo mkdir -p /var/lock<br />
sudo chmod 777 /var/lock</p></blockquote>
<p>You&#8217;ll also get a prompt to enter your system password to authorize the changes.  Once you do this, restart processing and you should be good to go.</p>
<p>Also to note:<br />
Depending on your operating system and the configuration of your computer, the serial ports may appear in a different order than the example in the lab.  Make sure you&#8217;re selecting the port that your Arduino in on.</p>
<p>&nbsp;</p>
