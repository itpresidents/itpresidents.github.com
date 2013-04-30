---
title: Intro to OF
author: Lia
layout: post
dsq_thread_id:
  - 1059899203
categories:
  - Uncategorized
---
#

Hi all,
[Here is the example ][1]we looked at with a vector of bouncing ball objects.
To try it out, download and unzip the repo.  Then, move the “ball\_bounce\_demo” folder into your Openframeworks “myApps” folder and open the xcode project file( ball\_bounce\_demo.xcodeproj).

 [1]: https://github.com/itpresidents/oF_bouncing_ball_objects_with_vectors

Here’s the presentation that we used to guide us through the workshop.
If you need more help, please don’t hesitate to come for office hours with Lia, Genevieve, Nick or Merche!



———–
addendum (Lia):
There was a question about when to use or not use the “new” operator when creating new objects in C . I didn’t answer it very well (and probably still won’t), but it has to do with memory management. In Processing, we make a new object like so, where we always use the “new” operator:

`myClass x = new myClass();`

in C , there are two ways to make a new class, and which way you choose depends on if you want to allocate memory from the heap or the stack.

`    // on the stack
    myClass x;
    // or on the heap ... see the pointer??
    myClass *x = new myClass;`

If you’re using the stack (no pointer), you access member variables and functions like so:

`x.myVariable; `

if you’re using the heap (pointer), you would use this:
`x->myVariable; `

We don’t want to get too much into it at this point, but if you want to read more about Heaps and Stacks, [try this link. ][2]. Here is Jeff Crouse’s tutorial on [C constructors][3]. **tldr**: unless your object is large, or you need to use it beyond local scope, use the stack (no pointers) way.

 [2]: http://www.learncpp.com/cpp-tutorial/79-the-stack-and-the-heap/
 [3]: http://www.jeffcrouse.info/teaching/cpp-constructors.html