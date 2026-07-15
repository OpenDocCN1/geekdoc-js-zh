![](OEBPS/cover.jpg)

## Table of Contents

Chapter 1JavaScript Introduction

Chapter 2Syntax

Chapter 3Components of a statement

Chapter 4Computer memory

Chapter 5Data Types

Chapter 6Functions

Chapter 7Conditional Statements

Chapter 8Loops

Chapter 9Arrays

Foreward

What makes me qualified to write a book on JavaScript?

I am a full-stack web developer who has been working in the industry for many years. The term full-stack simply means that I am experienced in bringing a product from concept all the way to completion. I have worked as a lonely contractor and worked my way up into the corporate world.

As a web developer I have worked with front end and back end languages. JavaScript, which is a front end scripting language, has become one of my strongest assets.

My experience with JavaScript and understanding how it fits in the bigger picture of web development makes me uniquely qualified to write this book.

Who should you read this book?

This book is meant for those who have a basic understanding of HTML, but know nothing about JavaScript. This book will focus on JavaScript fundamentals. This book is a completely separate course for those looking to learn JavaScript.

Why should you read this book instead of the countless JavaScript books out on the market?

This fundamentals course has cut out a lot of the extra stuff that tends to distract beginners from learning JavaScript. If you want a course that presents the material with a focus on eliminating convoluted concepts better suited for a more advanced course then this book is for you. By the end of this course you will be able to code JavaScript, but more importantly you will understand the underlying foundation of JavaScript. Ultimately, understanding JavaScript fundamentals will make you a better programmer and open you up to even more opportunities in the work place.

Chapter 1

## JavaScript Introduction

What is JavaScript? JavaScript is a scripting language that can be used to make web pages interactive. JavaScript is not a programming language. Programming languages are compiled from a higher level human readable language into machine code. Instead, JavaScript is interpreted by web browsers, like Google Chrome, Firefox, Safari, and Internet Explorer. So instead of directly compiling into code that the computer can understand, JavaScript is interpreted. This means that different browsers may interpret the script differently than others. This is a common obstacle web developers have to deal with when attempting to create cross browser solutions.

JavaScript is not the only thing the browsers interpret. In fact HTML, and CSS are also interpreted by the browser. These 3 languages are considered client side languages. This is because these languages are interpreted on the client side machine opposed to the web server. Other languages are processed by the web server; these are known as "Server Side" languages. In fact, server side languages are processed before the server "serves" the web page to the browser, while client side scripts are processed after the browser receives the served web page. This means that the server is not slowed down by executing JavaScript commands. JavaScript is a great way to add logic to your website without eating up server resources. 

JavaScript uses syntax similar to other languages you may have heard of: like C#, C++, and Java. Even though the syntax is similar, I would like to note that JavaScript is exactly like those other languages. While this is more of an advanced concept, JavaScript is known as a prototypal language. For the purpose of this fundamentals course it is enough to know that it is unique. Ultimately, instructions are written in either procedural form (in sequential order, step by step), functional form (encapsulating reusable sections of code inside a function), or a mix of the two. We will talk more about this later on in the fundamentals.

## JavaScript code editors

You do not need special software to work with JavaScript. In fact you can write JavaScript in any standard notepad or word processing software, many of which come preinstalled on your computer. While these programs are sufficient for writing JavaScript, there are some more robust web development software programs that can be better used to code in JavaScript. Many of these are offered completely free. One of these is notepad ++, a free web development program that offers tools like syntax highlighting, macros that allow you to record actions and then replay them at the push of a button, and even third party plugins for added extensibility.

Notepad ++ is the program that I have chosen to use when taking screenshots of code examples. This does not mean that this is the best web development software available. I chose it because it is FREE, very simplistic with a low learning curve, fast because it is not bloated with extra bells and whistles, customizable with plugins and extensive preferences. Another very important reason I chose this software is because it is open source, meaning that it has a community of developers constantly working on improving it. I personally prefer using open source software as a philosophical position. With all of that being said, Notepad ++ does not have the greatest UI design, and looks very much like it was build 2 decades ago. Many good developers have chosen to use different software simply because of how ugly Notepad ++ looks. No one wants to looks like they are behind the times.

Notepad ++ is only for windows operating systems, which means a large portion of the web development community will not be able to use this software. For this reason I would like to mention a few other web development programs that are commonly used in the industry. Atom, which is another free open source code editor with a modern UI. It is supported on all major operating systems. Atom is a great code editor. You may be asking why I didn’t use Atom instead of notepad ++. The main reason is that is a fundamentals course, focused on teaching JavaScript basics without encumbering my readers with a large number of extra features. This means that I consider all of cool modern features that come preloaded in Atom a distraction during this fundamentals course.

Another very common software that is used across the industry is Adobe Dreamweaver. This is not a free program neither is it open source. It does offers a great deal of tools to assist web development. Among which is a more visual coding environment, with drag and drop features. While I understand why many people prefer to use this software, I have found this program to be very slow and bloated. Code generated by Dreamweaver tends to be bloated as well, and the code format is not always industry standard. I would not recommend Dreamweaver.

It is also important to note that enterprise level organizations that incorporate more robust team development methods, like agile development, will use advanced development software. The most common software in this case is Visual Studio, which is also not free nor open source. Of all of the paid coding environments commonly used across the industry, this is the most powerful.

No matter which code editor you use, JavaScript is the same. I encourage you to investigate the many options that are available to you, and pick the code editor that best fits your needs as a developer. There are no right or wrong choices. JavaScript can coded in all of them. Once you have made your decision, you will need to download and install your editor.

## Client side web development workflow

Now that you have a code editor I would like to discuss the basic workflow you will experience when following the examples found in this book. JavaScript can be run directly from your local machine. Well, most of JavaScript can be run locally that is. What do I mean when I say “run from your local machine” you may be asking yourself? You see, web development requires you to eventually put your code on a web server. This “server” is a computer that makes itself available to other computers across the internet. A web server receives requests from outside computers. The server then responds to those requests by serving them a web page. This is why they are called servers.

Think of them as waiters at a restraint. A guest sits down, and looks at the menu. When they are ready they request something from the menu. The waiter receives the request and then goes to the kitchen to gather the items the guest has requested. Once the waiter gathers all of the requested items they serve them to the guest. In the same way a web server receives requests from guests, and then gathers the requested items serving them up to the guest. This is a simplified explanation of how a web users makes a request for a web page and how the web server responds by serving up the requested page.

