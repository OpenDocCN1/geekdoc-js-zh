![](images/cover.jpg)

![Cover: Software Design by Example: A Tool-Based Introduction with JavaScript, written by Greg Wilson, published by CRC Press, Taylor and Francis Group, Boca Raton, London, New York, CRC Press is an imprint of the Taylor and Francis Group, an informa business, a Chapman and Hall book.](images/cover.jpg)

First edition published 2023

by CRC Press

6000 Broken Sound Parkway NW, Suite 300, Boca Raton, FL 33487-2742

and by CRC Press

4 Park Square, Milton Park, Abingdon, Oxon, OX14 4RN

© 2023 Greg Wilson

*CRC Press is an imprint of Taylor & Francis Group, LLC*

Reasonable efforts have been made to publish reliable data and information, but the author and publisher cannot assume responsibility for the validity of all materials or the consequences of their use. The authors and publishers have attempted to trace the copyright holders of all material reproduced in this publication and apologize to copyright holders if permission to publish in this form has not been obtained. If any copyright material has not been acknowledged please write and let us know so we may rectify in any future reprint.

Except as permitted under U.S. Copyright Law, no part of this book may be reprinted, reproduced, transmitted, or utilized in any form by any electronic, mechanical, or other means, now known or hereafter invented, including photocopying, microfilming, and recording, or in any information storage or retrieval system, without written permission from the publishers.

