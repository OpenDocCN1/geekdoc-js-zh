![](Images/cover00531.jpeg)

JavaScript

Object-Oriented Programming

By Examples

- First Edition -

Neo D. Truman

# Copyright

JavaScript Object-Oriented Programming By Examples

Copyright © 2022 by Neo D. Truman

All rights reserved.

No part of this publication may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, electronic, mechanical, photocopying, recording, scanning, or otherwise, without the Author’s prior consent.

# Table of Contents

[Copyright](#part0001.xhtml__Toc100078102)

[Table of Contents](#part0002.xhtml__Toc100078103)

[Preface](#part0003.xhtml__Toc100078104)

[Book Audience](#part0004.xhtml__Toc100078105)

[How to Contact Us](#part0005.xhtml__Toc100078106)

[Conventions Used in This Book](#part0006.xhtml__Toc100078107)

[Chapter 1 Setting Up a Development Environment](#part0007.xhtml__Toc100078108)

[1.1 Installing a Code Editor](#part0008.xhtml__Toc100078109)

[1.2 Using a Web Browser](#part0009.xhtml__Toc100078110)

[1.2.1 Using Developer Tools of The Browser](#part0009.xhtml__Toc100078111)

[1.2.2 Using Console Tool](#part0010.xhtml__Toc100078112)

[1.2.3 Using Source Tool](#part0011.xhtml__Toc100078113)

[1.3 Preparing a Workspace](#part0012.xhtml__Toc100078114)

[Chapter 2 Object](#part0013.xhtml__Toc100078115)

[2.1 Creating Objects](#part0013.xhtml__Toc100078116)

[2.2 Accessor Properties](#part0014.xhtml__Toc100078117)

[2.3 Global Object](#part0015.xhtml__Toc100078118)

[2.4 Upgrading Object Literal](#part0016.xhtml__Toc100078119)

[2.4.1 Shorthand Properties](#part0016.xhtml__Toc100078120)

[2.4.2 Shorthand Methods](#part0017.xhtml__Toc100078121)

[2.4.3 Computing Property Keys](#part0018.xhtml__Toc100078122)

[2.5 Prototype of Objects](#part0019.xhtml__Toc100078123)

[2.6 Prototype Chain](#part0020.xhtml__Toc100078124)

[Chapter 3 Function](#part0021.xhtml__Toc100078125)

[3.1 Creating a Function](#part0022.xhtml__Toc100078126)

[3.1.1 Function Declaration](#part0022.xhtml__Toc100078127)

[3.1.2 Function Expression](#part0023.xhtml__Toc100078128)

[3.1.3 Using Function Constructor](#part0024.xhtml__Toc100078129)

[3.2 Calling Functions](#part0025.xhtml__Toc100078130)

[3.3 The return Statement](#part0026.xhtml__Toc100078131)

[3.4 Function Parameters](#part0027.xhtml__Toc100078132)

[3.4.1 Default Parameters](#part0028.xhtml__Toc100078133)

[3.4.2 Rest Parameters](#part0029.xhtml__Toc100078134)

[3.5 The arguments Object](#part0030.xhtml__Toc100078135)

[3.6 Recursive Function](#part0031.xhtml__Toc100078136)

[3.7 Arrow Function Expressions](#part0032.xhtml__Toc100078137)

[3.8 Immediately Invoked Function Expressions](#part0033.xhtml__Toc100078138)

[3.9 Function Scope](#part0034.xhtml__Toc100078139)

[3.10 Passing by Value vs. by Reference](#part0035.xhtml__Toc100078140)

[3.11 Function Overloading](#part0036.xhtml__Toc100078141)

[3.12 First-class Function](#part0037.xhtml__Toc100078142)

[3.13 Context Binding](#part0038.xhtml__Toc100078143)

[3.13.1 bind](#part0038.xhtml__Toc100078144)

[3.13.2 call](#part0039.xhtml__Toc100078145)

[3.13.3 apply](#part0040.xhtml__Toc100078146)

[3.14 Closure](#part0041.xhtml__Toc100078147)

[3.14.1 Closure Introduction](#part0041.xhtml__Toc100078148)

[3.14.2 Private Properties and Methods using Closures](#part0042.xhtml__Toc100078149)

[3.15 Callback Function](#part0043.xhtml__Toc100078150)

[3.16 Generator Function](#part0044.xhtml__Toc100078151)

[Chapter 4 this in JavaScript](#part0045.xhtml__Toc100078152)

[4.1 this in Functions](#part0045.xhtml__Toc100078153)

[4.2 this in Object’s Methods](#part0046.xhtml__Toc100078154)

[4.2.1 Implicit Binding](#part0047.xhtml__Toc100078155)

[4.2.2 Implicit Lost Binding](#part0048.xhtml__Toc100078156)

[4.3 globalThis](#part0049.xhtml__Toc100078157)

[Chapter 5 Object-Oriented Programming](#part0050.xhtml__Toc100078158)

[5.1 Basic Concepts in OOP](#part0051.xhtml__Toc100078159)

[5.1.1 Encapsulation](#part0051.xhtml__Toc100078160)

[5.1.2 Class and Instance](#part0052.xhtml__Toc100078161)

[5.1.3 Inheritance](#part0053.xhtml__Toc100078162)

[5.1.4 Polymorphism](#part0054.xhtml__Toc100078163)

[5.1.5 Virtual Method](#part0055.xhtml__Toc100078164)

[5.2 The new Operator](#part0056.xhtml__Toc100078165)

[5.3 The prototype Property of Functions](#part0057.xhtml__Toc100078166)

[5.4 Extend Function Objects](#part0058.xhtml__Toc100078167)

[5.5 Reflect](#part0059.xhtml__Toc100078168)

[5.6 Classes](#part0060.xhtml__Toc100078169)

[5.6.1 Class declarations](#part0060.xhtml__Toc100078170)

[5.6.2 Class expressions](#part0061.xhtml__Toc100078171)

[5.6.3 Constructor](#part0062.xhtml__Toc100078172)

[5.6.4 Static Methods and Properties](#part0063.xhtml__Toc100078173)

[5.6.5 Private Methods and Properties](#part0064.xhtml__Toc100078174)

[5.6.6 Sub Classing with Extends](#part0065.xhtml__Toc100078175)

[5.6.7 ES5 JavaScript OOP for Old Browsers](#part0066.xhtml__Toc100078176)

[About the Author](#part0072.xhtml__Toc100078177)

[Other Books by The Author](#part0073.xhtml__Toc100078178)

[Please leave a Review/Thought on Amazon](#part0074.xhtml__Toc100078179)

# Preface

Object-Oriented Programming (OOP) is a programming method that takes objects as the foundation. This book introduces OOP concepts like encapsulation, classes, and instances, object inheritance, etc., and guides you on how to do OOP in JavaScript.

JavaScript is the world's most used programming language, which is one of the core technologies of the World Wide Web, alongside HTML and CSS. Websites use JavaScript on the client-side for web page behavior and user interaction. All major web browsers have their JavaScript engine to execute the JavaScript code on the web pages.

## Book Audience

The book targets intermediate developers who already know basic JavaScript programming. It starts by introducing all concepts related to OOP. Then, Object-Oriented Programming in JavaScript will be introduced in the last chapter when you knew all the related concepts.

If you want to learn JavaScript from basic to the most difficult topics, please read [another book by the author](https://www.amazon.com/dp/B09VDRLYBT).

## How to Contact Us

My email is [neodtruman@gmail.com](mailto:neodtruman@gmail.com). If you have any questions, please send me an email. I am always happy to hear from people who’ve read my books. I’ll try my best to answer every email I receive. The subject should be “[JavaScript Object-Oriented Programming By Examples] <Your subject here>” so that I could filter and answer your questions quickly.

You can also follow me on the Amazon Author page, [https://www.amazon.com/Neo-D-Truman/e/B09P6LHL2M](https://www.amazon.com/Neo-D-Truman/e/B09P6LHL2M)

## Conventions Used in This Book

The following typographical conventions are used in this book:

Italic

Indicates new terms, URLs, email addresses, filenames, and file extensions.

Bold

Indicates important concepts or UI items such as menu items and buttons to be selected or clicked.

Constant width

Indicates computer code including statements, functions, classes, objects, methods, properties, etc.

Constant width bold

Shows commands or other text that should be typed literally by the user.

Constant width italic

Shows text that should be replaced with user-supplied values or values determined by context.

![Fish with solid fill](Images/image00491.jpeg) This element signifies a general note.

![Rat with solid fill](Images/image00492.jpeg) This element signifies a tip or suggestion.

![Crocodile with solid fill](Images/image00493.jpeg) This element indicates a warning or caution.

# Chapter 1
Setting Up a Development Environment

The first step in setting up your development environment is choosing your code editor. Almost editors have essential features like autocompletion, syntax highlighting, formatting code, and smart refactoring. Using them helps you to prevent potential mistakes. Other features such as line-by-line debugging could be already available in the editor. However, we will use the Developer Tools of web browsers while debugging JavaScript code. When finished setting up the development environment, your coding will be amazingly easy and fast.

![Rat with solid fill](Images/image00494.jpeg) There are several tools you might consider so that you could always choose any of them. No matter what tools you choose, you’ll follow a similar process to learn the lessons.

## 1.1 Installing a Code Editor

In this book, we use Visual Studio Code (shortened to VS Code) as the code editor. You can download this free at [https://code.visualstudio.com/download](https://code.visualstudio.com/download). In Stack Overflow’s survey, VS Code was ranked as the most popular code editor across languages.

At the first-time opening VS Code, you could be asked to select a language to get started; just choose JavaScript for now.

## 1.2 Using a Web Browser

We will use Google Chrome as a tool to run and debug our JavaScript code since it is the most popular browser. Moreover, it also includes amazing Developer Tools that will be described below.

### 1.2.1 Using Developer Tools of The Browser

The Developer Tools are usually presented as a tabbed group of panes at the right or bottom of the web browser window. To open the developer tools in Google Chrome, open the Chrome Menu  in the upper-right-hand corner of the browser window and select More Tools > Developer tools.

You can also use Shift + CTRL + J (on Windows/Linux), or Option + ⌘ + J (on macOS) to open the tools.

![](Images/image00495.jpeg)

The Developer Tools will either open up in a new window or within the Chrome window as below picture.

![](Images/image00496.jpeg)

We can undock it into a separate window or only change the dock side following these steps:

● Click the “Customize and control Dev Tools” button in the upper-right-hand corner.

● Then select the dock side that you want as in the below picture.

![](Images/image00497.jpeg)

### 1.2.2 Using Console Tool

If the Console tool wasn’t selected, you might have to select the Console tab. We can check the values of variables or try JavaScript code directly in the Console tool as below.

![](Images/image00498.jpeg)

The Console panel is the one that shows the messages you output with  console.log() and any unhandled errors.

### 1.2.3 Using Source Tool

You may have to select the Sources tab to open the debugging tool. It supports line-by-line debugging with breakpoints, reviewing the call stack, scope chain, etc. The details will be introduced with code later.

![](Images/image00499.jpeg)

1.3 Preparing a Workspace

Please follow these steps to create your workspace:

● Create the Example folder, such as “D:\Example”

● Open the Visual Studio Code

● In the VS Code, select menu File > Open Folder…

● Select your folder, “D:\Example” in my example

● Hover the mouse on the EXAMPLE folder, some icons will appear as below.

![](Images/image00500.jpeg)

● Click the New File icon.

![](Images/image00501.jpeg)

● Type “index.html” and press Enter

● Then type below HTML code into the editor

<!DOCTYPE  html>

<html>

<body>

 <h2>Testing Page</h2>

 <!-- Your HTML code here -->

 <script  src="app.js"></script>

</body>

</html>

● Select menu File > Save to save the change to the index.html file.

![](Images/image00502.jpeg)

● Hover the mouse on the EXAMPLE folder and click the New File icon.

● Type “app.js” and press Enter.

● Then type the below JavaScript code into the editor.

"use strict";

console.log('This is your first JS code.');

● Select menu File > Save to save the change to the app.js file.

![](Images/image00503.jpeg)

![Rat with solid fill](Images/image00504.jpeg) While learning this book, you will change JavaScript code in the app.js file and HTML code in the index.html file.

Let’s try the code by opening the index.html file in a web browser, such as Google Chrome.

![](Images/image00505.jpeg)

Then, open the Console panel to see the result.

![](Images/image00506.jpeg)

# Chapter 2
Object

In JavaScript, object is the most-used component that could contain many key-value pairs. In an object, a key can have value as a function, called a method of the object.

## 2.1 Creating Objects

We can create an object using the curly brackets ({}) which enclose some key-value pairs in the below syntax.

{

 key1: value1,

    key2: value2,

    …

    keyN: valueN

}

Example:

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman", |
| 5 | getFullname: function() { |
| 6 |  return  this.firstName + " " + this.lastName; |
| 7 |     } |
| 8 | }; |
| 9 | console.log(typeof obj); // object |
| 10 | console.log(obj.getFullname()); // Neo D. Truman |

In the above example, the  firstName property of the  obj object has the value  "Neo" and  getFullname is a method of the object since it’s a function.

There are three ways to get values of the properties:

● Object.PropertyName

console.log(obj.firstName); // "Neo"

● Object[StringOfPropertyName]

console.log(obj["firstName"]); // "Neo"

● Object[StringVariable]

let propertyName = "lastName";

console.log(obj[propertyName]); // "D. Truman"

If there is nothing between the curly brackets, we call it an empty object. We can create an empty object and then add its properties like the below example.

| 1 | "use strict"; |
| 2 | let o1 = {}; |
| 3 | o1.firstName = "Neo"; |

We can also use  new Object() to create an object, but this is not recommended. Because the object literal (as the  obj and  o1 variables) makes your code simpler and easier to maintain.

| 1 | "use strict"; |
| 2 | let o2 = new Object(); |
| 3 | o2.lastName = "D. Truman"; |

## 2.2 Accessor Properties

In JavaScript, an object’s properties can be get-only or set-only as in the below examples.

Getters use the  get keyword as a modifier of its function.

Example 1:

| 1 | "use strict"; |
| 2 | const obj = { |
| 3 | _message: 'Initial message', |
| 4 |  get message() { // this is a getter |
| 5 |  return  this._message; |
| 6 |     }, |
| 7 | setMessage: function(newMessage) { |
| 8 |  this._message = newMessage; |
| 9 |     } |
| 10 | }; |
| 11 | console.log(obj.message); // Initial message |
| 12 | obj.setMessage('Hello'); |
| 13 | console.log(obj.message); // Hello |
| 14 | // Try to set value to the get-only property cause TypeError: |
| 15 | // Cannot set property which has only a getter |
| 16 | obj.message = 'Hi'; // TypeError |

Setters use the  set keyword as a modifier of its function.

Example 2:

| 1 | "use strict"; |
| 2 | const obj = { |
| 3 | _message: 'Initial message', |
| 4 |  set message(newMessage) { |
| 5 |  this._message = newMessage; |
| 6 |     }, |
| 7 | getMessage: function() { |
| 8 |  return  this._message; |
| 9 |     } |
| 10 | }; |
| 11 | console.log(obj.getMessage()); // Initial message |
| 12 | obj.message = 'Hello'; |
| 13 | console.log(obj.getMessage()); // Hello |
| 14 | console.log(obj.message); // undefined |
| 15 | // Try to get value of the set-only property will return undefined |

The  _message property is still public in examples 1 and 2. That means we can access  obj._message.

We can combine getter and setter to add more processing while manipulating the properties of an object.

Example 3: keeps all assignments in an array, called  logs.

| 1 | "use strict"; |
| 2 | const obj = { |
| 3 |     logs: [], |
| 4 |  get message() { |
| 5 |  if (this.logs.length === 0) { |
| 6 |  return  undefined; |
| 7 |         } |
| 8 |  return  this.logs[this.logs.length - 1]; |
| 9 |     }, |
| 10 |  set message(msg) { |
| 11 |  this.logs.push(msg); |
| 12 |     } |
| 13 | }; |
| 14 | console.log(obj.message); // undefined |
| 15 | obj.message = "hi"; |
| 16 | obj.message = "hello"; |
| 17 | console.log(obj.message); // "hello" |
| 18 | console.log(obj.logs); // ["hi", "hello"] |

## 2.3 Global Object

In web browsers, Global Object is the  window object so that any global variables or functions can be accessed as properties of it. Variables and functions which are not in any function are global and can be accessed from any JavaScript code within any file.

Example:

The app.js should look like this:

| 1 | "use strict"; |
| 2 | var aGlobalVar = 'Global Variable'; |
| 3 | function aGlobalFunc() { |
| 4 |     console.log("Message from aGlobalFunc()"); |
| 5 | } |
| 6 |  |
| 7 | let aScriptVar = 'Script Variable'; |
| 8 | let aScriptFunc = function () { |
| 9 |     console.log("Message from aScriptFunc()"); |
| 10 | } |
| 11 |  |
| 12 | console.log("Script variable and function don't belong to window object:"); |
| 13 | console.log(window.aScriptVar); // undefined |
| 14 | console.log(window.aScriptFunc); // undefined |
| 15 | console.log('----------------------'); |

In this example, we create a new JavaScript file, named app2.js. The app2.js should look like this:

| 1 | console.log('Access global variable and function from another file:'); |
| 2 | console.log(window.aGlobalVar); // Global Variable |
| 3 | window.aGlobalFunc(); // Message from aGlobalFunc() |
| 4 | console.log('----------------------'); |
| 5 |  |
| 6 | console.log('Access global variable and function from another file but not use window object:'); |
| 7 | console.log(aGlobalVar); // Global Variable |
| 8 | aGlobalFunc(); // Message from aGlobalFunc() |
| 9 | console.log('----------------------'); |
| 10 |  |
| 11 | console.log("Access script variable and function from another file:"); |
| 12 | console.log(aScriptVar); // Script Variable |
| 13 | aScriptFunc(); // Message from aScriptFunc() |
| 14 | console.log('----------------------'); |

The index.html should look like this:

| 1 | <!DOCTYPE  html> |
| 2 | <html> |
| 3 |  |
| 4 | <body> |
| 5 |  <h2>Testing Page</h2> |
| 6 |  <!-- Your HTML code here --> |
| 7 |  |
| 8 |  <script  src="app.js"></script> |
| 9 |  <script  src="app2.js"></script> |
| 10 | </body> |
| 11 | </html> |

We could add  debugger; at beginning of the file app2.js in order to check the scope chain.

![](Images/image00507.jpeg)

In the above picture, global variables and functions can be located in these two scopes:

● Script scope: variables are declared with the  let keyword and function expressions.

● Global scope: variables declared with the  var keyword and function declarations.

Global Objects in different JavaScript environments are different. For example, the Global Object in NodeJS servers is different from the Global Object in web browsers.

## 2.4 Upgrading Object Literal

### 2.4.1 Shorthand Properties

We can use variables to define an object’s properties. And in case the property name is the same as the name of the variable, we can use the shorthand form as below.

Example:

| 1 | "use strict"; |
| 2 | let firstName = 'Neo'; |
| 3 | let lastName = 'D. Truman'; |
| 4 |  |
| 5 | let user = { |
| 6 |     firstName, |
| 7 |     lastName, |
| 8 | email: "neodtruman@gmail.com" |
| 9 | } |
| 10 | console.log(user); |
|  | // {//     firstName: 'Neo',//     lastName: 'D. Truman',//     email: 'neodtruman@gmail.com'// } |

### 2.4.2 Shorthand Methods

To define the methods of an object quickly, we can use the shorthand methods by omitting “: function”.

Example:

| 1 | "use strict"; |
| 2 | let user = { |
| 3 | name: 'Neo D. Truman', |
| 4 |     logInfo() { |
| 5 |         console.log(this.name); |
| 6 |     } |
| 7 | } |
| 8 | user.logInfo(); // Neo D. Truman |
| 9 | console.log(user); |
|  | // {name: 'Neo D. Truman', logInfo: f} |

### 2.4.3 Computing Property Keys

We can compute the property keys like this example.

| 1 | "use strict"; |
| 2 | let objKey = 'name'; |
| 3 | let country = { |
| 4 | [objKey]: 'Canada', |
| 5 | [objKey + 'Abb']: 'ca' |
| 6 | } |
| 7 | console.log(country); // {name: 'Canada', nameAbb: 'ca'} |

## 2.5 Prototype of Objects

In JavaScript, every object has a private prototype (__proto__) which is also an object.

We use  Object.create() to assign an object to the prototype of another object to inherit the properties and methods of the base object.

Example:

| 1 | "use strict"; |
| 2 | let obj1 = { |
| 3 | firstName: 'Neo', |
| 4 | lastName: 'D. Truman', |
| 5 | logFullname: function() { |
| 6 |         console.log(this.firstName + ' ' + this.lastName); |
| 7 |     } |
| 8 | }; |
| 9 |  |
| 10 | let obj2 = Object.create(obj1); |
| 11 | obj2.firstName = 'John'; |
| 12 | obj2.logFullname(); // John D. Truman |

We can open the Console panel to see the result and check the value of the  obj2 variable by typing “obj2” at the cursor (>), then pressing Enter. Try to expand the object and its prototype ([[Prototype]]) to see more information in this picture.

![](Images/image00508.jpeg)

In the above picture, we can see Prototype of  obj2 is the  obj1 object.

The following describes how  obj2.logFullname(); can print “John D. Truman” to the console panel.

● Since  obj2 doesn’t have the  logFullname() method, the JavaScript engine did search the method in  obj2’s prototype.

● Because the prototype of  obj2 is the  obj1 object, the  logFullname() method was found and invoked.

● In the method,  this was  obj2 so that  this.firstName is “John”.

● As  obj2 doesn’t have the property  lastName, the JavaScript engine again searched the  lastName property in  obj2’s prototype.

● Because the prototype of  obj2 is the  obj1 object, the  lastName property was found (“D. Truman”) and used. As a result, “John D. Truman” was printed on the Console panel.

![Crocodile with solid fill](Images/image00509.jpeg) We could access the prototype of  obj2 using  obj2.__proto__ but this way of coding is not recommended since  Object.__proto__ is deprecated.

## 2.6 Prototype Chain

Since the prototype (*) of an object is also another object, the prototype (*) could have its own prototype. We call that is a prototype chain. At the end of the prototype chain, we will see a  null object. When an object does not find a property or method, it will search for them in its prototype and then in prototype of the prototype until found.

The below example demonstrates a prototype chain.

| 1 | "use strict"; |
| 2 | let obj1 = { |
| 3 | firstName: 'Neo', |
| 4 | lastName: 'D. Truman', |
| 5 | logFullname: function() { |
| 6 |         console.log(this.firstName + ' ' + this.lastName); |
| 7 |     } |
| 8 | }; |
| 9 |  |
| 10 | let obj2 = Object.create(obj1); |
| 11 | obj2.firstName = 'John'; |
| 12 |  |
| 13 | let obj3 = Object.create(obj2); |
| 14 | obj3.age = 39; |
| 15 | obj3.logFullname(); // John D. Truman |

We can open the Console panel to see the result and check the value of the  obj3 variable by typing “obj3” at the cursor (>), then pressing Enter. Try to expand the object and its prototype ([[Prototype]]) to see more information in this picture.

![](Images/image00510.jpeg)

In the above picture, we can see the prototype of  obj3 is the  obj2 object, and the prototype of  obj2 is the  obj1 object.

The following describes how  obj3.logFullname(); can print “John D. Truman” to the console panel.

● Since  obj3 doesn’t have the  logFullname() method, the JavaScript engine did search the method in  obj3’s prototype which is  obj2.

● Since  obj2 doesn’t have the  logFullname() method, the JavaScript engine searched the method in  obj2’s prototype.

● Because the prototype of  obj2 is the  obj1 object, the  logFullname() method was found and invoked.

● In the method,  this was  obj3 but obj3 doesn’t have properties  firstName and  lastName. Therefore, the JavaScript engine again searched the properties in  obj3’s prototype which is  obj2.

● The  firstName property was found in  obj2 so that  this.firstName was resolved to “John”.

● As  obj2 doesn’t have the property  lastName, the JavaScript engine again searched the  lastName property in  obj2’s prototype.

● Because the prototype of  obj2 is the  obj1 object, the  lastName property was found (“D. Truman”) and used. As a result, “John D. Truman” was printed on the console panel.

![Fish with solid fill](Images/image00511.jpeg) Searching through the prototype chain could happen again and again until it reaches  null since  null has no prototype.

# Chapter 3
Function

A function is a set of statements that come together to complete a task. These statements are enclosed in curly braces({}) and executed when the function is invoked.

A function is also an object so that we can add properties to it.

| 1 | "use strict"; |
| 2 | function myFunc() { |
| 3 | } |
| 4 | console.log(Function instanceof  Object); // true |
| 5 | myFunc.version = 1.2; |
| 6 | console.log(myFunc.version); // 1.2 |

## 3.1 Creating a Function

### 3.1.1 Function Declaration

A function declaration or function statement is defined using the  function keyword, followed by a function name.

For example, the following code defines a simple function named  sum:

| 1 | "use strict"; |
| 2 | function sum(x, y) { |
| 3 |  return x + y; |
| 4 | } |
| 5 | console.log(typeof sum); // "function" |
| 6 | console.log(sum(10, 20)); // 30 |

The function  sum takes two parameters, called x and y. The function consists of one statement that says to return the summary of the two parameters. The statement  return specifies the value returned by the function.

### 3.1.2 Function Expression

A function expression is an anonymous function that does not have a name. Therefore, it is often assigned to a variable so that we can call the function using the variable. For example, the function  sum could have been defined as:

| 1 | "use strict"; |
| 2 | let sum = function (x, y) { |
| 3 |  return x + y; |
| 4 | } |
| 5 | console.log(typeof sum); // "function" |
| 6 | console.log(sum(10, 20)); // 30 |

![Crocodile with solid fill](Images/image00512.jpeg) Function expression can have an issue with hoisting as in the below example.

| 1 | "use strict"; |
| 2 | console.log(typeof sum); // ReferenceError: Cannot access 'sum' before initialization |
| 3 | let sum = function (x, y) { |
| 4 |  return x + y; |
| 5 | } |

### 3.1.3 Using Function Constructor

Function constructor can be used to create a function programmatically. It means that parameters and function bodies could be defined at runtime.

The syntax is:

new Function(param1, ..., paramN, functionBody)

when

●     param1, ..., paramN: Names to be used by the function as formal parameters.

●     functionBody: A string containing the JavaScript statements comprising the function definition.

The following code creates a function that takes two parameters and return summary of them.

| 1 | "use strict"; |
| 2 | const sum = new Function('x', 'y', 'return x + y'); |
| 3 | console.log(sum(10, 20)); // 30 |

## 3.2 Calling Functions

A function is invoked by using the brackets  ()with the arguments.

A function declaration (not function expression) can be hoisted (appear below the call in the code), as in this example:

| 1 | "use strict"; |
| 2 | console.log(sum(10, 20)); // 30 |
| 3 | function sum(x, y) { |
| 4 |  return x + y; |
| 5 | } |

In the above example,

●     x and y are parameters of the function;

● while  10 and  20 are arguments used when we call the function.

## 3.3 The return Statement

The  return keyword is used to finish the processing of functions and return something to the caller.

The syntax is:

return [expression];

where the  expression whose value is to be returned. If omitted,  undefined is returned instead.

Example 1:

| 1 | "use strict"; |
| 2 | function test() { |
| 3 |  return 100; |
| 4 | } |
| 5 | let x = test(); |
| 6 | console.log(x); // 100 |

Example 2:

| 1 | "use strict"; |
| 2 | function test() { |
| 3 |  return; |
| 4 |     console.log('Will be ignored'); |
| 5 | } |
| 6 | let x = test(); |
| 7 | console.log(x); // undefined |

Example 3:

| 1 | "use strict"; |
| 2 | function test() { |
| 3 | } |
| 4 | let x = test(); |
| 5 | console.log(x); // undefined |

## 3.4 Function Parameters

JavaScript doesn’t require the number of arguments must be equal to the number of function parameters. For example, we have a function having two parameters like this example.

| 1 | "use strict"; |
| 2 | function sum(x, y) { |
| 3 |  return x + y; |
| 4 | } |

And we can invoke the above function with different number of arguments without any errors.

● One argument: lacking input will be  undefined

console.log(sum(10)); // NaN (since y is undefined)

● Two arguments

console.log(sum(10, 20)); // 30

● Three arguments: redundant input will be ignored

console.log(sum(10, 20, 30)); // 30

### 3.4.1 Default Parameters

Default function parameters are values used when the number of arguments is less than the number of parameters.

For example, the  sum function has two parameters but when invoking it, we input only one argument. In that case, the default parameter will be used.

| 1 | "use strict"; |
| 2 | function sum(x, y = 0) { |
| 3 |  return x + y; |
| 4 | } |
| 5 | console.log(sum(10)); // 10 (since y = 0) |

### 3.4.2 Rest Parameters

The rest parameter syntax helps us collect inputs into an array.

| 1 | "use strict"; |
| 2 | function sum(...numbers) { |
| 3 | console.log(numbers instanceof  Array); // true |
| 4 |  |
| 5 |  let result = 0; |
| 6 |  for (let i = 0; i < numbers.length; i++) { |
| 7 |         result += numbers[i]; |
| 8 |     } |
| 9 |  return result; |
| 10 | } |
| 11 | console.log(sum(10, 20, 30)); // 60 |
| 12 | console.log(sum(10, 20, 30, 40)); // 100 |

And this is an example of using rest parameters in combination with ordinary parameters.

| 1 | "use strict"; |
| 2 | function multiply(multiplier, ...numbers) { |
| 3 |  let result = []; |
| 4 |  for (let i = 0; i < numbers.length; i++) { |
| 5 |         result.push(numbers[i] * multiplier); |
| 6 |     } |
| 7 |  return result; |
| 8 | } |
| 9 | let arr = multiply(2, 10, 20, 30); |
| 10 | console.log(arr); // [20, 40, 60] |

## 3.5 The arguments Object

The  arguments object of a function is a special object that contains all arguments which were inputted by users.

Example:

| 1 | "use strict"; |
| 2 | function sum() { |
| 3 |  let total = 0; |
| 4 |  for (let n of  arguments) { |
| 5 |         total += n; |
| 6 |     } |
| 7 |  return total; |
| 8 | } |
| 9 | console.log(sum(1, 2, 3, 4, 5)); // 15 |

## 3.6 Recursive Function

A recursive function calls itself in its function body.

For example, consider the following function which will calculate a summary of integers from  start number to  end number. To focus on the concept, we don’t put the validation code of the parameters.

| 1 | "use strict"; |
| 2 | function sum(start, end) { |
| 3 |  let result = 0; |
| 4 |  for (let i = start; i <= end; i++) { |
| 5 |         result += i; |
| 6 |     } |
| 7 |  return result; |
| 8 | } |
| 9 | console.log(sum(2, 6)); // 2 + 3 + 4 + 5 + 6 = 20 |

We can write the above example in another way as a recursive function.

| 1 | "use strict"; |
| 2 | function sum(start, end) { |
| 3 |  return start === end ? end : start + sum(start + 1, end); |
| 4 | } |
| 5 | console.log(sum(2, 6)); |
|  | // = 2 + sum(3, 6)// = 2 + 3 + sum(4, 6)// = 2 + 3 + 4 + sum(5, 6)// = 2 + 3 + 4 + 5 + sum(6, 6)// = 2 + 3 + 4 + 5 + 6 |

![Crocodile with solid fill](Images/image00513.jpeg) Recursive functions push return addresses onto the Call Stack making them run slower than normal functions. Therefore, we should avoid using recursive functions if we can.

## 3.7 Arrow Function Expressions

An arrow function expression is anonymous with some limitations as below.

● Does not have its bindings to  this or  super, and should not be used as a method of objects.

● Not suitable for the  call,  apply and  bind methods, which generally rely on establishing a scope.

● Cannot be used as constructors.

● Cannot use  yield, within its body.

The syntax of arrow function expression:

● One parameter. With simple expression return is implicit:

param => expression

● Multiple parameters require parentheses. With simple expression return is implicit:

(param1, ..., paramN) => expression

● Multiple statements require curly braces:

param => {

    expressions

}

● Multiple parameters require parentheses and multiple statements require curly braces:

(param1, ..., paramN) => {

    expressions

}

Example 1:

| 1 | "use strict"; |
| 2 | let sayHi = name  => console.log("Hello " + name); |
| 3 | sayHi('Neo'); // "Hello Neo" |

Example 2:

| 1 | "use strict"; |
| 2 | let sayHi = (firstName, lastName) => console.log(`Hello ${firstName}  ${lastName}`); |
| 3 | sayHi('Neo', 'D. Truman'); // "Hello Neo D. Truman" |

Example 3:

| 1 | "use strict"; |
| 2 | let sayHi = name  => { |
| 3 |  let upperCaseName = name.toUpperCase(); |
| 4 |     console.log("Hello " + upperCaseName); |
| 5 | } |
| 6 | sayHi('Neo'); // "Hello NEO" |

Example 4:

| 1 | "use strict"; |
| 2 | let sayHi = (firstName, lastName) => { |
| 3 |  let upperCaseFirstname = firstName.toUpperCase(); |
| 4 |  let upperCaseLastname = lastName.toUpperCase(); |
| 5 |     console.log(`Hello ${upperCaseFirstname}  ${upperCaseLastname}`); |
| 6 | } |
| 7 | sayHi('Neo', 'D. Truman'); // "Hello NEO D. TRUMAN" |

## 3.8 Immediately Invoked Function Expressions

An IIFE (Immediately Invoked Function Expression) is a function that is called immediately right after its definition code. One purpose of using IIFE is to avoid polluting the global namespace.

The syntax is as below.

(function () {

 // some code here

})(); // parentheses in this line does invoking the function

Example:

| 1 | "use strict"; |
| 2 | (() => { |
| 3 |  let someVariable = 10; |
| 4 |     console.log(someVariable); |
| 5 |  // some initiation code using above variable(s) |
| 6 | })(); |
| 7 | // someVariable will be discarded after the function is executed. |

## 3.9 Function Scope

Variables defined inside a function are only available inside the function or its child functions via the closure.

However, a function can access all variables and functions defined inside the scope in which it is defined.

● In other words, a function defined in the global scope can access all variables defined in the global scope.

| 1 | "use strict"; |
| 2 | // These variables are defined in the global scope |
| 3 | let num1 = 10, |
| 4 |     num2 = 20; |
| 5 | // This function is also defined in the global scope |
| 6 | function sum() { |
| 7 |  return num1 + num2; |
| 8 | } |
| 9 | console.log(sum()); // 30 |

● A function defined inside another function can also access to variables defining in its parent function.

| 1 | "use strict"; |
| 2 | // These variables are defined in the global scope |
| 3 | let num1 = 10, |
| 4 |     num2 = 20; |
| 5 |  |
| 6 | // A nested function example |
| 7 | function test() { |
| 8 |  let x = 1, |
| 9 |         y = 2; |
| 10 |  |
| 11 |  function add() { |
| 12 |  return num1 + num2 + x + y; |
| 13 |     } |
| 14 | console.log(add()); // 33 |
| 15 | } |
| 16 | test(); |

![Rat with solid fill](Images/image00514.jpeg) The above example is also an example of closure which will be introduced soon.

## 3.10 Passing by Value vs. by Reference

Parameters, which are not objects, are passed to functions by value — so if the code within the body of a function assigns new values to parameters that were passed to the function, the change is not reflected globally or in the code called that function.

| 1 | "use strict"; |
| 2 | let x = 10; |
| 3 | function test(param) { |
| 4 |     param = 100; |
| 5 | } |
| 6 | test(x); |
| 7 | console.log(x); // 10 |

When you pass an object as a parameter, if the function changes the object's properties, that change is visible outside the function, as shown in the following example. We say that the param was passed by reference.

| 1 | "use strict"; |
| 2 | let o = { info: 10 }; |
| 3 | function testObject(obj) { |
| 4 |     obj.info = 100; |
| 5 | } |
| 6 | testObject(o); |
| 7 | console.log(o); // {info: 100} |
| 8 |  |
| 9 | let a = [1, 2, 3]; |
| 10 | function testArray(arr) { |
| 11 |     arr[0] = 10; |
| 12 | } |
| 13 | testArray(a); |
| 14 | console.log(a); // [10, 2, 3] |

## 3.11 Function Overloading

If two or more functions have the same name, the latest function definition will override the others.

Example 1:

| 1 | "use strict"; |
| 2 | function sum(x, y) { |
| 3 |  return x + y; |
| 4 | } |
| 5 | function sum(x, y, z) { |
| 6 |  return x + y + z; |
| 7 | } |
| 8 | console.log(sum(1, 2)); // NaN since z is undefined |
| 9 | console.log(sum(1, 2, 3)); // 6 |

Example 2:

| 1 | "use strict"; |
| 2 | function sum(x, y, z) { |
| 3 |  return x + y + z; |
| 4 | } |
| 5 | function sum(x, y) { |
| 6 |  return x + y; |
| 7 | } |
| 8 | console.log(sum(1, 2)); // 3 |
| 9 | console.log(sum(1, 2, 3)); // 3 since the 3rd argument was ignored |

## 3.12 First-class Function

First-class functions are functions that are treated as variables. For example,

● a function can be assigned as a value to a variable

| 1 | "use strict"; |
| 2 | const sayHello = function () { |
| 3 |     console.log("Hello!"); |
| 4 | } |
| 5 | sayHello(); // Hello! |

● a function can be passed as an argument to other functions

| 1 | "use strict"; |
| 2 | function sayHello() { |
| 3 |  return  "Hello "; |
| 4 | } |
| 5 | function greeting(helloMessage, name) { |
| 6 |     console.log(helloMessage() + name); |
| 7 | } |
| 8 | // Pass sayHello as an argument to greeting function |
| 9 | greeting(sayHello, "Neo"); // Hello Neo |

● a function can be returned by another function

| 1 | "use strict"; |
| 2 | function sayHello() { |
| 3 |  return  function () { |
| 4 |         console.log("Hello!"); |
| 5 |     } |
| 6 | } |
| 7 | const myFunc = sayHello(); |
| 8 | myFunc(); // Hello! |

## 3.13 Context Binding

### 3.13.1 bind

The Function.prototype.bind() method helps us change the context of the  this keyword.

The syntax is:

bind(thisArg, arg1, ... , argN)

where

●     thisArg is the object that the  this keyword will point to

●     arg1, arg2, ...argN (optional) are arguments of the function.

Example 1:

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | }; |
| 6 |  |
| 7 | function logInfo() { |
| 8 |     console.log(this.firstName + " " + this.lastName); |
| 9 | } |
| 10 | let logInformation = logInfo.bind(obj); |
| 11 | logInformation(); // Neo D. Truman |

Example 2: input arguments into  bind()

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | }; |
| 6 |  |
| 7 | function logInfo(email) { |
| 8 |     console.log(this.firstName + " " + this.lastName); |
| 9 |     console.log(email); |
| 10 | } |
| 11 | let logInformation = logInfo.bind(obj, "neodtruman@gmail.com"); |
| 12 | logInformation(); |
| 13 | // Neo D. Truman |
| 14 | // neodtruman@gmail.com |

Example 3: does not input arguments into  bind()

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | }; |
| 6 |  |
| 7 | function logInfo(email) { |
| 8 |     console.log(this.firstName + " " + this.lastName); |
| 9 |     console.log(email); |
| 10 | } |
| 11 | let logInformation = logInfo.bind(obj); |
| 12 | logInformation("neodtruman@gmail.com"); |
| 13 | // Neo D. Truman |
| 14 | // neodtruman@gmail.com |

### 3.13.2 call

The  Function.prototype.call() method works in the same way as  bind() however  call() will invoke the function (as its name, “call”) but  bind() does not.

The syntax is:

call(thisArg, arg1, ... , argN)

where

●     thisArg is the object that the  this keyword will point to

●     arg1, arg2, ...argN (optional) are arguments of the function.

Example 1:

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | }; |
| 6 |  |
| 7 | function logInfo() { |
| 8 |     console.log(this.firstName + " " + this.lastName); |
| 9 | } |
| 10 | logInfo.call(obj); // Neo D. Truman |

Example 2:

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | }; |
| 6 |  |
| 7 | function logInfo(email) { |
| 8 |     console.log(this.firstName + " " + this.lastName); |
| 9 |     console.log(email); |
| 10 | } |
| 11 | logInfo.call(obj, "neodtruman@gmail.com"); |
| 12 | // Neo D. Truman |
| 13 | // neodtruman@gmail.com |

call() provides a new value of  this to the function/method. With  call(), you can write a method once and then inherit it in another object without rewriting the method for the new object.

| 1 | "use strict"; |
| 2 | let obj1 = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman", |
| 5 | getFullname: function () { |
| 6 |  return  this.firstName + " " + this.lastName; |
| 7 |     } |
| 8 | }; |
| 9 | let obj2 = { |
| 10 | firstName: "John", |
| 11 | lastName: "Conner", |
| 12 | } |
| 13 | let fullname = obj1.getFullname.call(obj2); |
| 14 | console.log(fullname); // John Conner |

We can also use  call() to chain constructors for an object like the below example.

| 1 | "use strict"; |
| 2 | function Thing(name, price) { |
| 3 |  this.name = name; |
| 4 |  this.price = price; |
| 5 | } |
| 6 |  |
| 7 | function SchoolThing(name, price) { |
| 8 |     Thing.call(this, name, price); |
| 9 |  this.category = 'School Thing'; |
| 10 | } |
| 11 |  |
| 12 | const book = new SchoolThing('Student Book', 6); |
| 13 | console.log(book); |
| 14 | // SchoolThing {name: 'Student Book', price: 6, category: 'School Thing'} |

### 3.13.3 apply

The  Function.prototype.apply() method works in the same way as  call() however  apply() will receive an array of arguments of the function. Accepting an array of arguments helps us generate the arguments at runtime and “send” to the function.

The syntax is:

apply(thisArg, argsArray)

where

●     thisArg is the object that the  this keyword will point to

●     argsArray (optional) is the array of arguments of the function.

Example:

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | }; |
| 6 |  |
| 7 | function logInfo(email) { |
| 8 |     console.log(this.firstName + " " + this.lastName); |
| 9 |     console.log(email); |
| 10 | } |
| 11 | // We can get email from user and push it into the array of arguments |
| 12 | let args = ["neodtruman@gmail.com"]; |
| 13 | logInfo.apply(obj, args); |
| 14 | // Neo D. Truman |
| 15 | // neodtruman@gmail.com |

## 3.14 Closure

### 3.14.1 Closure Introduction

A closure gives you access to an outer function's scope from an inner function. In JavaScript, closure is created every time a function is created inside another function and the function does use its parent’s variables.

| 1 | "use strict"; |
| 2 |  |
| 3 | function sayHi(firstName) { |
| 4 |  let lastName = 'D. Truman'; |
| 5 |  return  function doLog(message) { |
| 6 |  debugger; |
| 7 |         console.log( |
| 8 |  `Hello ${firstName}  ${lastName}. ${message}` |
| 9 |         ); |
| 10 |     } |
| 11 | } |
| 12 |  |
| 13 | let greetingFunc = sayHi('Neo'); |
| 14 | greetingFunc('How are you?'); |
| 15 | // Hello Neo D. Truman. How are you? |

When we run the above code, the debugger of the browser will stop at the  debugger breakpoint (line 6) as in the below picture.

![](Images/image00515.jpeg)

We can see in the above picture, the  doLog() function can access to these variables:

● Local variables

message: parameter of the  doLog() function

● Closure variables from the  sayHi() function

firstName: parameter of the  sayHi() function

lastName: local variable of the  sayHi() function

The reason is that nested functions in JavaScript could form closures. A closure is actually a function scope that consists of all local variables of the function so that the inner function could refer to them. In this case,  greetingFunc is a reference to the instance of the function  doLog() that is created when  sayHi() is run. The instance of  doLog() having references (fisrtName and  lastName) to its parent function. For this reason, the  fisrtName and  lastName variables are available in the  Closure (sayHi). As a result, when  greetingFunc is invoked,  "Hello Neo D. Truman. How are you?" is printed to the console panel.

![Crocodile with solid fill](Images/image00516.jpeg) The closure will negatively affect script performance both in terms of processing speed and memory consumption. Therefore, we should avoid creating nested functions if we don’t need them.

The below example shows that there are nested functions but there is no closure since the inner function doesn’t refer to its parent’s variables.

| 1 | "use strict"; |
| 2 |  |
| 3 | function sayHi(firstName) { |
| 4 |  let lastName = 'D. Truman'; |
| 5 |  return  function doLog(message) { |
| 6 |  debugger; |
| 7 |  console.log(message); |
| 8 |     } |
| 9 | } |
| 10 |  |
| 11 | let greetingFunc = sayHi('Neo'); |
| 12 | greetingFunc('How are you?'); |

When we run the above code, the debugger of the browser will stop at the  debugger breakpoint (line 6) as below picture.

![](Images/image00517.jpeg)

We can see in the above picture, that the  doLog() function didn’t access any variables of the  sayHi() function. Therefore, in the Scope Chain, there is no Closure (sayHi) as in the previous example.

### 3.14.2 Private Properties and Methods using Closures

We can emulate private properties and methods of objects using closures since the object can access variables and functions in its closure but does not own them.

The following code illustrates how to use closures to define private properties and methods of an object.

| 1 | "use strict"; |
| 2 | function makeUserObject() { |
| 3 |  let name = 'Neo'; |
| 4 |  function allCap(str) { |
| 5 |  return str.toUpperCase(); |
| 6 |     } |
| 7 |  |
| 8 |  return { |
| 9 | getUpperCaseName: function () { |
| 10 |  debugger; |
| 11 |  return allCap(name); |
| 12 |         }, |
| 13 | getName: function () { |
| 14 |  return name; |
| 15 |         }, |
| 16 | setName: function (newName) { |
| 17 |             name = newName; |
| 18 |         } |
| 19 |     } |
| 20 | } |
| 21 | let u = makeUserObject(); |
| 22 | console.log(u); |
| 23 |  |
| 24 | console.log(u.name); // undefined |
| 25 | console.log(u.allCap); // undefined |
| 26 |  |
| 27 | console.log(u.getUpperCaseName()); // 'NEO' |
| 28 |  |
| 29 | u.setName('John'); |
| 30 | console.log(u.getName()); // 'John' |

When we run the above code, the debugger of the browser will stop at the  debugger breakpoint (line 10) as in the below picture.

![](Images/image00518.jpeg)

The  getUpperCaseName() function can access variable  name and invoke function  allCap() of the Closure. However, the u variable (user instance) cannot access the  name variable and the  allCap() function. This behavior emulates the private properties and methods of the object.

## 3.15 Callback Function

A callback function is a function treated as a parameter of another function so that the parent function will invoke it later.

Example:

| 1 | "use strict"; |
| 2 | function doLog(info) { |
| 3 |     console.log(info); |
| 4 | } |
| 5 | function doAlert(info) { |
| 6 |     alert(info); |
| 7 | } |
| 8 |  |
| 9 | function processName(callback) { |
| 10 |  let name = 'Neo'; |
| 11 |     callback(name); |
| 12 | } |
| 13 | processName(doLog); |
| 14 | processName(doAlert); |

## 3.16 Generator Function

The  function* is exactly a generator that returns different values based on the  yield expressions inside the function body or the yield*, to another generator function.

The  next() method of generators returns an object with  value and  done properties.

Example 1:

| 1 | "use strict"; |
| 2 | function* generator(x) { |
| 3 |  yield x; |
| 4 |  yield x * 2; |
| 5 |  yield x * 5; |
| 6 | } |
| 7 |  |
| 8 | const gen = generator(10); |
| 9 |  |
| 10 | console.log(gen.next()); // {value: 10, done: false} |
| 11 | console.log(gen.next()); // {value: 20, done: false} |
| 12 | console.log(gen.next()); // {value: 50, done: false} |
| 13 | console.log(gen.next()); // {value: undefined, done: true} |

Example 2:

| 1 | "use strict"; |
| 2 | function* anotherGenerator(y) { |
| 3 |  yield y * 3; |
| 4 |  yield y * 4; |
| 5 | } |
| 6 |  |
| 7 | function* generator(x) { |
| 8 |  yield x; |
| 9 |  yield x * 2; |
| 10 |  yield* anotherGenerator(x); |
| 11 |  yield x * 5; |
| 12 | } |
| 13 |  |
| 14 | const gen = generator(10); |
| 15 |  |
| 16 | console.log(gen.next()); // {value: 10, done: false} |
| 17 | console.log(gen.next()); // {value: 20, done: false} |
| 18 | console.log(gen.next()); // {value: 30, done: false} |
| 19 | console.log(gen.next()); // {value: 40, done: false} |
| 20 | console.log(gen.next()); // {value: 50, done: false} |
| 21 | console.log(gen.next()); // {value: undefined, done: true} |

A  return statement in a generator will make the generator done its job (i.e., the  done property of the object returned by it will be set to  true). The returned value will be set as the value property of the object returned by the generator.

Example 3:

| 1 | "use strict"; |
| 2 | function* generator(x) { |
| 3 |  yield x; |
| 4 |  return x * 2; |
| 5 |  yield x * 5; // unreachable |
| 6 | } |
| 7 |  |
| 8 | const gen = generator(10); |
| 9 |  |
| 10 | console.log(gen.next()); // {value: 10, done: false} |
| 11 | console.log(gen.next()); // {value: 20, done: true} |
| 12 | console.log(gen.next()); // {value: undefined, done: true} |

Much like a  return statement, an error thrown inside the generator will make the generator finished — unless caught within the generator's body. When a generator is finished, subsequent  next() calls will not execute any of that generator's code, they will just return an object of this form:  {value: undefined, done: true}.

Example 4:

| 1 | "use strict"; |
| 2 | function* generator(x) { |
| 3 |  yield x; |
| 4 |  throw  'Error here'; |
| 5 |  yield x * 5; // unreachable |
| 6 | } |
| 7 |  |
| 8 | const gen = generator(10); |
| 9 |  |
| 10 | console.log(gen.next()); // {value: 10, done: false} |
| 11 | try { |
| 12 |  console.log(gen.next()); |
| 13 | } catch (error) { |
| 14 | console.log(error); // Error here |
| 15 | } |
| 16 | console.log(gen.next());// {value: undefined, done: true} |

Provide a parameter to the  next() method to send a value to the generator. The syntax is:

next(value)

where

*   variable = yield expression, the value passed to the  next() function will be assigned to  variable.

Example:

| 1 | "use strict"; |
| 2 | function* idGenerator() { |
| 3 |  let counter = 0; |
| 4 |  while (true) { |
| 5 |  let seeker = yield ++counter; |
| 6 |  if (seeker) { |
| 7 |             counter += seeker; |
| 8 |         } |
| 9 |     } |
| 10 | } |
| 11 |  |
| 12 | const generateId = idGenerator(); |
| 13 | console.log(generateId.next().value); // 1 |
| 14 | console.log(generateId.next().value); // 2 |
| 15 | console.log(generateId.next().value); // 3 |
| 16 | console.log(generateId.next(2).value); // 6 (skip two ids) |
| 17 | console.log(generateId.next().value); // 7 |
| 18 | console.log(generateId.next(-3).value); // 5 (rollback three ids) |
| 19 | console.log(generateId.next().value); // 6 |

# Chapter 4
this in JavaScript

## 4.1 this in Functions

In non-strict mode,  this in functions (all kinds of functions) is the Window object when working on a Web Browser, as the below example.

| 1 | // function declaration |
| 2 | function testFunc1() { |
| 3 |     console.log(this); // Window object |
| 4 | } |
| 5 | testFunc1(); |
| 6 |  |
| 7 | // function expression |
| 8 | let testFunc2 = function () { |
| 9 |     console.log(this); // Window object |
| 10 | } |
| 11 | testFunc2(); |
| 12 |  |
| 13 | // nested functions |
| 14 | function test3() { |
| 15 |  // function declaration |
| 16 |  function testFunc3() { |
| 17 |         console.log(this); // Window object |
| 18 |     } |
| 19 |     testFunc3(); |
| 20 | } |
| 21 | test3(); |
| 22 |  |
| 23 | function test4() { |
| 24 |     // arrow function expression |
| 25 |  let testFunc4 = () => { |
| 26 |         console.log(this); // Window objects |
| 27 |     } |
| 28 |     testFunc4(); |
| 29 | } |
| 30 | test4(); |

this in arrow function expressions, which is not in another function, is always (in both strict mode and non-strict mode) the Window object when working on a Web Browser.

| 1 | "use strict"; |
| 2 | // arrow function expression |
| 3 | let testFunc5 = () => { |
| 4 |     console.log(this); // Window object |
| 5 | } |
| 6 | testFunc5(); |

In strict mode,  this in functions (except the arrow functions) is  undefined in as the below example.

| 1 | "use strict"; |
| 2 | // function declaration |
| 3 | function testFunc1() { |
| 4 |     console.log(this); // undefined |
| 5 | } |
| 6 | testFunc1(); |
| 7 |  |
| 8 | // function expression |
| 9 | let testFunc2 = function () { |
| 10 |     console.log(this); // undefined |
| 11 | } |
| 12 | testFunc2(); |
| 13 |  |
| 14 | // nested functions |
| 15 | function test3() { |
| 16 |     // function declaration |
| 17 |  function testFunc3() { |
| 18 |         console.log(this); // undefined |
| 19 |     } |
| 20 |     testFunc3(); |
| 21 | } |
| 22 | test3(); |
| 23 |  |
| 24 | function test4() { |
| 25 |  // arrow function expression |
| 26 |  let testFunc4 = () => { |
| 27 |         console.log(this); // undefined |
| 28 |     } |
| 29 |     testFunc4(); |
| 30 | } |
| 31 | test4(); |

## 4.2 this in Object’s Methods

Since object’s methods are also functions, the  this keyword in the methods behaves the same as in functions (described in the previous section) except for methods that are defined using function expressions.

this in methods that are defined using function expressions is always the object as in the below examples.

Example 1:

| 1 | "use strict"; |
| 2 | let user = { |
| 3 | name: 'Neo', |
| 4 | logInfo: function () { // function expression |
| 5 |         console.log(this); |
| 6 |     }, |
| 7 | showInfo: () => { // arrow function |
| 8 |         console.log(this); |
| 9 |     } |
| 10 | } |
| 11 | user.logInfo(); // {name: 'Neo', logInfo: f, showInfo: f} |
| 12 | user.showInfo(); // Window object |

Example 2:

| 1 | "use strict"; |
| 2 | function testUser() { |
| 3 |  let user = { |
| 4 | name: 'Neo', |
| 5 | logInfo: function () { // function expression |
| 6 |             console.log(this); |
| 7 |         }, |
| 8 | showInfo: () => { // arrow function |
| 9 |             console.log(this); |
| 10 |         } |
| 11 |     } |
| 12 | user.logInfo(); // {name: 'Neo', logInfo: f, showInfo: f} |
| 13 | user.showInfo(); // undefined     |
| 14 | } |
| 15 | testUser(); |

Example 3:  this in nested function will be  undefined

| 1 | "use strict"; |
| 2 | let user = { |
| 3 | firstName: 'Neo', |
| 4 | lastName: 'D. Truman', |
| 5 | showFullname: function () { |
| 6 |         console.log(this.firstName + ' ' + this.lastName); |
| 7 |  function sayHi() { |
| 8 |             console.log(this); // undefined |
| 9 |             console.log('Hi ' + this.firstName + ' ' + this.lastName); // TypeError |
| 10 |         } |
| 11 |         sayHi(); |
| 12 |     } |
| 13 | } |
| 14 | user.showFullname(); |

Example 4: a solution for example 3 is saving the pointer to object at outer function and use it in the inner function (a closure)

| 1 | "use strict"; |
| 2 | let user = { |
| 3 | firstName: 'Neo', |
| 4 | lastName: 'D. Truman', |
| 5 | showFullname: function () { |
| 6 |         console.log(this.firstName + ' ' + this.lastName); |
| 7 |  let self = this; |
| 8 |  function sayHi() { |
| 9 |             console.log(self); |
| 10 |  // self is {firstName: 'Neo', lastName: 'D. Truman', showFullname: f} |
| 11 |             console.log('Hi ' + self.firstName + ' ' + self.lastName); |
| 12 |  // Hi Neo D. Truman |
| 13 |         } |
| 14 |         sayHi(); |
| 15 |     } |
| 16 | } |
| 17 | user.showFullname(); |

We should not use arrow functions in these cases:

● Case #1: Define methods in object or class. Examples areas above.

● Case #2: Define callback events of DOM’s elements.

● Case #3: Define methods in the object’s prototype.

since  this might refer to the  Window object or could be  undefined as above examples.

Example for case #2:

HTML code (added to index.html):

<button id="btn-test">Test</button>

JavaScript code:

| 1 | "use strict"; |
| 2 | let btnTest = document.getElementById('btn-test'); |
| 3 | // on clicked |
| 4 | btnTest.addEventListener('click', () => { |
| 5 |  // this is not the btnTest button as expected |
| 6 |     console.log(this); // Window object |
| 7 | }); |
| 8 | // on double-clicked |
| 9 | btnTest.addEventListener('dblclick', function () { |
| 10 |     console.log(this); // the 'btn-test' button |
| 11 | }); |

Example for case #3:

| 1 | "use strict"; |
| 2 | function User(name) { |
| 3 |  this.name = name; |
| 4 | } |
| 5 |  |
| 6 | User.prototype.logInfo = () => { |
| 7 |     console.log(this); |
| 8 | } |
| 9 | User.prototype.showInfo = function () { |
| 10 |     console.log(this); |
| 11 | } |
| 12 |  |
| 13 | let user = new User('Neo'); |
| 14 | user.logInfo(); // Window object |
| 15 | user.showInfo(); // {name: 'Neo'} |

### 4.2.1 Implicit Binding

The below example defines object’s method using function expression. Therefore, the  this keyword refers to the object.

Example:

| 1 | "use strict"; |
| 2 | function welcome() { |
| 3 |     console.log(this); // {name: 'Neo', sayHi: f} |
| 4 |     console.log('Hi ' + this.name); // Hi Neo |
| 5 | } |
| 6 |  |
| 7 | let user = { |
| 8 | name: 'Neo', |
| 9 |     sayHi: welcome |
| 10 | } |
| 11 | user.sayHi(); |

### 4.2.2 Implicit Lost Binding

Continue the example of implicit binding, we assign the object’s method to a variable and invoke it as a function expression. As a result,  this in function expression will be  undefined.

| 1 | "use strict"; |
| 2 | function welcome() { |
| 3 |     console.log(this); // undefined |
| 4 |     console.log('Hi ' + this.name); // TypeError |
| 5 | } |
| 6 | let user = { |
| 7 | name: 'Neo', |
| 8 |     sayHi: welcome |
| 9 | } |
| 10 | let greetingFunc = user.sayHi; |
| 11 | greetingFunc(); |

## 4.3 globalThis

The globalThis property is used to ensure working on the global object of the current environment. In the case of web browsers,  globalThis is always the Window object.

An example that is run on a web page:

| 1 | "use strict"; |
| 2 |  |
| 3 | function test() { |
| 4 |     console.log(this); // undefined |
| 5 | console.log(globalThis); // Window object |
| 6 | } |
| 7 | test(); |

# Chapter 5
Object-Oriented Programming

Object-Oriented Programming (OOP) is a programming method that takes objects as the foundation for building algorithms and building programs.

In OOP, an object is understood as an instance in which the data and the procedures that act on the data are encapsulated together. The object is characterized by several operations and the information remembers the impact of these operations. Operations on an object are called methods or behaviors of that object.

## 5.1 Basic Concepts in OOP

In this section, we will learn concepts like encapsulation, classes, and instance, object inheritance, polymorphism, and virtual methods where the concept of data hiding through encapsulation is the key matter.

### 5.1.1 Encapsulation

Encapsulation is the ability to store data and the methods that act on an object separately from the others. All information in an object-oriented system is stored within its objects and can only be manipulated when the objects are ordered to perform operations.

Encapsulation is not just the collection of data and programs into a block, they are also understood in the sense that it is the identity of the data and the operations that act on that data. All that is visible of the encapsulated object is the object's communication methods.

### 5.1.2 Class and Instance

Class is a data type defined in the program. However, the concept of a class goes even further, it contains the implementation of the properties as well as possible operations on the data. In general, the class characterizes a sample of several objects and describes the internal structure of these objects. Objects of the same class have the same definition of their operations and the same data structure.

An instance is a real object in memory. In other words, the instance is a variable declared of type class. An instance is an object created from a class. The class describes the structure that includes the behavior and information of the instance, while the current state of the instance is determined by the operations performed on that instance.

### 5.1.3 Inheritance

Classification of objects is the arrangement of objects with the same communication behavior into the same group. After subclassing, the next job is to build classes that are derived from existing classes called base classes. These classes, in addition to their properties, retain the characteristics of the base classes. In other words, they inherit the behavior and data of the base class. The class that inherits from the base class is called a derived class. These derived classes in turn act as the base classes of other derived classes.

With inheritance we do not have to rebuild from scratch new classes, just need to add the necessary properties and methods into the derived classes. Thanks to inheritance, objects of different classes will share some methods of communication behaviors. Then we can send the same message to all objects with the same property, that is, objects with the same base type.

### 5.1.4 Polymorphism

Polymorphism is the ability to send the same message to different objects that share the same characteristics. In other words, the message is sent regardless of which class the receiver belongs to, only that the set of recipients has a certain property in common.

In OOP languages, polymorphism is represented by the ability to describe methods with the same name in different classes. This feature saves programmers from having to write cumbersome control structures in their programs. The different possibilities of the message are only really required when the program executes. The polymorphism of object-oriented programming is achieved mainly through concepts such as virtual methods, and dynamic linking techniques as below.

### 5.1.5 Virtual Method

The dynamic binding technique allows us to interfere with the operation of entities without recompiling the program. We can transmit and receive information from these new objects just like the existing ones.

To get that advantage, while implementing the object's classes we have to implement virtual methods. These are methods that will carry specific content at program execution time. When the compiler compiles the source program into machine language, the program segments of the virtual methods are included in the table of virtual methods. At program execution time, virtual methods will be called from this virtual method table.

## 5.2 The new Operator

The  new operator lets developers create an instance of a user-defined object type or of one of the built-in object types that have a constructor function.

![Rat with solid fill](Images/image00519.jpeg) We capitalize the first letter of function constructors to distinguish them from the normal functions.

Example:

| 1 | "use strict"; |
| 2 | function User(firstName, lastName) { |
| 3 |  this.firstName = firstName; |
| 4 |  this.lastName = lastName; |
| 5 | } |
| 6 | let user1 = new User('Neo', 'D. Truman'); |
| 7 | console.log(user1); |
| 8 | // User {firstName: 'Neo', lastName: 'D. Truman'} |

When the code  new User(...) is executed, the following things happen:

● A new empty object is created.

● The prototype of the object will have a new property, called “constructor”, which will be assigned the  User function to it.

● Finally, the constructor is called with  this binding to the object at the first step.

## 5.3 The prototype Property of Functions

In JavaScript, functions are also objects, because they can have properties and methods just like any other objects. What distinguishes them from other objects is that functions can be called.

This is an example of the  prototype property of functions.

| 1 | "use strict"; |
| 2 | function User(firstName, lastName) { |
| 3 |  this.firstName = firstName; |
| 4 |  this.lastName = lastName; |
| 5 | } |
| 6 | console.log(typeof User); // function |
| 7 | // Using function.prototype |
| 8 | User.prototype.logName = function () { |
| 9 |     console.log(this.firstName + ' ' + this.lastName); |
| 10 | } |
| 11 |  |
| 12 | let user1 = new User('Neo', 'D. Truman'); |
| 13 | console.log(user1); // User {firstName: 'Neo', lastName: 'D. Truman'} |
| 14 | user1.logName(); // Neo D. Truman |

The  user1 object doesn’t have the method  logName() but  user1.logName() worked and printed “Neo D. Truman” to the Console panel.

Let’s open the Console panel to see the result. Try to expand the  user1 object and its prototype ([[Prototype]]) to see more information in this picture.

![](Images/image00520.jpeg)

In the above picture, we can see the Prototype of  user1 is an object having the  logName() method because we defined the  User.prototype.logName as a function expression.

The following describes how  user1.logName(); can print “Neo D. Truman” to the console panel.

● Since  user1 doesn’t have the  logName() method, the JavaScript engine did search the method in  user1’s prototype.

● Because the prototype of  user1 is an object having the  logName() method, the desired method was found and invoked.

● In the method,  this was  user1 so that  this.firstName is “Neo” and  this.lastName is “D. Truman”. As a result, “Neo D. Truman” was printed on the console panel.

There is another prototype in  user1’s prototype (as in the picture) and we call them a Prototype Chain. Searching through the prototype chain could happen again and again until

● it found the desired property or method

● or it reaches  null since  null has no prototype.

Methods of objects should be defined in the  Function.prototype objects because of these advantages:

● Save memory since it only takes up one memory area.

● Can modify the methods easily after creating instances since all instances only refer to one prototype object.

Let’s try the below example:

| 1 | "use strict"; |
| 2 | function User(firstName, lastName) { |
| 3 |  this.firstName = firstName; |
| 4 |  this.lastName = lastName; |
| 5 |  this.badMethod = function () { |
| 6 |         console.log('Should not define method like this'); |
| 7 |     } |
| 8 | } |
| 9 |  |
| 10 | User.prototype.logName = function () { |
| 11 |     console.log(this.firstName + ' ' + this.lastName); |
| 12 | } |
| 13 |  |
| 14 | let user1 = new User('Neo', 'D. Truman'); |
| 15 | let user2 = new User('John', 'Conner'); |
| 16 |  |
| 17 | user2.badMethod = function () { |
| 18 |     console.log('The badMethod() method of user2'); |
| 19 | } |
| 20 | user1.badMethod(); // Should not define method like this |
| 21 | user2.badMethod(); // The badMethod() method of user2 |
| 22 |  |
| 23 | User.prototype.logName = function () { |
| 24 |     console.log('The logName() method was modified'); |
| 25 | } |
| 26 | user1.logName(); // The logName() method was modified |
| 27 | user2.logName(); // The logName() method was modified |

## 5.4 Extend Function Objects

We can use the  prototype property of functions to extend the function objects. The below example implements the  String.format() method that returns a formatted string by given format and arguments.

Example:

| 1 | "use strict"; |
| 2 | String.prototype.format = function () { |
| 3 |  let args = arguments; |
| 4 |  return  this.replace(/{(\d+)}/g, function (match, number) { |
| 5 |  return  typeof args[number] != 'undefined' ? args[number] : match; |
| 6 |     }); |
| 7 | } |
| 8 |  |
| 9 | let greetingStr = 'Hello {0} {1}. How are you, {0}?'.format('Neo', 'D. Truman'); |
| 10 | console.log(greetingStr); |
| 11 | // Hello Neo D. Truman. How are you, Neo? |

## 5.5 Reflect

Reflect is a built-in object that helps:

● Detecting or retrieving whether an object contains certain properties.

| 1 | "use strict"; |
| 2 | let obj = { |
| 3 | firstName: "Neo", |
| 4 | lastName: "D. Truman" |
| 5 | } |
| 6 | Reflect.has(obj, 'firstName'); // true |
| 7 | Reflect.get(obj, 'firstName'); // Neo |
| 8 | Reflect.has(obj, 'age'); // false |

● Returning the object's own keys

| 9 | Reflect.ownKeys(obj); // ['firstName', 'lastName'] |

● Adding a new property to the object

| 10 | Reflect.set(obj, 'age', 39); |
| 11 | console.log(obj.age); // 39 |

● Setting the prototype of an object. Returns  true if the update was successful.

| 1 | "use strict"; |
| 2 | let obj1 = { |
| 3 | firstName: 'Neo', |
| 4 | lastName: 'D. Truman', |
| 5 | logFullname: function () { |
| 6 |         console.log(this.firstName + ' ' + this.lastName); |
| 7 |     } |
| 8 | } |
| 9 |  |
| 10 | let obj2 = { |
| 11 | firstName: 'John' |
| 12 | } |
| 13 | // Set obj1 as prototype of obj2 |
| 14 | Reflect.setPrototypeOf(obj2, obj1); |
| 15 | obj2.logFullname(); // John D. Truman |

## 5.6 Classes

Classes in JavaScript are built on the prototype chain and used to create objects. There are two types of classes; these are class expression and class declaration, but no types support hoisting.

### 5.6.1 Class declarations

One way to define a class is using a class declaration. To declare a class, you use the  class keyword with the name of the class.

Example:

| 1 | "use strict"; |
| 2 | class  User { |
| 3 |  constructor(firstName, lastName) { |
| 4 |  this.firstName = firstName; |
| 5 |  this.lastName = lastName; |
| 6 |     } |
| 7 |     logName() { |
| 8 |         console.log(this.firstName + ' ' + this.lastName); |
| 9 |     } |
| 10 | } |
| 11 |  |
| 12 | let user1 = new User('Neo', 'D. Truman'); |
| 13 | console.log(user1.firstName); // Neo |
| 14 | console.log(user1); |

We can open the Console panel to see the result. Try to expand the  user1 object and its prototype ([[Prototype]]) to see more information in this picture.

![](Images/image00521.jpeg)

As in the picture,  user1 is an object having two properties  firstName and  lastName. The  logName() method of  user1 is put inside the object’s prototype.

### 5.6.2 Class expressions

The class expression is another way to define classes. Class expressions can be named or unnamed. The name given to a class expression is local to the class's body.

Example:

| 1 | "use strict"; |
| 2 | // unnamed |
| 3 | let User = class { |
| 4 |  constructor(firstName, lastName) { |
| 5 |  this.firstName = firstName; |
| 6 |  this.lastName = lastName; |
| 7 |     } |
| 8 | } |
| 9 | console.log(User.name); // User |
| 10 | let user1 = new User('Neo', 'D. Truman'); |
| 11 |  |
| 12 | // named |
| 13 | let AnotherUser = class  UserClass{ |
| 14 |  constructor(firstName, lastName) { |
| 15 |  this.firstName = firstName; |
| 16 |  this.lastName = lastName; |
| 17 |     } |
| 18 | } |
| 19 | console.log(AnotherUser.name); // UserClass |
| 20 | // But AnotherUser must be used to create objects |
| 21 | let user2 = new AnotherUser('Neo', 'D. Truman'); |

### 5.6.3 Constructor

The  constructor method is a function that will be called automatically when creating new objects. They are often used as a gateway that receives initial data for the objects.

In a constructor’s function body, we can use the  super keyword to call the constructor of the super class.

### 5.6.4 Static Methods and Properties

The  static keyword is used to specify static variables and methods of classes. Static variables or methods are accessed via the class name (not through the class instance).

Example:

| 1 | "use strict"; |
| 2 | class  User { |
| 3 |  static staticProperty = "Static Value"; |
| 4 |  |
| 5 |  constructor(firstName, lastName) { |
| 6 |  this.firstName = firstName; |
| 7 |  this.lastName = lastName; |
| 8 |     } |
| 9 |     logInfo() { |
| 10 |         console.log(this.firstName + ' ' + this.lastName); |
| 11 |     } |
| 12 |  static staticMethod() { |
| 13 |         console.log('This is a static method'); |
| 14 |     } |
| 15 | } |
| 16 |  |
| 17 | console.log(User.staticProperty); // Static Value |
| 18 | User.staticMethod(); // This is a static method |
| 19 |  |
| 20 | let user1 = new User('Neo', 'D. Truman'); |
| 21 | console.log(user1.staticProperty); // undefined |
| 22 | console.log(user1.staticMethod); // undefined |
| 23 | console.log(user1); |

Inside a class, static methods and static properties can only be used within another static method of the class.

| 1 | "use strict"; |
| 2 | class  User { |
| 3 |  static staticProperty = "Static Value"; |
| 4 |  |
| 5 |  constructor(firstName, lastName) { |
| 6 |  this.firstName = firstName; |
| 7 |  this.lastName = lastName; |
| 8 |     } |
| 9 |     logInfo() { |
| 10 |         console.log('Access the static property from non-static method: ' + this.staticProperty); |
| 11 |     } |
| 12 |  static staticMethod() { |
| 13 |         console.log('Value of the static property: ' + this.staticProperty); |
| 14 |     } |
| 15 | } |
| 16 |  |
| 17 | User.staticMethod(); |
| 18 | // Value of the static property: Static Value |
| 19 |  |
| 20 | let user1 = new User('Neo', 'D. Truman'); |
| 21 | user1.logInfo(); |
| 22 | // Access the static property from the non-static method: undefined |

![Crocodile with solid fill](Images/image00522.jpeg) We can refer to the static properties and method as properties of the  constructor:  this.constructor.STATIC_PROPERTY / this.constructor.STATIC_METHOD(). However, we should avoid using them because it breaks the pattern that is “We can only call static methods or use static properties within another static method of the same class”.

### 5.6.5 Private Methods and Properties

The hash # prefix is used to declare private properties and private methods of objects. Private fields can only be accessed inside the classes. They are not available for the class instances or in the derived classes.

Example:

| 1 | "use strict"; |
| 2 | class  User { |
| 3 |  // Private properties must be declared here |
| 4 |     #age; |
| 5 |  constructor(firstName, lastName, age) { |
| 6 |  this.firstName = firstName; |
| 7 |  this.lastName = lastName; |
| 8 |  this.#age = age; |
| 9 |     } |
| 10 |     logInfo() { |
| 11 |         console.log(this.firstName + ' ' + this.lastName); |
| 12 |  this.#logAge(); |
| 13 |     } |
| 14 |  |
| 15 |     #logAge() { |
| 16 |         console.log(this.#age); |
| 17 |     } |
| 18 | } |
| 19 |  |
| 20 | let user1 = new User('Neo', 'D. Truman', 39); |
| 21 | user1.logInfo(); |
| 22 | console.log(user1); |
| 23 |  |
| 24 | // Un-comment the below lines will cause SyntaxError |
| 25 | // user1.#age; // SyntaxError |
| 26 | // user1.#logAge(); // SyntaxError |

We can open the Console panel to see the result and check the value of the  user1 variable. Try to expand the object and its prototype ([[Prototype]]) to see more information in this picture.

![](Images/image00523.jpeg)

We can see that all private fields are located directly in the object, not in its prototype. And if we refer to # names from out of scope, a  SyntaxError will be thrown.

![Crocodile with solid fill](Images/image00524.jpeg) It is also a syntax error to attempt to remove private fields with  delete.

### 5.6.6 Sub Classing with Extends

The  extends keyword is used to create a class as a derived class (child of another class).

The  super keyword is used to call the constructor of the super class.

![Fish with solid fill](Images/image00525.jpeg) If there is a constructor present in the subclass, it needs to first call  super() before using "this".

Example:

Source code of the  User class:

| 1 | "use strict"; |
| 2 | class  User { |
| 3 |  // Private properties must be declared here |
| 4 |     #age; |
| 5 |  |
| 6 |  constructor(firstName, lastName, age) { |
| 7 |  this.firstName = firstName; |
| 8 |  this.lastName = lastName; |
| 9 |  this.#age = age; |
| 10 |     } |
| 11 |  |
| 12 |  // getter and setter of private properties |
| 13 |     getAge() { |
| 14 |  return  this.#age; |
| 15 |     } |
| 16 |     setAge(newAge) { |
| 17 |  this.#age = newAge; |
| 18 |     } |
| 19 |  |
| 20 |  // Public methods here |
| 21 |     logInfo() { |
| 22 |         console.log(`Name: ${this.firstName}  ${this.lastName}`); |
| 23 |  this.#logAge(); |
| 24 |     } |
| 25 |  |
| 26 |  // Private methods here |
| 27 |     #logAge() { |
| 28 |         console.log(`Age: ${this.#age}`); |
| 29 |     } |
| 30 | } |

Source code of the  Student class:

| 1 | "use strict"; |
| 2 | class  Student  extends User { |
| 3 |  constructor(firstName, lastName, age, id) { |
| 4 |  // Must call constructor of the super class before using 'this.' |
| 5 |  super(firstName, lastName, age); |
| 6 |  this.id = id; |
| 7 |     } |
| 8 |  |
| 9 |     logInfo() { |
| 10 |         console.log('Information of the student:'); |
| 11 |  |
| 12 |  // Constructor of the super class initialized the firstName and lastName properties but the Student class still owns the properties |
| 13 |  // super.firstName; // undefined |
| 14 |  // super.lastName; // undefined |
| 15 |         console.log(`Name: ${this.firstName}  ${this.lastName}`); |
| 16 |  |
| 17 |  // Cannot access private fields of super class |
| 18 |  // super.#age; // SyntaxError |
| 19 |  // super.#logAge(); // SyntaxError |
| 20 |  // Therefore, we must use the getter as below |
| 21 |         console.log(`Age: ${super.getAge()}`); |
| 22 |  // We can use this.getAge() instead of super.getAge() since the method could be found in the prototype chain |
| 23 |  |
| 24 |         console.log(`Id: ${this.id}`); |
| 25 |     } |
| 26 | } |

Source code of the  Teacher class:

| 1 | class  Teacher  extends User { |
| 2 |     logInfo() { |
| 3 |         console.log('Information of the teacher:'); |
| 4 |         console.log('...'); |
| 5 |     } |
| 6 | } |

Source code of the  SecurityGuard class:

| 1 | class  SecurityGuard  extends User { } |

Let’s try the above code!

| 1 | let student1 = new Student('John', 'Conner', 20, '123456'); |
| 2 | console.log(student1); |
| 3 | student1.logInfo(); |
| 4 |  |
| 5 | let teacher1 = new Teacher('Neo', 'D. Truman', 39); |
| 6 | console.log(teacher1); |
| 7 | teacher1.logInfo(); |
| 8 |  |
| 9 | let guard1 = new SecurityGuard('William', 'Smith', 30); |
| 10 | console.log(guard1); |
| 11 | guard1.logInfo(); |

We can open the Console panel to see the result and check the values of the  student1, teacher1, and  guard1 variables. Try to expand the objects and their prototypes ([[Prototype]]) to see more information as the below pictures.

![](Images/image00526.jpeg)

The  student1 object has its prototype object having a method named “logInfo”. This  logInfo() method is different from the  logInfo() method in the User class.

student1’s prototype object also has its prototype which is a  User object.

When executed student1.logInfo(), JS engine searched the method in the  student1 object first but was not found. Therefore, it continued to search for it in  student1’s prototype. It found the method there and invoked it.

![](Images/image00527.jpeg)

teacher1.logInfo() proceeded in the same way as student1.logInfo() since  teacher1’s structure is almost the same as student1’s structure.

![](Images/image00528.jpeg)

The  guard1 object has its prototype object (called Object I). And  guard1’s prototype object also has its prototype which is a User object (called Object II).

When executed  guard1.logInfo(), JS engine searched the method in the  guard1  object first but was not found. Therefore, it continued to search in  guard1’s prototype (Object I) but was not found again. Followed the prototype chain, it continued to search in Object II and found the method there and invoked it.

In conclusion, subclassing in JavaScript is built on the prototype chain.

### 5.6.7 ES5 JavaScript OOP for Old Browsers

The  class keyword is not supported by old browsers such as Internet Explorer. Therefore, we have another solution in this section that implement JavaScript OOP in ES5 code.

We will implement the  __extendsClass function to create a derived class from the base class. This function will

● set up the prototype chain so that derived class can use public methods of the base class

● initialize all properties of the derived class based on the base class

● create the constructor of the derived class

The  __extendsClass function is as below.

| 1 | var __extendsClass = (this && this.__extendsClass) &#124;&#124; (function () { |
| 2 |  // d: derived; b: base; p: property |
| 3 |  var extendStatics = function (d, b) { |
| 4 |     extendStatics = Object.setPrototypeOf &#124;&#124; |
| 5 | ({ __proto__: [] } instanceof  Array && function (d, b) { |
| 6 |         d.__proto__ = b; |
| 7 |       }) &#124;&#124; |
| 8 |  function (d, b) { |
| 9 |  for (var p in b) |
| 10 |  if (Object.prototype.hasOwnProperty.call(b, p)) |
| 11 |             d[p] = b[p]; |
| 12 |       }; |
| 13 |  return extendStatics(d, b); |
| 14 |   }; |
| 15 |  return  function (d, b) { |
| 16 |  if (typeof b !== "function" && b !== null) |
| 17 |  throw  new TypeError(String(b) + " is not a constructor or null"); |
| 18 |     extendStatics(d, b); |
| 19 |  function __() { |
| 20 |  this.constructor = d; |
| 21 |     } |
| 22 | d.prototype = b === null ? Object.create(b) : (__.prototype = b.prototype, new __()); |
| 23 |   }; |
| 24 | })(); |

Source code of the  User class:

| 1 | var User = (function () { |
| 2 |  // Private properties here |
| 3 |  var _age; |
| 4 |  |
| 5 |  // Private methods here |
| 6 |  function _logAge() { |
| 7 |     console.log("Age: " + _age); |
| 8 |   } |
| 9 |  |
| 10 |  // Constructor |
| 11 |  function User(firstName, lastName, age) { |
| 12 |  this.firstName = firstName; |
| 13 |  this.lastName = lastName; |
| 14 |     _age = age; |
| 15 |   } |
| 16 |  |
| 17 |  // Public methods here |
| 18 | User.prototype.getAge = function () { |
| 19 |  // Access private property (_age) via Closure |
| 20 |  return _age; |
| 21 |   }; |
| 22 | User.prototype.setAge = function (newAge) { |
| 23 |     _age = newAge; |
| 24 |   }; |
| 25 | User.prototype.logInfo = function () { |
| 26 |     console.log("Name: " + this.firstName + " " + this.lastName); |
| 27 |  // Access private method (_logAge) via Closure |
| 28 |     _logAge(); |
| 29 |   }; |
| 30 |  // Public methods are supported by using Prototype Chain |
| 31 |  |
| 32 |  // Static properties here |
| 33 |   User.staticProp = 0; |
| 34 |  |
| 35 |  // Static methods here |
| 36 | User.staticMethod = function () { |
| 37 |     console.log('Message from static method'); |
| 38 |   }; |
| 39 |  // Static properties and methods are implemented as Properties of Function |
| 40 |  |
| 41 |  return User; |
| 42 | }()); |

Source code of the  Student class:

| 1 | var Student = (function (_super) { |
| 2 |  // Call the __extendsClass function at the beginning |
| 3 |   __extendsClass(Student, _super); |
| 4 |  |
| 5 |  // Private properties here |
| 6 |  var _privateProp = 'Private Property'; |
| 7 |  |
| 8 |  // Constructor |
| 9 |  function Student(firstName, lastName, age, id) { |
| 10 |  this.id = id; |
| 11 |  var argArray = [firstName, lastName, age]; |
| 12 |  return _super !== null && _super.apply(this, argArray) &#124;&#124; this; |
| 13 |  // return _super !== null && _super.apply(this, arguments) &#124;&#124; this; |
| 14 |   } |
| 15 |  |
| 16 |  // Public methods here |
| 17 | Student.prototype.logInfo = function (times) { |
| 18 |     console.log('Information of the student:'); |
| 19 |     console.log("Name: " + this.firstName + " " + this.lastName); |
| 20 |     console.log("Age: " + this.getAge()); // call public method of super class |
| 21 |     console.log("Id: " + this.id); |
| 22 |     console.log('Access _privateProp from the method:', _privateProp); |
| 23 |   }; |
| 24 |  |
| 25 |  return Student; |
| 26 | }(User)); // enter base class here |

Source code of the  Teacher class:

| 1 | var Teacher = (function (_super) { |
| 2 |  // Call the __extendsClass function at the beginning |
| 3 |   __extendsClass(Teacher, _super); |
| 4 |  |
| 5 |  // Constructor |
| 6 |  function Teacher() { |
| 7 |  // Arguments of Teacher's constructor is the same as User's constructor |
| 8 |  return _super !== null && _super.apply(this, arguments) &#124;&#124; this; |
| 9 |   } |
| 10 |  |
| 11 |  // Public methods here |
| 12 | Teacher.prototype.logInfo = function (times) { |
| 13 |     console.log('Information of the teacher:'); |
| 14 |     console.log('...'); |
| 15 |   }; |
| 16 |  |
| 17 |  return Teacher; |
| 18 | }(User)); // enter base class here |

Source code of the  SecurityGuard class:

| 1 | var SecurityGuard = (function (_super) { |
| 2 |  // Call the __extendsClass function at the beginning |
| 3 |   __extendsClass(SecurityGuard, _super); |
| 4 |  |
| 5 |  // Constructor |
| 6 |  function SecurityGuard() { |
| 7 |  // Arguments of SecurityGuard's constructor is the same as User's constructor |
| 8 |  return _super !== null && _super.apply(this, arguments) &#124;&#124; this; |
| 9 |   } |
| 10 |  |
| 11 |  return SecurityGuard; |
| 12 | }(User)); // enter base class here |

Let’s try the above code!

| 1 | console.log('Access static property and method:'); |
| 2 | console.log(User.staticProp); |
| 3 | User.staticMethod(); |
| 4 | console.log('-------------'); |
|  | /* On the Console panel, we will see:Access static property and method:0Message from static method-------------*/ |
| 5 |  |
| 6 | let student1 = new Student('John', 'Conner', 20, '123456'); |
| 7 | console.log(student1); |
| 8 | student1.logInfo(); |
| 9 | console.log('Access _privateProp via instance:', student1._privateProp); |
|  | /* On the Console panel, we will see:Student {id: '123456', firstName: 'John', lastName: 'Conner'}Information of the student:Name: John ConnerAge: 20Id: 123456Access _privateProp from the method: Private PropertyAccess _privateProp via instance: undefined*/ |
| 10 |  |
| 11 | let teacher1 = new Teacher('Neo', 'D. Truman', 39); |
| 12 | console.log(teacher1); |
| 13 | teacher1.logInfo(); |
|  | /* On the Console panel, we will see:Teacher {firstName: 'Neo', lastName: 'D. Truman'}Information of the teacher:...*/ |
| 14 |  |
| 15 | let guard1 = new SecurityGuard('William', 'Smith', 30); |
| 16 | console.log(guard1); |
| 17 | guard1.logInfo(); |
|  | /* On the Console panel, we will see:SecurityGuard {firstName: 'William', lastName: 'Smith'}Name: William SmithAge: 30*/ |

# About the Author

Neo D. Truman has been using computers since 1998 when he was a child. He’s got a Master of Science in Information Technology degree in 2011\. He has 15+ years of experience in software development, especially full-stack web development.

# Other Books by The Author

![](Images/image00529.jpeg)

[https://www.amazon.com/dp/B09VDRLYBT](https://www.amazon.com/dp/B09VDRLYBT)

![](Images/image00530.jpeg)

[https://www.amazon.com/dp/B09P6KH74B](https://www.amazon.com/dp/B09P6KH74B)

# Please leave a Review/Thought on Amazon

Thank you for purchasing and reading my book. I am extremely grateful and hope you found value in reading it.

Please consider sharing it with friends or family and leaving a review on the Amazon website. Your feedback and support are always appreciated, and inspire me to continue doing what I love. Please go to Amazon and leave a review if you’d like my book.

My email is [neodtruman@gmail.com](mailto:neodtruman@gmail.com). If you have any questions, please send me an email. I am always happy to hear from people who’ve read my books. I’ll try my best to answer every email I receive. The subject should be “[JavaScript Object-Oriented Programming By Examples] <Your subject here>” so that I could filter and answer your questions quickly.

You can also follow me on the Amazon Author page, [https://www.amazon.com/Neo-D-Truman/e/B09P6LHL2M](https://www.amazon.com/Neo-D-Truman/e/B09P6LHL2M)