---
title: Intro to OF
author: Lia
layout: post
dsq_thread_id:
  - 1059899203
categories:
  - Uncategorized
---
<p>Hi all,<br />
<a href="https://github.com/itpresidents/oF_bouncing_ball_objects_with_vectors">Here is the example </a>we looked at with a vector of bouncing ball objects.<br />
To try it out, download and unzip the repo.  Then, move the &#8220;ball_bounce_demo&#8221; folder into your Openframeworks &#8220;myApps&#8221; folder and open the xcode project file( ball_bounce_demo.xcodeproj).</p>
<p>Here&#8217;s the presentation that we used to guide us through the workshop.<br />
If you need more help, please don&#8217;t hesitate to come for office hours with Lia, Genevieve, Nick or Merche!</p>
<p><iframe src="https://docs.google.com/presentation/d/1w0RH3kLu9kgd1k7kk_J4BlC0EEESMvypGPS9XGr5PAQ/embed?start=false&amp;loop=false&amp;delayms=3000" height="749" width="960" allowfullscreen="true" frameborder="0"></iframe></p>
<p>&#8212;&#8212;&#8212;&#8211;<br />
addendum (Lia):<br />
There was a question about when to use or not use the &#8220;new&#8221; operator when creating new objects in C++. I didn&#8217;t answer it very well (and probably still won&#8217;t), but it has to do with memory management. In Processing, we make a new object like so, where we always use the &#8220;new&#8221; operator:</p>
<p><code>myClass x = new myClass();</code></p>
<p>in C++, there are two ways to make a new class, and which way you choose depends on if you want to allocate memory from the heap or the stack. </p>
<p><code>    // on the stack<br />
    myClass x;</p>
<p>    // or on the heap ... see the pointer??<br />
    myClass *x = new myClass;</code></p>
<p>If you&#8217;re using the stack (no pointer), you access member variables and functions like so: </p>
<p><code>x.myVariable; </code></p>
<p>if you&#8217;re using the heap (pointer), you would use this:<br />
<code>x->myVariable; </code></p>
<p>We don&#8217;t want to get too much into it at this point, but if you want to read more about Heaps and Stacks, <a href="http://www.learncpp.com/cpp-tutorial/79-the-stack-and-the-heap/">try this link. </a>. Here is Jeff Crouse&#8217;s tutorial on <a href="http://www.jeffcrouse.info/teaching/cpp-constructors.html">C++ constructors</a>. <strong>tldr</strong>: unless your object is large, or you need to use it beyond local scope, use the stack (no pointers) way. </p>
