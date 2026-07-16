![](image_rsrc21P.jpg)

NODE JS

FOR BEGINNER

AND

MySQL

In This Book You Will Learn Explanation with Diagramme and

Working Exercises with Successfull Execution of Exercises with Output

Readymade Solution With Step By Step Explanation

AMIT K

Contents

Beginners Guide to Learn Node Js Programming Step by Step

Introduction

Chapter 1 : Introduction to NodeJs

1  What is NodeJs

2  Chrome & V8 Javascript Engine

3  NodeJS

4  NodeJs Javascript Library

Chapter 2 : Install Atom Editor

1  What is Atom software

Chapter 3 : Install NodeJS on Windows

1  Install NodeJS

Chapter 4 : What is NPM

1  What is NPM

2  Features of the NPM

Chapter 5 : NodeJS

1  Create a NodeJS project

2  Express

3  Create structure for project

Chapter 6 : Create a Simple HTTP Server with NodeJS

1  Create NodeJS HTTP Server

Chapter 7 : NodeJS Modules

1  What is NodeJS Module

2  Create your Module

Chapter 8 : Concept of Callback in NodeJS

1  What is Callback

2  NodeJS Callback

Chapter 9 : Understanding Event Loop in NodeJS

1  NodeJS Event Loop Overview

2  Event Loop

3  Thread Pool

Chapter 10 : NodeJS EventEmitter

1  NodeJS EventEmitter

2  Listener

Chapter 11 : Software  Installation

1  Introduction

2  Eclipse Installation

3  Jdk1.6 Installation And Configuring to Eclipse

4  Tomcat1.6 Installation And Configuring to Eclipse

5  MySql5.0 Installation

6  Eclipse Font Size Increase

Introduction

Learning Node Js step by step.

Node Js For Beginner : The Ultimade Guide for Intermediate Developer to Unleash the Power of Server Side Javascript

Unlock the full potential of Node.js and revolutionize your web and server-side development skills with "Mastering Node.js: The Ultimate Guide for Intermediate Developers to Unleash the Power of Server-Side JavaScript."

Node.js has taken the world of web development by storm, thanks to its speed, scalability, and rich ecosystem. In this comprehensive ebook, we take you on a journey from intermediate to advanced Node.js developer, arming you with the knowledge and skills to tackle complex projects and build high-performance applications.

Discover the core concepts of Node.js, from asynchronous programming and event-driven architecture to managing dependencies with npm and Yarn. Dive into the world of web applications with Express.js and explore specialized frameworks for creating RESTful APIs, whether it's building a single-page application or a high-traffic service.

Learn the art of real-time communication with WebSockets, perfect for crafting interactive applications and delivering data updates in real-time. Explore database integration with MySQL databases.

Chapter 1 :

Introduction to NodeJs

What is NodeJs

Before directly answering the question "What is NodeJS?", I am going to introduce you about the birth context of the NodeJS, which helps you understand the matter more easily.

Chrome & V8 Javascript Engine

Everyone knows that Chrome is a famous and free Google browser with the first version released in December 2008, of which V8 JavaScript Engine is a program written on C++, open source code, used in the Google Chrome to parse and execute Javascript code with high performance. It parses Javascript syntax and interprets it into computer code for execution.

| ![](image_rsrc21R.jpg) |

Note : The Browser other than the Chrome may use another Javascript Engine.

| Browser | Javascript Engine |
| Chrome | V8 JS Engine |
| Firefox | SpiderMonkey |
| IE, Edge | Chakra |

NodeJS

You can use "thesyntax of Javascript" to write code snippets to connect to a database. The V8 JS Engine will parse your Javascript code and interprets it into computer code for execution. Of course, such code snippet is not for execution at the client side. it is used at the server side. Thus, an ability is opened, you can use "theJavascript syntax" to write server-side web applications instead of using PHP or Java.

Javascript code

| const mysql = require('mysql');const connection = mysql.createConnection({host: 'localhost',user: 'user',password: 'password',database: 'database name'});connection.connect((err) => {if (err) throw err;console.log('Connected!');}); |

and NodeJS was born. The V8 Javascript Engine is one of components of the NodeJS. Below is the architecture image of the NodeJS:

NodeJs Javascript Library

| ![](image_rsrc21S.jpg) |

In short, the NodeJS may replace PHP, Java to build Server-side web applications. Instead of writing code by PHP, Java you use the syntax of Javascript.

