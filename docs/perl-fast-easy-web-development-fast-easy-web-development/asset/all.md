Cover

![Image](content/583149e04f28ca193ce0338167beca6f.jpg)

* * *

| **title** | **:** | Perl Web Development Fast & Easy |
| **author** | **:** | Bate, Les. |
| **publisher** | **:** | Course PTR |
| **isbn10 &#124; asin** | **:** | 1931841179 |
| **print isbn13** | **:** | 9781931841177 |
| **ebook isbn13** | **:** | 9780585456782 |
| **language** | **:** | English |
| **subject** |   | Perl (Computer program language) , Web site development. |
| **publication date** | **:** | 2003 |
| **lcc** | **:** | QA76.73.P22B39 2003eb |
| **ddc** | **:** | 005.2/762 |
| **subject** | **:** | Perl (Computer program language) , Web site development. |

Page i

**Perl fast&easy® *web development***

Page ii

*This page intentionally left blank.*

Page iii

# Perl fast&easy® *web development*

Les Bate

![Image](content/b71c3bf4ec47ee2a5215ae5d6977ec76.gif)

Page iv

© 2003 by Premier Press, a division of Course Technology. All rights reserved. No part of this book may be reproduced or transmitted in any form or by any means, electronic or mechanical, including photocopying, recording, or by any information storage or retrieval system without written permission from Premier Press, except for the inclusion of brief quotations in a review.

| ![Image](content/b71c3bf4ec47ee2a5215ae5d6977ec76.gif) | The Premier Press logo and related trade dress are trademarks of Premier Press, Inc. and may not be used without written permission. All other trademarks are the property of their respective owners. |

**Publisher:** Stacy L. Hiquet

**Marketing Manager:** Heather Hurley

**Acquisitions Editor:** Kevin Harreld

**Project Editor:** Estelle Manticas

**Technical Reviewer:** Michelle Jones

**Copy Editor:** Kate Givens

**Interior Layout:** Jill Flores

**Cover Design:** Mike Tanamachi

**Indexer:** Kelly Talbot

**Proofreader:** Kim Benbow

Perl is a registered trademark of Larry Wall. All other trademarks are the property of their respective owners.

*Important*: Premier Press cannot provide software support. Please contact the appropriate software manufacturer's technical support line or Web site for assistance.

Premier Press and the author have attempted throughout this book to distinguish proprietary trademarks from descriptive terms by following the capitalization style used by the manufacturer.

Information contained in this book has been obtained by Premier Press from sources believed to be reliable. However, because of the possibility of human or mechanical error by our sources, Premier Press, or others, the Publisher does not guarantee the accuracy, adequacy, or completeness of any information and is not responsible for any errors or omissions or the results obtained from use of such information. Readers should be particularly aware of the fact that the Internet is an ever-changing entity. Some facts may have changed since this book went to press.

ISBN: 1-931841-17-9

Library of Congress Catalog Card Number: 20011096997
Printed in the United States of America

03 04 05 06 07 BH 10 9 8 7 6 5 4 3 2 1

Premier Press, a division of Course Technology
2645 Erie Avenue, Suite 41
Cincinnati, Ohio 45208

Page v

*To my lovely wife Pauline, and my beautiful daughter Victoria
with all my love…
and to my cats Cassie and Biggles for walking across my keyboard*!

Page vi

## **Acknowledgments**

There are many people that I should like to thank and I am bound to forget someone, I am sorry if one of them is you!

First I should like to thank Julie C. Meloni, who told me my first sample text was good enough. Also thanks to Lynette Quinn for her encouragement in the early stages. Likewise thank you to Estelle Manticas, for encouraging me with her good humor and helpful remarks, and for turning my gibberish into this book. Thanks to Kevin Harreld, who kept me on the rails throughout.

Thank you to my wife Pauline and my daughter Victoria for putting up with my absences.

I would also like to thank my past UWE lecturers, especially Simon Langley, Nigel Baker and Jane Berry, who fired up my enthusiasm for computing, and in the case of Simon, fired up my sense of humor too!

Thank you to Mum and Dad for being my Mum and Dad!

Finally, a special thank you to my good friend Clarisse Craen, who gave me the initial shove to start this project: thank you, my mate!

Les

Page vii

## **About the Author**

**LES BATE** is a Senior Analyst Programmer working for CSC at the British Aerospace (Airbus) site in Filton, Bristol, in the UK. He started out as a TV engineer for Visionhire in the West Midlands, England, spending many years at college learning about analogue and digital electronics before becoming a self-employed electronics engineer.

Les later switched careers and moved into systems analysis and programming at British Aerospace. Originally working on mainframe batch and CICS programming, Les finally made the move into Lotus Notes development and from there to Web development.

In 1998 he gained a BSc (Hons) in Computing from the University of the West of England, which he says opened totally new horizons for him in terms of technology and its application in computing.

Les has used many of the currently available technologies, including C, C++, Perl, PHP, Java, JavaScript, VBScript, ASP, and HTML, and he enjoys exploring the possibilities that new technologies offer.

In his spare time he messes around with electronics, plays the guitar (he says very badly!), and enjoys listening to music, traveling, and reading. He attributes his love for reading solely to the works of J.R.R. Tolkien.

Page viii

## **Contents at a Glance**

| **Introduction** | **xv** |
| **Chapter 1** Getting Started | 1 |
| **Chapter 2** Taking Your First Steps with Perl | 21 |
| **Chapter 3** Perl Data Types: Scalars | 33 |
| **Chapter 4** Operators | 51 |
| **Chapter 5** Array | 81 |
| **Chapter 6** Hashes | 95 |
| **Chapter 7** Program Flow | 105 |
| **Chapter 8** Perl Functions | 119 |
| **Chapter 9** A Diversion: HTML | 145 |
| **Chapter 10** CGI Programming | 191 |
| **Chapter 11** CGI: Making the Connection | 221 |
| **Chapter 12** Using Files in Perl | 235 |
| **Chapter 13** Sending E-mail in Perl | 259 |
| **Chapter 14** Using Perl with Databases | 277 |
| **Chapter 15** Another Diversion: JavaScript | 309 |
| **Chapter 16** The CGI.pm Module | 341 |
| **Chapter 17** Case Study: A Contact Database | 361 |
| **Appendix A** More Perl Functions | 395 |
| **Appendix B** Web Site Resources | 403 |
| **Index** | **407** |

Page ix

## **Contents**

| **Introduction** | **xv** |
| **Chapter 1 Getting Started** | **1** |
| Where Can I Get Perl? | 2 |
| How Do I Install Perl? | 3 |
| Personal Web Server (PWS) | 11 |
| **Chapter 2 Taking Your First Steps with Perl** | **21** |
| Before You Start | 22 |
| The Basics of Coding in Perl | 22 |
| Perl Syntax | 22 |
| Beginning Perl | 23 |
| Getting Things In and Out of Perl Programs | 26 |
| Getting Input for a Perl Program | 29 |
| **Chapter 3 Perl Data Types: Scalars** | **33** |
| Scalar Variables | 34 |
| Strings | 42 |
| The $_ Variable | 43 |
| Escape Sequences For Formatting | 48 |
|  |  |

Page x

| **Chapter 4 Operators** | **51** |
| The Assignment Operator | 52 |
| Arithmetic Operators | 54 |
| Other Operators | 57 |
| String Operators | 62 |
| Changing Case | 67 |
| Mixing Strings and Numbers | 69 |
| Comparison Operators | 71 |
| Logical Operators | 77 |
| **Chapter 5 Arrays** | **81** |
| Declaring Arrays | 82 |
| Loading Arrays | 88 |
| Joining Arrays | 90 |
| Array Functions and Array Manipulation | 91 |
| **Chapter 6 Hashes** | **95** |
| What are Hashes? | 96 |
| Hash Prefixes | 96 |
| Initializing a Hash | 97 |
| Creating a Hash | 98 |
| Loading and Searching Hashes | 99 |
| Removing Keys from a Hash | 100 |
| **Chapter 7 Program Flow** | **105** |
| What Is Program Flow? | 106 |
| Program Flow in Perl | 107 |
| The If Statement | 107 |
| Loops in Perl | 111 |
|  |  |

Page xi

| **Chapter 8 Perl Functions** | **119** |
| What is a Function? | 120 |
| String Functions | 120 |
| Array Functions | 132 |
| Hash Functions | 139 |
| Subroutines | 140 |
| **Chapter 9 A Diversion: HTML** | **145** |
| Saving HTML Files and Testing HTML Pages | 146 |
| The Structure of an HTML Document | 147 |
| Writing an HTML Document | 147 |
| More Text Formatting | 153 |
| Adding Structure and Color | 155 |
| Images | 171 |
| Hyperlinks | 174 |
| Linking within a Page | 175 |
| Frames | 181 |
| Frame Tags | 182 |
| **Chapter 10 CGI Programming** | **191** |
| What Is CGI? | 192 |
| A Simple Perl CGI Program | 193 |
| HTML Forms | 203 |
| Using the Form | 206 |
| **Chapter 11 CGI: Making the Connection** | **221** |
| Receiving Data from Forms | 222 |
|  |  |

Page xii

| **Chapter 12 Using Files in Perl** | **235** |
| Opening Files in Perl | 236 |
| Reading Data from a File | 237 |
| Error Checking | 241 |
| Writing to a File | 243 |
| Deleting a File | 247 |
| Using Directories with Perl | 249 |
| Data Files | 253 |
| **Chapter 13 Sending E-mail in Perl** | **259** |
| Using FTP | 260 |
| What Is FTP? | 261 |
| Sending E-mail Using SMTP in Perl | 264 |
| Sending E-mail Using Blat.exe | 267 |
| Sending Mail on a UNIX Server Using Sendmail | 272 |
| **Chapter 14 Using Perl with Databases** | **277** |
| Level 1 head here | 278 |
| Creating a Data Source Name (DSN) | 286 |
| Reading Records from a Database Using ADO | 289 |
| Adding Records to a Database with ADO | 294 |
| Updating a Record in a Database Table Using ADO | 296 |
| Deleting a Record from a Database table with ADO | 297 |
| DBI | 299 |
| **Chapter 15 Another Diversion: JavaScript** | **309** |
| A Few Notes about JavaScript | 310 |
| Object Orientation | 310 |
| Elements of JavaScript | 313 |
| Where Do You Put Your JavaScript? | 314 |
|  |  |

Page xiii

| More JavaScript Syntax | 315 |
| JavaScript Variables | 319 |
| Your First Form Validation JavaScript Function | 321 |
| **Chapter 16 The CGI.pm Module** | **341** |
| What's the Idea Behind the CGI.pm Module? | 342 |
| Starting and Ending an HTML Page with CGI.pm | 343 |
| Forms and CGI.pm | 348 |
| Getting Data from Forms | 352 |
| CGI.pm in Object-Oriented Mode | 354 |
| **Chapter 17 Case Study: A Contact Database** | **361** |
| The Requirements | 362 |
| The Home Page | 363 |
| The listcontacts.pl Program | 365 |
| addcontact.htm | 369 |
| The insertrec.pl Program | 376 |
| The editcontact.pl Program | 379 |
| The updaterec.pl Program | 387 |
| The Database | 390 |
| A Final Word | 392 |
| Creating the Record-Addition Script | 308 |
| Populating Your Table | 313 |
| **Appendix A More Perl Functions** | **395** |
| The length() Function | 396 |
| The reverse() Function | 396 |
| The index() Function | 397 |
| The rindex() Function | 397 |
| The substr() Function | 398 |
|  |  |

Page xiv

| The tr/// Operator | 399 |
| The chr() Function | 400 |
| The ord() Function | 400 |
| The join() Function | 400 |
| The sort() Function | 401 |
| The rand() Function | 401 |
| The Here Document | 402 |
| **Appendix B Web Site Resources** | **403** |
| Official Sites for Obtaining Perl and More | 404 |
| Learning More about Perl | 404 |
| Free Perl Scripts | 405 |
| Learning More about HTML and JavaScript | 405 |
| **Index** | **407** |

Page xv

## **Introduction**

Perl was born in October, 1987\. Written by Larry Wall as a Ph.D. project, it first appeared on the comp.sources News Group as Perl version 1.0\. Perl now offers a standard set of supplied libraries, object-oriented programming facilities, and expanded regular expressions. Perl used to be written as PERL (and sometimes still is), reminding us that it stands for Practical Extraction and Reporting Language. That is what it did, back when it was first written. Now it does much more.

Perl is an interpreted language. That means it isn't as fast as languages like C, but it also means you don't have to keep cycling through the laborious process of editing, compiling testing, then re-editing, recompiling, and so on. With Perl, you just edit and run! It's a fast language to develop in and a great one to prototype with! Perl can also be very concise. It is possible to achieve a lot with very little code. In current parlance, then, Perl is a results-oriented language.

Perl has become the ''glue" that allows many other tools to be linked together. It has been "ported" to many platforms and has become an essential tool for OS administrators and Web Programmers. It has been used to build complete systems, and it is also used for creating throw-away code snippets to do one-off jobs. Perl is used world-wide on numerous platforms and with many different Web servers. In many cases it is the default Web language. If an ISP offers any CGI-type programming facilities, it is likely that they will include Perl. If it offers only one language, that language is probably Perl. Perl is powerful, Perl is fast (for an interpreted language!), and Perl is useful! There is virtually no job that cannot be done with Perl, and often jobs can be done with far less code than would be possible using most other languages.

Page xvi

In this book you will explore many of Perl's features before looking at how you can use it to build dynamic Web sites. You will not trawl through huge conceptual discussions on the whys and wherefores of Perl. Rather, you'll take the language and select the methods and mechanisms that can help you most in your quest to write active Web sites. In other words, you'll be exploring ways of solving problems. After all, that's what programming languages are designed to do! My aim in this book is to get you to your destination in the shortest possible time, at the same time seeking to help you understand how Perl works in this field.

### **How is This Book Organized?**

This is very much a ''get you started" book. I have deliberately avoided some of the more difficult aspects of learning a language such as Perl, for that way lies the seeds of exasperation, disillusionment, and the probable abandonment of the language.

You will find that first chapters of the book are concerned with the creation of the Web development environment—installing Perl and a Web server. From there to a little over half-way through the book, you'll find bite-sized pieces of Perl code, each designed to demonstrate one particular aspect of the Perl language. The step-by-step code examples are accompanied by screenshots showing the code and its resulting execution.

From there onwards, you will work to wards building real Perl applications—examining CGI and forms, as well as files and e-mail. The book ends with a full Perl database Web application.

### **Who Should Read this Book?**

This book assumes as little as it is possible to assume. It is aimed at someone who has little knowledge of Web development, or someone who has used WYSIWYG point-and-click-type Web authoring tools and now wants to move into creating Web applications in as short a time as possible.

Page xvii

### **Software/Hardware Requirements**

To use this book and the examples supplied, you will need a Web server. If you're using Windows 95 then you can obtain Personal Web Server. This is often to be found on freebie magazine-mounted CDs lurking in a free product called NT Server 4 Option Pack. The Option Pack also contains Peer Web Services for Windows NT 4, which does the same job. Users of Windows 98 / ME should find that they have a copy of Personal Web Server already on their machine. If not, check your Windows installation CD. Windows 2000 professional / XP Professional users should find they have a copy of Internet Information Server (IIS) on their machine, which is even better. UNIX users can make use of the brilliant Apache Web server available from www.apache.org (a Windows version is also available).

Of course, you will need Perl itself; where to obtain it and how to install it are covered in the book.

