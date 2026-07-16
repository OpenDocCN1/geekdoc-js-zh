![](cover.jpeg)

PowerShell

Become A Master In PowerShell

h

Written by

Richard Dorsey

t

Table of Contents

h

[Introduction](#part0003.html_Book)

[Chapter 1: What is PowerShell?](#part0004.html_Book)

[Chapter 2: PowerShell Commands](#part0005.html_Book)

[Chapter 3: The Programming Logic behind PowerShell](#part0006.html_Book)

[Chapter 4: Scripting](#part0007.html_Book)

[Chapter 5: More Advanced - Filtering and Formatting](#part0008.html_Book)

[Chapter 6: PowerShell Terminology](#part0009.html_Book)

[Conclusion](#part0010.html_Book)

© Copyright 2017 by Richard Dorsey - All rights reserved.

The follow book is reproduced below with the goal of providing information that is as accurate and reliable as possible. Regardless, purchasing this book can be seen as consent to the fact that both the publisher and the author of this book are in no way experts on the topics discussed within and that any recommendations or suggestions that are made herein are for entertainment purposes only. Professionals should be consulted as needed prior to undertaking any of the action endorsed herein.

This declaration is deemed fair and valid by both the American Bar Association and the Committee of Publishers Association and is legally binding throughout the United States.

Furthermore, the transmission, duplication or reproduction of any of the following work including specific information will be considered an illegal act irrespective of if it is done electronically or in print. This extends to creating a secondary or tertiary copy of the work or a recorded copy and is only allowed with express written consent from the Publisher. All additional right reserved.

The information in the following pages is broadly considered to be a truthful and accurate account of facts and as such any inattention, use or misuse of the information in question by the reader will render any resulting actions solely under their purview. There are no scenarios in which the publisher or the original author of this work can be in any fashion deemed liable for any hardship or damages that may befall them after undertaking information described herein.

Additionally, the information in the following pages is intended only for informational purposes and should thus be thought of as universal. As befitting its nature, it is presented without assurance regarding its prolonged validity or interim quality. Trademarks that are mentioned are done without written consent and can in no way be considered an endorsement from the trademark holder.

Introduction

h

Congratulations on downloading PowerShell and thank you for doing so.

The following chapters will discuss the setup and use of PowerShell on your computer. More than that, it will tell you exactly what PowerShell is and the multitude of ways that it can be used.

There are plenty of books on this subject on the market, thanks again for choosing this one! Every effort was made to ensure it is full of as much useful information as possible, please enjoy!

Chapter 1

h

What is PowerShell?

So at this point, you’ve bought the book and you’re wanting to dig into its contents and start working with the super powerful PowerShell. However, there are some essential questions that we have to topic first before we even think about digging into the meatiest parts of the content like that.

For example, I’m not exactly certain what your reasoning for picking up this book was. Maybe you’re just genuinely curious about what PowerShell is and about all of the things that you can do it with it. Maybe you’ve heard about it through work or school and are needing ample opportunity to get ahead working with this application. Moreover, maybe you’re just a hobbyist who read about PowerShell in a tutorial or on a forum and you’re looking for a proper opportunity to start working with this incredibly dynamic tool. Well, this book is going to teach you to do exactly that. However, before we get started on the hows, we really need to spend some time looking at the whats.

So what is the PowerShell? In essence, the PowerShell is a tool built by Microsoft intended to allow people to handle their configurations and automate tasks through a command line and some programming knowledge. Recently, the PowerShell was also made available for other operating systems.

PowerShell also contains a built-in scripting language. This scripting language is what allows you to build small programs in order to automate different things on your computer. This ability to script is what gives PowerShell a lot of its famous functionality and makes it a perfect choice for all of the automatic tasks that you’ll need to perform.

I suppose that, to this point, I haven’t quite made clear what PowerShell is. I’ll jump on that now. See, in every single version of Windows that’s been released, there has been a way for the user to interface directly with the tool by way of a command line. These methods of interface are referred to specifically as shells. By use of the shell, you can feed commands directly into the computer, which will allow you to do certain things rather easily or with an unprecedented level of control that you hadn’t had before. Traditional shells have a scripting language known as batch, common across most command line interfaces, whether it be Windows, Linux, or Mac. Batch files are rudimentary scripts that can be run in order to automatically do certain tasks from the command line that are written out ahead of time.

For all intents and purposes, though, batch is incredibly simple. Stupidly simple, even. Because of this, Batch doesn’t allow the generation of scripts that can do much beyond execute commands and follow very, very basic logic.

Microsoft’s first attempt to ameliorate the situation regarding scripting and command line shells came in 1998 when they put forward the Windows Script Host alongside the operating system Windows 98.This allowed, through its compatibility with Active Script, for scripts to be written in languages such as VBScript. This meant a huge step forward in terms of programming the command line and automating certain tasks. Regardless of the major step, though, the system still was far from apt; for example, it was not built into the command line shell. To the same end, documentation regarding it was very difficult to find, meaning that people who wanted to use it had a hard time and that hardly anybody could become “masters”.

Worst of all, however, were the security holes that were present in it. It was incredibly easy to take advantage of the Windows Script Host in order to build and execute computer viruses wherever they really should not be. This caused the Windows Script Host to rapidly be seen as a major net loss for the system.

After the relative failure of Windows Script Host, Microsoft decided that they needed to shift gears and start working on a new way for users to manage their command line; a uniform way that would make the shell truly worthwhile. It was around this time that a shell known as Monad, or Microsoft Shell, began to take place. The ideas started to be published as early as the summer of 2002.

Monad was fantastic, because it was something completely different. What Monad brought to the table was a command line that was extremely extensible - that is, you can add on to it with ease and make it perform whatever tasks you need to - that was, well, full-featured in a certain sense. What I mean by full-featured was that Monad promised the ability to perform a huge number of different administrative duties. What this meant for the end user was that they’d finally be able to unleash the full potential of their computer without any problem whatsoever, as they entered in commands and executed scripts.

The first public release of Monad happened in the summer of 2005 and was updated quite a bit throughout the year following. In 2006, Microsoft came out and said that Monad would instead be called Windows PowerShell. This was a huge boost for the project in terms of credibility as it positioned it to be a major tool for systems management and information tech jobs in general. PowerShell intimated something much bigger than Monad did - PowerShell intimated strength.

The first version of PowerShell was formally released in the first quarter of 2007\. While work on the first version of PowerShell was ongoing, work on PowerShell version 2.0 started to take place as well. PowerShell version 2.0 was released formally in the summer of 2009 alongside Windows 7, which it became a major part of. A little bit after its initial release, versions compatible with earlier forms of Windows were released.

Since 2009, the biggest step forward for PowerShell was when it became open source and ported to multiple different platforms. In the summer of 2016, PowerShell’s code was released to the world for all to see and users of other operating systems like Linux, CentOS, and macOS were finally able to take full advantage of the clever shell program.

So at this point, you may be asking what makes PowerShell different. Well, there are a whole lot of things, basically.

The first and foremost is that it is heavily integrated with the .NET Framework. In case you don’t know what Microsoft .NET is, it offers an infrastructure for languages to work with one another and is essentially one of Microsoft’s most important offerings right now. So how does this integrate with PowerShell? Well, one can write cmdlets - programs written using .NET Framework languages - that are actually made to work with PowerShell. However, cmdlets also work in a different way. They can also be run from PowerShell. Therefore, not only can you write Cmdlets in .NET languages, but whenever you use the PowerShell and execute certain commands in PowerShell in order to do different things, you are actually invoking Cmdlets that are set up at runtime, as well. Beyond this, every single object created in PowerShell is a .NET object, which means it will work as .NET objects do, with every method and class attribute thereof.

Another way that it’s different is that the PowerShell implements the notion of a pipeline. If you’ve ever worked with Unix pipelines then you probably have a moderate idea of how this works. Essentially, what happens is that the result of one cmdlet is given as an argument (or input data) to another cmdlet.

Perhaps the final thing that sets PowerShell apart and makes it a fantastic tool is the extremely verbose scripting language. Using the scripting language, you can automate a huge number of different things. The scripting language, too, is actually relatively full-featured compared to scripts written in languages such as Batch. For example, it supports general control flow like looping and conditionals (more on this later), allows one to catch and throw exceptions, and is entirely integrated with the .NET framework.

Having a proper knowledge of PowerShell is becoming more and more important for people working in information technology now that Windows Server 10 increasingly utilizes and integrates it. The good thing about PowerShell is that PowerShell comes automatically with Windows, so you don’t need to set it up too much. However, if you do have another operating system then, as I’ve already said, PowerShell is open source and will more than likely be available for the operating system that you’re using.

Chapter 2

h

PowerShell Commands

As I’ve said before, one of the most charming things about PowerShell is its system of cmdlets. Indeed, this system is one of the most important and integral things about it. The entire reason for using a command line shell is so that you can speak directly to the computer, server, router, or whatever and potentially do things that you couldn’t do otherwise. The command line simply serves as the most direct line of communication between you and your computer or hardware without the layer of abstraction provided by the desktop. With this higher degree of control, however, also comes a far higher learning curve. Fortunately, though, PowerShell keeps this from being all too difficult. Before we jump into this, I feel that it’s necessary that I explain briefly how command lines even work.

Commands in PowerShell have two forms. There are cmdlets and there are aliases. Aliases will perform the action of the cmdlet for which they are an alias, so don’t worry about the difference too much. The reason the aliases exist is in order to make the shell easier to use for people who are used to other sorts of shells like the Unix Shell or like the old Windows command line. The handy thing about cmdlets is that while other shell commands tend to have rather archaic or hard to understand names, cmdlet names follow a very strict order that serves to make them very readable.

Anyhow, now I’m going to go through the major cmdlets and their aliases one by one, explaining each. However, note that since cmdlets can be created and since the PowerShell is a huge program with a huge integration with .NET, there are hundreds of different cmdlets. It simply wouldn’t be practical to go through each and every one of them in this book when you quite simply aren’t going to need all of them. What I’m going to do instead is simply give you those which are most pertinent and which you’ll most likely need.

Get-ChildItem - This one can also be entered as gci, dir, or ls. The name might sound a little weird, but if you’ve ever used other shells, you know exactly what this command does. What it does is look to see where you are in the hard drive and lists every single file and directory within that folder.

Test-Connection - This one is known on other systems as ping, but doesn’t have an alias in PowerShell curiously. What it does is contact another machine and tries to get a response back. This will help you to determine whether there is a connection established between the two, either by the internet or otherwise. This is a very useful cmdlet to know how to use.

Get-Content - This one is known on other systems as gc, type, and cat, and these same aliases may be entered for it with no problem. What this does is simply get the content of a file for something to be done with it.

Get-Command - If you want to see all of the commands that are available for you to use, you simply use this cmdlet (or its alias, gcm). Upon entering this cmdlet into PowerShell, you’ll be greeted with an incredibly long list of different commands, each of which performs a different, unique, and powerful function that will help you get your work done. If you have the time and the patience, I urge you to use Get-Command and poke around and see what all you can do with it.

Get-Help - This is an extremely useful command. On the old Windows command line, it is known as help, and on the Unix shell it is known as apropos and man; help and man are the two aliases that may be used for it within PowerShell if yodu do not wish to type Get-Help. What this command does is, well, exactly what it says - it gives you help with a specified command. All that you have to do is state which cmdlet you’re wanting help and details on after the name, like so:

                                Get-Help Get-Command

However, you can also simply type Get-Help if you want some help understanding the other ways in which you can use the command. It’s actually rather versatile and so I encourage you to get to know the different ways that it can be used.

Clear-Host - This command is known also as cls on Windows and clear on Unix systems like Linux and Mac, and may be entered as either if you do not wish to type out Clear-Host completely. This command just clears the console and gives you a blank canvas.

Copy-Item - This command is as straightforward as the name implies. On the Windows command line, this command was known as copy, and on Unix shells it was known as cp. Both of these terms may be used as an alias, and so may the term cpi. This command allows you to designate a file or directory, as well as a target location. Upon using the command, the file or directory will be copied over to the target location. This can be extremely useful for, for example, making backups of important files.

Move-Item - This command is known on Windows command lines as move and on Unix shells as mv. The command is functionally similar to the copy command. However, instead of leaving the current files and directory behind and making a carbon copy of it, it instead will move them entirely and they will no longer be at the current location.

Remove-Item - This command has a huge number of names, so let me delegate through those which can be used. On the old Windows command line, this command was known as del, erase, rmdir, and rd. On Unix shells, the command is known as rmdir and rm. The aliases for this command are all of the aforementioned, as well as one more: ri. So, you can invoke this command was del, erase, rmdir, rd, rm, and ri. In case you’ve never been told before, you need to be incredibly careful with this command, as it is very, very powerful. If you aren’t careful with it, you could accidentally do something like systematically delete your entire hard drive, and doing that isn’t fun. Play it safe with this command and, honestly, as you get to know it, I would practice with a Unix shell in a virtual machine running a Linux distribution that way no real damage can be done. This command is very infamous, so I’m simply giving you fair warning now that if you aren’t careful, you can mess up big time with it.

Rename-Item - This command is extremely straightforward. It allows you to rename files or directories. It is also known by the aliases mi, ren, and mv.

Get-Location - This command is another which does pretty much exactly what it says - noticing a pattern? On the old Windows command line, this was known as cd, and on Unix shells it was known as pwd. Both of these will work as aliases, as will the term gl. All this does is list the current working directory.

Push-Location - This is a little bit more complicated. This lets you keep a running list of directories on the stack. In case you don’t know what a stack is in computer science, a stack is essentially a list of data that can be updated with new values. When you add a new value, that same value must also be the first to be taken off. So if you have the values 3, 1, and 6, and you want to add the value 8, your stack will look like this: 3, 1, 6, 8\. This will make more sense in a second, but this essentially does that while storing the location instead of some arbitrary numeric value. On Unix and Windows alike, this command has been known as pushd, and this alias is the one which PowerShell uses.

Pop-Location - This is the counterpart to the push-location cmdlet. This will change your working directory to that which was most recently added to the stack - popping that value off of the stack, if you will. So remember that: you push values on, you pop values off. This removes the directory from the stack, so if you want it to stay there, you’ll have to add it to the stack again. The command for this on Windows and Unix alike has been popd, and this is the command which PowerShell uses as well.

Set-Location - This is altogether one of the most important commands for navigating your computer by way of the command line and any sort of command line shells. I really cannot stress the importance of this command enough - it is essentially the end-all be-all of command line navigation and knowing how to properly use it is essential. What this lets you do is change location on your hard drive. You can either enter a specific location on the hard drive, like a directory address, or you can just name a directory within the directory that you’re in. (If you don’t know exactly what directories are in whatever folder you’re in, make sure that you use the Get-ChildItem cmdlet in order to to list the directories.) In Windows and Unix command lines, this command has always been known as cd. It’s also referenceable in Windows by the term chdir. Both of these terms will work as an alias for the Get-ChildItem cmdlet. However, you may also use the term sl if you so desire.

Tee-Object - This has nothing to do with golf and if you think it does then you are dumb. Rather, this command will send the given input to a file or a value, then send it along the pipeline. Sometimes - but not always - this will just mean the output stream, meaning it will be printed in your command line window. However, it may also be passed onto the next command in the pipeline, if there is another. The alias for this is simply tee, and it’s relatively new to Windows (it didn’t exist in older versions of the command line shell.)

Write-Output - This command does pretty much exactly what it sounds like it would do. It writes the given output to the output stream, generally the console window. The aliases for this term are echo, from the Windows and Unix command line shells, and write.

Get-Process - This can be relatively useful, too. You know how you can launch the Task Manager with Ctrl+Alt+Delete and see all of the processes that are currently running on your computer (and kill them if necessary)? This lists all of the processes from within PowerShell, which makes it really easy to use the command which follows this one when you need to. On Unix shells, this command was known as ps, and on Windows shells, it has been known as tasklist. Either of these will work. So will the command gps.

Stop-Process - This is the command I was referring to in the last paragraph. Let’s face it, sometimes computers are terrible. Sometimes a program completely quits working or stops working as expected, or maybe you’re trying to launch one program that connects through the internet and another is blocking the necessary port but you can’t quit it. This is where the Stop-Process command comes in handy. You will use the process name as listed in the list given by the Get-Process cmdlet. After that, the process will have been suspended and killed. In Windows and Unix command line shells alike, this has been known as kill, and this name carries over as an alias. You can also use spps as an alias.

Select-String - This will return the strings in a given file or input stream (if you don’t know what strings are, you’ll find out next chapter) to the pipeline, normally to the output stream. It will return the entire line that a string is on, so if I did a Select-String for pack over a file with a bunch of random words in it, it would return not only pack but also backpack, unpack, repack, and so forth. The only alias for this cmdlet is sls.

Set-Variable - This command will allow you to create variables or change their value. (More on this in the next chapter.) The aliases are simply sv and set.

Get-Member - This is a super important command that will allow you to see the methods and values within a given object. This may not make sense right now but it will. Remember this one, you will need it.

Invoke-WebRequest - This one will pull data from the internet and send it to the pipeline. On Unix shells, this command has historically been known as wget and curl. On older Windows command line shells, the command never actually existed. The aliases for this one are curl, wget, and iwr.

Of course, this is nowhere near all of the cmdlets. These are just the most pertinent and important ones for what you’ll most likely be doing starting out.

As I said before, if you want a far more complete list, you can also use the get-command cmdlet in order to get a full list and get-help for any that you don’t entirely understand.

However, those are just the basics. We haven’t even started talking about functions yet.

Functions are very simply things which are carried out and actions which are performed. Generally, within PowerShell, functions will give a value back - however, this isn’t always the case, sometimes they will simply print a value to the shell or they will just do something like file system operations.

While cmdlets are the core of PowerShell, functions are equally important to understand and will make up a big part of your PowerShell experience.

Let’s talk a bit more, now, about how the general logic of programming and computer science works its way into PowerShell, starting in the next chapter.

Chapter 3

h

The Programming Logic behind PowerShell

As I’ve said before, one of the bigger draws of PowerShell is that it has a very full-featured scripting language accompanying it. When I say full-featured, I mean that in many ways this language is as powerful as other major scripting languages like Python and Lua.

The reason that it can be so full-featured and powerful is because it’s tightly integrated with things like .NET, sure. I’m sure you could have told me that. But that does leave another question open - what exactly does that mean?

Everything in PowerShell is an object, a .NET object to be exact. What an object means is that it’s a derivative of a class or, sometimes, a namespace. So what does this mean in practical terms?

A class, in terms of programming, is a way of grouping different attributes together (this may not make sense yet) so that you can always generate something with the same attributes. For example, every car has a certain number of doors, a certain kind of motor, and a certain top speed. A class allows you to group these intrinsic qualities and have every instance of the car object bear them, albeit in their own unique way.

All cars can also go. The act of going would be the equivalent of a function. A function is something which performs an action and may or may not return a value, too. PowerShell is as dependent upon functions as it is upon cmdlets, and every cmdlet is just an object that has functions affixed to it.

You can also make custom objects with their own values and methods.

So why is this important? Because these methods are what will allow you to do a lot more advanced things in PowerShell than you’d realized. They’ll allow you to manipulate data, to learn all sorts of things about the different cmdlets and objects you’re working on. This is really important.

The thing you need to understand most here is that any object is the things that define it. Every single property and function defined for an object is an intrinsic part of what makes that object that object. For example, a car has a lot of intrinsic properties, as we discussed. In order for it to be one car and not another, these properties must be a certain way. This may not make much sense, but let me say it this way: let’s say that you had a silver 2004 Pontiac Grand Am with 150,000 miles. If you change one of these properties, suddenly you’re not referring to the same car. This is because every single car has intrinsic properties as such. Every car has a color; every car has a production year; every car has a make and model; and every car has a certain amount of miles on it. (Even if that amount of miles is 0.)

So if we were talking about this car but instead referred to a red 2004 Pontiac Grand Am with 150,000 miles, then we’d be talking about a different car entirely - the red one and not the silver one. Despite the fact that literally everything else is the same, that one intrinsic property of the object defines it as its own object.

As such, it’s important that you understand exactly what these properties mean and how to get to them. We’ll talk about that in just a little bit. For now, we need to move on to the scripting aspect of PowerShell, where things get automated.

Chapter 4

h

Scripting

So we’ve talked about how one can write scripts for PowerShell and the various things that they can do. This is where we’re going to get into a lot of the logic behind programming types.

Now, since the PowerShell is built on the .NET Framework, it is essentially a programming language in many ways. This means that certain things that we associate with programming languages - data types, values, variables, even program logic - can be understood in much the same way that they can with other programming languages.

To you, as a (presumably) new programmer and person who is (presumably) new to PowerShell, this may not mean too much. It may not make any sense at all, actually. But that’s okay - it will in just a moment. We just have to carry on with this topic a bit and start at the very basics.

The first thing that we need to talk about is why creating script files is necessary. By creating script files, you allow yourself to automate a number of things that you wouldn’t be able to otherwise. You also allow things to execute differently than they would by simply opening PowerShell and then typing in the commands.

This makes it slightly different from batch files. For example, in batch files on typical command line shells, you would simply type the commands that you would otherwise. Sure, there were certain keywords like GOTO or things of that nature that could make a batch file do a bit more, but they weren’t necessarily sophisticated by any particular stretch of the imagination, especially not compared to something as large as the PowerShell scripting language.

Now, don’t get me wrong, the PowerShell scripting language isn’t particularly sophisticated itself - well, it is, and it’s more than sufficient for most of what you’ll need to do. However, it is not nearly as large as some other languages. VBScript, for example, has a couple hundred different keywords that you can choose to use. Compare this to PowerShell, which has about 24. That’s a pretty marked difference.

However, don’t be confused. That reduction in keywords doesn’t make it any less powerful at all, and the language will be more than enough for every single thing that you need to do regarding the command line and any sort of automation. After all, the command line does things for you that you would otherwise have to put a lot of code into - retrieving content from a webpage, for example, is as simple as using the curl command in PowerShell.

Anyway, the key point here is that PowerShell is extremely powerful, though it’s small. Learning to harness the power of PowerShell is key to doing everything that you’re wanting to do from the command line.

So how exactly does one create and run these PowerShell scripts? Well, it’s relatively simple, actually. All that you do is start a file in any given text editor, put your code inside of it, and then name it what you want. The only catch is that the filename extension has to be ps1. So if you had a file called “cabbages” and you wanted it to be a script, you would called it cabbages.ps1. Easy peasy.

You can use any text editor that you’d like, really. Even Notepad would work just fine. Personally, I feel I must recommend Atom.io, because it’s just a really strong text editor. There are a lot of reasons to use it. The first is that it’s completely free. The second is that it’s extensible - there are a lot of addons for it that you can get, very easily, to make your life and your programming easier. The third is that it just looks really nice given that it’s free, and it works tremendously well. I couldn’t leave a more glowing review of Atom if I tried. However, if you are so inclined, you can even use something like Emacs, Vim, Notepad++, or Sublime Text. Whatever tickles your fancy, so long as it can generate plaintext files.

Now we need to talk about actual program logic. I guess that the easiest way to get into this whole thing is to start by making our first program. Get your text editor. Next, write the following within it:

Write-Output “Hello world”

Then save it as hello.ps1, wherever you would like for it to be saved. Next, you can either go to that location, right-click it, and choose “Run with PowerShell”, or you can do something more complicated (but which is far better practice and gives much better results, too.)

Open your start menu and in the search bar, type PowerShell ISE. Right-click the version which says PowerShell ISE (x86). Then click Run as Administrator. From there, you’re going to see a bigger version of the normal PowerShell open, with more options and a side panel full of pertinent information. What you’re going to want to do is type the following:

Set-ExecutionPolicy RemoteSigned

And then press Enter. What this will do is make it so that your user account on your computer is authorized to execute PowerShell scripts. Then what you’re going to do is navigate to wherever you saved the script. As I said earlier, “cd” and “ls” are your friends here. If you need to go up in directories, you’ll type “cd ..”, which will take you up one level. If you need to know which folders are in the current directory, you use “ls”, which will list them all. Keep poking around until you find your file “hello.ps1”.

Once you’ve found it, what you need to type to execute it is this:

.\hello.ps1

And then press Enter. You should see a little white-on-blue hello world pop up in the box. How exciting is that? Your first PowerShell script!

So now we need to get to talking about slightly more complicated concepts, such as values and variables.

So what are values? We’ve talked a lot about values but what exactly do they mean? Well, I haven’t quite referred to values by their actual names. When I’ve referred to values before in this book, I’ve been referring to variables or properties, depending upon context. We’ll talk about those in a second but the first thing that we really need to talk about in terms of writing a script is what a value is.

A value, I’m sure you know, is a piece of data in one way or another. For example, we talk about value all the time when we ask for the value of a house or a car. In terms of computer programming, a value refers simply to a piece of data that stands on its own. Values can be of multiple different types and sorts depending upon what they are.

For reference, here are the primary different types of values in PowerShell scripting:

| Name | Description |
| Array | A set of different values put together |
| Bool | A type of data which is either true or false |
| DateTime | A type of data which stores information regarding the date and the time. |
| Float | A type of data which stores a decimal number, known in computer science as a floating point number. |
| Guid | A type of data which stores a globally unique ID. |
| HashTable | Much like a dictionary, if you’ve done any sort of Python or Java programming. It’s a table of keys which connect to values. They connect in a somewhat intrinsic way - every key links to one specific value. |
| Int | Integers - essentially, whole numbers. |
| PsObject | A custom PowerShell object. |
| Regex | This stores a regular expression. |
| ScriptBlock | This type of data holds a script within it. |
| String | A type of data which consists of several text characters joined together, like “Hello” or “How are you today?” |

Every single thing that holds a value in programming has a certain data type, as such.

Values are stored within things called variables. Variables are things that allow you to keep and change values as you wish, without losing them. This way, you don’t have to type the same thing over and over, or you don’t have to do all of the math within your program by hand.

In the olden days, you used to have to explicitly say what type of data every value was. For example, in the programming language C, you’d have to type the type of the variable every single time that you created one, and you’d also have to give types to the functions. (More on functions, or “methods”, in a second)

However, when you’re scripting with modern languages like PowerShell, that’s no longer necessary. Some languages intentionally keep the functionality, but most modern ones do not. The separation between the two is known as implicit vs. explicit typing.

Anyway, when you decide you want to store a value, you need to do what’s called declaring a variable.

In PowerShell, this is somewhat similar to declaring variables in Perl, but it’s a lot less of a pain, too. In order to declare a variable of any type in PowerShell, all that you do is put a dollar sign ($), then the name of the variable - which can technically be anything and even have spaces so long as it has brackets around it, but best practice dictates not to do that - and then finally the value of the variable, like so.

$name = ‘Joseph’

By doing this, we just created a variable of the data type string, which means that it’s a sequence of characters. Inside of this variable, we are storing the value of the string of characters which reads “Joseph”. We can now incorporate this into our other code. Create a new file, name it whatever you like, and type the following:

$name = ‘Joseph’

Write-Output “Your name is $name?”

Then save it and try to run it. It should say “Your name is Joseph?”. That’s the first example of us using and manipulating a variable within a PowerShell script. There will be many more, but this is the first major and noteworthy one, and you should be proud.

Right now, it’s important that we draw a distinction. If you’re printing out strings, it’s best that you use single quotes around it, unless you’re printing out a variable within it, in which case you should use double quotes. Again, this is just convention and best practice.

Anyhow, what we’re going to do now is work with some other data types. Go ahead and create two variables called $varOne and $varTwo. Assign the values of 3 and 5 to these respectively.

$varOne = 3

$varTwo = 5

Now create another variable called varThree, which is going to take the value of $varOne and $varTwo.

$varThree = $varOne + $varTwo

Now type the following:

Write-Output “$varOne + $varTwo = $varThree”.

Ideally, it should print out 3 + 5 = 8, which is not only charming but mathematically correct. How cool is that?

Math in PowerShell scripting is much like math in other programming languages. Here are the signs and their individual meanings:

| + | Addition | 4 + 2 (=6) |
| - | Subtraction | 4 - 2 (=2) |
| * | Multiplication | 4 * 2 (=8) |
| / | Division | 4 / 2 (=2) |
| - (before) | Negative number | -4 + 2 (= -2) |
| % | Modulo (gives remainder) | 4 % 2 (= 0, no remainder) |

Those are the essential PowerShell math operators. It’s absolutely imperative that you understand these because math is going to be a huge component of the vast majority of the scripts that you write. Even if they’re just doing something simple like culling results or something along those lines, you’re still going to need math because you’ll have to, for example, loop through a sequence.

Now it’s time that we move onto something a tad bit more fun: control flow. Control flow is a super important part of any given program, but it’ll be especially important to your scripts. There are two major parts to control flow: conditionals, and loops. Both of them rely upon the idea that you can compare data sets against one another and determine if something is true or not, so before we jump into all of that, we’re going to talk about booleans for just a moment.

The idea of boolean values is rather simple. Booleans simply refer to the truth or falsehood of a given thing. This means that a boolean value can be either true or false, depending upon various conditions, but it will only ever be true or false. A boolean value, for example, can’t be a number, nor can it be a sequence of text.

PowerShell’s boolean setup is very, very simple. In a lot of ways, it’s reminiscent of the old style of doing booleans from the C era, where booleans were literally a 1 or a 0, a 1 meaning true or a 0 meaning false. And in some ways, this still is true. For example, if you check to see if the string “false” is actually false in the boolean sense, it’ll be true because of the fact that it has a value that isn’t 0 (since it is a populated string). As you can see, it’s a little fickle. However, the logic underlying is very simple. What’s more is that PowerShell has predefined variables for $true and $false which it will automatically define things as when you try to see if something is true or not.

So now it’s important that we start to talk about boolean comparisons, or boolean expressions. These are how you can compare one value to another and make a rational decision about whether or not that statement is true. This is actually extremely easy in PowerShell, like many other things.

The logic underlying these is actually relatively simple. Simply think back to high school or college when you were solving algebraic inequalities. Remember how those disjointed equations would try to make you solve what could and couldn’t be on a graph, and then point them out? The logical comparisons of boolean expressions are actually rather simple in the way that they are set up.

There are a lot of different comparison operators in PowerShell. These all have their own unique uses and places where they’d be the best option for comparison. Here are the comparison operators and their meanings.

| -eq | Checks to see if the values are equal to one another. |
| -ne | Checks to see if values are not equal to one another. |
| -gt | Checks to see if left value is greater than right value. |
| -lt | Checks to see if left value is less than right value. |
| -ge | Checks to see if left is greater than or equal to right. |
| -le | Checks to see if left is less than or equal to right. |
| -like | Checks to see if there’s a textual match. |
|  | “Meep” -like “*ep”) would be true. |
| -notlike | Checks to see if there isn’t a textual wildcard match. |
| -match | Checks to see if a string matches a part of another. |
| -notmatch | Opposite of match. |
| -contains | Checks to see if any set of values contains a specific one. |
| -notcontains | Opposite of contains. |
| -in | Checks to see if one value is in a set of other values. |
| -notin | Checks to see if a value is not in a given set of values. |

As you can see, the idea here is relatively simple. All that you’re doing is comparing two (or more) values and evaluating whether something is true or not.

So moving on, when you start a boolean comparison, an innate truth or falsehood is returned. This veracity can be used in order to make bigger decisions.

What kind of decisions can be made here, then? Well, this is where we get to the first major part of all of this. We can use these statements of truth or falsehood in order to make decisions. This is called using conditional statements.

Think about it. All the time, we go out and we compare things - whether they’re tangible objects or whether they’re immalleable events - and then make a decision based off of that. For example, “if it rains this evening, I won’t take a walk in the park.” If we were to say that, then what we would do is wait around until it was that evening, check to see whether or not it’s raining, and then go to the park if it isn’t or stay home if it’s not. Decision making is everywhere, and we do it all of the time.

So how can we incorporate this sort of decision making into our programming and our script writing? Well, actually, it’s rather simple!

Let’s say we had a variable called $apples and it had the value of 1. Well, let’s say that we wanted our script to look at the value of $apples and, if it’s 1, print out “I have one apple.” This would be really easy!

The syntax of an if statement is like this:

if (condition) {

... code here

}

The condition would be whether or not $apples was equal to 1, so we just check for that.

$apples = 1

if ($apples -eq 1) {

Write-Output “I have one apple.”

}

However, you might find that this lacks a little nuance. After all, what if we didn’t have one apple? What if we had two apples, or no apples? Obviously we couldn’t say the same thing for all of these because the grammar would be improper! That’s entirely unthinkable. So obviously we have to allot for these as well. This is where elseif and else statements come in handy. These are attached to your if statement. Note that for logical control flow, neither of these is needed, but they can definitely help you with decision making in your program. They allow you to more tightly control what happens when things don’t meet the first condition.

If you have only an if and an else statement, then the condition in the if statement will be tested; if it’s true, what is in the if statement will be executed. If it’s not true, what’s in the else statement will be executed. The else if statement just allows you to test for another condition on top of whatever you’re already testing in the first; if the first condition fails, it’ll move to the second condition mentioned by the else if statement.

So if we wanted to test to see if we had 1 apple, more than 1 apple, or 0 apples, then we would want 1 apple to be our if condition, 0 apples to be our else if condition (since it’s a specific condition), and then more than 1 apple to be our else condition (since anything that isn’t 1 or 0 will meet it). Here’s about how that would work out:

if ($apples -eq 1) {

Write-Output “I have one apple.”

} elseif ($apples -eq 0) {

Write-Output “I don’t have an apple.”

} else {

Write-Output “I have more than one apple!”

}

And with that, you know the basics of conditionals. Now we need to talk about the other major aspect of control flow: loops.

The first loop we’re going to talk about is the for loop. The for loop is intended for the user to iterate through a set until a certain condition is met. The condition is defined when the for loop is defined. The for loop has three parts of its definition: the initialization of the iterator variable, where the variable that the loop is going to increment or decrement is created; the end condition - when this condition isn’t met; and the incremental step, by which the iterator variable increases every time the loop is iterated through.

Let’s say we wanted to count from 1 to 10\. (Bear in mind that ++ and -- mean “increase by one” or “decrease by one”, respectively.) This is right about how the for loop would look:

For ($i=1; $i -le 10; $i++) {

Write-Output “$i”

}

If you were to put this in a script and run it, it would count from 1 to 10 in the console.

There are also while and do while loops. The only difference between the two is that do while loops execute at least once, then check a condition after and execute while that condition is met. While loops execute for as long as a condition is met, only if that condition is true to start out with.

Do while loops are set up like this:

Do {

}

While (condition)

And while loops are set up like this:

While (condition) {

}

Now, let’s say that we wanted to count from 1 to 10 using a while loop instead. This is going to be a bit different of a setup. Since we aren’t iterating within the loop’s initialization, we have to iterate within the loop itself.

Let’s talk about the logic of the loop. We’re going to want to carry out the loop for as long as our iterator variable, let’s say i again, is less than or equal to 10\. So for as long as it’s less than or equal to 10, the loop will carry on. If it hits 11, the loop terminates.

The first thing we have to do is create the variable before the loop, otherwise the value will reset with every iteration of the loop and it will never terminate.

$i = 1

Now we need to create the beginning of the loop:

$i = 1

While ($i -le 10) {

}

Now, inside the loop, we’re going to have to print the current value of i, of course, but we’re also going to have to increase the value of i every time, too. Otherwise, i will stay the same number and the loop won’t terminate.

$i = 1

While ($i -le 10) {

Write-Output “$i”

$i++

}

Now, if you were to save that into a script and run it, it’d count from 1 to 10\. And with that, you understand the very basics of control flow in PowerShell scripting. It’s an incredibly valuable skill and knowing how it works is going to help you a lot in automating things and making your Windows experience much better.

The last thing that we really have to cover in this book, having covered the basics of scripting and programming logic, is a higher level idea of formatting and filtering that will allow you to take your scripts to the next level.

Chapter 5

h

More Advanced - Filtering and Formatting

A lot of what you’re going to be doing is parsing data. For that reason, I’ve decided to devote a little bit of this book to covering the processes that will go into parsing data,

The first thing that we’re going to talk about is filtering collections. This is important for parsing information from various sources. Generally, when you receive information about the system, it’ll be in the form of object collections. Knowing how to break apart the information that is fed into you is extremely important because that is how you get to the meat of the content that you’re looking for. For example, if you pull up the data on any given process, you’ll get a lot of meaningless drivel that doesn’t quite mean much. There’s not much practical that you can really pull together to do with this, most of the time. However, if you take the time to learn how to filter the information from a given collection, then you can quite easily break apart everything.

What is extremely handy about PowerShell, though, is that it makes the process incredibly simple for you. Or, simple in relative terms at least. For example, there are a lot of built-in cmdlets that will help you to do anything that you need to do.

The most well-known of these is the where-object. In fact, if you ever find yourself talking with other PowerShell scripters or developers then you’ll probably hear them talking about this a fair amount.

We’ve talked before about how everything in PowerShell is an object, since PowerShell is based upon the .NET Framework. And as such, every object has a bunch of intrinsic values and data, called properties. We also talked about how these properties are malleable and can change depending upon the object and the actions performed upon it, and how these properties are innately intrinsic to the object itself. With all of this in mind, there must be a way to filter objects by certain criteria, knowing that these intrinsic and innately defining properties exist, right?

Well, yes. That’s pretty much exactly what the Where-Object cmdlet does. The Where-Object cmdlet will look at a certain collection as given back by another cmdlet and then allow you to sift through the collection according to certain different specified criteria.

Before we go on with this, we need to talk briefly about the idea of the pipeline. We talked about it a little bit earlier in the book, but not nearly in the same scope as we’re about to. When we touched on it briefly earlier, we only talked about what the pipeline is technically capable of - the passing of information from one thing to another until it eventually lands at its end location, generally the output stream. That’s all well and good, of course, but that doesn’t really explain what’s going on here.

In the last chapter, we talked about how functions are able to return a given value, and how cmdlets always return a given object as well. So with that being said, we can understand that this is designed to be quite literally like a pipeline. You put an object in, it goes through and through the pipeline until it comes out the other end.

However, in the PowerShell pipeline, you can actually have the thing that you put in the pipe make some necessary stops along the way. These stops can change the value of the thing that you put in it, output information about it, report diagnostics, do all sorts of different things basically. Then, in the end, your object would come out with all of the relevant information that you were looking for.

In order to designate a “stop” in the pipeline and the transferring of an object to a new process before it comes out the other end, you simply need to type a vertical line character: |

This is all very simple once it’s been explained and you start to understand, but don’t feel bad if it takes you a little bit of working to understand entirely how the pipeline concept even works. It can be a little tricky at first. Basically, just remember that with the first command you execute in a PowerShell directive (or a line in a script), you are generating an object (or a collection of objects) that you can actually pass along and perform procedures upon.

So what does this mean in terms of filtering? Well, it means that first we have to have something that we want to pass along to our filter. For the purposes of this explanation, let’s say that we wanted to filter the results of the cmdlet Get-Process, which returns all processes currently running on the computer, as we talked about earlier. Right now, our statement would look something like this:

Get-Process

Now, before we filter this, let’s figure out what we can actually filter it by. The way to do this is simple. You simply use the Get-Member cmdlet in order to return the members of the object, meaning the methods and properties of the object which are contained within.

Now, we can’t just run Get-Member. We have to pass something to Get-Member in order to, well, get the members, so we have to specify what that is. In this case, we want to know what we can filter Get-Process by, so let’s just go ahead and do that.

What we have to do here is run Get-Process and then throw what it specifies in the pipeline to the Get-Member cmdlet. We would, in that case, type the following in our PowerShell window:

Get-Process | Get-Member

Then press enter. The result will be something along the lines of this:

| Name | MemberType | Definition |
| ---- | ---------- | ---------- |
| Handles | AliasProperty | Handles = Handlecount |
| Name | AliasProperty | Name = ProcessName |
| NPM | AliasProperty | NPM = NonpagedSystemMemorySize64 |
| PM | AliasProperty | PM = PagedMemorySize64 |
| SI | AliasProperty | SI = SessionId |
| VM | AliasProperty | VM = VirtualMemorySize64 |
| WS | AliasProperty | WS = WorkingSet64 |
| Disposed | Event | System.EventHandler Disposed(System.Object, Sy... |
| ErrorDataReceived | Event | System.Diagnostics.DataReceivedEventHandler Er... |
| Exited | Event | System.EventHandler Exited(System.Object, Syst... |
| OutputDataReceived | Event | System.Diagnostics.DataReceivedEventHandler Ou... |
| BeginErrorReadLine | Method | void BeginErrorReadLine() |
| BeginOutputReadLine | Method | void BeginOutputReadLine() |
| CancelErrorRead | Method | void CancelErrorRead() |
| CancelOutputRead | Method | void CancelOutputRead() |
| Close | Method | void Close() |
| CloseMainWindow | Method | bool CloseMainWindow() |
| CreateObjRef | Method | System.Runtime.Remoting.ObjRef CreateObjRef(ty... |
| Dispose | Method | void Dispose(), void IDisposable.Dispose() |
| Equals | Method | bool Equals(System.Object obj) |
| GetHashCode | Method | int GetHashCode() |
| GetLifetimeService | Method | System.Object GetLifetimeService() |
| GetType | Method | type GetType() |
| InitializeLifetimeService | Method | System.Object InitializeLifetimeService() |
| Kill | Method | void Kill() |
| Refresh | Method | void Refresh() |
| Start | Method | bool Start() |
| ToString | Method | string ToString() |
| WaitForExit | Method | bool WaitForExit(int milliseconds), void WaitF... |
| WaitForInputIdle | Method | bool WaitForInputIdle(int milliseconds), bool ... |
| __NounName | NoteProperty | string __NounName=Process |
| BasePriority | Property | int BasePriority {get;} |
| Container | Property | System.ComponentModel.IContainer Container {get;} |
| EnableRaisingEvents | Property | bool EnableRaisingEvents {get;set;} |
| ExitCode | Property | int ExitCode {get;} |
| ExitTime | Property | datetime ExitTime {get;} |
| Handle | Property | System.IntPtr Handle {get;} |

[...]

As you can see, that’s quite a bit of information - that’s still far under half of the values which are returned when we use the Get-Member method. So because of this, we can draw that there are quite a few things that we can technically sort by. But let’s take a look at the information that would actually be relevant by running “Get-Process”.

In my case, the list came back looking a bit like this:

| Handles | NPM(K) | PM(K) | WS(K) | CPU(s) | Id | SI | ProcessName |
| ------- | ------ | ----- | ----- | ------ | -- | -- | ----------- |
| 260 | 24 | 10016 | 16964 | 280.23 | 4868 | 1 | A6100 |
| 331 | 27 | 6028 | 16352 | 3.22 | 3128 | 0 | AgentSvc |
| 195 | 20 | 3448 | 10636 | 30.19 | 2896 | 0 | AppleMobileDeviceService |
| 287 | 17 | 10192 | 19108 | 1.38 | 10712 | 1 | ApplicationFrameHost |
| 790 | 14 | 15924 | 16992 | 189.20 | 13564 | 0 | audiodg |
| 257 | 19 | 4840 | 15764 | 5.59 | 7336 | 1 | BrccMCtl |
| 183 | 14 | 2128 | 11012 | 0.16 | 9208 | 1 | BrMfcWnd |
| 195 | 14 | 2504 | 9320 | 0.17 | 7688 | 1 | BrMfimon |
| 329 | 15 | 3960 | 15248 | 0.30 | 6740 | 1 | browser_broker |
| 3444 | 116 | 344248 | 214400 | 2,025.42 | 2712 | 1 | chrome |
| 92 | 8 | 1432 | 524 | 0.94 | 7216 | 0 | conhost |
| 718 | 25 | 2748 | 9148 | 104.48 | 340 | 1 | csrss |
| 145 | 11 | 1876 | 6472 | 0.11 | 2932 | 0 | dirmngr |
| 416 | 64 | 112724 | 92668 | 101.88 | 11528 | 1 | Discord |
| 163 | 9 | 2716 | 9600 | 0.66 | 14880 | 1 | dllhost |
| 602 | 43 | 77564 | 42544 | 2,435.56 | 1304 | 1 | dwm |
| 142 | 12 | 3028 | 9448 | 0.78 | 8852 | 1 | E_YATINBE |
| 233 | 21 | 2936 | 11200 | 0.36 | 8752 | 1 | EEventManager |

[...]

Obviously, this list has been shortened by a fair amount, but you can get the basic gist of the information which is there. Essentially, the processes in this list are filtered by things such as the number of handles the program is using, the non-paged memory, the paged memory, the working set size, the CPU usage, the virtual ID, and the session ID.

So let’s say that we wanted to see what processes currently running had a session ID of 1\. This is relatively simple. First, you have to understand the syntax of the Where-Object cmdlet. (Oh, and for the record, PowerShell programmers almost never call it - or type it - as Where-Object, opting instead for where the vast majority of the time.)

Anyhow, going back to the whole syntax thing, the Where-Object syntax is as such:

Where-Object { condition }

It will print out the relevant data according to the specified condition as it is or isn’t met. So let’s take a second and look at this. We know that the object that Get-Process returns will have a bunch of innate members. Let’s look for one which designates the Session ID. Looking back at the Get-Member data (it should still be in your PowerShell window), look for a member that has a data type of integer (since the session ID represents an integer) and references the session ID. Since it’s organized alphabetically, this should be pretty simple.

When you look at the member list, you’ll see this tucked somewhere in the middle:

SessionId                     Property         int SessionId {get;}

And that, pretty much, is our golden ticket. So now we can sort according to that. So let’s think about how we can do this.

First off, we have to access the SessionId property of everything on the list. In order to do that, we need to reference whatever object is currently being put through the pipeline. The way that you do that is by the $_ operator. Then we need to access that object’s properties, which we’ll do with a period:

$_.

The period indicates that you’re trying to access a specific member, method, or property of that object. Anyhow, let’s keep moving forward with this. So the thing that we’re going to do next is indicate that for every object passed through the pipeline, the SessionId property must be equal to 1. Here’s how we would do that:

$_.SessionID -eq 1

Now all that we have to do is throw that into our Where-Object cmdlet, like so:

Where-Object { $_.SessionID -eq 1 }

Pay special attention to the curly braces! They’re absolutely necessary and delineate exactly where the condition of the method begins, which is important information.

But wait, if we try to just run this, it’s not going to go all too well… it doesn’t have any information to filter through! So we have to send it the results of Get-Process through the pipeline. The end command should be like so:

Get-Process | Where-Object {$_.SessionID -eq 1}

Now just press Enter. If everything went well, you should see something a bit like this:

| Handles | NPM(K) | PM(K) | WS(K) | CPU(s) | Id | SI | ProcessName |
| ------- | ------ | ----- | ----- | ------ | -- | -- | ----------- |
| 260 | 24 | 10004 | 17152 | 282.39 | 4868 | 1 | A6100 |
| 287 | 17 | 10192 | 19012 | 1.38 | 10712 | 1 | ApplicationFrameHost |
| 257 | 19 | 4840 | 15548 | 5.59 | 7336 | 1 | BrccMCtl |
| 183 | 14 | 2128 | 10832 | 0.16 | 9208 | 1 | BrMfcWnd |
| 193 | 14 | 2436 | 9348 | 0.17 | 7688 | 1 | BrMfimon |
| 329 | 15 | 3960 | 15204 | 0.30 | 6740 | 1 | browser_broker |
| 3512 | 134 | 344244 | 215408 | 2,039.88 | 2712 | 1 | chrome |
| 102 | 9 | 1584 | 6192 | 0.16 | 5220 | 1 | conhost |
| 717 | 26 | 2748 | 9056 | 106.17 | 340 | 1 | csrss |
| 416 | 63 | 108888 | 100344 | 102.45 | 11528 | 1 | Discord |
| 159 | 9 | 2608 | 9220 | 0.66 | 14880 | 1 | dllhost |
| 601 | 43 | 77480 | 42056 | 2,449.88 | 1304 | 1 | dwm |
| 142 | 12 | 3032 | 9464 | 0.78 | 8852 | 1 | E_YATINBE |
| 233 | 21 | 2936 | 10960 | 0.36 | 8752 | 1 | EEventManager |
| 2319 | 84 | 67492 | 103224 | 178.11 | 5896 | 1 | explorer |
| 420 | 28 | 11476 | 31452 | 2.34 | 11484 | 1 | FlashUtil_ActiveX |
| 37 | 5 | 816 | 3052 | 0.02 | 4612 | 1 | fontdrvhost |

The thing you need to pay special attention to here is the SI column, which is no longer a mess of 1s and 0s - you filtered through everything where the session ID wasn’t equal to 1! That’s how you neatly filter through information in PowerShell.

Now, we need to talk about formatting the list so that we get the relevant information and only the relevant information that we’re wanting. For example, let’s look at the list prior. Let’s say we only wanted to show the process’s name, ID, and the time that it was started (a member property of the process object). How could we do such?

Well, this is relatively simple too. There are many different ways to format things in PowerShell, and I’m only going to go over two here: formatting into a list and formatting into a table.

Both follow the same general syntax: simply the name of the cmdlet (Format-List or Format-Table), followed by any parameters that you may need to add. Here, we’re going to work specifically with the parameter -Property, because that is the parameter that you use when you’re working specifically with the properties of given objects.

It’s actually pretty simple, in all reality: let’s say we’re working with properties, and we wanted to format the session ID filtered list into a list which held only the process name, the process ID, and the time it was started, as we previously said. Well, we’d just have to have the names of those properties - name, ID, and startTime respectively - and then work off of that.

To do this, we’d have to first take our session ID filtered list:

Get-Process | Where-Object {$_.SessionId -eq 1}

and then pass it along the pipeline to the Format-List cmdlet:

Get-Process | Where-Object {$_.SessionId -eq 1} | Format-List

But we’re not done yet, we have to sort the list and create it by the properties we specified earlier. For this, we have to initiate the -Property parameter and then sort by the properties that we specified earlier, like so:

Get-Process | Where-Object {$_.SessionId -eq 1} | Format-List -Property name,ID,StartTime

Which would yield the following results:

| Name | : A6100 |
| Id | : 4868 |
| StartTime | : 5/31/2017 7:51:44 PM |
| Name | : ApplicationFrameHost |
| Id | : 10712 |
| StartTime | : 5/31/2017 8:34:03 PM |
| Name | : BrccMCtl |
| Id | : 7336 |
| StartTime | : 5/31/2017 7:52:31 PM |
| Name | : BrMfcWnd |
| Id | : 9208 |
| StartTime | : 5/31/2017 7:52:30 PM |

Formatting for a table would be exactly the same, but using the Format-Table cmdlet instead. If we were to type Format-Table instead of Format-List, it would yield this:

| Name | Id | StartTime |
| ---- | -- | --------- |
| A6100 | 4868 | 5/31/2017 7:51:44 PM |
| ApplicationFrameHost | 10712 | 5/31/2017 8:34:03 PM |
| BrccMCtl | 7336 | 5/31/2017 7:52:31 PM |
| BrMfcWnd | 9208 | 5/31/2017 7:52:30 PM |
| BrMfimon | 688 | 5/31/2017 7:52:31 PM |
| browser_broker | 6740 | 5/31/2017 8:34:04 PM |
| chrome | 2712 | 5/31/2017 7:54:16 PM |
| conhost | 5220 | 5/31/2017 7:51:41 PM |
| csrss | 340 | 5/31/2017 7:48:48 PM |
| Discord | 11528 | 5/31/2017 9:17:38 PM |
| dllhost | 14880 | 5/31/2017 8:27:16 PM |
| dwm | 1304 | 5/31/2017 7:48:50 PM |

And with that, you now know how to sort through, filter, and format sets of information in PowerShell, a super useful feature that I’m sure you’ll be glad you learned.

Chapter 6

h

PowerShell Terminology

The terms involved with PowerShell can get a little bit confusing. In fact, it can seem like you’re somewhat lost in an alphabet soup of different computer terms. Well, don’t worry! Here, I’ve tried to compile some of the most important terms from throughout the book so that you can understand exactly what you’re looking at, just in case you need to go back and reread something.

| Term | Meaning |
| Cmdlet | A name for the various commands that you can issue within PowerShell. Always return an object. |
| Directory | Another term for “folder”. |
| Method (or function) | Code which performs an action in the same way, which may or may not take arguments. |
| .NET Framework | The framework which PowerShell, as well as VB.Net and C#, are all built on. |
| Object | An instance of a class; something which has intrinsic qualities such as methods and properties. |
| Property | Something that has a value stored to it - think the color of a car, the number of tires the car has, and so forth. These are all properties of the car. |
| Working Directory | The folder that you’re currently in on your drive. |

Conclusion

h

Thank you for making it through to the end of PowerShell, let’s hope it was informative and able to provide you with all of the tools you need to achieve your goals whatever it may be.

The next step is to start using the skills that you’ve learned in this book and putting them to good use, automating your computer and doing all sorts of things from the command line that you didn’t know you could do.

The information in this book can only, honestly, get you started - that’s all a beginner book can do. It is on you, my friend, to do the experimenting and the research to carry you from somebody who knows the basics about PowerShell and scripting to somebody who has a solid grasp on everything that they need to do. The reason that I can’t get overly specific is because I’m trying to be rather broad so that you understand the concepts at play. This is important, because I can teach you specific situations all day long, but if you don’t run into those specific situations, that knowledge is absolutely useless.

No, it’s far better as a beginner that you learn the concepts at work so that you can apply those broader concepts to more specific and finite ideas. So spend some time poking around with PowerShell, get a list of the different cmdlets and start playing around. Maybe spend some time learning about things like curl for web scraping. Look up PowerShell tutorials online and follow them.

What this book has given you is something valuable: it’s given you the broad knowledge of the huge amount of different concepts that are at play within PowerShell; it’s a lot to take on at once to try to understand bigger concepts such as objects or frameworks, as well as trying to remember all of these different esoteric commands that PowerShell and command line programming in general entails. However, I genuinely hope that I’ve done a good job of breaking it down into the individual parts and making something worth reading that will give a beginner, like yourself, a great opportunity to learn a lot not just about scripting or PowerShell but computing in general.

Just one last time, I’d like to wish you the best of luck on your PowerShell journey. Thank you again for reading.