So, What is NodeJS

The NodeJS is JavaScript Runtime Environment outside browser. The NodeJS also consists of other components and libraries so that it may operate like a Web Application Server.

Important note: The NodeJS is not the extended language of Javascript.

Chapter 2 :

Install Atom Editor

What is Atom software

Atom is a text (and source code) editor free of charge. The open source code supports operating systems such as Linux, Mac OS, Windows. It supports plugins to program with the NodeJS and embed Git-Control, which is developed by GitHub.

Atom is evaluated as text editing (and source code) software with a modern, easy-to-use interface and outstanding features compared to similar pieces of software.

The languages are supported by the Atom:

C/C++, C#, Clojure, CSS, CoffeeScript, GitHub Flavored Markdown, Go, Git, HTML, JavaScript, Java, JSON, Julia, Less, Make, Mustache, Objective-C, PHP, Perl, Property List (Apple), Python, Ruby on Rails, Ruby, Sass, Shell script, Scala, SQL, TOML, XML, YAML

| ![](image_rsrc21T.jpg) |

Download Atom

To download the Atom, let's visit its home page at the following address. it is noted that the Atom supports all of three kinds of operating systems: Windows, Mac OS, and Linux. If you use Windows, ensure that your operating system is Windows 7 64bit or later.

*   https://atom.io/

| ![](image_rsrc21U.jpg) |

After downloading successfully, you have a file with capacity of approximately 150MB.

| ![](image_rsrc21V.jpg) |

OK, after finishing downloading and installing the Atom, this is the interface image of the Atom:

| ![](image_rsrc21W.jpg) |

Chapter 3 :

Install NodeJS on Windows

Download NodeJS

To download NodeJS, you need to access to the following address:

*   https://nodejs.org/en/download/

| ![](image_rsrc21X.jpg) |

After downloading successfully, you have a file.

| ![](image_rsrc21Y.jpg) |

Install NodeJS

The installation of NodeJS on Windows is very simple. Accept default options and press "Next .. Next" until final step.

| ![](image_rsrc21Z.jpg) |

| ![](image_rsrc220.jpg) |

| ![](image_rsrc221.jpg) |

By default, NPM software is also installed in your system. This is a piece of software that manages Javascript libraries.

| ![](image_rsrc222.jpg) |

| ![](image_rsrc223.jpg) |
| ![](image_rsrc224.jpg) |

Check and configure

OK, in the above step, we have downloaded and installed the NodeJS successfully. Now, you need to check installation results and configure the NodeJS.

Open the CMD window and execute the following command to inspect the version of the NodeJS and the NPM:

| node -vnpm -v |

| ![](image_rsrc225.jpg) |

Chapter 4 :

What is NPM

What is NPM

NPM stands for Node Package Manager, which is a (program) tool managing Javascript programming libraries for Node.js. This tool is actually necessary for the open source world. In the Javascript community, developers share hundreds of thousands of code snippets that help new projects avoid rewriting basic components, programming libraries or even frameworks. Each of these code snippets may depend on many other open source codes. Fortunately, library management tools are born. If not, it will take a lot of effort to manage these libraries.

NPM is basically similar to Maven. The difference here is that the NPM manages Javascript libraries while the Maven manages Java libraries.

A piece of software similar to the NPM is Yarn, developed by Facebook, with outstanding features is emerging as an alternative to the NPM. In the same situation, Java library management software is Gradle, with its outstanding features, which is gradually replacing Maven.

Features of the NPM

To be able to run NPM software, your system needs installing NodeJS. The NPM software is built in NodeJS installer, therefore, when you have finished installing the NodeJS, you will have both of them.

After the NPM has been installed on your computer, you can examine its version:

| npm –v |

| ![](image_rsrc226.jpg) |

Because the NPM is a piece of software installed on your computer, you can use it to install Javascript libraries from the Internet. To install a library, it is necessary to open only CMD window and execute the command as below:

| npm install <package name> |

| npm install vue |

And you can use Vue.js in your Javascript code:

javascript

| var Vue = require('vue'); |

Chapter 5 :

NodeJS

Create a NodeJS project

First of all, you need to create a directory named MyProject, or a name that you want.

| ![](image_rsrc227.jpg) |

Open CMD and CD windows to the directory just created by you. After that run the following command so that NPM creates project for you.

| npm init |

| ![](image_rsrc228.jpg) |

Accept default options and press "Enter" until completion.

