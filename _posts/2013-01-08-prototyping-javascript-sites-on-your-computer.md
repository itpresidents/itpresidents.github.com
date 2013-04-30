---
title: Prototyping Javascript Sites on Your Computer
author: Steve
layout: post
permalink: /prototyping-javascript-sites-on-your-computer/
dsq_thread_id:
  - 1015197300
categories:
  - Tutorial
  - Web
---
# 

Testing out Javascript in the developer console or with JSFiddle is easy. However, when you want to create your own files and work from your favorite text editor things can get a bit trickier.

If you open an HTML file with a web browser from your computer, you’ll notice that the URL starts with “file://”. Every web page you go to has a URL that starts with “http://”. This indicates the protocol that your web browser is trying to open the file with. When the protocol is “file” sometimes Javascript won’t work properly. Luckily, on a Mac, it’s easy to get around this.

1.  Open the Terminal program
2.  Now, point Terminal to the folder where your files are.  
    Type “cd ” (don’t forget that space). And then drag the folder containing index.html and your Javascript files in to Terminal.  
    Hit enter.
3.  Now, type the following \`python -m SimpleHTTPServer\` and hit enter.
4.  Go to http://localhost:8000 and find your index.html file.
5.  To quit the server, type CTRL C