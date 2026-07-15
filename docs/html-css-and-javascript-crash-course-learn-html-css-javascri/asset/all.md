![](image_rsrc3EN.jpg)

html, CSS and javascript

CRASH COURSE:

learn HTML, CSS & JAVASCRIPT From Scratch AND

MASTER IT

Alan Hopper

© Copyright 2024 - All rights reserved.

The content contained within this book may not be reproduced, duplicated or transmitted without direct written permission from the author or the publisher.

Under no circumstances will any blame or legal responsibility be held against the publisher, or author, for any damages, reparation, or monetary loss due to the information contained within this book. Either directly or indirectly.

Legal Notice: This book is copyright protected. This book is only for personal use. You cannot amend, distribute, sell, use, quote or paraphrase any part, or the content within this book, without the consent of the author or publisher.

Disclaimer Notice: Please note the information contained within this document is for educational and entertainment purposes only. All effort has been executed to present accurate, up to date, and reliable, complete information. No warranties of any kind are declared or implied. Readers acknowledge that the author is not engaging in the rendering of legal, financial, medical or professional advice. The content within this book has been derived from various sources. Please consult a licensed professional before attempting any techniques outlined in this book.

By reading this document, the reader agrees that under no circumstances is the author responsible for any losses, direct or indirect, which are incurred as a result of the use of information contained within this document, including, but not limited to, — errors, omissions, or inaccuracies.

Table of Contents