| ![](image_rsrc229.jpg) |

A file with the name of package.json has been created on your project.

| ![](image_rsrc22A.jpg) |

There are some library packages necessary for your project, and you need to install it with the support of NPM:

Express

Express.js (or simply Express) means a Web Application Framework for the NodeJS. It provides a set of strong features to web and mobile applications.

Ejs

EJS stands for "Embedded JavaScript templating", which is a library, used to parse ejs files and create HTML to return to client (browser).

| npm install express ejs |

| ![](image_rsrc22B.jpg) |

After the installation finishes, you can see changes on your project:

| ![](image_rsrc22C.jpg) |

Create structure for project

In the above step, we have created a project by command. Now we will open this project by a more visual tool. Here, I use Atom editor (The software which I advise you to install in the above step).

*   File/Add Project Folder

| ![](image_rsrc22D.jpg) |

OK, Project is opened on the Atom:

| ![](image_rsrc22E.jpg) |

On the project, create 2 sub-directories: public & views:

*   public: a directory containing all files which users can access, for example image, video,..
*   views: Your website will have a lot of pages, for example, home page, login page, ...This directory is the place containg all your pages.

| ![](image_rsrc22F.jpg) |

In views directory, we create 2 files:

*   homePage.ejs
*   testPage.ejs

| ![](image_rsrc22G.jpg) |

homePage.ejs

| <!DOCTYPE html><html lang="en" dir="ltr"><head><meta charset="utf-8"><title>Home</title></head><body><h1>This is Home Page</h1></body></html> |

testPage.ejs

| <!DOCTYPE html><html lang="en" dir="ltr"><head><meta charset="utf-8"><title>Test</title></head><body><h1>This is Test Page</h1></body></html> |

Next, create a file named index.js, and enter contents for this file. This is configuration file for your project:

| ![](image_rsrc22H.jpg) |

index.js

| var express = require("express");var app = express();app.use(express.static("public"));app.set("view engine", "ejs");app.set("views", "./views");app.listen(3000);app.get("/", function(request, response)  {response.render("homePage");});app.get("/test", function(request, response)  {response.render("testPage");}); |

OK, Now, it is time to explain the contents of the index.js above file.

| Code | Description |
| var express = require("express"); | ExpressJS means a Web Application Framework.This code line says that you want to use it. |
| var app = express(); | Create an Express object. |
| app.use(express.static("public")); | This code line tells Application Server that you want to use public directory to contain static data, users can access the files in this directory. |
| app.set("view engine", "ejs"); | This code line tells the Application Server that you want to use EJS library. It is a machinery to handle your page. The EJS will create HTML to return to user's browser. |
| app.set("views", "./views"); | This code line shows the Application Server the path to the directory containing your pages |
| app.listen(3000); | Your application will listen on port 3000 when it is deployed |
| app.get("/test", function(req, res) { ...}); | Define the path to access to a page. |

Run Application Server

Open the CMD, and CD window to go to the directory of your project and perform the following command to deploy your application.

| node index.js |

| ![](image_rsrc22J.jpg) |

The above command will start the Web Application Server, and deploy your application on this Web Server. At this moment, it is ready to serve the request sent from the client.

| ![](image_rsrc22K.jpg) |

Note: Not close the CMD window, because your Application Serser is running. Open the browser and visit the link:

*   http://localhost:3000/
*   http://localhost:3000/test

| ![](image_rsrc22M.jpg) |

What will take place at the Server when the user accesses the above address.

| ![](image_rsrc22N.jpg) |

Chapter 6 :

Create a Simple HTTP Server with NodeJS

The objective of post

In this post, I am going to show you how to create a very simple HTTP Server with NodeJS. And you can access static data sources such as HTML, Javascript, CSS, etc in the directory via http, for example:

*   http://localhost:8080/abc.html
*   http://localhost:8080/abc.js

Instead of accessing through file:///

*   file:///E:/webexamples/reactjs/abc.html
*   file:///E:/webexamples/reactjs/abc.js

| ![](image_rsrc22P.jpg) |

The question is why do you need a HTTP only to access static data sources.

If you want to learn ReactJS you will need an HTTP. Although ReactJS is just a Javascript library, and HTML files can be run directly in a browser. However, sometimes browser prevents the operations of the local Javascript files. It requires the Javascript file to come from one of the schemas: http, data, chrome, chrome-extension, https.

| ![](image_rsrc22R.jpg) |

Error Message!

