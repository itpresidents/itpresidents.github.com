---
title: Introduction to Git and Github
author: Steve
layout: post
dsq_thread_id:
  - 853465536
categories:
  - Git
  - Tutorial
---
<p><script type="text/javascript" src="//speakerdeck.com/assets/embed.js" data-id="50535db817bbf5000206d2db" data-ratio="1.6"></script></p>
<p><em>This post is a mirror of the original article on Steve&#8217;s blog, which is <a href="http://skli.se/2012/09/22/introduction-to-git/" target="_blank">here</a>.</em></p>
<p>This tutorial will teach you the basics of using Git and Github and is based on a workshop given on September 12th and 13th at ITP.</p>
<h2>Audience</h2>
<p>This tutorial is intended for someone who has had at least a little exposure to programming and none to the command line. The goal is to give you, the reader, an introduction to Git and Github that will inform you both technically and conceptually as to what all of this is.</p>
<h2>Outline</h2>
<ul>
<li>What is Git?</li>
<li>What is Github?</li>
<li>Install Git</li>
<li>Learning to talk to your computer</li>
<li>Your first Git repository</li>
<li>Summary of Git workflow</li>
<li>Sign up for a Github Account</li>
<li>Pushing code from your computer and Github</li>
<li>References and further reading</li>
</ul>
<h2>What is Git?</h2>
<p>Git is a version tracking program used to track changes to files and folders. Git allows you to switch back to older versions of these files.</p>
<p>Each project you want to track with Git needs to be in its own folder on your computer. Git will monitor changes to all files within that folder. Each folder tracked by Git is referred to as a repository.</p>
<p>Git is really awesome and really, really powerful. I could go on for pages about all of the stuff Git can do. Instead, let&#8217;s dive right in and start using it</p>
<h2>What is Github?</h2>
<p>Github is a website, a social website where instead of photos of partying with your friends you post files of code to program with your friends.</p>
<h2>Install Git</h2>
<p>Git needs to be installed on your computer. You can download it from the <a href="http://git-scm.com/download">Git SCM</a> website.</p>
<h3>Mac</h3>
<p>If you are on a Mac and have Xcode installed you should already have Git and can skip this step, but there&#8217;s no harm in re-installing.</p>
<p>Install the program from the package. When you get to the end of the installer you&#8217;ll notice your computer looks very similar to how it did when you started. There is no icon for Git in your Applications or Program Files folder. Don&#8217;t worry. Git gets installed in a different place and doesn&#8217;t have an icon to click on. Don&#8217;t worry about using Git yet, we&#8217;ll cover that later in the tutorial.</p>
<h5>Attention Mountain Lion Users</h5>
<p>Apple has decided to protect your computer making it harder for you to install Git.</p>
<p>To fix this, open up <strong>System Preferences</strong> and click on <strong>Security &amp; Privacy</strong> (top row, third from the right).</p>
<p>Now click the padlock in the bottom left corner and enter the password for your computer and click the <strong>Unlock</strong> button.</p>
<p>Under &#8220;Allow applications downloaded from:&#8221; select &#8220;Anywhere&#8221; like so:</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/gatekeeper.png" alt="" /></p>
<p>Once you&#8217;ve done that you should be able to install Git.</p>
<h3>Windows</h3>
<p>If you&#8217;ve got a Windows computer, download the setup exe file and use all the default settings.</p>
<p>When you get to the <strong>Adjusting your PATH environment</strong> screen, be sure to choose the option for <strong>Use Git Bash Only</strong>. Git Bash is a program that will be installed that lets you interact with Git and your computer in much the same way as the Terminal application on Apple computers.</p>
<p>You should have now have a program in your Start Menu called Git Bash. If you hit the Windows key to pull up the start menu and type &#8220;git bash&#8221; you should see the program highlighted. I&#8217;m going to explain a bit about what Git and Github are before we need to open the program.</p>
<h2>Learning to talk to your computer</h2>
<p>Git is a program with out a graphical user interface. Git has no buttons, no icons. There are quite a few programs that give Git a graphical user interface, but we aren&#8217;t going to use those.</p>
<p>Why? Because I prefer the keyboard to the mouse/trackpad but also because the buttons and icons obscure what Git is doing and what you are telling Git to do. So we&#8217;re going to learn the hard way so that you learn more.</p>
<h3>No Buttons</h3>
<p>Most of the programs you use have graphical user interfaces (GUIs), the Finder (Explorer on Windows), web browsers, word processors, etc. You click on a button and something happens.</p>
<p>Before GUIs there was the command line. No buttons, just text input. On the command line you have to type in what you want the computer to do and it responds. It is through this command line that we will interact with Git.</p>
<h3>Opening Terminal (or Git Bash)</h3>
<p>To get to the command line on a Mac open up the application <strong>Terminal</strong>. The quickest way to open Terminal is to click the magnifying glass in the top right corner of your screen and type &#8220;terminal&#8221; and click the first result, looking something like this:</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/open-terminal.png" alt="" /></p>
<p>On Windows, we will use <strong>Git Bash</strong> which is a program that was installed with Git and emulates the same command line as on OS X. To open Git Bash, hit the Windows Key and type &#8220;git bash&#8221; you should see a program listed first with an orange icon, click that to open it. If you don&#8217;t see this program, reinstall <a href="http://git-scm.com/downloads">Git</a> and be sure to select the option to install Git Bash.</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/open-git-bash.png" alt="" /></p>
<p>For the rest of this tutorial I&#8217;m going to use &#8220;Terminal&#8221; to refer to both Terminal.app on Mac and Git Bash.exe on Windows.</p>
<h3>What is this Terminal?</h3>
<p>You can think of the Terminal as an alternate view of the files and folders on your computer, instead of a Finder or Explorer window, it&#8217;s this black or white box with a cursor.</p>
<p>In the Finder each folder has a list or grid of the contents of the folder. In Terminal we have something called the <strong>prompt</strong>, it&#8217;s all that text to the left of the cursor.</p>
<p>Hit enter a few times and you&#8217;ll see the same thing repeated down the screen of the Terminal. That&#8217;s your prompt. Treat it like a good friend, get to know it.</p>
<p>Somewhere in your prompt you should see a tilde (<code>~</code>). In every Finder window you&#8217;re looking at a location on your computer. It could be your Downloads folder or your Pictures folder. This is the same in Terminal. The tilde is the folder you are currently in. Wait, you don&#8217;t have a folder named &#8220;~&#8221;? That&#8217;s because the tilde is a variable for <code>/Users/sklise</code> but instead of &#8220;sklise&#8221; it would be your username. On Windows the &#8220;~&#8221; stands for <code>/c/Users/sklise</code>. When you direct Terminal to a different folder the &#8220;~&#8221; will change to reflect the name of the folder you are in. This is the only visual clue as to where you are, so pay close attention to it.</p>
<h3>Seeing Files, Moving to Folders</h3>
<p>Finally, some commands for Terminal.</p>
<p>Let&#8217;s see what the contents of <code>~</code> are. To do this we will use the command <strong><code>ls</code></strong>. Type the following in to Terminal and hit enter:</p>
<pre><code>$ ls </code></pre>
<p>(Whenever you see <code>$</code> at the beginning of a line of code, don&#8217;t type it, it&#8217;s there to say &#8220;This is something typed in to Terminal.&#8221;)</p>
<p>What just happened? Your computer gave you some output and then returned you to your prompt. Here&#8217;s what my output looked like, you&#8217;ll probably have less items listed than I do:</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/ls.png" alt="" /></p>
<p>The list you see is a list of the folders and files inside of <code>/Users/sklise</code>. Now I want to move to the Desktop, just because. In the Finder I&#8217;m able to just click on the word &#8220;Desktop&#8221; and there I am. In Terminal we have to type a command to get there.</p>
<p>The command to move to move to a folder is <strong><code>cd</code></strong>. CD stands for &#8220;change directory.&#8221; Directories and folders are the same thing. When we use the <code>cd</code> command we need to tell it what directory we want to change to.</p>
<p>Type the following into Terminal and hit enter:</p>
<pre><code>$ cd ~/Desktop </code></pre>
<p>Are you back at your prompt? Is anything different? You should see the <code>~</code> has been replaced with <code>Desktop</code>. That means we are now in the Desktop folder. If you type</p>
<pre><code>$ ls </code></pre>
<p>You&#8217;ll get a list of all the files and folders on your Desktop. This may be a lot of files or it may be nothing.</p>
<h3>Make a Folder, Make a File</h3>
<p>Thus far we&#8217;ve only looked at things with the Terminal, we haven&#8217;t modified or created any thing. And by &#8220;thing&#8221; I mean folders or files on your computer.</p>
<p>For this tutorial we will work with a Processing sketch. If you don&#8217;t already have Processing installed, go <a href="http://processing.org">download it</a> now.</p>
<p>I want to make a Processing sketch called &#8220;radsketch.&#8221; Processing requires all sketch files to be inside of folders with the same name. So we will need a folder named &#8220;radsketch&#8221; and a file inside that folder called &#8220;radsketch.pde&#8221;. Let&#8217;s get started.</p>
<p>The command to make a folder is <strong><code>mkdir</code></strong>. This stands for &#8220;make directory,&#8221; programmers are lazy and don&#8217;t like to type unnecessary characters. Dropping vowels from words started way before the internet. We need to give the <code>mkdir</code> command the name of the directory (remember, folder and directory are the same thing) we want to make. Terminal doesn&#8217;t deal well with spaces, and in general having spaces in folder and file names will just slow you down. Anyways, Processing doesn&#8217;t let you have spaces in folder or sketch names. Let&#8217;s make our folder &#8220;radsketch&#8221;:</p>
<pre><code>$ mkdir radsketch </code></pre>
<p>It looks like nothing happened in the Terminal, you are right back at your prompt and nothing has changed. But if you look at your desktop you should find a folder named &#8220;radsketch&#8221;.</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/mkdir.png" alt="" /></p>
<p>Now to make the file &#8220;radsketch.pde&#8221;. For this we will use the <strong><code>touch</code></strong> command. Why&#8217;s it called touch? Because this command is used to update the timestamps on a file, if the file doesn&#8217;t exist, <code>touch</code> creates the file.</p>
<p>But first we want to be inside the &#8220;radsketch&#8221; folder. Do the following:</p>
<pre><code>$ cd ~/Desktop/radsketch </code></pre>
<p>Now we&#8217;ll use the touch command:</p>
<pre><code>$ touch radsketch.pde </code></pre>
<p>If you look in the radsketch folder on your desktop you&#8217;ll see a file you can open with Processing.</p>
<p>Leave the Terminal open and open radsketch.pde in Processing.</p>
<p>Our Processing sketch is not rad right now. Let&#8217;s make it rad. Open the file in Processing and write some code. This is what I&#8217;ll write:</p>
<pre><code>// radsketch.pde void setup() { size(200,200); background(255); smooth(); noStroke(); fill(255,0,0); ellipse(width/2, height/2, 50, 50); fill(255); triangle(width/2, height/2 - 25, width/2 + cos(radians(210))*25, height/2 - sin(radians(210))*25, width/2 + cos(radians(330))*25, height/2 - sin(radians(330))*25 ); } </code></pre>
<p>Kinda rad. It could be radder, but I don&#8217;t want to lose this state of the sketch. What should I do? Track the sketch with Git!</p>
<h2>Setting up Git</h2>
<p>We need to take a quick detour and execute two commands before we use Git. These two commands you only need to do once, ever. Or until you get a new computer.</p>
<p>A note about the following commands, put your name and preferred email address inside the quote marks. These values will be stored with Git and with every project you work on with Git. So be sure that the email address you use is ok to be public.</p>
<pre><code>$ git config --global user.name "YOUR_FULL_NAME" $ git config --global user.email "YOUR_EMAIL_ADDRESS" </code></pre>
<p>What&#8217;s the deal with this? Why does Git need to know your name and email address? Git is used to track changes to files in a project, part of tracking changes is noting who made the changes.</p>
<h2>Your first Git repository</h2>
<p>To start tracking a project with Git you need to tell Git to start doing so.</p>
<p>In the same Terminal window as we&#8217;ve been using, execute the following:</p>
<pre><code>$ git init </code></pre>
<p>You&#8217;ll get a one line response similar to the following</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/init.png" alt="" /></p>
<p>What just happened was Git created a folder inside the radsketch folder named &#8220;.git&#8221; which is hidden by the operating system. This folder is where Git stores all of the information needed to do what Git does. You&#8217;ll never have a reason to look at the contents of this folder.</p>
<h3>Status Updates</h3>
<p>What does Git know about the radsketch folder and its contents, and how do we find out what Git knows?</p>
<pre><code>$ git status </code></pre>
<p>Returns:</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/untracked.png" alt="" /></p>
<p>This is a really awesome message. Git is telling us that it sees one file in the folder that it is not tracking. This means Git doesn&#8217;t care about any changes to this file right now. And we are told to use <code>git add</code> to track the file.</p>
<p>Git is great at giving descriptive messages. <strong>So read the messages Git gives you.</strong></p>
<p>Really, if you don&#8217;t read what Git spits out you won&#8217;t know what you&#8217;ve done or if it worked properly.</p>
<p>Seriously. <strong>READ THE MESSAGES THE COMPUTER GIVES YOU WHEN YOU EXECUTE A COMMAND.</strong></p>
<h3>Staging</h3>
<p>Git uses a concept called a &#8220;staging area.&#8221; This is a liminal &#8220;space&#8221; between changes to files and a commit. It&#8217;s the prep area. You earmark the state of a file to be included in a commit and then you commit it.</p>
<p>This two step process will make more sense when you are dealing with a project with many files, right now it&#8217;s sufficient to tell you this is how it works and you have to do it this way.</p>
<p>Files are added to Git by typing <code>git add</code> and then the name of the file:</p>
<pre><code>$ git add radsketch.pde </code></pre>
<p>If you execute that command it looks like nothing happened—there&#8217;s no response. It&#8217;s time to run <code>git status</code> again.</p>
<pre><code>$ git status </code></pre>
<p><img src="http://skli.se/images/posts/introduction-to-git/staged.png" alt="" /></p>
<p>The status message has changed and we see that radsketch.pde is marked as a &#8220;new file&#8221; and under the heading &#8220;Changes to be committed.&#8221; So let&#8217;s make a commit already.</p>
<h3>Always Leave A Message</h3>
<p>When making a commit with Git you are required to leave a message. When working with others on a project it&#8217;s important to leave messages about what the changes were that you made to the code. Otherwise everyone on your team would have to read through your code and figure out what you were doing or you could just tell them &#8220;Made the circle green&#8221; and they can get back to work.</p>
<p>Also, as your projects grow in scale you&#8217;ll have a lot of commits and maybe take a few months off from working on a project. When you return to work on a project, say after summer vacation, you&#8217;ll probably have forgotten what you had been doing. Now, I&#8217;m not saying I did that with my thesis, but here is a section of commit messages from my thesis:</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/leave-a-message.png" alt="" /></p>
<p>You can see some descriptive messages but then also a string of 4 commits where the error message is &#8220;debugging.&#8221; To figure out what the heck I was doing then I&#8217;ll have to back and look at the commits in detail, much more tedious than if I had left myself a good message.</p>
<p>This is not a contrived example and no, I didn&#8217;t make those 4 &#8220;debugging&#8221; commits 6 months ago just for use in this blog post.</p>
<p>So, please, leave good messages. You&#8217;ll thank yourself later.</p>
<h3>Committing</h3>
<p>Now, where were we. Make a commit. Ok. The command to make a commit is <code>git commit -m</code>. The <code>-m</code> is to leave a message. Always leave a message.</p>
<pre><code>$ git commit -m "Created a triangle in a circle" </code></pre>
<p><img src="http://skli.se/images/posts/introduction-to-git/first-commit.png" alt="" /></p>
<p>We&#8217;ve made our first commit. Let&#8217;s do <code>git status</code> again and see what&#8217;s going on.</p>
<pre><code>$ git status </code></pre>
<p><img src="http://skli.se/images/posts/introduction-to-git/post-commit-status.png" alt="" /></p>
<p>Git doesn&#8217;t see any changes to the files since the last commit. Let&#8217;s make some changes and see what <code>git status</code> says after that.</p>
<pre><code>// radsketch.pde void setup() { size(200,200); background(255); smooth(); noStroke(); fill(0,255,0); rect(width/2 - 25, height/2 - 25, 50, 50); fill(255,0,0); ellipse(width/2, height/2, 50, 50); fill(255); triangle(width/2, height/2 - 25, width/2 + cos(radians(210))*25, height/2 - sin(radians(210))*25, width/2 + cos(radians(330))*25, height/2 - sin(radians(330))*25 ); } </code></pre>
<p>Now save those changes and execute:</p>
<pre><code>$ git status </code></pre>
<p><img src="http://skli.se/images/posts/introduction-to-git/modified.png" alt="" /></p>
<p>Geez, Git is great. It knows that we changed the file and it even tells us what we could do next. We&#8217;re going to do <code>git add</code> but before that let&#8217;s dig a bit deeper in to what is happening.</p>
<pre><code>$ git diff </code></pre>
<p><img src="http://skli.se/images/posts/introduction-to-git/diff.png" alt="" /></p>
<p>Git doesn&#8217;t just know that the file has changed, Git knows which lines have changed and more specifically that they are additions. When we add radsketch.pde and commit it Git will only store the contents of the change, which means that you aren&#8217;t wasting space making copies of everything that didn&#8217;t change which is what would happen if you copied the whole folder and renamed it &#8220;radsketch_v2&#8243;.</p>
<p>So let&#8217;s add radsketch.pde and make a commit</p>
<pre><code>$ git add radsketch.pde $ git commit -m "Added a rectangle behind the other shapes" </code></pre>
<p><img src="http://skli.se/images/posts/introduction-to-git/second-commit.png" alt="" /></p>
<p>That in a nutshell is how Git works on your computer. Everything we&#8217;ve done has been on our own computer. At no point did we reach out to the internet or use Github in anyway. That&#8217;s next.</p>
<p>Leave Terminal open, we&#8217;ll be returning to it soon.</p>
<h2>Sign up for a Github Account</h2>
<p><a href="https://github.com/signup/free">Click here</a> to sign up for a free Github account.</p>
<h3>Github is a Website</h3>
<p>Github is a website. Git is program on your computer. They may sound the same but they are distinct and separate.</p>
<p>Say it with me, Github is a website and Git is a program on your computer.</p>
<p>It&#8217;s not quite that simple though. Github is a website made of many servers some of which run Git. But the key thing to realize is that Github is not on your computer. We&#8217;ll be going over 2 Git commands that let your computer talk to Github&#8217;s servers.</p>
<h2>Get Your Code on Github</h2>
<p>We need to make a &#8220;new repository&#8221; on Github in order to send our Processing sketch to their servers.</p>
<p>Click the button in the top right of the screen, third icon from the left that says &#8220;Create a New Repo&#8221; when you hover over it.</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/new-repo-button.png" alt="" /></p>
<h3>We already have a repository, why are we making a new one?</h3>
<p>Github is a website and websites get their information from a database. So when we click &#8220;Create a New Repo&#8221; what we are doing is creating a new database entry on Github for this &#8220;repo.&#8221; One field in that entry is the location of the actual Git repository. In this case &#8220;Repository&#8221; refers both to the database entry and the actual Git repository.</p>
<h3>Filling out this form</h3>
<p>Here&#8217;s how I filled out this form</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/new-repo-form.png" alt="" /></p>
<p>Notes on this form:</p>
<ul>
<li>The &#8220;Repository name&#8221; does not need to match the name of the folder on your computer.</li>
<li>Description is of course optional.</li>
<li>Private repos on Github cost money. But if you&#8217;re a student you can <a href="https://github.com/edu">request a free micro plan</a>.</li>
<li>Don&#8217;t check the &#8220;Initialize this repository with a README.&#8221; Readmes are important and useful but for right now this will throw a wrench in the tutorial.</li>
</ul>
<p>Click &#8220;Create repository.&#8221;</p>
<h3>Telling Git about Github</h3>
<p>The page we are brought to has instructions for telling Git (on your computer) about this new Github repository we&#8217;ve created. Scroll down to &#8220;Push an existing repository from the command line&#8221; because we&#8217;ve made a repository on our computer already and we haven&#8217;t done this before.</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/add-remote-instructions.png" alt="" /></p>
<p>There are two lines there for us to copy and paste in to the Terminal.</p>
<p>Let&#8217;s copy and paste the first line in Terminal and then talk about it. My line is different than yours because yours will have <em>your</em> Github username in it.</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/git-remote-add.png" alt="" /></p>
<p>We are adding a <strong>remote</strong> to this Git repository. A remote is another computer that we want to share our repository with. Remotes are URLs. But those URLs are long so we can give the remote a name, in our case <strong>origin</strong>, so we don&#8217;t have to type the entire URL over and over.</p>
<p>At this point Git has <em>still</em> not connected to Github, we&#8217;ve merely told it the URL to connect to.</p>
<h3>A Push or a Shove</h3>
<p>At this point in the talk, hand motions were used. You&#8217;ll need to imagine them, or mime along with the reading.</p>
<p>We&#8217;ve told Git about Github, now we want to show Github what we&#8217;ve got. Let&#8217;s copy and paste the second line of the instructions into Terminal and hit enter.</p>
<pre><code>$ git push -u origin master </code></pre>
<p>You&#8217;ll be prompted for your Github username, type it in and hit enter. Then you&#8217;ll be prompted for you Github password. Type it in. <strong>The cursor will not move, you won&#8217;t see any visual indication of your typing</strong>. This is a security measure, if you mess up your password just hit DELETE…maybe 30 times, 40 for safe measure. Hit enter, you&#8217;ll get a response similar to but not identical to the following screenshot</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/first-push.png" alt="" /></p>
<p>Go back to your browser and refresh the page.</p>
<p><img src="http://skli.se/images/posts/introduction-to-git/post-push.png" alt="" /></p>
<p>You&#8217;ll see radsketch.pde on the page, if you click it, there&#8217;s the contents of the file. Awesome.</p>
<p>This is the end of this blog post. I haven&#8217;t even touched on the most amazing parts of either Git or Github. That&#8217;s coming in the next blog post.</p>
<p>For now, repeat this process with your own homework assignments. Only through repeated practice will you get better.</p>
<h2>References &amp; Further Reading</h2>
<ul>
<li><a href="http://git-scm.com/book/en/Getting-Started-About-Version-Control">What is Version Control</a></li>
<li><a href="http://git-scm.com/book/en/Getting-Started-Git-Basics">Git Basics</a></li>
<li><a href="http://help.github.com">Github&#8217;s help pages</a></li>
<li><a href="http://git-scm.com/book/">Pro Git Book</a></li>
</ul>
<h2>Did I make a mistake?</h2>
<p>If you find something wrong or missing or unclear, please let me know by opening an <a href="https://github.com/stevenklise/stevenklise.github.com/issues">issue</a> on Github.</p>
