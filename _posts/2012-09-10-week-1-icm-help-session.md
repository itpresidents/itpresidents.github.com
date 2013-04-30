---
title: Week 1 ICM Help Session
author: Lia
layout: post
permalink: /week-1-icm-help-session/
dsq_thread_id:
  - 841725004
categories:
  - ICM
  - Tutorial
---
# 

**GENERAL REFERENCES **

[tutorial in processing.org][1]

 [1]: http://processing.org/learning/curves/

[ICM Git Repository][2] – Examples from Class and More! – Great place to get started with HWs. – Click the “ZIP” file to download the whole enchilada.

 [2]: https://github.com/ITPNYU/ICM/

[Processing Reference][3] – If you have a question that starts with, “How do I…?” check here first.

 [3]: http://processing.org/reference/

[Instructions for uploading your homework][4] to the web.

 [4]: http://itp.nyu.edu/varwiki/ClassWork/Homework-upload-instructions

**WHERE TO FIND CODE EXAMPLES WITHIN THE PROCESSING APP**

Go to the menu File>>Examples…>>Basics.

**DRAWING CURVES, ARCS**

There were A LOT of questions about drawing curves

[curves in processing.org][1] (arcs, splines, bezier)  
[drawing in processing][5] (coordinate system, simple shapes)  
[working with color][6]

 [5]: http://processing.org/learning/drawing/
 [6]: http://processing.org/learning/color/

[Anatomy of a Circle][7]

 [7]: http://www.khanacademy.org/math/geometry/circles-topic/v/circles--radius--diameter-and-circumference

[![][9]][9]

 []: http://itp.nyu.edu/residents/wp-content/uploads/2012/09/Screen-Shot-2012-09-10-at-4.56.31-PM1.png

*Radians and Degrees, scanned from [Getting Started With Processing][9] (Reas, Fry 2010)*

 [9]: http://shop.oreilly.com/product/0636920000570.do

The Unit Circle  
[![][11]][11]

 []: http://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Unit_circle_angles_color.svg/600px-Unit_circle_angles_color.svg.png

If you are more comfortable working with degrees, you can convert from Degrees to Radians with the[ radians()][11] function. So instead of saying

 [11]: http://processing.org/reference/radians_.html

**arc(50, 15, 80, 80, HALF_PI, PI);**

you might write:

arc(50, 75, 80, 80, **radians (90), radians (180)**);

and it would be the same thing.

UPDATE (9/18) Dan Shiffman posted an example with different usages of arc() [here][12].

 [12]: https://github.com/ITPNYU/ICM/blob/master/extras/arcs/arcs.pde

 

**PRINTING YOUR MOUSE COORDINATES TO THE CONSOLE**

Drawing in Processing can be tedious if you always have to estimate where your coordinates should be. Wouldn’t it be great if you could use the coordinates of your mouse position to tell you where you need to draw?

Type this within the DRAW loop:

[println][13] (“X: ” mouseX ” Y: ” mouseY);

 [13]: http://processing.org/reference/println_.html

now move your mouse pointer around the sketch and check your console for the coordinates!