| Failed to load file:///E:/webexamples/reactjs/hello-reactjs/person.jsx:Cross origin requests are only supported for protocol schemes: http, data, chrome, chrome-extension, https. |

Create NodeJS HTTP Server

Create an empty directory:

| ![](image_rsrc22S.jpg) |

Open the CMD window, and CD to the folder you created in the previous step.

| ![](image_rsrc22T.jpg) |

Run the following command to install http-server:

| npm install -g http-server |

| ![](image_rsrc22U.jpg) |

Start HTTP-Server:

| # Note: -c-1 to disable caching!!http-server -c-1 |

| ![](image_rsrc22V.jpg) |

Your HTTP Server has been started.it is listening at port 8080\. You can check it by visiting the following link:

*   http://localhost:8080/

| ![](image_rsrc22W.jpg) |

Create a HTML file in that directory, and you can access it via HTTP:

| ![](image_rsrc22X.jpg) |

| ![](image_rsrc22Y.jpg) |

Chapter 7 :

NodeJS Modules

What is NodeJS Module

Speaking simply, NodeJS Module is a Javascript library. It is a set of functions, objects and variables, which you can put into your applications to use. Using Module helps simplify writing code and manage it in your application. Normally, each module will be written in a separate file.

The NodeJS builds in quite many Modules. It has standard libraries for you to develop applications. Below is the list:

| Module | Description |
| assert | Provides a set of assertion tests |
| buffer | To handle binary data |
| child_process | To run a child process |
| cluster | To split a single Node process into multiple processes |
| crypto | To handle OpenSSL cryptographic functions |
| dgram | Provides implementation of UDP datagram sockets |
| dns | To do DNS lookups and name resolution functions |

| events | To handle events |
| fs | To handle the file system |
| http | To make Node.js act as an HTTP server |
| https | To make Node.js act as an HTTPS server. |
| net | To create servers and clients |
| os | Provides information about the operation system |
| path | To handle file paths |
| querystring | To handle URL query strings |

| readline | To handle readable streams one line at the time |
| stream | To handle streaming data |
| string_decoder | To decode buffer objects into strings |
| timers | To execute a function after a given number of milliseconds |
| tls | To implement TLS and SSL protocols |
| tty | Provides classes used by a text terminal |
| url | To parse URL strings |
| util | To access utility functions |

To use a module, use require(moduleName) function. For example, http is a module that makes the NodeJS work like a HTTP Server.

On your NodeJS project, create a module-examples directory to contain the Javascript files which you practise in this lesson.

| ![](image_rsrc22Z.jpg) |

Create a file named http-example.js in the module-examples directory.

| ![](image_rsrc230.jpg) |

http-example.js

| var http = require("http");http.createServer(function(req, res)  {res.writeHead(200, {"Content-Type": "text/html"});res.write("<h1>Hello World</h1>");res.write("<h2>Hello Http</h2>");res.end();}).listen(8080) |

Open CMD and CD windows to go to your project directory, use the NodeJS to run the http-example.js file:

| node ./module-examples/http-example.js |

Open the browser and visit the path:

*   http://localhost:8080/

| ![](image_rsrc231.jpg) |

Create your Module

In the NodeJS, you can create a customized module. The Module is a Javascript file. please note to the position of this file because it affect the way for you to use it . You have 2 ways of choosing position of this file:

1   The Module file is put in the directory named

node_modules (subdirectory of the project). This is

encouraged position.

2   The Module file is put in one of your directories, not

node_modules.

| ![](image_rsrc232.jpg) |

The NodeJS advises you to place your Module files into the node_modules directory of the project. Wait for a minute, I am going to explain the reason why your module should be put in this directory.

The syntax for exporting something in your Javascript file.

| exports = something;// or:module.exports = something; |

my-first-module.js

First of all, create a my-first-module.js file in the node_modules directory and the test-my-first-module.js file in another directory.

| ![](image_rsrc233.jpg) |

In this example, the my-first-module.js file has a lot of functions but I only export"sum" function.

node_modules/my-first-module.js

| subtract = function(a, b)  {return a - b;}sum = function (a, b)  {return a + b;}module.exports = sum; |

| ![](image_rsrc234.jpg) |

module-examples/test-my-first-module.js

| var sum = require("my-first-module.js");console.log("Sum 100 and 150");var c = sum(100, 150);console.log("Value = " + c); |

Run the above example:

| node ./module-examples/test-my-first-module.js |

