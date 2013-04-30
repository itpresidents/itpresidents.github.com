---
title: WordPress Basics
author: Antonius
layout: post
dsq_thread_id:
  - 845365692
categories:
  - Tutorial
  - Wordpress
---
#

Now that you have your WordPress Blog set up, [thanks to Steve’s tutorial][1], let’s make a simple blog post with some text, a photo and a couple of videos. [A finished example looks like this][2].

 [1]: http://itp.nyu.edu/residents/installing-a-blog-with-wordpress-on-the-itp-student-server/
 [2]: http://itp.nyu.edu/residents/photo-and-video-3/

First, if you’re not logged into your blog, go to:

http://itp.nyu.edu/~**YourNetID/YourBlog**/wp-admin/

Replace YourNetID with your NetID and YourBlog with the name of the directory you installed WordPress on.

Then login with your username and password.



[![WPLogin][4]][4]

 []: http://www.flickr.com/photos/31090466@N08/7932029884/

Next, you’ll see the WordPress dashboard. We’re going to create a new post by hovering over Posts in the left hand menu, and selecting “Add New” from the list of selections.

[![DashboardWelcomeAddNew][5]][5]

 []: http://www.flickr.com/photos/31090466@N08/7932048010/

In this window, we’re able to give a title to our blog post and to write the text in the main textbox. Try it out.

**Uploading Media**

We can also add photos and other media by selecting the Upload/Insert button on the upper left side of your textbox.

[![AddMedia][6]][6]

 []: http://www.flickr.com/photos/31090466@N08/7932146302/

In order to upload a photo from our computer into our blog post, first either drag and drop the image into the appropriate box or browse to it from WordPress. Then wait for the file to load, scroll down and then select “insert into post” at the bottom.

[![InsertingImage2][7]][7]

 []: http://www.flickr.com/photos/31090466@N08/7932209366/

**Embedding Media**

To embed a video from Vimeo or Youtube in WordPress version 2.9 and above, you can simply paste the URL of the video and WordPress will recognize it as an embeddable object. This doesn’t work with every site – wordpress has whitelisted certain commonly used services. You can read more about how to [embed videos and images into wordpress here][7].

 [7]: http://codex.wordpress.org/Embeds

[![AlsoYoutube][9]][9]

 []: http://www.flickr.com/photos/31090466@N08/7932243572/

One common problem with embedding videos happens when the URL gets surrounded by html tags. For example, maybe I want to make my entire post center-aligned. I can do this by selecting all, and then pressing the center-align button. If you do this through WordPress’s default visual text editor, it will mess up the video embeds and show the URL as a text rather than an embedded video. But if we surround the video URLs [with the embed shortcode][7], then it should work all right. First we need to access the HTML view (upper right corner of the main textbox). Then surround the URL with the embed shortcodes, as shown below:

[![Shortcodes][10]][10]

 []: http://www.flickr.com/photos/31090466@N08/7932326502/

And your embeds should work like before. If you’re getting confused about HTML tags, I suggest going over [the basics of HTML here][10].

 [10]: http://www.w3schools.com/html/default.asp

What I like about embedding media outside of WordPress is it’s easy to access the media and post it elsewhere. For example, you too can make the exact blog post that I made just by copying the code below and pasting it into a new post with html view:


      Hey Check out this photo:



      [embed]http://www.flickr.com/photos/31090466@N08/7897383054/[/embed]



      Then check out this video:



      [embed]http://vimeo.com/47875656[/embed]



      And this one:



      [embed]http://www.youtube.com/watch?v=NRDXohpWAIo[/embed]


And if you’re wondering how I got that gist in there, well, you’ll have to check out my next tutorial on how to install wordpress plugins.