![](Images/default_cover.jpeg)

![](Images/default_cover.jpeg)

## Your First Week With Node.js, 2nd Edition

Copyright © 2020 SitePoint Pty. Ltd.

Ebook ISBN: 978-1-925836-38-7

*   **Product Manager:** Simon Mackie
*   **Project Editor Editor:** James Hibbard
*   **English Editor:** Ralph Mason
*   **Cover Designer:** Alex Walker

## Notice of Rights

All rights reserved. No part of this book may be reproduced, stored in a retrieval system or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical articles or reviews.

## Notice of Liability

The author and publisher have made every effort to ensure the accuracy of the information herein. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors and SitePoint Pty. Ltd., nor its dealers or distributors will be held liable for any damages to be caused either directly or indirectly by the instructions contained in this book, or by the software or hardware products described herein.

## Trademark Notice

Rather than indicating every occurrence of a trademarked name as such, this book uses the names only in an editorial fashion and to the benefit of the trademark owner with no intention of infringement of the trademark.

![SitePoint logo](Images/sitepoint-logo-2012.png)
Published by SitePoint Pty. Ltd.

Level 1, 110 Johnston St, Fitzroy
VIC Australia 3065
Web: www.sitepoint.com
Email: books@sitepoint.com

## About SitePoint

