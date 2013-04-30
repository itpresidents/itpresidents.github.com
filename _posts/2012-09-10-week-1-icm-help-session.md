---
title: Week 1 ICM Help Session
author: Lia
layout: post
dsq_thread_id:
  - 841725004
categories:
  - ICM
  - Tutorial
---
<p><strong>GENERAL REFERENCES </strong></p>
<p><a href="http://processing.org/learning/curves/">tutorial in processing.org</a></p>
<p><a href="https://github.com/ITPNYU/ICM/">ICM Git Repository</a> &#8211; Examples from Class and More! &#8211; Great place to get started with HWs. &#8211; Click the &#8220;ZIP&#8221; file to download the whole enchilada.</p>
<p><a href="http://processing.org/reference/">Processing Reference</a> &#8211; If you have a question that starts with, &#8220;How do I&#8230;?&#8221; check here first.</p>
<p><a href="http://itp.nyu.edu/varwiki/ClassWork/Homework-upload-instructions">Instructions for uploading your homework</a> to the web.</p>
<p><strong>WHERE TO FIND CODE EXAMPLES WITHIN THE PROCESSING APP</strong></p>
<p>Go to the menu File&gt;&gt;Examples&#8230;&gt;&gt;Basics.</p>
<p><strong>DRAWING CURVES, ARCS</strong></p>
<p>There were A LOT of questions about drawing curves</p>
<p><a href="http://processing.org/learning/curves/">curves in processing.org</a> (arcs, splines, bezier)<br />
<a href="http://processing.org/learning/drawing/">drawing in processing</a> (coordinate system, simple shapes)<br />
<a href="http://processing.org/learning/color/">working with color</a></p>
<p><a href="http://www.khanacademy.org/math/geometry/circles-topic/v/circles--radius--diameter-and-circumference">Anatomy of a Circle</a></p>
<p><a href="http://itp.nyu.edu/residents/wp-content/uploads/2012/09/Screen-Shot-2012-09-10-at-4.56.31-PM1.png"><img class="alignnone size-full wp-image-192" title="Radians and Degrees" src="http://itp.nyu.edu/residents/wp-content/uploads/2012/09/Screen-Shot-2012-09-10-at-4.56.31-PM1.png" alt="" width="662" height="625" /></a></p>
<p><em>Radians and Degrees, scanned from <a href="http://shop.oreilly.com/product/0636920000570.do">Getting Started With Processing</a> (Reas, Fry 2010)</em></p>
<p>The Unit Circle<br />
<a href="http://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Unit_circle_angles_color.svg/600px-Unit_circle_angles_color.svg.png"><img class="alignnone" title="Unit Circle" src="http://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Unit_circle_angles_color.svg/600px-Unit_circle_angles_color.svg.png" alt="" width="600" height="600" /></a></p>
<p>If you are more comfortable working with degrees, you can convert from Degrees to Radians with the<a href="http://processing.org/reference/radians_.html"> radians()</a> function. So instead of saying</p>
<p><strong>arc(50, 15, 80, 80, HALF_PI, PI);</strong></p>
<p>you might write:</p>
<p>arc(50, 75, 80, 80, <strong>radians (90), radians (180)</strong>);</p>
<p>and it would be the same thing.</p>
<p>UPDATE (9/18) Dan Shiffman posted an example with different usages of arc() <a href="https://github.com/ITPNYU/ICM/blob/master/extras/arcs/arcs.pde">here</a>.</p>
<p>&nbsp;</p>
<p><strong>PRINTING YOUR MOUSE COORDINATES TO THE CONSOLE</strong></p>
<p>Drawing in Processing can be tedious if you always have to estimate where your coordinates should be. Wouldn&#8217;t it be great if you could use the coordinates of your mouse position to tell you where you need to draw?</p>
<p>Type this within the DRAW loop:</p>
<p><a href="http://processing.org/reference/println_.html">println</a> (&#8220;X: &#8221; + mouseX + &#8221; Y: &#8221; + mouseY);</p>
<p>now move your mouse pointer around the sketch and check your console for the coordinates!</p>
