![](images/00071.jpeg)

## Your First Meteor Application

### A Complete Beginner's Guide to Meteor.js

#### David Turnbull

© 2014 David Turnbull

## Table of Contents

*   [1 Introduction](#part0002.html_leanpub-auto-introduction)
    *   [1.1 Prerequisites](#part0003.html_leanpub-auto-prerequisites)
    *   [1.2 What You’ll Need](#part0004.html_leanpub-auto-what-youll-need)
    *   [1.3 This Book](#part0005.html_leanpub-auto-this-book)
*   [2 Getting Started](#part0006.html_leanpub-auto-getting-started)
    *   [2.1 Command Line](#part0007.html_leanpub-auto-command-line)
    *   [2.2 Installing Meteor](#part0008.html_leanpub-auto-installing-meteor)
*   [3 Projects](#part0009.html_leanpub-auto-projects)
    *   [3.1 What is Leaderboard?](#part0010.html_leanpub-auto-what-is-leaderboard)
    *   [3.2 Create a Project](#part0011.html_leanpub-auto-create-a-project)
    *   [3.3 Launch the Local Server](#part0012.html_leanpub-auto-launch-the-local-server)
    *   [3.4 Default Application](#part0013.html_leanpub-auto-default-application)
    *   [3.5 Client vs. Server](#part0014.html_leanpub-auto-client-vs-server)
*   [4 Databases, Part 1](#part0015.html_leanpub-auto-databases-part-1)
    *   [4.1 MongoDB vs. SQL](#part0016.html_leanpub-auto-mongodb-vs-sql)
    *   [4.2 Collections](#part0017.html_leanpub-auto-collections)
    *   [4.3 Inserting Data](#part0018.html_leanpub-auto-inserting-data)
    *   [4.4 Finding Data](#part0019.html_leanpub-auto-finding-data)
*   [5 Templates](#part0020.html_leanpub-auto-templates)
    *   [5.1 Create a Template](#part0021.html_leanpub-auto-create-a-template)
    *   [5.2 Create a Helper](#part0022.html_leanpub-auto-create-a-helper)
    *   [5.3 `each` Blocks](#part0023.html_leanpub-auto-each-blocks)
*   [6 Events](#part0024.html_leanpub-auto-events)
    *   [6.1 Create an Event](#part0025.html_leanpub-auto-create-an-event)
    *   [6.2 Event Selectors](#part0026.html_leanpub-auto-event-selectors)
    *   [6.3 Event Types](#part0027.html_leanpub-auto-event-types)
*   [7 Sessions](#part0028.html_leanpub-auto-sessions)
    *   [7.1 Thinking Ahead](#part0029.html_leanpub-auto-thinking-ahead)
    *   [7.2 Create a Session](#part0030.html_leanpub-auto-create-a-session)
    *   [7.3 The Player’s ID](#part0031.html_leanpub-auto-the-players-id)
    *   [7.4 Selected Effect](#part0032.html_leanpub-auto-selected-effect)
*   [8 Databases, Part 2](#part0033.html_leanpub-auto-databases-part-2)
    *   [8.1 Another Event](#part0034.html_leanpub-auto-another-event)
    *   [8.2 Advanced Operators](#part0035.html_leanpub-auto-advanced-operators)
    *   [8.3 Sorting Documents](#part0036.html_leanpub-auto-sorting-documents)
    *   [8.4 Retrieving Data](#part0037.html_leanpub-auto-retrieving-data)
*   [9 Forms](#part0038.html_leanpub-auto-forms)
    *   [9.1 Create a Form](#part0039.html_leanpub-auto-create-a-form)
    *   [9.2 The ‘submit’ Event](#part0040.html_leanpub-auto-the-submit-event)
    *   [9.3 Grabbing Data](#part0041.html_leanpub-auto-grabbing-data)
    *   [9.4 Removing Players](#part0042.html_leanpub-auto-removing-players)
    *   [9.5 Decreasing Scores](#part0043.html_leanpub-auto-decreasing-scores)
*   [10 Accounts](#part0044.html_leanpub-auto-accounts)
    *   [10.1 Login Providers](#part0045.html_leanpub-auto-login-providers)
    *   [10.2 `Meteor.users`](#part0046.html_leanpub-auto-meteorusers)
    *   [10.3 Login Interface](#part0047.html_leanpub-auto-login-interface)
    *   [10.4 Check Logged in Status, Part 1](#part0048.html_leanpub-auto-check-logged-in-status-part-1)
    *   [10.5 Check Logged in Status, Part 2](#part0049.html_leanpub-auto-check-logged-in-status-part-2)
    *   [10.6 One Leaderboard Per User](#part0050.html_leanpub-auto-one-leaderboard-per-user)
    *   [10.7 Project Reset](#part0051.html_leanpub-auto-project-reset)
    *   [10.8 Other Login Providers](#part0052.html_leanpub-auto-other-login-providers)
*   [11 Publish & Subscribe](#part0053.html_leanpub-auto-publish--subscribe)
    *   [11.1 Thinking Securely](#part0054.html_leanpub-auto-thinking-securely)
    *   [11.2 autopublish](#part0055.html_leanpub-auto-autopublish)
    *   [11.3 isServer](#part0056.html_leanpub-auto-isserver)
    *   [11.4 Publications](#part0057.html_leanpub-auto-publications)
    *   [11.5 Subscriptions](#part0058.html_leanpub-auto-subscriptions)
    *   [11.6 Precise Publications](#part0059.html_leanpub-auto-precise-publications)
*   [12 Methods](#part0060.html_leanpub-auto-methods)
    *   [12.1 insecure](#part0061.html_leanpub-auto-insecure)
    *   [12.2 Create a Method](#part0062.html_leanpub-auto-create-a-method)
    *   [12.3 Inserting Data](#part0063.html_leanpub-auto-inserting-data-1)
    *   [12.4 Passing Arguments](#part0064.html_leanpub-auto-passing-arguments)
    *   [12.5 Removing Players](#part0065.html_leanpub-auto-removing-players-1)
    *   [12.6 Modifying Scores](#part0066.html_leanpub-auto-modifying-scores)
*   [13 Structure](#part0067.html_leanpub-auto-structure)
    *   [13.1 Your Project, Your Choice](#part0068.html_leanpub-auto-your-project-your-choice)
    *   [13.2 Thin Files, Fat Files](#part0069.html_leanpub-auto-thin-files-fat-files)
    *   [13.3 isClient](#part0070.html_leanpub-auto-isclient)
    *   [13.4 isServer](#part0071.html_leanpub-auto-isserver-1)
    *   [13.5 Other Conventions](#part0072.html_leanpub-auto-other-conventions)
*   [14 Deployment](#part0073.html_leanpub-auto-deployment)
*   [15 Conclusion](#part0074.html_leanpub-auto-conclusion)

## 1 Introduction

There’s a lot to love about the Meteor JavaScript framework:

*   You can build entire web applications with nothing but JavaScript.
*   Your applications are real-time by default, similar to desktop applications.
*   There’s a large and helpful community to help you along the way.

Meteor is also relatively easy to learn, making it a great for web development beginners who might have never built a web application before but still want to make software on the cutting edge of what’s possible on the web (and hopefully you fit somewhere on that spectrum).

It’s these reasons that, quite quickly, led me to becoming a Meteor fanboy. I’ve drunk the Kool-aid and I am loving the taste. It’s so enjoyable, in fact, that:

*   I’ve read almost every tutorial and watched every screencast out there.
*   I started [a blog about Meteor](http://meteortips.com) to share what I’m learning along the way.
*   I started writing this book.

Because while there are some great resources for learning Meteor, and while many of these resources are meant for beginners, I still found myself bouncing between multiple resources before certain Meteor concepts were able to “stick” in my mind. I couldn’t find a single resource that taught everything in the way I thought it should be taught. But that got me thinking — why not just write the book that I wanted to read?

So here we are.

*Your First Meteor Application*.

A detailed beginner’s guide for the Meteor JavaScript framework.

Let’s begin.

### 1.1 Prerequisites

In the coming pages, I’ve made a particular effort to write with beginning developers in mind. Specifically, this means:

*   You won’t need any prior experience with Meteor.
*   You won’t need to have made a web application before.
*   You won’t need to consult other sources along the way.

You will, however, need:

*   A basic understanding of JavaScript.
*   A basic understanding of databases.

For JavaScript, this means familiarity with variables, loops, conditionals, and functions, and for databases, this means familiarity with tables, rows, columns, and primary keys.

If you’re in need of these skills, then a site like [Lynda.com](http://www.lynda.com/promo/trial/Default.aspx?lpk35=1833&utm_medium=ldc-partner&utm_source=SSPRC&utm_content=655&utm_campaign=CD16647&bid=655&subID1=book&aid=CD16647) will come in handy, but in either case, I won’t expect readers to be JavaScript ninjas or database pros. The plan is to move slow and steady to guarantee consistent progress for almost anyone.

We’re not in a rush.

### 1.2 What You’ll Need

You don’t need much stuff to begin developing Meteor applications. Certain tools will make life easier but, for the moment, we’ll keep it simple.

As of writing these words, Meteor is officially supported on:

*   Mac: OS X 10.6 and above
*   Linux: x86 and x86_64 systems

There is, however, official support coming for Windows in the future and, as I’ll cover later, unofficial options are available for Windows so any major (and relatively current) operating system will work fine.

To write code, you’ll need a text editor. You probably have a preference and, if that’s the case, stick with it. We won’t be doing any power-user tricks. Personally, I use [Sublime Text](http://sublimetext).

For viewing Meteor applications on your local computer, Google Chrome is the browser of choice. It comes with handy development tools we’ll use later on and that you’ll be using throughout your life as a Meteor developers.

Once these basics are in order, you’re good to go.

### 1.3 This Book

Growing up, I read a lot of technical books, and honestly, many of them just weren’t that good. Writing at [Meteor Tips](http://meteortips.com) has shown me how difficult technical writing can be but it still seems silly that many books make the same, frustrating mistakes, like:

*   Explaining difficult concepts before they need to be explained.
*   Bloating pages with useless information to make the book longer.
*   Assuming that a single explanation is enough to explain an idea.
*   Trying to appeal to everyone – amateurs, pros, and everyone inbetween.
*   Drowning readers in theory while skimping on the practical stuff.

As such, I’d like to blatantly state that I’ve been careful to avoid these same mistakes that I’ve encountered over the years.

Have I done a perfect job?

Probably not, no.

I am, however, committed to doing the best job possible, so the plan is to never be “done” with this book. Instead, I’ll continue to rework the chapters when:

*   There’s updates to Meteor.
*   Reader feedback needs addressing.
*   My teaching philosophy changes.

But I don’t want to make it seem like you’ll read my words and all of a sudden “get” the intricacies of Meteor. It’s a great framework for beginners but it’s still programming. You do have to use your brain and certain ideas may not stick right away. You can do it, but it will take effort.

As the teacher, I’m treating your education as my responsibility, but as the student, there’s a few strategies that will significantly help your ability to learn and retain information:

1.  **Read through everything once**. Do this without writing any code. Get a sense of what you’ll be doing. Maybe write down any points that you struggle to grasp.
2.  **Read through everything again, slowly**. This time, write code, but don’t rush to the end. Take your time. It’s not a race. Give your brain time to absorb everything.
3.  **Tweak example code in simple ways**. Use different variable names. Output different strings in the JavaScript Console. Make the code “yours” to make sure that you’re properly engaged (rather than just going through the motions).
4.  **Commit to a set duration of study every day**. Do this instead of trying to reach a new milestone every day. Set a short duration – 20 minutes or so – and don’t break the chain.
5.  **Treat this like a marathon, not a sprint**. You can’t learn Meteor in a week. You can learn it though. Just be in this for the long haul. Being in a rush will only make it more difficult.
6.  **When you get stuck, stop**. Take a break. Go for a walk. Maybe shut the computer off for the day. Let your mind rest, then return to the problem at a later time.
7.  **Persist**. Don’t give up. Just keep going. Persistence is the greatest equaliser. It sounds cheesy but, if you don’t give up, you can’t fail. Sing it to the heavens: “I will not quit!”

Also know that **struggling is learning**. You don’t have to grasp new concepts for study sessions to be useful. Every time you sit down to code, you’re moving forward, even if you don’t feel like it. In the words of *Adventure Time*, “Suckin’ at something is the first step to being sorta good at something.”

## 2 Getting Started

Since we’re not in the same room, I can’t be sure of what you do and don’t know about building web applications. As such, I’ll make a couple of assumptions:

*   You have never used the command line.
*   You have not installed Meteor.

If these assumptions are wrong, feel free to skip over (or skim) this chapter. If these assumptions are not wrong, then you’re lucky that I’m so thoughtful since I’m about to explain everything you’ll need to know.

### 2.1 Command Line

Once upon a time, computers didn’t have graphical user interfaces with buttons, windows, or menus. Instead, for a user to be able to do anything on a computer, they would have to type out commands, tap the “Return” key on their keyboard, and in response to those commands, the computer would do something.

These days, *command line interfaces* are used by:

1.  People who forgot to update their operating systems.
2.  Developers.

Because while graphical interfaces are convenient and simple to use, they’re also time-consuming to create and ultimately slower to use. (You might think clicking is faster than typing a command but being able to use a computer without lifting your fingers from the keyboard is one of those abilities that will make you both look and feel superhuman.)

For these reasons, we don’t use a graphical interface when working with Meteor. It’d waste the time of Meteor’s developers to create it and any developer with a bit of command line experience prefers that approach anyway.

All computers should have access to a command line application and they’ll generally work in the same way, so don’t worry about whether or not you use Mac or Windows or Linux. The precise name of the command line application, however, will vary based on the operating system:

*   On Mac OS X, the command line is the *Terminal* application.
*   On Windows, the command line is the *Command Prompt* application.
*   On Linux, the name will depend on the distribution, but if you’re using Linux, you probably know what you’re doing anyway.

Whatever operating system you’re using, find the command line application with the search functionality so we can start writing our first commands.

![This is Terminal on Mac OS X 10.10](images/00001.jpeg)

This is Terminal on Mac OS X 10.10

### 2.2 Installing Meteor

At the moment, Meteor is officially supported on:

*   Mac: OS X 10.6 and above
*   Linux: x86 and x86_64 systems

Windows is missing from this list but Windows users can still install Meteor using unofficial options available at [win.meteor.com](http://win.meteor.com). The steps will be a little different from what I’m about to explain but Meteor will work as expected. Official support for Windows is planned for the future but there’s no reason to not get started today.

For the rest of us, the installation process couldn’t be simpler.

First, copy the following command to your clipboard:

```
curl https://install.meteor.com | /bin/sh
```

You don’t have to understand what this command actually means. Just make sure it’s on your clipboard and ready to be pasted.

Then:

1.  Open your command line application.
2.  Paste the command into the command line application.
3.  Tap the “Return” key.

At this point, your computer will connect to `install.meteor.com` and retrieve the latest version of Meteor. It’ll then download the latest version of Meteor and install it.

![Downloading the latest version of Meteor.](images/00002.jpeg)

Downloading the latest version of Meteor.

If the command *doesn’t* work – if an error appears – try the following command:

```
sudo curl https://install.meteor.com | /bin/sh
```

Here, the addition of this `sudo` keyword allows us to run the command as the administrator of the computer. You’ll be prompted for your password, so simply enter that and once again tap the “Return” key.

We’ll talk about some other commands in the next chapter but, honestly, it doesn’t get more difficult than what we’ve done here. You might want to read [The Command Line Crash Course](http://cli.learncodethehardway.org/book/) by Zed Shaw at some point, but you won’t need any special knowledge during this book. It’s just that, the more you know about the command line, the more productive you can be as a developer. You can also find some peace in the fact that, while graphical interfaces change based on trends and whims, the command line remains beautifully steadfast, so there’s no need to worry about your mastery of it suddenly becoming redundant overnight.

## 3 Projects

On the official website for Meteor, there’s an “[Examples](http://meteor.com/examples/)” section that shows off four different example applications:

*   Leaderboard
*   Parties
*   Todos
*   Wordplay

These applications are designed to show off the features of Meteor and, since the source code of each application can be downloaded and explored, they also act as great learning tools for developers.

In this chapter, we’ll take a look at Leaderboard – the simplest of these four applications – and then start rebuilding it from scratch.

Throughout the rest of the book, we’ll continue to work on Leaderboard but add some extra features to our creation so we can learn more about Meteor.

### 3.1 What is Leaderboard?

A common mistake that beginners make is attempting to write code before they have a clear idea of what they’re trying to build, but this is like driving to a destination without ever looking at a map. You might make a little progress in the right direction but you probably won’t get where you need to go.

In the future, once you have some more development experience, it’ll be easier to throw together a prototype application without a lot of preparation, but at least for now: **think about what you’re trying to build before you try to build it**. If this sounds obvious, wonderful. If not, then know that a mix of planning and patience is one of your greatest assets as a developer.

It’s for this reason that I like to use the Leaderboard application as the core of this tutorial. It’s not the most exciting thing to build but:

1.  **It’s conceptually simple**. You won’t struggle to grasp the end result and that’ll make it easier to take steps toward the end result.
2.  **It already exists**. You can see it and play with it, so when I explain what we’re going to build, you’ll know what I’m talking about.

Other technical books provide example applications that are more ambitious and interesting, which can be a little more motivating in the short term, but it also forces readers to think too much about what they’re building rather than how to build it. My belief is, it’s best to scale back on the ambition, make sure you don’t have to think too hard about what we’re building, and then you can derive motivation from making real progress.

To see the Leaderboard application in action, [watch this video](http://meteor.com/examples/leaderboard), or to play with it yourself, [check out this demo](http://leaderboard.meteor.com). It won’t take long to grasp the core features that we’ll soon recreate:

*   There’s a list of players.
*   Each player has a score.
*   A player’s score determines their rank.
*   You can select a player by clicking on them.
*   You can increment a selected player’s score.

It’s not a long list but there’s still a lot we can learn from working on this small amount of functionality.

### 3.2 Create a Project

When we’re ready to create our first Meteor application, we’ll need to start by creating a *project*, and a project is the self-contained set of files that forms the foundation of an application.

Every project is different but will generally contain:

*   HTML files, to define templates.
*   CSS files, to define styles.
*   JavaScript files, to define logic.
*   Folders, to keep things organised.

In a moment, we’ll create a project for the Leaderboard application but, before we do that, enter the following command into the command line:

```
mkdir Meteor
```

This `mkdir` command stands for “make directory” and as the name implies, it’s used to create a directory. Here, we’ve named the directory “Meteor” but you can name it whatever you want. The point of this directory is to store our Meteor projects so we’re able to keep them organised in one place. The exact location where this directory is created will depend on the operating system but, at least on Mac OS X, it will appear inside the “Home” directory. (This is where searching might come in handy.)

![The directory we just made.](images/00003.jpeg)

The directory we just made.

Once this directory is created, we can *change* (navigate) into it with this command:

```
cd Meteor
```

The `cd` command stands for “change directory” and is the command line equivalent to double-clicking on a directory inside the Finder.

![Entering commands into the command line.](images/00004.jpeg)

Entering commands into the command line.

Because of the `cd` command, we’re now inside the “Meteor” directory, which means it’s time to create our first Meteor project with the following command:

```
meteor create leaderboard
```

This command has three parts:

*   The `meteor` part defines this as a command related to Meteor.
*   The `create` part clarifies that we want to create a Meteor project.
*   The `leaderboard` part is the name we’re assigning to our project.

In place of the `create` keyword, we can use a range of other keywords to achieve different tasks. I’ll explain these other keywords when they’re relevant.

![Creating a Meteor project.](images/00005.jpeg)

Creating a Meteor project.

After running the previous command, a “leaderboard” directory will appear insde the “Meteor” directory that we created earlier. This directory is our Meteor project and, by default, will contain three files and a hidden directory :

*   .meteor
*   leaderboard.html
*   leaderboard.css
*   leaderboard.js

The `.meteor` directory contains important code that’s required for our application to function, so it’s best just to leave it alone. The remainder of the files contain default code that we’ll delete a few steps from now.

![Inside our "Meteor" folder.](images/00006.jpeg)

Inside our “Meteor” folder.

**Note:** If the names of your files are different, that’s because, by default, the names of the files are based on the name of the project. The names of your files are ultimately irrelevant though so they don’t have to match the name of the project.

### 3.3 Launch the Local Server

Web applications are not like static websites made of HTML and CSS. You can’t simply load the files into a web browser to see them in action. First, we need to launch what’s known as a *local server*.

From the command line, change into the “leaderboard” directory:

```
cd leaderboard
```

Then enter this command:

```
meteor run
```

Again, the `meteor` part defines this as a command related to Meteor, and then we have the `run` part to clarify the precise action we want to take.

In response to this command, and after a few seconds of loading, the following will appear within the command line:

```
=> Started proxy.
=> Started MongoDB.     
=> Started your app.
=> App running at: http://localhost:3000/
```

That last line is the important part because:

1.  It means the local server has launched.
2.  It provides a URL for the local server.

At this point, open Google Chrome and navigate to [http://localhost:3000](http://localhost:3000). You should see something like the following:

![The default Meteor application, running in Google Chrome.](images/00007.jpeg)

The default Meteor application, running in Google Chrome.

This is the result of the default code that’s included with every new Meteor project. If it appears in the browser, then everything’s working as expected. Leave the local server running from this point onward to continually see the results of your code.

### 3.4 Default Application

The default Meteor application isn’t that exciting and I won’t bother explaining what’s going on behind the scenes since we’ll cover all of the same content when working on Leaderboard anyway. I will, however, ask you to click on that lonesome button sitting within our bleary interface.

What happens when you click that button?

You’ll be forgiven for saying, “Nothing.”

In truth, something *is* happening – that something is just not communicated through the interface, so it’s not immediately obvious.

For proof of this, open the JavaScript Console within Google Chrome:

1.  Click on the `View` menu.
2.  Hover over the `Developer` option.
3.  Select the `JavaScript Console` option.

A pane will open at the bottom of the browser. Click the button within the application’s interface for a second time and notice that a message appears inside this pane that says, “You pressed the button.”

![A statement sent to the JavaScript Console.](images/00008.jpeg)

A statement sent to the JavaScript Console.

Within our project’s files, there’s a `console.log` statement that’s been written to trigger whenever the button is pressed. That statement looks like this:

```
console.log("You pressed the button.");
```

We don’t particularly care about this button, but:

1.  We’ll be using `console.log` statements in the coming chapters to display data instead of immediately creating a user interface.
2.  A range of commands can be entered into the JavaScript Console which allow us to easily manipulate our Meteor application’s database.
3.  Errors will appear inside the JavaScript Console, making it a handy tool for fixing problems with our code.

For these reasons, leave the JavaScript Console from this point onward.

### 3.5 Client vs. Server

To begin the coding of our Meteor application, open the HTML and JavaScript files inside our project and delete their contents. Don’t even look at the code. Just select it all and tap the “Delete” button. You won’t need to touch the CSS file since it’s empty by default.

After saving the HTML and JavaScript files, you might notice that the web browser automatically refreshes. This is because Meteor comes with a “LiveReload” feature that refreshes the browser for us when we make changes.

Inside the JavaScript file, write the following line of code:

```
console.log("Hello world");
```

This is the `console.log` statement we came across before and, if you switch back to Google Chrome, you’ll see the “Hello world” string in the JavaScript Console.

!["Hello World" in the JavaScript Console.](images/00009.jpeg)

“Hello World” in the JavaScript Console.

Without writing any other code though, switch to the command line. What do you see? You should see the exact same “Hello world” string.

!["Hello World" in the command line.](images/00010.jpeg)

“Hello World” in the command line.

This is significant because **we’ve written a single line of code that’s executed in two places**. The code has run on both the client (within the user’s browser) and on the server (where the application is hosted).

I mention this detail now for two reasons:

1.  It’s one of Meteor’s core features that allows for some very cool things to happen. (We’ll cover these “very cool things” throughout the book.)
2.  In the coming chapters, there’s a lot of code that we *don’t* want running in both places and we need to know how to control this behaviour.

On that second point, write the following conditional beneath the previous line:

```
if(Meteor.isClient){
    console.log("Hello client");
}
```

Save the file and see that the “Hello client” string appears in the JavaScript Console – on the client, within the user’s web browser – but does not appear on the command line.

!["Hello Client" in the command line.](images/00011.jpeg)

“Hello Client” in the command line.

We can also do the reverse:

```
if(Meteor.isServer){
    console.log("Hello server");
}
```

This “Hello server” string will appear on the command line – on the server, where the application is hosted – but not in the JavaScript Console.

**But if the ability to have one line of code execute in two places is one of Meteor’s core features, why do we want some code to *not* run in both places?**

Imagine we write some JavaScript code that affects our user interface. Maybe we write some code that displays some data from a database. That sort of code would have no need to run on the server. It wouldn’t even make logical sense. How could we “display” data on the server? That’s where background processing occurs. A user interface can’t be seen on a server.

The same is true in reverse. In some cases, it makes no logical sense for code to run on the client (within the user’s browser), and if you try to run code where it can’t logically run, Meteor will spit back an error. I’ll demonstrate one of these errors in a later chapter to illustrate this point.

For the moment, know that:

1.  One line of code can run on both the client and the server.
2.  Sometimes, we don’t want our code to run in both places.

Before the end of this book, the scenarios where this information is relevant will become obvious. It’s just important that I mention this early since we’ll continually come back to it while making our application.

To end this chapter:

1.  Delete the `console.log` statements.
2.  Leave the conditionals where they are.

Then let’s start making Leaderboard.

## 4 Databases, Part 1

One of the difficult parts of writing a technical book is deciding when to introduce ideas. The usual approach is to talk about creating the interface first, which has two main benefits:

1.  You can immediately see something in your browser.
2.  You feel like you’re making quick progress.

But it also introduces a couple of problems that will only short-change readers as they continue through the pages:

1.  It’s harder to truly grasp anything concerning the front-end (the interface) when you’re not familiar with what’s happening on the back-end (the database, etc).
2.  If we talk about the front-end first, we’ll have to back-track in the next chapter anyway, and that just makes it feel like progress has come to a sudden halt.

For these reasons, we won’t start by talking about interfaces. Instead, we’ll start by talking about *databases*. If that word alone sends you to sleep, fair enough, but if we spend a few minutes talking about what’s going on behind the scenes, you’ll have have a stronger foundation for the rest of the book.

### 4.1 MongoDB vs. SQL

If you’ve ever installed WordPress, used phpMyAdmin, or built a web application in PHP, you’ve come into contact with an SQL database.

By default, every Meteor project comes with its own database. There’s no setup or configuration required. It’s just ready to got the moment your project exists. This database, however, is *not* an SQL database. Instead, it’s a MongoDB database.

If you’ve never come across MongoDB before, you might be a little worried, but there’s no need to be. A MongoDB database is different from an SQL database but, to a beginner, these differences are small.

For the moment, you need to know two things:

First, **there’s no other type of database available for Meteor**. If you want to use an SQL database, it’s just not possible as of writing these words. Other options will be available in the future but, in either case, MongoDB is a good default option because:

1.  It’s fast.
2.  It’s scalable.
3.  It’s easy to earn.

So even if you’ve never come across it before, any database experience should be enough to quickly get a good handle on the basics.

Second, **MongoDB uses different words to describe familiar concepts**. We won’t, for instance, use words like tables, rows, or columns, but the concepts are basically the same.

You can see the differences in this table:

![SQL vs. MongoDB](images/00012.jpeg)

SQL vs. MongoDB

It is, of course, tricky to think of familiar concepts with different words, but I’ll remind you what the words mean along the way so they should stick by the time you reach the end.

### 4.2 Collections

The core feature of the Leaderboard application is the list of players. Without the list of players, we can’t build anything else of value. This makes the list a good place to begin our development journey – from the “middle” of our application and moving outward, toward the finer details.

But where do we store a player’s data?

The generic answer is, “In a database.”

The more precise and useful answer is, “In a *collection*,” and as shown in the table before, a collection is equivalent to an SQL table.

If we were to recreate WordPress in Meteor, we’d create a collection for the posts, a collection for the users, and a collection for the comments. There would be a collection for each type of data. Since we’re a creating this Leaderboard application though, we’ll want to create a collection for the players.

To do this, open the JavaScript file and write the following statement at the top (outside of the `isClient` and `isServer` conditionals):

```
new Meteor.Collection('players');
```

Here, we’ve created a collection named “players” but you can call it whatever you want. Just make sure the name is unique. There is, however, a problem: we have no way of referencing this collection and, therefore, no way of manipulating it.

To fix this, we need to associate a variable with our collection:

```
PlayersList = new Meteor.Collection('players');
```

Notice that we didn’t use the `var` keyword to define this variable. That’s because we want a global variable, since that will allow us to reference the variable throughout all of our files rather than just in one of them.

To confirm that the collection exists, switch back to Google Chrome and enter the name of the collection into the JavaScript Console:

```
PlayersList
```

You should see the following:

![The "PlayersList" collection.](images/00013.jpeg)

The “PlayersList” collection.

If an error is returned, it’s probably because you’ve mistyped the name of the variable or made a mistake with the syntax in the JavaScript file.

If an error is not returned, we can continue.

### 4.3 Inserting Data

Our collection exists but it’s empty. To fix this, we need to insert some data into the collection and, to achieve this, we can insert data:

1.  Through the JavaScript Console.
2.  Through the JavaScript file.
3.  Through a form in the interface.

I’ll explain these approaches during this book but, as you’ll see, manipulating the database through the JavaScript Console is the most convenient option.

To begin, enter the following statement into the JavaScript Console:

```
PlayersList.insert();
```

This is the syntax we use to manipulate our database. We start with the variable of our collection. Then we attach a function to it. But while this is a valid MongoDB statement, we haven’t passed any data through the brackets so the statement doesn’t do anything. The function is executed but the collection remains unchanged.

To actually insert data into the collection, we use the following syntax:

```
PlayersList.insert({
    name: 'David',
    score: 0
});
```

Here, we’ve done a few things.

First, we’ve added a pair of curly braces between the brackets. Within these braces, our data is structured in the JSON format. If you’re not familiar with the JSON format, you’ll pick it up along the way. (It’s not difficult.)

Second, we’ve defined the name of the *fields* in our collection:

*   name
*   score

You can name these fields whatever you like but, since we’ll be referencing them in our code, it’s best to make them simple and direct.

Third, we’re setting the values of the fields we’ve created. As shown in this table, we’ve given the `name` field a value of “David” and the `score` field a value of “0”:

![The structure of our collection.](images/00014.jpeg)

The structure of our collection.

Fourth, we’ve used a comma to separate the different fields. This is something that’s easy to overlook but, without a comma, we’d get an error. (If you do come across an error, check the commas!)

Ultimately, what we’ve done here is create a MongoDB *document* – the equivalent to a *row* in SQL terminology – and our plan is to create one document per player in our list. If you want six players in the list, you’ll need to create six different documents.

To achieve this, the same syntax will be the same. You just need to enter each statement into the JavaScript Console individually:

```
PlayersList.insert({
    name: 'Bob',
    score: 0
});
```

The white space is unnecessary though, so it’s fine to write:

```
PlayersList.insert({ name: 'Mary', score: 0 });
```

Also notice that, after each insert, a jumble of numbers and letters appears in the JavaScript Console. This jumble is a unique ID that MongoDB associates with each document. This ID is the *primary key* and it’ll be important later in the tutorial.

![Each document has a primary key.](images/00015.jpeg)

Each document has a primary key.

Before continuing, insert as many players into your collection as you like. The example applications has six players and that should be enough.

The players in my list are:

*   David
*   Bob
*   Mary
*   Bill
*   Warren
*   Tim

They all have a score of “0” but it doesn’t precisely matter if the players start with different scores.

### 4.4 Finding Data

We have a collection that contains our players and their scores but we need a way of pulling that data from the collection whenever want it. This can be achieved with the `find` function.

In the JavaScript Console, enter the following:

```
PlayersList.find();
```

This statement will return the data from the collection but it won’t be in its most readable form. That’s why it’s best to pair it with the `fetch` function:

```
PlayersList.find().fetch();
```

When working in the JavaScript Console, the `fetch` function will convert the data returned by the `find` function into an array. Simply click on the down-facing arrows to see the data contained within each docment.

![Using the `fetch` function.](images/00016.jpeg)

Using the `fetch` function.

To retrieve a precise selection of data from the collection, rather than all of the data, we can write something like:

```
PlayersList.find({ name: 'David' }).fetch();
```

Here, we’re passing a field and a value through the `find` function and, as a result, we’re able to just retrieve the documents in the collection where the player’s name is equal to “David”. If you don’t have any players in your collection with the name of “David”, an empty array will be returned.

![Retrieving precise data.](images/00017.jpeg)

Retrieving precise data.

What’s also useful is the ability to count the number of documents in a collection by attaching the `count` function to the `find` function:

```
PlayersList.find().count();
```

If you have six players (documents) in your collection, this pair of chained functions will return `6`.

![Using the `count` function.](images/00018.jpeg)

Using the `count` function.

To count a precise selection of data from the collection, pass something through the brackets of the `find` function and attach a `count` function to that, like so:

```
PlayersList.find({ name: 'David' }).count();
```

Here, we’re counting the number of documents in the collection where the “name” field is set to “David”. If one of your player’s names is set to “David”, this statement will return `1`. If none of your player’s names are set to “David”, this statement will return `0`.

At this point, we’ve only scratched the surface of the `find` function but a lot of functionality is available through what we’ve learned.

## 5 Templates

With a collection created and some data in place, we can start building the user interface for the Leaderboard application.

To begin, setup the basic HTML structure for our application by opening the HTML file and pasting the following code into it:

```
<head>
 <title>Leaderboard</title>
</head>
<body>
 <h1>Leaderboard</h1>
</body>
```

Right off the bat, there appears to be a few things missing from this code:

1.  We haven’t included the `html` tags.
2.  We haven’t included any JavaScript files.
3.  We haven’t included any CSS files.

But we haven’t included these things because we don’t have to include them. Meteor takes care of it for us. It includes the `html` tags automatically and also includes any CSS and JavaScript files that our application needs.

One of Meteor’s core principles is developer happiness, so there’s a lot of handy features like this that’ll make your development life easier.

![The current interface.](images/00019.jpeg)

The current interface.

### 5.1 Create a Template

Up next, we want to create a *template*, and by placing parts of our user interface inside templates, we’re able to interact with them using JavaScript code. (We’ll seen an example of this soon.)

To create a template, add the following code beneath the closing `body` tags inside the HTML file:

```
<template name="leaderboard">
 Hello world
</template>
```

Templates have a fairly vanilla structure. We use this `template` tag and attach a name to the template with this `name` attribute. I’ve named this template “leaderboard” but you can name it whatever you like. Just know that we’ll be referencing it shortly so, as per usual, it helps to choose a simple and direct name that’s easy to remember.

If you save the file in its current state though, the template doesn’t appear in the web browser. It’s in our raw HTML code but nowhere else.

What’s wrong?

Well, templates don’t appear by default because, in some cases:

*   You might want a template appear at specific times.
*   You might want a template to *dis*appear at specific times.
*   You might want a template to appear in multiple locations.

As such, templates need to manually included after they’re created. This might feel like just an extra step but it’ll be increasingly useful as we get deeper into development.

To make the “leaderboard” template appear in the browser, place this tag between the `body` tags:

```
{{> leaderboard}}
```

So obviously, this isn’t a HTML tag. The double-curly braces means it’s part of Meteor’s templating engine – Spacebars. Inspired by the Handlebars syntax, this is the syntax we use in our HTML when we want something dynamic to occur. We’ll use Spacebars a lot in this tutorial but, for now, just know that:

1.  All Spacebars tags use the double-curly braces to distinguish themselves.
2.  We only use the greater-than symbol when we want to include a template.

At this stage, the HTML file should resemble:

```
<head>
 <title>Leaderboard</title>
</head>
<body>
 <h1>Leaderboard</h1>
 {{> leaderboard}}
</body>

<template name="leaderboard">
 Hello World
</template>
```

After saving the file, the “Hello World” text should appear in the browser.

![The template is now appearing.](images/00020.jpeg)

The template is now appearing.

### 5.2 Create a Helper

In our HTML file, we have a template, but it’s static. It doesn’t do anything aside from display the boring “Hello World” text. To fix this, we can create a *helper*, and a helper is a JavaScript function that’s attached to a template. This is best understood with code, so let’s write some.

Switch to the JavaScript file and write the following statement beneath the line where we created our collection:

```
Template.leaderboard.player
```

This is the syntax we use to create a helper and it has three parts.

First, we use the `Template` keyword to search through the templates in our Meteor application. We only have one at the moment but a complete application may have dozens or even hundreds.

Second, we use the `leaderboard` keyword to reference the name of the template we created earlier. Every helper function we create needs to be attached to a single template.

Third, we use the `player` keyword to name our helper. We’ll reference this name in the HTML file and, again, you can name it whatever you like.

To attach code to this helper, we associate it with a function, like so:

```
Template.leaderboard.player = function(){
    // code goes here
}
```

We haven’t done anything special here. It’s just a regular function. The code inside this function will execute when we reference the `player` name in our HTML file.

There is, however, a problem. If you save the file and switch back to Google Chrome, you’ll see that the application is broken. That’s because we’ve failed to account for the fact that some code can’t run on both the client and the server.

![An error with our application.](images/00021.jpeg)

An error with our application.

Since we’re working with templates though – you know, user interface stuff – it doesn’t make sense for this helper function to exist on the server. As a result, Meteor doesn’t let it run on the server and an errror is returned.

What we have to do is place the helper inside the `isClient` conditional:

```
if(Meteor.isClient){
    // put the helper here
}
```

The code should then resemble:

```
if(Meteor.isClient){
    Template.leaderboard.player = function(){
    // code goes here
    }
}
```

After saving the file, the error will disappear.

To finally give our helper function some functinality, add a `return` statement inside of it:

```
Template.leaderboard.player = function(){
    return "A list of players should be here.";
}
```

Then switch back to the HTML file, remove the “Hello World” text, and place the following tag inside the “leaderboard” template:

```
{{player}}
```

Here, we’re using another Spacebars tag (as evidenced by the double-curly braces). We’re not, however, using the greater-than symbol. This is because we’re not including a template. We are instead referencing the name of our helper function and that is achieved with just the double-curly braces.

After saving the file, the text from the `return` statement will appear in the browser. It’s not a grand and exciting feature, but:

1.  This is similar to how we’ll use helpers later on, so the simplicity is a feature of Meteor rather than me trying to make it simple on purpose.
2.  We’re about to use helpers to retrieve the players from our collection and display them within the interface, and that’s quite a bit more interesting.

Let’s continue.

![Text from the `return` statement.](images/00022.jpeg)

Text from the `return` statement.

### 5.3 `each` Blocks

Within the “player” helper, change the `return` statement to the following:

```
Template.leaderboard.player = function(){
    return PlayersList.find();
}
```

Here, we’re using the `find` function that we covered earlier and, like before, we’re attaching it to the collection that holds the list of players. Because we’ve placed this statement in a helper though, we can reference this function in the template and display the data that it’s retrieved.

To do this, switch back to the HTML file and remove this tag:

```
{{player}}
```

This tag does reference our helper but not in the way we want. Instead, we want to write the following in our “leaderboard” template:

```
{{#each player}}
test
{{/each}}
```

Here, a few things are going on.

First, the players are being retrieved by referencing the “player” function.

Second, we’re looping through these players with an `each` block (again, using the Spacebars syntax).

Third, we’re outputting the word “test” for each player that’s in the list.

Conceptually, it’s like we have an array:

```
var player = ['David', 'Bob', 'Bill', 'Mary', 'Warren', 'Tim'];
```

…and it’s like we’re using a `forEach` loop to loop through the values within this array:

```
player.forEach(function(){
    document.write('test');
});
```

As a result, the amount of times the word “test” appears in the interface will be equal to the amount of players in the collection. If there’s six players in the collection, the word “test” will appear six times.

Within this `each` block that we’ve created, we can also retrieve the fields associated with the data that we’re retrieving. We’re retrieving data from the “PlayersList” collection, so we can display the values from both the `name` and `score` fields.

To to make our list show a list of player’s names, for instance, we can write:

```
{{#each player}}
    {{name}}
{{/each}}
```

(When referencing fields, we surround the field name with double-curly braces and nothing else.)

![A list of the player's names.](images/00023.jpeg)

A list of the player’s names.

We could also display the player’s scores beside their names:

```
{{#each player}}
    {{name}} {{score}}
{{/each}}
```

But while I’m not too concerned with making the user interface pretty – I’ve always found that focusing on design in a technical book is a waste of time – it is helpful if the interface has slightly better structure:

```
<ul>
    {{#each player}}
        <li>{{name}}: {{score}}</li>
    {{/each}}
</ul>
```

The names of the players will now appear in a list with their scores beside their names. By default, the players will be sorted by the date they were inserted into the collection in ascending order (from oldest to youngest).

![A list of players and their scores.](images/00024.jpeg)

A list of players and their scores.

If you’ve come to Meteor from any other framework or language, you can probably see that we’re getting a lot of functionality from a small amount of code, and it only gets better from here.

## 6 Events

At the moment, we have a list of players but no way to interact with this list of players. We’re retrieving data from a collection but, as far as the user is concerned, the web application is static. It’ll take a few steps to fix this but, first, we’ll create the effect of selecting players. Specifically, when a user clicks on an `li` element that contains a player’s name, the background of that `li` element will change colour.

To achieve this, we’ll use two components of Meteor:

*   Events, to detect that the user has clicked something.
*   Sessions, to store the data of what they’ve clicked.

In this chapter, we’ll focus on *events*.

### 6.1 Create an Event

By creating events within Meteor, we’re able to trigger the execution of code when the user clicks a button, submits a form, taps a key on their keyboard, or does one of the many things that we’re able to track and respond to. Meteor can detect a range of different events and we’re able to make something happen when those events occur.

To see this in action, write the following line within the `isClient` conditional:

```
Template.leaderboard.events();
```

Here, a few things are happening.

First, the `Template` keyword searches through the available templates in our application. (This is exactly what we did when creating the helper function.)

Second, the `leaderboard` keyword is the name of the template we want to associate with our events. As with helpers, events must be attached to a template.

Third, we use the `events` keyword to specify that, within the coming block of code, we want to create one or more events.

Inside the brackets at the end of this statement, we’ll define our events in the JSON format, meaning we’ll use a pair of curly braces:

```
Template.leaderboard.events({
    // events go here
});
```

We’ll then use the following syntax between the curly braces to create our first event:

```
'click': function(){
    // code goes here
}
```

This syntax might look a little weird but I’ll explain what’s going on.

First, we’ve defined the event *type*. That’s the `click` part within the inverted commas. This means the code within the associated function will execute when a user clicks something. We haven’t specific what the user has to click so the code will execute when the user clicks anything within the bounds of the “leaderboard” template.

Second, we’ve attached a function to this event and, within this function, we can write whatever code we want to execute when the event is triggered (when the click occurs).

To see this in action, add a `console.log` statement inside the event:

```
'click': function(){
    console.log("You clicked something");
}
```

The entire events block should now resemble:

```
Template.leaderboard.events({
    'click': function(){
        console.log("You clicked something");
    }
});
```

After saving the file, switch back to Google Chome and click anywhere within the bounds of the “leaderboard” template. With each click, the “You clicked something” string will appear in the JavaScript Console.

![Clicking something.](images/00025.jpeg)

Clicking something.

Feel free to (temporarily) change the `click` event to the `dblclick` event so the event’s function will respond to double clicks rather than single clicks:

```
'dblclick': function(){
    console.log("You double-clicked something");
}
```

There is, however, a fairly obvious problem:

Our code executes when a user clicks anywhere within our “leaderboard” template, and that’s not the most useful feature. We want to trigger our event’s function when something specific is clicked, like a button or an `li` element.

To achieve this, we’ll use event *selectors*.

### 6.2 Event Selectors

By using event selectors, we can attach events to specific HTML elements within our web application. If you’ve ever used jQuery before, this will be familiar. If not, then it still won’t be too tricky.

Earlier, we placed `li` tags in our HTML tags:

```
<li>{{name}}: {{score}}</li>
```

The plan now is to change our event so it responds when we click on of these `li` elements, rather than responding when we click anywhere. Here’s how we do that:

```
'click li': function(){
    console.log("You clicked a list item");
}
```

Here, we did two things:

1.  Added the `li` part after the `click` keyword.
2.  Changed the ouput of the `console.log` statement.

Because of that first, our event will only trigger – and the code within our event’s function will only execute – when we click on an `li` element.

But what if we had other `li` elements within the “leaderboard” template that weren’t part of the player’s list? You’d be right to assume that this would cause a problem. Our event would trigger when we didn’t want it to trigger.

To fix this, we can add a `player` class to our `li` elements:

```
<li class="player">{{name}}: {{score}}</li>
```

Then reference this class when creating the event:

```
'click li.player': function(){
    console.log("You clicked a player's list item");
}
```

Here, we made similar changes to before:

1.  Attached the `player` class to the `li` element.
2.  Changed the output of the `console.log` statement.

We have a lot of flexibility when defining events. As long as we state the event type first, we can use any selector as we normally would in a CSS file. To keep things simple though, let’s stick with the event that we’ve created.

![Clicking an `li.player` element.](images/00026.jpeg)

Clicking an `li.player` element.

### 6.3 Event Types

As much as possible, I’m trying to avoid taking detours as we talk about Meteor. I’d rather get from Point A to Poing B as quickly as possible, then help fill in the blanks once you’ve had the chance to make something. But since it’s fun to mess around with the different event types in Meteor, I think it’s worth taking a slight detour.

Within Meteor, we have a range of event types available to us:

*   click
*   dblclick
*   focus
*   blur
*   change
*   mouseenter
*   mouseleave
*   mousedown
*   mouseup
*   keydown
*   keypress
*   keyup
*   submit

We’ve covered `click` and `dblclick` already, and we’ll talk about the `submit` event a little later on, but here’s my suggestion:

1.  Create another Meteor project.
2.  Play with the other event types.

You may not understand what each event type does by looking at their names but that’s where some Googling will come in handy. (Research is a huge part of the software development process, so get into the habit of assuming someone has had the same questions that you might have.)

For a taste, here is what you can expect from some of the event types:

*   The `focus` event fires when an element on the page is said to have focus – a user’s cursor is inside an input field, for instance.
*   The `blur` event fires when an element on the page loses focus, like when a user removes their cursor from an input field.
*   The `mouseenter` event fires when the user’s cursor hovers within the bounds of the associated element.
*   The `mouseleave` event fires when the user’s cursor stops hovering within the bounds of the associated element.
*   The `change` event fires when the value of certain elements change, like when a checkbox is either checked or unchecked.

Aside from being fun, the benefit of experimenting with event types is that you’ll intuitively know when to use them in real-world development. That said, it’s far from necessary at this point, so feel free to just skip ahead.

## 7 Sessions

At this stage, a function executes whenever the user clicks one of the `li` elements in our list. Using this function, we want to create the effect of players being selected when we click them. Specifically, the `click` event will change the background colour of an `li` element when it’s clicked. To achieve this, we’ll need to use *sessions*.

Sessions are used to store small pieces of data that:

*   Isn’t saved to the database.
*   Won’t be remembered on return visits.

This sort of temporary data might not sound immediately useful but it’s handy when creating interface, and as stated in Meteor’s own documentation, sessions can be used to “store things like the currently selected item in a list.”

### 7.1 Thinking Ahead

As I mentioned in the “Projects” chapter:

> …a common mistake that beginners make is attempting to write code before they have a clear idea of what they’re trying to build.

This doesn’t just apply to projects as a whole though. Even if you have a clear idea of the project you’re trying to build, it’s all too easy to rush ahead and try to build features before you have any sort of plan.

For small features, this isn’t a big deal since you can still make a decent amount of progress with trial and error, but since it’ll take a few steps to create the effect of selecting players on our list, it helps to explain what we’re doing rather than just jumping into the deep end.

In a moment we’ll create a session that contains:

*   A name (referred to as a *key*).
*   A value.

The name will be “selectedPlayer” and we’ll use this name at a later time to retrieve the value of our session. The value of the session will be set to the unique ID of the player that the user clicks.

If you’ve forgotten where “the unique ID of the player” comes from, think back to the “Inserting Data” chapter. Each time we used the `insert` function in the JavaScript Console, a jumble of numbers and letters appeared. This jumble was the unique ID – the primary key, if you recall – of the player we’d just created. This is also the ID we wish to store inside a session.

Having access to the unique ID of each player means the following is possible:

1.  A user clicks on a player.
2.  The `click` event is triggered.
3.  As a result, the “selectedPlayer” session is created. This session stores the unique ID of the player that was just clicked.
4.  Using a conditional, the ID stored in our session is matched against the IDs of the players in our list.
5.  When a match returns `true`, a CSS class is applied to that player’s `li` element. This class will alter the background colour of the `li` element.

What I’ve shared here is more conceptual than I would usually care to share, but ideally, you’ll understand what we’re trying to do before we try to do it. If not though, then no big deal. You may have to run through the coming chapter a couple of times (which I’d always recommend anyways) but there’ll be plenty of practicality from here on out, and that’ll help the details sink in.

### 7.2 Create a Session

Inside our `click li.player` event, delete the `console.log` statement and insert the following line:

```
Session.set('selectedPlayer', 'session value test');
```

The code for the events block should now resemble:

```
Template.leaderboard.events({
    'click li.player': function(){
        Session.set('selectedPlayer', 'session value test');
    }
});
```

The syntax we’re using here is as complicated as a sessions’s syntax will ever become. As we covered before, a session holds just two pieces of data:

*   The name of the session.
*   The value of the session.

In this example we’re storing the “session value test” string inside a session that we’ve named “selectedPlayer”.

To prove that our session is doing something, let’s immediately retrieve the value of the session with the following syntax:

```
Session.get('selectedPlayer');
```

Here, we’re using `get` instead of `set`, and we’re only passing through the name of the session that we want to retrieve. To output the value of this session to the JavaScript Console though, let’s store it inside a variable:

```
var selectedPlayer = Session.get('selectedPlayer');
```

Then add a `console.log` statement beneath this line:

```
console.log(selectedPlayer);
```

The final code for the events block should resemble:

```
Template.leaderboard.events({
    'click li.player': function(){
        Session.set('selectedPlayer', 'session value test');
        var selectedPlayer = Session.get('selectedPlayer');
        console.log(selectedPlayer);
    }
});
```

With this code in place, the “session value test” string will be stored in a session when a user clicks on a player’s `li` element, and that same string will then be immediately output to the JavaScript Console

![Outputting our session.](images/00027.jpeg)

Outputting our session.

This isn’t very useful code but it does demonstrate how we’re able to store a small piece of data inside a session and then retrieve it.

### 7.3 The Player’s ID

To make our session useful, we need our session to store the unique ID of the player that the user clicks. To prepare for this, let’s create a `playerId` variable *above* the `Session.set` statement:

```
var playerId = 'session value test';
```

Then change the `Session.set` statement to use this variable as the source of its value, rather than using a hard-coded string:

```
Session.set('selectedPlayer', playerId);
```

The code within the event’s function should now resemble:

```
var playerId = 'session value test';
Session.set('selectedPlayer', playerId);
var selectedPlayer = Session.get('selectedPlayer');
console.log(selectedPlayer);
```

But how do we make it so the value of the `playerId` variable is set the unique ID of the player that the user clicks? The code itself is extremely concise but also a little weird and abstract:

```
var playerId = this._id;
```

Confused?

Let’s break it down.

First, we refer to `this`, but as always, the value of `this` will depend on the context. In this context, `this` refers to the player that the user has clicked.

Second, the `_id` part is the name of the field that stores the player’s unique ID. In the same way that we created `name` and `score` field, MongoDB creates the `_id` field.

(The field is named `_id` rather than “id” simply because that’s how MongoDB names the field. The underscore differentiates between fields that we’ve created and fields that MongoDb creates for us. There’s no special meaning behind it.)

By attaching the `_id` field to `this`, we’re saying, “Give me the unique ID of the player that the user has just clicked.” Therefore, when the user clicks one of the players, the `playerId` variable will store the ID of that player.

As for our code, this is what it should now resemble:

```
Template.leaderboard.events({
    'click li.player': function(){
        var playerId = this._id;
        Session.set('selectedPlayer', playerId);
        var selectedPlayer = Session.get('selectedPlayer');
        console.log(selectedPlayer);
    }
});
```

It’s also worth mentioning that a single session can only hold a single piece of data. Therefore, if a user clicks on another player, the unique ID of that player will overwrite the value previously stored in the session.

![Retrieving the player's unique IDs by clicking on them.](images/00028.jpeg)

Retrieving the player’s unique IDs by clicking on them.

### 7.4 Selected Effect

When a user clicks on one of the players – specifically, on one of the `li` elements that contains a player – we want to attach a CSS class to that `li` element. This class will alter the background colour of that `li` element.

To create this feature, start by adding the following class to the CSS file:

```
.selected{
    background-color:#ccc;
}
```

Then create a new helper function in the JavaScript file:

```
Template.leaderboard.selectedClass = function(){
    // code goes here
}
```

We’ve attached this helper to the “leaderboard” template and assigned it a name of “selectedClass”.

Next, add a return statement to this function:

```
Template.leaderboard.selectedClass = function(){
    return 'selected';
}
```

Then switch to the HTML file and change this part:

```
<li class="player">{{name}}: {{score}}</li>
```

…to this:

```
<li class="player {{selectedClass}}">{{name}}: {{score}}</li>
```

The “leaderboard” template should now resemble:

```
<template name="leaderboard">
<ul>
    {{#each player}}
        <li class="player {{selectedClass}}">{{name}}: {{score}}</li>
    {{/each}}
</ul>
</template>
```

You might, however, be disappointed to discover that the `li` elements now have an ugly grey background. If you check the source code, you’ll see that this is because we’ve attached the “selected” class to the `li` elements. This is not the exact result we want but it’s a step in the right direction.

![An ugly background for the `li` elements.](images/00029.jpeg)

An ugly background for the `li` elements.

The next step is to create a variable inside our “selectedClass” helper function that holds the value of the “selectedPlayer” session:

```
var selectedPlayer = Session.get('selectedPlayer');
```

Then after this line, write the following statement:

```
var playerId = this._id;
```

So this is the same statement we added to the `click li.player` event and, again, we’re using it to retrieve the unique ID of a player. We can access this ID because the `{{selectedClass}}` tag is inside the `each` block. As a result, `this` refers to the player that is currently being iterated through within that `each` loop, allowing us to access the `_id` field of the players.

This allows us to write the following conditional inside the helper function:

```
if(selectedPlayer === playerId){
    return 'selected';
}
```

Here, we’re comparing the ID stored in the “selectedPlayer” session with the unique ID of the player that’s currently being iterated through in the `each` block. If there’s a match, the “selected” string is returned and attached to the appropriate `li` element. Otherwise, nothing happens.

This is what the final helper function should look like:

```
Template.leaderboard.selectedClass = function(){
    var selectedPlayer = Session.get('selectedPlayer');
    var playerId = this._id;
    if(selectedPlayer === playerId){
        return 'selected';
    }
}
```

With this code in place, users will be able to click on any `li` element that contains a player’s name and have the background colour of that `li` element change to the colour defined in our CSS file. This creates the effect of a player being selected when a user clicks on them.

![Here, I've clicked on Bob.](images/00030.jpeg)

Here, I’ve clicked on Bob.

## 8 Databases, Part 2

Yes, we’re talking about databases again. You’ll be happy to hear though that we won’t dwell on any theory.

In the coming pages, we’ll:

*   Create a button that, when clicked, increments the score of the selected player.
*   Rank the players based on their score (from highest to lowest).
*   Display the selected player’s name beneath the list.

This might sound like a fair few features for a single chapter but, as you’ll see, it doesn’t require a lot of code.

### 8.1 Another Event

To create the “Give 5 Points” button, place the following code in the “leaderboard” template:

```
<input type="button" id="increment" value="Give 5 Points" />
```

Make sure this button:

*   Is outside of the `each` block.
*   Has an ID that we can reference.

I also chose to wrap my button in `li` tags so I could align it nicely at the bottom of my list.

![My design skills.](images/00031.jpeg)

My design skills.

Next, we need to attach an event to this button, so switch back to the JavaScript file and take a look at the current events block:

```
Template.leaderboard.events({
    'click li.player': function(){
        var playerId = this._id;
        Session.set('selectedPlayer', playerId);
        var selectedPlayer = Session.get('selectedPlayer');
        console.log(selectedPlayer);
    }
});
```

Because the event we want to create will also be attached to the “leaderboard” template, we don’t have to create a new events block. We can place both events inside this block by separating them with commas:

```
Template.leaderboard.events({
    'click li.player': function(){
        var playerId = this._id;
        Session.set('selectedPlayer', playerId);
        var selectedPlayer = Session.get('selectedPlayer');
        console.log(selectedPlayer);
    },
    'click #increment': function(){
        // code goes here
    }
});
```

**Don’t forget the comma**. It’s one of the simplest mistakes you can make and will only result in an abundance of unnecessary hair-pulling.

Within the `click #increment` event that we’ve created, we’ll need to access the ID of the player that the user has clicked because we’ll use that ID to:

1.  Find the player with that ID in our collection.
2.  Increment the `score` field of that player by 5.
3.  Save the result to the database.

The ID will still be stored in our session so let’s create a variable and use `Session.get` to access this session inside our event:

```
var selectedPlayer = Session.get('selectedPlayer');
```

At this point, our event should resemble:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
}
```

So when a user clicks on the `#increment` button, the ID of the selected player will be pulled from the session and stored in the `selectedPlayer` variable. We’ll reference this variable in the next step.

### 8.2 Advanced Operators

Inside the `click #increment` event, add the following line beneath our previous statement:

```
PlayersList.update();
```

This is the function we use to update an individual player – specifically, an individual player’s document – within our collection. It doesn’t work exactly as you might first expect though.

When I first encountered MongoDB, I thought that, if I wanted to change the value of a field, then I could write something like the following:

```
PlayersList.update(
    {_id: selectedPlayer},
    {score: 5}
);
```

Without checking the MongoDB documentation, my theory was:

*   A document would be retrieved based on the ID being passed to the `_id` field.
*   Any field specified between the second set of curly braces would be updated.

But while this theory was almost correct, there was a big flaw in that **any field not specified between the second set of curly braces is deleted**.

As such, the above code would change the value of the `score` field to “5” but it would also delete the `name` field from that document. The document will retain the same primary key – the same unique ID – but if you’re not careful, the `update` function can easily delete a field you don’t want it to delete. This is because, in its current form, the `update` function:

1.  Deletes the original version of the document.
2.  Recreates the document with the specified fields.

If you need further clarification of what’s happening, add that previous block of code inside the `click #increment` event, like so:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.update(
        {_id: selectedPlayer},
        {score: 5}
    );
}
```

Then test it for yourself. Select one of the players in the list, click on the “Give 5 Points” button, and notice that the name of the player you selected disappears. Then use the `find` function in the JavaScript Console to see how the structure of that player’s document has changed:

```
PlayersList.find().fetch();
```

It’s not just the value of the `name` field is being deleted. It’s that the entire `name` field is being deleted from that document.

To get the `update` function working in the way that I originally expected it to work – updating the value of the `score` field without touching the rest of the document – we have to write the following:

```
PlayersList.update(
    {_id: selectedPlayer},
    {$set: {score: 5}}
);
```

Here, we’re using the `$set` operator. This allows us to change the value of a specific field without affecting the rest of the document. There’s a few extra curly braces though, so let’s break it down.

First, we have the `score` field an the value we want to set for that field:

```
score: 5
```

Second, we wrap this in curly braces:

```
{score: 5}
```

(This is all that we had before.)

Third, we place the `$set` operator in front of the curly braces:

```
$set: {score: 5}
```

MongoDB has a range of these special operators that have the `$` symbol in front of their name and we’ll talk about another one shortly.

Fourth, we wrap this line in another pair of curly braces:

```
{$set: {score: 5}}
```

With this code in place, the event should resemble:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.update(
        {_id: selectedPlayer},
        {$set: {score: 5}}
    );
}
```

You will also now be able to select a player from the list, click on the “Give 5 Points” button, and the selected player’s score will change to “5” without deleting the value of the `name` field or otherwise affecting the document.

![Setting the `score` field to a value of "5".](images/00032.jpeg)

Setting the `score` field to a value of “5”.

But still, the `$set` operator only *sets* the value of the `score` field to “5”. We could click the “Give 5 Points” button a thousand times but, in its current form, a player’s score would change to “5” on the first click and then simply remain at that same, static value. We’ve taken this slight detour for a couple of reasons though:

*   You’ll come across the `$set` operator before too long, so it’s helpful to know about it sooner rather than later.
*   There’s a similar operator we can use to increment a number.

That similar operator is the `$inc` operator and it’s format is the same:

```
{$inc: {score: 5}}
```

This operator, however, will:

1.  Find the current value of the `score` field.
2.  Add the specified number on top of the current value.
3.  Save the new value to the document.

In the end, the code for the event should resemble:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: 5}}
    );
}
```

To see this new functionality in action:

1.  Switch back to Google Chrome.
2.  Select one of the players in the list.
3.  Click the “Give 5 Points” button.

The score of the selected player will increment in real time features, the list will automatically update when teh form is submitted..

![Incrementing the `score` field with a value of "5".](images/00033.jpeg)

Incrementing the `score` field with a value of “5”.

### 8.3 Sorting Documents

One of the most noticeable problems with our application is that the players in our list are ranked by the time they were inserted into the collection, rather than by their score. This is easy enough to fix though.

In the JavaScript file, take a look at the “player” helper:

```
Template.leaderboard.player = function(){
    return PlayersList.find();
}
```

Then change the `return` statement to this:

```
return PlayersList.find({});
```

Here, we’re passing empty curly braces into the `find` function to explicitly state that we want to retrieve all of the documents – all of the players – from the “PlayersList” collection.

So what we had before:

```
return PlayersList.find();
```

…is technically the same as what we have now:

```
return PlayersList.find({});
```

The difference is, by using these curly braces, we’re able to pass a second argument through the `find` function, and that second argument is where w can start setting options that will be applied to the `find` function. We need a first argument – even an empty one – before we define a second one though.

For this second argument, we’ll use the `sort` operator:

```
{sort: {score: -1}}
```

There’s no `$` this time around but this is a similar structure to the `$set` and `$inc` operators that we covered before.

First, we start with the field we want to affect. In this case, we want to sort based on the `score` field, so we write:

```
{score: -1}
```

Then we place the operator before it and wrap it all in curly braces:

```
{sort: {score: -1}}
```

As for the `-1` value, this allows us to sort in descending order – meaning from the highest number to the lowest number. If the `score` field contained text, it would sort from Z to A. To sort the `score` field in ascending order – from lowest to highest – we could set this value to `1` rather than `-1`.

At this point, the `return` statement should resemble:

```
return PlayersList.find({}, {sort: {score: -1}});
```

…and the players in the list should be ranked by their scores, with the highest scoring player at the top.

![Sorting the players.](images/00034.jpeg)

Sorting the players.

But what happens if two players have the same score? At the moment, our code doesn’t account for this. Ideally though, two players with the same score will be ranked by their names. So if Bob and Bill hve the same score, Bill would be ranked above Bob.

To achieve this, we make the following change to the `sort` operator:

```
{sort: {score: -1, name: 1}}
```

Here, we’re sorting by the `score` field first in descending order, and then by the `name` field second in ascending order.

The final `return` statement should resemble:

```
return PlayersList.find({}, {sort: {score: -1, name: 1}});
```

Because of Meteor’s real time features, the list will automatically update when teh form is submitted. features, the player’s ranks will automatically update as their scores change.

![Sorting the players with more precision.](images/00035.jpeg)

Sorting the players with more precision.

### 8.4 Retrieving Data

Within the original Leaderboard application, there’s a feature that outputs the name of the selected player beneath the player’s list. I don’t think this feature is particularly useful but:

1.  It allows us to cover a few useful points.
2.  It’s the final feature of the original Leaderboard application, so we may as well get it done before continuing with the new stuff.

To begin, create the following helper function inside the JavaScript file:

```
Template.leaderboard.showSelectedPlayer = function(){
    // code goes here
}
```

As always, make sure it sits within the `isClient` conditional. The syntax we’re using should also be familiar at this point. We’re searching through our templates with the `Template` keyword, using the `leaderboard` keyword to specify that this helper function is for the “leaderboard” template, and then giving the helper function a name of “showSelectedPlayer”.

Within this helper, we’ll retrieve the ID of the selected player. We’ve done this a couple of times and, since the ID of the selected player will be in the session, there’s nothing new here either:

```
var selectedPlayer = Session.get('selectedPlayer');
```

Next, we’ll retrieve the selected player’s document from the “PlayersList” collection using their ID. To do this though, we’ll use the `findOne` function, which we haven’t discussed yet:

```
return PlayersList.findOne(selectedPlayer);
```

The benefit of the `findOne` function is that it will only ever retrieve a single document from a collection, so if you ever only need to retrieve a single document from a collection, this will be the most efficient approach.

As for how we’re using the `findOne` function, we’re passing through the ID of the selected player as the only parameter and, as a result, the document of that player is returned to us.

The code for our helper should resemble:

```
Template.leaderboard.showSelectedPlayer = function(){
    var selectedPlayer = Session.get('selectedPlayer');
    return PlayersList.findOne(selectedPlayer);
}
```

We can now reference this helper in the “leaderboard” template by wrapping its name in a pair of double curly braces:

```
{{showSelectedPlayer}}
```

But as you’ll see, the output’s not quite right, and that’s because the `findOne` function is returning the entire document from the collection, but we just want to specifically display the `name` field.

![We're retrieving the whole document at the moment.](images/00036.jpeg)

We’re retrieving the whole document at the moment.

To only display the `name` field, we can use this dot syntax:

```
{{showSelectedPlayer.name}}
```

We could also retrieve the `score` field of the selected player if we wanted:

```
{{showSelectedPlayer.score}}
```

Or even the `_id` field:

```
{{showSelectedPlayer._id}}
```

One last detail worth adding is a conditional that will only try to display the data of the selected player if a player is actually selected. Spacebars supports conditionals, so the following code will do:

```
{{#if showSelectedPlayer}}
    Selected Player: {{showSelectedPlayer.name}}
{{/if}}
```

If a player is *not* selected, the “showSelectedPlayer” helper function will return `null` and our template won’t try to render the non-existent data.

![Displaying the selected player.](images/00037.jpeg)

Displaying the selected player.

## 9 Forms

If a user stumbled across our Leaderboard application, there wouldn’t be a lot they could do with it. They can increment scores, but only for a list of players that we’ve defined, and that’s not particularly useful.

In the coming chapter, then, we’ll make it possible for users to both add and remove players from the list. Maybe then it’ll be kind of useful.

### 9.1 Create a Form

Switch to the HTML file and create a new template by placing the following code beneath the previous template:

```
<template name="addPlayerForm">
</template>
```

We don’t *have* to create a new template but, the bigger an application becomes, the easier it is to manage if it’s separated into smaller chunks. In this case, I’ve named the template “addPlayerForm”, but you can call it whatever you want.

Inside this template, create the following form:

```
<form>
    <input type="text" id="playerName">
    <input type="submit" value="Add Player">
</form>
```

There’s nothing special about this form. The only thing worth mentioning is that we’ve assigned the “playerName” ID to the text field and we’ll reference that ID in a coming step.

To include this form within our interface, we use the Spacebars syntax:

```
{{> addPlayerForm}}
```

I’ve placed this tag just before the closing `body` tag but you could place it inside the “leaderboard” template if you wanted to.

![Our beautiful form.](images/00038.jpeg)

Our beautiful form.

### 9.2 The ‘submit’ Event

Earlier, we talked about different event types like `click` and `dblclick`. Another useful event type is the `submit` event. This type allows us to trigger the execution of code when a form is submitted. We’ll use the `submit` event to insert data into the “PlayersList” collection when the form is submitted.

To begin, create a second events block inside the JavaScript file:

```
Template.addPlayerForm.events({
    // events go here
});
```

Note othat we need to create this new events block because each block must be associated with a specific template. A new template, therefore, means a new events block. We also need to make sure this code is still within the `isClient` conditional.

To create a new event, we then use a familiar syntax inside this block:

```
'submit form': function(){
    // code goes here
}
```

Here, we’re using the `submit` keyword as the event type. This is different from attaching a `click` event to our form’s submit button because a form submission can also occur by tapping the Return key on a keyboard. Using the `submit` keyword accounts for every possible way a form might be submitted.

The `form` keyword is in reference in reference to the `form` element that we created earlier. If we had multiple forms in a single template, we could associate an ID with each form and create events with the following syntax:

```
'submit form#idGoesHere': function(){
    // code goes here
}
```

But since we only have the one form in our template, we don’t need to be so specific.

To make sure our event is working, place a `console.log` statement inside of it:

```
'submit form': function(){
    console.log("Form submitted");
}
```

With this code in place, clicking on the “Add Player” button – or submitting the form with the Return key – will make the “Form submitted” message appear in the JavaScript Console.

There is, however, a problem, since submitting the form also makes the page refresh instantly. This happens because, usually, forms work like this:

1.  The user fills out some form fields.
2.  The user submits the form.
3.  The data is sent somewhere.

But when building a Meteor application, the process is a little different:

1.  The user fills out some form fields.
2.  The user submits the form.
3.  The data is extracted from the form fields.

So the form isn’t submitted in the traditional sense since the data isn’t being sent anywhere. It’s just immediately extracted.

The problem, then, is that the web browser expects the data to be sent somewhere and, when it’s not, it’s not smart enough to figure out what’s going on – hence, the page simply refreshes.

To fix this problem, we need to disable the default behaviour of the form so we have complete control over how it works.

First, let’s take a look at our event:

```
'submit form': function(){
    console.log('Form submitted');
}
```

Then make this change:

```
'submit form': function(theEvent){
    console.log('Form submitted');
}
```

Here, we’ve added the `theEvent` keyword as the first argument within our event’s function. The placement of this keyword means we can now use it to refer to the event from within the event itself.

Sound a little weird?

Consider this code:

```
'submit form': function(theEvent){
    console.log(theEvent.type);
}
```

Here, we’re able to reference our event from within the event using the `theEvent` keyword, and display the `type` parameter of our event in the JavaScript Console. In this instance, the word “submit” will appear in the JavaScript Console because the event is of the `submit` type. (But the page which still refresh, so the string will only appear briefly.)

We’ll reference our event for a different purpose though.

Change the `submit form` event to the following:

```
'submit form': function(theEvent){
    theEvent.preventDefault();
    console.log('Form submitted');
}
```

Here, we’re referencing the event from within the event itself using the `theEvent` keyword, and then using this `preventDefault` function to prevent our form’s default behaviour. As a result, our form won’t have any inherent behaviour and we’ll be able to manipulate it from scratch.

At this stage, the `console.log` statement will trigger when the form is submitted and the page won’t refresh.

![Submitting the form, successfully.](images/00039.jpeg)

Submitting the form, successfully.

### 9.3 Grabbing Data

Inserting data into the “PlayersList” collection. We can add the syntax we’ve used in the JavaScript Console into the `submit form` event:

```
PlayersList.insert({
    name: 'David',
    score: 0
});
```

But this precise statement would insert the hard-coded value of “David” for the `name` field, when what we want to happen is for our code to:

1.  Grab the value from our text field.
2.  Use that value for the `name` field.

Setting the score to the hard-coded value of “0” is fine, since every player should start from the same footing, the value of the `name` field needs to be set dynamically based on the user’s input.

To do this, let’s pass a second argument through our event’s function:

```
'submit form': function(theEvent, theTemplate){
    theEvent.preventDefault();
    console.log('Form submitted');
}
```

Here, we’ve added the `theTemplate` keyword to the function and this keyword refers to the template that our event is attached to. Our event is attached to the “addPlayerForm” template, so we can use the `theTemplate` keyword to:

1.  Search through the “addPlayerForm” template.
2.  Retrieve the value of the text field with the “playerName” ID.
3.  Create a document that uses this value for the `name` field.

Consider the following code:

```
theTemplate.find('#playerName');
```

Here, we’re referencing the “addPlayerForm” by using the `theTemplate` keyword, then using a `find` function to search through this template. The value we’re passing through this `find` function is a CSS selector. Earlier, added the “playerName” ID to our form’s text field, so now we can use the `#playerName` syntax to reference that ID.

The statement we’ve written basically says, “Search through our event’s template for this particular element…”

For the sake of convenience, add a variable to this statement:

```
var playerNameVar = theTemplate.find('#playerName');
```

Then reference this variable in a `console.log` statement:

```
console.log(playerNameVar);
```

At this point, the code should resemble:

```
'submit form': function(theEvent, theTemplate){
    theEvent.preventDefault();
    var playerNameVar = theTemplate.find('#playerName');
    console.log(playerNameVar);
}
```

But there’s a problem. This `find` function that we’re using only retrieves the HTML element itself – meaning, the text field. We don’t just want the text field though. We want the value inside of the text field.

![Retrieving the HTML element itself.](images/00040.jpeg)

Retrieving the HTML element itself.

To access the value inside of the text field, use the `value` property:

```
var playerNameVar = theTemplate.find('#playerName').value;
```

Now, whatever the user types into the text field will appear in the JavaScript Console when the form is submitted.

![Retrieving the value of the HTML element.](images/00041.jpeg)

Retrieving the value of the HTML element.

To make the form properly functional, add the `insert` function to the bottom of the event, like so:

```
'submit form': function(theEvent, theTemplate){
    theEvent.preventDefault();
    var playerNameVar = theTemplate.find('#playerName').value;
    PlayersList.insert({
        name: playerNameVar,
        score:0
    });
}
```

After saving the file, typing a name into the text field and submitting the form will create a document in the “PlayersList” collection that uses the submitted value as the value of the `name` field within that document.

![Adding a seventh player to the list.](images/00042.jpeg)

Adding a seventh player to the list.

### 9.4 Removing Players

To account for the other end of the spectrum – the ability to delete players – let’s add a button to the interface that will allow a user to remove the selected player from the “PlayersList” collection.

Somewhere in the “leaderboard” template, create a new button:

```
<input type="button" id="remove" value="Remove Player" />
```

I placed this next to the “Give 5 Points” button but the precise placement doesn’t matter.

![The addition of a "Remove Player" button.](images/00043.jpeg)

The addition of a “Remove Player” button.

In the JavaScript file, attach an event to the “leaderboard” template:

```
'click #remove': function(){
    // code goes here
}
```

(Don’t forget to separate the events in this block with commas.)

This event responds to the `click` event type and is attached to the element with the “remove” ID (which is the button we just created).

Inside this event, we need to:

1.  Retrieve the ID of the currently selected player.
2.  Remove that player from the collection based on their ID.

The first step is something we’ve done a couple of times before and we’ll do it in the same way again using our session.

Write the following statement inside the event:

```
var selectedPlayer = Session.get('selectedPlayer');
```

Then, beneath this line, we’ll use the `remove` function:

```
PlayersList.remove(selectedPlayer);
```

We haven’t talked about this function yet but there’s not much to say. We pass an ID through the function as the only parameter and, if that ID is found in the collection, the associated document will be removed.

The final code for this event should resemble:

```
'click #remove': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.remove(selectedPlayer);
}
```

In the web browser, users will now be able to select a player and click the “Remove Player” button to delete that player’s document from the collection.

![I removed Jerry from the list.](images/00044.jpeg)

I removed Jerry from the list.

### 9.5 Decreasing Scores

Imagine that a user accidentally increments the score of the wrong player. What are they to do? With our application in its current form, there’s nothing much they can do aside from delete the player, add the player back into the collection, and click the “Give 5 Points” until their score reaches the appropriate level. But that’s not the most elegant approach.

To account for human error, we’ll place a “Take 5 Points” beside the “Give 5 Points” button. That way, users can both increment and decrement scores.

First, let’s look at the “Give 5 Points” button in the HTML file:

```
<input type="button" id="increment" value="Give 5 Points" />
```

…and place a “Take 5 Points” button beside it:

```
<input type="button" id="increment" value="Give 5 Points" />
<input type="button" id="decrement" value="Take 5 Points" />
```

Notice that I’ve changed the ID of the button form “increment” to “decrement”, since we’ll need a separate reference to attach an event to this button.

![The addition of a "Take 5 Points" button.](images/00045.jpeg)

The addition of a “Take 5 Points” button.

Next, switch back to the JavaScript file and, inside the events block that’s attached to the “leaderboard” template, insert the following code:

```
'click #decrement': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: -5}}
    );
}
```

(As always, don’t forget the commas to separate the events.)

Usually, I don’t like pasting chunks of code in front of you, but this code is almost identical to the `click #increment` event that we created before.

We’ve made just two changes:

1.  When defining the event, it’s now `click #decrement` rather than `click #increment`.
2.  The value in the `$inc` operator is now `-5` rather than `5`. This reverses the effect of the operator and *decreases* the value of the `score` field by “5”.

Otherwise, the code works in the same way:

The function is triggered when the user clicks on the element we’ve specified – in this case, the element with the ID of “decrement” – and the ID the selected player is pulled from the “selectedPlayer” session. That ID is used inside the `update` function to find the selected player’s document, and the `$inc` operator is used to modify the value of the `score` field.

After saving the file, the new “Take 5 Points” button will allow users to decrement the scores of whatever player they select.

![Took some points from David.](images/00046.jpeg)

Took some points from David.

## 10 Accounts

If we deployed our Leaderboard application to the web in its current state, there’d be a lot of problems, but perhaps the most obvious problem is that it wouldn’t support multiple users.

At this point, we have a single leaderboard and a single list of players. If one user adds players to the list and another user adds players to the list, all of these players will be on the same list, which isn’t so useful. It also won’t take long for chaos to erupt considering that all of the users can freely remove players from the list and modify their scores. Users could never trust that they’re in control of the leaderboard.

To fix this, we’ll create a user accounts system, but while that might sound like a long, boring, possibly confusing process, it’s nothing of the sort when working with Meteor. Creating a user accounts system is actually one of the simplest things we can do.

In this chapter, we’ll make it so:

*   Users can register and login to the application.
*   Logged out users won’t be able to see the “Add Player” form.
*   Every user will have their own, unique leaderboard.

We’ll cover a lot of ground and it won’t take a lot of code.

### 10.1 Login Providers

Included with every installation of Meteor is a series of “login provider” packages. These are plugins, created by Meteor’s developers, that allow us to easily add the back-end of an account system to our application.

This back-end includes:

*   A collection to store our user’s data.
*   A number of useful functions we’ll soon cover.

To add one of these packages into our project, enter the following command into the command line:

```
meteor add accounts-password
```

(If the local server is currenty running, you’ll need to open a new command line window or tab to enter this command.)

![Adding the `accounts-password` package.](images/00047.jpeg)

Adding the `accounts-password` package.

This `accounts-password` package creates the back-end for an accounts system that, by default, uses an email and a password for registration and logging in. There’s an option available that allows users to choose a username if they want but I prefer to leave that option disabled. Other login provider packages are available which allow users to login via services like Twitter and Facebook, and we’ll talk about those briefly in a later section.

### 10.2 `Meteor.users`

After adding the `accounts-password` package to our project, Meteor creates a collection in our project’s database that will store the data of our users. This collection is referenced as `Meteor.users` and, although it may look a little different with that dot in the middle of the name, it function exactly the same as any other collection in our project.

For proof of this, enter the following into the JavaScript Console:

```
Meteor.users
```

If everything’s working as expected, the JavaScript Console should spit back some data that confirms that, yes, this is a collection no different from any collection that we could create ourselves.

![Looking at the `Meteor.users` collection.](images/00048.jpeg)

Looking at the `Meteor.users` collection.

With this in mind, we can use familiar functions on this collection, like the `fetch` function:

```
Meteor.users.find().fetch();
```

Or the `count` function:

```
Meteor.users.find().count();
```

But since no one had registered for our application yet, our collection is empty, so the first statement returns an empty array and the second statement returns `0`. Therefore, let’s allow users to register.

![Counting the users in our collection.](images/00049.jpeg)

Counting the users in our collection.

### 10.3 Login Interface

The `accounts-password` package added the back-end for our accounts system but we still need a front-end. We need a form for users to register and login, and an interface so users can change settings, recover lost passwords, etc.

This might sound like a lot to add but Meteor includes this functionality in another package known as `accounts-ui`.

To add this package to our project, enter the following command into the command line:

```
meteor add accounts-ui
```

Once the package is installed, open the HTML file and add the following tag between the `body` tags:

```
{{> loginButtons}}
```

Here, we’re including a “loginButtons” template. But where does this template come from? It’s from inside the `accounts-ui` package we added to the project.

Switch to the web browser and notice that we now have a “Sign In” button and, when clicked, there’ll also be a “Create Account” link.

![The interface for our accounts system.](images/00050.jpeg)

The interface for our accounts system.

This is not just a dummy interface though. It connects to the `accounts-password` package that we added earlier, meaning our accounts system is now fully functional.

Users can:

*   Register.
*   Login.
*   Logout.
*   Change their settings.
*   Recover a lost password.

To test this, click on the “Create Account” link and register with an email and password. You won’t be asked to confirm your email address but this option could easily be enabled.

![Registering.](images/00051.jpeg)

Registering.

After registering, also notice that a document has been added to the `Meteor.users` collection. You can see this by entering the following command into the JavaScript Console:

```
Meteor.users.find().fetch();
```

Or use the `count` function to see that it no longer returns `0`:

```
Meteor.users.find().count();
```

If you’re the only registered user, this statement should return `1`.

![Counting the users in our collection (again).](images/00052.jpeg)

Counting the users in our collection (again).

### 10.4 Check Logged in Status, Part 1

In the JavaScript Console, enter the following statement:

```
Meteor.user();
```

This function, provided to us by the `accounts-password` package, allows us to retrieve the MongoDB document of the currently logged in user. Therefore, if you’re logged in at the moment, it should return the data associated with your specific account. If you’re *not* logged in, this function will return `null`.

![The data associated with my account.](images/00053.jpeg)

The data associated with my account.

This function is useful for creating conditionals that test whether or not the current user is logged, like the following:

```
if(Meteor.user()){
    console.log("You're logged in!");
} else {
    console.log("You're not logged in.");
}
```

If the user is logged in, that first condition will return `true`. If the user is not logged in, then the `else` condition will trigger.

But do we need to use this `Meteor.user()` function right now?

No, not right now. It won’t play a part in the Leaderboard application. It will, however, play a part in many of your Meteor applications in the future, and for that reason, it was worth mentioning.

### 10.5 Check Logged in Status, Part 2

We don’t need to check whether or not the user is logged in using our JavaScript file but we do need to check whether or not the user is logged in from inside our template.

Why?

Because, if we don’t, even logged out users will see the “Add Player” form. We could disable the functionality of this form if users are not logged in but it’s easier if we make it so the form doesn’t appear in the first place.

To do this, write the following conditional inside our “addPlayerForm” template:

```
{{#if currentUser}}
    <p>You're logged in.</p>
{{/if}}
```

Here, there’s two things going on.

First, we’re using the Spacebars syntax to create the `if` statement itself. As was the case with the `each` block, we use the `#` symbol before the `if` keyword.

Second, we’re referring to this `currentUser` object, and this is just like referring to the `Meteor.user()` function, only that it’s designed for use in our templates. So, if the current user is logged in, `currentUser` will return the current user’s details – or `true` if used in a conditional – and if the current is not logged in, `currentUser` will return `null`.

The end result is that this “You’re logged in” message will only appear when the current user is logged in.

![Checking if the current user is logged in.](images/00054.jpeg)

Checking if the current user is logged in.

To use this in our application, wrap the form in the “addPlayerForm” template with a `currentUser` conditional, like so:

```
{{#if currentUser}}
    <form>
        <input type="text" id="playerName" />
        <input type="submit" value="Add Player" />
    </form>
{{/if}}
```

As a result, the form will no longer appear for logged out users.

![Logged out.](images/00055.jpeg)

Logged out.

### 10.6 One Leaderboard Per User

A critical addition to our application is for each and every user to have their own, unique leaderboard. This requires a couple of steps.

First, open the JavaScript file and find the `submit form` event that’s attached to the “addPlayerForm” template. This is what it looks like:

```
'submit form': function(event, template) {
    event.preventDefault();
    var playerName = template.find('#playerName').value;
    PlayersList.insert({
        name: playerName,
        score: 0
    });
}
```

Beneath the statement where we set the `playerName` variable, create another variable like the following:

```
var currentUserId = Meteor.userId();
```

Here, we’re using a function I haven’t mentioned before – `Meteor.userId()` – and this function returns the ID of the currently logged in user. (We don’t have to store this value in a variable. It’s just my personal preference.)

Next, add a field to the `insert` function within this event and set the value of that field to the ID of the currently logged in user:

```
PlayersList.insert({
    name: playerName,
    score: 0,
    createdBy: currentUserId
});
```

(Don’t forget the comma after the value of the `score` field.)

Here, we’ve added this `createdBy` field, and since we’re attaching the logged in user’s ID to this field, it means that every player that’s now added to the collection will be associated with one of the registered users.

To see this in action:

1.  Add a player to the collection using the form.
2.  Use the `find` and `fetch` function in the JavaScript Console.
3.  Click on the downward facing arrow for the latest document.

You should see something like the following:

![The addition of the `createdBy` field.](images/00056.jpeg)

The addition of the `createdBy` field.

That’s the first step done.

For, the second step find the “player” helper that’s attached to the “leaderboard” template. It should look something like the following:

```
Template.leaderboard.player = function(){
    return PlayersList.find({}, {sort: {score: -1, name: 1}});
}
```

Then, above the `return` statement, create another `currentUserId` variable:

```
var currentUserId = Meteor.userId();
```

Once again, we’re retrieving the ID of the currently logged in user.

We’re now going to change the `return` statement so it only retrieves players from the “PlayersList” collection where the value of the `createdBy` field is equal to the ID of the currently logged in user.

This is how we do that:

```
Template.leaderboard.player = function(){
    var currentUserId = Meteor.userId();
    return PlayersList.find(
        {createdBy: currentUserId},
        {sort: {score: -1, name: 1}}
        );
}
```

Here, we added the `createdBy: currentUserId` part between the first set of curly braces. As we covered in an earlier chapter, this allows us to retrieve a selection of data rather than all of the data from the collection. In this case, we’re only retrieving documents from the “PlayersList” collection where the `createdBy` field is equal to the ID of the currently logged in user.

With these steps complete, users will only see players they create.

![Monica is the only player attached to my account.](images/00057.jpeg)

Monica is the only player attached to my account.

### 10.7 Project Reset

A slight issue is that we have players in our collection who are not attached to a user. These are players who were added to the collection before we setup the `createdBy` field. To get rid of them:

1.  Stop the local server. You can do this by switching to the command line and pressing `CTRL` + `C` on your keyboard.
2.  Enter the following command into the command line:

```
meteor reset
```

This command wipes the database clean, giving us a fresh start and making sure none of the players are not attached to a user. You will, however, need to register for a second time since you account will also be deleted.

![Resetting the project.](images/00058.jpeg)

Resetting the project.

### 10.8 Other Login Providers

Earlier, we talked about the `accounts-password` package. This is what provided us with an entire back-end for an accounts system that allows users to register and login with an email and password. This is not the only login provider package available to us though.

As of writing these words, the following packages are also available:

*   accounts-facebook
*   accounts-github
*   accounts-google
*   accounts-twitter
*   accounts-weibo

These additional packages make it possible to easily add functionality like “Login with Twitter” and “Login with Facebook” to our applications. It’s not something I’ll detail in this book but I’m mentioning it because:

1.  It’s something you can play around with yourself.
2.  It’s cool.

Because while there’s a few extra steps involved, these other packages work in the same way as the `accounts-password` package. This means the user data is still stored in a `Meteor.users` collection and the objects we’ve referenced in the past few chapters like `Meteor.user()` and `currentUser` work without us changing anything.

To use any of these packages, just add them to your project:

```
meteor add accounts-twitter
```

Then add the `accounts-ui` package if it’s not already installed:

```
meteor add accounts-ui
```

After including the `{{> loginButtons}}` tag within the HTML file, you’ll be shown further instructions for connecting your application with each of these third-party services.

It’s also worth mentioning that you can add multiple login provider packages to a single application. This means you can allow users to choose how they want to register. To use multiple login provider packages, just add them as you normally would with the `meteor` add command.

## 11 Publish & Subscribe

It might seem like our application is basically finished – it still looks ugly but it has a fair few features now – but there’s something pretty major we haven’t talked about yet: *security*.

This book won’t provide everything there is to know about security, but over the next couple of chapters, you’ll get a good handle on the basics.

### 11.1 Thinking Securely

For this demonstration, create two accounts within your application and, for each account, add three players to the leaderboard.

As an example, here are my two users and their players:

![My users and their players.](images/00059.jpeg)

My users and their players.

Next, logout of either account and enter the following statement into the JavaScript Console:

```
PlayersList.find().fetch();
```

This is nothing new. We’re just retrieving all of the documents from the “PlayersList” collection and converting the results into an array.

![Retrieving the data.](images/00060.jpeg)

Retrieving the data.

There is, however, a problem you may not have considered:

**What happens when the application is deployed to the web?**

What happens if the average user has this same level of access available to them by opening the JavaScript Console and typing commands? Maybe not *every* user has that knowledge but isn’t this still a huge security risk? Users can freely navigate all of the data in the “PlayersList” collection, including:

*   Player IDs.
*   Player names.
*   Player scores.
*   User ID in the `createdBy` field.

Is this the most sensitive data in the world? Maybe not. But imagine if we built an application for sharing private messages. It’d be unforgivable if someone could open the JavaScript Console and browse through all of those messages with complete freedom.

But no matter what you’re building, it’s never a good idea to let users have access to more data than they need to have access to. It’s both:

*   A security risk.
*   A performance hazard.

Because while we’ll focus on the more important issue of security, you will greatly improve the performance of your application if users aren’t granted access to each and every piece of data inside your collections.

You might be wondering though: **why does our Meteor application include such a huge security risk by default?** But the answer’s quite simple:

Convenience.

Because of this security risk, we’re able to easily navigate through all of the data inside our database through the JavaScript Console. We’ve used the `find` and `fetch` functions on numerous occassions and these have been very useful because we’re not limited by what data we can access.

It’s just that, before our application is made available to the world, we have to make sure that we precisely define what data is available to each and every user. Users should be able to access the data they need, but no more than that.

To achieve this, we’ll discuss *publications* and *subscriptions*. They’re some of the more abstract concepts for beginners to learn, but for that exact reason, we’ll take this nice and slow (and keep it plenty practical).

### 11.2 autopublish

By default, this security risk is contained within a package that’s included with every Meteor project. This package, known as the `autopublish` package, allows access to all of the data in our database through the JavaScript Console. If we remove this package, our application will become more secure, but:

1.  All of the data in the “PlayersList” collection will become inaccessible.
2.  We’ll have to precisely define what data should be accessible.

(You might be wondering what will happen with the `Meteor.users` collection, but push aside that thought for a moment.)

To remove the `autopublish` package, enter the following command into the command line:

```
meteor remove autopublish
```

If you’re logged out, you might not notice an immediate change, but if you use the `find` and `fetch` functions in the JavaScript Console, it’ll appear as if we’ve deleted all of the data from the “PlayersList” collection:

```
PlayersList.find().fetch();
```

You can also login to an account and see that the leaderboard is also empty, once again making it appear as if we’ve deleted all of the data.

![After removing the `autopublish` package.](images/00061.jpeg)

After removing the `autopublish` package.

But fear not. Our data still exists. We just have to take an extra step before that data is made available to the client (to the user’s browser) and it’s that extra step which gives us a lot more control in terms of security.

### 11.3 isServer

So far, almost all of our code has been written within the `isClient` conditional. This is because we’ve been creating helpers and events, and neither of these things should occur outside of the user’s browser. It’s time to embark into new territory though as we use the `isServer` conditional.

If the `isServer` conditional is not already within the JavaScript file, write the following:

```
if(Meteor.isServer){
    // code goes here
}
```

Any code within this block will only execute on the server, which means two important things:

1.  The code we write here won’t (directly) affect the user interface.
2.  The code we write here will be inherently trusted.

That second point is the important point at the moment, since even though we’ve removed the `autopublish` package, we can still freely retrieve whatever data we want to retrieve as long as we’re retrieving it on the server.

For example, write the following inside the `isServer` conditional:

```
console.log(PlayersList.find().fetch());
```

This wouldn’t be the most useful code in the world but, if you save the file and check the command line (*not* the JavaScript Console), you’ll notice that our data is retrieved without any trouble.

![Retrieving data on the server.](images/00062.jpeg)

Retrieving data on the server.

### 11.4 Publications

What we want to do now is *publish* the data from within our “PlayersList” collection. You can think of this as transmitting our data from the server and into the ether. We’re basically saying, “This is the data we want to be available to users…” But we don’t specify anything more than that.

Within the `isServer` conditional, write the following:

```
Meteor.publish('thePlayers');
```

Here, we’re initiating the `publish` function and passing through a name as the first argument. This name is simply used as a reference.

Next up, pass a function through as the second argument:

```
Meteor.publish('thePlayers', function(){
    // this is where we retrieve the data
});
```

Within this function, we specify the data that we want to make available to users of our application. For the moment, let’s return all of the data from our collection:

```
Meteor.publish('thePlayers', function(){
    return PlayersList.find();
});
```

To be clear, this function will make *all* of the data from our collection available to users, which means it’ll duplicate the functionality of the `autopublish` package. Ultimately, this is not what we want, but it’ll do for the time being.

### 11.5 Subscriptions

Now that the data from the “PlayersList” collection is being transmitted from the server and into the ether, we need a way of grabbing this data from within the client. This process is referred to as *subscribing*.

Within the `isClient` conditional, write the following:

```
Meteor.subscribe('thePlayers');
```

Here, we’re initiating the `subscribe` function and passing through the name that we defined in our `publish` function as the first (and only) argument.

Save the file, switch back to the browser, and notice that the `find` and `fetch` functions are once again working in the JavaScript Console:

```
PlayersList.find().fetch();
```

If you log back into either of the user accounts, you’ll also see that our leaderboards are once again functional. But like I said, we’re sending all of the data to the client with our `publish` function, so our application isn’t secure yet. It’s simply ready to be secured.

![Duplicating the `autopublish` package.](images/00063.jpeg)

Duplicating the `autopublish` package.

### 11.6 Precise Publications

Inside the `isServer` conditional, this is what our `publish` functions looks like:

```
Meteor.publish('thePlayers', function(){
    return PlayersList.find();
});
```

But instead of the `publish` function retrieving all of the data from the “PlayersList” function, we want to make it so the function only retrieves the data that belongs to the currently logged in user.

This will have two notable effects:

1.  Logged in users will only have access to their data.
2.  Logged out users won’t have access to any data.

To make this change, create a `currentUserId` variable above the `return` statement within the `publish` function:

```
var currentUserId = this.userId;
```

Within a `publish` function, we’re unable to use the `Meteor.userId()` function that we used earlier. We can, however, refer to `this.userId` within the `publish` function and achieve the same result.

Our reference to `this.userId` will:

1.  Return the unique ID of the logged in user.
2.  Return `null` if the user is not logged in.

The variable isn’t necessary but it makes the code more readable.

Next, change the `return` statement to the following:

```
return PlayersList.find({ createdBy: currentUserId });
```

The final `publish` function should resemble:

```
Meteor.publish('thePlayers', function(){
    var currentUserId = this.userId;
    return PlayersList.find({ createdBy: currentUserId });
});
```

After saving the file, the application will be considerably more secure.

For proof of this, switch to Google Chrome, open the JavaScript Console, and enter the following statement:

```
PlayersList.find().fetch();
```

This statement will return an empty array because none of the data from the “PlayersList” collection is being sent to the client. Why? Because the `return` statement in our `publish` function only returns data where the value of the `createdBy` is equal to the current user’s ID. If the current user is not logged in, they have no ID and therefore nothing is returned. This means random visitors to the application have no way of navigating through any data within our database.

![The published data.](images/00064.jpeg)

The published data.

Next, login to one of the accounts. You’ll see that the players that “belong” to that user appear within the leaderboard. You can even see the data of these players by repeating the previous statement within the JavaScript Console:

```
PlayersList.find().fetch();
```

But the JavaScript Console *only* returns the data that belongs to the logged in user. This means:

1.  Users can only ever access their own data.
2.  Data is only passed around when it needs to be passed around.

The next chapter will cover another important aspect of security but we’ve made good progress here, so pat yourself on the back and maybe take a break before we continue. You (and your brain) deserve a little rest.

## 12 Methods

By default, every Meteor project has *two* major security issues:

*   The first issue is what we covered in the previous chapter – the ability for any user to access all of the data in the database.
*   The second issue is that users are still able to insert, modify, and remove data from our database with very few restrictions.

This second issue is what we’ll learn to fix in the coming chapter.

### 12.1 insecure

In the JavaScript Console, enter the following command:

```
PlayersList.insert({name: 'Cheater', score: 1000});
```

See the problem?

If we deployed our application to the web in its current state, anyone could open the JavaScript Console and freely insert whatever data they want into the “PlayersList” collection. They could also modify and remove data.

Again, this functionality is convenient for developers – we’ve been taking advantange of this direct manipulation of our database throughout this book – but it’s not something we can leave lingering.

As was the case with the `autopublish` package, this functionality is contained within a package known as the `insecure` package.

To remove the `insecure` package, enter the following command into the command line (not the JavaScript Console):

```
meteor remove insecure
```

After removing this package, our accounts system will still work, but the rest of our application will be completely broken:

1.  We can’t add players to any list.
2.  We can’t remove players from any list.
3.  We can’t modify player’s scores.

You’ll continue to see all of the current data from the database – that’s still handled by publications and subscriptions – but we’ll have no way of changing or manipulating this data. This is, however, a good thing.

![Failing to insert data.](images/00065.jpeg)

Failing to insert data.

So far, the `insert`, `update`, and `remove` functions have been running on the client. All of them are within the `isClient` conditional. But while this is convenient, our database will remain at risk for as long as users are able to modify data from the client since we can never reasonably trust a user. We have to assume that any code on the client is at risk of unwanted manipulation.

The alternative approach – and what removing the `insecure` package forces upon us – is to move all of the `insert`, `update`, and `remove` functions to the server. This is because any code on the server is inherently trusted. *We* run the server, after all. We’re in control. This makes it a safer place for our code to run because users don’t have direct access to it.

In the coming pages, then, our aim is to move any database manipulations from the `isClient` conditional to the `isServer` conditional.

This will require us to create our first *methods*.

### 12.2 Create a Method

In the JavaScript file, write the following inside the `isServer` conditional:

```
Meteor.methods({
    // methods go here
});
```

Within this block, we can define code that we want to run on the server but that can be triggered from the client.

To demonstrate how this works, let’s make it so submitting the “Add Player” form will trigger a `console.log` statement on the server.

First, choose a name for our method:

```
Meteor.methods({
    'executeLogStatement'
});
```

You can name methods whatever you like but I usually prefer using longer names since being descriptive will help make the code more readable.

Next, we associate a function with this name:

```
Meteor.methods({
    'executeLogStatement': function(){
        console.log("You submitted the form");
    }
});
```

(Notice that this is as similar syntax to an `events` block, so we’re not doing anything too radical here.)

At this point, we can *call* this method from elsewhere in our code. To trigger the method when the “Add Player” form is submitted, place this call within the `submit form` event, like so:

```
'submit form': function(theEvent, theTemplate){
    theEvent.preventDefault();
    var playerNameVar = theTemplate.find('#playerName').value;
    PlayersList.insert({
        name: playerNameVar,
        score:0
    });
    Meteor.call('executeLogStatement');
}
```

So this is the only code we added:

```
Meteor.call('executeLogStatement');
```

We run this `call` function and pass through the name of the method that we defined within the `isServer` conditional.

Now, whenever you submit the form, the “You submitted the form” string will appear within the command line (*not* the JavaScript Console). Hopefully, this shows how we can execute code on the server but trigger it from the client.

![This code was triggered from the client.](images/00066.jpeg)

This code was triggered from the client.

### 12.3 Inserting Data

At this point, it’s time to move the `insert` function from the `submit form` event to a method within the `isServer` conditional.

First, change the name of our current method:

```
Meteor.methods({
    'insertPlayerData': function(){
        console.log("You submitted the form");
    }
});
```

Then add a simple `insert` function into the method:

```
Meteor.methods({
    'insertPlayerData': function(){
        var currentUserId = Meteor.userId();
        PlayersList.insert({
            name: 'David',
            score: 0,
            createdBy: currentUserId
        });
    }
});
```

Here, we’ve also created another `currentUserId` variable and this code works exactly as expected by retrieving the ID of the current user.

You’ll notice that our `insert` function uses the hard-coded value of “David” for the player’s name, which isn’t exactly what we want, but we’ll solve that problem in a moment.

For now, remove the `insert` function from the `submit form` event and change the name passed through the `call` function.

The code within the event should then resemble:

```
'submit form': function(theEvent, theTemplate){
    theEvent.preventDefault();
    var playerNameVar = theTemplate.find('#playerName').value;
    Meteor.call('insertPlayerData');
}
```

If you login to an account and try adding a player to the leaderboard, you’ll notice that it kind of works. With the current code, the player’s name will always be “David” no matter what you enter into the form, but that’s still a step in the right direction.

![We can only insert players named "David".](images/00067.jpeg)

We can only insert players named “David”.

Before we continue, there’s three important things to note:

*   The user is unable to insert, update, or remove data through the JavaScript Console, so our application has remained secure.
*   When the form is submitted, the `insertPlayerData` method is called and the code within that method is executed.
*   Because our method executes on the server, the `insert` function can execute without trouble since code on the server is inherently trusted.

We do, however, need to allow users to once again choose the name of the player they want to insert into the database.

### 12.4 Passing Arguments

It’s possible to pass arguments intoto our method calls to make them a lot more useful. For example, change the `Meteor.call` function to the following:

```
Meteor.call('insertPlayerData', playerNameVar);
```

Here, we’re attaching the `playerNameVar` variable (which contains the value from within our text field) to our method call. This means we can now access this data from within our method *if* we allow our method to access it.

To do this, change the `insertPlayerData` method to the following:

```
'insertPlayerData': function(playerNameVar){
    var currentUserId = Meteor.userId();
    PlayersList.insert({
        name: 'David',
        score: 0,
        createdBy: currentUserId
    });
}
```

Here, we’ve added the `playerNameVar` parameter between the brackets of our function. We can then reference this parameter within the function, like so:

```
'insertPlayerData': function(playerNameVar){
    var currentUserId = Meteor.userId();
    PlayersList.insert({
        name: playerNameVar,
        score: 0,
        createdBy: currentUserId
    });
}
```

Here, we’ve replaced the hard-coded value of “David” with the `playerNameVar` variable.

This is the basic flow of what’s happening:

1.  When the form is submitted, the `insertPlayerData` method is called and the value from the text field is attached to this call.
2.  The method is executed and accepts `playerNameVar` as its first and only argument. We can then reference `playerNameVar` within the method.
3.  Inside the method, the `insert` function is executed, using the value stored within `playerNameVar` as the value for the `name` field.

The end result is that our “Add Player” form works as expected. The user types a name into the text field, submits the form, and that name is added to that user’s leaderboard. The only difference is, the `insert` function is executing within the trusted environment of the server and users are still unable to use the `insert`, `update`, or `remove` functions from the JavaScript Console. As a result, our application is a lot more secure.

This was just one method though. We still need to move some code from the `isClient` conditional to the `isServer` conditional to make everything once again functional.

### 12.5 Removing Players

Within the same `methods` block we created before, create a new method to handle the removal of players from the collection:

```
'removePlayer': function(){
    // code goes here
}
```

Make sure the methods within this block are separated with commas, meaning the entire block should resemble the following:

```
Meteor.methods({
    'insertPlayerData': function(playerNameVar){
        var currentUserId = Meteor.userId();
        PlayersList.insert({
            name: playerNameVar,
            score: 0,
            createdBy: currentUserId
        });
    },
    'removePlayer': function(){
        // code goes here
    }
});
```

Inside the `isClient` conditional, change the `click #remove` event from this:

```
'click #remove': function(){
      var selectedPlayer = Session.get('selectedPlayer');
      PlayersList.remove(selectedPlayer);
}
```

To this:

```
'click #remove': function(){
      var selectedPlayer = Session.get('selectedPlayer');
      Meteor.call('removePlayer');
}
```

So when a user clicks on the “Remove Player” button, the `removePlayer` method will now execute. We need to make sure the ID of the selected player is passed through though, so attach the `selectedPlayer` variable to the `call` function:

```
'click #remove': function(){
      var selectedPlayer = Session.get('selectedPlayer');
      Meteor.call('removePlayer', selectedPlayer);
}
```

We can then change the `removePlayer` method to accept this argument:

```
'removePlayer': function(selectedPlayer){
    // code goesh ere
}
```

…and use it to remove the selected player from the collection:

```
'removePlayer': function(selectedPlayer){
    PlayersList.remove(selectedPlayer);
}
```

### 12.6 Modifying Scores

I haven’t called this section “Incrementing Scores” or “Decrementing Scores” because we’re going to do something special by merging the `click #increment` and `click #decrement` events. This means, not only will our code be more secure because of methods, there’ll also be less code for us to manage.

As a reference, this is what the `click #increment` event looks like:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: 5}}
    );
}
```

The only difference between this event and the `click #decrement` event though is that the `click #decrement` event has the value of the `score` field set to `-5` rather than `5`. It’s a minute difference and a lot of duplicate code.

To continue fixing our application’s functionality, create another method inside the same block as before:

```
'modifyPlayerScore': function(){
    // code goes here
}
```

Then cut and paste the `update` function from the `click #increment` event and into this new method:

```
'modifyPlayerScore': function(){
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: 5}}
    );
}
```

From there, add the `call` function to the `click #increment` event:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    Meteor.call('modifyPlayerScore');
}
```

As we did with in the previous section, we’ll need to pass the `selectedPlayer` variable through our `call` function:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    Meteor.call('modifyPlayerScore', selectedPlayer);
}
```

…and then make sure our method accepts this argument:

```
'modifyPlayerScore': function(selectedPlayer){
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: 5}}
    );
}
```

In its current form, this `modifyPlayerScore` will successfully increment a player’s score when it’s called, but let’s make a simple change so it can both increment *and* decrement a score when it’s called.

To do this, let’s pass a *second* argument through the `call` function:

```
'click #increment': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    Meteor.call('modifyPlayerScore', selectedPlayer, 5);
}
```

Then allow our method to accept this argument:

```
'modifyPlayerScore': function(selectedPlayer, scoreValue){
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: 5}}
    );
}
```

Here, we’ve created this new `scoreValue` argument that we can now reference within our method. So if we make this final change:

```
'modifyPlayerScore': function(selectedPlayer, scoreValue){
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: scoreValue}}
    );
}
```

Then we can use call the `modifyPlayerScore` function in two different ways.

If we want to increment a player’s score, we can write:

```
Meteor.call('modifyPlayerScore', selectedPlayer, 5);
```

But if we want to *decrement* a player’s score, we can write:

```
Meteor.call('modifyPlayerScore', selectedPlayer, -5);
```

The only change we’ve made to this `call` function is passing through `-5` as the second argument instead of `5`, but this completely flips the utility of the method without any additional code. Pretty slick, right?

At this point, change the `click #decrement` event from this:

```
'click #decrement': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    PlayersList.update(
        {_id: selectedPlayer},
        {$inc: {score: -5}}
    );
}
```

To this:

```
'click #decrement': function(){
    var selectedPlayer = Session.get('selectedPlayer');
    Meteor.call('modifyPlayerScore', selectedPlayer, -5);
}
```

Both the “Give 5 Points” and “Take 5 Points” buttons should now work as expected, only now with all of the data manipulation code running within the trusted environment of the server.

## 13 Structure

Considering how much progress we’ve made with the Leaderboard application, it’s strange that we haven’t talked about a seemingly fundamental aspect of building software: structure. But while learning about how to best structure your code and project files is important, I don’t think it makes a lot of sense to talk about it right away. How can you truly understand the structure of an application before you know how to build one? (Answer: You can’t.)

I’d rather help you make something as quickly (and as messily) as possible, and then talk about how to clean it up. That way, everything you read about structure will sink in without much resistance.

In this chapter, then, I’ll share a quick tour of how to structure your Meteor application. I’m not going to provide any hard and fast rules though, since:

1.  **Meteor itself doesn’t have any hard and fast rules**. There are some conventions that I’ll explain but nothing strict that you *must* do.
2.  **People are still figuring out the best practices for Meteor**. As such, it’d be silly to become too dogmatic when there’s so much more to learn.

You can also expect big changes to this chapter in the future as opinions and conventions evolve to structure Meteor applications more effectively.

### 13.1 Your Project, Your Choice

Meteor doesn’t enforce a strict file structure. It’s perfectly fine, for instance, that our project consists of just these three files:

*   leaderboard.html
*   leaderboard.js
*   leaderboard.css

We could write a much larger application and still operate from within just these three files. The code would eventually become extremely painful to manage, but it could be done.

To take advantage of this flexibility, I’d suggest keeping your projects as simple as possible as you become familiar with Meteor. Stick with just three files in a project until it becomes an inconvenience. Then let the structure naturally evolve beyond that point. This won’t make sense in a professional environment, or when working with clients – it’ll require back-tracking – but if you’re hacking together projects for your own amusement and education, structure isn’t the most pressing matter.

### 13.2 Thin Files, Fat Files

In their current form, our project files are quite *fat*. This means we’re packing a lot of code into a tight space. This isn’t always a bad thing – in some cases, a fat file will be easier to manage – but a lot of the time, it makes sense to split it across multiple files so it becomes easier to manage.

As an example, let’s consider the `leaderboard.html` file. It’s not exactly fat, but it does have a couple of templates we might like to split into other files:

*   leaderboard
*   addPlayerForm

To make the transition, start by creating a couple of new HTML files within your project’s directory. These are the file names I’ll choose:

*   leaderboardList.html
*   addPlayerForm.html

To be clear though, **the file names can be whatever you want them to be**. You don’t have to base the file names on the names of the templates. The file names could be complete gibberish if you wanted them to be since you’ll never directly reference the file names. (But clearer file names will make it easier to navigate your project.)

Next, copy and paste the template code into the appropriate HTML file. So this would be the entire contents of the `leaderboardList.html` file:

```
<template name="leaderboard">
<ul>
    {{#each player}}
        <li class="player {{selectedClass}}">{{name}}: {{score}}</li>
    {{/each}}
    <li>
        <input type="button" id="increment" value="Give 5 Points" />
        <input type="button" id="decrement" value="Take 5 Points" />
        <input type="button" id="remove" value="Remove Player" />
    </li>
    <li>
    {{#if showSelectedPlayer}}
        Selected Player: {{showSelectedPlayer.name}}
    {{/if}}
    </li>
</ul>
</template>
```

…and this would be the entire contents of the `addPlayerForm.html` file:

```
<template name="addPlayerForm">
{{#if currentUser}}
    <form>
        <input type="text" id="playerName" />
        <input type="submit" value="Add Player" />
    </form>
{{/if}}
</template>
```

You can then freely remove the original template code from the `leaderboard.html` file, meaning the `leaderboard.html` file will now resemble:

```
<head>
    <title>Leaderboard</title>
</head>
<body>
    {{> loginButtons}}
    <h1>Leaderboard</h1>
    {{> leaderboard}}
    {{> addPlayerForm}}
</body>
```

But what about these tags that reference our templates? Don’t we have to do something special to make sure that Meteor can recognise what these tags are actually referencing now that we’ve moved the template?

Nope.

As long as your templates are somewhere in your project folder, Meteor can figure out where they are. The same applies to all code within your project. You don’t have to precisely worry about where it is (aside from a few conventions that I’ll explain in a moment). To simplify the JavaScript file, for instance, we could create these files:

*   helpers.js
*   events.js
*   methods.js

Then split our helpers, events, and methods across them so our code is easier to manage. Once again, the file names are irrelevant, but let’s talk about a few of the conventions to keep in mind.

### 13.3 isClient

Inside our `leaderboard.js` file, there’s a lot of code within the `isClient` conditional, and if we start splitting our code across multiple files, placing all of it inside `isClient` conditionals is not the most elegant approach.

To avoid such a horrible fate, Meteor has provided a simple convention: **any code placed within a folder named `client` will only run on the client**.

To illustrate this:

1.  Open the `leaderboard.js` file.
2.  Cut all the code between the `isClient` conditional.
3.  Paste this code into a new file (without the conditional).
4.  Save this file into a folder named `client`.

You should have a project that looks a little something like this:

![The addition of the `client` folder.](images/00068.jpeg)

The addition of the `client` folder.

Based on this change, nothing will be overtly different about our application, but it’s a starting point for splitting our application into modular chunks.

For example, we could split this new file we’ve created in a couple of different files, like so:

*   helpers.js
*   events.js

If these files are both in the `client` folder, then we won’t need to use that `isClient` conditional in both (or either) of them.

But another approach would be to create a JavaScript file for each template in our applications, like this:

*   leaderboardList.js
*   addPlayerForm.js

Then we could have all of the events and helpers associated with the “leaderboard” template inside the `leaderboardList.js` file, and all of the events and helpers associated with the “addPlayerForm” template inside the `addPlayerForm.js` file.

Is this the best way to handle things?

Again, I don’t want to offer a definitive answer because it will depend on what you’re building and also on the scope of what you’re building. What’s important to know for the time being is that:

1.  You can split your files in these ways.
2.  You can avoid an abundance of `isClient` conditionals.

What you do with this knowledge will inevitably involve some experimentation.

### 13.4 isServer

Similar to the convention we just discussed, **any code placed within a folder named `server` will only run on the server**. The same rules apply, so I won’t repeat myself too much. Just follow the same steps from before:

1.  Open the `leaderboard.js` file.
2.  Cut all the code between the `isServer` conditional.
3.  Paste this code into a new file (without the conditional).
4.  Save this file into a folder named `server`.

You’ll then have a project that looks a little something like this:

![The addition of the `server` folder.](images/00069.jpeg)

The addition of the `server` folder.

The application will continue to function as expected, but there won’t be a need to place the server-side code within `isServer` conditionals.

### 13.5 Other Conventions

At this point, the default `leaderboard.js` file should only have the following line of code inside of it:

```
PlayersList = new Meteor.Collection('posts');
```

This line of code can remain where it is but it’s worth mentioning that:

1.  You *shouldn’t* put this code inside the `client` or `server` folder since we need this collection to run on both the client and the server.
2.  It’s common for Meteor developers to create a “collections” folder and create a separate file for each of their collections. This is not an official convention though and has no special meaning.

There are also other conventions for structuring a Meteor application but, since these conventions have no use with our Leaderboard application, I won’t dive into detail.

If you’re particularly curious about structure though:

*   [Read the “Structuring Your App” section of the official documentation](http://docs.meteor.com/#structuringyourapp).
*   Check out [these](http://tech.exponential.io/meteor/building-large-modular-apps-meteor/) [three](http://stackoverflow.com/questions/10122977/what-are-the-best-practices-for-structuring-a-large-meteor-app-with-many-html-te) [resources](https://github.com/Differential/docs/blob/master/METEOR-STANDARDS.md) for further opinions and insight.

I might discuss structure in more detail in a future update but Leaderboard is such a simple application that it’d be silly to spread it thinner than we already have. I’ll also continue to argue that it’s not the most pressing matter and your time is better spent hacking together a few messy projects before worrying about the best practices.

## 14 Deployment

To share our creation with the world, we need to *deploy* it to the web. This, unfortunately, isn’t so simple as just uploading our project to a web host.

In a future update to this book, I’ll detail a range of deployment options – along with advantages, disadvantages, and other things to consider – but for the moment, let’s deploy to the official Meteor.com servers. This has the advantage of being:

*   Free.
*   Quick.
*   Easy.

It won’t be enough for an application with more than a handful of users, but it’ll be enough for sharing prototypes with friends, family, and other developers when you’re looking for feedback.

To begin, switch to the command line and write:

```
meteor deploy APPLICATIONNAME.meteor.com
```

Here, we’re using this `deploy` command and then specifying the name that will be used in the URL for our Meteor application.

After tapping the “Return” key, your project will be bundled together into a single file and uploaded to the Meteor.com servers.

You’ll see something like the following in the command line:

![Deployed.](images/00070.jpeg)

Deployed.

This is all it takes to get a Meteor application deployed to the web (for the purpose of sharing prototypes, at least).

To host your Meteor application with a custom domain name, use the following command during deployment:

```
meteor deploy YOURDOMAINNAME.com
```

Then, afterward, set the CNAME of that domain name to `origin.meteor.com`. If you’re unsure of how to set the CNAME of a domain name, here are guides from a few popular domain name registrars:

*   [NameCheap](https://www.namecheap.com/support/knowledgebase/article.aspx/1031/2/demo-how-to-set-up-a-cname-record)
*   [GoDaddy](http://support.godaddy.com/help/article/680/managing-dns-for-your-domain-names)
*   [Hover](https://help.hover.com/entries/21204757-How-to-Edit-DNS-records-A-CNAME-MX-TXT-and-SRV)

If you’re looking for a more long-term deployment solution, I’d suggest a using:

*   [Digital Ocean](https://www.digitalocean.com/?refcode=125faab8c8c8) to host the application.
*   [Meteor Up](https://github.com/arunoda/meteor-up) to deploy to Digital Ocean.

As this is just the start of your Meteor journey though, it’s a good idea to not to “jump the gun” and by rushing something to release. You don’t have to immediately launch something for all the world to see. Give yourself some time to enjoy Meteor for the sake of creation. Then you can have all of the fun and (basically) none of the stress.

## 15 Conclusion

It feels strange to write a conclusion because, honestly, I’m just getting started. You’ve now read the first draft of *Your First Meteor Application*, but it’s the first of many drafts that I plan to publish in the coming years.

For future editions, the scope of the book will remain similar, but:

*   Every chapter will be heavily revised (from scratch).
*   Explanations will be more detailed (but still without bloat).
*   Errors will be aggressively obliterated.

There’ll also be new features added to the book, including:

*   A “Summary” section at the end of each chapter to reiterate the main points from within that chapter.
*   An “Exercises” section at the end of each chapter to give readers something extra to do when they’ve finished reading the chapter (or the book).
*   Source code files so you’re able to more easily see how exactly the project’s code should look at each stage of development.

And, as always, I’m curious to hear what *you* want to see from the book, so feel free to send an email to [hello@meteortips.com](mailto:hello@meteortips.com) and I’ll get back to you shortly.

That’s basically it for now though. There’s a lot of work ahead, so I guess I should go back to writing.

Talk soon,<br /> David Turnbull

P.S. If you’re wondering where to go from here, checking out [the tutorials section on the blog](http://meteortips.com/tutorials) is a good place to begin.