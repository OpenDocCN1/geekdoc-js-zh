![](images/cover.jpg)

![image](images/cover.jpg)

# Decoding
JavaScript

![](images/line.jpg)

# *A Simple Guide for the not-so-simple JavaScript
Concepts, Libraries, Tools, and Frameworks*

![](images/line.jpg)

# Rushabh Mulraj Shah

![](images/logo.jpg)

[www.bpbonline.com](http://www.bpbonline.com)

**FIRST EDITION 2021**

**Copyright © BPB Publications, India**

**ISBN: 978-93-90684-816**

All Rights Reserved. No part of this publication may be reproduced, distributed or transmitted in any form or by any means or stored in a database or retrieval system, without the prior written permission of the publisher with the exception to the program listings which may be entered, stored and executed in a computer system, but they can not be reproduced by the means of publication, photocopy, recording, or by any electronic and mechanical means.

**LIMITS OF LIABILITY AND DISCLAIMER OF WARRANTY**

The information contained in this book is true to correct and the best of author’s and publisher’s knowledge. The author has made every effort to ensure the accuracy of these publications, but publisher cannot be held responsible for any loss or damage arising from any information in this book.

All trademarks referred to in the book are acknowledged as properties of their respective owners but BPB Publications cannot guarantee the accuracy of this information.

**Distributors:**

**BPB PUBLICATIONS**

20, Ansari Road, Darya Ganj

New Delhi-110002

Ph: 23254990/23254991

**MICRO MEDIA**

Shop No. 5, Mahendra Chambers,

150 DN Rd. Next to Capital Cinema,

V.T. (C.S.T.) Station, MUMBAI-400 001

Ph: 22078296/22078297

**DECCAN AGENCIES**

4-3-329, Bank Street,

Hyderabad-500195

Ph: 24756967/24756400

**BPB BOOK CENTRE**

376 Old Lajpat Rai Market,

Delhi-110006

Ph: 23861747

![](images/logo1.jpg)

Published by Manish Jain for BPB Publications, 20 Ansari Road, Darya Ganj, New Delhi-110002 and Printed by him at Repro India Ltd, Mumbai

[www.bpbonline.com](http://www.bpbonline.com/)

# Dedicated to

*Mulraj D. Shah & Harsha M. Shah
My parents, for not giving in to social norms and pushing me to fly.*

*Unnati Vora
From being friends to being my wife, you have been
the perfect pillar of support.*

*John Thomas
When I wanted a friend, I ended up getting
an elder brother and a mentor.*

*Dr. Soudip Roy Chowdhury
The gaffer, who always believed in me and never gave up on me.*

# About the Author

**Rushabh Mulraj Shah** is a published technical author, technical mentor, content-creator, and a Senior UI Developer. He is also one of the founding members of an exciting AI startup that goes by the name of eugenie.ai. In his 5+ years of experience, while working for companies like Capgemini International, Fractal, and eugenie.ai, he has interacted with several prominent clients, including the Indian Navy, Mondelez India, Colgate Palmolive, EY, RB, and many others.

Apart from his usual stint, Rushabh has also been an influential blogger and a content writer. His articles on SportsKeeda, Little Black Book (LBB), NearFox, Zomato, and other such platforms have garnered more than 600K views. His private blog (**[http://thevegfoodgasms.blogspot.com/](http://thevegfoodgasms.blogspot.com/)**) has been nominated for four consecutive years on the national level.

# About the Reviewer

**Vinay Joshi** has 9 years of experience with Applications development in web, mobile and platforms using tools like .Net, Java, Node, Azure, GCP, Openshfit, with programming languages like C#, Javascript, Java, Typescript, Python, etc. He pursued Masters in Computer Applications from Dehradun Institute of Technology Dehradun, Uttarakhand. He has worked with companies like Publicis.Sapient, Next Gen Invent Corporation. He is currently working as Full Stack Developer in Role of Technology lead in Optum Global Solutions which is part of United Health Group in Gurgaon location.

# Acknowledgement

When I started writing this book, an unthinkable event happened. As the first chapter went into drafts, the entire world slowly ceased to a standstill. The novel Coronavirus (COVID-19) forced the world to lock itself down. The lonely streets were accompanied by silent offices and quiet parks. In these tough times, I wouldn't have been able to complete this book if it was not for the constant support from my family. I would like to thank my parents - Mulraj D. Shah, Harsha M. Shah, and my wife, Unnati, for putting up with my late-night writing shenanigans.

The next acknowledgment goes to the entire team at BPB Publications for giving me this wonderful opportunity to write this book and share my experiences with everyone.

My final thanks goes to Mr. John Thomas, a genuine friend with a golden heart, for teaching me the best practices, and Mrs. Shweta Doshi and her team of GreyAtom to bring forth my love for teaching.

# Preface

It's fair to say that the year 2020 will be imprinted boldly in the books of history. 2020 is the year when our fast-paced world took a pause, locked itself inside, and embarked on a journey to save the world, albeit strikingly different from the way the silver screen and its larger-than-life heroes portray it. It has also been the year when the Internet came to the fore. From rescue operations, data analysis, information service to locked-in entertainment, the Web and its insane variety of applications helped humanity wherever possible. It can only make you wonder the importance of the Web and its helpful associates.

This book is about web development. It is about unleashing the magic of JavaScript, a pretty straight-forward scripting language, that can help you create incredible next-generation applications on the Internet.

In simple words, web development is the process of creating and maintaining websites and web applications. The entire idea of web development revolves around the following three simple questions:

1.  What can a user see on the screen?
2.  How does it look?
3.  What happens when a user interacts with what he/she sees on the screen?

While the answer to the first two questions creates a web page that the users can only see but not interact with, it is the answer to the third question that brings alive a web page. The three technologies, which help solve the three stated problems are HTML, CSS, and JavaScript. In this book, we will not only explore, but master advanced JavaScript. This will help you set up a base to build next-generation web applications.

**Over the 16 chapters in this book, you will learn the following:**

**[Chapter 1](#c01.xhtml)** will introduce you to the world of JavaScript. In this chapter, we will revise the fundamental concepts of JavaScript. We will go through topics like the syntax of JavaScript, data types, operators, conditionals, looping, and hoisting in JavaScript. We will also see certain flavors of advanced JavaScript concepts.

**[Chapter 2](#c02.xhtml)** will help you explore the handy Chrome Developer Tools of Google Chrome. Typically, every code you write for your web application should be browser-agnostic, i.e., it should be generalized and not specific for any browser. However, based on popularity and for the sake of simplicity, we will be working with the Google Chrome browser.

**[Chapter 3](#c03.xhtml)** will teach you everything about functions. We will look at topics like when and why to use functions, types of functions, scopes, and closures.

**[Chapter 4](#c04.xhtml)** will help you revise the concept of arrays. At the same time, we will also glance at several important in-built methods of arrays that you will be using daily.

**[Chapter 5](#c05.xhtml)** will help you learn you everything about objects. We will look at topics like objects properties and methods, constructors, prototypes, and when to use objects.

**[Chapter 6](#c06.xhtml)** will introduce you to ECMAScript 2015, popularly known as ES6\. ES6 rejuvenated JavaScript and cemented its position as the top standard language for developing web applications. In this chapter, we will explore and learn multiple concepts introduced by ES6, including, but not limited to let and const, arrow functions, new array methods, modules, destructuring, and so on.

**[Chapter 7](#c07.xhtml)** explores a concept introduced by ES6 – classes. Here, we will learn the need for classes, how to write classes, and how to handle inheritance.

**[Chapter 8](#c08.xhtml)** will kickstart the section 'Reaching out to the Servers'. In this chapter, we will first understand the concept of Asynchronous JavaScript. It will teach us how to resume execution of JavaScript while servers respond to requests sent from the browsers. After that, we will learn about callbacks and promises – the two methods for implementing asynchronous JavaScript.

**[Chapter 9](#c09.xhtml)** will take us on the journey of connecting with a live server using the principles of AJAX. We will also read about JSON, the universally accepted format for transmitting data across the Web.

**[Chapter 10](#c10.xhtml)** will give you the first taste of creating a live application using the concepts we have learned so far. We will create a JavaScript web application that can be hosted on any server for the world to see. We will follow traditional SDLC methods to create this application.

**[Chapter 11](#c11.xhtml)** will explain the concept of storing data on the browsers.

**[Chapter 12](#c12.xhtml)** will teach you how to debug applications that have crashed or applications that are performing erroneously. We will also learn how to handle errors in this chapter.

**[Chapter 13](#c13.xhtml)** will help you realise the importance of testing JavaScript code often. We will look at several testing frameworks and write a sample code using one of them.

**[Chapter 14](#c14.xhtml)** will teach you an important concept called Regular Expressions. It is primarily used for searching strings and patterns. However, it has a far more significance, not only in JavaScript, but in several programming languages.

**[Chapter 15](#c15.xhtml)** explores life after ES6\. ES6 revolutionised JavaScript to be the most popular language for web development. However, several versions post ES6, have taken the language to another level. We will look at all the versions from ES6 to ES11.

**[Chapter 16](#c16.xhtml)** is the final chapter of this book. Here, we will simply look at some of the best practices followed by leading product companies like Google, Facebook, Twitter, and so on. We will also look at several tips and tricks to make life easier for developers.

# How to use this book?

**This book comprises seven sections.**

**The first three sections -** Foundations, Functions and Objects, and ES6, will update your knowledge base with fundamental concepts of basic and advanced JavaScript. It's a given that every resilient building needs a strong foundation. The first three sections will help you cement that foundation for advanced topics.

**The next two sections –** Reaching out to the Servers and Web Storage, will take you on the journey you will tread often. Here, you will learn how to interact with the servers to create next-gen web applications. In the midst of learning these cool concepts, we will together create a live web application. It will give you a taste of what real-life web development feels like.

**Section six** – Debugging and Testing, will exclusively explain you the importance of testing your code. It will also teach you how to handle errors in your code.

The final section includes bonus topics like Regular Expressions, Versions of ECMAScript (the scripting standard adopted by JavaScript), and Tips & Tricks. This section will improve your coding skills to adapt to the ever-changing world.

As we mentioned earlier, during the course of this book, we will be creating a live project with an actual server. It will help you incorporate all your learnings in one real-life application. The end result can be used on your personal profile, and resume. We will also help you publish your code on a public platform for the world to see. At the end of every chapter, there will be questions to test your knowledge of the chapter. Text written in monospaced font represent code. It is highly recommended for you to practice this code on your local machines.

# Downloading the code
bundle and coloured images:

Please follow the link to download the
***Code Bundle*** and the ***Coloured Images*** of the book:

# [https://rebrand.ly/da750a](https://rebrand.ly/da750a)

# Errata

We take immense pride in our work at BPB Publications and follow best practices to ensure the accuracy of our content to provide with an indulging reading experience to our subscribers. Our readers are our mirrors, and we use their inputs to reflect and improve upon human errors, if any, that may have occurred during the publishing processes involved. To let us maintain the quality and help us reach out to any readers who might be having difficulties due to any unforeseen errors, please write to us at :

**[errata@bpbonline.com](mailto:errata@bpbonline.com)**

Your support, suggestions and feedbacks are highly appreciated by the BPB Publications’ Family.

Did you know that BPB offers eBook versions of every book published, with PDF and ePub files available? You can upgrade to the eBook version at **[www.bpbonline.com](http://www.bpbonline.com)** and as a print book customer, you are entitled to a discount on the eBook copy. Get in touch with us at **[business@bpbonline.com](mailto:business@bpbonline.com)** for more details.

At **[www.bpbonline.com](http://www.bpbonline.com)**, you can also read a collection of free technical articles, sign up for a range of free newsletters, and receive exclusive discounts and offers on BPB books and eBooks.

# BPB is searching for authors like you

If you're interested in becoming an author for BPB, please visit [**www.bpbonline.com**](http://www.bpbonline.com/) and apply today. We have worked with thousands of developers and tech professionals, just like you, to help them share their insight with the global tech community. You can make a general application, apply for a specific hot topic that we are recruiting an author for, or submit your own idea.

The code bundle for the book is also hosted on GitHub at **[https://github.com/bpbpublications/Decoding-JavaScript](https://github.com/bpbpublications/Decoding-JavaScript)**. In case there's an update to the code, it will be updated on the existing GitHub repository.

We also have other code bundles from our rich catalog of books and videos available at **[https://github.com/bpbpublications](https://github.com/bpbpublications)**. Check them out!

# PIRACY

If you come across any illegal copies of our works in any form on the internet, we would be grateful if you would provide us with the location address or website name. Please contact us at [**business@bpbonline.com**](mailto:business@bpbonline.com) with a link to the material.

# If you are interested in becoming an author

If there is a topic that you have expertise in, and you are interested in either writing or contributing to a book, please visit [**www.bpbonline.com**.](http://www.bpbonline.com/)

# REVIEWS

Please leave a review. Once you have read and used this book, why not leave a review on the site that you purchased it from? Potential readers can then see and use your unbiased opinion to make purchase decisions, we at BPB can understand what you think about our products, and our authors can see your feedback on their book. Thank you!

For more information about BPB, please visit [**www.bpbonline.com**.](http://www.bpbonline.com/)

# [CHAPTER 1](#toc.xhtml_c01)

# [Introduction to JavaScript](#toc.xhtml_c01)

**You can't build a great building on a weak foundation. You must have a solid foundation if you are going to have a super-strong structure.**

*— Gordon B. Hinkley*

On a slightly less serious note, to create next-generation kick-ass web applications, we need to write excellent JavaScript code. And to write a great JavaScript code, we need to have a substantial idea of the basic JavaScript concepts. In short, good command of the basic concepts of JavaScript will help you become the next best web developer in the industry. With that in view, let's kickstart our journey by refreshing our knowledge of the basic concepts of JavaScript.

One quick note here though, is that since this book caters towards advanced JavaScript concepts, we will not go through an extensive and detailed study of the basic concepts.

# [Structure](#toc.xhtml_s1a)

In this chapter, we will cover the following topics:

*   Getting started with JavaScript
*   Datatypes and operators in JavaScript
*   Conditions and looping in JavaScript
*   The journey of the web page
*   JavaScript and the DOM

# [Objective](#toc.xhtml_s2a)

After studying this chapter, you should be able to learn the basics of JavaScript. You will be able to write a basic code in JavaScript and understand the process of web development.

# [Getting started with JavaScript](#toc.xhtml_s3a)

Every great story starts on a beautiful, if not, an enthralling beginning. Similarly, to understand a concept or a topic better, more often than not, it's essential to realize why it became necessary to birth the idea. What was it like before the concept came into existence?

In this section, we will start by exploring the conditions that turned JavaScript as the de facto coding language of web development. By the end of this section, we will have learned what JavaScript is, how does it contribute to the process of web development, and, finally, how to set up JavaScript in our HTML files.

# [The Inception of JavaScript](#toc.xhtml_s4a)

In the early years of the **World Wide Web** (**WWW**), the most popular web browser was a particular Netscape Navigator by the computer services company, Netscape. The web pages, in those times, were capable of only showing static content. Once a web page was loaded, there was no capability for any dynamic behavior, like clicking or hovering.

To remove this limitation, in 1995, Netscape proposed and introduced a scripting language that can work on client machines (read: browsers) called *JavaScript*. Sources claim that the company decided to ride on the then-success wave of the Java language, and used the name JavaScript as a clever marketing ploy, even though there is no connection between the two programming languages.

Although JavaScript was an instant success, the introduction of a few competing browsers, and their scripting languages made it difficult for web developers to write code that can work on all the browsers. All this chaos finally led to the standardization of client-side (browser) scripting language. A company by the name **European Computer Manufacturers Association** (**ECMA**) International achieved this standardization, which was to be followed by all the browsers. Hence, JavaScript is often confused with ECMAScript. However, they are two different concepts. ECMAScript is the standard from which JavaScript is derived. Imagine JavaScript as a subset of ECMAScript.

There have been several versions of ECMAScript. However, the most popular and accepted standard by all major browsers is version 3, which was released in 1999\. Since then, the most significant update has been version 6, coined as **ES6**, in *2015*. In this book, we will be working majorly on ES6\. As time passes, newer versions will also be released. At the end of this book, we will look at versions till ES11, which are confirmed but not widely implemented.

# [What exactly is JavaScript?](#toc.xhtml_s5a)

In the last section, we understood why browsers introduced JavaScript. Now, let's explore where does JavaScript fit in the web development paradigm.

To give an analogy, let's understand web development with the help of an example of a construction of a building.

Building construction takes place in the following three phases:

![](images/Figure-1.1.jpg)

**Figure 1.1:** Stages of development

Let’s understand each of these stages in the construction of a building and ultimately, derive an analogy with web development:

*   **Stage 1**: When the building construction begins, workers lay down the iron rods at the designated space, and fill in the cement. The result is a grey-colored construction (often inhabitable), a foundation, with spaces allotted for rooms.
*   **Stage 2**: This is the stage where the workers style the construction. The workers add designs and colors to the formerly grey building to make it look presentable.
*   **Stage 3**: While the building at the end of stage two can suffice for living in, this stage truly completes the construction. In this stage, workers add the essentials like elevators, parking spaces, electricity, and so on.

The third stage might not be mandatory, but it's notably significant. Similarly, in web development, HTML and CSS complete the first two stages of development of web pages – foundation and style. However, the result will solely be a website with zero interaction. JavaScript is the stage three that takes the website/web application a notch higher.

JavaScript, commonly known as JS, not only adds interaction to your web pages, but comes preloaded with a bunch of features:

*   Running code in response to particular events like clicking on an item on the webpage, pressing a key on the keyboard, scrolling down a web page, and many more.
*   It is built-in on all major browsers like *Google Chrome*, *Mozilla Firefox, Safari, Microsoft Internet Explorer, Microsoft Edge, Opera*, and many more, and it is free to use.
*   It is a structured and object-oriented programming language.
*   It is an interpreted language, that is, it works in a run-time environment, which means that there is no need to compile the code beforehand!
*   It can fetch data from the servers using a concept called AJAX, and utilize it to render elements on a web page.
*   It can get HTML elements shown on a web page, and it can also manipulate them.
*   Databases like MongoDB and platforms for server-side programming, for instance Nodejs, use JavaScript as their query language and application, respectively.

# [Setting up the system](#toc.xhtml_s6a)

In this section, we will set up our system to write exceptional code in JavaScript:

*   Since JavaScript (JS) is built-in in the majority of web browsers, you can use one of *Google Chrome, Mozilla Firefox, Safari, Internet Explorer, Microsoft Edge*, or *Opera* browsers for viewing your web pages. However, using *Google Chrome* is highly preferable because of its security and a superior developers' console.
*   Although you can use a simple text editor like Notepad on Windows machines for writing HTML, CSS, and JS code, it would be highly preferable if you install an **Integrated Development Environment** (**IDE**) software like *Visual Studio Code* or *Atom*.

In this book, we will be using **Google Chrome** and **Visual Studio Code** for development.

And that's it! You are ready to begin your journey of JavaScript!

# [How to add JavaScript to your web page?](#toc.xhtml_s7a)

You can apply **JavaScript** (**JS**) to the web page in the same way you add CSS to the web page. Like CSS, there are two distinct ways of adding JS to your code:

*   **Internal JavaScript**: In this method, you can add JS to your HTML code by inserting a **`<script>`** tag in the **`<head>`** or the **`<body>`** of your HTML. Since you are adding JS inside your HTML code or in other words, internally, this method is known as Internal JavaScript.

    To add JS code internally, open the *Visual Studio Code* application on your machine, and follow the steps, mentioned as follows:

    1.  Create an empty folder at a preferred location on your computer. Give the folder a suitable name.

        **Tip:** Naming conventions are very significant in web development. Although we will discuss this in greater lengths in the Bonus Chapters, a useful tip at this junction is that a good name should be short (less than 60 characters) and one look at the name should notify the reader about the content of that folder or file.

    2.  Create an HTML file, as shown, by the name **`index.html`**, and save it inside the folder you just created.
        1.  `<!DOCTYPE html>`
        2.  `<html>`
        3.  `      <head>`
        4.  `         <meta charset="utf-8">`
        5.  `         <title``>Adding JavaScript to the webpage</title>`
        6.  `     </head>`
        7.  `     <body>`
        8.  `         <p>Hello World!</p>`
        9.  `     </body>`
        10.  `</html>`

            **Code 1.1:** index.html

    3.  Next, create a **`<script>`** tag inside the head tag of your HTML code, and add the following lines:

        1.  `<script>`
        2.  `    alert("Hello World!");`
        3.  `</script>`

            **Code 1.2:** Adding the script tag to the HTML

        **Note:** You can add the `<script>` tag inside the `<body>` of your HTML code, as well. The difference between adding `<script>` in the `<head>` and the `<body>` is a marked difference in the performance of your website. We will have a look at this in the topic, The journey from typing a URL to the rendering of a web page.

        And that's it! Now, when you open index.html on your web browser, you will see a pop-up/dialog box with the words "**`Hello World`**" written inside it.

        ![](images/Figure-1.2.jpg)

        **Figure 1.2:** Screen showing an alert “Hello World”

*   **External JavaScript**: Going by the name of the term itself, External JavaScript (JS) refers to JS code added externally. It means that you do not write the JS code inside your HTML file. Instead, you write it on a separate file and inject (you will come across this term quite often) the JavaScript in your HTML file. To add external JS, follow the following steps:

    1.  Inside the same folder where you have created your HTML file, create another folder called *scripts*.
    2.  Inside the scripts folder, create a JS file by the name **`index.js`**. Remember, it's crucial to end the JS file with the extension **`.js`**. At this point, your folder structure should look like this:

        ![](images/Figure-1.3.jpg)

        **Figure 1.3:** Folder structure for External JS

    3.  Copy the JS code you had written for internal JS, without the **`<script>`** tag, and paste that in the file **`index.js`**. Your **`index.js`** file will now look like the following:
        1.  `alert("Hello World!");`

            **Code 1.3:** Adding alert to the index.js file

    4.  Now remove the **`<script>`** tag from your **`index.html`** and replace it with the following:

        1.  `<script src="./scripts/index.js"></script>`

            **Code 1.4:** Adding the external script tag

        Your HTML file will now look like the following:

        1.  `<!DOCTYPE html>`
        2.  `<html lang="en">`
        3.  `  <head>`
        4.  `          <meta charset="UTF-8">`
        5.  `             <meta` `name="viewport" content="width=device-width, initial-scale=1.0">`
        6.  `             <title>Adding JavaScript to the webpage</title>`
        7.  `             <script src="./scripts/index.js"></script``>`
        8.  `        </head>`
        9.  `        <body>`
        10.  `            <p>Hello World</p>`
        11.  `        </body>`
        12.  `</html>`

            **Code 1.5:** HTML file after adding the external JS

    The src attribute refers to the path where your JS file is stored. The string "./" in src refers to the current folder. So, we are moving to the scripts folder, and using /, we move inside the scripts folder and select the **`index.js`** file.

Now, when we open **`index.html`** in the browser, you will see a pop-up/dialog box with the words "**`Hello World`**" written inside it, as shown in *[figure 1.2](#c01.xhtml_fig1_2)*.

# [Comments in JavaScript](#toc.xhtml_s8a)

As with every significant programming language, JavaScript also provides a way to add comments that the browser will ignore. These comments are extremely useful in providing instructions to the developers who are working on the code on how the code functions.

JavaScript provides the following two styles of comments:

| // This is a single line comment | /*This is amulti-linecomment*/ |

**Table 1.1:** Single-line comment vs multi-line comment

# [Datatypes and operators in JavaScript](#toc.xhtml_s9a)

Almost every programming language works on values and the operations between the values. For instance, when you try to sign into your email account, you enter your email address and a password. The email address and the password are nothing but values. Similarly, if you use Facebook or Instagram as a social media application, and you like a photo/post, then you will notice the count of the likes (again, values) increase by 1\. Here, the web application performs the operation of adding 1 to the existing number of likes. In this section, we will learn about the different types of data (for instance, a text or a password in the first example and a number in the second) used in JavaScript, and the operators you can use on these data types.

# [Datatypes and variables in JavaScript](#toc.xhtml_s10a)

In every programming language, there is a container for storing values. This container is useful for storing numbers that you might require during a mathematical operation, or some text, or even an entire dictionary of information about some object like cars. This container is known as a **variable**.

In JavaScript (JS), variables can store just about anything. JS variables can store text strings, numbers, complex data, and entire functions.

To use a variable, we need to do the following things:

1.  Create a variable. (declaration)
2.  Give value to the variable. (initialization)

# [Create a variable (declaration)](#toc.xhtml_s11a)

To create a variable, we need to use the JS keyword var. (In *section 3* ES6, we will look at a few more keywords to create variables.)

The syntax for creating a variable is:

1.  `var name;`
2.  `var age;`

    **Code 1.6:** Syntax of variables

When you type the preceding command, JavaScript reserves a space in the memory for this variable. Think about this as an empty box (since we do not have any value assigned to it) placed in the system memory, which has the label of the name you attach to the variable.

**Note:** A variable that exists with no value assigned is *NOT THE SAME* as a variable that does not exist. Think about this as an empty box versus a box that does not exist. The former can place values inside it, while the latter cannot. A variable that has no value is called undefined.

# [Give a value to the variable (initialization)](#toc.xhtml_s12a)

Once a variable has been created (declared), you can give it a value. This process is known as *initializing a variable*. To initialize a variable, you type the name of the variable, followed by an equals sign (=), and complete it with the value you want to give to the variable.

1.  `name = 'John Doe';`
2.  `age = 24;`

    **Code 1.7:** Initializing variables

In the preceding examples, we assign the values 'John Doe' and '24' to the variables we created in the previous section.

You can also declare and initialize variables in one line.

1.  `var` `name = 'John Doe';`

    **Code 1.8:** Declaring and initializing a variable in one line

You can also update the value of a variable, which already has a value by typing the variable name followed by an equals sign, and the new value. For instance:

1.  `name = 'Cristiano Ronaldo';`

    **Code 1.9:** Changing the value of a variable

If you try to print the value of the name variable now, it will no longer be John Doe. The value of the name variable now will be Cristiano Ronaldo.

# [Data types in JavaScript](#toc.xhtml_s13a)

The data or the value that you store inside a variable can be of different types. For instance, in the preceding examples, we have seen numbers and text types. Unlike other programming languages, you don't require different keywords for different types of data in JavaScript. The different types of data in JavaScript are as follows:

*   **Numbers**: It comprises of whole numbers; for example, 30, or decimal numbers like 245.67\. You don't need to put these values in quotes.
    1.  `var num1 = 45;`

        **Code 1.10:** Number datatype

*   **Strings**: Strings are nothing but text. When you assign a string value to a variable, you need to wrap it with single-quotes or double-quotes.
    1.  `var name = 'John Doe';`

        **Code 1.11:** String datatype

*   **Booleans**: Booleans have two values - true or false. You don't need to wrap the value in quotes. Booleans are mostly used for testing conditions. For instance, if the value of the boolean variable is true, then you can execute certain code, or else you can set some other code for execution. It can also contain an expression like 10>5 as the value. In this case, as numeric10 is greater than numeric 5, the value of the variable containing this expression will be true.
    1.  `var isNumber = true;`

        **Code 1.12:** Boolean datatype

*   **Arrays**: Arrays are a complex data type that can store multiple values. Multiple values are stored inside square brackets and separated by commas. We will study arrays in more detail in *[Chapter 4: Arrays](#c04.xhtml)*.
    1.  `var cars = ['BMW', 'Audi', 'Rolls Royce'];`

        **Code 1.13:** Array datatype

*   **Objects**: Objects are also a complex data type which can store multiple values. However, unlike arrays, in objects, you can name the data that you are storing. Objects are used for modelling a real-life object. The multiple values are named and stored inside curly brackets.
    1.  `var employee = {name: 'John Doe', age: 24, city: 'London'}`

        **Code 1.14:** Objects datatype

JavaScript automatically detects the type of the value of a variable. Hence, JS is also called as a '*dynamically typed language*'.

# [Operators in JavaScript](#toc.xhtml_s14a)

JavaScript (JS) operators allow you to do mathematical operations, combine two strings, compare values, determine logic between variables or values, and also find the data type of a variable. Since this book caters specifically towards advanced JavaScript, we expect the readers to have a basic idea of JavaScript operators. While we will go through the theory of the basic JS concepts, and also look at one or two examples, we encourage the readers to practices different patterns on their own to refresh their knowledge of these basic concepts.

There are the following six major types of operators in JavaScript:

*   **Arithmetic Operators**: They are used to perform arithmetic operations on numbers. Arithmetic operators include + (addition), - (subtraction), * (multiplication), / (division), % (modulus, the remainder of a division), ++ (increment), and – (decrement).
    1.  `var sum = 4 + 3;      `*`//Output will be 7`*

        **Code 1.15:** Example of arithmetic operators

*   **Assignment Operators**: These operators are used for assigning values to the JavaScript variables.

    | **Operator** | **Example** | **Meaning** |
    | = | a = 5 | a = 5 |
    | += | a += 5 | a = a + 5 |
    | -= | a -= 5 | a = a - 5 |
    | *= | a *= 5 | a = a * 5 |
    | /= | a /= 5 | a = a / 5 |
    | %= | a %= 5 | a = a % 5 |
    | **= | a **= 5 | a = a ** 5 |

    **Table 1.2:** Assignment Operators

*   **String operators**: When the + operator is used on strings; it concatenates two strings.

    1.  `var txt1 = 'Hello';`
    2.  `var txt2 = 'World';`
    3.  `var greeting = txt1 + txt2;` *`//HelloWorld`*

        **Code 1.16:** Example of string operators

    **Note:** When you use the + operator on a number and a numeric string, the answer will be a string. For example, 5 + '5' will be '55'. However, if use any other arithmetic operator on a combination of strings and numeric strings, the arithmetic operation will succeed, and the answer will be numeric. For instance, '25'/5 will give 5.

*   **Comparison operators**: These operators are used for comparing two or more variables and/or values. The answer to the operations using comparison operators are boolean values. The various comparison operators are as follows:

    | **Operator** | **Example** | **Result** |
    | == (check equality) | 5 == '5' | true |
    | === (check for equal value AND type) | 5 === '5' | false |
    | != (check for non-equality) | 5 != '5' | false |
    | !== (check for non-equal value AND type) | 5 !== '5' | true |
    | > (greater than) | 5 > 2 | true |
    | >= (greater than or equal to) | 5 >= 5 | true |
    | < (less than) | 5 < 2 | false |
    | < (less than or equal to) | 2 <= 2 | true |

    **Table 1.3:** Comparison Operators

*   **Logical operators**: The logical operators determine the logic between variables and values. There are two major logical operators - && (logical and) and || (logical or). These operators will be extremely useful when you want to check multiple statements in conditional logic.
    1.  `(10 > 5) && (2 > 3)      `*`//false`*

        **Code 1.17:** Example of logical operators

*   **Type operators**: The **`typeof`** operator returns the data type of a variable or a value.
    1.  `typeof 'John Doe'` *`//string`*
    2.  `typeof 24` *`//number`*

        **Code 1.18:** Example of type operators

# [Conditionals and looping in JavaScript](#toc.xhtml_s15a)

Let's assume that we are creating an e-commerce application like Amazon or eBay. It's safe to expect that we will need to build hundreds, if not thousands, of rectangle cards to show items that are up for sale. *Would you spend hours manually creating every individual card?*

Given that it's an e-commerce application, there is every possibility that our user might search for a particular group of items. So, essentially, we will have to check whether the displayed items match the text typed by the user.

It's for cases like the ones mentioned here that we need concepts like looping and conditionals in JavaScript.

# [Conditional coding in JavaScript](#toc.xhtml_s16a)

Think about the following scenario:

You have an application that greets the user on the loading page. If it is morning or afternoon, the web application welcomes the user with the message "*Good Day*". If it is past 4 PM, the web application greets the user with "*Good Evening* ".

The very essence of our preceding problem statement relies on the if…else condition. JavaScript achieves this conditional coding using two types of conditionals – if…else and switch.

# [If…else conditional statement](#toc.xhtml_s17a)

The if…else conditionals are reasonably simple to use.

You type the keyword `if` followed by parentheses.

Inside the parentheses, you write a conditional test. If the value of the test is true, statement 1 will be executed. If the value of the test is false, then statement 2 will be executed.

![](images/Figure-1.4.jpg)

**Figure 1.4:** Syntax of if…else statement

For our problem statement, the code could look something like the following:

1.  `var hours = new Date().getHours();`
2.  `if(hours < 16) {`
3.  `    alert("Good Morning");`
4.  `} else {`
5.  `    alert("Good evening");`
6.  `}`

    **Code 1.19:** Example of if…else conditional statement

It's alright if you don't understand the first line of the code. You will read it in the future chapters. It gets the current date and fetches the hours as per the 24-hour format. The next two lines are basic conditional statements. To add multiple conditions, you can replace the **`else`** with an **`else if(condition)`**.

1.  `var hours = new Date().getHours();`
2.  `if(hours < 16) {`
3.  `    alert("Good Morning");`
4.  `} else if(hours > 16 && hours < 23) {`
5.  `    alert("Good evening");`
6.  `} else {`
7.  `    alert("Good night");`
8.  `}`

    **Code 1.20:** Example of if…else…if conditional statement.

# [Switch conditional statement](#toc.xhtml_s18a)

Let’s consider another scenario. In this use-case, a variable receives the grade of a student from the server. Based on the grade, our web application should print a message. If the grade is '*A*', it should print '*Excellent*'. If the grade is '*B*', it should print '*Good*'. '*C*' should print '*Average*', and '*D*' should print '*Failed*'.

In such a case, we can use the if…else…if conditionals, but the resultant code will be long and not so elegant. An elegant solution will be the switch statement.

In a switch statement, an expression or a variable is fed to the keyword switch. The answer to the expression or the value of the variable are one of the cases inside the curly braces following the switch keyword. If the case value matches the expression answer or the value of the variable, the statement inside the case is executed. If no value is matched, then the default case is executed.

![](images/Figure-1.5.jpg)

**Figure 1.5:** Syntax of switch statement

So, our example can be resolved using the following code:

`1\. var grade = 'A';`

`2.`

`3\. switch(grade) {`

`4.     case 'A':`

`5.         alert('Excellent');`

`6.         break;`

`7.     case 'B':`

`8.         alert('Good');`

`9.         break;`

`10.     case 'C':`

`11.         alert('Average');`

`12.         break;`

`13.     case 'D':`

`14.         alert('Failed');`

`15.         break;`

`16.     default: alert('Not present for exams');`

`17.}`

**Note:** Having a break statement is extremely important in switch statements. If you remove the break statements and execute this code, you will observe that all the cases get executed.

Think of a switch statement as a waterfall. It will go through everything unless you apply an obstruction (break) in between.

# [Looping in JavaScript](#toc.xhtml_s19a)

Let's assume you have a task to display numbers from 1 to 100\. What will you do? You would possibly go about creating 100 <p> elements having numbers from 1 to 100, correct? What if I increase the difficulty and make that 100 to 100,000?

In such cases, we make use of a JavaScript concept called loops. Looping functions basically begin with an initial value and keep incrementing or decrementing the value, until you resolve a condition.

![](images/Figure-1.6.jpg)

**Figure 1.6:** Flowchart of looping

There are two types of looping functions in JavaScript – for loop and while loop (with an alternate version called do…while loop). As shown in *[figure 1.5](#c01.xhtml_fig1_5)*, all the logics follow the same following pattern:

1.  Initialize a variable with a value.
2.  Test that value.
3.  Execute if true, quit if false.

In the following *[table 1.4](#c01.xhtml_tab1_4)*, we will understand and compare the different looping methods in JavaScript:

| `for(var i=0; i<100; i++) {``console.log(i);``}` | `var i=0;``while(i<100) {``console.log(i);``i++;``}` | `var i=0;``do {``console.log(i);``i++``}``while(i<100);` |
| In a for loop, the keyword `for` is followed by three expressions inside parentheses, separated by semicolon (;).The first expression initializes the value, the second expression sets the condition, and the third expression updates the value.After the statements inside the curly braces are updated, the value is updated by the third expression.As long as the result of the condition expression is true, the statements inside the curly braces will be executed. If the result of the condition becomes false, the code will break out of the for loop. | In a while loop, the variable is initialized outside the actual looping statement.The keyword `while` is followed by a condition expression. As long as the result of the condition expression is true, the statements inside the curly braces will be executed.The value is updated inside the curly braces. After the statements inside the curly braces are executed and the subsequent value is updated, the condition at the top is checked again.If the condition is true, the process is repeated, else the code will break out of the loop. | The do…while loop is similar to the while loop. The only difference here is that the condition is checked only after the statements inside the curly braces are executed at least once.If the condition is true, the statements will be executed again or else the code will break out of the loop. |

**Table 1.4:** The different looping methods in JavaScript

# [The Journey of the Web Page](#toc.xhtml_s20a)

**The process we know** is that we type a URL in the browser. A few seconds later, a web page magically appears on the browser.

**The process we don't know** is that the webpage goes through an entire adventure from the moment a user enters the URL to the point the browser shows the webpage. It begins its journey, as a URL, from the user's browser to a remote server, sends a request to the server, and receives the server's response to the request. Finally, it travels back from the server, and loads itself on the user browser as a webpage.

![](images/Figure-1.7.jpg)

**Figure 1.7:** The journey of the webpage from a URL to a rendered page

Let's try to understand this process with an example of **https://www.google.com**:

![](images/Figure-1.8.jpg)

**Figure 1.8:** Opening **www.google.com** on the browser

1.  **Fetching the domain name**: When a user types the URL '**https://www.google.com**' in the browser, the browser takes the host-name (sometimes also called the domain-name) of the URL and calls the service of the DNS server. In a URL, the host-name is the part after the https (which is known as the protocol). In our case, the domain name, as a whole, will be www.google.com.
2.  **Resolving the IP address**: The **Domain Name System** (**DNS**) server is nothing but a public directory of domain names. The DNS server contains a list of hostnames and their IP addresses (a numeric label assigned to a device connected to a computer network). The DNS server looks up the IP address for **www.google.com** and returns that IP address to the browser.
3.  **Creating the HTTP request**: The browser creates an HTTP request for the server hosting the previously mentioned IP address and requests the server to send the HTML page for www.google.com.
4.  **Returning the response**: If the request is successful, the server sends back an HTTP response to the server with the HTML page attached to the response.

    At this point, let’s just assume that our HTML page looks like the following (**Disclaimer**: It looks entirely different from this, but for the sake of simplicity, we are assuming this to be the HTML response):

    1.  `<html>`
    2.  `    <head>`
    3.  `        <title>Google</title>`
    4.  `    </head>`
    5.  `    <body>`
    6.  `        <h1>Google</h1>`
    7.  `        <div>`
    8.  `            <p>Search</p>`
    9.  `            <button>Search Google</button>`
    10.  `        </div>`
    11.  `    </body>`
    12.  `</html>`

        **Code 1.22:** Sample HTML response

5.  **Creating the DOM tree**: When the browser receives the HTML, it tries to create a **Document Object Model** (**DOM**) tree. (A quick HTML refresher, all HTML tags need to end with a '/'.)
    1.  When the HTML parser goes through this HTML file, the first thing it finds is an open html tag. So, the parser adds the html tag to the root of the tree.

        ![](images/Figure-1.9.jpg)

        **Figure 1.9:** html will be added as a root node.

    2.  Now, the parser moves to the next line and actively looks for the closing tag of the html that has just been added to the DOM tree. Instead, it finds another open tag – head. Since, the html tag has not been closed yet, the parser interprets the head as a child of the html tag. So, it creates a head branch under the html root of the tree.

        ![](images/Figure-1.10.jpg)

        **Figure 1.10:** head will be added as a child

    3.  The parser now changes its priority and it actively looks for the closing tag for the head element. Instead, it finds another tag called title. Similar to the last process, the HTML parser interprets title as a child of the head tag.

        ![](images/Figure-1.11.jpg)

        **Figure 1.11:** title is added as a child to the head

    4.  Inside the title tag, it now comes across a text called *Google*. Since it’s not an HTML element, the parser adds that as a content to the title branch of the tree. Once again, the parser changes its priority to finding the closing tag of the title tag.
    5.  Right after the text "*Google*", the parser finally comes across the closing tag for title. Since, it has now received the closing tag for title, the parser considers that task as complete and now moves one level above the title tag, and changes its task to finding the closing tag for the head element.
    6.  Next, the parser finds the closing tag for the head, and therefore, completes that process and moves one level up to the root element on the tree, and moves to the next line in the code.
    7.  With the title and the head elements closed, the parser now searches for the closing tag for the html element, but instead finds a new element called body. Going through the same process we encountered, it now interprets body as a child element for the html.

        ![](images/Figure-1.12.jpg)

        **Figure 1.12:** body is added as a child of html

The parser similarly goes through the entire HTML file, until it finds the closing tag for the html element, and creates a DOM tree that looks like the following:

![](images/Figure-1.13.jpg)

**Figure 1.13:** The final DOM tree

The final DOM tree for the HTML is shown in the preceding screenshot.

With the help of this DOM tree, all the elements of the HTML can now be accessed with their content and attributes stored within them. Each HTML element is now considered as an object.

# [JavaScript and the DOM](#toc.xhtml_s21a)

In the previous section, we understood the structure of the DOM. In this section, we will explore how **JavaScript** (**JS**) uses the DOM to fetch elements and manipulate them.

In HTML, you must have learnt about classes and IDs. JavaScript works on those concepts to fetch the elements. JS uses the term Document object to fetch elements. The Document object refers to the entry point for the loaded web page, which is the DOM tree. You can select elements from the DOM using the following methods:

1.  **`document.getElementById(id)`**: Using this method, JavaScript parses through the DOM tree, and finds the first element having the same ID and terminates the search. Hence, if there are multiple elements having the same ID, only the first element will be returned.
2.  **`document.getElementsByClassName(classnames)`**: In this method, JavaScript parses through the entire DOM tree and locates all elements having the class name mentioned inside the parentheses. The result is a list of elements stored in an array-like datatype called as **HTMLCollection**. This method can also be called only on the element and not the entire document.
3.  **`document.getElementsByTagName(name)`**: Similar to the previous method, JavaScript parses through the entire DOM, collects all the elements having the same tag-name, and stores them inside an **HTMLCollection**. However, this method turns the name inside the parentheses to lower-case before proceeding. So, you need to be careful about elements which are written in *camelCase*.
4.  **`document.querySelector(selectors)`**: This method returns the first element that matches the CSS selector that you add in between the parentheses. For example,
    1.  `var element = document.querySelector('#container');`

        **Code 1.23:** Example of document.querySelector()

To manipulate an HTML element’s content, you can fetch the element using any of the preceding methods. After that, you can use a method called **`innerHTML`** to fetch the contents of the element. For instance:

1.  `var content = document.getElementById('container').innerHTML;`

    **Code 1.24:** Fetching an element using innerHTML

Here, content will give you the content inside the element having an ID container.

Similarly, if you want to modify the content, you can use the same method for setting the content. For instance:

1.  `document.getElementById('container').innerHTML = "Hello World";`

    **Code 1.25:** Change the HTML of an element

# [Conclusion](#toc.xhtml_s22a)

In this chapter, we refreshed the basic concepts of JavaScript. We covered variables, data types, operators, conditionals, and looping in JavaScript. We also had a detailed look at the DOM tree and how JS uses the DOM tree to fetch and manipulate elements. There is a likely chance that you might already have a great idea about the topics we just covered. However, these topics will prove to be a rigid foundation for the advanced concepts that we will be learning in this book.

In the next chapter, we will begin by exploring the Developer's Console, a remarkably handy tool to help you code in JavaScript and web development.

# [Points to remember](#toc.xhtml_s23a)

*   JavaScript (JS) variables which are declared but not initialized, are undefined. They are not the same as JavaScript variables which are not declared.
*   JS is a dynamically typed language. It means that the declared variable can change its datatype if a new value with a different datatype is assigned to it.
*   If you use the '+' operator on numeric strings, for example, "5"+"5", it will concatenate the string and give you the result as "55". However, if you use any other arithmetic operator on numeric strings, for example, "5" * "5", it will perform the arithmetic operation on the result and give you the mathematical value, for instance, "25" in the preceding case.
*   '==' only compares the value, while '===' compares the value and the datatype.
*   JavaScript uses the DOM tree extensively to fetch and manipulate HTML elements.

# [Multiple choice questions](#toc.xhtml_s24a)

1.  **Which of the following is not a datatype in JavaScript?**
    1.  string
    2.  number
    3.  int
    4.  boolean
2.  **Which of the following statement is not true?**
    1.  '===' does a strict comparison of two variables or values.
    2.  JavaScript is a dynamically typed language.
    3.  '200'+'2' will give you '202'.
    4.  Variables which are not initialized return undefined.

# [Answers](#toc.xhtml_s25a)

1.  c
2.  c

# [CHAPTER 2](#toc.xhtml_c02)

# [The Developer’s Tools](#toc.xhtml_c02)

In the previous chapter, we refreshed our knowledge of the basic concepts of JavaScript. In this chapter, we will look at a web developer's best friend in the process of web development – *The Developer’s Tools*.

However, before we start exploring the **Developer Tools** (**DevTools**), we will quickly run through another useful JavaScript concept, called *Event Listeners*. After that, we will explore the DevTools of the Google Chrome browser through a series of screenshots, live coding (optional), and a few theoretical concepts.

# [Structure](#toc.xhtml_s26a)

In this chapter, we will cover the following topics:

*   Event Listeners in JavaScript
*   Introduction to the Developer Tools
*   Panels in DevTools
*   JavaScript and the DevTools

# [Objective](#toc.xhtml_s27a)

After studying this chapter, you should be able to understand events in JavaScript. You can listen for events happening on the web page, and handle these events using JavaScript and make use of the browser’s in-built Developer Tools to debug your JavaScript code.

# [Event Listeners in JavaScript](#toc.xhtml_s28a)

In a web development scenario, events are incidents or actions that happen on your web page. For instance, a user is trying to login to his/her Gmail account. The user will enter his/her username and password, and click on the **`Sign In`** button. If the username and the password are accurate, the web page will show the user his/her mails. If they are inaccurate, the web page will show an error message.

In JavaScript, this action of clicking a button is an event. The web page actively waits for this event to occur – this is called event listening. Finally, the result of displaying the user's emails or an error message after the click of the **`Sign In`** button is known as *event handling*.

In JavaScript, events are fired inside the web browser. These events are attached to either the item that fires the event, a set of HTML elements, the HTML document which houses the web page, or the entire browser window.

Apart from click, there are many other events in JavaScript. A few commonly encountered events include the following:

*   When a web page has finished loading.
*   The user has submitted a form.
*   The user presses a key on the keyboard.
*   The user hovers over an HTML element.
*   An error occurs.

Let's take a look at an example of how to add an event listener to a button:

1.  `<!DOCTYPE html>`
2.  `<html>`
3.  `    <head>`
4.  `        <title>Event Listeners</title>`
5.  `        <script src="./scripts/index.js"></script>`
6.  `     </head>`
7.  `     <body>`
8.  `        <button id="btn">`
9.  `            Turn me red!`
10.  `        </button>`
11.  `    </body>`
12.  `</html>`

    **Code 2.1:** The index.html file for adding the event listeners

In the preceding code example, we have created the index.html file, which has a button with an id 'btn'. We have also imported the index.js file externally in the **`index.html`** file.

1.  `var button = document.querySelector("#btn");` *`//Store the element in a variable`*
2.  `button.addEventListener('click', function(event) {`
3.  `event.target.style.backgroundColor = 'red';`
4.  `});`

    **Code 2.2:** The JavaScript in index.js for adding event listeners

The preceding code example shows the index.js file, where we add an event listener to the button 'btn' defined in the *[code example 2.1](#c02.xhtml_co2_1)*.

To add event listeners, you need to use a function aptly called **`addEventListener`**. The function **`addEventListener`** needs to be called on the element (or the variable containing the element).

It takes the following two arguments:

*   The first argument is the type of event; for example, click, hover, keypress, and so on. (You can check out the entire list of events on **[https://developer.mozilla.org/en-US/docs/Web/Events](https://developer.mozilla.org/en-US/docs/Web/Events).**)
*   The second argument is a function or a block of code that needs to be executed when the event occurs. This event handler function comes up with an optional pre-defined argument/parameter. You can name it whatever you’d like to. This optional argument stores the built-in JavaScript object called *Event*, which contains the details of the event that has just occurred.

**Code explanation**: In the preceding *[code example 2.2](#c02.xhtml_co2_2)*, we have used the optional pre-defined argument/parameter inside the function argument of the **`addEventListener`** method to fetch more details about the click event on the button.

As we learnt earlier, we can give any name to this parameter. In the *[code example 2.2](#c02.xhtml_co2_2)*, we name it event. Apart from the various details about the click event on the button, this variable possesses a key called target. The target key contains the HTML element from which the event has been fired. In our case, this will be the button element having the id 'btn'. Therefore, the code **`event.target`** refers to the HTML element button where this event happened.

Next, we change the background-color of the button stored in the **`event.target`** to red by typing **`style.backgroundColor`**. By typing style after **`event.target`**, we fetch all the styles of the button. Then, by adding **`backgroundColor`** to the **`event.target.style`**, we fetch the background-color property of the element. Finally, we change it to 'red'.

# [Introduction to the Developer Tools](#toc.xhtml_s29a)

The Developer Tools, popularly known as *DevTools*, are a set of phenomenal tools that are pre-built inside modern browsers. These set of tools provide extraordinary features to the web developers, as shown in the following screenshot:

![](images/Figure-2.1.jpg)

**Figure 2.1:** Features of the Developer Tools

The features of the Developer Tools are as follows:

*   Inspecting the currently loaded web page’s HTML, CSS, and JavaScript.
*   Editing web pages on-the-fly.
*   Displaying a list of all the resources, including images, videos, XML documents, PDFs, and so on, that make up the web page’s UI.
*   Figuring out the time taken by every resource to get downloaded from the server to the user’s browser.
*   Simulating how the web page would look on different devices, like different mobile phones, iPad, laptops, and so on.
*   Analysing run-time performance and helping the user in optimizing the website speed.

The preceding list is just a collection of features commonly available in the developer tools of different modern browsers. The developer tools in different modern browsers might also provide a set of additional features from the ones mentioned previously.

In this book, we will be working on the developer tools of the *Google Chrome* browser. At the time of writing, I used the *Google Chrome version 85.0.4183.83*. For future updates and features, check out **https://developers.google.com/web/updates**.

# [Opening the DevTools](#toc.xhtml_s30a)

There are multiple ways of opening the Chrome DevTools. In this section, we will go through all the different ways in which you can open the Chrome DevTools. Feel free to choose any method that you feel convenient. Let’s have a look at the following different ways of opening Chrome DevTools:

*   **Clicking Inspect to view a particular DOM Element:** The first method to open the DevTools is by inspecting any HTML element on the web page. To inspect an element, you need to complete the following steps:

    ![](images/Figure-2.2.jpg)

    **Figure 2.2:** Clicking on Inspect to open Chrome DevTools.

    1.  Open a web page on your Google Chrome.
    2.  Right-click on any particular UI element on the web page. As shown in the preceding screenshot, a dropdown menu appears when you right-click a UI element. On the dropdown that appears on the screen, click on Inspect.
    3.  The window of Chrome DevTools will appear to the right side of your web page. Since you have opened DevTools by clicking on Inspect, it will open in a panel called *Elements*. (We will learn more about the different panels of the Chrome DevTools in the next section.)![](images/Figure-2.3.jpg)

    **Figure 2.3:** Chrome DevTools open to the right of the web page in Elements panel

*   **Opening DevTools from the *Google Chrome* toolbar:** The second method is to follow the traditional method of opening the DevTools from the toolbar of *Google Chrome.*

    ![](images/Figure-2.4.jpg)

    **Figure 2.4:** Opening Chrome DevTools from the Chrome toolbar

    On the extreme right of the Google Chrome toolbar, you will notice three vertical dots ![](images/vert.jpg). Click on the three vertical dots to reveal a menu. Go to **`More Tools`** -> **`Developer Tools`**.

*   **Keyboard shortcut for opening the Elements Panel:** Press *Control + Shift + C* (on Windows and Linux machines) or *Command(*⌘*) + Shift + C* (on Mac machines) to open the Elements panel of Chrome DevTools. The Elements panel is typically used for inspecting the HTML or the CSS of the web page.
*   **Keyboard shortcut for opening the Console panel:** Press *Control + Shift + J* (on Windows and Linux machines) or *Command(*⌘*) + Shift + J* (on Mac machines) to open the Console panel of Chrome DevTools. The Console panel is typically used for running JavaScript or for viewing logged messages.
*   **Keyboard shortcut for opening the last panel that you had opened:** Press *Control + Shift + I* (on Windows and Linux machines) or *Command(*⌘*) + Option(*⌥*) + I* (on Mac machines) to open the last panel of Chrome DevTools that you had opened.

# [Panels of DevTools](#toc.xhtml_s31a)

If you open the Chrome DevTools using any of the methods listed earlier, you will see a collection of tabs at the top of the DevTools. These tabs are called as *panels*. Each panel of the DevTools caters to a different aspect of the loaded web page. In this chapter, we will primarily try to understand the Sources and the Console panel, as they cater to the JavaScript of the page. Let's take a brief look at the different panels of the Chrome DevTools:

*   **Elements Panel:** The Elements Panel is used for viewing the HTML and the CSS of the loaded web page. You can also double-click on an element or a property to change its value and the corresponding change(s) can be seen on the web page. One of the best features of the Elements Panel is the CSS Box Model denoted by the multi-coloured box on the bottom right of the following screenshot. It helps you understand how the element is placed, the dimensions of the elements, the space it occupies, and much more.

    ![](images/Figure-2.5.jpg)

    **Figure 2.5:** Elements Panel of Chrome DevTools

*   **Console Panel:** The Console Panel is used for viewing the messages, warnings, or the errors raised by the webpage. The Console panel can also be used for running any JavaScript code.

    ![](images/Figure-2.6.jpg)

    **Figure 2.6:** Console Panel of Chrome DevTools

*   **Sources Panel:** This panel is greatly useful for debugging JavaScript code of the loaded webpage. You can add breakpoints to view the status of your code and the variables at various points of your code lifecycle. You can also edit JavaScript and save the edited changes to the disk.

    ![](images/Figure-2.7.jpg)

    **Figure 2.7:** Sources Panel of Chrome DevTools

*   **Network Panel:** In the Network Panel, you can view the network activity of the web page. Network activity includes the requests sent by the browser to download the various resources like HTML files, CSS files, images, videos, and so on, that are required by the webpage. You can also observe the amount of time taken by each resource to get downloaded.

    ![](images/Figure-2.8.jpg)

    **Figure 2.8:** Network Panel of Chrome DevTools

*   **Performance Panel:** The Performance Panel is used for monitoring the performance of the web page. This panel will give you detailed information about the time taken by each process from loading to rendering. It also generates performance reports of the web pages.
*   **Memory Panel:** The Memory Panel is used for tracking the memory usage and leaks.
*   **Application Panel:** This panel contains the user data stored in the browser in the form of cookies, local storage (permanent storage), or session storage (temporary storage). This panel also holds information about the application cache, the images, the fonts, and the stylesheets.
*   **Security Panel:** This panel is concerned with the security of the webpages.

# [JavaScript and the DevTools](#toc.xhtml_s32a)

As mentioned earlier, the Sources and the Console panels cater to the JavaScript on the Chrome DevTools. Using the Chrome DevTools, we can do the following in JavaScript:

*   Viewing or changing the HTML DOM of the loaded webpage.
*   Execute JavaScript unrelated to the webpage.
*   Pause the execution of the webpage’s JavaScript to view or change the page’s DOM.

To begin with, let's explore the Console panel and the Sources panel.

# [Console Panel](#toc.xhtml_s33a)

The primary job of the console panel is to display the various logs, errors, or warnings thrown by the webpage. However, you can also execute completely unrelated JavaScript code on the Console Panel. Moreover, when the JavaScript execution of the web page has been paused, you can print, and check the values received by the variables before the pausing of the code. You can even execute and test conditions related to the code during the pause in the execution.

![](images/Figure-2.9.jpg)

**Figure 2.9:** Console Panel

The preceding screenshot shows the Console Panel of the Chrome DevTools. The Console Panel has two major sections that are denoted by numbers 1 and 2.

# [Console Area](#toc.xhtml_s34a)

The section denoted by number 1 in *[figure 2.9](#c02.xhtml_fig2_9)* denotes the actual console area, which shows the messages logged by the JavaScript written for the web page or the messages logged by the browser itself.

All the messages, irrespective of their category, show a clickable link to the extreme right. Each link represents the source from where that particular message has been logged.

In *[figure 2.9](#c02.xhtml_fig2_9)*, the source of the first three messages is the file **`index.js`**. The number after the colon (:) represents the line number at which the message has been logged.

The source of the last three messages is the code (script) written on the browser itself – hence, their source links are tagged as VM, followed by a number. Since the script has been written on the browser, the term VM here stands for Virtual Machine, followed by an ID that has been assigned to the script written on the browser. If you click on these links, they will direct you to the Sources panel.

Additionally, this console area also serves as a free area for trying any JavaScript code, even if it’s not related to the web page itself. For instance, in the preceding *[figure 2.9](#c02.xhtml_fig2_9)*, below the red messages, we have created an array 'numbers', which stores the numbers 2, 3, and 4, and a for loop which prints every number from the array 'numbers'.

# [Filter Area](#toc.xhtml_s35a)

The section denoted by the number 2 in *[figure 2.9](#c02.xhtml_fig2_9)* is the filter area of the console. It shows a sidebar, which has grouped the messages shown in section 1\. Before we try to understand the sidebar shown in *[figure 2.9](#c02.xhtml_fig2_9)*, let’s try to understand the different types of messages shown in the Console panel.

**Types of messages (logs)**

To begin with, there are the following two main categories of console messages (logs):

*   **User messages**: User messages (logs) are the messages that are logged on to the console by the user, that is, either an explicit JavaScript code written for the web page console by a web developer, or some arbitrary code written by the user viewing the console. For instance, in *[figure 2.9](#c02.xhtml_fig2_9)*, the messages that are logged after the for loop has been executed, are the messages logged by the user viewing the console. So, they belong to the user messages category. Similarly, if you click on the link next to the first two messages, it will open the index.js file on the Sources panel. Here, you will see that the developer who has written the **`index.js`** file has typed a script called **`console.warn()`** and **`console.error()`**. Since these messages have been logged by the script, where the user has explicitly asked the browser to log these messages, they also belong to the user messages category.

    To filter out all the user messages, you can click on the second item in the sidebar, which has the keyword 'user messages'.

    ![](images/Figure-2.10.jpg)

    **Figure 2.10:** Filtering user messages on the Console

    After clicking on the user messages, if you compare *[figure 2.9](#c02.xhtml_fig2_9)* and *[figure 2.10](#c02.xhtml_fig2_10)*, you will observe that a message with the red background that started with '**`Uncaught TypeError`**', is no longer shown on the console. This shows that the message '**`Uncaught TypeError`**' was, in fact, logged by the browser.

*   **Browser messages**: Browser messages are the messages that are logged by the browser itself. These messages are not prompted by the script that has been written by the web developer for the loaded web page. These messages are logged when the browser parses through the JavaScript code, and believes that there might be some problem with the web page. For instance, in the *[figure 2.9](#c02.xhtml_fig2_9)*, the browser threw an error when it could not find an element by the id 'btn'. Hence, it could not apply the style.

As you can see in *[figure 2.10](#c02.xhtml_fig2_10)*, there are four more categories of logged messages. These four categories are based on the severity of the message. The four categories are **Verbose**, **Info**, **Warning**, and **Error**.

*   The Verbose messages refer to the code written on the browser. For instance, the variable numbers and the for loop in *[figure 2.10](#c02.xhtml_fig2_10)* belong to the verbose category.
*   The messages logged using **`console.log()`** are called as Info messages.
*   The messages which serve as a warning are called Warning messages. They are seen on the console with a faint yellow background. They can also be manually printed using **`console.warn()`**.
*   Finally, the messages that have crashed the application or have the potential to crash the application, belong to the Error messages category. They are seen with a bright red background. They can also be manually logged using **`console.error()`**.

# [Header of the console](#toc.xhtml_s36a)

The header of the console panel is shown as follows:

![](images/Figure-2.11.jpg)

**Figure 2.11:** The header of the console panel

Let’s have a detailed look at the different parts of the header of console panel. However, solely reading this text might not help you in understanding them. My personal recommendation would be to go back in time and act like a kid, and try out every button to see what happens. (* inserts tongue-out smiley *)

*   The first button ![](images/Image47220.jpg) is used to show/hide the filter section denoted by the number 2 in *[figure 2.9](#c02.xhtml_fig2_9)*.
*   The second button ![](images/Image47230.jpg) is used to clear all the messages on the console.
*   The third section ![](images/Image47237.jpg) is a dropdown, which shows the JavaScript context. By default, it is set to top, which denotes the DOM of the loaded web page. However, if you have an ad embedded in your page, this ad will be a part of an iframe. Such iframes create a different context on the console. By selecting a context, you can filter the console messages for a particular web document.
*   The fourth button ![](images/Image47245.jpg) is used for creating live expressions. If you believe that some script always needs to be executed on the console, you can create that using Live Expressions. For example, it could be the date and time at which the web page is currently being shown.
*   The filter box is used for filtering messages by typing some text.
*   The Default Levels dropdown is the same as the filter section denoted by number 2 in *[figure 2.9](#c02.xhtml_fig2_9)*. When the filter section is hidden, the Default Levels dropdown shows the various categories of the messages.
*   Finally, the ![](images/Image47256.jpg) button displays the settings of the Console, which include options like preserving the log messages even after the web page has been reloaded.

# [Sources Panel](#toc.xhtml_s37a)

The second of the two panels that deal with JavaScript on the Chrome DevTools is the Sources Panel. The Sources Panel is primarily used for debugging the JavaScript code. As shown in the following screenshot, the Sources Panel has the following three parts:

1.  The **File Navigator** pane displays all the files requested by the page in folders.
2.  The **Code Editor** pane shows the content of the file selected in the File Navigator pane.
3.  The **JavaScript Debugging** pane is used for inspecting the page’s JavaScript.

    ![](images/Figure-2.12.jpg)

    **Figure 2.12:** The Sources Panel

We will try to understand the different panes of the Sources panel using a live coding example. Create a folder by the name *Exploring DevTools* on your local machine, and add an **`index.html`** file inside it. Add another folder inside the *Exploring DevTools* folder, and name it 'scripts'.

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `    <head>`
4.  `        <meta charset="UTF-8">`
5.  `        <title>Learning JavaScript</title>`
6.  `    </head>`
7.  `    <body>`
8.  `        <p id="total"></p>`
9.  `        <script src="scripts/console.js"></script>`
10.  `    </body>`
11.  `</html>`

    **Code 2.3:** index.html for Exploring DevTools

Inside the folder 'scripts', add a JavaScript (JS) file, and name it **`console.js`**.

1.  `function add(n1, n2) {`
2.  `    var num1 = n1;`
3.  `    var num2 = n2;`
4.  `    var total = num1 + num2;`
5.  `    document.getElementById('total').innerHTML = total;`
6.  `}`
7.  `add("5", "4");`

    **Code 2.4:** console.js for Exploring DevTools

When you save these files and open index.html on your browser, you will notice that the **`<p>`** element gets the value 54 instead of 9\. (It’s alright if you don’t understand the code written inside **`console.js`**. We will cover functions in the next chapter.) To understand where our function **`add`** went wrong, our first instinct would tell us that we should check the part of our code where the addition happens.

The Sources panel of the DevTools can help us in such a scenario by pausing the execution of the JavaScript, and the rendering of the page’s UI, with the help of breakpoints. We can, then, check the JavaScript code to understand where our execution is failing.

In our scenario, we would like to pause our JS execution at the point where the variable total adds the two numbers, right before its value gets added to the element with the id **`total`**. To pause our execution, we need to add breakpoints to our code. There are two ways of adding breakpoints to the JS code:

*   **Adding debugger to the code**: To add a debugger to the code, you need to add the word debugger, right before you want the browser to stop JS execution. In our scenario, we want to pause the execution right after the sum is calculated. Hence, it will be right before the **`document.getElementById()`**. After the addition of the debugger, the code inside console.js will look like the following:
    1.  `function add(n1, n2) {`
    2.  `    var num1 = n1;`
    3.  `    var num2 = n2;`
    4.  `    var total = num1 + num2;`
    5.  `    debugger;`
    6.  `    document.getElementById('total').innerHTML = total;`
    7.  `}`
    8.  `add("5", "4");`

        **Code 2.5:** console.js after adding the debugger

*   **Selecting a breakpoint in the DevTools:** Alternatively, you can add a breakpoint to a particular line of code on the Sources panel by clicking on the number next to the line.

    ![](images/Figure-2.13.jpg)

    **Figure 2.13:** Selecting a breakpoint on the DevTools

    The moment you click on the number next to the line of code you want to add a breakpoint to, two things will happen – A blue arrow icon will appear on the number (indicating it is a breakpoint) and that particular line will be added to a section called Breakpoints in the JavaScript debugging pane.

After adding the breakpoint, when you refresh the webpage, the JavaScript execution will stop at the line of the breakpoint.

![](images/Figure-2.14.jpg)

**Figure 2.14:** JavaScript execution pausing at the debugger

In the first case scenario, as shown in the preceding screenshot, the JS execution stops at the point where the debugger has been added into the code.

In the second case scenario, as shown in the following screenshot, the JS execution stops at the point where the blue breakpoint has been added.

![](images/Figure-2.15.jpg)

**Figure 2.15:** JavaScript execution pauses at the line highlighted by blue marker

In both the cases, the rendering of the webpage is paused.

If you look at the preceding screenshot closely, you will observe the following:

1.  In the **Code Editor** pane, next to every line of code, it shows the value of the variables on that line. Similarly, if you hover over any variable name, it will show the value of that variable in a tooltip.
2.  In the **Scope** pane of the JavaScript Debugging section, you can see the value of all the variables used in the code so far.

Thanks to the breakpoints, we can now see that the values received in the variables n1 and n2 are of type string (indicated by the double quotes). As we have learnt before, adding two strings with a '+' operator, concatenates the two strings. To resolve this, we will need to convert the strings on lines 2 and 3 to numbers.

Now that we have successfully debugged the code, we can click on the ![](images/Image47412.jpg) (Resume Script Execution) icon in the JavaScript (JS) Debugging pane to resume the JS execution of the page. If there is another breakpoint, the JS execution will be paused at that breakpoint. The next button on the header ![](images/Image47422.jpg) (Step over) will continue the pause of the JS execution, but will also move it to the next line of code. To try this, in the Sources panel, add a breakpoint on line number 2, where we define the variable n1\. When the page is refreshed, the JS execution stops at line number 2, indicated by a green background. If you now press the Stepover function, you will notice that the web page is still paused, but the green background has now moved to line number 3.

By default, the JS execution will not enter functions or loops. The group of buttons ![](images/Image47429.jpg) (Step into and Step out) are used for entering and exiting the JS execution inside the loops or functions.

The first button in the group of buttons ![](images/Image47440.jpg) is used for disabling all the breakpoints, while the second button is used for ensuring that the code always pauses its execution whenever an error or an exception is thrown. If you click on the first button on the Sources panel, you will see it turn to a shade of blue. Now, when you refresh the page, the JS execution will not be paused. The first button pauses execution for both debuggers and breakpoints added on the Sources panel.

**Tip:** When the JavaScript (JS) execution has been paused due to the breakpoints or the debugger, typing the name of the variables in the console panel (used in the JS code so far) will render their values in the Console. In this way, you can execute expressions or test conditions in the Console panel while the JS execution has been paused. Try it out! (Pause your JS execution at line 3 of code *example 2.5* and type n1 in the console panel.)

# [Conclusion](#toc.xhtml_s38a)

In this chapter, we refreshed the JavaScript concept of events and event listeners. We also explored debugging the JavaScript code using the **`Sources`** and the **`Console`** panel of the JavaScript. Finally, we learnt about the different types of messages that can be logged on the console by the user or the browser.

In the next chapter, we will explore the concept of functions in JavaScript. Functions are probably the most useful thing for any JavaScript developer.

# [Points to remember](#toc.xhtml_s39a)

*   In JavaScript (JS), events are the incidents or actions that are happening on the web page. You can listen to, and handle the events using the JS function called **`addEventListener()`**.
*   The Chrome **Developer Tools** (**DevTools**) cater to every aspect of the web page. The JavaScript of the webpage can be handled and viewed by the Console and the Sources panel of the DevTools.
*   The Console panel shows the different types of messages that are logged by the user or the browser. Messages can be either Verbose (code typed by the user on the console), Info (informational messages logged using **`console.log()`**), Warning (warnings triggered by the user code or by the browser), and Error (errors triggered by the user code or by the browser).
*   Messages on the Console panel that are logged by the user in the JavaScript code are called user messages. When the browser considers a user code to create a problem, it logs an error or a warning on the console. These errors or warnings are called as browser messages.
*   You can pause the execution of the JS code by adding a debugger to the code, or by adding a breakpoint by clicking on the line number next to a line of code on the Sources panel.

# [Multiple choice questions](#toc.xhtml_s40a)

1.  **It is mandatory to use the e argument shown in the following function. – True or False?**
    1.  `document.getElementById('btn').addEventListener('click', function(e) {`
    2.  `    e.target.innerHTML = 'Button clicked';`
    3.  `})`

        **Code 2.6:** MCQ Question 1

    1.  True
    2.  False
2.  **In the *[code example 2.6](#c02.xhtml_co2_6)*, what happens when line 2 is executed?**
    1.  An alert is displayed on the web page with the text 'Button clicked'.
    2.  The text inside the button changes to 'Button Clicked'.
    3.  The text 'Button Clicked' is appended to the text inside the button.
    4.  The button is removed from the web page.

# [Answers](#toc.xhtml_s41a)

1.  **b**
2.  **b**

# [CHAPTER 3](#toc.xhtml_c03)

# [Functions](#toc.xhtml_c03)

Let's picture a simple scenario. In our potential web application, we will add a primary login process that will request the user to enter his/her email address and password. Now, when the user inserts his/her details, and clicks on the login button, several things happen.

To begin with, we will first fetch the email address entered by the user, and check for its validity. If the email address exists in our database, it implies that the user has registered with our website, and that the email address entered by the user is valid.

Next, we will fetch the password, and match it with the password that is added to our database by the user. If the passwords match, it indicates that the user is genuine, and we can give him the access to the home page of our application. If the passwords do not match, we need to inform the user on the login page itself that the password entered is incorrect.

As you can see, a simple click of a button will require the execution of a specific code, which is exclusive to the process of login only. Moreover, this block of code needs to be executed every time the user will try to login to the system.

For such scenarios where we need to write reusable blocks of code, we use functions.

# [Structure](#toc.xhtml_s42a)

In this chapter, we will cover the following topics:

*   Exploring functions
*   Types of functions
*   JavaScript Scope
*   JavaScript Closure

# [Objective](#toc.xhtml_s43a)

After studying this chapter, you should be able to successfully understand when and how to create functions. You will understand when to reuse a block of code and create functions for writing reusable pieces of code. This chapter will help you improve your coding knowledge by using the latest functionalities.

# [Exploring Functions](#toc.xhtml_s44a)

In simple terms, a JavaScript (JS) function is a block of code that is designed to perform a specific task. Think of functions like a container where we store expensive cutlery reserved for guests. Only when we have guests coming over, we open that box to use the fancy cutleries.

![](images/Figure-3.1.jpg)

**Figure 3.1:** Imagine functions as containers storing code which will be opened only when it is needed

In JavaScript terminology, the instance of 'storing the cutlery' or creating a function is called as defining or declaring a function. Similarly, the act of 'opening the box of cutlery when required' or using a function is called as invoking or calling a function.

# [Syntax](#toc.xhtml_s45a)

The syntax (structure of statements) of a JS function is as follows:

1.  `function functionName(argument_1, argument_2, …, argument_n) {`
2.  *`//code to be executed`*
3.  `}`

    **Code 3.1:** Syntax of function declaration

**Explanation**: To create/declare a JS function, you need to do the following four things:

1.  Use the keyword function.
2.  Typically, the keyword function will be followed by a name to represent the function. To write the function name, camel casing is highly recommended.
3.  It will be followed by a pair of parentheses '()'. Universally, in programming languages, a function is denoted by a pair of parentheses. These parentheses can either be empty, or they can store variables that can be used in the function’s code execution. These variables are called as arguments.
4.  Finally, since the primary job of a function is to store a block of code that will be executed at will, this block of code is stored inside a pair of curly braces '{}'.

**Tip:** Naming a function is an extremely crucial task. Think of it this way, if you are creating an e-commerce web application, then you will be creating hundreds of functions for different purposes. Say, you have created two functions – login and logsin. The login function checks the username and the password, while the logsin contains the block of code to be executed after a user has successfully logged in. Now, coding for a massive platform like an e-commerce application which might house close to ~20000 lines of code, there is every chance that you might accidentally type logsin where you wanted to type login, or vice versa. This mistyping might even crash the application. Imagine your user yelling at their screen when your application crashes in the middle of some payment. To avoid such a scenario, the name of the function should clearly tell you what task the function will perform. In the preceding example, we could name the two functions as `onLogin` and `onLoginSuccess`.

Let’s try to understand the preceding syntax using a simple example:

1.  `function add(number1, number2) {`
2.  `    var sum = number1 + number2;`
3.  `    console.log("The sum of " + number1 + " and " + number2 + " is " + sum);`
4.  `}`

    **Code 3.2:** Declaring the function add

I would urge you to try this example on your own by creating a JS file in your local machine or by typing the preceding code in the Console panel of your browser.

In the preceding lines, we have created a function **`add`** that adds two numbers. As you can see, the function add receives two values as arguments. It adds these two values and stores the result in a variable by the name, sum. It then prints the variable sum on the console.

In the preceding example, we declared a function which adds two numbers. Now, let’s move to the second part, where we call this function.

The syntax for calling or invoking a function is as follows:

1.  `functionName(argument_1, argument_2, …, argument_n);`

    **Code 3.3:** Syntax of function invocation.

**Explanation**: To call a function, we simply need to write the function name and follow it up with a pair of parentheses '()'. The sole job of the parentheses it to call the function. If you don’t add the parentheses after the function name while invoking/calling the function, the function will not be called and subsequently, it will not be executed.

In *code 3.2*, we declared a function add which adds two numbers. Now, let’s use the syntax that we learnt in code 3.3 to call/invoke our function add.

1.  `add(1, 2);`

    **Code 3.4:** Calling the function add

When you type this code on your VS Code or the console, you should get a statement in your console which has the text '**`The sum of 1 and 2 is 3`**'.

In the following screenshot, we have declared and called the function add on the Console panel of the browser. As you can see in the screenshot, we have boasted the reusability of our function add by calling the function add repeatedly using different numbers.

![](images/Figure-3.2.jpg)

**Figure 3.2:** Declaring and calling the function add on the console

So far, we have seen functions which require and accept arguments. However, there might be times when your function will not require any arguments. For example, consider this scenario where we want to welcome the user when our web application loads on the user’s browser window. Let’s look at an example showing a function with no arguments:

1.  `window.onload = greetUser();`
2.  `function greetUser() {`
3.  `    alert("Welcome to Amazon!");`
4.  `}`

    **Code 3.5:** Functions without arguments

In the preceding *[code example 3.5](#c03.xhtml_co3_5)*, we call the function **`greetUser`** after the window has been loaded. The keyword window refers to the HTML that is loaded on the user’s browser window. On the loading of the HTML, the browser calls the function **`greetUser`**. Since the sole purpose of the function **`greetUser`** is to call the alert dialog-box with the text '**`Welcome to Amazon!`**', we do not require any arguments.

# [Functions returning values](#toc.xhtml_s46a)

In the example shown in *code 3.2*, we have a function add which adds two numbers and shows the result on the console. Now, consider a scenario where the function **`add`** is called twice with different values. The results of the function’s execution are then required to change two different HTML elements. How will you solve this problem statement?

To solve such scenarios, we use a keyword called return to send back a value after the function has completed its execution. This value will be returned to the line of code where the function was called. Let’s understand this with a coding example. Create a folder '**`Functions returning values`**' on your local machine. Inside the folder, create an **`index.html`**, as shown in the *[code example 3.5](#c03.xhtml_co3_5)*. Create another folder inside the folder '**`Functions returning values`**', and name it '**`scripts`**'.

1.  `<!DOCTYPE html>`
2.  `<html>`
3.  `    <head>`
4.  `        <title>Functions returning values</title>`
5.  `    </head>`
6.  `    <body>`
7.  `        <div>`
8.  `            The result of 2 and 3 is <span id="result1"></span>`
9.  `        </div>`
10.  `        <div>`
11.  `            The result of 12 and 10 is <span id="result2"></span>`
12.  `         </div>`
13.  `     </body>`
14.  `</html>`

    **Code 3.5:** index.html

Inside '**`scripts`**', create a file called **`index.js`** and inside the file **`index.js`**, type the code, as shown in following *[code example 3.6](#c03.xhtml_co3_6)*:

1.  `function add(number1, number2) {`
2.  `    return number1 + number2;`
3.  `}`
4.  `var result1 = add(2, 3);`
5.  `console.log("result1: ", result1);`
6.  `var result2 = add(12, 10);`
7.  `console.log("result2: ", result2);`
8.  `document.getElementById("result1").innerHTML = result1;`
9.  `document.getElementById("result2").innerHTML = result2;`

    **Code 3.6:** index.js showing the function add returning values.

After saving the two files, when you open **`index.html`**, you will see the following:

![](images/Figure-3.3.jpg)

**Figure 3.3:** Executing a function that returns values

As you can see in the Console panel of the DevTools, the function **`add`** calculated the sum of the two values passed in its arguments and returned the respective results to the lines 5 and 8 of **`index.js`** from where it was called. These respective results are stored in the variables result1 and result2 on lines 5 and 8 respectively. These values are then populated inside the HTML elements having ids result1 and result2.

# [Types of functions](#toc.xhtml_s47a)

In the preceding sections, we have seen a simple declaration of the function, and its subsequent execution. The function add, which we have seen in the preceding examples, is just one style of writing functions. Let’s take a look at the different varieties of the following functions:

*   **Named functions**: The function declaration of the function add, which we have seen in the example *code 3.2*, is an example of named functions. In named functions, we create a function by giving it a name.
    1.  `function add(number1, number2) {`
    2.  `    return number1 + number2;`
    3.  `}`
    4.  `add(2, 3);`

        **Code 3.7:** Named functions

*   **Immediately Invoked functions**: Whenever a variable or a function is declared, a space in the global memory (in our case, it is the memory of the browser, which is accessible by calling the object window) is reserved for that variable/function.

    In the case of immediately invoked functions, we call the functions as soon as they are declared. Hence, they are known as *Immediately Invoked functions*. The benefit of an immediately invoked function is that since no variables are created, it does not take up space in the global object or the global memory.

    Immediately invoked functions are especially useful when you have already used up a lot of global memory and the execution of this function warrants an immediate result, instead of waiting for the result.

    1.  `(function (number1, number2) {`
    2.  `    return number1 + number2;`
    3.  `})(2, 3);`

        **Code 3.8:** Immediately invoked functions

*   **Anonymous functions**: In simple terms, an anonymous function is a function without a name. However, unlike immediately invoked functions, anonymous functions are not executed as soon as they are declared. As shown in the example *code 3.9*, we have replicated the example *code 3.7* of named functions. However, instead of giving the function a name, we are keeping it unnamed and storing the function in a variable by the name sum.

    1.  `var sum = function(number1, number2) {return number1+ number2;};`
    2.  `sum(2, 4);`

        **Code 3.9:** Adding an anonymous function to the variable sum

    So, why and where do we need anonymous functions?

    1.  `setTimeout(function() {`
    2.  `    console.log("This message appears after 3 seconds");`
    3.  `}, 3000);`

        **Code 3.10:** Anonymous functions as an argument to the setTimeout() method of JavaScript

    There are two major scenarios where we can use anonymous functions, which are as follows:

    1.  When the function is very short in size, it’s always preferable to omit the name and keep the function declaration short.
    2.  When you are passing a function as an argument to another function. For instance, in the *[code example 3.10](#c03.xhtml_co3_10)*, we use a function as an argument to the JavaScript method of **`setTimeout()`**. In the *[code example 3.10](#c03.xhtml_co3_10)*, the function will be executed after waiting for 3 seconds.
*   **Recursive functions**: A recursive function is a function that keeps calling itself. The recursive function also contains a condition inside its block of code. If the condition fails, the recursive function will stop calling itself. The perfect example to explain recursive functions is to create a countdown timer. In the following *[code example 3.11](#c03.xhtml_co3_11)*, the function countdown keeps calling itself until the value of the variable **`nextNum`** is 0.
    1.  `function countdown(number) {`
    2.  `    console.log(number);`
    3.  `    var nextNum = number - 1;`
    4.  `    if(nextNum > 0) {countdown(nextNum);}`
    5.  `}`
    6.  `countdown(5);`

        **Code 3.11:** An example of a recursive function

*   **Method**: The functions that are a part of an object are called *methods*. For instance, in the *[code example 3.12](#c03.xhtml_co3_12)*, we have an anonymous function as the value of the key **`getFullName`** inside the object person. This function **`getFullName`** is called as the method of the object person. To call the method **`getFullName`**, you need to type the **`objectName.functionName()`** or **`objectName[functionName]()`**.
    1.  `var person = {`
    2.  `    firstName: "John",`
    3.  `    lastName: "Doe",`
    4.  `    getFullName: function() {`
    5.  `        console.log(this.firstName + " " + this.lastName);`
    6.  `    }`
    7.  `};`
    8.  `person.getFullName();` *`//John Doe`*

        **Code 3.12:** The getFullName method of the object person

# [JavaScript Scope](#toc.xhtml_s48a)

To understand the concept of scope, let’s imagine a zoo. In a zoo, every animal is kept in its own private enclosure. What if the zookeepers decided to keep the deer and the lion in the same enclosure? Similarly, what if the giraffes were kept in the same icy enclosure as a penguin? It would result in problems. Similarly, in JavaScript, variables that are defined inside a function have their own enclosure or a private space. This space is called as a *scope* and it is not accessible to the code outside the function.

There are two types of scopes in JavaScript:

*   **Global Scope**: The global scope refers to the space outside all the functions and the code block. This scope refers to the JavaScript program as a whole. Every function and every code of block can access the value of the variables stored in the global scope.
*   **Local Scope**: When a variable is declared inside a function or inside a pair of curly braces, its access is limited only to the block of code inside that function or inside those curly braces. Any block of code outside the function or the curly braces cannot access this variable which is defined inside the function. This variable is local to the function, hence, such variables are having a local scope.
    1.  `var number = 25;`
    2.  `console.log("Call 1 | Before and outside the function. Number: ", number);`
    3.  `function displayNumber() {`
    4.  `    console.log("Call 2 | Inside the function before re-initializing. Number: ", number);`
    5.  `    var number = 40;`
    6.  `    console.log("Call 3 | Inside the function after re-initializing. Number: ", number);`
    7.  `}`
    8.  `console.log("Call 4 | After the function, before calling the function. Number: ", number);`
    9.  `displayNumber();`
    10.  `console.log("Call 5 | After the function, after calling the function. Number: ", number);`

        **Code 3.13:** JavaScript scope example.

When you execute this code, the result is as follows:

![](images/Figure-3.4.jpg)

**Figure 3.4:** The result of the code executed in code 3.13

The following are a few points to remember:

*   The chain of the scope works from inwards to outwards. It means that when the browser encounters a variable, it searches for the variable inside the local scope. If it is not found inside the local scope, then the browser searches for the variable in the global scope. If it is not found in the global scope as well, then the variable is considered undefined.
*   In the *[code example 3.14](#c03.xhtml_co3_14)*, we have two functions – **`func1`** and **`func2`**. They are declared separately in the global scope. As you can see in the code, one of the functions **`func2`** is called inside the code block of the function **`func1`**. However, the variable declared inside **`func1`** is not accessible inside **`func2`**. This is because the two functions are called separately in the global scope. Because of this, the two functions have separate local scopes. Hence, the variable **`i`** defined inside the function **`func1`** belongs to the local scope of **`func1`** and hence, it cannot be accessed inside the function **`func2`**.
    1.  `function func1() {`
    2.  `    var i = 20;`
    3.  `    func2();`
    4.  `}`
    5.  `function func2() {`
    6.  `    console.log(i);`
    7.  `}`
    8.  `func1();` *`//undefined`*

        **Code 3.14:** The functions are defined separately in the global scope

*   When a function has multiple nested (children) functions, every child function will have access to all the variables stored in its ancestors’ scope. This scope is called as *Lexical Scope*. However, a point to be noted here is that while the child functions have access to all the ancestors’ codes, the ancestors’ code will not have access to the code of the children. Let’s try the lexical scope in *[code example 3.15](#c03.xhtml_co3_15)*:
    1.  `function grandparent() {`
    2.  `    var g_age = 75;`
    3.  `    parent();`
    4.  `    function parent() {`
    5.  `        var p_age = 50;`
    6.  `        child();`
    7.  `        function child() {`
    8.  `            var c_age = 25;`
    9.  `            console.log(g_age, p_age, c_age);`
    10.  `        }`
    11.  `    }`
    12.  `}`
    13.  `grandparent();` *`//75 50 25`*

        **Code 3.15:** Functions that are nested inside each other

# [JavaScript Closure](#toc.xhtml_s49a)

A closure in JavaScript is a function that has access to the parent scope even after the parent scope has closed. In layman’s terms, it incorporates the idea of a private function. High-level programming languages like Java include concepts known as private and public. Private functions imply that these functions cannot be called by any code, except the one hosting it. Closures in JavaScript help us achieve such a feat. Let’s understand the closure with an example shown in the following screenshot:

![](images/Figure-3.5.jpg)

**Figure 3.5:** Closures

The first thing that we observe in the preceding screenshot is that the variable add is a combination of an anonymous function and an immediately invoked function. Now, let’s first try to understand the inner function after the variable counter has been defined (starting at line 3). In the inner function, we access the value of the variable counter defined in the outer parent anonymous function. (Lexical scope, remember? :P) The inner function updates this counter value. It increases the value of the variable counter by 1 and returns this value. Therefore, when the function add is called for the first time, the value of the variable counter received inside the inner function will be 0. Next, this value 0 will be increased to 1, and this value 1 will be returned back to line 3 (where the function was called). Simple so far, right?

Now, we have the value returned from the inner function at line number 3 as 1\. However, right before the inner function is defined on line number 3, we have a keyword called return. This return statement belongs to the outer anonymous function. So basically, the value returned by the inner function now becomes the value of the outer function, and it is this value which is returned by the outer function. Therefore, when we call the function add for the first time, the value returned is 1.

Now, when we call the function add for the second time, remember the value of the outer function in the previous execution was changed to 1. Therefore, the value now received by the inner function is 1, which is then updated to 2 and returned back to the outer anonymous function. Hence, the second invocation of the add function will give you the value 2.

Similarly, the third execution will use the retained value of 2, update it to 3, and return the value 3.

This process of retaining the value is commonly conceived as a private variable in the object-oriented languages like Java. In JavaScript, we emulate the concept of private variables using this method, which is called as *closure*.

# [Conclusion](#toc.xhtml_s50a)

The most important takeaway from this chapter is how to reuse code. Often, as developers, we fall into the pit of repeating our code.

Repeating code is not only wasting your precious time, but it also means that more lines of code = bigger size of the web page = more time taken to download from the server = more time taken to load on the browser.

In short, if you don’t want your customers to get bored waiting for your web page to load, reuse your code. Functions are literally blocks of code which complete a task. More often than not, these blocks of code need to be repeated more than once. So, functions quite literally help your web page to load faster.

In the next chapter, we will look at arrays – one of the ways to store multiple related data.

# [Points to remember](#toc.xhtml_s51a)

*   Functions help you to write code which will be reused again and again. Writing functions will not only save your time, but will also help your page load faster.
*   Creating a function is called declaring or defining a function. Using a function is called calling or invoking a function.
*   The pair of parentheses '()' are the most important part of functions. Functions can be called only if the pair of parentheses are present.
*   When you wish to create a function which will be reused, it’s ideal to name that function. When you want to save global memory, you can use immediately invoked functions. When a function is small in size or when a function needs to be passed as an argument to another function, we use anonymous functions.
*   In scenarios where we need to ask a function to call itself repeatedly until a condition to stop calling it becomes true, use recursive functions.
*   Functions that are a part of an object are called as methods.
*   The accessibility of a variable defined inside a function or a block of code is called local scope. The accessibility of a variable defined outside all the functions is called a global scope.
*   The innermost nested function can access the variables of all its ancestors. This concept is called as lexical scope.
*   JavaScript closures emulate the concept of private variables.

# [Multiple choice questions](#toc.xhtml_s52a)

1.  **We use an immediately invoked function when we need to pass a function as an argument to another function. – True or False?**
    1.  True
    2.  False
2.  **What will be the output of the following code?**
    1.  `function grandparent() {`
    2.  `    var g_age = 75;`
    3.  `    parent();`
    4.  `    function parent() {`
    5.  `        var p_age = 50;`
    6.  `        sibling();`
    7.  `    }`
    8.  `    function sibling() {`
    9.  `        var s_age = 25;`
    10.  `        console.log(g_age, p_age, s_age);`
    11.  `    }`
    12.  `}`
    13.  `grandparent();`

        **Code 3.16:** MCQ Question 1

    1.  75 50 25
    2.  75 25 50
    3.  25 50 75
    4.  Error

# [Answers](#toc.xhtml_s53a)

1.  **b**
2.  **d**

# [CHAPTER 4](#toc.xhtml_c04)

# [Arrays](#toc.xhtml_c04)

In simple words, we use an array for storing multiple related values.

Say, if someone asks you to list down five luxury cars. You might reply with, say, BMW, Audi, Mercedes, Jaguar, and Lamborghini. If you observe closely, all of these names/values belong to the same category or the same type, which is cars.

In JavaScript, this category '*cars*' can be an array, and this array can store multiple values of the same or the related concept, which in this case is cars.

In this chapter, we will dive deep into this concept of arrays. We will begin by understanding the idea of arrays. After that, we will learn how to create an array, and finally, we will explore the astounding methods of array. As always, it is highly recommended to practice the codes shown in this chapter to understand the concepts better.

# [Structure](#toc.xhtml_s54a)

In this chapter, we will cover the following topics:

*   Introducing arrays
*   Using arrays
*   Array properties and methods

# [Objective](#toc.xhtml_s55a)

After studying this chapter, you should be able to understand the concept of arrays and then use them for storing multiple related values. You will learn to utilize the remarkable properties of arrays.

# [Introducing Arrays](#toc.xhtml_s56a)

In the introduction earlier, we learned that arrays are used for storing multiple related values. Let's continue with the example we explored in the introduction.

If someone asks you to list down five luxury cars in JavaScript, how would you do that? Based on whatever you've learned so far, you will create a separate variable for every car. Our code will look something like the following:

1.  `var car1 = 'Audi';`
2.  `var car2 = 'BMW';`
3.  `var car3 = 'Mercedes';`
4.  `var car4 = 'Jaguar';`
5.  `var car5 = 'Lamborghini';`

    **Code 4.1:** Listing down variables for every car

Since we had to list only five cars, it was fairly easy to create five different variables. However, if you were asked to name every car brand on the planet, would you end up creating a thousand separate variables? Creating thousands of variables would invite several problems. A few of them are as follows:

*   It pollutes the global memory space by reserving space for thousands of variables.
*   You might lose track of the variables created. For instance, you might often face the question, 'What name have I given to the variable that stores the value of BMW?'
*   What if you want to loop through every car brand, and print only those cars whose name starts with B?
*   If you have to create HTML elements showing every car brand, can you imagine the efforts you will need to take to achieve such a simple task?

To solve all these problems, JavaScript introduced the concept of arrays.

An array is a unique variable that can store multiple values. It can hold multiple values under one single variable name!

Arrays are ordered collections. It means every value stored inside an array has an indexed position assigned to it. If you want to fetch any value stored inside the collection, all you need to do is access the value by its position.

# [Using Arrays](#toc.xhtml_s57a)

Now that we know what arrays are, let’s first understand how arrays are created. After that, we will learn how to use the arrays, and where to use them.

# [Creating an array](#toc.xhtml_s58a)

Previously, we learned about creating variables. As we learned earlier, to create a variable, we need to declare a variable, and then initialize it. Similarly, to create an array, we need to declare and initialize the array.

# [Declaring an array](#toc.xhtml_s59a)

There are two ways to declare an array, which are as follows:

*   **An array literal**: Using an array literal is the simplest way to create an array. Like variables, you will need to use a JavaScript keyword followed by a name for the array. To declare an array, you assign the variable name with square bracket notations. These square bracket notations are called as array literals. This will create an empty array.
    1.  `var cars = [];`
    2.  `var numbers = [];`

        **Code 4.2:** Declaring an array using array literals.

*   **The JavaScript keyword new**: The second method involves using the JavaScript keyword new, and the JavaScript object Array, followed by a pair of parentheses. This method will also create an empty array.
    1.  `var cars = new Array();`
    2.  `var numbers = new Array();`

        **Code 4.3:** Declaring an array with JavaScript keyword new.

Although you can use both the methods to declare an array, it is highly recommended to use the first method for declaring an array. The first method is simpler. It has better readability, and its execution speed is also faster.

# [Initializing an array](#toc.xhtml_s60a)

Like variables, after an array is declared, we initialize the array. Since an array can store multiple values, each value will be separated using commas (as shown in *[code example 4.4](#c04.xhtml_co4_4)*). An array can store values of any datatype. Like the declaration of an array, there are two ways of initializing the array, which are as follows:

*   **An array literal**: For arrays initialized using an array literal, all you need to do is type the array name, and assign the values separated by commas inside the square notations. As you can see in the following *[code example 4.4](#c04.xhtml_co4_4)*, arrays can store values of any datatype.
    1.  `cars = ['BMW', 'Audi', 'Mercedes', 'Jaguar', 'Lamborghini'];`
    2.  `numbers = [2, 4, 5, 6, 8];`
    3.  `console.log(cars);` *`//(5) ["BMW", "Audi", "Mercedes", "Jaguar", "Lamborghini"]`*
    4.  `console.log(numbers);` *`//(5) [2, 4, 5, 6, 8]`*

        **Code 4.4:** Initializing an array of array literals

*   **The JavaScript keyboard new**: Like the preceding method, you can initialize the array that was created using the JavaScript keyword `new` by supplying multiple values separated by commas inside the parentheses. As shown in the *[code example 4.5](#c04.xhtml_co4_5)*, values separated by comma need to be added inside the parentheses.

    1.  `cars = new Array('BMW', 'Audi', 'Mercedes', 'Jaguar', 'Lamborghini');`
    2.  `numbers = new Array(2, 4, 5, 6, 8);`
    3.  `console.log(cars);` *`//(5) ["BMW", "Audi", "Mercedes", "Jaguar", "Lamborghini"]`*
    4.  `console.log(numbers);` *`//(5) [2, 4, 5, 6, 8]`*

        **Code 4.5:** Initializing an array that is created using new keyword

    However, one drawback of this method is that when you add a single number inside the parentheses, it initializes an array with a length specified in the number passed inside the parentheses. As shown in the *[code example 4.6](#c04.xhtml_co4_6)*, it creates an array of empty values with the length specified in the parentheses.

    1.  `var numbers = new Array();`
    2.  `numbers = new Array(5);`
    3.  `console.log(numbers);` *`//(5) [empty × 5]`*

        **Code 4.6:** Initializing with a single number will create empty values

    Like variables, you can also declare and initialize an array on the same line:

    1.  `var cars = ['BMW', 'Audi', 'Mercedes', 'Jaguar', 'Lamborghini'];`

        **Code 4.7:** Declaring and initializing the array on the same line.

# [Access the elements of an array](#toc.xhtml_s61a)

The values that are stored inside the array are called the elements of the array. As we had learnt earlier, arrays are ordered collection. It means that every element in an array is stored at an indexed position. In an array, the indexed position starts with 0\. It basically means that the first element of an array is at position 0, the second element is at position 1, and so on.

Let’s use the array created in the *[code example 4.7](#c04.xhtml_co4_7)* as an example in this section. Arrays are generally denoted graphically using square boxes, as shown in the following screenshot:

![](images/Figure-4.1.jpg)

**Figure 4.1:** Positions of an element

To access the elements inside an array, you can write the name of the array, followed by the position of the element inside square brackets. As shown in the *[code example 4.8](#c04.xhtml_co4_8)*, to access the third element in the array cars, we type cars [2].

1.  `var cars = ['Audi', 'BMW', 'Mercedes', 'Jaguar', 'Lamborghini'];`
2.  `console.log(cars[2]);` *`//Mercedes`*

    **Code 4.8:** Accessing an element

As we can see in the *[code examples 4.9](#c04.xhtml_co4_9), [4.10](#c04.xhtml_co4_10),* and *[figure 4.2](#c04.xhtml_fig4_2)*, printing an array inside an element will print a comma-separated string of values inside the element.

We first create the following **`index.html`**:

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `<head>`
4.  `    <meta charset="UTF-8">`
5.  `    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
6.  `    <title>Document</title>`
7.  `</head>`
8.  `<body>`
9.  `    <span id="text1"></span>`
10.  `    <script src="scripts/index.js"></script>`
11.  `</body>`
12.  `</html>`

    **Code 4.9:** index.html for printing array inside the HTML element

Then, we create the following **`index.js`**:

1.  `var cars = ['BMW', 'Audi', 'Mercedes'];`
2.  `console.log(cars);`
3.  `document.getElementById('text1').innerHTML = cars;`

    **Code 4.10:** index.js for printing array inside the HTML element

Finally, we get the following output:

![](images/Figure-4.2.jpg)

**Figure 4.2:** Array printed inside the HTML element.

# [Change the elements of an array](#toc.xhtml_s62a)

To change the elements of an array, you need to access the position of the array where you need to make a change, and assign the new value using '='.

1.  `var cars = ['BMW', 'Audi', 'Mercedes'];`
2.  `console.log('Cars before changing the element: ',cars);`
3.  `cars[1] = 'Jaguar';`
4.  `console.log('Cars after changing the element at position 1: ',cars);`
5.  `cars[7] = 'Rolls Royce';`
6.  `console.log('Cars after changing the element at position 7: ',cars);`

    **Code 4.11:** Changing elements of an array – index.js

As shown in the *[code example 4.11](#c04.xhtml_co4_11)* and the subsequent *[figure 4.3](#c04.xhtml_fig4_3)*, we changed the element at the position 1 of the array cars from Audi to Jaguar. However, if you try to change the element at a position far beyond its actual length, the element gets added with empty elements in between.

![](images/Figure-4.3.jpg)

**Figure 4.3:** Console panel of changing elements of an array

# [Array Properties and Methods](#toc.xhtml_s63a)

In the preceding sections, we have learnt a great deal about arrays. We have learnt what arrays are, their declaration, and their initialization. More importantly, we have determined that arrays are used when we need to store multiple related values in one place.

However, the primary strength of the arrays is the properties and methods of the arrays. In this section, we will explore the remarkably useful properties and the methods of arrays.

# [length](#toc.xhtml_s64a)

The length property of an array returns the length of the array, that is, the number of elements inside the array.

1.  `var cars = ['BMW', 'Audi', 'Mercedes'];`
2.  `console.log(cars.length);` *`//3`*

    **Code 4.12:** The length property of arrays

# [Accessing first and last elements of an array](#toc.xhtml_s65a)

In the previous section, we had learnt that to access an element of an array, we need to provide the position of the element. With that logic, it’s fairly easy to access the first element of an array since the first position of every array is 0.

However, accessing the last element of the array using that logic is tricky, as the size of arrays will vary with every array. Therefore, we will never truly know what the index position of the last element is.

Thanks to the length property, we can now access the last position of the element. As shown in the *[code example 4.13](#c04.xhtml_co4_13)*, **`array.length`** will give the length of the array. Since the array starts with 0, the last element will always be a number less than the length of the entire array. In this way, to access the last element of an array, we can simply type **`array.length-1`** as the position index of the array.

1.  `var cars = ['BMW', 'Audi', 'Mercedes'];`
2.  `console.log(cars[0]);` *`//BMW`*
3.  `console.log(cars.length - 1);` *`//2`*
4.  `console.log(cars[cars.length-1]);` *`//Mercedes`*

    **Code 4.13:** Accessing the last element of an array

# [Looping through an array](#toc.xhtml_s66a)

We have seen a few instances of the for loop in the previous chapters. The best way to loop through all the elements of an array is to use the for loop. We will use the length of the array as the condition till which the for loop should keep executing. As shown in the following screenshot, after a few iterations, the value of the variable **`i`** will become equal to the length of the array. Since the conditional part of the array checks for the condition where the value of **`i`** is less than the length of the array, it will fail and break out of the loop.

![](images/Figure-4.4.jpg)

**Figure 4.4:** Looping through an array

# [push and pop](#toc.xhtml_s67a)

The push and the pop methods are used for adding elements to an array or removing elements from an array. To understand the concept of push and pop, let’s consider the example of a building or a block of LEGOs.

Imagine an array as a building, or a block of LEGOs that are placed one over another. In both the cases, the first floor or the first block is always placed right at the bottom. Similarly, the last floor or the last block will always be the one right at the top.

Now, let’s understand the arrays using these blocks or the building as an analogy. Like the building, the first element of the array will be the one right at the bottom, while the last one will be at the top.

![](images/Figure-4.5.jpg)

**Figure 4.5:** An array as a block of LEGOs or a building

Now, if I would ask you to add a new floor to the building, or add a new block to the block of LEGOs that you have created, where would you add the new floor or the new block?

At the top, correct? Using the preceding concept as an analogy, if you have to add a new element to the array, you will place it at the top, that is, after the last element. Similarly, the logic behind removing an element would be to remove the element which is at the very top. In this scenario, if you would try to remove a floor from the middle of the building, it could end up destroying the entire building.

![](images/Figure-4.6.jpg)

**Figure 4.6:** Pushing and popping an element

As shown in the preceding screenshot, pushing is when you place an element at the top (at the end) of an array. Popping is when you remove the element from the top (from the end) of an array. As shown in the following screenshot, when you use the push method, you need to provide a value in the parentheses. However, when you pop an element, you don’t need to add any value, as it will remove whichever element is at the top of the stack in the array (at the end of the array).

![](images/Figure-4.7.jpg)

**Figure 4.7:** Pushing and popping arrays.

# [delete](#toc.xhtml_s68a)

In the previous example, we learnt about removing elements from the end of the array. Now, what if you wanted to remove an element from the middle of an array?

There will always be a scenario where you might want to remove an element from a particular position of the array. To achieve this, we use delete.

![](images/Figure-4.8.jpg)

**Figure 4.8:** Deleting an element from a particular position of the array

As shown in the preceding screenshot, to delete an element from a particular position of the array, we need to use the keyword delete, followed by the position of the element in the array.

However, remember, deleting an element in the array using delete will leave an empty space in the array. It will not make the elements of the array shift their positions to cover up the empty undefined space in the array.

# [shift and unshift](#toc.xhtml_s69a)

Previously, we learned that push and pop will remove elements from the end of the array. In this section, we will learn adding and removing elements from the beginning of the array without leaving an empty space at the start.

The advantage of push and pop was that since it operates at the end of the array, it would neither replace an element, nor would it leave an ugly gaping hole in our array. Imagine if you want to add an element at the beginning of the array. As shown in the following screenshot, you might use cars[0] to try to add a new element to the array. However, it will only replace the element at the first position of the array. Similarly, deleting the first element of the array will remove the element 'Jaguar' from the first position. In an ideal scenario, if we delete an element from the array, we would expect the size of the array to reduce by 1, and we would also expect the elements of the array to shift around to cover the empty space. But, as we have all seen in the section earlier, that’s not how delete works.

![](images/Figure-4.9.jpg)

**Figure 4.9:** Adding and removing the first element of the array.

To overcome this problem, when dealing with the first element of the array, JavaScript introduced the methods shift and unshift. Similar to push and pop, shift and unshift removes and adds elements to the array, albeit in the first position or at the beginning of the array.

As shown in the following screenshot, to use shift, we only need to call the method shift. JavaScript automatically deletes the first element of the array and "*shifts*" the rest of the element one position before their original position. Printing the method shift will display the element that has just been removed. Similarly, to "*unshift*" the array, we will need to provide an element which will be added to the beginning of the array. When we use unshift, JavaScript automatically asks the rest of the element to shift one position, and adds the new element at the now-empty first position of the array. Printing the method unshift will return the length of the array.

![](images/Figure-4.10.jpg)

**Figure 4.10:** Adding and removing the first element of the array.

You can picture this visually as the following:

![](images/Figure-4.11.jpg)

**Figure 4.11:** Picturising shift method. Unshift will work in the reverse direction.

# [splice and slice](#toc.xhtml_s70a)

In the previous sections, we have looked at different ways of adding and removing elements. However, they all end up leaving empty undefined spaces in the array. JavaScript, therefore, introduced two methods to add or remove elements from any position in the array. Let’s begin by understanding the **`splice()`** method.

# [Splicing an array](#toc.xhtml_s71a)

The **`splice()`** method takes multiple arguments. The first argument requests a position index inside the array where new elements need to be added; the second argument defines how many elements should be removed; the rest of the arguments define the new elements to be added. Let’s understand this with an example.

![](images/Figure-4.12.jpg)

**Figure 4.12:** Adding elements to an array using splice without removing any elements.

Code explanation: In the preceding screenshot, we call the splice method by providing position index 1 as the first argument. It means JavaScript will add new elements at the position index 1\. The second argument of the splice method is 0\. It means, we do not want to remove any elements. Finally, the rest of the parameters are the new elements to be added. As a result, the final output is that the rest of the parameters – Jaguar and Rolls Royce, are added from the first position of the array cars without removing any values.

Now, let’s look at an alternate version of the code example, as shown in *[figure 4.12](#c04.xhtml_fig4_12)*. In the following code example, as shown in *[figure 4.13](#c04.xhtml_fig4_13)*, instead of passing 0 as the second argument, we pass 2\. Since the second argument denotes the number of elements that needs to be removed, we remove the next two elements in the array, which are Audi and Mercedes. Now, we have provided two more values after the second argument, so these two arguments, Jaguar and Rolls Royce, will be added starting from position 1\. Thus, we achieved replacement.

![](images/Figure-4.13.jpg)

**Figure 4.13:** Replacing elements using splice.

# [Slicing an array](#toc.xhtml_s72a)

The slice method is similar to the splice method, albeit with two major differences, which are as follows:

*   It accepts only two arguments – a start position and an optional end position.
*   It does not affect the original array. It creates a new array.

Let’s understand the slice method with the following example:

![](images/Figure-4.14.jpg)

**Figure 4.14:** Slicing an array

In the preceding screenshot, we have used two variants of the slice method.

In the first method, we only provide the first argument, which is the position at which the slicing should begin. When the slice method receives only one argument, it copies the original array cars from the position specified in the first argument till the end of the array to a new array. Therefore, as you can see in *[figure 4.14](#c04.xhtml_fig4_14)*, the **`updatedCars`** array starts from Audi till the last element Rolls Royce.

In the second method, we provide two values, 1 and 3\. In this case, the slicing of the array cars begins at index position 1 and stops before the index position 3\. Therefore, two elements are copied to the new array, **`updatedCars2`**.

**Note:** The splice method affects the original array. It means that the original array will be changed when splice method is called on it. However, the slice method does not affect the original array. In fact, a new array is created when you apply slice to the original array.

# [concat](#toc.xhtml_s73a)

When you want to merge two or more arrays, you use the **`concat`** method of JavaScript arrays. As shown in *[figure 4.14](#c04.xhtml_fig4_14)*, to use the **`concat`** method, we first need to give the root array in which the other arrays will be merged. In *[figure 4.15](#c04.xhtml_fig4_15)*, we use the array **`comfyCars`** as the root array. On the root array, you call the **`concat`** method and supply the arrays (in order) that you want to merge into the root array in the parentheses. In *[figure 4.15](#c04.xhtml_fig4_15)*, we have supplied the arrays **`vipCars`** and **`luxuryCars`** in the parentheses. The result is a new array with all the values supplied in the three arrays.

As you can see in the following screenshot, the **`concat`** method does not check for duplicate values. It does a simple merging of the arrays:

![](images/Figure-4.15.jpg)

**Figure 4.15:** Using the concat method on the arrays.

# [toString](#toc.xhtml_s74a)

If you want to convert an array into a string, there are two ways of doing that. In the first method, you simply call the method **`toString`** on the array you want to convert to a string. It will convert the array into a comma-separated string, as shown in the following screenshot:

![](images/Figure-4.16.jpg)

**Figure 4.16:** Using the toString method.

# [join](#toc.xhtml_s75a)

In the previous method, the array is converted into a string with a default comma separator between the values. In the join method, you can provide a separator for your string. As you can see in the following screenshot, we have used the separator '-' to separate the values of an array.

![](images/Figure-4.17.jpg)

**Figure 4.17:** Using the join method.

# [Conclusion](#toc.xhtml_s76a)

In this chapter, we’ve learnt a great deal about arrays. We had a detailed look at the concept of arrays. We learnt about the scenarios where we need to use arrays, how to use arrays, and more importantly, how to use some of the remarkable properties of arrays.

In the next chapter, we will take a look at another JavaScript datatype called *Objects*. Like arrays, objects are also used for strong multiple values.

# [Points to remember](#toc.xhtml_s77a)

*   Arrays are used for storing multiple related values.
*   You can define an array by specifying values inside square bracket notations.
*   When you try to access a position of an array which exceeds the length of an array, you will get undefined.
*   Arrays are ordered collection and every element stored inside an array is given an indexed position.
*   Arrays start with the position index 0.

# [Multiple choice questions](#toc.xhtml_s78a)

1.  **The slice method of an array does not affect the original array – True or False?**
    1.  True
    2.  False
2.  **If you supply only the first two arguments as non-zero integer values in the splice method, what will happen?**
    1.  The splice method will not work.
    2.  The elements will not be removed.
    3.  The elements will only be removed, and no new elements will be added.
    4.  Splice method takes only one value.

# [Answers](#toc.xhtml_s79a)

1.  **a**
2.  **c**

# [CHAPTER 5](#toc.xhtml_c05)

# [Objects](#toc.xhtml_c05)

In this chapter, we will learn one of the most fundamental concepts of JavaScript – *objects*. Across the internet, almost every introduction of JavaScript will call it as a loosely based **object-oriented programming** (**OOP**) language.

In simple words, OOP considers real-life things as objects. For instance, think of a person. Almost every person will have a name, and a set of physical features like, for this example, eyes. However, these features may vary from one person to another. In JavaScript, each individual will be considered as an object, and every object of a person will possess their own private features.

Now, compare the two scenarios – dedicating an entire variable to an individual versus creating hundreds of variables describing the same individual. In every sense, the former case sounds miles better than the latter. This structuring of data by creating objects helps developers immensely in maintaining and using data across JavaScript efficiently. And in this chapter, we will learn in depth about JavaScript objects.

# [Structure](#toc.xhtml_s80a)

In this chapter, we will cover the following topics:

*   Introducing objects
*   Using objects
*   Object properties and methods
*   Object constructors
*   Object prototypes

# [Objective](#toc.xhtml_s81a)

After studying this chapter, you should be able to understand the crux of JavaScript – objects. You can create and use objects efficiently from this chapter. You will learn how to create blueprint of objects and differentiate objects from arrays.

# [Introducing Objects](#toc.xhtml_s82a)

Let’s understand objects with another example – cars:

![](images/Figure-5.1.jpg)

**Figure 5.1:** A car as an object

If you think about it deeply, almost every real-life thing possesses two characteristics. It has properties, and it has methods (behaviors). Let's take the example of the car shown in the preceding screenshot.

Every car will have several properties. A few of the properties are as follows:

*   The name of the company which manufactured the vehicle (for example, *Ford*, *Nissan*, *BMW*, and so on)
*   The make or the model of the carrier (for example, *Ford Mustang*, *Nissan GT-R*, *BMW X-4*, and so on)
*   The color of the car
*   Whether the automobile possesses a sunroof
*   Whether the vehicle is a two-seater or a four-seater automobile

Similarly, every car will have several methods, or in simple terms, behaviors, which are relative to the vehicle. For instance, a few of these methods are as follows:

*   Turning right
*   Turning left
*   Taking a reverse
*   Turning the headlights on

Every car will definitely have these set of properties and behaviors. However, the values of these properties will differ from one car to another. Similarly, the various methods will also be performed at different times by different cars.

*JavaScript emulates these properties and methods of real-life items with the help of objects.*

JavaScript objects are similar to JavaScript arrays, in the sense that they both can store multiple values. However, the notable difference between the two (apart from the syntax) is that you can give a name to every value that you store. Unlike arrays, objects are unordered collections. They don’t store indexed positions of their values.

The syntax of a JS object is to store the values in the name: value format. And the collection of these '**`name: value`**' formats will be wrapped inside curly braces.

For instance, the example of the car in the preceding screenshot can be stored in an object, as shown in the following *[code example 5.1](#c05.xhtml_co5_1)*:

1.  `var car = {`
2.  `    companyName: 'BMW',`
3.  `    model: 'X4',`
4.  `    color: 'white',`
5.  `    turnRight: function() {`
6.  *`//code for turning right`*
7.  `    },`
8.  `    applyBrakes: function() {`
9.  *`//code for applying brakes`*
10.  `    }`
11.  `}`

    **Code 5.1:** Storing car in an object

In the preceding *[code example 5.1](#c05.xhtml_co5_1)*, we are storing the various properties of a car in the name: value format. Therefore, the name of the company is stored as **`companyName: 'BMW';`** the color of the car is stored as **`color: 'white'`**, and so on. Similarly, the behaviors or the methods of the car are stored as functions. In the next section, we will look at another example of JavaScript.

# [Using objects](#toc.xhtml_s83a)

Now that we have a fair idea about JavaScript objects, let's understand how to create and use JS objects. As we learned earlier with variables and arrays, in JavaScript, we can create an object by declaring and initializing it.

# [Object definition](#toc.xhtml_s84a)

There are three distinct ways of defining (declaring + initializing) an object. These three methods are as follows:

# [An object literal](#toc.xhtml_s85a)

This is the easiest way to create a JavaScript object. An object literal is a list of **name: value** pairs inside curly braces.

1.  `var person = {`
2.  `    firstName: 'John',`
3.  `    lastName: 'Doe',`
4.  `    age: 24`
5.  `}`

    **Code 5.2:** An example of object literal

As shown in the preceding *[code example 5.2](#c05.xhtml_co5_2)*, and the *[code example 5.1](#c05.xhtml_co5_1)* shown earlier, to create a JavaScript object using an object literal, we add several '**`key: value`**' pairs, place them inside a pair of curly braces, and give the variable a name.

# [JavaScript keyword new](#toc.xhtml_s86a)

To define a JavaScript object using the keyword new, you need to create a variable, and assign it the value new **`Object()`**.

1.  `var person = new Object();`
2.  `person.firstName = 'John';`
3.  `person.lastName = 'Doe';`
4.  `person.age = 24;`

    **Code 5.3:** An example of object definition using JavaScript keyword new

As shown in the *[code example 5.3](#c05.xhtml_co5_3)*, we add the keys (names) of the objects by typing the variable name of the object followed by a dot notation and the name of the key. If you look closely at the *[code examples 5.2](#c05.xhtml_co5_2)* and *[5.3](#c05.xhtml_co5_3)*, you will observe that in the *[code example 5.2](#c05.xhtml_co5_2)*, we have used the colon notation ('*:*') for the key and values. In the *[code example 5.3](#c05.xhtml_co5_3)*, we use the equal sign ('=') for assigning values to the object.

In simple words, when you assign values to keys inside the object literal (curly braces), you use the colon notation ('*:*').

However, if you are assigning the values to the keys of the object outside the curly braces, you use the equals sign notation ('=').

**Note :** Between the two methods of creating JavaScript objects that we just explored, it is always preferable and recommended to create an object using the first method. Creating objects using the new keyword has slower execution speed, and poorer readability than the object literal.

# [Constructor](#toc.xhtml_s87a)

For the time being, let’s just think of a constructor as a blueprint to an object. We will learn more about this method in the section, Object Constructors.

# [Object properties and methods](#toc.xhtml_s88a)

In the *[code example 5.2](#c05.xhtml_co5_2)*, we have created an object person with several **key: value** pairs. As we have learnt earlier, every object can contain properties or features, and behaviours or methods. In this section, we will look at the properties and methods of an object.

# [Object properties](#toc.xhtml_s89a)

The **`key: value`** pairs in a JavaScript object are called properties of the JavaScript object. Think of the properties as a feature that describes the object. For instance, if we consider the *[code example 5.2](#c05.xhtml_co5_2)*, we have an object person with the following properties (features):

| **Property** | **Property Value** |
| firstName | John |
| lastName | Doe |
| Age | 24 |

**Table 5.1:** Properties of the object person

We can visualize these properties on an object person (with an extra property called *eyeColor*, for visual explanation), as depicted in the following screenshot:

![](images/Figure-5.2.jpg)

**Figure 5.2:** Properties of the object person

As shown in the preceding *[table 5.1](#c05.xhtml_tab5_1)* and *[figure 5.2](#c05.xhtml_fig5_2)*, the person’s first name is basically a feature or a property of that person. Its value is John. Similarly, the person depicted in *[figure 5.2](#c05.xhtml_fig5_2)* and *[table 5.1](#c05.xhtml_tab5_1)* has a few more properties, like the last name, age, and eye color.

# [Accessing Object Properties](#toc.xhtml_s90a)

We can access the properties of an object in the following two ways:

# [Dot notation](#toc.xhtml_s91a)

As shown in *[code example 5.4](#c05.xhtml_co5_4)*, to access the property **`firstName`** of the object person, shown in *[code example 5.2](#c05.xhtml_co5_2)*, we write the name of the object, followed by a dot ('.') and the name of the property (key) that we want to access.

1.  `person.firstName` *`//John`*

    **Code 5.4:** Accessing objects using dot notation

# [Square bracket notation](#toc.xhtml_s92a)

The second method to access the property of an object is the square bracket notation. In this method, as shown in the *[code example 5.5](#c05.xhtml_co5_5)*, we write the name of the object, followed by the square brackets ('[]'). Inside the square brackets, we write the name of the property (key) that we want to access within single or double quotes.

1.  `person["firstName"];` *`//John`*

    **Code 5.5:** Accessing objects using square bracket notation

We use quotes for the key name because it's not a variable that has been created by us. If we had created a variable called **`firstName`** that has the string **`firstName`**, then we could add the key name without the quotes.

1.  `var firstName = "firstName";`
2.  `person[firstName];` *`//John`*

    **Code 5.6:** Accessing objects using square bracket notation and a variable

# [Changing object properties](#toc.xhtml_s93a)

Similarly, if you want to change the property of an object, you can access the property name using the preceding methods, and set a new value using the equal ('=') sign, as shown in the following *[code example 5.7](#c05.xhtml_co5_7)*:

1.  `console.log("Before changing the value of the firstname:  ", person.firstName);    `*`//John`*
2.  `person["firstName"] = "Jane";`
3.  `console.log("Before changing the value of the firstname:  ", person.firstName);    `*`//Jane`*

    **Code 5.7:** Changing the value of a key inside the object

# [Displaying object properties](#toc.xhtml_s94a)

If we try to display an object on the HTML DOM, it will print **`[object Object]`**, which is obviously not desirable.

![](images/Figure-5.3.jpg)

**Figure 5.3:** Displaying object on HTML shows [object Object]

To print an object, you can follow one of the following methods.

# [Display object properties by name](#toc.xhtml_s95a)

To display an object property by name, you can simply write the object name followed by a dot or a square bracket notation and the key name. This will display the object property’s value on the HTML.

![](images/Figure-5.4.jpg)

**Figure 5.4:** Using property names to display an object.

**Display object by looping through the properties:**

An alternate method to print an object is to loop through the entire object and print the values one by one. As shown in the following screenshot, you can use a special type of for loop to access every property of an object. This for loop is called as a for…in loop. The for…in loop will iterate through the entire object one by one. We need to provide a variable, which will store the key of the property accessed during a particular iteration.

![](images/Figure-5.5.jpg)

**Figure 5.5:** Displaying object using for…in loop

# [Using Object.values()](#toc.xhtml_s96a)

The method **`Object.values()`** returns all the values of the object passed inside the parentheses in the form of an array. As shown in the following screenshot, you can then use this array to print the values on HTML.

![](images/Figure-5.6.jpg)

**Figure 5.6:** Displaying object using Object.values()

# [Object methods](#toc.xhtml_s97a)

We've seen that a JavaScript object can store values of several data types, like strings, numbers, boolean, and so on. In JavaScript, objects can also store functions. As we have seen in the chapter on Functions earlier, functions stored inside an object are called *methods*.

1.  `var person = {`
2.  `    firstName: 'John',`
3.  `    lastName: 'Doe',`
4.  `    age: 24,`
5.  `    fullName: function() {`
6.  `        return this.firstName + "  " + this.lastName`
7.  `    }`
8.  `}`

    **Code 5.8:** Changing the value of a key inside the object

As shown in the preceding *[code example 5.8](#c05.xhtml_co5_8)*, we have added a key **`fullName`** inside the object person. This key **`fullName`** contains a function, which returns a string concatenation of the key **`firstName`** and the key **`lastName`** of the object person.

# [The 'this' keyword](#toc.xhtml_s98a)

In a JavaScript function, the **`this`** keyword refers to the owner of the function. In the preceding *[code example 5.8](#c05.xhtml_co5_8)*, the owner of the function inside **`fullName`** is the object **`person`**. Therefore, inside the function of **`fullName`**, this refers to the object **`person`**, and **`this.firstName`** will refer to the key **`firstName`** inside the object person.

To access a method inside an object, you have to type the name of the object, followed by the dot or the square bracket notation, and a pair of parentheses '()'.

![](images/Figure-5.7.jpg)

**Figure 5.7:** Calling an object method

As shown in the preceding screenshot, if you forget to add the pair of parentheses, it will simply print the function definition of the method. Only after you add the parentheses, you will be able to call the function.

# [Objects versus Primitive values](#toc.xhtml_s99a)

A primitive value in JavaScript is a value that does not have any properties or methods. In JavaScript, we have the following five data types of primitive values:

*   string
*   number
*   boolean
*   null
*   undefined

If you observe the primitive values closely, you will realise that the primitive values are immutable, that is, the values cannot be changed.

1.  `var name = 'John Doe';`

    **Code 5.9:** A primitive value of string

In the preceding *[code example 5.9](#c05.xhtml_co5_9)*, we can set a different value to the variable name, but we cannot change the value of the string **`John Doe`** itself.

Objects, on the other end, are mutable. In the preceding *[code example 5.7](#c05.xhtml_co5_7)*, we have seen that we can change the value of a property inside an object. By default, it means that the value of the object changes.

Another major difference between the primitive values like strings, booleans, and so on, and non-primitive values, like objects and arrays, is that primitive values copy by value, and non-primitive values copy by reference. Let’s understand the difference between the two.

# [Copy by value](#toc.xhtml_s100a)

To understand the concept of *copy by value*, let’s consider the following example:

1.  `var number1 = 50;`

    **Code 5.10:** Setting the value of variable number1

In the *[code example 5.10](#c05.xhtml_co5_10)*, we set the value of the variable number1 as 50\. Behind-the-scenes, a space is reserved in the JavaScript memory by the name number1 and the value 50 is stored inside that space.

![](images/Figure-5.8.jpg)

**Figure 5.8:** Setting the value of the variable in the JavaScript memory.

As shown in the preceding screenshot, a fictional address by the number 001 in the JavaScript memory is reserved for the variable number1, and its value 50 is stored inside the address 001.

Now, in the *[code example 5.11](#c05.xhtml_co5_11)*, we create another variable number2 and set the value of the number2 as the variable number1.

1.  `var number2 = number1;`

    **Code 5.11:** Setting the value of variable number2 as number1

So, what do you think will be the value of the new variable number2?

When we execute the *[code example 5.11](#c05.xhtml_co5_11)*, JavaScript copies the value stored inside the variable number1\. The value of the variable number1, 50, is stored in the memory address 001\. JavaScript copies this value and assigns it to the variable number2\. As shown in *[figure 5.8](#c05.xhtml_fig5_8)*, JavaScript reserves another space in the memory for the new variable number2\. This space is denoted by the fictional address 002, as shown in the following screenshot. Now, JavaScript places the copied value 50 in the memory space reserved for the variable number2\. Therefore, the value 50 is stored in 002.

![](images/Figure-5.9.jpg)

**Figure 5.9:** Setting the value of the variable number2 in the JavaScript memory

Now, if we print the values of the variables number1 and number2, we will get the following:

![](images/Figure-5.10.jpg)

**Figure 5.10:** Displaying the values of the variables number1 and number2

Fairly simple, right?

Now, what if we change the value of the variable number1 to 25? What will be the output of the line numbers 2 and 3 in the *[code example 5.12](#c05.xhtml_co5_12)*?

1.  `number1 = 25;`
2.  `console.log("Number1:  ", number1);`
3.  `console.log("Number2:  ", number2);`

    **Code 5.12:** Changing the value of the variable number1

When we execute the *[code example 5.12](#c05.xhtml_co5_12)*, the output looks like the following:

![](images/Figure-5.11.jpg)

**Figure 5.11:** Displaying the values of the variables number1 and number2.

So what exactly happened here? If we have changed the value of the variable number1 to 25, shouldn’t the value of number2 also change to 25?

Let’s try to understand why the value of the variable number2 is still 50.

When JavaScript parses the line number 1 of the *coding example 5.12*, it basically changes the value stored inside the memory address 001 (where the variable number1 is stored) to 25\. Now, since the code has requested the value of the variable number1 to be changed, JavaScript will not touch the value stored in the address 002, where the variable number2 is stored. Therefore, the value of variable number1 changes to 25, while the value of the variable number2 stored in the address 002 remains 50.

![](images/Figure-5.12.jpg)

**Figure 5.12:** The values of the variables number1 and number2 after the value change.

Based on what we have learnt here, we can conclude that all the primitive values follow the ideology of '*copy by value*'.

# [Copy by reference](#toc.xhtml_s101a)

Let’s understand the concept of *copy by reference* with an example as well.

1.  `var person1 = {`
2.  `     name: 'Mark Zuckerberg',`
3.  `     age: 36,`
4.  `    nationality: 'American'`
5.  `};`

7.  `var person2 = person1;`
8.  `console.log("Person1:   ", person1);`
9.  `console.log("Person2:   ", person2);`

    **Code 5.13:** Creating two objects

In the preceding *[code example 5.13](#c05.xhtml_co5_13)*, we declare a variable **`person1`** and initialize it with an object. Next, we create another variable **`person2`** and pass the variable **`person1`** as its value.

What do you think will be the output of the lines 8 and 9 of the *[code example 5.13](#c05.xhtml_co5_13)*?

![](images/Figure-5.13.jpg)

**Figure 5.13:** The values of the variables person1 and person2

The answer, as shown in the preceding screenshot, is pretty obvious. Both the variables **`person1`** and **`person2`** will display the exact same value.

Now, what if we change the value of the key name in the object **`person1`**?

1.  `person1.name = 'Elon Musk';`
2.  `console.log("Person1:   ", person1);`
3.  `console.log("Person2:   ", person2);`

    **Code 5.14:** Changing the value of the name key in person1

When we execute the preceding *[code example 5.14](#c05.xhtml_co5_14)*, we get the following result:

![](images/Figure-5.14.jpg)

**Figure 5.14:** The values of the variables person1 and person2 after changing the key

As we can see in the preceding screenshot, the key name of both the objects, **`person1`** and **`person2`** have changed their respective value to Elon Musk. Now, why did this happen?

Let’s understand the preceding example using the memory reference. When we execute the *[code example 5.13](#c05.xhtml_co5_13)*, a memory in the space with the fictional address 006 is reserved for the variable person1\. The entire value of the object person1 is stored inside this memory 006.

When we execute the line number 6 in the *[code example 5.13](#c05.xhtml_co5_13)*, a new address 007 in the JavaScript memory is reserved for the variable **`person2`**. However, the value of the object person1 stored inside the address 006 is *not* copied inside the address of the variable **`person2`** – 007. Instead, the address or the reference of the variable person1 is stored inside 007.

![](images/Figure-5.15.jpg)

**Figure 5.15:** The person2 variable stores the reference of the variable person1

Because of the preceding stated reason, when the value inside 006 changes, the variable **`person1`** definitely shows the new change. However, since the reference of the object **`person1`** (006) is stored inside the memory space of the variable **`person2`** (007), the variable **`person2`** also shows the same changed value as **`person1`**.

![](images/Figure-5.16.jpg)

**Figure 5.16:** The person2 variable reflects the change of the variable person1

**As we have seen in the preceding examples, arrays and objects follow the ideology of '*copy by reference*'.**

# [Object Constructors](#toc.xhtml_s102a)

In the previous examples, we have created a separate object for every individual. Let’s consider a scenario where we have to create objects for a family of ten. All the family members will have the same properties – *first name, last name, age, and color of the eyes*.

Given what we have learned so far, we would have to create 10 separate objects, each having 6 lines of code with several characters for every property, correct?

Instead, we can create a blueprint function for our object. This blueprint will contain all the properties needed for our object. Calling this blueprint function will create objects on-the-fly. This could save us from typing a lot of lines, and at the same time, it can improve the execution and the loading speed of our web page.

This blueprint of an object is called as an *object constructor*. Let’s understand constructors with an example:

![](images/Figure-5.17.jpg)

**Figure 5.17:** An example of object constructor

In the preceding screenshot, we have created a function **`Person`** which takes in the arguments – first, last, age, and color. Earlier in the chapter, we learned that the keyword **this** refers to the owner of a property. In the preceding example, we use the keyword **this** to assign properties to the parent function **`Person`**. Using the values received in the arguments, we define four properties of the function **`Person`**. Since we are creating properties, we are essentially creating an object with the help of the properties.

In the subsequent lines, we call this function six times, thereby creating six different instances of the function. Since we use the keyword new, it creates six different objects with the properties assigned to the function.

**However, you cannot add new properties or methods to an object constructor in the same way you add properties or methods to an object.**

As shown in the following screenshot, adding the nationality to the **`Person`** object constructor does not work.

![](images/Figure-5.18.jpg)

**Figure 5.18:** Adding property to a constructor does not work

If you want to add a new property to the object constructor, you need to add it to the object construction definition itself.

# [Object Prototypes](#toc.xhtml_s103a)

In the previous section, we learned how to create an object constructor. We also learned that we cannot add a new property or a new method to the object constructor. The keyword prototype helps us in adding new properties or new methods to the object constructor. Let’s understand prototypes with an example:

![](images/Figure-5.19.jpg)

**Figure 5.19:** Adding property to a constructor using prototype works

As shown in the preceding sreenshot, adding a property to the constructor using the keyword **prototype** works. Every object created using the object constructor **`Person`** will now have the property nationality set to '**`French`**'.

# [Conclusion](#toc.xhtml_s104a)

Objects form the crux of JavaScript. JavaScript objects store multiple values. Unlike arrays, objects don’t store indexed positions of their values. In objects, values are stored in the form of **`name: value`** pairs. You can also store functions inside objects. In real-life development using JavaScript, objects are used extensively.

In the next chapter, we will be exploring the changes brought about by the most popular version of JavaScript – ES6\. This will mark our ascent toward Advanced JavaScript Development.

# [Points to remember](#toc.xhtml_s105a)

*   There are multiple ways of creating objects, but the most efficient way of defining an object is by using *object literals*.
*   Objects can have **`name: value`** pairs called *properties*, and *functions* called as *methods*.
*   In JavaScript function definition, the '**`this`**' keyword refers to the owner of the function.
*   JavaScript objects work on the principle of copy by reference. It means that copying an object copies the reference of the object and not the value of the object.
*   When you need to create multiple objects having the same properties, you can use an object constructor. However, you cannot add new properties or new methods to an object constructor. You need to use the keyword prototype to add new properties and new methods to the object.

# [Multiple choice questions](#toc.xhtml_s106a)

1.  **`Object.values()`** **returns all the values of an object in the form of a string – True or False?**
    1.  True
    2.  False
2.  **Objects follow the principle of copy by __________.**
    1.  reference
    2.  value

# [Answers](#toc.xhtml_s107a)

1.  **b**
2.  **a**

# [CHAPTER 6](#toc.xhtml_c06)

# [ES6](#toc.xhtml_c06)

Through its brief history, JavaScript has seen several versions and numerous updates. However, one of the most significant updates arrived in 2015\. This update was called *ECMAScript2015* or, as it is more popularly known, ES6\. This update turned up with some brilliant new features and methods. In fact, at the time of writing, several front-end libraries, which power applications like Facebook, Instagram, Twitter, etc, strongly recommend learning in-depth about ES6.

In this chapter, we will explore a few of the most important concepts introduced in ES6\. If you complete this chapter by practicing the codes given, you should reach a stage where you can begin learning front-end libraries like React and Angular.

# [Structure](#toc.xhtml_s108a)

In this chapter, we will cover the following topics:

*   Introduction to ES6
*   JavaScript hoisting
*   New ES6 syntax
*   Arrow functions
*   New array methods – map, filter, and reduce
*   Array and Object Destructuring
*   ES6 modules

# [Objective](#toc.xhtml_s109a)

After studying this chapter, you should be able to apply the latest and the most advanced methods in JavaScript to your application. You will learn about modules, which forms the basis of libraries like Angular and React and write optimised JavaScript code.

# [Introduction to ES6](#toc.xhtml_s110a)

Up until 2015, JavaScript was functioning primarily on version 3, released in 1999, and version 5, released in 2009\. For a considerably long time, no new updates were added to the scripting language of web development.

Finally, in 2015, the sixth edition of JavaScript was released, and it was titled ECMAScript2015\. For the sake of simplicity, this version became popular as ES6.

ES6 brought for a variety of new features and methods. A few of them are listed as follows:

*   New keywords for creating variables – **`Let`** and **`Const`**.
*   Object extensions like Bind, Call, and Apply.
*   Arrow functions.
*   JavaScript hoisting.
*   Advanced operators like ternary operators and spread operators.
*   Advanced array methods like map, filter, and reduce.
*   Template literals.
*   Module imports and exports.

In the next few sections, we will be learning the different preceding listed concepts.

# [JavaScript hoisting](#toc.xhtml_s111a)

As per the official documents of MDN Web Docs (it is pretty much like the Holy Bible for the web developers), JavaScript Hoisting was officially specified in the version ECMAScript2015, aka, ES6.

In layman terms, JavaScript hoisting is the default behavior of JavaScript to move declarations to the top. Let’s understand this with an example.

1.  `number = 1;`
2.  `console.log(number);`
3.  `var number;`

    **Code 6.1:** An example of JavaScript Hoisting

Traditionally, we declare the JavaScript variable first and then initialise it. However, in the preceding *[code example 6.1](#c06.xhtml_co6_1)*, we are initializing the variable before declaring it. Based on what we have learnt so far, what do you think will be the output of line number 2?

![](images/Figure-6.1.jpg)

**Figure 6.1:** Output of the [code example 6.1](#c06.xhtml_co6_1)

As you can see in the preceding screenshot, the output of the line number 2 in the *[code example 6.1](#c06.xhtml_co6_1)* is 1 and it did not throw an error. Why did this happen?

In technical terms, JavaScript puts the variable declarations and the function declarations into the memory during compile phase. In layman terms, no matter where you have declared your variable, it can be visualised as moving to the top of the code. Therefore, all the variable declarations in your code are executed first and then the JavaScript continues its normal execution line-by-line.

Therefore, in the *[code example 6.1](#c06.xhtml_co6_1)*, the declaration of the variable number on line number 3 happens before the first line is executed. Hence, when JavaScript executes line number 1, it already has an empty declared variable called number. JavaScript then initialises it with the value 1, as shown on the line number 1 of the *[code example 6.1](#c06.xhtml_co6_1)*. Since it has been both, declared and initialised, the execution of the line number 2 of the *[code example 6.1](#c06.xhtml_co6_1)* results in the value 1\. Imagine this process as the task of filling water inside a container. To fill water inside a container (to add a value to a variable), it is obvious that we need to make sure that the container exists before we try to fill it with water (the variable exists before we add a value)

![](images/Figure-6.2.jpg)

**Figure 6.2:** JavaScript Hoisting as an example of container and water

Let’s understand the concept of hoisting with a few more examples:

![](images/Figure-6.3.jpg)

**Figure 6.3:** Not defined vs undefined in JavaScript Hoisting

So what on earth happened in the preceding screenshot? Let’s understand it one line at a time.

**Code Explanation:**

Let’s begin by understanding what happened to the variable number2:

Based on the prior explanation and the preceding screenshot, we understand that the variable number2 was declared and initialised after the statement to print it using **`console.log`**. However, since JavaScript moves all the declarations to the top, when the line number 3 (**`console.log("number2: ", number2);`**) is executed, JavaScript already has the declared variable number2.

So, then why did it not print 50? Because hoisting only moves declarations to the top, it does not move the initialisations to the top. Imagine this as placing the container (declaration) before you fill water (the value 50) inside it. Therefore, when the line number 3 is executed, JavaScript holds an empty declaration of the variable number2 (or in the other sense, we have the container already placed but we have not yet filled the water inside it). Hence, it prints number2 as undefined.

Now, let’s understand what happened to the variable number1:

Unlike the *[code example 6.1](#c06.xhtml_co6_1)*, in *[figure 6.3](#c06.xhtml_fig6_3)*, we initialise the variable number1 with the value 25, but never declare it, even after printing it on the console.

So, in that case, since the variable number1 is not declared and we are attempting to print it, it should throw an error, right? The answer is no. Call it intelligence, but since you are initialising the variable number1 with the value 25, JavaScript presumes that you want to declare it. Therefore, it automatically declares the variable number1, since it has been initialised. Consider the abstract example of the container and the water that we imagined earlier. If you tell someone that you are filling water inside a container, they will already presume that you do have a container.

So, why do we need to declare a variable at all? Why do we need to write **`var`** before we give it a value? The answer to these questions is that the keyword **`var`** helps us in defining the scope or the usability of the variable. In ES6, JavaScript introduces two new ways of declaring a variable, which will completely change the way we look at scopes. In the next few sections, we will understand the two new keywords (**`let`** and **`const`**) for declaring the variables, and that will answer the question here.

Finally, what happens to the variable number3?

If we look at our code, at no point in time do we initialise or declare the variable number3\. It means that the variable number3 simply does not exist. In the line number 4, we are trying to print the value of something which does not exist. In every sense, it will throw an error saying that the variable does not exist or in JavaScript terms, it will say the variable number3 is not defined.

Like variables, JavaScript also moves function declarations to the top. Let’s understand this with examples:

![](images/Figure-6.4.jpg)

**Figure 6.4:** JavaScript Hoisting with functions

As shown in the preceding screenshot, even though we call the function add before it is declared and initialised, JavaScript still shows the output of the function execution. As we learnt earlier, JavaScript hoisting moves the function declaration to the top. In this case, we are also initialising the function by typing the code that needs to be executed when the function is called. Hence, we are initialising and declaring the code together.

Now, let’s take a look at some erroneous coding with JavaScript hoisting and functions:

![](images/Figure-6.5.jpg)

**Figure 6.5:** JavaScript Hoisting for functions with error

In the preceding screenshot, we have declared a variable add. Even if this variable is placed after the line number 2, it is not initialised. Hence, it will have no value. At this point, it is not even a function. However, in line number 2, we consider the variable add to be a function and call it with the arguments 1 and 6\. To state the obvious, it will throw an error stating that the variable add is not a function.

Now, let’s take a look at one final example of functions and JavaScript hoisting:

![](images/Figure-6.6.jpg)

**Figure 6.6:** JavaScript Hoisting for anonymous functions

In the preceding screenshot, we have used an anonymous function. We initialise the variable **`add`** with the anonymous function. However, as per JavaScript hoisting, only the variable declaration moves to the top. At the point of calling the anonymous function stored in the variable add with arguments 1 and 6, it is only an empty undefined variable. Hence, we get the error stating that add is not a function.

# [New ES6 Syntax](#toc.xhtml_s112a)

ES6 introduced several new syntaxes for JavaScript developers. These new syntaxes amplify the speed of code execution and optimise the JavaScript code to a great extent. Let’s understand these new syntaxes one by one:

# [Let and const](#toc.xhtml_s113a)

As we have learnt earlier in *[Chapter 3: Functions](#c03.xhtml)*, before the introduction of ES6, JavaScript had two types of scope: *global scope* and *local scope*. Variables declared with the JavaScript keyword **`var`** will have a local scope inside a function. Similarly, the variables declared with the JavaScript keyword **`var`** will have a global scope outside the functions (that is, the variables declared outside the function will be accessible by everyone).

ES6 introduces a new level of scope called block-level scope. You can create a block-level scope in JavaScript using the keywords **`let`** and **`const`**. The word block in the term block-level scope means a block of code. This block could be a block of code inside a pair of curly braces, a block of code defined inside a function, or a block of code in the entire script. The most important thing to understand about these blocks is that each block is a separate entity and has its own private space. Let’s understand what block-level scope is, and how to create it.

# [let](#toc.xhtml_s114a)

In JavaScript, if you declare a variable with the keyword **`var`** inside curly braces and access the variable outside, you will be able to access the variable.

![](images/Figure-6.7.jpg)

**Figure 6.7:** Scope by keyword var

As shown in the preceding screenshot, we have declared a variable number and initialised it with a value 20 inside curly braces. When we try to access the variable number outside the curly braces and AFTER the variable definition, we are able to access the value, as shown in the output.

In an ideal scenario, the variables declared inside curly braces should NOT be accessible outside the braces. Let’s consider a practical example for this scenario:

![](images/Figure-6.8.jpg)

**Figure 6.8:** Why var can be complicated!

In the preceding screenshot, we have defined a variable number with the value 25 on line number 1\. After that, we have opened curly braces and redefined the variable number with the value 50.

As we learnt earlier, the curly braces resemble a block. The values inside this block should ideally remain accessible only inside the block. Similarly, since the code outside the curly braces forms a separate block, we would imagine the values declared outside the curly braces (block) to retain their respective values outside. However, as we can see in *[figure 6.8](#c06.xhtml_fig6_8)*, if a user has redefined a variable with another value inside the curly braces, the old value gets completely replaced everywhere after the redeclaration.

Now, imagine a script of approximately 1000 lines of code. It’s practically impossible to remember the names of all the variables used in a script. If a developer accidentally uses the same variable name to define a new value, there is every chance that the code might crash.

![](images/Figure-6.9.jpg)

**Figure 6.9:** Using same variable name with var changes the value

Imagine the user has defined the variable title for storing the name of the user. However, somewhere in the middle of the script, the developer also uses the same variable name title for storing the name of the user’s car. Now, even though the developer must have planned to initially reserve the variable name title for storing the name of the user, it will show the name of the user’s car wherever it is used after the redefinition.

To solve such erroneous coding, ES6 introduced two new JavaScript keywords to create variables – **`let`** and **`const`**. The keyword let has the following four features:

*   **Variables declared inside a block cannot be accessed outside the block**

    In analogy with *[figure 6.7](#c06.xhtml_fig6_7)* that we saw earlier, let’s understand the same example by using the keyword let instead:

    ![](images/Figure-6.10.jpg)

    **Figure 6.10:** Variables created with let keyword is not accessed outside

    As shown in the preceding screenshot, the variable `number` created with the keyword `let` inside the curly braces (a block of code) cannot be accessed outside the curly braces.

*   **Variables declared outside the block cannot be accessed inside the block**

    Similarly, in analogy with *[figure 6.8](#c06.xhtml_fig6_8)*, we will use the same example with the keyword let.

    As shown in the following screenshot, you cannot access a variable inside the curly braces (block) if it is declared outside the block and a new variable with the same name is not redefined inside the block. Since the code outside and the code inside the curly braces form different blocks, value inside one block cannot be accessed inside another block.

    ![](images/Figure-6.11.jpg)

    **Figure 6.11:** Variables declared with let outside cannot be accessed inside

*   **Variables retain their values in their block**

    In conjunction with the previous bullet point, every block will retain their own value. As you can see in the following screenshot, the variable number declared outside the curly braces will retain its value after the curly braces end. Similarly, the value inside the curly braces will not impact the value outside.

    ![](images/Figure-6.12.jpg)

    **Figure 6.12:** Each block has its own value

*   **Variables with the same name cannot be redeclared inside a block**

    Finally, one of the most important features of the keyword let is that it does not let you create variables with the same name inside a block. However, you can create variables with the same name in another block. As shown in the following screenshot, you are allowed to redeclare the variable number inside another block, as shown on the line number 4 in *[figure 6.13](#c06.xhtml_fig6_13)*. However, if you try to redeclare the variable number after the curly braces, you are not allowed to do that. It’s not allowed because the code outside the curly braces forms a different block, and the variable number is already defined on the line number 1 in that block.

    ![](images/Figure-6.13.jpg)

    **Figure 6.13:** Variables cannot be redeclared inside the same block

Thus, the keyword let allows you to create a block-level scope for variables. This would solve the problem we encountered in *[figure 6.9](#c06.xhtml_fig6_9)*. Why don’t you test the script we saw in *[figure 6.9](#c06.xhtml_fig6_9)* by using the keyword let instead of **`var`**, on your own?

# [const](#toc.xhtml_s115a)

The variables declared with the keyword **`const`** work in similar fashion to the variables created with the keyword **`let`**. They also follow the laws of block-level scope. However, a major difference between the two is that you cannot reassign a different value to the variables declared with const. In simple words, you create a constant value that cannot be changed.

![](images/Figure-6.14.jpg)

**Figure 6.14:** Variables cannot have new value using const

The general convention for writing constants is by writing the variable name in uppercase and separating multiple words using underscores.

A few things that we need to know about **`const`** are as follows:

*   **You cannot assign a new value to variables declared with const**

    As shown in *[figure 6.14](#c06.xhtml_fig6_14)*, you cannot assign a new value to the variables defined with **`const`**.

*   **You cannot reassign an already declared variable with const**

    Since **`const`** follows the same principle as let, you cannot redefine an already declared variable with **`const`**.

    ![](images/Figure-6.15.jpg)

    **Figure 6.15:** Variables cannot be redeclared with const

*   **It is *compulsory* to assign a value when using const**

    As shown in the following screenshot, you always need to initialise a variable declared with const. If you don’t initialise a variable when using **`const`**, it will result in an error:

    ![](images/Figure-6.16.jpg)

    **Figure 6.16:** You need to initialise a variable with const

*   **You can change the properties of objects declared using const…**

    As shown in the following screenshot, you can change the properties of an object declared with the variable const:

    ![](images/Figure-6.17.jpg)

    **Figure 6.17:** Properties of objects declared with const can be changed

*   **…but you cannot assign a new object to the same variable**

    As shown in the following screenshot, you cannot assign a new object to the variable declared with const:

    ![](images/Figure-6.18.jpg)

    **Figure 6.18:** You cannot assign a new object to the same variable using const

**Tip:** To overcome the flaw where the properties of an object declared with `const` can be changed, you can use `Object.freeze()`.

![](images/Figure-6.19.jpg)

**Figure 6.19:** Object.freeeze

As shown in the preceding screenshot, if an object has been passed as an argument inside `Object.freeze`, it will not change its value. However, remember `Object.freeze()` does not work on objects created inside an object.

# [Bind, call, and apply](#toc.xhtml_s116a)

ES6 introduces three new methods for objects – bind, call, and apply. Let’s directly delve into understanding these three methods with the help of examples:

![](images/Figure-6.20.jpg)

**Figure 6.20:** Object method returns NaN when called

In the preceding screenshot, execution of the script results in the value NaN. Any guesses why?

Let’s revisit the concept of the **`this`** keyword. We have learnt that the **`this`** keyword corresponds to the owner of the function. In the preceding case, when the object is defined, the this keyword inside the method **`getFullName`** refers to the **`person`** object. However, on the line number 9, we assign the method to the variable **`fullName`**. Since the variable **`fullName`** belongs to the global object, when the variable **`fullName`** is called, the value of this shifts to the global object. And since the global object does not have variables **`firstName`** and **`lastName`**, we get the value NaN.

To resolve this, JavaScript provides three new methods for the global object **`Object`**. Let’s understand every method one-by-one.

# [bind](#toc.xhtml_s117a)

The bind method creates a new copy of the function. It accepts a value as an argument. The bind function sets the value of the **`this`** keyword to the value provided in the argument. Building on the example we saw earlier in *[figure 6.20](#c06.xhtml_fig6_20)*, we pass the value of the object person to the bind function in the line number 9, as shown in the following screenshot:

![](images/Figure-6.21.jpg)

**Figure 6.21:** The bind method

In the preceding screenshot, we pass the object person as an argument to the bind method in the invocation of the **`getFullName`** method. The bind method creates a new copy of the original method **`getFullName`** and sets the **`this`** keyword to the person object.

# [call](#toc.xhtml_s118a)

The call method does the same thing as the bind method. However, there are three notable differences between the two methods:

*   The call method does not create a new copy of the function.
*   The call method immediately executes the function.
*   The bind method accepts arguments.

Let’s understand this with an example.

![](images/Figure-6.22.jpg)

**Figure 6.22:** The call method

If you compare *[figures 6.21](#c06.xhtml_fig6_21)* and *[6.22](#c06.xhtml_fig6_22)*, you will notice that in *[figure 6.21](#c06.xhtml_fig6_21)*, you had to invoke the function separately after applying the bind method. In *[figure 6.22](#c06.xhtml_fig6_22)*, you can notice that you don’t need to separately invoke the function. Instead, the call method, by default, calls the function. Another important thing to notice is that the call method does not create a new copy of the function. For these two reasons, the call method is used for applying methods on different objects.

In the following screenshot, you can observe another feature of the call method. In the arguments that you pass to the call method, after you pass the object required for the **`this`** keyword, you can also pass multiple comma-separated arguments to be used by the method.

![](images/Figure-6.23.jpg)

**Figure 6.23:** The call method with arguments

# [apply](#toc.xhtml_s119a)

The apply method is similar to the call method with just one difference. In the apply method, you need to pass the extra arguments as an array instead of comma-separated values.

![](images/Figure-6.24.jpg)

**Figure 6.24:** The apply method

If you compare *[figures 6.23](#c06.xhtml_fig6_23)* and *[6.24](#c06.xhtml_fig6_24)*, you will notice that the only difference is that the arguments are supplied as an array in the latter. The benefit of supplying the arguments as an array is that you will always know that there will be only two maximum arguments to be passed inside the apply method. Additionally, you can simply outsource the array creation to a variable holding an array.

# [Advanced operators](#toc.xhtml_s120a)

We have explored several JavaScript operators in *[Chapter 1: Introduction to JavaScript](#c01.xhtml)* of this book. ES6 introduced a few more operators which make coding simpler. In this section, we will look at three important features introduced by ES6 – Ternary operators, rest parameters, and spread operators.

# [Ternary operator](#toc.xhtml_s121a)

The ternary operators simplify the way we write an if…else conditional in JavaScript. Let’s try to understand the ternary operator with a simple if…else example:

1.  `let result;`
2.  `if(number%2 === 0) {`
3.  `    result = "The number is even.";`
4.  `} else {`
5.  `    result = "The number is odd.";`
6.  `}`

    **Code 6.2:** An if…else conditional in JavaScript

In the *[code example 6.2](#c06.xhtml_co6_2)*, we have introduced a simple JavaScript if…else conditional to find out whether a number is even or odd. However, as you can see in the *[code example 6.2](#c06.xhtml_co6_2)*, it takes five lines of code. Even if we cut down on white spaces, we will still be typing a lot of characters.

To simplify the if…else conditional, ES6 introduces the ternary operator. The syntax of a ternary operator is as follows:

1.  `condition ? ifTrue : ifFalse`

    **Code 6.3:** Syntax of ternary operators

As shown in the *[code example 6.3](#c06.xhtml_co6_3)*, the syntax of the ternary operator requires two symbols – a question mark '?' and a colon ':'. In a ternary operator, you need to add the condition to test before the question mark. If the result of the condition is true, then the statement or the expression after the question mark (denoted by **`ifTrue`** in the *[code example 6.3](#c06.xhtml_co6_3)*) will be executed. If the evaluation of the condition is false, the statement or the expression after the colon symbol will be executed (denoted by **`ifFalse`** in the *[code example 6.3](#c06.xhtml_co6_3)*). Let’s understand this syntax with the code shown in the *[code example 6.2](#c06.xhtml_co6_2)*:

1.  `let result = number%2 === 0 ? "The number is even" : "The number is odd";`

    **Code 6.4:** Example of ternary operator

As shown in the preceding *[code example 6.4](#c06.xhtml_co6_4)*, thanks to the ternary operator, we converted the seven lines of code in the *[code example 6.2](#c06.xhtml_co6_2)* to a single line of code in the *[code example 6.4](#c06.xhtml_co6_4)*.

Ternary operators work best when you need to return a single line of expression or a simple execution.

Let’s look at one more practical example of ternary operators:

![](images/Figure-6.25.jpg)

**Figure 6.25:** Example of ternary operator

As you can see in the preceding screenshot, the ternary operator can handle null values. If the condition evaluates to null or if the expression received in the condition is null, it automatically executes the else part (the part after the colon). In *[figure 6.25](#c06.xhtml_fig6_25)*, since the ternary operator received null in the second invocation of the function, it returns stranger.

# [Rest Parameters](#toc.xhtml_s122a)

Before we set out to explore the rest parameters, let’s reiterate over a few important terms of JavaScript functions. In JavaScript functions, the variables that you create in the parentheses during the function declaration are called as parameters and the variables or the values that you pass inside the parentheses when you call (invoke) the function are called as *arguments*. In the following screenshot, we can see the difference between parameters and arguments in a visual format:

![](images/Figure-6.26.jpg)

**Figure 6.26:** Parameters vs arguments

Now that we know the difference between parameters and arguments, let’s understand the concept of rest parameters introduced in ES6\. To understand rest parameters, let’s look at the example of the function **`add`**, shown in *[figure 6.26](#c06.xhtml_fig6_26)*.

In *[figure 6.26](#c06.xhtml_fig6_26)*, we have a simple function which adds two numbers.

*But, what if we needed a function to add three numbers?*

We will need to create a brand new function which has three parameters.

*But, what if we needed a function to add four numbers?*

We will need one more new function which has four parameters.

*What if we need a function where the number of parameters can vary? For instance, I need a function which can take any number of arguments, and it will still compute the results. I could write add(2, 3) or I could write add(4, 5, 6, 102, 12, 23), and I will get the results in both the cases.*

This can be achieved using the rest parameters. The rest parameters have a prefix of three dots. This notation allows you to introduce indefinite number of arguments in a function. These arguments will be represented as an array. As usual, let’s try to understand this with an example.

![](images/Figure-6.27.jpg)

**Figure 6.27:** Rest parameters

As you can see in the preceding screenshot, we have created a function which takes two primary arguments number1 and number2\. In the function declaration shown in the first line of *[figure 6.27](#c06.xhtml_fig6_27)*, after typing the parameters number1 and number2, we have introduced a rest parameter denoted by a prefix of three dots (…) and a variable by the name numbers. This rest parameter numbers can store unlimited parameters in the form of an array. With the help of the rest parameters, now we don’t need to create multiple new functions for different number of parameters. In fact, the user can now supply any number of arguments and our function will be able to handle all of them.

In simple words, to use our function add, a user has to provide a minimum of two arguments.

As you can see in *[figure 6.27](#c06.xhtml_fig6_27)*, if the user supplies only two arguments, as in, **`add(1, 2)`**, the rest parameter numbers will show an empty array. If the user supplies three arguments, as in, **`add(2, 3, 4)`**, we will have the array numbers with one value which is the third argument 4\. Finally, if the user supplies five arguments, as in, **`add(6, 7, 8, 9, 12)`**, we will have the array numbers of three values 8, 9, and 12.

# [Spread operators](#toc.xhtml_s123a)

ES6 introduced a new operator called the spread operator. The spread operator is also denoted by the prefix three dots (…). However, the spread operator is completely different from the rest parameters that we learnt in the last section. The most literal translation of the task done by the spread operator is to spread out the elements of an iterable object like an array.

To understand spread operators better, let’s check out the different functionalities of the spread operator:

*   **Insert an array/object in another array/object**

    The spread operator allows you to insert an array into another array initialisation. Let’s understand this with an example:

    ![](images/Figure-6.28.jpg)

    **Figure 6.28:** Inserting an array into another array initialisation

    In the preceding screenshot, we have an array of initial characters with four values on the first line. In the next line, we are creating another array by the name **`allCharacters`** where we want to add the list of characters listed in the array **`initialCharacters`** along with two new characters. To achieve this, we simply use the spread operator to insert the **`initialCharacters`** array at a particular position. As you can see in the second and the third lines of *[figure 6.28](#c06.xhtml_fig6_28)*, the spread operator will insert the entire array only at the position where you use the spread operator.

    As shown in the following screenshot, you can also insert an object into the initialisation of another object using the spread operator:

    ![](images/Figure-6.29.jpg)

    **Figure 6.29:** Inserting an object into another object initialisation

*   **Concatenate arrays/objects**

    The spread operator can also be used to concatenate two or more arrays or objects. As shown in the following screenshot, to concatenate multiple arrays, you need to insert the name of the arrays with the spread operator prefix (…), in the order you want.

    ![](images/Figure-6.30.jpg)

    **Figure 6.30:** Concatenating two arrays using the spread operator

    Similarly, you can concatenate multiple objects using the same technique of the spread operators, as shown in the following screenshot:

    ![](images/Figure-6.31.jpg)

    **Figure 6.31:** Concatenating two objects using the spread operator

*   **Copying arrays/objects**

    In the previous chapter, we had learnt that the arrays and the object follow the concept of '*copy by reference*'. As shown in the following screenshot, it basically means that when you copy an object, its value is not copied but a reference to the object is copied. Therefore, when you change any one of the object, the value of the other object also changes.

    ![](images/Figure-6.32.jpg)

    **Figure 6.32:** Objects follow the concept of copy by reference

    This could be particularly disastrous if you want to make a change to only one of the object but the value of both the objects change. Think of the example in the preceding screenshot. In a practical analogy, the objects person1 and person2 are two different individuals. If we change the age of one of the persons, it’s not correct that the age of the other person should increase. Or say, if we add the nationality of person2 as Spanish, it does not conclude that the person1 is also Spanish.

    To solve this dilemma, we can use the spread operator. When we use the spread operator to copy an object, it copies the content of the object and not its reference.

    As shown in the following screenshot, to use a spread operator to copy an object, you open a pair of curly braces. Inside the curly braces, you use the spread operator notation (…) and type the name of the object you want to copy. Similarly, if you want to copy an array, you follow the same steps, except that instead of the curly braces, you use the array notation, that is, square brackets ([]).

    ![](images/Figure-6.33.jpg)

    **Figure 6.33:** Using spread operator to copy value of an object

# [Template literals](#toc.xhtml_s124a)

So far, whenever we want to use variables in a string, we use single quotes (') or double quotes (") to create the text of the string. To insert variables in this string, we have to end the quotes and then insert the variables using the plus operator (+). This is called as a string literal.

As shown in the following *[code example 6.5](#c06.xhtml_co6_5)*, we face a lot of issues while creating string literals using quotes. From breaking the string at multiple points to using escape characters (\) to ensure the string does not crash, writing a string literal is seldom easy.

1.  `let name = "John Doe";`
2.  `let age = 27;`
3.  `let nationality = "British";`

5.  `let string = "Today's first candidate is " + name + ". He is " + age + " years old. His nationality is " + nationality + ". His favorite quote is \"If not now, then when?\"";`

    **Code 6.5:** String literals

To solve this, ES6 introduced template literals. Template literals help us to work with strings in a simpler, cleaner, and safer way. To use template literals, we wrap the string in backticks (`). Whenever we want to insert a variable in the template literal, we use a special syntax - **`${variableName}`**. Let’s understand this with an example:

1.  `let name = "John Doe";`
2.  `let age = 27;`
3.  `let nationality = "British";`

5.  ``let string = `Today's first candidate is ${name}.``
6.  `He is ${age} years old. His nationality is ${nationality}.`
7.  ``His favorite quote is "If not now, then when?"`;``

    **Code 6.6:** Template literals

As shown in the *[code example 6.6](#c06.xhtml_co6_6)*, we solve the following three problems with the help of template literals:

*   **String formatting**: We can substitute variables easily compared to adding it using the traditional string literals.
*   **HTML Escaping**: In the *[code example 6.5](#c06.xhtml_co6_5)*, since we were using double quotes, we had to use an escape character to ensure the double quote for the string is not considered as the end of the string. Template literals save us a lot of trouble here by avoiding the escaping of characters.
*   **Multi-line statements**: In the *[code example 6.5](#c06.xhtml_co6_5)*, we will need to use the escape character (\n) to enter a new line. In template literals, it is as simple as entering the text on a new line.

# [Arrow functions](#toc.xhtml_s125a)

In *[Chapter 3: Functions](#c03.xhtml)*, earlier in this book, we learned a great deal about functions. In 2015, ES6 introduced a much shorter syntax for writing the functions. This new syntax for functions are called as arrow functions. A funny name for a function, right? The arrow functions are called so because the most important syntax in an arrow function is the fat arrow notation (=>).

Arrow functions provide two significant advantages over traditional approach to writing functions:

*   Shorter syntax
*   Removes the binding of the **`this`** keyword

# [Shorter syntax](#toc.xhtml_s126a)

Let’s try to understand the arrow functions with examples:

1.  `var add = function(number1, number2) {`
2.  `    return number1 + number2;`
3.  `}`

    **Code 6.7:** Traditional method of writing the functions

As shown in the preceding *[code example 6.7](#c06.xhtml_co6_7)*, we have created an anonymous function add using the traditional method of writing functions. ES6 reduces the same function to a much shorter syntax, as shown in the following *[code example 6.8](#c06.xhtml_co6_8)*:

1.  `let add = (number1, number2) => number1 + number2;`

    **Code 6.8:** ES6 method of writing the functions

So what exactly happened here? Let’s understand it word by word:

1.  The first thing that an arrow function does is removing the dependency on the keyword function.
2.  Next, after you add the function parameters (if any), you add the fat arrow notation of ES6.
3.  Now comes the interesting part. If the function is to return some value and the code that needs to be executed is only one line, you can completely discard the curly braces and the keyword return.

As you can see in the following screenshot, the function performs in the exact same manner:

![](images/Figure-6.34.jpg)

**Figure 6.34:** The arrow function variant of [code example 6.8](#c06.xhtml_co6_8)

If your function has no parameters, you need to provide empty parentheses. If your function has only one parameter, then you can discard the parentheses as well. This is depicted in the following *[code example 6.9](#c06.xhtml_co6_9)*:

1.  ``let greeting = () => `Good morning, user!`;``
2.  ``let greeting = name => `Good morning, ${name}!`;``

4.  `greeting();     //Good morning, user!`
5.  `greeting('John');     //Good morning, John!`

    **Code 6.9:** ES6 method of writing the function with zero or one parameter

# [The this keyword in ES6 functions](#toc.xhtml_s127a)

The arrow functions change the scope of the **`this`** keyword in functions. This change makes function execution much more intuitive.

Traditionally, when we use the **`this`** keyword, it refers to the owner of the function where it is executed or the window object. In the following screenshot, we are printing two statements on the console. The first statement is printed on the very first line inside the **`getFullName`** method. The second statement is inside an anonymous function stored in the variable print. This anonymous function is a part of the **`getFullName`** method.

![](images/Figure-6.35.jpg)

**Figure 6.35:** The “this” keyword in tradtional functions

*Any idea why the inner statement is returning undefined?*

We have learned that the **`this`** keyword refers to the owner of the function in which it is used. In the case of the outer statement, the **`this`** keyword belongs to the method **`getFullName`**, and the owner of the method is the object person. Fair to say, since the person object has both the **`firstName`** and the **`lastName`** properties, we get the value of the outer statement as John Doe.

However, in the case of the inner statement, the **`this`** keyword belongs to the function inside the variable print. The owner of the anonymous function print is the method **`getFullName`** and from *[figure 6.35](#c06.xhtml_fig6_35)*, we can see that the v method does not have the **`firstName`** and the **`lastName`** properties.

The arrow function solves this complexity by removing the bindings of the **`this`** keyword. Let’s understand that with an example:

![](images/Figure-6.36.jpg)

**Figure 6.36:** The “this” keyword in arrow functions

In the preceding screenshot, we have used the arrow function for the inner statement. As we can see, the output of the inner statement now is John Doe, as well. So what happened here?

The arrow functions do not have their own **this**. So, the **`this`** value of the enclosing or the parent scope is used. In *[figure 6.36](#c06.xhtml_fig6_36)*, since the anonymous function print does not have a this keyword, it looks for the this keyword in the scope of the **`getFullName`** method. And as we have seen earlier, since the **`getFullName`** method belongs to the person object, it derives its value from there.

# [New array methods – map, filter, and reduce](#toc.xhtml_s128a)

In *[Chapter 4: Arrays](#c04.xhtml)*, earlier in this book, we learned about arrays. In that chapter, we learned that one of the ways to access every element of an array is to use a for loop. ES6 introduced three new ways to manipulate an array, which are far more simpler and effective than the for loop. We will go through each of these methods one-by-one.

# [map()](#toc.xhtml_s129a)

The **`map()`** method calls a function for every element in the array. The results of every function for every element is then populated into a new array by the **`map()`** method. The **`map()`** method does not change the original array.

Let’s understand the **`map()`** method with a simple example. If I give you an array of numbers and ask you to double the value of all the elements inside the array, how will you do it?

Of the many methods that you can employ, the best method will be the following:

1.  `var numbers = [2, 4, 6];`
2.  `var double = [];`

4.  `for(var i=0; i<numbers.length; i++) {`
5.  `    let value = numbers[i]*2;`
6.  `    double.push(value);`
7.  `}`
8.  `console.log("Double:    ", double);  //Double:    [4, 8, 12];`

    **Code 6.10:** Traditional method to double values in an array

ES6 simplifies this to a greater extent by the **`map()`** method.

1.  `let numbers = [2, 4, 6];`
2.  `let double = numbers.map(number => number * 2);`

4.  `console.log("Double:   ", double);      //Double:   [4, 8, 12]`

    **Code 6.11:** ES6 method to double values in an array

As you can see in the preceding *[code example 6.11](#c06.xhtml_co6_11)*, we have used the arrow functions in the map method. We call the map method on the array numbers. The map method passes through every element of the array one by one, performs some calculation (execution) on the element at that point, and returns the calculated (executed) value at the exact position in a new array.

In the *[code example 6.11](#c06.xhtml_co6_11)*, the variable number refers to every element in the array numbers. Going by the functionality of the arrow functions, every element of the array defined by the variable number is multiplied by two and that value is returned at the same position in a new array.

You can imagine it visually as

![](images/Figure-6.37.jpg)

**Figure 6.37:** A visual reference to the map method

**Note:** Use the map method only when you want to return an array. If you don’t intend to return any array, then *do not use* the map method. Instead, you can use the `for…of` condition or `forEach` condtion. *6*

# [filter()](#toc.xhtml_s130a)

The literal job of the **`filter()`** method is to filter out elements from an array based on a condition. Imagine if you are provided an array of numbers. If I ask you to remove only those elements which are odd numbers, how will you do it?

The **`filter()`** method provides a short and a simple syntax to filter out elements in an array. The **`filter()`** method returns a new array of the filtered elements.

1.  `let numbers = [1, 20, 21, 46, 213, 452, 615, 729, 8901];`
2.  `let even = numbers.filter(number => number%2 === 0);`

4.  `console.log("Even numbers:    ", even);    // Even numbers:  [20, 46, 452]`

    **Code 6.12:** ES6 method to filter values

As shown in the preceding *[code example 6.12](#c06.xhtml_co6_12)*, once again, we make use of the arrow functions in the filter method of ES6\. Like the map method, we call the filter method on the array numbers. The variable number refers to every single element inside the array numbers. This element is then checked against the condition shown after the fat arrow notation. If the condition is satisfied, that element is added to the new final array which will be returned. If the condition is not satisfied, that element is not added to the new final array.

# [reduce()](#toc.xhtml_s131a)

The **`reduce()`** method of ES6 reduces an array to a single value. The reduce method contains two parameters. The first parameter is an accumulator. In simple words, it will be the final value which will be returned as the result of the **`reduce()`** method. The second parameter is the current element of the array. Finally, after the fat arrow function, we execute some code on one or both the arguments. The resultant value is then stored in the accumulator (the first argument) for the next iteration. This process keeps on going until the method reaches the last element of the array.

Without much further ado, let’s understand this with a simple example:

1.  `let numbers = [2, 4, 6, 8, 12];`
2.  `let sum = numbers.reduce((total, number) => total + number);`

4.  ``console.log(`The sum is ${sum}`);      //The sum is 32``

    **Code 6.13:** ES6 method to reduce an array to a single value

In the preceding *[code example 6.13](#c06.xhtml_co6_13)*, we have called the reduce method on the array numbers. It will pass through every element of the array numbers.

We have named the two parameters as total and number respectively. The variable total is the accumulator, that is, it will store the collection of the calculated value. The second variable number refers to the current element of the array. Finally, after the fat arrow function, we add the two parameters and store the result in the accumulator, that is, the variable total in our case. Therefore, the reduce method passes through every element, adds the current value to the total and finally returns the accumulator total as the final value.

# [Array and object destructuring](#toc.xhtml_s132a)

The English dictionary states the meaning of the word destructuring as destroying the structure of something, or to dismantle something. In ES6, we use this concept of destructuring to break down values of an array into simple variables. We can think of it as unpacking a box of values.

![](images/Figure-6.38.jpg)

**Figure 6.38:** Destructuring is similar to unpacking items from a box

Let’s understand this 'unpacking' using examples:

![](images/Figure-6.39.jpg)

**Figure 6.39:** Destructuring an array

As you can see in the preceding screenshot, we have initialised the array colors with four values of strings. Now, if you remember *[Chapter 4](#c04.xhtml)* correctly, arrays are called as an organized collection. It means that an array has indexed values, that is, the emphasis is on the index or the position of the element.

In array destructuring, we mimic an array on the left hand side, and provide variables where we want to unpack and store certain values of the array. On the right hand side, we assign this mock array with the value of the original array from which we want to unpack the values. As you can see, the array destructuring matches the variables on the left hand side with the positions of the actual array colors, and assigns the variables on the left with their corresponding positions of the original array on the right.

In the case of object destructuring, since objects are not indexed collections, we cannot use the same method we used for the arrays. For objects, we need to provide the same variable names on the left that are actually present as keys in the object. Alternatively, we can provide these keys a pseudo-variable name using the colon symbol.

![](images/Figure-6.40.jpg)

**Figure 6.40:** Destructuring an object

As shown in the preceding screenshot, we can store the keys and the values of an object into individual variables using the same technique we have used for array destructuring. Instead of the mock array, we now use a mock object with the curly braces on the left side and the object on the right side of the assignment. The mock object contains the names of the keys of the object. As you can see in *[figure 6.40](#c06.xhtml_fig6_40)*, we do not have a key called wheels in the original object car. Therefore, when we try to unpack the object using the variable wheels, it returns undefined. However, we can assign a new variable to the original key by using the colon, as we have used for the key name type.

# [ES6 Modules](#toc.xhtml_s133a)

In the early years of JavaScript, codes with thousands of lines of code were rare. Fast forward to 2020, and we have entire applications created using JavaScript. It’s fair to say that across several pages of an application, there might be several blocks of code we might want to reuse. Sometimes, these blocks of code do not even belong to the flow of the code. For instance, we can have a function to add several numbers. Instead of writing the function add multiple times, we can define this function once and use it multiple times. This conversion of code into small reusable parts is called as modular coding and the small pieces of codes are called as modules.

Now, these modules might not even belong in the flow of the code. For example, a JavaScript file might be dedicated to the functionality of login. It’s obvious that the add function does not belong in the middle of the logic of login. Besides, there might be many other JavaScript files that would need the assistance of this add function.

It, therefore, makes sense to store such a utility function in a separate JavaScript file of its own where it can be used by everyone. Now, the next problem here is how to make it available to every file in the system. This is where the ES6 imports and exports come into the picture.

To understand ES6 modules, imports and exports, we will create a sample **`index.html`** file:

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `<head>`
4.  `    <meta charset="UTF-8">`
5.  `    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
6.  `    <title>ES6 Modules</title>`
7.  `</head>`
8.  `<body>`
9.  `    <p>The sum is <span id="result"></span></p>`
10.  `    <script type="module" src="./scripts/index.js"></script>`
11.  `</body>`
12.  `</html>`

    **Code 6.14:** index.html for modules

As you can see in the preceding *[code example 6.14](#c06.xhtml_co6_14)*, it’s a simple **`index.html`** file with one major change – we are adding a type module to the import of **`index.js`** file in the HTML.

This is to make sure that the browser knows that this file will be using import and export in its code.

Now, let’s create a folder called **`scripts`**, and inside that, let’s create a file called **`utils.js`**. Inside **`utils.js`**, we will create out module function **`add`**.

1.  `export const add = (number1, number2) => number1 + number2;`

    **Code 6.15:** utils.js for the module

As you can see in the preceding *[code example 6.15](#c06.xhtml_co6_15)*, we have now created the modular reusable function add using ES6 arrow functions. It takes two values, adds them and returns the sum. The only additional thing we have done here is that we used the keyword export. This keyword ensures that this function will be available to be used by all the files who would like to import it.

Now, finally, we will create the **`index.js`** file that we have mentioned in the **`index.html`**. It will look like the following code:

1.  `import {add} from './utils.js';`

3.  `let result = add(5, 6);`
4.  `document.getElementById('result').innerHTML = result;`

    **Code 6.16:** index.js for the module

In the **`index.js`** file, the first thing that we try to do is import the function **`add`** from the **`utils.js`** file. To do that, we use the keyword import, and then import the name of the function inside the curly braces. Finally, we complete the line by stating the path of the file from which we need to import this function. Why do we add the curly braces? We add the curly braces because every file might export several other functions. It’s possible that we might want to use only a few of these functions. These functions can be imported by separating their names with commas.

If we would have added the keyword default after the keyword export in the *[code example 6.15](#c06.xhtml_co6_15)*, it would mean that the entire file is used for exporting only one function, which is the add function. In that case, we do not need the curly braces while importing.

The rest of the *[code example 6.16](#c06.xhtml_co6_16)* stores the value of the function execution of the function add, and assigns it to an empty span element in the HTML file.

I urge you to execute this file on your machine. This will help you to understand the code better.

# [Conclusion](#toc.xhtml_s134a)

In this rather long chapter, we learned about several features introduced by ES6\. Singling out any feature would be a sin. However, to name certain ES6 features that you will be regularly using for creating next-gen applications include, but is not limited to, arrow functions, let and const, destructuring, and spread operators. To put it in a nutshell, functions like arrow functions and the new array methods like **`map`**, **`filter`**, and **`reduce`** not only reduced the number of lines of code, but it also simplifies and increases the speed of execution of JavaScript. Similarly, **`let`** and **`const`** help you to create scopes which can avoid major pitfalls while creating enterprise-level applications. The rest of the features help improve and facilitate faster execution of JavaScript. ES6 forms the basis of several top-notch front-end libraries, used for creating popular web applications like *Facebook*, *Twitter*, *Instagram*, and so on. In fact, libraries like *ReactJS* actively ask the developers to learn ES6 before learning React. React heavily uses several important features of ES6\. In the next chapter, we will learn about classes. Classes is a JavaScript concept introduced by ES6 to simplify the creation of object templates.

# [Points to remember](#toc.xhtml_s135a)

*   Hoisting in JavaScript is the process of moving declarations to the top. It is important to note that only the declarations, and not the initializations are moved to the top.
*   ES6 introduced two new keywords for creating variables – **`let`** and **`const`**. Both **`let`** and **`const`** create a new type of scope called block-level scope. In a block-level scope, the variables’ existence is limited solely to the block. These variables are not accessible outside the block. You cannot change the value set by **`const`**.
*   The bind, call, and apply method for objects are used for binding the value of this for objects.
*   The ternary operator is a simplified way for conditional if…else statement. Ternary operators are best used for cases when you need to return certain value.
*   The advantage of rest parameters is when you are not certain about the number of parameters required in the function. Spread operators have the same syntax as that of the rest parameters. However, spread operators are used for concatenating or copying arrays or objects.
*   Perhaps, one of the best features introduced by ES6 are the template literals. Replacing the traditional method of concatenating strings, template literals not only allow a simpler way of inserting variables in strings, but also allow multi-line strings.
*   Arrow functions serve two significant purposes – simplifying the process of writing functions that return values, and removing the bindings of the **`this`** keyword inside functions.
*   ES6 introduced three new methods of arrays – map, filter, and reduce. All the three methods parse through every element of the array, and should be used only when you need to return a new array. The map method allows you to manipulate every element of an array, the filter method allows you to filter elements of an array based on a condition, and the reduce method is to reduce all the elements of the array to a single value.
*   Array and object destructuring is akin to unboxing values of an array or an object into separate variables.
*   ES6 modules is a method of creating reusable functions that can be imported and exported across the application workspace.

# [Multiple choice questions](#toc.xhtml_s136a)

1.  **What will be the output of the line number 5 in the following code?**
    1.  `let number = 50;`
    2.  `{`
    3.  `    let number = 25;`
    4.  `}`
    5.  `console.log(number);`
    1.  25
    2.  50
    3.  Error
2.  **What will be the output of the line number 4 in the following code?**
    1.  `let numbers = [2, 4, 6];`
    2.  `let even = numbers;`
    3.  `numbers[0] = 7;`
    4.  `console.log(even);`
    1.  [7, 4, 6]
    2.  [2, 4, 6]
    3.  Error

# [Answers](#toc.xhtml_s137a)

1.  **b**
2.  **a**

# [CHAPTER 7](#toc.xhtml_c07)

# [Classes](#toc.xhtml_c07)

In the previous chapter, we explored ES6 in depth. In this chapter, we will be learning about one of the most exciting additions to JavaScript – ES6 classes. At the time of writing, classes have become an indispensable part of coding in JavaScript. In simple words, classes are nothing but "*special functions*." As we will go through this chapter, we will understand how and why classes are a beautiful extension of the functions that we have learned earlier in this book. Learning classes will be of immense help if you intend to learn front-end libraries like ReactJS or VueJS.

# [Structure](#toc.xhtml_s138a)

In this chapter, we will cover the following topics:

*   Understanding classes
*   Classes and methods
*   Inheritance
*   Getters and setters

# [Objective](#toc.xhtml_s139a)

After studying this chapter, you should be able to understand how to use JavaScript classes and use them as template to create objects. You will be able to create a rigid structure to encapsulate data.

# [Understanding classes](#toc.xhtml_s140a)

ES6 introduced JavaScript to the world of classes. Outside this book, you will learn that ReactJS (one of the most popular front-end libraries in the world, created by Facebook Incorporation) turned classes into a crucial part of the web development language.

Classes, as I mentioned earlier, are a special kind of function. In *[Chapter 5: Objects](#c05.xhtml)*, we learned about objects and prototypes to create objects. Let’s look at that example again:

1.  `function Person(first, last) {`
2.  `    this.firstName = first;`
3.  `    this.lastName = last;`
4.  `}`

6.  `Person.prototype.getFullName = function() {`
7.  ``    console.log(`${this.firstName} ${this.lastName}`);``
8.  `}`

    **Code 7.1:** Objects and Prototypes

In the preceding *[code example 7.1](#c07.xhtml_co7_1)*, we have used a function to create a template for the Object **`persons`**. Before ES6, the best way to create an object template was to make use of functions. ES6 introduced classes to create a dignified and structured format to generate object templates.

The example shown in the preceding *[code example 7.1](#c07.xhtml_co7_1)* can be rewritten as a class in the following way:

1.  `class Person {`
2.  `    constructor(first, last) {`
3.  `        this.firstName = first;`
4.  `        this.lastName = last;`
5.  `    }`

7.  `    getFullName = () => {`
8.  ``        console.log(`${this.firstName} ${this.lastName}`);``
9.  `    }`
10.  `}`
11.  `let father = new Person('John', 'Doe');`
12.  `father.getFullName();  //John Doe`

    **Code 7.2:** Classes

As shown in the *[code example 7.2](#c07.xhtml_co7_2)*, we have a more structured approach for creating object templates in the form of classes. To define a class, we use the keyword class, followed by a name for the class, and a pair of curly braces.

Every class always has a default method called *constructor*. The constructor specifies the properties of the class. Even if the user does not explicitly create the method constructor, it always exists. This constructor method is the first thing to be always called when the class object is initialized.

You can also add methods inside the classes. We will learn in detail about the methods in the next section.

Finally, to use a class, you need to create an instance of the class using the JavaScript keyword new, and a pair of parentheses. You can add any number of arguments in the parentheses. By logic, these arguments should be accessed inside the constructor. As shown in the line number 12 of the *[code example 7.2](#c07.xhtml_co7_2)*, using the keyword new will create an instance of the class **`Person`**.

# [When to use functions and when to use classes?](#toc.xhtml_s141a)

In layman terms, the simple difference between functions and classes is as follows:

*   **Functions** are a way to package reusable code.
*   **Classes** are a blueprint for a JavaScript object.

Therefore, when we are writing code that will be reused several times in the script, we can package it inside a function. However, when we need to create an object that needs to be generated multiple times, we make use of a class to define the object properties and methods.

# [Are classes hoisted?](#toc.xhtml_s142a)

In the previous chapters, we have learned that in JavaScript, variable and function declarations are "*moved to the top*" of the script. This "*moving to the top*" is called as *JavaScript hoisting*.

However, unlike variables and functions, JavaScript classes are not hoisted. As shown in the following screenshot, JavaScript throws an error on the very first line (denoted by the number 1 after the colon in the error highlighted in red). It means that every time you need to use a class, you need to define it first before using it.

![](images/Figure-7.1.jpg)

**Figure 7.1:** Class declarations are not hoisted

# [Classes and methods](#toc.xhtml_s143a)

In *[Chapter 5: Objects](#c05.xhtml)*, we have learned that the functions defined inside an object are called as *methods*. Since classes are primarily a blueprint for creating objects, functions created inside a class are also called as *methods*. In the preceding *[code example 7.2](#c07.xhtml_co7_2)*, we have already seen two methods – **`constructor`** and **`getFullName`**. If you observe the *[code example 7.2](#c07.xhtml_co7_2)* closely, you will notice that we do not need to declare the methods created inside a class.

Inside a JavaScript class, there are the following four types of methods:

*   **constructor**

    The constructor is a special method of the class. It is present by default, even if the developer chooses not to explicitly create it. If the developer chooses not to add a constructor, JavaScript adds an invisible and empty constructor method. The constructor is called automatically when a class is initialized.

    The primary job of the constructor is to create and initialize the object of the class. You can specify the properties of the class inside the constructor.

    Let’s revise the syntax of the constructor with the help of the *[code example 7.3](#c07.xhtml_co7_3)*:

    1.  `class Person {`
    2.  `    constructor(first, last) {`
    3.  `        this.firstName = first;`
    4.  `        this.lastName = last;`
    5.  `        this.nationality = "French";`
    6.  `    }`
    7.  `}`

    9.  `let father = new Person('John', 'Doe');`

        **Code 7.3:** The constructor method of a class

    As shown in the preceding *[code example 7.3](#c07.xhtml_co7_3)*, to create a constructor, you need to use the keyword constructor. Do note, only the exact name constructor can be used for creating a constructor. As shown in the *[code example 7.3](#c07.xhtml_co7_3)*, the constructor method can take multiple parameters. These parameters are the ones which are passed when a new instance of the class is created using the **`new`** keyword. As shown on the line number 9 of the *[code example 7.3](#c07.xhtml_co7_3)*, the arguments "**`John`**" and "**`Doe`**" are passed as parameters to the constructor method.

    **Tip:** Use the constructor method when you need to initialize data before any of the code in the class is executed.

*   **General methods**

    We have already seen an example of a general JavaScript method in the *[code example 7.2](#c07.xhtml_co7_2)*. Let’s understand the methods of a class with another code example:

    1.  `class Person {`
    2.  `    constructor(first, last) {`
    3.  `        this.firstName = first;`
    4.  `        this.lastName = last;`
    5.  `    }`

    7.  `    getFullName = () => {`
    8.  ``        console.log(`${this.firstName} ${this.lastName}`);``
    9.  `    }`

    11.  `    addNationality() {`
    12.  `        this.nationality = "French";`
    13.  `    }`
    14.  `}`

    16.  `let father = new Person('John', 'Doe');`
    17.  `father.getFullName();    //John Doe`
    18.  `father.addNationality();`
    19.  `console.log(father);    //{age: 24, firstName: "John", lastName: "Doe"}`

        **Code 7.4:** Traditional JavaScript methods

    As shown in the *[code example 7.4](#c07.xhtml_co7_4)*, you can either use the ES6 arrow functions or the traditional JavaScript functions. To invoke (call) a method inside a class, you first need to create an instance of the class, as shown in the line number 16 in the *[code example 7.4](#c07.xhtml_co7_4)*. Next, you can call the method name by typing the name of the class instance, and then calling the method name with a pair of parentheses. As with general JavaScript methods, you can pass arguments to these methods by adding values inside the parentheses during the method invocation.

    If you have been noticing closely, you don’t need to declare a method when you use it inside the class. It is because these methods are a part of the class object **`Person`**.

*   **Static methods**

    A static method is a special kind of method. You can use a static method in any of the following cases:

    *   **No dependency on class instance**: The code inside the method is not dependent on the instance of the class getting generated. In fact, if the code inside the method will not be using the instance variable at all, we should use it as a static method.
    *   **Code sharing**: If all the methods in the instance will be sharing a piece of code, it makes more sense to use it as a static method. For instance, if we have a class Area which calculates the area of any geometrical figure, we will probably require a function to restrict the decimal points of any number to just two points. Such a function will be shared by all the methods inside the class for calculations. This function or rather, this method should be a static method.
    *   **No change in method definition**: A static method should be used if the definition of the method or the code written in the method should not be changed or overridden.
    *   **Utility classes**: If you are writing a class that is not a part of the actual flow of the code, but it helps the actual flow indirectly, it should possess static methods.

    Static methods are defined on the class itself, and not on the instance of the class.

    To create static methods, we need to add the JavaScript keyword static in front of the method.

    As shown in the following screenshot, we have defined a static method **`toTwoDecimals`**. If we call the static method on the class itself, it will execute. However, if you attempt to execute the **`toTwoDecimals`** method on the class instance rectangle, it results in an error.

    ![](images/Figure-7.2.jpg)

    **Figure 7.2:** Static methods

# [Inheritance](#toc.xhtml_s144a)

In simple words, inheritance means receiving properties or money from the previous holder. JavaScript follows a similar interpretation. In JavaScript, when you use the JavaScript keyword **extends** during a class definition, it inherits all the methods from the class name that is specified after the keyword **extends**. Along with the keyword, you also need to call the **`super()`** method in the constructor of the child element to access all the properties and the methods of the parent class.

Let’s understand inheritance with an example:

![](images/Figure-7.3.jpg)

**Figure 7.3:** Inheritance

In the preceding screenshot, we have a class **`Person`** having in-built properties, nationality and language set to English and UK English. The **`Person`** class also accepts a parameter age. We also have a class **`Student`** which extends the class **`Person`**. When we use the keyword extends, JavaScript enables a class to inherit properties and methods from another class. In the case of *[figure 7.3](#c07.xhtml_fig7_3)*, the class **`Student`** calls the super (props) method to access all the properties and the methods of the parent class **`Person`**. Hence, when the method display of the class **`Student`** is called, it displays values from the properties of both the class **`Student`** and the class **`Person`**.

Inheritance is useful for code reusability. It helps reuse of the existing properties and the methods of a class when you create a new class.

# [Getters and Setters](#toc.xhtml_s145a)

In the preceding section, we saw four different types of methods used in ES6 Classes. The last category is known as Getters and Setters. Going by the definition of the word itself, getters and setters are the methods inside JavaScript classes to get the value of properties of the class and to set the value of the properties of the class. These methods seamlessly fit into the class definition. However, we can do much more than simply getting and setting the values. These methods can help us in writing some code which needs to be executed before we get or set the value. For instance, if we want to send a request to the server before setting a value, we can do that inside the set method.

To keep it simple, getters and setters is a structured way for fetching and setting the values of the class. We can create a get and a set method using the JavaScript keywords get and set. In the case of the setters, it can also accept parameters to set the property values.

One important thing to keep in mind here is that the name of the getter and the setter method cannot be the same as the name of the property. Let’s understand it with an example:

In *[figure 7.4](#c07.xhtml_fig7_4)*, we have a class **`Person`** with a property name. We have also created a **`get`** method and a **`set`** method. As I had mentioned earlier, you cannot use the same name for the getters and setters as the name of the property. Hence, we have used the name of the method as **`personName`** instead of the property name **`name`**. Kindly do notice that you don’t need to explicitly call the get and set method. They work behind the scenes when you try to fetch or set a value of the properties.

Now, let’s consider the example of a toaster. At some point in our lives, we must have either used or seen a toaster. It’s an easy-to-use product. All you need to do is insert the slices of breads at the designated areas and turn on the machine. When the slice of breads will get toasted, they will pop out. On the exterior, there are two empty spaces to place the bread, a button to pop out the slices of breads, a button to turn on the machine and a knob for setting up the level of toast darkness. However, if I ask you to open up the machine to its complex interiors and then use it for toasting, would you be able to use it?

This example shows why it’s crucial to keep certain implementations and methods private to a tool, and the strong reason to not expose it to the public. In a similar analogy, we can turn certain variables and methods private to a class. We will look at this in greater detail with the latest introduction of private methods in the second last chapter – ES6 and beyond.

![](images/Figure-7.4.jpg)

**Figure 7.4:** Getters and setters

# [Conclusion](#toc.xhtml_s146a)

Classes serve as an excellent way to create object templates. In fact, as I have mentioned earlier, classes turn up to be one of the most significant features of JavaScript when you use front-end libraries like ReactJS or VueJS. In this chapter, we have learned how to create classes and more importantly, where to use classes. We also learned about the different types of methods that we can use in classes. From the next chapter onwards, we will move into a more practical application of advanced JavaScript with reaching out to the server.

# [Points to remember](#toc.xhtml_s147a)

*   Classes were introduced in ES6 to create a more structured format for writing object templates.
*   Classes have four different types of methods.
*   The constructor method is the default method inside a class. It is the first thing to be called when an object is initialized. Typically, the constructor is used for setting the initial values of the class.
*   Even if the user has not explicitly created the method constructor, it is by default called behind-the-scenes by JavaScript.
*   If you have a method, which is not dependent on the class instance or the script inside the method will not be modified, you can use the JavaScript keyword static to turn it into a static method.
*   JavaScript classes can inherit the properties and the methods of a class using the **extends** keyword, and calling the **`super()`** method inside the child’s constructor.
*   Finally, classes provide an optional separate method for getting or setting the values of the properties of the class. Care must be taken to avoid naming these methods with the name of the properties.

# [Multiple choice questions](#toc.xhtml_s148a)

1.  **The constructor is not the first method to be called when a class has been initialized – True or False?**
    1.  True
    2.  False
2.  **What will be the output of the line number 8 in the following code?**
    1.  `class Person {`
    2.  `    static display(name) {`
    3.  `        console.log(name);`
    4.  `    }`
    5.  `}`

    7.  `let father = new Person("John");`
    8.  `father.display();`

        **Code 7.5:**

    1.  John
    2.  undefined
    3.  Error: **`father.display()`** is not a function

# [Answers](#toc.xhtml_s149a)

1.  **b**
2.  **c**

# [CHAPTER 8](#toc.xhtml_c08)

# [Callbacks and Promises](#toc.xhtml_c08)

With this chapter, you will be ushering yourself into the mean, real-world of practical web development. This chapter earmarks the introduction to Reaching Out to the Servers.

Let's take the example of a typical web application like Twitter or Facebook (at the time of writing). These applications together have close to 100,000,000 users who use it daily. It's quite obvious that these platforms would require a safe and secure environment to not only store and fetch the mammoth size of the data of the users, but also perform complex calculations when needed. Such places are called as servers in the world of technology, and every true-blue web application requires servers for its sane functioning.

In this chapter, you will be understanding how to interact with the servers from the front-end of your web application. To begin with, you will explore the world of Asynchronous JavaScript that forms the crux of working with servers. After that, you will learn in detail about the callback functions (a concept that we explored in *[Chapter 3: Functions](#c03.xhtml)*), and finally we will complete this chapter with an understanding of JavaScript Promises – a simplified way of dealing with asynchronous JavaScript.

# [Structure](#toc.xhtml_s150a)

In this chapter, we will cover the following topics:

*   Asynchronous JavaScript
*   Callbacks
*   Callback Hell
*   Promises

# [Objective](#toc.xhtml_s151a)

After studying this chapter, you should be able to understand the concept of asynchronous JavaScript. You will be able to interact and fetch data from the server without affecting the flow of your web application. You can use JavaScript callbacks and promises for dealing with asynchronous requests.

# [Asynchronous JavaScript](#toc.xhtml_s152a)

A majority of the JavaScript you have witnessed so far in this book has been synchronous. Synchronous code means that every line of code diligently waits for the previous line of code to finish execution. Let's understand this with an example.

1.  `console.log("Wake up");`
2.  `console.log("Brush your teeth");`
3.  `console.log("Take a shower");`

    **Code 8.1:** Synchronous JavaScript

When we execute the script shown in the preceding *[code example 8.1](#c08.xhtml_co8_1)*, the output understandably looks something like the following:

![](images/Figure-8.1.jpg)

**Figure 8.1:** Output of synchronous JavaScript

As we can see from the *[code example 8.1](#c08.xhtml_co8_1)* and *[figure 8.1](#c08.xhtml_fig8_1)*, every line of code waits for the previous line to complete execution before it executes the code on its line. This behavior of waiting for the code on the previous line to complete its execution is called as *synchronous JavaScript*.

Now let's modify the code, shown in the *[code example 8.1](#c08.xhtml_co8_1)*.

1.  `console.log("Wake up");`

3.  `setTimeout(() => {`
4.  `    console.log("Brush your teeth");`
5.  `}, 2000);`

7.  `console.log("Take a shower");`

    **Code 8.2:** Asynchronous JavaScript

In the previous chapters, we had studied the **`setTimeout`** function. To quickly revise, the **`setTimeout`** function takes two arguments – an anonymous function and time in milliseconds. It waits for the time specified in the second argument, and then executes the code in the first argument. Keeping that in mind, the output for the *[code example 8.2](#c08.xhtml_co8_2)* will be the following:

![](images/Figure-8.2.jpg)

**Figure 8.2:** Output of asynchronous JavaScript

As you can see in the preceding screenshot, the statement *Brush your teeth* is logged after the statement *Take a shower*. In this case, the code on the line number 7 in the *[code example 8.2](#c08.xhtml_co8_2)* does not wait for the code on the line numbers 3-5 to finish execution. Instead, it completes its execution while the browser waits for the two seconds to elapse since it reached line numbers 3-5\. After the two seconds are completed, the code on line numbers 3-5 is executed.

This method of not waiting for the previous code to complete its execution is called as *asynchronous JavaScript*. In the preceding example, the **`setTimeout`** function makes the line number 4 asynchronous.

# TRY IT YOURSELF

What will happen if you execute the code shown in the following *[code example 8.3](#c08.xhtml_co8_3)*?

Spend a couple of seconds to think of the solution before you try it out on your browser or machine.

1.  `console.log("The order arrives.");`

3.  `setTimeout(() => {`
4.  `    console.log("Eat fries.");`
5.  `}, 2000);`

7.  `console.log("Eat the burger.");`
8.  `console.log("Eat the pasta.");`

10.  `setTimeout(() => {`
11.  `    console.log("Drink the soda.");`
12.  `    console.log("Eat the garlic bread.");`
13.  `}, 3000);`

15.  `console.log("Eat the chocolate cake.");`

    **Code 8.3:** Try it yourself example

# [When to use asynchronous JavaScript](#toc.xhtml_s153a)

Let's consider a more practical scenario. When you type **https://www.google.com** on your browser's address bar, does the browser render the home page of Google at the exact same time always?

The answer is NO. It's fair to say that the rendering of the home page of Google depends on several factors. Amongst those, the primary ones include the speed of your internet, and the server speed to resolve your request.

Now, what if our entire JavaScript code is synchronous, and it is dependent on the response received from a server? For all we know, our web page would take more than a minute to render completely in the worst-case scenario. Think of all the times when you have typed in a website's name, and the website took forever to load on your browser. It’s quite obvious that you or any other user for that case would be frustrated and quit the page after some time.

For this reason, when you are working with a server, it’s imperative to make sure the code is asynchronous. It will ensure that even if the server takes a long time to respond, the JavaScript will not keep waiting, and the code ahead will execute.

# [Callback Functions](#toc.xhtml_s154a)

In *[Chapter 3: Functions](#c03.xhtml)*, we have seen several types of functions. One particular type of function that comes in use for asynchronous (async) JavaScript is the *callback* function. When a function accepts another function as an argument, the contained function is called a callback function. Perhaps, the best example of a callback function is the **`setTimeout`** function that we have seen in the *[code examples 8.2](#c08.xhtml_co8_2)* and *[8.3](#c08.xhtml_co8_3)*.

However, it’s not necessary that the callback function should be anonymous. Let’s look at an example of a named callback function:

1.  `function greet(name) {`
2.  ``    console.log(`A very good day to you, ${name}`);``
3.  `}`

5.  `function initialize(firstName, lastName, callback) {`
6.  ``    let fullName = `${firstName} ${lastName}`;``

8.  `    callback(fullName);`
9.  `}`

11.  `initialize('John', 'Doe', greet);`

    **Code 8.4:** Named callback function

In the preceding *[code example 8.4](#c08.xhtml_co8_4)*, we have two functions – initialize and greet. When the function initialize is defined, we pass the function greet as an argument.

![](images/Figure-8.3.jpg)

**Figure 8.3:** Output of the [code example 8.4](#c08.xhtml_co8_4)

As you can see in the preceding screenshot, the function greet is passed as an argument. Inside the function initialize, the function greet is inside the variable parameter callback. This variable callback is called, with the variable **`fullName`** passed as an argument to it. The output shown on the last line ensures that our named callback was indeed called.

# [How can callback functions help in asynchronous JavaScript](#toc.xhtml_s155a)

The very nature of the async JavaScript function is that the developer rarely has any clue when the script will receive the response (in the case of the servers). It essentially means that if there is a certain block of code that is dependent on the response received from the server, it should be executed only after the response has been received.

For instance, an e-commerce web application has requested data from the server about the items added to the cart by the user. Until it receives this particular data from the server, it doesn't make any sense showing the cart page, correct? If we try showing this page even when the response is not received, it will display either an empty cart or an incorrect cart. At the same time, since only the page showing the cart is dependent on the request, the rest of the pages should continue rendering without getting blocked.

To resolve this, we can introduce a callback function to execute the dependent block of code only when the request has been successfully resolved. Let’s understand this with an example.

1.  `const view = (url) => {`
2.  ``    console.log(`Loading ${url}`);``
3.  `}`

5.  `const download = (url, callback) => {`
6.  `    setTimeout(() => {`
7.  ``        console.log(`Downloading ${url}`);``
8.  `        callback(url);`
9.  `    }, 2000)`
10.  `}`

12.  `download("https://cdn.shopify.com/s/files/1/0329/9547/5515/files/350X240_55x.png?v=1603344594", view);`

    **Code 8.5:** Callback function in async code

In the preceding *[code example 8.5](#c08.xhtml_co8_5)*, we have two functions – **`view`** and **`download`**. At this moment, to keep the code simple, the sole job of these functions is to print a statement. However, in a practical scenario, we can only view an image after we download the image, correct? This logic makes the function view dependent on the result of the function download. Hence, the function view, that is passed as a callback to the function download, is called only after the function download has finished printing its statement. When you execute the *[code example 8.5](#c08.xhtml_co8_5)* on your local machine, after two seconds the output on the screen will be, as shown in the following screenshot:

![](images/Figure-8.4.jpg)

**Figure 8.4:** Output of the [code example 8.5](#c08.xhtml_co8_5)

However, there will always be a scenario where the request to the server might fail. There could be several reasons for the failure – from network issues to wrong URL. If we do not handle this server request failure, sometimes it might even crash the application. A good practice in web development is to include an error handler in your asynchronous code. For the preceding *[code example 8.5](#c08.xhtml_co8_5)*, we will introduce the error handling by introducing an if…else condition. In the last section of this chapter – Promises, we will learn a better way of handling errors.

1.  `const view = url => {`
2.  ``    console.log(`Loading ${url}`);``
3.  `}`

5.  `const errorHandler = error => {`
6.  ``    console.log(`The error is ${error}`);``
7.  `}`

9.  `const download = (url, success, error) => {`
10.  `    setTimeout(() => {`
11.  ``        console.log(`Downloading ${url}…`);``
12.  `        if(!url || url.length === 0) {`
13.  `            error('URL is not provided');`
14.  `        } else {`
15.  `            success(url);`
16.  `        }`
17.  `    }, 2000)`
18.  `}`

20.  `download("https://cdn.shopify.com/s/files/1/0329/9547/5515/files/350X240_55x.png?v=1603344594", view, errorHandler);`
21.  `download("", view, errorHandler);`

    **Code 8.6:** Error handling in callback

In the preceding *[code example 8.6](#c08.xhtml_co8_6)*, we have introduced an error handler inside the asynchronous function download. In fact, we pass the error handler function as the third argument to the function download. Inside the function download, we check for the existence of the URL passed in the parameters and the length of the URL. If either of the condition returns false, the error handling callback function will be called, otherwise the success callback function is called. When you execute the preceding code, the output looks like the following:

![](images/Figure-8.5.jpg)

**Figure 8.5:** Output of the [code example 8.6](#c08.xhtml_co8_6)

In the next chapter, we will be introducing APIs to connect to existing servers. Therefore, in this chapter, we will mock the asynchronous behavior of JavaScript code with the help of the **`setTimeout`** function.

# [Callback Hell](#toc.xhtml_s156a)

In the previous section, we learned how to use callbacks to solve the problem with asynchronous code in JavaScript. However, there is one major problem with using callbacks. Let's understand this problem with the help of an example.

In the previous examples, we have dealt with downloading and viewing only one URL. What if there are multiple URLs to download from? Additionally, what if every download was dependent on the completion of the prior download?

Kindly spend some time to think and try out a solution to the preceding question.

With some code modification to suit our needs, we can replicate the preceding *[code example 8.6](#c08.xhtml_co8_6)* to download three URLs, as shown in the following *[code example 8.7](#c08.xhtml_co8_7)*:

1.  `const view = url => {`
2.  ``    console.log(`Loading ${url}`);``
3.  `}`

5.  `const errorHandler = error => {`
6.  ``    console.log(`The error is ${error}`);``
7.  `}`

9.  `const download = (url, callback) => {`
10.  ``    console.log(`Downloading ${url}…`);``
11.  `    callback();`
12.  `}`

14.  `let url1 = "https://images.freeimages.com/images/large-previews/4ab/fruits-and-vegetables-1-1324165.jpg";`
15.  `let url2 = "https://images.freeimages.com/images/large-previews/d42/vegetables-4-1189021.jpg"`
16.  `let url3 = "https://images.freeimages.com/images/large-previews/360/banana-1-1330048.jpg"`

18.  `download(url1, function() {`
19.  `    setTimeout(() => {`
20.  `   if(url1.length !== 0) {`
21.  `     view(url1);`
22.  `     download(url2, function() {`
23.  `      setTimeout(() => {`
24.  `       if(url2.length !== 0) {`
25.  `                view(url2);`
26.  `                  download(url3, function() {`
27.  `                   setTimeout(() => {`
28.  `                     if(url3.length !== 0) {`
29.  `                       view(url3);`
30.  `                      } else {`
31.  `                       errorHandler("URL is not provided");`
32.  `                      }`
33.  `                    }, 2000)`
34.  `                  })`
35.  `              } else {`
36.  `               errorHandler("URL is not provided");`
37.  `              }`
38.  `      }, 2000)`
39.  `    })`
40.  `  } else {`
41.  `        errorHandler("URL is not provided");`
42.  `      }`
43.  `  }, 2000)`
44.  `});`

    **Code 8.7:** Callback hell

If you initially had trouble reading or understanding the code from lines 18 to 44 in the preceding *[code example 8.7](#c08.xhtml_co8_7)*, this is precisely called *Callback Hell*.

In simple terms, when you are dealing with multiple function calls that are dependent on the execution of a request or a condition, it results in a disorganized and confusing format of callback functions. This confusing structure is called the *Pyramid of Doom* or *Callback Hell*. In fact, the larger the number of requests, the more difficult it is to maintain this conditional functioning of callbacks. In the preceding *[code example 8.7](#c08.xhtml_co8_7)*, we are dealing with three URLs to be downloaded sequentially. Imagine if we had to deal with 20 or 100 such requests. To solve this problem of callback hell, JavaScript introduced the concept of async/await and Promises.

# [Promises](#toc.xhtml_s157a)

To understand promises, let me give you a very simple real-life example:

*A popular music band has millions of fans worldwide. This band is famous for hosting concerts across cities for their fans. However, since the past few months, the band has not been hosting any shows. Worried fans are frequently urging the band to reveal details of their next concert. Finally, the music band responded and requested their fans to follow the band on social media platforms like Twitter and Facebook. The band promised the fans that whoever is following them on their social media platforms will be the first ones to receive an update about their next concert. In fact, if the band won't be performing any shows for any unforeseen circumstances, the fans following them on social media will also be the first ones to be informed.*

The preceding example perfectly defines the functioning of JavaScript Promises. If we observe the preceding example closely, we will notice that there are three important parts, which are as follows:

*   A producer, or in programming terms, a producing code: It refers to something that might take some time to complete a task. In the preceding example, it refers to the music band who will take some time to host a concert.
*   A consumer, or in programming terms, a consuming code: It refers to the receiver of the results of the producer. For instance, in the preceding example, it refers to the fans who are waiting for the music band to host their next concert.
*   A promise that links the producer to the consumer: In the preceding example, the social media platform is the link between the producer (the music band) and the consumer (the fans). The producer takes its own sweet time to achieve the results, and the promise makes it available to all the consumers, when ready.

This can be graphically visualized as the following:

![](images/Figure-8.6.jpg)

**Figure 8.6:** A graphical representation of promises

JavaScript promises do a lot more than simply linking a producing code to the consumer code. As we have noted earlier, we will never know when a request will be completed, or if it will fail. JavaScript promises hold the state of the asynchronous request. The pending promise will either be fulfilled, or it will be rejected. When either of the two happens, handlers associated to the Promise will be informed immediately.

At any given time, a Promise is in one of these states:

*   **Pending**: The initial state when a Promise is created. It is neither fulfilled, nor rejected.
*   **Fulfilled**: It means that the request was completed successfully.
*   **Rejected**: It means that the request failed.

The syntax for a **`Promise`** is as follows:

1.  `const promise = new Promise(function(resolve, reject) {`
2.  *`//Description of the promise`*
3.  `}`

    **Code 8.8:** Syntax of a promise

As shown in the *[code example 8.8](#c08.xhtml_co8_8)*, the **`Promise`** object is created using the **`new`** keyword. The **`Promise`** contains a function execution with a resolve, and a reject callback. This function that is passed to the **`Promise`** object is called as an executor. When a **`Promise`** is created, the executor is executed immediately and automatically.

Typically, a request to the server is added inside the executor.

Whenever the executor gets the result, it should call one of the callbacks:

*   **resolve(value)**: If the request or the task completed successfully with a result denoted by the variable value.
*   **reject(error)**: If the request failed with the error denoted by the variable error.

Visually, the functioning of a Promise looks like the following:

![](images/Figure-8.7.jpg)

**Figure 8.7:** Functioning of a Promise

Let's put the example at the beginning of this section into a code:

1.  `let ready = true;`

3.  `let promise = new Promise((resolve, reject) => {`
4.  `    setTimeout(() => {`
5.  `        if(ready) {`
6.  `            let details = {`
7.  `                location: 'Manchester Arena',`
8.  `                city: 'Manchester, UK',`
9.  `                date: '21/12/2020',`
10.  `                time: '17:00 CST'`
11.  `            };`
12.  `            resolve(details);`
13.  `        } else {`
14.  `            reject('Sorry, we will not be hosting any concerts this year.');`
15.  `        }`
16.  `    }, 2000);`
17.  `});`

19.  `promise.then((details) => {`
20.  `  console.log("Hooray! The concert is happening!");`
21.  `  console.log(details);`
22.  `})`
23.  `.catch((error) => {`
24.  `    console.log(error);`
25.  `})`

    **Code 8.9:** The concert example as a promise

As you can see in the preceding *[code example 8.9](#c08.xhtml_co8_9)*, the syntax is more structured and easier to read than callbacks. The *[code example 8.9](#c08.xhtml_co8_9)* can be divided into two parts. The lines of code from line number 3 to line number 18 define “*How to create a Promise?”,* and the lines of code from line number 19 to line number 25 show “*How to use a Promise?”.*

In the preceding *[code example 8.9](#c08.xhtml_co8_9)*, we have created a **`Promise`** object using the keyword **`new`**, and assigned it to the variable promise. Inside the Promise, we have mocked the asynchronous code using the **`setTimeout`** function as the executor and a timer of two seconds. Inside the executor, the code checks for the value of the variable ready. If the value of ready is true, it signifies that the request has been completed successfully; hence, we call the resolve callback. Inside the resolve callback, we pass the details of the next concert as an argument. However, if the value of ready is false, it signifies that the request failed and hence, we call the reject callback with the error message in the argument as '*Sorry, we will not be hosting any concerts this year*'.

As shown in the lines 19 to 25 of the *[code example 8.9](#c08.xhtml_co8_9)*, to use the **`Promise`**, we need to chain the **`.then()`** and **`.catch()`** method to the Promise. If the request has been completed successfully and the resolve callback has been called, it will execute the code inside the then method. If the request has failed and the callback has been called, it will execute the code inside the catch method.

Since we have supplied the value of the ready variable as true, the output of our code after waiting is as follows:

![](images/Figure-8.8.jpg)

**Figure 8.8:** Output of the [code example 8.9](#c08.xhtml_co8_9) if ready===true.

Similarly, if the variable ready was false, the output after waiting would have been the following:

![](images/Figure-8.9.jpg)

**Figure 8.9:** Output of the [code example 8.9](#c08.xhtml_co8_9) if ready===false.

This process can be visualized as follows:

![](images/Figure-8.10.jpg)

**Figure 8.10:** Process of promise

# [Chaining Promises](#toc.xhtml_s158a)

Now, that we have seen how to create and use Promises, let’s understand how we can solve the problem of callback hell using Promises.

Adding to the *[code example 8.9](#c08.xhtml_co8_9)*, we create another Promise:

1.  `const bookTicket = (date) => {`
2.  `return new Promise((resolve, reject) => {`
3.  ``    let message = `Book ticket for ${date}`;``
4.  `    resolve(message);`
5.  `  })`
6.  `}`

    **Code 8.10:** Creating a new promise

In the *[code example 8.10](#c08.xhtml_co8_10)*, we create a new function **`bookTicket`**. Inside **`bookTicket`**, we create a new **`Promise`**. In the executor of this Promise, we call the resolve callback with the variable message.

Next, we make a few changes to the original *[code example 8.9](#c08.xhtml_co8_9)*:

1.  `let response = promise.then((details) => {`
2.  `    console.log("Hooray! The concert is happening!");`
3.  `    console.log("Details:  ", details);`
4.  `    return bookTicket(details.date);`
5.  `})`
6.  `.catch((error) => {`
7.  `    console.log(error);`
8.  `})`

    **Code 8.11:** Adding the new promise to the then method of our promise

In the *[code example 8.11](#c08.xhtml_co8_11)*, we modify the code shown in the *[code example 8.9](#c08.xhtml_co8_9)* by adding the following two things:

*   First, we add the function **`bookTicket`** created in the *[code example 8.10](#c08.xhtml_co8_10)* to the then method of our Promise. Since we are passing the resolve of the message in the function **`bookTicket`**, we add return in front of function invocation of **`bookTicket`** inside the then method.
*   Second, we place the entire Promise resolution inside a variable response.

Finally, we add the Promise resolution methods **`.then()`** and **`.catch()`** to the variable response, holding the return of the new Promise created in *[code example 8.10](#c08.xhtml_co8_10)*.

1.  `response.then((details) => {`
2.  `    console.log(details);`
3.  `}).catch((error) => {`
4.  `    console.log(error);`
5.  `})`

    **Code 8.12:** Creating the promise resolution methods of the variable response

Adding all of the preceding codes, we get something like the following:

1.  `let ready = true;`

3.  `let promise = new Promise((resolve, reject) => {`
4.  `    setTimeout(() => {`
5.  `        if(ready) {`
6.  `            let details = {`
7.  `                location: 'Manchester Arena',`
8.  `                city: 'Manchester, UK',`
9.  `                date: '21/12/2020',`
10.  `                time: '17:00 CST'`
11.  `            };`
12.  `            resolve(details);`
13.  `        } else {`
14.  `            reject('Sorry, we will not be hosting any concerts this year.');`
15.  `        }`
16.  `    }, 2000);`
17.  `});`

19.  `const bookTicket = (date) => {`
20.  `return new Promise((resolve, reject) => {`
21.  ``   let message = `Book ticket for ${date}`;``
22.  `    resolve(message);`
23.  `  })`
24.  `}`

26.  `let response = promise.then((details) => {`
27.  `    console.log("Hooray! The concert is happening!");`
28.  `    console.log("Details:  ", details);`
29.  `    return bookTicket(details.date);`
30.  `})`
31.  `.catch((error) => {`
32.  `    console.log(error);`
33.  `})`

35.  `response.then((details) => {`
36.  `    console.log(details);`
37.  `}).catch((error) => {`
38.  `    console.log(error);`
39.  `})`

41.  `promise.then((details) => {`
42.  ``     console.log(`The concert is happening at ${details.location} in the city of ${details.city} on ${details.date} at ${details.time}.`)``
43.  `})`

    **Code 8.13:** Chaining promises

In the *[code example 8.13](#c08.xhtml_co8_13)*, we compile the code written in the *[code examples 8.9](#c08.xhtml_co8_9), [8.10](#c08.xhtml_co8_10), [8.11](#c08.xhtml_co8_11)*, and *[8.12](#c08.xhtml_co8_12)*. At the end, we add one more resolution method to the variable promise holding the Promise object we created in the *[code example 8.9](#c08.xhtml_co8_9)*.

When we execute the *[code example 8.13](#c08.xhtml_co8_13)*, the output is as follows:

![](images/Figure-8.11.jpg)

**Figure 8.11:** Output of the [code example 8.13](#c08.xhtml_co8_13)

The preceding screenshot shows the following:

*   Since the variable ready is true, the line numbers 27 and 28 in the *[code example 8.13](#c08.xhtml_co8_13)* are executed first.
*   On the line number 29, we call the **`bookTicket`** function.
*   However, we have another **`.then()`** method on the line number 41 of the *[code example 8.13](#c08.xhtml_co8_13)* for the first promise that we have created on the line number 3 of the *[code example 8.13](#c08.xhtml_co8_13)*. Hence, the code on the lines 41-43 is executed before the function **`bookTicket`** is executed.
*   Finally, the resolve value returned by the Promise inside the executor of the **`bookTicket`** function is stored in the value of the variable response. This causes the code on the line numbers 35-39 to be executed. Hence, we get the final response shown in *[figure 8.11](#c08.xhtml_fig8_11)*.

This is how we can chain multiple promises.

# [async and await](#toc.xhtml_s159a)

The keywords **`async`** and **`await`** are syntactic sugar for writing promises. They are used in conjunction.

# [async](#toc.xhtml_s160a)

An **`async`** function returns a Promise. If the **`async`** function returns a value, the Promise will be resolved with the value. However, if the **`async`** function throws an error, the Promise is rejected with that value. Let’s see an example of an **`async`** function:

1.  `async function eyeColor {`
2.  `    return "red";`
3.  `}`

    **Code 8.14:** An example of async method

The code shown in the *[code example 8.14](#c08.xhtml_co8_14)* is the same as the code shown in the *[code example 8.15](#c08.xhtml_co8_15)*:

1.  `function eyeColor {`
2.  `    return Promise.resolve("red");`
3.  `}`

    **Code 8.15:** An example of the promise

# [await](#toc.xhtml_s161a)

The keyword await is used only with an **`async`** function. If you use await with a **`non-async`** function, it will result in an error.

The await keyword ensures that all the promises wait for each other. If we use await, then we no longer need to use the **`.then()`** and the **`.catch()`** method. Instead, we need to use the traditional JavaScript try and catch methods. Let’s understand this with examples.

1.  `async function setName() {`
2.  `    let promise = new Promise((resolve, reject) => {`
3.  `        setTimeout(() => resolve("John Doe"), 2000);`
4.  `    })`

6.  `    let result = await promise;`

8.  `    console.log(result);`
9.  `}`
10.  `setName();` *`//John Doe`*

    **Code 8.16:** An example of the async and await

As shown in the *[code example 8.16](#c08.xhtml_co8_16)*, the line number 6 removes the dependency on the then and catch methods for a Promise. In the preceding example, we have successfully received the response for resolve. Now, let’s quickly look at an example of error handling using await.

1.  `async function error() {`
2.  `    await Promise.reject(new Error("This is an error!");`
3.  `}`

5.  `async function error() {`
6.  `    throw new Error("This is an error!");`
7.  `}`

    **Code 8.17:** Examples of await and error

In the preceding *[code example 8.17](#c08.xhtml_co8_17)*, both the codes are the same, and do the same thing. To handle errors with **`async`** and **`await`**, we need to use **`try`** and **`catch`**:

1.  `async function setName() {`
2.  `    try{`
3.  `        let promise = new Promise((resolve, reject) => {`
4.  `            setTimeout(() => reject("Error"), 2000);`
5.  `        })`

7.  `        let result = await promise;`
8.  `    }`
9.  `    catch(error) {`
10.  `        console.log(error);`
11.  `    }`

13.  `    console.log(result);`
14.  `}`

16.  `setName();` *`//Error`*

**Code 8.18:** Error handling with async and await

As shown in the *[code example 8.18](#c08.xhtml_co8_18)*, when the promise throws an error, it is caught in the catch. This is how we can deal with server requests and their errors.

# [Conclusion](#toc.xhtml_s162a)

In this chapter, we set the base for learning the APIs and the server requests in the next chapter. In this chapter, we explored the concept of asynchronous JavaScript. Asynchronous JavaScript is best used when the requests may take a long time to yield results, especially in the case of servers. To deal with asynchronous JavaScript, we then learned about callbacks. However, callbacks often result in a myriad problem called *Callback Hell*. To resolve this, we learned JavaScript Promises. In the next chapter, we will be working with actual APIs in real time; we will also learn AJAX, a method of Promise to deal with server requests.

# [Points to remember](#toc.xhtml_s163a)

*   There is no fixed time in which the servers can respond to a request. It depends heavily on the internet speed and the load capacity of the server. It’s unwise to let the execution of JavaScript be blocked by server requests. This process of deferring execution of code dependent on the server response, and allowing the remaining code to execute is called as **asynchronous JavaScript**.
*   Callbacks are best for dealing with short asynchronous requests. You can pass a callback function to a function dealing with asynchronous code. This callback function will be called only when the response of the server is received.
*   However, large number of requests does not work well with callbacks. It results in a disorganized mess, called the *Pyramid of Doom* or the *Callback Hell*.
*   Promises are a link between the code that takes time to produce something and the code that needs to consume the result of the producer code.
*   If the request works, the resolve callback is called, and if the request fails, the reject callback is called. If the resolve callback has been called, it will be accessible in the then method of the promise resolution. Similarly, the reject callback will be caught in the catch method of promise resolution.
*   Finally, async and await reduce the syntax of promises.

# [Multiple choice questions](#toc.xhtml_s164a)

1.  **The await keyword can be used without the async keyword – True or False?**
    1.  True
    2.  False
2.  **Which of the following is not a state of the promise?**
    1.  Pending.
    2.  Holding.
    3.  Fulfilled.
    4.  Rejected.

# [Answers](#toc.xhtml_s165a)

1.  **b**
2.  **b**

# [CHAPTER 9](#toc.xhtml_c09)

# [AJAX and Interacting with Servers](#toc.xhtml_c09)

To be honest, this chapter is perhaps the most significant one in the entire book. Let us understand this claim with a simple example. If you think about it for a moment, you will realize that every time you open a social media website, like Facebook, on your browser, the content is not always the same. You will see different content because every time you open Facebook, your browser sends several requests to the servers hosted by Facebook. The response to these requests renders the **user interface** (**UI**) that you see on your browser. In the mean real world out there, your work will significantly involve creating UI that is dependent on the data you receive from servers.

In this chapter, we will not only learn how to interact with servers (and all the hullaballoo associated with it), but also lay down the foundations for creating a live webpage using APIs in the next chapter! In this chapter, you will be learning about AJAX (a JavaScript process for connecting to the servers), JSON (the universal format for sending or receiving data from the servers), requests, responses, and understand the basics for creating a live application.

# [Structure](#toc.xhtml_s166a)

In this chapter, we will cover the following topics:

*   JSON – The Web’s favorite file format
*   AJAX
*   HTTP Headers

# [Objective](#toc.xhtml_s167a)

After studying this chapter, you should be able to interact with actual real-life servers (finally!). You can update UI efficiently using data received from the servers and send requests and receive responses safely across the internet

# [JSON – The Web’s favorite file format](#toc.xhtml_s168a)

In the introduction, we read about browsers exchanging data with the servers. In the simplest of imaginations, we can visualize this as follows:

![](images/Figure-9.1.jpg)

**Figure 9.1:** Graphical visualization of data exchange between browser and server

If you let your imaginations run wild, you can think of a hundred different formats for exchanging data between a browser sitting on a client machine and a server. However, imagine if the server has to send a 400MB video as a response over the internet. Even with the best internet speeds, it's fair to say the user would be bored to death waiting for the browser to receive this video as the server response. To add to that, imagine if your JavaScript is not asynchronous! It would mean your user will see nothing but a blank screen or a loading icon until the video ultimately reaches the browser. (It could take more than half-hour on slow networks!)

![](images/Figure-9.2.jpg)

**Figure 9.2:** When disappointment strikes.

Therefore, for simplicity, browsers exchange data in text format. It is simple and fairly lightweight.

**Tip: A potential next question could be**: How will you show videos or images that reside on the server? While there are several answers to this question, one of the best answers is a relative path to the image/video stored in the server. In this scenario, we store the media files like the images and the videos inside a folder residing on the server. In the server response, the browser only receives the relative path to that image/video. Using that path in the `<img>` or the `<video>` tag, it will show the respective image/video without having the user waste several bytes of data to download it.

In *[Chapter 5: Objects](#c05.xhtml)*, we learned that objects are a brilliant way of emulating real-life data. It means if you want to send multiple information about a specific object like a car, a person or quite literally anything, you can store all that information inside a simple object.

Combining the best of both the worlds of text and objects, JavaScript introduced a new format called **JavaScript Object Notation** (**JSON**).

Officially, according to the **Mozilla Developer Network** (**MDN**) docs, **JavaScript Object Notation** (**JSON**) is a standard text-based format for representing structured data based on JavaScript object syntax.

In its simplest form, JSON is a string that resembles the JavaScript object. It can also be used independently from JavaScript. In fact, several programming environments have the ability to read and generate JSON. You can also store JSON as a file. JSON files must be saved with the extension **`. json`**.

# [Structure of JSON](#toc.xhtml_s169a)

As mentioned earlier, the JSON object bores a marked resemblance to the JavaScript object. Without much further ado, let's quickly take a look at the structure of a JSON object.

1.  `"{`
2.  `     "firstName":"John",`
3.  `     "lastName":"Doe",`
4.  `     "address": {`
5.  `          "building":"River View Apartments",`
6.  `          "apartment":12,`
7.  `          "road":"York Road",`
8.  `          "city":"London",`
9.  `          "country":"England"`
10.  `    },`
11.  `    "cars": ["BMW","Audi","Jaguar"]`
12.  `}"`

    **Code 9.1:** Syntax of JSON Object

As you can see in the *[code example 9.1](#c09.xhtml_co9_1)*, the JSON object is remarkably similar to the JavaScript object literal. Just like the JavaScript object literal, the data inside a JSON object is in key: value pairs and separated by commas. Similarly, objects (like address in the *[code example 9.1](#c09.xhtml_co9_1)*) and arrays (like cars in the *[code example 9.1](#c09.xhtml_co9_1)*) are denoted using the curly braces and square bracket notation, respectively. Also, as per the JavaScript standards, the JSON value having number as a data type should not be in quotes.

However, there are some significant differences between a JSON object and a JavaScript object literal:

*   In the JSON objects, every key in the *key: value* pair needs to be in double-quotes.
*   The JSON values cannot be a function, a date, or undefined.
*   You *cannot* use single quotes for JSON keys or values.

JSON works in two formats:

*   **String**: When data needs to be transmitted.
*   **Object**: When you need to access the data.

JavaScript provides a global JSON object that helps in converting JSON from one form to another. We will understand both the formats in the next section.

# [Working with JSON](#toc.xhtml_s170a)

Now that we have a fair understanding of the structure of a JSON, and we know that JSON exists in two different forms, let's underline the process for working with JSON.

We know that the best format for data exchange between browsers and servers is the text format. However, once we receive the data on our browsers from the servers in the text format, we need to convert the text format to an object format for accessing the data. The global JSON object of JavaScript provides two methods for easy conversion between the two formats.

# [JSON.stringify()](#toc.xhtml_s171a)

To convert a JavaScript object into a text format to be sent across the internet, JavaScript provides a JSON method called **`JSON.stringify()`**. All we need to do is provide the object inside the parentheses of the **`JSON.stringify()`** method. Let’s understand this with an example.

1.  `let obj = {`
2.  `    firstName: "John",`
3.  `    lastName: "Doe",`
4.  `    address: {`
5.  `        building: "River View Apartments",`
6.  `        apartment: 12,`
7.  `        road: "York Road",`
8.  `        city: "London",`
9.  `        country: "England"`
10.  `    },`
11.  `    cars: ["BMW", "Audi", "Jaguar"]`
12.  `}`

14.  `JSON.stringify(obj);`

    **Code 9.2:** JSON.stringify() method

As you can see in the *[code example 9.2](#c09.xhtml_co9_2)*, we have a JavaScript object **`person`**. To convert this to a JSON string, we need to pass the object person inside the parentheses of the method **`JSON.stringify()`**. When you execute the *[code example 9.2](#c09.xhtml_co9_2)*, the results would look something like the following:

![](images/Figure-9.3.jpg)

**Figure 9.3:** Output of [code example 9.2](#c09.xhtml_co9_2)

As you can see in the preceding screenshot, the output of line number 14 of the *[code example 9.2](#c09.xhtml_co9_2)* is a JSON string. If you observe *[figure 9.3](#c09.xhtml_fig9_3)* closely, you can see that the object person of the *[code example 9.2](#c09.xhtml_co9_2)* has been converted to the JSON format in *[figure 9.3](#c09.xhtml_fig9_3)*. The keys of the object person are now encased in double-quotes, as per the JSON format. In fact, the output itself is printed inside double quotes. If you use the JavaScript operator **`typeof`** in front of this output, you will receive the output as a string, as shown in the following screenshot:

![](images/Figure-9.4.jpg)

**Figure 9.4:** The data type of the output of the stringify method

# [JSON.parse()](#toc.xhtml_s172a)

In the previous section, we learned how to convert a JavaScript object to a JSON string. Now, we also need to understand how to convert a JSON string received from the server to a JavaScript object that we can use in our web application. To convert a JSON string to a JavaScript object, JavaScript provides us with the method **`JSON.parse()`**. Similar to the **`JSON.stringify()`** method, we need to pass the JSON string inside the parentheses of the **`JSON.parse()`** method. Let’s look at an example.

![](images/Figure-9.5.jpg)

**Figure 9.5:** An example of JSON.parse()

As shown in the preceding screenshot, we have used a JSON text (the one that we have received as the output in *[figure 9.3](#c09.xhtml_fig9_3)*) and supplied it to the **`JSON.parse()`** method. As you can see, the output of the **`JSON.parse()`** method is a JavaScript object, denoted by the absence of the double-quotes.

# [Exchanging data](#toc.xhtml_s173a)

In the previous sections, we saw the process of converting JSON from one form to another. Moreover, we also understood when to use JSON as a string, and when to use it as a JavaScript object. With these points in mind, let's look at the process of exchanging data between a browser sitting on a client machine and a server with the help of a diagram:

![](images/Figure-9.6.jpg)

**Figure 9.6:** An example of JSON.parse()

As shown in the preceding screenshot, when the client browser is sending data across the internet, it uses **`JSON.stringify()`** to convert the JavaScript object into a JSON text. Similarly, when the client browser receives data from the server in a JSON text, it uses **`JSON.parse()`** to convert the text to a JavaScript object.

# [AJAX](#toc.xhtml_s174a)

Now that we have read about the format used for exchanging data between the servers, let's finally learn how to interact with servers.

AJAX is the JavaScript process of connecting to the servers. It stands for Asynchronous JavaScript and XML.

AJAX is a web developer's dream. It not only enables sending and receiving data from the servers, but it also updates a web page without reloading.

However, before we understand AJAX and learn the simple four-step process of AJAX to interact with a server, we need to take a quick pitstop, and first need to understand a protocol involved in the exchange of data between servers and clients.

# [HTTP](#toc.xhtml_s175a)

The protocol or the system of rules that we use in web development for the exchange of data is the **Hypertext Transfer Protocol** (**HTTP**). The HTTP works in a simple request-response fashion that we have seen earlier in this chapter. The logic is as follows:

![](images/Figure-9.7.jpg)

**Figure 9.7:** The logic of HTTP

As shown in the preceding screenshot, the client browser sends a request to the server. The client browser can request several things from the server. It includes, but is not limited to, HTML file for showing on the browser, media like images, and videos, fonts, and data like objects and arrays (as we have seen in JSON). In fact, at times, the client browser can even send a request for updating the data stored in the server. The server receives this request, parses it, and sends a response back to the client. In response, the server always sends information about the status of the request. In addition to that, the server also sends data in the response if the browser has requested it.

Let's first explore the various methods of requests.

# [HTTP Methods](#toc.xhtml_s176a)

There are several HTTP methods - **`GET`**,**`POST`**,**`PUT`**,**`PATCH`**,**`DELETE`**,**`HEAD`**, and **`OPTIONS`**. Each of these methods caters to a different need. However, the most commonly used methods are **`GET`** and **`POST`**.

Let's go through each of the HTTP methods one by one:

# [GET](#toc.xhtml_s177a)

The GET method is used for requesting data from a specified resource. An example of this would be requesting an HTML file or the list of employees from a server.

However, we need to be aware of several pointers when using the GET method:

*   The GET method should be used only for requesting the data. It should *not* be used for modifying the data.
*   If we need to send data as a part of the **`GET`** request, it will be sent in the URL of the request. An example of this is to send the bank account details of a user for fetching the transaction details of the user. Therefore, it is advisable to not use **`GET`** requests when you need to send sensitive data in the requests.
*   The **`GET`** requests can be cached and bookmarked. They remain in the browser history.
*   The **`GET`** requests have restrictions on the length of the data.

# [POST](#toc.xhtml_s178a)

The **`POST`** method is specifically used for sending data to a server. Its primary purpose is to create the data on the server. A few additional points on the **`POST`** request are as follows:

*   The data sent in a **`POST`** request is stored in the request body of the **`HTTP`** request.
*   The **`POST`** requests are neither cached nor bookmarked. They do not remain in the browser history.
*   The **`POST`** requests do not have any restriction on the length of the data.
*   Sending a **`POST`** request will create a new resource on the server.

# [PUT](#toc.xhtml_s179a)

The **`PUT`** method is also used for sending data to a server. Like **`POST`**, its primary purpose is to create and also, update the data on the server. There are the following two major differences between **`POST`** and **`PUT`**:

*   **Exact URI**: PUT requests need to know the exact URI of the resource while **`POST`** does not mandatorily require the entire URI.

    For example, let’s imagine we have a URI for a list of employees on the server, and it is **`/employees`**. It means that if you send a **`POST`** request to the URI **`/employees`** with the data of the new employee, it can create a new **`employee`** on the server and assign it a unique ID. For the sake of understanding the example, let’s imagine that this employee has been assigned the **`ID 423`**. Alternatively, we can also create the new user on the server by sending data as a **`POST`** request specifically to **`/employees/423`**. If no IDs are provided, the **`POST`** request will automatically generate a new ID for the new data. This shows that the **`POST`** request does not necessarily need a complete URI to work.

    However, if you are sending a PUT request to **`/employees`** with the data of the new employee, it will fail. As mentioned before, the **`PUT`** request needs to know the exact URI to work. Therefore, if you send a PUT request to the **`/employees/423`**, it will either create a new employee if the ID 423 does not exist or it will replace the employee at the ID 423.

    |  | **POST** | **PUT** |
    | **`/employees/`** | ![](images/Image54833.jpg) | ![](images/Image54841.jpg) |
    | **`/employees/123/`** | ![](images/Image54849.jpg) | ![](images/Image54849.jpg) |

    **Table 9.1:** POST vs PUT

*   **Idempotence**: Probably, one of the most significant reasons for working with **PUT** over **`POST`** is the property of idempotence. It means that if you accidentally or deliberately send the **`POST`** request N times to the server with the same data, it will create N different resources on the server. However, if you accidentally or deliberately send the **`PUT`** request N times to the server with the same data, it will be equivalent to a single request modification.

# [PATCH](#toc.xhtml_s180a)

The **`PATCH`** request is useful for the scenarios where we wish to make a partial update to the resource stored in the server. For instance, let’s say we have a resource on the server that looks like the following:

1.  `{`
2.  `    firstName: 'John',`
3.  `    lastName: 'Doe',`
4.  `    age: 24,`
5.  `    location: 'Detroit'`
6.  `}`

    **Code 9.3:** A resource on the server

Let’s say we wish to change the location of the resource shown in the *[code example 9.3](#c09.xhtml_co9_3)*. If we send a **`PUT`** request with the data **`{location: 'New York'}`**, it will replace the entire object with the location as New York. It’s because, for the **`PUT`** request, we require the entire resource. If we want to send only one part of the resource to be modified, we need to use the **`PATCH`** request.

Therefore, when we send a **`PATCH`** request with the data **`{location: 'New York'}`**, it will update the resource as the following:

1.  `{`
2.  `    firstName: 'John',`
3.  `    lastName: 'Doe',`
4.  `    age: 24,`
5.  `    location: 'New York'`
6.  `}`

    **Code 9.4:** The resource after the PATCH request

To simplify understanding **`POST`** vs **`PUT`** vs **`PATCH`**, refer to the following diagram:

![](images/Figure-9.8.jpg)

**Figure 9.8:** POST vs PUT vs PATCH

# [DELETE](#toc.xhtml_s181a)

The **`DELETE`** method deletes the specified resource.

# [HEAD](#toc.xhtml_s182a)

The **`HEAD`** method is similar to the **`GET`** method, but it does not return a body in the response. It means if you send a **`GET`** request to the URI **`/employees`**, you will get a list of employees in the response. However, if you send a **`HEAD`** request to the same URI, it will not return the list of employees. **`HEAD`** methods are extremely useful for checking what a **`GET`** request will return. It’s run before making the actual **`GET`** request.

# [OPTIONS](#toc.xhtml_s183a)

The **`OPTIONS`** request is used for requesting information about the communication options for the target resource. For example, if we want to know what request methods are allowed for a particular URI, we can use **`OPTIONS`** to fetch that information.

# [HTTP status messages](#toc.xhtml_s184a)

In the introduction of the section – HTTP Methods, we learned that the server always returns the status of the request. As we will see in the next topic – The Process of AJAX, the status responses are useful to understand what happened to our requests at the server.

For instance, if you open **https://www.google.com** on your Google Chrome browser, and open the **`Network`** tab of your Chrome Developer Tools, you will see the first request titled **`www.google.com`**. As shown in the following screenshot, if you look at the **`Headers`** tab, you will see a key aptly called **Status Code**.

![](images/Figure-9.9.jpg)

**Figure 9.9:** The status code shown in Network tab of Chrome Developer Tools

The status messages come in two parts – a status code and a status message. The first digit of the status code defines a category of the status message. You can see the entire list of status messages here – **[https://developer.mozilla.org/en-US/docs/Web/HTTP/Status](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)**.

For the sake of understanding, we will look at a few of the significant status codes in every category that are used frequently in web development:

# [1xx: Information](#toc.xhtml_s185a)

Status code beginning with 1 are informational in nature. For example, the status code 100 has the status message as Continue. It means the server has received the request headers, and it informs the client to proceed to send the body of the request.

# [2xx: Successful](#toc.xhtml_s186a)

Status codes beginning with 2 are successful in nature. In *[figure 9.9](#c09.xhtml_fig9_9)*, we have seen the status code 200, which signifies that the request has been successful. A few of the commonly used status codes starting with 2 are listed as follows:

| **Status Code** | **Status Message** | **Description** |
| 200 | OK | The standard response for successful requests. |
| 201 | Created | A new resource has been created. |

**Table 9.2:** Codes beginning with 2

# [3xx: Redirection](#toc.xhtml_s187a)

Status codes beginning with 3 denote redirection. It means the URL you accessed has been moved, or you have been redirected to another location. A few of the commonly used status codes that begin with 3 are as follows:

| **Status Code** | **Status Message** | **Description** |
| 301 | Moved Permanently | The requested page or resource has been moved to a new URL. |
| 302 | Found | The requested page or resource has been temporarily moved to a new URL. |

**Table 9.3:** Codes beginning with 3

# [4xx: Client Error](#toc.xhtml_s188a)

One of the most commonly seen status codes are the ones that begin with 4\. It denotes error from the client browser or the client machine. A few of the commonly seen 4xx status codes are as follows:

| **Status Code** | **Status Message** | **Description** |
| 400 | Bad Request | Request cannot be fulfilled because of a bad syntax. |
| 401 | Unauthorized | The request was legal, but the server refuses to respond. This happens commonly when the authentication has not yet been provided. |
| 403 | Forbidden | The server does not allow this request. |
| 404 | Not Found | The requested page or resource could not be found. |

**Table 9.4:** Codes beginning with 4

# [5xx: Client Error](#toc.xhtml_s189a)

Finally, the status code beginning with 5 refer to errors happening on the server. A few of the commonly seen 5xx status codes are as follows:

| **Status Code** | **Status Message** | **Description** |
| 500 | Internal Server Error | A generic server error message. |
| 501 | Not Implemented | Server does not recognize the request or lacks the ability to complete the request. |
| 502 | Bad Gateway | The server was acting as a proxy/gateway and it received an invalid response. |
| 503 | Service Unavailable | The server is unavailable. |

**Table 9.5:** Codes beginning with 5

We will be using these status codes in the next topic – The Process of AJAX.\

# [The Process of AJAX](#toc.xhtml_s190a)

Finally, now that we have updated our knowledge with almost every pre-requisite information necessary for implementing AJAX, let’s begin learning the process of AJAX.

There are four simple steps for working with AJAX, which are as follows:

![](images/Figure-9.10.jpg)

**Figure 9.10:** The process of AJAX

As shown in the preceding screenshot, the process of AJAX involves the following four basic steps:

1.  **Create Request**: As basic as it sounds, the very first step in the process of AJAX is to create a request that needs to be sent to the server. The foundation of the entire AJAX process is the **`XMLHttpRequest`** object.

    **Note:** To break it down, XML stands for Extensible Markup Language. It is a markup language like HTML that uses tags to define elements within a document.

    HTTP stands for Hypertext Transfer Protocol, the topic we learned in the previous section.

    The **`XMLHttpRequest`** object is used for exchanging data with a web server behind the scenes. All the modern browsers at the time of writing (including Google Chrome, Mozilla Firefox, Microsoft Internet Explorer 7+, Microsoft Edge, Safari, Opera) support the **`XMLHttpRequest`** object.

    The syntax for creating a **`XMLHttpRequest`** is as follows:

    `let request = new XMLHttpRequest();`

    **Code 9.5:** Creating a request

    As shown in the *[code example 9.5](#c09.xhtml_co9_5)*, to create a **`XMLHttpRequest`** object, we need to use the JavaScript keyword new. Since we need to use this request often, it’s wise to store the request in a variable.

2.  **Open Request**: After creating the request, the next step is to open that request. Now, this is the most vital step in the process of AJAX. In this step, we need to provide the URL of the server that we intend to connect with our webpage/web application. Moreover, we also need to specify the method or type of request, whether this request will be asynchronous, and whether we need a username and a password.

    The general verbose syntax for opening a request is as follows:

    `open(`*`method`*`,` *`url`*`, async,` *`username`*`,` *`password`*`)`

    **Code 9.6:** Syntax of opening a request

    As shown in the preceding *[code example 9.6](#c09.xhtml_co9_6)*, the open method takes five parameters. However, the last three options are optional. Let’s understand each parameter one by one.

    **Method**: The very first parameter is the method parameter. The method parameter helps the server understand the type of request made by the client browser. In the section –HTTP Methods, we had a look at the several methods of an HTTP request. We can add any one of those methods as the first parameter to the open method.

    **URL**: The second parameter to the open method is the URL of the server. This URL can be an API endpoint or a location on the server. We will be looking at the APIs in more detail in the next chapter. Alternatively, it can also be the location of a file on the server. Generally, these files can perform actions on the server before sending back the response.

    **Asynchronous**: The third parameter is an optional parameter to set whether the request is asynchronous. It's a boolean value – so you can either send true or false as the third parameter to the open method. As we already know the meaning of asynchronous from the last chapter, setting the third parameter as true will not make JavaScript stop the execution, and wait for the response of this request. Instead, JavaScript will continue its execution and the user interaction until the server response arrives. However, if the third parameter is set to false, JavaScript will stop all its execution until the response of this request is received. Its default value is true.

    **Username and Password**: The fourth and the fifth parameters are also optional. The fourth and the fifth parameters are for username and password, respectively. They can be used for authentication purposes. Their default values are null.

    Continuing our *[code example 9.6](#c09.xhtml_co9_6)*, let’s try the open method with an actual API request:

    `request.open('GET', 'https://www.themealdb.com/api/json/v1/1/search.php?s=Arrabiata', true);`

    **Code 9.7:** An example of opening a request

    In preceding *[code example 9.7](#c09.xhtml_co9_7)*, we have used the variable request that we have created in *[code example 9.5](#c09.xhtml_co9_5)*. We invoke the open method on the variable request and pass three parameters to it. The first parameter should be the type of HTTP request. Therefore, we have added the '**`GET`**' method as the first parameter. For the second parameter that should be a URL, we have added an API of a popular public API platform called The Meal DB. Finally, we have added the optional third parameter for asynchronous behavior as true. We do not need the optional fourth and fifth parameters.

3.  **Send Request**: The third step in the process of AJAX is to send the request that we have created in the first two steps. The syntax for sending a request is **`request.send()`** in case of **`GET`** requests, and **`request.send(str)`** in case of **`POST`** requests. Continuing the example used in *[code examples 9.5](#c09.xhtml_co9_5)* and *[9.7](#c09.xhtml_co9_7)*, we will now send the following request:

    `request.send();`

    **Code 9.8:** Sending a request

    As shown in *[code example 9.8](#c09.xhtml_co9_8)*, since the **`XMLHttpRequest`** that we have created earlier is a **`GET`** method, we will invoke the send method without any parameters.

4.  **Wait for the response**: With the first three steps, we have completed creating, opening, and sending the request to a server. The server now parses the request, prepares a response, and returns the response to the client. To understand the response, and how to receive it, we first need to understand a concept called **`readyState`**.

    The **`readyState`** property belongs to the **`XMLHttpRequest`** object. It holds the state of the **`XMLHttpRequest`** client. There are five values of the **`readyState`** property:

    | **Value** | **State** | **Description** |
    | 0 | UNSENT | The client has been created. When we complete the first step of the AJAX process, the value of the `readyState` becomes 0. |
    | 1 | OPENED | The `open()` method has been invoked. When we complete the second step of the AJAX process, the value of the `readyState` becomes 1. |
    | 2 | HEADERS_RECEIVED | The send() method has been invoked. When we complete the third step of the AJAX process, the value of the readyState becomes 2\. At this point, the response headers have been received. |
    | 3 | LOADING | The response’s body is being received. |
    | 4 | DONE | The operation is complete. It means either the data transfer has been successful or failed. |

    **Table 9.6:** Values of readyState

    As we can see in *[table 9.6](#c09.xhtml_tab9_6)*, the values of the property **`readyState`** changes with every action or every step of the AJAX process. Moreover, from *[table 9.6](#c09.xhtml_tab9_6)*, we can see that when the value of **`readyState`** denotes 4, it signifies that the process of interaction with the server is complete.

    The **`XMLHttpRequest`** object contains a property called **`onreadystatechange`**. Every time the value of the **`readyState`** property changes, the event handler inside the **`onreadystatechange`** property is called. Let’s try understanding the **`onreadystatechange`** property with an example:

    1.  `request.onreadystatechange = function() {`
    2.  `    if(this.readyState === 4 && this.status === 200) {`
    3.  `        console.log(this.responseText);`
    4.  `    }`
    5.  `}`

        **Code 9.9:** An example of the onreadystatechange property

    In *[code example 9.9](#c09.xhtml_co9_9)*, we have continued using the variable request that we have created and used in *[code examples 9.5](#c09.xhtml_co9_5)*, *[9.7](#c09.xhtml_co9_7)*, and *[9.8](#c09.xhtml_co9_8)*. As you can see in *[code example 9.9](#c09.xhtml_co9_9)*, we have attached a function for listening to the event when the **`readyState`** property of the variable request changes. Inside the function, we check for the condition whether the **`readyState`** property is 4 and the status of the response is 200\. As we have seen in *[tables 9.2](#c09.xhtml_tab9_2)* and *[9.6](#c09.xhtml_tab9_6)*, the **`readyState`** property is 4 when the entire operation of request and response has been completed. Similarly, the status of the request becomes 200 when the request has been successful. To sum it up, it means that our request to the sever has completed and it has been successful. When the two conditions are met, we execute the statement to log the **`responseText`**. The property **`responseText`** returns the text received from the server.

    Combining our entire code, it looks like the following:

    1.  `let request = new XMLHttpRequest();`
    2.  `request.open('GET', 'https://www.themealdb.com/api/json/v1/1/search.php?s=Arrabiata', true);`
    3.  `request.send();`
    4.  `request.onreadystatechange = function() {`
    5.  `    if(this.readyState === 4 && this.status === 200) {`
    6.  `        console.log(this.responseText);`
    7.  `    }`
    8.  `}`

        **Code 9.10:** The complete process of AJAX

As you can see from *[code example 9.10](#c09.xhtml_co9_10)*, it’s fairly easy to create and send a request to the server. Also, we have limitless opportunities to deal with the server responses. Instead of the **`console.log`** statement, we can also include a callback function to deal with the successful response. Alternatively, if the request fails and we get a status starting with 4 or 5, we can include another condition to deal with the failed requests. In fact, we can also execute special code for situations where we want to execute something before the request is sent or during the loading of the request.

# [HTTP Headers](#toc.xhtml_s191a)

In the previous section, we successfully completed an interaction with a public API server. Let's have a quick look at the Network Panel of our Chrome Developer Tools to see the request in action.

To achieve this, let’s create a small project. On a favorable location on your machine, create a folder and name it *'Nom Nom'*. This will be the name of our simple application. You are free to choose whatever name you’d like to give to this project. Inside this folder, create an HTML file called **`index.html`**. The following is what our simple HTML file would look like:

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `<head>`
4.  `    <meta charset="UTF-8">`
5.  `    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
6.  `    <title>Nom Nom</title>`
7.  `</head>`
8.  `<body>`
9.  `    <div>`
10.  `        <h1>Welcome to Nom Nom</h1>`
11.  `        <h5>The best place to learn mouth-watering recipes!</h5>`
12.  `    </div>`
13.  `    <script src="scripts/index.js"></script>`
14.  `</body>`
15.  `</html>`

    **Code 9.11:** The index.html file

Now, we will create a folder on the same level as the **`index.html`** file and name it as scripts. You can visualize this as follows:

![](images/Figure-9.11.jpg)

**Figure 9.11:** The folder structure for Nom Nom

Inside the scripts folder, we will create a JavaScript file and name it **`index.js`**. Inside **`index.js`**, we will paste the code that we have seen in *[code example 9.10](#c09.xhtml_co9_10)*.

When you click on the **`index.html`** file inside the folder **`Nom Nom`**, it will open up our web page on the default browser of your machine. Since I constantly use Google Chrome for development, the default browser on my machine is Google Chrome. After clicking on **`index.html`**, our web page will look like the following on the browser:

![](images/Figure-9.12.jpg)

**Figure 9.12:** The web page of Nom Nom

As we had learned in *[Chapter 2: The Developer’s Tools](#c02.xhtml)*, we can open the Chrome Developer Tools by pressing right-click on any part of the web page inside the browser and clicking on **`Inspect`**. From there, we can navigate to the **`Network`** panel by clicking on the **`Network`** tab at the top of the Developer Tools. When you complete this, you will see something like the following:

![](images/Figure-9.13.jpg)

**Figure 9.13:** View of the Network Panel of the Chrome Developer Tools

As you can see in the preceding screenshot, when you open the **`Network`** panel for the first time, it’s blank. In fact, it asks us to perform a request or hit refresh. So, let’s go ahead and refresh the page by pressing the shortcut key *F5* on your machine, or by clicking on the ![](images/Image55092.jpg) button next to the address bar of your browser.

When you hit refresh, you will see three requests populated on your **`Network`** panel, as shown in the following screenshot. If you hover on each of the items in the **`Name`** column, you will notice that the three items are the requests for index.html, index.js, and finally, our server API request.

![](images/Figure-9.14.jpg)

**Figure 9.14:** Requests shown in Network Panel

If we click on the last request shown in *[figure 9.14](#c09.xhtml_fig9_14)*, it will reveal a sidebar next to the **`Name`** column of the requests. Based on your history of working with the **`Network`** panel, the sidebar might open up on any of the tabs shown in the following screenshot. However, it’s very likely that if you are opening it for the first time, it might open up on the **`Preview`** tab:

![](images/Figure-9.15.jpg)

**Figure 9.15:** The Preview tab of the sidebar on Network Panel

As shown in the preceding screenshot, the **`Preview`** tab shows you a preview of the response sent by the server to our request. As you can see, for the API GET request **[https://www.themealdb.com/api/json/v1/1/search.php?s=Arrabiata](https://www.themealdb.com/api/json/v1/1/search.php?s=Arrabiata)**, the server responds with an object pertaining to the dish 'Spicy Arrabiata Penne'. However, as we have seen earlier in this chapter, the server does not send an object as a response across the internet. In fact, it sends a JSON string as a response. If you move to the **`Response`** tab of the sidebar inside the **`Network`** panel, you will see the actual response sent by the server. The Chrome Developer Tools basically detect and convert the JSON string into an object for the Preview tab, so that it becomes easier for the developers to comprehend the response.

In this section, we will be concentrating on the **`Headers`** tab of the sidebar in the **`Network`** panel. So, if you move to the **`Headers`** tab on the sidebar inside the **`Networks`** panel, you will see something like the following:

![](images/Figure-9.16.jpg)

**Figure 9.16:** The Headers tab of the sidebar on Network Panel

If you scroll down the **`Headers`** tab, you will see four different sections. They are titled General, Response Headers, Request Headers, and Query String Parameters. So, what exactly are headers?

HTTP Headers let both the client and the server send additional information with the request or the response. The HTTP Headers consist of a case-insensitive name followed by its value. The HTTP headers can be grouped into four different categories:

*   **General Headers**: These headers are applicable to both the request sent by the client and the response sent by the server. However, they are not related to the data inside the body or the content of the request or the response. The most common general headers are Date (it contains the date and time at which the message was originated), Cache-Control (it holds instructions for caching both requests and responses), or Connection (it specifies whether the connection should remain open after the current transaction finishes), and so on.
*   **Request Headers**: These headers are applicable in the HTTP request, but they are not related to the content of the request. These requests send additional information about the request, so that it becomes easier for the server to send the accurate response. The request headers like Accept, Accept-* or If-* (where * denotes that it can be replaced by another keyword) are useful for adding conditions to the request. For example, Accept informs the server about the types of data that the server can send back. Similarly, Accept-Language informs the server about the languages that will be acceptable when the server sends the response. Apart from the conditional requests, you also have headers like User-Agent (which informs the server about operating system, software vendor, software version, and so on), Cache-Control (which informs the server about the cache policies of the response), Referer (which informs about the previous web page which called this web page), and so on.
*   **Response Headers**: Response headers are used in HTTP response, and they are not related to the content of the message. They are useful for giving more details about the response.

    A few of the response headers include Age (which conveys the time since the client requested the server), Retry-After (which can be used to indicate the client how long the service is expected to be unavailable), Set-Cookie (it contains a name-value pair of information to retain for this particular URL), and so on.

*   **Entity Headers**: Entity headers contain information about the body of the resource. Commonly used entity headers include Content-Length (the size of the resource in bytes), Content-Type (the media type of the resource, also known as MIME type), Content-Encoding (the compression algorithm for the resource), Content-Language (the human language intended for the audience), and so on. Entity Headers do not form a separate column on the **`Headers`** tab inside the **`Network`** panel. They are distributed amongst the **`Request`** and **`Response`** headers.

The Query String Parameters section that you see in the **`Headers`** tab on sending the request to the MealDB API server is the string attached to the end of the GET request. As we have read in the previous section, GET requests append additional information that needs to be sent to the server, to the URL of the request (hence, it is not safe!). Whenever a set of information is to be appended to a request, it can be achieved by adding the string after appending a question mark (?) to the end of the request URL.

![](images/Figure-9.17.jpg)

**Figure 9.17:** The Request URL of the API shows the Query String Parameters

As we can see in the preceding screenshot, the Request URL that should end at **`search.php`**, contains an extra string ?s=Arrabiata. The string **`s=Arrabiata`** helps the server to filter and send all the recipes which have the name *Arrabiata* in the title. Whenever we need to add such a string to the URL, we first need to append a question mark symbol (?) at the end of the URL. This question mark symbol denotes that we are sending additional data to the server for a **`GET`** request. Then, the actual string(s) need to be added in the key=value format after the question mark. In case of multiple strings, we need to use the ampersand (&) symbol to separate the multiple strings. This addition to the URL is called as a *query string*.

For the sake of sanity, we have not printed the entire list of the header requests in this book. If you wish to have a look at the entire list of HTTP headers, you can check it out on the official MDN docs here – **[https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)**.

If you look at the brief list of HTTP headers shared before *[figure 9.17](#c09.xhtml_fig9_17),* or the complete list shown in the preceding link shared, you will figure that there might be several scenarios where you will need to send headers in the request. For instance, if you want to inform the server to send you the response only in particular formats, you will need to send the required extensions to the server. As we have seen in the preceding list shared, you will have to specify the required formats in the Accept header while sending the request to the server. For such instances, AJAX provides a method called **`setRequestHeader()`**.

# [setRequestHeader()](#toc.xhtml_s192a)

The **`XMLHttpRequest`** method **`setRequestHeader()`** sets the value of a HTTP Request Header. This method should be called only after you have opened a request, and before sending a request, as shown in the following screenshot:

![](images/Figure-9.18.jpg)

**Figure 9.18:** The exact moment when you should call setRequestHeader

If this method is called several times with the same header, the values are merged into one single request header. In *[figure 9.18](#c09.xhtml_fig9_18)*, we have specifically set the request header to accept only responses with the format '**`application/json`**'. If the **`Accept`** header is not set, the default value '*/*' is sent.

# [Conclusion](#toc.xhtml_s193a)

In this chapter, we explored and learned how to interact with a server using APIs. We started this chapter by understanding JSON – the format used for exchanging data across the internet. We applied this knowledge of JSON and its methods in the next section, AJAX, and the process of AJAX. In that section, we tried out a live example with a public API of the MealDB platform. However, before that, we familiarized ourselves with the different HTTP methods and the status codes. Finally, at the end of this chapter, we studied the various HTTP Headers. Everything that we have learned in this chapter, along with the knowledge of the past eight chapters, will help us in creating a live application in the next chapter.

In the next chapter, we will be using the APIs of the MealDB platform to create a web application for showing recipes. Here, we will not just write the code for creating the web application, but also look at the several non-technical aspects of creating an application, like how to zero in on the idea, looking at the target users, how to calculate the number of pages, and what needs to be done after the application has been created.

# [Points to remember](#toc.xhtml_s194a)

*   For the sake of faster exchange and simplicity, data is sent across the internet between different entities in text format. **JavaScript Object Notation** (**JSON**) is the standard text-based format representing a JavaScript object syntax. It is used for exchanging data across the internet.
*   The JSON and a JavaScript object literal are similar but not the same. Unlike the JavaScript object literal, you cannot use single quotes in JSON. Similarly, all the keys in JSON need to be wrapped in double quotes, and you cannot have functions, dates or undefined values for the JSON values.
*   For web development, we use a protocol called **Hypertext Transfer Protocol** (**HTTP**) for exchanging data between clients (browsers) and servers. There are several HTTP methods for exchanging data with the servers, based on the requirements. The **`GET`** and the **`POST`** requests are more commonly used.
*   The server always sends a status response to a request. Even if the request has failed, a status message is always returned to the client.
*   Asynchronous JavaScript and XML (AJAX) is the standard process for interacting with servers. It uses a JavaScript object **`XMLHttpRequest`** for creating, opening, sending, and receiving a response.
*   The benefit of using AJAX is that the rendering of the web page is not affected by the interaction with servers. In fact, even if a part of the UI needs to be changed, the browser does not need to refresh the page with AJAX.
*   Finally, HTTP headers provide additional information to the servers and the clients about the requests, and the responses respectively. In the case of clients, they need to use headers to help the server curate accurate results. In case of servers, headers are sent to provide the client more information about the response.

# [Multiple choice questions](#toc.xhtml_s195a)

1.  **"{name: "John Doe", "age": 24}" – Is this statement a valid JSON syntax?**
    1.  Yes
    2.  No
2.  **What does the value 3 of the XMLHttpRequest property readyState signify?**
    1.  The request has been created, but not sent.
    2.  The operation of interaction with the servers is complete.
    3.  The send() method has been invoked.
    4.  The response’s body is being received.

# [Answers](#toc.xhtml_s196a)

1.  **b**
2.  **d**

# [CHAPTER 10](#toc.xhtml_c10)

# [Developing a Live Application!](#toc.xhtml_c10)

At the risk of sounding cliched, the famous English poet *John Keats* once said – *Nothing ever becomes real till it is experienced!*

While this inspiring thought can be applied to several fields, it couldn’t stand more true for web development. It’s fairly simple to rote learn the syntax, or mentally visualise what the output of your code might look like. However, you can only truly learn web development when you sit down and start coding.

With that in view, this chapter is solely dedicated to gaining that experience by creating a web application from scratch. We will be making use of several concepts that we have explored in the last nine chapters. In fact, we will not only write the code of the application, but also apply various principles of software development lifecycle to our development. This will give you a taste of the real-life process of web development in product companies.

As we move from ideation to testing, we will also pick up a few topics that have not yet been covered in the previous chapters. Once you complete the development, you can push your code on a code repository platform like *GitHub* to showcase it to the world!

# [Structure](#toc.xhtml_s197a)

In this chapter, we will cover the following topics:

*   The Live Application – Nom Nom!
*   The Idea
*   Laying the foundations
*   The initial styling
*   Connecting to the server
*   Updating the Home Page with the server response
*   Updating the Recipe Details page
*   System testing

# [Objective](#toc.xhtml_s198a)

After studying this chapter, you should be able to create your very own live application powered by data from a server! You will learn to explore the real-life world of web development and showcase your project to the entire world!

# [The live application – Nom Nom!](#toc.xhtml_s199a)

In the last chapter, we learned a great deal about interacting with servers. Using that knowledge, combined with the understandings of the previous chapters, we will be creating a live application on recipes. It is highly recommended to code the application simultaneously on your local machines. It will help you understand the process and the code better.

# [Software development lifecycle](#toc.xhtml_s200a)

A vast majority of successful product companies across the world follow the following pattern to create a new web product or roll out a new feature:

![](images/Figure-10.1.jpg)

**Figure 10.1:** The Software Development Lifecycle

The following is the summation of the process mentioned in the preceding screenshot:

*   **Idea**: Every feature/product starts with an idea. For instance, the idea behind the social media application, Instagram was to create a platform where users can share and like photos.
*   **Business Requirements Gathering**: Once the idea is generated, the next step is to understand the scope of this idea. It involves understanding who will be the target users for this idea, how will the factors like age group, geography, ethnicity, and so on, appeal to the concept, what should be the ideal number of pages, and many such decisions. This job is either done by a product manager or a dedicated team of researchers. At the end of step 2, a document is generated, which will detail out every information about the application from the business requirements to the ideal application structure.
*   **Design**: The business requirements document is now shared with the **User Experience** (**UX**) team. The team of UX/UI designers will now create a template that suffices the requirements of the business. This template is now shared with the development team.
*   **Development**: This is where we, as developers come into the picture. Based on the design shared by the UX team, it is the job of the team of developers to create a live version of the idea that the users can "*use*".
*   **Testing**: Once the development is completed, the feature/application is given to the team of testers for thorough testing. If the team of testers find any bugs or errors, it is reported to the development team. Once all the bugs have been resolved by the developers, the feature/application is tested once again. When the product/feature is deemed bugs-free, the product finally moves to the final phase.
*   **Public Release**: The final phase involves updating the released application with the new feature or releasing the product in the market. It also involves marketing, sales, and customer relations.

The lifecycle shown earlier varies from team to team. Based on the finance involved and the requirements, one or more lifecycle processes can be added or removed. However, in a majority of the scenarios, the preceding structure is the one that is followed.

Based on the preceding lifecycle, we need to complete the first three steps before we begin the application development. To save time, let’s create an application that will show a list of recipes to the user. Let’s start with the very first step – ideation, in the next section.

# [The Idea](#toc.xhtml_s201a)

Our simple application’s main purpose and motive is to help the user cook mouth-watering dishes by providing them the recipes. To entice the users with a memorable name, we will call our application as Nom Nom, (feel free to name the web application on your machine with whatever name you like).

To fetch the recipes for our application, we will be using a public API platform called The *MealDB*. You can check out the platform by typing this URL in your browser: **[https://www.themealdb.com/](https://www.themealdb.com/)**. As mentioned on their website, it is a crowd-sourced database of recipes from around the world. You can use their API platform to fetch recipes to be shown on our webpage. To know more about their APIs, you can click on the API tab on the navigation bar of the MealDB webpage.

**Note:** In this chapter, for the sake of implementing the knowledge that we have learned so far, we will not be adding a lot of features to our web application. However, after you finish creating the application by following the steps mentioned, feel free to add additional features like search, filter, more recipes, and so on.

Since we want to spend a majority of our time in understanding the development of our application, we will combine the second step of the business requirement gathering, and the design of our application in this section.

# [The Flow](#toc.xhtml_s202a)

Coming back to our application, the simple flow should be as follows:

![](images/Figure-10.2.jpg)

**Figure 10.2:** The flow of the application

Now that we know the flow, we can decide on the number of pages that our application should contain. Based on the preceding screenshot, we will need the following two pages to be shown on our application:

*   The first page should be the landing page or the home page. On this page, we will have a list of dishes. The user can select any one of the dishes to view its recipe.
*   The second page should be the recipe-detail page. On the second page, we should show the user the recipe of the dish they have selected.

# [The Design](#toc.xhtml_s203a)

As discussed in the last section, the simple requirement of our home page is to show the user a list of recipes, and allow them to choose a recipe. With that in mind, a low-level design of our home page should look like the following:

![](images/Figure-10.3.jpg)

**Figure 10.3:** A low level design of the home page.

Inside the header of the preceding screenshot, we can add the name of our application to showcase our brand. To avoid clutter, we will show only three recipes in one row.

For the recipe detail page, let’s think of the design from a user’s perspective. We know that this page will show the details of the recipe selected by the user on the home page. If you are a user searching for a recipe, what all would you like to see on a recipe detail page?

In our case, since we are keen on using the *MealDB* server, a part of our design is also dependent on the acquisition of data. We will show the users the title of the dish that they have selected, a YouTube video link for showing the video of the recipe, a list of ingredients, and finally, the instructions of the recipe.

With this in mind, the low-level design of our recipe detail page should look like the following:

![](images/Figure-10.4.jpg)

**Figure 10.4:** A low level design of the recipe detail page

As shown in the preceding screenshot, the design should suffice the general need of a user searching for a recipe. Since it is preferable to watch videos on a wider scale, we will provide a larger space for the video. It’s very crucial for the users to have an idea about both the ingredients and recipe. To save space and make our web page look clean, let’s include them side by side.

Now, that we have completed the first three steps of SDLC, let’s move to the most important part of this chapter – the development.

# [Laying the foundations](#toc.xhtml_s204a)

In the previous section, we finalized the number of pages, the flow, and the motive of our application. In this section, let’s first create the folder structure of our application and then create the HTML files.

# [The folder structures](#toc.xhtml_s205a)

Let’s start with the most basic steps, which are as follows:

1.  Create a folder at a suitable location on your local machine and name it '*Nom Nom – The Recipe App*' or the name that you have decided for your application. This is to ensure that you do not have trouble finding the location of your application code when you open your machine the next time.
2.  Inside this folder, create two files – **`index.html`** and **`recipe-detail.html`**. As decided earlier, the **`index.html`** will serve as the home page for our application, while the **`recipe-detail.html`** will provide the user with the details of the recipe that they have selected on the home page. Keep the files blank for the time being.

    **NOTE:** By default, when you upload your application on the server, it will always consider the `index.html` file to be the default home page of the website/web application.

3.  Create two folders called **`scripts`** and **`styles`**. The scripts folder will contain all our JS files, while the styles folder will host all the CSS files. Again, feel free to give a logical name of your choice to these folders. We will add the JS and the CSS files to these folders as we go ahead. If you intend to grow your application later, you might also need images and fonts to be added to your web page. These images and fonts should be stored in a separate folder called assets.

And with that, we have completed the folder structure of our application. At the end of these three steps, your folder structure should look like the following:

![](images/Figure-10.5.jpg)

**Figure 10.5:** The folder structure for Nom Nom

You must have noticed a **`README.md`** file inside the folder structure shown in the preceding screenshot. This file is a markdown file, denoted by the extension **`.md`**. Markdown files are text files that can be formatted with headers, indentations, and styling.

**Note:** The `README.md` file shown in the preceding *figure 9.19* is useful for hosting our application on the code repository platform called *GitHub*. While it’s not mandatory right now to host your project on *GitHub*, it’s very important to put up your projects on a code repository (repo) platform. By uploading your projects on a code repo platform like *GitHub*, you can download and use your code on any machine across the world. However, *GitHub* is much more than a simple repository platform. Trusted and used by almost all the developers in the world, it not only keeps your code safe, but you can also work on your code with peers and followers. In fact, several top companies insist on hiring only those candidates who have a prior experience with Git.

You can find out more information about GitHub by typing the following on your browser: **[https://www.github.com](https://www.github.com)**.

Now that we have completed our folder structure, let’s start creating our HTML files.

**NOTE:** It is highly recommended to use the Visual Studio Code IDE for coding.

# [Creating the HTML files](#toc.xhtml_s206a)

In this section, we will start creating the HTML files. We will first create the **`index.html`** file and after that, we will create the **`recipe-detail.html`** file.

# [Index.html](#toc.xhtml_s207a)

On our landing page, we will need a header which brands and showcases the name of our application – *NOM NOM*. Apart from that, we will need a list of all the recipes to be shown to the user. With this minimal knowledge, let’s create our **`index.html`** file:

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `<head>`
4.  `    <meta charset="UTF-8">`
5.  `    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
6.  `    <title>Nom Nom</title>`
7.  `</head>`
8.  `<body>`
9.  `    <div class="header">`
10.  `        <p class="title">NOM NOM</p>`
11.  `        <p class="subtitle">The best place to learn mouth-watering recipes!</p>`
12.  `    </div>`
13.  `    <div class="recipes-container">`
14.  `        <p class="section-title">Recipes</p>`
15.  `        <div class="recipes">Here, we will show all the recipes.</div>`
16.  `    </div>`
17.  `</body>`
18.  `</html>`

    **Code 10.1:** The index.html file for Nom Nom

As shown in the *[code example 10.1](#c10.xhtml_co10_1)*, we have created an *index.html* for our landing page. As you can see here, inside the body of our webpage, we have created two div elements.

The first div element contains the header of our webpage for branding. Inside the first **`div`** element, we have the first paragraph for the title and the second paragraph for a catchy subtitle.

The second **`div`** element will show the list of recipes to our users. We have aptly named the class of the second **`div`** element as recipes-container. Inside this **`div`**, we have first created a **`p`** element for the title of the section and a **`div`** element where we will show the recipes. For the time being, we have typed a placeholder text to show the location of our recipes list section on the web page. When we save this and open our web page by clicking on the **`index.html`** file inside our newly created folder, we will see something like the following:

![](images/Figure-10.6.jpg)

**Figure 10.6:** The view of the index.html file of Nom Nom

Now, let’s create the second HTML file of our web application.

# [Recipe-detail.html](#toc.xhtml_s208a)

On the second page, we want to show the user the recipe of the dish that he/she has selected. Keeping *[figure 10.4](#c10.xhtml_fig10_4)* in mind, we will add the following to the **`recipe-detail.html`**:

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `<head>`
4.  `    <meta charset="UTF-8">`
5.  `    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
6.  `    <title>Nom Nom | Recipe</title>`
7.  `</head>`
8.  `<body>`
9.  `    <div class="header">`
10.  `        <div>`
11.  `            <p class="title">NOM NOM</p>`
12.  `            <p class="subtitle">The best place to learn mouth-watering recipes!</p>`
13.  `        </div>`
14.  `        <p class="all-recipes">All Recipes</p>`
15.  `    </div>`
16.  `    <div class="recipe-details-container">`
17.  `        <p class="recipe-title">Title of the selected recipe</p>`
18.  `        <div class="recipe-video">`
19.  `            <iframe class="video" src="" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>`
20.  `        </div>`
21.  `        <div class="details">`
22.  `            <div class="ingredients">`
23.  `                <p class="section-title">Ingredients</p>`
24.  `                <ol class="ingredients-list">Here, we will have the list of the ingredients.</ol>`
25.  `            </div>`
26.  `            <div class="recipe">`
27.  `                <p class="section-title">Recipe</p>`
28.  `                <p class="instruction">Here, we will have the instructions of the recipe.</p>`
29.  `            </div>`
30.  `        </div>`
31.  `    </div>`
32.  `</body>`
33.  `</html>`

    **Code 10.2:** The recipe-detail.html file for Nom Nom

As shown in the *[code example 10.2](#c10.xhtml_co10_2)*, we have first added the header for our application inside the body, to maintain consistency across the pages. However, we have made a small change to the code shown in *[code example 10.1](#c10.xhtml_co10_1)*. We have now added a paragraph element with the text All Recipes inside the header. This text will help the user go back to the landing page.

Below the header, we have created a **`div`** element which houses the title of the recipe, an iframe element for housing the video, and another div element for the ingredients and the recipe. On saving this and opening the **`recipe-detail.html`** page inside our folder, we will see the following:

![](images/Figure-10.7.jpg)

**Figure 10.7:** The view of the recipe-detail.html file of Nom Nom

With this, we have created the foundation or the HTML of our webpage. Now, let’s move to the styling.

# [The Initial Styling](#toc.xhtml_s209a)

Styling is a critical part of any web application or a web page. It is the styling of the web page that attracts and retains consumers and users. A quick tip is to never go overboard with styling. It means, excess animations or very bright colors repel users.

For our application, we will maintain a clean and dignified styling.

If you think about our application for a moment, you will realize that certain elements in both the web pages will require a common set of styling, for instance, headers. However, a majority of the elements will require different styles.

As a rule of thumb, always keep different stylesheets for different web pages. It will not only help your CSS files remain clean, it will also help in cases when you need to change the CSS property of one of the elements on any one of the pages. If you have a separate stylesheet, it will be easier for you to find and change the style without affecting other styles. With this in mind, we will be creating three stylesheets – **`common.css`** (for common styles on both the web pages), **`index.css`** (for **`index.html`**), and **`recipe-detail.css`** (for **`recipe-detail.html`**).

Since the primary concern of this book is JavaScript, we will not be learning or exploring CSS in detail. If you have any doubts or queries, kindly refer the internet for the resolution.

Inside the styles folder, we will first create a file called **`common.css`**. This file will tend to the styling of the elements that will be common between all the files. Inside **`common.css`**, type the following code and save it:

1.  `html, body {`
2.  `    padding: 0 15px;`
3.  `    margin: 0;`
4.  `    height: 100%;`
5.  `    font-family: 'Roboto', 'Helvetica', sans-serif;`
6.  `}`

8.  `.header {`
9.  `    padding-top: 10px;`
10.  `    margin-bottom: 32px;`
11.  `}`

13.  `.title, .subtitle,`
14.  `.section-title {`
15.  `    margin: 0;`
16.  `}`

18.  `.title {`
19.  `    font-size: 40px;`
20.  `}`

22.  `.subtitle {`
23.  `    font-size: 18px;`
24.  `}`
25.  **Code 10.3:** The common.css file for Nom Nom

Since the elements inside the **`div`** header and the html/body will be common for all the pages, we have written the styles for the same in **`common.css`**.

Next, we will add the styling for the **`index.html`** file. Inside the styles folder, we will now create a file by the name **`index.css`**. Inside **`index.css`**, we will type the following style code:

1.  `.section-title {`
2.  `    font-size: 24px;`
3.  `    margin-bottom: 12px;`
4.  `}`

6.  `.recipes {`
7.  `    display: grid;`
8.  `    grid-template-columns: 1fr 1fr 1fr;`
9.  `    row-gap: 16px;`
10.  `}`

    **Code 10.4:** The index.css file for Nom Nom.

As shown in the *[code example 10.4](#c10.xhtml_co10_4)*, for the **`div`** storing all the recipes, we wish to show only three recipes in one row. Hence, we have used the grid display and three columns occupying the free space.

Finally, we will create the **`recipe-detail.css`** file for the **`recipe-detail.html`** file:

1.  `.header {`
2.  `    display: flex;`
3.  `    flex-direction: row;`
4.  `    justify-content: space-between;`
5.  `}`

7.  `.all-recipes {`
8.  `    cursor: pointer;`
9.  `    color: #007bff;`
10.  `}`

12.  `.recipe-title {`
13.  `    font-size: 32px;`
14.  `}`

16.  `.details {`
17.  `    width: 100%;`
18.  `}`

20.  `.section-title {`
21.  `    font-size: 18px;`
22.  `}`

24.  `.recipe {`
25.  `    overflow-y: auto;`
26.  `}`

28.  `.recipe-video {`
29.  `    margin-bottom: 16px;`
30.  `}`

32.  `.video {`
33.  `    height: 400px;`
34.  `    width: 100%;`
35.  `}`

37.  `.ingredients-list {`
38.  `    padding-left: 15px;`
39.  `}`

    **Code 10.5:** The recipe-detail.css file for Nom Nom.

With this, we have added the initial styling for our web pages. Now, we need to link these CSS files inside our respective HTML files. In **`index.html`**, right before we end the **`head`** tag and after the **`title`** tag, we will add the following:

1.  `<link href="styles/common.css" rel="stylesheet" />`
2.  `<link href="styles/index.css" rel="stylesheet" />`

    **Code 10.6:** Linking the CSS files in index.html

Similarly, we will link the CSS files to the **`recipe-detail.html`** page at the end of the head tag:

1.  `<link href="styles/common.css" rel="stylesheet" />`
2.  `<link href="styles/recipe-detail.css" rel="stylesheet" />`

    **Code 10.7:** Linking the CSS files in recipe-detail.html

After following the preceding steps, when you refresh the page, the **`index.html`** page will look like the following:

![](images/Figure-10.8.jpg)

**Figure 10.8:** The index.html after applying CSS

Similarly, the **`recipe-detail.html`** will now look like the following:

![](images/Figure-10.9.jpg)

**Figure 10.9:** The recipe-detail.html after applying CSS

With this, we have completed applying the initial CSS to our web application. Let’s move to JavaScript!

# [Connecting to the server](#toc.xhtml_s210a)

In the previous sections, we completed creating the HTML files and applying style to it using CSS. Now, we will start working on the JavaScript.

To revise an old concept, interaction with servers generally happens using an interface known as **Application Programming Interface** (**API**). In simple layman terms, an API is very similar to a URL for a server/application. APIs allow two applications to talk to each other. For instance, every time you use a social media application like *Facebook* or *Instagram*, an API request is sent to the server to fetch the data to be shown on your phone/machine. In this section, we will be working with the APIs provided by a public API platform called *The MealDB*.

If you will have a look at the API section of the *MealDB* platform, you will see a list of APIs (also known as endpoints). Every API serves a different purpose.

![](images/Figure-10.10.jpg)

**Figure 10.10:** The API page of the MealDB platform

For our application *Nom Nom*, we will require a list of recipes to be shown on the landing page. While there are several different approaches to get that from the MealDB server, we will be using the endpoint **[https://www.themealdb.com/api/json/v1/filter.php?c=Seafood](https://www.themealdb.com/api/json/v1/filter.php?c=Seafood)**, for our needs. However, instead of Seafood, I will be fetching a list of recipes for the category Pasta.

(You can check out the list of all the categories by copying the API **[https://www.themealdb.com/api/json/v1/1/categories.php](https://www.themealdb.com/api/json/v1/1/categories.php)** and pasting it in your browser URL.)

So, without much further ado, we will now create a new file inside the folder scripts and name it **`index.js`**. Inside **`index.js`**, we will now create, open, and send the request to the API (endpoint): **[https://www.themealdb.com/api/json/v1/filter.php?c=Pasta](https://www.themealdb.com/api/json/v1/filter.php?c=Pasta)**

1.  `let request = new XMLHttpRequest();`
2.  `request.open('GET', 'https://www.themealdb.com/api/json/v1/1/filter.php?c=Pasta', true);`
3.  `request.send();`
4.  `request.onreadystatechange = function() {`
5.  `    if(this.readyState === 4 && this.status === 200) {`
6.  `        console.log("JSON string:  ", this.responseText);`
7.  `        console.log("After parsing:  ", JSON.parse(this.responseText));`
8.  *`//createRecipeCards(this.responseText);`*
9.  `    }`
10.  `}`

    **Code 10.8:** Creating AJAX request on index.js

In *[code example 10.8](#c10.xhtml_co10_8)*, it’s easy to comprehend the first five lines of the code. We have simply created an AJAX request, opened it, sent it to the server, and now we are waiting for the server response to be 200.

After line number 5, once we have successfully received the response, we need to use that response to create a list of recipes on index.html. To achieve that, I am assigning that duty to a function called **`createRecipeCards`**. We intend to pass the server response to the **`createRecipeCards`** function. However, before we pass the response, let’s have a look at the response received from the server. To understand it better, we will also apply **`JSON.parse`** on the **`responseText`**, as shown on the line number 7\. Hence, we will comment out the line number 7 by adding // at the beginning of the line.

We will now save the **`index.js`** file and import this file inside our **`index.html`**. To do that, we will add the following code right before we close the **`body`** tag of our **`index.html`**:

`<script src="scripts/index.js"></script>`

**Code 10.9:** Importing index.js in index.html

When you save this and hit refresh on our webpage, you will see the following in your console:

![](images/Figure-10.11.jpg)

**Figure 10.11:** The response of the API shown in the console

As you can see in the preceding screenshot, we are receiving an object with the key meals. The value of the key meals is an array of objects which includes our recipes. It is this array of objects that we need to send to the function **`createRecipeCards`** for creating a list of recipes. So, let’s make a quick modification to our code inside **`index.js`**.

Let’s remove the console.log statements from line numbers 6 and 7. Also, let’s uncomment the function call to **`createRecipeCards`** on line number 8 and modify the arguments that we send to the function. Instead of simply passing the response text, we will now parse the JSON string and send the value that is stored inside the key meals:

`createRecipeCards(JSON.parse(this.responseText).meals);`

**Code 10.10:** Parsing the response and sending it.

With this, we have successfully received a response from the server and passed it to function to create the list.

# [Updating the Home page with the server response](#toc.xhtml_s211a)

In the last section, we received the response for a server; to maintain a clean code, we are assigning the job of creating a list of recipes to a function **`createRecipeCards`**. Inside this function, using the DOM methods that we had learned in *[Chapter 1: Introduction to JavaScript](#c01.xhtml)*, we will create a list of recipes for the user.

Now, there’s a very common saying that pictures speak louder than words. In fact, people tend to remember pictorial or graphical description better than textual description. With that ideology in mind, let’s create a pictorial list of recipes for our users. It will not only make our page look livelier, but it will also entice the user to check out maximum number of recipes.

In *[code example 10.4](#c10.xhtml_co10_4)*, we had added the CSS property **`display: grid`** and **`grid-template-columns: 1fr 1fr 1fr`** to the **`div`** element where the recipes will be shown. It means a rough diagram of our recipes container will look something like the following:

![](images/Figure-10.12.jpg)

**Figure 10.12:** The structure of the recipes container

As shown in the preceding screenshot, each box will represent a recipe. As decided earlier, once the user clicks on any of the boxes depicting a recipe, the user will be taken to the **`recipe-detail`** page for the detailed recipe of the selection.

To help us code better, let’s look at an individual recipe received in the server response:

![](images/Figure-10.13.jpg)

**Figure 10.13:** The structure of an individual recipe in the server response

If you observe the preceding screenshot, you will notice that every recipe has a link for the recipe image stored in the key **`strMealThumb`**. We will use this link to add images to the boxes shown in *[figure 10.12](#c10.xhtml_fig10_12)*. Additionally, we can use the key **`strMeal`** for the name of the recipe. With this in mind, let’s create the function **`createRecipeCards`** inside **`index.js`**:

1.  `const createRecipeCards = list => {`
2.  `    let recipesContainer = document.querySelector(".recipes");`
3.  `    for(let recipe of list) {`
4.  *`// Create the recipe card i.e. the box where we will show the recipe`*
5.  `        let recipeCard = document.createElement('div');`
6.  `        recipeCard.setAttribute("id", recipe.idMeal);`
7.  `        recipeCard.setAttribute("class", "recipe-card");`

9.  *`// Create and add the image to the recipe card we just created`*
10.  `        let recipeImg = document.createElement("img");`
11.  `        recipeImg.setAttribute("src", recipe.strMealThumb);`
12.  `        recipeImg.setAttribute("class", "recipe-img");`
13.  `        recipeImg.setAttribute("alt", recipe.strMeal);`
14.  `        recipeCard.appendChild(recipeImg);`

16.  *`// Create and add a p element to show the name of the recipe to the recipe card`*
17.  `        let recipeTitle = document.createElement("p");`
18.  `        recipeTitle.setAttribute("class", "recipe-title");`
19.  `        recipeTitle.innerHTML = recipe.strMeal;`
20.  `        recipeCard.appendChild(recipeTitle);`

22.  *`// Add the recipe card to the main container`*
23.  `        recipesContainer.appendChild(recipeCard);`
24.  `    }`

    **Code 10.14:** Creating the function createRecipeCards to add the recipes list

As shown in *[code example 10.14](#c10.xhtml_co10_14)*, we receive the list of recipes as an argument to the function **`createRecipeCards`**.

*   The first thing that we need to do is fetch the container where our recipes will be stored. We achieve that in line number 2 of *[code example 10.14](#c10.xhtml_co10_14)* and store that container inside the variable **`recipesContainer`**.
*   Next, we parse through every element inside the array of objects list, as shown in line number 3.
*   The next thing that we need to do now is create the box for an individual recipe. We do that on line numbers 5-7\. First, we create the element **`div`** on line number 5 and we assign that to the variable **`recipeCard`**. After that, we assign this element an attribute id with the key **`idMeal`** that we have received in the server response. This id will be useful when we need to get a detailed individual recipe from the **`MealDB`** server. When a user clicks on the card, we will try to fetch this id and pass it to the recipe-detail page. Finally, we assign a class recipe-card to this **`div`** element to add styling to our card.
*   Next, we create the image that needs to be added to the individual boxes inside the container of recipes. In the preceding *[code example 10.14](#c10.xhtml_co10_14)*, in lines 10-14, we create the image element, assign the **`strMealThumb`** as the source to the image element, assign a class to the image element, assign the name of the recipe to the alt attribute of the image, and finally append the image element to the **`recipeCard`** we created on line number 5.
*   The last thing that we need to add to the recipe card is the text, that is, the name of the recipe. We do that in lines 17-20.
*   Finally, we need to attach this recipe card created for an individual recipe from the list to the recipes container. We do that on line number 23.

Since we have created new elements, let’s also add the styles for these new elements in the **`index.css`** file:

1.  `.recipe-card {`
2.  `    border: 1px solid #ddd;`
3.  `    margin-right: 10px;`
4.  `    display: flex;`
5.  `    border-radius: 8px;`
6.  `    position: relative;`
7.  `    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);`
8.  `    cursor: pointer;`
9.  `    opacity: .7;`
10.  `}`

12.  `.recipe-card:nth-child(3n) {`
13.  `    margin-right: 0;`
14.  `}`

16.  `.recipe-card:hover {`
17.  `    box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);`
18.  `    opacity: 1;`
19.  `}`

21.  `.recipe-title {`
22.  `    font-size: 18px;`
23.  `    position: absolute;`
24.  `    color: #FFF;`
25.  `    bottom: 10px;`
26.  `    left: 10px;`
27.  `    margin: 0;`
28.  `    background-color: rgba(0, 0, 0, 0.5);`
29.  `    padding: 5px;`
30.  `    border-radius: 5px;`
31.  `}`

33.  `.recipe-img {`
34.  `    width: 100%;`
35.  `    max-height: 350px;`
36.  `}`

    **Code 10.15:** Adding the styles for new elements in index.css

In the preceding *[code example 10.15](#c10.xhtml_co10_15)*, we have added the styles for the new elements that were created in *[code example 10.14](#c10.xhtml_co10_14)*. While most of the CSS properties mentioned earlier are simple to understand, one quirky thing that we have done to grasp the user’s attention is lowering the opacity of the recipe card. Only when the user hovers over the recipe card, the card will be shown clearly.

When we save both the JS and the CSS files and refresh the **`index.html`** page on the browser, we will see something like the following:

![](images/Figure-10.14.jpg)

**Figure 10.14:** The structure of an individual recipe in the server response

# [Moving to the Recipe Detail page](#toc.xhtml_s212a)

In the previous section, we completed creating the **`index.html`**, that is, the Home Page of our application *Nom Nom*. The next step is to make sure that when the user clicks on any of the recipes on the home page, he/she is directed to the **`recipe-detail.html`**. On the **`receipe-detail.html`**, the user should be shown the detailed recipe of the one he/she selected on the home page.

To some extent, we have laid the foundation for directing the user to the **`recipe-detail.html`** page. In *[code example 10.14](#c10.xhtml_co10_14)*, we assigned an id to the individual recipe cards on the home page. Now, we need to assign a click event listener on the individual recipe cards. This event listener will fetch the id of the selected card and pass it to the **`recipe-detail.html`** page.

To begin with, let’s create the event handler function in **`index.js`**:

``const viewRecipe = id => window.location.href = `recipe-detail.html?id=${id}`;``

**Code 10.16:** Event handler on the click of the recipe card

In *[code example 10.16](#c10.xhtml_co10_16)*, we have created an ES6 function called **`viewRecipe`**. The function **`viewRecipe`** accepts an id as the parameter. This function directs the user to the recipe-detail.html page and passes the id as a query parameter.

In *[code example 10.16](#c10.xhtml_co10_16)*, we have used the **`window.location.href`** property. The **`window.location.href`** property returns the current URL of the page. As it goes with JavaScript properties, if you set a value to the **`window.location.href`** property, it will set that value to the URL of the page, that is, it will open that URL on the current tab. Therefore, in the preceding code, we are making the window of the current web page to be directed to the **`recipe-detail.html`** page.

As decided earlier, we also wish to send the ID of the selected recipe to the recipe-detail page. This can be achieved using a concept called query string parameters. Whenever you need to pass values in a URL, you can pass them as key=value pairs in the URL. To specify query string parameters, you need to add a question mark symbol at the end of your URL and add the key=value pairs after that. In case of multiple parameters (key=value pairs), they need to be separated by an ampersand symbol (&).

Hence, with the help of the **`window.location.href`** property and query string parameters, we have achieved the task of redirecting the user to the Recipe Detail page.

Now we need to attach an event listener to every recipe-card element. To do that, in *[code example 10.14](#c10.xhtml_co10_14)*, we will add an onclick event right after the code that exists on line number 23 **`recipesContainer.appendChild(recipeCard)`**;. We will add the following line after line number 23 of *[code example 10.14](#c10.xhtml_co10_14)* in **`index.js`**:

`recipeCard.onclick = () => viewRecipe(recipe.idMeal);`

**Code 10.17:** The event handler for the recipe cards.

By adding the code, as shown in the preceding *[code example 10.17](#c10.xhtml_co10_17)*, every time the user clicks on the recipe card, it will call the **`viewRecipe`** function and pass the meal ID to it. We have to make sure that we add the code shown in *[code example 10.17](#c10.xhtml_co10_17)* inside the for loop. It will ensure that every recipe card gets this event listener.

After saving these two lines of code, when we run our application, you will see that clicking on any of the recipe will take you to the Recipe Detail page. If you will look at the URL of the recipe-detail page, you will notice that every time you click a different recipe, a different ID will be populated in the URL.

# [Updating the Recipe Details page](#toc.xhtml_s213a)

Now that we have completed the first part of our web page, let’s create the second part of our website – the **`recipe-detail.html`**. In the previous section, we were redirecting the user to the recipe-**`detail.html`** page when he/she clicked on any of the recipes shown on the home page. We were passing the ID as a query string parameter in the URL.

Let’s complete the Recipe Details page in the following fashion:

1.  Fetch the ID from the URL and send a request to the server for the detailed recipe.
2.  Use the server response to create the necessary HTML elements.
3.  Finally, add styling to these elements using CSS.

# [Fetching the detailed recipe](#toc.xhtml_s214a)

In order to fetch the detailed recipe, we can check the API list on the *MealDB* server to find the API endpoint that can help us achieve this. You will find that the endpoint **[https://www.themealdb.com/api/json/v1/1/lookup.php?i=52772](https://www.themealdb.com/api/json/v1/1/lookup.php?i=52772)** will help us fetch the detailed recipe with the help of an ID. So, let’s write the code for fetching the ID and sending the request.

# [Fetching the id passed from the home page](#toc.xhtml_s215a)

For this, we will create a new JavaScript file called **`recipe-detail.js`** inside the scripts folder. Inside the **`recipe-detail.js`**, we will first fetch the id that we receive in the URL.

1.  `const fetchId = () => {`
2.  `    let paramsString = window.location.search.slice(1);`
3.  `    let paramsArr = paramsString.split('&');`
4.  `    let id = paramsArr`
5.  `            .find(param => param.split('=')[0] === 'id')`
6.  `            .split('=')[1];`
7.  `    return id;`
8.  `}`

10.  `let id = fetchId();`

    **Code 10.18:** The code for fetching the ID from the URL.

As shown in *[code example 10.18](#c10.xhtml_co10_18)*, we have created a function for fetching the id. We have aptly named the function as **`fetchId`**. Inside this function, we first fetch the query string parameter. To understand this better, let’s open the Developer Tools on the **`Console`** tab for **`recipe-detail.html`**. Inside the console, let’s type **`window.location`**. You will see something like the following on your console window:

![](images/Figure-10.15.jpg)

**Figure 10.15:** window.location

As you can see in the preceding screenshot, the **`window.location`** has all the information related to the URL of a web page. What concerns us right now is the search property of the **`window.location`**. Inside the search property, we have the entire query string parameter.

*   In *[code example 10.18](#c10.xhtml_co10_18)*, on line number 2, we take the **`window.location.search`** property and slice the first character using the JavaScript slice method. When we do this, we will get the value **`id=52835`** inside the variable **`paramsString`**.
*   On the next line – line number 3, we consider the possibility of multiple parameters in the query string. Using the JavaScript array method of split, we split the string inside the variable **`paramsString`** at the character &. It will result in an array of values separated at the ampersand (&) character. We store this array in the variable **`paramsArr`**.
*   On lines 4-6, we now parse through every element of the array **`paramsArr`** to find the parameter which has the id passed from **`index.js`**. On line number 5, we use the JavaScript method **`find()`**. The **`find()`** method is similar to the **`filter()`** method, with the difference that the filter method returns an array of all the elements that passes a conditional test, while the find method returns the first element that passes the test. In this case, since we are sure that we will be having only one instance of a query parameter having the key id, we will use the find method, as it directly passes the object/value instead of an array. To find the key, we will need to once again split the key=value string at the equals (=) sign to retrieve the key. Since the key will always be the first element, that is, the element at position 0 of the resultant array, we check the condition for the first element of the split array to have the text 'id'.
*   Once we get the object that has the key id, we need to use its value for fetching the id. On line number 6, we once again split the string and grab the element at position 1 of the split array, which will be the value. Since this is the value that we require for our code, we will store and return this value from the function **`fetchId`**.

The result of the function **`fetchId`** is stored inside a variable ID on line number 10.

# [Sending a request to the server with the id](#toc.xhtml_s216a)

Now, that we have the id received from the **`index.js`** file, let’s quickly send a request to the server with the received id to fetch the detailed recipe. As we have seen at the start of the section, we will be using the API **[https://www.themealdb.com/api/json/v1/1/lookup.php?i=52772](https://www.themealdb.com/api/json/v1/1/lookup.php?i=52772)** by replacing the ID given at the end:

1.  `let request = new XMLHttpRequest();`
2.  ``request.open('GET', `https://www.themealdb.com/api/json/v1/1/lookup.php?i=${id}`, true);``
3.  `request.send();`
4.  `request.onreadystatechange = function() {`
5.  `    if(this.readyState === 4 && this.status === 200) {`
6.  `        console.log(JSON.parse(this.responseText));`
7.  `        addRecipeDetails(JSON.parse(this.responseText).meals);`
8.  `    }`
9.  `}`

    **Code 10.19:** The code for fetching the recipe detail from the server

As we have seen with *[code example 10.8](#c10.xhtml_co10_8)*, in *[code example 10.19](#c10.xhtml_co10_19)*, we create, open, and send a request to the *MealDB* server with the URL for fetching recipe details based on the id received. Once again, we will assign the job of creating the various HTML elements on the **`recipe-detail.html`** to a function. This time, in the recipe-detail.js, we will be using a function by the name **`addRecipeDetails`**. Like we have done previously, we will first use **`JSON.parse`** to convert the JSON string to a JavaScript object. Then, we will send the value inside the key meals of this JavaScript object to the function.

# [Create the HTML elements inside the Recipe Details page](#toc.xhtml_s217a)

Before we start our work on the function, let’s have a quick look at the JSON parsed server response. Since we have added a **`console.log`** statement on the line number 6 of *[code example 10.19](#c10.xhtml_co10_19)*, let’s take a look at the Console panel of the Developer Tools to see its value:

![](images/Figure-10.16.jpg)

**Figure 10.16:** Response of detailed recipe

As you can see in the preceding screenshot, we receive an array with a single value (because for a given id, there will always be only one recipe). So, before we look ahead, let’s make a quick change to line number 7 of *[code example 10.19](#c10.xhtml_co10_19)*. Instead of sending the array inside the meals key of the response, we will now send the first and the only element inside the array:

`addRecipeDetails(JSON.parse(this.responseText).meals[0]);`

**Code 10.20:** Modification to the function call

Coming back to the server response, we can see that we have a lot of information that can help us in creating the recipe details page. However, we will only require the *YouTube* link that is shared in the **`strYoutube`** property, the name of the recipe shared in the **`strMeal`** property, the instructions shared in the **`strInstructions`** property, and finally the list of ingredients and measures stored in the several **`strIngredient`** and **`strMeasure`** properties.

Adding the **`strYoutube`**, **`strMeal`**, and the **`strInstructions`** property is pretty straight-forward. So, let’s first add the data from these properties to the UI. Additionally, we can use the **`strMeal`** property to update the title of our page. Since we will be using the **`addRecipeDetails`** function for updating the UI, let’s add the code for adding these properties inside the **`addRecipeDetails`** function:

1.  `const addRecipeDetails = response => {`
2.  ``    document.title = `Nom Nom | ${response.strMeal}`;``
3.  `    document.querySelector(".recipe-title").innerHTML = response.strMeal;`
4.  `    document.querySelector(".video").setAttribute('src', response.strYoutube);`
5.  `    document.querySelector(".instruction").innerHTML = response.strInstructions;`
6.  `}`

    **Code 10.21:** Adding several properties to the UI

When we save this and refresh our web page, we will not see any changes on the **`recipe-detail.html`**. It is because we have not received any id in the URL from **`index.html`**. So, let’s go back to **`index.html`** by changing the URL in the address bar. Now, when you select a recipe, the **`recipe-detail.html`** page will look like the following:

![](images/Figure-10.17.jpg)

**Figure 10.17:** CORS error

If we compare *[figure 10.17](#c10.xhtml_fig10_17)* with *[figure 10.9](#c10.xhtml_fig10_9)*, you will notice that we have progressed massively. However, the video is not working. When you check the console for the errors, you will see the following:

![](images/Figure-10.18.jpg)

**Figure 10.18:** Recipe Detail page after adding several properties

By default, for security reasons, browsers do not allow resources to be shared between different servers. To solve this issue, we will make a small modification to the iframe code on line number 4 of *[code example 10.21](#c10.xhtml_co10_21)*:

`document.querySelector(".video").setAttribute('src', response.strYoutube.replace("watch?v=", "embed/"));`

**Code 10.22:** Enabling the video on recipe detail page

With the help of the code shown in *[code example 10.22](#c10.xhtml_co10_22)*, we will now convert the video link received in the server to an embedded link. In the second argument of the **`setAttribute`** method of *[code example 10.22](#c10.xhtml_co10_22)*, we replace the string **`watch?v=`** with **`embed/`**. The **`watch?v=`** in the URL signifies watching the video on the YouTube platform while the embed/implies embedding or adding the YouTube video inside a web page. Now, after making this change, when we refresh the page, we will see the following:

![](images/Figure-10.19.jpg)

**Figure 10.19:** View of the recipe detail page after enabling video

For the ingredients, we need to make sure the ingredients and their measures are shown together like the following: Ingredient N (Measure N). Currently, every ingredient is separately provided in the response. To solve this, we will create another function and invoke it from within the **`addRecipeDetails`** function:

1.  `const getIngredients = response => {`
2.  `    let ingredients = [],`
3.  `        measurements = [],`
4.  `        ingredientsWithMeasurements = [];`
5.  `    for(let key in response) {`
6.  `        if(key.includes("strIngredient") && response[key].length > 0)`
7.  `            ingredients.push(response[key]);`
8.  `        if(key.includes("Measure") && response[key].length > 0 && response[key] !== " ")`
9.  `            measurements.push(response[key]);`
10.  `    }`

12.  `    for(let index in ingredients) {`
13.  ``        ingredientsWithMeasurements.push(`${ingredients[index]} (${measurements[index]})`);``
14.  `    }`

16.  `    return ingredientsWithMeasurements;`
17.  `}`

    **Code 10.23:** Making an array of ingredients string

In *[code example 10.23](#c10.xhtml_co10_23)*, we will accept the entire response as an argument. Since the ingredients and measures are added separately in the response, as shown in *[figure 10.16](#c10.xhtml_fig10_16)*, it’s important to receive the entire response in this function.

If you look at the server response in *[figure 10.16](#c10.xhtml_fig10_16)* closely, you will notice that all ingredients have the text **`strIngredient`** common with a number appended after that. Likewise, all the measurements have the text Measure common with a number appended after that. In fact, every indexed ingredient corresponds to its indexed measure. It means (check *[figure 10.16](#c10.xhtml_fig10_16)*), **`strIngredient1`** – Macaroni should have the measurement of **`strMeasure1`** – 8 ounces (230 gms). It also means the count of ingredients will be equal to the count of the measurements.

Keeping this in mind, inside the function, we run a for loop to parse through every property of the response. If the key matches the text "**`strIngredient`**" and its value is not blank, we push its value inside the ingredients array. Likewise, we do the same for measurements on line 8 and 9.

When both the arrays are populated, we will now run a for loop through the newly created ingredients array. Since both the ingredients array and the measurements array will have the same length, we can use any one of them to get the index value. Using this index value, we will convert them to "Ingredients (Measurements)" format. This final array created on line number 13 of *[code example 10.23](#c10.xhtml_co10_23)* will be passed back to the **`addRecipeDetails`** function.

So, we will update our **`addRecipeDetails`** function to receive the string-formatted list of ingredients and measurements. Additionally, we will use this list to populate our recipe detail page with the missing piece of ingredients:

1.  `const addRecipeDetails = response => {`
2.  ``    document.title = `Nom Nom | ${response.strMeal}`;``
3.  `    document.querySelector(".recipe-title").innerHTML = response.strMeal;`
4.  `    document.querySelector(".video").setAttribute('src', response.strYoutube.replace("watch?v=", "embed/"));`
5.  `    let ingredientsList = document.querySelector(".ingredients-list");`
6.  `    let ingredients = getIngredients(response);`
7.  `    for(let ingredient of ingredients) {`
8.  `        let listElement = document.createElement('li');`
9.  `        listElement.innerHTML = ingredient;`
10.  `        ingredientsList.appendChild(listElement);`
11.  `    }`
12.  `    document.querySelector(".instruction").innerHTML = response.strInstructions;`
13.  `}`

    **Code 10.24:** Updating the addRecipeDetails function to use ingredients

So, now we have updated the **`addRecipeDetails`** function. We first fetch the HTML container to store the ingredients. Next, we call the **`getIngredients`** function to receive the string formatted ingredients and store it in the variable ingredients. Finally, we use this variable ingredients to create a list of elements and append it to the recipe detail page. On saving this and refreshing the web page, we will see the following:

![](images/Figure-10.20.jpg)

**Figure 10.20:** View of the recipe detail page after adding lists

If you noticed it acutely, we see the placeholder message while we wait for the server to respond. To solve this, remove the placeholders on the corresponding line numbers 24 and 28 of your **`recipe-detail.html`** (refer *[code example 10.2](#c10.xhtml_co10_2)*) and line number 16 of index.html (refer *[code example 10.1](#c10.xhtml_co10_1)*).

# [Adding the link back to the home page](#toc.xhtml_s218a)

A final piece of code that needs to be added to the Recipe Detail page is activating the "**`All Recipes`**" text in the header. To do that, let’s create a function **`goToHome`** and add it to **`recipe-detail.js`**.

`const goToHome = () => window.location.href = "index.html";`

**Code 10.25:** Function for going back to the home page

As we have learned earlier, setting the **`window.location.href`** property will redirect the browser to the value set. So, we add the value **`index.html`** to this property. Now, that the function is created, we need to add the invocation of this function to the text "**`All Recipes`**". In our **`recipe-detail.html`** file, we will now find this text and add the onclick event listener property to it:

`<p class="all-recipes" onclick="goToHome()">All Recipes</p>`

**Code 10.26:** Adding the onclick property to All Recipes.

After saving the changes, we can test this by refreshing our recipe-detail page and clicking on the "**`All Recipes`**" text. It should now go to the home page of our application.

With this, we have successfully completed the development of our application. Let’s move to the next part – Testing!

# [System testing](#toc.xhtml_s219a)

In *[figure 10.1](#c10.xhtml_fig10_1)*, we saw that once the development is completed, the next process is testing. Testing or **Quality Assurance** (**QA**) is the process of testing the application. There are several types of testing. A few of them are as follows:

*   **Unit Testing**: In this test, we check every individual component that builds up the UI. Tests are done to check whether they are working in the expected fashion.
*   **Component Testing**: Component testing is done to verify the functionality of the component. For example, a component can be a module, or can be the profile page of a website, built up of several small components that we tested using unit testing.
*   **Smoke Testing**: This testing is done for new "*builds*". Whenever the development team finishes their tasks, they "*build*" the code for uploading it to the server. Smoke testing is an initial test to check whether the new builds, that is, every new update to the code is stable.
*   **Integration Testing**: The integration testing is done for checking how different components work with each other. Primarily, it is used to check if the functioning of one module is crashing the other.
*   **Regression Testing**: It is used to check if the changes or modification to any feature/functionality is not breaking or crashing the original functionality.
*   **Sanity Testing**: It is similar to smoke testing. It is used for checking if the fixes to resolve a bug in the code has resolved the code. It is also used for identifying whether the resolution has resulted in any new bugs or not.
*   **System Testing**: Generally, it is the final round of testing done by the testers. It mirrors the actual environment in which the users will be using the application. It checks whether the application as a whole is performing well against its actual technical, functional, and business requirements.

In this chapter, we will only be performing the system testing to check whether our application '*Nom Nom*' is working based on the crude expectations that we set in *[figure 10.2](#c10.xhtml_fig10_2)*.

To perform system testing, we will closely observe every single functionality of our web application. It involves, but is not limited to, the correct opening of the web page on the browser, checking the headers, the list of recipes, the clicking of the recipe cards, the redirection to the recipe detail page, the loading of the recipe, the working of the YouTube video, and whether the text is getting populated at the right places on the web page. It also involves checking the styling of our web page and whether any elements or components (individual functionalities) are looking good or not. Additionally, it also includes checking the requests that have been sent and whether we are receiving the correct response.

Spend a considerable amount of time to perform system testing on the application that you have just created on your machine.

If you have completed performing system testing on the application, you will observe two shortcomings of our application:

*   Whenever we are sending a request to the *MealDB* server, the page remains blank with no indication whether the request has been sent, or if the list or the details are loading. It could be critical if the network or the internet speed is low. In that case, the server might take more than 2-3 minutes to respond to the request. If we do not provide a message or any indication, the user might simply see a blank screen while the response is being received and he/she might leave the application.
*   In case the server request fails, we do not have any way to handle the errors.

So, let’s resolve these issues.

# [Adding a text for loading](#toc.xhtml_s220a)

As mentioned earlier, the time taken by a server to respond to a request is never fixed. In case of slower networks, it might even take the server ten minutes to send a response to the client. In such cases, it’s always wise to inform the user of the application that we are awaiting a response from the server. To keep the user engaged, we can include text like '*Loading…*', '*Fetching information from the server…*', or a graphical image like a spinning circle to denote loading. The options are endless and limited only to your creativity.

For our application, we will be adding a simple '*Loading…*' text.

Since we are making a server request at two places, we need to add the 'Loading…' text to both the files. Let’s first add it to the **`index.html`** file.

On our home page, that is, **`index.html`**, it would make sense to add the loading text in the recipes container where the recipe pictures are eventually loaded. So, let’s go ahead and add a **`<p>`** element with the text loading to the **`div`** element with the class name recipes-container. After adding the **`p`** element, the recipes-container will look like the following:

1.  `<div class="recipes-container">`
2.  `    <p class="section-title">Recipes</p>`
3.  `    <div class="recipes"></div>`
4.  `    <p class="loading">Loading…</p>`
5.  `</div>`

    **Code 10.27:** Adding the loading text to recipes-container

Now, we need to trigger and show the loading text when we are waiting for the response, and hide it when the response is received. To do this, we can use the **`readyState`** property. In the last chapter, we learned about the **`readyState`** property of the **`XMLHttpRequest`** object. When we send the **`XMLHttpRequest`** object, the value of the **`readyState`** property becomes 2\. In *[code example 10.8](#c10.xhtml_co10_8)*, we used the **`onreadystatechange`** property of the **`XMLHttpRequest`** object to check the condition when the response is received, and the value of the **`readyState`** property becomes 4\. Now, we will add one more condition inside the function for handling the **`onreadystatechange`** property:

1.  `request.onreadystatechange = function() {`
2.  `    if(this.readyState === 2) {`
3.  `        document.querySelector(".loading").style.display = 'block';`
4.  `    }`
5.  `    if(this.readyState === 4 && this.status === 200) {`
6.  `        document.querySelector(".loading").style.display = 'none';`
7.  `        createRecipeCards(JSON.parse(this.responseText).meals);`
8.  `    }`
9.  `}`

    **Code 10.28:** Adding the hide/show logic in index.js

In *[code example 10.28](#c10.xhtml_co10_28)*, we first check for the condition when the value of the **`readyState`** property is 2\. When that happens, we fetch the element of loading using **`document.querySelector(".loading")`** and make sure the element showing the text is visible. As soon as we receive the response, that is, when the value of the **`readyState`** property becomes 4, we will once again fetch the element (as shown on line number 6) and hide it.

When you save the preceding code and refresh our web page, depending on your internet speed, you will briefly see the loading text before it vanishes, and the recipes are shown:

![](images/Figure-10.21.jpg)

**Figure 10.21:** The loading text seen on the home page.

Similarly, let’s make similar changes to the recipe detail page. Let’s add the loading icon inside the **`recipe-details-container`** element. Next, let’s add the hide/show logic in the **`recipe-detail.js`**. At the same time, let’s change the title of the web page to incorporate loading:

1.  `request.onreadystatechange = function() {`
2.  `    if(this.readyState === 2) {`
3.  `        document.querySelector(".loading").style.display = "block";`
4.  `        document.title = "Nom Nom | Loading…";`
5.  `    }`
6.  `    if(this.readyState === 4 && this.status === 200) {`
7.  `        document.querySelector(".loading").style.display = "none";`
8.  `        addRecipeDetails(JSON.parse(this.responseText).meals[0]);`
9.  `    }`
10.  `}`

    **Code 10.29:** Adding the hide/show logic for loading in recipe-detail.js

When we save the preceding code and refresh the web page, we will see the following:

![](images/Figure-10.22.jpg)

**Figure 10.22:** The loading text seen on the recipe-detail page with bugs

As you can see in the preceding screenshot, we need to hide the headers for the Ingredients and Recipe, as well. To begin with, we first need to update the CSS property of the container with the class name details and add the property display: none. This will make sure the headers remain hidden in normal scenarios. Now, in **`recipe-detail.js`**, let’s update the code inside the **`onreadystatechange`** property:

1.  `request.onreadystatechange = function() {`
2.  `    if(this.readyState === 2) {`
3.  `        document.querySelector(".loading").style.display = "block";`
4.  `        document.title = "Nom Nom | Loading…";`
5.  `    }`
6.  `    if(this.readyState === 4 && this.status === 200) {`
7.  `        document.querySelector(".details").style.display = "grid";`
8.  `        document.querySelector(".details").style.gridTemplateColumns = "30% 70%";`
9.  `        document.querySelector(".loading").style.display = "none";`
10.  `        addRecipeDetails(JSON.parse(this.responseText).meals[0]);`
11.  `    }`
12.  `}`

    **Code 10.30:** Updating the recipe-detail.js to update hide/show of details container

As shown in *[code example 10.30](#c10.xhtml_co10_30)*, we have now updated the code to ensure that the details container becomes **`display: grid`** when the response is received. When we save this and refresh our page, we will see the loading icon before the recipe detail is shown:

![](images/Figure-10.23.jpg)

**Figure 10.23:** The loading text seen on the recipe-detail page

With this, we have successfully added the loading icons wherever necessary.

# [Error Handling](#toc.xhtml_s221a)

Now, the only thing remaining for our application is to handle the UI when the requests fail. If you trigger a request error by adding a random character in the URL passed in **`request.open()`** method of both **`index.js`** and **`recipe-detail.js`**, you will see that the recipes do not load, but the page remains blank. To resolve this, all we need to do is add the error handling messages in our HTML files and control their display through the **`onreadystatechange`** property as we did in the previous section.

In both **`index.html`** and **`recipe-detail.html`**, we will add the following line at the end of the body tag just before we import our JS files:

`<p class="error">Oops! Looks like the connection to the server failed!</p>`

**Code 10.31:** Adding the error message to both the HTML files.

We want to make sure that this text is not seen by default, so we will add the following line in **`common.css`**:

1.  `.error {`
2.  `    display: none;`
3.  `}`

    **Code 10.32:** Making sure the error message remains hidden by default

Now, we need to handle its display in our JS files. In both the JS files, inside the **`onreadystatechange`** property, we will add the following lines after the if condition of **`readyState === 4`**:

1.  `else if(this.readyState === 4 && this.status !== 200) {`
2.  `    handleNetworkFailure();`
3.  `}`

    **Code 10.33:** Adding the callback function to handle errors

In *[code example 10.33](#c10.xhtml_co10_33)*, we will call the **`handleNetworkFailure`** function if the status code is not 200, that is, if the response is not successful.

Now, we will create the **`handleNetworkFailure`** function in both the files. In **`index.js`**, we will write the following code inside the **`handleNetworkFailure`** function:

1.  `const handleNetworkFailure = () => {`
2.  `    document.querySelector(".recipes-container").style.display = "none";`
3.  `    document.querySelector(".error").style.display = "block";`
4.  `}`

    **Code 10.34:** Defining the callback function to handle errors in index.js

Similarly, in the **`recipe-detail.js`**, we will add the following code:

1.  `const handleNetworkFailure = () => {`
2.  `    document.querySelector(".recipe-details-container").style.display = "none";`
3.  `    document.querySelector(".error").style.display = "block";`
4.  `}`

    **Code 10.35:** Defining the callback function to handle errors in recipe-detail.js

Finally, on a failed request, our web page could show a message like the following:

![](images/Figure-10.24.jpg)

**Figure 10.24:** The error message on request failure

With this, we have finally completed developing a live application – *Nom Nom*!

You can view the website on - **[https://rushabhshah1993.github.io/nomnom/](https://rushabhshah1993.github.io/nomnom/)**

You can check out the entire code here - **[https://github.com/rushabhshah1993/nomnom](https://github.com/rushabhshah1993/nomnom)**

# [Conclusion](#toc.xhtml_s222a)

In this chapter, we used the knowledge that we had acquired in the last nine chapters to create a live web application. This application has been powered by the generous public API platform MealDB. Throughout this chapter, we have tried our best to imitate the real-life software development. While we used a majority of the JavaScript concepts learned in the last nine chapters, we also learned a new concept of **`window.location`**. We used this concept extensively in our application.

In the next chapter, we will be learning how to store data on the client browsers. Storing data on the client browsers helps save a lot of network bandwidth and improve the performance of our websites.

# [Points to remember](#toc.xhtml_s223a)

*   The first tip for creating a great website is to think from a user’s perspective. Everything from the design to the functionality should be created, keeping the user in mind.
*   Next, you need to make sure your design is clean. Users will seldom be happy with a cluttered design and lot of animations.
*   Write modular code. You should write code that can be separated into smaller functions. Also, it would help if you could write codes that can be reused.

# [Multiple choice questions](#toc.xhtml_s224a)

1.  **The query parameters string is stored in which property of the** **`window.location`** **object?**
    1.  search
    2.  hostname
    3.  origin
    4.  pathname
2.  **System testing is the end-to-end testing of the entire application in client-like environment – True or False?**
    1.  True
    2.  False

# [Answers](#toc.xhtml_s225a)

1.  **a**
2.  **a**

# [CHAPTER 11](#toc.xhtml_c11)

# [Storing Data in Browsers](#toc.xhtml_c11)

In the last chapter, we read that the vast majority of the websites on the internet these days are dynamic. These websites store data in the servers, request servers to send the data when needed, and use the response data to show the user the HTML. However, to improve the performance of the web page and save network bandwidth, modern web browsers support several ways to store data on the user's machine itself. It will not only save network bandwidth, but also increase the loading speed of the website and save websites for offline use. In this chapter, we will look at the several methods allowed by the browser to store data.

# [Structure](#toc.xhtml_s226a)

In this chapter, we will cover the following topics:

*   Introduction to Web Storage
*   Cookies
*   Web Storage APIs
*   IndexedDB API
*   Service workers
*   Cache API
*   Testing on console

# [Objective](#toc.xhtml_s227a)

After studying this chapter, you should be able to improve the performance and speed of your web application/website by storing data in the browsers. You can implement the various web storage methods and understand when to cache data or implement web storage.

# [Introduction to Web Storage](#toc.xhtml_s228a)

As mentioned earlier, in the previous chapter, we implemented an example where we fetched data from a server to populate the HTML of our web page. However, there might be several cases where storing data in the user's browser makes more sense. For instance, if you are developing an e-commerce website, it makes sense to remember the content stored in a user's cart from the previous session. Another instance is when the user wants the browser to remember that he/she has logged in, so that they don’t have to login the next time they open the web page. In such cases, it is wise to store some data on the browser. This process is known as *client-side storage*.

The client-side storage involves JavaScript API that allows data to be stored on your machine. This information can be retrieved when necessary. The several benefits of having client-side storage are as follows:

*   For personalizing the website preferences (for example, dark/light theme of the website, color scheme, font-size, and so on.)
*   Storing the user activity (for example, storing items stored in the user’s cart from the previous sessions, remembering the user’s login, and so on.)
*   Saving assets like font, images, and so on, and data on the machine browser to save time and bandwidth on re-downloading the resources. This can help load the site faster as it removes the time to reach the server, waiting for the server response, and the time for downloading the assets.
*   Save certain documents locally to enable viewing the website online.

Based on the time when they were introduced, we can divide the web storage practices into three distinct categories (at the time of writing):

*   **Old School**: The earliest method of client-side storage that is still in practice on many websites are HTTP cookies. To a greater extent, majority of the websites use cookies for user personalization or showing personalized advertisements to the user on their webpages.
*   **New School**: At the time of writing, the most common and easier methods of storing data on browsers are Web Storage APIs and IndexedDB APIs. The former is useful for storing simple data like the user’s name, or whether the user has selected a dark or a light theme. The latter is useful for storing complex databases.
*   **The Future**: The concept of cache has been a part of the web development industry since a long time. However, at the time of writing, only few modern web browsers support the new Cache API. Cache APIs work in tandem with the Service Worker APIs. They are useful for offline storage of data.

In this chapter, we will be touching base on all the five types of web storage. However, we will pay more attention to the Web Storage APIs. At this point in time, the Web Storage APIs are more proficient in nature.

# [Cookies](#toc.xhtml_s229a)

HTTP Cookies are small pieces of data sent by the server to a user’s browser. These cookies are generally stored in the form of text files on the user’s browser. The browser attaches this cookie with later requests to the same server.

In a more general sense of view, servers treat every request as a new request, that is, servers and the HTTP protocol do not maintain a state of the requests. By sending the stored cookie in a user’s browser, it is possible for the servers to "*remember*" the information about the user.

# [Usage](#toc.xhtml_s230a)

Cookies are mainly used for the following three purposes:

![](images/Figure-11.1.jpg)

**Figure 11.1:** Usage of cookies

As shown in the preceding screenshot, cookies have been serving three important purposes since JavaScript introduced them. The first one is session management. It includes helping the server remember important information about the user, including but not limited to, logins, shopping carts, games scores, and so on. The second use case is for remembering user preferences and themes. Cookies are majorly used for the third scenario – to record and analyse user behaviour. It helps the server understand user’s behavioural patterns.

# [Disadvantage](#toc.xhtml_s231a)

A major disadvantage of cookies is that they are sent with every server request which could potentially worsen the speed and performance of the webpage. As per the official documents of Microsoft, majority of the browsers support cookies of maximum 4096 bytes, which is a relatively small size.

# [Structure](#toc.xhtml_s232a)

Cookies are saved in name-values pairs like the following:

`username = john.doe`

**Code 11.1:** Structure of a cookie

# [Creating cookie with JavaScript](#toc.xhtml_s233a)

To create, read, or delete cookies, we use the JavaScript property **`document.cookie`**.

`document.cookie = "username=john.doe; expires=Fri, 27 Nov 2020 20:08:00 GMT; path: /"`

**Code 11.2:** Setting a cookie with JavaScript

As shown in *[code example 11.2](#c11.xhtml_co11_2)*, to set a cookie with JavaScript, you need to assign a string value to the **`document.cookie`** property. By default, the cookie is deleted when the browser is closed. To set the cookie to expire at a later time, you can add the name-value pair of expires with a date for expiry. Similarly, the path key tells the browser what path the cookie belongs to.

# [Reading cookies with JavaScript](#toc.xhtml_s234a)

By typing **`document.cookie`**, you will fetch all the values of the cookie stored for the particular webpage in the browser. It will return all the values in one string. To fetch the cookies by their name-value pairs, you can then create a function to split the string on semicolon:

1.  `document.cookie = "username=john.doe; theme=dark; expires=Fri, 27 Nov 2020 20:08:00 GMT; path: /";`

3.  `console.log(document.cookie);`
4.  `console.log(document.cookie.split(";"));`

    **Code 11.3:** Reading a cookie with JavaScript

When you type the preceding code in your JS file and open your web page and the Developer Console, you will see the following:

![](images/Figure-11.2.jpg)

**Figure 11.2:** Output of [code example 11.3](#c11.xhtml_co11_3)

# [Deleting cookies with JavaScript](#toc.xhtml_s235a)

To delete a cookie, you can select a cookie by its path and set its expiry date to a past time. This will delete the cookie.

# [Security](#toc.xhtml_s236a)

It’s important to remember that cookies can pose a direct threat to user privacy if set using JavaScript. Since values of cookies can be accessed using JavaScript, it is important to never add sensitive data to the cookies set using JavaScript. Alternatively, while creating requests and responses, servers can set the attribute **`HttpOnly`** to prevent access to cookie values using JavaScript.

# [Third-party cookies](#toc.xhtml_s237a)

A cookie is associated with a domain. A domain name is the name that the users can use to access your website. For instance, *facebook.com* is the domain name for the Facebook web application. If the domain associated with a cookie is the same as the domain of the web page you are on, it is known as a first-party cookie. However, if the domain is different, then it is known as a third-party cookie. Websites normally allow third-party cookies for advertisements and banners. A third-party server can build up a user’s profile by tracking its behaviour and browsing history when this cookie is sent to it when accessing multiple websites. Since this is a major security hazard, many browsers allow third-party cookies to be blocked. This may cause several web pages to not function properly.

# [Web storage APIs](#toc.xhtml_s238a)

The Web Storage APIs provide two mechanisms to store data in a more secure and intuitive fashion than cookies. Unlike cookies, web storage is far more secure as large amount of data is stored locally on the browser and this information is never sent to the server. Moreover, the storage limit is far larger (at least 5 MB).

HTML Web Storage provides the following two objects for storing data on the browser:

*   **`window.localStorage`**
*   **`window.sessionStorage`**

Both the objects store data on the browser. However, the major difference between the two is that the **`sessionStorage`** object stores data only for one session, that is, data will be deleted if the browser is closed, while **`localStorage`** persists the data with no expiration date.

# [Session Storage](#toc.xhtml_s239a)

The session storage object stores the data only for one session. It means once the browser or the tab with the web page is closed, all the data inside the session storage will be deleted. However, refreshing the web page or restoring the web page will not remove the data inside the session storage.

# [Setting the value inside session storage](#toc.xhtml_s240a)

To set the value with the **`sessionStorage`** object, we use the **`setItem`** method of the **`sessionStorage`** object. The **`setItem`** method accepts two arguments – a key and a value. Let’s understand this with an example. Create a simple index.html file and an **`index.js`** file. Import the index.js file inside the **`index.html`** file. Inside the **`index.js`** file, type the following command:

`sessionStorage.setItem("username", "john.doe");`

**Code 11.4:** Setting a value for session storage.

The code in *[code example 11.4](#c11.xhtml_co11_4)* will set the value of the username inside the session storage to **`john.doe`**.

# [Fetching the value from session storage](#toc.xhtml_s241a)

To fetch the value stored inside the session storage object, you can use the **`getItem`** method of the **`sessionStorage`** object. Inside the **`getItem`** method, you should pass the key name for the value you intend to fetch. Continuing with the previous example, to fetch the value set with the key username, you can add the following code in **`index.js`**:

`console.log(sessionStorage.getItem("username"));`

**Code 11.5:** Getting a value in session storage.

Typing the preceding code in **`index.js`** and refreshing the page will show the following value in the console:

![](images/Figure-11.3.jpg)

**Figure 11.3:** Output of [code example 11.5](#c11.xhtml_co11_5)

Now, inside your **`index.js`**, remove the code written in *[code example 11.4](#c11.xhtml_co11_4)* and only keep the code written in *[code example 11.5](#c11.xhtml_co11_5)*. It means you are not setting any value inside the session storage, but only fetching the value of username set inside the session storage. When you refresh the page, you will still see the output seen in *[figure 11.3](#c11.xhtml_fig11_3)*. Now, close the tab and reopen the **`index.html`** file. If you now check the console, you will find that the value of **`getItem`** is null. This shows that the data inside **`sessionStorage`** is deleted when you close the tab.

# [Removing a value from session storage](#toc.xhtml_s242a)

The data inside the session storage gets deleted on its own when the browser or the tab is closed. However, if you still want to remove the data before this action, you can use the **`removeItem`** method of the **`sessionStorage`** object.

To remove a single data, you need to add the name of the key you wish to remove inside the parentheses of the method.

`sessionStorage.removeItem("username");`

**Code 11.6:** Removing a value from session storage.

To remove all the data from the **`sessionStorage`**, you can use the following method:

`sessionStorage.clear();`

**Code 11.7:** Removing all data from sessionStorage

# [Local Storage](#toc.xhtml_s243a)

Local storage is similar to the session storage in terms of the methods and the principle of storing data in the browsers. The only difference between them is that the data inside local storage will never expire or delete. Even if the browser or the tab is closed, the data will persist. This data can only be cleared using JavaScript or by clearing the cache of the browser or clearing the locally stored data.

# [Setting the value inside local storage](#toc.xhtml_s244a)

Similar to the **`sessionStorage`** object, to set a value inside **`localStorage`**, you need to use the **`setItem`** method. Like **`sessionStorage`**, the **`setItem`** method accepts two arguments – key name and the value:

`localStorage.setItem("isLogin", true);`

**Code 11.8:** Setting a value inside local storage.

# [Fetching the value from local storage](#toc.xhtml_s245a)

Once again, the value of a key can be fetched from the local storage using the method **`getItem`**. It accepts one argument, that is the name of the key to be passed inside the **`getItem`** method:

`console.log(localStorage.getItem("isLogin"));`

**Code 11.9:** Fetching a value from local storage.

Typing the code shown in *[code example 11.8](#c11.xhtml_co11_8)* will fetch the following output:

![](images/Figure-11.4.jpg)

**Figure 11.4:** Output of [code example 11.8](#c11.xhtml_co11_8)

Now, in **`index.js`**, comment the line that you typed in *[code example 11.8](#c11.xhtml_co11_8)*, save the file, and close the tab/browser. When you reopen **`index.html`**, you will still find the value, as shown in *figure 11.8*. This shows that the data inside a local storage persists.

# [Removing a value from local storage](#toc.xhtml_s246a)

As mentioned earlier, to remove data from a local storage, you need to use either JavaScript to clear it, or you empty the cache of the browser.

To remove individual values, you can use the **`removeItem`** method of the **`localStorage`** object. As seen earlier, you need to add the name of the key you wish to remove inside the parentheses of the method.

`localStorage.removeItem("isLogin");`

**Code 11.10:** Removing a value from local storage.

To flush out the entire **`localStorage`**, you can use the clear method:

`localStorage.clear();`

**Code 11.11:** Removing all data from local storage.

# [IndexedDB API](#toc.xhtml_s247a)

As we saw in the previous section, local storage and web storage can store simple data. To store complex and larger amount of data, we can use the *IndexedDB* API. The advantage of using *IndexedDB* API is replicating an entire database like SQL. The downside of using it is that it involves a lot more process than the Web Storage APIs.

# [Features of IndexedDB API](#toc.xhtml_s248a)

There are several advantages of using *IndexedDB* API. A few of them are as follows:

*   It is a large-scale, NoSQL storage system.
*   It can let you store just about anything in the user’s browser, including files.
*   It supports get, search, put, and also transactions with the data.
*   It is unique to every site domain or subdomain. It means that this database will not be accessible to other websites on the browser.
*   It is mostly asynchronous, that is, it does not affect your website performance.

# [IndexedDB terms](#toc.xhtml_s249a)

Before we begin exploring and using *IndexedDB* API, let’s first understand the terms used in *IndexedDB*:

*   **Database**: This is the highest level of the *IndexedDB*. It contains object stores, which in turn contain the data you would like to store. You can create multiple databases, but it is good practice to have one database per app.
*   **Object Store**: An object store is an individual bucket to store the data. The best analogy for an object store is tables of traditional relational database. You will create object store for every "*type*" of your data. For instance, if you are storing a database for books, "*fiction*" and "*non-fiction*" can be object stores.

    ![](images/Figure-11.5.jpg)

    **Figure 11.5:** Hierarchy in IndexedDB

*   **Index**: Like traditional relational database, an index can be visualized as a column name for retrieving data. For instance, we can fetch a particular book from the fiction object store by the book name, book ID, or author.
*   **Transaction**: A transaction is a wrapper around operations, that is, any interaction with a database. It ensures database integrity. It means if one of the transactions fails, none of them are applied and database returns to the state it was before the transactions began.

# [IndexedDB process](#toc.xhtml_s250a)

The process of *IndexedDB* involves several steps, but the most important are as follows:

![](images/Figure-11.6.jpg)

**Figure 11.6:** Steps of IndexedDB process

The preceding steps will be explained in the next section.

# [Check if IndexedDB is supported](#toc.xhtml_s251a)

The first thing you always need to do is check whether the user’s browser supports IndexedDB. If it doesn’t, ideally you should console a message saying it is not supported. The IndexedDB can be accessed in the window object of the browser. Since we will be needing it frequently, we should store it in a variable. In your **`index.js`**, type the following code:

1.  `let idb = window.indexedDB;`

3.  `if(!idb) {`
4.  `    console.log("Your browser doesn't support IndexedDB!");`
5.  `}`

    **Code 11.12:** Check for IndexedDB support

# [Open the database](#toc.xhtml_s252a)

It’s fair to say that the next step in the process would be to open the database for storing. To open a database, you need to call the open method of the **`window.indexedDB`** object. It takes two parameters – a name for the database and its version. Since it’s a request, you will also be using the **onsuccess** and the **onerror** event handlers to check the status of the request to open a database. Another event handler that we use is the **`onupgradeneeded`** event handler. This event handler is called when we open a request with the same data base name but a higher version number, that is, an upgrade. We will use this event handler in the next section. In the following *[code example 11.13](#c11.xhtml_co11_13)*, we add the code to the **`index.js`** after the code shown in *[code example 11.12](#c11.xhtml_co11_12)*:

1.  `let db;`
2.  `let request = idb.open("newDB", 1);`

4.  `request.onerror = function(event) {`
5.  `    console.log(event);`
6.  `}`
7.  `request.onsuccess = function(event) {`
8.  `    db = request.result;`
9.  `}`

    **Code 11.13:** Opening your database

As shown in *[code example 11.13](#c11.xhtml_co11_13)*, we create a variable db which will store the result of our request on success. Before that, we create a variable request where we call the IndexedDB method open with the database name as "*newDB*" and the version as 1 on the variable idb that we created in *[code example 11.12](#c11.xhtml_co11_12)*. As mentioned earlier, failure of the request will be handled by the onerror event handler, while the success will be handled by the onsuccess event handler. Inside the onsuccess event handler, we store the result of our request in the variable db.

# [Add data](#toc.xhtml_s253a)

We can add data to the database that we have created in *[code examples 11.12](#c11.xhtml_co11_12)* and *[11.13](#c11.xhtml_co11_13)* in the following two ways:

*   In the previous section, we learned about an event handler called **`onupgradeneeded`**. This event is called whenever a new request is opened with a higher version. This will also be called the first time an open request is created.
*   When an add function is explicitly called to add data to the database.

In the section – IndexedDB terms, we had seen that every database has an object store which contains the actual data. So, the very first step is to create the object store. Since the **`onupgradeneeded`** function is called the first time, we will create the object store inside it.

In our **`index.js`**, we will add the following lines after the code that you have added in *[code example 11.13](#c11.xhtml_co11_13)*:

1.  `const data = [`
2.  `    {id: "01", name: "John Doe", age: 27},`
3.  `    {id: "02", name: "Jane Doe", age: 27}`
4.  `];`

6.  `request.onupgradeneeded = function(event) {`
7.  `    let db = event.target.result;`
8.  `    let objectStore = db.createObjectStore("employee", {keyPath: "id", autoIncrement: true});`
9.  `    objectStore.add(data[0]);`
10.  `}`

    **Code 11.14:** Creating onupgradeneeded function

In *[code example 11.14](#c11.xhtml_co11_14)*, we have stored the result of the request in the variable db. Next, we will use the **`createObjectStore`** method of the IndexedDB object. The **`createObjectStore`** method requires a mandatory argument of a name. In terms of analogy, this will be equivalent to setting the name of the table for a database. We can also pass optional parameters while creating an object store. The optional parameters can be as follows:

*   **keypath**: It will define the key name or the column name for identifying a particular data. For instance, in *[code example 11.14](#c11.xhtml_co11_14)*, an individual employee can be fetched and identified with the help of the key "id".
*   **autoincrement**: It means a key will be automatically generated for every data inside the object store.

Finally, we use the add method to add the first row of the data to the object store "**`employee`**" of the database "**`newDB`**".

An alternate way of adding data is by creating an explicit function for adding data. In the following *[code example 11.15](#c11.xhtml_co11_15)*, we have achieved that:

1.  `function add() {`
2.  `    let request = db.transaction(["employee"], "readwrite");`
3.  `    let objectStore = request.objectStore("employee")`
4.  `    let storeRequest = objectStore.add(data[1]);`
5.  `}`

    **Code 11.15:** Creating add function

In *[code example 11.15](#c11.xhtml_co11_15)*, since we have already created the **`objectStore`** once, we will use the transaction method of the IndexedDB object to return a transaction containing the **`objectStore`** method. This **`objectStore`** method will be useful for accessing the object store. The transaction method requires the following three arguments:

*   The first mandatory argument is for providing the object store names (in case of multiple store names, we use an array).
*   The optional second argument is for providing the mode or the type of access – **`readonly`**, **`readwrite`**, or **`readwriteflush`** for accessing the object store. We will use the **`readwrite`** mode to write/update into our object store employee. The result of this request is stored in the variable request.
*   The third argument is also optional. It will store the options for storing the cache.

Next, once the request has been created, we will obtain the **`objectStore`** we require from inside the request. Since the transaction method allows us to fetch multiple object stores, we will require the **`objectStore`** method to fetch the object store we require.

Finally, we add the second object inside the data array to the **`objectStore`** employee.

For sanity, we will call this add method through a button call only after the entire JS file has been parsed and all the requests have been completed.

# [View data](#toc.xhtml_s254a)

The final thing we need to do is view the data stored in the IndexedDB. We can do that with the help of the following function:

1.  `function read() {`
2.  `    let transaction = db.transaction(["employee"]);`
3.  `    let objectStore = transaction.objectStore("employee");`
4.  `    let request = objectStore.get("02");`
5.  `    request.onerror = function(event) {alert("Unable to retrieve!");};`
6.  `    request.onsuccess = function(event) {console.log(request.result);}`
7.  `}`

    **Code 11.16:** Viewing data stored in object stores

For viewing the data, we have created a read function in *[code example 11.16](#c11.xhtml_co11_16)*. In this function, we use the transaction and the **`objectStore`** method used in *[code example 11.15](#c11.xhtml_co11_15)* to fetch our object store employee. After we get our object store employee, we will use the get method to fetch data from inside the employee object store. As we had noted earlier in the **`createObjectStore`** method of *[code example 11.14](#c11.xhtml_co11_14)*, we will pass the id value as an argument to the get request. As it is with requests, errors will be handled by **`onerror`** event handler, and the success will be handled by the **`onsuccess`** event handler.

As you can see, IndexedDB is mighty useful for storing large and complex data. However, it comes at the cost of writing extra code.

# [Service workers](#toc.xhtml_s255a)

At this point in time, we will not be studying the concepts of service workers and caching in detail. However, we will spend a considerable amount of time to understand the idea behind both the concepts.

Service workers act like proxy servers sitting between web applications, the browsers, and the network (when available). Service workers are normally used for providing a rich offline viewing experience for websites. Service workers work in close conjunction with the Cache APIs to provide this experience. They intercept network requests and take appropriate action based on whether the network is available. They also allow access to push notifications and background sync APIs.

A service worker is a JavaScript file that controls the webpage that it is associated with. It intercepts and modifies navigation and resource requests. It caches resources to give you full control on how the webpage will behave in certain situations (especially when network is not available).

Service workers have no DOM access. In fact, it runs on a different thread to the main JavaScript of your webpage. Hence, it will not block your rendering. Service workers only run over HTTPS, for security reasons.

There are four steps for working with service workers:

![](images/Figure-11.7.jpg)

**Figure 11.7:** Steps for Service Workers

To sum up the process, first you need to check whether the browser supports service workers. If it supports, we will register the service worker. Next, it downloads the service worker and installs it. After installation, it gets activated. Let’s quickly look at an example of a service worker. This example is inspired from the one provided on MDN.

Inside the folder, where we have created the **`index.html`** and the **`index.js`** for IndexedDB, we will create another file called sw.js. Inside **`sw.js`**, we will type the following code:

1.  `self.addEventListener('install', function(e) {`
2.  `    e.waitUntil(`
3.  `        caches.open('employees').then(function(cache) {`
4.  `            return cache.addAll([`
5.  `                '/index.html',`
6.  `                '/index.js'`
7.  `            ]);`
8.  `        })`
9.  `    );`
10.  `});`

    **Code 11.18:** Registering the service worker

In the preceding *[code example 11.18](#c11.xhtml_co11_18)*, we call the method self of the JavaScript window object. It is corresponding to the current window opened on the browser. We add an event listener for an installation on the window. Inside, we call the **`waitUntil`** method of the event object to request the browser to complete the promise passed as parameters. Only after it has been completed, the installation should be completed. Inside the parameters, we call the open method of the Caches API (similar to IndexedDB), and in its promise, we ask cache to store the **`index.html`** and the **`index.js`** files on the browser.

Inside the **`index.js`**, we will add the following code:

1.  `if('serviceWorker' in navigator) {`
2.  `    navigator.serviceWorker`
3.  `            .register('sw.js')`
4.  `            .then(function() {console.log("Service Worker registered");})`
5.  `}`

    **Code 11.19:** Registering the service worker

In the preceding *[code example 11.19](#c11.xhtml_co11_19)*, we first test if **`serviceWorker`** is accepted on the browser. If yes, we call the **`serviceWorker`** method of the navigator object (the JavaScript navigator object corresponds to the browser). We call the register method to register the **`sw.js`** file that we have created in *[code example 11.18](#c11.xhtml_co11_18)*. Since it is a JavaScript Promise, we can add the then and the catch methods for its success and failure respectively. When you run this, the preceding files will be stored inside your browser as cache. We will look into this in the last section of this chapter.

# [Caches](#toc.xhtml_s256a)

The Caches API is an interface that is often used with Service Workers to cache, that is, store data on the browser. By storing data as cache in the browser, you can save valuable network bandwidth and server webpages faster. We will not be looking at Caches API in detail in this section.

In the previous section, we used the **`addAll`** method of the Cache interface to take an array of URLs, retrieve them, and add them to the cache. There are several available methods of the Cache interface. Let’s add one piece of code to the code that we have been writing in this chapter. So far, in the previous section, we have stored index.html and index.js files in the cache. Now, let’s write a code to serve these files instead of sending a request the next time.

Inside **`sw.js`**, add the following lines:

1.  `self.addEventListener('fetch', function(e) {`
2.  `    console.log(e.request.url);`
3.  `    e.respondWith(`
4.  `        caches.match(e.request).then(function(response) {`
5.  `            return response || fetch(e.request);`
6.  `        })`
7.  `    )`
8.  `})`

    **Code 11.20:** Using cache to serve web pages

In the preceding *[code example 11.20](#c11.xhtml_co11_20)*, we add another event listener to the current window opened on the browser. We check for fetch requests. If they exist, the **`callback`** function is called where we check the requested URL. Inside the fetch event’s method **`respondWith`**, we then use the Cache interface’s method match for checking whether the request exists in the cache. If it exists, we return that as response, or we ask the browser to send the request.

You can check the entire Cache API here: **[https://developer.mozilla.org/en-US/docs/Web/API/Cache](https://developer.mozilla.org/en-US/docs/Web/API/Cache)**.

# [Testing on Console](#toc.xhtml_s257a)

You can check the web storage of any web page on the Application panel of the Developer Tools for Google Chrome. When you open the Application Panel of the Chrome Developer Tools, you will notice a sidebar which has options ranging from service workers, local storage, to cache. You can check every option to see the values registered by our **`index.js`** file. To test the service workers, you will need to make use of a Visual Studio plugin called *Live Server*. Since service workers work only on HTTPS, you will need to open index.html, using a live server to check the service workers.

# [Conclusion](#toc.xhtml_s258a)

In this chapter, we have learned about the several client-side storage options for JavaScript. Amongst the five options, the easiest and the most commonly used client-side storage options are the Web Storage APIs – Local Storage and Session Storage. As we have seen, every option caters to a different need of the user and the website. We also learned about Cookies, IndexedDB, Service Workers, and Cache API. Cookies are a traditional method of storing data. IndexedDB are used for storing complex data. The last two are used for storing cache. In the next chapter, we will be looking at debugging and handling errors using JavaScript.

# [Points to remember](#toc.xhtml_s259a)

*   Web Storage, that is, client-side storage helps improve the speed and the performance of the website by storing data in the user browser.
*   Cookies are a traditional way of storing data on the browser. However, third-party cookies are known for encroaching upon user privacy.
*   Session storage stores data until the user session, that is, the browser/tab is open. Local Storage retains data with no expiry date.
*   IndexedDB is used for storing large amount of complex data.
*   Service Workers and Caches API work in tandem to serve offline pages.

# [Multiple choice questions](#toc.xhtml_s260a)

1.  **Service Workers can work with local resources or HTTP – True or False?**
    1.  True
    2.  False
2.  **What method is used for clearing data inside Web Storage APIs?**
    1.  clear
    2.  remove
    3.  empty

# [Answers](#toc.xhtml_s261a)

1.  **b**
2.  **a**

# [CHAPTER 12](#toc.xhtml_c12)

# [Debugging and Error Handling](#toc.xhtml_c12)

You will remember that in *[Chapter 10: Live Application Development](#c10.xhtml)*, we faced a bunch of errors or issues while developing our application. In every practical scenario, you are bound to face some errors while using a programming language. While some of these errors or bugs are relatively minor, and will not affect the user's experience while using your application, you will also find several errors or bugs that will crash your web page/application. It's moot to mention here that if you, as a user, find an application that you intend to use frequently (for instance, a stocks application or a social media application), crashing often, you will stop using that application. In fact, you might look for alternatives. Therefore, it is crucial to detect and find errors. In this chapter, we will first learn about the several ways to debug (identify) errors using examples, and then we will explore ways to handle those errors.

# [Structure](#toc.xhtml_s262a)

In this chapter, we will cover the following topics:

*   Errors
*   Introduction to Debugging
*   The **`console.log()`** method
*   Debugging with breakpoints
*   The debugger keyword
*   Try, catch, and finally

# [Objective](#toc.xhtml_s263a)

After studying this chapter, you should be able to diagnose and detect where errors are happening and utilize JavaScript methods to rectify errors. You will learn how to use JavaScript methods to handle erroneous code without letting it impact the UI.

# [Errors](#toc.xhtml_s264a)

In JavaScript, errors happen when a mistake or an issue is found in your code. Whenever a runtime error occurs, the JavaScript Error objects are thrown. These errors are often shown in a red background on the **`Console`** panel of the browser’s developer tools.

As we learned earlier, several errors can impact the **`User Interface`** (**`UI`**) of your application. Often, when an error occurs in your JavaScript, the JavaScript execution stops at that point. This can also stop the rendering of the HTML on your web page, if not handled. At this point, if the rendering stops, the user could possibly end up looking at a blank screen with no notification of what is happening. As a result, many users will simply stop using the application and leave. To avoid this, we will first understand the several types of errors. After that, we will learn how to debug, that is, identify or detect these errors, and finally we will learn how to handle these errors from impacting the rest of the code or the UI.

# [Types of Errors](#toc.xhtml_s265a)

There are several error constructors that are thrown for specific issues in your JavaScript. Let’s have a look at the several error constructors:

# [EvalError](#toc.xhtml_s266a)

An EvalError is thrown when an error occurs with the global **`eval()`** function. The **`eval()`** function is used for evaluating or executing expressions inside its argument. This exception is not thrown by JavaScript anymore; however, the **`EvalError`** object remains for compatibility.

# [RangeError](#toc.xhtml_s267a)

A RangeError is thrown when a value is outside the set or range of legal values. For instance, as shown in *[code example 12.1](#c12.xhtml_co12_1)*, we are using the **`toFixed()`** method of the Number object. The permissible range for the argument inside the **`toFixed()`** method is between 0 and 100. However, in *[code example 12.1](#c12.xhtml_co12_1)*, we are passing the argument as 500, which is outside the range of legal values.

1.  `let number = 200;`
2.  `number.toFixed(500);`

    **Code 12.1:** An erroneous code for RangeError

When we execute the preceding code, we will see the following message on the Console Panel of the Developer Tools:

![](images/Figure-12.1.jpg)

**Figure 12.1:** The RangeError thrown for [code example 12.1](#c12.xhtml_co12_1)

# [ReferenceError](#toc.xhtml_s268a)

The ReferenceError is thrown when a non-existent variable is referenced. For instance, in the following screenshot, we try to refer the variable person which has not yet been declared. Hence, it results in the **`ReferenceError`** being thrown:

![](images/Figure-12.2.jpg)

**Figure 12.2:** An example of ReferenceError

# [SyntaxError](#toc.xhtml_s269a)

It is thrown when JavaScript encounters a code with incorrect syntax. We can see one such example in the following screenshot:

![](images/Figure-12.3.jpg)

**Figure 12.3:** An example of SyntaxError

In *[figure 12.3](#c12.xhtml_fig12_3)*, we have wrapped the string inside the variable name with quotes. We open the string with double quotes. However, we end it with a single quote. Since this is syntactically wrong, a SyntaxError is thrown.

# [TypeError](#toc.xhtml_s270a)

A TypeError is thrown when JavaScript cannot execute a code because the value is not of the expected type. A TypeError can occur in the following cases:

*   An argument passed inside a function is incompatible with the type expected by the function.
*   Attempting to modify a value that cannot be changed.
*   Attempting to use a value in an inappropriate way.

For instance, in the following screenshot, we are using the **`toFixed`** method of the Number object for a string stored inside the variable name. As you can see, it results in a **`TypeError`**:

![](images/Figure-12.4.jpg)

**Figure 12.4:** An example of TypeError

# [URIError](#toc.xhtml_s271a)

Finally, the URIError is thrown when you use illegal characters in a **Uniform Resource Identifier** (**URI**) function. URI is a string that refers to a resource. A **Uniform Resource Locator** (**URL**) is a type of URI that is used for identifying location on the Web. JavaScript has functions to encode or decode URI. If you pass illegal characters like ‘%’ in the JavaScript **`decodeURI`** function, as shown in the following screenshot, you will receive an **`URIError`**:

![](images/Figure-12.5.jpg)

**Figure 12.5:** An example of URIError

There are two more types of errors – AggregateError and InternalError. The former – AggregateError simply represents an error when several errors need to be wrapped in a single error. The latter – InternalError is not standard and hence, it’s recommended to not use it for any website that will be used by users.

# [Introduction to Debugging](#toc.xhtml_s272a)

If you are creating a complex application (for instance, an e-commerce application like Amazon), you will be writing several hundred lines of code. In such a vast JavaScript file, there are higher chances of encountering or writing a code which may contain errors. You might accidentally forget adding the closing quotes for a string, or you might accidentally refer a variable without declaring it first.

Debugging is the process of searching for and identifying these errors. In the upcoming sections, we will look at various methods to debug errors in the JavaScript code.

We will be using the following erroneous JavaScript code for debugging in the next sections:

1.  `const add = (num1, num2) => {`
2.  `    return num1 + num2;`
3.  `}`

5.  `let number1 = "20";`
6.  `let number2 = Math.random()*100.toFixed(500);`

8.  `let sum = add(number1, number2);`

10.  ``document.getElementById("result").innerText = `The result of ${number1} and ${number2} is ${sum}.`;``

    **Code 12.2:** An erroneous code for debugging

In the previous section, we looked at several types of errors thrown by JavaScript. It will help us in identifying the mistake we have made in our JavaScript code. Now that we have a fair idea about the types of errors, it should be a little easier for us to understand how to detect these errors.

# [The console.log() method](#toc.xhtml_s273a)

We have seen and used the **`console.log()`** method in the previous chapter. The **`console.log()`** method writes a message to the console. Let’s try to understand how we can use this method to debug code that is shown in *[code example 12.2](#c12.xhtml_co12_2)*.

We will first create a folder for implementing this code. There are several options to execute JavaScript code; however, to continue the method that we have been following over the last few chapters, we will create a new folder with an HTML and a JavaScript file. We will name our HTML file as **`index.html`** and inside the body, we will create a **`p`** element with the **`id`** result. After adding the HTML file, our **`index.html`** file will look like the following:

1.  `<!DOCTYPE html>`
2.  `<html lang="en">`
3.  `<head>`
4.  `    <meta charset="UTF-8">`
5.  `    <meta name="viewport" content="width=device-width, initial-scale=1.0">`
6.  `    <title>Debugging</title>`
7.  `</head>`
8.  `<body>`
9.  `    <p id="result"></p>`
10.  `    <script src="index.js"></script>`
11.  `</body>`
12.  `</html>`

    **Code 12.3:** The index.html file

We will name the JavaScript file as **`index.js`**, and we will paste the code from *[code example 12.2](#c12.xhtml_co12_2)* inside our **`index.js`** file. When we save both the files and open **`index.html`**, we will see a blank screen. Upon opening the Console Panel inside the Developer Tools, you will see the following:

![](images/Figure-12.6.jpg)

**Figure 12.6:** The error message for index.html

As shown in the preceding screenshot, we have received a SyntaxError for our code. As we have seen in *[Chapter 2: The Developer’s Tools](#c02.xhtml)*, the text **`index.js:6`** refers to the place where the error occurred. It means the error occurred on line number 6 of **`index.js`**. If we look at line number 6 of *[code example 12.2](#c12.xhtml_co12_2)*, it looks like the error happened with the definition of the variable number2.

Let’s try to understand our mistake while defining the variable. On line number 6, we are doing two things. First, we are using the **`Math.random()`** function to generate a random number, and we are multiplying this randomly generated number by 100\. Next, we are using the **`toFixed`** method of the Number object on this, and passing an argument 500 to this **`toFixed`** method. Let’s use **`console.log()`** method to check these two values one-by-one. So, we will comment the code starting from line number 6 of *[code example 12.2](#c12.xhtml_co12_2)*, and on the previous line, add the following code:

1.  `console.log(Math.random());`

    **Code 12.4:** Adding console.log to Math.raandom()

When we save the preceding changes in *[code example 12.2](#c12.xhtml_co12_2)* and refresh our web page, we will see the following value in the console:

![](images/Figure-12.7.jpg)

**Figure 12.7:** The console after adding [code example 12.4](#c12.xhtml_co12_4)

In the preceding screenshot, we can see that the value **`Math.random()`** is correct and it is not returning the error. Let’s add the next step to our code to check if that is the reason for our error. Updating the *[code example 12.4](#c12.xhtml_co12_4)*, we will now multiply that value by 100:

1.  `console.log(Math.random()*100);`

    **Code 12.5:** Checking multiplication by 100

Saving this update and refreshing the page gives us a new value in the console:

![](images/Figure-12.8.jpg)

**Figure 12.8:** The console after adding [code example 12.5](#c12.xhtml_co12_5)

The **`Math.random()`** function returns a new number every time. Comparing *[figures 12.7](#c12.xhtml_fig12_7)* and *[12.8](#c12.xhtml_fig12_8)*, we can see that it looks like the new number generated using **`Math.random()`** function is now multiplied by 100 and it returns the value shown in *[figure 12.8](#c12.xhtml_fig12_8)*. Again, we have not encountered an error. So, let’s add the next step – adding a **`toFixed`** function to the *[code example 12.5](#c12.xhtml_co12_5)*:

1.  `console.log(Math.random()*100.toFixed());`

    **Code 12.6:** Adding the toFixed function

When we update our code, as shown in *[code example 12.6](#c12.xhtml_co12_6)*, and refresh the page, we receive the following message in our console:

![](images/Figure-12.9.jpg)

**Figure 12.9:** The console after adding [code example 12.6](#c12.xhtml_co12_6)

As shown in the preceding screenshot, we can finally see where the error is happening. It seems that the **`toFixed()`** function does not work on the *[code example 12.5](#c12.xhtml_co12_5)*. Let’s try to explore the reason why we received this error. We know that **`Math.random()*100`** gives us the correct value. From the previous chapters, we also know that the **`toFixed()`** function works perfectly on the data type number. However, it looks like we are applying the **`toFixed()`** method on the *100 part of our code, that is, an incomplete part of an expression. To make sure the **`toFixed()`** method is applied to the entire expression, we will place our entire expression inside parentheses and apply the **`toFixed()`** method to this expression inside parentheses:

1.  `console.log((Math.random()*100).toFixed());`

    **Code 12.7:** Adding the toFixed function to the parentheses

When we update the code with *[code example 12.7](#c12.xhtml_co12_7)* and refresh our page, we will see that we no longer receive any errors. Instead, we now see a number on our console:

![](images/Figure-12.10.jpg)

**Figure 12.10:** No errors seen on the console.

So, it looks like we have resolved the error. Let’s add the final step seen in line number 6 of *[code example 12.2](#c12.xhtml_co12_2)* to check whether that results in an error or not. So, let’s add the value 500 as an argument inside the parentheses of the code, seen in *[code example 12.7](#c12.xhtml_co12_7)*.

1.  `console.log((Math.random()*100).toFixed(500));`

    **Code 12.8:** Adding 500 as an argument to toFixed method

When we refresh our webpage after making the preceding changes, we will see that we have received another error on our console:

![](images/Figure-12.11.jpg)

**Figure 12.11:** A new error occurs in the code

This time, we see a rather straightforward error of **`RangeError`**. As we have seen in the previous section, a **`RangeError`** happens when you provide a value which is outside the set or range of legal values. Fortunately, in *[figure 12.11](#c12.xhtml_fig12_11)*, JavaScript tells us the actual range of values that needs to be added for the **`toFixed()`** method. So, let’s update the code in *[code example 12.8](#c12.xhtml_co12_8)* and replace the value 500 with 2\. When we save this and refresh the page, we will see that the error is removed and a new number with two decimals is seen instead:

![](images/Figure-12.12.jpg)

**Figure 12.12:** The errors have been resolved and our code shows no errors.

Now, let’s update our original code in *[code example 12.2](#c12.xhtml_co12_2)* with the preceding changes:

1.  `const add = (num1, num2) => {`
2.  `    return num1 + num2;`
3.  `}`
4.  `let number1 = "20";`
5.  `let number2 = (Math.random()*100).toFixed(2);`

7.  `let sum = add(number1, number2);`
8.  ``document.getElementById("result").innerText = `The result of ${number1} and ${number2} is ${sum}.`;``

    **Code 12.9:** The new updated code with changes to the variable number2

When we save this and refresh our page, we finally get the output of the function **add** without any errors thrown on the console, and the statement on line number 8 is shown on the console like the following:

![](images/Figure-12.13.jpg)

**Figure 12.13:** The output of the [code example 12.9](#c12.xhtml_co12_9)

However, if you observe the preceding screenshot, you will notice that the answer to the addition of the two numbers is wrong. Addition of 20 and 70.30 should result in 90.30, but the value shown is 2070.30\. If you look at the value closely, you will notice that instead of adding the two numbers, they are concatenated. If you remember operators from *[Chapter 1: Introduction to JavaScript](#c01.xhtml)*, you will remember that if a number and a numeric string, or two numeric strings are added, it will not perform the operation of addition. Instead, it will concatenate it as two strings. From *[figure 12.13](#c12.xhtml_fig12_13)*, we can observe that something similar is happening in this case. So, let’s quickly use **`console.log`** method to check the data type of the two numbers passed as arguments to the add method.

Let’s modify our function add from *[code example 12.9](#c12.xhtml_co12_9)*, to include console.log method to check for the data type of our arguments:

1.  `const add = (num1, num2) => {`
2.  `    console.log("Type of num1:   ", typeof num1);`
3.  `    console.log("Type of num2:   ", typeof num2);`
4.  `    return num1 + num2;`
5.  `}`

    **Code 12.10:** Adding console.log to method inside function add

When we save this and refresh our webpage, we will see the following:

![](images/Figure-12.14.jpg)

**Figure 12.14:** The output of the [code example 12.10](#c12.xhtml_co12_10)

As we can see in the preceding screenshot, the two arguments inside the function add are of data type string. It confirms our doubts that we are receiving two string values inside our add function. Now that we know what is giving the wrong answer, let’s rectify this erroneous code. The Number object has several methods to convert strings to numbers. To make the code generic, we will make use of the + operator before a string to convert the values of string to a number. Before we add this exploration to our code, let’s test it using **`console.log()`** method. In *[code example 12.10](#c12.xhtml_co12_10)*, we will make a couple of small changes:

1.  `const add = (num1, num2) => {`
2.  `    console.log("Type of num1 after adding + before it:   ", typeof +num1);`
3.  `    console.log("Type of num2 after adding + before it:   ", typeof +num2);`
4.  `    return num1 + num2;`
5.  `}`

    **Code 12.11:** Modifying console.log method inside function add

When we update and refresh our page, we will see the following:

![](images/Figure-12.15.jpg)

**Figure 12.15:** Changing string to number

In *[figure 12.15](#c12.xhtml_fig12_15)*, we can see that we can successfully convert our strings to a number data type using the + operator. Let’s remove this **`console.log()`** method and replace line number 2 of *[code example 12.9](#c12.xhtml_co12_9)* to the following:

1.  `const add = (num1, num2) => {`
2.  `    return +num1 + +num2;`
3.  `}`

    **Code 12.12:** Modifying the add function of conde example 12.9

When we save this and finally refresh our page, we will see the following:

![](images/Figure-12.16.jpg)

**Figure 12.16:** The output after [code example 12.12](#c12.xhtml_co12_12) is added

Finally, with the help of **`console.log()`** method, we have rectified all the bugs in our code.

# [Debugging with breakpoints](#toc.xhtml_s274a)

In the previous section, we have used the **`console.log()`** method systematically to detect and resolve the bug. Another way of debugging the JavaScript code is to make use of breakpoints. In *[Chapter 2: The Developer’s Tools](#c02.xhtml)*, we had a brief look at adding breakpoints to the code. We will look at breakpoints in more detail in this section, and solve one of the bugs in *[code example 12.2](#c12.xhtml_co12_2)* using breakpoints.

A majority of the modern browsers support adding breakpoints. However, in this book, we will primarily work with Google Chrome. To add a breakpoint to the JavaScript code, you should follow these steps:

1.  Open the **`Sources`** Panel of the Chrome Developer Tools.
2.  Find and open the **`index.js`** file from the sidebar on the left. This sidebar is known as the File Navigator pane.
3.  Choose a line of code on the section to the right of the File Navigator pane. This right section is known as the Code Editor pane.
4.  Add a breakpoint to the chosen line of code by clicking on its line number in the Code Editor pane. Now, whenever the browser is executing **`index.js`** file, it will pause at the breakpoint added in the point 4 mentioned earlier. When a breakpoint is added to the code, the execution of JavaScript is paused at that point in the **`index.js`** file.
5.  Using the controls present in the third and the final section at the bottom of the Sources Panel, you can move to the next line or continue execution of the code. This pane is called the JavaScript Debugging pane.

Let’s use the breakpoints to solve one of our bugs. Breakpoints are especially useful if you want to check errors other than SyntaxError. For instance, if you place a breakpoint on line number 6 of *[code example 12.2](#c12.xhtml_co12_2)*, the JavaScript execution will not pause at line number 6\. Instead, it will not even begin execution of the file index.js once the error is found while parsing the file. (Try adding a breakpoint on line number 6 and refresh the page.) However, if there was an error like a **`TypeError`** or a **`ReferenceError`**, it will be caught. It is because syntax errors are very crucial for the entire JavaScript.

However, if we resolve the first bug and then, in case of the second bug where we are getting a wrong result of the computation, you can pause the execution to check the values inside the function.

**Note:** A good debugging involves using all the three methods together to find out the root problem.

So, let’s presume that we have resolved the problem on line number 6 of *[code example 12.2](#c12.xhtml_co12_2)* using **`console.log`**. Now, the code that we need to debug for the wrong result provided by the function add is the code shared in *[code example 12.9](#c12.xhtml_co12_9)*. So, let’s remove the changes we updated in **`index.js`** after *[code example 12.9](#c12.xhtml_co12_9)*. Finally, in the index.js on the Sources Panel, let’s add a breakpoint on line number 2. When you complete this, your code will pause its execution on line number 2 and your Sources Panel will look like the following:

![](images/Figure-12.17.jpg)

**Figure 12.17:** Sources Panel after adding a breakpoint.

As shown in the preceding screenshot, there are several approaches to find out the values received in the function add:

*   You can check line number 1 of the Code Editor pane where the values of the arguments are shown with a brown background.
*   You can check the values on the right section of the JavaScript Debugging pane at the bottom of the **`Sources`** panel.
*   You can hover over the variables num1 and num2 either on line number 1 or line number 2 on the Code Editor pane. (Refer line number 1 of Code Editor pane of *[figure 12.17](#c12.xhtml_fig12_17).*)
*   With the breakpoint pausing code execution, you can head to the Console panel of the Developer Tools and type the variables **`num1`** and **`num2`** to find out their values or perform any operations on them without it affecting the actual code.

No matter which approach you use, you can notice that the value received in the arguments is wrapped in double quotes, which points out that it’s a string. To confirm this, with the breakpoint still pausing the execution, you can head to the Console panel of the Developer Tools, and type the following:

![](images/Figure-12.18.jpg)

**Figure 12.18:** Checking value and type on the Console panel

As you can see from the Console panel, the **`num1`** and the **`num2`** variables receive a string value. As we have previously resolved in *[code example 12.12](#c12.xhtml_co12_12)*, we can then use the + operator before the string value to convert them to a number format. It will then execute our code without any bugs. To continue the execution of our code, i.e., to stop the breakpoint from pausing our code execution, you can press the play button highlighted in blue in the JavaScript Debugging pane. As seen in *[Chapter 2: The Developer’s Tool](#c02.xhtml)*, if you want to move to the next line of the code, you will press on the button next to the play button in the JavaScript Debugging pane.

# [The debugger keyword](#toc.xhtml_s275a)

An alternative to adding the breakpoints manually in the previous section is to add the JavaScript keyword **`debugger`**; before the line which we want to examine. It will pause the execution of your JavaScript code at that point.

As it goes with adding breakpoints, you cannot use a debugger for **`SyntaxError`**. For errors like **`TypeError`** or **`ReferenceError`** or for the computational second case, we can add a debugger; keyword before line number 2 inside the function add. When you do this, your code will look like the following:

1.  `const add = (num1, num2) => {`
2.  `    debugger;`
3.  `    return num1 + num2;`
4.  `}`
5.  `let number1 = "20";`
6.  `let number2 = (Math.random()*100).toFixed(2);`

8.  `let sum = add(number1, number2);`
9.  ``document.getElementById("result").innerText = `The result of ${number1} and ${number2} is ${sum}.`;``

    **Code 12.13:** Adding the debugger inside the function

When you save this and refresh the page, you will see that the JavaScript execution of our **`index.js`** will be paused on the line where we have added debugger to our code, as shown in the following screenshot:

![](images/Figure-12.19.jpg)

**Figure 12.19:** Checking value and type on the Console panel using debugger

As with the debugging seen in the previous section, the JavaScript Debugging pane will show the values of the two variables **`num1`** and **`num2`** that the function add receives as parameters. You can also check their values or perform operations on these variables using the four approaches from the previous section.

Finally, now that we know the values of the variables **`num1`** and **`num2`**, we can apply the changes seen in *[code example 12.12](#c12.xhtml_co12_12)* to solve our bug.

# [Try, catch, and finally](#toc.xhtml_s276a)

In the previous sections, we have looked at several ways to debug an issue in our code. As we have seen in the **`console.log`** section, if the JavaScript execution is not stopped, a blank page will be shown to the user since our code crashed. Often, this is not desirable. For instance, think of an e-commerce application. If the code crashes, the users will see a blank page or some ugly error message on their screen. It would act as a repellent for the users. To handle such unexpected errors, we use the JavaScript exception handling.

There are four keywords used in JavaScript exception handling, which are as follows:

*   **try**: When you want to test a block of code for errors, you will add that code inside a try statement code block.
*   **catch**: If any errors occur in the code inside the try block of code, these errors will be caught and sent to the catch block of code. Here, you can handle these errors safely.
*   **throw**: It is used for throwing custom errors.
*   **finally**: JavaScript will execute the code inside the finally statement after try and catch, regardless of the result.

It essentially means you will want all the code inside the try statement to execute successfully, without any errors. However, if it does not, and results in any errors, the control will automatically shift to the catch block. Inside the catch block, we can write a block of code to handle this exception safely. If no exceptions or errors are found inside the try statement, the block of code inside the catch block will be skipped. The code inside the finally statement will be executed immediately after try and catch blocks are completed.

To bypass the syntax error, let’s try to introduce a TypeError in the updated example of our code that we have used in *[code example 12.2](#c12.xhtml_co12_2)* and *12.9*:

1.  `const add = (num1, num2) => {`
2.  `    return +num1 + +num2;`
3.  `}`

5.  `try {`
6.  `    let number1 = "20";`
7.  `    let number2 = (Math.random()*100).tosFixed(500);`

9.  `    let sum = add(number1, number2);`
10.  ``    document.getElementById("result").innerHTML = `The result of ${number1} and ${number2} is ${sum}.`;``
11.  `}`
12.  `catch(error) {`
13.  ``    document.getElementById("result").innerHTML = `Sorry, it looks like we encountered an error.`;``
14.  `}`

    **Code 12.14:** Introducing a TypeError

In *[code example 12.14](#c12.xhtml_co12_14)*, the first thing that we have done is introduce a TypeError in our code. On line number 7, we have added an incorrect spelling of the JavaScript method **`toFixed`** to **`tosFixed`**. Next, we have added the entire code in the try block. If the code will encounter an error (and it should), it will be picked up by the catch block. Inside the catch block, we make sure we tell the user that we have encountered an error.

If you comment out the **`try`** and **`catch`** blocks, you will see that on refreshing the page, you will only see a blank screen. However, if you keep the *[code example 12.14](#c12.xhtml_co12_14)* intact, you will see our webpage like the following:

![](images/Figure-12.20.jpg)

**Figure 12.20:** Page after error handling

Therefore, we have handled a potential error and not let it impact the UI of our web page.

# [Conclusion](#toc.xhtml_s277a)

We started this chapter by learning about the various types of errors and why they occur. After that, we learned about the different methods of debugging, that is, detecting errors in our code. The first method is using **`console.log()`** method. It simply logs a statement inside the Console Panel of the browser, if supported. The second and third methods – adding a breakpoint and using debugger – pause the execution of the code. Finally, we had a look at handling errors using try, catch, and finally, to not let it affect the UI.

In the next chapter, we will have a detailed look at testing and testing frameworks.

# [Points to remember](#toc.xhtml_s278a)

*   Debugging in JavaScript is the process of identifying and rectifying errors in JavaScript code.
*   The **`console.log()`** method logs a statement inside the browser’s Console panel. It will not pause the execution of the code.
*   You can pause the execution of the code to check the values passed at the point of error. To pause code execution, you can manually add the breakpoint in the Sources panel of the Developer’s Tools, or you can add the keyword debugger before the error code.
*   If errors are not handled, they can affect the UI of the webpage. To handle errors, we use the try, catch, and finally block. The code to be tested will be placed inside the try block. If it catches an error, it will be moved to the catch block. The code inside finally block will be executed regardless of the result after try and catch.

# [Multiple choice questions](#toc.xhtml_s279a)

1.  **The code inside the finally block will not be executed if errors are not found – True or False?**
    1.  True
    2.  False
2.  **Which of the following Error will be thrown if we reference a variable that has not been declared?**
    1.  TypeError
    2.  ReferenceError
    3.  SyntaxError

# [Answers](#toc.xhtml_s280a)

1.  **b**
2.  **b**

# [CHAPTER 13](#toc.xhtml_c13)

# [Testing and Test Frameworks](#toc.xhtml_c13)

Let's start this chapter with a practical example.

In 2014, a popular Indian e-commerce website came up with a quirky marketing strategy to lure customers to their website. The e-commerce website advertised that on one of the festive days in 2014, more than half of the products on the website will be available for as less as Re. 1\. Needless to say, this lucrative marketing deal created the perfect buzz for this e-commerce website. However, on the day of the deal, the website crashed for a majority of the users. For a select few, the deals that they selected ended up as out-of-stock by the time users checked out for payment. The website's popularity with the masses took a severe hit with this experiment. In fact, several loyal customers moved on to other e-commerce platforms.

The lesson that we get to learn from this example is that if the developers at the e-commerce website had tested the website thoroughly, the entire fiasco could have been avoided. It is one of the examples why testing is so crucial for every brand and every website. In this chapter, we will first understand the process of testing. Next, we will look at the several types of testing. We will end this chapter by exploring the several testing frameworks, before trying out one of the frameworks for unit testing.

# [Structure](#toc.xhtml_s281a)

In this chapter, we will cover the following topics:

*   Introduction to testing
*   Types of testing
*   Ideal testing structure
*   Testing frameworks
*   Jest

# [Objective](#toc.xhtml_s282a)

After studying this chapter, you should be able to understand the importance of testing your web site/application. You will learn to implement several types of testing at different stages of your development and use Jest framework for unit testing.

# [Introduction to testing](#toc.xhtml_s283a)

As we learned earlier, testing plays a crucial part in your web application/website. In *[Chapter 12: Debugging and Error Handling](#c12.xhtml)*, we had learned about a concept called *bugs*. Whenever a program gives unexpected or incorrect results, we label it as a bug. As we saw in the previous chapter, if bugs are left unattended, they can crash the entire website/web application. In the previous chapter, we explored several ways to detect bugs and handle the issues caused by these bugs. In this chapter, we will understand ways to test our codes to avoid bugs.

While working on projects at a technical company, you will often come across terms like TDD and BDD. The terms, TDD and BDD are paradigms or models of the agile methodology of development. While there are several more paradigms, these are the ones which are extremely popular amongst development teams. Testing your web development work is moderately dependent on the paradigm you choose. The full form of TDD is Test-Driven Development, while BDD stands for Behavior-Driven Development.

The difference between TDD and BDD is the way you approach a feature.

# [Test-Driven Development](#toc.xhtml_s284a)

In TDD, we first write a test for developing a feature. For instance, to create a login page, we mandatorily require two input boxes – one for username/email and another for the password. In TDD, we do not start writing code for creating the two input boxes. First, we write a test case that states that the login page will require two input boxes. Since we have not typed a code that will render two input boxes, the test is bound to fail. Only after we write the correct code for rendering the two inputs, the test will pass. In this manner, we will create "*blueprints*" for every smallest part of the feature to pass. It will ensure that there is a blueprint for every piece of code that you write.

![](images/Figure-13.1.jpg)

**Figure 13.1:** Flow of TDD

Since we write tests before development, that is, tests are driving the development, this process is known as TDD. It answers the question "*Does my code work?*".

# [Behavior-Driven Development](#toc.xhtml_s285a)

Unlike TDD, the **Behavior-Driven Development** (**BDD**) concentrates on the behavior of your system. In BDD, the question that is answered is "*Does my code do what it’s supposed to do?*".

Taking a leaf out of the example that we have used in the previous section, in BDD, we will not be looking at whether the page has two input boxes. Instead, we will be concentrating on whether the page achieves the job of logging a user in (the behavior). In BDD, a combination of the native language (to describe the behavior or the function) and a knowledge of the domain is necessary.

In conclusion, there is no comparison between TDD and BDD. TDD is extremely useful for small teams, and it reduces the likelihood of having bugs. At the same time, BDD is extremely useful for large teams where we need to track the behavior of the user actions, but it comes with a downside that bugs become slightly difficult to track. Depending on your development and the goal of your work, it’s important to pick up one of the testing styles. However, the most important part of this chapter is to ingrain the principle that tests are very important for development. In the next section, we will take a look at several types of testing.

# [Types of testing](#toc.xhtml_s286a)

There are several types or styles of testing. However, in this section, we will cover the most important types of testing.

# [Unit tests](#toc.xhtml_s287a)

Unit testing involves testing small pieces of code independently. It is significantly useful for reducing the occurrence of bugs during deployment. Since we write a test for the smallest pieces of a feature, the chances of bugs happening at the higher levels is significantly reduced. Unit tests break down the software into specific functions and perform individual tests on these functions. The main aim or purpose of a unit test is to identify and eradicate a bug before it’s pushed to production, that is, before the users can use your application.

# [Integration tests](#toc.xhtml_s288a)

In unit tests, we write code that will test an individual function or a piece of code. While this can ensure that the individual function will rarely throw an error, it does not cover the interaction of this individual component with another such individual component. It’s possible that both the individual components will work perfectly as expected on their own. However, when these components interact with each other, it might result in an error that might crash the application. For instance, on an e-commerce application, the unit test for a mobile page involves ensuring that there is an exact number of mobile phones as seen in the database. Similarly, the unit test for a cart page will accurately show the information of the items added in the cart with the several input boxes for the user to enter their personal and payment details. However, if the '**`Add to Cart`**' button on the mobile page for every mobile does not update the items on the cart page, the interaction between the two fails. It might crash the application.

Integration testing is the one where individual components are combined as a group and then tested. Typically, it involves testing several modules where every module consists of two or more small components of the application. Integration tests are used for testing interactions between these components. It helps in finding major bugs when several components are run together in the application.

# [End-to-end tests](#toc.xhtml_s289a)

The end-to-end testing is the final piece of the testing jigsaw. The end-to-end testing is also known as E2E testing or function testing. It is used for testing the entire flow of the application from the start to the end. In E2E testing, the smaller technicalities of the functions are ignored. Here, we test how scenarios work on the product itself, by controlling the browser or the website. In this style, we look at the website or the web application from the eyes of the user. We replicate and try to emulate the environment and the behavior of the user while testing the application from the start to the end. The shortcoming of this style is that it’s difficult to find the root cause of the failure. Hence, it’s not particularly useful for large projects.

# [Ideal testing structure](#toc.xhtml_s290a)

We already know that testing is crucial for every web development project. However, it does not make sense to write test for every line of code or every small functionality that you write. Similarly, it is wrong to use only one style of testing for your entire application.

The point is to *write just enough tests – write the right tests*. It’s never about reaching 100% test coverage.

A typical testing structure should have the following layers:

![](images/Figure-13.2.jpg)

**Figure 13.2:** An ideal testing structure

The preceding screenshot shows the following:

**Static Tests**: The most basic thing that you need to do is include a static type system or a linter to check for basic errors like typos or syntax error. IDEs like Visual Studio Code provide an in-built system of capturing such typos or syntax errors while the user is typing the code.

**Unit Tests**: You need to write effective unit tests that will target critical behavior of the application. Instead of writing unit tests for every single function of your application, you should include tests only for those functionalities which are extremely crucial to your application.

**Integration Tests**: It is extremely important to include integration tests in your application, especially for all those components which have a serious implication or consequence from a user perspective. We have looked at one example in the preceding sub-section of integration testing.

**End-to-end Tests**: Finally, you need to ensure that your application works as expected from the start to the end.

Adding these four layers will ensure your web application runs smoothly, and without any major bugs that might affect the user experience of your web application.

# [Testing Frameworks](#toc.xhtml_s291a)

There are several great testing frameworks and testing tools. In this section, we will look at a list of tools that are the most popular in the web development industry, best maintained, and the ones that you should definitely be aware of.

# [jsdom](#toc.xhtml_s292a)

jsdom is a pure JavaScript implementation of many web standards. In simple terms, jsdom simulates a browser’s environment with the help of simple JavaScript. In simulated browser environment, tests will run really fast. However, not everything can be simulated. For instance, taking a screenshot is not a behavior of a browser. Hence, it cannot be emulated. There are several such implementations that cannot be implemented.

You can read more about jsdom here: **[https://github.com/jsdom/jsdom](https://github.com/jsdom/jsdom)**

# [Karma](#toc.xhtml_s293a)

Karma hosts a test server. This test server will have a special web page to run your tests in the page’s environment. This page can be tested across many browsers and simulated-browser environments like **`jsdom`**.

You can check Karma here: **[https://karma-runner.github.io/2.0/index.html](https://karma-runner.github.io/2.0/index.html)**

# [Chai](#toc.xhtml_s294a)

Chai is one of the most popular assertion libraries for testing. An assertion library is the one where you write an expectation for a particular variable or a value and test this expectation against the received value. It has several plugins and extensions.

You can check Chai here: **[https://github.com/chaijs/chai](https://github.com/chaijs/chai)**

# [Cucumber](#toc.xhtml_s295a)

Cucumber specializes in BDD style of development. It divides the test between the acceptance criteria files using the Gherkin syntax (a business readable, domain specific language) and tests that correspond to them. Tests can be written in a variety of languages, including JavaScript.

You can read more about Cucumber here: **[https://github.com/cucumber/cucumber-js](https://github.com/cucumber/cucumber-js)**

# [Jest](#toc.xhtml_s296a)

Jest is a very popular testing framework created and maintained by *Facebook*. It is one of the most popular library frameworks used by developers. It is considered to be faster for big projects. It is clear, consistent, and comes with a lot of features like assertions, mocks, and spies. It also gives you code coverage, and it updates only the files which are updated, so tests are running faster in comparison. React framework also suggests using *Jest* framework.

You can check Jest here: **[https://jestjs.io/](https://jestjs.io/)**

# [Jasmine](#toc.xhtml_s297a)

Jasmine is the testing framework that Jest is based on. Jasmine framework is a legacy framework, and it has been around for longer. It is a ready-to-go framework that helps you kickstart testing. In fact, Angular framework suggests using Jasmine framework.

You can check Jasmine here: **[https://github.com/jasmine/jasmine](https://github.com/jasmine/jasmine)**

# [Mocha](#toc.xhtml_s298a)

Again, mocha is one of the most used libraries. Unlike *Jasmine*, it is used with third party assertions, mocking and spying tables. *Mocha* is a little harder to set up. However, it is more flexible and open to extensions.

Mocha can be checked out here: **[https://github.com/mochajs/mocha](https://github.com/mochajs/mocha)**

# [Selenium](#toc.xhtml_s299a)

Selenium dominated the market of functional testing for years. It can be used for testing your application on several browsers. It was not written specifically for testing, and it can control a browser for many purposes by exposing a driver that controls browsers using browser extensions.

You can check out Selenium here: **[https://github.com/SeleniumHQ/selenium](https://github.com/SeleniumHQ/selenium)**

# [Jest](#toc.xhtml_s300a)

As we have learned earlier, *Jest* is a popular testing framework created and maintained by popular social media powerhouse, Facebook Incorporation. Apart from the several prominent features, Jest concentrates on simplicity. It works with frameworks like *Angular* and *React*. In fact, the official documentation of ReactJS recommends using Jest for testing applications created using React framework.

In this chapter, we will be acquainting ourselves with the knowledge of the Jest framework. We will create a simple JavaScript example to understand how to use the Jest framework for testing.

To use Jest for your web applications, you need to install one of the two dependencies on your local machine – **`npm`** or **`yarn`**. Before we understand **`npm`** or **`yarn`**, we need to understand Node. Node.js is an open-source JavaScript runtime environment that runs JavaScript code outside a browser.

Now, npm is a package manager for the JavaScript programming language. The npm registry contains several packages (for example, *Jest*), which, in turn, are either Node modules or contain node modules. Basically, node modules are files that can be loaded by the Node platform using **`require()`** method.

**`yarn`** is also a package manager that is developed by *Facebook*. It performs similar functionalities as npm.

Therefore, to use the Jest framework for testing our application, we simply need to use npm to install the Jest framework in our application. So, let’s start with the following:

# [Install package managers](#toc.xhtml_s301a)

To use npm or yarn, first you need to install them on your machine.

To install npm, check out: **[https://www.npmjs.com/get-npm](https://www.npmjs.com/get-npm)**

To install yarn, check out: **[https://www.npmjs.com/package/yarn](https://www.npmjs.com/package/yarn)**

# [Initialize a new project](#toc.xhtml_s302a)

Next, we need to initialize a project with npm. To do that, first we should fix the location where we want to create our project. In our case, I have created a folder called Testing on the Desktop. Here, I will initialize our project.

To initialize a project, we need to use the following command:

`npm init`

**Code 13.1:** Initializing a project

When you type the preceding command, you will receive several prompts on your terminal to fill in details about your project. It’s completely fine if you leave the details empty right now by clicking the *Enter* key after every prompt. When you complete filling out all the details, your terminal will look like the following:

![](images/Figure-13.3.jpg)

**Figure 13.3:** Terminal when initializing a project

When you complete the preceding process, you will notice that a new file has been created in the folder called **`package.json`**. It will have the details added by you in the terminal:

`{`

`"name": "testing",`

`"version": "1.0.0",`

`"description": "",`

`"main": "index.js",`

`"scripts": {`

`"test": "echo \"Error: no test specified\" && exit 1"`

`},`

`"author": "",`

`"license": "ISC"`

`}`

**Code 13.2:** The package.json file

# [Install Jest using npm or yarn](#toc.xhtml_s303a)

Now, we need to install Jest in our project. Back in the terminal, we need to go to our project folder, and add the following code:

`npm install --save-dev jest`

**Code 13.3:** Installing jest using npm

For yarn, we will need to use the following command:

`yarn add --dev jest`

**Code 13.4:** Installing jest using yarn

In *[code example 13.3](#c13.xhtml_co13_3)*, we have used save-dev. It will install jest as a development dependency. It means jest will be used only during development, and not during production, that is, when a user is using the application. Instead, if we used –save, it will save this as a dependency. It means jest will be used for both development and during production. Since we need to test our application only during the development and, of course, not when the user is actually using it, we save Jest as a development dependency.

# [Create a function for testing](#toc.xhtml_s304a)

Now, we need to create a function that we need to test using Jest. I will be creating a simple addition function. For that, we will create a new file called **`index.js`** in our folder. Inside **`index.js`**, we will write our addition function as follows:

1.  `const add = (num1, num2) => num1 + num2;`

3.  `module.exports = add;`

    **Code 13.5:** Add function in index.js

In *[code example 13.5](#c13.xhtml_co13_5)*, we have created a function add using the ES6 arrow functions. We have added one more line which exports our function add. It will ensure that the function add will be available to all the other files in our project.

# [Create the test file](#toc.xhtml_s305a)

Next, we create the test file. First, we need to create a file with the same name as the file where our function is stored. We need to add an extra extension for our file. We will name our test file as **`index.test.js`**. Inside **`index.test.js`**, we will write the following code:

1.  `const add = require('./index');`

3.  `test('Adding 2 and 3 should be equal to 5', () => {`
4.  `     expect(add(2, 3)).toBe(5);`
5.  `})`

    **Code 13.6:** Creating the test file for addition

In *[code example 13.6](#c13.xhtml_co13_6)*:we’ve done the following,

*   On the first line, we have imported our **`index.js`** file.
*   Next, we added the code or the condition for testing inside the test method of Jest. It accepts two arguments – a statement to identify the test and a callback function.
*   Inside the callback, we have used the expect method. If you observe closely, inside the expect method, we are calling our add function with the values 2 and 3 passed inside as arguments. As per its English definition, the method expect signifies that the value received by the invocation of this function will be tested against something.
*   Outside the expect method, we used a Jest "*matcher*" to validate our test. In other terms, the matchers are the expectation or the expected answer to the function called inside the expect method. In our case, we are using the matcher toBe. The toBe matcher is used for comparison of primitive values. Here, we expect the result to be 5, hence, we have added 5 inside the parentheses of the toBe matcher.

As a whole, we are telling Jest that the value returned by the function execution of the add function is expected to be 5.

# [Add/Modify package.json](#toc.xhtml_s306a)

In this step, we will add or modify our **`package.json`** file to include a command for testing. We will replace the quote "**`echo \"Error: no test specified\`**" **`&& exit 1`**" with a single word "**`jest`**". Calling this command will run our tests. Our updated **`package.json`** file will look like the following:

1.  `{`
2.  `   "name": "testing",`
3.  `   "version": "1.0.0",`
4.  `   "description": "",`
5.  `   "main": "index.js",`
6.  `   "scripts": {`
7.  `     "test": "jest"`
8.  `  },`
9.  `   "author": "",`
10.  `   "license": "ISC",`
11.  `"devDependencies": {`
12.  `     "jest": "^26.6.3"`
13.  `  }`
14.  `}`

    **Code 13.7:** Modifying the package.json file for testing

You will notice that since we had used save-dev earlier in our command, the jest package has been saved in **`devDependencies`**. It means it is stored as a dependency only during development.

# [Running the test](#toc.xhtml_s307a)

Finally, we will run the test. To do that, we will go to the terminal and to the folder where our project is stored. Here, we will type npm run test. The test seen in the command here refers to the word test in the scripts object of our **`package.json`**. Inside the test keyword of our **`package.json`**, we have the command jest. Therefore, on typing the command, npm will run the command stored inside test, which is jest. When we do that, we will see the following in the terminal:

![](images/Figure-13.4.jpg)

**Figure 13.4:** Terminal when running a test

As you can see in the preceding screenshot, our test ran successfully, and we received the output as 5\. To check if the test function indeed works correctly, let’s try to fail this test.

In our **`index.test.js`**, we will add one more condition:

1.  `test('Adding 1 and 4 should not be equal to 6', () => {`
2.  `    expect(add(1, 4)).toBe(6);`
3.  `})`

    **Code 13.8:** Adding a condition to fail

When we save the preceding code, and run our tests, we will see the following:

![](images/Figure-13.5.jpg)

**Figure 13.5:** Terminal showing one passed and one failed test

As shown in the preceding screenshot, the first test passes while the second test fails.

In this way, we can use several different matchers to test different parts of our code. For the entire list of matchers, refer to the following link: **[https://jestjs.io/docs/en/expect](https://jestjs.io/docs/en/expect)**.

# [Conclusion](#toc.xhtml_s308a)

In this chapter, we learned about several techniques to avoid bugs in our code. We can achieve so by using the JavaScript testing modules. We started out the chapter by understanding the difference between a test-driven development (TDD) and a behavior-driven development (BDD). We followed that up with understanding the important types of testing and an ideal structure to test JavaScript applications. Next, we explored several testing frameworks before implementing one of the most popular JavaScript testing frameworks, Jest.

In conclusion, we have learned the importance of testing and how to implement testing for our JavaScript applications. In the next chapter, we will look at *Regular Expressions* in JavaScript. It provides a nice framework to search for words in JavaScript.

# [Points to remember](#toc.xhtml_s309a)

*   An application without testing can end up exposing bugs to the user. Depending on the severity of the bug, the application might crash, and it would make the users move away and stop using your application.
*   Test-driven development insists on writing tests before you write the actual code. It will ensure you adhere to strict rules and in turn, it will result in very few bugs in the system.
*   Behavior-driven development insists on writing code that tests the behavior or the functionality of the code. It doesn’t stress on strict rules.
*   An ideal testing structure does not signify 100% test coverage. It instead concentrates on having effective unit tests (that tests the individual’s smallest components) on crucial parts of the application. Along with the unit tests, there should be several integration tests at crucial parts of the application followed by an end-to-end testing of the platform.
*   There are several frameworks of testing for different use-cases. However, Jest is popularly used for its simplicity.

# [Multiple choice questions](#toc.xhtml_s310a)

1.  **If we use –save instead of –save-dev, it will store the dependency only for runtime – True or False?**
    1.  True
    2.  False
2.  **_____ testing involves checking whether individual components can work together.**
    1.  Unit
    2.  Integration
    3.  End-to-end

# [Answers](#toc.xhtml_s311a)

1.  **b**
2.  **b**

# [CHAPTER 14](#toc.xhtml_c14)

# [Regular Expressions](#toc.xhtml_c14)

In the previous chapters, we have learned a great deal about JavaScript and its implementations. Finally, we have reached the conclusion of our book. Starting with this chapter, and in the next two chapters, we will learn a few auxiliary concepts that will help you write better JavaScript. In this chapter, we will learn the concept of regular expressions. Regular expressions are heavily used for matching character combinations in strings.

Let’s understand it with the following practical example:

Every email should mandatorily have a "@" symbol and a "." in it. Let’s imagine that we have an application where we ask the user to provide us with their valid email ID for communication or for sending the link to reset their password. If you choose not to use input type=email, it is very crucial to make sure that the email consists of the preceding two symbols at their appropriate positions. Additionally, if we intend to ask the user to supply their Gmail IDs, we also need to confirm that the text between "*@*" and "." is "*gmail*". For such scenarios and many other such similar scenarios, we need advanced methods to check the string. This is one of the places where regular expressions are extremely useful.

# [Structure](#toc.xhtml_s312a)

In this chapter, we will cover the following topics:

*   Introduction to Regular Expressions
*   Writing Regular Expression patterns
*   Advanced searching with flags
*   JavaScript methods for Regular Expressions
*   Practical example of Regular Expressions

# [Objective](#toc.xhtml_s313a)

After studying this chapter, you should be able to understand the concept of Regular Expressions and learn how to use regular expressions for pattern matching in JavaScript.

# [Introduction to Regular Expressions](#toc.xhtml_s314a)

In simple words, a regular expression is a sequence of characters that define a search pattern. When we need to search a sequence of characters inside a string, we can use patterns created using Regular Expressions.

Several programming languages use Regular Expressions in different formats for searching characters using patterns. In JavaScript, we can use Regular Expressions in its literal format or by calling the RegExp JavaScript object.

# [Creating a Regular Expression](#toc.xhtml_s315a)

As mentioned earlier, you can construct a regular expression in one of the two following ways:

# [Regular Expression Literal](#toc.xhtml_s316a)

To write regular expression literal, we need to write patterns for searching, inside slashes:

`let pattern = /abc/;`

**Code 14.1:** A Regular Expression Literal

In *[code example 14.1](#c14.xhtml_co14_1)*, we have used a regular expression literal with slashes. We will look at regular expression literals in more detail, later in this chapter. For the time being, the *[code example 14.1](#c14.xhtml_co14_1)* signifies that we will search for a pattern "*abc*" in the exact order inside any string.

# [JavaScript RegExp Object](#toc.xhtml_s317a)

Alternatively, you can use the JavaScript object RegExp to create search patterns. The code shown in *[code example 14.1](#c14.xhtml_co14_1)* can be rewritten with the RegExp object as follows:

`let pattern = new RegExp('abc');`

**Code 14.2:** A Regular Expression JavaScript object

Both *[code examples 14.1](#c14.xhtml_co14_1)* and *[14.2](#c14.xhtml_co14_2)* create a pattern and store it inside the variable pattern.

# [Writing Regular Expressions pattern](#toc.xhtml_s318a)

A regular expression pattern is made up of simple characters. There are three ways of writing patterns using regular expressions, based on the complexity of the search pattern. One important thing to notice is that regular expressions are case-sensitive, that is, "*A*" is not the same as "*a*". In a majority of cases, you will be mixing and matching the three patterns to search or replace texts inside a string.

# [Using simple patterns](#toc.xhtml_s319a)

When you want to find a direct match for a sequence of characters in your strings, you make use of a simple pattern. We have already seen an example of simple pattern in *[code example 14.1](#c14.xhtml_co14_1)*. A simple pattern is used when we need to search for an exact sequence of characters, that is, all characters together and in the same order. A good example for simple pattern is as follows:

![](images/Figure-14.1.jpg)

**Figure 14.1:** Examples of simple pattern search

In the preceding screenshot, we have used a regular expression literal to define a simple pattern for searching. Next, we have used the search method of JavaScript String object to search for this pattern in the string variables **`str1`** and **`str2`**. As you can see from the **`console.log`** statements, we successfully receive the value 12 denoting the starting position of the pattern apples in the variable **`str1`**. However, for the second string variable **`str2`**, it returns -1\. It means the pattern apples could not be found in **`str2`**. If you look at **`str2`** closely, you will see that **`str2`** also has a-p-p-l-e-s in the same order but the character s is separated from the first five characters with a space. In a simple pattern, spaces are not ignored. Hence, searching for the pattern in **`str2`** returns -1.

**Note:** Regular Expressions, on its own, have a large variety of patterns to search from. For sanity’s sake, starting from the next sub-topic, we will only be looking at the most popular patterns that are commonly used. For the entire list of patterns, you can check the official MDN docs.

# [Using groups and ranges](#toc.xhtml_s320a)

Often you might need to search for or replace characters from a certain group or within a certain range. For instance, you might want to search for a pattern where the text might contain the word green or the word red. Another instance will be when you want to search for a string where the characters can be either a, b, c, or *. Such cases can be handled using groups in regular expressions. Let’s look at the different types of grouping regular expression patterns.

# [x|y](#toc.xhtml_s321a)

Here, x and y represent any string while the pipe symbol (|) represents an "or". It means if we want to search for a pattern where the text is either x or y, we can use this operator in regular expressions. As you can see in the following screenshot, the search method will return a value other than -1 only for the string containing the word blue or gold:

![](images/Figure-14.2.jpg)

**Figure 14.2:** Am example of |

**Note:** In the next two sections, you can use either of the formats separated by "or". The "or" is merely a separator and not a part of the syntax. The two formats separated by "or" are individual syntax on their own.

# [[xyz] or [x-z]](#toc.xhtml_s322a)

When you want to create a search pattern to search any one character from a chosen few characters (including special characters) or search any one character from a range of characters, you use the preceding two patterns. As shown in *[figure 14.3](#c14.xhtml_fig14_3)*, we have used the first pattern to request JavaScript to search and return the position of any one of the characters from a, -, b, f, z. If you look at the second **`console.log`** statement, you will notice that the word Candidate-3 includes both a and hyphen (-). However, as we encounter the a before the hyphen, the position of a is returned. Similarly, in the second and third examples, you can see that if we want to create a pattern where the string should have any one of the numbers between 0 and 5, you can either use [012345] or [0-5].

![](images/Figure-14.3.jpg)

**Figure 14.3:** An example of grouping

# [[^xyz] or [^x-z]](#toc.xhtml_s323a)

It is similar to the pattern we have seen earlier with one notable difference. In this case, it will match everything that is not included in square brackets.

# [Using special characters](#toc.xhtml_s324a)

When the search for a match requires more than an exact or a direct match, we make use of special characters. For instance, if you want to find one or more a’s or if you want to match a pattern where the character H is followed by one or more i’s, we use special characters. There are several categories of special characters based on where and how we can use them. Let’s go through them one by one.

# [Assertions](#toc.xhtml_s325a)

Assertions include boundaries, that is, indicating the start and end of lines and words. It also includes conditional expressions.

# [^](#toc.xhtml_s326a)

It indicates the beginning of an input. It means the very first character of the string. As we have seen in the previous section, it has a different notation when used with a group.

![](images/Figure-14.4.jpg)

**Figure 14.4:** An example of ^

# [$](#toc.xhtml_s327a)

It indicates the end of the input. It means the last character of the string. As shown in the following screenshot, the first **`console.log`** returns a value other than -1 because it ends with y.

![](images/Figure-14.5.jpg)

**Figure 14.5:** An example of $

# [\b](#toc.xhtml_s328a)

It is used for denoting a word boundary. It signifies a position where a word character is not followed or preceded by another word character, such as between a letter and a space. For instance, /\ba/ will match the "a" in "apple". It will also match /le\b/ in "apple" as there are no word character after "le" in "apple". However, /le\b/ will not match the "le" in "left", because "le" is followed by f.

# [x(?=y)](#toc.xhtml_s329a)

# [(?<=y)x](#toc.xhtml_s330a)

The preceding combinations are known as *lookahead* and *lookbehind* assertions respectively. As seen earlier, you can replace the x and y with any string. If you observe it closely, you will see that in the first case, that is, *x(?=y)*, it will only return a positive search if it finds y after x, or in other words, y is following x. Similarly, in the second case, *(?<=y)x*, it will only return a positive search if y is preceding or before x. You can see this in the following example:

![](images/Figure-14.6.jpg)

**Figure 14.6:** An example of lookbehind and lookahead assertions

# [Character Classes](#toc.xhtml_s331a)

It is one of the most used and significant type of regular expressions. It helps you identify between letters, numbers, and special characters. We will look at a combined example of all character classes at the end of the chapter.

*   **`\d`**: It matches any digits in the string. It is equivalent to [0-9] as a group that we saw earlier.
*   **`\D`**: It matches anything except digits in the string. It is equivalent to [^0-9] as a group.
*   **`\w`**: It matches any alphanumeric characters from basic Latin alphabet, including the underscore in the string. It is equivalent to [A-Za-z0-9_].
*   **`\W`**: It matches everything except alphanumeric characters from basic alphabet in the string. It is equivalent to [^A-Za-z0-9_].
*   **`\s`**: It matches a single white space character including space, tab, form feed, or line feed.
*   **`\t`**: It matches a horizontal tab.
*   **`\`**: It is used for escape characters. For instance, if you want to create a pattern to match a backslash, we cannot simply use **`\`**. To search for backslash, we will need to use **`\\`** for JavaScript to understand it’s a backslash. The same applies for other characters, such as * that we will see in the next section.

Combining the principles we have learned so far, we have included them in the following screenshot:

![](images/Figure-14.7.jpg)

**Figure 14.7:** An example of character classes

In the preceding screenshot, we have used a different JavaScript method called **`match`**. It performs the same job as search, that is, searching a string against a pattern. However, it does not return the position of the string, but an array object instead. Unlike search, if it does not find a match, it returns null.

In *[figure 14.7](#c14.xhtml_fig14_7)*, as you can see, for the first statement, we are searching for a digit in the statement and it is duly returned. Similarly, in the third statement, we are again looking for a digit, but since it could not find any, it returned null. In the second statement, we combined several principles.

*   Firstly, we use the ^ assertion to make sure that the character after ^ is the first character of the string input.
*   Next, we have used the square bracket grouping that we learned earlier. It denotes that either a or A should exist. Combining the preceding point with this, it means the string to match needs to start with a or A.
*   After that, we have used the **`\s`** character class to denote that a space should exist after the first word.
*   After that, we have used a **`\d`** sandwiched between two **`\b`**. As we have learned previously and in this section, **`\`** is used for escaping and **`\b`** refers to a word boundary. It means we should have a digit which has spaces at both ends.

Thus, we are able to match that pattern accordingly.

# [Quantifiers](#toc.xhtml_s332a)

It is used for indicating the number of characters or expressions for matching. We will look at the several types of following quantifiers. As usual, the x in the following examples can be replaced by any string. We will look at a combined example at the end of the chapter.

*   **x*** : It means it should match the term denoted by x, 0 or more times. For instance, /lo*/ matches "*looo*" in "*Helooo*". Similarly, /e*/ matches "*e*" in "*Hey*", but it will return nothing in "*Hola*".
*   **x+**: It means it should match the term denoted by x, 1 or more times. For instance, /a+/ matches "a" in "Ha!" and all the a’s in "*Haaaaaaaa!*", but it will return null for "*Byeee*".
*   **x?**: It means it should match the term denoted by x, 0 or 1 times. For instance, /e?l/ matches "*le*" in "*Angel*" and /le?/ matches "*l*" in "*Angel*".
*   **x{n}**: It means it should match the exact n occurrences of the preceding item x. For instance, it will return "*ll*" for /l{2}/ match of "*Hello*", but it will return null for /l{3}/ match.
*   **x{n,}**: It means it should match at least n occurrences of the preceding item x. For instance, it will return "*ll*" for /l{2,}/ match of "*Hello*", but it will return null for "*Halo*".
*   **x{n, m}**: It means it should match at least n and at most m occurrences of the preceding item x. For instance, it will return "*ll*" for /l{2, 4}/ match of "*Hello*", but it will return null for "*Helllllo*".

Let’s look at examples for the quantifiers. In *[figure 14.8](#c14.xhtml_fig14_8)*, for the first two statements, we get "*taaaaaaaa*", that is, all the a’s because the first match requires zero or more a’s and the second one requires one or more a’s. However, in the third match, we get only one a, as we request for 0 or 1 matches of a.

For the next three console.log statements, we have first set a boundary using \b. In the fourth console.log statement, inside the boundary, we have requested for any word with an exact occurrence of three characters. If you look at the variable statement, you will notice that the first word with three characters is "*the*", hence "*the*" is returned. In the fifth statement, we are looking for words with occurrence of three or more characters. We find that in the first word itself "*this*". Finally, in the sixth statement, we are looking for a word which has characters between 1 and 3\. Hence, we get the second word "*is*".

![](images/Figure-14.8.jpg)

**Figure 14.8:** An example of quantifiers

# [Advanced searching with flags](#toc.xhtml_s333a)

In this chapter so far, we have observed the following two things:

*   Searches are case-sensitive, that is, if I search for "*apple*" and the string that needs to be searched has "*Apple*", it will return null.
*   Searches return only the first match.

We can override this behavior with the help of flags. Flags are added right at the end of your regular expression, i.e., after the final slash (/). You can add multiple flags together.

There are six flags that are provided by Regular Expressions. However, we will be looking at only the first three, because you will be using these frequently in comparison.

# [g](#toc.xhtml_s334a)

The g stands for global search. It will return all the occurrences of the match. For instance, in the following screenshot, when we add the g flag to our match pattern of "*is*", we get three "*is*". Apart from the two obvious "*is*", it also caught the "*is*" inside "*This*":

![](images/Figure-14.9.jpg)

**Figure 14.9:** An example of g

# [i](#toc.xhtml_s335a)

The i stands for case-insensitive search. It will return the first occurrence of the word irrespective of its case. For instance, in the following screenshot, when we add the **`i`** flag to our match pattern of "*she*", we get the first "*She*" and not the other one:

![](images/Figure-14.10.jpg)

**Figure 14.10:** An example of i

# [m](#toc.xhtml_s336a)

The **m** stands for multi-line search. It will return the first occurrence of the word, irrespective of its case.

![](images/Figure-14.11.jpg)

**Figure 14.11:** An example of m

As mentioned earlier, the shortcomings of **m** and **i** flags are that they are case-sensitive and return only the first match. To overcome this, we can combine the three flags to perform a case-insensitive, multi-line search that returns all the matches:

![](images/Figure-14.12.jpg)

**Figure 14.12:** An example of gim

# [JavaScript methods for Regular Expressions](#toc.xhtml_s337a)

In the previous few sections, we checked two JavaScript methods that can be used for working with Regular Expressions. Now, we will look at a few more JavaScript methods:

# [exec()](#toc.xhtml_s338a)

The **`exec()`** method belongs to the RegExp object that we had seen earlier in this chapter. It performs the same functionality as match. However, here, we add the string to be checked for as an argument to the exec method:

![](images/Figure-14.13.jpg)

**Figure 14.13:** An example of exec

# [test()](#toc.xhtml_s339a)

The **`test()`** method also belongs to the RegExp object. It returns true or false based on the search result:

![](images/Figure-14.14.jpg)

**Figure 14.14:** An example of test

# [matchAll()](#toc.xhtml_s340a)

The **`matchAll()`** method is similar to **`match()`**. The **`match()`** returns only the first matched value, while **`matchAll()`** returns a RegExp String Iterator array of all the matched values:

![](images/Figure-14.15.jpg)

**Figure 14.15:** An example of matchAll

# [replace()](#toc.xhtml_s341a)

The **`replace()`** method searches for a string and replaces it with the value provided in the second argument. It returns a new string with the replaced value:

![](images/Figure-14.16.jpg)

**Figure 14.16:** An example of replace

# [replaceAll()](#toc.xhtml_s342a)

The **`replaceAll()`** method searches for all occurrences of the regular expression in the string and replaces all with the value provided in the second argument, forgoing the grammatical mistake:

![](images/Figure-14.17.jpg)

**Figure 14.17:** An example of replaceAll

# [Practical example of Regular Expressions](#toc.xhtml_s343a)

Now that we have a fair understanding of regular expressions, let’s have a look at the most common example of regular expressions. In this example, we will be using regular expressions to validate an email address.

A valid email address, (for instance, **abc23@gmail.com**), should have a mandatory "@" and a period (".") icon in the text. The "@" symbol should precede the "." and there should be certain text between these two symbols. Similarly, certain text should precede the "@" symbol and follow the "." symbol. Let’s put that down to regular expressions:

1.  The start of, an email address can include case-insensitive characters, digits, underscore ("_"), plus ("+"), period (".") and hyphen. When we add this in a group using square brackets, it signifies a single character. We need to ensure that there are one or more characters of the group. We can achieve that using the "+" quantifier. Let’s visualize that as follows:

    `let emailRegEx = /^[a-zA-Z0-9+_.-]+/;`

    **Code 14.3:** The regular expression to check for start of text

2.  Next, we need to make sure that we add the "@" symbol at the end of *[code example 14.3](#c14.xhtml_co14_3)*. This will make sure that there is always an "@" symbol in the text:

    `let emailRegEx = /^[a-zA-Z0-9+_.-]+@/;`

    **Code 14.4:** The regular expression to check for @

3.  Now, we need to make sure there are more than one characters without any special characters. We can achieve that by adding a group which includes digits and alphabets with a "+" quantifier:

    `let emailRegEx = /^[a-zA-Z0-9+_.-]+@[a-zA-Z0-9]+/;`

    **Code 14.5:** The regular expression to check for text after @

4.  Next, we need to make sure there is a period sign at the end of the *[code example 14.5](#c14.xhtml_co14_5)*. We can add that by including the period sign and escaping it using the "\" icon:

    `let emailRegEx = /^[a-zA-Z0-9+_.-]+@[a-zA-Z0-9]+\./;`

    **Code 14.6:** The regular expression to check for period

5.  Finally, we need to make sure the text after the period sign should have one or more alphabets:

    `let emailRegEx = /^[a-zA-Z0-9+_.-]+@[a-zA-Z0-9]+\.[a-zA-Z]+/;`

    **Code 14.7:** The regular expression to check for text after period

Now that we have the regular expression, let’s test it:

![](images/Figure-14.18.jpg)

**Figure 14.18:** Testing validity of email

# [Conclusion](#toc.xhtml_s344a)

In this chapter, we learned an auxiliary concept called *Regular Expressions*. Regular Expressions are useful for searching patterns inside strings. It is very commonly used when you are searching, for instance, the various bank and account related information in a person’s bank account number or SSN. We started the chapter by learning that there are two ways you can use regular expressions. After that, we learned about the several styles, simple and complex to create search patterns. Finally, we ended our chapter with exploring JavaScript methods for utilizing Regular Expressions. In the next chapter, which is the penultimate chapter of this book, we will look at the various versions of JavaScript that have been released for posterity. We will understand the new features brought about in ES7-ES10.

# [Points to remember](#toc.xhtml_s345a)

*   Regular Expression is a sequence of characters that define a search pattern. It is especially used for finding parts inside a string.
*   You can use square brackets ([]) to restrict your search to a certain character set.
*   ^ denotes the start of a string, and $ denotes the end, while \b is used for adding word boundaries to your search pattern.
*   \d represents all digits, \w represents alphanumeric characters including digits, and underscore, \s represents space.
*   In quantifiers, * represents zero or more occurrences, + signifies one or more occurrences, ? represents zero or one occurrences. If you want to fix the number of occurrences, you can use {} to specify that.
*   The flag g represents all instances of the occurrences, the flag i represents case-insensitive search, while the flag m represents the multi-line search.
*   Finally, JavaScript methods like **`match()`**, **`exec()`**, and **`search()`** help find the position of the searching pattern, **`replace()`** searches and replaces the searching pattern text on the string, and **`test()`** returns whether the pattern exists in a string.

# [Multiple choice questions](#toc.xhtml_s346a)

1.  Which flag is used for case-insensitive search results?
    1.  g
    2.  i
    3.  m
2.  What does the + quantifier do?
    1.  It represents one or more characters match.
    2.  It represents zero or more characters match.
    3.  It represents zero or one characters match.

# [Answers](#toc.xhtml_s347a)

1.  **b**
2.  **c**

# [CHAPTER 15](#toc.xhtml_c15)

# [Life After ES6](#toc.xhtml_c15)

In the very first chapter of this book, we read a piece of short information about the early years of JavaScript. We read about the journey from its scripting origin to ES6, the version released in 2015\. As we have seen throughout this book, the majority of the modern browsers and UI frameworks actively support and recommend ES6\. The journey of JavaScript, however, doesn't stop at ES6. ECMA International (the Swiss standards association), tasked with the standardization of ECMAScript, releases a new set of specifications every year to keep up with the changing trends in the world of programming. In this chapter, we will look at the new sets of specifications released every year after ES6.

# [Structure](#toc.xhtml_s348a)

In this chapter, we will cover the following topics:

*   Introduction to ECMAScript
*   ES7
*   ES8
*   ES9
*   ES10
*   ES11
*   ES.next

# [Objective](#toc.xhtml_s349a)

After studying this chapter, you should be able to clearly understand the origins of JavaScript, and how it has shaped up over the years and explore and utilise the new specs released in the latest versions.

# [Introduction to ECMAScript](#toc.xhtml_s350a)

In *[Chapter 1: Introduction to Javascript](#c01.xhtml)* of this book, we had a quick look at the origins of JavaScript at Netscape. In fact, we used ES5 and ES6 majorly throughout this book. In this section, we will dig a little deeper to understand how the language has shaped itself over the years.

# [The Origin](#toc.xhtml_s351a)

As we have read earlier, the current JavaScript language specification is based on several originating technologies. Primarily, it is based on the following two technologies:

JavaScript for Netscape browsers that was invented by *Brendan Eich* at *Netscape* for the company’s Navigator 2.0 browser.

JScript by Microsoft.

All subsequent browsers from *Netscape Navigator 2.0* and *Microsoft Internet Explorer 3.0* started using this technology.

# [The Browser War](#toc.xhtml_s352a)

When Netscape released the earliest version of JavaScript on its *Navigator 2.0* browser in 1995, it was only supported by Netscape on their browsers.

In 1996, Microsoft released its own scripting dialect called *JScript*.

It’s mentioned by *Douglas Crockford*, an American programmer who is involved in the development of JavaScript, that *Microsoft did not want to deal with Sun Microsystems (Netscape) about the trademark issue, so they called their implementation as JScript, to avoid trademark issues.*

Technically, both the implementations by *Netscape* and *Microsoft* are extremely similar, if not the exact same. However, developers had to create two different implementations of their code to support both the browsers as Microsoft’s version would not work on the Netscape browsers and vice-versa.

# [The Standardization](#toc.xhtml_s353a)

The browser war came to a conclusion with the Swiss standards association ECMA International walking into the picture. *Netscape* and *Sun Microsystems* (who originally owned the trademark for the term JavaScript) approached ECMA International to maintain a specification for JavaScript to enable other browser vendors to implement it. The ECMA International created a community called *Technical Committee 39* (popularly known as TC39) to evolve and maintain the language.

This TC39 (who, at the time of writing, still exists and is in charge of releasing new versions of ECMAScript) released the very first edition of the specification and called it ECMA-262 alias ECMAScript in June 1997.

With its release, several languages adopted these standards, including *JavaScript*.

# [So, is JavaScript the same as ECMAScript?](#toc.xhtml_s354a)

The answer is NO. ECMAScript is the standard upon which JavaScript is based. As we already know, ECMA released the first edition in June 1997. JavaScript adopted the standards of the ECMAScript specification. In fact, several other languages implemented ECMAScript, including the following:

ActionScript (the scripting language behind Flash). It is losing popularity, and was officially discontinued in 2020.

Jscript (the Microsoft scripting dialect). Microsoft adopted the ECMAScript specification for Jscript, thereby enabling all browsers to maintain a standard. Until Microsoft Internet Explorer 9, Microsoft supported JScript before discontinuing it.

**Note:** The TC39 committee, at the time of writing in 2020, includes several top companies like Mozilla, Google, Facebook, Apple, Microsoft, Intel, PayPal, Salesforce, and others. It also includes several top web developers and collaborators. The TC39 is responsible for maintaining and releasing new standards of ECMAScript. Every standard version proposal goes through various stages before being officially released and published in all browsers.

# [The Versions](#toc.xhtml_s355a)

ECMAScript is popularly abbreviated as ES. **ECMAScript 1** (**ES1**), the first version, was released in June 1997\. A year later, in 1998, **ECMAScript 2** (**ES2**) was released with minor editorial changes. ES3, released in December 1999, introduced a lot of popular features like regular expressions, try/catch exception handling, and number formatting. Around this time, World Wide Web became popular and riding on that success, a lot of browsers started supporting ES3, and it became famous.

Work had begun on ES4 in early 2004 and it was deemed to be a major upgrade. However, for some reason, work stopped completely on ES4\. Around this time, several new toolkit libraries based on JavaScript came into existence, like jQuery, Prototype, AJAX, and so on. It rejuvenated the TC39 to begin work on ES4 once again. However, due to technical differences between several companies inside TC39, ES4 was officially abandoned.

Finally, a decade later from 1999, ES5 was released in December 2009. It is the version that is fully supported in all the browsers in use today, (as of 2020). It added several enhancements, like JSON parsing/serialization, Array methods like **`forEach`**, and **`Object.keys`**. It also allowed reserved words like new and for. Finally, it introduced strict mode, which makes JavaScript a cleaner language.

# [ES6 – The new future!](#toc.xhtml_s356a)

Six years after the release of the popular ES5, ECMA International released the next version called ES6 in June 2015\. As we have seen, ES6 released a host of exciting new features that reshaped the way developers worked with JavaScript.

It included features like the following:

*   Block Scope - let and const
*   Arrow functions
*   Classes
*   Template literals
*   Destructuring
*   Promises
*   Modules and many more

Given the history, this time, the TC39 committee decided to release ECMAScript on a yearly cadence. It means, every year, certain modifications and enhancements to the previous version will be released. With this in view, they decided to rename the sixth edition of ECMAScript from ES6 to ECMAScript2015\. However, since the standard was already established, the name ES6 caught on and hence, this version is popularly known as ES6 over ES2015.

And this is what we have learned so far!

# [ES7](#toc.xhtml_s357a)

Following the new yearly cadence, ES7 was released in 2016\. ES7 introduced the following two new features:

# [Array.prototype.includes()](#toc.xhtml_s358a)

It checks whether a value exists in an array. It checks the array for the value passed as an argument. It returns true if array contains the value. Otherwise, it returns false.

Earlier, we needed to check the existence of a value in an array using the Array method **`indexOf`**, and check whether the value returned by **`indexOf`** is not -1\. Now, we can simply use includes to check for the existence:

![](images/Figure-15.1.jpg)

**Figure 15.1:** Example of Array.prototype.includes()

# [Exponentiation Operator](#toc.xhtml_s359a)

The exponent operator that we have seen in *[Chapter 1, Introduction to JavaScript](#c01.xhtml)* was officially introduced in ES7 (ES2016). Using the exponentiation operator denoted by **, you can raise a number to the power specified after the ** symbol, as shown in the following screenshot:

![](images/Figure-15.2.jpg)

**Figure 15.2:** Example of exponentiation operator.

# [ES8](#toc.xhtml_s360a)

In the summer of 2017, the next version ES8 or ES2017 was released. Features included the following:

# [Object.values()](#toc.xhtml_s361a)

Instead of iterating through every element of an object, we can use **`Object.values()`** to return all values of an object in the form of an array:

![](images/Figure-15.3.jpg)

**Figure 15.3:** Example of Object.values

# [Object.entries()](#toc.xhtml_s362a)

It can turn an object into an array of attributes:

![](images/Figure-15.4.jpg)

**Figure 15.4:** Example of Object.entries

# [String padding](#toc.xhtml_s363a)

It pads the current string with another string (multiple times, if needed) until the resulting string reaches the given length. You can add padding at the start using the **`padStart`** method, or at the end using the **`padEnd`** method.

It takes two arguments. The mandatory first argument specifies the target length. It means the length of the resultant string after adding the padded values. If the value of the argument is less than the original string’s length, the original string is returned as is. The second optional argument is a string to be added as a padding.

As shown in *[figure 15.5](#c15.xhtml_fig15_5)*, on the first line, we add the **`padStart(5)`** to the string "Hey". It means the total length of the resultant string after applying **`padStart()`** should be 5. Since we have not added any optional second argument, it adds two white spaces to the start to make the total length as 5\. On the second line, since we have specified a length lesser than the actual length of the string (3), the string is returned as-is. On the fourth line, we use the **`padEnd`** method to the string – loading. We want the target length to be 10\. This time, we have added the optional second argument as '.'. Therefore, when the final string is padded, it adds three dots to the seven length of the original string to create "loading…".

Finally, we use a practical example where we try to hide a phone number. We slice the original number to show only the last three digits, and using **`padStart`**, we add * to the start for the total length of the original number.

![](images/Figure-15.5.jpg)

**Figure 15.5:** Example of string padding

# [Async functions (async and await)](#toc.xhtml_s364a)

The asynchronous keywords **`async`** and **`await`** were introduced in ES8\. It has simplified working with JavaScript promises.

# [Trailing commas in functions](#toc.xhtml_s365a)

ES8 enables us to write a valid declaration with commas in the end. For instance, code example with a trailing comma in argument is valid:

`const getName = (name, age,) => {…}`

**Code 15.1:** An example of trailing commas

# [Object.getOwnPropertyDescriptors()](#toc.xhtml_s366a)

It returns an object describing the configuration of a specific property on a given object. It takes two arguments. The first argument is for the name of the object and the second argument is a specific key of the object.

As shown in the following screenshot, we have used the **`getOwnPropertyDescriptors()`** on our object nations. As you can see, if you don’t specify a value in the second parameter, it returns the property descriptors of all the keys.

![](images/Figure-15.6.jpg)

**Figure 15.6:** Example of property descriptors

# [ES9](#toc.xhtml_s367a)

The ninth edition of ECMAScript was released in 2018\. Amongst the many features, the most significant one are featured as follows:

# [Rest/Spread properties](#toc.xhtml_s368a)

The rest/spread properties that we have seen earlier in this book for arrays was released with ES6\. The rest/spread properties was officially released for objects with ES9.

# [Regular Expression – Lookahead and Lookbehind](#toc.xhtml_s369a)

The lookahead "**`?=`**" assertion and the lookbehind "**`?<=`**" assertion that we learned in the previous chapter were also introduced with ES9.

# [Asynchronous Iterations](#toc.xhtml_s370a)

ES9 introduced the for await…of loop for looping over async and sync iterable objects. Like the await keyword, it can only be used inside **`async`** functions. It is similar to the original for…of loop, but for **`async`** functions:

`(async function() {`

`for await (let num of asyncObj) {`

`console.log(num);`

`}`

`})();`

**Code 15.2:** An example of async iterations

# [Finally in promises](#toc.xhtml_s371a)

In the previous chapters, we have learned and used promises for asynchronous operations. To get the value received by a promise, we would chain **`.then`** and **`.catch`** for catching the resolution and the rejection, respectively. ES9 introduced **finally** for Promises. We can chain finally to the promise, and it will be expected irrespective of the successful or not successful execution of the promise.

As you can see in *[figure 15.7](#c15.xhtml_fig15_7)*, we have created a variable **`isLoading`** at the start of our script. We next create the promise by mocking an asynchronous function with the help of a **`setTimeout`** function. As soon as we create the promise, we turn the **`isLoading`** variable to true. Imagine this to be a flag to show the loading icon on the UI while we wait for a response from the server. As you can see, the value is true.

In *[figure 15.7](#c15.xhtml_fig15_7)*, after three seconds we reject the promise. It makes the catch attached to the promise activated and it receives the text sent with reject. Inside the catch, it logs the statement received from the promise. After that, the finally is executed and we first log a statement saying the promise is completed. Then, we turn the loading flag as false. Imagine this as the flag to toggle the loading on the UI. Since our promise is complete, we turn the flag to false. Hypothetically, we can imagine this to hide the loading icon on the UI. Therefore, the finally in promises is used to carry out any after-effect of a promise.

![](images/Figure-15.7.jpg)

**Figure 15.7:** Example of finally in promises

# [ES10](#toc.xhtml_s372a)

The tenth edition of the ECMAScript was released in 2019\. A few of the most significant features included the following:

# [Array.flat()](#toc.xhtml_s373a)

As the word suggests, it flattens an array. In technical terms, in case of nested arrays, it creates a new array with all sub-array elements concatenated into it recursively up to specified depth. Alternatively, if there are holes or empty spaces in an array, the flat method can remove that.

As seen in the following *[figure 15.8](#c15.xhtml_fig15_8)*:

The first **`console.log`** statement denoted by point "1.", the original array is printed and we can see that after the fourth element, we have an array containing four elements inside it (in which the fourth element is an array).

When we use the flat method on our array, it takes the four elements of the first nested array and concatenates it to the original array, as shown by the second **`console.log`** statement.

If we call the flat method twice on an array, it basically means flattening it for the first time, then calling the flat method on the flattened array received from the first call of flat, as shown by third **`console.log`** statement. Instead, we can add an argument inside the flat method which takes the depth of the array. It means it will flatten the array up to the depth specified in the arguments. In other words, it will call the **`flat()`** method n number of times, where n is the number passed in the argument. You can check this in the statements 3, 4, 5, and 6.

In the seventh statement, we pass Infinity as the argument. It will keep flattening the array until all the sub-arrays are removed.

Finally, in the eight statement, we can see that the empty space in the **`arr2`** was removed by the flat method.

![](images/Figure-15.8.jpg)

**Figure 15.8:** Example of Array.flat()

# [Array.flatMap()](#toc.xhtml_s374a)

The **`Array.flatMap()`** method first maps each element of an array like the normal map method. It then flattens the result into a new array. In the following screenshot, **`flatMap`** maps every element and returns an array of every element which contains the element and its value multiplied by 2\. Finally, it applies **`flat()`** method to these arrays to convert them and concatenate them into one single array.

![](images/Figure-15.9.jpg)

**Figure 15.9:** Example of Array.flatMap()

# [Object.fromEntries()](#toc.xhtml_s375a)

It transforms an iterable object like arrays (not objects) into an object:

![](images/Figure-15.10.jpg)

**Figure 15.10:** Example of Object.fromEntries()

# [String.trimStart() and String.trimEnd()](#toc.xhtml_s376a)

We have seen the JavaScript trim method which trims or removes white spaces from a string. If you wish to remove white spaces only before or only after the string, we can use the preceding methods:

![](images/Figure-15.11.jpg)

**Figure 15.11:** Example of trimStart() and trimEnd()

# [Function.toString()](#toc.xhtml_s377a)

It represents a string representing the source code of a function:

![](images/Figure-15.12.jpg)

**Figure 15.12:** Example of function toString()

# [Optional catch binding](#toc.xhtml_s378a)

Earlier, we needed to provide an argument to the catch of the **`try…catch`** exception handling. After ES10, it is no longer mandatory to provide an argument for the catch.

# [ES11](#toc.xhtml_s379a)

Since this book is written towards the last three months of the year 2020, we also have the eleventh edition of ECMAScript standards that were released in June 2020\. Here are some of the exciting new features with this edition:

Nullish Coalescing operator

Often, you will come across instances where you need to set default values to a variable. You will often use something like the following:

`const price = settings.price || 100;`

**Code 15.3:** An example of default value setting

It means if the price key is not available inside a certain settings object, set the value of the variable price to 100\. However, the default value 100 will be set when the **`settings.price`** is 0 or false or "". It could lead to unwanted results. To avoid this, ES11 introduces the nullish coalescing operator (??). It will make sure the default value is set only if the first condition returns null or undefined:

![](images/Figure-15.13.jpg)

**Figure 15.13:** Example of ??

# [Optional chaining operator](#toc.xhtml_s380a)

Let’s understand this with an example. In *[figure 15.14](#c15.xhtml_fig15_14)*, we are fetching an element using **`document.getElementById`**. On the next line, we check if the element exists. If it exists, we fetch its value to be stored inside the variable **`phoneNumber`**, else we store undefined. We need to do this because if we directly try to access the value of the element and if the element does not exist, the JavaScript code will crash. A cleaner way of achieving this is by using the optional chaining operator (**`?.`**). It will chain the value only if the variable storing the element is not null or undefined. It will automatically store undefined otherwise.

![](images/Figure-15.14.jpg)

**Figure 15.14:** Example of optional chaining operator

# [Private fields](#toc.xhtml_s381a)

In *[Chapter 7: Classes](#c07.xhtml)*, we had read about the need for private variables to hide the crucial internal implementation. Let's have a look at that example again:

A toaster is an easy-to-use machine for toasting slices of bread. If I ask you to toast two slices of bread for me with the help of a toaster, there's a high chance you would not require a manual to do so. A majority of the toasters have the following four or five designated sections:

*   Two or more empty spaces for placing the bread.
*   A lever-like button for popping the slices of bread out.
*   A button for turning on the machine.
*   A knob for adjusting the darkness of the toast.

However, if I open up the machine to its complex internal parts and ask you to repeat the same exercise, would you be able to do that without a manual?

The entire point of this exercise is to help you understand that we should not expose certain internal implementations and methods. In a similar analogy, there are several instances where we would not like to expose the internal variables and methods of classes. For example, if we have a class Person where we store a person's personal information, we would like to ensure that properties like an individual's bank account number or methods like fetching the balance should not be accessible by anyone. These properties and functions should be accessible for usage inside the class only.

In ES11, ECMAScript introduced the # symbol for turning variables and functions private. Adding the hash (#) symbol before a variable or a function will make it accessible only inside the class. Trying to access it from outside will result in error. Let’s look at an example:

![](images/Figure-15.15.jpg)

**Figure 15.15:** Example of private fields

As shown in the preceding screenshot, for obvious reasons, we wish to hide the bank account number of the class Person and the method which is used for fetching the last five transactions. We make them private variables by adding the hash (#) symbol before defining them. Since we have not made the display function as private, it is executed as shown by the first output. Inside display, we invoke (call) the **`fetchLastFiveTransactions`** method. The **`fetchLastFiveTransactions`** method sets the value of the variable **`amountSpent`** to 2345.67\. This value is used for printing on the console. As you can see in *[figure 15.15](#c15.xhtml_fig15_15)*, trying to access the private fields shows undefined and an error, but internally it works like a charm. In this way, you can make fields inside a class private.

# [Dynamic Imports](#toc.xhtml_s382a)

Earlier, whenever we needed to import a file, we needed to add a static declaration like the following:

`import * as modules from './../utils/allModules.js';`

**Code 15.4:** An example of static import

Now, instead of pre-defined imports, you can import dynamically during run-time using the new **`import()`** statement. It can improve the performance speed drastically. You need to provide any string as the parameter, which suffices as a module specifier. It will return a promise:

`const books = await import('./../utils/allModules.js');`

**Code 15.5:** An example of dynamic import

# [Import meta](#toc.xhtml_s383a)

The **`import.meta`** object provides metadata for the current module. A few trusted websites say that it is only available for the property URL, so we will skip it for now.

New export syntax

If you want to import from a certain file and export the file you just imported, you can do that in the following manner. It combines import and export syntax:

`export * as myModule from './../utils/modules.js';`

**Code 15.6:** An example of export

# [New datatype - bigint](#toc.xhtml_s384a)

ES11 introduces a new datatype **`bigint`** for numeric values greater than 253\. So far, every numeric value, including float, belonged to data type Number, and the maximum safe integer is 253\. The new datatype values overcome this shortcoming. It will be especially useful for complex mathematical calculations and large numeric values.

Remember, Number and BigInt are two different datatypes.

# [globalThis](#toc.xhtml_s385a)

We have seen and experienced the pains of using the "**`this`**" variable throughout JavaScript’s history. Finally, we have a new JavaScript object **`globalThis`**, which always accesses the global object across different JavaScript environments.

# [matchAll](#toc.xhtml_s386a)

The **`matchAll`** method for regular expressions that we saw in the previous chapter was introduced in ES11.

# [Promise.allSettled()](#toc.xhtml_s387a)

Given the scope of our book, we did not study about the **`Promise.all()`** method, where you can add multiple promises in the form of an array. It returns a promise only when all promises are fulfilled. However, if one of the promises are rejected, you will only receive a rejection. You will never know the state of the rest of the promises. **`Promise.allSettled()`** resolves this by providing the value of all promises, regardless of their result.

# [ES.Next](#toc.xhtml_s388a)

**`ES.Next`** is a dynamic name for whatever is the next version at the time of writing. At the time of writing, **`ES.Next`** referred to ES12 or ES2021.

# [Conclusion](#toc.xhtml_s389a)

In the chapter, we did an exhaustive exploration of life before and after ES6\. We learned about the origin of the ECMAScript and primarily the difference between ECMAScript and JavaScript. We also looked at every version of ECMAScript specification. In the latter sections, we especially learned about some useful concepts that can help us in improving our coding.

In the final chapter of this book, that is, the next chapter, we will be looking at some handy tips to help you excel at your workplace. We will look at some neat tricks and rules to abide by while coding.

# [Points to remember](#toc.xhtml_s390a)

*   JavaScript and ECMAScript are not the same. ECMAScript is a standard that is followed by JavaScript.
*   After ES6 got released in 2015, the TC39 decided to release yearly cadence of ECMAScript.
*   In the latest version, ES11, we have several top-notch introductions from a new datatype to several new operators.

# [Multiple choice questions](#toc.xhtml_s391a)

1.  **`Object.values`** returns all the keys of an object – True or False?
    1.  True.
    2.  False.
2.  **`Object.fromEntries`** works on objects – True or False?
    1.  True.
    2.  False.

# [Answers](#toc.xhtml_s392a)

1.  **b**
2.  **b**

# [CHAPTER 16](#toc.xhtml_c16)

# [Tips and Tricks](#toc.xhtml_c16)

In the previous fifteen chapters, we have tried to decode, decipher, and simplify the complex network of JavaScript that often unnerves the best of the developers. In the final chapter of this book, we will be taking you through some quirky tips and tricks that are picked up over the years. These tips can help you write optimized code, improve the performance of your code, and amaze your teammates. So, without further ado, let's start the final chapter of simplifying JavaScript.

# [Structure](#toc.xhtml_s393a)

In this final chapter, we will cover the following topics:

*   Best practices
*   Tips and tricks

# [Objective](#toc.xhtml_s394a)

After studying this chapter, you should be able to code efficiently in JavaScript. You will understand and employ the best practices for writing JavaScript. You can write optimized code that will improve the performance of your application and take advantage of the tips and tricks to avoid writing longer code.

# [Best practices](#toc.xhtml_s395a)

In this section, we will be mentioning the best practices that are followed by a vast majority of developers across the world. It’s not mandatory to follow these practices, but it is highly recommended. It will not only help you maintain the readability of your code, but it will also help you improve the efficiency of your code.

# [Naming](#toc.xhtml_s396a)

If you search the term '*best practices*' for any programming language, a majority of the articles will point towards naming. It implies that you should ensure that the names you give to your variables are easy enough for anyone to understand what the variable is storing. For instance, if we ask you to select the code from the following examples that is easier to understand, which will you choose?

1.  `// Example 1`
2.  `let c = "main";`
3.  `let x = f(c);`
4.  `let a = [],`
5.  `     i;`
6.  `for(i=0;i<x.length;i++) {`
7.  `    if(x[i].id.includes("box")) a.push(x[i]);`
8.  `}`
9.  `function f(a) {return document.getElementsByClassName(a);}`
10.  `//-----------------------------------------------------------------------`

12.  `// Example 2`
13.  `let boxElements = [];`
14.  `let className = "main";`
15.  `let elements = findElements(className);`

17.  `for(let index = 0; index < elements.length; index++) {`
18.  `    if(elements[index].id.includes("box")) {`
19.  `        boxElements.push(elements[index]);`
20.  `    }`
21.  `}`

23.  `function findElements(class) {`
24.  `    return document.getElementsByClassName(class);`
25.  `}`

    **Code 16.1:** Naming variables

As we can see in *[code example 16.1](#c16.xhtml_co16_1)*, both the examples 1 and 2 are performing the same task. However, it’s far easier to understand the example 2 than example 1\. If you observe closely, you will notice that every variable clearly denotes what it’s storing or what task it is asked to perform.

**Tip:** A rule of thumb, write the names of variables in such a way that even a person who has no idea of programming should be able to understand what the variable does or stores.

# [Naming conventions](#toc.xhtml_s397a)

In the previous section, we looked at naming variables. Naming conventions implies the way in which you write your variable names. For instance, SQL database developers recommend using underscores to separate multiple words, for example, date_of_birth.

There are four primary styles of conventions:

1.  Hyphens (for example, date-of-birth)
2.  Snake Case (for example, date_of_birth)
3.  Pascal Case (for example, DateOfBirth)
4.  Camel Case (for example, dateOfBirth)

To be quite honest with you, the naming convention for your code depends on the team that you are working with. However, Google Styles and a host of top web developers recommend using the camel case. It means the first letter should be in lower case, and if there are multiple words, the subsequent words should have their first letters capitalized.

Also, Google Styles recommends naming constants in uppercase of snake case, for example, DATE_OF_BIRTH.

**Note:** The problem with hyphens is that it can be mistaken for a subtraction attempt. Similarly, snake cases involve adding underscore to the empty spaces between two words. It is often used in SQL or PHP. Pascal Case is preferred by C programmers.

# [White Spaces](#toc.xhtml_s398a)

An important point to remember while coding is that there will always be someone who will be looking at your code. It could be your peers, your manager, your team lead, or if your work becomes popular, a lot of people wishing to replicate your code will be looking at your code. It’s essential to make their read worthwhile!

One of the best ways to improve code readability is to include appropriate white spaces:

1.  `// Always add spaces between operators, including assignment operators.`
2.  `let name = "John Doe";`
3.  `let sum = number1 + number2;`

5.  `// Add spaces after semicolon (";") inside for loops`
6.  `for(let i=0; i<20; i++) {/*code*/}`

8.  `//Before any curly braces ("{") except when you are using template literals`
9.  `let person = {`
10.  `    name: "John Doe",`
11.  `    address: {`
12.  `        city: "New York",`
13.  `        country: "United States"`
14.  `    }`
15.  `}`

17.  `` let speech = `His name is ${firstName}.` ``

19.  `//All new declarations should be on new line:`
20.  `let firstName,`
21.  `     lastName,`
22.  `    age;`

24.  `//More than one arguments should be on a new line`
25.  `function getRole (`
26.  `    name,`
27.  `    id,`
28.  `    department,`
29.  `    manager`
30.  `) {/*code*/}`

    **Code 16.2:** White spaces

# [Rule of 80](#toc.xhtml_s399a)

The rule that is religiously followed by every top product company in the world is the rule of 80\. It means every line should have a maximum of 80 characters. If the code on your line crosses the 80-charaacter limit, you should wrap it to the next line.

1.  `//The following line contains 91 characters`
2.  `let affordableFruits = foodItems.filter(item => item.type === "fruit" && item.price < 100);`

4.  `//To maintain the rule of 80, you can instead change it to:`
5.  `let affordableFruits = foodItems.filter(item =>`
6.  `    item.type === "fruit" && item.price < 100);`

    **Code 16.3:** Rule of 80

# [Declarations at the top of the scope](#toc.xhtml_s400a)

To maintain code readability, always keep variable declarations at the top of the respective scopes.

# [Consistency with quotes](#toc.xhtml_s401a)

As you already know, JavaScript allows you to use both the single quotes and double quotes for strings. You are free to choose either of the two for your JavaScript files. However, it is very crucial to use the same selection throughout your code. If you have used double quotes, make sure you use the double quotes everywhere in your code, and do not use single quotes anywhere.

# [Comment your code often](#toc.xhtml_s402a)

As I’ve mentioned earlier, your JavaScript code will be viewed by a lot of people. In fact, there will be times when you will refer to your code several months or years after you wrote it for the first time. There will also be instances when you have managed to solve a really complex problem with the help of complicated code. For the preceding reasons, it’s crucial to write appropriate comments at the right places in your code, so that it is easier for you and your viewers to read the code.

# [Tips and Tricks](#toc.xhtml_s403a)

Now that we have a fair idea about the best practices to write JavaScript, let’s explore several tricks to improve code efficiency.

# [Filter unique values in an array](#toc.xhtml_s404a)

If you want to remove the duplicate values from an array, there are several longer ways to achieve this. However, the best way to do this is to use the **`Set`** object type introduced in ES6\. The **`Set`** object lets you store unique values of any type, including primitive values and object references:

![](images/Figure-16.1.jpg)

**Figure 16.1:** Set object type

As you can see in the preceding screenshot, Set object will not allow you to add duplicate values. Now, as shown in *[figure 16.2](#c16.xhtml_fig16_2)*, if you have an array with duplicate values, you can use the **`Set`** object with the spread operator to remove duplicates. As we have understood earlier, the spread operator (…) will copy the values (and not the reference) of an array, and adding the array inside a **`Set`** object will remove the duplicates:

![](images/Figure-16.2.jpg)

**Figure 16.2:** Removing duplicates from an array

# [Object destructuring](#toc.xhtml_s405a)

As shown in *[code example 16.4](#c16.xhtml_co16_4)*, to fetch the values of certain keys from an object, we use the dot notation or the bracket notation to fetch and store their respective values in variables:

1.  `let person = {`
2.  `    name: "John Doe";`
3.  `    age: 27,`
4.  `    language: "English",`
5.  `    nationality: "English",`
6.  `    eyeColor: "black",`
7.  `    gender: "male"`
8.  `};`

10.  `let name = person.name;`
11.  `let age = person.age;`
12.  `let language = person.language;`

    **Code 16.4:** Traditional way of storing object values

You can shorten this process by using object destructuring to fetch only certain keys from an object:

![](images/Figure-16.3.jpg)

**Figure 16.3:** Object destructuring

# [Get last items of an array](#toc.xhtml_s406a)

If you want to fetch the last items of an array, you can use the JavaScript slice method with negative values to fetch it:

![](images/Figure-16.4.jpg)

**Figure 16.4:** Fetching last values of an array

# [Set dynamic keys of an object](#toc.xhtml_s407a)

If you want to dynamically set the key to an object, you can use the square bracket notation to achieve it. For instance, in *[figure 16.5](#c16.xhtml_fig16_5)*, we are creating an object called **`dateObj`**. It will contain the date and the year. However, if it’s a leap year, we want to name the key as leapYear. If it is not, the key name should be year. On line number 2, we take advantage of JavaScript Date object. In the new constructor of Date, the first argument is the year. The second argument is the month, and it starts from 0, i.e., January is 0, February is 1, and so on. The third argument adds the number of days provided in the third argument to the date specified by the first two arguments. It means, new Date (2020, 1) will print the date as February 1, 2020\. If we add the third argument as 29, it will add 29 days to February 1, 2020\. If 2020 is a leap year, 29 days after the leap year should give the result as February 29, 2020\. If it is not a leap year, the result will be March 1, 2020.

On the second line, we perform the operation mentioned earlier and then, we fetch the month of the result. If it’s a leap year, the month will be February, that is, 1 (since January is 0) and if it is not a leap year, the month will be March, that is, 2\. If the value is 1, we store the value "*leapYear*" in the variable **`keyName`** or else, we store the value "**`year`**".

With the help of bracket notation, we are now storing the dynamic key name for object:

![](images/Figure-16.5.jpg)

**Figure 16.5:** Dynamic key names

# [Truncate an array](#toc.xhtml_s408a)

If you want to remove the values from an array destructively, you can set the length of the array to the value from where you want to remove the values:

![](images/Figure-16.6.jpg)

**Figure 16.6:** Truncating an array

# [Improving conditionals](#toc.xhtml_s409a)

If we want to execute some code based on a condition, we tend to do the following:

1.  `let isLeap = new Date(2020, 1, 29).getMonth() === 1;`

3.  `if(isLeap === true) {`
4.  `    printStatement();`
5.  `}`

7.  `function printStatement() {`
8.  ``    console.log(`It is a leap year.`);``
9.  `}`

    **Code 16.5:** Traditional way of writing conditionals

Instead, we can shorten this process with the help of the logical operator &&. As shown in the following screenshot, if **`isLeap`** is true, then the function **`printStatement`** will be executed:

![](images/Figure-16.7.jpg)

**Figure 16.7:** New way of conditionals

# [Setting default values](#toc.xhtml_s410a)

To set default values, we can either use the || operator, or you can use the nullish coalescing operator (??) introduced in ES11 that we explored in *[Chapter 15: Life After ES6](#c15.xhtml)*:

![](images/Figure-16.8.jpg)

**Figure 16.8:** Setting default values

# [Every and some](#toc.xhtml_s411a)

The every and some methods of an array are useful for testing all the elements of the array against conditions. In the case of every, it will only return true if all the elements of the array pass the conditions as true. Alternatively, some will return true if at least one of the elements passes the condition. Please check the following screenshot:

![](images/Figure-16.9.jpg)

**Figure 16.9:** Every and some

# [Conclusion](#toc.xhtml_s412a)

We concluded simplifying JavaScript in this book with this chapter on tips and tricks. Before this chapter, we had a look at several concepts of JavaScript. In this chapter, we brought a conclusion to all our learnings with the best practices and the tips and tricks. Although it is not mandatory, it is highly recommended to follow the best practices mentioned in this chapter. It will help you become global-ready for any UI Development.

In this chapter, we also looked at several tips and tricks to improve the way we write the code. Together, these concepts will help you simplify your JavaScript to a greater extent. Remember, the more you code, the better a coder you will become. Happy Coding!

# [Points to remember](#toc.xhtml_s413a)

*   At the end of the day, you should always write your code with the view that several years down the line, either you will be referring to this code or your work will propel several followers to check your code.
*   Keeping the preceding point in mind, you should always include insightful comments at appropriate places and whitespaces added correctly in your code.
*   Variable names are extremely crucial. As we have seen in the preceding section, unclear variable names can make it extremely confusing to understand the code.
*   Finally, you can use the several tips to improve your coding. In fact, the more you code, the higher are your chances to find even better tips and tricks for JavaScript.

Happy Coding!

# [Index](#toc.xhtml_ind)

A

addEventListener function [27](#c02.xhtml_page27)

advanced operators, ES6

about [113](#c06.xhtml_page113)

rest parameters [114](#c06.xhtml_page114)-[116](#c06.xhtml_page116)

spread operators [116](#c06.xhtml_page116)

template literals [119](#c06.xhtml_page119)

ternary operators [113](#c06.xhtml_page113), [114](#c06.xhtml_page114)

AggregateError [254](#c12.xhtml_page254)

AJAX

about [171](#c09.xhtml_page171), [172](#c09.xhtml_page172)

implementing [178](#c09.xhtml_page178)

process [178](#c09.xhtml_page178)

working [178](#c09.xhtml_page178)

anonymous function

about [54](#c03.xhtml_page54)

using [55](#c03.xhtml_page55)

API page, MealDB platform [206](#c10.xhtml_page206)

application development. *See* live application - Nom Nom

Application Panel [34](#c02.xhtml_page34)

Application Programming Interface (API) [206](#c10.xhtml_page206)

apply method [112](#c06.xhtml_page112)

arithmetic operations [11](#c01.xhtml_page11)

array destructuring, ES6 [127](#c06.xhtml_page127)

array literal

using [65](#c04.xhtml_page65), [66](#c04.xhtml_page66)

Array.prototype.includes() [304](#c15.xhtml_page304), [305](#c15.xhtml_page305)

arrays

about [10](#c01.xhtml_page10), [63](#c04.xhtml_page63)-[65](#c04.xhtml_page65)

array, creating [65](#c04.xhtml_page65)

array, declaring [65](#c04.xhtml_page65)

array, initializing [66](#c04.xhtml_page66)

array literal, using [65](#c04.xhtml_page65)

array, slicing [76](#c04.xhtml_page76)

array, splicing [75](#c04.xhtml_page75)

elements, accessing [67](#c04.xhtml_page67), [68](#c04.xhtml_page68)

elements, changing [68](#c04.xhtml_page68), [69](#c04.xhtml_page69)

elements, deleting [72](#c04.xhtml_page72), [73](#c04.xhtml_page73)

first element, accessing [70](#c04.xhtml_page70)

JavaScript keyword new, using [65](#c04.xhtml_page65)

last element, accessing [70](#c04.xhtml_page70)

looping through [70](#c04.xhtml_page70)

properties and methods [69](#c04.xhtml_page69)

using [65](#c04.xhtml_page65)

arrow functions, ES6

about [121](#c06.xhtml_page121)

shorter syntax [121](#c06.xhtml_page121), [122](#c06.xhtml_page122)

this keyword in functions [122](#c06.xhtml_page122), [123](#c06.xhtml_page123)

assertions

^ [288](#c14.xhtml_page288)

$ [288](#c14.xhtml_page288)

\b [288](#c14.xhtml_page288)

x(?=y) [288](#c14.xhtml_page288), [289](#c14.xhtml_page289)

(?<=y)x [288](#c14.xhtml_page288), [289](#c14.xhtml_page289)

assignment operators [11](#c01.xhtml_page11)

async function

about [161](#c08.xhtml_page161)

example [161](#c08.xhtml_page161), [162](#c08.xhtml_page162)

asynchronous JavaScript

about [147](#c08.xhtml_page147)

using [148](#c08.xhtml_page148)

autoincrement parameter [244](#c11.xhtml_page244)

await keyword

using, with async function [162](#c08.xhtml_page162), [163](#c08.xhtml_page163)

B

Behavior-Driven Development (BDD) [271](#c13.xhtml_page271)

best practices

about [320](#c16.xhtml_page320)

comment your code often [323](#c16.xhtml_page323)

consistency with quotes [323](#c16.xhtml_page323)

naming [320](#c16.xhtml_page320), [321](#c16.xhtml_page321)

naming conventions [321](#c16.xhtml_page321)

rule of [80](#c05.xhtml_page80) [323](#c16.xhtml_page323)

variable declarations, at top of scopes [323](#c16.xhtml_page323)

white spaces [322](#c16.xhtml_page322)

bind method [111](#c06.xhtml_page111)

block-level scope

about [104](#c06.xhtml_page104)

creating [104](#c06.xhtml_page104)

booleans [10](#c01.xhtml_page10)

breakpoints

about [42](#c02.xhtml_page42)

used, for debugging [260](#c12.xhtml_page260)-[264](#c12.xhtml_page264)

breakpoints, adding to JS code

breakpoint, selecting in DevTools [42](#c02.xhtml_page42)

debugger, adding to code [41](#c02.xhtml_page41)

JavaScript execution, pausing at debugger [43](#c02.xhtml_page43)-[45](#c02.xhtml_page45)

C

Caches API

about [248](#c11.xhtml_page248)

URL [248](#c11.xhtml_page248)

callback function

about [148](#c08.xhtml_page148)

example [148](#c08.xhtml_page148), [149](#c08.xhtml_page149)

using, in asynchronous JavaScript [149](#c08.xhtml_page149)-[152](#c08.xhtml_page152)

callback hell [152](#c08.xhtml_page152), [154](#c08.xhtml_page154)

call method [111](#c06.xhtml_page111), [112](#c06.xhtml_page112)

car object

methods [82](#c05.xhtml_page82), [83](#c05.xhtml_page83)

properties [82](#c05.xhtml_page82)

catch block [265](#c12.xhtml_page265), [266](#c12.xhtml_page266)

Chai

about [274](#c13.xhtml_page274)

reference link [274](#c13.xhtml_page274)

character classes

\ [289](#c14.xhtml_page289)

\d [289](#c14.xhtml_page289)

\D [289](#c14.xhtml_page289)

\s [289](#c14.xhtml_page289)

\t [289](#c14.xhtml_page289)

\w [289](#c14.xhtml_page289)

\W [289](#c14.xhtml_page289)

example [290](#c14.xhtml_page290)

Chrome DevTools

opening [29](#c02.xhtml_page29)-[31](#c02.xhtml_page31)

panels [32](#c02.xhtml_page32)

using, in JS [35](#c02.xhtml_page35)

classes

about [134](#c07.xhtml_page134)

constructor method [136](#c07.xhtml_page136), [137](#c07.xhtml_page137)

general methods [137](#c07.xhtml_page137), [138](#c07.xhtml_page138)

static method [138](#c07.xhtml_page138), [139](#c07.xhtml_page139)

using [135](#c07.xhtml_page135)

client-side storage

about [234](#c11.xhtml_page234)

benefits [234](#c11.xhtml_page234)

closure

about [59](#c03.xhtml_page59), [60](#c03.xhtml_page60)

example [59](#c03.xhtml_page59)

comments [8](#c01.xhtml_page8)

comparison operators [12](#c01.xhtml_page12)

component testing [224](#c10.xhtml_page224)

concat method [76](#c04.xhtml_page76), [77](#c04.xhtml_page77)

conditional coding

about [13](#c01.xhtml_page13)

if…else conditional statement [13](#c01.xhtml_page13), [14](#c01.xhtml_page14)

switch conditional statement [14](#c01.xhtml_page14), [15](#c01.xhtml_page15)

console.log() method

about [255](#c12.xhtml_page255)

used, for debugging code [255](#c12.xhtml_page255)-[260](#c12.xhtml_page260)

Console Panel

about [33](#c02.xhtml_page33), [35](#c02.xhtml_page35)

console area [36](#c02.xhtml_page36)

filter area [36](#c02.xhtml_page36)

construction of building example, web development

development stages [3](#c01.xhtml_page3)

constructor [135](#c07.xhtml_page135)

constructor method [136](#c07.xhtml_page136), [137](#c07.xhtml_page137)

cookies

about [235](#c11.xhtml_page235)

creating, with JavaScript [236](#c11.xhtml_page236)

deleting, with JavaScript [237](#c11.xhtml_page237)

disadvantage [236](#c11.xhtml_page236)

reading, with JavaScript [236](#c11.xhtml_page236)

security [237](#c11.xhtml_page237)

structure [236](#c11.xhtml_page236)

third-party cookies [237](#c11.xhtml_page237)

usage [235](#c11.xhtml_page235)

copy by reference [93](#c05.xhtml_page93)-[95](#c05.xhtml_page95)

copy by value [91](#c05.xhtml_page91)-[93](#c05.xhtml_page93)

Cucumber

about [274](#c13.xhtml_page274)

reference link [274](#c13.xhtml_page274)

D

database [241](#c11.xhtml_page241)

data types

about [8](#c01.xhtml_page8)-[10](#c01.xhtml_page10)

arrays [10](#c01.xhtml_page10)

booleans [10](#c01.xhtml_page10)

numbers [10](#c01.xhtml_page10)

objects [10](#c01.xhtml_page10)

strings [10](#c01.xhtml_page10)

debugger keyword [263](#c12.xhtml_page263), [264](#c12.xhtml_page264)

debugging

about [254](#c12.xhtml_page254), [255](#c12.xhtml_page255)

console.log() method [255](#c12.xhtml_page255)

debugger keyword [263](#c12.xhtml_page263)

with breakpoints [260](#c12.xhtml_page260)-[263](#c12.xhtml_page263)

DELETE method [175](#c09.xhtml_page175)

Developer Tools (DevTools)

about [25](#c02.xhtml_page25), [28](#c02.xhtml_page28)

features [28](#c02.xhtml_page28), [29](#c02.xhtml_page29)

ways, of opening [29](#c02.xhtml_page29)

document.getElementById(id) method [22](#c01.xhtml_page22)

document.getElementsByClassName (classnames) method [22](#c01.xhtml_page22)

document.getElementsByTagName(name) method [22](#c01.xhtml_page22)

Document object [22](#c01.xhtml_page22)

Document Object Model (DOM)

using, in JS [22](#c01.xhtml_page22)

document.querySelector(selectors) method [22](#c01.xhtml_page22)

Domain Name System (DNS) server [19](#c01.xhtml_page19)

DOM tree

creating [19](#c01.xhtml_page19)-[22](#c01.xhtml_page22)

E

ECMAScript

about [3](#c01.xhtml_page3), [302](#c15.xhtml_page302), [303](#c15.xhtml_page303)

browser war [302](#c15.xhtml_page302)

origin [302](#c15.xhtml_page302)

standardization [303](#c15.xhtml_page303)

versions [303](#c15.xhtml_page303), [304](#c15.xhtml_page304)

ECMAScript [1](#c01.xhtml_page1) (ES1) [303](#c15.xhtml_page303)

ECMAScript [2](#c01.xhtml_page2) (ES2) [303](#c15.xhtml_page303)

elements, array

accessing [67](#c04.xhtml_page67)

changing [69](#c04.xhtml_page69)

Elements Panel [32](#c02.xhtml_page32)

end-to-end testing (E2E testing) [272](#c13.xhtml_page272)

entity headers [187](#c09.xhtml_page187)

error handling

with async and await [163](#c08.xhtml_page163)

Error messages [38](#c02.xhtml_page38)

errors

about [252](#c12.xhtml_page252)

types [252](#c12.xhtml_page252)

error types

AggregateError [254](#c12.xhtml_page254)

EvalError [252](#c12.xhtml_page252)

InternalError [254](#c12.xhtml_page254)

RangeError [252](#c12.xhtml_page252), [253](#c12.xhtml_page253)

ReferenceError [253](#c12.xhtml_page253)

SyntaxError [253](#c12.xhtml_page253)

TypeError [253](#c12.xhtml_page253), [254](#c12.xhtml_page254)

URIError [254](#c12.xhtml_page254)

ES6

about [100](#c06.xhtml_page100), [304](#c15.xhtml_page304)

advanced operators [113](#c06.xhtml_page113)

array destructuring [126](#c06.xhtml_page126), [127](#c06.xhtml_page127)

arrow functions [121](#c06.xhtml_page121)

features [100](#c06.xhtml_page100)

new array methods [123](#c06.xhtml_page123)

object destructuring [127](#c06.xhtml_page127), [128](#c06.xhtml_page128)

ES6 classes

about [134](#c07.xhtml_page134), [135](#c07.xhtml_page135)

getters and setters [140](#c07.xhtml_page140), [141](#c07.xhtml_page141)

inheritance [139](#c07.xhtml_page139), [140](#c07.xhtml_page140)

ES6 methods

apply [110](#c06.xhtml_page110)-[112](#c06.xhtml_page112)

bind [110](#c06.xhtml_page110), [111](#c06.xhtml_page111)

call [110](#c06.xhtml_page110)-[112](#c06.xhtml_page112)

ES6 modules [128](#c06.xhtml_page128)-[130](#c06.xhtml_page130)

ES6 Syntax

about [104](#c06.xhtml_page104)

const [104](#c06.xhtml_page104)

let [104](#c06.xhtml_page104)-[106](#c06.xhtml_page106)

ES7

about [304](#c15.xhtml_page304)

Array.prototype.includes() [304](#c15.xhtml_page304), [305](#c15.xhtml_page305)

exponentiation operator [305](#c15.xhtml_page305)

ES8

about [305](#c15.xhtml_page305)

async functions (async and await) [307](#c15.xhtml_page307)

Object.entries() [306](#c15.xhtml_page306)

Object.getOwnPropertyDescriptors() [307](#c15.xhtml_page307), [308](#c15.xhtml_page308)

Object.values() [305](#c15.xhtml_page305)

string padding [306](#c15.xhtml_page306), [307](#c15.xhtml_page307)

trailing commas in functions [307](#c15.xhtml_page307)

ES9

about [308](#c15.xhtml_page308)

asynchronous iterations [309](#c15.xhtml_page309)

finally in promises [309](#c15.xhtml_page309), [310](#c15.xhtml_page310)

regular expression - lookahead and lookbehind [308](#c15.xhtml_page308)

rest/spread properties [308](#c15.xhtml_page308)

ES10

about [310](#c15.xhtml_page310)

Array.flat() [310](#c15.xhtml_page310), [311](#c15.xhtml_page311)

Array.flatMap() method [311](#c15.xhtml_page311)

Function.toString() [312](#c15.xhtml_page312)

Object.fromEntries() [312](#c15.xhtml_page312)

optional catch binding [312](#c15.xhtml_page312)

String.trimEnd() [312](#c15.xhtml_page312)

String.trimStart() [312](#c15.xhtml_page312)

ES11

about [313](#c15.xhtml_page313)

dynamic imports [315](#c15.xhtml_page315)

globalThis [316](#c15.xhtml_page316)

import meta [316](#c15.xhtml_page316)

matchAll method [316](#c15.xhtml_page316)

new datatype bigint [316](#c15.xhtml_page316)

optional chaining operator [313](#c15.xhtml_page313)

private fields [314](#c15.xhtml_page314), [315](#c15.xhtml_page315)

Promise.allSettled() [316](#c15.xhtml_page316)

ES.Next [317](#c15.xhtml_page317)

European Computer Manufacturers Association (ECMA) [2](#c01.xhtml_page2)

EvalError [252](#c12.xhtml_page252)

eval() function [252](#c12.xhtml_page252)

event listener

about [26](#c02.xhtml_page26)

adding, to button [26](#c02.xhtml_page26)-[28](#c02.xhtml_page28)

exact URI [173](#c09.xhtml_page173)

exec() method [294](#c14.xhtml_page294)

exponentiation operator

using [305](#c15.xhtml_page305)

F

filter area, Console Panel

about [36](#c02.xhtml_page36)

types of messages (logs) [36](#c02.xhtml_page36)

filter() method [125](#c06.xhtml_page125), [126](#c06.xhtml_page126)

flags

about [292](#c14.xhtml_page292)

advanced searching, with [292](#c14.xhtml_page292)

example [294](#c14.xhtml_page294)

g [292](#c14.xhtml_page292)

i [293](#c14.xhtml_page293)

m [293](#c14.xhtml_page293)

folder structure, Nom Nom application

creating [196](#c10.xhtml_page196)-[198](#c10.xhtml_page198)

functions

exploring [48](#c03.xhtml_page48)

method [55](#c03.xhtml_page55)

returning values [51](#c03.xhtml_page51)-[53](#c03.xhtml_page53)

types [53](#c03.xhtml_page53)

using [135](#c07.xhtml_page135)

G

general headers [187](#c09.xhtml_page187)

general methods [137](#c07.xhtml_page137), [138](#c07.xhtml_page138)

GET method

about [173](#c09.xhtml_page173)

using [173](#c09.xhtml_page173)

getters and setters method

about [140](#c07.xhtml_page140)

example [141](#c07.xhtml_page141)

g flag [292](#c14.xhtml_page292)

global scope [56](#c03.xhtml_page56)

Google Chrome [4](#c01.xhtml_page4)

grouping regular expression patterns

x|y [286](#c14.xhtml_page286)

[xyz] or [x-z] [287](#c14.xhtml_page287)

[^xyz] or [^x-z] [287](#c14.xhtml_page287)

H

header, Console Panel [38](#c02.xhtml_page38), [39](#c02.xhtml_page39)

HEAD method [176](#c09.xhtml_page176)

home page, Nom Nom application

updating [209](#c10.xhtml_page209)-[212](#c10.xhtml_page212)

HTMLCollection [22](#c01.xhtml_page22)

HTML files, Nom Nom application

creating [198](#c10.xhtml_page198)

index.html [198](#c10.xhtml_page198), [199](#c10.xhtml_page199)

recipe-detail.html [199](#c10.xhtml_page199)-[201](#c10.xhtml_page201)

HTTP headers

about [182](#c09.xhtml_page182)-[186](#c09.xhtml_page186)

entity headers [187](#c09.xhtml_page187)

general headers [187](#c09.xhtml_page187)

request headers [187](#c09.xhtml_page187)

response headers [187](#c09.xhtml_page187)

HTTP methods

about [172](#c09.xhtml_page172)

DELETE method [175](#c09.xhtml_page175)

GET method [173](#c09.xhtml_page173)

HEAD method [176](#c09.xhtml_page176)

OPTIONS request [176](#c09.xhtml_page176)

PATCH request [174](#c09.xhtml_page174), [175](#c09.xhtml_page175)

POST method [173](#c09.xhtml_page173)

PUT method [173](#c09.xhtml_page173)

HTTP status messages

about [176](#c09.xhtml_page176)

status code with 1, information [177](#c09.xhtml_page177)

status code with 2, successful [177](#c09.xhtml_page177)

status code with 3, redirection [177](#c09.xhtml_page177)

status code with 4, client error [177](#c09.xhtml_page177)

status code with 5, client error [178](#c09.xhtml_page178)

Hypertext Transfer Protocol (HTTP) [172](#c09.xhtml_page172)

I

ideal testing structure

end-to-end tests [273](#c13.xhtml_page273)

integration tests [273](#c13.xhtml_page273)

static tests [273](#c13.xhtml_page273)

unit tests [273](#c13.xhtml_page273)

if…else conditional statement [13](#c01.xhtml_page13), [14](#c01.xhtml_page14)

i flag [293](#c14.xhtml_page293)

immediately invoked functions [54](#c03.xhtml_page54)

index [241](#c11.xhtml_page241)

IndexedDB

data, adding [243](#c11.xhtml_page243), [244](#c11.xhtml_page244)

database, opening [242](#c11.xhtml_page242)-[245](#c11.xhtml_page245)

data viewing [245](#c11.xhtml_page245)

hierarchy [241](#c11.xhtml_page241)

process [242](#c11.xhtml_page242)

support, checking [242](#c11.xhtml_page242)

IndexedDB API

about [240](#c11.xhtml_page240)

features [241](#c11.xhtml_page241)

IndexedDB terms

database [241](#c11.xhtml_page241)

index [241](#c11.xhtml_page241)

object store [241](#c11.xhtml_page241)

transaction [241](#c11.xhtml_page241)

index.html file [198](#c10.xhtml_page198)

Info messages [38](#c02.xhtml_page38)

inheritance

about [139](#c07.xhtml_page139)

example [139](#c07.xhtml_page139), [140](#c07.xhtml_page140)

Integrated Development Environment (IDE) software [4](#c01.xhtml_page4)

integration testing [225](#c10.xhtml_page225), [272](#c13.xhtml_page272)

InternalError [254](#c12.xhtml_page254)

J

Jasmine

about [275](#c13.xhtml_page275)

reference link [275](#c13.xhtml_page275)

JavaScript

about [1](#c01.xhtml_page1), [2](#c01.xhtml_page2)

applying, to web page [5](#c01.xhtml_page5)

Chrome DevTools, using [35](#c02.xhtml_page35)

closure [59](#c03.xhtml_page59)

comments [8](#c01.xhtml_page8)

conditional coding [13](#c01.xhtml_page13)

conditionals [13](#c01.xhtml_page13)

data types [8](#c01.xhtml_page8)

DOM, using [22](#c01.xhtml_page22), [23](#c01.xhtml_page23)

event listeners [26](#c02.xhtml_page26)

exploring [3](#c01.xhtml_page3)

features [4](#c01.xhtml_page4)

inception [2](#c01.xhtml_page2)

looping [13](#c01.xhtml_page13), [16](#c01.xhtml_page16)

objects [82](#c05.xhtml_page82)

operators [8](#c01.xhtml_page8), [11](#c01.xhtml_page11)

scope [56](#c03.xhtml_page56)

system, setting up [4](#c01.xhtml_page4)

variables [8](#c01.xhtml_page8)

web development example [3](#c01.xhtml_page3)

JavaScript, adding to code

external JavaScript [6](#c01.xhtml_page6), [7](#c01.xhtml_page7)

internal JavaScript [5](#c01.xhtml_page5)

JavaScript exception handling

keywords [264](#c12.xhtml_page264)

JavaScript hoisting

about [100](#c06.xhtml_page100), [101](#c06.xhtml_page101)

examples [101](#c06.xhtml_page101), [102](#c06.xhtml_page102)

with functions [103](#c06.xhtml_page103), [104](#c06.xhtml_page104)

JavaScript (JS) function

about [48](#c03.xhtml_page48)

calling [50](#c03.xhtml_page50), [51](#c03.xhtml_page51)

creating [49](#c03.xhtml_page49)

declaring [49](#c03.xhtml_page49)

invoking [50](#c03.xhtml_page50)

syntax [48](#c03.xhtml_page48)

JavaScript keyword new

using [65](#c04.xhtml_page65), [66](#c04.xhtml_page66)

JavaScript keyword var [104](#c06.xhtml_page104), [105](#c06.xhtml_page105)

JavaScript methods, for regular expression

exec() method [294](#c14.xhtml_page294)

matchAll() method [295](#c14.xhtml_page295)

replaceAll() method [296](#c14.xhtml_page296)

replace() method [295](#c14.xhtml_page295)

test() method [295](#c14.xhtml_page295)

JavaScript Object Notation. *See* JSON

JavaScript, on Chrome DevTools

about [35](#c02.xhtml_page35)

Console Panel [35](#c02.xhtml_page35)

header of console panel [38](#c02.xhtml_page38)

Sources Panel [39](#c02.xhtml_page39), [40](#c02.xhtml_page40)

Jest

about [275](#c13.xhtml_page275)

function, creating for testing [278](#c13.xhtml_page278)

installing, npm or yarn used [277](#c13.xhtml_page277), [278](#c13.xhtml_page278)

new project, initializing [276](#c13.xhtml_page276), [277](#c13.xhtml_page277)

package.json, adding/modifying [279](#c13.xhtml_page279), [280](#c13.xhtml_page280)

package managers, installing [276](#c13.xhtml_page276)

reference link [275](#c13.xhtml_page275)

test file, creating [278](#c13.xhtml_page278), [279](#c13.xhtml_page279)

test, running [280](#c13.xhtml_page280), [281](#c13.xhtml_page281)

using [276](#c13.xhtml_page276)

join method [77](#c04.xhtml_page77), [78](#c04.xhtml_page78)

jsdom

about [274](#c13.xhtml_page274)

reference link [274](#c13.xhtml_page274)

JSON

about [166](#c09.xhtml_page166), [167](#c09.xhtml_page167)

data, exchanging [171](#c09.xhtml_page171)

JSON.parse() method [170](#c09.xhtml_page170)

JSON.stringify() method [169](#c09.xhtml_page169)

object format [168](#c09.xhtml_page168)

string format [168](#c09.xhtml_page168)

structure [168](#c09.xhtml_page168)

working with [169](#c09.xhtml_page169)

JSON.parse() method [170](#c09.xhtml_page170)

JSON.stringify() method [169](#c09.xhtml_page169), [170](#c09.xhtml_page170)

K

Karma

about [274](#c13.xhtml_page274)

reference link [274](#c13.xhtml_page274)

keypath parameter [244](#c11.xhtml_page244)

keyword const

about [108](#c06.xhtml_page108)

features [108](#c06.xhtml_page108), [109](#c06.xhtml_page109)

keyword let

features [106](#c06.xhtml_page106)-[108](#c06.xhtml_page108)

keywords, JavaScript exception handling

catch [265](#c12.xhtml_page265)

finally [265](#c12.xhtml_page265)

throw [265](#c12.xhtml_page265)

try [265](#c12.xhtml_page265)

L

length property [69](#c04.xhtml_page69)

Lexical Scope [58](#c03.xhtml_page58)

live application - Nom Nom

about [192](#c10.xhtml_page192)

design [195](#c10.xhtml_page195), [196](#c10.xhtml_page196)

flow [194](#c10.xhtml_page194)

folder structure, creating [196](#c10.xhtml_page196)

foundations, laying [196](#c10.xhtml_page196)

home page, updating with server response [209](#c10.xhtml_page209)-[212](#c10.xhtml_page212)

HTML files, creating [198](#c10.xhtml_page198)

idea [194](#c10.xhtml_page194)

initial styling [201](#c10.xhtml_page201)-[205](#c10.xhtml_page205)

recipe detail page, creating [213](#c10.xhtml_page213), [214](#c10.xhtml_page214)

recipe detail page, updating [214](#c10.xhtml_page214), [215](#c10.xhtml_page215)

request, sending to server with id [217](#c10.xhtml_page217)

server, connecting to [206](#c10.xhtml_page206)-[208](#c10.xhtml_page208)

software development lifecycle [192](#c10.xhtml_page192), [193](#c10.xhtml_page193)

testing [224](#c10.xhtml_page224)

local scope [56](#c03.xhtml_page56), [57](#c03.xhtml_page57)

local storage

about [239](#c11.xhtml_page239)

value, fetching from [240](#c11.xhtml_page240)

value, removing from [240](#c11.xhtml_page240)

value, setting [239](#c11.xhtml_page239)

logged messages

Error messages [38](#c02.xhtml_page38)

Info messages [38](#c02.xhtml_page38)

Verbose messages [38](#c02.xhtml_page38)

Warning messages [38](#c02.xhtml_page38)

logical operators [12](#c01.xhtml_page12)

looping

about [16](#c01.xhtml_page16)

do…while loop [17](#c01.xhtml_page17)

for loop [16](#c01.xhtml_page16), [17](#c01.xhtml_page17)

while loop [16](#c01.xhtml_page16), [17](#c01.xhtml_page17)

M

map() method [124](#c06.xhtml_page124), [125](#c06.xhtml_page125)

matchAll() method [295](#c14.xhtml_page295)

Memory Panel [34](#c02.xhtml_page34)

method function [55](#c03.xhtml_page55)

methods and properties, arrays. *See* properties and methods, arrays

methods, for selecting elements from DOM

document.getElementById(id) [22](#c01.xhtml_page22)

document.getElementsByClassName (classnames) [22](#c01.xhtml_page22)

document.getElementsByTagName(name) [22](#c01.xhtml_page22)

document.querySelector(selectors) [22](#c01.xhtml_page22)

m flag [293](#c14.xhtml_page293)

Mocha

about [275](#c13.xhtml_page275)

reference link [275](#c13.xhtml_page275)

Mozilla Developer Network (MDN) [167](#c09.xhtml_page167)

N

named functions

about [54](#c03.xhtml_page54)

example [54](#c03.xhtml_page54)

Network Panel [34](#c02.xhtml_page34)

new array methods, ES6

filter() method [125](#c06.xhtml_page125), [126](#c06.xhtml_page126)

map() method [124](#c06.xhtml_page124), [125](#c06.xhtml_page125)

reduce() method [126](#c06.xhtml_page126)

Nom Nom application

web page [184](#c09.xhtml_page184)

npm [276](#c13.xhtml_page276)

numbers [10](#c01.xhtml_page10)

O

Object Constructors [85](#c05.xhtml_page85), [95](#c05.xhtml_page95)-[97](#c05.xhtml_page97)

object definition

about [84](#c05.xhtml_page84)

constructor [85](#c05.xhtml_page85)

JavaScript keyword new [84](#c05.xhtml_page84), [85](#c05.xhtml_page85)

object literal, using [84](#c05.xhtml_page84)

object destructuring, ES6 [127](#c06.xhtml_page127), [128](#c06.xhtml_page128)

object methods [85](#c05.xhtml_page85)

object-oriented programming (OOP) language [81](#c05.xhtml_page81)

object properties

about [85](#c05.xhtml_page85), [86](#c05.xhtml_page86)

accessing [86](#c05.xhtml_page86)

changing [87](#c05.xhtml_page87)

displaying [87](#c05.xhtml_page87)

displaying by name [88](#c05.xhtml_page88)

dot notation [86](#c05.xhtml_page86)

looping through [88](#c05.xhtml_page88)

square bracket notation [86](#c05.xhtml_page86)

Object Prototypes [97](#c05.xhtml_page97)

objects

about [10](#c01.xhtml_page10), [82](#c05.xhtml_page82), [83](#c05.xhtml_page83)

car example [82](#c05.xhtml_page82)

displaying, by looping through properties [88](#c05.xhtml_page88)

syntax [83](#c05.xhtml_page83)

using [84](#c05.xhtml_page84)

object store [241](#c11.xhtml_page241)

Object.values()

object methods [89](#c05.xhtml_page89)

objects, versus primitive values [90](#c05.xhtml_page90), [91](#c05.xhtml_page91)

this keyword [90](#c05.xhtml_page90)

using [89](#c05.xhtml_page89)

onreadystatechange property

example [181](#c09.xhtml_page181), [182](#c09.xhtml_page182)

operators

about [8](#c01.xhtml_page8), [11](#c01.xhtml_page11)

arithmetic operators [11](#c01.xhtml_page11)

assignment operators [11](#c01.xhtml_page11)

comparison operators [12](#c01.xhtml_page12)

logical operators [12](#c01.xhtml_page12)

string operators [11](#c01.xhtml_page11)

type operators [12](#c01.xhtml_page12)

OPTIONS request [176](#c09.xhtml_page176)

P

panels, Chrome DevTools

about [32](#c02.xhtml_page32)

Application Panel [34](#c02.xhtml_page34)

Console Panel [33](#c02.xhtml_page33)

Elements Panel [32](#c02.xhtml_page32)

Memory Panel [34](#c02.xhtml_page34)

Network Panel [34](#c02.xhtml_page34)

Performance Panel [34](#c02.xhtml_page34)

Security Panel [34](#c02.xhtml_page34)

Sources Panel [33](#c02.xhtml_page33)

PATCH request [174](#c09.xhtml_page174), [175](#c09.xhtml_page175)

Performance Panel [34](#c02.xhtml_page34)

POST method

about [173](#c09.xhtml_page173)

using [173](#c09.xhtml_page173)

practical example, of regular expressions

email address, validating [296](#c14.xhtml_page296), [297](#c14.xhtml_page297)

primitive values

about [90](#c05.xhtml_page90)

data types [90](#c05.xhtml_page90)

problem solving, with template literals

HTML escaping [120](#c06.xhtml_page120)

multi-line statements [120](#c06.xhtml_page120)

string formatting [120](#c06.xhtml_page120)

process, of AJAX

about [182](#c09.xhtml_page182)

create request [178](#c09.xhtml_page178), [179](#c09.xhtml_page179)

open request [179](#c09.xhtml_page179), [180](#c09.xhtml_page180)

send request [180](#c09.xhtml_page180)

wait for response [181](#c09.xhtml_page181)

process, of web page

about [17](#c01.xhtml_page17)

domain name, fetching [18](#c01.xhtml_page18)

DOM tree, creating [19](#c01.xhtml_page19)-[22](#c01.xhtml_page22)

HTTP request, creating [19](#c01.xhtml_page19)

IP address, resolving [19](#c01.xhtml_page19)

response, returning [19](#c01.xhtml_page19)

promises

about [154](#c08.xhtml_page154)

chaining [158](#c08.xhtml_page158)-[161](#c08.xhtml_page161)

concert example [157](#c08.xhtml_page157)

functioning [156](#c08.xhtml_page156), [157](#c08.xhtml_page157)

graphical representation [155](#c08.xhtml_page155)

process [158](#c08.xhtml_page158)

real-life example [154](#c08.xhtml_page154)

syntax [155](#c08.xhtml_page155)

properties and methods, arrays

about [69](#c04.xhtml_page69)

concat [76](#c04.xhtml_page76), [77](#c04.xhtml_page77)

for loop [70](#c04.xhtml_page70)

join [77](#c04.xhtml_page77), [78](#c04.xhtml_page78)

length property [69](#c04.xhtml_page69)

push and pop method [71](#c04.xhtml_page71), [72](#c04.xhtml_page72)

shift and unshift method [73](#c04.xhtml_page73), [74](#c04.xhtml_page74)

splice and slice [75](#c04.xhtml_page75)

toString [77](#c04.xhtml_page77)

PUT method

about [173](#c09.xhtml_page173)

idempotence [174](#c09.xhtml_page174)

versus, POST method [173](#c09.xhtml_page173), [174](#c09.xhtml_page174)

Q

Quality Assurance (QA) [224](#c10.xhtml_page224)

quantifiers

x? [291](#c14.xhtml_page291)

x* [291](#c14.xhtml_page291)

x+ [291](#c14.xhtml_page291)

x{n,} [291](#c14.xhtml_page291)

x{n} [291](#c14.xhtml_page291)

x{n, m} [291](#c14.xhtml_page291)

about [290](#c14.xhtml_page290)

examples [291](#c14.xhtml_page291), [292](#c14.xhtml_page292)

Query String Parameters, Headers tab [187](#c09.xhtml_page187), [188](#c09.xhtml_page188)

R

RangeError [252](#c12.xhtml_page252)

readyState property

about [181](#c09.xhtml_page181)

DONE [181](#c09.xhtml_page181)

HEADERS_RECEIVED [181](#c09.xhtml_page181)

LOADING [181](#c09.xhtml_page181)

OPENED [181](#c09.xhtml_page181)

UNSENT [181](#c09.xhtml_page181)

real-life example, promises

consumer [154](#c08.xhtml_page154)

producer [154](#c08.xhtml_page154)

promise [154](#c08.xhtml_page154)

recipe-detail.html [199](#c10.xhtml_page199)-[201](#c10.xhtml_page201)

recipe detail page, Nom Nom application

creating [213](#c10.xhtml_page213), [214](#c10.xhtml_page214)

detailed recipe, fetching [215](#c10.xhtml_page215)

HTML elements, creating [218](#c10.xhtml_page218)-[223](#c10.xhtml_page223)

id passed from home page, fetching [215](#c10.xhtml_page215)-[217](#c10.xhtml_page217)

link, adding to home page [224](#c10.xhtml_page224)

updating [214](#c10.xhtml_page214), [215](#c10.xhtml_page215)

recursive function [55](#c03.xhtml_page55)

reduce() method [126](#c06.xhtml_page126)

ReferenceError [253](#c12.xhtml_page253)

regression testing [225](#c10.xhtml_page225)

regular expression

about [283](#c14.xhtml_page283), [284](#c14.xhtml_page284)

advanced searching, with flags [292](#c14.xhtml_page292)

creating [284](#c14.xhtml_page284)

flags [292](#c14.xhtml_page292)

JavaScript methods [294](#c14.xhtml_page294)

JavaScript RegExp object, using [285](#c14.xhtml_page285)

practical example [296](#c14.xhtml_page296), [297](#c14.xhtml_page297)

regular expression literal, writing [284](#c14.xhtml_page284)

regular expression pattern

about [285](#c14.xhtml_page285)

assertions [288](#c14.xhtml_page288)

character classes [289](#c14.xhtml_page289)

grouping regular expression patterns [286](#c14.xhtml_page286)

groups and ranges, using [286](#c14.xhtml_page286)

quantifiers [290](#c14.xhtml_page290), [291](#c14.xhtml_page291)

simple patterns, using [285](#c14.xhtml_page285), [286](#c14.xhtml_page286)

special characters, using [287](#c14.xhtml_page287)

reject(error) [155](#c08.xhtml_page155)

replaceAll() method [296](#c14.xhtml_page296)

replace() method [295](#c14.xhtml_page295)

request headers [187](#c09.xhtml_page187)

resolve(value) [155](#c08.xhtml_page155)

response headers [187](#c09.xhtml_page187)

rest parameters [114](#c06.xhtml_page114)-[116](#c06.xhtml_page116)

S

sanity testing [225](#c10.xhtml_page225)

scope

about [56](#c03.xhtml_page56)

functions [58](#c03.xhtml_page58)

global scope [56](#c03.xhtml_page56)

local scope [56](#c03.xhtml_page56)

points to remember [57](#c03.xhtml_page57)

Security Panel [34](#c02.xhtml_page34)

Selenium

about [275](#c13.xhtml_page275)

reference link [275](#c13.xhtml_page275)

service workers

about [246](#c11.xhtml_page246)

registering [247](#c11.xhtml_page247)

working with [246](#c11.xhtml_page246)

session storage

about [238](#c11.xhtml_page238)

value, fetching from [238](#c11.xhtml_page238), [239](#c11.xhtml_page239)

value, removing from [239](#c11.xhtml_page239)

value, setting [238](#c11.xhtml_page238)

setRequestHeader() [188](#c09.xhtml_page188), [189](#c09.xhtml_page189)

shift method [73](#c04.xhtml_page73), [74](#c04.xhtml_page74)

shorter syntax [121](#c06.xhtml_page121), [122](#c06.xhtml_page122)

simple patterns

about [285](#c14.xhtml_page285)

using [285](#c14.xhtml_page285), [286](#c14.xhtml_page286)

slice method [76](#c04.xhtml_page76)

smoke testing [224](#c10.xhtml_page224)

software development lifecycle

about [192](#c10.xhtml_page192)

business requirements gathering [193](#c10.xhtml_page193)

design [193](#c10.xhtml_page193)

development [193](#c10.xhtml_page193)

idea [193](#c10.xhtml_page193)

public release [193](#c10.xhtml_page193)

testing [193](#c10.xhtml_page193)

Sources Panel [33](#c02.xhtml_page33), [39](#c02.xhtml_page39), [40](#c02.xhtml_page40)

splice() method [75](#c04.xhtml_page75)

spread operator

about [116](#c06.xhtml_page116)

array, inserting into another array [116](#c06.xhtml_page116), [117](#c06.xhtml_page117)

arrays, concatenating [117](#c06.xhtml_page117)

arrays, copying [118](#c06.xhtml_page118), [119](#c06.xhtml_page119)

static method

about [138](#c07.xhtml_page138)

creating [139](#c07.xhtml_page139)

string literal [119](#c06.xhtml_page119)

string operators [11](#c01.xhtml_page11)

strings [10](#c01.xhtml_page10)

styling [201](#c10.xhtml_page201)

styling, Nom Nom application

maintaining [201](#c10.xhtml_page201)-[205](#c10.xhtml_page205)

switch conditional statement [14](#c01.xhtml_page14), [15](#c01.xhtml_page15)

synchronous JavaScript

about [146](#c08.xhtml_page146)

example [146](#c08.xhtml_page146)

SyntaxError [253](#c12.xhtml_page253)

syntax, for opening request

asynchronous [180](#c09.xhtml_page180)

method [179](#c09.xhtml_page179)

password [180](#c09.xhtml_page180)

URL [179](#c09.xhtml_page179)

username [180](#c09.xhtml_page180)

system

setting up [4](#c01.xhtml_page4)

system testing

about [225](#c10.xhtml_page225)

error handling [229](#c10.xhtml_page229)-[231](#c10.xhtml_page231)

performing [225](#c10.xhtml_page225)

text for loading, adding [226](#c10.xhtml_page226)-[229](#c10.xhtml_page229)

T

template literals

about [119](#c06.xhtml_page119), [120](#c06.xhtml_page120)

example [120](#c06.xhtml_page120)

used, for problem solving [120](#c06.xhtml_page120)

ternary operator

about [113](#c06.xhtml_page113)

example [114](#c06.xhtml_page114)

syntax [113](#c06.xhtml_page113)

Test-Driven Development (TDD) [270](#c13.xhtml_page270), [271](#c13.xhtml_page271)

testing

about [270](#c13.xhtml_page270)

BDD [271](#c13.xhtml_page271)

ideal testing structure [273](#c13.xhtml_page273)

TDD [270](#c13.xhtml_page270), [271](#c13.xhtml_page271)

types [271](#c13.xhtml_page271)

testing frameworks

about [274](#c13.xhtml_page274)

Chai [274](#c13.xhtml_page274)

Cucumber [274](#c13.xhtml_page274)

Jasmine [275](#c13.xhtml_page275)

Jest [275](#c13.xhtml_page275)

jsdom [274](#c13.xhtml_page274)

Karma [274](#c13.xhtml_page274)

Mocha [275](#c13.xhtml_page275)

Selenium [275](#c13.xhtml_page275)

testing, Nom Nom application

component testing [224](#c10.xhtml_page224)

integration testing [225](#c10.xhtml_page225)

regression testing [225](#c10.xhtml_page225)

sanity testing [225](#c10.xhtml_page225)

smoke testing [224](#c10.xhtml_page224)

system testing [225](#c10.xhtml_page225)

unit testing [224](#c10.xhtml_page224)

test() method [295](#c14.xhtml_page295)

this keyword, in ES6 functions [122](#c06.xhtml_page122), [123](#c06.xhtml_page123)

tips and tricks

array, truncating [327](#c16.xhtml_page327)

conditionals, improving [327](#c16.xhtml_page327)

default values, setting [328](#c16.xhtml_page328)

dynamic keys of object, setting [326](#c16.xhtml_page326)

every and some methods [328](#c16.xhtml_page328)

filter unique values, in array [324](#c16.xhtml_page324)

last items of array, fetching [326](#c16.xhtml_page326)

object destructuring [325](#c16.xhtml_page325)

toFixed() method [252](#c12.xhtml_page252)

toString method [77](#c04.xhtml_page77)

transaction [241](#c11.xhtml_page241)

try block [265](#c12.xhtml_page265), [266](#c12.xhtml_page266)

TypeError [253](#c12.xhtml_page253), [265](#c12.xhtml_page265), [266](#c12.xhtml_page266)

type operators [12](#c01.xhtml_page12)

types, of functions

about [53](#c03.xhtml_page53)

anonymous functions [54](#c03.xhtml_page54), [55](#c03.xhtml_page55)

immediately invoked functions [54](#c03.xhtml_page54)

named functions [54](#c03.xhtml_page54)

recursive function [55](#c03.xhtml_page55)

types of messages (logs)

browser messages [37](#c02.xhtml_page37), [38](#c02.xhtml_page38)

user messages [36](#c02.xhtml_page36), [37](#c02.xhtml_page37)

types of testing

end-to-end testing [272](#c13.xhtml_page272)

integration tests [272](#c13.xhtml_page272)

unit tests [272](#c13.xhtml_page272)

U

unit testing [224](#c10.xhtml_page224), [272](#c13.xhtml_page272)

unshift method [73](#c04.xhtml_page73), [74](#c04.xhtml_page74)

URIError [254](#c12.xhtml_page254)

User Experience (UX) team [193](#c10.xhtml_page193)

user interface (UI) [165](#c09.xhtml_page165)

V

variable

about [8](#c01.xhtml_page8)

creating [9](#c01.xhtml_page9)

declaration [9](#c01.xhtml_page9)

initialization [9](#c01.xhtml_page9)

value, assigning [9](#c01.xhtml_page9)

Verbose messages [38](#c02.xhtml_page38)

Visual Studio Code [4](#c01.xhtml_page4)

W

Warning messages [38](#c02.xhtml_page38)

web page

process [17](#c01.xhtml_page17), [18](#c01.xhtml_page18)

web storage

about [234](#c11.xhtml_page234)

client-side storage [234](#c11.xhtml_page234)

testing, on console [248](#c11.xhtml_page248), [249](#c11.xhtml_page249)

Web Storage APIs

about [237](#c11.xhtml_page237), [238](#c11.xhtml_page238)

Caches API [248](#c11.xhtml_page248)

cookies [235](#c11.xhtml_page235)

IndexedDB API [240](#c11.xhtml_page240)

local storage [239](#c11.xhtml_page239)

session storage [238](#c11.xhtml_page238)

web storage practices

future [235](#c11.xhtml_page235)

new school [234](#c11.xhtml_page234)

old school [234](#c11.xhtml_page234)

World Wide Web (WWW) [2](#c01.xhtml_page2)

X

XMLHttpRequest object [178](#c09.xhtml_page178), [179](#c09.xhtml_page179)

Y

yarn [276](#c13.xhtml_page276)