Chapter 8 :

The concept of Callback in NodeJS

What is Callback

To explain what the Callback is, let's see a situation as follows:

You come to a shop to buy a something you like. The shop staff tells you that the item is out of stock now. You leave the phone number and ask them to call back immediately after the goods is available. Then you can go out or do a job and do not need to care about the shop anymore, until you get a phone call notifying of the item asked by you from the shop.

| ![](image_rsrc235.jpg) |

NodeJS server can receive many requests from many users. Therefore to improve serviceability, all APIs of the NodeJS are designed to support Callback. The "callback" is a function that will be called when the NodeJs completes a specific task.

NodeJS Callback

In the NodeJS, APIs is designed to support the Callback. Assume that you are writing a program to read 2 files. To do this you use the fs module, which gives you two functions such as readFile and readFileSync to read the file. We will learn about the differences between these two functions.

Blocking

The readFileSync is a function reading files synchronously,. Therefore, while this function is executing, it will block the program from executing next code lines.

blocking-example.js

| var fs = require("fs");// -----> Read file 1:console.log("\n");console.log("Read File 1");var data1 = fs.readFileSync('C:\\test\\file1.txt');console.log("- Data of file 1: ");console.log(data1.toString());// -----> Read file 2:console.log("\n");console.log("Read File 2");var data2 = fs.readFileSync('C:\\test\\file2.txt');console.log("- Data of file 2: ");console.log(data2.toString());console.log("\n");console.log("Program Ended"); |

Open CMD window and execute the blocking-example.js file

| node callback-examples/blocking-example.js |

Non Blocking

You should use readFile function to achieve better performance for the program. This function reads files asynchronously. It doesn't block the program executing the next code lines. In other words, the program does not wait for the function to complete. But when this function completes its task, it calls the Callback function.

| // Read a file Asynchronous.fs.readFile('C:\\test\\file1.txt', aCallbackFunction ); |

See the full example:

non-blocking-example.js

| var fs = require("fs");// A Callback function!function readFinishedFile1(err, data)  {if (err) console.log(err);console.log("- Data of file 1: ");console.log(data.toString());}// A Callback function!function readFinishedFile2(err, data)  {if (err) console.log(err);console.log("- Data of file 2: ");console.log(data.toString());}// -----> Read file 1:console.log("\n");console.log("Read File 1");fs.readFile('C:\\test\\file1.txt', readFinishedFile1);// -----> Read file 2:console.log("\n");console.log("Read File 2");fs.readFile('C:\\test\\file2.txt', readFinishedFile2);console.log("\n");console.log("Program Ended \n"); |

Open CMD window and run the non-blocking-example.js file:

| node callback-examples/non-blocking-example.js |

Chapter 9 :

Understanding Event Loop in NodeJS

NodeJS Event Loop Overview

NodeJS is a Single Thread application, which operates on a platform written by C++. This platform uses multi-thread to carry out tasks at the same time.

The following figure illustrates requests sent to the NodeJS server from the users side.

| ![](image_rsrc236.jpg) |

Each request from the users side is treated to be an event by the NodeJS. They is placed into an Event Queue. The NodeJS uses FIFO (First In First Out) principle, which means that the requests coming first will be handled first.

Event Loop

As an endless loop, it passes the requests to the thread Pool and each request is registered a Callback function. When a request is finished handling, the corresponding Callback function will be called to be executed.

Thread Pool

Being a program by C++ language, it supports multi threads. Therefore, herein, requests will be handled on different threads. The NodeJS also supports Multi Processes. This means that they can be executed on different cores.

| ![](image_rsrc237.jpg) |

When a request is finished handling. The NodeJS will call the Callback function (registered for this request) to execute it.

| ![](image_rsrc238.jpg) |

CONCLUSIONS:

First basic conclusion: If each connection to Server opens a Thread . It will take very much memory. This has been proven when you compare Apache and Nginx (two Web Servers deploying PHP applications). The Apache uses much more memory than the Nginx.

The NodeJS is similar to the Nginx in the fact that they use only a Single thread to receive connections from an user, and treat each request of the user as an event.

Second basic conclusion:I/O activities cost many resources of the system, therefore, the NodeJS manages use of I/O activities strictly. So you need to use only Callback when you execute the duties related to I/O.

Chapter 10 :

NodeJS EventEmitter

NodeJS EventEmitter