Like I mentioned earlier, JavaScript can run locally. This means that you do not have to have your code on a web server for you to see it. While you can view it locally, no one else across the inter webs can see it. For this reason, working locally is one of the best ways to review as is it gives you a chance to review your code before it is deployed to a web server.

Ultimately, for others to enjoy your awesome JavaScript your code needs to be deployed to a web server. However, the basic concepts of JavaScript can be illustrated without delving into to nuances of how to get your code on to a web server. As web deployment is a more advanced topic, it reaches beyond the scope of this fundamentals course. For the purpose of this fundamentals course the examples in this course have been optimized to run locally.

The JavaScript code in this book is written inline, which is to say that it is in the same file as the HTML markup. This is definitely not the best practice, but it is the easiest way to illustrate JavaScript basics. I do not recommend coding inline. Once you have mastered the basic concepts of JavaScript I recommend looking into JavaScript best practice. This will include writing your JavaScript code in external js files.  This allows you to keep you static HTML markup clear of dynamic code. Keeping these separate is very advantageous. While this is the true, it is one more thing that can distract someone who is just starting on their JavaScript journey. For this reason I have decided to go against convention and common sense in order to better teach the basics of JavaScript.

## Your first JavaScript web page

Now that you have a very basic grasp of what JavaScript is let’s make our very first web page. Start by creating a blank text file, with the “.html” file extension instead of the “.txt” file extension. Type the following into the html page.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAl3AAAAJDU0NmZiYTUxLTU2NTYtNGZiZS05MmI3LWFkOWM3NzY2ZTAyYQ.png](Image00000.jpg)

This is the basic HTML 5 structure. Next add a script tag into the body of the page at line 7\. This will be the container in which we will write our JavaScript.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAfaAAAAJDk5YTI5ZGVkLTk2ZmEtNDFjZi1iNmI3LWNmODY1YjgyMThmNA.png](Image00001.jpg)

Between the open and closing script tag on line 7 we will begin to write our script. Traditionally the first program beginners are instructed to write is a hello world program. This is a program that simply writes the phrase "Hello World" to the screen. In JavaScript this can be done multiple ways, but the easiest is using a built in function in JavaScript called “alert.” This is a function that has 1 parameter, and it creates a pop up alert window and displays the content of the passed parameter inside that pop up.  Let's take a look at the hello word script (fig. 3).

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAhrAAAAJGQ0MjJjNmYwLTZjNTItNGJlYi1hNjVhLTZhODc3M2M2ZmI0Ng.png](Image00002.jpg)

This is all it takes to write your first JavaScript web page. If you were to save this file with the html extension and run it in your browser you would notice a pop up that said "Hello World" (fig. 4). To run this you can either double click on the html file or drag and drop this file into an open web browser.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAfjAAAAJGNjMDBiZjhiLTVlYTAtNDBjZi1hNGZkLTdmYzk5OWFhZTVkMg.png](Image00003.jpg)

Chapter 2

## Syntax

If you search the word "syntax" in google you will get the following quick definition.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAjhAAAAJDRmNjg3ZmFiLTkwN2UtNDIzMC04MDVhLWQ3MmQ2ZjZmYWZmNw.png](Image00004.jpg)

Ultimately, syntax describes how a computer language forms an instruction. Let’s take a look at our hello world script as our example.  For now we will be focusing only on the portion written between the script tag, line 8.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAkdAAAAJDdkZmIwYTY1LWMxODgtNGQyZC1hMTg4LWE1ZmE4YTBhY2E5Mw.jpg](Image00005.jpg)

Remember that our hello word web page had only 1 instruction. It told the browser to create a pop up alert window with the text "Hello World" in it. A single instruction is knownas a statement. In JavaScript statements end in a semicolon. Statements can instruct the browser to do a wide variety of things, like define a variable, assign a value to a variable, call a function, check to see if a condition is met, and much more. For now focus on the order of the words in the statement.

## Well-formed statements

What do you think would happen if we moved the location of the semicolon to be between the function name and the parameter list? This is a great example to try for yourself.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAhjAAAAJDlhYWFkNTc3LTYzZmMtNDc1OC05YjIxLTg1NDE4OWZkY2E0Yg.png](Image00006.jpg)

If you created the above webpage and opened it with your browser your browser would not have created the pop up alert as it did before. This is because the statement is not well formed, as the semicolon was in the wrong place. If you were to take the words in this sentence and move them around at random the sentence would no longer have the same meaning. In fact the sentence would likely be gibberish, and hold no meaning at all. An important fact to remember is that computer's don't do very well with gibberish. When a human reads a nonsensical sentence, like the following, they can skip over it:

"gibberish very well do don’t computer’s with."

However, when computers read gibberish they are unable to skip past the nonsensical instructions. When this happens, the program usually experiences an error which causes it to stop reading all together. This concept of having well-formed instructions, is important if you want to have code that will run from beginning to end without any errors. We will cover debugging JavaScript later in this course, but for now try to understand that the order in which an instruction is constructed (syntax) is vital.

## Whitespace

JavaScript ignores whitespace, the empty space between parts of a statement. Whitespace is comprised of spaces, tabs, and line break character. However, please note that whitespace inside a quotation, also known as a string literal, is not ignored. To illustrate how JavaScript ignores whitespace, let us compare some JavaScript statements.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAgHAAAAJDg2OTE2MDc4LTgyYWMtNDE4ZS05YjUxLTNmMTcwMjllY2VmMQ.png](Image00007.jpg)

Notice in line 1 we have our hello world script. I have duplicated this line 2 times and added in some whitespace. In line 2 there are spaces and tabs between the word "alert" and the string literal warped in parenthesis, as well as the semicolon. On lines 3 and 4 a carriage return was entered between the word "alert" and the remainder of the statement. All three of these statements are identical to JavaScript. 

## Case Sensitive

JavaScript is a case sensitive language. This means that JavaScript detects if a letter in part of a statement is upper case or lower case. A lower case letter is not the same as an uppercase letter, and by simply changing the case of the letter you are ultimately telling JavaScript a completely different instruction. This primarily affects how you name things in JavaScript, and is the bane of many a programmer. Often time bugs in code are simply a letter in the wrong case, and can be hard to detect as our minds tend to skip over the case of a letter. 

