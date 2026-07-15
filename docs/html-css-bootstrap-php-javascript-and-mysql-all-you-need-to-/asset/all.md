## Olga Cucaro

# Html css bootstrap

UUID: 8210cf0f-edb0-461a-8fb6-1bbbc83357c2Questo libro è stato realizzato con StreetLib Write
[https://writeapp.io](https://writeapp.io)

## Indice dei contenuti

*   [HTML, CSS, BOOTSTRAP, PHP, JAVASCRIPT AND MYSQL](#chapter.2.xhtml)
*   [Thanks & copyright](#chapter.3.xhtml)
*   [Summary](#chapter.4.xhtml)
*   [Introduction](#chapter.5.xhtml)
*   [GENERAL PART](#chapter.6.xhtml)
*   [Difference between sites and blogs](#chapter.7.xhtml)
*   [What are domains and hosting](#chapter.8.xhtml)
*   [How to create pages without knowing languages ​​with WordPress](#chapter.9.xhtml)
*   [How to create pages using HTML and CSS](#chapter.10.xhtml)
*   [Dynamic and static sites](#chapter.11.xhtml)
*   [Responsive and Bootstrap sites](#chapter.12.xhtml)
*   [How to use Bootstraps on the internet](#chapter.13.xhtml)
*   [Download the Bootstraps](#chapter.14.xhtml)
*   [Create or modify the style sheets and therefore the graphics of the site](#chapter.15.xhtml)
*   [What are databases and what are they for](#chapter.16.xhtml)
*   [Create and manage databases with phpMyAdmin](#chapter.17.xhtml)
*   [Database Management](#chapter.18.xhtml)
*   [Client-side and server-side languages](#chapter.19.xhtml)
*   [PHP](#chapter.20.xhtml)
*   [The JavaScript](#chapter.21.xhtml)
*   [Example of creating a site](#chapter.22.xhtml)
*   [Create the project](#chapter.23.xhtml)
*   [Use Notepad](#chapter.24.xhtml)
*   [Create the pages](#chapter.25.xhtml)
*   [Change the layout of the pages](#chapter.26.xhtml)
*   [Choose images and colors](#chapter.27.xhtml)
*   [Free and paid images](#chapter.28.xhtml)
*   [Images created specifically for the site](#chapter.29.xhtml)
*   [Use XAMPP OR WAMP in Windows to manage websites locally](#chapter.30.xhtml)
*   [What is WAMP and how it works](#chapter.31.xhtml)
*   [Download and install WAMP](#chapter.32.xhtml)
*   [Use WAMP](#chapter.33.xhtml)
*   [phpMyAdmin and MySQL](#chapter.34.xhtml)
*   [Login and menu for inserting images and news](#chapter.35.xhtml)
*   [Example site pages and scripts](#chapter.36.xhtml)
*   [Site pages in html](#chapter.37.xhtml)
*   [Html pages saved in php as they include php code in them](#chapter.38.xhtml)
*   [Php file to be placed in the site folder](#chapter.39.xhtml)
*   [Other files present in the site folder](#chapter.40.xhtml)
*   [Change the style of the site](#chapter.41.xhtml)
*   [See the site on WAMP](#chapter.42.xhtml)
*   [Publication of the site](#chapter.43.xhtml)
*   [Conclusions](#chapter.44.xhtml)

# HTML, CSS, BOOTSTRAP, PHP, JAVASCRIPT AND MYSQL

All you need to know to create a dynamic site

Inside a complete example of a website with image insertion through password access

Of

Olga Maria Stefania Cucaro 

# Thanks & copyright

I thank all my computer professors and my mother, who allowed me to study this beautiful subject

Copyright by Olga Maria Stefania Cucaro

This book is covered by copyright as well as the example of a site included in the same which despite being a derivative and substantially original work and therefore also covered by copyright

# Summary

Introduction 5

GENERAL PART 6

Difference between sites and blogs 6

What are domains and hosting 6

How to create pages without knowing languages ​​with WordPress 7

How to create pages using HTML and CSS 7

Dynamic and static sites 21

Responsive and Bootstrap sites 21

How to use Bootstraps on the internet 22

Download the Bootstraps 22

Create or modify the style sheets and therefore the graphics of the site 28

What are databases and what are they for 47

Create and manage databases with phpMyAdmin 48

Database Management 49

Client-side and server-side languages 49

PHP 49

The JavaScript 50

Example of creating a site 50

Create the project 50

Use Notepad 51

Create the pages 52

Change the layout of the pages 52

Choose images and colors 53

Free and paid images 53

Images created specifically for the site 53

Use XAMPP OR WAMP in Windows to manage websites locally 53

What is WAMP and how it works 54

Download and install WAMP 54

Use WAMP 54

phpMyAdmin and MySQL 60

Login and menu for inserting images and news 63

Example site pages and scripts 70

Site pages in html 71

Html pages saved in php as they include php code in them 98

Php file to be placed in the site folder 162

Other files present in the site folder 196

Change the style of the site 197

See the site on WAMP 199

Publication of the site 207

Conclusions 214

# Introduction

This book aims to initiate those who want to independently create a website, to the world of domains and programming linked to the web. The author conceived this work as a scientific work intended for educational and study use for all those who approach the study of client-side and server-side programming.

In the first place the difference between the various domains existing on the network will be explained and at a later time we will try to explain the CSS and HTML and then enter the PHP programming (server side) and JavaScript (client side) with the creation of databases via phpMyAdmin.

All this will be explained through an example website created specifically using a free Bootstrap for simplicity and basic convenience and programming a control panel with login connected to the site via database for inserting images directly from the web by uploading them to the database created with connected phpMyAdmin to the site. Obviously, after entering the world of databases and programming, you can apply this knowledge to any other need for iteration by the user required by the site project.

The aim of this study is not to create simple web pages that today can be done easily with WordPress or other easy-to-use software, but for purely educational purposes to explain the use of databases and server and client-side programming to make a dynamic otherwise static site. In summary, this work can be useful for those who want to approach the fascinating world of website programming from the beginning.

# GENERAL PART

# Difference between sites and blogs

The blog is updated daily, or weekly not new news which the blogger has decided to talk about in the blog built ad hoc (cooking blog, programming, etc.). The site can only be updated when company information changes or in the case of a portfolio or e-commerce site when products or prices change.

Sites can be both static and dynamic, while a blog must necessarily be dynamic as it must be continuously updated. Static sites are created in html and css and are only editable by an expert through the source files, while dynamic sites have many iterations with the user that modify the pages automatically. Examples of dynamic sites are e-commerce sites and blogs that allow you to select what interests you or interact with the site in various ways.

To create dynamic and responsive sites or blogs we now use hosting with simple control panels also called Content Management System (CMS) such as the open source Wordpress software. This is the simplest method to continuously and easily create and update your site without having any specific knowledge.

# What are domains and hosting

A domain is required to make a website public. The domain is made available by a provider and can be free or paid. Usually the top-level domains are those that identify a territory, while those that interest users are those of the second, third and fourth level.

The second level domains are those that we will usually find for a fee and identify the user (for example www.user.com). The second and third level ones are mostly available for free on the web (eg we can have www.altervista.user.com). The second, third and fourth level domains can also be connected to your site (eg we can have blog.user.com).

When we want to put web pages online, we must also request a hosting (web space), from the English “to host” which means “to host”. Often the provider we choose will give us both the domain and the free or paid hosting. This depends on the conditions offered by the provider.

In the example that we will explain later in this book, we have chosen a hosting with a free third level domain from Altervista.

Obviously, if you are a programmer and you are selling a site to a customer, you will not be able to use a third level domain, but you will use a second level domain with paid hosting that you will transfer to the company after creating the site or that you will manage annually. This will depend on the contract drawn up with the customer.

As in everything related to programming, the choice of paid or free hosting depends on the final result you want to achieve. Paid hosting has additional services and various e-mail addresses associated with the domain, furthermore being composed only of the name of the company or of the person it could be facilitated in the Google search.

# How to create pages without knowing languages ​​with WordPress

Wordpress is an open source software that allows you to dynamically create and update your blog or site. Through a very intuitive CMS (Content Management System) it allows you to add textual content, videos and images without working on the code directly on the pages of our site. It also offers the possibility if you know the basics of html language, to modify it directly from the source code. Obviously this platform offers many possibilities to use widgets and templates to be able to have, at the end of the creation work, a personalized blog, but not as much as it would allow us to make a personalized creation with html, php, javascript and mysql code where we can create our own. site from scratch with no pre-made themes. To customize the site more based on a theme, I can add a CSS to the

Wordpress is still an excellent choice and also allows us to insert php code. In this case I can go to the theme editor aspect and enter the theme functions a file called function.php. This is not very recommendable as all additional code will be lost when the theme is updated.

Instead, there is a plug-in to insert the php code which is called "Code Snippets". After installation and activation, I will find Snippets on the main menu and I will be able to use some existing files or create new ones.

# How to create pages using HTML and CSS

When we write a site in html, our PC (CLIENT) communicates with another computer called SERVER which provides a response to the Client.

![](images/ebook_image_205181_703517eb8fd7628f.png)

The client makes a request to the Server which responds by interpreting the html language and viewing the site.

To create web pages you can use a simple wordpad or notepad or the more advanced Notepad which also highlights the writing errors of the instructions.

![](images/ebook_image_205181_21fede7b73179a10.jpg)

HTML represents the structure of the site, while CSS can be considered the dress (the graphics) of the site.

HTML is a markup language and not a programming language. In fact, the browser translates the code and allows us to view the web page.

The tags are essential to give a structure to the page which will then be translated by the browser.

Example of element or tag:

<h1> Page title </h1>

<h2> Paragraph title </h2>

<p> Page title </p>

![](images/ebook_image_205181_1b8270989c4394fa.jpg)

If we copy this code on a note sheet and save it with an html extension, we will see that our raw site will appear.

![](images/ebook_image_205181_005417cdbf31f424.jpg)

We then save the file with the html extension. We will call it index.html because it is the name that the browser will recognize as the main page of our site.

![](images/ebook_image_205181_8c7cbb94d3e8819f.jpg)

If we double click on the desktop file it will display on the browser:

![](images/ebook_image_205181_99b9ec547b485235.jpg)

You see that the browser recognizes the tags and formats our text as we wanted. This is a simple example of how the browser reads html pages.

The browser then translates the tags into elements of the web page.

From chrome if we type:

Ctrl + u will display the html code of any web page.

***Index.html:***

<! DOCTYPE html>

<html>

<head>

<title> Sample Web Designer | Welcome </title>

</head>

<body>

<header>

<h1> Web Design Example </h1>

</header>

<nav>

<ul>

<li class = "current"> <a href="index.html"> Home </a> </li>

<li> <a href="about.html"> About </a> </li>

<li> <a href="services.html"> Services </a> </li>

</ul>

</nav>

<p> Body of the site </p>

<footer>

<p> Example Web Deisgner, Copyright & copy; 2022 </p>

</footer>

</body>

</html>

<! DOCTYPE html>

<html>

<head>

<title> Sample Web Designer | Welcome </title>

</head>

<body>

<header>

<h1> Web Design Example </h1>

</header>

<nav>

<ul>

<li class = "current"> <a href="index.html"> Home </a> </li>

<li> <a href="about.html"> About </a> </li>

<li> <a href="services.html"> Services </a> </li>

</ul>

</nav>

<p> Body of the site </p>

<footer>

<p> Example Web Deisgner, Copyright & copy; 2022 </p>

</footer>

</body>

</html>

![](images/ebook_image_205181_628cdb868dd82a6a.jpg)

Obviously, if we do not insert the html file of the contacts, an error page will appear.

![](images/ebook_image_205181_50e5ac1543784dbe.jpg)

We must therefore create the contact page.html

<! DOCTYPE html>

<html>

<head>

<title> Sample Web Designer | Welcome </title>

</head>

<body>

<header>

<h1> Web Design Example </h1>

</header>

<p> You can find us via xxxxxx n. xxx <br> our number is xxxx </p>

<footer>

<p> Example Web Deisgner, Copyright & copy; 2022 </p>

</footer>

</body>

</html>

![](images/ebook_image_205181_39f124dc940ff50d.jpg)![](images/ebook_image_205181_e93b60b2d1f6b34c.jpg)

Obviously, a precise page style will be missing which can be inserted directly into the html page or in a particular file defined style.css which will contain the page style file as we will see later.

Now that the files have increased, let's create a special folder for the site that we will call base site and where we will insert the file with the .css extension and the files with the.html extension to view the site, click twice on the index.html page. The style file will also be written to the notepad for simplicity and saved with the .css extension as follows.

***Style.css:***

background {

font: 15px / 1.5 Arial, Helvetica, sans-serif;

padding: 0;

margin: 0;

background-color: # ff55dc;

}

/ * Global * /

.container{

width: 80%;

margin: auto;

overflow: hidden;

}

ul {

margin: 0;

padding: 0;

}

/ * Header ** /

header {

background: blue;

color: #ffffff;

padding-top: 30px;

min-height: 70px;

border-bottom: # e8491d 3px solid;

}

header to {

color: #ffffff;

text-decoration: none;

text-transform: uppercase;

font-size: 16px;

}

header li {

float: left;

display: inline;

padding: 0 20px 0 20px;

}

header #branding {

float: left;

}

header #branding h1 {

margin: 0;

}

header nav {

float: right;

margin-top: 10px;

}

header .highlight, header .current a {

color: # ff6940;

font-weight: bold;

}

header a: hover {

color: #cccccc;

font-weight: bold;

}

footer {

padding: 20px;

margin-top: 20px;

color: #ffffff;

background-color: orange;

text-align: center;

}

***Index.html:***

<! DOCTYPE html>

<html>

<head>

<link rel = "stylesheet" href = "./ style.css">

<title> Sample Web Designer | Welcome </title>

</head>

<body>

<header>

<h1> Web Design Example </h1>

</header>

<nav>

<ul>

<li class = "current"> <a href="index.html"> Home </a> </li>

<li> <a href="contacts.html"> Contacts </a> </li>

</ul>

</nav>

<p> Body of the site </p>

<footer>

<p> Example Web Deisgner, Copyright & copy; 2022 </p>

</footer>

</body>

</html>

![](images/ebook_image_205181_96eba7a4ed31aaed.jpg)

***Contact.html:***

<! DOCTYPE html>

<html>

<head>

<link rel = "stylesheet" href = "./ style.css">

<title> Sample Web Designer | Welcome </title>

</head>

<body>

<header>

<h1> Web Design Example </h1>

</header>

<nav>

<ul>

<li> <a href="index.html"> Home </a> </li>

<li class = "current"> <a href="contacts.html"> Contacts </a> </li>

</ul>

</nav>

<p> You can find us via xxxxxx n. xxx <br> our number is xxxx </p>

<footer>

<p> Example Web Deisgner, Copyright & copy; 2022 </p>

</footer>

</body>

</html>

![](images/ebook_image_205181_23ae2bbba0bca2ae.jpg)

All the html pages that we insert in the folder will have the same formatting inserted in the style.css style sheet

Another choice would be to use other resources available online to create or edit CSS style sheets.

There are some online tools you can use for this, such as:

[https://www.toptal.com/developers/css3maker/](https://www.toptal.com/developers/css3maker/)

[https://css3generator.com/](https://css3generator.com/)

[https://webcode.tools/generators/css/background-color](https://webcode.tools/generators/css/background-color)

[https://css-generator.netlify.app/](https://css-generator.netlify.app/)

Obviously, in addition to the css style sheet, we must create the html files to write the content of the site.

In this regard we can also use the Amaya software with which we can create both the css and html file.

[https://amaya.it.uptodown.com/windows](https://amaya.it.uptodown.com/windows)

![](images/ebook_image_205181_08c4e1c55fecdbc3.jpg)![](images/ebook_image_205181_4f5d2bac56a8b324.jpg)![](images/ebook_image_205181_965928ff86cd8cc9.jpg)![](images/ebook_image_205181_5c87daeaa91fd4b2.jpg)

Nowadays, creating responsive sites that work on any device and with various links and pages can be very complex and take a lot of time so it can be useful to download already prepared models such as bootstraps from the internet or download examples of complete sites directly from the internet. to be modified at will, always respecting the licenses available to the user.

![](images/ebook_image_205181_2776e40399723c87.jpg)![](images/ebook_image_205181_6e67c777397dbb20.jpg)![](images/ebook_image_205181_8e8d88ad3e0b684e.jpg)

# Dynamic and static sites

Static sites are the sites that in past years represented most of the sites on the internet. Today the situation is changing dramatically and static sites are in less and less quantity.

The static site is the simplest to create and provides an unchanged site up to the changes made by the programmer through code. The dynamic site is more sophisticated and requires level programming within the site pages both of the client and server type. The dynamic site allows the user to interact with the site by making queries to the underlying databases and connected to the site itself through a scripting present within the code.

Examples of dynamic sites are:

*   e-commerce with the choice of products in real time

*   social

These sites provide for continuous updating implemented through interactions with the user.

# Responsive and Bootstrap sites

Responsive means reactive which in IT jargon means adaptable. A site is identified as responsive when it can be viewed on all types of devices without detecting any display problems, adapting perfectly to each individual device by automatically resizing and arranging all its parts in the best possible way.

In the past, since there were not many types of devices, the sites could only be made for the PC and we did not remotely think of responsive sites, but now it has become an essential requirement for the creation of websites.

To start we can say that making a site fully responsive is a difficult job. We can say that if we think in percentages and not in pixels in the style sheet and if we insert in the html code of the page:

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

This adapts the page to the surface of the device, but the important thing is to think in percentage terms in the style sheet.

However, given the difficulties inherent in making a site responsive, if you do not want to waste time and are not experts in CSS and html, it is better to use the resources on the internet as we will do in this book to devote ourselves to programming. Resources can be Bootstrap and Wordpress.

# How to use Bootstraps on the internet

# Download the Bootstraps

On the web we can find both paid and free bootstraps and this depends on the resources available to the creator of the site and his needs.

[https://azmind.com/free-bootstrap-themes-templates/](https://azmind.com/free-bootstrap-themes-templates/)

From this site you can download both templates for individual needs and themes, that is to say real fear to be applied to obtain real sites.

[https://getbootstrap.com/docs/3.4/customize/](https://getbootstrap.com/docs/3.4/customize/)

[https://templatemo.com/tm-571-hexashop](https://templatemo.com/tm-571-hexashop)

[https://www.free-css.com/free-css-templates/page273/interior-design](https://www.free-css.com/free-css-templates/page273/interior-design)

[https://www.free-css.com/free-css-templates/page272/be](https://www.free-css.com/free-css-templates/page272/be)

To begin with, we could download a theme of your choice among those available in the various sites just highlighted. After choosing the theme we need also based on the license given. In fact, there are personal and commercial licenses and you have to be careful what type of license you use. This is a useful tip for everything we download from the internet and want to reuse for our projects.

[https://azmind.com/free-bootstrap-business-template-gioia/](https://azmind.com/free-bootstrap-business-template-gioia/)

On the website you will find this description:

Free Joy Template - Bootstrap Business Theme

Updated on: May 29 2018 by Anli

Today's web design resource is a new free Bootstrap template named Gioia and it's a perfect business theme for an agency or portfolio website for yourself or your clients.

Gioia is very similar to Andia template and it comes with 5 responsive pages: Home, Portfolio, Services, About and Contact.

Some of its features include: responsive image slider, modern filterable portfolio, AJAX contact and email subscription forms, Flickr photos, font icons, CSS3 animations, Google Maps, etc.

![](images/ebook_image_205181_5e9ebc78d2ac307c.jpg)

LICENSE:

You can use this template in personal and commercial projects, but you can't sell or distribute it directly, “as is”. If you plan to use it, a link to this page or any form of spreading the word will be much appreciated.

![](images/ebook_image_205181_176c44caacba3efb.jpg)![](images/ebook_image_205181_c962a70352da7199.jpg)

[https://azmind.com/free-html-template-andia-responsive-agency-portfolio-template-twitter-bootstrap/](https://azmind.com/free-html-template-andia-responsive-agency-portfolio-template-twitter-bootstrap/)

On the website you will find this description:

Free HTML Template Andia: Responsive Agency / Portfolio Bootstrap Theme

Today's free web design resource is a big one! It's a responsive agency / portfolio HTML template named Andia and built with Bootstrap. Andia comes with 7 fully responsive pages, Home, Home 2, Portfolio, Services, About, Contact, Pricing Tables and it's perfect for creating a website for a small business or a personal portfolio.

![](images/ebook_image_205181_b9775f5024f599b4.jpg)

You can use this template in personal projects. You can't remove the footer copyright link. Support is not guaranteed or timely.

Commercial License:

You can use this template in commercial projects for yourself or your clients. You can remove the footer copyright link. Support is free and fast.

(not available at the moment)

![](images/ebook_image_205181_05b4bc7338d566fa.jpg)![](images/ebook_image_205181_fc8fccfb2f28b8bb.jpg)

After downloading the folder you will find these files:

![](images/ebook_image_205181_5a84c2a2e41e7203.jpg)

You can also choose a one page bootstrap theme, which is very common now

[https://azmind.com/riona-free-one-page-business-bootstrap-theme/](https://azmind.com/riona-free-one-page-business-bootstrap-theme/)

![](images/ebook_image_205181_f05bf83bbfb0a4ae.jpg)![](images/ebook_image_205181_4e591ccd797b2ee9.jpg)

I unzip the downloaded folder and modify its contents to obtain the site I had imagined.

![](images/ebook_image_205181_4132992947d195fa.jpg)![](images/ebook_image_205181_f3f3aa9d6d4cf2bb.jpg)![](images/ebook_image_205181_86a6ca96f8844ca9.jpg)

# Create or modify the style sheets and therefore the graphics of the site

To change the pages and the css if the license allows me I can use various applications from both desktop and mobile including:

***Nicepage***

![](images/ebook_image_205181_c40a7429a18b8bdd.jpg)

Nicepage to edit html pages and css

![](images/ebook_image_205181_29c56c71a5f2d1ac.png)

Start a tutorial for using the software

![](images/ebook_image_205181_527996e7ec1bb6c2.jpg)

It's great for changing pages quickly.

![](images/ebook_image_205181_33448521d18d4836.jpg)![](images/ebook_image_205181_f4005584bc0840ac.jpg)

If you click on an image, you can change it to the automatic internet search for free images.

![](images/ebook_image_205181_8f77b83b2836ad9b.jpg)![](images/ebook_image_205181_21575890f9e27723.jpg)![](images/ebook_image_205181_a39ed92b8d09bf2c.jpg)

From mobile we can use:

***TrebEdit***

![](images/ebook_image_205181_6773457d89d9cb7d.jpg)![](images/ebook_image_205181_76bd522407b0e515.jpg)![](images/ebook_image_205181_3bd9bb022b64406f.jpg)![](images/ebook_image_205181_2204e33c34ae59b2.jpg)![](images/ebook_image_205181_f785d91f4a3459a5.jpg)

Being responsive, the site will adapt to all devices and therefore it will be displayed on the PC as follows:

![](images/ebook_image_205181_89db417ff860294b.jpg)

The app already has an example of a responsive website with three pages that you can easily edit.

![](images/ebook_image_205181_5df1172571968789.jpg)![](images/ebook_image_205181_00950032aaaae202.jpg)![](images/ebook_image_205181_85519ca1037b0637.jpg)

To view the page from the code you have to click the play arrow at the top right.

From the example in the application by varying some background and font colors in the style.css file and changing the initial image, changing the size of some tags and adding a box and resizing the boxes in the style sheet to fit four boxes to the instead of three, we get a completely different index file:

![](images/ebook_image_205181_e51be7aa6ae518ec.jpg)

The application is very simple to use and contains in the side menu the possibility to select a color with the automatic insertion of the code of the latter in the style sheet.

Being responsive, the site will adapt to all devices and therefore it will be displayed on the PC as follows:

![](images/ebook_image_205181_448da45f1d515e82.jpg)![](images/ebook_image_205181_26e1a15f8f675ccc.jpg)

***Index.html:***

<! DOCTYPE html>

<html>

<head>

<meta charset = "utf-8">

<meta name = "description" content = "Affordable and professional web design">

<meta name = "keywords" content = "web design, affordable web design, professional web design">

<meta name = "author" content = "Brad Traversy">

<title> Sample Web Designer | Welcome </title>

<link rel = "stylesheet" href = "./ css / style.css">

<link rel = "icon" href = "img / favicon.png">

</head>

<body>

<header>

<div class = "container">

<div id = "branding">

<h1> <span class = "highlight"> Example </span> Web Design </h1>

</div>

<nav>

<ul>

<li class = "current"> <a href="index.html"> Home </a> </li>

<li> <a href="about.html"> About </a> </li>

<li> <a href="services.html"> Services </a> </li>

</ul>

</nav>

</div>

</header>

<section id = "showcase">

<h1> <span> Web designer </span> </h1> </h1>

<p> Creating websites is a passion that the author has been pursuing for many years </p>

</div>

</section>

<section id = "newsletter">

<div class = "container">

<h1> Subscribe To Our Newsletter </h1>

<form>

<input type = "email" placeholder = "Enter Email ..." required>

<button type = "submit" class = "button_1"> Subscribe </button>

</form>

</div>

</section>

<section id = "boxes">

<div class = "container">

<div class = "box">

<img src = "./ img / logo_html.png">

<h3> HTML5 Markup </h3>

<p> Writing web pages in html is easier than you think </p>

</div>

<div class = "box">

<img src = "./ img / logo_css.png">

<h3> CSS3 Styling </h3>

<p> Creating an attractive style sheet is crucial for the success of a website </p>

</div>

<div class = "box">

<img src = "./ img / logo_brush.png">

<h3> Graphic Design </h3>

<p> The graphics of a site can determine the success of the site </p>

</div>

<div class = "box">

<img src = "./ img / logo_javascript.png">

<h3> Programmer </h3>

<p> Client-side and server-side programming can make your site dynamic </p>

</div>

</div>

</section>

<footer>

<p> Example Web Deisgner, Copyright & copy; 2022 </p>

</footer>

</body>

</html>

![](images/ebook_image_205181_ef429c516a71bcf2.jpg)

***Style.css:***

background {

font: 15px / 1.5 Arial, Helvetica, sans-serif;

padding: 0;

margin: 0;

background-color: # ff55dc;

}

/ * Global * /

.container{

width: 80%;

margin: auto;

overflow: hidden;

}

ul {

margin: 0;

padding: 0;

}

.button_1 {

height: 38px;

background: # ff5f2a;

border: 0;

padding-left: 20px;

padding-right: 20px;

color: #ffffff;

}

.dark {

padding: 15px;

background: # 5f2420;

color: #ffffff;

margin-top: 10px;

margin-bottom: 10px;

}

/ * Header ** /

header {

background: # 1c3d6e;

color: #ffffff;

padding-top: 30px;

min-height: 70px;

border-bottom: # e8491d 3px solid;

}

header to {

color: #ffffff;

text-decoration: none;

text-transform: uppercase;

font-size: 16px;

}

header li {

float: left;

display: inline;

padding: 0 20px 0 20px;

}

header #branding {

float: left;

}

header #branding h1 {

margin: 0;

}

header nav {

float: right;

margin-top: 10px;

}

header .highlight, header .current a {

color: # ff6940;

font-weight: bold;

}

header a: hover {

color: #cccccc;

font-weight: bold;

}

/ * Showcase * /

#showcase {

min-height: 300px;

background: url ('../ img / showcase.jpg') no-repeat;

background-position: center;

background-size: cover;

text-align: center;

color: #ffffff;

}

#showcase h1 {

margin-top: 100px;

font-size: 55px;

margin-bottom: 10px;

}

#showcase p {

font-size: 35px;

}

/ * Newsletter * /

#newsletter {

padding: 15px;

color: #ffffff;

background: # 1b456d

}

#newsletter h1 {

float: left;

}

#newsletter form {

float: right;

margin-top: 15px;

}

#newsletter input [type = "email"] {

padding: 4px;

height: 25px;

width: 250px;

}

/ * Boxes * /

#boxes {

margin-top: 20px;

}

#boxes .box {

float: left;

text-align: center;

width: 22%;

padding: 10px;

}

#boxes .box img {

width: 70px;

}

/ * Sidebar * /

aside # sidebar {

float: right;

width: 30%;

margin-top: 10px;

}

aside # sidebar .quote input, aside # sidebar .quote textarea {

width: 90%;

padding: 5px;

}

/ * Main-col * /

article # main-col {

float: left;

width: 65%;

}

/ * Services * /

ul # services li {

list-style: none;

padding: 20px;

border: #cccccc solid 1px;

margin-bottom: 5px;

background: # e6e6e6;

}

footer {

padding: 20px;

margin-top: 20px;

color: #ffffff;

background-color: # ff6940;

text-align: center;

}

/ * Media Queries * /

@media (max-width: 768px) {

header #branding,

header nav,

header nav there,

#newsletter h1,

#newsletter form,

#boxes .box,

article # main-col,

aside # sidebar {

float: none;

text-align: center;

width: 100%;

}

header {

padding-bottom: 20px;

}

#showcase h1 {

margin-top: 40px;

}

#newsletter button, .quote button {

display: block;

width: 100%;

}

#newsletter form input [type = "email"], .quote input, .quote textarea {

width: 100%;

margin-bottom: 5px;

}

}

![](images/ebook_image_205181_802ee6baa146f491.jpg)

You can also upload the folders downloaded from the web and modify them at will. With a little practice you can directly modify the css style sheet and in particular the .css file contained in the css folder which varies the graphics of the site and not the content. To vary the content of the pages, however, we must vary the individual Html sheets. By clicking on the arrow of the play we can see the result on the web emulator incorporated in the App.

![](images/ebook_image_205181_e51be7aa6ae518ec.jpg)

# What are databases and what are they for

What are databases? Whenever we want to store data on which we have to operate, we will surely have a database. Databases or databases are like containers that contain the data we want to store. The databases are used not only for the web but also for various kinds of applications created in various programming languages ​​(visual basic, C, python, java, javascript, etc.).

Databases are divided into relational and non-relational. In most cases, relational databases are used, which as you can also understand from the term are based on relationships and in particular on relational tables connected through one-to-one, one to all, all to all relationships between the tables themselves.

Types of existing relationships:

![](images/ebook_image_205181_f2cc5449993836ce.jpg)

The tables are linked together through the keys which can be primary or secondary.

I remind you that the primary key must be unique and identify the individual instances of the entity we are considering.

I remind you that the primary key of a table can become the foreign key of another table with which the first has a relationship.

To create a database, first we start from the single tables that contain all the data we need and at a later time we will remove the duplicate fields in the various tables that must not be repeated in the Database because they can be retrieved through a simple database query.

An example of a relational database with relational tables, linked by primary keys and foreign keys, can be the salary of employees or the warehouse of products, and others in which there are data linked together by some fields identified as keys. For example, the employee master data table can be linked to the payslip table through the employee code or the Products table can be linked to the Invoices table and the Customers table and so on.

In this project the Databases will only be used to insert the images we have chosen on our site and to insert the News on the homepage, so they will be composed of non-relational tables with only primary keys. In particular we will have three tables: one for the images and the text of the News included in the homepage (index.php), one for the clothing collections and one for the login. In the image tables we will have only the primary key as the automatic ID and n as the number of images to insert, while in the News table we will have both the images with the variable n and the text relating to them. In the last login table we have the username and the encrypted password.

# Create and manage databases with phpMyAdmin

Databases can be created with various software including Office Application Access or other software of various kinds. Data can be inserted, selected, modified and deleted on the database. The language for querying relational databases is SQL.

To manage the databases we could download MySql from the web or download the packages that also include MySql, as for the web WAMP or XAMPP which we will explain better later. For now we specify that these two applications contain phpMyAdmin.

In our case they will be used to make our example site dynamic, varying the data based on the interactions with the user and in this regard we will use phpMyAdmin.

***I remind you that the Databases can also be used with WordPress.***

# Database Management

In this work we do not have to solve all the knots concerning the doubts on the databases, but we intend to give a smattering of the subject which is extremely useful for the purposes of the applied example.

To manage the databases we must use the MySql language. Queries are requests made to the database that work with clauses.

With the SELECT clause you select the records of the selected table of the Database:

$ query = "SELECT * FROM data WHERE id = 1";

In this case we will select all the columns because we have entered *.

The DELETE clause deletes the selected records:

$ query = "DELETE FROM data_news WHERE id2 = '$ i'";

The UPDATE clause updates the records with the data we want to insert:

$ query = "UPDATE data_news set id2 = '$ o' WHERE id = $ id";

All these clauses will be included in the management of our database.

# Client-side and server-side languages

When writing web pages you need to use both server-side and client-side languages. If the programmer does not foresee requests to the server connected to databases located on the server itself, then the client-side languages ​​will suffice, therefore in the case of websites (html and javascript). If, on the other hand, the site provides access to a server-side database and therefore accessible to all clients on the network, then it must be written in a server-side language such as PHP. An example is the creation of dynamic sites with CMS or e-commerce sites with the choice of online products.

# PHP

Php is a server-side programming language used to create dynamic web pages born in 1994\. It spread around the world with WordPress managing the CMS created in PHP. The PHP interpreter is distributed free of charge with a license.

Php is the most famous server side language which therefore serves to communicate with the external server.

The php code can be inserted into the html page directly or they can be saved separately with the php extension, but always identified by:

<? php

?>

The .php files must be included in the html page:

<? php

include ("view-slider-home.php");

?>

# The JavaScript

Javascript is a client-side programming language used for event-linked web page scripts. With javascript users can interact with the site transforming the site from static to dynamic. Examples of javascript are, the insertion of keys that perform actions chosen by the user. A translator with the user's choice of language could be a javascript program.

Javascript is read from top to bottom so it must be inserted in a specific part of the code. It is an example of interpreted code that differs from compiled code that is processed by a compiler that translates the programming language into machine language.

Even if javascript has been a client side language for several years now there is NodeJS that transforms javascript into server side language. This will certainly be a topic for the next book.

The javascript code can be embedded in the web page in html or be inserted in a separate js file and recalled only from the html page.

It can be inserted in the body of the page:

<script type = "text / javascript" src = "js / search.js"> </script>

It can be inserted in a specific part of the page like in the bootstrap:

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

I remind you that to be recognized as a javascript code you must insert the <script> </script> tags

# Example of creating a site

# Create the project

Our example site concerns a clothing store with three stores in which to insert photos of the collections present in the various shops. The example is not an e-commerce, but only has to display the photos of the collections.

Our goal in this example will be to insert images directly from the site with an encrypted password access via phpMysql, php and javascript.

First of all we need to establish how many pages the site must consist of and which ones they must be (home, who we are, services or products and contacts). We can also decide to create a single scrolling page (One page website) or several split pages. For today's habit of the user to scroll the social networks perhaps it would be better to create a "one page" website. If we then want to direct the user towards a specific action we will create a landing page (landing page) these are for example the pages directed by specific marketing campaigns.

In our example we have decided to create four main pages with direct access from the main menu with the addition of two pages for the two collections (man and woman) and three pages for the shops with access from submenus in the main navigation bar.

In this phase we can both write the main characteristics, which the various pages must have, and draw the graphics of the pages themselves on some sheets. You could also create a mockup (template) of the page graphics to understand what to change in the project.

# Use Notepad

We have already mentioned that all files for the web in html, javascript and php can be written easily with a simple notepad, the important thing is to save the file with the specific extension (.html, .php, etc.). Obviously in this case we must know very well the language we want to use, otherwise the file will not work. To overcome this problem we can use Notepad which, unlike a simple notepad, suggests us while we write the words contained in that language to avoid code writing errors.

![](images/ebook_image_205181_21fede7b73179a10.jpg)![](images/ebook_image_205181_1199a514666053f0.jpg)

# Create the pages

In this phase of the project we can choose whether to independently create the pages in html or use various types of resources from the internet such as the already created Bootstraps that we will have to modify according to our needs.

We have already explained previously the difficulties and time needed to create a CSS that is congruent with the specific needs required by the market today as dynamic and responsive sites. This is why in this work aimed at teaching and especially at the creation of a dynamic menu for inserting images, we have decided to use resources already available for free on the internet.

As we will see later in this first moment of page creation, we will write all the main pages in html code and as we progress in the work we will realize what usefulness to deepen with the javascript and php languages ​​and then save some pages in php because they contain code php.

# Change the layout of the pages

After creating the main pages we will dedicate ourselves to adapting the pages to the needs of the site we intend to create. In this phase we must understand what the site will have to do, how it will have to interact with the user and what information we want to enter and give to the user by selecting those that will be displayed statically from those that will be chosen by the user dynamically.

In this phase we realized that the collections of our example site had to be updated easily by a common user who owned the site who did not know the programming codes at all and who had to update the photos of the site.

This is where the need arose to create a menu with personal access for inserting images in the relative web pages via javascript and php. This is the goal of this study and will be explained in the next paragraphs.

# Choose images and colors

The images and colors chosen for a website can make the difference for a website as well as for any other design product. Web design was born for this reason, so if you want a professional level design you have to go to a professional. In case you want to do it all yourself, you can choose a bootstrap or a model already made and change something to customize it. And if you are a CSS expert you can create your site from scratch to your liking by also seeing some sites you like on the internet.

# Free and paid images

There are various sites on the internet to download free or paid images.

[https://www.pinterest.it/pxhere/](https://www.pinterest.it/pxhere/)

[https://pixabay.com/](https://pixabay.com/)

There are also various applications on the Google play store such as:

*   free images;

*   pixabay.

I recommend that you insert sliders and images relevant to the subject of the site and color them to attract attention, but avoiding disturbing colors.

The sliders are long images that slide to give movement to the site. These can be inserted by the CSS. In our example we have decided to insert the sliders.

# Images created specifically for the site

We can also create images ourselves through the means that the internet makes available to us to create or modify images such as:

*   Photoshop;

*   Gimp.

In this case we can take photos and modify them with these software and then insert them on our site.

***I remind you to be very careful about the resolution of the images to be inserted. The larger the files, the longer it will take to load the site. I also recommend that you save them with the save for web function.***

There are also some mobile applications, very useful for this purpose, such as:

*   Adobe Draw;

*   Picsart.

# Use XAMPP OR WAMP in Windows to manage websites locally

It is very useful for a programmer to test the functioning of the sites before they are published.

For this purpose we can use free software packages available on the internet such as WAMP or XAMPP. We can see these software as local web simulators.

XAMPP stands for cross-platform (multiplatform), apache, MySql and php and perl. Let's say that between XAMPP and WAMP there is not much difference. Apache is a local web server for testing the website project without going to the web. MySql is used to create and manage databases. To open MySql we need to install php.

We may not even use XAMPP or WAMP, but in this case we will not be able to interact with the databases and see the functioning of programs written in PHP and Javascript locally.

It follows that if we have not provided any type of interaction with the user on our site, we can easily view the pages with the chosen browser without downloading any type of simulator such as WAMP by simply clicking on the html pages.

XAMPP is cross-platform and also supports PERL, while WAMP only supports MySQL, PHP and Apache and only works on Windows.

***I remind you that WAMP is the Windows stack, but that there is also LAMP for Linux and the version for MAC which is called MAMP.***

# What is WAMP and how it works

In this work to test our example site we decided to use WAMP as a Windows stack. WAMP is the acronym that derives from Windows, Apache, Mysql and PHP. The software package is called WampServer and is free.

# Download and install WAMP

After searching the internet for WAMP, the package will be installed. There are various sites from which you can download WAMP for free.

At the end of the installation, the wamp folder will appear in the C: folder of our computer.

Wamp will also install other software useful in programming such as Notepad.

# Use WAMP

After installing the WAMP software we will have the following folder in C:

![](images/ebook_image_205181_6175e09d1dc215a6.jpg)

To enter the simulator we have to click wampmanager.exe, while if we want to create a site or transfer the folders of a site already created in WAMP, click on the www folder and import the site files we need.

![](images/ebook_image_205181_e6fc015ae0d97639.jpg)![](images/ebook_image_205181_d710df81cc9a3197.jpg)![](images/ebook_image_205181_d0e811503d70f5eb.jpg)![](images/ebook_image_205181_28ba7a45f6e23cf7.jpg)![](images/ebook_image_205181_245db4447a20391b.jpg)![](images/ebook_image_205181_cb2996b096641c14.jpg)

To enter the WAMP menu, click on wampmanager.exe in the wamp folder or by clicking on the W icon on the desktop.

![](images/ebook_image_205181_e4a69be38f5d9de1.jpg)![](images/ebook_image_205181_a9659a5396d9b1e2.jpg)![](images/ebook_image_205181_fa0fae3622b1f6d7.jpg)![](images/ebook_image_205181_6eddc5c3a9e4d5ba.jpg)![](images/ebook_image_205181_63132a94f90e5d1e.jpg)

***I remind you that WAMP can also be used with wordPress by copying the wordpress folder in the www folder of wamp and installing it directly after creating a database from wamp in phpMyAdmin that we will insert in the WordPress configuration.***

# phpMyAdmin and MySQL

Using databases is not easy, first of all we have to choose whether to create the site directly on the web or test it on a local web simulator which we will then bring back to the web. However, even if we decide to test the site on our PC, we still have to create the same databases on the hosting that we bought or got for free. Each hosting with a link to a website will contain a database management software such as phpMyAdmin.

***I remind you that the database data will be re-entered into the software linked to the address of your website, while the pages and the various files in php can be uploaded directly from the hosting.***

The Databases of our project are constructed as follows:

*   Data table;

*   Data_news table;

*   Login table.

The first table contains the data useful for uploading the images of the collections and sliders. The second contains the useful data for uploading the news and the third contains the useful data for the login (username and password).

![](images/ebook_image_205181_59b631724902e444.jpg)![](images/ebook_image_205181_d8953d8ad807b49b.jpg)![](images/ebook_image_205181_63fc81fe253650a4.jpg)

In fields:

*   n the number of images in the women's collection will be saved;

*   n2 will be the number of images in the men's collection;

*   N3 will be the number of sliders on the home, shop 1, shop 2 and shop 3 pages.

![](images/ebook_image_205181_301fd016309dbeb6.jpg)

In this table we will have the news field containing all the news inserted in the homepage of our site that we can delete and modify as well as we can insert new ones through the control panel.

![](images/ebook_image_205181_a84c7d362c6d3ae2.jpg)

***I remind you that for greater security we have entered the password in SHA1 code.***

In particular, we went to the site to encrypt and decrypt passwords:

[https://www.online-toolz.com/tools/sha1-generator.php](https://www.online-toolz.com/tools/sha1-generator.php)

We have selected the SHA1 code and copied this code into the database. Subsequently, it is advisable to save the original password in a data file that you will need to access the Databases.

***I remind you that to access the login you will enter the original username and password that our php code will encrypt and check with the SHA1 code entered in the database.***

# Login and menu for inserting images and news

We will access the control panel from the login page available at the top of the pages of our site identified with the image of the little man and the word Login.

![](images/ebook_image_205181_a9f821d4ec6f19c1.jpg)![](images/ebook_image_205181_14343614c654d182.jpg)![](images/ebook_image_205181_4cb2259da9f09fb0.jpg)![](images/ebook_image_205181_ee163627126ece80.jpg)![](images/ebook_image_205181_4e854029cc75be15.jpg)![](images/ebook_image_205181_e97b2e3a60a79663.jpg)![](images/ebook_image_205181_d3a4ce17daf9e2e2.jpg)![](images/ebook_image_205181_1f0cfa3cec2db12c.jpg)![](images/ebook_image_205181_18d358ee3f1e66f8.jpg)![](images/ebook_image_205181_63fbd57d42114ff9.jpg)

Even if the message reports a format error, the procedure will still upload the photo to the men's collection page.

![](images/ebook_image_205181_caaef77e956118f9.jpg)

For the news the speech is a little different as we will insert the image and the written News that we can modify or delete in the future. In this case we will also insert the written news in the Database.

![](images/ebook_image_205181_1835e6c869328670.jpg)![](images/ebook_image_205181_b5a31bd33e4c80bf.jpg)

# Example site pages and scripts

For this school example for educational use we have used various programs in php useful for our purposes that can be downloaded for free from the internet and that we have included in this book for educational purposes only. Obviously some resources have been modified to be adapted to the usefulness of the example site included in this book.

In the WAMP WWW folder we will have the folder containing all the archives and files that we will later upload to the hosting provider that will host the site. Remember to also create the Databases directly in the hosting as we will describe later.

Our example site folder we created contains the following files and subfolders:

![](images/ebook_image_205181_e5af83ae2855b69a.jpg)

The files for the site pages are divided into files.html and files. php based on database usage or not.

**I remind you that the pages that contain php files must be saved in php and not in html otherwise they do not work, in fact we will have pages saved in html and pages saved in php depending on whether they are used or not in the databases.**

# Site pages in html

***Below are the files saved in html for some pages not containing php code, which as we have already said will be saved in php.***

***For ease of reading we have entered the file name as a note. I remind you that in html the note must be included between <! - note -!>. if you forget the exclamation marks or hyphens it will be read as a tag.***

<! DOCTYPE html>

<html lang = "en">

<! - file name: who_we are.html ->

<head>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li class = "active"> <a href='#'> About us </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "wrap-clear"> </div>

<div class = "container">

<div> </div>

<br>

<br>

<div class = "testimonial-image wow fadeInUp">

<div class = ''>

<div class = 'row'>

<h6>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

</div>

</h6>

</div>

</div>

<br>

<div class = "testimonial-image wow fadeInUp">

<h4> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h4>

</div>

</div>

</div>

<div class = "container">

<div class = "col-sm-2 about-us-text wow fadeInLeft" style = "text-align: justify">

</div>

<div class = "col-sm-8 about-us-text wow fadeInLeft" style = "text-align: justify">

<p>

<br>

Our company is a leader in the manufacturing of men's and women's clothes for all ages that combines practicality with elegance and high quality at an excellent price. Our motto is low cost elegance for all ages and all sizes.

</p>

<br> <br> <H2 style = "text-align: CENTER">

WE SEARCH FOR YOU THE BEST DRESSES AT THE BEST PRICE FOR EVERY OCCASION </H2>

<br>

<br>

</div> </div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> NEGOZIO 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </ span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </ span> Phone: 0039 </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: 0039 </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - NEGOZIO 1 SRL - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "en">

<! - file name: contacts.html ->

<head>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li class = "active"> <a href='#'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "container">

<div> </div>

<br>

<br>

<div class = "testimonial-image wow fadeInUp">

<div class = ''>

<div class = 'row'>

<h6>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

</div>

</h6>

</div>

</div>

<br>

<div class = "testimonial-image wow fadeInUp">

<h4> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h4>

</div>

</div>

<! - Page Title ->

<div class = "page-title-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-10 col-sm-offset-1 page-title wow fadeIn">

<span aria-hidden = "true" class = "icon_mail"> </span>

<h1> Contact us / </h1>

<p> How to contact us </p>

</div>

</div>

</div>

</div>

<! - Contact Us ->

<div class = "contact-us-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-7 contact-form wow fadeInLeft">

<p>

</p>

<form role = "form" action = "contact.php" method = "post">

<input type = "hidden "name =" to "value =" @ gmail.com "id =" to "/>

<input type = "hidden" name = "subject" id = "subject" value = "[information request]" />

<input type = "hidden" value = "" name = "flaginvia" ID = "flaginvia" />

<div class = "form-group">

<label for = "contact-surname"> Surname * </label>

<input type = "text" name = "surname" placeholder = "Enter the surname ..." class = "contact-name form-control" id = "contact-surname">

</div>

<div class = "form-group">

<label for = "contact-name"> Name * </label>

<input type = "text" name = "name" placeholder = "Enter the name ..." class = "contact-name form-control" id = "contact-name">

</div>

<div class = "form-group">

<label for = "contact-subject"> Phone </label>

<input type = "text" name = "phone" placeholder = "Enter the phone number ..." class = "contact-subject form-control" id = "contact-phone">

</div>

<div class = "form-group">

<label for = "contact-email"> Email * </label>

<input type = "text" name = "email" placeholder = "Enter the email address ..." class = "contact-email form-control" id = "contact-email">

</div>

<div class = "form-group">

<label for = "contact-message"> Message * </label>

<textarea name = "message" placeholder = "Enter the message ..." class = "contact-message form-control" id = "contact-message"> </textarea>

</div>

<div class = "form-group">

<textarea cols = "65" rows = "6" readonly wrap = "VIRTUAL" class = "contact-name form-control">

Dear Customer,

we wish to inform you that the Legislative Decree n.196 of 30.6.2003 ("Code regarding the protection of personal data") establishes that "Anyone has the right to the protection of personal data concerning him".

In compliance with the law, NEGOZIO 1 Srl will treat all your data according to the principles of correctness, lawfulness, transparency and protection of your privacy and your rights.

Pursuant to and for the purposes of Article 13 of Legislative Decree 196/2003, therefore, we provide you with the following information regarding your data:

TYPE OF DATA: personal data and identification data (as defined in art.4).

METHOD: organization of archives on paper and in a mainly automated form (in accordance with Article 11).

NATURE: mandatory (data you provided for the aforementioned purposes) and optional (data you provided for other purposes not included in the previous list - for example e-mail - which will be used to send information material relating to the activities of STORE 1 Srl

REFUSAL TO PROVIDE DATA

Any refusal to provide personal data of a mandatory nature, as defined above, will make it impossible to accept the application for registration or the inclusion of the curriculum in the bulletin board. Any refusal to provide personal data of an optional nature, as defined above, does not entail any consequences in relation to the acceptance of the application for registration.

DISSEMINATION: no external dissemination will be made to NEGOZIO 1 Srl.

DATA CONTROLLER: NEGOZIO 1 Srl

RESPONSIBLE FOR TREATMENT: NEGOZIO 1 Srl

Finally, we remind you that you will be able to exercise all your rights pursuant to Legislative Decree 196/2003 and, in particular, request the owner to access, modify and update or delete your data. Furthermore, we remind you that, in the event of your refusal to consent to mandatory data, we will not be able to perform the tasks requested by you.

The person in charge of the treatment

SHOP 1 SRL

</textarea>

</div>

<div class = "form-group">

<label for = "contact-message"> I authorize * </label>

<input name = "privacy" value = "yes" type = "checkbox" ID = "checkbox" />

</div>

<button type = "submit" class = "btn"> Submit </button>

<br>

<br>

<div>

(*) mandatory data

</div>

</form>

</div>

</div>

</div>

</div>

<! - End graphics ->

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - NEGOZIO 1 SRL - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "en">

<! - file name: privacy.html ->

<head>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "about-us-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-12 about-us-text wow fadeInLeft" style = "text-align: justify">

<h3> D. Lgs 196/2003 </h3>

<br>

<br>

<td class = "textblack"> The Legislative Decree 196/2003, called "Code regarding the protection of personal data", brings together in a single context the Law 675/1996 and the other legislative decrees, regulations and ethical codes have happened in recent years in terms of the processing of personal data. <br>

Legislative Decree 196/2003 dictates a series of prescriptions aimed at ensuring that the processing of personal data is carried out in compliance with the rights, fundamental freedoms and dignity of individuals, with particular reference to confidentiality and personal identity. Likewise, the Decree guarantees the rights of legal persons and of any other body or association. <br>

Safeguarding the confidentiality of the personal data of our interlocutors is our primary commitment.

<br> <br>

This information is provided pursuant to art. 13 of Legislative Decree 196/2003 regarding the data provided by all those who interact with web services accessible electronically starting from the address http: //www.STORE 1.it

<br> <br>

1\. The information is provided only for the NEGOZIO 1 SRL site and not for other websites that may be consulted by the user via links.

<br> <br>

2\. Your personal data are processed by NEGOZIO 1 SRL and used for the purposes and in the manner indicated by specific information contained or displayed on the pages of the site for particular services or requests.

<br> <br>

3\. The provision of your personal data is optional, but failure to provide it has the consequence of not allowing the undersigned to provide the requested services.

<br> <br>

4\. Your personal data may also be disclosed to companies controlled and connected to NEGOZIO 1 SRL for the purposes highlighted from time to time in the specific information.

The data will in no case be disclosed.

<br> <br>

5\. Your personal data are processed with automated tools for the time strictly necessary to achieve the purposes for which they were collected.

<br> <br>

6\. Your personal data are processed in compliance with the security measures imposed by Legislative Decree 196/2003 in order to prevent data loss, illicit or unauthorized use, or unauthorized access.

<br> <br>

7\. We inform you that, in relation to your personal data, you are entitled to the rights referred to in Article 7 of the aforementioned Legislative Decree and, in particular, the right to access your personal data, to request its correction, the updating and cancellation, if incomplete, erroneous or collected in violation of the law, as well as to oppose their treatment for legitimate reasons.

<br> <br>

8\. The data controller is NEGOZIO 1 SRL.

<br> <br>

9\. To exercise the above rights or for further information on the subject, please contact us at the following email address: <a href="mailto:STORE 1@gmail.com "class="linkwhite"> STORE 1 @ gmail .com </a> </div>

<br>

<br>

This approach allows you to change the classic view of the contract

for the benefit of a real partnership oriented towards sharing

of the objectives and the guarantee of the result. </div> </td>

</div>

</div>

</div>

</div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE- <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "en">

<! - file name: services.html ->

<head>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li class = "active"> <a href='#'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "wrap-clear"> </div>

<div class = "wrapper">

<div class = "testimonial-image wow fadeInUp">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<div class = ''>

<div class = 'row'>

<h6>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

</div>

</h6>

</div>

</div>

<br>

<div class = "testimonial-image wow fadeInUp">

<h4> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h4>

</div>

</div>

<div class = "page-title-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-10 col-sm-offset-1 page-title wow fadeIn">

<span aria-hidden = "true" class = "icon_group"> </span>

<h1> Services offered </h1>

<p> </p>

</div>

</div>

</div>

</div>

<div class = "about-us-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-4">

<div class = "work wow fadeInUp">

<img src = "img / link / sale.jpg" alt = "" data-at2x = "img / link / sale.jpg">

<div class = "testimonial-text">

<h3> Assisted sales </h3>

<p> </p>

<br>

</div>

</div>

</div>

<div class = "col-sm-4">

<div class = "work wow fadeInUp">

<img src = "img / link / sartoria1.jpg" alt = "" data-at2x = "img / link / sartoria1.jpg" width = "60%">

<div class = "testimonial-text">

<h3> Ability to make tailoring changes </h3>

<p> </p>

<br>

</div>

</div>

</div>

<div class = "col-sm-4">

<div class = "work wow fadeInUp">

<a class="testimonial-image" href="http://www.paginegialle.it/ -ba/abbigliamento/STORE 1">

<img src = "img / link / taglie1.png" alt = "" data-at2x = "img / link / taglie1.png" width = "">

</a>

<div class = "testimonial-text">

<h3> Comfortable sizes for men and women </h3>

<p> </p>

<br>

</div>

</div>

</div>

</div>

</div>

</div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "en">

<! - file name: webcredits.html ->

<head>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='#'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "about-us-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-12 about-us-text wow fadeInLeft" style = "text-align: justify">

<h3> </h3>

<br>

<br>

<td class = "col-sm-12 about-us-text wow fadeInLeft" style = "text-align: justify"> <P>

All images on all pages of this website are protected by copyright and e & grave; Even partial reproduction of images and contents is prohibited.

<BR>

<BR>

The site is; was made by:

<BR> <a href="http://xxxxx.org/"> Example </a>. </p>

</div>

</td>

</div>

</div>

</div>

</div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 2 <br>

<br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

# Html pages saved in php as they include php code in them

Below we insert the pages saved in php because they include some php code. If they are saved in html the code will not work.

<! DOCTYPE html>

<html lang = "it">

<! - file name: index.php ->

<head>

<meta http-equiv = "Content-Type" content = "text / html; charset = utf-8" />

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, cheaters, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries ->

<! - WARNING: Respond.js doesn't work if you view the page via file: // ->

<! - [if lt IE 9]>

<script src = "https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"> </script>

<script src = "https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"> </script>

<! [endif] ->

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li class = "active"> <a href='#'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'man_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div>

<! - Slider ->

<div class = "slider-container">

<div class = "slider">

<div class = "flexslider">

<ul class = "slides">

<? php

include ("view-slider-home.php");

?>

</ul>

</div>

</div>

</div>

<div class = "wrap-clear"> </div>

<div class = "container">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<h1> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h1>

</div>

<div class = "testimonial-image wow fadeInUp">

</div>

</div>

<div class = "testimonials-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-12 testimonials-title wow fadeIn" style = "text-align: center;"> <h2>

<a class="big-link-2"style="text-align:center;"> <span class = "icon_document"> </span> </a> News </h2>

</div>

</div>

<div class = "row">

<div class = "col-sm-10 testimonial-list wow fadeInLeft">

<div role = "tabpanel">

<! - Tab panes ->

<div class = 'tab-content'>

<? php

include ("visnews.php");

?>

<! -

<div role = "tabpanel" class = "tab-pane fade" id = "tab2">

<div class = "testimonial-image">

<img src = "img / brochure / img9.png" alt = "" data-at2x = "img / brochure / img9.png">

</div>

<div class = "testimonial-text">

<p>

<br>

<a href="#"> </a>

</p>

</div>

</div>

<div role = "tabpanel" class = "tab-pane fade" id = "tab3">

<div class = "testimonial-image">

<img src = "img / brochure / img12.png" alt = "" data-at2x = "img / brochure / img12.png">

</div>

<div class = "testimonial-text">

<p>

<br>

<a href="#"> </a>

</p>

</div>

</div>

<div role = "tabpanel" class = "tab-pane fade" id = "tab4">

<div class = "testimonial-image">

<img src = "img / brochure / img15.png" alt = "" data-at2x = "img / brochure / img15.png">

</div>

<div class = "testimonial-text">

<p>

<br>

<a href="#"> </a>

</p>

</div>

</div> ->

</div>

<! - Nav tabs ->

<ul class = "nav nav-tabs" role = "tablist">

<? php

include ("tabnews.php");

?>

<! -

<li role = "presentation" class = "active">

<a href="#tab1" aria-controls="tab1" role="tab" data-toggle="tab"> </a>

</li>

<li role = "presentation">

<a href="#tab2" aria-controls="tab2" role="tab" data-toggle="tab"> </a>

</li>

<li role = "presentation">

<a href="#tab3" aria-controls="tab3" role="tab" data-toggle="tab"> </a>

</li>

<li role = "presentation">

<a href="#tab4" aria-controls="tab4" role="tab" data-toggle="tab"> </a>

</li>

->

</ul>

</div>

</div>

<div class = "col-sm-2 testimonial-icon wow fadeInUp">

<div>

<span aria-hidden = "true" class = "icon_pushpin"> </span>

</div>

</div>

</div>

</div>

</div>

<div> <p> STORE 1 - Clothing and formal wear - P.IVA <a href="https://www.facebook.com/STORE 1-Bari-1510212975727828/" target="_blank"> <img src = "images / facebook.png"> </a> </p> </div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creativity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: 0039 </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: 0039 </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE- <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "en">

<! - file name: login.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<! - END PHOT GALLERY: PRETTY PHOTO ->

</head>

<body>

<! - HEADER ->

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<! - FINE HEADER ->

<! - CONTENTS ->

<div class = "wrap-clear"> </div>

<div class = "wrapper">

<div class = "testimonial-image wow fadeInUp">

<div class = ''>

<div class = 'row'>

<h6>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

</div>

</h6>

</div>

</div>

<br>

<div class = "testimonial-image wow fadeInUp">

<h4> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h4>

</div>

</div>

<br>

<br>

<div>

<form id = "login" action = "verification.php" method = "post">

<fieldset id = "inputs">

<input id = "username" name = "username" type = "text" placeholder = "Username" autofocus required>

<input id = "password" name = "password" type = "password" placeholder = "Password" required>

</fieldset>

<br>

<fieldset id = "actions">

<input type = "submit" id = "submit" value = "Connect">

</fieldset>

<br>

</form>

</div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Our company is a leader in the manufacturing of men's and women's clothes for all ages that combines practicality with elegance and high quality at an excellent price. Our motto is low cost elegance for all ages and all sizes.

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2022 - NEGOZIO 1 Srl - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<! - file name: woman_collection.php ->

<html lang = "it">

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<! - END PHOT GALLERY: PRETTY PHOTO ->

<script> window.twttr = (function (d, s, id) {

var js, fjs = d.getElementsByTagName (s) [0],

t = window.twttr || {};

if (d.getElementById (id)) return t;

js = d.createElement (s);

js.id = id;

js.src = "https://platform.twitter.com/widgets.js";

fjs.parentNode.insertBefore (js, fjs);

t._e = [];

t.ready = function (f) {

t._e.push (f);

};

return t;

} (document, "script", "twitter-wjs")); </script>

</head>

<body>

<! - HEADER ->

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li class = "active"> <a href='#'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "wrap-clear"> </div>

<div class = "wrap-clear"> </div>

<div class = "container">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<div class = ''>

<div class = 'row'>

<h6>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

</div>

</h6>

</div>

</div>

<br>

<div class = "testimonial-image wow fadeInUp">

<h4> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h4>

</div>

</div>

<script>

/ *

(document) .ready (function () {

$ (document) .bind ('contextmenu', function (e) {

return false;

});

});

* /

</script>

<! - FINE HEADER ->

<! - CONTENTS ->

<div align = "center">

<div class = "container-clothes">

<div class = "row">

<ul id = "grid">

<? php

includes ("dresses-woman.php");

?>

</ul>

</div>

</div>

</div>

<div class = "container" align = "center">

<div class = "col-sm-2 about-us-text wow fadeInLeft" style = "text-align: justify">

</div>

<div class = "col-sm-8 about-us-text wow fadeInLeft" style = "text-align: justify">

<p> <br />

Our company is a leader in the manufacturing of men's and women's clothes for all ages that combines practicality with elegance and high quality at an excellent price. Our motto is low cost elegance for all ages and all sizes.

<br />

<br /> </p>

</div>

</div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "it">

<! - file name: man_collection.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<! - END PHOT GALLERY: PRETTY PHOTO ->

<script> window.twttr = (function (d, s, id) {

var js, fjs = d.getElementsByTagName (s) [0],

t = window.twttr || {};

if (d.getElementById (id)) return t;

js = d.createElement (s);

js.id = id;

js.src = "https://platform.twitter.com/widgets.js";

fjs.parentNode.insertBefore (js, fjs);

t._e = [];

t.ready = function (f) {

t._e.push (f);

};

return t;

} (document, "script", "twitter-wjs")); </script>

</head>

<body>

<! - HEADER ->

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li class = "active"> <a href='#'> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div class = "wrap-clear"> </div>

<div class = "wrap-clear"> </div>

<div class = "container">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<div class = ''>

<div class = 'row'>

<h6>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

</div>

</h6>

</div>

</div>

<br>

<div class = "testimonial-image wow fadeInUp">

<h4> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h4>

</div>

</div>

<script>

/ *

(document) .ready (function () {

$ (document) .bind ('contextmenu', function (e) {

return false;

});

});

* /

</script>

<! - FINE HEADER ->

<! - CONTENTS ->

<div align = "center">

<div class = "container-clothes">

<div class = "row">

<ul id = "grid">

<? php

includes ("man-suits.php");

?>

</ul>

</div>

</div>

</div>

<div class = "container" align = "center">

<div class = "col-sm-2 about-us-text wow fadeInLeft" style = "text-align: justify">

</div>

<div class = "col-sm-8 about-us-text wow fadeInLeft" style = "text-align: justify">

<p> <br />

Our company is a leader in the manufacturing of men's and women's clothes for all ages that combines practicality with elegance and high quality at an excellent price. Our motto is low cost elegance for all ages and all sizes.

<br />

<br /> </p>

</div>

</div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "it">

<! - file name: insert woman-dresses-photos.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - CEREMONY DRESSES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> SHOP 1 - CEREMONY DRESSES </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - Management </h1> <h1> WOMEN'S COLLECTION </h1>

</div>

</div>

<div>

<div align = "center">

<br>

<h5> Dress images from the women's_collection page </h5>

<! -

<p> enter in the space provided the number of photos of dresses you want to view on the "women's collection" page </p>

<script> var n = 0; </script>

<form method = get action = "numtot-dresses-woman.php">

<DIV id = "search-bar" class = "clearfix">

<input type = n name = n value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <input type = "submit" value = "submit" name = "send">

</DIV>

<form id = "login" action = "verification2.php" method = "post">

<input type = "submit" value = "insert number" name = "send">

</form>

->

</form>

<br>

<h4> insert photos from zipped archive (.ZIP) </h4>

<p> Remember that the single zip archive can be up to 2MB in size. If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-dresses-woman-archive.php" method = "post"> <input name = "userimage" type = "file" /> <br> < input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "woman-dresses.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send"> </ form>

<br>

<br>

<h4> insert single photos </h4>

<p> If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-dresses-woman.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "woman-dresses.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send"> </ form>

<br>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - file name: insert photo-suits-men.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - CEREMONY DRESSES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> SHOP 1 - CEREMONY DRESSES </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - Management </h1> <h1> MEN'S COLLECTION </h1>

</div>

</div>

<div align = "center">

<br>

<h5> Dress images from the men's_collection page </h5>

<! -

<p> enter in the space provided the number of photos of clothes you want to view on the "men's collection" page </p>

<script> var n2 = 0; </script>

<form method = get action = "numtot-man-suits.php">

<DIV id = "search-bar" class = "clearfix">

<input type = n2 name = n2 value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <input type = "submit" value = "submit" name = "send">

</DIV>

<form id = "login" action = "verification2.php" method = "post">

<input type = "submit" value = "insert number" name = "send">

</form>

->

</form>

<br>

<h4> insert photos from zipped archive (.ZIP) </h4>

<p> Remember that the single zip archive can be up to 2MB in size. If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-men's-suits-archive.php" method = "post"> <input name = "userimage" type = "file" /> <br> < input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "man-suits.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send"> </ form>

<br>

<br>

<h4> insert single photos </h4>

<p> If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-man-suits.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "man-suits.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send"> </ form>

<br>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - filename: insert photo-slider-home.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - Management </h1> <h1> HOME SLIDER MANAGEMENT </h1>

</div>

</div>

<div>

<div align = "center">

<br>

<h5> SLIDER images of the HOME page </h5>

<! -

<p> enter in the space provided the number of photos of accessories you want to view on the "HOME" page </p>

<script> var n3 = 0; </script>

<form method = get action = "numtot-accessories-woman.php">

<DIV id = "search-bar" class = "clearfix">

<input type = n3 name = n3 value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <input type = "submit" value = "submit" name = "send">

</DIV>

<form id = "login" action = "verification2.php" method = "post">

<input type = "submit" value = "insert number" name = "send">

</form>

->

</form>

<br>

<h4> insert photos from zipped archive (.ZIP) </h4>

<p> Remember that the single zip archive can be up to 2MB in size. If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-home-archive.php" method = "post"> <input name = "userimage" type = "file" /> <br> < input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-home.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send"> </form>

<br>

<br>

<br>

<h4> insert single photos </h4>

<p> If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-home.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-home.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send"> </form>

<br>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - filename: insert photo-slider-STORE 1.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - Management </h1> <h1> SLIDER MANAGEMENT STORE 1 </h1>

</div>

</div>

<div>

<div align = "center">

<br>

<h5> SLIDER images of the SHOP 1 page </h5>

<! -

<p> enter in the space provided the number of photos of accessories you want to view on the "SHOP 1" page </p>

<script> var n3 = 0; </script>

<form method = get action = "numtot-accessories-woman.php">

<DIV id = "search-bar" class = "clearfix">

<input type = n3 name = n3 value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <input type = "submit" value = "submit" name = "send">

</DIV>

<! -

<form id = "login" action = "verification2.php" method = "post">

<input type = "submit" value = "insert number" name = "send">

</form>

->

</form>

<br>

<h4> insert photos from zipped archive (.ZIP) </h4>

<p> Remember that the single zip archive can be up to 2MB in size. If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-STORE 1-archive.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-STORE 1.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send" > </form>

<br>

<br>

<br>

<h4> insert single photos </h4>

<p> If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-STORE 1.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-STORE 1.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send" > </form>

<br>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - filename: insert photo-slider-STORE 2.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - Management </h1> <h1> SLIDER MANAGEMENT STORE 2 </h1>

</div>

</div>

<div>

<div align = "center">

<br>

<h5> SLIDER images of the SHOP 2 page </h5>

<! -

<p> enter in the space provided the number of photos of accessories you want to view on the "SHOP 2" page </p>

<script> var n3 = 0; </script>

<form method = get action = "numtot-accessories-woman.php">

<DIV id = "search-bar" class = "clearfix">

<input type = n3 name = n3 value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <input type = "submit" value = "submit" name = "send">

</DIV>

<form id = "login" action = "verification2.php" method = "post">

<input type = "submit" value = "insert number" name = "send">

</form>

->

</form>

<br>

<h4> insert photos from zipped archive (.ZIP) </h4>

<p> Remember that the single zip archive can be up to 2MB in size. If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-STORE 2-archive.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-STORE 2.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send" > </form>

<br>

<br>

<br>

<h4> insert single photos </h4>

<p> If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-STORE 2.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-STORE 2.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send" > </form>

<br>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - filename: insert photo-slider-STORE 3.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1, sweaters, sweaters, trousers, shirts, jeans, belts, shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - Management </h1> <h1> SHOP 3 SLIDER MANAGEMENT </h1>

</div>

</div>

<div>

<div align = "center">

<br>

<h5> SLIDER images of the HOME page </h5>

<! -

<p> enter in the space provided the number of photos of accessories you want to view on the "SHOP 3" page </p>

<script> var n3 = 0; </script>

<form method = get action = "numtot-accessories-woman.php">

<DIV id = "search-bar" class = "clearfix">

<input type = n3 name = n3 value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <input type = "submit" value = "submit" name = "send">

</DIV>

<form id = "login" action = "verification2.php" method = "post">

<input type = "submit" value = "insert number" name = "send">

</form>

->

</form>

<br>

<h4> insert photos from zipped archive (.ZIP) </h4>

<p> Remember that the single zip archive can be up to 2MB in size. If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-STORE 3-archive.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-SHOP 3.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send" > </form>

<br>

<br>

<br>

<h4> insert single photos </h4>

<p> If you want to overwrite the photos, you should always use the same names like "1", "2", etc. also to recognize the photos on the page </p>

<form enctype = "multipart / form-data" action = "upload-fullscreen-slider-SHOP 3.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload photo" name = "send"> </form>

<form enctype = "multipart / form-data" action = "view-slider-SHOP 3.php" method = "post"> <br> <input type = "submit" value = "View photo" name = "send" > </form>

<br>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - filename: insert-news.php ->

<head>

<! -

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: portrait)" href = "ipad-portrait.css" type = " text / css "/>

<link rel = "stylesheet" media = "all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation: landscape)" href = "ipad-landscape.css" type = " text / css "/>

<link rel = "stylesheet" media = "screen and (color)" href = "pretty2.css" />

->

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "shop 1, suits, suits, ceremony, clothing, man, woman, elegant, fur, footwear, sizes, comfortable, sweaters, sweaters, trousers, shirts, jeans, belts, shoes">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<! -

<link rel = "stylesheet" media = "max-width: 1024px" href = "css / pretty2.css;" type = "text / css" />

->

<link rel = "stylesheet" href = "css / prettyPhoto.css" type = "text / css" media = "all" />

<link rel = "stylesheet" media = "all and (max-width: 1024px)" href = "css / pretty2.css;" type = "text / css" />

<! - CSS ->

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

<script src = "js / jquery-1.6.4.min.js" type = "text / javascript"> </script>

<! - PHOTO GALLERY: PRETTY PHOTO ->

<script src = "js / jquery.prettyPhoto.js" type = "text / javascript"> </script>

<script type = "text / javascript" charset = "utf-8">

$ (document) .ready (function () {

$ ("a [rel ^ = 'prettyPhoto']"). prettyPhoto ();

});

</script>

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<script type = "text / javascript" src = "numtot.js"> </script>

</head>

<body>

<br>

<div class = "container">

<div class = "col-sm-2">

<p> <img src = "img / user-login2.png" width = "80"> <br> </p>

<? php

// I open the session and ...

session_start ();

// Retrieve the data ...

$ username = $ _SESSION ['username'];

// let's make a printout!

echo "Hello". $ username;

?>

</div>

<div class = "col-sm-8" style = "background-color: powderblue; border: 1px solid # 333333; box-shadow: 10px 10px 5px # 888888; text-shadow: 2px 2px # f8f8f8">

<h1> Control Panel - NEWS Management </h1>

</div>

</div>

<div>

<h5> News of the Index page </h5>

<p> To avoid problems before carrying out any operation (insert-modify-delete) always view the news </p>

<form method = get action = "visualizzanews.php">

<DIV id = "search-bar" class = "clearfix">

<input type = "submit" value = "displays news" name = "send">

</DIV>

<br>

<h4> insert news images </h4>

<p> remember to insert a photo in resolution (340x340) with the names eg. "imgnews1.jpg", "imgnews2.jpg" and so on </p>

<div align = "center">

<form enctype = "multipart / form-data" action = "uploadnews1.php" method = "post"> <input name = "userimage" type = "file" /> <br> <input type = "submit" value = "Upload news images" name = "send"> </form>

<! - <form enctype = "multipart / form-data" action = "uploadnews2.php" method = "post"> <input name = "userimage" type = "file" /> <input type = "submit" value = "Upload news" name = "send"> </form>

->

</div>

<br>

<h4> post the news </h4>

<p> enter the news in the text box below </p>

<form method = get action = "uploadnews3.php">

<DIV id = "search-bar" class = "clearfix">

<textarea rows = "6" cols = "40" type = news name = news value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> </ textarea > <input type = "submit" value = "send" name = "send">

</form>

</DIV>

<br>

<h4> edit the news already; existing </h4> <p> <strong> by entering the number of the news and the new text in the boxes below </strong> </p>

<p> remember to always view news with the "view news" button before changing because the 'id' number may have changed </p>

<form method = get action = "uploadnews4.php">

<DIV id = "search-bar" class = "clearfix">

<input type = i name = i value = 0 size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> <br> <br>

<textarea rows = "6" cols = "40" type = news name = news value = "" size = "20" onfocus = if (this.value == this.defaultValue) this.value = ""> </ textarea >

<input type = "submit" value = "send" name = "send">

</DIV>

</form>

<br>

<h4> delete news </h4> <p> <strong> by entering the number of the news to be deleted in the box below </strong> </p>

<p> remember to always view news with the "view news" button before deleting any news because the 'id' number <br> may have changed as it auto-updates after each deletion </p>

<form method = get action = "uploadnews5.php">

<DIV id = "search-bar" class = "clearfix">

<input type = i name = i value = 0 size = "20" onfocus = if (this.value == this.defaultValue) this.value = "">

<input type = "submit" value = "send" name = "send"> </form>

</DIV>

</div>

</div>

<br>

<h4> To end the management click on end management </h4>

<form enctype = "multipart / form-data" action = "finegestione.php" method = "post"> <input type = "submit" value = "END OF MANAGEMENT" name = "send"> </form>

<br>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

<html>

<! DOCTYPE html>

<html lang = "it">

<! - file name: STORE 1.php ->

<head>

<meta http-equiv = "Content-Type" content = "text / html; charset = utf-8" />

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> STORE 1 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries ->

<! - WARNING: Respond.js doesn't work if you view the page via file: // ->

<! - [if lt IE 9]>

<script src = "https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"> </script>

<script src = "https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"> </script>

<! [endif] ->

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li class = "active"> <a href='#'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li> <a href='STORE 2.php'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div>

<! - Slider ->

<div class = "slider-container">

<div class = "slider">

<div class = "flexslider">

<ul class = "slides">

<? php

include ("view-slider-STORE 1.php");

?>

</ul>

</div>

</div>

</div>

<div class = "wrap-clear"> </div>

<div class = "container">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<h1> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h1>

</div>

<div class = "testimonial-image wow fadeInUp">

</div>

</div>

<div class = "testimonials-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-12 contact-address wow fadeInUp">

<h3> We are here </h3>

<div class = "map"> </div>

<h3> Address </h3>

<p> Via <br> </p>

<p> Phone: 0039 </p>

<p> Fax: </p>

<p> E-mail: STORE 1@gmail.com </p>

<p> </p>

<br>

<h3> Opening hours </h3>

<p> Monday to Saturday 09: 00-13: 00/16: 00-20: 30 </p>

</div>

</div>

</div>

</div>

<div> <p> STORE 1 - Clothing and formal wear - P.IVA <a href="https://www.facebook.com/STORE 1- -1510212975727828/" target="_blank"> <img src = "images / facebook.png"> </a> </p> </div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> Via <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 2 <br> Via <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: 0039 </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "it">

<! - file name: STORE 2.php ->

<head>

<meta http-equiv = "Content-Type" content = "text / html; charset = utf-8" />

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> SHOP 2 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries ->

<! - WARNING: Respond.js doesn't work if you view the page via file: // ->

<! - [if lt IE 9]>

<script src = "https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"> </script>

<script src = "https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"> </script>

<! [endif] ->

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li> <a href='STORE 3.php'> STORE 3 </a> </li>

<li class = "active"> <a href='#'> STORE 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div>

<! - Slider ->

<div class = "slider-container">

<div class = "slider">

<div class = "flexslider">

<ul class = "slides">

<? php

include ("view-slider-STORE 2.php");

?>

</ul>

</div>

</div>

</div>

<div class = "wrap-clear"> </div>

<div class = "container">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<h1> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h1>

</div>

<div class = "testimonial-image wow fadeInUp">

</div>

</div>

<div class = "testimonials-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-12 contact-address wow fadeInUp">

<h3> We are here </h3>

<div class = "map"> </div>

<h3> Address </h3>

<p> Via <br> </p>

<p> Phone: </p>

<p> Fax: </p>

<p> E-mail: STORE 1@gmail.com </p>

<p> </p>

<br>

<h3> Opening hours </h3>

<p> Monday to Saturday 09: 00-13: 00/16: 00-20: 30 </p>

</div>

</div>

</div>

</div>

<div> <p> STORE 1 - Clothing and formal wear - P.IVA <a href="https://www.facebook.com/STORE 1- -1510212975727828/" target="_blank"> <img src = "images / facebook.png"> </a> </p> </div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Tradition and creactivity are combined with modernity and elegance.

NEGOZIO 1 Srl, a leading Italian company in men's and women's clothing

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - EXAMPLE - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts3.js"> </script>

</body>

</html>

<! DOCTYPE html>

<html lang = "it">

<! - file name: SHOP 3.php ->

<head>

<meta http-equiv = "Content-Type" content = "text / html; charset = utf-8" />

<meta http-equiv = Content-Type content = "text / html; charset = windows-1252">

<meta http-equiv = "X-UA-Compatible" content = "IE = edge">

<meta name = "viewport" content = "width = device-width, initial-scale = 1">

<meta name = "description" content = "SHOP 1 - MEN'S / WOMEN'S CLOTHES">

<meta name = "keywords" content = "SHOP 1, suits, dresses, ceremony, apparel, man, woman, elegant, fur, footwear, sizes, comfortable, SHOP 1,, sweaters, sweaters, trousers, shirts, jeans, belts , shoes ">

<meta name = "copyright" content = "Example">

<meta name = "author" content = "Example">

<title> SHOP 3 - MEN'S / WOMEN'S SUITS </title>

<! - CSS ->

<link href = "css / reset.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link href = "css / menu-style.css" rel = "stylesheet" type = "text / css" media = "screen" />

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Open+Sans:400italic,400">

<link rel = "stylesheet" href = "http://fonts.googleapis.com/css?family=Montserrat:700,400">

<link rel = "stylesheet" href = "bootstrap / css / bootstrap.min.css">

<link rel = "stylesheet" href = "elegant-font / code / style.css">

<link rel = "stylesheet" href = "css / animate.css">

<link rel = "stylesheet" href = "css / magnific-popup.css">

<link rel = "stylesheet" href = "flexslider / flexslider.css">

<link rel = "stylesheet" href = "css / form-elements.css">

<link rel = "stylesheet" href = "css / style.css">

<link rel = "stylesheet" href = "css / media-queries.css">

<! - HTML5 Shim and Respond.js IE8 support of HTML5 elements and media queries ->

<! - WARNING: Respond.js doesn't work if you view the page via file: // ->

<! - [if lt IE 9]>

<script src = "https://oss.maxcdn.com/libs/html5shiv/3.7.0/html5shiv.js"> </script>

<script src = "https://oss.maxcdn.com/libs/respond.js/1.4.2/respond.min.js"> </script>

<! [endif] ->

<! - Favicon and touch icons ->

<link rel = "shortcut icon" href = "ico / favicon.png">

<link rel = "apple-touch-icon-precomposed" sizes = "144x144" href = "ico / apple-touch-icon-144-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "114x114" href = "ico / apple-touch-icon-114-precomposed.png">

<link rel = "apple-touch-icon-precomposed" sizes = "72x72" href = "ico / apple-touch-icon-72-precomposed.png">

<link rel = "apple-touch-icon-precomposed" href = "ico / apple-touch-icon-57-precomposed.png">

<script type = "text / javascript" src = "js / search.js"> </script>

</head>

<body>

<div id = "first-line" class = "visible-desktop">

<div id = "top-line" class = "container">

<div class = "pull-right login">

<a href="login.html" class="login-lnk"> <img src = "img / user-login2.png" width = "30"> Login </a>

</div>

</div>

</div>

<! - Top menu ->

<nav class = "navbar" role = "navigation">

<div class = "container">

<div class = "navbar-header">

<button type = "button" class = "navbar-toggle collapsed" data-toggle = "collapse" data-target = "# top-navbar-1">

<span class = "sr-only"> Toggle navigation </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

<span class = "icon-bar"> </span>

</button>

<a class="navbar-brand" href="index.php"> </a>

</div>

<! - Collect the nav links, forms, and other content for toggling ->

<div class = "collapse navbar-collapse" id = "top-navbar-1">

<ul class = "nav navbar-nav navbar-right">

<li> <a href='index.php'> Home </a> </li>

<li> <a href='who_are.html'> Who we are </a> </li>

<li> <a href='servizi.html'> Our services </a> </li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

Gallery <b class = "caret"> </b> </a>

<ul class = "dropdown-menu">

<li> <a href='collezione_woman.php'> Women's collection </a> </li>

<li> <a href = 'men's_collection.php '> Men's collection </a> </li>

</ul>

</li>

<li class = "dropdown">

<a href="#" class="dropdown-toggle" data-toggle="dropdown">

<B class = "caret"> </b> </a> points of sale

<ul class = "dropdown-menu">

<li> <a href='STORE 1.php'> STORE 1 </a> </li>

<li class = "active"> <a href='STORE 3.php'> STORE 3 </a> </li>

<li><a href = 'SHOP 2.php'> SHOP 2 </a> </li>

</ul>

</li>

<li> <a href='contatti.html'> Contact us </a> </li>

</ul>

</ul>

</div>

</div>

</nav>

<div id = "google_translate_element"> </div> <script type = "text / javascript">

function googleTranslateElementInit () {

new google.translate.TranslateElement ({pageLanguage: 'it', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google_translate_element');

}

</script> <script type = "text / javascript" src = "// translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"> </script>

<div>

<! - Slider ->

<div class = "slider-container">

<div class = "slider">

<div class = "flexslider">

<ul class = "slides">

<? php

include ("view-slider-SHOP 3.php");

?>

</ul>

</div>

</div>

</div>

<div class = "wrap-clear"> </div>

<div class = "container">

<div class = "testimonial-image wow fadeInUp">

<br>

<br>

<h1> MEN'S - WOMEN'S CLOTHING <br>

CEREMONY DRESSES <br>

PLUS SIZES <br>

ACCESSORIES AND FOOTWEAR <br>

</h1>

</div>

<div class = "testimonial-image wow fadeInUp">

</div>

</div>

<div class = "testimonials-container">

<div class = "container">

<div class = "row">

<div class = "col-sm-12 contact-address wow fadeInUp">

<h3> We are here </h3>

<div class = "map"> </div>

<h3> Address </h3>

<p> Via <br> </p>

<p> Phone: </p>

<p> Fax: </p>

<p> E-mail: STORE 1@gmail.com </p>

<p> </p>

<br>

<h3> Opening hours </h3>

<p> Monday to Saturday 09: 00-13: 00/16: 00-20: 30 </p>

</div>

</div>

</div>

</div>

<div> <p> STORE 1 - Clothing and formal wear - P.IVA <a href="https://www.facebook.com/STORE 1- -1510212975727828/" target="_blank"> <img src = "images / facebook.png"> </a> </p> </div>

<! - Footer ->

<footer>

<div class = "container">

<div class = "row">

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> COMPANY </h4>

<div class = "footer-box-text">

<p>

Our company is a leader in the manufacturing of men's and women's clothes for all ages that combines practicality with elegance and high quality at an excellent price. Our motto is low cost elegance for all ages and all sizes.

</p>

<p> <a href="who_we are.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Privacy </h4>

<div class = "footer-box-text">

<p>

Legislative Decree 196/2003, called the Personal Data Protection Code, brings together Law 675/1996 and other legislative decrees in a single context ...

</p>

<p> <a href="privacy.html"> Learn more ... </a> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInUp">

<h4> THE SHOPS </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 1 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> SHOP 3 <br> <br> </p>

<p> <span aria-hidden = "true" class = "icon_pin"> </span> STORE 2 <br> <br> </p>

</div>

</div>

<div class = "col-sm-3 footer-box wow fadeInDown">

<h4> Contact us </h4>

<div class = "footer-box-text footer-box-text-contact">

<p> <span aria-hidden = "true" class = "icon_pin"> </span> Address: </p>

<p> <span aria-hidden = "true" class = "icon_phone"> </span> Phone: </p>

<p> <span aria-hidden = "true" class = "icon_profile"> </span> Fax: </p>

<p> <span aria-hidden = "true" class = "icon_mail"> </span> Email: <a href=" STORE 1@gmail.com "> STORE 1@gmail.com </a> </ p >

</div>

</div>

</div>

<div class = "row">

<div class = "col-sm-12 wow fadeIn">

<div class = "footer-border"> </div>

</div>

</div>

<div class = "row">

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Copyright 2017 - - <a href="webcredits.html"> Web Credits </a>. </p>

<script> document.write (document.lastModified) </script>

<div class = "col-sm-7 footer-copyright wow fadeIn">

<p> & copy; Gioia - All rights reserved. Template by <a href="http://azmind.com"> Azmind </a>. </p>

</div>

</div>

<div class = "col-sm-5 footer-social wow fadeIn">

<a href="#"> <span class = "social_facebook"> </span> </a>

<a href="#"> <span class = "social_dribbble"> </span> </a>

<a href="#"> <span class = "social_twitter"> </span> </a>

<a href="#"> <span class = "social_pinterest"> </span> </a>

</div>

</div>

</div>

</footer>

<! - Javascript ->

<script src = "js / jquery-1.11.1.min.js"> </script>

<script src = "bootstrap / js / bootstrap.min.js"> </script>

<script src = "js / bootstrap-hover-dropdown.min.js"> </script>

<script src = "js / wow.min.js"> </script>

<script src = "js / retina-1.1.0.min.js"> </script>

<script src = "js / jquery.magnific-popup.min.js"> </script>

<script src = "flexslider / jquery.flexslider-min.js"> </script>

<script src = "js / jflickrfeed.min.js"> </script>

<script src = "js / masonry.pkgd.min.js"> </script>

<script src = "http://maps.google.com/maps/api/js?sensor=true"> </script>

<script src = "js / jquery.ui.map.min.js"> </script>

<script src = "js / scripts3.js"> </script>

</body>

</html>

# Php file to be placed in the site folder

***Now let's insert the script of the server-side php files useful for database management:***

<? php

// filename woman-dresses.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n = $ line ['n'];

// echo "<div text-align = 'center'>"

$ dir = 'UPLOAD / fullscreen /';

$ files = scandir ($ dir);

foreach ($ files as $ fil)

{

$ filename = $ dir. "/". $ fil;

$ cont = $ cont + 1;

if ($ cont> 2) {

$ c = $ cont-2;

echo "<li> <a href='$filename' rel='prettyPhoto [] []] <img src = '$ filename' title = 'woman $ c' /> </a>";

echo "<p> woman $ c </p> </li>";

}

}

// echo "</div>"

?>

<? php

// file name men's-suits.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n2 = $ line ['n2'];

// echo "<div text-align = 'center'>"

$ dir = 'UPLOAD2 / fullscreen /';

$ files = scandir ($ dir);

foreach ($ files as $ fil)

{

$ filename = $ dir. "/". $ fil;

$ cont = $ cont + 1;

if ($ cont> 2) {

$ c = $ cont-2;

echo "<li> <a href='$filename' rel='prettyPhoto []]> <img width = '200' src = '$ filename' title = 'man $ c' /> </a>";

echo "<p> man $ c </p> </li>";

}

}

// echo "</div>"

?>

<? php

// filename: config.php

// general

$ website_internet = "";

$ date = (date ("dmy"));

$ vers = "2.0";

// URL FOR HTACCESS

// $ base_url = "http: // localhost / yoursite";

// DB connection

$ host = "localhost";

$ db_user = "root";

$ db_psw = "";

$ db_name = "mydb";

?>

<? php

// filename: connection_db.php

include ("config.php"); // include configuration file for variable retrieval

$ connection = mysql_connect ("$ host", "$ db_user", "$ db_psw");

if (! $ connection)

{

die ("Critical Database Connection Error". mysql_error ());

}

?>

<? php

<! - file name: contact.php ->

// Email address verification

function isEmail ($ email) {

return (preg_match ("/ ^ [-_. [: alnum:]] + @((([[: alnum:]] | [[: alnum:]] [[: alnum:] -] * [[: alnum:]]) \.) + (ad | ae | aero | af | ag | ai | al | am | an | ao | aq | ar | arpa | as | at | au | aw | az | ba | bb | bd | be | bf | bg | bh | bi | biz | bj | bm | bn | bo | br | bs | bt | bv | bw | by | bz | ca | cc | cd | cf | cg | ch | ci | ck | cl | cm | cn | co | com | coop | cr | cs | cu | cv | cx | cy | cz | de | dj | dk | dm | do | dz | ec | edu | ee | eg | eh | er | es | et | eu | fi | fj | fk | fm | fo | fr | ga | gb | gd | ge | gf | gh | gi | gl | gm | gn | gov | gp | gq | gr | gs | gt | gu | gw | gy | hk | hm | hn | hr | ht | hu | id | ie | il | in | info | int | io | iq | ir | is | it | jm | jo | jp | ke | kg | kh | ki | km | kn | kp | kr | kw | ky | kz | la | lb | lc | li | lk | ​​lr | ls | lt | lu | lv | ly | ma | mc | md | mg | mh | mil | mk | ml | mm | mn | mo | mp | mq | mr | ms | mt | mu | museum | mv | mw | mx | my | mz | na | name | nc | ne | net | nf | ng | ni | nl | no | np | nr | nt | nu | nz | om | org | pa | pe | pf | pg | ph | pk | pl | pm | pn | pr | pro | ps | pt | pw | py | qa | re | ro | ru | rw | sa | sb | sc | sd | se | sg | sh | si | sj | sk | sl | sm | sn | so | sr | st | su | sv | sy | sz | tc | td | tf | tg | th | tj | tk | tm | tn | to | tp | tr | tt | tv | tw | tz | ua | ug | uk | um | us | uy | uz | va | vc | ve | vg | vi | vn | vu | wf | ws | ye | yt | yu | za | zm | zw) $ | (([0-9] [0-9]? | [0-1] [0-9] [0- 9] | [2] [0-4] [0-9] | [2] [5] [0-5]) \.) {3} ([0-9] [0-9]? | [0-1] [0-9] [0-9] | [2] [0-4] [0-9] | [2] [5] [0-5])) $ / i ", $ email));

}

if ($ _ POST) {

// Enter the email where you want to receive the message

$ emailTo = '@ gmail.com';

$ clientName = addslashes (trim ($ _ POST ['name']));

$ clientSurname = addslashes (trim ($ _ POST ['surname']));

$ clientEmail = addslashes (trim ($ _ POST ['email']));

$ message = addslashes (trim ($ _ POST ['message']));

$ ClientPhone = addslashes (trim ($ _ POST ['phone']));

$ privacy = addslashes (trim ($ _ POST ['privacy']));

$ array = array ();

$ array ['nameMessage'] = '';

$ array ['surnameMessage'] = '';

$ array ['emailMessage'] = '';

$ array ['messageMessage'] = '';

$ array ['phoneMessage'] = '';

$ array ['privacyMessage'] = '';

if ($ clientSurname == '') {

$ array ['surnameMessage'] = 'Please enter your surname.';

}

if ($ clientName == '') {

$ array ['nameMessage'] = 'Please enter your name.';

}

if (! isEmail ($ clientEmail)) {

$ array ['emailMessage'] = 'Please insert a valid email address.';

}

if ($ message == '') {

$ array ['messageMessage'] = 'Please enter your message.';

}

$ content_mail = "Surname: $ clientSurname \ n \ n";

$ content_mail. = "Name: $ clientName \ n \ n";

$ content_mail. = "Phone: $ ClientPhone \ n \ n";

$ contents_mail. = "Privacy consent: $ privacy \ n \ n";

$ content_mail. = "Message: $ message \ n \ n";

if ($ clientSurname! = '' && $ clientName! = '' && isEmail ($ clientEmail) && $ message! = '') {

// Send email

$ headers = "From:". $ clientName. "<". $ clientEmail. ">". "\ r \ n". "Reply-To:". $ clientEmail;

mail ($ emailTo, $ subject. '(site information request)', $ contents_mail, $ headers);

}

echo json_encode ($ array);

}

?>

<? php

// file name: logout.php

session_start ();

$ _SESSION = array ();

session_destroy (); // destroy all sessions

// create a varibial with a message

$ msg = "Info: log out successful.";

// I encode it via urlencode info-logout-successful-

$ msg = urlencode ($ msg); // send the message via get

// return to index.php using GET I can retrieve and print the logout message on the screen

header ("location: index.php? msg = $ msg");

exit ();

?>

'; ?>

'; ?>

'; ?>

'; ?>

<? php

// filename: subscribe.php

// Email address verification

function isEmail ($ email) {

return (preg_match ("/ ^ [-_. [: alnum:]] + @((([[: alnum:]] | [[: alnum:]] [[: alnum:] -] * [[: alnum:]]) \.) + (ad | ae | aero | af | ag | ai | al | am | an | ao | aq | ar | arpa | as | at | au | aw | az | ba | bb | bd | be | bf | bg | bh | bi | biz | bj | bm | bn | bo | br | bs | bt | bv | bw | by | bz | ca | cc | cd | cf | cg | ch | ci | ck | cl | cm | cn | co | com | coop | cr | cs | cu | cv | cx | cy | cz | de | dj | dk | dm | do | dz | ec | edu | ee | eg | eh | er | es | et | eu | fi | fj | fk | fm | fo | fr | ga | gb | gd | ge | gf | gh | gi | gl | gm | gn | gov | gp | gq | gr | gs | gt | gu | gw | gy | hk | hm | hn | hr | ht | hu | id | ie | il | in | info | int | io | iq | ir | is | it | jm | jo | jp | ke | kg | kh | ki | km | kn | kp | kr | kw | ky | kz | la | lb | lc | li | lk | ​​lr | ls | lt | lu | lv | ly | ma | mc | md | mg | mh | mil | mk | ml | mm | mn | mo | mp | mq | mr | ms | mt | mu | museum | mv | mw | mx | my | mz | na | name | nc | ne | net | nf | ng | ni | nl | no | np | nr | nt | nu | nz | om | org | pa | pe | pf | pg | ph | pk | pl | pm | pn | pr | pro | ps | pt | pw | py | qa | re | ro | ru | rw | sa | sb | sc | sd | se | sg | sh | si | sj | sk | sl | sm | sn | so | sr | st | su | sv | sy | sz | tc | td | tf | tg | th | tj | tk | tm | tn | to | tp | tr | tt | tv | tw | tz | ua | ug | uk | um | us | uy | uz | va | vc | ve | vg | vi | vn | vu | wf | ws | ye | yt | yu | za | zm | zw) $ | (([0-9] [0-9]? | [0-1] [0-9] [0- 9] | [2] [0-4] [0-9] | [2] [5] [0-5]) \.) {3} ([0-9] [0-9]? | [0-1] [0-9] [0-9] | [2] [0-4] [0-9] | [2] [5] [0-5])) $ / i ", $ email));

}

if ($ _ POST) {

// Enter the email where you want to receive the notification when someone subscribes

$ emailTo = '@ gmail.com';

$ subscriber_email = addslashes (trim ($ _ POST ['email']));

if (! isEmail ($ subscriber_email)) {

$ array = array ();

$ array ['valid'] = 0;

$ array ['message'] = 'Insert a valid email address!';

echo json_encode ($ array);

}

else {

$ array = array ();

$ array ['valid'] = 1;

$ array ['message'] = 'Thanks for your subscription!';

echo json_encode ($ array);

// Send email

$ subject = 'New Subscriber (joy)!';

$ body = "You have a new subscriber! \ n \ nEmail:". $ subscriber_email;

// uncomment this to set the From and Reply-To emails, then pass the $ headers variable to the "mail" function below

// $ headers = "From:". $ subscriber_email. "<". $ subscriber_email. ">". "\ r \ n". "Reply-To:". $ subscriber_email;

mail ($ emailTo, $ subject, $ body);

}

}

?>

<? php

// filename: tabnews.php

$ i = 0;

$ u = $ i + 1;

if ($ number <1) {

print "<center> <p> Your search did not return any results </p> </center>";

} else {

while ($ number> $ i) {

if ($ u == 1) {"<li role = 'presentation' class = 'active'> <a href = '# tab $ u' aria-controls = 'tab $ u' role = 'tab' data-toggle = 'tab'> </a>

</li> ";

} {

echo "<li role = 'presentation'> <a href='#tab$u' aria-controls='tab$u' role='tab' data-toggle='tab'> </a>

</li> ";

}

$ i ++;

$ u = $ i + 1;

}

}

?>

<? php

// filename: upload-fullscreen-women's-dresses.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: upload-fullscreen-women's-dresses-archive.php

// Various settings to be changed at will

$ max_size = '10000000000000'; // Maximum size of photos

$ upload_dir = 'UPLOAD / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF", "zip", "ZIP"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

$ name = '';

$ filen = '';

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

print $ file;

print $ upload_dir;

require_once ('pclzip.lib.php');

// $ filename = "backup.zip"; // enter the exact path and name of the .zip file

$ archive = new PclZip ($ upload_dir. '/'. $ file);

if ($ archive-> extract (PCLZIP_OPT_PATH, $ upload_dir,

PCLZIP_OPT_REMOVE_PATH, 'install / release') == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Extract files successfully";

if (unlink ($ upload_dir. '/'. $ file)) {

echo 'the file was deleted';

} else {

echo 'the file was NOT deleted';

}

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

/ *

// Create .zip file of a specific folder

$ path = getcwd (). '/'; // path of the server folder (Indicate the path of the folder that contains the files to be compressed)

$ filename = $ newname; // name of the archive .zip file

$ x = 0;

if ($ handle = opendir ($ path)) {

while (false! == ($ arrayfile = readdir ($ handle))) {

if ($ arrayfile! = '.' and $ arrayfile! = '..') {

$ array_all_file [$ x] = $ path. $ arrayfile; // list of files and folders

$ x ++;

}

}

closedir ($ handle);

}

// fundamental call of the PclZip library

require_once ('pclzip.lib.php');

$ archive = new PclZip ($ filename);

// A list of filenames to be compressed

$ listOfFilesToCompress = implode (",", $ array_all_file);

// I add the files to the archive

$ v_list = $ archive-> create ($ listOfFilesToCompress);

if ($ v_list == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Archive created successfully.";

* /

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

$ filename = $ upload_dir. '/'. $ newname;

print $ thatsAll;

// print $ filename;

} else print $ wrongUp;

}

/ *

// $ archive = new PclZip ("archive.zip");

require_once ('pclzip.lib.php');

$ archive = new PclZip ("C: / wamp / www / STORE 1 woman-man-footwear-accessories - Last / UPLOAD / fullscreen / fullscreen.zip");

$ list = $ archive-> extract (PCLZIP_OPT_EXTRACT_DIR_RESTRICTION, './base_dir');

if ($ list == 0) {

die ("ERROR: '". $ archive-> errorInfo (true). "'");

}

* /

// unzip the zip file

// fundamental call of the PclZip library

/ *

function unzip ($ location, $ newLocation) {

if (exec ("unzip $ location", $ arr)) {

mkdir ($ newLocation);

for ($ i = 1; $ i <count ($ arr); $ i ++) {

$ file = trim (preg_replace ("~ inflating: ~", "", $ arr [$ i]));

copy ($ location. '/'. $ file, $ newLocation. '/'. $ file);

unlink ($ location. '/'. $ file);

}

return TRUE;

} else {

return FALSE;

}

}

if (unzip ($ filename, $ upload_dir))

echo 'Successful!';

else

echo 'Error';

$ archive = new ZipArchive ();

$ filename = $ filename;

if ($ archive-> open ($ filename)! == TRUE)

{

@exit ("Unable to open <$ filename> \ n");

}

echo "<pre>";

print_r ($ archive);

var_dump ($ archive);

echo "</pre>";

echo "The archive". $ filename. "contains the following files: \ n <br>";

echo "<pre>";

for ($ j = 0; $ j <$ archive-> numFiles; $ j ++)

{

print_r ($ archive-> statIndex ($ j));

}

echo "</pre>";

$ archive-> extractTo ('./ folder /');

$ archive-> close ();

* /

?>

<? php

// filename: upload-fullscreen-men's-suits.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD2 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: upload-fullscreen-men's-suits-archive.php

// Various settings to be changed at will

$ max_size = '10000000000000'; // Maximum size of photos

$ upload_dir = 'UPLOAD2 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF", "zip", "ZIP"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

$ name = '';

$ filen = '';

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

print $ file;

print $ upload_dir;

require_once ('pclzip.lib.php');

// $ filename = "backup.zip"; // enter the exact path and name of the .zip file

$ archive = new PclZip ($ upload_dir. '/'. $ file);

if ($ archive-> extract (PCLZIP_OPT_PATH, $ upload_dir,

PCLZIP_OPT_REMOVE_PATH, 'install / release') == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Extract files successfully";

if (unlink ($ upload_dir. '/'. $ file)) {

echo 'the file was deleted';

} else {

echo 'the file was NOT deleted';

}

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

/ *

// Create .zip file of a specific folder

$ path = getcwd (). '/'; // path of the server folder (Indicate the path of the folder that contains the files to be compressed)

$ filename = $ newname; // name of the archive .zip file

$ x = 0;

if ($ handle = opendir ($ path)) {

while (false! == ($ arrayfile = readdir ($ handle))) {

if ($ arrayfile! = '.' and $ arrayfile! = '..') {

$ array_all_file [$ x] = $ path. $ arrayfile; // list of files and folders

$ x ++;

}

}

closedir ($ handle);

}

// fundamental call of the PclZip library

require_once ('pclzip.lib.php');

$ archive = new PclZip ($ filename);

// A list of filenames to be compressed

$ listOfFilesToCompress = implode (",", $ array_all_file);

// I add the files to the archive

$ v_list = $ archive-> create ($ listOfFilesToCompress);

if ($ v_list == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Archive created successfully.";

* /

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

$ filename = $ upload_dir. '/'. $ newname;

print $ thatsAll;

// print $ filename;

} else print $ wrongUp;

}

/ *

// $ archive = new PclZip ("archive.zip");

require_once ('pclzip.lib.php');

$ archive = new PclZip ("C: / wamp / www / STORE 1 woman-man-footwear-accessories - Last / UPLOAD / fullscreen / fullscreen.zip");

$ list = $ archive-> extract (PCLZIP_OPT_EXTRACT_DIR_RESTRICTION, './base_dir');

if ($ list == 0) {

die ("ERROR: '". $ archive-> errorInfo (true). "'");

}

* /

// unzip the zip file

// fundamental call of the PclZip library

/ *

function unzip ($ location, $ newLocation) {

if (exec ("unzip $ location", $ arr)) {

mkdir ($ newLocation);

for ($ i = 1; $ i <count ($ arr); $ i ++) {

$ file = trim (preg_replace ("~ inflating: ~", "", $ arr [$ i]));

copy ($ location. '/'. $ file, $ newLocation. '/'. $ file);

unlink ($ location. '/'. $ file);

}

return TRUE;

} else {

return FALSE;

}

}

if (unzip ($ filename, $ upload_dir))

echo 'Successful!';

else

echo 'Error';

$ archive = new ZipArchive ();

$ filename = $ filename;

if ($ archive-> open ($ filename)! == TRUE)

{

@exit ("Unable to open <$ filename> \ n");

}

echo "<pre>";

print_r ($ archive);

var_dump ($ archive);

echo "</pre>";

echo "The archive". $ filename. "contains the following files: \ n <br>";

echo "<pre>";

for ($ j = 0; $ j <$ archive-> numFiles; $ j ++)

{

print_r ($ archive-> statIndex ($ j));

}

echo "</pre>";

$ archive-> extractTo ('./ folder /');

$ archive-> close ();

* /

?>

<? php

// filename: upload-fullscreen-slider-home.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD3 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: upload-fullscreen-slider-home-archive.php

// Various settings to be changed at will

$ max_size = '10000000000000'; // Maximum size of photos

$ upload_dir = 'UPLOAD3 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF", "zip", "ZIP"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

$ name = '';

$ filen = '';

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

print $ file;

print $ upload_dir;

require_once ('pclzip.lib.php');

// $ filename = "backup.zip"; // enter the exact path and name of the .zip file

$ archive = new PclZip ($ upload_dir. '/'. $ file);

if ($ archive-> extract (PCLZIP_OPT_PATH, $ upload_dir,

PCLZIP_OPT_REMOVE_PATH, 'install / release') == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Extract files successfully";

if (unlink ($ upload_dir. '/'. $ file)) {

echo 'the file was deleted';

} else {

echo 'the file was NOT deleted';

}

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

/ *

// Create .zip file of a specific folder

$ path = getcwd (). '/'; // path of the server folder (Indicate the path of the folder that contains the files to be compressed)

$ filename = $ newname; // name of the archive .zip file

$ x = 0;

if ($ handle = opendir ($ path)) {

while (false! == ($ arrayfile = readdir ($ handle))) {

if ($ arrayfile! = '.' and $ arrayfile! = '..') {

$ array_all_file [$ x] = $ path. $ arrayfile; // list of files and folders

$ x ++;

}

}

closedir ($ handle);

}

// fundamental call of the PclZip library

require_once ('pclzip.lib.php');

$ archive = new PclZip ($ filename);

// A list of filenames to be compressed

$ listOfFilesToCompress = implode (",", $ array_all_file);

// I add the files to the archive

$ v_list = $ archive-> create ($ listOfFilesToCompress);

if ($ v_list == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Archive created successfully.";

* /

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

$ filename = $ upload_dir. '/'. $ newname;

print $ thatsAll;

// print $ filename;

} else print $ wrongUp;

}

/ *

// $ archive = new PclZip ("archive.zip");

require_once ('pclzip.lib.php');

$ archive = new PclZip ("C: / wamp / www / STORE 1 woman-man-footwear-accessories - Last / UPLOAD / fullscreen / fullscreen.zip");

$ list = $ archive-> extract (PCLZIP_OPT_EXTRACT_DIR_RESTRICTION, './base_dir');

if ($ list == 0) {

die ("ERROR: '". $ archive-> errorInfo (true). "'");

}

* /

// unzip the zip file

// fundamental call of the PclZip library

/ *

function unzip ($ location, $ newLocation) {

if (exec ("unzip $ location", $ arr)) {

mkdir ($ newLocation);

for ($ i = 1; $ i <count ($ arr); $ i ++) {

$ file = trim (preg_replace ("~ inflating: ~", "", $ arr [$ i]));

copy ($ location. '/'. $ file, $ newLocation. '/'. $ file);

unlink ($ location. '/'. $ file);

}

return TRUE;

} else {

return FALSE;

}

}

if (unzip ($ filename, $ upload_dir))

echo 'Successful!';

else

echo 'Error';

$ archive = new ZipArchive ();

$ filename = $ filename;

if ($ archive-> open ($ filename)! == TRUE)

{

@exit ("Unable to open <$ filename> \ n");

}

echo "<pre>";

print_r ($ archive);

var_dump ($ archive);

echo "</pre>";

echo "The archive". $ filename. "contains the following files: \ n <br>";

echo "<pre>";

for ($ j = 0; $ j <$ archive-> numFiles; $ j ++)

{

print_r ($ archive-> statIndex ($ j));

}

echo "</pre>";

$ archive-> extractTo ('./ folder /');

$ archive-> close ();

* /

?>

<? php

// filename: upload-fullscreen-slider-STORE 1.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD4 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: upload-fullscreen-slider-STORE 1-archive.php

// Various settings to be changed at will

$ max_size = '10000000000000'; // Maximum size of photos

$ upload_dir = 'UPLOAD4 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF", "zip", "ZIP"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

$ name = '';

$ filen = '';

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

print $ file;

print $ upload_dir;

require_once ('pclzip.lib.php');

// $ filename = "backup.zip"; // enter the exact path and name of the .zip file

$ archive = new PclZip ($ upload_dir. '/'. $ file);

if ($ archive-> extract (PCLZIP_OPT_PATH, $ upload_dir,

PCLZIP_OPT_REMOVE_PATH, 'install / release') == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Extract files successfully";

if (unlink ($ upload_dir. '/'. $ file)) {

echo 'the file was deleted';

} else {

echo 'the file was NOT deleted';

}

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

/ *

// Create .zip file of a specific folder

$ path = getcwd (). '/'; // path of the server folder (Indicate the path of the folder that contains the files to be compressed)

$ filename = $ newname; // name of the archive .zip file

$ x = 0;

if ($ handle = opendir ($ path)) {

while (false! == ($ arrayfile = readdir ($ handle))) {

if ($ arrayfile! = '.' and $ arrayfile! = '..') {

$ array_all_file [$ x] = $ path. $ arrayfile; // list of files and folders

$ x ++;

}

}

closedir ($ handle);

}

// fundamental call of the PclZip library

require_once ('pclzip.lib.php');

$ archive = new PclZip ($ filename);

// A list of filenames to be compressed

$ listOfFilesToCompress = implode (",", $ array_all_file);

// I add the files to the archive

$ v_list = $ archive-> create ($ listOfFilesToCompress);

if ($ v_list == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Archive created successfully.";

* /

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

$ filename = $ upload_dir. '/'. $ newname;

print $ thatsAll;

// print $ filename;

} else print $ wrongUp;

}

/ *

// $ archive = new PclZip ("archive.zip");

require_once ('pclzip.lib.php');

$ archive = new PclZip ("C: / wamp / www / STORE 1 woman-man-footwear-accessories - Last / UPLOAD / fullscreen / fullscreen.zip");

$ list = $ archive-> extract (PCLZIP_OPT_EXTRACT_DIR_RESTRICTION, './base_dir');

if ($ list == 0) {

die ("ERROR: '". $ archive-> errorInfo (true). "'");

}

* /

// unzip the zip file

// fundamental call of the PclZip library

/ *

function unzip ($ location, $ newLocation) {

if (exec ("unzip $ location", $ arr)) {

mkdir ($ newLocation);

for ($ i = 1; $ i <count ($ arr); $ i ++) {

$ file = trim (preg_replace ("~ inflating: ~", "", $ arr [$ i]));

copy ($ location. '/'. $ file, $ newLocation. '/'. $ file);

unlink ($ location. '/'. $ file);

}

return TRUE;

} else {

return FALSE;

}

}

if (unzip ($ filename, $ upload_dir))

echo 'Successful!';

else

echo 'Error';

$ archive = new ZipArchive ();

$ filename = $ filename;

if ($ archive-> open ($ filename)! == TRUE)

{

@exit ("Unable to open <$ filename> \ n");

}

echo "<pre>";

print_r ($ archive);

var_dump ($ archive);

echo "</pre>";

echo "The archive". $ filename. "contains the following files: \ n <br>";

echo "<pre>";

for ($ j = 0; $ j <$ archive-> numFiles; $ j ++)

{

print_r ($ archive-> statIndex ($ j));

}

echo "</pre>";

$ archive-> extractTo ('./ folder /');

$ archive-> close ();

* /

?>

<? php

// filename: upload-fullscreen-slider-STORE 2.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD5 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: upload-fullscreen-slider-STORE 2-archive.php

// Various settings to be changed at will

$ max_size = '10000000000000'; // Maximum size of photos

$ upload_dir = 'UPLOAD5 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF", "zip", "ZIP"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

$ name = '';

$ filen = '';

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

print $ file;

print $ upload_dir;

require_once ('pclzip.lib.php');

// $ filename = "backup.zip"; // enter the exact path and name of the .zip file

$ archive = new PclZip ($ upload_dir. '/'. $ file);

if ($ archive-> extract (PCLZIP_OPT_PATH, $ upload_dir,

PCLZIP_OPT_REMOVE_PATH, 'install / release') == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Extract files successfully";

if (unlink ($ upload_dir. '/'. $ file)) {

echo 'the file was deleted';

} else {

echo 'the file was NOT deleted';

}

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

/ *

// Create .zip file of a specific folder

$ path = getcwd (). '/'; // path of the server folder (Indicate the path of the folder that contains the files to be compressed)

$ filename = $ newname; // name of the archive .zip file

$ x = 0;

if ($ handle = opendir ($ path)) {

while (false! == ($ arrayfile = readdir ($ handle))) {

if ($ arrayfile! = '.' and $ arrayfile! = '..') {

$ array_all_file [$ x] = $ path. $ arrayfile; // list of files and folders

$ x ++;

}

}

closedir ($ handle);

}

// fundamental call of the PclZip library

require_once ('pclzip.lib.php');

$ archive = new PclZip ($ filename);

// A list of filenames to be compressed

$ listOfFilesToCompress = implode (",", $ array_all_file);

// I add the files to the archive

$ v_list = $ archive-> create ($ listOfFilesToCompress);

if ($ v_list == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Archive created successfully.";

* /

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

$ filename = $ upload_dir. '/'. $ newname;

print $ thatsAll;

// print $ filename;

} else print $ wrongUp;

}

/ *

// $ archive = new PclZip ("archive.zip");

require_once ('pclzip.lib.php');

$ archive = new PclZip ("C: / wamp / www / STORE 1 woman-man-footwear-accessories - Last / UPLOAD / fullscreen / fullscreen.zip");

$ list = $ archive-> extract (PCLZIP_OPT_EXTRACT_DIR_RESTRICTION, './base_dir');

if ($ list == 0) {

die ("ERROR: '". $ archive-> errorInfo (true). "'");

}

* /

// unzip the zip file

// fundamental call of the PclZip library

/ *

function unzip ($ location, $ newLocation) {

if (exec ("unzip $ location", $ arr)) {

mkdir ($ newLocation);

for ($ i = 1; $ i <count ($ arr); $ i ++) {

$ file = trim (preg_replace ("~ inflating: ~", "", $ arr [$ i]));

copy ($ location. '/'. $ file, $ newLocation. '/'. $ file);

unlink ($ location. '/'. $ file);

}

return TRUE;

} else {

return FALSE;

}

}

if (unzip ($ filename, $ upload_dir))

echo 'Successful!';

else

echo 'Error';

$ archive = new ZipArchive ();

$ filename = $ filename;

if ($ archive-> open ($ filename)! == TRUE)

{

@exit ("Unable to open <$ filename> \ n");

}

echo "<pre>";

print_r ($ archive);

var_dump ($ archive);

echo "</pre>";

echo "The archive". $ filename. "contains the following files: \ n <br>";

echo "<pre>";

for ($ j = 0; $ j <$ archive-> numFiles; $ j ++)

{

print_r ($ archive-> statIndex ($ j));

}

echo "</pre>";

$ archive-> extractTo ('./ folder /');

$ archive-> close ();

* /

?>

<? php

// filename: upload-fullscreen-slider-STORE 3.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD6 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: upload-fullscreen-slider-STORE 3-archive.php

// Various settings to be changed at will

$ max_size = '10000000000000'; // Maximum size of photos

$ upload_dir = 'UPLOAD6 / fullscreen'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF", "zip", "ZIP"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

$ name = '';

$ filen = '';

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

print $ file;

print $ upload_dir;

require_once ('pclzip.lib.php');

// $ filename = "backup.zip"; // enter the exact path and name of the .zip file

$ archive = new PclZip ($ upload_dir. '/'. $ file);

if ($ archive-> extract (PCLZIP_OPT_PATH, $ upload_dir,

PCLZIP_OPT_REMOVE_PATH, 'install / release') == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Extract files successfully";

if (unlink ($ upload_dir. '/'. $ file)) {

echo 'the file was deleted';

} else {

echo 'the file was NOT deleted';

}

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

/ *

// Create .zip file of a specific folder

$ path = getcwd (). '/'; // path of the server folder (Indicate the path of the folder that contains the files to be compressed)

$ filename = $ newname; // name of the archive .zip file

$ x = 0;

if ($ handle = opendir ($ path)) {

while (false! == ($ arrayfile = readdir ($ handle))) {

if ($ arrayfile! = '.' and $ arrayfile! = '..') {

$ array_all_file [$ x] = $ path. $ arrayfile; // list of files and folders

$ x ++;

}

}

closedir ($ handle);

}

// fundamental call of the PclZip library

require_once ('pclzip.lib.php');

$ archive = new PclZip ($ filename);

// A list of filenames to be compressed

$ listOfFilesToCompress = implode (",", $ array_all_file);

// I add the files to the archive

$ v_list = $ archive-> create ($ listOfFilesToCompress);

if ($ v_list == 0) {

die ("Error:". $ archive-> errorInfo (true));

}

echo "Archive created successfully.";

* /

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

$ filename = $ upload_dir. '/'. $ newname;

print $ thatsAll;

// print $ filename;

} else print $ wrongUp;

}

/ *

// $ archive = new PclZip ("archive.zip");

require_once ('pclzip.lib.php');

$ archive = new PclZip ("C: / wamp / www / STORE 1 woman-man-footwear-accessories - Last / UPLOAD / fullscreen / fullscreen.zip");

$ list = $ archive-> extract (PCLZIP_OPT_EXTRACT_DIR_RESTRICTION, './base_dir');

if ($ list == 0) {

die ("ERROR: '". $ archive-> errorInfo (true). "'");

}

* /

// unzip the zip file

// fundamental call of the PclZip library

/ *

function unzip ($ location, $ newLocation) {

if (exec ("unzip $ location", $ arr)) {

mkdir ($ newLocation);

for ($ i = 1; $ i <count ($ arr); $ i ++) {

$ file = trim (preg_replace ("~ inflating: ~", "", $ arr [$ i]));

copy ($ location. '/'. $ file, $ newLocation. '/'. $ file);

unlink ($ location. '/'. $ file);

}

return TRUE;

} else {

return FALSE;

}

}

if (unzip ($ filename, $ upload_dir))

echo 'Successful!';

else

echo 'Error';

$ archive = new ZipArchive ();

$ filename = $ filename;

if ($ archive-> open ($ filename)! == TRUE)

{

@exit ("Unable to open <$ filename> \ n");

}

echo "<pre>";

print_r ($ archive);

var_dump ($ archive);

echo "</pre>";

echo "The archive". $ filename. "contains the following files: \ n <br>";

echo "<pre>";

for ($ j = 0; $ j <$ archive-> numFiles; $ j ++)

{

print_r ($ archive-> statIndex ($ j));

}

echo "</pre>";

$ archive-> extractTo ('./ folder /');

$ archive-> close ();

* /

?>

<? php

// filename: uploadnews1.php

// Various settings to be changed at will

$ max_size = '12600000'; // Maximum size of photos

$ upload_dir = 'UPLOAD / news / img'; // Folder where I place the photos

$ extensions = array ("png", "jpg", "gif", "PNG", "JPG", "GIF"); // Allowed File Types

$ noSubmitSend = 'No upload done!'; // Error message when the PHP script is invoked directly

$ wrongExt = 'Invalid file extension!'; // Error message for file type not allowed

$ tooBig = 'The file exceeds the max size!'; // Error message for file too large

$ thatsAll = 'Photo uploaded successfully!'; // OK message for successful upload

$ wrongUp = 'Something wrong here!'; // Error message when script fails to upload

// ***************************************

// Check the submit of the HTML form ...

if (isset ($ _ POST ['send'])) {

$ file = $ _FILES ['userimage'] ['name'];

// Check the file type ...

if (in_array (array_pop (explode ('.', $ file)), $ extensions)) {

// Check the file size ...

$ file_size = $ _FILES ['userimage'] ['size'];

if ($ file_size> $ max_size) {

print $ tooBig;

} else {

doUpload ($ file, $ upload_dir);

}

} else {

print $ wrongExt;

}

} else {

print $ noSubmitSend;

}

function doUpload ($ file, $ upload_dir) {

global $ thatsAll;

$ filename = $ _FILES ['userimage'] ['tmp_name'];

$ realname = $ _FILES ['userimage'] ['name'];

$ realname = htmlentities (strtolower ($ realname));

if (is_uploaded_file ($ filename)) {

$ newname = ($ realname);

$ ext = end (explode ('.', $ realname));

$ filename = explode ('.', $ realname);

/ *

if (file_exists ($ upload_dir. '/'. $ realname)) {

$ filename [0]. = '.';

for ($ a = 0; $ a <= 9; $ a ++)

$ filename [0]. = chr (rand (97,122));

$ newname = $ filename [0]. '.' . $ ext;

}

* /

$ newname = str_replace ('', '_', $ newname);

@move_uploaded_file ($ filename, ($ upload_dir. '/'. $ newname));

print $ thatsAll;

} else print $ wrongUp;

}

?>

<? php

// filename: uploadnews3.php

// Get the value of the "type" parameter

$ news = $ _GET ['news'];

// Get the value of the "model" parameter

// $ car_model = $ _GET ['model'];

// Now I just print the result on the screen

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ news = mysql_real_escape_string ($ news);

// POST variables with anti sql Injection

// mysql_real_escape_string ($ news); // escape malicious characters

// $ id1 = mysql_insert_id ();

// $ id1 = "SELECT LAST_INSERT_ID ()";

/ *

$ result = mysql_query ("SELECT max (id) FROM data_news");

if (! $ result) {

die ('Could not query:'. mysql_error ());

}

$ id1 = mysql_result ($ result, 0, 'id');

/ *

$ idquery = "SELECT MAX (id) as max FROM data_news";

$ row = mysql_fetch_array ($ idquery);

$ id1 = $ row ['max']; * /

// $ id11 = (int) $ id1;

$ id1 = mysql_query ("SELECT MAX (id2) FROM data_news");

// echo $ id1;

// $ id1 = MAX (id);

$ id2 = $ id1 + 1;

$ query = "INSERT INTO data_news (news, id2) VALUES ('$ news', '$ id2')";

$ result = mysql_query ($ query);

// $ query = "ALTER TABLE data_news AUTO_INCREMENT = $ id1";

// check the outcome

if (! $ result) {

die ("Error in query $ query:". mysql_error ());

}

// get the autoincrement id generated by MySQL for the new record inserted

$ inserted_id = mysql_insert_id ();

$ id1 = $ inserted_id;

// mysql_close ($ connection);

$ query = "SELECT * FROM data_news ORDER BY 'id'";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ number = mysql_num_rows ($ ris);

$ i = 0;

$ o = $ i + 1;

if ($ number <1) {

print "<center> <p> Your search did not return any results </p> </center>";

} else {

while ($ number> $ i) {

$ id = mysql_result ($ ris, $ i, "id");

$ query = "UPDATE data_news set id2 = '$ o' WHERE id = $ id";

$ result = mysql_query ($ query);

// check the outcome

if (! $ result) {

die ("Error in query $ query:". mysql_error ());

}

{

}

$ i ++;

$ o = $ i + 1;

}

}

echo '<script language = javascript> document.location.href = "insert photo.php" </script>';

?>

<? php

// filename: uploadnews4.php

// Get the value of the "type" parameter

$ o = $ _ GET ['i'];

$ i = (int) $ o;

// $ i = parseInt ($ o);

$ news = $ _GET ['news'];

// Get the value of the "model" parameter

// $ car_model = $ _GET ['model'];

// Now I just print the result on the screen

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

// POST variables with anti sql Injection

$ news = mysql_real_escape_string ($ news);

// mysql_real_escape_string ($ news); // escape malicious characters

// $ news = str_replace ($ news, "'", "' '");

// var_dump ($ news);

// $ news = addslashes ($ news); // adds the slash

// $ news = addslashes ($ news);

// $ query = "UPDATE data_news set news =". $ news. "WHERE id =". $ i;

// $ news2 = addslashes ($ news);

$ query = "UPDATE data_news set news = '$ news' WHERE id2 = '$ i'";

$ result = mysql_query ($ query);

// check the outcome

if (! $ result) {

die ("Error in query $ query:". mysql_error ());

}

{

// get the autoincrement id generated by MySQL for the new record inserted

// mysql_close ($ connection);

}

echo '<script language = javascript> document.location.href = "insert photo.php" </script>';

?>

<? php

// filename: uploadnews5.php

// Get the value of the "type" parameter

$ o = $ _ GET ['i'];

$ i = (int) $ o;

// $ i = parseInt ($ o);

// Get the value of the "model" parameter

// $ car_model = $ _GET ['model'];

// Now I just print the result on the screen

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

// POST variables with anti sql Injection

// mysql_real_escape_string ($ news); // escape malicious characters

$ query = "DELETE FROM data_news WHERE id2 = '$ i'";

$ result = mysql_query ($ query);

// check the outcome

if (! $ result) {

die ("Error in query $ query:". mysql_error ());

}

// $ query = "ALTER TABLE data_news AUTO_INCREMENT = $ i";

/ *

// get the autoincrement id generated by MySQL for the new one

record inserted using column id with a prepared statement

$ query = 'DELETE FROM data_news WHERE id =: id';

prepare the statement

$ stmt = $ pdo-> prepare ($ query);

execute the statement while setting the id prepared statement

$ result = $ stmt-> execute (array (': id' => $ id));

if ($ result) {

echo 'Record Successfully Deleted';

}

* /

$ query = "SELECT * FROM data_news ORDER BY 'id'";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ number = mysql_num_rows ($ ris);

$ i = 0;

$ o = $ i + 1;

if ($ number <1) {

} else {

while ($ number> $ i) {

$ id = mysql_result ($ ris, $ i, "id");

$ query = "UPDATE data_news set id2 = '$ o' WHERE id = $ id";

$ result = mysql_query ($ query);

// check the outcome

if (! $ result) {

die ("Error in query $ query:". mysql_error ());

}

{

}

$ i ++;

$ o = $ i + 1;

}

}

echo '<script language = javascript> document.location.href = "insert photo.php" </script>';

?>

<? php

// filename: verify.php

session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

// POST variables with anti sql Injection

$ username = mysql_real_escape_string ($ _ POST ['username']); // escape malicious characters

$ password = mysql_real_escape_string (sha1 ($ _ POST ['password'])); // sha1 encrypts the password here also in this way corresponds to that of the db

$ _SESSION ['username'] = $ username;

$ query = "SELECT * FROM login WHERE username = '$ username' AND password = '$ password'";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ cod = $ line ['username'];

/ * I check * /

if ($ cod == NULL) $ found = 0;

else $ found = 1;

/ * Username and password correct * /

if ($ found === 1) {

/ * Log session * /

// session_register ('authorized');

$ _SESSION ["authorized"] = 1;

/ * Register user code * /

$ _SESSION ['cod'] = $ cod;

/ * Redirect to the reserved page * /

echo '<script language = javascript> document.location.href = "insert photo.php" </script>';

} else {

/ * Wrong username and password, redirect to login page * /

echo '<script language = javascript> document.location.href = "login.html" </script>';

}

?>

<? php

// filename: verify2.php

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n = $ line ['n'];

echo $ n;

$ num = $ n + 1;

for ($ i = 1; $ i <= $ num; ++ $ i) {

echo "ceremony0 $ i.jpg";

echo "<a href='UPLOAD/fullscreen/cerimonia0$i.jpg' rel='prettyPhoto [[]]> ​​<img src = 'UPLOAD / thumbnails / ceremony0 $ i.jpg' class = 'photo_preview' /> </ a> ";

}

?>

<? php

// filename: vismod.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

$ i = $ _GET ['i'];

mysql_select_db ("$ db_name", $ connection);

// $ i = mysql_real_escape_string ($ _ POST ['i']);

$ query = "SELECT * FROM data_news WHERE id2 = '$ i'";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ news = $ line ['news'];

$ _SESSION ['news'] = $ news;

echo $ _POST ['$ news'];

echo '<script language = javascript> document.location.href = "insert photo.php" </script>';

?>

<? php

// filename: visnews.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data_news";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ number = mysql_num_rows ($ ris);

$ i = 0;

$ o = $ i + 1;

$ n = $ number + 1;

if ($ number <1) {

print "<center> <p> Your search did not return any results </p> </center>";

} else {

while ($ number> $ i) {

$ news = mysql_result ($ ris, $ i, "news");

if ($ o == 1) {echo "<div role = 'tabpanel' class = 'tab-pane fade in active' id = 'tab $ o'> <a class='testimonial-image'> <img src = 'UPLOAD / news / img / imgnews $ o.jpg' alt = '' data-at2x = 'UPLOAD / img / news / img / imgnews $ o.jpg'> </a> <div class = 'testimonial-text' > <h3> News $ o </h3> <p> $ news </p> </div> </div> ";

} {

echo "<div role = 'tabpanel' class = 'tab-pane fade' id = 'tab $ o'> <div class = 'testimonial-image'> <img src = 'UPLOAD / news / img / imgnews $ o. jpg 'alt =' 'data-at2x =' UPLOAD / img / news / img / imgnews $ o.jpg '> </div> <div class =' ​​testimonial-text '> <h3> News $ o </h3> <p> $ news </p> </div> </div> ";

}

$ i ++;

$ o = $ i + 1;

}

}

?>

<? php

// filename: view ws.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data_news";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ number = mysql_num_rows ($ ris);

$ i = 0;

$ o = $ i + 1;

$ n = $ number + 1;

if ($ number <1) {

print "<center> <p> Your search did not return any results </p> </center>";

} else {

while ($ number> $ i) {

$ news = mysql_result ($ ris, $ i, "news");

$ id2 = mysql_result ($ ris, $ i, "id2");

echo "<div class = 'testimonial-image'> <img src = 'UPLOAD / news / img / imgnews $ o.jpg' alt = '' data-at2x = 'UPLOAD / img / news / img / imgnews $ o. jpg 'width =' 8% '> </div> <div class =' ​​testimonial-text '> <p> id = $ id2 - news = $ news </p> </div> ";

$ i ++;

$ o = $ i + 1;

}

}

?>

<? php

// filename: view-slider-home.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n3 = $ line ['n3'];

$ dir = 'UPLOAD3 / fullscreen /';

$ files = scandir ($ dir);

foreach ($ files as $ fil)

{

$ filename = $ dir. "/". $ fil;

$ cont = $ cont + 1;

if ($ cont> 2) {

$ c = $ cont-2;

echo "

<li>

<img src = '$ filename'>

<div class = 'flex-caption'>

<h5>

<div class = 'row'>

<div class = 'col-sm-4'>

STORE 1

</div>

<div class = 'col-sm-4'>

STORE 3

</div>

<div class = 'col-sm-4'>

STORE 2

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'col-sm-4'>

</div>

<div class = 'row'>

<br>

<br>

</h5>

What are you waiting for! Come and visit us !!

</div>

</h1>

</li>

";

}

}

?>

<? php

// filename: view-slider-STORE 1.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n3 = $ line ['n3'];

$ dir = 'UPLOAD4 / fullscreen /';

$ files = scandir ($ dir);

foreach ($ files as $ fil)

{

$ filename = $ dir. "/". $ fil;

$ cont = $ cont + 1;

if ($ cont> 2) {

$ c = $ cont-2;

echo "

<li>

<img src = '$ filename'>

<div class = 'flex-caption'>

<h5>

<div class = 'row'>

STORE 1

<br>

</div>

</h5>

</li>

";

}

}

?>

<? php

// filename: view-slider-STORE 2.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n3 = $ line ['n3'];

$ dir = 'UPLOAD5 / fullscreen /';

$ files = scandir ($ dir);

foreach ($ files as $ fil)

{

$ filename = $ dir. "/". $ fil;

$ cont = $ cont + 1;

if ($ cont> 2) {

$ c = $ cont-2;

echo "

<li>

<img src = '$ filename'>

<div class = 'flex-caption'>

<h5>

<div class = 'row'>

STORE 2

<br>

</div>

</h5>

</li>

";

}

}

?>

<? php

// filename: view-slider-STORE 3.php

// session_start (); // start the session

// I include the files necessary to connect to the db with its login script

include ("connection_db.php");

include ("config.php");

// I connect

mysql_select_db ("$ db_name", $ connection);

$ query = "SELECT * FROM data WHERE id = 1";

$ ris = mysql_query ($ query, $ connection) or die (mysql_error ());

$ line = mysql_fetch_array ($ ris);

/ * I collect the user ID * /

$ n3 = $ line ['n3'];

$ dir = 'UPLOAD6 / fullscreen /';

$ files = scandir ($ dir);

foreach ($ files as $ fil)

{

$ filename = $ dir. "/". $ fil;

$ cont = $ cont + 1;

if ($ cont> 2) {

$ c = $ cont-2;

echo "

<li>

<img src = '$ filename'>

<div class = 'flex-caption'>

<h5>

<div class = 'row'>

STORE 3

<br>

</div>

</h5>

</li>

";

}

}

?>

# Other files present in the site folder

The filepclzip.lib.phpcan be downloaded from the internet and is used to zip and unzip files:

[https://github.com/chamilo/pclzip/blob/master/pclzip.lib.php](https://github.com/chamilo/pclzip/blob/master/pclzip.lib.php)

Remember to download this file and insert it in the site folder otherwise you will not be able to upload the zipped images from the site menu.

If you can't download it you can copy it from the internet and paste it on notepad and save the file with the name pclzip.lib.php, if you don't know where to put your hands, never change the names of the files because they are linked to other files.

The js files written in javascript actually in this project were downloaded with bootstrap or free from internet for image scrolling like prettyPhoto. In this book we did not want to deepen the javascript language which will be the subject of a future book.

I remind you that prettyPhoto also exists as a WordPress plugin.

The javascript files present in the JS folder are:

![](images/ebook_image_205181_6994a3c6324732b0.jpg)

***I remind you that in your site you can incorporate all the codes that you will find on the internet respecting the relative licenses if they exist, but always paying attention to the general functioning of the site and to the slowdown in load that too many programs bring.***

# Change the style of the site

In this case, if we are at the beginning of the project, we can directly change the whole site by downloading a bootstrap or creating it from scratch, as seen previously, otherwise if we are already at the end of the work, we can only change the CSS style sheet manually with Notepad or by copying the style folder from another Bootstrap or from another site and modifying it with Nicepage or with a mobile application such as TrebEdit or Html Creator and many others present on the various stores as previously indicated.

The original page is the one below:

![](images/ebook_image_205181_90ea14796411ed44.jpg)

Here is an example of changing the entire Bootstrap style folder, after finishing the site:

![](images/ebook_image_205181_d40a63f6f98d9e60.jpg)

Obviously, after having changed the style sheet, it would be better to open the sheet itself with Notepad and check it carefully, keeping in mind the result you want to obtain.

***Small warning for non-experts is to always save the previous work in a backup folder before making any changes.***

# See the site on WAMP

To view the site created on WAMP you must first click on wampmanager.exe to activate WAMP_ then enter the menu at the bottom left of WAMP and click on localhost.![](images/ebook_image_205181_6eddc5c3a9e4d5ba.jpg)![](images/ebook_image_205181_7ef619f1277aacf5.jpg)![](images/ebook_image_205181_c6ad06d7b4976fc1.jpg)

Now, if we click on the folder we are interested in, we will probably have an error screen like the following.

![](images/ebook_image_205181_c7e8448aae50fc2c.jpg)

In this case we have to type 127.0.0.1 in the address before the folder address and our site will appear in simulation with the php files and working databases. To access our site located in the www folder of wamp we will therefore insert the address in the bar always with the address 127.0.0.1 otherwise it will not work. The address 127.0.0.1, in fact, identifies your computer and is therefore the address of the localhost in which we can view our site.

[http://127.0.0.1/negozio%20abbigliamento%20donna-uomo-calzature-accessori%20%2027%2011%202021%20aggiornato/](http://127.0.0.1/negozio%20abbigliamento%20donna-uomo-calzature-accessori%20%2027%2011%202021%20aggiornato/)

Our final site will consist of nine web pages plus a control panel for inserting images and news.

![](images/ebook_image_205181_2c3359e5ea691c40.jpg)![](images/ebook_image_205181_b18a6fc46c684d45.jpg)![](images/ebook_image_205181_84b4a9ea8f747e4b.jpg)![](images/ebook_image_205181_4d6582c5b0afc9f6.jpg)![](images/ebook_image_205181_30bf861ad73f82ef.jpg)![](images/ebook_image_205181_8e1e3dae3973846b.jpg)![](images/ebook_image_205181_91ed55d6c19380c2.jpg)![](images/ebook_image_205181_d7b3438d8b3c3c33.jpg)![](images/ebook_image_205181_96435919c75d4ed8.jpg)![](images/ebook_image_205181_f866bd9fc53c012e.jpg)![](images/ebook_image_205181_86c8fce4a9a6e22d.jpg)

***I remind you that if you have to change the names of the files inserted in the html pages, you have to change the name on all the pages that contain the link and then update each page on the browser or on WAMP to see the result. It is advisable to make any changes at the beginning of the work on the site as the more pages you complete, the more complicated the update becomes.***

# Publication of the site

To publish the site after having taken a complete hosting of Database and memory space, we will copy the files of the www folder of WAMP, we will create the Databases in the hosting and we will change some connection files of the Databases themselves as indicated later.

In fact, when we go to publish the site on a hosting with the files copied from the WAMP folder without modifying them it will certainly not work, in this do not worry because over time some codes become deprecated in MySql and may not work, also you will have to configure the Database with the password and database name you have chosen. In this case you have to modify the following files:

***I remind you that when you transfer the site files to the hosting on the network you will have to reconfigure the databases and enter the user, the database name and the password chosen during the creation of the database in the hosting itself using the procedure already described above.***

In fact, in WAMP the Database is set by default:

<? php

// filename: config.php

// general

$ website_internet = "";

$ date = (date ("dmy"));

$ vers = "2.0";

// URL FOR HTACCESS

// $ base_url = "http: // localhost / yoursite";

// DB connection

$ host = "localhost";

$ db_user = "root";

$ db_psw = "";

$ db_name = "mydb";

?>

![](images/ebook_image_205181_8cf0046680172bd2.jpg)![](images/ebook_image_205181_d2afa50aaaaeb229.jpg)

The file will have to be modified in the highlighted lines:

<? php

// general

$ website_internet = "";

$ date = (date ("dmy"));

$ vers = "2.0";

// URL FOR HTACCESS

// $ base_url = "http: // localhost / yoursite";

// DB connection

$ host = "localhost";

$ db_user = " my_user ";

$ db_psw = "";

$ db_name = "my_nomedb";

?>

***I remind you that in MySql many times over time some instructions can become deprecated and not make the entire code work. In this case we have to modify the following files:***

Connection_db.php file:

<? php

include_once ('mysql-fix.php');

include ("config.php"); // include configuration file for variable retrieval

$ connection = mysql_connect ("$ host", "$ db_user", "$ db_psw");

if (! $ connection)

{

die ("Critical Database Connection Error". mysql_error ());

}

?>

Mysql-fix.php file :

<? php

if (! function_exists ("mysql_connect")) {

/ * warning: fatal error "cannot redeclare" if a function was disabled in php.ini with disable_functions:

disable_functions = mysql_connect, mysql_pconnect, mysql_select_db, mysql_ping, mysql_query, mysql_fetch_assoc, mysql_num_rows, mysql_fetch_array, mysql_error, mysql_insert_id, mysql_real_stress_close, mysql_strata_close, mysql_strata_close

* /

define ("MYSQL_ASSOC", MYSQLI_ASSOC);

define ("MYSQL_NUM", MYSQLI_NUM);

define ("MYSQL_BOTH", MYSQLI_BOTH);

function mysql_fetch_array ($ result, $ result_type = MYSQL_BOTH) {

$ row = mysqli_fetch_array ($ result, $ result_type);

return is_null ($ row)? false: $ row;

}

function mysql_fetch_assoc ($ result) {

$ row = mysqli_fetch_assoc ($ result);

return is_null ($ row)? false: $ row;

}

function mysql_fetch_row ($ result) {

$ row = mysqli_fetch_row ($ result);

return is_null ($ row)? false: $ row;

}

function mysql_fetch_object ($ result) {

$ row = mysqli_fetch_object ($ result);

return is_null ($ row)? false: $ row;

}

function mysql_connect ($ host, $ username, $ password, $ new_link = FALSE, $ client_flags = 0) {

global $ global_link_identifier;

$ global_link_identifier = mysqli_connect ($ host, $ username, $ password);

return $ global_link_identifier;

}

function mysql_pconnect ($ host, $ username, $ password, $ client_flags = 0) {

global $ global_link_identifier;

$ global_link_identifier = mysqli_connect ("p:". $ host, $ username, $ password);

return $ global_link_identifier;

}

function mysql_select_db ($ dbname, $ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_select_db ($ link_identifier, $ dbname);

}

function mysql_ping ($ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_ping ($ link_identifier);

}

function mysql_query ($ stmt, $ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_query ($ link_identifier, $ stmt);

}

function mysql_num_rows ($ result) {

return mysqli_num_rows ($ result);

}

function mysql_affected_rows ($ link_identifier = NULL) {

// TODO: check, if working when called without argument: mysql_affected_rows ()

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_affected_rows ($ link_identifier);

}

function mysql_list_tables ($ dbname, $ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

$ sql = "SHOW TABLES FROM $ dbname";

$ result = mysql_query ($ sql, $ link_identifier);

return $ result;

}

function mysql_error ($ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_error ($ link_identifier);

}

function mysql_errno ($ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_errno ($ link_identifier);

}

function mysql_insert_id ($ link_identifier = NULL) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_insert_id ($ link_identifier);

}

function mysql_close ($ link_identifier = NULL) {

return true;

}

function mysql_real_escape_string ($ unescaped_string, $ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_real_escape_string ($ link_identifier, $ unescaped_string);

}

function mysql_data_seek ($ result, $ row_number) {

return mysqli_data_seek ($ result, $ row_number);

}

function mysql_result ($ result, $ row = 0, $ col = 0) {

$ numrows = mysqli_num_rows ($ result);

if ($ numrows && $ row <= ($ numrows-1) && $ row> = 0) {

mysqli_data_seek ($ result, $ row);

$ resultrow = (is_numeric ($ col))? mysqli_fetch_row ($ result): mysqli_fetch_assoc ($ result);

if (isset ($ resultrow [$ col])) {

return $ resultrow [$ col];

}

}

return false;

}

function mysql_escape_string ($ s, $ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_real_escape_string ($ link_identifier, $ s);

}

function mysql_field_name ($ result, $ i) {

return mysqli_fetch_field_direct ($ result, $ i);

}

function mysql_free_result ($ result) {

return mysqli_free_result ($ result);

}

function mysql_get_server_info ($ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_get_server_info ($ link_identifier);

}

function mysql_set_charset ($ csname, $ link_identifier = null) {

global $ global_link_identifier;

if ($ link_identifier == null) {

$ link_identifier = $ global_link_identifier;

}

return mysqli_set_charset ($ link_identifier, $ csname);

}

}

?>

***Now that you have rectified the previous files you will be able to see your site working in all its parts.***

***Obviously the site will only allow the insertion of images, to modify and delete them you will have to change the settings of the Database and insert the images directly into the latter as we did for the text part of the News.***

# Conclusions

In this work we wanted to explain the basics for creating a dynamic website with an example based on three clothing stores belonging to the same company. We applied and modified a bootstrap according to our needs and used clent-side and server-side programming.

To complete the topic we have explained what databases are and how phpMyadmin works.

We also learned to use WAMP to view the result of our site locally and we figured out how to bring the site created back to hosting.

You are now ready to experiment with creating your own dynamic site yourself.