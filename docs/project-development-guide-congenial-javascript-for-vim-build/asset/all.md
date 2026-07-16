![](Image00000.jpg)

ProjectDevelopmentGuide  Congenial JavaScript for Vim Build your portfolio with this comprehensive guide to Developing the Congenial-JavaScript Plugin for the Vim text-editor.Prerequisite: Basics of Vim and JavaScriptProjectRay Voice
The Project Development Guide to Congenial-JavaScriptPublished Independently by Ray Voice.Copyright © 2020 Ray Voice. All rights reserved.All rights reserved. This book or parts thereof may not be reproduced in any form, stored in any retrieval system, or transmitted in any form by any means—electronic, mechanical, photocopy, recording, or otherwise—without prior written permission of the publisher, except as provided by United States of America copyright law. Requests to the copyright owner for permission should be addressed to the author at [rayvanet@gmail.com](mailto:rayvanet@gmail.com) .Disclaimer: The information in this book was correct at the time of publication, but the Author does not assume any liability for loss or damage caused by errors or omissions. The Author or any other persons involved in the production of this book cannot be held responsible for any of the damages, liability, or misrepresentation. To maintain the anonymity of the individuals involved, some names and details have been changed. Some sample scenarios in this book are fictitious. Any similarity to actual persons, living or dead, is coincidental.LIMIT OF LIABILITY/DISCLAIMER OF WARRANTY: THE PUBLISHER AND THE AUTHOR MAKE NO REPRESENTATIONS OR WARRANTIES WITH RESPECT TO THE ACCURACY OR COMPLETENESS OF THE CONTENTS OF THIS WORK AND SPECIFICALLY DISCLAIM ALL WARRANTIES, INCLUDING WITHOUT LIMITATION WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE. NO WARRANTY MAY BE CREATED OR EXTENDED BY SALES OR PROMOTIONAL MATERIALS. THE ADVICE AND STRATEGIES CONTAINED HEREIN MAY NOT BE SUITABLE FOR EVERY SITUATION. THIS WORK IS SOLD WITH THE UNDERSTANDING THAT THE PUBLISHER IS NOT ENGAGED IN RENDERING LEGAL, ENGINEERING, OR OTHER PROFESSIONAL SERVICES. IF PROFESSIONAL ASSISTANCE IS NEEDED, THE SERVICES OF A COMPETENT PROFESSIONAL PERSON SHOULD BE SOUGHT. NEITHER THE PUBLISHER NOR THE AUTHOR SHALL BE LIABLE FOR DAMAGES ARISING HEREFROM. THE FACT THAT AN ORGANIZATION OR WEBSITE IS REFERRED TO IN THIS WORK AS A CITATION AND/OR A POTENTIAL SOURCE OF FURTHER INFORMATION DOES NOT MEAN THAT THE AUTHOR OR THE PUBLISHER ENDORSES THE INFORMATION THE ORGANIZATION OR WEBSITE MAY PROVIDE OR RECOMMENDATIONS IT MAY MAKE. FURTHER, READERS SHOULD BE AWARE THAT INTERNET WEBSITES LISTED IN THIS WORK MAY HAVE CHANGED OR DISAPPEARED BETWEEN WHEN THIS WORK WAS WRITTEN AND WHEN IT IS READ.Outline[Introduction](#text00005.html_a2BJ)[About Authors](#text00007.html_a2AP)[Author’s Acknowledgments](#text00008.html_a2D5)[Chapter 1 - Development of the Initial Idea](#text00009.html_a2D6)[Chapter 2 - Initiating the project](#text00024.html_a2BT)[Chapter 3 – Programming the Software](#text00027.html_a2BZ)[Chapter 4 – Advanced Features](#text00056.html_a2CJ)[Chapter 5 – Functional Programming Code for JavaScript](#text00068.html_a2AA)[Chapter 6 - Post-development work, Writing documentation, and Making a pull request](#text00069.html_a2A5)[Chapter 7 - Making the plugin presentable for the portfolio](#text00078.html_a2BK)[Kanban Board](#text00081.html_a2BP)Table of Contents[Introduction](#text00005.html_a2BJ)[Prerequisites](#text00006.html_a2CW)[About Authors](#text00007.html_a2AP)[Author’s Acknowledgments](#text00008.html_a2D5)[Chapter 1 - Development of the Initial Idea](#text00009.html_a2D6)[Development Process](#text00010.html_a2D4)[Initial Idea](#text00011.html_a2AY)[Forensic Programming](#text00012.html_a29N)[The General outline](#text00013.html_a2B0)[Development Features](#text00014.html_a2BF)[Project Requirements Mockup](#text00015.html_a2A1)[Our Project Requirements (abstract)](#text00016.html_a2CA)[Our Project Requirements (Official)](#text00017.html_a2BY)[Scaling down the demands](#text00018.html_a2D7)[Proof-of-Concept and Beta-testing](#text00021.html_a2CD)[Setting up a Project Management System](#text00022.html_a2BG)[Modules](#text00023.html_a29T)[Chapter 2 - Initiating the project](#text00024.html_a2BT)[Initializing the project](#text00025.html_a2D8)[Dividing up Duties](#text00026.html_a2AB)[Chapter 3 – Programming the Software](#text00027.html_a2BZ)[Fundamentals of VimScript](#text00028.html_a29W)[Program to Generate a Variable](#text00029.html_a2AM)[Write](#text00030.html_a2C0)[Test and Debug (AddToDoc)](#text00031.html_a2D2)[Explanation](#text00032.html_a2AV)[Test and Debug (GenerateVariableWithScope)](#text00035.html_a2D1)[Program to Generate a label](#text00036.html_a2AS)[Write](#text00037.html_a2AJ)[Test and Debug](#text00038.html_a29S)[Program to Generate a For Loop](#text00039.html_a2CE)[Write](#text00040.html_a2A2)[Test and Debug](#text00041.html_a2BM)[Program to Generate an Array](#text00042.html_a2CZ)[Write](#text00043.html_a2CP)[Test and Debug](#text00044.html_a29B)[Program to Generate Array methods](#text00045.html_a2AD)[Write](#text00046.html_a2A6)[Test and Debug](#text00047.html_a2AE)[Program to Generate Timer Loop](#text00048.html_a2CT)[Write](#text00049.html_a2B2)[Test and debug](#text00050.html_a2B3)[Program to Generate Stdout logs](#text00051.html_a29M)[Write and Test](#text00052.html_a2A3)[Program to Generate Loops to Iterate over Arrays (For-Each)](#text00053.html_a2BH)[Write, Test and Debug](#text00054.html_a299)[Note](#text00055.html_a2B7)[Chapter 4 – Advanced Features](#text00056.html_a2CJ)[Basic features](#text00057.html_a2BS)[NodeJS](#text00058.html_a2C2)[Built-in Variables](#text00059.html_a2AT)[Process props](#text00060.html_a2AU)[Events](#text00061.html_a2BR)[Refactoring code](#text00062.html_a2C3)[Custom Events Emitter](#text00063.html_a2CG)[Creating a Server with HTTP code](#text00064.html_a2BU)[FS module code](#text00065.html_a2BN)[JavaScript Require() and Export](#text00066.html_a2D0)[Basic Express Server Tools for NodeJS](#text00067.html_a2AR)[Chapter 5 – Functional Programming Code for JavaScript](#text00068.html_a2AA)[Chapter 6 - Post-development work, Writing documentation, and Making a pull request](#text00069.html_a2A5)[Post-development work](#text00070.html_a2C1)[Refactoring Comments](#text00071.html_a2BX)[Writing Documentation](#text00074.html_a2C6)[Making a pull request](#text00075.html_a29K)[Steps To Install the package](#text00076.html_a2AZ)[Steps to make modification and make a pull request](#text00077.html_a2D3)[Chapter 7 - Making the plugin presentable for the portfolio](#text00078.html_a2BK)[Adding ASCIINEMA casts to your project](#text00079.html_a29J)[Recording an ASCIICAST and putting it on GitHub](#text00079.html_a2CY)[Other suggestions](#text00080.html_a2CR)[Kanban Board](#text00081.html_a2BP)Introduction​ This book is a comprehensive guide for developing the notorious Congenial-JavaScript Plugin for Vim. This book takes the reader through six comprehensive yet concise steps to develop and present your software, starting from developing the initial idea behind the program, all the way to the final distribution and future development phases.​ The book includes the following steps to development:

1.  Development of the initial idea.
2.  Initiating the project, including Team Member Role Initialization.
3.  Programming and Coding the Software, including writing unit tests for Vim using by building a custom testing framework.
4.  Writing documentation.
5.  Making the plugin presentable for your portfolio. Heavy focus on the 3-Rs of Elegant Programming (Readability, Re-usability, and Refactoring).
6.  Final distribution including putting your work in front of other people including potential employers for peer-review.

​ A very concise and straightforward manner has been taken to present this book, with detailed steps and explanations for even the smallest possible things.​ It will be my intention to keep nothing off-screen; so nothing will happen off-screen, from writing the first line of code to Refactoring and Rewriting, everything will be thoroughly documented in a reader-friendly manner.​ Once you develop the project, you can even use it in your portfolio.The original project is MIT Licensed; please add credit aka “Public-attribution” in your source code to the original author (Ray Voice).​ The book is written from a solo-coder/project manager point of view, hence it will be easy to go over alone, and it will prepare you for becoming part of a larger team.Prerequisites​ To go over this book, all you need is to know is the following:

1.  Basics of Vim, like what is Normal Mode, Insert Mode, etc. Some VimScript/VimL is also worth knowing.
2.  Basics of JavaScript. We don’t use any JavaScript in this book but we are developing an aid for coding in JavaScript.
3.  Basics of Programming. You need to know stuff like variables, functions, importing, etc. If you know JavaScript then this should be a breeze.

​ You can acquire all these prerequisites by reading the following books, however it’s not required to read them if you know what you are doing.Simply Vim : A Comprehensive Guide to Mastering the Vim text-editor – Ray VoiceSimply Web Development : An introduction to the world of Web development – Anna Voice and Ray VoiceSimply ES6 : Mastering JavaScript and ES6 to its fullest – Ray Voice and Anna (For Advanced JavaScript)About Authors![](Image00002.jpg)Ray Voice is a Mathematician, Computer Researcher, Software Developer, Serial Entrepreneur, and Bestselling Author. He is the MD, and CEO of “Ray & A Group Solutions”, a Technology Business Consultation firm based in Asia, with clients all around the world. He is also the Founder and Director of “Technology Application, Research, and Development Initiative Stratagem” aka “TARDIS”, a cleverly named R&D facility whose primary purpose is to make the world a better place by developing the technology of tomorrow. Members come from all walks of life. Much of the work done by them is Open Source and uses MIT, and BSD licenses. A big chuck of funding for their R&D operations comes from conducting training seminars and workshops.Twitter: @RayShortHeadAuthor’s AcknowledgmentsThe following people were involved in the development of this book, without them this book wouldn’t have been possible.Anna Voice (editor)Siena Dahl-Joy (contributor)Ospan Ali (stock image)All of them have my thanks.Chapter 1 - Development of the Initial Idea​ In this chapter, we will start working on the initial idea of the project. We’ll take a walk through the development process, then we will dive right into stuff like mock designs and proof-of-concept development, and finally we do some market testing.Development Process​ Here is the thing, I believe that once the initial Idea and the Team of Developers is in place it’s the process that influences the ultimate success of a project! Hence, it’s very important to get the process right before getting ahead of the development.​ Small and Lean Startups have the advantage of using unique development processes for each project, this can be really good for the project if the person leading the project knows what they are doing. However, this model is not really scalable in most cases, it’s better to use Agile methods like Kanban or Scrum.​ The development process of this project will be kept lean enough so one person can follow it. The process will look like the following:

1.  A General Idea will be written down in a clean and straightforward manner without external help.
2.  A collection of requirements and their timeline will be listed for the project. This type of document is usually given to your financial backer or whomever is in-charge of inventory/accounts management for your project. This must be done right, since this will be use to draw up a runway timeline for your startup/company. A trained accountant with IT experience can save you a significant amount of cash.
3.  A Mock and a Proof-of-Concept is built to share with other team members, usually the developer who envisioned the program builds this with little to no external help.
4.  An internal market testing session of the Proof-of-concept is done with the team members and some external individuals. This is a very critical time as this may set up the tone for a lot of future stuff.
5.  A project management system like SCRUM is set-up for larger projects, while for smaller projects like this one a single person can micro-manage a hand full of developers.
6.  The project is initiated and a Repository is shared with all team members. In my projects, I force everyone to use a hierarchy management system where they can only commit code to their own Repo, and can only merge it with their supervisor’s repo. Each person thoroughly reviews the work of their subordinates before they merge it to the origin Repo.
7.  Briefings are held among the team members to divide duties. In this part, I develop and review Kanban boards with my team. This can also be done as part of SCRUM.
8.  The actual programming section of development is started.
9.  Final touch-ups including beta-testing is done.
10.  The project is pushed to the master repo where it’s distributed to the users as one of the following:
    1.  Update to their already existing software.
    2.  Upgrade to their current version.
    3.  Rolling release, which is sort of like an update.
    4.  Live version, which means the users are always using the latest version.
11.  A launch party or ritual is usually held.

​ If these steps overwhelm you then don’t worry at all! We won’t be performing certain steps like step #10, and I’m certainly not throwing you a party!Initial Idea​ Every project has an inspiration, there is always a need the developer is trying meet, or a gap they are trying to fill. The Congenial-coding practices sprung out of the following needs:

1.  I have carpel tunnel! I can’t type much, so I have to rely on dictation, speech-to-text programs, and programs like Emmett-vim to help me code.
2.  I code in many languages, I have worked as a Forensic Programmer for a really long time, so forgetting syntax of a programming language is a grave sin in my life, but it still happens from time to time.

Forensic Programming​ I describe myself as a Forensic Programmer, as a Forensic Programmer I diagnose problems in software, source-code, UI/UX, etc. and fix them; I make sure they don’t occur again in an unpredictable manner. The initial idea is much like Bug Bounty hunting, in fact bug hunting is a part of the job, however Forensic Programming is broader and has different goals.​ As a Forensic Programmer, I have worked with many programming languages, libraries, and frameworks, editors, people, etc. including but not limited to the following:

1.  JavaScript
2.  TypeScript
3.  ReactJS and React-Native
4.  C, C++, C#, Go, and OpenCL
5.  Lua
6.  Common Lisp
7.  Java, Kotlin, and Scala
8.  FORTRAN, Alef, and Limbo (one time)
9.  Python
10.  MATLAB, Octave, BRL-CAD, etc.
11.  Sh/BASH Shell, BASIC, and DOS batch
12.  Haskell
13.  Curl
14.  Swift
15.  Rust
16.  AWK
17.  Dart for Flutter
18.  PHP and SQL
19.  Ruby
20.  Perl
21.  Zig and Racket
22.  BrainFuck and Shakespeare (for fun)

​ The list turned out to be longer then I thought! However my point is that we (yes, there are other Forensic Programmers like me) can’t really remember proper syntax for all of these languages, for this reason we need a plugin to help us through it.The General outline​ So, what I needed is a program that has the following features:

1.  It allows me to write hundreds of lines of code with the least amount of typing.
2.  It should help with the syntax of the language.
3.  It should be intuitive enough so I don’t forget how to use it, otherwise what’s the point!

Development Features​ The program also needs some silent aka development features.

1.  It needs to be easily adaptable to languages other than JavaScript so I can port it for other languages.
2.  It should be uniform and in conduct to all languages, for example a command to declare a variable should be same in JavaScript and C language, but it’s output will obviously be different.
3.  It needs to be blazing fast; any plugin that slows down Vim is not worth it.

Project Requirements Mockup​ I will be developing this project without much external help; however, I will still show you how it’s done so you have at-least some idea of how a firm works.​ Before development begins we need a budget for the development periods, someone from the financial depart clears the budget and then the project manager has full control of it!Although the following is usually not the case, I have worked with teams where the financial department never gives up control of the budget, this in turn harms the project to a great extent; one of the worst thing you can do to someone is to give them a responsibility but don’t actually give them the power to carry it out.Our Project Requirements (abstract)Let’s make a list of things we need to develop this project.

1.  We need some people who can code in VimScript.
2.  We need someone to write unit tests and generate reports on development using VimScript, Python, etc.
3.  We need someone to write the documentation, this requires a separate skill-set. Documentation’s written by programmers make readers suicidal.
4.  We need some people to beta-test our software.
5.  We are assuming that we have the room and equipment to develop the project.

Our Project Requirements (Official)​ While we have our list of initial requirements, we can’t send a rough list like the one presented above to the financial department, they need clear guidelines to calculate the budget. We need to develop an official list that describes the precise quality and quantity of the labour and budget we are demanding. Following is a more formal version of the list:

1.  VimScript coders x2-x4.
2.  VimScript coder with experience in writing unit tests.
3.  A coder with experience in writing documentation.
4.  Budget for impartial focus-groups.
5.  Intra-development budget of $200 for additional payroll, petty-cash, equipment maintenance, etc.

​ Now this is a good official document! Although the 5th point will infuriate some people. The official document will look something like the following:![](Image00003.jpg)Note: This is only a mock document.​ Once this document is delivered usually there is some negotiation, however a project manager mustn’t make any claims they can’t deliver, and should never budge on reasonable requests.​ Remember, setting improbable goals on low budgets is very harmful for the project, and can be very harmful to the reputation of people associated with that project.Scaling down the demands​ Sometimes we don’t have all the resources or the budget to develop a project at large scale, if this is the case we can take the following approaches:The Lean Entrepreneur approach

1.  Instead of using multiple coders and a separate coder for writing unit tests, we hire a small duo to do the job and test each other’s work. This can prove to be disastrous in large-scale projects. It’s also smart to outsource some stuff.
2.  Give the role of documentation writer to a low-paid Intern.
3.  Instead of booking Focus-groups use organic feedback from the figurative “friends and family”.

The Broke Entrepreneur approach

1.  DIY some of the program including the unit tests, put the rest on GitHub, GitLab, BitBucket, etc. for others to contribute
2.  Partially write the documentation yourself, and put the rest on GitHub for others to contribute.
3.  Share the program online with others; you can get some pretty great (hurtful) feedback this way. Just keep an open mind and ironclad nerves.

Proof-of-Concept and Beta-testing​ I will be taking on the role of your Project Manager, and I’ve written a proof-of-concept for you. The code is provided below, put it in your “.vimrc” file and you will be able to test the proof of concept yourself:1  “ start of the proof-of-concept code2   function ! Append (dataToAppend) abort3      execute 'normal i' .a:dataToAppend4    endfunction5   6   function ! GenerateVariable () abort7     let scope = input ( 'var/let/const Pick 1/2/3: ' )8     let scopeOptions = [ 'var' , 'let' , 'const' ]9      let scopeRes = scopeOptions [ scope -1]10   11    let name = input ( 'Name of Variable: ' )12    let value = input ( 'Value of Variable: ' )13    14    call Append ( scopeRes . ' ' . name . ' = ' . value . ';' )15 endfunction1617 nnoremap ,var :call GenerateVariable ()<cr>18 “ end of codeNote: You don’t need to know what this VimScript code does for now, basic VimScript stuff like making variables and functions will be explained in this book at a later stage.Warning: Don’t copy/paste code, type it out by hand.​ After adding this code to your “.vimrc” file and debugging any installation problems (if any) we can test the proof-of-concept using the following steps:

1.  Make sure the code you appended to your “.vimrc” file is proper. Windows users can use something like `:echo $HOME ` to find their HOME directory.
2.  Open a new file in Vim by using the command `vim ` from the Terminal.
3.  Once in a new file use `,var ` in Normal-mode to see the magic. This command is used to declare variables in JavaScript and control their scope.
4.  The system will ask you for the “scope” of the variable, you can press 1, 2, or 3 for var, let, or const, then press Enter. For the first testing, write 1 and then press Enter.
5.  The system will ask you for the “name” of the variable. Give it a name, then press Enter. For the first testing name the variable “player1Health” and then press Enter.
6.  Lastly, the system will ask you for the variable value, you can pass it a value like 1, 200, 31, true, false, “JavaScript”, “Hello World”, etc. quotations are required for strings. For the first testing, write 100 as the value and then press Enter.
7.  If you did everything right you should see the following appear in your document:

var player1Health = 100;

8.  If you see it then congratulations you just screened the initial concept behind the program.
9.  Now you should pass around the program for others to test. Iron out any problem with the concept before moving on.
10.  Now you need to develop a version of this program that is actually useful and can be mass distributed.
11.  Before moving on remove the proof-of-concept code from your `.vimrc` file.

Setting up a Project Management System​ For this project, I have given you a simple project management system to deal with the project. The system is comprised of 5 steps:

1.  B acklog
2.  W rite
3.  T est and Debug
4.  Problem
5.  D one

It will look like this on a Kanban Board:![](Image00004.jpg)​ I will give you a backlog of features to implement in the code, the features will be given in form of cards/stories. For example, it will look like the following on a Kanban Board:![](Image00005.jpg)​ In the Write step you will pick up a module/feature card from the backlog, move it from Backlog column to Write column, and code it. Assuming that you picked “Feature A”, the Kanban Board will look like the following:![](Image00006.jpg)​ In the Test step, you will pick up a feature card from the write column and put it under the “Test and Debug” column, perform tests on that feature, and debug code if required. If you pick “feature A” then the board will look like the following:![](Image00007.jpg)​ When you are done developing “Feature A” you will move it’s card to the “Done” column, and then you will have some personal bandwidth available to start working on another feature from the Backlog.​ The Problem column is for stuff that doesn't belong in any other column, leave a card there with a note if needed.​ Using the Kanban method you can assign each team/teammate a single column to work with, also called Vertical assignment, or you can assign a single feature to a team/teammate and he/she will take it through each column until it’s in the Done column, also called a horizontal assignment.​ Each team has it’s own assignments, and their own sub-Kanban boards.​ The hierarchy in my projects using a lingo where the central board is known as the Origin-Board, and the sub-boards are known as the Macro-Boards, the sub-sub-boards, are called Meso-Boards, and the sub-sub-sub-boards are called Micro-Boards. However, this is obviously made up lingo! The idea is to conserve the superiority of the superior boards, so a Meso-Board will never be out of sync with a Micro-Board. I did all this because I don’t like people touching my Origin-board, make of it what you will!​ A template of this Kanban Board is provided at the end of this book, you can print it out for your own use.​ You can also use a program like Task Warrior for solo, mono-tonal project management.Modules​ Following is a list of modules we need to work on:

1.  congenial-JavaScript.vim (Yellow)
2.  modules/sourceCodeGenerator.vim (Green)
3.  docs/outline.txt (Blue)

​ Each module can be assigned a card-color, and then the backlog can be filled with features that will be implemented in those modules. I have already create the following Backlog for you; we’ll start working on it after the next chapter.![](Image00008.jpg)Chapter 2 - Initiating the project​ In this chapter, we will initialize the project’s origin Repository, share a Repo with all members, and then divide up duties with our co-developers.​ You can initialize your project with Git if you want, although it’s not required. You can use Git or any other Version Control System; the usage of Version Control Systems is heavenly recommended, but don’t use them unless you are familiar with them.​ Instructions for Version Control are not provided here, so steps for checking-out, merging, pushing, etc. will not be given, you are to deal with Version control yourself, if you don’t know how then avoid it for now, this is a small project.​ Instructions for making files like `contributors.md`, LICENSE, `README.md`, etc. are not provided since they are not required in personal projects, but if you put your project’s on GitHub you can provide these files.Initializing the project​ Following are the steps we will take to initialize the project:

1.  Make a directory named `congenial-JavaScript` in your HOME directory.
2.  Inside congenial-JavaScript make the following directories :
    1.  docs
    2.  modules
3.  Inside congenial-JavaScript make the following files :
    1.  congenial-JavaScript.vim
    2.  docs/outline.txt
    3.  modules/sourceCodeGenerator.vim
4.  Go to your ~/.vim/after/ftplugin/javascript/ directory, if it doesn't exist, or if any of it’s parent directories doesn't exist then make them.
5.  In this directory make a symbolic link aka shortcut for your congenial-JavaScript directory made in step #1\. Use the command:

ln -s ~/congenial-JavaScript congenial-JavaScript

6.  Now in ~/.vim/after/ftplugin/javascript/ make a file named `plugins.vim`. This file is used to activate plugins for JavaScript files. The plugins are to be imported in `plugins.vim` like in step #8.
7.  Now you should have the following layout of directories for `.vim` and `congenial-JavaScript`:

~/|_ .vim/| |_ after/| | !_ after/| |   !_ ftplugin/| |     |_ javascript/| |     | |_ congenial-JavaScript/| |     | !_ plugins.vim (for activating plugins)| |     |_…| |_ autoload/| |_ colors/| |_ ftplugin/| |…|_ .vimrc (for vim code, not relevant to us)|_ congenial-Javascript/| |_ congenial-JavaScript.vim (central plugin file)| |_ docs/| | !_ outline.txt (congenial-JavaScript docs)| !_ modules/|   !_ sourceCodeGenerator.vim (important module)|_…

8.  Inside `plugins.vim` add the following lines of code and save it:

1   " This is a file with a list of plugins activated for JavaScript2   " The syntax is to write the name of a plugin followed my sourcing that plugin's central file3  " The program congenial-JavaScript was originally developed by RayVoice “GitHub/Ray6464” “@rayshorthead” “rayvanet@gmail.com” on MIT License4   " congenial-JavaScript5   so ~/.vim/after/ftplugin/javascript/congenial-JavaScript/congenial-JavaScript.vim

9.  The code on line#5 practically imports the `congenial-JavaScript.vim` script in the `plugins.vim` script. You can add other plugin you develop in this file too.
10.  When we open a JavaScript file in Vim it will execute `plugins.vim`, which will activate the congenial-JavaScript plugin.
11.  Now project initiation is complete.

Dividing up Duties​ Now let’s divide up the duties of development, as I have promised you that nothing will happen off-screen, I have contacted my friend Siena to get involved in this project, and the following was her response:![](Image00009.jpg)​ Unfortunately, I can’t really share the actual pictures from a private forum, but the conversation went like this:

1.  I sent her the proof-of-concept to test and she liked it.
2.  I told her about the stuff I needed to cover, like making variables, loops, etc. and promised to send a full list later.
3.  She and I agreed to set up a system of communication, we basically agreed to a type of communication where we will set up an online Git controlled private remote Repo, I will write code for implementing the required features, and she will write tests for those features in a FIFO (first-in-first-out) fashion and push/upload them to the remote Repo. However I will write at-least one test for the sake of demonstration.

​ Let’s start the development!Chapter 3 – Programming the Software​ In this chapter, we will cover the basics of VimScript, followed by the actual programming of our software, and then testing. The Write/Test cycle will be repeated for each feature until a satisfactory number of features are covered.​ To get my point across we've have kept the coding sections concise, if you are having any problems than consider increasing your exposure to VimScript.Fundamentals of VimScript​ In the following list the basic features of VimScript are described, this is not meant to be a tutorial. Anyone with some programming experience should be able to understand this.

1.  The `so` keyword is short for source, it practically imports a script in to another script, however this definition isn’t literal. Importing works differently in VimScript.
2.  The `nnoremap` keyword tells Vim to create a bond between a key-sequence and a command in Normal-mode.
3.  The `inoremap` keyword tells Vim to create a bond between a key-sequence and a command in Insert-mode.
4.  The `function!` keyword is used to start writing a function, and the `endfunction` keyword is used to end it.
5.  The `echo` keyword is used to log stuff to Vim.
6.  The `let` keyword is used to declare and reassign variables.
7.  The `call` keyword is used to call functions.
8.  The `abort` keyword at the end of the function declaration is for aborting a function’s process if an error occurs.
9.  Further explanations will be given when needed, but only brief ones, for a full guide on Vim and VimScript use the following book.

Simply Vim : A Comprehensive Guide to Mastering the Vim text-editor – Ray VoiceProgram to Generate a Variable​ In JavaScript we have 3 kinds of basic variables, they are declared with the `var | let | const` keywords. The variables control the scope of access and mutability of values, however that is all irrelevant here! We only need to code it.​ Each module will go through the write/test cycle followed by explanations.Write​ Follow these steps to write the first feature:

1.  Inside `congenial-JavaScript.vim` add the following lines of code and save it:

so ~/.vim/after/ftplugin/javascript/congenial-JavaScript/modules/sourceCodeGenerator .vim

2.  Add the following code to your `congenial-JavaScript.vim` file too:

nnoremap ,var :call GenerateVariableWithScope()<cr>

3.  Add the following code to your `modules/sourceCodeGenerator.vim` file:

1  " The program congenial-JavaScript was originally developed by RayVoice “GitHub/Ray6464” “@rayshorthead” “rayvanet@gmail.com” on MIT License2   function ! AddToDoc(dataToAdd) abort3       execute 'normal i' .a:dataToAdd4   endfunction56   function ! GenerateVariableWithScope() abort7     let sSel = input( 'var/let/const Pick 1/2/3: ' )8     let sOps = [ 'var' , 'let' , 'const' ]9      let sStd = sOps[sSel-1]1011    let vName = input( 'Name of Variable: ' )12    let vVal = input( 'Value of Variable: ' )1314    call AddToDoc(sStd. ' ' .vName. ' = ' .vVal. ';' )15 endfunction

4.  In this code we have used abbreviations to fit the code in the page, however to avoid confusion I suggest you reverse the abbreviations, so instead of “sSel” write “scopeScelection”. Following is a list of abbreviations:
    1.  sOps = scopeOptions
    2.  sStd = scopeSelected
    3.  vName = variableName or varName
    4.  vVal = variableValue or varValue
5.  Remember that Readability is very important to code, make sure your code is readable like a story. In the latter chapters, I will show you how to write clean and readable code that reads like a story.
6.  Now after saving both files, make a file named “something.js”. In Vim you can use `:e something.js`.
7.  Now in Normal-mode in `something.js` use `,var `, almost immediately Vim should ask you the following questions:
    1.  Scope
    2.  Name
    3.  Value
8.  Give it the Scope value: 1
9.  Give it the Name value: health
10.  Give it the Value value: 100
11.  Now you should see the following:

var health = 100;

12.  If everything is working then congratulations, if not then debug your code. VimScript is very easy to debug, help can easily be found online, you can also raise an issue on GitHub at `Ray6464/congenial-JavaScript`.

Test and Debug (AddToDoc)​ The following instructions will teach you how to test the `AddToDoc()` function shown in step #3 of the previous section.

1.  In your `modules` directory make a file named `tests.vim`.
2.  Inside `congenial-JavaScript.vim` add the following lines of code and save it:

so ~/.vim/after/ftplugin/javascript/congenial-JavaScript/modules/tests .vim

3.  In the `tests.vim` file add the following code:

1   function ! Report(functionName) abort2      echo "Report: The Function [" . a:functionName . "] is working.     (PASS)"3   endfunction56  function ! Error(functionName) abort7      echo "Error: The Function [" . a:functionName. "] is not working.     (FAIL)"8   endfunction910 function ! ClearFile() abort11     execute 'normal ggdG'12 endfunction1314 function ! TestAddToDoc() abort15    let testName = "AddToDoc" ;16  call AddToDoc( "Hello World" )17  if getline ( "1" ) == "Hello World"18      call Report(testName)19     else20      call Error(testName)21     endif22 endfunction2324 function ! TestStart()25     call TestAddToDoc()26     “call ClearFile()27 endfunction

4.  Now save the file.
5.  Now in another Terminal open `vim something.js`.
6.  In `something.js` use `:call TestStart() ` to see the test results. It should log a single test and say that it Passed it.

Explanation​ In this section, I will explain the steps we took in the previous sections:Explaining Write Section

1.  In step #1 we are importing the `sourceCodeGenerator.vim` script in `congenial-JavaScript.vim`.
2.  In step #2 we are programming the key-binding `,var ` to call the `GenerateVariableWithScope()` method.
3.  The `nnoremap` compound-keyword is used declare key-bindings, and `<cr>` means the “Enter” key.
4.  In step #3:
    1.  On line #2 the function `AddToDoc()` is used to add text to the file we are editing.
    2.  On line #6 `GenerateVariableWithScope()` is used to generate a variable by telling Vim it’s scope, name, and value.
    3.  On line #7 the `sSel` aka `scopeSelect` variable uses `input()` to prompt used to write 1, 2, or 3 to pick the variable scope.
    4.  On line #8 `sOps` or `scopeOptions` is a list/array that holds the kinds of variables in JavaScript corresponding to different scopes.
    5.  On line #9 `sStd` or `scopeSelected` puts `scopeSelect` and `scopeOptions` together, and gets the required “kind of variable” in return; so if the user gave Vim `3` the “kind of variable” is “const”.
    6.  Lines #11 and #12 asks the user for the Name and Value of the variable.

Explaining Test and Debug Section

1.  In step #1 we are creating a test module. We didn’t create it in the initialization because strictly speaking the two aren't mutual.
2.  In step #2 we are importing the `sourceCodeGenerator.vim` script in `congenial-JavaScript.vim`.
3.  In step #2:
    1.  There is a function named `Report()` which is used to log the passing tests in a uniform fashion, meaning all the reports need to look similar.
    2.  There is a function named `Error()` which is similar to `Report()` but for failing tests.
    3.  There is a function `ClearFile()` to clear the file after each test runs it’s course, `execute “normal ggdG”` tells Vim to execute `ggdG` in normal mode. `gg` takes up to the top line in Vim, and `dG` deletes all line till the bottom line.
    4.  The function `TestAddToDoc()` is a test that calls the function `AddToDoc(“Hello World”)` from `sourceCodeGenerator.vim`, see line #16. This writes `Hello World` on line #1 in the new JavaScript file.
    5.  On line #17, the function `TestAddToDoc()` then tests if line #1 of the opened JavaScript file has `Hello World` written on it, if true then the function logs the passing report, if false it logs the failing error.
    6.  The `getline(“1”)` code reads the text on line #1, when used with “.” instead of “1” we can get the text on current line. The `expand("<cword>")` can read the work under our cursor.
    7.  The `tests.vim` file is able to call functions from the `sourceCodeGenerator.vim` file because they were both activated by the `congenial-JavaScript.vim` file, which was activated by the `plugins.vim` file, which was activated upon opening a JavaScript file due to it being in the `~/.vim/after/ftplugin/javascript/` directory. Its a slippery slope, but it’s the best one we got!
    8.  The function `TestAddToDoc()` is called by the function `TestStart()` which is designed to call a test, then clear the file, then call another test, the clear the file again, and so on. Here we can append more tests later.
    9.  The tests won’t work until the developer/user uses `:call TestStart() ` from a JavaScript file.
    10.  `:.w !bash ` can be used to run commands on the current line through bash, however this is not required here. The command writes the text on current line in a bash StdIn, we can write it on the StdIn of any program.
    11.  We can also use `new “somefile.js”` to automate opening of a test file during development. We aren’t using it here because I like to do it manually. `quit! `
    12.  Notice how clear file is commented out, it’s still in progress in the greater scheme of things.

Test and Debug (GenerateVariableWithScope)​ The following instructions can be used to write a test that can automate Steps #7 to #11 in the previous Write section, these steps will be used to test the function `GenerateVariableWithScope()`.

1.  First of all we need to update our code in the `modules/sourceCodeGenerator.vim` file, here we have rewritten the `GenerateVariableWithScope()` function:

1 function ! GenerateVariableWithScope( ... ) abort2    if a:0 > 03       let scopeSelection = a:14       let varName = a:25       let varValue = a:36     else7       let scopeSelection = input ( 'var/let/const Pick 1/2/3: ' )9       let varName = input ( 'Name of Variable: ' )10     let varValue = input ( 'Value of Variable: ' )11    endif12   let scopeOptions = [ 'var' , 'let' , 'const' ]13   let scopeSelected = scopeOptions[scopeSelection-1]14   call AddToDoc(scopeSelected. ' ' .varName. ' = ' .varValue. ';' )15 endfunction

2.  This new version of `GenerateVariableWithScope()` is improved so it provides an interface for testing. From now on, we will be using “Test-Driven Development” approach, where unit-tests are written before actual source-code!

3.  If you want to use unit-testing in your development I suggest using Jenkins (MIT) and Selenium.
4.  Notice the `...` symbol on line #1, this allows functions to take in up-to 20 optional arguments. The argument are accessible via `a:1, a:2, a:3, …, a:20`, while `a:0` stores the number of arguments passed to the function.
5.  Here on line #2 the code checks the number of arguments passed to the function, if that number is greater than 0, then we run the automated test version of the function, else we run the function that takes input from the user.
6.  Now, in `modules/tests.vim` add the following code before the function `TestStart()`, ignore the line numbers, write the function where you see fit.

1   function ! TestGenerateVariableWithScope() abort2      let testName = "GenerateVariableWithScope"3      call GenerateVariableWithScope( 1 , "Health" , 100 )4      call NextLine()5      call GenerateVariableWithScope( 2 , "alive" , "true" )6      call NextLine()7      call GenerateVariableWithScope( 3 , "class" , "'hero'")8     let expectedOutput = "var Health = 100;let alive = true;const class = 'hero';"9      if getline( "2" ).getline( "3" ).getline( "4" ) == expectedOutput10       call Report(testName)11     else12       call Error(testName)13     endif14 endfunction

7.  Now in `modules/tests.vim` modify the `TestStart()` function so it looks like this:

function ! TestStart()  call WriteTestHeaderToFile()  call TestAddToDoc()  call NextLine()  call TestGenerateVariableWithScope()  call ReadTestReport()"  call ClearFile()endfunction

8.  A few more functions are added to the `tests.vim` file, it ultimately looks like this:

1   function ! Report(functionName) abort2      let result = "Report: The Function [" . a:functionName . "] is working.     (PASS)"3      call WriteToFile(result)4   endfunction5  6  function ! Error(functionName) abort7      let result = "Error: The Function [" . a:functionName . "] is not working.     (FAIL)"8      call WriteToFile(result)9   endfunction1011 function ! WriteToFile(data) abort12     " Test Report is saved in the local project Dir13     call writefile([ a:data ], "testReport.txt" , "a" )14     " appends logs to file15 endfunction1617 function ! WriteTestHeaderToFile() abort18     call WriteToFile( '' )19     call WriteToFile( '----------------------' )20     call WriteToFile(strftime( '%c' ))21     call WriteToFile( '----------------------' )22 endfunction23  24 function ! ReadTestReport() abort25     " Opens Test Report in a New Vim Window26      execute "new ./testReport.txt"27   endfunction28  29  "function! ClearFile() abort30  "  execute 'normal ggdG'31   "endfunction32  33  function ! NextLine() abort34      execute 'normal o'35   endfunction36  37  function ! TestAddToDoc() abort38     … … … …39   endfunction40  41  function ! TestGenerateVariableWithScope() abort42     … … … …43   endfunction44  45  function ! TestStart()46     … … … …47   endfunction

9.  No modification is done to the `TestAddToDoc()` function. The `… … … … ` is a placeholder for inner content.
10.  With these new modification we have a completely new Report generating mechanism that generates the Reports in an external file named `testReport.txt `.
11.  Now I will send this file to Siena and she’ll take care of the rest. We will now focus on the code of the actual program.

Program to Generate a label​ In JavaScript, we have a thing called labels, which are used for a wide range of reasons. To learn more about them read the book “Simply ES6 – Ray Voice, Anna Voice”. Let’s write some code to generate a label.Write​ Follow these steps to write the first feature:

1.  Inside `congenial-JavaScript.vim` add the following lines of code and save it:

nnoremap ,label :call GenerateLabel()<cr>

2.  This binds `,label` to trigger the`GenerateLabel()` function.
3.  Now add the following code to `modules/sourceCodeGenerator.vim `:

function ! GenerateLabel( ... ) abort  if a:0 > 0     let labelName = a:1   else    let labelName = input( 'Name of Label: ' )   endif  call AddToDoc(labelName. ':{}' )endfunction

4.  Here is another Generator, it is used to generate JavaScript labels where needed.

Test and Debug

1.  Following is the test Siena wrote for this Generator:

function ! TestGenerateLabel() abort  let testName = "GenerateLabel"  let labelName = "QATests"  let expectedOutput = labelName. ":{}"  call GenerateLabel(labelName)  call GenerateReport(testName, expectedOutput)endfunction

2.  You may be having problem in understanding this since it’s slightly different from last test case, this is because Siena has completely transformed the `tests.vim` file since the last time we saw it; in this case she actually made it better. The whole file is provided at GitHub ray6464/congenial-JavaScript , in the modules directory.
3.  Before moving on visit the Repo at GitHub and check out how professional Tests look, Siena is known for writing amazing tests in VimScript, Selenium, etc.
4.  Following is the output of these tests:

----------------------Sat 20 Jun 2020 11:45:45 AM JST------------------------------*Output: Hello World*--------Report: The Function [AddToDoc] is working.     (PASS)--------*Output: var Health = 100;*--------Report: The Function [GenerateVariableWithScope] is working.     (PASS)--------*Output: let alive = true;*--------Report: The Function [GenerateVariableWithScope] is working.     (PASS)--------*Output: const class = 'hero';*--------Report: The Function [GenerateVariableWithScope] is working.     (PASS)--------*Output: QATests:{}*--------Report: The Function [GenerateLabel] is working.     (PASS)Program to Generate a For Loop​ In JavaScript, we have 3 types of fundamental “for” Loops. There are For loops for iterating over Ranges like 0-10, these are the regular C-language like For Loops; then there are For loops of iterating of Indices and members of arrays and other Iterables, these are the For/In and For/Of Loops. Let’s get with it!Write

1.  Add the following code to `congenial-JavaScript.vim`:

nnoremap ,loop :call GenerateForLoop()<cr>

2.  This binds `,loop ` to GenerateForLoop().
3.  Now add the following Function to `sourceCodeGenerator.vim`:

1  function ! LoopOverRange(...) abort2      if IsTest( a : 0 )3        let initialCounterValue = a : 14        let counterLimitCompatative = a : 25        let counterIterationValue = a : 36      else7        let initialCounterValue = input( 'Initial Counter Value: ' )8        let counterLimitCompatative = input( 'Comparative (<10)/(>5)/(==20): ' )9        let counterIterationValue = input( 'Counter Iteration Value (++/+2/-3): ' )10     endif11     call AddToDoc( 'for (let i=' .initialCounterValue. '; i' .counterLimitCompatative. '; i' .counterIterationValue. '){}' )12 endfunction1314 function ! LoopOverMembers(...) abort15     if IsTest( a : 0 )16       call AddToDoc( 'for (let m of ' . a : 1 . '){}' )17     else18       call Suggest( 'Give the name of an already declared array, for example: myList | myArray | myArr' )19       let arrayToIterateOver = input( 'Array to Iterate Over: ' )20       call AddToDoc( 'for (let m of ' .arrayToIterateOver. '){}' )21     endif22 endfunction2324 function ! LoopOverIndices(...) abort25     if IsTest( a : 0 )26       call AddToDoc( 'for (let i in ' . a : 1 . '){}' )27     else28       call Suggest( 'Give the name of an already declared array, for example: myList | myArray | myArr' )29       let arrayToIterateOver = input( 'Array to Iterate Over: ' )30       call AddToDoc( 'for (let i in ' .arrayToIterateOver. '){}' )31     endif32 endfunction

4.  The three Functions shown here render three different types of loops, the For-loop, the For/Of loop, and the For/In loop. This will be called from another Function, which prompts the user for the type of loop they need.
5.  Now add the following Function to `sourceCodeGenerator.vim`:

1  function ! GenerateForLoop( ... ) abort2      if IsTest( a:0 )3        let loopTypeSelectionIndex = a:14      else5        let loopTypeSelectionIndex = input ( 'Loop over Range/Members/Indices Pick 1/2/3: ' )6      endif7      let loopTypesShelf = [ ' loopOverRange' , 'loopOverMembers' , 'loopOverIndices' ]8      let loopSelection = loopTypesShelf[loopTypeSelectionIndex- 1 ]9      if IsTest( a:0 )10 "----------------------------------------------11       if loopSelection == loopTypesShelf[ 0 ] "for12         call LoopOverRange(0, "<10" , "++" )13       elseif loopSelection == loopTypesShelf[ 1 ] "forOf14         call LoopOverMembers( "myLoop" )15       elseif loopSelection == loopTypesShelf[ 2 ] "forIn16         call LoopOverIndices( "myLoop" )17       endif18 "----------------------------------------------19     else20 "----------------------------------------------21       if loopSelection == loopTypesShelf[ 0 ]22         call LoopOverRange()23       elseif loopSelection == loopTypesShelf[ 1 ]24         call LoopOverMembers()25       elseif loopSelection == loopTypesShelf[ 2 ]26         call LoopOverIndices()27       endif28 "----------------------------------------------29     endif30 endfunction

6.  This function generates three types of loops by calling their respective functions like code on line # 22, #25, #26.
7.  On lines #2 to #6 the Function is checks if it’s called by a person or a test!
8.  Lines #7 and #8 figures out which type of loop we need; for example if we entered “1” when prompted on line #5, then lines #7 and #8 will resolve to a classical For loop.
9.  On line #9 the Function is checks if it’s called by a person or a test! Again.
10.  On lines #10 to #18 and on #20 to #28 the Function matches the type of loop we called with the appropriate function, and then calls that function; for example if we called for a “loopOverRange” aka “classical For loop”, then the Function will call the `LoopOverRange()` Function.

Test and Debug

1.  Following is the test for For Loops:

1  function ! TestGenerateForLoop() abort2      let testName = "GenerateForLoop"3      let expectedOutput1 = "for (let i=0; i<10; i++){}"4      let expectedOutput2 = "for (let m of myLoop){}"5      let expectedOutput3 = "for (let i in myLoop){}"6      call GenerateForLoop( 1 )7      call NextLine()8      call GenerateForLoop( 2 )9      call NextLine()10  call GenerateForLoop( 3 )11  call GenerateReport(testName, expectedOutput1)12  call GenerateReport(testName, expectedOutput2)13  call GenerateReport(testName, expectedOutput3)14   endfunction

2.  Again, if you are having problems familiarizing yourself with the tests then don’t worry, its part of working with another person on the team.
3.  Check the whole file on GitHub at ray6464/congenial-JavaScript for any invisible parts.
4.  On lines #3, #4, and #5 we are declaring that the provided For, For/Of, and For/In Loops are the expected outputs.
5.  One lines #6, #8, #10 we are generating the loops with the Function we are testing.
6.  On lines #11, #12, and #13 we are generating reports for the outputs generated in the previous step. Keep in mind that the lines `GenerateReport() ` works on are decided by the `lineNumber ` variable in `modules/tests.vim`.
7.  The output should be the following:

----------------------Sun 21 Jun 2020 11:48:07 AM JST------------------------------*Output: Hello World*--------Report: The Function [AddToDoc] is working.     (PASS)--------*Output: var Health = 100;*--------Report: The Function [GenerateVariableWithScope] is working.     (PASS)--------*Output: let alive = true;*--------Report: The Function [GenerateVariableWithScope] is working.     (PASS)--------*Output: const class = 'hero';*--------Report: The Function [GenerateVariableWithScope] is working.     (PASS)--------*Output: QATests:{}*--------Report: The Function [GenerateLabel] is working.     (PASS)--------*Output: for (let i=0; i<10; i++){}*--------Report: The Function [GenerateForLoop] is working.     (PASS)--------*Output: for (let m of myLoop){}*--------Report: The Function [GenerateForLoop] is working.     (PASS)--------*Output: for (let i in myLoop){}*--------Report: The Function [GenerateForLoop] is working.     (PASS)Number of Tests performed: 8Number of Tests Passed: 8Number of Tests Failed: 0Program to Generate an Array​ In this section, we will develop a method to generate Arrays of JavaScript. Let’s get started with it!Write

1.  Add the following code to `sourceCodeGenerator.vim`:

1  function ! GenerateArray(...) abort2      if a : 0 > 03        let arrayName = a : 14        let numberOfMembersInArray = a : 25      else6        let arrayName = input( 'Name of Array: ' )7        let numberOfMembersInArray = input( 'Number of Members in Array: ' )8      endif9      call AddToDoc( 'let ' .arrayName. ' = [ ' )1011     let i = 012     while i < numberOfMembersInArray13      14       if a : 0 > 015         let valueOfNthMember = a : 3 + i16       else17         let valueOfNthMember = input( 'Value of ' . i . 'th member: ' )18       endif1920       call AddToDoc(valueOfNthMember. " " )2122       if i < numberOfMembersInArray -123         call AddToDoc( ', ' )24       endif2526       let i = i + 127     endwhileTest and Debug

1.  Now let’s see the test code:

1  function TestGenerateArray() abort2        let testName = "GenerateArray"3    let expectedOutput1 = "let myArray = [1,2,3];"4    call GenerateArray( "myArray" , 3 , 1 , 2 , 3 )5     call GenerateReport(testName, expectedOutput)6   endfunction

2.  On line #4 we have called the GenerateArray() function and passed it arguments to make it match the expected output(). If you are having problems here the problem may as well lie in the output Vim produces instead of your code, always check manually the first time.
3.  All 9 tests should be passed at this point.

Program to Generate Array methods​ In this section we will develop two array methods, `split`, and `map`. Let’s get started with it!Write

1.  Add the following code to `sourceCodeGenerator.vim`:

1  function ! SplitArray(...) abort2      if a : 0 > 03        let arrayName = a : 14        let splitByCharacter = a : 25      else6        let arrayName = input( 'Array Name: ' )7        let splitByCharacter = input( 'Split by character: ' )8      endif9      call AddToDoc(arrayName. '.split("' .splitByCharacter. '");' )10 endfunction1112 function ! MapArray(...) abort13     if a : 0 > 014       let arrayName = a : 115       let expressionToExecute = a : 216     else17       let arrayName = input( 'Array Name: ' )18       let expressionToExecute = input( 'Expression to execute per iteration: ' )19     endif20     call AddToDoc(arrayName. '.map(element => ' .expressionToExecute. ');' )21 endfunction

2.  The code is pretty self-explanatory so by this time you should be able to instantly recognize/understand the code written by yourself or anyone else for this project.
3.  Try to understand the code yourself! It follows a similar pattern to all the other code written in this file.

Test and Debug

1.  Now let’s see the test code (I wrote this since Siena was off the clock):

1  function TestSplitArray() abort2      let testName = "SplitArray"3      let expectedOutput = 'myArray.split(",");'4      call SplitArray( "myArray" , "," )5      call GenerateReport(testName, expectedOutput)6   endfunction7  8  function TestMapArray() abort9      let testName = "MapArray"10     let expectedOutput = 'myArray.map(element => console.log(element));'11     call MapArray( "myArray" , "console.log(element)" )12     call GenerateReport(testName, expectedOutput)13   endfunction

2.  Try to understand the code yourself; all of the code written beyond this point follows a clear pattern.
3.  Once you understand this code try to reduce it (but keep it readable).

Program to Generate Timer Loop​ In this section we will develop a method for a timer loop like `SetInterval`. Let’s get started with it!Write

1.  Add this code to the `sourceCodeGenerator.vim` file:

1  function ! GenerateTimer(...) abort2      if a : 0 > 03        let intervalName = a : 14        let intervalLength = a : 25      else6        let intervalName = input( 'IntervalName: ' )7        let intervalLength = input( 'interval length in ms: ' )8      endif9      call AddToDoc( 'const ' .intervalName. ' = setInterval(function(){/*code-here*/},' .intervalLength. ');' )10 endfunction

2.  Figure out how this code works; find out which lines are for testing and which are for users.

Test and debug

1.  Add this code to the `tests.vim` file:

1  function TestGenerateTimer() abort2      let testName = "GenerateTimer"3      let expectedOutput = "const myTimer = setInterval(function(){/*code-here*/},1000);"4      call GenerateTimer( "myTimer" , 1000 )5      call GenerateReport(testName, expectedOutput)6   endfunction

2.  Figure out how this code works.

Program to Generate Stdout logs​ In this section, we will develop a method for Stdout logs. Let’s get started with it!Write and Test

1.  Add this code to the `sourceCodeGenerator.vim` file:

1  function ! GenerateLog(...) abort2      if a : 0 > 03        let valueToLog = a : 14      else5        let valueToLog = input( 'Value to log: ' )6      endif7      call AddToDoc( 'console.log(' .valueToLog. ');' )8   endfunction

2.  Add this code to the `tests.vim` file:

1  function TestGenerateLog() abort2      let testName = "GenerateLog"3      let expectedOutput = 'console.log("Hello World");'4      call GenerateLog( '"Hello World"' )5      call GenerateReport(testName, expectedOutput)6   endfunction

3.  Figure out how this code works.

Program to Generate Loops to Iterate over Arrays (For-Each)​ In this section, we will develop a function to generate a JavaScript method to iterate over arrays. Let’s get started with it!Write, Test and Debug

1.  Add this code to the `sourceCodeGenerator.vim` file:

1  function ! GenerateLoopOverArray(...) abort2      if a : 0 > 03        let arrayName = a : 14      else5        let arrayName = input( 'Array Name: ' )6      endif7      call AddToDoc(arrayName. '.forEach((member, index, thisArray)=>{' )8      call NewLine()9      call AddToDoc( '  console.log (index, member, thisArray);' )10      call NewLine()11      call AddToDoc( '});' )12   endfunction

2.  Add this code to the `tests.vim` file:

1  function ! GenerateMultiLineReport(testName, expectedOutputs) abort2      let linesInExpectedOutput = len( a :expectedOutputs)3      call WriteToFile( '--------*Output: ' .getline( g :lineNumber). "..." .(linesInExpectedOutput -1 ). " more lines*--------" )4      let goodLines = 05  6      for expectedOutput in a :expectedOutputs7        if getline( g :lineNumber) == expectedOutput8          let goodLines = goodLines + 19        endif10       let g :lineNumber = g :lineNumber + 111     endfor1213     if goodLines == linesInExpectedOutput14       call Report( a :testName)15     else16       call Error( a :testName)17     endif18 endfunction1920 function ! TestGenerateLoopOverArray() abort21     let testName = "GenerateLoopOverArray"22     let line1 = 'myArray.forEach((member, index, thisArray)=>{'23     let line2 = '  console.log (index, member, thisArray);'24     let line3 = '});'25     let expectedOutputs = [line1, line2, line3]26     call GenerateLoopOverArray( "myArray" )27     call GenerateMultiLineReport(testName, expectedOutputs)28 endfunction

3.  In the tests file we have two functions, the first one on line #1 allows us to generate reports on functions that are expecting multi-line output, and the second one is to test out Loop-over-array method’s code.
4.  You may not be familiar with the `len()` method, and `for/in` loops of VimScript! See below for instructions.

​ The `len()` method is for getting the length of an array/list. For example:

1.  `let myArray = [“a”, “b”, “c”] ` has 3 members.
2.  `len(myArray) ` will return `3 `.

​ The `for/in` loop is for iterating over arrays/lists while the “Man of the hour” variable assumes the role of a single member from the array.

1.  `let myFruits = [“apple”, “mango”, “banana”] ` has 3 members, them being “apple”, “mango”, and “banana”.
2.  The `for/in` loop `for fruit in myFruits ` will iterate over each member of the `myFruits` array.
3.  During each iteration the “Man of the hour” variable (which is `fruit`) will be equal to a member from `myFruits`.
4.  So during the 1st iteration `fruit` will be equal to `apple`.
5.  In the 2nd iteration `fruit` will be equal to `mango`.
6.  Finally in the 3rd iteration `fruit` will be equal to `banana`.

​ Now go back to the VimScript code, and figure out how it works.Note​ More features for JavaScript, ES6+, React, Vue, Angular, NodeJS, ElectronJS, Commonly used JavaScript Libraries, etc. will be added in future editions of this book.​ If you want to work on any of these features as part of your portfolio then look-up ray6464/congenial-JavaScript on GitHub, or contact me on Twitter @rayshorthead. Every contributor will be credited accordingly.​ Start small, like working on generating boilerplate code for libraries like lodash (assuming it’s not already taken by someone else)! Please let me know if you are working on a feature by opening an issue. I look forward to collaborating with you!Chapter 4 – Advanced Features​ In this chapter, we will work on some NodeJS code. You will also be given a list of basic features, try to develop them on your own! Help from the internet is allowed but help from other developer is to be refrained from.Basic features​ Try to build the following features yourself, when you are successful than you can go ahead and make a pull request on the official repo at ray6464/congenial-JavaScript on GitHub.

1.  JavaScript Comments Generator (single-line)
2.  JavaScript Comments Generator (multi-line)
3.  Array.filter()
4.  Array.join()
5.  Array.split()
6.  Array.pop()
7.  Array.push()
8.  Array.shift()
9.  Array.unshift()
10.  Array.slice()
11.  Array.splice() (mutative)
12.  Array.concat()
13.  etc.

NodeJS​ NodeJS (released in 2009) is a JavaScript Framework that allows us to run JavaScript on servers. Before NodeJS, JavaScript could only be used to create gimmicky websites, it basically acted as a styling-agent with additional features; however now JavaScript is one of the most powerful languages out there, possibly the most powerful (in a manner of speaking).​ If you want to learn, NodeJS use the book:“ Simply Web Development : An introduction to the world of Web development - Anna Voice, Ray Voice”​ This book has comprehensive introduction-level lessons to all topics you need to learn for both front-end and back-end web development, and it’s part of a complete series which can be used during your journey to become a full-stack engineer.​ For NodeJS you may want to learn about stuff like NPM for package management, NVM for version management, etc. before moving on.Note: Some off-screen modifications may be made to the code here, but nothing too morbid; you can figure it out yourself, or modify the code to work without those modifications.Built-in Variables​ NodeJS has several built-in global variables; to add the use of these features in congenial-JavaScript we can use the following code:modules/sourceCodeGenerator.vim:1   function ! GenBuiltInVars() abort2     let objectChoices = [ 'console' , 'global' , 'process' , 'document' ]3     let objectChoiceIndex = input( 'console/global/process/document' . ' Pick 1/2/3/etc: ' )4      let objectChoice = objectChoices[objectChoiceIndex -1 ]5      call AddToDoc(objectChoice)6    endfunctioncongenial-JavaScript.vim:nnoremap ,gvar : call GenBuiltInVars()< cr >inoremap < c - y >gvar <esc>: call GenBuiltInVars()< cr >​ Here we have the option to generate essential variables required for back-end development; objects like `global`, `process`, etc. are the heart of NodeJS.Process props​ The `process` object has several essential props like `argv`, ‘env’, `platform`, etc. the following code is used to generate process props (including the ‘process’ object):modules/sourceCodeGenerator.vim:1   function ! GenProcessVars() abort2     let objectChoices = [ 'argv' , 'env' , 'emitWarning()' , 'pid' , 'platform' ]3     let objectChoiceIndex = input( 'argv/env/emitWarning/pid/platform' . ' Pick 1/2/3/etc: ' )4      let objectChoice = objectChoices[objectChoiceIndex -1 ]5      call AddToDoc( 'process.' .objectChoice)6    endfunctioncongenial-JavaScript.vim:nnoremap ,pvar : call GenProcessVars()< cr >inoremap < c - y >pvar <esc>: call GenProcessVars()< cr >Events​ NodeJS is a run-time with capabilities to move heavy operations to another thread (also called non-blocking runtimes and event-loops), making NodeJS great for servers.​ To generate NodeJS events we can use the following code:modules/sourceCodeGenerator.vim:1   function ! GenEventVars() abort2     let objectChoices = [ 'exit' , 'beforeExit' , 'abort' ]3     let objectChoiceIndex = input( 'Events exit/beforeExit/abort' . ' Pick 1/2/3/etc: ' )4      let objectChoice = objectChoices[objectChoiceIndex -1 ]5      call AddToDoc( 'process.on("' .objectChoice. '", function() {});' )6    endfunctioncongenial-JavaScript.vim:nnoremap ,event :call GenEventVars()<cr>inoremap < c - y >event <esc>: call GenProcessVars()< cr >Refactoring code​ Here I have seen a pattern emerging among the functions described in this chapter, so I have refactored the code to the following:modules/sourceCodeGenerator.vim:1   function ! ObjectWriter(objectChoices, index, preCode, postCode) abort2      let objectChoice = a :objectChoices[ a :index]3      call AddToDoc( a :preCode.objectChoice. a :postCode)4    endfunction5   6   function ! GenerateBuiltInVariables() abort7     let objectChoices = [ 'console' , 'global' , 'process' , 'window' , 'document' ]8     let objectChoiceIndex = input( 'console/global/process/window/document' . ' Pick 1/2/3/etc: ' )9      call ObjectWriter(objectChoices, objectChoiceIndex -1 , '' , '' )10 endfunction11   12 function ! GenerateProcessVariables() abort13    let objectChoices = [ 'argv' , 'env' , 'emitWarning()' , 'pid' , 'platform' , 'arch' ]14    let objectChoiceIndex = input( 'argv/env/emitWarning/pid/platform/arch' . ' Pick 1/2/3/etc: ' )15    call ObjectWriter(objectChoices, objectChoiceIndex -1 , 'process.' , '' )16 endfunction17   18 function ! GenerateEventVariables() abort19    let objectChoices = [ 'exit' , 'beforeExit' , 'abort' ]20    let objectChoiceIndex = input( 'Events exit/beforeExit/abort' . ' Pick 1/2/3/etc: ' )21    call ObjectWriter(objectChoices, objectChoiceIndex -1 , 'process.on("' , '", function() {});' )22 endfunctionNote: In all honesty, I developed the pattern on purpose for this book.​ Now, this code can be further refactored and reduced, but this is enough for now.Custom Events Emitter​ To generate custom NodeJS events emitter we can use the following code:modules/sourceCodeGenerator.vim:1   function ! GenEventEmitter() abort2     call AddToDoc( "const { EventEmitter } = require('events')" )3      call NewLine()4     call AddToDoc( 'const eventEmitter = new EventEmitter();' )5      call NewLine()6      call AddToDoc( "eventEmitter.on('launch', () => {" )7      call NewLine()8      call AddToDoc( "console.log('Server launched')" )9      call NewLine()10     call AddToDoc( "})" )11     call NewLine()12     call AddToDoc( "eventEmitter.emit('launch')" )13 endfunctioncongenial-JavaScript.vim:nnoremap ,emit : call GenEventEmitter()< cr >inoremap < c - y >emit <esc>: call GenEventEmitter()< cr >Creating a Server with HTTP code​ To generate code for HTTP server code we can use the following code:Note: Here I have built a new feature into “AddToDoc()” for appending new lines at the end of the output.modules/sourceCodeGenerator.vim:1   function ! GenServerCode() abort2     let serverPort = input( "Which port to use (8080, 3000, etc.): " )3       4      call AddToDoc( "var http = require('http');" )5      call NewLine()6      call NewLine()7     call AddToDoc( "http.createServer(function (req, res) {" , "newLine" )8      call AddToDoc( "  res.writeHead(200, {'Content-Type': 'text/html'});" , "newLine" )9      call AddToDoc( "  res.write('server at " .serverPort. " is up');" , "newLine" )10     call AddToDoc( "  return res.end();" , "newLine" )11     call AddToDoc( "}).listen(" .serverPort. ");" , "newLine" )12 endfunctioncongenial-JavaScript.vim:nnoremap ,server : call GenServerCode()< cr >inoremap < c - y >server <esc>: call GenServerCode()< cr >FS module code​ One of the most powerful modules in NodeJS is the File System aka FS module; it provides both blocking (sync) and non-blocking (async) methods to work with files, directories, etc. Here we will develop some basic file reading and writing method generators for it.​ Take a look at “https://nodejs.org/api/fs.html”.Note: Sync functions are blocking, which means the whole program must wait for the “blocking code” to do it’s job.​ To generate code for FS module usage we can use the following code (this is a long one):modules/sourceCodeGenerator.vim:1   function ! GenFSModuleCode() abort2   " needs more methods3     let fsMethods = input( '(1) Read File, (2) Write File 1/2: ' )4     let blocking = input( 'blocking (sync) or non-blocking (async) 1/2: ' )5      let fileName = input( 'fileName: ' )6   7      if fsMethods == '2'8       let textOutput = input( 'What text do you want written to that file: ' )9       let dataVarName = input( 'Name of the variable that will store data: ' )10     endif1112    if fileName == ''13       let fileName = './database.json'14     endif1516    if blocking == '1'17       if fsMethods == '1'18         call AddToDoc( "const { readFileSync } = require('fs');" , "newLine" )19         call AddToDoc( "const txt = readFileSync('" .fileName. "', 'utf8');" , "newLine" )20         call AddToDoc( "console.log(txt);" , "newLine" )21       elseif fsMethods == '2'22         call AddToDoc( "const { writeFileSync } = require('fs');" , "newLine" )23         call AddToDoc( "const " .dataVarName. " = new Uint8Array(Buffer.from('" .textOutput. "'));" , "newLine" )24         call AddToDoc( "writeFileSync('" .fileName. "', " .dataVarName. ");" , "newLine" )25       endif26    elseif blocking == '2'27       if fsMethods == '1'28         call AddToDoc( "const { readFile } = require('fs');" , "newLine" )29         call AddToDoc( "readFile('" .fileName. "', 'utf8', (err, txt)=>{" , "newLine" )30         call AddToDoc( "  console.log(txt);" , "newLine" )31         call AddToDoc( "});" , "newLine" )32       elseif fsMethods == '2'33         call AddToDoc( "const { writeFile } = require('fs');" , "newLine" )34         call AddToDoc( "const " .dataVarName. " = new Uint8Array(Buffer.from('" .textOutput. "'));" , "newLine" )35         call AddToDoc( "writeFile('" .fileName. "', " .dataVarName. ", (err) => {" , "newLine" )36         call AddToDoc( "  if (err) throw err;" , "newLine" )37         call AddToDoc( "  console.log('The file has been saved!');" , "newLine" )38         call AddToDoc( "});" , "newLine" )39       endif40     endif41 endfunctioncongenial-JavaScript.vim:nnoremap ,fs : call GenFSModuleCode()< cr >inoremap < c - y >emit <esc>: call GenFSModuleCode()< cr >​ This code allows us to generate FS methods to read and write files, both in a blocking and non-blocking manner.JavaScript Require() and Export​ In JavaScript we use `Require()` and `modules.export` for importing and exporting data from distinguished files, for more info read the book:Simply ES6: Mastering JavaScript and ES6 to Its Fullest, 2nd Edition​ To generate code for Import and Export (non-ES modules) we can use the following code:modules/sourceCodeGenerator.vim:1   function ! GenRequire() abort2     let moduleName = input( "Module Name: " )3     let moduleImportedAs = input( "Import data as: " )4   5      if moduleImportedAs == ''6        let moduleImportedAs = moduleName7      endif8   9     call AddToDoc( "const " .moduleName. " = require('" .moduleImportedAs. "');" , "newline" )10 endfunction1112 function ! AddProp() abort13    let propName = input( "Prop Name: " )14    let propValue = input( "Prop value: " )15     call AddToDoc( '  ' .propName. ': ' .propValue. ',' , 'newLine' )16    let morePropPrompt = input( "Add another Prop? y/n: " )17    if morePropPrompt == "y"18       call AddProp()19     endif20 endfunction2122 function ! GenExport() abort23    call AddToDoc( 'module.exports = {' , "newLine" )24     call AddProp()25     call AddToDoc( '}' , "newLine" )26 endfunctioncongenial-JavaScript.vim:nnoremap ,require : call GenRequire()< cr >inoremap < c - y >require <esc>: call GenRequire()< cr >nnoremap ,export : call GenExport()< cr >inoremap < c - y >export <esc>: call GenExport()< cr >Basic Express Server Tools for NodeJS​ To generate code for a Basic Express based server with NodeJS we can use the following code:modules/sourceCodeGenerator.vim:1   function ! GenExpServer() abort2   call AddToDoc( "const express = require('express');" , 'newLine' )3     call AddToDoc( "const app = express();" , 'newLine' )4      call NewLine()5     call AddToDoc( "app.get('/', (req, res) => {" , 'newLine' )6      call AddToDoc( "  res.sendFile('index.html', {root: __dirname});" , 'newLine' )7      call AddToDoc( "});" , 'newLine' )8      call NewLine()9     call AddToDoc( "const port = process.env.PORT || 8080;" , 'newLine' )10    call AddToDoc( "app.listen(port, ()=>{console.log(`System Online: ${port}`)});" , 'newLine' )11 endfunction1213 function ! GenExpGet() abort14    let node = input( "Node home/aboutme/etc: " )15    let fileURL = input( 'name and URL of File index.html/main.css/etc: ' )16    call AddToDoc( "app.get('" .node. "', (req, res) => {" , 'newLine' )17    call AddToDoc( "  res.sendFile('" .fileURL. "', {root: __dirname});" , 'newLine' )18     call AddToDoc( '});' , 'newLine' )19 endfunctioncongenial-JavaScript.vim:nnoremap ,express : call GenExpServer()< cr >inoremap < c - y >express <esc>: call GenExpServer()< cr >nnoremap ,express : call GenExpressGet()< cr >inoremap < c - y >express <esc>: call GenExpGet()< cr >​ This code will allow Vim users to generate express servers and Get requests in a few key strokes.​ This covers most of the basic functionality needed by NodeJS developers. From here on out developers can deploy NodeJS apps via Virtual Private Servers (VPS), Google App Engine, etc.Chapter 5 – Functional Programming Code for JavaScript​ Functional programming is a way to write code that is not only vastly better than OOP (not always), but it’s also cleaner. When function programming is required, we should emphasize on:-

1.  Writing higher order functions.
2.  Not mutating any data while we are at it.
3.  Using methods like filter, map, etc. that works on a piece of data and returns a modified version of the data without mutating the original data.

​ JavaScript has some built-in methods like `map()`, `filter()`, etc. but I still prefer the usage of some custom higher order functions described down the line.​ When writing code in a functional programming paradigm we must adhere to the following rules:

*   Functions may not be influenced by the state of the program.
*   Functions may not influence the state of the program.
*   Functions must be used to break the program down into small, testable parts.
*   Functions may be treated as first class citizens, which basically means just like any other data functions will have concrete names, will be passed as arguments, will be returned from other functions, etc.
*   Functions may not take input from users.

​ Having extensive study experience with Common Lisp and Wolfram, I prefer to lean towards functional programming for JavaScript as well. Let’s start building some Generators for dynamic boiler-plate code.​ Following is some brief terminology for Function Programming intellectuals.

1.  Isolated functions - there is no dependence on the state of the program, which includes global variables that are subject to change.
2.  Pure functions - the same input always gives the same output.
3.  The functions that take a function as an argument, or return a function as a return value are called Higher Order Functions.
4.  When the functions are passed into another function or returned from another function, then those functions which gets passed in or returned can be called a lambda.
5.  Functions must not have dependencies, if a dependency is needed then it must be passed as an argument, always declare your dependencies explicitly.

​ Following are some brief over-simplified guidelines for functional programming newbies:-

1.  Write a lot of functions.
2.  Never mess with variables without intent.
3.  Use `const` as much as possible.
4.  Write functions that take other functions as arguments.
5.  Write functions that return other functions as arguments.
6.  Write code in an easily testable way. Here “Tests” mean unit tests, and other automated testing methods.
7.  Functions can be used with constructors to work like Classes, in which case they will be assigned a name starting with a capital letter.

​ Following are some elementary examples of functional JavaScript code compared to regular code:Non-functional example:let x = 6;function double() {  return ++x;}Functional example:let x = 6;function double(input) {  return ++input;}​ Following is an example of embedding methods in the Array object in JavaScript.var myArray = [ 1 , 2 , 3 , 4 ] ;Array . prototype . newMap = function ( callback ){  let neoArray = [] ;  this . forEach (( e , i ) => {    neoArray [ i ] = callback ( e ) ;  }) ;  return neoArray ;} ;var newArray = newArray . myMap ( function ( item ){  return item * 2 ;}) ;​ Notice how we have use the `this ` keyword, and the `callback ` word. The `this` keyword is used instead of Array . The `callback` word refers to a parameter that demands a function as it’s value. This type of code is often used when using functional programming.Note: I don’t recommend modifying the Array object without proper care.​ This concludes the section for writing code for our plugin, the project’s offical repo is at:- [https://github.com/Ray6464/congenial-JavaScript](https://github.com/Ray6464/congenial-JavaScript)​ If you’d like to contribute feel free to make a PR. You can start by writing code for stuff like generating Array.forEach, Array.find(), Array.some(), Array.every(), Array.reduce(), Array.includes(), etc.Chapter 6 - Post-development work, Writing documentation, and Making a pull request​ In this chapter, we will work on one of the most important aspects of Project-development! Writing documentation.​ Ideally, we should be working on refactoring code before writing the documentation, but in this project I’ve decided to leave it to the FOSS army on GitHub. I’ll do some refactoring, but leave the rest to online contributors.Post-development work​ Following is a list of examples of Post-development work that I usually carry out, you should also do it before presenting your work.Examples of Post-development work

1.  Checking each comment and realizing if they are beneficial, removing any useless comments.
2.  Deal with any commented out code.
3.  Make sure your comments aren’t misdirecting others.
4.  Making sure your code follows the 3 R’s of Clean code, Readability, Re-usability, and Refactoring!

Refactoring Comments​ When dealing with comments remember the following quote:“Write code not comments”​ Instead of describing or informing you, I’ll just show you what I mean in the following case-studies of our code.Note: This code is written for instructive purposes.Warning: Don’t get distracted by line numbering in the following snapshots.Case 1​ In this case, we are looking at the `modules/tests.vim` file.Code (before):1   "----------------------2  let numberOfTestsPassed = 03   "----------------------4  5   "----------------------6  let numberOfTestsFailed = 07   "----------------------…Several lines Below...45 " each test is ran on a different line Number46 "----------------------47 let lineNumber = 148 "----------------------Code (After):1   "----------------------2  let numberOfTestsPassed = 03  let numberOfTestsFailed = 04  let headOverlineNumber = 15   "----------------------​ Now compare the “before” and “after” snapshot, in the “before” snapshot we have a ton of lines which makes it look incommodious, in the “after” snapshot we have reduced the lined down to 5 (including beautified comments).​ Another change is the change of name and line number of the variable `lineNumber`; the name is changed to `headOverLineNumber` where “head” refers to the “head” of the device used to explain the Turing Machine concept. This demands that we change the variable name everywhere, in Vim we can use `:%s/lineNumber/headOverLineNumber/g ` to do this.Case 2​ In this case, we are looking at the `modules/tests.vim` file.Code (before):" lines are incremented here so the test-head moves from line #1 -> #2, #2 -> #3, ...let g :headOverLineNumber = g :headOverLineNumber + 1Note: This code is present in the functions `GenerateReport()` and `GenerateMultiLineReport`.Code (after):function ! MoveHeadToNextLine() abort  let g :headOverLineNumber = g :headOverLineNumber + 1endfunction​ Here the comment appears to be in a troubling mood in the “before” snapshot, in the after snapshot we will give it it’s own function (shown in the “after” snapshot), then we will replace code in the “before” snapshot with:call ModeHeadToNextLinein both `GenerateReport()` and `GenerateMultiLineReport` functions.Writing Documentation​ For this project, we have 2 documentation files:

1.  README.md (for GitHub main page)
2.  docs/outline.txt (for basic user info)

​ You can find the content of these files on GitHub at ray6464/congenial-JavaScript. Following is a brief example of outline.txt:Key Bindings to generate Dynamic Boilerplate--------------------------------------------Command   |  Generates (JavaScript)     ,outline  |  Outline of Features        ,var      |  Variable                   ,label    |  Label                      ,loop     |  Loop                       ,array    |  Array                      ,log      |  Stdout aka console.log()   ,timer    |  Timer Loops (setInterval)  ,split    |  Array.split()              ,map      |  Array.map()                ,loarray  |  Loop Over Array (forEach)  ​ The purpose of the `outlint.txt` file is to serve as a short-cut for users to see what features they have available at hand.Making a pull request​ In this section, you will learn how to clone the official Congenial-JavaScript project from GitHub and make modifications to it.​ For the following instructions, you will need a GitHub account, and some basic knowledge of Git usage. Also a Pull Request is easily made with the web GUI provided by GitHub, so it’s not covered here.​ The instructions are provided for linux users, windows and mac users can modify the instructions for their use.Steps To Install the package

1.  Use `cd ~ && git clone [https://github.com/Ray6464/congenial-JavaScript](https://github.com/Ray6464/congenial-JavaScript) ` to fork this repo in your Home directory.

1.  In a terminal go to `~/.vim/after/ftplugin/javascript/ `, make these directories if they are absent!
2.  Make a symbolic-link to the cloned directory with `ln -s ~/congenial-JavaScript `.
3.  Execute `cp ~/.vim/after/ftplugin/javascript/congenial-JavaScript/modules/plugins.vim ~/.vim/after/ftplugin/javascript/plugins.vim `. This primes the plugin to work only in files with `.js` extension.
4.  Now open a JavaScript file in Vim, like `vim something.js ` and try out the magic. The plugin should work now, if not check the latest instructions to install it on your machine.
5.  After the 1st step you will have a clone of my repo in your home directory, once you make modifications to it you can Commit them to Git, and then Push them to the origin repo I created on GitHub using the following instructions. Ideally, we break down bigger commits to smaller ones, but for the sake of simplicity let’s make a big one here.
6.  Once you have made the changes, stage them via `git add . `.
7.  Now commit them via `git commit -m “Write a heading describing the changes you have made” -m “Write a description about what changes you have made” `.
8.  If you’d like to revert an older commit use `git revert CommitRefNumber`.

Steps to make modification and make a pull request​ Following are a few guidelines to follow while working with Git Repositories.

1.  Clone or fork a Repo.
2.  Make any modifications you want to the source-code files.
3.  Never make changes to LICENSE.
4.  Save your modifications by committing them.
5.  Go to `[https://github.com/Ray6464/congenial-JavaScript](https://github.com/Ray6464/congenial-JavaScript/pulls) `.
6.  Make a pull request.

Disclaimer: The author of this book or any other related person/persons cannot be held liable for any loss of data, or any other loss.Chapter 7 - Making the plugin presentable for the portfolio​ In this chapter, we will learn a few tricks to embellish the project and make it more presentable. This chapter provides suggestions to improve the overall appearance of your project.Adding ASCIINEMA casts to your project​ This is a very useful trick, Asciinema is a tool that can record terminal sessions in files called Casts and “asciicast2gif ” is a tool that can convert those casts to GIF images, these images can be included in the README.md file and then can be viewed by potential users.​ Asciicasts serve as eye-candy; they can really prettify a project!Recording an ASCIICAST and putting it on GitHub

1.  You can use ASCIINEMA to record terminals; see installation instructions on their website.

◦         Use `asciinema rec congenialJScast –stdin` to start recording your terminal and saving the data to a file named `congenialJScast`.◦          Use `ctrl+d` to stop recording.◦          Use `asciinema play congenialJScast` to play the cast.

2.  Install `asciinema/asciicast2gif`, See installation instructions form their GitHub repo or install it from npm using `npm install --global asciicast2gif `.
3.  Alternatively you can install and use `svg-term-cli` via `npm install -g svg-term-cli`.
4.  Use `ffmpeg` or any other tool to further edit your GIF files.
5.  Now add these GIF files by putting them in the `docs` directory of your projects and then embedding them your README.md file.

Other suggestions

1.  Use GitHub Pages to provide free hosting to your project’s website. Like `emmet.io`, `cylonjs.com`, etc.
2.  You can also look at free hosting alternatives like Tumbler, nearlyfreespeech.net, 000webhostapp, blogspot, etc.
3.  If you have a commercial project I suggest you to buy a VPS (not VPN), which is basically a Private Server where you have root access, use “Namecheap” for a VPS and “Epik” for domain names (not affiliated marketing advertisements).
4.  Fill your project with good copy (as in copy-writing), you can write this copy yourself or ask someone with copy-writing experience to do this for you.
5.  Once your project is complete send it out to peers or review, post it on Reddit, find people on Angel-list and send them your portfolio.
6.  Make sure to act on useful criticism, don’t let criticism discourage you! The art of scouring and accepting criticism is one of the most useful skills in life.

Kanban Board![](Image00010.jpg)