## Code Blocks

Sometimes statements need to be grouped together, as in a function or when dealing with conditions. When grouping statements together they are wrapped in curly braces "{" and "}". 

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAlbAAAAJDRhMmE1MzJhLWQwYTAtNGY5Mi05ZTkxLTQ5OTI3NzhhYTlhYQ.png](Image00008.jpg)

If we look at lines 8 to 11 we can see our first custom function, which contains 2 statements. We are not ready for functions just yet, but notice how lines 9 and 10 are wrapped with the curly braces (end of line 8 and beginning of line 11). This means that the statements are grouped together. Any time that this function is called, it will perform all the statements in the group in sequential order. Code blocks are essentially what they sound line, block of code that are grouped together.

Often times it is the case the fixing errors is a way of life for programmers. Like with any craft, the better you know your tools the better you will be at using them. These 4 concepts of JavaScript syntax will be useful in writing code without errors. 

Chapter 3

## Components of a statement

There are 5 components of a JavaScript statement: Values, Expressions, Operators, Keywords, and Comments.

## Values

There are two types of values in JavaScript. We mentioned a string literal in our last lesson. A string literal is the value of a string represented literally. Similarly, a literal value is the value of a specific data type represented literally. All value types can be represented in literal form. Values can also be stored in the computer’smemory, in a placeholder called a variable. 

In most programming languages, including JavaScript, you have to declare your intent to store data in memory by associating it with an identifier. This is known as declaring a variable, and ultimately it allows the computer to set aside a predetermined amount of space to be used as a storage container for data. It is also important to point out at this point that values are represented in memory as different data types. Primarily a data type defines how much memory a value takes up. We will cover this in greater detail later on.

Literal values cannot change. The number 7 is a literal number value. It will always be of the numerical value 7\. It will never be equal to 8, neither will it be equal to the string value of "seven." Literal values are often used when setting the starting value of a variable, a practice called initializing a variable.

Unlike literal values, variables can change. If I were to declare a variable called myVariable and initialize it at a value of 7, I could later assign that same variable a different value. Let’s take a look at what literal values and variables look like in JavaScript.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAcvAAAAJGE4OGYyNGZhLWI0YTMtNGNhNy04ZWMyLTcwMTFlMzM2YTE1Mw.png](Image00009.jpg)

Notice on line 9 we are setting the value of myVariable to be equal to the numerical value 7\. Immediately after that, in line 10, we are setting myVariable equal to 8\. The value that is stored in memory starts off as 7 but will be 8 when the script is done. 

## Expressions

An expression is part of a statement that returns a value or evaluates to a value. A statement can contain 1 or more expressions in it.  Expressions contain operands and operators. An expression is a shorthand function that performs an operation on operands. The shorthand has a left hand operand, an operator, and then a right hand operand. In the Expression A + B:  A is the left hand operand, B is the right hand operand, while + is the operator.

The following are example expressions:

1 + 1 is an expression that returns the numerical value 2.

1 > 2 is an expression that evaluates to a Boolean value false.

"Hello " + "World" is an expression that returns the string value "Hello World". 

## Operators

An Operator is used to indicate which operation should be performed in an expression. There is another factor that determine what operation is performed, and that is the data type of the operands. If A and B were both numerical values then the + operator would indicate an operation of addition. If either the A or B operands were of type string this would indicate anoperation of concatenation (combining multiple strings together). For an exhaustive list of operators I suggest using [w3schools.com ](http://www.w3schools.com/jsref/jsref_operators.asp)as a reference. 

## Keywords

Keywords are reserved words that have specific meaning to the JavaScript language. The keywords cannot be used as identifiers, as they already are associated with elements at the core of the language itself. In our previous example (fig. 1) we were already using a keyword to declare our intention of storing a value in memory. Notice on line 8 the keyword var, which is short for variable. We use var to declare a variable in JavaScript. We will go over specific keywords as they naturally are of use to us during this fundamental.

## Comments

Comments are lines of text that in JavaScript that are not executed by the computer. They are used to explain complex code. There are two ways of inserting comments in JavaScript. The double forward slash // at the beginning of a comment will make all text that appears after it on the same line a comment. You can also wrap text with the /* and */ characters to mark all text between them as a comment. This method of commenting, unlike the first, persists beyond the end of a line and can span multiple lines.

## Tying it all together

You may be asking yourself why you would want to store a value in memory. Let’stake a look at a more practical script to illustrate the usefulness of variables (fig. 2)

![](Image00010.jpg)

In the above script we are declaring a variable called myName. Next we are calling the function prompt. Prompt is a built in JavaScript function that will show a popup window with a text box and a question or prompt to the user. Once the user enters in their response in the text box and clicks the "Ok" button the value that the user typed is returned. We are then assigning our variable myName to be equal to the value that the prompt function returned. The script continues to the next statement, which calls the alert function. We are familiar with what the alert function does, but notice how I am concatenating (combining) the two string values together. What do you think will appear in the alert box?

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAjpAAAAJDY5MmYwOTJhLWZmNjMtNDIwZC05YzdjLWVkZGYzZGRiMWZjZA.png](Image00011.jpg)

When I opened this page and filled out the prompt with my name it remembered what I typed in. It then used that value in a later instruction to alert the welcome message "Hello, Brennien Coker” to the popup

I have presented the all the components of a statement. While this lesson was a bit lengthier than previous lessons I am confident that your brain did not melt. Feel free to wear shirts that gloat of your programming prowess.

Chapter 4

## Computer memory

In the last lesson we said that values are stored in memory as different data types, and that this is what determines the amount of memory that is used to do so. Let’s take a moment to understand how a computer stores values in memory.

## Decimal System

In modern times we represent number values with the decimal system. These are numbers as commonly used in your everyday life, and the numerical characters are: 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9\. The decimal system uses a base of 10, which means that a single digit can represent 10 unique values. 

In order to represent a value larger than the 10th character, which is the number 9, you will need to use 2 digits. For example 9 + 1 = 10\. Notice that the number 10 is represented by 2 digits. Now we don't typically look at numbers this way. Most of us have learned to do this so well it is all automatic, but let’s take a look at how the value is represented by the decimal system.

