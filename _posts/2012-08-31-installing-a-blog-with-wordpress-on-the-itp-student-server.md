---
title: Installing a Blog with WordPress on the ITP Student Server
author: Steve
layout: post
permalink: /installing-a-blog-with-wordpress-on-the-itp-student-server/
dsq_thread_id:
  - 841749288
categories:
  - Tutorial
  - Wordpress
---
# 

This article will show you how to install WordPress on the ITP Student server for all your documentations needs.

## Download The Programs

### FTP

We will be installing your blog on the ITP Student Server, which is a computer with no screen or keyboard that you can’t touch so we’ll need a program to access this computer and put your files on it.

To do this we’ll get **[Cyberduck][1]**, an FTP program. FTP is like HTTP but is for moving files only and not web pages.

 [1]: http://cyberduck.ch/

Download and install.

### WordPress

Next we need to download WordPress which is a program but works in a different way than `.app` and `.exe` files. There are hundreds of files ending in `.php` that together form the WordPress web application.

[Download WordPress by clicking here][2]. It doesn’t matter what operating system you use.

 [2]: http://wordpress.org/download/

Download the zip file and hold on to it for a later step.

### Suggested Text Editors

During setup we’ll need to edit a few files. Your computer already has a program to edit these files with, but there are better ones out there.

#### Free Text Editors

*   Mac: [TextWranger][3]
*   Windows: [Notepad ][4]

 [3]: http://www.barebones.com/products/TextWrangler/download.html
 [4]: http://notepad-plus-plus.org/download/v6.1.6.html

#### Paid (with free trial)

If you think you’ll be doing a lot of web programming I highly recommend getting [Sublime Text 2][5]. It costs money but comes with a free trial.

 [5]: http://www.sublimetext.com/2

## Connect to the ITP Student Server

Now we’re going to connect to the Student Server. Open Cyberduck and click the “Open Connection” button.

*   Select “SFTP” from the drop down menu.
*   Server: stu.itp.nyu.edu
*   Port: 22 (This should be set automatically when you select SFTP)
*   Username: your NYU netID
*   Password: your NYU netID password

Click connect.

## Uploading WordPress

You’ve downloaded WordPress as a .zip file. With Cyberduck we’ll need to unzip WordPress before we upload it.

### Preparing the files

Unzip `wordpress-3.4.1.zip` by double clicking on it.

Rename the folder to whatever you want your blog to be called. For instance, if you don’t rename the folder your blog will be:

        http://itp.nyu.edu/~sk3453/wordpress
    

I’m going to name my folder “blog.”

### The fun part

Now go back to Cyberduck and double click on `public_html`. Everything inside this folder can be accessed from a web browser. And that’s exactly what we want WordPress to be.

So now that the `public_html` folder is opened drag your WordPress files, folder and all, and drop it inside of Cyberduck.

A window will pop up and tell you how everything is transferring. While we wait for WordPress to upload, we need to get the password to your database.

## How WordPress Works

WordPress, and most other web applications, consist of 3 parts

*   The database. Databases are a little strange. You can think of them like huge spreadsheets with fancy search functions. Each row in the spreadsheet is a “post” or a “comment” an individual data point or **model** and the columns are the title of the post, the content of the post and everything else. When you view a blog post one a blog post **model** is retrieved from the database and displayed in the browser.
*   WordPress uses themes to display your blog posts. A theme is a set of files that correspond to the main page and individual blog posts and have variables where the **model** is inserted. In web app language a theme is referred to as the **view**. The final part of the application determines which **model** and which **view** to put together when you ask for a page.
*   The application files that contain the instructions for responding to browser requests and knowing when to put what where. This is called the **controller**.

That was a long winded way to say that there are a lot of different parts working together to make WordPress work. The takeaway here is that your blog posts live in the database, your theme lives in the `/wp-content/themes` folder and everything else you can leave alone.

## Configuring WordPress

In Cyberduck click the BACK button and look for a file called “sqlpw.” Right click on this file and download it. It’s a file that has plain text in it but your computer doesn’t know how to open it. Right click on the downloaded ‘sqlpw’ file and select OPEN WITH and choose a text editor (TextWrangler, Notepad , TextEdit, etc).

What you see is your password to log in to the database. Select it with your cursor and copy it (Mac: CMD C, Windows: CTRL C).

Now go to your blog, mine is here:

        http://itp.nyu.edu/~sk3453/blog
    

Substitute your netid and whatever you named your WordPress folder for ‘sk3453′ and ‘blog’ respectively.

Click “Create Configuration File”.

This screen tells you what you need to set up WordPress, we have it all. Click “Let’s Go.”

Set “Database name” to your netID.

Fill in this form using your netID as the username and paste the password in the password field (MAC: CMD P, Windows: CTRL P). Make sure there are no spaces at the end of your password.

You can leave everything else alone, you *must* leave ‘Database Host’ as ‘localhost’.

Now set your username and password and hit submit.