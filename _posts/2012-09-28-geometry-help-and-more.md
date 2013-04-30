---
title: Geometry Help and More!
author: Mimi
layout: post
dsq_thread_id:
  - 863167663
categories:
  - ICM
---
<p><script src="//ajax.googleapis.com/ajax/libs/jquery/1.8.0/jquery.min.js" type="text/javascript"></script><br />
<script type="application/javascript">
var apiKey = "c6af2d1bcf1086db7e38a6db5ab8df0d:8:56988301"; 
//var baseURL = "http://api.nytimes.com/svc/search/v2/article.jsonp";
var baseURL = "http://api.nytimes.com/svc/books/v2/lists/hardcover-fiction.jsonp";
var queryURL = baseURL + "?query=outer+space&#038;begin_date=19850101&#038;end_date=19860101&#038;api-key=" + apiKey;
$.getJSON(queryURL, function(data) {
  console.log(data);
});
</script></p>
<p><strong>Next Session: Thursday Oct 11th 6-7:30PM Room 15</strong></p>
<p>Are you waking up in the middle of the night wondering&#8230;</p>
<ol>
<li>How do I draw more awesome curves?</li>
<li>How do I make stuff that goes in a circle-like manner (e.g. sun rays)?</li>
<li>How do I create &#8220;Photoshop&#8221; effects (e.g. drop shadows)?</li>
<li>How do I create more interesting motion effects?</li>
<li>How do I make cool patterns?</li>
</ol>
<p>Come to the residents&#8217; workshop on Geometry Help and More!</p>
<p><script type="application/processing">
float anchor1X, anchor1Y, anchor2X, anchor2Y;
float control1X, control1Y, control2X, control2Y;
float t, factor;
void setup() {
  size(600, 400);

  anchor1X = width/2;
  anchor1Y = height/3;
  anchor2X = width/2;
  anchor2Y = height/3;

  control1X = width/2;
  control1Y = height/3;
  control2X = width/2;
  control2Y = height/3;

  factor = 1;
}

void draw() {
  background(255);
  t+=.01;
  //factor += cos(t)*.1;
  anchor1X += cos(t*2)*factor*.5;
  anchor1Y += sin(t*33)*factor*.2;
  anchor2X += cos(t*.33)*factor*.5;
  anchor2Y += sin(t*.5)*factor*.67;

  control1X += cos(t*.67)*factor*.33;
  control1Y += sin(t*.33)*factor*.2;
  control2X += cos(t*2)*factor*.2;
  control2Y += sin(t*.33)*factor*.5;

  noFill();
  stroke(0);
  strokeWeight(50);
  bezier(anchor1X, anchor1Y, control1X, control1Y, control2X, control2Y, anchor2X, anchor2Y);

  noStroke();
  fill(255, 0, 0);
  ellipse(anchor1X, anchor1Y, 10, 10);
  ellipse(anchor2X, anchor2Y, 10, 10);

  fill(0, 0, 255);
  ellipse(control1X, control1Y, 10, 10);
  ellipse(control2X, control2Y, 10, 10);

  stroke(200);
  strokeWeight(1);
  line(anchor1X, anchor1Y, control1X, control1Y);
  line(anchor2X, anchor2Y, control2X, control2Y);
}
</script></p>
<p>We&#8217;ll de-mystify some of Processing&#8217;s basic geometry functions to &#8220;do more with less code.&#8221;</p>
<p>We will begin with absolute basics and assume no prior knowledge of anything.</p>
<p>This session should be helpful for people working in JS too as we&#8217;ll cover concepts that translate easily to other languages.</p>
<p><strong>Monday Oct 8th 1-2PM Conference Room</strong></p>
