---
title: Recursions
author: Antonius
layout: post
dsq_thread_id:
  - 869921279
categories:
  - ICM
  - Uncategorized
---
<p>A student asked me how to do recursions (on the first week of ICM!!).</p>
<p>I asked her to go through the first 3 Processing tutorials, make something more simple, and taught her some cool tricks. I forget just how ambitious ITP students can get. But then I kind of went on a tangent and instead of writing the Processing JS tutorial I promised, I made this sketch. It&#8217;s a good test to see how well the ProcessingJS plugin works, I guess. If you don&#8217;t see anything, even after a couple page refreshes, let me know.</p>
<p><script type="application/processing">
//Info: http://processingjs.org/reference
// Antonius Wiriadjaja http://antoni.us
// Made following Dan Shiffman's in-class demo, for Nature of Code
// Simple Recursion

String title = "Recursion Squares Demo";

// play button
Transport transport;

void setup() {
  size(640, 480);
  smooth();
  
  // play button
  transport = new Transport(title);
}

void app() {
  background(0);
  rectMode(CENTER);
  float angle = map(mouseX,0,width,-360,360*2);  
  pushMatrix();
  translate(width/2, height/2);
  rotate(radians(angle));
  float s = map(angle,-360,360*2,1.,10.);
  scale(s);
  drawSquare(0, 0, 300);
  popMatrix();
  
  transport.checkPaused();
}

void drawSquare(float x, float y, float diam) {
  noFill();
  stroke(255);
  rect(x, y, diam, diam);

  if (diam>8) { // exit condition
    drawSquare(x+diam*.5, y, diam*0.5);
        drawSquare(x-diam*.5, y, diam*0.5);
//    drawSquare(x, y+diam*.5, diam*0.5);
                drawSquare(x, y-diam*.5, diam*0.5);
  }
}

void draw() {
  if (transport.transportStop) {
    transport.stopDisplay();
  } 
  else if(transport.play) {
    app();
  }
  else if(transport.pause){
    transport.pauseDisplay();
  }
}

// Transport Controls class
class Transport {
  String t;
  PFont myFont = createFont("FFScala", 32);
  PFont stopFont = createFont("FFScala", 10);

  boolean clicked = false;
  boolean play = false;
  boolean pause = false;
  boolean transportStop = true;

  Transport(String _t) {
    t = _t;
  }

  void stopDisplay() {
    background(0);

    noStroke();

    fill(255);  
    textFont(myFont);
    text(t, width/20, height/10);
    //ellipse

    pushMatrix();
    translate(width/2, height/2);
    fill(200);
    ellipseMode(CENTER);
    ellipse(0, 0, width/2.5, width/2.5);

    fill(180);
    ellipseMode(CENTER);
    ellipse(0, 0, width/2.8, width/2.8);

    popMatrix();

    //triangle
    pushMatrix();
    translate(width/2+(width/28), height/2);
    if (intersects()) {
      fill(100);
    } 
    else {
      fill(150);
    }
    beginShape(TRIANGLES);
    vertex(-width/7, -height/7);
    vertex(-width/7, height/7);
    vertex(width/8, 0);
    endShape();
    popMatrix();
    if (mousePressed && intersects()) {
      transportStop=false;
      play=true;
      pause=false;
      background(0);
    }
  }
  
  void checkPaused(){
    
    rectMode(CORNER);
    noStroke();
    fill(255);
    rect(0,height-(height/8), height/8,height/8);
    
    textFont(stopFont);
    fill(0);
    text("STOP",(width/32),height-(height/16));

      if (mousePressed && intersectsPaused()) {
      transport.transportStop=true;
      transport.play=false;
      transport.pause=false;
      background(0);
    }
  }

  boolean intersects() {
    float distance = dist(mouseX, mouseY, width/2, height/2);
    if (distance<((width/2.5)/2)) {
      return true;
    } 
    else {
      return false;
    }
  }
  
    boolean intersectsPaused() {
    float distance = dist(mouseX, mouseY, 0, height);
    if (distance<((width/4.5)/2)) {
      return true;
    } 
    else {
      return false;
    }
  }
  
    void pauseDisplay() {

    noStroke();

    fill(255);  
    text(t, width/20, height/10);
    //ellipse

    pushMatrix();
    translate(width/2, height/2);
    fill(200);
    ellipseMode(CENTER);
    ellipse(0, 0, width/2.5, width/2.5);

    fill(180);
    ellipseMode(CENTER);
    ellipse(0, 0, width/2.8, width/2.8);

    popMatrix();

    //triangle
    pushMatrix();
    translate(width/2+(width/28), height/2);
    if (intersects()) {
      fill(100);
    } 
    else {
      fill(150);
    }
    beginShape(TRIANGLES);
    vertex(-width/7, -height/7);
    vertex(-width/7, height/7);
    vertex(width/8, 0);
    endShape();
    popMatrix();
    if (mousePressed && intersects()) {
      transportStop=false;
      play=true;
      pause=false;
      background(0);
    }
  }
}
</script></p>