NodeJS supports events in applications very perfectly. Every action on a computer is an event. For example, when you read a file on hard drive. It means that you have to do two actions "open the file" and "close it" after finishing reading it, so here we have two " Open "&" Close " events. Based on events, you insert your codes to do something.

| var fs = require('fs');// Create a stream to read filevar rs = fs.createReadStream('C:/test/demo.txt');// The event 'open':rs.on('open', function() {console.log('File opened!');}); |

Module events provides you with an EventEmitter class, that is a central class in the NodeJS, assisting in defining an event, registering Listeners of this event, and emitting (emit) the event.

Listener

In the NodeJS, the Listener is a function. It will be called to execute when an event occurs. Probably, 0, 1 or many Listeners are being bound to such event.

For simplicity, look at the following illustration: a mouse and a mouse trap. An event is prepared to take place. When the event occurs (the cake is stolen), the mouse trap will perform its task. The mouse trap herein is a "Listener", which will work when the event happens.

Example of EventEmitter

Import Eventsmodule, and declare an EventEmitter object:

| // Import events modulevar events = require('events');// Create an EventEmitter objectvar eventEmitter = new events.EventEmitter(); |

Register Listeners (The functions will be called to execute when an event occurs).

| // Add Event ListenereventEmitter.addListener('bellRing', bellRingHandler1);// Add Event ListenereventEmitter.addListener('bellRing', bellRingHandler2); |

Emit the event:

| // Fire bellRing event!!eventEmitter.emit('bellRing', 'Jerry'); |

| ![](image_rsrc239.jpg) |

first-example.js

| // Import events modulevar events = require('events');// Create an eventEmitter objectvar eventEmitter = new events.EventEmitter();// A Listenervar bellRingHandler1 = function bellRingHandler1(who) {console.log("\n");console.log('The Bell Ringing..... (Handler 1)');console.log(" " + who + " was standing behind the door!");if(who == 'Jerry') {console.log(' Tom, help me!!');return;}console.log(" Welcome " + who);}// A Listenervar bellRingHandler2 = function bellRingHandler2(who) {console.log("\n");console.log('The Bell Ringing..... (Handler 2)');eventEmitter.emit("nobodyIsAtHome");}// A Listenervar nobodyIsAtHomeHandler = function nobodyIsAtHomeHandler()  {console.log("\n");console.log(" Sorry, Nobody is at home now, Please leave your message!")}// Add Event ListenerseventEmitter.addListener('bellRing', bellRingHandler1);eventEmitter.addListener('bellRing', bellRingHandler2);eventEmitter.addListener('nobodyIsAtHome', nobodyIsAtHomeHandler);// ----- Testing ------// Fire bellRing event!!eventEmitter.emit('bellRing', 'Jerry'); |

Run the example:

| node eventemitter-examples/first-example.js |

Chapter 11 :

Software  Installation

1   Introduction

2   Eclipse Installation

3   Jdk1.6 Installation And Configuring to Eclipse

4   Tomcat1.6 Installation And Configuring to Eclipse

5   MySql5.0 Installation

6   Eclipse Font Size Increase

1   Introduction

First          →    We will see

→    Software Installation and Configuration

Second     →    We will see

→    Complete Explanation of  Different Topics   

With Diagrams

2   Eclipse Installation

| ![](image_rsrc23A.jpg) |

Step 1 :

| ![](image_rsrc23B.jpg) |

Step 2 :

| ![](image_rsrc23C.jpg) |

Step 3 :

| ![](image_rsrc23D.jpg) |

Step 4 :

| ![](image_rsrc23E.jpg) |

Step 5 :

| ![](image_rsrc23F.jpg) |

Step 6 :

| ![](image_rsrc23G.jpg) |

Step 7 :

| ![](image_rsrc23H.jpg) |

Step 8 :

| ![](image_rsrc23J.jpg) |

Step 9 :

| ![](image_rsrc23K.jpg) |

Step 10 :

| ![](image_rsrc23M.jpg) |

3   Jdk1.6 Installation And Configuring to Eclipse

| ![](image_rsrc23N.jpg) |

Step 1 :

| ![](image_rsrc23P.jpg) |

Step 2 :

| ![](image_rsrc23R.jpg) |

Step 3 :

| ![](image_rsrc23S.jpg) |

Step 4 :

| ![](image_rsrc23T.jpg) |

Step 5 :

| ![](image_rsrc23U.jpg) |

Step 6 :

| ![](image_rsrc23V.jpg) |