The value of each digit is calculated by a basic formula, and then those values are added together at the end. First we look at each digit like it is a list written from right to left. The first thing we need is the digit's position in the list. To calculate the digit's position we count to that digit starting from the right most digit, and then subtract 1\. We do this because we were taught to count starting from the number 1, but the first numerical character is actually 0\. This gives us the digit's actual position. We then raise the base (which is 10) to the power of the digit's position. This gives us the base of the digit. We Next we multiply the digit base by the digit value. This gives us the value that particular digit represents. We do this for all the digits, and add their values together.

Take the decimal value 10 as example, the left most digit is the 2nd position in the list. 2 minus 1 give us the digit's actual position which is 1\. The decimal system base 10 to the power of 1 is equal to 10\. 10 times 1 is 10\. The next digit in the list is in the 1st position. The digit's actual position is 0\. The base 10 to the power of 0 equals 1\. 1 times 0 equals 0\. Finally we add all of the digit values together. 10 plus 0 equals 10. Let’s write this out so we can see this easier.

10 = 1 * (10^1) + 0 *(10^0) simplified to 10 + 0 = 10

## Binary System

Computers work in a similar system to represent values, with 1 major difference. Instead of using a base of 10 it has a base of 2\. This system is called the binary system, and its numerical characters are 0 and 1\. A single character in binary is called a bit. In order to represent the value of 10 you need 4 bits.

10 = 1 * (2^3) + 0 * (2^2) + 1 * (2^1) + 0 * (2^0) simplified to 8 + 0 + 2 + 0 = 10

This indicates to us that 10 is represented as 1010 in the binary system. Computers group 8 bits together, much like we group letters to form a word. Groups of 8 bits are called a byte, which is the next standard unit of measure in computer memory.

With a single byte, you can represent 256 unique values. How do you think we represent values that are greater than 256? We group bytes together, of course. Data types are standardized groupings of bytes that can be used to store a variety of values. Before we discuss the different data types there is one more key feature of data types that needs to be understood, and that is non numerical values.

## Non Numerical Values

Non numerical values are stored in memory using the binary system. However non numerical values are translated from a numerical value into some other type of value. Textual values, or enumerated values for example.  During translation the computer uses a predefined key to determine what the numerical value should be represented by. The key associates specific numerical values to specific non numerical values. This is most common in the non-numerical value char (short for character). Char values store a single letter of text. Most programming languages use char values and translate them using the ASCII key. [The ASCII key](http://www.ascii-code.com/) is a standardized key that associates common text characters to numerical values. For example, the ASCII key associates the decimal value of 65 with the "A" symbol, and the decimal value of 97 with the "a" symbol.

Chapter 5

## Data types

There are 6 data types in JavaScript: Boolean, Number, String, Null, Undefined, and Object. The first 5 are said to be primitive data types, while the last is a composite data type. In today's lesson we will be going over the first 3 primitive types. Burt first let’s do a quick review of what we know about data types already.

If you remember in lesson 3 I mentioned that you need to declare your intent to store a value by associating it with an Identifier. This process is knownas declaring a variable. This is done using the var keyword in JavaScript. The keyword var is short for "variable", and is followed by the variable's identifier. It is like telling JavaScript "Hey JavaScript! Create a variable with the following name."

![https://media.licdn.com/mpr/mpr/shrinknp_400_400/AAEAAQAAAAAAAAeiAAAAJDIxYjVjMTVmLWVkOTItNDZmNy1hZDMxLWQ1MmM3ZmQ3NDZjZQ.png](Image00012.jpg)

Once a variable is declared a value can then be assigned to it. The process of setting the initial value of a variable is called initializing the variable. We use the assignment operator = in JavaScript to assign a value to a variable. This is like telling JavaScript "Hey JavaScript! Create a variable with the following name and then assign it the following value."

![https://media.licdn.com/mpr/mpr/shrinknp_400_400/AAEAAQAAAAAAAAhYAAAAJGIxODYxZWZhLTM5OGQtNDU2YS04YzNkLWEwYjk1MGYwZGNjMg.png](Image00013.jpg)

In JavaScript you can combine the declaration and initialization processes into one statement.

![https://media.licdn.com/mpr/mpr/shrinknp_400_400/AAEAAQAAAAAAAAktAAAAJGRjNTgxOWU0LTYzNGQtNDFlNS04YTdhLWY2ZDk0M2U3NjJhNg.png](Image00014.jpg)

Note that the variable will conform to the data type of the value assigned to it. 

## Boolean

The JavaScript Boolean data type is a non-numerical value, thattranslates a single bit from a 1 or a 0 to true or false respectively.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAfTAAAAJDM2NjljOGZiLWE2NTctNGJlMS05MjlkLTkxNTNhNjkwNzkxNg.png](Image00015.jpg)

## Number

The JavaScript Number data type is a numerical value that is stored using 64 bits. Notice that the JavaScript number is a double precision signed floating point. This means that not all 64 of the binary characters are used strictly to represent the value. In fact bits 0 to 51 describe up to a 17 digit decimal value. Bits 52 to 62 are used to represent an exponent that the decimal value is raised to. The 63 bit is used to describe the sign of the value, which is to say whether the value is positive or negative. Given this information, we are told that JavaScript's Number data type can be used to store values as large as 9,007,199,254,740,992 or as small as -9,007,199,254,740,992\. It can also handle decimals precise up to 17 decimal spaces, for example 0.00000000000000001 is the most precise numerical value JavaScript's number data type can represent. If you try to assign a value that is larger or greater, or even more precise than what the JavaScript Number data type can represent the web browser may throw an error.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAhtAAAAJGQ3Nzk3MWJhLTU4NzUtNGY2OS1iNTllLTM5ZDNiMmRiM2FjNw.png](Image00016.jpg)

## String

The JavaScript String data type is a list of characters. If you remember from our previous lesson we discussed characters. Characters are non-numerical values that use the ASCII key to translate a numerical value into a textual character. A character is 8 bits (1 byte) of memory which can represent 256 unique values. A string is a list of these characters. We will discuss lists and arrays later in this fundamental, but for now the thing to walk away with is that, theoretically, there is no limit to how many characters can be in the list. It can be a list with only 1 character in it, or a list of hundreds of characters in it. 

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAd4AAAAJDIyY2JlOTUyLTMzMTYtNGM4My05ODQ2LTRlNTNiZTA2NjcxMg.png](Image00017.jpg)

Today we covered the 3 most common JavaScript primitive variables. These are the bread and butter of the JavaScript world. With these 3 data types you will be able to write just about anything. There is much more to cover, but take a moment to recognize that you have made it through 5 fundamental JavaScript lessons. If I could commemorate this moment with a trophy or a colored belt I would. Perhaps you can celebrate your cerebral achievement by starting this day with a fresh cup of coffee, or tea. Go ahead; you have my permission to feel accomplished!

## Special data types

The Null and Undefined data types are sometimes called special data types. This is because the value they represent is always the same value. For example, if you were to declare a variable and initialize it to a string value that variable would conform the string data type. You could later assign that same variable a different string value. This is because the String, as well as the Number and Boolean, data types area able to represent a variety of values. 

## Null

The Null data type is used to represent a value of nothing. There is only one null value, unlike the other data types. 

When are you likely to work with a null value? Let’s say you wanted to create a function that would iterate through a collection of objects and return all the objects that are not equal to a specific object for example. Normally this function would return a collection that is a subset of the original list, but what would happen if the original collection only contained a bunch of that specific object. As the code iterated through the collection it would skip all of the items because they all match. There would be nothing to return. In that case, null would be returned. 

It is important to note that JavaScript has a well know bug with regard to the Null data type. The typeof operator is used to determine what data type a variable is, however, it returns "object" as the type for null. This is unfortunate, as null is considered its own data type.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAh3AAAAJGU5ODk5NmYzLTU3NWQtNDBkYi05MGRmLTc5YmIzNGVlYWI4OQ.png](Image00018.jpg)

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAgeAAAAJGFhMWI4OTY1LTcyOTctNDAxNy04N2YzLWRlZDE2YTQwNWY5Yw.png](Image00019.jpg)

