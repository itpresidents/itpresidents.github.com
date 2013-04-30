---
title: Introduction to Git and Github
author: Steve
layout: post
permalink: /introduction-to-git-and-github/
dsq_thread_id:
  - 853465536
categories:
  - Git
  - Tutorial
---
# 

*This post is a mirror of the original article on Steve’s blog, which is [here][1].*

 [1]: http://skli.se/2012/09/22/introduction-to-git/

This tutorial will teach you the basics of using Git and Github and is based on a workshop given on September 12th and 13th at ITP.

## Audience

This tutorial is intended for someone who has had at least a little exposure to programming and none to the command line. The goal is to give you, the reader, an introduction to Git and Github that will inform you both technically and conceptually as to what all of this is.

## Outline

*   What is Git?
*   What is Github?
*   Install Git
*   Learning to talk to your computer
*   Your first Git repository
*   Summary of Git workflow
*   Sign up for a Github Account
*   Pushing code from your computer and Github
*   References and further reading

## What is Git?

Git is a version tracking program used to track changes to files and folders. Git allows you to switch back to older versions of these files.

Each project you want to track with Git needs to be in its own folder on your computer. Git will monitor changes to all files within that folder. Each folder tracked by Git is referred to as a repository.

Git is really awesome and really, really powerful. I could go on for pages about all of the stuff Git can do. Instead, let’s dive right in and start using it

## What is Github?

Github is a website, a social website where instead of photos of partying with your friends you post files of code to program with your friends.

## Install Git

Git needs to be installed on your computer. You can download it from the [Git SCM][2] website.

 [2]: http://git-scm.com/download

### Mac

If you are on a Mac and have Xcode installed you should already have Git and can skip this step, but there’s no harm in re-installing.

Install the program from the package. When you get to the end of the installer you’ll notice your computer looks very similar to how it did when you started. There is no icon for Git in your Applications or Program Files folder. Don’t worry. Git gets installed in a different place and doesn’t have an icon to click on. Don’t worry about using Git yet, we’ll cover that later in the tutorial.

##### Attention Mountain Lion Users

Apple has decided to protect your computer making it harder for you to install Git.

To fix this, open up **System Preferences** and click on **Security & Privacy** (top row, third from the right).

Now click the padlock in the bottom left corner and enter the password for your computer and click the **Unlock** button.

Under “Allow applications downloaded from:” select “Anywhere” like so:

![][3]

 [3]: http://skli.se/images/posts/introduction-to-git/gatekeeper.png

Once you’ve done that you should be able to install Git.

### Windows

If you’ve got a Windows computer, download the setup exe file and use all the default settings.

When you get to the **Adjusting your PATH environment** screen, be sure to choose the option for **Use Git Bash Only**. Git Bash is a program that will be installed that lets you interact with Git and your computer in much the same way as the Terminal application on Apple computers.

You should have now have a program in your Start Menu called Git Bash. If you hit the Windows key to pull up the start menu and type “git bash” you should see the program highlighted. I’m going to explain a bit about what Git and Github are before we need to open the program.

## Learning to talk to your computer

Git is a program with out a graphical user interface. Git has no buttons, no icons. There are quite a few programs that give Git a graphical user interface, but we aren’t going to use those.

Why? Because I prefer the keyboard to the mouse/trackpad but also because the buttons and icons obscure what Git is doing and what you are telling Git to do. So we’re going to learn the hard way so that you learn more.

### No Buttons

Most of the programs you use have graphical user interfaces (GUIs), the Finder (Explorer on Windows), web browsers, word processors, etc. You click on a button and something happens.

Before GUIs there was the command line. No buttons, just text input. On the command line you have to type in what you want the computer to do and it responds. It is through this command line that we will interact with Git.

### Opening Terminal (or Git Bash)

To get to the command line on a Mac open up the application **Terminal**. The quickest way to open Terminal is to click the magnifying glass in the top right corner of your screen and type “terminal” and click the first result, looking something like this:

![][4]

 [4]: http://skli.se/images/posts/introduction-to-git/open-terminal.png

On Windows, we will use **Git Bash** which is a program that was installed with Git and emulates the same command line as on OS X. To open Git Bash, hit the Windows Key and type “git bash” you should see a program listed first with an orange icon, click that to open it. If you don’t see this program, reinstall [Git][5] and be sure to select the option to install Git Bash.

 [5]: http://git-scm.com/downloads

![][6]

 [6]: http://skli.se/images/posts/introduction-to-git/open-git-bash.png

For the rest of this tutorial I’m going to use “Terminal” to refer to both Terminal.app on Mac and Git Bash.exe on Windows.

### What is this Terminal?

You can think of the Terminal as an alternate view of the files and folders on your computer, instead of a Finder or Explorer window, it’s this black or white box with a cursor.

