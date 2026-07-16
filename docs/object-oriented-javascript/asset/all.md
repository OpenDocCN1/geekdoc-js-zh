![](images/00031.jpeg)

![](images/00001.jpeg)1

## **Table of Contents**

[Introduction...............................................................................1](#part0000.html_link0)
[Who Is This Book For?.........................................................1](#part0000.html_link1)
[What Do You Need To Know To Use This Book?...............2](#part0000.html_link2)
[Getting Around the File System.......................................2](#part0000.html_link3)
[getElementById?..............................................................3](#part0000.html_link4)
[jQuery?.............................................................................3](#part0000.html_link5)
[Web Browser Developer's Tools......................................3](#part0000.html_link6)
[Web Browsers..................................................................3](#part0000.html_link7)
[Are You Ready?...............................................................4](#part0000.html_link8)
[Where Can You Get The Code Samples...............................4](#part0000.html_link9)
[Plunker..............................................................................4](#part0000.html_link10)
[Editing Plunker Scripts.....................................................5](#part0000.html_link11)
[Why Did I Write This Book?................................................5](#part0000.html_link12)
[Important Note About Memory Models................................6](#part0000.html_link13)
[Simplified Models For Instruction....................................6](#part0000.html_link14)
[About The Author.................................................................7](#part0000.html_link15)
[Experience........................................................................7](#part0000.html_link16)
[Broad Technical Scope.....................................................7](#part0000.html_link17)
[Broad Industry Experience...............................................7](#part0000.html_link18)
[Broad Experience.............................................................7](#part0000.html_link19)
[How This Book Is Different..................................................8](#part0000.html_link20)
[Cutting the Onions............................................................8](#part0000.html_link21)
[Chapter 1...................................................................................9](#part0000.html_link22)
[Setting the Foundation: Types...................................................9](#part0000.html_link23)
[How JavaScript Handles Types............................................9](#part0000.html_link24)
typeof Operator Indicates Type From JavaScript [Interpreter.......................................................................11](#part0000.html_link25)
[See It Run At Plunker.....................................................11](#part0000.html_link26)
[Easy Way To Run Code Examples: RunAnyJS..............12](#part0000.html_link27)
[A Closer Look At Your Number Variable..........................13](#part0000.html_link28)
[You Write JavaScript, You Control Memory Chips.......13](#part0000.html_link29)
[What The JavaScript Interpreter Does................................13](#part0000.html_link30)
[First Step: Find Memory.................................................14](#part0000.html_link31)
[The Architects of the JavaScript Interpreter...................14](#part0000.html_link32)

ii [JavaScript Primitive Number: 64 bits (8 bytes)..............14](#part0000.html_link33)
[Reading and Writing That Memory................................17](#part0000.html_link34)
[Value Stored At Address Is Changed..................................18](#part0000.html_link35)
[undefined Will Make More Sense Now..............................19](#part0000.html_link36)
[My Guess At How undefined Is Defined............................20](#part0000.html_link37)
[Booleans Are Easy, But Remember true/false Case............21](#part0000.html_link38)
[Boolean, Probably Stores In One Byte................................22](#part0000.html_link39)
[String Type.........................................................................23](#part0000.html_link40)
[Terminating Character ...................................................25](#part0000.html_link41)
[What If The String Grows?.............................................25](#part0000.html_link42)
[Strings Are Probably Implemented With References..........26](#part0000.html_link43)
[Main Difference Between Reference and Primitive Types. 26](#part0000.html_link44)
[Big Blue Bar : Wall of Memory.....................................27](#part0000.html_link45)
[Why Would They Store the Address Instead of Value?..28](#part0000.html_link46)
[Let The Sub-system Handle the Problem........................28](#part0000.html_link47)
[What Happens When a String Is Changed?........................28](#part0000.html_link48)
[Finally, Objects...................................................................28](#part0000.html_link49)
[Objects Take Up A Varying Number of Bytes in Memory. 29](#part0000.html_link50)
[Empty Object, Stored In Memory.......................................29](#part0000.html_link51)
[An Object Is Composed of Other Types.............................30](#part0000.html_link52)
[JavaScript Arrays Are Reference Types..............................31](#part0000.html_link53)
[Does Understanding All This Memory Stuff Matter to JavaScript Programmers?....................................................32](#part0000.html_link54)
[How Does Primitive Versus Reference Type Impact JavaScript Developers?.......................................................33](#part0000.html_link55)
[First Easy One, What Happens When You Copy?..............33](#part0000.html_link56)
[Step By Step Explanation of Copying Types......................36](#part0000.html_link57)
[Step 1..............................................................................36](#part0000.html_link58)
[Step 2..............................................................................38](#part0000.html_link59)
[Step 3..............................................................................38](#part0000.html_link60)
[Step 4..............................................................................40](XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX)
Step 5..............................................................................41
Steps 6............................................................................42
The Primitive Is Owned By the Reference......................42
Reference Types : Expandable In Memory.....................43
Step 7..............................................................................43

iii Create Copy of Reference Type..........................................44
Step 8..............................................................................44
Ran Out of Memory (Spaces) In My Example...............44
Step 9..............................................................................45
Both of Your References Point To The Same Thing......45
SIDEBAR - Assembly Language? I Thought This Was JavaScript............................................................................47
Chapter 2.................................................................................51
Functions: They're Objects Too...............................................51
JavaScript's new Operator...................................................53
Objects Have Their Own Memory......................................53
Objects Are Memory Wrappers..........................................53
A Closer Look at person Object In Memory...................55
Another Way To State The JavaScript............................56
Natural Language Statement Equal to JavaScript...........56
The Wrapper Is Also Scope............................................56
Error Indicates Scope..........................................................56
Functions Are Objects, They Have Scope...........................57
What Does First-class Type Mean?.....................................57
Using JavaScript typeof Operator...................................57
Functions Are Reference Types: Objects............................61
Passing Objects and Primitives to Functions.......................62
Primitive Type Parameters Have Function Scope...............64
Passing A Reference Type to A Function.......................66
Reference (Base Memory Address) Is Passed To Function ........................................................................................68
Value Changed, Because Memory Address Is Same......69
Summary of Pass by Reference Versus Pass By Primitive ........................................................................................70
Passing Functions To Functions..........................................70
Functions are Reference Types.......................................70
setTimeout – Pass A Function.............................................71
Architectural Principle Revealed In Passing Function........72
A Callback Function ..........................................................73
Separating Functionality To Replace Later.....................74
Replacing Functionality With Less Testing....................74
Functions Are First-class Types..........................................76 JavaScript Makes It Easier..................................................77 Create Template Objects For Instantiation..........................77 JavaScript new Operator.....................................................80 Create Person Object At New Memory Address.............80 What About this?................................................................81 Construction: Automatically Running Code.......................82 Constructor Runs Only Once Per Application................82 More About this .............................................................83 Reference From Inside An Object..................................84 What About getEmployeeId Function Address?.................84 Summary.............................................................................84

v This page intentionally left blank.

# **Introduction**

The person who knows how will always have a job.
The person who knows why will always be his boss. ~Diane Ravitch

## **Who Is This Book For?**

This book is for advanced beginners of JavaScript and software developers who have experience in other languages but little experience in JavaScript. I'll attempt to go fast in this book, always driving the reader's focus to the main point: Object Oriented JavaScript Principles. So, if you don't even know how to declare variable in JavaScript (var x = 15;) you are going to get lost fast.

However, notice that I am not excluding JavaScript developers who have only beginning experience. That is because all through the book I attempt to explain everything as if you are learning it for the first time. (No, I won't treat you like a dummy. I'll just explain things in order, with diagrams and in ways you haven't seen them explained before.) That's why I include Advanced Beginners of JavaScript. What is an Advanced Beginner? To me, he is someone who is first and foremost excited at the prospect of developing in JavaScript. Passion makes up for a lot of other short-comings. In other words, if someone is forcing you to read this book, then maybe you should read something else.

But, if the idea of understanding how Object Oriented Programming in JavaScript works and how the JavaScript Interpreter really handles that code excites you then I believe you'll find this book a valuable investment of your time. In an attempt to further define The Advanced Beginner, I would say she is also someone who has written a few scripts which use arrays, objects and maybe even done some event handling. The Advanced Beginner has definitely written his own functions and knows the syntax to do so:

function <functionName>(<params>) { code;
code;
more code;

}

## What Do You Need To Know To Use This Book?

*Getting Around the File System*

You need to know how to get around your file system and of course how to get your web browser going. I'll provide a skeleton HTML file but you'll need to know how to reference a script from the HTML file.

<script src="main.js"></script>

***getElementById?***

You should probably be familiar with:

document.getElementById("idName").inn erHTML = "some text";

The main reason you need to know getElementById is because I use it in my samples to output example text so you can see the result.

***jQuery?***

I might even get lazy at some point and include jQuery in a script or five so I can use the jQuery selector:

$("#idName").text("some text");

So, if you've ever used jQuery at all, you are ready. If not, figure out the jQuery selector I just showed you and you'll be fine.

***Web Browser Developer's Tools***

I also use console.logand I use Google Chrome a lot with the Developer's Tools which show up at the bottom of the browser window – obviously with the console to view output.

Have you ever used Developer's Tools in any browser? If you have, then you are an advanced beginner. If not, you should learn how to get to them (F12 will get you to them in both Chrome and Internet Explorer).

***Web Browsers***

You can use any browser you want as long as it's one of the

Big 5 (Microsoft Internet Explorer, Google Chrome, Mozilla FireFox, Apple Safari or Opera). Whatever version you use must support HTML5, that way we know it is *new enough*.

***Are You Ready?***

If you understand all of what I just said, you are ready for this book and you'll have no trouble getting through it. If you understand 80% you are fine, because all of those things are very simple. You can just look them up as we go, it'll just slow you down a bit. If you only understand 25% of what I just said, but you are very excited about learning these advanced JavaScript concepts then you'll be okay too. Just expect to have to look up some additional things along the way.

## **Where Can You Get The Code Samples**

I have made all of the code samples avaialable at : http://NewtonSaber.com/OOJavaScript/OOJSamples.zip

I am also building this scripts at plnkr.co (Plunker) so you may click the associated link in the book and see the sample run before your eyes.

***Plunker***

Just keep the following in mind when examining the Plunker code.

The HTML and JavaScript are split into different files so when you click the link to one of the Plunker samples you'll see something like what is shown in Illustration 1.

The sample will display the HTML by default, but to see the associatd JavaScript code, please click the script.js (indicated by the red arrow in the illustration).

![](images/00002.jpeg)*Illustration 1: Plunker sample*

http://NewtonSaber.com/OOJavaScript/Images/Illus1.png

***Editing Plunker Scripts***

Feel free to run and edit any of the Plunker scripts you find in this book. When you alter them and save them it doesn't do any harm to the originals.

## **Why Did I Write This Book?**

There are a few reasons I decided to write this book:

1\. I am an old C++ developer so I've been a little closer to the metal when I've developed software in the past than the “safe” distance JavaScript enforces. I find it interesting, however, that understanding how objects (reference types) are created and stored in memory versus how primitives (intrinsic types, like Number) are stored can open up a JavaScript developer's
understanding of the entire JavaScript Interpreter and what is really going on. I find all of this fascinating (yet another reason I wanted to write this book).

2\. With my background I see things a little differently than how I've seen it explained in numerous other books so I really wanted to put my explanation out there to provide a different take on what is going on.

3\. I love to write, focus on a specific topic and examine programming languages like a research scientist, step by step.

I believe all of these reasons will help the book to be more fun and interesting to read.

## **Important Note About Memory Models**

After writing the first two chapters, I've come back to this introduction to add this note, because I am sure someone will complain about the way I've represented some object or item in memory. First of all, let's talk about strings. At some point someone out there is going to see a place where I show the bytes in memory and you're going to think, "wait a second, a string is immutable and memory gets re-allocated every time the string is changed and this can't be right."

***Simplified Models For Instruction***

Please understand that I have created simplified memory models (illustrations) so that I can help the user focus on one concept at a time and learn the point in isolation from other issues. The point of the illustrations and explanations is not to provide the exact implementation of JavaScript in memory, but to explain how things are probably implemented to lead the reader to a solid understanding of how these lower-level things impact her JavaScript code.
Here's a bit about me, since you've probably never heard of me before.

## About The Author

*Experience*

I've been developing software (writing computer programs), as a professional, since 1993.

***Broad Technical Scope***

I've written programs in C++, Visual C++, Visual Basic (versions 1.0, 3.0, 5.0, 6.0 and VB.Net), Java (not to be confused with JavaScript), C#, PERL, Python, and of course, JavaScript. And many other programming languages (some scripting languages).

***Broad Industry Experience***

I've worked in companies ranging in size from extremely small (50 or less employees) to extremely large (thousands of employees). These companies have been in various industries such as civil engineering, real-estate management, legal data storage and retrieval, mortgage banking, biotech, and ecommerce.

***Broad Experience***

I started out building computers for a small computer shop. I moved on to customer support (help desk) where every call had an angry person on the other end who needed a solution immediately. I worked my way into Software QA (Quality Assurance – testing software) and finally clawed my way into the world of programming computers.

## **How This Book Is Different**

This book is different because I'm different. It's possible that a lot of the computer book writers are true software engineers who come from an academic background and are extremely intelligent.

***Cutting the Onions***

I'm not extremely intelligent. Instead, I just work it. You know what I mean? I may not be the sharpest knife in the drawer, but I can cut the onions. Heck, I've been stuck up a river without a paddle and had to get myself out of the log jam. I've had red-faced managers scream down my neck and threaten my job, if I didn't develop a software solution - fast. I've been at work until 3am working on intractable problems. I've put myself on the line and used everything I have to get the thing working.

You can visit my web site at : http://www.NewtonSaber.com You can visit the book’s web site at:
http://NewtonSaber.com/OOJavascript
You can contact me at newton@newtonsaber.com

Now, let’s get started.

# Chapter 1

### Setting the Foundation: Types

Because of the way the mind works, it is easiest to learn when we focus on one thing at a time. However, when taking on a subject as large as JavaScript which has been in use since it was originally created by Brendan Eich for use in Netscape Navigator 2.0 back in September of 1995, it can be a challenge to know what to focus on first. Additionally, if you don't get your basic foundations set in place it can be much more difficult to learn advanced concepts later. That's why I want to take you back to a very basic concept which underlies everything that goes on in JavaScript: The Type System.

At first look, you may think focusing on the type system is too simple and boring, but I promise I'll keep it short and lively and when we're done you'll understand how JavaScript works better than ever.

## **How JavaScript Handles Types**

In JavaScript – as in many high-level languages – all types can be organized into two categories:

1\. Primitive types -- memory address indicates where the data (or value) is stored.*

2\. Reference types -- memory address indicates where there object is stored.*

* This statement may be confusing. I'll explain this in just a few moments.

First, let's take a look at the primitives.
There are only five primitive types in JavaScript and they are: 1. Number
2\. Boolean
3\. String
4\. undefined
5\. null

Those last two probably look a little odd to you and we'll get to them, but first let's take a look at the first three and learn why it is important to understand that all of these are primitive types. Then, we'll delve into Reference Types and how they are different. The knowledge of the contrast of these two types will actually help you understand how the JavaScript Interpreter – which runs all of your JavaScript code – works and how that creating Objects (Reference types) is so much different than creating these Primitive types.

Creating any one of the Primitive types is very easy in JavaScript.

Just type the keyword var followed by the name you want to use to refer to your variable and then set it to some value. var counter = 0;// becomes a Number type var isConfigured = false;// becomes a Boolean type

var firstName = “David”;// becomes a String

***typeof Operator Indicates Type From JavaScript Interpreter***

We can use the typeof operator to determine what type the JavaScript Interpreter believes a variable is. Of course, whatever the JavaScript Interpreter believes your variable type to be is what it is.

Here's some code to show you how the typeof operator works.

var counter = 0; // becomes a Number type
var isConfigured = false; // becomes a Boolean type
var firstName = “David”; // becomes a String
console.log("counter is a " + typeof counter);
console.log("isConfigured is a " + typeof isConfigured);
console.log("firstName is a " + typeof firstName);

After you run this code and view the console output you should see the following:

counter is a number
isConfigured is a boolean
firstName is a string

***See It Run At Plunker***

Plunker provides a way to see JavaScript samples run, so I'll add these scripts there. If you want to see this first script's code and see it run simply go to the Plunker I created at:
http://plnkr.co/edit/MHEokt?p=preview

***Easy Way To Run Code Examples: RunAnyJS***

If you'd like to run the code example above without having to create an HTML page and include the JavaScript and save the files, you can point your browser at:

http://uncoveryourlife.com/learnjs/runanyjs.htm

You can then copy the JavaScript code above into the textarea on that page and click the [Update Script] button – to indicate that you've added a script you want to run. Then after that simply click the [Run Script] button and the code will run.

You can see what it looks like in Figure 1: Chrome RunAnyJS.htm with Console window.

![](images/00003.jpeg)

*Figure 1: Chrome RunAnyJS.htm with Console window* http://NewtonSaber.com/OOJavaScript/Images/Figure1.png **A Note On Images Within This Book**

**Note** : Because digital books still don't display images very well at times, I also include web links in this book to the larger size images, in case you need them. You'll find them after each image in the book

## **A Closer Look At Your Number Variable**

Now allow me to go back to that somewhat odd statement I made about primitives where I stated:

"memory address indicates where the data (or value) is stored."

What does that mean?

To understand it better you have to remember that all data is stored in memory at some addressable location. Data has to be stored that way so that other program elements can access it. Otherwise, if there was no way to tell where the data was stored there would be no way the computer program could manipulate or display the data and that data would become inaccessible and useless.

***You Write JavaScript, You Control Memory Chips***

Also, keep in mind that down at the bottom, somewhere the value you indicated you want to store is actually stored in memory somewhere which has a unique address. That's right, you are actually controlling the switches on a memory chip somewhere in the computer simply by typing:

var x = 55;

Again, all you have to do to create a Number in JavaScript is write code like the following:

var x = 31;
var z = 56;

## **What The JavaScript Interpreter Does**

The JavaScript Interpreter notices that you've set the value to a numeric and decides that the type will be Number. Since it is a Number, the Interpreter knows that it will take a certain number of bytes to store up to a maximum value.

It is necessary for the Interpreter to know what type it is because of what is really going on behind the scenes – at the lower level of computing. When you simply create a Number variable (var counter = 5;) the Javascript Interpreter has to do a some things so the computer's processor knows what you want to do.

Here are some of those things the Interpreter does: 1\. find a memory location which has enough contiguous slots to store a Number type.

2\. Create an entry in an internal lookup table to store the name of your variable with the name of your variable – so it can know where your variable is stored in memory when you refer to it using the name you defined.

***First Step: Find Memory***

To complete the first step, the JavaScript Interpreter has to know the number of bytes that a Number type takes up in memory.

***The Architects of the JavaScript Interpreter***

In the case of a primitive type (Number, Boolean, String, etc) the architects who created the JavaScript Interpreter have decided that each of them will take a predetermined number of bytes in memory.

***JavaScript Primitive Number: 64 bits (8 bytes)***

Currently in JavaScript running in browsers Number types get 8 bytes (64 bits) of memory space. Some architect made that decision as a trade-off on the max value that you can store and the memory it will take up for every Number in your program.

At the lower level where the CPU (main processor) is running and where memory is read in bits, it makes things much easier for a low-level programmer when data is written in sequential memory addresses.

What It Looks Like

When you create a new number variable the JavaScript Interpreter goes out and finds 8 sequential bytes in the addressable memory space that is available to it and sets the bits it finds there to represent the value you have stored.

var counter = 27;

Interpreter stores 27 at the address 0x00FFC0.

![](images/00004.gif)*Figure 2: Value 27 stored in memory*

http://NewtonSaber.com/OOJavaScript/Images/Figure2.png

Take a close look at Figure 2: Value 27 stored in memory.

Imagine that each rectangle represents a byte of memory. Most modern computers only allow you to address one byte of memory (not down to bit level) and so each address represents that one byte. In our case when we wrote var counter = 27; the Interpreter found 8 bytes of memory which starts at address 0x00CCF0 and it sets the bits to equal 27\. Also, note that even though we can store the value in the first byte, the Interpreter (and web browser and Operating System) actually set aside the entire 8 byte block of memory. I've set those bytes to have all their bits zeroed out to indicate that they are in use. That means nothing else can use those bytes or else JavaScript would interpret that to mean that the value of counter had changed. That memory is solely under the control of JavaScript for the purpose of storing values to the counter variable.

***Reading and Writing That Memory***

After the JavaScript Interpreter remembers that your name of counter is how it will get to that memory. That way when code further down in your program does something like:

counter++; // increment the counter.

Then it can retrieve the value that is stored there (27), add one to that value and store it in the same place again so that memory will now look like what you see in Figure 3: Value 28 stored at location.

![](images/00005.gif)*Figure 3: Value 28 stored at location*

http://NewtonSaber.com/OOJavaScript/Images/Figure3.png

## **Value Stored At Address Is Changed**

The point here is that the **value** stored at the memory address has changed. Also, now that the Interpreter has stored the address where this data is located, you cannot change that address within this program. It is locked. That means you can update the value at the address by changing the value of your variable, but you can never change the address that the variable points to. Ah, as a matter of fact, in other languages (C, C++) there are pointer variables which allow you to change the address the variable points to.

In just a moment we will contrast this to what happens when a Reference type is changed and it is very important to your understanding of how JavaScript works.

## **undefined Will Make More Sense Now**

Now that I've explained that, I can explain to you the undefined primitive value. Remember when I told you that when you set the variable to a value then the JavaScript Interpreter decides what type it is?

Well, suppose you do the following in JavaScript: var x;
What type is x?

It is an undefined and we can prove it with the following code:

var x;
console.log("x is " + typeof x + " type");

Now, let's think about what JavaScript has to do in this case. It cannot determine the type and yet it has to keep track of the fact that you created a new variable. But, what should it's value be? In many languages (C++, C#, Java – no relation to JavaScript) it has a value of null. But in JavaScript the architects have created this special value of undefined for this case.

In this case, the variable has not had any memory assigned to it. It cannot, because the Interpreter has no idea how much memory the thing will take up in memory.

## **My Guess At How undefined Is Defined**

Here's my guess at what JavaScript does.

Somewhere way down in memory, there is one lonely address that has an undefined type sitting in it. It may look something like this what you see in Figure 4: the one undefined object in the address space.

![](images/00006.gif)*Figure 4: the one undefined
object in the address space*

http://NewtonSaber.com/OOJavaScript/Images/Figure4.png

Then, when you create a new variable without setting it's value, the Interpreter stores the name of your variable in its lookup table and then sets its value to that location (0x000001) so that when you ask what type var x is, it returns the type it is pointing to: undefined. That is supposed to indicate to the JavaScript developer that the variable has not had its value set yet.

Okay, so what about null? Okay, so far we've looked at two of the primitive types Number and undefined. Let's take a quick look at the Boolean and String types, because they are very similar to Number, then we'll look at our Reference types and it'll be a bit easier to understand the null type.

## **Booleans Are Easy, But Remember true/false Case**

A Boolean simply allows you to create a variable that stores only two states: true or false.

You can create a Boolean variable very easily:

var isConfigured = false;
console.log("isConfigured is a " + typeof isConfigured);

If you run it at my site
(http://uncoveryourlife.com/learnJs/runanyjs.htm) you will see the result shown in Figure 5: Result of create Boolean.

*Figure 5: Result of create Boolean*

http://NewtonSaber.com/OOJavaScript/Images/Figure5.png You can see the Plunker for these two Boolean scripts at: http://plnkr.co/edit/KCNVZvljPhVkNssZwqZp?p=preview

Notice that the falseis lowercase. It has to be because lowercasetrueand lowercasefalseare keywords in JavaScript True and False are not.

You can see that by running this code:

var isConfigured = False;
console.log("isConfigured is a " + typeof isConfigured);

False is undefined in JavaScript so you get an error as soon as you attempt to set the variable.

## **Boolean, Probably Stores In One Byte**

A Boolean probably stores in one byte since you could literally store it in one bit (either 1 or 0). The Boolean probably looks similar to what is shown in Figure 6: Boolean value of true (1) stored in memory.

![](images/00007.gif)*Figure 6: Boolean value of
true (1) stored in memory.*

http://NewtonSaber.com/OOJavaScript/Images/Figure6.png

If the value is false, then most likely all bits are 0 with a final value of 0\. However, notice again, that it stores the value of the variable at the memory address.

## **String Type**

Finally, let's take a look at the String type.

You can create a String with the following code.

var firstName = "robert";
console.log("firstName is a " + typeof firstName);

You can see the results of that code in Figure 7: Creating a string type.

*Figure 7: Creating a string type*

http://NewtonSaber.com/OOJavaScript/Images/Figure7.png You can see this code Plunker at:
http://plnkr.co/edit/BoYunjGYMQ9MkGfDzOcI?p=preview

Strings are a little different, because each character in the string takes a byte to store, but the length of the string can not be determined until the variable has it's value set.

The Interpreter (and lower layers like web browser and lower to the Operating System) still has the constraint that it must find contiguous memory to store the string in.

That means there is more work for the underlying layers to do to store your string.

Let's look at this a bit more closely by looking at the memory when you store a string with the following JavaScript: var companyName = "Big House";

Take a look at Figure 8: string in memory.

![](images/00008.gif)*Figure 8: string in memory*

http://NewtonSaber.com/OOJavaScript/Images/Figure8.png

***Terminating Character***

First of all notice that last odd character located at 0x00CD01. Since the string can be any length, there has to be a way to determine the last byte that is associated with the string. In C and C++ they used a \0 (backslash followed by zero) to denote this. It's probably the same in JavaScript. The point to take away from this is that someone has to handle the issue that strings are of different lengths and the constraint that associated memory for a variable has to be contiguous.

***What If The String Grows?***

Instantly this should bring to mind the problem. What if the string becomes longer, because you set it to a new string value?

For example, if later in the program you store:

companyName = "Big House Crafts";

Suddenly the program needs seven more contiguous bytes. But, what if the bytes past 0x00CD01 are already taken for use with other variables?

## **Strings Are Probably Implemented With References**

That is why that most likely a string in JavaScript is not actually implemented by value, but by reference. Now, we are moving toward our understanding of Reference Types.

## **Main Difference Between Reference and Primitive Types**

While primitive types store the actual value at the memory address. Reference types store an address at the memory address. Let me say that again. Instead of storing the actual data value at the memory address, reference types store an address which points to another place in memory where the data is actually stored.

Think about those pictures of memory I've shown you so far and compare it to the one in Figure 9: Storing a Reference Type, which is what memory looks like when we store a Reference type.

![](images/00009.gif)*Figure 9: Storing a Reference Type*

http://NewtonSaber.com/OOJavaScript/Images/Figure9.png

First of all, in Figure 9 I am still showing you the storage of the Number primitive (in 0x00CCF0 - 0x00CCF7). However, we want to focus on the value (which is another address) that is stored at location 0x00CCF8.

***Big Blue Bar : Wall of Memory***

The big blue bar simply represents a separation of the memory on the left to the memory on the right so I can show you that the Reference type stored a memory address which points to another section of memory, which is where the actual data for the string is stored.

The memory address it points to is 0x00AA01\. That is the base address where the variable length string (in this case 16 bytes + 1 byte for terminator) is stored.

***Why Would They Store the Address Instead of Value?***

The string type points out the challenge of storing a type which will take up a variable number of bytes in memory. As soon as you change the length you need a different block of memory and so the Interpreter would have to keep changing that value in its lookup table. Instead of doing that the architects can simply store an address and then go to the address whenever it changes, because the string has changed.

***Let The Sub-system Handle the Problem***

There is a lot more to it than this, because some other lower level process (beneath the Interpreter) would also have to find the contiguous bytes of memory and that's why the Interpreter handles Reference types this way: to make it easier on itself and let the sub-system handle that problem.

## **What Happens When a String Is Changed?**

Now, you can see that when a string is changed, all the Interpreter does is count the bytes in the string and ask a subsystem to go and store the string and then report back the base address where the string is stored. Next, all the Interpreter has to do is store the address.

## **Finally, Objects**

This brings us into the land of Reference Types.
A reference type is an object or a User Defined Type (UDT). A user defined type will also require a varying number of bytes depending on how it is defined.

## **Objects Take Up A Varying Number of Bytes in Memory**

Let's take a look at a basic Object and learn more about why it is true that it will take up a varying number of bytes in memory.

Here's one way to create a new object in JavaScript:

var firstObj = {};
console.log("firstObj is an " + typeof firstObj);

When you run that code, it will write the following to your web browser conosle:
firstObj is an object

You can see the Plunker at:

http://plnkr.co/edit/wkUzhlrCeotoYq5OAYgl?p=preview

## **Empty Object, Stored In Memory**

That object is basically empty, because we haven't added any properties to it. I don't know how many bytes it takes up in memory because that depends upon how the JavaScript Interpreter architects have implemented the basic JavaScript object but for our intents and purposes all we know is that the Interpreter has requested that the sub-system create an object in memory and has requested the base address of that object and stored it so it can get to it again.
It might look something like what you see in Figure 10: Empty Object in memory.

![](images/00010.gif)*Figure 10: Empty Object in memory*

http://NewtonSaber.com/OOJavaScript/Images/Figure10.png

## **An Object Is Composed of Other Types**

However, an object can be – and usually is – composed of other types.
For example, if we take our previous object and add a couple of items to it we need more memory to store the entire object.

firstObj.name = "builder";
firstObj.counter = "0";
firstObj.isConfigured = false;

At this point, we need at least 17 bytes to store all of this: 7 bytes for the string + 1 byte for the string terminator + 8 bytes for the number and one more byte for the Boolean. However, Object is a Reference type so it doesn't matter. What happens instead is that the new memory is allocated and the base address is reported to back and stored by the Interpreter.

## **JavaScript Arrays Are Reference Types**

Are there other Reference types? Yes, the JavaScript Array is a Reference type because it has a variable size in memory also since you can push or pop items onto the array.
You can create an array and push values on and pop values off (altering its size on the fly) Here is an advanced script which adds numerous things to an array. Run it or check out the output in Figure 11: Array contains object and more, because it should make you think about the fact that the item in the array is growing in memory on the fly. It matters.

var allItems=[];
allItems.push({});
allItems.push({});
console.log("There are " + allItems.length + " items in allItems.");
allItems[0].x = 55;
allItems[0].today = new Date(); console.log(allItems[0]);

![](images/00011.jpeg)*Figure 11: Array contains object and more*

http://NewtonSaber.com/OOJavaScript/Images/Figure11.png

You can examine the script closer and alter it at the Plunker: http://plnkr.co/edit/sMcU70Gg1bRAofaRtLir?p=preview

Notice that the Chrome Developer tools allow you to output the array item to the console and then inspect what is contained inside that item. In the example in Figure 11: Array contains object and more, you can see that I've added a variable size object to the array which also varies in size in memory. This is all possible because of Reference types.

## **Does Understanding All This Memory Stuff Matter to JavaScript Programmers?**

Okay, so now you know about this distinction between primitive types which store their values at the address and reference types which store a memory address in the initial memory address, but how does that impact you as a JavaScript developer? I'm glad you asked, because it has a huge impact on understanding your code.

## **How Does Primitive Versus Reference Type Impact JavaScript Developers?**

If you've read through the previous material and you have a basic handle on it, then you are at a different place than 90% of the JavaScript developers out there, because they do understand that primitives and reference types are stored differently. Understanding this in depth helps us build more robust code. Let's take a look at a sample to show you how important it is.

## **First Easy One, What Happens When You Copy?**

Now, we can begin to talk about what happens when you copy a primtive type versus what happens when you copy a reference type.

Copying a primitive type is different than copying a reference type and it is different because of the way these different types are stored in memory.

Let's take a look at that right now with one script that displays the difference.
NOTE: I'm providing the entire script here which you can run at http://UncoverYourLife.com/LearnJS/RunAnyJS.htm However, it is probably difficult to read in this formatting so I am also placing an image of the script with output at Figure 12: Copy of Primitive Type verus Copy of Reference Type.

// ### Create primitive copy it into another primitive ###
var numberOfChildren = 1; // STEP 1 console.log("numberOfChildren is : " + numberOfChildren + " - STEP 1"); numberOfChildren = 3; // STEP 2 console.log("Changed numberOfChildren to : " + numberOfChildren + " - STEP 2");
var numberOfGrandkids =
numberOfChildren; // STEP 3
console.log("numberOfGrandkids is : " + numberOfGrandkids + " - STEP 3"); console.log("changing
numberOfGrandkids to 5...");
numberOfGrandKids = 5; // STEP 4 console.log("numberOfChildren is still : " + numberOfChildren + " STEP 4");

// ### Create Reference and copy it into another reference ####
var infoOrig = {} // STEP 5
infoOrig.children = 2; // STEP 6 console.log("infoOrig.children is : " + infoOrig.children + " - STEP 5 & 6");
infoOrig.children = 4; // STEP 7 console.log("Changed
infoOrig.children to : " +
infoOrig.children + " - STEP 7");

var infoCopy = infoOrig; // STEP 8 console.log("infoCopy.children : " + infoCopy.children + " - STEP 8");

infoCopy.children = 7; // STEP 9 console.log("infoOrig.children HAS CHANGED!!: " + infoOrig.children + "
- STEP 9");

You can examine the script more closely at the Plunker: http://plnkr.co/edit/IDbJAGTEfvdAh3fyOj5Z?p=preview

Take a look at Figure 12: Copy of Primitive Type verus Copy of Reference Type to see the output. Next I'll take you through each of the steps and show you what actually happens in memory and why the copy of the Reference type seems to act strangely.

![](images/00012.jpeg)*Figure 12: Copy of Primitive Type verus Copy of Reference Type* http://NewtonSaber.com/OOJavaScript/Images/Figure12.png

## **Step By Step Explanation of Copying Types**

Now, match up the following steps to the steps you see in the script and you'll see why the copy of the Reference type seems to do something wrong, even though it behaves exactly in the way the JavaScript Interpeter architects designed it.

***Step 1***

Create a primitive (numberOfChildren) and set its value to 1 (it's a Number type).

![](images/00013.gif)*Figure 13: STEP 1 - Create Number Primitive*

http://NewtonSaber.com/OOJavaScript/Images/Figure13.png

Notice that we have a base memory address of 0x00CCF0and that the value is 1\. I've set all the bytes to be
numberOfChildrenjust so you can see that those bytes are assigned to that primitive for the lifetime of the program. Change the value ofnumberOfChildren. Since this is a primitive, the Interpreter knows the base memory address and sets that memory to be a value of 3 now. *00000011 is binary 3.*

![](images/00014.gif)*Figure 14: Step 2 - Change value of numberOfChildren*

http://NewtonSaber.com/OOJavaScript/Images/Figure14.png

***Step 3***

Create a new primitive (of type Number) named

numberOfGrandkids and copy the value from numberOfChildreninto it. When the new primitive is created, it gets a base address of0x00CCF9and the value of 3 gets copied into that new memory address.

![](images/00015.gif)*Figure 15: Step 3 - Create new primitive copy value into it*

http://NewtonSaber.com/OOJavaScript/Images/Figure15.png

Set the value of numberOfGrandkids to 5;

![](images/00016.gif)*Figure 16: Set numberOfGrandkids = 5*

http://NewtonSaber.com/OOJavaScript/Images/Figure16.png

Look closely at Figure 16: Set numberOfGrandkids = 5 and recognize a couple of things:

1\. the value of numberOfGrandkids is now 5 (binary 00000101)

2\. the value for numberOfChildren has **not** changed. It is still 3\. The script prints out this value to display that.

***Step 5***

Now we create a Reference type (Object) named infoOrig. Remember that we can initialize an empty object with the open/closed {} brackets.

![](images/00017.gif)*Figure 17: Create Reference type (Object)*

http://NewtonSaber.com/OOJavaScript/Images/Figure17.png

Just as we learned before, we see that the Interpreter gets a base address (0x00AA01) for the Object in memory and stores that base address in its address space (at 0x00CCF8) instead of a value.

***Steps 6***

Now, we add a new primitive (Number) named childrento the Object we just created (infoOrig), then we set the primitive's value to 2.

![](images/00018.gif)*Figure 18: Add new primitive to reference type*

http://NewtonSaber.com/OOJavaScript/Images/Figure18.png

You can see in Figure 18: Add new primitive to reference type that the new primitive has been created and stored in memory (in the yellow highlight).

***The Primitive Is Owned By the Reference***

Keep in mind that the primitive named childrenis now owned by the Reference type (infoOrig) so it manages the memory of that particular item. That also means that the reference item takes up the entire memory space of the new primitive plus any memory that the reference object itself takes up – such as the memory at address0x00AA01.

***Reference Types : Expandable In Memory***

This is one of the primary reasons an Object is a Reference type: because it's size in memory cannot be predetermined since it is a User Defined Type (UDT). In this case our UDT is only made up of a Number, but in other cases the object may contain any number of primitives and/or other reference types.

***Step 7***

Step 7 is similar to what we did in Step 2 when we worked with the first primitive type (numberOfChildren). In Step 7 we are simply changing the value ofchildrento 4\. The only difference is that this primitive is owned by the reference type (infoOrig). However, you see effectively no difference at this point.

Memory will now look like what you see in Figure 19: Alter value of primitive type owned by reference type – now the value ofchildrenis 4 (binary 00000100).

![](images/00019.gif)*Figure 19: Alter value of primitive type owned by reference type* http://NewtonSaber.com/OOJavaScript/Images/Figure19.png

## **Create Copy of Reference Type**

Now we set up for the extremely interesting change which should amaze you and will definitely open your mind to understanding programming from a new angle.

***Step 8***

Understanding this one concept will make you a better programmer in all languages, because you will understand what is really happening when you write code.

To create a copy simply means to create a new variable name and assign that variable name the previously created value. We did it with the primitive and now we'll do the same thing with this one line of code:

var infoCopy = infoOrig;

However, that one line of code is vastly different, because we are attempting to create a new Reference Type which has the same value of the previously created Reference type.

What you have to remember though, is that the value stored for a reference type is an address (memory location which points to the place in memory where the object exists).

***Ran Out of Memory (Spaces) In My Example***

I seem to have ran out of memory (spaces) in my example figures so I will take the value at 0x00CCEE (assuming that those values were emptied out and not used). I'm doing this simply for the print space.

When the JavaScript Interpreter sees the line of code it does the following:

1\. creates a new Reference object (infoCopy) in its internal table.

2\. Saves the address of infoOrig (0x00AA01) at the address where it refers to infoCopy (0x00AA01)

It all looks like what you see in Figure 20: infoCopy Reference Type Created. Notice that now, you have two variables which point to the same place in memory. Both of these variables ***refer*** to the same object in memory – the one at address 0x00AA01.

![](images/00020.gif)*Figure 20: infoCopy Reference Type Created*

http://NewtonSaber.com/OOJavaScript/Images/Figure20.png

***Step 9
Both of Your References Point To The Same Thing***

This is the reason that now when you alter the value of infoCopy with the JavaScriptinfoCopy.children = 7 you are also altering the value of infoOrig.children.

When the Interpreter runs that line of code, it looks up the base address for infoCopy and gets (0x00AA01). It then finds the property named children inside that object and sets it to the value 7.
When that happens, your other variable (infoOrig) is still referencing the same memory so you have altered that value also.
Now memory looks like what you see in Figure 21: infoCopy and infoOrig Both Point to Same Address.

![](images/00021.gif)*Figure 21: infoCopy and infoOrig Both Point to Same Address*

http://NewtonSaber.com/OOJavaScript/Images/Figure21.png

Do you see how fast it is to create a copy – also known as a new reference -- of an object now?

Everything else you learn about JavaScript objects is based upon this and that is why it is so important to know what is actually going on behind the scenes.

We will look further into the implications of Reference types as we go through the book, but now that you know that you will be able to understand that rest of the book even more. I'll leave you in this chapter with the sidebar on Assembly Language and we'll meet again in the next chapter to talk about JavaScript Functions (they're reference types too).

## **SIDEBAR - Assembly Language? I Thought This Was JavaScript**

In the past programmers didn't have all the nice GUI (graphical user interfaces) we have now and they had to know how to talk directly to the CPU (main processor) of the computer and tell it to store their data at a specific memory location (address).

They used Assembly language or even before that they used Machine language – which spoke the exact cryptic language that the processor spoke.

At times, their code – in Machine Language – literally looked like a list of zeros and ones:
11100101011100000100101010001101001.

That would tell the CPU to store the value 15 at memory address 0x00CC10\. Not really, I just made it up. But, honestly, their code really was just a list of zeros and ones in Machine language.

**Mistake Prone**

Lots of mistakes were made as computer scientists' eyes crossed as they tried to determine if it was three ones and a zero or four ones and a zero. Debugging that code was killer hard. And, hard on the eyes.

**3^(rd) Generation Language**

You are now using a 3GL (3^(rd)Generation Language) or a high-level language, because you don't have to speak directly to the processor. Instead you write code which looks a bit more like natural language and something turns that code into something the computer can understand.

**JavaScript Interpreter Works For You**

The something that does that work in our case is the JavaScript Interpreter and the Interpreter runs inside the web browser. The Interpreter determines how to translate the JavaScript commands you type into commands the computer can understand and carry out.That means that us lucky developers can now write code that is much easier to learn (JavaScript). Instead of having to understand cryptic processor Op Codes (operation codes) and memory addresses, all you have to do to store a value at a memory location is type the following valid JavaScript:var x = 15;

# Chapter 2

### Functions: They're Objects Too

We learned a lot about what happens behind the scenes in the last chapter and this chapter will continue on in the same way. Last time we learned that we could create an object in the following way:

var person = {};
person.firstName = "frank";
person.lastName = "smith";

But, now suppose you want to create anotherperson.

You want to do so, because you don't want to have to type all the code to add the properties (lastNameand firstName again).

You might think, okay, I'll do the following:

var person2 = person;

However, as we learned in the last chapter, that doesn't create a new object. Instead it just makes a new reference to the same object using a new variable name.

That doesn't help us if we want person2to have a different firstNameand lastName i.e. new memory addresses where we can store new values.

In other languages, like C++, Java, or C# we would create a class template which we could then instantiate into an object. It would look something like the following:

// C# code comparison
class person
{

// this is constructor, which is automatically called
// when the new object is
instantiated
public person(firstName,
lastName);
public string lastName;
public string firstName;
}

Then whenever we wanted to use this object we would just do the following:

// ### C# CODE ########
person ted = new person();
ted.firstName = "ted";
ted.lastName = "jones";

**Definition** : Instantiate means to allocate memory and construct the object in the physical memory. It means the object is a valid structure residing in memory and (depending upon accessibility) is accessible and usable to your program.

In C++, Java, C# you have the newkeyword which allows you to create a new object that exists at a new memory address. Whenever you want a new one, you simply tell the compiler : person variableName = new person()and you get one.

## **JavaScript's new Operator**

JavaScript does have a new Operator, however it does not have the concept of a class template. Fortunately, in JavaScript, we can mimic what I showed you in C# sample above, by using functions.

That is because functions are actually objects. Since functions are objects, let's talk about another aspect of objects for a moment.

## **Objects Have Their Own Memory**

Remember that objects have their own memory space. Another way to say that is objects may contain other primitive types (Number, Boolean, etc) and other reference types (Objects, Arrays, etc) and you cannot get to those without going through the instantiated object.

In code it looks like the following:

person.firstName = "Wilma";

JavaScript does not provide any other way to get to firstName, except to go through the instantiated person object. The object memory is segregated.

## **Objects Are Memory Wrappers**

Another way to say this, might be to say that objects are memory wrappers. Let's take a look at a picture of memory again. This time we'll create a more advanced object which contains a Number, String, Boolean and an Array (Reference type).

Here's the JavaScript code:

var person = {};
person.firstName = "Ted"; person.age = 53;
person.hasChildren = true; person.children = [];
person.children.push("sam"); person.children.push("sara"); person.children.push("sandy");

You can see what the person object might look like in memory by examining Figure 22: person Object In Memory.

![](images/00022.gif)*Figure 22: person Object In Memory*

http://NewtonSaber.com/OOJavaScript/Images/Figure22.png

***A Closer Look at person Object In Memory***

In Figure 22, you can see :
1\. The base address of the person object is 0x00AA01 – that address points to where the actual person object (light orange area in Figure 22) is located in memory

2\. The person object contains a reference type (Array object) named childrenwhich points to the base address of the array object at 0x10FF00 (light green area in Figure 22.

3\. The bytes of each string in childrenare stored in the array object.

You can examine the code more closely at the Plunker: http://plnkr.co/edit/ou3IpPVMhQqNu89fS7J9?p=preview

You cannot get to the values inside the childrenArray without going through theArrayobject. For example if you want one of those values you can reference it with the following JavaScript snippet.

console.log(person.children[0]);

That is because you have no way of referencing the memory which is contained within that array without referring to the array itself. It is as if the Array object has built walls around those values and you have to come to the Array object to get to the values.

The same is true for the items which are contained within the person object. As a matter of fact, we can call an object a container. You cannot get to any of the items in theperson object without doing something like the following JavaScript:

console.log(person.age);

***Another Way To State The JavaScript***

That JavaScript syntax is like saying :
Go to the person object and look inside (dot .) and find a property called age and tell me the value that is stored there.

***Natural Language Statement Equal to JavaScript***

This is basically another way of saying:
Look in the internal JavaScript table and find the address of the person object. It is 0x00AA01, so go to that address and lookup the address of the age Number (primitive). That address is 0x00AA05 so look at the memory and determine what value is stored there.

***The Wrapper Is Also Scope***

The interesting thing about these object wrappers is that they create a scope. They limit the scope of how you can view the values which are contained within them.

As a matter of fact Java, C++, and C# use some keywords to indicate whether or not a property is viewable outside of an object. You saw that in the sample code earlier where I had some statements which began with the word public.

## **Error Indicates Scope**

You can see that the scope is limited because if you add the following line to your script:

console.log(age);
In Google Chrome you will receive an error that states: "age is not defined"

That's because you are looking in your applicationscope and not yourpersonobject scope.
I showed you all that so that you may now better understand functions. In JavaScript, functions are objects and they have scope.

## **Functions Are Objects, They Have Scope**

Scope is very important in the programming world. And, it can be very confusing in the JavaScript world.

One of the main reasons to use functions in our code is to break them up into manageable pieces we can work on. Each function has its own scope and allows us to manage the variables they manipulate so we can be sure that something else is not manipulating them behind our backs.

That is how scope helps us as programmers. We'll talk more about scope as we look closer at functions. Functions are also a type in JavaScript.

## **What Does First-class Type Mean?**

It just so happens that functions are also considered First-class types in JavaScript.

If you read around about JavaScript you will probably stumble upon people saying "functions are first-class objects" or "functions are first-class types". However, they rarely explain what that means in plain terms so I want to do that here.

It simply means that a function actually becomes a type in JavaScript. Just as there is a primitive Number type or an Object Reference type, there is a Function type also and it too is a Reference type.

***Using JavaScript typeof Operator***

We can see this new type (function) by using the JavaScript typeofoperator.

First, we need to define a function that we can test. Here's a simple function which counts the number of characters in a string which is passed to it.

function charCounter(targetString)

{
return targetString.length;
}

Here's some code to use that function:

var el =
document.getElementById("first"); var output = "this string's length is ";
el.innerHTML = output +
charCounter(output);

Now, we can check the type of the thing named charCounter.

var element2 =
document.getElementById("second"); element2.innerHTML = "charCounter is a " + typeof charCounter;

Of course, once you run that code you'll see that it displays : charCounter is a function

The JavaScript Interpreter knows it is an object of type function.
Functions and Scope

Just as we've learned that Objects have scope, we also learn that functions have scope.

Take a look at the following function
function getRandomInteger()
{

var randomVal = Math.ceil(Math.random()*1000); }
// call the function to generate a random number
getRandomInteger();

Even though the function above generates the random number, you can only access that value within the function. Obviously, we can add the following line to the function so that we can get the value:

return randomVal;

The point here is that functions have their own scope and that is helpful to a JavaScript programmer so you can keep your values straight.

// create a variable with application scope
var randomVal = 55;
el1 =
document.getElementById("first"); el1.innerHTML = "randomVal is : " + randomVal;
function getRandomInteger()
{

// create var with function scope var randomVal =

Math.ceil(Math.random()*1000); var el2 =
document.getElementById("second"); el2.innerHTML = "inside
getRandomInteger randomVal is " +
randomVal;
}
getRandomInteger();
var el3 =
document.getElementById("third");
el3.innerHTML = "back outside
getRandomInteger, randomVal is " +
randomVal;

If you run that code you'll see that altering the randomVal inside the function has no affect on the randomVal at the application scope.

The output looks like what you see in

![](images/00023.jpeg)*Figure 23: Function scope and variables*

http://NewtonSaber.com/OOJavaScript/Images/Figure23.png

Since the first randomVal is defined outside of the function and the other one is defined within the function they are two different variables stored at two seperate memory locations.

## **Functions Are Reference Types: Objects**

A function is a Reference type and is stored in memory the same way objects are – they are objects -- so memory will look very similar to what we saw earlier. Take a look at the view of memory for this last program shown in Figure 24: function object in memory.

![](images/00024.gif)*Figure 24: function object in memory*

http://NewtonSaber.com/OOJavaScript/Images/Figure24.png

While you are examining Figure 24 there are a number of things to examine closely.

1\. The randomVal on the left (orange color) is the application-wide variable not the same one as the randomVal on the right (green color) which is the one which is scoped to the getRandomInteger function. As you can see, they have different base memory addresses and setting one will have no affect on the other.

2\. The function in memory (green color on the right) looks just like our previous examples of other Reference types. That is because it is a Reference type and inherits from the JavaScript base Object type.

3\. The application scope contains two Reference types to HtmlDivElements (el1 and el3). The function scope contains one reference to an HtmlDivElement. Those are used simply to output the strings so you can see them so I have not shown the extra memory for those. Just be aware that those three items become References also, since they are references to HTML elements.

4\. One more thing to notice here is that in our sample the randomVal inside the function got the value of 897 which will not fit into 8 bits (one byte) so you'll see that to set the binary value it leaks over into the second byte (address 0x00AA03) since we need more bits to store that large of a value. The entire value would look like the following: 00000011 10000001 The Just wanted to point this out since it is different than our previous samples.

## **Passing Objects and Primitives to Functions**

Now, that you've seen that functions are objects it will be a bit more obvious that we can pass a function as a parameter on a function, just as we can pass an object to another function.

Since, we haven't examined it closely, let's take a look at how that passing a Primitive type is different than passing a primitive type like a Number, Boolean, etc.

Again, you will see that this will be much more clear to you, because you understand the memory model – the way JavaScript (and subsystems) allocate memory for each of these types.

function double(inNumber)

{
inNumber = inNumber * 2;
}
View this sample at plnkr.co:
http://plnkr.co/edit/lD3b4BbmLgXzjnqTdujI?p=preview

Below is the code for this example, which you can run at:

http://uncoveryourlife.com/LearnJS/RunAnyJs.htmvar el =

document.getElementById("first"); var el2 =
document.getElementById("second"); var el3 =
document.getElementById("third");

var paramVal = 17;
function double(inNumber) {
inNumber = inNumber * 2;
el2.innerHTML = "inNumber, inside double(), is " + inNumber;
}

el.innerHTML = "paramVal, BEFORE being passed to double(), is " + paramVal;
double(paramVal);
el3.innerHTML = "paramVal, AFTER being passed to double(), is " + paramVal;

This sample, simply creates an application variable named paramVal which we use to pass in to our double() function.

Inside of the double() function we do not create a new variable, but instead, just set the value of inNumber to double its value.

Then, when we return from our double() function we see that our paramVal still has the value it was originally set to (17).

## **Primitive Type Parameters Have Function Scope**

That's because the memory for the inNumber primitive is created in the double() function scope.

Let's take a look at the memory model for the previous code to get an idea of what is really happening. Examine Figure 25: Passing a primitive to a function and I'll explain what is happening below.

![](images/00025.gif)*Figure 25: Passing a primitive to a function*

http://NewtonSaber.com/OOJavaScript/Images/Figure25.png

**Note**: the value ofinNumberin Figure 25 is 34 (the value after the function has run).

After examining the memory model you can see that

1\. The paramValis created as an application-wide variable – (in orange color)paramValhas its base address at 0x000CCF0.

2\. The parameter is created as a primitive which is scoped to the function object double(). In other words, inNumbergets a base address (0x00AA02) that is created within thedouble()function.

3\. Since, inNumbergets its own memory the value **does not affect the original value** (paramVal) which was sent in to thedouble()function.

You may believe that seems quite obvious, however, lets change our examination to what happens when you pass a Reference type to a function.

***Passing A Reference Type to A Function***

Let's leave most of our previous example the same as it was. Instead, we'll just add a new object which will contain the primitive which we will pass in to thedouble()function.

The JavaScript to create the new application object will look like the following:
var container = {}; // create object
container.paramVal = 17;

Now, instead of passing theparamValitself, we will pass the entire container object to the function.

Now, the function call will look like the following: double(container);

That means we are passing an object to the function so we'll have to alter the code in the function a bit to get the primitive out of the object. It'll look like the following:

inNumber.paramVal = inNumber.paramVal * 2;
inNumberis now an object, simply because we passed that type in.

Below is the updated code which you can run at the RunAnyJS page or you can check out the code at the plnkr.co:

http://plnkr.co/edit/C8RRuFvHL7ALVgLlvMvw?p=preview

var el =
document.getElementById("first"); var el2 =
document.getElementById("second"); var el3 =
document.getElementById("third");

var container = {};
container.paramVal = 17;
function double(inNumber) {

inNumber.paramVal =
inNumber.paramVal * 2;
el2.innerHTML = "inNumber, inside double(), is " + inNumber.paramVal; }

el.innerHTML = "paramVal, BEFORE being passed to double(), is " + container.paramVal;
double(container);
el3.innerHTML = "paramVal, AFTER being passed to double(), is " + container.paramVal;

If you run that code, you will now see some output which looks similar to the following and is attempting to show you that **the primitive value of the passed object is altered by the double() function**.

### paramVal, BEFORE being passed to double(), is 17 inNumber, inside double(), is 34 paramVal, AFTER being passed to double(), is 34

Because we have gone through this in memory, you may understand why the Object type is altered. Figure 26: Passing Reference type : part 1 shows this in memory. Notice that the contain.paramVal has a value of 17 – before the double() function is called.

![](images/00026.gif)*Figure 26: Passing Reference type : part 1*

http://NewtonSaber.com/OOJavaScript/Images/Figure26.png

***Reference (Base Memory Address) Is Passed To Function*** When the function is called, the reference to the container is passed. We can think of this reference as the base memory address of the container variable (Object)l.

That means that the inNumber parameter refers a memory address where the object can be found which will then be able to get to the primitive value which is stored inside it.

***Value Changed, Because Memory Address Is Same***

That is why the value is changed. In the previous example, with the primitive we saw that we had two memory locations (one for each primitive). However, since we've passed a reference to the container object, we now have one memory address for the primitive (scoped to the container object).

That means when we change the value, we are changing the value inside the original container object.

Shows step 2 of the process – after the function changes the paramVal inside the container object.

![](images/00027.gif)*Figure 27: Passing Reference type: part 2*

http://NewtonSaber.com/OOJavaScript/Images/Figure27.png

***Summary of Pass by Reference Versus Pass By Primitive***

The value with the box around it is now 34, whereas previously it was 17\. When you pass by reference (by object) you manipulate the memory of the object that you passing.

However, when you pass a primitive (by value) you are only passing the value and new memory is created to store the value.

Now that you know you will get different results when passing Reference types versus passing Primitive types you will understand how JavaScript is manipulating these types in memory and you will better understand how code executes.

Now our phrasing is going to get a bit odd, because we are going to talk about passing a function to a function. Doesn't that sound a bit odd? I think it does.

## **Passing Functions To Functions**

Now that you know that you can pass an Object to a function and you know that a function is an Object you will be able to understand one of the most confusing things in JavaScript and in the Computer Science world: passing functions to functions.

***Functions are Reference Types***

First of all, at their roots all functions are objects. That means they are reference types. That means when you pass the function, you are passing an address to its base address in memory: just like an object.

I repeat this simply because this is all tied up with our understanding of scope. The function creates a scope for all those variables it wraps, just as an object does. However, when you pass the function into a function you will get the base address of the function and be able to manipulate the values located at those addresses, which means you will alter the object (function) that is passed in to the function. All of this means you need to be careful and know exactly what you are attempting to do.

However, at this point you might wonder, "why would I ever want to pass a function to a function?" It does seem to be an odd thing to want to do, but it is how numerous built-in JavaScript functions work, such as thesetTimeout() function.

## **setTimeout – Pass A Function**

The global window object in JavaScript has a setTimeout() function which you can call to invoke a function at a later time.

setTimeout takes two parameters. The first one is a function and the second one is the number of milliseconds to wait before the function is called. The function you pass to the setTimeout represents the commands you want to run when the timer fires after N milliseconds.

setTimeout(functionName, millis);

Here's a quick example you can try or watch.

var el =
document.getElementById("first"); el.innerHTML = "After 3 seconds (3000ms) you will see another message.";
var el2 =
document.getElementById("second"); setTimeout(showAnswer, 3000);

function showAnswer()

{ el2.innerHTML = "It has been
approx. 3 seconds, since I was told
to run.";
setTimeout(hideAnswer,3000);
}

function hideAnswer() {
el2.innerHTML = "";
setTimeout(showAnswer,3000);

}

You can watch a similar sample at my plnkr.co: http://plnkr.co/edit/BJn9UZiYpSWu34ydRCR7?p=preview

I've made this script call the setTimeout() method in two different places so that after the text appears it will disappear and then when it disappears, it will appear again. That way you will be sure to see it all happen.

Now you can see at least one reason (and there are many more) to pass a function to a function let's go ahead and take a look at how we can create a function that takes a function as a parameter and uses it.

## **Architectural Principle Revealed In Passing Function**

This next example will subtly reveal an architectural principle to you while we look at passing a function to a function. Here's the initial code.

function displayData(item)

{
alert(item);
}

function mainWork(targetFunc) {
var allThings = [];
allThings.push("thing1"); allThings.push("thing2"); allThings.push("thing3"); allThings.push("thing4"); for (x in allThings) {
targetFunc(allThings[x]); }
}

mainWork(displayData);
If you go to the Plunker for that code or run it using RunAnyJS you will immediately learn that it is quite annoying, because it uses an alert() modal dialog box to provide the user with information.

http://plnkr.co/edit/cVmbtIeYVqDXUEuIdLvr?p=preview

## **A Callback Function**

Notice that the mainWork method takes a function that it will later use to display the data to the user. This is the computer science concept – albeit a very simplistic example – of a callback function. That means, the functionality which will be called or used by another function is separated out so it can easily be replaced.

***Separating Functionality To Replace Later*** Since it is a function that we pass in, we can replace our displayData function with any compatible function.

***Replacing Functionality With Less Testing***

Now, instead of forcing all of the code in mainWork to be retested because we change something in it, we can just replace the displayData function and we only have to test to insure that the replacement function works.

This is a huge architectural principle and gets you closer to designing architectural solutions rather than just pasting some scripts together.

Let me show you how it works with the following sample. Basically we add a new function named
displayDataViaDiv(item);

That function is simple and basically says just append the value of item to the DIV's text.

function displayDataViaDiv(item)

{
el.innerHTML += " " + item;
}

Finally, we simply change the original call to
mainWork(displayData) with the new one to call our new function mainWork(displayDataViaDiv);

That's it. Now it will display the data in the DIV instead of those annoying pop-ups.

The entire code listing is below so can try it. Or run this Plunker and check it out:

http://plnkr.co/edit/BKK6RhEmXFnyILPE8f8Y?p=preview
function displayData(item)

{
alert(item);
}
// initialize our div for output
var el =
document.getElementById("first");
el.innerHTML = "";

function displayDataViaDiv(item)

{
el.innerHTML += " " + item;
}

function mainWork(targetFunc) {
var allThings = [];
allThings.push("thing1"); allThings.push("thing2"); allThings.push("thing3"); allThings.push("thing4"); for (x in allThings) {
targetFunc(allThings[x]); }
}

mainWork(displayDataViaDiv);

A few things to notice about this new script are:

1\. The old displayData function does not have to be deleted or altered. That means the old functionality can run as it did. Now, we simply implement the new functionality. This is great for ongoing development because we don't break old code.

2\. We still have to keep our function's public interface the same. This just means that the function still takes an item and that item is a string in this case. If we had really wanted to separate this out then that type could have been a base type (top of an inheritance chain) and the type would implement a specific interface that is known and always the same. We'll learn more about this as we look at dependency injection, but I thought I might just mention it here.

Now, before closing this chapter I'd like to return to that old phrase, *functions are first-class types*.

## **Functions Are First-class Types**

In other languages, functions are not objects nor do they really have their own type. So in those languages functions are not considered first-class types. They are second-class citizens who are not formally recognized.

As a matter of fact, in C++, Java, and C# they aren't types so it is difficult or impossible to pass a function to a function.

C++ (along with C) implemented a pointer so you could pass a function to a function. A pointer is C++ is simply an address which you can pass. That address may *point to* any type (integer, string, or function). However, the syntax was quite ugly. For example if you had a function named getDouble, which returned nothing (void) and took an integer your function pointer would look like the following:

void(*ptrName)(int*); // this creates the ptrName variable
// to set the pointer to point to the function you'd do this
ptrName = &getDouble;

That last line with the & (ampersand) means, get the address where the function named getDouble exists in memory and save it in the ptrName variable.

That's about enough of that ugliness.

## **JavaScript Makes It Easier**

I just wanted to mention that JavaScript makes it a whole lot easier since you can pass the name of the function as the function parameter.

Now that you understand all of these very important, but rarely explained details about Objects in memory, it will now be much easier to understand how we can use JavaScript functions to create templates (almost like classes in Java, C++ and C#) for common UDT (User Defined Types) that we want to re-use in our applications.

## **Create Template Objects For Instantiation**

First I'll show you the JavaScript you write to create a simple template object and then I'll show you how to instantiate it.

function Person(firstName, lastName, startDate, workTitle)
{

this.firstName = firstName; this.lastName = lastName; this.startDate = startDate; this.workTitle = workTitle; this.empId = getEmployeeId(); function getEmployeeId() {

return
Math.ceil(Math.random() * 5000000); }
}

To use the template we just created we use the JavaScript new operator. The code looks like the following:

var employee = new Person("elmer", "fudd","2012-03-14","manager");

You can see a simple script which uses this template object at: http://plnkr.co/edit/GWAq6VGkOyUOulVT8uys?p=preview

Because you understand how functions (and objects) are stored in memory, it will be much easier for you to understand what is going on here. There are just a couple of things you need to know about :

1\. the thiskeyword
2\. thenewkeyword

Those are confusing concepts when you haven't seen an object in memory, but again, since you have it'll all come together now.

Okay, so let's take a look at the template object in memory. It'll look something like what you see in Figure 28: Function As An Object Template.

![](images/00028.gif)*Figure 28: Function As An Object Template*

http://NewtonSaber.com/OOJavaScript/Images/Figure28.png

There are a number of things to examine closely in Figure 28\. 1\. The Person contains five properties and 1 function (shown in orange).

2\. I'm showing the string types as references, as they most likely are implemented that way since their sizes in memory fluctuate. (You'll see these go from null values to addresses in the next image.)

3\. I've initialized empId to 0 and each of the references to null although I am not sure exactly what values web browsers / JavaScript initialize these to. Keep in mind this is a simplified model to increase our understanding, not turn us into Computer Scientists.

4\. This is a view of the Person function before wenewup another object based upon this template.

Now, let's take a look at what happens in memory after the employeeobject is instantiated with thenewoperator.

## **JavaScript new Operator**

The new operator tells JavaScript that we want a new slice of memory that is not used by any other object.

***Create Person Object At New Memory Address***

When the JavaScript Interpreter comes across the following line of code it knows that it is not copying the Person object into a new variable, but it will create an entirely new Person Object at a new memory address.

var employee = new Person("elmer", "fudd","2012-03-14","manager");

Instead of copying the address of the Person function into our employee variable, the Interpreter will now take the Person object and create a new on at another memory location and return that address. That means, the memory will now look something like what you see in Figure 29: New Object Means New Memory.

![](images/00029.gif)*Figure 29: New Object Means New Memory*

http://NewtonSaber.com/OOJavaScript/Images/Figure29.png

The blue area on the right in Figure 29 represents the object at the moment it is instantiated and before it is initialized (by the values sent in the parameters). You can see that there is a new chunk of memory set aside for this new object. Of course, from our previous investigation you now understand that means you have a new entity in memory instead of just a another reference to the same memory the Person template points to. This is a significant difference in your JavaScript programs, since you will not be overwriting memory that is used by another object.

## **What About this?**

The initialization is where thethisoperator comes in to play.

Now that new memory has been set aside for this object and the object has been instantiated in memory it is a common thing to want to initialize values in the new object so that it is ready to represent a real-world thing, such as an employee with a name and employeeId.

## **Construction: Automatically Running Code**

When the new object is created in memory a one-time construction process occurs as the code which is not wrapped in another function automatically runs.

In our case the code that automatically runs is the following:

this.firstName = firstName; this.lastName = lastName; this.startDate = startDate; this.workTitle = workTitle; this.empId = getEmployeeId();

Just as it does in a normal function, the code runs from the top down, unless it is wrapped in another function – as in the case with ourgetEmployeeId()function.

Also, consider another point: there is no way to run the lines above again, after the object is instantiated.

***Constructor Runs Only Once Per Application***

Do you see why? The answer is because there is no way to access those lines again. You cannot refer specifically to those lines from anywhere else in the program. This becomes the constructor code for our new object which is built off of the template object.

In contrast, notice that you can run the getEmployeeId() function any time simply by writing the following JavaScript code:

employee.getEmployeeId(); // returns random number

Take a look at Figure 30: New Object Initialized Using this Operator and you'll see the initialized employee object in memory, while the original template object has not been altered. You can see the changed values in the boxed area of the blue object.

![](images/00030.gif)*Figure 30: New Object Initialized Using this Operator*

http://NewtonSaber.com/OOJavaScript/Images/Figure30.png

I set the value of the empId to 7 just for our example. The function that sets that value simply generates a random value between 1 and 5,000,000.

***More About this***

The this operator is really a short-hand way that JavaScript allows you to use to refer to the base memory address. When you call this inside the object, you are saying, go ahead and look at this object and add a property named firstName and set it to the value that came in (named firstName).

***Reference From Inside An Object***

You need the this operator, because there would be no other way to refer to the object that you are currently inside of. Outside the object we refer to it as the employee object, but within the object itself we refer to it as the this.

That means that anything you do to the this object you are doing to the object itself.

## **What About getEmployeeId Function Address?**

You may have noticed that in the template object ( Person) and the new object (employee) I decided to set both of the addresses which point to the getEmployeeId function to the same value (0x2CFC01). I did that because it makes sense to me that the Interpreter would be smart enough to see that those are the same functions since they are going to do the same work and that the Interpreter would do this optimization to save memory. Otherwise, it would have the same function loaded into memory at different addresses that each object (Person and employee) would then refer to. That seems like a waste of memory to me.

## **Summary**

Now that you understand how objects are created in memory, how to create template objects and how to use the new and this operators you are ready for even more and I'm sure you're finding that your understanding of JavaScript has expanded exponentially in your mind.