## Undefined

 Much like Null, the Undefined data type can only represent one value. There is a difference between the nothingness of null and the value of undefined. The undefined value represents something that has no value. It is more like a placeholder value that stands in the place of values that should exist but for one reason or another they do not.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAluAAAAJDVhNDNmNWRmLTJjZTgtNDE4Zi1iMGI3LTVhYjNkMmE4YWI1OQ.png](Image00020.jpg)

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAleAAAAJDRhYTQ5MzY2LWUyMzgtNDBjYy04OGZlLWQxYzcxNGRjMGNmNw.png](Image00021.jpg)

After a variable is declared but before it is initialized that variable is of the data type Undefined, and has the value undefined. This is the most common occurrence of the undefined value. Once a value of a different data type is assigned to the variable, it conforms to that data type and stores that value. The undefined value is useful when checking to see if a function parameter was omitted. Instead of throwing an error, JavaScript will assign the variable the value undefined. Also, if a function does not explicitly return a value it will return the value undefined. Another way the value undefined is commonly experienced, is when you try to access an object's property that does not exist. Most other languages would throw an error, but JavaScript instead returns the value undefined.

## Object

Objects are central to object oriented programming (OOP), and JavaScript is a form of OOP. In the real world we are surrounded by objects and OOP is a way of taking concepts about the real world and applying them to the world of code. For example, an apple in the real world is an object. This apple has traits (attributes) that define what it is, like: shape, color, taste, size, weight, age, etc. This apple is different than all other apples in that it is a uniquely separate object (Identity). Even if you could duplicate this apple, and create an exact copy, this apple is not that apple. This apple can do stuff (behavior), like grow on a tree for example. While the deeper concepts of OOP are outside the scope of this fundamentals course it is important to note these three features of an object: Identity, Attributes, and Behavior.

Essentially objects are a collection of variables and functions, called properties and methods respectively. We have yet to cover functions, but we have mentioned them on occasion thus far. It is enough to know for now that functions are used to perform a reusable code, we will cover them in the next lesson. These properties and methods describe to JavaScript what a particular object is. Let’s take a look at an example object.

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAiXAAAAJGE5MTc4MWU2LTFhYjAtNGE1NS1hODk2LTZjYTY3OWIwNjYzZA.png](Image00022.jpg)