In the Finder each folder has a list or grid of the contents of the folder. In Terminal we have something called the **prompt**, it’s all that text to the left of the cursor.

Hit enter a few times and you’ll see the same thing repeated down the screen of the Terminal. That’s your prompt. Treat it like a good friend, get to know it.

Somewhere in your prompt you should see a tilde (`~`). In every Finder window you’re looking at a location on your computer. It could be your Downloads folder or your Pictures folder. This is the same in Terminal. The tilde is the folder you are currently in. Wait, you don’t have a folder named “~”? That’s because the tilde is a variable for `/Users/sklise` but instead of “sklise” it would be your username. On Windows the “~” stands for `/c/Users/sklise`. When you direct Terminal to a different folder the “~” will change to reflect the name of the folder you are in. This is the only visual clue as to where you are, so pay close attention to it.

### Seeing Files, Moving to Folders

Finally, some commands for Terminal.

Let’s see what the contents of `~` are. To do this we will use the command **`ls`**. Type the following in to Terminal and hit enter:

    $ ls 

(Whenever you see `$` at the beginning of a line of code, don’t type it, it’s there to say “This is something typed in to Terminal.”)

What just happened? Your computer gave you some output and then returned you to your prompt. Here’s what my output looked like, you’ll probably have less items listed than I do:

![][7]

 [7]: http://skli.se/images/posts/introduction-to-git/ls.png

The list you see is a list of the folders and files inside of `/Users/sklise`. Now I want to move to the Desktop, just because. In the Finder I’m able to just click on the word “Desktop” and there I am. In Terminal we have to type a command to get there.

The command to move to move to a folder is **`cd`**. CD stands for “change directory.” Directories and folders are the same thing. When we use the `cd` command we need to tell it what directory we want to change to.

Type the following into Terminal and hit enter:

    $ cd ~/Desktop 

Are you back at your prompt? Is anything different? You should see the `~` has been replaced with `Desktop`. That means we are now in the Desktop folder. If you type

    $ ls 

You’ll get a list of all the files and folders on your Desktop. This may be a lot of files or it may be nothing.

### Make a Folder, Make a File

Thus far we’ve only looked at things with the Terminal, we haven’t modified or created any thing. And by “thing” I mean folders or files on your computer.

For this tutorial we will work with a Processing sketch. If you don’t already have Processing installed, go [download it][8] now.

 [8]: http://processing.org

I want to make a Processing sketch called “radsketch.” Processing requires all sketch files to be inside of folders with the same name. So we will need a folder named “radsketch” and a file inside that folder called “radsketch.pde”. Let’s get started.

The command to make a folder is **`mkdir`**. This stands for “make directory,” programmers are lazy and don’t like to type unnecessary characters. Dropping vowels from words started way before the internet. We need to give the `mkdir` command the name of the directory (remember, folder and directory are the same thing) we want to make. Terminal doesn’t deal well with spaces, and in general having spaces in folder and file names will just slow you down. Anyways, Processing doesn’t let you have spaces in folder or sketch names. Let’s make our folder “radsketch”:

    $ mkdir radsketch 

It looks like nothing happened in the Terminal, you are right back at your prompt and nothing has changed. But if you look at your desktop you should find a folder named “radsketch”.

![][9]

 [9]: http://skli.se/images/posts/introduction-to-git/mkdir.png

Now to make the file “radsketch.pde”. For this we will use the **`touch`** command. Why’s it called touch? Because this command is used to update the timestamps on a file, if the file doesn’t exist, `touch` creates the file.

But first we want to be inside the “radsketch” folder. Do the following:

    $ cd ~/Desktop/radsketch 

Now we’ll use the touch command:

    $ touch radsketch.pde 

If you look in the radsketch folder on your desktop you’ll see a file you can open with Processing.

Leave the Terminal open and open radsketch.pde in Processing.

Our Processing sketch is not rad right now. Let’s make it rad. Open the file in Processing and write some code. This is what I’ll write:

    // radsketch.pde void setup() { size(200,200); background(255); smooth(); noStroke(); fill(255,0,0); ellipse(width/2, height/2, 50, 50); fill(255); triangle(width/2, height/2 - 25, width/2   cos(radians(210))*25, height/2 - sin(radians(210))*25, width/2   cos(radians(330))*25, height/2 - sin(radians(330))*25 ); } 

Kinda rad. It could be radder, but I don’t want to lose this state of the sketch. What should I do? Track the sketch with Git!

## Setting up Git

We need to take a quick detour and execute two commands before we use Git. These two commands you only need to do once, ever. Or until you get a new computer.

A note about the following commands, put your name and preferred email address inside the quote marks. These values will be stored with Git and with every project you work on with Git. So be sure that the email address you use is ok to be public.

    $ git config --global user.name "YOUR_FULL_NAME" $ git config --global user.email "YOUR_EMAIL_ADDRESS" 

