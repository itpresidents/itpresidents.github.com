---
title: Installing a Blog with WordPress on the ITP Student Server
author: Steve
layout: post
dsq_thread_id:
  - 841749288
categories:
  - Tutorial
  - Wordpress
---
<p>This article will show you how to install WordPress on the ITP Student server for all your documentations needs.</p>
<h2>Download The Programs</h2>
<h3>FTP</h3>
<p>We will be installing your blog on the ITP Student Server, which is a computer with no screen or keyboard that you can&#8217;t touch so we&#8217;ll need a program to access this computer and put your files on it.</p>
<p>To do this we&#8217;ll get <strong><a href="http://cyberduck.ch/">Cyberduck</a></strong>, an FTP program. FTP is like HTTP but is for moving files only and not web pages.</p>
<p>Download and install.</p>
<h3>WordPress</h3>
<p>Next we need to download WordPress which is a program but works in a different way than <code>.app</code> and <code>.exe</code> files. There are hundreds of files ending in <code>.php</code> that together form the WordPress web application.</p>
<p><a href="http://wordpress.org/download/">Download WordPress by clicking here</a>. It doesn&#8217;t matter what operating system you use.</p>
<p>Download the zip file and hold on to it for a later step.</p>
<h3>Suggested Text Editors</h3>
<p>During setup we&#8217;ll need to edit a few files. Your computer already has a program to edit these files with, but there are better ones out there.</p>
<h4>Free Text Editors</h4>
<ul>
<li>Mac: <a href="http://www.barebones.com/products/TextWrangler/download.html">TextWranger</a></li>
<li>Windows: <a href="http://notepad-plus-plus.org/download/v6.1.6.html">Notepad++</a></li>
</ul>
<h4>Paid (with free trial)</h4>
<p>If you think you&#8217;ll be doing a lot of web programming I highly recommend getting <a href="http://www.sublimetext.com/2">Sublime Text 2</a>. It costs money but comes with a free trial.</p>
<h2>Connect to the ITP Student Server</h2>
<p>Now we&#8217;re going to connect to the Student Server. Open Cyberduck and click the &#8220;Open Connection&#8221; button.</p>
<ul>
<li>Select &#8220;SFTP&#8221; from the drop down menu.</li>
<li>Server: stu.itp.nyu.edu</li>
<li>Port: 22 (This should be set automatically when you select SFTP)</li>
<li>Username: your NYU netID</li>
<li>Password: your NYU netID password</li>
</ul>
<p>Click connect.</p>
<h2>Uploading WordPress</h2>
<p>You&#8217;ve downloaded WordPress as a .zip file. With Cyberduck we&#8217;ll need to unzip WordPress before we upload it.</p>
<h3>Preparing the files</h3>
<p>Unzip <code>wordpress-3.4.1.zip</code> by double clicking on it.</p>
<p>Rename the folder to whatever you want your blog to be called. For instance, if you don&#8217;t rename the folder your blog will be:</p>
<pre><code>    http://itp.nyu.edu/~sk3453/wordpress
</code></pre>
<p>I&#8217;m going to name my folder &#8220;blog.&#8221;</p>
<h3>The fun part</h3>
<p>Now go back to Cyberduck and double click on <code>public_html</code>. Everything inside this folder can be accessed from a web browser. And that&#8217;s exactly what we want WordPress to be.</p>
<p>So now that the <code>public_html</code> folder is opened drag your WordPress files, folder and all, and drop it inside of Cyberduck.</p>
<p>A window will pop up and tell you how everything is transferring. While we wait for WordPress to upload, we need to get the password to your database.</p>
<h2>How WordPress Works</h2>
<p>WordPress, and most other web applications, consist of 3 parts</p>
<ul>
<li>The database. Databases are a little strange. You can think of them like huge spreadsheets with fancy search functions. Each row in the spreadsheet is a &#8220;post&#8221; or a &#8220;comment&#8221; an individual data point or <strong>model</strong> and the columns are the title of the post, the content of the post and everything else. When you view a blog post one a blog post <strong>model</strong> is retrieved from the database and displayed in the browser.</li>
<li>WordPress uses themes to display your blog posts. A theme is a set of files that correspond to the main page and individual blog posts and have variables where the <strong>model</strong> is inserted. In web app language a theme is referred to as the <strong>view</strong>. The final part of the application determines which <strong>model</strong> and which <strong>view</strong> to put together when you ask for a page.</li>
<li>The application files that contain the instructions for responding to browser requests and knowing when to put what where. This is called the <strong>controller</strong>.</li>
</ul>
<p>That was a long winded way to say that there are a lot of different parts working together to make WordPress work. The takeaway here is that your blog posts live in the database, your theme lives in the <code>/wp-content/themes</code> folder and everything else you can leave alone.</p>
<h2>Configuring WordPress</h2>
<p>In Cyberduck click the BACK button and look for a file called &#8220;sqlpw.&#8221; Right click on this file and download it. It&#8217;s a file that has plain text in it but your computer doesn&#8217;t know how to open it. Right click on the downloaded &#8216;sqlpw&#8217; file and select OPEN WITH and choose a text editor (TextWrangler, Notepad++, TextEdit, etc).</p>
<p>What you see is your password to log in to the database. Select it with your cursor and copy it (Mac: CMD+C, Windows: CTRL+C).</p>
<p>Now go to your blog, mine is here:</p>
<pre><code>    http://itp.nyu.edu/~sk3453/blog
</code></pre>
<p>Substitute your netid and whatever you named your WordPress folder for &#8216;sk3453&#8242; and &#8216;blog&#8217; respectively.</p>
<p>Click &#8220;Create Configuration File&#8221;.</p>
<p>This screen tells you what you need to set up WordPress, we have it all. Click &#8220;Let&#8217;s Go.&#8221;</p>
<p>Set &#8220;Database name&#8221; to your netID.</p>
<p>Fill in this form using your netID as the username and paste the password in the password field (MAC: CMD+P, Windows: CTRL+P). Make sure there are no spaces at the end of your password.</p>
<p>You can leave everything else alone, you <em>must</em> leave &#8216;Database Host&#8217; as &#8216;localhost&#8217;.</p>
<p>Now set your username and password and hit submit.</p>