You will need an editor to code with. You can use a simple editor, such as Notepad in Windows or Vi or Emacs on the UNIX platform. For Windows, a personal favorite of mine is HTMLPad 2000 (http://www.blumentals.net/). There is also OptiPerl (http://www.xarka.com/optiperl/) which offers a full Integrated Development Environment (IDE) for Perl.

You do not need an incredibly powerful machine to develop in Perl; almost anything will do, as long as it has plenty of memory (128Mb+) and few hundred megabytes of space free for you to develop in.

And of course you will need a Web Browser; most of you will have Microsoft's Internet Explorer already on your machine, but you may also want to try Opera (www.opera.com), an excellent browser that comes with a decent mail client built in.

Page xviii

*This page intentionally left blank.*

Page 1

## **1
Getting Started**

This first chapter will cover setting up Perl on your machine. The emphasis here is for Windows users, but there is no shortage of advice for setup on other platforms. See the useful URLs in Appendix B of this book, where you will find Web addresses for the Perl organization and for huge Perl resources supplying detailed advice, examples, and updates. When you are surfing the Internet, take a look at these sites—they really are awesome sources for all things Perl!

Specifically, this chapter will cover:

![Image](content/d938f552af65a53b177029c39d905885.gif) Where to obtain Perl

![Image](content/d938f552af65a53b177029c39d905885.gif) How to Install Perl

![Image](content/d938f552af65a53b177029c39d905885.gif) Configuring Personal Web Server

Page 2

### **Where Can I Get Perl?**

Perl is available from a number of sources. The best known are http://www.activestate.com and http://www.perl.com.

I advise you not to download a ''development version" of Perl, as doing so may cause some confusion if you get any errors. Development versions of software are, as their name suggests, not final, fully debugged versions and may include bugs that could lead you to think that you had made a mistake in your code. For this reason, development versions of Perl are often referred to as "unstable." When you are more experienced in the use of Perl you may want to try development versions, in order to make use of new facilities provided, but until then it is best to stick to the latest "stable" version.

In addition to downloading Perl, you might want might want to look around at some of the resources available for Perl developers. Some useful Internet sites are given here, and there are more in Appendix B.

![Image](content/59cdbf9790a710347720b20579d20ea2.gif)

These sites will keep you up-to-date with what is happening in the world of Perl and will provide you with invaluable resources for techniques, coding ideas, and loads of news about the Perl language and those who use it. Perl is a natural language for the Internet, so it is equally natural that you will find lots of ongoing support for this powerful and much respected language on the World Wide Web and in News Groups, email lists, and bulletin boards.

Page 3

### **How Do I Install Perl?**

Before you can use Perl, you need to install it and set up the Web server with which you are going to use it. You will learn how to set up the Web server shortly, but for now, here is the information you need to get started with Perl. Perl can be used at the ''command prompt" the way you may have run DOS programs in the old days! Perl began life as a system administration and reporting tool, so it works equally well in this way.

#### **Windows Installation**

**1.** Download Perl from www.activestate.com or www.perl.com.

**2.** When the download is complete, double-click the file to begin installation.

**3.** Follow the on-screen prompts to install Perl on your machine. If the installation fails, you may need to obtain the latest copy of the Microsoft Installer. If you are using the Activestate site, you will find a link to the latest MS installer there under the Downloads link.

The installation process should update the windows path so that the Perl executable can be found. Open an MS-DOS "prompt" command window to run Perl and verify its version.

![Image](content/5b32858dc3d698dfcc4d5a6b520de2f0.gif)

Page 4

![Image](content/dc68634add35451725f047e05bd370e6.gif)

![Image](content/cdce72593c6ac71366b916c11de7024b.gif)

Page 5

![Image](content/1598d7de45333d4220309b70df5a32da.gif)

![Image](content/9576f99551ac1391d9793d0c03b90936.gif)

Page 6

![Image](content/ab869b948df80fc9f2b4d1016ea580e5.gif)

![Image](content/48010c84edc2083d69a8ff525227e2e3.gif)

Windows 95 / 98 allows you to update the PATH variable via the autoxec.bat file. If you are using Windows 98 and you want to use the Windows 98 facilities to update the autoexec.bat, then follow the next set of steps.

Page 7

**1.** Go to the Start menu, at the bottom left of your screen.

![Image](content/84252c48179cd374757c809a42b37b3d.gif)

![Image](content/41630065ceb65c1dc6ce4abb81f4c856.gif)

Page 8

![Image](content/3112624aab930398aabf192868ed4ff2.gif)

![Image](content/58981e38a39677f5776fd4020c39720b.gif)

**10.** You will now be asked to restart your machine. Do so and wait for your machine to reboot.

Page 9

Your machine should now have Perl installed and ready to go.

Now run a simple test to make sure that Perl is working and that your operating system knows where to find it.

![Image](content/3426ac44c4eda57c540d690236938d69.gif)

![Image](content/4b125f115ffad8f62c13bc1bbafc5512.gif)

Page 10

![Image](content/2480c0c0dab286fb7c9acaca8d6c2478.gif)

Assuming all is okay, you are now ready to make a start with Perl!

#### **Installing Perl on a UNIX Machine**

Installing Perl on a UNIX machine is very different from doing so on a Windows machine. To install Perl on a UNIX machine you must first obtain a copy of the Perl Bundle, as it is known, from either http://www.perl.com or from http://www.activestate.com. Note that there is a Production version and a version that is often marked as ''Development." I recommend that you go for the Production version (sometimes referred to as the "Stable" version).

| **TIP** |
| You will also find a number of other useful tools on these sites, as well as lots of helpful articles, tutorials, helpful hints, and so on. |

Having obtained your UNIX Perl Bundle, you must now build your Perl system. For this you will need an ANSI C Compiler. There are a number to choose from, and you may well already have one on your UNIX "box."

In fact, you may already have a copy of Perl on your machine, as many machines are now shipped with Perl as part of the operating system.

Page 11

As with the Windows test, try typing:

Perl -v

If you have Perl you will get a version report; if not, you will get a ''UNIX command not found" message.

It is worth checking around on the activestate.com or perl.com Web sites to see what packages are available. Things are improving all the time, and it is likely that you will find an easy-to-install version for your platform. Just download it, follow the instructions to the letter, and all should be fine.

| **NOTE** |
| Of course there is also a version of Perl for the Mac. Known as MacPerl, it is available from http://www.perl.com. You should be able to find a downloadable version there and unpack it using the well-known StuffIt expander program. If you don't have a copy of that, go to http://www.aladdinsys.com/expander/ and download a copy. (Incidentally, StuffIt is available for other platforms, too!) |

### **Personal Web Server (PWS)**

![Image](content/9598e6261dc6130d4b109963586ffee0.gif)

Page 12

| **NOTE** |
| Apache can be downloaded from http://www.apache.org, and Personal Web Server can be downloaded as part of a download Option Pack from Microsoft. The easiest way to install Personal Web Server (for Windows NT or for Windows 95) is to use the NT Server 4 Option Pack, which is free when downloaded, or is occasionally available from magazine ''freebie disks." 
Note that to view pages through your Personal Web Server, you must use a "special" IP address: http://127.0.0.1, or you can use http://localhost/. |

If you have Windows 98, you should find Personal Web Server easily; it is already available in your program list:

![Image](content/4887cf914aebfdb7e9faab249735ec8c.gif)

Page 13

![Image](content/226685b7bbac5eeb39c4dde0919e9e3a.gif)

| **NOTE** |
| It is not a good idea to have the Web server running when you are connected to the Internet, as it provides a nice gateway for hackers! Make sure that PWS is not in your Startup list, and if it is loaded (you will see an icon in the Taskbar tray), make sure that the server is stopped by using the Stop/Start toggle button when you are on the Internet. |

When your Web server is running, you will see that the Stop button is showing—that is, the server is started. Conversely, when the Web server is stopped, the Start button is visible where the Stop button was. (It sounds confusing, I know, but you will see what I mean as you use it!)

Page 14

The five buttons down the left side are:

![Image](content/ae6ae057ad40975edde086216f79af7c.gif)

#### **PWS Advanced Options**

![Image](content/09fb331a629cd1c6ec0d950645e16206.gif)

Page 15

PWS (and all other servers) allows you to store files other than HTML files in locations outside of the Web server root structure, but allows you to connect the Web server to them by using the Web server alias feature (sometimes referred to as a virtual directory or folder).

Notice also that you get, as a default, a SCRIPTS folder; this is similar to the usual CGI-BIN folder found on most normal Web servers. You will almost certainly find one on your ISP upload (FTP) directory list.

![Image](content/f0f760f3a3720a643e9f00886dfaf022.gif)

The Add button leads you though a wizard to set up a new folder. Let's assume you want to add a new site to your Web server—a site we can refer to as a collection of Web files (HTML and so on) that has a home page at its root and probably a set of other supporting pages, images, and so on.

To illustrate the point, you will now set up a new folder called Test on your Web server.

Page 16

**1.** Create a folder called Test under the C:\inetpub\wwwroot folder.

| **NOTE** |
| You can also create a new folder through the My Computer interface using File, New Options, or through the Windows Explorer interface. |

![Image](content/72ea46f0ba29957f9f9abf72294b77eb.gif)

**3.** Save the file as default.htm in your new test folder.

Page 17

![Image](content/11db94a9250882a063ffe9381f5730c5.gif)

![Image](content/c803947b24a7b04c92ce048b25c62ec7.gif)

Page 18

| **CAUTION** |
| Note the Access check boxes below the main window. These set the access options for your new folder or virtual directory. You will probably find Read and Scripts access already checked. These are the ''safe" options that allow scripts and HTML pages to be run and read, respectively. The middle option, Execute, is to allow you to run executable programs within your folder. This is potentially dangerous if the folder also has "write" access set up in the Operating System permissions. Also, many commercial Web servers have a "write access" feature in the web server, and UNIX allows you to set permissions through the use of the CHMOD command. 
Whichever platform you have, always bear in mind that it is dangerous to have a folder that has both execute and write access. This allows a hacker to potentially install his own program into your folder and then to execute it and to write to your disk – with possibly disastrous results! |

![Image](content/1841f70e40480678cdf58d2124404f3a.gif)

Page 19

![Image](content/2bd20662d88ab168f10765e4940d3092.gif)

If you are using a different Web server, follow the vendor's instructions to get to a similar point with your chosen server.

You should now have a working Web server and a working copy of Perl, and we can now start to discuss the basics of Perl.

Page 20

*This page intentionally left blank.*

Page 21

## **2
Taking Your First Steps with Perl**

This fairly short chapter is meant to get you started by writing a simple Perl program and running it, and, hopefully, understanding what's going on in the process.

As Perl is an interpreted language, (a language in which each line of code is converted into machine code and immediately executed) it is fairly easy to test. You can keep your editor open and run your code in another window. If there is a problem, you can nip back into your editor, make changes, and run it again, repeating the process until you get it right. Since most of the problems you encounter will be typos, this is a very convenient way to work.

Though Perl is actually quite fast for an interpreted language, you will eventually be using it in online applications, where speed is not normally a huge issue (compared, for example, to high-volume batch processing).

In this chapter you will learn:

![Image](content/d938f552af65a53b177029c39d905885.gif) The basics of coding in Perl

![Image](content/d938f552af65a53b177029c39d905885.gif) Basic Perl syntax

![Image](content/d938f552af65a53b177029c39d905885.gif) How get input for a Perl program

Page 22

### **Before You Start**

It will be useful at this stage to decide which text editor you'd like to use to write and edit your programs. There are many available, from Notepad (on Windows) and Vi (on UNIX) to more sophisticated editors with specific language-support functions, buttons, and help. A good starter's editor is HTMLPad 2000\. It is great for HTML, Perl, and quite a few other languages, and although it doesn't offer real language support, it does ''color code" your source code, making it easier to read. HTMLPad 2000 is a nice, easy-to-use editor to learn with; later, you can choose an editor that includes the language support you want and works in a way that suits you.

For this chapter, and for the next few chapters, create a new folder anywhere on your hard drive. You could create a new folder called "test" (or whatever you prefer to call it) inside the top-level c:\Perl folder, or create a folder called "myPerl" on your hard drive. It doesn't matter where you put it, really, as long as you can find it easily!

### **The Basics of Coding in Perl**

In this chapter, you will begin looking at the structure of Perl, what elements make up a Perl program, and how to use them. So you can learn the basic concepts, the examples at this stage will be kept as simple as possible. As you proceed into later sections, you will be introduced to other useful Perl concepts and gradually increase your knowledge. Finally, a full CGI Perl sample program will bring together all you have learned, and add new practical elements and concepts as you try the example.

Now it's time to learn how to put Perl programs together and how to represent and manipulate data. You'll also have a chance to examine some simple processing mechanisms.

### **Perl Syntax**

You don't need to learn all parts of Perl syntax in this chapter, but there are a few general points you need to understand before you can begin to put together a Perl program.

Page 23

#### **Statement Formatting**

Following are a few definitions to help you with statement formatting:

• A *statement* is the smallest complete unit of code that actually does something. It is the computing equivalent of a sentence in English.

• An *expression* is a value, or an arithmetic, algebraic, or string value.

• A *comment* is a line (or more than one line) that performs no function in the program. It is descriptive text used to help a human reader to understand what is going on in the code. Each line of a comment in Perl starts with a # sign.

Perl is a *free format* language. That is, there can be as much white space (spaces, tabs, line breaks, and so on) as you wish. This means that you can write your code in a manner that makes it a lot more readable than some other languages.

It also means that Perl needs some way of showing when it has reached the end of a statement. This is achieved by the use of the semicolon (;). So a Perl statement may look like this:

print ''I think Perl is great \n";

This is a common method of terminating a statement. C, C++, Java, PHP, and Pascal, among others, all use the semicolon to terminate statements; so if you are coming from one of those languages, you will be familiar with this already.

Okay, assuming you have selected which editor you would like to work with, you can now plunge into some Perl and see how it hangs together!

### **Beginning Perl**

All Perl programs should begin with what is affectionately known as the "shebang" statement. The shebang statement should occur in the beginning at the first column on the first line of the program, and it should contain the file path to the Perl interpreter, perl.exe. Why it should be called the "shebang" statement is open

Page 24

to debate, but it is typical of the type of names that are used in computing for some special characters (the exclamation mark is often referred to as the ''shriek" or the "splat").

The shebang statement starts with a # sign, indicating that it is a comment line. However, it is actually the one exception to this! On UNIX systems, this line tells the operating system where to find Perl so that the program can be executed.

| **NOTE** |
| Remember: A Perl program should always begin with 
"#!pathname_to_Perl,

in column 1, line 1. |

![Image](content/33549e68164280b7e867150c26ec4542.gif)

Page 25

![Image](content/0ef74731c8a15bca09ed8211e9d798f1.gif)

Note, though, that for Windows, this is purely a comment!

![Image](content/8083fa0014e484251ef12143f22545b4.gif)

| **CAUTION** |
| Here is an important difference between the UNIX and NT platforms. Any statement starting with a # is regarded by Perl as a comment and is therefore ignored by the interpreter. An exception to this is the first line of a Perl program, as described earlier. This first statement tells the UNIX operating system where to find the Perl interpreter. As long as the program file is made an executable file (by setting chmod to 755), then just typing its name will cause it to run. 
You can of course still use the -w flag on the command line in NT. |

Page 26

On the NT platform, this first line will be treated as a comment. However, NT uses ''association" between a program and the file extension of its file name. In other words, when Windows NT (and Windows 9x, and so on) sees a .pl extension, it will automatically invoke the Perl interpreter.

### **Getting Things In and Out of Perl Programs**

We have already seen that we can display things on the screen by using the Perl print command:

![Image](content/e1d11719c13e1653ddef2f88f5249731.gif)

(Note the semicolon at the end of the statement.)

**4.** Save this little program as 02-01.pl in your "Test" folder.

Page 27

**5.** Open an MS-DOS command prompt, go to the place where you saved your program, and type:

perl 02-01.pl

Your program should display the simple message:

Perl Fast & Easy Web Development!

#### **Print Formatting**

Before you can achieve anything very exciting with your Perl print statements, you must take a small diversion. You will revisit the subject again later, in Chapter 3, but it's worthwhile to learn a little about print (screen display) formatting so that you can use it in the early sample program code snippets without getting too confused.

Output to the screen can be formatted using the built-in ''escape sequences." Table 2.1 lists some common escape codes.

| **TABLE 2.1 Common Escape Codes** |
| **Escape code** | **Meaning or effect** |
| \n | Inserts a newline character |
| \t | Inserts a tab character |
| \r | Go back to the beginning of the current line (that is, carriage return but no newline) |
| \\ | This is how you add a backslash to the output string (otherwise, it would "escape" the next character. |
| \" | As above but for double quotes |
| \' | As above but for single quotes |
| \$ | This is needed to stop Perl interpreting a $ for the beginning of a variable. |

Page 28

So try the following:

![Image](content/b6fc6dc698fbf23ac57371ee96e7a1de.gif)

| **NOTE** |
| A *newline* is an empty line created by forcing carriage returns. |

**6.** Save the program as 02-02.pl in your Test folder.

![Image](content/ae1f0c48ac101d6cc6ec8deb57aa4b8a.gif)

Page 29

### **Getting Input for a Perl Program**

One of the most useful functions provided by any language is to allow the user to provide input for your program, to make your program interactive. Perl can operate as a command line programming language and it can accept input from the user at the command line.

Try the following:

**1.** Open your text editor.

![Image](content/0d69b9b1ed806c6df0e27adc9a5e7f0d.gif)

**6.** Save the program as, say, 02-03.pl.

**7.** Open an MS-DOS Command box.

Page 30

![Image](content/1fd6e30c1c2a6fc2a7f93f727d073ed0.gif)

**9.** Type in your name and press the Enter key.

![Image](content/e6d67eba15611c34e9f5ae9d97c49bf6.gif)

So how does this program work?

Page 31

Here is the program again with line numbers:

![Image](content/d583f6a23f3beb26f3292bf08ea591ef.gif)

Note that the variable remains inside the printed string. Perl substitutes the variable with the value contained within the variable.

You've made a start. You can write a small program to obtain user input and to display a message. But most computing problems are about data. To be able to manipulate data, you need to be able to store it in your programs. So, next you will start to learn about variables.

Page 32

*This page intentionally left blank.*

Page 33

## **3
Perl Data Types: Scalars**

Perl has four built-in data types. They are scalars, arrays, hashes (also known as associative arrays) and references (used for file handles and so on). *Scalars* are basically single items of data. *Arrays* are lists of data accessed by means of a numeric subscript, and *hashes* are lists of data accessed via another scalar variable or literal; arrays and hashes will be covered in later chapters. A *reference* is a ''pointer" to something else. For example, references are used as "file handles" in order to point to a file (you will examine files in Chapter 12, "Using Files in Perl").

This chapter concerns the scalar data type in Perl. Specifically, you will learn about:

![Image](content/d938f552af65a53b177029c39d905885.gif) Scalar variables

![Image](content/d938f552af65a53b177029c39d905885.gif) Strings

![Image](content/d938f552af65a53b177029c39d905885.gif) The $_ variable

![Image](content/d938f552af65a53b177029c39d905885.gif) Escape sequences for formatting

Page 34

### **Scalar Variables**

All scalar variable names are preceded by the dollar sign ($). So, for instance, the variable to hold the age of a person may be written as

$age

If you are not used to languages that use this kind of variable notation, you could easily forget the $ and find some strange errors creeping into your code.

| **NOTE** |
| Perl variable names are case sensitive. Case-sensitivity is common in modern languages, but do keep it in mind, as it can be the source of some frustration when debugging Perl programs. |

Scalar variables are variables that hold a single value. They can be integer, string, floating-point numbers (real numbers), or references. A reference scalar variable is a variable that simply holds the address of another variable; that is, it is a pointer to that variable.

An integer scalar is simply a variable that holds a whole number:

$age = 20;

Of course, you can do all the things that you can normally do with a numeric variable. To demonstrate this and to show how you use simple arithmetic in Perl, try the following:

**1.** Open your text editor.

Page 35

![Image](content/d4827923e9acabca146a5852cca24bc0.gif)

| **NOTE** |
| Blank lines are optional, but they do help to make the program easier to read. Code that follows on line after line looks a bit crowded. Leaving blank lines between blocks of code that logically belong as a group is easier on the eye and the brain! |

The first of the three lines is a print statement to display what you are about to do. The second creates a variable called $result and assigns a value to it equal to the result of $number_one + $number_two. The third statement is another print statement to demonstrate the result.

Page 36

![Image](content/d11aca275cb3ac519ba65331018ed384.gif)

![Image](content/d4cd7173bb0be655c06a00beef14314f.gif)

Page 37

![Image](content/d3b2149305f5d54541538ad56ad86103.gif)

**10.** Save the code in your test folder as 03-01.pl.

**11.** Open a DOS command prompt.

**12.** Navigate to your program test folder.

**13.** Run your code using the perl 03-01.pl command.

Page 38

![Image](content/9f390b26279fadd59a0f7d8b6fa0122f.gif)

If your output does not look correct, return to Step 2 and look for any typos.

This exercise demonstrates the simple arithmetic operations you might want to perform using the normal arithmetic operators.

#### **Other Operators**

There are a few more simple operators that might look a bit strange. These are the increment, decrement, and the assignment operators. Let's have a quick look at those.

**1.** Open your text editor.

![Image](content/4dc4cff798c6e397284d1b7e85084208.gif)

**3.** After a blank line, create a variable called $number and assign the value 5.

$number = 5; #Normal "assignment"

Note the comment preceded by the hash symbol.

Page 39

![Image](content/a0c80448cd88dc5ab8596b2d9a40b28f.gif)

| **NOTE** |
| Note that the variable name, $number, is preceded by a backslash (\) so that the variable is not *interpolated* (that is, its name is printed rather than its value). At the end of the line the variable is printed, and this time there is no backslash, so the variable is replaced by its value. There are two further newline characters at the end of the line, so there will be two more carriage returns in the displayed output. |

Page 40

![Image](content/9c94e4bf097b048dc861ea8002afc7ba.gif)

![Image](content/7f70820f1f25606570380160b1b53a02.gif)

Page 41

![Image](content/168255912fe818e9d606ee7a1f24d983.gif)

**9.** Save the code in a test folder as 03-02.pl.

**10.** Open a DOS command prompt.

**11.** Navigate to your program test folder.

**12.** Run your code using the perl 03-02.pl command.

![Image](content/cb0b2bdffec62bd384c9a46752cca17e.gif)

Page 42

| **NOTE** |
| Note the way that comments appear automatically in italics. This is a function of the editor I have chosen to use here. If you are using another editor your comments may not appear in italics, though it is common in most modern editors. |

Looking back at your program, note the backslash (\) before the variable name in lines 6, 10, 15, and so on. This is used so that Perl will print $number as a literal and not try to treat it as a variable. Where the $ is not preceded by a backslash you will notice that the value is substituted for the variable name.

There is a slight complication to the increment and decrement assignment operators. This is that they can occur either before or after the variable. The effect of the operator is the same except that when the operator is before the variable, the value of the variable is updated before the variable is used. If the operator is after the variable, the value of the variable is updated after the variable is used. If you are at all familiar with C, C++, Java, PHP, and so on, you will be familiar with this; otherwise it might sound confusing. Don't worry too much about it for now—uses for these techniques will suggest themselves as you get deeper into Perl.

### **Strings**

Strings are also held in scalar variables, for instance, a person's surname might be held in a scalar, like so:

$surname

But remember, a scalar is a scalar. For example, I can also use the $surname variable to hold a number. However, it is not all chaotic. Perl will recognize that you are using a scalar as a number by the action you are carrying out upon it. For example, if you carry out an arithmetic operation upon a numeric scalar you will get a sensible result.

If you do the same on a scalar variable containing a string you will probably get zero. In other words, Perl recognizes a variable type by the *context* in which it is

Page 43

used; you will often hear the word *context* used in conjunction with Perl data types. If you are used to a ''strongly typed" language this will seem a little strange, but you'll soon get used to it.

### **The $_ Variable**

If you use some functions in Perl that require a parameter or argument but do not supply one, Perl will use its special "default" variable. This variable is $_, and it can have many uses as well as being occasionally the source of confusion.

For example, you would normally expect the print statement to have a parameter passed to it—the thing you want printed. If you do not pass a parameter to print, print does not fail, it merely prints the contents of $_.

Try this:

**1.** Open your editor.

![Image](content/9f65a35bd032b6340024195be926aea6.gif)

Page 44

**5.** Save your program as 03-03.pl.pl.

**6.** Run the program by using the usual command prompt and typing perl 03-03.pl

![Image](content/3a5edd1c49ebf75a70c5705966991df3.gif)

Now, just to prove all of the previous points, try the following program and run it from the command prompt.

**1.** Open your editor.

![Image](content/88d1124e05061e72711c981b92b52352.gif)

Page 45

![Image](content/6b92df1ced2d6370570ffe6f28877b86.gif)

**8.** Save your program as 03-04.pl.

**9.** Run the program (perl 03-04.pl from the command prompt).

Page 46

![Image](content/beaf574c8415f656422b5a4dbfadefeb.gif)

This example shows how scalars can be used for numeric or string values and also what happens when you try to perform arithmetic on a string scalar value.

The last two lines demonstrate the use of the $_ variable. You will use this again as you continue through your exploration of Perl.

Once again, note that the variables in the print statement are enclosed in quotes. Double quotes allow you to interpolate a variable within a string. It is important that you fully understand this mechanism.

$thing = ''Fred"; print "the value of the string is $thing \n";

will give you

the value of the string is Fred

Single quotes work in a similar way for literals, but they *do not* cause interpolation to occur, and so variables are *not* evaluated within a string.

In other words, the following code:

$thing = "Fred"; print 'the value of the string is $thing';

will give you

the value of the string is $thing \n

Page 47

Try it and you'll see what I mean.

Finally, note the \n characters at the end of the print statements. Those familiar with C, C++, Java, PHP, and so on will recognize that this is the newline character. This causes any subsequent text output to move to the next line on the screen. Note that this, too, will not be interpolated as a newline character if singles quotes are used in the print statement.

Single quotes cause escape sequences to be ignored. If you put one of the print statements in the previous program in singles quotes, the \n sequences will be displayed and there will be no newlines.

Note that a scalar variable can contain nothing. For example, if you do the following:

print $string1;

$string1 now exists but has no value. However, you can check for the existence of a scalar using the following:

if (defined $string1) { print ''That variable has been defined! \n"; }

You can even "uninitialize" a scalar variable like this:

undef($string1);

or

$string1 = undef;

You will be examining more things that you can do with strings in Perl as you come to use strings for real.

Page 48

### **Escape Sequences For Formatting**

You have already used the print function in Perl. And you recently learned about the use of an escape character \n to give a newline character—that is, to force a line break and move the text cursor to the next line, and \t to give a tab character.

In Chapter 2 you saw a short table of escape sequences. There are a number of other escape sequences that provide text formatting. See Table 3.1 for a more complete list of these common escape sequences.

| **TABLE 3.1 Escape Sequences** |
| **Escape codes** | **Meaning** |
| \b | Backspace |
| \n | Newline |
| \r | Carriage return (go to the beginning of the line) |
| \t | Tab |
| \b | Backspace |
| \u | Convert the next character to uppercase |
| \U | Convert the following characters to uppercase |
| \l | Convert the next character to lowercase |
| \L | Convert the following characters to lowercase |
| \\ | Display a backslash |
| \' | Display a single quote |
| \'' | Display a double quote |
| \E | End an U or L effect |

Note that the backslash can also be used for purposes other than text formatting. For example, what if you want to display a string such as \n or even just a \ ?

Page 49

You'd place another backslash in front of what you want to print (or to place the string in single quotes). So, if you want to display \n, use

print \\n;

If you want to display a backslash, use

print ''\\";

Also, if you want to display quotes, you can do this:

print "One of the words here has \"quotes\" around it \n";

Now you know how to set up a string value and how to display it. Next you will learn about something that you cannot do much programming without—operators.

Page 50

*This page intentionally left blank.*

Page 51

## **4
Operators**

You have used some operators already, such as the addition (+) and subtraction (-) operators. In this chapter you will learn a little more about them, and about a few new ones.

In this chapter you'll have a chance to examine:

![Image](content/d938f552af65a53b177029c39d905885.gif) The Assignment operator

![Image](content/d938f552af65a53b177029c39d905885.gif) String operators

![Image](content/d938f552af65a53b177029c39d905885.gif) Comparison operators

![Image](content/d938f552af65a53b177029c39d905885.gif) Logical operators

Page 52

### **The Assignment Operator**

The first operator to mention is the assignment operator. This is the equals sign (=), and you have already used it. The assignment operator is common to almost every programming language and doesn't need a lot of explanation.

Very simply, the value on the right of the equal sign is copied—not moved—to the variable on the left.

$surname = ''Smith"; $age = 30;

Try the following little program:

**1.** Open your editor.

![Image](content/53bcb342c59d15808cb473ec9ffd0122.gif)

**4.** Save the program as 04-01.pl or the name of your choice.

**5.** Open a command window and run the program (perl 04-01.pl).

Page 53

![Image](content/aeaa6d4cec1d93c8b0e5936fd3924e9a.gif)

Again, like most other languages, you can *daisy chain* assignments together, so that all variables have the same value and that value is the last one in the chain. (This is often done to set lots of variables at the beginning of a program.)

Try this program.

![Image](content/6ae66b9e406ba26780732d1c188a6b9b.gif)

Your program should look like the one shown here.

Page 54

**4.** Save your program (I've used the name 04-02.pl, you can use any name that suits you).

**5.** Run your program. You should see that all the variables have been set to the same value.

![Image](content/099b151e2b6b1428ad0b0003defc7e26.gif)

### **Arithmetic Operators**

Perl has a familiar (to programmers) list of arithmetic operators.

(+) The addition operator

(-) The subtraction operator

(*) The multiplication operator

(/) The division operator

(%) The modulus operator

(**) The exponentiation operator

Page 55

We have mentioned most of them before, but here's a description of the last two:

• The modulus operator (%) gives the value of the remainder following a division operation. For example:

33 % 7 gives the value 5 (33 / 7 remainder 5).

• The exponentiation operator (**) gives the value of a number after being raised to a power. A simple demonstration would be

5 ** 3 would give 125

That is, 5 raised to the power of 3 (5 3) gives 125.

Just so that you know what they look like when coded, here are a few examples of arithmetic operations as used in Perl.

**1.** Open your editor.

![Image](content/6c85b47f9aa834fae4d4a2118e36453d.gif)

Page 56

**5.** Save your program as 04-03.pl.

**6.** Open an MS-DOS command prompt window.

**7.** Run your program (perl 04-03.pl).

![Image](content/dc0a1e1b5a1fc43e6738310ca203eea5.jpg)

Page 57

### **Other Operators**

Perl also supports the increment and decrement operators, as you discovered earlier; now you can take a look at them in a little more detail. These operators are a shorthand way of updating the value of a numeric variable.

| $counter++; | # This is the same as: | $counter = $counter + 1; |
| $counter-; | # This is the same as: | $counter = $counter - 1; |

If you want to add more than one to a numeric variable, you can do the following.

| $counter+=5; | # This is the same as: | $counter = $counter + 5; |

Similarly:

| $counter-=5; | # This is the same as: | $counter = $counter - 5; |

This shorthand method of updating variables also works with other operators, as shown here:

| $counter %=5; | # This is the same as: | $counter = $counter % 5; |

(That is, divide $counter by 5, and then place the remainder into $counter.)

| $counter*=5; | # This is the same as | $counter = $counter * 5; |

By way of a reminder, here is a little program to demonstrate these operators.

Page 58

**1.** Open your editor.

![Image](content/2697724246cc1959ffbb8aed51b6946f.gif)

Page 59

![Image](content/7e4f52d85f3cdfcd2f4b38d6dd6aba38.gif)

**8.** Save it as 04-04.pl.

**9.** Open an MS-DOS command prompt window.

**10.** Run the program (perl 04-04.pl).

![Image](content/474e1e4dc13def304d30d7a79a32e97f.gif)

Page 60

There is one more thing that is probably worth mentioning before you move on. The increment and decrement operators can occur before the variable name, like this:

++$count;

Initially, it might not appear to be any different than the following:

$count++;

And there isn't a lot of difference. After all, the value still ends up incremented by 1\. The only difference is that, in situations where the variable is used in a loop, the value contained in the variable $count is incremented *before* its value is used in the first case, and *after* it is used in the second case. It might not appear to matter much at first sight, but remember it; I guarantee you will find a reason to use one rather than the other.

Try this simple example to demonstrate the subtle difference.

**1.** Open your editor.

**2.** Start a new file.

![Image](content/c0514e956b6e1e22b94913b0a9b7fa60.gif)

Page 61

![Image](content/26885e25cfa113e3035bfadf1847bc85.gif)

**7.** Save the program as 04-05.pl.

**8.** Open a command window.

**9.** Run the program and observe the results. Can you see the subtle difference?

![Image](content/c6c5906e44fb5dad3af71667a06f44fa.gif)

That is probably enough about numeric operators to give you an idea of how they work. Next you will learn about string operators.

Page 62

### **String Operators**

String operators provide you with some useful methods of manipulating strings; with these operators you can join strings together (known as *concatenation*) or extract ''substrings" from other strings. You will learn about some different string operators in the next sections.

#### **The Concatenation Operator**

You can join strings together in Perl using the "dot" (concatenation) operator. Try this example.

**1.** Open your editor.

![Image](content/08fb7d425924d486b5adc3fa472c98a7.gif)

| **NOTE** |
| It is good practice to do this throughout your programs—you'll be glad you did when you come back later to fix them! |

Page 63

![Image](content/0745905aa0df7f778f282293af0be5ca.gif)

**9.** Save it as 04-06.pl.

![Image](content/0f441d4c672a778ada0b060fefed372b.gif)

**10.** Open a command window.

**11.** Type **perl 04-06.pl** to run your program and observe how the strings have been joined together or concatenated.

As you can see, concatenating strings and string variables is easy in Perl, once you know how!

Page 64

#### **Variable Interpolation Revisited**

You have learned already about interpolation, wherein if a variable is contained within a string enclosed in double quotes, the variable will be replaced by the value of that variable.

$language = ''Perl"; print "The best Web Programming language is $language \n";

will give you

"The best Web Programming language is Perl"

There are occasions when you want a variable value when interpolated to join up to an adjacent word. Consider the following example:

$something = "comfort"; print "This chair is very $somethingable\n";

This is trying to join $something to the literal part able of the main string. Unfortunately, it will not work, as Perl will try to expand a variable called $somethingable. If you add a space to try to fix it, obviously you'll get a space in the result.

Try this example and prove it to yourself.

![Image](content/b092a92598fb7c57f58481826777f785.gif)

**2.** Save the code as 04-07.pl.

**3.** Open a command window.

**4.** Run your program.

Page 65

![Image](content/0df27df2da563a799b518141b6f43026.gif)

Note that you have a space between comfort and able—that's not what you want!

But Perl has a fix for this. You can wrap your variable name in braces.

![Image](content/24a4638380e8b46f439af30244974974.gif)

**3.** Re-save your program.

**4.** Open a command window.

Page 66

![Image](content/6d71bcd8d3c7a1a541e27d2fca26ae45.gif)

That's better! Again, this is another example of something very simple, but very useful, fixing a potentially frustrating problem.

#### **Substrings**

Perl enables you to extract a part of a string and print it or place it in another variable. However, the Perl function that performs the substring action is more sophisticated. The syntax of the function is

substr(stringb, startpos, length)

This means you should obtain the value to be found in stringb; that value being taken from the character at startpos for length number of characters.

If that's confusing, try this small program.

Page 67

![Image](content/45d188e878ec49a037606221873169c5.gif)

**4.** Save the program as 04-08.pl.

**5.** Open a command prompt window and run the program (perl 04-08.pl).

![Image](content/f4ffd3ca7354697c1da860c12cb14d9b.gif)

| **NOTE** |
| The length parameter of the substr() function is optional. If you omit it, then substr() will assume that the length value is to the end of the string. |

### **Changing Case**

You may want to change the ''case" of a string, for example, prior to doing a comparison of values. Perl has several strings that perform this function.

Page 68

Very simply, these Perl functions perform the following operations:

• **uc.** Converts a string to all uppercase.

• **lc.** Converts a string to all lowercase.

• **ucfirst.** Converts just the first character of a string to uppercase.

• **lcfirst.** Converts just the first character of a string to lowercase.

Try this sample program.

![Image](content/028f9533e1d5036144cb5c5ed0af3d18.gif)

Page 69

**5.** Save your program as 04-09.pl.

**6.** Open a command prompt and run your program.

![Image](content/00b0dfd6884d8efa8887c8f0c6ee805c.gif)

As you can see, Perl is a very powerful language with some very useful string functions. In fact, Perl is extremely rich in functions for all kinds of purposes. You are learning a lot of the most useful ones, and there is a wealth of others just waiting for you to discover them. And all the time, the army of Perl authors and programmers are creating more functions, helping to keep Perl as one of the most powerful languages around.

### **Mixing Strings and Numbers**

As you learned earlier, Perl decides what to do with a scalar variable based on context in which it is being used. This can lead to some confusion unless you're ready for the results!

Try the following code example and read the comments against each line in order to understand what is happening; then, if you wish, enter the code into your editor and try the program out.

Page 70

![Image](content/ae1c19b390f3f5416719c6430bbd1444.gif)

**5.** Save the program as 04-10.pl.

Page 71

![Image](content/1c97ebebb88404bda42f03e06c437bb1.gif)

Can you follow through what's happening? The rule is that Perl will treat a scalar variable as the type it appears to be. If it looks like a number, Perl will most likely treat it like one. Copy the above snippet of code into a new Perl program file in your editor, save it, and try running it. Play with the code and test what works and what does not.

### **Comparison Operators**

When you write if statements, you use comparison operators to test the value of strings, numbers, and so on.

#### **Numeric Comparison Operators**

If you are testing numeric scalar values you would use the following comparison operators.

• (>) Greater than

• (==) Equal to

• (<) Less than

• (>=) Greater than or equal to

• (<=) Less than or equal to

• (!=) Not equal to

Try the next program to see the use of numeric operators.

Page 72

**1.** Open your editor.

![Image](content/7a9e080323654c96d1ebe8b5655fae55.gif)

| **NOTE** |
| The if statement is described in Chapter 7, ''Program Flow," but I hope you have been able to follow the simple if statements used here. If not, return here after reading Chapter 7 and reexamine this code. |

**4.** Save your program as 04-11.pl.

**5.** Open a command window.

Page 73

![Image](content/1178b5f250ee8cea206bd876585b518e.gif)

| **NOTE** |
| It cannot be emphasized enough about the use of the equality comparison operator == when checking for equality of values. Remember that the = sign is an *assignment* operator. This is the source of many bugs. |

Other similar operators are used in exactly the same way as the previous example.

if ($numvar > 5) { print ''You chose a number greater than 5 \n"; } if ($numvar >= 5) { print "You chose a number greater than 4 \n"; }

And so on.

You will be using numeric operators again later. Their use is pretty obvious, as later examples in real Web application code will show.

Page 74

#### **String Comparison Operators**

The above operators (==, <, >, and so on) should only be used for testing numeric values. Why? Try the following program, which will demonstrate the difference between numeric comparisons and string comparisons.

![Image](content/e0c64420293cbcc185c68e3fe5d74553.gif)

**3.** Save your program as stringcomp1.pl.

**4.** Open a command prompt window and run your program.

Page 75

![Image](content/076174661d8523e0022b636e337741a7.gif)

The reason for this is that = = is a numeric comparison operator, and so Perl will interpret $string1 and $string2 as numeric variables. Because Perl will be unable to evaluate them as numbers, they will be set to zero. Therefore, both variables are numerically equal and so the test is passed and the string ''Those two names are the same!" is printed.

For this reason, Perl has a different set of comparison operators for strings.

• **eq.** Equal to

• **ne.** Not equal to

• **it.** Less than

• **gt.** Greater than

• **le.** Less than or equal to

• **ge.** Greater than or equal to

These operators are used in a similar manner to the numeric ones, but obviously only with string variables.

Here is an identical program, except you will be using the string eq comparison operator, and there is an else option to catch the result; otherwise you would see no output.

**1.** Open a new file or copy the previous one.

Page 76

![Image](content/e973c5fe246bd23ca19d71322d7f7cc4.gif)

**5.** Save your program as 04-13.pl.

Page 77

![Image](content/e9b0056c730e5a1e5d3694224d87ccc5.gif)

Before we leave operators for now, you will learn a little about logical operators.

### **Logical Operators**

Finally, in your brief examination of operators, comes the logical operator. A *logical operator* is used to evaluate whether or not a condition being tested is true or false. You will often see True and False capitalized, as here, to emphasize that this is a logical, or Boolean, value.

The term *Boolean* comes from the name of a mathematician, George Boole, who pioneered the rules of a logical form of algebra. Computers rely on the logic to work, and so you will often come across the terms *True* (often represented by the value 1, but can be represented by any non-zero value) and *False* (often represented by the value zero).

A numeric True value is any non-zero value and, therefore, numeric zero equates to False. So 1, 5, 7, 232, -175, and so on are all True. Only numeric zero is False. We can apply True/False checks to strings, too. The word Olympic is True, a string containing ''0" is True, and a single empty space is True. Only the absence of any alphanumeric characters at all is False.

Page 78

There are basically three logical operators: and, or, and not.

This means that you can check whether two variables have a value simply by doing this:

if ($num1 and $num2) { print ''Both of those variables have a non-zero value.\n"; }

Or you can say:

if (not $num1) { print "That variable is empty.\n"; }

And you can say:

if ($num1 OR $num2) { print "One of those variables has a non-zero value.\n"; }

You can combine conditions such as:

if ($num1 and $num2 or $num3) { print "Both of the first variables have a non-zero value or that last one does!.\n"; }

The logical operators all work in exactly the same way. As you have discovered, the empty string equates to False, and all other values equate to True.

Page 79

Finally, there are symbols that can be used instead of and, or, and not.

|| is the same as the or logical operator

&& is the same as the and operator

! is the same as the not operator

The only difference between using these instead of the word operators and, or, and not is that the symbol version has a greater precedence. That is, a || will be dealt with before an or. Don't worry about that too much. If you want something evaluated before something else, just enclose the one want you want done first in parentheses.

Logical operators seem simple, but misuse can lead to very confusing errors. You will use logical operators quite a lot later. Try using the previous examples and playing with the code, or just read on and wait for some real examples.

Page 80

*This page intentionally left blank.*

Page 81

## **5
Arrays**

*Arrays* are simply collections of scalars. The array has a name much like the simple scalar does, but it also has a number of elements. Each element has the same name and is pointed at by a numeric subscript.

In this chapter you will learn about:

![Image](content/d938f552af65a53b177029c39d905885.gif) Declaring arrays

![Image](content/d938f552af65a53b177029c39d905885.gif) Loading arrays

![Image](content/d938f552af65a53b177029c39d905885.gif) Joining arrays

![Image](content/d938f552af65a53b177029c39d905885.gif) Array function and manipulation

Page 82

Conceptually, an array can be thought of as a number of ''pigeon-holes," each of which can contain separate items of data. As mentioned, each element shares a common name with all of the others, and uses a *subscript* (a sort of address) to determine which element in the array is being referenced.

You will remember that the scalar variable was preceded by the dollar sign ($). The array uses a prefix to make it instantly recognizable just as the scalar variables do. Scalar variables use the $ sign as a prefix, whereas arrays use the @ sign instead, so that you can instantly recognize that it is an array in a program source code listing.

| **NOTE** |
| As in most programming languages, the first item in an array is element zero. I will mention this again as time goes on, and I'll make no apology for doing so, as it cannot be emphasized enough. This concept can be the source of some confusing programming errors if you are not used to it. |

### **Declaring Arrays**

You can declare an array prior to use, or you can load the array at the same time that you declare it.

An example will illustrate the point.

**1.** Open your editor and start a new program.

Page 83

![Image](content/6cdf8084fe32fecd96c86895371e1d93.gif)

**4.** Save your program as 05-01.pl.

**5.** Now open a command window.

**6.** Run the program (perl 05-01.pl)

Page 84

![Image](content/6a4cc76f958d702494b4649b7d33b81a.gif)

You can have a break in a range when defining an array, like this:

![Image](content/3139fc13d5608ced561c361291522386.gif)

**3.** Save your program as 05-02.pl.

Page 85

![Image](content/ac78016af59738db843ee75766be3617.gif)

You can do the same thing with characters, like this:

![Image](content/85b55fcd34a60f96ea44dcedea32708b.gif)

Page 86

**3.** Save your program as 05-03.pl.

![Image](content/df7f9382f48a0df2793ac64afa03bab6.gif)

You are not limited to using one character, either.

![Image](content/736efe2a4d55d024b8aef2ba5b89f0f2.gif)

Page 87

This time brackets (parentheses) have been used rather than the simple carriage return so that you can see all of the values and validate the output from this program.

**3.** Save the program as 05-04.pl.

![Image](content/cdfecc1fd3b0c2a4d83deab3f7f91b37.gif)

And finally, you can mix the element types, like this:

@things = (''Fred", 16, 57.23456, $title);

Here, there is a literal string, an integer, a floating point number, and a scalar variable containing whatever it does.

![Image](content/d0d584be255a6e9f9b78ee0ed891162d.gif)

Page 88

**3.** Save it as 05-05.pl.

![Image](content/389327290c46cc64dac349c06fc874ad.gif)

**5.** Run the program. You should see this.

### **Loading Arrays**

There is a lot that you can do with arrays, and many functions are available to manipulate them. Here are a few examples.

Say you have an array called ships. You can load it like this:

@ships=('Bismarck', 'Titanic', 'Hood', );

And you can refer to the individual elements of the array by the use of a numeric subscript like this:

$shipname = @ships[1];

Page 89

![Image](content/94d056126148ba8d0e1e05f135ef74d2.gif)

![Image](content/a3c4f3dfd6cb921a2a996ef3b803aea4.gif)

**5.** Run your program. You should get this result.

Note that as arrays start with element 0 (zero), the subscript 1 points at the *second* element in the array. So the following statement:

Print @ships[1];

will print

Titanic

Page 90

### **Joining Arrays**

You can also join arrays together. If you take two arrays like this:

@warships = ('Hood', 'Bismarck', 'Washington'); @passengerships = ('Titanic', 'Olympic', 'Britannic');

You can join them together like this:

@ships = (@warships, @passengerships);

![Image](content/d68a03e2976a874d5265be12ce1db7ed.gif)

Page 91

| **NOTE** |
| You could use a loop, as you did in some previous examples, to display the contents of the array. |

**4.** Save your program as 05-07.pl.

**5.** Open a command window.

![Image](content/d2ed2fbde6f10ff8c48e70d18ee3a0e5.gif)

### **Array Functions and Array Manipulation**

Perl arrays are pretty flexible, and really, you have only just scratched the surface of what they can do. There are also lots of built-in functions that are designed to help you manipulate arrays, as you will learn.

Would you like to know how many elements there are in an array? Try this:

print $#ships;

Now try the modified program.

Page 92

![Image](content/88aa0aa009edb261bbd6857ae744fc26.gif)

**2.** Save your program as 05-08.pl.

![Image](content/b4bf88a201cda72db8a738a5659dfc93.gif)

| **NOTE** |
| If you used the array example you tried a minute ago, you will get a result of 5\. (Don't forget that Perl arrays start at element 0, so if there are 6 elements, that will give you a result of 5). |

Page 93

Want to fill an array with 250 zeros? This will do the trick:

@zeros = (0) x 250;

It looks a little confusing doesn't it? But it just means to take a zero and load it into a new array element 250 times and then call the array ''zeros"!

Try it and see for yourself.

![Image](content/5f3dfe5a7711886acdbec9943588d68c.gif)

**4.** Save the program as 05-09.pl.

Page 94

![Image](content/8c4add94f1fa215e94bbe97dfddcacbb.gif)

Perl, unlike most other languages, supports only single-dimensional arrays, and so two-dimensional arrays must be simulated using arrays of references, or pointers. You'll have a chance to examine references soon.

Page 95

## **6
Hashes**

Hashes are sometimes regarded as a difficult subject in Perl. This perception is largely due to the so-called ''misleading and inconsistent" syntax. For this reason, the beginning of this short chapter includes a discussion of what hashes are and how you refer to them in Perl. Hopefully, you will see that hashes are not only useful, but also perfectly logical! You will then learn and practice how to use this powerful data structure. So, read on and bear with me; the short ride will be worth it.

In this chapter you will learn what a hash is and how to use hash prefixes, as well as how to:

![Image](content/d938f552af65a53b177029c39d905885.gif) Initialize a hash

![Image](content/d938f552af65a53b177029c39d905885.gif) Create a hash

![Image](content/d938f552af65a53b177029c39d905885.gif) Load and search hashes

![Image](content/d938f552af65a53b177029c39d905885.gif) Remove keys from hashes

Page 96

### **What are Hashes?**

Hashes (sometimes referred to as *associative arrays*) are similar to ''normal" arrays in as much as they are a list of scalar values. However, the way in which they are accessed is different—the mechanism utilizes "keys" rather than the simple numeric subscript. The important thing to remember about hashes is simply the order in which you quote or specify them, that is, the key and then the value. In most other respects, hashes might be considered a bucket into which you can pour data.

Hashes have a prefix just like scalars and arrays do. For hashes, the prefix is the % symbol. This denotes, when used, that you are referring to the whole hash; if you want to access a single element of a hash you use the $ prefix as you do with arrays. This might seem confusing until you consider that you are only referencing a single scalar within the hash; therefore, you use the scalar notation. Only when you are accessing the whole hash do you use the hash % prefix symbol.

Hashes provide you with a useful lookup mechanism that is a bit like some database tables. A unique key is used to locate a given value. Hashes are uniformly fast; that is, hashes can grow very large with very little degradation in speed, and, as long as your machine has the resources to cope with them, you can make them as large as you like!

Hashes have many uses, not least in Web applications, where they are useful for handling input from HTML forms, CGI environment variables, and other elements, as you will see.

### **Hash Prefixes**

You have just learned that you refer to a hash using the % sign. You will also see the prefixes $ and @ used. Confusing? Well, actually it is quite simple. Always try to think what it is that you are doing with Perl, and all will become clear.

For example, if you are trying to return a single item from a hash, you will see

$item = $hashname{'keyvalue'}

Page 97

Notice that the hash is using the $ prefix. That makes sense doesn't it? It does, because you are returning a single item, that is, a scalar. Similarly, when you want to return a number of values you use this:

@arrayofvalues = @hashname{'keyvalue1', 'keyvalue2'}

This means: return an array of item values from the given hash that correspond to (in this case) the two key values supplied. You are returning more than one item, so you use the @ prefix. Why? You are returning more than one item into an array.

Just to make it more fun, you can even do this:

@arrayofvalues = @hashname{@arrayofkeys}

Instead of supplying the keys in a list in the braces (yes, those are braces, not parentheses), you supply an array of keys. Still, you are returning a number of values just like in the previous example, so you use the hash name prefixed by @.

Like a lot of things in Perl, at first sight things might seem contradictory or illogical, but when you look at them and think about it, it all makes perfect sense. Perl does force you to think, but you soon realize that if it is logical, it will work in Perl. As you become more proficient in Perl, you will grow ideas of your own and you will be amazed to discover that your logical idea works just fine.

You are now going to try creating and manipulating hashes. It's easier than it seems at first, I promise.

### **Initializing a Hash**

To initialize a hash, simply do this:

%animals = ();

You now have a hash called animals, with no keys or values.

You will try this out in a moment, but let's cover a few more simple hash operations first. You will begin by adding keys and values to a hash.

Page 98

### **Creating a Hash**

You can add key-value pairs to a hash individually or many at a time. To add elements to a hash you can do something like this:

$animals{'Horse'} = 'Red Rum';

This adds one key-value pair to the hash animals. (Note the $ prefix. As you saw previously, you use the $ prefix because you are accessing a single element of the hash).

If you want to add several at once, you can do so in the following manner:

%animals = ('Red Rum', 'Horse', 'Jaws', 'Shark', 'King Kong', Gorilla);

Now, this is okay, but have you noticed what starts to happen as you read along the list? As you grow the list, imagine what happens when you try to jump into the middle of the list. With the subjects and names you're using here it is fairly obvious which is a key and which is a value. However, in some cases this will not be quite so obvious, and so Perl has another notation that helps you to determine which is which, no matter how long the list. The notation is known as the *comma-arrow operator* and looks it like this:

%animals = (Horse => 'Red Rum', Shark => 'Jaws', Gorilla => 'King Kong');

Now you can easily see that the => operator is pointing from the key to the data for that pair in the hash. Not only that, but you can now add newline / carriage returns and other whitespace characters and it will still work, so you can make your hash definitions more readable in your programs by using one key-value pair per line, like this:

%animals = (Horse => 'Red Rum', Shark => 'Jaws', Gorilla => 'King Kong' );

This notation is probably called the comma-arrow operator because the => replaces a comma in the previous example. Whatever the reason, the comma-arrow operator makes the pairs easier to identify.

Let's load your first hash.

Page 99

### **Loading and Searching Hashes**

Now you'll learn how to load hashes and how to find data within them. As you are beginning to see, hashes are not much more difficult to use than arrays, and they are very powerful.

**1.** Open your editor.

![Image](content/3511523d14f05cf2e4c0f7d0333921aa.gif)

**5.** Save the program as 06-01.pl.

**6.** Open a command window.

Page 100

![Image](content/aefad4be8c6c691bbb43cf652e99d5b7.gif)

Here is a brief examination of the last program:

Line 3 shows a method of loading a hash.

Line 5 shows how to get a single value back from a hash, given a key.

Lines 7 through 10 show how you can list all of the keys of a hash.

Finally, note that you can print the whole of a hash very simply by using a statement such as

print %animals;

But the results are printed one joined onto the other, which isn't very useful at all!

### **Removing Keys from a Hash**

To remove a single key from a hash, simply use the delete function.

delete($animals{Shark});

Page 101

![Image](content/c15b3f8bf26c93723c7ddf3288f37842.gif)

**4.** Save the program as 06-02.pl.

![Image](content/b0bb09a2b2c719462a6c5779c7243ba4.gif)

You can also remove all the keys (and values) from a hash, like this:

%animals=();

Notice that you have not really deleted anything. You have just *re-initialized* the hash, or started it afresh. But the effect is the same.

Page 102

Once again, modify the previous program and try it.

**1.** Again taking the previous program as a starting point, add the following lines at the end of the program:

print ''\n\n'emptying' the hash …\n\n"; %animals=();

![Image](content/01a4c1d656b86ed840ea0aec652ee59e.gif)

**3.** Save the program as 06-03.pl.

![Image](content/c0fa4b96d2a46df99fca01e712104fc7.gif)

As a last demonstration of hashes (for now), you can test whether a particular key exists in a hash.

**1.** Open your editor.

**2.** Take a copy of 06-01.pl.

Page 103

![Image](content/de2b9f828e5b464ccfd38a4d905e8940.gif)

**4.** Save the program as 06-04.pl.

**5.** Open a command window.

Page 104

![Image](content/5a5fcf8f1970917badc8d730a49aabaa.gif)

As you have discovered, hashes are very powerful and probably easier to use than you first thought. When you get into Web CGI programming, you will use them extensively and you will be thankful that they exist.

This has been enough information to serve as a gentle introduction to hashes. Following this and the previous chapters, you should now have a feel for some of the ways of handling data in Perl.

Next, you will learn a little more about how to control the flow of a program in Perl—how you make decisions and control loops for performing repetitive actions. You have seen some of this already, but the next chapter is entirely dedicated to this subject.

Page 105

## **7
Program Flow**

This chapter will begin with a basic discussion on what program flow is (regardless of the language being used, there is always some kind of flow control in a program). You will then learn how to use flow control to produce the result you want from your Perl programs.

If you are already familiar with basic programming techniques, you may want to skip this short introduction. If you're a Web author branching out into Web development, or someone fairly new to programming who wishes to become a Web developer, you may find this section to be of interest.

In this chapter you will learn:

![Image](content/d938f552af65a53b177029c39d905885.gif) What program flow is

![Image](content/d938f552af65a53b177029c39d905885.gif) How program flow works in Perl

![Image](content/d938f552af65a53b177029c39d905885.gif) How to use the if statement

![Image](content/d938f552af65a53b177029c39d905885.gif) How to use loops in Perl

Page 106

### **What Is Program Flow?**

*Program flow* is the property of a program that gives that program the capability to make decisions or to do repetitive work. In programming logic, there are basically three program structures: sequence, selection, and iteration.

#### **Sequence**

*Sequence* is a mode of programming in which a sequence of instructions is executed in the order in which the instructions are written until the program reaches the end. Most of the old assembly language programs were of this type (with a few ''go to" statements or something similar thrown in).

#### **Selection**

*Selection* is concerned with the route through a program dependent upon values presented to it or values calculated or derived within a program. In other words, when a program is executed, the statements that are executed are decided upon based on certain data. Some of that data might come from outside the program under consideration; other data might be the result of calculations occurring within the program.

The main tools used in selection are variants of the IF and CASE statements.

#### **Iteration**

Iteration is a fancy name for looping. *Looping*, when it is unintentional, can be a programmer's nightmare. But it can also be very useful if used correctly; for example, a loop construct can be used to process records in a file or database.

There are a number of loop constructs; the most common in most languages are the for loop, the while loop, and the repeat loop.

Page 107

### **Program Flow in Perl**

First of all, let us discuss the program block. This is a group of statements that are always executed one after the other. They are wrapped in braces, like this:

{ statement one; statement two; statement three; statement four; }

You can nest a block of statements inside another block. Note that although it makes no difference to the way a program works, blocks of code are usually indented from the rest of the code before and after them. This helps to make code more readable and to simplify future maintenance. Blocks are usually found in loop constructs and IF statements, and these too will be indented, again, just to make the program easier to read.

### **The If Statement**

The if statement is one of Perl's selection statements. It enables Perl to make decisions based on the values contained in variables.

The if statement in Perl is similar to that in C, C++, and other languages.

If (condition) { statement …; statement …; } elsif { statement …; statement …; } else {

Page 108

statement …; statement …; }

Note that often you will find the first curly brace on the same line as the if (condition) part of the statement, like this:

If (condition) { statement …; }

Once again, this is just convention and it is up to you whether or not to adopt it. If you are not working to any set rules within an organization, just be consistent. Otherwise you might confuse people who attempt to maintain or learn from your program.

The elsif/else part of the if construct is optional. You might not need one; in fact, often you will not. Also note that spelling of elsif.

You can also have if statements within if statements or within else clauses, and you will come across many differing examples. You have leaned the basic syntax of the if statement, so now it is time to try one out. You have actually seen this example before, but it won't hurt to cover it again.

**1.** Open your editor.

![Image](content/83d14884e5e23c9fac256bf04e9c18ce.gif)

Page 109

if ($number == 5) { print ''\n\n\$number is equal to 5\n\n"; }

**4.** Save the code as 07-01.pl.

**5.** Open a command window and run the program.

![Image](content/57287b0a581c9eb2c450f13d4ee83fc1.gif)

That was a simple if statement. Here is an if statement using the full if statement syntax.

**1.** Open your editor.

![Image](content/a27762a866560bd69a7cf96c0b6da95b.gif)

Page 110

| **NOTE** |
| This sets the value of $number to 1; then, do whatever is in the loop (between the following curly braces) as long as $number<= 3\. $number++ increments the value of $number on each execution of the loop. |

![Image](content/d333de12bd158227cb263f0004be23f7.gif)

**6.** Save the code as 07-02.pl.

**7.** Open a command window and run the program.

Page 111

![Image](content/518d314f68ce3c2f4ade0f4039b8e7fa.gif)

### **Loops in Perl**

Perl is fairly rich in its loop facilities. Perl can loop while a condition is True. It can loop until a condition is True. Perl can do a loop while or until a condition is True or False, performing the loop at least once. Finally, Perl can loop a predetermined number of times using the for loop. Next you will learn how to use each of these loop structures.

#### **The while and until Loops**

The while loop runs a loop as long as a given condition is True. If the condition specified is not True to begin with, the code within the while loop is never executed. The while loop looks like this:

While (condition) { statement …; statement …; }

| **NOTE** |
| Note that again you will often see the opening brace on the same line as the while (condition)—it is just another convention. |

Page 112

The until loop is very similar to the while loop. As the names of these loops suggest, the while loop continues to loop *while* a given condition is satisfied, whereas the until loop continues to loop *until* a condition arises.

Here is an example with both types of loops.

**1.** Start a new program in your editor.

**2.** Announce what you are going to do (this is optional, of course).

print ''The While Loop:\n";

![Image](content/b94a4eea33f14f1795a5eb1117c6a6f7.gif)

Page 113

![Image](content/f174e855d0fbc0de33f6d97ab94da300.gif)

**8.** Save your program as 07-03.pl.

![Image](content/431549e0361e584b0818e6da8b09b94f.jpg)

| **NOTE** |
| I have not inserted line breaks in the print statements of the program so that the output is captured on a single screen. |

This example uses the shorthand increment operator:

$loopcounter++;

You could of course use

$loopcounter = $loopcounter + 1;

#### **The Do Loop**

The do loop is a variation on the while and until loops; the important difference is that the condition is tested at the end of the loop (either ''while a condition is True" or "until a condition is True") thus ensuring that the loop executes at least once.

Page 114

Here is an example of both the do-while and the do-until loop.

**1.** Open your editor, starting a new program file.

![Image](content/b413b6c33b17c4627499ad0fd71542a2.gif)

Page 115

**7.** Save the program as 07-04.pl.

**8.** Open an MS-DOS command window and execute the program.

![Image](content/aa1af053a212afa5c56f4b1dae92759a.gif)

Both of the loops in this example are similar to the preceding while and until loops, but as has already been stated, the main difference is that the loop in the do versions is executed at least once.

#### **The For Loop**

This is similar to the C/C++ for loop. The format of the for loop is

for(loop_variable = initial_value; loop_termination_condition; loop_variable_update)

The syntax begins with the keyword for, followed by an open bracket, and then the initial condition of the for statement, followed by the test that determines whether the loop should finish or not, followed by the update to the variable being tested. Often this is an increment, but it can also be a decrement value. Finally, there is the closing bracket. Then there is the block of code to be executed while the test condition allows.

Following is an example of the Perl for loop.

Page 116

**1.** Open a new program in your editor.

![Image](content/75db13ed4993efdd1059edbe3eb78f49.gif)

**4.** Save the program as 07-05.pl.

**5.** Open a command window and run the program.

![Image](content/54ded46a49e85f957c7c03053369dbf9.gif)

The increment can also be a decrement, so you might see this instead:

for($linenumber = 1; $linenumber < 10; $linenumber-)

Page 117

You will sometimes see odd implementations of for loops. Try this one:

for(;;) { print ''Perl Fast & easy \n"; }

This loop has no initialized variable, no test, and no update of any test variable, so it will loop forever. Often, this means that you don't always know under what conditions the loop should terminate, and so this technique is sometimes used to allow you a different method of deciding when you should break out of the loop. An unusual use of this type of loop, but it serves to illustrate the flexibility of the Perl for loop.

We have discussed the data types used in Perl and given a few examples of how they can be used. You have also learned the syntax of some program flow processing elements of the Perl language. There is more to learn in these respects, and you will be extending your knowledge of the language as you need to. The rest of this book will provide much of that knowledge; your own experience and looking at the work of others (who were once where you are now) will fill in the gaps and extend your experience.

Page 118

*This page intentionally left blank.*

Page 119

## **8
Perl Functions**

Perl is a very function-rich language. In this chapter you will explore many of the functions that Perl provides, especially those that help you with your Web applications. Some functions are found in many languages, others are unique to Perl; after you've learned to use them, you'll wish that all languages provided the same facilities.

In this chapter you will learn how to use:

![Image](content/d938f552af65a53b177029c39d905885.gif) String functions

![Image](content/d938f552af65a53b177029c39d905885.gif) Array functions

![Image](content/d938f552af65a53b177029c39d905885.gif) Hash functions

![Image](content/d938f552af65a53b177029c39d905885.gif) Subroutines

Page 120

### **What is a Function?**

A *function* is normally considered to be a section of code that performs a limited set of related actions. It might act upon a value (or a number of values passed to it, called *arguments* or *parameters*), and it often returns a *result*. A function that does not return a result is often called a *subroutine*.

To begin with, take a look at some of the functions you can use in Perl, a few of which you have seen before in earlier chapters.

### **String Functions**

There are many string functions provided by Perl. In this chapter you will learn about the following:

• chop() • chomp() • length() • substr() • lc() • uc() • lcfirst() • ucfirst()

#### **Chopping a String: chop()**

The chop function removes a character from the end of a scalar variable (in other words, it will work with numeric values as well as strings).

The basic syntax for the chop function is

$scalar_variable = chop($other_scalar_variable);

Page 121

For example:

**1.** Open a new program in your editor.

![Image](content/4e9678c4119899017a6f31e0e2af5676.gif)

**6.** Save the program as 08-01.pl.

**7.** Open a command window.

Page 122

![Image](content/6aa6363a24283d543338c3a62593d0a3.gif)

**8.** Check out the result.

**9.** After executing the previous code, $word2 will contain the string ''y". (The character "chopped" and $word contains the original string minus the "y".)

So, the chop() function is doubly useful, simultaneously giving you the chopped word and the character it chopped.

As you have already learned, this will also work with numbers; try this example to prove it.

**1.** Open your editor.

![Image](content/5bd64d59631b1ee45169eae649b7cf21.gif)

Page 123

**6.** Save the program as 08-02.pl.

**7.** Open a command window.

![Image](content/5cd4aef4e8e7e551e46fd27697568d1e.gif)

chop() has behaved in exactly the same way as it did for the string variable. This is not altogether surprising; as you will remember, a scalar can be string or numeric, in fact any single value of any data type. Chop() receives a scalar variable as its argument (or parameter) and so regardless of what it contains, chop() deals with it in the same way.

The chop function is very useful when it comes to things like removing the carriage return character at the end of a line in a file, for example. But you will find other uses for it as you go along.

#### **A Smart Chop: chomp()**

chomp is similar to chop, except that you have some control over what it chops…err, chomps. It too takes characters from the end of a line (string), but this time only the characters you tell it to. It does this through the use of a special variable known as the input record separator. The *input record separator* is represented like this:

$/

$/ will contain the character you want removed from the end of a string, which means if the string you give it doesn't have the character(s) you wanted removed, the original string is returned. Check out the example on the next page.

Page 124

$/ = ''\n"; $stringvalue = "This is a string \n"; print ($stringvalue);

This will return

This is a string

If you do the following:

$/ = "\n"; $stringvalue = "This is a string"; # note no \n in this string print ($stringvalue);

Then this will still return

This is a string

To illustrate this, try the following program.

**1.** Open your editor.

![Image](content/5318ce14783a76c9028382b1a3b088e6.gif)

| **NOTE** |
| Note though, that \n is the default value for $/, so you do not really need to do this unless $/ previously contained something else. |

Page 125

![Image](content/02fafb94dd2ecb417611e42851fc53e6.gif)

**8.** Display the result.

print ''The string that had NO newline character becomes: $stringvalue"; print " and this is a following string\n\n";

**9.** Save the program as 08-03.pl.

**10.** Open a command window.

Page 126

![Image](content/697f25498b9ca2db40c4cd88436d59e9.gif)

As you can see, chomp() is a bit more flexible than chop(), and it saves you having to check if the unwanted character is at the end of the string before chopping it.

Let's look at a few more Perl functions.

#### **Measuring String Length: length()**

This is a simple function that enables you to measure the length of a string.

Try this easy example.

**1.** Open your editor.

![Image](content/a2a10f1bce6bea30c7866386565d3182.gif)

Page 127

![Image](content/4eda03867b76c65ff04a94487d52a483.gif)

**5.** Save the program as 08-04.pl.

**6.** Open a command window.

![Image](content/190727d4adc656a59ae078f4ee2703f5.gif)

The length() function is a very simple but a very useful Perl string function, with many uses in many different applications. You'll be surprised how often you use it.

#### **Getting Substrings: substr()**

The substr function enables you to extract a part of a string. Perl needs this function as, unlike C, a Perl string scalar is not an array of chars, and therefore you cannot address characters individually using things like the example on the next page.

Page 128

$stringvalue = ''Perl is a great language"; $char = $stringvalue[5]; # This will NOT work!!

The substr function allows you to extract one or more characters from a string scalar like this:

**1.** Open your editor.

![Image](content/a0c0237ddeaddb01ef1f9c7ca2599717.gif)

**5.** Save the program as 08-05.pl.

**6.** Open a command window.

Page 129

![Image](content/988ebbbd04dbf90bdb39e1e9a48eb175.gif)

The substr function therefore accepts three parameters; the string being worked upon, the starting character position for the substring you want to extract, and the length (number of characters) to extract.

| **NOTE** |
| The starting position for a string is ZERO, that is, in the above example, 
$anotherstring = substr($stringvalue, 1, 3);

would return

erl |

Substr is a very useful function and you will no doubt be using it a lot. There will be many times that you will want to extract a domain from an e-mail address or a page name from a URL.

#### **Changing Case: lc (), uc (), lcfirst (), ucfirst ()**

You first learned about these functions in Chapter 4, but you'll examine them in more detail here.

The lc() function simply changes any uppercase characters in a string to lowercase. In this example, string2 will contain ''smith".

Page 130

$string1 = ''SMITH"; $string2 = lc($string1);

As you would expect, uc() has the opposite effect. In this example, string2 will contain "SMITH".

$string1 = "smith"; $string2 = uc($string1);

lcfirst() does what you might expect it to do. I assume that this function has been added for completeness, as there are few occasions when you'd really need to use it. In this example, string2 will contain "sMITH".

$string1 = "SMITH"; $string2 = lcfirst($string1);

Finally, a slightly more useful function is ucfirst(). This takes a string and capitalizes the first letter, as you might want to do for a name. In this example, string2 will contain "Smith".

$string1 = "smith"; $string2 = ucfirst($string1);

The short example here will illustrate all of these functions.

**1.** Open your editor.

Page 131

![Image](content/4f9c8dd7a5c37f1d81a475d985c2709f.gif)

**8.** Save it as 08-06.pl.

Page 132

**9.** Open a command window.

![Image](content/9993a11b284aa9831bc3829e88e0396e.gif)

### **Array Functions**

In this section you will learn about some of the functions provided by Perl for manipulating arrays.

#### **Printing Arrays: print**

Earlier, you learned a little about a concept called ''context." This concept also affects functions, and what functions do can depend upon what is sent to them.

The print function will easily print an array. Try this simple array example.

**1.** Open your editor.

![Image](content/b3bae9f122ce5b27f1a94edf0b11b562.gif)

Page 133

**4.** Save the program as 08-07.pl.

**5.** Open a command window.

![Image](content/1ea17b00fbf197bada9277ba5f994359.gif)

You might not often want to print an array like that, but Perl can do it easily if ever you do.

#### **Finding the Size of an Array: scalar**

In Chapter 5, you saw how to print the size of an array. The function scalar() returns the size of an array so that it can be stored in a variable to be used for some other purpose or again to allow the size of the array to be printed. Beginning with that method, here are a few examples describing the measurement of the size of an array.

Page 134

![Image](content/8df089d3715fb4837c51798a3a77fa04.gif)

**2.** Save your program as 08-08.pl.

![Image](content/c4c0b1a9c3d357957761abd97b243bca.gif)

That gives you the number of elements in your array. Here is another way of determining the size of an array.

To print the size of an array, as you learned about in Chapter 5, you can do this:

print $#passengerships;

This prints 2 as the array size, because the value returned is a count of elements starting at 0.

Page 135

Finally, you can use

$arraysize = @passengerships; print $arraysize;

which will return a value of 3.

To show these techniques in action, once again modify the previous program.

![Image](content/5eb2bebeec25921bb056af625ec7471b.gif)

**6.** Save it as 08-09.pl.

Page 136

![Image](content/56e48506b0def5efb311b8d0ba85bafa.gif)

As you will see, measuring the size of an array will prove to be very useful, and Perl enables you to easily obtain the information you need.

#### **Adding to the End of an Array: push()**

You can add elements to the end of an array by using the push() function.

Sticking with the array in the previous example, you can add another element to the end of the array like this:

push(@passengerships, ''QE2");

Try this example.

**1.** Open your editor.

![Image](content/3c5f7b82cf85bf481918fae392158615.gif)

Page 137

![Image](content/0d7c9e398cd3eff2e32f1a7df4c758ea.gif)

**5.** Save the program as 08-10.pl.

**6.** Open a command window.

![Image](content/45eeddf29c676ba3a869c5fd4ac8bcf8.gif)

Perl arrays are not sized at definition time or fixed in size at any point, so you can keep adding elements. And of course, in the previous example, you could have added more elements at the same time by just adding more values separated by commas.

#### **Removing an Element from an Array: pop()**

You can remove the elements from the end of an array using the pop() function.

Page 138

![Image](content/0fe33f4ace4820d832cb9a72b3a03f70.gif)

**4.** Save the modified program as 08-11.pl.

After the ''pop" function call, $poppedstring will contain "QE2".

![Image](content/ec71f90cb5c27cd3913191bdc6f8d5cd.gif)

Now you have a few useful array functions to get you started with working on arrays.

Page 139

### **Hash Functions**

Perl provides a number of hash functions. Take a brief look at a much-used one. The each function enables you to run through the key value pairs of a hash so that you can do what ever you want with the values. A simple example would be to print all the values of a hash.

![Image](content/fdcdfd62e6067b9db6d989f49f743d94.gif)

**3.** Save the program as 08-12.pl.

![Image](content/d0cf79e262bcaa1363cd4be2bd312f6f.gif)

Page 140

| **NOTE** |
| Note that the each function should not be confused with the foreach loop. foreach is a loop construct with many purposes and not a specific function for processing hashes. |

I have kept the examples of Perl functions very simple in order to help you to understand the material in this chapter. You have just started to scratch the surface of some of the built-in functions available in Perl, though. There are many more, as you will see.

For now though, take a look at another type of function—the *subroutine*.

### **Subroutines**

Subroutines are very similar to functions, except they are *user-defined functions*. You can go and write your own subroutines and when they are written, your program can call them like it does a built-in Perl function. These days, the term subroutine is used interchangeably with *function*. However, so that it is clear that you are looking at sub-routines that you have written yourself, the distinction will be maintained in this text.

Subroutines are created using the following syntax:

Sub subroutine_name { statement1 …; statement2 …; statement3 …; statement4 …; . . . . . . }

The subroutine is called in a similar way to a function.

Subroutine_name( );

Page 141

To get a subroutine to return a value as a Perl built-in function does, you use the return statement. Usually this will be a matter of returning a value of a variable.

Sub subroutine_name { statement1 …; statement2 …; return($variable); }

If you are expecting a value to be returned, you can capture that value like this:

$result = subroutine_name( );

You can also pass parameters as you do with many built-in functions.

$result = subroutine_name($);

If this looks odd, try this simple example to help you fully understand what is going on.

![Image](content/20b69a29dc26149bc3400a3709a931c8.gif)

Page 142

![Image](content/cbbbf4eda7973abaa42ee37d2e02a14d.jpg)

**10.** Finally, you must close the braces to end your subroutine.

}

Page 143

**11.** Save the program as 08-13.pl.

![Image](content/05c13aa21fae3fab351beaa3fe40602e.gif)

You have seen just one way of writing a subroutine. You will see different approaches and techniques used; read through these examples carefully and see if you can work out what is going on. In Perl, there are many ways to achieve the same result.

When writing your own subroutines, there are many aspects to consider, such as scope and global versus local variables (or Perl's answer to them—the my keyword, for example). It is best to introduce yourself to those subjects slowly, when they can be best shown with practical usage.

You have just begun to scratch the surface of Perl. That is not to say you have not learned much, because you have! But Perl is a huge language, and there are many experienced programmers and Web developers out there who still do not know all there is to know about Perl. Right now, you need to begin covering some groundwork for Web applications. So far, you have looked at Perl from the point of view of using it as a ''console" or "command line" programming language. However, in order to use Perl for the Web, you have to use it in a slightly different way. Before you can do that, you have to know all about the main language of the Web: HTML.

Page 144

*This page intentionally left blank.*

Page 145

## **9
A Diversion: HTML**

In order to use Perl for the Web, you have to know the main language of the Web, HTML. This chapter is bit of a diversion into HTML for those who don't have any experience with it (or for those who use WYSIWYG editors). Even if you do prefer to use point and click editors, an understanding of HTML is useful if you want to know what is really going on in an application.

If you're already familiar with HTML, you can skip this chapter. If you have never seen any HTML, then read on. If you are unsure, treat it as a refresher course—we all need those from time to time!

In this chapter you will learn how to:

![Image](content/d938f552af65a53b177029c39d905885.gif) Write an HTML document

![Image](content/d938f552af65a53b177029c39d905885.gif) Add headers and color

![Image](content/d938f552af65a53b177029c39d905885.gif) Add images and hyperlinks

![Image](content/d938f552af65a53b177029c39d905885.gif) Add frames

Page 146

### **Saving HTML Files and Testing HTML Pages**

HTML is merely text, and so can be written using any text editor (like Notepad, WordPad, Word, HTMLPad 2000 and so on). There are many HTML editors on the market but they differ from ordinary text editors only in so far as they have specialized tools that enable you to write HTML more quickly and with (hopefully) fewer errors.

When you save an HTML file, you will normally save it so that it has an .htm extension.

Home.htm

| **NOTE** |
| You can also use the .html extension, which is usually the standard on UNIX-based systems. The three-character .htm extension probably came about because of the 8.3 filename limitation in DOS and Windows 3.1 |

Be careful when using editors such as Notepad or Word because they might (unless you explicitly ask them to do otherwise) add a .txt or a .doc extension to your HTML filename.

You can test your HTML pages simply by opening a file directly in the Web browser. In Windows, you would do this simply by double-clicking the file, which causes the browser to open, displaying the contents of the HTML file. Of course, a better way to test the files is to save them into a folder under wwwroot or htdocs (depending upon your platform, Web server, and so on). You can then use the http://127.0.0.1/*foldername* type of address in your browser location window.

| **NOTE** |
| When you actually write Perl Web (CGI) programs, you *must* save them in a scripts folder (or another folder with execute permissions) under your Web server or they will not work. |

Page 147

From this point on, it's up to you to decide which method to use for testing your HTML files.

### **The Structure of an HTML Document**

HTML tags tell the Web browser all about your page and how to format it. In most cases, HTML tags have a *start tag* and an *end tag* so that the browser knows when to start the formatting and when to end it. Often, you can get away without the end tag, but it is poor practice and might cause problems with some browsers.

There are many optional elements in an HTML document, but basically, an HTML document consists of the <HEAD> tag and the <BODY> tag. In turn, the <HEAD> tag and the <BODY> tag may consist of a number of other tags.

The <HEAD> tag can contain:

• The <TITLE> tag. This is the title that appears on the title bar right at the top of the browser window.

• The <SCRIPT> tag. Optionally, scripts can be added inside the HTML header, for example, for Form field validation—more on that later.

• Other tags such as <META …> tags, which contain information about the Web page and are used by search engines to find and catalogue your page.

The <BODY> tag contains the actual content of the page—often referred to as the *document*—which consists of a wide range of possible HTML tags.

### **Writing an HTML Document**

In this chapter, you'll learn the basics of HTML to get you up and running with Web applications as quickly as possible, but you should know that there are formal, recognized standards for HTML as there are most other things in computing. As you become more proficient in writing Web applications, you will want to know more about these standards. There are many sites on the Web, as well as some excellent books, that will help you to extend your knowledge.

Page 148

HTML is simple, but like most things in life, it does have rules. Follow the text and try the examples; by the time you get to the end of this chapter, you should be able to write a Web page from scratch, using little more than a simple text editor and your Web browser.

Start by telling the browser that this is an HTML document. To do this, you use the <HTML> tag. You end the HTML document with the </HTML> tag. All end tags are the same as the start tags, except they have the forward slash at the start of the tag name.

So, the header tag is <HEAD> and ends with </HEAD>. And the body tag is <BODY> and ends with </BODY>. Get the idea?

Open your editor and start coding some HTML.

![Image](content/4e41b178a466443b8e2715e6c78b1dda.gif)

The title for an HTML page (the one that appears on the blue title bar at the top of your Web browser, not in the Web page itself!) is coded as

<HEAD> <TITLE>This is a Web Page</TITLE>

| **NOTE** |
| The <HEAD> tag opens the HTML page header. The <HEAD> is used to contain the title and other things such as script code, for example, JavaScript, VBScript, and so on. You will see a little of this when you come to code forms. |

Page 149

![Image](content/adde3880609fb628c67024101ad0af72.gif)

| **NOTE** |
| Notice that the HTML tags are all in uppercase letters. This is purely by convention. You can use uppercase or lowercase, whichever you prefer. |

**4.** Save it as 09-01.htm on your hard drive.

Page 150

![Image](content/e5184138c38e2ba816672c7f5b30be1c.gif)

![Image](content/c4f1bf1d2f0828b20548691bfcca98c5.gif)

Page 151

![Image](content/65c9a9c83c7a7247afd6766e7c85a6ca.gif)

The browser joined the two lines of text together. In an HTML document, carriage returns are ignored. This is done so that the document flow can be flexible so that if you change the size of the browser window, the text moves around to occupy the available space. If you put ordinary carriage returns in the document this resizing would not work very well.

If you want to force a carriage return you must use the HTML tag <BR>. This stands for break (line break).

To demonstrate this

![Image](content/6cea91fd5e710a2fe9bf3bb63f219584.gif)

Page 152

![Image](content/82749c6fa47929b36f1112ed7019d441.gif)

<BR> is one of the many simple HTML text-formatting commands. There are many others and you will see more of them as you continue through this chapter.

#### **Spaces**

The Web browser only notices the first space character it encounters. If you place three spaces between words, one space will be displayed but any subsequent spaces will be ignored. To overcome this problem you must enter an HTML *non-breaking space*. This is not an HTML tag, but an escape code:

&nbsp;

It is called an *escape code* (or *escape sequence*) because it causes the system to escape from the current process, carry out the code, and then return to the system. The & character starts the escape and the semicolon signifies the end of the code.

You can group a number of &nbsp; codes together to move a piece of text further along a line, giving another form of simple text formatting. There are much better ways, but this method does have its uses.

Once again, modify your HTML code to add some &nbsp; escape codes.

**1.** Open the previous HTML page in your editor.

Page 153

![Image](content/57aeeaf74bb34b8a9153cb7e3d28c253.gif)

![Image](content/f4aaaca7a123deb29bef6995cd456bd3.gif)

Three &nbsp; codes have been added and each one gives a single space, so the second line of text is moved along by three spaces.

### **More Text Formatting**

Okay, so now you can create a new document, give it a title, display text, force line breaks, and put larger gaps comprised of spaces into your HTML document.

Page 154

Here are some more simple text formats you can use:

• **Bold** is achieved using the <B> tag and ends with the </B> tag.

• *Italics* are achieved using the <I> tag and ends with the </I> tag.

• Underline is achieved using the <U> tag and ends with the </U> tag.

You can combine any or all of these tags to combine the effect. So now you can make your test1.htm document look a bit more interesting.

**1.** Modify the previous HTML file.

![Image](content/73a6d40cc9c88f6e6174d783bd4071ac.gif)

| **NOTE** |
| You still have the <BR> tag at the end of the line to give a line break. On the second line of text, add italic and underline effects by using the <I> …</I> and <U> …</U> tags respectively: |
| <I><U>It is just a simple demonstration</U></I> |
| There are no &nbsp; codes this time. This is just for clarity so that you can focus on the subject at hand. If you want to include them to see the effect, please do. |

Page 155

![Image](content/b85ba6e03929ff5baab67ec848b58c46.gif)

It is normal to end tags in the reverse order to the way you started them. If you open the italic tag first, you close it last (as you have done above). But it is not mandatory to do this, and the browser will forgive you if you get the order wrong. However, it is good practice to get the order right, as it makes modifying or debugging the page much easier.

### **Adding Structure and Color**

Web Pages were originally about text and then, later, images. Now however, Web pages are much more complex, and a wide variety of tags and associated attributes can be used to give your pages structure and color. Next, you will learn more about some of the most useful tags that add richness to your Web pages.

#### **HTML Headings**

What you have so far is all very well, but you still need to be able to add things like titles and, if you are to use the main advantage of the Web, you also need to be able to use hyperlinks.

Titles, or in HTML-speak *headings* or *headers*, are easily implemented using the <Hx> tags (where x = a number between one and six). <H1> is a start tag for the largest header. As usual, an end tag </H1> is placed after the heading text. Once again, an example will show the effect.

In your editor, open a new file and write a new HTML page.

Page 156

![Image](content/7587e5dee95e45f4a4af8e7f517d2704.gif)

Page 157

![Image](content/3a6d5b633f5374a00f840d93714f3a18.gif)

**8.** Save it as 09-02.htm, or any other name you are happy with.

![Image](content/8bcc6f97cc848c7d5073117200e39630.gif)

| **NOTE** |
| <H1> tags can also be combined with most other text formatting tags to produce desired effects, such as the <B>, <I>, and <U> tags (just don't forget the end tags—</B>, </I> and <U>). |

There are other tags that might also be combined, and more of these will be covered later.

Page 158

#### **Text Positioning**

Now you can create headings for passages of text in your Web pages, but note that in the previous example, the titles are all left-justified, that is, they are lined up with the left hand edge of the page. Sometimes, you might want to have a title or heading that is centered on the page.

There are two ways of doing this—by using the <CENTER></CENTER> tags or the <DIV ALIGN=CENTER></DIV> tags. (The <DIV> tag can be used for a number of purposes but here is used for centering text). The <CENTER> tag is a deprecated tag, and it is therefore preferable to use the <DIV> tag.

| **NOTE** |
| A *deprecated tag* is a tag that is now considered obsolete but is still supported by current versions of HTML and browsers but may be dropped from future versions. |

Notice that here, the DIV tag uses the ALIGN= parameter to perform positioning. This can also be used to position text (or images) to the left or to the right. As you would expect, the tags then read as <DIV ALIGN=LEFT></DIV> or <DIV ALIGN=RIGHT>.

**1.** Re-open the previous HTML page.

![Image](content/3eeaabd07e3d7a300ac8c753f2457019.gif)

Page 159

| **NOTE** |
| The <DIV></DIV> tag can enclose one title or line of text or as many as you want so that you do not have enclose each line you want to be centered with separate <DIV></DIV tags. |

**4.** Now save the page as 09-03.htm.

**5.** Open 09-03.htm in your browser.

![Image](content/64d1097d9496d6ae54de171a35053e98.gif)

Now you are getting quite good at formatting and positioning text, but it still looks a bit bland! Next, you will take a quick look at adding some color to your pages.

#### **Color**

Now you can create HTML documents, you can create titles of different sizes and position them across the width of the page, and you can create text for the pages and render it bold, italicized, underlined, and so on. Unfortunately, it looks a bit boring because the text is all black on a white background. This would be even worse on some browsers, especially older ones, as the background will be gray.

Page 160

But you can liven up your pages with a bit of color. The subject of color can be as simple or as complicated as you want to make it. You will see what I mean in a moment.

The Web, and in particular Web browsers, uses the RGB color system, as does your PC (usually). With this system, using a mixture of red, green, and blue colors in varying strengths makes all of the required colors available. The strength (or saturation) of each color is variable in 255 discrete steps. So, maximum saturation of red = 255, green = 255, and blue = 255, gives white, and black is given by red = 0, green = 0 and blue = 0—it's rather like mixing paint at school.

A further complication is that computers often use a number representation known as *hexadecimal*. Humans count in multiples of ten, probably because we have ten fingers. Computers use *binary* as they only understand 1 or 0, on or off, and so on. Hexadecimal is a hybrid that is readable by both humans (just about) and computers. It is similar to our decimal system except when you start counting, you don't go into double figures until you reach 16.

To represent the digits greater than 9 you use A through F, so you count like this in Hex (as hexadecimal is abbreviated): 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, F ….

Then it continues … 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 1A, 1B, 1C, 1D, 1E, 1F …20, and so on.

Got the idea? (Don't worry if you haven't; you don't need to understand it unless you are interested, as you will see in a moment).

As I have said, white is represented by 255 red, 255 green, and 255 blue. In HTML you convert these numbers to Hex and join them all together. In Hex, 255 is represented as FF, so when you convert all three numbers and join them together, white becomes FFFFFF (3 FFs joined together, in the order red, green, blue).

HTML precedes these numbers with a # sign. This merely signifies that the number is in Hexadecimal. So now white is represented as #FFFFFF. Black is #000000\. Bright yellow would be #FFFF00.

Page 161

Note I said that you do not need to worry about the representation of colors using hexadecimal values. There are two main reasons for this.

• The Web browser is capable of displaying colors from a palette of 216 colors.

• Many HTML editors or other Web authoring tools have some kind of color palette that enables you to point and click to set colors.

Finally, many of the colors have been given names so that you can set colors using English names such as YELLOW and BLUE, and so on that then replace the #FFFF00 and #0000FF, respectively.

Okay, now that you know how to represent colors, let's try using them.

#### **Backgrounds**

Setting the background color of a document is achieved through the use of the BGCOLOR attribute of the <BODY> tag. Using what you have learned, you can now set the background color of the page.

![Image](content/f997147e8059d689de96fbf9bf622c8f.gif)

| **NOTE** |
| The hex characters after (#) character describe the color being used as three pairs of hex numbers, or you can use the color name without a hash sign. |

Page 162

| **NOTE** |
| Notice that BGCOLOR is an attribute of a tag, and not a tag in its own right. Attributes modify the behavior of the tag they belong to and you will come across many more as you continue learning HTML. |

![Image](content/96427cadda5f1d8a60873e8e14ac2380.gif)

**4.** Experiment with changing the #xxxxxx numbers and see the difference. If you increase the first two digits, your background will be more red. If you increase the middle two digits there will be more green and of course, if you increase the last two digits there will be more blue. If you increase them all or decrease them all the color will get brighter or darker, respectively.

#### **Background Images**

You can also make the background even more interesting by using the BACKGROUND attribute of the <BODY> tag.

Try modifying the previous example to demonstrate the difference. Use a simple background texture graphic. In the example shown here, the graphic has been called bground.jpg.

Page 163

The graphic does not have to be the size of the page—a small graphic will tile over the whole page. This enables you to fill the screen with a background graphic using a very small file, which means that it takes very little time to download to the browser. Graphics packages (such as Paint Shop Pro) are available that will enable you to produce seamless graphics so that when they tile on your page background they do not produce a horrible grid of joins.

Where before you put the BGCOLOR=#, put

BACKGROUND=''bground.jpg"

![Image](content/3b0f838898d7f7064531bd00851f3be6.gif)

Page 164

**3.** Save your HTML file as 09-05.htm and then test it in your browser.

Save whatever image you have decided to use into the same folder as your HTML as bground.jpg so that the BACKGROUND=''bground.jpg" attribute of the BODY tag can find the graphic.

![Image](content/506a71948834f8d1e9decbd6b41a65f9.gif)

You can also use this principle to produce some interesting effects that you have probably seen during your Web surfing.

![Image](content/9d51410ff0ae22df57cf9b81a64d8e27.gif)

![Image](content/6deab77fd1c848c3ccaba62fb6ab3964.gif)

There are many other effects that might be achieved using similar techniques—experiment with some ideas of your own.

Page 165

#### **Fonts in HTML**

So now you can set background colors and position headings of various sizes where you want them on the page. But what about ''normal" text?

You can do a lot with that too, using the <FONT></FONT> tag. With <FONT> you can set the size, typeface, and color, and of course you can again combine the <FONT> tag with any of the other text formatting tags.

A typical font tag looks like this:

<FONT FACE=facename SIZE=n COLOR=#xxxxxx>here is some text</FONT>

Try modifying the previous HTML page to include some <FONT> settings; you can then combine them with some of the other tags you learned about earlier.

Here are some examples for you to add to your HTML page.

<FONT FACE="arial" SIZE="2" COLOR=#804040>This is funny reddish arial text</FONT><BR> <FONT FACE="Tahoma" SIZE="5" COLOR=#FF0000>This is red tahoma text</FONT><BR> <FONT FACE="arial" SIZE="3" COLOR="#0000FF"><B>This is medium sized blue arial bold text</B></FONT><BR> <FONT FACE="Times New Roman" SIZE="1" COLOR="GREEN"><I>This is tiny green Times New Roman italic text</I></FONT><BR> <FONT FACE="arial" SIZE="7" COLOR=#000000><B><I>This is large black arial bold italic text</I></B></FONT><BR> <FONT FACE="Courier" SIZE="6" COLOR="White"><U>This is fairly large white Courier underlined text</U></FONT><BR>

Page 166

![Image](content/850786122964c15605722b4b4b70c4e3.gif)

**2.** Save it as 09-10.htm.

![Image](content/513df7cae7e403a736887964e8d2c0a5.gif)

| **NOTE** |
| A single <FONT></FONT> tag can be wrapped around many paragraphs of text. Also note that you lose sight of the white text, as it is on a largely white background. |

Page 167

#### **The Horizontal Rule Tag**

One other tag of interest at this point is the <HR> tag. HR stands for *horizontal rule*, and it gives a dividing line across the screen. It is not employed as often as it used to be because authors now favor more graphical methods, but it is useful as a simple page divider. Note that an end tag is not required.

Modify an earlier page to show what HR looks like (it doesn't matter which example you use, or whether you make up your own).

The horizontal rule tag can be a very simple tag, as shown here:

<HR>

Or you can add other attributes to it such as its width as a percentage, like this:

<HR WIDTH=75%>

And you can even add a color attribute like this:

<HR WIDTH=500 SIZE=5 COLOR=''#804040">

**1.** Add the following to the second sample Web page (09-02.htm):

<HR WIDTH=75%> It is just a simple demonstration<BR> <HR> Here is some more text<BR> <HR WIDTH=500 SIZE=5 COLOR="#804040">

![Image](content/7be0cc6d67c3a29d1a1759a632982c55.gif)

**3.** Save this example as 09-07.htm.

Page 168

| **NOTE** |
| Notice that there are three examples in the previous listing. The first one states that the horizontal rule should be 75% of the width of the page. This means that the rule will adjust its width to always be 75% of the current width of the page, so that if you change the browser window size the width of the rule will change with it. |

![Image](content/030c079e2d38edf6902278540e771007.gif)

| **TIP** |
| Drag the corner with your mouse and watch what happens to the width of the lines. Note that the 75% rules adjust themselves to maintain their width relative to that of the window. |

Page 169

#### **The Paragraph Tag**

The paragraph tag <P> is used to split up sections of text into paragraphs. It is preferable to the <BR> tag, which is used simply for breaking lines. The <P> tag has an end tag </P> and this should be used. Right now you might be able to get away with not using it, but it is meant to be there, and there is no guarantee that future browsers will not insist on it being present. Anyway, it helps keep your HTML tidy, so use it!

Here is a simple example of the paragraph tag.

![Image](content/f266db97a08f98b677279362a78cbaad.gif)

Page 170

![Image](content/e02cbec0d541d1c679eacf445a9df641.gif)

**11.** save your HTML as 09-08.htm.

![Image](content/2b169682e1a8489aa807fea89b35fb10.gif)

Page 171

### **Images**

In addition to text, a Web page can also hold pictures, sound, video, and almost anything you want. Right now, you can find out more about images and using them in your Web pages. Web browsers normally support two image formats, the JPEG and the GIF image.

#### **JPEG Files**

JPEG files are very good where there are lots of colors, such as in photographs, as they can achieve a high degree of compression so that the file size is reduced and the time taken to download them is shorter.

#### **GIF Files**

The GIF format was developed by the ISP CompuServe and has become a popular image standard. It achieves a degree of compression by limiting the maximum number of colors to 256\. GIF images are better where there are fewer colors in an image. It is possible to remove all unused colors to reduce the file size and download time.

There is a new image format (PNG) that seemed likely to rise to prominence in the near future, but so far has failed to catch on. You don't need to worry about that here. In any event, the same principle will apply in so far as Web pages are concerned.

Let's add an image to a Web page. Create a new Web page for this example; keep it nice and simple.

Page 172

![Image](content/8c84e9ef9c5cac69e0cd03658f163ee9.gif)

**1.** Create a new HTML page.

![Image](content/075dfa4375989af698940f36c4c7d1b3.gif)

Page 173

**6.** Now display an image.

<IMG SRC=''biggles.jpg" WIDTH=400 HEIGHT=486>

![Image](content/f13d78415740f27abc526b33ca0ddc0b.gif)

**10.** Save your HTML as 09-09.htm.

**11.** Use a photograph of your own and change the name accordingly in the SRC= attribute. (And don't forget to put the image in the same folder as your HTML.)

**12.** Now load 09-09.htm into your browser.

Page 174

![Image](content/f9dbd3e25705e3ebbe5174a3215c08ef.gif)

There are a couple of things to note here. The SRC= attribute gives the name of the file and the path to the file if it is not in the same folder as the HTML file. The image file could even be at another location, in which case you could give the full URL. If the image file is in a folder called Images below the current folder (that is, below the folder the HTML file is in), you would specify the SRC attribute as:

Images/biggles.jpg

If your Images folder is stored above the current folder you would denote this as

../images/biggles.jpg

If the Images folder were right at the top of the site, you would indicate this by

/images/biggles.jpg

All this might seem a little confusing, but you will come across it again when you learn about hyperlinks, and you will find it gets clearer as you go along.

### **Hyperlinks**

You will shortly be learning about frames. Before you do, you need to understand hyperlinks, because frames are pretty useless without them. Indeed, the whole Internet would cease to exist without hyperlinks (sometimes called *hypertext links*)

Page 175

Linking pages is very simple; you use *anchor* tags to accomplish it. The anchor tag looks like this:

<A HREF=''http://www.microsoft.com">Go to the Microsoft Home Page</A>

This anchor tag shows the text "Go to the Microsoft Home Page." When displayed on the Web page it is (usually) colored blue and underlined to show that it is a hyperlink. You can set the color of the link text in the <BODY> tag. (HREF stands for hypertext reference).

You can use images instead of the link text shown in the previous example.

<A HREF="http://www.microsoft.com"><IMG SRC=image1.jpg WIDTH="30" HEIGHT="10" BORDER ="0"></A>

| **NOTE** |
| The BORDER= "0" attribute is used to prevent a box being displayed around the image. |

### **Linking within a Page**

You can link to a location within a page by using the anchor NAME attribute.

<A HREF=#placename</A>

Lower in the page you must put an anchor name tag.

<A NAME=placename>

You can also jump to a location within another page by combining the URL type HREF and the "place name," or anchor name.

<A HREF="http://www.mydomain.com/index.htm#location2">Go to the Microsoft Home Page</A>

This will cause index.htm to be loaded and to be immediately scrolled down the place in the page containing the <A NAME=location1> tag.

Page 176

Try this simple hypertext link demonstration.

**1.** Create an HTML page using the usual <HEAD> tags and so on and with an appropriate title.

<HTML> <HEAD> <TITLE>Hyperlink Test Page</TITLE> </HEAD>

![Image](content/c0fad88cc4cd4783c830575ff56ebcae.gif)

Page 177

![Image](content/3255899c880ed011edc8ea3484004455.gif)

**7.** Save the listing as 09-10.htm.

**8.** Now type the following listing into your editor (It's *The Desiderata*, by Max Ehrmann):

<HTML> <HEAD> <TITLE>The Desiderata</TITLE> </HEAD> <BODY ALINK=FUCHSIA BGCOLOR=#C8FFFF LINK=BLUE VLINK=BLUE> <H1 ALIGN=CENTER> <FONT FACE=''arial" COLOR=#cc3333>The Desiderata<BR></font> </H1> <BR> <DIV ALIGN=CENTER> <FONT FACE="arial" SIZE=3> Go placidly amid the noise and haste, and remember what peace there may be in silence. <BR><BR> As far as possible, without surrender, be on good terms with all persons. <BR><BR> Speak your truth quietly and clearly; and listen to others,<BR><BR> even to the dull and ignorant; they too have their story.<BR><BR> Avoid loud and aggressive persons; they are vexations to the spirit.<BR><BR> If you compare yourself with others, you may become vain or bitter,<BR><BR> for always there will be greater and lesser persons than yourself.<BR><BR> Enjoy your achievements as well as your plans. <BR><BR> Keep interested in your own career, however humble, <BR><BR> it's a real possession in the changing fortunes of time.<BR><BR> Exercise caution in your business affairs, for the world is full of trickery. <BR><BR>

Page 178

But let this not blind you to what virtue there is; <BR><BR> many persons strive for high ideals, and everywhere life is full of heroism. <BR><BR> Be yourself. <BR><BR> Especially do not feign affection. Neither be cynical about love; <BR><BR> for in the face of all aridity and disenchantment,<BR><BR> it is as perennial as the grass.<BR><BR> Take kindly the counsel of the years, <BR><BR> gracefully surrendering the things of youth.<BR><BR> Nurture strength of spirit to shield you in sudden misfortune. <BR><BR> But do not distress yourself with dark imaginings. <BR><BR> Many fears are born of fatigue and loneliness. <BR><BR> Beyond a wholesome discipline, be gentle with yourself. <BR><BR> <A NAME=child>You are a child</a> of the universe no less than the trees and the stars; <BR><BR> you have a right to be here. <BR><BR> And whether or not it is clear to you, <BR><BR> no doubt the universe is unfolding as it should. <BR><BR> Therefore be at peace with God, whatever you conceive him to be. <BR><BR> And whatever your labours and aspirations, in the noisy confusion of life,<BR><BR> keep peace in your soul. <BR><BR> With all its sham, drudgery and broken dreams, it is still a beautiful world. <BR><BR> Be cheerful. Strive to be happy. <BR><BR> </FONT> </DIV> </BODY> </HTML>

**9.** Note the <A NAME=child> tag. This is where the second link in the previous HTML page will link to.

Page 179

![Image](content/8af32c96b3e4d87812369a30d094625a.gif)

**11.** Save the listing as desiderata.htm.

**12.** Now open 09-10.htm in your browser and test the links to see the effects.

![Image](content/3fb3c0c4511cc25483093b7a150b2880.gif)

**14.** Try adding a link at the bottom of desiderata.htm to take you back to 09-10.htm.

**15.** Then try adding a link at the bottom of desiderata.htm back to the top of the page. (You will need a new <A NAME= tag.)

Finally, you can also direct the link to open a new browser window for the new page by using the TARGET attribute.

The TARGET attribute has a number of predefined values that can be used. For the time being, just use the ''_new" attribute.

Page 180

![Image](content/d6a72ecef6832d71bf25c1073737a151.gif)

in both the <A HREF= … tags so that the listing looks like this.

![Image](content/507b76885f684651c109dd8d3daab883.gif)

| **NOTE** |
| You can use the attribute _blank instead of _new– it has the same effect. |

That's all on hyperlinks for the time being, but you will be using them again shortly during our discussion on frames.

Page 181

### **Frames**

Before you start, a warning: use frames sparingly—they can make your site slower to load and they don't always look the same in all browsers. However they do have their uses. The most common purpose is to aid navigation.

You have seen Web sites where you have a menu of options down the left side and perhaps a banner at the top of the screen. If you find that when you scroll down the main screen the left side menu doesn't move, this site has probably been created using frames.

![Image](content/9eebb89239d5fa4d7bae37137c395350.gif)

Of course, this is only one option. You can create frame layouts of any type you want to set up, but this is one of the most commonly used.

| **NOTE** |
| If you created a page that described the above layout and then tried to view it in a browser, you would see nothing. As I have already said, the frame page merely describes the frame layout that will contain the pages that fit into each frame. Those pages are set up separately as conventional HTML pages and are then loaded into the required frame. |

Page 182

In summary, a *frameset* is a collection of frames designed to contain HTML pages, which are then displayed as one page in the browser.

### **Frame Tags**

There can be several frames in a frameset but more than two or three becomes impractical. For each frame, you specify the size of the frame. The frames effectively divide up the page area that you see in the browser. This is achieved by specifying the width or height of each frame.

To get the frames to look like you want them to appear can be difficult at first, but it is logical. Honestly.

![Image](content/db031499d74df629643257ed81c78adc.gif)

Remember that you will need an HTML page to fit into each of the above frames. To fit in with the scheme, you can call them Banner.htm, Menu.htm, and Page1.htm.

The coding needed to produce the frames page to achieve the layout is as follows:

<HTML> <HEAD> <TITLE>Frames Demo</TITLE> </HEAD> <FRAMESET ROWS=''20%,80%" COLS="*" FRAMEBORDER="0"> <FRAME SRC="banner.htm" NAME="banner"> <FRAMESET COLS="20%,80%" ROWS="*"> <FRAME SRC="menu.htm" name="menu"> <FRAME SRC="page1.htm" name="main">

Page 183

</FRAMESET> </FRAMESET> <NOFRAMES><BODY BGCOLOR=''#FFFFFF"> Sorry, Your browser does not support frames. </BODY></NOFRAMES> </HTML>

![Image](content/ab47990438c72403cb31600e0703b9b5.gif)

Page 184

![Image](content/48fa062156cd31397c64479e358a3fd7.gif)

**11.** Notice that the COLS attribute in the first FRAMESET is set to *, which means ALL or in this case the whole width. Similarly, the second FRAMESET has ROWS set to *, the whole height.

Try changing the values of the numbers in the FRAMESET tags to observe the effect.

Try replacing the * values in the ROWS and COLS attributes with numbers and see what you get.

Now add additional numbers separated by commas to the FRAMESET attributes.

<FRAMESET ROWS=''100,500,100" COLS="100,200">

Also, note that although here the values are specified as a numbers of pixels, you can also use percentage values.

<FRAMESET ROWS="10%, 90%" COLS="* >

Now let's put something into the frames.

Page 185

For this demo, you will need to build five pages.

**1.** You should already have the framedemo page. If not, copy the following into your editor and save it as framedemo.htm.

<HTML> <HEAD> <TITLE>Frames Demo</TITLE> </HEAD> <FRAMESET ROWS=''20%,80%" COLS="*" FRAMEBORDER="0"> <FRAME SRC="banner.htm" NAME="banner"> <FRAMESET COLS="20%,80%" ROWS="*"> <FRAME SRC="menu.htm" name="menu"> <FRAME SRC="page1.htm" name="main"> </FRAMESET> </FRAMESET> <NOFRAMES><BODY BGCOLOR="#FFFFFF"> Sorry, Your browser does not support frames. </BODY></NOFRAMES></HTML>

![Image](content/86173057246a71203f02d793cb22e05a.gif)

Page 186

![Image](content/b04791ae2352611727c1dbd7e629cb13.gif)

| **NOTE** |
| Notice the TARGET attributes— this means open the page in the frame called ''main," the main window. Of course, this name can be anything you want it to be. |

And now, three pages to go into the main window.

Page 187

![Image](content/83b940e78ac29f38aea91b3c696b0a02.gif)

![Image](content/d7749d8fbae99de954c81cb142eb652a.gif)

Page 188

![Image](content/45d746e27ea22731beed0ec5176cba6d.gif)

![Image](content/e79ab7d24a6d771a4a21db216b7c4288.gif)

Sometimes you might not want to see the lines that separate the windows or frames—you can remove these using the FRAMEBORDER=''0" attribute. Try modifying the first FRAMESET tag in framedemo.htm so that it looks like this:

<FRAMESET ROWS="20%,80%" COLS="*" FRAMEBORDER="0">

**8.** Save it and try again.

**9.** Re-open the page; the lines should have disappeared.

Page 189

That's enough on frames to get you started.

A couple of major components of HTML, forms and tables, have been omitted. You will learn about these as you learn about writing Web applications.

Page 190

*This page intentionally left blank.*

Page 191

## **10
CGI Programming**

Remember right back at the beginning, in Chapter 1, when you installed your Web server and tested it? Now it is time to start using it.

In this chapter you will:

![Image](content/d938f552af65a53b177029c39d905885.gif) Learn what CGI is and what you can do with it

![Image](content/d938f552af65a53b177029c39d905885.gif) Try your first Perl CGI Program

![Image](content/d938f552af65a53b177029c39d905885.gif) Use HTML forms

Page 192

### **What Is CGI?**

Let's have a quick overview of what the Web server does. Normally, the Web server receives a *request*, as it is known, from the user's Web browser. That is, the user requests a page from a Web site. The Web server receives the request, finds the page, and returns it to the browser. The browser renders the page using the HTML tags we talked about earlier to format the page on the user's screen.

![Image](content/5040fcbe599d6c3e70b72846fd650452.gif)

This is fine for HTML pages, but what happens when you want your Web page to use a Perl program to update a database? A Web server cannot handle that by itself. When such a request arrives at the Web server it is passed to other external software. This is achieved through the *Common Gateway Interface*; and this is what CGI programming is all about.

#### **CGI Processing**

![Image](content/8334920a9104bcb2a68cdbf71ce6ee99.gif)

The CGI box shown can consist of many things. For instance, if you intend to use ASP for your Web applications, any requests for an ASP page will be diverted to the program asp.dll. But of most interest right now is Perl; requests for Perl scripts or programs are passed to perl.exe. In Chapter 1 you installed Perl on your machine, so now you should be all ready to go.

Page 193

#### **What Can I Do with CGI?**

CGI programming allows you to do almost any Web-based task you could ever want to do with a Perl CGI program.

There are some rules for using Perl to talk to its Web surroundings that you'll need to learn. There are also some features of CGI itself to learn that you will find useful.

### **A Simple Perl CGI Program**

At last you are going to try a real CGI program. You are going to write a very simple Perl program to display the IP address of your machine on a Web page.

| **NOTE** |
| An IP *address* is the network address of your PC. Every computer connected to the Internet has an IP address. An IP address looks like this: 121.236.157.53\. That is, four sets of numbers separated by dots (periods). The Internet uses names to find Web site addresses, but these names are converted into IP addresses by Domain Name Servers (DNS), computers whose job it is to carry out this conversion so that computers can find each other. |

In Chapter 1, you learned about the Web server and how to set up folders for Web sites. You also learned about the cgi-bin, or scripts folder. You will be putting your Perl program in the scripts folder if you are using Microsoft Personal Web Server or into the cgi-bin folder if you are using a UNIX machine and something like Apache Web Server (an excellent choice).

Of course, if your ISP enables you to run your own Perl scripts, find out from them where you should put your scripts and if there are any do's and don'ts for your Web space. You will be using the 127.0.0.1 address to access your Web pages from your Web browser. Remember though, that if you choose to host your programs on your ISP Web space, you will use an address like:

http://*www.mydomain*.com/scripts/

Page 194

for the Perl code, and something like:

http://*www.mydomain*.com/

for the HTML.

Of course, if your IP address is static (that is, it doesn't change—most of them do) then you can use that instead of your domain name.

To create your first Perl CGI program, follow these steps, paying careful attention to the actual coding to make sure you don't leave out any code or make any typos.

**1.** Open your editor, creating a new file.

![Image](content/751124974c2b8c174e85c65ff3eb5a13.gif)

This line tells the Web server what kind of data is being sent. In this case, you are telling the server that this is going to be an HTML document, which is a subtype of a text document (hence the text/html part).

Note the two newline characters. These are very important—they are not for cosmetic purposes. The Content-type: text/html statement *must* be followed by two newline characters; otherwise, your program will not work and you will get a message telling you that you sent back incomplete headers or something similar.

Page 195

![Image](content/69fc939a86b2903551ee67b2377a2e26.gif)

| **NOTE** |
| Environment variables are variables that contain information about the server and the client (your Web browser). This information can be very useful when it comes to writing Web applications. |

Page 196

![Image](content/5ccd8db247cc66aa7094c54061211fec.gif)

And that's it—your first Perl CGI program. Not very exciting perhaps, but it's a good start and you will use it to check that your Perl/Web server setup is working.

**7.** Save your program in the scripts (or cgi-bin folder) as cgi1.pl, or if you want to follow the chapters in this book, call it 10-01.pl.

Now, open your Web browser, and in the location or address box, type the address of your server followed by the path to your script. Do you remember what the local IP address of you machine is? It's127.0.0.1.

**OR**

You can also use *localhost* as a name instead of the IP address, like this: http://localhost. So, you'd type in the following address and press the Enter key:

![Image](content/5ffb0042b4e5e26acff1499c5037a70f.gif)

Page 197

![Image](content/230c29059e768c26a26df5f2b9f4ae4d.gif)

If you are a Windows user and you get this problem, then do this:

**1.** Open the Start menu.

![Image](content/6a72e20df4834f2d1059d2506e9d0a1d.gif)

Page 198

![Image](content/f15522d6631e71dd5bb07e74577fae10.gif)

![Image](content/bb798e4719786019a8d6ee63d8367f77.gif)

Page 199

![Image](content/ac96409d6bc28b81c9d9d782fee9deb5.gif)

![Image](content/b1d281632dab0e8b8743c638c2bd5dde.gif)

Page 200

![Image](content/f9d9d4f298c14495f7eea165db38a7ae.gif)

Restart your computer.

| **NOTE** |
| Use lowercase s in the %s %s; %S %S will not work. |

| **CAUTION** |
| If you are at all unsure about modifying values in your computer's registry, then do not attempt to make any modifications. If you make a mistake when making changes to the registry, you can render your computer unusable, perhaps requiring the re-installation of Windows! Always follow your computer vendor's instructions on backing up the registry before making any changes. |

You have now proven that your programs should work with your setup. Now you can go a little further.

You just used a Perl program to display your IP address using an environment variable. You can display all of these variables with another simple Perl CGI program.

Page 201

**1.** Start your editor.

![Image](content/56077e79a976472ce82c7ee96a4853b9.gif)

![Image](content/07a2b7de0f37795e1249c2bdd9f5cf7f.gif)

Page 202

![Image](content/a3dedc6e228679a081a61407c0a1464e.gif)

**7.** Save your program as 10-02.pl.

**8.** Open your Web browser.

![Image](content/1474e69bce731a7023d79b97ee79fbd6.gif)

Page 203

![Image](content/465034c9d3335f4c340d0a1e39d9c4ae.gif)

Keep this program handy because it is useful to see what each environment variable does. You will want to use many of them when you start to build your own Web applications.

Your Perl Web applications are beginning to get just a little more interesting. But what can you do with them? You can find out information about the client browser and so on, but there is something missing.

### **HTML Forms**

To make Web applications really useful, you have to be able to ''talk" to them—to send them data and to get data back. You can get data back using the print HTML type statements we have used already. But how do you send data? To do this you need a little more HTML than we have covered so far. You need HTML forms.

| **NOTE** |
| Before you go any further, create a folder called myhtml under the wwwroot folder if you have not done so already. It will be useful for the examples you are about to try. |

HTML forms allow users to interact with Web sites by entering data which can then be used to populate a database or file, or perhaps to send an email to the owner of the site. Forms make Web pages useful! Using forms, you can collect information from users of your site and give them the information they want and need.

Page 204

#### **What Are Forms?**

If you are to build anything other than a flat HTML site; that is, if you want the page to do something other than display text and images, you have to connect the page to some storage mechanism. This would enable you to store data so that you can capture data from users and send data to a user's Web browser.

Normally, data is held in databases or files. If your page is to be able to manipulate data of some kind then you must be able to enter data in some way—this entry mechanism is the form.

The form has a number of elements, described in Table 10.1.

| **TABLE 10.1 Form elements and their purposes** |
| **Element** | **Purpose** |
| Text | Enables entry of short strings. |
| Textarea | Enables the entry of longer strings occupying a number of lines of text. |
| Radio Button | A ''one of n" choice selection mechanism. |
| Check Box | A true/false indicator—a box with a tick or an X when selected. |
| Select Boxes | A pull-down list of options from which one (or more) options can be selected. |
| Hidden | A text box wherein the box is not visible on the page. It is often used to carry data that the user does not need to see. |
| Password | Similar to a text box, but represents each character with an asterisk as the user types. |
| Submit Button | A button that enables the data entered into the form to be transferred to the processing mechanism. |
| Reset Button | A button that clears all data from the form so that the user can begin again. |

The form itself is defined using the <FORM> </FORM> tags and within them are tags to represent all of the data items needed.

Page 205

Here is a typical FORM tag:

<FORM NAME=''myform" METHOD="POST" ACTION="/scripts/myscript.pl">

The NAME attribute enables elements within the form to be referenced by scripts within the page, such as JavaScript, VBScript, and so on. You'll learn more about JavaScript in Chapter 15.

METHOD usually is set to either "POST" or "GET." This is a method of sending data to a script or other program.

##### ***METHOD="GET"***

Data sent by the GET method is sent along with the URL to the script all as one string. You might have noticed, when filling in a form on the Internet, something like this in the URL location box of the browser:

http://www.somedomain.com/scripts/ascript.exe?dataitem1=value1

Note the question mark separating the name of the script from the data that follows it.

The main disadvantages of this method are that the data that is being passed can be easily seen and also the length of the data string is limited.

##### ***METHOD="POST"***

This method sends the data to the "standard input" of the program to which the data is being sent. Programmers, especially those who have written software in C, C++, and so on, will understand what this means. Suffice it to say that this is a standard method of getting data into a program.

The main advantage of this method is that the amount of data that can be transferred is unlimited.

Page 206

#### **ACTION**

The ACTION is the attribute that describes the location and the name of the script or program to be executed. It will be something like

/scripts/myprogram.pl

Of course, you can use a program that lives elsewhere, perhaps on another server at another domain, in which case you can use the full syntax for the program like this:

http://www.mydomain.net/scripts/myprogram.pl

### **Using the Form**

Place the tags you need to represent all of the data to be collected by the form between the <FORM> and </FORM> tags.

You will now look at some typical tags used to describe the data input fields. Almost all fields in an HTML form are of the INPUT tag type.

| **NOTE** |
| Tag names in the following text will appear both all capitalized (example: SELECT) and all lowercase (example: select). In the early days of HTML it was a convention to always uppercase HTML tags. In recent years, it has become the convention to use lowercase characters through an HTML document, probably because HTML (or the programs that generate the HTML) is now often coded by programmers who are used to using lowercase in languages such as C, C++, Java, and so on. You should get used to seeing tag names written both ways. |

#### **Text Fields**

The text field is probably the most commonly used. Often, almost all fields on forms are of this type. They give you the usual rectangular input box that takes a single line of text.

Page 207

The HTML code for the text field looks like this:

<INPUT TYPE=''TEXT" NAME="surname" SIZE="30" MAXLENGTH="25">

The size attribute is optional and determines the size of the box in characters.

The MAXLENGTH attribute is also optional, and is used when you want to limit the amount of text that can be typed into the box. In this case, the limit has been set to 25 characters.

#### **Password Fields**

The password field is, in most respects, the same as the text field. The main difference is that text typed into a password field cannot be seen. Each character entered is replaced by an asterisk.

The HTML code for a typical password field would look like this:

<INPUT TYPE="Password" NAME="pwrd">

Obviously, the password field is useful for login type functions in Web applications.

#### **Hidden Fields**

Hidden fields are also very similar to text fields. The main difference is that you cannot see the field on the Web page at all. You might think that pretty useless, but it's very handy for quietly passing data from one page to another page or to a Perl CGI program.

The HTML code for a typical hidden field would look like this:

<INPUT TYPE="hidden" NAME="secret" value=3000>

#### **Radio Buttons**

The radio button gets its name from the old radios with the mechanical selection buttons for waveband. You used to press the button and any previously selected buttons would pop out. These radio buttons behave in a logically similar way. They are

Page 208

round in appearance (on most browsers.); if there are several of them and you select one by clicking it with the mouse, any previously selected buttons will be deselected.

The syntax of the radio button is

<INPUT TYPE=''RADIO" NAME="choice1">

If you want this type of field to be already selected, you add the SELECTED attribute.

<INPUT TYPE="RADIO" NAME="choice1" SELECTED>

The radio button can also have a value like this:

<INPUT TYPE="RADIO" NAME="choice1" value="1" SELECTED>

Here is a very simple HTML example just so that you get the idea.

**1.** Open your editor.

![Image](content/86cf78a7c7b4ff43101ed596cf57e066.gif)

Page 209

![Image](content/e2ee5f861bf95c1baaf3704ceb020764.gif)

| **NOTE** |
| The name attributes of the radio buttons all have the same name. It is this that causes the radio button effect. If you give them all different names, you can select any or all of them at once. Try it and see. |

**8.** Save your HTML in your myhtml folder or wherever you want to save it.

**9.** Open your Web browser.

Page 210

**10.** Type the address to your new HTML file in the address box of your browser and press the Enter key.

![Image](content/d3b68c9045e508ddb694e26167a47dea.gif)

**11.** Play with the radio buttons and observe the effect.

**12.** Change the names of the radio button name attributes and see how they no longer reset each other when you select them.

#### **Check Boxes**

The check box is another useful type of input box. It is similar in principle to the radio button, except that it is designed for multiple choices—you have no doubt seen the online survey forms wherein you are asked to choose from a list all of the items that you like or agree with.

Even giving the check boxes the same name does not change their behavior. It does make them a little more difficult to deal with, so it would make more sense to give them their own individual names. You can have a page full of check boxes and select as few or as many as you want.

Also, note that you deselect check boxes by clicking them again.

<INPUT TYPE=''CHECKBOX" NAME="selection1">

Again, if you want to show this field already checked, then add the checked attribute.

<INPUT TYPE="checkbox" NAME="choice1" checked>

Here is an example similar to the previous one, but for check boxes instead.

Page 211

**1.** As in the previous example, open your editor and start a new HTML file.

**2.** Complete the usual HTML header.

<html> <head> <title>Checkbox Demo</title> <head>

![Image](content/31f202ad3fe221cd3c3ab820d3b0117a.gif)

**8.** Save your program in your myhtml folder as check.htm.

Page 212

![Image](content/1906f59ae86b4825d51f63010910818e.gif)

#### **Drop-Down Boxes**

For drop-down boxes you use the <SELECT> tag. The select tag is a little different from the others in that it is not a variation on the <input type= > type tag.

A typical select tag looks like this:

<SELECT NAME=''country"> <OPTION value="UK" SELECTED>UK</OPTION> <OPTION value="USA">USA</OPTION> <OPTION value="France">France</OPTION> <OPTION value="Germany">Germany</OPTION> </SELECTED>

The select tag has embedded within it a number of option tags. Each option tag holds one option. The value clause of the option statement is the value that is actually used by the form. The text immediately before the option tag is the text that is actually displayed on the page, although often the two will be the same.

If you want to show one of the options as preselected when the page loads, you include the selected attribute within the option tag.

Page 213

You can also specify a size for the select tag, but this looks confusing to the user. But you can use the size tag when you add the multiple attribute to the select tag. This tells the select tag that you can select more than one option. The user does this by holding down the Ctrl key and then clicking more options with the mouse. You can also select a block of options by clicking the first option, moving down the select list until you get to the end of the block you want to select, and finally holding down the Shift key and clicking the last item. All the selections in the block then are selected and turn blue.

Now you can use the size attribute of the select tag. The size attribute determines how many options are visible.

Try the following to see an example of both types of select tags.

**1.** Open your editor.

**2.** Start a new file.

![Image](content/cffbb55adb72ff21dc3a9d33f9851890.gif)

Page 214

![Image](content/dc8dd5aeb0d8ea0196a9e5ba1b9e2e61.gif)

Page 215

![Image](content/8bed435e485f2a64d4d7ae26b9359155.gif)

| **NOTE** |
| This time there is no selected option, but you do have the multiple attribute on the select tag, so more than one value can be selected. |

**13.** Save your new HTML page as select.htm.

Page 216

**14.** Open your browser.

![Image](content/107065b0d3f0b8a688c16bce607a31c1.gif)

You will find the <select> tags very useful for many reasons. Say you are going to save data from an HTML form in a database and you want to be able to manipulate that database later. Suppose you want to pick out the people who live in London. Some people will type **London**, some will type **london**, and some might even spell it wrong. If you use a select box for all such fields, you eliminate the possibility of input error for those fields.

#### **Text Area Fields**

The text area field is useful when users want to type in lots of text. You can provide a place for users to type with the <input type=text> tag, but with that method, the user can't see what he's typed once he's filled the box, because the text ''tickertapes" out of the box to the left. With a text area field, you have a number of rows of text, so that as the user types the text scrolls up the box. You can also have a scrollbar so that the user can scroll up and down the text to review it.

<TEXTAREA NAME="comments" COLS="50" ROWS="50"></TEXTAREA>

There is not a value clause with the text area. If there is a default text, then you place it between the <textarea> and the </textarea> tags.

Page 217

Here is an example of the text area box.

**1.** Open your editor.

**2.** Start a new file.

![Image](content/05765e361011395a3732167a175458e6.gif)

**8.** Save your new HTML page as textarea.htm.

Page 218

**9.** Open your browser.

![Image](content/c2cfffe0cf182a0407a81345338119ab.gif)

If you wanted default text in the text area, the HTML code would look something like this:

<textarea name=bigtext cols=60 rows=5>Here is some default text</textarea>

That's enough about form input elements for now. Next, you can put together a complete form ready to send data back to your Web server and to your waiting Perl program. When you have written it, that is.

#### **Submit and Reset Buttons**

Before the form becomes really useful, you will need a submit button; that's pretty straightforward too.

Also, you might sometimes want a button to reset the form, so that if the user has made a hopeless mess of the form, he or she can click the reset button to clear all of the form entries and start again.

Try this.

**1.** Open your editor.

**2.** Open a previous program, such as select.htm.

Page 219

![Image](content/ef35b58576a0b4d1c27bce27ec62164d.gif)

**7.** Now save your program in the myhtml folder as form1.htm.

![Image](content/494414f24aeb1eb2ef8854ab643d2b01.gif)

Page 220

Now the form will work, but if you click the submit button, you will get an error because you do not yet have a program to handle your form. You can test the Reset button by making your selections and typing something into the notes field, and then clicking the Reset button. Your selections should be reset and the text you typed into the Notes text box should disappear.

Now you know how to capture user input. Next you will learn how to handle that data at the server and how to send replies or ''responses" back to the browser on the client machine.

Page 221

## **11
CGI: Making the Connection**

You now know the basics of Perl—you know how Perl variables work, you can build forms, and you even know what you can do with data after you get it onto the server. You can build an HTML page, and you have learned how to provide navigation through hyperlinks, how to add color, and how to build forms to capture data from users. You have even learned about environment variables and how useful they might be.

What you have not learned yet is how the information gets from your form into your Perl program on the Web server. Now you'll see how to make the connection from HTML form to Perl script.

In this chapter you will:

![Image](content/d938f552af65a53b177029c39d905885.gif) Examine how data is received from forms

![Image](content/d938f552af65a53b177029c39d905885.gif) Learn how to use HTML tables

![Image](content/d938f552af65a53b177029c39d905885.gif) Learn how to get form data via the GET and POST methods

Page 222

### **Receiving Data from Forms**

As always, the best way to demonstrate the way you use forms is by way of a simple example. But first, you should learn about another feature of HTML: tables. This is a good time to discuss HTML tables, as they are very useful for creating neat form layouts!

#### **HTML Tables**

HTML tables are used to (amongst other things) format the contents of a Web page. In this section you'll learn how to use them to make a Web input HTML form look prettier. Tables are not essential for forms—but they do make them look better. You could just use spaces (&nbsp;) and breaks (<BR>) to position the form elements on the page, but it probably wouldn't look very good.

As you would expect, a table starts with the <TABLE> tag. The <TABLE> tag has a number of attributes; for example, you can use background = imagename.jpg to set the background image of a table, just like you did for the <BODY> tag. In the same way, you can set the background color using the bgcolor attribute.

You can set the width of the table using the width=nnn or width=nn% attributes of the table tag, rather like the width attribute of the <HR>, horizontal rule tag.

A typical table tag might look like this:

<table width=600 bgcolor=lightblue>

This code says to create a table 600 pixels in width with a light blue background color. Simple enough, isn't it?

A table achieves its aims by being what you would expect it to be: a table of rows and columns into which you can place the elements, pictures, or text you choose.

At the top of a table, you can have an optional ''header" row, intended for things like titles. A header row looks like this:

<tr><th width=200>Column Title 1</th><th width=200>Column Title 2</th><th width=200>Column Title 3</th><tr>

Page 223

The <tr> tag signifies the start of a table row. The <th> tag defines a table header for a column, in this case the width of the header, and therefore the whole column has been fixed at 200 pixels (again, percentages could be used). The </th> tag closes this header. In this example, there are three identical headers containing three column titles for the table.

Note that although the width of the headers is set in this example to 200 pixels, if the title between the <th> and </th> tags exceeds 200-pixel width, the column will stretch (that is, any cells directly beneath the header tag will stretch) to accommodate the text, image, or whatever you choose to place within it.

At the end of the headers, the row is closed using the </tr> tag.

Following rows can contain what HTML calls *data*. The format of the data rows is very similar to the header row, except that the individual cells are defined by <td> tags instead of the <th> tag of the header row. A header row or a data row can also have its own width tags, background color tags, and so on.

A data row may look like this:

<tr><td>Column Title 1</td><td>Column Title 2</td><td>Column Title 3</td><tr>

An HTML table can contain many rows of data, which is, as you will see, very useful in Web-based applications.

Each <td> or <th> tag can have its own background color, bgcolor, width, and height attributes. They also can have tags for aligning the contents of the cell. Horizontally, alignment can be specified as left, center, or right. Vertically, alignment can be specified as top, middle, or bottom. So for example, a <td> tag can have its alignment attributes specified thus:

<td align=''center" valign="top">

Note that the valign and height attributes can also be added to the <tr> tag.

The HTML table is closed, as you would expect, using the </table> tag.

The following form example shows how a table is used to position the form elements to produce a neat layout.

Page 224

**1.** Open your editor.

**2.** Create a new HTML page.

![Image](content/f6b12346217b6b43074253fe70df9fa5.gif)

| **NOTE** |
| You are using the POST method. You learned a bit about this method in Chapter 9\. You will learn a little more about POST and GET in this chapter. |

Page 225

![Image](content/484d77d767f5d86df2f0e1873db8a32c.gif)

Page 226

![Image](content/e5cbbeadfe8be06f2039f89989b72b35.gif)

**13.** Save the form HTML as 11-01.htm in a suitable folder under the wwwroot folder in your Web server folders.

![Image](content/83ba0e91140d0ced263e065a7f916e28.gif)

At this point you cannot actually submit the form without receiving an error, as you have no Perl program yet to accept the data. That's what you are going to do next.

#### **Getting Form Data via the POST Method**

In your editor, start a new Perl program. Now you are going to add a Perl program to deal with the input from your HTML form. This small Perl program will require some explanation, as there will be some code you haven't seen before.

Page 227

**1.** Start your program in the usual way, and add the HTTP header line.

#!c:/perl/bin print ''Content-type: text/html\n\n";

![Image](content/1a87ad2a7d3bb6153ac32505555a6de0.gif)

An array, called @pairs, is used to contain the key value pairs from the form. This line of code uses the split function to separate each key-value pair from all the other pairs so that you end up with an array of pairs each containing a field and its associated value. (Notice that each pair is separated from the next by an & character; the split function in this case uses this character to separate the data into discrete pairs.) You are almost at the stage where you have something useful.

Page 228

![Image](content/1298867538bd7488096a846929e57129.gif)

Page 229

| **NOTE** |
| Again you have a pattern-matching line using the binding operator. The command using the pattern is the substitute command, s. In this case, hexadecimal codes, which replace symbols during their transmission via HTTP, are substituted with their character equivalent. The /g at the end of the command simply means ''global," that is, replace each occurrence found in the data. |

![Image](content/ee13b7f65bfe202169f4b65f7e5525ab.gif)

That seemed like hard work didn't it? But read through each line and the notes attached to each step and I think you will agree it's a lot simpler than it might first appear.

Page 230

**12.** Save your code as 11-01.pl.

![Image](content/17e15a3aef50120666174b3fa00c9eac.gif)

![Image](content/fe2db9f1f4635c6c5f8f4b1a2c970f4e.gif)

#### **Getting Form Data via the GET Method**

Okay, now you know how to get at data sent from a form using the POST method. How about the GET method?

The good news is that most of the code is the same. In fact, in the form, all you need to do is to change the: method= ''post" attribute to: method= "get".

Page 231

Try the following:

**1.** Re-open your 11-01.htm page into your editor.

![Image](content/8392f51d14365a152ca9b14d395f2bd1.gif)

**4.** Now re-open your 11-01.pl program.

**5.** Remove the following line:

read(STDIN,$tempbuffer,$ENV{'CONTENT_LENGTH'});

![Image](content/41ad95c2aeba1e90ceebc34dffe848cf.gif)

Page 232

| **NOTE** |
| Now you are taking the data contained within the environment variable QUERY_STRING as your source for the form data. Note that you do not have a ''read" command anymore, as the data is, in the case of the GET method, simply a part of the URL, and therefore appears in QUERY_STRING. |

**7.** The rest of the code is identical to the 11-01.pl; now save this code as 11-02.pl in your scripts folder.

![Image](content/5f771ad0140928cbe85387135a168c9e.gif)

Page 233

![Image](content/f96f09e9c610774d631054c1ff26300b.gif)

Once again the data fields used on the form are displayed along with their respective values.

In this chapter you learned how to obtain user input from an HTML form using both the GET and POST methods. This is a major milestone, as you have now made the link from user input at a form in the user's Web browser to actual data available for use on the server.

So, you can create the forms and you can grab the data in your Perl program. Now, what are you going to do? One thing you might like to do is to save the data into a file. So, in the next chapter you will learn about files.

Page 234

*This page intentionally left blank.*

Page 235

## **12
Using Files in Perl**

In this chapter, you'll learn how to use files in Perl—how to create them, write to them, read from them, and delete them. You will also learn how to create and remove directories in Perl.

In this chapter you will learn how to:

![Image](content/d938f552af65a53b177029c39d905885.gif) Open a file in Perl

![Image](content/d938f552af65a53b177029c39d905885.gif) Read data from a file

![Image](content/d938f552af65a53b177029c39d905885.gif) Close a file

![Image](content/d938f552af65a53b177029c39d905885.gif) Use directories

![Image](content/d938f552af65a53b177029c39d905885.gif) Delete a file

Page 236

### **Opening Files in Perl**

Before you can do anything with a file, you need to open it. This is done using the Perl open function. The general syntax for the open function is

Open(MYFILE, ''testfile.dat") || die "Error encountered when opening file ...";

This means that Perl will attempt to open a file whose file handle is MYFILE. A *file handle* is a reference variable that is used to store the *internal name* of the file, that is, the name by which the Perl program will recognize the file.

Following the file handle is the real name of the file; in this example, testfile.dat.

Notice in the line of code that the next thing on the line is a *double pipe*. This is the OR operator and is used here to execute whatever follows it if the file open code fails. In other words, if for any reason the file cannot be opened by Perl, the code following the || symbol will be executed.

The code after the double pipe OR operator simply says

die "Error encountered when opening file ..."

The die function then stops the program running after displaying the message "Error encountered when opening file . . .".

A general error message in itself isn't very helpful. However, Perl also has a special error variable that holds the error message for an event such as this. This is the $! variable. You can now add this variable to the die error message:

Open(MYFILE, "testfile.dat") || die "Error encountered when opening file . . . $!";

As you would be unable to see anything when a file is successfully opened, trying an example would be a bit pointless right now. The next step will be to read a file so that you can see the open function in action and see how data is read from a file. If you want to, you can rename the input file so that the program cannot find it, and then try out the die function and error message.

Page 237

### **Reading Data from a File**

Data may be read from a file in Perl using the angle operator, < >. To get a line of data, you simply wrap the file handle in the angle operator like this:

$dataline = <MYDATA>;

This will take any data from MYDATA (testfile.dat) and store it into $dataline. The data will stop when a newline character is encountered.

The end of a file is recognized when the file handle returns ''undefined." So to read and display the whole contents of a file you can do this:

while (defined($dataline=<MYFILE>)) { print "$dataline <br>"; }

This can be simplified still further if you do not have any other conditions in the while statement. The while statement will execute while the conditions in the following parentheses are True. The condition "undefined" of the file handle is effectively False.

Therefore, you can now say

while (<MYFILE>) { print; }

Note that now, unless you had <BR> tags at the end of your lines of data in the file, the data would all be joined together. Of course, you could put a separate print line after the empty one to provide the <br> tag.

while (<MYFILE>) { print; print "<br>"; }

Page 238

| **NOTE** |
| You cannot add a <BR> tag to the first print statement, as it would then no longer be reading the data from $_, but would instead just directly print <br> and nothing else. |

Now, providing you have a file to work with, you can try out both the open function and reading data from a file.

**1.** Open your editor and clear it of any default code that the editor might create so that you have a completely clear file.

![Image](content/caac84632ae530b5207b47ddb5d37731.gif)

Page 239

![Image](content/c6b065e9ef81ada54c01cd8fd0a1fdcc.gif)

| **NOTE** |
| Note the use of double backslashes. The string is double-quoted and so *interpolation* will occur. If this was not done, then, should any part of the path begin with an ''n," it would be treated as a newline character. The double backslashes suspend the interpolation process for the characters following those double backslashes. An alternative to prevent character combinations being treated as special characters is to use forward slashes, as you will see in UNIX programs. This will work with Windows too, so you may prefer to use forward slashes rather than double backslashes like this: |
| open(MYFILE, "c:/inetpub/wwwroot/filetest/testfile.dat")        &#124;&#124; die print "Error encountered opening file . . . $!"; |

Page 240

![Image](content/c64b966316b67b481a1bb484ad1280ce.gif)

| **NOTE** |
| So you have a while loop, the terminating condition of which is when the input from the file is undefined; that is, you receive a null input from the file. |

**8.** Save your file as 12-01.pl.

![Image](content/b116c5961677c6f06f29c7275189f0fe.gif)

Page 241

![Image](content/39202078bdcf952788d4e5d09f24e654.gif)

**10.** Save the program as 12-02.pl.

![Image](content/444635b2989b84e0b63e262eb4e57e34.gif)

Just to prove that the error condition is indeed trapped, try temporarily renaming your data file to anything you like and then re-running your code. You should get the error message.

### **Error Checking**

The die function you have used so far is the simplest way of checking for errors. As an alternative you could use the code on the next page.

Page 242

If (open(MYFILE, ''testfile.dat")) { while (defined($dataline=<MYFILE>)) { print "$dataline <br>"; } } else { print "There was an error opening the file …"; }

This works because the open function returns a False value if it fails. (More correctly, if you displayed the value, you would find that it is returned as undefined). If it succeeds, it will return a non-zero value. Any non-zero value equates logically to True, so the rest of the code to read data from the file is executed.

The advantage of trapping errors in this way is that the program does not have to abort. The die function stops execution of the program, and therefore should be used where failure to open a file is considered a catastrophic error.

#### **Closing a File**

When you have finished with a file, you should always close it. Doing so is good programming practice and also ensures that resources no longer being used are returned to the operating system. If this is not done in large systems, the upper limit for the number of file handles that can be open at any one time may be reached and the system may then fail.

To close a file, simply use the close function. For the previous example, it would be coded like this:

close (MYFILE);

Page 243

![Image](content/d4403fc31ff740f7bac36e82cbe42627.gif)

Save your updated program as 12-03.pl and check that it works.

### **Writing to a File**

You have learned one way to get data from a file. Now you are going to learn how to write data to a new file, and how to add data to an existing file.

#### **Opening the File for Writing**

Opening a file for writing is just as easy as opening a file for reading. You simply use the open function, like this.

open(MYFILE, ''>c:\\inetpub\\wwwroot\\filetest\\outfile.dat")

Note that there is only a very subtle difference between this and opening the file for reading—the inclusion of the > symbol in front of the filename.

Page 244

To create a file from a Perl program, do the following.

![Image](content/2315ca870dbd83955a501ae273159806.gif)

| **NOTE** |
| Each entry in the array ends in \n and each entry is double quoted so that the newline \n characters are correctly interpreted. |

Page 245

![Image](content/5cd5147158e4f2747e042af607370738.gif)

| **CAUTION** |
| In this example you used the > symbol at the front of the filename in the open function, causing a new file to be written. If you run the program again, it will still do the same. That is, any previous file will be overwritten. It is very important to remember this for the future to avoid losing important files. |

**9.** Now save your file as 12-04.pl.

**10.** Run your program (http://127.0.0.1/scripts/12-04.pl).

Page 246

![Image](content/7cbe913177c75d164dc88c494c843a21.gif)

##### ***Adding Data to an Existing File***

You can also add data to an existing file. The change in the code to achieve this is very subtle. Remember that you added a > sign to the front of a filename in the open function so that you could write to the file. All you have to do to open a file to append data is to put two > signs at the front of the name.

Try it:

**1.** Re-open your write file program (12-04.pl).

![Image](content/908231b86e47526be0ba51ea63935ef0.gif)

**3.** you now have >> at the front of the filename attribute of the file open statement.

**4.** Save your program as 12-05.pl.

Page 247

**5.** Run your program (http://127.0.0.1/scripts/12-04.pl).

![Image](content/2cd1fcd93bed811e121092f955b1ebd3.gif)

![Image](content/f9abfd276310a8607990accb5ad7f581.gif)

As you can see, instead of overwriting the file outfile.dat as 12-03.pl would do, you are now adding each copy of the text in your program to the end of the file.

### **Deleting a File**

Deleting a file is very straightforward. It is accomplished using the oddly-named unlink function.

To demonstrate the unlink function, delete the output file you just created.

Page 248

![Image](content/89e407d152a2043fb753b3e5145be0a2.gif)

Page 249

| **NOTE** |
| Multiple files can be specified by separating the filenames with commas. |
| Unlink(''c:/inetpub/wwwroot/filetest/outfile.dat,    c:/inetpub/wwwroot/filetest/anotherfile.dat ")
   &#124;&#124; die "File(s) could not be deleted …"; |
| You can also store all the filenames to be deleted in an array so that your delete becomes |
| @files = {"c:/inetpub/wwwroot/filetest/outfile.dat",    "c:/inetpub/wwwroot/filetest/anotherfile.dat"}
unlink(@files)
   &#124;&#124; die "Files could not be deleted …"; |

**5.** Save your program as 12-06.pl.

![Image](content/84e42b551944acce1d39299001c2d7bc.gif)

### **Using Directories with Perl**

Perl is also able to create and remove directories or folders. This makes it very powerful, as it's able to create any environment or file and folder structure that your application needs.

Page 250

#### **Making a Directory**

Making directories or folders with Perl is very easy, and the functions used are very similar to the equivalent DOS and UNIX commands. The function used to create a directory is mkdir.

Try this simple program.

![Image](content/5185edee439eef45057994f3119180e9.gif)

**4.** Save your program as 12-07.pl.

Page 251

![Image](content/78cf753c9cdbe1ae7457d2ffd68c9617.gif)

![Image](content/b56eead726a8fa3c0ed068610f490705.gif)

#### **Removing a Directory**

Removing a directory is just as easy as creating one, and as you would expect, it uses a similar syntax to the DOS rmdir command.

Page 252

![Image](content/c0ea1d408e048ccf42dd15f672e21c51.gif)

**4.** Save your program as 12-08.pl.

![Image](content/e2d66a0c02cbb92dee0b4bfb6a863cab.gif)

Page 253

![Image](content/5a5cb61feb12f3ec07f5e9c60c6ba7f7.gif)

There are lots of other things you can do with folders, such as change permissions and so on, but that is beyond the scope of this book. In most cases, being able to change permissions on folders through a Web application could be pretty dangerous.

### **Data Files**

You have already seen how to read data from and to write data to a file. But in that case, the data was simple strings of text. On most occasions your data will be more sophisticated than that. For example, a simple employee directory may store its data in separate fields for data items such as forename, surname, department, telephone number, and so on. How do you know which bit of data belongs where in a file?

You have to tell your program how to determine that. It's not as daunting as it sounds. All you have to do is to decide on a character to use as a *field separator*. Often, you will see the comma used for this purpose, but what if there are commas in the data? Just use a different character that is not likely to appear in the data. You can use any character you like; in the following examples you will see the *not* (¬) character used. It really doesn't matter what you use as long as you can use it to separate each data item from the next, and as long as that separator does not appear in the text.

Page 254

| **NOTE** |
| If you have a U.S. Keyboard (or any other besides British), you can get the ¬ character into your editor by holding down the ALT key and typing 170 on the numeric keypad on the right hand side of the keyboard. Release the ALT key and the character will appear in your editor code. But, as I said, you can use any character you like. |

Right now, take a look at reading and writing data from and to files and see how you can retrieve the information as separate fields of data.

#### **Writing Files**

Try the following example, which is almost identical to a previous example except for the data, which is stored in a field called $thisline. The difference is that this is not *one* item of data but *four*, as you will see.

![Image](content/f63992675d9e1431450e57ac30207d7e.gif)

Page 255

![Image](content/6e74121eb8b110ab773b903522c74a55.gif)

**6.** Save your program as 12-09.pl.

![Image](content/245a7151c13cc4f85185258a5e0844dd.gif)

Page 256

![Image](content/6c1a5f77c9e1b1f838df6a27e7dda052.gif)

The next step is to be able to get your data back from the file.

#### **Reading Files**

Now try retrieving the data you just wrote to the file called personnel.dat.

![Image](content/e6f5aeadd6823d6115047c576ac6d4bf.gif)

Page 257

**3.** Using a while loop, read the data from the file.

while (defined($dataline=<MYFILE>)) { print ''Reading file …<br>";

![Image](content/f2db618c2070f0d37f75ab09b35a103a.gif)

**8.** Save your program as 12-10.pl.

Page 258

![Image](content/5e10c3f2192cf6d8aefa99540faffcb8.gif)

As you can see, files are useful to have available when building applications, and indeed there is much you can do with them.

By now, you have learned the basics of the Perl language and now you can use some of the features of Perl to grab data from a user on your Web page and store that data in a file. You have learned how to retrieve that data and send it back to the user, or do whatever you want to do with it. You can now build applications that are fully interactive with the user. You may not be confident yet—so far this books has shown you brief, easy to understand examples, and the leap from those to a full application may seem a little daunting—but you are getting there.

Files have enabled you to complete the loop. They give permanence (often referred to as *persistence*) to your data, so that when your users come back another day, they can see their input staring back at them. And that is something that, as a budding Web developer, you will find immensely satisfying.

Even more powerful are databases, but before you learn about how to use them in Perl, you will learn about another subject that is very useful in Web applications: e-mail.

Page 259

## **13
Sending E-mail in Perl**

E-mail is a useful addition to the facilities in your Perl Web applications. And it is not difficult to send e-mail in Perl. Unfortunately, the methods used to do so differ, and it is largely a matter of asking your ISP for information. E-mail requires a program called a Mail Transfer Agent (MTA) to send the e-mail to an SMTP server. On the UNIX platform, the shell command sendmail does this. In Windowstype environments there is the SMTP server that comes with Microsoft's Internet Information Server (IIS), but there is no MTA in Windows. Instead, you can use a package called SMTP in Perl to help you send e-mail, or you can use a more recent module called sender.pm. A program called Blat.exe can also be used on Windows platforms to send e-mail via SMTP.

In this chapter you will learn:

![Image](content/d938f552af65a53b177029c39d905885.gif) What FTP is and how to use it

![Image](content/d938f552af65a53b177029c39d905885.gif) How to use SMTP in Perl to send e-mail

![Image](content/d938f552af65a53b177029c39d905885.gif) How to send e-mail using Blat.exe

![Image](content/d938f552af65a53b177029c39d905885.gif) How to send e-mail on a UNIX server using Sendmail

Page 260

Because methods of using e-mail vary from ISP to ISP, I will describe each method generally, but with real code. Obviously, it is difficult to demonstrate with screenshots that e-mail has worked, but I'll describe and show the code as usual. Please check with your ISP if you have any problems, or ask your ISP before you start if there is anything you need to know about your particular environment. Most problems will be minor—you may have to change the path to the Blat.exe or the Sendmail program, for example.

Regardless of the platform that is being used, the method of sending e-mail is similar. Certain information is needed to send an e-mail, no matter what hardware or software you are using. For example, the following data items will always be required:

• Recipient

• Subject

• Message body

• Sender

Armed with this basic information, you can build a Perl program to send e-mail.

As I have said, the basic method of sending e-mail on all platforms is similar. The general method is to:

**1.** Define the path to the mail program.

**2.** Open the mail connection.

**3.** Supply the recipient and subject information.

**4.** Send the mail body data.

**5.** Close the e-mail connection.

### **Using FTP**

Before you begin to learn about e-mail in Perl, you need to know how to get your files from your machine up to your ISP or hosting company Web space because, for this chapter, you need to step outside of your development cocoon (Microsoft Personal Web Server if you're using Windows 9x or Peer Web Services if you're

Page 261

using Windows NT). You will also need to use Web space that has an e-mail service attached to it. You need an SMTP server or some means of being able to send e-mail. To get your work onto your ISP Web space, you're going to have to learn how to get your files from your machine up to the ISP server using FTP (File Transfer Protocol)

### **What Is FTP?**

FTP is the means by which you are able to transfer your files from your computer to another, usually a server at your ISP installation where you keep your Web sites and Web applications.

It isn't difficult to learn to use FTP, but it's a good idea idea to become familiar with it to remove some of the guesswork and to speed you along your way. So, before you start to learn about sending e-mail, read this short briefing on how to use FTP. I shall use one example of an FTP client; there are many, but they are basically very similar. There are a number of FTP clients on the market, and some of them are free for personal use.

| **NOTE** |
| For the purposes of this discussion, I will concentrate on WS-FTP LE (the LE stands for Light Edition). This is an excellent, free FTP client that is easy to use and very effective. |

#### **How Do I Use FTP?**

First of all, obtain a copy of WS-FTP from http://www.ipswitch.com. Download a copy of the installation file, follow the onsite instructions, and install a copy of WS-FTP LE. There are a number of FTP clients out there, so you may want to shop around to find a product that suits you once you are comfortable using FTP.

After you have installed the product, you have to configure it. To do so, follow this procedure.

Page 262

![Image](content/90be19eef1c9962c8307ac9c891b3122.gif)

![Image](content/d136068e03aadf3d7e8d18e872da8c21.gif)

Page 263

![Image](content/6c36fa2c1d730a5e80e04923cb65454a.gif)

![Image](content/c6b723d2322680b047e29240148ca9dd.gif)

Page 264

| **NOTE** |
| Of course, you can also transfer them the other way, by highlighting files in the right window and clicking the left arrow button. You can select more than one file by holding down the Shift key as you click with the mouse to select a list of files that are grouped together in the list, or by using the Ctrl key as you click the mouse to select files that are not together in the list. |

Try transferring some files and you will soon see how easy WS-FTP is. Like most Windows-type tools, the easiest way to learn how to use them is to play with them and read the help screens.

One thing to note is that you will want to transfer your Perl and HTML files as ASCII. Your images will be transferred as binary files. If you look at the bottom of the WS-FTP transfer screen, you will see radio buttons for ASCII and Binary. Select the appropriate one for the type of file you are transferring.

| **TIP** |
| The Auto button uses the file extension to determine whether to use binary transfer mode or ASCII. To set up the extensions in order to transfer files automatically, click the Options button, select the Extensions tab, then add all of the ASCII extensions you may want to use. |

There are lots of settings for you to play with in WS-FTP LE, but I will leave you to discover them yourself; I suggest you read the help documentation before changing any setting.

### **Sending E-mail Using SMTP in Perl**

Perl has a module called Net that contains its networking functions. One of the components of Net is the SMTP module that contains all of the functions needed to send e-mail via an SMTP server. Try the example on the next page.

Page 265

**1.** Open a new program in your editor.

#!c:\perl\bin

![Image](content/71f461378958daf040684cdafd8da3fb.gif)

![Image](content/ee77ecf673a85ddf3a17b771e1d1e503.gif)

Page 266

![Image](content/f846acc58b7dd4c4d3f1664609e611e1.gif)

![Image](content/99a40abfe4ea7bea3bda8d6fe4b5153c.gif)

| **NOTE** |
| The subject was terminated with two newline characters. This tells the SMTP server that this is the end of the header information, and that what follows is the body of the message. The message also ends with two newline characters, indicating that the end of the message has been reached, as you will see next. |

Page 267

![Image](content/6797db198fec910febbf4bcd0b0a5d7d.gif)

**17.** Save the program as 13-01.pl and upload it into your cgi-bin or scripts folder in your ISP or hosting company's Web space using a suitable FTP client.

**18.** Open your browser and enter the URL for your program (http://www.*yourdomain*.com/cgi-bin/13-01.pl). Notice that you will not see any output on the screen. If you want to see something to reassure yourself that the program completed, put in a print statement with a suitable message.

That's one way of sending an e-mail. There is another way that you may find useful if your site is hosted on a Windows server: using the Blat program.

### **Sending E-mail Using Blat.exe**

Many Windows-based ISPs send e-mails by means of a freeware program called Blat.exe. This was actually originally developed as a command-line e-mail program, and it sends its e-mail text from a file. In fact, where this program is used on the Web, it still uses a file and it stills uses Blat.exe as a command-line program, sort of. You use the system Perl command that is designed to enable you to run any executable program from within a Perl program.

Page 268

So, under normal circumstances, what you have to do is collect the address information and data (text) you are going to send from an HTML form. Then you save the text data to a file. Then call the Blat.exe program and send your data and message text file as parameters. *Parameters* are just individual items of data that a program needs to complete its job or to tell the program how to behave. In this case they are items of data such as recipient address, sender address, and name of the text file containing the message.

Try out the following program (if your ISP or hosting company offers the Blat.exe facility).

**1.** Start a new program in your editor.

#!c:\perl\bin

![Image](content/d5d6fd02ff3f5619c4721bf240f65c78.gif)

| **NOTE** |
| Note the \ character; this enables you to escape special characters such as the @ character, which would otherwise be interpreted as an array indicator by Perl. 
For testing, you will probably want to put your own address in the $recipient variable. |

Page 269

![Image](content/66b8f2dad452fea85a4b9db8b6dff4a5.gif)

![Image](content/c171be3afff32435a7169c68397ff2c4.gif)

Page 270

![Image](content/23b1de7462cd4e0d884dea86f8573102.gif)

Note the different use of the if statement. It simply means do the first part of the statement if the variable being checked has something in it.

![Image](content/a94f7dabbacfd63a8295ebe1aced010b.gif)

Page 271

![Image](content/730ac2621890b0053aac4fbd010211f3.gif)

**17.** Now save your program as 13-02.pl.

**18.** Upload the program to your Web space.

**19.** Create a text file containing a message and save it at the location you put in your $message variable.

**20.** Upload the message file to that location.

**21.** Open your Web browser and enter the URL (the location of your scripts folder will be determined by your ISP or hosting company) for your script to run it.

All being well, you will shortly receive an e-mail. If you do not, check your script again. If you can't see anything wrong with it, consult your ISP or hosting company and ask it for an example of how to use Blat.exe on its system (ISPs often have sample scripts that you can use, in which case you save yourself a lot of work).

Page 272

The Blat program is not very sophisticated and the additional step of having to create a file is a nuisance. But it can be useful, and it may be all your ISP or hosting company offers, so it is a good program to learn.

You can also create a file using Perl from data that a user has given on a form. So you would get the data from the form (you already know how to do that now), write the text data to a file (you can do that too), and then let blat.exe run as shown previously.

The program given here is a typical example of a Perl program for sending e-mails, but there are lots of possible variations in terms of directories and so on, so talk to whomever you host with. You may find that your ISP will supply you with a working example to plug in to your applications.

### **Sending Mail on a UNIX Server Using Sendmail**

The UNIX community has had for years a mail program called Sendmail. It is quite simple to use, but again, before you start, talk to your hosting company or ISP to learn about any local variations or hints for using sendmail from their servers.

Try this example, after you have spoken to your hosting company, making any modifications that your company indicates for its particular installation (again, the company may offer you a pre-written example that will save you time on debugging).

Following is a simple example of using Sendmail in Perl.

Page 273

**1.** Open your editor and start a new program.

#!/usr/bin/perl

| **NOTE** |
| Note the UNIX shebang statement—the path is different, which matters in the case of UNIX, as the shebang statement is not just a comment, but is used by the operating system to find Perl. |

![Image](content/5399ff07f103cc71691ebcf9f4d3872b.gif)

| **NOTE** |
| For testing, you will probably want to put your own address in the $to variable. |

Page 274

![Image](content/46d63af0ea41883ad4ce00d58f82baa7.gif)

**9.** Save your program as 13-03.pl.

| **NOTE** |
| Note the pipe symbol (&#124;) before the $sendmailpath variable. This tells sendmail that its input can be taken from STDIN, which is the default input stream. 
The option–t is added to the Sendmail open command. This simply tells Sendmail to scan for To, CC, and BCC data.

Also note the use of the die option and the use of the $! variable to report (hopefully) some meaningful information in the event of an error. |

Page 275

**10.** Now upload your program to your ISP host.

**11.** Open your browser and enter the URL for your Perl mail program and press the Enter key.

If all has gone well, you should receive an e-mail. If not, check the script and correct any errors. If you still have problems contact your ISP to check the details for Sendmail on its servers.

Sendmail is a very well-known, tried, and tested e-mail program, and you shouldn't find many problems with it. It is also the most commonly available program on UNIX type servers. It is also increasingly becoming available for Windows platforms.

Keep an eye on the Web and look out for new tools that suit you and your host environment. And remember, talk to your ISP and read the forums that many of them provide for new ideas and facilities. You'll be glad you did.

Page 276

*This page intentionally left blank.*

Page 277

## **14
Using Perl with Databases**

You have learned how, using Perl, you can collect data from users. You know how to store data in files and how to retrieve it. You know how to use Perl to respond to people who visit your Web site using e-mail. Now you are going to use Perl to store your data in a much more powerful way, by using relational databases.

Essentially, a *database* is almost any store of related data. For example, a filing cabinet is a database. But generally these days, what we really mean is an electronic database.

In this chapter you will learn how to:

![Image](content/d938f552af65a53b177029c39d905885.gif) Add MS Access databases to your Web site

![Image](content/d938f552af65a53b177029c39d905885.gif) Read, add, update, and delete records from a database using ADO

![Image](content/d938f552af65a53b177029c39d905885.gif) Read, add, update, and delete records from a database using DBI

Page 278

### **Access 97 and Relational Databases**

Access 97 is a database package that includes sufficient code to enable the user to create complete standalone applications using forms, SQL, and so on. However, in this chapter you are only interested in using the database engine itself. There are many other database systems that are as good or better, such as MySQL, PostgreSQL, and SQL Server, but Microsoft Access is widely used and available to many users, so I'll use it for the examples in this chapter.

| **NOTE** |
| You can also use Access 2000 for the exercises in this chapter. |

Access 97 is a *relational* database system. A relational database allows the data structures to be defined or described. The data is organized into tables. A *table* is a collection of identically organized records and each record, or row, in a table contains the same *fields*, forming columns of that field. One or more fields may be designated as *keys*, allowing searches for specific values to be speeded up.

For the purposes of this chapter, you will learn how to write the scripts that would be the basis of building a simple address book. For simplicity, the HTML forms will be left out and values to enter into the database you are going to build will be hard-coded into the Perl code. Obviously this is not a practical arrangement, but you already know how to get data back from a form (if you have forgotten, refer to Chapter 11).

Right now, concentrate on learning the techniques and code necessary to manipulate a simple address book database.

#### **The Database Design**

This will be a simple database that will be easy to implement in Access 97\. The data items you are going to use are given in Table 14.1, along with some typical test data that you might want to enter to test your code.

Page 279

| **TABLE 14.1 Database Items and Test Data** |
| **ID** | **First name** | **Last name** | **Address** |
| 1 | Joe | Bloggs | 14 High Street |
| 2 | Fred | Smith | 1 Sun Street |
| 3 | Jane | Doe | 4 Love Lane |
| 4 | Angus | McCoatup | 17 Lake Close |

Note the ID column. This will not be used in this chapter, but you will have a use for it when you expand this simple example into the Contact Database case study in Chapter 17\. Briefly, the ID field (or whatever you decide to call it) is a unique reference to each record (or row) in the database. This is needed, as certain operations on the database need to know precisely to which record you are referring. For example, if you had to delete a record from the database, a unique ID would ensure that the correct record and only the correct record is deleted. This is much better than a system where, for example, if you tried to delete a record for someone by the name of Smith, the database wouldn't know which one you meant and so would probably delete them all. Of course, there are times when you want to do something like that, but often you want to pluck out a certain record, and that is when the ID field, a unique key, is so useful.

Another consideration of databases is that of *data types*. Not all data is text data. There are date and time fields (notorious for creating problems), Boolean fields (which are used as flags and contain values that signify yes or no, on or off, 1 or 0, or True or False), and memo fields (which are able to hold large amounts of text).

Finally, there are *rules* and *default values*. An example of a rule might be ''allow zero length strings." Default values are used to fill in a field with a value in the absence of a value coming back from a form.

Databases can be very complex. You can have a large number of tables, many of which link to each other through a system of foreign keys so that one table can do a lookup on another. This sort of database, and the complex SQL to go with it, are beyond the scope of this book, but as your experience and confidence in building simple applications grows, you will want to extend your knowledge in this area.

Page 280

#### **Creating a Database in Access 97**

Let's build a database. In this section I'll run through the basics of creating a database table that you can use in your Web site application.

To build your first database table, do the following:

**1.** Start Microsoft Access 97\. A dialog box will open, offering to let you open a blank database, use the Database Wizard, or to open an existing database.

![Image](content/2538638d851c02e3ac16a455472f60c3.gif)

![Image](content/cc44681624cf890ed75bd3a778cd4602.gif)

Page 281

![Image](content/92431576176d39e1e32e33277b9f733d.gif)

![Image](content/d46f09df364b7db6fc271b95ee39c4ba.gif)

Page 282

![Image](content/2777da9623031135b2b2ed06a3fa392c.gif)

![Image](content/10e3bb564ead722d3981c7e52072a2ef.gif)

Page 283

![Image](content/cbbdd1256d4173163bf884e993e6003a.gif)

![Image](content/b423caa38bc4e102040cc549befcc9b1.gif)

Page 284

![Image](content/befe14d7227c7aaba0da13df3963aaa8.gif)

![Image](content/1e9229bbb96438e1d47ccd9b111ce138.gif)

Page 285

![Image](content/1a267787ac7bd6a52fb98439aae0cb6f.gif)

![Image](content/3064a7c0c8f378dddf206d6cd92a1f32.gif)

**16.** Click into the next firstname field and enter another name. Complete the other two fields as you did for the first one, but with different names and addresses.

**17.** Close the database Table dialog box and then close Access 97.

Page 286

### **Creating a Data Source Name (DSN)**

Now you have a database with some data in it; soon you will write a Perl program to read the records from the data. Before you do that, however, you have one more thing to do. You need to create a Data Source Name (DSN). To do that, follow these simple steps:

![Image](content/218d6445bd611e963c73a803e10a0515.gif)

![Image](content/fdbec3b8cfcbbbf6478a63de98e729b7.gif)

Page 287

![Image](content/1176bf950bb2f1e0ed16d0e1e791c202.gif)

![Image](content/46548d5fe37b72621960675e6d0a7ee4.gif)

The ODBC Microsoft Access Setup dialog box will open.

Page 288

![Image](content/2391be38bf73598e9700dbd18738fb7d.gif)

| **NOTE** |
| The Description field is just for documentation; leave it blank or enter some text to remind you what this database is for. |

![Image](content/2f9fe8a4f30375d467b97cbe70cb8dd1.gif)

Page 289

![Image](content/a68110f768572a7a3b6d974ce36385cd.gif)

**12.** Close the Control Panel and My Computer.

### **Reading Records from a Database Using ADO**

In this chapter you are going to learn two methods of using databases with Perl—using OLE (Object Linking and Embedding) database access, and the Perl DBI method. The first method is often referred to as ActiveX Data Objects, or ADO. In this section you will learn how to select records from a relational database using ADO and SQL (Structured Query Language, the language used to select records from the database, write records to it, and so on). An in-depth discussion on SQL is beyond the scope of this book, but you will learn sufficient SQL here to be able to perform the most common database functions—read, write, delete, and so on.

Page 290

**1.** Open your editor and start a new program.

#!c:/perl/bin

![Image](content/6259ed7ec1934d40400f10b74bc16f76.gif)

| **NOTE** |
| A *recordset* is a temporary table containing the records that are returned from your database SQL query. |

Page 291

![Image](content/8613995acc8a34a97a2b93a37393f1af.gif)

| **NOTE** |
| This statement means: Select all the columns from a table whose name is held in the variable $table. That is, * means ''all columns." You could instead simply name all the fields you want returned from the query, like this: |
| $sql = "SELECT firstname, lastname, address FROM $table"; |
| You can also add a WHERE clause, which filters the records, like this: |
| $sql = "SELECT * FROM $table WHERE lastname= 'Bate'"; |
| Finally, you can change the order of the records by using the ORDER BY clause, like this: |
| $sql = "SELECT * FROM $table ORDER BY lastname"; |

Page 292

![Image](content/c99716efaa2dd777609b582b35223b31.gif)

| **NOTE** |
| The 1, 1 is an advanced feature that controls the way in which the records are read using cursors (you can have different cursors for reading and writing to database tables) and LockTypes (as they are called in ADO parlance), which determine what kind of locking should be used for different purposes. These are advanced features that we will not delve into here; for now, just code them as they are. |

Page 293

![Image](content/cd78771fa4614a6af4c30ab2a6292dbf.gif)

**18.** Save your program as 14-01.pl in your scripts folder.

![Image](content/561ca2dd1523c6a066069d462a6857e4.gif)

If you don't get results like this, check the code and try again.

Page 294

### **Adding Records to a Database with ADO**

The code for adding a record to the database is even simpler than that in the last example.

**1.** Open a new program in your editor, and again bring in the WIN32::OLE modules.

#!c:/perl/bin use Win32::OLE; use Win32::OLE::Const 'Microsoft ActiveX Data Objects';

![Image](content/ec1d1565f14fc6d52989bf90ace616c0.gif)

Page 295

![Image](content/9139ba1380c006c21390a0ef5b068422.gif)

**8.** Save your program as 14-02.pl.

![Image](content/ccbe4f327e78c451b10ea4feec66a151.gif)

Page 296

![Image](content/d13660c8dbb2088f8912a33352f9c62c.gif)

Next, you are now going to learn how to update a record in a table.

### **Updating a Record in a Database Table Using ADO**

This is almost identical to the previous example, except that the SQL is slightly different, as you would expect.

**1.** Re-open your 14-02.pl program.

![Image](content/1da5df669273b9e48de5c90ddbd640bf.gif)

**4.** Save your program as 14-03.pl.

Page 297

![Image](content/0709de0a4ae4df88acbd85b7337d8759.gif)

![Image](content/c308cb176a6c6788708eb589eb9bc00c.gif)

All you need to know now is how to delete a record from the database table.

### **Deleting a Record from a Database Table with ADO**

Once again, this is just a simple change to the programs SQL.

Page 298

**1.** Re-open your previous program.

![Image](content/30ba46e2676431fe4c3d9495f114de8b.gif)

**4.** Save your program as 14-04.pl in your scripts folder.

![Image](content/f597835225b439d05e2ad9d171461e1d.gif)

Page 299

![Image](content/595b0d76b9dbfdf4293e580d9be01783.gif)

So there you have it. You are now able to carry out all of the CRUD (Create, Read, Update, and Delete) operations on a database table.

### **Perl DBI**

DBI, Perl's database interface, has been around for some time. It is used extensively on UNIX-type platforms but also works on Windows platforms, so it is worth covering that briefly here.

#### **Installing DBI**

Before you can use DBI, you must install the DBI module in Perl. To do this on Windows, follow these simple instructions. Of course, your ISP may already have DBI installed for you.

Page 300

![Image](content/5995cebc790b48db91a043a021e69d1e.gif)

The process may take several minutes, and when it completes, you will see a list of all the modules currently installed.

Any time you want to confirm what modules you have installed, simply enter the command **ppm query** at an MS-DOS command line (or at the command prompt on a UNIX machine).

#### **Reading Database Tables Using DBI**

Okay, now let's look at how you can use DBI. You will run through the same set of exercises as you did with ADO, but using DBI instead.

![Image](content/6ee5ba8565868e7df5fd1473d7ff10c4.gif)

Page 301

This operation returns a handle that is used to reference the database in future operations in your program. The connect string specifies the database is being accessed via DBI, that it is an ODBC database (you can substitute this for any database type supported by DBI), and finally, that the name of the database is address.

![Image](content/ab7a565964515c2ce713b0b370d568c9.gif)

Page 302

![Image](content/0e2bb7c3785e5b7c7da60c947a85fa3a.gif)

**11.** Save your program as 14-05.pl.

![Image](content/01fd785c93d2f3d0c75bb2e237cc2dba.gif)

#### **Writing to Database Tables Using DBI**

The method of writing to a database with DBI is very similar to the previous example.

Page 303

![Image](content/257554955c2f13c57db381ea62d69b1c.gif)

**2.** Now remove the loop and read through the records in the previous example.

![Image](content/ce352eceb0c94411b1bdd2e65088c8f7.gif)

Page 304

![Image](content/b2e3fae1d3287679257fa62dcac2d34a.gif)

| **TIP** |
| If you do not always see what you expect in the Web browser, try clicking the Refresh button. |

#### **Updating Database Tables Using DBI**

The following example of updating database tables using DBI is identical to the previous example, except for the SQL statement.

**1.** Open your previous program (14-06.pl).

![Image](content/686d15ed14e125110baefc67edc0af4d.gif)

**3.** Save your program as 14-07.pl.

Page 305

![Image](content/8a498fe1fa160d10e7fb9f27fb3a4d6d.gif)

![Image](content/b92a000bc73a309066ce43adfb9a881e.gif)

Now, if you're still with me, let's take a look at deleting records with DBI.

#### **Deleting Records from Database Tables Using DBI**

Once again, the code to remove a record from the database is identical to that used in the previous example.

Page 306

**1.** Re-open 14-07.pl.

![Image](content/9b636a0778b5fad0ca83df30722645d1.gif)

**3.** Save your program as 14-08.pl.

![Image](content/85206d4fcf307f203c9c93d48525f44f.gif)

Page 307

![Image](content/30d97c4b50d7b3ef74d44ecf980a4452.gif)

And that's it. You now know the basics of manipulating databases through two possible methods, ADO and DBI.

You will see more examples of practical code in the case study in Chapter 17.

Page 308

*This page intentionally left blank.*

Page 309

## **15
Another Diversion: JavaScript**

You know how to create a form and how to get the data sent by the form into your Perl program. But what if the data entered by the user is invalid? You can get your Perl program to return the form with an indication of what the problem is, but this is an inefficient way of checking the form data because each error discovered means that the page is re-sent over and over until the user has corrected all of his mistakes. Wouldn't it be nice if you knew (as far as possible) that the data being received into your Perl program was okay?

This is where JavaScript comes in. JavaScript can check your form data at the client (that is, within your Web page) and can prevent your form being submitted until all the errors in the entered data have been corrected. This means that you get instant notification of any errors and there is (hopefully) only one trip across the Internet for your form.

In this chapter you will learn about:

![Image](content/d938f552af65a53b177029c39d905885.gif) Object orientation

![Image](content/d938f552af65a53b177029c39d905885.gif) JavaScript syntax

![Image](content/d938f552af65a53b177029c39d905885.gif) JavaScript variables

![Image](content/d938f552af65a53b177029c39d905885.gif) Using JavaScript to validate form data

Page 310

### **A Few Notes about JavaScript**

JavaScript is an interpreted, object-oriented programming language developed for use in HTML Web pages (that is, client-side programming). Although it can also be used as a server-side programming language, we are not going to discuss that aspect of JavaScript here.

JavaScript is similar in its syntax to Java and C++, and behaves in much the same way. However, JavaScript is not the same as Java. Java enables you to build full-blown, stand-alone applications; JavaScript does not. It simply reacts with *objects* within a Web page.

### **Object Orientation**

Object orientation attempts to bring the real world into programming. Real world objects (I'll give an example of such an object soon) are represented as software objects. In theory, object-oriented programs are simpler, more reliable, and more closely model their real-world subjects.

Object orientation should also be more efficient in terms of software creation, as you do not, in theory, have to keep re-writing things. Objects are described using what is known as a *class*. This class contains all the definitions of the data that are relevant to that object and all of the functions that operate upon that data. Classes can be reused and modified to suit a particular purpose without having to re-write things from scratch. This gives rise to a property known as *inheritance*.

An example of a real-world object is a bank account. You could have a class describing such an account. The data for a bank account would include

• Account number

• Account name

• Sort node

• Balance

These items describe the data contained within the description of the class.

Page 311

Having decided upon the data that might be contained within a class, you now need to be able to manipulate these data items to read, write, update, and delete them. That is, to use the account you need to be able to

• Open the account

• Add funds

• Debit funds

• Close the account

In a class definition you would write methods (know as functions in normal programming terms) to deal with each of these actions.

With the definition of the object (in the form of a class) you can now create the bank account object itself; in fact you can create lots of them. Where ordinary languages might have arrays of integers and so on, in object-oriented languages you can have arrays of objects too. This is very powerful indeed. Imagine trying to keep track of loads of accounts in a normal procedural language.

One of the main points of object orientation is that the data within an object can be set up to be accessed only via that object's methods. This helps to ensure the integrity of the data and reduces bugs. This feature is known as *data hiding*.

Creating an object from the class definition is referred to as *instantiation*.

A form of notation has been developed to help you to describe the act of accessing the methods within an object. This is sometimes referred to as *dot notation*. For example, if you want to access the add_funds() method of an object you can write it as

account.add_funds( )

Note the dot between account and add_funds().

If you are with me so far, here is another twist.

Page 312

Having created your account class, you can now slightly change the purpose of the account. For example, you can have current accounts and savings accounts. The basic information that defines an account (account number, balance, and so on) can be held in a super class. Then other classes can inherit from this class and provide the more specific information that describes a particular type of account. This is an illustration of the potential flexibility of object orientation. This use of inheritance is an example of the much-discussed code re-use advantage of object-oriented languages.

Let's go for a silly example, and create a class called Animal.

What data can you hold about an animal?

Carnivore (true/false) Number of legs (integer)

What methods (functions) could you have? Most animals make a sound of some sort, so you could have a method called

talk( );

This gives a basic animal class. You can inherit from this class and specialize into more specific subclasses. Your subclasses can inherit the basic methods from the superclass, or higher level class. So you can create a class for a cat and one for a dog, both based on the animal superclass but with their own specializations that describe the differences from the basic animal class.

Now calling the talk() method for each object you create, such as dog.talk(), cat.talk(), causes an appropriate response from each object—the dog will bark and the cat will meow.

This ability to produce an equivalent but appropriate response is known as *polymorphism*. Perhaps you can begin to see the possible uses of such behavior.

An in-depth discussion about all the aspects of object orientation is beyond the scope of this book, but I hope that you can begin to see there are possible advantages of object orientation over conventional procedural programming. Now let's turn back to discussing JavaScript.

Page 313

### **Elements of JavaScript**

JavaScript uses objects. The HTML page that you might be on at any particular time is referred to as the *document object*. There are many other objects as well, such as the window object, the form object, the form element object (containing the <INPUT TYPE=…> elements), and the button object.

Many of these objects produce *events*, that is, a result of the user's action or a change in the state of some element on a page or in a window. For example, clicking a button on a form triggers the onClick event. When you roll your mouse over an image you trigger the onMouseOver event. You can attach JavaScript code to these events to cause things to happen.

As in other object-oriented languages, you use methods to cause something to happen to an object. Here is a simple example. If you want to move the cursor into a text field called Surname on a form called MyForm1 you would write

document.MyForm1.Surname.focus();

Note the dot notation again. This means that the document object contains a form object called MyForm1, and object MyForm1 contains an object called Surname. The object called Surname has a method within it called Focus(), which is what is being called, or executed, in the example. So you have objects contained within objects, a bit like a Russian nesting doll.

Also notice the parentheses at the end of the method name. These show that this is a method, but they are also used to pass parameters to methods that accept them. In our earlier bank account example, you might want to add funds. When you use the method to do this, you can write

account1.addfunds(500.00)

This means (in this example) you are adding $500.00 to account1.

Much of the time, the parentheses following a method name are empty. Sometimes, as in the previous example, the parentheses are used to pass information to the method.

Page 314

So now you have an idea of how objects are used; you will start to build upon this with some examples. But before you do that, you must learn how to incorporate JavaScript into your Web pages.

### **Where Do You Put Your JavaScript?**

Now you have some idea of what JavaScript is all about, it is time to look at where to put it. To tell the Web browser that you are using any kind of script, you have to use the <SCRIPT> tag. This is a general HTML tag and not anything to do with JavaScript itself. It is used to point out that some kind of script follows. The default script language (for IE5 at least) is VBScript. So, if you want to use JavaScript, you should use

<SCRIPT LANGUAGE=''JavaScript">

If you don't specify the language, the browser is usually clever enough to recognize which language you are using, but don't assume anything.

</SCRIPT> is used to end all script sections, whether they are VBScript, JavaScript, or another language.

Note also that there are several versions of JavaScript, so you might see:

<SCRIPT LANGUAGE="JavaScript1.0">

or

<SCRIPT LANGUAGE="JavaScript1.1">

or

<SCRIPT LANGUAGE="JavaScript1.2">

These versions offer more updated functionality, and you will need to become more aware of the differences as you become more proficient at using JavaScript and want to extend the complexity of your scripts.

Page 315

Another thing to remember is that you can place script either in the <BODY> of an HTML document or in the <HEAD>.

Generally, you use JavaScript in the body of a document if you want it to execute as the page loads. JavaScript placed in the head of a document is generally used as it is required, or *called*, as the action of executing it is called. The script in the head usually takes the form of *functions* (discrete sections of code), each function having a specific purpose.

### **More JavaScript Syntax**

JavaScript uses code blocks all over the place. These are lines of code enclosed in braces, very much like Perl.

For example:

{ Document.write (''Hello There!"); Alert("This is a pop-up box!"); }

It is unusual to see a block of code like this on its own. Often it is the body of a function, as in this example:

![Image](content/5f3df98b1f0efd945d63b2f3b08440f2.gif)

Page 316

![Image](content/6db65e2846138e0680f876cd592d7e06.gif)

Page 317

![Image](content/8ed0ca1bdd3f806d88a3c5a9af547f68.gif)

| **NOTE** |
| Normally, you would save this either in a folder under your wwwroot folder, or you would upload it to your hosting company to use on the Internet and you would then access it using the appropriate URL as you do when you are connecting to a normal Web site. 
If you saved this page into a folder called *test* at the top level of your ISP Web space, you would enter something like

http://www.mydomainname.com/test/15-01.htm |

Page 318

**14.** Save it as 15-01.htm.

**15.** Use the preview option in your editor to test your JavaScript, or double-click the 15-01.htm file and it will open in your browser. Either way, you will see the button you created.

![Image](content/42bdee57336b49ee111c30c80b890d9e.gif)

![Image](content/a8763f8063033c6ae27d75c43546992d.gif)

This is a full example of a very simple JavaScript function, showing the use of braces, {}, around the code. It also shows where functions are placed and one method of calling a function (onClick=).

Just to remind you, the <!--- and ---> tags are normally used to embrace HTML comments (text that is designed to be informative to humans but is ignored by the browser) and therefore anything inside them is ignored. Modern browsers

Page 319

recognize that there is script inside them and therefore execute it. Older browsers (that do not understand JavaScript) ignore the JavaScript code; this prevents unnecessary error messages. Of course, the JavaScript code won't work on an older browser, either. The opening HTML comment needs a less than symbol (<) followed by at least two dashes like this:

<!--

It should end with at least two dashes followed by a greater than symbol (>), like this:

-->

Note that case is very important when specifying keywords in JavaScript—function is a keyword, *Function* isn't.

### **JavaScript Variables**

As do all other languages, JavaScript uses variables to store information. Variables can be created on-the-fly as and when you need them, but it is a good idea to create them at the beginning of your script so that it is easier to follow, and so you know where to look for them. To create a variable you use the var keyword.

var age; var name;

And so on.

To assign a value to a variable you use the assignment operator, =.

age = 17; name = ''fred";

Most JavaScript statements end with a semicolon. JavaScript, like most modern languages, is *free format*, that is, it can be split over many lines if desired, usually to aid readability. It uses the semicolon to indicate the end of a statement, a form of notation borrowed from C++ and Java (and of course, Perl) languages.

Page 320

Other things you will want to do with JavaScript include

• Add numbers together

• Subtract

• Multiply

• Divide

You might add the values of a couple of variables like this:

firstNumber = 13; secondNumber = 23; ressultOne = firstNumber + secondNumber;

Note that the standard convention is to capitalize the second word in a variable. This makes the code easier to read and reduces mistakes. It is up to you whether to follow this convention, but doing so will make it easier for other people following along behind you to update your code.

Subtraction, multiplication, and division are performed in a similar manner to the previous example, using the -, *, and / operators, respectively.

There are many other things that you might want to do; for example, you might want to get the length of a character string.

stringVar = ''fred"; sLength = stringVar.length;

There are no parentheses after length because this is not a method, but an attribute of the string object, stringVar.

To test a value you use the equals operator, = = (remember that you already used the = operator to assign a value to a variable).

So you would say

if(numVar = = 5) {

Page 321

Other operators are

• > (greater than)

• < (less than)

• <= (less than or equal to)

You can do many hundreds of other things too with JavaScript, including opening new windows, jumping to different Web pages, opening dialog boxes, and so on. JavaScript is a large, complex, and immensely powerful language.

You will learn more features of the language with experience, but now we have to be ruthless and stick to things that will help you with your Web applications.

### **Your First Form Validation JavaScript Function**

One of the most interesting and useful things you can do with JavaScript is client-side validation. But before we go any further, let us briefly re-visit the object discussion. All things in JavaScript are regarded as objects. An HTML page is called a *document object*. As you learned a short time ago, a form is another object that lives inside a document and has a name by which you can refer to it. Therefore, you refer to a form that has a NAME=''addrecord" attribute like this.

document.addrecord

Note the dot!

This is not a complete statement yet, but it means "go to the form addrecord contained within the document."

Any fields in the form are referred to in a similar way. So, if you have a field called surname, like this:

<INPUT TYPE=TEXT NAME="surname">

Page 322

Then you would refer to it like this:

document.addrecord.surname

This gets you to the field object inside the form object, which is inside the document object. Now you have reached the field object. But this object has many attributes, such as length, value, and so on. So, to access the value of your field, you refer to the value of the field like this:

document.addrecord.surname.value

Now, you can have a look at what is in the field. To do this, use the JavaScript if statement. If you want to check that the field is empty, you can do this:

if (document.addrecord.surname.value == ''") { Do something ... Do something else ... } back to the rest of the code that doesn't care if the field is empty or not …

As you can see, the braces are used here again, and now you can see why. They limit the scope of the if statement. In other words, only the code inside the braces is dependent upon the condition in the if statement.

Also, note that you use two equal signs (==) to check for equality. A single = in JavaScript is used to assign a value to a variable. Other tests are:

• != not equal to

• > greater than

• < less than

• <= less than or equal to

• >= greater than or equal to

You can have multiple conditions in your if statement. These conditions can be ANDed or ORed together (or a combination of the two) by using the JavaScript AND operator, which is the double ampersand, &&, and the JavaScript OR operator, which is the double pipe, ||.

Page 323

So, a JavaScript if statement might look like this:

if ((document.formname.department.value = = ''HR" || document.formname.expenses.value != 0) && (document.formname.jobtitle.value = = "Manager")) {

The parentheses force conditions to be grouped together in the way you intend rather than the way JavaScript decides if you leave the inner parentheses out. There are rules about operator precedence that define in what order conditions will be tested. If you do not want to learn them, or you are at all unsure as to how your conditions will be interpreted, use parentheses to group them together.

#### **Submitting Forms Using JavaScript**

You can submit your form to a server-side script or program (such as your Perl programs) from within a JavaScript function. This can be done by using the submit() method of the form object, like this:

document.addrecord.submit( );

#### **Conditional Form Submission**

Now you can check the value contained within fields in your form and you can submit your form. But there is much more to learn yet.

How do you check for the possibility that a field is blank? You have met the if statement briefly; the full syntax for the if statement is

If (condition) { do something[ …] do something else[ …] } else { do some other stuff[ …] do some more other stuff![ …] }

Page 324

So, putting it all together, try the following example and see what you get.

**1.** First, open a new HTML page in your editor.

<HTML> <HEAD> <TITLE>JavaScript Example</TITLE>

![Image](content/8a5e90e8960a3fc67d49f9c80ba3e573.gif)

**6.** The if statement has its own code block, so you will need to open a new brace.

    {

Page 325

![Image](content/2f5bcb566289b8965111d68a16e232f5.gif)

Page 326

![Image](content/5e2fea19e01f99bdfacd3d8b6f4c7f42.gif)

Page 327

![Image](content/66e2ea173f3e10e2ec9b1b158ef81d4b.gif)

| **NOTE** |
| TYPE=BUTTON is used rather than TYPE=SUBMIT, preventing the form contents being immediately sent to the server. Instead, you can invoke your JavaScript function which can check that you have completed any required fields, displaying any error messages where appropriate, or, if there are no errors, can submit your form. |

**21.** Save your page as 15-02.htm and check it to make sure it works.

Page 328

![Image](content/9e04b26f41445962c02b34b1976911f4.gif)

| **NOTE** |
| If you add a name in the surname field, then as has been said, you will see nothing happen except perhaps the page refresh and the surname field will empty. |

There is one other method that makes the form more useful and friendly, especially on a form with lots of fields. You can direct the user back to a field in error by using the focus() JavaScript method.

![Image](content/d33b9db6ffab4b93be2bd2ef6547efa4.gif)

**2.** Save your page as 15-03.htm and make sure it works.

Page 329

![Image](content/7ece97f997bbd332bd4d3fb9b2047816.gif)

#### **More JavaScript Functions**

What if you wanted to check that what the user typed was a number? JavaScript has a function called isNaN() which means ''is not a number." This function returns a Boolean result (True or False), True being returned if the number sent to it is not a number.

You use isNaN like this:

if(isNaN(variable) {

Page 330

![Image](content/9314c0ad05cde4a53dcc0f28239f2aeb.gif)

**3.** Save the page as 15-04.htm.

![Image](content/59404ea124d337100720d8f6d194b02c.gif)

Page 331

![Image](content/5c0acb28d8ecd96e00a032f3a784ac38.gif)

What if you want to check two fields, such as age and surname? You can put both of the checks in one function, which will work fine. But what if the form contains 15 or 20 fields? And what if there are a lot of errors?

Well, the user will get lots of error messages, but will probably only remember the last two or three; he or she will then have to click the button again to get the rest of the errors. A better way is to check each field in turn and when you find a problem, skip the rest of the checks and display the first error message. The user then corrects that error and then when he or she clicks the button again, the next error message appears until the form is free from errors, at which point the form is submitted.

This is easy to do.

**1.** Open your HTML page again.

![Image](content/7f732100cd7e83650e46bfcb67a72297.gif)

Page 332

![Image](content/af67dc84f9ebb6fb89e5f282556b7cf5.gif)

| **NOTE** |
| Notice that the if statement says |
| If (isNAN(testVariable) && okeydokey) |
| Remember I said that any non-zero value was True? This means that the above okeydokey gets substituted by the value True. 
Follow the logic and see if you can understand how this works! |

Page 333

![Image](content/5a73d9f4183fa42aacf52203287e7b17.gif)

**9.** Save the page as 15-05.htm.

![Image](content/2e234312145c6f2604badb51ea4a7f33.gif)

Page 334

![Image](content/9046019f0d24b176c696fe119871055f.gif)

Now you know how to check for empty fields in a form and how to guide the user back to the fields that were completed incorrectly.

#### **E-mail Address Validation**

E-mail address validation is one more useful function that you might want to achieve with JavaScript. But how do you check an e-mail address? There are a few basic checks that are worth making to avoid the occasional typographic error.

A valid e-mail address would normally have the following:

• An @ symbol within the e-mail address string.

• Some characters before the @ symbol.

• Some text after the @ symbol.

• A period amongst the characters after the @ symbol.

If these checks do not reveal a problem, the address is probably okay.

Page 335

![Image](content/18096b64dd94999e9087e95dd9650603.gif)

![Image](content/a1b984c5ea7803d956e0e6e3f1cbc52e.gif)

Page 336

![Image](content/9b6acf8800678d9c4c9b7b291a67f5e0.gif)

Page 337

![Image](content/b829bfae91b5621b5741faf23d8a4723.gif)

![Image](content/afc0a2672e3d7ec485269814f9ea9011.gif)

Page 338

![Image](content/2a17b55978fa7b9e1be5bc919a97eb53.gif)

Page 339

![Image](content/886babc456cff6e5bd749b1e537a18c5.gif)

![Image](content/85119a90cf15e1465289815d37049dbd.gif)

There are many books, Web sites, and courses set up to teach JavaScript. I urge you to look deeper into JavaScript, as it is a really useful tool that can save you lots of server-side work and time.

Page 340

*This page intentionally left blank.*

Page 341

## **16
The CGI.pm Module**

In this book, you have so far learned (amongst other things) about Perl, HTML, and how to create HTML from Perl. This has been useful, as learning about how to create HTML on-the-fly from Perl has reinforced the HTML that you have learned. In this chapter you'll learn a little about a module called CGI.pm, which simplifies the creation of HTML from Perl.

Specifically, you'll learn:

![Image](content/d938f552af65a53b177029c39d905885.gif) What CGI.pm does

![Image](content/d938f552af65a53b177029c39d905885.gif) How to start and end an HTML page with CGI.pm

![Image](content/d938f552af65a53b177029c39d905885.gif) How to use forms with CGIpm

![Image](content/d938f552af65a53b177029c39d905885.gif) How to use GGI.pm in object-oriented mode

Page 342

### **What's the Idea Behind the CGI.pm Module?**

The CGI.pm module attempts to simplify and formalize the functions used in CGI applications. Some of the actions that need to be taken in the execution of CGI programs are not intuitive, and the reason for the necessity of some of them is lost in the mists of time—way back in the 1990s!

Perl is a powerful language and yet it still has to perform some pretty obscure gymnastics to do some things that should be fairly easy. The truth is that the existing technologies have moved on and some new technologies have arrived, but in many cases, we still have fairly primitive mechanisms available to us to access these technologies.

You have seen how tedious it is to have to send headers (print ''Content-type: text/html \n\n";) and how cumbersome it can be to get data back from forms. The CGI.pm module is intended to simplify all of this and provide an interface into the CGI functions and to enable you to create HTML forms and back-end CGI scripts much more quickly and easily. There are many functions available in the CGI.pm module, and in this chapter you are going to learn some of the most commonly used.

To use the CGI.pm functions, you must import the CGI.pm module methods. You do this by using the following statement; this statement makes the functions contained within the CGI.pm module available within your program:

use CGI qw(:standard);

The qw is simply a way of wrapping :standard in quotes.

You can also use

use CGI ':standard';

The ':standard' refers to the standard set of functions, so that you can use a less long-winded way of referring to functions.

The best way to learn some of theses CGI.pm functions quickly is by example, so let's get right on with it.

Page 343

### **Starting and Ending an HTML Page with CGI.pm**

Starting and ending a page using conventional HTML is not difficult. You can use the Perl print statement to create the HTML line by line (a bit tedious) or you can use the document as described in Appendix A, ''More Perl Functions," or as demonstrated in Chapter 17, "Case Study: A Contact Database."

But try this:

**1.** Open your editor and start a new Perl program.

#!c:/perl/bin

![Image](content/cd2226193b2b246888e7ce17b4e2c1b0.gif)

Page 344

![Image](content/35d8ba303d482b2964542575d623af5c.gif)

| **NOTE** |
| This is the same as using <H1>Welcome to Perl Fast and Easy: the CGI.pm module!</H1> |

| **NOTE** |
| This is like using </BODY>
</HTML> |

**9.** Save your program as 16-01.pl in your scripts folder.

Page 345

![Image](content/e0526f31b881e938dddd95a6a9bce0b0.gif)

That's a bit neater than standard HTML, isn't it?

Some things don't appear to be any easier using the CGI.pm functions than using the print function and the usual HTML. Here is an example. To print a horizontal rule using CGI.pm, you would do this:

print hr( );

Not difficult, but not exactly shorter. Of course, in these days of modern programming there is much to be said for consistency, and if you are using the CGI.pm module, perhaps you might want to use it throughout your program to avoid confusing others who come along after you. But to be honest, mixing and matching of standard Perl with CGI.pm stuff allows you to mix useful features of the CGI.pm module with other standard features of Perl that you are already familiar with.

Other similar ''unpaired tags" such as the <BR> and the <P> tags are treated in a similar way. Try the short program on the next page to demonstrate the use of some other tags via CGI.pm.

Page 346

![Image](content/673b05f5a00ba13fd29752b1e3bc4fde.gif)

| **NOTE** |
| The ordered list is preceded by the CGI.pm equivalent of the <h3>Languages</h3> header in HTML. |

Page 347

**6.** Save this program as 16-02.pl in your script folder.

![Image](content/3357608dd847f426b734d603eea48d43.gif)

![Image](content/edcd1d0d931e32ae084638ec65db3b67.gif)

Let's take a look at a few more things that CGI.pm can do.

Page 348

### **Forms and CGI.pm**

CGI.pm can also build forms. You can generate the HTML on-the-fly to create forms, including all the usual elements, such as select boxes, text areas, and a submit button. Try the following program, which has many of the usual elements you might expect to find in a form. I'll leave you to judge how easy it is to use.

The page you are going to create here is going to call itself. This form will also remember the state or values of all the fields on each execution of the form. You will see what I mean in a moment.

**1.** Open a new program in your editor.

#!c:/perl/bin

![Image](content/e72d44c096ce583c799a00d4b2e8e938.gif)

Page 349

![Image](content/11ac64b67168d14bf826b70b451c8415.gif)

| **NOTE** |
| Note the parameters: Default is any text you want the field to have when the form is displayed, the 50 is the length of the field. 
This is the same as <INPUT TYPE=''TEXT" ., NAME="surname" VALUE="Default" SIZE="50"> |

Note the parameters for the name of the check box group, and the value for each check box.

Page 350

![Image](content/f8a8fe4f7ee9dbbe08b90af4196f7094.gif)

**13.** Save the script as 16-03.pl.

![Image](content/36c2454c5be37b62e56a7ad5a3b352b0.gif)

Page 351

![Image](content/633a2d59f3931f90f3d34546e5722fbb.gif)

Before you go any further, a word of warning: There are a few cases that may cause confusion, the most common being that if you use the tr() function to try to create a table row (yes CGI.pm handles tables, too) you will end up invoking the Perl translate function. A similar conflict occurs with select (as in select lists). To be honest, you are better off creating tables using the conventional HTML; then you won't encounter the conflicts.

Incidentally, if I've left you wondering, you can generate a table like this:

print table(Tr( td('Some Data'), td('Some More Data'), td('Even More Data')));

which will generate the normal HTML, like this:

<table><tr><td>Some Data</td> <td>Some More Data</td> <td>Even More Data</td></tr></table>

Next you'll learn something really useful, something that the CGI.pm does that really takes the hard work out of grabbing data from HTML forms.

Page 352

### **Getting Data from Forms**

Here is an area where CGI.pm really does come into its own. Getting data from forms using CGI.pm is so much easier and more intuitive for the programmer. With CGI.pm, you don't have to think about how you're going to separate the key value pairs, or how you are going to separate the form field name from its accompanying value.

Remember all that stuff you learned about getting the data from a form and having to convert characters, splitting on = and so on? Well, thanks to CGI.pm you can now dodge all that. If you are using the POST method, you can simply get at form data by using CGI.pm's param('fieldname') function.

The param() function simply returns the value of the field named in the param() function parentheses. So

myfield = param('surname');

returns the value that had been typed into a field called Surname on the sending form. Now that's useful!

Try this:

**1.** Re-open your last program in your editor.

Page 353

![Image](content/6976470ab72380f9ce5f85d517194ba0.gif)

**3.** The if statement checks to see if there are any values in the fields and displays them if there are. Which is what I mean by saying the page *calls itself* and remembers its state between executions.

**4.** Save the program as 16-04.pl.

Page 354

![Image](content/817ab9708280fa0176a372be6781da47.gif)

![Image](content/59f51d18c7317a22a483a594e3c04659.gif)

Form manipulation is a very useful area in which to use CGI.pm. In my opinion, the most useful of all! However, there is one other aspect that will interest you—the object-oriented mode of CGI.pm.

### **CGI.pm in Object-Oriented Mode**

Before we leave the subject of CGI.pm, there is a little more you should know about it. You have so far used CGI.pm in what is known as *function-oriented* mode. CGI.pm can also be used in an *object-oriented* way.

Page 355

This has a few advantages:

• If you treat CGI as a class, you can have more than one CGI object.

• You can inherit from a CGI class and modify the resulting object's behavior to suit your requirements.

• Using CGI.pm in object-oriented mode uses less memory.

• You can use parameters of tags generated by name, so you don't have to learn the positional location of a parameter; you just name it and assign a value in any order you like.

• You can save a CGI object to disk and reload it.

However, the object-oriented mode is also more verbose, so it means more typing.

Just for fun, let's do a program similar to the last program (16-04.pl) in object-oriented mode and you'll see what I mean.

**1.** Start a new program in your editor.

#!c:/perl/bin

![Image](content/6ba55fe14b589ef9c54429b680915e0e.gif)

Page 356

![Image](content/fd0a98a27364e9ed4294341a6a52dd99.gif)

Page 357

![Image](content/6b4de4b30de776a5ef5bfca8ad3b271a.gif)

**16.** Save your program as 16-05.pl.

Page 358

![Image](content/968a710cfceabd3d458e22e28c97358d.gif)

![Image](content/3e888af956d0d3834f7e90738c95f4e3.gif)

Page 359

![Image](content/f9476d9be12da19f82a684bfbd47e1ec.gif)

The significant thing about the object-oriented way of using CGI.pm is that you can have lots of independent CGI objects and handle them all separately (q2, q3 and so on). In fact, Perl itself now has an object-oriented mode, which is unfortunately beyond the scope of this book. But should you wish to learn more about it, there is lots of information at the Web sites listed in Appendix B in the back of this book.

Page 360

*This page intentionally left blank.*

Page 361

## **17
Case Study: A Contact Database**

In this chapter you are going to see how all of the things you have learned so far can be brought together to demonstrate a complete Perl database-driven application. This application is a simple contacts database. You can, of course, modify it to do any number of different jobs including the ubiquitous Guest book. I think you will find many useful things to do with the techniques used in this application.

In this chapter you will:

![Image](content/d938f552af65a53b177029c39d905885.gif) Create a home page

![Image](content/d938f552af65a53b177029c39d905885.gif) Use the listcontacts.pl program to read and list the contents of a database table

![Image](content/d938f552af65a53b177029c39d905885.gif) Use the editcontact.pl program to insert data in the database

![Image](content/d938f552af65a53b177029c39d905885.gif) Use the editcontact.pl program to load data into fields

Page 362

### **The Requirements**

What are the requirements for a contacts database application?

Very simply, you need to be able to:

• Add a new contact

• Update an existing contact

• Delete a contact

• List contacts

Yes, there are variations and refinements that can be applied, but basically this is the core requirement of any database application. Everything else is a tweak (although some of the tweaks are very useful). I will mention some tweaks that you might like to try at the end of this chapter.

You know what you want to do with the database, so what data items might you be interested in? Here is a set to begin with.

• First name

• Middle initial

• Last name

• Address (number, street, and so on)

• Town/City

• Post code/ZIP code

• Telephone number

• E-mail address

This forms the basis of a useful set of information. There are other bits of information you might want to store, and you can go back and add any extra bits you would like. Or, of course, you can change all the data and use the application for something else entirely.

Now you know what we are going to do and what we are going to do it with. It's

Page 363

time to visualize what the application should look like, and how it should behave. When I say ''look like," I don't mean aesthetically—that isn't important, and it is something you can tinker with when you're happy with your application. What I mean is how it is going to work.

A good place to start is to imagine you are the user of the new application. What would you expect to see when the application started? How do you see new records being added and how should this work? How would you navigate around the system? In short, how can you best make your application friendlier and less cumbersome?

A good starting point is draw out your ideas on paper and plan out what your application is to consist of and how it should hang together, paying attention to navigation and to a logical sequence of events.

![Image](content/ff7dab7912fd1c7fb393d4bf57f57b5a.gif)

Here is the approach I took for this simple application. I think this simple design is fairly self-explanatory. I have named the files to give you an idea of what they should be doing. The solid lines are links to the different parts of the application. The dotted lines are possible links that you might want to have to ease navigation.

Now you can start putting together your application.

### **The Home Page**

A good place to start is with the home.htm page, which is a simple HTML page to act as the home page and the menu for your application.

Page 364

The top-level page (home.htm) is nothing exciting. It is as simple an HTML page as you can get with a couple of links to the List Contacts program and the Add a New Contact Page.

**1.** Open your editor and start a new HTML page.

<html> <head>

![Image](content/e8fd965b29abfc9be90592d8179589be.gif)

Page 365

![Image](content/ef7796c3c795e4dfb36090c0714acf35.gif)

**8.** Save your page as home.htm in a suitable folder called, say, Contacts.

**9.** If you wish, open your browser and view your home.htm page.

Okay, so you have made a start on your contacts database application. You will also want a Perl script to display the contacts from your database as a list. Let's do that next.

### **The listcontacts.pl Program**

The listcontacts.pl program simply reads the contents of the database table and lists the first name, last name, and town fields for each record. (A view of the database design is at the end of this chapter). In this program, ADO is being used to connect with the Access database. There should be no surprises here, but if something doesn't make sense to you, refer to Chapter 14, ''Databases."

Page 366

**1.** Open your editor and start a new Perl program.

#!c:/perl/bin

![Image](content/b7a0362508eceee3461c5e17cf59e656.gif)

Page 367

![Image](content/f33738f91d09e9e0784996f44815f83b.gif)

| **NOTE** |
| Note that you are using the SELECT * FROM $table type of SQL statement, meaning get all of the columns. This is fine for a small program like this, but you are actually bringing back columns that you do not need and therefore the database and the network are doing unnecessary work. It keeps things simple for this example, but a better SQL statement would be: |
| $sql = ''SELECT id, firstname, lastname, town FROM $table"; |

Page 368

![Image](content/afc177cd2dee2d70c6cde598ac3dc095.gif)

Page 369

![Image](content/efc70583ba21a5f415da0acac9328aee.gif)

**8.** Just to tidy things up, close the <body> and <html> tags.

</body> </html>

**9.** Save your program as listcontacts.pl in your scripts folder.

That completes the listcontacts.pl program. Of course, you cannot run it yet, as you do not have a database to run it against! Next you are going to create the HTML form to add data to your database and a Perl script to actually insert the data into the database table.

### **addcontact.htm**

This is a simple HTML form that sends data to the insertrec.pl program. You are also going to check, using JavaScript, if the user has entered the data he or she should have and then give them an appropriate message if they did not.

Page 370

![Image](content/d52879be9125d6adba06546558d5b0bd.gif)

<Script Language=JavaScript> function checkfields( ) { var okeydokey; okeydokey = 1; if(document.addrec.firstname.value == ''") { alert("You have not entered the contact's First Name"); okeydokey = 0; document.addrec.firstname.focus( ); } if(document.addrec.lastname.value == "" && okeydokey) { alert("You have not entered the contact's Last Name"); okeydokey = 0; document.addrec.lastname.focus( ); } if(document.addrec.street.value == "" && okeydokey) { alert("You have not entered the contact's Street Address");

Page 371

okeydokey = 0; document.addrec.street.focus( ); } if(document.addrec.town.value == ''" && okeydokey) { alert("You have not entered the contact's Town"); okeydokey = 0; document.addrec.town.focus( ); } if(document.addrec.postcode.value == "" && okeydokey) { alert("You have not entered the contact's Zip / Post Code"); okeydokey = 0; document.addrec.postcode.focus( ); } if(document.addrec.phone.value == "" && okeydokey) { alert("You have not entered the contact's Phone No."); okeydokey = 0; document.addrec.phone.focus( ); } if(document.addrec.email.value == "" && okeydokey) { alert("You have not entered the contact's e-mail address"); okeydokey = 0; document.addrec.email.focus( ); } if(okeydokey) { document.addrec.submit( ); } } </script>

Page 372

| **NOTE** |
| Note the last part of the function. It uses the if(true) check on the okeydokey variable to decide whether or not to submit the form. If there are errors and okeydokey is False, the submit method will not be executed and the form will sit there waiting for the user to correct the errors. Each time the errors are corrected, the checkfields() function will be executed again. If all is well, the form will be submitted and your data will be sent to the Perl program that will insert the data into the database table. |

![Image](content/e45f9b093c40934404d05ae3458dbeb7.gif)

Page 373

![Image](content/28b13b95801359bb239d5cb61e959be4.gif)

Page 374

Page 375

![Image](content/49772bf3827d9000910820d864cc643e.gif)

**10.** Save your HTML page as addcontact.htm in, say, a Contacts folder beneath wwwroot.

Page 376

### **The insertrec.pl Program**

You now have your HTML form and all the data that you need to pass to the Perl program that's going to insert the data into the database; here it is going to be called insertrec.pl.

**1.** Open a new Perl program in your editor:

#!c:/perl/bin

![Image](content/86f309183eee6a76bd680ab61d5f041b.gif)

Page 377

![Image](content/d8f8a1bc8fca0e5b33e7203f11ad8087.gif)

Page 378

![Image](content/9225d159b487df6016c2082f98356f0e.gif)

**14.** Save your program as insertrec.pl

Page 379

### **The editcontact.pl Program**

Remember that the listcontacts.pl program had a form sending the record number of any selected record? Now you are going to look at how your new program, editcontact.pl, will load all of the data for a record into the fields ready to be modified by the user. Then you will examine how to pass any changes (in fact you will pass all of the fields, changed or not) to the database update program, updaterec.pl.

**1.** Open a new Perl program in your editor.

#!c:/perl/bin

![Image](content/2033d537679a7cf218fc0e039c3fd901.gif)

Page 380

![Image](content/2bb76371b3870e41f683492bcf91aebc.gif)

Page 381

| **NOTE** |
| Note that this is very similar to the listcontacts.pl processing, except there you were processing a list and so there was a while loop wrapped around the above statements. Here you only want one record, and you know that it exists because your listcontacts.pl program found it. |

![Image](content/4da9acaf1885399bfade3e6aa367354c.gif)

From now on, everything is almost identical to the addcontact.htm program, so you can copy and paste the form from your addcontact.htm page. Following are a few of things that you will have to change.

Page 382

![Image](content/b2e3ed48f5ac4712270fc621e65c6dfb.gif)

![Image](content/0622cef0d1b36b64415fe8914e039dbb.gif)

**12.** Change the name of the form referred to in the JavaScript checkfields() function to ''editrec" Doing so doesn't alter the way it works, but it looks appropriate to anyone reading your code! As long as the form name reference in the JavaScript matches the name of the form, everything will work.

<html> <head> <title>Update Contact</title> <Script Language=JavaScript> function checkfields( ) { var okeydokey; okeydokey = 1; if(document.editrec. firstname.value == "") { alert("You have not entered the contact's First Name"); okeydokey = 0; document.editrec. firstname.focus( ); } if(document.editrec.lastname.value == "" && okeydokey) { alert("You have not entered the contact's Last Name"); okeydokey = 0; document.editrec.lastname.focus( ); }

Page 383

if(document.editrec.street.value == ''" && okeydokey) { alert("You have not entered the contact's Street Address"); okeydokey = 0; document.editrec.street.focus( ); } if(document.editrec.town.value == "" && okeydokey) { alert("You have not entered the contact's Town"); okeydokey = 0; document.editrec.town.focus( ); } if(document.editrec.postcode.value == "" && okeydokey) { alert("You have not entered the contact's Zip / Post Code"); okeydokey = 0; document.editrec.postcode.focus( ); } if(document.editrec.phone.value == "" && okeydokey) { alert("You have not entered the contact's Phone No."); okeydokey = 0; document.editrec.phone.focus( ); } if(document.editrec.email.value == "" && okeydokey) { alert("You have not entered the contact's e-mail address"); okeydokey = 0; document.editrec.email.focus( ); } if(okeydokey) { document.editrec.submit( ); } }

Page 384

</script> </head>

![Image](content/92cdd9052f47bef0286f685d88f5edf5.gif)

![Image](content/99b9614c4440244b2df4792b927dc786.gif)

Page 385

Page 386

![Image](content/3d45a5c54d1c0458db7342fc22b61b9e.gif)

Page 387

![Image](content/15fa8549b7646fd5ce2d9a62d529b029.gif)

**17.** Save the program as editcontact.pl.

And that is the editcontact.pl program completed. This program will ''call" the program updaterec.pl, which is what you are going to code next.

### **The updaterec.pl Program**

The form in the editcontact.pl program points at the updaterec.pl program. Again, a hidden field is used to pass the id to the updaterec.pl program, as the user does not need to see it displayed. This is another simple program using SQL and ADO to update the data as supplied by the form in editcontact.pl.

Page 388

**1.** Open a new Perl program in your editor.

#!c:/perl/bin

![Image](content/c7530823ff756ae413b0aa617e5230d5.gif)

Page 389

![Image](content/36e95d605de0ee1d6de4959c7ae4d930.gif)

![Image](content/8a51c4e23a5b142a76aabe5ab53798fa.gif)

Page 390

![Image](content/9df6601ad37b46a97918a455fb50670c.gif)

**12.** Save your program as updaterec.pl

And that's it! All you have to do now is to create the database itself and then you're in business.

### **The Database**

This is the last step in creating your application. You are going to create the database that your application ''talks" to. Create the database (contact.mdb) in exactly the same way as you did in Chapter 14. Don't forget that for added security, the database should be stored above the Web root (wwwroot).

Make sure that the option "Allow Zero Length" for each field is set to "Yes." This prevents errors if you decide that completion of a field is not mandatory and you therefore remove the JavaScript code pertaining to that field.

Page 391

Don't forget to set up the data source name using the ODBC feature of the control panel. If you can't remember how, refer to Chapter 14.

Save your database as contact.mdb.

![Image](content/e0033becda0fcde35eab3bf8361dfbc8.gif)

You now have a full, working application. I did leave out one function: the delete option. See if you can work out how to do it. Here's a clue: the deleterec.pl would be almost identical to the updaterec.pl program. Do you remember how the listcontacts.pl program links to the editcontact.pl program using the hidden id field? The delete function will work in exactly the same way! You will need another separate form like that used for the edit buttons in the listcontacts.pl program. But this time you can go directly to the deleterec.pl program because you're not editing anything.

There are a number of improvements you can make to this program. You can improve the look and feel, you can add a search facility (remember the ''LIKE %data% option in SQL?), and you could add a separate view option that doesn't have edit options, so that you can just look at the data. You could even allow an e-mail to be sent directly from your program.

Page 392

### **A Final Word**

That brings us to the end of this book. I have not tried to make you an expert in Perl, but I hope I have helped you to get up and running writing Web applications with the minimum of fuss and complexities. There is much more you will want to learn that is beyond the scope of this book; I will have to leave you to research this on your own.

Please feel free to e-mail me with any questions or problems that you may have. I cannot promise to answer every question, but I will certainly read them all and create a FAQ page to answer the most frequently asked.

E-mail me at perl@sparksoft.net.

Good Luck and happy Perl Fast & Easy programming!

Page 393

## **Appendixes**

| ***Appendix A*** |  |
| **More Perl Functions** | **395** |
| ***Appendix B*** |  |
| **Web Site Resources** | **403** |

Page 394

*This page intentionally left blank.*

Page 395

## **A
More Perl Functions**

This appendix is a ragbag of functions and other features in Perl that you might find useful in your future applications.

Page 396

### **The length() Function**

The length() function returns the length of a scalar variable. The syntax for the length function is

$size = length($variable);

For example, the following code:

$variable = ''fred"; $size = length($variable); print "The length of \$size = $size";

would display

The length of $size = 4

### **The reverse() Function**

The reverse() function takes an array as its argument, and returns an array in which the order of the elements has been reversed. The syntax is

@reversedarray = reverse( @startarray );

So, if you do this

@startarray = (A .. K); @reversedarray = reverse( @startarray ); print "Array = @reversedarray \n";

Then you will see

K J I H G F E D C B A

Page 397

### **The index() Function**

The index() function finds the postion of the first occurrence of another string. By default, it starts at the leftmost character of the string being searched. If you add a third optional parameter, the function will start at the location in this parameter.

The syntax is as follows:

$position = index($teststring, $substring);

Or

$position = index($teststring, $substring, $startposition);

So, for example

$teststring = ''Perl Fast & Easy Web Development"; $position = index($teststring, "Web"); print "The position of \"Web\" in \$teststring is: $position \n";

will display

The position of "Web" in $teststring is: 17;

| **NOTE** |
| The first location in the string is 0\. If the substring being searched for is not found, the function will return the value –1. |

### **The rindex() Function**

The rindex() function finds the rightmost position of the first occurrence of another string. That is, it searches the string backwards. In all other respects, this function is the same as the index() function.

Page 398

The syntax is as follows:

$position = rindex($teststring, $substring);

Or

$position = rindex($teststring, $substring, $startposition);

So, for example

$teststring = ''Perl Fast & Easy Web Development"; $position = rindex($teststring, "Web" ); print "The position of \"Web\" in \$teststring is: $position \n";

will also display

The position of "Web" in $teststring is: 17;

### **The substr() Function**

The substring() function enables you to extract a partial string from another string. The syntax is as follows:

Substr( $wholestring, offset, length, $replacementstring);

This means inspect $wholestring (which can be a variable or a literal), starting at offset position, for a length of length, and replace the substring if found with the contents of $replacementstring (which can also be a literal).

So the following:

$wholestring = "Cats are cute"; $substring = substr( $wholestring, 0, 4, "Dogs"); print $substring;

will you give you

Cats are cute

Page 399

If you leave out the $replacementstring parameter, then just the substring is returned so that the same code as above but without the $replacementstring parameter, would give

Cats

substr() is quite a powerful function.

### **The tr/// Operator**

The tr/// operator is not, strictly speaking, a function, but it can be argued that it provides one. The syntax of the tr/// operator is

tr/ searchstring / replacestring /

The forward slashes are simply delimiters.

The tr/// operator is very powerful. Consider the following:

$newstring =~ tr/a-z/A - Z/

This will replace every character in a string, of the range a to z, and replace it with the uppercase equivalent A to Z.

Note the =~ symbol. This is called the *binding operator* and if it is not used, the operation is carried out on whatever is in $_. In this case you will not use a variable on the lefthand side, like this:

tr/a-k/A-K

You can also add modifiers onto the end of the translation operator. So

tr/a-k/h-k/c

(where /c is the modifier) replaces any character that is not in the search string.

tr/a-k/h-k/d

deletes any characters that are found that match the searchstring characters, but where no replacement is present in replacestring.

Page 400

### **The chr() Function**

The chr() function returns the character corresponding to the ASCII code supplied in the parentheses.

Chr(67)

returns the letter C.

This function can be useful for issuing special codes such as linefeed characters, tab characters, and so on.

### **The ord() Function**

Essentially, the ord() function does the opposite of the chr() function. So if you provide C as an argument or parameter, 67 will be returned.

If you send more than one character to the function, only the first character is used.

So

$asciinumber = ord(''Cat");

returns 67 in the variable $asciinumber.

### **The join() Function**

The join() function is an interesting function. It joins together lists or strings into one string, but separates them by a supplied separator. The syntax is like this:

$wholestring = join (separator_character, list);

Often the separator will be a comma or some other character considered useful as a field separator. This has obvious uses in creating comma-separated value (csv) files.

Page 401

For example:

@array1 = ( ''Lord", "of", "the", "rings"); $string1 = join( ', ' @array1); print $string1;

will display

Lord, of, the, rings

The separator can be any string you like.

### **The sort() Function**

The sort() function sorts lists of values.

The syntax is

sort (@listofvalues);

For example, if you do this:

print sort("animal", "vegetable", "mineral");

then

animalmineralvegetable

would be displayed. You can separate the words again using the join() function.

### **The rand() Function**

The rand() function generates a random floating-point number that is less than 1 but greater then zero. If you want a larger number you have to supply the maximum value you want. If you want an integer you must use the int() function to return a whole number, like this:

print int(rand(10);

This prints an integer between 0 and 9.

Page 402

### **The Here Document**

This is a peculiar but very useful feature. The Here document enables you to pass everything that follows an opening identifier to pass straight through so that everything is quoted as though it were text until Perl sees a closing identifier.

If you put an unquoted identifier at the beginning of the Here document, Perl will interpolate any variables it finds in the text. This is very useful if you are sending a form back to use with variables assigned to form elements. It saves a lot of coding.

This is the basic syntax:

<<an_identifer_string; a line of text and another line of text and yet another line of text an_identifer_string

If the closing identifier is the last line of your Perl program, there must be another carriage return.

A quoted opening identifier such as

<<'an_identifer_string';

prevents interpolation.

There is an example of this in use in Chapter 17, ''Case Study: Contact Database."

I hope you find these additional functions and features useful. This book does not describe or constitute a full list of the features and functions available in Perl, nor has every possible use of every parameter of every function been described. But I hope there has been enough to whet your appetite without scaring you away.

Page 403

## **B
Web Site Resources**

Page 404

### **Official Sites for Obtaining Perl and More**

Here are a list of some of the best Perl Web sites, where you can find just about any information you need regarding Perl. As you will find, the available resources for this powerful and ubiquitous language are huge, and the list grows daily. My small list will help to get you started. Happy Surfing!

• http://www.perl.com/

• http://www.activestate.com/

• http://www.perl.org/

• http://www.cpan.org/

### **Learning More about Perl**

If you want to study Perl in more depth, these sites will give you a good start. There is a lot of good quality content on the sites, and even if you can't find exactly what you are looking for, you will probably find something that will nudge you into generating a solution of your own.

Following are some sites where you can get all the official downloads of Perl, Perl news, version information and lots more:

• http://www.perlmonks.org/index.pl?node=Tutorials

• http://www.webreference.com/perl/

• http://cgi.resourceindex.com/Documentation/Programming_Languages/Programming_in_Perl/

• http://www.devshed.com/Server_Side/Perl

• http://www.perlmasters.com/tutorial/

Page 405

### **Free Perl Scripts**

Here are some sites offering free Perl scripts that do lots of jobs. These scripts make great learning tools. If you want to find something fast or you're having an idle day, try one of these sites!

• http://www.scriptarchive.com/ (This site is probably one of the best for code examples and ideas..)

• http://www.bignosebird.com/cgi.shtml

• http://cgi.resourceindex.com/

• http://www.freeperlcode.com/

### **Learning More about HTML and JavaScript**

Did you find the sections on HTML and JavaScript interesting? Would you like to learn more? These sites will teach you lots more:

• http://www.w3schools.com/

• http://www.htmlgoodies.com/

• http://www.w3schools.com/html/

• http://www.pageresource.com/jscript/

• http://www.w3schools.com/js/default.asp

• http://javascriptkit.com/

• http://developer.netscape.com/tech/javascript/resources.html

I hope these have given you a good taste of what is on the Web for the Perl developer. As I have said, there are vast resources waiting to be tapped.

Page 406

*This page intentionally left blank.*

Page 407

## **Index**

### **Symbols**

**-- (decrement operator),** 40, 57-61

**' (single quotes),** 46

**!**

exclamation marks, 24

not operator, 79

**# (comment sign),** 24

**$**

hashes, 96

subroutine placeholder, 142

**$! variable,** 236

**$/ (input record separator),** 123

**$_ scalar variable,** 43-47

**$blatpath variable,** 269

**$commandline variable,** 270

**$conn variable,** 290

**$count variable,** 60-61

**$dbhandle variable,** 300-302

**$from variable,** 273

**$fromaddress variable,** 265

**$fromsender variable,** 268

**$loopcounter variable,** 112

**$message variable,** 266, 269, 273

**$number variable,** 38-42

**$recipients variable,** 268

**$result variable,** 35

**$rs variable,** 290

**$sendmailpath variable,** *273-274*

**$server variable,** 265, 269

**$smtp variable,** 266

**$sql variable,** 291

**$sqlstatement variable,** 301

**$statementhandle variable,** 301

**$string variable,** 62

**$subject variable,** 265, 269, 273

**$table variable,** 290

**$tempbuffer variable,** 227

**$thisline variable,** 254-256

**$title variable,** 87

**$to variable,** 273

**$toaddress variable,** 265

**$WIN_TEMPFILE variable,** 269

**%**

hashes, 96

modulus operator, 54-56

**&& (and operator),** 79

**&nbsp code,** 151-153

**() (parentheses),** 79

*** HTML value,** 184

**** (exponentiation operator),** 54-56

Page 408

**. (concatenation operator),** 62-63

**; (semicolon),** 23, 319

**@**

array sign, 82

hashes, 96

**@_ variable,** 142

**@alphabet array,** 85-86

**@letters array,** 86-87

**@months array,** 83

**@mynumbers array,** 84-85

**@things array,** 87-88

**[] (brackets),** 86

**\ (backslash),** 42, 48

**\n (newline character),** 47

**{} (braces),** 65, 108

**|| (or operator),** 79

**++ (increment operator),** 40, 57-61

**= (assignment operator),** 52-54

**=> operator,** 98

**> (file writing character),** 243-247

**¬ (not character),** 253-254

### **A**

**<A> tag,** 175-180

**accessing folders,** 18

**Access 97 databases.** *See* databases

**Active Data Objects.** *See* ADO

**Active State Web site,** 2

**addcontact.htm form (contacts database),** 369-375

**adding records,** 294-296

**addresses**

IP, 193

validating, 334-339

**ADO (Active Data Objects),** 289

LockTypes, 292

records

adding, 294-296

deleting, 297-299

reading, 289-293

recordsets, 290

updating, 296-297

**Aladdin Systems Web site,** 11

**alert command,** 316

**alert() method,** 325

**alias (PWS),** 15

**aligning text,** 158-159

**@alphabet array,** 85-86

**and operator (&&),** 78-79

**Apache Web site,** 12

**arguments**

default variables, 43-47

functions, 120

**arithmetic operators,** 54-56

**arrays**

@ sign, 82

@alphabet, 85-86

associative. See hashes

brackets ([]), 86

declaring, 82-88

element zero, 82

functions, 91-94, 132

pop(), 137-138

print(), 132-133

push(), 136-137

scalar(), 133-136

joining, 89-91

@letters, 86-87

loading, 88-89

@months, 83

@mynumbers, 84-85

@things, 87-88

two-dimensional, 94

Page 409

**assigning values,** 35, 319

**assignment operator (=),** 52-54

**associative arrays.** *See* hashes

**attributes**

BACKGROUND, 162-164

BGCOLOR, 161-162

blank, 180

case sensitivity, 149

CHECKED, 210

COLS, 184

MAXLENGTH, 207

METHOD, 205-206

NAME, 175, 205-206

new, 180

ROWS, 184

SIZE, 207

TARGET, 179

**autoexec.bat file,** 6-10

### **B**

**b() function,** 346

**<B> tag,** 154

**background,** 161-164

**BACKGROUND attribute,** 162-164

**backslashes (\),** 42, 48

**BGCOLOR attribute,** 161-162

**blank attribute,** 180

**blank lines,** 35

**Blat.exe,** 267-272

**$blatpath variable,** 269

**blocks of code,** 107, 315

**<BODY> tag,** 147-149, 161-164

**Boolean values,** 77-79

**br() function,** 346

**<BR> tag,** 151

**braces ({}),** 65, 108

**brackets ([]),** 86

**building**

databases, 280-285

forms (CGI.pm), 348-351

**bulletin boards,** 2

**buttons (HTML forms),** 218-220

### **C**

**case sensitivity**

debugging programs, 34

escape codes, 48-49

HTML tags, 149

JavaScript, 319

string operators, 67-69

variables, 34

**<CENTER> tag,** 158-159

**CGI (Common Gateway Interface).** *See also* CGI.pm

processing, 192

programs, 193-203

troubleshooting, 197-200

**CGI-BIN folder (PWS),** 15

**CGI.pm.** *See also* CGI

building forms, 348-351

form data, 352-354

HTML pages, 343-347

object-oriented mode, 354-359

troubleshooting tables, 351

**check boxes,** 210-212

**checkbox_group() function,** 349

**CHECKED attribute,** 210

**checkfields() function,** 375

**checking errors,** 241-242

**checkit() method,** 324, 327

**CHMOD command,** 18

**chomp() function,** 123-126

**chop() function,** 120-123

**chr() function,** 398

Page 410

**classes**

inheritance, 310

superclasses, 312

**close() function,** 242-243

**closing files,** 242-243

**code blocks,** 107, 315

**code color,** 22

**code source,** 22

**coding basics,** 22

**color**

coding, 22

HTML documents, 159-161

**COLS attribute,** 184

**columns, selecting,** 367

**comma-arrow operator,** 98

**command line e-mail,** 267-272

**command prompt (MS-DOS),** 3-6, 27

**$commandline variable,** 270

**commands.** *See also* statements

alert, 316

CHMOD, 18

document.write, 316

PATH, 6-10

Perl -v, 5

ppm install dbi, 300

ppm query, 300

print, 26-28

SET, 6

**comments,** 23

# sign, 24

italics, 42

**Common Gateway Interface.** *See* CGI

**comparison operators,** 71-77

numeric, 71-73

string, 74-77

**compiled languages,** 21

**concatenation operator (.),** 62-63

**conditional statements.** *See also* loops

elsif, 108

if, 107-111

**conditional submission,** 323-328

**configuring FTP,** 261-264

**$conn variable,** 290

**contacts database,** 390-391

addcontact.htm form, 369-375

editcontact.pl program, 379-387

home pages, 363-365

insertrec.pl program, 376-378

listcontacts.pl, 365-369

ODBC, 366

requirements, 362-363

selecting columns, 367

updaterec.pl program, 387-390

**context,** 42

**$count variable,** 60-61

**counters,** 112

**creating hashes,** 98

**Ctrl+A keyboard shortcut,** 26

### **D**

**daisy chains,** 53

**data**

files, 253-254

forms (CGI.pm), 352-354

hiding, 311

HTML forms

GET method, 230-233

POST method, 226-230

passing, 142

reading, 237-241

**data() function,** 266

**Data Source Name (DSN),** 286-289

**data types,** 279

**Database Interface.** *See* DBI

Page 411

**databases.** *See also* tables

building, 280-285

contacts database. See contacts database

data types, 279

default values, 279

design, 278-279

DSN, 286-289

records

adding, 294-296

deleting, 297-299

reading, 289-293

recordsets, 290

updating, 296-297

relational, 278

rules, 279

UIDs, 279

**dataend() function,** 267

**datasend() function,** 266-267

**$dbhandle variable,** 300, 302

**DBI (Database Interface),** 299

deleting, 305-307

installing, 299-300

reading, 300-302

updating, 304-305

writing, 302-304

**debugging programs,** 34

**declaring arrays,** 82-88

**decrement operator (--),** 40, 57-61

**default values (databases),** 279

**default variables,** 43-47

**defining variable sets,** 53

**delete() function,** 100-104

**deleting**

DBI, 305-307

files, 247-249

keys (hashes), 100-104

records, 297-299

**design, database,** 278-279

**development versions, downloading,** 2

**die() function,** 236, 241-242

**directories,** 249

creating, 250-251

deleting, 251-253

PWS, 15

**<DIV> tag,** 158-159, 168

**DNS (Domain Name Server),** 193

**do loops,** 113-115

**document objects,** 313

**document.write command,** 316

**documents**

Here, 400

HTML

background, 161-164

color, 159-161

structure, 147

writing, 147-153

publishing, 14

**Domain Name Server (DNS),** 193

**DOS commands**

PATH, 6-10

Perl -v, 5

SET, 6

**dot notation,** 311

**downloading**

development versions, 2

FTP, 261

PWS, 12

Web sites, 402

**drop-down boxes (HTML forms),** 212-216

**DSN (Data Source Name),** 286-289

### **E**

**each() function,** 139-140

**editcontact.pl (contacts database),** 379-387

**editors, selecting,** 22

Page 412

**element zero (arrays),** 82

**elements (HTML forms),** 204-206

**elsif statements,** 108

**em() function,** 346, 353

**e-mail**

address validation, 334-339

Blat.exe, 267-272

command-line, 267-272

FTP. See FTP

lists, 2

platforms, 260

Sendmail, 272-275

SMTP, 264-267

UNIX, 272-275

**end_html function,** 344

**environment variables,** 195

**error-checking,** 241-242

**escape codes.** *See also* keyboard shortcuts

HTML, 151-153

text formatting, 48-49

**events**

onClick, 313

onMouseOver, 313

**exclamation marks (!),** 24

**exponentiation operator (**),** 54-56

**expressions,** 23

### **F**

**FAQ Web site,** 392

**fields**

$thisline, 254-256

forms, 328-329

separators, 253-254

tables, 278

**files**

deleting, 247-249

autoexec.bat, 6-10

closing, 242-243

data, 253-254

directories, 249

creating, 250-251

deleting, 251-253

error checking, 241-242

field separators, 253-254

file handles, 236

GIFs, 171

HTML, 146

JPEGs, 171-174

naming, 236

opening, 236

paths, 23-26

PNGs, 171

reading, 256-258

reading data, 237-241

Test Home Page, 16

writing, 243-247, 254-256

**flag -w,** 24

**flow.** *See* program flow

**focus() method,** 328

**Focus() method,** 313

**folders**

access, 18

CGI-BIN (PWS), 15

creating, 16

Home (PWS), 14

myhtml, 203

myPerl, 22

scripts, 193

SCRIPTS (PWS), 15

Test (PWS), 15-19

wwwroot, 203

**<FONT> tag,** 165-166

**fonts,** 165-166

**for loops,** 109-111, 115-117

**foreach loops,** 140

**<FORM> tag,** 204

Page 413

**format, free,** 23

**formatting text,** 48-49, 153-155

**forms**

building, 348-351

data, 352-354

HTML, 203

check boxes, 210-212

contacts database, 369-375

data retrieval, 226-233

drop-down boxes, 212-216

elements, 204-206

hidden fields, 207

password fields, 207

radio buttons, 207-210

reset buttons, 218-220

submit buttons, 218-220

text area fields, 216-218

text fields, 206-207

JavaScript

conditional submission, 323-328

fields, 328-329

submitting, 323

validating, 321-323

**frames,** 181-188

**<FRAMESET> tag,** 182-188

**free format,** 23

**$from variable,** 273

**$fromaddress variable,** 265

**$fromsender variable,** 268

**FTP,** 261

configuring, 261-264

downloading, 261

ISPs, 260-261

**functions.** *See also* methods

arguments, 120

arrays, 91-94, 132-138

b(), 346

br(), 346

checkbox_group(), 349

checkfields(), 375

chomp(), 123-126

chop(), 120-123

chr(), 398

close(), 242-243

data(), 266

dataend(), 267

datasend(), 266-267

delete(), 100-104

die(), 236, 241-242

each(), 139-140

em(), 346, 353

end_html, 344

h1(), 344

hash, 139-140

header(), 343

hr(), 345

i(), 346

index(), 395

int(), 399-400

join(), 353, 398-399

lc(), 68, 129-132

lcfirst(), 68, 129-132

length(), 126-127, 394

li(), 346

mail(), 266

mkdir(), 250-251

networking, 264-267

ol(), 346

onClick(), 375

open(), 236, 243-247, 256-258

ord(), 398

param(), 352-354

parameters, 120

pop(), 137-138

popup_menu(), 349

print(), 132-133, 239

push(), 136-137

quit(), 267

Page 414

qw, 342

radio_group(), 350

rand(), 399-400

results, 120

return(), 142

reverse(), 394

rindex(), 395-396

rmdir(), 251-253

scalar(), 133-136

sort(), 399

start_html, 343

strings, 120-132

subroutines, 120, 140-143

substr(), 66-67, 127-129, 396-397

td(), 351

textarea(), 349

textfield(), 349

to(), 266

tr(), 351

tr///(), 397

uc(), 68, 129-132

ucfirst(), 68, 129-132

unlink(), 247-249

user-defined. *See* subroutines

### **G**

**GET method,** 230-233

**GIFs,** 171

### **H**

**h1() function,** 344

**handles,** 236

**hashes**

% symbol, 96

creating, 98

deleting keys, 100-104

functions, 139-140

initializing, 97, 101

loading, 99, 100

operators, 98

prefixes, 96-97

**<HEAD> tag,** 147-149

**header() function,** 343

**headings**

HTML, 155-157

troubleshooting, 194

**Here document,** 400

**hidden fields (HTML forms),** 207

**Home folder (PWS),** 14

**home pages**

contacts database, 363-365

creating, 14

**horizontal rules,** 167-168

**hr() function,** 345

**<HR> tag,** 167-168

**HTML**

attributes

BACKGROUND, 162-164

BGCOLOR, 161-162

blank, 180

case sensitivity, 149

CHECKED, 210

COLS, 184

MAXLENGTH, 207

METHOD, 205-206

NAME, 175, 205-206

new, 180

ROWS, 184

SIZE, 207

TARGET, 179

CGI.pm, 343-347

documents

background, 161-164

color, 159-161

structure, 147

writing, 147-153

Page 415

escape codes, 151-153

files, 146

forms, 203

check boxes, 210-212

contacts database, 369-375

data retrieval, 226-233

drop-down boxes, 212-216

elements, 204-206

hidden fields, 207

password fields, 207

radio buttons, 207-210

reset buttons, 218-220

submit buttons, 218-220

text area fields, 216-218

text fields, 206-207

frames, 181-188

headings, 155-157

horizontal rules, 167-168

images, 171-174

linking, 174-180

newlines, 151

spaces, 151-153

tables, 222-226

tags

* value, 184

<A>, 175-180

<B>, 154

<BODY>, 147-164

<BR>, 151

<CENTER>, 158-159

<DIV>, 158-159, 168

<FONT>, 165-166

<FORM>

<FRAMESET>, 182-188

<HEAD>, 147-149

<HR>, 167-168

<HTML>, 148

<Hx>, 155-157

<I>, 154

<INPUT TYPE>, 216

<META>, 147

<P>, 169-170

<SCRIPT>, 147, 314-315

<SELECT>, 212-216

<STDIN>, 31

<TABLE>, 222-226

<TD>, 223

<TEXTAREA>, 216-218

<TH>, 223

<TITLE>, 147-148

<TR>, 223

<U>, 154

text

aligning, 158-159

fonts, 165-166

formatting, 153-155

Web sites, 403

**<HTML> tag,** 148

**HTMLPad 2000,** 22

**<Hx> tags,** 155-157

### **I**

**i() function,** 346

**<I> tag,** 154

**if() method,** 322-328

**if statements,** 107-111

**images**

GIFs, 171

HTML, 171-174

JPEGs, 171-174

PNGs, 171

**increment operator (++),** 40, 57-61

**index() function,** 395

Page 416

**inheritance, classes,** 310

**initializing hashes,** 97, 101

**input**

record separator, 123

users, 29-31

**<INPUT TYPE> tag,** 216

**insertrec.pl (contacts database),** 376-378

**Installer (MS),** 3

**installing**

DBI, 299, 300

Macintosh, 11

UNIX, 10, 11

Windows, 3-10

**instantiation,** 311

**int() function,** 399-400

**Internet security (PWS),** 13

**interpolating**

operators, 52

single quotes, 46

strings, 239

variables, 39, 64-66

**interpreted languages,** 21

**interpreter (perl.exe),** 23-26

**IP addresses,** 193

**IP Switch Web site,** 261

**isNaN() method,** 329-334

**ISPs (FTP),** 260-261

**italics, comments,** 42

**iterating.** *See* looping

### **J**

**JavaScript**

;(semicolon), 319

case-sensitivity, 319

classes

inheritance, 310

superclasses, 312

code blocks, 315

commands

alert, 316

document.write, 316

data hiding, 311

document objects, 313

dot notation, 311

e-mail address validation, 334-339

forms

conditional submission, 323-328

fields, 328-329

submitting, 323

validating, 321-323

instantiation, 311

methods, 311

alert(), 325

checkit(), 324, 327

focus(), 328

if(), 322-328

isNaN(), 329-334

submit(), 323-325

objects, 313-314

operators, 320

placing, 314-315

polymorphism, 312

statements, 319

syntax, 315-319

values, 319

variables, 319-321

Web sites, 403

**join() function,** 353, 398-399

**joining arrays,** 89-91

**JPEGs,** 171-174

Page 417

### **K**

**keyboard shortcuts.** *See also* escape codes Ctrl+A, 26

**keyboards,** 31

*keys, deleting*, 100-104

**keyword var,** 319

### **L**

**languages**

compiled, 21

interpreted, 21

**lc() function,** 68, 129-132

**lcfirst() function,** 68, 129-132

**length parameter,** 67

**length() function,** 126-127, 394

**@letters array,** 86-87

**li() function,** 346

**lines, HTML,** 167-168

**linking HTML,** 174-180

**listcontacts.pl (contacts database),** 365-369

**listing parameters,** 142

**literals,** 42

**loading**

arrays, 88-89

operators, 99-100

**LockTypes,** 292

**logical operators,** 77-79

**$loopcounter variable,** 112

**loops.** *See also* conditional statements

do, 113-115

for, 109-111, 115-117

foreach, 140

program flow, 106

until, 111-113

variables, 60-61

while, 111-113, 237-241

### **M**

**Macintosh, installing,** 11

*MacPerl*, 11

**Mail Transfer Agent (MTA),** 259

**mail() function,** 266

**MAXLENGTH attribute,** 207

**$message variable,** 266, 269, 273

**<META> tag,** 147

**METHOD attribute,** 205-206

**methods.** *See also* functions

alert(), 325

checkit(), 324, 327

focus(), 328

Focus(), 313

GET, 230-233

if(), 322-328

isNaN(), 329-334

POST, 226-230

submit(), 323, 325

Win32, 290

**Microsoft Installer,** 3

**Microsoft System Information page,** 7

**mkdir() function,** 250-251

**modules**

CGI.pm, 342

building forms, 348-351

form data, 352-354

HTML pages, 343-347

object-oriented mode, 354-359

troubleshooting tables, 351

Net, 264-267

**modulus operator (%),** 54-56

**@months array,** 83

**MS Installer,** 3

**MS-DOS prompt,** 3-6, 27

**MTA (Mail Transfer Agent),** 259

Page 418

**myhtml folder,** 203

**@mynumbers array,** 84-85

**myPerl folder,** 22

### **N**

**\\n (newline character),** 47

**NAME attribute,** 175, 205-206

**naming**

files, 236

variables, 92

**&nbsp code,** 151-153

**Net module,** 264-267

**networking functions,** 264-267

**new attribute,** 180

**newlines,** 39

HTML, 151

\\n, 47

**newsgroups,** 2, 402

**non-breaking spaces,** 151-153

**not character (¬),** 253-254

**not operator (!),** 78-79

**NT,** 24-26

**NT Server 4 Option Pack,** 12

**$number variable,** 38-42

**numeric comparison operators,** 71-73

**numeric variables,** 69-71

### **O**

**Object Linking and Embedding (OLE),** 289

*object-oriented mode (CGI.pm)*, 354-359

**object-oriented programming (OOP).** *See* JavaScript

**objects**

document objects, 313

JavaScript, 313-314

**ODBC,** 366

**ol() function,** 346

**OLE (Object Linking and Embedding),** 289

**onClick event,** 313

**onClick() function,** 375

**onMouseOver event,** 313

**OOP (object-oriented programming).** *See* JavaScript

**open() function,** 236, 243-247, 256-258

**opening files,** 236

**operators**

! (not), 79

&& (and), 79

() (parentheses), 79

. (concatenation), 62-63

|| (or), 79

=>, 98

and, 78

arithmetic, 54-56

assignment (=), 52-54

comma-arrow, 98

comparison, 71-77

numeric, 71-73

string, 74-77

decrement (--), 40, 57-61

exponentiation (**), 54-56

hashes, 98

increment (++), 40, 57-61

interpolation, 52

JavaScript, 320

logical, 77-79

modulus (%), 54-56

not, 78

or, 78

precedence, 79

searching, 99-100

strings, 62-71

case, 67-69

numeric variables, 69-71

substrings, 66, 67

variable interpolation, 64-66

Page 419

variables

precedence, 42, 60-61

scalar variables, 35-37

updating, 57-61

**or operator (||),** 78-79

**ord() function,** 398

**output, troubleshooting,** 239

### **P**

**<P> tag,** 169-170

**pages**

home, 14

Microsoft System Information, 7

viewing (PWS), 12

**param() function,** 352-354

**parameters**

default variables, 43-47

functions, 120

length, 67

listing, 142

placeholders, 142

programs, 268

**parentheses (()),** 79

**passing data,** 142

**password fields (HTML forms),** 207

**PATH command,** 6-10

**paths, updating,** 6-10

**Peer Web Services,** 11

**Perl Bundle,** 10

**Perl -v command,** 5

**Perl Web sites,** 2, 402

**perl.exe,** 23-26

**permissions (UNIX),** 18

**Personal Web Manager,** 13

**Personal Web Server.** *See* PWS

**placeholder, $,** 142

**placing JavaScript,** 314-315

**platforms,** 24-26, 260

**PNGs,** 171

**polymorphism,** 312

**pop() function,** 137-138

**popup_menu() function,** 349

**POST method,** 226-230

**ppm install dbi command,** 300

**ppm query command,** 300

**precedence, operators,** 42, 60-61, 79

**prefixes, hashes,** 96-97

**print command,** 26-28

**print() function,** 132-133, 239

**processing CGI,** 192

**Production version,** 10

**programs**

CGI, 193-203

troubleshooting, 197-200

debugging, case-sensitivity, 34

contacts database

editcontact.pl, 379-387

insertrec.pl, 376-378

listcontacts.pl, 365-369

updaterec.pl, 387-390

flow, 106

code blocks, 107

looping, 106

selection, 106

sequence, 106

parameters, 268

StuffIt Expander, 11

**prompts.** *See* command prompts

**publishing documents,** 14

**push() function,** 136-137

**PWS (Personal Web Server),** 11-19

alias, 15

CGI-BIN folder, 15

downloading, 12

Home folder, 14

home pages, 14

Page 420

Internet security, 13

Peer Web Services, 11

Personal Web Manager, 13

publishing documents, 14

SCRIPTS folder, 15

Test folder, 15-19

touring, 14

viewing pages, 12

virtual directories, 15

### **Q**

**quit() function,** 267

**quotes, single ('),** 46

**qw function,** 342

### **R**

**radio buttons,** 207-210

**radio_group() function,** 350

**rand() function,** 399-400

**reading**

data, 237-241

DBI, 300-302

files, 256-258

records, 289-293

**$recipients variable,** 268

**record separator, input,** 123

**records**

adding, 294-296

deleting, 297-299

reading, 289-293

recordsets, 290

updating, 296-297

**recordsets,** 290

**reference scalar variables,** 34

**Registry Editor,** 197-200

**relational databases,** 278

**REMOTE_HOST variable,** 195

**requirements (contacts database),** 362-363

**reset buttons,** 218-220

**resources,** 2

**$result variable,** 35

**results (functions),** 120

**return() function,** 142

**reverse() function,** 394

**rindex() function,** 395-396

**rmdir() function,** 251-253

**ROWS attribute,** 184

**$rs variable,** 290

**rules (databases),** 279

### **S**

**scalar variables,** 34-42

$_, 43-47

$number, 38-42

operators, 35-37

references, 34

strings, 42-43

**scalar() function,** 133-136

**screen display.** *See* printing

**<SCRIPT> tag,** 147, 314-315

**scripts**

folders, 193

URLs, 193

Web sites, 403

**SCRIPTS folder (PWS),** 15

**searching, operators,** 99-100

**security (PWS),** 13

**SELECT statement,** 367

**<SELECT> tag,** 212-216

**selecting**

all, 26

columns, 367

text editors, 22

**selection (program flow),** 106

**semicolon (;),** 23, 319

**Sendmail,** 272-275

Page 421

**$sendmailpath variable,** 273-274

**separator, input record,** 123

**sequence (program flow),** 106

**$server variable,** 265, 269

**SET command,** 6

**sets, variables,** 53

**Shebang statement,** 23-26

**shrieks,** 24

**simulating two-dimensional arrays,** 94

**single quotes ('),** 46

**SIZE attribute,** 207

**slashes, comparing,** 239

**SMTP,** 264-267

**$smtp variable,** 266

**sort() function,** 399

**source code,** 22

**spaces**

HTML, 151-153

troubleshooting, 65

**splats,** 24

**SQL (Structured Query Language).** See ADO

**$sql variable,** 291

**$sqlstatement variable,** 301

**stable versions,** 10

**Standard Input Stream or Device,** 31

**start_html function,** 343

**$statementhandle variable,** 301

**statements.** *See also* commands

code blocks, 107

conditional. See loops

elsif, 108

if, 107-111

JavaScript, 319

SELECT, 367

Shebang, 23-26

system, 271

terminating, 23

**<STDIN> tag,** 31

**$string variable,** 62

**strings**

comparison operators, 74-77

functions, 120

chomp(), 123-126

chop(), 120-123

lc(), 129-132

lcfirst(), 129-132

length(), 126-127

substr(), 127-129

uc(), 129-132

ucfirst(), 129-132

interpolating, 239

operators, 62-71

case, 67-69

numeric variables, 69-71

substrings, 66-67

variable interpolation, 64-66

scalar variables, 42-43

**structure (HTML documents),** 147

**Structured Query Language.** *See* ADO

**StuffIt Expander program,** 11

**$subject variable,** 265, 269, 273

**submit buttons,** 218-220

**submit() method,** 323, 325

**submitting forms,** 323-328

**subroutines**

$ placeholder, 142

data, passing, 142

functions, 120, 140-143

parameters, 142

**substr() function,** 66-67, 127-129, 396-397

**substrings,** 66-67

**superclasses,** 312

**support,** 2

**syntax,** 22

blank lines, 35

checker, 24

Page 422

exclamation marks (!), 24

JavaScript, 315-319

semicolons (;), 23

**System Configuration Utility,** 7-8

**system statement,** 271

### **T**

**<TABLE> tag,** 222-226

**$table variable,** 290

**tables.** *See* also databases

fields, 278

HTML, 222-226

troubleshooting, 351

**tags.** *See* HTML tags

**TARGET attribute,** 179

**td() function,** 351

**<TD> tag,** 223

**$tempbuffer variable,** 227

**terminating statements,** 23

**Test folder (PWS),** 15-19

**Test Home Page file,** 16

**text**

aligning, 158-159

fonts, 165-166

formatting, 48-49, 153-155

selecting

all, 26

editors, 22

**text area fields (HTML forms),** 216-218

**text fields (HTML forms),** 206-207

**textarea() function,** 349

**<TEXTAREA> tag,** 216-218

**textfield() function,** 349

**<TH> tag,** 223

**@things array,** 87-88

**$thisline variable,** 254-256

**<TITLE> tag,** 147-148

**$title variable,** 87

**to() function,** 266

**$to variable,** 273

**$toaddress variable,** 265

**touring PWS,** 14

**tr() function,** 351

**tr///() function,** 397

**<TR> tag,** 223

**troubleshooting**

CGI programs, 197-200

files, 241-242

headers, 194

output, 239

spaces, 65

syntax, 24

tables, 351

**two-dimensional arrays,** 94

### **U**

**<U> tag,** 154

**uc() function,** 68, 129-132

**ucfirst() function,** 68, 129-132

**UIDs (unique IDs),** 279

**unique IDs,** 279

**UNIX,** 24-26

DBI

deleting, 305-307

installing, 299-300

reading, 300-302

updating, 304-305

writing, 302-304

e-mail, 272-275

installing, 10-11

Perl Bundle, 10

permissions, 18

versions, 10

**unlink() function,** 247-249

Page 423

**unstable versions,** 2

**until loops,** 111-113

**updaterec.pl (contacts database),** 387-390

**updating**

DBI, 304-305

paths, 6-10

records, 296-297

variables, 57-61

**URLs, scripts,** 193

**user input,** 29-31

**user-defined functions.** See subroutines

**utility, System Configuration Utility,** 7-8

### **V**

**validating**

addresses, 334-339

forms, 321-323

**values**

assigning, 35, 319

Boolean, 77-79

default, 279

**var keyword,** 319

**variables**

@_, 142

$!, 236

$/ (input record separator), 123

assigning values, 35

$blatpath, 269

case-sensitivity, 34

$commandline, 270

$conn, 290

context, 42

$count, 60-61

daisy chains, 53

$dbhandle, 300, 302

default, 43-47

environment, 195

$from, 273

$fromaddress, 265

$fromsender, 268

interpolating, 39, 64-66

JavaScript, 319-321

literals, 42

$loopcounter, 112

looping, 60-61

$message, 266, 269, 273

names, 92

numeric string operators, 69-71

operators

precedence, 42, 60-61

updating, 57-61

$recipients, 268

REMOTE_HOST, 195

$result, 35

$rs, 290

scalar, 34-42

$_, 43-47

$number, 38-42

operators, 35-37

references, 34

strings, 42-43

$sendmailpath, 273-274

$server, 265, 269

sets, 53

$smtp, 266

$sql, 291

$sqlstatement, 301

$statementhandle, 301

$string, 62

$subject, 265, 269, 273

$table, 290

$tempbuffer, 227

$thisline, 254-256

$title, 87