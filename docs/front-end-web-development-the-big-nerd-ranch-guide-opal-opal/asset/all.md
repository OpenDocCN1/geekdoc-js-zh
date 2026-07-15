![](Front/cover.jpg)

# Front-End Web Development: The Big Nerd Ranch Guide

### by Chris Aquino and Todd Gandee

Copyright © 2016 Big Nerd Ranch, LLC

All rights reserved. Printed in the United States of America. This publication is protected by copyright, and permission must be obtained from the publisher prior to any prohibited reproduction, storage in a retrieval system, or transmission in any form or by any means, electronic, mechanical, photocopying, recording, or likewise. For information regarding permissions, contact

Big Nerd Ranch, LLC
200 Arizona Ave NE
Atlanta, GA 30307
(770) 817-6373
http://www.bignerdranch.com/
book-comments@bignerdranch.com

The 10-gallon hat with propeller logo is a trademark of Big Nerd Ranch, LLC.

Exclusive worldwide distribution of the English edition of this book by

Pearson Technology Group
800 East 96th Street
Indianapolis, IN 46240 USA
http://www.informit.com

The authors and publisher have taken care in writing and printing this book but make no expressed or implied warranty of any kind and assume no responsibility for errors or omissions. No liability is assumed for incidental or consequential damages in connection with or arising out of the use of the information or programs contained herein.

Many of the designations used by manufacturers and sellers to distinguish their products are claimed as trademarks. Where those designations appear in this book, and the publisher was aware of a trademark claim, the designations have been printed with initial capital letters or in all capitals.

ISBN-10  0134432533
ISBN-13  978-0134432533

First edition, first printing, July 2016
Release E.1.1.1

# Dedication

|   | <samp class="emphasis">To Mom and Dad, for buying us that computer. To Dave and Glenn, for letting your little brother completely hog it. And to Angela, for giving me a life away from the screen.</samp> |   |
|   | — C.A. |

|   | <samp class="emphasis">To my mom and dad, thank you for giving me room to find my own way. To my wife, thank you for loving a nerd.</samp> |   |
|   | — T.G. |

# Acknowledgments

As authors, we can take full credit for typing the words and creating the diagrams. (Yay, us!) But the whole truth is that we would still be staring at a blank page if not for the efforts of an army of contributors, collaborators, and mentors.

*   Aaron Hillegass, for believing that the two of us could produce a work worthy of the Big Nerd Ranch name. Thank you for your immeasurable faith and support.

*   Matt Mathias, for guiding us through the development of this book, especially during the crucial last mile. You made sure that time that would have been spent watching cat videos or Downton Abbey reruns was instead dedicated to writing.

*   Brandy Porter, for the care and (literal) feeding of the authors on numerous occasions. You worked your magic behind the curtain, orchestrating a sequence of events that made finishing this work possible. Thank you.

*   Jonathan Martin, our coinstructor and language maven. Thank you for enthusiastically teaching the in-progress course materials on which this book is based and offering thoughtful criticism throughout the many revisions.

*   Our proofreaders, technical reviewers, and guinea pigs: Mike Zornek, Jeremy Sherman, Josh Justice, Jason Reece, Garry Smith, Andrew Jones, Stephen Christopher, and Bill Phillips. Thank you for volunteering as tribute.

*   Elizabeth Holaday, our infinitely patient and reassuring editor. Thank you for breaking us out of the echo chamber, being the voice of reason, and reminding us always of our readers.

*   Ellie Volckhausen, who designed our cover.

*   Simone Payment, our proofreader, who kept things consistent.

*   Chris Loper at IntelligentEnglish.com, who designed and produced the print and ebook versions of the book. His DocBook toolchain made life much easier, too.

Lastly, thank you to the countless students who have taken the week-long training. Without your curiosity and your questions, none of this matters. This work is a reflection of the insight and inspiration you have given us over the span of those many weeks. We hope the otters made the training a little lighter.

# Table of Contents

[Introduction](#pr03.html)

[Learning Front-End Web Development](#pr03.html_idm494071170704)

[Prerequisites](#pr03s02.html)

[How This Book Is Organized](#pr03s03.html)

[How to Use This Book](#pr03s04.html)

[Challenges](#pr03s05.html)

[For the More Curious](#pr03s06.html)

[Using an eBook](#pr03s07.html)

[I. Core Browser Programming](#pt01.html)

[1\. Setting Up Your Development Environment](#ch01.html)

[Installing Google Chrome](#ch01.html_idm494071104784)

[Installing and Configuring Atom](#ch01s02.html)

[Atom plug-ins](#ch01s02.html_idm494071072528)

[Documentation and Reference Sources](#ch01s03.html)

[Crash Course in the Command Line](#ch01s04.html)

[Finding out what directory you are in](#ch01s04.html_se-finding-out-what-directory-you-are-in)

[Creating a directory](#ch01s04.html_se-creating-a-directory)

[Changing directories](#ch01s04.html_se-changing-directories)

[Listing files in a directory](#ch01s04.html_idm494070925952)

[Getting administrator privileges](#ch01s04.html_se-if-you-need-administrator-privileges)

[Quitting a program](#ch01s04.html_se-quitting-a-program)

[Installing Node.js and browser-sync](#ch01s05.html)

[For the More Curious: Alternatives to Atom](#ch01s06.html)

[2\. Setting Up Your First Project](#ch02.html)

[Setting Up Ottergram](#ch02.html_se-setting-up-your-project-folders)

[Initial HTML](#ch02.html_se-creating-the-document)

[Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)

[Adding content](#ch02.html_se-adding-an-unordered-list)

[Adding images](#ch02.html_se-setting-up-styles)

[Viewing the Web Page in the Browser](#ch02s02.html)

[The Chrome Developer Tools](#ch02s03.html)

[For the More Curious: CSS Versions](#ch02s04.html)

[For the More Curious: The favicon.ico](#ch02s05.html)

[Silver Challenge: Adding a favicon.ico](#ch02s06.html)

[3\. Styles](#ch03.html)

[Creating a Styling Baseline](#ch03.html_se-setting-up-layout)

[Preparing the HTML for Styling](#ch03s02.html)

[Anatomy of a Style](#ch03s03.html)

[Your First Styling Rule](#ch03s04.html)

[The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

[Style Inheritance](#ch03s05.html)

[Making Images Fit the Window](#ch03s06.html)

[Color](#ch03s07.html)

[Adjusting the Space Between Items](#ch03s08.html)

[Relationship selectors](#ch03s08.html_idm494070191376)

[Adding a Font](#ch03s09.html)

[Bronze Challenge: Color Change](#ch03s10.html)

[For the More Curious: Specificity! When Selectors Collide…](#ch03s11.html)

[4\. Responsive Layouts with Flexbox](#ch04.html)

[Expanding the Interface](#ch04.html_se-expanding-the-interface)

[Adding the detail image](#ch04.html_se-adding-the-detail-image)

[Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails)

[Flexbox](#ch04s02.html)

[Creating a flex container](#ch04s02.html_idm494069939200)

[Changing the flex-direction](#ch04s02.html_idm494069907888)

[Grouping elements within a flex item](#ch04s02.html_idm494069892384)

[The flex shorthand property](#ch04s02.html_idm494069865184)

[Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504)

[Centering the detail image](#ch04s02.html_idm494069756352)

[Absolute and Relative Positioning](#ch04s03.html)

[5\. Adaptive Layouts with Media Queries](#ch05.html)

[Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

[Adding a Media Query](#ch05s02.html)

[Bronze Challenge: Portrait](#ch05s03.html)

[For the More Curious: Common Solutions (and Bugs) with Flexbox Layouts](#ch05s04.html)

[Gold Challenge: Holy Grail Layout](#ch05s05.html)

[6\. Handling Events with JavaScript](#ch06.html)

[Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

[Your First Script](#ch06s02.html)

[Overview of the JavaScript for Ottergram](#ch06s03.html)

[Declaring String Variables](#ch06s04.html)

[Working in the Console](#ch06s05.html)

[Accessing DOM Elements](#ch06s06.html)

[Writing the setDetails Function](#ch06s07.html)

[Accepting arguments by declaring parameters](#ch06s07.html_idm494069199216)

[Returning Values from Functions](#ch06s08.html)

[Adding an Event Listener](#ch06s09.html)

[Accessing All the Thumbnails](#ch06s10.html)

[Iterating Through the Array of Thumbnails](#ch06s11.html)

[Silver Challenge: Link Hijack](#ch06s12.html)

[Gold Challenge: Random Otters](#ch06s13.html)

[For the More Curious: Strict Mode](#ch06s14.html)

[For the More Curious: Closures](#ch06s15.html)

[For the More Curious: NodeLists and HTMLCollections](#ch06s16.html)

[For the More Curious: JavaScript Types](#ch06s17.html)

[7\. Visual Effects with CSS](#ch07.html)

[Hiding and Showing the Detail Image](#ch07.html_idm494068847072)

[Creating styles to hide the detail image](#ch07.html_idm494068824128)

[Writing the JavaScript to hide the detail image](#ch07.html_idm494068784320)

[Listening for the keypress event](#ch07.html_idm494068768944)

[Showing the detail image again](#ch07.html_idm494068716320)

[State Changes with CSS Transitions](#ch07s02.html)

[Working with the transform property](#ch07s02.html_se-working-with-the-transform-property)

[Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)

[Using a timing function](#ch07s02.html_idm494068618640)

[Transition on class change](#ch07s02.html_se-transition-on-class-change)

[Triggering transitions with JavaScript](#ch07s02.html_se-triggering-with-javascript)

[Custom Timing Functions](#ch07s03.html)

[For the More Curious: Rules for Type Coercion](#ch07s04.html)

[II. Modules, Objects, and Forms](#pt02.html)

[8\. Modules, Objects, and Methods](#ch08.html)

[Modules](#ch08.html_se-module-pattern)

[The module pattern](#ch08.html_se-module-as-transforming-portal)

[Modifying an object with an IIFE](#ch08.html_se-using-iife-to-modify)

[Setting Up CoffeeRun](#ch08s02.html)

[Creating the DataStore Module](#ch08s03.html)

[Adding Modules to a Namespace](#ch08s04.html)

[Constructors](#ch08s05.html)

[A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)

[Adding methods to the constructor](#ch08s05.html_se-creating-the-get-and-getall-methods)

[Creating the Truck Module](#ch08s06.html)

[Adding orders](#ch08s06.html_se-writing-createorder)

[Removing orders](#ch08s06.html_se-writing-deliverorder)

[Debugging](#ch08s07.html)

[Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)

[Setting the value of this with bind](#ch08s07.html_se-changing-the-value-of-this-with-.bind)

[Initializing CoffeeRun on Page Load](#ch08s08.html)

[Creating the Truck instance](#ch08s08.html_se-creating-the-truck-instance)

[Bronze Challenge: Truck ID for Non-Trekkies](#ch08s09.html)

[For the More Curious: Private Module Data](#ch08s10.html)

[Silver Challenge: Making data Private](#ch08s11.html)

[For the More Curious: Setting this in forEach’s Callback](#ch08s12.html)

[9\. Introduction to Bootstrap](#ch09.html)

[Adding Bootstrap](#ch09.html_se-adding-bootstrap)

[How Bootstrap works](#ch09.html_se-how-bootstrap-works)

[Creating the Order Form](#ch09s02.html)

[Adding text input fields](#ch09s02.html_se-adding-a-textfield)

[Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

[Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)

[Adding a range slider](#ch09s02.html_se-adding-a-slider)

[Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

[10\. Processing Forms with JavaScript](#ch10.html)

[Creating the FormHandler Module](#ch10.html_se-creating-the-formhandler-module)

[Introduction to jQuery](#ch10.html_se-orphan-jquery)

[Importing jQuery](#ch10.html_se-importing-jquery)

[Configuring instances of FormHandler with a selector](#ch10.html_se-configuring-the-instance-with-a-selector)

[Adding the submit Handler](#ch10s02.html)

[Extracting the data](#ch10s02.html_se-extracting-the-data)

[Accepting and calling a callback](#ch10s02.html_se-accepting-a-callback)

[Using FormHandler](#ch10s03.html)

[Registering createOrder as a submit handler](#ch10s03.html_se-registering-createorder-as-a-submit-handler)

[UI Enhancements](#ch10s04.html)

[Bronze Challenge: Supersize It](#ch10s05.html)

[Silver Challenge: Showing the Value as the Slider Changes](#ch10s06.html)

[Gold Challenge: Adding Achievements](#ch10s07.html)

[11\. From Data to DOM](#ch11.html)

[Setting Up the Checklist](#ch11.html_se-setup-forms2)

[Creating the CheckList Module](#ch11s02.html)

[Creating the Row Constructor](#ch11s03.html)

[Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)

[Creating CheckList Rows on Submit](#ch11s04.html)

[Manipulating this with call](#ch11s04.html_se-use-.call-to-manipulate-the-value-of-this)

[Delivering an Order by Clicking a Row](#ch11s05.html)

[Creating the CheckList.prototype.removeRow method](#ch11s05.html_se-adding-the-removerow-prototype-method-to-checklist.)

[Removing overwritten entries](#ch11s05.html_se-ensuring-unique-entries)

[Writing the addClickHandler method](#ch11s05.html_se-adding-the-event-click-handler)

[Calling addClickHandler](#ch11s05.html_se-calling-addclickhandler)

[Bronze Challenge: Adding the Strength to the Description](#ch11s06.html)

[Silver Challenge: Color Coding by Flavor Shot](#ch11s07.html)

[Gold Challenge: Allowing Order Editing](#ch11s08.html)

[12\. Validating Forms](#ch12.html)

[The required Attribute](#ch12.html_se-the-required-attribute)

[Validating with Regular Expressions](#ch12s02.html)

[Constraint Validation API](#ch12s03.html)

[Listening for the input event](#ch12s03.html_se-listening-for-the-input-event)

[Associating the validation check with the input event](#ch12s03.html_se-associating-the-validation-check-with-the-input-event)

[Triggering the validity check](#ch12s03.html_se-triggering-the-validity-check)

[Styling Valid and Invalid Elements](#ch12s04.html)

[Silver Challenge: Custom Validation for Decaf](#ch12s05.html)

[For the More Curious: The Webshims Library](#ch12s06.html)

[13\. Ajax](#ch13.html)

[XMLHttpRequest Objects](#ch13.html_se-xmlhttprequest-objects)

[RESTful Web Services](#ch13s02.html)

[The RemoteDataStore Module](#ch13s03.html)

[Sending Data to the Server](#ch13s04.html)

[Using jQuery’s $.post method](#ch13s04.html_se-using-jquerys-.post-method)

[Adding a callback](#ch13s04.html_se-adding-a-callback)

[Inspecting the Ajax request and response](#ch13s04.html_se-inspecting-the-ajax-request-and-response)

[Retrieving Data from the Server](#ch13s05.html)

[Inspecting the response data](#ch13s05.html_se-inspecting-the-response-data)

[Adding a callback argument](#ch13s05.html_se-adding-a-callback-argument)

[Deleting Data from the Server](#ch13s06.html)

[Using jQuery’s $.ajax method](#ch13s06.html_se-using-jquerys-.ajax-method)

[Replacing DataStore with RemoteDataStore](#ch13s07.html)

[Silver Challenge: Validating Against the Remote Server](#ch13s08.html)

[For the More Curious: Postman](#ch13s09.html)

[14\. Deferreds and Promises](#ch14.html)

[Promises and Deferreds](#ch14.html_se-promise-foundation)

[Returning Deferred](#ch14s02.html)

[Registering Callbacks with then](#ch14s03.html)

[Handling Failures with then](#ch14s04.html)

[Using Deferreds with Callback-Only APIs](#ch14s05.html)

[Giving DataStore a Promise](#ch14s06.html)

[Creating and returning Promises](#ch14s06.html_se-creating-returning-promises)

[Resolving a Promise](#ch14s06.html_se-resolving-rejecting)

[Promise-ifying the other DataStore methods](#ch14s06.html_se-updating-other-methods)

[Silver Challenge: Fallback to DataStore](#ch14s07.html)

[III. Real-Time Data](#pt03.html)

[15\. Introduction to Node.js](#ch15.html)

[Node and npm](#ch15.html_se-node-and-npm)

[npm init](#ch15.html_se-npm-init)

[npm scripts](#ch15.html_se-npm-scripts)

[Hello, World](#ch15s02.html)

[Adding an npm Script](#ch15s03.html)

[Serving from Files](#ch15s04.html)

[Reading a file with the fs module](#ch15s04.html_se-reading-a-file-with-the-fs-module)

[Working with the request URL](#ch15s04.html_se-working-with-the-request-url)

[Using the path module](#ch15s04.html_se-using-the-path-module)

[Creating a custom module](#ch15s04.html_se-create-a-custom-module)

[Using your custom module](#ch15s04.html_se-using-your-custom-module)

[Error Handling](#ch15s05.html)

[For the More Curious: npm Module Registry](#ch15s06.html)

[Bronze Challenge: Creating a Custom Error Page](#ch15s07.html)

[For the More Curious: MIME Types](#ch15s08.html)

[Silver Challenge: Providing a MIME Type Dynamically](#ch15s09.html)

[Gold Challenge: Moving Error Handling to Its Own Module](#ch15s10.html)

[16\. Real-Time Communication with WebSockets](#ch16.html)

[Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

[Testing Your WebSockets Server](#ch16s02.html)

[Creating the Chat Server Functionality](#ch16s03.html)

[First Chat!](#ch16s04.html)

[For the More Curious: socket.io WebSockets Library](#ch16s05.html)

[For the More Curious: WebSockets as a Service](#ch16s06.html)

[Bronze Challenge: Am I Repeating Myself?](#ch16s07.html)

[Silver Challenge: Speakeasy](#ch16s08.html)

[Gold Challenge: Chat Bot](#ch16s09.html)

[17\. Using ES6 with Babel](#ch17.html)

[Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

[The Chattrbox Client Application](#ch17s02.html)

[First Steps with Babel](#ch17s03.html)

[Class syntax](#ch17s03.html_se-class-syntax)

[Using Browserify for Packaging Modules](#ch17s04.html)

[Running the build process](#ch17s04.html_se-running-the-build-process)

[Adding the ChatMessage Class](#ch17s05.html)

[Creating the ws-client Module](#ch17s06.html)

[Connection handling](#ch17s06.html_se-building-handlers)

[Handling events and sending messages](#ch17s06.html_idm494065676352)

[Sending and echoing a message](#ch17s06.html_idm494065645568)

[For the More Curious: Compiling to JavaScript from Other Languages](#ch17s07.html)

[Bronze Challenge: Default Import Name](#ch17s08.html)

[Silver Challenge: Closed Connection Alert](#ch17s09.html)

[For the More Curious: Hoisting](#ch17s10.html)

[For the More Curious: Arrow Functions](#ch17s11.html)

[18\. ES6, the Adventure Continues](#ch18.html)

[Installing jQuery as a Node Module](#ch18.html_se-installing-jquery-as-a-node-module)

[Creating the ChatForm Class](#ch18s02.html)

[Connecting ChatForm to the socket](#ch18s02.html_se-connecting-the-chatform-to-the-socket)

[Creating the ChatList Class](#ch18s03.html)

[Using Gravatars](#ch18s04.html)

[Prompting for Username](#ch18s05.html)

[User Session Storage](#ch18s06.html)

[Formatting and Updating Message Timestamps](#ch18s07.html)

[Bronze Challenge: Adding Visual Effects to Messages](#ch18s08.html)

[Silver Challenge: Caching Messages](#ch18s09.html)

[Gold Challenge: Separate Chat Rooms](#ch18s10.html)

[IV. Application Architecture](#pt04.html)

[19\. Introduction to MVC and Ember](#ch19.html)

[Tracker](#ch19.html_se-ember-an-mvc-framework)

[Ember: An MVC Framework](#ch19s02.html)

[Installing Ember](#ch19s02.html_se-install)

[Creating an Ember application](#ch19s02.html_se-creating-an-ember-application)

[Starting up the server](#ch19s02.html_se-start-up-the-server)

[External Libraries and Addons](#ch19s03.html)

[Configuration](#ch19s04.html)

[For the More Curious: npm and Bower Install](#ch19s05.html)

[Bronze Challenge: Limiting Imports](#ch19s06.html)

[Silver Challenge: Adding Font Awesome](#ch19s07.html)

[Gold Challenge: Customizing the NavBar](#ch19s08.html)

[20\. Routing, Routes, and Models](#ch20.html)

[ember generate](#ch20.html_se-ember-generate)

[Nesting Routes](#ch20s02.html)

[Ember Inspector](#ch20s03.html)

[Assigning Models](#ch20s04.html)

[beforeModel](#ch20s05.html)

[For the More Curious: setupController and afterModel](#ch20s06.html)

[21\. Models and Data Binding](#ch21.html)

[Model Definitions](#ch21.html_se-model-definitions)

[createRecord](#ch21s02.html)

[get and set](#ch21s03.html)

[Computed Properties](#ch21s04.html)

[For the More Curious: Retrieving Data](#ch21s05.html)

[For the More Curious: Saving and Destroying Data](#ch21s06.html)

[Bronze Challenge: Changing the Computed Property](#ch21s07.html)

[Silver Challenge: Flagging New Sightings](#ch21s08.html)

[Gold Challenge: Adding Titles](#ch21s09.html)

[22\. Data – Adapters, Serializers, and Transforms](#ch22.html)

[Adapters](#ch22.html_se-adapter)

[Content Security Policy](#ch22s02.html)

[Serializers](#ch22s03.html)

[Transforms](#ch22s04.html)

[For the More Curious: Ember CLI Mirage](#ch22s05.html)

[Silver Challenge: Content Security](#ch22s06.html)

[Gold Challenge: Mirage](#ch22s07.html)

[23\. Views and Templates](#ch23.html)

[Handlebars](#ch23.html_se-handlebars)

[Models](#ch23s02.html)

[Helpers](#ch23s03.html)

[Conditionals](#ch23s03.html_se-conditionals)

[Loops with {{#each}}](#ch23s03.html_se-loops-with-each)

[Binding element attributes](#ch23s03.html_se-binding-element-attributes)

[Links](#ch23s03.html_se-links)

[Custom Helpers](#ch23s04.html)

[Bronze Challenge: Adding Link Rollovers](#ch23s05.html)

[Silver Challenge: Changing the Date Format](#ch23s06.html)

[Gold Challenge: Creating a Custom Thumbnail Helper](#ch23s07.html)

[24\. Controllers](#ch24.html)

[New Sightings](#ch24.html_se-new-sightings)

[Editing a Sighting](#ch24s02.html)

[Deleting a Sighting](#ch24s03.html)

[Route Actions](#ch24s04.html)

[Bronze Challenge: Sighting Detail Page](#ch24s05.html)

[Silver Challenge: Sighting Date](#ch24s06.html)

[Gold Challenge: Adding and Removing Witnesses](#ch24s07.html)

[25\. Components](#ch25.html)

[Iterator Items as Components](#ch25.html_se-iterator-items-as-components)

[Components for DRY Code](#ch25s02.html)

[Data Down, Actions Up](#ch25s03.html)

[Class Name Bindings](#ch25s04.html)

[Data Down](#ch25s05.html)

[Actions Up](#ch25s06.html)

[Bronze Challenge: Customizing the Alert Message](#ch25s07.html)

[Silver Challenge: Making the NavBar a Component](#ch25s08.html)

[Gold Challenge: Array of Alerts](#ch25s09.html)

[26\. Afterword](#ch26.html)

[The Final Challenge](#ch26.html_idm494063307712)

[Shameless Plugs](#ch26s02.html)

[Thank You](#ch26s03.html)

[Index](#ix01.html)

# Introduction

## Learning Front-End Web Development

Doing front-end web development may require a shift in perspective, as it is a very different animal from development for other platforms. Here are a few things to keep in mind as you are learning.

<samp class="emphasis">The browser is a platform.</samp>

Perhaps you have done native development for iOS or Android; written server-side code in Ruby or PHP; or built desktop applications for OS X or Windows. As a front-end developer, your code will target the browser – a platform available on nearly every phone, tablet, and personal computer in the world.

<samp class="emphasis">Front-end development runs along a spectrum.</samp>

At one end of the spectrum is the look and feel of a web page: rounded corners, shadows, colors, fonts, whitespace, and so on. At the other end of the spectrum is the logic that governs the intricate behaviors of that web page: swapping images in an interactive photo gallery, validating data entered into a form, sending messages across a chat network, etc. You will need to become proficient with the core technologies all along this spectrum, and you will often need to use multiple technologies in synergy to create a good web application.

<samp class="emphasis">Web technologies are open.</samp>

There is no one company that controls how browsers should work. That means that front-end developers do not get a yearly SDK release that contains all the changes they will need to deal with for the next twelve months. Native platforms are a frozen pond on which you can comfortably skate. The web is a river; it curves, moves quickly, and is rocky in some places – but that is part of its appeal. The web is the most rapidly evolving platform available. Adapting to change is a way of life for a front-end developer.

This book’s purpose is to teach you how to develop for the browser. As you follow this guide, you will be taken through the process of building a series of projects. Each project will call for a different mixture of technologies along the front-end spectrum. Because of the sheer number of front-end tools, libraries, and frameworks available, this book will focus on the most essential and portable patterns and techniques.

## Prerequisites

This book is not an introduction to programming. It assumes you have experience with the fundamentals of writing code. You are expected to be familiar with basic types, functions, and objects.

That said, it also does not assume you already know JavaScript. It introduces you to JavaScript concepts in context, as you need them.

## How This Book Is Organized

This book walks you through writing four different web applications. Each application has its own section of the book. Each chapter in a section adds new features to the application you are building.

Doing the work of building these four applications takes you from one extreme of the front-end spectrum to the other.

| <samp class="emphasis">Ottergram</samp> |
| <samp class="emphasis">CoffeeRun</samp> |
| <samp class="emphasis">Chattrbox</samp> |
| <samp class="emphasis">Tracker</samp> |

As you work through these applications, you will be introduced to a number of tools, including:

*   the Atom text editor and some useful plug-ins for working with code

*   documentation resources like the Mozilla Developer Network

*   the command line, using the OS X <samp class="application">Terminal</samp> app or the Windows command prompt

*   browser-sync

*   Google Chrome’s Developer Tools

*   normalize.css

*   Bootstrap

*   jQuery and libraries like crypto-js and moment

*   Node.js, the Node package manager (npm), and nodemon

*   WebSockets and the wscat module

*   Babel, Babelify, Browserify, and Watchify

*   Ember.js and addons like Ember CLI, Ember Inspector, Ember CLI Mirage, and Handlebars

*   Bower

*   Homebrew

*   Watchman

## How to Use This Book

This book is not a reference book. Its goal is to get you over the initial hump to where you can get the most out of the reference and recipe books available. It is based on our five-day class at Big Nerd Ranch, and, as such, it is meant to be worked through from the beginning. Chapters build on each other, and skipping around would be unproductive.

In our classes, students work through these materials, but they also benefit from the right environment – a dedicated classroom, good food and comfortable board, a group of motivated peers, and an instructor to answer questions.

As a reader, you want your environment to be similar. That means getting a good night’s rest and finding a quiet place to work. These things can help, too:

*   Start a reading group with your friends or coworkers.

*   Arrange to have blocks of focused time to work on chapters.

*   Participate in the forum for this book at [<samp class="uri">forums.bignerdranch.com</samp>](http://forums.bignerdranch.com), where you can discuss the book and find errata and solutions.

*   Find someone who knows front-end web development to help you out.

## Challenges

Most chapters in this book end with at least one challenge. Challenges are opportunities to review what you have learned and take your work in the chapter one step further. We recommend that you tackle as many of them as you can to cement your knowledge and move from <samp class="emphasis">learning</samp> JavaScript development from us to <samp class="emphasis">doing</samp> JavaScript development on your own.

Challenges come in three levels of difficulty:

*   Bronze challenges typically ask you to do something very similar to what you did in the chapter. These challenges reinforce what you learned in the chapter and force you to type in similar code without having it laid out in front of you. Practice makes perfect.

*   Silver challenges require you to do more digging and more thinking. Sometimes you will need to use functions, events, markup, and styles that you have not seen before, but the tasks are still similar to what you did in the chapter.

*   Gold challenges are difficult and can take hours to complete. They require you to understand the concepts from the chapter and then do some quality thinking and problem solving on your own. Tackling these challenges will prepare you for the real-world work of JavaScript development.

You should make a copy of your code before you work on the challenges for any chapter. Otherwise, the changes that you make may not be compatible with subsequent exercises.

If you get lost, you can always visit [<samp class="uri">forums.bignerdranch.com</samp>](http://forums.bignerdranch.com) for some assistance.

## For the More Curious

Many chapters also have “For the More Curious” sections. These sections offer deeper explanations or additional information about topics presented in the chapter. The information in these sections is not absolutely essential, but we hope you will find it interesting and useful.

## Using an eBook

If you are reading this book on a eReader, reading the code may be tricky at times. Longer lines of code may wrap to a second line, depending on your selected font size.

The longest lines of code in this book are 86 monospace characters, like this one.

```
<link href="https://cdnjs.cloudflare.com/ajax/libs/normalize/3.0.3/normalize.min.css">
```

You can play with your eReader’s settings to find the best for viewing long code lines.

If you are reading on an iPad with iBooks, we recommend you go to the Settings app, select iBooks, and set <samp class="guilabel">Full Justification OFF</samp> and <samp class="guilabel">Auto-hyphenation OFF</samp>.

When you get to the point where you are actually typing in code, we suggest opening the book on your Mac (or PC) in Adobe Digital Editions. (Adobe Digital Editions is a free eReader application you can download from [<samp class="uri">www.adobe.com/​products/​digitaleditions</samp>](http://www.adobe.com/products/digitaleditions/).) Make the application window large enough so that you can see the code with no wrapping lines. You will also be able to see the figures in full detail.

# <samp class="part_number">Part I</samp>
<samp class="part_name">Core Browser Programming</samp>

# <samp class="chapter_number">1</samp>
<samp class="chapter_name">Setting Up Your Development Environment</samp>

There are countless tools and resources for front-end development, with more being built all the time. Choosing the best ones is challenging for developers of all skill levels. Throughout the projects in this book, we will guide you in the use of some of our favorites.

To get started, you will need three basic tools: a browser, a text editor, and good reference documentation for the many technologies used in front-end development. Also, there are several extras that – while not essential – will make your development experience smoother and more enjoyable.

For the purposes of this book we recommend that you use the same software we use to get the most benefit from our directions and screenshots. This chapter walks you through installing and configuring the <samp class="application">Google Chrome</samp> browser, the <samp class="application">Atom</samp> text editor, <samp class="application">Node.js</samp>, and a number of plug-ins and extras. You will also find out about good documentation options and get a crash course in using the <samp class="firstterm">command line</samp> on Mac and Windows. In the next chapter, you will put all these resources to use as you begin your first project.

## Installing Google Chrome

Your computer should already have a browser installed by default, but the best one to use for front-end development is <samp class="application">Google Chrome</samp>. If you do not already have the latest version of <samp class="application">Chrome</samp>, you can get it from [<samp class="uri">www.google.com/​chrome/​browser/​desktop</samp>](https://www.google.com/chrome/browser/desktop/) ([Figure 1.1](#ch01.html_fig-chrome-download-page "Figure 1.1  Downloading Google Chrome")).

**Figure 1.1  Downloading Google Chrome**

![Downloading Google Chrome](Setup/img/chrome-download-page.png)

## Installing and Configuring Atom

Of the many text editor programs out there, one of the best for front-end development is the <samp class="application">Atom</samp> editor by GitHub. It is a good choice because it is highly configurable, has many plug-ins to help with writing code, and is free to download and use.

You can download <samp class="application">Atom</samp> for Mac or Windows from [<samp class="uri">atom.io</samp>](https://atom.io) ([Figure 1.2](#ch01s02.html_fig-atom-download-page "Figure 1.2  Downloading Atom")).

**Figure 1.2  Downloading Atom**

![Downloading Atom](Setup/img/atom-download-page.png)

Follow the installation instructions for your platform. After <samp class="application">Atom</samp> is installed, there are several plug-ins you will want to install as well.

### Atom plug-ins

The primary things you want out of your text editor are documentation lookup, autocompletion, code formatting, and code linting (more on that in a bit). <samp class="application">Atom</samp> gives you some of these features by default, but installing a few plug-ins will make it even better.

Open <samp class="application">Atom</samp> and reveal its Settings screen. On a Mac, this is done by choosing <samp class="guimenu">Atom</samp> → <samp class="guimenuitem">Preferences...</samp> or using the keyboard shortcut Command-, (that is, the Command key plus the comma). On Windows, you can access it via <samp class="guimenu">File</samp> → <samp class="guimenuitem">Settings</samp> or using the keyboard shortcut Ctrl-,.

On the lefthand side of the Settings screen, click <samp class="guilabel">+ Install</samp> ([Figure 1.3](#ch01s02.html_fig-atom-settings-install "Figure 1.3  Atom’s Install Packages screen")).

**Figure 1.3  Atom’s Install Packages screen**

![Atom’s Install Packages screen](Setup/img/atom-settings-install.png)

Here, you can search for plug-in packages by name. Begin by searching for “emmet.”

Writing a lot of HTML can be very tedious and is error-prone. The <samp class="application">emmet</samp> plug-in ([Figure 1.4](#ch01s02.html_fig-emmet-install "Figure 1.4  Installing emmet")) lets you write well-formatted HTML using a convenient shorthand. Click the <samp class="guibutton">Install</samp> button to get <samp class="application">emmet</samp>.

**Figure 1.4  Installing emmet**

![Installing emmet](Setup/img/package-emmet.png)

Next, search for “atom-beautify.” The <samp class="application">atom-beautify</samp> plug-in ([Figure 1.5](#ch01s02.html_fig-beautify-install "Figure 1.5  Installing atom-beautify")) helps with the indentation of your code, which helps with readability. Again, click <samp class="guibutton">Install</samp> to get this plug-in.

**Figure 1.5  Installing atom-beautify**

![Installing atom-beautify](Setup/img/package-atom-beautify.png)

Search for and install the <samp class="application">autocomplete-paths</samp> plug-in ([Figure 1.6](#ch01s02.html_fig-autocomplete-install "Figure 1.6  Installing autocomplete-paths")). Very often, your code will need to refer to other files and folders in your project. This plug-in helps by offering filenames in an autocomplete menu as you type.

**Figure 1.6  Installing autocomplete-paths**

![Installing autocomplete-paths](Setup/img/package-autocomplete-paths.png)

Your next plug-in to install is the <samp class="application">api-docs</samp> package ([Figure 1.7](#ch01s02.html_fig-api-docs-install "Figure 1.7  Installing api-docs")), which lets you look up documentation based on keyword. It displays the documentation in a separate tab in the editor.

**Figure 1.7  Installing api-docs**

![Installing api-docs](Setup/img/package-api-docs.png)

Next, search for and install the <samp class="application">linter</samp> package ([Figure 1.8](#ch01s02.html_fig-linter-install "Figure 1.8  Installing linter")). A <samp class="firstterm">linter</samp> is a program that checks the syntax and style of your code. Make sure you find and install the package that is just named “linter.” This is a base linter that works with language-specific plug-ins. You will need it in order to use the other linter plug-ins below.

**Figure 1.8  Installing linter**

![Installing linter](Setup/img/package-linter.png)

There are three companions to <samp class="application">linter</samp> that you will want to install to check your CSS, HTML, and JavaScript code. Start with <samp class="application">linter-csslint</samp> ([Figure 1.9](#ch01s02.html_fig-linter-csslint-install "Figure 1.9  Installing linter-csslint")), which ensures that your CSS is syntactically correct and also offers suggestions about writing performant CSS.

**Figure 1.9  Installing linter-csslint**

![Installing linter-csslint](Setup/img/package-linter-css.png)

The next <samp class="application">linter</samp> companion plug-in to install is <samp class="application">linter-htmlhint</samp> ([Figure 1.10](#ch01s02.html_fig-linter-htmlhint-install "Figure 1.10  Installing linter-htmlhint")), which confirms that your HTML is well formed. It will warn you about mismatched HTML tags.

**Figure 1.10  Installing linter-htmlhint**

![Installing linter-htmlhint](Setup/img/package-linter-htmlhint.png)

The last <samp class="application">linter</samp> companion plug-in to install is <samp class="application">linter-eslint</samp> ([Figure 1.11](#ch01s02.html_fig-linter-eslint-install "Figure 1.11  Installing linter-eslint")). This plug-in checks the syntax of your JavaScript and can be configured to check the style and formatting of your code (for example, how many spaces lines are indented or how many blank lines come before and after comments).

**Figure 1.11  Installing linter-eslint**

![Installing linter-eslint](Setup/img/package-linter-eslint.png)

<samp class="application">Chrome</samp> and <samp class="application">Atom</samp> are now ready for front-end development. There are just a few more steps to completing your coding environment: accessing documentation, learning command-line basics, and downloading two final tools.

## Documentation and Reference Sources

Front-end development is different from programming for platforms like iOS and Android. Aside from the obvious differences, front-end technologies have no official developer documentation other than the technical specifications. This means that you will need to look elsewhere for guidance. We recommend that you familiarize yourself with the resources below and consult them regularly as you work through the book and continue on with front-end development.

The Mozilla Developer Network (MDN) is the best reference for anything to do with HTML, CSS, and JavaScript. One way to access it is [<samp class="uri">devdocs.io</samp>](http://devdocs.io), an excellent documentation interface ([Figure 1.12](#ch01s03.html_fig-devdocs-io "Figure 1.12  Accessing documentation via devdocs.io")). It pulls documentation from MDN for core front-end technologies – and it can work offline, so you can check it even when you do not have an internet connection.

**Figure 1.12  Accessing documentation via `devdocs.io`**

![Accessing documentation via devdocs.io](Setup/img/devdocs-io.png)

Note that <samp class="application">Safari</samp> currently does not support the offline caching mechanism used by [<samp class="uri">devdocs.io</samp>](http://devdocs.io). You will need to use a different browser, such as <samp class="application">Chrome</samp>, to access it.

You can also use MDN’s website, [<samp class="uri">developer.mozilla.org/​en-US</samp>](https://developer.mozilla.org/en-US/) ([Figure 1.13](#ch01s03.html_fig-mdn "Figure 1.13  The Mozilla Developer Network website")), or simply add “MDN” as a search engine keyword to find the information you need.

**Figure 1.13  The Mozilla Developer Network website**

![The Mozilla Developer Network website](Setup/img/mdn.png)

Another site to know about is [<samp class="uri">stackoverflow.com</samp>](http://stackoverflow.com) ([Figure 1.14](#ch01s03.html_fig-stackoverflow "Figure 1.14  The Stack Overflow website")). Officially, this is not a source of documentation. It is a place where developers can ask each other about code. The answers vary in quality, but are often very thorough and quite helpful. So it is a useful resource – as long as you bear in mind that the answers are not definitive, due to its crowdsourced nature.

**Figure 1.14  The Stack Overflow website**

![The Stack Overflow website](Setup/img/stackoverflow.png)

Web technologies are always changing. Support for features and APIs will vary from browser to browser and over time. Two websites that can help you determine which browsers (and which versions of individual browsers) support what features are [<samp class="uri">html5please.com</samp>](http://html5please.com) and [<samp class="uri">caniuse.com</samp>](http://caniuse.com). When you need information about feature support, we suggest starting with [<samp class="uri">html5please.com</samp>](http://html5please.com) to know whether a feature is recommended for use. For more detailed information about which browser versions support a specific feature, go to [<samp class="uri">caniuse.com</samp>](http://caniuse.com).

## Crash Course in the Command Line

Throughout this book, you will be instructed to use the <samp class="firstterm">command line</samp> or <samp class="firstterm">terminal</samp>. Many of the tools you will be using run exclusively as command-line programs.

To access the command line on a Mac, open <samp class="application">Finder</samp> and go to the <samp class="guilabel">Applications</samp> folder, then the <samp class="guilabel">Utilities</samp> folder. Find and open the program named <samp class="application">Terminal</samp> ([Figure 1.15](#ch01s04.html_fig-mac-finder-utilities-finder "Figure 1.15  Finding the Terminal app on a Mac")).

**Figure 1.15  Finding the Terminal app on a Mac**

![Finding the Terminal app on a Mac](Setup/img/mac-finder-utilities-finder.png)

You should see a window that looks like [Figure 1.16](#ch01s04.html_fig-mac-terminal "Figure 1.16  Mac command line").

**Figure 1.16  Mac command line**

![Mac command line](Setup/img/mac-terminal.png)

To access the command line on Windows, go to the Start menu and search for “cmd.” Find and open the program named <samp class="application">Command Prompt</samp> ([Figure 1.17](#ch01s04.html_fig-windows-cortana-cmd "Figure 1.17  Finding the Command Prompt program on Windows")).

**Figure 1.17  Finding the Command Prompt program on Windows**

![Finding the Command Prompt program on Windows](Setup/img/windows-cortana-cmd.png)

Click it to run the standard Windows command-line interface, which looks like [Figure 1.18](#ch01s04.html_fig-windows-cmd "Figure 1.18  Windows command line").

**Figure 1.18  Windows command line**

![Windows command line](Setup/img/windows-cmd.png)

From now on, we will refer to “the terminal” or “the command line” to mean both the Mac <samp class="application">Terminal</samp> and the Windows <samp class="application">Command Prompt</samp>. If you are unfamiliar with using the command line, here is a short walkthrough of some common tasks. All commands are entered by typing at the prompt and pressing the Return key.

### Finding out what directory you are in

The command line is location based. That means that at any given time it is “in” a particular directory within the file structure, and any commands you enter will be applied within that directory. The command-line prompt shows an abbreviated version of the directory it is in. To see the whole path on a Mac, enter the command `pwd` (which stands for “print working directory”), as in [Figure 1.19](#ch01s04.html_fig-mac-terminal-pwd "Figure 1.19  Showing the current path using pwd on a Mac").

**Figure 1.19  Showing the current path using `pwd` on a Mac**

![Showing the current path using pwd on a Mac](Setup/img/mac-terminal-pwd.png)

On Windows, use the command `echo %cd%` to see the path, as in [Figure 1.20](#ch01s04.html_fig-windows-echo-path "Figure 1.20  Showing the current path using echo %cd% on Windows").

**Figure 1.20  Showing the current path using `echo %cd%` on Windows**

![Showing the current path using echo %cd% on Windows](Setup/img/windows-echo-path.png)

### Creating a directory

The directory structure of front-end projects is important. Your projects can grow quickly, and it is best to keep them organized from the beginning. You will create new directories regularly during your development. This is done using the `mkdir` or “make directory” command followed by the name of the new directory.

To see this command in action, set up a directory for the projects you will build as you work through this book. Enter this command:

```
mkdir front-end-dev-book
```

Next, create a new directory for your first project, Ottergram, which you will begin in the next chapter. You want this new directory to be a subdirectory of the <samp class="filename">front-end-dev-book</samp> directory you just created. You can do this from your home directory by prefacing the new directory name with the name of the projects directory and, on a Mac, a slash:

```
mkdir front-end-dev-book/ottergram
```

On Windows, you use the backslash instead:

```
mkdir front-end-dev-book\ottergram
```

### Changing directories

To move around the file structure, you use the command `cd`, or “change directory,” followed by the path of the directory you want to move into.

You do not always need to use the complete directory path in your `cd` command. For example, to move down into any subdirectory of the directory you are in, you simply use the name of the subdirectory. So when you are in the <samp class="filename">front-end-dev-book</samp> directory, the path of the <samp class="filename">ottergram</samp> folder is just <samp class="filename">ottergram</samp>.

Move into your new project directory:

```
cd front-end-dev-book
```

Now, you can move into the <samp class="filename">ottergram</samp> directory:

```
cd ottergram
```

To move up to the parent directory, use the command `cd ..` (that is, `cd` followed by a space and two periods). The pair of periods represents the path of the parent directory.

```
cd ..
```

Remember that you can check your current directory by using the `pwd` command (or `echo %cd%` on Windows). [Figure 1.21](#ch01s04.html_fig-terminal-cli-tutorial "Figure 1.21  Changing and checking directories") shows the author creating directories, moving between them, and checking the current directory.

**Figure 1.21  Changing and checking directories**

![Changing and checking directories](Setup/img/terminal-cli-tutorial.png)

You are not limited to moving up or down one directory at a time. Let’s say that you had a more complex directory structure, like the one shown in [Figure 1.22](#ch01s04.html_fig-path-diagram "Figure 1.22  An example file structure").

**Figure 1.22  An example file structure**

![An example file structure](Setup/img/finder-folder-structure.png)

Suppose you are in the <samp class="filename">ottergram</samp> directory and you want to go directly to the <samp class="filename">stylesheets</samp> directory inside of <samp class="filename">coffeerun</samp>. You would do this with `cd` followed by a path that means “the <samp class="filename">stylesheets</samp> directory inside the <samp class="filename">coffeerun</samp> directory inside the parent directory of where I am now”:

```
cd ../coffeerun/stylesheets
```

On Windows, you would use the same command but with backslashes:

```
cd ..\coffeerun\stylesheets
```

### Listing files in a directory

You may need to see a list of files in your current directory. On a Mac, you use the `ls` command for that ([Figure 1.23](#ch01s04.html_fig-terminal-ls "Figure 1.23  Using ls to list files in a directory")). If you want to list the files in another directory, you can supply a path:

```
ls
ls ottergram
```

**Figure 1.23  Using `ls` to list files in a directory**

![Using ls to list files in a directory](Setup/img/terminal-ls.png)

By default, `ls` will not print anything if a directory is empty.

On Windows, the command is `dir` ([Figure 1.24](#ch01s04.html_fig-windows-dir "Figure 1.24  Using dir to list files in a directory")), which you can optionally give a path:

```
dir
dir ottergram
```

**Figure 1.24  Using `dir` to list files in a directory**

![Using dir to list files in a directory](Setup/img/windows-dir.png)

By default, the `dir` command will print information about dates, times, and file sizes.

### Getting administrator privileges

On some versions of OS X and Windows, you will need <samp class="firstterm">superuser</samp> or administrator privileges in order to run some commands, such as commands that install software or make changes to protected files.

On a Mac, you can give yourself privileges by prefixing a command with `sudo`. The first time you use `sudo` on a Mac, it will give you a stern warning, shown in [Figure 1.25](#ch01s04.html_fig-sudo-warning "Figure 1.25  sudo warning").

**Figure 1.25  `sudo` warning**

![sudo warning](Setup/img/sudo-warning.png)

`sudo` will prompt you for your password before it runs the command as the superuser. As you type, your keystrokes will not be echoed back, so type carefully.

On Windows, if you need to give yourself privileges you do so in the process of opening the command-line interface. Find the command prompt in the Windows <samp class="guimenu">Start Menu</samp>, right-click it, and choose <samp class="guilabel">Run as Administrator</samp> ([Figure 1.26](#ch01s04.html_fig-windows-cmd-as-administrator "Figure 1.26  Opening the command prompt as an administrator")). Any commands you run in this command prompt will be run as the superuser, so be careful.

**Figure 1.26  Opening the command prompt as an administrator**

![Opening the command prompt as an administrator](Setup/img/windows-cmd-as-administrator.png)

### Quitting a program

As you proceed through the book, you will run many apps from the command line. Some of them will do their job and quit automatically, but others will run until you stop them. To quit a command-line program, press Control-C.

## Installing Node.js and browser-sync

There is one final set-up step before you begin your first project.

<samp class="application">Node.js</samp> (or simply “<samp class="application">Node</samp>”) lets you use programs written in JavaScript from the command line. Most front-end development tools are written for use with <samp class="application">Node.js</samp>. You will learn lots more about <samp class="application">Node.js</samp> in [Chapter 15](#ch15.html "15 Introduction to Node.js"), but you will begin using one tool that depends on it, `browser-sync`, right away.

Install <samp class="application">Node</samp> by downloading the installer from [<samp class="uri">nodejs.org</samp>](https://nodejs.org/en/) ([Figure 1.27](#ch01s05.html_fig-nodejs-download-site "Figure 1.27  Downloading Node.js")). The version of <samp class="application">Node.js</samp> used in this book is 5.11.1, and you will likely see a different version available for download.

**Figure 1.27  Downloading Node.js**

![Downloading Node.js](Setup/img/nodejs-download-site.png)

Double-click the installer and follow the prompts.

When you install <samp class="application">Node</samp>, it provides two command-line programs: `node` and `npm`. The `node` program does the work of running programs written in JavaScript. You will not need to use it until [Chapter 15](#ch15.html "15 Introduction to Node.js"). The other program is the <samp class="application">Node</samp> package manager, `npm`, which is needed for installing open-source development tools from the internet.

`browser-sync` is one such tool, and it will be invaluable to you throughout the book. It makes your example code easier to run in the browser and automatically reloads the browser when you save changes to your code.

Install `browser-sync` using this command at the command line:

```
npm install -g browser-sync
```

(The `-g` in the command stands for “global.” Installing the package globally means that you will be able to run `browser-sync` from any directory.)

It does not matter what directory you are in when you run this command, but you will probably need superuser privileges. If that is the case, run the command using `sudo` on a Mac:

```
sudo npm install -g browser-sync
```

If you are on Windows, first open a command prompt as the administrator, as shown above.

When you start `browser-sync`, as you will in the next chapter, it will run until you press Control-C. It is a good idea to quit `browser-sync` when you are done working on a project for a while. That means that you will need to start `browser-sync` each time you begin work on the first two projects in this book (Ottergram and CoffeeRun).

With that, you have the tools you need to get started on your Ottergram project!

## For the More Curious: Alternatives to Atom

There are many, many text editors to choose from. If you are not that keen on <samp class="application">Atom</samp>, when you are done working through the projects in this book you may want to try out one of the following two options. Both are available for free for Mac and Windows, and both have a large number of plug-ins to customize your development experience. Also, like <samp class="application">Atom</samp>, both are built using HTML, CSS, and JavaScript, but run as desktop applications.

<samp class="application">Visual Studio Code</samp> is Microsoft’s open source text editor, made specifically for developing web applications. It can be downloaded from [<samp class="uri">code.visualstudio.com</samp>](https://code.visualstudio.com/) ([Figure 1.28](#ch01s06.html_fig-vs-code "Figure 1.28  The Visual Studio Code website")).

**Figure 1.28  The Visual Studio Code website**

![The Visual Studio Code website](Setup/img/vs-code.png)

Adobe’s <samp class="application">Brackets</samp> text editor is particularly good for building user interfaces with HTML and CSS. In fact, it provides an extension for helping you work with Adobe’s layered PSD image files. <samp class="application">Brackets</samp> is available from [<samp class="uri">brackets.io</samp>](http://brackets.io/) ([Figure 1.29](#ch01s06.html_fig-brackets-io "Figure 1.29  The Adobe Brackets website")).

**Figure 1.29  The Adobe Brackets website**

![The Adobe Brackets website](Setup/img/brackets-io.png)

# <samp class="chapter_number">2</samp>
<samp class="chapter_name">Setting Up Your First Project</samp>

When you visit a website, your browser has a conversation with a server, another computer on the internet.

Browser: “Hey there! Can I please have the contents of the file named <samp class="filename">cat-videos.html</samp>?”

Server: “Certainly. Let me take a look around … here it is!”

Browser: “Ah, it’s telling me that I need another file named <samp class="filename">styles.css</samp>.”

Server: “Sure thing. Let me take a look around … here it is!”

Browser: “OK, that file says that I need another file named <samp class="filename">animated-background.gif</samp>.”

Server: “No problem. Let me take a look around … here it is!”

That conversation goes on for some time, sometimes lasting thousands of milliseconds ([Figure 2.1](#ch02.html_fig-request-response "Figure 2.1  The browser sends a request, the server responds")).

**Figure 2.1  The browser sends a request, the server responds**

![The browser sends a request, the server responds](Ottergram/Foundation/img/request-response.png)

It is the browser’s job to send requests to the server; interpret the HTML, CSS, and JavaScript it receives in the response from the server; and present the result to the user. Each of these three technologies plays a part in the user’s experience of a website. If your app were a living creature, the HTML would be its skeleton and organs (the mechanics), the CSS would be its skin (the visible layer), and the JavaScript would be its personality (how it behaves).

In this chapter, you are going to set up the basic HTML for your first project, Ottergram. In the next chapter, you will set up your CSS, which you will refine in [Chapter 4](#ch04.html "4 Responsive Layouts with Flexbox"). In [Chapter 6](#ch06.html "6 Handling Events with JavaScript"), you will begin adding JavaScript.

## Setting Up Ottergram

In [Chapter 1](#ch01.html "1 Setting Up Your Development Environment"), you created a folder for the projects in this book as well as a folder for Ottergram. Start your <samp class="application">Atom</samp> text editor and open the <samp class="filename">ottergram</samp> folder by clicking <samp class="guimenu">File</samp> → <samp class="guimenuitem">Open</samp> (or <samp class="guimenu">File</samp> → <samp class="guimenuitem">Open Folder...</samp> on Windows). In the dialog box, navigate to the <samp class="filename">front-end-dev-book</samp> folder and choose the <samp class="filename">ottergram</samp> folder. Click <samp class="guibutton">Open</samp> to tell <samp class="application">Atom</samp> to use this folder ([Figure 2.2](#ch02.html_fig-atom-file-open-dialog "Figure 2.2  Opening your project folder in Atom")).

**Figure 2.2  Opening your project folder in Atom**

![Opening your project folder in Atom](Ottergram/Foundation/img/atom-file-open-dialog.png)

You will see the <samp class="filename">ottergram</samp> folder in the lefthand panel of <samp class="application">Atom</samp>. This panel is for navigating among the files and folders in your project.

You are going to create some files and folders within the <samp class="filename">ottergram</samp> project folder using <samp class="application">Atom</samp>. Control-click (right-click) <samp class="filename">ottergram</samp> in the lefthand panel and click <samp class="guimenuitem">New File</samp> in the pop-up menu. You will be prompted for a name for the new file. Enter <samp class="filename">index.html</samp> and press the Return key ([Figure 2.3](#ch02.html_fig-new-file-prompt "Figure 2.3  Creating a new file in Atom")).

**Figure 2.3  Creating a new file in Atom**

![Creating a new file in Atom](Ottergram/Foundation/img/new-file-prompt.png)

You can use the same process to create folders using <samp class="application">Atom</samp>. Control-click (right-click) <samp class="filename">ottergram</samp> in the lefthand panel again, but this time click <samp class="guimenuitem">New Folder</samp> in the pop-up. Enter the name <samp class="filename">stylesheets</samp> in the prompt that appears ([Figure 2.4](#ch02.html_fig-new-folder-prompt "Figure 2.4  Creating a new folder in Atom")).

**Figure 2.4  Creating a new folder in Atom**

![Creating a new folder in Atom](Ottergram/Foundation/img/new-folder-prompt.png)

Finally, create a file named <samp class="filename">styles.css</samp> in the <samp class="filename">stylesheets</samp> folder: Control-click (right-click) <samp class="filename">stylesheets</samp> in the lefthand panel and choose <samp class="guimenuitem">New File</samp>. The prompt will pre-fill the text “stylesheets/”. After this, enter <samp class="filename">styles.css</samp> and press the Return key ([Figure 2.5](#ch02.html_fig-new-css-file-prompt "Figure 2.5  Creating a new CSS file in Atom")).

**Figure 2.5  Creating a new CSS file in Atom**

![Creating a new CSS file in Atom](Ottergram/Foundation/img/new-css-file-prompt.png)

When you are finished, your project folder should look like [Figure 2.6](#ch02.html_fig-project-folder "Figure 2.6  Initial files and folders for Ottergram").

**Figure 2.6  Initial files and folders for Ottergram**

![Initial files and folders for Ottergram](Ottergram/Foundation/img/initial-folder-setup.png)

There are no rules about how to structure your files and folders or what to name them. However, Ottergram (like the other projects in this book) follows conventions used by many front-end developers. Your <samp class="filename">index.html</samp> file will hold your HTML code. Naming the main HTML file <samp class="filename">index.html</samp> dates back to the early days of the web, and the convention continues today.

The <samp class="filename">stylesheets</samp> folder, as the name suggests, will hold one or more files with styling information for Ottergram. These will be CSS, or “cascading style sheets,” files. Sometimes developers give their CSS files names that describe what part of the page or site they pertain to, such as <samp class="filename">header.css</samp> or <samp class="filename">blog.css</samp>. Ottergram is a simple project and only needs one CSS file, so you have named it <samp class="filename">styles.css</samp> to reflect its global role.

### Initial HTML

Time to get coding. Open <samp class="filename">index.html</samp> in <samp class="application">Atom</samp> and add some basic HTML to get started.

Start by typing `html`. <samp class="application">Atom</samp> will offer you an autocomplete option, as shown in [Figure 2.7](#ch02.html_fig-html-autocomplete "Figure 2.7  Atom’s autocomplete menu"). (If it does not, make sure you installed the <samp class="application">emmet</samp> plug-in as directed in [Chapter 1](#ch01.html "1 Setting Up Your Development Environment").)

**Figure 2.7  Atom’s autocomplete menu**

![Atom’s autocomplete menu](Ottergram/Foundation/img/html-autocomplete.png)

Press the Return key, and <samp class="application">Atom</samp> will provide bare-bones HTML elements to get you started ([Figure 2.8](#ch02.html_fig-html5-doc "Figure 2.8  HTML created using autocomplete")).

**Figure 2.8  HTML created using autocomplete**

![HTML created using autocomplete](Ottergram/Foundation/img/html5-doc.png)

Your cursor is between `<title>` and `</title>` – the opening and closing `title` tags. Type “ottergram” to give the project a name. Now, click to put your cursor in the blank line between the opening and closing `body` tags. There, type “header” and press the Return key. <samp class="application">Atom</samp> will convert the text “header” into opening and closing `header` tags with a blank line between them ([Figure 2.9](#ch02.html_fig-header-autocomplete "Figure 2.9  Header tag created with autocomplete")).

**Figure 2.9  Header tag created with autocomplete**

![Header tag created with autocomplete](Ottergram/Foundation/img/header-autocomplete.png)

Next, type “h1” and press Return. Again, your text is converted into tags, this time without a blank line. Enter the text “ottergram” again. This will be the heading that will appear on your web page.

Your file should look like this:

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>ottergram</title>
  </head>
  <body>
    <header>
      <h1>ottergram</h1>
    </header>
  </body>
</html>
```

<samp class="application">Atom</samp> and <samp class="application">emmet</samp> have together saved you some typing and helped you build well-formed initial HTML.

Let’s examine your code. The first line, `<!doctype html>`, defines the <samp class="firstterm">doctype</samp> – it tells the browser which version of HTML the document is written in. The browser may render, or draw, the page a little differently based the doctype. Here, the doctype specifies HTML5.

Earlier versions of HTML often had long, convoluted, and hard to remember doctypes, such as:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

Often, folks had to look up the doctype each time they created a new document.

With HTML5, the doctype is short and sweet. It is the one that will be used throughout all of the projects in this book, and you should use it for your apps.

After the doctype is some basic HTML markup consisting of a `head` and a `body`.

The `head` will hold information about the document and how the browser should handle the document. For example, the title of the document, what CSS or JavaScript files the page uses, and when the document was last modified are all included in the `head`.

Here, the `head` contains a `<meta>` tag. `<meta>` tags provide the browser with information about the document itself, such as the name of the document’s author or keywords for search engines. The `<meta>` tag in Ottergram, `<meta charset="utf-8">`, specifies that the document is encoded using the UTF-8 character set, which encompasses all Unicode characters. Use this tag in your documents so that the widest range of browsers can interpret them correctly, especially if you expect international traffic.

The `body` will hold all of the HTML code that represents the content of your page: all the images, links, text, buttons, and videos that will appear on the page.

Most tags enclose some other content. Take a look at the `h1` heading you included; its anatomy is shown in [Figure 2.10](#ch02.html_fig-tag-anatomy "Figure 2.10  Anatomy of a simple HTML tag").

**Figure 2.10  Anatomy of a simple HTML tag**

![Anatomy of a simple HTML tag](Ottergram/Foundation/img/anatomy-of-a-tag.png)

HTML stands for “hypertext markup language.” Tags are used to “mark up” your content, designating their purpose – such as headings, list items, and links.

The content enclosed by a set of tags can also include other HTML. Notice, for example, that the `<header>` tags enclose the `<h1>` tag shown above (and the `<body>` tags enclose the `<header>`!).

There are a lot of tags to choose from – more than 140\. To see a list of them, visit MDN’s HTML element reference, located at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​HTML/​Element</samp>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element). This reference includes a brief description of each element and groups elements by usage (e.g., text content, content sectioning, or multimedia).

### Linking a stylesheet

In [Chapter 3](#ch03.html "3 Styles"), you will write styling rules in your stylesheet, <samp class="filename">styles.css</samp>. But remember the conversation between the browser and the server at the beginning of this chapter? The browser only knows to ask for a file from the server if it has been told that the file exists. You have to <samp class="firstterm">link</samp> to your stylesheet so that the browser knows to ask for it. Update the `head` of `index.html` with a link to your <samp class="filename">styles.css</samp> file.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>ottergram</title>
    <link rel="stylesheet" href="stylesheets/styles.css">
  </head>
  <body>
...
```

The `<link>` tag is how you attach an external stylesheet to an HTML document. It has two <samp class="firstterm">attributes</samp>, which give the browser more information about the tag’s purpose ([Figure 2.11](#ch02.html_fig-anatomy-tag-attribute "Figure 2.11  Anatomy of a tag with attributes")). (The order of HTML attributes does not matter.)

**Figure 2.11  Anatomy of a tag with attributes**

![Anatomy of a tag with attributes](Ottergram/Foundation/img/anatomy-tag-attribute.png)

You set the `rel` (or “relationship”) attribute to `"stylesheet"`, which lets the browser know that the linked document provides styling information. The `href` attribute tells the browser to send a request to the server for the `styles.css` file located in the `stylesheets` folder. Note that this file path is <samp class="emphasis">relative</samp> to the current document.

Save <samp class="filename">index.html</samp> before you move on.

### Adding content

A web page without content is like a day without coffee. Add a list after your `header` to give your project a reason for living.

You are going to add an <samp class="firstterm">unordered list</samp> (that is, a bulleted list) using the `<ul>` tag. In the list, you will include five list items using `<li>` tags, and in each list item you will include some text surrounded by `<span>` tags.

The updated <samp class="filename">index.html</samp> is shown below. Note that throughout this book we show new code that you are adding in bold type. Code that you are to delete is shown struck through. Existing code is shown in plain text to help you position your changes within the file.

We encourage you to make use of <samp class="application">Atom</samp>’s autocompletion and autoformatting features. With your cursor in position, type “ul” and press Return. Next, type “li” and press Return twice, then type “span” and press Return once. Enter the name of an otter, then create four more list items and spans in the same way.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>ottergram</title>
    <link rel="stylesheet" href="stylesheets/styles.css">
  </head>
  <body>
    <header>
      <h1>ottergram</h1>
    </header>
    <ul>
      <li>
        <span>Barry</span>
      </li>
      <li>
        <span>Robin</span>
      </li>
      <li>
        <span>Maurice</span>
      </li>
      <li>
        <span>Lesley</span>
      </li>
      <li>
        <span>Barbara</span>
      </li>
    </ul>
  </body>
</html>
```

The `<span>` tags nested inside each `<li>` tag do not have any special meaning. They are generic containers for other content. You will be using them in Ottergram for styling purposes, and you will see other examples of container elements as you continue through this book.

Next, you will add images of otters to go with the names you have entered.

### Adding images

The resource files for all the projects in this book are at [<samp class="uri">www.bignerdranch.com/​downloads/​front-end-dev-resources.zip</samp>](http://www.bignerdranch.com/downloads/front-end-dev-resources.zip). They include five Creative Commons-licensed otter images taken by Michael L. Baird, Joe Robertson, and Agunther that were found on [<samp class="uri">commons.wikimedia.org</samp>](https://commons.wikimedia.org).

Download and unzip the resources. Inside the <samp class="filename">ottergram-resources</samp> folder, locate the <samp class="filename">img</samp> folder. Copy the <samp class="filename">img</samp> folder to your <samp class="filename">ottergram/</samp> project directory. (The .zip contains other resources, but for now you will only need the <samp class="filename">img</samp> folder.)

You want your list to include clickable thumbnail images in addition to the titles. You will achieve this by adding anchor and image tags to each item in your `ul`. We will explain these changes in more detail after you enter them. (If you use autocompletion, note that you will need to move the `</a>` tags so that they follow the `span`s.)

```
...
    <ul>
      <li>
        <a href="#">
          <img src="img/otter1.jpg" alt="Barry the Otter">
          <span>Barry</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter2.jpg" alt="Robin the Otter">
          <span>Robin</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter3.jpg" alt="Maurice the Otter">
          <span>Maurice</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter4.jpg" alt="Lesley the Otter">
          <span>Lesley</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter5.jpg" alt="Barbara the Otter">
          <span>Barbara</span>
        </a>
      </li>
    </ul>
...
```

If your lines are not nicely indented, you can take advantage of the <samp class="application">atom-beautify</samp> plug-in that you installed. Click <samp class="guimenu">Packages</samp> → <samp class="guisubmenu">Atom Beautify</samp> → <samp class="guimenuitem">Beautify</samp> and your code will be aligned and indented for you.

Let’s look at what you have added.

The `<a>` tag is the <samp class="firstterm">anchor</samp> tag. Anchor tags make elements on the page clickable, so that they take the user to another page. They are commonly referred to as “links,” but beware: They are not like the `<link>` tag you used earlier.

Anchor tags have an `href` attribute, which indicates the resource the anchor points to. Usually the value is a web address. Sometimes, though, you do not want a link to go anywhere. That is the case for now, so you assigned the “dummy” value `#` to the `href` attributes. This will make the browser scroll to the top of the page when the image is clicked. Later you will use the anchor tags to open a larger copy of an image when the thumbnail is clicked.

Inside the anchor tags you added `<img>`, or <samp class="firstterm">image</samp>, tags with `src` attributes indicating filenames in the <samp class="filename">img</samp> directory you added earlier. You also added a descriptive `alt` attribute to your image tags. `alt` attributes contain text that replaces the image if it is unable to load. `alt` text is also what screen readers use to describe an image to a user with a visual impairment.

Image tags are different from most other elements in that they do not wrap other elements, but instead refer to a resource. When the browser encounters an `<img>` tag, it draws the image to the page. This is known as a <samp class="firstterm">replaced element</samp>. Other replaced elements include embedded documents and applets.

Because they do not wrap content or other elements, `<img>` tags do not have a corresponding closing tag. This makes them <samp class="firstterm">self-closing</samp> tags (also known as <samp class="firstterm">void</samp> tags). You will sometimes see self-closing tags written with a slash before the right angle-bracket, like `<img src="otter.jpg"/>`. Whether to include the slash is a matter of preference and does not make a difference to the browser. In this book, self-closing tags are written without the slash.

Save <samp class="filename">index.html</samp>. In a moment, you will see the results of your coding.

## Viewing the Web Page in the Browser

To view your web page, you need to be running the `browser-sync` tool that you installed in [Chapter 1](#ch01.html "1 Setting Up Your Development Environment").

Open the terminal and change directory to your <samp class="filename">ottergram</samp> folder. Recall from [Chapter 1](#ch01.html "1 Setting Up Your Development Environment") that you change directory using the `cd` command followed by the path of the folder you are moving into. One easy way to get the <samp class="filename">ottergram</samp> path is to Control-click (right-click) the <samp class="filename">ottergram</samp> folder in <samp class="application">Atom</samp>’s lefthand panel and choose <samp class="guimenuitem">Copy Full Path</samp> ([Figure 2.12](#ch02s02.html_fig-copy-full-path "Figure 2.12  Copying the ottergram folder path from Atom")). Then, at the command line, type `cd`, paste the path, and press Return.

**Figure 2.12  Copying the `ottergram` folder path from Atom**

![Copying the ottergram folder path from Atom](Ottergram/Foundation/img/copy-full-path.png)

The path you enter might look something like this:

```
cd /Users/chrisaquino/Projects/front-end-dev-book/ottergram
```

Once you are in the <samp class="filename">ottergram</samp> directory, run the following command to open Ottergram in <samp class="application">Chrome</samp>. (We have broken the command across two lines so that it fits on the page. You should enter it on a single line.)

```
browser-sync start --server --browser "Google Chrome"
                   --files "stylesheets/*.css, *.html"
```

If <samp class="application">Chrome</samp> is your default browser, you can leave out the `--browser "Google Chrome"` portion of the command:

```
browser-sync start --server --files "stylesheets/*.css, *.html"
```

This command starts `browser-sync` in server mode, allowing it to send responses when a browser sends a request to get a file, such as the <samp class="filename">index.html</samp> file you created.

The command you entered also tells `browser-sync` to automatically reload the browser if any HTML or CSS files are changed. This makes the development experience much nicer. Before tools like `browser-sync`, you had to manually reload the page after every change.

[Figure 2.13](#ch02s02.html_fig-mac-browser-sync "Figure 2.13  Starting browser-sync in the OS X Terminal") shows the result of entering this command on a Mac.

**Figure 2.13  Starting browser-sync in the OS X Terminal**

![Starting browser-sync in the OS X Terminal](Ottergram/Foundation/img/cd-ottergram-browsersync-mac.png)

You should see the same output on Windows ([Figure 2.14](#ch02s02.html_fig-pc-output "Figure 2.14  Starting browser-sync in the Windows Command Prompt")).

**Figure 2.14  Starting browser-sync in the Windows Command Prompt**

![Starting browser-sync in the Windows Command Prompt](Ottergram/Foundation/img/cd-ottergram-browsersync-win.png)

Once the Ottergram page has loaded in <samp class="application">Chrome</samp>, you should see your page with the “ottergram” heading, “ottergram” as the tab label, and a series of otter photos and names ([Figure 2.15](#ch02s02.html_fig-barebones-otters "Figure 2.15  Viewing Ottergram in the browser")).

**Figure 2.15  Viewing Ottergram in the browser**

![Viewing Ottergram in the browser](Ottergram/Foundation/img/barebones-otters.png)

## The Chrome Developer Tools

<samp class="application">Chrome</samp> has built-in Developer Tools (commonly known as “DevTools”) that are among the best available for testing styles, layouts, and more on the fly. Using the DevTools is much more efficient than trying things out in code. The DevTools are very powerful and will be your constant companion as you do front-end development.

You will start using the DevTools in the next chapter. For now, open the window and familiarize yourself with its major areas.

To open the DevTools, click the ![The Chrome Developer Tools](Ottergram/Foundation/img/hamburger.png) icon to the right of the address bar in <samp class="application">Chrome</samp>. Next, click <samp class="guimenu">More Tools</samp> → <samp class="guimenuitem">Developer Tools</samp> ([Figure 2.16](#ch02s03.html_fig-open-devtool "Figure 2.16  Opening the Developer Tools")).

**Figure 2.16  Opening the Developer Tools**

![Opening the Developer Tools](Ottergram/Foundation/img/opening-the-dev-tools.png)

<samp class="application">Chrome</samp> displays the DevTools to the right by default. Your screen will look something like [Figure 2.17](#ch02s03.html_fig-devtool-intro "Figure 2.17  The DevTools showing the elements panel").

**Figure 2.17  The DevTools showing the elements panel**

![The DevTools showing the elements panel](Ottergram/Foundation/img/labeled-dev-tools.png)

The DevTools show the relationship between the code and the resulting page elements. They let you inspect individual elements’ attributes and styles and see immediately how the browser is interpreting your code. Seeing this relationship is critical for both development and debugging.

In [Figure 2.17](#ch02s03.html_fig-devtool-intro "Figure 2.17  The DevTools showing the elements panel"), you can see the DevTools next to the web page, displaying the elements panel. The elements panel is divided into two sections. On the left is the <samp class="firstterm">DOM tree view</samp>. This is a representation of the HTML, interpreted as DOM elements. (You will learn much more about DOM, which stands for “document object model,” in upcoming chapters.) On the righthand side of the elements panel is the styles pane. This shows any visual styles applied to individual elements.

Having the DevTools docked on the right side of the screen while you are working is usually convenient. If you want to change the location of the DevTools, you can click the ![The DevTools showing the elements panel](Ottergram/Foundation/img/devtools-config-button.png) button near the upper-right corner. This will show you a menu of options, including buttons for the <samp class="guilabel">Dock side</samp>, which will change the anchor location of the DevTools ([Figure 2.18](#ch02s03.html_fig-devtool-dock-side "Figure 2.18  Changing the dock side of the DevTools")).

**Figure 2.18  Changing the dock side of the DevTools**

![Changing the dock side of the DevTools](Ottergram/Foundation/img/toggle-dock-side.png)

With your otters and markup in place and the DevTools open, you are ready to begin styling your project in the next chapter.

## For the More Curious: CSS Versions

The version history of CSS includes standard versions 1, 2, and 2.1\. After 2.1, it was decided that the standard needed to be broken up because it was getting too big.

There is no version 3\. Instead, CSS3 is a blanket term for a number of modules, each with its own version number.

**Table 2.1  CSS versions, real and imagined**

| Version Number | Release Year | Notable Features |
| --- | --- | --- |
| 1 | 1996 | Basic font properties (`font-family`, `font-style`), foreground and background colors, text alignment, margin, border, and padding. |
| 2 | 1998 | Absolute, relative, and fixed positioning; new font properties. |
| 2.1 | 2011 | Removed features that were poorly supported by browsers. |
| “3” | Various | A collection of different specifications, such as media queries, new selectors, semi-transparent colors, `@font-face`. |

## For the More Curious: The favicon.ico

Have you ever noticed the little icon that appears at the left end of your browser’s address bar when you visit most websites? Sometimes they also appear in your browser tab, as in [Figure 2.19](#ch02s05.html_fig-bnr-favicon "Figure 2.19  The bignerdranch.com favicon.ico").

**Figure 2.19  The `bignerdranch.com` `favicon.ico`**

![The bignerdranch.com favicon.ico](Ottergram/Foundation/img/bnr-favicon.png)

That is the `favicon.ico` image file. Many sites have one, and browsers request one by default. Because Ottergram does not have one, you may see an error like the one in [Figure 2.20](#ch02s05.html_fig-favicon-error "Figure 2.20  Error about missing favicon.ico") in the DevTools.

**Figure 2.20  Error about missing `favicon.ico`**

![Error about missing favicon.ico](Ottergram/Foundation/img/favicon-warning.png)

Do not worry about this error if it appears. It will not affect your project. However, you can easily add a `favicon.ico` image – and that is your first challenge.

## Silver Challenge: Adding a favicon.ico

You have decided that you like otters more than you like seeing the `favicon.ico` error message. You are going to create a <samp class="filename">favicon.ico</samp> file using one of the otter images.

Do a web search for “favicon generator” and you should see a list of websites that will do a file conversion for you. Most will let you upload an image and then provide you with a <samp class="filename">favicon.ico</samp> version.

Choose one and upload any one of the otter images.

Save the resulting <samp class="filename">favicon.ico</samp> file in the same folder as your <samp class="filename">index.html</samp> file. Finally, reload your browser. Your browser tab will look something like [Figure 2.21](#ch02s06.html_fig-ottergram-favicon "Figure 2.21  Ottergram with a favicon.ico").

**Figure 2.21  Ottergram with a `favicon.ico`**

![Ottergram with a favicon.ico](Ottergram/Foundation/img/ottergram-favicon.png)

# <samp class="chapter_number">3</samp>
<samp class="chapter_name">Styles</samp>

In this chapter, you will design a static version of Ottergram. In the chapters that follow, you will make Ottergram interactive.

When you reach the end of this chapter, your website will look like [Figure 3.1](#ch03.html_fig-end-of-chapter "Figure 3.1  Ottergram: stylish").

**Figure 3.1  Ottergram: stylish**

![Ottergram: stylish](Ottergram/Styles/img/oh-yeah-header.png)

This chapter introduces a number of concepts and examples. Do not worry if you do not feel that you have mastered all of them when you get to the end. You will be encountering them again and again as you progress through this book, and your work in this chapter will provide a solid foundation on which you will build true understanding.

Of course, we can only introduce you to a tiny fraction of all the styles that are available in CSS. You will want to consult the MDN for information about the full set of properties and their values.

Front-end developers have to choose between two approaches to styling a website: start with the overall layout and work down to the smallest details, or start with the smallest details and work up to the overall layout.

Not only does working from detail to big picture produce cleaner, more reusable code, it also has a cool name: <samp class="firstterm">atomic styling</samp>. You will use this approach as you style the otter thumbnails first, then the thumbnail list layout. In the next chapter, you will work on the layout of the site as a whole.

## Creating a Styling Baseline

You are going to begin by adding the <samp class="filename">normalize.css</samp> file to your project. <samp class="filename">normalize.css</samp> helps the CSS you write display consistently across browsers. All browsers come with a set of default styles, but the defaults are different from browser to browser. <samp class="filename">normalize.css</samp> gives you a good starting point for developing your own custom CSS for a website or web app.

<samp class="filename">normalize.css</samp> is freely available online. You do not need to download it. To add it to Ottergram, you only need to link to it in <samp class="filename">index.html</samp>.

To ensure that you are using the most current version of <samp class="filename">normalize.css</samp>, you are going to get its address from a content sharing site. Go to [<samp class="uri">cdnjs.com/​libraries/​normalize</samp>](http://cdnjs.com/libraries/normalize/) and find the version of the file ending with `.min.css`. (This version is a smaller download than the others, with the extra whitespace stripped out.) Click the <samp class="guibutton">Copy</samp> button to copy its address ([Figure 3.2](#ch03.html_fig-normalize-address "Figure 3.2  Getting a link to normalize.css from cdnjs.com")).

**Figure 3.2  Getting a link to `normalize.css` from `cdnjs.com`**

![Getting a link to normalize.css from cdnjs.com](Ottergram/Styles/img/normalize-cdn.png)

The current version at the time of this writing is 3.0.3, but the version you use may be more recent.

Open your Ottergram folder in <samp class="application">Atom</samp>, then open <samp class="filename">index.html</samp>. Add a new `<link>` tag and paste in the address. (In the code below, the `<link>` has been broken into two lines to fit on the page. You can leave yours on a single line.)

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>ottergram</title>
    <link rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/normalize/3.0.3/normalize.min.css">
    <link rel="stylesheet" href="stylesheets/styles.css">
  </head>
...
```

Make sure that you add the `<link>` tag for <samp class="filename">normalize.css</samp> <samp class="emphasis">before</samp> the `<link>` tag for <samp class="filename">styles.css</samp>. The browser needs to read the styles found in <samp class="filename">normalize.css</samp> before it reads yours.

And, just like that, your project can take advantage of this useful tool. No other setup is required.

You may be wondering why you are linking to an address on a completely different server. In fact, it is not unusual for an HTML file to specify resources located on different servers ([Figure 3.3](#ch03.html_fig-multiple-servers "Figure 3.3  Requesting resources from different servers")).

**Figure 3.3  Requesting resources from different servers**

![Requesting resources from different servers](Ottergram/Styles/img/request-from-multiple-servers.png)

In this case, <samp class="filename">normalize.css</samp> is hosted on [<samp class="uri">cdnjs.com</samp>](https://cdnjs.com/), a public server that is part of a <samp class="firstterm">content delivery network</samp>, or CDN. CDNs have servers all around the world, each with copies of the same files. When users request a file, they receive it from a server nearby, cutting down on the load time for that file. [<samp class="uri">cdnjs.com</samp>](https://cdnjs.com/) hosts many versions of popular front-end libraries and frameworks.

## Preparing the HTML for Styling

In the last chapter, you created a stylesheet called <samp class="filename">styles.css</samp>, and in this chapter you will add a number of CSS <samp class="firstterm">styling rules</samp> to it. But before you get started adding styles, you need to set up your HTML with targets for your styling rules to refer to.

You are going to add `class` attributes identifying the `span` elements with the otters’ names as “thumbnail titles.” `class` attributes are a way to identify a group of HTML elements, usually for styling. Your “thumbnail title” `class` will allow you to easily style all the names at once.

In <samp class="filename">index.html</samp>, add the class name `thumbnail-title` as an attribute of the `span`s inside the `li` elements, as shown:

```
...
    <ul>
      <li>
        <a href="#">
          <img src="img/otter1.jpg" alt="Barry the Otter">
          <span>Barry</span>
          <span class="thumbnail-title">Barry</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter2.jpg" alt="Robin the Otter">
          <span>Robin</span>
          <span class="thumbnail-title">Robin</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter1.jpg" alt="Maurice the Otter">
          <span>Maurice</span>
          <span class="thumbnail-title">Maurice</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter4.jpg" alt="Lesley the Otter">
          <span>Lesley</span>
          <span class="thumbnail-title">Lesley</span>
        </a>
      </li>
      <li>
        <a href="#">
          <img src="img/otter5.jpg" alt="Barbara the Otter">
          <span>Barbara</span>
          <span class="thumbnail-title">Barbara</span>
        </a>
    </ul>
...
```

In a moment, you will use this class name to style all the image titles.

## Anatomy of a Style

When you create individual styles, you do so by writing styling rules, which consist of two main parts: <samp class="firstterm">selectors</samp> and <samp class="firstterm">declarations</samp> ([Figure 3.4](#ch03s03.html_fig-style-anatomy "Figure 3.4  Anatomy of a styling rule")).

**Figure 3.4  Anatomy of a styling rule**

![Anatomy of a styling rule](Ottergram/Styles/img/anatomy-of-a-style-declaration.png)

The first part of a styling rule is one or more selectors. Selectors describe the elements that the style should be applied to, like `h1`, `span`, or `img`. But selectors are not limited to tag names. You can write selectors that apply to a more targeted set of elements by increasing the selector’s <samp class="firstterm">specificity</samp>.

For example, you can write selectors based on attributes – such as the `thumbnail-title` class attribute you just added to the `<span>` tags. Selectors based on attributes are more specific than selectors based on element names.

In addition to making sure that styles are only applied to a limited set of elements (e.g., elements with the class name `thumbnail-title` versus all `<span>` elements), specificity also determines the selector’s relative priority. If a stylesheet contains multiple styles that could apply to the same element, the styles with a selector of higher specificity will be used instead styles whose selector has a lower specificity. You can read more about specificity in a For the More Curious section at the end of this chapter.

Throughout this chapter, you will be introduced to a number of different kinds of selectors that vary in their specificity. Though there are often many ways to target the same element for styling, understanding specificity is key to choosing the best selector to use so that your styles are maintainable.

The second part of a styling rule is the declaration block, wrapped in curly braces, which defines the styles to be applied. The individual declarations within the block each include a property name and a value for that property.

In your first styling rule, you will use the `class` attribute you just added as a selector to apply styles around the otters’ names.

## Your First Styling Rule

To use a `class` as a selector in a styling rule, you prefix the class name with a dot (period), as in `.thumbnail-title`. The first styles you are going to add will set the background and foreground colors for the `.thumbnail-title` class.

Open <samp class="filename">styles.css</samp> and add your styling rule:

```
.thumbnail-title {
  background: rgb(96, 125, 139);
  color: rgb(202, 238, 255);
}
```

You will learn more about color later in this chapter. For now, just take a look at your changes. Save <samp class="filename">styles.css</samp> and make sure `browser-sync` is running. If you need to restart it, the command is:

```
browser-sync start --server --browser "Google Chrome"
                   --files "stylesheets/*.css, *.html"
```

This will open your web page in <samp class="application">Chrome</samp> ([Figure 3.5](#ch03s04.html_fig-look-colors "Figure 3.5  A slightly more colorful Ottergram")).

**Figure 3.5  A slightly more colorful Ottergram**

![A slightly more colorful Ottergram](Ottergram/Styles/img/look-colors.png)

You can see that you have set the background for the thumbnail titles to a deep gray-blue and the font color to a lighter blue. Nice.

Continue styling the thumbnail titles: Return to `styles.css` and add to your existing styling rule for the `.thumbnail-title` class, as shown:

```
.thumbnail-title {
  display: block;
  margin: 0;
  padding: 4px 10px;

  background: rgb(96, 125, 139);
  color: rgb(202, 238, 255);
}
```

The three declarations you have added all affect an element’s <samp class="firstterm">box</samp>. For every HTML tag that has a visual representation, the browser draws a rectangle to the page. The browser uses a scheme called the <samp class="firstterm">standard box model</samp> (or just “box model”) to determine the dimensions of that rectangle.

### The box model

To understand the box model, you are going to look at its representation in the DevTools. Save <samp class="filename">styles.css</samp>, switch to <samp class="application">Chrome</samp>, and make sure the DevTools are open ([Figure 3.6](#ch03s04.html_fig-opened-after-linking-css "Figure 3.6  Exploring the box model")).

**Figure 3.6  Exploring the box model**

![Exploring the box model](Ottergram/Styles/img/opened-after-linking-css.png)

Click the ![Exploring the box model](Ottergram/Styles/img/inspect-element-icon.png) button in the upper-left of the elements panel. This is the <samp class="firstterm">Inspect Element</samp> button. Now move your cursor over the word “ottergram” on the web page. As you hover over the word, the DevTools surrounds the heading with a blue- and peach-colored rectangle ([Figure 3.7](#ch03s04.html_fig-h1-hover "Figure 3.7  Hovering over the heading")).

**Figure 3.7  Hovering over the heading**

![Hovering over the heading](Ottergram/Styles/img/heading-being-inspected.png)

Click the word “ottergram” on the web page. Although you no longer see the multicolored overlay, the element is now selected and the DOM tree view in the elements panel will expand to show and highlight the corresponding `<h1>` tag.

The rectangular diagram in the lower-right of the elements panel represents the box model for the `h1` element. You can see that the regions of the diagram have some of the same colors as the rectangle you saw overlaying the heading when you inspected it ([Figure 3.8](#ch03s04.html_fig-box-model "Figure 3.8  Viewing the box model for an element")).

**Figure 3.8  Viewing the box model for an element**

![Viewing the box model for an element](Ottergram/Styles/img/box-model.png)

The box model incorporates four aspects of the rectangle drawn for an element (which the DevTools renders in four different colors in the diagram).

content (shown in blue)

the visual content – here, the text

padding (shown in green)

transparent space around the content

border (shown in yellow)

a border, which can be made visible, around the content and padding

margin (shown in peach)

transparent space around the border

The numbers in [Figure 3.8](#ch03s04.html_fig-box-model "Figure 3.8  Viewing the box model for an element") are <samp class="firstterm">pixel</samp> values; a pixel is a unit corresponding to the smallest rectangular area of a computer screen that can display a single color. In the case of the `h1` element, the content area has been allocated an area of 197 pixels by 54 pixels (your values may be different, depending on the size of your browser window). There is padding of 40 pixels on the left side. The border is set at 0, and there is a margin of 16 pixels above and below the element.

Where did that margin value come from? Each browser provides a default stylesheet, called the <samp class="firstterm">user agent stylesheet</samp>, in case an HTML file does not specify one. Styles that you specify override the defaults. Because you have not specified values for the `h1` element’s box, the default styles have been applied.

Now you are ready to understand the styling declarations you added:

```
.thumbnail-title {
  display: block;
  margin: 0;
  padding: 4px 10px;

  background: rgb(96, 125, 139);
  color: rgb(202, 238, 255);
}
```

The `display: block` declaration changes the box for all elements of the class `.thumbnail-title` so that they occupy the entire width allowed by their containing element. (Notice in [Figure 3.6](#ch03s04.html_fig-opened-after-linking-css "Figure 3.6  Exploring the box model") that the background color for the titles now covers a wider area.) Other `display` values, such as the `display: inline` property you will see later, make an element’s width fit to its content.

You also set the margin for the thumbnail titles to 0 and the padding to two different values: 4px and 10px (<samp class="firstterm">px</samp> is the abbreviation for “pixels”). This sets the padding to specific pixel values, overriding the default size set by the user agent stylesheet.

Padding, margin, and certain other styles can be written as <samp class="firstterm">shorthand properties</samp>, in which one value is applied to multiple properties. You are taking advantage of this here: When two values are provided for the padding, the first is applied to both vertical values (top and bottom) and the second is applied to both horizontal values (left and right). It is also possible to provide a single value to be applied to all four sides or to specify a separate value for each side.

To sum up, your new declarations say that the box for all elements of the `.thumbnail-title` class will fill the width of its container with no margin and with padding that is 4 pixels at the top and bottom and 10 pixels at the left and right sides.

## Style Inheritance

Next, you are going to add styles to change the size and appearance of the text.

Add a new styling rule in <samp class="filename">styles.css</samp> to set the font size for the `body` element. To do this, you will use a different type of selector – an <samp class="firstterm">element selector</samp> – by simply using the element’s name.

```
body {
  font-size: 10px;
}

.thumbnail-title {
  display: block;
  margin: 0;
  padding: 4px 10px;

  background: rgb(96, 125, 139);
  color: rgb(202, 238, 255);
}
```

This styling rule sets the `body` element’s `font-size` to `10px`.

You will rarely use element selectors in your stylesheets, because you will not often want to apply the exact same styles to every occurrence of a particular tag. Also, element selectors limit your ability to reuse styles; using them means that you may end up retyping the same declarations throughout your stylesheets. This is not great for maintenance if you need to alter those styles.

But, in this case, targeting the `body` element is exactly the right amount of specificity. There can be only one `<body>` element, and you will not be reusing its styles.

Save <samp class="filename">styles.css</samp> and check out your web page in <samp class="application">Chrome</samp> ([Figure 3.9](#ch03s05.html_fig-ottergram-with-10px-font "Figure 3.9  After setting the body font size")).

**Figure 3.9  After setting the `body` font size**

![After setting the body font size](Ottergram/Styles/img/ottergram-with-10px-font.png)

Your headline and thumbnail titles have gotten smaller. You may – or may not – have expected this. While the headline is directly within the `body` element where you declared the `font-size` property, the thumbnail titles are not. They are nested several levels deep. However, many styles, including font size, are applied to the elements specified by the styling rule as well as the <samp class="firstterm">descendants</samp> of those elements.

The structure of your document can be described using a tree diagram, as in [Figure 3.10](#ch03s05.html_fig-ottergram-tree "Figure 3.10  Simplified structure of Ottergram"). Representing your elements as a tree is a good way to visualize the DOM.

**Figure 3.10  Simplified structure of Ottergram**

![Simplified structure of Ottergram](Ottergram/Styles/img/ottergram-dom.png)

An element contained within another element is said to be its descendent. In this case, your `span`s are all descendents of the `body` (as well as the `ul` and their respective `li`), so they inherit the `body`’s `font-size` style.

In the DevTools’ DOM tree view, locate and select one of the `span` elements. In the styles pane, notice the boxes labeled <samp class="guilabel">Inherited from a</samp>, <samp class="guilabel">Inherited from li</samp>, and <samp class="guilabel">Inherited from ul</samp>. These three areas, as indicated, show styles inherited at each level from the user agent stylesheet. Under <samp class="guilabel">Inherited from body</samp>, you can see that the `font-size` property has been inherited from the style set for the `body` element in <samp class="filename">styles.css</samp> ([Figure 3.11](#ch03s05.html_fig-devtools-demo-cascade "Figure 3.11  Styles inherited from ancestor elements")).

**Figure 3.11  Styles inherited from ancestor elements**

![Styles inherited from ancestor elements](Ottergram/Styles/img/devtools-demo-cascade.png)

What if a different font size were set at another level, such as the `ul`? Styles from the closer ancestor take priority, so a font size set in <samp class="filename">styles.css</samp> for the `ul` would override one set for the `body` and a font size set for the `span` element itself would override them both.

To see this, click on the `ul` element in the DOM tree view. This will allow you to try out styles on the fly. The styles you add here will be immediately reflected in the web page view, but will not be added to your actual project files.

At the top of the styles pane in the elements panel, you will see a section labeled `elements.style`. Click anywhere in between the curly braces of the `elements.style`, and the DevTools will give you a prompt ([Figure 3.12](#ch03s05.html_fig-elements-style-prompt "Figure 3.12  Prompting for a style rule")).

**Figure 3.12  Prompting for a style rule**

![Prompting for a style rule](Ottergram/Styles/img/elements-style-prompt.png)

Start typing `font-size`, and the DevTools will suggest possible completions ([Figure 3.13](#ch03s05.html_fig-begin-typing-font-size "Figure 3.13  Autocompletion options in styles pane")).

**Figure 3.13  Autocompletion options in styles pane**

![Autocompletion options in styles pane](Ottergram/Styles/img/begin-typing-font-size.png)

Choose `font-size`, then press the Tab key. Enter a large value, such as `50px`, and press Return. You may need to scroll the page, but you will see that the `ul`’s `font-size` has overridden the `body`’s ([Figure 3.14](#ch03s05.html_fig-scroll-big-font "Figure 3.14  Giving the ul a font-size of 50px")).

**Figure 3.14  Giving the `ul` a `font-size` of 50px**

![Giving the ul a font-size of 50px](Ottergram/Styles/img/scroll-big-font.png)

Not all style properties are inherited – `border`, for example, is not. To find out whether a property is inherited, refer to the property’s MDN reference page.

Back in <samp class="filename">styles.css</samp>, update your declaration block for the `.thumbnail-title` class to override the `body`’s `font-size` and use a larger font.

```
body {
  font-size: 10px;
}

.thumbnail-title {
  display: block;
  margin: 0;
  padding: 4px 10px;

  background: rgb(96, 125, 139);
  color: rgb(202, 238, 255);

  font-size: 18px;
}
```

For elements of the class `.thumbnail-title`, you changed the font size to 18 pixels.

Save <samp class="filename">styles.css</samp> and admire your thumbnail titles in <samp class="application">Chrome</samp> ([Figure 3.15](#ch03s05.html_fig-thumbnail-titles-styled "Figure 3.15  Styled thumbnail titles")).

**Figure 3.15  Styled thumbnail titles**

![Styled thumbnail titles](Ottergram/Styles/img/thumbnail-title-box.png)

They look good, but the user agent stylesheet is adding underlines to the `.thumbnail-title` elements. This is because you wrapped them (along with the `.thumbnail-image` elements) with an anchor tag, making them inherit the underline style.

You do not need the underlines, so you are going to remove them by changing the `text-decoration` property for the anchor tags in a new styling rule in <samp class="filename">styles.css</samp>. What selector should you use for this rule?

If you are confident that you want to remove the underlines from the thumbnail titles <samp class="emphasis">as well as any other anchor elements in Ottergram</samp>, you can simply use an element selector:

```
a {
  /* style declaration */
}
```

(The text between the `/* */` indicators is a CSS <samp class="firstterm">comment</samp>. Code comments are ignored by the browser; they allow the developer to make notes in the code for future reference.)

If you think you might use anchors for another purpose (and will want to style them differently), you can pair the element selector with an <samp class="firstterm">attribute selector</samp>, like this:

```
a[href]{
  /* style declaration */
}
```

This selector would match any anchor element with an `href` attribute. Of course, anchor elements generally do have `href` attributes, so that might not be targeted enough to match only the thumbnail images and titles. To make an attribute selector more precise, you can also specify the value of the attribute, like this:

```
a[href="#"]{
  /* style declaration */
}
```

This selector would match only those anchor elements whose `href` attribute has a value of `#`.

By the way, you can also use attribute selectors, with or without values, on their own, such as:

```
[href]{
  /* style declaration */
}
```

As it happens, Ottergram is a fairly simple project and you will not, in fact, be using anchor tags for anything other than the thumbnails and their titles. It is therefore safe to use an element selector, and you should do so because it is the most straightforward solution with the right amount of specificity.

Add the new style declaration to <samp class="filename">styles.css</samp>:

```
body {
  font-size: 10px;
}

a {
  text-decoration: none;
}

.thumbnail-title {
  ...
}
```

Save your file and check your browser. The underlines are gone and your thumbnail titles are nicely styled ([Figure 3.16](#ch03s05.html_fig-no-underline "Figure 3.16  After setting text-decoration to none")).

**Figure 3.16  After setting `text-decoration` to `none`**

![After setting text-decoration to none](Ottergram/Styles/img/removed-text-decoration.png)

Note that you should not remove the underlines from links that are in normal text – text that is not an obvious heading, title, or caption. The underlining of linked text is an important visual indicator that users have come to expect. You did it here because the thumbnails do not require the same visual cues. Users will reasonably expect them to be clickable.

In the rest of the chapter, you will use class selectors to style the thumbnail images, the unordered list of images, the list items (which include the thumbnail images and their titles), and, finally, the header. Go ahead and add class names to the `h1`, `ul`, `li`, and `img` elements in <samp class="filename">index.html</samp> so they are ready as you need them.

```
...
  </head>
  <body>
    <header>
      <h1>ottergram</h1>
      <h1 class="logo-text">ottergram</h1>
    </header>
    <ul>
    <ul class="thumbnail-list">
      <li>
      <li class="thumbnail-item">
        <a href="#">
          <img src="img/otter1.jpg" alt="Barry the Otter">
          <img class="thumbnail-image" src="img/otter1.jpg" alt="Barry the Otter">
          <span class="thumbnail-title">Barry</span>
        </a>
      </li>
      <li>
      <li class="thumbnail-item">
        <a href="#">
          <img src="img/otter2.jpg" alt="Robin the Otter">
          <img class="thumbnail-image" src="img/otter2.jpg" alt="Robin the Otter">
          <span class="thumbnail-title">Robin</span>
        </a>
      </li>
      <li>
      <li class="thumbnail-item">
        <a href="#">
          <img src="img/otter3.jpg" alt="Maurice the Otter">
          <img class="thumbnail-image" src="img/otter3.jpg" alt="Maurice the Otter">
          <span class="thumbnail-title">Maurice</span>
        </a>
      </li>
      <li>
      <li class="thumbnail-item">
        <a href="#">
          <img src="img/otter4.jpg" alt="Lesley the Otter">
          <img class="thumbnail-image" src="img/otter4.jpg" alt="Lesley the Otter">
          <span class="thumbnail-title">Lesley</span>
        </a>
      </li>
      <li>
      <li class="thumbnail-item">
        <a href="#">
          <img src="img/otter5.jpg" alt="Barbara the Otter">
          <img class="thumbnail-image" src="img/otter5.jpg" alt="Barbara the Otter">
          <span class="thumbnail-title">Barbara</span>
        </a>
      </li>
    </ul>
...
```

By adding class names to these elements, you have given yourself targets for the styles you will be adding.

We favor class selectors over other kinds of selectors, and you should, too. You can write very descriptive class names that make your code easy to develop and maintain. Also, you can add multiple class names to an element, making them a flexible and powerful tool for styling.

Be sure to save <samp class="filename">index.html</samp> before moving on.

## Making Images Fit the Window

Following the atomic styling pattern, the images are next in line for styling. They are so large that they are cut off unless the browser window is also large. Add a styling rule for `.thumbnail-image` in <samp class="filename">styles.css</samp> to make the thumbnails fit in the window:

```
...
a {
  text-decoration: none;
}

.thumbnail-image {
  width: 100%;
}

.thumbnail-title {
  ...
}
```

You set the `width` to `100%`, which constrains it to the width of its container. This means that as you widen the browser window, the images get proportionally larger. Check it out: Save <samp class="filename">styles.css</samp>, switch to your browser, and make your browser window larger and smaller. The images grow and shrink along with the browser window, always keeping their proportions. [Figure 3.17](#ch03s06.html_fig-fit-image-width "Figure 3.17  Fitting an image by width") shows Ottergram in one narrow and one wider browser window.

**Figure 3.17  Fitting an image by width**

![Fitting an image by width](Ottergram/Styles/img/constrained-width.png)

If you look closely, the spacing around the `.thumbnail-title`s is off, so that it appears that the titles go with the images below them. Fix that in <samp class="filename">styles.css</samp> by setting the `.thumbnail-image`’s `display` property to `block`.

```
...
.thumbnail-image {
  display: block;
  width: 100%;
}
...
```

Now the space between the image and its title is gone ([Figure 3.18](#ch03s06.html_fig-whitespace-fix "Figure 3.18  After setting .thumbnail-image to display: block")).

**Figure 3.18  After setting `.thumbnail-image` to `display: block`**

![After setting .thumbnail-image to display: block](Ottergram/Styles/img/fixed-li-spacing-display-block.png)

Why does this work? Images are `display: inline` by default. They are subject to similar rendering rules as text. When text is rendered, the letters are drawn along a common baseline. Some characters, such as <samp class="literal">p</samp>, <samp class="literal">q</samp>, and <samp class="literal">y</samp>, have a <samp class="firstterm">descender</samp> - the tail that drops below this baseline. To accommodate them, there is some whitespace included below the baseline.

Setting the `display` property to `block` removes the whitespace because there is no need to accommodate any text (or any other `display: inline` elements that might be rendered alongside the image).

## Color

It is time to explore color a little more deeply. Add the following color styles for the `body` element and the `.thumbnail-item` class in <samp class="filename">styles.css</samp>.

```
body {
  font-size: 10px;
  background: rgb(149, 194, 215);
}

a {
  text-decoration: none;
}

.thumbnail-item {
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);
}
...
```

You have declared values for the `.thumbnail-item`’s border twice. Why? Notice that the two declarations use slightly different color functions: `rgb` and `rgba`. The `rgba` color function accepts a fourth argument, which is the opacity. However, some browsers do not support `rgba`, so providing both declarations is a technique that provides a <samp class="emphasis">fallback</samp> value.

All browsers will see the first declaration (`rgb`) and register its value for the `border` property. When browsers that do not support `rgba` see the second declaration, they will not understand it and will simply ignore it, using the value from the first declaration. Browsers that <samp class="emphasis">do</samp> support `rgba` will use the value in the second declaration and discard the value from the first declaration.

(Wondering why the `body`’s background color is defined with integers and the `.thumbnail-item`’s border color is defined with percentages? We will come back to that in just a moment.)

Save <samp class="filename">styles.css</samp> and switch to your browser ([Figure 3.19](#ch03s07.html_fig-thumbnail-item-border-color "Figure 3.19  Background color and borders")).

**Figure 3.19  Background color and borders**

![Background color and borders](Ottergram/Styles/img/thumbnail-item-border-color.png)

In the DevTools, you can see that <samp class="application">Chrome</samp> supports `rgba`. It denotes that the `rgb` color is not used by striking through the style ([Figure 3.20](#ch03s07.html_fig-inheritance-crossout "Figure 3.20  rgba is used when supported by browser"))

**Figure 3.20  rgba is used when supported by browser**

![rgba is used when supported by browser](Ottergram/Styles/img/inheritance-crossout.png)

Now, still in the DevTools, select the `body`. In the styles pane, notice the declaration for the background color that you just added. To the left of the RGB value is a small square showing you what the color will look like.

Click that square, and a color picker opens ([Figure 3.21](#ch03s07.html_fig-color-picker "Figure 3.21  The color picker in the styles pane")). The color picker lets you choose a color and will give you the CSS color value in a variety of different formats.

**Figure 3.21  The color picker in the styles pane**

![The color picker in the styles pane](Ottergram/Styles/img/color-picker.png)

To see the background color in different color formats, click the up and down arrows to the right of the RGBA values. You can cycle through HSLA, HEX, and RGBA formats.

The HSLA format (which stands for “hue saturation lightness alpha”) is used less frequently than the others, partly because some of the most popular design tools do not provide HSLA values that are accurate for CSS. If you are curious about HSLA, visit the HSLA Explorer at [<samp class="uri">css-tricks.com/​examples/​HSLaExplorer</samp>](https://css-tricks.com/examples/HSLaExplorer/).

Take a look at the HEX value for the background color: `#95C2D7`. HEX, or hexadecimal, is the oldest color specification format. Each digit represents a value from 0 to 15\. (If you are not familiar with hexadecimal numbers, this is done by including the characters A through F as digits.) Each pair of digits, then, can represent a value from 0 to 255\. From left to right, the pairs of digits correspond to the intensity of red, green, and blue in the color being specified ([Figure 3.22](#ch03s07.html_fig-hex-diagram "Figure 3.22  HEX values correspond to red, green, and blue values")).

**Figure 3.22  HEX values correspond to red, green, and blue values**

![HEX values correspond to red, green, and blue values](Ottergram/Styles/img/hex-diagram.png)

Many find HEX colors unintuitive. A modern alternative is to use RGB (red, green, and blue) values. In this model, each color is also assigned a value from 0 to 255, but the values are represented in more familiar decimal numbers and separated by color. As mentioned earlier, for more capable browsers a fourth value can specify the opacity or transparency of the specified color, from 0.0 (fully transparent) to 1.0 (fully opaque). The opacity is officially known as the <samp class="firstterm">alpha</samp> value – hence the A in RGBA. The RGBA value of the `body`’s background color is `(149, 194, 215, 1)`.

As an alternative to declaring integer values for red, green, and blue, you can also use percentages, as you did for the `.thumbnail-item` borders. There is no functional difference between the two options. Just do not mix percentages and integers in the same declaration.

By the way, for help selecting pleasing color palettes, Adobe provides a free online tool at [<samp class="uri">color.adobe.com</samp>](https://color.adobe.com/).

## Adjusting the Space Between Items

Ottergram now has some nice colors reminiscent of otters’ ocean home. But adding the colors has revealed some unwanted whitespace inside the border of the `.thumbnail-item` elements. Also, those pesky bullets are drawing attention away from the glory of the otters.

To get rid of the bullets, set the `.thumbnail-list`’s `list-style` property to `none` in <samp class="filename">styles.css</samp>:

```
...
.thumbnail-item {
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);
}

.thumbnail-list {
  list-style: none;
}

.thumbnail-image {
  ...
```

To get rid of the whitespace, you will use the same technique you used with the `.thumbnail-image`. Each `.thumbnail-item` has that whitespace by default to accommodate items in a list, just as the `.thumbnail-image` elements had whitespace to accommodate neighboring text. Add a `display: block` declaration for `.thumbnail-item` to remove it.

```
...
.thumbnail-item {
  display: block;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);
}
...
```

With those additions, the bullets and the excess space above the images disappear, resulting in the more polished layout shown in [Figure 3.23](#ch03s08.html_fig-whitespace-removed "Figure 3.23  Improved layout").

**Figure 3.23  Improved layout**

![Improved layout](Ottergram/Styles/img/whitespace-removed.png)

Why use a bullet list if you do not want bullets? It is best to choose HTML tags based on what they are and not how the browser will style them by default. In this case, you want an unordered list of images, so a `ul` is the way to go. The `ul` container for your images will let you style them as a scrolling list when you add a detail image to your project in [Chapter 4](#ch04.html "4 Responsive Layouts with Flexbox"). The fact that the browser represents `ul`s with bullets by default is not important, as they are easily removed.

Next, you are going to adjust the spacing of the items in the list. The individual `.thumbnail-item` elements currently have no space between them. You are going to add margins between adjacent thumbnails.

However, you do not want to add a margin to <samp class="emphasis">all</samp> of the list items. Why not? Because the heading already has a margin, so the first list item does not need one. This means that you cannot use the `.thumbnail-item` class selector, at least not on its own. Instead, you will use selector syntax that targets elements based on their relationship to other elements.

### Relationship selectors

Look again at the diagram of your project in [Figure 3.10](#ch03s05.html_fig-ottergram-tree "Figure 3.10  Simplified structure of Ottergram"). It looks much like a family tree, doesn’t it? This similarity gives the set of relationship selectors their names: <samp class="firstterm">descendent selectors</samp>, <samp class="firstterm">child selectors</samp>, <samp class="firstterm">sibling selectors</samp>, and <samp class="firstterm">adjacent sibling selectors</samp>.

Relationship selector syntax includes two selectors (like class or element selectors) joined by a symbol called a <samp class="firstterm">combinator</samp> that determines the targeted relationship between them. To understand how relationship selectors work, it is important to keep in mind that the browser reads selector syntax from <samp class="emphasis">right to left</samp>. Let’s look at some examples.

A descendent selector targets any element of one specified type that is the descendent of another specified element. For example, to select any `span` element that is the descendent of the `body` element, the syntax would be:

```
body span {
  /* style declarations */
}
```

This syntax uses no combinator. Because it is read from right to left, it targets any `span` descended from a `body`, which in the current code means the thumbnail titles. It would also affect any `span`s that might be added within the `header` or elsewhere within the `body`.

Note that you can also use a class selector (or attribute selector, or indeed any type of selector) within a relationship selector, so the selector above could also be written as:

```
body .thumbnail-title {
  /* style declarations */
}
```

Child selectors target elements of a specified type that are the immediate children of another specified element. Child selector syntax uses the combinator `>`. To use child selector syntax to target all the `span`s currently in Ottergram, the syntax would be:

```
li > span {
  /* style declarations */
}
```

Reading from right to left, this selector targets any `span` that is the immediate child of a `li` element – again, the thumbnail titles.

Sibling selector syntax uses the combinator `~`. As you might expect, this syntax targets elements with the same parent. However, because of the directional nature of relationship selectors, the results might not be exactly as you expect. Take this example:

```
header ~ ul {
  /* style declarations */
}
```

This selector targets any `ul` that is <samp class="emphasis">preceded</samp> by a `header` with the same parent element. This selector would effectively target Ottergram’s `ul`, because it has a sibling `header` that precedes it in the code. However, reversing the syntax (`ul ~ header`) would result in no elements being selected, because there is no `header` preceded by a sibling `ul`.

The final relationship selector type is the adjacent sibling selector, which targets elements that are <samp class="emphasis">immediately</samp> preceded by a sibling of the specified type. The adjacent sibling combinator is `+`:

```
li + li {
  /* style declarations */
}
```

This syntax would select all `li` elements immediately preceded by a sibling `li`. The result is that the declared styles would be applied to the second through fifth `li` – but not the first, because it is not immediately preceded by another `li`. (Note that the general sibling selector and the adjacent sibling selector would work the same way at the moment, due to Ottergram’s relatively simple structure.)

Back to the task at hand: adding a margin to the top of each list item except the first. If you used a descendent or child selector to target the `.thumbnail-item` class or the `span` or `li` elements, the margin would be applied to all five thumbnails. Because you want to style all but the first, use the adjacent sibling syntax in <samp class="filename">styles.css</samp> to add a top margin to only those thumbnails that are immediately preceded by another thumbnail.

```
...
a {
  text-decoration: none;
}

.thumbnail-item + .thumbnail-item {
  margin-top: 10px;
}

.thumbnail-item {
  ...
```

Save your file and check out the results in your browser ([Figure 3.24](#ch03s08.html_fig-sibling-spacing "Figure 3.24  Spacing between adjacent .thumbnail-item elements")).

**Figure 3.24  Spacing between adjacent `.thumbnail-item` elements**

![Spacing between adjacent .thumbnail-item elements](Ottergram/Styles/img/adjacent-spacing.png)

Note that the DevTools give you an easy way to find out the nesting path of an element, which can help with writing relationship selectors. If you click one of the `span` elements inside one of the `li` elements, you can see its path at the bottom of the elements panel ([Figure 3.25](#ch03s08.html_fig-nesting-path "Figure 3.25  Nesting path shown by the elements panel")).

**Figure 3.25  Nesting path shown by the elements panel**

![Nesting path shown by the elements panel](Ottergram/Styles/img/selector-path.png)

For one final tweak to the thumbnail list’s appearance, return to <samp class="filename">styles.css</samp> and override the padding that the `ul` inherits from the user agent stylesheet so that the images are no longer indented.

```
...
.thumbnail-list {
  list-style: none;
  padding: 0;
}
...
```

As usual, save your file and switch to your browser to see your results ([Figure 3.26](#ch03s08.html_fig-ul-styled "Figure 3.26  ul with padding removed")).

**Figure 3.26  `ul` with padding removed**

![ul with padding removed](Ottergram/Styles/img/removed-ul-padding.png)

Ottergram is starting to look polished. With some styling for the header, you will have a nice static web page.

## Adding a Font

Earlier, you added the `.logo-text` class to the `h1` element. Use that class as the selector for a new styling rule in <samp class="filename">styles.css</samp>. Insert it after the styles for the anchor tag. (In general, the order of your styles only matters when you have multiple rule sets for the same selector. In Ottergram, the styles are arranged in roughly the same order as they appear in the code. This is a matter of preference, and you are free to organize your styles as you see fit.)

```
...
a {
  text-decoration: none;
}

.logo-text {
  background: white;

  text-align: center;
  text-transform: uppercase;
  font-size: 37px;
}

.thumbnail-item + .thumbnail-item {
  ...
```

First, you gave the header a white background. Then you centered the text inside the `.logo-text` element and used the `text-transform` property to format it as uppercase. Finally, you set the font size. Your results will look like [Figure 3.27](#ch03s09.html_fig-plain-header "Figure 3.27  Styling the header").

**Figure 3.27  Styling the header**

![Styling the header](Ottergram/Styles/img/plain-header.png)

Ottergram looks great. Great… but a little plain for a website with <samp class="emphasis">otters</samp>. To add some pizzazz, you can use a font for the header other than the default provided by the user agent stylesheet.

We included some fonts in the resource files you already downloaded and added to your project directory. To use them, you need to copy the <samp class="filename">fonts</samp> folder into your project. Place it <samp class="emphasis">inside</samp> your <samp class="filename">stylesheets</samp> folder ([Figure 3.28](#ch03s09.html_fig-fonts-inside-stylesheets "Figure 3.28  fonts folder inside stylesheets folder")).

**Figure 3.28  `fonts` folder inside `stylesheets` folder**

![fonts folder inside stylesheets folder](Ottergram/Styles/img/fonts-inside-stylesheets.png)

Now you only need to point some styles to those fonts.

The resource files include many formats of each font. As usual, different browser vendors support different kinds of fonts. To support the widest array of browsers, you need to include all of them in your project. Yes, all of them.

To help you out, the <samp class="firstterm">@font-face</samp> syntax lets you give a custom name to a family of fonts that you can then use in the rest of your styles.

An `@font-face` block is a little different from the declaration blocks you have been using. Inside of the `@font-face` block are three main parts:

*   First, the `font-family` property, whose value is a string identifying the custom font name you can use throughout your CSS file.

*   Next, several `src` declarations specifying different font files. (Take note – the order is important!)

*   Last, declarations that modify the font’s presentation, such as the `font-weight` and the `font-style`.

Add an `@font-face` declaration for the `lakeshore` font family to the top of <samp class="filename">styles.css</samp> and a style declaration to use the new font for the `.logo-text` class.

```
@font-face {
    font-family: 'lakeshore';
    src: url('fonts/LAKESHOR-webfont.eot');
    src: url('fonts/LAKESHOR-webfont.eot?#iefix') format('embedded-opentype'),
         url('fonts/LAKESHOR-webfont.woff') format('woff'),
         url('fonts/LAKESHOR-webfont.ttf') format('truetype'),
         url('fonts/LAKESHOR-webfont.svg#lakeshore') format('svg');
    font-weight: normal;
    font-style: normal;
}

body {
  font-size: 10px;
  background: rgb(149, 194, 215);
}

a {
  text-decoration: none;
}

.logo-text {
 background: white;

 text-align: center;
 text-transform: uppercase;
 font-family: lakeshore;
 font-size: 37px;
}
...
```

Admittedly, getting the `@font-face` declaration just right can be tricky, because the order of the individual `url` values is important. It is a good idea to keep a copy of the declaration for reference. You can also look into <samp class="application">Atom</samp>’s snippets documentation at [<samp class="uri">flight-manual.atom.io/​using-atom/​sections/​snippets</samp>](http://flight-manual.atom.io/using-atom/sections/snippets/) to see how to create your own code “snippet,” or template.

After declaring the custom `@font-face`, the rest of your CSS has access to the new `lakeshore` value for the `font-family` property. In the `.logo-text` declaration, you set `font-family: lakeshore` to apply the new font.

Save <samp class="filename">styles.css</samp>, switch to <samp class="application">Chrome</samp>, and see how good it feels to have a web page as stylish as an otter ([Figure 3.29](#ch03s09.html_fig-oh-yeah-header "Figure 3.29  Applying a custom font to the header")).

**Figure 3.29  Applying a custom font to the header**

![Applying a custom font to the header](Ottergram/Styles/img/oh-yeah-header.png)

You did a lot of styling work in this chapter, and Ottergram looks great! In the next chapter you will make it even better by adding interactive functionality.

## Bronze Challenge: Color Change

Change the background color styles for `body`. Use the color picker in the DevTools ([Figure 3.21](#ch03s07.html_fig-color-picker "Figure 3.21  The color picker in the styles pane")) to help you choose one.

For a more sophisticated color palette, go to [<samp class="uri">color.adobe.com</samp>](https://color.adobe.com/) and create your own scheme for the `body` and `.thumbnail-title` background colors.

## For the More Curious: Specificity! When Selectors Collide…

You have already seen how you can override styles. You included the link for <samp class="filename">normalize.css</samp> before the one for <samp class="filename">styles.css</samp>, for example. This made the browser use <samp class="filename">normalize.css</samp>’s styles as a baseline, with your styles taking precedence over the baseline styles.

This is the first basic concept of how the browser chooses which styles to apply to the elements on the page, known to front-end developers as <samp class="firstterm">recency</samp>: As the browser processes CSS rules, they can override rules that were processed earlier. You can control the order in which the browser processes CSS by changing the order of the `<link>` tags.

This is simple enough when the rules have the same selector (for example, if your CSS and <samp class="filename">normalize.css</samp> were to declare a different `margin` for the `body` element). In this case, the browser chooses the more recent declaration. But what about elements that are matched by more than one selector?

Say you had these two rules in your Ottergram CSS:

```
.thumbnail-item {
  background: blue;
  }

li {
  background: red;
}
```

Both of these match your `<li>` elements. What background color will your `<li>` elements have? Even though the `li { background: red; }` rule is more recent, `.thumbnail-item { background: blue; }` will be used. Why? Because it uses a class selector, which is more specific (i.e., assigned a higher specificity value) than the element selector.

Class selectors and attribute selectors have the same degree of specificity, and both have a higher specificity than element selectors. The highest degree of specificity goes to <samp class="firstterm">ID selectors</samp>, which you have not seen yet. If you give an element an `id` attribute, you can write an ID selector that is more specific than any other selector.

ID attributes look like other attributes. For example:

```
<li class="thumbnail-item" id="barry-otter">
```

To use the ID in a selector, you prefix it with `#`:

```
.thumbnail-item {
  background: blue;
}

#barry-otter {
  background: green;
}

li {
  background: red;
}
```

In this example, the `<li>` is matched by all three selectors, but it will have a green background because the ID selector has the highest specificity. The order of your rulesets makes no difference here, because each has a different specificity.

One note about using ID selectors: It is best to avoid them. ID values must be unique in the document, so you cannot use the `id="barry-otter"` attribute for any other element in your document. Even though ID selectors have the highest specificity, their associated styles cannot be reused, making them a maintenance “worst practice.”

To learn more about specificity, go to the MDN page [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​CSS/​Specificity</samp>](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity).

The Specificity Calculator at [<samp class="uri">specificity.keegan.st</samp>](http://specificity.keegan.st/) is a great tool for comparing the specificty of different selectors. Check it out to get a more precise understanding of how specificity is computed.

# <samp class="chapter_number">4</samp>
<samp class="chapter_name">Responsive Layouts with Flexbox</samp>

One of the duties of front-end developers is to provide the best experience to users regardless of what device or browser they are using.

This was not always the prevailing attitude, and the companies that made browsers were partly to blame. In the early days of the web, browser makers were fighting a war. Each would invent new nonstandard features in an attempt to out-do the others. In response, web developers came up with schemes for detecting which browser was requesting a document and what screen size was being used. Based on this information, a different version of the document was served out.

Sadly, this meant that front-end development became weighed down with creating multiple copies of every page on a site, each copy built with the markup and styles that would work for a specific version of a browser running at a particular screen size. Maintaining all of these copies was both time consuming and frustrating.

Thankfully, the Browser Wars are over, and browser makers now strive to conform to the same set of standard features – and modern front-end developers are free to focus on a single codebase for a website. Gone are the days of needing to create browser-specific versions of a page. But that does not mean that developers can no longer provide tailored pages based on different screen sizes or orientations. New technologies – like <samp class="firstterm">flexbox</samp>, which you will learn about in this chapter – allow layouts to adjust to the user’s screen size without requiring duplicate documents.

In this chapter, you are going to expand Ottergram from a simple list of images to a proper user interface ready for interactive content. Using flexbox and CSS positioning, you will build a set of interface components that adjust as needed to variations in the size of the browser window while maintaining the overall layout. At the end of the chapter, Ottergram will feature a scrolling list of thumbnail images and an area that displays a large, detailed version of a single image ([Figure 4.1](#ch04.html_fig-flexbox-otters "Figure 4.1  Ottergram with flexible layout")).

**Figure 4.1  Ottergram with flexible layout**

![Ottergram with flexible layout](Ottergram/Flexbox/img/flexbox-otters.png)

You will do this in two parts. First, you will add the minimal markup and styles necessary to show the large image on the page and to make the thumbnails smaller and scrollable. Then, you will add styles that let parts of the page stretch and shrink as the window changes size or to accommodate screens of different sizes.

## Expanding the Interface

Since the introduction of the iPhone, the trend toward accessing the internet via a smartphone, rather than a desktop or laptop, has grown steadily.

For front-end developers, this trend has meant that <samp class="firstterm">mobile-first development</samp> has proven to be the best design approach: designing for small screens first, then building on that design for tablet-size screens, and finally building up to a desktop-sized design.

Ottergram’s simple layout is already mobile-friendly. It displays the text and images at a scale that is appropriate for smaller screen sizes. Because of this, you can move right into adding the next level of complexity to your layout.

A vertically scrolling list of otters is fine, but it would be even better if the user could also see a larger version of the images. The plan for Ottergram is to make the thumbnail list scroll horizontally while a larger detail image is featured. For now, the detail image will be below the list. This plan is diagrammed in [Figure 4.2](#ch04.html_fig-layout-diagram "Figure 4.2  New layout for Ottergram").

**Figure 4.2  New layout for Ottergram**

![New layout for Ottergram](Ottergram/Flexbox/img/layout-diagram.png)

You will begin by adding the detail image.

### Adding the detail image

For now, your detail image will be fixed to a single image. In [Chapter 6](#ch06.html "6 Handling Events with JavaScript") you will add functionality so that the user can click on a thumbnail to make any image the detail image.

Add a new section of code to create the detail image in <samp class="filename">index.html</samp>:

```
...
      <li class="thumbnail-item">
        <a href="#">
          <img class="thumbnail-image" src="img/otter5.jpg" alt="Barbara the Otter">
          <span class="thumbnail-title">Barbara</span>
        </a>
      </li>
    </ul>

    <div class="detail-image-container">
      <img class="detail-image" src="img/otter1.jpg" alt="">
      <span class="detail-image-title">Stayin' Alive</span>
    </div>

  </body>
</html>
```

You added a `<div>` with a `detail-image-container` class. A `<div>` is a generic container for content – usually for the purpose of applying styling to the enclosed content, which is exactly how you will use it.

Inside the `<div>` you added an `<img>` tag to display the large version of the otter image. You also added a `<span>`, which wraps around the title text for the detail image. You gave the `<img>` and `<span>` tags the class names `detail-image` and `detail-image-title`, respectively.

Save <samp class="filename">index.html</samp>, switch to <samp class="filename">styles.css</samp>, and, at the end, constrain the width of your new `.detail-image` class.

```
...
.thumbnail-title {
  ...
}

.detail-image {
  width: 90%;
}
```

Save <samp class="filename">styles.css</samp> and start `browser-sync` to open your project in <samp class="application">Chrome</samp> ([Figure 4.3](#ch04.html_fig-detail-image-initial-style "Figure 4.3  Initial styling for the detail image")). (The command is `browser-sync start --server --browser "Google Chrome" --files "stylesheets/*.css, *.html"`.)

**Figure 4.3  Initial styling for the detail image**

![Initial styling for the detail image](Ottergram/Flexbox/img/detail-image-initial-style.png)

Your `.detail-image` will appear at the bottom of the page, a bit narrower than your thumbnails. By making the detail image 90% of its container’s width, you have left a little space next to it. The browser puts the text of the `.detail-image-title` in that space. (You will style that text later in this chapter.)

If you resize the page, you will discover a bug: The detail image may be pushed out of view by the thumbnails as they adjust to the new width. You will address this problem later in this chapter.

### Horizontal layout for thumbnails

Next, you will update the `.thumbnail-list` and `.thumbnail-item` classes so that the images scroll horizontally.

To help you test your scrolling, duplicate all five `<li>` elements in <samp class="filename">index.html</samp>. This will give you lots of content to scroll through. To do this, simply select all of the lines between `<ul class="thumbnail-list">` and `</ul>`, copy them, and paste the result just above the `</ul>`. You should end up with 10 list items, containing images <samp class="filename">otter1.jpg</samp> through <samp class="filename">otter5.jpg</samp> twice.

Be sure to save <samp class="filename">index.html</samp> when you are done. Duplicating content while you are developing is a good technique for simulating a more robust project. It allows you to see how your code handles real-world situations.

For a horizontally scrolling list of thumbnails, each thumbnail must be constrained to a specific width and the thumbnails should be laid out horizontally on a single line.

The `display: block` property, which you have used several times, will not create the desired effect. It causes the browser to render a line break before and after the element. However, a related style, `display: inline-block`, is perfect for this situation. With `inline-block`, the element’s box is drawn as if you declared `display: block`, but without the line breaks – allowing your thumbnails to stay lined up in a row.

Add a `width` declaration and change the `display` declaration for the `.thumbnail-item` class in <samp class="filename">styles.css</samp>.

```
...
.thumbnail-item {
  display: block;
  display: inline-block;
  width: 120px;
  border: 1px solid rgb(100%, 100%, 100%, 0.8);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);
}
...
```

(Note that <samp class="application">Atom</samp>’s linter may warn you that “Using width with border can sometimes make elements larger than you expect.” This is because the `width` property only applies to the content portion – not the padding or border – of the element’s box. You do not need to do anything about this warning.)

With the `.thumbnail-item` element’s width set to an absolute value of `120px`, the `.thumbnail-image` is effectively fixed as well, since the `.thumbnail-image` adjusts to its container’s width.

Why not just set the `.thumbnail-image` to `width: 120px`? You want the `.thumbnail-image` and the `.thumbnail-title` to be the same width. Instead of setting the `width` property for each of these, you set it on their common parent element. That way, if you need to change the `width`, you only need to change it in one place. Generally, it is a good practice to have inner elements adapt to their containers.

Save <samp class="filename">styles.css</samp> and check your page in <samp class="application">Chrome</samp>. You can see that the `.thumbnail-item` elements line up side by side – but when they fill the width of their container, they wrap around ([Figure 4.4](#ch04.html_fig-wrapping-rows "Figure 4.4  inline-block creates rows that wrap")).

**Figure 4.4  `inline-block` creates rows that wrap**

![inline-block creates rows that wrap](Ottergram/Flexbox/img/wrapping-thumbnails.png)

To get the scrolling behavior you want, set `.thumbnail-list` to prevent wrapping and allow scrolling in <samp class="filename">styles.css</samp>.

```
...
.thumbnail-list {
  list-style: none;
  padding: 0;

  white-space: nowrap;
  overflow-x: auto;
}
...
```

The `white-space: nowrap` declaration prevents the `.thumbnail-item` elements from wrapping. The `overflow-x: auto` tells the browser that it should add a scrollbar along the horizontal space (the x axis) of the `.thumbnail-list` element to accommodate content that overflows – i.e., does not fit within the `.thumbnail-list`. Without this declaration, you would have to scroll the entire web page to see the additional thumbnails.

Save your file again and take a look at the results in your browser. The thumbnails are now in a single row, and you should be able to scroll through them horizontally ([Figure 4.5](#ch04.html_fig-no-wrap-yes-scroll "Figure 4.5  Horizontally scrolling thumbnails")).

**Figure 4.5  Horizontally scrolling thumbnails**

![Horizontally scrolling thumbnails](Ottergram/Flexbox/img/non-wrapping-thumbnails.png)

This is a good start to the enhanced Ottergram interface. It works just fine for some screen sizes. However, it is not perfect, because it does not adapt well to a wide range of sizes – especially those that are much larger or smaller than the computer you are currently using.

In the next two sections, you will add code that gives Ottergram a more fluid layout and allows its UI - its <samp class="firstterm">user interface</samp> - to shift between different layouts to adapt to ranges of screen sizes.

## Flexbox

You have seen `display` styles specifying the properties `block` and `inline`. Inline elements, like the thumbnail items in your newly scrolling list, are laid out next to one another, while block elements occupy their own horizontal line.

Another way to think of this is that block elements <samp class="emphasis">flow</samp> from top to bottom and inline elements flow from left to right ([Figure 4.6](#ch04s02.html_fig-block-vs-inline "Figure 4.6  Block vs inline elements")).

**Figure 4.6  Block vs inline elements**

![Block vs inline elements](Ottergram/Flexbox/img/block-vs-inline.png)

The `display` property tells the browser how an element should flow in the layout. For blogs or online encyclopedias, the `inline` and `block` values work well. But for application-style layouts like web-based email and social media sites, there is a new CSS specification that allows elements to flow more dynamically. This is the <samp class="firstterm">flexible box model</samp>, or flexbox.

Flexbox CSS properties can ensure that thumbnail and detail areas fill the screen and maintain their proportions relative to one another. This is exactly what you need for Ottergram. You can also use flexbox properties to center the contents of the detail area both horizontally and vertically, a task which is notoriously difficult using standard box model properties.

### Creating a flex container

Before you add your first flexbox property, set your `<html>` and `<body>` elements to `height: 100%` in <samp class="filename">styles.css</samp>. The `<html>` element is the root element of your DOM tree, with the `<body>` as a child element drawn inside of it. Setting the `height` to `100%` for both of them allows the content to fill the browser or device window.

```
@font-face {
  ...
}

html, body {
  height: 100%;
}

body {
  font-size: 10px;
  background: rgb(149, 194, 215);
}
...
```

Notice that you have grouped two selectors, separated by a comma, in this styling rule. Selectors of any type can be combined in this way to set common styles.

Notice also that you now have two styling rules with the `body` element selector. When the browser sees additional styling declarations for a selector, it simply adds to its existing styling information for that selector. In this case, it first sees that the `<body>` should have a `height` of 100% and stores that information. When it reads the next styling rule for the `<body>`, it stores the `background` and `font-size` information along with the `height` style.

Now you are ready to create your first <samp class="firstterm">flex container</samp>. When an element is a flex container, it can control how its child elements (its <samp class="firstterm">flex items</samp>) are laid out. Inside a flex container, the size and placement of flex items occurs along the <samp class="firstterm">main axis</samp> and the <samp class="firstterm">cross axis</samp> ([Figure 4.7](#ch04s02.html_fig-main-cross-axes "Figure 4.7  The main and cross axes of a flex container")).

**Figure 4.7  The main and cross axes of a flex container**

![The main and cross axes of a flex container](Ottergram/Flexbox/img/main-cross-axes.png)

Make your `<body>` element a flex container by adding a `display: flex` declaration to its styling rule in <samp class="filename">styles.css</samp>.

```
...
body {
  display: flex;

  font-size: 10px;
  background: rgb(149, 194, 215);
}
...
```

If you saved now, your browser would display a rather sad-looking Ottergram, as in [Figure 4.8](#ch04s02.html_fig-broken-in-flex-direction-row "Figure 4.8  Flex items laid out along the main axis"). This is because the main axis goes from left to right, laying the flex items (all the children of the `<body>`) out in a row.

**Figure 4.8  Flex items laid out along the main axis**

![Flex items laid out along the main axis](Ottergram/Flexbox/img/broken-in-flex-direction-row.png)

However, you can see that the individual items shrink to accommodate the space, instead of wrapping. That is the first piece of good news. The second piece of good news is that you can fix the layout with just one style. (Well, almost.)

### Changing the flex-direction

To fix the layout, set the `<body>` element’s `flex-direction` to `column` in <samp class="filename">styles.css</samp>:

```
...
body {
  display: flex;
  flex-direction: column;

  font-size: 10px;
  background: rgb(149, 194, 215);
}
...
```

This swaps the main and cross axes for the flex container, as illustrated in [Figure 4.9](#ch04s02.html_fig-main-cross-axes-column "Figure 4.9  Main and cross axes with flex-direction: column").

**Figure 4.9  Main and cross axes with `flex-direction: column`**

![Main and cross axes with flex-direction: column](Ottergram/Flexbox/img/main-cross-axes-column.png)

After changing the `flex-direction` to `column`, Ottergram is back to normal – almost. There is a visual bug in the layout when the browser window is a lot wider than it is tall, shown in [Figure 4.10](#ch04s02.html_fig-missing-thumbnails "Figure 4.10  Missing thumbnails when the page is stretched wide").

**Figure 4.10  Missing thumbnails when the page is stretched wide**

![Missing thumbnails when the page is stretched wide](Ottergram/Flexbox/img/missing-thumbnails.png)

You will remedy this by adding a wrapper element and applying new flexbox properties.

### Grouping elements within a flex item

The `<body>` has three flex items: the `<header>`, the `.thumbnail-list`, and the `.detail-image-container`. No matter what happens during the development (and use) of Ottergram, the `<header>` is not likely to change much in its layout or complexity. It is going to be at the top of the page, displaying text. That is about it.

On the other hand, as you develop Ottergram the `.thumbnail-list` and `.detail-image-container` and their contents may very well change in layout and complexity. Also, changes to one of these items are likely to affect the other.

For these reasons, you are going to group the `.thumbnail-list` and the `.detail-image-container` in their own flex container. To do this, you will wrap them in a `<main>` tag with a class name of `.main-content` ([Figure 4.11](#ch04s02.html_fig-introducing-extra-top-level-flex-item "Figure 4.11  Wrapping the .thumbnail-list and .detail-image-container")).

**Figure 4.11  Wrapping the `.thumbnail-list` and `.detail-image-container`**

![Wrapping the .thumbnail-list and .detail-image-container](Ottergram/Flexbox/img/introducing-extra-top-level-flex-item.png)

Make it so in <samp class="filename">index.html</samp>: Give the `<header>` element the class `main-header`, then wrap the `.thumbnail-list` (`<ul>`) and the `.detail-image-container` (`<div>`) in a `<main>` element with the class `main-content`.

```
...
  <body>
    <header>
    <header class="main-header">
      <h1 class="logo-text">ottergram</h1>
    </header>
    <main class="main-content">
      <ul class="thumbnail-list">
      ...
      </ul>

      <div class="detail-image-container">
        <img class="detail-image" src="img/otter1.jpg" alt="">
        <span class="detail-image-title">Stayin' Alive</span>
      </div>
    </main>
...
```

`.main-header` and `.main-content` are now the two flex items inside the `<body>`.

By wrapping the `.thumbnail-list` and `.detail-image-container` in the `.main-content` element, you are now free to declare a `height` for the `<header>`, leaving the rest of the `<body>`’s vertical space for the `.main-content` to occupy. That way, the space inside of `.main-content` can be distributed to `.thumbnail-list` and `.detail-image-container` without affecting the header.

Save <samp class="filename">index.html</samp>. Now that you have the markup for the two flex items inside the `body`, you can set their sizes relative to one another using the `flex` property.

### The flex shorthand property

A flex container distributes its space to the flex items inside of it. If the flex items do not specify their size along the main axis, then the container distributes the space evenly based on the number of flex items, with each flex item getting the same share of space along the main axis. This is the default, illustrated in [Figure 4.12](#ch04s02.html_fig-flex-equal "Figure 4.12  Equal distribution of space between three flex items").

**Figure 4.12  Equal distribution of space between three flex items**

![Equal distribution of space between three flex items](Ottergram/Flexbox/img/flex-equal.png)

But imagine that one of the three flex items in [Figure 4.12](#ch04s02.html_fig-flex-equal "Figure 4.12  Equal distribution of space between three flex items") is a bit greedier than the others and claims two shares of the total space. In that case, the flex container divides the space along the main axis into four shares. The greedy item occupies two of them (half the space) and the other items get one share each ([Figure 4.13](#ch04s02.html_fig-flex-unequal "Figure 4.13  Unequal distribution of space between three flex items")).

**Figure 4.13  Unequal distribution of space between three flex items**

![Unequal distribution of space between three flex items](Ottergram/Flexbox/img/flex-unequal.png)

In Ottergram, you want the `.main-content` element to be the greedy element, taking up as much space along the main axis as possible. The `.main-header`, on the other hand, should take up as little space as possible.

The `flex` property lets your flex items specify how much of the available space they will take up. It is a shorthand property, as shown in [Figure 4.14](#ch04s02.html_fig-flex-property-shorthand "Figure 4.14  The flex shorthand property and its values").

**Figure 4.14  The `flex` shorthand property and its values**

![The flex shorthand property and its values](Ottergram/Flexbox/img/flex-property-shorthand.png)

We strongly recommend that you use `flex` instead of the individual properties it represents. It protects you from inadvertently leaving a property out and getting unexpected results.

The first value is the one to focus on right now, as it determines how much the flex item can grow. By default flex items do not grow at all. You want that default behavior for your `.main-header`, but not your `.main-content`.

In <samp class="filename">styles.css</samp>, add a declaration block for the `.main-header` class selector, specifying a `flex` shorthand property with default values: `0 1 auto`.

```
...
a {
  text-decoration: none;
}

.main-header {
  flex: 0 1 auto;
}

.logo-text {
  background: white;
  ...
```

The value `0 1 auto` can be read as, “I do not want to grow any larger; I will shrink as needed; please calculate my size for me.” The end result will be that the `.main-header` will take up only as much space as it needs, and no more.

Next, add a declaration block for `.main-content`, setting its `flex` to `1 1 auto`.

```
...
.logo-text {
  ...
}

.main-content {
  flex: 1 1 auto;
}

.thumbnail-item + .thumbnail-item {
  ...
```

The first value in `.main-content`’s `flex` declaration corresponds to the `flex-grow` property. A value of `1` tells the container, “I would like to grow as much as possible.” Because its only sibling has declared that it will <samp class="emphasis">not</samp> grow, the `.main-content` element will grow to take up all the space not needed for the `.main-header`.

The `<body>`’s two flex items, the `.main-header` and the `.main-content` elements, occupy the flexible space according to their needs. Now it is time to adjust the layout of the `.main-content` element.

### Ordering, justifying, and aligning flex items

Flexbox also allows you to subdivide flex items into flex containers. This technique lets you focus on the layers. In a moment, you are going to make your `.main-content` a flex container.

Working with nested flex containers is an exception to the atomic styling approach to creating the look and feel of visual components. Instead of styling the smallest, innermost elements first and then working your way out to the largest elements, when working on a layout with flexbox it is more useful to start with the outermost elements and work your way in.

Here is what you will tackle next. You will change the `.main-content` to a flex container with a vertical main axis. Also, you will specify the `flex` properties for `.main-content`’s flex items so that the `.thumbnail-list` takes the default amount of space and `.detail-image-container` grows to fill the space left over. Finally, you will move the `.thumbnail-list` below the `.detail-image-container` ([Figure 4.15](#ch04s02.html_fig-layout-diagram2 "Figure 4.15  Making .main-content a flex container")).

**Figure 4.15  Making `.main-content` a flex container**

![Making .main-content a flex container](Ottergram/Flexbox/img/main-content-as-flex-container.png)

Make these changes in <samp class="filename">styles.css</samp> by adding `display: flex` and `flex-direction: column` to `.main-content`’s declaration block, adding `flex` properties to `.thumbnail-list`’s declaration block, and writing a new declaration block for the `.detail-image-container` class.

```
...
.main-content {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
}

...

.thumbnail-list {
  flex: 0 1 auto;
  list-style: none;
  padding: 0;

  white-space: nowrap;
  overflow-x: auto;
}

...

.thumbnail-title {
  ...
}

.detail-image-container {
  flex: 1 1 auto;
}

.detail-image {
  ...
```

You might be wondering why you are not defining the heights of the `.thumbnail-list` and `.detail-image-container` boxes with percentages, the way you defined the width of the `.detail-image`. Setting the height of the `.thumbnail-list` at, for example, 25% and the `.detail-image-wrapper` at 75% seems logical – but it would not work the way you intend. The interaction with the `width` property of the `.detail-image` would result in the `.detail-image-container` being much too large, and the `.thumbnail-list` would end up either too small or too large, depending on the window size.

In short, using the `flex` property to set the flex items’ sizes in conjunction with the one fixed size you care about – the width of the `.detail-image` – is the way to go.

Now to move the thumbnail list below the detail image. By default, flex items are drawn in the order that they appear in the HTML. This is known as <samp class="firstterm">source order</samp> and is the main way that developers control the order in which elements are drawn.

One option for moving the detail image up would be to cut and paste the markup for the detail image so that it came before the markup for the `.thumbnail-list` – to change the source order. However, it can also be done using a new flexbox property.

To change the order using flexbox, add an `order` declaration to the `.thumbnail-list` selector in <samp class="filename">styles.css</samp>.

```
...
.thumbnail-list {
  flex: 0 1 auto;
  order: 2;
  list-style: none;
  padding: 0;

  white-space: nowrap;
  overflow-x: auto;
}
...
```

The `order` property can be assigned any integer value. The default value is `0`, which tells the browser to use the source order. Any other values, including negative numbers, tell the browser to draw a flex item before or after other flex items. Giving `.thumbnail-list` the declaration `order: 2` tells the browser to draw it <samp class="emphasis">after</samp> any of its siblings that have a lower value for `order` – such as `.detail-image-container`, which is using the default.

Save <samp class="filename">styles.css</samp> and switch to <samp class="application">Chrome</samp>. You will see that the thumbnails are rendered along the bottom of the page ([Figure 4.16](#ch04s02.html_fig-flexbox-order "Figure 4.16  Changing the order elements are drawn")).

**Figure 4.16  Changing the order elements are drawn**

![Changing the order elements are drawn](Ottergram/Flexbox/img/flexbox-order.png)

Next, you will continue to apply `display: flex` as you work on the layout of the Ottergram UI. So far, you have worked with flex containers that hold only a couple of flex items. Make the `.thumbnail-list` a flex container so that you can further explore what flexbox can offer you.

```
...
.thumbnail-list {
  flex: 0 1 auto;
  order: 2;
  display: flex;
  list-style: none;
  padding: 0;

  white-space: nowrap;
  overflow-x: auto;
}
...
```

Do not panic if you save your changes and see that the thumbnails are rendered oddly, as in [Figure 4.17](#ch04s02.html_fig-janky-otter-thumbnails "Figure 4.17  Otters, askew").

**Figure 4.17  Otters, askew**

![Otters, askew](Ottergram/Flexbox/img/janky-otter-thumbnails.png)

To fix this, replace the `.thumbnail-item`’s `width` declaration with a pair of declarations, one for `min-width` and another for `max-width`. This will remove the variations in size that are causing the strange layout.

You can also remove the declaration block that sets the `margin-top` for `.thumbnail-item + .thumbnail-item` elements. It is no longer needed for this layout.

```
...
.thumbnail-item + .thumbnail-item {
  margin-top: 10px;
}

.thumbnail-item {
  display: inline-block;
  width: 120px;
  min-width: 120px;
  max-width: 120px;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);
}
...
```

Next, you will work with the spacing of the flex items inside of `.thumbnail-list`. In <samp class="filename">styles.css</samp>, add a declaration for `justify-content` to the `.thumbnail-list` selector.

```
...
.thumbnail-list {
  flex: 0 1 auto;
  order: 2;
  display: flex;
  justify-content: space-between;
  list-style: none;
  padding: 0;

  white-space: nowrap;
  overflow-x: auto;
}
...
```

The `justify-content` property lets a flex container control how flex items are drawn on the main axis. You used `space-between` as the value to make sure there is an even amount of spacing around each individual flex item.

There are five different values you can specify for `justify-content`. [Figure 4.18](#ch04s02.html_fig-flex-justification "Figure 4.18  Values for the justify-content property") illustrates how each of these values works.

**Figure 4.18  Values for the `justify-content` property**

![Values for the justify-content property](Ottergram/Flexbox/img/flex-justification.png)

You have tackled the layout of the `.thumbnail-list`. Next, you will work with the `.detail-image-container` and its contents.

### Centering the detail image

The detail image should be Ottergram’s main focus. It should be front and center to make sure that the user is admiring the majesty of the otter. It should also be adorned with a snazzy title.

To center the detail image, you will first wrap the image and its title in a container, then center the <samp class="emphasis">wrapper</samp> inside the `.detail-image-container`. This idea is illustrated in [Figure 4.19](#ch04s02.html_fig-image-frame-centering "Figure 4.19  Framing the .detail-image and .detail-image-title").

**Figure 4.19  Framing the `.detail-image` and `.detail-image-title`**

![Framing the .detail-image and .detail-image-title](Ottergram/Flexbox/img/image-frame-centering.png)

While you could center the `.detail-image` itself inside the `.detail-image-container`, it would be difficult to correctly offset the `.detail-image-title`, because both the `.detail-image` and the `.detail-image-container` are dynamically resizing.

An intermediary wrapper element is a useful technique for this situation. It will constrain the size of the `.detail-image` and serve as a reference for positioning the `.detail-image-title`.

In <samp class="filename">index.html</samp>, begin by adding a `<div>` with the class name `detail-image-frame`:

```
...
      </ul>

      <div class="detail-image-container">
        <div class="detail-image-frame">
          <img class="detail-image" src="img/otter1.jpg" alt="">
          <span class="detail-image-title">Stayin' Alive</span>
        </div>
      </div>
    </main>
  </body>
</html>
```

Save <samp class="filename">index.html</samp>. Now, in <samp class="filename">styles.css</samp>, add a declaration block for `.detail-image-frame` with a single style declaration: `text-align: center`. This is one way to center content without flexbox, but note that it only works horizontally.

```
...
.detail-image-container {
  flex: 1 1 auto;
}

.detail-image-frame {
  text-align: center;
}

.detail-image {
  width: 90%;
}
```

Next, to center the `.detail-image-frame` inside the `.detail-image-container`, update <samp class="filename">styles.css</samp> to make `.detail-image-container` a flex container. Draw its flex items in the center of the main axis (in this case, horizontally – the default) with `justify-content: center`, and add a new flexbox property, `align-items: center`, to draw its flex items in the center of the cross axis (vertically).

```
...
.detail-image-container {
  flex: 1 1 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
...
```

Save your changes and enjoy the proud otter, nobly centered in the `.detail-image-container` ([Figure 4.20](#ch04s02.html_fig-centered-otter "Figure 4.20  After centering .detail-image-frame inside .detail-image-container")).

**Figure 4.20  After centering `.detail-image-frame` inside `.detail-image-container`**

![After centering .detail-image-frame inside .detail-image-container](Ottergram/Flexbox/img/centered-otter.png)

## Absolute and Relative Positioning

Sometimes you need to place an element in an exact spot inside of another element. CSS gives you a way to do this using <samp class="firstterm">absolute positioning</samp>.

You will use absolute positioning to place the `detail-image-title` in the lower left corner of the `.detail-image-frame`, as shown in [Figure 4.21](#ch04s03.html_fig-image-title-absolute-pos "Figure 4.21  Absolutely positioned .detail-image-title").

**Figure 4.21  Absolutely positioned `.detail-image-title`**

![Absolutely positioned .detail-image-title](Ottergram/Flexbox/img/image-title-absolute-pos.png)

There are three requirements for absolute positioning. The absolutely positioned element must have:

*   the property `position: absolute`, to tell the browser to take it out of the <samp class="emphasis">normal flow</samp> rather than laying it out along with its siblings

*   coordinates, provided using one or more of the `top`, `right`, `bottom`, and `left` properties; absolute lengths (such as pixels) or relative lengths (such as percentages) may be used as values

*   an ancestor element with an explicitly declared `position` property with a value of `relative` or `absolute`; this is important – if no ancestor has a declared `position` property, the absolutely positioned element will be placed relative to the `<html>` element (the browser window)

A word of warning: It might be tempting to use `position: absolute` for everything, but it should be used sparingly. A whole layout with absolute positioning is nearly impossible to maintain and will look terrible on any screen size other than the one it was developed for.

When specifying a coordinate, you are really specifying the distance from the edge of the element to the edge of its container, as shown in [Figure 4.22](#ch04s03.html_fig-absolute-positioning "Figure 4.22  Elements are absolutely positioned based on their edges").

**Figure 4.22  Elements are absolutely positioned based on their edges**

![Elements are absolutely positioned based on their edges](Ottergram/Flexbox/img/absolute-positioning.png)

[Figure 4.22](#ch04s03.html_fig-absolute-positioning "Figure 4.22  Elements are absolutely positioned based on their edges") has two examples of absolute positioning. In the first one, the element is positioned so that its top edge is `50px` from its container’s top edge and its left edge is `200px` from its container’s left edge. The second example shows a variation, where the element is positioned by its bottom and left edges.

To position the `.detail-image-title`, start by declaring the `.detail-image-frame` to have `position: relative` in <samp class="filename">styles.css</samp>. You will position the `.detail-image-title` relative to it.

```
...
.detail-image-frame {
  position: relative;
  text-align: center;
}
...
```

You used `position: relative` for `.detail-image-frame` because you want it to remain in normal flow. You also want it to serve as the container for an absolutely positioned descendant, so its `position` property must be explicitly defined.

At the end of <samp class="filename">styles.css</samp>, add a declaration block for the `.detail-image-title` selector. For now, make the title white and set the font size to be four times the default.

```
...
.detail-image {
  width: 90%;
}

.detail-image-title {
  color: white;
  font-size: 40px;
}
```

So far, so good ([Figure 4.23](#ch04s03.html_basic-white "Figure 4.23  Basic text styling for .detail-image-title")). But so basic.

**Figure 4.23  Basic text styling for `.detail-image-title`**

![Basic text styling for .detail-image-title](Ottergram/Flexbox/img/basic-white.png)

For a touch of style, let’s add some text effects to the `.detail-image-title`. When positioning styled text elements, bear in mind that the element’s box may change due to the visual characteristics of a custom typeface or other effects. For this example, you will do all of the text styling for `.detail-image-title` before you set its position. Add a `text-shadow` property to `.detail-image-title` in <samp class="filename">styles.css</samp>.

```
...
.detail-image-title {
  color: white;
  text-shadow: rgba(0, 0, 0, 0.9) 1px 2px 9px;
  font-size: 40px;
}
```

As the name suggests, the `text-shadow` property adds a shadow to text. It accepts a color for the shadow, a pair of lengths for the <samp class="firstterm">offset</samp> (i.e., whether the shadow falls above or below and to the left or right of the text), and a length for the <samp class="firstterm">blur radius</samp> – an optional part of a `text-shadow` declaration that makes the shadow larger and lighter in color as you make the value higher.

You gave your shadow the color attribute `rgba(0, 0, 0, 0.9)` to make it a slightly transparent black. It is offset, or shifted, `1px` to the right and `2px` below the text (negative values would place it to the left or above the text). The last value of `9px` is the blur radius. [Figure 4.24](#ch04s03.html_gotta-have-more-shadow "Figure 4.24  A text-shadow for the .detail-image-title") shows your new shadow.

**Figure 4.24  A `text-shadow` for the `.detail-image-title`**

![A text-shadow for the .detail-image-title](Ottergram/Flexbox/img/gotta-have-more-shadow.png)

Try adjusting the `text-shadow` values in the styles pane of the DevTool’s elements panel to get a feel for how they work ([Figure 4.25](#ch04s03.html_ottergram-exaggerated-text-shadow "Figure 4.25  Exaggerating the text shadow using the DevTools")).

**Figure 4.25  Exaggerating the text shadow using the DevTools**

![Exaggerating the text shadow using the DevTools](Ottergram/Flexbox/img/ottergram-exaggerated-text-shadow.png)

When you are ready, add one last flourish with a custom font. As you did in [Chapter 3](#ch03.html "3 Styles"), add an `@font-face` declaration in <samp class="filename">styles.css</samp> to add the Airstream font to your project. Add a `font-family: airstreamregular` declaration to `.detail-image-title` to put it to use.

```
@font-face {
    font-family: 'airstreamregular';
    src: url('fonts/Airstream-webfont.eot');
    src: url('fonts/Airstream-webfont.eot?#iefix') format('embedded-opentype'),
         url('fonts/Airstream-webfont.woff') format('woff'),
         url('fonts/Airstream-webfont.ttf') format('truetype'),
         url('fonts/Airstream-webfont.svg#airstreamregular') format('svg');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'lakeshore';
    ...
}

...

.detail-image-title {
  font-family: airstreamregular;
  color: white;
  text-shadow: rgba(0, 0, 0, 0.9) 1px 2px 9px;
  font-size: 40px;
}
```

So far, so stylish ([Figure 4.26](#ch04s03.html_fig-so-slick "Figure 4.26  I gotta have more fancy"))!

**Figure 4.26  I gotta have more fancy**

![I gotta have more fancy](Ottergram/Flexbox/img/so-slick.png)

Now that you have finished the styling of `.detail-image-title`, give it a `position: absolute` declaration so that the browser will place it at a precise location within `.detail-image-frame`. Specify that location with `bottom: -16px` and `left: 4px`, to put it just <samp class="emphasis">below</samp> the bottom edge of `.detail-image-frame` and a little bit inside the left edge of `.detail-image-frame`. (Negative values are fine for the coordinates.)

```
...
.detail-image-title {
  position: absolute;
  bottom: -16px;
  left: 4px;

  font-family: airstreamregular;
  color: white;
  text-shadow: rgba(0, 0, 0, 0.9) 1px 2px 9px;
  font-size: 40px;
}
```

Save <samp class="filename">styles.css</samp>, and you will see in the browser that the `.detail-image-title` now sits below and near the left of the otter photo. You now have a positively chic Ottergram in your browser ([Figure 4.27](#ch04s03.html_fig-final-countdown "Figure 4.27  Hello, gorgeous!")).

**Figure 4.27  Hello, gorgeous!**

![Hello, gorgeous!](Ottergram/Flexbox/img/final-countdown.png)

Take a step back to enjoy the fruits of your labor. Ottergram has a dynamic, fluid layout thanks to the addition of flexbox to your styles. In the next chapter you will make the layout adapt to different browser window sizes.

# <samp class="chapter_number">5</samp>
<samp class="chapter_name">Adaptive Layouts with Media Queries</samp>

In this chapter, you will explore a technique for turning styles on and off based on the size of the browser window and other characteristics. You will provide an alternate layout for larger screens using a minimal amount of code. The browser will be able to switch between the different layouts in real time, as the browser window changes size – without reloading the page. [Figure 5.1](#ch05.html_fig-layout-side-by-side "Figure 5.1  Two Ottergram layouts") shows the original layout and the alternate layout.

**Figure 5.1  Two Ottergram layouts**

![Two Ottergram layouts](Ottergram/Media-Queries/img/layout-side-by-side.png)

The industry term for this behavior is <samp class="firstterm">responsive website</samp>. Unfortunately, this term is often a point of confusion. Some think that it means “fast website” or “website with visual animations.” We prefer to call it an <samp class="firstterm">adaptive layout</samp>.

There are several ways of including alternate styles to be used based on the current browser conditions. The recommended approach is to write your styles for the smallest screen and then provide override styles in <samp class="firstterm">media queries</samp> that are triggered when the <samp class="firstterm">viewport</samp> – the browser’s viewable area – is larger than a set threshold.

On a traditional browser (like the one you are using while developing Ottergram), the viewport is the area shown by the browser window. This is pretty intuitive. On a mobile browser, it gets more complicated. Mobile browsers have multiple viewports, and each one plays a role in how a page is rendered.

Front-end developers need to focus on the <samp class="firstterm">layout viewport</samp> (sometimes called the <samp class="firstterm">actual viewport</samp>). The layout viewport tells the browser, “Pretend that I’m actually 980 pixels wide and then draw the page.”

Users are more concerned with a mobile browser’s <samp class="firstterm">visual viewport</samp>. This is the thing that they can pinch to zoom in and out on a page ([Figure 5.2](#ch05.html_fig-viewport-1 "Figure 5.2  Visual viewport vs layout viewport")).

**Figure 5.2  Visual viewport vs layout viewport**

![Visual viewport vs layout viewport](Ottergram/Media-Queries/img/viewport-1.png)

If you viewed Ottergram on your smartphone right now, you would see something like [Figure 5.2](#ch05.html_fig-viewport-1 "Figure 5.2  Visual viewport vs layout viewport"), with the browser zoomed in on the upper-left corner of the page. Needless to say, even though a mobile user can zoom out manually, you do not want Ottergram to behave like this by default.

Earlier we mentioned that you are taking a mobile-first approach to developing Ottergram. That was mostly true. Your markup and styles were written in a mobile-friendly way – using a minimal amount of markup and styling the smallest elements first. Now, you just need to give the browser information about the layout viewport it should use.

## Resetting the Viewport

In [Chapter 3](#ch03.html "3 Styles") you added <samp class="filename">normalize.css</samp> to Ottergram. This ensured that any browser viewing Ottergram would have the same set of default styles. On top of these defaults, you could confidently add your own CSS, knowing it would work consistently from browser to browser.

You will do something similar for the layout viewport. Just as every browser may have a different user agent stylesheet, every browser may have a different default layout viewport. However, unlike using <samp class="filename">normalize.css</samp>, you are not going to reset the viewport for all browsers to the same value. Instead, you will use a `<meta>` tag to tell all browsers to display Ottergram at the best size for the device’s physical screen.

In <samp class="filename">index.html</samp>, add a `<meta>` tag that tells the browser that the `width` of the layout viewport is the same as the device’s screen width. Make sure to set the zoom to 100% by setting the `initial-scale` to `1`.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/normalize/3.0.3/normalize.min.css">
    <link rel="stylesheet" href="stylesheets/styles.css">
    <title>Ottergram</title>
  </head>
...
```

Save your changes. This technique sets the layout viewport to the <samp class="firstterm">ideal viewport</samp>. The ideal viewport is best viewport size for a specific device, as recommended by the browser maker. This varies significantly, since there are many, many different devices and quite a number of different browsers.

[Table 5.1](#ch05.html_tab-viewports "Table 5.1  Summary of the different viewports") summarizes the different types of viewports.

**Table 5.1  Summary of the different viewports**

| Viewport | Description | Device |
| --- | --- | --- |
| viewport | The area equal to the browser’s window. It serves as the `<html>` element’s container. | desktop, laptop |
| layout viewport | A virtual screen, larger than the actual device screen, used for calculating the page layout. | mobile |
| visual viewport | The zoomable area that a user can see on a device’s screen. Zooming has no effect on the page layout. | mobile |
| ideal viewport | The optimal dimensions for a specific browser on a specific device. | mobile |

Start `browser-sync` and make sure the DevTools are open in <samp class="application">Chrome</samp>. Look to the left of the <samp class="guimenuitem">Elements</samp> menu item and find the <samp class="guibutton">Toggle Device Mode</samp> button, which looks like this: ![Summary of the different viewports](Ottergram/Media-Queries/img/toggle-device-mode-button.png). It is shown in context in [Figure 5.3](#ch05.html_fig-responsive-testing-tool "Figure 5.3  Toggle Device Mode button").

**Figure 5.3  Toggle Device Mode button**

![Toggle Device Mode button](Ottergram/Media-Queries/img/responsive-testing-tool.png)

Click this button to activate <samp class="firstterm">device mode</samp>. You will see that the web page view now shows Ottergram on a simulated smartphone screen. There is a menu for choosing between different screen sizes based on popular devices. You can also click the gray bar below the presets to toggle between small, medium, and large screen sizes. And there is a menu for quickly choosing a screen orientation of landscape or portrait. [Figure 5.4](#ch05.html_fig-device-mode-tools "Figure 5.4  Using device mode for responsive testing") shows a screenshot of the device mode at the time of this writing. Yours may look quite different, as the DevTools undergo regular updates.

**Figure 5.4  Using device mode for responsive testing**

![Using device mode for responsive testing](Ottergram/Media-Queries/img/device-mode-tools.png)

You can see that, thanks to your new `<meta>` element, Ottergram displays well on a small screen, such as a smartphone. For devices with larger screens, such as tablets or laptops, a slightly different layout may be more appropriate. Next, you will apply different layout styles using a combination of flexbox and media queries.

Click the ![Using device mode for responsive testing](Ottergram/Media-Queries/img/toggle-device-mode-button.png) button again to deactivate device mode before you continue.

## Adding a Media Query

Media queries let you group CSS declaration blocks and specify the conditions under which they should be applied. Those conditions may be something like “if the screen is at least 640 pixels wide” or “if the screen is wider than it is tall and has a high pixel density.”

The syntax begins with `@media`, followed by the conditions to be matched. Next is a set of curly braces that wraps around entire declaration blocks. Let’s see what this looks like.

Begin your first media query at the end of <samp class="filename">styles.css</samp>. You will create a media query that will activate styles when being viewed on any kind of device when the viewport is at least 768 pixels wide, which is a common device width for tablets.

```
...
.detail-image-title {
  ...
}

@media all and (min-width: 768px) {
  /* Styles will go here */
}
```

`@media` is followed by the <samp class="firstterm">media type</samp> `all`. Media types were originally intended to differentiate between devices, such as smart televisions and handheld devices. Unfortunately, browsers do not implement this accurately, so you should always specify `all`. The only time you might not use `all` is when you want to specify styles for printing, when you can safely use the media type `print`.

After the media type, you write the conditions for applying the styles. Here, you are using the useful condition `min-width`. You can see that conditions look similar to style declarations.

To achieve the effect shown in [Figure 5.1](#ch05.html_fig-layout-side-by-side "Figure 5.1  Two Ottergram layouts"), you will need to change the `flex-direction` of the `.main-content` element. This will let the thumbnails and the detail image sit next to one another. You do not want the thumbnails to cause the browser to scroll. Instead, they should continue to scroll independently of the browser window. For that, you will add `overflow: hidden`.

Add those styles to your media query at the end of <samp class="filename">styles.css</samp>.

```
...
@media all and (min-width: 768px) {
  /* Styles will go here */
  .main-content {
    flex-direction: row;
    overflow: hidden;
  }
}
```

You would be in for a shock if you saved and then stretched your browser wide enough to trigger your media query. At the moment, your page looks like [Figure 5.5](#ch05s02.html_fig-terrible "Figure 5.5  Otters in disarray"). Not to worry. You will fix this with only a few more lines of code.

**Figure 5.5  Otters in disarray**

![Otters in disarray](Ottergram/Media-Queries/img/terrible.png)

The thumbnails need to be displayed in a column instead of a row. This is easy to do, because you used flexbox for laying them out. Add a declaration block inside the body of the media query in <samp class="filename">styles.css</samp> setting `.thumbnail-list`’s `flex-direction` to `column`.

```
...
@media all and (min-width: 768px) {
  .main-content {
    flex-direction: row;
    overflow: hidden;
  }

  .thumbnail-list {
    flex-direction: column;
  }
}
```

Save <samp class="filename">styles.css</samp>. That has improved things significantly ([Figure 5.6](#ch05s02.html_fig-better "Figure 5.6  After setting flex-direction to column"))!

**Figure 5.6  After setting `flex-direction` to `column`**

![After setting flex-direction to column](Ottergram/Media-Queries/img/better.png)

According to your design, the thumbnails should go on the left. You can solve this by changing `.thumbnail-list`’s `order`. Earlier, you set it to `2` so that it would be drawn after the `.detail-image-container`. Now, set it to `0` within the media query in <samp class="filename">styles.css</samp> so that it follows the source order and is drawn before the `.detail-image-container`.

```
...
@media all and (min-width: 768px) {
  .main-content {
    flex-direction: row;
    overflow: hidden;
  }

  .thumbnail-list {
    flex-direction: column;
    order: 0;
  }
}
```

Save your changes and confirm that the thumbnails are drawn on the left side of the page.

You are almost there! Add a few more styles in <samp class="filename">styles.css</samp> for the `.thumbnail-list` and `.thumbnail-item`s to make the sizing and spacing a little nicer.

```
...
@media all and (min-width: 768px) {
  .main-content {
    flex-direction: row;
    overflow: hidden;
  }

  .thumbnail-list {
    flex-direction: column;
    order: 0;
    margin-left: 20px;
  }

  .thumbnail-item {
    max-width: 260px;
  }

  .thumbnail-item + .thumbnail-item {
    margin-top: 20px;
  }
}
```

Once again, save <samp class="filename">styles.css</samp> and switch to your browser. Your layout now looks sharp whether the viewport is narrower or wider ([Figure 5.7](#ch05s02.html_fig-double-otter-responsive "Figure 5.7  Responsive otters")).

**Figure 5.7  Responsive otters**

![Responsive otters](Ottergram/Media-Queries/img/double-otter-responsive.png)

Ottergram is making steady progress! You have created a good-looking website with a layout that can adapt to many screen sizes. In the next chapter, you will begin using JavaScript to add a layer of interactivity to Ottergram.

## Bronze Challenge: Portrait

Your current media query changes the layout based on the width of the viewport. You could look at this in a different way. One is for viewports that are taller than they are wide, and the other is for viewports that are wider than they are tall. These are two <samp class="firstterm">orientation</samp> modes that your viewport can be in.

Check MDN’s documentation for media queries and update your media query so that the layout changes according to orientation and not based on width.

## For the More Curious: Common Solutions (and Bugs) with Flexbox Layouts

Philip Walton is a developer who maintains two very important flexbox resources. The first is the Solved by Flexbox site ([<samp class="uri">philipwalton.github.io/​solved-by-flexbox</samp>](https://philipwalton.github.io/solved-by-flexbox/)), which offers demos of common layouts implemented using flexbox and all the information you need to create them yourself. Some of the layouts are very difficult to achieve without flexbox.

The second resource is the Flexbugs page at [<samp class="uri">github.com/​philipwalton/​flexbugs</samp>](https://github.com/philipwalton/flexbugs). Flexbox is wonderful, but it is not perfect. Flexbugs provides solutions and workarounds for common problems that developers run into when using flexbox. The information is provided by members of the development community who have encountered these bugs, and the list is well maintained.

## Gold Challenge: Holy Grail Layout

Be sure to make a copy of your code before attempting this challenge! It will require significant changes to the markup and styles. Use your copy for working on the challenge and leave the original intact for starting the next chapter.

Using Solved by Flexbox as a reference, implement the Holy Grail layout in Ottergram. Create a second navigation bar with thumbnails, but place it on the other side of the viewport.

Make sure to add a footer element to the bottom of your page. Use the `<footer>` tag and put an `<h1>` inside of it.

# <samp class="chapter_number">6</samp>
<samp class="chapter_name">Handling Events with JavaScript</samp>

You know what is cool about otters? Among other things, they hold hands when they sleep so that they do not float away. Keep this image in mind as you learn to work with event callbacks in JavaScript.

JavaScript is a programming language that adds interactivity to websites by manipulating DOM elements and CSS styles on a page. It was originally created for use by people who were not professional programmers. It has grown in power and popularity and is now used for many kinds of application development. When you use sites like Gmail or Netflix, you are interacting with programs written in JavaScript. In fact, the <samp class="application">Atom</samp> text editor is actually a desktop application written in JavaScript.

Despite its power and widespread use, it has its quirks, like any programming language. As you continue working on Ottergram and the other projects in this book, you will learn to navigate the rough patches of the language and to take advantage of its best parts.

There are several versions of JavaScript, and you will use three of them for the projects in this book. They are all revisions of a standard specification known as ECMAScript (or “ES”). [Table 6.1](#ch06.html_tab-js-versions "Table 6.1  JavaScript versions used in this book") summarizes them.

**Table 6.1  JavaScript versions used in this book**

| ECMAScript Edition | Release Date | Notes |
| --- | --- | --- |
| 3 | December 1999 | Most widely supported version; encompasses most of the language features you will use, such as variables, types, and functions. |
| 5 | December 2009 | Backward compatible, with opt-in enhancements such as a <samp class="firstterm">strict mode</samp> that prevents the usage of the more error-prone parts of the language. |
| 6 | June 2015 | Includes new syntax and language features; at the time of this writing, most browsers do not yet support ES6, but ES6 code can be translated into ES5, making it usable by most browsers. |

In this chapter, you will use JavaScript to make Ottergram interactive: The detail image and detail title will change when the user clicks or taps one of the thumbnails.

To do this, you are going to write a JavaScript <samp class="firstterm">function</samp> – a set of steps for the browser to follow – that reads the URL for an image and shows it in the detail area. Then you will ensure that this function is run when a thumbnail is clicked. You will also write a separate function that hides the detail area and run that function when the Escape key is pressed.

At the end of the chapter, Ottergram will be able to feature any otter in the detail image ([Figure 6.1](#ch06.html_fig-finito "Figure 6.1  Clicking thumbnails changes detail image and title")).

**Figure 6.1  Clicking thumbnails changes detail image and title**

![Clicking thumbnails changes detail image and title](Ottergram/Functions/img/finito.png)

As you write these functions, you will interact with the page using a set of predefined interfaces built into the browser. There are a large number of them, and the code will only walk you through the ones necessary for the task at hand. If you are curious, you can find more in-depth information about them on the MDN at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​API/​Element</samp>](https://developer.mozilla.org/en-US/docs/Web/API/Element).

## Preparing the Anchor Tags for Duty

Before you start adding interactive features with JavaScript, you need to make a few updates to the markup. Your thumbnail images are wrapped in anchor tags, but those tags do not actually link to any resource. Instead, they use the `#` value for the `href` attribute, which tells the browser to stay on the same page. In order to make a click on a thumbnail do anything interesting, you need to fix that.

First, in <samp class="filename">index.html</samp>, remove all but five of the `.thumbnail-item` elements. You no longer need the duplicates, because your layout is in good shape.

Then, change the anchor tags’ `href` properties to no longer use the dummy value `#`. Instead, set the values to be the same as each `<img>` tag’s `src` value.

<samp class="application">Atom</samp> can help you make these changes, taking the tedium out of working with HTML. Like any text editor, it has a way to find and replace text. Select <samp class="guimenu">Find</samp> → <samp class="guimenuitem">Find in Buffer</samp> or use the keyboard shortcut Command-F (Ctrl-F). This will open the <samp class="guilabel">Find in Buffer</samp> panel at the bottom of the editor window ([Figure 6.2](#ch06.html_fig-atom-find-replace "Figure 6.2  Using Atom’s find-and-replace feature")).

**Figure 6.2  Using Atom’s find-and-replace feature**

![Using Atom’s find-and-replace feature](Ottergram/Functions/img/atom-find-replace.png)

Enter “#” in the <samp class="guilabel">Find in current buffer</samp> text box and “img/otter.jpg” in the <samp class="guilabel">Replace in current buffer</samp> text box. Then click <samp class="guibutton">Replace All</samp> in the lower right.

This will change all of the `<a href="#">` tags to `<a href="img/otter.jpg">`. Now it is just a matter of manually adding the appropriate number to each one (`img/otter1.jpg`, `img/otter2.jpg`, etc.).

Press the Escape key to close the <samp class="guilabel">Find in Buffer</samp> panel. <samp class="filename">index.html</samp> should look like this:

```
...
      <ul class="thumbnail-list">
        <li class="thumbnail-item">
          <a href="#">
          <a href="img/otter1.jpg">
            <img class="thumbnail-image" src="img/otter1.jpg" alt="">
            <span class="thumbnail-title">Barry</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="#">
          <a href="img/otter2.jpg">
            <img class="thumbnail-image" src="img/otter2.jpg" alt="">
            <span class="thumbnail-title">Robin</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="#">
          <a href="img/otter3.jpg">
            <img class="thumbnail-image" src="img/otter3.jpg" alt="">
            <span class="thumbnail-title">Maurice</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="#">
          <a href="img/otter4.jpg">
            <img class="thumbnail-image" src="img/otter4.jpg" alt="">
            <span class="thumbnail-title">Lesley</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="#">
          <a href="img/otter5.jpg">
            <img class="thumbnail-image" src="img/otter5.jpg" alt="">
            <span class="thumbnail-title">Barbara</span>
          </a>
        </li>
      </ul>
...
```

Next, you need to add additional properties to your anchor elements so you can access them using JavaScript. When styling with CSS, you use class name selectors to refer to elements on the page. For JavaScript, you use <samp class="firstterm">data attributes</samp>.

Data attributes are just like the other HTML attributes you have been using except that, unlike attributes such as `src` or `href`, data attributes do not have special meaning to the browser. The only requirement is that the attribute name starts with `data-`. Using custom data attributes lets you designate what HTML elements on the page your JavaScript interacts with.

Technically, in JavaScript, you could access elements on the page using class names. Likewise, you could use data attributes in your selectors for styling. But you really should not. Your code will be much more maintainable if your JavaScript and your CSS do not rely on the same attributes.

Update your anchor tags in <samp class="filename">index.html</samp> with data attributes. Note that the line breaks in the code below have been added to make sure that everything fits nicely on the page. You are free to add them or not, as you prefer. They will not make a difference to the browser.

```
...
        <li class="thumbnail-item">
          <a href="img/otter1.jpg" data-image-role="trigger"
                                   data-image-title="Stayin' Alive"
                                   data-image-url="img/otter1.jpg">
            <img class="thumbnail-image" src="img/otter1.jpg" alt="">
            <span class="thumbnail-title">Barry</span>
          </a>
        </li>
          <li class="thumbnail-item">
            <a href="img/otter2.jpg" data-image-role="trigger"
                                     data-image-title="How Deep Is Your Love"
                                     data-image-url="img/otter2.jpg">
            <img class="thumbnail-image" src="img/otter2.jpg" alt="">
            <span class="thumbnail-title">Robin</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="img/otter3.jpg" data-image-role="trigger"
                                   data-image-title="You Should Be Dancing"
                                   data-image-url="img/otter3.jpg">
            <img class="thumbnail-image" src="img/otter3.jpg" alt="">
            <span class="thumbnail-title">Maurice</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="img/otter4.jpg" data-image-role="trigger"
                                   data-image-title="Night Fever"
                                   data-image-url="img/otter4.jpg">
            <img class="thumbnail-image" src="img/otter4.jpg" alt="">
            <span class="thumbnail-title">Lesley</span>
          </a>
        </li>
        <li class="thumbnail-item">
          <a href="img/otter5.jpg" data-image-role="trigger"
                                   data-image-title="To Love Somebody"
                                   data-image-url="img/otter5.jpg">
            <img class="thumbnail-image" src="img/otter5.jpg" alt="">
            <span class="thumbnail-title">Barbara</span>
          </a>
        </li>
...
```

Add data attributes for the detail image, as well:

```
...
      <div class="detail-image-container">
        <div class="detail-image-wrapper">
    <img class="detail-image" data-image-role="target" src="img/otter1.jpg" alt="">
    <span class="detail-image-title" data-image-role="title">Stayin' Alive</span>
        </div>
      </div>
...
```

Your JavaScript code can refer to these data attributes to access specific elements on the page because the browser lets you use JavaScript to make queries about the contents of a web page. For example, you can query for any elements that match a selector, such as `data-image-role="trigger"`. If the query finds matches, it will return <samp class="firstterm">references</samp> to the matching elements.

When you have a reference to an element, you can do all sorts of things with the element. You can read or change the values of its attributes, change the text inside of it, and even get access to the elements around it. When you make changes to an element using a reference, the browser updates the page immediately.

In this chapter, you will write JavaScript code that will get references to the anchor and detail image elements, read the values from the anchor’s data attributes, and then change the value of the detail image’s `src` attribute. This is how you will make Ottergram interactive.

You may have noticed that the anchor tags and the detail image’s `<img>` tag all have a `data-image-role` attribute, but their values are different.

Using the same data attribute names for the anchor and `<img>` tags is not required, but it is a good practice. It reminds you, the developer, that these elements will be part of the same JavaScript behavior.

One last change is needed in your HTML before you begin work on your JavaScript: You need to tell the HTML to run the JavaScript. Do this by adding a `<script>` tag in <samp class="filename">index.html</samp>. This `<script>` tag will refer to the file <samp class="filename">scripts/main.js</samp>, which you will create in just a moment.

```
...
        </div>
      </div>
    </main>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

When the browser sees a `<script>` tag, it begins running the code in the referenced file immediately. JavaScript cannot access an element within your HTML before it has been rendered by the browser, so putting the `<script>` tag at the bottom of the `body` ensures that your JavaScript does not run until after all the markup has been parsed.

Your HTML is now ready to connect with the JavaScript you are about to write. Be sure to save <samp class="filename">index.html</samp> before you move on.

## Your First Script

Time to create a <samp class="filename">scripts</samp> folder and the <samp class="filename">main.js</samp> file. Recall that you can create folders from within the <samp class="application">Atom</samp> editor. Control-click (right-click) <samp class="filename">ottergram</samp> in the lefthand panel and click <samp class="guimenuitem">New Folder</samp> in the pop-up. Enter the name <samp class="filename">scripts</samp> in the prompt that appears.

Then, Control-click (right-click) <samp class="filename">scripts</samp> in the lefthand panel and choose <samp class="guimenuitem">New File</samp>. The prompt will pre-fill the text <samp class="filename">scripts/</samp>. After this, enter <samp class="filename">main.js</samp> and press Return.

Make sure your folder structure looks like [Figure 6.3](#ch06s02.html_fig-functions-file-structure "Figure 6.3  Ottergram folder structure").

**Figure 6.3  Ottergram folder structure**

![Ottergram folder structure](Ottergram/Functions/img/functions-file-structure.png)

The name <samp class="filename">main.js</samp> does not have any special significance for the browser, but it is a common convention used by many front-end developers.

One last thing before you dive into JavaScript. You need to start `browser-sync`, and to do so you need to change the command you have been using slightly:

```
browser-sync start --server --browser "Google Chrome"
                   --files "*.html, stylesheets/*.css, scripts/*.js"
```

You added the path `scripts/*.js` to the list of files so that `browser-sync` will watch for changes to the JavaScript as well as the HTML and CSS.

## Overview of the JavaScript for Ottergram

Before you start coding, it is always good to have a plan. Here is the plain English version of what you need to do with Ottergram.

1.  Get all the thumbnails.

2.  Listen for a click on each one.

3.  If a click occurs, update the detail image with info from that thumbnail.

You can break down #3 into three subparts:

1.  Get the image URL from the thumbnail’s data attribute.

2.  Get the title text from the thumbnail’s data attribute.

3.  Set the image and title on the detail image.

Here is that same plan expressed as a diagram ([Figure 6.4](#ch06s03.html_fig-process-diagram "Figure 6.4  Plan of attack for Ottergram"))

**Figure 6.4  Plan of attack for Ottergram**

![Plan of attack for Ottergram](Ottergram/Functions/img/process-diagram.png)

This chapter will walk you through creating the code starting with the last step. This is the “bottom-up” approach, and it works well when writing JavaScript.

## Declaring String Variables

Your first JavaScript task is to create string variables for each of the data attributes you added to the markup. (If those are unfamiliar terms, do not worry – we will explain in just a moment.)

At the top of <samp class="filename">main.js</samp>, start by adding a variable named `DETAIL_IMAGE_SELECTOR` and assigning it the string `'[data-image-role="target"]'`.

```
var DETAIL_IMAGE_SELECTOR = '[data-image-role="target"]';
```

This might not be much code, but it is worth a closer look. Let’s start in the middle, with the `=` symbol. This is the <samp class="firstterm">assignment operator</samp>. Unlike in mathematics, the `=` symbol in JavaScript does not mean that two things are equal. Instead, it means “Take the value on the righthand side and give it the name on the lefthand side.”

On the righthand side of this particular assignment is a <samp class="firstterm">string</samp> of text: `'[data-image-role="target"]'`. A string is just a sequence of characters representing text, and it is delimited by single quotation marks. The text inside the single quotes happens to be the attribute selector for your detail image. This is a clue that you will use this string to access that element.

On the lefthand side of the assignment is a <samp class="firstterm">variable declaration</samp>. It may be useful to think of a variable as a label that you can use to refer to some value, which could be a numeric value, a string (as in this case), or some other type of value. Using the `var` keyword, you are creating a variable named `DETAIL_IMAGE_SELECTOR`.

Next, declare variables in <samp class="filename">main.js</samp> for the detail title selector and the thumbnail anchor selector. Assign the strings for these selectors as well.

```
var DETAIL_IMAGE_SELECTOR = '[data-image-role="target"]';
var DETAIL_TITLE_SELECTOR = '[data-image-role="title"]';
var THUMBNAIL_LINK_SELECTOR = '[data-image-role="trigger"]';
```

As the name <samp class="firstterm">variable</samp> suggests, their values can be reassigned – they can vary. Writing variable names in all capital letters is a convention that developers sometimes use when the values should not change. Other languages have <samp class="firstterm">constants</samp> that serve this purpose. JavaScript is in transition: ES5 does not have constants; ES6 does – but, as we said earlier, it is not yet fully supported. Until constants become well supported, you can follow this convention to label a value that should not change.

As an aside, strings can be delimited by single or double quotes. You are free to use either, but this book will use single quotes as a convention and we suggest that you follow along at least for the projects in this book.

If you want to use double quotes, you have to <samp class="firstterm">escape</samp> any double quotes that are part of the string so that the browser does not incorrectly parse them as part of the code. To escape a character, you precede it with a backslash, like this:

```
var DETAIL_IMAGE_SELECTOR = "[data-image-role=\"target\"]";
```

Using single quotes is not a guarantee that you will not need to escape characters. If a string delimited by single quotes contains single quotes – or apostrophes – you have to escape them.

Save <samp class="filename">main.js</samp>. With these variables in hand, let’s take them for a spin in <samp class="application">Chrome</samp>’s DevTools.

## Working in the Console

One of the most useful parts of the DevTools is the console, which lets you enter JavaScript code and evaluate it immediately. This is especially useful for iteratively developing JavaScript code that makes changes to a page.

In the DevTools, click on the <samp class="guilabel">Console</samp> tab, to the right of the <samp class="guilabel">Elements</samp> tab ([Figure 6.5](#ch06s05.html_fig-console-tab-next-to-elements "Figure 6.5  Choosing the console tab")).

**Figure 6.5  Choosing the console tab**

![Choosing the console tab](Ottergram/Functions/img/console-tab-next-to-elements.png)

The console has a prompt where you can enter lines of code. Click to the right of the ![Choosing the console tab](Ottergram/Functions/img/console-prompt-arrow.png) symbol so that the console is ready for input ([Figure 6.6](#ch06s05.html_fig-console-prompt "Figure 6.6  The console, ready for input")).

**Figure 6.6  The console, ready for input**

![The console, ready for input](Ottergram/Functions/img/console-prompt.png)

Type the following math expression into the console:

```
137 + 349
```

Press the Return key. The console will print out the result ([Figure 6.7](#ch06s05.html_fig-math-1 "Figure 6.7  Evaluating a math expression")).

**Figure 6.7  Evaluating a math expression**

![Evaluating a math expression](Ottergram/Functions/img/math-1.png)

The console’s main job is to tell you, in the simplest terms, the value of the code you enter.

As with many things in life, order matters. If you need certain items to be evaluated as a group, you can wrap parentheses around them. (This is much easier than memorizing the order in which JavaScript would do this without the parentheses.) Enter the following expression in the console.

```
3 * ( (2 * 4) + (3 + 5) )
```

Press the Return key, and the console will crunch the numbers in the correct order ([Figure 6.8](#ch06s05.html_fig-math-2 "Figure 6.8  Evaluating a more complex math expression")). (By the way, although we have added spaces between the numbers and operators for the sake of readability, you do not need to include them. The console does not care.)

**Figure 6.8  Evaluating a more complex math expression**

![Evaluating a more complex math expression](Ottergram/Functions/img/math-2.png)

Now, on to using your variables. You can clear the contents of the console by pressing the ![Evaluating a more complex math expression](Ottergram/Functions/img/clear-console.png) icon in the upper left of the console panel or with the keyboard shortcut Command-K (Ctrl-K).

Start typing `DETAIL_IMAGE_SELECTOR`. As you type the first few letters, you can see that the console already knows about the variables you created and provides a list of autocomplete suggestions ([Figure 6.9](#ch06s05.html_fig-console-autocomplete-menu "Figure 6.9  The console’s autocomplete menu")).

**Figure 6.9  The console’s autocomplete menu**

![The console’s autocomplete menu](Ottergram/Functions/img/console-autocomplete-menu.png)

Press the Tab key and let the console autocomplete the variable name for you. When you press the Return key, the console reports that the value of `DETAIL_IMAGE_SELECTOR` is the string `"[data-image-role="target"]"`.

**Figure 6.10  The console printing a variable’s value**

![The console printing a variable’s value](Ottergram/Functions/img/variable-value-printed-to-console.png)

(The console always prints strings with double quotes, even though you actually used single quotes in <samp class="filename">main.js</samp>.)

Strings are one of five <samp class="firstterm">primitive</samp> value types in JavaScript. (Numbers and Booleans are two of the others.) They are “primitive” because they represent simple values. This is in contrast to more complex values in JavaScript, which you will learn about next.

## Accessing DOM Elements

You have just seen that the console gives you access to the variables you created. Earlier we said that these variables could be used for accessing elements on the page. You can try that now. Enter the following in the console:

```
document.querySelector(DETAIL_IMAGE_SELECTOR);
```

Press the Return key. It will show you the HTML for the detail image. Hover over this HTML in the console. You will see that the detail image is highlighted on the page, just as if you clicked HTML in the elements panel ([Figure 6.11](#ch06s06.html_fig-console-dom-query-hover "Figure 6.11  HTML in the console corresponds to an element on the page")).

**Figure 6.11  HTML in the console corresponds to an element on the page**

![HTML in the console corresponds to an element on the page](Ottergram/Functions/img/console-dom-query-hover.png)

In the line of code you wrote on the console, the word `document` is the variable built into the browser that gives you access to the web page. Its value is not one of the primitive types. It is a complex value, whose type is <samp class="firstterm">object</samp>.

The `document` object corresponds to the entire page. It gives you access to a number of <samp class="firstterm">methods</samp> for getting references to elements on the page. Methods are a type of function (they are functions with an explicitly designated owner, but you do not need to worry about that detail right now) – a list of steps for the browser to follow. You used the <samp class="methodname">querySelector</samp> method in the line you entered in the console. The <samp class="firstterm">dot operator</samp> (i.e., the period) in <samp class="methodname">document.querySelector</samp> is how you access an object’s methods.

You asked the `document` to use its <samp class="methodname">querySelector</samp> method to find any element matching the string `'[data-image-role="target"]'`. <samp class="methodname">querySelector</samp> responded with a reference to the element that it found, the detail image ([Figure 6.12](#ch06s06.html_fig-document-and-qs-correspondence "Figure 6.12  Access to the page provided by document and document.querySelector")).

**Figure 6.12  Access to the page provided by `document` and `document.querySelector`**

![Access to the page provided by document and document.querySelector](Ottergram/Functions/img/document-and-qs-correspondence.png)

And now, a bit of terminology. You did not really “ask” the page for matching elements. You <samp class="emphasis">called</samp> the `document`’s <samp class="methodname">querySelector</samp> method and you <samp class="firstterm">passed</samp> it a string. The method <samp class="firstterm">returned</samp> a reference to the detail image element.

When you call a method, you are making it run whatever task it was designed to perform. You will often need to pass it information it needs to do that task, which you place in parentheses after the method’s name. Then, in addition to its assigned tasks, the method may return a value that you can use.

Remember that <samp class="varname">DETAIL_IMAGE_SELECTOR</samp> was assigned the value `'[data-image-role="target"]'`, which means that this is what is passed to <samp class="methodname">querySelector</samp>.

Behind the scenes, <samp class="methodname">querySelector</samp> uses this string to search for any elements that match that selector. When it searches, the `document` is not actually searching the page, it is searching the <samp class="emphasis">document object model</samp>, or DOM. The DOM is the browser’s internal representation of an HTML document. It builds this representation as it reads through and interprets the HTML.

In JavaScript, you can interact with the DOM using the `document` object and its methods, such as <samp class="methodname">querySelector</samp>. For each HTML tag, there is a corresponding element in the DOM, and you can interact with any of these elements using JavaScript. (Generally, when we refer to an “element,” we mean a “DOM element.”)

In the console, call <samp class="methodname">document.querySelector</samp> again, passing it `DETAIL_IMAGE_SELECTOR` to get a reference to the element for the detail image. But this time, assign the reference to a new variable named <samp class="varname">detailImage</samp>:

```
var detailImage = document.querySelector(DETAIL_IMAGE_SELECTOR);
```

Press Return, and the console will print `undefined` ([Figure 6.13](#ch06s06.html_fig-declaring-var-in-console "Figure 6.13  Declaring a variable in the console")). Do not panic! This is not an error.

**Figure 6.13  Declaring a variable in the console**

![Declaring a variable in the console](Ottergram/Functions/img/declaring-var-in-console.png)

The console is just doing its job, telling you that there is no resulting value from declaring a variable. In JavaScript, the absence of a value is represented by the keyword `undefined`.

That does not mean that your <samp class="varname">detailImage</samp> variable was not assigned. To check it, just type <samp class="varname">detailImage</samp> in the console and press Return. You will see the HTML representation of the detail image, just as you saw when you entered `document.querySelector(DETAIL_IMAGE_SELECTOR)` ([Figure 6.14](#ch06s06.html_fig-detail-image-assigned "Figure 6.14  Checking the value of detailImage")).

**Figure 6.14  Checking the value of `detailImage`**

![Checking the value of detailImage](Ottergram/Functions/img/detail-image-assigned.png)

What is the point of all this? By assigning a reference to a variable, you can use the variable name any time you want to refer to the element. Now, instead of having to type `document.querySelector(DETAIL_IMAGE_SELECTOR)` every time, you can just type <samp class="varname">detailImage</samp>.

When you have a reference to the detail image, it is easy to change the value of its `src` attribute. In the console, assign `detailImage.src` to the string `'img/otter2.jpg'`.

```
detailImage.src = 'img/otter2.jpg';
```

Using the dot operator, you accessed the `src` <samp class="firstterm">property</samp> of the <samp class="varname">detailImage</samp> object. A property is like a variable, but it belongs to a particular object. When you assign (or <samp class="emphasis">set</samp>) `src` to the string `'img/otter2.jpg'`, you will see that a different otter occupies the detail image area ([Figure 6.15](#ch06s06.html_fig-detail-img-src-otter2 "Figure 6.15  Setting the src property of the detail image")).

**Figure 6.15  Setting the `src` property of the detail image**

![Setting the src property of the detail image](Ottergram/Functions/img/detail-img-src-otter2.png)

The `src` property corresponds to the `src` attribute of the `<img>` tag in <samp class="filename">index.html</samp>. Because of this relationship, another way to achieve the same result is to use the <samp class="varname">detailImage</samp>’s <samp class="methodname">setAttribute</samp> method.

Call this method in the console and pass it two strings: the name of the attribute and the new value.

```
detailImage.setAttribute('src', 'img/otter3.jpg');
```

The detail image changes once again ([Figure 6.16](#ch06s06.html_fig-detail-image-set-attribute "Figure 6.16  Using setAttribute to change the image")).

**Figure 6.16  Using `setAttribute` to change the image**

![Using setAttribute to change the image](Ottergram/Functions/img/detail-image-set-attribute.png)

You now have all the pieces you need to create an automated way to change the detail image. Get ready to write your first function!

## Writing the setDetails Function

You have been working with methods and have seen that they can be invoked to cause a block of code to run. Functions and methods are really just a list of steps that you would like to use again and again. Calling a function is like saying “Make a sandwich” instead of “Lay out two slices of bread. Put prosciutto, salami, and provolone on one slice. Put the other slice of bread on top.”

You will write seven functions for Ottergram in this chapter. Your first function will do two things: change the detail image and the detail image title. Add this <samp class="firstterm">function declaration</samp> to <samp class="filename">main.js</samp>.

```
var DETAIL_IMAGE_SELECTOR = '[data-image-role="target"]';
var DETAIL_TITLE_SELECTOR = '[data-image-role="title"]';
var THUMBNAIL_LINK_SELECTOR = '[data-image-role="trigger"]';

function setDetails() {
  'use strict';
  // Code will go here
}
```

You declared a function named <samp class="function">setDetails</samp> using the `function` keyword. When declaring a function, the name is always followed by a pair of parentheses. They are not part of the name, however – you will find out what they are for soon.

After the parentheses is a pair of curly braces. Inside the curly braces is the <samp class="firstterm">body</samp> of the function. The body will contain the steps the function needs to perform. These steps are more formally referred to as <samp class="firstterm">statements</samp>.

The first line of your function is the string `'use strict';`. You will use this string at the beginning of all your functions to tell the browser that they conform to the most recent standard version of JavaScript. (There is more about strict mode in a For the More Curious section at the end of this chapter.)

The other line in the <samp class="function">setDetails</samp> function is a comment. Like CSS comments, JavaScript comments are ignored by the browser but useful for developers. JavaScript comments that are only one line can be written this way, with `//`. For comments that span multiple lines, you can use the `/* */` style. Both are correct in JavaScript.

In the console, you have already tried out all of the statements needed to change the photo in the detail image. Go back to the console and press the Up arrow key. You will see the most recent statement you entered copied at the prompt. The Up and Down arrows allow you to go backward and forward through your history of statements.

Using the arrow keys, find the statement that gets a reference to the detail image: `var detailImage = document.querySelector(DETAIL_IMAGE_SELECTOR);`. Copy this line from the console and paste it into <samp class="filename">main.js</samp> in place of the comment. Then, copy and paste the line in the console that calls the `detailImage.setAttribute` method: `detailImage.setAttribute('src', 'img/otter3.jpg');`.

Your <samp class="function">setDetails</samp> function in <samp class="filename">main.js</samp> should look like this:

```
...
function setDetails() {
  'use strict';
  // Code will go here
  var detailImage = document.querySelector(DETAIL_IMAGE_SELECTOR);
  detailImage.setAttribute('src', 'img/otter3.jpg');
}
```

Save <samp class="filename">main.js</samp> and go back to the console. Enter the following and press Return to run your <samp class="function">setDetails</samp> function.

```
setDetails();
```

Entering – or calling – the name of a function followed immediately by parentheses makes the function execute all of the code in its body. You should see that <samp class="filename">img/otter3.jpg</samp> is now displayed as the detail image ([Figure 6.17](#ch06s07.html_fig-running-setdetails-static "Figure 6.17  Running setDetails to change the image")).

**Figure 6.17  Running `setDetails` to change the image**

![Running setDetails to change the image](Ottergram/Functions/img/presto-chango.png)

<samp class="function">setDetails</samp> has changed the detail image, but not the detail image title. You want it to do both. As you did with the detail image, you will add statements to get a reference to the element and to change the element’s properties.

In your <samp class="function">setDetails</samp> function in <samp class="filename">main.js</samp>, call <samp class="methodname">document.querySelector</samp> again, passing it `DETAIL_TITLE_SELECTOR`. Assign the result to a new variable named `detailTitle`. Then, set its `textContent` property to `'You Should Be Dancing'`.

```
...
function setDetails() {
  'use strict';
  var detailImage = document.querySelector(DETAIL_IMAGE_SELECTOR);
  detailImage.setAttribute('src', 'img/otter3.jpg');

  var detailTitle = document.querySelector(DETAIL_TITLE_SELECTOR);
  detailTitle.textContent = 'You Should Be Dancing';
}
```

The `textContent` property is the text (not including HTML tags) inside of an element.

Save your changes and run <samp class="function">setDetails</samp> in the console. Now the image <samp class="emphasis">and</samp> title change ([Figure 6.18](#ch06s07.html_fig-set-details-img-and-title "Figure 6.18  Changing the image and title using setDetails")).

**Figure 6.18  Changing the image and title using `setDetails`**

![Changing the image and title using setDetails](Ottergram/Functions/img/set-details-img-and-title.png)

### Accepting arguments by declaring parameters

<samp class="function">setDetails</samp> does the work of changing the detail image and title. But every time you run it, it sets the image’s `src` to `'img/otter3.jpg'` and the title’s `textContent` to `'You Should Be Dancing'`. What if you want to use other images and text?

You need a way to tell <samp class="function">setDetails</samp> <samp class="emphasis">which</samp> image and <samp class="emphasis">what</samp> text to use when you call it.

To achieve this, you need your function to accept <samp class="firstterm">arguments</samp> – values that are passed to the function and that it can work with. And to do that, you have to specify <samp class="firstterm">parameters</samp> in the function declaration.

Add two parameters to <samp class="function">setDetails</samp> in <samp class="filename">main.js</samp>:

```
...
function setDetails(imageUrl, titleText) {
  'use strict';
  var detailImage = document.querySelector(DETAIL_IMAGE_SELECTOR);
  detailImage.setAttribute('src', 'img/otter3.jpg');

  var detailTitle = document.querySelector(DETAIL_TITLE_SELECTOR);
  detailTitle.textContent = 'You Should Be Dancing';
}
```

Now, use those parameters in place of `'img/otter3.jpg'` and `'You should Be Dancing'`:

```
...
function setDetails(imageUrl, titleText) {
  'use strict';
  var detailImage = document.querySelector(DETAIL_IMAGE_SELECTOR);
  detailImage.setAttribute('src', 'img/otter3.jpg');
  detailImage.setAttribute('src', imageUrl);

  var detailTitle = document.querySelector(DETAIL_TITLE_SELECTOR);
  detailTitle.textContent = 'You Should Be Dancing';
  detailTitle.textContent = titleText;
}
```

Your two parameters, `imageUrl` and `titleText`, are used as labels assigned to values passed to <samp class="function">setDetails</samp>. Save <samp class="filename">main.js</samp> and try it out in the console to see this working.

Call <samp class="function">setDetails</samp> and pass it the values `'img/otter4.jpg'` and `'Night Fever'`. (Make sure there is a comma between them.)

```
setDetails('img/otter4.jpg', 'Night Fever');
```

You should see the new image and title text, as in [Figure 6.19](#ch06s07.html_fig-set-details-with-args "Figure 6.19  Passing values to setDetails").

**Figure 6.19  Passing values to `setDetails`**

![Passing values to setDetails](Ottergram/Functions/img/set-details-with-args.png)

There is an important distinction between arguments and parameters. <samp class="emphasis">Parameters are defined as part of the function.</samp> In JavaScript, parameters are exactly like variables that are declared inside a function body. <samp class="emphasis">Arguments are values you supply to a function when you call it.</samp>

Also, be aware that no matter what variable names you use for your arguments, their values are always mapped to the parameter names so they can be used inside the function body. For example, imagine that you used variables for the image URL and the title text. When you call <samp class="function">setDetails</samp>, you pass in these two variables as arguments.

```
var otterOneImage = 'img/otter1.jpg';
var otterOneTitle = 'Stayin\' Alive';

setDetails(otterOneImage, otterOneTitle);
```

The <samp class="function">setDetails</samp> function accepts the values, labels them with the parameter names `imageUrl` and `titleText`, and then runs the code inside its body. That code uses `imageUrl` and `titleText`, passing them as arguments to <samp class="methodname">document.querySelector</samp>.

Like variable names, parameter names are just labels for values. You can use whatever parameter names you like, but it is good practice to use descriptive names, as you have done here, to make your code easier to read and maintain.

## Returning Values from Functions

You have completed the first (or, rather, last) item on the plan and picked up some JavaScript know-how along the way. Now you will move on to the next two items on the list: getting the image and the title from a thumbnail. For each of these, you will write a new function.

Add a function declaration in <samp class="filename">main.js</samp> for <samp class="function">imageFromThumb</samp>. It will accept a single parameter, `thumbnail`, which is a reference to a thumbnail anchor element. It will retrieve and return the value of the `data-image-url` attribute.

```
...
function setDetails(imageUrl, titleText) {
  ...
}

function imageFromThumb(thumbnail) {
  'use strict';
  return thumbnail.getAttribute('data-image-url');
}
```

The <samp class="methodname">getAttribute</samp> method does the opposite of the <samp class="methodname">setAttribute</samp> method you used in the <samp class="function">setDetails</samp> function. It only takes a single argument, the name of an attribute.

Unlike <samp class="function">setDetails</samp>, the <samp class="function">imageFromThumb</samp> function uses the `return` keyword. When you call a function that has a `return` statement, it gives you back a value. <samp class="function">querySelector</samp> is an example of this. When you called it, it returned a value that you then assigned to a variable.

Save <samp class="filename">main.js</samp> and try out the following in the console, pressing Return between the lines.

```
var firstThumbnail = document.querySelector(THUMBNAIL_LINK_SELECTOR);
imageFromThumb(firstThumbnail);
```

The console reports that the value returned was the string `"img/otter1.jpg"`, because <samp class="function">imageFromThumb</samp> returns the `data-image-url` of the thumbnail.

**Figure 6.20  Value returned from `imageFromThumb`**

![Value returned from imageFromThumb](Ottergram/Functions/img/value-returned-from-image-from-thumb.png)

Note that any statements that come after a `return` statement will not be run. A `return` statement effectively stops a running function.

The next function to write is one that will accept a thumbnail element reference and return the title text.

Add a function declaration in <samp class="filename">main.js</samp> for <samp class="function">titleFromThumb</samp>, with a `thumbnail` parameter. It will return the value of the `data-image-title` attribute.

```
...
function imageFromThumb(thumbnail) {
  ...
}

function titleFromThumb(thumbnail) {
  'use strict';
  return thumbnail.getAttribute('data-image-title');
}
```

Save <samp class="filename">main.js</samp> and try this function out in the console, too:

```
var firstThumbnail = document.querySelector(THUMBNAIL_LINK_SELECTOR);
titleFromThumb(firstThumbnail);
```

**Figure 6.21  Value returned from `titleFromThumb`**

![Value returned from titleFromThumb](Ottergram/Functions/img/value-returned-from-title-from-thumb.png)

The next function to write brings the three other functions together for convenience, so that you do not need to call them separately. It will accept a reference to a thumbnail element and then call <samp class="function">setDetails</samp>, passing in the values from calling <samp class="function">imageFromThumb</samp> and <samp class="function">titleFromThumb</samp>.

Add <samp class="function">setDetailsFromThumb</samp> in <samp class="filename">main.js</samp>.

```
...
function titleFromThumb(thumbnail) {
  ...
}

function setDetailsFromThumb(thumbnail) {
  'use strict';
  setDetails(imageFromThumb(thumbnail), titleFromThumb(thumbnail));
}
```

Notice that <samp class="function">setDetails</samp> is being called with two arguments – and those arguments are function calls, too. How does this work?

Before <samp class="function">setDetails</samp> is actually called, its arguments are reduced to their simplest values. First, <samp class="function">imageFromThumb(thumbnail)</samp> runs and returns a value. Then, <samp class="function">titleFromThumb(thumbnail)</samp> runs and returns a value. Finally, <samp class="function">setDetails</samp> is called with the values returned by <samp class="function">imageFromThumb(thumbnail)</samp> and <samp class="function">titleFromThumb(thumbnail)</samp>. [Figure 6.22](#ch06s08.html_fig-nested-function-call "Figure 6.22  Function calls as arguments") shows this process.

**Figure 6.22  Function calls as arguments**

![Function calls as arguments](Ottergram/Functions/img/nested-function-call.png)

Save <samp class="filename">main.js</samp>. You have completed all the code for retrieving data-attribute values from thumbnails and using those values to update what is shown in the detail image and title.

Moving up from the low-level operations, the next thing to do is write code that will perform your data transfer from thumbnail to detail when the user clicks a thumbnail.

## Adding an Event Listener

Browsers are busy pieces of software. Every tap, click, scroll, and keystroke is noticed by the browser. Each of these is an <samp class="firstterm">event</samp> that the browser may respond to. To make websites more dynamic and interactive, you can trigger your own code when one of these events occurs. In this section, you will add <samp class="firstterm">event listeners</samp> to each of your thumbnails.

An event listener is an object that, as the name suggests, “listens” for a particular event, such as a mouse click. When its assigned event occurs, the event listener triggers a function call in response to the event.

(Mouse events, like clicks and double-clicks, and keyboard events like keypresses are among the most common event types. For a complete listing of events, check the event reference in the MDN at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​Events</samp>](https://developer.mozilla.org/en-US/docs/Web/Events).)

The <samp class="methodname">addEventListener</samp> method is available on every DOM element, including the `document`. As before, you will experiment with some code in the console first and then use your tested code to write functions in <samp class="filename">main.js</samp>.

Switch to <samp class="application">Chrome</samp> and enter the following code in the console. You will need to press Shift-Return to enter the line breaks. Press Return when you have finished typing all the code.

```
document.addEventListener('click', function () {
  console.log('you clicked!');
});
```

The code you entered added an event listener for the `document` object that is listening for any clicks that occur on the page. When a click happens, the event listener will print “you clicked!” to the console using the built-in <samp class="methodname">console.log</samp> method ([Figure 6.23](#ch06s09.html_fig-registering-click-handler "Figure 6.23  Adding a listener for click events")).

**Figure 6.23  Adding a listener for click events**

![Adding a listener for click events](Ottergram/Functions/img/registering-click-handler.png)

Click on the header, the detail image, or the background. You should see that the text “you clicked!” appears printed in the console. (Do not click the thumbnails – those will take you away from Ottergram’s <samp class="filename">index.html</samp> page. When you are not on the <samp class="filename">index.html</samp> page, none of your markup, CSS, or JavaScript will be loaded and running in the browser.)

<samp class="methodname">addEventListener</samp> accepts two arguments: a string with the name of the event and a function. This function will be run by <samp class="methodname">addEventListener</samp> any time the event occurs for the element. The way this function is written may look a little strange at first. It is an <samp class="firstterm">anonymous function</samp>.

So far, you have worked with <samp class="firstterm">named functions</samp>, like <samp class="function">setDetails</samp> and <samp class="function">titleFromThumb</samp>. Named functions have names – no surprise there – and are created using function declarations.

You can also write literal function values, the same way you can write literal number values like `42` and literal string values like `"Barry the Otter"`. Another name for literal function values is <samp class="firstterm">anonymous functions</samp>.

Anonymous functions are frequently used as arguments to other functions, like the one you passed as the second argument to <samp class="function">document.addEventListener</samp>. This practice of passing a function to another function is quite common in JavaScript and is known as a <samp class="firstterm">callback pattern</samp> because the function you pass in as an argument will get “called back” at some point in the future.

It is perfectly fine to use a named function as a callback, but many front-end developers will use anonymous functions because they can provide more flexibility than named functions. You will see how this works shortly.

Now you will add an event listener for an individual thumbnail. Enter the following in the console. (Remember to use Shift-Return for the line breaks in the call to <samp class="methodname">firstThumbnail.addEventListener</samp>.)

```
var firstThumbnail = document.querySelector(THUMBNAIL_LINK_SELECTOR);
firstThumbnail.addEventListener('click', function () {
  console.log('you clicked!');
});
```

If you try clicking the first thumbnail (Barry the Otter, farthest to the left), your browser will take you to the large image of Barry. What happened? Remember that each thumbnail is wrapped in an anchor tag with an `href` that points to an image, like <samp class="filename">img/otter1.jpg</samp>. This is the normal behavior of a browser when a user clicks a link: It has opened the file indicated by the `href` attribute.

But you do not want to navigate away from Ottergram when a thumbnail is clicked, and you should not have to change your anchor tags to something else. Luckily, you can handle all of this from your callback function.

Recall from earlier in the chapter that functions carry out their tasks without you having to worry about the details. Usually you only need to know what information to pass as arguments and what information will be returned. When you pass a callback function as an argument, there is one more thing you need to know: what information will be passed to your callback.

When you call <samp class="methodname">addEventListener</samp>, you are telling the browser, “When the `firstThumbnail` is clicked, call this function” – and then the browser diligently waits for that element to be clicked. If a click happens, the browser makes note of all the details about the event (such as the exact position of the mouse, whether it was the left or right mouse button, and whether it was a single or double click). The browser then passes an object with this information to your function. This object is an <samp class="firstterm">event object</samp>.

This relationship is diagrammed in [Figure 6.24](#ch06s09.html_fig-anon-func-param-mapping "Figure 6.24  Passing an anonymous function that expects an argument"), using a made-up implementation of <samp class="methodname">addEventListener</samp>.

**Figure 6.24  Passing an anonymous function that expects an argument**

![Passing an anonymous function that expects an argument](Ottergram/Functions/img/anon-func-param-mapping.png)

In a moment, you will pass an anonymous function to <samp class="methodname">addEventListener</samp>, just like before. But, this time, your anonymous function will expect to receive an argument. Make sure Ottergram is on the <samp class="filename">index.html</samp> page and enter the following in the console:

```
var firstThumbnail = document.querySelector(THUMBNAIL_LINK_SELECTOR);
firstThumbnail.addEventListener('click', function (event) {
  event.preventDefault();
  console.log('you clicked!');
  console.log(event);
});
```

The browser will call your anonymous function each time <samp class="varname">firstThumbnail</samp> is clicked, and it will pass your anonymous function the event object. Using this object (which you have labeled <samp class="varname">event</samp>), you call its <samp class="methodname">preventDefault</samp> method. This method will stop the link from taking the browser to a different page. Finally, you call <samp class="function">console.log</samp> on the `event` object so that you can inspect it in the DevTools.

Now click on the first thumbnail. Your browser remains on the Ottergram page and the event is logged to the console: `MouseEvent {isTrusted: true}`. If you click the disclosure arrow next to `MouseEvent`, you should see quite a bit of information about the event ([Figure 6.25](#ch06s09.html_fig-mouse-event-logged "Figure 6.25  Preventing the event default and logging the event object")), including the mouse coordinates on the page, which mouse button was clicked, and whether any special modifier keys were pressed during the click.

**Figure 6.25  Preventing the event default and logging the event object**

![Preventing the event default and logging the event object](Ottergram/Functions/img/mouse-event-logged.png)

For now, do not focus on the different properties of the event object. Just know that it carries lots of information about the browser event that was triggered.

By the way, it is not required that the callback function’s parameter be named `event` – it will be mapped to the value that is passed in no matter what you name it. You can use whatever parameter names you like, but it is good practice to use descriptive names, as you have done here, to make your code easier to read and maintain.

You now have a function that accepts a thumbnail and adds an event listener. Add a function declaration to <samp class="filename">main.js</samp> for <samp class="function">addThumbClickHandler</samp>. It should define a parameter named `thumb`.

You can copy your experimental <samp class="methodname">addEventListener</samp> code from the console and paste it into the body of <samp class="function">addThumbClickHandler</samp>. Modify it so that you are calling <samp class="function">thumb.addEventListener</samp>. For now, you will only need the call to `event.preventDefault` in the event callback.

```
...
function setDetailsFromThumb(thumbnail) {
  ...
}

function addThumbClickHandler(thumb)
  'use strict';
  thumb.addEventListener('click', function (event) {
    event.preventDefault();
  });
}
```

Inside the event callback, you have access to the `thumb` parameter declared as part of <samp class="function">addThumbClickHandler</samp>. Pass it to a call to <samp class="function">setDetailsFromThumb</samp>.

```
...
function addThumbClickHandler(thumb) {
  'use strict';
  thumb.addEventListener('click', function (event) {
    event.preventDefault();
    setDetailsFromThumb(thumb);
  });
}
```

JavaScript, like many other programming languages, has rules about defining and accessing variables and functions. The anonymous function you passed to <samp class="methodname">addEventListener</samp> is able to access the <samp class="function">setDetailsFromThumb</samp> function because <samp class="function">setDetailsFromThumb</samp> was declared in the <samp class="firstterm">global scope</samp>. This means that it can be accessed from any other function or from the console. The same is true for variables like <samp class="varname">DETAIL_IMAGE_SELECTOR</samp>, which is also declared in the global scope.

However, the variables <samp class="varname">detailImage</samp> and <samp class="varname">detailTitle</samp>, which you declared <samp class="emphasis">inside</samp> <samp class="function">setDetails</samp>, are only available within the body of <samp class="function">setDetails</samp>. You cannot access them from the console or from other functions. These variables are declared in the <samp class="firstterm">function scope</samp> (or <samp class="firstterm">local scope</samp>) of <samp class="function">setDetails</samp>. A function’s parameters work very much like variables declared inside a function. They too are part of that function’s scope.

Normally, functions cannot access variables or parameters that are part of another function’s scope. <samp class="function">addThumbClickHandler</samp> is interesting because it defines the parameter <samp class="varname">thumb</samp>, which is accessed by another function – the callback function you passed to <samp class="methodname">addEventListener</samp>. This is possible because the callback function is part of <samp class="function">addThumbClickHandler</samp>’s scope.

You can read more about how all of this works in a For the More Curious section at the end of this chapter.

## Accessing All the Thumbnails

In the console, you added an event listener for the first thumbnail. Now you will add an event listener for all of the thumbnails, using a new DOM method.

When you retrieved the detail image and the detail title, you used the <samp class="methodname">document.querySelector</samp> method to search the DOM for an element that matched the selector passed in. <samp class="methodname">document.querySelector</samp> will only return a single value, even if you pass in a selector that matches multiple elements.

The <samp class="methodname">document.querySelectorAll</samp> method, on the other hand, will return a list of all matching elements. Call `document.querySelectorAll(THUMBNAIL_LINK_SELECTOR)` in the console and examine the results. You should see the list of anchor element results ([Figure 6.26](#ch06s10.html_fig-qsa-thumbnail-link "Figure 6.26  document.querySelectorAll returns multiple matching elements")).

**Figure 6.26  `document.querySelectorAll` returns multiple matching elements**

![document.querySelectorAll returns multiple matching elements](Ottergram/Functions/img/qsa-thumbnail-link.png)

Knowing this, you can test <samp class="function">setDetailsFromThumb</samp> properly. In the console, assign the result of calling `document.querySelectorAll(THUMBNAIL_LINK_SELECTOR)` to a variable named `thumbnails`. Use <samp class="firstterm">bracket syntax</samp> to retrieve the fifth element from the `thumbnails` list, passing it to <samp class="function">setDetailsFromThumb</samp>. Bracket syntax lets you specify an item in the list by its numerical index. The index starts at 0, so the fifth item is at index 4.

Here is your code for the console:

```
var thumbnails = document.querySelectorAll(THUMBNAIL_LINK_SELECTOR);
setDetailsFromThumb(thumbnails[4]);
```

After running this in the console, you can see that an item from the `thumbnails` list can be passed to <samp class="function">setDetailsFromThumb</samp>, successfully updating the detail image and title ([Figure 6.27](#ch06s10.html_fig-hooray-nodelist "Figure 6.27  Passing an item from querySelectorAll to setDetailsFromThumb")).

**Figure 6.27  Passing an item from `querySelectorAll` to `setDetailsFromThumb`**

![Passing an item from querySelectorAll to setDetailsFromThumb](Ottergram/Functions/img/hooray-nodelist.png)

In <samp class="filename">main.js</samp>, add a function named <samp class="function">getThumbnailsArray</samp> and paste in the code that retrieves all matching elements for `THUMBNAIL_LINK_SELECTOR` and assigns the result to a `thumbnails` variable.

```
...
function addThumbClickHandler(thumb) {
  ...
}

function getThumbnailsArray() {
  'use strict';
  var thumbnails = document.querySelectorAll(THUMBNAIL_LINK_SELECTOR);
}
```

Before you go any further, there is a small “gotcha” when working with DOM methods. Methods that return lists of elements do not return <samp class="firstterm">arrays</samp>. Instead, they return <samp class="firstterm">NodeLists</samp>. Both arrays and NodeLists are lists of items, but arrays have a number of powerful methods for working with collections of items, some of which you will want for Ottergram.

You will need to convert the NodeList returned from <samp class="methodname">querySelectorAll</samp> to an array using an odd-looking bit of JavaScript. Do not worry about this syntax right now. It is a backward-compatible way to convert from a NodeList to an array. Make this change in <samp class="filename">main.js</samp>:

```
...
function getThumbnailsArray() {
  'use strict';
  var thumbnails = document.querySelectorAll(THUMBNAIL_LINK_SELECTOR);
  var thumbnailArray = [].slice.call(thumbnails);
  return thumbnailArray;
}
```

Now, armed with all of the otter thumbnails, you can connect them to your event listening code, which will change the detail image and title in response to a click.

## Iterating Through the Array of Thumbnails

Connecting the thumbnails to your event handling code will be short and sweet. You will write a function that will be the starting point for all of Ottergram’s logic. Other programming languages have a built-in mechanism for starting an application, which JavaScript lacks. But not to worry – it is easy enough to implement by hand.

Begin by adding an <samp class="function">initializeEvents</samp> function at the end of <samp class="filename">main.js</samp>. This method will tie together all of the steps for making Ottergram interactive. First, it will get the array of thumbnails. Then, it will iterate over the array, adding the click handler to each one. After you have written the function, you will add a call to <samp class="function">initializeEvents</samp> at the very end of <samp class="filename">main.js</samp> to run it.

In the body of your new function, add a call to <samp class="function">getThumbnailsArray</samp> and assign the result (the array of thumbnails) to a variable named `thumbnails`.

```
...
function getThumbnailsArray() {
  ...
}

function initializeEvents() {
  'use strict';
  var thumbnails = getThumbnailsArray();
}
```

Next, you need to go through the array of thumbnails, one item at a time. As you visit each one, you will call <samp class="function">addThumbClickHandler</samp> and pass the thumbnail element to it. That may seem like several steps, but because `thumbnails` is a proper array, you can do all of this with a single method call.

Add a call to the `thumbnails.forEach` method in <samp class="filename">main.js</samp> and pass it the <samp class="function">addThumbClickHandler</samp> function as a callback.

```
...
function initializeEvents() {
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);
}
```

Note that you are passing a named function as a callback. As you will read later, this is not always a good choice. However, in this case it works well, because <samp class="function">addThumbClickHandler</samp> only needs information that will be passed to it when <samp class="methodname">forEach</samp> calls it – an item from the `thumbnails` array.

Finally, to see everything in action, add a call to <samp class="function">initializeEvents</samp> at the very end of <samp class="filename">main.js</samp>.

```
...
function initializeEvents() {
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);
}

initializeEvents();
```

Remember, as the browser reads through each line of your JavaScript code, it runs the code. For most of <samp class="filename">main.js</samp>, it is only running variable and function declarations. But when it reaches the line `initializeEvents();`, it will run that function.

Save and return to the browser. Click a few different thumbnails and see the fruits of your labor ([Figure 6.28](#ch06s11.html_fig-dancing "Figure 6.28  You should indeed be dancing")).

**Figure 6.28  You should indeed be dancing**

![You should indeed be dancing](Ottergram/Functions/img/dancing.png)

Sit back, relax, and enjoy clicking some otters! There was a lot to work through and absorb while building your site’s interactive layer. In the next chapter you will finish Ottergram by adding visual effects for extra pop.

## Silver Challenge: Link Hijack

The <samp class="application">Chrome</samp> DevTools give you a lot of power for toying with pages that you visit. This next challenge is to change all of the links on a search results page so that they do not go anywhere.

Go to your favorite search engine and search for “otters.” Open the DevTools to the console. With the functions you wrote in Ottergram as a reference, attach event listeners to all of the links and disable their default click functionality.

## Gold Challenge: Random Otters

Write a function that changes the `data-image-url` of a random otter thumbnail so that the detail image no longer matches the thumbnail. Use the URL of an image of your choosing (though a web search for “tacocat” should provide a good one).

For an extra challenge, write a function that resets your otter thumbnails to their original `data-image-url` values and changes another one at random.

## For the More Curious: Strict Mode

What is strict mode, and why does it exist? It was created as a cleaner mode of JavaScript, catching certain kinds of coding mistakes (like typos in variable names), steering developers away from some error-prone parts of the language, and disabling some language features that are just plain bad.

Strict mode provides a number of benefits. It:

*   enforces the use of the `var` keyword

*   does not require `with` statements

*   places restrictions on the way the `eval` function can be used

*   treats duplicate names in a function’s parameters as a syntax error

All this just for adding the `'use strict'` directive to the top of a function. As a bonus, the `'use strict'` directive is ignored by older browsers that do not support it. (These browsers simply see the directive as a string.)

You can read more about strict mode on the MDN at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​JavaScript/​Reference/​Strict_mode</samp>](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode).

## For the More Curious: Closures

Earlier we mentioned that developers often prefer to use anonymous functions as callbacks instead of named functions. <samp class="function">addThumbClickHandler</samp> illustrates why an anonymous function is a better solution.

Let’s say you tried to use a named function, <samp class="function">clickFunction</samp>, for the callback. Inside of that function, you have access to the `event` object because it will be passed in by <samp class="methodname">addEventListener</samp>. But the body of <samp class="function">clickFunction</samp> has no access to the `thumb` object. That parameter is only accessible <samp class="emphasis">inside</samp> the <samp class="function">addThumbClickHandler</samp> function.

```
function clickFunction (event) {
  event.preventDefault();

  setDetailsFromThumb(thumb); // <--- This will cause an error
}

function addThumbClickHandler(thumb) {
  thumb.addEventListener('click', clickFunction);
}
```

On the other hand, using an anonymous function does give it access to the `thumb` parameter, because it is also inside of <samp class="function">addThumbClickHandler</samp>. When a function is defined inside of another function, it can use any of the variables and parameters of this outer function. In computer science terms, this is known as a <samp class="firstterm">closure</samp>.

When the <samp class="function">addThumbClickHandler</samp> function runs, it calls <samp class="methodname">addEventListener</samp>, which associates the callback function with the click event. The browser keeps track of these associations, internally holding a reference to the callback function and running the callback when the event occurs.

Technically, when the callback is eventually executed, the variables and parameters of <samp class="function">addThumbClickHandler</samp> no longer exist. They went away when <samp class="function">addThumbClickHandler</samp> finished running. But, the callback “captures” the values of <samp class="function">addThumbClickHandler</samp>’s variables and parameters. The callback uses these captured values when it runs.

For a deeper dive, read up on closures in the MDN.

## For the More Curious: NodeLists and HTMLCollections

There are two ways to retrieve lists of elements that live in the DOM. The first one is <samp class="methodname">document.querySelectorAll</samp>, which returns a NodeList. The other is <samp class="methodname">document.getElementsByTagName</samp>, which differs from <samp class="methodname">document.querySelectorAll</samp> in that you can only pass it a string with a tag name, like `"div"` or `"a"`, and also in that it returns an <samp class="firstterm">HTMLCollection</samp>.

Neither NodeLists nor HTMLCollections are true arrays, so they lack array methods such as <samp class="methodname">forEach</samp>, but they do have some very interesting properties.

HTMLCollections are <samp class="firstterm">live nodes</samp>. This means that when changes are made to the DOM, the contents of an HTMLCollection can change without you having to call <samp class="methodname">document.getElementsByTagName</samp> again.

To see how this works, try the following in the console.

```
var thumbnails = document.getElementsByTagName("a");
thumbnails.length;
```

After getting all of the anchor elements as an HTMLCollection, you print the `length` of that list to the console.

Now, remove some of the anchor tags from the page using the elements panel in the DevTools: Control-click (right-click) one of the list items and choose <samp class="guilabel">Delete element</samp> ([Figure 6.29](#ch06s16.html_fig-delete-element "Figure 6.29  Deleting a DOM element with the DevTools")).

**Figure 6.29  Deleting a DOM element with the DevTools**

![Deleting a DOM element with the DevTools](Ottergram/Functions/img/delete-element.png)

Do this several times, then enter `thumbnails.length` into the console again. You should see that the `length` is different ([Figure 6.30](#ch06s16.html_fig-deleted-otters "Figure 6.30  The length value changes after deleting elements")).

**Figure 6.30  The length value changes after deleting elements**

![The length value changes after deleting elements](Ottergram/Functions/img/deleted-otters.png)

Converting NodeLists and HTMLCollections to arrays not only makes them more convenient to work with via array methods, but you also have the guarantee that the items in the array will not change, even if the DOM is modified.

## For the More Curious: JavaScript Types

Throughout the chapter, you created variables so you could refer to some data inside your functions. Early on, we told you that strings, numbers, and Booleans are three of the five <samp class="firstterm">primitive data types</samp>. The other two types are null and undefined.

[Table 6.2](#ch06s17.html_tab-data-types "Table 6.2  Primitive data types in JavaScript") summarizes the properties of the five primitive types.

**Table 6.2  Primitive data types in JavaScript**

| Type | Example | Description |
| --- | --- | --- |
| string | “And you get $100! And you get $100! And…!” | Letters, numbers, or symbols enclosed in matching quotation marks. |
| number | 42, 3.14159, -1 | Whole numbers and decimals. |
| Boolean | true, false | The keywords `true` and `false`, corresponding to logical true and false. |
| null | null | The value that denotes an invalid value. |
| undefined | undefined | The value of a variable that has not been assigned to anything. |

All other types in JavaScript are considered <samp class="firstterm">compound types</samp> or <samp class="firstterm">complex types</samp>. These include arrays and objects, which can have other types inside of them. For example, you wrote a function that produced an array of thumbnail objects. Arrays also have properties (like `length`) and methods (such as <samp class="methodname">forEach</samp>).

You will continue to work with primitive and complex data types throughout this book.

# <samp class="chapter_number">7</samp>
<samp class="chapter_name">Visual Effects with CSS</samp>

In the last chapter, you gave Ottergram the ability to respond to user interaction by changing the detail image when the user clicks a thumbnail. You will build on that in this chapter by adding three different visual effects to Ottergram.

The first effect is a simple layout change that involves hiding the detail image and letting the thumbnails take up the width of the page. When the user clicks a thumbnail, you will make the detail image reappear and return the thumbnails to their previous size.

The other two effects will use CSS to create visual animations for the thumbnails and the detail image ([Figure 7.1](#ch07.html_fig-final "Figure 7.1  Ottergram with transition effects")).

**Figure 7.1  Ottergram with transition effects**

![Ottergram with transition effects](Ottergram/Transitions/img/final.png)

## Hiding and Showing the Detail Image

Ottergram’s users may want to be able to scroll through the thumbnails without the detail image being on the page ([Figure 7.2](#ch07.html_fig-hidden-detail-mode "Figure 7.2  Detail image visible and hidden")).

**Figure 7.2  Detail image visible and hidden**

![Detail image visible and hidden](Ottergram/Transitions/img/hidden-detail-mode.png)

To make this happen, you need to be able to apply styles to your `.thumbnail-list` and `.detail-image-container` based on a condition that will turn on and off as the website is in use. You could do this by creating new class selectors, like `.thumbnail-list-no-detail` and `.hidden-detail-image-container`, and add those classes to the target elements with JavaScript. The trouble with this approach is that it would be inefficient.

The event that will cause the detail image to hide will <samp class="emphasis">simultaneously</samp> cause the thumbnail list to reposition itself. It is a single event. Adding classes to your `<ul>` and `<div>` elements separately does not reflect this.

A better approach is to use JavaScript to add a <samp class="emphasis">single</samp> class selector that affects the layout as a whole. Then, you can target the `.thumbnail-list` and `.detail-image-container` when they are descendents of the new selector.

You are going to dynamically add a class name to the `<body>` element to hide the detail image and enlarge the thumbnails, and then dynamically remove the class name to return to your current styles ([Figure 7.3](#ch07.html_fig-ancestor-class-change "Figure 7.3  Restyling descendants with class change to ancestor")).

**Figure 7.3  Restyling descendants with class change to ancestor**

![Restyling descendants with class change to ancestor](Ottergram/Transitions/img/ancestor-class-change.png)

This technique is similar in two ways to the one you used with the media queries.

First, it involves styles that are activated when an ancestor meets a particular condition. With media queries, that ancestor is the viewport and the condition is a minimum width. In this new code, the ancestor will be any element you select that the target elements share, and the condition will be that the ancestor has a particular class name.

The second similarity is that you must place the conditional styles <samp class="emphasis">after</samp> the other declarations for the affected elements in your stylesheet because these conditional styles need to override the previous declarations when they are active.

You will proceed in three steps:

1.  In your CSS, define the styles that create the visual effect you are trying to get. Also, test your styles in the DevTools.

2.  Write JavaScript functions to add and remove a class name for the `<body>` element.

3.  Add an event listener to trigger your JavaScript function.

### Creating styles to hide the detail image

To hide the `.detail-image-container`, you will add a declaration that sets `display: none` for this element. `display: none` tells the browser that the element should not be rendered.

The class you will be adding dynamically to the `<body>` will be called `hidden-detail`. Therefore, you only want to apply `display: none` to `.detail-image-container` when it is a descendent of `.hidden-detail`.

Add the style to hide the detail image in <samp class="filename">styles.css</samp>:

```
...
.detail-image-title {
  ...
}

.hidden-detail .detail-image-container {
  display: none;
}

@media all and (min-width: 768px) {
  ...
}
```

Now, give some thought to what your `.thumbnail-list` will look like. Based on the current styles, it will be a column along the left side of wider screens and a horizontal row at the top of narrower screens. A centered column would be better when the detail image is hidden, regardless of the screen size.

Add styles to the `.thumbnail-list` and `.thumbnail-item` in <samp class="filename">styles.css</samp> when they are descendents of `.hidden-detail`.

```
...
.hidden-detail .detail-image-container {
  display: none;
}

.hidden-detail .thumbnail-list {
  flex-direction: column;
  align-items: center;
}

.hidden-detail .thumbnail-item {
  max-width: 80%;
}

@media all and (min-width: 768px) {
  ...
}
```

Now, the `.thumbnail-list` will always be displayed as a column while the `.detail-image-container` is hidden.

You have also added a declaration setting the width of the `.thumbnail-item` elements to `max-width: 80%` when the detail image is hidden. This overrides the `max-width` styles set elsewhere for the `.thumbnail-item`s so that they will become the focus of the page.

When the `.detail-image-container`, `.thumbnail-list`, and `.thumbnail-item` elements are nested anywhere inside of an element with the class `hidden-detail`, these new styles will be activated.

Note that you added these <samp class="emphasis">before</samp> your media queries. As you already know, the order of your CSS code matters, with styles that appear later in the file overriding those that came before. In general, for the same selector, the browser uses the styles it has seen most recently. In this case, however, your new styles use selectors that are more specific than the ones that appear in your media queries, and specificity trumps recency.

Generally, it is best to keep your media queries at the end of the file. Your media queries will usually reuse the same selectors from existing styles, so putting them at the end makes sure that your media queries overwrite those existing styles. Also, it makes your media queries easier to locate, because they are always at the end of the file.

Save your file. Before you write the JavaScript that depends on the styles you have added, it is wise to test them. Start `browser-sync` (using `browser-sync start --server --browser "Google Chrome" --files "*.html, stylesheets/*.css, scripts/*.js"`) and open the DevTools. In the elements panel, Control-click (right-click) the `<body>` element and choose <samp class="guimenuitem">Add Attribute</samp> from the menu that appears ([Figure 7.4](#ch07.html_fig-adding-class-to-body "Figure 7.4  Choosing the Add Attribute menu item")).

**Figure 7.4  Choosing the Add Attribute menu item**

![Choosing the Add Attribute menu item](Ottergram/Transitions/img/adding-class-to-body.png)

The DevTools provides a space for you to start typing inside the `<body>` tag. Enter `class="hidden-detail"` and press Return ([Figure 7.5](#ch07.html_fig-adding-hidden-detail-attribute "Figure 7.5  Adding the hidden-detail class attribute")).

**Figure 7.5  Adding the `hidden-detail` class attribute**

![Adding the hidden-detail class attribute](Ottergram/Transitions/img/adding-hidden-detail-attribute.png)

After you add the `hidden-detail` class to the `<body>` in the DevTools, the detail image disappears and the thumbnails become much larger – just as you intended ([Figure 7.6](#ch07.html_fig-hidden-detail-added "Figure 7.6  Layout change after applying hidden-detail class")).

**Figure 7.6  Layout change after applying `hidden-detail` class**

![Layout change after applying hidden-detail class](Ottergram/Transitions/img/hidden-detail-added.png)

### Writing the JavaScript to hide the detail image

Next, you will write the JavaScript that will toggle the `.hidden-detail` class for the `<body>` element.

In <samp class="filename">main.js</samp>, add a variable named `HIDDEN_DETAIL_CLASS`.

```
var DETAIL_IMAGE_SELECTOR = '[data-image-role="target"]';
var DETAIL_TITLE_SELECTOR = '[data-image-role="title"]';
var THUMBNAIL_LINK_SELECTOR = '[data-image-role="trigger"]';
var HIDDEN_DETAIL_CLASS = 'hidden-detail';
...
```

Now, write a new function in <samp class="filename">main.js</samp> named <samp class="function">hideDetails</samp>. Its job is to add a class name to the `<body>` element. You will use the <samp class="methodname">classList.add</samp> DOM method to manipulate the class name.

```
...
function getThumbnailsArray() {
  ...
}

function hideDetails() {
  'use strict';
  document.body.classList.add(HIDDEN_DETAIL_CLASS);
}

function initializeEvents() {
  ...
}
...
```

You accessed the `<body>` element using the `document.body` property. This DOM element corresponds to the `<body>` tag in your markup. Like all DOM elements, it gives you a convenient way to manipulate its class names.

You also called the <samp class="methodname">add</samp> method on `document.body` to add the `hidden-detail` class to the `<body>`.

### Listening for the keypress event

Now you need a way to trigger the detail image to hide. As before, you will use an event listener, but this time your event listener will listen for a keypress instead of a click.

We use the term “keypress” generally to mean pressing and releasing a key, but that simple process actually triggers multiple events. When the key is first depressed, the `keydown` event is sent. If it is a character key (as opposed to a modifier key like Shift) then the `keypress` event is also sent. When the key is released, the `keyup` event is sent.

For Ottergram, these differences are minimal. You are going to use the `keyup` event.

In <samp class="filename">main.js</samp>, add a function named <samp class="function">addKeyPressHandler</samp> that calls <samp class="function">document.body.addEventListener</samp>, passing it the string `'keyup'` and an anonymous function that declares a parameter named `event`. Inside the body of this anonymous function, make sure to <samp class="function">preventDefault</samp> for the `event`, and then <samp class="function">console.log</samp> the `event`’s `keyCode`.

```
...
function hideDetails() {
  ...
}

function addKeyPressHandler() {
  'use strict';
  document.body.addEventListener('keyup', function (event) {
    event.preventDefault();
    console.log(event.keyCode);
  });
}

function initializeEvents() {
  ...
}
...
```

All of the keypress events have a property called <samp class="varname">keyCode</samp> that corresponds to the key that triggered the event. The <samp class="varname">keyCode</samp> is an integer, like 13 for Return, 32 for the space bar, and 38 for the up arrow.

Update the <samp class="function">initializeEvents</samp> function in <samp class="filename">main.js</samp> so that it calls <samp class="function">addKeyPressHandler</samp>. You need to do this so that the `<body>` element can listen for keyboard events when the page loads.

```
...
function initializeEvents() {
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);
  addKeyPressHandler();
}

initializeEvents();
```

Save and switch back to the browser. Make sure the console is visible, then click on the page to make sure that the focus is not on the DevTools – otherwise, the event listener will not be triggered. Now press some keys on your keyboard. You will see numbers printed to the console ([Figure 7.7](#ch07.html_fig-keycode-logging "Figure 7.7  Logging the keyCode to the console")).

**Figure 7.7  Logging the `keyCode` to the console**

![Logging the keyCode to the console](Ottergram/Transitions/img/keycode-logging.png)

You want to hide the detail image when the Esc key is pressed, not just any key. If you press the Esc key, you will see that the corresponding <samp class="varname">event.keyCode</samp> value is 27. You will use that to make your event listener more specific.

Add a variable to the top of <samp class="filename">main.js</samp> for the Esc key’s value.

```
var DETAIL_IMAGE_SELECTOR = '[data-image-role="target"]';
var DETAIL_TITLE_SELECTOR = '[data-image-role="title"]';
var THUMBNAIL_LINK_SELECTOR = '[data-image-role="trigger"]';
var HIDDEN_DETAIL_CLASS = 'hidden-detail';
var ESC_KEY = 27;
...
```

Now, update your `keyup` event listener to call <samp class="methodname">hideDetails</samp> when the value of <samp class="varname">event.keyCode</samp> matches the value of <samp class="varname">ESC_KEY</samp>.

```
...
function addKeyPressHandler() {
  'use strict';
  document.body.addEventListener('keyup', function (event) {
    event.preventDefault();
    console.log(event.keyCode);
    if (event.keyCode === ESC_KEY) {
      hideDetails();
    }
  });
}
...
```

You used the <samp class="firstterm">strict equality operator</samp> (`===`) to compare the values of <samp class="varname">event.keyCode</samp> and <samp class="varname">ESC_KEY</samp>. When these value are the same, you call <samp class="methodname">hideDetails</samp>.

You could have used the <samp class="firstterm">loose equality operator</samp> (`==`) to compare the values instead, but it is usually best to use the strict equality operator. The major difference between the equality operators is that the loose equality operator will automatically convert from one type of value to another. The strict equality operator will not do the conversion. With strict equality, if the types are not the same, then the result of the comparison is always `false`.

Many front-end developers refer to this automatic type conversion as <samp class="firstterm">type coercion</samp>. It is performed when values need to be compared (when using an equality operator), added together (in the case of numbers), or concatenated (as with strings).

Because of this automatic conversion, there is no syntax error if you try to add the string `"27"` with the number `42` – though the result might not be what you expect ([Figure 7.8](#ch07.html_fig-coercion "Figure 7.8  JavaScript will automatically convert between types")).

**Figure 7.8  JavaScript will automatically convert between types**

![JavaScript will automatically convert between types](Ottergram/Transitions/img/coercion.png)

This is very important when working with user-provided data, which you will do in [Chapter 10](#ch10.html "10 Processing Forms with JavaScript").

Save <samp class="filename">main.js</samp> and test your new functionality in the browser ([Figure 7.9](#ch07.html_fig-poof "Figure 7.9  Poof! Pressing Esc hides the detail image and title")).

**Figure 7.9  Poof! Pressing Esc hides the detail image and title**

![Poof! Pressing Esc hides the detail image and title](Ottergram/Transitions/img/poof.png)

### Showing the detail image again

There is one small but important piece to add: making the detail image visible again. This will be triggered when a thumbnail is clicked.

You used <samp class="methodname">classList.add</samp> to add a class name to the `<body>` element. You will use <samp class="methodname">classList.remove</samp> to remove that class name when a thumbnail is clicked. Add a new function named <samp class="function">showDetails</samp> to <samp class="filename">main.js</samp>.

```
...
function hideDetails() {
  ...
}

function showDetails() {
  'use strict';
  document.body.classList.remove(HIDDEN_DETAIL_CLASS);
}

function addKeyPressHandler() {
  ...
}
...
```

Now add a call to <samp class="function">showDetails</samp> in your <samp class="function">addThumbClickHandler</samp> function – no need to add a new event listener.

```
...
function addThumbClickHandler(thumb) {
  'use strict';
  thumb.addEventListener('click', function (event) {
    event.preventDefault();
    setDetailsFromThumb(thumb);
    showDetails();
  });
}
...
```

Save <samp class="filename">main.js</samp> and switch to your browser. Try out your new functionality: Hide the detail image, then click on a thumbnail to bring it back ([Figure 7.10](#ch07.html_fig-otters-return "Figure 7.10  Esc hides details; click shows details")). The otters look like they approve, don’t they?

**Figure 7.10  Esc hides details; click shows details**

![Esc hides details; click shows details](Ottergram/Transitions/img/otters-return.png)

Now, Ottergram can dynamically adapt its layout based on the viewport, using media queries, as well as in response to user input.

At the moment, the layout changes happen abruptly. In the next section, you will smooth that out using CSS transitions.

## State Changes with CSS Transitions

CSS transitions create a gradual change from one visual state to another, which is just what you need to make Ottergram’s show/hide effect more polished.

When you create a CSS transition, you are telling the browser, “I would like this element’s styles to change to these new properties, and I would like for that change to take exactly as long as I tell you.”

One common example is the fly-out menu seen on many sites, such as the small-screen version of [<samp class="uri">bignerdranch.com</samp>](http://www.bignerdranch.com). In a browser with a narrow viewport, clicking the menu icon makes the navigation menu appear from the top – but it does not appear all at once. Instead, it slides down from the header, visually animating from the initial state (hidden) to the end state (visible) ([Figure 7.11](#ch07s02.html_fig-hamburger "Figure 7.11  Fly-out navigation on bignerdranch.com")). Clicking the menu icon again causes the navigation menu to slide back up until it is hidden again.

**Figure 7.11  Fly-out navigation on `bignerdranch.com`**

![Fly-out navigation on bignerdranch.com](Ottergram/Transitions/img/hamburger.png)

Before you create the transition effect for showing and hiding the detail image, you will build a simpler transition for your thumbnails.

In general, you should create transitions in three steps:

1.  Decide what the end state should be. One good approach is to add the CSS declarations for the end state to the target element. This allows you to see them in the browser and make sure that they look the way you intend.

2.  Move the declarations from the target element’s existing declaration block to a new CSS declaration block. You may want to use a new class for the selector for the new block.

3.  Add a `transition` declaration to the target element. The `transition` property tells the browser that it will need to visually animate the changes from the current CSS values to the end-state CSS values and that the transition should take place over a specific period of time.

### Working with the transform property

Your first transition will increase the size of a thumbnail when you hover over it with the cursor ([Figure 7.12](#ch07s02.html_fig-zoom-effect-thumbnail "Figure 7.12  A thumbnail with zoom effect")). However, you will not directly change the `width` or `height` styles. You will use the <samp class="firstterm">transform</samp> property, which can alter the shape, size, rotation, and location of an element without interrupting the flow of the elements around it.

**Figure 7.12  A thumbnail with zoom effect**

![A thumbnail with zoom effect](Ottergram/Transitions/img/zoom-effect-thumbnail.png)

The target element for this transition is the `.thumbnail-item`. You will begin by adding a `transform` declaration directly to the `.thumbnail-item` element.

After you have tested it and determined that it is working the way you want, you will move the transformation to a new `.thumbnail-item:hover` declaration block. Finally, you will add a `transition` declaration to `.thumbnail-item`.

In <samp class="filename">styles.css</samp>, begin by adding a `transform` declaration to `.thumbnail-item`.

```
...
.thumbnail-item {
  display: inline-block;
  min-width: 120px;
  max-width: 120px;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);

  transform: scale(2.2);
}
...
```

`transform: scale(2.2)` tells the browser that the element should be drawn at 220% of its original size. There are many values that can be used with `transform`, including advanced 3D effects. The MDN has good coverage of them at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​CSS/​transform</samp>](https://developer.mozilla.org/en-US/docs/Web/CSS/transform).

Save and view the changes in your browser ([Figure 7.13](#ch07s02.html_fig-huge-thumbnails "Figure 7.13  Dramatically large otter thumbnails")).

**Figure 7.13  Dramatically large otter thumbnails**

![Dramatically large otter thumbnails](Ottergram/Transitions/img/unhappy-otters.png)

You can see that the thumbnails are now much larger than before. In fact, they are too large. Change the value so that they are only a little bit larger:

```
...
.thumbnail-item {
  display: inline-block;
  min-width: 120px;
  max-width: 120px;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);

  transform: scale(2.2);
  transform: scale(1.2);
}
...
```

After you save, you should see that the otter thumbnails are only slightly larger than their original size ([Figure 7.14](#ch07s02.html_fig-little-larger-thumbnails "Figure 7.14  Reasonably large otter thumbnails")).

**Figure 7.14  Reasonably large otter thumbnails**

![Reasonably large otter thumbnails](Ottergram/Transitions/img/reasonably-large-thumbnails.png)

This scale for the thumbnails looks good, so you can move on to the next step.

### Adding a CSS transition

Now it is time to move the end-state style to a new style declaration and set up the transition for the `.thumbnail-item` element.

When the user hovers the mouse cursor over a thumbnail, that thumbnail should increase its `scale` by 120%. Add a declaration block to <samp class="filename">styles.css</samp> that uses the modifier `:hover` to designate styles that should only be applied when the user hovers over the element.

```
...
.thumbnail-item {
  display: inline-block;
  min-width: 120px;
  max-width: 120px;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);

  transform: scale(1.2);
}

.thumbnail-item:hover {
  transform: scale(1.2);
}
...
```

The proper name for this modifier is <samp class="firstterm">pseudo-class</samp>. The psuedo-class `:hover` matches an element when the user holds the mouse cursor over it. There are a number of pseudo-class keywords that describe the various states an element can be in. You will encounter some when you work with forms later in this book, and you can search the MDN to learn more.

Next, make this change happen as a transition by adding a `transition` declaration to `.thumbnail-item` in <samp class="filename">styles.css</samp>. You need to specify the property to animate and how long the animation should take.

```
...
.thumbnail-item {
  display: inline-block;
  min-width: 120px;
  max-width: 120px;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);

  transition: transform 133ms;
}

.thumbnail-item:hover {
  transform: scale(1.2);
}
...
```

You set a `transition` for the `transform` property. This tells the browser that it will need to animate the change, but only for the `transform` property. You also specified that the transition should take place over a period of 133 milliseconds.

Save and give your new transition a try. You should see that each thumbnail enlarges when you hover over it. When you move your mouse away, the transition runs in reverse, and the thumbnail returns to its original size ([Figure 7.15](#ch07s02.html_fig-hover-in-out "Figure 7.15  Transition occurs when hovering, reverses on mouse out")).

**Figure 7.15  Transition occurs when hovering, reverses on mouse out**

![Transition occurs when hovering, reverses on mouse out](Ottergram/Transitions/img/hover-in-out.png)

The DevTools give you a handy way to test pseudo-class states. Go to the elements panel and expand the tags until one of the `<li>` tags is displayed. Click the tag so that it is highlighted and you will see an ellipsis to the left. Click the ellipsis, and in the contextual menu that is revealed choose `:hover` from the list of pseudo-classes ([Figure 7.16](#ch07s02.html_fig-pseudo-menu "Figure 7.16  Toggling a pseudo-class in the elements panel")).

**Figure 7.16  Toggling a pseudo-class in the elements panel**

![Toggling a pseudo-class in the elements panel](Ottergram/Transitions/img/right-click-to-set-pseudo-class.png)

An orange circle appears to the left of the `<li>` tag in the elements panel, telling you that one of the pseudo-classes has been activated via the DevTools. The corresponding thumbnail will remain in the `:hover` state, even if you mouse over it and then mouse away from it.

Open the contextual menu again, by clicking the orange circle, and disable the `:hover` state before you continue.

Your transition is nice, but there is a small bug. Currently, the hover effect causes parts of the thumbnail to be cut off. This is because the `transform` applied to the `.thumbnail-item` does not cause its parent to adjust <samp class="emphasis">its</samp> size. The solution is to add a bit of padding to the `.thumbnail-list`. Change the vertical padding for `.thumbnail-list` in <samp class="filename">styles.css</samp>.

```
...
.thumbnail-list {
  flex: 0 1 auto;
  order: 2;
  display: flex;
  justify-content: space-between;
  list-style: none;
  padding: 0;
  padding: 20px 0;

  white-space: nowrap;
  overflow-x: auto;
}
...
```

You used the shorthand for the `padding` property. The first value, `20px`, applies to the top and bottom padding, while the second value applies to the left and right padding. Make a similar adjustment inside your `@media` query, but add an extra padding of `35px` to the left and right.

```
...
@media all and (min-width: 768px) {
  .main-content {
  ...
  }

  .thumbnail-list {
    flex-direction: column;
    order: 0;
    margin-left: 20px;

    padding: 0 35px;
  }
  ...
```

Save and check the results in your browser. This produces a nicer effect for the thumbnails ([Figure 7.17](#ch07s02.html_fig-breathing-room "Figure 7.17  Extra room for the hover effect in portrait and landscape")).

**Figure 7.17  Extra room for the hover effect in portrait and landscape**

![Extra room for the hover effect in portrait and landscape](Ottergram/Transitions/img/breathing-room.png)

### Using a timing function

Your hover effect is looking good! But it lacks that visual <samp class="emphasis">pop</samp> that would make it really special. With CSS transitions, you can not only specify how much time a transition should take, but also make it transition at different speeds during that time.

There are several timing functions that you can use with transitions. By default, the <samp class="firstterm">linear</samp> timing function is used, which makes the transition animate at a single, constant rate. The others are more interesting, and give the transition the feeling of speeding up or slowing down.

Update your transition in <samp class="filename">styles.css</samp> so that it uses the `ease-in-out` timing function. This will make the rate of the transition slower at the beginning and end and faster in the middle.

```
...
.thumbnail-item {
  display: inline-block;
  min-width: 120px;
  max-width: 120px;
  border: 1px solid rgb(100%, 100%, 100%);
  border: 1px solid rgba(100%, 100%, 100%, 0.8);

  transition: transform 133ms ease-in-out;
}
...
```

Save and then hover over one of your thumbnails. The effect is subtle, but noticeable.

There are a number of timing functions available. See the list on the MDN at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​CSS/​transition-timing-function</samp>](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function).

Your `transition` uses the same duration value and timing function for both the transition <samp class="emphasis">to</samp> the end state and the transition <samp class="emphasis">from</samp> the end state. That does not have to be the case – you can use different values depending on the direction of the transition. If you specify a `transition` property on both the beginning-state declaration and the end-state declaration, the browser uses the value of the declaration it is moving toward.

It might be easier to see this in action. For a quick demonstration, add a `transition` declaration to `.thumbnail-item:hover` in <samp class="filename">styles.css</samp>. (You will delete it after trying it out in the browser.)

```
...
.thumbnail-item:hover {
  transform: scale(1.2);
  transition: transform 1000ms ease-in;
}
...
```

Save and again hover over one of the thumbnails in the browser. The scaling effect will be very slow, taking a full second to complete. This is because it is using the value declared for `.thumbnail-item:hover`. Now, move your mouse off of the thumbnail. This time, the transition takes 133 milliseconds, the value declared for `.thumbnail-item`.

Remove the `transition` declaration from `.thumbnail-item:hover` before you continue.

```
...
.thumbnail-item:hover {
  transform: scale(1.2);
  transition: transform 1000ms ease-in;
}
...
```

### Transition on class change

Your second transition will make the `.detail-image-frame` look like it is zooming in from very far away.

Instead of using a pseudo-class selector to trigger a transition, this time you will add and remove class names with JavaScript to trigger a transition. Why? Because there is no pseudo-class that corresponds to a click event. Using JavaScript gives you much more control over how and when these UI changes are triggered.

Also, you will set different duration times for the beginning and end of the transition. The end result will be that when you click a thumbnail the corresponding otter image will be used for the detail image. It will immediately be sized down to a tiny dot in the center of the detail area, then it will transition to its full size ([Figure 7.18](#ch07s02.html_fig-little-big "Figure 7.18  Clicking a thumbnail scales it from very small to full size")).

**Figure 7.18  Clicking a thumbnail scales it from very small to full size**

![Clicking a thumbnail scales it from very small to full size](Ottergram/Transitions/img/little-big.png)

Start by adding a style declaration for a new class named `is-tiny` in <samp class="filename">styles.css</samp>.

```
...
.detail-image-frame {
  ...
}

.is-tiny {
  transform: scale(0.001);
  transition: transform 0ms;
}

.detail-image {
  ...
```

You added two styles for `.is-tiny`. The first `scale`s the element down to a small fraction of its original size. The second specifies that any `transition` for the `transform` property should last 0 milliseconds, applying the style change immediately. Put another way, going toward the `.is-tiny` class styles, the detail image will effectively have no transition. Because it lasts for 0 milliseconds, there is no need to specify a timing function.

Next, you will add another `transition` declaration with a 333 millisecond duration. This value will be used when transitioning away from the `.is-tiny` class, making the detail image grow to normal size over a period of a third of a second. Add this `transition` declaration to the `.detail-image-frame` in <samp class="filename">styles.css</samp>.

```
...
.detail-image-frame {
  position: relative;
  text-align: center;

  transition: transform 333ms;
}
...
```

Save <samp class="filename">styles.css</samp> before you move on.

### Triggering transitions with JavaScript

Now that your transition styles are in place, you need to trigger them with JavaScript. To give your JavaScript a hook, add a data attribute to the `.detail-image-frame` element in <samp class="filename">index.html</samp>.

```
...
      <div class="detail-image-container">
        <div class="detail-image-frame" data-image-role="frame">
    <img class="detail-image" data-image-role="target" src="img/otter1.jpg" alt="">
    <span class="detail-image-title" data-image-role="title">Stayin' Alive</span>
        </div>
      </div>
...
```

Save <samp class="filename">index.html</samp>. Now, in <samp class="filename">main.js</samp>, you just need to add variables for your `.is-tiny` class and `data-image-role="frame"` selector, and then you will update <samp class="function">showDetails</samp> to perform the class name changes to that trigger the transition.

Begin with the variables. Add a `DETAIL_FRAME_SELECTOR` variable for a selector string `'[data-image-role="frame"]'`. Also, add a `TINY_EFFECT_CLASS` variable for the `is-tiny` class name.

```
var DETAIL_IMAGE_SELECTOR = '[data-image-role="target"]';
var DETAIL_TITLE_SELECTOR = '[data-image-role="title"]';
var DETAIL_FRAME_SELECTOR = '[data-image-role="frame"]';
var THUMBNAIL_LINK_SELECTOR = '[data-image-role="trigger"]';
var HIDDEN_DETAIL_CLASS = 'hidden-detail';
var TINY_EFFECT_CLASS = 'is-tiny';
var ESC_KEY = 27;
...
```

It is not required that you put your variables in this order. (It makes no difference to the browser.) But it is a good idea to keep them organized. In <samp class="filename">main.js</samp>, all of the selector variables are grouped together, followed by the class variables, followed by the numeric code for the Escape key.

Now, update <samp class="function">showDetails</samp> in <samp class="filename">main.js</samp> so that it gets a reference to the `[data-image-role="frame"]` element. To trigger the `transition`, you will need to add the `TINY_EFFECT_CLASS` and remove it.

```
...
function showDetails() {
  'use strict';
  var frame = document.querySelector(DETAIL_FRAME_SELECTOR);
  document.body.classList.remove(HIDDEN_DETAIL_CLASS);
  frame.classList.add(TINY_EFFECT_CLASS);
  frame.classList.remove(TINY_EFFECT_CLASS);
}
...
```

If you saved this and tried it in the browser, you would not see a transition take place. Why not? Because the `TINY_EFFECT_CLASS` is added and then immediately removed. The net result is that there is no actual class change to render. This is an optimization on the part of the browser.

You need to add a small delay before removing the `TINY_EFFECT_CLASS`. JavaScript, however, does not have a built-in delay or sleep function, as some other languages do. Time for a workaround!

You are going to use the <samp class="methodname">setTimeout</samp> method, which takes a function and a delay (specified in milliseconds). After the delay, the function is queued for execution by the browser.

Add a call to <samp class="methodname">setTimeout</samp> after calling <samp class="methodname">frame.classList.add</samp> in <samp class="filename">main.js</samp>. Pass it two arguments: a function with a list of steps to perform and the number of milliseconds to wait before invoking that function argument. There is only one step to perform, and that is to remove `TINY_EFFECT_CLASS`.

```
...
function showDetails() {
  'use strict';
  var frame = document.querySelector(DETAIL_FRAME_SELECTOR);
  document.body.classList.remove(HIDDEN_DETAIL_CLASS);
  frame.classList.add(TINY_EFFECT_CLASS);
  setTimeout(function () {
    frame.classList.remove(TINY_EFFECT_CLASS);
  }, 50);
}
...
```

Let’s take a closer look at what this code does. First, it adds the `.is-tiny` class to the `frame` element. This applies your `transform: scale(0.001)`.

Then, the browser is told to wait 50 milliseconds, after which it will add an anonymous function to its execution queue. The <samp class="function">showDetails</samp> function finishes. Fifty milliseconds later, the anonymous function is queued for execution. (Basically, it gets in line for the CPU, waiting behind any other functions that were already in line.)

When this anonymous function runs, it removes the `TINY_EFFECT_CLASS` from the `frame`’s class list. This causes the `transform` transition to run over a period of 333 milliseconds, making the `frame` grow to its normal size.

Save your changes and admire the results. Click the thumbnails and enjoy those wacky otters zooming into view.

## Custom Timing Functions

Now, for some icing on your Ottergram cake: You can create custom timing functions for your transitions instead of being limited to the built-in ones.

Timing functions can be graphed to show the transition’s progress over time. Graphs of the built-in timing functions (from the site [<samp class="uri">cubic-bezier.com</samp>](http://cubic-bezier.com)) are shown in [Figure 7.19](#ch07s03.html_fig-cubic-bezier-builtins "Figure 7.19  Built-in timing functions").

**Figure 7.19  Built-in timing functions**

![Built-in timing functions](Ottergram/Transitions/img/cubic-bezier-builtins.png)

The shapes in these graphs are known as <samp class="firstterm">cubic Bezier curves</samp>. The lines in the graphs describe the behavior of the animation over time. They are defined by four points. You can create custom transitions by specifying the four points that define a curve. Try the following `cubic-bezier` as part of your `transition` declaration for `.detail-image-frame` in <samp class="filename">styles.css</samp>.

```
...
.detail-image-frame {
  position: relative;
  text-align: center;

  transition: transform 333m cubic-bezier(1,.06,.28,1);
}
...
```

Save it and click on some thumbnails in the browser to see the difference in the transition.

Thanks to developer Lea Verou and her site [<samp class="uri">cubic-bezier.com</samp>](http://cubic-bezier.com), creating custom timing functions is painless ([Figure 7.20](#ch07s03.html_fig-cubic-bezier "Figure 7.20  Creating a custom timing function with cubic-bezier.com")).

**Figure 7.20  Creating a custom timing function with `cubic-bezier.com`**

![Creating a custom timing function with cubic-bezier.com](Ottergram/Transitions/img/cubic-bezier.png)

On the left side is a curve with red and blue drag handles. The curve is a graph of how much of the transition has occurred over the duration. Click and drag the handles to change the curve. As it changes, the decimal values at the top of the page change, too.

On the right side are the built-in timing functions: `ease`, `linear`, `ease-in`, `ease-out`, and `ease-in-out`. Click on one, then on the <samp class="guibutton">GO!</samp> button next to <samp class="guilabel">Preview & compare</samp>. The icons representing the two timing functions – the custom `cubic-bezier` and the built-in function – will animate, allowing you to see your custom timing in action and compare it to a built-in option.

Create a custom timing function and, when you are happy with it, copy and paste the values from the website to your code in <samp class="filename">styles.css</samp>:

```
...
.detail-image-frame {
  position: relative;
  text-align: center;

  transition: transform 333m cubic-bezier(your values here);
}
...
```

Congratulations! Ottergram is feature-complete! Save your file and admire your finished product. You have taken Ottergram from a simple, static web page to an interactive, responsive page with animated visual effects.

You have come a long way, and hopefully you have enjoyed learning about the basics of front-end development. It is time to wave goodbye to the otters, because you will be starting a new project in the next chapter.

## For the More Curious: Rules for Type Coercion

As mentioned in [Chapter 6](#ch06.html "6 Handling Events with JavaScript"), JavaScript was originally created so that folks who were not professional programmers could add interactivity to web pages. It was thought that these “regular humans” should not need to worry about whether a value was a number, an object, or a banana. (Just kidding – there is no banana type in JavaScript.)

One of the ways this is achieved is through type coercion. With type coercion, you can compare two values, regardless of their types, using the `==` operator and concatenate two values using the `+` operator. When you do, JavaScript will figure out a way to make that work – even if it has to do something a little weird, like changing the string `"2"` to the number `2`.

This has mystified programmers and nonprogrammers alike. Most programmers agree that it is best to use strict comparison using the `===` operator. However, the rules for type coercion are very well defined in the language, and they are worth knowing about.

Let’s say you are trying to compare two variables: `x == y`. If they are the same type and have the same value, the comparison results in a Boolean `true`. The only exception to this is: If either `x` or `y` have the value `NaN` (the language constant meaning “not a number”), then the result is `false`.

However, if `x` and `y` are different types, things get a bit tricky. Here are some of the rules JavaScript applies:

*   These comparisons result in `true`: `null == undefined` and `undefined == null`.

*   When comparing a string and a number, first convert the string to its numerical equivalent. This means that `"3" == 3` is `true`, and `"dog" == 20` is `false`.

*   When comparing a Boolean to another type, first convert the Boolean to a number: `true` to the number `1`, and `false` to the number `0`. This means that `false == 0` is `true`, and `true == 1` is also `true`.

*   Finally, if you compare a string or a number to an object, first try to convert the object to a primitive value. If that conversion does not work, then try converting the object to a string.

For even more information, check out the MDN’s discussion at [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​JavaScript/​Equality_comparisons_and_sameness</samp>](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness).

# <samp class="part_number">Part II</samp>
<samp class="part_name">Modules, Objects, and Forms</samp>

# <samp class="chapter_number">8</samp>
<samp class="chapter_name">Modules, Objects, and Methods</samp>

Over the next seven chapters, you will build a shopping-cart style application called CoffeeRun to manage coffee orders for a food truck. You will create CoffeeRun in three layers of code: the UI, the internal logic, and the server communication.

In this chapter, you will create the internal logic and interact with it through the DevTools console, as shown in [Figure 8.1](#ch08.html_fig-end-of-chap "Figure 8.1  CoffeeRun, under the hood").

**Figure 8.1  CoffeeRun, under the hood**

![CoffeeRun, under the hood](CoffeeRun/Modules/img/excelsior.png)

## Modules

CoffeeRun is more complex than Ottergram, so it is important to organize your code to make it easier to debug and to extend. CoffeeRun will be structured in components, which are diagrammed in [Figure 8.2](#ch08.html_fig-architecture "Figure 8.2  Overview of components and interactions in CoffeeRun").

**Figure 8.2  Overview of components and interactions in CoffeeRun**

![Overview of components and interactions in CoffeeRun](CoffeeRun/Modules/img/architecture.png)

Each part of the application will focus on one area of responsibility. The code for your application’s internal logic will manage the data. The UI code will handle events and DOM manipulation (much like the code for Ottergram). The server communication code will talk to a remote server, saving and retrieving data over the network.

JavaScript was created for writing very small scripts that add tiny bits of interactivity, not for writing complex applications. CoffeeRun is not extremely complex, but it breaks the threshold for what should be accomplished in a single script file.

To keep your code neatly separated, you will create three JavaScript files for the subsets of functionality within your application. You will have different files for your internal logic, your UI, and your server communication code. You will achieve this separation by writing your code in separate units, or <samp class="firstterm">modules</samp>.

How to group code into modules is entirely up to the developer. Most often, code is grouped around concepts, like “inventory” or “food menu.” In terms of code, modules group related functions together. Some of the functions will be available externally, while others will only be used internally by the module.

Think about a restaurant. The kitchen has lots of tools and ingredients that are available internally, but the customers only see a menu with a few items. That menu is the customer’s interface to the food-making module called the kitchen.

Likewise, if the restaurant has a bar, the drink-making tools and ingredients are internal; the customer can only access the items on the drink list, which is their interface to the drink-making module called the bar.

As a customer, you cannot borrow the butcher’s knife from the kitchen or use the blender from the bar. You cannot grab an extra pat of butter from the refrigerator or pour an extra shot in your cocktail. You are restricted to the interfaces provided by the kitchen and bar modules.

Similarly, each of CoffeeRun’s modules will keep some of its functionality private. Only a portion of its functionality will be made publicly accessible, so that other modules can interact with it.

For CoffeeRun, you will continue to work in ES5, which is the best-supported version of JavaScript as of this writing. (Your next project, Chattrbox, will use the most recent version, ES6). ES5 does not have a formal way to organize code into self-contained modules, but you can get the same kind of organization by putting related code (variables and functions) inside the body of a function.

### The module pattern

Code can be organized using functions, but it is a common practice to use a variation of a regular function for this purpose. Before you get started with your new project, let’s take a brief look at the <samp class="firstterm">module pattern</samp> for organizing code, examining how a function from Ottergram could be rewritten as a module.

Here is the code for a basic module:

```
(function () {
  'use strict';
  // Code will go here
})();
```

If this is the first time you have seen this pattern, it probably looks rather odd. This is known as an <samp class="firstterm">immediately invoked function expression</samp> (or IIFE), and it is best to examine it from the inside out.

The main part of it is the anonymous function:

```
function () {
  'use strict';
  // Code will go here
}
```

You worked with anonymous functions in Ottergram, so this should be familiar.

Here, however, the anonymous function is enclosed in parentheses:

```
(function () {
  'use strict';
  // Code will go here
})
```

These enclosing parentheses are very important because they tell the browser, “Please do not interpret this code as a function declaration.”

The browser sees the parentheses and says, “Ah. OK. I get that I am looking at an anonymous function. I will hold off from doing anything with it.”

Most of the time, you use an anonymous function by passing it as an argument. In this case, you are calling it immediately. This is done with the empty pair of parentheses:

```
(function () {
  'use strict';
  // Code will go here
})()
```

When the browser sees the empty parentheses, it realizes that you want it to invoke whatever comes before them, and says, “Oh! I see that I’ve got an anonymous function that I can run!”

You may be thinking, “This is both crazy and useless.” Actually, you have already written code that works similarly. Recall Ottergram’s <samp class="function">initializeEvents</samp> function. After you declared it, you called it immediately and never called it again. Here is that code for reference.

```
function initializeEvents() {                 // Function declared
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);

  addKeyPressHandler();
}

initializeEvents();                          // Function called
```

The purpose of this function was to bundle some steps together and run them when the page loads. Here is that same code, rewritten as an IIFE. (You do not need to change your Ottergram code; this is just to illustrate the concept.)

```
function initializeEvents() {
(function () {
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);

  addKeyPressHandler();
}
})();

initializeEvents();
```

IIFEs are useful when you want to run some code once without creating any extra global variables or functions. To understand why this is important, consider the variables and functions you wrote for Ottergram.

In Ottergram, you built up a collection of useful functions and then called them as needed. These functions had names like <samp class="function">getThumbnailsArray</samp> and <samp class="function">addKeyPressHandler</samp>. Luckily, these names were unique. If you had tried to define two functions with the same name, the first one would have simply been replaced by the second one.

When you define functions or variables, they are added to the <samp class="firstterm">global namespace</samp> by default. This is the browser’s registry of all of the function and variable names for your JavaScript program, along with any built-in functions and variables. More generally, a <samp class="firstterm">namespace</samp> is the means by which code is organized: Code is organized in namespaces the same way files on your computer are organized in folders.

In CoffeeRun, you may have functions that could reasonably have the same name, like <samp class="function">add</samp> or <samp class="function">addClickHandler</samp>. Instead of adding them to the global namespace, where they could be accidentally overwritten, you can declare them inside of a function. This protects them from being accessed or overwritten by code outside of the function.

As you group code together in a module, you will want to make some, but not all, of the functionality accessible to the world outside of the module. To do this, you will take advantage of the fact that IIFEs, like any function, can accept arguments.

### Modifying an object with an IIFE

IIFEs are not only good for running set-up code, like Ottergram’s <samp class="function">initializeEvents</samp>. They are also good for running code that augments an object, which is usually passed in as an argument. To illustrate how this works, our friend <samp class="function">initializeEvents</samp> will be used once again.

Here is a version of <samp class="function">initializeEvents</samp> whose job is to modify the thumbnails by adding a click handler. (To simplify things, the <samp class="function">addKeyPressHandler</samp> call has been removed.)

```
function initializeEvents() {
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);
}

initializeEvents();
```

In this form, <samp class="function">initializeEvents</samp> modifies an array of thumbnails using <samp class="function">addThumbClickHandler</samp>. But it could also receive the array as an argument. To do that, you would declare a parameter as part of the function definition. Then, when you call it, you would pass in the array, like this:

```
function initializeEvents(thumbnails) {
  'use strict';
  var thumbnails = getThumbnailsArray();
  thumbnails.forEach(addThumbClickHandler);
}

var thumbnails = getThumbnailsArray();
initializeEvents(thumbnails);
```

To rewrite this as an IIFE, you would remove the function name, wrap the function in parentheses, and add a pair of empty parentheses to invoke the function:

```
(function initializeEvents(thumbnails) {
  'use strict';
  thumbnails.forEach(addThumbClickHandler);
})();

var thumbnails = getThumbnailsArray();
initializeEvents(thumbnails);
```

However, you would still need to pass in the array of thumbnails as an argument. You can do this by moving the call to <samp class="function">getThumbnailsArray</samp>. Instead of assigning the result to a variable, you would pass the result to your IIFE:

```
(function (thumbnails) {
  'use strict';
  thumbnails.forEach(addThumbClickHandler);
})(getThumbnailsArray());

var thumbnails = getThumbnailsArray();
```

In this version of the code, an array (resulting from calling <samp class="function">getThumbnailsArray</samp>) is passed in to the IIFE. The IIFE receives this array and places the label <samp class="varname">thumbnails</samp> on it. Inside the body of the IIFE, the event listeners are attached to each item in the array ([Figure 8.3](#ch08.html_fig-iife-modifies "Figure 8.3  IIFE modifying its arguments")).

**Figure 8.3  IIFE modifying its arguments**

![IIFE modifying its arguments](CoffeeRun/Modules/img/iife-modifies.png)

Anything can be passed to an IIFE for modification. Your CoffeeRun IIFEs will be passed the `window` object. But instead of attaching their module code directly to the global namespace, they will attach code to a single <samp class="varname">App</samp> property <samp class="emphasis">within</samp> the global namespace. Every CoffeeRun module will be contained in its own file and loaded into the browser by an individual `<script>` tag. An overview of this process is shown in [Figure 8.4](#ch08.html_fig-script-iife-app "Figure 8.4  <script> tags load modules, which modify window.App").

**Figure 8.4  `<script>` tags load modules, which modify `window.App`**

![<script> tags load modules, which modify window.App](CoffeeRun/Modules/img/script-iife-app.png)

## Setting Up CoffeeRun

Enough theory – let’s get to work. Because this is a new project, start by creating a new directory. Open <samp class="application">Atom</samp> and choose <samp class="guimenu">File</samp> → <samp class="guimenuitem">Add Project Folder...</samp>. Select your <samp class="filename">front-end-dev-book</samp> directory and click <samp class="guibutton">New Folder</samp>. Name the new folder <samp class="filename">coffeerun</samp> and click <samp class="guibutton">Open</samp>.

Next, Control-click (right-click) your new <samp class="filename">coffeerun</samp> folder in <samp class="application">Atom</samp>’s navigation panel. Choose <samp class="guilabel">New File</samp> and enter <samp class="filename">index.html</samp> for the filename. Control-click (right-click) on <samp class="filename">coffeerun</samp> again and choose <samp class="guilabel">New Folder</samp>. Name the folder <samp class="filename">scripts</samp>.

In your <samp class="filename">front-end-dev-book</samp> folder, you should now have a folder for each of your projects, <samp class="filename">ottergram</samp> and <samp class="filename">coffeerun</samp>, with similar file structures ([Figure 8.5](#ch08s02.html_fig-folder-setup "Figure 8.5  Creating files and folders for CoffeeRun")).

**Figure 8.5  Creating files and folders for CoffeeRun**

![Creating files and folders for CoffeeRun](CoffeeRun/Modules/img/folder-setup.png)

If you already have a terminal session open and running `browser-sync`, close `browser-sync` using Control-C. If you do not, open a new terminal window. Either way, change to your new <samp class="filename">coffeerun</samp> directory (refer to the commands in [Chapter 1](#ch01.html "1 Setting Up Your Development Environment") if you are not sure about how to do this) and start `browser-sync` again. As a reminder, the command to start it is `browser-sync start --server --files "stylesheets/*.css, scripts/*.js, *.html"`.

In <samp class="filename">index.html</samp> add the basic skeleton of your document. (Remember, <samp class="application">Atom</samp>’s autocomplete will do most of this for you; just start typing “html.”)

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
  </head>
  <body>

  </body>
</html>
```

You are now ready to create your first module!

## Creating the DataStore Module

The first module you will write will store coffee order information in a simple database, not unlike writing down the orders by hand. Each order will be stored by the customer’s email address. To get started, you will only keep track of a text description of the order, like “quadruple espresso” ([Figure 8.6](#ch08s03.html_fig-database "Figure 8.6  Initial structure of CoffeeRun’s database")).

**Figure 8.6  Initial structure of CoffeeRun’s database**

![Initial structure of CoffeeRun’s database](CoffeeRun/Modules/img/database.png)

Later, you will also keep track of the size, flavor, and caffeine strength of each coffee order. The customer’s email address will serve as the unique identifier for the entire order, so all of the order details will be associated with a single email address. (Sorry, coffee addicts! Only one order per customer.)

Create a new file called <samp class="filename">scripts/datastore.js</samp>. Next, in <samp class="filename">index.html</samp>, add the `<script>` tag to include the new file in your project.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
  </head>
  <body>
    <script src="scripts/datastore.js" charset="utf-8"></script>
  </body>
</html>
```

Save <samp class="filename">index.html</samp>. In `scripts/datastore.js`, begin with the basic IIFE for your module structure:

```
(function (window) {
  'use strict';
  // Code will go here
})(window);
```

Now that the skeleton of your module exists and has a corresponding `<script>` tag, it is time to attach it to the namespace for your application.

## Adding Modules to a Namespace

Many other programming languages have special syntax for creating modules and packaging them together. ES5 does not. Instead, you can get the same kind of organization using objects.

You can use objects to associate any kind of data with a key name. In fact, this is precisely how you will organize your modules. Specifically, you will use a single object as the namespace for your CoffeeRun application. This namespace is where individual modules register themselves, which makes them available for use by your other application code.

There are three steps to using IIFEs to register modules in a namespace:

1.  Get a reference to the namespace, if it exists.

2.  Create the module code.

3.  Attach your module code to the namespace.

Let’s see what that looks like in practice. Update your IIFE in <samp class="filename">datastore.js</samp> as shown. We will explain the code after you enter it.

```
(function (window) {
  'use strict';
  // Code will go here
  var App = window.App || {};

  function DataStore() {
    console.log('running the DataStore function');
  }

  App.DataStore = DataStore;
  window.App = App;
})(window);
```

In the body of the IIFE, you declared a local variable named <samp class="varname">App</samp>. If there is already an <samp class="varname">App</samp> property of the `window`, you assign the local <samp class="varname">App</samp> to it. If not, the label <samp class="varname">App</samp> will refer to a new, empty object, represented by `{}`. The `||` is the <samp class="firstterm">default operator</samp>, otherwise known as the <samp class="firstterm">logical or operator</samp>. It can be used to provide a valid value (in this case, `{}`) if the first choice (`window.App`) has not yet been created.

Each of your modules will do this same check. It is like saying “Whoever gets there first: Go ahead and start a new object. Everyone else will use that object.”

Next, you declared a function named <samp class="function">DataStore</samp>. You will add more code to this function shortly.

Finally, you attached <samp class="function">DataStore</samp> to the <samp class="varname">App</samp> object and reassigned the global <samp class="varname">App</samp> property to your newly modified <samp class="varname">App</samp>. (If it did not already exist and you had to create it as an empty object, you must attach it.)

Save your files and switch over to the browser. Open the DevTools, click on the tab for the console, and call your <samp class="function">DataStore</samp> function with the following code:

```
App.DataStore();
```

<samp class="function">DataStore</samp> runs and prints some text to the console ([Figure 8.7](#ch08s04.html_fig-running-datastore "Figure 8.7  Running the App.DataStore function")).

**Figure 8.7  Running the `App.DataStore` function**

![Running the App.DataStore function](CoffeeRun/Modules/img/running-datastore.png)

Notice that you did not need to write `window.App.DataStore();`. This is because the `window` object is the global namespace. All of its properties are available to any JavaScript code you write, including in the console.

## Constructors

IIFEs let you take advantage of function scope to create namespaces to organize large pieces of your code. There is another use of functions that makes them act like factories for objects that all have similar properties and methods. In other languages, you might use a class for this kind of organization. Strictly speaking, JavaScript does not have classes, but it does give you a way to create custom types.

You have already started to create the <samp class="function">DataStore</samp> type. Now you will customize it in two steps. In the first step, you will give it a property that will be used internally for storing data. In the second step, you will give it a set of methods for interacting with that data. You do not need to give other objects direct access to that data, so this type will provide an external interface through a set of methods.

Object factory functions are called <samp class="firstterm">constructors</samp> in JavaScript.

Add the following code to the body of the <samp class="function">DataStore</samp> function in <samp class="filename">datastore.js</samp>.

```
(function (window) {
  'use strict';
  var App = window.App || {};

  function DataStore() {
    console.log('running the DataStore function');
    this.data = {};
  }

  App.DataStore = DataStore;
  window.App = App;
})(window);
```

The job of a constructor is to create and customize a new object. Inside the body of the constructor, you can refer to that new object with the keyword `this`. You used the dot operator to create a property named `data` on your new object and assigned an empty object to `data`.

You may have noticed that you capitalized the first letter of <samp class="function">DataStore</samp>. This is a convention in JavaScript when naming constructors. It is not necessary, but it is a good practice as a way to tell other developers that the function should be used as a constructor.

To differentiate a constructor from a regular function, you use the keyword `new` when you call it. This tells JavaScript to create a new object, set up the reference from `this` to that new object, and to <samp class="firstterm">implicitly</samp> `return` that object. That means it will `return` the object without an explicit `return` statement in the constructor.

Save and return to the console. To learn how to use a constructor, you are going to create two <samp class="function">DataStore</samp> objects (or <samp class="firstterm">instances</samp>) and add values to them. Begin by creating the instances.

```
var dsOne = new App.DataStore();
var dsTwo = new App.DataStore();
```

You created these <samp class="function">DataStore</samp> instances by calling the <samp class="function">DataStore</samp> constructor. At this point, each has an empty `data` property. Add some values to them:

```
dsOne.data['email'] = 'james@bond.com';
dsOne.data['order'] = 'black coffee';
dsTwo.data['email'] = 'moneypenny@bond.com';
dsTwo.data['order'] = 'chai tea';
```

Then inspect the values:

```
dsOne.data;
dsTwo.data;
```

The results tell you that each instance holds different information ([Figure 8.8](#ch08s05.html_fig-new-datastores-with-data "Figure 8.8  Saving values to instances of the DataStore constructor")).

**Figure 8.8  Saving values to instances of the `DataStore` constructor**

![Saving values to instances of the DataStore constructor](CoffeeRun/Modules/img/new-datastores-with-data.png)

### A constructor’s prototype

Using a <samp class="function">DataStore</samp> instance, you can manually store and retrieve data. But, in its current form, <samp class="function">DataStore</samp> is just a roundabout way of creating an object literal, and any module that will use a <samp class="function">DataStore</samp> instance has to be coded to use the <samp class="varname">data</samp> property directly.

This is not good software design. It would be better if <samp class="function">DataStore</samp> provided a public interface for adding, removing, and retrieving data – all while keeping the details of how it works a secret.

The second part of creating your custom <samp class="function">DataStore</samp> type is to provide these methods for interacting with the data. The goal is for these methods to serve as the interface that other modules use when they interact with a <samp class="function">DataStore</samp> instance. To accomplish this, you will make use of a very cool feature of JavaScript functions, the <samp class="firstterm">prototype</samp> property.

Functions in JavaScript are also objects. This means that they can have properties. In JavaScript, all instances created by a constructor have access to a shared storehouse of properties and methods: the `prototype` property of the constructor.

To create these instances, you used the `new` keyword when you called the constructor. The `new` keyword not only creates your instance and returns it but also creates a special link from the instance to the constructor’s `prototype` property. This link exists for any instance created when the constructor is created with the `new` keyword.

When you add a property to the `prototype` and assign it a function, every instance you create with the constructor will have access to that function. You can use the keyword `this` inside of the function body, and it will refer to the instance.

To see this in action, create the <samp class="function">add</samp> function in <samp class="filename">datastore.js</samp> as a property of the prototype. You can also delete the call to `console.log`.

```
(function (window) {
  'use strict';
  var App = window.App || {};

  function DataStore() {
    console.log('running the DataStore function');
    this.data = {};
  }

  DataStore.prototype.add = function (key, val) {
    this.data[key] = val;
  };

  App.DataStore = DataStore;
  window.App = App;
})(window);
```

You gave `DataStore.prototype` the property <samp class="methodname">add</samp> and you assigned a function to it. That function takes two arguments, `key` and `val`. Inside the function body, you used those arguments to make changes to the instance’s `data` property.

In terms of how <samp class="function">DataStore</samp> works with coffee orders, it will store the order information (the `val`), using the customer’s email address (the `key`).

You are not setting up a true database, but <samp class="function">DataStore</samp> works well enough for CoffeeRun. It is able to save some information, `val`, under the unique identifier specified by `key`. Because you are using a JavaScript object for storage, each `key` is guaranteed to be a unique entry in the database. (In a JavaScript object, a property name is always unique, like function names within a namespace. If you tried to store different values using the same key, you would just overwrite any previous values for that key.)

This aspect of JavaScript objects fulfills the one major requirement of any database: keeping the individual pieces of data separate.

Save your code and switch back to the browser. Create an instance of <samp class="function">DataStore</samp> in the console and use its <samp class="methodname">add</samp> method to store some information.

```
var ds = new App.DataStore();
ds.add('email', 'q@bond.com');
ds.add('order', 'triple espresso');
ds.data;
```

Inspect the `data` property to confirm that it works ([Figure 8.9](#ch08s05.html_fig-using-add-prototype-method "Figure 8.9  Calling a prototype method")).

**Figure 8.9  Calling a prototype method**

![Calling a prototype method](CoffeeRun/Modules/img/using-add-prototype-method.png)

### Adding methods to the constructor

The next thing to do is to create methods for accessing the data. In <samp class="filename">datastore.js</samp>, add a method to look up a value based on a given key and one to look up all keys and values.

```
...
  DataStore.prototype.add = function (key, val) {
    this.data[key] = val;
  };

  DataStore.prototype.get = function (key) {
    return this.data[key];
  };

  DataStore.prototype.getAll = function () {
    return this.data;
  };

  App.DataStore = DataStore;
  window.App = App;
})(window);
```

You created a <samp class="methodname">get</samp> method that accepts a `key`, looks up the value for it in the instance’s `data` property, and `return`s it. You also created a <samp class="methodname">getAll</samp> method. It is almost the same, but instead of looking up the value for a single key, it returns a reference to the `data` property.

You can now add and retrieve information from a <samp class="function">DataStore</samp> instance. To complete the cycle, you need to add a method for removing information. Add that to <samp class="filename">datastore.js</samp> now.

```
...
  DataStore.prototype.getAll = function () {
    return this.data;
  };

  DataStore.prototype.remove = function (key) {
    delete this.data[key];
  };

  App.DataStore = DataStore;
  window.App = App;
})(window);
```

The `delete` operator removes a key/value pair from an object when your new <samp class="methodname">remove</samp> method is called.

With that, you have completed the <samp class="function">DataStore</samp> module, which provides the most important part of the CoffeeRun application. It can store data, provide stored data in response to queries, and delete unnecessary data on command.

To see all of your methods in action, save your code and go to the console after `browser-sync` has reloaded your browser. Enter the following code, which exercises all of the methods of <samp class="function">DataStore</samp>:

```
var ds = new App.DataStore();
ds.add('m@bond.com', 'tea');
ds.add('james@bond.com', 'eshpressho');
ds.getAll();
ds.remove('james@bond.com');
ds.getAll();
ds.get('m@bond.com');
ds.get('james@bond.com');
```

As shown in [Figure 8.10](#ch08s05.html_fig-ds-interface-exercise "Figure 8.10  Working with DataStore using only its prototype methods"), <samp class="function">DataStore</samp>’s instance methods should now work as expected. These methods are exactly the way that other modules will interact with your application’s database.

**Figure 8.10  Working with `DataStore` using only its prototype methods**

![Working with DataStore using only its prototype methods](CoffeeRun/Modules/img/ds-interface-exercise.png)

Your next module will use the same structure: an IIFE with a parameter for the namespace to modify. But it will provide completely different functionality from <samp class="function">DataStore</samp>.

## Creating the Truck Module

The next module you will write is the <samp class="function">Truck</samp> module, which will provide all of the functionality for managing the food truck. It will have methods for creating and delivering orders and for printing a list of pending orders. [Figure 8.11](#ch08s06.html_fig-truck-datastore "Figure 8.11  Truck module interacting with DataStore module") shows how the <samp class="function">Truck</samp> module will work with the <samp class="function">DataStore</samp> module.

**Figure 8.11  `Truck` module interacting with `DataStore` module**

![Truck module interacting with DataStore module](CoffeeRun/Modules/img/truck-datastore.png)

When a <samp class="function">Truck</samp> instance is created, it is given a <samp class="function">DataStore</samp> object. A <samp class="function">Truck</samp> has methods for working with coffee orders, but it should not need to worry about how to store and manage that information. Instead, the <samp class="function">Truck</samp> just passes those duties to the <samp class="function">DataStore</samp>. For example, when you call the <samp class="function">Truck</samp>’s <samp class="methodname">createOrder</samp> method, it calls the <samp class="function">DataStore</samp>’s <samp class="methodname">add</samp> method.

Create the <samp class="filename">scripts/truck.js</samp> file and add a `<script>` tag for it to <samp class="filename">index.html</samp>.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
  </head>
  <body>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
  </body>
</html>
```

Save <samp class="filename">index.html</samp>. In <samp class="filename">truck.js</samp>, set up your module with an IIFE and a constructor for the <samp class="function">Truck</samp> type.

```
(function (window) {
  'use strict';
  var App = window.App || {};

  function Truck() {
  }

  App.Truck = Truck;
  window.App = App;

})(window);
```

Next, you will add parameters to your constructor so that each instance will have a unique identifier and its own <samp class="function">DataStore</samp> instance. The identifier is just a name for differentiating one <samp class="function">Truck</samp> instance from another. The <samp class="function">DataStore</samp> instance will play a much more important role.

Add the new parameters in <samp class="filename">truck.js</samp>.

```
(function (window) {
  'use strict';
  var App = window.App || {};

  function Truck(truckId, db) {
    this.truckId = truckId;
    this.db = db;
  }

  App.Truck = Truck;
  window.App = App;

})(window);
```

You declared parameters for the `truckId` and the `db`, then you assigned each of them as properties to the newly constructed instance.

The <samp class="function">Truck</samp> instances will need methods for managing coffee orders, and you will add those next. Order data will include an email address and a drink specification.

### Adding orders

The first method to add is <samp class="methodname">createOrder</samp>. When this method is called, the <samp class="function">Truck</samp> instance will interact with its `db` property through the <samp class="function">DataStore</samp> methods you declared earlier. Specifically, you will call <samp class="function">DataStore</samp>’s <samp class="methodname">add</samp> method to store a coffee order, using the email address associated with the order.

Declare this new prototype method in <samp class="filename">truck.js</samp>.

```
...
  function Truck(truckId, db) {
    this.truckId = truckId;
    this.db = db;
  }

  Truck.prototype.createOrder = function (order) {
    console.log('Adding order for ' + order.emailAddress);
    this.db.add(order.emailAddress, order);
  };

  App.Truck = Truck;
  window.App = App;

})(window);
```

You log a message to the console in <samp class="methodname">createOrder</samp>, then you store the order information using `db`’s <samp class="methodname">add</samp> method.

Using the <samp class="methodname">add</samp> method was as simple as referring to the <samp class="function">Truck</samp>’s <samp class="varname">db</samp> instance variable and calling <samp class="methodname">add</samp>. You did not need to specify the <samp class="function">App.DataStore</samp> namespace or mention the <samp class="function">DataStore</samp> constructor anywhere in this module. Instances of <samp class="function">Truck</samp> are designed to work with anything that has the same method names as a <samp class="function">DataStore</samp>. There is no need for <samp class="function">Truck</samp> to know any details beyond that.

Save your file and test <samp class="methodname">createOrder</samp> in the console using the following entries:

```
var myTruck = new App.Truck('007', new App.DataStore());
myTruck.createOrder({ emailAddress: 'dr@no.com', coffee: 'decaf'});
myTruck.createOrder({ emailAddress: 'me@goldfinger.com', coffee: 'double mocha'});
myTruck.createOrder({ emailAddress: 'm@bond.com', coffee: 'earl grey'});
myTruck.db;
```

Your results should look like [Figure 8.12](#ch08s06.html_fig-using-createorder "Figure 8.12  Taking Truck.prototype.createOrder for a test drive").

**Figure 8.12  Taking `Truck.prototype.createOrder` for a test drive**

![Taking Truck.prototype.createOrder for a test drive](CoffeeRun/Modules/img/using-createorder.png)

When the console prints the value of `myTruck.db`, you will need to click the ![Taking Truck.prototype.createOrder for a test drive](CoffeeRun/Modules/img/arrow.png) icon so that you can see the nested properties (such as the `dr@no.com` property inside the `data` object).

### Removing orders

When an order is delivered, the <samp class="function">Truck</samp> instance should remove the order from its database. Add a new <samp class="methodname">deliverOrder</samp> method to the `Truck.prototype` object in <samp class="filename">truck.js</samp>.

```
...
  Truck.prototype.createOrder = function (order) {
    console.log('Adding order for ' + data.emailAddress);
    this.db.add(data.emailAddress, order);
  };

  Truck.prototype.deliverOrder = function (customerId) {
    console.log('Delivering order for ' + customerId);
    this.db.remove(customerId);
  };

  App.Truck = Truck;
  window.App = App;

})(window);
```

You assigned a function expression to <samp class="methodname">Truck.prototype.deliverOrder</samp>. This function accepts a `customerId` argument, which it then passes to <samp class="methodname">this.db.remove</samp>. The value of `customerId` should be the email address associated with an order.

Just like <samp class="methodname">createOrder</samp>, <samp class="methodname">deliverOrder</samp> is only interested in calling the <samp class="methodname">remove</samp> method of <samp class="varname">this.db</samp>. It does not need any details about how <samp class="methodname">remove</samp> actually works.

Save and switch to the console. Create a <samp class="function">Truck</samp> instance, add a few orders with <samp class="methodname">createOrder</samp>, and then make sure that <samp class="methodname">deliverOrder</samp> removes them from the instance’s `db`. (You can press Return or Shift-Return after each call to <samp class="methodname">createOrder</samp> and <samp class="methodname">deliverOrder</samp>, but make sure you press Return after each `myTruck.db` entry.)

```
var myTruck = new App.Truck('007', new App.DataStore());
myTruck.createOrder({ emailAddress: 'm@bond.com', coffee: 'earl grey'});
myTruck.createOrder({ emailAddress: 'dr@no.com', coffee: 'decaf'});
myTruck.createOrder({ emailAddress: 'me@goldfinger.com', coffee: 'double mocha'});
myTruck.db;
myTruck.deliverOrder('m@bond.com');
myTruck.deliverOrder('dr@no.com');
myTruck.db;
```

As you enter these test commands, you will see that the order information in `myTruck.db` changes after you call <samp class="methodname">deliverOrder</samp> ([Figure 8.13](#ch08s06.html_fig-using-deliverorder "Figure 8.13  Removing order data with Truck.prototype.deliverOrder")).

**Figure 8.13  Removing order data with `Truck.prototype.deliverOrder`**

![Removing order data with Truck.prototype.deliverOrder](CoffeeRun/Modules/img/using-deliverorder.png)

Note that the console shows you the state of the data <samp class="emphasis">at the time</samp> you click the ![Removing order data with Truck.prototype.deliverOrder](CoffeeRun/Modules/img/arrow.png) icon. If you do not inspect the values in `myTruck.db` until after calling <samp class="methodname">deliverOrder</samp>, it will seem as though the data was never added ([Figure 8.14](#ch08s06.html_fig-unexpected "Figure 8.14  Console shows values at time of clicking arrow icon")).

**Figure 8.14  Console shows values at time of clicking arrow icon**

![Console shows values at time of clicking arrow icon](CoffeeRun/Modules/img/unexpected.png)

## Debugging

Your last method to add to the `Truck.prototype` object is <samp class="methodname">printOrders</samp>. This method will get an array of all of the customer email addresses, iterate through the array, and <samp class="methodname">console.log</samp> the order information.

The code for this method is very similar to other functions and methods you have already written. But it will start out with a bug, which you will find using <samp class="application">Chrome</samp>’s debugging tools.

Let’s take this step by step. Start by creating the basic version of <samp class="methodname">printOrders</samp> in <samp class="filename">truck.js</samp>. In the body, you will retrieve all the coffee orders from the <samp class="varname">db</samp> object. Then you will use the <samp class="methodname">Object.keys</samp> method to get an array containing the email addresses for the orders. Finally, you will iterate through the email address array and run a callback function for each element in the array.

```
...
  Truck.prototype.deliverOrder = function (customerId) {
    console.log('Delivering order for ' + customerId);
    this.db.remove(customerId);
  };

  Truck.prototype.printOrders = function () {
    var customerIdArray = Object.keys(this.db.getAll());

    console.log('Truck #' + this.truckId + ' has pending orders:');
    customerIdArray.forEach(function (id) {
      console.log(this.db.get(id));
    });
  };

  App.Truck = Truck;
  window.App = App;

})(window);
```

Inside the new <samp class="methodname">printOrders</samp> method, you call <samp class="methodname">this.db.getAll</samp> to retrieve all the orders as key/value pairs and pass them to <samp class="methodname">Object.keys</samp>, which returns an array containing only the keys. You assign this array to the variable <samp class="varname">customerIdArray</samp>.

When you iterate through this array, you pass a callback to <samp class="methodname">forEach</samp>. In the body of that callback, you try to <samp class="methodname">get</samp> the order associated with an <samp class="varname">id</samp> (the customer email address).

Save and return to the console. Create a new instance of `Truck` and add some coffee orders. Then try your new <samp class="methodname">printOrders</samp> method.

```
var myTruck = new App.Truck('007', new App.DataStore());
myTruck.createOrder({ emailAddress: 'm@bond.com', coffee: 'earl grey'});
myTruck.createOrder({ emailAddress: 'dr@no.com', coffee: 'decaf'});
myTruck.createOrder({ emailAddress: 'me@goldfinger.com', coffee: 'double mocha'});
myTruck.printOrders();
```

Instead of a list of the coffee orders, you will see the error `Uncaught TypeError: Cannot read property 'db' of undefined` ([Figure 8.15](#ch08s07.html_fig-uncaught-error-this-db "Figure 8.15  Error when printOrders is run")).

**Figure 8.15  Error when `printOrders` is run**

![Error when printOrders is run](CoffeeRun/Modules/img/uncaught-error-this-db.png)

This is one of the most common errors that you will see when writing JavaScript. Many developers find it especially frustrating because it can be hard to pinpoint the cause. Knowing how to use the debugger, as you are about to do, is key to locating the problem.

### Locating bugs with the DevTools

Debugging requires you to reproduce the error as you progressively isolate the buggy code. The <samp class="application">Chrome</samp> debugger makes this process (almost) enjoyable.

When an error occurs, the console shows you the filename and the line number of the code that caused the error. (In [Figure 8.15](#ch08s07.html_fig-uncaught-error-this-db "Figure 8.15  Error when printOrders is run"), the reference is to `truck.js:30`; your line number might be different.) Click that text to open the offending line of code in the debugging tools ([Figure 8.16](#ch08s07.html_fig-offending-line "Figure 8.16  Viewing the error in the debugging tools")).

**Figure 8.16  Viewing the error in the debugging tools**

![Viewing the error in the debugging tools](CoffeeRun/Modules/img/offending-line.png)

You are now viewing the sources panel of the DevTools. Click the red icon in the problem line to see the error information ([Figure 8.17](#ch08s07.html_fig-callout "Figure 8.17  Error line called out in the sources panel")).

**Figure 8.17  Error line called out in the sources panel**

![Error line called out in the sources panel](CoffeeRun/Modules/img/callout.png)

This error message indicates that the browser thinks you are trying to read a property named `db`, but that the object it belongs to does not exist.

The next step is to run the code just up to the line that is causing the error and then check the value of that object. In the sources panel, click the line number to the left of the line with the error flag. This sets a <samp class="firstterm">breakpoint</samp> for the debugger, telling the browser to pause just before it tries to run this line. When you set a breakpoint, the line number on the left turns blue and an entry is added to the breakpoints panel on the right ([Figure 8.18](#ch08s07.html_fig-breakpoint-set "Figure 8.18  Setting a breakpoint")).

**Figure 8.18  Setting a breakpoint**

![Setting a breakpoint](CoffeeRun/Modules/img/breakpoint-set.png)

Press the Escape key to show the console at the bottom of the sources panel ([Figure 8.19](#ch08s07.html_fig-showing-console-drawer "Figure 8.19  Showing the console drawer")). This is also known as the <samp class="firstterm">drawer</samp>. You will need to be able to see the code in the sources panel and interact with the console at the same time.

**Figure 8.19  Showing the console drawer**

![Showing the console drawer](CoffeeRun/Modules/img/showing-console-drawer.png)

Run `myTruck.printOrders();` again in the console. The browser will activate the debugger, and your code will pause at the breakpoint ([Figure 8.20](#ch08s07.html_fig-paused "Figure 8.20  Debugger paused at breakpoint")).

**Figure 8.20  Debugger paused at breakpoint**

![Debugger paused at breakpoint](CoffeeRun/Modules/img/paused.png)

When the debugger pauses, you have access to all of the variables that are available at that point. Using the console, you can check the values of the variables, looking for signs of trouble.

Try to reproduce the error by evaluating parts of the line of code with the error flag. Start with the code that is nested furthest inside of any parentheses. In this case, that is the <samp class="varname">id</samp> variable. When you enter that on the console, it reports that the value is `m@bond.com` ([Figure 8.21](#ch08s07.html_fig-id "Figure 8.21  Inspecting the innermost value")).

**Figure 8.21  Inspecting the innermost value**

![Inspecting the innermost value](CoffeeRun/Modules/img/id.png)

Because that did not reproduce the error, try the code just outside that set of parentheses, `this.db.get(id)`. Evaluate it on the console. You should see that the error is reported ([Figure 8.22](#ch08s07.html_fig-reproduced-error "Figure 8.22  Reproducing the error")).

**Figure 8.22  Reproducing the error**

![Reproducing the error](CoffeeRun/Modules/img/reproduced-error.png)

Now you can further isolate the cause. Begin evaluating that same piece of code, but remove parts of it, starting from the right. You will do this until the error is no longer printed. Start with `this.db.get`. After that, enter `this.db`. The console continues to report the error ([Figure 8.23](#ch08s07.html_fig-grrr "Figure 8.23  The search continues")).

**Figure 8.23  The search continues**

![The search continues](CoffeeRun/Modules/img/grrr.png)

Finally, enter `this`. You are now at the point where the error is not happening ([Figure 8.24](#ch08s07.html_fig-found-it "Figure 8.24  Trimming down the code to find the cause of the error")).

**Figure 8.24  Trimming down the code to find the cause of the error**

![Trimming down the code to find the cause of the error](CoffeeRun/Modules/img/found-it.png)

Why does `this` have the value `undefined` inside of your callback? Inside of a callback function, `this` is not assigned to an object. You need to explicitly assign one.

This situation is different from your <samp class="methodname">Truck.prototype</samp> methods, where `this` refers to the instance of <samp class="function">Truck</samp>. Even though the callback is inside of <samp class="methodname">Truck.prototype.printOrder</samp>, it has its own `this` variable, which is <samp class="emphasis">not</samp> assigned to a value and is therefore `undefined`.

Before fixing your code, you should be familiar with two other ways you could have located the bug. If you mouse over the different parts of the code in the sources panel, the debugger will show you their values. With the mouse over `this`, it shows you that its value is `undefined` ([Figure 8.25](#ch08s07.html_fig-hover-debug "Figure 8.25  Hovering the mouse reveals values")).

**Figure 8.25  Hovering the mouse reveals values**

![Hovering the mouse reveals values](CoffeeRun/Modules/img/hover-debug.png)

To the right of the code is the scope panel, which contains a list of variables available. You can see that values for <samp class="varname">id</samp> and <samp class="varname">this</samp> are shown – and, again, that `this` is `undefined` ([Figure 8.26](#ch08s07.html_fig-scope-variable-list "Figure 8.26  Variable values shown in scope panel")).

**Figure 8.26  Variable values shown in scope panel**

![Variable values shown in scope panel](CoffeeRun/Modules/img/scope-variable-list.png)

Click the blue ![Variable values shown in scope panel](CoffeeRun/Modules/img/play.png) button at the top of the right hand panel ([Figure 8.27](#ch08s07.html_fig-controls "Figure 8.27  Debugger control panel")). This unpauses your code, allowing it to resume execution.

**Figure 8.27  Debugger control panel**

![Debugger control panel](CoffeeRun/Modules/img/controls.png)

Before moving on, remove the breakpoint by clicking the blue line number again. The blue indicator will disappear ([Figure 8.28](#ch08s07.html_fig-toggle-breakpoint "Figure 8.28  Click the line number to toggle a breakpoint")).

**Figure 8.28  Click the line number to toggle a breakpoint**

![Click the line number to toggle a breakpoint](CoffeeRun/Modules/img/toggle-breakpoint.png)

Now, it is time to fix that pesky bug!

### Setting the value of this with bind

In JavaScript, the keyword `this` inside of a function is automatically assigned a value when you call that function. For constructor functions and for prototype methods, the value of `this` is the instance object. The instance is called the <samp class="firstterm">owner</samp> of the function call. Using the keyword `this` gives you access to the properties of the owner.

As we said earlier, for callback functions `this` is not automatically assigned to an object. You can manually specify what object should be the owner by using a function’s <samp class="methodname">bind</samp> method. (Remember that JavaScript functions are actually objects and can have their own properties and methods, such as <samp class="methodname">bind</samp>.)

The <samp class="methodname">bind</samp> method accepts an object argument and returns a new version of the function. When you call the new version, it will use the object argument passed in to <samp class="methodname">bind</samp> as the value of `this` inside of the function’s body.

Inside the <samp class="methodname">forEach</samp> callback, `this` is `undefined` because the callback has no owner. Fix that by calling <samp class="methodname">bind</samp> and passing it a reference to the <samp class="function">Truck</samp> instance.

Add the call to <samp class="methodname">bind</samp> in <samp class="filename">truck.js</samp>.

```
...
  Truck.prototype.printOrders = function () {
    var customerIdArray = Object.keys(this.db.getAll());

    console.log('Truck #' + this.truckId + ' has pending orders:');
    customerIdArray.forEach(function (id) {
      console.log(this.db.get(id));
    }.bind(this));
  };
...
```

Outside the body of the <samp class="methodname">forEach</samp> callback, the keyword `this` refers to the <samp class="function">Truck</samp> instance. By adding `.bind(this)` immediately after the anonymous function – but inside the parentheses for the <samp class="methodname">forEach</samp> call – you are passing <samp class="methodname">forEach</samp> a modified version of the anonymous function. This modified version uses the <samp class="function">Truck</samp> instance as its owner.

Save and confirm that the orders are printed correctly. You will need to re-declare <samp class="varname">myTruck</samp> and run <samp class="function">createOrder</samp> again.

Your output should look like [Figure 8.29](#ch08s07.html_fig-printorders "Figure 8.29  printOrders works after using bind(this)").

**Figure 8.29  `printOrders` works after using `bind(this)`**

![printOrders works after using bind(this)](CoffeeRun/Modules/img/printorders-debugging-3.png)

## Initializing CoffeeRun on Page Load

Your <samp class="function">DataStore</samp> and <samp class="function">Truck</samp> modules work correctly. You have been able to instantiate a new <samp class="function">Truck</samp> on the console, supplying it a new <samp class="function">DataStore</samp> as part of its creation.

Now you are going to create a module that performs these same steps when the page loads. Create a <samp class="filename">scripts/main.js</samp> file and add a `<script>` tag to <samp class="filename">index.html</samp>.

```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
  </head>
  <body>
    <script src="scripts/datastore.js" charset="utf-8"></script>>
    <script src="scripts/truck.js" charset="utf-8"></script>>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

Save <samp class="filename">index.html</samp>. You are going to add an IIFE to <samp class="filename">main.js</samp>, as you have done with the other modules, but this time you will not need to export any new properties to `window.App`. Set up <samp class="filename">main.js</samp> as shown:

```
(function (window) {
  'use strict';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
})(window);
```

The job of this module is to receive the <samp class="varname">window</samp> object for use inside the function body. It also retrieves the constructors you defined as part of the <samp class="varname">window.App</samp> namespace.

Technically, you can just write all of your code with the full names (e.g., `App.Truck` and `App.DataStore`), but your code is more readable when you have shorter names.

### Creating the Truck instance

Now, just as you did on the console, you will create an instance of <samp class="function">Truck</samp>, providing it an <samp class="varname">id</samp> and an instance of <samp class="function">DataStore</samp>.

Call the <samp class="function">Truck</samp> constructor in <samp class="filename">main.js</samp>, passing it an <samp class="varname">id</samp> of `ncc-1701` and a new instance of <samp class="function">DataStore</samp>.

```
(function (window) {
  'use strict';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var myTruck = new Truck('ncc-1701', new DataStore());
})(window);
```

This is nearly the same as the code you entered in the console earlier, but you do not need to prefix <samp class="function">Truck</samp> or <samp class="function">DataStore</samp> with `App`, because you created local variables that point to `App.Truck` and `App.DataStore`.

At this point, your application code is nearly complete. However, you still cannot interact with the instance of <samp class="function">Truck</samp>. Why not? The variable is declared inside of a function, the `main` module. Functions protect their variables from being accessed by code outside of the function, including code you write on the console.

So that you can interact with the instance of <samp class="function">Truck</samp>, export it to the global namespace in <samp class="filename">main.js</samp>.

```
(function (window) {
  'use strict';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var myTruck = new Truck('ncc-1701', new DataStore());
  window.myTruck = myTruck;
})(window);
```

Save your work and go back to the console. Reload the page manually to make sure that any prior work you did in the console has been cleared out.

Start typing `myTruck` and you should see that the console is trying to autocomplete it ([Figure 8.30](#ch08s08.html_fig-mytruck-autocomplete "Figure 8.30  The console finds myTruck in the global namespace")). That means that it found the `myTruck` variable that you exported as a property of the `window` object.

**Figure 8.30  The console finds `myTruck` in the global namespace**

![The console finds myTruck in the global namespace](CoffeeRun/Modules/img/mytruck-autocomplete.png)

Call <samp class="function">myTruck.createOrder</samp> a few times, providing it some test data. You can do this easily by letting the console autocomplete your previous calls to <samp class="function">createOrder</samp> ([Figure 8.31](#ch08s08.html_fig-previous-createorder "Figure 8.31  Console autocompleting previous calls to createOrder")).

**Figure 8.31  Console autocompleting previous calls to `createOrder`**

![Console autocompleting previous calls to createOrder](CoffeeRun/Modules/img/previous-createorder.png)

Alternatively, enter the following code to confirm that everything functions as expected.

```
myTruck.createOrder({ emailAddress: 'me@goldfinger.com', coffee: 'double mocha'});
myTruck.createOrder({ emailAddress: 'dr@no.com', coffee: 'decaf'});
myTruck.createOrder({ emailAddress: 'm@bond.com', coffee: 'earl grey'});
myTruck.printOrders();
myTruck.deliverOrder('dr@no.com');
myTruck.deliverOrder('m@bond.com');
myTruck.printOrders();
```

After exercising the methods <samp class="methodname">createOrder</samp>, <samp class="methodname">printOrders</samp>, and <samp class="methodname">deliverOrder</samp>, you should see something like [Figure 8.32](#ch08s08.html_fig-excelsior "Figure 8.32  One busy coffee truck").

**Figure 8.32  One busy coffee truck**

![One busy coffee truck](CoffeeRun/Modules/img/excelsior.png)

Congratulations! You have completed the foundation of CoffeeRun. It does not have a UI yet, but you will add that in upcoming chapters. And you will not need to make changes to the core, because the UI will simply call the `Truck.prototype` methods you have already written and tested.

This is the advantage of the modular approach: You can work on your application in layers, knowing that each new layer is built on working code in the underlying modules.

## Bronze Challenge: Truck ID for Non-Trekkies

In <samp class="filename">main.js</samp>, pass in a different string for the `truckId`.

(Some good options include “Serenity,” “KITT,” or “Galactica.” “HAL” is probably a bad idea.)

## For the More Curious: Private Module Data

Inside a module, your constructors and prototype methods have access to any variables declared inside the IIFE. As an alternative to adding properties to the `prototype`, this is a way to share data between instances but make it hidden from any code outside the module. It looks like this:

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var launchCount = 0;

  function Spaceship() {
    // Initialization code goes here
  }

  Spaceship.prototype.blastoff = function () {
    // Closure scope allows access to the launchCount variable
    launchCount++;
    console.log('Spaceship launched!')
  }

  Spaceship.prototype.reportLaunchCount = function () {
    console.log('Total number of launches: ' + launchCount);
  }

  App.Spaceship = Spaceship
  window.App = App;
})(window);
```

Other languages provide a way to declare a variable as <samp class="emphasis">private</samp>, but JavaScript does not. You can take advantage of closure scope (a function using variables declared in the outer scope) to simulate private variables.

## Silver Challenge: Making data Private

Update your <samp class="function">DataStore</samp> module so that the `data` property is private to the module.

Are there any reasons you would <samp class="emphasis">not</samp> want to do this? What happens if you declare multiple instances of <samp class="function">DataStore</samp>?

## For the More Curious: Setting this in forEach’s Callback

We told a small fib earlier. Using <samp class="methodname">bind</samp> is not the <samp class="emphasis">only</samp> way to set the value of <samp class="varname">this</samp> for the callback to <samp class="methodname">forEach</samp>.

Look at the documentation for <samp class="methodname">Array.prototype.forEach</samp> on MDN ([<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​JavaScript/​Reference/​Global_Objects/​Array/​forEach</samp>](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)). You can see that <samp class="methodname">forEach</samp> takes an optional second argument, which it will use as the value of <samp class="varname">this</samp> in the callback.

That means that you could have also written the <samp class="methodname">printOrders</samp> method like so:

```
...
Truck.prototype.printOrders = function () {
  var customerIdArray = Object.keys(this.db.getAll());

  console.log('Truck #' + this.truckId + ' has pending orders:');
  customerIdArray.forEach(function (id) {
    console.log(this.db.get(id));
  }, this);
};
...
```

<samp class="methodname">bind</samp>, however, is a useful method that you will see again in the coming chapters. <samp class="methodname">Truck.prototype.printOrders</samp> provided a good opportunity to introduce you to the syntax.

# <samp class="chapter_number">9</samp>
<samp class="chapter_name">Introduction to Bootstrap</samp>

In this chapter, you will create the HTML markup for your UI. You will use the styles provided by the popular <samp class="application">Bootstrap</samp> CSS framework to give your UI a bit of polish without having to create the CSS yourself. This way, you can focus on the application logic in JavaScript, which you will do in [Chapter 10](#ch10.html "10 Processing Forms with JavaScript").

You will be creating the UI for the CoffeeRun app in two parts. The first consists of a form into which a user can enter a coffee order with all of its details ([Figure 9.1](#ch09.html_fig-final-bootstrap "Figure 9.1  CoffeeRun styled with Bootstrap")). In the second part, the existing coffee orders will be displayed in a checklist. Each of these parts will have a corresponding JavaScript module to handle user interaction.

**Figure 9.1  CoffeeRun styled with Bootstrap**

![CoffeeRun styled with Bootstrap](CoffeeRun/Bootstrap/img/add-buttons.png)

## Adding Bootstrap

The <samp class="application">Bootstrap</samp> CSS library provides a collection of styles that you can use for your sites and applications. Because of its popularity, you may not want to use <samp class="application">Bootstrap</samp> for your user-facing production site without making some customizations. Otherwise, your site may end up looking like everyone else’s. However, <samp class="application">Bootstrap</samp> is great for quickly creating good-looking prototypes.

As you did with <samp class="application">normalize.css</samp> in Ottergram, you will get <samp class="application">Bootstrap</samp> by loading it from [<samp class="uri">cdnjs.com</samp>](http://cdnjs.com). Use version 3.3.6 of <samp class="application">Bootstrap</samp>, which is at [<samp class="uri">cdnjs.com/​libraries/​twitter-bootstrap/​3.3.6</samp>](https://cdnjs.com/libraries/twitter-bootstrap/3.3.6). (To find the most current version for your own projects, search [<samp class="uri">cdnjs.com</samp>](http://cdnjs.com) for “twitter bootstrap.”)

Make sure to get the link for <samp class="filename">bootstrap.min.css</samp> ([Figure 9.2](#ch09.html_fig-cdnjs-bootstrap "Figure 9.2  cdnjs.com page for twitter-bootstrap")), not one for the theme or fonts.

**Figure 9.2  `cdnjs.com` page for `twitter-bootstrap`**

![cdnjs.com page for twitter-bootstrap](CoffeeRun/Bootstrap/img/cdnjs.png)

After you have copied the link, open <samp class="filename">index.html</samp> and add a `<link>` tag with the URL. (Although we had to wrap the `href` attribute around to a second line to fit on this page, you should enter it on one line.)

```
...
  <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootst
rap/3.3.6/css/bootstrap.min.css">
  </head>
...
```

### How Bootstrap works

<samp class="application">Bootstrap</samp> can provide out-of-the-box responsive styling for your website or web app. Most of the time, you will just need to include the CSS file and then add classes to your markup. One of the main classes you will use is the `container` class.

Add the `container` class to your `<body>` element in <samp class="filename">index.html</samp>. While you are there, add a header to your page as well.

```
...
    <title>coffeerun</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootst
rap/3.3.6/css/bootstrap.min.css">
  </head>
  <body>
  <body class="container">
    <header>
      <h1>CoffeeRun</h1>
    </header>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

The `container` class acts as a wrapper for all the content that needs to adapt to the size of the viewport. This provides basic responsive behavior to the layout.

Save <samp class="filename">index.html</samp>, make sure `browser-sync` is running, and view your page. It should resemble [Figure 9.3](#ch09.html_fig-bootstrap-1 "Figure 9.3  Header styled with Bootstrap").

**Figure 9.3  Header styled with Bootstrap**

![Header styled with Bootstrap](CoffeeRun/Bootstrap/img/bootstrap-1.png)

Although there is not much to your page yet, notice that there is already a comfortable amount of padding around your header and that it has a font style applied to it.

<samp class="application">Bootstrap</samp> has styles for a huge number of different visual elements. CoffeeRun will just scratch the surface, but you will get a chance to explore more styles in a later chapter. For now, it is time to add the markup for the order form.

## Creating the Order Form

Add a `<section>` tag, two `<div>`s, and a `<form>` to <samp class="filename">index.html</samp>, below the `<header>` element you just created.

```
...
    <header>
      <h1>CoffeeRun</h1>
    </header>
    <section>
      <div class="panel panel-default">
        <div class="panel-body">
          <form data-coffee-order="form">
            <!-- Input elements will go here -->
          </form>
        </div>
      </div>
    </section>
    <script src="scripts/datastore.js" charset="utf-8"></script>
...
```

The `<form>` tag is going to be where all the important stuff happens. You gave it a `data-coffee-order` attribute with the value `form`. In CoffeeRun, you will use data attributes for accessing DOM elements from JavaScript, just as you did in Ottergram.

For layout, you added two `<div>` tags. It is not important that you use `<div>` tags, specifically. What is important is that you are applying the `panel`, `panel-default`, and `panel-body` classes to them. These are <samp class="application">Bootstrap</samp> classes that will trigger styles for you.

Remember, `<div>`s are just general-purpose block-level containers for other markup. They take up as much horizontal space as provided by their containing parent element. They will be used often in CoffeeRun, and you will see them throughout the examples in the <samp class="application">Bootstrap</samp> documentation.

You may be wondering why the `<section>` tag wraps around your `<div>` and `<form>` tags. `<div>`s have no semantic meaning. `<section>`s do: they logically group other markup. This one will house the UI for the form. You could easily have another `<section>` of the page that is for some other piece of the UI.

### Adding text input fields

The main piece of information that you care about is the coffee order itself. If you have been in a coffee shop in the last decade, you know how complicated orders can get. For now, you will use a single-line text field to represent an order. Later you will add more fields to capture more information about the order.

When you use <samp class="application">Bootstrap</samp> for your forms, you add extra `<div>` elements that are solely for applying styles defined in the <samp class="application">Bootstrap</samp> library.

Add another `<div>` to <samp class="filename">index.html</samp> with the class `form-group`. The `form-group` <samp class="application">Bootstrap</samp> class provides consistent vertical spacing for form elements. Then add `<label>` and `<input>` elements.

```
...
      <div class="panel panel-default">
        <div class="panel-body">
          <form data-coffee-order="form">
            <!-- Input elements will go here -->
            <div class="form-group">
              <label>Coffee Order</label>
              <input class="form-control" name="coffee">
            </div>
          </form>
        </div>
      </div>
...
```

The `form-control` class is another one defined by <samp class="application">Bootstrap</samp>. It provides layout and typography styling for your form elements.

Save <samp class="filename">index.html</samp> and check the results in the browser ([Figure 9.4](#ch09s02.html_fig-input-field "Figure 9.4  Input field for a coffee order")).

**Figure 9.4  Input field for a coffee order**

![Input field for a coffee order](CoffeeRun/Bootstrap/img/add-textfield.png)

Your `<input>` element defaults to a single-line text field. Other than its `form-control` class, it has one attribute: `name`. When a form is submitted, the data will be sent to a server, and the `name` attribute will be sent with that data. If you think about form data as a key/value pair, then the `name` attribute is the key and the data that the user types in the field is the value.

#### Linking a label and a form element

`<label>` tags are important usability enhancements for your form elements. You tell a `<label>` what form element it is labeling by setting its `for` attribute to match the `id` attribute of the form element.

In <samp class="filename">index.html</samp>, add `for` and `id` attributes to your `<label>` and `<input>` form elements, respectively. Give both attributes the same `coffeeOrder` value.

```
...
      <div class="panel panel-default">
        <div class="panel-body">
          <form data-coffee-order="form">
            <div class="form-group">
              <label for="coffeeOrder">Coffee Order</label>
              <input class="form-control" name="coffee" id="coffeeOrder">
            </div>
          </form>
        </div>
      </div>
...
```

When a `<label>` is linked to a form element, you can click the `<label>`’s text on the page and it will make the linked form element active. You should always link your `<label>`s to their form elements.

To see this in action, save <samp class="filename">index.html</samp>, switch to the browser, and click the <samp class="guilabel">Coffee Order</samp> label text. The `<input>` should gain focus, ready for you to start typing ([Figure 9.5](#ch09s02.html_fig-click-label-to-focus "Figure 9.5  Clicking the linked label causes the input to gain focus")).

**Figure 9.5  Clicking the linked label causes the input to gain focus**

![Clicking the linked label causes the input to gain focus](CoffeeRun/Bootstrap/img/click-label-to-focus.png)

#### Adding autofocus

Because this is the first field on the screen, you want the user to be able to enter text in it as soon as the page loads, instead of having to click.

To achieve this, add an `autofocus` attribute to the `<input>` in <samp class="filename">index.html</samp>.

```
...
            <div class="form-group">
              <label for="coffeeOrder">Coffee Order</label>
              <input class="form-control" name="coffee" id="coffeeOrder" autofocus>
            </div>
...
```

Save your changes to <samp class="filename">index.html</samp> and return to the browser. You will see that the text input field has a cursor and a highlight as soon as the page loads ([Figure 9.6](#ch09s02.html_fig-autofocus-on-page-load "Figure 9.6  Input field with autofocus on page load")).

**Figure 9.6  Input field with autofocus on page load**

![Input field with autofocus on page load](CoffeeRun/Bootstrap/img/autofocus-on-page-load.png)

Notice that the `autofocus` attribute does not have a value. It does not need one. The mere presence of the `autofocus` attribute in an `<input>` tag tells the browser to activate that field. The `autofocus` attribute is a <samp class="firstterm">Boolean</samp> attribute, which means that its only possible values are `true` and `false`. You only need to add the attribute name to the tag in order to set its value. When it is present, it has the value `true`. When it is not present, the attribute is considered `false`.

#### Adding an email input field

When you created your `Truck` and `DataStore` modules, you tracked orders by the customer’s email address. Now you will capture that information using another `<input>` element.

Add another `.form-group` element to <samp class="filename">index.html</samp> with a `<label>` and an `<input>`. For the `<input>` element, set the `type` as `email`, the `name` to `emailAddress`, and the `id` to `emailInput`. Also, add a `value` attribute, set to an empty string. This ensures that this field is blank when the page loads. Finally, link the `<input>` and the `<label>` using the `id`.

```
...
          <form data-coffee-order="form">
            <div class="form-group">
              <label for="coffeeOrder">Coffee Order</label>
              <input class="form-control" name="coffee" id="coffeeOrder" autofocus>
            </div>
            <div class="form-group">
              <label for="emailInput">Email</label>
              <input class="form-control" type="email" name="emailAddress"
                id="emailInput" value="">
            </div>
          </form>
...
```

Save <samp class="filename">index.html</samp> and check the browser to see your new form field ([Figure 9.7](#ch09s02.html_fig-email-field "Figure 9.7  Input field for an email address")).

**Figure 9.7  Input field for an email address**

![Input field for an email address](CoffeeRun/Bootstrap/img/add-emailfield.png)

##### Showing example input with placeholder text

Sometimes users appreciate a suggestion about what they should enter into a text field. To create example text, use the `placeholder` attribute.

Add a `placeholder` attribute to your new `<input>` element in <samp class="filename">index.html</samp>.

```
...
            <div class="form-group">
              <label for="emailInput">Email</label>
              <input class="form-control" type="email" name="emailAddress"
                id="emailInput" value="" placeholder="dr@who.com">
            </div>
...
```

Save your file. The result will look like [Figure 9.8](#ch09s02.html_fig-email-dr-who "Figure 9.8  Placeholder text in the email input").

**Figure 9.8  Placeholder text in the email input**

![Placeholder text in the email input](CoffeeRun/Bootstrap/img/add-placeholder.png)

The value of the `placeholder` attribute appears in the text field until the user enters some text, at which point it disappears. If the user deletes all of the text in the field, the placeholder text appears again.

### Offering choices with radio buttons

Next, you want the user to be able to specify the size of their coffee drink. They should be able to choose between short, tall, and grande – and they should not be able to choose more than one size. For this kind of data input, you can use `<input>` fields whose `type` attribute is set to `radio`.

The markup for your radio buttons will be different from your other `<input>` fields. Each radio button will have an `<input>` field, <samp class="emphasis">wrapped</samp> by a `<label>` element. The `<label>` will be wrapped in a `<div>` whose `class` is <samp class="emphasis">also</samp> `radio`.

The `<label>` elements will not need the `for` attribute that you added to the `<label>`s for the coffee order and email. Because the `<input>` is wrapped with the `<label>`, they are automatically linked.

In case you are wondering why the HTML is different for radio buttons, it is because <samp class="application">Bootstrap</samp> styles them differently from the other form elements.

When writing your own code, you can choose to wrap an `<input>` element in a `<label>` or to use the `for` attribute – both are correct. But, when you use <samp class="application">Bootstrap</samp>, you must follow its patterns and conventions for the styles to work as expected. Refer to the <samp class="application">Bootstrap</samp> documentation for examples of how to structure your HTML ([<samp class="uri">getbootstrap.com/​css/​#forms</samp>](http://getbootstrap.com/css/#forms)).

In <samp class="filename">index.html</samp>, add the markup for your radio buttons just after the email `<input>`.

```
...
              <div class="form-group">
                <label for="emailInput">Email</label>
                <input class="form-control" type="email" name="emailAddress"
                  id="emailInput" value="" placeholder="dr@who.com">
              </div>
              <div class="radio">
                <label>
                  <input type="radio" name="size" value="short">
                  Short
                </label>
              </div>
              <div class="radio">
                <label>
                  <input type="radio" name="size" value="tall" checked>
                  Tall
                </label>
              </div>
              <div class="radio">
                <label>
                  <input type="radio" name="size" value="grande">
                  Grande
                </label>
              </div>
            </form>
...
```

You gave all three of your radio inputs the same value for the `name` attribute (`size`). This tells the browser that only one of them can be selected (or “checked”) at a time. You gave the <samp class="guilabel">Tall</samp> radio button a Boolean attribute named `checked`. This works the same way that `autofocus` does: When it is present, the value of the attribute is `true` and when it is absent it is `false`.

Save <samp class="filename">index.html</samp> and take a look at your new radio buttons ([Figure 9.9](#ch09s02.html_fig-add-radio "Figure 9.9  Radio buttons for coffee sizes")).

**Figure 9.9  Radio buttons for coffee sizes**

![Radio buttons for coffee sizes](CoffeeRun/Bootstrap/img/add-radio.png)

Try clicking either a radio button or the text next to it. Either way, that radio button should indicate that it was selected.

### Adding a dropdown menu

Some folks are crazy for flavored coffee. You want to give them the option to choose from a few different flavors. By default, no flavor shot will be added.

You could use a set of radio buttons for this, but you might add many more flavors to the list. To make sure that the flavor choices do not clutter up the UI, you will use a dropdown menu.

To create a dropdown menu styled with <samp class="application">Bootstrap</samp>, add a `<div>` to <samp class="filename">index.html</samp> with the `class` `form-group`. Create a `<select>` element with the `class` `form-control`. <samp class="application">Bootstrap</samp> will style this element as a dropdown. Link it to its `<label>` with the `id` `flavorShot`. Inside of the `<select>`, add an `<option>` element for each of the menu items you want to display, giving each of them a matching `value`.

```
...
            <div class="radio">
              <label>
                <input type="radio" name="size" value="grande">
                Grande
              </label>
            </div>
            <div class="form-group">
              <label for="flavorShot">Flavor Shot</label>
              <select id="flavorShot" class="form-control" name="flavor">
                <option value="">None</option>
                <option value="caramel">Caramel</option>
                <option value="almond">Almond</option>
                <option value="mocha">Mocha</option>
              </select>
            </div>
          </form>
        </div>
      </div>
...
```

Each of the `<option>` elements provides one of the possible `value`s, while the `<select>` element specifies the `name`.

Save <samp class="filename">index.html</samp> and check that your dropdown is displayed with all of the `options` you added ([Figure 9.10](#ch09s02.html_fig-add-dropdown "Figure 9.10  Coffee flavor dropdown")).

**Figure 9.10  Coffee flavor dropdown**

![Coffee flavor dropdown](CoffeeRun/Bootstrap/img/add-dropdown.png)

By default, the first `<option>` element is selected. You can also add the `selected` Boolean attribute to an `option` element, if you want one other than the first to be selected automatically.

You set the `value` attribute to an empty string for the first dropdown item. If you left off the `value` attribute completely, the browser would have used the string `"None"` as the value. It is best to set the `value` attribute, as you should never assume that browsers will do what you expect.

### Adding a range slider

Not everyone wants a killer coffee buzz. You want to let users choose a value between 0 and 100 for the strength of their coffee. On the other hand, you do not want them to have to type in an exact value.

For this, add an `<input>` element in <samp class="filename">index.html</samp> whose `type` is `range`. This creates a <samp class="firstterm">range slider</samp>. The `<input>` and `<label>` should be linked and wrapped in a `<div>` with the `form-group` class. Go easy on your coffee customers and provide a default `value` of `30`.

```
...
                <option value="mocha">Mocha</option>
              </select>
            </div>
            <div class="form-group">
              <label for="strengthLevel">Caffeine Rating</label>
              <input name="strength" id="strengthLevel" type="range" value="30">
            </div>
          </form>
...
```

Save <samp class="filename">index.html</samp> and try out your new slider in the browser. It will look like [Figure 9.11](#ch09s02.html_fig-add-slider "Figure 9.11  Slider for caffeine strength").

**Figure 9.11  Slider for caffeine strength**

![Slider for caffeine strength](CoffeeRun/Bootstrap/img/add-slider.png)

### Adding Submit and Reset buttons

The last thing to do in the markup is to add a <samp class="guibutton">Submit</samp> button. As a usability convenience, you should also add a <samp class="guibutton">Reset</samp> button to clear the form, in case the user wants to start over.

Normally, <samp class="guibutton">Submit</samp> buttons are just an `<input>` element whose type is `submit`. Likewise, <samp class="guibutton">Reset</samp> buttons are `<input>` elements whose type is `reset`. However, to take advantage of <samp class="application">Bootstrap</samp>’s CSS, you will use a `<button>` element instead.

In <samp class="filename">index.html</samp>, add two `<button>` elements with the class names `btn btn-default`. Set the `type` of the first one to `submit`, and set the `type` of the second one to `reset`. In between the opening and closing tags, put `Submit` and `Reset` as descriptive text.

```
...
            <div class="form-group">
              <label for="strengthLevel">Caffeine Rating</label>
              <input name="strength" id="strengthLevel" type="range" value="30">
            </div>
            <button type="submit" class="btn btn-default">Submit</button>
            <button type="reset" class="btn btn-default">Reset</button>
          </form>
...
```

When you save your changes, your browser will add the buttons at the bottom of the form ([Figure 9.12](#ch09s02.html_fig-add-buttons "Figure 9.12  Submit and Reset buttons")).

**Figure 9.12  Submit and Reset buttons**

![Submit and Reset buttons](CoffeeRun/Bootstrap/img/add-buttons.png)

Your <samp class="guibutton">Submit</samp> button will not do anything yet. That is coming in the next chapter. However, your <samp class="guibutton">Reset</samp> button will reset the values to their defaults.

These buttons have a pair of classes that might seem redundant. This is a convention of <samp class="application">Bootstrap</samp> and is purely for styling. The `btn` class provides all of the standard visual properties of a <samp class="application">Bootstrap</samp> button. This includes rounded corners and padding. The `btn-default` class adds a white background color.

You have used the <samp class="application">Bootstrap</samp> UI framework to style your CoffeeRun app. By applying <samp class="application">Bootstrap</samp>’s pattern of markup and class names, your app will have a consistent look and feel for a variety of screen sizes and browser versions.

To learn more about what <samp class="application">Bootstrap</samp> has to offer, look through the excellent documentation at [<samp class="uri">getbootstrap.com/​css</samp>](http://getbootstrap.com/css/).

<samp class="application">Bootstrap</samp> is particularly good for quickly styling an app while you focus on the application logic. In the next chapters, you will do just that.

# <samp class="chapter_number">10</samp>
<samp class="chapter_name">Processing Forms with JavaScript</samp>

CoffeeRun is off to a good start. It has two JavaScript modules that handle its internal logic and an HTML form styled with <samp class="application">Bootstrap</samp>. In this chapter, you will write a more complex module that connects the form to the logic, allowing you to use the form to enter coffee orders.

Recall from [Chapter 2](#ch02.html "2 Setting Up Your First Project") that browsers communicate with servers by sending requests for information for a particular URL. Specifically, for every file that the browser needs to load, it sends a `GET` request to the server for that file.

When the browser needs to send information <samp class="emphasis">to</samp> a server, such as when a user fills out and submits a form, the browser takes the form data and puts it in a `POST` request. The server receives the request, processes the data, and then sends back a response ([Figure 10.1](#ch10.html_fig-post-request-response "Figure 10.1  Traditional server-side form processing")).

**Figure 10.1  Traditional server-side form processing**

![Traditional server-side form processing](CoffeeRun/Forms/img/post-request-response.png)

In CoffeeRun, you will not need to send the form data to a server for processing. Your <samp class="function">Truck</samp> and <samp class="function">DataStore</samp> modules serve the same purpose as traditional server-side code. Their job is to handle the business logic and data storage for your application.

Because this code lives in the browser and not on a server, you need to capture the data from the form before it goes out. In this chapter you will create a new module called <samp class="function">FormHandler</samp> to do just that. In addition, you will add the jQuery library to CoffeeRun to help you with your work. As you build out CoffeeRun over the next few chapters, you will use more of jQuery’s powerful features.

## Creating the FormHandler Module

The <samp class="function">FormHandler</samp> module will prevent the browser from trying to send form data to a server. Instead, it will read the values from the form when the user clicks the <samp class="guibutton">Submit</samp> button. Then it will send that data to a <samp class="function">Truck</samp> instance, using the <samp class="methodname">createOrder</samp> method you wrote in [Chapter 8](#ch08.html "8 Modules, Objects, and Methods") ([Figure 10.2](#ch10.html_fig-formhandler-diagram-1 "Figure 10.2  Application architecture of CoffeeRun with App.FormHandler")).

**Figure 10.2  Application architecture of CoffeeRun with `App.FormHandler`**

![Application architecture of CoffeeRun with App.FormHandler](CoffeeRun/Forms/img/formhandler-diagram-1.png)

Create a new file called <samp class="filename">formhandler.js</samp> in your <samp class="filename">scripts</samp> folder and add a `<script>` tag for it in <samp class="filename">index.html</samp>.

```
...
          </form>
        </div>
      </div>
    </section>
    <script src="scripts/formhandler.js" charset="utf-8"></script>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

Like your other modules, <samp class="function">FormHandler</samp> will use an IIFE to encapsulate the code and attach a constructor to the `window.App` property.

Open <samp class="filename">scripts/formhandler.js</samp> and create an IIFE. Inside the IIFE, create an `App` variable. Assign it the existing value of `window.App`. If `window.App` does not exist yet, assign it an empty object literal. Declare a <samp class="function">FormHandler</samp> constructor function, and export it to the `window.App` property.

```
(function (window) {
  'use strict';
  var App = window.App || {};

  function FormHandler() {
    // Code will go here
  }

  App.FormHandler = FormHandler;
  window.App = App;

})(window);
```

So far, this code follows the familiar pattern you used in your <samp class="function">Truck</samp> and <samp class="function">DataStore</samp> modules. It will be different soon, though, in that it will import and use jQuery to do its work.

### Introduction to jQuery

The jQuery library was created by John Resig in 2006\. It is one of the most popular general-purpose open-source JavaScript libraries. Among other things, it provides convenient shorthands for DOM manipulation, element creation, server communication, and event handling.

It is useful to be familiar with jQuery, because there is so much code that has been written using it. Also, many libraries have copied jQuery’s conventions. In fact, jQuery has directly influenced the standard DOM API (`document.querySelector` and `document.querySelectorAll` are two examples of this influence).

jQuery will not be covered in depth right now. Instead, aspects of it will be introduced as needed to help you build more complex parts of CoffeeRun. Should you want to explore jQuery further, check out the documentation at [<samp class="uri">jquery.com</samp>](http://jquery.com).

As you did with <samp class="application">Bootstrap</samp>, you will add a copy of jQuery to your project from [<samp class="uri">cdnjs.com</samp>](http://cdnjs.com). Go to [<samp class="uri">cdnjs.com/​libraries/​jquery</samp>](https://cdnjs.com/libraries/jquery/) to find version 2.1.4 and copy its address. (There may be a more recent version available, but you should use 2.1.4 for CoffeeRun to avoid any compatibility issues.)

Add jQuery in a `<script>` tag in <samp class="filename">index.html</samp>.

```
...
      </div>
    </section>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.4/jquery.min.js"
      charset="utf-8"></script>
    <script src="scripts/formhandler.js" charset="utf-8"></script>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
...
```

Save <samp class="filename">index.html</samp>.

### Importing jQuery

<samp class="function">FormHandler</samp> will import jQuery the same way that it is importing `App`. The reason for doing this is to make it explicit that your module is using code that is defined elsewhere. This is a best practice for coordinating with team members and for future maintenance.

In <samp class="filename">formhandler.js</samp>, create a local variable named <samp class="varname">$</samp> and then assign it the value `window.jQuery`.

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var $ = window.jQuery;

  function FormHandler() {
    // Code will go here
  }

  App.FormHandler = FormHandler;
  window.App = App;

})(window);
```

When you added the jQuery `<script>` tag, it created a function named <samp class="function">jQuery</samp> as well as a variable, named <samp class="varname">$</samp>, pointing to the function. Most developers prefer to use <samp class="varname">$</samp> in their code. In keeping with that practice, you are importing `window.jQuery` and assigning it to the local variable <samp class="varname">$</samp>.

Wondering why <samp class="varname">$</samp> is used for the variable name? JavaScript variable names can contain letters, numbers, the underscore (_), or the dollar sign ($). (They can only <samp class="emphasis">start</samp> with letters, underscores, or dollar signs, though – not numbers.) The creator of jQuery chose the <samp class="varname">$</samp> variable name because it is short and unlikely to be used by any other code in a project.

### Configuring instances of FormHandler with a selector

Your <samp class="function">FormHandler</samp> module should be usable with any `<form>` element. To achieve this, the <samp class="function">FormHandler</samp> constructor will be passed a selector matching the `<form>` element in <samp class="filename">index.html</samp>.

Update <samp class="filename">formhandler.js</samp> to add a parameter called `selector` to the <samp class="function">FormHandler</samp> constructor. Throw an <samp class="function">Error</samp> if it is not passed in.

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var $ = window.jQuery;

  function FormHandler(selector) {
    // Code will go here
    if (!selector) {
      throw new Error('No selector provided');
    }
  }

  App.FormHandler = FormHandler;
  window.App = App;

})(window);
```

<samp class="function">Error</samp> is a built-in type that lets you formally signal that there is an unexpected value or condition in your code. For now, your <samp class="function">Error</samp> instance will simply print out your message on the console.

Save and try instantiating a new <samp class="function">FormHandler</samp> object without passing it an argument ([Figure 10.3](#ch10.html_fig-custom-error "Figure 10.3  Instantiating a FormHandler object without passing arguments")). (Remember to start `browser-sync`, if it is not already running.)

**Figure 10.3  Instantiating a `FormHandler` object without passing arguments**

![Instantiating a FormHandler object without passing arguments](CoffeeRun/Forms/img/custom-error.png)

This is the first step in making <samp class="function">FormHandler</samp> more reusable. In Ottergram, you created variables for the selectors you used in your DOM code. You will not be doing that with the <samp class="function">FormHandler</samp> module. Instead, you will use the selector that was passed in to the constructor and use jQuery to find the matching elements.

jQuery is most often used for finding elements in the DOM. To do that, you call the jQuery <samp class="function">$</samp> function and pass it a selector as a string. In fact, you use it the same way you have been using <samp class="methodname">document.querySelectorAll</samp> (although jQuery works differently under the hood, as we will explain in a moment). It is common to refer to this as “selecting elements from the DOM” with jQuery.

Declare an instance variable named <samp class="varname">$formElement</samp> in <samp class="filename">formhandler.js</samp>. Then find a matching element in the DOM using that selector and assign the result to <samp class="varname">this.$formElement</samp>.

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var $ = window.jQuery;

  function FormHandler(selector) {
    if (!selector) {
      throw new Error('No selector provided');
    }

    this.$formElement = $(selector);
  }

  App.FormHandler = FormHandler;
  window.App = App;

})(window);
```

Prefixing a variable with `$` is a sign that the variable refers to elements selected using jQuery. This prefix is not a requirement when using jQuery, but it is a common convention used by many front-end developers.

When you use jQuery’s <samp class="function">$</samp> function to select elements, it does not return references to DOM elements, the way that <samp class="methodname">document.querySelectorAll</samp> does. Instead, it returns a single object, and the <samp class="emphasis">object</samp> contains references to the selected elements. The object also has special methods for manipulating the collection of references. This object is called a “jQuery-wrapped selection” or “jQuery-wrapped collection.”

Next, you want to make sure that the selection successfully retrieved an element from the DOM. jQuery will return an empty selection if it does not find anything – it will not throw an error if the selector does not match anything. You will need to check manually, because <samp class="function">FormHandler</samp> cannot do its work without an element.

The `length` property of a jQuery-wrapped selection tells you how many elements were matched. Update <samp class="filename">formhandler.js</samp> to check the `length` property of <samp class="varname">this.$formElement</samp>. If it is `0`, throw an `Error`.

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var $ = window.jQuery;

  function FormHandler(selector) {
    if (!selector) {
      throw new Error('No selector provided');
    }

    this.$formElement = $(selector);
    if (this.$formElement.length === 0) {
      throw new Error('Could not find element with selector: ' + selector);
    }
  }

  App.FormHandler = FormHandler;
  window.App = App;

})(window);
```

Your <samp class="function">FormHandler</samp> constructor can be configured to work with any `<form>` element based on the selector passed in. Also, it keeps a reference to that `<form>` element as an instance variable. This ensures that your code will not make make unnecessary trips to the DOM. This is a performance best practice. (The alternative is to call <samp class="function">$</samp> over and over, which re-selects the same elements each time.)

## Adding the submit Handler

The next step is for <samp class="function">FormHandler</samp> to listen for the `submit` event on the `<form>` element and run a callback when it occurs.

To make the <samp class="function">FormHandler</samp> module more reusable, you will not hardcode the `submit` handler code. You will instead write a method that accepts a function argument, adds the `submit` listener, and then calls the function argument inside that listener.

First, add a prototype method called <samp class="methodname">addSubmitHandler</samp> to <samp class="filename">formhandler.js</samp>.

```
...
    if (this.$formElement.length === 0) {
      throw new Error('Could not find element with selector: ' + selector);
    }
  }

  FormHandler.prototype.addSubmitHandler = function () {
    console.log('Setting submit handler for form');
    // More code will go here
  };

  App.FormHandler = FormHandler;
...
```

Instead of using the <samp class="methodname">addEventListener</samp> method as you did with Ottergram, you will use jQuery’s <samp class="methodname">on</samp> method. It is similar to <samp class="methodname">addEventListener</samp> but provides added conveniences. For now, though, you will use it the same way you would use <samp class="methodname">addEventListener</samp>. (You will take advantage of some of the extra conveniences in the next chapter.)

```
...
    if (this.$formElement.length === 0) {
      throw new Error('Could not find element with selector: ' + selector);
    }
  }

  FormHandler.prototype.addSubmitHandler = function () {
    console.log('Setting submit handler for form');
    // More code will go here
    this.$formElement.on('submit', function (event) {
      event.preventDefault();
    });
  };
...
```

The <samp class="methodname">on</samp> method accepts the name of the event and a callback to run when the event is triggered. Its callback should expect to receive the event object. You called <samp class="methodname">event.preventDefault</samp> to ensure that submitting the form does not take the user away from the CoffeeRun page. (You did the same thing with the thumbnail links in Ottergram.)

### Extracting the data

When the form is submitted, your code should read the user input from the form, then <samp class="emphasis">do</samp> something with that data. In the `submit` handler in <samp class="filename">formhandler.js</samp>, create a new variable named `data`. Assign it an object literal. It will hold the `value` of each element of the form.

```
...
  FormHandler.prototype.addSubmitHandler = function () {
    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();

      var data = $(this).serializeArray();
      console.log(data);

    });
  };
...
```

Inside your `submit` handler callback, the <samp class="varname">this</samp> object is a reference to the `form` element. jQuery provides a convenience method (<samp class="methodname">serializeArray</samp>) for getting the values from the form. In order to use <samp class="methodname">serializeArray</samp>, you need to “wrap” the form using jQuery. Calling `$(this)` gives you a wrapped object, which has access to the <samp class="function">serializeArray</samp> method.

<samp class="function">serializeArray</samp> returns the form data as an array of objects. You are assigning that to a temporary variable named <samp class="varname">data</samp> and logging it to the console. To get an idea of what <samp class="function">serializeArray</samp> looks like, save your file and run the following code in the console:

```
var fh = new App.FormHandler('[data-coffee-order="form"]');
fh.addSubmitHandler();
```

Next, fill out the form with some test data and click the <samp class="guibutton">Submit</samp> button. You should see the array printed to the console. Click the ![Extracting the data](CoffeeRun/Forms/img/arrow.png) next to a couple of the `Object` items in the array. You should see something like [Figure 10.4](#ch10s02.html_fig-console-log-serialize-array "Figure 10.4  serializeArray returns form data as an array of objects").

**Figure 10.4  `serializeArray` returns form data as an array of objects**

![serializeArray returns form data as an array of objects](CoffeeRun/Forms/img/console-log-serialize-array.png)

You can see that each object in the array has a key that corresponds to the `name` attribute of a `<form>` element and the user-supplied `value` for that element.

Now you can iterate through the array and copy the values from each element. Add a call to the <samp class="methodname">forEach</samp> method to <samp class="function">serializeArray</samp> in <samp class="filename">formhandler.js</samp> and pass it a callback. As the callback is run for each object in the array, it will use the object’s <samp class="varname">name</samp> and <samp class="varname">value</samp> to create a new property on the <samp class="varname">data</samp> object.

```
...
  FormHandler.prototype.addSubmitHandler = function () {
    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();

      var data = $(this).serializeArray(); {};
      $(this).serializeArray().forEach(function (item) {
        data[item.name] = item.value;
        console.log(item.name + ' is ' + item.value);
      });
      console.log(data);

    });
  };
...
```

To see this in action, save your changes and run your test code again in the console before filling out the form:

```
var fh = new App.FormHandler('[data-coffee-order="form"]');
fh.addSubmitHandler();
```

When you fill out the form and click the <samp class="guibutton">Submit</samp> button, you should see that the information you entered is copied to the <samp class="varname">data</samp> object and logged to the console ([Figure 10.5](#ch10s02.html_fig-caff-fiend "Figure 10.5  Form data is copied in the iterator callback")).

**Figure 10.5  Form data is copied in the iterator callback**

![Form data is copied in the iterator callback](CoffeeRun/Forms/img/caff-fiend.png)

### Accepting and calling a callback

Now that you have the form data as a single object, you need to pass that object to your <samp class="function">Truck</samp> instance’s <samp class="methodname">createOrder</samp> method. But <samp class="function">FormHandler</samp> has no access to the <samp class="function">Truck</samp> instance. (And it would do no good to create a new <samp class="function">Truck</samp> instance here.)

You can solve this by making <samp class="methodname">addSubmitHandler</samp> accept a function parameter, which it can call inside the event handler.

In <samp class="filename">formhandler.js</samp>, add a parameter called `fn`.

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();
...
```

The `submit` handler callback will be called any time the form’s `submit` event is triggered in the browser. When that happens, you want the `fn` function to be called.

Call `fn` inside the `submit` handler callback in <samp class="filename">formhandler.js</samp> and pass it the `data` object that contains the user input.

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    ...
      console.log(data);
      fn(data);
    });
  };
...
```

Now, when a <samp class="function">FormHandler</samp> instance is created, any callback can be passed to <samp class="function">addSubmitHandler</samp>. From then on, when the form is submitted, the callback will be invoked and will be passed whatever data the user entered into the form.

## Using FormHandler

In `main.js`, you need to instantiate a <samp class="function">FormHandler</samp> instance and pass it the selector for the `<form>` element: `[data-coffee-order="form"]`. Create a variable at the top of `main.js` for this selector so that it can be reused if needed.

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var App = window.App;
...
```

Next, create a local variable called <samp class="function">FormHandler</samp> and assign it to `App.FormHandler`.

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var FormHandler = App.FormHandler;
  var myTruck = new Truck('ncc-1701', new DataStore());
  ...
```

At the end of the `main.js` module, call the <samp class="function">FormHandler</samp> constructor and pass it the `FORM_SELECTOR` variable. This will make sure that the instance of <samp class="function">FormHandler</samp> will work with the DOM element matching that selector. Assign the instance to a new variable called <samp class="function">FormHandler</samp>.

```
...
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var FormHandler = App.FormHandler;
  var myTruck = new Truck('ncc-1701', new DataStore());
  window.myTruck = myTruck;
  var formHandler = new FormHandler(FORM_SELECTOR);

  formHandler.addSubmitHandler();
  console.log(formHandler);
})(window);
```

When you save your code and return to the browser, the console should report `Setting submit handler for form`, showing that <samp class="methodname">addSubmitHandler</samp> was called when the page loaded. However, if you fill out and submit the form, you will get an error ([Figure 10.6](#ch10s03.html_fig-esprso "Figure 10.6  Calling addSubmitHandler on page load")).

**Figure 10.6  Calling `addSubmitHandler` on page load**

![Calling addSubmitHandler on page load](CoffeeRun/Forms/img/esprso.png)

This is because you did not pass anything to <samp class="methodname">addSubmitHandler</samp>. You will correct that in the next section.

### Registering createOrder as a submit handler

You want <samp class="function">createOrder</samp> to be called each time a `submit` event occurs. But you cannot just pass a reference to <samp class="function">createOrder</samp> to <samp class="methodname">formHandler.addSubmitHandler</samp>. This is because `createOrder`’s <samp class="emphasis">owner</samp> changes when it is invoked inside of the event handling callback. With a different owner, the value of `this` inside the body of `createOrder` will not be the <samp class="classname">Truck</samp> instance, thus causing an error when `createOrder` runs.

Instead, you will pass a <samp class="firstterm">bound reference</samp> to <samp class="methodname">myTruck.createOrder</samp> to <samp class="methodname">formHandler.addSubmitHandler</samp>.

Update <samp class="filename">formhandler.js</samp> with this change. Make sure to <samp class="function">bind</samp> the method reference so that its owner is guaranteed to be `myTruck`.

```
...
  window.myTruck = myTruck;
  var formHandler = new FormHandler(FORM_SELECTOR);

  formHandler.addSubmitHandler(myTruck.createOrder.bind(myTruck));
  console.log(formHandler);
})(window);
```

Could you have added <samp class="function">bind</samp> to the definition of the original prototype method? When defining prototype methods, you have access to the instance, but only <samp class="emphasis">inside</samp> the method body. <samp class="function">bind</samp> requires you to have a reference to the intended owner of the invocation – a reference that must be available outside of the method body. As you have no way of referencing the instance from outside the method body, you cannot <samp class="function">bind</samp> the original prototype method.

Save and fill out your form. After you submit, you should be able to call `myTruck.printOrders` and see that the data you entered into the form has been added to the list of pending orders, as shown in [Figure 10.7](#ch10s03.html_fig-ambrosia "Figure 10.7  createOrder is called when the form is submitted").

**Figure 10.7  `createOrder` is called when the form is submitted**

![createOrder is called when the form is submitted](CoffeeRun/Forms/img/ambrosia.png)

## UI Enhancements

It would be nice if the form were cleared of its old data after it was submitted, so that the user could immediately start entering the next order. Resetting the form is as simple as calling the `<form>` element’s <samp class="methodname">reset</samp> method.

Find the `FormHandler.prototype.addSubmitHandler` method in <samp class="filename">formhandler.js</samp>. At the end of the `this.$formElement.on('submit'...)` callback, add a call to the form’s <samp class="methodname">reset</samp> method:

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();

      var data = {};
      $(this).serializeArray().forEach(function (item) {
        data[item.name] = item.value;
        console.log(item.name + ' is ' + item.value);
      });
      console.log(data);
      fn(data);
      this.reset();
    });
  };
...
```

Save and enter some data into the form. When you submit the form, you should see that the data is cleared out.

Finally, add one last tweak to the UI. When a form field is ready for input, it has focus, as you saw in the last chapter. To set the focus on a specific form field, you can call its <samp class="methodname">focus</samp> method. (The `autofocus` attribute you added to the coffee order field only takes effect when the page first loads.)

You can conveniently access the individual form fields via the form’s `elements` property. The `elements` property is an array of the form’s fields, which you can refer to by their indices, starting with 0.

In <samp class="filename">formhandler.js</samp>, right after the call to <samp class="methodname">this.reset</samp> in the `submit` handler callback, invoke the <samp class="methodname">focus</samp> method on the first field.

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();

      var data = {};
      $(this).serializeArray().forEach(function (item) {
        data[item.name] = item.value;
        console.log(item.name + ' is ' + item.value);
      });
      console.log(data);
      fn(data);
      this.reset();
      this.elements[0].focus();
    });
  };
...
```

CoffeeRun is now jQuery-powered and can accept user input! You have bridged the gap between your HTML and your JavaScript modules. In the next chapter, you will complete the picture by creating interactive DOM elements based on the data captured from the form.

## Bronze Challenge: Supersize It

Add another size option for coffee orders – one with an inspiringly large-sounding name, such as “Coffee-zilla.”

Add a new order using this extra-large size and check your application data in the console to make sure it is being saved correctly.

## Silver Challenge: Showing the Value as the Slider Changes

Create a handler for the slider’s `change` event. As the value of the slider changes, show the number next to the label for the slider.

As an extra challenge, change the color of the number (or the label) to reflect the intensity of the caffeine strength. Use green for weaker coffee, yellow for regular strength coffee, and red for very strong coffee.

## Gold Challenge: Adding Achievements

When users submit an order for the largest, strongest coffee with a flavor shot, unlock an achievement: Bring up a <samp class="application">Bootstrap</samp> modal to inform them of their amazing intensity and commitment to flavor. Ask them if they would like to use their achievement, and, if so, add an additional form field that is only visible when their email address is entered in the `email` field. It should let them choose one or more power-up options for their coffee, like time travel, mind reading, or bug-free code.

Refer to the documentation at [<samp class="uri">getbootstrap.com/​javascript</samp>](http://getbootstrap.com/javascript/) for information on how to include and trigger <samp class="application">Bootstrap</samp>’s modal behaviors. (You will need to add a `<script>` tag from <samp class="uri">cdnjs.com</samp> for <samp class="application">Bootstrap</samp>’s JavaScript code.)

# <samp class="chapter_number">11</samp>
<samp class="chapter_name">From Data to DOM</samp>

In the last chapter, you built the <samp class="function">FormHandler</samp> module. It serves as a bridge between the form that the user interacts with and the rest of your code. By intercepting its `submit` event, you supply the user’s input to your <samp class="function">Truck</samp> module, which saves it to its <samp class="function">DataStore</samp> instance.

In this chapter, you will build the other piece of UI code, the <samp class="function">CheckList</samp> module. Like the <samp class="function">Truck</samp> module, it will receive data from the <samp class="function">FormHandler</samp>, but its job is to add a checklist of pending orders to the page. When a checklist item is clicked, the <samp class="function">CheckList</samp> will remove it from the page and signal the <samp class="function">Truck</samp> to remove it from the <samp class="function">DataStore</samp>. [Figure 11.1](#ch11.html_fig-intravenous-drip "Figure 11.1  Keep those orders coming!") shows CoffeeRun equipped with its checklist of pending orders.

**Figure 11.1  Keep those orders coming!**

![Keep those orders coming!](CoffeeRun/Forms2/img/intravenous-drip.png)

## Setting Up the Checklist

You will continue to use <samp class="application">Bootstrap</samp> classes for styling your form elements. Begin in <samp class="filename">index.html</samp> by adding a pair of `<div>` elements with the <samp class="application">Bootstrap</samp> class names `panel`, `panel-default`, and `panel-body`, as you did for your coffee order form. Inside of them, add a header and another `<div>` that will hold the actual checklist items. This markup should be added after the `<div>`s that hold your form.

```
...
    <header>
      <h1>CoffeeRun</h1>
    </header>
    <section>
      <div class="panel panel-default">
        <div class="panel-body">
          <form data-coffee-order="form">
            ...
          </form>
        </div>
      </div>

      <div class="panel panel-default">
        <div class="panel-body">
          <h4>Pending Orders:</h4>
          <div data-coffee-order="checklist">
          </div>
        </div>
      </div>
    </section>
...
```

As before, you added `<div>`s to carry the styling provided by <samp class="application">Bootstrap</samp>. The main part of your checklist is the `[data-coffee-order="checklist"]` element. It will be the target for the JavaScript that creates an individual coffee order checklist item and adds it to the DOM.

Save <samp class="filename">index.html</samp>, start `browser-sync`, and make sure CoffeeRun shows an empty <samp class="guilabel">Pending Orders</samp> area ([Figure 11.2](#ch11.html_fig-empty-pending-orders "Figure 11.2  After adding the markup for the checklist items")).

**Figure 11.2  After adding the markup for the checklist items**

![After adding the markup for the checklist items](CoffeeRun/Forms2/img/empty-pending-orders.png)

Now you are ready to dive back into the JavaScript.

## Creating the CheckList Module

Create a new file in your <samp class="filename">scripts</samp> folder called <samp class="filename">checklist.js</samp> and add a link to it in <samp class="filename">index.html</samp>:

```
...
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.4/jquery.js"
      charset="utf-8"></script>
    <script src="scripts/checklist.js" charset="utf-8"></script>
    <script src="scripts/formhandler.js" charset="utf-8"></script>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
...
```

Save <samp class="filename">index.html</samp>. In <samp class="filename">checklist.js</samp>, add the standard module code using an IIFE. Import the `App` namespace and jQuery, assigning each to a local variable. Create a constructor for <samp class="function">CheckList</samp>, making sure to confirm that there is a selector passed in and that the selector matches at least one element in the DOM. At the end of the IIFE, export the <samp class="function">CheckList</samp> constructor as part of the `App` namespace.

```
(function (window) {
  'use strict';

  var App = window.App || {};
  var $ = window.jQuery;

  function CheckList(selector) {
    if (!selector) {
      throw new Error('No selector provided');
    }

    this.$element = $(selector);
    if (this.$element.length === 0) {
      throw new Error('Could not find element with selector: ' + selector);
    }
  }

  App.CheckList = CheckList;
  window.App = App;
})(window);
```

The <samp class="function">CheckList</samp> module will need three methods to do its work. One will create a checklist item, including the checkbox and the text description. Think of this group of elements as a row in a table.

Another method will remove a row from the table. The third method will add a listener for `click` events, so that your code knows <samp class="emphasis">when</samp> to remove a row.

The first method you will tackle is the one to create a row for a new order. [Figure 11.3](#ch11s02.html_fig-checklist-diagram-1 "Figure 11.3  Order of events when the order form is submitted") shows how <samp class="function">CheckList</samp> will add checklist items to the page when the order form is submitted.

**Figure 11.3  Order of events when the order form is submitted**

![Order of events when the order form is submitted](CoffeeRun/Forms2/img/checklist-diagram-1.png)

## Creating the Row Constructor

You cannot create the markup in <samp class="filename">index.html</samp> for the checklist items, because they need to be added after the page has already been rendered, in response to form submissions. Instead, you will add a <samp class="function">Row</samp> constructor to the <samp class="function">CheckList</samp> module.

The <samp class="function">Row</samp> constructor will be in charge of creating all the DOM elements necessary to represent a single coffee order, including the checkbox and text description. But the <samp class="function">Row</samp> constructor will not be exported to the `App` namespace. It will only be used internally by one of the `CheckList.prototype` methods.

Add the <samp class="function">Row</samp> constructor in <samp class="filename">checklist.js</samp>, just before the `App.CheckList = CheckList;` statement. It should accept an argument called `coffeeOrder` that will be the same data that is sent to <samp class="methodname">Truck.prototype.createOrder</samp>.

```
...
    this.$element = $(selector);
    if (this.$element.length === 0) {
      throw new Error('Could not find element with selector: ' + selector);
    }
  }

  function Row(coffeeOrder) {
    // Constructor code will go here
  }

  App.CheckList = CheckList;
  window.App = App;
})(window);
```

### Creating DOM elements with jQuery

Your <samp class="function">Row</samp> constructor will use jQuery to build DOM elements. You will declare variables for the individual elements that make up a checklist item. Then the constructor will append them together into a <samp class="firstterm">subtree</samp> of DOM elements, as shown in [Figure 11.4](#ch11s03.html_fig-checklist-creates-appends "Figure 11.4  CheckList creates a row and appends its DOM elements"). The <samp class="function">CheckList</samp> will take that subtree and attach it to the page’s DOM tree as a child of the `[data-coffee-order="checklist"]` element.

**Figure 11.4  `CheckList` creates a row and appends its DOM elements**

![CheckList creates a row and appends its DOM elements](CoffeeRun/Forms2/img/checklist-creates-appends.png)

(The “[39x]” in the order description represents the caffeine strength.)

The DOM subtree created by the <samp class="function">Row</samp> constructor in [Figure 11.4](#ch11s03.html_fig-checklist-creates-appends "Figure 11.4  CheckList creates a row and appends its DOM elements") is the equivalent of the following markup:

```
<div data-coffee-order="checkbox" class="checkbox">
  <label>
    <input type="checkbox" value="chewie@rrwwwgg.com">
    tall mocha iced coffee, (chewie@rrwwwgg.com) [39x]
  </label>
</div>
```

A `<div>` with a `checkbox` class is used to house your `<label>` and an `<input>` element. The `checkbox` class will apply the appropriate <samp class="application">Bootstrap</samp> styles to the `<div>`. The `data-coffee-order` attribute will be used in your JavaScript when you need to trigger the click action on the checkbox.

Note that the `type` attribute of your `<input>` is also `checkbox`. This tells the browser to draw the input as a checkbox form element. A plain text description of the order comes right after the `<input>`. The `<label>` wraps both the checkbox input and the plain text description. This turns the text and the input into a click target for the checkbox.

You will create the `<label>`, `<div>`, and `<input>` elements one at a time. Then you will manually place the elements inside of one another to create a DOM subtree that you will attach to the live DOM (the DOM tree currently shown on the page). You will also create a string that holds the text description of the order, like “tall mocha iced coffee, (chewie@rrwwwgg.com) [39x].”

To create these elements, you will use jQuery’s <samp class="function">$</samp> function. Up to now, you only used the <samp class="function">$</samp> function to select elements from the DOM, but it can also be used to create them.

First, you are going to create the `<div>` by calling the <samp class="function">$</samp> function in the <samp class="function">Row</samp> constructor in <samp class="filename">checklist.js</samp>. Pass it two arguments describing the DOM element you want it to create. Make the first argument a string with the HTML tag of the DOM element, in this case `'<div></div>'`. Make the second argument an object that specifies the attributes that jQuery should add to the `<div>`. The key/value pairs of the object literal are translated into the attributes of the new element.

The result is a DOM element created by jQuery that you will assign to a new variable called <samp class="varname">$div</samp>. This will not be an instance variable (that is, it is just <samp class="varname">$div</samp> and not `this.$div`). It is prefixed with the `$` to denote that it is not a plain DOM element, but one that jQuery created a reference to.

Make it so in <samp class="filename">checklist.js</samp>.

```
...
  function Row(coffeeOrder) {
    // Constructor code will go here
    var $div = $('<div></div>', {
      'data-coffee-order': 'checkbox',
      'class': 'checkbox'
    });
  }
...
```

Notice that your two property names are in single quotation marks. You might assume from this that you should always use single quotes around property names when creating a DOM element using jQuery, but actually that is not the case. Property names that have special characters (like the dash) need to be in quotes, otherwise it is considered a syntax error. Valid characters that can be used in a property name (or a variable name) without single quotes are the letters of the alphabet, numerical digits, the underscore (<samp class="literal">_</samp>), and the dollar sign (<samp class="literal">$</samp>).

`'class'` is in single quotes because “class” is a JavaScript-reserved word, so single quotes are needed to prevent the browser from reading it as JavaScript (which would also result in a syntax error).

Next, create the `<label>` element in <samp class="filename">checklist.js</samp> with the <samp class="function">$</samp> function but without an object argument. It does not need any extra attributes.

```
...
  function Row(coffeeOrder) {
    var $div = $('<div></div>', {
      'data-coffee-order': 'checkbox',
      'class': 'checkbox'
    });

    var $label = $('<label></label>');
  }
...
```

Now, create the `<input>` element for the checkbox by calling the <samp class="function">$</samp> function and passing it the HTML for an `<input>` tag. For the second argument, specify that the type should be a `checkbox` and that the `value` should be the email address of the customer. Because none of these property names use special characters, you do not need to put them in single quotes.

```
...
  function Row(coffeeOrder) {
    var $div = $('<div></div>', {
      'data-coffee-order': 'checkbox',
      'class': 'checkbox'
    });

    var $label = $('<label></label>');

    var $checkbox = $('<input></input>', {
      type: 'checkbox',
      value: coffeeOrder.emailAddress
    });
  }
...
```

By setting the `value` to the customer’s email address, you are associating the checkbox with the customer’s coffee order. Later, when you add the `click` handler, you can identify which coffee order was clicked based on the email address in the `value` attribute.

The last thing to create is the text description that will be displayed next to the checkbox. You will build a string for this by concatenating the pieces using the `+=` operator.

Create a variable called <samp class="varname">description</samp> in <samp class="filename">checklist.js</samp>. Set it to the `size` property of the order, then add a comma and a space. If a flavor was provided, concatenate it using `+=`. Then concatenate the `coffee`, `emailAddress`, and `strength` values. The `emailAddress` should be wrapped in parentheses and the `strength` should be in brackets and followed by the letter “x.” (The parentheses and brackets are not for syntactic purposes, just for formatting the text.)

```
...
  function Row(coffeeOrder) {
    ...

    var $checkbox = $('<input></input>', {
      type: 'checkbox',
      value: coffeeOrder.emailAddress
    });

    var description = coffeeOrder.size + ' ';
    if (coffeeOrder.flavor) {
      description += coffeeOrder.flavor + ' ';
    }

    description += coffeeOrder.coffee + ', ';
    description += ' (' + coffeeOrder.emailAddress + ')';
    description += ' [' + coffeeOrder.strength + 'x]';
  }
...
```

The `+=` concatenation operator does addition and assignment in one step. That means that the following two lines of code are equivalent:

```
description += coffeeOrder.flavor + ' ';
description = description + coffeeOrder.flavor + ' ';
```

You now have all the individual parts of the checklist item and are ready to append them to one another ([Figure 11.5](#ch11s03.html_fig-loose-elements-to-subtree "Figure 11.5  Assembling the individual DOM elements into a subtree")).

**Figure 11.5  Assembling the individual DOM elements into a subtree**

![Assembling the individual DOM elements into a subtree](CoffeeRun/Forms2/img/loose-elements-to-subtree.png)

You will do this in three steps:

1.  Append the <samp class="varname">$checkbox</samp> to the <samp class="varname">$label</samp>

2.  Append the <samp class="varname">description</samp> to the <samp class="varname">$label</samp>

3.  Append the <samp class="varname">$label</samp> to the <samp class="varname">$div</samp>

More generally, you will build the subtree by working from left to right, bottom to top. This approach is similar to how you developed your CSS for Ottergram in [Chapter 3](#ch03.html "3 Styles"), by beginning with the smallest, innermost elements and working your way up.

In <samp class="filename">checklist.js</samp>, use the jQuery <samp class="methodname">append</samp> method to connect the elements together. This method accepts either a DOM element or a jQuery-wrapped collection and adds it as a child element.

```
...
  function Row(coffeeOrder) {
    ...
    description += coffeeOrder.coffee + ', ';
    description += ' (' + coffeeOrder.emailAddress + ')';
    description += ' [' + coffeeOrder.strength + 'x]';

    $label.append($checkbox);
    $label.append(description);
    $div.append($label);
  }
...
```

Your <samp class="function">Row</samp> constructor can now create and assemble the subtree of elements using the coffee order data passed in. However, because <samp class="function">Row</samp> will be used as a constructor and not as a regular function, it cannot simply return this subtree. (In fact, constructors should <samp class="emphasis">never</samp> have a return statement; JavaScript automatically returns a value for you when you use the keyword `new` with a constructor.)

Instead, make the subtree available as a property of the instance by assigning it to <samp class="varname">this.$element</samp> in <samp class="filename">checklist.js</samp>. (This name was chosen just to follow the convention used with your other constructors; it does not have any special meaning by itself.)

```
...
  function Row(coffeeOrder) {
    ...
    $label.append($checkbox);
    $label.append(description);
    $div.append($label);

    this.$element = $div;
  }
...
```

The <samp class="function">Row</samp> constructor is ready for work. It can build up the DOM subtree necessary to represent an individual coffee order with a checkbox. It holds on to that DOM representation in an instance variable.

## Creating CheckList Rows on Submit

Next, you will add a method to <samp class="function">CheckList</samp> that will use the <samp class="function">Row</samp> constructor to create <samp class="function">Row</samp> instances. It will append each <samp class="function">Row</samp> instance’s <samp class="varname">$element</samp> to the live DOM on the page.

In <samp class="filename">checklist.js</samp>, add a method to `CheckList.prototype` called <samp class="methodname">addRow</samp>. It should accept an argument called `coffeeOrder`, which will be an object that contains all of the data for a single coffee order.

In this new method, create a new <samp class="function">Row</samp> instance by calling the <samp class="function">Row</samp> constructor and passing it the `coffeeOrder` object. Assign the new instance to the variable <samp class="varname">rowElement</samp>. Then, `append` the <samp class="varname">rowElement</samp>’s <samp class="varname">$element</samp> property (which contains the DOM subtree) to the <samp class="function">CheckList</samp> instance’s <samp class="varname">$element</samp> property (which is a reference to the container for the checklist items).

```
...
  function CheckList(selector) {
    ...
  }

  CheckList.prototype.addRow = function (coffeeOrder) {
    // Create a new instance of a row, using the coffee order info
    var rowElement = new Row(coffeeOrder);

    // Add the new row instance's $element property to the checklist
    this.$element.append(rowElement.$element);
  };

  function Row(coffeeOrder) {
    ...
```

This is all you need to do to add the <samp class="function">Row</samp>’s DOM subtree to the page. Save <samp class="filename">checklist.js</samp>.

In <samp class="filename">main.js</samp>, add a variable for the selector that matches the entire checklist area, `[data-coffee-order="checklist"]`. Then, import the <samp class="function">CheckList</samp> module from the `App` namespace to a local variable, <samp class="varname">CHECKLIST_SELECTOR</samp>.

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var CHECKLIST_SELECTOR = '[data-coffee-order="checklist"]';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var FormHandler = App.FormHandler;
  var CheckList = App.CheckList;
  var myTruck = new Truck('ncc-1701', new DataStore());
...
```

Now you can instantiate a <samp class="function">CheckList</samp> instance to add checklist items.

You might be tempted to just add another call to <samp class="methodname">formHandler.addSubmitHandler</samp>, but this would not work the way you might expect. Why not? Each time you call <samp class="methodname">addSubmitHandler</samp>, it registers a new callback that resets the form (by calling <samp class="methodname">this.reset</samp>).

Consider the following code:

```
...
// Instantiate a new CheckList
var checkList = new CheckList(CHECKLIST_SELECTOR);

var formHandler = new FormHandler(FORM_SELECTOR);
formHandler.addSubmitHandler(myTruck.createOrder.bind(myTruck));

// This will not do what you want!
formHandler.addSubmitHandler(checkList.addRow.bind(checkList));
...
```

This code registers two callbacks that will run when the form is submitted. After the first `submit` handler (<samp class="function">myTruck.createOrder</samp>) is called, the form gets reset. When the second `submit` handler (<samp class="function">checkList.addRow</samp>) is called, there is no information left in the form. The result is that the data is added to the <samp class="function">DataStore</samp>, but a checklist item does not get added to the page.

To get around this, you need to pass a single anonymous function to <samp class="methodname">formHandler.addSubmitHandler</samp> and have that anonymous function call both <samp class="methodname">myTruck.createOrder</samp> and <samp class="methodname">checkList.addRow</samp>.

Also, each of these methods needs to be bound to a specific instance (meaning its `this` keyword needs to be set). You have been using <samp class="methodname">bind</samp> to set the value of `this`, but you will use a different technique here.

### Manipulating this with call

The <samp class="methodname">call</samp> method works similarly to <samp class="methodname">bind</samp> to set the value of `this`. The difference between the two is that while <samp class="methodname">bind</samp> returns a new version of the function or method, it does not invoke it. <samp class="methodname">call</samp> actually invokes the function or method and allows you to pass in the value of `this` as the first argument. (If you need to pass any other arguments to the function, you just add them to the argument list.) <samp class="methodname">call</samp> runs the body of the function and returns any value that would normally be returned.

You need to use <samp class="methodname">call</samp> instead of <samp class="methodname">bind</samp> here because you need to invoke <samp class="methodname">myTruck.createOrder</samp> and <samp class="methodname">checkList.addRow</samp> in addition to setting the value of `this`.

In <samp class="filename">main.js</samp>, remove the existing invocation of <samp class="methodname">formHandler.addSubmitHandler</samp>. Add a new call to <samp class="methodname">formHandler.addSubmitHandler</samp> and pass it an anonymous function that expects a single argument, `data`. Inside the anonymous function, use the <samp class="methodname">call</samp> methods of <samp class="methodname">myTruck.createOrder</samp> and <samp class="methodname">checkList.addRow</samp> to set the value of `this`, passing the `data` object as the second argument.

```
...
  var myTruck = new Truck('ncc-1701', new DataStore());
  window.myTruck = myTruck;
  var checkList = new CheckList(CHECKLIST_SELECTOR);
  var formHandler = new FormHandler(FORM_SELECTOR);

  formHandler.addSubmitHandler(myTruck.createOrder.bind(myTruck));
                               function (data) {
    console.log(formHandler);
    myTruck.createOrder.call(myTruck, data);
    checkList.addRow.call(checkList, data);
  });
})(window);
```

You have created a single `submit` handler function that invokes both <samp class="methodname">createOrder</samp> and <samp class="methodname">addRow</samp>. When it invokes them, it passes the correct value of `this` and the `data` from the form.

Save your changes and try out your checklist functionality in the browser by entering some data and submitting the form. When you submit each order, you will see it added to the <samp class="guilabel">Pending Orders</samp> checklist, as in [Figure 11.6](#ch11s04.html_fig-adding-checklist-items "Figure 11.6  Submitting the form adds an item to the checklist").

**Figure 11.6  Submitting the form adds an item to the checklist**

![Submitting the form adds an item to the checklist](CoffeeRun/Forms2/img/adding-checklist-items.png)

## Delivering an Order by Clicking a Row

You are almost there! CoffeeRun’s users can fill out the form to add orders. When they submit the form, it adds the order information to the application’s database and draws a checklist item for the order.

Next, users should be able to check off the checklist items. When a checklist item is clicked, meaning that the order has been delivered, the order information should be deleted from the database and the checklist item should be removed from the page. [Figure 11.7](#ch11s05.html_fig-checklist-diagram-2 "Figure 11.7  Sequence diagram: clicking a checklist item") shows this process.

**Figure 11.7  Sequence diagram: clicking a checklist item**

![Sequence diagram: clicking a checklist item](CoffeeRun/Forms2/img/checklist-diagram-2.png)

First, you will create the functionality for removing the checklist item from the page.

### Creating the CheckList.prototype.removeRow method

When you create a <samp class="function">Row</samp>, the `value` of the `<input>` is set to the customer’s email address. <samp class="methodname">removeRow</samp> will use the email address argument to find the right <samp class="function">CheckList</samp> item to remove from the UI. It will do that by creating an attribute selector to find the `<input>` whose `value` attribute matches the email address.

When it has found the matching element, it will move up the DOM until it finds the `[data-coffee-order="checkbox"]`.

This is the `<div>` that wraps around all of the elements that are part of a row. Finally, with that `<div>` selected using jQuery, its <samp class="methodname">.remove</samp> method can be called, removing the element from the DOM and also cleaning up any event listeners that were attached to any element in that DOM subtree.

Add the <samp class="methodname">removeRow</samp> method in <samp class="filename">checklist.js</samp> and specify an `emailAddress` parameter. Use the <samp class="varname">$element</samp> instance property to search for any descendant elements whose `value` attribute matches the `email` parameter. From that matching element, add a call to <samp class="methodname">closest</samp> to search for an ancestor whose `data-coffee-order` attribute is equal to `"checkbox"`. Finally, call <samp class="methodname">remove</samp> on that element. (You will notice some new syntax in this code, which we will explain after you enter it.)

```
...
  CheckList.prototype.addRow = function (coffeeOrder) {
    ...
  };

  CheckList.prototype.removeRow = function (email) {
    this.$element
      .find('[value="' + email + '"]')
      .closest('[data-coffee-order="checkbox"]')
      .remove();
  };

  function Row(coffeeOrder) {
    ...
```

Here, you have <samp class="firstterm">chained</samp> several method calls together. jQuery is designed so that you can write multiple method calls for an object like a list of steps. You only include the semicolon at the end of the very last method call.

The requirement for chaining is that a method must return a jQuery-wrapped selection in order to have another method call chained to it. <samp class="methodname">find</samp> returns a jQuery-wrapped selection, as does <samp class="methodname">closest</samp>. This allows you to chain the three method calls together.

Notice that you used <samp class="methodname">this.$element.find</samp>. This does a <samp class="firstterm">scoped</samp> selection: Instead of searching the entire DOM, it only searches the descendants of the checklist, which you have a reference to with `this.$element`.

### Removing overwritten entries

Save your file and switch to the browser. Using your form, enter two orders for the same email address. Make the `coffee` for the first “order 1” and for the second “order 2.” After submitting both orders, call <samp class="function">myTruck.printOrders</samp> in the console. [Figure 11.8](#ch11s05.html_fig-greedy "Figure 11.8  Orders for same email address remain in UI") shows the result.

**Figure 11.8  Orders for same email address remain in UI**

![Orders for same email address remain in UI](CoffeeRun/Forms2/img/greedy.png)

You decided early on to allow only one open order per customer. Because you are using a simple key/value store for your data, any subsequent orders for the same customer email address overwrite the existing one. So, as the console shows, “order 2” is the only pending order. “Order 1” has been overwritten.

But the checklist does not reflect this – it still shows rows for both “order 1” and “order 2.” When you add a row for an order, you need to make sure that any existing rows associated with the same customer email address are removed.

Now that you can remove rows based on the customer’s email address, this is straightforward. In <samp class="filename">checklist.js</samp>, update the <samp class="methodname">addRow</samp> prototype method so that the first thing it does is call <samp class="methodname">removeRow</samp>, passing in the email address of the customer.

```
...
  CheckList.prototype.addRow = function (coffeeOrder) {
    // Remove any existing rows that match the email address
    this.removeRow(coffeeOrder.emailAddress);

    // Create a new instance of a row, using the coffee order info
    var rowElement = new Row(coffeeOrder);

    // Add the new row instance's $element property to the checklist
    this.$element.append(rowElement.$element);
  };
...
```

Save <samp class="filename">checklist.js</samp> and verify in the browser that the first order’s checklist item is removed when a second order with the same email is submitted.

Now that you can remove a checklist row from the UI, turn your attention to handling the checklist `click` event.

### Writing the addClickHandler method

To handle clicks to the checklist, you will use the same event handler registration technique that you used with <samp class="function">FormHandler</samp>.

<samp class="methodname">FormHandler.prototype.addSubmitHandler</samp> accepts a function argument, <samp class="varname">fn</samp>, and then registers an anonymous function to handle the `submit` event of `this.$formElement`. Inside of that anonymous function, <samp class="varname">fn</samp> is invoked. Here is that method definition for reference:

```
 FormHandler.prototype.addSubmitHandler = function (fn) {

    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();

      var data = {};
      $(this).serializeArray().forEach(function (item) {
        data[item.name] = item.value;
        console.log(item.name + ' is ' + item.value);
      });
      console.log(data);

      fn(data);
      this.reset();
      this.elements[0].focus();
    });
  };
```

This makes <samp class="methodname">FormHandler.prototype.addSubmitHandler</samp> flexible, because it can be passed any function that needs to run when the form is submitted. This way, <samp class="methodname">FormHandler.prototype.addSubmitHandler</samp> does not need to know the details of that function or what steps it takes.

You will add a prototype method to <samp class="function">CheckList</samp> called <samp class="methodname">addClickHandler</samp> that will work the same way as <samp class="function">FormHandler</samp>’s <samp class="methodname">addSubmitHandler</samp>. That is, it will:

1.  Accept a function argument.

2.  Register an event handler callback.

3.  Invoke the function argument inside the event handler callback.

<samp class="methodname">CheckList.prototype.addClickHandler</samp> differs from <samp class="methodname">FormHandler.prototype.addSubmitHandler</samp> in that it will listen for a `click` event and <samp class="methodname">bind</samp> the callback to the <samp class="function">CheckList</samp> instance.

In <samp class="filename">checklist.js</samp>, add the <samp class="methodname">addClickHandler</samp> method and specify a parameter named `fn`. Listen for a `click` event using jQuery’s <samp class="methodname">on</samp> method.

Inside the event handler function, declare a local variable named <samp class="varname">email</samp> and assign it `event.target.value`, which is the customer’s email address. Then call <samp class="methodname">removeRow</samp>, passing it <samp class="varname">email</samp>. After that, invoke `fn` and pass it <samp class="varname">email</samp> also. Make sure to use <samp class="methodname">bind(this)</samp> to set the context object of the event handler function.

```
...
  function CheckList(selector) {
    ...
  }

  CheckList.prototype.addClickHandler = function (fn) {
    this.$element.on('click', 'input', function (event) {
      var email = event.target.value;
      this.removeRow(email);
      fn(email);
    }.bind(this));
  };

  CheckList.prototype.addRow = function (coffeeOrder) {
    ...
```

When you registered the event handler callback with `this.$element.on`, you specified `click` as the event name. But you also passed in a <samp class="firstterm">filtering selector</samp> as the second argument. The filtering selector tells the event handler to run the callback function <samp class="emphasis">only</samp> if the event was triggered by an `<input>` element.

This is a pattern called <samp class="firstterm">event delegation</samp>. It works because some events, like clicks and keypresses, <samp class="firstterm">propagate</samp> through the DOM, meaning each ancestor element is informed about the event.

Any time you need to listen for an event on elements that are dynamically created and removed, such as the checklist items, you should use event delegation. It is easier and more performant to add a single listener to the dynamic elements’ container and then run the handler function based on what element triggered the event.

Notice that you do <samp class="emphasis">not</samp> call `event.preventDefault` inside the event handler. Why not? If you called `event.preventDefault`, the checkbox would not actually change its visual state to show a checkmark in the box.

Also, notice that you <samp class="methodname">bind</samp> the event handler callback to `this`, which refers to the instance of <samp class="function">CheckList</samp>.

### Calling addClickHandler

<samp class="methodname">addClickHandler</samp> needs to be connected to <samp class="methodname">deliverOrder</samp>. Go to <samp class="filename">main.js</samp> to make that connection. Pass a bound version of <samp class="methodname">deliverOrder</samp> to <samp class="methodname">checkList.addClickHandler</samp>.

```
...
  var myTruck = new Truck('ncc-1701', new DataStore());
  window.myTruck = myTruck;
  var checkList = new CheckList(CHECKLIST_SELECTOR);
  checkList.addClickHandler(myTruck.deliverOrder.bind(myTruck));
  var formHandler = new FormHandler(FORM_SELECTOR);
...
```

Save your changes and add some coffee orders in the form. Click either the checkbox or the text of one of the checklist items, and it will be removed ([Figure 11.9](#ch11s05.html_fig-click-a-checklist-item "Figure 11.9  Clicking a checklist item removes it"))!

**Figure 11.9  Clicking a checklist item removes it**

![Clicking a checklist item removes it](CoffeeRun/Forms2/img/click-a-checklist-item.png)

You have learned how to create dynamic form elements and work with the events they generate. You were able to associate each one with a specific coffee order by using the email address as an identifier.

Using these techniques, you completed the modules that manage the UI, turning what was a console-only application into one that could be used for a real-world task.

You have completed two of the three major parts of CoffeeRun. The internal logic governs the data within the application. The form elements, <samp class="function">FormHandler</samp>, and <samp class="function">CheckList</samp> provide the interactive UI. The next chapters deal with preparing and exchanging data with a remote server.

## Bronze Challenge: Adding the Strength to the Description

You have decided that the strength of the coffee is a more important piece of information and should be the first part of the description.

Change the way you are writing the order descriptions so that the coffee strength is at the beginning of the description text.

## Silver Challenge: Color Coding by Flavor Shot

Color code your orders based on the flavor shot. Based on the options chosen for each coffee, display the row in the checklist with a different background color.

Make sure that the text has enough contrast with the background color.

## Gold Challenge: Allowing Order Editing

Allow existing orders to be edited. You will need to change the way the checklist works.

If the user double-clicks an order, load it back into the form for editing. If the user only clicks once, gray out the row. After a few seconds, treat the item as if it were delivered and remove it from the checklist and from the application’s data.

As an extra bonus, make sure that after the user finishes editing the existing row is updated in place, not removed and replaced with a new row.

# <samp class="chapter_number">12</samp>
<samp class="chapter_name">Validating Forms</samp>

CoffeeRun is humming along! Users can enter coffee orders in the form, and the order information is processed and stored. But what would happen to your app – and your coffee truck – if someone submitted an order with missing or unusable information?

Not to worry. You can easily handle these scenarios with a little bit of code to make sure the data is OK for your application to use. In fact, this is an essential step if you ever send data back to a server. Almost every modern browser is prepared to validate form data when it is submitted. All you need to do is provide the rules.

In this chapter, you are going to learn two techniques for form validation. The first technique is to add validation attributes to the HTML, allowing the browser’s built-in validation mechanisms to take effect. The second is to write your own validation code in JavaScript, using the Constraint Validation API.

## The required Attribute

The most basic form of validation is to check whether a field has a value and is not completely empty. This kind of check does not make sense for fields with default values, like your size, flavor, and strength fields. But it is just what you need for your order and email fields – you definitely do not want orders to be submitted with those fields left blank.

In <samp class="filename">index.html</samp>, add the `required` Boolean attribute to the order and email fields.

```
...
            <div class="form-group">
              <label for="coffeeOrder">Order</label>
              <input class="form-control" name="coffee" id="coffeeOrder"
                autofocus required />
            </div>

            <div class="form-group">
              <label for="emailInput">Email</label>
              <input class="form-control" type="email" name="emailAddress"
              id="emailInput" value="" placeholder="dr@who.com"
                required />
            </div>
...
```

Remember that a Boolean attribute should not be assigned a value. If you make the mistake of writing something like `required="false"`, the value will be `true` and the field will be required! The browser only cares about the <samp class="emphasis">existence</samp> of the attribute and ignores any value assigned.

That point bears repeating: If a Boolean attribute exists for an element, the browser considers the value to be `true`, regardless of the value you set for it.

Save <samp class="filename">index.html</samp>, make sure `browser-sync` is running, and load CoffeeRun in the browser. Try submitting the form without filling out either or both of the required fields. You will see a warning, as in [Figure 12.1](#ch12.html_fig-required-validation-errors "Figure 12.1  Errors when required fields are blank").

**Figure 12.1  Errors when required fields are blank**

![Errors when required fields are blank](CoffeeRun/Validation/img/required-validation-errors.png)

Also, notice that there are no console messages from your `submit` handlers. The `submit` event only fires <samp class="emphasis">after</samp> the browser validates your form ([Figure 12.2](#ch12.html_fig-submission-validation-flow "Figure 12.2  Two possible sequences of events when a form is validated")).

**Figure 12.2  Two possible sequences of events when a form is validated**

![Two possible sequences of events when a form is validated](CoffeeRun/Validation/img/submission-validation-flow.png)

## Validating with Regular Expressions

Making a field `required` is an easy way to ensure that the user does not leave the field blank. But what if you want to be specific about what should go into a field? This kind of validation calls for the `pattern` attribute.

After the `required` attribute on your order `<input>`, add a `pattern` attribute. Assign it a specially formatted string called a <samp class="emphasis">regular expression</samp>, which we will explain in a moment.

```
...
            <div class="form-group">
              <label for="coffeeOrder">Order</label>
              <input class="form-control" name="coffee" id="coffeeOrder"
                autofocus required pattern="[a-zA-Z\s]+" />
            </div>
...
```

A regular expression is a sequence of characters for pattern matching. The regular expression `[a-zA-Z\s]+` matches any character from the set consisting of lowercase letters (`a-z`), uppercase letters (`A-Z`), and whitespace characters (`\s`), repeated one or more times (`+`).

In short, when you submit the form this field will only be valid if it contains letters or spaces.

Save and reload. See what happens if you put symbols or numbers into the order field and try to submit the form.

## Constraint Validation API

The most robust way to validate a form field in the browser is to write a validation function. You can use validation functions in conjunction with the Constraint Validation API to trigger built-in validation behavior.

But there is a catch, and it is not a small one: The Constraint Validation API has poor support in Apple’s <samp class="application">Safari</samp> browser.

Despite this oversight, it is important to write code that targets standard behavior and then add a JavaScript library that adds support for noncompliant browsers. (You can read more about this in [the section called *For the More Curious: The Webshims Library*](#ch12s06.html "For the More Curious: The Webshims Library") at the end of this chapter.)

Suppose your coffee truck is only for employees of your company, so you want to make sure that the customer is an employee. One way to do this would be to ensure that the email address that is submitted is from your company’s domain.

You <samp class="emphasis">could</samp> use a `pattern` attribute for your `emailAddress` field. But this problem is a good one for learning the Constraint Validation API. (Also, after you work through the next chapter, you could expand beyond a simple email domain check and query a remote server to find out whether the email address actually exists.)

Create a new file, <samp class="filename">scripts/validation.js</samp>, to hold your validation functions. Add a `<script>` tag in <samp class="filename">index.html</samp> for your new module.

```
...
      </div>
    </section>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.4/jquery.js"
      charset="utf-8"></script>
    <script src="scripts/validation.js" charset="utf-8"></script>
    <script src="scripts/checklist.js" charset="utf-8"></script>
    <script src="scripts/formhandler.js" charset="utf-8"></script>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

Save <samp class="filename">index.html</samp>. In <samp class="filename">validation.js</samp>, add an IIFE module that creates an empty object literal, assigns it to a variable named <samp class="varname">Validation</samp>, and then exports that variable to the `App` namespace.

```
(function (window) {
  'use strict';
  var App = window.App || {};

  var Validation = {

  };

  App.Validation = Validation;
  window.App = App;
})(window);
```

Your new `Validation` module will only be used for organizing functions, so it does not need to be a constructor.

Add a method called <samp class="function">isCompanyEmail</samp>. This method will test an email address against a regular expression and return `true` or `false`. (Feel free to change the email domain specified.)

```
(function () {
  'use strict';
  var App = window.App || {};

  var Validation = {
    isCompanyEmail: function (email) {
      return /.+@bignerdranch\.com$/.test(email);
    }
  };

  App.Validation = Validation;
  window.App = App;
})(window);
```

You created a literal regular expression by putting a pattern between the forward slashes, `//`. Inside the slashes, you specify a string that consists of one or more characters (`.+`), followed by “@bignerdranch.com” – you also used a backslash to indicate that the period in <samp class="literal">bignerdranch.com</samp> should be treated as a literal period. (Normally, a period in a regular expression is a wildcard that matches any character.) The “$” at the end of regular expression means that “@bignerdranch.com” should be at the end of the string – there should be no more characters that appear after it.

This regular expression is an object and has a <samp class="methodname">test</samp> method. You can pass a string to the <samp class="methodname">test</samp> method, and it will return a Boolean – `true` if the regular expression matches the string and `false` if not. (For a list of other regular expression methods, see [<samp class="uri">developer.mozilla.org/​en-US/​docs/​Web/​JavaScript/​Reference/​Global_Objects/​RegExp</samp>](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp).)

Test your <samp class="function">App.Validation.isCompanyEmail</samp> function on the console ([Figure 12.3](#ch12s03.html_fig-iscompanyemail-validation "Figure 12.3  Testing App.Validation.isCompanyEmail on the console")).

**Figure 12.3  Testing `App.Validation.isCompanyEmail` on the console**

![Testing App.Validation.isCompanyEmail on the console](CoffeeRun/Validation/img/iscompanyemail-validation.png)

You now have a function that can check for valid email addresses. The next thing to do is to connect it to the form.

### Listening for the input event

When should you use this function? There are several events that the input field could trigger while a user is filling out the form. One occurs as the user types each character. Another is when the user removes focus from the field. Or you could run the function when the form is submitted.

The Constraint Validation API requires that invalid fields be marked prior to submission. If any fields are invalid, the browser stops short of triggering the `submit` event. So doing the check on submit is too late.

The event triggered when the user removes focus from a field is known as a <samp class="firstterm">blur</samp> event. It is not a good choice for validation, either. Suppose the user’s cursor is in the email input, so that field has focus. If the user then presses the Return key, this would trigger form submission, but the `blur` event would not be triggered and any validation tied to it would not be performed.

So the validation check will need to happen as the user enters each character. Update the <samp class="function">FormHandler</samp> module in <samp class="filename">formhandler.js</samp> with an <samp class="methodname">addInputHandler</samp> prototype method. It should add a listener for the `input` event of the form. Like the <samp class="methodname">addSubmitHandler</samp> method, it should accept a function argument.

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    ...
  };

  FormHandler.prototype.addInputHandler = function (fn) {
    console.log('Setting input handler for form');
  };

  App.FormHandler = FormHandler;
  window.App = App;
...
```

Attach the listener for the `input` event using jQuery’s <samp class="methodname">on</samp> method. Make sure to use the event delegation pattern to filter out events created by anything but the `[name="emailAddress"]` field.

```
...
  FormHandler.prototype.addInputHandler = function (fn) {
    console.log('Setting input handler for form');
    this.$formElement.on('input', '[name="emailAddress"]', function (event) {
      // Event handler code will go here
    });
  };

  App.FormHandler = FormHandler;
  window.App = App;
...
```

Inside the event handler, extract the value of the email field from the `event.target` object. Then `console.log` the result of running <samp class="methodname">addInputHandler</samp>’s function argument <samp class="varname">fn</samp> and passing it the value of the email field.

```
...
  FormHandler.prototype.addInputHandler = function (fn) {
    console.log('Setting input handler for form');
    this.$formElement.on('input', '[name="emailAddress"]', function (event) {
      // Event handler code will go here
      var emailAddress = event.target.value;
      console.log(fn(emailAddress));
    });
  };

  App.FormHandler = FormHandler;
  window.App = App;
...
```

Save <samp class="filename">formhandler.js</samp>.

### Associating the validation check with the input event

In <samp class="filename">main.js</samp>, import <samp class="function">Validation</samp> from the `App` namespace and assign it to a local variable.

```
...
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var FormHandler = App.FormHandler;
  var Validation = App.Validation;
  var CheckList = App.CheckList;
  var myTruck = new Truck('ncc-1701', new DataStore());
...
```

With the <samp class="function">Validation</samp> object imported, you can connect it to <samp class="function">FormHandler</samp>’s new <samp class="methodname">addInputHandler</samp> method.

At the end of <samp class="filename">main.js</samp>, pass <samp class="methodname">Validation.isCompanyEmail</samp> to the <samp class="methodname">addInputHandler</samp> method of the <samp class="varname">formHandler</samp> instance:

```
...
  formHandler.addSubmitHandler(function (data) {
    myTruck.createOrder.call(myTruck, data);
    checkList.addRow.call(checkList, data);
  });

  formHandler.addInputHandler(Validation.isCompanyEmail);

})(window);
```

Save and reload. Fill out the email field and see what appears on the console. As you type a valid email address, the console will show a number of `false` results, printed by the `console.log(fn(emailAddress));` line in <samp class="methodname">FormHandler.prototype.addInputHandler</samp>. When you have finished typing a valid email address, you will see `true` printed in the console ([Figure 12.4](#ch12s03.html_fig-validating-email-console "Figure 12.4  Logging the email validation check")).

**Figure 12.4  Logging the email validation check**

![Logging the email validation check](CoffeeRun/Validation/img/validating-email-console.png)

Your validation function is run each time a character is entered (or removed) from the email field. When you have confirmed that it is correctly checking your input, you can use it to show a custom error message.

### Triggering the validity check

Now that you can reliably test that the email address is from your company’s domain, you should notify the user if the validation fails. You will use the <samp class="methodname">setCustomValidity</samp> method for the <samp class="varname">event.target</samp> to mark it as invalid.

In <samp class="filename">formhandler.js</samp>, remove the `console.log` statement and replace it with a variable for a warning message and an `if`/`else` clause. If the `fn(emailAddress)` call returns `true`, clear the custom validity of the field. If it returns `false`, assign the <samp class="varname">message</samp> variable to a string with the warning message and set the custom validity to <samp class="varname">message</samp>.

```
...
  FormHandler.prototype.addInputHandler = function (fn) {
    console.log('Setting input handler for form');
    this.$formElement.on('input', '[name="emailAddress"]', function (event) {
      var emailAddress = event.target.value;
      console.log(fn(emailAddress));
      var message = '';
      if (fn(emailAddress)) {
        event.target.setCustomValidity('');
      } else {
        message = emailAddress + ' is not an authorized email address!'
        event.target.setCustomValidity(message);
      }
    });
  };
...
```

You passed in the error message that should be shown to the user. If there is no error, you still have to call <samp class="methodname">setCustomValidity</samp>, but with an empty string as the argument. This has the effect of marking the field as valid.

The validation check that occurs as you type only marks the field as valid or invalid. It does not display the error message. When you press the <samp class="guibutton">Submit</samp> button, the browser checks for invalid fields and displays the validation message if it finds any.

To try it out, submit the form after entering an email address that does not match the domain. Right after you press the <samp class="guibutton">Submit</samp> button, you should see your custom validation message appear as a warning next to the field ([Figure 12.5](#ch12s03.html_fig-knope "Figure 12.5  Only valid email addresses allowed!")).

**Figure 12.5  Only valid email addresses allowed!**

![Only valid email addresses allowed!](CoffeeRun/Validation/img/knope.png)

## Styling Valid and Invalid Elements

CoffeeRun now validates both the order field and the email address. Now it is time to enhance the UI by visually marking invalid fields. For this very short piece of CSS, you will add one ruleset in a `<style>` tag to the `<head>` in <samp class="filename">index.html</samp>.

```
...
  <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootst
rap/3.3.6/css/bootstrap.min.css">
    <style>
      form :invalid {
        border-color: #a94442;
      }
    </style>
  </head>
...
```

This adds a border to any field inside your form that has the pseudo-class `:invalid`. This pseudo-class is automatically added by the browser when the form runs its validation checks.

Save and return to the browser. Press the Tab key a few times (or click outside of the text-entry fields) to focus on a form element other than the order or email fields. The two required fields will have a reddish border color ([Figure 12.6](#ch12s04.html_fig-trust-us "Figure 12.6  Trust us: These borders are red")).

**Figure 12.6  Trust us: These borders are red**

![Trust us: These borders are red](CoffeeRun/Validation/img/trust-us.png)

It would be more appropriate for the border to only appear on an invalid field that is required and has focus. Add two more pseudo-classes to your selector in <samp class="filename">index.html</samp>:

```
 <head>
    <meta charset="utf-8">
    <title>coffeerun</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootst
rap/3.3.6/css/bootstrap.min.css">
    <style>
      form :focus:required:invalid {
        border-color: #a94442;
      }
    </style>
  </head>
...
```

You have specified that fields that have the three pseudo-classes `:focus`, `:required`, and `:invalid` will get the new border color ([Figure 12.7](#ch12s04.html_fig-trust-us-focus "Figure 12.7  :invalid border color only for field with focus")).

**Figure 12.7  `:invalid` border color only for field with focus**

![:invalid border color only for field with focus](CoffeeRun/Validation/img/trust-us-focus.png)

CoffeeRun is developing into a fully featured web app. In the next two chapters, you will sync the data to a remote server using Ajax.

## Silver Challenge: Custom Validation for Decaf

Add another function to your `Validation` module. It should accept two arguments: a string and an integer. If the string contains the word “decaf” and the integer is greater than 20, the function should return `false`.

Add listeners for the coffee order text field and for the caffeine strength slider. Trigger the custom validation for whichever field is currently being edited and caused the validation failure.

## For the More Curious: The Webshims Library

As mentioned earlier, one notable browser that does not support the Constraint Validation API is Apple’s <samp class="application">Safari</samp> browser. Should you need to support <samp class="application">Safari</samp>, you can use a library, or <samp class="firstterm">polyfill</samp>, that simulates the API for browsers that do not implement it.

One library that will provide Constraint Validation in <samp class="application">Safari</samp> is the Webshims Lib, which you can download from [<samp class="uri">github.com/​aFarkas/​webshim</samp>](https://github.com/aFarkas/webshim).

Actually, the Webshims library can act as a polyfill for many, many features. Setting it up and using it is straightforward. (However, it does do a lot of different things, and it is easy to get lost in the documentation.)

Here is how you use it with CoffeeRun so that <samp class="application">Safari</samp> works with your <samp class="function">Validation</samp> module. First, download a zip file from the project page: [<samp class="uri">github.com/​aFarkas/​webshim/​releases/​latest</samp>](https://github.com/aFarkas/webshim/releases/latest). Unzip the file and put the <samp class="filename">js-webshim/webshim</samp> folder in your <samp class="filename">coffeerun</samp> directory (next to <samp class="filename">index.html</samp> and your <samp class="filename">scripts</samp> folder).

Add a `<script>` tag in <samp class="filename">index.html</samp> for the <samp class="filename">webshim/polyfiller.js</samp> file.

```
...
      </div>
    </section>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.4/jquery.js"
      charset="utf-8"></script>
    <script src="webshim/polyfiller.js" charset="utf-8"></script>
    <script src="scripts/validation.js" charset="utf-8"></script>
    <script src="scripts/checklist.js" charset="utf-8"></script>
    <script src="scripts/formhandler.js" charset="utf-8"></script>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

Then, add these lines to <samp class="filename">main.js</samp>:

```
...
  var Validation = App.Validation;
  var CheckList = App.CheckList;
  var webshim = window.webshim;
  var myTruck = new Truck('ncc-1701', new DataStore());

  ...

  formHandler.addInputHandler(Validation.isCompanyEmail);

  webshim.polyfill('forms forms-ext');
  webshim.setOptions('forms', { addValidators: true, lazyCustomMessages: true });

}(window));
```

This imports the `webshim` library and then configures it for use with forms.

Finally, there is one quirk with the library that you need to know. Anywhere you use <samp class="methodname">setCustomValidity</samp>, you must wrap the objects with jQuery. For CoffeeRun, you need to wrap the `event.target` objects of the <samp class="methodname">addInputHandler</samp> function in <samp class="filename">formhandler.js</samp>:

```
...
  FormHandler.prototype.addInputHandler = function (fn) {
    console.log('Setting input handler for form');
    this.$formElement.on('input', '[name="emailAddress"]', function (event) {
      var emailAddress = event.target.value;
      var message = '';
      if (fn(emailAddress)) {
        $(event.target).setCustomValidity('');
      } else {
        message = emailAddress + ' is not an authorized email address!'
        $(event.target).setCustomValidity(message);
      }
    });
  };
...
```

The authors of Webshim chose to implement the polyfill functionality entirely as an extension of jQuery. Other than this wrapping, you do not need to modify your code.

After you save your changes, you can test your validation in <samp class="application">Safari</samp>. You should see that it also reports an issue if you forget to fill out the coffee order or if you enter an invalid email address ([Figure 12.8](#ch12s06.html_fig-safari-polyfill "Figure 12.8  Using Webshim as a Safari polyfill")).

**Figure 12.8  Using Webshim as a Safari polyfill**

![Using Webshim as a Safari polyfill](CoffeeRun/Validation/img/safari-polyfill.png)

Webshim goes well beyond providing form validation. You should browse through the documentation to see what else it can do for you on your projects.

# <samp class="chapter_number">13</samp>
<samp class="chapter_name">Ajax</samp>

In the last chapter, you used the browser’s built-in validation to ensure that the user entered data that fit CoffeeRun’s parameters. After doing those checks, you can feel confident about sending that data to the server.

At the moment, the <samp class="methodname">FormHandler.prototype.addSubmitHandler</samp> method calls the event object’s <samp class="methodname">preventDefault</samp> method to keep the browser from sending a request to the server. Normally, the server sends back a response that causes the page to reload. Instead, you are extracting the data that the user enters into the form and updating the form and the checklist with JavaScript.

In this chapter, you will create a <samp class="function">RemoteDataStore</samp> module that sends a request to the server and handles the response ([Figure 13.1](#ch13.html_fig-end-of-callbacks-chapter "Figure 13.1  CoffeeRun at the end of the chapter")). But it will do this in the background using <samp class="firstterm">Ajax</samp>, without causing the browser to reload.

**Figure 13.1  CoffeeRun at the end of the chapter**

![CoffeeRun at the end of the chapter](CoffeeRun/Ajax-Callbacks/img/coffee-orders-over-network.png)

Ajax is a technique for communicating with a remote server via JavaScript. The JavaScript usually changes the contents of a web page using data returned by the server without reloading the browser. This can improve the experience of using a web application.

Originally, the term “Ajax” was an acronym for “asynchronous JavaScript and XML,” but it is now used generically for this style of asynchronous data communication, regardless of what technologies are actually involved. (Asynchronous communication means that the app, having sent a request, does not have to wait for a response from the server before continuing with other tasks.) Ajax is now the standard mechanism for sending and receiving data in the background.

## XMLHttpRequest Objects

At the core of Ajax is the `XMLHttpRequest` API. In modern browsers, you can instantiate new `XMLHttpRequest` objects, which allow you to send requests to servers without causing a page reload. They perform their work in the background.

Using `XMLHttpRequest` objects, you can attach callbacks to different stages of the request/response cycle, much in the same way that you listen to events on DOM objects. You can also inspect the `XMLHttpRequest` object’s properties to access information about the status of the request/response cycle. Two useful properties are `response` and `status`, which are updated as soon as any changes occur. The `response` property contains the data (such as HTML, XML, JSON, or another format) sent back by the server. The `status` is a numeric code that tells you whether the HTTP response was successful or not. These are officially known as <samp class="firstterm">HTTP Status Codes</samp>.

Status codes are grouped in ranges, and these ranges have basic meanings. For example, the status codes in the 200-299 range are success codes, while status codes in the 500-599 range mean that there was a server error. You will often see these ranges referred to generically, as in “2xx” or “3xx” statuses.

[Table 13.1](#ch13.html_tab-http-response-codes "Table 13.1  Common HTTP status codes") shows some of the more common codes.

**Table 13.1  Common HTTP status codes**

| Status Code | Status Text | Description |
| --- | --- | --- |
| 200 | OK | The request was successful. |
| 400 | Bad Request | The server did not understand the request. |
| 404 | Not Found | The resource could not be found, often because the file or path name did not match anything on the server. |
| 500 | Internal Server Error | The server encountered an error, such as an unhandled exception in the server-side code. |
| 503 | Service Unavailable | The server could not handle the request, often because it is overloaded or down for maintenance. |

jQuery has a number of methods that create and manage `XMLHttpRequest` objects and provide a concise, backward-compatible, cross-browser API. It is not the only library available for managing Ajax requests, but many other libraries simply follow jQuery’s lead. You will be using jQuery’s <samp class="methodname">get</samp> and <samp class="methodname">post</samp> methods to work with Ajax `GET` and `POST` requests and the jQuery <samp class="methodname">ajax</samp> method to handle `DELETE` requests.

## RESTful Web Services

You are going to enhance CoffeeRun by using a remote web service to store your application data. The server you will use has been created specifically for this book.

The CoffeeRun server provides a RESTful web service. “REST” stands for “representational state transfer,” which is a style of web service that relies on HTTP verbs (`GET`, `POST`, `PUT`, `DELETE`) and URLs that identify resources on the server.

Frequently, the URL path (the part that comes after the server name) will refer either to a collection of things (such as `/coffeeorders`) or to individual things, specified by an ID (such as `/coffeeorders/[customer email]`).

This difference affects how the HTTP verbs apply. For example, when working with a collection, a `GET` request retrieves a list of all items in the collection. With an individual item, a `GET` request retrieves all of the details for that item.

The URL and HTTP verb patterns are summarized in [Table 13.2](#ch13s02.html_tab-url-http "Table 13.2  Example of RESTful URL and HTTP verb patterns").

**Table 13.2  Example of RESTful URL and HTTP verb patterns**

| URL Path | `GET` | `POST` | `PUT` | `DELETE` |
| --- | --- | --- | --- | --- |
| `/coffeeorders` | list all records | create one record | - | delete all records |
| `/coffeeorders/a@b.com` | get the record | - | update the record | delete the record |

## The RemoteDataStore Module

In a moment, you will create a new module called <samp class="function">RemoteDataStore</samp>. The job of <samp class="function">RemoteDataStore</samp> will be to talk to a server on behalf of the rest of the application. It will have all the same methods as <samp class="function">DataStore</samp> – <samp class="methodname">add</samp>, <samp class="methodname">get</samp>, <samp class="methodname">getAll</samp>, and <samp class="methodname">remove</samp> – which it will use to communicate with the server ([Figure 13.2](#ch13s03.html_fig-remote-vs-local-datastore "Figure 13.2  DataStore vs RemoteDataStore")).

**Figure 13.2  `DataStore` vs `RemoteDataStore`**

![DataStore vs RemoteDataStore](CoffeeRun/Ajax-Callbacks/img/remote-vs-local-datastore.png)

You will be able to use an instance of <samp class="function">RemoteDataStore</samp> in place of <samp class="function">DataStore</samp> without having to change your <samp class="function">Truck</samp>, <samp class="function">FormHandler</samp>, or <samp class="function">CheckList</samp> modules. (You will not be deleting your <samp class="function">DataStore</samp> module, though. You might want to create a future enhancement allowing CoffeeRun to switch between the two storage modules based on whether the app is running online or offline.)

<samp class="function">RemoteDataStore</samp>’s methods will communicate asynchronously with the server by sending a network request in the background. When the browser receives the response from the server, it has an opportunity to invoke a callback.

Each of <samp class="function">RemoteDataStore</samp>’s methods will accept a function argument that will be invoked after the response arrives with any data from the server.

Create a new <samp class="filename">scripts/remotedatastore.js</samp> file and add a `<script>` tag for it in <samp class="filename">index.html</samp>.

```
...
    <script src="scripts/validation.js" charset="utf-8"></script>
    <script src="scripts/checklist.js" charset="utf-8"></script>
    <script src="scripts/formhandler.js" charset="utf-8"></script>
    <script src="scripts/remotedatastore.js" charset="utf-8"></script>
    <script src="scripts/datastore.js" charset="utf-8"></script>
    <script src="scripts/truck.js" charset="utf-8"></script>
    <script src="scripts/main.js" charset="utf-8"></script>
  </body>
</html>
```

Save <samp class="filename">index.html</samp>. In <samp class="filename">remotedatastore.js</samp>, import the `App` namespace and jQuery, then create an IIFE module with a constructor named <samp class="function">RemoteDataStore</samp>. The constructor should accept an argument for a remote server URL and throw an error if a URL is not passed in. At the end of the module definition, export the <samp class="function">RemoteDataStore</samp> to the `App` namespace:

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var $ = window.jQuery;

  function RemoteDataStore(url) {
    if (!url) {
      throw new Error('No remote URL supplied.');
    }

    this.serverUrl = url;
  }

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;

})(window);
```

## Sending Data to the Server

The first method you will create is the <samp class="methodname">add</samp> method to store customer order data on the remote web service.

Add a prototype method to <samp class="function">RemoteDataStore</samp>. Like <samp class="function">DataStore</samp>’s <samp class="methodname">add</samp> method, it will accept arguments called `key` and `val`. Note that it is not required for you to use the same parameter names, but it is good practice to keep them consistent.

```
...
  function RemoteDataStore(url) {
    ...
  }

  RemoteDataStore.prototype.add = function (key, val) {
    // Code will go here
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

### Using jQuery’s $.post method

Inside the <samp class="function">RemoteDataStore</samp> module, you will use jQuery’s <samp class="methodname">$.post</samp> method. This method sends a `POST` request in the background as an `XMLHttpRequest` object ([Figure 13.3](#ch13s04.html_fig-remotedatastore-jquery "Figure 13.3  RemoteDataStore uses jQuery for Ajax")).

**Figure 13.3  `RemoteDataStore` uses jQuery for Ajax**

![RemoteDataStore uses jQuery for Ajax](CoffeeRun/Ajax-Callbacks/img/remotedatastore-jquery.png)

The <samp class="methodname">$.post</samp> method only requires two pieces of information: the URL of the server to send the request to and what data to include.

In <samp class="filename">remotedatastore.js</samp>, update the body of the <samp class="methodname">add</samp> method so that it calls <samp class="methodname">$.post</samp>, passing it `this.serverUrl` and the `val`.

```
...
  RemoteDataStore.prototype.add = function (key, val) {
  // Code will go here
    $.post(this.serverUrl, val);
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

Notice that the `key` argument is not used. It is kept as part of the method declaration so that the <samp class="methodname">add</samp> method of <samp class="function">RemoteDataStore</samp> is identical to the <samp class="methodname">add</samp> method of <samp class="function">DataStore</samp>. Both take the coffee order information as the second argument. For the <samp class="function">RemoteDataStore</samp>, this is the crucial part.

### Adding a callback

Like many jQuery methods, <samp class="methodname">$.post</samp> can accept additional, optional arguments. You are going to pass it a callback function as a third argument. When the response arrives from the server, this function will be called and the data in the response will be passed to it.

This is similar to the event handling code you have written – you register a function to run at some point in the future. When handling events, this point is something like a mouse click or a form submission. When handling remote data, it is the the arrival of a response from the server.

Add an anonymous function as the third argument to <samp class="methodname">$.post</samp>. This anonymous function should expect an argument, which you will label `serverResponse`. Print this `serverResponse` to the console using <samp class="methodname">console.log</samp>.

```
...
  RemoteDataStore.prototype.add = function (key, val) {
    $.post(this.serverUrl, val, function (serverResponse) {
      console.log(serverResponse);
    });
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

Now <samp class="methodname">$.post</samp> knows three things: who to talk to, what to say, and what to do with the information it gets back in the response.

After you save these changes to <samp class="filename">remotedatastore.js</samp>, start `browser-sync` and open the console in your browser. Instantiate a <samp class="function">RemoteDataStore</samp> object with the URL shown below, which is the address of the test server created for this book. (Once again, this line is broken in order to fit on the page; enter it on one line.)

```
var remoteDS = new App.RemoteDataStore
    ("http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders");
```

Now invoke its <samp class="methodname">add</samp> method, passing it some test data:

```
remoteDS.add('a@b.com', {emailAddress: 'a@b.com', coffee: 'espresso'});
```

In the console, look at what was printed from your <samp class="methodname">console.log</samp> statement ([Figure 13.4](#ch13s04.html_fig-result-of-rds-add "Figure 13.4  Console showing result of calling RemoteDataStore.add")).

**Figure 13.4  Console showing result of calling `RemoteDataStore.add`**

![Console showing result of calling RemoteDataStore.add](CoffeeRun/Ajax-Callbacks/img/result-of-rds-add.png)

The object in the console’s log statement contains some information sent back by the server in its response: the `coffee` and `emailAddress` information, in addition to some bookkeeping data that will vary from server to server.

### Inspecting the Ajax request and response

In the DevTools, open the network panel by clicking <samp class="guimenuitem">Network</samp> in the menu at the top (between <samp class="guimenuitem">Sources</samp> and <samp class="guimenuitem">Timeline</samp>). This panel shows a list of requests that your browser has made and lets you inspect each of them for more information ([Figure 13.5](#ch13s04.html_fig-network-panel "Figure 13.5  Viewing Ajax requests in the network panel")).

**Figure 13.5  Viewing Ajax requests in the network panel**

![Viewing Ajax requests in the network panel](CoffeeRun/Ajax-Callbacks/img/network-panel.png)

Your network panel will likely have many network requests in the list. Clear it out by clicking the ![Viewing Ajax requests in the network panel](CoffeeRun/Ajax-Callbacks/img/clear-network.png) icon near the upper left of the DevTools. Then activate the console drawer at the bottom so you can see the console as well as the network panel. You can do this by pressing the Escape key on your keyboard or by clicking the ![Viewing Ajax requests in the network panel](CoffeeRun/Ajax-Callbacks/img/dots.png) icon in the upper right. This will open a menu with the option <samp class="guilabel">Show console</samp>.

The console drawer will appear at the bottom of the DevTools ([Figure 13.6](#ch13s04.html_fig-console-drawer "Figure 13.6  Console drawer open below the network panel")).

**Figure 13.6  Console drawer open below the network panel**

![Console drawer open below the network panel](CoffeeRun/Ajax-Callbacks/img/console-drawer.png)

In the console, enter the following:

```
var remoteDS = new App.RemoteDataStore
    ("http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders");
remoteDS.add('a@b.com', {emailAddress: 'a@b.com', coffee: 'espresso'});
```

You will see a new entry in the network panel ([Figure 13.7](#ch13s04.html_fig-ajax-request-network-panel "Figure 13.7  Ajax request in network panel")).

**Figure 13.7  Ajax request in network panel**

![Ajax request in network panel](CoffeeRun/Ajax-Callbacks/img/ajax-request-network-panel.png)

To find out more about the request, click on its entry ([Figure 13.8](#ch13s04.html_fig-ajax-headers-form-data "Figure 13.8  Request details")). You may find it easier to view the details if you hide the console drawer.

**Figure 13.8  Request details**

![Request details](CoffeeRun/Ajax-Callbacks/img/ajax-headers-form-data.png)

The details include some general information about the request at the top and the form data at the bottom. In the middle are panes that show the request and response <samp class="firstterm">headers</samp>. Headers are metadata and options that have been specified for the request and response.

Of all this data, the status code (in the <samp class="guilabel">General</samp> pane) and the <samp class="guilabel">Form Data</samp> pane are usually the most useful while developing and debugging Ajax requests.

## Retrieving Data from the Server

Your <samp class="function">RemoteDataStore</samp> module can save individual coffee orders to the server. The next thing to do is add a <samp class="methodname">getAll</samp> prototype method so that it can retrieve all orders from the server. Get it started in <samp class="filename">remotedatastore.js</samp>:

```
...
  RemoteDataStore.prototype.add = function (key, val) {
    ...
  };

  RemoteDataStore.prototype.getAll = function () {
    // Code will go here
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

Next you will add a call to jQuery’s <samp class="methodname">$.get</samp> method. Like <samp class="methodname">$.post</samp>, you will pass it the server URL. But you will not pass it any data, because you are retrieving information instead of saving information. You will need to pass it a function argument so that it knows what to do with the data when it comes back from the server.

Call <samp class="methodname">$.get</samp> in <samp class="methodname">RemoteDataStore.prototype.getAll</samp>.

```
...
  RemoteDataStore.prototype.getAll = function () {
    // Code will go here
    $.get(this.serverUrl, function (serverResponse) {
      console.log(serverResponse);
    });
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

Save and return to the DevTools in the browser.

### Inspecting the response data

In the console, instantiate a <samp class="function">RemoteDataStore</samp> with the same URL as before. (Pro tip: Instead of re-typing the very long line with the URL, you can use the up and down arrow keys to cycle through statements you have entered into the console.) Then call its <samp class="methodname">getAll</samp> method:

```
var remoteDS = new App.RemoteDataStore
    ("http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders");
remoteDS.getAll();
```

In the network panel of the DevTools, you will see that the `GET` request went out. It should return within a few dozen milliseconds. Some coffee order info (from data preloaded on the server) will appear in the console ([Figure 13.9](#ch13s05.html_fig-inspecting-get-all "Figure 13.9  Inspecting the response from getAll")).

**Figure 13.9  Inspecting the response from `getAll`**

![Inspecting the response from getAll](CoffeeRun/Ajax-Callbacks/img/inspecting-get-all.png)

You may see slightly different results, depending on what has been added to the server. However, getting any result shows that you are successfully retrieving data from the server.

### Adding a callback argument

You can retrieve the data from the server, but you cannot return it from <samp class="methodname">getAll</samp>. This is because <samp class="methodname">getAll</samp> only makes the initial Ajax request; it does not handle the response.

Instead, you pass a response handling callback to <samp class="methodname">$.get</samp>. Your response handling callback will work like the event handling callbacks you have written – in both cases, the callback should expect to receive an argument. This means that the response data is only available inside the body of the callback. How will you access it outside of that callback?

If you pass <samp class="methodname">getAll</samp> a function argument, you can call that function <samp class="emphasis">inside</samp> the <samp class="methodname">$.get</samp> callback. There, you have access to both the function argument <samp class="emphasis">and</samp> the server response.

Add the function argument and call in <samp class="filename">remotedatastore.js</samp>:

```
...
  RemoteDataStore.prototype.getAll = function (cb) {
    $.get(this.serverUrl, function (serverResponse) {
      console.log(serverResponse);
      cb(serverResponse);
    });
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

The <samp class="methodname">getAll</samp> method retrieves all the coffee orders on the remote server and passes them to the callback <samp class="function">cb</samp> function that is passed in.

You also need to implement the <samp class="methodname">get</samp> method, which retrieves a single coffee order by the customer email address. Like <samp class="methodname">getAll</samp>, it will accept a function argument, which it will call and pass the retrieved coffee order.

Add this implementation of <samp class="methodname">get</samp> to <samp class="filename">remotedatastore.js</samp>:

```
...
  RemoteDataStore.prototype.getAll = function (cb) {
    ...
  };

  RemoteDataStore.prototype.get = function (key, cb) {
    $.get(this.serverUrl + '/' + key, function (serverResponse) {
      console.log(serverResponse);
      cb(serverResponse);
    });
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

Save your changes to <samp class="filename">remotedatastore.js</samp>. Enter the following code in the console, passing an empty anonymous function to <samp class="methodname">remoteDS.get</samp>. (It is expecting a function argument, but you only want to take it for a quick test.)

```
var remoteDS = new App.RemoteDataStore
    ("http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders");
remoteDS.get('a@b.com', function () {});
```

Your console will look something like [Figure 13.10](#ch13s05.html_fig-testing-get "Figure 13.10  Testing RemoteDataStore.prototype.get").

**Figure 13.10  Testing `RemoteDataStore.prototype.get`**

![Testing RemoteDataStore.prototype.get](CoffeeRun/Ajax-Callbacks/img/testing-get.png)

## Deleting Data from the Server

Using Ajax, you can now save orders to the server and retrieve orders from the server. The last thing to do is to delete orders from the server when they are delivered.

To do this, you will send an HTTP request to the URL for an individual order. As you did with <samp class="methodname">RemoteDataStore.prototype.get</samp>, you will use the server URL, but you will append a slash and the customer’s email address.

You will be sending the server a `DELETE` request. `DELETE` is one of the HTTP verbs. The server knows to remove the data associated with that customer’s email address if it receives a `DELETE` request at that URL.

### Using jQuery’s $.ajax method

jQuery provides the <samp class="methodname">$.get</samp> and <samp class="methodname">$.post</samp> methods as a convenience because these are the two most common HTTP verbs used. For example, a `GET` request is used whenever the browser asks for an HTML, CSS, JavaScript, or image file (among others). A `POST` request is used most often when a form is submitted.

jQuery does not provide a convenience method for sending `DELETE` requests via Ajax. Instead, you will need to use the <samp class="methodname">$.ajax</samp> method. (<samp class="methodname">$.get</samp> and <samp class="methodname">$.post</samp> actually call <samp class="methodname">$.ajax</samp> for you, specifying `GET` and `POST` as the HTTP verbs.)

In <samp class="filename">remotedatastore.js</samp>, add the <samp class="methodname">remove</samp> prototype method. In it, call the <samp class="methodname">$.ajax</samp> method, passing it two arguments. The first argument is an individual coffee order’s URL, made up of the server URL, a slash, and the <samp class="varname">key</samp> (the customer’s email address). The second argument is an object that contains the options, or settings, for the Ajax request. The only option you need to specify for the <samp class="methodname">remove</samp> method is that the `type` is <samp class="literal">DELETE</samp>.

```
...
  RemoteDataStore.prototype.get = function (key, cb) {
    ...
  };

  RemoteDataStore.prototype.remove = function (key) {
    $.ajax(this.serverUrl + '/' + key, {
      type: 'DELETE'
    });
  };

  App.RemoteDataStore = RemoteDataStore;
  window.App = App;
...
```

(There are many options available for Ajax requests, which you can read about at [<samp class="uri">api.jquery.com/​jquery.ajax</samp>](http://api.jquery.com/jquery.ajax/).)

Save and return to the console. Instantiate a new <samp class="function">RemoteDataStore</samp> and invoke the <samp class="methodname">remove</samp> method. Pass it the email address for the test orders you have created. Finally, call <samp class="methodname">getAll</samp> to confirm that it is no longer included in the orders returned from the server.

```
var remoteDS = new App.RemoteDataStore
    ("http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders");
remoteDS.remove('a@b.com');
remoteDS.getAll();
```

If you inspect the response from the server for the `DELETE` request, you can see that the server sends back information about what it did ([Figure 13.11](#ch13s06.html_fig-inspect-delete "Figure 13.11  Inspecting the response from a DELETE request")). (As we mentioned earlier, other servers may provide different information in the response.)

**Figure 13.11  Inspecting the response from a `DELETE` request**

![Inspecting the response from a DELETE request](CoffeeRun/Ajax-Callbacks/img/inspect-delete.png)

## Replacing DataStore with RemoteDataStore

Your <samp class="function">RemoteDataStore</samp> module is complete. It is time to replace your <samp class="function">DataStore</samp> instance with a <samp class="function">RemoteDataStore</samp> instance.

Open <samp class="filename">main.js</samp>. Begin by importing <samp class="function">RemoteDataStore</samp> from the `App` namespace.

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var CHECKLIST_SELECTOR = '[data-coffee-order="checklist"]';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var RemoteDataStore = App.RemoteDataStore;
  var FormHandler = App.FormHandler;
...
```

Also, add a new variable called <samp class="varname">SERVER_URL</samp> and assign it a string with the URL of the CoffeeRun test server.

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var CHECKLIST_SELECTOR = '[data-coffee-order="checklist"]';
  var SERVER_URL = 'http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders';
  var App = window.App;
  var Truck = App.Truck;
  var DataStore = App.DataStore;
  var RemoteDataStore = App.RemoteDataStore;
...
```

Next, create a new instance of <samp class="function">RemoteDataStore</samp>, passing it <samp class="varname">SERVER_URL</samp>.

```
...
  var RemoteDataStore = App.RemoteDataStore;
  var FormHandler = App.FormHandler;
  var Validation = App.Validation;
  var CheckList = App.CheckList;
  var remoteDS = new RemoteDataStore(SERVER_URL);
  var webshim = window.webshim;
  var myTruck = new Truck('ncc-1701', new DataStore());
  window.myTruck = myTruck;
...
```

Finally, instead of passing the <samp class="function">Truck</samp> constructor a new instance of <samp class="function">DataStore</samp>, pass it <samp class="varname">remoteDS</samp>. Because <samp class="function">DataStore</samp> and <samp class="function">RemoteDataStore</samp> have methods with the same names and take (mostly) the same arguments, this change will work seamlessly.

```
...
  var RemoteDataStore = App.RemoteDataStore;
  var FormHandler = App.FormHandler;
  var Validation = App.Validation;
  var CheckList = App.CheckList;
  var remoteDS = new RemoteDataStore(SERVER_URL);
  var webshim = window.webshim;
  var myTruck = new Truck('ncc-1701', new DataStore()); remoteDS);
  window.myTruck = myTruck;
...
```

Save your changes and go back to the browser. Enter some coffee order information and submit the form. Keep the network panel open while you do so. You should see network transactions for every coffee order you add through the form or deliver via the checklist ([Figure 13.12](#ch13s07.html_fig-coffee-orders-over-network "Figure 13.12  Saving coffee orders to the remote server")).

**Figure 13.12  Saving coffee orders to the remote server**

![Saving coffee orders to the remote server](CoffeeRun/Ajax-Callbacks/img/coffee-orders-over-network.png)

Congratulations! CoffeeRun is fully functional and is integrated with a remote web service.

The next chapter is the final one for CoffeeRun. It does not add any new features. Instead, it focuses on refactoring your existing code so you can learn a new pattern for working with asynchronous code.

## Silver Challenge: Validating Against the Remote Server

Your validation code currently does a simple domain check. Update your validation code so that it also checks whether an email address has already been used for an order that exists on the server. Prevent the form from being submitted if that address has been used and provide an appropriate validation warning.

You may want to open a second browser window for CoffeeRun and enter different coffee orders in the two windows.

Pay attention to how often a request is sent to the server when doing this validation check. (You can see these in the DevTools network panel.) Can you find a good way to minimize the number of requests?

## For the More Curious: Postman

One of the best tools for sending test requests to a server is <samp class="application">Postman</samp>, a free plug-in for <samp class="application">Chrome</samp>. It lets you build HTTP requests and specify the HTTP verbs, form data, headers, and user credentials ([Figure 13.13](#ch13s09.html_fig-postman-app "Figure 13.13  The Postman")).

**Figure 13.13  The Postman**

![The Postman](CoffeeRun/Ajax-Callbacks/img/postman-app.png)

<samp class="application">Postman</samp> is an indispensable tool for exploring an API before you write your server communication code. Download it from the <samp class="application">Chrome</samp> web store, [<samp class="uri">chrome.google.com/​webstore</samp>](https://chrome.google.com/webstore/). (Search for “Postman” to find it.)

# <samp class="chapter_number">14</samp>
<samp class="chapter_name">Deferreds and Promises</samp>

In CoffeeRun, your modular code has helped you avoid the dreaded “spaghetti code” that can easily happen when you mix event-handling (UI) code with your application’s internal logic.

Your modules interact via function arguments, also known as callbacks. Callbacks are a fine solution for situations in which you have code that only depends on a single, asynchronous step. [Figure 14.1](#ch14.html_fig-promise-flow "Figure 14.1  Asynchronous flow for adding a coffee order") shows a simplified version of one asynchronous flow from CoffeeRun.

**Figure 14.1  Asynchronous flow for adding a coffee order**

![Asynchronous flow for adding a coffee order](CoffeeRun/Ajax-Promises/img/promise-flow.png)

What happens when you have many dependent asynchronous steps? One option is to nest lots of callbacks, but this quickly becomes unwieldy and dangerous. With a simplified version of your submit handler code that does extra error checking, that approach might look like this:

```
formHandler.addSubmitHandler(function (data) {
  try {
    myTruck.createOrder(function (error) {
      if (error) {
        throw new Exception(error)
      } else {
        try {
          saveOnServer(function (error) {
            if (error) {
              throw new Exception({message: 'server error'});
            } else {
              try {
                checkList.addRow();
              } catch (e2) {
                handleDomError(e2);
              }
            }
          })
        } catch (e) {
          handleServerError(e, function () {
            // Try adding the row again
            try {
              checkList.addRow();
            } catch (e3) {
              handleDomError(e3);
            }
          });
        }
      }
    });
  } catch (e) {
    alert('Something bad happened.');
  }
});
```

`Promise`s, which you will learn about in this chapter, are a better solution. That same series of steps might be expressed as a <samp class="firstterm">chain</samp> of `Promise`s like this:

```
formHandler.addSubmitHandler()
  .then(myTruck.createOrder)
  .then(saveOnServer)
  .catch(handleServerError)
  .then(checkList.addRow)
  .catch(handleDomError);
```

`Promise`s provide a way to architect very complex asynchronous code in a manageable way, and in this chapter you will use them to simplify the architecture of CoffeeRun. `Promise`s are a relatively new feature, but they are well supported in recent browsers, including <samp class="application">Chrome</samp>.

In CoffeeRun, you are mainly interested in performing the next step if the current one succeeds without errors. `Promise`s make this simple. Instead of relying on callback arguments, you will return `Promise` objects, which will let you decouple your modules even further.

## Promises and Deferreds

`Promise` objects are always in one of three states: <samp class="firstterm">pending</samp>, <samp class="firstterm">fulfilled</samp>, or <samp class="firstterm">rejected</samp> ([Figure 14.2](#ch14.html_fig-promise-states "Figure 14.2  Three states of a Promise object")).

**Figure 14.2  Three states of a `Promise` object**

![Three states of a Promise object](CoffeeRun/Ajax-Promises/img/promise-states.png)

Every `Promise` object has a <samp class="methodname">then</samp> method that is triggered when the `Promise` becomes fulfilled. You can call <samp class="methodname">then</samp> and pass it a callback; when the `Promise` is fulfilled, the callback is invoked and passed whatever value the `Promise` received when doing its asynchronous work.

You can also chain multiple <samp class="methodname">then</samp> calls together. Instead of writing functions that accept and then invoke callbacks, it is better to return `Promise` objects and let the caller chain a <samp class="methodname">then</samp> off of that `Promise`.

You are going to start with jQuery’s `Deferred` object, which works similarly to a `Promise` for simple use cases.

jQuery’s <samp class="methodname">$.ajax</samp> methods (including <samp class="methodname">$.post</samp> and <samp class="methodname">$.get)</samp> return a `Deferred`. `Deferred` objects have methods that let you register callbacks for two of their states: <samp class="firstterm">fulfilled</samp> and <samp class="firstterm">rejected</samp>. You are going to start by updating <samp class="function">RemoteDataStore</samp> so that it returns the `Deferred`s produced by jQuery’s Ajax methods. Later, you will modify your other modules to register callbacks with the `Deferred`s.

## Returning Deferred

Take advantage of the `Deferred` objects returned by jQuery’s <samp class="methodname">$.ajax</samp> methods. In <samp class="filename">remotedatastore.js</samp>, update the prototype methods so that they return the result of calling <samp class="methodname">$.get</samp>, <samp class="methodname">$.post</samp>, and <samp class="methodname">$.ajax</samp>.

```
...
  RemoteDataStore.prototype.add = function (key, val) {
    return $.post(this.serverUrl, val, function (serverResponse) {
      console.log(serverResponse);
    });
  };

  RemoteDataStore.prototype.getAll = function (cb) {
    return $.get(this.serverUrl, function (serverResponse) {
      console.log(serverResponse);
      cb(serverResponse);
    });
  };

  RemoteDataStore.prototype.get = function (key, cb) {
    return $.get(this.serverUrl + '/' + key, function (serverResponse) {
      console.log(serverResponse);
      cb(serverResponse);
    });
  };

  RemoteDataStore.prototype.remove = function (key) {
    return $.ajax(this.serverUrl + '/' + key, {
      type: 'DELETE'
    });
  };
...
```

Because they now return the <samp class="function">Deferred</samp> produced by jQuery’s Ajax methods, it is not absolutely necessary for <samp class="methodname">get</samp> and <samp class="methodname">getAll</samp> to accept callbacks. To account for the possibility of no callback, add an `if` statement to check that <samp class="varname">cb</samp> was passed in before invoking it.

```
...
  RemoteDataStore.prototype.getAll = function (cb) {
    return $.get(this.serverUrl, function (serverResponse) {
      if (cb) {
        console.log(serverResponse);
        cb(serverResponse);
      }
    });
  };

  RemoteDataStore.prototype.get = function (key, cb) {
    return $.get(this.serverUrl + '/' + key, function (serverResponse) {
      if (cb) {
        console.log(serverResponse);
        cb(serverResponse);
      }
    });
  };
...
```

Save <samp class="filename">remotedatastore.js</samp>. Since the <samp class="function">RemoteDataStore</samp> methods return `Deferred`s, you will need to update the <samp class="function">Truck</samp> methods to do the same. For now, you will focus on <samp class="methodname">createOrder</samp> and <samp class="methodname">deliverOrder</samp>.

Open <samp class="filename">truck.js</samp> and add a `return` to these two methods where you call them on `this.db`.

```
...
  Truck.prototype.createOrder = function (order) {
    console.log('Adding order for ' + order.emailAddress);
    return this.db.add(order.emailAddress, order);
  };

  Truck.prototype.deliverOrder = function (customerId) {
    console.log('Delivering order for ' + customerId);
    return this.db.remove(customerId);
  };
...
```

Save <samp class="filename">truck.js</samp>. <samp class="function">Truck</samp> now returns the `Deferred`s that <samp class="function">RemoteDataStore</samp> produces. When using `Promise`s and `Deferred`s, it is a best practice to return them from your functions. Returning them lets any object that calls <samp class="methodname">createOrder</samp> or <samp class="methodname">deliverOrder</samp> register callbacks that are triggered when the asynchronous work is finished.

In the next section, you will do just that.

## Registering Callbacks with then

<samp class="methodname">$.ajax</samp> returns a `Deferred`, which has a <samp class="methodname">then</samp> method. The <samp class="methodname">then</samp> method registers a callback that is run when the `Deferred` is resolved. When the callback is invoked, it is passed the value sent back in the server response ([Figure 14.3](#ch14s03.html_fig-promise-rainbow "Figure 14.3  Deferred object invokes callbacks registered with then")).

**Figure 14.3  Deferred object invokes callbacks registered with `then`**

![Deferred object invokes callbacks registered with then](CoffeeRun/Ajax-Promises/img/promise-rainbow.png)

Start with a simple usage of <samp class="methodname">then</samp>. In <samp class="filename">main.js</samp>, your submit handler calls <samp class="methodname">createOrder</samp> and <samp class="methodname">addRow</samp>. Change this so that <samp class="methodname">addRow</samp> is registered as a callback of <samp class="methodname">createOrder</samp>.

Open <samp class="filename">main.js</samp> and update the call to <samp class="methodname">formHandler.addSubmitHandler</samp>. Chain a <samp class="methodname">.then</samp> to the invocation of <samp class="methodname">createOrder</samp>. Pass it a callback that runs <samp class="methodname">checkList.addRow</samp>.

```
...
  formHandler.addSubmitHandler(function (data) {
    myTruck.createOrder.call(myTruck, data);
      .then(function () {
        checkList.addRow.call(checkList, data);
      });
  });
...
```

Instead of invoking <samp class="methodname">addRow</samp> immediately after <samp class="methodname">createOrder</samp>, you are making <samp class="methodname">addRow</samp> dependent on <samp class="methodname">createOrder</samp> completing without errors or exceptions.

## Handling Failures with then

<samp class="methodname">then</samp> accepts a second argument, which is invoked when the `Deferred` shifts to the rejected state. To see this in action, add a second function argument (making sure to add a comma between the two function arguments) to <samp class="methodname">formHandler.addSubmitHandler</samp> in <samp class="filename">main.js</samp>. Inside of this function, show an alert with a simple error message.

```
...
  formHandler.addSubmitHandler(function (data) {
    myTruck.createOrder.call(myTruck, data)
      .then(function () {
        checkList.addRow.call(checkList, data);
      },
      function () {
        alert('Server unreachable. Try again later.');
      }
      );
  });
...
```

At the top of <samp class="filename">main.js</samp>, misspell the server name so that Ajax requests fail. (This change will only be temporary, so you may want to simply cut a section out of the URL that you can paste back in later.)

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var CHECKLIST_SELECTOR = '[data-coffee-order="checklist"]';
  var SERVER_URL = 'http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders/';
  var App = window.App;
...
```

Save your changes, make sure `browser-sync` is running, and open CoffeeRun in the browser. Fill out the form. You should see an alert pop up when you submit it ([Figure 14.4](#ch14s04.html_fig-oh-no "Figure 14.4  Alert shown when Ajax call fails")).

**Figure 14.4  Alert shown when Ajax call fails**

![Alert shown when Ajax call fails](CoffeeRun/Ajax-Promises/img/oh-no.png)

Restore the <samp class="varname">SERVER_URL</samp> to <samp class="literal">http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders/</samp>. You can also delete the function argument that shows the <samp class="function">alert</samp>.

```
(function (window) {
  'use strict';
  var FORM_SELECTOR = '[data-coffee-order="form"]';
  var CHECKLIST_SELECTOR = '[data-coffee-order="checklist"]';
  var SERVER_URL = 'http://coffeerun-v2-rest-api.herokuapp.com/api/coffeeorders/';

  ...

  formHandler.addSubmitHandler(function (data) {
    myTruck.createOrder.call(myTruck, data)
      .then(function () {
        checkList.addRow.call(checkList, data);
      },
      function () {
        alert('Server unreachable. Try again later.');
      }
      );
  });
...
```

Using <samp class="methodname">then</samp> to register callbacks maps onto the way `Promise`s work. If the `Promise` changes state to fulfilled, one set of callbacks is run. If the `Promise` changes state to rejected, the other set of callbacks is run.

## Using Deferreds with Callback-Only APIs

Sometimes you will need to coordinate your `Deferred`-based code with callback-only APIs, such as event listeners.

Currently, <samp class="methodname">formHandler.addSubmitHandler</samp> resets the form and focuses on the first element – no matter what happens with the Ajax request. However, you only want those things to happen if the Ajax request is successful. Put another way, you only want those things to happen if the `Deferred` is fulfilled.

How can you know whether the `Deferred` is fulfilled? Your function argument to <samp class="methodname">addSubmitHandler</samp> can return the `Deferred`, and inside of <samp class="methodname">addSubmitHandler</samp> you can chain a <samp class="methodname">.then</samp> call to the `Deferred`.

In <samp class="filename">main.js</samp>, add a `return` keyword to the callback.

```
...
  formHandler.addSubmitHandler(function (data) {
    return myTruck.createOrder.call(myTruck, data)
      .then(function () {
        checkList.addRow.call(checkList, data);
      });
  });
...
```

Save <samp class="filename">main.js</samp>. Next, open <samp class="filename">formhandler.js</samp>, find the <samp class="methodname">addSubmitHandler</samp> method, and locate the call to the anonymous function, <samp class="varname">fn</samp>. Because that anonymous function now returns a `Deferred`, you can chain a call to <samp class="methodname">.then</samp> on the end of it. Use <samp class="methodname">.then</samp> to register a callback that resets the form and focuses on the first element.

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    console.log('Setting submit handler for form');
    this.$formElement.on('submit', function (event) {
      event.preventDefault();

      var data = {};
      $(this).serializeArray().forEach(function (item) {
        data[item.name] = item.value;
        console.log(item.name + ' is ' + item.value);
      });
      console.log(data);
      fn(data);
      .then(function () {
        this.reset();
        this.elements[0].focus();
      });
    });
  };
...
```

Before, you had three sequential statements: invoke the callback, reset the form, and focus on the first form element. Now, you have one statement that depends on the result of the previous statement. You invoke the callback and – <samp class="emphasis">if</samp> the promised work finishes execution normally, without encountering an exception – <samp class="emphasis">then</samp> you reset the form and focus on the first form element.

There is just one concern. When you register a callback function with <samp class="methodname">.then</samp>, that callback function has a new scope. You need to <samp class="methodname">.bind</samp> that anonymous function so that the value of `this` is set to the <samp class="function">FormHandler</samp> instance.

Make this change in <samp class="filename">formhandler.js</samp>.

```
...
  FormHandler.prototype.addSubmitHandler = function (fn) {
    ...
      fn(data)
        .then(function () {
          this.reset();
          this.elements[0].focus();
        }.bind(this));
    });
  };
...
```

Save <samp class="filename">formhandler.js</samp>.

Similarly, you only want to remove an item from the checklist if the call to <samp class="methodname">Truck.prototype.deliverOrder</samp> is successful.

Chain a call to <samp class="methodname">.then</samp> off the function passed to <samp class="methodname">addClickHandler</samp> in <samp class="filename">checklist.js</samp>. Remember to <samp class="methodname">.bind</samp> the value of `this` for the anonymous function.

```
...
  CheckList.prototype.addClickHandler = function (fn) {
    this.$element.on('click', 'input', function (event) {
      var email = event.target.value;
      this.removeRow(email);
      fn(email);
        .then(function () {
          this.removeRow(email);
        }.bind(this));
    }.bind(this));
  };
...
```

Save <samp class="filename">checklist.js</samp>. Recall that you invoke <samp class="methodname">addClickHandler</samp> in <samp class="filename">main.js</samp>:

```
checkList.addClickHandler(myTruck.deliverOrder.bind(myTruck);
```

There is no need to make any changes to this method call. Because <samp class="methodname">Truck.prototype.deliverOrder</samp> is returning the `Deferred`, <samp class="methodname">addClickHandler</samp> will work as written.

All of your data is remote, which means you need to load it and draw checklist items for each coffee order. You can use the <samp class="methodname">Truck.prototype.printOrders</samp> method along with the <samp class="methodname">CheckList.prototype.addRow</samp> method to do this.

You will make two changes to <samp class="methodname">printOrders</samp>. First, you will update <samp class="methodname">printOrders</samp> to work with `Deferred`s. Then, you will add a function argument to <samp class="methodname">printOrders</samp> which it will call as it iterates through the data to print.

In <samp class="filename">truck.js</samp>, your code for <samp class="methodname">Truck.prototype.printOrders</samp> currently looks like this:

```
...
  Truck.prototype.printOrders = function () {
    var customerIdArray = Object.keys(this.db.getAll());

    console.log('Truck #' + this.truckId + ' has pending orders:');
    customerIdArray.forEach(function (id) {
      console.log(this.db.get(id));
    }.bind(this));
  };
...
```

Update this implementation to call and return <samp class="methodname">this.db.getAll</samp>, chaining a <samp class="methodname">.then</samp> to it. Pass an anonymous function to <samp class="methodname">.then</samp> and set its `this` keyword using <samp class="methodname">.bind</samp>:

```
...
  Truck.prototype.printOrders = function () {
    return this.db.getAll()
      .then(function (orders) {
        var customerIdArray = Object.keys(this.db.getAll());

        console.log('Truck #' + this.truckId + ' has pending orders:');
        customerIdArray.forEach(function (id) {
          console.log(this.db.get(id));
        }.bind(this));
      }.bind(this));
  };
...
```

Your anonymous function expects to receive an object containing all of the coffee order data retrieved from the server. Extract the keys from that object and assign them to the variable named `customerIdArray`.

```
...
  Truck.prototype.printOrders = function () {
    return this.db.getAll()
      .then(function (orders) {
        var customerIdArray = Object.keys(this.db.getAll()); orders);

        console.log('Truck #' + this.truckId + ' has pending orders:');
        customerIdArray.forEach(function (id) {
          console.log(this.db.get(id));
        }.bind(this));
      }.bind(this));
  };
...
```

Likewise, change the <samp class="methodname">console.log</samp> statement so that it does not call `this.db.get(id)`. It should use the `allData` object, which already has all of the coffee orders. You should not make an extra Ajax call for each item that needs to be printed.

```
...
  Truck.prototype.printOrders = function () {
    return this.db.getAll()
      .then(function (orders) {
        var customerIdArray = Object.keys(orders);

        console.log('Truck #' + this.truckId + ' has pending orders:');
        customerIdArray.forEach(function (id) {
          console.log(this.db.get(id)); orders[id]);
        }.bind(this));
      }.bind(this));
  };
...
```

<samp class="methodname">printOrders</samp> should take an optional function argument. You need to check whether it was passed in and, if it was, invoke it. When you invoke it, you will pass it the current coffee order `allData[id]`.

```
...
  Truck.prototype.printOrders = function (printFn) {
    return this.db.getAll()
      .then(function (orders) {
        var customerIdArray = Object.keys(orders);

        console.log('Truck #' + this.truckId + ' has pending orders:');
        customerIdArray.forEach(function (id) {
          console.log(orders[id]);
          if (printFn) {
            printFn(orders[id]);
          }
        }.bind(this));
      }.bind(this));
  };
...
```

Save <samp class="filename">truck.js</samp>. In <samp class="filename">main.js</samp>, invoke <samp class="methodname">printOrders</samp> and pass it <samp class="methodname">checkList.addRow</samp>. Make sure that <samp class="methodname">addRow</samp> is bound to the <samp class="function">CheckList</samp> instance.

```
...
  formHandler.addInputHandler(Validation.isCompanyEmail);

  myTruck.printOrders(checkList.addRow.bind(checkList));

  webshim.polyfill('forms forms-ext');
  webshim.setOptions('forms', { addValidators: true, lazyCustomMessages: true });

})(window);
```

Save and return to the browser. CoffeeRun should show the existing coffee orders in the checklist. Manually reload to confirm that the checklist is repopulated each time. Inspect the network panel and see that Ajax requests are taking place ([Figure 14.5](#ch14s05.html_fig-loading-orders-on-page-load "Figure 14.5  Drawing orders on page load")).

**Figure 14.5  Drawing orders on page load**

![Drawing orders on page load](CoffeeRun/Ajax-Promises/img/loading-orders-on-page-load.png)

## Giving DataStore a Promise

By returning <samp class="function">Deferred</samp>s from <samp class="function">RemoteDataStore</samp>’s methods, you have a flexible way to use the data sent back from the server.

But you may have noticed that <samp class="function">RemoteDataStore</samp>’s methods now stray far away from how <samp class="function">DataStore</samp>’s methods work. If you were to swap a regular <samp class="function">DataStore</samp> back in, you would see that it no longer works with your application ([Figure 14.6](#ch14s06.html_fig-no-worky "Figure 14.6  Uh oh. DataStore is no longer compatible")).

**Figure 14.6  Uh oh. DataStore is no longer compatible**

![Uh oh. DataStore is no longer compatible](CoffeeRun/Ajax-Promises/img/no-worky.png)

In [Figure 14.6](#ch14s06.html_fig-no-worky "Figure 14.6  Uh oh. DataStore is no longer compatible"), you can see that instantiating a <samp class="function">Truck</samp> with a regular <samp class="function">DataStore</samp> throws errors and fails to work correctly with the UI. CoffeeRun expects a `Promise`-based <samp class="function">DataStore</samp> in order to function correctly.

To remedy this situation, you are going to change <samp class="function">DataStore</samp>’s four methods so that they return `Promise`s.

jQuery’s `Deferred` objects have treated you well. However, because <samp class="function">DataStore</samp> is not using the jQuery <samp class="methodname">$.ajax</samp> methods you have been using to access `Deferred`s, you will need to use the native <samp class="function">Promise</samp> constructor to create and return `Promise`s.

### Creating and returning Promises

In <samp class="filename">datastore.js</samp>, you are going to update the <samp class="methodname">add</samp> method. But first, create a <samp class="varname">Promise</samp> variable and assign it the value `window.Promise`. While not absolutely necessary, it is a good idea to continue this pattern of importing anything from the global scope that you will need inside of your module.

Inside the <samp class="methodname">add</samp> method, create a new variable called <samp class="varname">promise</samp>. Assign it a new instance of <samp class="function">Promise</samp>. Make sure to return the <samp class="varname">promise</samp> variable at the end of <samp class="methodname">add</samp>.

```
(function (window) {
  'use strict';
  var App = window.App || {};
  var Promise = window.Promise;

  function DataStore() {
    this.data = {};
  }

  DataStore.prototype.add = function (key, val) {
    this.data[key] = val;
    var promise = new Promise();

    return promise;
  };
...
```

The <samp class="function">Promise</samp> constructor needs a function argument. Pass it an anonymous function that accepts two function arguments, <samp class="varname">resolve</samp> and <samp class="varname">reject</samp>.

```
...
  DataStore.prototype.add = function (key, val) {
    this.data[key] = val;
    var promise = new Promise(function (resolve, reject) {
    });

    return promise;
  };
...
```

When the <samp class="function">Promise</samp> does its work, it will invoke the anonymous function argument and pass it two values: <samp class="varname">resolve</samp> and <samp class="varname">reject</samp>. The <samp class="varname">resolve</samp> function is invoked to change the state of the `Promise` object to fulfilled. The <samp class="varname">reject</samp> function is invoked to change the state of the `Promise` object to rejected.

Next, move the data storage line (`this.data[key] = val;`) down into the body of the anonymous function. To make sure that `this.data` correctly refers to the <samp class="function">DataStore</samp>’s <samp class="varname">data</samp> instance variable, <samp class="methodname">bind</samp> the anonymous function to <samp class="varname">this</samp>.

```
...
  DataStore.prototype.add = function (key, val) {
    this.data[key] = val;
    var promise = new Promise(function (resolve, reject) {
      this.data[key] = val;
    }.bind(this));

    return promise;
  };
...
```

### Resolving a Promise

At the very end of the anonymous function, invoke <samp class="varname">resolve</samp> with no argument.

```
...
  DataStore.prototype.add = function (key, val) {
    var promise = new Promise(function (resolve, reject) {
      this.data[key] = val;
      resolve(null);
    }.bind(this));

    return promise;
  };
...
```

Why use `null` as the argument? <samp class="methodname">add</samp>ing a value to the <samp class="function">DataStore</samp> does not produce a value, so there is nothing for it to <samp class="methodname">resolve</samp> to. When you need to explicitly return a non-value you should use `null`. (You could also use `resolve(val)` to give the next function in the chain access to the freshly stored value. For <samp class="function">CoffeeRun</samp>, this is not necessary, and therefore not included as part of the example.)

### Promise-ifying the other DataStore methods

You could manually update the other three methods using this same pattern of code. But instead of retyping all that code, create a helper function called <samp class="function">promiseResolvedWith</samp> to create a <samp class="function">Promise</samp>, resolve it, and return it. Update <samp class="methodname">DataStore.prototype.add</samp> to use this helper.

```
...
  function DataStore() {
    this.data = {};
  }

  function promiseResolvedWith(value) {
    var promise = new Promise(function (resolve, reject) {
      resolve(value);
    });
    return promise;
  }

  DataStore.prototype.add = function (key, val) {
    var promise = new Promise(function (resolve, reject) {
      this.data[key] = val;
      resolve(null);
    }.bind(this));

    return promise;
    return promiseResolvedWith(null);
  };
...
```

<samp class="function">promiseResolvedWith</samp> is a reusable form of the `Promise` code you wrote in the <samp class="methodname">add</samp> method. It accepts a parameter called <samp class="varname">value</samp>, creates a new variable named <samp class="varname">promise</samp>, and assigns it to a new instance of <samp class="function">Promise</samp>. It passes an anonymous function to the <samp class="function">Promise</samp> constructor that accepts two arguments: <samp class="varname">resolve</samp> and <samp class="varname">reject</samp>. Inside the anonymous function, you invoke <samp class="varname">resolve</samp> and pass it the <samp class="varname">value</samp> argument.

In <samp class="function">promiseResolvedWith</samp>, you do not need to <samp class="methodname">bind</samp> the function argument to `this`, as there are no references to <samp class="varname">this</samp> that need to be maintained.

Update the other methods to use <samp class="function">promiseResolvedWith</samp>. Pass <samp class="methodname">get</samp> and <samp class="methodname">getAll</samp> the value you were returning in the non-`Promise` version. Pass `null` to <samp class="methodname">remove</samp>.

```
...
  DataStore.prototype.get = function (key) {
    return this.data[key];
    return promiseResolvedWith(this.data[key]);
  };

  DataStore.prototype.getAll = function () {
    return this.data;
    return promiseResolvedWith(this.data);
  };

  DataStore.prototype.remove = function (key) {
    delete this.data[key];
    return promiseResolvedWith(null);
  };
...
```

Finally, update <samp class="filename">main.js</samp> to use a <samp class="function">DataStore</samp> instead of a <samp class="function">RemoteDataStore</samp>.

```
...
  var remoteDS = new RemoteDataStore(SERVER_URL);
  var webshim = window.webshim;
  var myTruck = new Truck('ncc-1701', remoteDS); new DataStore());
  window.myTruck = myTruck;
...
```

After making these changes, save your code and take CoffeeRun for another spin. You should see that it works correctly using <samp class="function">DataStore</samp>, but makes no Ajax requests ([Figure 14.7](#ch14s06.html_fig-done "Figure 14.7  CoffeeRun is done!")).

**Figure 14.7  CoffeeRun is done!**

![CoffeeRun is done!](CoffeeRun/Ajax-Promises/img/done.png)

CoffeeRun has taken you on quite a journey! Along the way, you wrote some pretty serious JavaScript using IIFEs, callbacks, and `Promise`s. You also got a taste of jQuery, which you used to manipulate DOM elements and communicate with a RESTful web service.

It is time to part ways with CoffeeRun and move on. The next app, Chattrbox, is a <samp class="firstterm">full-stack</samp> chat application. You will not only create the front-end code but also write the server. Do not worry if this is your first server application. You will still be using JavaScript, just not for the browser. Get ready to work with <samp class="application">Node.js</samp>!

## Silver Challenge: Fallback to DataStore

If you are lucky, you have a nice, stable network connection all the time. But you should be prepared in case your connection goes down while using CoffeeRun.

Update CoffeeRun so that it uses a <samp class="function">DataStore</samp> when its Ajax requests cannot reach the server.

To make sure that this is working, turn off your computer’s network connection while loading and saving coffee orders.

# <samp class="part_number">Part III</samp>
<samp class="part_name">Real-Time Data</samp>

# <samp class="chapter_number">15</samp>
<samp class="chapter_name">Introduction to Node.js</samp>

<samp class="application">Node.js</samp> is an open-source project that lets you write JavaScript that runs outside the browser.

When you write JavaScript for the browser, your code is given access to global objects like the `document` and `window`, as well as other APIs and libraries. With <samp class="application">Node</samp>, your code can access the hard drive, databases, and the network ([Figure 15.1](#ch15.html_fig-JS_in_browser_node "Figure 15.1  JavaScript running in browser vs via Node")).

**Figure 15.1  JavaScript running in browser vs via Node**

![JavaScript running in browser vs via Node](Chattrbox/Node.js/js-engines.png)

Using <samp class="application">Node</samp>, you can create anything from command-line tools to web servers. Over the next four chapters, you will use <samp class="application">Node</samp> to help create a real-time chat application called Chattrbox ([Figure 15.2](#ch15.html_fig-Chattrbox "Figure 15.2  Chattrbox: strictly for important conversations")).

**Figure 15.2  Chattrbox: strictly for important conversations**

![Chattrbox: strictly for important conversations](Chattrbox/Node.js/chattrbox-final-screenshot.png)

Chattrbox will consist of two parts: a <samp class="application">Node.js</samp> server and a JavaScript app running in the browser. The browser will connect to the <samp class="application">Node</samp> server and receive the HTML, CSS, and JavaScript files. At that point, the JavaScript app in the browser will begin handling real-time communication over WebSockets. This process is diagrammed in [Figure 15.3](#ch15.html_fig-network_diagram "Figure 15.3  Network diagram of the Chattrbox application").

**Figure 15.3  Network diagram of the Chattrbox application**

![Network diagram of the Chattrbox application](Chattrbox/Node.js/chattrbox-data-diagram.png)

You will learn about WebSockets in the next chapter. This chapter focuses on getting you familiar with <samp class="application">Node</samp>.

## Node and npm

When you installed <samp class="application">Node.js</samp> in [Chapter 1](#ch01.html "1 Setting Up Your Development Environment"), you got access to two command-line programs: `node` and the <samp class="application">Node</samp> package manager, `npm`. You may recall that `npm` allows you to install open-source development tools, like `browser-sync`. The `node` program does the work of running programs written in JavaScript.

Most of your work will be with `npm` in this chapter. The `npm` command-line tool can perform a variety of tasks, like installing third-party code that you can incorporate into your project and managing your project’s workflow and external dependencies. In this chapter, you will be using `npm` to:

*   create the <samp class="filename">package.json</samp> file, using `npm init`

*   add third-party modules, using `npm install --save`

*   run frequently used tools saved in <samp class="filename">package.json</samp>’s `scripts` section

<samp class="application">Node</samp> is much more than the <samp class="application">node</samp> and `npm` commands. It also includes a number of useful modules that provide constructors to help you do things like work with files and folders, communicate over a network, and handle events. Also, when writing JavaScript for <samp class="application">Node</samp> you will have access to utility functions that facilitate JavaScript’s interaction with the <samp class="application">Node</samp> module ecosystem. For example, <samp class="application">Node</samp> provides a much simpler module pattern than the IIFEs you used for CoffeeRun.

The <samp class="filename">package.json</samp> file mentioned above is a file that acts as your <samp class="application">Node</samp> project’s manifest. It holds your project’s name, version number, description, and other information. More important, it is where you can store configuration settings and commands for `npm` to use when testing and building your application.

You could create this file by hand, but it is much easier to let `npm` do it for you.

### npm init

Create a directory in your projects folder named <samp class="filename">chattrbox</samp>. In your terminal program, change to that directory and run `npm init` to have `npm` create <samp class="filename">package.json</samp>.

`npm` will prompt you for information about the project. It will also offer default answers, which are fine for now. Press the Return key to accept the defaults ([Figure 15.4](#ch15.html_fig-running_npm_init "Figure 15.4  Running npm init")).

**Figure 15.4  Running `npm init`**

![Running npm init](Chattrbox/Node.js/npm-init.png)

Open the <samp class="filename">chattrbox</samp> project folder in <samp class="application">Atom</samp>. You will see that the <samp class="filename">package.json</samp> file was indeed created for you ([Figure 15.5](#ch15.html_fig-package_json "Figure 15.5  package.json contents after npm init")).

**Figure 15.5  `package.json` contents after `npm init`**

![package.json contents after npm init](Chattrbox/Node.js/package-json-screenshot.png)

### npm scripts

In <samp class="filename">package.json</samp>, notice the section labeled `"scripts"`. This is for commands that you might need to run again and again while working on your project.

As you build Chattrbox, you will add to the `"scripts"` section of <samp class="filename">package.json</samp> to make your development workflow more efficient. Create your first `npm` workflow script by adding a `"start"` script (note that you must add a comma to the end of the `"test"` line):

```
...
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node index.js"
  },
...
```

This lets you start your <samp class="application">Node</samp> server by running `npm start` from the command line.

## Hello, World

To introduce you to the world of writing JavaScript outside the browser, you are going to start with a classic <samp class="application">Hello, World</samp> program. Create a new file named <samp class="filename">index.js</samp> within your <samp class="filename">chattrbox</samp> folder and type the following, which we will explain after you have entered it:

```
var http = require('http');

var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  res.end('<h1>Hello, World</h1>');
});
server.listen(3000);
```

On the first line, you used <samp class="application">Node</samp>’s built-in <samp class="function">require</samp> function to access the `http` module included with <samp class="application">Node</samp>. This module provides a number of tools for working with HTTP requests and responses, such as the <samp class="function">http.createServer</samp> function.

<samp class="function">http.createServer</samp> takes in one argument, a function. This function is called for every HTTP request. You may recognize this as the callback pattern you used with browser events – except that in this case it is a server-side event (receiving an HTTP request) that triggers the callback.

In your callback, you log a message to the console and write some HTML text to the response. In <samp class="application">Node</samp>, it is common to use <samp class="varname">req</samp> and <samp class="varname">res</samp> as the variable names for HTTP request and response objects.

Finally, you tell the server to listen on port 3000 using <samp class="function">server.listen</samp>. This is commonly referred to as “binding to a port.”

Save your files. To see your <samp class="application">Node</samp> server in action, run the command `npm start`. The terminal results are shown in [Figure 15.6](#ch15s02.html_fig-running_indexjs "Figure 15.6  Running index.js via npm start").

**Figure 15.6  Running index.js via `npm start`**

![Running index.js via npm start](Chattrbox/Node.js/chattrbox-npm-start.png)

Next, open your browser to [<samp class="uri">http://​localhost:3000</samp>](http://localhost:3000). Your results will look like [Figure 15.7](#ch15s02.html_fig-Hello_World "Figure 15.7  Accessing your Node server in a browser"). (Note that in some browsers other than <samp class="application">Chrome</samp>, you may see your HTML as plain text. These browsers are expecting either a `doctype` or an extra piece of metadata in the response declaring that the response should be interpreted as HTML. You will address this as one of the challenges at the end of the chapter.)

**Figure 15.7  Accessing your Node server in a browser**

![Accessing your Node server in a browser](Chattrbox/Node.js/chattrbox-hello-browser.png)

Unlike when you ran Ottergram and CoffeeRun, there is no JavaScript to see in the browser. By the time you see this page, your JavaScript code has already done its work on the server.

Return to your terminal. You should see that <samp class="methodname">console.log</samp> printed `Responding to a request` when the request was received ([Figure 15.8](#ch15s02.html_fig-chattrbox-first-req "Figure 15.8  console.log when request arrives")).

**Figure 15.8  `console.log` when request arrives**

![console.log when request arrives](Chattrbox/Node.js/chattrbox-first-req.png)

## Adding an npm Script

In addition to letting you write command-line JavaScript programs, <samp class="application">Node</samp> gives you a way to orchestrate your workflow as you develop these programs. It is a powerful feature that you should take advantage of. To see how this works, you will add a bit of automation to your project.

Take running your server, for example. Every time you want to try something new in your code, you have to repeat a few steps:

*   make the change to the code in your editor

*   switch to your terminal

*   press Control-C to stop the program

*   run `npm start` to start your program again

You could write a program to automate the work of restarting your service. You are in luck, though – someone has already written it for you, in a module called `nodemon`. Integrating `nodemon` into your workflow early on will make writing your program a much smoother experience.

In the terminal, stop your program and run the following command to install the `nodemon` module:

```
npm install --save-dev nodemon
```

You will see the lines below, in which `npm` is warning you about some blank fields in your <samp class="filename">package.json</samp> file. Do not be alarmed – just be aware that `npm` is a stickler for details.

```
npm WARN chattrbox@1.0.0 No description
npm WARN chattrbox@1.0.0 No repository field.
```

Notice the `--save-dev` option that you used in this `npm install` command. It tells `npm` to help you keep a list of any third-party modules your application depends on. That list is stored in your <samp class="filename">package.json</samp> file. If necessary, all of the dependencies in that list can be installed by running the <samp class="application">npm install</samp> command (with no arguments). This means that when you are sharing your code you do not need to include all of the third-party modules as well.

If you look in your <samp class="filename">package.json</samp> file, you will see that `npm` created a new `"devDependencies"` section for you, with an entry for `nodemon`.

```
...
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "nodemon": "^1.9.1"
  }
```

Now, update your <samp class="filename">package.json</samp> to add another item to the `"scripts"` section:

```
...
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "start": "node index.js",
  "dev": "nodemon index.js"
},
...
```

In the terminal, restart your <samp class="application">node</samp> program via your new `npm` script using the command `npm run dev`. Note that the command is not simply `npm dev`. This differs from `npm start` in that `npm` assumes that certain commands (like `start`) will exist. For custom `npm` scripts, you must specify that you want to `run` them.

You should see that `nodemon` is now managing your <samp class="application">node</samp> program ([Figure 15.9](#ch15s03.html_fig-npm_run_dev "Figure 15.9  Running via npm run dev")).

**Figure 15.9  Running via `npm run dev`**

![Running via npm run dev](Chattrbox/Node.js/chattrbox-npm-run-dev.png)

In <samp class="filename">index.js</samp>, change `"Hello, World"` to `"Hello, World!!"` and save the changes. `nodemon` notices and restarts your <samp class="application">node</samp> program automatically ([Figure 15.10](#ch15s03.html_fig-nodemon_restart "Figure 15.10  nodemon restarts when your code changes")).

**Figure 15.10  `nodemon` restarts when your code changes**

![nodemon restarts when your code changes](Chattrbox/Node.js/chattrbox-npm-run-dev-restart.png)

As you continue to work with <samp class="application">node</samp> and `npm` in the following chapters, you will periodically pull in a new module to help out.

## Serving from Files

Being able to write and run JavaScript on your server is nice. Most servers will want to vend out and process content living in files, too. Your next job is to make your server read files from a subfolder and send them in a response back to the browser. This is similar to what `browser-sync` was doing for you in earlier chapters.

Create a new folder named <samp class="filename">app</samp> inside of your <samp class="filename">chattrbox</samp> project folder. In it, create an <samp class="filename">index.html</samp> file with the following text:

```
Hello, File!
```

You do not need any actual HTML in this file – it only needs some content that can be read. Your project folder should look like [Figure 15.11](#ch15s04.html_fig-project_layout "Figure 15.11  Chattrbox project layout").

**Figure 15.11  Chattrbox project layout**

![Chattrbox project layout](Chattrbox/Node.js/chattrbox-folder-structure-basics.png)

### Reading a file with the fs module

In <samp class="filename">index.js</samp>, import the <samp class="application">Node.js</samp> file system module, `fs`, and call its <samp class="methodname">readFile</samp> method.

```
var http = require('http');
var fs = require('fs');

var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  res.end('<h1>Hello, World</h1>');
  fs.readFile('app/index.html', function (err, data) {
    res.end(data);
  });
});
server.listen(3000);
```

The <samp class="methodname">readFile</samp> method takes a file name and a callback. Inside your callback, you sent the contents of the file instead of the HTML text using `res.end`.

Notice that your callback accepts an `err` argument as well as the data from reading the file. This is a <samp class="application">Node.js</samp> programming convention that we will discuss later in this chapter.

`nodemon` should have restarted your program, so you can go directly to your browser and reload. In your browser, you should see exactly what you wrote in your <samp class="filename">index.html</samp> file:

```
Hello, File!
```

This is a good start, but your chat application will need to do more than serve a single HTML file. That HTML file may request other CSS or JavaScript files. To fulfill those requests, your <samp class="application">node</samp> program will need to understand what file is being requested and where to look for the requested file. You will work on that next.

### Working with the request URL

First, you need to get the URL path from the request object. If the path is just `'/'`, it is best to return the <samp class="filename">index.html</samp> file. This is a common convention from the early days of the web.

Otherwise, you should try to return the file the request object is asking for.

In <samp class="filename">index.js</samp>, update your callback to check what file the browser is requesting.

```
var http = require('http');
var fs = require('fs');

var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  var url = req.url;

  var fileName = 'index.html';
  if (url.length > 1) {
    fileName = url.substring(1);
  }
  console.log(fileName);
  fs.readFile('app/index.html', function (err, data) {
    res.end(data);
  });
});
server.listen(3000);
```

Using the request object’s `url` property, you can see whether the browser is asking for the default (<samp class="filename">index.html</samp>) or another file. If it is another file, you call <samp class="methodname">url.substring(1)</samp> to strip off the first character, which will be a `'/'`.

For now, you are just logging the filename to the console.

After `nodemon` restarts your program, try going to `http://localhost:3000/woohoo` or any other path, including the default `'/'` path. The results in your terminal will look something like [Figure 15.12](#ch15s04.html_fig-file_paths "Figure 15.12  Logging the requested file path").

**Figure 15.12  Logging the requested file path**

![Logging the requested file path](Chattrbox/Node.js/woohoo.png)

(Recall from [Chapter 2](#ch02.html "2 Setting Up Your First Project") that browsers will automatically ask for a <samp class="filename">favicon.ico</samp> file, so you may see a request for it logged to the terminal as well.)

Now it is time to make use of this path information.

### Using the path module

You could just pass the <samp class="varname">fileName</samp> to <samp class="methodname">fs.readFile</samp>, but it is better to use the `path` module, which has utilities for handling and transforming file paths. One small but important reason for using the module is that some operating systems use a forward slash and some use a backslash. The `path` module handles these differences with ease.

Update <samp class="filename">index.js</samp> to import the `path` module and use it to find the file that was requested.

```
var http = require('http');
var fs = require('fs');
var path = require('path');

var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  var url = req.url;

  var fileName = 'index.html';
  if (url.length > 1) {
    fileName = url.substring(1);
  }
  console.log(fileName);
  var filePath = path.resolve(__dirname, 'app', fileName);
  fs.readFile('app/index.html'filePath, function (err, data) {
    res.end(data);
  });
});
server.listen(3000);
```

Test a few filepaths in the browser to make sure your application still works the same. The default path should return <samp class="filename">index.html</samp>, and nonexistent paths (like `'/woohoo/'`) should show nothing and log out their filename.

Next, create a <samp class="filename">test.html</samp> file in the <samp class="filename">app</samp> folder. Write the following inside it:

```
Hola, Node!
```

Try to access it in the browser. Your <samp class="application">node</samp> program should return it without any trouble ([Figure 15.13](#ch15s04.html_fig-test_html "Figure 15.13  Retrieving test.html")).

**Figure 15.13  Retrieving `test.html`**

![Retrieving test.html](Chattrbox/Node.js/test-html.png)

You have added code that successfully serves a specific file based on the URL path. The next thing to do is abstract out that functionality into its own module.

### Creating a custom module

Your callback has (at least) two jobs. It figures out what file is being requested, and it reads that file to send back in the response. To make the code a bit more modular and maintainable, one of those responsibilities should be moved to its own module.

In CoffeeRun, you declared modules in an IIFE that assigned a value to a property of the global namespace. Modules in `Node` programs work differently. You still write your module code in a file by itself, but you do not need the IIFE.

Create a new file called <samp class="filename">extract.js</samp> in the same directory as your <samp class="filename">index.js</samp> (not in the <samp class="filename">app</samp> directory). Add a function called <samp class="function">extractFilePath</samp> that finds the appropriate file. (This code is very similar to what you already wrote in <samp class="filename">index.js</samp>.)

```
var path = require('path');

var extractFilePath = function (url) {
  var filePath;
  var fileName = 'index.html';

  if (url.length > 1) {
    fileName = url.substring(1);
  }
  console.log('The fileName is: ' + fileName);

  filePath = path.resolve(__dirname, 'app', fileName);
  return filePath;
};
```

You have taken much of the code from `index.js` and placed it in its own function, called <samp class="function">extractFilePath</samp>. Next, make the <samp class="function">extractFilePath</samp> function available so that other modules can import it with <samp class="function">require</samp>. To do this, assign <samp class="function">extractFilePath</samp> to a global variable named <samp class="varname">module.exports</samp>. This is a special variable provided by <samp class="application">Node</samp>. Whatever value is assigned to it is the value other modules are able to import. Any other variables or functions will not be visible to other modules.

```
...
  filePath = path.resolve(__dirname, 'app', fileName);
  return filePath;
};

module.exports = extractFilePath;
```

This new line tells <samp class="application">Node</samp> that when you import the `extract` module by calling `require('./extract')`, the value returned is the <samp class="function">extractFilePath</samp> function. Do that now in <samp class="filename">index.js</samp>.

### Using your custom module

Update <samp class="filename">index.js</samp> to use your new `extract` module instead of handling those responsibilities.

```
var http = require('http');
var fs = require('fs');
var path = require('path');
var extract = require('./extract');

var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  var url = req.url;

  var fileName = 'index.html';
  if (url.length > 1) {
    fileName = url.substring(1);
  }
  console.log(fileName);
  var filePath = path.resolve(__dirname, 'app', fileName);
  var filePath = extract(req.url);
  fs.readFile(filePath, function (err, data) {
    res.end(data);
  });
});
server.listen(3000);
```

You imported your custom module using the <samp class="function">require</samp> function. You assigned the value of the module to the new variable <samp class="varname">extract</samp>. Now you are able to use the <samp class="function">extract</samp> function just as you would the <samp class="function">extractFilePath</samp> function.

After `nodemon` has reloaded your code, test some URL paths and confirm that the default <samp class="filename">index.html</samp> and <samp class="filename">test.html</samp> still load. Also, make sure that nonexistent paths come up as a blank page and without an error.

## Error Handling

One last job remains. When a file cannot be found, it is better to return an error code than to silently pretend that all is well. To do that, you will need to detect when <samp class="methodname">fs.readFile</samp> returns an error instead of a file.

In JavaScript, it is common to pass callbacks to API methods. The same is true for <samp class="application">Node.js</samp>, and callbacks typically take in an error as their first argument. Because the error comes before the result, you are forced to at least see the error, whether or not you handle it.

In <samp class="filename">index.js</samp>, check for a file error and write a `404` error code if one is found:

```
var http = require('http');
var fs = require('fs');
var extract = require('./extract');

var handleError = function (err, res) {
  res.writeHead(404);
  res.end();
};

var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  var filePath = extract(req.url);
  fs.readFile(filePath, function (err, data) {
    if (err) {
      handleError(err, res);
      return;
    } else {
      res.end(data);
    }
  });
});
server.listen(3000);
```

Save your changes. After <samp class="application">nodemon</samp> restarts, go to a nonexistent path, such as `http://localhost:3000/woohoo`. Open the network panel in the DevTools, and you should see the error code, as in [Figure 15.14](#ch15s05.html_fig-woo-hoo-404 "Figure 15.14  404 Status code in the network panel").

**Figure 15.14  404 Status code in the network panel**

![404 Status code in the network panel](Chattrbox/Node.js/woo-hoo-404.png)

In your callback, the very first thing you do is check whether this <samp class="varname">err</samp> argument has a value that is not `null` or `undefined` and do something with it. In this example, you pass the error information along to the function <samp class="function">handleError</samp> and then `return` to exit the anonymous callback.

Errors should never be silently discarded. A simple `404` will do fine for now, which is what <samp class="function">handleError</samp> does.

This pattern – “errors first, return early” – is one of the best practices that is a part of the <samp class="application">Node</samp> ecosystem. All of the modules that come with <samp class="application">Node</samp> follow this pattern, as do most open-source modules.

You have built a working web server with just a few dozen lines of JavaScript, using patterns (such as callbacks) that you were already familiar with.

<samp class="application">Node</samp> provides a rich set of modules for working with networks and files, such as the `http` and `fs` modules you used in this project. Thanks to <samp class="application">Node</samp>’s `require` and `module.exports` keywords, you can modularize your own code very easily.

Over the next three chapters, you will continue to build the Chattrbox server as well as a working front end.

## For the More Curious: npm Module Registry

There are a wealth of available packages that can be installed via `npm`. You can search or browse these packages in the Module Registry, [<samp class="uri">www.npmjs.com</samp>](https://www.npmjs.com).

Make sure to look at the documentation for `npm` at [<samp class="uri">docs.npmjs.com</samp>](https://docs.npmjs.com). You might also be interested in creating your own modules for others to use. If so, see [<samp class="uri">docs.npmjs.com/​getting-started/​creating-node-modules</samp>](https://docs.npmjs.com/getting-started/creating-node-modules).

## Bronze Challenge: Creating a Custom Error Page

When you go to a path for a file that does not exist, you currently get a blank browser page and a 404 status code.

For this challenge, create a special error page to display to the user instead of returning the error as a status code.

## For the More Curious: MIME Types

Have you ever wondered how a computer knows how to open a movie file with a video player and a PDF with a document viewer? Your computer keeps a table of file types and the programs associated with those file types. It infers a file’s type by looking at the file extension (e.g., `.html` or `.pdf`).

A browser needs those same associations so that it knows whether to render the response as HTML, use a plug-in to play music, or download a file to the hard drive. But HTTP responses do not have file extensions. Instead, the server must tell the browser what type of information is in the response.

It does this by specifying the <samp class="firstterm">MIME type</samp> or <samp class="firstterm">media type</samp> in the response’s `Content-Type` header. For example, [Figure 15.15](#ch15s08.html_fig-content-type "Figure 15.15  Inspecting the Content-Type header on www.bignerdranch.com") shows what you would see in the network panel of the DevTools if you inspected the response for [<samp class="uri">www.bignerdranch.com</samp>](https://www.bignerdranch.com).

**Figure 15.15  Inspecting the Content-Type header on [`www.bignerdranch.com`](http://www.bignerdranch.com)**

![Inspecting the Content-Type header on www.bignerdranch.com](Chattrbox/Node.js/content-type.png)

The `Content-Type` header is set to `text/html` – the MIME type for HTML. You can set this header in your projects. This is what that would look like for Chattrbox:

```
...
var server = http.createServer(function (req, res) {
  console.log('Responding to a request.');
  var filePath = extract(req.url);
  fs.readFile(filePath, function (err, data) {
    if (err) {
      handleError(err, res);
      return;
    } else {
      res.setHeader('Content-Type', 'text/html');
      res.end(data);
    }
  });
});
server.listen(3000);
```

(Note that you must set the header before you end the response.)

To find out more about MIME types in general, check out [<samp class="uri">en.wikipedia.org/​wiki/​Media_type</samp>](https://en.wikipedia.org/wiki/Media_type). For more about setting headers in your <samp class="application">Node</samp> programs, go to [<samp class="uri">nodejs.org/​api/​http.html#http_response_setheader_name_value</samp>](https://nodejs.org/api/http.html#http_response_setheader_name_value).

## Silver Challenge: Providing a MIME Type Dynamically

Dynamically provide a MIME type for your responses based on the file type. To help you with this task, install the `mime` module using `npm`. Information and documentation about the `mime` module is available at [<samp class="uri">github.com/​broofa/​node-mime</samp>](https://github.com/broofa/node-mime).

Add different files to your <samp class="filename">app</samp> folder, including plain text, PDFs, audio files, and movies. Make sure that your browser is displaying each type correctly.

## Gold Challenge: Moving Error Handling to Its Own Module

Take the code that does the file reading and error handling and move it into its own module.

Also, make the module configurable so that when you import it you can specify what base folder the static HTML, CSS, and JavaScript are in.

# <samp class="chapter_number">16</samp>
<samp class="chapter_name">Real-Time Communication with WebSockets</samp>

With regular `GET` and `POST` requests, your browser has to make a new request and wait for a response for each exchange of data with the server. As you learned in earlier chapters, this is also the case with Ajax requests. While Ajax requests do not cause page reloads, they do generate just as much network traffic, with each request and response requiring a little bit of overhead to produce and process.

WebSockets, on the other hand, provides a two-way communication protocol over HTTP. It creates a single connection and keeps it open for real-time communication ([Figure 16.1](#ch16.html_fig-ajax_websockets_requests "Figure 16.1  Multiple Ajax requests vs a single WebSockets connection")).

**Figure 16.1  Multiple Ajax requests vs a single WebSockets connection**

![Multiple Ajax requests vs a single WebSockets connection](Chattrbox/WebSockets/req-resp.png)

With WebSockets, web applications can go beyond saving and loading remote data. Push notifications, collaborative document editing, and real-time chat are just the beginning. WebSockets makes it possible for servers to handle the load of the Internet of Things (e.g., smart lights, smart locks, smart cars). Traditional techniques like Ajax polling are ineffective at coordinating such intense traffic.

In this chapter, you will build a chat client and server. If you were to use Ajax to build this, you would have to juggle at least two connections – one to poll for new messages and a second to send messages. Using WebSockets, you can accomplish the same thing with a single connection.

When you reach the end of the chapter, Chattrbox will be able to handle multiple, simultaneous chat clients, sending new messages along to each client ([Figure 16.2](#ch16.html_fig-pirate-talk "Figure 16.2  Pirate chat-arr")).

**Figure 16.2  Pirate chat-arr**

![Pirate chat-arr](Chattrbox/WebSockets/pirate-talk.png)

## Setting Up WebSockets

To set Chattrbox up with WebSockets, you are going to:

1.  install the `ws` module

2.  create a WebSockets server

3.  add chat functionality to the server

4.  accommodate new users by having the server send them the message history

Begin at the beginning.

The `http` module that comes with <samp class="application">Node.js</samp> gives you a simple way to start an HTTP server so that browsers can talk to the server.

Similarly, the `ws` module gives your <samp class="application">Node.js</samp> programs an easy way to communicate via WebSockets. There are several modules that implement WebSockets for <samp class="application">Node.js</samp>, but `ws` is the standard implementation and performs well.

Begin by installing the `ws` WebSockets module in your Chattrbox directory. (Do not be alarmed if you see warnings from `npm` about a missing description or repository field for your project.)

```
npm install --save ws
```

Next, create a file in Chattrbox’s root folder named <samp class="filename">websockets-server.js</samp>. Add the following code to import the `ws` module and start listening.

```
var WebSocket = require('ws');
var WebSocketServer = WebSocket.Server;
var port = 3001;
var ws = new WebSocketServer({
    port: port
});

console.log('websockets server started');
```

You imported the `ws` module with the `require` statement. The module contains a <samp class="varname">Server</samp> property that you will need in order to create a working WebSockets server.

The code `var ws = new WebSocketServer(/*...*/);` does just that. When this runs, the WebSockets server is established and bound to the specified port (here, `3001`).

Unlike the module you created in <samp class="filename">extract.js</samp>, you will not need a `module.exports` assignment. The code in <samp class="filename">websockets-server.js</samp> will run when it is imported. It handles all initialization and events related to the WebSocket.

Now that you have a WebSockets server, the first thing you will do with it is handle connections. In <samp class="filename">websockets-server.js</samp>, establish a callback for any `connection` events for your WebSockets server:

```
var WebSocket = require('ws');
var WebSocketServer = WebSocket.Server;
var port = 3001;
var ws = new WebSocketServer({
    port: port
});

console.log('websockets server started');

ws.on('connection', function (socket) {
  console.log('client connection established');
});
```

The event-handling syntax is similar to jQuery’s. You will notice that many JavaScript libraries (in <samp class="application">Node</samp> and in the browser) use this style.

Your event-handler callback accepts a single argument named `socket`. When a client makes a connection to your WebSockets server, you have access to that connection via this `socket` object.

Before you write the chat server code, you will set up your server to repeat any messages sent to it. This is commonly known as an <samp class="firstterm">echo server</samp>.

Add the echo functionality in <samp class="filename">websockets-server.js</samp> by registering a callback for any `message` events generated by the client connection.

```
...
console.log('websockets server started');

ws.on('connection', function (socket) {
  console.log('client connection established');

  socket.on('message', function (data) {
    console.log('message received: ' + data);
    socket.send(data);
  });
});
```

You registered the event handler directly on the `socket` object. Your `message` event callback is passed any information sent by the client. For now, you are simply `send`ing it back to the same `socket` connection.

You will see this in action in just a moment.

You could run your WebSockets server by itself with the command `node websockets-server.js`, but it is just as easy to connect it to <samp class="filename">index.js</samp>. This has the benefit of taking advantage of `nodemon` to automatically reload your code when you make changes to either <samp class="filename">websockets-server.js</samp> or <samp class="filename">index.js</samp>.

At the top of <samp class="filename">index.js</samp>, add a `require` statement to import the `websockets-server` module.

```
var http = require('http');
var fs = require('fs');
var extract = require('./extract');
var wss = require('./websockets-server');
...
```

Save your file and `nodemon` will reload your code, making it ready for you to try out.

## Testing Your WebSockets Server

One way to easily test your server is to use the `wscat` `npm` module. `wscat` is a tool for connecting to and communicating with a WebSockets server. The module provides a command-line program that you will use as a chat client.

Open a second terminal window and install `wscat` globally. You may need to run this command with administrator privileges. (If you need a refresher, refer to [Chapter 1](#ch01.html "1 Setting Up Your Development Environment").)

```
npm install -g wscat
```

When `wscat` is installed, you are ready to connect to your WebSockets server.

In the second terminal window, run the command `wscat -c ws://localhost:3001`. You should see the message `connected (press CTRL+C to quit)` in the second terminal window and `'client connection established'` in the first window.

In the second terminal window, enter some text at the prompt. Each time you type some text and press the Return key, your text will be repeated by the WebSockets server, as shown in [Figure 16.3](#ch16s02.html_fig-testing-server "Figure 16.3  Testing the server with wscat").

**Figure 16.3  Testing the server with `wscat`**

![Testing the server with wscat](Chattrbox/WebSockets/echo.png)

Now that you have confirmed that you are able to communicate with your server via WebSockets, it is time to add the real functionality that will power Chattrbox’s chat system.

## Creating the Chat Server Functionality

With your WebSockets server up and running, you are now ready to build out your chat server. Your chat server needs to do a few things:

*   keep a log of the messages sent so far to the server

*   broadcast older messages to new people joining the chat

*   broadcast new messages to all clients

Keeping a log of messages as your users send them is necessary in order to send the message history to new users, so you will tackle that first.

In <samp class="filename">websockets-server.js</samp>, create an array to hold on to messages.

```
var WebSocket = require('ws');
var WebSocketServer = WebSocket.Server;
var port = 3001;
var ws = new WebSocketServer({
    port: port
});
var messages = [];

console.log('websockets server started');
...
```

If you were creating a more robust chat system, you might store your messages in a database. For now, a simple array is fine.

Next, call <samp class="methodname">messages.push(data)</samp> to add each new message to your array as it arrives.

```
...
ws.on('connection', function (socket) {
  console.log('client connection established');

  socket.on('message', function (data) {
    console.log('message received: ' + data);
    messages.push(data);
    socket.send(data);
  });
});
```

Just like that, you have an array of all the messages that have been received by your chat server.

The next step is to allow new users to see all the previous messages. Update the connection event handler in <samp class="filename">websockets-server.js</samp> to send out all the old messages to each new connection as it arrives.

```
...
ws.on('connection', function (socket) {
  console.log('client connection established');

  messages.forEach(function (msg) {
    socket.send(msg);
  });

  socket.on('message', function (data) {
    console.log('message received: ' + data);
    messages.push(data);
    socket.send(data);
  });
});
```

As soon as a connection is made, the server iterates through the messages and sends each one to the new connection.

The last job is to send new messages to all the users as each new message comes in. WebSockets keeps track of your connected users for you. Use this mechanism in <samp class="filename">websockets-server.js</samp> to rebroadcast your received messages.

```
...
ws.on('connection', function (socket) {
  console.log('client connection established');

  messages.forEach(function (msg) {
    socket.send(msg);
  });

  socket.on('message', function (data) {
    console.log('message received: ' + data);
    messages.push(data);
    ws.clients.forEach(function (clientSocket) {
      clientSocket.send(data)
    });

    socket.send(data);
  });
});
```

The <samp class="varname">ws</samp> object keeps track of all connections via its `clients` property. It is an array that you can iterate through. In your iterator callback, you only need to `send` the message data.

Finally, because you end up sending your message to your own socket when you iterate over all the sockets, you no longer need the call to <samp class="methodname">socket.send(data)</samp>. Deleting it cleans things up nicely.

## First Chat!

Let’s test the new functionality. Make sure that `nodemon` has reloaded your code. (If you need to, you can manually stop `nodemon` with Control-C and restart it with `npm run dev`.)

Open a third terminal window and run the command `wscat -c http://localhost:3001`. (You should have one terminal running `nodemon` and two running `wscat`.) Enter some chat messages in the two windows connected to the server.

After you have chatted with yourself for a bit, open a fourth terminal and run `wscat -c http://localhost:3001`. This chat client should be sent all the previous messages.

If everything went well, you should see something like [Figure 16.4](#ch16s04.html_fig-first-chat "Figure 16.4  Chatting with some friends").

**Figure 16.4  Chatting with some friends**

![Chatting with some friends](Chattrbox/WebSockets/breaking-bad-chat.png)

Congratulations! You have written a fully functional chat server using WebSockets – and it took less than two dozen lines of JavaScript.

## For the More Curious: socket.io WebSockets Library

The `ws` `npm` module is a perfectly fine WebSockets implementation. But, admittedly, it is lacking in a few ways. For example, WebSockets connections sometimes get dropped, but the `ws` module provides no way to automatically reconnect.

Another problem is that `ws` lives in <samp class="application">Node.js</samp>. That means that it is only available on the server. In your client-side JavaScript, you would need to learn a totally different library that accomplishes essentially the same task.

On top of that, on the client side you may have additional challenges: What if your browser is old and does not support WebSockets? You would need to provide a fallback mechanism of some kind.

`socket.io` ([<samp class="uri">socket.io</samp>](http://socket.io)) provides a solution to these problems. For browsers, it provides backward-compatible fallbacks, including a Flash implementation. In addition, it has been ported to a number of other platforms, including iOS and Android.

## For the More Curious: WebSockets as a Service

If you are interested in a real-time platform as a service, you may want to look into `firebase` ([<samp class="uri">www.firebase.com</samp>](https://www.firebase.com/)). If `socket.io` tries to make writing your server simpler, `firebase` goes one step further: It provides the entire server for you, including mechanisms for clients to share and synchronize data. `firebase` provides solutions for web, iOS, and Android.

## Bronze Challenge: Am I Repeating Myself?

Update your `message` handler so that every message received is sent twice to each user.

Test it out using `wscat` and confirm that each message is repeated.

For a really interesting effect, increment the number of repetitions by one each time a new message is sent.

## Silver Challenge: Speakeasy

In the United States, it was illegal to produce or sell alcohol during the 1920s. In response, “speakeasies” were created: secret establishments that sold alcoholic beverages and required a password before patrons were allowed to enter.

Create a speakeasy version of your chat program – but without the alcohol. Hide all messages from a user until they enter a secret password. (“Swordfish” is a good one, for historical reasons.)

When users enter the password, send them all previous messages and allow them to see new messages.

## Gold Challenge: Chat Bot

You used the `WebSocket.Server` property to create the chat server. You can also programmatically create a chat client by using `WebSocket` as a constructor.

The following line is an example:

```
var chatClient = new WebSocket('http://localhost:3001');
```

The documentation at [<samp class="uri">github.com/​websockets/​ws</samp>](https://github.com/websockets/ws) has a simple example of sending and receiving text data.

Create a chat bot that automatically connects to the chat server. It should greet each new user but otherwise remain silent unless directly spoken to. For example, if your chat bot responds to the name “Jinx,” you could type “Jinx, put Max in space,” and your chat bot would respond appropriately. (The appropriate response is up to you.)

Make sure that the code for your chat bot is in a separate module, not built directly into the chat server code.

# <samp class="chapter_number">17</samp>
<samp class="chapter_name">Using ES6 with Babel</samp>

The JavaScript language was created in 1994, received a few updates in 1999, but went unchanged from 1999 to 2009\. A set of small changes was introduced in 2009, resulting in the version of JavaScript known as ES5, or the fifth edition of the standard.

In 2015, a number of language improvements were added as the sixth edition of the standard. Many of these new language features were influenced by languages like Ruby and Python. Technically, this sixth edition is named ES2015, but it is more commonly known as ES6.

ES6 is well supported by <samp class="application">Google Chrome</samp>, <samp class="application">Mozilla Firefox</samp>, and <samp class="application">Microsoft Edge</samp>. These are <samp class="firstterm">evergreen</samp> browsers, meaning that they self-update without the user needing to manually download and install the latest version. As Google, Mozilla, and Microsoft have added more and more ES6 compatibility to their browsers, they have been able to roll out these enhancements quickly to their users.

However, non-evergreen and most mobile browsers have poor support for ES6\. [Figure 17.1](#ch17.html_fig-browser-support "Figure 17.1  ES6 feature support as of spring 2016") shows the percentage of ES6 features supported by recent versions of desktop and mobile browsers. (In the figure, IE = <samp class="application">Internet Explorer</samp>, FF = <samp class="application">Mozilla Firefox</samp>, CH = <samp class="application">Google Chrome</samp>, SF = <samp class="application">Safari</samp>, KQ = <samp class="application">Konqueror</samp>, and AN = Android.)

**Figure 17.1  ES6 feature support as of spring 2016**

![ES6 feature support as of spring 2016](Chattrbox/ES6-Babel/kangax-support-table.png)

If you would like a closer or up-to-date look at browser support for ES6, go to [<samp class="uri">kangax.github.io/​compat-table/​es6/</samp>](http://kangax.github.io/compat-table/es6/) to check out the latest information. The table’s creator, Juriy Zaytsev, updates the data frequently.

Support may be spotty among older browsers, but we love, love, love ES6\. It is a beautiful thing, and it is worth the effort to switch over as soon as possible rather than waiting until support is universal.

In this chapter, you will begin working on the user-facing portion of Chattrbox, which you will write using a number of ES6 features. To make sure your application works on all browsers, you will use the open-source tool <samp class="application">Babel</samp> to take care of compatibility.

There is one item of housekeeping to take care of before you begin. So that you can focus on learning ES6 and using <samp class="application">Babel</samp>, the <samp class="filename">index.html</samp> and <samp class="filename">stylesheets/styles.css</samp> files for Chattrbox are provided for you at [<samp class="uri">www.bignerdranch.com/​downloads/​front-end-dev-resources.zip</samp>](http://www.bignerdranch.com/downloads/front-end-dev-resources.zip). Download the .zip file and extract the contents (including the entire <samp class="filename">stylesheets/</samp> folder) into your <samp class="filename">chattrbox/app</samp> directory. (<samp class="filename">index.html</samp> will replace your existing copy of <samp class="filename">index.html</samp>.)

Also, one note: While working through the code in this chapter, you may see a warning in the console about the MIME type of your CSS files. It is safe to ignore this warning.

Onward and upward! By the end of this chapter, Chattrbox will communicate over WebSockets with your chat server ([Figure 17.2](#ch17.html_ss-chattrbox-end-of-chapter "Figure 17.2  Chattrbox at the end of this chapter")).

**Figure 17.2  Chattrbox at the end of this chapter**

![Chattrbox at the end of this chapter](Chattrbox/ES6-Babel/end-of-chapter.png)

## Tools for Compiling JavaScript

<samp class="application">Babel</samp> is a compiler. Its job is to translate ES6 syntax into the equivalent ES5 code to be run by a browser’s JavaScript engine ([Figure 17.3](#ch17.html_fig-Babel-compiling "Figure 17.3  Building ES5 code from ES6 files")).

**Figure 17.3  Building ES5 code from ES6 files**

![Building ES5 code from ES6 files](Chattrbox/ES6-Babel/compilation.png)

To use <samp class="application">Babel</samp> effectively, you will need to install a few `npm` modules to create an automated build process. You will use <samp class="application">Babel</samp> to compile your ES6 code to ES5, <samp class="application">Browserify</samp> to bundle your modules together into a single file, and <samp class="application">Babelify</samp> to make the two work together. Additionally, you will use <samp class="application">Watchify</samp> to trigger the build process any time you save changes to your code ([Figure 17.4](#ch17.html_fig-compile-workflow "Figure 17.4  Compilation workflow")).

**Figure 17.4  Compilation workflow**

![Compilation workflow](Chattrbox/ES6-Babel/compilation-workflow.png)

First, you need to install <samp class="application">Babel</samp>. It has a few different moving parts, depending on your needs. In your case, you will need the ability to compile in two ways: from the command line and programmatically. The tools `babel-cli` and `babel-core`, respectively, will address these needs. You will also need to install a <samp class="application">Babel</samp> configuration suitable for compiling the ES6 standard, which is called `babel-preset-es2015`.

Run the following `npm` commands in your <samp class="filename">chattrbox</samp> directory to install the appropriate <samp class="application">Babel</samp> tooling. (If you need a refresher on how to run `npm install -g` with administrator privileges, refer to [Chapter 1](#ch01.html "1 Setting Up Your Development Environment").)

```
npm install -g babel-cli
npm install --save-dev babel-core
npm install --save-dev babel-preset-es2015
```

Now you need to configure <samp class="application">Babel</samp> to compile using the `es2015` preset you installed. Create a file called <samp class="filename">.babelrc</samp> in your root <samp class="filename">chattrbox</samp> folder and add the following configuration information to it:

```
{
  "presets": [
    "es2015"
  ],
  "plugins": []
}
```

Finally, install <samp class="application">Babelify</samp>, <samp class="application">Browserify</samp>, and <samp class="application">Watchify</samp> to the <samp class="filename">chattrbox/node_modules/</samp> directory:

```
npm install --save-dev browserify babelify watchify
```

You will be using these three tools later in this chapter, after you have <samp class="application">Babel</samp> up and running.

## The Chattrbox Client Application

You already built the Chattrbox server, which serves out the static files and handles communication over WebSockets. The client application will send and receive messages to and from the server over WebSockets. It will define a format for individual messages. The user will be able to view the messages in a list as well as create new messages by entering text into a form.

Those responsibilities will be handled by three modules:

*   the <samp class="filename">ws-client</samp> module will manage the WebSockets communication for the client

*   the <samp class="filename">dom</samp> module will display data to the UI and handle form submissions

*   the <samp class="filename">app</samp> module will define the structure of messages and pass messages between <samp class="filename">ws-client</samp> and <samp class="filename">dom</samp>

[Figure 17.5](#ch17s02.html_fig-app-modules "Figure 17.5  Chattrbox application modules") diagrams the relationships among the three modules.

**Figure 17.5  Chattrbox application modules**

![Chattrbox application modules](Chattrbox/ES6-Babel/app-architecture.png)

In your <samp class="filename">chattrbox/app</samp> folder, create <samp class="filename">scripts</samp>, <samp class="filename">scripts/dist</samp>, and <samp class="filename">scripts/src</samp> subfolders, as shown in [Figure 17.6](#ch17s02.html_fig-folders "Figure 17.6  chattrbox/app folder structure").

**Figure 17.6  `chattrbox/app` folder structure**

![chattrbox/app folder structure](Chattrbox/ES6-Babel/folder-with-scripts-folders.png)

Now, create four JavaScript files in <samp class="filename">scripts/src</samp>:

*   <samp class="filename">app.js</samp>

*   <samp class="filename">dom.js</samp>

*   <samp class="filename">main.js</samp>

*   <samp class="filename">ws-client.js</samp>

Your file structure should look like [Figure 17.7](#ch17s02.html_fig-file-structure "Figure 17.7  chattrbox/app").

**Figure 17.7  `chattrbox/app`**

![chattrbox/app](Chattrbox/ES6-Babel/folder-with-scripts-files.png)

<samp class="filename">app.js</samp>, <samp class="filename">dom.js</samp>, and <samp class="filename">ws-client.js</samp> correspond to the modules shown in [Figure 17.5](#ch17s02.html_fig-app-modules "Figure 17.5  Chattrbox application modules"). The <samp class="filename">main.js</samp> file will contain the code that initializes your application.

## First Steps with Babel

Now that you have your tools installed and your files in place, it is time to get started with ES6.

For the moment, you will use <samp class="application">Babel</samp> from the command line. Later, you will add it to your `npm` scripts so that compilation happens automatically. That way, as you work with new ES6 features you can focus on the new syntax without worrying about running extra commands in the terminal.

### Class syntax

The first ES6 feature you will use for building the Chattrbox client is the `class` keyword. It is important to keep in mind that the ES6 `class` keyword does not work exactly like classes in other programming languages. Instead, ES6 classes merely provide a shorter syntax for constructor functions and `prototype` methods.

Open <samp class="filename">app.js</samp> and define a new class called <samp class="classname">ChatApp</samp>.

```
class ChatApp {
}
```

In this chapter, <samp class="classname">ChatApp</samp> will not do much. Ultimately, though, <samp class="classname">ChatApp</samp> will be responsible for most of your application logic.

The definition of the class is currently empty. Add a <samp class="methodname">constructor</samp> method with a <samp class="methodname">console.log</samp> statement:

```
class ChatApp {
  constructor() {
    console.log('Hello ES6!');
  }
}
```

<samp class="methodname">constructor</samp> is a method that is run any time you create a new instance of a class. Usually, the constructor will set values for properties belonging to the instance.

Next, create an instance of <samp class="classname">ChatApp</samp> in <samp class="filename">app.js</samp>, right after the class declaration:

```
class ChatApp {
  constructor() {
    console.log('Hello ES6!');
  }
}
new ChatApp();
```

Let’s give your code a test run. Open a second terminal window and switch to Chattrbox’s root directory, where <samp class="filename">package.json</samp>, <samp class="filename">index.js</samp>, and <samp class="filename">app/</samp> live. You will use this window to run your build commands and keep the other one open for running your server.

To test your code, use <samp class="application">Babel</samp> to compile <samp class="filename">app/scripts/src/app.js</samp> and output the result to <samp class="filename">app/scripts/dist/main.js</samp>:

```
babel app/scripts/src/app.js -o app/scripts/dist/main.js
```

If you do not see anything happen in your terminal, that is normal – and good news. <samp class="application">Babel</samp> will not report anything on the command line unless there is an error ([Figure 17.8](#ch17s03.html_fig-quiet-babel "Figure 17.8  Babel works quietly")).

**Figure 17.8  Babel works quietly**

![Babel works quietly](Chattrbox/ES6-Babel/babel-slient.png)

Make sure your <samp class="application">Node</samp> server is running in your other terminal (with `npm run dev`), and open your browser to `http://localhost:3000`. Now you will see your results ([Figure 17.9](#ch17s03.html_fig-test-results "Figure 17.9  Hello, ES6!")).

**Figure 17.9  Hello, ES6!**

![Hello, ES6!](Chattrbox/ES6-Babel/hello-es6.png)

Your <samp class="filename">app/index.html</samp> sources the <samp class="filename">main.js</samp> you generated from <samp class="filename">app.js</samp>. And because <samp class="filename">app.js</samp> creates a new <samp class="classname">ChatApp</samp>, the code in <samp class="classname">ChatApp</samp>’s constructor is run, logging out “Hello ES6!”

Now that you have confirmed that <samp class="application">Babel</samp> is working with a single JavaScript file, it is time to start working with multiple modules.

## Using Browserify for Packaging Modules

One thing that ES5 does not have is a built-in module system. When you built CoffeeRun, you used a workaround that let you write modular code – but depended on modifying a global variable.

ES6 provides true modules, like those in many other programming languages. <samp class="application">Babel</samp> understands ES6 module syntax, but there is no equivalent ES5 code for it to convert to. That is why <samp class="application">Browserify</samp> is necessary.

[Figure 17.10](#ch17s04.html_fig-babel-browserify "Figure 17.10  Converting from ES6 modules to ES5 modules with Babel and Browserify") shows how <samp class="application">Browserify</samp> and <samp class="application">Babel</samp> will work together.

**Figure 17.10  Converting from ES6 modules to ES5 modules with Babel and Browserify**

![Converting from ES6 modules to ES5 modules with Babel and Browserify](Chattrbox/ES6-Babel/es6-node-iifes.png)

By default, <samp class="application">Babel</samp> converts ES6 module syntax into the equivalent <samp class="application">Node.js</samp>-style `require` and `module.exports` syntax. <samp class="application">Browserify</samp> then converts <samp class="application">Node.js</samp> module code into ES5-friendly functions.

Open <samp class="filename">package.json</samp> and add a configuration section for <samp class="application">Browserify</samp>:

```
...
  "scripts": {
    "test": "echo \"Error: no test specified\" &&
     exit 1",
    "start": "node index.js",
    "dev": "nodemon index.js",
  },
  "browserify": {
    "transform": [
      ["babelify", {"presets": ["es2015"], "sourceMap": true}]
    ]
  },
...
```

This tells <samp class="application">Browserify</samp> to use <samp class="application">Babelify</samp> as a plug-in. It passes two options to <samp class="application">Babelify</samp>: First, it activates the ES2015 compiler option. It also turns on the `sourceMap` option, which helps with debugging. You will learn how to debug with source maps as you build the rest of Chattrbox.

You will also want to write some scripts for common <samp class="application">Browserify</samp> tasks, as you did for `nodemon`. Write those in your `"scripts"` section in <samp class="filename">package.json</samp>. (Remember to add the comma at the end of `"dev": "nodemon index.js"`.)

```
...
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node index.js",
    "dev": "nodemon index.js",
    "build": "browserify -d app/scripts/src/main.js -o app/scripts/dist/main.js",
    "watch": "watchify -v -d app/scripts/src/main.js -o app/scripts/dist/main.js"
  },
  "browserify": {
    "transform": [
      ["babelify", {"presets": ["es2015"], "sourceMap": true}]
    ]
  },
...
```

The first script, `build`, uses the `browserify` command directly. The second script, `watch`, uses `watchify` to rerun `browserify` whenever your code changes. (It serves a similar purpose to `nodemon`.)

Now to use the ES6 module system. In ES6 modules, you must explicitly export the pieces of your module you want others to use. Update <samp class="filename">app.js</samp> to export your <samp class="classname">ChatApp</samp> class rather than simply creating an instance.

```
class ChatApp {
  constructor() {
    console.log('Hello ES6!');
  }
}
new ChatApp();
export default ChatApp;
```

You specified that <samp class="classname">ChatApp</samp> is the default value available from the <samp class="filename">app</samp> module. Some of your other modules will `export` multiple values. When you only need to export a single value, it is best to use `export default`.

In <samp class="filename">main.js</samp>, import the <samp class="classname">ChatApp</samp> class and create a new instance of it.

```
import ChatApp from './app';
new ChatApp();
```

<samp class="filename">main.js</samp> is `import`ing the <samp class="classname">ChatApp</samp> class that <samp class="filename">app.js</samp> `export`ed. After the import, you create a new instance of the <samp class="classname">ChatApp</samp> class.

One important note here: The name <samp class="classname">ChatApp</samp> is not significant in <samp class="filename">main.js</samp>. Because <samp class="classname">ChatApp</samp> is the default export from <samp class="filename">app.js</samp>, writing `import MyChatApp from './app'`, for example, would assign the default export value to the local <samp class="classname">MyChatApp</samp> name. Naming it <samp class="classname">ChatApp</samp> is a best practice, however, because that is its name inside <samp class="filename">app.js</samp>.

### Running the build process

Next, go to your terminal and run your build script:

```
npm run build
```

`npm` will run your `build` command, which will then run `browserify`. As it runs each command, it will show you what it is doing. <samp class="application">Browserify</samp> itself will be silent, though, unless there is an error ([Figure 17.11](#ch17s04.html_fig-quiet-browserify "Figure 17.11  Running Browserify via npm run build")).

**Figure 17.11  Running Browserify via `npm run build`**

![Running Browserify via npm run build](Chattrbox/ES6-Babel/npm-run-build.png)

When <samp class="application">Browserify</samp> is successful, it will package your en-<samp class="application">Babel</samp>ed <samp class="filename">main.js</samp> in your <samp class="filename">app/dist/</samp> folder, just as you did earlier by hand.

Now to reload your browser and see the output. You added no new functionality, other than restructuring where the call to <samp class="classname">ChatApp</samp>’s constructor lives. So you should see the same message in the console that you saw earlier ([Figure 17.12](#ch17s04.html_fig-second-test-same "Figure 17.12  Hello again!")).

**Figure 17.12  Hello again!**

![Hello again!](Chattrbox/ES6-Babel/hello-es6.png)

The next piece to integrate is <samp class="application">Watchify</samp>. <samp class="application">Watchify</samp> will do the same thing for running your <samp class="application">Browserify</samp> build that `nodemon` did for running your <samp class="application">Node.js</samp> server: It will automatically trigger a rebuild every time you modify one of your source files.

Start <samp class="application">Watchify</samp> to kick off the build process any time you make a change to your code:

```
npm run watch
```

<samp class="application">Watchify</samp> will confirm that it is running ([Figure 17.13](#ch17s04.html_fig-watchify-watching "Figure 17.13  Running Watchify via npm run watch")).

**Figure 17.13  Running Watchify via `npm run watch`**

![Running Watchify via npm run watch](Chattrbox/ES6-Babel/npm-run-watch.png)

<samp class="application">Watchify</samp> is a bit chattier than <samp class="application">Browserify</samp>. Every time it runs <samp class="application">Browserify</samp>, it tells you how many bytes it wrote to the file. That is not terribly interesting, but it does tell you when the output changes. Leave <samp class="application">Watchify</samp> running in one of your terminals as you continue to work on Chattrbox. (Your server should still be running in the other terminal.)

## Adding the ChatMessage Class

Chatting between two terminals is fun (and makes you look cool at the coffee shop), but it is time to upgrade to sending messages from browser to browser. You will write a helper class that handles constructing and formatting message data.

There are three pieces of information you will want to track for each message. You need to know the text of the message, who sent it, and at what time.

JavaScript Object Notation – more commonly known as JSON (pronounced “Jason,” per creator Douglas Crockford) – is a lightweight data-interchange format. You have already been using JSON for your <samp class="filename">package.json</samp> file. It is human readable and language independent, and it is ideal for sending and receiving the kind of data you want to exchange with Chattrbox.

Here is a sample message formatted as JSON:

```
{
  "message": "I'm Batman",
  "user": "batman",
  "timestamp": 614653200000
}
```

Chattrbox message data will come from two different sources. One source is in the client, when the user fills out the form. The other source is the server, when the message is sent over a WebSocket connection to other clients.

When message data comes from the form, you will need to add the username and timestamp before sending it to the server. When the data comes from the server, all three pieces of information should be included. How should you handle this discrepancy? There are a number of options. Let’s briefly look at a few of them, including some that take advantage of some handy ES6 features.

Create a class to represent individual chat messages in <samp class="filename">app.js</samp>.

```
class ChatApp {
  constructor() {
    console.log('Hello ES6!');
  }
}

class ChatMessage {
  constructor(data) {
  }
}

export default ChatApp;
```

The first way to approach the problem is a simple constructor that accepts the message text, username, and timestamp. (Do not make this change in your file. It is only an example.)

```
...
class ChatMessage {
  constructor(message, user, timestamp) {
    this.message = message;
    this.user = user || 'batman';
    this.timestamp = timestamp || (new Date()).getTime();
  }
}
...
```

You have seen this pattern a number of times. You assign the parameter values to instance properties, providing fallbacks for <samp class="varname">username</samp> and <samp class="varname">timestamp</samp> using the `||` operator.

This is fine, but ES6 gives you a more compact way to write this same pattern using <samp class="firstterm">default arguments</samp>.

```
...
class ChatMessage {
  constructor(message, user='batman', timestamp=(new Date()).getTime()) {
    this.message = message;
    this.user = user;
    this.timestamp = timestamp;
  }
}
...
```

This syntax makes it obvious which values must be passed in and which ones are optional. You can see that only the <samp class="varname">message</samp> argument is mandatory. The others have defaults.

This version of the constructor can handle messages received from the server or created by the form. But it requires that the caller know the order of arguments, which can get cumbersome for functions and methods that have three or more arguments.

An alternative to this is for the constructor to receive a single object as argument, with the key/value pairs specifying the values for <samp class="varname">message</samp>, <samp class="varname">user</samp>, and <samp class="varname">timestamp</samp>. For that, you can use the <samp class="firstterm">destructuring assignment syntax</samp>.

```
...
class ChatMessage {
  constructor({message: m, user: u, timestamp: t}) {
    this.message = m;
    this.user = u;
    this.timestamp = t;
  }
}
...
```

Destructuring may look a little odd, but here is how it works. You call the constructor like this:

```
new ChatMessage({message: 'hello from the outside',
                 user='adele25@bignerdranch.com', timestamp=1462399523859});
```

The destructuring syntax looks for the key `message` in the argument. It finds the value `'hello from the outside'` and assigns it to a new local variable <samp class="varname">m</samp>. This variable can then be used inside the body of the constructor. The same thing happens for the <samp class="varname">username</samp> and <samp class="varname">timestamp</samp> properties.

But with this syntax you lose the convenience of the default parameters. Luckily, you can combine the two techniques. This final version of the constructor is the one you should add to <samp class="filename">app.js</samp>:

```
...
class ChatMessage {
  constructor(data){
    message: m,
    user: u='batman',
    timestamp: t=(new Date()).getTime()
}) {
    this.message = m;
    this.user = u;
    this.timestamp = t;
  }
}
...
```

In this version, you are plucking values out of the object that is passed to the constructor. For any values that do not exist, defaults are provided.

While default arguments can only exist as part of a function (or constructor) definition, destructuring can be used as part of an assignment. You might also write the constructor like this:

```
...
class ChatMessage {
  constructor(data) {
    var {message: m, user: u='batman', timestamp: t=(new Date()).getTime()} = data;
    this.message = m;
    this.user = u;
    this.timestamp = t;
  }
}
...
```

OK, the detour is over. Time to get back to building Chattrbox!

Your <samp class="classname">ChatMessage</samp> class stores all of the important information as properties, but its instances also inherit <samp class="classname">ChatMessage</samp>’s methods and other information. That makes <samp class="classname">ChatMessage</samp> instances unsuitable for sending through WebSockets. A stripped-down version of that information is necessary.

Write a <samp class="methodname">serialize</samp> method in <samp class="filename">app.js</samp> to represent the data in <samp class="classname">ChatMessage</samp>’s properties as a plain JavaScript object.

```
...
class ChatMessage {
  constructor({
    message: m,
    user: u='batman',
    timestamp: t=(new Date()).getTime()
  }) {
    this.user = user;
    this.message = message;
    this.timestamp = timestamp;
  }
  serialize() {
    return {
      user: this.user,
      message: this.message,
      timestamp: this.timestamp
    };
  }
}

export default ChatApp;
```

Your <samp class="classname">ChatMessage</samp> class is now ready for use. It is time to move on to the next module for Chattrbox.

## Creating the ws-client Module

The <samp class="filename">ws-client.js</samp> module will handle communicating with your <samp class="application">Node</samp> WebSocket server.

It will have four responsibilities:

*   connecting to the server

*   performing initial setup when the connection is first opened

*   forwarding incoming messages to their handlers

*   sending outgoing messages

Check out how those responsibilities relate to your other components ([Figure 17.14](#ch17s06.html_dig-app-architecture-ws-client "Figure 17.14  ws-client’s interfaces")).

**Figure 17.14  `ws-client`’s interfaces**

![ws-client’s interfaces](Chattrbox/ES6-Babel/app-architecture-ws-client.png)

As you build out your client, you will get a tour of some new ES6 features as well.

### Connection handling

First, build out your collection handling. Begin by opening <samp class="filename">ws-client.js</samp> and declaring a variable for the WebSocket connection.

```
let socket;
```

This declaration uses a new way of defining variables in ES6 called <samp class="firstterm">let scoping</samp>. If you use let scoping to declare a variable – using the keyword `let` instead of `var` – your variable will not be <samp class="firstterm">hoisted</samp>.

Hoisting means that the variable declarations get moved to the top of the function scope in which they are created. This is something that the JavaScript interpreter does behind the scenes. Unfortunately, it can lead to hard-to-find errors.

You will read more about hoisting at the end of the chapter. For now, know that `let` is a safer way to declare variables in `if/else` clauses and in the body of loops.

Now, add a method to <samp class="filename">ws-client.js</samp> to initialize your connection.

```
let socket;

function init(url)  {
  socket = new WebSocket(url);
  console.log('connecting...');
}
```

The <samp class="function">init</samp> function connects to the WebSockets server. Next, you want to wire up <samp class="filename">ws-client.js</samp> to <samp class="classname">ChatApp</samp> in <samp class="filename">app.js</samp>.

To be a functioning module, <samp class="filename">ws-client.js</samp> needs to specify what it exports. You need to export a single value: an object code with the exported functions as its properties. You are going to use the same `export default` syntax that you used at the beginning of the chapter – plus an additional bit of ES6 handiness.

Add the export to the end of <samp class="filename">ws-client.js</samp>, as shown.

```
...
function init(url)  {
  socket = new WebSocket(url);
  console.log('connecting...');
}

export default {
  init,
}
```

Notice that you did not have to specify the property names. This syntactic shortcut is the equivalent of:

```
export default {
  init: init
}
```

If the key and value have the same name, ES6 allows you to omit the colon and the value. The key will automatically be the variable name, and the value will automatically be the value associated with that name. This feature of ES6 is the <samp class="firstterm">enhanced object literal</samp> syntax.

Now that you have the <samp class="filename">ws-client</samp> module set up, it is time to import the values it provides in <samp class="filename">app.js</samp>. Begin by adding an import statement to the top of <samp class="filename">app.js</samp>:

```
import socket from './ws-client';

class ChatApp {
  constructor() {
    console.log('Hello ES6!');
  }
}
...
```

<samp class="varname">socket</samp> will be the object you exported from <samp class="filename">ws-client.js</samp>.

Next, in the <samp class="classname">ChatApp</samp> constructor, call <samp class="function">socket.init</samp> with the URL of your WebSocket server.

```
import socket from './ws-client';

class ChatApp {
  constructor() {
    console.log('Hello ES6!');
    socket.init('ws://localhost:3001');
  }
}
...
```

Your `npm` script should rebuild the code for you. (You may need to restart `npm run watch` and `npm run dev` in separate windows, if you have let one or both of them stop.) Reload your browser and you should see `'connecting...'` logged to the console, as shown in [Figure 17.15](#ch17s06.html_fig-connecting-message-logged "Figure 17.15  Message logged on WebSocket initialization").

**Figure 17.15  Message logged on WebSocket initialization**

![Message logged on WebSocket initialization](Chattrbox/ES6-Babel/ws-connecting.png)

With that, you have the skeleton of your app up and running.

### Handling events and sending messages

When your `App` module calls <samp class="methodname">init</samp>, a new <samp class="function">WebSocket</samp> object is instantiated and a connection is made to the server. But your `App` module needs to know when this process has completed so that it can do something with the connection.

The <samp class="function">WebSocket</samp> object has a set of special properties for handling events. One of these is the <samp class="varname">onopen</samp> property. Any function assigned to this property will be called when the connection to the WebSocket server is made. Inside this function, you can carry out any steps that need to be made upon connecting.

In order for the `ws-client` module to be flexible and reusable, you will not hardcode the steps that the `App` module needs to make upon connecting. Instead, you will use the same pattern you used for registering click and submit handlers in CoffeeRun.

Add a function called <samp class="function">registerOpenHandler</samp> to <samp class="filename">ws-client.js</samp>. <samp class="function">registerOpenHandler</samp> will accept a callback, assign a function to <samp class="varname">onopen</samp>, and then invoke the callback inside the <samp class="varname">onopen</samp> function.

```
let socket;

function init(url)  {
  socket = new WebSocket(url);
  console.log('connecting...');
}

function registerOpenHandler(handlerFunction) {
  socket.onopen = () => {
    console.log('open');
    handlerFunction();
  };
}
...
```

This function definition is different from what you have written before. This is a new ES6 syntax called an <samp class="firstterm">arrow function</samp>. Arrow functions are a shorthand for writing anonymous functions. Apart from being a bit easier to write, arrow functions work exactly the same as anonymous functions.

<samp class="function">registerOpenHandler</samp> takes a function argument (<samp class="function">handlerFunction</samp>) and assigns an anonymous function to the `onopen` property of the socket connection. Inside of this anonymous function, you call the <samp class="function">handlerFunction</samp> that was passed in.

(Using an anonymous function is more complicated than writing `socket.onopen = handlerFunction`. This pattern will serve you well when you need to respond to an event but have intermediary steps that must happen before forwarding it on – like writing a log message, as you have done here.)

Next, you need to write an interface for handling messages as they come in over your WebSockets connection. Write a new method called <samp class="methodname">registerMessageHandler</samp> in <samp class="filename">ws-client.js</samp>. Assign an arrow function to the <samp class="varname">socket</samp>’s <samp class="varname">onmessage</samp> property; this arrow function should expect to receive an event argument.

```
...
function registerOpenHandler(handlerFunction) {
  socket.onopen = () => {
    console.log('open');
    handlerFunction();
  };
}

function registerMessageHandler(handlerFunction) {
  socket.onmessage = (e) => {
    console.log('message', e.data);
    let data = JSON.parse(e.data);
    handlerFunction(data);
  };
}
...
```

Arrow function parameters go inside the parentheses, just as they do for regular functions.

The Chattrbox client receives an object from the server in its <samp class="methodname">onmessage</samp> callback inside <samp class="function">registerMessageHandler</samp>. This object represents the event and has a <samp class="varname">data</samp> property that contains the JSON string from the server. Each time you receive a string, you convert the string to a JavaScript object. You then forward it along to <samp class="function">handlerFunction</samp>.

The last bit is the piece that will actually send the message to your WebSocket. Write this in <samp class="filename">ws-client.js</samp> as a function called <samp class="function">sendMessage</samp>. You will do this in two parts. First, you will turn your message payload (containing the message, the username, and the timestamp) into a JSON string. Then you will send that JSON string to the WebSocket server.

```
...
function registerMessageHandler(handlerFunction) {
  socket.onmessage = (e) => {
    console.log('message', e.data);
    let data = JSON.parse(e.data);
    handlerFunction(data);
  };
}

function sendMessage(payload) {
  socket.send(JSON.stringify(payload));
}
...
```

Finally, add exports for your new methods using the enhanced object literal syntax.

```
...
function sendMessage(payload) {
  socket.send(JSON.stringify(payload));
}

export default {
  init,
  registerOpenHandler,
  registerMessageHandler,
  sendMessage
}
```

With that, <samp class="filename">ws-client.js</samp> has everything it needs to communicate back and forth with the server. Your last job in <samp class="filename">ws-client.js</samp> will be to test it by sending a message.

### Sending and echoing a message

Update the <samp class="classname">ChatApp</samp> constructor in <samp class="filename">app.js</samp>. After calling <samp class="methodname">socket.init</samp>, call <samp class="function">registerOpenHandler</samp> and <samp class="function">registerMessageHandler</samp>, passing them arrow functions.

```
import socket from './ws-client';

class ChatApp {
  constructor() {
    socket.init('ws://localhost:3001');
    socket.registerOpenHandler(() => {
      let message = new ChatMessage({ message: 'pow!' });
      socket.sendMessage(message.serialize());
    });
    socket.registerMessageHandler((data) => {
      console.log(data);
    });
  }
}
...
```

When the connection is open, you are immediately sending a dummy message. And when a message is received, you are logging it to the console.

Save your code and reload the browser when the build process finishes. You should see that a message was sent and echoed back ([Figure 17.16](#ch17s06.html_fig-call-and-response "Figure 17.16  Call and response with WebSockets")).

**Figure 17.16  Call and response with WebSockets**

![Call and response with WebSockets](Chattrbox/ES6-Babel/eureka.png)

Excellent work! You have two of the three primary modules for Chattrbox working. You will finish Chattrbox in the next chapter by creating a module that connects your existing modules to the UI. This module will draw new messages to the message list and send messages when the form is submitted.

## For the More Curious: Compiling to JavaScript from Other Languages

There are quite a few languages that will compile to JavaScript. Here is a short list:

*   CoffeeScript: [<samp class="uri">coffeescript.org</samp>](http://coffeescript.org/)

*   TypeScript: [<samp class="uri">www.typescriptlang.org</samp>](http://www.typescriptlang.org/)

*   C/C++: [<samp class="uri">kripken.github.io/​emscripten-site</samp>](http://kripken.github.io/emscripten-site/)

One of the most prominent is CoffeeScript, which provides shorthand syntax for some of the most common patterns (e.g., the arrow syntax for anonymous functions). In fact, CoffeeScript had a significant influence on ES6.

Google, Microsoft, Mozilla, and others are collaborating on a project to standardize an assembly language for JavaScript engines, called WebAssembly. The goal is to create a high-performance, low-level language that can be compiled to from many different languages.

The intention for WebAssembly is to supplement JavaScript – not replace it – and to capitalize on the strengths of multiple languages. JavaScript is good at creating browser-based applications, for example, but not at rendering math-intensive game graphics. C and C++, meanwhile, excel at rendering game code. Rather than porting C++ code over to JavaScript and potentially introducing bugs, it could be compiled to WebAssembly.

The WebAssembly project sprang out of an earlier project called asm.js, which specified a subset of the JavaScript language for writing high-performance code.

For more information about asm.js and WebAssembly, check out this blog post by the creator of JavaScript: [<samp class="uri">brendaneich.com/​2015/​06/​from-asm-js-to-webassembly</samp>](https://brendaneich.com/2015/06/from-asm-js-to-webassembly/).

## Bronze Challenge: Default Import Name

In <samp class="filename">main.js</samp>, your import statement creates a local variable named <samp class="varname">ChatApp</samp>. What happens if you change this to <samp class="varname">ApplicationForChatting</samp>?

Try it (making sure you also change the `new` statement on the next line) and find out whether it still works. If so, why? If not, why not?

## Silver Challenge: Closed Connection Alert

In the <samp class="filename">ws-client</samp> module, add another function called <samp class="function">registerCloseHandler</samp>. It should take a callback that is invoked when the `close` event is triggered on the socket.

In <samp class="filename">main.js</samp>, use <samp class="function">registerCloseHandler</samp> to alert the user that the connection is closed. Then, test it to make sure it works.

How can you test it? Obviously, you cannot close the browser window. You will need to close the other end of the connection.

For an added bonus, write a function that attempts to reconnect. You can either use a <samp class="function">setTimeout</samp> or you can prompt the user for confirmation (search the MDN for details).

## For the More Curious: Hoisting

JavaScript was created so that nonprofessional programmers could create web content with some basic interactivity. Although the language has features intended to make code error-resistant, some of its features end up causing errors in practice. One of these features is hoisting.

When the JavaScript engine interprets your code, it finds all of the variable and function declarations and moves them to the top of the function they are in. (Or, if they are not in a function, they are evaluated before the rest of the code.)

This is best illustrated with an example. When you write this code:

```
function logSomeValues () {
  console.log(myVal);
  var myVal = 5;
  console.log(myVal);
}
```

it is interpreted as though you had written:

```
function logSomeValues () {
  var myVal;
  console.log(myVal);
  myVal = 5;
  console.log(myVal);
}
```

If you called <samp class="function">logSomeValues</samp> the console, you would see this:

```
> logSomeValues();
undefined
5
```

Notice that it is only the <samp class="emphasis">declaration</samp> that is hoisted. The assignment stays in place. Naturally, this can cause confusion, especially if you were to try to declare variables in an `if` statement or inside of a loop. In other languages, the curly braces denote a <samp class="firstterm">block</samp>, which has its own scope. In JavaScript, curly brace blocks do not create scope. Only functions create scope.

Take a look at another example:

```
var myVal =  11;
function doNotWriteCodeLikeThis() {
  if (myVal > 10) {
    var myVal = 0;
    console.log('myVal was greater than 10; resetting to 0');
  } else {
    console.log('no need to reset.');
  }
  return myVal;
}
```

You might expect that <samp class="literal">'myVal was greater than 10; resetting to 0'</samp> would be printed to the console and the value <samp class="literal">0</samp> returned. Instead, this is what would be printed:

```
> doNotWriteCodeLikeThis();
no need to reset.
undefined
```

The declaration `var myVal` is moved to the top of the function, so before the `if` clause is evaluated, <samp class="varname">myVal</samp> has a value of `undefined`. The assignment stays inside the `if` block.

Function declarations are also hoisted, but in their entirety. That means that this works just fine:

```
boo();

// Declare after calling:
function boo() {
  console.log('BOO!!');
}
```

JavaScript moves the entire function declaration block to the top, allowing the invocation of <samp class="function">boo</samp> to happen without any problems:

```
> boo();
BOO!!
```

`let` statements are immune to hoisting. <samp class="firstterm">const</samp> statements, which let you declare variables that cannot be reassigned, are also immune.

## For the More Curious: Arrow Functions

We fibbed. Arrow functions do not work <samp class="emphasis">exactly</samp> like anonymous functions. For some situations, they are <samp class="emphasis">better</samp>.

In addition to providing shorter syntax, arrow functions:

*   work as though you had written `function () {}.bind(this)`, making <samp class="varname">this</samp> work as expected in the body of the arrow function

*   allow you to omit the curly braces if you only have one statement

*   return the result of the single statement when curly braces are omitted

For example, here is CoffeeRun’s <samp class="methodname">CheckList.prototype.addClickHandler</samp> method:

```
CheckList.prototype.addClickHandler = function(fn) {
  this.$element.on('click', 'input', function (event) {
    var email = event.target.value;
    fn(email)
      .then( function () {
        this.removeRow(email);
      }.bind(this));
  }.bind(this));
};
```

Replacing the anonymous functions with arrow functions makes this code a bit clearer:

```
CheckList.prototype.addClickHandler = (fn) => {
  this.$element.on('click', 'input', (event) => {
    let email = event.target.value;
    fn(email)
      .then(() => this.removeRow(email));
  });
};
```

The work that <samp class="methodname">addClickHandler</samp> is doing is more apparent without the extra noise of `function` and `.bind(this)`.

# <samp class="chapter_number">18</samp>
<samp class="chapter_name">ES6, the Adventure Continues</samp>

Chattrbox is a working application, but right now it focuses on “under the hood” business logic. It connects to the WebSockets server. It defines a message format and is able to send and receive messages.

In this chapter, you will complete Chattrbox by wiring up the UI layer. You will continue to use <samp class="application">Node</samp> and `npm` to manage your build process and act as a server, and at the end of the chapter you will have a fully functional web-based chat app ([Figure 18.1](#ch18.html_ss-chattrbox-end-of-chapter-preview "Figure 18.1  The completed Chattrbox")).

**Figure 18.1  The completed Chattrbox**

![The completed Chattrbox](Chattrbox/ES6-Babel-2/finished-chattrbox.png)

When you built CoffeeRun, you created <samp class="classname">FormHandler</samp> and <samp class="classname">CheckList</samp> modules that corresponded to the form and the list area. You will use the same pattern with Chattrbox for creating the <samp class="classname">ChatForm</samp> and <samp class="classname">ChatList</samp> modules.

You will also create a <samp class="function">UserStore</samp> module that will hold information about the current chat user. These will make Chattrbox more robust and make its main modules more reusable.

## Installing jQuery as a Node Module

Chattrbox will make use of jQuery for DOM manipulation. But you will not load jQuery from <samp class="uri">cdnjs.com</samp>, as you did for CoffeeRun, nor will you use a `<script>` tag in your HTML, the way you have been integrating client-side dependencies.

With <samp class="application">Browserify</samp>, this is no longer necessary. <samp class="application">Browserify</samp> automatically builds your JavaScript dependencies into your application bundle to be used in your browser. So, all you need to do to integrate jQuery is include it via `import`, and <samp class="application">Browserify</samp> will take care of the rest.

Begin by installing the jQuery library to the <samp class="filename">node_modules</samp> folder:

```
npm install --save-dev jquery
```

Open <samp class="filename">dom.js</samp> to begin writing this module. The <samp class="filename">dom.js</samp> module will use jQuery, so add an `import` statement to include it.

```
import $ from 'jquery';
```

Later in this chapter, you will install and use another third-party library. When you do, you will follow these same steps for installing and importing it.

## Creating the ChatForm Class

As you did with CoffeeRun, you will create an object to manage the form element in the DOM. This will be the <samp class="classname">ChatForm</samp> class. Using ES6 classes will make your code a bit more readable than your code from CoffeeRun.

Creating a <samp class="classname">ChatForm</samp> instance and initializing its event handlers will occur in two separate steps, because a constructor’s job should only be to set the properties of an instance. Other work (like attaching event listeners) should be done in other methods.

Define <samp class="classname">ChatForm</samp> in <samp class="filename">dom.js</samp> with a constructor that accepts selectors. In the constructor, add properties for the elements the instance will need to track.

```
import $ from 'jquery';

class ChatForm {
  constructor(formSel, inputSel) {
    this.$form = $(formSel);
    this.$input = $(inputSel);
  }
}
```

Next, add an <samp class="methodname">init</samp> method that will associate a callback with the form’s `submit` event.

```
...
class ChatForm {
  constructor(formSel, inputSel) {
    this.$form = $(formSel);
    this.$input = $(inputSel);
  }

  init(submitCallback) {
    this.$form.submit((event) => {
      event.preventDefault();
      let val = this.$input.val();
      submitCallback(val);
      this.$input.val('');
    });

    this.$form.find('button').on('click', () => this.$form.submit());
  }
}
```

In the <samp class="methodname">init</samp> method, you used an arrow function for the submit handler. Inside the arrow function, you prevented the default form action, retrieved the value from the input field, and then passed that value to <samp class="function">submitCallback</samp>. Finally, you reset the value of the input.

To make sure the form submits when the button is clicked, you added a click handler that causes the form to fire its `submit` event. You did this by getting the form element with jQuery and then calling jQuery’s <samp class="methodname">submit</samp> method. You used the single-expression version of the arrow function, allowing you to omit the curly braces.

To make this module useful, you need to `export` <samp class="classname">ChatForm</samp>. In the previous chapter, you used `export default` for this purpose. This allowed you to export a single value for the module. In some cases, you used a plain JavaScript object to package up multiple values within that single default value.

In this chapter, you will use <samp class="firstterm">named exports</samp> to export multiple named values instead of a single default value.

Export <samp class="classname">ChatForm</samp> as a named value to users of this module by adding the `export` keyword just before the `class` declaration.

```
...
export class ChatForm {
  constructor(formSel, inputSel) {
    this.$form = $(formSel);
    this.$input = $(inputSel);
  }
  ...
```

Easy enough. Now to import <samp class="classname">ChatForm</samp> in <samp class="filename">app.js</samp>.

In Ottergram and CoffeeRun, you used the `var` keyword for selector strings. In ES6, you can declare constants for this purpose, because the values of the strings will not change. Like `let`, `const` is block-scoped, meaning that it is visible to any code inside the same set of curly braces. When it is outside all curly braces (which will be the case here), it is visible to any code in the same file.

In <samp class="filename">app.js</samp>, import the <samp class="classname">ChatForm</samp> class and create constants for the form’s selector and message input selector. Also, create an instance of <samp class="classname">ChatForm</samp> in <samp class="classname">ChatApp</samp>’s constructor function.

```
import socket from './ws-client';
import {ChatForm} from './dom';

const FORM_SELECTOR = '[data-chat="chat-form"]';
const INPUT_SELECTOR = '[data-chat="message-input"]';

class ChatApp {
  constructor() {
    this.chatForm = new ChatForm(FORM_SELECTOR, INPUT_SELECTOR);

    socket.init('ws://localhost:3001');
    socket.registerOpenHandler(() => {
      let message = new ChatMessage('pow!');
      socket.sendMessage(message.serialize());
    });
    socket.registerMessageHandler((data) => {
      console.log(data);
    });
  }
}
...
```

When you imported <samp class="classname">ChatForm</samp>, you wrapped it in curly braces: `{ChatForm}`. This signifies a <samp class="firstterm">named import</samp>. The named import for <samp class="classname">ChatForm</samp> declares a local variable named `ChatForm` and binds it to the value from the `dom` module of the same name.

### Connecting ChatForm to the socket

In the last chapter, you sent a dummy message: `"pow!"`. Now you are ready to send real form data from <samp class="classname">ChatForm</samp>.

Inside the `socket.registerOpenHandler` callback, you will initialize the <samp class="classname">ChatForm</samp> instance. It is important to do this <samp class="emphasis">after</samp> the socket is open, instead of initializing immediately after creating the instance. By waiting, you prevent your user from entering chat messages before they can actually be sent to the server. (That would be a bad thing.)

Remember that <samp class="classname">ChatForm</samp>’s <samp class="methodname">init</samp> method accepts a callback. This callback will be used to handle form submissions.

In <samp class="filename">app.js</samp>, delete your dummy message code and replace it with a call to `ChatForm.init`, passing it a callback that sends message data coming from <samp class="classname">ChatForm</samp> to your <samp class="varname">socket</samp>.

```
...
class ChatApp {
  constructor() {
    this.chatForm = new ChatForm(FORM_SELECTOR, INPUT_SELECTOR);

    socket.init('ws://localhost:3001');
    socket.registerOpenHandler(() => {
      let message = new ChatMessage('pow!');
      socket.sendMessage(message.serialize());
      this.chatForm.init((data) => {
        let message = new ChatMessage(data);
        socket.sendMessage(message.serialize());
      });
    });
    socket.registerMessageHandler((data) => {
      console.log(data);
    });
  }
}
...
```

Let’s look at what <samp class="classname">ChatApp</samp> is doing now. First, it opens the socket connection to the server. When the connection is open, <samp class="classname">ChatApp</samp> initializes your instance of <samp class="classname">ChatForm</samp> with a form submission callback.

Now, when the user submits a message in the form the <samp class="classname">ChatForm</samp> instance will take that data and send it to <samp class="classname">ChatApp</samp>’s callback, and the callback will then package it up as a <samp class="classname">ChatMessage</samp> and send it to the WebSockets server.

## Creating the ChatList Class

That takes care of sending outgoing chat messages. Your next job is to display new messages from the server as they come in. To do that, you will create a second class in <samp class="filename">dom.js</samp> representing the list of chat messages the user sees.

<samp class="classname">ChatList</samp> will create DOM elements for each message, which will display the name of the user who sent the message and the message text. In <samp class="filename">dom.js</samp>, create and `export` a class definition for a new class called <samp class="classname">ChatList</samp> to fulfill this role:

```
import $ from 'jquery';

export class ChatForm {
  ...
}

export class ChatList {
  constructor(listSel, username) {
    this.$list = $(listSel);
    this.username = username;
  }
}
```

<samp class="classname">ChatList</samp> accepts the attribute selector and the username. It needs the attribute selector so that it knows where to attach the message list elements it creates. And it needs the username so it can see which messages were sent by your user and which were sent by everyone else. (Your messages will be displayed differently from those sent by other users.)

Now that <samp class="classname">ChatList</samp> has a constructor, it also needs to be able to create DOM elements for messages.

Add a <samp class="methodname">drawMessage</samp> method to <samp class="classname">ChatList</samp>. It will expect to receive an object argument, which it will destructure into local variables for the username, timestamp, and text associated with the message. (To make it clearer what the destructuring assignment is doing, single character local variables are used.)

```
...
export class ChatList {
  constructor(listSel, username) {
    this.$list = $(listSel);
    this.username = username;
  }

  drawMessage({user: u, timestamp: t, message: m}) {
    let $messageRow = $('<li>', {
      'class': 'message-row'
    });

    if (this.username === u) {
      $messageRow.addClass('me');
    }

    let $message = $('<p>');

    $message.append($('<span>', {
      'class': 'message-username',
      text: u
    }));

    $message.append($('<span>', {
      'class': 'timestamp',
      'data-time': t,
      text: (new Date(t)).getTime()
    }));

    $message.append($('<span>', {
      'class': 'message-message',
      text: m
    }));

    $messageRow.append($message);
    $(this.listId).append($messageRow);
    $messageRow.get(0).scrollIntoView();
  }
}
```

Your <samp class="methodname">drawMessage</samp> method creates a row for the message with the username, timestamp, and the message itself displayed. If you are the sender of the message, it adds an extra CSS class for styling. It then appends your message’s row to <samp class="classname">ChatList</samp>’s list element and scrolls the new message row into view.

With that, <samp class="classname">ChatList</samp> is ready to rock. Time to integrate it into <samp class="classname">ChatApp</samp>.

In <samp class="filename">app.js</samp>, update the `dom` import statement so that it also imports <samp class="classname">ChatList</samp>. Add a `const` for the list selector, then instantiate a new <samp class="classname">ChatList</samp> in the constructor.

```
import socket from './ws-client';
import {ChatForm, ChatList} from './dom';

const FORM_SELECTOR = '[data-chat="chat-form"]';
const INPUT_SELECTOR = '[data-chat="message-input"]';
const LIST_SELECTOR = '[data-chat="message-list"]';

class ChatApp {
  constructor() {
    this.chatForm = new ChatForm(FORM_SELECTOR, INPUT_SELECTOR);
    this.chatList = new ChatList(LIST_SELECTOR, 'wonderwoman');

    socket.init('ws://localhost:3001');
    ...
```

You are almost up and running. The final step to getting basic chat functionality is to draw new messages as they come in by calling <samp class="methodname">chatList.drawMessage</samp>. Do this in <samp class="methodname">registerMessageHandler</samp> in <samp class="filename">app.js</samp>:

```
...
class ChatApp {
  ...
    socket.registerMessageHandler((data) => {
      console.log(data);
      let message = new ChatMessage(data);
      this.chatList.drawMessage(message.serialize());
    });
  }
}
...
```

You create a new <samp class="classname">ChatMessage</samp> using the incoming data, then you <samp class="methodname">serialize</samp> the <samp class="varname">message</samp>. This is a precautionary step to strip away extra metadata that might have been added to the data. Creating a new <samp class="classname">ChatMessage</samp> from the socket data gives you your message, and <samp class="methodname">this.chatList.drawMessage</samp> draws that <samp class="methodname">serialize</samp> message into your browser.

Time to give it a whirl. If you have not already, start <samp class="application">Watchify</samp> (with `npm run watch`) and `nodemon` (with `npm run dev`). Open or refresh your browser and type in a message ([Figure 18.2](#ch18s03.html_ss-intermediate-1-shark-repellent "Figure 18.2  Seeing your own chat message")).

**Figure 18.2  Seeing your own chat message**

![Seeing your own chat message](Chattrbox/ES6-Babel-2/amazonia-doctor.png)

Hooray! You now have a working chat application. It just needs a few design touches for some polish.

## Using Gravatars

Gravatar is a free service that lets you associate a profile picture with your email address. Gravatar makes each user’s profile image available via a specially formatted URL. For example, [Figure 18.3](#ch18s04.html_ss-gravatar-example-wonderwoman "Figure 18.3  Gravatar image example") shows the Gravatar of one of our test accounts.

**Figure 18.3  Gravatar image example**

![Gravatar image example](Chattrbox/ES6-Babel-2/gravatar-url.png)

See the end of the URL? That is a unique identifier generated from the user’s email address. This identifier is called a <samp class="firstterm">hash</samp> and is easy to generate with the help of a third-party library called `crypto-js`.

Add `crypto-js` to your project using `npm`:

```
npm install --save-dev crypto-js
```

`crypto-js` is now installed in your project’s local `node_modules` folder and ready for use.

When you create strings in JavaScript, you often need to concatenate the string with some other value. ES6 provides a better way to create strings that include values from expressions and variables, called <samp class="firstterm">template strings</samp>. You will use this feature to create the URL for accessing Gravatar images.

In <samp class="filename">dom.js</samp>, add another `import` statement for the `md5` submodule of the `crypto-js` library, using a <samp class="literal">/</samp> to separate the name of the main module and the name of the submodule. Then, write a <samp class="function">createGravatarUrl</samp> function that accepts a username, generates an MD5 hash, and returns the URL for the Gravatar.

```
import $ from 'jquery';
import md5 from 'crypto-js/md5';

function createGravatarUrl(username) {
  let userhash = md5(username);
  return `http://www.gravatar.com/avatar/${userhash.toString()}`;
}
...
```

Take note: In `` return `http://www.gravatar.com/avatar/${userhash.toString()}` ``, those are not single quote characters. They are backticks, located just below the Escape key on most US keyboard layouts.

Inside the backticks, you can use the `${userhash.toString()}` syntax to include JavaScript expression values directly in your string. Here, you refer to the variable <samp class="varname">userhash</samp> and call its <samp class="methodname">toString</samp> method, but any expression is valid inside of the curly brackets.

Next, use this function to display the Gravatar in new messages. At the bottom of <samp class="classname">ChatList</samp>’s <samp class="methodname">drawMessage</samp> method (still in <samp class="filename">dom.js</samp>), create a new image element and set its `src` attribute to the user’s Gravatar.

```
...
    $message.append($('<span>', {
      class: 'message-message',
      text: m
    }));

    let $img = $('<img>', {
      src: createGravatarUrl(u),
      title: u
    });

    $messageRow.append($img);
    $messageRow.append($message);
    $(this.listId).append($messageRow);
    $messageRow.get(0).scrollIntoView();
...
```

Run your chat app, and you should see a Gravatar pop up this time ([Figure 18.4](#ch18s04.html_ss-intermediate-2-shark-repellent "Figure 18.4  Showing a Gravatar")).

**Figure 18.4  Showing a Gravatar**

![Showing a Gravatar](Chattrbox/ES6-Babel-2/great-hera.png)

Sadly, there is no Gravatar for the `wonderwoman` username. As a result, you get the unexciting default Gravatar.

## Prompting for Username

It would be really cool to be Wonder Woman. But it is more cool to be a JavaScript developer using Chattrbox. (Especially because real users actually have Gravatars.) In order to know who is using Chattrbox, you will need to prompt users for their usernames.

It is the responsibility of the <samp class="filename">dom</samp> module to interact with the UI, so create a <samp class="function">promptForUsername</samp> function in <samp class="filename">dom.js</samp>. Add it to the `export`s instead of making it part of <samp class="classname">ChatForm</samp> or <samp class="classname">ChatList</samp>.

```
...
function createGravatarUrl(username) {
  let userhash = md5(username);
  return `http://www.gravatar.com/avatar/${userhash.toString()}`;
}

export function promptForUsername() {
  let username = prompt('Enter a username');
  return username.toLowerCase();
}
...
```

In the <samp class="function">promptForUsername</samp> function, you created a `let` variable to hold the text entered by the user. (The <samp class="function">prompt</samp> function is built into the browser and returns a string.) Then you returned a lowercase version of that text.

Next, you will need to update <samp class="filename">app.js</samp> to use this new function. Update the `import` statement for the <samp class="filename">dom</samp> module and call the <samp class="function">promptForUsername</samp> function to get a value for the <samp class="varname">username</samp> variable:

```
import socket from './ws-client';
import {ChatForm, ChatList, promptForUsername} from './dom';

const FORM_SELECTOR = '[data-chat="chat-form"]';
const INPUT_SELECTOR = '[data-chat="message-input"]';
const LIST_SELECTOR = '[data-chat="message-list"]';

let username = '';
username = promptForUsername();

class ChatApp {
  ...
```

Now, update <samp class="classname">ChatMessage</samp> to use that username as the default. Remember, only messages received from the server have a `data.user` value.

```
...
class ChatMessage {
  constructor({
    message: m,
    user: u='batman', username,
    timestamp: t=(new Date()).getTime()
...
```

Finally, pass the username to the <samp class="classname">ChatList</samp> constructor:

```
...
class ChatApp {
  constructor() {
    this.chatForm = new ChatForm(FORM_SELECTOR, INPUT_SELECTOR);
    this.chatList = new ChatList(LIST_SELECTOR, 'wonderwoman' username);
    ...
```

After the build process completes, reload your browser and enter a username in the prompt ([Figure 18.5](#ch18s05.html_fig-prompt "Figure 18.5  Prompting for a username")).

**Figure 18.5  Prompting for a username**

![Prompting for a username](Chattrbox/ES6-Babel-2/prompt.png)

Now, try sending messages. You should see your selected username echoed back at you, as well as the Gravatar associated with that username ([Figure 18.6](#ch18s05.html_fig-in-the-computer "Figure 18.6  Your user’s name")).

**Figure 18.6  Your user’s name**

![Your user’s name](Chattrbox/ES6-Babel-2/wonder-woman-quotes.png)

Gravatars are assigned using email addresses. If you do not have one associated with your email address, try diana.prince@bignerdranch.com or clark.kent@bignerdranch.com.

## User Session Storage

Typing the username each time you reload the page gets tedious. It would be better to store that username in the browser. For simple storage, the browser provides two APIs for storing key/value pairs (with one limitation – the value must be a string). These are <samp class="firstterm">localStorage</samp> and <samp class="firstterm">sessionStorage</samp>. The data stored in `localStorage` and `sessionStorage` is associated with your web application’s server address. Code from different sites cannot access each other’s data.

Using `localStorage` would work. But you might only want to keep the username until you close the tab or the window, so in this case you will use the `sessionStorage` API. It is just like `localStorage`, but the data is erased when the browsing session ends (either by closing the browser tab or the window).

You will create a new set of classes to manage your `sessionStorage` information.

Create a new file named <samp class="filename">storage.js</samp> in the <samp class="filename">app/scripts/src</samp> folder and add a class definition:

```
class Store {
  constructor(storageApi) {
    this.api = storageApi;
  }
  get() {
    return this.api.getItem(this.key);
  }

  set(value) {
    this.api.setItem(this.key, value);
  }
}
```

Your new <samp class="classname">Store</samp> class is generic and can be used with either `localStorage` or `sessionStorage`. It is a thin wrapper around the Web Storage APIs. You specify which storage API you want to use when you instantiate one.

Notice that there are references to `this.key`, which is <samp class="emphasis">not</samp> set in the constructor. This implementation of <samp class="classname">Store</samp> is not intended to be used on its own. Instead, you use it by building a subclass that defines the `key` property.

Create a subclass, using the `extends` keyword, that you can use for storing the username in `sessionStorage`:

```
class Store {
  constructor(storageApi) {
    this.api = storageApi;
  }
  get() {
    return this.api.getItem(this.key);
  }

  set(value) {
    this.api.setItem(this.key, value);
  }
}

export class UserStore extends Store {
  constructor(key) {
    super(sessionStorage);
    this.key = key;
  }
}
```

<samp class="classname">UserStore</samp> only defines a constructor, which performs two actions. First, it calls <samp class="methodname">super</samp>, which invokes the <samp class="classname">Store</samp>’s constructor, passing it a reference to `sessionStorage`. Second, it sets the value of `this.key`.

Now the value of <samp class="varname">api</samp> is set for the <samp class="classname">Store</samp>, and the value of <samp class="varname">key</samp> is set for the <samp class="classname">UserStore</samp> instance. This means that all the pieces are in place for a <samp class="classname">UserStore</samp> instance to invoke the <samp class="methodname">get</samp> and <samp class="methodname">set</samp> methods.

<samp class="classname">UserStore</samp> will be what <samp class="filename">app.js</samp> will use, so that is what you export here.

Now to use your new <samp class="classname">UserStore</samp>. Import <samp class="classname">UserStore</samp> into <samp class="filename">app.js</samp>, create an instance, and use it to stash the username:

```
import socket from './ws-client';
import {UserStore} from './storage';
import {ChatForm, ChatList, promptForUsername} from './dom';

const FORM_SELECTOR = '[data-chat="chat-form"]';
const INPUT_SELECTOR = '[data-chat="message-input"]';
const LIST_SELECTOR = '[data-chat="message-list"]';

let username = '';
let userStore = new UserStore('x-chattrbox/u');
let username = userStore.get();
if (!username) {
  username = promptForUsername();
  userStore.set(username);
}

class ChatApp {
  ...
```

Run Chattrbox one more time in your browser. This time, you should only be prompted for your username when you initially load the page. Subsequent reloads should have the same username you initially entered.

To confirm that your username is being stored in `sessionStorage`, you can use the resources panel in the DevTools. After you click to activate the resources panel, you will see a list on the left. Click the ![User Session Storage](Chattrbox/ES6-Babel-2/arrow.png) next to the <samp class="guimenuitem">Session Storage</samp> item in the list, revealing [<samp class="uri">http://​localhost:3000</samp>](http://localhost:3000). Click this URL to reveal the data being stored by <samp class="classname">UserStore</samp> ([Figure 18.7](#ch18s06.html_fig-resources-browser "Figure 18.7  The resources panel in the DevTools")).

**Figure 18.7  The resources panel in the DevTools**

![The resources panel in the DevTools](Chattrbox/ES6-Babel-2/resources-browser.png)

At the bottom of this list of key value pairs, there are buttons for refreshing the list and for deleting items from the list. You can use these if you need to manually modify the stored data.

## Formatting and Updating Message Timestamps

Your messages have timestamps that are not very human-friendly. (Seriously, who tells time by the number of milliseconds since January 1, 1970?) To provide nicer timestamps (such as “10 minutes ago”), you will add a module called `moment`. Install it using `npm` and save it as a development dependency:

```
npm install --save-dev moment
```

Each of your messages stores its timestamp as a data attribute. Write an <samp class="methodname">init</samp> method for <samp class="classname">ChatList</samp> that calls the built-in function <samp class="function">setInterval</samp>, which takes two arguments: a function to run and how often that function should be run. Your function will update each message with a human-readable timestamp.

To set the timestamp string, use jQuery in <samp class="filename">dom.js</samp> to find all elements with a `data-time` attribute whose value is the numerical timestamp. Create a new <samp class="classname">Date</samp> object using that numerical timestamp and pass the object to <samp class="function">moment</samp>. Then call the <samp class="methodname">fromNow</samp> method to produce the final timestamp string and set that string as the element’s HTML text.

```
...
  drawMessage({user: u, timestamp: t, message: m}) {
    ...
  }

  init() {
    this.timer = setInterval(() => {
      $('[data-time]').each((idx, element) => {
        let $element = $(element);
        let timestamp = new Date().setTime($element.attr('data-time'));
        let ago = moment(timestamp).fromNow();
        $element.html(ago);
      });
    }, 1000);
  }
}
```

You are running this function every 1,000 milliseconds. To make sure a human-readable timestamp appears immediately, update <samp class="methodname">drawMessage</samp>. Use <samp class="function">moment</samp> to create a formatted timestamp string when the message is first drawn to the chat list.

```
...
  drawMessage({user: u, timestamp: t, message: m}) {
    ...
    $message.append($('<span>', {
      'class': 'timestamp',
      'data-time': t,
      text: (new Date(t)).getTime()
      text: moment(t).fromNow()
    }));
    ...
```

Finally, update <samp class="filename">app.js</samp>, adding a call to `this.chatList.init` inside the `socket.registerOpenHandler` callback:

```
...
class ChatApp {
  constructor () {
    this.chatForm = new ChatForm(FORM_SELECTOR, INPUT_SELECTOR);
    this.chatList = new ChatList(LIST_SELECTOR, username);

    socket.init('ws://localhost:3001');
    socket.registerOpenHandler(() => {
      this.chatForm.init((text) => {
        let message = new ChatMessage({message: text});
        socket.sendMessage(message.serialize());
      });
      this.chatList.init();
    });
    ...
```

Save and let your `npm` scripts compile your changes. Refresh the browser and start chatting. You should see your new timestamps appear with your message text. After a couple of minutes, you will notice that the message timestamps update ([Figure 18.8](#ch18s07.html_ss-chattrbox-final-end-of-chapter "Figure 18.8  Not-so-secret identities")).

**Figure 18.8  Not-so-secret identities**

![Not-so-secret identities](Chattrbox/ES6-Babel-2/finished-chattrbox.png)

You have come to the end of the road with Chattrbox. Though it only spanned a few chapters, it had quite a few moving parts. You learned how to write two kinds of servers in <samp class="application">Node.js</samp>: a basic web server and a WebSocket server. You built the client application using ES6, utilizing <samp class="application">Babel</samp> and <samp class="application">Browserify</samp> to compile your code to ES5 so that Chattrbox can be used in older browsers, and you automated your workflow with `npm` scripts.

Chattrbox is the culmination of the techniques you have learned so far. The next application, Tracker, will introduce you to <samp class="application">Ember.js</samp>, a framework for building large applications. It will build on your hard-won knowledge of modularity, asynchronous programming, and workflow tools.

## Bronze Challenge: Adding Visual Effects to Messages

Give new messages a visual effect. You can fade them in or have them slide in. (Check jQuery’s *Effects* documentation for options.)

For an added challenge, apply this effect only to truly new messages – not to messages already in the chat that are loaded by the app when users first sign on or refresh their browser.

How can you tell which messages are old and which are new? Each message has a data attribute that can help you tell whether it is more than a second or two old.

## Silver Challenge: Caching Messages

If you are in the middle of a chat and need to reload the browser, all of your messages disappear. It is nice that your <samp class="classname">UserStore</samp> remembers your username – but it would be better if you also had a similar mechanism for caching chat messages.

Create a <samp class="classname">MessageStore</samp> that subclasses <samp class="classname">Store</samp>. It should store messages as they come in, making sure not to store the same message more than once.

When the page loads, Chattrbox should get any cached messages from <samp class="classname">MessageStore</samp>. Decide if you would like messages to persist even if the browser tab is closed and re-opened. (If so, what alternative to `sessionStorage` would you use?)

## Gold Challenge: Separate Chat Rooms

This challenge will require you to modify both the server and client applications.

Add separate chat rooms for your users. After they enter their username, prompt them to enter the name of the chat room they would like to use.

When users are logged in to a chat room, they should only receive messages for that room over the WebSocket connection. You might need to change how you store messages on the server, how you send messages to the client, or both.

For an added challenge, show a dropdown of available chat rooms in the client UI so that users can switch from room to room. When changing to another room, make sure that any new messages are received from the server and displayed in the chat list.

# <samp class="part_number">Part IV</samp>
<samp class="part_name">Application Architecture</samp>

# <samp class="chapter_number">19</samp>
<samp class="chapter_name">Introduction to MVC and Ember</samp>

Model-View-Controller (MVC) is an extremely useful software design pattern. It works well in web applications, allowing you to build structure in separate layers. This chapter introduces the MVC pattern and walks you through installing and setting up <samp class="application">Ember</samp>, a framework for MVC. The next few chapters focus on individual pieces of the pattern as you create a new application layer by layer.

There are many interpretations of MVC, especially in the front-end world. [Figure 19.1](#ch19.html_fig-MVC-pattern "Figure 19.1  The Model-View-Controller pattern") shows the interpretation we will use.

**Figure 19.1  The Model-View-Controller pattern**

![The Model-View-Controller pattern](Tracker/MVC/img/MVC.png)

Here is a breakdown of what each layer does:

*   <samp class="emphasis">Models</samp> manage data. When data changes, the model tells anyone who is listening.

*   <samp class="emphasis">Views</samp> manage the user interface. They handle the presentation of models and listen for any changes. Also, when UI events fire in response to user input, they call handler functions in the controller.

*   <samp class="emphasis">Controllers</samp> hold application logic. They retrieve model instances and give them to views. They also contain handler functions that make changes to model instances.

If this seems circular, it is. The three pieces work together. Application data flows from the models to the view. Event data flows from the view to the controller. Controllers trigger data changes in the model based on UI events.

You may be wondering how, then, you get into the circular pattern of MVC. In [Chapter 8](#ch08.html "8 Modules, Objects, and Methods"), you created the CoffeeRun application and enclosed all the functionality you needed in the `Window.App` object. Each added module had a specific role in the application and was named for its functionality. The MVC pattern needs an initial set-up function, like creating a new <samp class="function">Truck</samp>, to load controllers. Controllers, in turn, load models and views.

Your next application, called Tracker, will load an initial DOM state in an HTML file as only an empty `<body>` tag. The scripts to initialize your application will be loaded from this HTML file as well. In the MVC pattern, views (HTML content) are dynamically rendered depending on the route and state of the data (models).

The application you are going to build will require more than CoffeeRun’s seven modules. The MVC pattern helps you break up modules into functionality-specific files and maintain consistent organization – whether you have a dozen modules or a hundred.

## Tracker

Your Tracker application will include <samp class="firstterm">URL routing</samp>, one of the best features of web applications. It will have models to define the data, controllers to handle user actions, templates to define the UI, and routes to assign the models to the templates. As you build the application, you will pick up some new patterns and techniques that will make your code lightweight and elegant.

Your customer for the Tracker application is a cryptozoologist, traveling the world in search of animals like Bigfoot, chupacabras, the Loch Ness Monster, and unicorns. This client wants an app for tracking these mysterious creatures and recording information about any sightings. The requirements may change (and they usually do), but to begin with the user should be able to:

*   list existing sightings

*   add new sightings

*   link creatures to sightings

*   see the latest sightings via flash messages

Each sighting should have the following model data and associations:

| Sighting model attribute | Attribute type |
| --- | --- |
| date creature was seen | date object |
| location | string |
| creature | creature model key |
| witness(es) | array of witness keys |

Each creature should have the following model data:

| Creature model attribute | Attribute type |
| --- | --- |
| name | string |
| type | string |
| image path | string |

And each witness should have the following model data and associations:

| Witness model attribute | Attribute type |
| --- | --- |
| first name | string |
| last name | string |
| full name | string: concatenation of first name and last name |
| email | string |
| sighting(s) | array of sighting keys |

Building Tracker will be slightly different than building the previous applications in this book. It will more closely resemble real-world application development. There will be more code in sections and less instant feedback. However, you will get a realistic sense of app development and will build a satisfyingly complex app ([Figure 19.2](#ch19.html_fig-final-app "Figure 19.2  Finished Tracker app")).

**Figure 19.2  Finished Tracker app**

![Finished Tracker app](Tracker/MVC/img/final-app-img.png)

## Ember: An MVC Framework

As you build Tracker, you will learn the basic pattern of web application development using <samp class="application">Ember</samp>, one of the leading MVC frameworks. <samp class="application">Ember</samp> incorporates concepts and naming conventions that allow for rapid development. As you build your application, you will learn the <samp class="application">Ember</samp> fundamentals.

As described on <samp class="application">Ember</samp>’s homepage ([<samp class="uri">emberjs.com</samp>](http://emberjs.com)), <samp class="application">Ember</samp> is “a framework for building ambitious web applications.” In contrast to a library like jQuery, a framework like <samp class="application">Ember</samp> informs your app’s structure and often includes <samp class="firstterm">scaffolding tools</samp>, which are scripts to create boilerplate files in the correct directories. Since its inception in 2011, the <samp class="application">Ember</samp> community has been building a diverse ecosystem of libraries and tooling to accelerate development.

You will start your <samp class="application">Ember</samp> journey with <samp class="application">Ember CLI</samp>, <samp class="application">Ember</samp>’s tool for scaffolding, development, testing, and building. If you are not familiar with the term <samp class="firstterm">CLI</samp>, it stands for “command-line interface.” You will create a new project, load dependencies, generate your <samp class="application">Ember</samp> objects, and build and run your Tracker application from this tool.

### Installing Ember

To get started, you will need to install some tools.

First, make sure you are using the latest version of <samp class="application">Node.js</samp> (>0.12.0). You can check your version with the terminal command `node --version`. At the time of this writing, <samp class="application">Node</samp> is at version 5.5.0\. (Yeah, that is a large difference from the minimum requirement of 0.12.0\. For more on the history of when and why <samp class="application">Node</samp> jumped from version 0.12.0 to 4.0.0, check out Wikipedia’s article at [<samp class="uri">en.wikipedia.org/​wiki/​Node.js</samp>](https://en.wikipedia.org/wiki/Node.js).)

If necessary, download an updated version of <samp class="application">Node.js</samp> from [<samp class="uri">nodejs.org</samp>](https://nodejs.org).

Once <samp class="application">Node</samp> is up to date, you are ready to install <samp class="application">Ember CLI</samp> using the following terminal command:

```
npm install -g ember-cli@2.4
```

The installation may take a few minutes. If you get this error: `Please try running this command again as root/Administrator`, then there is an issue with owner permissions. **Do not rerun** the install command with `sudo`, as `npm` and `sudo` do not play well together. Instead, run this command: `sudo chown -R $USER /usr/local`. Then rerun the original install command (without sudo).

You may get other errors when you install <samp class="application">Ember CLI</samp> that have to do with incompatibility with your existing system. Most errors have instructions for repairing the install process. Some install errors will require basic internet searches to update existing programs running on your computer. If you need more information, the <samp class="application">Ember CLI</samp> website has a page for common issues at [<samp class="uri">ember-cli.com/​user-guide/​#commonissues</samp>](http://ember-cli.com/user-guide/#commonissues).

Next, install <samp class="application">Bower</samp>, another asset management tool.

```
npm install -g bower
```

<samp class="application">Bower</samp> and `npm` are required to create an <samp class="application">Ember</samp> application.

Next, install the <samp class="application">Ember Inspector</samp> plug-in for <samp class="application">Chrome</samp>. To do this, open <samp class="application">Chrome</samp> and, in the address bar, enter `chrome://extensions/`. At the bottom of the extension page, click <samp class="guilabel">Get more extensions</samp>. Search for “Ember Inspector” ([Figure 19.3](#ch19s02.html_fig-ember-inspector-install "Figure 19.3  Installing the Ember Inspector extension for Chrome")), click <samp class="guibutton">Add to Chrome</samp>, and follow the prompts to install the extension.

**Figure 19.3  Installing the Ember Inspector extension for Chrome**

![Installing the Ember Inspector extension for Chrome](Tracker/MVC/img/extension-ember.png)

<samp class="application">Ember CLI</samp> uses a program called <samp class="application">Watchman</samp> when it is running. <samp class="application">Watchman</samp> is a command-line tool that integrates with browsers to enable live reload of applications.

On a Mac, you can install <samp class="application">Watchman</samp> via <samp class="application">Homebrew</samp>. <samp class="application">Homebrew</samp>, a package manager for OS X, can be downloaded using a terminal command you can copy from its website, [<samp class="uri">brew.sh</samp>](http://brew.sh/). Once <samp class="application">Homebrew</samp> is installed, install <samp class="application">Watchman</samp> (version 3.0.0 or greater) with this terminal command:

```
brew install watchman
```

Instructions for installing <samp class="application">Watchman</samp> on Windows can be found at [<samp class="uri">facebook.github.io/​watchman/​docs/​install.html</samp>](https://facebook.github.io/watchman/docs/install.html)

With that, you have the tools you need to begin your <samp class="application">Ember</samp> project, Tracker.

### Creating an Ember application

<samp class="application">Ember</samp>’s emphasis on conventions and patterns allows you to create an application with minimal code. The framework does a lot of the work behind the scenes, generating a number of objects and events when your application starts. As you build out more of the Tracker app, you will use your own objects in place of the ones <samp class="application">Ember</samp> created for you.

In the terminal, navigate to your projects folder. The command `ember new [project name]` will create a directory and will scaffold all the necessary files to start developing.

Create a new <samp class="application">Ember</samp> app called <samp class="filename">tracker</samp>:

```
ember new tracker
```

Creating a new <samp class="application">Ember</samp> application may take a few minutes. As you can see from the terminal output, some of which is shown below, the `ember new` command creates the base project files and directory structure. Also, it uses `npm` and <samp class="application">Bower</samp> to load external library assets. These libraries are essential to running an <samp class="application">Ember</samp> application and also to running the server to compile, build, and test your application.

```
installing app
  create .bowerrc
  create .editorconfig
  create .ember-cli
  create .jshintrc
  create .travis.yml
  create .watchmanconfig
  create README.md
  create app/app.js
  create app/components/.gitkeep
  create app/controllers/.gitkeep
  create app/helpers/.gitkeep
  create app/index.html
  create app/models/.gitkeep
  create app/router.js
  create app/routes/.gitkeep
  create app/styles/app.css
  create app/templates/application.hbs
  . . .
Successfully initialized git.
Installed packages for tooling via npm.
Installed browser packages via Bower.
```

When <samp class="application">Ember</samp> has finished setting up the Tracker app, verify that everything is working by starting a local server.

### Starting up the server

In a moment, you are going to use the command `ember server` (or `ember s`, for those looking to save a few keystrokes) to build your application and start a server so that you can access it locally. As a convenience, `ember server` watches your files for changes and restarts the build/serve/watch process to make sure you only see the latest code in the browser (much like the `browser-sync` tool you used in Ottergram and CoffeeRun).

<samp class="application">Ember CLI</samp> uses the <samp class="application">Broccoli</samp> program for compilation. If you have programmed in languages like Java or Objective-C, you may think of “compilation” a bit differently than what it means in JavaScript. In this case, <samp class="application">Broccoli</samp> combines all of the JavaScript files needed to run your application, while ensuring that all dependencies are met.

It is time to <samp class="emphasis">fight for the user</samp>. Change directories into the Tracker folder and start up the server:

```
cd tracker
ember server
```

In <samp class="application">Chrome</samp>, open a new browser window and go to `http://localhost:4200` to see your new <samp class="application">Ember</samp> app in action ([Figure 19.4](#ch19s02.html_fig-ember-server "Figure 19.4  Ember server")). You will also want to open the <samp class="guilabel">Ember</samp> tab in the DevTools, as shown.

**Figure 19.4  Ember server**

![Ember server](Tracker/MVC/img/ember-setup_new.png)

As mentioned above, <samp class="application">Ember CLI</samp> will reload the browser page when you make changes to the application files. This is called `Livereload`, and you will see it mentioned in the terminal output as:

```
Livereload server on http://localhost:49152
```

In [Figure 19.4](#ch19s02.html_fig-ember-server "Figure 19.4  Ember server"), notice that both the console and <samp class="application">Ember Inspector</samp> list various components that were generated for you, along with their versions. This book uses version 2.4 of both <samp class="application">Ember</samp> and <samp class="application">Ember Data</samp>. At the time of publication, <samp class="application">Ember CLI</samp> generates a 2.x <samp class="application">Ember</samp> application, as you can see by the version numbers in the figure. If you see version numbers starting with 1.x.x, you may have skipped the step to install or update <samp class="application">Ember-CLI</samp>.

(Note that the `Version` you see after starting a server in the terminal is the version of <samp class="application">Ember CLI</samp>, not the version of the actual <samp class="application">Ember</samp> app you are launching.)

## External Libraries and Addons

<samp class="application">Ember CLI</samp> is set up to offer developers speed in many ways, including adding code from the open-source community. In previous chapters, you added `node` modules to your local environment via `npm`. Earlier in this chapter we discussed loading external libraries via <samp class="application">Bower</samp>, another package manager.

<samp class="application">Ember CLI</samp> works well with both of these package managers. Installing libraries or tools is done with simple commands like:

```
npm install [package name] --save-dev
npm install [package name] --save
bower install [package name] --save
```

When using external libraries, these command-line tools load files to the directories <samp class="filename">bower_components</samp> and <samp class="filename">node_modules</samp>.

You used <samp class="application">Bootstrap</samp> for CoffeeRun, and you are going to start Tracker with it as well. To add <samp class="application">Bootstrap</samp> with <samp class="application">Bower</samp>, enter the following command in the terminal:

```
bower install bootstrap-sass --save
```

You have now loaded the <samp class="application">Bootstrap</samp> library locally, with all its JavaScript and style files. You will roll this library into the <samp class="application">Ember CLI</samp> build process so that you can ship your application with the <samp class="application">Bootstrap</samp> assets your application needs.

The modern web workflow for developing scripts and styles includes compilation. You are going to add a tool to help reduce the complexity of compilation: <samp class="application">ember-cli-sass</samp> will handle converting SCSS stylesheets to CSS during the <samp class="application">Ember CLI</samp> build process. SCSS, commonly referred to as “Sass,” adds many familiar programmatic constructs to your stylesheets like variables, functions, loops, and key/value pairs – without losing the CSS syntax you know and love.

Install <samp class="application">ember-cli-sass</samp> from the terminal:

```
ember install ember-cli-sass
```

<samp class="application">ember-cli-sass</samp> is an example of an <samp class="application">Ember</samp> addon. Addons ([<samp class="uri">www.emberaddons.com</samp>](https://www.emberaddons.com)) are projects that have added external libraries or configuration code, created helpers or components, or done some other type of heavy lifting for you. <samp class="application">Ember CLI</samp> makes it easy to add these existing projects to your project with the `ember install` command.

Note that <samp class="application">Ember CLI</samp> is a relatively new tool, and addons can be out of sync. If you run into problems with a particular addon, visit the issues page at the addon’s GitHub repository.

You have just added the ability to compile SCSS files. Now you need to change the <samp class="filename">app/styles/app.css</samp> to be a `.scss` file. Rename <samp class="filename">app/styles/app.css</samp> to <samp class="filename">app/styles/app.scss</samp>. Restart the <samp class="application">Ember</samp> server when you are done so the new CLI tools initialize.

To test the new CLI tool, you are going to add a SCSS variable to your stylesheet. With a `$` as a prefix, create a name/value pair to test the SCSS compilation in <samp class="filename">app/styles/app.scss</samp>:

```
$bg-color: coral;
html {
  background: $bg-color;
}
```

Check your browser. Your page now displays a background color ([Figure 19.5](#ch19s03.html_fig-ember-sass "Figure 19.5  Compiling SCSS: test")).

**Figure 19.5  Compiling SCSS: test**

![Compiling SCSS: test](Tracker/MVC/img/ember-setup_sass.png)

Next, you will add <samp class="application">Bootstrap</samp> styles and scripts to your project. Earlier you added the SCSS version of <samp class="application">Bootstrap</samp> via `bower install bootstrap-sass`. To add the library to your stylesheet, you will need to import the style library into your file and configure <samp class="application">Ember CLI</samp> to build your application with those assets.

## Configuration

<samp class="application">Broccoli</samp>, the compilation engine we mentioned earlier, requires some configuration when adding new JavaScript and stylesheet assets.

<samp class="application">Ember-CLI</samp> generates a configuration file named <samp class="filename">ember-cli-build.js</samp>. This file is where you can inject dependencies and configure the output structure of your application. For Tracker, you will only be adding external libraries and settings for SCSS compilation.

Open <samp class="filename">ember-cli-build.js</samp>, assign a variable to the directory path to <samp class="filename">bootstrap</samp>, and add <samp class="application">Bootstrap</samp>’s <samp class="filename">stylesheets</samp> directory to the key `includePaths` in the `sassOptions`:

```
...
var EmberApp = require('ember-cli/lib/broccoli/ember-app');

module.exports = function(defaults) {

  var bootstrapPath = 'bower_components/bootstrap-sass/assets/';

  var app = new EmberApp(defaults, {
    // Add options here
    sassOptions: {
      includePaths: [
        bootstrapPath + 'stylesheets'
      ]
    }
  });

  // ... Template comments ...

  // Create paths to bootstrap assets
  // Add assets to app with import
  app.import(bootstrapPath + 'javascripts/bootstrap.js');

  return app.toTree();
};
```

You have added a configuration for <samp class="application">Ember CLI</samp> to look for <samp class="filename">*.scss</samp> files in the <samp class="filename">bower_components/bootstrap-sass/assets/stylesheets</samp> directory. Save your file and restart the <samp class="application">Ember</samp> server so the new configuration can load with the application.

You can now use the `@import` directive in your <samp class="filename">app.scss</samp> file to import <samp class="application">Bootstrap</samp>’s styles:

```
$bg-color: coral;
html {
  background: $bg-color;
}

// ----------------------------
// bootstrap variable overrides
// ----------------------------

// end bootstrap variable overrides
@import 'bootstrap';
```

The `@import` directive adds the contents of <samp class="filename">bootstrap.scss</samp> to <samp class="filename">app.scss</samp>, which will be created by the <samp class="application">Ember CLI</samp> build process. <samp class="application">Bootstrap</samp>’s file is found in the directory <samp class="filename">bower_components/bootstrap-sass/assets/stylesheets/</samp>.

In <samp class="filename">ember-cli-build.js</samp>, you added <samp class="application">Bootstrap</samp>’s JavaScript components to the application build process with `app.import(bootstrapPath + 'javascripts/bootstrap.js');`. An import in the CLI build configuration adds the file to the list of assets to be concatenated into a single `dist/assets/vendor.js` file. <samp class="application">Bootstrap</samp>’s `bootstrap.js` has individual JavaScript modules for collapsing DOM elements, modals, tabs, dropdowns, and many others all in a single file. Adding all the JavaScript components is probably overkill, but in the future you can tweak your <samp class="filename">ember-cli-build.js</samp> configuration to only add the specific components you need.

After you add assets, you should always make sure they are working before you move forward. In the <samp class="filename">app</samp> directory, there is an <samp class="filename">index.html</samp> file – but this is not the place to test your new <samp class="application">Bootstrap</samp> code. This file is mainly for the build process.

Instead, all of your HTML elements will be added to application <samp class="firstterm">templates</samp>, in the <samp class="filename">app/templates</samp> directory. You will learn about templates in greater detail in [Chapter 23](#ch23.html "23 Views and Templates").

For now, add a <samp class="application">Bootstrap</samp> `NavBar` component to <samp class="filename">app/templates/application.hbs</samp>:

```
<h2 id="title">Welcome to Ember</h2>

{{outlet}}
<header>
  <nav class="navbar navbar-default">
    <div class="container-fluid">
      <!-- Brand and toggle get grouped for better mobile display -->
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed"
          data-toggle="collapse" data-target="#top-navbar-collapse">
          <span class="sr-only">Toggle navigation</span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <a class="navbar-brand">Tracker</a>
      </div>

      <!-- Collect the nav links, forms, and other content for toggling -->
      <div class="collapse navbar-collapse" id="top-navbar-collapse">
        <ul class="nav navbar-nav">
          <li>
            <a href="#">Test Link</a>
          </li>
          <li>
            <a href="#">Test Link</a>
          </li>
        </ul>
      </div><!-- /.navbar-collapse -->
    </div><!-- /.container-fluid -->
  </nav>
</header>
<div class="container">
  {{outlet}}
</div>
```

You have added <samp class="application">Bootstrap</samp>’s `NavBar` component with specific HTML attributes: IDs, class names, and data attributes. Also, the existing `{{outlet}}` has been moved from the main containing element to inside a `<div>` element. This piece of code is how templates nest child templates. You will learn more about the `{{outlet}}` in the next chapter.

The result of your code is shown in [Figure 19.6](#ch19s04.html_fig-testing-bootstrap-style "Figure 19.6  Bootstrap NavBar").

**Figure 19.6  Bootstrap `NavBar`**

![Bootstrap NavBar](Tracker/MVC/img/ember-setup_bootstrap.png)

The `NavBar` component is responsive and shows a collapse button when the browser window is less than 768px wide. This button responds to click events by opening and closing the list of links ([Figure 19.7](#ch19s04.html_fig-testing-bootstrap-collapse "Figure 19.7  Testing Bootstrap NavBar's collapse component")). The event listener setup for the collapse feature is the code written in the `bootstrap.js` file.

**Figure 19.7  Testing Bootstrap `NavBar`'s collapse component**

![Testing Bootstrap NavBar's collapse component](Tracker/MVC/img/ember-setup_bootstrap-open-nav.png)

Congratulations – you have an <samp class="application">Ember</samp> app up and running! You installed tools to generate code, compile assets, load dependencies, and serve the app. You now have a solid starting point for building the rest of your app in upcoming chapters.

## For the More Curious: npm and Bower Install

The options `--save-dev` and `--save` at the end of the commands `npm install` and `bower install` add key/value pairs of library names and versions to a JSON for each tool. In the case of <samp class="application">Bower</samp>, the JSON is <samp class="filename">bower.json</samp>; for `npm` – as you saw in Chattrbox – it is <samp class="filename">package.json</samp>.

For example, in <samp class="filename">bower.json</samp> the key/value pairs added in this chapter were:

```
{
  "name": "tracker",
  "dependencies": {
    "ember": "~2.4.3",
  }
}
```

The file <samp class="filename">bower.json</samp> lists the dependency `ember.js` with its minimum version number. The libraries and assets listed will not be saved to your development project repository or version control system, only the <samp class="filename">bower.json</samp> file. A developer who checks out the code can run `bower install` and `npm install` to create a local environment for development.

## Bronze Challenge: Limiting Imports

Change <samp class="filename">ember-cli-build.js</samp> to only import the <samp class="filename">collapse.js</samp> and <samp class="filename">transition.js</samp> files. When you do this, your <samp class="filename">vendor.js</samp> will be smaller in size and your `NavBar` component will still work.

Before you make any changes, find <samp class="filename">dist/assets/vendor.js</samp> and note the number of lines of code (or file size). Make the change and compare the new file size.

## Silver Challenge: Adding Font Awesome

Font Awesome is a UI library for adding commonly used icons to your project. The icons can be scaled, just like a font. Add Font Awesome with <samp class="application">Ember CLI</samp> addons and add an icon to <samp class="filename">app/templates/application.hbs</samp>. Check out the addon’s GitHub repository for more information.

## Gold Challenge: Customizing the NavBar

<samp class="application">Bootstrap</samp> is written in SCSS and makes liberal use of variables and functions. When you use the SCSS version in your project, you can control how the library compiles its style rules. You can even create <samp class="application">Bootstrap</samp> themes to modify the default variables.

Change the `background-color`, `border-radius`, and `padding` value of the `NavBar` by only adding or changing variables in your <samp class="filename">app/stylesheets/app.scss</samp>.

# <samp class="chapter_number">20</samp>
<samp class="chapter_name">Routing, Routes, and Models</samp>

At this point, you have the shell for your Tracker application. Now you need to decide what pages – or <samp class="firstterm">routes</samp> – your application will contain.

Routing is like a traffic cop: When a user pulls up a specific URL, routing directs the user to the data that makes up that page. In earlier projects, you built event listeners for form submission and button clicks. Routing is like an event listener, but it watches for changes to the current URL.

Every website uses some form of routing. For example, if you go to [<samp class="uri">www.bignerdranch.com/​we-teach/</samp>](https://www.bignerdranch.com/we-teach/), the server maps the route `/we-teach/` to the HTML files in a folder on the server named `we-teach`. Other servers may do it differently: Instead of retrieving static HTML files, they may run a function that outputs some HTML.

An <samp class="application">Ember</samp> app can do the same thing, but without asking a server for the HTML. When your app needs to go to a different screen, it will update the URL with a new route name. The `Router`, which is a child of the main application object, has event listeners and handlers for URL changes. Using the new route, it does a lookup in its routing table and finds an `Ember.Route` object. The `Router` then calls a series of methods from this route object, which starts the process of getting the data needed for the next screen. This process of callbacks is called <samp class="firstterm">route lifecycle hooks</samp>.

Creating routes is fundamental to <samp class="application">Ember</samp> development. <samp class="application">Ember</samp>’s naming conventions assume you will be creating associated controllers and templates with names that match your routes. So, for example, when you create a route called `sightings`, the router will map a request for `/sightings` to `SightingsRoute`, which in turn sets up a `SightingsController` and, finally, renders a <samp class="filename">app/templates/sightings.hbs</samp> template.

In this chapter, you will learn about <samp class="application">Ember</samp> application constructs and use <samp class="application">Ember CLI</samp> to create Tracker’s route module files and templates. Routes are the key to an <samp class="application">Ember</samp> application, and work in this chapter will set you up to develop your app over the next five chapters.

[Figure 20.1](#ch20.html_fig-index-model-listing "Figure 20.1  Tracker app") shows Tracker at the end of this chapter.

**Figure 20.1  Tracker app**

![Tracker app](Tracker/Routing-Routes-Models/img/sightings-index-route-model.png)

## ember generate

<samp class="application">Ember CLI</samp> provides a scaffolding tool called `generate` that can be useful while you are learning <samp class="application">Ember</samp>’s conventions and naming patterns. You will use `ember generate`, or `ember g` for short, to create files and add boilerplate code to your project.

Recall that Tracker’s purpose is to record sightings of cryptids – creatures like the Sasquatch. It will track information about sighting events, cryptids, and witnesses. It will need quite a few routes:

| Route | Route path | Route data |
| --- | --- | --- |
| index | /index | no data – redirects to sightings |
| sightings | /sightings | list of sightings |
| cryptids | /cryptids | list of cryptids |
| witnesses | /witnesses | list of witnesses |
| sighting | /sighting | individual sighting details |
| cryptid | /cryptid | individual cryptid details |
| witness | /witness | individual witness details |
| sightings index | /sightings/index | landing page for sightings list |
| sightings new | /sightings/new | form to create new sighting |
| sighting index | /sighting/:sighting_id/index | landing page for individual sighting |
| sighting edit | /sighting/:sighting_id/edit | form to edit individual sighting |

You will create all of these with `ember generate`. Open the terminal and navigate to your <samp class="filename">tracker</samp> directory. Run the following commands, one line at a time, to generate your routes:

```
ember g route index
ember g route sightings
ember g route sightings/index
ember g route sightings/new
ember g route sighting
ember g route sighting/index
ember g route sighting/edit
ember g route cryptids
ember g route cryptid
ember g route witnesses
ember g route witness
```

This will look something like [Figure 20.2](#ch20.html_fig-generating-routes "Figure 20.2  Generating routes").

**Figure 20.2  Generating routes**

![Generating routes](Tracker/Routing-Routes-Models/img/ember-g-routes.png)

Now, take a look at what `ember g` created for you. You should have new files under the `routes/` and `templates/` directories.

Open <samp class="filename">app/routes/index.js</samp> and notice that the module `import`s `Ember` and `export`s an `Ember.Route`:

```
import Ember from 'ember';

export default Ember.Route.extend({
});
```

The method <samp class="methodname">.extend</samp> creates a new subclass of an `Ember.Route` and accepts a JavaScript object as its argument. Using the ES6 module syntax, you can create individual modules for each route.

<samp class="application">Ember CLI</samp> will automatically find the `Ember.Route` module you just created and import it into your app – whether you use the `generate` command, as you did here, or create modules manually. `generate` is convenient because it adds some boilerplate code to the file.

Open <samp class="filename">app/templates/index.hbs</samp>, which <samp class="application">Ember CLI</samp> also generated for you. This template will be used for the `IndexRoute`. It has a single line in it: `{{outlet}}`.

You probably remember this bit of code from the last chapter, when you were editing the `templates/application.hbs` file. This helper allows templates to nest content between routes. You will learn more about the `{{outlet}}` helper shortly.

For now, leave this line in <samp class="filename">app/templates/index.hbs</samp> alone and add an HTML `<h1>` element above it:

```
<h1>Index Route</h1>
{{outlet}}
```

Now start up the app with `ember server`. Leave the server running while working on your project. If you need to interact with the <samp class="application">Ember CLI</samp> (for example, to generate more modules), just open a second terminal window. The server will load the new modules into your <samp class="application">Ember</samp> app and reload your browser.

In <samp class="application">Chrome</samp>, navigate to `http://localhost:4200`. Your app should look like [Figure 20.3](#ch20.html_fig-index-route "Figure 20.3  Index route").

**Figure 20.3  Index route**

![Index route](Tracker/Routing-Routes-Models/img/routing-index-route.png)

You should see the `NavBar` elements from <samp class="filename">app/templates/application.hbs</samp> and the `<h1>` element from <samp class="filename">app/templates/index.hbs</samp>. How did this element get here?

When you created your application, a number of files were generated for you, including <samp class="filename">app.js</samp> and <samp class="filename">router.js</samp>. The <samp class="filename">app.js</samp> file is the starting point for your application, and it handles things like initialization. It has functions to create a new <samp class="application">Ember</samp> app, much like creating a new <samp class="function">Truck</samp> in CoffeeRun.

In particular, the <samp class="application">Ember</samp> app will instantiate a `Router` object and an `ApplicationRoute` object when the application is loaded or restarted. These two <samp class="application">Ember</samp> objects control your application.

In your <samp class="filename">router.js</samp> file, you will register `routes` to associate URLs with specific pages. Each `route` can be configured with a few options. You can even create nested routes. This powerful feature of <samp class="application">Ember</samp> lets you reuse content and logic on different screens.

Open <samp class="filename">router.js</samp> and take a look at the method that registers your routes:

```
import Ember from 'ember';
import config from './config/environment';

const Router = Ember.Router.extend({
  location: config.locationType
});

Router.map(function() {
  this.route('sightings', function() {
    this.route('new');
  });
  this.route('sighting', function() {
    this.route('edit');
  });
  this.route('cryptids');
  this.route('cryptid');
  this.route('witnesses');
  this.route('witness');
});

export default Router;
```

<samp class="methodname">Router.map</samp> is being passed a callback. Inside this callback, the <samp class="methodname">route</samp> method registers your routes. This method also takes callbacks. <samp class="application">Ember</samp> converts these nested callbacks into a hierarchy of routes. At the top of this hierarchy is the `ApplicationRoute`.

When you visit the URL for a nested route, <samp class="application">Ember</samp> uses the HTML from the parent template. Inside that parent template, it will look for an `{{outlet}}` helper, which indicates “This is where you should put the HTML from the child template.”

Let’s see how this works in your app.

<samp class="application">Ember</samp> renders the content of the `ApplicationRoute` with the content of the `IndexRoute` nested inside. Behind the scenes, <samp class="application">Ember</samp> is checking for a file called <samp class="filename">index.js</samp> in the `routes/` folder of your project. You can create a landing page for any route by creating an <samp class="filename">index.js</samp> in the corresponding folder. In fact, this is a common practice that you should use in your own <samp class="application">Ember</samp> apps.

You may have noticed that there are no references to `index` routes in <samp class="filename">router.js</samp>. <samp class="application">Ember</samp> autogenerates the `index` route for all parent routes with nested child routes, just as though they appeared in <samp class="filename">router.js</samp>:

```
...
Router.map(function() {
  this.route('index');
  this.route('sightings', function() {
    this.route('index');
    this.route('new');
  });
  this.route('sighting', function() {
    this.route('index');
    this.route('edit');
  });
  this.route('cryptids');
  this.route('cryptid');
  this.route('witnesses');
  this.route('witness');
});
...
```

## Nesting Routes

Routes allow you to structure data in views. Like folders, nested routes group together related routes under a base URL. It is helpful to think of parent routes as representing nouns and child routes as representing verbs or adjectives:

```
// Parent route is noun
this.route('sightings', function() {
  // Child route is verb or adjective
  this.route('new');
});
```

`sightings` is a parent route representing <samp class="emphasis">sightings</samp>, which are things (nouns), and `new` is a nested route representing the action of <samp class="emphasis">creating</samp> a sighting (a verb). <samp class="methodname">this.route</samp> is used to build up the URL including the parent and child.

With template nesting, parts of your site can be rendered on all routes (such as navigation), while others will only show on more specific routes (like `IndexRoute` on the root URL). You will instruct each route on how to retrieve its data using callback functions.

Now, you are going to edit some of the template files you generated along with your routes and navigate to different pages of your application. The code you are adding in this section is temporary, but it will allow you to see the relationship between your routes.

To begin, open the <samp class="filename">app/templates/sightings.hbs</samp> template file and add an `<h1>` element above the existing `{{outlet}}` helper.

```
<h1>Sightings</h1>
{{outlet}}
```

Next, edit the <samp class="filename">app/templates/sightings/index.hbs</samp> template. Add another `<h1>` element, and this time delete the `{{outlet}}` helper. Parent templates use `{{outlet}}` to nest child views. <samp class="filename">app/templates/sightings/index.hbs</samp> is a child template without any nested route, so it does not need an `{{outlet}}` helper.

```
{{outlet}}
<h1>Index Route</h1>
```

Save your files and point your browser to [<samp class="uri">http://​localhost:4200/​sightings/</samp>](http://localhost:4200/sightings/) to see the results ([Figure 20.4](#ch20s02.html_fig-sightings-nested-routes "Figure 20.4  Sightings: nested routes")).

**Figure 20.4  Sightings: nested routes**

![Sightings: nested routes](Tracker/Routing-Routes-Models/img/sightings-index-route.png)

Next, edit <samp class="filename">app/templates/sightings/new.hbs</samp>. This route tree also ends with this child route, so delete `{{outlet}}` and add an `<h1>` element.

```
{{outlet}}
<h1>New Route</h1>
```

Now, change the URL in your browser to `http://localhost:4200/sightings/new` ([Figure 20.5](#ch20s02.html_fig-sightings-new-route "Figure 20.5  Sightings: new route")).

**Figure 20.5  Sightings: new route**

![Sightings: new route](Tracker/Routing-Routes-Models/img/sightings-new-route.png)

Your Tracker app now has nested routes rendering a template for the parent <samp class="filename">app/templates/sightings.hbs</samp> file and for each child: <samp class="filename">app/templates/sightings/index.hbs</samp> and <samp class="filename">app/templates/sightings/new.hbs</samp>. The parent template uses `{{outlet}}` to nest the views.

## Ember Inspector

The <samp class="application">Ember Inspector</samp> gives you an easy way to see all of your application’s routes. Click the `Routes` menu item in the <samp class="application">Ember Inspector</samp> to see them ([Figure 20.6](#ch20s03.html_fig-route-structure "Figure 20.6  Route structure")).

**Figure 20.6  Route structure**

![Route structure](Tracker/Routing-Routes-Models/img/ember-dev-tool-routes.png)

That is a lot of routes! Even more than you generated. Notice that there are numerous routes ending in `loading` and `error`. These are autogenerated routes for the lifecycle states of loading data in routes. Like `index` routes, these objects are created by <samp class="application">Ember</samp> to fill gaps to get from one route state to another route state.

## Assigning Models

The next step is to get data to each route using the route’s model callback. Each `Ember.Route` has a method to assign a model (which, remember, is the data backing the template) to a controller. This method, called <samp class="methodname">model</samp>, returns data as a `Promise`.

Under the hood, the <samp class="application">Ember</samp> app initializes the `Route` object when the URL changes. This `Route` object has four <samp class="firstterm">hooks</samp> to set itself up: <samp class="methodname">beforeModel</samp>, <samp class="methodname">model</samp>, <samp class="methodname">afterModel</samp>, and <samp class="methodname">setupController</samp>.

We will focus on the <samp class="methodname">model</samp> callback for now.

Add some dummy data in the <samp class="methodname">model</samp> callback in the `SightingsRoute`, <samp class="filename">app/routes/sightings.js</samp>:

```
import Ember from 'ember';

export default Ember.Route.extend({
  model(){
    return [
      {
        id: 1,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      },
      {
        id: 2,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      },
      {
        id: 3,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      },
      {
        id: 4,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      },
      {
        id: 5,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      },
      {
        id: 6,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      }
    ];
  }
});
```

Notice the syntax of the <samp class="methodname">model</samp> hook:

```
model() {
  [your code goes here]
}
```

This is ES6 shorthand for:

```
model: function() {
  [your code goes here]
}
```

Throughout the next chapters you will be using this syntax to define your object methods in <samp class="application">Ember</samp>.

The <samp class="methodname">model</samp> callback is a place to retrieve data needed to render a template. The route lifecycle methods in an `Ember.Route` return objects for each hook. The <samp class="methodname">model</samp> hook will eventually return data to a <samp class="methodname">setupController</samp> hook, which sets a property named `model` on `SightingsController`. You can access this data in your templates: <samp class="filename">app/templates/sightings.hbs</samp> and <samp class="filename">app/templates/sightings/index.hbs</samp>.

Edit <samp class="filename">app/templates/sightings/index.hbs</samp> as shown. We will explain the code after you enter it.

```
<h1>Index Route</h1>
<div class="panel panel-default">
  <ul class="list-group">
    {{#each model as |sighting|}}
      <li class="list-group-item">
        {{sighting.location}} - {{sighting.sightedAt}}
      </li>
    {{/each}}
  </ul>
</div>
```

This code might look strange if you have never used template languages. The words in the double curlies (`{{ }}`) are essentially JavaScript functions disguised as statements. In English, these lines say, “For each `sighting` in the `model` property (which is expected to be an array), render an `<li>` element with the `sighting`’s `location` and `sightedAt` date.”

You will learn about `{{ }}` syntax in general and `{{#each}}` in particular in [Chapter 23](#ch23.html "23 Views and Templates").

Switch to [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings) in your browser, where your app should look like [Figure 20.7](#ch20s04.html_fig-index-model-listing2 "Figure 20.7  Index model listing").

**Figure 20.7  Index model listing**

![Index model listing](Tracker/Routing-Routes-Models/img/sightings-index-route-model.png)

You have now completed the first half of the route cycle by passing data to the template for it to display. In the next chapter, you will explore the <samp class="application">Handlebars</samp> templating language. This language allows you represent the state of your application with properties from a controller, rendering only necessary DOM elements as the state of the application changes.

## beforeModel

As described above, the route object calls a sequence of functions, starting with <samp class="function">beforeModel</samp>. This function is a good place to check the state of the application before retrieving data. It is also a good place to reroute a user who cannot be on a page, such as to check for user authentication.

You will use <samp class="function">beforeModel</samp> to unconditionally transition the user to a new page. The `IndexRoute` is a good place to do this. You may want to add a dashboard in the future, but for now the landing page will be `sightings`.

In <samp class="filename">app/routes/index.js</samp>, add a <samp class="function">beforeModel</samp> callback:

```
import Ember from 'ember';

export default Ember.Route.extend({
  beforeModel(){
    this.transitionTo('sightings');
  }
});
```

Now, when you navigate to [<samp class="uri">http://​localhost:4200/</samp>](http://localhost:4200/) the URL changes to [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings), and you should see the sightings list from <samp class="filename">app/templates/sightings/index.hbs</samp>.

The last two routing hooks, <samp class="methodname">afterModel</samp> and <samp class="methodname">setupController</samp>, will not be used in Tracker. When creating a `route` file, you are cloning the `Ember.Route` object and overwriting the method, much like an interface in languages like Java. The <samp class="methodname">setupController</samp> hook will run by default to set the <samp class="methodname">model</samp> property on the route object’s `controller`.

At this point, your application has some basic routes that outline its functionality: a landing page, a list of sightings, and a route for adding a new sighting. You created templates for your routes and added model data to the `sightings` route. You rerouted the index route to the sightings index. You are off to a great start!

In the next chapter, you will learn about `Ember.Model`s, adapters, computed properties, and storage mechanisms.

## For the More Curious: setupController and afterModel

The hook <samp class="methodname">setupController</samp> is for setting properties on a controller that will render those properties. It is possible to run the default behavior of setting the `controller`’s `model` property while setting other active `controller` properties with `this._super`:

```
setupController(controller, model) {
  this._super(controller, model);
  // this.controllerFor('[other controller]').set("[property name]", [value]);
}
```

The hook <samp class="methodname">afterModel</samp> is run after the <samp class="methodname">model</samp> hook (which is a `Promise`) is resolved. Note that there are special cases where the <samp class="methodname">model</samp> hook would not be called because the `Promise` has already been resolved. In these cases, <samp class="methodname">afterModel</samp> is called before <samp class="methodname">setupController</samp> and can be used as a method to test the integrity of the model data before passing it to the `controller`.

# <samp class="chapter_number">21</samp>
<samp class="chapter_name">Models and Data Binding</samp>

For the next part of the Tracker app, you will focus only on the data layer.

You have already worked quite a bit with data in the form of object literals. You have created and modified objects and their properties, and you have created functions to quickly make objects with default values. You know how to store data in `localStorage` and `sessionStorage`.

In Tracker, you are going to work with data in the form of models. Models are essentially functions that create objects with specific properties and methods. They are the architecture of data flowing through your application.

<samp class="application">Ember</samp> has an object class that can take care of your initial need to define your app’s data architecture: <samp class="classname">Ember.Object</samp>. All <samp class="application">Ember</samp> classes inherit from this class. With a simple definition and naming pattern, <samp class="application">Ember</samp> gives you the power to create, retrieve, update, and destroy model instances while the app is running.

However, for your modern application you need more than what <samp class="classname">Ember.Object</samp> provides. Your models need to be able to persist themselves when business logic asks them to retrieve or save data from a data source.

Enter <samp class="firstterm">Ember Data</samp>, a JavaScript library built on top of <samp class="classname">Ember.Object</samp>, which will help you add model-specific functionality. <samp class="application">Ember Data</samp> adds classes built on <samp class="classname">Ember.Object</samp> that abstract the complexity of working with various data sources: `RESTful APIs`, `localStorage`, and even static fixture data.

<samp class="application">Ember Data</samp> also adds an in-memory store for data. The data store is where you create, retrieve, update, and delete your model instances.

## Model Definitions

<samp class="application">Ember CLI</samp> has already loaded the <samp class="application">Ember Data</samp> library, so you are ready to build your models.

In the last chapter, you used `ember g route [route name]` to make <samp class="application">Ember CLI</samp> create route files for you. You can also use `ember generate` to create a model file with the command `ember g model [model name]`.

Create the model files you will need to back your routes for cryptids, sightings, and witnesses:

```
ember g model cryptid
ember g model sighting
ember g model witness
```

Cryptids will have a model definition in the file <samp class="filename">app/models/cryptid.js</samp>. Open this file and add attributes for name, cryptid type (species), profile image, and sightings to the `cryptid` model:

```
import DS from 'ember-data';

export default DS.Model.extend({
  name: DS.attr('string'),
  cryptidType: DS.attr('string'),
  profileImg: DS.attr('string'),
  sightings: DS.hasMany('sighting')

});
```

<samp class="application">Ember Data</samp>, referenced here as `DS` (for “data store”), has an <samp class="methodname">attr</samp> method that is used to specify model attributes. When data is parsed from the source, <samp class="methodname">attr</samp> returns the value. If you give <samp class="methodname">attr</samp> an attribute type, it will be coerced to that type. If you do not set the attribute type, your data will be passed through to the appropriate key unchanged.

There are a few attribute types built in: <samp class="type">string</samp>, <samp class="type">number</samp>, <samp class="type">boolean</samp>, and <samp class="type">date</samp>. You can also create custom model attributes using `transforms`, which you will learn about in [Chapter 22](#ch22.html "22 Data – Adapters, Serializers, and Transforms").

<samp class="methodname">attr</samp> can also take a second argument to specify default values. This optional argument is a hash with a single key: <samp class="varname">defaultValue</samp>. Here are some examples:

```
name: DS.attr('string', {defaultValue: 'Bob'}),
isNew: DS.attr('boolean', {defaultValue: true}),
createdAt: DS.attr('date', {defaultValue: new Date()}),
numOfChildren: DS.attr('number', {defaultValue: 1})
```

In the cryptid definition, you used the <samp class="type">string</samp> attribute type for the <samp class="varname">name</samp>, <samp class="varname">cryptidType</samp>, and <samp class="varname">profileImg</samp> attributes. (Why a <samp class="type">string</samp> type for <samp class="varname">profileImg</samp>? It will reference the image path, not the image itself.)

The <samp class="varname">sightings</samp> attribute uses a different method to define its data: <samp class="methodname">hasMany</samp>. This method is part of <samp class="application">Ember Data</samp>’s relationship methods. When you query a `RESTful API` for a cryptid, it will have associated sightings. That association will be returned as an array of sighting <samp class="varname">id</samp>s referencing an instance of a sighting model.

<samp class="application">Ember Data</samp> has methods to handle one-to-one, one-to-many, and many-to-many relationship types:

| Relationship | “Owning” model | “Owned” model |
| --- | --- | --- |
| one-to-one | <samp class="methodname">DS.hasOne</samp> | <samp class="methodname">DS.belongsTo</samp> |
| one-to-many | <samp class="methodname">DS.hasMany</samp> | <samp class="methodname">DS.belongsTo</samp> |
| many-to-many | <samp class="methodname">DS.hasMany</samp> | <samp class="methodname">DS.hasMany</samp> |

The first argument is the model to associate. In your app, a cryptid will have many <samp class="varname">sighting</samp> instances (you would be surprised how often people see these creatures). The second argument is an optional hash which, similar to <samp class="methodname">attr</samp>’s second argument, is a configuration object to set values when evaluating the function. It contains an `async` key and a value (with a default of `true`).

Model relationships could require requests to a server to retrieve other model data. For cryptids, a request to `sightings` is needed to display sighting data for each cryptid. The same is true for the inverse relationship of sightings <samp class="emphasis">belonging to</samp> a cryptid. The default value, `async: true`, requires a separate request and API endpoint to retrieve the linked data.

If your API has the ability to send all the data together, you can set the `async` value to `false`. For the Tracker app, leave the value as the default, `true`.

Next, open the model for witnesses in <samp class="filename">app/models/witness.js</samp> and add attributes for a witness’s first and last name, email address, and recorded sightings:

```
import DS from 'ember-data';

export default DS.Model.extend({
  fName: DS.attr('string'),
  lName: DS.attr('string'),
  email: DS.attr('string'),
  sightings: DS.hasMany('sighting')
});
```

You defined a witness to be an object that contains a first name (<samp class="varname">fName</samp>), a last name (<samp class="varname">lName</samp>), an email address (<samp class="varname">email</samp>), and a many-to-many relationship to sightings (<samp class="varname">sightings</samp>).

Finally, open your third model file: <samp class="filename">app/models/sighting.js</samp>. Add attributes to your `sightings` model for the who, what, where, and when of the sighting as well as the date the sighting was recorded:

```
import DS from 'ember-data';

export default DS.Model.extend({
  location: DS.attr('string'),
  createdAt: DS.attr('date'),
  sightedAt: DS.attr('date'),
  cryptid: DS.belongsTo('cryptid'),
  witnesses: DS.hasMany('witness')
});
```

Sightings are defined much like witnesses and cryptids, with basic properties defined as strings. The <samp class="varname">location</samp> is a value the user will input in the app, while <samp class="varname">createdAt</samp> and <samp class="varname">sightedAt</samp> will be added server-side when the sighting has been added to the database.

The relationship for the property <samp class="varname">cryptid</samp> is something new, <samp class="methodname">DS.belongsTo('cryptid')</samp>. This method is a one-to-many relationship linking a <samp class="varname">cryptid</samp> instance to the <samp class="varname">sighting</samp> instance – one-to-many because each cryptid will have many sightings.

## createRecord

When the application initializes, <samp class="application">Ember Data</samp> creates `store`, a local store object. `this.store` is the object that will create, retrieve, update, and delete all of the Tracker app’s model records. <samp class="application">Ember</samp> injects the `store` object in all `Routes`, `Controllers`, and `Components`. In the scope of route methods, you have access to the `store` from `this`.

To create a record, you will call <samp class="methodname">this.store.createRecord</samp>. This method expects two arguments: a model name, as a string, and record data, as an object.

Open <samp class="filename">app/routes/sightings.js</samp>. Delete your dummy sightings and create three new <samp class="varname">sighting</samp> records, each with a <samp class="varname">location</samp> value as a string and a <samp class="varname">sightedAt</samp> value as a <samp class="methodname">new Date</samp>:

```
import Ember from 'ember';

export default Ember.Route.extend({
  model() {
    return [
      {
        id: 1,
        location: 'Asilomar',
        sighted_at: new Date('2016-03-07')
      },
      ...
      {
        id: 6,
        location: 'Asilomar',
        sightedAt: new Date('2016-03-07')
      }
    ];
    let record1 = this.store.createRecord('sighting', {
      location: 'Atlanta',
      sightedAt: new Date('2016-02-09')
    });

    let record2 = this.store.createRecord('sighting', {
      location: 'Calloway',
      sightedAt: new Date('2016-03-14')
    });

    let record3 = this.store.createRecord('sighting', {
      location: 'Asilomar',
      sightedAt: new Date('2016-03-21')
    });

    return [record1, record2, record3];
  }
});
```

In [Chapter 20](#ch20.html "20 Routing, Routes, and Models"), the `sightings` route model returned an array. Instead of returning JavaScript objects, you have created three sighting records and returned these records in an array. Run `ember server`, if it is not running already, to see your new records on the `sightings` route, [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings) ([Figure 21.1](#ch21s02.html_fig-sightings-atlanta "Figure 21.1  create sightings")).

**Figure 21.1  `create` sightings**

![create sightings](Tracker/Models/img/model-sightings-atlanta.png)

This example shows that creating <samp class="application">Ember Data</samp> models is very similar to creating JavaScript objects. The advantage to having <samp class="application">Ember Data</samp> model objects is all the methods these objects give you. Let’s start with <samp class="methodname">get</samp> and <samp class="methodname">set</samp>.

## get and set

At the core of <samp class="application">Ember Data</samp>’s model records is an <samp class="classname">Ember.Object</samp>. This object definition contains the methods <samp class="methodname">get</samp> and <samp class="methodname">set</samp>. Unlike most languages, JavaScript does not force the use of getters and setters on object instances. <samp class="application">Ember</samp> applies the concepts of getters and setters with these methods to force a function to be run when changing an object property. This allows <samp class="application">Ember</samp> to add event triggers to <samp class="methodname">set</samp> and make programmers be intentional when getting properties.

The <samp class="methodname">get</samp> method takes a single argument, the property name, to retrieve the property value. Try it out in the <samp class="filename">app/routes/sightings.js</samp> `model` callback.

```
import Ember from 'ember';

export default Ember.Route.extend({
  model() {
    let record1 = this.store.createRecord('sighting', {
      location: 'Atlanta',
      sightedAt: new Date('2016-02-09')
    });
    console.log("Record 1 location: "  +  record1.get('location') );
    ...
    return [record1, record2, record3];
  }
});
```

Reload your browser. Make sure the DevTools are open and select the JavaScript console tab. You should see the log notes from <samp class="application">Ember</samp>, ending with the line: “Record 1 location: Atlanta.”

Next, back in <samp class="filename">app/routes/sightings.js</samp>, <samp class="methodname">set</samp> the value of <samp class="varname">record1</samp>’s <samp class="varname">location</samp> after creating the record and before you log the property.

```
import Ember from 'ember';

export default Ember.Route.extend({
  model() {
    let record1 = this.store.createRecord('sighting', {
      location: 'Atlanta',
      sightedAt: new Date('2016-02-09')
    });
    record1.set('location', 'Paris, France');
    console.log("Record 1 location: " + record1.get('location'));
    ...
    return [record1, record2, record3];
  }
});
```

Reload the browser and you will see that the console reflects the <samp class="methodname">set</samp> value: “Record 1 location: Paris, France” ([Figure 21.2](#ch21s03.html_fig-creating-sightings "Figure 21.2  set location")).

**Figure 21.2  `set` location**

![set location](Tracker/Models/img/model-create-sightings.png)

These are basic examples of <samp class="methodname">get</samp> and <samp class="methodname">set</samp>. When setting a property on a model record, you can also assign other model records to the record property in order to create a relationship between two model records for properties that were defined with <samp class="methodname">hasMany</samp> or <samp class="methodname">belongsTo</samp>.

## Computed Properties

Computed properties are a huge part of managing model properties for your templates and components. <samp class="methodname">Ember.computed</samp> is a method that takes the values of scoped properties and returns a value when the method ends. Invoking the following, for example, would give you a computed property with the object’s <samp class="varname">first_name</samp> property changed to lowercase:

```
Ember.computed('first_name', function(){
  return this.get('first_name').toLowerCase();
});
```

In this example, <samp class="methodname">Ember.computed</samp> is acting as an event listener for changes to <samp class="varname">first_name</samp>. You do not have to change the <samp class="methodname">set</samp> method to trigger an event, you do not have to add an event listener, and you do not have to change the <samp class="varname">first_name</samp> property. All you do is create a new property that returns the value you want.

The use of computed properties is fairly global in <samp class="application">Ember</samp>. You will also be creating computed properties for components in [Chapter 25](#ch25.html "25 Components"). A computed property is used either as a <samp class="firstterm">decorator</samp> for a view or component, like the example above, or to retrieve specific data embedded deep in the model object.

“Decorating” data means formatting it a certain way – such as making a string lowercase. Data from an API is not always formatted the way you want it. Decorators are functions that input arguments and output objects or arrays to be used specifically for the view layer of an application. The formatting or construction of new decorated data generally does not return to the database. For this reason, decorators are generally added to a controller, unless every page is rendering data from a model that is not formatted in the database.

Add a computed property for a <samp class="varname">fullName</samp> to your witness model in <samp class="filename">app/models/witness.js</samp>.

```
import DS from 'ember-data';

export default DS.Model.extend({
  fName: DS.attr('string'),
  lName: DS.attr('string'),
  email: DS.attr('string'),
  sightings: DS.hasMany('sighting'),
  fullName:  Ember.computed('fName', 'lName', function(){
    return this.get('fName') + ' ' + this.get('lName');
  })
});
```

(If the autorestarting server complains, be sure you added the trailing comma to the sightings property declaration. It is an easy one to miss.)

The property you added to the <samp class="varname">witness</samp> model is a function that will be invoked every time <samp class="varname">fName</samp> and <samp class="varname">lName</samp> change. Computed properties can take any number of arguments as observed properties with the final argument being the function to return a value. Each argument that is a property will trigger the function argument to be invoked.

Open <samp class="filename">app/routes/witnesses.js</samp> and create a new witness record to test the computed property of the <samp class="varname">witness</samp> model:

```
import Ember from 'ember';

export default Ember.Route.extend({
  model() {
    let witnessRecord = this.store.createRecord('witness', {
      fName: "Todd",
      lName: "Gandee",
      email: "fake@bignerdranch.com"
    });
    return [witnessRecord];
  }
});
```

To get your witness data onscreen, edit <samp class="filename">app/templates/witnesses.hbs</samp> to use the same <samp class="methodname">{{#each}}</samp> iterator used in <samp class="filename">app/templates/sightings/index.hbs</samp>:

```
{{outlet}}
<h1>Witnesses</h1>
<div class="row">
  {{#each model as |witness|}}
    <div class="col-xs-12 col-sm-6 col-md-4">
      <div class="well">
        <div class="thumbnail">
          <div class="caption">
            <h3>{{witness.fullName}}</h3>
            <div class="panel panel-danger">
              <div class="panel-heading">Sightings</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  {{/each}}
</div>
```

Navigate to `http://localhost:4200/witnesses` and check out the results ([Figure 21.3](#ch21s04.html_fig-witness-listing "Figure 21.3  Witnesses listing")).

**Figure 21.3  Witnesses listing**

![Witnesses listing](Tracker/Models/img/model-computed-property-witnesses.png)

In this view, you added the listing of witnesses (which, at the moment, includes just one witness) and used a computed property to display the witness’s <samp class="varname">fullName</samp> property. This property was generated from the values you added when creating the witness record. With <samp class="methodname">witnessRecord.set</samp>, you can supply a different first name or last name before the model callback returns the record to see the property change.

You have come pretty far in these first few chapters on <samp class="application">Ember</samp>! You can now define your data models, create records, create computed properties, and get and set property values. In a moment, you will read about retrieving, updating, and destroying records using an API.

In the next chapter, you will learn about using adapters, serializers, and transforms to link your data models with data on the web.

## For the More Curious: Retrieving Data

As mentioned above, the data store manages model data and knows how to retrieve it. In the previous chapter, you returned data in the `SightingRoute` model callback with an array. In [Chapter 22](#ch22.html "22 Data – Adapters, Serializers, and Transforms"), you will retrieve model data in this route and return data as a `Promise` using <samp class="methodname">this.store.findAll</samp> and other data retrieval methods.

Below is a table of methods <samp class="application">Ember Data</samp>’s `store` object has at its disposal for retrieving data from an API, storing it in memory, and returning it to the requester.

| Request type | Retrieve all records | Retrieve a single record |
| --- | --- | --- |
| find persisted and local records | <samp class="methodname">findAll</samp> | <samp class="methodname">findRecord</samp> |
| find local records only | <samp class="methodname">peekAll</samp> | <samp class="methodname">peekRecord</samp> |
| find filtered records | <samp class="methodname">query</samp> | <samp class="methodname">queryRecord</samp> |

Retrieval methods come in several flavors: persisted and local, local only, and filtered persisted and local. Most use cases call for <samp class="methodname">findAll</samp> and <samp class="methodname">findRecord</samp>. The arguments for each match closely to the API endpoints that <samp class="application">Ember Data</samp> will create to request the data from the API.

For <samp class="methodname">findAll</samp>, the only required argument is the model name. For example, a request for all the witnesses would be <samp class="methodname">findAll('witness')</samp>. Notice the singular name? Remember, this argument is the model name. <samp class="application">Ember Data</samp> will make sure the request has a plural name when it builds the Ajax URL `/witnesses/`.

For <samp class="methodname">findRecord</samp>, an additional argument is needed to indicate a specific record. This argument is the identifier, usually the `id` of the record, such as `this.store.findRecord('witness', 5)`. When called, `findRecord('witness', 5)` will create a request for data at `/witnesses/5`.

For <samp class="methodname">peekAll</samp> and <samp class="methodname">peekRecord</samp>, the same arguments are needed to retrieve data. Invoking these methods will return the data immediately, not as a `Promise`.

Querying your API for data is another way to form requests. If your API supports query parameters, or <samp class="firstterm">params</samp>, for individual endpoints, <samp class="application">Ember Data</samp>’s <samp class="methodname">query</samp> and <samp class="methodname">queryRecord</samp> are great options. Like the other `store` methods, these methods take the model name as their first argument. The last argument is the query object, whose key/value pairs are converted into query string values. For <samp class="methodname">query</samp>, the request will find all records filtered by keys and values. <samp class="methodname">queryRecord</samp> is used when you know the request will return a single record.

For example, calling

```
this.store.query('user',{fName: "todd"})
```

would produce this request: `/users/?f_name=todd`. Alternatively,

```
this.store.queryRecord('user', {email: 'me@test.com'})
```

would produce this request: `/users?email=me@test.com`.

All of these `store` methods leverage adapters, which you will read about in the next chapter.

## For the More Curious: Saving and Destroying Data

Updating (i.e., saving) and destroying records are the next logical steps after creating and retrieving. (There is a mnemonic for this: CRUD, which stands for “create, read, update, destroy.”) The methods <samp class="methodname">save</samp> and <samp class="methodname">destroyRecord</samp> are available directly on model instances. These methods trigger requests through the adapter to update the data store. They return `Promise` objects, so you can chain callbacks with `.then` to do something with the returned data.

As you saw in this chapter, <samp class="methodname">set</samp> is the way to change property values on your model records. If you change a value locally in the app, the data will be different from the persisted source. Therefore, after you change a value with <samp class="methodname">set</samp>, you should save your data. You can do this with <samp class="methodname">modelRecord.save</samp>. Saving a model will tell the `store` to make a request to the API with a `POST` or `PUT`, depending on the state of the record.

Although this was not mentioned above, when retrieving data the `store` will make <samp class="methodname">get</samp> requests for data. When saving data, requests are sent with a type `POST` when the data does not exist in the persisted source and `PUT` when the data does exist and is being updated.

When you call <samp class="methodname">createRecord</samp>, as noted earlier, you are not saving the data to the database. You are merely making an in-memory object. Calling <samp class="methodname">save</samp> is for creation and updating.

Destroying records is the last step. Like the methods for retrieving and updating records, <samp class="methodname">modelRecord.destroyRecord</samp> uses a request method – in this case `DELETE` – to remove a record from the persisted source. The `store` then removes the record from memory. Like <samp class="methodname">save</samp>, <samp class="methodname">destroyRecord</samp> is actually two function calls in one, <samp class="methodname">deleteRecord</samp> and <samp class="methodname">save</samp>, because <samp class="methodname">deleteRecord</samp> only deletes the record locally. <samp class="methodname">destroyRecord</samp> is more commonly used because it combines these steps into a single action.

## Bronze Challenge: Changing the Computed Property

The <samp class="varname">fullName</samp> computed property currently uses <samp class="varname">fName</samp> and <samp class="varname">lName</samp>. Change the bound properties to be <samp class="varname">email</samp> and <samp class="varname">fName</samp> to create a <samp class="varname">fullName</samp> that displays as `Todd - tgandee@bignerdranch.com`.

## Silver Challenge: Flagging New Sightings

Add a new Boolean attribute to sightings, <samp class="varname">isNew</samp>. Give this attribute a <samp class="varname">defaultValue</samp> of `false`. Add this property to one of your created records and set it to `true`. Navigate to the `sightings` route and use the <samp class="application">Ember Inspector</samp> in <samp class="application">Chrome</samp> to review the data for the route. Only one sighting instance should have an <samp class="varname">isNew</samp> property set to `true`.

## Gold Challenge: Adding Titles

The witnesses need a proper title, such as <samp class="emphasis">Mr.</samp> Gandee. Add a <samp class="varname">title</samp> property to the model, then set it for each witness record except one. Add an object argument with a <samp class="varname">defaultValue</samp>. Pick an interesting default title for instances without a specified title. After creating the <samp class="varname">title</samp> property and supplying your created record with some new data, add a computed property to display the <samp class="varname">titleName</samp>.

Have fun with your default title. Wikipedia has a nice list of titles ([<samp class="uri">en.wikipedia.org/​wiki/​Title</samp>](https://en.wikipedia.org/wiki/Title)). “Mahatma Gandee” sounds pretty good…

# <samp class="chapter_number">22</samp>
<samp class="chapter_name">Data – Adapters, Serializers, and Transforms</samp>

Applications require data going in and out of the interface. Connecting to a data source is an important aspect of developing an application. Otherwise, you have a complex system of forms, events, and listings with no data to display.

In this chapter, you will learn some of the basics of wiring up a data source in <samp class="application">Ember</samp>. You will use an API created for this book and create an adapter for your application.

This chapter is a little different from the other chapters in the book. It has more information and less coding. However, this chapter will give you an important real-world view of application development with a server and database that may not be under your control. In the next chapter you will return to your regularly scheduled coding.

As mentioned in [Chapter 21](#ch21.html "21 Models and Data Binding"), adapters are the translators of your application. When you communicate with a data source, your application will need to request and send data in a variety of ways. <samp class="application">Ember Data</samp> comes with built-in adapter objects to handle some of the most common data scenarios: `JSONAPI` and generic “RESTful” APIs.

You are going to use the `JSONAPIAdapter` object to connect to a data source and return `JSONAPI`-formatted data. The `RESTAdapter` object is set of methods to work with data formatted from APIs generated from <samp class="application">Rails</samp> and <samp class="application">ActiveRecord</samp> plug-ins for <samp class="application">Rails</samp>.

The `JSONAPI` spec was created to give API consumers a predictable and scalable pattern for sending and receiving data from servers. While there are numerous server languages – and API object pattern conventions for each – `JSONAPI` set out to be a pattern any language could use so that front-end applications were not affected by a change in server technology. You can find out more about `JSONAPI` at its website, [<samp class="uri">jsonapi.org</samp>](http://jsonapi.org/).

In this chapter, you will also learn about security issues as well as <samp class="firstterm">serializers</samp>, which are the translation layer in the adapter flow. Finally, you will be introduced to <samp class="firstterm">transforms</samp>, the tool to coerce your data into the types your models expect. Adapters, serializers, and transforms work together as shown in [Figure 22.1](#ch22.html_fig-adapter-serializer-flow "Figure 22.1  Adapter, serializers, and transforms").

**Figure 22.1  Adapter, serializers, and transforms**

![Adapter, serializers, and transforms](Tracker/Adapters/img/Adapter-diagram.png)

At the end of this chapter, Tracker will look like [Figure 22.2](#ch22.html_fig-witness-list "Figure 22.2  Tracker at the end of this chapter").

**Figure 22.2  Tracker at the end of this chapter**

![Tracker at the end of this chapter](Tracker/Adapters/img/adapters-findAll-witnesses.png)

## Adapters

The <samp class="application">Ember</samp> team has built their framework with specific conventions in mind. Adapters are a large part of those conventions. The `JSONAPIAdapter` will communicate with a `REST` API for all requests originating from the `store`. Each request will add the model name and appropriate attribute data to a relative path of the domain.

To generate a specific URL for Ajax requests, the adapter needs the properties `host` and `namespace`. The adapter makes Ajax requests and expects the JSON responses to be formed with a particular structure. For example, the `JSONAPIAdapter` would expect a response for witnesses on a `GET` request to look like this:

```
{
"links": {
  "self": "http://bnr-tracker-api.herokuapp.com/api/witnesses"
},
"data": [
  {
    "id": "5556013e89ad2a030066f6e0",
    "type": "witnesses",
    "attributes": {
      "lname": "Gandee",
      "fname": "Todd"
    },
    "links": {
      "self": "/api/witnesses/5556013e89ad2a030066f6e0"
    },
    "relationships": {
      "sightings": {
      "data": [],
      "links": {
        "self":
        "/api/witnesses/5556013e89ad2a030066f6e0/relationships/sightings"
        }
      }
    }
  }
]
}
```

With each response, for example, the `type` of each object is expected to be the model name requested, in order to resolve all records for that model type. Also, an `id` is expected to be the primary key for each individual model object.

Begin by generating an application adapter:

```
ember g adapter application
```

Your application will be making requests to the Big Nerd Ranch Tracker API. As we have said, the `JSONAPIAdapter` property values require a host URL and a namespace, which is added to the end of the host when making an Ajax request for model data. Open <samp class="filename">app/adapters/application.js</samp> and declare the host and namespace.

```
import JSONAPIAdapter from 'ember-data/adapters/json-api';

export default DS.JSONAPIAdapter.extend({
  host: 'https://bnr-tracker-api.herokuapp.com',
  namespace: 'api'
});
```

Like other <samp class="application">Ember</samp> classes, naming patterns also apply to adapters – and adapters can be created to customize any model’s API needs. Irregularities in the data structure on the server can be contained in a single adapter rather than forcing all models to conform to edge cases.

What you have added to <samp class="filename">app/adapters/application.js</samp> is a global setting for all data requests. This is all you need for Tracker, because the API is sending all JSON responses from the same host and namespace. But if the witness model, for example, needed a different namespace or host, you could create an <samp class="filename">app/adapters/witness.js</samp> file and configure that particular adapter for witness requests.

Next, you need to retrieve your data from the API via the `store`. The API has cryptids and witnesses ready to go.

Open <samp class="filename">app/routes/witnesses.js</samp>. Delete the dummy data and replace it with a call to the retrieval method you learned in [Chapter 21](#ch21.html "21 Models and Data Binding").

```
...
  model(){
    let witnessRecord = this.store.createRecord('witness', {
      fname: "Todd",
      lname: "Gandee",
      email: "fake@bignerdranch.com"
    });
    return [witnessRecord];
    return this.store.findAll('witness');
  }
});
```

Now, restart your application from the terminal with `ember server` and point your browser to [<samp class="uri">http://​localhost:4200/​witnesses</samp>](http://localhost:4200/witnesses) ([Figure 22.3](#ch22.html_fig-witness-list-good "Figure 22.3  Witnesses listing")).

**Figure 22.3  Witnesses listing**

![Witnesses listing](Tracker/Adapters/img/adapters-findAll-witnesses.png)

Like most lifecycle flows in <samp class="application">Ember</samp>, adapters have a number of methods that get your data from the API to the `store` and to your routes, controllers, and templates. The purpose of a specific adapter, like the `JSONAPIAdapter`, is to handle a broad pattern and deal with an expected input/output for each model. Our example uses a <samp class="application">Node.js</samp> server backed by a <samp class="application">MongoDB</samp> database using a `json-api` `node` module to have API endpoints that work with `JSONAPI`-spec’d data.

Working with an API that has a specific pattern to follow (with minor edge cases of irregularity) makes for a happy programmer. You also might need to handle some extra data in your request, like authentication or request headers. Adapters can be customized to deal with any scenario.

<samp class="application">Ember</samp> previously had built-in adapters for other data source scenarios, like `localStorage` and fixture data. These adapters, and others, are now addons. They can be added via <samp class="application">Ember CLI</samp> when your model data needs to sync with other sources.

If you find that you have to hack together an adapter, dive into the documentation to find your answers. Some methods and properties of note are: <samp class="methodname">ajaxOptions</samp>, <samp class="methodname">ajaxError</samp>, <samp class="methodname">handleResponse</samp>, and <samp class="varname">headers</samp>.

At this point, your app is making requests to a server to receive a collection of witnesses. Before you move on to reading about the content security policy, serializers, and transforms, you will use the same method, <samp class="methodname">this.store.findAll</samp>, to retrieve all the <samp class="varname">cryptid</samp> records from the API. Because there is no view template for <samp class="varname">cryptids</samp>, you will examine the returned records with the <samp class="application">Ember Inspector</samp>.

Add the method call to <samp class="filename">app/routes/cryptids.js</samp>:

```
import Ember from 'ember';

export default Ember.Route.extend({
  model(){
    return this.store.findAll('cryptid');
  }
});
```

Now that you have the data returning, reload the app in the browser and navigate to [<samp class="uri">http://​localhost:4200/​cryptids</samp>](http://localhost:4200/cryptids). Use the <samp class="application">Ember Inspector</samp> to examine the returning data: In the DevTools, select the <samp class="guilabel">Ember</samp> tab and click <samp class="guilabel">Data</samp>, then <samp class="guilabel">cryptid(4)</samp> ([Figure 22.4](#ch22.html_fig-cryptid-data "Figure 22.4  Cryptid data")).

**Figure 22.4  Cryptid data**

![Cryptid data](Tracker/Adapters/img/adapters-cryptids-findAll.png)

Up to this point, there has not been a need to use the <samp class="application">Ember Inspector</samp> in depth. It is used here to show you how to examine in-memory data. <samp class="application">Ember</samp> retrieves the data from the API and populates the `store` with the correct model data. When debugging issues with model data, tracing the path of the request can be tedious. The <samp class="application">Ember Inspector</samp> should be the first place to look when you have this problem.

## Content Security Policy

<samp class="application">Ember</samp> makes use of a new security layer in JavaScript for detecting cross-origin requests before they hit your server. The working standard is called `Content Security Policy`. <samp class="application">Ember CLI</samp> has a `contentSecurityPolicy` object to add the appropriate information. The defaults are fairly strict when it comes to requesting data, scripts, images, styles, and other file types outside of your app’s domain.

There is an addon to set some defaults and integrate the security policy into your app: <samp class="application">ember-cli-content-security-policy</samp>. You do not need it for Tracker, but it is good to know about. This addon makes it easier to add environment variables to set the security policy. The security policy object will work with the browser specification `content-security-policy`. This browser spec, available in some newer browsers, is a standard introduced to prevent cross-site scripting and other code injection attacks resulting from execution of malicious content in the application.

Here is an example of the `contentSecurityPolicy` object:

```
module.exports = function(environment) {
  ...
  // config/environment.js
  ENV.contentSecurityPolicy = {
    'default-src': "",
    'script-src': "",
    'font-src': "",
    'connect-src': "",
    'img-src': "",
    'style-src': "",
    'media-src': null
  }
  ...
}
```

Each line of the security policy creates a <samp class="firstterm">whitelist</samp> – a set of safe paths – for each type of request. `default-src` is a catch-all setting and is originally set to `null` to force programmers to whitelist the settings they need. Other settings, like `script-src` and `connect-src`, are for requests external to the application domain, like [<samp class="uri">https://​bnr-tracker-api.herokuapp.com</samp>](https://bnr-tracker-api.herokuapp.com).

For more information, see the MDN *Content Security Policy* page and the GitHub repository for the <samp class="application">Ember CLI</samp> addon.

## Serializers

When data comes in and goes out, the JSON structure is serialized and deserialized. The adapter uses the serializer to get the data in and out of the store to build and resolve request/response data.

You can create a serializer with `ember g serializer [application or model name]`, which will create a serializer file with boilerplate code, like this:

```
import DS from 'ember-data';

export default DS.JSONAPISerializer.extend({
});
```

The serializer is an object assigned to the `serializer` property in the adapter. Without a specific serializer file in your application, <samp class="application">Ember</samp> will use a default adapter and serializer, the `JSONAPIAdapter` and `JSONAPISerializer`.

When you include a new serializer for the application, that serializer will be used as the `defaultSerializer` for the corresponding <samp class="filename">app/adapters/application.js</samp> file. Using the model’s name as the command option in `ember g serializer` allows you customize serialization of data for a specific model.

As with the `JSONAPIAdapter`, the configuration should only be changed if your API does not conform to the `JSONAPI` specification or if you have strange edge cases. If, in your own project, you were to need changes to request or response data, here are some methods to investigate in the <samp class="application">Ember Data</samp> documentation: <samp class="methodname">keyForAttribute</samp>, <samp class="methodname">keyForRelationship</samp>, <samp class="methodname">modelNameFromPayloadKey</samp>, and <samp class="methodname">serialize</samp>.

<samp class="methodname">keyForAttribute</samp> is a method to transform attribute names from the model to a keyname sent in the request. This method expects three arguments: <samp class="varname">key</samp>, <samp class="varname">typeClass</samp>, and <samp class="varname">method</samp>. For the `JSONAPISerializer`, this method returns the `key` <samp class="firstterm">dasherized</samp>, meaning that any underscores or camelcasing in the keyname will be converted to dashes. For example, if a model has a property `first_name`, the request object will have a key of `first-name`. If your API expects `first_name`, you will need to make a change to your the <samp class="methodname">keyForAttribute</samp> method to resolve the naming issue.

<samp class="methodname">keyForRelationship</samp> follows the same process, only for relationship keys. If your model names contain underscores you will need to edit this method for `JSONAPISerializer` when you have linked models with <samp class="methodname">belongsTo</samp> or <samp class="methodname">hasMany</samp> relationships. Some APIs expect relationships to add a suffix of `_id` or `_ids` for these relationships. This is the method to make that change.

The `bnr-tracker-api` you are using for Tracker uses the appropriate `JSONAPI` key names with dashes, such as `cryptid-type`. You will not need to add a serializer in your app. However, for illustration, here is an example of using the <samp class="application">Ember</samp> utility method <samp class="methodname">Ember.String.underscore</samp> to change the attribute keys of the incoming and outgoing JSON data.

```
import Ember from 'ember';
import DS from 'ember-data';
var underscore = Ember.String.underscore;
export default DS.JSONAPISerializer.extend({
  keyForAttribute(attr) {
    return underscore(attr);
  },
  keyForRelationship(rawKey) {
    return underscore(rawKey);
  }
});
```

<samp class="application">Ember</samp> provides a number of string manipulation methods on the `Ember.String` object. <samp class="methodname">Ember.String.underscore</samp> converts a string with dashes or camelcase to use an underscore to separate words.

The serializer methods are called during the lifecycle of a request for data, such as `this.store.findAll('witness')`. One way to examine the callback flow of a data request would be to add a `debugger` statement in this code to see what comes in and what goes out of the method.

Here is an example:

```
import Ember from 'ember';
import DS from 'ember-data';

var underscore = Ember.String.underscore;

export default DS.JSONAPISerializer.extend({
  keyForAttribute(attr) {
    let returnValue = underscore(rawKey);
    debugger;
    return returnValue;
    return underscore(rawKey);
  },
  keyForRelationship(rawKey) {
    return underscore(rawKey);
  }
});
```

When working with a new API, this style of debugging comes in handy. You have access to the `Ember.String` object for when you need to manipulate the `attr` argument to serialize your key names. Thankfully, <samp class="application">Ember</samp> and the <samp class="application">Ember</samp> community build adapters and serializers for numerous API patterns.

## Transforms

<samp class="application">Ember Data</samp> gives you the ability to transform data from your API to fit the needs of your application. You have already seen in [Chapter 21](#ch21.html "21 Models and Data Binding") that <samp class="application">Ember Data</samp> has built-in transforms – the methods <samp class="methodname">DS.attr('string')</samp>, <samp class="methodname">DS.attr('boolean')</samp>, <samp class="methodname">DS.attr('number')</samp>, and <samp class="methodname">DS.attr('date')</samp>.

When you add a transform to your application, you can call <samp class="methodname">DS.attr</samp> with your target attribute type. Transforms are like JavaScript coercion – they take a value and return the value in a specified type.

Here is an example of a basic <samp class="methodname">DS.attr('object')</samp> transform:

```
export default DS.Transform.extend({
  deserialize(value) {
    if (!Ember.$.isPlainObject(value)) {
      return {};
    } else {
      return value;
    }
  },
  serialize(value) {
    if (!Ember.$.isPlainObject(value)) {
      return {};
    } else {
      return value;
    }
  }
});
```

The transform has two methods: <samp class="methodname">deserialize</samp> and <samp class="methodname">serialize</samp>. The first, <samp class="methodname">deserialize</samp>, tests whether the incoming data is an object and returns it. Otherwise, it returns an empty object. The second, <samp class="methodname">serialize</samp>, returns the outgoing data if it is an object, and otherwise returns an empty object. The transforms guarantee that the data returning from the API and going out to the API are the type defined in the model.

## For the More Curious: Ember CLI Mirage

One the most common blockers for front-end application development is the API. A number of problems can come up: the API might not have been created, the API might be in development, or the API might be behind a firewall while you are developing.

The easiest solution to an inaccessible API is using static text or fixture data. But this solution might introduce a number of other issues, like changing the application logic to suit the inaccessible data, changing the requests to `this.store`, or changing the adapter or serializer.

<samp class="application">Ember CLI Mirage</samp> is an addon that will proxy the requests to specific API routes. You can set up models to establish relationships, set up factories to seed data, create fixture data for specific responses, and define CRUD routes to intercept specific requests to the API. Once these are set up, you can develop as though the API were in place.

While <samp class="application">Mirage</samp> is enabled, all requests will be diverted to the local <samp class="application">Mirage</samp> setup.

At the time of printing, `ember-cli-mirage` is in version `0.2.0-beta.8`. You are going to explore <samp class="application">Mirage</samp> in just a moment as part of a challenge. To find out more about <samp class="application">Ember CLI Mirage</samp>, visit [<samp class="uri">www.ember-cli-mirage.com</samp>](http://www.ember-cli-mirage.com/).

In the next chapter, you will bring together the concepts of the last three chapters and create a working application that routes requests and displays data. In [Chapter 24](#ch24.html "24 Controllers"), you will create, edit, and delete content. You will see the power of <samp class="application">Ember Data</samp>, adapters, and serializers when you can call <samp class="methodname">save</samp> and <samp class="methodname">destroyRecord</samp> on models and your data is sent to the API without much heartache.

## Silver Challenge: Content Security

Adding layers of security in an application is always important. As mentioned above, there is a new browser API for Content Security Policy, and <samp class="application">Ember</samp> has an environment object to handle configuring your application’s whitelist policy. Install the addon and follow the console errors to make sure your application’s external request endpoints are added to the policy.

## Gold Challenge: Mirage

<samp class="application">Ember CLI Mirage</samp> is a great addition to your development arsenal. It allows you to develop your application’s API needs before the back-end team finishes their stack.

Install `ember-cli-mirage` from your terminal to start using it:

```
ember install ember-cli-mirage
```

Next, to turn <samp class="application">Mirage</samp> on and off, add an environment variable to <samp class="filename">config/environment.js</samp>:

```
if (environment === 'development') {
  // ENV.APP.LOG_RESOLVER = true;
  // ENV.APP.LOG_ACTIVE_GENERATION = true;
  // ENV.APP.LOG_TRANSITIONS = true;
  // ENV.APP.LOG_TRANSITIONS_INTERNAL = true;
  // ENV.APP.LOG_VIEW_LOOKUPS = true;
  ENV['ember-cli-mirage'] = {
    enabled: true
  }
}
```

Finally, add fake data in the form of <samp class="firstterm">factories</samp> for your witness and cryptid endpoints.

To work with your Tracker app, you can retrieve a configured <samp class="filename">app/mirage</samp> directory from the supplied example assets in <samp class="filename">Tracker/Data_Chapter/mirage-example</samp>. We will keep the example up to date for current releases of the addon.

# <samp class="chapter_number">23</samp>
<samp class="chapter_name">Views and Templates</samp>

The V in MVC is for <samp class="emphasis">views</samp>. In Tracker, the views will be templates. Templates are processed with JavaScript to create HTML elements. This allows you to change the DOM without firing off a new request to the server.

In this chapter, you will be creating template files and adding the data retrieved in the route <samp class="methodname">model</samp> hook. The template language and helper functions built into <samp class="application">Ember</samp> will allow you to create templates with minimal effort beyond regular HTML syntax.

By the end of this chapter, you will have created listings like [Figure 23.1](#ch23.html_fig-templates-end "Figure 23.1  Sightings listing").

**Figure 23.1  Sightings listing**

![Sightings listing](Tracker/Templates/img/templates-sighting-end.png)

## Handlebars

You will be using <samp class="application">Handlebars</samp>, a powerful language for creating dynamic templates. It is similar to server-side templating languages like <samp class="application">PHP</samp>, <samp class="application">JSP</samp>, <samp class="application">ASP</samp>, and <samp class="application">ERB</samp>. It includes HTML element tags and delimiters to process data objects.

In <samp class="application">Handlebars</samp>, the delimiters are double curly braces, like `{{}}`. Inside the “double curlies,” you can render strings of data and execute limited logic using helper methods. You have seen two helper methods like this already: {{outlet}} and {{#each}}.

<samp class="application">Ember</samp>’s implementation of <samp class="application">Handlebars</samp> recently transitioned to a new mechanism, nicknamed “HTMLBars.” Some of the details of the language in this chapter are from HTMLBars, but are applicable to older versions of <samp class="application">Ember</samp> (at least back to version 1.13.x) as well.

## Models

In <samp class="application">Ember</samp>, templates are always backed by models. This means that an object (or array of objects) will be passed as an argument when the template is rendered to a string of HTML and appended to the DOM.

The model object can have properties with strings, arrays, or other objects. When writing templates with <samp class="application">Ember</samp> and <samp class="application">Handlebars</samp>, you access this object with the double curlies.

When you want to display the value of a model property, you write `{{model.name}}`, where `name` is a property on the `model` object. The dot syntax should feel familiar, but do not be fooled into thinking any JavaScript code can go within the curlies.

## Helpers

<samp class="application">Handlebars</samp> templates are strings interpolated by JavaScript functions. When the function comes across double curlies, it tries to resolve the instance of the delimiter with an object property or invoke a nested function to return a string. These nested functions are called <samp class="firstterm">helpers</samp> and are created in the application. There are a few helpers built into the <samp class="application">Handlebars</samp> library, and <samp class="application">Ember</samp> adds some of its own.

Helpers can take two forms. The first are inline helpers, which use the syntax `{{[helper name] [arguments]}}`. The arguments can include a hash of options, such as:

```
{{input type="text" value=firstName disabled=entryNotAllowed size="50"}}
```

More complex helpers use a block syntax:

```
{{#[helper name] [arguments]}}
  [block content]
{{/[helper name]}}
```

For example, if you wanted to present a sign-in link only to users who were not already logged in, you could use something like the block below:

```
{{#if notSignedIn}}
  <a href="/">Sign In</a>
{{/if}}
```

For block helpers, content can be passed to the block to augment the output with dynamic segments. <samp class="application">Handlebars</samp>’ built-in conditionals, described in the next section, are block helpers.

You are going to use helpers to render sections of your templates for sightings and cryptids as well as the `NavBar`.

### Conditionals

Conditional statements let you introduce basic control flow into <samp class="application">Handlebars</samp> templates. Their syntax looks like this:

```
{{#if argument}}
  [render block content]
{{else}}
  [render other content]
{{/if}}
```

Or, alternatively, like this:

```
{{#unless argument}}
  [render block content]
{{/unless}}
```

Conditional statements take a single argument that resolves to a truthy or falsy value. (Those are not typos. A <samp class="firstterm">truthy</samp> value is one that evaluates to true in a Boolean context. All values are truthy except those defined as <samp class="firstterm">falsy</samp>: the values false, 0, "", null, undefined, and NaN.)

Time to get to work. Open <samp class="filename">app/templates/sightings/index.hbs</samp> and add a conditional statement so that sighting entries display either the location or, if there is no location data, a polite warning about the missing data.

```
<div class="panel panel-default">
  <ul class="list-group">
    {{#each model as |sighting|}}
      <li class="list-group-item">
        {{sighting.location}} - {{sighting.sightedAt}}
      </li>
    {{/each}}
  </ul>
</div>
<div class="row">
  {{#each model as |sighting|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        <div class="caption">
          {{#if sighting.location}}
            <h3>{{sighting.location}} - {{sighting.sightedAt}}</h3>
          {{else}}
            <h3 class="text-danger">Bogus Sighting</h3>
          {{/if}}
        </div>
      </div>
    </div>
  {{/each}}
</div>
```

You changed the DOM structure of your sightings template to start outputting sighting information in the form of styled elements using <samp class="application">Bootstrap</samp>’s <samp class="firstterm">wells</samp> style. The use of `{{#if}} and {{else}}` allows you to render different HTML when the location of the sighting has not been added.

Now you need to change the data sent from the route to the template to see the results of your new conditional. In your sightings route model in <samp class="filename">app/routes/sightings.js</samp>, set the `location` property of one sighting to the empty string.

```
...
  model(){
    ...
    let record3 = this.store.createRecord('sighting', {
      location: 'Asilomar',
      sightedAt: new Date('2016-03-21')
    });

    return [record1, record2, record3];
  }
});
```

Start your server and point your browser to [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings) to see the new list of sightings ([Figure 23.2](#ch23s03.html_fig-bogus "Figure 23.2  Bogus sighting")).

**Figure 23.2  Bogus sighting**

![Bogus sighting](Tracker/Templates/img/templates-sightings-if-bogus.png)

The conditional statement evaluated the truthy value of the empty string for the last sighting instance. Thus, the template rendered the block content with the text “Bogus Sighting.”

### Loops with {{#each}}

You have already used the `{{#each}}` block helper in the index template. This helper renders each object in the array as an instance of the content in the block. The argument for `{{#each}}` is the `array` as an `|instance|` contained in the block argument. The block will only render if the argument passed in to `{{#each}}` is an array with at least one element.

Like the `{{#if}}` block helper, this helper supports an `{{else}}` block that will render when the array argument is empty.

Use `{{#each}} {{else}} {{/each}}` to create a listing of all recorded cryptids – or, if there are none, the text “No Creatures” – in <samp class="filename">app/templates/cryptids.hbs</samp>:

```
{{outlet}}
<div class="row">
  {{#each model as |cryptid|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        <div class="caption">
          <h3>{{cryptid.name}}</h3>
        </div>
      </div>
    </div>
  {{else}}
    <div class="jumbotron">
      <h1>No Creatures</h1>
    </div>
  {{/each}}
</div>
```

Similar to sightings, you are listing the cryptids in styled wells. The `{{else}}` block allows you to include a condition in your template when there are no items in the array you are listing. Your app can render a different element for this conditional of an empty model array.

Navigate to [<samp class="uri">http://​localhost:4200/​cryptids</samp>](http://localhost:4200/cryptids) to see your new cryptid listing ([Figure 23.3](#ch23s03.html_fig-new-cryptid-listing "Figure 23.3  Cryptids listing")).

**Figure 23.3  Cryptids listing**

![Cryptids listing](Tracker/Templates/img/templates-cryptids-listing-full.png)

Now, in <samp class="filename">app/routes/cryptids.js</samp>, remove the `model` callback by commenting out the `return` statement to exercise the `else` of your conditional.

```
...
  model(){
    // return this.store.findAll('cryptid');
  }
});
```

Reload [<samp class="uri">http://​localhost:4200/​cryptids</samp>](http://localhost:4200/cryptids). Your cryptid listing is now blank ([Figure 23.4](#ch23s03.html_fig-empty-list "Figure 23.4  Empty cryptids listing")).

**Figure 23.4  Empty cryptids listing**

![Empty cryptids listing](Tracker/Templates/img/templates-cryptids-listing-empty.png)

With `{{each}} {{else}} {{/each}}`, you can have conditional views based on the presence of data and very little conditional logic. Now that you have seen (and tested) the wonders of conditional iterators, return <samp class="filename">app/routes/cryptids.js</samp> to its previous state:

```
...
  model(){
    // return this.store.findAll('cryptid');
  }
});
```

### Binding element attributes

Element attribute values can be rendered from controller properties just as element content is rendered between DOM element tags. In earlier versions of <samp class="application">Ember</samp>, there was a helper to bind attributes called `{{bind-attr}}`. Now, thanks to HTMLBars, you can you just use `{{}}` to bind a property to the attribute.

Attribute binding is common with element properties like `class` and `src`. Your cryptids have an image path in their data, so you can dynamically bind their `src` property to a `model` attribute.

Add an image to the cryptid listing in <samp class="filename">app/templates/cryptids.hbs</samp>:

```
<div class="row">
  {{#each model as |cryptid|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        <img class="media-object thumbnail" src="{{cryptid.profileImg}}"
          alt="{{cryptid.name}}" width="100%" height="100%">
        <div class="caption">
          <h3>{{cryptid.name}}</h3>
        </div>
      </div>
    </div>
  {{else}}
    <div class="jumbotron">
      <h1>No Creatures</h1>
    </div>
  {{/each}}
</div>
```

You will need to add the cryptid images from your course assets to the directory <samp class="filename">tracker/public/assets/image/cryptids</samp>. When the <samp class="application">Ember</samp> server is running, the <samp class="filename">public</samp> directory is the root for assets. For a production application you may need to configure these paths, but for development, <samp class="filename">public/assets</samp> is a good place to work. These files are copied to the <samp class="filename">dist</samp> directory where your application is compiled and served.

When deploying an application to a server and adding images to persisted data you need to be conscious of the path to the actual image file. In our example, we are serving the images from the same directory as our application, and the database stores the relative path of the image to our application.

Before HTMLBars, the `{{bind-attr}}` helper could be used as an inline ternary operation for assigning properties based on a Boolean property. Now, you can use the inline `{{if}}` helper. This is common when your UI has styles that represent true and false states of a specific property.

Use the ternary form in <samp class="filename">app/templates/cryptids.hbs</samp> to handle missing images:

```
<div class="row">
  {{#each model as |cryptid|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        <img class="media-object thumbnail" src="{{cryptid.profileImg}}"
          src="{{if cryptid.profileImg cryptid.profileImg
          'assets/images/cryptids/blank_th.png'}}"
          alt="{{cryptid.name}}" width="100%" height="100%">
        <div class="caption">
        ...
```

Unlike the block `{{#if}}` helper, the inline `{{if}}` helper does not yield block content. The inline helper evaluates the first argument as a Boolean and outputs either the second or third argument.

Here, you are evaluating the truthiness of `{{cryptid.profileImg}}` for the first argument. If it is truthy, the output is the cryptid’s image path. Otherwise, a placeholder image is specified.

You can use a dynamic value as an argument to all inline helpers. You can also pass any JavaScript primitive as an argument, such as a string, number, or Boolean.

Before you look at the results of your conditional, create a cryptid without an image path in the <samp class="methodname">beforeModel</samp> hook in <samp class="filename">app/routes/cryptids.js</samp>:

```
import Ember from 'ember';

export default Ember.Route.extend({
  beforeModel(){
    this.store.createRecord('cryptid', {
      "name": "Charlie",
      "cryptidType": "unicorn"
    });
  },
  model(){
    return this.store.findAll('cryptid');
  }
});
```

Now reload [<samp class="uri">http://​localhost:4200/​cryptids</samp>](http://localhost:4200/cryptids) and check out your new images ([Figure 23.5](#ch23s03.html_fig-cryptid-images "Figure 23.5  Cryptids listing with images")).

**Figure 23.5  Cryptids listing with images**

![Cryptids listing with images](Tracker/Templates/img/templates-cryptids-if-img.png)

### Links

As discussed in [Chapter 20](#ch20.html "20 Routing, Routes, and Models"), routing is unique to browser-based applications. <samp class="application">Ember</samp> listens to a couple of event hooks to manage routing in your application. For this reason, you should create links with `{{#link-to}}` block helpers. This helper takes the route (represented by a string) as the first argument to create an anchor element. For example, `{{#link-to 'index'}}Home{{/link-to}}` creates a link to the root index page.

To see how this works, you are going to update your main navigation with links using `{{#link-to}}` helpers.

Begin in <samp class="filename">app/templates/application.hbs</samp>. Replace the `NavBar`’s test links with links to your sightings, cryptids, and witnesses:

```
...
      <div class="collapse navbar-collapse" id="top-navbar-collapse">
        <ul class="nav navbar-nav">
          <li>
            <a href="#">Test Link</a>
          </li>
          <li>
            <a href="#">Test Link</a>
          </li>
          <li>
            {{#link-to 'sightings'}}Sightings{{/link-to}}
          </li>
          <li>
            {{#link-to 'cryptids'}}Cryptids{{/link-to}}
          </li>
          <li>
            {{#link-to 'witnesses'}}Witnesses{{/link-to}}
          </li>
        </ul>
      </div><!-- /.navbar-collapse -->
```

Now that you have links to your listing pages, reload your app and test them. Click around. Hit the back button. You have a working web app! Take a moment to celebrate.

Your next task is to make the images on the cryptids page link to an individual page for each creature. To do this, you will take advantage of the fact that the `{{#link-to}}` helper can take multiple arguments to customize the link. In <samp class="filename">app/templates/cryptids.hbs</samp>, wrap the `<img>` tag with a link to a specific cryptid using `cryptid.id` as the second argument:

```
...
    <div class="media well">
      {{#link-to 'cryptid' cryptid.id}}
        <img class="media-object thumbnail"
        src="{{if cryptid.profileImg cryptid.profileImg
        'assets/images/cryptids/blank_th.png'}}"
        alt="{{cryptid.name}}" width="100%" height="100%">
      {{/link-to}}
      <div class="caption">
        <h3>{{cryptid.name}}</h3>
      </div>
    </div>
...
```

Now that you have links to the `cryptid` route and the anchor has a path to <samp class="uri">cryptids/​[cryptid_id]</samp>, you will need to edit <samp class="filename">router.js</samp> so the `CryptidRoute` knows to expect a dynamic value.

```
...
Router.map(function() {
  this.route('sightings', function() {
    this.route('new');
  });
  this.route('sighting', function() {
    this.route('edit');
  });
  this.route('cryptids');
  this.route('cryptid', {path: 'cryptids/:cryptid_id'});
  this.route('witnesses');
  this.route('witness');
});
...
```

Try it out. You should see a blank page after clicking one of the cryptid images. This is good. Your app is routing you to the `CryptidRoute`, which is rendering the <samp class="filename">app/templates/cryptid.hbs</samp>, singular. That file is currently blank.

If you clicked on Charlie the unicorn’s image, you probably got an error. Recall that his record was created in the <samp class="methodname">beforeModel</samp> hook and does not have an `id`. That means that the value it tries to pass to the `{{#link-to}}` helper is `null`.

This is a good time to remove that <samp class="methodname">beforeModel</samp> hook. Creation should be reserved for pages creating new cryptids, which we will cover in [Chapter 24](#ch24.html "24 Controllers").

Remove the hook from <samp class="filename">app/routes/cryptids.js</samp>.

```
...
  beforeModel(){
    this.store.createRecord('cryptid', {
      "name": "Charlie",
      "cryptidType": "unicorn"
    });
  },
  model(){
    return this.store.findAll('cryptid');
  }
...
```

Next, add the request for cryptid data in the <samp class="filename">app/routes/cryptid.js</samp> (singular).

```
import Ember from 'ember';

export default Ember.Route.extend({
  model(params){
    return this.store.findRecord('cryptid', params.cryptid_id);
  }
});
```

The `cryptid_id` dynamic route parameter is passed to the route’s `model` hook as an argument. You use this parameter to call the `store`’s <samp class="methodname">findRecord</samp> method.

Now, edit the template for an individual cryptid, <samp class="filename">app/templates/cryptid.hbs</samp>, to show the cryptid’s image and name.

```
{{outlet}}
<div class="container text-center">
  <img class="img-rounded" src="{{model.profileImg}}" alt="{{model.type}}">
  <h3>{{model.name}}</h3>
</div>
```

The <samp class="varname">model</samp> passed to this template is a single object, not an array of objects to iterate over. The <samp class="methodname">this.store.findRecord</samp> method returns a single <samp class="varname">cryptid</samp> instance. In the template, the <samp class="varname">model</samp> is this instance and the properties are retrieved using <samp class="literal">{{model.[property-name]}}</samp>.

In the browser, use your `NavBar` to navigate to <samp class="guilabel">Cryptids</samp> and then click one of the cryptid images to view its detail page ([Figure 23.6](#ch23s03.html_fig-detail-image "Figure 23.6  Cryptid detail page")).

**Figure 23.6  Cryptid detail page**

![Cryptid detail page](Tracker/Templates/img/templates-cryptid-detail.png)

You will explore `{{#link-to}}` more in future chapters. Remember, helpers are functions that are invoked when the template is rendered. <samp class="application">Ember</samp> comes with its own, but you are not limited to the built-in helpers.

## Custom Helpers

The sighting’s <samp class="varname">sightedAt</samp> date property is displayed as an ugly raw date string. To format your dates more nicely, you are going to use the same `moment` library you used in Chattrbox.

Add `moment` from the terminal:

```
bower install moment --save
```

Then, use `app.import` to add `moment` to your vendor assets in <samp class="filename">ember-cli-build.js</samp>:

```
...
  // Add assets to app with import
  app.import(bootstrapPath + 'javascripts/bootstrap.js');
  app.import('bower_components/moment/moment.js');

  return app.toTree();
};
```

Changes to your server configurations require a restart, so after you change the <samp class="filename">ember-cli-build.js</samp>, stop your <samp class="application">Ember</samp> server (Control+C) and start it back up (`ember server`).

Now you need to generate the helper module from the terminal:

```
ember g helper moment-from
```

From here, you will create a function that will return HTML as a string. The function will have a date as an argument, and it will process the date with the `moment.js` library. You will surround the date with an HTML `<span>` tag and apply a <samp class="application">Bootstrap</samp> text utility to the element.

Open the generated file, <samp class="filename">app/helpers/moment-from.js</samp>, and create this new function:

```
import Ember from 'ember';

export function momentFrom(params/*, hash*/) {
  return params;
}
export function momentFrom(params) {
  var time = window.moment(...params);
  var formatted = time.fromNow();
  return new Ember.Handlebars.SafeString(
    '<span class="text-primary">'
    + formatted + '</span>'
  );
}

export default Ember.Helper.helper(momentFrom);
```

Now that you have created the helper, use it in your <samp class="filename">app/templates/sightings/index.hbs</samp> template:

```
...
          {{#if sighting.location}}
            <h3>{{sighting.location}} - {{sighting.sightedAt}}</h3>
            <p>{{moment-from sighting.sightedAt}}</p>
          {{else}}
...
```

The `moment-from` helper takes a single argument and returns the formatted date as a string of HTML. When you use a custom helper to render HTML elements, <samp class="application">Ember</samp> provides the <samp class="methodname">Ember.Handlebars.SafeString</samp> method to output clean markup.

Check out your newly formatted dates ([Figure 23.7](#ch23s04.html_fig-sightings-moment-date "Figure 23.7  Sightings moment.js date")).

**Figure 23.7  Sightings `moment.js` date**

![Sightings moment.js date](Tracker/Templates/img/templates-sighting-moment-date.png)

The `moment.js` library takes the date object and formats it as something like “2 months ago.” That looks much better than “Tue Feb 9 2016 19:00:00 GMT-0500 (EST)”! (There are many options in `moment.js` for formatting dates – explore [<samp class="uri">momentjs.com</samp>](http://momentjs.com) to find out more.)

By creating a helper to output the specific text, you can remove some logic from the template. Custom helpers allow you to cut down on repetition and centralize UI formatting. This is the first step to abstracting your code into <samp class="application">Ember Components</samp>, which you will learn about in [Chapter 25](#ch25.html "25 Components").

In this chapter, you learned to display basic model properties and customize your templates with conditionals and loops. You bound HTML element attributes to properties and created new routes with dynamic attributes to load individual records as the model backing the template. Finally, you used helpers for linking to pages and rounded out your understanding of helpers by building your own helper to format dates.

In the next chapter, you will complete the application lifecycle by creating and editing data with controllers. You will learn about actions, retrieve multiple collections from your data store, and create decorators.

## Bronze Challenge: Adding Link Rollovers

The links you created need some rollover content. To achieve this, add a title attribute to your `{{#link-to}}` helpers. The title should be the sighting’s cryptid name.

## Silver Challenge: Changing the Date Format

The `{{moment-from}}` helper has made the date less clunky, but now it is not as informative as it should be. Review the `moment` documentation and change the output of the helper to format the date as “Sunday May 31, 2016.”

## Gold Challenge: Creating a Custom Thumbnail Helper

The markup for the cryptid thumbnails seems a bit long. Create a custom helper to display cryptid thumbnails by passing the image path to the helper. Clean up your code by using the helper in all the places the cryptid images appear.

# <samp class="chapter_number">24</samp>
<samp class="chapter_name">Controllers</samp>

Controllers are the last piece of the MVC pattern. As you learned in [Chapter 19](#ch19.html "19 Introduction to MVC and Ember"), controllers hold application logic, retrieve model instances and give them to views, and contain handler functions that make changes to model instances.

The controllers you will build in this chapter will not be particularly large pieces of code. That is the idea behind MVC: distributing the complexity of an application to the places it belongs. Managing the data is the job of the models, and handling the UI is the province of the views. The controller only needs to, well, <samp class="emphasis">control</samp> the models and views.

Without your knowledge, <samp class="application">Ember</samp> has been adding controller objects to your application when it is running. Controllers are a proxy between the route object and the template, passing the model through. When you do not add a controller object, <samp class="application">Ember</samp> knows that the model data is sufficient to pass to the template, and it does that for you.

Creating a controller in <samp class="application">Ember</samp> allows you to define the events or actions to listen for when the route is active. It also allows you to define decorator properties to augment model data you want to display without persisting it.

One of the goals of the Tracker application is for the user to be able to create new sightings. For this goal, you will need to create a route, a controller, controller properties, and controller actions.

You have already created the new sighting route, <samp class="filename">app/routes/sightings/new.js</samp>. For this page, you are you going to create a new sighting record and load the collections of cryptids and witnesses. Each new sighting will need the relationships of belonging to a cryptid and having one or many witnesses. The form you will create will look like [Figure 24.1](#ch24.html_fig-sighting-form-for-ch-end "Figure 24.1  Tracker’s New Sighting form").

**Figure 24.1  Tracker’s New Sighting form**

![Tracker’s New Sighting form](Tracker/Controllers/img/ember-controller-new-template.png)

When you have all of that set up, you will create a controller to manage events from the new sighting form. You will also expand on your work to allow existing sightings to be edited and deleted.

## New Sightings

The `SightingsRoute`’s model that you have set up returns all the sightings. For the new sightings model, you will return the result of creating a single new, empty sighting. Also, you will return a set of `Promise`s for the cryptids and witnesses. To do this you will return `Ember.RSVP.hash({})`.

Let’s get started. Open <samp class="filename">app/routes/sightings/new.js</samp> and add a model hook to return a collection of `Promise`s as an <samp class="methodname">Ember.RSVP.hash</samp>:

```
...
export default Ember.Route.extend({
  model() {
    return Ember.RSVP.hash({
      sighting: this.store.createRecord('sighting')
    });
  }
});
```

When this route is active, a new record of a sighting is returned. If you were to return to the `sightings`, you would see a blank entry, because you created a new record. You will handle the <samp class="firstterm">dirty records</samp> (model data that has been changed but not saved to the persisted source) toward the end of this chapter. For now, know that <samp class="methodname">createRecord</samp> has added a new sighting to the local collection.

When creating a new sighting, you will need the list of cryptids and witnesses. Here, `Ember.RSVP.hash({})` is used to say you are returning a hash of `Promise`s. The only key is `sighting`, which means that your `model` reference in the template will need to do a look-up on `model.sighting` to reference the sighting record you created.

Add the retrieval methods for cryptids and witnesses to this hash (do not neglect the comma after `this.store.createRecord('sighting')`).

```
...
export default Ember.Route.extend({
  model() {
    return Ember.RSVP.hash({
      sighting: this.store.createRecord('sighting'),
      cryptids: this.store.findAll('cryptid'),
      witnesses: this.store.findAll('witness')
    });
  }
}
```

Next, you are going to use `<select>` tags in your new sightings template to present the lists of cryptids and witnesses to the user. But before you set up your template with the new model data, you will need an <samp class="application">Ember CLI</samp> plug-in that makes it easy to use `<select>` tags with bound properties.

From the command line, install <samp class="application">emberx-select</samp>:

```
ember install emberx-select
```

You will use this component, usually called <samp class="application">x-select</samp>, in your template. This saves you from writing `onchange` actions for each `<select>` tag.

Restart `ember server` before using the <samp class="application">x-select</samp> component.

With all the model data set up, you can now edit the template, <samp class="filename">app/templates/sightings/new.hbs</samp>, to create the new sighting form:

```
<h1>New Route</h1>
<h1>New Sighting</h1>
<form>
  <div class="form-group">
    <label for="name">Cryptid</label>
    {{#x-select value=model.sighting.cryptid class="form-control"}}
      {{#x-option}}Select Cryptid{{/x-option}}
      {{#each model.cryptids as |cryptid|}}
        {{#x-option value=cryptid}}{{cryptid.name}}{{/x-option}}
      {{/each}}
    {{/x-select}}
  </div>
  <div class="form-group">
    <label>Witnesses</label>
    {{#x-select value=model.sighting.witnesses multiple=true class="form-control"}}
      {{#x-option}}Select Witnesses{{/x-option}}
      {{#each model.witnesses as |witness|}}
        {{#x-option value=witness}}{{witness.fullName}}{{/x-option}}
      {{/each}}
    {{/x-select}}
  </div>
  <div class="form-group">
    <label for="location">Location</label> {{input value=model.sighting.location
      type="text" class="form-control" name="location" required=true}}
  </div>
</form>
```

Wow! That has got everything you have been working on – and more. The route is using a new <samp class="methodname">Ember.RSVP</samp> method, the template is using helpers, and the new `{{x-select}}` and `{{x-option}}` components are used.

The `{{x-select}}` component is built to use the `<select>` element to assign a value to a property. It is designed to work just like a `<select>` element in the <samp class="application">Ember</samp> data-binding environment. You assign the `value` to the sightings model’s cryptid property and the component will handle the `onchange` event when a new option is selected. This works because the cryptid property needs a cryptid model record as its value.

For the witnesses, there is an extra attribute, `multiple=true`, which will allow your users to select multiple witnesses for a sighting. Multiple selections will translate into a collection of <samp class="methodname">hasMany</samp> witnesses.

Before you go any further, you will need to add a link to the sightings route template so you have a way to get to the `sightings.new` route. Open <samp class="filename">app/templates/sightings.hbs</samp> and take care of that.

```
<h1>Sightings</h1>
<div class="row">
  <div class="col-xs-6">
    <h1>Sightings</h1>
  </div>
  <div class="col-xs-6 h1">
    {{#link-to "sightings.new" class="pull-right btn btn-primary"}}
      New Sighting
    {{/link-to}}
  </div>
</div>
{{outlet}}
```

Your link takes advantage of the simplicity of <samp class="application">Bootstrap</samp> formatting to create a button. Load [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings) to see it ([Figure 24.2](#ch24.html_fig-new-sightings-button2 "Figure 24.2  New Sighting button")).

**Figure 24.2  New Sighting button**

![New Sighting button](Tracker/Controllers/img/ember-controller-new-button.png)

Now you have the ability to navigate to the `sightings.new` route. The new button adds a link to create a new sighting from anywhere in the sightings route tree structure.

Also, notice that when you are on the `sightings.new` route, the button is active. <samp class="application">Ember</samp> has thought of it all, giving an active class to a link even when the current route is the link’s route. Having an active state on a button or link signifies the current route in the form of UI cues.

Actions are the key to handling form events – or any other events in your app. The `actions` property is a hash where you assign functions to keys. The keys will be used in the templates to trigger the callback.

You are ready to create the controller for the `sightings.new` route, using this terminal command:

```
ember g controller sightings/new
```

<samp class="application">Ember</samp> creates the <samp class="filename">app/controllers/sightings/new.js</samp> file. Open it and add the `create` and `cancel` actions you will need to create sightings:

```
import Ember from 'ember';

export default Ember.Controller.extend({
  actions: {
    create() {
    },
    cancel() {
    }
  }
});
```

When creating a form element, the `action` attribute usually has a URL to which you submit the form. With <samp class="application">Ember</samp>, the form element only needs the name of a function to run.

In <samp class="filename">app/templates/sightings/new.hbs</samp>, have the form element set the action for `submit`. Also, add <samp class="guibutton">Create</samp> and <samp class="guibutton">Cancel</samp> buttons:

```
<h1>New Sighting</h1>
<form {{action "create" on="submit"}}>
...
  <div class="form-group">
    <label for="location">Location</label> {{input value=model.location
      type="text" class="form-control" name="location" required=true}}
  </div>
  <button type="submit" class="btn btn-primary btn-block">Create</button>
  <button {{action 'cancel'}} class="btn btn-link btn-block">Cancel</button>
</form>
```

<samp class="application">Atom</samp> may complain about the syntax of the lines with the `{{action}}` helpers. You can ignore its complaints. (You can also install <samp class="application">Language-Mustache</samp> and enable it in <samp class="application">Atom</samp>’s preferences so that <samp class="application">Atom</samp> recognizes this syntax. The package can be found at [<samp class="uri">atom.io/​packages/​language-mustache</samp>](https://atom.io/packages/language-mustache).)

The two `{{action}}` helpers have string arguments matching the actions you created in <samp class="filename">app/controllers/sightings/new.js</samp>. Actions are bound to event handlers. The `{{action}}` helper accepts an argument, `on`, to which the action is assigned. A click event listener is assigned to the action if you do not add the `on` argument to the helper.

In the new sightings form, you added `on="submit"` to specify that the `create` action will be called on submit. You did not give an `on` argument to the cancel button, on the other hand, so the event bound with the action will be a click.

Your form now works to submit and cancel using controller actions, but those actions need some code. Start with the `create` action. Update <samp class="filename">app/controllers/sightings/new.js</samp> to complete the sighting, save it, and return to the sightings listing.

```
...
  actions: {
    create() {
      var self = this;
      this.get('model.sighting').save().then(function() {
        self.transitionToRoute('sightings');
      });
    },
    cancel() {
    }
  }
});
```

When the form is submitted, <samp class="methodname">create</samp> is called. First, you set a reference to the controller with `self`. Next, you get the sighting model and call <samp class="methodname">save</samp>.

The last step is saving to the persistent source. There is a flag on the model for `hasDirtyAttributes` that is set to false when a model is saved.

Saving a model returns a `Promise`. You chained that `Promise` with `then`, which takes a function to be called when the model has been saved successfully. Finally, you return to the sightings listing with <samp class="methodname">transitionToRoute</samp>.

Check out your form at [<samp class="uri">http://​localhost:4200/​sightings/​new</samp>](http://localhost:4200/sightings/new) ([Figure 24.3](#ch24.html_fig-sighting-form "Figure 24.3  New Sighting form")).

**Figure 24.3  New Sighting form**

![New Sighting form](Tracker/Controllers/img/ember-controller-new-template.png)

Fill in the form and click <samp class="guibutton">Create</samp>. Although you successfully added a new sighting, your sightings list route model is still returning the records created inline. Open <samp class="filename">app/routes/sightings.js</samp>, delete the dummy data, and replace it with a call to the `store` to retrieve the sightings.

```
import Ember from 'ember';

export default Ember.Route.extend({
  model() {
    let record1 = this.store.createRecord('sighting', {
      location: 'Atlanta',
      sightedAt: new Date('2016-02-09')
    });
    record1.set('location', 'Paris, France');
    console.log("Record 1 location: " + record1.get('location'));

    let record2 = this.store.createRecord('sighting', {
      location: 'Calloway',
      sightedAt: new Date('2016-03-14')
    });

    let record3 = this.store.createRecord('sighting', {
      location: '',
      sightedAt: new Date('2016-03-21')
    });

    return [record1, record2, record3];
    return this.store.findAll('sighting', {reload: true});
  }
});
```

Now your app has creation and retrieval.

Notice the second argument of <samp class="methodname">findAll</samp>, the object literal with the single key `reload`. This argument tells the `store` to request fresh data from the API each time the route model is called. Adding this argument makes it explicit that you always want the freshest data each time you view the list.

Next, the `cancel` action needs to delete the in-memory, dirty sighting instance. You will use <samp class="methodname">model.deleteRecord</samp>, as you did in [Chapter 21](#ch21.html "21 Models and Data Binding"). Add it to <samp class="filename">app/controllers/sightings/new.js</samp>.

```
...
  actions: {
    create() {
      var self = this;
      this.get('model.sighting').save().then(function() {
        self.transitionToRoute('sightings');
      });
    },
    cancel() {
      this.get('model.sighting').deleteRecord();
      this.transitionToRoute('sightings');
    }
  }
...
```

After deleting the record, the user will be returned to the listing. This scenario works when the user clicks the `cancel` button, but what happens when the top navigation is used to go back to the listing or another route?

If you do not destroy the dirty record, it will stay in memory while the user’s session is active. To destroy the record you will use an action in the route.

In the lifecycle of a route, there are actions called at different states and transitions. You can override these actions to customize callbacks for different stages of your route transition.

Open <samp class="filename">app/routes/sightings/new.js</samp> and override the `willTransition` action to ensure that dirty records are deleted:

```
...
  model(){
    return Ember.RSVP.hash({
      sighting: this.store.createRecord('sighting'),
      cryptids: this.store.findAll('cryptid'),
      witnesses: this.store.findAll('witness')
    });
  },
  actions: {
    willTransition() {
      var sighting = this.get('controller.model.sighting');
      if(sighting.get('hasDirtyAttributes')){
        sighting.deleteRecord();
      }
    }
  }
});
```

The action `willTransition` will fire when the route changes. Using <samp class="methodname">deleteRecord</samp> will destroy the model object, but only when the model property `hasDirtyAttributes` is true.

You have now covered your bases with a dirty record on creation. You are also set up to save to a persistent data source with minimal changes to the controller.

## Editing a Sighting

After creating and reading data, CRUD tells us that updating is the next step. You have an edit route for a sighting, but you need to put it to use by updating the sighting listing with a button to navigate to the edit route. You also need to add a form with sighting fields to the edit template; have the edit route’s <samp class="methodname">model</samp> retrieve witnesses, cryptids, and the sighting; and add route parameters to the edit route object in <samp class="filename">app/router.js</samp>. Finally, you need to create a controller to add actions for the edit form.

Let’s start with adding an <samp class="guibutton">Edit</samp> button in <samp class="filename">app/templates/sightings/index.hbs</samp>. To give more context to the list, add the name and image of the cryptid that was sighted as well.

```
...
      <div class="media well">
        <img class="media-object thumbnail" src="{{if sighting.cryptid.profileImg
          sighting.cryptid.profileImg 'assets/images/cryptids/blank_th.png'}}"
          alt="{{sighting.cryptid.name}}" width="100%" height="100%">
        <div class="caption">
          <h3>{{sighting.cryptid.name}}</h3>
          {{#if sighting.location}}
            <h3>{{sighting.location}}</h3>
            <p>{{moment-from sighting.sightedAt}}</p>
          {{else}}
            <h3 class="text-danger">Bogus Sighting</h3>
          {{/if}}
        </div>
        {{#link-to 'sighting.edit' sighting.id tagName="button"
          class="btn btn-success btn-block"}}
          Edit
        {{/link-to}}
      </div>
...
```

Load [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings) and check out your new <samp class="guibutton">Edit</samp> button ([Figure 24.4](#ch24s02.html_fig-sighting-list-edit-button "Figure 24.4  Sightings list with Edit button")).

**Figure 24.4  Sightings list with Edit button**

![Sightings list with Edit button](Tracker/Controllers/img/ember-controller-edit-list.png)

Now add the dynamic parameters to the edit route in <samp class="filename">router.js</samp>.

```
...
  this.route('sighting', function() {
    this.route('edit', {path: "sightings/:sighting_id/edit"});
  });
...
```

Add the retrieval methods for sightings, cryptids, and witnesses to the route in <samp class="filename">app/routes/sighting/edit.js</samp>:

```
...
export default Ember.Route.extend({
  model(params) {
    return Ember.RSVP.hash({
      sighting: this.store.findRecord('sighting', params.sighting_id),
      cryptids: this.store.findAll('cryptid'),
      witnesses: this.store.findAll('witness')
    });
  }
});
```

Next, add the form elements to <samp class="filename">app/templates/sighting/edit.hbs</samp>, as you did when creating a new sighting.

```
{{outlet}}
<h1>Edit Sighting:
  <small>
    {{model.sighting.location}} -
    {{moment-from model.sightin.sightedAt}}
  </small>
</h1>
<form {{action "update" model on="submit"}}>
  <div class="form-group">
    <label for="name">Cryptid</label>
    {{input value=model.sighting.cryptid.name type="text" class="form-control"
      name="location" disabled=true}}
  </div>
  <div class="form-group">
    <label>Witnesses</label>
    {{#each model.sighting.witnesses as |witness|}}
      {{input value=witness.fullName type="text" class="form-control"
        name="location" disabled=true}}
    {{/each}}
  </div>
  <div class="form-group">
    <label for="location">Location</label>
    {{input value=model.sighting.location type="text" class="form-control"
      name="location" required=true}}
  </div>
  <button type="submit" class="btn btn-info btn-block">Update</button>
  <button {{action 'cancel'}} class="btn btn-block">Cancel</button>
</form>
```

You are almost there; the controller is the final step. You need to set the form `{{action}}` to `update`. Also, because Tracker is only going to allow location changes at this point, you will render the cryptid and witnesses in disabled input fields.

Create the controller:

```
ember g controller sighting/edit
```

Open <samp class="filename">app/controllers/sighting/edit.js</samp> and add the `update` and `cancel` actions:

```
import Ember from 'ember';

export default Ember.Controller.extend({
  sighting: Ember.computed.alias('model.sighting'),
  actions: {
    update() {
      if(this.get('sighting').get('hasDirtyAttributes')){
        this.get('sighting').save().then(() => {
          this.transitionToRoute('sightings');
        });
      }
    },
    cancel() {
      if(this.get('sighting').get('hasDirtyAttributes')){
        this.get('sighting').rollbackAttributes();
      }
      this.transitionToRoute('sightings');
    }
  }
});
```

Similar to creating model records, updating is as easy as calling <samp class="methodname">save</samp>. You only want to call the API when your record has changed, hence `sighting.get('hasDirtyAttributes')`. <samp class="application">Ember</samp> has thought of it all!

Notice the use of `Ember.computed.alias`. This is a computed property assigned so you do not have to type as much when calling on the active `sighting`. You can alias any property to get quick access, especially if the properties are nested.

## Deleting a Sighting

Every so often a reported cryptid sighting turns out to be a hoax. While this may be rare, you do need a way to delete old or debunked data. Recall from [Chapter 21](#ch21.html "21 Models and Data Binding") that destroying records is achieved by calling <samp class="methodname">record.destroyRecord</samp>. Simple enough.

Make it so: Add a delete button to your template in <samp class="filename">app/templates/sighting/edit.hbs</samp>.

```
 <button type="submit" class="btn btn-info btn-block">Update</button>
  <button {{action 'cancel'}} class="btn btn-block">Cancel</button>
</form>

<hr>
<button {{action 'delete'}} class="btn btn-block btn-danger">
  Delete
</button>
```

In addition to the new button, you added a horizontal rule (a simple line) between the form elements to separate the <samp class="guibutton">Update</samp> and <samp class="guibutton">Cancel</samp> buttons from the new <samp class="guibutton">Delete</samp> button. The `<hr>` is a UI tool you are using to indicate that deleting a sighting is a separate process from editing a sighting.

Next, add the `delete` action to your controller, <samp class="filename">app/controllers/sighting/edit.js</samp>:

```
...
    cancel() {
      if(this.get('sighting').get('hasDirtyAttributes')){
        this.get('sighting').rollbackAttributes();
      }
      this.transitionToRoute('sightings');
    },
    delete() {
      var self = this;
      if (window.confirm("Are you sure you want to delete this sighting?")) {
        this.get('sighting').destroyRecord().then(() => {
          self.transitionToRoute('sightings');
        });
      }
    }
  }
});
```

The `delete` action adds a `window.confirm` to get the user’s confirmation. Aside from the conditional, this action is like the others: get the model, call a method, and add an async `then` to call when the API request is done.

Now navigate to <samp class="literal">http://localhost:4200/sightings</samp> and click the <samp class="guibutton">Edit</samp> button for one of your sightings to view the <samp class="filename">app/templates/sightings/edit.hbs</samp> and its new <samp class="guibutton">Delete</samp> button ([Figure 24.5](#ch24s03.html_fig-edit-sightings-form "Figure 24.5  Edit Sighting form")).

**Figure 24.5  Edit Sighting form**

![Edit Sighting form](Tracker/Controllers/img/ember-controller-edit-template.png)

The cycle is now complete: creation to destruction.

## Route Actions

Actions are not just for controllers. Routes can declare the actions for templates and override lifecycle actions. When an action is called, it bubbles up from the template to the controller to the route and to parent routes.

A route can therefore act as the controller when a controller definition is not needed. This might seem contradictory after all our talk about separating the application concerns, but <samp class="application">Ember</samp> really split the controller’s job into two units: route information and controller logic. Sometimes the route file has more logic and sometimes the controller has more logic. The file separation allows for small digestible chunks of code when the other file has numerous actions or decorators.

To see how this works, you are going to move the `create` and `cancel` actions from <samp class="filename">app/controllers/sightings/new.js</samp> to <samp class="filename">app/routes/sightings/new.js</samp>. Making this change will also broaden your perspective on methods and objects passed between these files – and it will be good practice for when you only want a route file and components controlling an application view. (You will learn about components in the next chapter.)

First, add the actions to <samp class="filename">app/routes/sightings/new.js</samp>:

```
import Ember from 'ember';

export default Ember.Route.extend({
  model() {
  ...
  },
  sighting: Ember.computed.alias('controller.model.sighting'),
  actions: {
    willTransition() {
      var sighting = this.get('controller.model.sighting');
      if(sighting.get('hasDirtyAttributes')) {
        sighting.deleteRecord();
      }
    },
    create() {
      var self = this;
      this.get('sighting').save().then(function(data) {
        self.transitionTo('sightings');
      });
    },
    cancel() {
      this.get('sighting').deleteRecord();
      this.transitionToRoute('sightings');
    }
  }
});
```

You also created an `Ember.computed.alias` for the sighting object in the route. The major difference in accessing the controller’s `model.sighting` object from the route is where that object lives. The `model` on the “new” route is not the same as the model on the “new” controller. To access the `sighting` object you use `get('controller.model.sighting')`. Creating an alias to this object will save you from typing that out each time.

Now, delete the actions from <samp class="filename">app/controllers/sightings/new.js</samp>:

```
import Ember from 'ember';

export default Ember.Controller.extend({
  actions: {
    create() {
      var self = this;
      this.get('model.sighting').save().then(function() {
        self.transitionToRoute('sightings');
      });
    },
    cancel() {
      this.get('model.sighting').deleteRecord();
      this.transitionToRoute('sightings');
    }
  }
});
```

Make sure your application has reloaded (or restart `ember server`). Navigate to [<samp class="uri">http://​localhost:4200/​sightings/​new</samp>](http://localhost:4200/sightings/new) and create a new sighting to make sure you can still run the route actions.

At this point, <samp class="filename">app/controllers/sightings/new.js</samp> is irrelevant. You can delete this file. <samp class="application">Ember</samp> will still create the controller object while the app is running, but you do not need the empty file cluttering up the <samp class="filename">app</samp> directory.

This chapter focused on <samp class="application">Ember</samp> controllers to show you how to create actions and properties for your templates, transition to new routes after saving data, and destroy records on cancel or a route change. Actions allow you to change the model data backing your application with a simple callback. The controller properties allow you to have page-specific properties before adding relationships to the model data. Last, you have completed the basic CRUD actions of updating and deleting records from an edit route.

<samp class="application">Ember</samp> allows rapid development by making the creation of controllers optional for when you need these specific details for your routes. Beyond these features, controllers allow you to fine-tune your views and have control over your model data. Actions are the key to user interaction. Furthermore, actions can live on routes, controllers, and components – which are the subject of the next (and final) chapter.

## Bronze Challenge: Sighting Detail Page

Create a sighting detail page with <samp class="filename">app/templates/sighting/index.hbs</samp> and <samp class="filename">app/routes/sighting.js</samp> to display the cryptid image, location, and list of witnesses. Add an <samp class="guibutton">Edit</samp> button for good measure. (Hint: You can add your actions on the route.)

## Silver Challenge: Sighting Date

When creating and editing a sighting, add a `sightingDate` property to the controller and an input that is bound to that property. Use either a basic text input or `input[type="date"]` to capture the sighting date. Convert the date to an ISO8601 string using <samp class="application">moment</samp> and set the sighting property `sightingAt` with that date string.

## Gold Challenge: Adding and Removing Witnesses

When creating a new sighting, build a list of witnesses from a `select onchange` action. Create a new property for the list of witnesses. On create, add the objects to the sightings property `witnesses`.

While on the page, make the collection of selected witnesses render as a list with a <samp class="guibutton">Remove</samp> button. Use the `select` element as a way to add to the list while removing the options from the `select` element. You will need two actions: `addWitness` and `removeWitness`.

# <samp class="chapter_number">25</samp>
<samp class="chapter_name">Components</samp>

Components are objects that hold the properties of controllers and views in <samp class="application">Ember</samp>. The concept behind components is to have reusable DOM elements that have their own context or scope. Components accept attributes to customize the content rendered inside their templates. Also, components can allow actions to be assigned to properties from a parent controller or parent route ([Figure 25.1](#ch25.html_fig-component-prop "Figure 25.1  Component property")).

**Figure 25.1  Component property**

![Component property](Tracker/Components/img/component-reusable-property-change.png)

As you assess the architecture of your application, you will start to see elements grouped together with minor differences throughout many routes and templates. If a grouping of elements can be removed from the template and described with variables depicting the elements’ state, it is a prime candidate to become a component.

This chapter will show you relatively simple examples of wrapping DOM elements in JavaScript objects to be used across multiple routes. Much like the helpers you saw in [Chapter 23](#ch23.html "23 Views and Templates"), components take arguments in the form of attributes to produce HTML. They also have the added feature of having their own actions and scoped properties to update themselves upon user interaction.

This chapter will only show you the tip of the iceberg of scalable application development. <samp class="application">Ember</samp> applications in production rely heavily on components to create consistent user interfaces and maintainable code bases that sometimes span hundreds of routes. However, the examples you see here will provide a foundation of understanding for future projects where you want to turn your route templates into reusable pages or single elements.

## Iterator Items as Components

An example of grouped elements that can often become a component is elements rendered in `{{#each}}` iterators. There may be a `<div>` container element with a particular `className` based on the iterator object, a title, an image path, a button with an action, and/or styles based on the object’s property states. To make these easily reusable, you can wrap all the DOM code in a component template and create a component JavaScript file to handle the decorators and actions that a controller would normally handle.

Your sightings list is built with an `{{#each}}` iterator, and you are going to create your first component to represent a sighting list item. Start by generating a component via <samp class="application">Ember CLI</samp> in the terminal:

```
ember g component listing-item
```

This creates three files: <samp class="filename">app/components/listing-item.js</samp>, <samp class="filename">app/templates/components/listing-item.hbs</samp>, and the test file <samp class="filename">tests/integration/components/listing-item-test.js</samp>.

Now that the component is created, you need to find the code you want the component to replace. Open <samp class="filename">app/templates/sightings/index.hbs</samp> and locate this block of code. You will be moving part of this code to the component in a moment. For now, just take a look at it.

```
<div class="row">
  {{#each model as |sighting|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        <img class="media-object thumbnail" src="{{if sighting.cryptid.profileImg
          sighting.cryptid.profileImg 'assets/images/cryptids/blank_th.png'}}"
          alt="{{sighting.cryptid.name}}" width="100%" height="100%">
        <div class="caption">
          <h3>{{sighting.cryptid.name}}</h3>
          {{#if sighting.location}}
            <h3>{{sighting.location}}</h3>
            <p>{{moment-from sighting.sightedAt}}</p>
          {{else}}
            <h3 class="text-danger">Bogus Sighting</h3>
          {{/if}}
        </div>
        {{#link-to 'sighting.edit' sighting.id tagName="button"
          class="btn btn-success btn-block"}}
          Edit
        {{/link-to}}
      </div>
    </div>
  {{/each}}
</div>
```

The container `<div>` with the `col-xs-12` class (that is, the shaded <div>) needs to be on this specific page. It is a visual container for the layout, specifying the size of its content. If you were to add this container to your sightings list component, the container size would be fixed for every instance of the component across the site.

However, the `<div class="media well">` container and its contents can be moved to a component. This component can then be added to any size of container while holding the characteristics of a single item in a list. The component will contain the major elements of the item being listed – mainly the `media` container and the image, title, and <samp class="guibutton">Edit</samp> button.

Open <samp class="filename">app/templates/components/listing-item.hbs</samp> and begin by adding the image and cryptid name:

```
<img class="media-object thumbnail" src="{{imagePath}}" alt="{{name}}"
  width="100%" height="100%">
<div class="caption">
  <h3>{{name}}</h3>
  {{yield}}
</div>
```

A component represents a single DOM element. Everything in the component template, then, is a child of that DOM element. By default, <samp class="application">Ember</samp>’s HTMLBars uses JavaScript to create `<div>` elements and renders the component template inside them.

The code you just wrote adds an image and a caption with a name to the `<div>` element created by a `{{#listing-item}}` component. Just like other templates, the component has dynamic portions that are variables you will pass in. (We will discuss the `{{yield}}` in a moment.)

When you add this component to the route template, it will render this:

```
<div>
  <img class="media-object thumbnail" src="[cryptid's imagePath string]"
    alt="[cryptid's name string]" width="100%" height="100%">
  <div class="caption">
    <h3>[cryptid's name string]</h3>
    {{yield}}
  </div>
</div>
```

The dynamic portions of the template, `{{name}}` and `{{imagePath}}`, will be attributes provided to the component. The `{{yield}}` is where you can pass child elements to the component to render in a specific location of the DOM node structure. The component template file acts a layout or master set of elements, and the `{{yield}}` is for elements you need to add with each instance of the component. You will use it later in the chapter.

While this is not exactly the markup you are replacing in <samp class="filename">app/templates/sightings/index.hbs</samp>, it is a good starting point.

Replace your existing code in <samp class="filename">app/templates/sightings/index.hbs</samp> with the component.

```
<div class="row">
  {{#each model as |sighting|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        <img class="media-object thumbnail" src="{{if sighting.cryptid.profileImg
          sighting.cryptid.profileImg 'assets/images/cryptids/blank_th.png'}}"
          alt="{{sighting.cryptid.name}}" width="100%" height="100%">
        <div class="caption">
          <h3>{{sighting.cryptid.name}}</h3>
          {{#if sighting.location}}
            <h3>{{sighting.location}}</h3>
            <p>{{moment-from sighting.sightedAt}}</p>
          {{else}}
            <h3 class="text-danger">Bogus Sighting</h3>
          {{/if}}
        </div>
        {{#link-to 'sighting.edit' sighting.id tagName="button"
          class="btn btn-success btn-block"}}
          Edit
        {{/link-to}}
      </div>
      {{#listing-item imagePath=sighting.cryptid.profileImg
        name=sighting.cryptid.name}}
      {{/listing-item}}
    </div>
  {{/each}}
</div>
```

You have replaced a lot of code with a single line. Some functionality was removed in the process, but you will fix that soon. The next step is adding the container styles back on the component element. It is missing the `"media"` and `"well"` <samp class="application">Bootstrap</samp> styles.

Open <samp class="filename">app/components/listing-item.js</samp> and add a <samp class="varname">classNames</samp> property to the `listing-item` component:

```
import Ember from 'ember';

export default Ember.Component.extend({
  classNames: ["media", "well"]
});
```

The property <samp class="varname">classNames</samp> passes its value to the <samp class="varname">classNames</samp> attribute of the `<div>` element created by the component.

Now the rendered component looks like this:

```
<div class="media well">
  <img class="media-object thumbnail" src="[imagePath string]" alt="[name string]"
    width="100%" height="100%">
  <div class="caption">
    <h3>[name string]</h3>
    {{yield}}
  </div>
</div>
```

Next, you will add elements to the `{{yield}}` section of the component template to make the implementation of this component instance unique to the sightings route. First, in <samp class="filename">app/templates/sightings/index.hbs</samp>, add the component’s contextual content that will render in the `{{yield}}`:

```
...
      {{#listing-item imagePath=sighting.cryptid.profileImg
        name=sighting.cryptid.name}}
        {{#if sighting.location}}
          <h3>{{sighting.location}}</h3>
            <p>{{moment-from sighting.sightedAt}}</p>
        {{else}}
          <h3 class="text-danger">Bogus Sighting</h3>
        {{/if}}
        {{#link-to 'sighting.edit' sighting.id tagName="button"
          class="btn btn-success btn-block"}}
          Edit
        {{/link-to}}
      {{/listing-item}}
```

This code, which should look familiar, reinstates the sighting location and time as well as the `Edit` button.

## Components for DRY Code

Time to DRY up your code.

Say what? DRY is a programming principle that stands for “don’t repeat yourself.” In other words, if you write something down, write it down in just one place.

Both the listings for sightings and cryptids use an element with `class="media well"` with images and titles. So this is some code that can be DRYed up. The component does not match exactly to the cryptid listing item, but that is where the `{{yield}}` comes in.

Add the new `{{#listing-item}}` component to the cryptids listing. In <samp class="filename">app/templates/cryptids.hbs</samp>, replace the `<div class="media well">` element and its child elements:

```
<div class="row">
  {{#each model as |cryptid|}}
    <div class="col-xs-12 col-sm-3 text-center">
      <div class="media well">
        {{#link-to 'cryptid' cryptid.id}}
          <img class="media-object thumbnail"
            src="{{if cryptid.profileImg cryptid.profileImg
            'assets/images/cryptids/blank_th.png'}}"
            alt="{{cryptid.name}}" width="100%" height="100%">
        {{/link-to}}
        <div class="caption">
          <h3>{{cryptid.name}}</h3>
        </div>
      </div>
      {{#link-to 'cryptid' cryptid.id}}
        {{listing-item imagePath=cryptid.profileImg name=cryptid.name}}
      {{/link-to}}
    </div>
  {{else}}
    <div class="jumbotron">
      <h1>No Creatures</h1>
    </div>
  {{/each}}
</div>
```

Did you notice that there is a difference between the way you referenced your component in the two templates? The sightings iterator uses the `{{yield}}` to add elements inside the `<div class="caption">` and the cryptids template does not. When you want a component to only use the code in the component template file, you can use an <samp class="firstterm">inline component</samp>, written without the hash (`#`) – `{{listing-item}}` – as you did here. With this syntax, there is no closing HTMLBars element (`{{/listing-item}}`).

To add a link to the component, you wrapped the component with a `{{#link-to}}`. In the old iterated elements, only the image linked to the cryptid detail page. Now the entire element links to the cryptid detail. This example shows the flexibility of components to conform to the context of different route templates while rendering similar content. You could also add more attributes to the component to account for the need for a link inside the component template.

## Data Down, Actions Up

Next, you will add a component to be controlled by a state change in the application. Specifically, you will create a flash alert to display a message when you create a new listing.

One of the tenets of components is “data (or state) down and actions up.” Unlike controllers, components should not change the state of an application; they should pass changes up through actions. The state of a component, on the other hand, should be passed in from a parent template – data down ([Figure 25.2](#ch25s03.html_fig-component-prop-action "Figure 25.2  Component Data Down Actions Up")).

**Figure 25.2  Component Data Down Actions Up**

![Component Data Down Actions Up](Tracker/Components/img/component-reusable-data-down-action-up.png)

A component could easily replace a controller by passing a route’s model directly to the component without the need for a controller’s decorators or actions.

You will create a new component and actions and add the component to the <samp class="filename">app/templates/application.hbs</samp> file to render a global message when a new sighting is created.

First, generate the new component in the terminal:

```
ember g component flash-alert
```

The `{{flash-alert}}` component will be a container element for a `<strong>` alert title and a text message.

Open and edit <samp class="filename">app/templates/components/flash-alert.hbs</samp> to make it so:

```
{{yield}}
<strong>{{typeTitle}}!</strong> {{message}}
```

Edit the component file <samp class="filename">app/components/flash-alert.js</samp> and add `classNames`:

```
import Ember from 'ember';

export default Ember.Component.extend({
  classNames: ["alert"]
});
```

Now the component will render the following elements:

```
<div class="alert">
  <strong>{{typeTitle}}!</strong> {{message}}
</div>
```

## Class Name Bindings

This container gives the impression that it will display the correct message, but the styling will not give you context to its alert type. <samp class="application">Bootstrap</samp> has state-variant styles for alert components: `"alert-success"`, `"alert-info"`, `"alert-warning"`, and `"alert-danger"`.

In order to set the correct alert type, you will add one of these classes with a computed property and class name binding.

Start with the computed property in <samp class="filename">app/components/flash-alert.js</samp>:

```
...
export default Ember.Component.extend({
  classNames: ["alert"],
  typeClass: Ember.computed('alertType', function() {
    return "alert-" + this.get('alertType');
  })
});
```

Here, you added a computed property for `typeClass`, which will be used to add a `className` to the component’s `<div>` element. The computed property expects a property called `alertType`, which you will add later, and returns a string with `"alert-"` prefixing the `"alertType"`. This allows you to pass in a property with a value of `"success"`, `"info"`, `"warning"`, or `"danger"` to supply the context of the alert. You will be using this same `alertType` property for another computed property.

Finally, add the `className` bindings in the <samp class="filename">app/components/flash-alert.js</samp> file for `className`s bound to component properties:

```
...
export default Ember.Component.extend({
  classNames: ["alert"],
  classNameBindings: ['typeClass'],
  typeClass: Ember.computed('alertType', function() {
    return "alert-" + this.get('alertType');
  })
});
```

This adds a `className` to the `classNames` array from the value of the computed property `typeClass`. When you set the `alertType` property, the style changes on the component.

Using `classNameBindings` is specific to the `classNames` attribute on an element. There is a complementary <samp class="application">Ember</samp> component property for the other attributes: `attributeBindings`. You can bind component properties to the attributes of the component’s element. A basic example is setting the `href` of a link to a `computedProperty`. For example:

```
export default Ember.Component.extend({
  attributeBindings: ['href', 'customHREF:href'],
  href: "http://www.mydomain.com",
  customHREF: "http://www.mydomain.com"
});
```

With attribute bindings you can set all the component’s attributes with the state data passed into the component. To explore this further, check out the <samp class="application">Ember</samp> documentation online.

Next, add a computed property to display the alert type as a string. The component template is expecting a property `typeTitle`, so you have to add this computed property to <samp class="filename">app/components/flash-alert.js</samp>:

```
import Ember from 'ember';

export default Ember.Component.extend({
  ...
  typeClass: Ember.computed('alertType', function() {
    return "alert-" + this.get('alertType');
  }),
  typeTitle: Ember.computed('alertType', function() {
    return Ember.String.capitalize(this.get('alertType'));
  })
});
```

Now you have a string in the message bound to the alert type that is capitalized and is a `<strong>` element in the template. You have bound a class name and a decorated property to the component by computing the value of each from data passed into the component via the `alertType` property.

Next you need to add your component to your page in <samp class="filename">app/templates/application.hbs</samp>:

```
<header>
  ...
</header>
<div class="container">
  {{flash-alert}}
  {{outlet}}
</div>
```

This component is an inline component, meaning there will be no elements to render in the `{{yield}}` and the component template does not need a `{{yield}}`.

## Data Down

At this point the alert does not have any state data to render content and `classNames`, only containers. Pass in the state of the component in <samp class="filename">app/templates/application.hbs</samp>:

```
...
  {{flash-alert message="This is the Alert Message" alertType="success"}}
  {{outlet}}
</div>
```

Start the server and open your browser to [<samp class="uri">http://​localhost:4200/​sightings</samp>](http://localhost:4200/sightings) to see the `{{flash-alert}}` component rendered with the inline data you supplied ([Figure 25.3](#ch25s05.html_fig-flash-alert "Figure 25.3  Flash alert")).

**Figure 25.3  Flash alert**

![Flash alert](Tracker/Components/img/component-flash-alert.png)

Now that the alert is on the screen, you want to set the properties of `message` and `alertType` dynamically. You will need an application controller to achieve this. Using the <samp class="application">Ember CLI</samp> generator, add the controller:

```
ember g controller application
```

The application controller will maintain the dynamic state of the `{{flash-alert}}` component. The controller will need properties to maintain the state of the alert. Add the following property to <samp class="filename">app/controllers/application.js</samp>:

```
import Ember from 'ember';

export default Ember.Controller.extend({
  alertMessage: null,
  alertType: null,
  isAlertShowing: false
});
```

You added properties that will be set by an action. Now you have controller properties to pass to the `flash-alert` component in <samp class="filename">app/templates/application.hbs</samp>:

```
...
</header>
<div class="container">
  {{#if isAlertShowing}}
    {{flash-alert message="This is the Alert Message" alertType="success"}}
                          alertMessage alertType=alertType}}
  {{/if}}
  {{outlet}}
</div>
```

The controller’s properties can now be set from an action. The application only needs to render the component when the `isAlertShowing` property is set to `true` and when the other properties have values. The action to set these properties will be coming from controllers all over the application. How do you bubble these actions up? <samp class="application">Ember</samp> does it for you ([Figure 25.4](#ch25s05.html_fig-flash-alert-process "Figure 25.4  Flash alert process")).

**Figure 25.4  Flash alert process**

![Flash alert process](Tracker/Components/img/components_action_bubble.png)

You have to add an action to a route. You can call an action from a controller, and it will hit the current controller, then the current route, the parent routes, then the application route.

Because your `flash-alert` is in the <samp class="filename">app/templates/application.hbs</samp>, you need an application route. Create one:

```
ember g route application
```

You will see this message returned in the command line:

```
[?] Overwrite app/templates/application.hbs?
```

Enter `n` or `no` to continue. You do not want to overwrite the template file you just created. You only want to add the JavaScript file <samp class="filename">app/routes/application.js</samp>.

Next you will need to edit the route in <samp class="filename">app/routes/application.js</samp>:

```
import Ember from 'ember';

export default Ember.Route.extend({
  actions: {
    flash(data){
      this.controller.set('alertMessage', data.message);
      this.controller.set('alertType', data.alertType);
      this.controller.set('isAlertShowing', true);
    }
  }
});
```

## Actions Up

Now you have an action to set the `flash-alert` to display the appropriate message. You just need to pass the action some data. That data will be an object with keys for `alertType` and `message`.

The `alertType` will be a part of both the `message` and the style with <samp class="application">Bootstrap</samp> alert variants: `"success"`, `"warning"`, `"info"`, or `"danger"`. Calling the action from a controller will look like this:

```
this.send('flash', {alertType: "success", message: "You Did It! Hooray!"});
```

You will be adding the call to the application action after creating a new sighting. In <samp class="filename">app/routes/sightings/new.js</samp>, add the following:

```
...
    create() {
      var self = this;
      this.get('sighting').save().then(function(data){
        self.send('flash', {alertType: "success", message: "New sighting."});
        self.transitionTo('sightings');
      });
...
```

Now navigate to create a new sighting by clicking the <samp class="guibutton">New Sighting</samp> button. Select a cryptid and a witness, type a new location, and click <samp class="guibutton">Save</samp>. Once the sighting is saved in the database, the app will route you to the list of sightings with a new flash message at the top of the list ([Figure 25.5](#ch25s06.html_fig-new-sighting-alert "Figure 25.5  Flash alert – new sighting")).

**Figure 25.5  Flash alert – new sighting**

![Flash alert – new sighting](Tracker/Components/img/component-flash-alert-new.png)

The last step is adding the action and event that will remove the alert from the screen. You only want to show the `flash-alert` after you have created a new message, so you need to flip the switch to hide the alert when you remove it.

In <samp class="filename">app/controllers/application.js</samp>, add an action called `removeAlert`:

```
...
export default Ember.Controller.extend({

  alertMessage: null,
  alertType: null,
  isAlertShowing: false,
  actions: {
    removeAlert(){
      this.set('alertMessage', "");
      this.set('alertType', "success");
      this.set('isAlertShowing', false);
    }
 }
});
```

This will set `isAlertShowing` to false, set the `alertMessage` to an empty string, and set the `alertType` to `"success"`.

Next, send the `removeAlert` action to the component. Add the following to <samp class="filename">app/templates/application.hbs</samp>:

```
...
</header>
<div class="container">
  {{#if isAlertShowing}}
    {{flash-alert message=alertMessage alertType=alertType}}
      close=(action "removeAlert")}}
  {{/if}}
  {{outlet}}
</div>
```

The syntax `close=(action "removeAlert")` probably looks weird. This is new to <samp class="application">Ember</samp> 2.0 and is called a <samp class="firstterm">closure action</samp>. The function literal is passed through to be called from the component as an attribute named `close`, much like an alias.

Older versions of <samp class="application">Ember</samp> had a more complex version of this flow. Closure actions are more than just functions passed from an object as an argument under the hood. To find out more about closure actions, visit the EmberJS blog post about the features for version 1.13 and 2.0 at [<samp class="uri">emberjs.com/​blog/​2015/​06/​12/​ember-1-13-0-released.html</samp>](http://emberjs.com/blog/2014/06/12/ember-1-13-0-released.html).

Next, you need to call this action from the component. Components are instances of DOM elements; thus, they have key/value pairs representing DOM element events. You can add a declaration of a `click` event listener and <samp class="application">Ember</samp> will add the listener to the `<div>` element wrapping the template. Add the following to <samp class="filename">app/components/flash-alert.js</samp>:

```
import Ember from 'ember';

export default Ember.Component.extend({
  ...
  typeTitle: Ember.computed('alertType', function() {
    return Ember.String.capitalize(this.get('alertType'));
  }),
  click() {
    this.get('close')();
  }
});
```

The property `close`, when called, will invoke the action `"removeAlert"` defined on the application controller. By using a closure action, you have assigned a component’s property to a function defined in the parent controller and tied the component’s functionality to the scope of its parent. You can add a `flash-alert` at any level and assign different functionality to `close` based on its context.

You have added a component that responds to data going down to customize the component and to actions going up to set the external state of the component from the parent controller. This the lifecycle of a component: data down, actions up. Keep this pattern in mind when creating components.

Throughout the Application Architecture chapters you have learned about the structure of modern applications built with <samp class="application">Ember</samp>. You have learned about the patterns of MVC and how this framework helps you separate concerns with pre-built JavaScript objects. It also helps you maintain sanity with naming patterns, scaffolding, build tools, and conventions. From here you can feel confident creating a new app with `ember new`. You can dive straight into your application needs modeling data, creating routes, and building components.

The <samp class="application">Ember</samp> community maintains this wonderful framework and continues to build in efficiencies as JavaScript matures. This framework is built by people who have struggled with the same challenges you will face as you hone your JavaScript skills. Remember to ask questions when something does not work, help fix bugs when you find something that is broken, and give back when you can. You are now part of the greater JavaScript community.

## Bronze Challenge: Customizing the Alert Message

The `{{flash-alert}}` you trigger when adding a sighting is generic. Add the sighting location and date to the message.

## Silver Challenge: Making the NavBar a Component

Make the `NavBar` in the application template a component. Add a property state to show two versions of the navigation. Add conditional statements in the `NavBar` component for showing specific links.

## Gold Challenge: Array of Alerts

Restructure the `flash-alert` component to accept an array of alerts with different alert types and messages. You may need to have multiple warnings on the screen at the same time. Use an `Ember.ArrayProxy` in place of the individual properties setting the alert. Add to the array with the message, type, and a new `index` property so that you can remove the item from the array when you click it.

# <samp class="chapter_number">26</samp>
<samp class="chapter_name">Afterword</samp>

Congratulations! You are at the end of this guide. Not everyone has the discipline to do what you have done and learn what you have learned. Take a quick moment to give yourself a pat on the back.

Your hard work has paid off: You are now a front-end developer.

## The Final Challenge

We have one last challenge for you: Become a <samp class="emphasis">good</samp> front-end developer. Good developers are good in their own ways, so you must find your own path from here on out.

Where might you start? Here are some ideas:

<samp class="emphasis">Write code.</samp> Now. You will quickly forget what you have learned here if you do not apply your knowledge. Contribute to a project or write a simple application of your own. Whatever you do, waste no time: Write code.

<samp class="emphasis">Learn.</samp> You have learned a little bit about a lot of things in this book. Did any of them spark your imagination? Write some code to play around with your favorite thing. Find and read more documentation about it – or an entire book, if there is one. Also, check out the JavaScript Jabber podcast for some thoughtful and entertaining discussion about the latest developments in front-end development ([<samp class="uri">devchat.tv/​js-jabber</samp>](https://devchat.tv/js-jabber)).

<samp class="emphasis">Meet people.</samp> Local meetups are a good place to meet like-minded developers. Lots of top-notch front-end developers are active on Twitter. And you can attend front-end conferences to meet other developers (maybe even us!).

<samp class="emphasis">Explore the open source community.</samp> Front-end development is exploding on [<samp class="uri">www.github.com</samp>](http://www.github.com). When you find a cool library, check out other projects from its contributors. Share your own code, too – you never know who will find it useful or interesting. We find the WDRL (Web Development Reading List) mailing list to be a great way to see what is happening in the front-end community ([<samp class="uri">wdrl.info</samp>](https://wdrl.info/)).

## Shameless Plugs

You can find us on Twitter. Chris is `@radishmouse` and Todd is `@tgandee`.

If you enjoyed this book, check out the other Big Nerd Ranch Guides at [<samp class="uri">www.bignerdranch.com/​books</samp>](http://www.bignerdranch.com/books). We also have a broad selection of week-long courses for developers, where we make it easy to learn a book’s worth of stuff in only a week. And of course, if you just need someone to write great code, we do contract programming, too. For more info, go to [<samp class="uri">www.bignerdranch.com</samp>](http://www.bignerdranch.com).

## Thank You

Without readers like you, our work would not exist. Thank you for buying and reading our book.

# Index

[A](#ix01.html_idx-nav-A) [B](#ix01.html_idx-nav-B) [C](#ix01.html_idx-nav-C) [D](#ix01.html_idx-nav-D) [E](#ix01.html_idx-nav-E) [F](#ix01.html_idx-nav-F) [G](#ix01.html_idx-nav-G) [H](#ix01.html_idx-nav-H) [I](#ix01.html_idx-nav-I) [J](#ix01.html_idx-nav-J) [K](#ix01.html_idx-nav-K) [L](#ix01.html_idx-nav-L) [M](#ix01.html_idx-nav-M) [N](#ix01.html_idx-nav-N) [O](#ix01.html_idx-nav-O) [P](#ix01.html_idx-nav-P) [Q](#ix01.html_idx-nav-Q) [R](#ix01.html_idx-nav-R) [S](#ix01.html_idx-nav-S) [T](#ix01.html_idx-nav-T) [U](#ix01.html_idx-nav-U) [V](#ix01.html_idx-nav-V) [W](#ix01.html_idx-nav-W) [X](#ix01.html_idx-nav-X) [Y](#ix01.html_idx-nav-Y)

### Symbols

+= (concatenation operator), [Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)
. (dot operator), [Accessing DOM Elements](#ch06s06.html)
:focus pseudo-class, [Styling Valid and Invalid Elements](#ch12s04.html)
:hover pseudo-class, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)
:invalid pseudo-class, [Styling Valid and Invalid Elements](#ch12s04.html)
:required pseudo-class, [Styling Valid and Invalid Elements](#ch12s04.html)
<a> tag, [Adding images](#ch02.html_se-setting-up-styles)
<body> tag, [Initial HTML](#ch02.html_se-creating-the-document)
<div> tag

> about, [Adding the detail image](#ch04.html_se-adding-the-detail-image), [Creating the Order Form](#ch09s02.html)

> for styling with Bootstrap, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)

<form> tag, [Creating the Order Form](#ch09s02.html)
<h1> tag, [Initial HTML](#ch02.html_se-creating-the-document)
<head> tag, [Initial HTML](#ch02.html_se-creating-the-document)
<hr> tag, [Deleting a Sighting](#ch24s03.html)
<img> tag, [Adding images](#ch02.html_se-setting-up-styles)
<input> tag

> for checkboxes, [Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)

> for radio buttons, [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

> for range sliders, [Adding a range slider](#ch09s02.html_se-adding-a-slider)

> for reset buttons, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> for submit buttons, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> for text input, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)

> linking to <label> tag, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element), [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

<label> tag

> about, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)

> linking to <input> tag, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element), [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

<link> tag, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)
<meta> tag, [Initial HTML](#ch02.html_se-creating-the-document)
<option> tag, [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)
<script> tag, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)
<section> tag, [Creating the Order Form](#ch09s02.html)
<select> tag, [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)
<span> tag, [Adding content](#ch02.html_se-adding-an-unordered-list)
<style> tag, [Styling Valid and Invalid Elements](#ch12s04.html)
<title> tag, [Initial HTML](#ch02.html_se-creating-the-document)
<ul> tag, [Adding content](#ch02.html_se-adding-an-unordered-list)
= (assignment operator), [Declaring String Variables](#ch06s04.html)
== (loose equality operator), [Listening for the keypress event](#ch07.html_idm494068768944)
=== (strict equality operator), [Listening for the keypress event](#ch07.html_idm494068768944)
@font-face declaration, [Adding a Font](#ch03s09.html)
@import directive, [Configuration](#ch19s04.html)
@media declaration, [Adding a Media Query](#ch05s02.html)
{{#each}} helper, [Loops with {{#each}}](#ch23s03.html_se-loops-with-each)
{{#if}} helper, [Conditionals](#ch23s03.html_se-conditionals)
{{#link-to}} helper, [Links](#ch23s03.html_se-links)
{{action}} helper, [New Sightings](#ch24.html_se-new-sightings)
{{if}} helper, [Binding element attributes](#ch23s03.html_se-binding-element-attributes)
{{outlet}} helper, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)
{{x-select}} component, [New Sightings](#ch24.html_se-new-sightings)
{{yield}} helper, [Iterator Items as Components](#ch25.html_se-iterator-items-as-components)
|| (default/logical or operator), [Adding Modules to a Namespace](#ch08s04.html)

### A

<a> tag, [Adding images](#ch02.html_se-setting-up-styles)
absolute positioning, [Absolute and Relative Positioning](#ch04s03.html)
{{action}} helper, [New Sightings](#ch24.html_se-new-sightings)
actual viewport (see [layout viewport](#ix01.html_pri_idm494069633616))
add method, [Writing the JavaScript to hide the detail image](#ch07.html_idm494068784320)
addEventListener method, [Adding an Event Listener](#ch06s09.html)
afterModel method, [For the More Curious: setupController and afterModel](#ch20s06.html)
Ajax

> about, [Ajax](#ch13.html)

> and jQuery, [XMLHttpRequest Objects](#ch13.html_se-xmlhttprequest-objects)

> XMLHttpRequest API, [XMLHttpRequest Objects](#ch13.html_se-xmlhttprequest-objects)

align-items flexbox property, [Centering the detail image](#ch04s02.html_idm494069756352)
alt attribute, [Adding images](#ch02.html_se-setting-up-styles)
anchor tags (see [<a> tag](#ix01.html_pri_idm494070672832))
anonymous functions

> about, [Adding an Event Listener](#ch06s09.html)

> vs named functions in callbacks, [For the More Curious: Closures](#ch06s15.html)

arguments, [Accepting arguments by declaring parameters](#ch06s07.html_idm494069199216)
arrow functions

> about, [Handling events and sending messages](#ch17s06.html_idm494065676352)

> vs anonymous functions, [For the More Curious: Arrow Functions](#ch17s11.html)

assignment operator (=), [Declaring String Variables](#ch06s04.html)
asynchronous communication

> about, [Ajax](#ch13.html)

> in callbacks, [Adding a callback argument](#ch13s05.html_se-adding-a-callback-argument)

Atom

> autocompletion with emmet, [Initial HTML](#ch02.html_se-creating-the-document), [Adding content](#ch02.html_se-adding-an-unordered-list)

> copying the project path, [Viewing the Web Page in the Browser](#ch02s02.html)

> creating a file, [Setting Up Ottergram](#ch02.html_se-setting-up-your-project-folders)

> creating a folder, [Setting Up Ottergram](#ch02.html_se-setting-up-your-project-folders)

> finding and replacing text, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

> installing, [Installing and Configuring Atom](#ch01s02.html)

> opening a project, [Setting Up Ottergram](#ch02.html_se-setting-up-your-project-folders)

> plug-ins, [Atom plug-ins](#ch01s02.html_idm494071072528)

> snippets, [Adding a Font](#ch03s09.html)

atomic styling

> about, [Styles](#ch03.html)

> flexbox as an exception to, [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504)

attr method, [Model Definitions](#ch21.html_se-model-definitions), [Transforms](#ch22s04.html)
attribute selectors, [Style Inheritance](#ch03s05.html)
attributes

> about, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)

> alt, [Adding images](#ch02.html_se-setting-up-styles)

> autofocus, [Adding autofocus](#ch09s02.html_se-adding-autofocus), [UI Enhancements](#ch10s04.html)

> Boolean, [Adding autofocus](#ch09s02.html_se-adding-autofocus), [The required Attribute](#ch12.html_se-the-required-attribute)

> checked, [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

> class, [Preparing the HTML for Styling](#ch03s02.html)

> data, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

> for, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)

> href, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet), [Adding images](#ch02.html_se-setting-up-styles)

> id, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)

> name, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)

> pattern, [Validating with Regular Expressions](#ch12s02.html)

> placeholder, [Showing example input with placeholder text](#ch09s02.html_se-adding-placeholder-text)

> rel, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)

> required, [The required Attribute](#ch12.html_se-the-required-attribute)

> src, [Adding images](#ch02.html_se-setting-up-styles)

> type, [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

autofocus attribute, [Adding autofocus](#ch09s02.html_se-adding-autofocus), [UI Enhancements](#ch10s04.html)

### B

Babel

> about, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

> for compiling, [Class syntax](#ch17s03.html_se-class-syntax)

> installing, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

Babelify

> about, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

> installing, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

beforeModel method, [beforeModel](#ch20s05.html)
belongsTo method, [Model Definitions](#ch21.html_se-model-definitions)
bind method

> about, [Setting the value of this with bind](#ch08s07.html_se-changing-the-value-of-this-with-.bind), [Registering createOrder as a submit handler](#ch10s03.html_se-registering-createorder-as-a-submit-handler)

> vs call, [Manipulating this with call](#ch11s04.html_se-use-.call-to-manipulate-the-value-of-this)

binding to a port, [Hello, World](#ch15s02.html)
blur event, [Listening for the input event](#ch12s03.html_se-listening-for-the-input-event)
<body> tag, [Initial HTML](#ch02.html_se-creating-the-document)
Boolean attributes, [Adding autofocus](#ch09s02.html_se-adding-autofocus), [The required Attribute](#ch12.html_se-the-required-attribute)
Booleans, [For the More Curious: JavaScript Types](#ch06s17.html)
Bootstrap

> adding, [Adding Bootstrap](#ch09.html_se-adding-bootstrap)

> btn class, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> btn-default class, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> checkbox class, [Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)

> container class, [How Bootstrap works](#ch09.html_se-how-bootstrap-works)

> documentation, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> form-control class, [Adding text input fields](#ch09s02.html_se-adding-a-textfield), [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)

> form-group class, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)

> installing with Bower, [External Libraries and Addons](#ch19s03.html)

borders, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
Bower, installing, [Installing Ember](#ch19s02.html_se-install)
box model, [Your First Styling Rule](#ch03s04.html)
bracket syntax, [Accessing All the Thumbnails](#ch06s10.html)
Brackets, [For the More Curious: Alternatives to Atom](#ch01s06.html)
breakpoints

> removing, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)

> restarting paused code, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)

> setting, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)

browser-sync

> installing, [Installing Node.js and browser-sync](#ch01s05.html)

> running, [Viewing the Web Page in the Browser](#ch02s02.html)

Browserify

> about, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

> and JavaScript dependencies, [Installing jQuery as a Node Module](#ch18.html_se-installing-jquery-as-a-node-module)

> installing, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

browsers

> communication with servers, [Setting Up Your First Project](#ch02.html)

> support for JavaScript versions, [Using ES6 with Babel](#ch17.html)

> support for web technologies, [Documentation and Reference Sources](#ch01s03.html)

> user agent stylesheet, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

bulleted list (see [<ul> tag](#ix01.html_pri_idm494070710688))

### C

call method vs bind, [Manipulating this with call](#ch11s04.html_se-use-.call-to-manipulate-the-value-of-this)
callbacks

> about, [Adding an Event Listener](#ch06s09.html)

> anonymous functions in, [Adding an Event Listener](#ch06s09.html)

> named functions in, [Iterating Through the Array of Thumbnails](#ch06s11.html)

> named vs anonymous functions in, [For the More Curious: Closures](#ch06s15.html)

caniuse.com, [Documentation and Reference Sources](#ch01s03.html)
cdnjs.com, [Creating a Styling Baseline](#ch03.html_se-setting-up-layout)
change event, [Silver Challenge: Showing the Value as the Slider Changes](#ch10s06.html)
checkboxes (see [<input> tag](#ix01.html_pri_idm494067876912))
checked attribute, [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)
child selectors, [Relationship selectors](#ch03s08.html_idm494070191376)
Chrome (see [Google Chrome](#ix01.html_pri_idm494071103888))
class attribute

> (see also individual class names)

> about, [Preparing the HTML for Styling](#ch03s02.html)

> adding dynamically, [Writing the JavaScript to hide the detail image](#ch07.html_idm494068784320)

> as a selector, [Your First Styling Rule](#ch03s04.html)

> removing dynamically, [Showing the detail image again](#ch07.html_idm494068716320)

> vs data attributes, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

class selectors, [Your First Styling Rule](#ch03s04.html)
classes in JavaScript, [Class syntax](#ch17s03.html_se-class-syntax)
classList.add method, [Writing the JavaScript to hide the detail image](#ch07.html_idm494068784320)
classList.remove method, [Showing the detail image again](#ch07.html_idm494068716320)
click event, [Adding an Event Listener](#ch06s09.html)
close event, [Silver Challenge: Closed Connection Alert](#ch17s09.html)
closures, [For the More Curious: Closures](#ch06s15.html)
code comments

> CSS, [Style Inheritance](#ch03s05.html)

> HTML, [Writing the setDetails Function](#ch06s07.html)

> JavaScript, [Writing the setDetails Function](#ch06s07.html)

color formats, [Color](#ch03s07.html)
color functions, [Color](#ch03s07.html)
command line (see [terminal commands](#ix01.html_pri_idm494070992272))
compound (or complex) types, [For the More Curious: JavaScript Types](#ch06s17.html)
concatenation operator (+=), [Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)
connection events, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)
console

> about, [Working in the Console](#ch06s05.html)

> entering line breaks, [Adding an Event Listener](#ch06s09.html)

> logging statements, [Adding an Event Listener](#ch06s09.html)

> opening in the drawer, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback), [Inspecting the Ajax request and response](#ch13s04.html_se-inspecting-the-ajax-request-and-response)

console.log method, [Adding an Event Listener](#ch06s09.html)
constants, [Declaring String Variables](#ch06s04.html), [Creating the ChatForm Class](#ch18s02.html)
constructor method, [Class syntax](#ch17s03.html_se-class-syntax)
constructors

> about, [Constructors](#ch08s05.html), [Creating the ChatForm Class](#ch18s02.html)

> implicit returns, [Constructors](#ch08s05.html)

> naming conventions, [Constructors](#ch08s05.html)

> prototype property, [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)

content delivery networks, [Creating a Styling Baseline](#ch03.html_se-setting-up-layout)
controllers in MVC, [Introduction to MVC and Ember](#ch19.html)
create method, [New Sightings](#ch24.html_se-new-sightings)
createRecord method, [createRecord](#ch21s02.html)
crypto-js, [Using Gravatars](#ch18s04.html)
CSS

> about, [Setting Up Ottergram](#ch02.html_se-setting-up-your-project-folders)

> history, [For the More Curious: CSS Versions](#ch02s04.html)

> properties (see [properties](#ix01.html_pri_idm494070466352))

> selectors (see [selectors (in CSS)](#ix01.html_pri_idm494070477408))

> styling rules, [Anatomy of a Style](#ch03s03.html)

CSS transitions

> creating, [State Changes with CSS Transitions](#ch07s02.html)

> triggering with JavaScript, [Triggering transitions with JavaScript](#ch07s02.html_se-triggering-with-javascript)

cubic-bezier property, [Custom Timing Functions](#ch07s03.html)
cubic-bezier.com, [Custom Timing Functions](#ch07s03.html)

### D

data attributes

> about, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

> accessing DOM elements with, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

> vs class attributes, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

debugging

> breakpoints
> 
> > (see also [breakpoints](#ix01.html_pri_idm494068133872))

> Chrome debugger, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)

declaration blocks, [Anatomy of a Style](#ch03s03.html)
default (logical or) operator (||), [Adding Modules to a Namespace](#ch08s04.html)
Deferred objects

> about, [Promises and Deferreds](#ch14.html_se-promise-foundation)

> callbacks with then, [Registering Callbacks with then](#ch14s03.html), [Using Deferreds with Callback-Only APIs](#ch14s05.html)

DELETE requests, [RESTful Web Services](#ch13s02.html), [Deleting Data from the Server](#ch13s06.html), [Using jQuery’s $.ajax method](#ch13s06.html_se-using-jquerys-.ajax-method)
descendent selectors, [Relationship selectors](#ch03s08.html_idm494070191376)
deserialize method, [Transforms](#ch22s04.html)
destroyRecord method, [For the More Curious: Saving and Destroying Data](#ch21s06.html)
devdocs.io, [Documentation and Reference Sources](#ch01s03.html)
Developer Tools (see [DevTools](#ix01.html_pri_idm494070606144))
DevTools

> about, [The Chrome Developer Tools](#ch02s03.html)

> adding a pseudo-class to an element, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)

> adding an attribute to an element, [Creating styles to hide the detail image](#ch07.html_idm494068824128)

> console (see [console](#ix01.html_pri_idm494069346032))

> device mode, [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

> Ember Inspector, [Installing Ember](#ch19s02.html_se-install), [Starting up the server](#ch19s02.html_se-start-up-the-server), [Ember Inspector](#ch20s03.html)

> opening, [The Chrome Developer Tools](#ch02s03.html)

> viewing Ajax requests, [Inspecting the Ajax request and response](#ch13s04.html_se-inspecting-the-ajax-request-and-response)

display: block property, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools), [Making Images Fit the Window](#ch03s06.html), [Flexbox](#ch04s02.html)
display: flex property, [Creating a flex container](#ch04s02.html_idm494069939200)
display: inline property, [Making Images Fit the Window](#ch03s06.html)
display: inline-block property, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails), [Flexbox](#ch04s02.html)
display: none property, [Creating styles to hide the detail image](#ch07.html_idm494068824128)
<div> tag

> about, [Adding the detail image](#ch04.html_se-adding-the-detail-image), [Creating the Order Form](#ch09s02.html)

> for styling with Bootstrap, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)

doctype, [Initial HTML](#ch02.html_se-creating-the-document)
document object, [Accessing DOM Elements](#ch06s06.html)
document object model (DOM), [Style Inheritance](#ch03s05.html), [Accessing DOM Elements](#ch06s06.html)
documentation resources

> caniuse.com, [Documentation and Reference Sources](#ch01s03.html)

> html5please.com, [Documentation and Reference Sources](#ch01s03.html)

> Mozilla Developer Network, [Documentation and Reference Sources](#ch01s03.html)

> stackoverflow.com, [Documentation and Reference Sources](#ch01s03.html)

dot operator (.), [Accessing DOM Elements](#ch06s06.html)
dropdown menu form fields (see [<select> tag](#ix01.html_pri_idm494067745648))
DS.attr method, [Model Definitions](#ch21.html_se-model-definitions), [Transforms](#ch22s04.html)
DS.belongsTo method, [Model Definitions](#ch21.html_se-model-definitions)
DS.hasMany method, [Model Definitions](#ch21.html_se-model-definitions)
DS.hasOne method, [Model Definitions](#ch21.html_se-model-definitions)

### E

{{#each}} helper, [Loops with {{#each}}](#ch23s03.html_se-loops-with-each)
ease-(in/out/in-out) timing functions, [Custom Timing Functions](#ch07s03.html)
element selectors, [Style Inheritance](#ch03s05.html)
elements property, [UI Enhancements](#ch10s04.html)
Ember

> about, [Ember: An MVC Framework](#ch19s02.html)

> actions property, [New Sightings](#ch24.html_se-new-sightings)

> adapters, [Data – Adapters, Serializers, and Transforms](#ch22.html)

> addons, [External Libraries and Addons](#ch19s03.html)

> afterModel method, [For the More Curious: setupController and afterModel](#ch20s06.html)

> ApplicationRoute object, [ember generate](#ch20.html_se-ember-generate)

> attribute binding, [Class Name Bindings](#ch25s04.html)

> beforeModel method, [beforeModel](#ch20s05.html)

> building and running a project, [Starting up the server](#ch19s02.html_se-start-up-the-server)

> class name binding, [Class Name Bindings](#ch25s04.html)

> closure actions, [Actions Up](#ch25s06.html)

> components, [Components](#ch25.html)

> computed properties, [Computed Properties](#ch21s04.html)

> Content Security Policy, [Content Security Policy](#ch22s02.html)

> controllers, [Controllers](#ch24.html)

> create method, [New Sightings](#ch24.html_se-new-sightings)

> createRecord method, [createRecord](#ch21s02.html)

> creating a project, [Creating an Ember application](#ch19s02.html_se-creating-an-ember-application)

> deserialize method, [Transforms](#ch22s04.html)

> destroyRecord method, [For the More Curious: Saving and Destroying Data](#ch21s06.html)

> DS.attr method, [Model Definitions](#ch21.html_se-model-definitions), [Transforms](#ch22s04.html)

> DS.belongsTo method, [Model Definitions](#ch21.html_se-model-definitions)

> DS.hasMany method, [Model Definitions](#ch21.html_se-model-definitions)

> DS.hasOne method, [Model Definitions](#ch21.html_se-model-definitions)

> Ember Data, [Models and Data Binding](#ch21.html), [Data – Adapters, Serializers, and Transforms](#ch22.html)

> .extend method, [ember generate](#ch20.html_se-ember-generate)

> findAll method, [For the More Curious: Retrieving Data](#ch21s05.html)

> findRecord method, [For the More Curious: Retrieving Data](#ch21s05.html)

> generating adapters, [Adapters](#ch22.html_se-adapter)

> generating components, [Iterator Items as Components](#ch25.html_se-iterator-items-as-components)

> generating controllers, [New Sightings](#ch24.html_se-new-sightings)

> generating custom helpers, [Custom Helpers](#ch23s04.html)

> generating models, [Model Definitions](#ch21.html_se-model-definitions)

> generating routes, [ember generate](#ch20.html_se-ember-generate)

> generating serializers, [Serializers](#ch22s03.html)

> get method, [get and set](#ch21s03.html)

> JSONAPIAdapter object, [Data – Adapters, Serializers, and Transforms](#ch22.html), [Adapters](#ch22.html_se-adapter)

> model method, [Assigning Models](#ch20s04.html)

> models, [Models and Data Binding](#ch21.html)

> naming conventions, [Routing, Routes, and Models](#ch20.html)

> nesting routes, [Nesting Routes](#ch20s02.html)

> nesting templates, [Nesting Routes](#ch20s02.html)

> peekAll method, [For the More Curious: Retrieving Data](#ch21s05.html)

> peekRecord method, [For the More Curious: Retrieving Data](#ch21s05.html)

> query method, [For the More Curious: Retrieving Data](#ch21s05.html)

> queryRecord method, [For the More Curious: Retrieving Data](#ch21s05.html)

> route lifecycle hooks, [Routing, Routes, and Models](#ch20.html)

> route method, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)

> Route object, [Assigning Models](#ch20s04.html)

> Router object, [Routing, Routes, and Models](#ch20.html), [ember generate](#ch20.html_se-ember-generate)

> Router.map method, [ember generate](#ch20.html_se-ember-generate)

> save method, [For the More Curious: Saving and Destroying Data](#ch21s06.html)

> serialize method, [Transforms](#ch22s04.html)

> serializers, [Data – Adapters, Serializers, and Transforms](#ch22.html), [Serializers](#ch22s03.html), [Transforms](#ch22s04.html)

> set method, [get and set](#ch21s03.html)

> setupController method, [Assigning Models](#ch20s04.html), [beforeModel](#ch20s05.html), [For the More Curious: setupController and afterModel](#ch20s06.html)

> store object, [createRecord](#ch21s02.html)

> templates, [Configuration](#ch19s04.html), [Views and Templates](#ch23.html)

> transforms, [Data – Adapters, Serializers, and Transforms](#ch22.html)

> transitionToRoute method, [New Sightings](#ch24.html_se-new-sightings)

> URL routing in, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)

> x-select, [New Sightings](#ch24.html_se-new-sightings)

> {{outlet}} helper, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)

Ember CLI Mirage, [For the More Curious: Ember CLI Mirage](#ch22s05.html)
Ember CLI, installing, [Installing Ember](#ch19s02.html_se-install)
Ember Inspector

> about, [Starting up the server](#ch19s02.html_se-start-up-the-server), [Ember Inspector](#ch20s03.html)

> installing, [Installing Ember](#ch19s02.html_se-install)

Ember.computed method, [Computed Properties](#ch21s04.html)
Ember.computed.alias property, [Editing a Sighting](#ch24s02.html)
Ember.Object class, [Models and Data Binding](#ch21.html), [get and set](#ch21s03.html)
enhanced object literals, [Connection handling](#ch17s06.html_se-building-handlers)
Error type, [Configuring instances of FormHandler with a selector](#ch10.html_se-configuring-the-instance-with-a-selector)
escaping characters, [Declaring String Variables](#ch06s04.html)
event delegation, [Writing the addClickHandler method](#ch11s05.html_se-adding-the-event-click-handler)
event listeners, [Adding an Event Listener](#ch06s09.html), [Listening for the keypress event](#ch07.html_idm494068768944)
event objects, [Adding an Event Listener](#ch06s09.html)
events

> about, [Adding an Event Listener](#ch06s09.html)

> blur, [Listening for the input event](#ch12s03.html_se-listening-for-the-input-event)

> change, [Silver Challenge: Showing the Value as the Slider Changes](#ch10s06.html)

> click, [Adding an Event Listener](#ch06s09.html)

> close, [Silver Challenge: Closed Connection Alert](#ch17s09.html)

> connection, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

> input, [Listening for the input event](#ch12s03.html_se-listening-for-the-input-event)

> keydown, [Listening for the keypress event](#ch07.html_idm494068768944)

> keypress, [Listening for the keypress event](#ch07.html_idm494068768944)

> keyup, [Listening for the keypress event](#ch07.html_idm494068768944)

> message, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

> onchange, [New Sightings](#ch24.html_se-new-sightings)

> submit, [Adding the submit Handler](#ch10s02.html)

export keyword, for named exports, [Creating the ChatForm Class](#ch18s02.html)
.extend method, [ember generate](#ch20.html_se-ember-generate)
extends keyword, [User Session Storage](#ch18s06.html)

### F

favicon.ico, [For the More Curious: The favicon.ico](#ch02s05.html)
filtering selectors, [Writing the addClickHandler method](#ch11s05.html_se-adding-the-event-click-handler)
findAll method, [For the More Curious: Retrieving Data](#ch21s05.html)
findRecord method, [For the More Curious: Retrieving Data](#ch21s05.html)
firebase, [For the More Curious: WebSockets as a Service](#ch16s06.html)
flexbox

> about, [Responsive Layouts with Flexbox](#ch04.html)

> display: flex property, [Creating a flex container](#ch04s02.html_idm494069939200)

> flex containers, [Creating a flex container](#ch04s02.html_idm494069939200), [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504)

> flex items, [Creating a flex container](#ch04s02.html_idm494069939200)

> flex shorthand property, [The flex shorthand property](#ch04s02.html_idm494069865184)

> flex-basis property, [The flex shorthand property](#ch04s02.html_idm494069865184)

> flex-direction property, [Changing the flex-direction](#ch04s02.html_idm494069907888)

> flex-grow property, [The flex shorthand property](#ch04s02.html_idm494069865184)

> flex-shrink property, [The flex shorthand property](#ch04s02.html_idm494069865184)

> Flexbugs resource, [For the More Curious: Common Solutions (and Bugs) with Flexbox Layouts](#ch05s04.html)

> main and cross axes, [Creating a flex container](#ch04s02.html_idm494069939200)

> order property, [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504)

> Solved by Flexbox resource, [For the More Curious: Common Solutions (and Bugs) with Flexbox Layouts](#ch05s04.html)

flexible box model (see [flexbox](#ix01.html_pri_idm494070059536))
focus method, [UI Enhancements](#ch10s04.html)
:focus pseudo-class, [Styling Valid and Invalid Elements](#ch12s04.html)
Font Awesome, [Silver Challenge: Adding Font Awesome](#ch19s07.html)
@font-face declaration, [Adding a Font](#ch03s09.html)
fonts, adding, [Adding a Font](#ch03s09.html)
for attribute, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)
forEach method, [Iterating Through the Array of Thumbnails](#ch06s11.html), [For the More Curious: Setting this in forEach’s Callback](#ch08s12.html)
<form> tag, [Creating the Order Form](#ch09s02.html)
function scope, [Adding an Event Listener](#ch06s09.html)
functions

> about, [Handling Events with JavaScript](#ch06.html), [Writing the setDetails Function](#ch06s07.html)

> anonymous, [Adding an Event Listener](#ch06s09.html)

> anonymous vs named in callbacks, [Iterating Through the Array of Thumbnails](#ch06s11.html), [For the More Curious: Closures](#ch06s15.html)

> arguments and parameters, [Accepting arguments by declaring parameters](#ch06s07.html_idm494069199216)

> arrow, [Handling events and sending messages](#ch17s06.html_idm494065676352), [For the More Curious: Arrow Functions](#ch17s11.html)

> as arguments, [Returning Values from Functions](#ch06s08.html)

> as objects, [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)

> callbacks, [Adding an Event Listener](#ch06s09.html)

> calling, [Writing the setDetails Function](#ch06s07.html)

> declaring, [Writing the setDetails Function](#ch06s07.html)

> exporting instances to the global namespace, [Creating the Truck instance](#ch08s08.html_se-creating-the-truck-instance)

> named, [Adding an Event Listener](#ch06s09.html)

> properties of, [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)

> returning a value, [Returning Values from Functions](#ch06s08.html)

### G

get method, [get and set](#ch21s03.html)
GET requests, [RESTful Web Services](#ch13s02.html), [Using jQuery’s $.ajax method](#ch13s06.html_se-using-jquerys-.ajax-method)
getAttribute method, [Returning Values from Functions](#ch06s08.html)
global namespace, [The module pattern](#ch08.html_se-module-as-transforming-portal)
global scope, [Adding an Event Listener](#ch06s09.html)
Google Chrome

> Developer Tools (see [DevTools](#ix01.html_pri_idm494070606144))

> installing, [Installing Google Chrome](#ch01.html_idm494071104784)

Gravatars, [Using Gravatars](#ch18s04.html)

### H

<h1> tag, [Initial HTML](#ch02.html_se-creating-the-document)
Handlebars

> about, [Handlebars](#ch23.html_se-handlebars)

> binding element attributes, [Binding element attributes](#ch23s03.html_se-binding-element-attributes)

> conditionals, [Conditionals](#ch23s03.html_se-conditionals)

> creating custom helpers, [Custom Helpers](#ch23s04.html)

> helpers, [Helpers](#ch23s03.html)

> links, [Links](#ch23s03.html_se-links)

> loops, [Loops with {{#each}}](#ch23s03.html_se-loops-with-each)

hasMany method, [Model Definitions](#ch21.html_se-model-definitions)
hasOne method, [Model Definitions](#ch21.html_se-model-definitions)
<head> tag, [Initial HTML](#ch02.html_se-creating-the-document)
Homebrew, installing, [Installing Ember](#ch19s02.html_se-install)
horizontal rule (see [<hr> tag](#ix01.html_pri_idm494063558160))
<hr> tag, [Deleting a Sighting](#ch24s03.html)
href attribute, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet), [Adding images](#ch02.html_se-setting-up-styles)
HTML, [Initial HTML](#ch02.html_se-creating-the-document)
HTML attributes (see [attributes](#ix01.html_pri_idm494070726960))
HTML elements

> accessing in JavaScript, [Writing the JavaScript to hide the detail image](#ch07.html_idm494068784320)

> list, [Initial HTML](#ch02.html_se-creating-the-document)

> replaced, [Adding images](#ch02.html_se-setting-up-styles)

HTML tags

> <a>, [Adding images](#ch02.html_se-setting-up-styles)

> <body>, [Initial HTML](#ch02.html_se-creating-the-document)

> <div>, [Adding the detail image](#ch04.html_se-adding-the-detail-image), [Creating the Order Form](#ch09s02.html)

> <form>, [Creating the Order Form](#ch09s02.html)

> <h1>, [Initial HTML](#ch02.html_se-creating-the-document)

> <head>, [Initial HTML](#ch02.html_se-creating-the-document)

> <hr>, [Deleting a Sighting](#ch24s03.html)

> <img>, [Adding images](#ch02.html_se-setting-up-styles)

> <input>, [Adding text input fields](#ch09s02.html_se-adding-a-textfield), [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

> <label>, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)

> <link>, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)

> <meta>, [Initial HTML](#ch02.html_se-creating-the-document)

> <option>, [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)

> <script>, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)

> <section>, [Creating the Order Form](#ch09s02.html)

> <select>, [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)

> <span>, [Adding content](#ch02.html_se-adding-an-unordered-list)

> <style>, [Styling Valid and Invalid Elements](#ch12s04.html)

> <title>, [Initial HTML](#ch02.html_se-creating-the-document)

> <ul>, [Adding content](#ch02.html_se-adding-an-unordered-list)

> about, [Initial HTML](#ch02.html_se-creating-the-document)

> list, [Initial HTML](#ch02.html_se-creating-the-document)

> self-closing, [Adding images](#ch02.html_se-setting-up-styles)

html5please.com, [Documentation and Reference Sources](#ch01s03.html)
HTMLCollections, [For the More Curious: NodeLists and HTMLCollections](#ch06s16.html)
HTTP status codes, [XMLHttpRequest Objects](#ch13.html_se-xmlhttprequest-objects)
HTTP verbs

> about, [RESTful Web Services](#ch13s02.html)

> and URL paths, [RESTful Web Services](#ch13s02.html)

### I

id attribute, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)
ID selectors, [For the More Curious: Specificity! When Selectors Collide…](#ch03s11.html)
ideal viewport, [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)
{{if}} helper, [Binding element attributes](#ch23s03.html_se-binding-element-attributes)
{{#if}} helper, [Conditionals](#ch23s03.html_se-conditionals)
image tags (see [<img> tag](#ix01.html_pri_idm494070662960))
<img> tag, [Adding images](#ch02.html_se-setting-up-styles)
immediately invoked function expressions (IIFEs)

> about, [The module pattern](#ch08.html_se-module-as-transforming-portal)

> modifying an object with, [Modifying an object with an IIFE](#ch08.html_se-using-iife-to-modify)

implicit return, [Constructors](#ch08s05.html)
@import directive, [Configuration](#ch19s04.html)
import keyword, for named imports, [Creating the ChatForm Class](#ch18s02.html)
input event, [Listening for the input event](#ch12s03.html_se-listening-for-the-input-event)
<input> tag

> for checkboxes, [Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)

> for radio buttons, [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

> for range sliders, [Adding a range slider](#ch09s02.html_se-adding-a-slider)

> for reset buttons, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> for submit buttons, [Adding Submit and Reset buttons](#ch09s02.html_se-adding-the-submit-and-reset-buttons)

> for text input, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)

> linking to <label> tag, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element), [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

:invalid pseudo-class, [Styling Valid and Invalid Elements](#ch12s04.html)

### J

JavaScript

> classes, [Class syntax](#ch17s03.html_se-class-syntax)

> compiling ES6 to ES5, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

> compiling from other languages, [For the More Curious: Compiling to JavaScript from Other Languages](#ch17s07.html)

> default arguments, [Adding the ChatMessage Class](#ch17s05.html)

> destructuring assignment syntax, [Adding the ChatMessage Class](#ch17s05.html)

> functions, [Handling Events with JavaScript](#ch06.html)

> types (see [types](#ix01.html_pri_idm494069312160))

> variable naming conventions, [Importing jQuery](#ch10.html_se-importing-jquery)

> versions, [Handling Events with JavaScript](#ch06.html), [Using ES6 with Babel](#ch17.html)

jQuery

> $ variable, [Importing jQuery](#ch10.html_se-importing-jquery)

> $.ajax method, [Using jQuery’s $.ajax method](#ch13s06.html_se-using-jquerys-.ajax-method)

> $.get method, [Retrieving Data from the Server](#ch13s05.html)

> $.post method, [Using jQuery’s $.post method](#ch13s04.html_se-using-jquerys-.post-method)

> about, [Introduction to jQuery](#ch10.html_se-orphan-jquery)

> adding, [Introduction to jQuery](#ch10.html_se-orphan-jquery)

> append method, [Creating DOM elements with jQuery](#ch11s03.html_se-creating-dom-elements-with-jquery)

> Deferred objects, [Promises and Deferreds](#ch14.html_se-promise-foundation)

> for managing Ajax requests, [XMLHttpRequest Objects](#ch13.html_se-xmlhttprequest-objects)

> length property, [Configuring instances of FormHandler with a selector](#ch10.html_se-configuring-the-instance-with-a-selector)

> on method, [Adding the submit Handler](#ch10s02.html)

> serializeArray method, [Extracting the data](#ch10s02.html_se-extracting-the-data)

jQuery-wrapped selections, [Configuring instances of FormHandler with a selector](#ch10.html_se-configuring-the-instance-with-a-selector), [Extracting the data](#ch10s02.html_se-extracting-the-data)
JSON, [Adding the ChatMessage Class](#ch17s05.html)
JSONAPI, [Data – Adapters, Serializers, and Transforms](#ch22.html)
justify-content property, [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504), [Centering the detail image](#ch04s02.html_idm494069756352)

### K

keyCode property, [Listening for the keypress event](#ch07.html_idm494068768944)
keydown event, [Listening for the keypress event](#ch07.html_idm494068768944)
keypress event, [Listening for the keypress event](#ch07.html_idm494068768944)
keyup event, [Listening for the keypress event](#ch07.html_idm494068768944)

### L

<label> tag

> about, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element)

> linking to <input> tag, [Linking a label and a form element](#ch09s02.html_se-linking-label-and-form-element), [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)

layout viewport, [Adaptive Layouts with Media Queries](#ch05.html), [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)
linear timing function, [Using a timing function](#ch07s02.html_idm494068618640), [Custom Timing Functions](#ch07s03.html)
<link> tag, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)
{{#link-to}} helper, [Links](#ch23s03.html_se-links)
linting, [Atom plug-ins](#ch01s02.html_idm494071072528)
list-style property, [Adjusting the Space Between Items](#ch03s08.html)
local scope, [Adding an Event Listener](#ch06s09.html)
localStorage vs sessionStorage, [User Session Storage](#ch18s06.html)
logical or (default) operator (||), [Adding Modules to a Namespace](#ch08s04.html)
loose equality operator (==), [Listening for the keypress event](#ch07.html_idm494068768944)

### M

Mac Terminal, opening, [Crash Course in the Command Line](#ch01s04.html)
margin property, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
margins, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
MDN (see [Mozilla Developer Network](#ix01.html_pri_idm494071021072))
@media declaration, [Adding a Media Query](#ch05s02.html)
media queries

> about, [Adding a Media Query](#ch05s02.html)

> location in stylesheet, [Creating styles to hide the detail image](#ch07.html_idm494068824128)

media types, [Adding a Media Query](#ch05s02.html), [For the More Curious: MIME Types](#ch15s08.html)
message events, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)
<meta> tag, [Initial HTML](#ch02.html_se-creating-the-document)
methods

> (see also [functions](#ix01.html_pri_idm494069472432))

> (see also individual method names)

MIME types, [For the More Curious: MIME Types](#ch15s08.html)
mobile-first development, [Expanding the Interface](#ch04.html_se-expanding-the-interface)
model method, [Assigning Models](#ch20s04.html)
Model-View-Controller (MVC), [Introduction to MVC and Ember](#ch19.html)
models in MVC, [Introduction to MVC and Ember](#ch19.html)
modules

> about, [Modules](#ch08.html_se-module-pattern)

> exporting, [Using Browserify for Packaging Modules](#ch17s04.html)

> importing, [Using Browserify for Packaging Modules](#ch17s04.html)

> pattern, [The module pattern](#ch08.html_se-module-as-transforming-portal)

moment, [Formatting and Updating Message Timestamps](#ch18s07.html)
Mozilla Developer Network, [Documentation and Reference Sources](#ch01s03.html)
MVC (see [Model-View-Controller (MVC)](#ix01.html_pri_idm494074270560))

### N

name attribute, [Adding text input fields](#ch09s02.html_se-adding-a-textfield)
named exports, [Creating the ChatForm Class](#ch18s02.html)
named functions

> about, [Adding an Event Listener](#ch06s09.html)

> vs anonymous functions in callbacks, [Iterating Through the Array of Thumbnails](#ch06s11.html), [For the More Curious: Closures](#ch06s15.html)

named imports, [Creating the ChatForm Class](#ch18s02.html)
namespaces

> about, [The module pattern](#ch08.html_se-module-as-transforming-portal)

> adding modules to, [Adding Modules to a Namespace](#ch08s04.html)

> using objects as, [Adding Modules to a Namespace](#ch08s04.html)

new keyword, [Constructors](#ch08s05.html), [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)
Node.js

> about, [Introduction to Node.js](#ch15.html)

> custom modules, [Creating a custom module](#ch15s04.html_se-create-a-custom-module)

> error handling, [Error Handling](#ch15s05.html)

> fs module, [Reading a file with the fs module](#ch15s04.html_se-reading-a-file-with-the-fs-module)

> fs.readFile method, [Reading a file with the fs module](#ch15s04.html_se-reading-a-file-with-the-fs-module)

> http module, [Hello, World](#ch15s02.html)

> http.createServer function, [Hello, World](#ch15s02.html)

> installing, [Installing Node.js and browser-sync](#ch01s05.html)

> module.exports, [Creating a custom module](#ch15s04.html_se-create-a-custom-module)

> nodemon module, [Adding an npm Script](#ch15s03.html)

> npm install --save-dev option, [Adding an npm Script](#ch15s03.html)

> npm Module Registry, [For the More Curious: npm Module Registry](#ch15s06.html)

> path module, [Using the path module](#ch15s04.html_se-using-the-path-module)

> require function, [Hello, World](#ch15s02.html)

> server.listen function, [Hello, World](#ch15s02.html)

> starting a Node server, [Hello, World](#ch15s02.html)

> ws module, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

NodeLists, [Accessing All the Thumbnails](#ch06s10.html), [For the More Curious: NodeLists and HTMLCollections](#ch06s16.html)
normalize.css, installing, [Creating a Styling Baseline](#ch03.html_se-setting-up-layout)
null type, [For the More Curious: JavaScript Types](#ch06s17.html)
numbers, [For the More Curious: JavaScript Types](#ch06s17.html)

### O

objects, [Accessing DOM Elements](#ch06s06.html)
onchange event, [New Sightings](#ch24.html_se-new-sightings)
<option> tag, [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)
order flexbox property, [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504)
{{outlet}} helper, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)
overflow property, [Adding a Media Query](#ch05s02.html)
overflow-x property, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails)

### P

package.json

> about, [Node and npm](#ch15.html_se-node-and-npm)

> creating, [npm init](#ch15.html_se-npm-init)

padding, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
padding property, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
parameters (in JavaScript functions), [Accepting arguments by declaring parameters](#ch06s07.html_idm494069199216)
pattern attribute, [Validating with Regular Expressions](#ch12s02.html)
peekAll method, [For the More Curious: Retrieving Data](#ch21s05.html)
peekRecord method, [For the More Curious: Retrieving Data](#ch21s05.html)
pixels (px), [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
placeholder attribute, [Showing example input with placeholder text](#ch09s02.html_se-adding-placeholder-text)
position: absolute property, [Absolute and Relative Positioning](#ch04s03.html)
position: relative property, [Absolute and Relative Positioning](#ch04s03.html)
POST requests, [RESTful Web Services](#ch13s02.html), [Using jQuery’s $.ajax method](#ch13s06.html_se-using-jquerys-.ajax-method)
Postman, [For the More Curious: Postman](#ch13s09.html)
preventDefault, [Adding the submit Handler](#ch10s02.html)
primtive types, [Working in the Console](#ch06s05.html), [For the More Curious: JavaScript Types](#ch06s17.html)
Promises

> about, [Promises and Deferreds](#ch14.html_se-promise-foundation)

> creating, [Creating and returning Promises](#ch14s06.html_se-creating-returning-promises)

prompt function, [Prompting for Username](#ch18s05.html)
properties

> about, [Anatomy of a Style](#ch03s03.html)

> align-items, [Centering the detail image](#ch04s02.html_idm494069756352)

> border, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

> cubic-bezier, [Custom Timing Functions](#ch07s03.html)

> display: block, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools), [Making Images Fit the Window](#ch03s06.html), [Flexbox](#ch04s02.html)

> display: flex, [Creating a flex container](#ch04s02.html_idm494069939200)

> display: inline, [Making Images Fit the Window](#ch03s06.html)

> display: inline-block, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails), [Flexbox](#ch04s02.html)

> display: none, [Creating styles to hide the detail image](#ch07.html_idm494068824128)

> elements, [UI Enhancements](#ch10s04.html)

> flex, [The flex shorthand property](#ch04s02.html_idm494069865184)

> flex-basis, [The flex shorthand property](#ch04s02.html_idm494069865184)

> flex-direction, [Changing the flex-direction](#ch04s02.html_idm494069907888)

> flex-grow, [The flex shorthand property](#ch04s02.html_idm494069865184)

> flex-shrink, [The flex shorthand property](#ch04s02.html_idm494069865184)

> justify-content, [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504), [Centering the detail image](#ch04s02.html_idm494069756352)

> list-style, [Adjusting the Space Between Items](#ch03s08.html)

> margin, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

> order, [Ordering, justifying, and aligning flex items](#ch04s02.html_idm494069823504)

> overflow, [Adding a Media Query](#ch05s02.html)

> overflow-x: auto, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails)

> padding, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

> position: absolute, [Absolute and Relative Positioning](#ch04s03.html)

> position: relative, [Absolute and Relative Positioning](#ch04s03.html)

> prototype, [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)

> shorthand, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

> text-align, [Centering the detail image](#ch04s02.html_idm494069756352)

> text-decoration, [Style Inheritance](#ch03s05.html)

> text-shadow, [Absolute and Relative Positioning](#ch04s03.html)

> textContent, [Writing the setDetails Function](#ch06s07.html)

> transform, [Working with the transform property](#ch07s02.html_se-working-with-the-transform-property)

> white-space, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails)

> width, [Making Images Fit the Window](#ch03s06.html)

prototype property, [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)
pseudo-classes

> :focus, [Styling Valid and Invalid Elements](#ch12s04.html)

> :hover, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)

> :invalid, [Styling Valid and Invalid Elements](#ch12s04.html)

> :required, [Styling Valid and Invalid Elements](#ch12s04.html)

> about, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)

> testing in DevTools, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)

push method, [Creating the Chat Server Functionality](#ch16s03.html)
PUT requests, [RESTful Web Services](#ch13s02.html)

### Q

query method, [For the More Curious: Retrieving Data](#ch21s05.html)
queryRecord method, [For the More Curious: Retrieving Data](#ch21s05.html)
querySelector method, [Accessing DOM Elements](#ch06s06.html)
querySelectorAll method, [Accessing All the Thumbnails](#ch06s10.html)

### R

radio button form fields (see [<input> tag](#ix01.html_pri_idm494067876912))
range slider form fields (see [<input> tag](#ix01.html_pri_idm494067876912))
recency (in CSS), [For the More Curious: Specificity! When Selectors Collide…](#ch03s11.html)
regular expressions, [Validating with Regular Expressions](#ch12s02.html), [Constraint Validation API](#ch12s03.html)
rel attribute, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)
relationship selectors, [Relationship selectors](#ch03s08.html_idm494070191376)
remove method, [Showing the detail image again](#ch07.html_idm494068716320)
replaced elements, [Adding images](#ch02.html_se-setting-up-styles)
required attribute, [The required Attribute](#ch12.html_se-the-required-attribute)
:required pseudo-class, [Styling Valid and Invalid Elements](#ch12s04.html)
reset buttons (see [<input> tag](#ix01.html_pri_idm494067876912))
reset method, [UI Enhancements](#ch10s04.html)
resource files, [Adding images](#ch02.html_se-setting-up-styles)
RESTful web services, [RESTful Web Services](#ch13s02.html)
return statement, [Returning Values from Functions](#ch06s08.html)
rgb and rgba, [Color](#ch03s07.html)
route method, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)
Router.map method, [ember generate](#ch20.html_se-ember-generate)

### S

save method, [For the More Curious: Saving and Destroying Data](#ch21s06.html)
<script> tag, [Preparing the Anchor Tags for Duty](#ch06.html_se-changes-to-index.html)
scrolling, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails)
<section> tag, [Creating the Order Form](#ch09s02.html)
<select> tag, [Adding a dropdown menu](#ch09s02.html_se-adding-a-dropdown)
selectors (in CSS)

> about, [Anatomy of a Style](#ch03s03.html)

> attribute, [Style Inheritance](#ch03s05.html)

> child, [Relationship selectors](#ch03s08.html_idm494070191376)

> class, [Your First Styling Rule](#ch03s04.html)

> descendent, [Relationship selectors](#ch03s08.html_idm494070191376)

> element, [Style Inheritance](#ch03s05.html)

> grouping, [Creating a flex container](#ch04s02.html_idm494069939200)

> ID, [For the More Curious: Specificity! When Selectors Collide…](#ch03s11.html)

> modifying with pseudo-classes, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)

> relationship, [Relationship selectors](#ch03s08.html_idm494070191376)

> sibling, [Relationship selectors](#ch03s08.html_idm494070191376)

> specificity, [Anatomy of a Style](#ch03s03.html), [For the More Curious: Specificity! When Selectors Collide…](#ch03s11.html)

> specificity vs recency, [Creating styles to hide the detail image](#ch07.html_idm494068824128)

self-closing tags, [Adding images](#ch02.html_se-setting-up-styles)
serialize method, [Transforms](#ch22s04.html)
sessionStorage vs localStorage, [User Session Storage](#ch18s06.html)
set method, [get and set](#ch21s03.html)
setAttribute method, [Accessing DOM Elements](#ch06s06.html)
setCustomValidity method, [Triggering the validity check](#ch12s03.html_se-triggering-the-validity-check)
setTimeout method, [Triggering transitions with JavaScript](#ch07s02.html_se-triggering-with-javascript)
setupController method, [Assigning Models](#ch20s04.html), [beforeModel](#ch20s05.html), [For the More Curious: setupController and afterModel](#ch20s06.html)
shorthand properties, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)
sibling selectors, [Relationship selectors](#ch03s08.html_idm494070191376)
<span> tag, [Adding content](#ch02.html_se-adding-an-unordered-list)
specificity calculator, [For the More Curious: Specificity! When Selectors Collide…](#ch03s11.html)
src attribute, [Adding images](#ch02.html_se-setting-up-styles)
stackoverflow.com, [Documentation and Reference Sources](#ch01s03.html)
strict equality operator (===), [Listening for the keypress event](#ch07.html_idm494068768944)
strict mode, [For the More Curious: Strict Mode](#ch06s14.html)
strings, [Declaring String Variables](#ch06s04.html), [For the More Curious: JavaScript Types](#ch06s17.html)
style inheritance

> about, [Style Inheritance](#ch03s05.html)

> overriding, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

<style> tag, [Styling Valid and Invalid Elements](#ch12s04.html)
stylesheets

> about, [Setting Up Ottergram](#ch02.html_se-setting-up-your-project-folders)

> linking, [Linking a stylesheet](#ch02.html_se-linking-a-stylesheet)

> user agent stylesheet, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

styling rules (in CSS), [Anatomy of a Style](#ch03s03.html)
subclasses, [User Session Storage](#ch18s06.html)
submit buttons (see [<input> tag](#ix01.html_pri_idm494067876912))
submit event, [Adding the submit Handler](#ch10s02.html)
super method, [User Session Storage](#ch18s06.html)

### T

template strings, [Using Gravatars](#ch18s04.html)
terminal commands

> about, [Crash Course in the Command Line](#ch01s04.html)

> changing directories, [Changing directories](#ch01s04.html_se-changing-directories)

> creating a directory, [Creating a directory](#ch01s04.html_se-creating-a-directory)

> installing tools with npm, [Installing Node.js and browser-sync](#ch01s05.html)

> listing files, [Listing files in a directory](#ch01s04.html_idm494070925952)

> quitting a program, [Quitting a program](#ch01s04.html_se-quitting-a-program)

> showing the current directory, [Finding out what directory you are in](#ch01s04.html_se-finding-out-what-directory-you-are-in)

> using administrator privileges, [Getting administrator privileges](#ch01s04.html_se-if-you-need-administrator-privileges)

text input form fields (see [<input> tag](#ix01.html_pri_idm494067876912))
text-align property, [Centering the detail image](#ch04s02.html_idm494069756352)
text-decoration property, [Style Inheritance](#ch03s05.html)
text-shadow, [Absolute and Relative Positioning](#ch04s03.html)
textContent property, [Writing the setDetails Function](#ch06s07.html)
then method, [Registering Callbacks with then](#ch14s03.html), [Using Deferreds with Callback-Only APIs](#ch14s05.html)
this keyword

> about, [Constructors](#ch08s05.html), [A constructor’s prototype](#ch08s05.html_se-a-constructors-prototype)

> in callbacks, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)

> setting value with bind, [Setting the value of this with bind](#ch08s07.html_se-changing-the-value-of-this-with-.bind)

> setting value with call, [Manipulating this with call](#ch11s04.html_se-use-.call-to-manipulate-the-value-of-this)

timing functions

> about, [Using a timing function](#ch07s02.html_idm494068618640), [Custom Timing Functions](#ch07s03.html)

> custom, [Custom Timing Functions](#ch07s03.html)

> ease-(in/out/in-out), [Custom Timing Functions](#ch07s03.html)

> linear, [Using a timing function](#ch07s02.html_idm494068618640), [Custom Timing Functions](#ch07s03.html)

<title> tag, [Initial HTML](#ch02.html_se-creating-the-document)
transform property, [Working with the transform property](#ch07s02.html_se-working-with-the-transform-property)
transition declaration, [Adding a CSS transition](#ch07s02.html_se-adding-a-css-transition)
transitionToRoute method, [New Sightings](#ch24.html_se-new-sightings)
type attribute, [Offering choices with radio buttons](#ch09s02.html_se-adding-radio-buttons)
type coercion, [Listening for the keypress event](#ch07.html_idm494068768944), [For the More Curious: Rules for Type Coercion](#ch07s04.html)
types

> Boolean, [For the More Curious: JavaScript Types](#ch06s17.html)

> compound (or complex), [For the More Curious: JavaScript Types](#ch06s17.html)

> null, [For the More Curious: JavaScript Types](#ch06s17.html)

> number, [For the More Curious: JavaScript Types](#ch06s17.html)

> primitive, [Working in the Console](#ch06s05.html), [For the More Curious: JavaScript Types](#ch06s17.html)

> string, [For the More Curious: JavaScript Types](#ch06s17.html)

> undefined, [For the More Curious: JavaScript Types](#ch06s17.html)

### U

<ul> tag, [Adding content](#ch02.html_se-adding-an-unordered-list)
Uncaught TypeError, [Locating bugs with the DevTools](#ch08s07.html_se-debugging-the-foreach-callback)
undefined type, [For the More Curious: JavaScript Types](#ch06s17.html)
unordered list (see [<ul> tag](#ix01.html_pri_idm494070710688))
URL paths and HTTP verbs, [RESTful Web Services](#ch13s02.html)
URL routing

> about, [Routing, Routes, and Models](#ch20.html)

> and Ember routes, [ember generate](#ch20.html_se-ember-generate), [Nesting Routes](#ch20s02.html)

user agent stylesheet, [The box model](#ch03s04.html_se-experimenting-with-the-developer-tools)

### V

validation

> and event handling, [The required Attribute](#ch12.html_se-the-required-attribute)

> with pattern, [Validating with Regular Expressions](#ch12s02.html)

> with required, [The required Attribute](#ch12.html_se-the-required-attribute)

> with validation functions, [Constraint Validation API](#ch12s03.html)

variables

> about, [Declaring String Variables](#ch06s04.html)

> declaring, [Declaring String Variables](#ch06s04.html)

> hoisting, [Connection handling](#ch17s06.html_se-building-handlers), [For the More Curious: Hoisting](#ch17s10.html)

> let scoping, [Connection handling](#ch17s06.html_se-building-handlers), [For the More Curious: Hoisting](#ch17s10.html)

viewports

> about, [Adaptive Layouts with Media Queries](#ch05.html), [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

> actual viewport (see [layout viewport](#ix01.html_pri_idm494069633616))

> ideal viewport, [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

> layout viewport, [Adaptive Layouts with Media Queries](#ch05.html), [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

> resetting, [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

> visual viewport, [Adaptive Layouts with Media Queries](#ch05.html), [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

views in MVC, [Introduction to MVC and Ember](#ch19.html)
Visual Studio Code, [For the More Curious: Alternatives to Atom](#ch01s06.html)
visual viewport, [Adaptive Layouts with Media Queries](#ch05.html), [Resetting the Viewport](#ch05.html_se-resetting-the-viewport)

### W

Watchify

> about, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

> installing, [Tools for Compiling JavaScript](#ch17.html_se-compiling-javascript)

Watchman, installing, [Installing Ember](#ch19s02.html_se-install)
Web Storage APIs, [User Session Storage](#ch18s06.html)
WebAssembly, [For the More Curious: Compiling to JavaScript from Other Languages](#ch17s07.html)
WebSockets

> about, [Real-Time Communication with WebSockets](#ch16.html)

> handling connections, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

> installing, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

> npm ws module, [Setting Up WebSockets](#ch16.html_se-setting-up-websockets)

> onopen property, [Handling events and sending messages](#ch17s06.html_idm494065676352)

> socket.io, [For the More Curious: socket.io WebSockets Library](#ch16s05.html)

white-space property, [Horizontal layout for thumbnails](#ch04.html_se-horizontal-layout-for-thumbnails)
width property, [Making Images Fit the Window](#ch03s06.html)
Windows Command Prompt, opening, [Crash Course in the Command Line](#ch01s04.html)
wscat module, [Testing Your WebSockets Server](#ch16s02.html)

### X

{{x-select}} component, [New Sightings](#ch24.html_se-new-sightings)

### Y

{{yield}} helper, [Iterator Items as Components](#ch25.html_se-iterator-items-as-components)