[Introduction](#part0003.xhtml)

[Chapter 1.​Fundamentals of HTML](#part0004.xhtml_a39E)

[Chapter 2.​HTML Styles](#part0005.xhtml_a39F)

[Chapter 3.​Forms In HTML](#part0006.xhtml_a39G)

[Chapter 4.​Frames, Colors, And Layout Of HTML](#part0007.xhtml_a39H)

[Chapter 5.​How to Put Images in HTML?](#part0008.xhtml_a39J)

[Chapter 6.​HTML Tables](#part0009.xhtml_a39K)

[Chapter 7.​Fundamentals Of CSS](#part0010.xhtml_a39M)

[Chapter 8.​CSS](#part0011.xhtml_a39N)

[Chapter 9.​CSS Links, Tables, And Forms](#part0012.xhtml_a39P)

[Chapter 10.             Image Manipulation in CSS](#part0013.xhtml_a39R)

[Chapter 11.             Length Units](#part0014.xhtml_a39S)

[Chapter 12.             CSS IDs and Classes](#part0015.xhtml_a39T)

[Chapter 13.             The Box Model In CSS](#part0016.xhtml_a39U)

[Chapter 14.             Step By Step Addition Of CSS To HTML Document](#part0017.xhtml_a39V)

[Chapter 15.             Introduction Tot](#part0018.xhtml_a39W)

[Chapter 16.             JavaScript Syntax](#part0019.xhtml_a39X)

[Chapter 17.             Definition of Arrays in JavaScript](#part0020.xhtml_a39Y)

[Chapter 18.             What to Do Next?](#part0021.xhtml_a39Z)

[Chapter 19.             Art of Computer Programming](#part0022.xhtml_a3A0)

[Conclusion](#part0023.xhtml)

[Index](#part0024.xhtml)

# Introduction

HTML stands for Hypertext Markup Language. It’s a special language that web browsers understand. It’s basically a bunch of instructions about the structure of the document.

Hypertext is probably the most important part of HTML letters because it means that you can link one document to another one. Hypertext is a text file that contains links to other text files.

This is the foundation stone of web, which at the beginning wasn’t much more than few pages interconnected with links. Today, the web is no longer just about text. Most of it is created by Hypermedia including video, photos and music. But if you strip down all the bells and whistles, you will still find this fundamental functionality of mutual linking between documents at the core of any modern web application including Twitter, Gmail and even the project we are about to build.

Markup means that HTML surrounds regular text with special code which tells the browser how to display the content of the document. It tells the browser what the structure of the document is.

Language means that HTML has some special syntax or the rules you need to follow to create the correct content. Just like with other languages where subjects and verbs have a special place in the sentence, HTML tags have a special structure you need to use. For instance, when you need to nest tags, you must place the closing part of the tag correctly.

When you build an HTML website, you actually need to learn different coding languages (even though it is called an HTML website). The structure or the core is provided by HTML, while CSS is about setting up the looks and the visual feel, in order to make your website appealing and pretty to look at. In order to make your website more dynamic and to add additional interaction with the user, you can use JavaScript. As you can see, in order to create a competitive website, you should at least learn the basics and how these languages work. 

These days, people use many devices with different screen sizes and resolutions to browse the Internet, so it is very important to be able to change the visible content based on what kind of device the user is currently using. This is referred to as a responsive approach or responsiveness and we will dive into it when we talk about CSS.

CSS provides styling for the structure. Let’s say you have a house with three rooms. One room is a kitchen, one room is a bedroom and one is a bathroom. Based on this description, you have a basic idea about the structure of the house, but you have no idea how big those rooms are and what are the colors of the walls. This is what CSS provides.

When it comes to real-world websites, the structure of the content is not enough. You probably experienced this yourself. When you search on the Internet for a restaurant, would you rather visit the one with a very nice, professional looking website or the one with just a simple blank page with general, unformatted text?

Regarding the content, they can both give you the same information as menu, opening hours, contact, and so on, but as you know, it's the package that sells the product. 

That's why it's crucial to focus on the styling of your content in a way that's pleasing and useful for the visitor of your website.

CSS (cascading style sheets) is technologies that will allow you to make your page look anything you want without the need to change the structure of the HTML document. 

CSS is immensely powerful in transforming the styling of the website without ever touching the content and its HTML structure.

Javascript provides the behavior. It gives HTML webpage event-driven functionality, like what will happen when the browser finishes loading the page or when the user clicks the Buy button on the web shop.

Javascript is the third language you are about to learn in this book. It is one of the three languages every web developer must know and understand.

As you already know, HTML defines the content of web pages, CSS specifies the layout and Javascript programs the behavior.

People usually don't appreciate the power of Javascript and this is probably caused by two main reasons.

First, they lack the proper understanding of the language fundamentals. Second, Javascript doesn't have a great reputation because in the early days of the web, the vendors of browsers implemented Javascript however they pleased. And this of course caused a lot of headaches to web developers, because they couldn't be sure how their code would run in different browsers, if at all.

Setting up frontend technologies is very easy. To get all three frontend technologies up and running, you need just one product, a web browser.

Also, you will need a good plaintext editor. Just make sure it doesn't add anything else to your code behind the scene. For this reason, you really shouldn't use document processors like Microsoft Word or Apple Pages. These are made for something entirely different and their built-in formatting features will ruin your code.

# Chapter 1.         Fundamentals of HTML

## What Is HTML?

Divisions were used for a long time in building a webpage structure. However, divisions have a problem in that they don’t provide a semantic value, making it difficult to tell divisions intensions. However, new elements which are structurally based are introduced by HTML5\. These elements include <header>, <nav>, <article>, <section>, 

<aside>, and <footer>.

These elements give meaning to the way web pages are organized and improve the structural semantics. All of these are block-level elements and have no implied style or position. All of these elements can also be used severally in a web page provided each element has a proper reflection of its semantic meaning. Let us discuss this one by one. 

## Header

Just as the name suggests, the <header> elements help us to identify the top of a web page, section or article, or any other segment of a web page. The <header> element may have a heading, an introductory text, and navigation. It is created as follows: 

<header>...</header>

Don’t confuse this <header> element with the <head> element or headings <h1> through <h6>. They all have different meanings when it comes to semantics. 

The <header> is a structural element that identifies the heading of a page segment. It should be added within the <body> element. 

The <head> element isn’t shown on a web page as it only provides the metadata for a web page. Examples of such metadata include the title of the web page and links to any external files. It should be added directly to the <html> element. 

The headings <h1> through <h6> help us to designate the multiple levels of text headings throughout a web page. 

## Navigation

The <nav> element is used for identifying a section of the major navigational links on a web page. The <nav> element should be used for primary navigation sections only, like a table of contents, global navigation, previous/next links and other groups of navigational links. It is created as follows:

<nav>...</nav>

## Article

We use the <article> element to identify a section of independent and self-contained content that can be used or distributed independently. Use the <article> element to markup newspaper articles, blog articles, user-submitted content, and other related content. 

Before using the <article> element, you have to ask yourself whether it is possible for you to replicate the content elsewhere without introducing confusion. If you remove the contents of the <article> element and you place them somewhere else like in an email, the <article> element should still be able to make sense. It is created as follows:

<article>...</article>

## Section

We use the <section> element to identify a group with same theme of content, which usually has a heading. The way the content is grouped within the <section> element can be general, but it will be good to ensure that the content is related. 

Use the <section> element to separate and create a hierarchy within your web page. It is created as follows:

<section>...</section>

Sometimes, determining the element to be used based on the semantic meaning of the element might still be difficult for you to do. The trick is simple, consider the content. The trick is simple, consider the content. 

The <section> and <article> elements play a significant contribution to the structure of a document and help in outlining documents. If styling is the purposes for grouping the content without adding value to the document structure, use the element <div>. 

If the content has an impact on the outline of the document and can be redistributed independently, use the element <article>. 

If the content has an impact on the outline of the document and is a representation of a group of content with a theme, use <section> element. 

## Aside

Use the <aside> element to hold contents such as inserts, sidebars and short explanations that are related to the surrounding content. When it is used with an <article> element, the <aside> element may be good for identifying the publisher of an article. 

See the <aside> element as the element that is displayed off to the sides (left or right) of a page. Remember that all structural elements like the <aside> are elements on a block-level and they will appear in a new line, and they will occupy the entire width provided by the web page or cover the whole length of the element they are nested within the parent element. 

It is created as follows:

<aside>...</aside>

## Footer

The f<footer> element is used to identify the end or closing of a web page, or any other part of a web page. Usually, the footer is added to the bottom part of its parent. It is created as follows:

<footer>...</footer>

## Practice

We need to put all the above into practice by creating a basic website. We will use hyperlinks to link together the various pages of the website. 

Step 1) We will first link the “My Website” text inside an <h1> element within the <header> element to the index.html page. This is the page that is first loaded when the user opens the website, showing the home page. This means that when a user clicks My Website text, they will be taken to the home page of the website. 

This is shown below:

<h1>

<a href="index.html">My Website</a>

</h1>

Step 2) For us to be able to navigate through the different web pages, we will create the navigation menu using the <nav> element within the header element. This will be done within the <header> element. We will add the About Us, Services, Location and Contact Us pages to go together with the Home page. We have to create links for all of these. The navigation menu can be created as follows:

<header>

...

<nav>

<a href="index.html">Home</a>

<a href="about.html">About Us</a>

<a href="services.html">Services</a>

<a href="location.html">Location</a>

<a href="contact.html">Contact Us</a>

</nav>

</header>

Step 3) For convenience purposes, let us add the same navigation to the footer section of the website. This can be done as follows:

<footer>

...

<nav>

<a href="index.html">Home</a>

<a href="about.html">About Us</a>

<a href="services.html">Services</a>

<a href="location.html">Location</a>

<a href="contact.html">Contact Us</a>

</nav>

</footer>

Step 4) In the <section> element, that introduces our website, we need to add a link that will urge them to contact us now. It will be good for this link to be added below a paragraph:

<section>

...

<a href="contact.html">Contact us Now</a>

</section>

Step 5) We need to add links to all sections that tease the other pages. Inside every section, we will wrap both <h3> and <h5> elements within an anchor element that links to the right page. This should be done for every section:

<section>

<section>

<a href="services.html">

<h5>Services</h5>

<h3>World-Class Services</h3>

</a>

<p>We served different customers from all over the world, and these are ready to share their testimonies.</p>

</section>

...

</section>

After that, you should create the other pages and make sure that they are stored in the same folder as the index.html file. These pages are the about.html, services.html, location.html and contact.html. 

For the purpose of ensuring that all pages look the same, use the same document structure for all pages and use the <header> and <footer> elements as the file index.html. 

Your combined code should be as follows:

<!DOCTYPE html>

<html>

<header>

<h1>

<a href="index.html">My Website </a>

</h1>

<nav>

<a href="index.html">Home</a>

<a href="about.html">About Us</a>

<a href="services.html">Services</a>

<a href="location.html">Location</a>

<a href="contact.html">Contact Us</a>

</nav>

</header>

<body>

<section>

<section>

<a href="services.html">

<h5>Services</h5>

<h3>World-Class Services</h3>

</a>

<p>We served different customers from all over the world, and these are ready to share their testimonies.</p>

...

</section>

<a href="contact.html">Contact us Now</a>

</section>

</body>

<footer>

<nav>

<a href="index.html">Home</a>

<a href="about.html">About Us</a>

<a href="services.html">Services</a>

<a href="location.html">Location</a>

<a href="contact.html">Contact Us</a>

</nav>

</footer>

</html>

It should return the following:

![00018.jpeg](image_rsrc3EP.jpg)

# Chapter 2.         HTML Styles

## Text Style

Text Style includes font-family, font-size, font-style, font-weight, font-variant.

| Font | Value |
| font-family | Arial, Times New Roman, Courier New, Georgia, Verdana |
| font-size | 9px, 10px……Large |
| font-style | normal, italic, oblique |
| font-weight | normal, bold, number |
| font-variant | normal, small-caps |

Text Style can be specified by { property: value }.

Example 6.1

<html>

<style type = "text/css">

#f{ font-family: Times New Roman; font-size: 28px; font-style: italic; font-weight: bold; font-variant: normal }

</style>

<div id = "f">This is a text content using a different style.</div>

</html>

Output:

This is a text content using a different style.

Explanation:

“font-family, font-size, font-style, font-weight, font-variant.” specifies the text style for the font.

## Spacing

The line-height can specify line spacing.

The word-spacing can specify word spacing.

The letter-spacing can specify letter spacing.

Example 6.2

<html>

<style type = "text/css">

#lineSpacing{ line-height:500% }

#wordSpacing{ word-spacing: 10px }

#letterSpacing{ letter-spacing: 5px }

</style>

<p id = "lineSpacing">Line Spacing Sample.</p>

<p id = "wordSpacing">Word Spacing Sample.</p>

<p id = "letterSpacing">Letter Spacing Sample.</p>

</html>

Output:

![00011.jpeg](image_rsrc3ER.jpg)

Explanation:

“line-height:500%” specifies the line height as 500%.

“word-spacing: 10px” specifies the word spacing as 10px.

“letter-spacing: 5px” specifies the letter spacing as 5px.

## Divided Style

The dividing <div></div> tags are used to group their content elements as blocks. <div> tags are useful for styling purposes.

| <div class = “xxx”></div><div id = “xxx”></div> |

The <div> tag can have id and class attribute in css style.

Example 6.3

<html>

<style type = "text/css">

.d1{font-style: italic; color: purple;}

#d2{font-family: arial black; color: blue;}

</style>

<body>

<div class = "d1"> <p>AAAAA</p> <p>BBBBB</p> <p>CCCCC</p> 

</div>

<div id = "d2"> <p>EEEEE</p> <p>FFFFF</p> <p>GGGGG</p>

</div>

</body>

</html>

Output:

AAAAA

BBBBB

CCCCC

EEEEE

FFFFF

GGGGG

Explanation:

<div class = "d1"></div> is divided as the first group which contains three pairs of <p> tags. They use “.d1” style.

<div id = "d2"></div> is divided as the second group which contains other three pairs of <p> tags. They use “#d2” style.

## Span Style

<span></span> can be used to group elements for styling purposes (using the class or id attributes).

| <span class = “xxx”></span><span id = “xxx”></span> |

The <span> tag can have id and class attribute in css style.

Example 6.4

<html>

<style type = "text/css">

div{background-color: yellow}

.d1{font-style: italic;color: purple;}

#d2{font-family: arial black;color: blue;}

</style>

<body>

<div><p>This is AAA text, 

<span class = "d1">This is BBB text,</span>

This is CCC text, 

<span id = "d2">This is DDD text,</span>

This is EEE text.</p></div> 

</body>

</html>

Output:

This is AAA text, This is BBB text, This is CCC text, This is DDD text, This is EEE text.

Explanation:

The above uses <span></span> tags to set the css style of two pieces of text within a paragraph which is contained in a block.

<span> is very much like a <div> element, but <div> is a block-level element whereas a <span> is an inline element.

## Border Style

| border-style: value |

“border-style: value” can set the border style by specifying different value. The “value” may be “solid, double, dashed, dotted, groove, ridge, inset, outset”.

Example 6.5

<html>

<style type = "text/css">

#b1{border-style: solid; border-width: 10px;}

#b2{border-style: double; border-width: 10px;}

#b3{border-style: dashed; border-width: 10px;}

#b4{border-style: dotted; border-width: 10px;}

#b5{border-style: groove; border-width: 10px;}

#b6{border-style: ridge; border-width: 10px;}

#b7{border-style: inset; border-width: 10px;}

#b8{border-style: outset; border-width: 10px;}

</style>

<body>

<p id = "b1">This is solid border.</p><br>

<p id = "b2">This is double border.</p><br>

<p id = "b3">This is dashed border.</p><br>

<p id = "b4">This is dotted border.</p><br>

<p id = "b5">This is groove border.</p><br>

<p id = "b6">This is ridge border.</p><br>

<p id = "b7">This is inset border.</p><br>

<p id = "b8">This is outset border.</p><br>

</body>

</html>

Output:

![00012.jpeg](image_rsrc3ES.jpg)![00013.jpeg](image_rsrc3ET.jpg)

Explanation:

The “border-style: value” may be “solid, double, dashed, dotted, groove, ridge, inset, outset”.

The “border-width: 10px” specifies the border width as 10 px.

## Border Color

| border-color: value |

“border-color: value” can set the bonder properties for color.

Example 6.6

<html>

<style type = "text/css">

#b5{border-style: groove;border-width: 20px; border-color:blue }

#b6{border-style: ridge;border-width: 20px; border-color:purple }

</style>

<p id = "b5">This is groove border.</p>

<p id = "b6">This is ridge border.</p>

</html>

Output:

![00014.jpeg](image_rsrc3EU.jpg)

Explanation: “border-color: value” can set the bonder color.

## Padding Style

The padding is the area around the text content in a content box. The padding width can be specified with a padding attribute.

| padding: value |

Example 6.7

<html>

<style type = "text/css">

#b1{border-style: solid; border-width: 5px; padding: 10px }

#b2{border-style: dotted; border-width: 5px; padding: 20px }

</style>

<p id = "b1">This padding is 10px.</p>

<p id = "b2">This padding is 20px.</p>

</html>

Output:

![00015.jpeg](image_rsrc3EV.jpg)

Explanation:   “padding: value” can set the padding width.

## Margin Style

The area around the border edges is called the margin.. 

The margin width can be specified with a margin attribute.

| margin: value; |

Example 6.8

<html>

<style type = "text/css">

#b1{border-style: solid; border-width: 5px; margin: 30px }

#b2{border-style: dotted; border-width: 5px; margin: 0px }

</style>

<p id = "b1">This margin is 30px.</p>

<p id = "b2">This margin is 0px.</p>

</html>

Output:

![00016.jpeg](image_rsrc3EW.jpg)

Explanation: “margin: value” can set the margin width.

## Absolute Positioning

The content position can be specified by position attribute.

| position: absolute;  top: value;  left: value;   |

“position: absolute” sets the precise location of the contents.

“top: value” sets the distance from the top edge of the window.

“left: value” sets the distance from the left edge of the window.

Example 6.9

<html>

<style type = "text/css">

#a1{ position:absolute; top: 0px; left: 30px }

#a2{ position:absolute; top: 30px; left: 60px }

</style>

<p id = "a1">This is position1.</p>

<p id = "a2">This is position2.</p>

</html>

Output:

![00017.jpeg](image_rsrc3EX.jpg)

Explanation:  “position: absolute;  top: value;  left: value;” specifies the absolute distance from the browser window edge. 

## Relative Positioning

| position: relative;  top: percentage;  left: percentage;   |

“position: relative” sets the relative location of the contents based on the browser window resolution or window size.

“top: percentage” sets the distance from the top edge of the window. “left: percentage” sets the distance from the left edge of the window.

Example 6.10

<html>

<style type = "text/css">

#r{ position:relative; top: 3%; left: 5% }

</style>

<p id = "r">This is the relative position.</p>

</html>

Output:

![00018.jpeg](image_rsrc3EY.jpg)

Explanation:

“position:relative; top: 3%; left: 5%” specifies the relative position based on the resolution or size of the browser window.

## Html Symbols

In HTML documents, when you meet some special symbols such as &, <, >, and space, you need to use corresponding codes, &amp; &lt; &gt; &nbsp;

| Symbols | Source Codes |
| < | &lt; |
| > | &gt; |
| & | &amp; |
| “” | &quot;  &quot; |
| © | &copy; |
| ® | &reg; |
| space | &nbsp; |
| ! | &#33; |
| : | &#59; |

Example 6.11

<html>

<body>

&lt; Java in 8 Hours &gt; &amp; &lt; Python in 8 Hours &gt; are very books&#33;<br>  

Copyright &copy; 2016 by Ray Yao &nbsp; &nbsp; &nbsp;

All Rights Reserved&#33;

</body>

</html>

Output:

< Java in 8 Hours > & < Python in 8 Hours > are very books!

Copyright © 2016 by Ray Yao       All Rights Reserved!

Explanation:

| Symbols | Code |
| <   > | &lt;    &gt; |
| > | &gt; |
| & | &amp; |
| © | &copy; |
| space | &nbsp; |
| ! | &#33; |

# Chapter 3.         Forms In HTML

## Web Forms Basics

Web pages are not just about reading documents and articles, but are also for social and business applications. You can hardly imagine any kind of web app without asking some data from users—just think about the most common functions, such as login and registration.

HTML forms are the part of the markup since the earliest versions, and now, after several twists—that are related to HTML-XHTML debates—we have a refined model of forms in HTML5, which still works with older browsers.

## How Web Forms Work

![00067.jpeg](image_rsrc3EZ.jpg)This shows a web form in action, which contains user interface components—or, with another name, controls. Not only textboxes, checkboxes and radio buttons are controls in this form, but labels, and frames surrounding the sections, too, as well as the Register button.

A web form in action

To design and code web forms, you need to understand how they work. Here is a simplified overview:

When the browser displays a web form, it simply renders its controls just like any other element, such as text, menus, images, and so on. Users fill it out, and then click a button that submits the form. The submission of a form means that the browser collects the data entered by the user, puts it into an HTTP/HTTPS request, and sends it to the server. When the server side receives the request, the web server finds out the type of application or module to dispatch the request with the collected data. The entity receiving the request analyzes the information collected, and decides what to do next.

For example, if the request contains registration data, the web server may store it in the database and send back a message about the success of registration. Or, if the data is invalid, for example a mandatory field has not been filled out, the webserver might send back the original form with the data specified by the user, and with additional markup that summarizes the issues found by the server application.

So, this process contains these fundamental steps:

1\. The browser collects the form data, and sends it to the web server.

2\. The web server processes the data, and sends back the result to the browser.

3\. The browser visualizes the result (which may be a web page, an error message, or some other kind of information, etc.)

Of course, the most difficult part of this process is step 2, which is carried out at the server side. There are many server technologies that can process web forms, but in this book we do not dive into them, we will only scratch the surface.

As the web evolved, and users expected fluent experience, new asynchronous technologies appeared, such as AJAX (Asynchronous JavaScript and XML). These do not expect the web server to retrieve a full web page, but only a part of the page—affected by the changes in regard to the information the users specified. This approach results in smaller network packages, and less flickering on the screen. The main virtue of the asynchronous technologies is that they can send data to—and retrieve data from—a server asynchronously in the background, without preventing user interaction.

In this chapter you will focus on building and using web forms at the client side.

## Representing Web Forms in HTML

The key HTML element is <form> that defines a web form within a page. The simplest web form takes only a few lines of markup:

<form action="ProcessAtServer.html">

<input type="submit" value="Do it!"/>

</form>

![00068.jpeg](image_rsrc3F0.jpg)This <form> contains a single <input> tag that is decorated with the type="submit" attribute, and it represents a submit button. The action property of <form> is set to ProcessAtServer.htlm, so when the user clicks the submit button, the content of the form will be sent to that page. Of course, as shown in the figure below, this form does not have any other useful element, so actually there is no information to send to the action page.

A very simple and useless web form

So, let’s create a form with a few real input fields:

<form action="#">

<input name="fname" />

<br />

<input name="lname" />

<br />

<input type="submit" value="Do it!"/>

</form>

This markup contains two input fields, having the names fname (first name) and lname (last name), respectively. Their corresponding <input> tags are not decorated with the type attribute so that these fields will be rendered as text boxes. The action attribute of the form is set to #, which will send the form data to the page itself.

![00069.jpeg](image_rsrc3F1.jpg)Let’s assume, you’ve put this code into the form.html file. When you display it in the browser, you can type data into the text boxes, as shown in figure below.

A simple form with two input fields

When you click the submit button, the form sends the data to the form.html file through a web request. The page is displayed again, with empty input fields. Only the address bar of your browser tells you that the page is displayed as a result of web request from the form, its URL is something like this:

http://127.0.0.1:8080/?fname=John&lname=Smith#

In the URL you can see the form data as ?fname=John&lname=Smith, indicating that this information was passed through the URL.

## Controls Overview

In these small markup snippets above you’ve already seen a few controls, such as the textbox and the submit button, but there are much more. You will learn to use them through exercises, but first you’ll be given a short overview of them.

So, as you already know, <form> is the markup element that encapsulates all controls. Most controls can be rendered with the <input> element that has a type attribute. This attribute specifies the type of the control, it determines how the control is rendered in the browser, and how it behaves. If you do not specify type, the control will be a textbox (and this is the same as setting type to text). You can choose from several kind of buttons, such as button (clickable button mostly used with JavaScript), checkbox, radio (radio button), submit (submits the form), image (an image as the submit button), and reset (resets all form values to their defaults).

There are several predefined textual controls with some extra semantics, such as password (characters are masked), email (defines a field for an email address), url (field for entering an URL), tel (field for a telephone number), search (field for search text), and number (field for entering a number). The type file provides a file-select field with a Browse button for file uploads. You can place hidden fields in a form, used to set form values programmatically.

HTML5 adds a number of date and time related controls to the old markup through the type attribute of <input>: date (date control with year, month, day, and no time), datetime (date and time control with the precision of fraction of a second, based on UTC time zone), datetime-local (date and time control with no time zone), month (a month and year control), time (a control for entering time, no time zone), and week (a week and year control, not time zone).

NOTE: Using date and time related controls on your web pages means you’re walking on thin ice. These controls are relatively new, and—as of this writing—in most browsers they are rendered only as text boxes, and not as nice date and time pickup controls.

HTML5 also adds two other types, color (color picker), and range (a kind of slider to choose a number in a specified range).

Beside <input> there are a few other HTML tags to allow specifying user data. With <select>, you can define a dropdown list with option values. To type in longer text, use the <textarea> element.

The <fieldset> element lets you group related controls into sections, the <legend> element adds a caption to a <fieldset> element.

Input fields do not tell anything about their role to users. You can use the <label> element to provide appellation to input controls. Besides adding a descriptive text, <label> element provides an improvement for people who uses mouse, because when the user clicks on the text within <label>, it allows it for control (for example a check box, or radio button), or moves the focus to the related input field.

Used with the button, submit or reset types, <input> elements are rendered as pushbuttons. With the <button> element you can create clickable buttons with the same behavior, but you can create compound button content instead of a simple text.

# Chapter 4.         Frames, Colors, And Layout Of HTML

## HTML Frame

Frames used to decrease day by day. At the present time the frame is not useless, because it is quite hard to print finished pages using frames together. Apart from it, many dislike it. Instead, CSS is now used to divide a page into more than one section. But there is a need to have some idea about frames to enrich the knowledge base of HTML.

Example Programs

<html>

<head>

<title> [www.lifeguruji.tk](http://www.tutohost.com/) </title>

</head>

<body bgcolor ="#00cc99">

<frameset rows ="12%,88%">

<frame src = "style.html" scrolling ="no">

<frameset cols ="27%,74%">

<frame src ="link.html">

<frame src ="textfor.html">

</frameset>

</frameset>

</body>

</html>

Create a folder with any file name and put it in style.html, link.html and textfor.html three html files. Open a Notepad and enter the code above and click on Save as the File menu, save as file name: index.html, Save as type: All files, open the index.html file using Mozilla Firefox or Google Chrome, and check how it’s look...

Discuss the program

First, frameset rows = "12%, 88%"> is divided into two parts along the row on the entire page.

Through the frameset cols = "27%, 74%"> the bottom row is divided into two sections along the column.

<frame src = "style.html" scrolling = "no"> The style.html page is displayed in the first frame.

<frame src = "link.html"> and <frame src = "textfor.html"> Arrangements are made to display links.html and textfor.html pages in the 1st and 2nd frame respectively.

## Eye Frames

Eye frames are one of the main ways to display one or more web pages on a web page. It is important to publish a link to different web pages on topics relevant to the presentation, as well as it is not bad if it can be scrolled in the short space.

Example Programs

<html>

<head>

<title> [www.lifeguruji.tk](http://www.tutohost.com/)</title>

</head>

<body bgcolor=" #f00">

<center>

<h2 style="color:#f00">This is an example of iframe.</h2><br/>

<iframe src="[http://www.lifeguruji.tk/bangla/html/](http://www.tutohost.com/bangla/html/)" width="350" height="170">

<p>This browser does not support iframes.</p>

</iframe>

</center>

</body>

</html>

Open a Notepad and enter the code above and click on Save as from the File menu, save as file name: index.html, Save as type: All files, open the index.html file using Mozilla Firefox or Google Chrome, and check how it’s look.

![00015.jpeg](image_rsrc3F2.jpg)

Sorry I don’t have internet at the moment….

Program discussion

<Iframe> </iframe> tags are used to create eyebrows.

width = "350" height = "170" These two attributes indicate the size of the I frame.

If a browser does not support the I frame, then this page does not support iframes. <P> This browser does not support iframes. </P> The text will be displayed.

## Colors And Codes

The use of colors on web pages is very important. A web page is composed of one or more paragraphs, titles, tables, borders, borders, etc. Each of these elements has to use some colors. To specify the background color of a particular page, after writing body in the <body> tag, bgcolor = "" should be written with a space followed by black, silver, gray, white, marrow, red, purple, fuchsia, green, lime, OLIVE, YELLOW, NAVY, BLUE, TEAL, and AQUA, any one of these sixteen colors will be visible in the page's background. Since case is not sensitive, there is no problem writing in lower case, as written, <body bgcolor = "green">.

Apart from the hexadecimal code, the background color can also be selected. For example, the above code can be written as: <body bgcolor = "# 00FF00">

The color piker can easily be collected for different color hexadecimal codes. Apart from the chart below, you can also do the job. The hexadecimal code has to start with a # symbol at the beginning of the code.

There is another interesting method to give a background color. These three colors are red, green and blue, and all the other colors are composed of these three colors. If you combine these three colors and create new colors, then it is not bad. To accomplish this task, the green background can be written as follows

<body bgcolor = "rgb (0,255,0)">.

Here rgb stands for red green blue (0, 255,0), meaning that the colors of red, green, blue, respectively, are 0%, 100%, 0% because of the pure green color here. And any color value can be up to 0-255\. Since the value of g or green is 255 so that is 100%. By changing the color of the three colors to 0-255, you can create new colors as desired.

Example Programs

<html>

<head>

<title> [www.lifeguruji.tk](http://www.tutohost.com/)</title>

</head>

<body bgcolor="green">

<h2 style=" color:#ff0000" >

This is the body of your web site.

</h2>

<p style="color:#093">

This is a paragraph.<br/>

This is a paragraph. <br/>

This is a paragraph.<br/>

This is a paragraph.<br/>

</p>

</body>

</html>

Open a Notepad and enter the code above and click on Save as from the File menu, save as file name: index.html, Save as type: All files, open the index.html file using Mozilla Firefox or Google Chrome, and check how it’s look...

![00016.jpeg](image_rsrc3F3.jpg)

## Layout

On the page layout, depending on how good a webpage should be. Previously all web site layouts were made using HTML only. Currently CSS is used with HTML. Rows and columns of <table> are used to create layouts using HTML only.

Example Programs

<html>

<head>

<title> [www.lifeguruji.tk](http://www.tutohost.com/)</title>

</head>

<body bgcolor="green">

<table width="400" border="0">

<tr>

<td colspan="3" style="background-color: #93C;">

<h1> Web Page header</h1>

</td>

</tr>

<tr valign="top">

<td style="background-color: #C99;width:100px;text-align:top;">

<p><b>Side bar</b><br />

<a href="#">PHP</a>

<br />

<a href="#">HTML</a>

<br />

<a href="#">CSS</a>

<a href="#">Wordpress</a>

</p></td>

<td style="background-color:#EEEEEE;height:200px;width:400px;text-align:top;"><h2 style="color:#900">This is heading.</h2>

<p style="color: #006">This is a paragraph.This is a paragraph. This is a paragraph.<br />

This is a paragraph.This is a paragraph. This is a paragraph.<br />

This is a paragraph.This is a paragraph.This is a paragraph.<br />

This is a paragraph.This is a paragraph.This is a paragraph.</p></td>

</tr>

<tr>

<td colspan="2" style="background-color:#999;text-align:center;">

Copyright © 2018 by Omar Faruq</td>

</tr>

</table>

</body>

</html>

Open a Notepad and enter the code above and click on Save as from the File menu, save as file name: index.html, Save as type: All files, open the index.html file using Mozilla Firefox or Google Chrome, and check how it’s look...

![00017.jpeg](image_rsrc3F4.jpg)

# Chapter 5.         How to Put Images in HTML?

There is a famous quotation that “picture says a thousand words”. Quotation shows how powerful pictures are in terms of delivering a message. Web sites show pictures to make web pages more exciting, optical and lively.

How do we show image or picture on any web page?

Examples of Images

Let’s see an example of picture on web page. Please go to the following page in Wikipedia https://en.wikipedia.org/wiki/Albert_Einstein . You see images as shown below:

![00033.jpeg](image_rsrc3F5.jpg)

Images

Example   

You can see that I have marked two images – one is of Albert Einstein and other is of Wikipedia Logo. Don’t you agree that these images have made this page lively? Images on the web page can be used in two ways:

ü✓ One way is just show image. Just show; nothing else.

ü✓ Other way is to use image as hyperlink. It means when you click on the image, it will take you to some other page. How interesting!

## Learning The Details

How do we show image on web page? We use <img> tag for this purpose. Please check the example below:

<img src="location of the image" alt="alternate text" width="width in pixel" height="height in pixel"></img>

We start <img> tag and then we close with </img> tag like we do for any HTML tag. But then we use various other attributes to make sure image is shown on the web page. Let’s look into these attributes in the table below.

Table 6.1: Attributes of the <img> tag

<img>  tag  attribute   Purpose  

src   src stands for source.  Like  hyperlink,  you  enter  address  of  the  image  for  this   attribute.  Address is the location where this image has been stored.      

The address could be internet based image.  It means image is stored at   internet somewhere like any web page.  Example is Albert Einstein image   stored at Wikipedia.  Address is:  

https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Einstein_19 21_by_F_Schmutzer_-­‐_restoration.jpg/220px-­‐

Einstein_1921_by_F_Schmutzer_-­‐_restoration.jpg    

Or it could an address from your computer/laptop hard disk.  It means the   image is stored somewhere in your local computer hard disk.  You provide   folder location of the image.  Example is -­‐ “file://C:/  

Books\HTMLforKids/mybook.jpg”      

You can use most types of images such as jpg, jpeg, png, gif and bmp.      

alt   alt  stands  for  alternate  text.  This  is  the  text  shown  on  web  page  if  image   could  not  be  shown  on  web  page  due  to  some  reason.  It is like a backup   plan.  You want to show some text in case image could not be shown due to   some problem.  

width   This tells the width of the image.  If you don’t provide this value, then it will show   image in its original width.    

Width is measured in pixel.  One pixel is like a dot on the screen.  Just like you   measure distance in meter or centimeter; in the same way you measure   length of the image in pixel.  

height   Tells the height of the image.  Similar to width, it is also measured in pixel.    

If you don’t provide this value, then it will show image in its original height.      

Let me show you image in HTML. I am going to use Albert Einstein image address given in the table above and will show that in my HTML page. I will make height 200 pixel and width also 200 pixels; like square. The HTML looks like following:

<html>

<head>

<title></title>

</head>

<body>

<h2>Albert Einstein</h2>

<img

src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Einstein_1921_ by_F_Schmu tzer_-_restoration.jpg/220px-Einstein_1921_by_F_Schmutzer__restoration.jpg” alt="Albert Einstein" width="200" height="200"></img>

</body> </html>  

The HTML page will be displayed as shown below.

![00034.jpeg](image_rsrc3F6.jpg)

Web Page Display You  see  it  shows  image  in  the  square  size  (200  x  200)  as  I  have  mentioned  in  <img>  tag  attribute.  

What will happen if some problem comes with image?  For example, you give wrong address to image.  I suggest you try it yourself.    

You observed it right. It is showing Alternate Text as defined in <img> tag attribute in place of the image.

Let’s move next! What about using image as hyperlink? Sounds great! Right? Following is the structure of hyperlink tag:

<a href="Address of web page"> text of hyperlink </a>

To make image as hyperlink, you will replace  text of hyperlink with <img> tag. For example, if I want to make image of Albert Einstein hyperlink which will take me to Wikipedia page, then my HTML <a> tag will look like the following:

<a href=" https://en.wikipedia.org/wiki/Albert_Einstein"> <img

src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Einstein_1921_ by_F_Schmu

tzer_-_restoration.jpg/220px-Einstein_1921_by_F_Schmutzer_-_restoration.jpg” alt="Albert Einstein" width="200" height="200"></img> </a>

Is this not simple and intuitive? I am sure you will agree with me.

# Chapter 6.         HTML Tables

Tables are very useful to represent the data in grid format. The data is divided into rows and columns. It helps us to understand the data on two axes. Each block in the table is called as table cell. Let’s take a look at how table is created in the HTML.

## Table Creation

<table> element is used to create a table. The contents of the table are written out row by row. <tr> element is used to represent a start of each row. <tr> means table row. Each cell of the table is represented using a <td> element. A table row can also be divided into table headings with the <the> tag. Let’s take a closer look at table creation with an example 

<!DOCTYPE html>

<html>

<body>

<table>

<tr>

<td>A</td>

<td>X</td>

<td>1</td>

</tr>

<tr>

<td>B</td>

<td>Y</td>

<td>2</td>

</tr>

<tr>

<td>C</td>

<td>Z</td>

<td>3</td>

</tr>

</table>

</body>

</html>

![](image_rsrc3F7.jpg)

Table looks good with borders. We will learn how to draw borders around the tables using CSS.

## Table Headings

The heading for either a row or column is represented using <th> element. <th> means table heading. Foe an empty cell you should use <td> or <th> element otherwise the table will not be created correctly. The scope attribute can be used on the <th> element to indicate whether it is row or column. It takes the values, row to indicate heading for a row or col to indicate heading for a column.  The contents of <th> element is displayed in the bold and centered way. Table can also be given caption using <caption> tag.

<!DOCTYPE html>

<html>

<body>

<table>

<caption><b>Ticket Sales</b></caption>

<tr>

<th></th>

<th scope="col">Saturday</th>

<th scope="col">Sunday</th>

</tr>

<tr>

<th scope="row">Tickets Sold</th>

<td>50</td>

<td>20</td>

</tr>

<tr>

<th scope="row">Total Sale</th>

<td>100</td>

<td>150</td>

</tr>

</body>

</html>

![](image_rsrc3F8.jpg)

## Spanning Columns

Sometimes you may need the entries in the table to stretch across many columns. For this purpose, colspan attribute is used. It indicates how many columns cell should run across.

<!DOCTYPE html>

<html>

<head>

<style>

table, th, td {

border: 1px solid black;

border-collapse: collapse;

}

th, td {

padding: 5px;

text-align: left;   

}

</style>

</head>

<body>

<h2>Cell that spans two columns:</h2>

<table style="width:100%">

<tr>

<th>Name</th>

<th colspan="2">Telephone</th>

</tr>

<tr>

<td>Mr ABC</td>

<td>666 77 854</td>

<td>888 77 855</td>

</tr>

</table>

![](image_rsrc3F9.jpg)

## Spanning Rows

In order to span a cell more than one row, you can use the rowspan attribute. Check example below.

<html>

<head>

<style>

table, th, td {

border: 1px solid black;

border-collapse: collapse;

}

th, td {

padding: 5px;

text-align: left;   

}

</style>

</head>

<body>

<h2>Cell that spans two rows:</h2>

<table style="width:100%">

<tr>

<th>Name:</th>

<td>Mr XYZ</td>

</tr>

<tr>

<th rowspan="2">Telephone:</th>

<td>222 77 854</td>

</tr>

<tr>

<td>888 77 855</td>

</tr>

</table>

</body>

</html>

![](image_rsrc3FA.jpg)

There is lot of code in HTML for formatting the table. But now we can use CSS for better formatting. Hence, details about table formatting in HTML have been omitted.

# Chapter 7.         Fundamentals Of CSS

Web page development used to be relatively simple.  Developers simply write a Web page in HTML that can be accessed by other similar computers.  But times are changing in two ways.  First, Web sites are becoming vastly more complex, often with hundreds if not thousands of Web pages, dynamic HTML that adjusts to different users, and greater demands from the customer base.  Writing a page at a time can be a nightmare for developers, a problem for maintenance, and can cause inconsistencies across pages within a Web site that annoy the customers or viewer.

Second, Web pages used to be accessed by a computer with a monitor, or even a laptop with a reasonable viewing area. Now we access Web pages with tablets, small web books, phones, and even black and white eBook readers (like that Amazon Kindle, pre-Fire). Viewers using non-computer devices can get very frustrated as the viewing area exceeds the screen by several thousand percent, or keystrokes are required, or data entry exists with no easy way to enter the data.  There is a wide diversity of browsers on the market now, but often, Web developers insist on developing for the 1024 x 768 pixel (or larger) computer monitor.

Web developer or managers should try to make their Web pages as universally accessible and available to their viewers or client base as possible, including those who want to view content on a smaller device. This can be done with newer technology, newer formatting, and newer Web page validation that have not been available for that long.

Previous versions of HTML (versions 3.2 and before) make use of the<font> tag and background tags for every HTML element, so that a table at the top of the page could (and often did) have different formatting than a table at the bottom of the page. The result was that many Web pages had vastly different appearances in HTML 3.2.  Studies showed that this annoyed the users.  A user who was used to one page would click on a link and be exposed to a whole new page, with new formatting, new form and table colors, and an overall new look.  HTML 4.0 attempted to change this, by standardizing the look of every page, often through the use of a Cascading Style Sheet (also known as a CSS).  The conceptual difference between HTML 3.2 (and before) and HTML 4.0 (and beyond).

![00033.jpeg](image_rsrc3FB.jpg)

Conceptual Changes in Html 4.0

This shows how we can manage the formatting of a page from a single CSS.  By using a single CSS linked to every page on your site, you not only streamline the look of your Web page across your site, but you also streamline maintenance and development costs by defining the formatting of page elements (like tables, text, and lists) only once.

## Html Styles

The ways of formatting Web pages that were accepted in the 1990s and early 2000s have fallen out of favor. 

Implementing styles requires some changes to your HTML.  To make formatting consistent, you now use a style attribute to determine how something should look.  This caused a change in the HTML language.  Older tags, like the <font> tag, and older attributes, like bgcolor or border that used to control the appearance of HTML elements are now considered deprecated, or obsolete.  The format for the style attribute is as follows:

<tagname style="              attribute1: value1;

attribute2: value2;

attribute3: value3;">

You can usually apply a style attribute to almost any HTML tag (like<li>,<td>,<p>, etc.). However, if you are just typing, and you want to change the font, color, etc., of the next paragraph or the rest of the sentence, you can use either a <div> or a <span> tag. A <div> tag returns to the next line before going any further. A <span> tag keeps you on the same line, and allows you to make a single line have different fonts, colors, etc.  For example, the following <div> tag shows how to display text in red:

<div style="color: Red;">

This text will be red

</div>

## Fonts

Fonts are great for giving your page a crisp look that differs from the default font. The style attribute (or the <font> tag on older, pre-4.0 Web pages) is used to control the font displayed on your HTML page. Table 1 shows some things you can do with the style attribute and most tags, or use the <span> tag or the <div> tag (or the <font> tag, if you must).

|  | Current/Strict(New Way -- HTML 4.0) | Deprecated/Transitional(Old Way -- HTML 3.2) |
| Change the Font (Font Family) | <div style="font-family: Comic Sans MS, Arial, Helvetica;">Browser will try Comic Sans MS first, then Arial, then Helvetica</div> | <font face="Comic Sans MS, arial,helvetica">Browser will try Comic Sans MS first, then Arial, then Helvetica</font> |
| Set Font Size (Absolute) | <span style="font-size: 18pt;">define the font size</span> | <font size="5">define the font size</font> |
| Increase Font Size (Relative) | <td style="font-size: 2em;">increase the size of the text</td> | <font size="+3">increase the size of the text</font> |
| Decrease Font Size (Relative) | <span style="font-size: .6em;">decrease the size of the text</span> | <font size="-2">decrease the size of the text</font> |

Table 1\. Setting Fonts

pt vs. px vs. em

When you are specifying font size, you can specify the size in one of three ways:

*   pt gives you the absolute point size which is defined by the user's client machine.
*   px gives you the absolute pixel height, which is independent of machine (but can shrink with lower resolution and grow with higher resolution). This often used for setting borders and margins.
*   em gives you the relative height, which is gives the height as the number of times the current height. This is a relative measure, depending on the current size.

You choose what you need.

## Colors

Colors on computer monitors are defined by light, not pigment, so the primary colors are red, green, and blue.  Also unlike pigments, combining all the colors of light results in a white light, whereas ![00034.jpeg](image_rsrc3FC.jpg)removing all the colors of light results in a black color.  Figure below shows how the primary colors mix, and how that mixture looks, at a very high level.

Colors are specified one of two ways. First, you can use an actual color (red, blue, purple, etc.) Second, you can use a RGB (red, green blue) representation of the color by providing the red component, the green component, and the blue component, each a number from 0 (hexadecimal #00 – black) to 255 (hexadecimal #ff – bright). For example, to get this color of purple, you specify <span style="color: #880088">. You can also use decimal with an RGB function, like <span style="color: rgb(133, 0, 133)">.

As with fonts, colors can be controlled using the <font> tag, but newer standards suggest using a style attribute, possibly in conjunction with a <span> or <div> tag.  Table 6 shows the HTML for some color manipulation.

|  | Current/Strict(New Way -- HTML 4.0) | Deprecated/Transitional(Old Way -- HTML 3.2) |
| Set the Color | <span style="color: red">Change text color to red</span> | <font color="red">Change text color to red</font> |
| Set the Background | <td style="background: rgb(221, 153, 221)">Change background to whatever color this is using RGB</td>              | <td bgcolor="#dd99dd">Change background to whatever color this is using Hex</td> |

Table 2\. Using Colors

## Alignment and Borders

You can use styles to control borders or to align images or text. The use of the float attribute can also make text float to the left or right with other text wrapping around the floating object. Table 7 shows some use of alignment.

|  | Current/Strict(New Way -- HTML 4.0) | Deprecated/Transitional(Old Way -- HTML 3.2) | Example |
| Align Text to the Right | <td style="text-align: right">929<div style="text-decoration: underline">+ 84</div>1013</td> | <td align="right">929<br><u>+ 84</u><br>1013</td> | 929+ 841013 |
| Center Text | <div style="text-align: center">Centered <br /> Text</div> | <center>Centered <br> Text</center> | CenteredText |
| Vertically Align Text (Top, Middle, Bottom) | <td style="vertical-align: top">vertical top</td> | <td valign="top"">vertical top</td> | vertical top |
| Center a Table | <table style="margin-left:auto; margin-right:auto"><tr><th>head 1</th><th>head 2</th></tr><tr><td>cell 1</td><td>cell 2</td></tr></table> | <table align="center"><tr><th>head 1</th><th>head 2</th></tr><tr><td>cell 1</td><td>cell 2</td></tr></table> |  |
| head 1 | head 2 |
| cell 1 | cell 2 |
|  |
| Place Border on Text (or anything else) | <divstyle="border-width: 5px;border-style: outset;border-color: blue;text-align: center">Text with border</div> | {Cannot be done without a single-cell table} | ![00035.jpeg](image_rsrc3FD.jpg) |

Table 3a. Alignment and Borders

(continued …)

|  | Current/Strict(New Way -- HTML 4.0) | Deprecated/Transitional(Old Way -- HTML 3.2) | Example |
| Place Border on Table | <tablestyle="border-width: 1px;border-style: outset;"><tr><tdstyle="border-width: 1px;border-style: inset;">cell 1</td><tdstyle="border-width: 1px;border-style: inset;">cell 2</td></tr><tr><tdstyle="border-width: 1px;border-style: inset;">cell 3</td><tdstyle="border-width: 1px;border-style: inset;">cell 4</td></tr></table> | <table border="1"><tr><td>cell 1</td><td>cell 2</td></tr><tr><td>cell 3</td><td>cell 4</td></tr></table> |  |
| cell 1 | cell 2 |
| cell 3 | cell 4 |
|  |

Table 3b. Alignment and Borders (continued)

# Chapter 8.         CSS

A style sheet is a type of document that contains formatting rules. A Web browser will simply read these rules and apply the formatting to your page. Using style sheets allows you to control page elements such as borders, colors, and margins, and even to embed fonts that aren't available locally on your computer.

Style sheets are officially known as CSS (for Cascading Style Sheets). CSS is a separate language with its own syntax, but don't let that frighten you. This language was specifically developed for formatting Web pages. It's so powerful that with a single command you can alter the appearance of a Web page.

You should always put your CSS rules into a separate file instead of embedding them directly into your Web page. The reason we do this is that it separates HTML code from your CSS rules and makes updating code much easier in the long run.

Before the introduction of CSS, Web designers looked for other ways to change the layouts on their Web pages. One such way was using table tags--a separate set of HTML tags that are used to make tables, table headers, table row, and so forth. But table tags were often misused. Instead of adding structure to a page, they were often being used to layout Web pages. And back before CSS, making changes to a large Web site with table tags or other formats was just difficult, time consuming and expensive, because you had to edit each page of a site individually.

CSS was specifically developed to eliminate the difficulties, expense, and time involved in using table tags. Just by editing a single CSS file you can instantly make changes to a large and complex Web site. For example, you can create a CSS rule to format font sizes, and every page on your Web site will then be updated to reflect those specific changes.

## Your First Style Sheet

Now we should put all of the things we've learned together and create your first CSS (Cascading Style Sheet).

If you're familiar with Web and have visited many Web sites, you'll know that your browser displays text links in blue and with an underline. (This is the browser's default (automatic) format display for text links.) But what if the blue links are at odds with the general look and feel of your own Web page?

You can build a style sheet rule that will change the text color of the link on your Web page. To do this, you simply have to use a CSS style attribute and declare it within an HTML element. Here is an example:

<a href="#" style:"color: red;"> Click Here </a>

A style attribute is made up of two parts: a property name and a value. Here is the format every attribute follows and how it looks as code:

<style: property; name: value;>

In this example, the property specifies the type of formatting that is applied to your HTML element. Here "color" is the property, which sets the color of the anchor link. The value is the actual name of the color ‒ "red. In another example of a CSS style attribute, the property name might be "font" and the value could be the "size" of font.

This CSS rule is commonly known as a statement. A statement is simply a piece of code; here, all it does is specifying the style property as color and make the anchor link ("Click Here") red (the color "value").

Create a new document in Sublime Text 2 by selecting File | New. Now type this code exactly as you see here:

<!doctype html>

<html>

<head>

<title> My First Style Sheet </title>

<meta charset="UTF-8" />

</head>

<body>

<p> <a href="#" style="color:red; text-decoration:none;">

Click Here </a> </p>

</body>

</html>

Once you've done this, save your file with the name colors.html in your HTML folder on your desktop. Now preview your file in your Web browser to check your work.

To remove the standard underlined text from your anchor link, use the text-decoration attribute and the value none (see example above, after color: red). The text-decoration is used to set the appearance of text – you can remove underlines, underline standard text, add a line above or through the middle of text and make the text blink.

The text-decoration attribute has the following possible values: underline, line-through, over line, none and blink. Here is an example of code for text decoration that makes the text blink:

text-decoration: blink;

Open up the Web page we've just been working on called colors.html and add the other values to the text-decoration attribute. Preview the file in your Web browser to see how your work is displayed.

<p> <a href="#" style="color:red; text-decoration:blink;">

Click Here </a> </p>

Try experimenting yourself by adding the values: underline, line-through and over line to the text-decoration attribute and see what happens.

## Inline Styles

Inline styles allow you to insert a property name and value of a style sheet right into an HTML tag. But you should try to avoid using this approach if you can. As Inline styles mix formatting with HTML markup, and it becomes difficult to make changes to your Web page: every style on a page must be hunted down in the source code ‒ as you'll soon see.

So here is our earlier example used to format an anchored link:

<a href="#" style="color:red; text-decoration:none;"> Click Here </a>

The rule above removes the default underline of the anchored link and makes the text color red. Inline style may seem much easier to use ‒ it's straightforward, and you can apply it wherever you want on a page. But if you format a page like this it can get quite messy and confusing. You'll soon realize why Web designers tend not to use this technique. Adding inline style to each and every HTML tag on your Web page not only makes the code difficult to read, but it is almost impossible to separate the presentation formatting (style sheets) from the actual HTML. For example, let's consider our earlier example but with several inline style rules added to the tag:

<a href="#" style="color:red; text-decoration:none; border-style: solid; border-color:blue; text-align: left; font-size: 16"> Click Here </a>

See how the anchor tag is already becoming a bit disorderly and chaotic. It's quite difficult to separate content ("Click Here") from the presentation formatting in the example above. So as good practice, HTML markup should always be in a separate, presentation-free document. If you can, try to avoid using inline styles entirely.

## The Anatomy of A CSS Rule

A style sheet is made up of rules. A rule is a formatting instruction that tells the Web browser to apply specific styles to your Web page.

Here is an example of a CSS rule that sets the color of a <p> paragraph element to red:

p { color:red;}

The CSS rule is then applied to our <p> paragraph element in the HTML document like this:

</p>

This shows an example of this paragraph style in action in a standard Web browser.

![00021.jpeg](image_rsrc3FE.jpg)

A css rule applied to the paragraph element

If you open up a style sheet to view the code in your browser, you'll see that CSS rules don't have any resemblance to HTML markup. Every CSS rule is basically made up of three things: selectors, properties and values. Ordinarily the property and value is always terminated by a semicolon(;).

Here is the format every CSS rule follows:

Selector {property: value;}

And here is what each part of the CSS rule actually means:

*   The selector is an HTML element that you want to apply formatting to. For example, the (<p>) paragraph tag can be used as a selector. A Web browser will then look for all the common elements in your Web page that match the selector and apply the code within the curly braces to your elements.
*   The property simply identifies the type of formatting you want to apply to your HTML element. So here you can choose from colors, fonts, sizes and so forth.
*   The value sets a value for the property. For example, if the property is color, then the value could be green or light blue.

Selectors, properties and values are essentially the basic building blocks of CSS rules. Once you begin to understand these, you're well on your way to becoming a style sheet guru.

## Creating an External Style Sheet

a {

color:red; text-decoration: none;

}

h1 {

font-family: arial, sans-serif

}

Before you go any farther, save your file with the name style.css in your main HTML folder on your desktop. A style sheet can have whatever name you want but must always use the file name extension .css. Remember, always save the style sheet in the same folder as your HTML pages, otherwise your page will not display the formatting.

Instead of embedding a style sheet directly into an HTML tag, you will be adding a link to the external .css style sheet from within the <head> portion of your document.

In the colors.html file, simply remove the inline style that was added to the anchor link previously. For comparison purposes, below are the old colors.html file with inline style and new colors.html file without inline style:

COLORS.HTML FILE WITH INLINE STYLE  ‒

<!doctype html>

<html>

<head>

<title> My First Style Sheet </title>

<meta charset="UTF-8" />

</head>

<body>

<h1> My First Style Sheet </h1>

<p> <a href="#" style="color:red; text-decoration:none;">

Click Here </a> </p>

</body>

</html>

COLORS.HTML FILE WITHOUT INLINE STYLE ‒

<!doctype html>

<html>

<head>

<title> My First Style Sheet </title>

<meta charset="UTF-8" />

</head>

<body>

<h1> My First Style Sheet </h1>

<p> <a href="#"> Click Here </a> </p>

</body>

</html>

View the file in your web browser after you save it to check your work. You will see that the formatting rules in the style sheet has not yet been applied to your Web page. This is because we haven't told the browser to point (link) to the style sheet.

You have to add the <link> element to the <head> portion in your HTML document in order to do this. The <link> element simply points the browser to the external style sheet and the browser will then apply the style sheet's formatting rules to your page.

Here is the <link> element added to the <head> portion of our page:

<!doctype html>

<html>

<head>

<title> My First Style Sheet </title>

<link rel="stylesheet" href="style.css" />

<meta charset="UTF-8" />

</head>

<body>

<h1> My First Style Sheet </h1>

<p> <a href="#"> Click Here </a> </p>

</body>

</html>

The <link> element has two parts to it. The rel attribute simply defines the relationship between the current page and the linked document. In actual fact, you are telling the Web browser it's a style sheet.

The href attribute (href stands for hypertext reference) points to the actual location of the external style sheet. When you're linking to a style sheet the rel attribute should always be a style sheet.

Save the file and then open it in your Web browser to see your work. Congratulations! You've just created your first external style sheet.

# Chapter 9.         CSS Links, Tables, And Forms

You can use a lot of other CSS properties to work with links and tables. You will learn how you can add color to each column of the chart to make it stands out of the rest. Similarly, you will also learn how to beautify the forms such as submissions forms, survey forms and any other form that you have created in HTML. 

You will be able to create beautiful buttons that can be integrated into the forms. Each code example also contains the displayed results of the code. You can take up the code, recreate it, modify or run it to see how it works. Even simply reading it will give you a general idea of how you have to proceed. 

<html>

<head>

<style>

a {

color: green;

}

</style>

</head>

<body>

<h1> Let me tell you a story.</h1>

<h2><b><a href="default.asp" target="_blank">Watch the video story here.</a></b></h2>

<p> Once, there was an eagle that flew high in the skies,

<br> touching upon the tip of the mountains. 

<br> One day she found a ring, stuck in the branch of an apple tree. </p> 

<p>She took it and flew to her nest. While playing with it, she got her head stuck in it. 

<br>She didn't panic or hit her head on the stump of a tree to get rid of it. 

<br>One day she drenched her head in oil and the ring came off of her neck.</p>

</body>

</html>

The result of the above style is as under. You can see the second line of code which has got a link hidden inside. 

Let me tell you a story.

Watch the video story here.

Once, there was an eagle that flew high in the skies, 

touching upon the tip of the mountains. 

One day she found a ring stuck in the branch of an apple tree.

She took it and flew to her nest. While playing with it, she got her head stuck in it. 

She didn't panic or hit her head on the stump of a tree to get rid of it. 

Then, one day she drenched her head in oil and the ring came off of her neck.

------------------------

CSS links are critical because many a time you have to connect your webpage to another website to offer your users an amazing and fruitful experience. There are four kinds of links that you can use for different purposes. They are named as a: link, a: hover, a: active, a: visited. Each link has a specific purpose. For example, a: hover is used to allow users to hover over the mouse on the link and make it open. Let’s try to create links by all the four methods. 

<html>

<head>

<style>

/* This is an unvisited link */

a:link {

color: green;

}

/* This is a visited link. */

a:visited {

color: blue;

}

/* This is a hover link. */

a:hover {

color: violet;

}

/* This is a selected link. */

a:active {

color: red;

}

</style>

</head>

<body>

<h1> Let me tell you a story.</h1>

<h2><b><a href="default.asp" target="_blank">Watch the video story here.</a></b></h2>

<p> Once, there was an eagle that flew high in the skies,

<br> touching upon the tip of the mountains. 

<br> One day she found a ring, stuck in the branch of an apple tree.</p> 

<p>She took it and flew to her nest. While playing with it, she got her head stuck in it. 

<br>She didn't panic or hit her head on the stump of a tree to get rid of it. 

<br>One day she drenched her head in oil and the ring came off of her neck.</p>

</body>

</html>

You might be thinking that I had entered four links, but just one color can be seen in the results if you have already tested the code. Links change their status. In the start, they are unvisited. Then you hover your mouse over them. Then you click them open and leave them visited. So, technically, you can add four different colors according to the status of your link. Let’s see what other things we can do to the links. Also, we can decorate the text of links and also add color to the background. Let’s see how to do that. 

<html>

<head>

<style>

/* This is an unvisited link */

a:link {

color: green;

text-decoration: none;

background-color: yellow

}

/* This is a visited link. */

a:visited {

color: blue;

text-decoration: none;

background-color: gray

}

/* This is a hover link. */

a:hover {

color: violet;

text-decoration: underline;

background-color: pink

}

/* This is a selected link. */

a:active {

color: red;

text-decoration: underline;

background-color: hotpink

}

</style>

</head>

<body>

<h1> Let me tell you a story.</h1>

<h2><b><a href="default.asp" target="_blank">Watch the video story here.</a></b></h2>

<p> Once, there was an eagle that flew high in the skies,

<br> touching upon the tip of the mountains. 

<br> One day she found a ring, stuck in the branch of an apple tree.</p> 

<p>  She took it and flew to her nest. While playing with it, she got her head stuck into it.

<br> She didn't panic and hit her head into the stump of the tree to get rid of it. 

<br> One day she drenched her head in oil and the ring moved out of her neck. </p>

</body>

</html>

## CSS Tables

CSS allows you to transform the way your tables look in HTML. You can add colors to the headings and to the columns. The font style and font size of the text inside the tables can also be changed. Let’s create one. 

<!DOCTYPE html>

<html>

<head>

<style>

#countries {

font-family: "Courier New", Gerogia, Helvetica, sans-serif;

border-collapse: collapse;

width: 80%;

}

#countries td, #countries th {

border: 2px solid green;

padding: 6px;

}

#countries tr:nth-child(even){background-color: violet;}

#countries tr:hover {background-color: #ddd;}

#countries th {

padding-top: 15px;

padding-bottom: 15px;

text-align: left;

background-color: #ffAc2b;

color: gray;

}

</style>

</head>

<body>

<table id="countries">

<tr>

<th>Country</th>

<th>Capital</th>

<th>Reasons for fame</th>

</tr>

<tr>

<td>Germany</td>

<td>Berlin</td>

<td>BMW</td>

</tr>

<tr>

<td>United States of America</td>

<td>Washington DC</td>

<td>Marvel</td>

</tr>

<tr>

<td>China</td>

<td>Beijing</td>

<td>cheap products</td>

</tr>

<tr>

<td>Pakistan</td>

<td>Islamabad</td>

<td>Footballs</td>

</tr>

<tr>

<td>Japan</td>

<td>Tokyo</td>

<td>Robotics</td>

</tr>

<tr>

<td>United Kingdom</td>

<td>London</td>

<td>Thames</td>

</tr>

<tr>

<td>Egypt</td>

<td>Cairo</td>

<td>Pyramids</td>

</tr>

<tr>

<td>India</td>

<td>New Delhi</td>

<td>Taj Mehal</td>

</tr>

<tr>

<td>Brazil</td>

<td>Sao Paulo</td>

<td>Statue of Jesus</td>

</tr>

<tr>

<td>Kingdom of Saudi Arabia</td>

<td>Riyadh</td>

<td>Pilgrimage</td>

</tr>

</table>

</body>

</html>

The results of the above code example can be seen below. You can change the values and yield out a different output in the internet browser. Tables are an essential element for a web page. You need them if you are running a website that displays information about the rise and fall in the prices of stock market shares. If you don’t style them properly with CSS, your visitors are not going to like their dull and boring look. Appropriately colored tables appear well on the website and keep visitors engaged for a while. 

| Country | Capital | Reasons for fame |
| Germany | Berlin | BMW |
| United States of America | Washington DC | Marvel |
| China | Beijing | cheap products |
| Pakistan | Islamabad | Footballs |
| Japan | Tokyo | Robotics |
| United Kingdom | London | Thames |
| Egypt | Cairo | Pyramids |
| India | New Delhi | Taj Mehal |
| Brazil | Sao Paulo | Statue of Jesus |
| Kingdom of Saudi Arabia | Riyadh | Pilgrimage |

You can alter the colors, the border, and padding by making slight changes in the HTML document. Adding more columns or rows to suit your specific requirement is also being done. In the above example, I have added background colors, padding, border colors and have also adjusted the width of the columns. You can take the example document and customize for learning practice.

## CSS Forms

HTML provides us with an easy way to create different types of forms that we can use to collect user information like their usernames, passwords, and email addresses. Some are subscription forms while others are survey forms. When we create an HTML form, its look is rigid and dull. Thanks to CSS, we can change that. We can make it look exceptionally well. Let’s create a form and then transform its look by adding some simple CSS properties. 

<!DOCTYPE html>

<html>

<style>

input[type=text], select {

width: 100%;

padding: 15px 25px;

margin: 10px 0;

display: inline-block;

border: 2px solid green;

border-radius: 6px;

box-sizing: border-box;

}

input[type=submit] {

width: 50%;

background-color: pink;

color: black;

padding: 12px 18px;

margin: 10px 0;

border: 2px solid green;

border-radius: 2px;

cursor: pointer;

font-size: 25px

}

input[type=submit]:hover {

background-color: #45b049;

}

div {

border-radius: 4px;

background-color: #f1f1f1;

padding: 15px;

}

</style>

<body>

<h1>I will be using CSS to style this raw HTML Form</h1>

<div>

<form action="/action_page.php">

<label for="name">Please enter your first Name</label>

<input type="text" id="name" name="firstname" placeholder="Plese enter here..">

<label for="lname">Please enter your last Name</label>

<input type="text" id="lname" name="lastname" placeholder="Please enter here..">

<label for="country">Where do you live?</label>

<select id="country" name="country">

<option value="USA">USA</option>

<option value="canada">Canada</option>

<option value="UK">UK</option>

<option value="china">China</option>

<option value="pakistan">Pakistan</option>

<option value="france">France</option>

</select>

<input type="submit" value="Submit">

</form>

</div>

</body>

</html>

The result is as under:

![00001.jpeg](image_rsrc3FF.jpg)

I have styled the border, the input fields, the submit button and a lot more. Let’s learn more about designing the buttons, as they are an essential part of forms on your web page.

<!DOCTYPE html>

<html>

<head>

<style>

input[type=refresh], input[type=submit], input[type=process] {

background-color: #4CAFBB;

border: 2px solid green;

color: white;

padding: 19px 34px;

text-decoration: none;

margin: 6px 4px;

cursor: pointer;

}

</style>

</head>

<body>

<h1>You are seeing styled input buttons.</h1>

<input type="refresh" value="Refresh It">

<input type="process" value="Process">

<input type="submit" value="Submit">

</body>

</html>

The result is as under:

![00002.jpeg](image_rsrc3FG.jpg)

In the end let’s see an example of a complete form. 

<!DOCTYPE html>

<html>

<head>

<style>

* {

box-sizing: border-box;

}

input[type=text], select, textarea {

width: 50%;

padding: 8px;

border: 1px solid #bbb;

border-radius: 2px;

resize: vertical;

}

label {

padding: 10px 0;

display: inline-block;

}

input[type=submit] {

background-color: #4CAF50;

color: white;

padding: 10px 18px;

border: none;

border-radius: 4px;

cursor: pointer;

float: right;

}

input[type=submit]:hover {

background-color: #45a049;

}

.container {

border-radius: 7px;

background-color: #f2f2f2;

padding: 15px;

}

.col-25 {

float: left;

width: 50%;

margin-top: 4px;

}

.col-75 {

float: left;

width: 50%;

margin-top: 4px;

}

/* Clear floats */

.row:after {

content: "";

display: table;

clear: both;

}

/* Responsive layout  */

@media screen and (max-width: 400px) {

.col-25, .col-75, input[type=submit] {

width: 50%;

margin-top: 0;

}

}

</style>

</head>

<body>

<h2>This is an example of a responsive Form</h2>

<p>You will have to resize the browser window to see the effect.</p>

<div class="container">

<form action="/action_page.php">

<div class="row">

<div class="col-25">

<label for="nname">Please enter your First Name</label>

</div>

<div class="col-75">

<input type="text" id="fname" name="firstname" placeholder="Please enter here..">

</div>

</div>

<div class="row">

<div class="col-25">

<label for="lname">Please enter your Last Name</label>

</div>

<div class="col-75">

<input type="text" id="lname" name="lastname" placeholder="Please enter here..">

</div>

</div>

<div class="row">

<div class="col-25">

<label for="country">Please choose your country</label>

</div>

<div class="col-75">

<select id="country" name="country">

<option value="usa">USA</option>

<option value="canada">Canada</option>

<option value="uk">UK</option>

</select>

</div>

</div>

<div class="row">

<div class="col-25">

<label for="bio">Please enter your bio here.</label>

</div>

<div class="col-75">

<textarea id="bio" name="bio" placeholder="Write here.." style="height:200px"></textarea>

</div>

</div>

<div class="row">

<input type="submit" value="Submit">

</div>

</form>

</div>

</body>

</html>

Your form will look like this:

![00003.jpeg](image_rsrc3FH.jpg)

# Chapter 10. Image Manipulation in CSS

You can add images to your documents using the img tag, or you can add a background image to the entire document.

Setting an image as background for a website.

You can use body tag’s background-image property to set a background image for the entire page.

body { background-image: url('draft.gif'); }

![](image_rsrc3FJ.jpg)

Positioning the background Image

Use the background-position property to specify where your background image will appear.

body {

background-image: url('draft.gif');

background-position: bottom right;

background-repeat: no-repeat;

}

![](image_rsrc3FK.jpg)

You can use the following keyword combinations with the background-position property:

| Keywords |  |
| top left | center left | bottom left |
| top center | center center | bottom center |
| top right | center right | bottom right |
|  |  |  |

These keywords can be written in either order. For example, “top left” and “left top” will both work correctly. The other value will default to center if you only specify a single value.

You can also use percentages to set the position.

background-position: 30% 80%;

If you want to position the image in the top left 0% 0% is the value, and 100% 100% would place it in the bottom right. Setting the background-position to 50% 50% would center the image, as would center center.

The following list shows how keyword settings match percentage settings:

| Keywords | Percentages |
| left top | 0% 0% |
| center top | 50% 0% |
| right top | 100% 0% |
| left center | 0% 50% |
| center center | 50% 50% |
| right center | 100% 50% |
| left bottom | 0% 100% |
| center bottom | 50% 100% |
| right bottom | 100% 100% |

If you use keywords or percentages, your background image’s position will adjust to the size of the window. You can also use pixels to set a non-adjusting position:

background-position: 20px 20px;

Adjusting background color or image position.

You can use the background-clip property to specify whether the background includes the border, padding, or only the content.

| div {padding:10px;border: 5px dotted #000;background-color: #f00;background-clip:border-box;} | ![](image_rsrc3FM.jpg) |
| div {padding:10px;border: 5px dotted #000;background-color: #f00;background-clip:padding-box;} | ![](image_rsrc3FN.jpg) |
| div {padding:10px;border: 5px dotted #000;background-color: #f00;background-clip:content-box;} | ![](image_rsrc3FP.jpg) |

Adding more than one image to the background

With CSS3, you can specify multiple background images. If you are supporting old browser versions, you can specify one background image with the html tag and another with the body tag.

CSS approach

body {

background-image: url('logo.gif'), url('draft.gif');

background-position: bottom right, 50% 50%; 

background-repeat: no-repeat;

![](image_rsrc3FR.jpg)}

Older browser version approach

html {

background-image: url('logo.gif');

background-position: bottom right;

background-repeat: no-repeat;

}

body {

background-attachment: fixed;

background-image: url('draft.gif');

background-position: 50% 50%;

background-repeat: no-repeat;

}

Fixing a background image to avoid scrolling

You can use the background-attachment property to fix an image in place and prevent it from scrolling with rest of the page’s content.

body {

background-attachment: fixed;

background-image: url('draft.gif');

background-position: 50% 50%;

background-repeat: no-repeat;

}

| Value | Description |
| repeat | The background repeats horizontally and vertically.This is the default setting. |
| repeat-x | The background repeats horizontally but not vertically. |
| repeat-y | The background repeats vertically bit not horizontally. |
| no-repeat | The background does not repeat horizontally or vertically. |

How do I resize a background image to fit an element?

You can use the background-size property to resize a background image to fit a larger or smaller element automatically.

| Value | Description |
| contain | Scales the image so the height and width fit in the element |
| cover | Scales the image so the height or width fits (whichever is smaller) |
| length | Sets the height and widthIf you only specify one value, the image is sized proportionally. |
| percentage | Sets the height and width as a percentage of the parent elementIf you only specify one value, the image is sized proportionally. |

Adding a shadow to the image

You can use the box-shadow property to add a shadow to images.

img { box-shadow: 5px 5px 10px 10px #f00; }

You can specify the following options for the shadow:

| Value | Description |
| blur | Amount (in pixels) of blurring around the shadow's edge |
| color | The shadow's color |
| offset-x | Horizontal offset (in pixels) of the shadow |
| offset-y | Vertical offset (in pixels) of the shadow |
| inset | Specifies an inner shadow |
| spread | Size (in pixels) of the shadow0 – shadow is the same size as the element |

Using an image as a border

You can use the border-image property to use an image as an element's border.

border-image:url(diamond.png) 20 20 round;

The following properties can be used to specify border images for different sides of the element:

border-top-image

border-right-image

border-bottom-image

border-left-image

| Value | Description |
| border-image-source | Path to the image |
| border-image-slice | The image's height and width offset |
| border-image-width | The image's width |
| border-image-outset | The image's height |
| border-image-repeat | Whether the image should be repeat or stretch |

Wrapping text to an image

You can use the float property to wrap text around an image.

CSS rule

.caution {

float: left;

margin-right: 10px;

}

Usage

<p><img class="caution" src="caution.jpg" />

caution caution caution</p>

![](image_rsrc3FS.jpg)

The margin-left property can be used to add space between the image and the text.

Placing of text on top of image

You can assign negative values to the position, top, and left properties to position text on top of an image. If the version is below the picture, setting its top property to a negative value will move the text on top of the film.

CSS rule

.overlap {

position: relative;

top: -200px;

left: 180px;

color: #ffffff;

}

Usage

<img src="sample.jpg" />

<p class="overlap">floating text</p>

![](image_rsrc3FT.jpg)

Adding a border around the image

Borders are most often used with tables, but you can also add borders around images using the border properties.

img {

border-width: 3px;

border-style: solid;

border-color: #000000;

![](image_rsrc3FU.jpg)}

You can also use CSS shorthand to specify borders:

img { border: 1px solid #000000; }

The examples above will add a border to all images. You can create a class if you want to apply borders only to specified images.

.imgBorder { border: 1px solid #000000; }

<img class=“imgBorder” src=“sampleImage.jpg” />

Or, you can apply a border to all images inside a div tag:

CSS rule

#menuBar img { border: 1px solid #000000; }

Usage

<div id=“menuBar”><img src=“sampleImage.jpg” /></div>

Adding a drop shadow to an image

You can use Internet Explorer’s filter property to add a drop shadow to an image.

img {

filter: progid:DXImageTransform.Microsoft.dropShadow (offX='3', offY='5', color='#c0c0c0', positive='true');

}

![](image_rsrc3FV.jpg)

The filter property was created by Microsoft and is not a part of the CSS recommendation. It is only supported by Internet Explorer.

For more information about Internet Explorer filters, see “How do I use Internet Explorer's filters?”

For other browsers, you can use the box-shadow property can be used to add a drop shadow around an image. However, it will not add the drop shadow inside transparent images.

![](image_rsrc3FW.jpg)

Another option is to use HTML5's canvas element. See the following website for an example: [philip.html5.org/demos/canvas/shadows/various.html](http://philip.html5.org/demos/canvas/shadows/various.html)

Making an image transparent

Using the opacity property to make an image transparent can also be done. For Internet Explorer, you can use the IE-specific alpha filter.

![](image_rsrc3FX.jpg)

img {

filter:alpha(opacity=50);

opacity:.50;

}

Removing link borders from an image

You can set an image’s border property to “0” to remove the border that appears around image links by default.

img { border: 0; }

How do I zoom images when the user hovers over them?

You can use the hover pseudo class to change an image’s width and height.

First, wrap a link around the image:

<a href="javascript:void(0);">

<img src="clickstart.jpg" />

</a>

Then, specify the image’s width and height when the user hovers over the image’s link:

a:hover img { width: 800px; height: 400px; }

In this example, the image will expand to 800x400 when the user hovers over the image, and when the mouse moves from the image it will return to its original size.

Making image expand on hover

You can use the transition property to make an image expand when the user hovers over it and shrink when it loses focus. For example, you could provide a "thumbnail" of an image that expands to full-size when the user hovers over it.

CSS rule

.thumbTrans {

width: 50px;

height: 50px;

-moz-transition-property: width,height;

-moz-transition-duration: 4s;

-moz-transition-delay: 1s;

-webkit-transition-property: width,height;

-webkit-transition-duration: 4s;

-webkit-transition-delay: 1s;

-o-transition-property: width,height;

-o-transition-duration: 4s;

-o-transition-delay: 1s;

transition-property: width,height;

transition-duration: 4s;

transition-delay: 1s;

}

.thumbTrans:hover {

width: 100%;

height: 100%;

-moz-transition-property: width,height;

-moz-transition-duration: 4s;

-moz-transition-delay: 1s;

-webkit-transition-property: width,height;

-webkit-transition-duration: 4s;

-webkit-transition-delay: 1s;

-o-transition-property: width,height;

-o-transition-duration: 4s;

-o-transition-delay: 1s;

transition-property: width,height;

transition-duration: 4s;

transition-delay: 1s;

}

Making an image ‘pop-out’ on hover

You can use the hover pseudo class to rotate images and add a shadow.

img:hover {

box-shadow:1px 2px 5px #666666;

-moz-transform:rotate(5deg) scale(1.5);

-webkit-transform:rotate(5deg) scale(1.5);

transform:rotate(5deg) scale(1.5);

}

![](image_rsrc3FY.jpg)

Inserting content using CSS

Using the content property to insert content before or after an element can also be done.

To insert content at the top or bottom of the page:

body:before {

content: "Confidential";

font-weight: bold;

}

body:after {

content: "\000A Copyright 2012";

}

To insert content before an element:

h1:before {

content: ">> ";

color: silver;

}

To add quotes before and after an element:

p.quotes:before { content: open-quote; }

p.quotes:after { content: close-quote; }

To add curly quotes:

p.boldCurlyQuotes { quotes: "\201C" "\201D"; }

p.boldCurlyQuotes:before { content: open-quote; }

p.boldCurlyQuotes:after { content: close-quote; }

The following table provides the Unicode values for commonly-used characters that can be inserted using the content property.

| Symbol | Description | Unicode value |
| " | double quotation | 0022 |
| ' | single quotation (apostrophe) | 0027 |
| “ | double left curly quotation | 201C |
| ” | double right curly quotation | 201D |
| < | single left angle quotation | 003C |
| > | single right angle quotation | 003E |
| « | double left angle quotation | 00AB |
| » | double right angle quotation | 00BB |
| ` | grave accent | 0060 |
| ´ | acute accent | 00B4 |

# Chapter 11. Length Units

As you have followed this tutorial, you may have noticed that when you change the size of text using CSS, there are a number of options.

You can see this for yourself in TopStyle.

Create a new style sheet, and click the "New Selector" button.  Select the "Simple" tab and select h1 from the HTML elements list. Next click the "Add" button, followed by "OK".

![](image_rsrc3FZ.jpg)In the style inspector, scroll down to the font category and click on the font-size property.  Click the downward arrow on the right of this row to view the options available:

In this book, we will concentrate on the first two items in this list – Percentage and Length. 

Percentage is a relative measurement (i.e.,  it defines a size that is relative to another one).

Length is an absolute measurement, since it defines an exact analysis.  However, with precise measurements come units. 

What are the units for an absolute measurement?

Well, let's find out.  Click on the font-size dropdown arrow, and select length.

Another dialogue box opens up, with another dropdown box (set to the default 'px'). 

![](image_rsrc3G0.jpg)Click on the down arrow of that dropdown box, and you'll see several more options:

WOW!  That’s a lot of different units.

These units can be divided into two groups:

1.    relative units (size is comparable to something)

2.    absolute units (size is an exact measurement)

The 'relative' units are:

-      ex

-      em

-      px

(The percentage unit is also relative).

The 'absolute' units are:

-      cm

-      mm

-      pc

-      in

-      pt

The main reason for using absolute units is to freeze the design of the web page so that it always looks the same, no matter how it's viewed. 

When relative measurements are used, the web design may look different, depending on the users Web browser settings.

Let's look at an example. 

![](image_rsrc3G1.jpg)

There are two headers, one defined in absolute terms, and the other in relative terms.

Older web browsers use to allow users to change the size of the fonts in their browsers to:

-      Largest

-      Larger

-      Medium

-      Smaller

-      Smallest

The problem was that any font size defined in absolute terms would not increase in size because it was set in total measurements, and therefore would always appear the same size on the screen.  The font size defined in relative terms would increase in size.

If you increased the font size to "Largest", you’d see the relative header increase in size while the absolute header would stay at the same size.

To some extent, web browsers have taken away the functionality of absolute measurements because they introduced a zoom feature instead of a font size feature.  This then magnified all text, absolute or relative, to the same extent, throwing out some web designer's carefully designed layouts.

OK, let's consider the units for measurements, and what they represent.

The five absolute measurements are as follows:

1.    cm - centimeters

2.    mm - millimeters

3.    in - inches

4.    pc - picas (1/6 inch or 12 points)

5.    pt - points (1/72 inch)

It should be noted that even if absolute measurements did work properly in browsers with the new zoom features, they would only ever work as desired if the browser knew the size of the screen, and the number of pixels the screen displayed.  In many cases, the browser would have to guess!  This, together with the more recent addition of zoom features, means that absolute measurements aren't the best units to use when designing your pages so that we won’t be looking into these.

It was important to mention absolute measurements in this book though, because I am sure you will come across them when you are exploring the CSS of your own (and other people's) web pages.

So relative measurements provide us with the best solution, especially when we don't know what device the end user will be viewing the site on.  For example, nowadays they could be browsing on a computer, a tablet, a Smartphone, or even some e-readers.  With relative measurements, the font sizes will be comparable to the size of the screen, and therefore give the user the very best viewing experience.

Here are the relative measurements in some detail:

## EX

The 'ex' is a measurement relative to the size of the font's lowercase 'x'. I never use this measurement so that we won’t be looking at it in this book.

## PX

The px is a relative measurement in screen pixels.

Pixels offer the designer the best control over layouts. You will see them used a lot for things like borders, margins, padding, plus height and width of screen regions when creating CSS layouts without tables.

What pixels are not recommended for is text size.  Most modern browser won’t have a problem, but some of the older ones won’t resize pixel-based text. 

## Percentage

Percentage measurements are always relative to another value. For example, if we want to increase the spacing between lines of a paragraph, you can define the line-height as a percentage (it will be a percentage of the font size).

Say for example we have: line-height: 150%.  This will create a space between the lines that is 150% of the font size.  Therefore, if the font size is 10px, then the space between lines will be 15px.  It is wise to define the font-size in your CSS file if using percentages, otherwise results can be unpredictable in the different browsers. This is because the font-size will be taken from the web browsers default CSS file.

Here is an example showing line spacing using percentages:

![](image_rsrc3G2.jpg)

(9.1.html and 9.1.css)

## EM

The "em" is a relative measurement for the font size. Think of it as being the size of a capital "M" to help you remember it, though that isn't entirely accurate, but it is an excellent way to memorize it.

This is my preferred unit for defining text size.  Because it's a measurement relative to the font size, if we set a font-size of say 10px, then one em is equal to 10px.  2 em would be similar to 20px, and 1.5 em would be 15 px.

To make this as easy as possible, it's a good idea to define the font size in the style sheet as follows:

Create a new style sheet.

Click on the "New Selector" button, and then go to the "Simple" tab.

Select body from the HTML Element list, and then click the "Add" button followed by "OK".

You'll see the following in your style sheet:

body {

}

Whatever properties you enter will be the default properties for all elements on the page that appear between the <body></body> tags, i.e., everything.

I can define a default font-size like this:

body { font-size: 11px; }

This would make the default font size 11px.  Here is a web page where I have defined the default text size in this manner:

![](image_rsrc3G3.jpg)

(9.2.html and 9.2.css)

In some older browsers, if you choose a larger font size, these sizes will remain the same because we defined the default font as 20 px – an absolute measurement.  However, since most browsers now use the zoom feature, this is less of a problem that it used to be.  Nevertheless, just to be safe, we are probably better off defining the default font-size this way:

body {          font-size: 0.7em; }

This would make the default text size 70% of the default text size. So just what is the default text size? 

Well, every browser has its own default CSS that it uses to display web pages.   If you want to see what that size looks like in different browsers, create a style sheet that sets the body text size to 1em.

body {          font-size: 1.0em; }

Then create a web page with some text on it that uses the style sheet, and view it in a few different browsers, or just look at 9.3.html and 9.3.css, as I have done this for you.

Here is an excellent article on using em for sizing text.  Richard Rutter uses percentages instead of em to define the default font-size:

[http://clagnut.com/blog/348](http://clagnut.com/blog/348)

# Chapter 12. CSS IDs and Classes

ID selectors can only (or should only), be used ONCE on a web page, and identify ONE item on the page. 

By using an ID selector to reference two images on the page, I was breaking a CSS rule.  I should have used a CLASS instead.

ID Selectors and classes do mostly the same thing, BUT, an ID can only be used once on the page, whereas types can be used multiple times.

Before we look at classes, let me give you an easy way to remember this:

Your ID refers to YOU and you alone.  No one else can have your ID. 

A class is a group of people so that a level can refer to multiple individuals.

Therefore, an ID is only used once, and a class can be used multiple times.

For this reason, we will use IDs for page elements that only occur once, e.g., when we come to look at page layouts using CSS, we'll define IDs for the page header area, the right and left margins, the main content section, and the footer.  These are obvious choices, since each of those sections only occurs once per page.

We will use classes whenever we want to reuse a style on a page more than once, for example, the alignment of images, font styling, and bullet points, etc.

OK, we know that IDs and Classes can be used to override default display properties, but we still haven't looked at how to create or use them yet. Let's look at that now, so that you can start using them in your page designs.

## ID Selectors

Start TopStyle and click on the "New Selector" button.

Switch to the "advanced" tab, and you will see a pair of radio buttons (aka option buttons), labeled Class and ID.

![](image_rsrc3G4.jpg)

Select ID, and then in the box underneath the radio buttons, type in a name for your ID.  I typed in "logo" for mine, since I am going to create the ID to be applied to the logo on the page (it only appears once).

You will notice that as you type, TopStyle adds a '#' to the start of your ID.  Click the "Add" button (located above the radio buttons), and then click the "OK" button on the bottom right. This will add this selector to your style sheet.

In style sheets, the '#' symbol specifies that what follows is an ID. Here's how mind looks:

#logo {

}

You can now add some styles to the ID in exactly the same way we have done in other examples. I’ve added a few to mine, and here the finished logo ID:

#logo {

font-size: 3em;

font-variant: small-caps;

font-weight: bolder;

background-color: Silver;

font-family: Verdana, Geneva, Arial, Helvetica, sans-serif;

}

The idea of this ID is to change the text properties in the logo area of my page so that it is more extensive ("em" is a unit of measurement). My sample here uses small caps, bold, has a silver background, and is the Verdana, Geneva… font family.  You probably knew this from seeing the style sheet though, didn’t you?

You can see the effects of what this does to the page here:

![](image_rsrc3G5.jpg)

(8.1.html and 8.1.css)

To use the ID in a web page, you simply modify the HTML tag to include:

ID = "logo"

Here is the HTML code before modifying:

<p>Mylogo.com</p>

Just before the first single right-pointing angle quotation mark ">", is where you insert your ID code:

<p ID="logo">Mylogo.com</p>

Now, anything inside the <p></p> tags will be formatted according to the properties of the ID "logo".

You will notice that in the raw HTML, the text is lowercase apart from the first letter “M”.  In the web page preview (above), the book is small capitals, or small caps.  That is what happens when we add the property:  font-variant: small-caps;

Classes are used in a very similar way, so let's now take a look at that:

## Class Selectors

Create a new style sheet, and click on the "New Selector" button. Go to the "Advanced" tab again and click on the "Class" radio button. Enter a name for your class underneath the radio button. I am using "yellowhighlight" for mine, as that is what my class will do. i.e., highlight some text in yellow.

![](image_rsrc3G6.jpg)

You’ll notice that as you type, TopStyle adds a "." in front of the text you are typing.  In CSS, that "." specifies that whatever follows is a class.

OK, once done, click the "Add" button and then click "OK" to save the changes to your style sheet.

![](image_rsrc3G7.jpg)

This is what mine looks like:

.yellowhighlight {

}

I will make just one style change to the background color:

.yellowhighlight { background-color: Yellow; }

Now I can simply highlight a paragraph in yellow by adding the following code to the HTML tag for the paragraph I want to change:

class="yellowhighlight"

We add it in the exact same way that we added the ID earlier.  Insert it right after the first ">" of the <p> tag.

Here is the html code:

<p class="yellowhighlight">the paragraph goes here</p>

Now look at this page:

![](image_rsrc3G8.jpg)

(8.2.html and 8.2.css)

The second paragraph is now highlighted in yellow. Note how the <p> tag has been modified from <p> to <p class = "yellowhighlight">:

Here is the HTML. 

Because I used a class to define the highlighting, I can happily use it on multiple paragraphs if I want to:

![](image_rsrc3G9.jpg)

(8.3.html and 8.3.css)

That's how easy it is to identify and use classes. 

Before we leave this though, I can hear you asking: "But what if we only want to highlight certain text in a paragraph, and not the whole section?"

Well, the problem here is that the way we have used the class so far is to modify a complete HTML tag (the whole paragraph), because we declared the course within the <p> tag.

However, there is another option. You can use a "span" tag, to surround a selection of text, and apply a class only to the "spanned" text. To do this, you have to surround the text you want to highlight with a <span></span> tag.  Let’s look at an example:

<p>I only want to highlight <span>this text</span>here.</p>

We can now add the class within the opening <span> tag, right before the ">", in much the same way as you saw previously with the other tags:

<p>I only want to highlight <span class="yellowhighlight">this text </span>here.</p>

Here it is in action on a web page:

![](image_rsrc3GA.jpg)

(8.4.html and 8.4.css)

This is an integral part of the CSS course, with some big lessons to learn.  We learnt how to use IDs and Classes to modify the elements of our web pages, and although there's still more to cover on classes, we'll take a break for now. 

# Chapter 13. The Box Model In CSS

The basis of the CSS layout is the box model since it directs the way in which elements are shown and the way in which they associate with one another. Imagine every element on the page as a rectangular box. Every box is made of particular dimensions and takes up a particular measure of space. The space the box occupies depends on the content in it, as well as the margins and the padding borders around the content:

![00100.jpeg](image_rsrc3GB.jpg)So, the box model is what dictates the amount of space each element has on the page. Now, let’s dive somewhat deeper into this idea by revising the main components that constitute the CSS box model. Start thinking of each HTML component on the page as a box. In fact, you can apply a global style rule that will add a red outline to all the elements on the page. To do this, simply add the following style rule to the top of the stylesheet: 

* {

outline: 2px solid red;  

}

This will add an outline to all the elements on the page and it will let us easily visualize each of the items on the page as a box: 

![00101.jpeg](image_rsrc3GC.jpg)

Each element is designed with a box or rectangle. Now, to effectively understand the concept of the CSS box model, it is essential that we know the two ways in which elements can be displayed. Every detail has a display property, depending on the kind of item it is. The default of most items is inline or block. Now, block elements are composed of a separate block that has to take up the full width that is available. A few examples of block elements include, list items, paragraphs, divs and any heading tag.

You can observe how the block-level divs on our page, and also the lists and headings are taking up a whole line of content. They’re additionally forcing another new line of text before and after the next element. Also, inline elements only take up as much width as they have to. They don’t constrain any lines, and they remain in line with whatever remains of the rest of the text. A few examples of inline elements are images, anchor elements, and span tags. 

In the title span element, observe how its width consumes the space of its text, and the reason it’s shown on its line is because a block-level h1 part exists beneath it. The block-level h1 forces the new line. So now, let’s examine how the margins, borders, and padding interact with one another to form a box since it’s essential to understand. The box model is designed with four distinct parts.

![00102.jpeg](image_rsrc3GD.jpg)The core component and innermost area of the box is the content area. This is the area in which the actual content, such as image or text of the element is contained. Surrounding the area of the text is the padding area. Padding is used to give elements some breathing space. The next outermost part of the box is known as the border area of the box. Think of it as an outline to the box model. There are a range of styles for borders such as thickness and color. Finally, the margin area is positioned outside of the box. This is the space around an element that isolates it from different components.

The padding area makes space inside of the box, and the margin area makes space outside of and around the box. Imagine you have a cardboard box that you have filled with fragile items, but you have surrounded it with bubble wrap to cushion any impact. The padding in the box model is similar to the bubble wrap, in that it is added inside the box.  The Google Chrome dev tool provides a really clear view of the box model for each element on the page. If you click on View > Developer > Developer Tools:

![00103.jpeg](image_rsrc3GE.jpg)

It will display the chrome developer tool panel at the bottom of the page: 

![00104.jpeg](image_rsrc3GF.jpg)

Once you have the dev tools panel open, in the elements tab on the left, open up the header element and click on the h1 element. This will be the element selected in the chrome dev tool and you will see the h1 highlighted on the page: 

![00105.jpeg](image_rsrc3GG.jpg)

Once the h1 element is selected, you can increase the width of the styles tab on the right and scroll down until you see the box model for the h1: 

![00106.jpeg](image_rsrc3GH.jpg)

As you can see from the above screenshot, the h1 element’s box model can be seen clearly. We have a default margin applied to the top and bottom, and it has no border or padding.  Hopefully, this will give you a better understanding of how each element on the page is represented, and how they interact with each other based on their display type.

# Chapter 14. Step By Step Addition Of CSS To HTML Document

## The Three Ways To Add CSS To An HTML Document

You may recall from your HTML knowledge that there are three ways to add CSS to an HTML document: as inline style, as an internal style, and as a link to an external stylesheet. In this the book internal style method will be used because it more easily demonstrates, for learning purposes, how CSS relates to HTML in a single screen window and when using short economical code snippets. However, normally you will want to be using CSS script in external style sheets, since that is the generally preferred method. Also for visual clarity, many redundant elements will be omitted, such as <!DOCTYPE html>, <html> and <body>. Just assume that, if these examples were used on real web pages, you would have all the requisite elements in place.

For review, let’s just remind ourselves of the syntax and method for each manner of adding CSS to an HTML document.

## Inline Style

Inline CSS is presented within the opening HTML tag, where style is a Global Attribute that can be used by any HTML element. The value of any applied style attribute is a property:value pairing declared inside of quotation marks, attached to the attribute through the assignment operator equal sign, = . Every property:value pairing should end in a semi-colon, and similarly when combining more than one inline style, each property: a semicolon should separate value pairing.

Before Cascading Style Sheets, a vast amount of work was entailed by having to style every HTML element individually. Any change of a style decided later on meant that each element that had the style had to be manually adjusted. Here’s an example of inline CSS as part of an HTML text file:

<h1 style="color:red; font-style:italic; font-weight:100;">Red Heading Typography</h1>

![](image_rsrc3GJ.jpg)

Above three styles have been applied, making the font color red, its style italic, and the font weight 100 (on a 9-item scale 100 to 900– note that not all fonts support all nine available CSS weights).

## Internal Style

With internal CSS, the style is placed inside the <head> section of the HTML document, which is always above the <body> section, you will recall. This method is internal to the HTML document, i.e. a single web page, as a whole, rather than specific to a single element, which is why it is called internal. The CSS is applied within the <style> HTML opening and closing tags instead of a style attribute declaration and is declared in the standard CSS format. The basic CSS syntax is:

s ​{

​property : value;

​property: value;

​}

The “s” above  stands for “selector”, which is any HTML element (in this context, “s” is not the HTML tag for “strikethrough!”). With internal CSS, the property:value pairs are declared within curly braces, {    },  instead of quotation marks. The property:value pairs taken together with the curly braces make up a declaration in CSS. At a high level, the syntactical construct can be understood as:

Selector {Declaration}  {Declaration}  {Declaration}

Selector {Declaration}  {Declaration}  

And each declaration in turn is made up of:

{property:value; property:value; property:value;}

{property:value; property:value;}

etc.

A selector and its declaration(s) together make up a rule set:

rule set = selector {declaration(s)}

To ground this syntax in a typical example, let’s look at the use of multiple declarations applied to a single selector. Note that sometimes the order of declarations has no effect on the visual result, but in other cases the order does have an effect.

<style>

h2 {

text-align: center;

font-family: cursive;

color: orange;

}

</style>

<h2>

Hi, I've been styled.

</h2>

![](image_rsrc3GK.jpg)

Multiple declarations on the <h2> selector.

Instead of declaring styles one after the another on the same line as with inline CSS, with internal CSS each style declaration starts a new line and is completed with a semicolon. You must always complete a declaration with a semicolon even with the final one, since it’s possible that later on you or another designer may add new styles and not realize that there are missing semicolons above in the code that can cause a bug when rendering the style.

The code below is the internal CSS version of the same style we applied above in the inline example. The CSS is now located inside of curly braces, which are inside of the <style> tags which are inside of the <head> section. The CSS is applied in the head first (before the body) since a browser linearly parses the code. In this way, the browser does not first load an unstyled version of a page and then get to work restyling it all, which is what would happen if internal CSS was placed at the bottom of the .html file. Rather, the browser obtains the needed style information first in the <head>, then all subsequent HTML content is rendered in the style that was first parsed from the internal style declarations.

<head>

<style>

h1 {

color: red;

font-style: italic;

font-weight: 100;

}

</style>

</head>

<h1>Red Heading Typography</h1>

![](image_rsrc3GJ.jpg)

## External Stylesheet

Well-developed styles are made up of many lines of code, and for this reason it is usually impractical to create too many style statements as internal CSS within the <head> area of an .html document. Instead, CSS code is usually placed in its own text file(s) that have the file extension .css. This external style is then linked to in the <head> of an .html document via a <link> element. This link to the external .css file will instruct the browser to obtain the styling information from the external file first before continuing to load, and style, the subsequent HTML content. When using code editors to write CSS les, make sure you set the file’s syntax to CSS, though many editors will automatically detect the language you are writing in. When you save the file, make sure it has the .css file extension so that it is usable as a style sheet for a browser.

<html>

<head>

<link rel="stylesheet" href="css.css" type="text/css">

</head>

<body>

</body>

</html>

Above, we define the relationship (the rel attribute in <link>) between the .html document and the external resource as a stylesheet relationship. The URL to locate the external style sheet is a relative URL path– in this example, the CSS file is in the same directory as the index.html document. As your websites become more complex, you will eventually want to have your CSS source code files in their directories or folders, in which case the URL in the href might instead be “CSS/css.css” or “scripts/css.css” and so on. These forward slashes indicate that the .css file is to be found inside of a directory called “CSS” or “scripts,” and that these directories are in the same directory as the .html file. Finally, the Media Type of the stylesheet is declared with the type attribute. CSS, like all source code, is always just a text file, but instead of the usual .txt  file extension used for text files, .css is used so that the browser knows to parse the code as containing styling information.

![](image_rsrc3GM.jpg)

Placing the .css file in the same directory as the .html file, OR alternately, in a scripts directory. The value of the href attribute has to specify the path needed to find the external style document.

# Chapter 15. Introduction To JavaScript

HTML is used to develop web pages, and web pages can become complex documents that define the content of a page. Materials produced using HTML can get CSS added to it, and done in different ways like attaching a background color, changing font sizes, image size, typeface, shadow, colour intensity, and so on. HTML and CSS can be used to attain a static beauty of a web page. With JavaScript, you can inject life into web pages using JavaScript effects such as form validation, modal, slider, pop up, and so on. The practice of developing web pages or applications with HTML, CSS, and JavaScript is called Frontend development, and it enhances the user’s interaction with web pages. JavaScript is a well-built client-side scripting language. JavaScript is also generally used for mobile and game application development.

## A Brief History of JavaScript

·         1995: While working at Netscape, "LiveScript" was created by Brendan Eich and later renamed to "JavaScript."

·         1996: Javascript released by Microsoft, a port, for IE3.

·         1997: JavaScript became standardized in the "ECMAScript" spec.

·         2005: "AJAX" was coined, and the web 2.0 age began.

·         2006: jQuery 1.0 was released.

·         2010: node.JS was released.

·         2010: angular.JS was released.

·         2012: ECMAScript Harmony spec nearly finalised.

Several programmers tend to believe that JavaScript and Java belong to the same category, and this opinion is false because Java and JavaScript are different from each other. Java is a sophisticated programming language, while JavaScript is a scripting language only. The C programming language influences the JavaScript Syntax.

What does the future hold for JavaScript?

The technologies of HTML5 and JavaScript can be used to create extensions for Windows 8 desktop widgets, browsers, Chrome OS, and Firefox OS applications. A large number of non-web related applications also adopt the scripting language of JavaScript, and it can be used to create HTML templates (Mustache), attach activities to PDF documents, database interaction (MongoDB), and also control (Cylon.js). JavaScript has a bright future because web platforms continue to mature and advance its usage beyond only browsers. This scripting language will remain an integral part of future developments.

How to Run JavaScript?

JavaScript is a scripting language that cannot run on its own. The browser does the code running of JavaScript. When a user requests an HTML page that contains JavaScript, the browser receives the script, and then the browser gets to decide its execution. All modern browsers support JavaScript, which is a massive advantage for the scripting language. JavaScript also runs on operating systems like Linux, Mac, and Windows.

### Requirements to Learning JavaScript

●       Basic knowledge of HTML and CSS

●       A text editor

●       A browser

●       Logical thinking and tenacity

Programming

Computer programming is the act of implementing and creating a different set of rules to allow a computer to perform a specific task. It is the process of speaking the computer language, which involves picking an algorithm and encoding it into a notation so that the computer can get it executed.

Types of Programming Languages

1\. Low-level language

• Machine code

• Assembly language

2\. High-level language

Inscribed in different languages such as Java, PHP, C, C++, JavaScript, C#, Python, etc. Computer programs can be either interpreted or compiled language, although JavaScript is an excellent example of Interpretation.

Keeping Them Separate

HTML: It defines the page content.

CSS: It determines the content’s presentation.

JavaScript: It controls content characters.

When these technologies are used in developing a web page, they must be stored differently.

1\. Create a separate .html file for HTML

2\. Create a separate .css for CSS

3\. Create a separate .js for JavaScript

The Wrong Approach

<p>

Whatever you do, <a href="666.html" style="color: red;" onclick="alert('I said dont

click')">don't click this link</a>!

</p>

The Right Approach

<p>

Whatever you do, <a href="666.html" id="warning">don't click this link</a>! </p>

<style>

#warning{

color:red;

}

</style>

<script>

var warningLink=document.getElementById("warning");

warningLink.addEventListener('click',alerter, false);

function alerter(){

alert("I said don't click");

}

</script>

The best approach is to save the style and script into a separate .css file and .js file and unite them via link tag and script tag in the HTML document. This approach is utilized in this manual.

<link rel="stylesheet" href="warning.css" /> <p>

Whatever you do, <a href ="666.html" id="warning">don't click this link</a>!

</p>

<script src="warning.js"></script>

JavaScript Basics

Statements

The JavaScript syntax is also known as a C-style syntax which is related to the syntax used by PHP. A JavaScript program consists of JavaScript language construct, command, and keyword. This manual will teach you how to develop amazing things with the use of JavaScript language constructs, command and keyword. Every statement must end with a semicolon or a new line. By popular convention a JavaScript programmer should write one statement per line and with a semicolon at the end.

document.write('Hello World') document.write('Here comes the JS Engineer')

document.write('Hello World'); document.write('Here comes the JS Engineer');

document.write('Hello World');

document.write('Here comes the JS Engineer');

Comments

These are human-readable texts which the computer disregards. JavaScript consists of two types of comments:

//This is a single line comment

/*

This is a multiple line comment on line one

This is a multiple line comment on line two

This is a multiple line comment on line three

*/

Variable

To declare a variable, Use the “var” keyword.

A variable is used to store data and references the memory location in computer memory (RAM.) A variable can perform 3 actions, and they are:

1\. Declaring the variable

2\. Inserting data inside the variable

3\. Getting the data into the variable

It is important to name a variable to enable easy differentiation. Few rules guide naming variables.

Variable naming rules

●       They consist of the following character; numbers, letters, dollar signs or underscores but a number cannot be the first character

●       Variables are case sensitive, therefore ‘number-one’ differs from ‘NumberOne.’

●       Variables cannot be JavaScript reserved words

●       Variables select meaning and clarity

●       Variables do not hold space variable that creates more than a word, therefore ‘number one’ is written   as ‘numberone’ but for easy readability ‘numberone’ is often written as ‘number_one’ or ‘numberOne.’

●       Select a naming convention and become accustomed to it.

var 2numberOne; //invalid variable name because it started with number

var numberOne!; //invalid variable name because it contains a non-permitted character!

var x; //valid variable name but not descriptive

var numberOne; //variable declaration

var numberTwo; //variable declaration

numberOne=5; //assigning data to variable

numberTwo=10; //assigning data to variable

document.write(numberOne); //calling data inside a variable

document.write(numberTwo); //calling data inside a variable

var numberOne=3; //variable declaration and assignment

var numberOne, numberTwo, numberTwo; //multiple variable declaration

var numberOne=2, numberTwo=4, numberTwo=6; //multiple variable declaration and assignment

# Chapter 16. JavaScript Syntax

We finally start to see JavaScript source code! So far everything we have seen in this manual may have seemed very theoretical, but from now on we hope you find it more enjoyable to start seeing more practical and directly related to programming.

The JavaScript language has a syntax very similar to Java because it is based on it. It is also very similar to that of the C language, so if the reader knows any of these two languages  ​​it will be easy to handle with the code

## Comments in The Code

A comment is a part of code that is not interpreted by the browser and whose utility lies in making it easier for the programmer to read. The programmer, as he develops the script, leaves individual phrases or words, called comments, which help him or anyone else to read the script more easily when modifying or debugging it.

Some JavaScript comments have been seen previously, but now we are going to count them again. The language has two types of comments. One of them, the double bar, is used to comment on a line of code. The other comment can be used to comment on several lines and is indicated with the signs / * to start the comment and * / to end it. Let's see some examples.

<SCRIPT>

// This is a one-line comment

/ * This comment can be extended

along several lines.

The ones you want * /

</SCRIPT>

## Upper Case and Lower Case

In JavaScript uppercase and lowercase letters must be respected. If we make a mistake when using them, the browser will respond with an error message, either syntax or indefinite reference.

For example, the alert () function is not the same as the Alert () function. The first displays text in a dialog box, and the second (with the first capital A) simply does not exist, unless we define it ourselves. As you can see, for the function to recognize JavaScript, you have to write all lowercase. We will see another clear example when we deal with variables, since the names we give to the variables are also case sensitive.

As a general rule, the names of things in JavaScript are always written in lowercase, unless a name with more than one word is used, since in this case the initials of the words following the first will be capitalized. For example, document.bgColor (which is a place where the background color of the web page is saved), it is written with the capital "C", as it is the first letter of the second word. You can also use capital letters in the initials of the first words in some cases, such as the names of the classes.

## Separation of Instructions

The different instructions that our scripts contain must be conveniently separated so that the browser does not indicate the corresponding syntax errors. JavaScript has two ways of separating instructions. The first is through the semicolon (;) character and the second is through a line break.

For this reason, JavaScript statements do not need to end with a semicolon unless we put two instructions on the same line.

It is not a bad idea, anyway, to get used to using the semicolon after each instruction because other languages  ​​such as Java or C force them to be used and we will be getting used to making a syntax more similar to the usual one in advanced programming environments.

## Variables in JavaScript

This is the first of the articles that we are going to dedicate to variables in JavaScript within the JavaScript Manual. We will see, if we do not already know, that variables are one of the fundamental elements when making programs, in JavaScript as well as in most of the existing programming languages.

So let's start by getting to know the concept of a variable and we'll learn how to declare them in JavaScript, along with detailed explanations of their use in the language.

## Variable Concept

A variable is a space in memory where data is stored, an area where we can store any type of information that we need to carry out the actions of our programs. We can think of it as a box, where we store data. That box has a name, so that later we can refer to the variable, retrieve the data as well as assign a value to the variable whenever we want.

For example, if our program performs sums, it will be very normal for us to store in variables the different addends that participate in the operation and the result of the sum. The effect would be something like this.

adding1 = 23

adding2 = 33

sum = adding1 + adding2

In this example we have three variables, adding1, adding2 and sum, where we save the result. We see that their use for us is as if we had a section where to save a data and that they can be accessed just by putting their name.

## Rules for Variable Naming in JavaScript

Variable names must be constructed with alphanumeric characters (numbers and letters), the underscore or underscore (_), and the dollar character $. Apart from this, there are a number of additional rules for constructing names for variables. The most important is that they cannot start with a numeric character. We cannot use rare styles such as the + sign, a space, or a - sign. Supported names for variables could be:

Age

country of birth

_Name

$ element

Other $ _Names

We must also avoid using reserved names as variables, for example we will not be able to call our variable words like return or for, which we will see that they are used for structures of the language itself. Let's now look at some variable names that you are not allowed to use:

12 months

your name

return

for

more or less

pe% pe

## Variable Names in JavaScript Are Case Sensitive

Remember that JavaScript is a case-sensitive language, so variables are also affected by that distinction. Therefore, the variable named "myname" is not the same as the variable "myName". "Age" is not the same as "age".

Keep this detail in mind, as it is a common source of code problems that are sometimes difficult to detect. This is because sometimes you think you are using a variable, which should have a specific data, but if you make a mistake when writing it and put upper or lower case where it should not, then it will be another different variable, which will not have the expected data. Since JavaScript does not force you to declare variables, the program will run without producing an error, however, the execution will not provide the desired effects.

## Declaration of Variables in JavaScript

Declaring variables consists of defining, and incidentally informing the system, that you are going to use a variable. It is a common custom in programming languages  ​​to explicitly specify the variables to be used in programs. In many programming languages  ​​there are some strict rules when it comes to declaring variables, but the truth is that JavaScript is quite permissive.

JavaScript skips many rules for being a somewhat free language when programming and one of the cases in which it gives a little freedom is when declaring the variables, since we are not obliged to do so, contrary to what happens in other programming languages  ​​like Java, C, C # and many others.

## Variable Declaration with Var

JavaScript has the word "var" that we will use when we want to declare one or more variables. Not surprisingly, that word is used to define the variable before using it.

Note: Although JavaScript does not force us to declare variables explicitly, it is advisable to declare them before using them and we will see from now on that it is also a good habit. In addition, in successive articles we will see that in some special cases, a script in which we have declared a variable and another in which we have not, will not produce exactly the same results, since the declaration does not affect the scope of the variables.

var operand1

var operand2

You can also assign a value to the variable when it is being declared

var operand1 = 23

var operand2 = 33

It is also allowed to declare several variables on the same line, provided they are separated by commas.

var operand1, operand2

## Declaration of JavaScript Variables with Let and Const

From Javascript in modern versions (remember that JavaScript is a standard and that as it evolves over time), specifically in Javascript in its ES6 version, there are other ways to declare variables:

Let declaration: This new way of declaring variables affects their scope, since they are local to the block where they are being declared.

Const Declaration: Actually "const" does not declare a variable but a constant, which cannot change its value during the execution of a program.

Perhaps at this point in the Javascript manual it is not necessary to delve too deeply into these declaration models and for those who are learning we recommend focusing on the use of declarations with "var". However, if you want to have more information about these new types of variables, we explain them in the article Let and const: variables in ECMAScript 2015\. If you want to see other news about the Javascript standard that came in 2015, we recommend reading the ES6 Manual.

# Chapter 17. Definition of Arrays in JavaScript

Another thing we need to take a look at when we work in this language is what an array is all about. To keep it simple, an array is just going to be a structure of data that can contain our group of elements. In most coding languages including JavaScript, we will find that the items inside an array are usually the same type of data, such as a string or an integer. Collections are going to be used in order to help a computer program, or your coding language, organize and sort your data so that a set of values that are related can be sorted through or searched through well. 

No matter what kind of coding language you decide to work with, you will find that keeping the data and the objects organized will be necessary. If you don’t take care of these objects and types of data, they are going to float around the work you are doing, and you will run into some troubles in the code. The part of the system you are in will not be able to find the objects and classes they need and your order won’t work. 

But when you are working with many of the modern types of coding languages out there, including JavaScript and a few others, you are going to rely on a bit more organization than what we are going to find in some of the older languages. You need to make sure things are organized, and the set of values that are related are going to be easy to search through and sort through as much as you would like. 

While the program is able to create a new variable, if it wanted, for all of the results that are found in it, this can really take up a lot of time and space in some of the codings you are doing, and it is definitely not going to be the most efficient method you can use here. Instead, you will find that storing all of the results (while we are still on the search engine example) in an array will be a more efficient method to use to pull up the results you want, while also managing your memory. 

Now, there are going to be a few different parameters and properties that can come with the array you would like to create. Being able to make this come together and work the way you want is essential, and understanding what each of these properties is all about will be a great way to get a better understanding of what you can do with them. Some of the features that come along with your array object, along with information on what all of these means, includes:

1.  Constructor: This will help us get back a reference to our array function, the one that was able to create the object. 
2.  Index: This will be the property in our array that will represent the zero-based index that will match up to that part inside of our string. 
3.  Input: This will be a property we are only going to see in specific arrays. When a range has been created by a regular expression and it all matches, then we are going to have this input. 
4.  Length: This will show us the number of elements we are going to be able to see in our array. 
5.  Prototype: We will discuss this one more in this guidebook, but this particular property will allow us a way to add methods and features to our object. 

This may not make a lot of sense right now, but we are going to expand upon it a bit and see more about what we will be able to do with these arrays and the different parts that come with it. Before we move into this though, we need to take some time to talk about some of the array methods that are important to our code. There are a lot of different ways that happen with our object of an array, so let’s take a look at what all of these mean. 

1.  Concat: This one will return to us a new array that will be comprised of not only this array but with the other values or ranges that we need. 
2.  Every(): This one will return true if we find that each and every element that falls in our array will satisfy the testing function that we provided. 
3.  Filter(): This one is responsible for creating a new array with all of the elements that fall into the current range for which the provided filtering function will give us honestly as the result. 
4.  forEach(): This one is responsible for calling up a function for each of the elements that are inside of our array. 
5.  indexOf(): This one will return the first (or the least) index that comes with the element that is inside of our array, as long as it is equal to the value that we specify. Or it will work with -1 if nothing is found to match in it. 
6.  Join(): This one will join together all of the elements of an array and can help turn these into a string. 
7.  lastIndexOf(): This one will return the previous, or the greatest, index of your element in the array as long as that element is equal to the value that we are trying to specify, or we will work with -1 if we can’t find a match in the array. 
8.  Map(): This one is responsible for helping us to create a brand new array with the results of calling up a provided function of all the elements that fall into this array. 
9.  Pop(): This one will help us remove the last element out of our array and then will return the item that we want. 
10.  Push(): This one is nice because it is able to add in at least one, but sometimes more, elements to the end of your array and then will return to you the new length that this makes your array. 
11.  Reduce: This will apply the function that you want at the same time against two values of the array, going from the left side over to the right side, in order to reduce it by one amount. 
12.  reduceRight(): This will be the same idea, but instead of going from the left side to the right side, we are going to reverse this and go from the right side to the left side. 
13.  Reverse: This will be responsible for reversing the order that your array elements are going to be in. The first element in the array will become the last element, and then the part that was the last one will go to the beginning of the collection. 
14.  Shift(): This one will remove the first element out of your array and then will give you a return of that element. 
15.  Slice: This one will extract a section of your array and will give you a return that has a brand new collection in it. 
16.  Some(): This one will return true as long as you have one or more elements in the array that is able to satisfy the testing function that you provided.
17.  toSource(): This one will help us to represent the source code that comes with our object.  
18.  Sort(): This one can be useful because it will help us to sort through all of the elements that come with our array. 
19.  Splice: This one will be there to help us to either add or remove the elements of the array. 
20.  toString(): This one will return a string that will represent the array and all of the elements that happen in it. 
21.  Unshift: This final one will take some time to add in one or more elements to the beginning of our array and then will let us know what the new length of this array will be when it is done. 

As we can see here, there are a lot of possibilities that we can work with when it comes to handling the arrays that show up in our codes. These arrays are going to help us to hold onto some of the data that we have more efficiently and will ensure that we can put it all together and pull out the elements that we need and want without a lot of struggle along the way. Make sure to take a look at some of the methods and functions available with these arrays, especially with JavaScript, so you know how to use them for some of your own needs as well. 

# Chapter 18. What to Do Next?

Hopefully by now, you have a somewhat solid understanding of how HTML and CSS work together. It's important to understand that we've only scratched the surface of HTML and CSS.

What's important to take away from this book is not to memorize all the different elements in HTML and properties in CSS. It's to be able to understand the two and how they work hand-in-hand.

There's no need to learn every single element and property. It will do more harm than good and chances are, you're not going to absorb all that information. That's precisely why I didn't want this book to be a 500-page manual of all the HTML elements and CSS properties. When you learn English, you don't just open up a dictionary and start reading. Coding is no different.

The critical skill that hopefully you have by now is to be able to look at new HTML elements and CSS properties and deduce and understand their functionalities from the code.

## Debugging

By far the most powerful tool in all of HTML and CSS is the ability to identify and fix errors. If you master this skill, it doesn't really matter how much you know and it doesn't matter if your initial code is filled with mistakes because it's the ability to spot and fix errors that brings you to your end result. It's also going through this process that allows you to absorb and understand concepts truly.

When it comes to debugging, your best friend is a browser developer tool. All of the main browsers have developer tools for you to look at the HTML and CSS of any given page you load. Safari has web inspector, Firefox has firebug, and Chrome has inspected element. We're going to showcase Chrome's inspect element.

So you're coding away and you open up your web page in your browser and something's not right. It looks off but you have no idea where you've made an error. Open up inspect element (right click -> click on inspect element).

Inspect element will show you exactly why the code is displayed in the way it is. As the mouse hover over the elements in the HTML on the left side, it will highlight the corresponding area in your window. Clicking on an HTML element, will show the CSS rule that corresponds to it on the right hand side. If you drag down the 'compound style' tab, it shows exactly the property values that are given and where they're coming from. A lot of the times, CSS rules are passed down from parent elements, and with this, you can see which parent rule is resulting in the given value.

Apart from the occasional careless mistake that takes a second to fix once you have realized it, the more trivial errors are always related to the CSS properties display and position. Things like font-size, colors, borders, etc. are all one-step fixes. Display and position can get way more complicated. It's by far the hardest concept to grasp for HTML and CSS. If you know display and position inside out, you're a HTML/CSS master.

The reason display and positioning can get complicated is because of the number of variables in play. Your output is not only indicative of the value of one property, but a combination of many. The display, position, and float properties of sister elements all work hand-in-hand. Not only that, but they also correlate to the properties of the parent element. Debugging this is not as simple as looking at one element. You must look at the bigger picture.

Here's how you should debug display and positioning errors.

Isolate your error. Figure out which element is resulting in the wrong display or position. Look at your declarations of not only this element, but also the sister and parent elements. When you debug display and position, it's important to realize that you have to look beyond just the specific element.

If you have an idea why the error is present, try and fix it in your browser. Remember, you can change and update values in your inspect element and the changes will be reflected live. If you're right and the changes correct the error, go to your code and make the same changes.

If you're completely clueless and have no clue why your position or display is wrong, do some research. Turn to Google and search for your problem. Simple searches like 'absolute position center issue' or 'can't see fixed position element' will render plenty of results. Literally every question that you can think of related to HTML and CSS has been asked and answered online. Tutorials and forums are great places to find answers. Use them hand-in-hand.

As for forums, the place for everything and anything coding related is stackoverflow.com. Chances are your answers will be there, but if not, there are plenty of more resources out there.

## Learning More

You're in a position now where you understand the language of HTML and CSS. What separates you from someone who's a master of HTML and CSS is simply experience. The way to learn and be good at coding is to code. Reading books or online manuals on all the specific rules is pointless. What you should do is set out to create a product. Even if you're not completely sure how to complete it, just get the ball rolling. Your generic questions will turn into specific questions, which you'll be able to find the answers to.

One last thing to keep in mind:

You can look for any code on any website, that’s the beauty of the HTML and CSS language. Your browser is the most powerful tool for learning. When you come across a website that has a spectacular design or something you want to implement, you can look at how it's done right in your browser. Take advantage of the power of your browser.

You can also use this for debugging. If you're drawing a blank for a display and position error, resort to reputable websites and see how they do it. The top technology websites spend a lot of money to hire the best of the best to code their website. Take advantage of this. Go to their websites and see how they style things. If there's something that Google or Facebook or Amazon or Twitter does that intrigues you, you can't go wrong learning from how they do it. There are no more hidden secrets and techniques when it comes to HTML & CSS. Everything is out there.

# Chapter 19. Art of Computer Programming

Becoming the best programmers depends on many factors besides learning programming techniques in classes or over the internet. In simple terms, it is not about programming as most beginners think. From my experience, your level of impacts plays a lot in determining the level of your success or how best you are as a programmer. Truly, people will not measure your experience from how happy you look when doing programing projects but how your programming projects are impacting the lives of many people in society. For example, there are some people who always feel happy after spending the whole day without doing any programming tasks while others feel unhappy if they do not handle any projects. Also, drinking alcohol everyday can make a person feel happy. Therefore, you level of experience and knowledge does not on how happy you are but how you use the learned skills. 

Several studies have proved that slacking off in computer programming not only makes person’s programming logic weaker but also destroys his/her tempo. Normally, we miss many things when we don’t attend the classes just like drinking coke every day ruins both our teeth and internal organs. Just like alcohol has impacts in our bodies, your success in programming is measured through its impacts. We will see you as a weaker programmer if you do not use the learned programming skills to create positive impact to you or to the society. 

## Levels of Impacts Resulting from Programming

Ideally, there are different levels of impacts we can use to determine how perfect you are with programming. Yes, most programmers do not know that their programming knowledge is judged on how it impacts them or the society. The following are levels of the impacts: 

First Level of Impact: You/ a person

One of the step to determine how you can measure the impact is by looking at the effects of programming has made on an individual. It is not only the simplest way but also very important since all programmers have goals in their mind before starting programming. Usually, you engage in various activities or jobs because you want a result not nothing. For example, we take our children to schools with two reasons; (1) get job in their future lives to live better life, and (2) obtain knowledge that will help them associate with other people in the society. It is important to know that doing something without a purpose makes you to experience an unexpected result on your way. Therefore, the impacts of programming on you show how best and successful you are as a programmer. 

## Relationships in Life

Do you know that programming can cause certain impacts on your relationship? In order to determine the effects of programming on your relationship, we always look at how close you are to your love, friends, and other people in the society. Some people chose to be software programmers because it is their passion while others chose it because of peer pressure or their parents forced them. 

Another main reason why people chose programming is getting jobs. In most cases, we work in projects, deliver them, and earn income once users use them. As programmers, we are only required to maintain the projects if there are crashes or bugs. This gives us more time for our relationships. Truly, human life is all about relationship but not how much we earn per day. You may be earning five or six digits but you are not happy at all because you lack freedom to associate with people, particularly your love ones and relatives. Let me tell you, people get more fulfillments out of life when there are some people whom they love and care for. You should spend your earnings with the people you love. As such, work is supposed to improve your relationship with love and relatives.

## Impacts On Your Health and Life

In this modern life, your mind and body are the two main assets you must value most. Both body and mind are irreplaceable in our life. Therefore, you must take care of our mind and bodies to avoid them deteriorating over the time. Surely, every person wants to have a longer life, and as such, it is important to consider health when measuring how best you are as a programmer. You career as a programmer would not be either good if you are not healthy. 

Money is worthless when compared to our mind and health. I tell you, money will always come on your way when you develop a good mind, which include practicing daily to solve problems, looking for answers, and thinking deep and creatively. You should not only get enough sleep but also build a habit that will train your mind just like writing and reading books. Make coding to be a favorite way to train you. The best programmers always spend at least thirty to forty minutes per day on programming. This is very important to their health. We can say health is your life and you should take care of it in order to live longer. 

## Having Full Enjoyment

We have seen previously that happy is not the measurement of the success of a person; it is only a part of it, though we need it. You can increase your productivity in programming by engaging in things that you enjoy. What do I mean? I mean that a person can be more productivity in his/her programming work if he/she gives himself/herself a chance to enjoy life. Being more productivity in programming has more impact too. In addition, you should know that there is a great difference between passion and hobbies. While hobby refers to doing something you enjoy, passion refers to thing you like doing throughout the life. For example, my passion is coding and my hobby is learning Japanese language. I always study Japanese when I am a little bit frustrated with some complex coding. This gives enough time to refresh my mind before diving back into the world of coding. 

Giving yourself enough time to relax or take a break to make your brain work on the problem subconsciously is always the right thing to do. But what do you do if you find it hard to solve the problem even after relaxing? It is easy. Just give your brain enough time to solve the problem in the background. In fact, this is one of the main reasons why most ideas come in our minds when we are eating, showering, or drinking tea.

## The Second Level of Impact

Now let us discuss how we can measure you programming level using the second level of impact.

## Impact On Others

Before you consider yourself as the best programmers, it is important to ask yourself about the impact you cause to other people when you are coding. Okay, you may be like that you know how to code because it is the most useful tool available for impacting the lives of many people positively. You can impact people by either enabling them to get data easily, improve their websites, or increase sales. One of the goals in programming is helping other people achieve their objectives. You will be recognized as the best programmers when you help others and organizations to succeed and at the same time meeting your goals. I know it is sometimes difficult for most programmers, but you can become the best programmers if you do this. 

## Giving Purpose to Other People

Every person has their own purpose (known or unknown) in life, and this is seen when an individual dedicates his/her life to doing certain thing. For programmers, their purpose is revealed when they engage in building projects and software. Now, let us ask ourselves where this sense of purpose comes from. In normal cases, our purpose comes from the surrounding, society, friends, and internet. For example, we develop an interest in programming after we encounter those who do programming and have achieved a lot in their lives. To be precise, they are the main people who can inspire you to engage in programming. But what will you do in case those people fail to give us ideas? There is a higher chance that you will not have a right purpose. We all have different purpose in our lives and that is the main reason why we all do different work. We were not born to do the same job. While some people are born to be developers, others are born to be doctors, teachers, or politicians. 

According to Mark Zuckerberg during his Harvard Commencement Speech, people must have a generational challenge for our society to continue moving forward. We should not only create new jobs for the youth or our people but promote a sense of purpose. However, it is not easy to have a purpose for yourself. You should also create a sense of purpose to other people in the society. Let us take the following example. You need to hire workers if you build a company. These workers play a significant role to the growth of your company. It is, however, your responsibility, as an employer, not only to give them a sense of purpose but also help them to grow in society.

# Conclusion

Creating a web page is something that has been wreathed in mysticism and cyber mumbo jumbo for years, but I hope that I’ve shown you that it’s not as scary as you might think. In fact, HTML is actually fairly straight forward. If you’re looking for a hobby that can really accomplish something and is easy to explain, then you’ve come to the right place. These are the foundations for you to build your web page and push on to greater things like CSS, Java, JavaScript, C++, and the list goes on and on. Remember, that you can never really get in over your head if you master and truly understand what it is that you’re working on in the moment.

If something doesn’t make sense to you or is confusing, my best suggestion to you is to open up your TextEdit or Notepad and start working on it. Pull it up in your browser and have a look at what it does for your page. Taking everything step by step will inevitably lead you to the path of success. There is never a reason to jump ahead without fully understanding what it is that you’ve done.

All of these programming languages are quite vast in their own right. However, since they are also simple and easy, you should not have too much of a problem mastering them. With hard work and a bit of time, you will be able to create full-fledged websites in no time at all.  The concepts will help you understand and apply the different scope of variables, invent types, loops and arrays, form structure, positioning, and so on.

Of course, this book should have given you enough to have a good base for all three languages. You should have already seen the hello world examples and noted how easy they are. As such, you should have no problems with the basic syntax for each language. 

You will have come across the basic functions, statements, and tags that are commonly used in these languages. More importantly, you should no longer have any problem using them in a web page of your creation. 

In HTML, you came to know how a simple web page can be written and filled with content. Then, with CSS, you will have been able to stylize that web page and make it look attractive. Finally, JavaScript allowed you to make your web page more interactive. As such, your web page should now be looking and feeling a lot like the web pages you have previously admired. 

As we get to the end, you have learned quite a lot about web development, and you learned the creation of functional and well-structured HTML documents as well as styling, color usage, layouts, and typography using tags. Practice what you have learned because practice is the best way to learn.

With everything that I have presented to you, you should be able to get the grasp on the beginnings of a web page and if you can get the beginning, it’s just a matter of taking the next step piece by piece. So good luck and get out there and make an amazing web page.

I hope you have learned something!

# Index

C

coding             8, 146, 147, 150, 151

codings             7

Colors             38, 40, 110

CSS              1, 57, 123, 124, 128, 129, 130, 131, 132, 143, 144, 145, 146, 147, 148

D

design             7, 133, 142, 145, 148

E

elements              9, 10, 11, 13, 18, 19, 37, 40, 58, 68, 72, 109, 112, 115, 117, 122, 123, 124, 125, 126, 128, 138, 143, 146, 147

H

HTML              1, 7, 9, 16, 28, 30, 31, 33, 123, 128, 129, 130, 131, 146, 147, 148

I

image              31, 45, 46, 47, 48, 95, 96, 98, 99, 100, 101, 103, 104, 105, 114, 125

J

JavaScript              30, 32, 33, 133, 137, 143, 144, 145

L

language              7, 58, 68, 131, 133, 137, 138, 139, 140, 144, 145, 147, 151, 153

link              11, 12, 30, 31, 32, 38, 39, 76, 77, 78, 79, 104, 128, 131, 132

P

Properties             109

S

semantics             9

Style              16, 18, 19, 20, 24, 25, 109, 115, 128, 129

Styles             2, 3, 4, 16, 58, 70

T

text              9, 11, 16, 17, 18, 19, 20, 24, 25, 26, 27, 31, 33, 34, 35, 37, 40, 43, 46, 48, 78, 79, 80, 85, 86, 88, 89, 92, 101, 102, 109, 112, 114, 124, 125, 128, 130, 131, 132, 137

Text             2, 7, 16, 48, 63, 64, 69

W

web             9

wеb             7

wеbѕіtе             7