For permission to photocopy or use material electronically from this work, access [www.copyright.com](http://www.copyright.com) or contact the Copyright Clearance Center, Inc. (CCC), 222 Rosewood Drive, Danvers, MA 01923, 978-750-8400\. For works that are not available on CCC please contact [mpkbookspermissions@tandf.co.uk](mailto:mpkbookspermissions@tandf.co.uk)

*Trademark notice*: Product or corporate names may be trademarks or registered trademarks and are used only for identification and explanation without intent to infringe.

**Library of Congress Cataloging-in-Publication Data**

Names: Wilson, Greg, 1963- author.

Title: Software design by example: a tool-based introduction with JavaScript/Greg Wilson.

Description: First edition. | Boca Raton: C&H/CRC Press, 2023\. | Includes bibliographical references and index.

Identifiers: LCCN 2022030475 (print) | LCCN 2022030476 (ebook) | ISBN 9781032399676 (hardback) | ISBN 9781032330235 (paperback) | ISBN 9781003317807 (ebook)

Subjects: LCSH: Software patterns. | Software architecture. | JavaScript (Compuer program language)

Classification: LCC QA76.76.P37 W55 2023 (print) | LCC QA76.76.P37 (ebook) | DDC 005.13/267–dc23/eng/20220906

LC record available at [https://lccn.loc.gov/2022030475](https://lccn.loc.gov/2022030475)

LC ebook record available at [https://lccn.loc.gov/2022030476](https://lccn.loc.gov/2022030476)

ISBN: 978-1-032-39967-6 (hbk)

ISBN: 978-1-032-33023-5 (pbk)

ISBN: 978-1-003-31780-7 (ebk)

DOI: [10.1201/9781003317807](https://doi.org/10.1201/9781003317807)

Typeset in SFRM

by KnowledgeWorks Global Ltd.

*Publisher's note:* This book has been prepared from camera-ready copy provided by the authors.

# Dedication

For Brian Kernighan, who taught us all how to write about programming.

And for all the students who took part in CSC49X: long may you run.

All royalties from sales of this book will go to support the Red Door Family Shelter in Toronto.

# 1Introduction

The best way to learn design is to study examples [[Schon1984](#refbib1.xhtml_refbib_25); [Petre2016]](#refbib1.xhtml_refbib_23), and some of the best examples of software design come from the tools programmers use in their own work. In these lessons we build small versions of things like file backup systems, testing frameworks, regular expression matchers, and browser layout engines both to demystify them and to give some insights into how experienced programmers think. We draw inspiration from [[Brown2011](#refbib1.xhtml_refbib_4); [Brown2012](#refbib1.xhtml_refbib_5); [Brown2016]](#refbib1.xhtml_refbib_3), Mary Rose Cook's[¹](#chapter1.xhtml_fn1_1) Gitlet[²](#chapter1.xhtml_fn1_2), and the books that introduced the Unix philosophy to an entire generation of programmers [[Kernighan1979](#refbib1.xhtml_refbib_15); [Kernighan1981](#refbib1.xhtml_refbib_16); [Kernighan1983](#refbib1.xhtml_refbib_14); [Kernighan1988]](#refbib1.xhtml_refbib_17).

All of the written material in this project can be freely reused under the terms of the Creative Commons - Attribution - NonCommercial license[³](#chapter1.xhtml_fn1_3), while all of the software is made available under the terms of the Hippocratic License[⁴](#chapter1.xhtml_fn1_4). All proceeds from this project will go to support the Red Door Family Shelter[⁵](#chapter1.xhtml_fn1_5).

## 1.1 Who is our audience?

Every lesson should be written with specific learners in mind. These three personas[⁶](#chapter1.xhtml_fn1_6) describe ours:

*   Aïsha started writing VB macros for Excel in an accounting course and never looked back. After spending three years doing front-end JavaScript work she now wants to learn how to build back-end applications. This material will fill in some gaps in her programming knowledge and teach her some common design patterns.

*   Rupinder is studying computer science at college. He has learned a lot about the theory of algorithms, and while he uses Git and unit testing tools in his assignments, he doesn't feel he understands how they work. This material will give him a better understanding of those tools and of how to design new ones.

*   Yim builds mobile apps for a living but also teaches two college courses: one on full-stack web development using JavaScript and Node and another titled “Software Design”. They are happy with the former, but frustrated that so many books about the latter subject talk about it in the abstract and use examples that their students can't relate to. This material will fill those gaps and give them starting points for a wide variety of course assignments.

Like these three personas, readers should be able to:

*   Write JavaScript programs using loops, arrays, functions, and classes.

*   Create static web pages using HTML and CSS.

*   Install Node on their computer and run programs with it from the command line.

*   Use Git[⁷](#chapter1.xhtml_fn1_7) to save and share files. (It's OK not to know the more obscure commands[⁸](#chapter1.xhtml_fn1_8).)

*   Explain what a tree is and how to process one recursively. (This is the most complicated data structure and algorithm we *don't* explain.)

This book can be read on its own or used as a classroom resource. If you are looking for a project to do in a software design course, adding a tool to those covered here would be fun as well as educational. Please see [Chapter 21](#chapter21.xhtml) for more details.

## 1.2 What tools and ideas do we cover?

Programmers have invented a lot of tools[⁹](#chapter1.xhtml_fn1_9) to make their lives easier. This volume focuses on a few that individual developers use while writing software; we hope future volumes will explore those used in the applications that programmers build.

Appendix E defines the terms we introduce in these lessons, which in turn define their scope:

*   How to process a program like any other piece of text.

*   How to turn a program into a data structure that can be analyzed and modified.

*   What design patterns are and which ones are used most often.

*   How programs are executed and how we can control and inspect their execution.

*   How we can analyze programs’ performance in order to make sensible design tradeoffs.

*   How to find and run code modules on the fly.

## 1.3 How are these lessons laid out?

We display JavaScript source code like this:

![](images/comp01_1.jpg)

Unix shell commands are shown like this:

![](images/comp01_2.jpg)

and data and output like this:

![](images/comp01_3.jpg)

We occasionally wrap lines in source code in unnatural ways to make listings fit the printed page, and sometimes use ... to show where lines have been omitted. Where we need to break lines of output for the same reason, we end all but the last line with a single backslash \. The full listings are all available in our Git repository[^(10)](#chapter1.xhtml_fn1_10) and on our website[^(11)](#chapter1.xhtml_fn1_11).

Finally, we write functions as functionName rather than functionName(); the latter is more common, but people don't use objectName{} for objects or arrayName[] for arrays, and the empty parentheses makes it hard to tell whether we're talking about “the function itself” or “a call to the function with no parameters”.

## 1.4 How did we get here?

In the early 2000s, the University of Toronto asked Greg Wilson[^(12)](#chapter1.xhtml_fn1_12) to teach an undergraduate course on software architecture. After delivering the course three times he told the university they should cancel it: between them, the dozen textbooks he had purchased with the phrase “software architecture” in their titles devoted a total of less than 30 pages to describing the designs of actual systems.

Frustrated by that, he and Andy Oram[^(13)](#chapter1.xhtml_fn1_13) persuaded some well-known programmers to contribute a chapter each to a collection called *Beautiful Code* [[Oram2007](#refbib1.xhtml_refbib_20)], which went on to win the Jolt Award in 2007\. Entries in the book described everything from figuring out whether three points are on a line to core components of Linux and the software for the Mars Rover, but the breadth that made them fun to read also meant they weren't particularly useful for teaching.

To fix that, Greg Wilson, Amy Brown[^(14)](#chapter1.xhtml_fn1_14), Tavish Armstrong[^(15)](#chapter1.xhtml_fn1_15), and Mike DiBernardo[^(16)](#chapter1.xhtml_fn1_16) edited a four-book series between 2011 and 2016 called *The Architecture of Open Source Applications*[^(17)](#chapter1.xhtml_fn1_17). In the first two volumes, the creators of fifty open source projects described their systems’ designs; the third book explored the performance of those systems, while in the fourth volume contributors built scale models of common tools as a way of demonstrating how those tools worked. These books were closer to what an instructor would need for an undergraduate class on software design, but still not quite right: the intended audience would probably not be familiar with many of the problem domains, and since each author used the programming language of their choice, much of the code would be hard to understand.

*Software Tools in JavaScript* is meant to address these shortcomings: all of the code is written in one language, and the examples are all tools that programmers use daily. Most of the programs are less than 60 lines long and the longest is less than 200; we believe each chapter can be covered in class in 1-2 hours, while the exercises range in difficulty from a few minutes to a couple of days.

## 1.5 How can people use and contribute to this material?

All of the written material on this site is made available under the Creative Commons - Attribution - NonCommercial 4.0 International license (CC-BY-NC-4.0), while the software is made available under the Hippocratic License. The first allows you to use and remix this material for non-commercial purposes, as-is or in adapted form, provided you cite its original source; the second allows you to use and remix the software on this site provided you do not violate international agreements governing human rights. Please see [Appendix A](#appendix1.xhtml_appendix1) for details.

If you would like to improve what we have or add new material, please see the Code of Conduct in [Appendix B](#appendix2.xhtml_appendix2) and the contributor guidelines in [Appendix C](#appendix3.xhtml_appendix3). If you have questions or would like to use this material in a course, please file an issue in our GitHub repository[^(18)](#chapter1.xhtml_fn1_18) or send us email.

## 1.6 Who helped us?

I am grateful to the creators of diagrams.net[^(19)](#chapter1.xhtml_fn1_19), Emacs[^(20)](#chapter1.xhtml_fn1_20), ESLint[^(21)](#chapter1.xhtml_fn1_21), Glosario[^(22)](#chapter1.xhtml_fn1_22), GNU Make[^(23)](#chapter1.xhtml_fn1_23), LaTeX[^(24)](#chapter1.xhtml_fn1_24), Node[^(25)](#chapter1.xhtml_fn1_25), NPM[^(26)](#chapter1.xhtml_fn1_26), Standard JS[^(27)](#chapter1.xhtml_fn1_27), SVG Screenshot[^(28)](#chapter1.xhtml_fn1_28), WAVE[^(29)](#chapter1.xhtml_fn1_29), and all the other open source tools used in creating these lessons: if we all give a little, we all get a lot. I would also like to thank Darren McElligott, Evan Schultz, and Juanan Pereira for their feedback; any errors, omissions, or misunderstandings that remain are entirely my fault.

# 2Systems Programming

Terms defined: **[anonymous function](#appendix5.xhtml_d10)**, **[asynchronous](#appendix5.xhtml_d19)**, **[Boolean](#appendix5.xhtml_d29)**, **[callback function](#appendix5.xhtml_d41)**, **[cognitive load](#appendix5.xhtml_d53)**, **[command-line argument](#appendix5.xhtml_d58)**, **[console](#appendix5.xhtml_d65)**, **[current working directory](#appendix5.xhtml_d71)**, **[destructuring assignment](#appendix5.xhtml_d84)**, **[edge case](#appendix5.xhtml_d99)**, **[filename extension](#appendix5.xhtml_d115)**, **[filesystem](#appendix5.xhtml_d116)**, **[filter](#appendix5.xhtml_d117)**, **[globbing](#appendix5.xhtml_d127)**, **[idiomatic](#appendix5.xhtml_d142)**, **[log message](#appendix5.xhtml_d176)**, **[path (in filesystem)](#appendix5.xhtml_d209)**, **[protocol](#appendix5.xhtml_d222)**, **[scope](#appendix5.xhtml_d243)**, **[single-threaded](#appendix5.xhtml_d255)**, **[string interpolation](#appendix5.xhtml_d271)**

The biggest difference between JavaScript and most other programming languages is that many operations in JavaScript are **asynchronous**. Its designers didn't want browsers to freeze while waiting for data to arrive or for users to click on things, so operations that might be slow are implemented by describing now what to do later. And since anything that touches the hard drive is slow from a processor's point of view, Node[¹](#chapter2.xhtml_fn2_1) implements **filesystem** operations the same way.

[Table 2.1:](#chapter2.xhtml_b2tbl2_1) Computer operation times at human scale.

| **Operation** | **Actual Time** | **Would Be…** |
| 1 CPU cycle | 0.3 nsec | 1 sec |
| Main memory access | 120 nsec | 6 min |
| Solid-state disk I/O | 50-150 µsec | 2-6 days |
| Rotational disk I/O | 1-10 msec | 1-12 months |
| Internet: San Francisco to New York | 40 msec | 4 years |
| Internet: San Francisco to Australia | 183 msec | 19 years |
| Physical system reboot | 5 min | 32,000 years |

Early JavaScript programs used **callback functions** to describe asynchronous operations, but as we're about to see, callbacks can be hard to understand even in small programs. In 2015, the language's developers standardized a higher-level tool called promises to make callbacks easier to manage, and more recently they have added new keywords called async and await to make it easier still. We need to understand all three layers in order to debug things when they go wrong, so this chapter explores callbacks, while [Chapter 3](#chapter3.xhtml) shows how promises and async/await work. This chapter also shows how to read and write files and directories with Node's standard libraries, because we're going to be doing that a lot.

## 2.1 How can we list a directory?

To start, let's try listing the contents of a directory the way we would in Python[²](#chapter2.xhtml_fn2_2) or Java[³](#chapter2.xhtml_fn2_3):

![](images/comp02_1.jpg)

We use import *module* from ‘source’ to load the library *source* and assign its contents to *module*. After that, we can refer to things in the library using *module.component* just as we refer to things in any other object. We can use whatever name we want for the module, which allows us to give short nicknames to libraries with long names; we will take advantage of this in future chapters.

Our little program uses the fs[⁴](#chapter2.xhtml_fn2_4) library which contains functions to create directories, read or delete files, etc. (Its name is short for “filesystem”.) We tell the program what to list using **command-line arguments**, which Node automatically stores in an array called process.argv. The name of the program used to run our code is stored process.argv[0] (which in this case is node), while process.argv[1] is the name of our program (in this case list-dir-wrong.js). The rest of process.argv holds whatever arguments we gave at the command line when we ran the program, so process.argv[2] is the first argument after the name of our program ([Figure 2.1](#chapter2.xhtml_fig2_1)).

![](images/fig2_1.jpg)

[Figure 2.1:](#chapter2.xhtml_b2fig2_1) How Node stores command-line arguments in process.argv.

If we run this program with the name of a directory as its argument, fs.readdir returns the names of the things in that directory as an array of strings. The program uses for (const name of results) to loop over the contents of that array. We could use let instead of const, but it's good practice to declare things as const wherever possible so that anyone reading the program knows the variable isn't actually going to vary—doing this reduces the **cognitive load** on people reading the program. Finally, console.log is JavaScript's equivalent of other languages’ print command; its strange name comes from the fact that its original purpose was to create **log messages** in the browser **console**.

Unfortunately, our program doesn't work:

![](images/comp02_2.jpg)![](images/comp02_3.jpg)

The error message comes from something we didn't write whose source we would struggle to read. If we look for the name of our file (list-dir-wrong.js) we see the error occurred on line 4; everything above that is inside fs.readdir, while everything below it is Node loading and running our program.

The problem is that fs.readdir doesn't return anything. Instead, its documentation says that it needs a callback function that tells it what to do when data is available, so we need to explore those in order to make our program work.

## 2.2 What is a callback function?

JavaScript uses a **single-threaded** programming model: as the introduction to this lesson said, it splits operations like file I/O into “please do this” and “do this when data is available”. fs.readdir is the first part, but we need to write a function that specifies the second part.

JavaScript saves a reference to this function and calls with a specific set of parameters when our data is ready ([Figure 2.2](#chapter2.xhtml_fig2_2)). Those parameters defined a standard **protocol** for connecting to libraries, just like the USB standard allows us to plug hardware devices together.

![](images/fig2_2.jpg)

[Figure 2.2:](#chapter2.xhtml_b2fig2_2) How JavaScript runs callback functions.

This corrected program gives fs.readdir a callback function called listContents:

![](images/comp02_4.jpg)

Node callbacks always get an error (if there is any) as their first argument and the result of a successful function call as their second. The function can tell the difference by checking to see if the error argument is null. If it is, the function lists the directory's contents with console.log, otherwise, it uses console.error to display the error message. Let's run the program with the **current working directory** (written as ‘.’) as an argument:

![](images/comp02_5.jpg)![](images/comp02_6.jpg)

Nothing that follows will make sense if we don't understand the order in which Node executes the statements in this program ([Figure 2.3](#chapter2.xhtml_fig2_3)):

1.  Execute the first line to load the fs library.

2.  Define a function of two parameters and assign it to listContents. (Remember, a function is just another kind of data.)

3.  Get the name of the directory from the command-line arguments.

4.  Call fs.readdir to start a filesystem operation, telling it what directory we want to read and what function to call when data is available.

5.  Print a message to show we're at the end of the file.

6.  Wait until the filesystem operation finishes (this step is invisible).

7.  Run the callback function, which prints the directory listing.

![](images/fig2_3.jpg)

[Figure 2.3:](#chapter2.xhtml_b2fig2_3) When JavaScript runs callback functions.

## 2.3 What are anonymous functions?

Most JavaScript programmers wouldn't define the function listContents and then pass it as a callback. Instead, since the callback is only used in one place, it is more **idiomatic** to define it where it is needed as an **anonymous function**. This makes it easier to see what's going to happen when the operation completes, though it means the order of execution is quite different from the order of reading ([Figure 2.4](#chapter2.xhtml_fig2_4)). Using an anonymous function gives us the final version of our program:

![](images/comp02_7.jpg)![](images/fig2_4.jpg)

[Figure 2.4:](#chapter2.xhtml_b2fig2_4) How and when JavaScript creates and runs anonymous callback functions.

## 2.4 How can we select a set of files?

Suppose we want to copy some files instead of listing a directory's contents. Depending on the situation we might want to copy only those files given on the command line or all files except some explicitly excluded. What we *don't* want to have to do is list the files one by one; instead, we want to be able to write patterns like *.js.

To find files that match patterns like that, we can use the glob[⁵](#chapter2.xhtml_fn2_5) module. (To **glob** (short for “global”) is an old Unix term for matching a set of files by name.) The glob module provides a function that takes a pattern and a callback and does something with every filename that matched the pattern:

![](images/comp02_8.jpg)![](images/comp02_9.jpg)

The leading ** means “recurse into subdirectories”, while *.* means “any characters followed by ‘.’ followed by any characters” ([Figure 2.5](#chapter2.xhtml_fig2_5)). Names that don't match *.* won't be included, and by default, neither are names that start with a ‘.’ character. This is another old Unix convention: files and directories whose names have a leading ‘.’ usually contain configuration information for various programs, so most commands will leave them alone unless told to do otherwise.

![](images/fig2_5.jpg)

[Figure 2.5:](#chapter2.xhtml_b2fig2_5) Using glob patterns to match filenames.

This program works, but we probably don't want to copy editor backup files whose names end with .bck. We can get rid of them by **filtering** the list that glob returns:

![](images/comp02_10.jpg)![](images/comp02_11.jpg)

Array.filter creates a new array containing all the items of the original array that pass a test ([Figure 2.6](#chapter2.xhtml_fig2_6)). The test is specified as a callback function that Array.filter calls once once for each item. This function must return a **Boolean** that tells Array.filter whether to keep the item in the new array or not. Array.filter does not modify the original array, so we can filter our original list of filenames several times if we want to.

![](images/fig2_6.jpg)

[Figure 2.6:](#chapter2.xhtml_b2fig2_6) Selecting array elements using Array.filter.

We can make our globbing program more idiomatic by removing the parentheses around the single parameter and writing just the expression we want the function to return:

![](images/comp02_12.jpg)

However, it turns out that glob will filter for us. According to its documentation, the function takes an options object full of key-value settings that control its behavior. This is another common pattern in Node libraries: rather than accepting a large number of rarely-used parameters, a function can take a single object full of settings.

If we use this, our program becomes:

![](images/comp02_13.jpg)

Notice that we don't quote the key in the options object. The keys in objects are almost always strings, and if a string is simple enough that it won't confuse the parser, we don't need to put quotes around it. Here, “simple enough” means “looks like it could be a variable name”, or equivalently “contains only letters, digits, and the underscore”.

To finish off our globbing program, let's specify a source directory on the command line and include that in the pattern:

![](images/comp02_14.jpg)

This program uses **string interpolation** to insert the value of srcDir into a string. The template string is written in back quotes, and JavaScript converts every expression written as ${expression} to text. We could create the pattern by concatenating strings using srcDir + ’/**/*.*’, but most programmers find interpolation easier to read.

## 2.5 How can we copy a set of files?

If we want to copy a set of files instead of just listing them we need a way to create the **paths** of the files we are going to create. If our program takes a second argument that specifies the desired output directory, we can construct the full output path by replacing the name of the source directory with that path:

![](images/comp02_15.jpg)

This program uses **destructuring assignment** to create two variables at once by unpacking the elements of an array ([Figure 2.7](#chapter2.xhtml_fig2_7)). It only works if the array contains enough elements, i.e., if both a source and destination are given on the command line; we'll add a check for that in the exercises.

![](images/fig2_7.jpg)

[Figure 2.7:](#chapter2.xhtml_b2fig2_7) Assigning many values at once by destructuring.

A more serious problem is that this program only works if the destination directory already exists: fs and equivalent libraries in other languages usually won't create directories for us automatically. The need to do this comes up so often that there is a function called ensureDir to do it:

![](images/comp02_16.jpg)

Notice that we import from fs-extra instead of fs; the fs-extra[⁶](#chapter2.xhtml_fn2_6) module provides some useful utilities on top of fs. We also use path[⁷](#chapter2.xhtml_fn2_7) to manipulate pathnames rather than concatenating or interpolating strings because there are a lot of tricky **edge cases** in pathnames that the authors of that module have figured out for us.

Our file copying program currently creates empty destination directories but doesn't actually copy any files. Let's use fs.copy to do that:

![](images/comp02_17.jpg)

The program now has three levels of callback ([Figure 2.8](#chapter2.xhtml_fig2_8)):

1.  When glob has data, do things and then call ensureDir.

2.  When ensureDir completes, copy a file.

3.  When copy finishes, check the error status.

![](images/fig2_8.jpg)

[Figure 2.8:](#chapter2.xhtml_b2fig2_8) Three levels of callback in the running example.

Our program looks like it should work, but if we try to copy everything in the directory containing these lessons we get an error message:

![](images/comp02_18.jpg)![](images/comp02_19.jpg)

The problem is that node_modules/fs.stat and node_modules/fs.walk match our globbing expression, but are directories rather than files. To prevent our program from trying to use fs.copy on directories, we must use fs.stat to get the properties of the things glob gives us and then check if they are files. The name “stat” is short for “status”, and since the status of something in the filesystem can be very complex, fs.stat returns an object with methods that can answer common questions[⁸](#chapter2.xhtml_fn2_8).

Here's the final version of our file copying program:

![](images/comp02_20.jpg)

It works, but four levels of asynchronous callbacks is hard for humans to understand. [Chapter 3](#chapter3.xhtml) will introduce a pair of tools that make code like this easier to read.

## 2.6 Exercises

### Where is Node?

Write a program called wherenode.js that prints the full path to the version of Node it is run with.

### Tracing callbacks

In what order does the program below print messages?

![](images/comp02_21.jpg)

### Tracing anonymous callbacks

In what order does the program below print messages?

![](images/comp02_22.jpg)

### Checking arguments

Modify the file copying program to check that it has been given the right number of command-line arguments and to print a sensible error message (including a usage statement) if it hasn't.

### Glob patterns

What filenames does each of the following glob patterns match?

*   results-[0123456789].csv

*   results.(tsv|csv)

*   results.dat?

*   ./results.data

### Filtering arrays

Fill in the blank in the code below so that the output matches the one shown. Note: you can compare strings in JavaScript using <, > =, and other operators, so that (for example) person.personal > ’P’ is true if someone's personal name starts with a letter that comes after ‘P’ in the alphabet.

![](images/comp02_23.jpg)![](images/comp02_24.jpg)

### String interpolation

Fill in the code below so that it prints the message shown.

![](images/comp02_25.jpg)![](images/comp02_26.jpg)

### Destructuring assignment

What is assigned to each named variable in each statement below?

1.  const first = [10, 20, 30]

2.  const [first, second] = [10, 20, 30]

3.  const [first, second, third] = [10, 20, 30]

4.  const [first, second, third, fourth] = [10, 20, 30]

5.  const {left, right} = {left: 10, right: 30}

6.  const {left, middle, right} = {left: 10, middle: 20, right: 30}

### Counting lines

Write a program called lc that counts and reports the number of lines in one or more files and the total number of lines, so that lc a.txt b.txt displays something like:

![](images/comp02_27.jpg)

### Renaming files

Write a program called rename that takes three or more command-line arguments:

1.  A **filename extension** to match.

2.  An extension to replace it with.

3.  The names of one or more existing files.

When it runs, rename renames any files with the first extension to create files with the second extension, but will *not* overwrite an existing file. For example, suppose a directory contains a.txt, b.txt, and b.bck. The command:

![](images/comp02_28.jpg)

will rename a.txt to a.bck, but will *not* rename b.txt because b.bck already exists.

# 3Asynchronous Programming

Terms defined: **[call stack](#appendix5.xhtml_d40)**, **[character encoding](#appendix5.xhtml_d45)**, **[class](#appendix5.xhtml_d49)**, **constructor**, **[event loop](#appendix5.xhtml_d106)**, **[exception](#appendix5.xhtml_d107)**, **[fluent interface](#appendix5.xhtml_d121)**, **method**, **[method chaining](#appendix5.xhtml_d185)**, **[non-blocking execution](#appendix5.xhtml_d194)**, **[promise](#appendix5.xhtml_d220)**, **[promisification](#appendix5.xhtml_d221)**, **protocol**, **UTF-8**

Callbacks work, but they are hard to read and debug, which means they only “work” in a limited sense. JavaScript's developers added **promises** to the language in 2015 to make callbacks easier to write and understand, and more recently they added the keywords async and await as well to make asynchronous programming easier still. To show how these work, we will create a **class** of our own called Pledge that provides the same core features as promises. Our explanation was inspired by Trey Huffine's[¹](#chapter3.xhtml_fn3_1) tutorial[²](#chapter3.xhtml_fn3_2), and we encourage you to read that as well.

## 3.1 How can we manage asynchronous execution?

JavaScript is built around an **event loop**. Every task is represented by an entry in a queue; the event loop repeatedly takes a task from the front of the queue, runs it, and adds any new tasks that it creates to the back of the queue to run later. Only one task runs at a time; each has its own **call stack**, but objects can be shared between tasks ([Figure 3.1](#chapter3.xhtml_fig3_1)).

![](images/fig3_1.jpg)

[Figure 3.1:](#chapter3.xhtml_b3fig3_1) Using an event loop to manage concurrent tasks.

Most tasks execute all the code available in the order it is written. For example, this one-line program uses Array.forEach to print each element of an array in turn:

![](images/comp03_1.jpg)![](images/comp03_2.jpg)

However, a handful of special built-in functions make Node[³](#chapter3.xhtml_fn3_3) switch tasks or add new tasks to the run queue. For example, setTimeout tells Node to run a callback function after a certain number of milliseconds have passed. Its first argument is a callback function that takes no arguments, and its second is the delay. When setTimeout is called, Node sets the callback aside for the requested length of time, then adds it to the run queue. (This means the task runs *at least* the specified number of milliseconds later.)

As the listing below shows, the original task can generate many new tasks before it completes, and those tasks can run in a different order than the order in which they were created ([Figure 3.2](#chapter3.xhtml_fig3_2)).

![](images/comp03_3.jpg)![](images/comp03_4.jpg)![](images/fig3_2.jpg)

[Figure 3.2:](#chapter3.xhtml_b3fig3_2) Using setTimeout to delay operations.

If we give setTimeout a delay of zero milliseconds, the new task can be run right away, but any other tasks that are waiting have a chance to run as well:

![](images/comp03_5.jpg)![](images/comp03_6.jpg)

We can use this trick to build a generic **non-blocking function** that takes a callback defining a task and switches tasks if any others are available:

![](images/comp03_7.jpg)![](images/comp03_8.jpg)

Node's built-in function setImmediate does exactly what our nonBlocking function does: Node also has process.nextTick, which doesn't do quite the same thing—we'll explore the differences in the exercises.

![](images/comp03_9.jpg)![](images/comp03_10.jpg)

## 3.2 How do promises work?

Before we start building our own promises, let's look at how we want them to work:

![](images/comp03_11.jpg)![](images/comp03_12.jpg)

This short program creates a new Pledge with a callback that takes two other callbacks as arguments: resolve (which will run when everything worked) and reject (which will run when something went wrong). The top-level callback does the first part of what we want to do, i.e., whatever we want to run before we expect a delay; for demonstration purposes, we will use setTimeout with zero delay to switch tasks. Once this task resumes, we call the resolve callback to trigger whatever is supposed to happen after the delay.

Now look at the line with then. This is a **method** of the Pledge object we just created, and its job is to do whatever we want to do after the delay. The argument to then is yet another callback function; it will get the value passed to resolve, which is how the first part of the action communicates with the second ([Figure 3.3](#chapter3.xhtml_fig3_3)).

![](images/fig3_3.jpg)

[Figure 3.3:](#chapter3.xhtml_b3fig3_3) Order of operations when a promise resolves.

In order to make this work, Pledge‘s **constructor** must take a single function called action. This function must take two callbacks as arguments: what to do if the action completes successfully and what to do if it doesn't (i.e., how to handle errors). Pledge will provide these callbacks to the action at the right times.

Pledge also needs two methods: then to enable more actions and catch to handle errors. To simplify things just a little bit, we will allow users to **chain** as many thens as they want, but only allow one catch.

## 3.3 How can we chain operations together?

A **fluent interface** is a style of object-oriented programming in which the methods of an object return this so that method calls can be chained together. For example, if our class is:

![](images/comp03_13.jpg)

then we can write:

![](images/comp03_14.jpg)

or even

![](images/comp03_15.jpg)

Array‘s fluent interface lets us write expressions like Array.filter(...).map(...) that are usually more readable than assigning intermediate results to temporary variables.

If the original action given to our Pledge completes successfully, the Pledge gives us a value by calling the resolve callback. We pass this value to the first then, pass the result of that then to the second one, and so on. If any of them fail and throw an **exception**, we pass that exception to the error handler. Putting it all together, the whole class looks like this:

![](images/comp03_16.jpg)

Let's create a Pledge and return a value:

![](images/comp03_17.jpg)![](images/comp03_18.jpg)

Why didn't this work?

1.  We can't use return with pledges because the call stack of the task that created the pledge is gone by the time the pledge executes. Instead, we must call resolve or reject.

2.  We haven't done anything that defers execution, i.e., there is no call to setTimeout, setImmediate, or anything else that would switch tasks. Our original motivating example got this right.

This example shows how we can chain actions together:

![](images/comp03_19.jpg)![](images/comp03_20.jpg)

Notice that inside each then we *do* use return because these clauses all run in a single task. As we will see in the next section, the full implementation of Promise allows us to run both normal code and delayed tasks inside then handlers.

Finally, in this example we explicitly signal a problem by calling reject to make sure our error handling does what it's supposed to:

![](images/comp03_21.jpg)![](images/comp03_22.jpg)

## 3.4 How are real promises different?

Let's rewrite our chained pledge with built-in promises:

![](images/comp03_23.jpg)![](images/comp03_24.jpg)

It looks almost the same, but if we read the output carefully we can see that the callbacks run *after* the main program finishes. This is a signal that Node is delaying the execution of the code in the then handler.

A very common pattern is to return another promise from inside then so that the next then is called on the returned promise, not on the original promise ([Figure 3.4](#chapter3.xhtml_fig3_4)). This is another way to implement a fluent interface: if a method of one object returns a second object, we can call a method of the second object immediately.

![](images/comp03_25.jpg)![](images/comp03_26.jpg)![](images/fig3_4.jpg)

[Figure 3.4:](#chapter3.xhtml_b3fig3_4) Chaining promises to make asynchronous operations depend on each other.

We therefore have three rules for chaining promises:

1.  If our code can run synchronously, just put it in then.

2.  If we want to use our own asynchronous function, it must create and return a promise.

3.  Finally, if we want to use a library function that relies on callbacks, we have to convert it to use promises. Doing this is called **promisification** (because programmers will rarely pass up an opportunity to add a bit of jargon to the world), and most functions in Node have already been promisified.

## 3.5 How can we build tools with promises?

Promises may seem more complex than callbacks right now, but that's because we're looking at how they work rather than at how to use them. To explore the latter subject, let's use promises to build a program to count the number of lines in a set of files. A few moments of search on NPM[⁵](#chapter3.xhtml_fn3_5) turns up a promisified version of fs-extra called fs-extra-promise, so we will rely on it for file operations.

Our first step is to count the lines in a single file:

![](images/comp03_27.jpg)![](images/comp03_28.jpg)![](images/comp03_29.jpg)

The next step is to count the lines in multiple files. We can use glob-promise to delay handling the output of glob, but we need some way to create a separate task to count the lines in each file and to wait until those line counts are available before exiting our program.

The tool we want is Promise.all, which waits until all of the promises in an array have completed. To make our program a little more readable, we will put the creation of the promise for each file in a separate function:

![](images/comp03_30.jpg)![](images/comp03_31.jpg)![](images/comp03_32.jpg)

However, we want to display the names of the files whose lines we're counting along with the counts. To do this our then must return two values. We could put them in an array, but it's better practice to construct a temporary object with named fields ([Figure 3.5](#chapter3.xhtml_fig3_5)). This approach allows us to add or rearrange fields without breaking code and also serves as a bit of documentation. With this change our line-counting program becomes:

![](images/comp03_33.jpg)![](images/fig3_5.jpg)

[Figure 3.5:](#chapter3.xhtml_b3fig3_5) Creating temporary objects with named fields to carry values forward.

As in [Chapter 2](#chapter2.xhtml), this works until we run into a directory whose name name matches *.*, which we do when counting the lines in the contents of node_modules. The solution once again is to use stat to check if something is a file or not before trying to read it. And since stat returns an object that doesn't include the file's name, we create another temporary object to pass information down the chain of thens.

![](images/comp03_34.jpg)![](images/comp03_35.jpg)![](images/comp03_36.jpg)

This code is complex, but much simpler than it would be if we were using callbacks.

## 3.6 How can we make this more readable?

Promises eliminate the deep nesting associated with callbacks of callbacks, but they are still hard to follow. The latest versions of JavaScript provide two new keywords async and await to flatten code further. async means “this function implicitly returns a promise”, while await means “wait for a promise to resolve”. This short program uses both keywords to print the first ten characters of a file:

![](images/comp03_37.jpg)![](images/comp03_38.jpg)

> **Translating code**
> 
> When Node sees await and async it silently converts the code to use promises with then, resolve, and reject; we will see how this works in [Chapter 15](#chapter15.xhtml). In order to provide a context for this transformation we must put await inside a function that is declared to be async: we can't simply write await fs.statAsync(...) at the top level of our program outside a function. This requirement is occasionally annoying, but since we should be putting our code in functions anyway it's hard to complain.

To see how much cleaner our code is with await and async, let's rewrite our line counting program to use them. First, we modify the two helper functions to look like they're waiting for results and returning them. They actually wrap their results in promises and return those, but Node now takes care of that for us:

![](images/comp03_39.jpg)

Next, we modify main to wait for things to complete. We must still use Promise.all to handle the promises that are counting lines for individual files, but the result is less cluttered than our previous version.

![](images/comp03_40.jpg)

## 3.7 How can we handle errors with asynchronous code?

We created several intermediate variables in the line-counting program to make the steps clearer. Doing this also helps with error handling; to see how, we will build up an example in stages.

First, if we return a promise that fails without using await, then our main function will finish running before the error occurs, and our try/catch doesn't help us ([Figure 3.6](#chapter3.xhtml_fig3_6)):

![](images/comp03_41.jpg)![](images/comp03_42.jpg)![](images/fig3_6.jpg)

[Figure 3.6:](#chapter3.xhtml_b3fig3_6) Wrong and right ways to handle errors in asynchronous code.

One solution to this problem is to be consistent and always return something. Because the function is declared async, the Error in the code below is automatically wrapped in a promise so we can use .then and .catch to handle it as before:

![](images/comp03_43.jpg)![](images/comp03_44.jpg)

If instead we return await, the function waits until the promise runs before returning. The promise is turned into an exception because it failed, and since we're inside the scope of our try/catch block, everything works as we want:

![](images/comp03_45.jpg)![](images/comp03_46.jpg)

We prefer the second approach, but whichever you choose, please be consistent.

## 3.8 Exercises

### Immediate versus next tick

What is the difference between setImmediate and process.nextTick? When would you use each one?

### Tracing promise execution

1.  What does this code print and why?

    ![](images/comp03_47.jpg)
2.  What does this code print and why?

    ![](images/comp03_48.jpg)
3.  What does this code print and why?

    ![](images/comp03_49.jpg)

Hint: try each snippet of code interactively in the Node interpreter and as a command-line script.

### Multiple catches

Suppose we create a promise that deliberately fails and then add two error handlers:

![](images/comp03_50.jpg)

When the code is run it produces:

![](images/comp03_51.jpg)

1.  Trace the order of operations: what is created and when is it executed?

2.  What happens if we run these same lines interactively? Why do we see something different than what we see when we run this file from the command line?

### Then after catch

Suppose we create a promise that deliberately fails and attach both then and catch to it:

![](images/comp03_52.jpg)

When the code is run it produces:

![](images/comp03_53.jpg)

1.  Trace the order of execution.

2.  Why is undefined printed at the end?

### Head and tail

The Unix head command shows the first few lines of one or more files, while the tail command shows the last few. Write programs head.js and tail.js that do the same things using promises and async/await, so that:

![](images/comp03_54.jpg)

prints the first five lines of each of the three files and:

![](images/comp03_55.jpg)

prints the last five lines of each file.

### Histogram of line counts

Extend count-lines-with-stat-async.js to create a program lh.js that prints two columns of output: the number of lines in one or more files and the number of files that are that long. For example, if we run:

![](images/comp03_56.jpg)

the output might be:

| **Length** | **Number of Files** |
| 1 | 7 |
| 3 | 3 |
| 4 | 3 |
| 6 | 7 |
| 8 | 2 |
| 12 | 2 |
| 13 | 1 |
| 15 | 1 |
| 17 | 2 |
| 20 | 1 |
| 24 | 1 |
| 35 | 2 |
| 37 | 3 |
| 38 | 1 |
| 171 | 1 |

### Select matching lines

Using async and await, write a program called match.js that finds and prints lines containing a given string. For example:

![](images/comp03_57.jpg)

would print all of the lines from the three files that contain the word “Toronto”.

### Find lines in all files

Using async and await, write a program called in-all.js that finds and prints lines found in all of its input files. For example:

![](images/comp03_58.jpg)

will print those lines that occur in all three files.

### Find differences between two files

Using async and await, write a program called file-diff.js that compares the lines in two files and shows which ones are only in the first file, which are only in the second, and which are in both. For example, if left.txt contains:

![](images/comp03_59.jpg)

and right.txt contains:

![](images/comp03_60.jpg)

then:

![](images/comp03_61.jpg)

would print:

![](images/comp03_62.jpg)

where 1, 2, and * show whether lines are in only the first or second file or are in both. Note that the order of the lines in the file doesn't matter.

Hint: you may want to use the Set class to store lines.

### Trace file loading

Suppose we are loading a YAML configuration file using the promisified version of the fs library. In what order do the print statements in this test program appear and why?

![](images/comp03_63.jpg)

### Any and all

1.  Add a method Pledge.any that takes an array of pledges and as soon as one of the pledges in the array resolves, returns a single promise that resolves with the value from that pledge.

2.  Add another method Pledge.all that takes an array of pledges and returns a single promise that resolves to an array containing the final values of all of those pledges.

This article[⁶](#chapter3.xhtml_fn3_6) may be helpful.

# 4Unit Testing

Terms defined: **[absolute error](#appendix5.xhtml_d1)**, **[actual result (of test)](#appendix5.xhtml_d7)**, **[assertion](#appendix5.xhtml_d17)**, **[caching](#appendix5.xhtml_d39)**, **[defensive programming](#appendix5.xhtml_d76)**, **[design pattern](#appendix5.xhtml_d83)**, **[dynamic loading](#appendix5.xhtml_d93)**, **[error (in a test)](#appendix5.xhtml_d104)**, **[exception handler](#appendix5.xhtml_d108)**, **[expected result (of test)](#appendix5.xhtml_d109)**, **[exploratory programming](#appendix5.xhtml_d110)**, **fail (a test)**, **[fixture](#appendix5.xhtml_d120)**, **[global variable](#appendix5.xhtml_d126)**, **[introspection](#appendix5.xhtml_d154)**, **[lifecycle](#appendix5.xhtml_d166)**, **[pass (a test)](#appendix5.xhtml_d207)**, **[relative error](#appendix5.xhtml_d235)**, **[side effect](#appendix5.xhtml_d253)**, **[Singleton pattern](#appendix5.xhtml_d257)**, **[test runner](#appendix5.xhtml_d278)**, **[test subject](#appendix5.xhtml_d279)**, **[throw (exception)](#appendix5.xhtml_d281)**, **[unit test](#appendix5.xhtml_d295)**

We have written many small programs in the previous two chapters, but haven't really tested any of them. That's OK for **exploratory programming**, but if our software is going to be used instead of just read, we should try to make sure it works.

A tool for writing and running **unit tests** is a good first step. Such a tool should:

*   find files containing tests;

*   find the tests in those files;

*   run the tests;

*   capture their results; and

*   report each test's result and a summary of those results.

Our design is inspired by tools like Mocha[¹](#chapter4.xhtml_fn4_1) and Jest[²](#chapter4.xhtml_fn4_2), which were in turn inspired by tools built for other languages from the 1980s onward [[Meszaros2007](#refbib1.xhtml_refbib_19); [Tudose2020]](#refbib1.xhtml_refbib_28).

## 4.1 How should we structure unit testing?

As in other unit testing frameworks, each test will be a function of zero arguments so that the framework can run them all in the same way. Each test will create a **fixture** to be tested and use **assertions** to compare the **actual result** against the **expected result**. The outcome can be exactly one of:

*   **Pass**: the **test subject** works as expected.

*   **Fail**: something is wrong with the test subject.

*   **Error**: something is wrong in the test itself, which means we don't know whether the test subject is working properly or not.

To make this work, we need some way to distinguish failing tests from broken ones. Our solution relies on the fact that exceptions are objects and that a program can use **introspection** to determine the class of an object. If a test **throws an exception** whose class is assert.AssertionError, then we will assume the exception came from one of the assertions we put in the test as a check ([Figure 4.1](#chapter4.xhtml_fig4_1)). Any other kind of assertion indicates that the test itself contains an error.

![](images/fig4_1.jpg)

[Figure 4.1:](#chapter4.xhtml_b4fig4_1) Running tests that can pass, fail, or contain errors.

## 4.2 How can we separate registration, execution, and reporting?

To start, let's use a handful of **global variables** to record tests and their results:

![](images/comp04_1.jpg)

We don't run tests immediately because we want to wrap each one in our own **exception handler**. Instead, the function hopeThat saves a descriptive message and a callback function that implements a test in the HopeTest array.

![](images/comp04_2.jpg)

Finally, the function main runs all registered tests:

![](images/comp04_3.jpg)

If a test completes without an exception, it passes. If any of the assert calls inside the test raises an AssertionError, the test fails, and if it raises any other exception, it's an error. After all tests are run, main reports the number of results of each kind.

Let's try it out:

![](images/comp04_4.jpg)![](images/comp04_5.jpg)

This simple “framework” does what it's supposed to, but:

1.  It doesn't tell us which tests have passed or failed.

2.  Those global variables should be consolidated somehow so that it's clear they belong together.

3.  It doesn't discover tests on its own.

4.  We don't have a way to test things that are supposed to raise AssertionError. Putting assertions into code to check that it is behaving correctly is called **defensive programming**; it's a good practice, but we should make sure those assertions are failing when they're supposed to, just as we should test our smoke detectors every once in a while.

## 4.3 How should we structure test registration?

The next version of our testing tool solves the first two problems in the original by putting the testing machinery in a class. It uses the **Singletondesign pattern** to ensure that only one object of that class is ever created [[Osmani2017]](#refbib1.xhtml_refbib_21). Singletons are a way to manage global variables that belong together like the ones we're using to record tests and their results. As an extra benefit, if we decide later that we need several copies of those variables, we can just construct more instances of the class.

The file hope.js defines the class and exports one instance of it:

![](images/comp04_6.jpg)

This strategy relies on two things:

1.  Node[³](#chapter4.xhtml_fn4_3) executes the code in a JavaScript module as it loads it, which means that it runs new Hope() and exports the newly-created object.

2.  Node **caches** modules so that a given module is only loaded once no matter how many times it is imported. This ensures that new Hope() really is only called once.

Once a program has imported hope, it can call Hope.test to record a test for later execution and Hope.run to execute all of the tests registered up until that point ([Figure 4.2](#chapter4.xhtml_fig4_2)).

![](images/fig4_2.jpg)

[Figure 4.2:](#chapter4.xhtml_b4fig4_2) Creating a singleton, recording tests, and running them.

Finally, our Hope class can report results as both a terse one-line summary and as a detailed listing. It can also provide the titles and results of individual tests so that if someone wants to format them in a different way (e.g., as HTML) they can do so:

![](images/comp04_7.jpg)

## 4.4 How can we build a command-line interface for testing?

Most programmers don't enjoy writing tests, so if we want them to do it, we have to make it as painless as possible. A couple of import statements to get assert and hope and then one function call per test is about as simple as we can make the tests themselves:

![](images/comp04_8.jpg)

But that just defines the tests—how will we find them so that we can run them? One option is to require people to import each of the files containing tests into another file:

![](images/comp04_9.jpg)

Here, all-the-tests.js imports other files so that they will register tests as a **side effect** via calls to hope.test and then calls Hope.run to execute them. It works, but sooner or later (probably sooner) someone will forget to import one of the test files.

A better strategy is to load test files **dynamically**. While import is usually written as a statement, it can also be used as an async function that takes a path as a parameter and loads the corresponding file. The program pray.js (shown below) does this; as before, loading files executes the code they contain, which registers tests as a side effect:

![](images/comp04_10.jpg)

By default, this program finds all files below the current working directory whose names match the pattern test-*.js and uses terse output. Since we may want to look for files somewhere else, or request verbose output, the program needs to handle command-line arguments.

The minimist[⁵](#chapter4.xhtml_fn4_5) module does this in a way that is consistent with Unix conventions. Given command-line arguments *after* the program's name (i.e., from process.argv[2] onward), it looks for patterns like -x something and creates an object with flags as keys and values associated with them.

Our **test runner** is now complete, so we can try it out with some files containing tests that pass, fail, and contain errors:

![](images/comp04_11.jpg)![](images/comp04_12.jpg)

Loading modules dynamically so that they can register something for us to call later is a common pattern in many programming languages. Control flow goes back and forth between the framework and the module being loaded as this happens so we must specify the **lifecycle** of the loaded modules quite carefully. [Figure 4.3](#chapter4.xhtml_fig4_3) illustrates what happens when a pair of files test-add.js and test-sub.js are loaded by our framework:

1.  pray loads hope.js.

2.  Loading hope.js creates a single instance of the class Hope.

3.  pray uses glob to find files with tests.

4.  pray loads test-add.js using import as a function.

5.  As test-add.js runs, it loads hope.js. Since hope.js is already loaded, this does not create a new instance of Hope.

6.  test-add.js uses hope.test to register a test (which does not run yet).

7.  pray then loads test-sub.js…

8.  …which loads Hope…

9.  …then registers a test.

10.  pray can now ask the unique instance of Hope to run all of the tests, then get a report from the Hope singleton and display it.

![](images/fig4_3.jpg)

[Figure 4.3:](#chapter4.xhtml_b4fig4_3) Lifecycle of dynamically-discovered unit tests.

## 4.5 Exercises

### Asynchronous globbing

Modify pray.js to use the asynchronous version of glob rather than glob.sync.

### Timing tests

Install the microtime[⁶](#chapter4.xhtml_fn4_6) package and then modify the dry-run.js example so that it records and reports the execution times for tests.

### Approximately equal

1.  Write a function assertApproxEqual that does nothing if two values are within a certain tolerance of each other but throws an exception if they are not:

    ![](images/comp04_14.jpg)
2.  Modify the function so that a default tolerance is used if none is specified:

    ![](images/comp04_15.jpg)
3.  Modify the function again so that it checks the **relative error** instead of the **absolute error**. (The relative error is the absolute value of the difference between the actual and expected value, divided by the absolute value.)

### Rectangle overlay

A windowing application represents rectangles using objects with four values: x and y are the coordinates of the lower-left corner, while w and h are the width and height. All values are non-negative: the lower-left corner of the screen is at (0, 0) and the screen's size is WIDTHxHEIGHT.

1.  Write tests to check that an object represents a valid rectangle.

2.  The function overlay(a, b) takes two rectangles and returns either a new rectangle representing the region where they overlap or null if they do not overlap. Write tests to check that overlay is working correctly.

3.  Do your tests assume that two rectangles that touch on an edge overlap or not? What about two rectangles that only touch at a single corner?

### Selecting tests

Modify pray.js so that if the user provides -s pattern or --select pattern then the program only runs tests in files that contain the string pattern in their name.

### Tagging tests

Modify hope.js so that users can optionally provide an array of strings to tag tests:

![](images/comp04_16.jpg)

Then modify pray.js so that if users specify either -t tagName or --tag tagName only tests with that tag are run.

### Mock objects

A mock object is a simplified replacement for part of a program whose behavior is easier to control and predict than the thing it is replacing. For example, we may want to test that our program does the right thing if an error occurs while reading a file. To do this, we write a function that wraps fs.readFileSync:

![](images/comp04_17.jpg)

and then modify it so that it throws an exception under our control. For example, if we define MOCK_READ_FILE_CONTROL like this:

![](images/comp04_18.jpg)

then the third and fifth calls to mockReadFileSync throw an exception instead of reading data, as do any calls after the fifth. Write this function.

### Setup and teardown

Testing frameworks often allow programmers to specify a setup function that is to be run before each test and a corresponding teardown function that is to be run after each test. (setup usually re-creates complicated test fixtures, while teardown functions are sometimes needed to clean up after tests, e.g., to close database connections or delete temporary files.)

Modify the testing framework in this chapter so that if a file of tests contains something like this:

![](images/comp04_19.jpg)

then the function createFixtures will be called exactly once before each test in that file. Add a similar way to register a teardown function with hope.teardown.

### Multiple tests

Add a method hope.multiTest that allows users to specify multiple test cases for a function at once. For example, this:

![](images/comp04_20.jpg)

should be equivalent to this:

![](images/comp04_21.jpg)

### Assertions for sets and maps

1.  Write functions assertSetEqual and assertMapEqual that check whether two instances of Set or two instances of Map are equal.

2.  Write a function assertArraySame that checks whether two arrays have the same elements, even if those elements are in different orders.

### Testing promises

Modify the unit testing framework to handle async functions, so that:

![](images/comp04_22.jpg)

does the right thing. (Note that you can use typeof to determine whether the object given to hope.test is a function or a promise.)

# 5File Backup

Terms defined: **[Application Programming Interface](#appendix5.xhtml_d12)**, **[collision](#appendix5.xhtml_d54)**, **[comma-separated values](#appendix5.xhtml_d57)**, **[Coordinated Universal Time](#appendix5.xhtml_d67)**, **[cryptographic hash function](#appendix5.xhtml_d70)**, **[data migration](#appendix5.xhtml_d74)**, **[handler](#appendix5.xhtml_d130)**, **[hash code](#appendix5.xhtml_d131)**, **[hash function](#appendix5.xhtml_d132)**, **JavaScript Object Notation**, **[mock object](#appendix5.xhtml_d186)**, **[pipe](#appendix5.xhtml_d211)**, **[race condition](#appendix5.xhtml_d228)**, **[SHA-1 hash](#appendix5.xhtml_d250)**, **[stream](#appendix5.xhtml_d268)**, **[streaming API](#appendix5.xhtml_d269)**, **Time of check/time of use**, **[timestamp](#appendix5.xhtml_d284)**, **[version control system](#appendix5.xhtml_d298)**

Now that we can test software, we have something worth saving. A **version control system** like Git[¹](#chapter5.xhtml_fn5_1) keeps track of changes to files so that we can recover old versions if we want to. Its core is a way to archive files that:

1.  records which versions of which files existed at the same time (so that we can go back to a consistent previous state), and

2.  stores any particular version of a file only once, so that we don't waste disk space.

In this chapter we will build a tool for doing both tasks. It won't do everything Git does: in particular, it won't let us create and merge branches. If you would like to know how that works, please see Mary Rose Cook's[²](#chapter5.xhtml_fn5_2) excellent Gitlet[³](#chapter5.xhtml_fn5_3) project.

## 5.1 How can we uniquely identify files?

To avoid storing redundant copies of files, we need a way to tell when two files contain the same data. We can't rely on names because files can be renamed or moved over time; we could compare the files byte-by-byte, but a quicker way is to use a **hash function** that turns arbitrary data into a fixed-length string of bits ([Figure 5.1](#chapter5.xhtml_fig5_1)).

![](images/fig5_1.jpg)

[Figure 5.1:](#chapter5.xhtml_b5fig5_1) How hash functions speed up lookup.

A hash function always produces the same **hash code** for a given input. A **cryptographic hash function** has two extra properties:

1.  The output depends on the entire input: changing even a single byte results in a different hash code.

2.  The outputs look like random numbers: they are unpredictable and evenly distributed (i.e., the odds of getting any specific hash code are the same).

It's easy to write a bad hash function, but very hard to write one that qualifies as cryptographic. We will therefore use a library to calculate 160-bit **SHA-1** hashes for our files. These are not random enough to keep data secret from a patient, well-funded attacker, but that's not what we're using them for: we just want hashes that are random to make **collision** extremely unlikely.

Node's[⁶](#chapter5.xhtml_fn5_6) crypto[⁷](#chapter5.xhtml_fn5_7) module provides tools to create a SHA-1 hash. To use them, we create an object that keeps track of the current state of the hashing calculations, tell it how we want to encode (or represent) the hash value, and then feed it some bytes. When we are done, we call its .end method and then use its .read method to get the final result:

![](images/comp05_1.jpg)![](images/comp05_2.jpg)![](images/comp05_3.jpg)

Hashing a file instead of a fixed string is straightforward: we just read the file's contents and pass those characters to the hashing object:

![](images/comp05_4.jpg)![](images/comp05_5.jpg)![](images/comp05_6.jpg)

However, it is more efficient to process the file as a **stream**:

![](images/comp05_7.jpg)![](images/comp05_8.jpg)![](images/comp05_9.jpg)

This kind of interface is called a **streamingAPI** because it is designed to process a stream of data one chunk at a time rather than requiring all of the data to be in memory at once. Many applications use streams so that programs don't have to read entire (possibly large) files into memory.

To start, this program asks the fs library to create a reading stream for a file and to **pipe** the data from that stream to the hashing object ([Figure 5.2](#chapter5.xhtml_fig5_2)). It then tells the hashing object what to do when there is no more data by providing a **handler** for the “finish” event. This is called asynchronously: as the output shows, the main program ends before the task handling the end of data is scheduled and run. Most programs also provide a handler for “data” events to do something with each block of data as it comes in; the hash object in our program does that for us.

![](images/fig5_2.jpg)

[Figure 5.2:](#chapter5.xhtml_b5fig5_2) Processing files as streams of chunks.

## 5.2 How can we back up files?

Many files only change occasionally after they're created, or not at all. It would be wasteful for a version control system to make copies each time the user wanted to save a snapshot of a project, so instead our tool will copy each unique file to something like abcd1234.bck, where abcd1234 is a hash of the file's contents. It will then store a data structure that records the filenames and hash keys for each snapshot. The hash keys tell it which unique files are part of the snapshot, while the filenames tell us what each file's contents were called when the snapshot was made (since files can be moved or renamed). To restore a particular snapshot, all we have to do is copy the saved .bck files back to where they were ([Figure 5.3](#chapter5.xhtml_fig5_3)).

![](images/fig5_3.jpg)

[Figure 5.3:](#chapter5.xhtml_b5fig5_3) Organization of backup file storage.

We can build the tools we need to do this using promises ([Chapter 3](#chapter3.xhtml)). The main function creates a promise that uses the asynchronous version of glob to find files and then:

1.  checks that entries in the list are actually files;

2.  reads each file into memory; and

3.  calculates hashes for those files.

![](images/comp05_10.jpg)

This function uses Promise.all to wait for the operations on all of the files in the list to complete before going on to the next step. A different design would combine stat, read, and hash into a single step so that each file would be handled independently and use one Promise.all at the end to bring them all together.

The first two helper functions that hashExisting relies on wrap asynchronous operation in promises:

![](images/comp05_11.jpg)

The final helper function calculates the hash synchronously, but we can use Promise.all to wait on those operations finishing anyway:

![](images/comp05_12.jpg)

Let's try running it:

![](images/comp05_13.jpg)![](images/comp05_14.jpg)![](images/comp05_15.jpg)

The code we have written is clearer than it would be with callbacks (try rewriting it if you don't believe this) but the layer of promises around everything still obscures its meaning. The same operations are easier to read when written using async and await:

![](images/comp05_16.jpg)

This version creates and resolves exactly the same promises as the previous one, but those promises are created for us automatically by Node. To check that it works, let's run it for the same input files:

![](images/comp05_17.jpg)![](images/comp05_18.jpg)![](images/comp05_19.jpg)

## 5.3 How can we track which files have already been backed up?

The second part of our backup tool keeps track of which files have and haven't been backed up already. It stores backups in a directory that contains backup files like abcd1234.bck and files describing the contents of particular snapshots. The latter are named ssssssssss.csv, where ssssssssss is the **UTCtimestamp** of the backup's creation and the .csv extension indicates that the file is formatted as **comma-separated values**. (We could store these files as **JSON**, but CSV is easier for people to read.)

![](images/comp05_20.jpg)

To test our program, let's manually create testing directories with manufactured (shortened) hashes:

![](images/comp05_21.jpg)![](images/comp05_22.jpg)

We use Mocha[⁸](#chapter5.xhtml_fn5_8) to manage our tests. Every test is an async function; Mocha automatically waits for them all to complete before reporting results. To run them, we add the line:

![](images/comp05_23.jpg)

in the scripts section of our project's package.json file so that when we run npm run test, Mocha looks for files in test sub-directories of the directories holding our lessons.

Here are our first few tests:

![](images/comp05_24.jpg)

and here is Mocha's report:

![](images/comp05_25.jpg)

## 5.4 How can we test code that modifies files?

The final thing our tool needs to do is copy the files that need copying and create a new index file. The code itself will be relatively simple, but testing will be complicated by the fact that our tests will need to create directories and files before they run and then delete them afterward (so that they don't contaminate subsequent tests).

A better approach is to use a **mock object** instead of the real filesystem. A mock object has the same interface as the function, object, class, or library that it replaces, but is designed to be used solely for testing. Node's mock-fs[⁹](#chapter5.xhtml_fn5_9) library provides the same functions as the fs library, but stores everything in memory ([Figure 5.4](#chapter5.xhtml_fig5_4)). This prevents our tests from accidentally disturbing the filesystem, and also makes tests much faster (since in-memory operations are thousands of times faster than operations that touch the disk).

![](images/fig5_4.jpg)

[Figure 5.4:](#chapter5.xhtml_b5fig5_4) Using a mock filesystem to simplify testing.

We can create a mock filesystem by giving the library a JSON description of the files and what they should contain:

![](images/comp05_26.jpg)

Mocha automatically calls beforeEach before running each tests, and afterEach after each tests completes (which is yet another protocol). All of the tests stay exactly the same, and since mock-fs replaces the functions in the standard fs library with its own, nothing in our application needs to change either.

We are finally ready to write the program that actually backs up files:

![](images/comp05_27.jpg)

The tests for this are more complicated than tests we have written previously because we want to check with actual file hashes. Let's set up some fixtures to run tests on:

![](images/comp05_28.jpg)

and then run some tests:

![](images/comp05_29.jpg)![](images/comp05_29_2.jpg)![](images/comp05_30.jpg)

## 5.5 Exercises

### Odds of collision

If hashes were only 2 bits long, then the chances of collision with each successive file assuming no previous collision are:

| **Number of Files** | **Odds of Collision** |
| 1 | 0% |
| 2 | 25% |
| 3 | 50% |
| 4 | 75% |
| 5 | 100% |

A colleague of yours says this means that if we hash four files, there's only a 75% chance of any collision occurring. What are the actual odds?

### Streaming I/O

Write a small program using fs.createReadStream and fs.createWriteStream that copies a file piece-by-piece instead of reading it into memory and then writing it out again.

### Sequencing backups

Modify the backup program so that manifests are numbered sequentially as 00000001.csv, 00000002.csv, and so on rather than being timestamped. Why doesn't this solve the time of check/time of use race condition mentioned earlier?

### JSON manifests

1.  Modify backup.js so that it can save JSON manifests as well as CSV manifests based on a command-line flag.

2.  Write another program called migrate.js that converts a set of manifests from CSV to JSON. (The program's name comes from the term **data migration**.)

3.  Modify backup.js programs so that each manifest stores the user name of the person who created it along with file hashes, and then modify migrate.js to transform old files into the new format.

### Mock hashes

1.  Modify the file backup program so that it uses a function called ourHash to hash files.

2.  Create a replacement that returns some predictable value, such as the first few characters of the data.

3.  Rewrite the tests to use this function.

How did you modify the main program so that the tests could control which hashing function is used?

### Comparing manifests

Write a program compare-manifests.js that reads two manifest files and reports:

*   Which files have the same names but different hashes (i.e., their contents have changed).

*   Which files have the same hashes but different names (i.e., they have been renamed).

*   Which files are in the first hash but neither their names nor their hashes are in the second (i.e., they have been deleted).

*   Which files are in the second hash but neither their names nor their hashes are in the first (i.e., they have been added).

### From one state to another

1.  Write a program called from-to.js that takes the name of a directory and the name of a manifest file as its command-line arguments, then adds, removes, and/or renames files in the directory to restore the state described in the manifest. The program should only perform file operations when it needs to, e.g., it should not delete a file and re-add it if the contents have not changed.

2.  Write some tests for from-to.js using Mocha and mock-fs.

### File history

1.  Write a program called file-history.js that takes the name of a file as a command-line argument and displays the history of that file by tracing it back in time through the available manifests.

2.  Write tests for your program using Mocha and mock-fs.

### Pre-commit hooks

Modify backup.js to load and run a function called preCommit from a file called pre-commit.js stored in the root directory of the files being backed up. If preCommit returns true, the backup proceeds; if it returns false or throws an exception, no backup is created.

# 6Data Tables

Terms defined: **character encoding**, **column-major storage**, **[data frame](#appendix5.xhtml_d73)**, **[fixed-width (of strings)](#appendix5.xhtml_d119)**, **[garbage collection](#appendix5.xhtml_d123)**, **[heterogeneous](#appendix5.xhtml_d135)**, **[homogeneous](#appendix5.xhtml_d137)**, **[immutable](#appendix5.xhtml_d144)**, **index (in a database)**, **JavaScript Object Notation**, **[join](#appendix5.xhtml_d158)**, **[pad (a string)](#appendix5.xhtml_d202)**, **row-major storage**, **[sparse matrix](#appendix5.xhtml_d260)**, **[SQL](#appendix5.xhtml_d261)**, **[tagged data](#appendix5.xhtml_d275)**, **[test harness](#appendix5.xhtml_d277)**

[Chapter 2](#chapter2.xhtml) said that operations in memory are thousands of times faster than operations that touch the filesystem, but what about different in-memory operations—how do they compare with each other? Putting it another way, how can we tell which of several designs is going to be the most efficient?

The best answer is to conduct some experiments. To see how to do this, we will take a look at several ways to implement data tables with one or more named columns and zero or more rows. Each row has one value for each column, and all the values in a column have the same type ([Figure 6.1](#chapter6.xhtml_fig6_1)). Data tables appear over and over again in programming, from spreadsheets and databases to the **data frames** in R's tidyverse[¹](#chapter6.xhtml_fn6_1) packages, Python's[²](#chapter6.xhtml_fn6_2) Pandas[³](#chapter6.xhtml_fn6_3) library, or the DataForge[⁴](#chapter6.xhtml_fn6_4) library for JavaScript [[Davis2018]](#refbib1.xhtml_refbib_8).

![](images/fig6_1.jpg)

[Figure 6.1:](#chapter6.xhtml_b6fig6_1) The structure of a data table.

The key operations on data tables are those provided by **SQL**: filter, select, summarize, and join. These can be implemented in about 500 lines of code, but their performance depends on how the data table is stored.

## 6.1 How can we implement data tables?

One way to store a table is **row-major** order, in which the values in each row are stored together in memory. This is sometimes also called **heterogeneous** storage because each “unit” of storage can contain values of different types. We can implement this design in JavaScript using an array of objects, each of which has the same keys ([Figure 6.2](#chapter6.xhtml_fig6_2)).

![](images/fig6_2.jpg)

[Figure 6.2:](#chapter6.xhtml_b6fig6_2) Row-major storage vs. column-major storage for data tables.

Another option is **column-major** or **homogeneous** order, in which all the values in a column are stored together. In JavaScript, this could be implemented using an object whose members are all arrays of the same length.

To find out which is better we will construct one of each, try some operations, record their execution times and memory use, and then compare them. Crucially, the answer will depend on both the implementations themselves and on what mix of operations we measure. For example, if one strategy works better for filter and another for select, the ratio of filters to selects may determine which is “best”.

For our first experiment, let's build a row-major table with some number of columns. To keep it simple, we will use the row indexes to fill the table:

![](images/comp06_1.jpg)

Next, we write filter and select for tables laid out this way. We need to provide a callback function to filter to determine which rows to keep like the callback for Array.filter; for selecting columns, we provide a list of the keys that identify the columns we want to keep. We expect filtering to be relatively fast, since it is recycling rows, while selecting should be relatively slow because we have to construct a new set of arrays ([Figure 6.3](#chapter6.xhtml_fig6_3)).

![](images/comp06_2.jpg)![](images/fig6_3.jpg)

[Figure 6.3:](#chapter6.xhtml_b6fig6_3) Operations on row-major data tables.

Now let's do the same for column-major storage. Building the object that holds the columns is straightforward:

![](images/comp06_3.jpg)

Filtering is more complex because the values in each row are scattered across several arrays, but selecting is just a matter of recycling the arrays we want in the new table. We expect selecting to be relatively fast, since only the references to the columns need to be copied, but filtering will be relatively slow since we are constructing multiple new arrays ([Figure 6.4](#chapter6.xhtml_fig6_4)). Note that this code assumes there is a column called label_1 that it can look at to find out how many rows there are in the table. This would be a horrible thing to put into production, but is good enough for some simple performance testing.

![](images/comp06_4.jpg)![](images/fig6_4.jpg)

[Figure 6.4:](#chapter6.xhtml_b6fig6_4) Operations on column-major data tables.

## 6.2 How can we test the performance of our implementations?

Now that we have our tables and operations, we can build a **test harness** to run those operations on data tables of varying sizes. We arbitrarily decide to keep half of the columns and one-third of the rows; these ratios will affect our decision about which is better, so if we were doing this for a real application we would test what happens as these fractions vary. And as we said earlier, the relative performance will also depend on how many filters we do for each select; our balance should be based on data from whatever application we intend to support.

Our performance measurement program looks like this:

![](images/comp06_5.jpg)

The functions that actually do the measurements use the microtime[⁵](#chapter6.xhtml_fn6_5) library to get microsecond level timing because JavaScript's Date only gives us millisecond-level resolution. We use object-sizeof[⁶](#chapter6.xhtml_fn6_6) to estimate how much memory our structures require; we also call process.memoryUsage() and look at the heapUsed value to see how much memory Node[⁷](#chapter6.xhtml_fn6_7) is using while the program runs, but that may be affected by **garbage collection** and a host of other factors outside our control.

![](images/comp06_6.jpg)

Let's run our program for a table with 100 rows and 3 columns and a 3:1 ratio of filter to select:

![](images/comp06_7.jpg)![](images/comp06_8.jpg)

What if we increase the table size to 10,000 rows by 30 columns with the same 3:1 filter/select ratio?

![](images/comp06_9.jpg)

And what if we keep the table size the same but use a 10:1 filter/select ratio?

![](images/comp06_10.jpg)

The results in [Table 6.1](#chapter6.xhtml_tbl6_1) show that column-major storage is better. It uses less memory (presumably because column labels aren't duplicated once per row) and the time required to construct new objects when doing select with row-major storage outweighs cost of appending to arrays when doing filter with column-major storage. Unfortunately, the code for column-major storage is a little more complicated to write, which is a cost that doesn't show up in experiments.

[Table 6.1:](#chapter6.xhtml_b6tbl6_1) Relative performance of operations on row-major and column-major data tables.

| **value** | **100-03-03** | **10000-30-03** | **10000-30-10** |
| nRows | 100 | 10000 | 10000 |
| nCols | 3 | 30 | 30 |
| filterPerSelect | 3 | 3 | 10 |
| rowFilterTime | 75 | 2929 | 2376 |
| rowSelectTime | 111 | 15863 | 15566 |
| colFilterTime | 137 | 4529 | 4380 |
| colSelectTime | 48 | 104 | 90 |

## 6.3 What is the most efficient way to save a table?

Data is valuable, so we are going to store data tables in files of some kind. If one storage scheme is much more efficient than another and we are reading or writing frequently, that could change our mind about which implementation to pick.

Two simple text-based schemes are row-oriented and column-oriented **JSON**—basically, just printing the data structures we have. Let's run the 10,000×30 test:

![](images/comp06_11.jpg)

The time needed for the row-major version is almost ten times greater than that needed for the column-major version; we assume that the redundant printing of the labels is mostly to blame, just as redundant storage of the labels was to blame for row-major's greater memory requirements.

If that diagnosis is correct, then a packed version of row-major storage ought to be faster. We save the column headers once, then copy the data values into an array of arrays and save that:

![](images/comp06_12.jpg)![](images/comp06_13.jpg)

These results show that changing layout for storage is faster than turning the data structure we have into a string. Again, we assume this is because copying data takes less time than turning labels into strings over and over, but column-major storage is still the best approach.

## 6.4 Does binary storage improve performance?

Let's try one more strategy for storing our tables. JavaScript stores values in **tagged** data structures: some bits define the value's type while other bits store the value itself in a type-dependent way ([Figure 6.5](#chapter6.xhtml_fig6_5)).

![](images/fig6_5.jpg)

[Figure 6.5:](#chapter6.xhtml_b6fig6_5) How JavaScript uses tagged data structures to store objects.

We can save space by keeping track of the types ourselves and just storing the bits that represent the values. JavaScript has an ArrayBuffer class for exactly this purpose. It stores any value we want as a set of bits; we then access those bits through a view that presents the data as a particular type, such as Boolean (one byte per value) or number (64 bits per number). As [Figure 6.6](#chapter6.xhtml_fig6_6) shows, we can mix different types of data in a single ArrayBuffer, but it's up to us to keep track of which bytes belong to which values.

![](images/fig6_6.jpg)

[Figure 6.6:](#chapter6.xhtml_b6fig6_6) Storing object values as bits with lookup information.

To store a column-major table we will fill an ArrayBuffer with:

1.  Two integers that hold the table's size (number of rows and number of columns).

2.  A string with the column labels joined by newline characters. (We use newlines as a separator because we assume column labels can't contain them.)

3.  The numbers themselves.

![](images/comp06_14.jpg)![](images/comp06_15.jpg)

Packing the data table saves time because copying bits is faster than turning numbers into characters, but it doesn't save as much space as expected. The reason is that double-precision numbers are 8 bytes long, but because we have chosen simple integer values for our tests, they can be represented by just 5 characters (which is 10 bytes). If we had “real” numbers the storage benefit would probably be more pronounced; once again, the result of our experiment depends on the test cases we choose.

## 6.5 Exercises

### Varying filter behavior

How does our decision about which storage format is better change if we keep 1% of rows when filtering instead of one-third? What if we keep 90% of rows?

### Filtering by strings

Modify the comparison of filter and select to work with tables that contain columns of strings instead of columns of numbers and see how that changes performance. For testing, create random 4-letter strings using the characters A-Z and then filter by:

*   an exact match,

*   strings starting with a specific character, and

*   strings that contain a specific character.

### Join performance

A join combines data from two tables based on matching keys. For example, if the two tables are:

| **[Key](#appendix5.xhtml_d159)** | **Left** |
| A | a1 |
| B | b1 |
| C | c1 |

and:

| **Key** | **Right** |
| A | a2 |
| A | a3 |
| B | b2 |

then the join is:

| **Key** | **Left** | **Right** |
| A | a1 | a2 |
| A | a1 | a3 |
| B | b1 | b2 |

Write a test to compare the performance of row-wise vs. column-wise storage when joining two tables based on matching numeric keys. Does the answer depend on the fraction of keys that match?

### Join optimization

The simplest way to **join** two tables is to look for matching keys using a double loop. An alternative is to build an **index** for each table and then use it to construct matches. For example, suppose the tables are:

| **Key** | **Left** |
| A | a1 |
| B | b1 |
| C | c1 |

and:

| **Key** | **Right** |
| A | a2 |
| A | a3 |
| B | b2 |

The first step is to create a Map showing where each key is found in the first table:

![](images/comp06_16.jpg)

The second step is to create a similar Map for the second table:

![](images/comp06_17.jpg)

We can then loop over the keys in one of the maps, look up values in the second map, and construct all of the matches.

Write a function that joins two tables this way. Is it faster or slower than using a double loop? How does the answer depend on the number of keys and the fraction that match?

### Flipping storage

Our tests showed that storing row-oriented tables as JSON is much slower than storing column-oriented tables. Write a test to determine whether converting a row-oriented table to a column-oriented table and then saving the latter is faster than saving the row-oriented table directly.

### Sparse storage

A **sparse matrix** is one in which most of the values are zero. Instead of storing them all, a program can use a map to store non-zero values and a lookup function to return zero for anything that isn't stored explicitly:

![](images/comp06_18.jpg)

The same technique can be used if most of the entries in a data table are missing. Write a function that creates a sparse table in which a random 5% of the values are non-zero and the other 95% are zero, then compare the memory requirements and performance of filter and select for this implementation versus those of row-wise and column-wise storage.

### Loading time

Modify the programs in this section to measure the time required to convert a data table from JSON or binary form back to a data structure.

### Saving fixed-width strings

To improve performance, databases often store **fixed-width** strings, i.e., they limit the length of the strings in a column to some fixed size and **pad** strings that are shorter than that.

1.  Write a function that takes an array of strings and an integer width and creates an ArrayBuffer containing the strings padded to that width. The function should throw an exception if any of the strings are longer than the specified width.

2.  Write another function that takes an ArrayBuffer as input and returns an array of strings. This function should remove the padding so that strings shorter than the fixed width are restored to their original form.

### Saving variable-width strings

**Fixed-width** storage is inefficient for large blocks of text such as contracts, novels, and resumés, since padding every document to the length of the longest will probably waste a lot of space. An alternative way to store these in binary is to save each entry as a (length, text) pair.

1.  Write a function that takes a list of strings as input and returns an ArrayBuffer containing (length, text) pairs.

2.  Write another function that takes such an ArrayBuffer and returns an array containing the original text.

3.  Write tests with Mocha to confirm that your functions work correctly.

### [ASCII](#appendix5.xhtml_d14) storage

The original ASCII standard specified a 7-bit **character encoding** for letters commonly used in English, and many data files still only use characters whose numeric codes are in the range 0–127.

1.  Write a function that takes an array of single-letter strings and returns an ArrayBuffer that stores them using one byte per character if all of the characters will fit into 7 bits, and multiple bytes per character if any of the characters require more than 7 bits.

2.  Write another function that takes an ArrayBuffer generated by the first function and re-creates the array of characters. The function must *only* take the ArrayBuffer as an argument, so the first element of the ArrayBuffer should indicate how to interpret the rest of its contents.

3.  Write tests with Mocha to check that your functions work correctly.

# 7Pattern Matching

Terms defined: **[base class](#appendix5.xhtml_d24)**, **[Chain of Responsibility pattern](#appendix5.xhtml_d44)**, **[child (in a tree)](#appendix5.xhtml_d46)**, **[coupling](#appendix5.xhtml_d69)**, **[depth-first](#appendix5.xhtml_d80)**, **[derived class](#appendix5.xhtml_d24)**, **[Document Object Model](#appendix5.xhtml_d91)**, **[eager matching](#appendix5.xhtml_d96)**, **[greedy algorithm](#appendix5.xhtml_d129)**, **[lazy matching](#appendix5.xhtml_d162)**, **[node](#appendix5.xhtml_d193)**, **[Open-Closed Principle](#appendix5.xhtml_d199)**, **[polymorphism](#appendix5.xhtml_d214)**, **query selector**, **[regular expression](#appendix5.xhtml_d233)**, **[scope creep](#appendix5.xhtml_d244)**, **test-driven development**

We have been globbing to match filenames against patterns since [Chapter 2](#chapter2.xhtml). This lesson will explore how that works by building a simple version of the **regular expressions** used to match text in everything from editor and shell commands to web scrapers. Our approach is inspired by Brian Kernighan's[¹](#chapter7.xhtml_fn7_1) entry in [[Oram2007]](#refbib1.xhtml_refbib_20).

Regular expressions have inspired pattern matching for many other kinds of data, such as **query selectors** for HTML. They are easier to understand and implement than patterns for matching text, so we will start by looking at them.

## 7.1 How can we match query selectors?

Programs stores HTML pages in memory using a **document object model** or DOM. Each element in the page, such as a heading and or paragraph, is a **node**; the **children** of a node are the elements it contains ([Figure 7.1](#chapter7.xhtml_fig7_1)).

![](images/fig7_1.jpg)

[Figure 7.1:](#chapter7.xhtml_b7fig7_1) Representing an HTML document as a tree.

The first step is to define the patterns we want to support ([Table 7.1](#chapter7.xhtml_tbl7_1)). According to this grammar, blockquote#important p.highlight is a highlighted paragraph inside the blockquote whose ID is "important". To find elements in a page that match it, our select function breaks the query into pieces and uses firstMatch to search recursively down the document tree until all the selectors in the query string have matched or no matches have been found ([Figure 7.2](#chapter7.xhtml_fig7_2)).

![](images/comp07_1.jpg)

[Table 7.1:](#chapter7.xhtml_b7tbl7_1) Supported patterns.

| **Meaning** | **Selector** |
| Element with tag "elt" | elt |
| Element with class="cls" | .cls |
| Element with id="ident" | #ident |
| child element inside a parent element | parent child |

![](images/fig7_2.jpg)

[Figure 7.2:](#chapter7.xhtml_b7fig7_2) Matching a simple set of query selectors.

The firstMatch function handles three cases:

1.  This node isn't an element, i.e., it is plain text or a comment. This can't match a selector, and these nodes don't have children, so the function returns null to indicate that matching has failed.

2.  This node matches the current selector. If there aren't any selectors left then the whole pattern must have matched, so the function returns this node as the match. If there *are* more selectors, we try to match those that remain against this node's children and return whatever result that produces.

3.  This node *doesn't* match the current selector, so we search the children one by one to see if there is a match further down.

This algorithm is called **depth-first search**: it explores one possible match to the end before considering any others. firstMatch relies on a helper function called firstChildMatch, which finds the first child of a node to match a set of selectors:

![](images/comp07_2.jpg)

and on the function matchHere which compares a node against a selector:

![](images/comp07_3.jpg)

This version of matchHere is simple but inefficient, since it breaks the selector into parts each time it is called rather than doing that once and re-using the results. We will build a more efficient version in the exercises, but let's try out the one we have. Our test cases are all in one piece of HTML:

![](images/comp07_4.jpg)

The program contains a table of queries and the expected matches. The function main loops over it to report whether each test passes or fails:

![](images/comp07_5.jpg)

main uses a helper function called getText to extract text from a node or return an error message if something has gone wrong:

![](images/comp07_6.jpg)

When we run our program it produces this result:

![](images/comp07_7.jpg)

We will rewrite these tests using Mocha[²](#chapter7.xhtml_fn7_2) in the exercises.

## 7.2 How can we implement a simple regular expression matcher?

Matching regular expressions against text relies on the same recursive strategy as matching query selectors against nodes in an HTML page. If the first element of the pattern matches where we are, we see if the rest of the pattern matches what's left; otherwise, we see if the the pattern will match further along. Our matcher will initially handle just the five cases shown in [Table 7.2](#chapter7.xhtml_tbl7_2). These cases are a small subset of what JavaScript provides, but as Kernighan wrote, “This is quite a useful class; in my own experience of using regular expressions on a day-to-day basis, it easily accounts for 95 percent of all instances.”

[Table 7.2:](#chapter7.xhtml_b7tbl7_2) Pattern matching cases.

| **Meaning** | **Character** |
| Any literal character *c* | *c* |
| Any single character | . |
| Beginning of input | ^ |
| End of input | $ |
| Zero or more of the previous character | * |

The top-level function that users call handles the special case of ^ at the start of a pattern matching the start of the target string being searched. It then tries the pattern against each successive substring of the target string until it finds a match or runs out of characters:

![](images/comp07_8.jpg)

matchHere does the matching and recursing:

![](images/comp07_9.jpg)

Once again, we use a table of test cases and expected results to test it:

![](images/comp07_10.jpg)![](images/comp07_11.jpg)

This program seems to work, but it actually contains an error that we will correct in the exercises. (Think about what happens if we match the pattern /a*ab/ against the string ’aab’.) Our design is also hard to extend: handling parentheses in patterns like /a(bc)*d/ will require major changes. We need to explore a different approach.

## 7.3 How can we implement an extensible matcher?

Instead of packing all of our code into one long function, we can implement each kind of match as a separate function. Doing this makes it much easier to add more matchers: we just define a function that we can mix in with calls to the ones we already have.

Rather than having these functions do the matching immediately, though, we will have each one return an object that knows how to match itself against some text. Doing this allows us to build a complex match once and re-use it many times. This is a common pattern in text processing: we may want to apply a regular expression to each line in a large set of files, so recycling the matchers will make our programs more efficient.

Each matching object has a method that takes the target string and the index to start matching at as inputs. Its output is the index to continue matching at or undefined indicating that matching failed. We can then combine these objects to match complex patterns ([Figure 7.3](#chapter7.xhtml_fig7_3)).

![](images/fig7_3.jpg)

[Figure 7.3:](#chapter7.xhtml_b7fig7_3) Using nested objects to match regular expressions.

The first step in implementing this is to write test cases, which forces us to define the syntax we are going to support:

![](images/comp07_12.jpg)

Next, we define a **base class** that all matchers will inherit from. This class contains the match method that users will call so that we can start matching right away no matter what kind of matcher we have at the top level of our pattern.

![](images/comp07_13.jpg)

The base class also defines a _ match method (with a leading underscore) that other classes will fill in with actual matching code. The base implementation of this method throws an exception so that if we forget to provide _ match in a **derived class** our code will fail with a meaningful reminder.

We can now define empty versions of each matching class that all say “no match here” like this one for literal characters:

![](images/comp07_14.jpg)

Our tests now run, but most of them fail: “most” because we expect some tests not to match, so the test runner reports true.

![](images/comp07_15.jpg)

This output tells us how much work we have left to do: when all of these tests pass, we're finished.

Let's implement a literal character string matcher first:

![](images/comp07_16.jpg)

Some tests now pass, others still fail as expected:

![](images/comp07_17.jpg)

We will tackle RegexSeq next so that we can combine other matchers. This is why we have tests for Seq(Lit(’a’), Lit(’b’)) and Lit(’ab’): all children have to match in order without gaps.

But wait: suppose we have the pattern /a*ab/. This ought to match the text "ab", but will it? The /*/ is **greedy**: it matches as much as it can (which is also called **eager matching**). As a result, /a*/ will match the leading "a", leaving nothing for the literal /a/ to match ([Figure 7.4](#chapter7.xhtml_fig7_4)). Our current implementation doesn't give us a way to try other possible matches when this happens.

![](images/fig7_4.jpg)

[Figure 7.4:](#chapter7.xhtml_b7fig7_4) Why overly greedy matching doesn't work.

Let's re-think our design and have each matcher take its own arguments and a rest parameter containing the rest of the matchers ([Figure 7.5](#chapter7.xhtml_fig7_5)). (We will provide a default of null in the creation function so we don't have to type null over and over again.) Each matcher will try each of its possibilities and then see if the rest will also match.

![](images/fig7_5.jpg)

[Figure 7.5:](#chapter7.xhtml_b7fig7_5) Using rest to match the remainder of a pattern.

This design means we can get rid of RegexSeq, but it does make our tests a little harder to read:

![](images/comp07_18.jpg)

Here's how this works for matching a literal expression:

![](images/comp07_19.jpg)

The _ match method checks whether all of the pattern matches the target text starting at the current location. If so, it checks whether the rest of the overall pattern matches what's left. Matching the start /^/ and end /$/ anchors is just as straightforward:

![](images/comp07_20.jpg)![](images/comp07_21.jpg)

Matching either/or is done by trying the first pattern and the rest, and if that fails, trying the second pattern and the rest:

![](images/comp07_22.jpg)

To match a repetition, we figure out the maximum number of matches that might be left, then count down until something succeeds. (We start with the maximum because matching is supposed to be greedy.) Each non-empty repetition matches at least one character, so the number of remaining characters is the maximum number of matches worth trying.

![](images/comp07_23.jpg)

With these classes in place, our tests all pass:

![](images/comp07_24.jpg)

The most important thing about this design is how extensible it is: if we want to add other kinds of matching, all we have to do is add more classes. That extensibility comes from the lack of centralized decision-making, which in turn comes from our use of polymorphism and the **Chain of Responsibility** design pattern. Each component does its part and asks something else to handle the remaining work; so long as each component takes the same inputs, we can put them together however we want.

## 7.4 Exercises

### Split once

Modify the query selector code so that selectors like div#id and div.class are only split into pieces once rather than being re-split each time matchHere is called.

### Find and fix the error

The first regular expression matcher contains an error: the pattern ’a*ab’ should match the string ’aab’ but doesn't. Figure out why it fails and fix it.

### Unit tests

Rewrite the tests for selectors and regular expressions to use Mocha.

### Find all with query selectors

Modify the query selector so that it returns *all* matches, not just the first one.

### Select based on attributes

Modify the query selector to handle [attribute="value"] selectors, so that (for example) div[align=center] returns all div elements whose align attribute has the value "center".

### Child selectors

The expression parent > child selects all nodes of type child that are immediate children of nodes of type parent—for example, div > p selects all paragraphs that are immediate children of div elements. Modify simple-selectors.js to handle this kind of matching.

### Find all with regular expressions

Modify the regular expression matcher to return *all* matches rather than just the first one.

### Find one or more with regular expressions

Extend the regular expression matcher to support +, meaning “one or more”.

### Match sets of characters

Add a new regular expression matching class that matches any character from a set, so that Charset(’aeiou’) matches any lower-case vowel.

### Make repetition more efficient

Rewrite RegexAny so that it does not repeatedly re-match text.

### Lazy matching

The regular expressions we have seen so far are **eager**: they match as much as they can, as early as they can. An alternative is **lazy matching**, in which expressions match as little as they need to. For example, given the string "ab", an eager match with the expression /ab*/ will match both letters (because /b*/ matches a ‘b’ if one is available) but a lazy match will only match the first letter (because /b*/ can match no letters at all). Implement lazy matching for the * operator.

### Optional matching

The ? operator means “optional”, so that /a?/ matches either zero or one occurrences of the letter ‘a’. Implement this operator.

# 8Parsing Expressions

Terms defined: **[finite state machine](#appendix5.xhtml_d118)**, **[literal](#appendix5.xhtml_d172)**, **[parser](#appendix5.xhtml_d206)**, **[precedence](#appendix5.xhtml_d217)**, **[token](#appendix5.xhtml_d285)**, **[Turing Machine](#appendix5.xhtml_d290)**, **[well formed](#appendix5.xhtml_d303)**, **[YAML](#appendix5.xhtml_d306)**

In [Chapter 7](#chapter7.xhtml) we created regular expressions by constructing objects. It takes a lot less typing to write them as strings as we did for HTML selectors, but if we're going to do that we need something to convert those strings to the required objects. In other words, we need to write a **parser**.

[Table 8.1](#chapter8.xhtml_tbl8_1) shows the grammar we will handle. When we are done we should be able to parse /^ (a|b|$)*z$/ as “start of text”, “any number of ‘a’, ‘b’, or ‘$’“, “a single ‘z’, and “end of text”. (We write regular expressions inside slashes to distinguish them from strings.) To keep things simple, we will create a tree of objects ([Figure 8.1](#chapter8.xhtml_fig8_1)) rather than instances of the regular expression classes from [Chapter 7](#chapter7.xhtml); the exercises will tackle the latter.

[Table 8.1:](#chapter8.xhtml_b8tbl8_1) Regular expression grammar.

| **Meaning** | **Character** |
| Any literal character *c* | *c* |
| Beginning of input | ^ |
| End of input | $ |
| Zero or more of the previous thing | * |
| Either/or | — |
| Grouping | (…) |

![](images/fig8_1.jpg)

[Figure 8.1:](#chapter8.xhtml_b8fig8_1) Representing the result of parsing a regular expression as an tree.

## 8.1 How can we break text into tokens?

A **token** is an atom of text, such as the digits making up a number or the letters making up a variable name. In our grammar the tokens are the special characters *, |, (, ), ^, and $, plus any sequence of one or more other characters (which count as one multi-letter token). This classification guides the design of our parser:

1.  If a character is special, create a token for it.

2.  If it is a **literal** then combine it with the current literal if there is one or start a new literal.

3.  Since ^ and $ are either special or regular depending on position, we must treat them as separate tokens or as part of a literal based on where they appear.

We can translate these rules almost directly into code to create a list of objects whose keys are kind and loc (short for location), with the extra key value for literal values:

![](images/comp08_1.jpg)

The helper function combineOrPush does exactly what its name says. If the thing most recently added to the list of tokens isn't a literal, the new character becomes a new token; otherwise, we append the new character to the literal we're building:

![](images/comp08_2.jpg)

We can try this out with a three-line test program:

![](images/comp08_3.jpg)![](images/comp08_4.jpg)

This simple tokenizer is readable, efficient, and wrong. The problem is that the expression /ab*/ means “a single a followed by zero or more b”. If we combine the a and b as we read them, though, we wind up with “zero or more repetitions of ab”. (Don't feel bad if you didn't spot this: we didn't notice the problem until we were implementing the next step.)

The solution is to treat each regular character as its own literal in this stage and then combine things later. Doing this lets us get rid of the nested if for handling ^ and $ as well:

![](images/comp08_5.jpg)

Software isn't done until it's tested, so let's build some Mocha[¹](#chapter8.xhtml_fn8_1) tests for our tokenizer. The listing below shows a few of these along with the output for the full set:

![](images/comp08_6.jpg)![](images/comp08_7.jpg)

## 8.2 How can we turn a list of tokens into a tree?

We now have a list of tokens, but we need a tree that captures the nesting introduced by parentheses and the way that * applies to whatever comes before it. Let's trace a few cases in order to see how to build this tree:

1.  If the regular expression is /a/, we create a Lit token for the letter a (where “create” means “append to the output list”).

2.  What if the regular expression is /a*/? We first create a Lit token for the a and append it to the output list. When we see the *, we take that Lit token off the tail of the output list and replace it with an Any token that has the Lit token as its child.

3.  Our next thought experiment is /(ab)/. We don't know how long the group is going to be when we see the (, so we put the parenthesis onto the output as a marker. We then add the Lit tokens for the a and b until we see the ), at which point we pull tokens off the end of the output list until we get back to the ( marker. When we find it, we put everything we have temporarily collected into a Group token and append it to the output list. This algorithm automatically handles /(a*)/ and /(a(b*)c)/.

4.  What about /a|b/? We append a Lit token for a, get the | and—and we're stuck, because we don't yet have the next token we need to finish building the Alt.

One way to solve this problem is to check if the thing on the top of the stack is waiting to combine each time we append a new token. However, this doesn't handle /a|b*/ properly. The pattern is supposed to mean “one a or any number of b”, but the check-and-combine strategy will turn it into the equivalent of /(a|b)*/.

A better (i.e., correct) solution is to leave some partially-completed tokens in the output and compress them later ([Figure 8.2](#chapter8.xhtml_fig8_2)). If our input is the pattern /a|b/, we can:

1.  Append a Lit token for a.

2.  When we see |, make that Lit token the left child of the Alt and append that without filling in the right child.

3.  Append the Lit token for b.

4.  After all tokens have been handled, look for partially-completed Alt tokens and make whatever comes after them their right child.

![](images/fig8_2.jpg)

[Figure 8.2:](#chapter8.xhtml_b8fig8_2) Mechanics of combining tokens while parsing regular expressions.

Again, this automatically handles patterns like /(ab)|c*|(de)/.

It's time to turn these ideas into code. The main structure of our parser is:

![](images/comp08_8.jpg)

We handle tokens case-by-case (with a few assertions to check that patterns are **well formed**):

![](images/comp08_9.jpg)

When we find the ) that marks the end of a group, we take items from the end of the output list until we find the matching start and use them to create a group:

![](images/comp08_10.jpg)

Finally, when we have finished with the input, we go through the output list one last time to fill in the right side of Alts:

![](images/comp08_11.jpg)

Once again, it's not done until we've tested it:

![](images/comp08_12.jpg)![](images/comp08_13.jpg)

While our final parser is less than 90 lines of code, it is doing a lot of complex things. Compared to parsers for things like JSON and YAML, though, it is still very simple. If we have more operators with different **precedences** we should switch to the shunting-yard algorithm[²](#chapter8.xhtml_fn8_2), and if we need to handle a language like JavaScript we should explore tools like ANTLR[³](#chapter8.xhtml_fn8_3), which can generate a parser automatically given a description of the language to be parsed. As we said at the start, though, if our design requires us to write a parser we should try to come up with a better design. CSV, JSON, YAML, and other formats have their quirks[⁴](#chapter8.xhtml_fn8_4), but at least they're broken the same way everywhere.

![](images/fig8_3.jpg)

[Figure 8.3:](#chapter8.xhtml_b8fig8_3) A finite state machine equivalent to a regular expression.

## 8.3 Exercises

### Create objects

Modify the parser to return instances of classes derived from RegexBase.

### Escape characters

Modify the parser to handle escape characters, so that (for example) ⁢ is interpreted as “a literal asterisk” and \\ is interpreted as “a literal backslash”.

### Lazy matching

Modify the parser so that *? is interpreted as a single token meaning “lazy match zero or more”.

### Character sets

Modify the parser so that expressions like [xyz] are interpreted to mean “match any one of the characters x, y, or z”.

### Back reference

Modify the tokenizer so that it recognizes \ 1, \ 2, and so on to mean “back reference”. The number may contain any number of digits.

### Named groups

1.  Modify the tokenizer to recognize named groups. For example, the named group /(? < triple > aaa)/ would create a named group called triple that matches exactly three consecutive occurrences of ‘a’.

2.  Write Mocha tests for your modified tokenizer. Does it handle nested named groups?

### Object streams

Write a parser that turns files of key-value pairs separated by blank lines into objects. For example, if the input is:

![](images/comp08_14.jpg)

then the output will be:

![](images/comp08_15.jpg)

Keys are always upper- and lower-case characters; values may be strings in double quotes or unquoted numbers.

### Tokenize HTML

1.  Write a tokenizer for a subset of HTML that consists of:

    *   Opening tags without attributes, such as < div > and < p >

    *   Closing tags, such as < /p > and < /div >

    *   Plain text between tags that does *not* contain ‘ > ’ or ‘ < ’ characters

2.  Modify the tokenizer to handle key="value" attributes in opening tags.

3.  Write Mocha tests for your tokenizer.

### The Shunting-Yard Algorithm

1.  Use the shunting-yard algorithm[⁶](#chapter8.xhtml_fn8_6) to implement a tokenizer for a simple subset of arithmetic that includes:

    *   single-letter variable names

    *   single-digit numbers

    *   the +, *, and ^ operators, where + has the lowest precedence and ^ has the highest

2.  Write Mocha tests for your tokenizer.

### Handling errors

1.  What does the regular expression tokenizer do with expressions that contain unmatched opening parentheses like /a(b/? What about expressions that contain unmatched closing parentheses like /ab)/?

2.  Modify it so it produces a more useful error message.

# 9Page Templates

Terms defined: **[bare object](#appendix5.xhtml_d23)**, **[dynamic scoping](#appendix5.xhtml_d95)**, **[environment](#appendix5.xhtml_d103)**, **[lexical scoping](#appendix5.xhtml_d164)**, **[stack frame](#appendix5.xhtml_d262)**, **[static site generator](#appendix5.xhtml_d267)**, **[Visitor pattern](#appendix5.xhtml_d300)**

Every program needs documentation in order to be usable, and the best place to put that documentation is on the web. Writing and updating pages by hand is time-consuming and error-prone, particularly when many parts are the same, so most documentation sites use some kind of **static site generator** to create web pages from templates.

At the heart of every static site generator is a page templating system. Thousands of these have been written in the last thirty years in every popular programming language (and one language, PHP[¹](#chapter9.xhtml_fn9_1), was created for this purpose). Most of these systems use one of three designs ([Figure 9.1](#chapter9.xhtml_fig9_1)):

1.  Mix commands in a language such as JavaScript with the HTML or Markdown using some kind of marker to indicate which parts are commands and which parts are to be taken as-is. This approach is taken by EJS[²](#chapter9.xhtml_fn9_2), which we used to write these lessons.

2.  Create a mini-language with its own commands like Jekyll[³](#chapter9.xhtml_fn9_3) (which is used by GitHub Pages[⁴](#chapter9.xhtml_fn9_4)). Mini-languages are appealing because they are smaller and safer than general-purpose languages, but experience shows that they eventually grow most of the features of a general-purpose language. Again, some kind of marker must be used to show which parts of the page are code and which are ordinary text.

3.  Put directives in specially-named attributes in the HTML. This approach has been the least popular, but since pages are valid HTML, it eliminates the need for a special parser.

![](images/fig9_1.jpg)

[Figure 9.1:](#chapter9.xhtml_b9fig9_1) Three different ways to implement page templating.

In this chapter we will build a simple page templating system using the third strategy. We will process each page independently by parsing the HTML and walking the DOM to find nodes with special attributes. Our program will execute the instructions in those nodes to do the equivalent of loops and if/else statements; other nodes will be copied as-is to create text.

## 9.1 What will our system look like?

Let's start by deciding what “done” looks like. Suppose we want to turn an array of strings into an HTML list. Our page will look like this:

![](images/comp09_1.jpg)

The attribute z-loop tells the tool to repeat the contents of that node; the loop variable and the collection being looped over are separated by a colon. The attribute z-var tells the tool to fill in the node with the value of the variable.

When our tool processes this page, the output will be standard HTML without any traces of how it was created:

![](images/comp09_2.jpg)

The next step is to define the API for filling in templates. Our tool needs the template itself, somewhere to write its output, and some variables to use in the expansion. These variables might come from a configuration file, from a YAML header in the file itself, or from some mix of the two; for the moment, we will just pass them into the expansion function as an object:

![](images/comp09_4.jpg)

## 9.2 How can we keep track of values?

Speaking of variables, we need a way to keep track of their current values; we say “current” because the value of a loop variable changes each time we go around the loop. We also need to maintain multiple sets of variables so that variables used inside a loop don't conflict with ones used outside it. (We don't actually “need” to do this—we could just have one global set of variables—but experience teaches us that if all our variables are global, all of our programs will be buggy.)

The standard way to manage variables is to create a stack of lookup tables. Each **stack frame** is an object with names and values; when we need to find a variable, we look through the stack frames in order to find the uppermost definition of that variable..

The values in a running program are sometimes called an **environment**, so we have named our stack-handling class Env. Its methods let us push and pop new stack frames and find a variable given its name; if the variable can't be found, Env.find returns undefined instead of throwing an exception ([Figure 9.2](#chapter9.xhtml_fig9_2)).

![](images/comp09_5.jpg)![](images/fig9_2.jpg)

[Figure 9.2:](#chapter9.xhtml_b9fig9_2) Using a stack to manage variables.

## 9.3 How do we handle nodes?

HTML pages have a nested structure, so we will process them using the **Visitor** design pattern. Visitor‘s constructor takes the root node of the DOM tree as an argument and saves it. When we call Visitor.walk without a value, it starts recursing from that saved root; if .walk is given a value (as it is during recursive calls), it uses that instead.

![](images/comp09_6.jpg)

Visitor defines two methods called open and close that are called when we first arrive at a node and when we are finished with it (shown for the p node in [Figure 9.3](#chapter9.xhtml_fig9_3)). The default implementations of these methods throw exceptions to remind the creators of derived classes to implement their own versions.

![](images/fig9_3.jpg)

[Figure 9.3:](#chapter9.xhtml_b9fig9_3) Using the Visitor pattern to evaluate a page template.

The Expander class is specialization of Visitor that uses an Env to keep track of variables. It imports a handler for each type of special node we support—we will write those in a moment—and uses them to process each type of node:

1.  If the node is plain text, copy it to the output.

2.  If there is a handler for the node, call the handler's open or close method.

3.  Otherwise, open or close a regular tag.

![](images/comp09_7.jpg)

Checking to see if there is a handler for a particular node and getting that handler are straightforward—we just look at the node's attributes:

![](images/comp09_8.jpg)

Finally, we need a few helper methods to show tags and generate output:

![](images/comp09_9.jpg)

Notice that this class adds strings to an array and joins them all right at the end rather than concatenating strings repeatedly. Doing this is more efficient and also helps with debugging, since each string in the array corresponds to a single method call.

## 9.4 How do we implement node handlers?

At this point we have built a lot of infrastructure but haven't actually processed any special nodes. To do that, let's write a handler that copies a constant number into the output:

![](images/comp09_10.jpg)

When we enter a node like < span z-num="123"/ > this handler asks the expander to show an opening tag followed by the value of the z-num attribute. When we exit the node, the handler asks the expander to close the tag. The handler doesn't know whether things are printed immediately, added to an output list, or something else; it just knows that whoever called it implements the low-level operations it needs.

Note that this expander is *not* a class, but instead an object with two functions stored under the keys open and close. We could use a class for each handler so that handlers can store any extra state they need, but **bare objects** are common and useful in JavaScript (though we will see below that we *should* have used classes).

So much for constants; what about variables?

![](images/comp09_11.jpg)

This code is almost the same as the previous example. The only difference is that instead of copying the attribute's value directly to the output, we use it as a key to look up a value in the environment.

These two pairs of handlers look plausible, but do they work? To find out, we can build a program that loads variable definitions from a JSON file, reads an HTML template, and does the expansion:

![](images/comp09_12.jpg)

We added new variables for our test cases one-by-one as we were writing this chapter. To avoid repeating text repeatedly, we show the entire set once:

![](images/comp09_13.jpg)

Our first test: is static text copied over as-is ([Figure 9.4](#chapter9.xhtml_fig9_4))?

![](images/fig9_4.jpg)

[Figure 9.4:](#chapter9.xhtml_b9fig9_4) Static text generated by page templates.

![](images/comp09_14.jpg)![](images/comp09_15.jpg)![](images/comp09_16.jpg)

Good. Now, does the expander handle constants ([Figure 9.5](#chapter9.xhtml_fig9_5))?

![](images/fig9_5.jpg)

[Figure 9.5:](#chapter9.xhtml_b9fig9_5) A single constant generated by page templates.

![](images/comp09_17.jpg)![](images/comp09_18.jpg)

What about a single variable ([Figure 9.6](#chapter9.xhtml_fig9_6))?

![](images/fig9_6.jpg)

[Figure 9.6:](#chapter9.xhtml_b9fig9_6) A single variable generated by page templates.

![](images/comp09_19.jpg)![](images/comp09_20.jpg)

What about a page containing multiple variables? There's no reason it should fail if the single-variable case works, but we should still check—again, software isn't done until it has been tested ([Figure 9.7](#chapter9.xhtml_fig9_7)).

![](images/fig9_7.jpg)

[Figure 9.7:](#chapter9.xhtml_b9fig9_7) Multiple variables generated by page templates.

![](images/comp09_21.jpg)![](images/comp09_22.jpg)

## 9.5 How can we implement control flow?

Our tool supports two types of control flow: conditional expressions and loops. Since we don't support Boolean expressions like and and or, implementing a conditional is as simple as looking up a variable (which we know how to do) and then expanding the node if the value is true:

![](images/comp09_23.jpg)

Let's test it ([Figure 9.8](#chapter9.xhtml_fig9_8)):

![](images/fig9_8.jpg)

[Figure 9.8:](#chapter9.xhtml_b9fig9_8) Conditional text generated by page templates.

![](images/comp09_24.jpg)![](images/comp09_25.jpg)

> **Spot the bug**
> 
> The open and close functions for if both check the value of the control variable. If something inside the if‘s body changes that value we could produce an opening tag without a matching closing tag. We haven't implemented assignment, so there's no way for that to happen now, but it could be a headache if we add it later.

Finally we come to loops. For these, we need to get the array we're looping over from the environment and do something for each of its elements. That “something” is:

1.  Create a new stack frame holding the current value of the loop variable.

2.  Expand all of the node's children with that stack frame in place.

3.  Pop the stack frame to get rid of the temporary variable.

![](images/comp09_26.jpg)

Once again, it's not done until we test it ([Figure 9.9](#chapter9.xhtml_fig9_9)):

![](images/fig9_9.jpg)

[Figure 9.9:](#chapter9.xhtml_b9fig9_9) Repeated text generated with a loop by page templates.

![](images/comp09_27.jpg)![](images/comp09_28.jpg)

Notice how we create the new stack frame using:

![](images/comp09_29.jpg)

This is an ugly but useful trick. We can't write:

![](images/comp09_30.jpg)

because that would create an object with the string indexName as a key, rather than one with the value of the variable indexName as its key. We can't do this either:

![](images/comp09_31.jpg)

though it seems like we should be able to. Instead, we create an array containing the string we want. Since JavaScript automatically converts arrays to strings by concatenating their elements when it needs to, our expression is a quick way to get the same effect as:

![](images/comp09_32.jpg)

Those three lines *are* much easier to understand, though, so we should probably have been less clever.

## 9.6 How did we know how to do all of this?

We have just implemented a simple programming language. It can't do arithmetic, but if we wanted to add tags like:

![](images/comp09_33.jpg)

we could. It's unlikely anyone would use the result—typing all of that is so much clumsier than typing width+1 that people wouldn't use it unless they had no other choice—but the basic design is there.

We didn't invent any of this from scratch, any more than we invented the parsing algorithm of [Chapter 8](#chapter8.xhtml). Instead, we did what you are doing now: we read what other programmers had written and tried to make sense of the key ideas.

The problem is that “making sense” depends on who we are. When we use a low-level language, we incur the cognitive load of assembling micro-steps into something more meaningful. When we use a high-level language, on the other hand, we incur a similar load translating functions of functions (of functions…) (or meta-classes templated on object factories) into actual operations on actual data.

More experienced programmers are more capable at both ends of the curve, but that's not the only thing that changes. If a novice's comprehension curve looks like the lower curve in [Figure 9.10](#chapter9.xhtml_fig9_10), then an expert's looks like the upper one. Experts don't just understand more at all levels of abstraction; their *preferred* level has also shifted so that $\sqrt{x^{2} + y^{2}}$ is actually more readable than the medieval expression “the side of the square whose area is the sum of the areas of the two squares whose sides are given by the first part and the second part”.

![](images/fig9_10.jpg)

[Figure 9.10:](#chapter9.xhtml_b9fig9_10) Novice and expert comprehension curves.

One implication of this is that for any given task, the software that is quickest for a novice to comprehend will almost certainly be different from the software that an expert can understand most quickly. In an ideal world our tools would automatically re-represent programs at different levels, so that with a click of a button we could view our code as either:

![](images/comp09_34.jpg)

or:

![](images/comp09_35.jpg)

just as we could change the colors used for syntax highlighting or the depth to which loop bodies are indented. But today's tools don't do that, and I suspect that any tool smart enough to translate between comprehension levels automatically would also be smart enough to write the code without our help.

## 9.7 Exercises

### Tracing execution

Add a directive < span z-trace="variable"/ > that prints the current value of a variable using console.error for debugging.

### Unit tests

Write unit tests for template expansion using Mocha.

### Trimming text

Modify all of the directives to take an extra optional attribute z-trim="true". If this attribute is set, leading and trailing whitespace is trimmed from the directive's expansion.

### Literal text

Add a directive < div z-literal="true" >... < /div > that copies the enclosed text as-is without interpreting or expanding any contained directives. (A directive like this would be needed when writing documentation for the template expander.)

### Including other files

1.  Add a directive < div z-include="filename.html"/ > that includes another file in the file being processed.

2.  Should included files be processed and the result copied into the including file, or should the text be copied in and then processed? What difference does it make to the way variables are evaluated?

### HTML snippets

Add a directive < div z-snippet="variable" >... < /div > that saves some text in a variable so that it can be displayed later. For example:

![](images/comp09_36.jpg)

would printed the word “Important:” in bold before each item in the list.

### YAML headers

Modify the template expander to handle variables defined in a YAML header in the page being processed. For example, if the page is:

![](images/comp09_37.jpg)

will create a paragraph containing the given name.

### Expanding all files

Write a program expand-all.js that takes two directory names as command-line arguments and builds a website in the second directory by expanding all of the HTML files found in the first or in sub-directories of the first.

### Counting loops

Add a directive < div z-index="indexName" z-limit="limitName" >... < /div > that loops from zero to the value in the variable limitName, putting the current iteration index in indexName.

### Auxiliary functions

1.  Modify Expander so that it takes an extra argument auxiliaries containing zero or more named functions:

    ![](images/comp09_38.jpg)
2.  Add a directive < span z-call="functionName" z-args="var,var"/ > that looks up a function in auxiliaries and calls it with the given variables as arguments.

# 10Build Manager

Terms defined: **[automatic variable](#appendix5.xhtml_d21)**, **[build manager](#appendix5.xhtml_d33)**, **[build recipe](#appendix5.xhtml_d34)**, **[build rule](#appendix5.xhtml_d35)**, **[build target](#appendix5.xhtml_d36)**, **[compiled language](#appendix5.xhtml_d62)**, **[cycle (in a graph)](#appendix5.xhtml_d72)**, **[dependency](#appendix5.xhtml_d77)**, **[directed acyclic graph](#appendix5.xhtml_d86)**, **[driver](#appendix5.xhtml_d92)**, **[interpreted language](#appendix5.xhtml_d151)**, **[link (a program)](#appendix5.xhtml_d168)**, **[pattern rule](#appendix5.xhtml_d210)**, **[runnable documentation](#appendix5.xhtml_d239)**, **[stale (in build)](#appendix5.xhtml_d263)**, **[Template Method pattern](#appendix5.xhtml_d276)**, **[topological order](#appendix5.xhtml_d286)**

Suppose we are using a page templating system to create a website ([Chapter 9](#chapter9.xhtml)). If we change a single page our tool should translate it, but it shouldn't waste time translating others. If we change a template, on the other hand, the tool should realize that every page in the site is potentially affected and automatically re-translate all of them.

Choosing what actions to take based on how files depend on one another is a common pattern. For example, programs in **compiled languages** like C and Java have to be translated into lower-level forms before they can run. In fact, there are usually two stages to the translation: compiling each source file into some intermediate form, and then **linking** the compiled modules to each other and to libraries to create a runnable program ([Figure 10.1](#chapter10.xhtml_fig10_1)). If a source file hasn't changed, there's no need to recompile it before linking.

![](images/fig10_1.jpg)

[Figure 10.1:](#chapter10.xhtml_b10fig10_1) Compiling source files and linking the resulting modules.

A **build manager** takes a description of what depends on what, figures out which files are out of date, determines an order in which to rebuild things, and then executes any necessary steps. Originally created to manage compilation, they are also useful for programs written in **interpreted languages** like JavaScript when we want to bundle multiple modules into a single loadable file ([Chapter 17](#chapter17.xhtml)) or re-create documentation from source code ([Chapter 16](#chapter16.xhtml)). In this chapter we will create a simple build manager based on Make[¹](#chapter10.xhtml_fn10_1), Bajel[²](#chapter10.xhtml_fn10_2), Jake[³](#chapter10.xhtml_fn10_3), and other systems discussed in [[Smith2011]](#refbib1.xhtml_refbib_26).

## 10.1 What's in a build manager?

The input to a build manager is a set of rules, each of which has:

*   a **target**, which is the file to be updated;

*   some **dependencies**, which are the things that file depends on; and

*   a **recipe** that specifies how to update the target if it is out of date compared to its dependencies.

The target of one rule can be a dependency of another rule, so the relationships between the files form a **directed acyclic graph** or DAG ([Figure 10.2](#chapter10.xhtml_fig10_2)). The graph is directed because “A depends on B” is a one-way relationship; it cannot contain cycles (or loops) because if something depends on itself we can never finish updating it. We say that a target is **stale** if it is older than any of its dependencies. When this happens, we use the recipes to bring it up to date.

![](images/fig10_2.jpg)

[Figure 10.2:](#chapter10.xhtml_b10fig10_2) How a build manager finds and respects dependencies.

Our build manager must:

1.  Read a file containing rules.

2.  Construct the dependency graph.

3.  Figure out which targets are stale.

4.  Build those targets, making sure to build things *before* anything that depends on them is built.

## 10.2 Where should we start?

We will store our rules in YAML files like this:

![](images/comp10_1.jpg)

We could equally well have used JSON, but it wouldn't have made sense to use CSV: rules have a nested structure, and CSV doesn't represent nesting particularly gracefully.

We are going to create our build manager in stages, so we start by writing a simple **driver** that loads a JavaScript source file, creates an object of whatever class that file exports, and runs the .build method of that object with the rest of the command-line parameters:

![](images/comp10_2.jpg)

We use the import function to dynamically load files in [Chapter 4](#chapter4.xhtml) as well. It only saves us a few lines of code in this case, but we will use this idea of a general-purpose driver for larger programs in future chapters.

To work with our driver, each version of our build manager must be a class that satisfies two requirements:

1.  Its [constructor](#appendix5.xhtml_d66) must take a configuration file as an [argument](#appendix5.xhtml_d13).

2.  It must provide a build method that needs no arguments.

The build method must create a graph from the configuration file, check that it does not contain any **cycles**, and then run whatever commands are needed to update stale targets. Just as we built a generic Visitor class in [Chapter 9](#chapter9.xhtml), we can build a generic base class for our build manager that does these steps in this order without actually implementing any of them:

![](images/comp10_3.jpg)

This is an example of the **Template Method** design pattern: the parent class defines the order of the steps and child classes fill them in ([Figure 10.3](#chapter10.xhtml_fig10_3)). This design pattern ensures that every child does the same things in the same order, even if the details of *how* vary from case to case.

![](images/fig10_3.jpg)

[Figure 10.3:](#chapter10.xhtml_b10fig10_3) The Template Method pattern in action.

We would normally implement all of the methods required by the build method at the same time; here, we will write them one-by-one to make the evolving code easier to follow. The loadConfig method loads the configuration file as the builder object is being constructed:

![](images/comp10_4.jpg)

The first line does the loading; the rest of the method checks that the rules are at least superficially plausible. We need these checks because YAML is a generic file format that doesn't know anything about the extra requirements of our rules. And as we first saw in [Chapter 3](#chapter3.xhtml), we have to specify that the character encoding of our file is UTF-8 so that JavaScript knows how to convert bytes into text.

The next step is to turn the configuration into a graph in memory. We use the graphlib[⁴](#chapter10.xhtml_fn10_4) module to manage nodes and links rather than writing our own classes for graphs, and store the recipe to rebuild a node in that node. Two features of graphlib that took us a while to figure out are that:

1.  links go *from* the dependency *to* the target, and

2.  setEdge automatically adds nodes if they aren't already present.

graphlib provides implementations of some common graph algorithms, including one to check for cycles, so we might as well write that method at this point too:

![](images/comp10_5.jpg)

We can now create something that displays our configuration when it runs but does nothing else:

![](images/comp10_6.jpg)

If we run this with our three simple rules as input, it shows the graph with v and w keys to represent the ends of the links:

![](images/comp10_7.jpg)![](images/comp10_8.jpg)

Let's write a quick test to make sure the cycle detector works as intended:

![](images/comp10_9.jpg)![](images/comp10_10.jpg)![](images/comp10_11.jpg)

## 10.3 How can we specify that a file is out-of-date?

The next step is to figure out which files are out-of-date. Make does this by comparing the timestamps of the files in question, but this isn't always reliable because computers’ clocks may be slightly out of sync, which can produce a wrong answer on a networked filesystem, and the operating system may only report file update times to the nearest millisecond (which seemed very short in 1970 but seems very long today).

More modern build systems store a hash of each file's contents and compare the current hash to the stored one to see if the file has changed. Since we already looked at hashing in [Chapter 5](#chapter5.xhtml), we will use the timestamp approach here. And instead of using a mock filesystem as we did in [Chapter 5](#chapter5.xhtml), we will simply load another configuration file that specifies fake timestamps for files:

![](images/comp10_12.jpg)

Since we want to associate those timestamps with files, we add a step to buildGraph to read the timestamp file and add information to the graph's nodes:

![](images/comp10_13.jpg)

Before we move on, let's make sure that adding timestamps works as we want:

![](images/comp10_14.jpg)![](images/comp10_15.jpg)

## 10.4 How can we update out-of-date files?

To figure out which recipes to execute and in which order, we set the pretended current time to the latest time of any file, then look at each file in topological order. If a file is older than any of its dependencies, we update the file *and* its pretended timestamp to trigger an update of anything that depends on it.

We can pretend that updating a file always takes one unit of time, so we advance our fictional clock by one for each build. Using graphlib.alg.topsort to create the topological order, we get this:

![](images/comp10_16.jpg)

The run method:

1.  gets a sorted list of nodes;

2.  sets the starting time to be one unit past the largest file time; and then

3.  uses Array.reduce to operate on each node (i.e., each file) in order. If that file is stale, we print the steps we would run and then update the file's timestamp. We only advance the notional current time when we do an update.

To check if a file is stale, we see if any of its dependencies currently have timestamps greater than or equal to its own. When we run this, it seems to do the right thing:

![](images/comp10_17.jpg)![](images/comp10_18.jpg)

## 10.5 How can we add generic build rules?

If our website has a hundred blog posts or a hundred pages of documentation about particular JavaScript files, we don't want to have to write a hundred nearly-identical recipes. Instead, we want to be able to write generic **build rules** that say, “Build all things of this kind the same way.” These generic rules need:

*   a way to define a set of files;

*   a way to specify a generic rule; and

*   a way to fill in parts of that rule.

We will achieve this by overriding buildGraph to replace variables in recipes with values. Once again, object-oriented programming helps us change only what we need to change, provided we divided our problem into sensible chunks in the first place.

Make provides **automatic variables** with names like $ < and $@ to represent the parts of a rule. Ours will be more readable: we will use @TARGET for the target, @DEPENDENCIES for the dependencies (in order), and @DEP[1], @DEP[2], and so on for specific dependencies ([Figure 10.4](#chapter10.xhtml_fig10_4)). Our variable expander looks like this:

![](images/comp10_19.jpg)![](images/fig10_4.jpg)

[Figure 10.4:](#chapter10.xhtml_b10fig10_4) Turning patterns rules into runnable commands.

The first thing we do is test that it works when there *aren't* any variables to expand by running it on the same example we used previously:

![](images/comp10_20.jpg)

This is perhaps the most important reason to create tests: they tell us right away if something we have added or changed has broken something that used to work. That gives us a firm base to build on as we de[bug](#appendix5.xhtml_d32) the new code.

Now we need to add **pattern rules**. Our first attempt at a rules file looks like this:

![](images/comp10_21.jpg)

and our first attempt at reading it extracts rules before expanding variables:

![](images/comp10_22.jpg)

However, that doesn't work:

![](images/comp10_23.jpg)

The problem is that our simple graph loader creates nodes for dependencies even if they aren't targets. As a result, we wind up tripping over the lack of a node for %.in before we get to extracting rules.

We can fix our problem by rewriting the rule loader to separate pattern rules from simple rules; we can tell the two apart by checking if the rule's dependencies include %. While we're here, we will enable timestamps as an optional field in the rules for testing purposes rather than having them in a separate file:

![](images/comp10_24.jpg)

Before we run this, let's add methods to show the state of our data structures:

![](images/comp10_25.jpg)![](images/comp10_26.jpg)![](images/comp10_27.jpg)

The output seems to be right, so let's try expanding rules *after* building the graph and rules but *before* expanding variables:

![](images/comp10_28.jpg)![](images/comp10_29.jpg)

## 10.6 What should we do next?

We have added a lot of steps to our original template method, which makes it a bit of a stretch to claim that the overall operation hasn't changed. Knowing what we know now, we could go back and modify the original SkeletonBuilder.build method to include those extra steps and provide do-nothing implementations.

The root of the problem is that we didn't anticipate all the steps that would be involved when we wrote our template method. It typically takes a few child classes for this to settle down; if it never does, then Template Method is probably the wrong pattern for our situation. This isn't a failure in initial design: we always learn about our problem as we try to capture it in code, and if we know enough to anticipate 100% of the issues that are going to come up, it's time to put what we've learned in a library for future use.

## 10.7 Exercises

### Handle failure

1.  Modify the build manager to accommodate build steps that fail.

2.  Write Mocha tests to check that this change works correctly.

### Dry run

Add an option to the build manager to show what commands would be executed and why if a build were actually run. For example, the output should display things like, “‘update A’ because A older than B”.

### Change directories

Modify the build manager so that:

![](images/comp10_30.jpg)

runs the build in the specified directory rather than the current directory.

### Merge files

Modify the build manager so that it can read multiple configuration files and execute their combined rules.

### Show recipes

Add a method to build manager to display all unique recipes, i.e., all of the commands it might execute if asked to rebuild everything.

### Conditional execution

Modify the build manager so that:

1.  The user can pass variable=true and variable=false arguments on the command-line to define variables.

2.  Rules can contain an if: variable field.

3.  Those rules are only executed if the variable is defined and true.

4.  Write Mocha tests to check that this works correctly.

### Define filesets

Modify the build manager so that users can define sets of files:

![](images/comp10_31.jpg)

and then refer to them later:

![](images/comp10_32.jpg)

### Globbing

Modify the build manager so that it can dynamically construct a set of files:

![](images/comp10_33.jpg)

and then refer to them later:

![](images/comp10_34.jpg)

### Use hashes

1.  Write a program called build-init.js that calculates a hash for every file mentioned in the build configuration and stores the hash along with the file's name in build-hash.json.

2.  Modify the build manager to compare the current hashes of files with those stored in build-hash.json in order to determine what is out of date, and to update build-hash.json each time it runs.

### Auxiliary functions

1.  Modify the builder manager so that it takes an extra argument auxiliaries containing zero or more named functions:

    ![](images/comp10_35.jpg)
2.  Modify the run method to call these functions before executing the rules for a node, and to only execute the rules if all of them return true.

3.  Write Mocha tests to check that this works correctly.

# 11Layout Engine

Terms defined: **[attribute](#appendix5.xhtml_d20)**, **[cache](#appendix5.xhtml_d38)**, **[confirmation bias](#appendix5.xhtml_d64)**, **[design by contract](#appendix5.xhtml_d82)**, **[easy mode](#appendix5.xhtml_d97)**, **[layout engine](#appendix5.xhtml_d161)**, **[Liskov Substitution Principle](#appendix5.xhtml_d170)**, **[query selector](#appendix5.xhtml_d226)**, **[signature](#appendix5.xhtml_d254)**, **[z-buffering](#appendix5.xhtml_d307)**

You might be reading this as an HTML page, an e-book (which is basically the same thing), or on the printed page. In all three cases, a **layout engine** took some text and some layout instructions and decided where to put each character and image. We will build a small layout engine in this chapter based on Matt Brubeck's[¹](#chapter11.xhtml_fn11_1) tutorial[²](#chapter11.xhtml_fn11_2) to explore how browsers decide what to put where.

Our inputs will be a very small subset of HTML and an equally small subset of CSS. We will create our own classes to represent these instead of using those provided by various Node[³](#chapter11.xhtml_fn11_3) libraries; to translate the combination of HTML and CSS into text on the screen, we will label each node in the DOM tree with the appropriate styles, walk that tree to figure out where each visible element belongs, and then draw the result as text on the screen.

![](images/fig11_1.jpg)

[Figure 11.1:](#chapter11.xhtml_b11fig11_1) Coordinate system with (0, 0) in the upper left corner.

## 11.1. How can we size rows and columns?

Let's start on **easy mode** without margins, padding, line-wrapping, or other complications. Everything we can put on the screen is represented as a rectangular cell, and every cell is either a row, a column, or a block. A block has a fixed width and height:

![](images/comp11_1.jpg)

A row arranges one or more cells horizontally; its width is the sum of the widths of its children, while its height is the height of its tallest child ([Figure 11.2](#chapter11.xhtml_fig11_2)):

![](images/comp11_2.jpg)![](images/fig11_2.jpg)

[Figure 11.2:](#chapter11.xhtml_b11fig11_2) Calculating sizes of blocks with fixed width and height.

Finally, a column arranges one or more cells vertically; its width is the width of its widest child and its height is the sum of the heights of its children. (Here and elsewhere we use the abbreviation col when referring to columns.)

![](images/comp11_3.jpg)

Rows and columns nest inside one another: a row cannot span two or more columns, and a column cannot cross the boundary between two rows. Any time we have a structure with that property we can represent it as a tree of nested objects. Given such a tree, we can calculate the width and height of each cell every time we need to. This is simple but inefficient: we could calculate both width and height at the same time and **cache** those values to avoid recalculation, but we called this “easy mode” for a reason.

As simple as it is, this code could still contain errors (and did during development), so we write some Mocha[⁶](#chapter11.xhtml_fn11_6) tests to check that it works as desired before trying to build anything more complicated:

![](images/comp11_4.jpg)![](images/comp11_5.jpg)

## 11.2. How can we position rows and columns?

Now that we know how big each cell is we can figure out where to put it. Suppose we start with the upper left corner of the browser: upper because we lay out the page top-to-bottom and left because we are doing left-to-right layout. If the cell is a block, we place it there. If the cell is a row, on the other hand, we get its height and then calculate its lower edge as y1 = y0 + height. We then place the first child's lower-left corner at (x0, y1), the second child's at (x0 + width0, y1), and so on ([Figure 11.3](#chapter11.xhtml_fig11_3)). Similarly, if the cell is a column we place the first child at (x0, y0), the next at (x0, y0 + height0), and so on.

![](images/fig11_3.jpg)

[Figure 11.3:](#chapter11.xhtml_b11fig11_3) Laying out rows and columns of fixed-size blocks.

To save ourselves some testing we will derive the classes that know how to do layout from the classes we wrote before. Our blocks are:

![](images/comp11_6.jpg)

while our columns are:

![](images/comp11_7.jpg)

and our rows are:

![](images/comp11_8.jpg)

Once again, we write and run some tests to check that everything is doing what it's supposed to:

![](images/comp11_9.jpg)![](images/comp11_10.jpg)

## 11.3. How can we render elements?

We drew the blocks on a piece of graph paper in order to figure out the expected answers for the tests shown above. We can do something similar in software by creating a “screen” of space characters and then having each block draw itself in the right place. If we do this starting at the root of the tree, child blocks will overwrite the markings made by their parents, which will automatically produce the right appearance ([Figure 11.4](#chapter11.xhtml_fig11_4)). (A more sophisticated version of this called **z-buffering** keeps track of the visual depth of each pixel in order to draw things in three dimensions.)

![](images/fig11_4.jpg)

[Figure 11.4:](#chapter11.xhtml_b11fig11_4) Render blocks by drawing child nodes on top of parent nodes.

Our pretended screen is just an array of arrays of characters:

![](images/comp11_11.jpg)

We will use successive lower-case characters to show each block, i.e., the root block will draw itself using the letter a, while its children will use b, c, and so on.

![](images/comp11_12.jpg)

To teach each kind of cell how to render itself, we have to derive a new class from each of the ones we have and give the new class a render method with the same **signature**:

![](images/comp11_13.jpg)

These render methods do exactly the same thing, so we have each one call a shared function that does the actual work. If we were building a real layout engine, a cleaner solution would be to go back and create a class called Cell with this render method, then derive our Block, Row, and Col classes from that. In general, if two or more classes need to be able to do something, we should add a method to do that to their lowest common ancestor.

Our simpler tests are a little easier to read once we have rendering in place, though we still had to draw things on paper to figure out our complex ones:

![](images/comp11_14.jpg)

The fact that we find our own tests difficult to understand is a sign that we should do more testing. It would be very easy for us to get a wrong result and convince ourselves that it was actually correct; **confirmation bias** of this kind is very common in software development.

## 11.4. How can we wrap elements to fit?

One of the biggest differences between a browser and a printed page is that the text in the browser wraps itself automatically as the window is resized. (The other, these days, is that the printed page doesn't spy on us, though someone is undoubtedly working on that.)

To add wrapping to our layout engine, suppose we fix the width of a row. If the total width of the children is greater than the row's width, the layout engine needs to wrap the children around. This assumes that columns can be made as big as they need to be, i.e., that we can grow vertically to make up for limited space horizontally. It also assumes that all of the row's children are no wider than the width of the row; we will look at what happens when they're not in the exercises.

Our layout engine manages wrapping by transforming the tree. The height and width of blocks are fixed, so they become themselves. Columns become themselves as well, but since they have children that might need to wrap, the class representing columns needs a new method:

![](images/comp11_15.jpg)

Rows do all the hard work. Each original row is replaced with a new row that contains a single column with one or more rows, each of which is one “line” of wrapped cells ([Figure 11.5](#chapter11.xhtml_fig11_5)). This replacement is unnecessary when everything will fit on a single row, but it's easiest to write the code that does it every time; we will look at making this more efficient in the exercises.

![](images/fig11_5.jpg)

[Figure 11.5:](#chapter11.xhtml_b11fig11_5) Wrapping rows by introducing a new row and column.

Our new wrappable row's constructor takes a fixed width followed by the children and returns that fixed width when asked for its size:

![](images/comp11_16.jpg)

Wrapping puts the row's children into buckets, then converts the buckets to a row of a column of rows:

![](images/comp11_17.jpg)

Once again we bring forward all the previous tests and write some new ones to test the functionality we've added:

![](images/comp11_18.jpg)![](images/comp11_19.jpg)

## 11.5. What subset of CSS will we support?

It's finally time to style pages that contain text. Our final subset of HTML has rows, columns, and text blocks as before. Each text block has one or more lines of text; the number of lines determines the block's height and the length of the longest line determines its width.

Rows and columns can have **attributes** just as they can in real HTML, and each attribute must have a single value in quotes. Rows no longer take a fixed width: instead, we will specify that with our little subset of CSS. Together, these three classes are just over 40 lines of code:

![](images/comp11_20.jpg)

We will use regular expressions to parse HTML (though as we explained in [Chapter 8](#chapter8.xhtml), this is a sin[⁷](#chapter11.xhtml_fn11_7)). The main body of our parser is:

![](images/comp11_21.jpg)

while the two functions that do most of the work are:

![](images/comp11_22.jpg)

and:

![](images/comp11_23.jpg)

The next step is to define a generic class for CSS rules with a subclass for each type of rule. From highest precedence to lowest, the three types of rules we support identify specific nodes via their ID, classes of nodes via their class attribute, and types of nodes via their element name. We keep track of which rules take precedence over which through the simple expedient of numbering the classes:

![](images/comp11_24.jpg)

An ID rule's **query selector** is written as #name and matches HTML like < tag id="name" >... < /tag > (where tag is row or col):

![](images/comp11_25.jpg)

A class rule's query selector is written as .kind and matches HTML like < tag class="kind" >... < /tag >. Unlike real CSS, we only allow one class per node:

![](images/comp11_26.jpg)

Finally, tag rules just have the name of the type of node they apply to without any punctuation:

![](images/comp11_27.jpg)

We could build yet another parser to read a subset of CSS and convert it to objects, but this chapter is long enough, so we will write our rules as JSON:

![](images/comp11_28.jpg)

and build a class that converts this representation to a set of objects:

![](images/comp11_29.jpg)

Our CSS ruleset class also has a method for finding the rules for a given DOM node. This method relies on the precedence values we defined for our classes in order to sort them so that we can find the most specific.

Here's our final set of tests:

![](images/comp11_30.jpg)

If we were going on, we would override the cells’ getWidth and getHeight methods to pay attention to styles. We would also decide what to do with cells that don't have any styles defined: use a default, flag it as an error, or make a choice based on the contents of the child nodes. We will explore these possibilities in the exercises.

## 11.6. Exercises

### Refactoring the node classes

Refactor the classes used to represent blocks, rows, and columns so that:

1.  They all derive from a common parent.

2.  All common behavior is defined in that parent (if only with placeholder methods).

### Handling rule conflicts

Modify the rule lookup mechanism so that if two conflicting rules are defined, the one that is defined second takes precedence. For example, if there are two definitions for row.bold, whichever comes last in the JSON representation of the CSS wins.

### Handling arbitrary tags

Modify the existing code to handle arbitrary HTML elements.

1.  The parser should recognize < anyTag >... < /anyTag >.

2.  Instead of separate classes for rows and columns, there should be one class Node whose tag attribute identifies its type.

### Recycling nodes

Modify the wrapping code so that new rows and columns are only created if needed. For example, if a row of width 10 contains a text node with the string “fits”, a new row and column are *not* inserted.

### Rendering a clear background

Modify the rendering code so that only the text in block nodes is shown, i.e., so that the empty space in rows and columns is rendered as spaces.

### Clipping text

1.  Modify the wrapping and rendering so that if a block of text is too wide for the available space the extra characters are clipped. For example, if a column of width 5 contains a line “unfittable”, only “unfit” appears.

2.  Extend your solution to break lines on spaces as needed in order to avoid clipping.

### Bidirectional rendering

Modify the existing software to do either left-to-right or right-to-left rendering upon request.

### Equal sizing

Modify the existing code to support elastic columns, i.e., so that all of the columns in a row are automatically sized to have the same width. If the number of columns does not divide evenly into the width of the row, allocate the extra space as equally as possible from left to right.

### Padding elements

Modify the existing code so that:

1.  Authors can define a padding attribute for row and column elements.

2.  When the node is rendered, that many blank spaces are added on all four sides of the contents.

For example, the HTML < row > text < /row > would render as:

![](images/comp11_31.jpg)

where the lines show the outer border of the rendering.

### Drawing borders

1.  Modify the existing code so that elements may specify border: true or border: false (with the latter being the default). If an element's border property is true, it is drawn with a dashed border. For example, if the border property of row is true, then < row > text < /row > is rendered as:

    ![](images/comp11_32.jpg)
2.  Extend your solution so that if two adjacent cells both have borders, only a single border is drawn. For example, if the border property of col is true, then:

    ![](images/comp11_33.jpg)

    is rendered as:

    ![](images/comp11_34.jpg)

# 12File Interpolator

Terms defined: **[header file](#appendix5.xhtml_d134)**, **[literate programming](#appendix5.xhtml_d173)**, **[loader](#appendix5.xhtml_d174)**, **[sandbox](#appendix5.xhtml_d240)**, **[search path](#appendix5.xhtml_d246)**, **[shell variable](#appendix5.xhtml_d252)**

Many of the examples in these lessons are too long to show comfortably in one block of code on a printed page, so we needed a way to break them up. As an experiment, we wrote a custom **module loader** that reads a source file containing specially-formatted comments and then reads and inserts the files specified in those comments before running the code ([Figure 12.1](#chapter12.xhtml_fig12_1)). Modern programming languages don't work this way, but C and C++ do this with **header files**, and static site generators ([Chapter 9](#chapter9.xhtml)) do this to share fragments of HTML.

![](images/fig12_1.jpg)

[Figure 12.1:](#chapter12.xhtml_b12fig12_1) Including fragments of code to create runnable programs.

The special comments in our source files contain the text to put in the displayed version and file to include when loading:

![](images/comp12_1.jpg)

We got this to work, but decided to use a different approach in this book. The stumbling block was that the style-checking tool ESLint[¹](#chapter12.xhtml_fn12_1) didn't know what to make of our inclusions, so we would either have to modify it or build a style checker of our own. (We will actually do that in [Chapter 14](#chapter14.xhtml), but we won't go nearly as far as ESLint.)

Despite being a dead end, the inclusion tool is a good way to show how JavaScript turns source code into something it can execute. We need to be able to do this in the next couple of chapters, so we might as well tackle it now.

## 12.1. How can we evaluate JavaScript dynamically?

We want to display files as they are on the web and in print, but interpolate the files referenced in special comments when we load things with import. To do this, we need to understand the lifecycle of a JavaScript program. When we ask for a file, Node[²](#chapter12.xhtml_fn12_2) reads the text, translates it into runnable instructions, and runs those instructions. We can do the second and third steps whenever we want using a function called eval, which takes a string as input and executes it as if it were part of the program ([Figure 12.2](#chapter12.xhtml_fig12_2)).

![](images/fig12_2.jpg)

[Figure 12.2:](#chapter12.xhtml_b12fig12_2) eval vs. normal translation and execution.

To see eval in action, let's evaluate an expression:

![](images/comp12_2.jpg)![](images/comp12_3.jpg)

Notice that the input to eval is *not* 2 + 2, but rather a string containing the digit 2, a space, a plus sign, another space, and another 2\. When we call eval, it translates this string using exactly the same parser that Node uses for our program and immediately runs the result.

We can make the example a little more interesting by constructing the string dynamically:

![](images/comp12_4.jpg)![](images/comp12_5.jpg)

The first time the loop runs the string is ’x + 1’; since there's a variable called x in scope, eval does the addition and we print the result. The same thing happens for the variables y and z, but we get an error when we try to evaluate the string ’oops + 1’ because there is no variable in scope called oops.

eval can use whatever variables are in scope when it's called, but what happens to any variables it defines? This example creates a variable called x and runs console.log to display it, but as the output shows, x is local to the eval call just as variables created inside a function only exist during a call to that function:

![](images/comp12_6.jpg)![](images/comp12_7.jpg)

However, eval can modify variables defined outside the text being evaluated in the same way that a function can modify global variables:

![](images/comp12_8.jpg)![](images/comp12_9.jpg)

This means that if the text we give to eval modifies a structure that is defined outside the text, that change outlives the call to eval:

![](images/comp12_10.jpg)![](images/comp12_11.jpg)

The examples so far have all evaluated strings embedded in the program itself, but eval doesn't care where its input comes from. Let's move the code that does the modifying into to-be-loaded.js:

![](images/comp12_12.jpg)

This doesn't work on its own because Seen isn't defined:

![](images/comp12_13.jpg)

But if we read the file and eval the text *after* defining Seen, it does what we want:

![](images/comp12_14.jpg)![](images/comp12_15.jpg)![](images/comp12_16.jpg)

## 12.2. How can we manage files?

The source files in this book are small enough that we don't have to worry about reading them repeatedly, but we would like to avoid re-reading things unnecessarily in large systems or when there might be network delays. The usual approach is to create a cache using the Singleton pattern that we first met in [Chapter 4](#chapter4.xhtml). Whenever we want to read a file, we check to see if it's already in the cache ([Figure 12.3](#chapter12.xhtml_fig12_3)). If it is, we use that copy; if not, we read it and add it to the cache using the file path as a lookup key.

![](images/fig12_3.jpg)

[Figure 12.3:](#chapter12.xhtml_b12fig12_3) Using the Singleton pattern to implement a cache of loaded files.

We can write a simple cache in just a few lines of code:

![](images/comp12_17.jpg)

Since we are using eval, though, we can't rely on export to make things available to the rest of the program. Instead, we rely on the fact that the result of an eval call is the value of the last expression evaluated. Since a variable name on its own evaluates to the variable's value, we can create a function and then use its name to “export” it from the evaluated file:

![](images/comp12_18.jpg)

To test our program, we load the implementation of the cache using import, then use it to load and evaluate another file. This example expects that “other file” to define a function, which we call in order to show that everything is working:

![](images/comp12_19.jpg)![](images/comp12_20.jpg)

## 12.3. How can we find files?

Each of the files included in our examples is in the same directory as the file including it, but in C/C++ or a page templating system we might include a particular file in several different places. We don't want to have to put all of our files in a single directory, so we need a way to specify where to look for files that are being included.

One option is to use relative paths, but another option is to give our program a list of directories to look in. This is called a **search path**, and many programs use them, including Node itself. By convention, a search path is written as a colon-separated list of directories on Unix or using semi-colons on Windows. If the path to an included file starts with ./, we look for it locally; if not, we go through the directories in the search path in order until we find a file with a matching name ([Figure 12.4](#chapter12.xhtml_fig12_4)).

![](images/fig12_4.jpg)

[Figure 12.4:](#chapter12.xhtml_b12fig12_4) Using a colon-separated list of directories as a search path.

Since the cache is responsible for finding files, it should also handle the search path. The outline of the class stays the same:

![](images/comp12_21.jpg)

To get the search path, we look for the **shell variable** NEED_PATH. (Writing shell variables’ names in upper case is another convention.) If NEED_PATH exists, we split it on colons to create a list of directories:

![](images/comp12_22.jpg)

When we need to find a file we first check to see if the path is local. If it's not, we try the directories in the search path in order:

![](images/comp12_23.jpg)

To test this, we put the file to import in a subdirectory called modules:

![](images/comp12_24.jpg)

and then put the file doing the importing in the current directory:

![](images/comp12_25.jpg)

We now need to set the variable NEED_PATH. There are many ways to do this in shell; if we only need the variable to exist for a single command, the simplest is to write it as:

![](images/comp12_26.jpg)

right before the command (on the same line). Here's the shell command that runs our test case using $PWD to get the current working directory:

![](images/comp12_27.jpg)![](images/comp12_28.jpg)

Now let's create a second importable file in the modules directory:

![](images/comp12_29.jpg)

and load that twice to check that caching works:

![](images/comp12_30.jpg)![](images/comp12_31.jpg)

## 12.4. How can we interpolate pieces of code?

Interpolating files is straightforward once we have this machinery in place. We modify Cache.find to return a directory and a file path, then add an interpolate method to replace special comments:

![](images/comp12_32.jpg)

We can now have a file like this:

![](images/comp12_33.jpg)

and subfiles like this:

![](images/comp12_34.jpg)

and this:

![](images/comp12_35.jpg)

Let's test it:

![](images/comp12_36.jpg)![](images/comp12_37.jpg)

When this program runs, its lifecycle is:

1.  Node starts to run test-import-interpolate.js.

2.  It sees the import of need-interpolate so it reads and evaluates that code.

3.  Doing this creates a singleton cache object.

4.  The program then calls need(’./import-interpolate.js’).

5.  This checks the cache: nope, nothing there.

6.  So it loads import-interpolate.js.

7.  It finds two specially-formatted comments in the text…

8.  …so it loads the file described by each one and inserts the text in place of the comment.

9.  Now that it has the complete text, it calls eval…

10.  …and stores the result of eval (which is a class) in the cache.

11.  It also returns that class.

12.  We then create an instance of that class and call its method.

This works, but as we said in the introduction we decided not to use it because it didn't play well with other tools. No piece of software exists in isolation; when we evaluate a design, we always have to ask how it fits into everything else we have.

## 12.5. What did we do instead?

Rather than interpolating file fragments, we extract or erase parts of regular JavaScript files based on specially formatted comments like the < fragment >... < /fragment > pair shown below.

![](images/comp12_38.jpg)

The code that selects the part of the file we want to display is part of our page templating system. It re-extracts code for display every time the web version of this site is built, which ensures that we always shows what's in the current version of our examples. However, this system doesn't automatically update the description of the code: if we write, “It does X,” then modify the code to do Y, our lesson can be inconsistent. **Literate programming** was invented to try to prevent this from happening, but it never really caught on—unfortunately, most programming systems that describe themselves as “literate” these days only implement part of Donald Knuth's[³](#chapter12.xhtml_fn12_3) original vision.

## 12.6. Exercises

### Security concerns

1.  Write a function loadAndRun that reads a file, evaluates it, and returns the result.

2.  Create a file trust-me.js that prints “nothing happening here” when it is evaluated, but also deletes everything in the directory called target.

3.  Write tests for this using [mock-fs][node-mock-fs][⁴](#chapter12.xhtml_fn12_4).

Please be careful doing this exercise.

### Loading functions

Write a function that reads a file containing single-argument functions like this:

![](images/comp12_39.jpg)

and returns an object containing callable functions.

### Registering functions

Write a function that loads one or more files containing function definitions like this:

![](images/comp12_40.jpg)

and returns a list containing all the loaded functions.

### Indenting inclusions

Modify the file inclusion system so that inclusions are indented by the same amount as the including comment. For example, if the including file is:

![](images/comp12_41.jpg)

and the included file is:

![](images/comp12_42.jpg)

then the result will be:

![](images/comp12_43.jpg)

i.e., all lines of the inclusion will be indented to match the first.

### Interpolating from subdirectories

Modify the file interpolator so that snippets can be included from sub-directories using relative paths.

### Recursive search for inclusions

1.  Modify the file interpolator so that it searches recursively through all subdirectories of the directories on the search path to find inclusions.

2.  Explain why this is a bad idea.

### Defining variables

Modify the file inclusion system so that users can pass in a Map containing name-value pairs and have these interpolated into the text of the files being loaded. To interpolate a value, the included file must use name@@.

### Specifying markers

Modify the file inclusion system so that the user can override the inclusion comment markers. For example, the user should be able to specify that /*! and !*/ be used to mark inclusions. (This is often used in tutorials that need to show the inclusion markers without them being interpreted.)

### Recursive inclusions

Modify the file interpolator to support recursive includes, i.e., to handle inclusion markers in files that are being included. Be sure to check for the case of infinite includes.

### Slicing files

Write a function that reads a JavaScript source file containing specially-formatted comments like the ones shown below and extracts the indicated section.

![](images/comp12_44.jpg)

Users should be able to specify any tag they want, and if that tag occurs multiple times, all of the sections marked with that tag should be kept. (This is the approach we took for this book instead of file interpolation.)

# 13Module Loader

Terms defined: **[absolute path](#appendix5.xhtml_d2)**, **[alias](#appendix5.xhtml_d9)**, **[circular dependency](#appendix5.xhtml_d48)**, **[closure](#appendix5.xhtml_d51)**, **[directed graph](#appendix5.xhtml_d87)**, **[encapsulate](#appendix5.xhtml_d101)**, **[immediately-invoked function expression](#appendix5.xhtml_d143)**, **[inner function](#appendix5.xhtml_d147)**, **Least Recently Used cache**, **[namespace](#appendix5.xhtml_d191)**, **[plugin architecture](#appendix5.xhtml_d213)**

[Chapter 12](#chapter12.xhtml) showed how to use eval to load code dynamically. We can use this to build our own version of JavaScript's require function. Our function will take the name of a source file as an argument and return whatever that file exports. The key requirement for such a function is to avoid accidentally overwriting things: if we just eval some code and it happens to assign to a variable called x, anything called x already in our program might be overwritten. We therefore need a way to **encapsulate** the contents of what we're loading. Our approach is based on [Casciaro2020], which contains a lot of other useful information as well.

## 13.1. How can we implement namespaces?

A **namespace** is a collection of names in a program that are isolated from other namespaces. Most modern languages provide namespaces as a built-in feature so that programmers don't accidentally step on each other's toes. JavaScript doesn't, so we have to implement them ourselves.

We can do this using **closures**. Every function is a namespace: variables defined inside the function are distinct from variables defined outside it ([Figure 13.1](#chapter13.xhtml_fig13_1)). If we create the variables we want to manage inside a function, then define another function inside the first and return that **inner function**, that inner function will be the only thing with references to those variables.

![](images/fig13_1.jpg)

[Figure 13.1:](#chapter13.xhtml_b13fig13_1) Using closures to create private variables.

For example, let's create a function that always appends the same string to its argument:

![](images/comp13_1.jpg)

When we run it, the value that was assigned to the parameter suffix still exists but can only be reached by the inner function:

![](images/comp13_2.jpg)

We could require every module to define a setup function like this for users to call, but thanks to eval we can wrap the file's contents in a function and call it automatically. To do this we will create something called an **immediately-invoked function expression** (IIFE). The syntax () = > {...} defines a function. If we put the definition in parentheses and then put another pair of parentheses right after it:

![](images/comp13_3.jpg)

we have code that defines a function of no arguments and immediately calls it. We can use this trick to achieve the same effect as the previous example in one step:

![](images/comp13_4.jpg)![](images/comp13_5.jpg)

## 13.2. How can we load a module?

We want the module we are loading to export names by assigning to module.exports just as require does, so we need to provide an object called module and create a IIFE. (We will handle the problem of the module loading other modules later.) Our loadModule function takes a filename and returns a newly created module object; the parameter to the function we build and eval must be called module so that we can assign to module.exports. For clarity, we call the object we pass in result in loadModule.

![](images/comp13_7.jpg)

[Figure 13.2](#chapter13.xhtml_fig13_2) and [Figure 13.3](#chapter13.xhtml_fig13_3) show the structure of our loader so far. We can use this code as a test:

![](images/comp13_8.jpg)![](images/fig13_2.jpg)

[Figure 13.2:](#chapter13.xhtml_b13fig13_2) Using IIFEs to encapsulate modules and get their exports (part 1).

![](images/fig13_3.jpg)

[Figure 13.3:](#chapter13.xhtml_b13fig13_3) Using IIFEs to encapsulate modules and get their exports (part 2).

and this short program to load the test and check its exports:

![](images/comp13_9.jpg)![](images/comp13_10.jpg)![](images/comp13_11.jpg)

## 13.3. Do we need to handle circular dependencies?

What if the code we are loading loads other code? We can visualize the network of who requires whom as a **directed graph**: if X requires Y, we draw an arrow from X to Y. Unlike the directed *acyclic* graphs we met in [Chapter 10](#chapter10.xhtml), though, these graphs can contain cycles: we say a **circular dependency** exists if X depends on Y and Y depends on X either directly or indirectly. This may seem nonsensical, but can easily arise with **plugin architectures**: the file containing the main program loads an extension, and that extension calls utility functions defined in the file containing the main program.

Most compiled languages can handle circular dependencies easily: they compile each module into low-level instructions, then link those to resolve dependencies before running anything ([Figure 13.4](#chapter13.xhtml_fig13_4)). But interpreted languages usually run code as they're loading it, so if X is in the process of loading Y and Y tries to call X, X may not (fully) exist yet.

![](images/fig13_4.jpg)

[Figure 13.4:](#chapter13.xhtml_b13fig13_4) Testing circular imports.

Circular dependencies work in Python[¹](#chapter13.xhtml_fn13_1), but only sort of. Let's create two files called major.py and minor.py:

![](images/comp13_12.jpg)![](images/comp13_13.jpg)

Loading fails when we run major.py from the command line:

![](images/comp13_14.jpg)

but works in the interactive interpreter:

![](images/comp13_15.jpg)

The equivalent test in JavaScript also has two files:

![](images/comp13_16.jpg)![](images/comp13_17.jpg)

It fails on the command line:

![](images/comp13_18.jpg)

and also fails in the interactive interpreter (which is more consistent):

![](images/comp13_19.jpg)

We therefore won't try to handle circular dependencies. However, we will detect them and generate a sensible error message.

## 13.4. How can a module load another module?

While we're not going to handle circular dependencies, modules do need to be able to load other modules. To enable this, we need to provide the module with a function called require that it can call as it loads. As in [Chapter 12](#chapter12.xhtml), this function checks a cache to see if the file being asked for has already been loaded. If not, it loads it and saves it; either way, it returns the result.

Our cache needs to be careful about how it identifies files so that it can detect duplicates loading attempts that use different names. For example, suppose that major.js loads subdir/first.js and subdir/second.js. When subdir/second.js loads ./first.js, our system needs to realize that it already has that file even though the path looks different. We will use **absolute paths** as cache keys so that every file has a unique, predictable key.

To reduce confusion, we will call our function need instead of require. In order to make the cache available to modules while they're loading, we will make it a property of need. (Remember, a function is just another kind of object in JavaScript; every function gets several properties automatically, and we can always add more.) Since we're using the built-in Map class as a cache, the entire implementation of need is just 15 lines long:

![](images/comp13_20.jpg)

We now need to modify loadModule to take our function need as a parameter. (Again, we'll have our modules call need(’something.js’) instead of require(’something’) for clarity.) Let's test it with the same small module that doesn't need anything else to make sure we haven't broken anything:

![](images/comp13_21.jpg)![](images/comp13_22.jpg)

What if we test it with a module that *does* load something else?

![](images/comp13_23.jpg)![](images/comp13_24.jpg)![](images/comp13_25.jpg)

This doesn't work because import only works at the top level of a program, not inside a function. Our system can therefore only run loaded modules by needing them:

![](images/comp13_26.jpg)![](images/comp13_27.jpg)![](images/comp13_28.jpg)

## 13.5. Exercises

### Counting with closures

Write a function makeCounter that returns a function that produces the next integer in sequence starting from zero each time it is called. Each function returned by makeCounter must count independently, so:

![](images/comp13_29.jpg)

must produce:

![](images/comp13_30.jpg)

### Objects and namespaces

A JavaScript object stores key-value pairs, and the keys in one object are separate from the keys in another. Why doesn't this provide the same level of safety as a closure?

### Testing module loading

Write tests for need.js using Mocha and mock-fs.

### Using module as a name

What happens if we define the variable module in loadModule so that it is in scope when eval is called rather than creating a variable called result and passing that in:

![](images/comp13_31.jpg)

### Implementing a search path

Add a search path to need.js so that if a module isn't found locally, it will be looked for in each directory in the search path in order.

### Using a setup function

Rewrite the module loader so that every module has a function called setup that must be called after loading it to create its exports rather than using module.exports.

### Handling errors while loading

1.  Modify need.js so that it does something graceful if an exception is thrown while a module is being loaded.

2.  Write unit tests for this using Mocha.

### Refactoring circularity

Suppose that main.js contains this:

![](images/comp13_32.jpg)

and plugin.js contains this:

![](images/comp13_33.jpg)

Refactor this code so that it works correctly while still using require rather than import.

### An LRU cache

A **Least Recently Used (LRU) cache** reduces access time while limiting the amount of memory used by keeping track of the N items that have been used most recently. For example, if the cache size is 3 and objects are accessed in the order shown in the first column, the cache's contents will be as shown in the second column:

| **Item** | **Action** | **Cache After Access** |
| A | read A | [A] |
| A | get A from cache | [A] |
| B | read B | [B, A] |
| A | get A from cache | [A, B] |
| C | read C | [C, A, B] |
| D | read D | [D, C, A] |
| B | read B | [B, D, C] |

1.  Implement a function cachedRead that takes the number of entries in the cache as an argument and returns a function that uses an LRU cache to either read files or return cached copies.

2.  Modify cachedRead so that the number of items in the cache is determined by their combined size rather than by the number of files.

### Make functions safe for renaming

Our implementation of need implemented the cache as a property of the function itself.

1.  How can this go wrong? (Hint: thing about aliases.)

2.  Modify the implementation to solve this problem using a closure.

# 14Style Checker

Terms defined: **[abstract syntax tree](#appendix5.xhtml_d4)**, **[Adapter pattern](#appendix5.xhtml_d8)**, **[column-major storage](#appendix5.xhtml_d55)**, **[dynamic lookup](#appendix5.xhtml_d94)**, **[generator function](#appendix5.xhtml_d124)**, **[intrinsic complexity](#appendix5.xhtml_d153)**, **[Iterator pattern](#appendix5.xhtml_d156)**, **[linter](#appendix5.xhtml_d169)**, **[Markdown](#appendix5.xhtml_d182)**, **[row-major storage](#appendix5.xhtml_d238)**, **[walk (a tree)](#appendix5.xhtml_d301)**

Programmers argue endlessly about the best way to format their programs, but everyone agrees that the most important thing is to be consistent [Binkley2012, Johnson2019]. Since checking rules by hand is tedious, most programmers use tools to compare code against various rules and report any violations. Programs that do this are often called **linters** in honor of an early one for C named lint (because it looked for fluff in source code).

In this chapter we will build a simple linter of our own inspired by ESLint[¹](#chapter14.xhtml_fn14_1), which we use to check the code in this book. Our tool will parse source code to create a data structure, then go through that data structure and apply rules for each part of the program. It will also introduce us to one of the key ideas of this book, which is that source code is just another kind of data.

## 14.1. How can we parse JavaScript to create an AST?

A parser for a simple language like arithmetic or JSON is relatively easy to write. A parser for a language as complex as JavaScript is much more work, so we will use one called Acorn[³](#chapter14.xhtml_fn14_3) instead. Acorn takes a string containing source code as input and produces an **abstract syntax tree** (AST) whose nodes store information about what's in the program ([Figure 14.1](#chapter14.xhtml_fig14_1)). An AST is for a program what the DOM is for HTML: an in-memory representation that is easy for software to inspect and manipulate.

![](images/fig14_1.jpg)

[Figure 14.1:](#chapter14.xhtml_b14fig14_1) The parse tree of a simple program.

ASTs can be quite complex—for example, the JSON representation of the AST for a single constant declaration is 84 lines long:

![](images/comp14_1.jpg)![](images/comp14_2.jpg)

Acorn's output is in Esprima[⁴](#chapter14.xhtml_fn14_4) format (so-called because it was originally defined by a tool with that name). The format's specification is very detailed, but we can usually figure out most of what we need by inspection. For example, here is the output for a 15-line program:

![](images/comp14_3.jpg)![](images/comp14_4.jpg)

Yes, it really is almost 500 lines long…

## 14.2. How can we find things in an AST?

If we want to find functions, variables, or anything else in an AST we need to **walk the tree**, i.e., to visit each node in turn. The acorn-walk[⁵](#chapter14.xhtml_fn14_5) library will do this for us using the Visitor design pattern we first saw in [Chapter 9](#chapter9.xhtml). If we provide a function to act on nodes of type Identifier, acorn-walk will call that function each time it finds an identifier. We can use other options to say that we want to record the locations of nodes (i.e., their line numbers) and to collect comments in an array called onComment. Our function can do whatever we want; for demonstration purposes we will add nodes to an array called state and report them all at the end ([Figure 14.2](#chapter14.xhtml_fig14_2)).

![](images/comp14_5.jpg)![](images/comp14_6.jpg)![](images/fig14_2.jpg)

[Figure 14.2:](#chapter14.xhtml_b14fig14_2) Walking a tree to perform an operation at each node.

## 14.3. How can we apply checks?

We don't just want to collect nodes: we want to check their properties against a set of rules. One way to do this would be to call walk.simple once for each rule, passing it a function that checks just that rule. Another way—the one we'll use—is to write a generic function that checks a rule and records any nodes that don't satisfy it, and then call that function once for each rule inside our Identifier handler. This may seem like extra work, but it ensures that all of our rule-checkers store their results in the same way, which in turn means that we can write one reporting function and be sure it will handle everything.

The function applyCheck takes the current state (where we are accumulating rule violations), a label that identifies this rule (so that violations of it can be stored together), the node, and a logical value telling it whether the node passed the test or not. If the node failed the test we make sure that state contains a list with the appropriate label and then append this node to it. This “create storage space on demand” pattern is widely used but doesn't have a well-known name.

![](images/comp14_7.jpg)

We can now put a call to applyCheck inside the handler for Identifier:

![](images/comp14_8.jpg)

We can't just use applyCheck as the handler for Identifier because walk.simple wouldn't know how to call it. This is a (very simple) example of the **Adapter** design pattern: we write a function or class to connect the code we want to call to the already-written code that is going to call it.

The output for the same sample program as before is:

![](images/comp14_9.jpg)

The exercises will ask why the parameter x doesn't show up as a violation of our rule that variables’ names must be at least four characters long.

## 14.4. How does the AST walker work?

The AST walker uses the Visitor pattern, but how does it actually work? We can build our own by defining a class with methods that walk the tree, take action depending on the kind of node, and then go through the children of that node (if any). The user can then derive a class of their own from this and override the set of action methods they're interested in.

One key difference between our implementation and acorn-walk‘s is that our methods don't need to take state as a parameter because it's contained in the object that they're part of. That simplifies the methods—one less parameter—but it does mean that anyone who wants to use our visitor has to derive a class, which is a bit more complicated than writing a function. This tradeoff is a sign that managing state is part of the problem's **intrinsic complexity**: we can move it around, but we can't get rid of it.

The other difference between our visitor and acorn-walk is that our class uses **dynamic lookup** (a form of introspection) to look up a method with the same name as the node type in the object. While we normally refer to a particular method of an object using object.method, we can also look them up by asking for object[name] in the same way that we would look up any other property of any other object. Our completed class looks like this:

![](images/comp14_10.jpg)

The code we need to use it is:

![](images/comp14_11.jpg)

and its output is:

![](images/comp14_12.jpg)

We think this approach to implementing the Visitor pattern is easier to understand and extend than one that relies on callbacks, but that could just be a reflection of our background and experience. As with code style, the most important thing is consistency: if we implement Visitor using classes in one place, we should implement it that way everywhere.

## 14.5. How else could the AST walker work?

A third approach to this problem uses the **Iterator** design pattern. Instead of taking the computation to the nodes, an iterator returns the elements of a structure for processing ([Figure 14.3](#chapter14.xhtml_fig14_3)). One way to think about it is that Visitor encapsulates recursion, while Iterator turns everything into a loop.

![](images/fig14_3.jpg)

[Figure 14.3:](#chapter14.xhtml_b14fig14_3) Finding nodes in the tree using the Iterator pattern.

We can implement the Iterator pattern in JavaScript using **generator functions**. If we declare a function using function * (with an asterisk) instead of function then we can use the yield keyword to return a value and suspend processing to be resumed later. The result of yield is a two-part structure with a value and a flag showing whether or not processing is done:

![](images/comp14_13.jpg)![](images/comp14_14.jpg)

As another example, this generator takes a string and produces its vowels one by one:

![](images/comp14_15.jpg)![](images/comp14_16.jpg)

A generator function doesn't actually generate anything; instead, it creates an object that we can then ask for values repeatedly. This gives us a way to have several generators in play at the same time.

Instead of a while loop it is much more common to use for...of, which knows how to work with generators:

![](images/comp14_17.jpg)

Finally, just as function * says “this function is a generator”, yield * says “yield the values from a nested generator one by one”. We can use it to walk irregular structures like nested arrays:

![](images/comp14_18.jpg)

Let's use generators to count the number of expressions of various types in a program. The generator function that visits each node is:

![](images/comp14_19.jpg)

and the program that uses it is:

![](images/comp14_20.jpg)

When we run it with our usual test program as input, we get:

![](images/comp14_21.jpg)

Generators are a clean solution to many hard problems, but we find it more difficult to check variable identifiers using generators than using the class-based Visitor approach because we want to accumulate violations to report later. Again, this could be a reflection of what we're used to rather than anything intrinsic; as with coding style, the most important thing is to be consistent.

## 14.6. What other kinds of analysis can we do?

As one final example, consider the problem of keeping track of which methods are defined where in a deeply nested class hierarchy. (This problem comes up in some of the later chapters in this book: we wrote so many classes that incrementally extended their predecessors for pedagogical purposes that we lost track of what was defined where.) To create a table of method definitions, we first need to find the ancestors of the last class in the hierarchy:

![](images/comp14_22.jpg)

Finding class definitions is a straightforward extension of what we have already done:

![](images/comp14_23.jpg)

To test this code, we start with the last of these three short files:

![](images/comp14_24.jpg)![](images/comp14_25.jpg)![](images/comp14_26.jpg)![](images/comp14_27.jpg)

Good: we can recover the chain of inheritance. Finding method definitions is also straightforward:

![](images/comp14_28.jpg)

And finally, we can print a **Markdown**-formatted table showing which methods are defined in which class:

![](images/comp14_29.jpg)

which renders as:

| **[method](#appendix5.xhtml_d184)** | **Upper** | **Middle** | **Lower** |
| additional | . | . | X |
| constructor | X | X | . |
| modify | X | X | . |
| report | X | . | X |

This may seem rather pointless for our toy example, but it proves its worth when we are looking at something like the virtual machine we will build in [Chapter 19](#chapter19.xhtml), which has a more complex method definition table:

| **method** | **Base** | **Interactive** | **Test** | **Exit** |
| clear | . | X | . | . |
| constructor | X | X | X | . |
| exit | . | X | . | X |
| getCommand | . | X | . | . |
| handle | . | X | . | . |
| help | . | X | . | . |
| input | . | X | X | . |
| interact | . | X | . | . |
| list | . | X | . | . |
| message | X | . | X | . |
| next | . | X | . | . |
| print | . | X | . | . |
| run | . | X | . | . |
| setTester | . | . | X | . |
| setVM | X | . | . | . |
| stop | . | X | . | . |
| variables | . | X | . | . |

## 14.7. Exercises

### Function length

Derive a class from Walker that reports the length in lines of each function defined in the code being checked.

### Expression depth

Derive a class from Walker that reports how deep each top-level expression in the source code is. For example, the depth of 1 + 2 * 3 is 2, while the depth of max(1 + 2 + 3) is 3 (one level for the function call, one for the first addition, and one for the nested addition).

### Downward and upward

Modify Walker so that users can specify one action to take at a node on the way down the tree and a separate action to take on the way up. (Hint: require users to specify Nodename_downward and/or Nodename_upward methods in their class, then use string concatenation to construct method names while traversing the tree.)

### Aggregating across files

Create a command-line program called sniff.js that checks for style violations in any number of source files. The first command-line argument to sniff.js must be a JavaScript source file that exports a class derived from Walker called Check that implements the checks the user wants. The other command-line arguments must be the names of JavaScript source files to be checked:

![](images/comp14_30.jpg)

### Finding assertions

Write a program find-assertions.js that finds all calls to assert or assert.something and prints the assertion message (if any).

### Finding a missing parameter

1.  Why doesn't the parameter x show up as a rule violation in the example where we check name lengths?

2.  Modify the example so that it does.

### Finding nested indexes

Write a tool that finds places where nested indexing is used, i.e., where the program contains expressions like arr[table[i]].

### Dynamic lookup

1.  Write a function dynamicExecution that takes an object, the name of a method, and zero or more parameters as arguments and calls that method on that object:

    ![](images/comp14_31.jpg)
2.  What *doesn't* this work for?

### Generators and arrays

1.  Write a generator that takes a two-dimensional table represented as an array of arrays and returns the values in **column-major** order.

2.  Write another generator that takes a similar table and returns the values in **row-major** order.

### Generators and identifiers

Rewrite the tool to check identifier lengths using a generator.

# 15Code Generator

Terms defined: **[byte code](#appendix5.xhtml_d37)**, **[code coverage (in testing)](#appendix5.xhtml_d52)**, **[compiler](#appendix5.xhtml_d63)**, **[Decorator pattern](#appendix5.xhtml_d75)**, **[macro](#appendix5.xhtml_d179)**, **[nested function](#appendix5.xhtml_d192)**, **[two hard problems in computer science](#appendix5.xhtml_d291)**

We've been writing tests since [Chapter 4](#chapter4.xhtml), but how much of our code do they actually check? One way to find out is to use a **code coverage** tool like Istanbul[¹](#chapter15.xhtml_fn15_1) that watches a program while it executes and keeps track of which lines have run and which haven't. Making sure that each line is tested at least once doesn't guarantee that the code is bug-free, but any code that *isn't* run shouldn't be trusted.

Our code coverage tool will keep track of which functions have and haven't been called. Rather than rewriting Node[²](#chapter15.xhtml_fn15_2) to keep track of this for us, we will modify the functions themselves by parsing the code with Acorn[³](#chapter15.xhtml_fn15_3), inserting the instructions we need into the AST, and then turning the AST back into code.

## 15.1. How can we replace a function with another function?

The first thing we need is a way to wrap up an arbitrary function call. If we declare a function in JavaScript with a parameter like ...args, all of the “extra” arguments in the call that don't line up with regular parameters are stuffed into the variable args ([Figure 15.1](#chapter15.xhtml_fig15_1)). We can also call a function by putting values in a variable and using func(...var) to spread those values out. There's nothing special about the names args and vars: what matters is the ellipsis ...

![](images/fig15_1.jpg)

[Figure 15.1:](#chapter15.xhtml_b15fig15_1) Using …args to capture and spread parameters.

We can use ...args to capture all of the arguments to a function call and forward them to another function. Let's start by creating functions with a varying number of parameters that run to completion or throw an exception, then run them to make sure they do what we want:

![](images/comp15_1.jpg)

We can now write a function that takes a function as an input and creates a new function that handles all of the errors in the original function:

![](images/comp15_2.jpg)

Let's try it out:

![](images/comp15_3.jpg)

This is an example of the **Decorator** design pattern. A decorator is a function whose job is to modify the behavior of other functions in some general ways. Decorators are built in to some languages (like Python[⁴](#chapter15.xhtml_fn15_4)), and we can add them in most others as we have done here.

## 15.2. How can we generate JavaScript?

We could use a decorator to replace every function in our program with one that keeps track of whether or not it was called, but it would be tedious to apply the decorator to every one of our functions by hand. What we really want is a way to do this automatically for everything, and for that we need to parse and generate code.

Our tool will parse the JavaScript with Acorn to create an AST, modify the AST, and then use a library called Escodegen[⁶](#chapter15.xhtml_fn15_6) to turn the AST back into JavaScript. To start, let's look at the AST for a simple function definition, which is 75 lines of pretty-printed JSON:

![](images/comp15_4.jpg)![](images/comp15_5.jpg)![](images/comp15_5_2.jpg)

After inspecting a few nodes, we can create some of our own and turn them into code. Here, for example, we have the JSON representation of the expression 40+2:

![](images/comp15_6.jpg)![](images/comp15_7.jpg)

## 15.3. How can we count how often functions are executed?

Our tool will find all the function declaration nodes in the program and insert a node to increment an entry in a global variable called _ _ counters. (Prefixing the name with two underscores doesn't guarantee that we won't accidentally clobber a variable in the user's program with the same name, but hopefully it makes that less likely.) Our test case is:

![](images/comp15_8.jpg)

and the main function of our program is:

![](images/comp15_9.jpg)

To insert a count we call insertCounter to record the function's name and modify the node:

![](images/comp15_10.jpg)

Notice how we don't try to build the nodes by hand, but instead construct the string we need, use Acorn to parse that, and use the result. Doing this saves us from embedding multiple lines of JSON in our program and also ensures that if a newer version of Acorn decides to generate a different AST, our program will do the right thing automatically.

Finally, we need to add a couple of helper functions:

![](images/comp15_11.jpg)

and run it to make sure it all works:

![](images/comp15_12.jpg)

## 15.4. How can we time function execution?

Now that we have a way to insert code into functions we can use it to do many other things. For example, we can find out how long it takes functions to run by wrapping them up in code that records the start and end time of each call. As before, we find the nodes of interest and decorate them, then stitch the result together with a bit of bookkeeping:

![](images/comp15_13.jpg)

Gathering nodes is straightforward:

![](images/comp15_14.jpg)

as is wrapping the function definition:

![](images/comp15_15.jpg)

The only big difference is how we make the wrapper function. We create it with a placeholder for the original function so that we have a spot in the AST to insert the actual code:

![](images/comp15_16.jpg)

Let's run one last test:

![](images/comp15_17.jpg)

Source-to-source translation is widely used in JavaScript: tools like Babel[⁷](#chapter15.xhtml_fn15_7) use it to transform modern features like async and await ([Chapter 3](#chapter3.xhtml)) into code that older browsers can understand. The technique is so powerful that it is built into languages like Scheme, which allow programmers to add new syntax to the language by defining **macros**. Depending on how carefully they are used, macros can make programs elegant, incomprehensible, or both.

## 15.5. Exercises

### JSON to JavaScript

Write a tool that uses Escodegen[⁸](#chapter15.xhtml_fn15_8) to translate simple expressions written in JSON into runnable JavaScript. For example, the tool should translate:

![](images/comp15_18.jpg)

into:

![](images/comp15_19.jpg)

### JavaScript to HTML

Write a function that takes nested JavaScript function calls for generating HTML like this:

![](images/comp15_20.jpg)

and turns them into HTML like this:

![](images/comp15_21.jpg)

### Handling modules

Modify the code that counts the number of times a function is called to handle functions with the same name from different modules.

### Tracking calls

Write a decorator that takes a function as its argument and returns a new function that behaves exactly the same way except that it keeps track of who called it.

1.  The program contains a stack where decorated functions push and pop their names as they are called and as they exit.

2.  Each time a function is called it adds a record to an array to record its name and the name at the top of the stack (i.e., the most-recently-called decorated function).

### Counting classical function definitions

Modify the code generator to handle functions declared with the function keyword as well as functions declared using = >.

### Recording input file size

1.  Write a program that replaces all calls to fs.readFileSync with calls to readFileSyncCount.

2.  Write the function readFileSyncCount to read and return a file using fs.readFileSync but to also record the file's name and size in bytes.

3.  Write a third function reportInputFileSizes that reports what files were read and how large they were.

4.  Write tests for these functions using Mocha and mock-fs.

### Checking argument types

Write a tool that modifies functions to check the types of their arguments at run-time.

1.  Each function is replaced by a function that passes all of its arguments to checkArgs along with the function's name, then continues with the function's original operation.

2.  The first time checkArgs is called for a particular function it records the actual types of the arguments.

3.  On subsequent calls, it checks that the argument types match those of the first call and throws an exception if they do not.

### Two-dimensional arrays

The function make2D takes a row length and one or more values and creates a two-dimensional array from those values:

![](images/comp15_22.jpg)

Write a function that searches code to find calls to make2D and replaces them with inline arrays-of-arrays. This function only has to work for calls with a fixed row length, i.e., it does *not* have to handle make2D(N, ’a’, ’b’).

### From require to import

Write a function that searches code for simple calls to require and replaces them with calls to import. This function only needs to work for the simplest case; for example, if the input is:

![](images/comp15_23.jpg)

then the output is:

![](images/comp15_24.jpg)

### Removing empty constructors

Write a function that removes empty constructors from class definitions. For example, if the input is:

![](images/comp15_25.jpg)

then the output should be:

![](images/comp15_26.jpg)

# 16Documentation Generator

Terms defined: **[accumulator](#appendix5.xhtml_d6)**, **[block comment](#appendix5.xhtml_d28)**, **[deprecation](#appendix5.xhtml_d79)**, **[doc comment](#appendix5.xhtml_d90)**, **[line comment](#appendix5.xhtml_d167)**, **[slug](#appendix5.xhtml_d258)**

Many programmers believe they're more likely to write documentation and keep it up to date if it is close to the code. Tools that extract specially-formatted comments from code and turn them into documentation have been around since at least the 1980s; many are used for JavaScript, including JSDoc[¹](#chapter16.xhtml_fn16_1) and ESDoc[²](#chapter16.xhtml_fn16_2). This chapter will use what we learned in [Chapter 15](#chapter15.xhtml) about parsing source code to build a simple documentation generator of our own.

## 16.1. How can we extract documentation comments?

We will use Acorn[³](#chapter16.xhtml_fn16_3) once again to parse our source files. This time we will use the parser's onComment option, giving it an array to fill in. For the moment we won't bother to assign the AST produced by parsing to a variable because we are just interested in the comments:

![](images/comp16_1.jpg)![](images/comp16_2.jpg)![](images/comp16_3.jpg)

There is more information here than we need, so let's slim down the JSON that we extract:

![](images/comp16_4.jpg)![](images/comp16_5.jpg)![](images/comp16_6.jpg)

Acorn distinguishes two kinds of comments ([Figure 16.1](#chapter16.xhtml_fig16_1)). **Line comments** cannot span multiple lines; if one line comment occurs immediately after another, Acorn reports two comments:

![](images/comp16_7.jpg)![](images/comp16_8.jpg)![](images/comp16_9.jpg)![](images/fig16_1.jpg)

[Figure 16.1:](#chapter16.xhtml_b16fig16_1) How line comments and block comments are distinguished and represented.

**Block comments**, on the other hand, can span any number of lines. We don't need to prefix each line with * but most people do for readability:

![](images/comp16_10.jpg)![](images/comp16_11.jpg)![](images/comp16_12.jpg)

By convention, we use block comments that start with /** for documentation. The first two characters are recognized by the parser as “start of comment”, so the first character in the extracted text is *:

![](images/comp16_13.jpg)![](images/comp16_14.jpg)

## 16.2. What input will we try to handle?

We will use Markdown[⁴](#chapter16.xhtml_fn16_4) for formatting our documentation. The **doc comments** for function definitions look like this:

![](images/comp16_15.jpg)

while the ones for class definitions look like this:

![](images/comp16_16.jpg)

The doc comments are unpleasant at the moment: they repeat the function and method names from the code, we have to create titles ourselves, and we have to remember the back-quotes for formatting code. We will fix some of these problems once we have a basic tool up and running.

The next step in doing that is to translate Markdown into HTML. There are many Markdown parsers in JavaScript; after experimenting with a few, we decided to use markdown-it[⁵](#chapter16.xhtml_fn16_5) along with the markdown-it-anchor[⁶](#chapter16.xhtml_fn16_6) extension that creates HTML anchors for headings. The main program gets all the doc comments from all of the input files, converts the Markdown to HTML, and displays that:

![](images/comp16_17.jpg)

To get all the comments, we extract comments from all the files, remove the leading * characters (which aren't part of the documentation), and then join the results after stripping off extraneous blanks:

![](images/comp16_18.jpg)

Extracting the comments from a single file is done as before:

![](images/comp16_19.jpg)

and removing the prefix * characters is a matter of splitting the text into lines, removing the leading spaces and asterisks, and putting the lines back together:

![](images/comp16_20.jpg)

One thing that isn't in this file (because we're going to use it in later versions) is the function slugify. A **slug** is a short string that identifies a header or a web page; the name comes from the era of newspapers, where a slug was a short name used to identify an article while it was in production. Our slugify function strips unnecessary characters out of a title, adds hyphens, and generally makes it something you might see in a URL:

![](images/comp16_21.jpg)

Let's run this generator and see what it produces ([Figure 16.3](#chapter16.xhtml_fig16_3) and [Figure 16.2](#chapter16.xhtml_fig16_2)):

![](images/comp16_22.jpg)![](images/comp16_23.jpg)![](images/fig16_2.jpg)

[Figure 16.2:](#chapter16.xhtml_b16fig16_2) How comments in code map to documentation in HTML.

![](images/fig16_3.jpg)

[Figure 16.3:](#chapter16.xhtml_b16fig16_3) The page produced by the documentation generator.

It works, but there is a double h1 header for each file (the filename and the title comment), the anchor IDs are hard to read, there are no cross-references, and so on. Some of the visual issues can be resolved with CSS, and we can change our input format to make processing easier as long as it also makes authoring easier. However, anything that is written twice will eventually be wrong in one place or another, so our first priority is to remove duplication.

## 16.3. How can we avoid duplicating names?

If a comment is the first thing in a file, we want to use it as title text; this will save us having to write an explicit level-1 title in a comment. For each other comment, we can extract the name of the function or method from the node on the line immediately following the doc comment. This allows us to write much tidier comments:

![](images/comp16_24.jpg)

To extract and display information from nodes immediately following doc comments we must find all the block comments, record the last line of each, and then search the AST to find nodes that are on lines immediately following any of those trailing comment lines. (We will assume for now that there are no blank lines between the comment and the start of the class or function.) The main program finds the comments as usual, creates a set containing the line numbers we are looking for, then searches for the nodes we want:

![](images/comp16_25.jpg)

The recursive search is straightforward as well—we delete line numbers from the target set and add nodes to the **accumulator** as we find matches:

![](images/comp16_26.jpg)

Finally, we use a function called condense to get the name we want out of the AST:

![](images/comp16_27.jpg)

We need this because we get a different structure with:

![](images/comp16_28.jpg)

than we get with:

![](images/comp16_29.jpg)

When we run this on our test case we get:

![](images/comp16_30.jpg)

We can use this to create better output ([Figure 16.4](#chapter16.xhtml_fig16_4)):

![](images/comp16_31.jpg)![](images/comp16_32.jpg)![](images/fig16_4.jpg)

[Figure 16.4:](#chapter16.xhtml_b16fig16_4) Filling in headers when generating documentation.

## 16.4. Code is Data

We haven't made this point explicitly in a while, so we will repeat it here: code is just another kind of data, and we can process it just like we would process any other data. Parsing code to produce an AST is no different from parsing HTML to produce DOM; in both cases we are simply transforming a textual representation that's easy for people to author into a data structure that's easy for a program to manipulate. Pulling things out of that data to create a report is no different from pulling numbers out of a hospital database to report monthly vaccination rates.

Treating code as data enables us to do routine programming tasks with a single command, which in turn gives us more time to think about the tasks that we can't (yet) automate. Doing this is the foundation of a tool-based approach to software engineering; as the mathematician Alfred North Whitehead once wrote, “Civilization advances by extending the number of important operations which we can perform without thinking about them.”

## 16.5. Exercises

### Building an index

Modify the documentation generator to produce an alphabetical index of all classes and methods found. Index entries should be hyperlinks to the documentation for the corresponding item.

### Documenting exceptions

Extend the documentation generator to allow people to document the exceptions that a function throws.

### Deprecation warning

Add a feature to the documentation generator to allow authors to mark functions and methods as **deprecation** (i.e., to indicate that while they still exist, they should not be used because they are being phased out).

### Usage examples

Enhance the documentation generator so that if a horizontal rule --- appears in a documentation comment, the text following is typeset as usage example. (A doc comment may contain several usage examples.)

### Unit testing

Write unit tests for the documentation generator using Mocha.

### Summarizing functions

Modify the documentation generator so that line comments inside a function that use //* are formatted as a bullet list in the documentation for that function.

### Cross referencing

Modify the documentation generator so that the documentation for one class or function can include Markdown links to other classes or functions.

### Data types

Modify the documentation generator to allow authors to define new data types in the same way as JSDoc[⁷](#chapter16.xhtml_fn16_7).

### Inline parameter documentation

Some documentation generators put the documentation for a parameter on the same line as the parameter:

![](images/comp16_33.jpg)

Modify the documentation generator to handle this.

### Tests as documentation

The doctest[⁸](#chapter16.xhtml_fn16_8) library for Python allows programmers to embed unit tests as documentation in their programs. Write a tool that:

1.  Finds functions that start with a block comment.

2.  Extracts the code and output from those blocks comments and turns them into assertions.

For example, given this input:

![](images/comp16_34.jpg)

the tool would produce:

![](images/comp16_35.jpg)

# 17Module Bundler

Terms defined: **[entry point](#appendix5.xhtml_d102)**, **[module bundler](#appendix5.xhtml_d188)**, **[transitive closure](#appendix5.xhtml_d287)**

JavaScript was designed in a hurry 25 years ago to make web pages interactive. Nobody realized it would become so popular, so it didn't include support for things that large programs need. One of those things was a way to turn a set of source files into a single file so that browsers could load what they needed with one request.

A **module bundler** finds all the files that an application depends on and combines them into a single loadable file ([Figure 17.1](#chapter17.xhtml_fig17_1)). This file is much more efficient to load: it's the same number of bytes but just one network request. (See [Table 2.1](#chapter2.xhtml_tbl2_1) for a reminder of why this is important.) Bundling files also tests that dependencies actually resolve so that the application has at least a chance of being able to run.

![](images/fig17_1.jpg)

[Figure 17.1:](#chapter17.xhtml_b17fig17_1) Combining multiple modules into one.

Bundling requires an **entry point**, i.e., a place to start searching for dependencies. Given that, it finds all dependencies, combines them into one file, and ensures they can find each other correctly once loaded. The sections below go through these steps one by one.

## 17.1. What will we use as test cases?

Our first test case is a single file that doesn't require anything:

![](images/comp17_1.jpg)![](images/comp17_2.jpg)

For our second test, main.js requires other.js:

![](images/comp17_3.jpg)

and other.js doesn't require anything:

![](images/comp17_4.jpg)

The output we expect is:

![](images/comp17_5.jpg)

Our third test case has multiple inclusions in multiple directories and is shown in [Figure 17.2](#chapter17.xhtml_fig17_2):

*   ./main requires all four of the files below.

*   ./top-left doesn't require anything.

*   ./top-right requires top-left and bottom-right.

*   ./subdir/bottom-left also requires top-left and bottom-right.

*   ./subdir/bottom-right doesn't require anything.

![](images/fig17_2.jpg)

[Figure 17.2:](#chapter17.xhtml_b17fig17_2) Dependencies in large module bundler test case.

The main program is:

![](images/comp17_6.jpg)

and the other four files use require and module.exports to get what they need. The output we expect is:

![](images/comp17_7.jpg)

We do not handle circular dependencies because require itself doesn't ([Chapter 13](#chapter13.xhtml)).

## 17.2. How can we find dependencies?

To get all the dependencies for one source file, we parse it and extract all of the calls to require. The code to do this is relatively straightforward given what we know about Acorn[¹](#chapter17.xhtml_fn17_1):

![](images/comp17_8.jpg)![](images/comp17_9.jpg)![](images/comp17_10.jpg)![](images/comp17_11.jpg)

To get all of the dependencies a bundle needs we need to find the **transitive closure** of the entry point's dependencies, i.e., the requirements of the requirements and so on recursively. Our algorithm for doing this uses two sets: pending, which contains the things we haven't looked at yet, and seen, which contains the things we have ([Figure 17.3](#chapter17.xhtml_fig17_3)). pending initially contains the entry point file and seen is initially empty. We keep taking items from pending until it is empty. If the current thing is already in seen we do nothing; otherwise we get its dependencies and add them to either seen or pending.

![](images/fig17_3.jpg)

[Figure 17.3:](#chapter17.xhtml_b17fig17_3) Implementing transitive closure using two sets.

Finding dependencies is complicated by the fact that we can load something under different names, such as ./subdir/bottom-left from main but ./bottom-left from ./subdir/bottom-right. As with the module loader in [Chapter 13](#chapter13.xhtml), we use absolute paths as unique identifiers. Our code is also complicated by the fact that JavaScript's Set class doesn't have an equivalent of Array.pop, so we will actually maintain the “set” of pending items as a list. The resulting code is:

![](images/comp17_14.jpg)![](images/comp17_15.jpg)![](images/comp17_16.jpg)![](images/comp17_17.jpg)

This works, but it isn't keeping track of the mapping from required names within files to absolute paths, so when one of the files in our bundle tries to access something, we might not know what it's after. The fix is to modify transitive closure to construct and return a two-level structure. The primary keys are the absolute paths to the files being required, while sub-keys are the paths they refer to when loading things ([Figure 17.4](#chapter17.xhtml_fig17_4)).

![](images/fig17_4.jpg)

[Figure 17.4:](#chapter17.xhtml_b17fig17_4) Data structure used to map names to absolute paths.

Adding this takes our transitive closure code from 23 lines to 28 lines:

![](images/comp17_18.jpg)![](images/comp17_19.jpg)![](images/comp17_20.jpg)![](images/comp17_21.jpg)

The real cost, though, is the extra complexity of the data structure: it took a couple of tries to get it right, and it will be harder for the next person to understand than the original. Comprehension and maintenance would be a little easier if we could draw diagrams directly in our source code, but as long as we insist that our programs be stored in a punchcard-compatible format (i.e., as lines of text), that will remain a dream.

## 17.3. How can we safely combine several files into one?

We now need to combine the files we have found into one while keeping each in its own namespace. We do this using the same method we used in [Chapter 13](#chapter13.xhtml): wrap the source code in an IIFE, giving that IIFE a module object to fill in and an implementation of require to resolve dependencies *within the bundle*. For example, suppose we have this file:

![](images/comp17_22.jpg)

The wrapped version will look like this:

![](images/comp17_23.jpg)

And we can test it like this:

![](images/comp17_24.jpg)![](images/comp17_25.jpg)

We need to do this for multiple files, so we will put these IIFEs in a lookup table that uses the files’ absolute paths as its keys. We will also wrap loading in a function so that we don't accidentally step on anyone else's toys:

![](images/comp17_26.jpg)

Breaking this down, the code in HEAD creates a function of no arguments while the code in TAIL returns the lookup table from that function. In between, combineFiles adds an entry to the lookup table for each file ([Figure 17.5](#chapter17.xhtml_fig17_5)).

![](images/fig17_5.jpg)

[Figure 17.5:](#chapter17.xhtml_b17fig17_5) Assembling fragments and modules to create a bundle.

We can test that this works in our two-file case:

![](images/comp17_27.jpg)![](images/comp17_28.jpg)

and then load the result and call initialize:

![](images/comp17_29.jpg)

## 17.4. How can files access each other?

The code we have built so far has not created our exports; instead, it has built a lookup table of functions that can create what we asked for. More specifically we have:

*   a lookup table from absolute filenames to functions that create module exports;

*   a lookup table from the importer's absolute filename to pairs storing the name of the required file as it was written and the required file's absolute filename; and

*   an entry point.

To turn this into what we want, we must look up the function associated with the entry point and run it, giving it an empty module object and a require function that we will describe below, then get the exports it has added to that module object. Our replacement for require is only allowed to take one argument (because that's all that JavaScript's require takes). However, it actually needs four things: the argument to the user's require call, the absolute path of the file making the call, and the two lookup tables described above. Those two tables can't be global variables because of possible name collisions: no matter what we call them, the user might have given a variable the same name.

As in [Chapter 13](#chapter13.xhtml) we solve this problem using closures. The result is probably the most difficult code in this book to understand because of its many levels of abstraction. First, we write a function that takes the two tables as arguments and returns a function that takes an absolute path identifying this module. When that function is called, it creates and returns a function that takes a local path inside a module and returns the exports. Each of these wrapping layers remembers more information for us ([Figure 17.6](#chapter17.xhtml_fig17_6)), but we won't pretend that it's easy to trace.

![](images/fig17_6.jpg)

[Figure 17.6:](#chapter17.xhtml_b17fig17_6) A function that returns functions that return functions.

We also need a third structure: a cache for the modules we've already loaded. Putting it all together we have:

![](images/comp17_30.jpg)

This code is hard to read because we have to distinguish what is being printed in the output versus what is being executed right now and because of the levels of nesting needed to capture variables safely. Getting this right took much more time per line of finished code than anything we have seen so far except the promises in [Chapter 3](#chapter3.xhtml). However, it is all intrinsic complexity: anything that does what require does is going to be equally convoluted.

To prove that our code works, we will look up the function main in the first file and call it. (If we were loading in the browser, we'd capture the exports in a variable for later use.) First, we create the bundled file:

![](images/comp17_31.jpg)![](images/comp17_32.jpg)

and then we run it:

![](images/comp17_33.jpg)

That was a lot of work to print one line, but what we have should work for other files. The two-file case with main and other works:

![](images/comp17_34.jpg)![](images/comp17_35.jpg)

and so does our most complicated test with main and four other files:

![](images/comp17_36.jpg)

## 17.5. Exercises

### Using test-driven development

Suppose we wanted to compress the files being stored by the file backup system in [Chapter 5](#chapter5.xhtml) instead of copying them as-is. What tests would you write before adding this feature in order to ensure that it worked correctly once it was implemented?

### Finding import dependencies

Modify the dependency finder to work with import statements instead of require calls.

### Track files using hashes

Modify the dependency finder to track files by hashing them instead of relying on paths, so that if exactly the same file is being required from two locations, only one copy is loaded.

### Using asynchronous file operations

Modify the dependency finder to use async and await instead of synchronous file operations.

### Unit testing transitive closure

Write unit tests for the tool that finds the transitive closure of files’ requirements using Mocha and mock-fs. (Rather than parsing JavaScript files in the mock filesystem, have each file contain only a list of the names of the files it depends on.)

### Exporting multiple functions

Create test cases for the module bundler in which files export more than one function and fix any bugs in the module bundler that they uncover.

### Checking integrity

Write a function that checks the integrity of the data structure returned by the transitive closure routine, i.e., that makes sure every cross-reference resolves correctly.

### Logging module loading

1.  Write a function called logLoad that takes a module name as an argument and prints a message using console.error saying that the module has been loaded.

2.  Modify the bundle generator to insert calls to this function to report when modules are actually loaded.

### Tracing execution

Trace the execution of every function called when the main function in the full bundle is called.

### Making bundles more readable

Modify the bundle creator to make its output more readable, e.g., by adding comments and indentation. (This does not matter to the computer, but can help debugging.)

# 18Package Manager

Terms defined: **[backward-compatible](#appendix5.xhtml_d22)**, **[combinatorial explosion](#appendix5.xhtml_d56)**, **[heuristic](#appendix5.xhtml_d136)**, **[manifest](#appendix5.xhtml_d181)**, **[patch](#appendix5.xhtml_d208)**, **[prune](#appendix5.xhtml_d223)**, **[SAT solver](#appendix5.xhtml_d241)**, **[scoring function](#appendix5.xhtml_d245)**, **[seed](#appendix5.xhtml_d247)**, **[semantic versioning](#appendix5.xhtml_d248)**

There is no point building software if you can't install it. Inspired by the Comprehensive TeX Archive Network CTAN[¹](#chapter18.xhtml_fn18_1), most languages now have an online archive from which developers can download packages. Each package typically has a name and one or more version(s); each version may have a list of dependencies, and the package may specify a version or range of versions for each dependency.

Downloading files requires some web programming that is out of scope for this book, while installing those files in the right places uses the systems programming skills of [Chapter 2](#chapter2.xhtml). The piece we are missing is a way to figure out exactly what versions of different packages to install in order to create a consistent setup. If packages A and B require different versions of C, it might not be possible to use A and B together. On the other hand, if each one requires a range of versions of C and those ranges overlap, we might be able to find a combination that works—at least, until we try to install packages D and E.

We *could* install every package's dependencies separately with it; the disk space wouldn't be much of an obstacle, but loading dozens of copies of the same package into the browser would slow applications down. This chapter therefore explores how to find a workable installation or prove that there isn't one. It is based in part on this tutorial[²](#chapter18.xhtml_fn18_2) by Maël Nison[³](#chapter18.xhtml_fn18_3).

## 18.1. What is semantic versioning?

Most software projects use **semantic versioning** for software releases. Each version number consists of three integers X.Y.Z, where X is the major version, Y is the minor version, and Z is the **patch** number. (The full specification[⁴](#chapter18.xhtml_fn18_4) allows for more fields, but we will ignore them in this tutorial.)

A package's authors increment its major version number every time something changes in a way that makes the package incompatible with previous versions. For example, if they add a required parameter to a function, then code built for the old version will fail or behave unpredictably with the new one. The minor version number is incremented when new functionality is **backward-compatible**—i.e., it won't break any existing code—and the patch number is changed for backward-compatible bug fixes that don't add any new features.

The notation for specifying a project's dependencies looks a lot like arithmetic: > = 1.2.3 means “any version from 1.2.3 onward”, < 4 means “any version before 4.anything”, and 1.0 - 3.1 means “any version in the specified range (including patches)”. Note that version 2.1 is greater than version 1.99: no matter how large a minor version number becomes, it never spills over into the major version number in the way that minutes add up to hours or months add up to years.

It isn't hard to write a few simple comparisons for semantic version identifiers, but getting all the different cases right is almost as tricky as handling dates and times correctly, so we will rely on the semver[⁵](#chapter18.xhtml_fn18_5) module. semver.valid(’1.2.3’) checks that 1.2.3 is a valid version identifier, while semver.satisfies(’2.2’, ’1.0 - 3.1’) checks that its first argument is compatible with the range specified in its second.

## 18.2. How can we find a consistent set of packages?

Imagine that each package we need is represented as an axis on a multi-dimensional grid, with its versions as the tick marks ([Figure 18.1](#chapter18.xhtml_fig18_1)). Each point on the grid is a possible combination of package versions. We can block out regions of this grid using the constraints on the package versions; whatever points are left when we're done represent legal combinations.

![](images/fig18_1.jpg)

[Figure 18.1:](#chapter18.xhtml_b18fig18_1) Finding allowable combinations of package versions.

For example, suppose we have the set of requirements shown in [Table 18.1](#chapter18.xhtml_tbl18_1). There are 18 possible configurations (2 for X × 3 for Y × 3 for Z) but 16 are excluded by various incompatibilities. Of the two remaining possibilities, X/2 + Y/3 + Z/3 is strictly greater than X/2 + Y/2 + Z/2, so we would probably choose the former ([Table 18.2](#chapter18.xhtml_tbl18_2)). If we wound up with A/1 + B/2 versus A/2 + B/1, we would need to add rules for resolving ties.

[Table 18.1:](#chapter18.xhtml_b18tbl18_1) Example package dependencies.

| **[Package](#appendix5.xhtml_d201)** | **Requires** |
| X/1 | Y/1-2 |
| X/1 | Z/1 |
| X/2 | Y/2-3 |
| X/2 | Z/1-2 |
| Y/1 | Z/2 |
| Y/2 | Z/2-3 |
| Y/3 | Z/3 |
| Z/1 |  |
| Z/2 |  |
| Z/3 |  |

[Table 18.2:](#chapter18.xhtml_b18tbl18_2) Result for example package dependencies.

| **X** | **Y** | **Z** | **Excluded** |
| 1 | 1 | 1 | Y/1 - Z/1 |
| 1 | 1 | 2 | X/1 - Z/2 |
| 1 | 1 | 3 | X/1 - Z/3 |
| 1 | 2 | 1 | Y/2 - Z/1 |
| 1 | 2 | 2 | X/1 - Z/2 |
| 1 | 2 | 3 | X/1 - Z/3 |
| 1 | 3 | 1 | X/1 - Y/3 |
| 1 | 3 | 2 | X/1 - Y/3 |
| 1 | 3 | 3 | X/1 - Y/3 |
| 2 | 1 | 1 | X/2 - Y/1 |
| 2 | 1 | 2 | X/2 - Y/1 |
| 2 | 1 | 3 | X/2 - Y/1 |
| 2 | 2 | 1 | Y/2 - Z/1 |
| 2 | 2 | 2 |  |
| 2 | 2 | 3 | X/2 - Z/3 |
| 2 | 3 | 1 | Y/3 - Z/1 |
| 2 | 3 | 2 | Y/3 - Z/2 |
| 2 | 3 | 3 | X/2 - Z/3 |

To construct [Table 18.1](#chapter18.xhtml_tbl18_1) we find the transitive closure of all packages plus all of their dependencies. We then pick two packages and create a list of their valid pairs. Choosing a third package, we cross off pairs that can't be satisfied to leave triples of legal combinations. We repeat this until all packages are included in our table.

In the worst case this procedure will create a **combinatorial explosion** of possibilities. Smart algorithms will try to add packages to the mix in an order that minimizes the number of new possibilities at each stage, or create pairs and then combine them to create pairs of pairs and so on. Our algorithm will be simpler (and therefore slower), but illustrates the key idea.

## 18.3. How can we satisfy constraints?

To avoid messing around with parsers, our programs reads a JSON data structure describing the problem; a real package manager would read the **manifests** of the packages in question and construct a similar data structure. We will stick to single-digit version numbers for readability, and will use this as our first test case:

![](images/comp18_1.jpg)

To check if a combination of specific versions of packages is compatible with a manifest, we add each package to our active list in turn and look for violations. If there aren't any more packages to add and we haven't found a violation, then what we have must be a legal configuration.

![](images/comp18_2.jpg)

The simplest way to find configurations is to sweep over all possibilities. For debugging purposes, our function prints possibilities as it goes:

![](images/comp18_3.jpg)

If we run this program on the two-package example shown earlier, we get this output:

![](images/comp18_4.jpg)![](images/comp18_5.jpg)

When we run it on our triple-package example, we get this:

![](images/comp18_6.jpg)![](images/comp18_7.jpg)

This works, but it is doing a lot of unnecessary work. If we sort the output by the case that caught the exclusion, it turns out that 9 of the 17 exclusions are redundant rediscovery of a previously known problem ([Table 18.3](#chapter18.xhtml_tbl18_3)).

[Table 18.3:](#chapter18.xhtml_b18tbl18_3) Package exclusions.

| **Excluded** | **X** | **Y** | **Z** |
| X/1 - Y/3 | 1 | 3 | 1 |
| … | 1 | 3 | 2 |
| … | 1 | 3 | 3 |
| X/1 - Z/2 | 1 | 1 | 2 |
| … | 1 | 2 | 2 |
| X/1 - Z/3 | 1 | 1 | 3 |
| … | 1 | 2 | 3 |
| X/2 - Y/1 | 2 | 1 | 1 |
| … | 2 | 1 | 2 |
| … | 2 | 1 | 3 |
| X/2 - Z/3 | 2 | 2 | 3 |
| … | 2 | 3 | 3 |
| Y/1 - Z/1 | 1 | 1 | 1 |
| Y/2 - Z/1 | 1 | 2 | 1 |
| … | 2 | 2 | 1 |
| Y/3 - Z/1 | 2 | 3 | 1 |
| … | 2 | 3 | 2 |
|  | 2 | 2 | 2 |

## 18.4. How can we do less work?

We can make this more efficient by **pruning** the search tree as we go along ([Figure 18.2](#chapter18.xhtml_fig18_2)). After all, if we know that X and Y are incompatible, there is no need to check Z as well.

![](images/fig18_2.jpg)

[Figure 18.2:](#chapter18.xhtml_b18fig18_2) Pruning options in the search tree to reduce work.

This version of the program collects possible solutions and displays them at the end. It only keeps checking a partial solution if what it has found so far looks good:

![](images/comp18_8.jpg)

The compatible function checks to see if adding something will leave us with a consistent configuration:

![](images/comp18_9.jpg)

Checking as we go gets us from 18 complete solutions to 11\. One is workable and two are incomplete—they represent 6 possible complete solutions that we didn't need to finish:

![](images/comp18_10.jpg)

Another way to look at the work is the number of steps in the search. The full search had 18×3 = 54 steps. Pruning leaves us with (12×3) + (2×2) = 40 steps so we have eliminated roughly 1/4 of the work.

What if we searched in the reverse order?

![](images/comp18_11.jpg)![](images/comp18_12.jpg)

Now we have (8×3) + (5×2) = 34 steps, i.e., we have eliminated roughly 1/3 of the work. That may not seem like a big difference, but if we go five levels deep at the same rate, it cuts the work in half. There are lots of **heuristics** for searching trees; none are guaranteed to give better performance in every case, but most give better performance in most cases.

## 18.5. Exercises

### Comparing semantic versions

Write a function that takes an array of semantic version specifiers and sorts them in ascending order. Remember that 2.1 is greater than 1.99.

### Parsing semantic versions

Using the techniques of [Chapter 8](#chapter8.xhtml), write a parser for a subset of the semantic versioning specification[⁶](#chapter18.xhtml_fn18_6).

### Using scoring functions

Many different combinations of package versions can be mutually compatible. One way to decide which actual combination to install is to create a **scoring function** that measures how good or bad a particular combination is. For example, a function could measure the “distance” between two versions as:

![](images/comp18_13.jpg)

1.  Implement a working version of this function and use it to measure the total distance between the set of packages found by the solver and the set containing the most recent version of each package.

2.  Explain why this doesn't actually solve the original problem.

### Using full semantic versions

Modify the constraint solver to use full semantic versions instead of single digits.

### Regular releases

Some packages release new versions on a regular cycle, e.g., Version 2021.1 is released on March 1 of 2021, Version 2021.2 is released on September 1 of that year, version 2022.1 is released on March 1 of the following year, and so on.

1.  How does this make package management easier?

2.  How does it make it more difficult?

### Writing unit tests

Write unit tests for the constraint solver using Mocha.

### Generating test fixtures

Write a function that creates fixtures for testing the constraint solver:

1.  Its first argument is an object whose keys are (fake) package names and whose values are integers indicating the number of versions of that package to include in the test set, such as {’left’: 3, ’middle’: 2, ’right’: 15}. Its second argument is a **seed** for random number generation.

2.  It generates one valid configuration, such as {’left’: 2, ’middle’: 2, ’right’: 9}. (This is to ensure that there is at least one installable set of packages.)

3.  It then generates random constraints between the packages. (These may or may not result in other installable combinations.) When this is done, it adds constraints so that the valid configuration from the previous step is included.

### Searching least first

Rewrite the constraint solver so that it searches packages by looking at those with the fewest available versions first. Does this reduce the amount of work done for the small examples in this chapter? Does it reduce the amount of work done for larger examples?

### Using generators

Rewrite the constraint solver to use generators.

### Using exclusions

1.  Modify the constraint solver so that it uses a list of package exclusions instead of a list of package requirements, i.e., its input tells it that version 1.2 of package Red can *not* work with versions 3.1 and 3.2 of package Green (which implies that Red 1.2 can work with any other versions of Green).

2.  Explain why package managers aren't built this way.

# 19Virtual Machine

Terms defined: **[Application Binary Interface](#appendix5.xhtml_d11)**, **[assembler](#appendix5.xhtml_d15)**, **[assembly code](#appendix5.xhtml_d16)**, **[bitwise operation](#appendix5.xhtml_d27)**, **[disassembler](#appendix5.xhtml_d89)**, **[instruction pointer](#appendix5.xhtml_d149)**, **[instruction set](#appendix5.xhtml_d150)**, **[label (address in memory)](#appendix5.xhtml_d160)**, **[op code](#appendix5.xhtml_d198)**, **register**, **[virtual machine](#appendix5.xhtml_d299)**, **[word (of memory)](#appendix5.xhtml_d304)**

Computers don't execute JavaScript directly. Instead, each processor has its own **instruction set**, and a compiler translates high-level languages into those instructions. Compilers often use an intermediate representation called **assembly code** that gives instructions names instead of numbers. To understand more about how JavaScript actually runs, we will simulate a very simple processor with a little bit of memory. If you want to dive deeper, have a look at Bob Nystrom's[¹](#chapter19.xhtml_fn19_1) *Crafting Interpreters[²](#chapter19.xhtml_fn19_2)*. You may also enjoy Human Resource Machine[³](#chapter19.xhtml_fn19_3)[, which asks you to solve puzzles of increasing difficulty using a processor almost as simple as ours.

## 19.1. What is the architecture of our virtual machine?

Our **virtual machine** has three parts, which are shown in [Figure 19.1](#chapter19.xhtml_fig19_1) for a program made up of 110 instructions:

1.  An **instruction pointer** (IP) that holds the memory address of the next instruction to execute. It is automatically initialized to point at address 0, which is where every program must start. This rule is part of the **Application Binary Interface** (ABI) for our virtual machine.

2.  Four **registers** named R0 to R3 that instructions can access directly. There are no memory-to-memory operations in our VM: everything happens in or through registers.

3.  256 **words** of memory, each of which can store a single value. Both the program and its data live in this single block of memory; we chose the size 256 so that each address will fit in a single byte.

![](images/fig19_1.jpg)

[Figure 19.1:](#chapter19.xhtml_b19fig19_1) Architecture of the virtual machine.

The instructions for our VM are 3 bytes long. The **op code** fits into one byte, and each instruction may optionally include one or two single-byte operands. Each operand is a register identifier, a constant, or an address (which is just a constant that identifies a location in memory); since constants have to fit in one byte, the largest number we can represent directly is 256\. [Table 19.1](#chapter19.xhtml_tbl19_1) uses the letters r, c, and a to indicate instruction format, where r indicates a register identifier, c indicates a constant, and a indicates an address.

[Table 19.1:](#chapter19.xhtml_b19tbl19_1) Virtual machine op codes.

| **Instruction** | **Code** | **Format** | **Action** | **Example** | **Equivalent** |
| hlt | 1 | -- | Halt program | hlt | process.exit(0) |
| ldc | 2 | rc | Load immediate | ldc R0 123 | R0: = 123 |
| ldr | 3 | rr | Load register | ldr R0 R1 | R0: = RAM[R1] |
| cpy | 4 | rr | Copy register | cpy R0 R1 | R0: = R1 |
| str | 5 | rr | Store register | str R0 R1 | RAM[R1]: = R0 |
| add | 6 | rr | Add | add R0 R1 | R0: = R0 + R1 |
| sub | 7 | rr | Subtract | sub R0 R1 | R0: = R0 - R1 |
| beq | 8 | ra | Branch if equal | beq R0 123 | if (R0 === 0) PC: = 123 |
| bne | 9 | ra | Branch if not equal | bne R0 123 | if (R0 !== 0) PC: = 123 |
| prr | 10 | r- | Print register | prr R0 | console.log(R0) |
| prm | 11 | r- | Print memory | prm R0 | console.log(RAM[R0]) |

We put our VM's architectural details in a file that can be shared by other components:

![](images/comp19_1.jpg)

While there isn't a name for this design pattern, putting all the constants that define a system in one file instead of scattering them across multiple files makes them easier to find as well as ensuring consistency.

## 19.2. How can we execute these instructions?

As in previous chapters, we will split a class that would normally be written in one piece into several parts for exposition. We start by defining a class with an instruction pointer, some registers, and some memory along with a prompt for output:

![](images/comp19_2.jpg)

A program is just an array of numbers representing instructions. To load one, we copy those numbers into memory and reset the instruction pointer and registers:

![](images/comp19_3.jpg)

In order to handle the next instruction, the VM gets the value in memory that the instruction pointer currently refers to and moves the instruction pointer on by one address. It then uses **bitwise operations** to extract the op code and operands from the instruction ([Figure 19.2](#chapter19.xhtml_fig19_2)):

![](images/comp19_4.jpg)![](images/fig19_2.jpg)

[Figure 19.2:](#chapter19.xhtml_b19fig19_2) Using bitwise operations to unpack instructions.

The next step is to extend our base class with one that has a run method. As its name suggests, this runs the program by fetching instructions and executing them until told to stop:

![](images/comp19_5.jpg)

Some instructions are very similar to others, so we will only look at three here. The first stores the value of one register in the address held by another register:

![](images/comp19_6.jpg)

The first three lines check that the operation is legal; the fourth one uses the value in one register as an address, which is why it has nested array indexing.

Adding the value in one register to the value in another register is simpler:

![](images/comp19_7.jpg)

as is jumping to a fixed address if the value in a register is zero:

![](images/comp19_8.jpg)

## 19.3. What do assembly programs look like?

We could figure out numerical op codes by hand, and in fact that's what the first programmers[⁴](#chapter19.xhtml_fn19_4) did. However, it is much easier to use an **assembler**, which is just a small compiler for a language that very closely represents actual machine instructions.

Each command in our assembly languages matches an instruction in the VM. Here's an assembly language program to print the value stored in R1 and then halt:

![](images/comp19_9.jpg)

Its numeric representation is:

![](images/comp19_10.jpg)

One thing the assembly language has that the instruction set doesn't is **labels on addresses**. The label loop doesn't take up any space; instead, it tells the assembler to give the address of the next instruction a name so that we can refer to that address as @loop in jump instructions. For example, this program prints the numbers from 0 to 2 ([Figure 19.3](#chapter19.xhtml_fig19_3)):

![](images/comp19_11.jpg)![](images/comp19_12.jpg)![](images/fig19_3.jpg)

[Figure 19.3:](#chapter19.xhtml_b19fig19_3) Flowchart of assembly language program to count up from 0 to 2.

Let's trace this program's execution ([Figure 19.4](#chapter19.xhtml_fig19_4)):

1.  R0 holds the current loop index.

2.  R1 holds the loop's upper bound (in this case 3).

3.  The loop prints the value of R0 (one instruction).

4.  The program adds 1 to R0\. This takes two instructions because we can only add register-to-register.

5.  It checks to see if we should loop again, which takes three instructions.

6.  If the program *doesn't* jump back, it halts.

![](images/fig19_4.jpg)

[Figure 19.4:](#chapter19.xhtml_b19fig19_4) Tracing registers and memory values for a simple counting program.

The implementation of the assembler mirrors the simplicity of assembly language. The main method gets interesting lines, finds the addresses of labels, and turns each remaining line into an instruction:

![](images/comp19_13.jpg)

To find labels, we go through the lines one by one and either save the label *or* increment the current address (because labels don't take up space):

![](images/comp19_14.jpg)

To compile a single instruction we break the line into tokens, look up the format for the operands, and pack them into a single value:

![](images/comp19_15.jpg)

Combining op codes and operands into a single value is the reverse of the unpacking done by the virtual machine:

![](images/comp19_16.jpg)

Finally, we need few utility functions:

![](images/comp19_17.jpg)

Let's try assembling a program and display its output, the registers, and the interesting contents of memory. As a test, this program counts up to three:

![](images/comp19_18.jpg)![](images/comp19_19.jpg)

## 19.4. How can we store data?

It is tedious to write interesting programs when each value needs a unique name. We can do a lot more once we have collections like arrays, so let's add those to our assembler. We don't have to make any changes to the virtual machine, which doesn't care if we think of a bunch of numbers as individuals or elements of an array, but we do need a way to create arrays and refer to them.

We will allocate storage for arrays at the end of the program by using .data on a line of its own to mark the start of the data section and then label: number to give a region a name and allocate some storage space ([Figure 19.5](#chapter19.xhtml_fig19_5)).

![](images/fig19_5.jpg)

[Figure 19.5:](#chapter19.xhtml_b19fig19_5) Allocating storage for arrays in the virtual machine.

This enhancement only requires a few changes to the assembler. First, we need to split the lines into instructions and data allocations:

![](images/comp19_20.jpg)![](images/comp19_21.jpg)

Second, we need to figure out where each allocation lies and create a label accordingly:

![](images/comp19_22.jpg)

And that's it: no other changes are needed to either compilation or execution. To test it, let's fill an array with the numbers from 0 to 3:

![](images/comp19_23.jpg)![](images/comp19_24.jpg)

## 19.5. Exercises

### Swapping values

Write an assembly language program that swaps the values in R1 and R2 without affecting the values in other registers.

### Reversing an array

Write an assembly language program that starts with:

*   the base address of an array in one word

*   the length of the array N in the next word

*   N values immediately thereafter

and reverses the array in place.

### Increment and decrement

1.  Add instructions inc and dec that add one to the value of a register and subtract one from the value of a register respectively.

2.  Rewrite the examples to use these instructions. How much shorter do they make the programs? How much easier to read?

### Using long addresses

1.  Modify the virtual machine so that the ldr and str instructions contain 16-bit addresses rather than 8-bit addresses and increase the virtual machine's memory to 64K words to match.

2.  How does this complicate instruction interpretation?

### Operating on strings

The C programming language stored character strings as non-zero bytes terminated by a byte containing zero.

1.  Write a program that starts with the base address of a string in R1 and finishes with the length of the string (not including the terminator) in the same register.

2.  Write a program that starts with the base address of a string in R1 and the base address of some other block of memory in R2 and copies the string to that new location (including the terminator).

3.  What happens in each case if the terminator is missing?

### Call and return

1.  Add another register to the virtual machine called SP (“stack pointer”) that is automatically initialized to the *last* address in memory.

2.  Add an instruction psh (short for “push”) that copies a value from a register to the address stored in SP and then subtracts one from SP.

3.  Add an instruction pop (short for “pop”) that adds one to SP and then copies a value from that address into a register.

4.  Using these instructions, write a subroutine that evaluates 2x+1 for every value in an array.

### Disassembling instructions

A **disassembler** turns machine instructions into assembly code. Write a disassembler for the instruction set used by our virtual machine. (Since the labels for addresses are not stored in machine instructions, disassemblers typically generate labels like @L001 and @L002.)

### Linking multiple files

1.  Modify the assembler to handle .include filename directives.

2.  What does your modified assembler do about duplicate label names? How does it prevent infinite includes (i.e., A.as includes B.as which includes A.as again)?

### Providing system calls

Modify the virtual machine so that developers can add “system calls” to it.

1.  On startup, the virtual machine loads an array of functions defined in a file called syscalls.js.

2.  The sys instruction takes a one-byte constant argument. It looks up the corresponding function and calls it with the values of R0-R3 as parameters and places the result in R0.

### Unit testing

1.  Write unit tests for the assembler.

2.  Once they are working, write unit tests for the virtual machine.

# 20Debugger

Terms defined: **[breakpoint](#appendix5.xhtml_d31)**, **[source map](#appendix5.xhtml_d259)**, **[tab completion](#appendix5.xhtml_d273)**, **[watchpoint](#appendix5.xhtml_d302)**

We have finally come to another of the topics that sparked this book: how does a debugger work? Debuggers are as much a part of programmers’ lives as version control but are taught far less often (in part, we believe, because it's harder to create homework questions for them). In this chapter we will build a simple single-stepping debugger and show one way to test interactive applications ([Chapter 4](#chapter4.xhtml)).

## 20.1. What is our starting point?

We would like to debug a higher-level language than the assembly code of [Chapter 19](#chapter19.xhtml), but we don't want to have to write a parser or wrestle with the ASTs of [Chapter 14](#chapter14.xhtml). As a compromise, we will represent programs as JSON data structures whose elements have the form [command...args]. If the JavaScript version of our program is:

![](images/comp20_1.jpg)

then the JSON representation is:

![](images/comp20_2.jpg)

Our virtual machine is structured like the one in [Chapter 19](#chapter19.xhtml). A real system would parse a program to create JSON, then translate JSON into assembly code, then assemble that to create machine instructions. Again, to keep things simple we will execute a program by removing comments and blank lines and then running commands by looking up the command name's and calling that method:

![](images/comp20_3.jpg)

Remember, functions and methods are just another kind of data, so if an object has a method called "meth", the expression this["meth"] looks it up and this["meth"](args) calls it. If "meth" is stored in a variable called name, then this[name](args) will do exactly the same thing.

The method in our VM that defines a new variable with an initial value looks like this:

![](images/comp20_4.jpg)

while the one that adds two values looks like this:

![](images/comp20_5.jpg)

Running a while loop is:

![](images/comp20_6.jpg)

and checking that a variable name refers to an array is:

![](images/comp20_7.jpg)

The other operations are similar to these.

## 20.2. How can we make a tracing debugger?

The next thing we need in our debugger is a **source map** that keeps track of where in the source file each instruction came from. Since JSON is a subset of JavaScript, we could get line numbers by parsing our programs with Acorn[¹](#chapter20.xhtml_fn20_1). However, we would then have to scrape the information we want for this example out of the AST. Since this chapter is supposed to be about debugging, not parsing, we will instead cheat and add a line number to each interesting statement by hand so that our program looks like this:

![](images/comp20_8.jpg)

Building the source map from that is simple; for now, we just modify exec to ignore the line number:

![](images/comp20_9.jpg)

The next step is to modify the VM's exec method so that it executes a callback function for each significant operation (where “significant” means “we bothered to record its line number”). Since we're not sure what our debugger is going to need, we give this callback the environment holding the current set of variables, the line number, and the operation being performed:

![](images/comp20_10.jpg)

We also modify the VM's constructor to record the debugger and give it a reference to the virtual machine ([Figure 20.1](#chapter20.xhtml_fig20_1)). We have to connect the two objects explicitly because each one needs a reference to the other, but one of them has to be created first. “A gets B then B tells A about itself” is a common pattern; we will look at other ways to manage it in the exercises.

![](images/fig20_1.jpg)

[Figure 20.1:](#chapter20.xhtml_b20fig20_1) Two-step initialization of mutually-dependent objects.

To run the program, we create a debugger object and pass it to the VM's constructor:

![](images/comp20_11.jpg)

A simple debugger just traces interesting statements as they run:

![](images/comp20_12.jpg)

Let's try it on a program that adds the numbers in an array:

![](images/comp20_13.jpg)![](images/comp20_14.jpg)

## 20.3. How can we make the debugger interactive?

What we have built so far is an always-on print statement. To turn it into an interactive debugger, we will use the prompt-sync[²](#chapter20.xhtml_fn20_2) module to manage user input with the following set of commands:

*   ? or help to list commands.

*   clear # to clear a **breakpoint** at a numbered line.

*   list to list lines and breakpoints.

*   next to go forward one line.

*   print name to show a variable while at a breakpoint.

*   run to run to the next breakpoint.

*   stop # to break at a numbered line.

*   variables to list all variable names.

*   exit to exit immediately.

When the virtual machine calls the debugger, the debugger first checks if it is on a numbered line. If it isn't, it hands control back to the VM. Otherwise, if we are single-stepping or this line is a breakpoint, the debugger takes over. Its overall structure is:

![](images/comp20_15.jpg)

It interacts with users by lookup up a command and invoking the corresponding method, just as the VM does:

![](images/comp20_16.jpg)

With this structure in place, the command handlers are pretty straightforward. For example, this method moves us to the next line:

![](images/comp20_17.jpg)

while this one prints the value of a variable:

![](images/comp20_18.jpg)

After using this for a few moments, though we realized that we needed to change the signature of the loop method. We want to stop the loop each time it runs, and need to know where we are. We didn't allow for this in the base class, and we don't want to have to change every method, so we take advantage of the fact that JavaScript ignores any extra arguments passed to a method:

![](images/comp20_19.jpg)

This is sloppy, but it works; we will tidy it up in the exercises.

## 20.4. How can we test an interactive application?

How can we test an interactive application like a debugger? The answer is, “By making it non-interactive.” Like many tools over the past 30 years, our approach is based on a program called Expect[³](#chapter20.xhtml_fn20_3). Our library replaces the input and output functions of the application being tested with callbacks, then provides input when asked and checks output when it is given ([Figure 20.2](#chapter20.xhtml_fig20_2)).

![](images/fig20_2.jpg)

[Figure 20.2:](#chapter20.xhtml_b20fig20_2) Replacing input and output to test interactive applications.

The results look like this:

![](images/comp20_20.jpg)

Our Expect class may be short, but it is hard to understand because it is so abstract:

![](images/comp20_21.jpg)

Piece-by-piece:

*   subject is the thing being tested.

*   start is a callback to start the system running. It gives control to the subject, which then calls back into the test framework for input and output.

*   get and send store things to be given to the subject and to be checked against its output. Both methods return this so that we can chain calls together.

*   run starts the system and checks that all expected interactions have been used up when testing is done.

*   toSystem and fromSystem use next to get the next test record, check its type, and return the string.

Let's modify the debugger to use the tester, keeping in mind that the prompt counts as an output (and yes, we forgot this in the first version):

![](images/comp20_22.jpg)

Again, we can't pass the tester as a constructor parameter because of initialization order, so we write a setup function to make sure everything is connected the right way:

![](images/comp20_23.jpg)

Let's try running our tests:

![](images/comp20_24.jpg)![](images/comp20_25.jpg)

That works—or does it? Why is only one test shown, and doesn't the summary appear? After a bit of digging, we realize that the debugger's exit command calls process.exit when the simulated program ends, so the whole program including the VM, debugger, and test framework stops immediately *before* the promises that contain the tests have run.

We could fix this by modifying the debugger callback to return an indication of whether or not execution should continue, then modify the VM to pay attention to that flag. However, this approach becomes very complicated when we have deeply-nested calls to exec, which will happen with loops and conditionals.

A better alternative is to use an exception for control flow. We can define our own kind of exception as an empty class: it doesn't need any data because we are only using it to get a typed object:

![](images/comp20_26.jpg)

Next, we modify the debugger to throw this exception when asked to exit:

![](images/comp20_27.jpg)

And finally we modify the VM to finish cleanly if this exception is thrown, but re-throw any other kind of exception:

![](images/comp20_28.jpg)

With these changes in place, we are finally able to test our interactive debugger:

![](images/comp20_29.jpg)![](images/comp20_30.jpg)

## 20.5. Exercises

### Implementing tab completion

Read the documentation for prompt-sync and then implement **tab completion** for the debugger.

### Modifying variables while running

Add a set command that sets the value of a variable to a new value in a running program. How do you handle setting array elements?

### Making output more readable

Modify the tracing debugger so that the statements inside loops and conditionals are indented for easier reading.

### Better loops

Our solution for handling loops is sloppy; fix it.

### Using a flag to continue execution

Modify the debugger and virtual machine to use a “continue executing” flag rather than throwing an exception when execution should end. Which approach is easier to understand? Which will be easier to extend in the future?

### Numbering lines

Write a tool that takes a JSON program representation *without* statement numbers and produces one that numbers all of the interesting statements for debugging purposes. Use whatever definition of “interesting” you think would be most useful.

### Looping around again

Implement a “next loop iteration” command that runs the program until it reaches the current point in the next iteration of the current loop.

### Looking up objects

Rather than having some objects call setXYZ methods in other objects, it is common practice to use a lookup table for mutual dependencies:

1.  Every object initializes calls table.set(name, this) in its constructor.

2.  Whenever object A needs the instance of object B, it calls table.lookup(’B’). It does *not* store the result in a member variable.

Modify the virtual machine and debugger to use this pattern.

### Watching for variable changes

Modify the debugger and virtual machine to implement **watchpoints** that halt the program whenever the value of a variable changes.

### Translating JSON to assembler

Write a tool that translates the JSON program representation into the assembly code of [Chapter 19](#chapter19.xhtml). To simplify things, increase the number of registers so that there is always storage for intermediate results when doing arithmetic.

# 21Conclusion

We have come a long way since we listed the contents of a directory in [Chapter 2](#chapter2.xhtml). Saving files in version control, making sure code meets style rules, debugging it and bundling it (hopefully in that order)—programmers do these things every day, and we hope that understanding how they work will help you do them better.

We also hope that your journey won't stop here. If you would like to add a chapter to this book or translate it into another programming language, human language, or both, your help would be very welcome: please see the introduction in [Chapter 1](#chapter1.xhtml) and the contributors’ guide in [Appendix C](#appendix3.xhtml_appendix3) for more information.

> We shape our tools, and thereafter our tools shape us.
> 
> — Marshall McLuhan

# ALicense

All of the written material is made available under the Creative Commons - Attribution - NonCommercial 4.0 International license (CC-BY-NC-4.0), while the software is made available under the Hippocratic License.

## Writing

*This is a human-readable summary of (and not a substitute for) the license. For the full legal text of this license, please see [https://creativecommons.org/licenses/by-nc/4.0/legalcode](https://creativecommons.org)[¹](#appendix1.xhtml_fnapp1_1).*

All of this site is made available under the terms of the Creative Commons Attribution - NonCommercial 4.0 license. You are free to:

*   **Share** — copy and redistribute the material in any medium or format

*   **Adapt** — remix, transform, and build upon the material

The licensor cannot revoke these freedoms as long as you follow the license terms. **Under the following terms:**

*   **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

*   **NonCommercial** — You may not use the material for commercial purposes.

*   **No additional restrictions** — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

**Notices:**

You do not have to comply with the license for elements of the material in the public domain or where your use is permitted by an applicable exception or limitation.

No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.

## Software

Licensor hereby grants permission by this license (“License”), free of charge, to any person or entity (the “Licensee”) obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

*   The above copyright notice and this License or a subsequent version published on the Hippocratic License Website[²](#appendix1.xhtml_fnapp1_2) shall be included in all copies or substantial portions of the Software. Licensee has the option of following the terms and conditions either of the above numbered version of this License or of any subsequent version published on the Hippocratic License Website.

*   Compliance with Human Rights Laws and Human Rights Principles:

    1.  Human Rights Laws. The Software shall not be used by any person or entity for any systems, activities, or other uses that violate any applicable laws, regulations, or rules that protect human, civil, labor, privacy, political, environmental, security, economic, due process, or similar rights (the “Human Rights Laws”). Where the Human Rights Laws of more than one jurisdiction are applicable to the use of the Software, the Human Rights Laws that are most protective of the individuals or groups harmed shall apply.

    2.  Human Rights Principles. Licensee is advised to consult the articles of the United Nations Universal Declaration of Human Rights[³](#appendix1.xhtml_fnapp1_3) and the United Nations Global Compact[⁴](#appendix1.xhtml_fnapp1_4) that define recognized principles of international human rights (the “Human Rights Principles”). It is Licensor's express intent that all use of the Software be consistent with Human Rights Principles. If Licensor receives notification or otherwise learns of an alleged violation of any Human Rights Principles relating to Licensee's use of the Software, Licensor may in its discretion and without obligation (i) (a) notify Licensee of such allegation and (b) allow Licensee 90 days from notification under (i)(a) to investigate and respond to Licensor regarding the allegation and (ii) (a) after the earlier of 90 days from notification under (i)(a), or Licensee's response under (i)(b), notify Licensee of License termination and (b) allow Licensee an additional 90 days from notification under (ii)(a) to cease use of the Software.

    3.  Indemnity. Licensee shall hold harmless and indemnify Licensor against all losses, damages, liabilities, deficiencies, claims, actions, judgments, settlements, interest, awards, penalties, fines, costs, or expenses of whatever kind, including Licensor's reasonable attorneys’ fees, arising out of or relating to Licensee's non-compliance with this License or use of the Software in violation of Human Rights Laws or Human Rights Principles.

*   Enforceability: If any portion or provision of this License is determined to be invalid, illegal, or unenforceable by a court of competent jurisdiction, then such invalidity, illegality, or unenforceability shall not affect any other term or provision of this License or invalidate or render unenforceable such term or provision in any other jurisdiction. Upon a determination that any term or provision is invalid, illegal, or unenforceable, to the extent permitted by applicable law, the court may modify this License to affect the original intent of the parties as closely as possible. The section headings are for convenience only and are not intended to affect the construction or interpretation of this License. Any rule of construction to the effect that ambiguities are to be resolved against the drafting party shall not apply in interpreting this License. The language in this License shall be interpreted as to its fair meaning and not strictly for or against any party.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

*The Hippocratic License is an Ethical Source license[⁵](#appendix1.xhtml_fnapp1_5).*

# BCode of Conduct

In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, education, socioeconomic status, nationality, personal appearance, race, religion, or sexual identity and orientation.

## Our Standards

Examples of behavior that contributes to creating a positive environment include:

*   using welcoming and inclusive language,

*   being respectful of differing viewpoints and experiences,

*   gracefully accepting constructive criticism,

*   focusing on what is best for the community, and

*   showing empathy towards other community members.

Examples of unacceptable behavior by participants include:

*   the use of sexualized language or imagery and unwelcome sexual attention or advances,

*   trolling, insulting/derogatory comments, and personal or political attacks,

*   public or private harassment,

*   publishing others’ private information, such as a physical or electronic address, without explicit permission, and

*   other conduct which could reasonably be considered inappropriate in a professional setting

## Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable behavior and are expected to take appropriate and fair corrective action in response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or reject comments, commits, code, wiki edits, issues, and other contributions that are not aligned to this Code of Conduct, or to ban temporarily or permanently any contributor for other behaviors that they deem inappropriate, threatening, offensive, or harmful.

## Scope

This Code of Conduct applies both within project spaces and in public spaces when an individual is representing the project or its community. Examples of representing a project or community include using an official project email address, posting via an official social media account, or acting as an appointed representative at an online or offline event. Representation of a project may be further defined and clarified by project maintainers.

## Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be reported by emailing the project team. All complaints will be reviewed and investigated and will result in a response that is deemed necessary and appropriate to the circumstances. The project team is obligated to maintain confidentiality with regard to the reporter of an incident. Further details of specific enforcement policies may be posted separately.

Project maintainers who do not follow or enforce the Code of Conduct in good faith may face temporary or permanent repercussions as determined by other members of the project's leadership.

## Attribution

This Code of Conduct is adapted from the Contributor Covenant[¹](#appendix2.xhtml_fnapp2_1) version 1.4.

# CContributing

Contributions are very welcome; please contact us by email or by filing an issue on this site. All contributors must abide by our Code of Conduct.

## Making Decisions

This project uses Martha's Rules[¹](#appendix3.xhtml_fnapp3_1) for consensus decision making:

1.  Before each meeting, anyone who wishes may sponsor a proposal by filing an issue in the GitHub repository tagged “proposal”. People must file proposals at least 24 hours before a meeting in order for them to be considered at that meeting, and must include:

    *   a one-line summary (the subject line of the issue)

    *   the full text of the proposal

    *   any required background information

    *   pros and cons

    *   possible alternatives

2.  A quorum is established in a meeting if half or more of voting members are present.

3.  Once a person has sponsored a proposal, they are responsible for it. The group may not discuss or vote on the issue unless the sponsor or their delegate is present. The sponsor is also responsible for presenting the item to the group.

4.  After the sponsor presents the proposal, a “sense” vote is cast for the proposal before any discussion:

    *   Who likes the proposal?

    *   Who can live with the proposal?

    *   Who is uncomfortable with the proposal?

5.  If everyone likes or can live with the proposal, it passes immediately.

6.  If most of the group is uncomfortable with the proposal, it is postponed for further rework by the sponsor.

7.  Otherwise, members who are uncomfortable can briefly state their objections. A timer is then set for a brief discussion moderated by the facilitator. After 10 minutes or when no one has anything further to add (whichever comes first), the facilitator calls for a yes-or-no vote on the question: “Should we implement this decision over the stated objections?” If a majority votes “yes” the proposal is implemented. Otherwise, the proposal is returned to the sponsor for further work.

## Formatting

This material uses Ivy[²](#appendix3.xhtml_fnapp3_2) with some custom extensions. Run make in the root directory to get a list of available commands. Some of these rely on scripts in the ./bin/ directory. Please see our Git repository[³](#appendix3.xhtml_fnapp3_3) for up-to-date instructions.

# DBibliography

*   **[Binkley2012]** Dave Binkley, Marcia Davis, Dawn Lawrie, Jonathan I. Maletic, Christopher Morrell, and Bonita Sharif. ‘‘The Impact of Identifier Style on Effort and Comprehension’’. In: ESE 18.2 (2012). doi: [10.1007/s10664-012-9201-4](http://doi.org/10.1007/s10664-012-9201-4).
*   [**[Brand1995]**](#chapter7.xhtml_b7refbib_2) Stewart Brand. How Buildings Learn: What Happens After They’re Built. Penguin USA, 1995\. isbn: 978-0140139969.
*   [**[Brown2016]**](#chapter1.xhtml_b1refbib_3) Amy Brown and Michael DiBernardo, eds. 500 Lines or Less: Experienced Programmers Solve Interesting Problems. Lulu, 2016. isbn: 978-1329871274.
*   [**[Brown2011]**](#chapter1.xhtml_b1refbib_4) Amy Brown and Greg Wilson, eds. The Architecture of Open Source Applications: Elegance, Evolution, and a Few Fearless Hacks. Lulu, 2011\. isbn: 978-1257638017.
*   [**[Brown2012]**](#chapter1.xhtml_b1refbib_5) Amy Brown and Greg Wilson, eds. The Architecture of Open Source Applications: Structure, Scale, and a Few More Fearless Hacks. Lulu, 2012\. isbn: 9780201103427.
*   **[Casciaro2020]** Mario Casciaro and Luciano Mammino. Node.js Design Patterns. Packt, 2020\. isbn: 978-1839214110.
*   [**[Conery2021]**](#chapter8.xhtml_b8refbib_7) Rob Conery. The Imposter’s Handbook: A CS Primer for Self-Taught Developers. Independently published, 2021\. isbn: 978-8708185266.
*   [**[Davis2018]**](#chapter6.xhtml_b6refbib_8) Ashley Davis. Data Wrangling with JavaScript. Manning, 2018\. isbn: 9781617294846.
*   [**[Feathers2004]**](#chapter5.xhtml_b5refbib_9) Michael C. Feathers. Working Effectively with Legacy Code. Prentice-Hall, 2004\. isbn: 978-0131177055.
*   [**[Fucci2017]**](#chapter7.xhtml_b7refbib_10) Davide Fucci, Hakan Erdogmus, Burak Turhan, Markku Oivo, and Natalia Juristo. ‘‘A Dissection of the Test-Driven Development Process: Does It Really Matter to Test-First or to Test-Last?’’ In: TSE 43.7 (July 2017). doi: [10.1109/tse.2016.2616877](http://doi.org/10.1109/tse.2016.2616877).
*   [**[Fucci2016]**](#chapter7.xhtml_b7refbib_11) Davide Fucci, Giuseppe Scanniello, Simone Romano, Martin Shepperd, Boyce Sigweni, Fernando Uyaguari, Burak Turhan, Natalia Juristo, and Markku Oivo. ‘‘An External Replication on the Effects of Test-driven Development Using a Multi-site Blind Analysis Approach’’. In: Proc. ESEM’16. ACM Press, 2016\. doi: [10.1145/2961111.2962592](http://doi.org/10.1145/2961111.2962592).
*   [**[Gregg2020]**](#chapter2.xhtml_b2refbib_12) Brendan Gregg. Systems Performance: Enterprise and the Cloud. Pearson, 2020\. isbn: 978-0136820154.
*   **[Johnson2019]** John Johnson, Sergio Lubo, Nishitha Yedla, Jairo Aponte, and Bonita Sharif. ‘‘An Empirical Study Assessing Source Code Readability in Comprehension’’. In: Proc. ICSME’19. 2019\. doi: [10.1109/ICSME.2019.00085](http://doi.org/10.1109/ICSME.2019.00085).
*   [**[Kernighan1983]**](#chapter1.xhtml_b1refbib_14) Brian W. Kernighan and Rob Pike. The Unix Programming Environment. Prentice-Hall, 1983\. isbn: 978-0139376818.
*   [**[Kernighan1979]**](#chapter1.xhtml_b1refbib_15) Brian W. Kernighan and P. J. Plauger. The Elements of Programming Style. McGraw-Hill, 1979\. isbn: 978-0070342071.
*   [**[Kernighan1981]**](#chapter1.xhtml_b1refbib_16) Brian W. Kernighan and P. J. Plauger. Software Tools in Pascal. Addison-Wesley Professional, 1981\. isbn: 978-0201103427.
*   [**[Kernighan1988]**](#chapter1.xhtml_b1refbib_17) Brian W. Kernighan and Dennis M. Ritchie. The C Programming Language. Prentice-Hall, 1988\. isbn: 978-0131103627.
*   [**[Kohavi2020]**](#chapter6.xhtml_b6refbib_18) Ron Kohavi, Diane Tang, and Ya Xu. Trustworthy Online Controlled Experiments: A Practical Guide to A/B Testing. Cambridge University Press, 2020\. isbn: 978-1108724265.
*   [**[Meszaros2007]**](#chapter4.xhtml_b4refbib_19) Gerard Meszaros. xUnit Test Patterns: Refactoring Test Code. Addison-Wesley, 2007\. isbn: 978-0131495050.
*   [**[Oram2007]**](#chapter1.xhtml_b1refbib_20) Andy Oram and Greg Wilson, eds. Beautiful Code: Leading Programmers Explain How They Think. O’Reilly, 2007\. isbn: 978-0596510046.
*   [**[Osmani2017]**](#chapter4.xhtml_b4refbib_21) Addy Osmani. *Learning JavaScript Design Patterns*. 2017\. url: [https://addyosmani.com/resources/essentialjsdesignpatterns/book/](https://addyosmani.com).
*   [**[Patterson2017]**](#chapter6.xhtml_b6refbib_22) David A. Patterson and John L. Hennessy. Computer Organization and Design: The Hardware/Software Interface. Morgan Kaufmann, 2017. isbn: 9780128122754.
*   [**[Petre2016]**](#chapter1.xhtml_b1refbib_23) Marian Petre and André van der Hoek. Software Design Decoded: 66 Ways Experts Think. MIT Press, 2016\. isbn: 978-0262035187.
*   [**[Petzold2008]**](#chapter17.xhtml_b17refbib_24) Charles Petzold. The Annotated Turing. Wiley, 2008\. isbn: 978-0470229057.
*   [**[Schon1984]**](#chapter1.xhtml_b1refbib_25) Donald A. Schon. The Reflective Practitioner: How Professionals Think in Action. Basic Books, 1984\. isbn: 978-0465068784.
*   [**[Smith2011]**](#chapter10.xhtml_b10refbib_26) Peter Smith. Software Build Systems: Principles and Experience. Addison-Wesley Professional, 2011\. isbn: 978-0134185965.
*   [**[Taschuk2017]**](#chapter18.xhtml_b18refbib_27) Morgan Taschuk and Greg Wilson. ‘‘Ten Simple Rules for Making Research Software More Robust’’. In: PLoS Comp Bio 13.4 (Apr. 2017). doi: [10.1371/journal.pcbi.1005412](http://doi.org/10.1371/journal.pcbi.1005412).
*   [**[Tudose2020]**](#chapter4.xhtml_b4refbib_28) Cătălin Tudose. JUnit in Action. Manning, 2020\. isbn: 978-1617297045.

# EGlossary

absolute error:

The absolute value of the difference between the observed and the correct value. Absolute error is usually less useful than **relative error**.

absolute path:

A path that points to the same location in the **filesystem** regardless of where it is evaluated. An absolute path is the equivalent of latitude and longitude in geography.

abstract method:

In **object-oriented programming**, a **method** that is defined but not implemented. Programmers will define an abstract method in a **parent class** to specify operations that **child classes** must provide.

abstract syntax tree (AST):

A deeply nested data structure, or **tree**, that represents the structure of a program. For example, the AST might have a **node** representing a while loop with one **child** representing the loop condition and another representing the **loop body**.

accidental complexity:

The extra (avoidable) complexity introduced by poor design choices. The term is used in contrast with **intrinsic complexity**.

accumulator:

A variable that collects and/or combines many values. For example, if a program sums the values in an array by adding them all to a variable called result, then result is the accumulator.

actual result (of test):

The value generated by running code in a test. If this matches the **expected result**, the test **passes**; if the two are different, the test **fails**.

Adapter pattern:

A **design pattern** that rearranges parameters, provides extra values, or does other work so that one function can be called by another.

alias:

A second or subsequent reference to the same object. Aliases are useful, but increase the **cognitive load** on readers who have to remember that all these names refer to the same thing.

anonymous function:

A function that has not been assigned a name. Anonymous functions are usually quite short, and are usually defined where they are used, e.g., as callbacks. In Python, these are called lambda functions and are created through use of the lambda reserved word.

Application Binary Interface (ABI):

The low-level layout that a piece of software must have to work on a particular kind of machine.

Application Programming Interface (API):

A set of functions provided by a software library or web service that other software can call.

argument:

A value passed to a function when it is called.

ASCII:

A standard way to represent the characters commonly used in the Western European languages as 7- or 8-bit integers, now largely superceded by **Unicode**.

assembler:

A **compiler** that translates software written in **assembly code** into machine instructions.

assembly code:

A low-level programming language whose statements correspond closely to the actual **instruction set** of a particular kind of processor.

assertion:

A **Boolean** expression that must be true at a certain point in a program. Assertions may be built into the language (e.g., Python's assert statement) or provided as functions (as with Node's assert library).

associative array:

See **dictionary**.

asynchronous:

Not happening at the same time. In programming, an asynchronous operation is one that runs independently of another, or that starts at one time and ends at another.

attribute:

A name-value pair associated with an object, used to store metadata about the object such as an array's dimensions.

automatic variable:

A variable that is automatically given a value in a **build rule**. For example, Make automatically assigns the name of a rule's **target** to the automatic variable $@. Automatic variables are frequently used when writing **pattern rules**.

backward-compatible:

A property of a system that enables interoperability with an older legacy system, or with input designed for such a system.

bare object:

An object that isn't an instance of any particular class.

base class:

In **object-oriented programming**, a **class** from which other classes are derived.

binary:

A system which can have one of two possible states, often represented as 0 and 1 or true and false.

bit:

A single binary digit (0 or 1).

bitwise operation:

An operation that manipulates individual bits in memory. Common bitwise operations include and, or, not, and xor.

block comment:

A **comment** that spans multiple lines. Block comments may be marked with special start and end symbols, like /* and */ in C and its descendents, or each line may be prefixed with a marker like #.

Boolean:

Relating to a variable or data type that can have either a logical value of true or false. Named for George Boole, a 19th century mathematician.

breadth first:

To go through a nested data structure such as a **tree** by exploring all of one level, then going on to the next level and so on, or to explore a problem by examining the first step of each possible solution, and then trying the next step for each.

breakpoint:

An instruction to a debugger telling it to suspend execution whenever a specific point in the program (such as a particular line) is reached.

bug:

A missing or undesirable **feature** of a piece of software.

build manager:

A program that keeps track of how files depend on one another and runs commands to update any files that are out-of-date. Build managers were invented to **compile** only those parts of programs that had changed, but are now often used to implement workflows in which plots depend on results files, which in turn depend on raw data files or configuration files.

build recipe:

The part of a **build rule** that describes how to update something that has fallen out-of-date.

build rule:

A specification for a **build manager** that describes how some files depend on others and what to do if those files are out-of-date.

build target:

The file(s) that a **build rule** will update if they are out-of-date compared to their **dependencies**.

byte code:

A set of instructions designed to be executed efficiently by an **interpreter**.

cache:

Something that stores copies of data so that future requests for it can be satisfied more quickly. The CPU in a computer uses a hardware cache to hold recently-accessed values; many programs rely on a software cache to reduce network traffic and latency. Figuring out when something in a cache is out-of-date and should be replaced is one of the **two hard problems in computer science**.

caching:

To save a copy of some data in a local **cache** to make future access faster.

call stack:

A data structure that stores information about the active subroutines executed.

callback function:

A function A that is passed to another function B so that B can call it at some later point. Callbacks can be used **synchronously**, as in generic functions like map that invoke a callback function once for each element in a collection, or **asynchronously**, as in a **client** that runs a callback when a **response** is received in answer to a **request**.

Cascading Style Sheets (CSS):

A way to control the appearance of HTML. CSS is typically used to specify fonts, colors, and layout.

catch (an exception):

To handle an error or other unexpected event represented by an **exception**.

Chain of Responsibility pattern:

A **design pattern** in which each **object** either handles a request or passes it on to another object.

character encoding:

A specification of how characters are stored as bytes. The most commonly-used encoding today is **UTF-8**.

child (in a tree):

A **node** in a **tree** that is below another node (called the **parent**).

child class:

In **object-oriented programming**, a **class** derived from another class (called the **parent class**).

circular dependency:

A situation in which X depends on Y and Y depends on X, either directly or indirectly. If there is a circular dependency, then the **dependency graph** is not **acyclic**.

class:

In **object-oriented programming**, a structure that combines data and operations (called **methods**). The program then uses a **constructor** to create an **object** with those properties and methods. Programmers generally put generic or reusable behavior in **parent classes**, and more detailed or specific behavior in **child classes**.

client:

A program such as a web browser that gets data from a **server** and displays it to, or interacts with, users. The term is used more generally to refer to any program A that makes requests of another program B. A single program can be both a client and a server.

closure:

A set of variables defined in the same **scope** whose existence has been preserved after that scope has ended.

code coverage (in testing):

How much of a **library** or program is executed when tests run. This is normally reported as a percentage of lines of code.

cognitive load:

The amount of working memory needed to accomplish a set of simultaneous tasks.

collision:

A situation in which a program tries to store two items in the same location in memory. For example, a collision occurs when a **hash function** generates the same **hash code** for two different items.

column-major storage:

Storing each column of a two-dimensional array as one block of memory so that elements in the same row are far apart.

combinatorial explosion:

The exponential growth in the size of a problem or the time required to solve it that arises when all possible combinations of a set of items must be searched.

comma-separated values (CSV):

A text format for tabular data in which each **record** is one row and **fields** are separated by commas. There are many minor variations, particularly around quoting of **strings**.

command-line argument:

A filename or control flag given to a command-line program when it is run.

command-line interface (CLI):

A user interface that relies solely on text for commands and output, typically running in a **shell**.

comment:

Text written in a script that is not treated as code to be run, but rather as text that describes what the code is doing. These are usually short notes, often beginning with a # (in many programming languages).

compile:

To translate textual source into another form. Programs in **compiled languages** are translated into machine instructions for a computer to run, and **Markdown** is usually translated into **HTML** for display.

compiled language:

Originally, a language such as C or Fortran that is translated into machine instructions for execution. Languages such as Java are also compiled before execution, but into **byte code** instead of machine instructions, while **interpreted languages** like JavaScript are compiled to byte code on the fly.

compiler:

An application that translates programs written in some languages into machine instructions or **byte code**.

confirmation bias:

The tendency for someone to look for evidence that they are right rather than searching for reasons why they might be wrong.

console:

A computer terminal where a user may enter commands, or a program, such as a shell that simulates such a device.

constructor:

A function that creates an **object** of a particular **class**.

Coordinated Universal Time (UTC):

The standard time against which all others are defined. UTC is the time at longitude 0°, and is not adjusted for daylight savings. **Timestamps** are often reported in UTC so that they will be the same no matter what timezone the computer is in.

corner case:

Another name for an **edge case**.

coupling:

The degree of interaction between two **classes**, **modules**, or other software components. If a system's components are **loosely coupled**, changes to one are unlikely to affect others. If they are **tightly coupled**, then any change requires other changes elsewhere, which complicates maintenance and evolution.

cryptographic hash function:

A **hash function** that produces an apparently-random value for any input.

current working directory:

The **folder** or **directory** location in which the program operates. Any action taken by the program occurs relative to this directory.

cycle (in a graph):

A set of links in a graph that leads from a node back to itself.

data frame:

A two-dimensional data structure for storing tabular data in memory. Rows represent **records** and columns represent **fields**.

data migration:

Moving data from one location or format to another. The term refers to translating data from an old format to a newer one.

Decorator pattern:

A **design pattern** in which a function adds additional features to another function or a **class** after its initial definition. Decorators are a feature of Python and can be implemented in most other languages as well.

defensive programming:

A set of programming practices that assumes mistakes will happen and either reports or corrects them, such as inserting **assertions** to report situations that are not ever supposed to occur.

dependency:

See **prerequisite**.

dependency graph:

A **directed graph** showing how things depend on one another, such as the files to be updated by a **build manager**. If the dependency graph is not **acyclic**, the dependencies cannot be resolved.

deprecation:

To indicate that while a function, method, or class exists, its use is no longer recommended (for example, because it is going to be phased out in a future release).

depth-first:

A search algorithm that explores one possibility all the way to its conclusion before moving on to the next.

derived class:

In **object-oriented programming**, a class that is a direct or indirect extension of a **base class**.

design by contract:

A style of designing software in which functions specify the **pre-conditions** that must be true in order for them to run and the **post-conditions** they guarantee will be true when they return. A function can then be replaced by one with weaker pre-conditions (i.e., it accepts a wider set of input) and/or stronger post-conditions (i.e., it produces a smaller range of output) without breaking anything else.

design pattern:

A recurring pattern in software design that is specific enough to be worth naming, but not so specific that a single best implementation can be provided by a **library**.

destructuring assignment:

Unpacking values from data structures and assigning them to multiple variables in a single statement.

dictionary:

A data structure that allows items to be looked up by value, sometimes called an **associative array**. Dictionaries are often implemented using **hash tables**.

directed acyclic graph (DAG):

A **directed graph** which does not contain any loops (i.e., it is not possible to reach a **node** from itself by following edges).

directed graph:

A **graph** whose **edges** have directions.

directory:

A structure in a **filesystem** that contains references to other structures, such as files and other directories.

disassembler:

A program that translates machine instructions into **assembly code** or some other higher-level language.

doc comment:

A documentation comment (“doc comment” for short) is a specially-formatted comment containing documentation about a piece of code that is embedded in the code itself.

Document Object Model (DOM):

A standard, in-memory representation of **HTML** and **XML**. Each **element** is stored as a **node** in a **tree** with a set of named **attributes**; contained elements are **child nodes**.

driver:

A program that runs other programs, or a function that drives all of the other functions in a program.

dynamic loading:

To **import** a **module** into the memory of a program while it is already running. Most **interpreted languages** use dynamic loading, and provide tools so that programs can find and load modules dynamically to configure themselves.

dynamic lookup:

To find a function or a property of an **object** by name while a program is running. For example, instead of getting a specific property of an object using obj.name, a program might use obj[someVariable], where someVariable could hold "name" or some other property name.

dynamic scoping:

To find the value of a variable by looking at what is on the **call stack** at the moment the lookup is done. Almost all programming languages use **lexical-scoping** instead, since it is more predictable.

eager matching:

Matching as much as possible, as early as possible.

easy mode:

A term borrowed from gaming meaning to do something with obstacles or difficulties simplified or removed, often for practice purposes.

edge:

A connection between two **nodes** in a **graph**. An edge may have data associated with it, such as a name or distance.

edge case:

A problem that only comes up under unusual circumstances or when a system is pushed to its limits; also sometimes called a **corner case**. Programs intended for widespread use have to handle edge cases, but doing so can make them much more complicated.

element:

A named component in an **HTML** or **XML** document. Elements are usually written < name >… < /name >, where “…” represents the content of the element. Elements often have **attributes**.

encapsulate:

To store data inside some kind of structure so that it is only accessible through that structure.

entry point:

Where a program begins executing.

environment:

A structure that stores a set of variable names and the values they refer to.

error (in a test):

Signalled when something goes wrong in a **unit test** itself rather than in the system being tested. In this case, we do not know anything about the correctness of the system.

error handling:

What a program does to detect and correct for errors. Examples include printing a message and using a default configuration if the user-specified configuration cannot be found.

event loop:

A mechanism for managing concurrent activities in a program. Tasks are represented as items in a queue; the event loop repeatedly takes an item from the front of the queue and runs it, adding any other tasks it generates to the back of the queue to run later.

exception:

An object that stores information about an error or other unusual event in a program. One part of a program will create and **raise an exception** to signal that something unexpected has happened; another part will **catch** it.

exception handler:

A piece of code that deals with an **exception** after it is **caught**, e.g., by recording a message, retrying the operation that failed, or performing an alternate operation.

expected result (of test):

The value that a piece of software is supposed to produce when tested in a certain way, or the state in which it is supposed to leave the system.

exploratory programming:

A software development methodology in which requirements emerge or change as the software is being written, often in response to results from early runs.

export:

To make something visible outside a **module** so that other parts of a program can **import** it. In most languages a module must export things explicitly in an attempt to avoid **name collision**.

fail (a test):

A test fails if the **actual result** does not match the **expected result**.

feature (in software):

Some aspect of software that was deliberately designed or built. A **bug** is an undesired feature.

field:

A component of a **record** containing a single value. Every record in a database **table** has the same fields.

filename extension:

The last part of a filename, usually following the ‘.’ symbol. Filename extensions are commonly used to indicate the type of content in the file, though there is no guarantee that this is correct.

filesystem:

The part of the **operating system** that manages how files are stored and retrieved. Also used to refer to all of those files and **directories** or the specific way they are stored (as in “the Unix filesystem”).

filter:

As a verb, to choose a set of **records** (i.e., rows of a table) based on the values they contain. As a noun, a command-line program that reads lines of text from files or **standard input**, performs some operation on them (such as filtering), and writes to a file or **stdout**.

finite state machine (FSM):

A theoretical model of computing consisting of a directed graph whose nodes represent the states of the computation and whose arcs show how to move from one state to another. Every **regular expression** corresponds to a finite state machine.

fixed-width (of strings):

A set of character strings that have the same length. Databases often used fixed-width strings to make storage and access more efficient; short strings are **padded** up to the required length and long strings are truncated.

fixture:

The thing on which a test is run, such as the **parameters** to the function being tested or the file being processed.

fluent interface:

A style of object-oriented programming in which methods return objects so that other methods can immediately be called.

folder:

Another term for a **directory**.

garbage collection:

The process of identifying memory that has been allocated but is no longer in use and reclaiming it to be re-used.

generator function:

A function whose state is automatically saved when it returns a value so that execution can be restarted from that point the next time it is called. One example of generator functions use is to produce streams of values that can be processed by for loops.

generic function:

A collection of functions with similar purpose, each operating on a different class of data.

global variable:

A variable defined outside any particular function or **package** namespace, which is therefore visible to all functions.

globbing:

To specify a set of filenames using a simplified form of **regular expressions**, such as *.dat to mean “all files whose names end in .dat”. The name is derived from “global”.

graph:

A plot or a chart that displays data, or a data structure in which **nodes** are connected to one another by **edges**.

greedy algorithm:

An algorithm that consumes as much input as possible, as early as possible.

handler:

A **callback function** responsible for handling some particular event, such as the user clicking on a button or new data being received from a file.

hash code:

A value generated by a **hash function**. Good hash codes have the same properties as random numbers in order to reduce the frequency of **collisions**.

hash function:

A function that turns arbitrary data into a bit array, or a **key**, of a fixed size. Hash functions are used to determine where data should be stored in a **hash table**.

hash table:

A data structure that calculates a pseudo-random key (location) for each value passed to it and stores the value in that location. Hash tables enable fast lookup for arbitrary data. This occurs at the cost of extra memory because hash tables must always be larger than the amount of information they need to store, to avoid the possibility of data collisions, when the hash function returns the same key for two different values.

header file:

In C and C++, a file that defines constants and function **signatures** but does not contain runnable code. Header files tell the including file what is defined in other files so that the compiler can generate correct code.

heterogeneous:

Containing mixed data types. For example, an array in Javascript can contain a mix of numbers, character strings, and values of other types.

heuristic:

A rule or guideline that isn't guaranteed to produce the desired result, but usually does.

homogeneous:

Containing a single data type. For example, a **vector** must be homogeneous: its values must all be numeric, logical, etc.

HTTP request:

A message sent from a **client** to a **server** using the **HTTPprotocol** asking for data. A request usually asks for a web page, image, or other data.

HTTP response:

A reply sent from a **server** to a **client** using the **HTTPprotocol** in response to a **request**. The response usually contains a web page, image, or data.

HyperText Markup Language (HTML):

The standard **markup language** used for web pages. HTML is represented in memory using **DOM** (Digital Object Model).

HyperText Transfer Protocol (HTTP):

The standard **protocol** for data transfer on the World-Wide Web. HTTP defines the format of **requests** and **responses**, the meanings of standard error codes, and other features.

idiomatic:

To use a language in the same way as a fluent or native speaker. Programs are called idiomatic if they use the language the way that proficient programmers use it.

immediately-invoked function expression (IIFE):

A function that is invoked once at the point where it is defined. IIFEs are typically used to create a **scope** to hide some function or variable definitions.

immutable:

Data that cannot be changed after being created. Immutable data is easier to think about, particularly if data structures are shared between several tasks, but may result in higher memory requirements.

import:

To bring things from a **module** into a program for use. In most languages a program can only import things that the module explicitly **exports**.

index (in a database):

An auxiliary data structure in a database used to speed up search for some entries. An index increases memory and disk requirements but reduces search time.

inner function:

A function defined inside another (outer) function. Creating and returning inner functions is a way to create **closures**.

instance:

An **object** of a particular **class**.

instruction pointer:

A special **register** in a processor that stores the address of the next instruction to execute.

instruction set:

The basic operations that a particular processor can execute directly.

interpreted language:

A high-level language that is not executed directly by the computer, but instead is run by an **interpreter** that translates program instructions into machine commands on the fly.

interpreter:

A program whose job it is to run programs written in a high-level **interpreted language**. Interpreters can run interactively, but may also execute commands saved in a file.

intrinsic complexity:

The unavoidable complexity inherent in a problem that any solution must deal with. The term is used in contrast with **accidental complexity**.

introspection:

Having a program examine itself as it is running; common examples are to determine the specific class of a generic object or to get the fields of an object when they are not known in advance.

ISO date format:

An international standard for formatting dates. While the full standard is complex, the most common form is YYYY-MM-DD, i.e., a four-digit year, a two-digit month, and a two-digit day, separated by hyphens.

Iterator pattern:

A **design pattern** in which a temporary **object** or **generator function** produces each value from a collection in turn for processing. This pattern hides the differences between different kinds of data structures so that everything can be processed using loops.

JavaScript Object Notation (JSON):

A way to represent data by combining basic values like numbers and character strings in **lists** and **key/value** structures. The acronym stands for “JavaScript Object Notation”; unlike better-defined standards like **XML**, it is unencumbered by a syntax for comments or ways to define a **schema**.

join:

An operation that combines two **tables**, typically by matching **keys** from one with keys from another.

key:

A **field** or combination of fields whose value(s) uniquely identify a **record** within a **table** or dataset. Keys are often used to select specific records and in **joins**.

label (address in memory):

A human-readable name given to a particular location in memory when writing programs in **assembly code**.

layout engine:

A piece of software that decides where to place text, images, and other elements on a page.

lazy matching:

Matching as little as possible while still finding a valid match.

Least Recently Used cache (LRU cache):

A **cache** that discards items that have not been used recently in order to limit memory requirements.

lexical scoping:

To look up the value associated with a name according to the textual structure of a program. Most programming languages use lexical scoping instead of **dynamic scoping** because the latter is less predictable.

library:

An installable collection of software, also often called a **module** or **package**.

lifecycle:

The steps that something is allowed or required to go through. The lifecycle of an **object** runs from its **construction** through the operations it can or must perform before it is destroyed.

line comment:

A **comment** in a program that spans part of a single line, as opposed to a **block comment** that may span multiple lines.

link (a program):

To combine separately **compiled** modules into a single runnable program.

linter:

A program that checks for common problems in software, such as violations of indentation rules or variable naming conventions. The name comes from the first tool of its kind, called lint.

Liskov Substitution Principle:

A design rule stating that it should be possible to replace objects in a program with objects of derived classes without breaking the program. **Design by contract** is intended to enforce this rule.

list:

A **vector** that can contain values of many different (**heterogeneous**) types.

literal:

A representation of a fixed value in a program, such as the digits 123 for the number 123 or the characters "abc" for the string containing those three letters.

literate programming:

A programming paradigm that mixes prose and code so that explanations and instructions are side by side.

loader:

A function whose job is to read files containing runnable code into memory and make that code available to the calling program.

local variable:

A variable defined inside a function which is only visible within that function.

log message:

A status report or error message written to a file as a program runs.

loop body:

The statement or statements executed by a loop.

loosely coupled:

Components in a software system are said to be loosely coupled if they are relatively independent of one another, i.e., if any one of them can be changed or replaced without others having to be altered as well.

macro:

Originally short for “macro-instruction”, an instruction to translate some of the text into a program into other text before using it.

Makefile:

A configuration file for the original **build manager**.

manifest:

A list that specifies the precise versions of a complete set of libraries or other software components.

Markdown:

A **markup language** with a simple syntax intended as a replacement for **HTML**.

markup language:

A set of rules for annotating text to define its meaning or how it should be displayed. The markup is usually not displayed, but instead controls how the underlying text is interpreted or shown. **Markdown** and **HTML** are widely-used markup languages for web pages.

method:

An implementation of a **generic function** that handles objects of a specific class.

method chaining:

A style of object-oriented programming in which an object's methods return that object as their result so that another method can immediately be called, as in obj.a().b().c().

mock object:

A simplified replacement for part of a program whose behavior is easy to control and predict. Mock objects are used in **unit tests** to simulate databases, web services, and other complex systems.

module:

A reusable software **package**, also often called a **library**.

module bundler:

A program that finds all the dependencies of a set of source files and combines them into a single loadable file.

multi-threaded:

Capable of performing several operations simultaneously. Multi-threaded programs are usually more efficient than **single-threaded** ones, but also harder to understand and debug.

name collision:

The ambiguity that arises when two or more things in a program that have the same name are active at the same time. Most languages use **namespaces** to prevent such collisions.

namespace:

A collection of names in a program that exists in isolation from other namespaces. Each function, **object**, **class**, or **module** in a program typically has its own namespace so that references to “X” in one part of a program do not accidentally refer to something called “X” in another part of the program. Scope is a distinct, but related, concept.

nested function:

A function that is defined inside another function.

node:

An element of a **graph** that is connected to other nodes by **edges**. Nodes typically have data associated with them, such as names or weights.

non-blocking execution:

To allow a program to continue running while an operation is in progress. For example, many systems support non-blocking execution for file I/O so that the program can continue doing work while it waits for data to be read from or written to the **filesystem** (which is typically much slower than the CPU).

object:

In **object-oriented programming**, a structure that contains the data for a specific instance of a **class**. The operations the object is capable of are defined by the class's **methods**.

object-oriented programming (OOP):

A style of programming in which functions and data are bound together in **objects** that only interact with each other through well-defined interfaces.

off-by-one error:

A common error in programming in which the program refers to element i of a structure when it should refer to element i-1 or i+1, or processes N elements when it should process N-1 or N+1.

op code:

The numerical code for a particular instruction that a processor can execute.

Open-Closed Principle:

A design rule stating that software should be open for extension but closed for modification, i.e., it should be possible to extend functionality without having to rewrite existing code.

operating system:

A program that provides a standard interface to whatever hardware it is running on. Theoretically, any program that only interacts with the operating system should run on any computer that operating system runs on.

package:

A collection of code, data, and documentation that can be distributed and re-used. Also referred to in some languages as a **library** or **module**.

pad (a string):

To add extra characters to a string to make it a required length.

parameter:

A variable specified in a function definition that is assigned a value when the function is called.

parent (in a tree):

A **node** in a **tree** that is above another node (called a **child**). Every node in a tree except the **root node** has a single parent.

parent class:

In **object-oriented programming**, the **class** from which a sub class (called the **child class**) is derived.

parser:

A piece of software that translates a textual representation of something into a data structure. For example, a **YAML** parser reads indented text and produces nested lists and objects.

pass (a test):

A test passes if the **actual result** matches the **expected result**.

patch:

A single file containing a set of changes to a set of files, separated by markers that indicate where each individual change should be applied.

path (in filesystem):

A **string** that specifies a location in a **filesystem**. In Unix, the **directories** in a path are joined using /.

pattern rule:

A generic **build rule** that describes how to update any file whose name matches a pattern. Pattern rules often use **automatic variables** to represent the actual filenames.

pipe:

To use the output of one computation as the input for the next, or the connection between the two computations responsible for the data transfer. Pipes were popularized by the **Unix shell**, and are now used in many different programming languages and systems.

pipe (in the Unix shell):

The | used to make the output of one command the input of the next.

plugin architecture:

A style of application design in which the main program loads and runs small independent modules that do the bulk of the work.

polymorphism:

Having many different implementations of the same interface. If a set of functions or objects are polymorphic, they can be called interchangeably.

post-condition:

Something that is guaranteed to be true after a function runs successfully. Post-conditions are often expressed as **assertions** that are guaranteed to be true of a function's results.

pre-condition:

Something that must be true before a function runs in order for it to work correctly. Pre-conditions are often expressed as as **assertions** that must be true of a function's inputs in order for it to run successfully.

precedence:

The priority of an operation. For example, multiplication has a higher precedence than addition, so a+b*c is read as “the sum of a with the product of b and c”.

prerequisite:

Something that a **build target** depends on.

process:

An **operating system**‘s representation of a running program. A process typically has some memory, the identity of the user who is running it, and a set of connections to open files.

promise:

A way to represent the result of a delayed or **asynchronous** computation. A promise is a placeholder for a value that will eventually be computed; any attempt to read the value before it is available blocks, while any such attempt after the computation finishes acts like a normal read.

promisification:

In JavaScript, the act of wrapping a callback function in a **promise** for uniform asynchronous execution.

protocol:

Any standard specifying how two pieces of software interact. A network protocol such as **HTTP** defines the messages that **clients** and **servers** exchange on the World-Wide Web; **object-oriented** programs often define protocols for interactions between **objects** of different **classes**.

prune:

To remove branches and nodes from a tree, or to rule out partially-complete solutions when searching for an overall solution in order to reduce work.

pseudo-random number:

A value generated in a repeatable way that resembles the true randomness of the universe well enough to fool observers.

pseudo-random number generator (PRNG):

A function that can generate **pseudo-random numbers**.

query selector:

A pattern that specifies a set of **DOM** nodes. Query selectors are used in **CSS** to specify the elements that rules apply to, or by JavaScript programs to manipulate web pages.

query string:

The portion of a **URL** after the question mark ? that specifies extra parameters for the **HTTP request** as name-value pairs.

race condition:

A situation in which a result depends on the order in which two or more concurrent operations are carried out.

raise (an exception):

To signal that something unexpected or unusual has happened in a program by creating an **exception** and handing it to the **error-handling** system, which then tries to find a point in the program that will **catch** it.

read-eval-print loop (REPL):

An interactive program that reads a command typed in by a user, executes it, prints the result, and then waits patiently for the next command. REPLs are often used to explore new ideas, or for debugging.

record:

A group of related values that are stored together. A record may be represented as a **tuple** or as a row in a **table**; in the latter case, every record in the table has the same **fields**.

register:

A small piece of memory (typically one **word** long) built into a processor that operations can refer to directly.

regular expression:

A pattern for matching text, written as text itself. Regular expressions are sometimes called “regexp”, “regex”, or “RE”, and are powerful tools for working with text.

relational database:

A database that organizes information into **tables**, each of which has a fixed set of named **fields** (shown as columns) and a variable number of **records** (shown as rows).

relative error:

The absolute value of the difference between the actual and correct value divided by the correct value. For example, if the actual value is 9 and the correct value is 10, the relative error is 0.1\. Relative error is usually more useful than **absolute error**.

relative path:

A path that is interpreted relative to some other location, such as the **current working directory**. A relative path is the equivalent of giving directions using terms like “straight” and “left”.

root (in a tree):

The **node** in a **tree** of which all other nodes are direct or indirect **children**, or equivalently the only node in the tree that has no **parent**.

row-major storage:

Storing each row of a two-dimensional array as one block of memory so that elements in the same column are far apart.

runnable documentation:

Statements about code that can be executed to check their correctness, such as **assertions** or **type declarations**.

sandbox:

A testing environment that is separate from the production system, or an environment that is only allowed to perform a restricted set of operations for security reasons.

SAT solver:

A library or application that determines whether there is an assignment of true and false to a set of **Boolean** variables that makes an expression true (i.e., that satisfies the expression).

schema:

A specification of the format of a dataset, including the name, format, and content of each **table**.

scope:

The portion of a program within which a definition can be seen and used.

scope creep:

Slow but steady increase in a project's goals after the project starts.

scoring function:

A function that measures or estimates how good a solution to a problem is.

search path:

The list of directories that a program searches to find something. For example, the Unix **shell** uses the search path stored in the PATH variable when trying to find a program whose name it has been given.

seed:

A value used to initialize a **pseudo-random number generator**.

semantic versioning:

A standard for identifying software releases. In the version identifier major.minor.patch, major changes when a new version of software is incompatible with old versions, minor changes when new features are added to an existing version, and patch changes when small **bugs** are fixed.

server:

Typically, a program such as a database manager or web server that provides data to a **client** upon request.

SHA-1 hash:

A **cryptographic hash function** that produces a 160-bit output.

shell:

A **command-line interface** that allows a user to interact with the **operating system**, such as Bash (for Unix and MacOS) or PowerShell (for Windows).

shell variable:

A variable set and used in the **Unix shell**. Commonly-used shell variables include HOME (the user's home directory) and PATH (their **search path**).

side effect:

A change made by a function while it runs that is visible after the function finishes, such as modifying a **global variable** or writing to a file. Side effects make programs harder for people to understand, since the effects are not necessarily clear at the point in the program where the function is called.

signature:

The set of parameters (with types or meaning) that characterize the calling interface of a function or set of functions. Two functions with the same signature can be called interchangeably.

single-threaded:

A model of program execution in which only one thing can happen at a time. Single-threaded execution is easier for people to understand, but less efficient than **multi-threaded** execution.

singleton:

A set with only one element, or a **class** with only one **instance**.

Singleton pattern:

A **design pattern** that creates a **singletonobject** to manage some resource or service, such as a database or **cache**. In **object-oriented programming**, the pattern is usually implemented by hiding the **constructor** of the **class** in some way so that it can only be called once.

slug:

An abbreviated portion of a page's URL that uniquely identifies it. In the example [https://www.mysite.com/category/post-name](https://www.mysite.com), the slug is post-name.

source map:

A table used to translate a piece of code back to the lines in the original source.

sparse matrix:

A matrix in which most of the values are zero (or some other value). Rather than storing many copies of the same values, programs will often use a special data structure that only stores the “interesting” values.

SQL:

The language used for writing queries for a **relational database**. The term was originally an acronym for Structured Query Language.

stack frame:

A section of the **call stack** that records details of a single call to a specific function.

stale (in build):

To be out-of-date compared to a **prerequisite**. A **build manager**‘s job is to find and update things that are stale.

standard error:

A predefined communication channel for a **process** typically used to report errors.

standard input:

A predefined communication channel for a **process**, typically used to read input from the keyboard or from the previous process in a **pipe**.

standard output:

A predefined communication channel for a **process**, typically used to send output to the screen or to the next process in a **pipe**.

static site generator:

A software tool that creates HTML pages from templates and content.

stream:

A sequential flow of data, such as the **bits** arriving across a network connection or the bytes read from a file.

streaming API:

An **API** that processes data in chunks rather than needing to have all of it in memory at once. Streaming APIs usually require **handlers** for events such as “start of data”, “next block”, and “end of data”.

string:

A block of text in a program. The term is short for “character string”.

string interpolation:

The process of inserting text corresponding to specified values into a **string**, usually to make output human-readable.

synchronous:

To happen at the same time. In programming, synchronous operations are ones that have to run simultaneously, or complete at the same time.

tab completion:

A technique implemented by most **REPLs**, **shells**, and programming editors that completes a command, variable name, filename, or other text when the TAB key is pressed.

table:

A set of **records** in a **relational database** or **data frame**.

tagged data:

A technique for storing data in a two-part structure, where one part identifies the type and the other part stores the bits making up the value.

Template Method pattern:

A **design pattern** in which a **parent class** defines an overall sequence of operations by calling **abstract methods** that **child classes** must then implement. Each child class then behaves in the same general way, but implements the steps differently.

test harness:

A program written to test some other program or set of functions, typically to measure their performance.

test runner:

A program that finds and runs software tests and reports their results.

test subject:

The thing being tested, sometimes also called the system under test (SUT).

test-driven development (TDD):

A programming practice in which tests are written before a new feature is added or a **bug** is fixed in order to clarify the goal.

throw (exception):

Another term for **raising** an exception.

tightly coupled:

Components in a software system are said to be tightly coupled if they depend on each other's internals, so that if one is altered then others have to be altered as well.

Time of check/time of use (ToCToU):

A **race condition** in which a process checks the state of something and then operates on it, but some other process might alter that state between the check and the operation.

timestamp:

A digital identifier showing the time at which something was created or accessed. Timestamps should use **ISO date format** for portability.

token:

An indivisible unit of text for a parser, such as a variable name or a number. Exactly what constitutes a token depends on the language.

topological order:

Any ordering of the **nodes** in a **graph** that respects the direction of its **edges**, i.e., if there is an edge from node A to node B, A comes before B in the ordering. There may be many topological orderings of a particular graph.

transitive closure:

The set of all **nodes** in a **graph** that are reachable from a starting node, either directly or indirectly.

tree:

A **graph** in which every node except the **root** has exactly one **parent**.

tuple:

A value that has a fixed number of parts, such as the three color components of a red-green-blue color specification.

Turing Machine:

A theoretical model of computation that manipulates symbols on an infinite tape according to a fixed table of rules. Any computation that can be expressed as an algorithm can be done by a Turing Machine.

two hard problems in computer science:

Refers to a quote by Phil Karlton: “There are only two hard problems in computer science—cache invalidation and naming things.” Many variations add a third problem as a joke, such as **off-by-one errors**.

type declaration:

A statement in a program that a variable or value has a particular data type. Languages like Java require type declarations for all variables; they are optional in TypeScript and Python, and not allowed in pure JavaScript.

Unicode:

A standard that defines numeric codes for many thousands of characters and symbols. Unicode does not define how those numbers are stored; that is done by standards like **UTF-8**.

Uniform Resource Locator (URL):

A unique address on the World-Wide Web. URLs originally identified web pages, but may also represent datasets or database queries, particularly if they include a **query string**.

unit test:

A test that exercises one function or feature of a piece of software and produces **pass**, **fail**, or **error**.

UTF-8:

A way to store the numeric codes representing **Unicode** characters in memory that is **backward-compatible** with the older **ASCII** standard.

vector:

A sequence of values, usually of **homogeneous** type.

version control system:

A system for managing changes made to software during its development.

virtual machine:

A program that pretends to be a computer. This may seem a bit redundant, but VMs are quick to create and start up, and changes made inside the virtual machine are contained within that VM so we can install new **packages** or run a completely different operating system without affecting the underlying computer.

Visitor pattern:

A **design pattern** in which the operation to be done is taken to each element of a data structure in turn. It is usually implemented by having a generator “visitor” that knows how to reach the structure's elements, which is given a function or method to call for each in turn, and that carries out the specific operation.

walk (a tree):

To visit each **node** in a **tree** in some order, typically **depth-first** or **breadth-first**.

watchpoint:

An instruction for a debugger telling it to suspect execution whenever the value of a variable (or more generally an expression) changes.

well formed:

A piece of text that obeys the rules of a formal grammar is said to be well formed.

word (of memory):

The unit of memory that a particular processor most naturally works with. While a byte is a fixed size (8 bits), a word may be 16, 32, or 64 bits long depending on the processor.

XML:

A set of rules for defining **HTML**-like tags and using them to format documents (typically data). XML was popular in the early 2000s, but its complexity led many programmers to adopt **JSON**, instead.

YAML:

Short for “YAML Ain't Markup Language”, a way to represent nested data using indentation rather than the parentheses and commas of **JSON**. YAML is often used in configuration files and to define **parameters** for various flavors of **Markdown** documents.

z-buffering:

A drawing method that keeps track of the depth of what lies “under” each pixel so that it displays whatever is nearest to the observer.

# Index

*   abstract syntax tree, [191](#chapter14.xhtml_p191), [207](#chapter15.xhtml_p207), [219](#chapter16.xhtml_p219), [275](#chapter20.xhtml_p275)
*   Accumulator pattern, [228](#chapter16.xhtml_p228)
*   Acorn, [191](#chapter14.xhtml_p191), [207](#chapter15.xhtml_p207), [212](#chapter15.xhtml_p212), [219](#chapter16.xhtml_p219), [235](#chapter17.xhtml_p235), [277](#chapter20.xhtml_p277)
*   actual result (in unit test), [41](#chapter4.xhtml_p41)
*   Adapter pattern, [196](#chapter14.xhtml_p196)
*   algorithm
    *   greedy, [93](#chapter7.xhtml_p93)
*   alias
    *   during import, [185](#chapter13.xhtml_p185)
*   anonymous function, [12](#chapter2.xhtml_p12)
*   ANTLR, [107](#chapter8.xhtml_p107)
*   API, [10](#chapter2.xhtml_p10), [24](#chapter3.xhtml_p24)
*   Application Binary Interface, [261](#chapter19.xhtml_p261)
*   Armstrong, Tavish, [4](#chapter1.xhtml_p4)
*   array implementation, [270](#chapter19.xhtml_p270)
*   Array.filter, [14](#chapter2.xhtml_p14)
*   Array.forEach, [23](#chapter3.xhtml_p23)
*   Array.reduce, [135](#chapter10.xhtml_p135)
*   ArrayBuffer, [76](#chapter6.xhtml_p76)
*   assembler, [266](#chapter19.xhtml_p266)
*   assembly code, [261](#chapter19.xhtml_p261), [275](#chapter20.xhtml_p275)
*   assertion
    *   as runnable documentation, [138](#chapter10.xhtml_p138)
    *   in unit test, [41](#chapter4.xhtml_p41)
*   assignment
    *   destructuring, [16](#chapter2.xhtml_p16)
*   async keyword, [34](#chapter3.xhtml_p34)
*   asynchronous execution, [7](#chapter2.xhtml_p7)
*   automatic variable (in build), [136](#chapter10.xhtml_p136)
*   await keyword, [34](#chapter3.xhtml_p34)

*   Babel, [215](#chapter15.xhtml_p215)
*   backward compatibility, [250](#chapter18.xhtml_p250)
*   Bajel, [127](#chapter10.xhtml_p127)
*   bare object, [118](#chapter9.xhtml_p118)
*   bind method to object, [28](#chapter3.xhtml_p28)
*   bitwise operation, [264](#chapter19.xhtml_p264)
*   block comment, [221](#chapter16.xhtml_p221)
*   Brown, Amy, [4](#chapter1.xhtml_p4)
*   Brubeck, Matt, [145](#chapter11.xhtml_p145)
*   build
    *   automatic variable, [136](#chapter10.xhtml_p136)
    *   clock synchronization, [133](#chapter10.xhtml_p133)
    *   dependency, [128](#chapter10.xhtml_p128)
    *   hash code, [133](#chapter10.xhtml_p133)
    *   pattern rule, [137](#chapter10.xhtml_p137)
    *   recipe, [128](#chapter10.xhtml_p128)
    *   rule, [136](#chapter10.xhtml_p136)
    *   stale, [128](#chapter10.xhtml_p128)
    *   timestamp, [133](#chapter10.xhtml_p133)
*   build manager, [127](#chapter10.xhtml_p127)
*   build target, [128](#chapter10.xhtml_p128)

*   C, [127](#chapter10.xhtml_p127), [165](#chapter12.xhtml_p165), [191](#chapter14.xhtml_p191)
*   C++, [165](#chapter12.xhtml_p165)
*   cache
    *   calculated values, [147](#chapter11.xhtml_p147)
    *   modules, [44](#chapter4.xhtml_p44)
    *   of loaded files, [169](#chapter12.xhtml_p169), [185](#chapter13.xhtml_p185)
*   call stack
    *   environment, [113](#chapter9.xhtml_p113)
    *   stack frame, [113](#chapter9.xhtml_p113)
*   callback function, [7](#chapter2.xhtml_p7)
    *   conventions for, [10](#chapter2.xhtml_p10)
*   caller module, [45](#chapter4.xhtml_p45)
*   chain of inheritance, [203](#chapter14.xhtml_p203)
*   Chain of Responsibility pattern, [97](#chapter7.xhtml_p97)
*   character encoding, [32](#chapter3.xhtml_p32)
    *   UTF-8, [32](#chapter3.xhtml_p32)
*   circular dependency, [182](#chapter13.xhtml_p182)
*   clock synchronization (in build), [133](#chapter10.xhtml_p133)
*   closure, [179](#chapter13.xhtml_p179)
*   code
    *   as data, [12](#chapter2.xhtml_p12), [230](#chapter16.xhtml_p230)
*   code coverage, [207](#chapter15.xhtml_p207)
*   coding style
    *   importance of consistency, [191](#chapter14.xhtml_p191)
    *   linter, [191](#chapter14.xhtml_p191)
*   cognitive load, [9](#chapter2.xhtml_p9), [123](#chapter9.xhtml_p123)
*   collision (in hashing), [54](#chapter5.xhtml_p54)
*   column-major storage order, [70](#chapter6.xhtml_p70)
*   combinatorial explosion, [252](#chapter18.xhtml_p252)
*   command-line argument, [8](#chapter2.xhtml_p8)
*   comment
    *   block, [221](#chapter16.xhtml_p221)
    *   doc, [222](#chapter16.xhtml_p222)
    *   line, [221](#chapter16.xhtml_p221)
*   compiled language, [127](#chapter10.xhtml_p127)
    *   linking, [127](#chapter10.xhtml_p127)
*   Comprehensive TeX Archive Network, [249](#chapter18.xhtml_p249)
*   confirmation bias, [154](#chapter11.xhtml_p154)
*   console.log, [9](#chapter2.xhtml_p9)
*   const declaration
    *   advantages of, [9](#chapter2.xhtml_p9)
*   Cook, Mary Rose, [53](#chapter5.xhtml_p53)
*   coordinate system, [145](#chapter11.xhtml_p145)
*   coupling, [91](#chapter7.xhtml_p91)
*   cryptographic hash function, [53](#chapter5.xhtml_p53)
*   CSS, [157](#chapter11.xhtml_p157), [226](#chapter16.xhtml_p226)
    *   struggles with, [161](#chapter11.xhtml_p161)

*   DAG, [128](#chapter10.xhtml_p128)
*   data frame, [69](#chapter6.xhtml_p69)
*   DataForge, [69](#chapter6.xhtml_p69)
*   debugger, [275](#chapter20.xhtml_p275)
    *   source map, [277](#chapter20.xhtml_p277)
*   Decorator pattern, [209](#chapter15.xhtml_p209)
*   dependency (in build), [128](#chapter10.xhtml_p128)
*   depth-first search, [85](#chapter7.xhtml_p85)
*   design by contract, [156](#chapter11.xhtml_p156)
*   design pattern
    *   Accumulator, [228](#chapter16.xhtml_p228)
    *   Adapter, [196](#chapter14.xhtml_p196)
    *   Chain of Responsibility, [97](#chapter7.xhtml_p97)
    *   Decorator, [209](#chapter15.xhtml_p209)
    *   Iterator, [198](#chapter14.xhtml_p198)
    *   Singleton, [43](#chapter4.xhtml_p43), [169](#chapter12.xhtml_p169)
    *   Template Method, [130](#chapter10.xhtml_p130), [142](#chapter10.xhtml_p142)
    *   Visitor, [114](#chapter9.xhtml_p114), [129](#chapter10.xhtml_p129), [193](#chapter14.xhtml_p193)
*   destructuring assignment, [16](#chapter2.xhtml_p16)
*   DiBernardo, Mike, [4](#chapter1.xhtml_p4)
*   directed acyclic graph, [182](#chapter13.xhtml_p182)
*   directed acyclic graph (DAG), [128](#chapter10.xhtml_p128)
*   directed graph, [182](#chapter13.xhtml_p182)
*   doc comment, [222](#chapter16.xhtml_p222)
*   Document Object Model, [83](#chapter7.xhtml_p83), [191](#chapter14.xhtml_p191)
*   DOM, [83](#chapter7.xhtml_p83), [111](#chapter9.xhtml_p111)
*   dynamic loading, [46](#chapter4.xhtml_p46)
*   dynamic lookup, [196](#chapter14.xhtml_p196)
*   dynamic scoping, [113](#chapter9.xhtml_p113)

*   eager matching, [93](#chapter7.xhtml_p93)
*   EJS, [111](#chapter9.xhtml_p111)
*   encapsulation, [179](#chapter13.xhtml_p179)
*   entry point (of module), [233](#chapter17.xhtml_p233)
*   environment (to store variables), [113](#chapter9.xhtml_p113)
*   error (in unit test), [41](#chapter4.xhtml_p41)
*   Escodegen, [209](#chapter15.xhtml_p209)
*   ESDoc, [219](#chapter16.xhtml_p219)
*   ESLint, [165](#chapter12.xhtml_p165), [191](#chapter14.xhtml_p191)
*   Esprima format, [192](#chapter14.xhtml_p192)
*   eval
    *   insecurity of, [166](#chapter12.xhtml_p166)
*   event handler
    *   streaming API, [55](#chapter5.xhtml_p55)
*   event loop, [23](#chapter3.xhtml_p23)
*   exception
    *   for control flow, [287](#chapter20.xhtml_p287)
    *   handler, [42](#chapter4.xhtml_p42)
    *   in promise, [27](#chapter3.xhtml_p27)
    *   throw, [41](#chapter4.xhtml_p41)
    *   with await, [37](#chapter3.xhtml_p37)
*   execution
    *   asynchronous, [7](#chapter2.xhtml_p7)
    *   event loop, [23](#chapter3.xhtml_p23)
    *   non-blocking, [24](#chapter3.xhtml_p24)
    *   single-threaded, [9](#chapter2.xhtml_p9)
    *   streaming, [55](#chapter5.xhtml_p55)
*   Expect, [284](#chapter20.xhtml_p284)
*   expected result (in unit test), [41](#chapter4.xhtml_p41)
*   experiments, [69](#chapter6.xhtml_p69)
    *   test harness, [73](#chapter6.xhtml_p73)
*   exploratory programming, [41](#chapter4.xhtml_p41)

*   fail (in unit test), [41](#chapter4.xhtml_p41)
*   filesystem operations, [7](#chapter2.xhtml_p7)
*   finite state machine
    *   correspondence with regular expressions, [108](#chapter8.xhtml_p108)
*   fixture (in unit test), [41](#chapter4.xhtml_p41)
*   fluent interface, [27](#chapter3.xhtml_p27)
*   fs.stat, [19](#chapter2.xhtml_p19)
*   function
    *   anonymous, [12](#chapter2.xhtml_p12)
    *   inner, [179](#chapter13.xhtml_p179)
    *   nested, [213](#chapter15.xhtml_p213)
*   function signature, [152](#chapter11.xhtml_p152)

*   generator function, [198](#chapter14.xhtml_p198)
*   Git, [53](#chapter5.xhtml_p53)
*   GitHub Pages, [111](#chapter9.xhtml_p111)
*   globbing, [13](#chapter2.xhtml_p13)
    *   filtering results, [13](#chapter2.xhtml_p13)
*   greedy algorithm, [93](#chapter7.xhtml_p93)

*   hash code, [53](#chapter5.xhtml_p53)
    *   in build, [133](#chapter10.xhtml_p133)
    *   SHA-1, [54](#chapter5.xhtml_p54)
*   hash function, [53](#chapter5.xhtml_p53)
    *   collision, [54](#chapter5.xhtml_p54)
    *   cryptographic, [53](#chapter5.xhtml_p53)
*   header file
    *   in C and C++, [165](#chapter12.xhtml_p165)
    *   static site generator, [165](#chapter12.xhtml_p165)
*   helper function, [57](#chapter5.xhtml_p57), [212](#chapter15.xhtml_p212)
*   heterogeneous storage, [70](#chapter6.xhtml_p70)
*   homogeneous storage, [70](#chapter6.xhtml_p70)
*   Hoye, Mike, [145](#chapter11.xhtml_p145)
*   HTML5 specification, [112](#chapter9.xhtml_p112)
*   Huffine, Trey, [23](#chapter3.xhtml_p23)
*   Human Resource Machine, [261](#chapter19.xhtml_p261)

*   immediately-invoked function expression, [180](#chapter13.xhtml_p180), [239](#chapter17.xhtml_p239)
*   immutable data, [70](#chapter6.xhtml_p70)
*   import
    *   alias, [185](#chapter13.xhtml_p185)
*   import module, [8](#chapter2.xhtml_p8)
*   import vs. require, [8](#chapter2.xhtml_p8), [234](#chapter17.xhtml_p234)
*   inner function, [179](#chapter13.xhtml_p179)
*   instruction pointer, [261](#chapter19.xhtml_p261)
*   instruction set, [261](#chapter19.xhtml_p261)
*   interpreted language, [127](#chapter10.xhtml_p127)
*   intrinsic complexity, [196](#chapter14.xhtml_p196), [243](#chapter17.xhtml_p243)
*   introspection
    *   in unit testing, [41](#chapter4.xhtml_p41)
    *   of methods, [196](#chapter14.xhtml_p196)
*   Istanbul, [207](#chapter15.xhtml_p207)
*   Iterator pattern, [198](#chapter14.xhtml_p198)
    *   generator function, [198](#chapter14.xhtml_p198)

*   Jake, [127](#chapter10.xhtml_p127)
*   Java, [8](#chapter2.xhtml_p8), [127](#chapter10.xhtml_p127), [209](#chapter15.xhtml_p209)
*   JavaScript
    *   hurried design of, [233](#chapter17.xhtml_p233)
*   Jekyll, [111](#chapter9.xhtml_p111)
*   Jest, [41](#chapter4.xhtml_p41)
*   JSDoc, [219](#chapter16.xhtml_p219)

*   Kernighan, Brian, [83](#chapter7.xhtml_p83), [87](#chapter7.xhtml_p87)
*   Knuth, Donald, [175](#chapter12.xhtml_p175)

*   label (on address), [266](#chapter19.xhtml_p266)
*   language
    *   compiled, [127](#chapter10.xhtml_p127)
    *   interpreted, [127](#chapter10.xhtml_p127)
*   layout engine, [145](#chapter11.xhtml_p145)
*   lexical scoping, [113](#chapter9.xhtml_p113)
*   lifecycle
    *   of file interpolation, [174](#chapter12.xhtml_p174)
    *   of unit test, [47](#chapter4.xhtml_p47)
*   line comment, [221](#chapter16.xhtml_p221)
*   linking (compiled language), [127](#chapter10.xhtml_p127)
*   linter, [191](#chapter14.xhtml_p191)
*   Liskov Substitution Principle, [156](#chapter11.xhtml_p156)
*   literal (in parsing), [100](#chapter8.xhtml_p100)
*   literate programming, [175](#chapter12.xhtml_p175)

*   macro, [215](#chapter15.xhtml_p215)
*   Make, [127](#chapter10.xhtml_p127)
*   manifest (of package), [252](#chapter18.xhtml_p252)
*   Markdown, [203](#chapter14.xhtml_p203), [222](#chapter16.xhtml_p222)
    *   parser, [223](#chapter16.xhtml_p223)
*   matching
    *   eager, [93](#chapter7.xhtml_p93)
*   method chaining, [27](#chapter3.xhtml_p27)
*   Mocha, [41](#chapter4.xhtml_p41), [60](#chapter5.xhtml_p60), [87](#chapter7.xhtml_p87), [102](#chapter8.xhtml_p102), [147](#chapter11.xhtml_p147)
    *   afterEach, [62](#chapter5.xhtml_p62)
    *   beforeEach, [62](#chapter5.xhtml_p62)
*   mock object
    *   for testing, [61](#chapter5.xhtml_p61)
*   module
    *   entry point, [233](#chapter17.xhtml_p233)
*   module bundler, [233](#chapter17.xhtml_p233)
*   module loader, [165](#chapter12.xhtml_p165)
*   mutual references, [279](#chapter20.xhtml_p279)

*   namespace, [179](#chapter13.xhtml_p179)
*   nested function, [213](#chapter15.xhtml_p213)
*   Nison, Maël, [249](#chapter18.xhtml_p249)
*   node, [83](#chapter7.xhtml_p83)
*   non-blocking execution, [24](#chapter3.xhtml_p24)
*   Nystrom, Bob, [261](#chapter19.xhtml_p261)

*   op code, [261](#chapter19.xhtml_p261)
*   Open-Closed Principle, [97](#chapter7.xhtml_p97)
*   operator precedence
    *   implementing, [107](#chapter8.xhtml_p107)
*   Oram, Andy, [4](#chapter1.xhtml_p4)

*   package manifest, [252](#chapter18.xhtml_p252)
*   Pandas, [69](#chapter6.xhtml_p69)
*   parser, [99](#chapter8.xhtml_p99)
    *   check-and-combine, [104](#chapter8.xhtml_p104)
    *   post-hoc compression strategy, [104](#chapter8.xhtml_p104)
    *   reasons not to write, [99](#chapter8.xhtml_p99)
    *   shunting-yard algorithm, [107](#chapter8.xhtml_p107)
*   pass (in unit test), [41](#chapter4.xhtml_p41)
*   patch number, [249](#chapter18.xhtml_p249)
*   pattern rule (in build), [137](#chapter10.xhtml_p137)
*   PHP, [111](#chapter9.xhtml_p111)
*   plugin architecture, [182](#chapter13.xhtml_p182)
*   polymorphism (in software design), [91](#chapter7.xhtml_p91)
*   process.argv, [8](#chapter2.xhtml_p8)
*   programming style
    *   fluent interface, [27](#chapter3.xhtml_p27)
*   promise
    *   as alternative to callback, [23](#chapter3.xhtml_p23)
    *   automatic creation of, [35](#chapter3.xhtml_p35)
    *   behavior, [26](#chapter3.xhtml_p26)
    *   catch, [27](#chapter3.xhtml_p27)
    *   reject, [26](#chapter3.xhtml_p26)
    *   resolve, [26](#chapter3.xhtml_p26)
    *   then, [27](#chapter3.xhtml_p27)
*   Promise.all, [32](#chapter3.xhtml_p32)
*   protocol
    *   API as, [10](#chapter2.xhtml_p10), [24](#chapter3.xhtml_p24)
    *   for unit testing, [62](#chapter5.xhtml_p62)
*   prune (a search tree), [254](#chapter18.xhtml_p254)
*   Python, [8](#chapter2.xhtml_p8), [69](#chapter6.xhtml_p69), [183](#chapter13.xhtml_p183), [209](#chapter15.xhtml_p209)

*   query selector, [159](#chapter11.xhtml_p159)
*   query selector (for HTML), [83](#chapter7.xhtml_p83)

*   R, [69](#chapter6.xhtml_p69)
*   race condition, [59](#chapter5.xhtml_p59)
    *   time of check/time of use, [59](#chapter5.xhtml_p59)
*   recipe (in build), [128](#chapter10.xhtml_p128)
*   recycling data, [71](#chapter6.xhtml_p71)
*   register (in computer), [261](#chapter19.xhtml_p261)
*   regular expression, [83](#chapter7.xhtml_p83)
*   reject promise, [26](#chapter3.xhtml_p26)
*   require
    *   caching modules, [44](#chapter4.xhtml_p44)
*   require vs. import, [8](#chapter2.xhtml_p8), [234](#chapter17.xhtml_p234)
*   resolve promise, [26](#chapter3.xhtml_p26)
*   row-major storage order, [70](#chapter6.xhtml_p70)
*   rule (in build), [136](#chapter10.xhtml_p136)
*   runnable documentation (assertions as), [138](#chapter10.xhtml_p138)

*   sandbox (for safe execution), [166](#chapter12.xhtml_p166)
*   SAT solver, [249](#chapter18.xhtml_p249), [257](#chapter18.xhtml_p257)
*   satisfiability, [249](#chapter18.xhtml_p249)
*   scope
    *   of variable definitions, [17](#chapter2.xhtml_p17)
*   scope creep
    *   when writing lessons, [87](#chapter7.xhtml_p87)
*   scoping
    *   dynamic, [113](#chapter9.xhtml_p113)
    *   lexical, [113](#chapter9.xhtml_p113)
*   search
    *   depth-first, [85](#chapter7.xhtml_p85)
*   search path, [171](#chapter12.xhtml_p171)
    *   shell variable, [172](#chapter12.xhtml_p172)
*   semantic versioning, [249](#chapter18.xhtml_p249)
    *   patch number, [249](#chapter18.xhtml_p249)
*   setImmediate, [25](#chapter3.xhtml_p25)
*   setTimeout, [24](#chapter3.xhtml_p24)
*   SHA-1 hash code, [54](#chapter5.xhtml_p54)
*   shell variable (for storing search path), [172](#chapter12.xhtml_p172)
*   shunting-yard algorithm, [107](#chapter8.xhtml_p107)
*   side effect
    *   for module registration, [46](#chapter4.xhtml_p46)
*   signature
    *   of function, [152](#chapter11.xhtml_p152)
*   sin
    *   using regular expressions to parse HTML, [108](#chapter8.xhtml_p108)
*   single-threaded execution, [9](#chapter2.xhtml_p9)
*   Singleton pattern, [43](#chapter4.xhtml_p43), [169](#chapter12.xhtml_p169)
*   slug (unique identifier), [225](#chapter16.xhtml_p225)
*   software design
    *   bare object, [118](#chapter9.xhtml_p118)
    *   coupling, [91](#chapter7.xhtml_p91)
    *   deferring problems, [278](#chapter20.xhtml_p278)
    *   design by contract, [156](#chapter11.xhtml_p156)
    *   driver, [129](#chapter10.xhtml_p129)
    *   encapsulation, [179](#chapter13.xhtml_p179)
    *   generic function, [195](#chapter14.xhtml_p195)
    *   Liskov Substitution Principle, [156](#chapter11.xhtml_p156)
    *   Open-Closed Principle, [97](#chapter7.xhtml_p97)
    *   plugin architecture, [182](#chapter13.xhtml_p182)
    *   polymorphism, [91](#chapter7.xhtml_p91)
    *   testability, [65](#chapter5.xhtml_p65)
*   source map, [277](#chapter20.xhtml_p277)
*   spread
    *   function arguments, [207](#chapter15.xhtml_p207)
*   SQL, [69](#chapter6.xhtml_p69)
*   stack frame, [113](#chapter9.xhtml_p113)
*   stale (in build), [128](#chapter10.xhtml_p128)
*   Standard JS, [191](#chapter14.xhtml_p191)
*   static site generator, [111](#chapter9.xhtml_p111)
    *   header file, [165](#chapter12.xhtml_p165)
*   storage
    *   heterogeneous, [70](#chapter6.xhtml_p70)
    *   homogeneous, [70](#chapter6.xhtml_p70)
*   storage order
    *   column-major, [70](#chapter6.xhtml_p70)
    *   row-major, [70](#chapter6.xhtml_p70)
*   streaming API, [55](#chapter5.xhtml_p55)
    *   event handler, [55](#chapter5.xhtml_p55)
*   string interpolation, [15](#chapter2.xhtml_p15)

*   tagged data structure, [76](#chapter6.xhtml_p76)
*   target
    *   build, [128](#chapter10.xhtml_p128)
*   TDD, [87](#chapter7.xhtml_p87)
*   Template Method pattern, [130](#chapter10.xhtml_p130), [142](#chapter10.xhtml_p142)
*   test harness, [73](#chapter6.xhtml_p73)
*   test runner, [47](#chapter4.xhtml_p47)
*   test subject (in unit test), [41](#chapter4.xhtml_p41)
*   test-driven development, [87](#chapter7.xhtml_p87)
*   testability
    *   as design criterion, [65](#chapter5.xhtml_p65)
*   tidyverse, [69](#chapter6.xhtml_p69)
*   time of check/time of use, [59](#chapter5.xhtml_p59)
*   timestamp
    *   in build, [133](#chapter10.xhtml_p133)
*   token (in parsing), [100](#chapter8.xhtml_p100)
*   topological order, [128](#chapter10.xhtml_p128)
*   transitive closure, [236](#chapter17.xhtml_p236), [251](#chapter18.xhtml_p251)
*   Turing Machine, [108](#chapter8.xhtml_p108)
*   two hard problems in computer science, [213](#chapter15.xhtml_p213)

*   unit test
    *   actual result, [41](#chapter4.xhtml_p41)
    *   error, [41](#chapter4.xhtml_p41)
    *   expected result, [41](#chapter4.xhtml_p41)
    *   fail, [41](#chapter4.xhtml_p41)
    *   fixture, [41](#chapter4.xhtml_p41)
    *   interactive application, [283](#chapter20.xhtml_p283)
    *   lifecycle, [47](#chapter4.xhtml_p47)
    *   pass, [41](#chapter4.xhtml_p41)
    *   requirements for, [41](#chapter4.xhtml_p41)
    *   test runner, [47](#chapter4.xhtml_p47)
    *   test subject, [41](#chapter4.xhtml_p41)
    *   using mock object, [61](#chapter5.xhtml_p61)
*   University of Toronto, [3](#chapter1.xhtml_p3)
*   UTF-8, [32](#chapter3.xhtml_p32)

*   variable definition
    *   scope, [17](#chapter2.xhtml_p17)
*   version control system, [53](#chapter5.xhtml_p53)
    *   Git, [53](#chapter5.xhtml_p53)
*   virtual machine, [261](#chapter19.xhtml_p261), [276](#chapter20.xhtml_p276)
    *   op code, [261](#chapter19.xhtml_p261)
*   Visitor pattern, [114](#chapter9.xhtml_p114), [129](#chapter10.xhtml_p129), [193](#chapter14.xhtml_p193)

*   walk a tree, [193](#chapter14.xhtml_p193)
*   Whitehead, Alfred North, [231](#chapter16.xhtml_p231)
*   Wilson, Greg, [3](#chapter1.xhtml_p3)
*   Wolfram Alpha, [54](#chapter5.xhtml_p54)