SitePoint specializes in publishing fun, practical, and easy-to-understand content for web professionals. Visit [http://www.sitepoint.com/](http://www.sitepoint.com/) to access our blogs, books, newsletters, articles, and community forums. You’ll find a stack of information on JavaScript, PHP, design, and more.

## About Craig Buckler

[Craig](https://craigbuckler.com/) is a freelance developer, author, and speaker who never shuts up about the web.

He started coding in the 1980s when applications had to squeeze into a few kilobytes of RAM. His passion for the Web was ignited in the mid 1990s when 28K modems were typical and 100KB pages were considered extravagant.

Over the past decade, Craig has written 1,200 tutorials for SitePoint as web standards evolved. Despite living in a technically wondrous future, he has never forgotten what could be achieved with modest resources.

# Preface

While there have been quite a few attempts to get JavaScript working as a server-side language, Node.js (frequently just called Node) has been the first environment that's gained any traction. It's now used by companies such as Netflix, Uber and Paypal to power their web apps. Node allows for blazingly fast performance; thanks to its event loop model, common tasks like network connection and database I/O can be executed very quickly indeed.

From a beginner's point of view, one of Node's obvious advantages is that it uses JavaScript, a ubiquitous language that many developers are comfortable with. If you can write JavaScript for the client-side, writing server-side applications with Node should not be too much of a stretch for you.

In this book, we'll offer a beginner's introduction to Node and its related technologies, and get you under way writing your first Node applications.

## Who Should Read This Book?

This book is for web developers who want to make a start using Node. It's assumed that you have a good understanding of JavaScript.

## Conventions Used

### Code Samples

Code in this book is displayed using a fixed-width font, like so:

```
 <h1>A Perfect Summer's Day</h1>
<p>It was a lovely day for a walk in the park.
The birds were singing and the kids were all back at school.</p> 
```

Where existing code is required for context, rather than repeat all of it, ⋮ will be displayed:

```
 function animate() {
    ⋮
new_variable = "Hello";
}
```

Some lines of code should be entered on one line, but we’ve had to wrap them because of page constraints. An ➥ indicates a line break that exists for formatting purposes only, and should be ignored:

```
 URL.open("http://www.sitepoint.com/responsive-web-
➥design-real-user-testing/?responsive1");
```

You’ll notice that we’ve used certain layout styles throughout this book to signify different types of information. Look out for the following items.

### Tips, Notes, and Warnings

#### Hey, You!

Tips provide helpful little pointers.

#### Ahem, Excuse Me ...

Notes are useful asides that are related—but not critical—to the topic at hand. Think of them as extra tidbits of information.

#### Make Sure You Always ...

... pay attention to these important points.

#### Watch Out!

Warnings highlight any gotchas that are likely to trip you up along the way.

## Supplementary Materials

*   [https://www.sitepoint.com/community/](https://www.sitepoint.com/community/) are SitePoint’s forums, for help on any tricky problems.
*   **books@sitepoint.com** is our email address, should you need to contact us to report a problem, or for any other reason.

# Chapter 1: What Is Node and When Should I Use It?

### by James Hibbard

So you’ve heard of Node.js, but aren’t quite sure what it is or where it fits into your development workflow. Or maybe you’ve heard people singing Node’s praises and now you’re wondering if it’s something you need to learn. Perhaps you’re familiar with another back-end technology and want to find out what’s different about Node.

If that sounds like you, then keep reading. In this guide, I’ll take a beginner-friendly, high-level look at Node.js and its main paradigms. I’ll examine Node’s main use cases, as well as the current state of the Node landscape, and offer you a wide range of jumping off points (for further reading) along the way.

#### “Node” or “Node.js”?

Please note that, throughout the guide, I’ll use “Node” and “Node.js” interchangeably.

## What Is Node.js?

There are plenty of definitions to be found online. Let’s take a look at a couple of the more popular ones. This is [what the project’s home page has to say](https://nodejs.org/en/):

> Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

And this is [what Stack Overflow has to offer](https://stackoverflow.com/tags/node.js/info):

> Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

Hmmm, “event-based”, “non-blocking”, “asynchronous I/O”—that’s quite a lot to digest in one go. So let’s approach this from a different angle and begin by focusing on the other detail that both descriptions mention—the V8 JavaScript engine.

### Node Is Built on Google Chrome’s V8 JavaScript Engine

[The V8 engine](https://v8.dev/) is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute.

However, when we say that Node is built on the V8 engine, we don’t mean that Node programs are executed in a browser. They aren’t. Rather, the creator of Node ([Ryan Dahl](https://en.wikipedia.org/wiki/Ryan_Dahl)) took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

## How Do I Install Node.js?

In this next section, we’ll install Node and write a couple of simple programs. We’ll also look at [npm](https://www.npmjs.com/), a package manager that comes bundled with Node.

### Node Binaries vs Version Manager

Many websites will recommend that you head to [the official Node download page](https://nodejs.org/en/download/) and grab the Node binaries for your system. While that works, I would suggest that you use a version manager instead. This is a program that allows you to install multiple versions of Node and switch between them at will. There are various advantages to using a version manager. For example, it negates potential permission issues when using Node with npm and lets you set a Node version on a per-project basis.

If you fancy going the version manager route, please consult our quick tip: [Install Multiple Versions of Node.js using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). Otherwise, grab the correct binaries for your system from the link above and install those.

### “Hello, World!” the Node.js Way

You can check that Node is installed on your system by opening a terminal and typing `node -v`. If all has gone well, you should see something like `v12.14.1` displayed. This is the current LTS version at the time of writing.

Next, create a new file `hello.js` and copy in the following code:

```
console.log("Hello, World!");
```

This uses Node’s [built-in console module](https://nodejs.org/api/console.html#console_console) to display a message in a terminal window. To run the example, enter the following command:

```
node hello.js
```

If Node.js is configured properly, “Hello, World!” will be displayed.

### Node.js Has Excellent Support for Modern JavaScript

As can be seen on this [compatibility table](https://node.green/), Node has excellent support for ECMAScript 2015 (ES6) and beyond. As you’re only targeting one runtime (a specific version of the V8 engine), this means that you can write your JavaScript using the latest and most modern syntax. It also means that you don’t generally have to worry about compatibility issues—as you would if you were writing JavaScript that would run in different browsers.

To illustrate the point, here’s a second program that makes use of several modern JavaScript features, such as tagged [template literals](https://www.sitepoint.com/understanding-ecmascript-6-template-strings/), [object destructuring](https://www.sitepoint.com/preparing-ecmascript-6-destructuring-assignment/) and [Array.prototype.flatMap()](https://thecodebarbarian.com/whats-new-in-es2019-flat-flatmap-catch.html#arrayflat-and-arrayflatmap):

```
function upcase(strings, ...values) {
  return values.map(name => name[0].toUpperCase() + name.slice(1))
    .join(' ') + strings[2];
}

const person = {
  first: 'brendan',
  last: 'eich',
  age: 56,
  position: 'CEO of Brave Software',
};

const { first, last } = person;
const emoticon = [ ['┌', '('], ['˘', '⌣'], ['˘', ')', 'ʃ'] ];

console.log(
  upcase`${first} ${last} is the creator of JavaScript! ` + emoticon.flat().join('')
);
```

Save this code to a file called `index.js` and run it from your terminal using the command `node index.js`. You should see `Brendan Eich is the creator of JavaScript! ┌(˘⌣˘)ʃ` output to the terminal.

## Introducing npm, the JavaScript Package Manager

As I mentioned earlier, Node comes bundled with a package manager called npm. To check which version you have installed on your system, type `npm -v`.

In addition to being *the* package manager for JavaScript, npm is also the world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. Let’s take a quick look at how we would use npm to install a package.

### Installing a Package Globally

Open your terminal and type the following:

```
npm install -g jshint
```

This will install the [jshint package](https://www.npmjs.com/package/jshint) globally on your system. We can use it to lint the `index.js` file from the previous example:

```
jshint index.js
```

You should now see a number of ES6-related errors. If you want to fix them up, add `/* jshint esversion: 6 */` to the top of the `index.js` file, re-run the command and linting should pass.

If you’d like a refresher on linting, see [A Comparison of JavaScript Linting Tools](https://www.sitepoint.com/comparison-javascript-linting-tools/).

### Installing a Package Locally

We can also install packages locally to a project, as opposed to globally, on our system. Create a `test` folder and open a terminal in that directory. Next type this:

```
npm init -y
```

This will create and auto-populate a `package.json` file in the same folder. Next, use npm to install the [lodash package](https://www.npmjs.com/package/lodash) and save it as a project dependency:

```
npm install lodash --save
```

Create a file named `test.js` and add the following:

```
const _ = require('lodash');

const arr = [0, 1, false, 2, '', 3];
console.log(_.compact(arr));
```

Finally, run the script using `node test.js`. You should see `[ 1, 2, 3 ]` output to the terminal.

### Working with the `package.json` File

If you look at the contents of the `test` directory, you’ll notice a folder entitled `node_modules`. This is where npm has saved lodash and any libraries that lodash depends on. The `node_modules` folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running `npm install` from within the project’s root.

If you open the `package.json` file, you’ll see lodash listed under the `dependencies` field. By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run.

If you’d like to find out more about npm, be sure to read our article [A Beginner’s Guide to npm—the Node Package Manager](https://www.sitepoint.com/beginners-guide-node-package-manager/).

## What Is Node.js Used For?

Now that we know what Node and npm are and how to install them, we can turn our attention to the first of their common uses: installing (via npm) and running (via Node) various build tools—designed to automate the process of developing a modern JavaScript application.

These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

We have a wide range of articles covering build tooling on SitePoint. Here’s a short selection of my favorites:

*   [A Beginner’s Guide to Webpack](https://www.sitepoint.com/webpack-beginner-guide/)
*   [Up and Running with ESLint—the Pluggable JavaScript Linter](https://www.sitepoint.com/up-and-running-with-eslint-the-pluggable-javascript-linter/)
*   [An Introduction to Gulp.js](https://www.sitepoint.com/introduction-gulp-js/)
*   [Unit Test Your JavaScript Using Mocha and Chai](https://www.sitepoint.com/unit-test-javascript-mocha-chai/)

And if you want to start developing apps with any modern JavaScript framework (for example, React or Angular), you’ll be expected to have a working knowledge of Node and npm (or maybe [Yarn](https://www.sitepoint.com/yarn-vs-npm/)). This isn’t because you need a Node back end to run these frameworks. You don’t. Rather, it’s because these frameworks (and many, many related packages) are all available via npm and rely on Node to create a sensible development environment in which they can run.

If you’re interested in finding out what role Node plays in a modern JavaScript app, read [The Anatomy of a Modern JavaScript Application](https://www.sitepoint.com/anatomy-of-a-modern-javascript-application/).

## Node.js Lets Us Run JavaScript on the Server

Next we come to one of the biggest use cases for Node.js—running JavaScript on the server. This isn’t a new concept, and was first attempted by Netscape way back in 1994\. Node.js, however, is the first implementation to gain any real traction, and it provides some unique benefits, compared to traditional languages. Node now plays a critical role in the technology stack of [many high-profile companies](https://www.netguru.co/blog/top-companies-used-nodejs-production). Let’s have a look at what those benefits are.

### The Node.js Execution Model

In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request. In a language such as PHP or Ruby, any subsequent I/O operations (for example, interacting with a database) block the execution of your code until the operation has completed. That is, the server has to wait for the database lookup to complete before it can move on to processing the result. If new requests come in while this is happening, the server will spawn new threads to deal with them. This is potentially inefficient, as a large number of threads can cause a system to become sluggish—and, in the worst case, for the site to go down. The most common way to support more connections is to add more servers.

Node.js, however, is single-threaded. It’s also **event-driven**, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in (one kind of event) the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished (another kind of event), the server will execute the callback and continue working on the original request. Under the hood, Node uses the [libuv](https://github.com/libuv/libuv) library to implement this asynchronous (that is, non-blocking) behavior.

Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. Node.js even has [a built-in module](https://nodejs.org/api/cluster.html) to help you implement a cloning strategy on a single server.

The following image depicts Node’s execution model:

![Node’s execution model](Images/node_event_loop.png)

*Image source: Introduction to Node.js, by Prof. Christian Maderazo and James Santos.*

Or, if you prefer videos, check out this awesome talk: [What the heck is the event loop anyway?](https://www.youtube.com/watch?v=8aGhZQkoFbQ) It’s not Node-specific, but does a great job of explaining the concept.

### Are There Any Downsides?

The fact that Node runs in a single thread does impose some limitations. For example, blocking I/O calls should be avoided, [CPU-intensive operations should be handed off to a worker thread](https://blog.logrocket.com/node-js-multithreading-what-are-worker-threads-and-why-do-they-matter-48ab102f8b10/), and errors should always be handled correctly for fear of crashing the entire process.

Some developers also dislike the callback-based style of coding that JavaScript imposes (so much so that there’s even [a site dedicated to the horrors of writing asynchronous JavaScript](http://callbackhell.com/)). But with the arrival of native Promises, followed closely by async await, [flow control in modern JavaScript](https://www.sitepoint.com/flow-control-callbacks-promises-async-await/) has become easier than it ever was.

### “Hello, World!”—Server Version

Let’s have a quick look at a "Hello, World!" example HTTP server:

```
const http = require('http');

http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
}).listen(3000);

console.log('Server running on http://localhost:3000');
```

To run this, copy the code into a file named `hello-world-server.js` and run it using `node hello-world-server.js`. Open up a browser and navigate to [http://localhost:3000](http://localhost:3000) to see “Hello, World!” displayed in the browser.

Now let’s have a look at the code.

We start by requiring Node’s native [HTTP module](https://nodejs.org/api/http.html). We then use its [createServer](https://nodejs.org/api/http.html#http_http_createserver_options_requestlistener) method to create a new web server object, to which we pass an anonymous function. This function will be invoked for every new connection that’s made to the server.

The anonymous function is called with two arguments (`request` and `response`). These contain the request from the user and the response, which we use to send back a 200 HTTP status code, along with our “Hello World!” message.

Finally, we tell the server to listen for incoming requests on port 3000, and output a message to the terminal to let us know it’s running.

Obviously, there’s a lot more to creating even a simple server in Node (for example, it’s important to handle errors correctly), so I’d advise you to [check the documentation](https://nodejs.org/en/docs/guides/anatomy-of-an-http-transaction/).

## What Kind of Apps Is Node.js Suited To?

Node is particularly suited to building applications that require some form of real-time interaction or collaboration—for example, chat sites, or apps such as [Codeshare](https://codeshare.io/), where you can watch a document being edited live by someone else. It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven (such as those needing to perform operations on a database), or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded. If this real-time aspect of Node is something you’d like to look into more, check out our tutorial on [Building a Real-time Chat App](https://www.sitepoint.com/building-real-time-chat-app-sails-js/).

Yet saying this, not everyone is going to be building the next Trello or the next Google Docs, and really, there’s no reason that you can’t use Node to build a simple CRUD app. However, if you follow this route, you’ll soon find out that Node is pretty bare-bones and that the way you build and structure the app is left very much up to you. There are various frameworks you can use to reduce the boilerplate, with [Express](http://expressjs.com) having established itself as the front runner. Yet even a solution such as Express is minimal, meaning that if you want to do anything slightly out of the ordinary, you’ll need to pull in additional modules from npm. This is in stark contrast to frameworks such as Rails or Laravel, which come with a lot of functionality out of the box.

## What Are the Advantages of Node.js?

Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server—as well as in the browser—is that your brain no longer needs to switch modes. You can do everything in the same language, which, as a developer, makes you more productive (and hopefully, happier). For example, you can easily share code between the server and the client.

Another of Node’s big pluses is that it speaks JSON. JSON is probably the most important data exchange format on the Web, and the lingua franca for interacting with object databases (such as MongoDB). JSON is ideally suited for consumption by a JavaScript program, meaning that when you’re working with Node, data can flow neatly between layers without the need for reformatting. You can have one syntax from browser to server to database.

Finally, JavaScript is ubiquitous: most of us are familiar with JavaScript, or have used it at some point. This means that transitioning to Node development is potentially easier than to other server-side languages. To quote Craig Buckler in his [Node vs PHP Smackdown](https://www.sitepoint.com/sitepoint-smackdown-php-vs-node-js/), JavaScript might remain [the world’s most misunderstood language](http://www.crockford.com/javascript/javascript.html)—but, once the concepts click, it makes other languages seem cumbersome.

## Other Uses of Node

And it doesn’t stop at the server. There are many other exciting and varied uses of Node.js!

For example [it can be used as a scripting language](https://www.sitepoint.com/shell-scripts-javascript/) to automate repetitive or error prone tasks on your PC. It can also be used to write your own command line tool, such as this [Yeoman-Style generator](https://www.sitepoint.com/scaffolding-tool-caporal-js/) to scaffold out new projects.

Node.js can also can be used to [build cross-platform desktop apps](https://www.sitepoint.com/premium/books/build-a-native-desktop-gif-search-app-using-nodegui/read/) and even to [create your own robots](https://www.sitepoint.com/an-introduction-to-nodebots/). What’s not to love?

## Conclusion

JavaScript is everywhere, and Node is a vast and expansive subject. Nonetheless, I hope that in this guide I’ve offered you the beginner-friendly, high-level look at Node.js and its main paradigms that I promised at the beginning. I also hope that when you re-read the definitions we looked at previously, things will make a lot more sense.

> Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

# Chapter 2: Build a Simple Page Counter Service with Node.js

### by Craig Buckler

You understand what Node.js is. You’ve read what it can do. Starting work on a real project is the best way to progress your Node.js knowhow!

This tutorial describes how to build a simple page counter service. Any page can use it to display “this has been viewed X times” just like HTML developers did twenty years ago.

The service will be developed using the standard [Node.js APIs](https://nodejs.org/dist/latest/docs/api/) to demonstrate concepts such as HTTP handling, URL parsing, storage, and file manipulation. No pre-built, third-party modules or applications will harmed in the production of this project: *we’re on our own!*

## Prerequisites

Download and [install Node.js](https://nodejs.org/en/download/) on a platform of your choice. Windows, macOS, and Linux ([package manager](https://nodejs.org/en/download/package-manager/) or [Snap package](https://snapcraft.io/node)) are all supported. You can also [use a version manager such as nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/). The latest LTS (even-numbered) Node release is a good choice.

A decent text editor will make coding more efficient and pleasurable. Popular options include [VS Code](https://code.visualstudio.com/), [Atom](https://atom.io/), [Sublime Text](https://www.sublimetext.com/), and [Brackets](http://brackets.io/).

You’ll be making extensive use of the command line, so ensure you know how to launch your terminal application. To get started, install [nodemon](https://nodemon.io/) and [small-static-server](https://www.npmjs.com/package/small-static-server) as global `npm` packages:

```
npm install -g nodemon small-static-server
```

*   `nodemon` can be used to launch and restart Node.js applications whenever source code is changed
*   `ss` can be used in any directory to launch a static, file-based web server

Finally, a little JavaScript knowledge will go a long way!

## Project Overview

During development, our Node.js web server will run at `http://localhost:3000/`. Any page can use it to display a counter by adding a snippet of HTML. For example:

```
<script src="http://localhost:3000/counter.js"></script>
```

In this scenario, the following things happen:

1.  The server finds the calling page’s URL by examining the `referer` in the HTTP request header.
2.  The server extracts the referrer’s protocol, host, and path (query strings are ignored) and generates a 32-character MD5 hash. This is more efficient than retaining a long URL.
3.  A counter for the URL hash is incremented.
4.  The server responds with a JavaScript `document.write()` to display the counter on the page.

`document.write()` is simple but can affect performance, because it blocks browser rendering until the full response is received. Three other counter options are also provided:

*   [An SVG counter](https://github.com/sitepoint-editors/pagehit-ram/blob/master/testpages/page-svg.html) which returns a generated image with the counter contained in a `<text>` block:

    ```
     <img src="http://localhost:3000/counter.svg" />
    ```

*   [A deferred script counter](https://github.com/sitepoint-editors/pagehit-ram/blob/master/testpages/page-jsdefer.html) which downloads in the background and updates the DOM after it has fully loaded:

    ```
     <script src="http://localhost:3000/counter-defer.js" defer></script>
    ```

*   An Ajax request can be made to `http://localhost:3000/counter.json`. This returns a `{"counter":X}` JSON response which can be parsed and used accordingly. (Here’s some [example code](https://github.com/sitepoint-editors/pagehit-ram/blob/master/testpages/page-jsajax.html).)

All these options are fundamentally the same but return a different HTTP response.

## Page Hit v1.0: In-memory Storage

The full example code is available from [https://github.com/sitepoint-editors/pagehit-ram](https://github.com/sitepoint-editors/pagehit-ram).

The initial implementation stores counters using an in-memory JavaScript object.

This may seem unusual to those coming from other technologies. For example, a PHP application is called by a web server such as Apache or NGINX which launches the PHP runtime with the appropriate code file. Any (variable) state within that code is immediately lost once a response is returned.

Node.js typically launches an application which implements a web server and associated functionality. It’s therefore possible to create variables which can be accessed by all requests and are retained while the application continues to run.

### Step 0 (optional): Source Control

Source control applications such as [Git](https://git-scm.com/) help to back up code and manage revisions. Services including [GitHub](https://github.com/) and [BitBucket](https://bitbucket.org/) provide free space so you can create and clone a repository prior to writing any code.

Git is beyond the scope of this tutorial. You don’t have to use it, but you’ll be pleased you did!

#### Modules and .gitignore

Although this project doesn’t use third-party modules, always add a `node_modules/` line to your `.gitignore` file. Modules can be installed with `npm install`, so there’s no need to include them in your repository.

### Step 1: Initialization

Create a new folder (or clone a new repository) somewhere on your system, and run `npm init` to create a `package.json` project configuration file:

```
mkdir project1
cd project1
npm init
```

Press `Return` to accept the defaults or provide your own values. The final file contains JSON content such as:

```
{
  "name": "project1",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```

The `"scripts"` section provides command-line shortcuts. Change it in your editor:

```
"scripts": {
  "debug": "nodemon --trace-warnings ./index.js",
  "start": "node ./index.js",
  "test": "echo \"Error: no test specified\" && exit 1"
},
```

These scripts are used once the application is ready:

*   `npm start` runs the `start` script.
*   `npm run debug` runs the `debug` script. It uses nodemon to monitor file changes and reports full stack traces (useful for Promise debugging).

If you’d like to find out more about npm scripts and how they work, please consult [this tutorial](https://www.sitepoint.com/guide-to-npm-as-a-build-tool/).

### Step 2: Main File (`index.js`)

Node.js applications are launched from a single file which loads all modules and implements the core logic. It’s named `index.js` in this project, so create that file and add the following code:

```
'use strict';

const
  // default HTTP port
  port = 3000,

  // Node.js modules
  http = require('http'),
  url = require('url');

// new server
http.createServer((req, res) => {

  let uri = url.parse(req.url).pathname;
  res.end(uri);

}).listen(port);

console.log(`page hit web service running on port ${port}`);
```

Save the file and run it from the console using `npm run debug`. Wait for the message:

```
page hit web service running on port 3000
```

Then load [http://localhost:3000/hello/world](http://localhost:3000/hello/world) in your browser. You should see this:

```
/hello/world
```

The code uses functionality in two Node.js modules: [HTTP](https://nodejs.org/dist/latest/docs/api/http.html) and [URL](https://nodejs.org/dist/latest/docs/api/url.html). By default, Node.js uses CommonJS `require` statements to reference code, although [experimental support](https://nodejs.org/dist/latest/docs/api/esm.html) for [ES6 Modules](https://www.sitepoint.com/understanding-es6-modules/) is available.

The code uses [`http.createServer`](https://nodejs.org/dist/latest/docs/api/http.html#http_http_createserver_options_requestlistener). This returns an [`http.Server`](https://nodejs.org/dist/latest/docs/api/http.html#http_class_http_server) object which [listens](https://nodejs.org/dist/latest/docs/api/http.html#http_server_listen) for HTTP requests on port 3000 (defined as a constant).

A function is passed to `http.createServer` which is used to handle incoming requests. Two parameters are defined:

1.  `req`: an incoming [HTTP request](https://nodejs.org/dist/latest/docs/api/http.html#http_http_request_url_options_callback) information object
2.  `res`: an outgoing [HTTP response](https://nodejs.org/dist/latest/docs/api/http.html#http_class_http_serverresponse) object for returning data

The code extracts the full URL used from `req.url` (`http://localhost:3000/hello/world`) and passes it to the Node.js `URL` parsing module to extract the [`pathname`](https://nodejs.org/dist/latest/docs/api/url.html#url_urlobject_pathname) (`/hello/world`). The path is returned to the browser using [res.end()](https://nodejs.org/dist/latest/docs/api/http.html#http_response_end_data_encoding_callback).

Node.js server frameworks such as [Express.js](https://expressjs.com/) all act in a similar way. They parse an incoming request, route to code which can handle that request, and output a response.

Press `Ctrl`/`Cmd` + `C` to stop the Node.js application running.

### Step 3: Additional Modules

It’s practical to split code into other files with reusable chucks of related functionality. Create a new `lib` directory. You can use any name you prefer except for `node_modules`. Then add the following files within it:

*   `lib/httpreferrer.js`: exports a function which accepts an HTTP request object as a parameter. If this object has a referer set, the function will concatinate its `protocol`, `host` and `pathname` values, then return a 32-character MD5 hash of this string. The URL and [Crypto](https://nodejs.org/dist/latest/docs/api/crypto.html) modules are used:

    ```
     'use strict';

      const
        url = require('url'),
        crypto = require('crypto');

      module.exports = (req) => {

        let
          r = url.parse(req.headers.referer || ''),
          ref = r.href ? r.protocol + r.host + r.pathname : null;

        return ref ? crypto.createHash('md5').update(ref).digest('hex') : null;

      };
    ```

*   `lib/httpresponse.js`: exports a function which, when passed an object containing an HTTP response object, responds with the appropriate HTTP headers and content:

    ```
     'use strict';

      module.exports = ({
        res     = null,
        status  = 200,
        mime    = 'text/plain',
        content = ''
      }) => {

        res.writeHead(status, {
          'Access-Control-Allow-Origin': '*',
          'Content-Type': mime,
          'Cache-Control': 'must-revalidate, max-age=0',
          'Content-Length': Buffer.byteLength(content)
        });
        res.end(content);

      };
    ```

    Note that `Access-Control-Allow-Origin` is a [cross-origin resource sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) header which allows any page to use the page hit service.

*   `lib/pagehit.js`: exports a JavaScript class responsible for recording page hits in a `this.counter` property:

    ```
     const httpReferrer = require('./httpreferrer');

      module.exports = class {

        // initialize
        constructor() {

          // counter storage
          this.counter = {};

        }

        // increase URL counter
        count(req) {

          let hash = httpReferrer(req);
          if (!hash) return null;

          // define count default
          this.counter[ hash ] = this.counter[ hash ] || 0;

          // return incremented count
          return ++this.counter[ hash ];
        }

      };
    ```

When the `count()` method is passed an HTTP request object, it generates a hash (using `lib/httpreferrer.js` above). This is used to initialize and increment a property of the `this.counter` object which has its total count value returned.

We can now change `index.js` to use these modules and implement a page hit system:

```
'use strict';

const
  // default HTTP port
  port = 3000,

  // Node.js modules
  http = require('http'),
  url = require('url'),

  // page counter object
  pagehit = new (require('./lib/pagehit'))(),

  // HTTP response
  httpResponse = require('./lib/httpresponse');

// new server
http.createServer((req, res) => {

  // get referring page count
  let count = pagehit.count(req);

  // error: referring page not found
  if (!count) {

    httpResponse({ res, status: 400, content: 'No referrer' });
    return;

  }

  // send appropriate response
  let uri = url.parse(req.url).pathname;
  switch (uri) {

    // JavaScript document.write() counter
    case '/counter.js':

      httpResponse({
        res,
        mime: 'application/javascript',
        content: `document.write('<span class="pagecounter">${count}</span>');`
      });
      break;

    // error: invalid HTTP request
    default:
      httpResponse({ res, status: 404, content: 'Not found' });
      break;

  }

}).listen(port);

console.log(`page hit web service running on port ${port}`);
```

The line `pagehit = new (require('./lib/pagehit'))()` initializes an object from the `lib/pagehit.js` class, so the `count()` method can be called in the server function.

In situations where no referring page is found, `pagehit.count` returns `null`, so an HTTP 400 error response is returned.

The `switch()` statement handles routing. In this case, only requests to `/counter.js` are valid; a JavaScript `document.write()` statement is returned, which outputs the value of `count`.

The [full `index.js` code](https://github.com/sitepoint-editors/pagehit-ram/blob/master/index.js) provides additional responses for deferred JavaScript, Ajax, and SVG requests. All other requests trigger an HTTP 404 error.

Start the server again using `npm run debug`.

### Step 4: Test Page

A counter must be added to a test page to see the service in action. Create another folder, such as `testpages`, with a file named `page-jswrite.html` containing the following code:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>page hits</title>
</head>
<body>

<p>
  This page has been viewed
    <script src="http://localhost:3000/counter.js"></script>
  times.
</p>

</body>
</html>
```

Run `ss` from this folder in another terminal:

```
cd testpages
ss
```

Start a static file web server at `http://localhost:8888`:

```
server address: http://localhost:8888
root folder   : ./testpages/
```

Open [http://localhost:8888/page-jswrite.html](http://localhost:8888/page-jswrite.html) in your browser and watch the number of views increase as you refresh the page. You can use similar code in other HTML files so each have their own unique hit counter.

The full example code is available from [https://github.com/sitepoint-editors/pagehit-ram](https://github.com/sitepoint-editors/pagehit-ram).

Press `Ctrl`/`Cmd` + `C` in both terminals to stop the Node.js applications running.

## Page Hit v2.0: File Storage

Storing page counters in memory means they reset every time the Node.js application is restarted. The system can be improved by saving counters to a file at regular intervals. The following are steps for achieving this:

1.  When the application starts, if necessary, a `data` directory is created in the project. (If you’re using Git, add `data/` to your `.gitignore` file.)
2.  When a page counter is incremented, the server will trigger a save event after ten seconds. (This ensures saving occurs as a background task and is throttled during times of high load.)
3.  The `this.counter` property of `pagehit.js` is converted to a JSON string and saved to a file with a unique name (based on the current date/time).
4.  Once the file has successfully saved, all previously saved files are deleted from the `data` directory. These may be present if a user has manually added their own, or if older files haven’t been deleted (due to altered permissions, the process having crashed, and so on).
5.  On subsequent launches, the application looks for the most recent JSON file in the `data` directory and imports it into `this.counter`.

The page hit server doesn’t care how `lib/pagehit.js` is implemented as long as it can execute the `count()` method. We need only update that logic; changes to `index.js` are unnecessary.

The full example code is available from [https://github.com/sitepoint-editors/pagehit-file](https://github.com/sitepoint-editors/pagehit-file).

### Node.js File System API

Node.js provides an extensive [File System (`fs`) API](https://nodejs.org/dist/latest/docs/api/fs.html) which can manipulate, read, and write files and directories. Early releases of Node.js provided callback-based functions which are still available. For example:

```
// append the current date to a file
const fs = require('fs');

fs.appendFile('myfile.txt', new Date(), (err) => {

  if (err) {
    console.log('file update failed:', err);
  }
  else {
    console.log('file updated');
  }

});
```

Synchronous `'sync'` equivalents are also available. However, these are not Promise-based and block the entire Node.js process until they complete. They’re best avoided unless you’re writing application initialization functions for older releases of Node.js:

```
// append the current date to a file
const fs = require('fs');

try {
  fs.appendFileSync('myfile.txt', new Date());
  console.log('file updated');
}
catch (err) {
  console.log('file update failed:', err);
}
```

It’s possible to *Promisify* any file system function using [`util.promisify`](https://nodejs.org/dist/latest/docs/api/util.html#util_util_promisify_original):

```
const
  util = require('util'),
  fs = require('fs'),
  appendFilePromise = util.promisify(fs.appendFile);

appendFilePromise('myfile.txt', new Date())
  .then(() => console.log('file updated'))
  .catch(err => console.log('file update failed:', err));
```

However, this is no longer necessary in recent versions of Node.js, because [`fs.promises`](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fs_promises_api) provides Promise-based equivalents of all file system functions:

```
const
  fs = require('fs'),
  fsPromise = fs.promise;

fsPromise.appendFile('myfile.txt', new Date())
  .then(() => console.log('file updated'))
  .catch(err => console.log('file update failed:', err));
```

If you’d like a refresher on callbacks, Promises and async/await, check out our tutorial on [flow control in modern JavaScript](https://www.sitepoint.com/flow-control-callbacks-promises-async-await/).

### Step 1: File Utilities

To help save page counter data, we’re going to add a number of utility functions to [`lib/fileutil.js`](https://github.com/sitepoint-editors/pagehit-file/blob/master/lib/fileutil.js). Create this file and add a reference to the file system objects:

```
'use strict';

const
  fs = require('fs'),
  fsPromise = fs.promises;
```

An `info()` function returns an object containing information about a file or directory, such as its type, permissions, and creation time. It uses two `fs` functions:

*   [access(path, mode)](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fspromises_access_path_mode): can test for existence, read, and write permissions
*   [stat](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fspromises_stat_path_options): returns meta information including the type (file or directory) and creation time

```
// returns information about a file/folder
function info(fn) {

  const file = {
    path:   fn,
    exists: false,
    read:   false,
    write:  false,
    isFile: false,
    isDir:  false,
    time:   0
  };

  // If the accessibility checks are successful, Promises are resolved with no value
  return Promise.all([
    fsPromise.access(fn, fs.constants.F_OK),
    fsPromise.access(fn, fs.constants.R_OK),
    fsPromise.access(fn, fs.constants.W_OK)
  ])
    .then(fInfo => {

      file.exists = !fInfo[0];

      if (!file.exists) return file;
      else {

        file.read  = !fInfo[1];
        file.write = !fInfo[2];

        // Promise is resolved with the fs.Stats object for the given path
        return fsPromise.stat(fn)
          .then(fStat => {

            file.isFile = fStat.isFile();
            file.isDir  = fStat.isDirectory();
            file.time   = fStat.mtimeMs;
            return file;

          })
          .catch(() => file);

      }

    })
    .catch(() => file);

}
```

A `folderUsable()` function uses `info()` to check whether a directory exists, creates it if necessary, and returns an associated information object. The `fs` [`mkdir`](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fspromises_mkdir_path_options) method is used to create the directory:

```
// return folder info object if it can be used
async function folderUsable(folder) {

  try {

    // fetch folder information
    let fInfo = await info(folder);

    // create folder if required
    if (!fInfo.isDir) {
      await fsPromise.mkdir(folder);
      fInfo = await info(folder);
    }

    // folder accessible?
    return (fInfo.isDir && fInfo.read && fInfo.write ? fInfo : false);

  }
  catch (err) {
    console.log('folderUsable error:', err);
    return false;
  }

}
```

A `folderList()` function returns an information object for every file in a directory. It can optionally filter by file extension and sort by a factor such as the creation date. The `fs` [`readdir`](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fspromises_readdir_path_options) method fetches all file names into an array. These are converted into information objects using [`Promise.all`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all), which executes asynchronous code in parallel:

```
// return a sorted array of info objects for all files in a folder
async function folderList(folder, ext = '', sortBy = 'time') {

  try {

    // names of all files in folder
    let filelist = await fsPromise.readdir(folder);

    // fetch file info
    filelist = await Promise.all(
      filelist.map(async f => await info(folder + f))
    );

    // remove unreadable files and sort
    return filelist
      .filter(fn => fn.isFile && fn.read && fn.path.endsWith(ext))
      .sort((f1, f2) => f2[sortBy] - f1[sortBy]);

  }
  catch (err) {
    console.log('folderList error', err);
    return false;
  }

}
```

A `write()` function uses the `fs` [`writeFile`](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fspromises_writefile_file_data_options) method to output content to a file:

```
// create a file, returns true or false
async function write(fn, content = '') {

  try {
    await fsPromise.writeFile(fn, content);
    return true;
  }
  catch (err) {
    console.log('write error', err);
    return false;
  }

}
```

An `unlinkMany()` function deletes all files passed in an array of path strings or information objects. The `fs` [`unlink`](https://nodejs.org/dist/latest/docs/api/fs.html#fs_fspromises_unlink_path) method is processed in parallel on all items:

```
// delete an array of files, return array of true/false
async function unlinkMany(fnlist) {

  return await Promise.all(

    fnlist.map(async fn => {

      try {
        await fsPromise.unlink(fn.path ? fn.path : fn);
        return true;
      }
      catch (err) {
        console.log('unlink error', err);
        return false;
      }

    })

  );

}
```

Finally, the public functions are exported for use in other modules:

```
// public functions
module.exports = {
  info,
  folderUsable,
  folderList,
  write,
  unlinkMany
};
```

### Step 2: Modify `lib/pagehit.js`

The original `lib/pagehit.js` file is modified to save counter data to a file. Additional modules and configuration variables are required:

```
const

  // modules
  fileUtil = require('./fileutil'),
  httpReferrer = require('./httpreferrer'),

  // default data folder
  path = require('path'),
  dataFolder = path.resolve('./data') + path.sep,

  // file save throttling - no more than every 10 seconds
  saveFrequency = 10 * 1000;
```

The [`path` module](https://nodejs.org/dist/latest/docs/api/path.html) provides useful cross-platform file path-parsing functions. In this case, it’s used to obtain the absolute name of a directory for saving data (`data` in the project’s folder).

The `constructor()` imports previous data from a file. Note that class constructors can’t be `async` themselves, but can run immediately involved `async` functions:

1.  Set the `folder` property to a file information object when the `data` directory is available (`fileUtil.folderUsable` will attempt to create it). The application resorts to memory-only counters if saving is not possible.
2.  Set the `saved` property to an array of information objects about each `.json` file in that directory. The array is sorted by creation time with the most recent first.
3.  If at least one `.json` file exists, it’s imported using `require`, which usefully converts it to a real JavaScript object. The previously saved data is merged into the `counter` property.

```
// initialize
constructor() {

  // counter storage
  this.counter = {};

  (async () => {

    // store folder available?
    this.folder = await fileUtil.folderUsable(dataFolder);
    if (!this.folder) return;

    // fetch all JSON files sorted most recent first
    this.saved = await fileUtil.folderList(this.folder.path, '.json');

    // import and merge latest data
    if (this.saved.length) {
      Object.assign(this.counter, require(this.saved[0].path));
    }

  })();

}
```

The `count()` method is changed to start a 10-second timer whenever a page counter is incremented. Further page hits don’t alter this timer, so `this.save()` is called 10 seconds after the first update occurs. Therefore, saving cannot occur more frequently than every 10 seconds and runs as a background task so the updated counter can be returned immediately.

```
// increase URL counter
count(req) {

  let hash = httpReferrer(req);
  if (!hash) return null;

  // define count default
  this.counter[ hash ] = this.counter[ hash ] || 0;

  // save event
  this.saveTimer = this.saveTimer || setTimeout(this.save.bind(this), saveFrequency);

  // return incremented count
  return ++this.counter[ hash ];
}
```

The `save()` method does the following:

1.  It converts the `counter` property to a JSON string and saves it using a file name based on the number of milliseconds since 1 January 1970.
2.  If the file is successfully created, all existing `.json` files referenced in the `saved` property are deleted. It then references the file just saved.
3.  The `saveTimer` property is reset so further saves become possible.

```
// store latest data
async save() {

  // can save
  if (!this.folder) return;

  // save new file
  let fn = `${this.folder.path}hit${+ new Date()}.json`;

  if (await fileUtil.write(fn, JSON.stringify(this.counter))) {

    console.log(`page hits stored: ${fn}`);

    // delete old files
    fileUtil.unlinkMany(this.saved);

    // add current file to saved list
    this.saved = [{ path: fn }];

  }

  // reset timer
  this.saveTimer = null;

}
```

### Step 3: Test

Start the server again using `npm run debug`. If file saving is possible, a new `data` sub-directory will appear in the project directory.

Use the [same test page](#node11-ch2.xhtml_step-4-test-page) as before and hit refresh a few times. Within 10 seconds, a file will appear in the data folder with a name such as `hit1579705252776.json`. It will contain (minified) hit counter data. For example:

```
{
  "987c5e69bb367d3d5e4f4412be35a0ab": 1,
  "3fe3473a2c564240ecb6823460ecd876": 2
}
```

New data files are created every 10 seconds when necessary. You can restart the project server and the number of page hits will be retained.

The full example code is available from [https://github.com/sitepoint-editors/pagehit-file](https://github.com/sitepoint-editors/pagehit-file).

## Job Done?

While these examples work, they’re not intended for production use, and you may have spotted potential problems …

*   The service is simplistic. It retains a total count, but couldn’t be used to determine how many people accessed within a period, such as today or this week.
*   A counter for every page is always retained in memory. All OS processes have a memory limit and a busy service would eventually fail.
*   File handling is difficult, and a busy service would need to save many megabytes of data every few seconds. It would be possible to split data into multiple files or only append changed counters, but file handling would become even more complicated.
*   File saving can fail—for example, if disk space runs out or the process halts during a save operation. It may be possible to return to a previous file, but data would be lost.
*   Data is also lost if a counter is updated during a file save operation and the service is stopped soon afterwards!

All these issues can be solved with a database, which can take responsibility for storing page hit information.

These are the next steps for you to take:

1.  Discover how Docker can be used for Node.js development, including database application management.
2.  Rewrite the page hit service to use MySQL or MongoDB.
3.  Use various tools and techniques to debug your Node.js code.

# Chapter 3: Understanding module.exports and exports in Node.js

### by James Hibbard

In programming, modules are self-contained units of functionality, which can be shared and reused across projects. They make our lives as developers easier, as we can use them to augment our applications with functionality that we haven’t had to write ourselves. They also allow us to organize and decouple our code, leading to applications that are easier to understand, debug and maintain.

In this guide, I’ll examine how to work with modules in Node.js, focusing on on how to export and consume them.

## Different Module Formats

As JavaScript originally had no concept of modules, a variety of competing formats have emerged over time. Here’s a list of the main ones to be aware of:

*   The [Asynchronous Module Definition (AMD)](https://en.wikipedia.org/wiki/Asynchronous_module_definition) format is used in browsers and uses a `define` function to define modules.
*   The [CommonJS (CJS)](https://en.wikipedia.org/wiki/CommonJS) format is used in Node.js and uses `require` and `module.exports` to define dependencies and modules. The npm ecosystem is built upon this format.
*   The [ES Module (ESM)](https://www.sitepoint.com/understanding-es6-modules/) format. As of ES6 (ES2015), JavaScript supports a native module format. It uses an `export` keyword to export a module’s public API and an `import` keyword to import it.
*   The [System.register](https://github.com/systemjs/systemjs/blob/master/docs/system-register.md) format was designed to support ES6 modules within ES5.
*   The [Universal Module Definition (UMD)](https://riptutorial.com/javascript/example/16339/universal-module-definition--umd-) format can be used both in the browser and in Node.js. It’s useful when a module needs to be imported by a number of different module loaders.

Please be aware that this guide deals solely with the **CommonJS format**, the standard in Node.js. If you’d like to read into any of the other formats, I recommend [this article](https://www.jvandemo.com/a-10-minute-primer-to-javascript-modules-module-formats-module-loaders-and-module-bundlers/), by SitePoint author Jurgen Van de Moere.

## Requiring a Module

Node.js comes with [a set of built-in modules](https://www.w3schools.com/nodejs/ref_modules.asp) that we can use in our code without having to install them. To do this, we need to require the module using the `require` keyword and assign the result to a variable. This can then be used to invoke any methods the module exposes.

For example, to list out the contents of a directory, you can use the [file system module](https://nodejs.org/api/fs.html) and its `readdir` method:

```
const fs = require('fs');
const folderPath = '/home/jim/Desktop/';

fs.readdir(folderPath, (err, files) => {
  files.forEach(file => {
    console.log(file);
  });
});
```

Note that in CommonJS, modules are loaded synchronously and processed in the order they occur.

## Creating and Exporting a Module

Now let’s look at how to create our own module and export it for use elsewhere in our program. Start off by creating a `user.js` file and adding the following:

```
const getName = () => {
  return 'Jim';
};

exports.getName = getName;
```

Now create an `index.js` file in the same folder and add this:

```
const user = require('./user');
console.log(`User: ${user.getName()}`);
```

Run the program using `node index.js` and you should see the following output to the terminal:

```
User: Jim
```

So what has gone on here? Well, if you look at the `user.js` file, you’ll notice that we’re defining a `getName` function, then using the `exports` keyword to make it available for import elsewhere. Then in the `index.js` file, we’re importing this function and executing it. Also notice that in the `require` statement, the module name is prefixed with `./`, as it’s a local file. Also note that there’s no need to add the file extension.

### Exporting Multiple Methods and Values

We can export multiple methods and values in the same way:

```
const getName = () => {
  return 'Jim';
};

const getLocation = () => {
  return 'Munich';
};

const dateOfBirth = '12.01.1982';

exports.getName = getName;
exports.getLocation = getLocation;
exports.dob = dateOfBirth;
```

And in `index.js`:

```
const user = require('./user');
console.log(
  `${user.getName()} lives in ${user.getLocation()} and was born on ${user.dob}.`
);
```

The code above produces this:

```
Jim lives in Munich and was born on 12.01.1982.
```

Notice how the name we give the exported `dateOfBirth` variable can be anything we fancy (`dob` in this case). It doesn’t have to be the same as the original variable name.

### Variations in Syntax

I should also mention that it’s possible to export methods and values as you go, not just at the end of the file.

For example:

```
exports.getName = () => {
  return 'Jim';
};

exports.getLocation = () => {
  return 'Munich';
};

exports.dob = '12.01.1982';
```

And thanks to [destructuring assignment](https://www.sitepoint.com/es6-destructuring-assignment/), we can cherry-pick what we want to import:

```
const { getName, dob } = require('./user');
console.log(
  `${getName()} was born on ${dob}.`
);
```

As you might expect, this logs:

```
Jim was born on 12.01.1982.
```

## Exporting a Default Value

In the above example, we’re exporting functions and values individually. This is handy for helper functions that could be needed all over an app, but when you have a module that exports just the one thing, it’s more common to use `module.exports`:

```
class User {
  constructor(name, age, email) {
    this.name = name;
    this.age = age;
    this.email = email;
  }

  getUserStats() {
    return `
      Name: ${this.name}
      Age: ${this.age}
      Email: ${this.email}
    `;
  }
}

module.exports = User;
```

And in `index.js`:

```
const User = require('./user');
const jim = new User('Jim', 37, 'jim@example.com');

console.log(jim.getUserStats());
```

The code above logs this:

```
Name: Jim
Age: 37
Email: jim@example.com
```

## What’s the Difference Between `module.exports` and `exports`?

In your travels across the Web, you might come across the following syntax:

```
module.exports = {
  getName: () => {
    return 'Jim';
  },

  getLocation: () => {
    return 'Munich';
  },

  dob: '12.01.1982',
};
```

Here we’re assigning the functions and values we want to export to an `exports` property on `module` — and of course, this works just fine:

```
const { getName, dob } = require('./user');
console.log(
  `${getName()} was born on ${dob}.`
);
```

This logs the following:

```
Jim was born on 12.01.1982.
```

So what *is* the difference between `module.exports` and `exports`? Is one just a handy alias for the other?

Well, kinda, but not quite …

To illustrate what I mean, let’s change the code in `index.js` to log the value of `module`:

```
console.log(module);
```

This produces:

```
Module {
  id: '.',
  exports: {},
  parent: null,
  filename: '/home/jim/Desktop/index.js',
  loaded: false,
  children: [],
  paths:
   [ '/home/jim/Desktop/node_modules',
     '/home/jim/node_modules',
     '/home/node_modules',
     '/node_modules' ] }
```

As you can see, `module` has an `exports` property. Let’s add something to it:

```
// index.js
exports.foo = 'foo';
console.log(module);
```

This outputs:

```
Module {
  id: '.',
  exports: { foo: 'foo' },
  ...
```

Assigning properties to `exports` also adds them to `module.exports`. This is because (initially, at least) `exports` is a reference to `module.exports`.

### So Which One Should I use?

As `module.exports` and `exports` both point to the same object, it doesn’t normally matter which you use. For example:

```
exports.foo = 'foo';
module.exports.bar = 'bar';
```

This code would result in the module’s exported object being `{ foo: 'foo', bar: 'bar' }`.

However, there is a caveat. Whatever you assign `module.exports` to is what’s exported from your module.

So, take the following:

```
exports.foo = 'foo';
module.exports = () => { console.log('bar'); };
```

This would only result in an anonymous function being exported. The `foo` variable would be ignored.

If you’d like to read more into the difference, I recommend [this article](https://www.hacksparrow.com/nodejs/exports-vs-module-exports.html).

## Conclusion

Modules have become an integral part of the JavaScript ecosystem, allowing us to compose large programs out of smaller parts. I hope this guide has given you a good introduction to working with them in Node.js, as well as helping to demystify their syntax.

# Chapter 4: Forms, File Uploads and Security with Node.js and Express

### by Mark Brown and James Hibbard

If you’re building a web application, you’re likely to encounter the need to build HTML forms on day one. They’re a big part of the web experience, and they can be complicated.

Typically the form-handling process involves:

*   displaying an empty HTML form in response to an initial `GET` request
*   user submitting the form with data in a `POST` request
*   validation on both the client and the server
*   re-displaying the form populated with escaped data and error messages if invalid
*   doing *something* with the sanitized data on the server if it’s all valid
*   redirecting the user or showing a success message after data is processed

Handling form data also comes with extra security considerations.

We’ll go through all of these and explain how to build them with Node.js and [Express](https://expressjs.com/) — the most popular web framework for Node. First, we’ll build a simple contact form where people can send a message and email address securely and then take a look what’s involved in processing file uploads.

![A contact form with email and message with validation errors](Images/node-forms.png)

#### The Repo

As ever, the complete code can be found in our [GitHub repo](https://github.com/sitepoint-editors/node-forms).

## Setup

Make sure you’ve got a recent version of Node.js installed. `node -v` should return `8.9.0` or higher.

Download the starter code from here with Git:

```
git clone -b starter https://github.com/sitepoint-editors/node-forms.git node-forms-starter
cd node-forms-starter
npm install
npm start
```

#### Repo Branches

The repo has two branches, `starter` and `master`. The `starter` branch contains the minimum setup you need to follow this guide. The `master` branch contains a full, working demo (link above).

There’s not *too much* code in there. It’s just a bare-bones Express setup with [EJS templates](https://www.npmjs.com/package/ejs) and error handlers:

```
// server.js
const path = require('path');
const express = require('express');
const layout = require('express-layout');

const routes = require('./routes');
const app = express();

app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'ejs');

const middlewares = [
  layout(),
  express.static(path.join(__dirname, 'public')),
];
app.use(middlewares);

app.use('/', routes);

app.use((req, res, next) => {
  res.status(404).send("Sorry can't find that!");
});

app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});

app.listen(3000, () => {
  console.log('App running at http://localhost:3000');
});
```

The root url `/` simply renders the `index.ejs` view:

```
// routes.js
const express = require('express');
const router = express.Router();

router.get('/', (req, res) => {
  res.render('index');
});

module.exports = router;
```

## Displaying the Form

When people make a GET request to `/contact`, we want to render a new view `contact.ejs`:

```
// routes.js
router.get('/contact', (req, res) => {
  res.render('contact');
});
```

The contact form will let them send us a message and their email address:

```
<!-- views/contact.ejs -->
<div class="form-header">
  <h2>Send us a message</h2>
</div>
<form method="post" action="/contact" novalidate>
  <div class="form-field">
    <label for="message">Message</label>
    <textarea class="input" id="message" name="message" rows="4" autofocus></textarea>
  </div>
  <div class="form-field">
    <label for="email">Email</label>
    <input class="input" id="email" name="email" type="email" value="" />
  </div>
  <div class="form-actions">
    <button class="btn" type="submit">Send</button>
  </div>
</form>
```

See what it looks like at `http://localhost:3000/contact`.

## Form Submission

To receive POST values in Express, you first need to include the `body-parser` middleware, which exposes submitted form values on `req.body` in your route handlers. Add it to the end of the `middlewares` array:

```
// server.js
const bodyParser = require('body-parser');

const middlewares = [
  // ...
  bodyParser.urlencoded({ extended: true }),
];
```

It’s a common convention for forms to POST data back to the same URL as was used in the initial GET request. Let’s do that here and handle POST `/contact` to process the user input.

Let’s look at the invalid submission first. If invalid, we need to pass back the submitted values to the view (so users don’t need to re-enter them) along with any error messages we want to display:

```
router.get('/contact', (req, res) => {
  res.render('contact', {
    data: {},
    errors: {}
  });
});

router.post('/contact', (req, res) => {
  res.render('contact', {
    data: req.body, // { message, email }
    errors: {
      message: {
        msg: 'A message is required'
      },
      email: {
        msg: 'That email doesn‘t look right'
      }
    }
  });
});
```

If there are any validation errors, we’ll do the following:

*   display the errors at the top of the form
*   set the input values to what was submitted to the server
*   display inline errors below the inputs
*   add a `form-field-invalid` class to the fields with errors

```
<!-- views/contact.ejs -->
<div class="form-header">
  <% if (Object.keys(errors).length === 0) { %>
    <h2>Send us a message</h2>
  <% } else { %>
    <h2 class="errors-heading">Oops, please correct the following:</h2>
    <ul class="errors-list">
      <% Object.values(errors).forEach(error => { %>
        <li><%= error.msg %></li>
      <% }) %>
    </ul>
  <% } %>
</div>

<form method="post" action="/contact" novalidate>
  <div class="form-field <%= errors.message ? 'form-field-invalid' : '' %>">
    <label for="message">Message</label>
    <textarea class="input" id="message" name="message" rows="4" autofocus><%= data.message %></textarea>
    <% if (errors.message) { %>
      <div class="error"><%= errors.message.msg %></div>
    <% } %>
  </div>
  <div class="form-field <%= errors.email ? 'form-field-invalid' : '' %>">
    <label for="email">Email</label>
    <input class="input" id="email" name="email" type="email" value="<%= data.email %>" />
    <% if (errors.email) { %>
      <div class="error"><%= errors.email.msg %></div>
    <% } %>
  </div>
  <div class="form-actions">
    <button class="btn" type="submit">Send</button>
  </div>
</form>
```

Submit the form at `http://localhost:3000/contact` to see this in action. That’s everything we need on the view side.

## Validation and Sanitization

There’s a handy middleware called [express-validator](https://www.npmjs.com/package/express-validator) for validating and sanitizing data using the [validator.js](https://github.com/chriso/validator.js) library. Let’s add it to our app.

### Validation

With the [validators](https://github.com/chriso/validator.js#validators) provided, we can easily check that a message and a valid email address was provided:

```
// routes.js
const { check, validationResult, matchedData } = require('express-validator');

router.post('/contact', [
  check('message')
    .isLength({ min: 1 })
    .withMessage('Message is required'),
  check('email')
    .isEmail()
    .withMessage('That email doesn‘t look right')
], (req, res) => {
  const errors = validationResult(req);
  res.render('contact', {
    data: req.body,
    errors: errors.mapped()
  });
});
```

### Sanitization

With the [sanitizers](https://github.com/chriso/validator.js#sanitizers) provided, we can trim whitespace from the start and end of the values, and normalize the email address into a consistent pattern. This can help remove duplicate contacts being created by slightly different inputs. For example, `' Mark@gmail.com'` and `'mark@gmail.com '` would both be sanitized into `'mark@gmail.com'`.

Sanitizers can simply be chained onto the end of the validators:

```
// routes.js
router.post('/contact', [
  check('message')
    .isLength({ min: 1 })
    .withMessage('Message is required')
    .trim(),
  check('email')
    .isEmail()
    .withMessage('That email doesn‘t look right')
    .bail()
    .trim()
    .normalizeEmail()
], (req, res) => {
  const errors = validationResult(req);
  res.render('contact', {
    data: req.body,
    errors: errors.mapped()
  });

  const data = matchedData(req);
  console.log('Sanitized:', data);
});
```

The `matchedData` function returns the output of the sanitizers on our input.

Also, notice our use of the [bail](https://express-validator.github.io/docs/validation-chain-api.html#bail) method, which stops running validations if any of the previous ones have failed. We need this because if a user submits the form without entering a value into the email field, the `normalizeEmail` will attempt to normalize an empty string and convert it to an `@`. This will then be inserted into our email field when we re-render the form.

## The Valid Form

If there are errors, we need to re-render the view. If not, we need to do something useful with the data and then show that the submission was successful. Typically, the person is redirected to a success page and shown a message.

HTTP is stateless, so you can’t redirect to another page *and* pass messages along without the help of a [session cookie](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies) to persist that message between HTTP requests. A “flash message” is the name given to this kind of one-time-only message we want to persist across a redirect and then disappear.

There are three middlewares we need to include to wire this up:

```
// server.js
const cookieParser = require('cookie-parser');
const session = require('express-session');
const flash = require('express-flash');

const middlewares = [
  // ...
  cookieParser(),
  session({
    secret: 'super-secret-key',
    key: 'super-secret-cookie',
    resave: false,
    saveUninitialized: false,
    cookie: { maxAge: 60000 }
  }),
  flash(),
];
```

The `express-flash` middleware adds `req.flash(type, message)`, which we can use in our route handlers:

```
// routes
router.post('/contact', [
  // validation ...
], (req, res) => {
  const errors = validationResult(req);
  if (!errors.isEmpty()) {
    return res.render('contact', {
      data: req.body,
      errors: errors.mapped()
    });
  }

  const data = matchedData(req);
  console.log('Sanitized: ', data);
  // Homework: send sanitized data in an email or persist to a db

  req.flash('success', 'Thanks for the message! I‘ll be in touch :)');
  res.redirect('/');
});
```

The `express-flash` middleware adds `messages` to `req.locals` which all views have access to:

```
<!-- views/index.ejs -->
<% if (messages.success) { %>
  <div class="flash flash-success"><%= messages.success %></div>
<% } %>

<h1>Working With Forms in Node.js</h1>
```

You should now be redirected to the `index` view and see a success message when the form is submitted with valid data. Huzzah! We can now deploy this to production and be sent messages by the prince of Nigeria. You can [find an online demo of this at CodeSandbox](https://codesandbox.io/embed/priceless-butterfly-u3557).

### Sending Email with Node

You might have noticed that the actual sending of the mail is left to the reader as homework. This is not as difficult as it might sound and can be accomplished using the [Nodemailer package](https://www.npmjs.com/package/nodemailer). You can find [bare-bones instructions on how to set this up here](https://www.w3schools.com/nodejs/nodejs_email.asp), or a [more in-depth tutorial here](https://stackabuse.com/how-to-send-emails-with-node-js/).

## Security considerations

If you’re working with forms and sessions on the Internet, you need to be aware of common security holes in web applications. The best security advice I’ve been given is “Never trust the client!”

### TLS over HTTPS

*Always use TLS encryption* over `https://` when working with forms so that the submitted data is encrypted when it’s sent across the Internet. If you send form data over `http://`, it’s sent in plain text and can be visible to anyone eavesdropping on those packets as they journey across the Web.

If you’d like to find out more about working with SSL/TLS in Node.js, please consult [this article](https://www.sitepoint.com/how-to-use-ssltls-with-node-js/).

### Wear Your Helmet

There’s a neat little middleware called [helmet](https://helmetjs.github.io/docs/) that adds some security from HTTP headers. It’s best to include right at the top of your middlewares and is super easy to include:

```
// server.js
const helmet = require('helmet');

middlewares = [
  helmet(),
  // ...
];
```

### Cross-site Request Forgery (CSRF)

You can protect yourself against [cross-site request forgery](https://en.wikipedia.org/wiki/Cross-site_request_forgery) by generating a unique token when the user is presented with a form and then validating that token before the POST data is processed. There’s a [middleware](https://expressjs.com/en/resources/middleware/csurf.html) to help you out here as well:

```
// routes.js
const csrf = require('csurf');
const csrfProtection = csrf({ cookie: true });
```

In the GET request, we generate a token:

```
// routes.js
router.get('/contact', csrfProtection, (req, res) => {
  res.render('contact', {
    data: {},
    errors: {},
    csrfToken: req.csrfToken()
  });
});
```

And also in the validation errors response:

```
router.post('/contact', csrfProtection, [
  // validations ...
], (req, res) => {
  const errors = validationResult(req);
  if (!errors.isEmpty()) {
    return res.render('contact', {
      data: req.body,
      errors: errors.mapped(),
      csrfToken: req.csrfToken()
    });
  }

  // ...
});
```

Then we just need include the token in a hidden input:

```
<!-- view/contact.ejs -->
<form method="post" action="/contact" novalidate>
  <input type="hidden" name="_csrf" value="<%= csrfToken %>">
  <!-- ... -->
</form>
```

That’s all that’s required.

We don’t need to modify our POST request handler, as all POST requests will now require a valid token by the `csurf` middleware. If a valid CSRF token isn’t provided, a `ForbiddenError` error will be thrown, which can be handled by the error handler defined at the end of `server.js`.

You can test this out yourself by editing or removing the token from the form with your browser’s developer tools and submitting.

### Cross-site Scripting (XSS)

You need to take care when displaying user-submitted data in an HTML view as it can open you up to [cross-site scripting(XSS)](https://developer.mozilla.org/en-US/docs/Glossary/Cross-site_scripting). All template languages provide different methods for outputting values. The EJS `<%= value %>` outputs the *HTML escaped* value to protect you from XSS, whereas `<%- value %>` outputs a raw string.

Always use the escaped output `<%= value %>` when dealing with user-submitted values. Only use raw outputs when you’re sure that it’s safe to do so.

## File Uploads

Uploading files in HTML forms is a special case that requires an encoding type of `"multipart/form-data"`. See [MDN’s guide to sending form data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data#A_special_case_sending_files) for more details about what happens with multipart form submissions.

You’ll need additional middleware to handle multipart uploads. There’s an Express package named [multer](https://www.npmjs.com/package/multer) that we’ll use here:

```
// routes.js
const multer = require('multer');
const upload = multer({ storage: multer.memoryStorage() });

router.post('/contact', upload.single('photo'), csrfProtection, [
  // validation ...
], (req, res) => {
  // error handling ...

  if (req.file) {
    console.log('Uploaded: ', req.file);
    // Homework: Upload file to S3
  }

  req.flash('success', 'Thanks for the message! I’ll be in touch :)');
  res.redirect('/');
});
```

This code instructs `multer` to upload the file in the “photo” field into memory and exposes the `File` object in `req.file`, which we can inspect or process further.

The last thing we need is to add the `enctype` attribute and our file input:

```
<form method="post" action="/contact?_csrf=<%= csrfToken %>" novalidate enctype="multipart/form-data">
  <input type="hidden" name="_csrf" value="<%= csrfToken %>">
  <div class="form-field <%= errors.message ? 'form-field-invalid' : '' %>">
    <label for="message">Message</label>
    <textarea class="input" id="message" name="message" rows="4" autofocus><%= data.message %></textarea>
    <% if (errors.message) { %>
      <div class="error"><%= errors.message.msg %></div>
    <% } %>
  </div>
  <div class="form-field <%= errors.email ? 'form-field-invalid' : '' %>">
    <label for="email">Email</label>
    <input class="input" id="email" name="email" type="email" value="<%= data.email %>" />
    <% if (errors.email) { %>
      <div class="error"><%= errors.email.msg %></div>
    <% } %>
  </div>
  <div class="form-field">
    <label for="photo">Photo</label>
    <input class="input" id="photo" name="photo" type="file" />
  </div>
  <div class="form-actions">
    <button class="btn" type="submit">Send</button>
  </div>
</form>
```

Try uploading a file. You should see the `File` objects logged in the console.

### Populating File Inputs

In case of validation errors, we can’t re-populate file inputs like we did for the text inputs ([it’s a security risk](https://stackoverflow.com/questions/1696877/how-to-set-a-value-to-a-file-input-in-html)). A common approach to solving this problem involves these steps:

*   uploading the file to a temporary location on the server
*   showing a thumbnail and filename of the attached file
*   adding JavaScript to the form to allow people to remove the selected file or upload a new one
*   moving the file to a permanent location when everything is valid

Because of the additional complexities of working with multipart and file uploads, they’re often kept in separate forms.

### Uploading Files with Node

Finally, you’ll notice that it’s been left to the reader to implement the actual upload functionality. This is not as difficult as it might sound and can be accomplished using various packages, such as [Formidable](https://www.npmjs.com/package/formidable), or [express-fileupload](https://www.npmjs.com/package/express-fileupload). You can find [bare-bones instructions on how to set this up here](https://flaviocopes.com/how-to-handle-file-uploads-node/), or a [more in-depth tutorial here](https://stackabuse.com/handling-file-uploads-in-node-js-with-expres-and-multer/).

## Thanks for Reading

I hope you enjoyed learning about HTML forms and how to work with them in Express and Node.js. Here’s a quick recap of what we’ve covered:

*   displaying an empty form in response to a GET request
*   processing the submitted POST data
*   displaying a list of errors, inline errors and submitted data
*   checking submitted data with validators
*   cleaning up submitted data with sanitizers
*   passing messages across redirects with a flash message
*   protecting yourself against attacks like CSRF and XSS
*   processing file uploads in multipart form submissions

# Chapter 5: Working with Databases in Node

### by Craig Buckler

The performance techniques described in this chapter are more radical and could be difficult to apply to an existing project. Fortunately, there are no such limitations when embarking on a new site or app, so we look deeper into CMS issues, JavaScript optimization, DOM handling, server-side rendering, static site generators (SSGs), and development processes.

## Evaluate CMS Templates and Plugins

Content management systems such as WordPress don’t generate bloated, badly performing pages … *until you start adding stuff!*

Free or commercial templates make financial sense. Why employ a developer when an off-the-shelf solution does everything you need for a few dollars? Unfortunately, there’s a hidden cost. Generic templates must sell hundreds of copies—if not thousands—to recoup the development effort. To attract buyers, the developers bundle every conceivable feature. Your site may only use a fraction of those facilities, but they can still be present in the code, so the download weight and processing are affected.

Similarly, be wary about plugins, since their quality and effectiveness vary. The best plugins can improve performance by optimizing database tables, caching data, and removing redundant code. The worst will duplicate assets, make convoluted configuration changes (such as `.htaccess` files), add unnecessary bloat, and affect responsiveness even though they’re inactive on a particular page.

Always evaluate page cost and performance when considering new templates and plugins. Where possible, choose more lightweight options, even if the purchase price is higher.

## Reduce Client-side Code

Blindingly obvious statement alert: *smaller files results in faster pages.*

Not all assets are created equal, though. 500KB of image data has a relatively low performance hit, since it’s downloaded once, cached in the browser, and positioned on the page. The same quantity of HTML, CSS, or JavaScript has a far bigger impact, because it must be downloaded, parsed, and processed.

Ideally, the number of HTML DOM nodes should be reduced to a minimum. A shallower tree depth means rendering and reflows are performed more effectively. Modern layout tools such as [Flexbox](https://www.sitepoint.com/flexbox-css-flexible-box-layout/) and [Grid](https://www.sitepoint.com/introduction-css-grid-layout-module/) allow you to remove wrapper elements that may have been necessary in float-based designs. Keep the document small and look out for signs of [DIVitis](https://en.wiktionary.org/wiki/divitis)!

Similarly, the fewer CSS rules you require, the quicker a document can be rendered. Look our for complex selectors, especially when using preprocessors such as [Sass](https://sass-lang.com/), which expand deeply nested rule sets. Check your compiled style sheet output to ensure it’s as efficient as is practical.

Try to embrace the [CSS cascade](https://developer.mozilla.org/docs/Web/CSS/Cascade) rather than working against it! A little understanding can reduce code and improve performance. For example, you can set default fonts, colors, sizes, tables, grids, and form fields that are universally applied but can be tweaked for individual components.

Also be wary of using CSS resets, which means having to re-apply default styling to every element. CSS normalization, such as [Normalize.css](https://necolas.github.io/normalize.css/), *could* be a better alternative, since it makes browsers render more consistently. That said, default styling between browsers is closer than ever.

## Optimize JavaScript Code

HTML is a robust technology; even the oldest browsers without HTML5 support will show content. Similarly, CSS can fail to download or have coding errors, but the page remains viewable. By contrast, JavaScript is fragile and computationally expensive. A single error, unsupported command, or long-running task can prevent further code from running.

It’s difficult to recommend JavaScript optimizations, since all applications will be different, but there are a few general tips that could improve performance. That said, be wary of micro-optimizations, which may shave a few milliseconds but aren’t called frequently enough to make a difference. Use your browser’s developer tools to check whether any gains have been achieved.

### Use JavaScript Sparingly

If a browser can do something in HTML and/or CSS alone, that should be your preferred option. You can still apply progressive enhancements where necessary (discussed below).

Modern browsers have implemented many regularly used features that previously required scripting, such as [form validation](https://developer.mozilla.org/docs/Learn/HTML/Forms/Form_validation), [field auto-complete](https://developer.mozilla.org/docs/Web/HTML/Element/datalist), [animations](https://developer.mozilla.org/docs/Web/CSS/animation), [video](https://developer.mozilla.org/docs/Web/HTML/Element/video), [expanding text](https://developer.mozilla.org/docs/Web/HTML/Element/details), [modal dialogs](https://developer.mozilla.org/docs/Web/HTML/Element/dialog), and more. There will be challenges—ask anyone who’s ever tried styling a `<select>` drop-down—but using a native feature will always be faster and use less code.

Consider the choice of using an HTML `<button>` verses a `<div>` as a form submit. The HTML code starts in a similar way:

```
<button>submit</button>
```

Styling a DIV in CSS may be easier:

```
<div class="button">submit</div>
```

However, the HTML `<button>`:

1.  offers default styling to look like an OS button
2.  works on all browsers even when CSS or JavaScript fails
3.  works immediately, as the page loads and before JavaScript has started executing
4.  will automatically submit its parent `<form>` (if validity checks pass)
5.  can be operated with a mouse, touch screen, keyboard, or any other input device
6.  can receive focus, and accepts keypress shortcuts
7.  requires no ARIA roles or other accessibility assistance

A button that’s simulated in CSS and JavaScript requires significant effort, and it will never function as effectively as the native HTML alternative.

### Avoid Long-running Tasks

Long-running tasks often trigger *unresponsive browser* messages, which prompt the user to halt JavaScript execution. Complex processing is best handled by a **[Web Worker](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers)**, which allows a script to run in a background thread.

Web Worker scripts are limited. They can’t interact with the page DOM, and must communicate with the main script using a message API, but they’re able to perform Ajax requests and launch their own child workers.

### Bind Events Sparingly

Applications can have dozens of event handlers. A handler function is registered to an event when it’s triggered on a specific DOM element—such as running the `doSomething()` function when a click is detected on the `myElement` node:

```
myElement.addEventListener('click', doSomething);
```

Each bound event has a performance hit. Ideally, you should only add events you require, return from handler functions quickly, and unbind using [removeEventListener](https://developer.mozilla.org/docs/Web/API/EventTarget/removeEventListener) when an event is no longer necessary.

Also be wary of quick-firing events such as `mousemove` and `scroll`, which can trigger rapid and wasteful rerunning of handler functions. One way around this is to use throttling to ensure an event is called no more than once every `N` milliseconds. For example:

```
// thottle event to delay ms
function eventThrottle(element, event, callback, delay = 300) {

  let throttle;
  element.addEventListener(event, (e) => {

    throttle = throttle || setTimeout(() => {
      throttle = null;
      callback(e);
    }, delay);

  }, false);

}

// call windowScrollHandler no more than once every 300ms
eventThrottle(window, 'scroll', windowScrollHandler);
```

Alternatively, **debouncing** can be used to ensure a handler is only called after the event has stopped being triggered for `N` milliseconds:

```
// debounce event until it no longer occurs for delay ms
function eventDebounce(element, event, callback, delay = 300) {

  let debounce;
  element.addEventListener(event, (e) => {
    clearTimeout(debounce);
    debounce = setTimeout(() => callback(e), delay);
  }, false);

}

// call windowScrollHandler when at least 300ms has elapsed since the last event
eventThrottle(window, 'scroll', windowScrollHandler);
```

Finally, remember to make effective use of event delegation. For example, presume you have an HTML `<table>` with thousands of cells and want to react to a `<td>` being clicked. Attaching an event to each cell requires significant processing and would need to be reapplied if the table changed. Instead, you can attach a single event handler to the `<table>` element and examine the target. For example:

```
// handle a click on any <td> element
document.getElementById('mytable').addEventListener('click', (e) => {

  let t = e.target.closest('td');
  if (!t) return;

  console.log('clicked cell', t);

});
```

### Analyze Modified Code

It’s rare to encounter code that hasn’t been modified before it reaches the browser!

*   Minifiers attempt optimizations such as rearranging lines or expanding loops.
*   Transpilers such as Babel convert ES6 to ES5 so the code runs in older browsers.
*   Compilers such as TypeScript, CoffeeScript, and Flow convert alternative or superset syntaxes to JavaScript.
*   Projects such as [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor) convert C# to [WebAssembly](https://webassembly.org/)—a low-level, assembly-like language that offers near-native OS performance in JavaScript engines.

All offer stability and performance benefits, but check that the conversion is optimal and that it’s not unnecessarily importing several kilobytes of transpiler library code. For example, consider the following 32-byte [ES6 for...of](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of) loop:

```
for (let p of n) console.log(p);
```

This results in 598 bytes of Babel-transpiled code. Each additional loop adds a similar quantity of code, and none will execute in IE11—*which partly defeats the point of transpiling!* Options to consider:

*   Use ES5 or more transpiler-efficient ES6 code to achieve the same result.
*   Use differential loading to serve [ES6 module-based code](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) to modern browsers and larger transpiled scripts to older applications.
*   Drop support for browsers without ES6 support (primarily IE). Your site or application can remain usable if you adopt server-side rendering and progressive enhancement techniques.

## Modify the DOM Effectively

Some modern JavaScript frameworks implement a virtual DOM. As you change page elements, the virtual DOM works out what’s been altered and determines how and when to make modifications. Ultimately, it must still change the real DOM, and you can make similar optimizations to improve performance without the additional overhead of virtual DOM calculations.

### Cache Regularly Used Nodes

Regularly used DOM nodes should be stored as JavaScript variables so they don’t need to be re-fetched. The DOM references are retained even when other tree nodes are modified:

```
const
  main    = document.getElementsByTagName('main')[0],
  heading = main.querySelector('h1'),
  tables  = main.getElementsByTagName('table');
```

#### Search from Any Node

Rather than searching the whole tree from `document`, many DOM methods allow you to start from any node. The example above searches for the first heading and tables within the `<main>` element.

[`querySelector()`](https://developer.mozilla.org/docs/Web/API/Element/querySelector) and [`querySelectorAll()`](https://developer.mozilla.org/docs/Web/API/Element/querySelector) can find elements using jQuery-like CSS selectors. They’re usually slower than [`getElementById()`](https://developer.mozilla.org/docs/Web/API/Document/getElementById), [`getElementsByTagName()`](https://developer.mozilla.org/docs/Web/API/Element/getElementsByTagName) and [`getElementsByClassName()`](https://developer.mozilla.org/docs/Web/API/Element/getElementsByClassName), although the speed difference is unlikely to affect most applications.

#### Running Benchmarks

Tools such as [jsPerf.com](https://jsperf.com/) provide a way to create code snippets and run benchmarks on any browser to prove the efficiency—or inefficiency—of alternative functions.

[`getElementsByTagName()`](https://developer.mozilla.org/docs/Web/API/Element/getElementsByTagName) and [`getElementsByClassName()`](https://developer.mozilla.org/docs/Web/API/Element/getElementsByClassName) also return *live* HTMLCollections, which update automatically as the DOM is modified—so that it’s not necessary to rerun the query.

### Minimize Reflows

When an element is added, modified, or removed from a page, it can trigger a cascade of layout changes to surrounding elements. For example, increasing a width by 1px could result in a neighboring element wrapping to the next line, which pushes all subsequent content down the page. It’s therefore more efficient to make changes that can’t impact the layout. For example:

*   use [opacity](https://developer.mozilla.org/docs/Web/CSS/opacity) and/or [transform](https://developer.mozilla.org/docs/Web/CSS/transform) to translate (move), scale, or rotate an element
*   limit the scope of the reflow by changing elements low in the DOM tree (those without deeply nested children)
*   update elements in their own `position: absolute;` or `position: fixed;` layer
*   modify hidden elements (`display: none;`), then show them after the change has been applied

### Batch-update Styles

The following example could cause three reflows:

```
let myelement = document.getElementById('myelement');
myelement.width = '100px';
myelement.height = '200px';
myelement.style.margin = '10px';
```

Performance can be improved by appending a class:

```
let myelement = document.getElementById('myelement');
myelement.classList.add('newstyles');
```

This applies CSS properties in one reflow operation:

```
.newstyles {
  width: 100px;
  height: 200px;
  margin: 10px;
}
```

### Batch-update Elements

Try to minimize the number of times you interact with the DOM. An empty [DocumentFragment](https://developer.mozilla.org/docs/Web/API/DocumentFragment) can be used to build elements in memory before applying those changes to the page. For example, you can create an unordered list with three items like so:

```
// create list
let
  frag = document.createDocumentFragment(),
  ul = frag.appendChild( document.createElement('ul') );

for (let i = 1; i <= 3; i++) {
  let li = ul.appendChild( document.createElement('li') );
  li.textContent = 'item ' + i;
}

// append list to the DOM
document.body.appendChild(frag);
```

The DOM is only modified on the last line.

### Use requestAnimationFrame

The [window.requestAnimationFrame()](https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame) method calls a function just before the browser performs the next repaint—normally once every sixtieth of a second (approximately every 17ms, presuming no other render-blocking processes are occurring). It’s normally used for animating frames in HTML5 games, although running it before any DOM update will be beneficial. For example:

```
function updateDOM() {
  let p = document.createElement('p');
  p.textContent = 'new element';
  document.body.appendChild( p );
}

requestAnimationFrame( updateDOM );
```

## Consider Progressive Rendering

Rather than using a single site-wide CSS file, **progressive rendering** is a technique that defines individual style sheets for separate components. Each is loaded immediately before the component is referenced in the HTML:

```
<head>

  <!-- core styles used across components -->
  <link rel='stylesheet' href='base.css' />

</head>
<body>

  <!-- header component -->
  <link rel='stylesheet' href='header.css' />
  <header>...</header>

  <!-- primary content -->
  <link rel='stylesheet' href='content.css' />
  <main>

    <!-- form styling -->
    <link rel='stylesheet' href='form.css' />
    <form>...</form>

  </main>

  <!-- header component -->
  <link rel='stylesheet' href='footer.css' />
  <footer>...</footer>

</body>
```

Each `<link>` still blocks rendering, but for a shorter time, because the file is smaller. The page is usable sooner, since each component renders in sequence; the top of the page can be viewed while remaining content loads. A similar approach is often adopted by [Web Components](https://developer.mozilla.org/docs/Web/Web_Components), which encapsulate CSS within the code.

The technique can be less practical in templates where the content dictates the layout (Flexbox and tables), since reflows are triggered more frequently as the page loads. Grid-based page layouts are generally more suitable.

There’s [some variation in how browsers treat progressive rendering](https://jakearchibald.com/2016/link-in-body/#changes-to-chrome), but the worst-case scenario is that the browser blocks rendering until all discovered CSS files have loaded. That’s no worse than loading each in the `<head>`.

Progressive rendering could benefit large sites where individual pages are constructed from a varied selection of different components.

## Use Server-side Rendering

Which process is quicker?

Process 1 (typically used by JavaScript frameworks):

1.  Request a URL.
2.  Respond with a (mostly) empty HTML file.
3.  Download and execute JavaScript.
4.  Use Ajax or similar techniques to fetch content according to the URL.
5.  Load the content into the page body.

Process 2 (old-school method):

1.  Request a URL.
2.  Respond with the full HTML.

Server-side rendering is always quicker for the initial page load.

Loading a second page can be faster in Process 1, since it’s able to start at step 4\. Assets such as style sheets, JavaScript, and images may already be available and parsed. Unfortunately, a large proportion of visitors may only view a single page, and the payload is higher because a larger quantity of JavaScript is necessary.

This is a better-performing process:

1.  Request a URL.
2.  Load HTML directly from the server into the browser.
3.  Download and execute JavaScript. Some *rehydration* may be necessary to initiate components with HTML data.
4.  Use Ajax or similar techniques to fetch and populate content according to URL navigation changes.

This can be more difficult to manage, since not all JavaScript frameworks provide server-based rendering capabilities using Node.js, PHP, Ruby, Python, and so on.

## Do You Need a JavaScript or CSS Framework?

A CSS and/or JavaScript framework can provide a good development structure for teams working on larger sites or applications. However, most are general-purpose tools: they provide a range of features you may not need or may have to adapt. Optimizing performance is often difficult because the core code isn’t under your control.

While a framework is certainly useful for prototyping, always question whether it’s necessary for the final site or application. How much weight does it add? Will it improve performance? Can it be updated easily? What happens when it’s eventually abandoned?

Invest time in researching the choices. Without investigation, every application looks like a nail to developers who understand a specific hammer. You should certainly avoid using more than one framework—with the possible exception of server-side options, or compilers such as [Svelte](https://svelte.dev/), which remove themselves from production code.

Even once you settle on a chosen framework, there may be modular or lightweight alternatives such as [Preact](https://preactjs.com/) instead of [React](https://reactjs.org/), or [bling.js](https://gist.github.com/paulirish/12fb951a8b893a454b32) instead of [jQuery](https://jquery.com/).

Ultimately, the most efficient and adaptable framework will be one written specifically for your application.

## Use a Static Site Generator

Most people start web development by creating (static) HTML, CSS, and possibly JavaScript files. The resulting assets can be hosted anywhere and are fast because they don’t use server- or client-side processing.

The main downside is content management: adding a new page could involve changing hard-coded navigation menus on every page in the site. At this point, developers often turn to server-side languages or a database-driven CMS, both of which have their own set of challenges.

What if you could create a fast, static site but make cross-site changes programmatically when something is added or removed? That’s exactly what a **static site generator** (SSG) does. It takes content—typically defined in markdown files—and builds a set of static web pages. The build-time process can construct menus, import images, generate styles, and so on, and can be rerun when anything changes. The resulting site is decoupled from a server and is often referred to as using a **JAMstack**: JavaScript, APIs, and markup.

Most SSGs build a set of folder-based HTML files with associated assets that can be uploaded to any web server capable of serving static content. The Ruby-based [Jekyll](https://jekyllrb.com/) was one of the first SSGs, but [StaticGen.com](https://www.staticgen.com/) lists dozens of alternatives for a range of languages. Options such as [Gatsby](https://www.gatsbyjs.org/) also create React-based JavaScript applications rather than HTML files. (*Whether or not that’s a benefit is another matter!)*

A static site can offer the best site performance, since it’s rendered once, then delivered to all users as is. There are no server-side dependencies, reliability is improved, version control is easy, and security issues can be eradicated.

There are some downsides:

*   configuration and setup takes time and is more difficult than a CMS
*   SSGs are rarely suitable for non-technical editors
*   there’s no concept of user roles or permission rights
*   site consistency can be more difficult to enforce, as editors can add any client-side code
*   the rebuild process can be slow, especially on larger sites

SSGs are ideal for sites that change relatively infrequently, but many of the issues can be overcome by importing data from a headless CMS or automating the build process.

## Use a Build System

Even the most conscientious developer can forget to minimize a CSS file, optimize an image, or remove debugging `console` statements. Whatever technology you use to create a site or app, a **build process** can automate mundane tasks to ensure there are no oversights. Additionally, they can run tests, verify code, and deploy to staging or live servers.

Creating a build process can take a day or two, but it should save time over the long term. Popular generic build tools include [Gulp.js](https://gulpjs.com/), [Grunt.js](https://gruntjs.com/), [Broccoli.js](https://broccoli.build/), and [Brunch](https://brunch.io/), which allow you to define and run tasks manually or when files are changed.

Alternatively, you could opt for web-specific module bundlers such as [webpack](https://webpack.js.org/) or [Parcel](https://parceljs.org/), which *understand* HTML, CSS, and JavaScript so they can parse and build optimized code, through operations like these:

*   dead asset elimination
*   code splitting and dependency handling
*   ES6 to ES5 transpiling
*   minification
*   source map generation
*   cache-busting
*   live reloading
*   enforcing performance budgets (discussed below)

Module bundlers often promise zero configuration … *although the reality may be somewhat different!*

A few tips to get started:

*   Choose a build system and stick with it for a while.
*   Automate the most frustrating tasks first.
*   Try not to overcomplicate your build process. Spend an hour or two creating an initial setup, then evolve it over time.
*   Do as much during the build process as possible. For example, an HTML template could be partially constructed from known data and partials rather than parsing everything at render time.

Further reading:

*   [A Guide to Using npm as a Build Tool](https://www.sitepoint.com/guide-to-npm-as-a-build-tool/)
*   [An Introduction to Gulp.js](https://www.sitepoint.com/premium/books/an-introduction-to-gulp-js/read/1)
*   [A Beginner’s Guide to Webpack](https://www.sitepoint.com/premium/books/a-beginner-s-guide-to-webpack/read/1)
*   [A Beginner’s Guide to Parcel](https://www.sitepoint.com/premium/books/a-beginner-s-guide-to-parcel/read/1)

## Use Progressive Enhancement

**Progressive enhancement** is a development approach rather than a technology. Each site or app feature starts with a baseline minimum viable implementation—perhaps an HTML-only solution. Enhancements are then added progressively when they’re supported by the user’s device. Consider a simple search box:

1.  The base solution is an HTML `<input type="search" />` field which, when a string is entered, triggers a new page load showing search results.
2.  HTML5 [constraint validation](https://developer.mozilla.org/docs/Web/Guide/HTML/HTML5/Constraint_validation) can be applied to ensure searching only occurs when a minimum of three characters has been entered.
3.  CSS styles are applied, showing basic formatting such as fonts, colors, borders, etc.
4.  When the field has focus, CSS animations could enlarge the field, show a submit button, etc.
5.  JavaScript could show suggestions as the user types characters.
6.  JavaScript could show a simple list of search results without the user having to leave the current page.
7.  PWA service workers could be used to cache suggestions and search results for later use.

Where necessary, the code tests that a feature is supported before attempting the enhancement. For example, suggestions could be implemented when JavaScript is running, events are supported, and the HTML5 [`<datalist>`](https://developer.mozilla.org/docs/Web/HTML/Element/datalist) element is available.

#### Adding Missing Features with Polyfills

It’s often possible to use a *polyfill* to add a missing feature to browsers without native support. This can range from additional prototypes, such as the [String.padStart() method](https://github.com/Financial-Times/polyfill-library/tree/master/polyfills/String/prototype/padStart), through to full APIs, such as one to [provide geolocation support using IP lookups](https://github.com/Financial-Times/polyfill-library/tree/master/polyfills/navigator/geolocation).

[Polyfill.io](https://polyfill.io/) provides a custom set of polyfills. However, be wary about the performance cost of attempting to polyfill everything. It may be preferable to offer IE users a fast, rudimentary feature than a slow, fully polyfilled experience.

In the search box example above, progressive enhancement offers the following benefits:

*   The search box is device agnostic and works in all browsers—old, current, and those released tomorrow.
*   Assuming the HTML loads, the search box is always operational. This includes the period before CSS and/or JavaScript is downloaded and parsed. In performance terms, the feature is responsive immediately.
*   The user gets the best possible experience their device can handle. Performance isn’t affected when an enhancement can’t be added.
*   The search box is fault-tolerant: any enhancement can work or fail without breaking the system. It doesn’t matter whether CSS and/or JavaScript are blocked, are slow to arrive, or fail to download.
*   It’s the responsible option, and doesn’t require more development effort in most situations.

The approach has no downsides. Progressive enhancement only breaks when:

1.  It isn’t considered from the start. It may be difficult to retrospectively enhance a feature that already requires a high base-level of CSS and JavaScript.
2.  You try to support all browsers equally. It’s futile to expect a decade-old version of IE to behave the same as a modern application. Progressive enhancement means you never need to worry about old browsers. Their users may not receive the best experience, but the feature remains usable.

## Adopt a Performance Budget

A performance budget imposes a limit on related metrics. Typical options include:

*   quantity-based limits, such as the maximum number of fonts, images, scripts, etc.
*   time-based limits, such as the first meaningful paint or interactive times
*   rule-based limits, such as a minimum performance and accessibility score in Lighthouse audits

You should experiment and discuss options with stakeholders to establish baseline criteria, such as:

*   the total size of a page must not exceed 500KB
*   a single image must be no more than 150KB
*   the home page must deliver less than 100KB of JavaScript
*   all pages must be readable within five seconds on a mid-range mobile device operating on an average 3G connection

Ideally, these criteria can be added to your build process. Tools such as the [Lighthouse module](https://www.npmjs.com/package/lighthouse) and file size plugins can report—*and potentially block*—any deviation from the budget. Exceeding the budget means you must either:

1.  optimize an existing feature/asset
2.  lazy load an existing feature/asset on demand
3.  remove an existing feature/asset
4.  reject the new feature/asset

The limitations can help teams prioritize features. Increasing the budget should always be tougher than implementing another solution! For example, a budget increase must be discussed, justified, and agreed to by a two-thirds majority at a monthly progress meeting!

Performance budget tools:

*   [performancebudget.io](https://performancebudget.io/): estimate file sizes according to download timings
*   [bundlesize](https://github.com/siddharthkp/bundlesize): calculate file sizes during the build process
*   [SpeedCurve](https://speedcurve.com/): track real-world performance (commercial)

## Create a Style Guide

A style guide is a set of agreed brand, content, design, and coding standards for teams generally working on large codebases developed over a long period. A good style guide promotes consistency and illustrates how developers should approach solutions. Front-end components can be demonstrated with example code that shows styling, animation, functionality, and restrictions. The benefits include:

*   new team members can become productive quickly
*   components are reused: developers are less likely to introduce their own HTML, CSS, and JavaScript
*   it becomes easier to update, maintain, and improve component performance when the same code is used throughout
*   code can be tested and quality assurance becomes simpler
*   users receive a consistent UI experience

A style guide can be as rigid or as flexible as you require. It’s often best to develop it as a set of HTML pages that can demonstrate code and be updated quickly. Example documents are available from [styleguides.io](http://styleguides.io/).

## Simplify and Streamline

Performance problems often start because stakeholders equate more features with more customers. This is rarely the case; most people prefer simplicity. They’re not using your site/app on a daily basis and just want to get a task done quickly and easily.

Average page weight reached 2MB because developers let it happen. We’re under pressure to deliver more in a shorter time, but are we doing the job effectively when it results in a slow, clunky application no one wants to use? Few clients will understand the intricacies of web performance, so it’s our responsibility to use efficient coding practices and to highlight potential pitfalls in layman’s terms.

1.  Be wary of the performance cost of any added features.
2.  Use analytics to monitor and identify little-used features.
3.  Fully remove unnecessary features or replace them with sleeker, lightweight alternatives.

Look after the bytes and the megabytes will take care of themselves!

## Learn to Love the Web

The Web evolved from a document publishing platform to an application delivery system that revolutionized the way we distribute and use software. Unfortunately, this has resulted in an alarming tendency to over-engineer solutions when simpler options could be more effective. Rather than choose a native HTML control, we import the latest JavaScript module. Instead of adding a few styles, we copy vast quantities of CSS from Stack Overflow and Bootstrap.

If there’s one piece of advice to take away from this book, it’s *learn the basics*. Somewhat contradictorily, HTML and CSS are either disregarded as too simplistic to warrant respect or considered impenetrable technologies that must be fixed using JavaScript. Yet they’re the fundamental building blocks of the Web:

*   HTML5 has around 120 elements. Half of those will rarely be used, but there’s usually a better alternative to `<div>` and `<span>`.
*   There are almost 400 CSS3 properties and more are being added. No one could name them all, but they’re modularized. The foundations can be learned quickly, but experimentation and experience is required to understand the concepts.

Learning HTML and CSS will make you a better web developer and advance your JavaScript skills. A little knowledge will considerably improve your application’s performance.

# Chapter 6: How to Build and Structure a Node.js MVC Application

### by Nilson Jacques and James Kolce

In a non-trivial application, the architecture is as important as the quality of the code itself. We can have well-written pieces of code, but if we don’t have good organization, we’ll have a hard time as the complexity increases. There’s no need to wait until the project is half-way done to start thinking about the architecture; the best time is before starting, using our goals as beacons for our choices.

Node.js doesn’t have a de facto framework with strong opinions on architecture and code organization in the same way that Ruby has the Rails framework, for example. As such, it can be difficult to get started with building full web applications with Node.

In this tutorial, we’re going to build the basic functionality of a note-taking app using the MVC architecture. To accomplish this, we’re going to employ the [Hapi.js](https://hapi.dev/) framework for [Node.js](https://nodejs.org/en/) and [SQLite](http://www.sqlite.org/) as a database, using [Sequelize.js](https://sequelize.org/v3/), plus other small utilities, to speed up our development. We’re going to build the views using [Pug](https://pugjs.org/api/getting-started.html), the templating language.

## What is MVC?

Model-View-Controller (or MVC) is probably one of the most popular architectures for applications. As with a lot of other [cool things in computer history](https://youtu.be/NdSD07U5uBs?t=29m2s), the MVC model was conceived at [PARC](https://en.wikipedia.org/wiki/PARC_(company)) for the Smalltalk language as a solution to the problem of organizing applications with graphical user interfaces. It was created for desktop applications, but since then, the idea has been adapted to other mediums including the Web.

We can describe the MVC architecture in simple terms:

*   **Model**: the part of our application that will deal with the database or any data-related functionality.
*   **View**: everything the user will see—basically, the pages that we’re going to send to the client.
*   **Controller**: the logic of our site, and the glue between models and views. Here we call our models to get the data, then we put that data on our views to be sent to the users.

Our application will allow us to create, view, edit and delete plain-text notes. It won’t have other functionality, but because we’ll have a solid architecture already defined we won’t have a lot of trouble adding things later.

This tutorial assumes you have a recent version of Node installed on your machine. If this isn’t the case, please consult our [tutorial on getting up and running with Node](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/).

You can check out the final application in the [accompanying GitHub repository](https://github.com/sitepoint-editors/notes-board), so you get a general overview of the application structure.

## Laying out the Foundation

The first step when building any Node.js application is to create a `package.json` file, which is going to contain all of our dependencies and scripts. Instead of creating this file manually, npm can do the job for us using the `init` command:

```
mkdir notes-board
cd notes-board
npm init -y
```

After the process is complete, we’ll have a `package.json` file ready to use.

#### npm Commands

If you’re not familiar with these commands, check out our [Beginner’s Guide to npm](https://www.sitepoint.com/beginners-guide-node-package-manager/).

We’re going to proceed to install Hapi.js—the framework of choice for this tutorial. It provides a good balance between simplicity, stability and features that will work well for our use case (although there are other options that would also work just fine).

```
npm install @hapi/hapi@18.4.0
```

This command will download Hapi.js and add it to our `package.json` file as a dependency.

#### Versions

I’ve specified v18.4.0 of Hapi.js, as it’s compatible with Node versions 8, 10, and 12\. If you’re using Node 12, you can opt to install the latest version (Hapi v19.1.0).

Now we can create our entry file—the web server that will start everything. Go ahead and create a `server.js` file in your application directory and add the following code to it:

```
"use strict";

const Hapi = require("@hapi/hapi");
const Settings = require("./settings");

const init = async () => {
  const server = new Hapi.Server({ port: Settings.port });

  server.route({
    method: "GET",
    path: "/",
    handler: (request, h) => {
      return "Hello, world!";
    }
  });

  await server.start();
  console.log(`Server running at: ${server.info.uri}`);
};

process.on("unhandledRejection", err => {
  console.log(err);
  process.exit(1);
});

init();
```

This is going to be the foundation of our application.

First, we indicate that we’re going to use [strict mode](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode), which is a [common practice](https://hapi.dev/policies/styleguide/#strict-mode) when using the Hapi.js framework.

Next, we include our dependencies and instantiate a new server object where we set the connection port to `3000` (the port can be any number [above 1023 and below 65535](http://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xml)).

Our first route for our server will work as a test to see if everything is working, so a “Hello, world!” message is enough for us. In each route, we have to define the HTTP method and path (URL) that it will respond to, and a handler, which is a function that will process the HTTP request. The handler function can take two arguments: `request` and `h`. The first one contains information about the HTTP call, and the second will provide us with methods to handle our response to that call.

Finally, we start our server with the `server.start()` method.

## Storing Our Settings

It’s good practice to store our configuration variables in a dedicated file. This file exports a JSON object containing our data, where each key is assigned from an environment variable—but without forgetting a fallback value.

In this file, we can also have different settings depending on our environment (such as development or production). For example, we can have an in-memory instance of SQLite for development purposes, but a real SQLite database file on production.

Selecting the settings depending on the current environment is quite simple. Since we also have an `env` variable in our file which will contain either `development` or `production`, we can do something like the following to get the database settings:

```
const dbSettings = Settings[Settings.env].db;
```

So `dbSettings` will contain the setting of an in-memory database when the `env` variable is `development`, or will contain the path of a database file when the `env` variable is `production`.

Also, we can add support for a `.env` file, where we can store our environment variables locally for development purposes. This is accomplished using a package like [dotenv](https://www.npmjs.com/package/dotenv) for Node.js, which will read a `.env` file from the root of our project and automatically add the found values to the environment.

#### Using a `.env` File

If you decide to also use a `.env` file, make sure you install the package with `npm install dotenv` and add it to `.gitignore` so you don’t publish any sensitive information.

Our `settings.js` file will look like this:

```
// This will load our .env file and add the values to process.env,
// IMPORTANT: Omit this line if you don't want to use this functionality
require("dotenv").config({ silent: true });

module.exports = {
  port: process.env.PORT || 3000,
  env: process.env.NODE_ENV || "development",

  // Environment-dependent settings
  development: {
    db: {
      dialect: "sqlite",
      storage: ":memory:"
    }
  },
  production: {
    db: {
      dialect: "sqlite",
      storage: "db/database.sqlite"
    }
  }
};
```

Now we can start our application by executing the following command and navigating to [http://localhost:3000](http://localhost:3000) in our web browser:

```
node server.js
```

#### Up-to-date Install

This project was tested on Node v12.15.0\. If you get any errors, ensure you have an updated installation.

## Defining the Routes

The definition of routes gives us an overview of the functionality supported by our application. To create our additional routes, we just have to replicate the structure of the route that we already have in our `server.js` file, changing the content of each one.

Let’s start by creating a new directory called `lib` in our project. Here we’re going to include all the JS components.

Inside `lib`, let’s create a `routes.js` file and add the following content:

```
"use strict";
const Path = require("path");

module.exports = [
  // we’re going to define our routes here
];
```

In this file, we’ll export an array of objects that contain each route of our application. To define the first route, add the following object to the array:

```
{
  method: "GET",
  path: "/",
  handler: (request, h) => {
    return "All the notes will appear here";
  },
  config: {
    description: "Gets all the notes available"
  }
},
```

Our first route is for the home page (`/`), and since it will only return information, we assign it a `GET` method. For now, it will only give us the message “All the notes will appear here”, which we’re going to change later for a controller function. The `description` field in the `config` section is only for documentation purposes.

Then, we create the four routes for our notes under the `/note/` path. Since we’re building a [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) application, we’ll need one route for each action with the corresponding [HTTP methods](http://www.w3schools.com/tags/ref_httpmethods.asp).

Add the following definitions next to the previous route:

```
{
  method: "POST",
  path: "/note",
  handler: (request, h) => {
    return "New note";
  },
  config: {
    description: "Adds a new note"
  }
},
{
  method: "GET",
  path: "/note/{slug}",
  handler: (request, h) => {
    return "This is a note";
  },
  config: {
    description: "Gets the content of a note"
  }
},
{
  method: "PUT",
  path: "/note/{slug}",
  handler: (request, h) => {
    return "Edit a note";
  },
  config: {
    description: "Updates the selected note"
  }
},
{
  method: "GET",
  path: "/note/{slug}/delete",
  handler: (request, h) => {
    return "This note no longer exists";
  },
  config: {
    description: "Deletes the selected note"
  }
}
```

We’ve done the same as in the previous route definition, but this time we’ve changed the method to match the action we want to execute.

The only exception is the delete route. In this case, we’re going to define it with the `GET` method rather than `DELETE` and add an extra `/delete` in the path. This way, we can call the delete action just by visiting the corresponding URL.

#### Strict REST

If you plan to implement a strict REST interface, then you would have to use the `DELETE` method and remove the `/delete` part of the path.

We can name parameters in the path by surrounding the word in curly braces. Since we’re going to identify notes by a slug, we add `{slug}` to each path, with the exception of the `POST` route; we don’t need it there because we’re not going to interact with a specific note, but to create one.

You can read more about Hapi.js routes on the [official documentation](https://hapi.dev/tutorials/routing/?lang=en_US).

Now, we have to add our new routes to the `server.js` file. Let’s import the routes file at the top of the file:

```
const Routes = require("./lib/routes");
```

Then let’s replace our current test route with the following:

```
server.route(Routes);
```

## Building the Models

Models allow us to define the structure of the data and all the functions to work with it.

In this example, we’re going to use the [SQLite](https://www.sqlite.org/index.html) database with [Sequelize.js](https://sequelize.org/v3/), which is going to provide us with a better interface using the ORM ([Object-Relational Mapping](https://en.wikipedia.org/wiki/Object-relational_mapping)) technique. It will also provide us a database-independent interface.

### Setting up the Database

You can install SQLite and Sequelize by executing the following command:

```
npm install sequelize sqlite3
```

Now create a `models` directory inside `lib/` with a file called `index.js`, which is going to contain the database and Sequelize.js setup, and include the following content:

```
"use strict";

const Fs = require("fs");
const Path = require("path");
const Sequelize = require("sequelize");
const Settings = require("../../settings");
const dbSettings = Settings[Settings.env].db;

const sequelize = new Sequelize(
  dbSettings.database,
  dbSettings.user,
  dbSettings.password,
  dbSettings
);
const db = {};

Fs.readdirSync(__dirname)
  .filter(file => file.indexOf(".") !== 0 && file !== "index.js")
  .forEach(file => {
    const model = sequelize.import(Path.join(__dirname, file));
    db[model.name] = model;
  });

db.sequelize = sequelize;
db.Sequelize = Sequelize;

module.exports = db;
```

First, we include the modules that we’re going to use:

*   `Fs`, to read the files inside the `models` folder, which is going to contain all the models
*   `Path`, to join the path of each file in the current directory
*   `Sequelize`, which will allow us to create a new Sequelize instance
*   `Settings`, which contains the data of our `settings.js` file from the root of our project

Next, we create a new `sequelize` variable that will contain a `Sequelize` instance with our database settings for the current environment. We’re going to use `sequelize` to import all the models and make them available in our `db` object.

The `db` object is going to be exported and will contain our database methods for each model. It will be available in our application when we need to do something with our data.

To load all the models, instead of defining them manually, we look for all the files inside the `models` directory (with the exception of the `index.js` file) and load them using the `import` function. The returned object will provide us with the CRUD methods, which we then add to the `db` object.

At the end, we add `sequelize` and `Sequelize` as part of our `db` object. The first one is going to be used in our `server.js` file to connect to the database before starting the server, and the second one is included for convenience if you need it in other files too.

### Creating Our Note Model

In this section, we’re going to use the [Moment.js](http://momentjs.com/) package to help with date formatting. You can install it and include it as a dependency with the following command:

```
npm install moment
```

We’re going to create a `note.js` file inside the `models` directory, which is going to be the only model in our application. It will provide us with all the functionality we need.

Add the following content to that file:

```
"use strict";

const Moment = require("moment");

module.exports = (sequelize, DataTypes) => {
  const Note = sequelize.define("Note", {
    date: {
      type: DataTypes.DATE,
      get: function() {
        return Moment(this.getDataValue("date")).format("MMMM Do, YYYY");
      }
    },
    title: DataTypes.STRING,
    slug: DataTypes.STRING,
    description: DataTypes.STRING,
    content: DataTypes.STRING
  });

  return Note;
};
```

We export a function that accepts a `sequelize` instance, to define the model, and a `DataTypes` object with all the types available in our database.

Next, we define the structure of our data using an object where each key corresponds to a database column and the value of the key defines the type of data we’re going to store. You can see the list of data types in the [Sequelize.js documentation](http://docs.sequelizejs.com/en/latest/api/datatypes/). The tables in the database are going to be created automatically based on this information.

In the case of the date column, we also define a how Sequelize should return the value using a [getter](https://sequelize.org/master/manual/getters-setters-virtuals.html) function (`get` key). We indicate that before returning the information. It should be first passed through the Moment utility to be formatted in a more readable way (`MMMM Do, YYYY`).

#### A Non-destructive Operation

Although we’re getting a simple and easy-to-read date string, it’s stored as a precise date string product of JavaScript’s [Date](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Date) object. So this is not a destructive operation.

Finally, we return our model.

### Synchronizing the Database

We now have to synchronize our database before we’re able to use it in our application. In `server.js`, import the models at the top of the file:

```
// Import the index.js file inside the models directory
const Models = require("./lib/models/");
```

Next, remove the following code block:

```
await server.start();
console.log(`Server running at: ${server.info.uri}`);
```

Replace it with this one:

```
await Models.sequelize.sync();

await server.start();
console.log(`Server running at: ${server.info.uri}`);
```

This code is going to synchronize the models to our database. Once that’s done, the server will be started.

## Building the Controllers

Controllers are functions that accept the [request](https://hapi.dev/api#request-properties) and [response toolkit](https://hapi.dev/api/#response-toolkit) objects from Hapi.js. The `request` object contains information about the requested resource, and we use `reply` to return information to the client.

In our application, we’re going to return only a JSON object for now, but we’ll add the views once we build them.

We can think of controllers as functions that will join our models with our views; they will communicate with our models to get the data, and then return that data inside a view.

### The Home Controller

The first controller that we’re going to build will handle the home page of our site. Create a `home.js` file inside a `lib/controllers` directory with the following content:

```
"use strict";

const Models = require("../models/");

module.exports = async (request, h) => {
  const result = await Models.Note.findAll({
    order: [["date", "DESC"]]
  });

  return {
    data: {
      notes: result
    },
    page: "Home—Notes Board",
    description: "Welcome to my Notes Board"
  };
};
```

First, we get all the notes in our database using the [`findAll`](https://sequelize.org/master/manual/model-querying-basics.html) method of our model. This function will return a Promise and, if it resolves, we’ll get an array containing all the notes in our database.

We can arrange the results in descending order, using the `order` parameter in the options object passed to the `findAll` method, so the last item will appear first. You can check all the available options in the [Sequelize.js documentation](https://sequelize.org/master/class/lib/model.js~Model.html#static-method-findAll).

Once we have the home controller, we can edit our `routes.js` file. First, we import the module at the top of the file, next to the `Path` module import:

```
const Home = require("./controllers/home");
```

Then we add the controller we just made to the array:

```
{
  method: "GET",
  path: "/",
  handler: Home,
  config: {
    description: "Gets all the notes available"
  }
},
```

You can check things are working at this point by restarting the server (`node server.js`) and visiting [http://localhost:3000/](http://localhost:3000/). You should see the following response:

```
{
  "data": { "notes": [] },
  "page":"Home—Notes Board",
  "description":"Welcome to my Notes Board"
}
```

### Boilerplate of the Note Controller

Since we’re going to identify our notes with a slug, we can generate one using the title of the note and the [slug](https://www.npmjs.com/package/slug) library, so let’s install it and include it as a dependency with the following command:

```
npm install slug
```

The last controller that we have to define in our application will allow us to create, read, update, and delete notes.

We can proceed to create a `note.js` file inside the `lib/controllers` directory and add the following content:

```
"use strict";

const { Note } = require("../models/");
const Slugify = require("slug");
const Path = require("path");

module.exports = {
  // Here we’re going to include our functions that will handle the remaining requests in the routes.js file.
};
```

### The `create` Function

To add a note to our database, we’re going to write a `create` function that’s going to wrap the `create` method on our model using the data contained in the payload object.

Add the following inside the object that we’re exporting:

```
create: async (request, h) => {
  const result = await Note.create({
    date: new Date(),
    title: request.payload.noteTitle,
    slug: Slugify(request.payload.noteTitle, { lower: true }),
    description: request.payload.noteDescription,
    content: request.payload.noteContent
  });

  // Generate a new note with the 'result' data
  return result;
},
```

Once the note is created, we’ll get back the note data and send it to the client as JSON using the `reply` function.

For now, we just return the result, but once we build the views in the next section, we’ll be able to generate the HTML with the new note and add it dynamically on the client. Although this is not completely necessary and will depend on how you’re going to handle your front-end logic, we’re going to return an HTML block to simplify the logic on the client.

Also, note that the date is being generated on the fly when we execute the function, using `new Date()`.

### The `read` Function

To search just one element, we use the `findOne` method on our model. Since we identify notes by their slug, the `where` filter must contain the slug provided by the client in the URL (`http://localhost:3000/note/:slug:`):

```
read: async (request, h) => {
  const note = await Note.findOne({
    where: {
      slug: request.params.slug
    }
  });

  return note;
},
```

As in the previous function, we’ll just return the result, which is going to be an object containing the note information. The views are going to be used once we build them in the [Building the Views](#node11-ch6.xhtml_building-the-views) section.

### The `update` Function

To update a note, we use the `update` method on our model. It takes two objects—the new values that we’re going to replace, and the options containing a `where` filter with the note slug, which is the note that we’re going to update:

```
update: async (request, h) => {
  const values = {
    title: request.payload.noteTitle,
    description: request.payload.noteDescription,
    content: request.payload.noteContent
  };

  const options = {
    where: {
      slug: request.params.slug
    }
  };

  await Note.update(values, options);
  const result = await Note.findOne(options);

  return result;
},
```

After updating our data, since our database won’t return the updated note, we can find the modified note again to return it to the client, so we can show the updated version as soon as the changes are made.

### The `delete` Function

The delete controller will remove the note by providing the slug to the `destroy` function of our model. Then, once the note is deleted, we redirect to the home page. To accomplish this, we use the [redirect](https://hapi.dev/api/?v=18.4.0#-hredirecturi) function of Hapi’s response toolkit:

```
delete: async (request, h) => {
  await Note.destroy({
    where: {
      slug: request.params.slug
    }
  });

  return h.redirect("/");
}
```

### Using the Note Controller in Our Routes

At this point, we should have our note controller file ready with all the CRUD actions. But to use them, we have to include it in our routes file.

First, let’s import our controller at the top of the `routes.js` file:

```
const Note = require("./controllers/note");
```

We have to replace each handler with our new functions, so we should have our routes file as follows:

```
{
  method: "POST",
  path: "/note",
  handler: Note.create,
  config: {
    description: "Adds a new note",
    payload: {
      multipart: true,
    }
  }
},
{
  method: "GET",
  path: "/note/{slug}",
  handler: Note.read,
  config: {
    description: "Gets the content of a note"
  }
},
{
  method: "PUT",
  path: "/note/{slug}",
  handler: Note.update,
  config: {
    description: "Updates the selected note",
    payload: {
      multipart: true,
    }
  }
},
{
  method: "GET",
  path: "/note/{slug}/delete",
  handler: Note.delete,
  config: {
    description: "Deletes the selected note"
  }
}
```

#### Referencing without Calling

We’re including our functions without `()` at the end, because we’re referencing our functions without calling them.

In Hapi v19, [`request.payload.multipart` was changed to `false` by default](https://github.com/hapijs/hapi/issues/4017). We need to set it back to `true` for the `POST` and `PUT` routes, as we’ll be using a `FormData` object to transmit data to the server, and the transmitted data will be in the `multipart/form-data` format.

## Building the Views

At this point, our site is receiving HTTP calls and responding with JSON objects. To make it useful to everybody, we have to create the pages that render our information in a nice way.

In this example, we’re going to use the [Pug](https://pugjs.org/api/getting-started.html) (formerly Jade) templating language, although this isn’t mandatory, and we can use other languages with Hapi.js. We’re going to use the [Vision](https://github.com/hapijs/vision) plugin to enable the view functionality in our server.

#### Beginner’s Guide to Pug

If you’re not familiar with Jade/Pug, see our [Beginner’s Guide to Pug](https://www.sitepoint.com/a-beginners-guide-to-pug/).

You can install the packages with the following command:

```
npm install @hapi/vision@5.5.4 pug
```

Here we’re installing v5.5.4 of the vision plugin, which is compatible with Hapi v18\. If you’ve opted to install Hapi v19, you can simply type `npm i @hapi/vision` to pull in the latest version.

### The Note Component

First, we’re going to build the note component that’s going to be reused across our views. Also, we’re going to use this component in some of our controller functions to build a note on the fly in the back end to simplify the logic on the client.

Create a file in `lib/views/components` called `note.pug` with the following content:

```
article.content
  h2.title: a(href=`/note/${note.slug}`)= note.title
  p.subtitle.is-6 Published on #{note.date}
  p=note.content
```

It’s composed of the title of the note, the publication date and the content of the note.

### The Base Layout

The base layout contains the common elements of our pages—or in other words, for our example, everything that’s not content. Create a file in `lib/views/` called `layout.pug` with the following content:

```
doctype html
head
  meta(charset='utf-8')
  meta(name='viewport' content='width=device-width, initial-scale=1')
  title=page
  meta(name='description' content=description)
  link(rel='stylesheet' href='https://cdn.jsdelivr.net/npm/bulma@0.8.0/css/bulma.min.css')
  script(defer='' src='https://use.fontawesome.com/releases/v5.3.1/js/all.js')
body
  block content
  script(src='/scripts/main.js')
```

The content of the other pages will be loaded in place of `block content`. Also, note that we’ll display a page variable in the `title` element, and a `description` variable in the `meta(name='description')` element. We’ll create those variables in our routes later.

For styling purposes, we’re including the [Bulma CSS framework](https://bulma.io/) and [Font Awesome](https://fontawesome.com/) from a CDN. We’re also including a `main.js` file at the bottom of the page, which will contain all of our custom JavaScript code for the front end. Please create that file now in a `static/public/scripts/` directory.

### The Home View

On our home page, we’ll show a list of all the notes in our database and a button that will show a modal window with a form that allows us to create a new note via Ajax.

Create a file in `lib/views` called `home.pug` with the following content:

```
extends layout

block content
  section.section
    .container

      h1.title.has-text-centered
        | Notes Board

      .tabs.is-centered
        ul
          li
            a.show-modal(href='#') Publish

      main(container).notes-list
        each note in data.notes
          include components/note
          hr

      .modal
        .modal-background
        .modal-card
          header.modal-card-head
            p.modal-card-title Add note
            button.delete(aria-label='close')
          section.modal-card-body
            form(action='/note' method='POST').note-form#note-form
              .field
                .control
                  input.input(name='noteTitle' type='text' placeholder='Title')
              .field
                .control
                  input.input(name='noteDescription' type='text' placeholder='Short description')
              .field
                .control
                  textarea.textarea(name='noteContent' placeholder='Contents')
              .field
                .control
                  button.button.is-link Save
```

### The Note View

The note page is pretty similar to the home page, but in this case, we show a menu with options specific to the current note, the content of the note and the same form as in the home page, but with the current note information already filled, so it’s there when we update it.

Create a file in `lib/views` called `note.pug` with the following content:

```
extends layout

block content
  section.section
    .container
      h1.title.has-text-centered
          | Notes Board

      .tabs.is-centered
        ul
          li: a(href='/') Home
          li: a.show-modal(href='#') Update
          li: a(href=`/note/${note.slug}/delete`) Delete

      include components/note

      .modal
        .modal-background
        .modal-card
          header.modal-card-head
            p.modal-card-title Edit note
            button.delete(aria-label='close')
          section.modal-card-body
            form(action=`/note/${note.slug}` method='PUT').note-form#note-form
              .field
                .control
                  input.input(name='noteTitle' type='text' placeholder='Title' value=note.title)
              .field
                .control
                  input.input(name='noteDescription' type='text' placeholder='Short description' value=note.description)
              .field
                .control
                  textarea.textarea(name='noteContent' placeholder='Contents') #{note.content}
              .field
                .control
                  button.button.is-link Save
```

### The JavaScript on the Client

To create and update notes, we’ll use some JavaScript, both to show/hide a modal with a form, and to submit the requests via Ajax. Although this is not strictly necessary, we feel it provides a better experience for the user.

This is the content of our `main.js` file in the `static/public/scripts/` directory:

```
// Modal

const modal = document.querySelector(".modal");
const html = document.querySelector("html");

const showModal = () => {
  modal.classList.add("is-active");
  html.classList.add("is-clipped");
};

const hideModal = () => {
  modal.classList.remove("is-active");
  html.classList.remove("is-clipped");
};

document.querySelector("a.show-modal").addEventListener("click", function(e) {
  e.preventDefault();
  showModal();
});

modal.querySelector(".modal .delete").addEventListener("click", function(e) {
  e.preventDefault();
  hideModal();
});

// Form submition

const form = document.querySelector("#note-form");
const url = form.getAttribute("action");
const method = form.getAttribute("method");

const prependNote = html => {
  const notesList = document.querySelector(".notes-list");
  const div = document.createElement("div");
  div.innerHTML = html;
  notesList.insertBefore(div.firstChild, notesList.firstChild);
};

const updateNote = html => {
  const article = document.querySelector("article");
  const div = document.createElement("div");
  div.innerHTML = html;
  article.parentNode.replaceChild(div.firstChild, article);
};

const onSuccess = html => {
  hideModal();
  form.reset();

  if (method === "POST") {
    prependNote(html);
  } else if (method === "PUT") {
    updateNote(html);
  }
};

form.addEventListener("submit", e => {
  e.preventDefault();

  fetch(url, {
    method,
    body: new FormData(form)
  })
    .then(response => response.text())
    .then(text => onSuccess(text))
    .catch(error => console.error(error));
});
```

Every time the user submits the form in the modal window, we get the information from the form elements and send it to our back end, depending on the action URL and the method (`POST` or `PUT`). Then, we’ll get the result as a block of HTML containing our new note data. When we add a note, we’ll just add it on top of the list on the home page, and when we update a note we replace the content for the new one in the note view.

### Adding Support for Views on the Server

To make use of our views, we have to include them in our controllers and add the required settings.

In our `server.js` file, let’s import the Node [Path](https://nodejs.org/api/path.html) utility at the top of the file, since we’re using it in our code to indicate the path of our views:

```
const Path = require("path");
```

Now, replace the `server.route(Routes);` line with the following code block:

```
await server.register([require("@hapi/vision")]);

server.views({
  engines: { pug: require("pug") },
  path: Path.join(__dirname, "lib/views"),
  compileOptions: {
    pretty: false
  },
  isCached: Settings.env === "production"
});

// Add routes
server.route(Routes);
```

In the code we’ve added, we first register the [Vision](https://github.com/hapijs/vision) plugin with our Hapi.js server, which is going to provide the view functionality. Then we add the settings for our views—like the engine we’re going to use and the path where the views are located. At the end of the code block, we add our routes back in.

This will make our views work on the server, but we still have to declare the view that we’re going to use for each route.

### Setting the Home View

Open the `lib/controllers/home.js` file and replace the `return` statement with the following:

```
return h.view('home', {
  data: {
    notes: result
  },
  page: 'Home—Notes Board',
  description: 'Welcome to my Notes Board'
});
```

After registering the Vision plugin, we now have a `view` method available on the reply object. We’re going to use it to select the `home` view in our `views` directory and to send the data that’s going to be used when rendering the views.

In the data that we provide to the view, we also include the page title and a meta description for search engines.

If you’d like to try things out at this point, head to [http://localhost:3000/](http://localhost:3000/). You should see a nicely styled notes board, with a **Publish** button that doesn’t do anything.

### Setting the Note View: `create` Function

Right now, every time we create a note we send a JSON object from the server to the client. But since we’re doing this process with Ajax, we can send the new note as HTML ready to be added to the page. To do this, we render the *note* component with the data we have.

Start off by requiring Pug at the top of the `controllers/note.js` file:

```
const Pug = require("pug");
```

Then, in the `create` method, replace the line `return result;` with the following code block:

```
// Generate a new note with the 'result' data
return Pug.renderFile(
  Path.join(__dirname, "../views/components/note.pug"),
  {
    note: result
  }
);
```

We use the `renderFile` method from Pug to render the note template with the data we just received from our model.

### Setting the Note View: `read` Function

When we enter a note page, we should get the note template with the content of our note. To do this, we have to replace the `read` function’s `return note;` line with this:

```
return h.view("note", {
  note,
  page: `${note.title}—Notes Board`,
  description: note.description
});
```

As with the home page, we select a view as the first parameter and the data that we’re going to use as the second one.

### Setting the Note View: `update` Function

Every time we update a note, we’ll reply similarly to when we create new notes. Replace the `return result;` line in the `update` function with the following code:

```
// Generate a new note with the updated data
return Pug.renderFile(
  Path.join(__dirname, "../views/components/note.pug"),
  {
    note: result
  }
);
```

#### No View Required

The delete function doesn’t need a view, since it will just redirect to the home page once the note is deleted.

## Serving Static Files

The JavaScript and CSS files that we’re using on the client side are provided by Hapi.js from the `static/public/` directory. But it won’t happen automatically; we have to indicate to the server that we want to define this folder as public. This is done using the [Inert](https://github.com/hapijs/inert) package, which you can install with the following command:

```
npm install @hapi/inert
```

In the `server.register` function inside the `server.js` file, import the Inert plugin and register it with Hapi like this:

```
await server.register([require("@hapi/vision"), require("@hapi/inert")]);
```

Now we have to define the route where we’re going to provide the static files, and their location on our server’s filesystem. Add the following entry at the end of the exported object in `routes.js`:

```
{
  // Static files
  method: "GET",
  path: "/{param*}",
  handler: {
    directory: {
      path: Path.join(__dirname, "../static/public")
    }
  },
  config: {
    description: "Provides static resources"
  }
}
```

This route will use the `GET` method, and we’ve replaced the handler function with an object containing the directory that we want to make public.

You can find more information about serving static content in the [Hapi.js documentation](https://hapi.dev/tutorials/servingfiles/?lang=en_US).

## Conclusion

At this point, we have a very basic Hapi.js application using the MVC architecture. Although there are still things we should take care of before putting our application in production (such as input validation, error handling, error pages, and so on) this should work as a foundation to learn and build your own applications.

If you’d like to take this example a bit further, after finishing all the small details (not related the architecture) to make this a robust application, you could implement an authentication system so only registered users are able to publish and edit notes. But your imagination is the limit, so feel free to fork the [application repository](https://github.com/sitepoint-editors/notes-board) and go to town!

# Chapter 7: Local Authentication Using Passport in Node.js

### by Paul Orac

A common requirement when building a web app is to implement a login system, so that users can authenticate themselves before gaining access to protected views or resources. Luckily for those building Node apps, there’s a middleware called [Passport](http://www.passportjs.org/) that can be dropped into any [Express](https://expressjs.com/)-based web application to provide authentication mechanisms in only a few commands.

In this tutorial, I’ll demonstrate how to use Passport to implement local authentication (that is, logging in with a username and password) with a MongoDB back end. If you’re looking to implement authentication via the likes of Facebook or GitHub, please refer to [this tutorial](https://www.sitepoint.com/passport-authentication-for-nodejs-applications/).

As ever, all of the code for this article is available for download on [GitHub](https://github.com/sitepoint-editors/LocalPassportAuth).

## Prerequisites

To follow along with this tutorial, you’ll need to have Node and MongoDB installed on your machine.

You can install Node by heading to [the official Node download page](https://nodejs.org/en/download/) and grabbing the correct binaries for your system. Alternatively, you can use a version manager—a program that allows you to install multiple versions of Node and switch between them at will. If you fancy going this route, please consult our quick tip, “[Install Multiple Versions of Node.js Using nvm](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/)”.

MongoDB comes in various editions. The one we’re interested in is the MongoDB Community Edition.

The project’s home page has excellent documentation and I won’t try to replicate that here. Rather, I’ll offer you links to instructions for each of the main operating systems:

*   [Install MongoDB Community Edition on Windows](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/)
*   [Install MongoDB Community Edition on macOS](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/)
*   [Install MongoDB Community Edition on Ubuntu](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)

If you use a non-Ubuntu–based version of Linux, you can check out [this page](https://docs.mongodb.com/manual/installation/#mongodb-community-edition-installation-tutorials) for installation instructions for other distros. MongoDB is also normally available through the official Linux software channels, but sometimes this will pull in an outdated version.

#### Name and Address

You don’t need to enter your name and address to download MongoDB. If prompted, you can normally dismiss the dialog.

If you’d like a quick refresher on using MongoDB, check out our beginner’s guide, “[An Introduction to MongoDB](https://www.sitepoint.com/an-introduction-to-mongodb/)”.

## Authentication Strategies: Session vs JWT

Before we begin, let’s talk briefly about authentication choices.

Many of the tutorials online today will opt for token-based authentication using [JSON Web Tokens](https://www.sitepoint.com/using-json-web-tokens-node-js/) (JWTs). This approach is probably the simplest and most popular one nowadays. It relegates part of the authentication responsibility to the client and makes them sign a token that’s sent with every request, to keep the user authenticated.

Session-based authentication has been around longer. This method relegates the weight of the authentication to the server. It uses cookies and sees the Node application and database work together to keep track of a user’s authentication state.

In this tutorial, we’ll be using session-based authentication, which is at the heart of the [passport-local strategy](http://www.passportjs.org/packages/passport-local/).

Both methods have their advantages and drawbacks. If you’d like to read more into the difference between the two, [this Stack Overflow thread](https://stackoverflow.com/q/43452896) might be a good place to start.

## Creating the Project

Once all of the prerequisite software is set up, we can get started.

We’ll begin by creating the folder for our app and then accessing that folder on the terminal:

```
mkdir AuthApp
cd AuthApp
```

To create the node app, we’ll use the following command:

```
npm init
```

You’ll be prompted to provide some information for Node’s `package.json`. Just keep hitting `Return` to accept the default configuration (or use the `-y` flag).

## Setting up Express

Now we need to install [Express](http://expressjs.com/). Go to the terminal and enter this command:

```
npm install express
```

We’ll also need to install the [body-parser](https://www.npmjs.com/package/body-parser) middleware which is used to parse the request body that Passport uses to authenticate the user. And we’ll need to install the [express-session](https://www.npmjs.com/package/express-session) middleware.

Let’s do that. Run the following command:

```
npm install body-parser express-session
```

When that’s done, create an `index.js` file in the root folder of your app and add the following content to it:

```
/*  EXPRESS SETUP  */

const express = require('express');
const app = express();

app.use(express.static(__dirname));

const bodyParser = require('body-parser');
const expressSession = require('express-session')({
  secret: 'secret',
  resave: false,
  saveUninitialized: false
});

app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: true }));
app.use(expressSession);

const port = process.env.PORT || 3000;
app.listen(port, () => console.log('App listening on port ' + port));
```

First, we `require` Express and create our Express app by calling [express()](http://expressjs.com/en/api.html#express). Then we define the directory from which to serve our static files.

The next line sees us `require` the body-parser middleware, which will help us parse the body of our requests. We’re also adding the express-session middleware to help us save the session cookie.

As you can, see we’re configuring express-session with a `secret` to sign the session ID cookie (you should choose a unique value here), and two other fields, [resave](https://github.com/expressjs/session#resave) and [saveUninitialized](https://github.com/expressjs/session#saveuninitialized). The `resave` field forces the session to be saved back to the session store, and the `saveUninitialized` field forces a session that is “uninitialized” to be saved to the store. To learn more about them, check out their documentation, but for now it’s enough to know that for our case we want to keep them `false`.

Then, we use `process.env.PORT` to set the port to the environment port variable if it exists. Otherwise, we’ll default to `3000`, which is the port we’ll be using locally. This gives you enough flexibility to switch from development, directly to a production environment where the port might be set by a service provider like, for instance, [Heroku](https://www.heroku.com/). Right below that, we called [app.listen()](http://expressjs.com/en/api.html#app.listen) with the port variable we set up and a simple log to let us know that it’s all working fine and on which port is the app listening.

That’s all for the Express setup. Now it’s on to setting up `Passport`.

## Setting up Passport

First, we install Passport with the following command:

```
npm install passport
```

Then we need to add the following lines to the bottom of the `index.js` file:

```
/*  PASSPORT SETUP  */

const passport = require('passport');

app.use(passport.initialize());
app.use(passport.session());
```

Here, we require `passport` and initialize it along with its session authentication middleware, directly inside our Express app.

## Creating a MongoDB Data Store

Since we’re assuming you’ve already installed Mongo, you should be able to start the Mongo shell using the following command:

```
mongo
```

Within the shell, issue the following command:

```
use MyDatabase;
```

This simply creates a datastore named `MyDatabase`.

Leave the terminal there; we’ll come back to it later.

## Connecting Mongo to Node with Mongoose

Now that we have a database with records in it, we need a way to communicate with it from our application. We’ll be using [Mongoose](http://mongoosejs.com/) to achieve this. Why don’t we just use plain Mongo? Well, as the Mongoose devs like to say [on their website](https://mongoosejs.com/docs/unstable/index.html):

> writing MongoDB validation, casting and business logic boilerplate is a drag.

Mongoose will simply make our lives easier and our code more elegant.

Let’s go ahead and install it with the following command:

```
npm install mongoose
```

We’ll also be using [passport-local-mongoose](https://www.npmjs.com/package/passport-local-mongoose), which will simplify the integration between Mongoose and Passport for local authentication. It will add a `hash` and `salt` field to our Schema in order to store the hashed password and the salt value. This is great, as [passwords should never be stored as plain text in a database](https://security.stackexchange.com/a/120541).

Let’s install the package:

```
npm install passport-local-mongoose
```

Now we have to configure Mongoose. Hopefully you know the drill by now: add the following code to the bottom of your `index.js` file:

```
/* MONGOOSE SETUP */

const mongoose = require('mongoose');
const passportLocalMongoose = require('passport-local-mongoose');

mongoose.connect('mongodb://localhost/MyDatabase',
  { useNewUrlParser: true, useUnifiedTopology: true });

const Schema = mongoose.Schema;
const UserDetail = new Schema({
  username: String,
  password: String
});

UserDetail.plugin(passportLocalMongoose);
const UserDetails = mongoose.model('userInfo', UserDetail, 'userInfo');
```

Here we require the previously installed packages. Then we connect to our database using `mongoose.connect` and give it the path to our database. Next, we’re making use of a [Schema](http://mongoosejs.com/docs/guide.html) to define our data structure. In this case, we’re creating a `UserDetail` schema with `username` and `password` fields.

Finally, we add `passportLocalMongoose` as a plugin to our Schema. This will work part of the magic we talked about earlier. Then, we create a [model](http://mongoosejs.com/docs/models.html) from that schema. The first parameter is the name of the collection in the database. The second one is the reference to our Schema, and the third one is the name we’re assigning to the collection inside Mongoose.

That’s all for the Mongoose setup. We can now move on to implementing our Passport strategy.

## Implementing Local Authentication

And finally, this is what we came here to do! Let’s set up the local authentication. As you’ll see below, we’ll just write the code that will set it up for us:

```
/* PASSPORT LOCAL AUTHENTICATION */

passport.use(UserDetails.createStrategy());

passport.serializeUser(UserDetails.serializeUser());
passport.deserializeUser(UserDetails.deserializeUser());
```

There’s quite some magic going on here. First, we make `passport` use the local strategy by calling `createStrategy()` on our `UserDetails` model—courtesy of `passport-local-mongoose`—which takes care of everything so that we don’t have to set up the strategy. Pretty handy.

Then we’re using `serializeUser` and `deserializeUser` callbacks. The first one will be invoked on authentication, and its job is to serialize the user instance with the information we pass on to it and store it in the session via a cookie. The second one will be invoked every subsequent request to deserialize the instance, providing it the unique cookie identifier as a “credential”. You can read more about that in the [Passport documentation](http://www.passportjs.org/docs/configure/#sessions).

## Routes

Now let’s add some routes to tie everything together. First, we’ll add a final package. Go to the terminal and run the following command:

```
npm install connect-ensure-login
```

The [connect-ensure-login](https://www.npmjs.com/package/connect-ensure-login) package is middleware that ensures a user is logged in. If a request is received that is unauthenticated, the request will be redirected to a login page. We’ll use this to guard our routes.

Now, add the following to the bottom of `index.js`:

```
/* ROUTES */

const connectEnsureLogin = require('connect-ensure-login');

app.post('/login', (req, res, next) => {
  passport.authenticate('local',
  (err, user, info) => {
    if (err) {
      return next(err);
    }

    if (!user) {
      return res.redirect('/login?info=' + info);
    }

    req.logIn(user, function(err) {
      if (err) {
        return next(err);
      }

      return res.redirect('/');
    });

  })(req, res, next);
});

app.get('/login',
  (req, res) => res.sendFile('html/login.html',
  { root: __dirname })
);

app.get('/',
  connectEnsureLogin.ensureLoggedIn(),
  (req, res) => res.sendFile('html/index.html', {root: __dirname})
);

app.get('/private',
  connectEnsureLogin.ensureLoggedIn(),
  (req, res) => res.sendFile('html/private.html', {root: __dirname})
);

app.get('/user',
  connectEnsureLogin.ensureLoggedIn(),
  (req, res) => res.send({user: req.user})
);
```

At the top, we’re requiring `connect-ensure-login`. We’ll come back to this later.

Next, we set up a route to handle a POST request to the `/login` path. Inside the handler, we use the [passport.authenticate](http://www.passportjs.org/docs/authenticate/) method, which attempts to authenticate with the strategy it receives as its first parameter—in this case `local`. If authentication fails, it will redirect us to `/login`, but it will add a query parameter—`info`—that will contain an error message. Otherwise, if authentication is successful, it will redirect us to the `'/'` route.

Then we set up the `/login` route, which will send the login page. For this, we’re using [res.sendFile()](http://expressjs.com/en/api.html#res.sendFile) and passing in the file path and our root directory, which is the one we’re working on—hence the `__dirname`.

The `/login` route will be accessible to anyone, but our next ones won’t. In the `/` and `/private` routes we’ll send their respective HTML pages, and you’ll notice something different here. Before the callback, we’re adding the `connectEnsureLogin.ensureLoggedIn()` call. This is our route guard. Its job is validating the session to make sure you’re allowed to look at that route. Do you see now what I meant earlier by “letting the server do the heavy lifting”? We’re authenticating the user every single time.

Finally, we’ll need a `/user` route, which will return an object with our user information. This is just to show you how you can go about getting information from the server. We’ll request this route from the client and display the result.

Talking about the client, let’s do that now.

## The Client

The client should be quite simple. We’ll create some `HTML` pages and a `CSS` file. Let’s begin with the home page, or index. In your project root, create a folder called `html` and add a file called `index.html`. Add the following to it:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title> Home </title>
  <link rel="stylesheet" href="css/styles.css">
</head>

<body>
  <div class="message-box">
    <h1 id="welcome-message"></h1>
    <a href="/private">Go to private area</a>
  </div>

  <script>
    const req = new XMLHttpRequest();
    req.onreadystatechange = function () {
      if (req.readyState == 4 && req.status == 200) {
        const user = JSON.parse(req.response).user;
        document.getElementById("welcome-message").innerText = `Welcome ${user.username}!!`;
      }
    };
    req.open("GET", "http://localhost:3000/user", true);
    req.send();
  </script>
</body>
</html>
```

Here we have an empty `h1` tag where we’ll place our welcome message and, below that, a link to `/private`. The crucial part here is the `script` tag at the bottom where we’ll handle getting the username to create the welcome message.

This is divided into four parts:

1.  We instantiate the request object using `new XMLHttpRequest()`.
2.  We set the `onreadystatechange` property with the function that will be called after we get our answer. In the callback, we’re checking if we got a successful response and if so, we parse the response, get the user object (the one we sent in the `/user` route, remember?), and we find the `welcome-message` element to set its `innerText` to our `user.username`.
3.  We `open()` the `GET` request to the user `URL` and we set the last parameter to `true` to make it `asynchronous`.
4.  Finally, we `send()` the request.

Now we’ll create the login page. As before, in the HTML folder create a file called `login.html` and add the following content to it:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <title> Login </title>
  <link rel="stylesheet" href="css/styles.css">
</head>

<body>
  <form action="/login" method="post">
    <div class="title">
      <h3>Login</h3>
    </div>
    <div class="field">
      <label>Username:</label>
      <input type="text" name="username" />
      <br />
    </div>
    <div class="field">
      <label>Password:</label>
      <input type="password" name="password" required />
    </div>
    <div class="field">
      <input class="submit-btn" type="submit" value="Submit" required />
    </div>
    <label id="error-message"></label>
  </form>

  <script>
    const urlParams = new URLSearchParams(window.location.search);
    const info = urlParams.get('info');

    if(info) {
      const errorMessage = document.getElementById("error-message");
      errorMessage.innerText = info;
      errorMessage.style.display = "block";
    }
  </script>
</body>
</html>
```

On this page, we have a simple login form, with `username` and `password` fields, as well as a **Submit** button. Below that, we have a label where we’ll display any error messages. Remember, these are contained in the query string.

The `script` tag at the bottom is far simpler this time. We’re instantiating a `URLSearchParams` object passing the `window.location.search` property, which contains the parameters string in our URL. Then we use the `URLSearchParams.get()` method, passing in the parameter name we’re looking for.

At this point, we either have an info message or not. So if we do, we get the `error-message` element and set its `innerText` to whatever that message is, and then set its `style.display` property to `block`. This will make it visible, given that by default it has a `display: "none"` value.

Let’s set up the private page now. Again, create a file in the HTML folder with the name `private.html` and add the following content:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <title> Private </title>
  <link rel="stylesheet" href="css/styles.css">
</head>

<body>
  <div class="message-box">
    <h2>This is a private area</h2>
    <h3>Only you can see it</h3>
    <a href="/">Go back</a>
  </div>
</body>
</html>
```

Super simple. Just a simple message and a `Go back` link which takes us back to the homepage.

That’s it for the HTML, but as you probably noticed, we’re referencing a `CSS` file the `head` tags. Let’s add that file now. Create a folder called `css` in the root of our project and add a `styles.css` file to it, with the following content:

```
body {
  display: flex;
  align-items: center;
  background: #37474F;
  font-family: monospace;
  color: #cfd8dc;
  justify-content: center;
  font-size: 20px;
}

.message-box {
  text-align: center;
}

a {
  color: azure;
}

.field {
  margin: 10px;
}

input {
  font-family: monospace;
  font-size: 20px;
  border: none;
  background: #1c232636;
  color: #CFD8DC;
  padding: 7px;
  border: #4c5a61 solid 2px;
  width: 300px;
}

.submit-btn {
  width: 100%
}

.title {
  margin: 10px 0px 20px 10px
}

#error-message {
  color: #E91E63;
  display: block;
  margin: 10px;
  font-size: large;
  max-width: fit-content;
}
```

This will make our pages look decent enough. Let’s check it out!

Grab a terminal pointing to the project root and run the following command:

```
node index.js
```

Now navigate to [http://localhost:3000/](http://localhost:3000/) in your browser. You should be redirected to the login page. If you try to go to [http://localhost:3000/private](http://localhost:3000/private), it should redirect you to the login page again. There’s our route guard doing its job.

Press `Ctrl` + `C` in the terminal window to stop our server. Then head back to the `index.js` file and, at the bottom of the file, add the following lines:

```
/* REGISTER SOME USERS */

UserDetails.register({username:'paul', active: false}, 'paul');
UserDetails.register({username:'jay', active: false}, 'jay');
UserDetails.register({username:'roy', active: false}, 'roy');
```

This uses the passport-local-mongoose `register` method to salt the password for us. We just have to pass it in in plain text.

Now we run `node index.js`. The users will be created. You should comment those last lines now.

Remember the MongoDB shell terminal we left open? Go back to it and type:

```
db.userInfo.find()
```

This should show your three users and, as you can see, the salt and hash now occupy a good portion of the space on the terminal.

That’s all we need for the app to work. We’re done!

Head back to the browser, try to log in with one of the credentials we entered and you’ll see the login message with the given username in it.

## Next Steps

We only added the necessary modules for this app to work—nothing more, nothing less. For a production app, you’ll need to add other middleware and separate your code in modules. You can take that as a challenge to set up a clean and scalable environment and grow it into something useful!

The first and easiest thing you should try is adding the `logout`, using Passport’s [req.logout()](http://www.passportjs.org/docs/logout/) method.

Then you could try implementing a register flow. You’ll need a registration form and a route to talk to. You should use the `UserDetails.register()` we added earlier as a template. For email confirmation, you should check out [nodemailer](https://www.npmjs.com/package/nodemailer).

Another thing you could do is try to apply these concepts to a single page application. Perhaps using Vue.js and its router. And there goes your weekend!

## Conclusion

Well, we’re finally at the end. In this article, we learned how to implement local authentication using `Passport` in a `Node.js` application. In the process, we also learned how to connect to `MongoDB` using `Mongoose`.

Perhaps this wasn’t as easy for you as I tried to paint it, but at least you got to see that it gets easier with these tools that work some magic in the background, letting us worry only about what we’re trying to build.

“Magic” tools are not always ideal, but reputable and actively maintained tools help us write less code—and code you don’t write is code you don’t maintain, and code you don’t maintain is code you don’t break.

Also, keep in mind that if a tool is actively maintained by a core team, chances are they know what they’re doing better than any of us. Delegate whenever possible.

I hope you enjoyed this tutorial, and maybe got some inspiration for your next project. Happy coding!

# Chapter 8: How to Debug a Node App

### by Craig Buckler

Software development is complex and, at some point, your Node.js application will fail. If you’re *lucky*, your code will crash with an obvious error message. If you’re unlucky, your application will carry on regardless but not generate the results you expect. If you’re really unlucky, everything will work fine until the first user discovers a catastrophic disk-wiping bug.

## What is Debugging?

**Debugging** is the black art of fixing software defects. Fixing a bug is often easy—a corrected character or additional line of code solves the problem. Finding that bug is another matter, and developers can spend many unhappy hours trying to locate the source of an issue. Fortunately, Node.js has some great tools to help trace errors.

### Terminology

Debugging has its own selection of obscure jargon, including the following:

| Term | Explanation |
| --- | --- |
| breakpoint | the point at which a debugger stops a program so its state can be inspected |
| debugger | a tool which offers debugging facilities such as running code line by line to inspect internal variable states |
| feature | as in the claim: “it’s not a bug, it’s a feature”. All developers say it at some point during their career |
| frequency | how often or under what conditions a bug will occur |
| it doesn’t work | the most-often made but least useful bug report |
| log point | an instruction to a debugger to show the value of a variable at a point during execution |
| logging | output of runtime information to the console or a file |
| logic error | the program works but doesn’t act as intended |
| priority | where a bug is allocated on a list of planned updates |
| race condition | hard-to-trace bugs dependent the sequence or timing of uncontrollable events |
| refactoring | rewriting code to help readability and maintenance |
| regression | re-emergence of a previously fixed bug perhaps owing to other updates |
| related | a bug which is similar or related to another |
| reproduce | the steps required to cause the error |
| RTFM error | user incompetence disguised as a bug report, typically followed by a response to “Read The *Flipping* Manual” |
| step into | when running code line by line in a debugger, step into the function being called |
| step out | when running line by line, complete execution of the current function and return to the calling code |
| step over | when running line by line, complete execution of a command without stepping into a function it calls |
| severity | the impact of a bug on system. For example, data loss would normally be considered more problematic than a UI issue unless the frequency of occurrence is very low |
| stack trace | the historical list of all functions called before the error occurred |
| syntax error | typographical errors, such as `console.lug()` |
| user error | an error caused by a user rather than the application, but may still incur an update depending on that person’s seniority |
| watch | a variable to examine during debugger execution |
| watchpoint | similar to a breakpoint, except the program is stopped when a variable is set to a specific value |

## How to Avoid Bugs

Bugs can often be prevented before you test your application …

### Use a Good Code Editor

A good code editor will offer numerous features including line numbering, auto-completion, color-coding, bracket matching, formatting, auto-indentation, variable renaming, snippet reuse, object inspection, function navigation, parameter prompts, refactoring, unreachable code detection, suggestions, type checking, and more.

Node.js devs are spoiled for choice with free editors such as [VS Code](https://code.visualstudio.com/), [Atom](https://atom.io/), and [Brackets](http://brackets.io/), as well as plenty of commercial alternatives.

### Use a Code Linter

A linter can report code faults such as syntax errors, poor indentation, undeclared variables, and mismatching brackets before you save and test your code. The popular options for JavaScript and Node.js include [ESLint](https://eslint.org/), [JSLint](https://www.jslint.com/), and [JSHint](https://jshint.com/).

These are often installed as global Node.js modules so you can run checks from the command line:

```
eslint myfile.js
```

However, most linters have code editor plugins, such as [ESLint for VS Code](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) and [linter-eslint for Atom](https://atom.io/packages/linter-eslint) which check your code as you type:

![ESLint for VS Code](Images/eslint.png)

### Use Source Control

A source control system such as [Git](https://git-scm.com/) can help safe-guard your code and manage revisions. It becomes easier to discover where and when a bug was introduced and who should receive the blame! Online repositories such as [GitHub](https://github.com/) and [Bitbucket](https://bitbucket.org/) offer free space and management tools.

### Adopt an Issue-tracking System

*Does a bug exist if no one knows about it?* An issue-tracking system is used to report bugs, find duplicates, document reproduction steps, determine severity, calculate priorities, assign developers, record discussions, and track progress of any fixes.

Online source repositories often offer basic issue tracking, but [dedicated solutions](https://en.wikipedia.org/wiki/Comparison_of_issue-tracking_systems) may be appropriate for larger teams and projects.

### Use Test-driven Development

[Test-driven Development](https://www.sitepoint.com/learning-javascript-test-driven-development-by-example/) (TDD) is a development process which encourages developers to write code which tests the operation of a function before it’s written—for example, *is X returned when function Y is passed input Z*.

Tests can be run as the code is developed to prove a function works and spot any issues as further changes are made. That said, your tests could have bugs too …

### Step Away

It’s tempting to stay up all night in a futile attempt to locate the source of a nasty bug. Don’t. Step away and do something else. Your brain will subconsciously work on the problem and wake you at 4am with a solution. Even if that doesn’t happen, fresh eyes will spot that obvious missing semicolon.

## Node.js Debugging: Environment Variables

[Environment variables](https://nodejs.org/api/cli.html#cli_environment_variables) that are set within the host operating system can be used to control Node.js application settings. The most common is `NODE_ENV`, which is typically set to `development` when debugging.

Environment variables can be set on Linux/macOS:

```
NODE_ENV=development
```

Windows `cmd`:

```
set NODE_ENV=development
```

Or Windows Powershell:

```
$env:NODE_ENV="development"
```

Internally, an application will enable further debugging features and messages. For example:

```
// is NODE_ENV set to "development"?
const DEVMODE = (process.env.NODE_ENV === 'development');

if (DEVMODE) {
  console.log('application started in development mode on port ${PORT}');
}
```

`NODE_DEBUG` enables debugging messages using the Node.js `util.debuglog` (see below), but also consult the documentation of your primary modules and frameworks to discover further options.

Note that environment variables can also be saved to a `.env` file. For example:

```
NODE_ENV=development
NODE_LOG=./log/debug.log
SERVER_PORT=3000
DB_HOST=localhost
DB_NAME=mydatabase
```

Then loaded using the [`dotenv` module](https://www.npmjs.com/package/dotenv):

```
require('dotenv').config();
```

## Node.js Debugging: Command Line Options

Various [command-line options](https://nodejs.org/api/cli.html) can be passed to the `node` runtime when launching an application. One of the most useful is `--trace-warnings`, which outputs stack traces for process warnings (including deprecations).

Any number of options can be set, including:

*   `--enable-source-maps`: enable source maps (experimental)
*   `--throw-deprecation`: throw errors when deprecated features are used
*   `--inspect`: activate the V8 inspector (see below)

By way of an example, let’s try to log [the crypto module’s `DEFAULT_ENCODING` property](https://nodejs.org/api/crypto.html#crypto_crypto_default_encoding), which was deprecated in Node v10:

```
const crypto = require('crypto');

function bar() {
  console.log(crypto.DEFAULT_ENCODING);
}

function foo(){
  bar();
}

foo();
```

Now run this with the following:

```
node index.js
```

We’ll then see this:

```
buffer
(node:7405) [DEP0091] DeprecationWarning: crypto.DEFAULT_ENCODING is deprecated.
```

However, we can also do this:

```
node --trace-warnings index.js
```

That produces the following:

```
buffer
(node:7502) [DEP0091] DeprecationWarning: crypto.DEFAULT_ENCODING is deprecated.
    at bar (/home/Desktop/index.js:4:22)
    at foo (/home/Desktop/index.js:8:3)
    at Object.<anonymous> (/home/Desktop/index.js:11:1)
    at Module._compile (internal/modules/cjs/loader.js:1151:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1171:10)
    at Module.load (internal/modules/cjs/loader.js:1000:32)
    at Function.Module._load (internal/modules/cjs/loader.js:899:14)
    at Function.executeUserEntryPoint [as runMain] (internal/modules/run_main.js:71:12)
    at internal/main/run_main_module.js:17:47
```

This tells us that the deprecation warning comes from the code in line 4 (the `console.log` statement), which was executed when the `bar` function ran. The `bar` function was called by the `foo` function on line 8 and the `foo` function was called on line 11 of our script.

Note that the same options can also be passed to [nodemon](https://nodemon.io/).

## Console Debugging

One of the easiest ways to debug an application is to output values to the console during execution:

```
console.log( myVariable );
```

Few developers delve beyond this humble debugging command, but they’re missing out on [many more possibilities](https://nodejs.org/api/console.html), including these:

| `console` method | description |
| --- | --- |
| [`.log(msg)`](https://nodejs.org/api/console.html#console_console_log_data_args) | output a message to the console |
| [`.dir(obj,opt)`](https://nodejs.org/api/console.html#console_console_dir_obj_options) | uses [`util.inspect`](https://nodejs.org/api/util.html#util_util_inspect_object_options) to pretty-print objects and properties |
| [`.table(obj)`](https://nodejs.org/api/console.html#console_console_table_tabulardata_properties) | outputs arrays of objects in tabular format |
| [`.error(msg)`](https://nodejs.org/api/console.html#console_console_error_data_args) | output an error message |
| [`.count(label)`](https://nodejs.org/api/console.html#console_console_count_label) | a named counter reporting the number of times the line has been executed |
| [`.countReset[label]`](https://nodejs.org/api/console.html#console_console_countreset_label) | resets a named counter |
| [`.group(label)`](https://nodejs.org/api/console.html#console_console_group_label) | indents a group of log messages |
| [`.groupEnd(label)`](https://nodejs.org/api/console.html#console_console_groupend) | ends the indented group |
| [`.time(label)`](https://nodejs.org/api/console.html#console_console_time_label) | starts a timer to calculate the duration of an operation |
| [`.timeLog([label]`](https://nodejs.org/api/console.html#console_console_timelog_label_data) | reports the elapsed time since the timer started |
| [`.timeEnd(label)`](https://nodejs.org/api/console.html#console_console_timeend_label) | stops the timer and reports the total duration |
| [`.trace()`](https://nodejs.org/api/console.html#console_console_trace_message_args) | outputs a stack trace (a list of all calling functions) |
| [`.clear()`](https://nodejs.org/api/console.html#console_console_clear) | clear the console |

`console.log()` accepts a list of comma-separated values. For example:

```
let x = 123;
console.log('x:', x);
// x: 123
```

However, [ES6 destructuring](https://www.sitepoint.com/es6-destructuring-assignment/) can offer similar output with less typing effort:

```
console.log({x});
// { x: 123 }
```

Larger objects can be output as a condensed string using this:

```
console.log( JSON.stringify(obj) );
```

[`util.inspect`](https://nodejs.org/api/util.html#util_util_inspect_object_options) will format objects for easier reading, but `console.dir()` does the hard work for you.

## Node.js `util.debuglog`

The Node.js `util` module offers a built-in [`debuglog`](https://nodejs.org/api/util.html#util_util_debuglog_section) method which conditionally writes messages to `STDERR`:

```
const util = require('util');
const debuglog = util.debuglog('myapp');

debuglog('myapp debug message [%d]', 123);
```

When the `NODE_DEBUG` environment variable is set to `myapp` (or a wildcard such as `*` or `my*`), messages are displayed in the console:

```
NODE_DEBUG=myapp node index.js
MYAPP 9876: myapp debug message [123]
```

Here, `9876` is the Node.js process ID.

By default, `util.debuglog` is silent. If you were to run the above script without setting a `NODE_DEBUG` variable, nothing would be output to the console. This allows you to leave helpful debug logging in your code without cluttering the console for regular use.

## Debugging with Log Modules

Third-party logging modules are available should you require more sophisticated options for messaging levels, verbosity, sorting, file output, profiling, and more. Popular options include:

*   [cabin](https://www.npmjs.com/package/cabin)
*   [loglevel](https://www.npmjs.com/package/loglevel)
*   [morgan](https://www.npmjs.com/package/morgan) (Express.js middleware)
*   [pino](https://www.npmjs.com/package/pino)
*   [signale](https://www.npmjs.com/package/signale)
*   [storyboard](https://www.npmjs.com/package/storyboard)
*   [tracer](https://www.npmjs.com/package/tracer)
*   [winston](https://www.npmjs.com/package/winston)

## Node.js V8 Inspector

In the following sections, the [pagehit project](https://github.com/sitepoint-editors/pagehit-ram) developed in Chapter 2 is used to illustrate debugging concepts. You can download it with:

```
git clone https://github.com/sitepoint-editors/pagehit-ram
```

Or you can use any of your own code.

Node.js is a wrapper around the V8 JavaScript engine which includes its own [inspector and debugging client](https://nodejs.org/api/debugger.html). To start, use the `inspect` argument (not to be confused with `--inspect`) to start an application:

```
node inspect ./index.js
```

The debugger will pause at the first line and display a `debug>` prompt:

```
< Debugger listening on ws://127.0.0.1:9229/6f38abc1-8568-4035-a5d2-dee6cbbf7e44
< For help, see: https://nodejs.org/en/docs/inspector
< Debugger attached.
Break on start in index.js:7
  5 const
  6   // default HTTP port
> 7   port = 3000,
  8
  9   // Node.js modules
debug> 
```

You can step through the application by entering:

*   `cont` or `c`: continue execution
*   `next` or `n`: run the next command
*   `step` or `s`: step into a function being called
*   `out` or `o`: step out of a function and return to the calling command
*   `pause`: pause running code

Other options include:

*   watching variable values with [`watch('myvar')`](https://nodejs.org/api/debugger.html#debugger_watchers)
*   setting breakpoints with the [`setBreakpoint()`/`sb()` command](https://nodejs.org/api/debugger.html#debugger_breakpoints) (it is usually easier to insert a `debugger;` statement in your code)
*   `restart` a script
*   `.exit` the debugger (the initial `.` is required)

If this sounds horribly clunky, *it is*. Only use the built-in debugging client when there’s absolutely no other option, you’re feeling particularly masochistic, and you’re not using Windows (it’s often problematic).

## Node.js Debugging with Chrome

The Node.js inspector (without the debugger client) is started with the `--inspect` flag:

```
node --inspect ./index.js
```

#### `nodemon`

`nodemon` can be used instead of `node` if necessary.

This starts the debugger listening on `127.0.0.1:9229`, which any local debugging client can attach to:

```
Debugger listening on ws://127.0.0.1:9229/20ac75ae-90c5-4db6-af6b-d9d74592572f
```

If you’re running the Node.js application on another device or Docker container, ensure port `9229` is accessible and grant remote access using this:

```
node --inspect=0.0.0.0:9229 ./index.js
```

Alternatively, you can use `--inspect-brk` to set a breakpoint on the first statement so the application is paused immediately.

Open Chrome and enter `chrome://inspect` in the address bar.

![Chrome inspect](Images/chrome-inspect.png)

#### Remote Target

If the Node.js application does’t appear as a **Remote Target**, ensure **Discover network targets** is checked, then click **Configure** to add the IP address and port of the device where the application is running.

Click the Target’s **inspect** link to launch DevTools. It will be immediately familiar to anyone with browser debugging experience.

![Chrome DevTools](Images/chrome-devtools.png)

The **+ Add folder to workspace** link allows you to select where the Node.js files are located on your system, so it becomes easier to load other modules and make changes.

Clicking any line number sets a breakpoint, denoted by a green marker, which stops execution when that code is reached:

![Chrome DevTools breakpoint](Images/chrome-breakpoint.png)

Variables can be added to the **Watch** pane on the right by clicking the **+** icon and entering their name. Their value is shown whenever execution is paused.

The **Call Stack** pane shows which functions were called to reach this point.

The **Scope** pane shows the state of all available local and global variables.

The **Breakpoints** pane shows a list of all breakpoints and allows them to be enabled or disabled.

The icons above the **Debugger paused** message can be used to resume execution, step over, step into, step out, step through, deactivate all breakpoints, and pause on exceptions.

## Node.js Debugging with VS Code

VS Code Node.js debugging can be launched without any configuration when you’re running a Node.js application on your local system. Open the starting file (typically `index.js`), activate the **Run and Debug** pane, and click the **Run and Debug Node.js (F5)** button.

![VS Code debugger](Images/vscode-debug.png)

The debugging screen is similar to Chrome DevTools with a **Variables**, **Watch**, **Call stack**, **Loaded scripts**, and **Breakpoints** list.

![VS Code breakpoint](Images/vscode-breakpoint.png)

A breakpoint can be set by clicking the gutter next to the line number. You can also right-click.

![VS Code breakpoint options](Images/vscode-points.png)

With this right-click, you can set the following:

1.  A standard breakpoint.
2.  A conditional breakpoint which stops when criteria are met—for example, `count > 3`.
3.  A logpoint, which is effectively `console.log()` without code! Any string can be entered with expressions denoted in curly braces—for example, `{count}` to display the value of the `count` variable.

    ![VS Code logpoint](Images/vscode-logpoint.png)

#### Return

Don’t forget to hit `Return` for VS Code to create your conditional breakpoint or logpoint.

The debugging icon bar at the top can be used to resume execution, step over, step into, step out, restart, or stop the application and debugging. Identical options are also available from the **Debug** item in the menu.

For more information, refer to [Debugging in Visual Studio Code](https://code.visualstudio.com/docs/introvideos/debugging).

### Advanced Debugging Configuration

Further configuration is required when you’re debugging a remote service or need to use different launch options. VS Code stores launch configurations in a `launch.json` file generated inside the `.vscode` folder within your project. To generate or edit the file, click the cog icon at the top right of the **Run and Debug** pane.

![VS Code launch configuration](Images/vscode-launch.png)

Any number of configuration settings can be added to the `configurations` array. Click the **Add Configuration** button to choose an option. VS Code can either:

1.  **launch** a process using Node.js itself, or
2.  **attach** to a Node.js inspector process, perhaps running on a remote machine or Docker container

In the example above, a single Nodemon launch configuration has been defined. Save `launch.json`, select `nodemon` from the drop-down list at the top of the **Run and Debug** pane, and click the green start icon.

![VS Code launch](Images/vscode-launchconfig.png)

For further information, see [VS Code Launch configurations](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations).

## Other Node.js Debugging Tools

The [Node.js Debugging Guide](https://nodejs.org/en/docs/guides/debugging-getting-started/) provides advice for other IDEs and editors including Visual Studio, JetBrains, WebStorm, Gitpod, and Eclipse. Atom also has a [node-debug](https://atom.io/packages/node-debug) extension.

[ndb](https://github.com/GoogleChromeLabs/ndb) offers an *improved debugging experience* with powerful features such as attaching to child processes and script blackboxing so only code in specific folders is shown.

The [IBM report-toolkit for Node.js](https://github.com/ibm/report-toolkit) works by analyzing data output when `node` is run with the `--experimental-report` option.

Finally, commercial services such as [LogRocket](https://logrocket.com/) and [Sentry.io](https://sentry.io/) integrate with your live web application in both the client and the server to record errors as they’re encountered by users.

## Get Debugging!

Node.js has a range of great debugging tools and code analyzers which can improve the speed and reliability of your application. Whether or not they can tempt you away from `console.log()` is another matter!

# Chapter 9: Node Testing for Beginners

### by M. David Green

Does testing seem like an unwelcome intrusion on your development work day? Don’t worry, I get it.

If you started out not writing tests as part of your development process, testing can seem weird and complex. That’s especially true when you want to believe you’ve already got everything working. Nobody enjoys being confronted with proof of how brittle all the complex and intricate code they’ve spent the last few days (or years) polishing and perfecting might be.

Testing conjures up the need for a whole new parallel codebase, perhaps as large as the one you already have, in an unfamiliar syntax. And the notion of test-driven development might force you to think through your requirements results-first instead of jumping straight into the fun coding bits. Who needs that?

But testing isn’t as painful as you might have been led to believe. Even better, working in Node gives you the advantage of a mature development community that embraced testing early on. In fact, depending on how you integrate it into your workflow, testing can make it easier to clarify your intentions, increase your flexibility, and relieve much of your anxiety around the eventual need to maintain and update your code.

## What Testing Is

At its simplest, testing is just a way to verify whether your code does a thing that you think it does. You write a test that asks whether running your code with a particular input produces an expected output. Once you make that test pass, and you like the way your updated code looks, you write another test to make sure that a different input produces a different expected output.

And so on. Then eventually you have tests for every condition you need to verify. Once they all pass, you can be pretty confident that you’re done!

## Basic Assertion Testing Built In

If you’ve looked around at test frameworks to use in Node, you may have noticed that there are several to choose from. It’s not easy for someone new to testing to decide which one makes the most sense for your purposes.

We’ll introduce you to a few of the more popular testing frameworks later in this guide. But to get started right away, you don’t need to worry about any of that. Node comes with a built-in assertion testing capability you can use immediately, just by requiring `assert`.

### The Existential Assertion

To see how `assert` works, we can start by creating a new directory for our application and its tests. In this case, we might know we’ll need functionality to test whether a number is even. That’s a pretty basic bit of functionality, but I want to keep this example simple so we can focus on how we test. What we’ll learn here will apply to more complex requirements as well.

To keep ourselves somewhat organized as we start to write our new application, we would first create a file called `tests.js` to keep all our tests in one place. The first step in our testing plan is to capture our first requirement without even making sure that the function we’re going to want to call exists. (And we know it doesn’t because we haven’t written it yet.)

```
const assert = require('assert');
const isFourEven = isEven(4);

assert(isFourEven, 'isEven(4) does not return falsy');
```

It’s just three lines of test code, but we’ve already started making some architectural assumptions about how we’re planning to write our application. Our first two lines set us up for testing, and our third line runs the first test.

We started by defining a local `assert` constant which gives us access to Node’s default assert functionality. In all of our tests, we’ll be using our `assert` to determine whether a behavior we’re looking for exists and is doing what we expect it to do.

In the second line we decided that we’re going to want to have an `isEven()` method somewhere in our code that we can call. For the sake of our test, we also want to create a constant containing the result of passing a specific value, `4`, to our proposed `isEven()` method.

Looking objectively at what we’ve written, we would expect a working `isEven()` method to produce a result of `true` when called with the value `4`. So we’re including a test to assert that behavior. The third line calls our `assert` method, passing in two parameters. The first parameter is our new constant with the result of calling `isEven(4)`, and the second is a message we want returned if the test fails, meaning the value in the first parameter is “[falsy](https://www.sitepoint.com/javascript-truthy-falsy/)” according to `assert`. **Falsy** is very broadly defined to mean it contains a value of `false`, `0`, an empty string, `Undefined`, `NaN`, or `null`.

Now, before we do anything else such as write an `isEven()` method, we can run these tests. We want to make sure our test fails so we can trust that writing a working `isEven()` will show us that we can make it pass. So with our terminal pointing to the same directory, type `node tests.js` and hit enter. You should get something like the following output:

```
$ node tests.js
/Users/david/Documents/node/node-testing-for-beginners/tests.js:2
const isFourEven = isEven(4);
                 ^

ReferenceError: isEven is not defined
    at Object.<anonymous> (/Users/david/Documents/node/node-testing-for-beginners/tests.js:2:18)
    at Module._compile (internal/modules/cjs/loader.js:955:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:991:10)
    at Module.load (internal/modules/cjs/loader.js:811:32)
    at Function.Module._load (internal/modules/cjs/loader.js:723:14)
    at Function.Module.runMain (internal/modules/cjs/loader.js:1043:10)
    at internal/main/run_main_module.js:17:11
```

This output is telling us a lot based on the expectations we described in our test, and guiding us toward the next step in writing our application.

At the end of the first line is a filename followed by a colon and a line number. This tells us that we had an assertion failure on line `2` in our `tests.js` file.

Next `assert` shows us the code on that line, and even highlights where we’re likely to find the error with a `^` on the next line pointing to the appropriate spot.

After that, we get a quick indented error trace, starting an unindented line telling us the kind of error we experienced and what it means. That’s usually enough information to jump in and start doing what’s needed to make our failing test pass. In this case, we’re being told that “isEven” is not defined.

So let’s define it!

```
const assert = require('assert');
const isFourEven = isEven(4);
const isEven = (value) => true;

assert(isFourEven, 'isEven(4) does not return falsy');
```

We’ve added what we believe to be the bare minimum code that we need in order to get our test to pass. We’ve defined an `isEven()` method that always returns `true`, since we only have one test and all it needs is a return value of `true`.

That may sound a little weird, but stick with me. Our pattern of iterative testing will tell us what we need to do next to get our `isEven()` method working the way we need it to reliably and consistently. Until it does, we’re better off writing as little code as we can to make the test we have pass. Otherwise, we may be writing more than we need, and creating behavior that isn’t supported by any test at all.

Now when we run `node tests.js` in the terminal, we get no output. And that’s a good thing! That means that all the tests in our `tests.js` file passed and there was nothing to show us.

(This would be a good time to commit our code using our preferred version control system, such as [Git](https://www.sitepoint.com/git-for-beginners/), but that’s a separate topic.)

At this point I think we can all agree that it’s a little unusual to put our application code into our `tests.js` file. We need a more practical place to keep our application code separate from our tests. And since we have our test passing, we can now safely refactor.

We may anticipate that we’ll define more than just this one function, and may eventually need a way to keep them organized. So we might as well start simply by creating an `app.js` file in the same directory as our `tests.js` file, and moving the code for our an `isEven()` function there, making sure to export it with an appropriate name:

```
const isEven = (value) => true;

module.exports = {
  isEven
};
```

Since the method we want to test is now in a separate `app.js` file, we need to `require` that file in our `tests.js` file. We’ll do that by adding a new `const` definition that pulls in our `isEven` from the module exports of `app.js`:

```
const assert = require('assert');
const { isEven } = require('./app');
const isFourEven = isEven(4);

assert(isFourEven, 'isEven(4) does not return falsy');
```

Now when we run `node tests.js` in the terminal, again we get no result, meaning that our test still passes with our refactored code. Imagine doing this kind of refactoring in a more complex application and you can see right away why you might want to have tests in place to make sure you haven’t broken any functionality in the process.

Again, it’s a good time to commit to our version control system.

### Asserting Equality

But does that mean we’re done? In some cases it might. But in our case I think we can all agree that our one test isn’t running our code through all the likely values we might expect to encounter. Let’s write a second test now:

```
const assert = require('assert');
const { isEven } = require('./app');
const isFourEven = isEven(4);
const isFiveEven = isEven(5);

assert(isFourEven, 'isEven(4) does not return falsy');
assert.equal(isFiveEven, false, 'isEven(5) returns true');
```

We’ve defined a new constant—`isFiveEven`—to carry the value returned when we run `isEven()` with a value of `5`. Rationally, we’d expect that to return `false`. But we already know our `isEven()` method is hard-coded to return `true` in every case. So we’ve used `assert.equal()` for our assertion to test whether our `isFiveEven` constant matches the value `false`.

A plain `assert` only verifies that a result passed to it is not falsy. We’re taking advantage of a more specific assertion matcher by using `assert.equal()`, which takes three parameters: a value to test, a desired value to compare it against, and a failure message.

When we run `node tests.js` in the terminal, we now get this output:

```
$ node tests.js
assert.js:92
  throw new AssertionError(obj);
  ^

AssertionError [ERR_ASSERTION]: isEven(5) returns true
    at Object.<anonymous> (/Users/david/Documents/node/node-testing-for-beginners/tests.js:7:8)
    at Module._compile (internal/modules/cjs/loader.js:955:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:991:10)
    at Module.load (internal/modules/cjs/loader.js:811:32)
    at Function.Module._load (internal/modules/cjs/loader.js:723:14)
    at Function.Module.runMain (internal/modules/cjs/loader.js:1043:10)
    at internal/main/run_main_module.js:17:11 {
  generatedMessage: false,
  code: 'ERR_ASSERTION',
  actual: true,
  expected: false,
  operator: '=='
}
```

The output looks a little different, but we can read it the same way as before. We can see that there was an `AssertionError` and that doesn’t tell us much by itself. We can also see that “isEven(5) returns true” according to the start of the error trace. That’s the test failure message we wrote for ourselves. Below the trace we can see more details about what message was generated, the actual and expected values, and even the comparison operator used.

With all this, we know that we need to improve our `isEven()` method to handle this new case. We have two tests defined that address our two most likely scenarios of even and odd numbers. Once we get both tests passing we’ll know a lot about the functionality of our new method.

There are a few ways to modify `isEven()` in our `app.js` file, but one simple approach to get both our tests to pass might be changing the definition to this:

```
const isEven = (value) => value % 2 === 0;
```

Now `isEven()` takes in a value and returns the result of applying `% 2` to the value and seeing if the remainder equals `0`. With that change, running `node tests.js` in our terminal now returns nothing—which means both our tests passed!

Now that your tests are all passing again, this is another a good time to commit your code to version control if you’re doing that, and to look for any ways you might want to refactor.

### Testing Edge Cases

Depending on the desired resiliency of our code, we may be done. The question to ask is whether our application’s behavior meets the acceptance criteria we agreed to before we started coding. For example, what if `isEven()` gets called with something other than an integer? Do we think it might be called with a floating point value? A negative number? How about a string? Could we find it getting called with no value at all passed in, an object, or `NaN`?

With the basic `assert` functionality built into Node, we now know we can write tests for any of these scenarios to see what happens. And if all the tests pass, we can trust the functionality of our code in all these scenarios. If one of them fails, we’ll get direction from the failure message telling us what we need to do next.

For example, let’s see what happens if we pass a string to our `isEven()` method. We’ll start by adding two lines to our `tests.js` file—one to define a new constant, and another to test a new assertion to see if it will fail:

```
const assert = require('assert');
const { isEven } = require('./app');
const isFourEven = isEven(4);
const isFiveEven = isEven(5);
const isStringEven = isEven("A");

assert(isFourEven, 'isEven(4) does not return falsy');
assert.equal(isFiveEven, false, 'isEven(5) returns true');
assert.equal(isStringEven, false, 'isEven("A") returns true');
```

Running `node tests.js` in our terminal after adding that test produces no result. That means our method is cleanly rejecting strings. This is good news, and another opportunity to commit to our version control system.

At this point we could add more tests for this method, or if we’re feeling confident that we’ve covered all the likely edge cases, we could refactor our code or start writing the first test for the next bit of behavior we’ll need.

## Structuring Your Tests

We’ve already written more test code than application code, but it’s pretty clear why we need everything we’ve written. And you can probably see already that writing all of your tests this way could start to make your test code pretty unreadable.

Our tests are all sitting at the same level in our `test.js` file, with our constants being declared further and further away from our assertions. Imagine trying to build out all the necessary tests for any real-world application with organization like this.

Ideally our tests should read like documentation, explaining clearly what we want each aspect of the code to do, and providing concrete examples of how it should behave under different conditions. A single flat file with no structure isn’t going to cut it.

To help address this concern, software tests are usually organized into patterns that make them easier to read, maintain, and run efficiently. It’s all about grouping like tests together logically, providing them with the resources they need to run the same way every time, and calling them in an organized way so you always know what you’re testing.

As you start researching potential frameworks and thinking about how they might help you take advantage of your new test writing superpowers, it might help if we define a few terms.

### Test Cases

What we’ve been writing in this guide are test cases. Each behavioral requirement usually calls for at least two test cases: one to show we get the expected result with the correct data, and one to prove that we don’t get the expected result with the wrong data.

### Test Suites

Once we have a set of test cases defined, we may want to keep them organized by defining a **test suite**. This can be a section of code within a test file, a separate file with a set of related tests, or even a nested directory structure depending on how complex your needs are. Different testing frameworks recommend different ways of structuring and organizing test code, but the same concepts apply regardless.

### Test Harnesses

A **test harness** is a system of organization and facilities that supports an automated approach for running a set of test cases consistently within any framework. The harness should include any resources and data necessary to populate and execute the tests the same way every time, so they can be checked for consistent results.

### Fixtures

A **fixture** helps define all the setup required to initialize a system for software testing in a specific fixed context. Defining the context before each test is run is essential, so you always know you’re starting from the same place with all the same inputs and resources. Otherwise, your tests could produce different results every time you run them, even if the code you’re testing hasn’t changed.

### Test Doubles

In the real world, our software may have complex, brittle, resource-intensive dependencies. We can’t always rely on having access to these in every environment where we want to run our tests. They may be too expensive to keep running just for testing purposes, they may rely on sensitive data that would be difficult to version and update if we made a mistake, or they may simply not be available in our testing environment due to regulations and other practical issues.

But we still need to make sure our code will work as expected under any of these conditions. That’s where test doubles such as mocks and stubs come in handy. They simulate real-world contexts so we don’t need to have the real thing handy all the time.

A **mock** sits inside of our test fixture and simulates the behavior of a real-world object our test may be expecting. Any call for that real-world object in our test gets intercepted and provided with the mock object we’ve created. This is very useful when the real-world object might vary depending on the time when it was called, the precise state of a complex system with many moving parts, a slow or expensive data source that would keep our tests from running efficiently as often as we need them to, or even a resource that hasn’t been created yet.

A **stub** provides similar artificial results as a mock, but for functions and methods. All calls to a given method are intercepted, providing instead a call to the stubbed version of that method. We can program stubs to be as simple as we need them to be to support the needs of our testing environment.

There are other test doubles as well that do things like provide feedback about the return values of code while it’s running. Some testing frameworks come with the ability to define many types of test doubles, or can be extended to include more than you get by default. Once you dive into the world of software testing, you may be amazed to discover what’s possible.

You could try writing all the tools to handle these testing needs yourself, or you could opt for an off-the-shelf testing framework with all the bells and whistles. So let’s talk about some of the options you have in the Node world.

## Frameworks for Automated Testing

Once we decide that we need to graduate from the built-in `assert` functionality of Node and start using a dedicated testing framework, we’re presented with a wide range of options. And there’s a lot of overlap across the various options, since they all do similar things in slightly different ways to suit different types of development. We can consider these in terms of their superlatives.

### Jasmine is the Oldest

Dating back to the pre-2010 days when JavaScript was primarily known as a browser-based, front-end development solution, [Jasmine](https://jasmine.github.io/) has a long history of bringing behavior-driven development to the community. It’s kept up well with the Node ecosystem, and remains a viable option.

Jasmine works great standalone, but you’ll need to rely on a separate test runner like [Karma](https://karma-runner.github.io/2.0/index.html) for deeper automation of test suites. It’s battle-tested and well documented, so you can usually find help when you need it.

### Jest is the Most Popular

One of the fastest ways to get started testing your Node apps these days is with [Jest](https://jestjs.io/), which is a relative newcomer to the Node testing scene. Its fast rise to popularity may be due to its roots in the Facebook engineering community, where [React](https://reactjs.org/) came from, and its associated ease of use for both server- and client-side React development.

If you’re an old-school JavaScript developer familiar with tools like Jasmine, you might notice a lot of similarities, since Facebook used Jasmine as a foundation when they built Jest. But Jest has been completely reworked from the inside out to provide faster, cleaner, and easier-to-manage tests.

### Mocha/Chai is the Most Comprehensive

While [Mocha](https://mochajs.org/) requires more configuration than some other solutions, and can take advantage of Node’s built in `assert` method, it also has access to a wider toolset when paired with the [Chai](https://www.chaijs.com/) library of assertions. Because it’s been around longer and has a well-supported suite of potential plugins, it may be the most versatile testing option.

Mocha relies on you to tell it what you need it to do to support all the features and behaviors you may desire. In exchange, it gives you access to a wide range of plugins and extensions that can grow with you as your testing needs mature, as well as a deep community of users to call on if you need help.

### Cypress is the Newest

Taking advantage of the end-to-end nature of modern Node development, [Cypress](https://www.cypress.io/) provides an integrated way to test your application from the back end to the browser. Cypress does away with older tools like Selenium to check what’s happening on the front end, and it’s built on top of Mocha and Chai.

Cypress [has been criticized](https://help.testim.io/docs/why-not-cypress) for trying to control everything in JavaScript at a potential cost to its versatility, and carrying forward some baggage from older legacy JavaScript apis. That may or may not be an issue for most use cases, and it’s being actively developed and supported, so it’s definitely an option worth checking out.

## Get Started Now

Testing can seem like an unwelcome intrusion on your work if you haven’t done it before. That’s true whether you’re a web development pioneer from the days when the idea of using JavaScript on the server seemed bizarre, or a fresh-faced explorer born into a world already used to the convenience of Node’s single-language, end-to-end development.

But any amount of testing is better than nothing. You wouldn’t stroll casually out onto a frozen lake without at least poking the ice ahead of you with a toe to see if it’s thick enough to keep you from falling in. Doesn’t your application deserve at least as much care?

No matter how big and unwieldy your code is now, it’s never a bad time to start writing tests. Write a few tests for every new piece of functionality you add. Write some tests to verify the most critical behaviors so you can be reassured that they won’t break as your code evolves. Start out just using `assert` in a flat file right now if that’s all you have. You can always refactor into something more sophisticated when you need it. Just get started!

# Chapter 10: How to Use SSL/TLS with Node.js

### by Florian Rappl and Almir Bijedic

In 2020, there’s no reason for your website not to use HTTPS. Visitors expect it, Google uses it as a ranking factor and browser makers will happily name and shame those sites not using it.

In this tutorial, I’ll walk you through a practical example of how to add a [Let’s Encrypt](https://letsencrypt.org/)–generated certificate to your Express.js server.

But protecting our sites and apps with HTTPS isn’t enough. We should also demand encrypted connections from the servers we’re talking to. We’ll see that possibilities exist to activate the SSL/TLS layer even when it’s not enabled by default.

#### SSL with NGINX

If you’re looking for instructions on how to set up SSL with NGINX when configuring it to work as a reverse proxy for a Node app, check out our quick tip, “[Configuring NGINX and SSL with Node.js](https://www.sitepoint.com/configuring-nginx-ssl-node-js/)”.

Let’s start with a short review of the current state of HTTPS.

## HTTPS Everywhere

[The HTTP/2 specification](https://en.wikipedia.org/wiki/HTTP/2) was published as RFC 7540 in May 2015, which means at this point it’s a part of the standard. This was a major milestone. Now we can all upgrade our servers to use HTTP/2\. One of the most important aspects is the backwards compatibility with HTTP 1.1 and the negotiation mechanism to choose a different protocol. Although the standard doesn’t specify mandatory encryption, currently no browser supports HTTP/2 unencrypted. This gives HTTPS another boost. Finally we’ll get HTTPS everywhere!

What does our stack actually look like? From the perspective of a website running in the browser (at the application level) we have to traverse the following layers to reach the IP level:

1.  Client browser
2.  HTTP
3.  SSL/TLS
4.  TCP
5.  IP

HTTPS is nothing more than the HTTP protocol on top of SSL/TLS. Hence all of HTTP’s rules still apply. What does this additional layer actually give us? There are multiple advantages: we get authentication by having keys and certificates; a certain kind of privacy and confidentiality is guaranteed, as the connection is encrypted in an asymmetric manner; and data integrity is also preserved, as transmitted data can’t be changed during transit.

One of the most common myths is that using SSL/TLS is computationally expensive and slows the server down. This is certainly not true anymore. We also don’t need any specialized hardware with cryptography units. Even for Google, [the SSL/TLS layer accounts for less than 1% of the CPU load and the the network overhead of HTTPS as compared to HTTP is below 2%](https://www.imperialviolet.org/2010/06/25/overclocking-ssl.html). All in all, it wouldn’t make sense to forgo HTTPS for the sake of a little overhead.

As Ilya Grigorik puts it, there is but one performance problem:

> TLS has exactly one performance problem: it is not used widely enough. Everything else can be optimized.

The most recent version is TLS 1.3\. TLS is the successor of SSL, which is available in its latest release SSL 3.0\. The changes from SSL to TLS preclude interoperability, but the basic procedure is, however, unchanged. We have three different encrypted channels. The first is a public key infrastructure for certificate chains. The second provides public key cryptography for key exchanges. Finally, the third one is symmetric. Here we have cryptography for data transfers.

TLS 1.3 uses hashing for some important operations. Theoretically, it’s possible to use any hashing algorithm, but it’s highly recommended to use SHA2 or a stronger algorithm. SHA1 has been a standard for a long time but has recently become obsolete.

HTTPS is also gaining more attention for clients. Privacy and security concerns have always been around, but with the growing amount of online accessible data and services, people are getting more and more concerned. For those sites that don’t implement it, there is a useful browser extension—[HTTPS Everywhere from the EFF](https://www.eff.org/https-everywhere)—which encrypts our communications with most websites.

![HTTPS-everywhere](Images/https-everywhere.png)

The creators realized that many websites offer HTTPS only partially. The plugin allows us to rewrite requests for those sites that offer only partial HTTPS support. Alternatively, we can also block HTTP altogether (see the screenshot above).

## Basic Communication

The certificate’s validation process involves validating the certificate signature and expiration. We also need to verify that it chains to a trusted root. Finally, we need to check to see if it’s been revoked. There are dedicated, trusted authorities in the world that grant certificates. In case one of these were to become compromised, all other certificates from the said authority would get revoked.

The sequence diagram for an HTTPS handshake looks as follows. We start with the initialization from the client, which is followed by a message with the certificate and key exchange. After the server sends its completed package, the client can start the key exchange and cipher specification transmission. At this point, the client is finished. Finally the server confirms the cipher specification selection and closes the handshake.

![HTTPS-sequence](Images/sequence.png)

The whole sequence is triggered independently of HTTP. If we decide to use HTTPS, only the socket handling is changed. The client is still issuing HTTP requests, but the socket will perform the previously described handshake and encrypt the content (header and body).

So what do we need to make SSL/TLS work with an Express.js server?

## HTTPS

By default, Node.js serves content over HTTP. But there’s also an [HTTPS module](https://nodejs.org/api/https.html) that we have to use in order to communicate over a secure channel with the client. This is a built-in module, and the usage is very similar to how we use the HTTP module:

```
const https = require("https"),
  fs = require("fs");

const options = {
  key: fs.readFileSync("/srv/www/keys/my-site-key.pem"),
  cert: fs.readFileSync("/srv/www/keys/chain.pem")
};

const app = express();

app.use((req, res) => {
  res.writeHead(200);
  res.end("hello world\n");
});

app.listen(8000);

https.createServer(options, app).listen(8080);
```

Ignore the `/srv/www/keys/my-site-key.pem` and and `/srv/www/keys/chain.pem` files for the moment. Those are the SSL certificates we need to generate, which we’ll do a bit later. This is the part that changed with Let’s Encrypt. Previously, we had to generate a private/public key pair, send it to a trusted authority, pay them and probably wait for a bit in order to get an SSL certificate. Nowadays, Let’s Encrypt instantly generates and validates your certificates for free!

## Generating Certificates

### Certbot

The TLS specification demands a certificate, which is signed by a trusted certificate authority (CA). The CA ensures that the certificate holder is really who they claim to be. So basically when you see the green lock icon (or any other greenish sign to the left side of the URL in your browser) it means that the server you’re communicating with is really who it claims to be. If you’re on facebook.com and you see a green lock, it’s almost certain you really are communicating with Facebook and no one else can see your communication—or rather, no one else can read it.

It’s worth noting that this certificate doesn’t necessarily have to be verified by an authority such as Let’s Encrypt. There are other paid services as well. [You can technically sign it yourself](https://stackoverflow.com/q/10175812), but then (as you’re not a trusted CA) the users visiting your site will likely see a large scary warning offering to get them back to safety.

In the following example, we’ll use the *Certbot*, which is used to generate and manage certificates with Let’s Encrypt.

[On the Certbot site](https://certbot.eff.org/) you can find instructions on how to install *Certbot* for almost any OS/server combination. You should choose the options that are applicable to you.

A common combination for deploying Node apps is NGINX on the latest LTS Ubuntu and that’s what I’ll use here.

```
sudo apt-get update
sudo apt-get install software-properties-common
sudo add-apt-repository universe
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update
```

#### Webroot

[Webroot is a Certbot plugin](https://certbot.eff.org/docs/using.html#webroot) that, in addition to the Certbot default functionality (which automatically generates your public/private key pair and generates an SSL certificate for those), also copies the certificates to your webroot folder and verifies your server by placing some verification code into a hidden temporary directory named `.well-known`. In order to skip doing some of these steps manually, we’ll use this plugin. The plugin is installed by default with *Certbot*. In order to generate and verify our certificates, we’ll run the following:

```
certbot certonly --webroot -w /var/www/example/ -d www.example.com -d example.com
```

You may have to run this command as sudo, as it will try to write to `/var/log/letsencrypt`.

You’ll also be asked for your email address. It’s a good idea to put in a real address you use often, as you’ll get a notification if your certificate is about to expire. The trade-off for Let’s Encrypt issuing a free certificate is that it expires every three months. Luckily, renewal is as easy as running one simple command, which we can [assign to a cron job](https://www.howtogeek.com/101288/how-to-schedule-tasks-on-linux-an-introduction-to-crontab-files/) and then not have to worry about expiration. Additionally, it’s a good security practice to renew SSL certificates, as it gives attackers less time to break the encryption. Sometimes developers even set up this cron to run daily, which is completely fine and even recommended.

Keep in mind that you have to run this command on a server to which the domain specified under the `-d` (for domain) flag resolves—that is, your production server. Even if you have the DNS resolution in your local hosts file, this won’t work, as the domain will be verified from outside. So if you’re doing this locally, it will most likely fail, unless you opened up a port from your local machine to the outside world and have it running behind a domain name which resolves to your machine. This is a highly unlikely scenario.

Last but not least, after running this command, the output will contain paths to your private key and certificate files. Copy these values into the previous code snippet—into the `cert` property for certificate, and the `key` property for the key:

```
// ...

const options = {
  key: fs.readFileSync("/var/www/example/sslcert/privkey.pem"),
  cert: fs.readFileSync("/var/www/example/sslcert/fullchain.pem") // these paths might differ for you, make sure to copy from the certbot output
};

// ...
```

## Tighetning It Up

### HTTP Strict Transport Security

Have you ever had a website where you switched from HTTP to HTTPS and there were some residual redirects still redirecting to HTTP? [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) (HSTS) is a web security policy mechanism to mitigate protocol downgrade attacks and cookie hijacking.

HSTS effectively forces the client (browser accessing your server) to direct all traffic through HTTPS—a “secure or not at all” ideology!

Express JS doesn’t allow us to add this header by default, so we’ll use [Helmet](https://www.npmjs.com/package/helmet), a Node module that allows us to do this. Install *Helmet* by running the following:

```
npm install helmet
```

Then we just have to add it as a middleware to our Express server:

```
const https = require("https"),
  fs = require("fs"),
  helmet = require("helmet");

const options = {
  key: fs.readFileSync("/srv/www/keys/my-site-key.pem"),
  cert: fs.readFileSync("/srv/www/keys/chain.pem")
};

const app = express();

app.use(helmet()); // Add Helmet as a middleware

app.use((req, res) => {
  res.writeHead(200);
  res.end("hello world\n");
});

app.listen(8000);

https.createServer(options, app).listen(8080);
```

### Diffie–Hellman Strong(er) Parameters

In order to skip some complicated math, let’s cut to the chase. In very simple terms, there are two different keys used for encryption: the certificate we get from the certificate authority, and one that’s generated by the server for key exchange. The default key for key exchange (also called [Diffie–Hellman key exchange](https://en.wikipedia.org/wiki/Diffie%E2%80%93Hellman_key_exchange), or DH) uses a “smaller” key than the one for the certificate. In order to remedy this, we’ll generate a strong DH key and feed it to our secure server for use.

In order to generate a longer (2048 bit) key, you’ll need `openssl`, which you probably have installed by default. In case you’re unsure, run `openssl -v`. If the command isn’t found, install `openssl` by running `sudo apt install openssl` (or visit their download page [here](https://www.openssl.org/source/)):

```
openssl dhparam -out /var/www/example/sslcert/dh-strong.pem 2048
```

Then copy the path to the file to our configuration:

```
// ...

const options = {
  key: fs.readFileSync("/var/www/example/sslcert/privkey.pem"),
  cert: fs.readFileSync("/var/www/example/sslcert/fullchain.pem"), // these paths might differ for you, make sure to copy from the certbot output
  dhparam: fs.readFileSync("/var/www/example/sslcert/dh-strong.pem")
};

// ...
```

## Conclusion

In 2020 and beyond, there’s no excuse to dismiss HTTPS. The future direction is clearly visible: HTTPS everywhere! In Node.js, we have lots of options for utilizing SSL/TLS. We can publish our websites in HTTPS, we can create requests to encrypted websites, and we can authorize otherwise untrusted certificates.

# Chapter 11: Configuring NGINX and SSL with Node.js

### by Nilson Jacques

[NGINX](https://www.nginx.com/) is a high-performance HTTP server as well as a [reverse proxy](https://medium.com/intrinsic/why-should-i-use-a-reverse-proxy-if-node-js-is-production-ready-5a079408b2ca). Unlike traditional servers, NGINX follows an event-driven, asynchronous architecture. As a result, the memory footprint is low and performance is high. If you’re running a Node.js-based web app, you should seriously consider using NGINX as a reverse proxy.

NGINX can be very efficient in serving static assets. For all other requests, it will talk to your Node.js back end and send the response to the client. In this tutorial, we’ll discuss how to configure NGINX to work with Node.js. We’ll also see how to setup SSL in the NGINX server.

#### Node’s Built-in HTTPS Module

Node also has a built-in HTTPS module and can be configured to read the necessary certificate files without the need for a reverse proxy. You can find out more about this in our article [How to Use SSL/TLS with Node.js](https://www.sitepoint.com/how-to-use-ssltls-with-node-js/).

## Installing NGINX

Assuming you already have Node.js installed on your machine (if not, check [here](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/)), let’s see how to install NGINX.

### Installation on Linux

If you’re running Ubuntu, you can use the following command to install NGINX:

```
sudo apt-get update
sudo apt-get install nginx
```

If you’re running a Linux distro other than Ubuntu, check out [the NGINX installation docs](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/#prebuilt) for more information.

NGINX will start automatically once it’s installed.

### Installation on macOS

If you’re on macOS, you can use [Homebrew](http://brew.sh/) to install NGINX easily. The steps are as following:

*   Homebrew needs the directory `/usr/local` to be `chown`’d to your username. So, run the following command in terminal first:

    ```
     sudo chown -R 'username here' /usr/local
    ```

*   Now the following two commands will install NGINX on your system:

    ```
     brew link pcre
      brew install nginx
    ```

*   Once the installation is complete, you can type the following command to start NGINX:

    ```
     sudo nginx
    ```

*   The NGINX config file can be found here: `/usr/local/etc/nginx/nginx.conf`.

### Installation on Windows

For Windows, head over to the NGINX [downloads](http://nginx.org/en/download.html) page and get the zip. The next step is unzipping the archive and moving to the directory in the command prompt as follows:

```
unzip nginx-1.3.13.zip
cd nginx-1.3.13
start nginx
```

As you can see, the command `start nginx` will start NGINX.

Now that the installation is done, let’s see how you can configure a simple server.

## Setting Up a Node.js Server

First, let’s create a simple Node.js server. We’ll start by initiating a project and installing the [Express package](https://www.npmjs.com/package/express):

```
mkdir node-demo && cd node-demo
npm init -y
npm i express
```

Create a file called `server.js`, with the following contents:

```
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(port, () => console.log(`Example app listening on port ${port}!`))
```

You can start the server by running `node server.js`.

## Configuring NGINX

Now let’s open up the NGINX default site config file:

```
sudo nano /etc/nginx/sites-available/default
```

If you want, you can go directly to the directory and open up the config file with your favorite text editor.

As you scroll down, you’ll find a `server` block. It looks something like this:

```
server {
  listen       80;
  server_name  localhost;

  ....
  more config goes here
}
```

Next, we’ll configure the `server` block to suit our needs. We want to configure NGINX to pass all requests through to our Node.js server. Replace the above `server` block with a new block as shown below:

```
server {
  listen       80;
  server_name  localhost;

  location / {
    proxy_pass http://localhost:3000;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  }
}
```

As you can see, the web server will listen on `http://localhost` port `80`. The `location /` block tells NGINX what to do with any incoming request. We use `proxy_pass` to point to our Node.js application, which is running at `http://localhost:3000` in our case.

At this point, you should save the file and type the following to restart NGINX, depending on your operating system.

**Ubuntu:**

```
sudo service nginx restart
```

Or:

```
sudo /etc/init.d/nginx restart
```

**macOS:**

```
sudo nginx -s stop && sudo nginx
```

**Windows:**

```
nginx -s reload
```

Once this is done, you can go to [http://localhost](http://localhost) to see our proxy in action. Although you’re accessing the NGINX web server, you’ll get the actual response from the Node.js server.

#### Port 80

You’ll need to make sure there isn’t anything else (such as Apache) running on port 80.

## Setting Up SSL

In order to create a secure connection with a user’s browser, we’ll need to obtain a digital certificate. Normally, you get one of these from a certificate authority such as [Let’s Encrypt](https://letsencrypt.org/). If you go the Let’s Encrypt route, be sure to install the certificate using [Certbot](https://certbot.eff.org/instructions), which will take care of reconfiguring NGINX for you.

For local development (and for following along with this tutorial) you can also [create a self-signed certificate](https://www.digitalocean.com/community/tutorials/how-to-create-a-ssl-certificate-on-nginx-for-ubuntu-12-04). The only problem is that browsers will show a warning that the “Certificate is not Trusted” when someone visits your website. But for testing on your local machine that’s perfectly fine.

Once you have a certificate and a private key, you can set up SSL in NGINX. You need to modify our previous server block to the following:

```
server {
  listen       80;
  listen       443 ssl;
  server_name  localhost;

  ssl_certificate  /etc/nginx/ssl/server.crt;
  ssl_certificate_key /etc/nginx/ssl/server.key;

  location / {
    proxy_pass http://localhost:3000;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  }
}
```

That’s it!

Now, if you access [https://localhost](https://localhost), your connection will be secure. The configuration above assumes that the certificate and private key are located at `/etc/nginx/ssl/server.crt` and `/etc/nginx/ssl/server.key` respectively, but you can change these locations if you wish.

## Bonus: Serving Static Assets

An additional benefit of having NGINX set up in front of our Node.js server is that we can easily configure it to serve up any static assets our app requires. This will save the overhead of passing through these requests for Node to handle.

To do this, we need to add a new `location` block to the server configuration:

```
server {
  listen       80;
  server_name  localhost;

  location / {
    ...
  }

  location /public {
    root /usr/local/var/www;
  }
}
```

Inside this `location` block we set the root to `/usr/local/var/www`, but you can choose a different directory if you like. As a result, whenever there’s a request to something like `http://localhost/public/somepath/file.html`, NGINX will serve the file from `/usr/local/var/www/public/somepath/file.html` directly.

## Conclusion

In this brief tutorial, we’ve seen how to use NGINX as a reverse proxy for our Node.js app and configure SSL. By using NGINX to handle the static resources, you can also take some load off your Node application.

# Chapter 12: Using Docker for Node.js Development

### by Craig Buckler

Node.js applications rarely exist in isolation. You could require a database, caching, message queues, reverse proxies, search, email routing, process monitoring, other language runtimes and more! Managing these dependencies on your development PC becomes significantly easier with Docker.

This guide provides an introduction to Docker. It concentrates on Node.js, but the concepts apply to any development languages or frameworks.

## “But it Works on My Machine!”

Imagine you’ve created an amazing application with Node.js and a MongoDB database. It’s so successful, you’ve had to employ another developer to add new features. They clone the repository, run `npm install && npm start` and **BANG**—it fails with an obscure error message.

Despite best intentions, your environments are different:

*   you use a Mac, they’re using Windows
*   you developed using Node.js v12, but they have v10 installed
*   you’re using MongoDB v3.6, they’re on v4.2

You may be able to solve these issues within a few hours, but must keep every dependency in sync forever. Is that practical as your team grows? Is it compatible with your live server?

## Virtual Machines

A virtual machine (VM) is an emulated computer system. Rather than installing an operating system (OS) on hardware, it’s run within a software emulation of server hardware. Cross-platform VM options include [VMware](https://www.vmware.com/) and [VirtualBox](https://www.virtualbox.org/).

You could create a Linux VM with all the application dependencies which can be run on Windows, macOS, or Linux. Every developer and the live server would have the same environment. Unfortunately, VMs quickly become impractical:

*   their disk images are large and difficult to copy
*   an individual VM could be updated automatically or by the developer so it’s out of sync with others
*   a VM requires considerable computing resources: it’s a full OS running within an OS

## Docker Overview

[Docker](https://www.docker.com/) is a platform which allows you to build, share, and run applications in *containers*. Think of a container as an isolated virtual machine with its own operating system, libraries, and the application files. *(In reality, containers are lightweight processes which share resources on the host.)*

Docker benefits include:

*   all developers can use the same Docker images on macOS, Linux, and Windows
*   identical containers can be used in development and production environments
*   installation, configuration, and maintenance of applications is easier
*   developers retain the benefits of local development and can experiment without risk
*   containers can easily be scaled—for example, more Node.js processes added to cope with increased traffic

A commercial enterprise edition of Docker is available. This guide uses the open-source community edition, but the same techniques apply.

## Docker Concepts and Terminology

Docker can be daunting initially, but understanding a few key concepts will aid development.

Docker is a client-server application. The server is responsible for container management and is controlled via a REST API. The command-line interface communicates with the API, so it’s possible to run the server daemon anywhere and connect from another device.

### Images

A Docker image is a snapshot of a file system and all application files. In some cases, you’ll use an image as is from the [Docker Hub](https://hub.docker.com/). It provides a wide range of popular applications including [MySQL](https://hub.docker.com/_/mysql) and [MongoDB](https://hub.docker.com/_/mongo).

Node.js applications will normally use a [base Node.js image](https://hub.docker.com/_/node), which is configured using a Dockerfile that describes all the installation and execution steps. The resulting image configuration can be pushed to the Docker Hub. That may be practical during development or where others want to use your application.

Separate images should be created for each application your project requires. For example, your project could use three containers: a Node.js runtime, a MySQL database, and an Elasticsearch engine. It’s technically possible to install all three applications inside a single image, but there are no practical benefits and management would become more difficult.

### Containers

A container is a running instance of an image. One or more containers can be launched from a single image, then used, and stopped as necessary.

By default, a stopped container remains available and can be restarted. However, during development it’s usually practical to delete a container once it has stopped.

Importantly, *containers do not retain state*. Data saved within a file or database is lost whenever a container restarts. You therefore need volumes …

### Volumes

Docker provides two types of storage to retain container state.

1.  **Volumes**: a Docker-managed file system
2.  **Bind mounts**: a file or directory on the host machine.

Either can be used to mount a directory on the container, such as `/data/db` for MongoDB data storage.

Volumes are the recommended way to persist data. In some cases, they’re the only option. MongoDB doesn’t currently support bind mounts on Windows and macOS hosts.

### Networks

A container can communicate with another using standard protocols and ports within their own isolated network. Specific ports can be exposed to other containers and the host machine as necessary.

For example, you could have a Node.js application running on port 3000 of a `nodejs` container which communicates with port `3306` of a `mysql` container. If both ports are exposed to the host, the application can be launched from `http://localhost:3000/` and MySQL clients can connect to `http://localhost:3306/`.

### Docker Compose

Docker Compose is a tool for managing multiple containers with associated volumes and networks. A single file named `docker-compose.yml` defines the configuration.

### Development and Production Environments

Development environments typically:

*   set environment variables such as `NODE_ENV=development`
*   react to code changes, perhaps autoloading using tools such as [nodemon](https://nodemon.io/)
*   enable debugging messages and protocols
*   expose directories and ports so databases and files can be inspected

A live production server is more restricted and has different scaling requirements, but Docker provides several opportunities:

1.  Docker can launch (and restart) any number of Node.js application containers. There’s no need to use [clustering](https://nodejs.org/dist/latest/docs/api/cluster.html) or processing solutions such as [PM2](https://pm2.keymetrics.io/) and [forever](https://www.npmjs.com/package/forever).
2.  Database containers can be solely used by the application. There are fewer security and maintenance issues than a database shared by multiple applications.
3.  Ports need only be exposed within the container network. Consider an NGINX container used as a reverse proxy to a Node.js container which accesses a MySQL container. Only the NGINX port need be exposed to the host (80 for HTTP or 443 for HTTPS). With two or more networks, it becomes possible to restrict MySQL access to the Node.js container only.
4.  A production-specific Docker Compose configuration can be developed. Alternative container management systems such as [Docker Swarm](https://docs.docker.com/engine/swarm/swarm-tutorial/), [Kubernetes](https://kubernetes.io/), or [AWS Fargate](https://aws.amazon.com/fargate/) can also be adopted.

Deploying containers to production servers has benefits, but it’s not absolutely necessary. Perhaps your host doesn’t support Docker or you prefer cloud-based services to locally installed databases? In that situation, Docker can still be used during development with a configuration which closely matches the production system.

### How to Install Docker

Instructions for installing the latest version of Docker on Linux are available on [Docker Docs](https://docs.docker.com/install/linux/docker-ce/ubuntu/). You can also use official repositories, although these are likely to have older editions. For example, on Ubuntu:

```
sudo apt-get update
sudo apt-get remove docker docker-engine docker.io
sudo apt install docker.io
sudo systemctl start docker
sudo systemctl enable docker
```

Docker Compose is [installed separately](https://docs.docker.com/compose/install/) on Linux:

```
sudo curl -L "https://github.com/docker/compose/releases/download/<VERSION>/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

Here, `<VERSION>` is the [latest release number](https://github.com/docker/compose/releases)—such as `1.25.3`.

Installation will vary across editions of Linux. *Search the web for appropriate instructions.*

[Docker CE Desktop for macOS Sierra 10.12 and above](https://hub.docker.com/editions/community/docker-ce-desktop-mac) and [Docker CE Desktop for Windows 10 Professional](https://hub.docker.com/editions/community/docker-ce-desktop-windows) are available as installable packages which contain both Docker and Docker Compose. You must register at [Docker Hub](https://hub.docker.com) and sign in to download.

Docker on Windows 10 uses the [Hyper-V virtualization platform](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/), which you can enable from **Turn Windows features on or off** in **Programs and Features** from the Control Panel. Docker can also use the [Windows Subsystem for Linux 2](https://docs.microsoft.com/en-us/windows/wsl/wsl2-index) (WSL2—*currently in beta for Windows Insider users*).

To ensure Docker can access the Windows file system, choose **Settings** from the Docker tray icon menu, navigate to the **Shared Drives** pane, and select which drives the server is permitted to use.

#### Windows 10 Home

If you’re running Windows 10 Home, check out our article [How to Install Docker on Windows 10 Home](https://www.sitepoint.com/docker-windows-10-home/).

Check Docker has successfully installed by entering `docker version` at your command prompt. Optionally, try `docker run hello-world` to verify Docker can pull images and start containers as expected.

### Permission Errors

On Linux, if you experience a `permission denied while trying to connect to the Docker daemon` error, you can remedy this as follows:

```
sudo groupadd docker
sudo usermod -aG docker $USER
```

Then reboot your machine.

You can find [more details in this Stack Overflow question](https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue).

## How to Launch a Database Container

Enter the following command in your terminal to launch a MongoDB container:

```
docker run -d --rm --name mongodb -p 27017:27017 --mount "src=mongodata,target=/data/db" mongo:4
```

The first time you run this command, Docker downloads and initializes the latest MongoDB 4 image which can take a few minutes. The [command line switches](https://docs.docker.com/engine/reference/commandline/run/) include:

| switch | description |
| --- | --- |
| `-d` | run a container as a background process |
| `-it` | run in interactive mode; you’ll see an activity log |
| `--rm` | remove the container after it stops |
| `--name` | a name given to the container (a random GUID is used otherwise) |
| `-p` | map a host port to a container port |
| `--mount` | create a persistent Docker-managed volume to retain data |
| `-e` | define one or more environment variables |
| `--env-file` | read environment variables from a file |
| `--entrypoint` | overrides the default starting application |

Any MongoDB client can now connect to `localhost:27017` (no user ID or password is necessary). Alternatively, connect directly to the container shell from another terminal:

```
docker exec -it mongodb sh
```

Start the MongoDB command line:

```
mongo
```

Then run any database commands. For example:

```
use test;
db.apps.insertOne({ name: 'Docker' });
db.apps.find();
```

Type `exit` to quit the MongoDB client, then `exit` again to quit the shell.

List running containers with:

```
docker container ls
```

To stop and remove the MongoDB container, enter:

```
docker container stop mongodb
```

Similarly, you can start a MySQL 8 container using:

```
docker run -d --rm --name mysql -p 3306:3306 --mount "src=mysqldata,target=/var/lib/mysql" -e MYSQL_ROOT_PASSWORD=mysecret mysql:8
```

Once it has launched (which can take several minutes), use any MySQL client to connect to `localhost:3306` with the user ID `root` and password `mysecret`. for example:

```
docker exec -it mysql sh
mysql -u root -pmysecret
```

The MySQL container can be stopped with:

```
docker container stop mysql
```

#### Address Already in Use

If you get an `address already in use` error, the chances are that you already have a MongoDB or MySQL service running on the port in question. Try stopping the service and re-running the `docker` command.

## How to Launch a Node.js Container

Running your Node.js application within a Docker container provides a more consistent environment than your host PC. Presume we want to *Dockerize* a simple Express.js application which shows a message when browsing to `http://localhost:3000/`. The starting files:

**package.json**

```
{
  "name": "docker-test",
  "version": "1.0.0",
  "description": "Docker test",
  "main": "index.js",
  "scripts": {
    "start": "node ./index.js",
    "debug": "nodemon --inspect ./index.js"
  },
  "dependencies": {
    "express": "^4.17.1"
  },
  "devDependencies": {
    "nodemon": "^2.0.2"
  }
}
```

**nodemon.json**

```
{
  "script": "./index.js",
  "ext": "js",
  "ignore": [
    ".git/",
    "node_modules/"
  ],
  "legacyWatch": true,
  "delay": 200,
  "verbose": true
}
```

(Note that `legacyWatch` uses an older file-watching process which is more reliable on most devices.)

**index.js**

```
'use strict';
const
  port = 3000,
  express = require('express'),
  app = express();

app.get('/', (req, res) => {
  res.send('Hello from Docker!');
});

app.listen(port, () =>
  console.log(`server running on port ${port}`)
);
```

An appropriate Node.js image can be selected from the [Docker Hub](https://hub.docker.com/_/node). In general:

*   most images are large and require a 100MB+ download
*   `alpine` images have the smallest 5MB download, but may not provide some OS dependencies your application requires
*   `slim` images are are cut-down versions of the main Linux images, which may be a reasonable pragmatic choice

In this case, we can use `lts-alpine`—the smallest image with the most recent LTS (even-numbered) version of Node.js.

A `Dockerfile` defines the build steps required to create an image for the application. Various [commands can be used](https://docs.docker.com/engine/reference/builder/), including these:

| command | description |
| --- | --- |
| `FROM` | build the image from a [Docker hub](https://hub.docker.com/) starting image |
| `ENV` | set an environment variable |
| `WORKDIR` | set a working directory |
| `USER` | set an active user |
| `RUN` | execute an installation command, such as `npm install` |
| `COPY` | copy files from the host machine |
| `EXPOSE` | expose a port to the host |
| `CMD` | the container launch command |

**Dockerfile**

```
FROM node:lts-alpine

ENV HOME=/home/node/app
ENV NODE_ENV=production

RUN mkdir -p $HOME && chown -R node:node $HOME

WORKDIR $HOME
USER node

COPY --chown=node:node package*.json $HOME/
RUN npm i && npm cache clean --force

COPY --chown=node:node . .

EXPOSE 3000

CMD npm start
```

This example presumes a production environment. However, we’ll override some settings on the Docker command line and in Docker Compose during development.

Also create a `.dockerignore` file to ensure non-essential files are not copied to the image:

**.dockerignore**

```
.git
.gitignore
.config
.npm
.vscode
node_modules
```

To build a new image named `nodetest`, from within the project root, enter:

```
docker image build -t nodetest .
```

The period at the end of the command is essential! Use `-f <file>` if you didn’t name your build file “`Dockerfile`”.

Docker creates a separate (hidden) image at each build step (enter `docker image ls -a` to view them all). This allows changes to be made more efficiently. For example, modifying the `EXPOSE` port is instantaneous because none of the previous build steps need to change. However, using a different `FROM` image would require a complete rebuild.

For this reason, Dockerfile commands should be ordered from least likely to most likely to change. In this case:

1.  The starting image and environment variables are set.
2.  A home directory is created and the `node` user is granted ownership.
3.  The working directory and user is defined.
4.  `package.json` is copied from the host and npm dependencies are installed.
5.  The rest of the application files are copied from the host.
6.  Port 3000 is exposed on the host.
7.  `npm start` is executed.

An interactive container named `nodeapp` can now be started from this image:

```
docker run -it --rm --name nodeapp -p 3000:3000 nodetest
```

Open [http://localhost:3000/](http://localhost:3000/) in a browser to see “Hello from Docker!”

The container runs in production mode. Any changes you make to `index.js` (or another application file) will not take effect until you stop the container, rebuild the image, and launch another container.

To make development more practical, stop the container with `Ctrl` / `Cmd` + `C` and start a new one using:

```
docker run -it --rm --name nodeapp -p 3000:3000 -e NODE_ENV=development -v $PWD:/home/node/app --entrypoint '/bin/sh' nodetest -c 'npm i && npm run debug'
```

#### $PWD and Windows

`$PWD` is a reference to the current folder on Linux and macOS. It’s not available in Windows Powershell or `cmd`. Replace it with the full project path using Linux forward-slash notation—for example, `/c/projects/nodetest`.

This command does the following:

1.  it changes the `NODE_ENV` environment variable to `development`
2.  it mounts the host’s project directory to the application path in the container
3.  it changes the starting command to `/bin/sh` to launch a shell
4.  it passes `-c 'npm i && npm run debug'` to that shell to install dependencies and run the `debug` script (which launches nodemon)

The `index.js` code can now be modified and the web server will automatically restart. There’s no need to rebuild the image or restart the container unless you install further modules (access the shell using `docker exec -it nodeapp sh`).

## Using Docker Compose During Development

Starting Docker containers individually is awkward, especially when the commands are so complex! Fortunately, Docker Compose can manage any number of containers quickly and effectively in a single command.

Presume we want to launch three containers in development mode within a Docker network named `localnet`:

1.  A MySQL database container named `mysql` saves data to a Docker volume named `mysqldata` and exposes port 3306.
2.  The PHP [Adminer database client](https://www.adminer.org/) named `adminer` exposes the web application on port 8080.
3.  The Node.js Express application defined above runs nodemon and exposes the web application on port 3000.

Create a file named `docker-compose.yml` in your project folder with the following content (tabs are critical):

```
version: '3'

services:

  mysql:
    environment:
      - MYSQL_ROOT_PASSWORD=mysecret
    image: mysql:8
    container_name: mysql
    volumes:
      - mysqldata:/var/lib/mysql
    ports:
      - "3306:3306"
    networks:
      - localnet

  adminer:
    image: adminer
    container_name: adminer
    depends_on:
      - mysql
    ports:
      - "8080:8080"
    networks:
      - localnet

  nodejs:
    environment:
      - NODE_ENV=development
    build:
      context: ./
      dockerfile: Dockerfile
    container_name: nodejs
    depends_on:
      - mysql
    command: /bin/sh -c 'npm i && npm run debug'
    volumes:
      - ./:/home/node/app
    ports:
      - "3000:3000"
    networks:
      - localnet

volumes:
  mysqldata:

networks:
  localnet:
```

Docker Compose configurations can use [many commands](https://docs.docker.com/compose/compose-file/), but this example sets similar options to the Docker development CLI commands used above. Notes:

*   The `mysql volumes` setting uses a Docker volume, while `node volumes` mounts the host’s file system (Docker Compose permits relative paths references on any OS).
*   [`depends_on`](https://docs.docker.com/compose/compose-file/#depends_on) defines start-up dependences. In this case, `adminer` and `nodejs` start after `mysql` has launched.

Before going any further, ensure you’ve stopped any running containers. It’s also advisable to [ensure your system is clean](#node11-ch12.xhtml_cleaning-up) by deleting existing images, containers, and networks by running:

```
docker system prune -af
```

All three containers can now be launched by entering:

```
docker-compose up
```

That’s it. The first run will take some time as images download and build, but all messages will be logged to the terminal.

You can now access the Node.js web service at [http://localhost:3000/](http://localhost:3000/). Nodemon will restart the application when `index.js` is modified.

You can use any MySQL client to connect to the database at `localhost:3306`. Alternatively, open Adminer in your browser at [http://localhost:8080/](http://localhost:8080/) and access the database using the credentials:

*   System: **MySQL**
*   Server: **mysql**
*   Username: **root**
*   Password: **mysecret**

Any container shell can be accessed from another terminal using:

```
docker-compose exec <name> sh
```

Here, `<name>` is the container name (`nodejs`, `mysql`, or `adminer`).

When you’re finished, press `Ctrl` / `Cmd` + `C` in the `docker-compose` terminal and all three containers will gracefully shut down and remove themselves. Subsequent runs of `docker-compose up` will be almost instantaneous.

## Using Docker Compose in Production

A similar Docker Compose configuration can be used in production. The main differences:

*   Applications should run in production mode (our `Dockerfile` default).
*   Development applications such as Adminer are not required. *(Admittedly, they can be useful on live servers, but they increase security and human error risks!)*
*   For additional security, ports such as MySQL `3306` need only be exposed within the Docker network rather than on the host. Using stronger passwords or `.env` files may also be beneficial!
*   Container [`restart`](https://docs.docker.com/compose/compose-file/#restart) and similar production options can be added.

Create a new Docker Compose file for production—that is, `docker-compose-production.yml`:

```
version: '3'

services:

  mysql:
    environment:
      - MYSQL_ROOT_PASSWORD=mysecret
    image: mysql:8
    container_name: mysql
    volumes:
      - mysqldata:/var/lib/mysql
    ports:
      - "3306"
    networks:
      - localnet
    restart: on-failure

  nodejs:
    build:
      context: ./
      dockerfile: Dockerfile
    container_name: nodejs
    depends_on:
      - mysql
    ports:
      - "3000:3000"
    restart: on-failure

volumes:
  mysqldata:

networks:
  localnet:
```

Docker containers can now be started as a background service on the live server:

```
 docker-compose -f .\docker-compose-production.yml up -d
```

Ideally, you’d also require a front-end web server such as [NGINX](https://www.nginx.com/) to act as an SSL-enabled reverse proxy to the Node.js application, but that could be installed on the host or as [another container](https://hub.docker.com/_/nginx).

To stop the containers, enter:

```
docker-compose stop
```

## Cleaning Up

Docker can use significant disk space: enter `docker system df` to view usage statistics.

To clean up stopped containers and dangling images, volumes, and networks not currently associated with a container, enter:

```
docker system prune
```

Add `-a` to remove images, or `-af` to also include containers and networks.

All volumes can be removed with `docker volume prune -f`, but remember to back up any data you require before doing so!

## Next Steps

Docker is a complex topic, but this guide covers the essentials for Node.js development. However, while the examples above launch Node.js and database containers, the application does not access or use a database at any point!

That’s the topic of Chapter 5\. You’ll discover:

1.  why databases are necessary for web applications
2.  the differences and benefits offered by SQL and NoSQL databases
3.  how to write a Node.js application using MongoDB, MySQL, and the Sequelize ORM.