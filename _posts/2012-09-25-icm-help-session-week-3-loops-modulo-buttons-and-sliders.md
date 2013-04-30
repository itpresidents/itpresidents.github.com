---
title: 'ICM Help Session Week 3: Loops, Modulo, Buttons and Sliders'
author: Mimi
layout: post
dsq_thread_id:
  - 858192652
categories:
  - ICM
  - Tutorial
---
<h1><a href="https://github.com/itpresidents/ICM-Help-Sessions/tree/master/ICM_Help_Session_Week_3">Code Examples Here</a></h1>
<h1>How to make a Slider | <a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_Slider/ICM_Help_Week3_Slider.pde">Code</a></h1>
<p>This is a great example for understanding the following Processing functions:<br />
<strong></strong></p>
<ol>
<li><strong><a href="http://processing.org/reference/constrain_.html">constrain()</a></strong> &#8211; How to make the slider button not fall off the ends of the slider.</li>
<li>Using variables to keep a bunch of shapes together relative to the mouse. (Our slider button is a complex shape comprising of 2 circles and 2 lines, all moving together relative to the y-location of the slider bar and the x-location of the mouse.)</li>
</ol>
<h1>Using Loops to Generate Patterns | <a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_LoopsAsPatterns/ICM_Help_Week3_LoopsAsPatterns.pde">Code</a></h1>
<ol>
<li><strong><a href="http://processing.org/reference/modulo.html">% modulo</a> </strong>- Use division to create &#8220;regular&#8221; patterns, e.g. alternating rectangles by only filling a rectangle with &#8220;black&#8221; if the index number of the rectangle (in the loop) can be divided by 2 without a remainder. (e.g. 0, 2, 4, 6, 8, 10, 12, etc&#8230;)</li>
</ol>
<h1>Interactive Buttons | <a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_Buttons/ICM_Help_Week3_Buttons.pde">Code</a></h1>
<p>We went over this example which shows 4 different kinds of interactive buttons working side by side.</p>
<ol>
<li>Momentary click</li>
<li>Turning a button ON and OFF</li>
<li>Mouseover or Hover effect</li>
<li>Momentary click plus Mouseover or Hover effect</li>
</ol>
<p>Concepts convered include:</p>
<ol>
<li>Using <strong>booleans</strong> to keep track of on/off states</li>
<li>What&#8217;s the difference between <a href="http://processing.org/reference/mousePressed.html">mousePressed</a> and <a href="http://processing.org/reference/mousePressed_.html">mousePressed()</a>?</li>
</ol>
<p><strong><a href="http://processing.org/reference/mousePressed.html">mousePressed</a></strong> is a Processing variable like mouseX that tells you if the mouse button is pressed down.</p>
<p><strong><a href="http://processing.org/reference/mousePressed_.html">mousePressed()</a></strong> is a function that runs code  you write <strong>ONE TIME</strong> when you click the mouse.</p>
<p><a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_2/ICM_Help_Session_Week_2_events/ICM_Help_Session_Week_2_events.pde">This sketch illustrates it. </a></p>
<p>So then can you guess what&#8217;s the difference between keyPressed and keyPressed()?</p>
<h1>Teaser For Next Week</h1>
<p>How do you create a grid of on/off switches?<br />
<a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_ToggleGrid_Alt/ICM_Help_Week3_ToggleGrid_Alt.pde">Approach 1</a><br />
<a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_ToggleGrid/ICM_Help_Week3_ToggleGrid.pde">Approach 2</a> (with hover state)<br />
<a href="https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_ToggleRandomWithLines_pde/ICM_Help_Week3_ToggleRandomWithLines_pde.pde">Approach 3</a> (randomly placed cells with drawing via objects)</p>
<p><a href="http://itp.nyu.edu/residents/wp-content/uploads/2012/09/photo1.jpg"><img class="alignnone size-large wp-image-440" title="photo" src="http://itp.nyu.edu/residents/wp-content/uploads/2012/09/photo1-1024x764.jpg" alt="" width="584" height="435" /></a></p>
