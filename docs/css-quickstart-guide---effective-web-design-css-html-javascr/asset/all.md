![](cover.jpeg)

## Table of Contents

*   [© Copyright 2016 - All rights reserved.](#part0002.html_9-020de52a65f8414d94e9614e31c22477)
*   [ContentsIntroduction](#part0003.html_S-020de52a65f8414d94e9614e31c22477)
*   [Introduction](#part0004.html_23-020de52a65f8414d94e9614e31c22477)
*   [Chapter 1: The Advantages of Using CSS](#part0005.html_2J-020de52a65f8414d94e9614e31c22477)
*   [Chapter 2: CSS Modules](#part0006.html_3J-020de52a65f8414d94e9614e31c22477)
*   [Chapter 3: Inclusion](#part0007.html_AT-020de52a65f8414d94e9614e31c22477)
*   [Chapter 4: Measurement Units](#part0008.html_HU-020de52a65f8414d94e9614e31c22477)
*   [Chapter 5: Colors](#part0009.html_IE-020de52a65f8414d94e9614e31c22477)
*   [Chapter 6: Background](#part0010.html_K0-020de52a65f8414d94e9614e31c22477)
*   [Chapter 7: Fonts](#part0011.html_VV-020de52a65f8414d94e9614e31c22477)
*   [Chapter 8: Text](#part0012.html_17T-020de52a65f8414d94e9614e31c22477)
*   [Chapter 9: Using Images](#part0013.html_1JK-020de52a65f8414d94e9614e31c22477)
*   [Chapter 10: Links](#part0014.html_1NB-020de52a65f8414d94e9614e31c22477)
*   [Chapter 11: Tables](#part0015.html_1SF-020de52a65f8414d94e9614e31c22477)
*   [Chapter 12: Borders](#part0016.html_2AT-020de52a65f8414d94e9614e31c22477)
*   [Chapter 13: Margins](#part0017.html_2M9-020de52a65f8414d94e9614e31c22477)
*   [Conclusion](#part0018.html_2TL-020de52a65f8414d94e9614e31c22477)

CSS:

Quick Start Guide - Effective Web Design

© Copyright 2016 - All rights reserved.

In no way is it legal to reproduce, duplicate, or transmit any part of this document in either electronic means or in printed format. Recording of this publication is strictly prohibited and any storage of this document is not allowed unless with written permission from the publisher. All rights reserved.

The information provided herein is stated to be truthful and consistent, in that any liability, in terms of inattention or otherwise, by any usage or abuse of any policies, processes, or directions contained within is the solitary and utter responsibility of the recipient reader. Under no circumstances will any legal responsibility or blame be held against the publisher for any reparation, damages, or monetary loss due to the information herein, either directly or indirectly.

Respective authors own all copyrights not held by the publisher.

Legal Notice:

This book is copyright protected. This is only for personal use. You cannot amend, distribute, sell, use, quote or paraphrase any part or the content within this book without the consent of the author or copyright owner. Legal action will be pursued if this is breached.

Disclaimer Notice:

Please note the information contained within this document is for educational and entertainment purposes only. Every attempt has been made to provide accurate, up to date and reliable complete information. No warranties of any kind are expressed or implied. Readers acknowledge that the author is not engaging in the rendering of legal, financial, medical or professional advice.

By reading this document, the reader agrees that under no circumstances are we responsible for any losses, direct or indirect, which are incurred as a result of the use of information contained within this document, including, but not limited to, —errors, omissions, or inaccuracies.

Contents

Introduction

Chapter 1: The Advantages of Using CSS

Chapter 2: CSS Modules

Chapter 3: Inclusion

Chapter 4: Measurement Units

Chapter 5: Colors

Chapter 6: Background

Chapter 7: Fonts

Chapter 8: Text

Chapter 9: Using Images

Chapter 10: Links

Chapter 11: Tables

Chapter 12: Borders

Chapter 13: Margins

Conclusion

# Introduction

CSS, the shortened version of Cascading Style Sheets, is one of the simplest of all the design languages, the one you need to use for the most effective web design. CSS will handle how your webpages look and how they feel; you can set the text color, the font style, how much space there is between each paragraph, how the web page columns are laid out and sized, the colors and images needed for the background and all the other layout and design variations that you need to make your website work on all different screen sizes and devices.

CSS is incredibly easy to understand and learn and it gives you powerful control over how your HTML document are presented. It is commonly combines with two of the more popular markup languages, HTML or XHTML, to provide you with all the tools you need to produce a well-designed website.

For the purpose of this book, I am going to take you through all of the main aspects of web design that you can control CSS, together with sample code. I hope that, by the end of it, you have some idea of how easy CSS is to use and the amazing results you can produce.

# Chapter 1: The Advantages of Using CSS

CSS has a lot of advantages over and above any other similar program, including:

Time-Savings - with CSS, you can write it once and then use the exact same sheet in a number of different HTML pages. Each HTML element can have its own separate style that can be applied to multiple web pages.

Faster Page Load Times – when you use CSS, there is no need to write the HTML tag attribute every single time. Instead, you can write just one rule for a tag and then apply it to every occurrence of the tag. Less code equals much faster loading times

Easy to Maintain -  when you want to make a global change, all you need to do is change the style; each element relating to that style in all the web pages it was used in will be changed

Superior to HTML in Style – CSS provides access to a much bigger range of attributes than HTML does so your HTML page will look better than if you used HTML attributes.

Compatibility with Multiple Devices – Your style sheets allow for content to be optimized for more multiple types of device. Using the same HTML document, you can produce different website versions for printing, for PDAs or for mobile devices, for example.

Global Web Standards – More and more, CS I being recommended over HTML so now is a good time to start learning it and using it in all your HTML pages. That way, they will be compatible with the browsers of the future.

Offline Browsing   CSS is able to store applications locally using offline cache. This mean that you will find it easier to view offline websites and, because of the cache, they will load faster and the website will perform better.

As you can see, CSS offers a ton of advantages over using HTML, not least the fact that it is now the recognized standard. With CSS becoming more and more poplar, now is the best time to start your learning process.

Without any further ado, let us delve into the CSS elements that you use for web design.

Before I go any further, I must state that some of the example code used in the book is attributed to www.tutorialspoint.com.

# Chapter 2: CSS Modules

CSS modules take on the existing CSS specifications along with a number of extension features, including:

*   Selectors
*   Box Model
*   Image Values
*   Backgrounds and borders
*   Replaced content
*   Text effect
*   D and 3D transformations
*   Animations
*   Multiple column layout
*   Use Interface

CSS is made up of a number of style rules that are interpreted by the browser before being applied to the right element of the document. Style rules are split into three:

Selector - this is the HTML tag that the style is applied to. Examples of these tags are, <h1> or <table>.

*   Property – Properties are types of HTML ta attributes. In simple terms, all HTML attributes are changed to CSS properties, for example, color border, etc.
*   Value – Each property is assigned a value or value. For example, the color property may have a value of red or perhaps #F2F2F2, etc.

The syntax for a CSS style rule is:

selector { property: value }

For eample, you could define a border on a table as:

table{ border :1px solid #C00; }

In this example, the table is a selector and border is a property. It has been given a value of 1px solid #C00

Selectors can be defined in a number of ways so let’s look at each different one:

Type Selectors

You saw an example of the Type selector above but let’s have a look at another - a way of adding a color to all of the level 1 headings:

h1 {

color: #36CFFF;

}

Universal Selectors

Instead of selecting the elements that relate to a specific type, this selector just matches the names of the element types. For example:

{

color: #000000;

}

In this example, the content of all the elements has been turned to black

Descendant Selectors

Let’s say you want to give a particular element a style but only when it is inside a specific element. In the following example, we are applying the style rule to the <em> element but only when it is outside of the <ul> tag:

ul em {

color: #000000;

}

Class Selectors

Class selectors allow you to use the class attribute of the elements to define your style rules. All of the elements of that particular class are formatted as per the defined rule:

.black {

color: #000000;

}

In this example, the rule has turned the content of all the elements with the class attribute of black to the color black. You could go one step further if you like:

h1.black {

color: #000000;

}

Now you have specified that only the content inside the <h1> element with a class attribute of black will be turned to black.

You are not limited to just one class selector for an element though. Look at this example:

<p class="center bold">

The style of this paragraph is defined by the classes Bold and Center

</p>

ID Selectors

Style rules can be defined on the id attribute of an element and, when a rule is defined, it will format all elements with the specified id attribute:

#black {

color: #000000;

}

This rule will turn the content of all elements that has the id attribute to black. You can be a bit more specific if you like, for example:

h1#black {

color: #000000;

}

This rule turns the content for <h1> elements to black ONLY if the id attribute is set to black.

The real power of an id selector become known when they are used as foundations for the descendant selector, for example:

#black h2 {

color: #000000;

}

Here, you can see that all of the level 2 headings will be turned to black only when they lie inside a tag that has the id attribute set as black

Child Selectors

The child selector is similar to the descendant selector but with different functionality. Look at this example:

body > p {

color: #000000;

}

This will turn the paragraphs to black only if they are the direct child of the <body> element. Other paragraphs that are inside other elements, like <td> or <div> would not change.

Attribute Selectors

Styles can also be applied to HTML element that have specific attributes. Look at the example below; you can see that the style rule is going to match all the input elements that have a type attribute with a text value:

input [type = "text"]{

color: #000000;

}

The advantage to using this method is that <input type = “submit” /> is not affected and the color change only applied to certain text fields.

The following rules are for the attribute selector:

*   p[lang] -  this selects all of the paragraph elements that have a lang attribute
*   p[lang]= “fr”] – this selects all the paragraph elements with lang attributes that have an exact value of “fr”
*   p[lang~="fr"] – this selects all the paragraph elements that have a lang attribute containing “fr”
*   p[lang|="en"] – this selects all the paragraph elements with a lang attribute containing exact values of “en” or that start with “en-“.

Multiple Style Rules

Multiple style rules can be defined for one single element and these should be defined to combine a number of properties and their corresponding value into one block, as in this example:

h1 {

                color: #36C;

                 font-weight: normal;

                letter-spacing: .4em;

                margin-bottom: 1em;

                text-transform: lowercase;

}

In this example, you can see that the pairs of properties and their value are each separated by a semi-colon (;). They can stay in one single line or you can spread them over multiple lines but, to read them better, we have kept them on single lines.

Grouping Selectors

Styles can be applied to multiple selectors. You just have to remember to separate each with a comma, as shown in this example:

h1, h2, h3 {

                color: #36C;

                font-weight: normal;

                letter-spacing: .4em;

                margin-bottom: 1em;

                text-transform: lowercase;

}

This style rule will apply to all of the h1, h2 and h3 elements as well. The order in the list is not relevant because all of the elements in the selector are going to have the declarations applied to them. As you can see from the example below, various class selectors can be combined:

#content, #footer, #supplement {

   position: absolute;

   left: 510px;

                width: 200px;

         }

# Chapter 3: Inclusion

You have four ways of associating styles with HTML documents, the most common of which is the inline CSS and the External CSS methods.

Embedded CSS

CSS rules can be put into an HTML document with the use of the <style> element. The tag goes inside the <head>…</head? Tag ad the rules that are defined with this syntax are applicable to all of the available elements. The following example shows and embedded CSS style element:

<!DOCTYPE html>

<html>

   <head>

      <style type = "text/css" media = "all">

         body {

            background-color: linen;

         }

         h1 {

            color: maroon;

            margin-left: 40px;

         }

      </style>

   </head>  

   <body>

      <h1>This is a heading</h1>

      <p>This is a paragraph.</p>

   </body>

</html>

Attributes

The attributes commonly associated with the <style> elements are shown in the following table:

| Attribute | Value | Description |
| type | Text/css | This attribute specifies the language for the style sheer as an MIME content type and s a required attribute |
| media | screenttytvprojectionhandheldprintbrailleauralall | This specifies which device the document is going to be displayed on. The default value is all and this is classed as an optional attribute |

Inline CSS

You can also use the style attributes from any HTML elements to define the rules. These specific rules will only be applied that the particular element. The generic syntax is:

<element style = "...style rules....">

Attributes

The value of a style attribute is a mixture of different style declarations, each separated by semi colons. The following example is based on the generic syntax:

<html>

   <head>

   </head>

   <body>

      <h1 style = "color:#36C;"> This is inline CSS </h1>

   </body>

</html>

External CSS - The <link> Element

You can use the <link> element as a way of including an external stylesheet in the HTML document. External stylesheet are separate text files that have a .css extension. You will define all of your style rules in this file and this can then be added to any HTML document by using the <link element. The generic syntax is:

<head>

   <link type = "text/css" href = "..." media = "..." />

</head>

Attributes

The attributes that are associated with the <style> elements are as follows:

| Attribute | Value | Description |
| type | text/css | This specifies the language for the style sheet as a MIME content type and is a required attribute |
| href | URL | This specifies that the style sheet has style rules and is also a required attribute |
| media | Screenttytvprojectionhandheldprintbrailleauralall | Tis specifies which devices the document can be displayed on and is an optional attribute. The default value is All |

As an example, consider a style sheet called mystyle.css with these rules:

h1, h2, h3 {

   color: #36C;

   font-weight: normal;

   letter-spacing: .4em;

   margin-bottom: 1em;

   text-transform: lowercase;

}

Now, using the following code, you can add this file to any HTML document:

<head>

   <link type = "text/css" href = "mystyle.css" media = " all" />

</head>

Imported CSS - @import Rule

The @import rule is used to import external stylesheets in a similar way to the <link> element. The generic syntax is:

<head>

   <@import "URL";

</head>

In this syntax, URL is used as the URL of the specific stylesheet that contains the style rules. Another way of writing it would be:

<head>

   <@import url("URL");

</head>

The following example shows you how to import the style sheet to the HTML document:

<head>

   @import "mystyle.css";

</head>

Overriding CSS Rules

So far, we have looked at four different ways to include a style sheet in an HTML document. Now we look at how to override any of the style sheet rules:

*   An inline style sheet will take the top priority, including over any rule that is defined in an external sheet or defined in <style> … </style> tags
*   Any <style> … </style> tag will override an external sheet file
*   External style sheet rules are the lowest priority and will only be applied if the inline style or <style> … </style> tags do not apply

How to Handle an Old Browser

There are quite a few of the older browsers that don’t provide support for CSS so, when you are writing your Embedded CSS in HTML documents, please take care. The following example show how to use comment tags as a way of hiding CSS from an older browser:

<style type="text/css">

   <!--

      body, td {

         color: blue;

      }

   -->

</style>

CSS Comments

Sometimes you will need to add extra comments in to your style sheet blocks but it is very easy to comment on any part of a style sheet. All you do is put your comments within /*…. this is a comment in a style sheet…. */.

You can also use /*…. */ to comment on multi-line blocks in the same way that you would in C or C++ languages.

For example:

<!DOCTYPE html>

<html>

   <head>

      <style>

         p {

            color: red;

            /* a single-line comment */

            text-align: center;

         }

         /* a multi-line comment */

      </style>

   </head>

   <body>

      <p>Hello World!</p>

   </body>

</html>

This will result in “Hello, World!” being displayed on your screen.

# Chapter 4: Measurement Units

CSS supports several different measurements including relative measures, like percentages, and absolute unit, like centimeters, inches, points, etc. These values are required when you specify measurements in the Style rules, for example, e.g. border = “1px solid red”.

The following table lists the CSS measurement units together with examples:

| Unit | Description | Example |
| % | This defines the measurement as a percentage relative to other values. A typical one would be an enclosing element. | p {font-size: 16pt; line-height: 125%;} |
| cm | This defines measurements in centimeters | div {margin-bottom: 2cm;} |
| em | This is a relative measurement for font height in em spaces. An em unit is the equivalent of the size of any given font and, because of this, if you were to assign 12 pt to a font, each of the em units would be 12 pt. This means that 2em would equal 24 pt. | p {letter-spacing: 7em;} |
| ex | This defines the measurement that is relative to the x-height of the font. We determine the x-height by the height of the lowercase x in the specified font | p {font-size: 24pt; line-height: 3ex;} |
| in | This defines the measurement in inches | p {word-spacing: .15in;} |
| mm | This defines the measurement in millimeters | p {word-spacing: 15mm;} |
| pc | This defines the measurement in picas, which is equivalent to 12 points. This means that there are 6 picas to an inch. | p {font-size: 20pc;} |
| pt | This define the measurement in points, which is defined as 1/72 of an inch | body {font-size: 18pt;} |
| px | Defines the measurement in screen pixels. | p {padding: 25px;} |
| vh | This is 1% of the viewport height. | h2 { font-size: 3.0vh; } |
| vw | This is 1% of the viewport width | h1 { font-size: 5.9vw; } |
| vmin | This is 1vw or 1vh, whichever is the smallest | p { font-size: 2vmin;} |

# Chapter 5: Colors

In CSS we use values to specify colors. Usually these are used when we set the color for the text of an element, which is the foreground, or the background of the element. We can also use them to change the color of decorative effects, such as a border.

The color values can be specified in several different formats, as displayed in the following table:

| Format | Syntax | Example |
| Hex Code | #RRGGBB | p{color:#FF0000;} |
| Short Hex Code | #RGB | p{color:#6A7;} |
| RGB % | rgb(rrr%,ggg%,bbb%) | p{color:rgb(50%,50%,50%);} |
| RGB Absolute | rgb(rrr,ggg,bbb) | p{color:rgb(0,0,255);} |
| keyword | aqua, black, etc. | p{color:teal;} |

Let’s look at these formats in more detail:

Hex Codes

Hexadecimals are 6-digit color representations. The first digit – RR – represent red values, GG represents green values and BB represents the blue values.

The values can be taken from graphics software, such as JASC Paintshop Pro, Adobe Photoshop, Advanced Paintbrush, etc. Each of the hexadecimal codes are preceded by a # or a £ sign and the following are examples of hexadecimal notations:

| Color | Color HEX |
|  | #000000 |
|  | #FF0000 |
|  | #00FF00 |
|  | #0000FF |
|  | #FFFF00 |
|  | #00FFFF |
|  | #FF00FF |
|  | #C0C0C0 |
|  | #FFFFFF |

Short Hex Codes

This is just a shorter version of the hex code, and each digit is replicated so that you get the equivalent 6-dgit value.  These values can also be taken from graphics software and are also preceded by the # or £ sign:

| Color | Color HEX |
|  | #000 |
|  | #F00 |
|  | #0F0 |
|  | #0FF |
|  | #FF0 |
|  | #0FF |
|  | #F0F |
|  | #FFF |

RGB Values

We specify this value with the rgb() property, which takes three values – red, green and blue. Values are percentages or integers between 0 and 255\. Be aware that not all browsers offer support for rgb() so try not to use it.

| Color | Color RGB |
|  | rgb(0,0,0) |
|  | rgb(255,0,0) |
|  | rgb(0,255,0) |
|  | rgb(0,0,255) |
|  | rgb(255,255,0) |
|  | rgb(0,255,255) |
|  | rgb(255,0,255) |
|  | rgb(192,192,192) |
|  | rgb(255,255,255) |

Building the Color Codes

If you use the CSS Color Code Builder, you can build, quite literally, millions of different color code but you will need a browser that is Java-enabled to do this.

Browser-Safe Colors

The following tables show you the 216 colors that are considered to be safe and are computer-independent. They vary from hexa code 000000 through to FFFFFF and are safe because all computers can display the colors in the right way on a 25 color palette:

| 000000 | 000033 | 000066 | 000099 | 0000CC | 0000FF |
| 003300 | 003333 | 003366 | 003399 | 0033CC | 0033FF |
| 006600 | 006633 | 006666 | 006699 | 0066CC | 0066FF |
| 009900 | 009933 | 009966 | 009999 | 0099CC | 0099FF |
| 00CC00 | 00CC33 | 00CC66 | 00CC99 | 00CCCC | 00CCFF |
| 00FF00 | 00FF33 | 00FF66 | 00FF99 | 00FFCC | 00FFFF |
| 330000 | 330033 | 330066 | 330099 | 3300CC | 3300FF |
| 333300 | 333333 | 333366 | 333399 | 3333CC | 3333FF |
| 336600 | 336633 | 336666 | 336699 | 3366CC | 3366FF |
| 339900 | 339933 | 339966 | 339999 | 3399CC | 3399FF |
| 33CC00 | 33CC33 | 33CC66 | 33CC99 | 33CCCC | 33CCFF |
| 33FF00 | 33FF33 | 33FF66 | 33FF99 | 33FFCC | 33FFFF |
| 660000 | 660033 | 660066 | 660099 | 6600CC | 6600FF |
| 663300 | 663333 | 663366 | 663399 | 6633CC | 6633FF |
| 666600 | 666633 | 666666 | 666699 | 6666CC | 6666FF |
| 669900 | 669933 | 669966 | 669999 | 6699CC | 6699FF |
| 66CC00 | 66CC33 | 66CC66 | 66CC99 | 66CCCC | 66CCFF |
| 66FF00 | 66FF33 | 66FF66 | 66FF99 | 66FFCC | 66FFFF |
| 990000 | 990033 | 990066 | 990099 | 9900CC | 9900FF |
| 993300 | 993333 | 993366 | 993399 | 9933CC | 9933FF |
| 996600 | 996633 | 996666 | 996699 | 9966CC | 9966FF |
| 999900 | 999933 | 999966 | 999999 | 9999CC | 9999FF |
| 99CC00 | 99CC33 | 99CC66 | 99CC99 | 99CCCC | 99CCFF |
| 99FF00 | 99FF33 | 99FF66 | 99FF99 | 99FFCC | 99FFFF |
| CC0000 | CC0033 | CC0066 | CC0099 | CC00CC | CC00FF |
| CC3300 | CC3333 | CC3366 | CC3399 | CC33CC | CC33FF |
| CC6600 | CC6633 | CC6666 | CC6699 | CC66CC | CC66FF |
| CC9900 | CC9933 | CC9966 | CC9999 | CC99CC | CC99FF |
| CCCC00 | CCCC33 | CCCC66 | CCCC99 | CCCCCC | CCCCFF |
| CCFF00 | CCFF33 | CCFF66 | CCFF99 | CCFFCC | CCFFFF |
| FF0000 | FF0033 | FF0066 | FF0099 | FF00CC | FF00FF |
| FF3300 | FF3333 | FF3366 | FF3399 | FF33CC | FF33FF |
| FF6600 | FF6633 | FF6666 | FF6699 | FF66CC | FF66FF |
| FF9900 | FF9933 | FF9966 | FF9999 | FF99CC | FF99FF |
| FFCC00 | FFCC33 | FFCC66 | FFCC99 | FFCCCC | FFCCFF |
| FFFF00 | FFFF33 | FFFF66 | FFFF99 | FFFFCC | FFFFFF |

# Chapter 6: Background

In this chapter, we are going to look at setting backgrounds for different HTML elements. The following properties can be set:

*   background-color -  to set the background color of the element
*   background-image -  to set the background image of the element
*   background-repeat – to control background image repetition
*   background-position – to control where a background image is positioned
*   background-attachment – to control how a background image scrolls
*   background – used as a shorthand method of specifying various background properties

Setting the Background Color

The following example shows you how to set background color on an element:

<html>

   <head>

   <body>

      <p style = "background-color:yellow;">

      This text has a yellow background color.</p>

   </body>

   </head>

<html>

You will see the following on your screen:

The text has a yellow background color.

How to Set the Background Image

The following example shows how to call a local stored image to set the background:

<html>

   <head>

      <style>

         body  {

            background-image: url("/css/images/css.jpg");

            background-color: #cccccc;

         }

      </style>

      <body>

         <h1>Hello World!</h1>

      </body>

   </head>

<html>

You will now see “Hello, World!” appear on the specified background

How to Repeat the Background Image:

The following is an example of how to repeat a small background image. The no-repeat value can be used for the background-repeat property if the image is NOT to be repeated and is only to be displayed once. By default, the value of background-repeat is set to repeat:

<html>

   <head>

      <style>

         body {

            background-image: url("/css/images/css.jpg");

            background-repeat: repeat;

         }

      </style>

   </head>

   <body>

      <p>Tutorials point</p>

   </body>

</html>

The background that we used in the last example will now be shown repeated. In the following example, we can see how to repeat an image vertically:

<html>

   <head>

      <style>

         body {

            background-image: url("/css/images/css.jpg");

            background-repeat: repeat-y;

         }

      </style>

   </head>

   <body>

      <p>Tutorials point</>

   </body>

</html>

The chosen background image will be repeated vertically.

In the next example, we look at horizontal repetition:

<html>

   <head>

      <style>

         body {

            background-image: url("/css/images/css.jpg");

            background-repeat: repeat-x;

         }

 </style>

   </head>

   <body>

      <p>Tutorials point</>

   </body>

</html>

The chosen background image will be repeated horizontally

How to Set the Position of the Background Image

This example shows you how to set the image in a position that is 100 pixels in from the left hand side:

<html>

   <head>

      <style>

         body {

            background-image: url("/css/images/css.jpg");

            background-position:100px;

         }

      </style>

   </head>

   <body>

      <p>Tutorials point</>

   </body>

</html>

The background image will be placed in the specified position

Now we look at how to set the image 100 pixels in from the left and 200 pixels from the top:

<html>

   <head>

      <style>

         body {

            background-image: url("/css/images/css.jpg");

            background-position:100px 200px;

         }

 </style>

   </head>

   <body>

      <p>Tutorials point</>

   </body>

</html>

The background image will be placed in the specified positon

How to Set the Background Attachment

This determines if an image is to be fixed or if it should scroll when the page is scrolled. First, we look at a fixed image:

<!DOCTYPE html>

<html>

   <head>

      <style>

         body  {

            background-image: url('/css/images/css.jpg');

            background-repeat: no-repeat;

            background-attachment: fixed;

         }

      </style>

   </head>

   <body>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

   </body>

</html>

You will see this line repeated however many times it is in the code:

The background-image is fixed. Try scrolling down the page.

Followed by this:

If you do not see any scrollbars, try to resize the browser window.

Next, we look at setting a scrolling background:

<!DOCTYPE html>

<html>

   <head>

      <style>

         body  {

            background-image: url('/css/images/css.jpg');

            background-repeat: no-repeat;

            background-attachment: fixed;

            background-attachment:scroll;

         }.

      </style>

   </head>

   <body>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

      <p>The background-image is fixed. Try scrolling down the page.</p>

   </body>

</html>

Again, you will see this message repeated on a scrolling background

The background-image is fixed. Try scrolling down the page.

Followed by this:

If you do not see any scrollbars, try to resize the browser window.

How to use the Shorthand Property

The final example shows how to set all of the background properties at the same time by using the shorthand background property:

<p style="background:url(/images/pattern1.gif) repeat fixed;">

   This paragraph has a fixed background image that will be repeated.

</p>

# Chapter 7: Fonts

Now we are going to look at how to set up the fonts. The following are the font properties that you can set for an element:

*   font-family              - is used to change the font face
*   font-style -  is used to turn a font oblique or italic
*   font-weight – is used to increase or decrease the boldness or lightness of a font
*   font-variant – used to give the font a small caps effect
*   font-size – is used to make a font bigger or smaller
*   font – shorthand for specifying various font properties

How to Set the Font Family

The following example shows how to set the font family of a specific element. The value can be any font family name:

<html>

   <head>

   </head>

   <body>

      <p style="font-family:georgia,garamond,serif;">

      This text will be rendered in georgia, garamond, or the default serif font

      depending on which ones are in your system.

      </p>

   </body>

</html>

It will produce the following result –

This text will be rendered in georgia,garamond, or the default serif font, depending on which ones are in your system

How to Set the Font Style

The following example shows how to set the style of an element. Values can be italic, normal, oblique, etc.

<html>

   <head>

   </head>

   <body>

      <p style="font-style:italic;">

      This text is rendered in italic style

      </p>

   </body>

</html>

You will get the following result:

This text is rendered in italic style

How to Set the Font Variant

This example shows how to set the font variant with possible values of small-caps, normal, etc.

<html>

   <head>

   </head>

   <body>

      <p style="font-variant:small-caps;">

      The text is going to be rendered as small caps

      </p>

   </body>

</html>

You will get the following result:

THE TEXT IS GOING TO BE RENDERED AS SMALL CAPS

How to Set the Font Weight

The next example shows how we set the font weight of an element. This property will specify the bold level of the font and possible values include – normal, lighter, bold, bolder, 100, 200, 300, 400, 500, 600, 700, 800, 900, etc.

<html>

   <head>

   </head>

   <body>

      <p style="font-weight:bold;">The font is bold.</p>

      <p style="font-weight:bolder;">The font is bolder.</p>

      <p style="font-weight:500;">The font is 500 weight.</p>

   </body>

</html>

You will get the following result:

The font is bold.

The font is bolder.

The font is 500 weight.

How to Set the Font Size

This example shows how to set up the font size of the element. This is used as a way of controlling the font size and has possible values of – small, x-small, xx-small, xx-large, x-large, large, smaller, larger, %, or size in pixels:

<html>

   <head>

   </head>

   <body>

      <p style="font-size:20px;">The font size is 20 pixels</p>

      <p style="font-size:small;">The font size is small</p>

      <p style="font-size:large;">The font size is large</p>

   </body>

</html>

You will get the following result:

The font size is 20 pixels

The font size is small

The font size is large

How to Set Font Size Adjust

This example will demonstrate how we set the font size adjust and lets you change the x-height to make the font more readable. The possible values can be any number:

<html>

   <head>

   </head>

   <body>

      <p style="font-size-adjust:0.61;">

         The text uses a font-size-adjust value.

      </p>

   </body>

</html>

You will get the following result -

THE TEXT USES A FONT-SIZE-ADJUST VALUE.

How to Set the Font Stretch

This next example shows you how to set up the font stretch and it relies on your computer to have either an expanded or a condensed version of the particular font. The values could possibly be – wider, normal, narrower, extra-condensed, ultra-condensed, condensed, semi-condensed, expanded, semi-expanded, extra-expanded, ultra-expanded:

<html>

   <head>

   </head>

   <body>

      <p style="font-stretch:ultra-expanded;">

         If this doesn't look like it works, most likely your computer does not have a condensed or expanded version of the font

      </p>

   </body>

</html>

It will produce the following result –

If this doesn't look like it works, most likely your computer does not have a condensed or expanded version of the font

How to Set the Shorthand Property

The final example shows you how to use the font property to set all of the font properties at the same time:

<html>

   <head>

   </head>

   <body>

      <p style="font:italic small-caps bold 15px georgia;">

      This will apply all of the properties on the text at the same time.

      </p>

   </body>

</html>

It will produce the following result –

THIS WILL APPLY ALL OF THE PROPERTIES ON THE TEXT AT THE SAME TIME.

# Chapter 8: Text

This chapter is going to take a look at how we can manipulate text with the use of some CSS properties. The following text properties can be used on an element:

*   color – used to set what color the text is
*   direction – used to set the direction of the text
*   letter-spacing – used to add in or remove spaces between letter in a word
*   text-indent – used to indent the first line of a paragraph of text
*   text-align – used to align the text in an entire document
*   text-decoration – used to add decoration to text, such as underline, overline, and strikethrough
*   text-transform – used to either capitalize the text or convert between upper and lower case letters
*   white-space – used to control text flow and formatting
*   text-shadow – used to set a shadow around the text

How to Set the Text Color

This example shows how we set the color of the text, using values of any color name in any format that is valid

<html>

   <head>

   </head>

   <body>

      <p style="color:red;">

      This text is shown in red.

      </p>

   </body>

</html>

You will see the following result -

This text is shown in red.

How to Set the Direction of the Text

The next example shows how we set the text direction, using values of ltr or rtl

<html>

   <head>

   </head>

   <body>

      <p style="direction:rtl;">

      This text is going to be rendered from right to left

      </p>

   </body>

</html>

You will see this result -

This text is going to be rendered from right to left

How to Set the Spaces Between Characters

This example shows how we set up the spaces between the characters, using values of normal or number specifying space

<html>

   <head>

   </head>

   <body>

      <p style="letter-spacing:5px;">

      This text will have spaces between letters.

      </p>

   </body>

</html>

You will see this result -

This text will have spaces between letters.

How to Set the Spaces Between Words

The next example shows how we set space in between words, using values of normal or number specifying space

<html>

   <head>

   </head>

   <body>

      <p style="word-spacing:5px;">

      This text has spaces between words.

      </p>

   </body>

</html>

You will see the following result -

This text has spaces between words.

How to Set the Text Indent

The next example shows how we indent the first line of a new paragraph using values of number specifying indent space or %

<html>

   <head>

   </head>

   <body>

      <p style="text-indent:1cm;">

      The text has the first line indented by 1cm and it will remain at

      this position. This is done using the CSS text-indent property.

      </p>

   </body>

</html>

You will see this result -

 The text has the first line indented by 1cm and it will remain at this position. This is done using the CSS text-indent property

How to Set up the Text Alignment

This example shows how we align text, using values of justify, left, right and center

<html>

   <head>

   </head>

   <body>

      <p style="text-align:right;">

      The text will be right aligned.

      </p>

      <p style="text-align:center;">

      The text will be center aligned.

      </p>

      <p style="text-align:left;">

      The text will be left aligned.

      </p>

   </body>

</html>

You will see the following result -

The text will be right aligned.

The text will be center aligned.

The text will be left aligned.

How to Decorate Text

Now we look at an example showing how we decorate text, using values of none, overline, underline, blink and strikethrough

<html>

   <head>

   </head>

   <body>

      <p style="text-decoration:underline;">

      This text is underlined

      </p>

      <p style="text-decoration:line-through;">

      This text is struck through.

      </p>

      <p style="text-decoration:overline;">

      This text has an over line.

      </p>

      <p style="text-decoration:blink;">

      This text has a blinking effect

      </p>

   </body>

</html>

You will see the following result -

This text is underlined

This text is struck through.

This text has an over line.

This text has a blinking effect

How to Set Text Cases

This example shows how we set up text cases using values of non, uppercase, lowercase and capitalize

<html>

   <head>

   </head>

   <body>

      <p style="text-transform:capitalize;">

      This text will be capitalized

      </p>

      <p style="text-transform:uppercase;">

      This text will be in uppercase

      </p>

      <p style="text-transform:lowercase;">

      This text will be in lowercase

      </p>

      </body>

</html>

You will see the following result -

This Text Will Be Capitalized

THIS text WILL BE IN UPPERCASE

this text will be in lowercase

How to Set Whitespace between Text

This example shows how to handle whitespace in an element, using values of nowrap, normal and pre

<html>

   <head>

   </head>

   <body>

      <p style="white-space:pre;">

      This text will have a line break and the white-space pre setting will tell the browser to honor

      it the same as the HTML pre tag.</p>

   </body>

</html>

You will see the following result -

This text will have a line break and the white-space pre setting will tell the browser to honor it the same as the HTML pre tag.</p>.

How to Set a Text Shadow

This final example shows how to set a shadow around a piece of text. Be aware that this may not have the support of every browser

<html>

   <head>

   </head>

   <body>

      <p style="text-shadow:4px 4px 8px blue;">

      Provided your browser will support CSS text-shadow property, the text will have a blue shadow

      </p>

   </body>

</html>

You will see the following result -

Provided your browser will support CSS text-shadow property, the text will have a blue shadow

# Chapter 9: Using Images

Images are an important part of websites and, although you shouldn’t use too many, those you do use should be of good quality and in the right place. CSS helps to control the display of these images by allowing you to set the following properties:

*   Border – this is used to set the width of the border on the image
*   Height – this is used to set the height of the image
*   Width – this is used to set the width of the image
*   -most-opacity -  this used to determine the opacity of the image

Image Border

This property is used to set the width of the border on the image and can use values of length or %. For example:

<html>

   <head>

   </head>

   <body>

      <img style="border:0px;" src="/css/images/logo.png" />

      <br />

      <img style="border:3px dashed red;" src="/css/images/logo.png" />

   </body>

</html>

The result will be a logo without a border and then a logo with a dotted red border

Image Height

This property is used to set how high an image is and can use values of length or %. When you use %, the value is applied to the box which the image is in:

<html>

   <head>

   </head>

   <body>

      <img style="border:1px solid red; height:100px;" src="/css/images/logo.png" />

      <br />

      <img style="border:1px solid red; height:50%;" src="/css/images/logo.png" />

   </body>

</html>

The result will be two logos, exactly the same, but one taller than the other

Image Width

This is used to set the width of an image using value of % or length. As with height, using percentage applies to the box the image is in

<html>

   <head>

   </head>

   <body>

      <img style="border:1px solid red; width:150px;" src="/css/images/logo.png" />

      <br />

      <img style="border:1px solid red; width:100%;" src="/css/images/logo.png" />

   </body>

</html>

The result will be two identical logos but of different sizes

-Moz-Opacity

The final property is use to set up the opacity of the image and is used with Mozilla Firefox. For Internet Explorer, we use filter:alpha (opacity:x), to come up with transparent images.

In Mozilla Firefox, in the property (-moz-opacity:x), x may hold a value of anywhere between 0.0 and 1.0\. The lower the value, the more transparent the image. By the same token, in Internet Explorer (filter:apha(opacity=x)), the value of x can be anywhere between 0 and 100. Again, the lower the value, the more transparent the image is.

<html>

   <head>

   </head>

   <body>

      <img style="border:1px solid red;-moz-opacity:0.4;filter:alpha(opacity=40);" src="/css/images/logo.png" />

   </body>

</html>

The result will be a logo with a border of solid red.

# Chapter 10: Links

In this chapter, we take a look at how to use CSS to set the properties of a hyper link. The following properties can be set:

*   :link is used to signify unvisited hyperlinks.
*   :visited is used to signify visited hyperlinks.
*   :hover is used to signify elements that have the mouse pointer hovering over the top.
*   :active is used to signify elements that are currently being clicked.

Normally, these properties are stored in the header of an HTML document. Remember the following rules for effective use:

*   a:hover comes after a:link and a:visited in CSS definition
*   a:active comes after a:hover, as shown in the next example:

<style type="text/css">

   a:link {color: #000000}

   a:visited {color: #006600}

   a:hover {color: #FFCC00}

   a:active {color: #FF00CC}

</style>

Next we will look at how these properties are used for different effects on hyperlinks.

Set the Color

This example shows how we set the color of a link using values that are of any color name in any format that is valid:

<html>

   <head>

      <style type="text/css">

         a:link {color:#000000}

     </style>

   </head>

   <body>

      <a href="">Link</a>

   </body>

</html>

The result will be a black link. Please note that none of these links are clickable; they are just for demonstration purposes.

Link

The Color of Visited Links

This example shows how to set the color of a visited link, again with values of any color name in any format that is valid:

<html>

   <head>

      <style type="text/css">

         a:visited {color: #006600}

      </style>

   </head>

   <body>

      <a href=""> link</a>

   </body>

</html>

The result will be the following link, black to start and green when clicked on.

Link

Color of Links with Mouse Hover

This example shows how to change the color of a link when we hover the mouse pointer over it:

<html>

   <head>

      <style type="text/css">

         a:hover {color: #FFCC00}

      </style>

   </head>

   <body>

      <a href="">Link</a>

   </body>

</html>

The result will be a black link that changes to yellow when the mouse is hovered over the top

Link

Color of Active Links

This example shows how we change the color of an active link:

<html>

   <head>

      <style type="text/css">

         a:active {color: #FF00CC}

      </style>

   </head>

   <body>

      <a href="">Link</a>

   </body>

</html>

The result will be a black link that changes to pink when it is clicked on.

Link

# Chapter 11: Tables

In this chapter, we are going to look at the properties we can set for HTML tables. The following properties can be set:

*   Border-collapse – this specifies whether the cells of the table should maintain their own appearance or if the browser should control the borders that touch             
*   Border-spacing – this specifies the width of the space between table cells
*   Caption-side captions – these are in the <caption> element and rendered, by default, above the table. They can be used to set the position of the table caption
*   Empty-cells – this specifies whether there should be a border shown on empty cells
*   Table-layout – this lets the browser speed up the table layout by using the first width property it finds for a column without having to load the table and then rendering it

Next we look at these properties with examples.

Border-Collapse

This property may have two values – collapse and separate. This example uses both:

<html>

   <head>

      <style type="text/css">

         table.one {border-collapse:collapse;}

         table.two {border-collapse:separate;}

         td.a {

            border-style:dotted;

            border-width:3px;

            border-color:#000000;

            padding: 10px;

         }

         td.b {

            border-style:solid;

            border-width:3px;

            border-color:#333333;

            padding:10px;

         }

      </style>

   </head>

   <body>

      <table class="one">

         <caption>Collapse Border Example</caption>

         <tr><td class="a1 Cell 1 Collapse Example</td></tr>

         <tr><td class="2"> Cell 2 Collapse Example</td></tr>

      </table>

      <br />

      <table class="two">

         <caption>Separate Border Example</caption>

         <tr><td class="1"> Cell 1 Separate Example</td></tr>

         <tr><td class="2"> Cell 2 Separate Example</td></tr>

      </table>

   </body>

</html>

This will give you these results;

| Collapse Border: |
| Cell 1 Collapse Example |
| Cell 2 Collapse Example |

| Separate Border: |
| Cell 1 Separate Example |
| Cell 2 Separate Example |

Border-Spacing

This property specifies how much distance there is between the border of two adjacent cells. It can take either of two values, each of which should be a length unit. One value applies to horizontal and vertical borders while using two values will refer to the vertical and the horizontal spacing.

<style type="text/css">

   /* If you provide a value */

   table.example {border-spacing:10px;}

   /* This is how to provide two values */

   table.example {border-spacing:10px; 15px;}

</style>

The next example modifies the first example:

<html>

   <head>

      <style type="text/css">

         table.one {

            border-collapse:separate;

            width:400px;

            border-spacing:10px;

         }

         table.two {

            border-collapse:separate;

            width:400px;

            border-spacing:10px 50px;

         }

      </style>

   </head>

   <body>

      <table class="one" border="1">

         <caption>Separate Border Example with border-spacing</caption>

         <tr><td> Cell A Collapse Example</td></tr>

         <tr><td> Cell B Collapse Example</td></tr>

      </table>

      <br />

      <table class="two" border="1">

         <caption>Separate Border Example with border-spacing</caption>

         <tr><td> Cell A Separate Example</td></tr>

         <tr><td> Cell B Separate Example</td></tr>

      </table>

   </body>

</html>

Caption-Side Property

This property allows you to specify the position of the <caption> element content in relation to the table.  It can use these four properties – top, left, bottom, right. The following example uses all of the four values:

<html>

   <head>

      <style type="text/css">

         caption.top {caption-side:top}

         caption.bottom {caption-side:bottom}

         caption.left {caption-side:left}

         caption.right {caption-side:right}

      </style>

   </head>

   <body>

      <table style="width:400px; border:1px solid black;">

         <caption class="top">

         This caption will appear at the top

         </caption>

         <tr><td > Cell A</td></tr>

         <tr><td > Cell B</td></tr>

      </table>

      <br />

      <table style="width:400px; border:1px solid black;">

         <caption class="bottom">

         The caption appears at the bottom

         </caption>

         <tr><td > Cell A</td></tr>

         <tr><td > Cell B</td></tr>

      </table>

      <br />

      <table style="width:400px; border:1px solid black;">

         <caption class="left">

         The caption appears at the left

         </caption>

         <tr><td > Cell A</td></tr>

         <tr><td > Cell B</td></tr>

      </table>

      <br />

      <table style="width:400px; border:1px solid black;">

         <caption class="right">

         The caption appears at the right

         </caption>

         <tr><td > Cell A</td></tr>

         <tr><td > Cell B</td></tr>

      </table>

   </body>

</html>

Empty-Cells

This property is used to indicate if an empty cell should have a border or not. It can have one of these three value – hide, show, inherit. This example shows the property being used to hide the borders of the empty cells in the <table> element:

<html>

   <head>

      <style type="text/css">

         table.empty{

            width:350px;

            border-collapse:separate;

            empty-cells:hide;

         }

         td.empty{

            padding:5px;

            border-style:solid;

            border-width:1px;

            border-color:#999999;

         }

      </style>

   </head>

   <body>

      <table class="empty">

      <tr>

         <th></th>

         <th>Title one</th>

         <th>Title two</th>

      </tr>

      <tr>

         <th>Row Title</th>

         <td class="empty">value</td>

         <td class="empty">value</td>

      </tr>

      <tr>

         <th>Row Title</th>

         <td class="empty">value</td>

         <td class="empty"></td>

      </tr>

      </table>

   </body>

</html>

Table-Layout

This property is meant to help you control how the browser lays out or renders a table. It can have one of these three value – inherit, auto or fixed. The next example shows the

<html>

   <head>

      <style type="text/css">

         table.auto {

            table-layout: auto

         }

         table.fixed{

            table-layout: fixed

         }

      </style>

   </head>

   <body>

      <table class="auto" border="1" width="100%">

      <tr>

         <td width="20%">1000000000000000000000000000</td>

         <td width="40%">10000000</td>

         <td width="40%">100</td>

      </tr>

      </table>

      <br />

      <table class="fixed" border="1" width="100%">

      <tr>

         <td width="20%">1000000000000000000000000000</td>

         <td width="40%">10000000</td>

         <td width="40%">100</td>

      </tr>

      </table>

   </body>

</html>

# Chapter 12: Borders

Border properties allow you to say what the border of an element box should look like. The following are the three properties that you can control

*   Border-color – allows you to specify the color of the border
*   Border-style – allows you to specify the style from a choice of values, including a solid line, dashed line, double line, etc.
*   Border-width – allows you to specify the width of the border

Border-Color

This property lets you change the color of a border surrounding an element. You can change each side of the border individually using these properties:

*   Border-bottom-color
*   Border-top-color
*   Border-left-color
*   Border-right-color

This example shows all four properties in use:

<html>

   <head>

      <style type="text/css">

         p.example1{

            border:1px solid;

            border-bottom-color:#009900; /* Green */

            border-top-color:#FF0000;    /* Red */

            border-left-color:#330000;   /* Black */

            border-right-color:#0000CC;  /* Blue */

         }

         p.example2{

            border:1px solid;

            border-color:#009900;        /* Green */

         }

      </style>

   </head>

   <body>

      <p class="example1">

      The example shows all borders in different colors.

      </p>

      <p class="example2">

      The example shows all borders in green only.

      </p>

   </body>

</html>

The result will

This example shows all borders in different colors.

This example shows all borders in green only.

Border-style

This property let you select one of these styles:

*   None – has no border at all
*   Solid – gives the border a solid line
*   Dotted – the border is made of dots
*   Dashed – the border is made of short lines
*   Double – this is two solid lines
*   Groove – make the border look like it has been carved into the page
*   Ridge – does the opposite of groove
*   Inset – the box looks embedded in the page
*   Outset – the box looks as though it is coming out of the page
*   Hidden – exactly the same as for None but with the exception of a border-conflict resolution for table elements

As with color, you can change the style of each individual side of the border, using these properties:

*   Border-bottom-style
*   Border-top-style
*   Border-left-style
*   Border-right-style

This example uses all four of these styles:

<html>

   <head>

   </head>

   <body>.

      <p style="border-width:4px; border-style:none;">

      This is a border with a width of none.

      </p>

      <p style="border-width:4px; border-style:solid;">

      This is a solid border.

      </p>

      <p style="border-width:4px; border-style:dashed;">

      This is a dashed border.

      </p>

      <p style="border-width:4px; border-style:double;">

      This is a double border.

      </p>

      <p style="border-width:4px; border-style:groove;">

      This is a groove border.

      </p>

      <p style="border-width:4px; border-style:ridge">

      This is a ridge border.

      </p>

      <p style="border-width:4px; border-style:inset;">

      This is an inset border.

      </p>

      <p style="border-width:4px; border-style:outset;">

      This is an outset border.

      </p>

      <p style="border-width:4px; border-style:hidden;">

      This is a hidden border.

      </p>

      <p style="border-width:4px;border-top-style:solid;

      border-bottom-style:dashed; border-left-style:groove; border-right-style:double;">

      This is a border with four different styles.

      </p>

   </body>

</html>

The result will be -

This is a border with none width.

This is a solid border.

This is a dashed border.

This is a double border.

This is a groove border.

This is a ridge border.

This is an inset border.

This is an outset border.

This is a hidden border.

This is a border with four different styles.

Border-Width

This allows you to set the width of the border, using a value of length in pt., px or cm or you can set it to thick, medium or thin. You can change each side of the border individually, using these properties:

*   border-bottom-width 
*   border-top-width 
*   border-left-width
*   border-right-width 

This example use all of these properties

<html>

   <head>

   </head>

   <body>

      <p style="border-width:4px; border-style:solid;">

      This is a solid border with a width of 4px.

      </p>

      <p style="border-width:4pt; border-style:solid;">

      This is a solid border whose width is 4pt.

      </p>

      <p style="border-width:thin; border-style:solid;">

      This is a solid border whose width is thin.

      </p>

      <p style="border-width:medium; border-style:solid;">

      This is a solid border whose width is medium;

      </p>

      <p style="border-width:thick; border-style:solid;">

      This is a solid border whose width is thick.

      </p>

      <p style="border-bottom-width:4px;border-top-width:10px;

      border-left-width: 2px;border-right-width:15px;border-style:solid;">

      This is a border with four different widths.

      </p>

   </body>

</html>

The result will be:

This is a solid border whose width is 4px.

This is a solid border whose width is 4pt.

This is a solid border whose width is thin.

This is a solid border whose width is medium;

This is a solid border whose width is thick.

This is a border with four different widths.

Shorthand Border Properties

Using the shorthand border property, you can specify the style, color and width of the lines using just one property instead of three. The following example uses the border property to combine all three and you will find that this is the most commonly used method of setting a border around an element:

<html>

   <head>

   </head>

   <body>

      <p style="border:4px solid red;">

Another example:

      </p>

   </body>

</html>

# Chapter 13: Margins

The final chapter deals with the margin property, i.e. the space around the HTML element. Martin property values are not inherited by child elements and it is also possible that you can use negative value as a way of overlapping the content.

Remember – the vertical margins that are adjacent to one another (that is the top and bottom margins) are going to collapse into each other so that distance between each block is NOT the sum of the margins; instead it is the larger of the margins or the same as one margin if both are the same size.

The following properties can be used:

*   Margin – specifies the shorthand for setting all the margin properties in one single declaration
*   Margin-bottom – specifies the bottom margin
*   Margin-top – specifies the top margin
*   Margin-left – specifies the left margin
*   Margin-right – specifies the right margin

Now we will look at how these properties are used.

Margin Property

This is a shorthand property that lets you set all properties for all four of the margin with a single declaration. The following example shows you how to set a margin round a paragraph:

<html>

   <head>

   </head>

   <body>

      <p style="margin: 15px; border:1px solid black;">

      all four margins will be 15px

      </p>

      <p style="margin:10px 2%; border:1px solid black;">

      top and bottom margin will be 10px, left and right margin will be 2% of the total width of the document.

      </p>

      <p style="margin: 10px 2% -10px; border:1px solid black;">

      top margin will be 10px, left and right margin will be 2% of the total width of the document, bottom margin will be -10px

      </p>

      <p style="margin: 10px 2% -10px auto; border:1px solid black;">

      top margin will be 10px, right margin will be 2% of the total width of the document, bottom margin will be -10px, left margin will be set by the browser

      </p>

   </body>

</html>

You will see the following result -

all four margins will be 15px

top and bottom margin will be 10px, left and right margin will be 2% of the total width of the document.

top margin will be 10px, left and right margin will be 2% of the total width of the document, bottom margin will be -10px

top margin will be 10px, right margin will be 2% of the total width of the document, bottom margin will be -10px, left margin will be set by the browser

Margin-Bottom

This allows you set up the bottom margin using a value of auto, length or %

<html>

   <head>

   </head>

   <body>

      <p style="margin-bottom: 15px; border:1px solid black;">

      This is a paragraph with a specified bottom margin.

      </p>

      <p style="margin-bottom: 5%; border:1px solid black;">

      This is another paragraph with a specified bottom margin in percent

      </p>

   </body>

</html>

The result will be -

This is a paragraph with a specified bottom margin

This is another paragraph with a specified bottom margin in percent

Margin-Top

This allows you to specify the top margin and uses a value of auto, length or %

<html>

   <head>

   </head>

   <body>

      <p style="margin-top: 15px; border:1px solid black;">

      This is a paragraph with a specified top margin

      </p>

      <p style="margin-top: 5%; border:1px solid black;">

      This is another paragraph with a specified top margin in percent

      </p>

   </body>

</html>

The result will be as follows -

This is a paragraph with a specified top margin

This is another paragraph with a specified top margin in percent

Margin-Left

This property allows you to set the left margin and use a value of %, auto or length

<html>

   <head>

   </head>

   <body>

      <p style="margin-left: 15px; border:1px solid black;">

      This is a paragraph with a specified left margin

      </p>

      <p style="margin-left: 5%; border:1px solid black;">

      This is another paragraph with a specified top margin in percent

      </p>

   </body>

</html>

The result will be as follows -

This is a paragraph with a specified left margin

This is another paragraph with a specified top margin in percent

Margin-Right

This property allows you to specify the right margin, using a value of auto, length or %

<html>

   <head>

   </head>

   <body>

      <p style="margin-right: 15px; border:1px solid black;">

      This is a paragraph with a specified right margin

      </p>

      <p style="margin-right: 5%; border:1px solid black;">

      This is another paragraph with a specified right margin in percent

      </p>

   </body>

</html>

The result will be shown as follows -

This is a paragraph with a specified right margin

This is another paragraph with a specified right margin in percent

# Conclusion

Thank you for purchasing my book, I hope that you found it helpful. As you have seen, CSS is a truly amazing tool for anyone who wants to get into the world of web design. Although it is one of the easiest to understand and learn, I won’t promise that you can learn it overnight. Like any computer language, it takes time and it takes patience.

You need to be dedicated to learning it and, once you have, you must be prepared to keep up with all the latest developments. CSS isn’t a program you can learn, forget about and then pick up again a few months later. While you will still have the basics in your mind, in those few months, much may have happened and many changes may have been made. It is vital that you keep up with the changes and that you use CSS on a daily basis to ensure that you do not lose any of your newfound skills.

CSS is a program that you learn, that you understand and that you live. Please may I ask a small favor of you - will you leave a review for me at Amazon.com? It isn’t only helpful to me; it is helpful to others who may decide to purchase my book.

As stated earlier, this is to reiterate that some of the example code that I have used in this book is attributed to www.tutorialspoint.com