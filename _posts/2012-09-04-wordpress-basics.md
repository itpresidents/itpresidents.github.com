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
<p>Now that you have your WordPress Blog set up, <a href="http://itp.nyu.edu/residents/installing-a-blog-with-wordpress-on-the-itp-student-server/">thanks to Steve&#8217;s tutorial</a>, let&#8217;s make a simple blog post with some text, a photo and a couple of videos. <a href="http://itp.nyu.edu/residents/photo-and-video-3/">A finished example looks like this</a>.</p>
<p>First, if you&#8217;re not logged into your blog, go to:</p>
<p>http://itp.nyu.edu/~<strong>YourNetID/YourBlog</strong>/wp-admin/</p>
<p>Replace YourNetID with your NetID and YourBlog with the name of the directory you installed WordPress on.</p>
<p>Then login with your username and password.</p>
<p><!--more--></p>
<p><a href="http://www.flickr.com/photos/31090466@N08/7932029884/"><img src="http://farm9.staticflickr.com/8298/7932029884_ecd49f19c6_z.jpg" alt="WPLogin" width="526" height="628" /></a></p>
<p>Next, you&#8217;ll see the WordPress dashboard. We&#8217;re going to create a new post by hovering over Posts in the left hand menu, and selecting &#8220;Add New&#8221; from the list of selections.</p>
<p><a href="http://www.flickr.com/photos/31090466@N08/7932048010/"><img src="http://farm9.staticflickr.com/8178/7932048010_5de62b1e8a_n.jpg" alt="DashboardWelcomeAddNew" width="260" height="320" /></a></p>
<p>In this window, we&#8217;re able to give a title to our blog post and to write the text in the main textbox. Try it out.</p>
<p><strong>Uploading Media</strong></p>
<p>We can also add photos and other media by selecting the Upload/Insert button on the upper left side of your textbox.</p>
<p><a href="http://www.flickr.com/photos/31090466@N08/7932146302/"><img src="http://farm9.staticflickr.com/8307/7932146302_83266cbfa2_n.jpg" alt="AddMedia" width="320" height="251" /></a></p>
<p>In order to upload a photo from our computer into our blog post, first either drag and drop the image into the appropriate box or browse to it from WordPress. Then wait for the file to load, scroll down and then select &#8220;insert into post&#8221; at the bottom.</p>
<p><a href="http://www.flickr.com/photos/31090466@N08/7932209366/"><img src="http://farm9.staticflickr.com/8317/7932209366_ba99f5b476_n.jpg" alt="InsertingImage2" width="320" height="309" /></a></p>
<p><strong>Embedding Media</strong></p>
<p>To embed a video from Vimeo or Youtube in WordPress version 2.9 and above, you can simply paste the URL of the video and WordPress will recognize it as an embeddable object. This doesn&#8217;t work with every site &#8211; wordpress has whitelisted certain commonly used services. You can read more about how to <a href="http://codex.wordpress.org/Embeds">embed videos and images into wordpress here</a>.</p>
<p><a href="http://www.flickr.com/photos/31090466@N08/7932243572/"><img src="http://farm9.staticflickr.com/8321/7932243572_0d27faa82d_n.jpg" alt="AlsoYoutube" width="320" height="216" /></a></p>
<p>One common problem with embedding videos happens when the URL gets surrounded by html tags. For example, maybe I want to make my entire post center-aligned. I can do this by selecting all, and then pressing the center-align button. If you do this through WordPress&#8217;s default visual text editor, it will mess up the video embeds and show the URL as a text rather than an embedded video. But if we surround the video URLs <a href="http://codex.wordpress.org/Embeds">with the embed shortcode</a>, then it should work all right. First we need to access the HTML view (upper right corner of the main textbox). Then surround the URL with the embed shortcodes, as shown below:</p>
<p><a href="http://www.flickr.com/photos/31090466@N08/7932326502/"><img src="http://farm9.staticflickr.com/8038/7932326502_3955cdeb9d_n.jpg" alt="Shortcodes" width="320" height="242" /></a></p>
<p>And your embeds should work like before. If you&#8217;re getting confused about HTML tags, I suggest going over <a href="http://www.w3schools.com/html/default.asp">the basics of HTML here</a>.</p>
<p>What I like about embedding media outside of WordPress is it&#8217;s easy to access the media and post it elsewhere. For example, you too can make the exact blog post that I made just by copying the code below and pasting it into a new post with html view:</p>
<script src="https://gist.github.com/3625400.js"></script><noscript><pre><code class="language- ">&lt;p style=&quot;text-align: center;&quot;&gt;
  Hey Check out this photo:
&lt;/p&gt;

&lt;p style=&quot;text-align: center;&quot;&gt;
  [embed]http://www.flickr.com/photos/31090466@N08/7897383054/[/embed]
&lt;/p&gt;

&lt;p style=&quot;text-align: center;&quot;&gt;
  Then check out this video:
&lt;/p&gt;

&lt;p style=&quot;text-align: center;&quot;&gt;
  [embed]http://vimeo.com/47875656[/embed]
&lt;/p&gt;

&lt;p style=&quot;text-align: center;&quot;&gt;
  And this one:
&lt;/p&gt;

&lt;p style=&quot;text-align: center;&quot;&gt;
  [embed]http://www.youtube.com/watch?v=NRDXohpWAIo[/embed]
&lt;/p&gt;</code></pre></noscript>
<p>And if you&#8217;re wondering how I got that gist in there, well, you&#8217;ll have to check out my next tutorial on how to install wordpress plugins.</p>
