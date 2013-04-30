---
title: Prototyping Javascript Sites on Your Computer
author: Steve
layout: post
dsq_thread_id:
  - 1015197300
categories:
  - Tutorial
  - Web
---
<p>Testing out Javascript in the developer console or with JSFiddle is easy. However, when you want to create your own files and work from your favorite text editor things can get a bit trickier.</p>
<p>If you open an HTML file with a web browser from your computer, you&#8217;ll notice that the URL starts with &#8220;file://&#8221;. Every web page you go to has a URL that starts with &#8220;http://&#8221;. This indicates the protocol that your web browser is trying to open the file with. When the protocol is &#8220;file&#8221; sometimes Javascript won&#8217;t work properly. Luckily, on a Mac, it&#8217;s easy to get around this.</p>
<ol>
<li>Open the Terminal program</li>
<li>Now, point Terminal to the folder where your files are.<br />
Type &#8220;cd &#8221; (don&#8217;t forget that space). And then drag the folder containing index.html and your Javascript files in to Terminal.<br />
Hit enter.</li>
<li>Now, type the following `python -m SimpleHTTPServer` and hit enter.</li>
<li>Go to http://localhost:8000 and find your index.html file.</li>
<li>To quit the server, type CTRL+C</li>
</ol>