![https://media.licdn.com/mpr/mpr/shrinknp_800_800/AAEAAQAAAAAAAAflAAAAJDdlNjFlZGJlLTRmNDQtNDNmZS1hZjk3LTI2MmJmOWVkODliMg.png](Image00023.jpg)

In the example above notice in lines 8 to 14 we are declaring a variable and initializing it with a value. The value is wrapped in the curly braces { and }. This indicates to JavaScript that the value is of the type Object. Inside the curly braces we have a list of variables and values separated by a comma. Each variable has a name identifying it, a colon which acts as an assignment operator, the variables initial value. Notice that each of the objects properties omit the var keyword, this is the syntax for declaring properties of an object and it differs from declaring a variable. You can access the object properties by placing a period after the object identifier followed by the property identifier. Also notice in line 22 we are accessing a property that was not declared and the value that is returned in undefined.

With JavaScript objects you can start turning real world objects into digital objects. With a little bit of motivation you could even create a matrix simulation of the real world. Just remember to take the blue pill Neo! Check back tomorrow for as we will cover functions.

Chapter 6

## Functions

Functions allow you to encapsulate a code block, essentially wrapping it up in a capsule that separates the code inside from the code outside. This capsule of code can be called multiples times and in different locations, each time the encapsulated code will execute. Calling a function is just 1 line of code, even though the function’s code block may be calling hundreds of lines of code. Imagine you had a process that was 5 steps long, and you wanted to be able to perform that process multiple times in various locations in your code. You could write the 5 step process in each location, but this is tedious to write. It also makes this code hard to manage. If you needed to update the 5 step process and insert a step between steps 1 and 2, you would have to touch each location to make the update. If you encapsulate this process into a function you only have to update it once. To update the encapsulated code you simply change the code inside the function, which will in turn be the code that is executed each time the function is called.

Encapsulation requires that the variables declared inside the encapsulated code block be completely separated from the variables declared outside of the function. This necessary feature of encapsulation is called Scope. Scope is a concept that determines which variables and functions are visible in a given code block. Code that is written outside of all other functions is said to be globally scoped, and therefore visible to all other scopes. However, a code block that has been encapsulated in a function is in essence in a different scope. If you were to call a function from within another function, the variables defined in each function would be in different scopes, and therefore not visible to one another.

Sometimes you may want to allow some variables outside of the function to pass into the function code block so that that variable value can be acted upon. Functions allow you explicitly list variables that should be allowed to enter into the functions code block. This list is called the parameter list. A parameter is a variable placeholder that can be filled when the function is called.

We will cover the 4 ways functions are commonly used in JavaScript: declared function, function expression, immediately-invoked function expression, and a method.

## Declared Function

The most common form of the function is the declared function. A declared function starts with the keyword function followed by the function identifier. Next is a comma separated parameter list wrapped in parenthesis. Finally the function’s code block wrapped in curly bracers. Let’s take a look at a declared function that has 2 parameters. We will multiply parameter1 by parameter2 and return the result.

![](Image00024.jpg)

Notice that line 15 is making a call to the function we declared and is passing 9 and 9 as values for the two parameters. If you were to save this page and load it in your browser you would get the following alert.

![](Image00025.jpg)

## Function Expression

The function expression is a less common form of a function then the declared function. However, function expressions can be very powerful. Function expressions allow you to overwrite previous implementations of a function. This technique is outside the scope of this fundamental course. It is sufficient to know how to write a function expression.

![](Image00026.jpg)

Notice the difference on line 9. First you declare a variable, giving it the identifier that you will use to call the function. You then use the assignment operator to assign a function to the variable with the function keyword. Notice that after the function keyword we have omitted the function identifier. This is because the identifier is already stated, it is the identifier associated with the variable. Next is the parameter list and function block, the same as with a declared function. If you were to save this page and load it in your browser you would get the following alert.

![](Image00025.jpg)

## Immediately-Invoked Function Expression

In our last two examples we have been calling the function later on in the code. What if you wanted to call the function as it were being declared? In these rare cases you would use an immediately-invoked function expression or IIFE (pronounced “if-fee”). IFFE’s are most commonly used to do something on page load, as soon the code is reached in the sequential order, it will perform it’s code block. Now of course this can also be done using declared functions, and function expressions as well, but the IFFE uses less lines of code. Let’s take a look at an IFFE.

![](Image00027.jpg)

First of all notice how fewer lines of code are required when compared to our first two examples. It is 1 line shorter, and does exactly the same thing. An IFFE is essentially a function expression wrapped in parenthesis and immediately followed by a comma separated value list wrapped in parenthesis. This value list contains the values that will be passed as the function’s parameters. Because this function returns a value we need to capture that returned value. Notice in Line 9 we are first declaring a variable and then assigning it the value that the function returns using the assignment operator. Next we see a function expression wrapped in parenthesis, directly followed by a value list. If you were to save this page and load it in your browser you would get the following alert.

![](Image00025.jpg)

## Method

If you remember I mentioned that objects can store variables and functions called properties and methods respectively. This means that methods are functions that are declared inside of objects. Methods are a useful way to assign action to an object, which will tie the function to the object’s scope instead of the global scope. A method has similar form as the function expression, but instead of using the normal assignment operator (=) the colon (:) serves as assignment operator instead.

![](Image00028.jpg)

Notice in line 9 of this example we are declaring an object, and inside of that object we are declaring a method using the colon assignment operator followed by a function expression. In order to call a method you must first start with the object. This is because the method is tied to the scope of the object and not the global scope. In essence, to access the object’s scope you use the object’s identifier followed by a period (.) and then the property or method within that objects scope. Notice in line 17 we are declaring a variable and initializing it the value returned from the method inside the objects scope. If you were to save this page and load it in your browser you would get the following alert.

![](Image00025.jpg)

Chapter 7

## Conditional Statements

A conditional statement executes a code block only when a specific condition is met. First a conditional statement defines the condition that needs to be met. Next it defines the code block that is to be executed. When the conditional statement is evaluated and the condition is met the associated code block is executed. When a conditional statement is evaluated and the condition is not met, the code block is skipped.

The condition is defined by one or more logical statements. Multiple logical statements can be combined using the logic operators. Logical statements will either evaluate to true or false, but not all statements are logical statements. Notice that the statement 5 + 5 does not return a logical true or false, but a numerical value of 10\. However, if we use the “is equal to” operator at the end it then becomes a logical statement. 5+5==10 is a logical statement that evaluates to true because 5 plus 5 is equal to 10\. The == operator is classified as a comparison operator. Comparison operators compare two values and return a Boolean value. A detailed explanation of each of the comparison operators and the Logical operators is outside the scope of the course. However, I would suggest looking at the following sites for

## The If conditional statement

Let’s create a function that takes 1 string parameter called test. In this test function we will use a built in JavaScript feature for strings that will return the string value converted to all lowercase letters.  We will then compare the lower case value of the string parameter with a literal string value. If it is equal to the string literal then we will alert a response. We will call this test function 2 times, the first time we will pass a value that is going to match. The second time we will pass a value that will not match.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\001A.png](Image00029.jpg)

If you were to save this page and load it in your browser you would get the following alerts.

Alert from the first call to the test function:

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\001B.png](Image00030.jpg)

Alert from the second call to the test function:

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\001C.png](Image00031.gif)

Notice that the second call to the test function alerts a value of undefined. This is because the value we passed into the function as a parameter did not evaluate to true in the conditional statement on line 10, and therefore was skipped. The variable RTN having not been initialized was of data type undefined. 

What do you suppose would happen if we assigned a value to the RTN variable after the conditional statement? Let’s take a look.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\002A.png](Image00032.jpg)

If you were to save this page and load it in your browser you would get the following alerts.

Alert from the first call to the test function:

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\002B.png](Image00033.jpg)

Alert from the second call to the test function:

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\002C.png](Image00034.jpg)

Notice that both alerts show the value we assigned the RTN variable after the condition statement. Even though the first call to test used a value that evaluated to true in the function’s conditional statement. This is because in programming code is executed in sequential order. In the first call to the test function the condition evaluates to true and assigns the value “hello” to the RTN variable. However, the function is not done, so it continues to execute all the way to the end. This means that line 13 will be executed next. Line 13 assigns a different value to the RTN variable, overwriting the original value, and then we return the RTN variable. In both calls line 13 is executed, and this is why both alerts showed that value.

## The Else conditional statement

