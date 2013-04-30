---
title: Putting Objects into Arrays
author: Steve
layout: post
categories:
  - ICM
---
<p>Here&#8217;s a small Processing sketch to exhibit working with arrays of Objects. I&#8217;ve split the sketch up in to 2 sections, &#8220;setting&#8221; a Point to each position in the array and then going through the array and getting the object out of the array.</p>
<p>If you have any questions, please put them in the comments and I&#8217;ll do my darnedest to answer.</p>
<script src="https://gist.github.com/3913991.js"></script><noscript><pre><code class="language-processing processing">class Point {
  int year;
  int population;
  float rateOfChange;
  
  
  Point(int _year, int _population){
    year = _year;
    population = _population;
  }
}

Point[] points;

void setup() {
  size(400,400);
  points = new Point[10];
  
  println(&quot;SET 'points'&quot;);
  
  for(int i=0; i &lt; points.length; i++) {
    int newYear = 1900 + i*5;
    int newPop = (int)random(30000);
    println(i + &quot; &quot; + newYear + &quot; &quot; + newPop);
    
    // Create a new Point instance and set its year and population
    Point newPoint = new Point(newYear, newPop);
    // Store newPoint into the points array.
    points[i] = newPoint;
  }
  
  println(&quot;GET from 'points'&quot;);
  
  for(int i = 0; i &lt; points.length; i++) {
    // Get the ith Point from the points array and store it as 'tempPoint'
    Point tempPoint = points[i];
    // Print out attributes of tempPoint
    println(i + &quot; &quot; + tempPoint.year + &quot; &quot; + tempPoint.population);
  }
}</code></pre></noscript>