What’s the deal with this? Why does Git need to know your name and email address? Git is used to track changes to files in a project, part of tracking changes is noting who made the changes.

## Your first Git repository

To start tracking a project with Git you need to tell Git to start doing so.

In the same Terminal window as we’ve been using, execute the following:

    $ git init 

You’ll get a one line response similar to the following

![][10]

 [10]: http://skli.se/images/posts/introduction-to-git/init.png

What just happened was Git created a folder inside the radsketch folder named “.git” which is hidden by the operating system. This folder is where Git stores all of the information needed to do what Git does. You’ll never have a reason to look at the contents of this folder.

### Status Updates

What does Git know about the radsketch folder and its contents, and how do we find out what Git knows?

    $ git status 

Returns:

![][11]

 [11]: http://skli.se/images/posts/introduction-to-git/untracked.png

This is a really awesome message. Git is telling us that it sees one file in the folder that it is not tracking. This means Git doesn’t care about any changes to this file right now. And we are told to use `git add` to track the file.

Git is great at giving descriptive messages. **So read the messages Git gives you.**

Really, if you don’t read what Git spits out you won’t know what you’ve done or if it worked properly.

Seriously. **READ THE MESSAGES THE COMPUTER GIVES YOU WHEN YOU EXECUTE A COMMAND.**

### Staging

Git uses a concept called a “staging area.” This is a liminal “space” between changes to files and a commit. It’s the prep area. You earmark the state of a file to be included in a commit and then you commit it.

This two step process will make more sense when you are dealing with a project with many files, right now it’s sufficient to tell you this is how it works and you have to do it this way.

Files are added to Git by typing `git add` and then the name of the file:

    $ git add radsketch.pde 

If you execute that command it looks like nothing happened—there’s no response. It’s time to run `git status` again.

    $ git status 

![][12]

 [12]: http://skli.se/images/posts/introduction-to-git/staged.png

The status message has changed and we see that radsketch.pde is marked as a “new file” and under the heading “Changes to be committed.” So let’s make a commit already.

### Always Leave A Message

When making a commit with Git you are required to leave a message. When working with others on a project it’s important to leave messages about what the changes were that you made to the code. Otherwise everyone on your team would have to read through your code and figure out what you were doing or you could just tell them “Made the circle green” and they can get back to work.

Also, as your projects grow in scale you’ll have a lot of commits and maybe take a few months off from working on a project. When you return to work on a project, say after summer vacation, you’ll probably have forgotten what you had been doing. Now, I’m not saying I did that with my thesis, but here is a section of commit messages from my thesis:

![][13]

 [13]: http://skli.se/images/posts/introduction-to-git/leave-a-message.png

You can see some descriptive messages but then also a string of 4 commits where the error message is “debugging.” To figure out what the heck I was doing then I’ll have to back and look at the commits in detail, much more tedious than if I had left myself a good message.

This is not a contrived example and no, I didn’t make those 4 “debugging” commits 6 months ago just for use in this blog post.

So, please, leave good messages. You’ll thank yourself later.

### Committing

Now, where were we. Make a commit. Ok. The command to make a commit is `git commit -m`. The `-m` is to leave a message. Always leave a message.

    $ git commit -m "Created a triangle in a circle" 

![][14]

 [14]: http://skli.se/images/posts/introduction-to-git/first-commit.png

We’ve made our first commit. Let’s do `git status` again and see what’s going on.

    $ git status 

![][15]

 [15]: http://skli.se/images/posts/introduction-to-git/post-commit-status.png

Git doesn’t see any changes to the files since the last commit. Let’s make some changes and see what `git status` says after that.

    // radsketch.pde void setup() { size(200,200); background(255); smooth(); noStroke(); fill(0,255,0); rect(width/2 - 25, height/2 - 25, 50, 50); fill(255,0,0); ellipse(width/2, height/2, 50, 50); fill(255); triangle(width/2, height/2 - 25, width/2   cos(radians(210))*25, height/2 - sin(radians(210))*25, width/2   cos(radians(330))*25, height/2 - sin(radians(330))*25 ); } 

Now save those changes and execute:

    $ git status 

![][16]

 [16]: http://skli.se/images/posts/introduction-to-git/modified.png

Geez, Git is great. It knows that we changed the file and it even tells us what we could do next. We’re going to do `git add` but before that let’s dig a bit deeper in to what is happening.

    $ git diff 

![][17]

 [17]: http://skli.se/images/posts/introduction-to-git/diff.png

Git doesn’t just know that the file has changed, Git knows which lines have changed and more specifically that they are additions. When we add radsketch.pde and commit it Git will only store the contents of the change, which means that you aren’t wasting space making copies of everything that didn’t change which is what would happen if you copied the whole folder and renamed it “radsketch_v2″.