Step 7 :

| ![](image_rsrc23W.jpg) |

Step 8 :

| ![](image_rsrc23X.jpg) |

Step 9 :

| ![](image_rsrc23Y.jpg) |

Step 10 :

| ![](image_rsrc23Z.jpg) |

Step 11 :

| ![](image_rsrc240.jpg) |

Step 12 :

| ![](image_rsrc241.jpg) |

Step 13 :

| ![](image_rsrc242.jpg) |

Step 14 :

| ![](image_rsrc243.jpg) |

Step 15 :

| ![](image_rsrc244.jpg) |

4   Tomcat1.6 Installation And Configuring to Eclipse

Step 1 :

| ![](image_rsrc245.jpg) |

Step 2 :

| ![](image_rsrc246.jpg) |

Step 3 :

| ![](image_rsrc247.jpg) |

Step 4 :

| ![](image_rsrc248.jpg) |

Step 5 :

| ![](image_rsrc249.jpg) |

Step 6 :

| ![](image_rsrc24A.jpg) |

Step 7 :

| ![](image_rsrc24B.jpg) |

Step 8 :

| ![](image_rsrc24C.jpg) |

Step 9 :

| ![](image_rsrc24D.jpg) |

Step 10 :

| ![](image_rsrc24E.jpg) |

Step 11 :

| ![](image_rsrc24F.jpg) |

Step 12 :

| ![](image_rsrc24G.jpg) |

Step 13 :

| ![](image_rsrc24H.jpg) |

Step 14 :

| ![](image_rsrc24J.jpg) |

Step 15 :

| ![](image_rsrc24K.jpg) |

Step 16 :

| ![](image_rsrc24M.jpg) |

Step 17 :

| ![](image_rsrc24N.jpg) |

Step 18 :

| ![](image_rsrc24P.jpg) |

Step 19 :

| ![](image_rsrc24R.jpg) |

Step 20 :

| ![](image_rsrc24S.jpg) |

5   MySql5.0 Installation

Here we will learn Step by Step Installation process.

Simply follow the steps.

| ![](image_rsrc24T.jpg) |

Step 1 :

| ![](image_rsrc24U.jpg) |

Step 2 :

| ![](image_rsrc24V.jpg) |

Step 3 :

| ![](image_rsrc24W.jpg) |

Step 4 :

| ![](image_rsrc24X.jpg) |

Step 5 :

| ![](image_rsrc24Y.jpg) |

Step 6 :

| ![](image_rsrc24Z.jpg) |

Step 7 :

| ![](image_rsrc250.jpg) |

Step 8 :

| ![](image_rsrc251.jpg) |

Step 9 :

| ![](image_rsrc252.jpg) |

Step 10 :

| ![](image_rsrc253.jpg) |

Step 11 :

| ![](image_rsrc254.jpg) |

Step 12 :

| ![](image_rsrc255.jpg) |

Step 13 :

| ![](image_rsrc256.jpg) |

Step 14 :

| ![](image_rsrc257.jpg) |

Step 15 :

| ![](image_rsrc258.jpg) |

Step 16 :

| ![](image_rsrc259.jpg) |

Step 17 :

| ![](image_rsrc25A.jpg) |

Step 18 :

| ![](image_rsrc25B.jpg) |

Step 19 :

| ![](image_rsrc25C.jpg) |

Step 20 :

| ![](image_rsrc25D.jpg) |

Step 21 :

| ![](image_rsrc25E.jpg) |

Step 22 :

| ![](image_rsrc25F.jpg) |

Step 23 :

| ![](image_rsrc25G.jpg) |

Step 24 :

| ![](image_rsrc25H.jpg) |

Step 25 :

| ![](image_rsrc25J.jpg) |

Step 26 :

| ![](image_rsrc25K.jpg) |

Step 27 :

| ![](image_rsrc25M.jpg) |

Step 28 :

| ![](image_rsrc25N.jpg) |

Step 29 :

| ![](image_rsrc25P.jpg) |

6   Eclipse Font Size Increase

Step 1 :

| ![](image_rsrc25R.jpg) |

Step 2 :

| ![](image_rsrc25S.jpg) |

Step 3 :

| ![](image_rsrc25T.jpg) |

Step 4 :

| ![](image_rsrc25U.jpg) |

Step 5 :

| ![](image_rsrc25V.jpg) |

Step 6 :

| ![](image_rsrc25W.jpg) |