Most programming languages have an “Else” statement that can complement the “if” statement. The else statement is executed when the condition evaluates to false. Let’s take a look at an if/else statement.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\003A.png](Image00035.jpg)

If you were to save this page and load it in your browser you would get the following alerts.

Alert from the first call to the test function:

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\003B.png](Image00036.jpg)

Alert from the second call to the test function:

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\008\003C.png](Image00037.jpg)

Notice that the if/else conditional statement controls which block of code is executed by evaluating a conditional statement to true or false. If/Else statements also called if then else statements are the most basic form of the conditional statement. With them you can control when specific code blocks are executed.

Sometimes you need to evaluate multiple conditions consecutively, one after the other. In these cases you could have an If statement inside another if statement, which is called nested If statements. Like the Russian nesting dolls these If statements fit inside each other. Let’s take a look at a nested If statement.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\001A.png](Image00038.jpg)

If you were to save this page and load it in your browser you would get the following alerts.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\001B.png](Image00039.jpg)

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\001C.png](Image00040.jpg)

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\001D.png](Image00041.jpg)

## Else if

The problem with nested If statements is that it is very easy to lose track of which if statement your code is associated with. Also the syntax becomes somewhat convoluted which makes it easy to misplace a curly brace and cause a syntax error. Else/ if statements are another a solution for evaluating multiple conditions. The Else/If is a much cleaner conditional statement than the nested If statements, and therefore less likely to be the cause of a misplaced curly brace. Some have said that the Else/If is the best performing way in JavaScript to evaluate multiple conditions.

The Else/If statement is straight forward, and as you may suspect it uses the Else keyword followed by the If keyword. Next in line is the conditional expression wrapped in in parenthesis. After that is the associated code block. Let’s take a look at an Else/If statement.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\002.png](Image00042.jpg)

If you were to save this page and load it in your browser you would get the same exact alerts as our previous example.

## Switch

While the Else/if Statement is cleaner than nested If statements some consider it hard to read. Switch statements are a completely different approach to evaluating multiple conditions, that offers reader friendly code. It is of note that in JavaScript the switch statement is slightly slower than the Else/If statement. If your code is evaluating a large group of conditions and page load times are being affected, consider using the Else/If statement instead of the Switch statement.

The switch statement defines the switch value and then compares it to multiple case values. The switch value is defined in the switch expression, and the case values are defined by each individual case / break expressions. The case / break expressions indicate a value and a code block. The case value is compared to the switch condition, with the “is equal to” (==) comparison operator by default. This comparison is implied, and the operator is not explicitly in the code of a switch statement. When the switch statement and the case value are compared and evaluated to true, the code associated with the case value is executed. Otherwise the associated code is skipped.

When using the switch conditional statement we first use the switch keyword followed by a condition expression wrapped in parenthesis. This condition expression represents the value that is being evaluated. Next is our code block, wrapped in curly braces. Inside our code block we have a series of case/break expressions. The case/ break expression starts with the case keyword followed by the case value and then a colon. Directly after the colon is the associated code, followed by the keyword break and a semicolon. In the following example we are going to create a function that tests a string value against multiple conditions. When comparing string values it is common convert the parameter to lowercase, to make the value passed into the function case insensitive. To do this in JavaScript, we use the built in string method “toLowerCase.” Let’s take a look at a standard switch statement.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\003.png](Image00043.jpg)

If you were to save this page and load it in your browser you would get the same exact alerts as our previous example.

It is also possible to have different conditional statements in each case. To do this we define the switch value as true, and the case values as the individual conditional statements wrapped in parenthesis. Ultimately this is comparing the value true to the result of the conditional statement. This is a more advanced version of the switch statement, and can be somewhat hard to read. Some consider this to defeat the purpose of the switch statement, and therefore opt to use Else/If statements instead.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\004.png](Image00044.jpg)

If you were to save this page and load it in your browser you would get the same exact alerts as our previous example.

Now let’s use the string method “indexOf” that is built into JavaScript, to create a conditional statement that does not use the == comparison operator. The indexOf method checks the string for the first occurrence of a string value, and returns the index of that occurrence in the string. If the string value is not found anywhere in the string then the value -1 is returned. This means if the string method indexOf returns a number that is greater than -1 the string value exists somewhere in the string.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\009\005.png](Image00045.jpg)

Chapter 8

## Loops

JavaScript allows you to execute a code block multiple times without writing it multiple times, using loops. There are several different loops in JavaScript: the “For” loop, the “For … In” loop, the “While” loop, and the “Do … While” loop. I like to categorize these further into two groups: the limited loops and the unlimited loops. The “For” loop and the “For … In” loop are both limited loops. This is because they both have a limit to the number of loop cycles that will be executed. This limit is explicitly defined in the loop statement. The “While” loop and the “Do … While” loop are unlimited loops. This is because there is no explicit limit set to the number of loop cycles will be executed. Instead, they loop endlessly until a condition is met.

Loops can be useful for Iteration. Iteration is the process of executing a code block upon a member in some sort of collection. Previously we have covered objects, which are a considered a collection. Objects are a collection of properties. Do note that there are other collections built into JavaScript. Most notably is the Array, which we will cover later on in this course. For now, it is enough to know that there are different types of collections, and loops can be used to iterate through them.

There is built in method for all objects that is called the “For Each” method. Ultimately the “For Each” method is a “For … In” loop that executes a callback function instead of a code block. For this reason, it is not considered a unique loop. It might be useful to know that other languages call the “For … In” loop a “For Each” loop.

## For

The For loop starts with the for keyword followed by 3 statements wrapped in parenthesis. The 1st statement is executed before the loop starts. It is used to declare and initialize the iterator variable. The most common identifier for an iterator variable is the letter “i”, and it stands for “iterator.” The 2nd statement is evaluated at the top of every cycle, and it typically defines the iterator’s limit. Once the iterator has reached its limit the loop is completed and no more cycles are executed. Ultimately, this is a conditional statement. When this statement evaluates to true the loop continues another cycle. When it evaluates to false the loop is exited. The 3rd statement is executed at the bottom of each cycle, and it typically modifies the iterator. Iterators are typically increased by 1 in value in this statement using the increment (++) operator. However, this is not always the case. The iterator can be increased or decreased by a value greater than 1, and other operators can be used. This means you can iterate in ascending or descending order through a list at different intervals. The increment operator returns a value that is equal to the value + 1\. It is a short hand for writing myValue = myValue + 1; and it looks like this: myValue++;. Let’s take a look at a “For” loop.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\010\001.png](Image00046.jpg)

