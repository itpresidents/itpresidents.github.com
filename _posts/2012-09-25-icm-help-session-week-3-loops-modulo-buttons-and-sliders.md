---
title: 'ICM Help Session Week 3: Loops, Modulo, Buttons and Sliders'
author: Mimi
layout: post
permalink: /icm-help-session-week-3-loops-modulo-buttons-and-sliders/
dsq_thread_id:
  - 858192652
categories:
  - ICM
  - Tutorial
---
# 

# [Code Examples Here][1]

 [1]: https://github.com/itpresidents/ICM-Help-Sessions/tree/master/ICM_Help_Session_Week_3

# How to make a Slider | [Code][2]

 [2]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_Slider/ICM_Help_Week3_Slider.pde

This is a great example for understanding the following Processing functions:  
****

1.  **[constrain()][3]** – How to make the slider button not fall off the ends of the slider.
2.  Using variables to keep a bunch of shapes together relative to the mouse. (Our slider button is a complex shape comprising of 2 circles and 2 lines, all moving together relative to the y-location of the slider bar and the x-location of the mouse.)

 [3]: http://processing.org/reference/constrain_.html

# Using Loops to Generate Patterns | [Code][4]

 [4]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_LoopsAsPatterns/ICM_Help_Week3_LoopsAsPatterns.pde

1.  **[% modulo][5] **- Use division to create “regular” patterns, e.g. alternating rectangles by only filling a rectangle with “black” if the index number of the rectangle (in the loop) can be divided by 2 without a remainder. (e.g. 0, 2, 4, 6, 8, 10, 12, etc…)

 [5]: http://processing.org/reference/modulo.html

# Interactive Buttons | [Code][6]

 [6]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_Buttons/ICM_Help_Week3_Buttons.pde

We went over this example which shows 4 different kinds of interactive buttons working side by side.

1.  Momentary click
2.  Turning a button ON and OFF
3.  Mouseover or Hover effect
4.  Momentary click plus Mouseover or Hover effect

Concepts convered include:

1.  Using **booleans** to keep track of on/off states
2.  What’s the difference between [mousePressed][7] and [mousePressed()][8]?

 [7]: http://processing.org/reference/mousePressed.html
 [8]: http://processing.org/reference/mousePressed_.html

**[mousePressed][7]** is a Processing variable like mouseX that tells you if the mouse button is pressed down.

**[mousePressed()][8]** is a function that runs code  you write **ONE TIME** when you click the mouse.

[This sketch illustrates it. ][9]

 [9]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_2/ICM_Help_Session_Week_2_events/ICM_Help_Session_Week_2_events.pde

So then can you guess what’s the difference between keyPressed and keyPressed()?

# Teaser For Next Week

How do you create a grid of on/off switches?  
[Approach 1][10]  
[Approach 2][11] (with hover state)  
[Approach 3][12] (randomly placed cells with drawing via objects)

 [10]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_ToggleGrid_Alt/ICM_Help_Week3_ToggleGrid_Alt.pde
 [11]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_ToggleGrid/ICM_Help_Week3_ToggleGrid.pde
 [12]: https://github.com/itpresidents/ICM-Help-Sessions/blob/master/ICM_Help_Session_Week_3/ICM_Help_Week3_ToggleRandomWithLines_pde/ICM_Help_Week3_ToggleRandomWithLines_pde.pde

[![][14]][14]

 []: http://itp.nyu.edu/residents/wp-content/uploads/2012/09/photo1.jpg