So let’s add radsketch.pde and make a commit

    $ git add radsketch.pde $ git commit -m "Added a rectangle behind the other shapes" 

![][18]

 [18]: http://skli.se/images/posts/introduction-to-git/second-commit.png

That in a nutshell is how Git works on your computer. Everything we’ve done has been on our own computer. At no point did we reach out to the internet or use Github in anyway. That’s next.

Leave Terminal open, we’ll be returning to it soon.

## Sign up for a Github Account

[Click here][19] to sign up for a free Github account.

 [19]: https://github.com/signup/free

### Github is a Website

Github is a website. Git is program on your computer. They may sound the same but they are distinct and separate.

Say it with me, Github is a website and Git is a program on your computer.

It’s not quite that simple though. Github is a website made of many servers some of which run Git. But the key thing to realize is that Github is not on your computer. We’ll be going over 2 Git commands that let your computer talk to Github’s servers.

## Get Your Code on Github

We need to make a “new repository” on Github in order to send our Processing sketch to their servers.

Click the button in the top right of the screen, third icon from the left that says “Create a New Repo” when you hover over it.

![][20]

 [20]: http://skli.se/images/posts/introduction-to-git/new-repo-button.png

### We already have a repository, why are we making a new one?

Github is a website and websites get their information from a database. So when we click “Create a New Repo” what we are doing is creating a new database entry on Github for this “repo.” One field in that entry is the location of the actual Git repository. In this case “Repository” refers both to the database entry and the actual Git repository.

### Filling out this form

Here’s how I filled out this form

![][21]

 [21]: http://skli.se/images/posts/introduction-to-git/new-repo-form.png

Notes on this form:

*   The “Repository name” does not need to match the name of the folder on your computer.
*   Description is of course optional.
*   Private repos on Github cost money. But if you’re a student you can [request a free micro plan][22].
*   Don’t check the “Initialize this repository with a README.” Readmes are important and useful but for right now this will throw a wrench in the tutorial.

 [22]: https://github.com/edu

Click “Create repository.”

### Telling Git about Github

The page we are brought to has instructions for telling Git (on your computer) about this new Github repository we’ve created. Scroll down to “Push an existing repository from the command line” because we’ve made a repository on our computer already and we haven’t done this before.

![][23]

 [23]: http://skli.se/images/posts/introduction-to-git/add-remote-instructions.png

There are two lines there for us to copy and paste in to the Terminal.

Let’s copy and paste the first line in Terminal and then talk about it. My line is different than yours because yours will have *your* Github username in it.

![][24]

 [24]: http://skli.se/images/posts/introduction-to-git/git-remote-add.png

We are adding a **remote** to this Git repository. A remote is another computer that we want to share our repository with. Remotes are URLs. But those URLs are long so we can give the remote a name, in our case **origin**, so we don’t have to type the entire URL over and over.

At this point Git has *still* not connected to Github, we’ve merely told it the URL to connect to.

### A Push or a Shove

At this point in the talk, hand motions were used. You’ll need to imagine them, or mime along with the reading.

We’ve told Git about Github, now we want to show Github what we’ve got. Let’s copy and paste the second line of the instructions into Terminal and hit enter.

    $ git push -u origin master 

You’ll be prompted for your Github username, type it in and hit enter. Then you’ll be prompted for you Github password. Type it in. **The cursor will not move, you won’t see any visual indication of your typing**. This is a security measure, if you mess up your password just hit DELETE…maybe 30 times, 40 for safe measure. Hit enter, you’ll get a response similar to but not identical to the following screenshot

![][25]

 [25]: http://skli.se/images/posts/introduction-to-git/first-push.png

Go back to your browser and refresh the page.

![][26]

 [26]: http://skli.se/images/posts/introduction-to-git/post-push.png

You’ll see radsketch.pde on the page, if you click it, there’s the contents of the file. Awesome.

This is the end of this blog post. I haven’t even touched on the most amazing parts of either Git or Github. That’s coming in the next blog post.

For now, repeat this process with your own homework assignments. Only through repeated practice will you get better.

## References & Further Reading

*   [What is Version Control][27]
*   [Git Basics][28]
*   [Github’s help pages][29]
*   [Pro Git Book][30]

 [27]: http://git-scm.com/book/en/Getting-Started-About-Version-Control
 [28]: http://git-scm.com/book/en/Getting-Started-Git-Basics
 [29]: http://help.github.com
 [30]: http://git-scm.com/book/

## Did I make a mistake?

If you find something wrong or missing or unclear, please let me know by opening an [issue][31] on Github.

 [31]: https://github.com/stevenklise/stevenklise.github.com/issues