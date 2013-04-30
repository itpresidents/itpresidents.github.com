---
title: 'ICM Help Session Week 2: Variables, Conditionals, and Interaction'
author: Mimi
layout: post
dsq_thread_id:
  - 849355221
categories:
  - ICM
  - Tutorial
---
<p>What we covered in Week 2&#8242;s ICM Help Session:</p>
<p>Here&#8217;s the <a href="https://github.com/itpresidents/ICM-Help-Sessions">example</a> we created together during the help session.</p>
<h1>Variables</h1>
<p>What are they useful for? Storing information your program needs to run, especially information that changes over time (e.g. location of a ball).</p>
<p>- Declaring variables : Telling your computer you want memory to store information. (To make variables &#8220;global&#8221;, declare them at the top of the sketch outside of setup and draw)<br />
- Initializing (Setup) : What values do you want your variables to start with when you run your program?<br />
- Running (Draw): How do you want your variable values to change over time?</p>
<h1>Conditionals</h1>
<p>I want one thing to happen if and only if something else happens.</p>
<p>- &amp;&amp; and || (ands and ors)<br />
- &gt;,=,</p>
<h1>Random</h1>
<p>- I want my ball to bounce around randomly. I want my ball to change color randomly.<br />
- Why do &#8220;randomly&#8221; generated things look so evenly spread out?</p>
<h1>Creating Counters</h1>
<p>I want something to happen, but only for 5 seconds.</p>
<h1>Mouse/Keyboard Interaction</h1>
<p>- Interrupts the draw loop to run code when you interact with your keyboard or mouse<br />
- mousePressed(), keyPressed(), etc&#8230;</p>
<p><a href="/uploads/2012/09/photo.jpg"><img class="alignnone size-large wp-image-347" title="photo" src="/uploads/2012/09/photo-1024x764.jpg" alt="" width="584" height="435" /></a></p>
<p>&nbsp;</p>
<p><strong>STATE SWITCHES</strong></p>
<p><a href="https://gist.github.com/3744207">Here</a> is an example of how to use a boolean, conditionals, and mousePressed to create a simple state switch- changing the color of a circle from one to another. </p>
<p>Click the mouse over the circle! </p>
<p><script type="application/processing">
//Info: http://processingjs.org/reference
color redColor;
color blueColor;

boolean colorIsRed;

void setup () {

  redColor = color (255, 0, 0);
  blueColor = color (0, 0, 255);

  colorIsRed = false; //default to a blue color

}

void draw () {

  background(255);

  //conditional changes the fill color based on the colorIsRed boolean
  if (colorIsRed == true) {
    fill (redColor);
  }
  else {
    fill (blueColor);
  }

  //draw the ellipse
  ellipseMode (CENTER);
  ellipse (width/2, height/2, 50, 50);
}

void mousePressed () {

  colorIsRed = !colorIsRed; //make colorIsRed equal to whatever colorIsRed is NOT
  println ("colorIsRed is: " + colorIsRed);
}


</script></p>