If you were to save this page and load it in your browser you would get the following alert.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\010\001B.png](Image00047.jpg)

## For In

The “For … In” starts with the “for” keyword followed by an open parenthesis. Next is the declaration of the iterator variable then the “in” keyword. After that is the collection that is being iterated then a closing parenthesis. The iterator's limit is defined by the number of members in the collection. Remember that an object is considered a collection of properties. This means that the members of the collection are the properties of the object. For our example we will be declaring an object, then iterating through its properties. Lastly is the code block that is associated with the loop. Let’s take a look at a “For … In” loop.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\010\002.png](Image00048.jpg)

If you were to save this page and load it in your browser you would get the following alert.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\010\002B.png](Image00049.jpg)

## While loop

The “While” loop is the simplest form of the Loop in JavaScript. It is designed to loop when a condition evaluates to true. When the condition does not evaluate to true, the Loop is exited. While loop starts with the keyword “while”, followed by a condition expression wrapped in parenthesis. After that is the code block associated with the loop. Let’s Take a look at a “while” loop.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\001A.png](Image00050.jpg)

If you were to save this page and load it in your browser you would get the following alert.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\001B.png](Image00051.jpg)

The “While” Loop places no emphasis on iteration. This does not mean that “While” loop cannot be used for iteration. In the above example we are counted from 0 to 9\. In this same fashion, we can declare and initialize a variable that acts as an iterator before we start a “while” loop. We can set the iterator’s limit as the “While” loop’s condition, and we can increment or decrement the iterator within the “While’ Loop. This iterator can then be used to iterate through a collection, just as in the “For” loop. The point here is that you do not have to use a “While” loop for iteration. By design it does not require you to define an iterator, set its limits, nor its modifier.

The “While” loop is can be used for state based logistics. A state is a predefined condition that is used to determine the functionality of a given aspect of code. State based logistics are used in graphical user interface (GUI), for example. When a button is pressed that button is in the down state. When it is not pressed it is in the up state. When a mouse is over a button it is in the hover state. The button has three distinct states, and they control the look and feel of that button in the GUI. Video games typically use state based logistics to control many aspects of gameplay mechanics. For example, video game A.I. tends to use state based logistics to determine the behavior of a non-player character (NPC). If the NPC has flagged a player character as hostile, the NPC will execute predefined tactics for hunt down the player character. If the NPC has not flagged any player characters as hostile, it will execute some other predefined behavior, like patrolling the perimeter of a building. Let’s take a look at a very simple state based “While” loop.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\002A.png](Image00052.jpg)

If you were to save this page and load it in your browser you would get the following alert.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\002B.png](Image00053.jpg)

## Do While Loop

All the other loops that we covered had conditions that were evaluated at the top of the code block. The condition is evaluated before the associated code block is executed. This means that the initial value of the iterator or state variables could cause the condition to evaluate to false before the code block is ever executed. The “Do … While” loop evaluates its condition at the bottom of the code block, meaning it is evaluated after the code block executes. This loop is used if you when you want the associated code block to run at least 1 time.

The “Do … While” loop starts with the “do” keyword, followed by the code block. After the code block is the “while” keyword followed by the conditional expression wrapped in parenthesis. Lastly we capped it off with a semicolon. Let’s take a look at a “Do … While” Loop.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\003.png](Image00054.jpg)

If you were to save this page and load it in your browser you would get the following alert.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\002B.png](Image00053.jpg)

To illustrate the usefulness of a “Do … While” loop, let’s compare two loops with two unique iterators. Both iterators will be initialized to the value of the Loop’s limit.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\004.png](Image00055.jpg)

If you were to save this page and load it in your browser you would get the following alert.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\JS 101\011\004B.png](Image00056.jpg)

Notice that the “While” loop skipped its code block because the iterator was initialized to the loop’s limit, but the “Do … While” loop did not skip the code block even though its iterator was also initialized to the loop’s limit. This is because the “Do … While” loop evaluated its condition at the bottom of the code block, causing the code block to run at least 1 time.

Chapter 9

## Arrays

JavaScript has many built in objects that are ready for use. One of the built objects is the Array. As mentioned earlier, an array is a collection. The Array is actually a collection of key value pairs. A key value pair is an identifier and a value that are associated to one another. Object properties are key value pairs. However, an Array does not explicitly define the key value pair’s key. It is implied by the values numerical position in the collection, which is called the index. Arrays are useful for storing related data while maintaining a sibling relationship with other key value pairs in the collection.

Arrays can be instantiated (an instance of that object created) three different ways: the associative shorthand, the implicit shorthand, and using the object constructor. As already mentioned, the Array is an object. This means that we can instantiate an array just as we would an object. This is the associative shorthand. The implicit shorthand can be used to implicitly define the key based on the index of the value in the collection. The Array constructor can also be used to instantiate an array. A constructor is a special method that constructs the object, hence the name constructor. The Array constructor takes 1 parameter which determines the specific length of the array. Let’s take a look at these three different ways of instantiating an Array.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\002.png](Image00057.jpg)

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\001A.png](Image00058.jpg)

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\003.png](Image00059.jpg)

If you were to save these pages and load them in your browser you would get the following alert for each of them.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\001B.png](Image00060.jpg)

Arrays can also have more than 1 dimension, otherwise called a multi-dimensional Array. More and more complex hierarchical data structures can be achieved using multi-dimensional arrays. Instead of just sibling relationships, multi-dimensional Arrays introduce parent-child relationships. For example, a 2 dimensional Array creates a hierarchy similar to that of a spreadsheet. You can consider the rows of a spreadsheet to be the children of the columns of that spreadsheet. This is an example of a parent-child hierarchy relationship. In this same way, data can be structured into more complex structures using multi-dimensional Arrays. Let’s take a look at the a multi-dimensional array.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\004.png](Image00061.jpg)

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\003.png](Image00062.jpg)

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\005.png](Image00063.jpg)

If you were to save these pages and load them in your browser you would get the following alert for each of them.

![H:\Projects\[Locker] Desktops\[Locker] Personal\JS 101\012\007B.png](Image00064.jpg)