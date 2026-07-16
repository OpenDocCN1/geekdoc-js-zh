![](common/cover.jpg)

![JavaScript for ABAP® Developers – Cover](common/cover.jpg)

Brandon Caulfield

# JavaScript for ABAP® Developers

This E-Bite is protected by copyright. It contains a digital watermark, a signature that indicates which person may use this copy. Full [Legal Notes](#usage_service_notes.html_legal_notes) and [Notes on Usage](#usage_service_notes.html_usage) can be found at the end of this publication.

![Logo Rheinwerk Publishing](common/logo_sap.png)

## SAP PRESS E-Bites

SAP PRESS E-Bites provide you with a high-quality response to your specific project need. If you’re looking for detailed instructions on a specific task; or if you need to become familiar with a small, but crucial sub-component of an SAP product; or if you want to understand all the hype around product xyz: SAP PRESS E-Bites have you covered. Authored by the top professionals in the SAP universe, E-Bites provide the excellence you know from SAP PRESS, in a digestible electronic format, delivered (and consumed) in a fraction of the time!

### The Author of this E-Bite

[![](bilderklein/klein2155_caulfield.png)](img-f_none_00_00.html)

Brandon Caulfield is a senior engineer at SAP and part of the SAP Customer Data Cloud team. He began his career in SAP Business One and after learning to code moved to ABAP development. He then branched out into SAPUI5 and SAP Cloud Platform, where he specialized in helping businesses build full-stack, cloud-based solutions. Although his focus as an engineer has now shifted to software as a service (SaaS), he is a regular contributor to open-source SAPUI5 libraries and tools through GitHub and SAP Community. In his spare time, he loves to learn new things and tinker with languages like Python and Go, alongside maintaining his developer YouTube channel called Code with Brandon.

## What You’ll Learn

In this E-Bite, you’ll learn how to code with the JavaScript language. Get started by exploring JavaScript principles and executing your first pieces of code in the browser and with Node.js. Then walk through key JavaScript elements and features including variables, operators, functions, data structures, the Document Object Model, AJAX, jQuery, and more. Each section includes comparisons to ABAP concepts and practical code examples so you can understand and then apply the basics of JavaScript programming. Finish with debugging and error handling tips to make sure your code runs smoothly.

[1](#01_001.html_h1)   [Introduction to JavaScript and its Basic Principles](#01_001.html_h1)

[1.1](#01_001.html_h1.1)   [ECMAScript and Browser Compatibility](#01_001.html_h1.1)

[1.2](#01_002.html_h1.2)   [Runtimes and Engines](#01_002.html_h1.2)

[1.3](#01_003.html_h1.3)   [Preparation, Tooling, and IDEs](#01_003.html_h1.3)

[1.4](#01_004.html_h1.4)   [Executing JavaScript Code in the Browser](#01_004.html_h1.4)

[1.5](#01_005.html_h1.5)   [Executing JavaScript Code with Node.js](#01_005.html_h1.5)

[1.6](#01_006.html_h1.6)   [Comments](#01_006.html_h1.6)

[2](#02_001.html_h2)   [Variables and Data Types](#02_001.html_h2)

[2.1](#02_001.html_h2.1)   [Variables](#02_001.html_h2.1)

[2.2](#02_002.html_h2.2)   [Data Types](#02_002.html_h2.2)

[2.3](#02_003.html_h2.3)   [Scope of Global and Local Variables](#02_003.html_h2.3)

[2.4](#02_004.html_h2.4)   [Old Syntax versus Modern Syntax](#02_004.html_h2.4)

[2.5](#02_005.html_h2.5)   [String and Number Methods](#02_005.html_h2.5)

[3](#03_001.html_h3)   [Operators and Loops](#03_001.html_h3)

[3.1](#03_001.html_h3.1)   [Arithmetic Operators](#03_001.html_h3.1)

[3.2](#03_002.html_h3.2)   [String Operators](#03_002.html_h3.2)

[3.3](#03_003.html_h3.3)   [Comparison Operators](#03_003.html_h3.3)

[3.4](#03_004.html_h3.4)   [Logical Operators](#03_004.html_h3.4)

[3.5](#03_005.html_h3.5)   [Conditional Operators](#03_005.html_h3.5)

[3.6](#03_006.html_h3.6)   [Loops](#03_006.html_h3.6)

[4](#04_001.html_h4)   [Functions](#04_001.html_h4)

[4.1](#04_001.html_h4.1)   [Function Definition](#04_001.html_h4.1)

[4.2](#04_002.html_h4.2)   [Parameters and the Return Statement](#04_002.html_h4.2)

[4.3](#04_003.html_h4.3)   [Global Scope and Closures](#04_003.html_h4.3)

[5](#05_001.html_h5)   [Data Structures](#05_001.html_h5)

[5.1](#05_001.html_h5.1)   [Arrays and Array Methods](#05_001.html_h5.1)

[5.2](#05_002.html_h5.2)   [Objects and Object Methods](#05_002.html_h5.2)

[6](#06_001.html_h6)   [JSON](#06_001.html_h6)

[6.1](#06_001.html_h6.1)   [JSON Syntax](#06_001.html_h6.1)

[6.2](#06_002.html_h6.2)   [JSON Methods](#06_002.html_h6.2)

[6.3](#06_003.html_h6.3)   [OData and SAPUI5](#06_003.html_h6.3)

[7](#07_001.html_h7)   [The Document Object Model (DOM)](#07_001.html_h7)

[7.1](#07_001.html_h7.1)   [DOM Example](#07_001.html_h7.1)

[7.2](#07_002.html_h7.2)   [Traversing the DOM](#07_002.html_h7.2)

[7.3](#07_003.html_h7.3)   [Selector Methods](#07_003.html_h7.3)

[7.4](#07_004.html_h7.4)   [DOM Manipulation](#07_004.html_h7.4)

[8](#08_001.html_h8)   [HTML Events](#08_001.html_h8)

[8.1](#08_001.html_h8.1)   [Registering Events](#08_001.html_h8.1)

[8.2](#08_002.html_h8.2)   [Handling Complimenting Events](#08_002.html_h8.2)

[8.3](#08_003.html_h8.3)   [Common HTML Events](#08_003.html_h8.3)

[9](#09_001.html_h9)   [Asynchronous JavaScript](#09_001.html_h9)

[9.1](#09_001.html_h9.1)   [Callbacks in JavaScript](#09_001.html_h9.1)

[9.2](#09_002.html_h9.2)   [JavaScript Promise](#09_002.html_h9.2)

[9.3](#09_003.html_h9.3)   [Async and Await](#09_003.html_h9.3)

[10](#10_001.html_h10)   [Classes](#10_001.html_h10)

[10.1](#10_001.html_h10.1)   [Class Definition](#10_001.html_h10.1)

[10.2](#10_002.html_h10.2)   [Methods](#10_002.html_h10.2)

[10.3](#10_003.html_h10.3)   [Static versus Dynamic Attributes and Methods](#10_003.html_h10.3)

[10.4](#10_004.html_h10.4)   [Inheritance](#10_004.html_h10.4)

[11](#11_001.html_h11)   [AJAX](#11_001.html_h11)

[11.1](#11_001.html_h11.1)   [XMLHttpRequest Object](#11_001.html_h11.1)

[11.2](#11_002.html_h11.2)   [Modern Syntax: Fetch API](#11_002.html_h11.2)

[12](#12_001.html_h12)   [jQuery: Your First JavaScript Library](#12_001.html_h12)

[12.1](#12_001.html_h12.1)   [Importing a jQuery Library](#12_001.html_h12.1)

[12.2](#12_002.html_h12.2)   [Using jQuery Selectors](#12_002.html_h12.2)

[12.3](#12_003.html_h12.3)   [Registering Events](#12_003.html_h12.3)

[12.4](#12_004.html_h12.4)   [Changing HTML Elements](#12_004.html_h12.4)

[12.5](#12_005.html_h12.5)   [Adding and Removing Elements from the DOM](#12_005.html_h12.5)

[12.6](#12_006.html_h12.6)   [Changing CSS](#12_006.html_h12.6)

[12.7](#12_007.html_h12.7)   [jQuery AJAX](#12_007.html_h12.7)

[13](#13_001.html_h13)   [Web APIs](#13_001.html_h13)

[13.1](#13_001.html_h13.1)   [Browser Navigation and History](#13_001.html_h13.1)

[13.2](#13_002.html_h13.2)   [Geolocation](#13_002.html_h13.2)

[13.3](#13_003.html_h13.3)   [Browser Storage](#13_003.html_h13.3)

[14](#14_001.html_h14)   [Debugging and Error Handling](#14_001.html_h14)

[14.1](#14_001.html_h14.1)   [Error Types and Views](#14_001.html_h14.1)

[14.2](#14_002.html_h14.2)   [Debugging](#14_002.html_h14.2)

[14.3](#14_003.html_h14.3)   [Error Handling](#14_003.html_h14.3)

[15](#15_001.html_h15)   [What’s Next?](#15_001.html_h15)

# 1    Introduction to JavaScript and its Basic Principles

JavaScript started life as a programming language that allowed you to take static webpages and add complex logic to dynamically react to user input or application programming interface (API) changes. Since then, it has developed into an all-purpose programming language that can be used to build almost anything with its vast ecosystem of libraries and frameworks. Undoubtably, one of the frameworks you might have heard of is part of the SAP product range, SAPUI5, or OpenUI5, which is the open-source version of SAPUI5.

JavaScript runs in all modern web browsers: Chrome, Firefox, Safari, Edge, and so on. With the introduction of runtimes such as Node.js, JavaScript also runs on servers, much like ABAP runs on the ABAP stack. This means JavaScript is no longer just a frontend language anymore but can perform backend server logic as well, effectively letting you build and run full stack applications using JavaScript code alone.

JavaScript at its core is a single-threaded, synchronous programming language, which means each piece of code is executed in the order it was written. This can become a limitation, as your functions cannot execute until the previous function has completed its action. In [Section 9](#09_001.html_h9), we will learn more about how to overcome this limitation using a concept called asynchronous JavaScript, which allows a function to run in the background without holding up the functions directly after.

Coming from ABAP, one of the main differences to get used to with JavaScript is its flexibility and dynamic (loose) typing system, which we’ll discuss further in [Section 2](#02_001.html_h2). Many of the errors in your JavaScript will only become apparent at runtime. This contrasts with ABAP (which is a compiled language), which has the benefit of catching most of these errors at compile time. So, it is crucial you implement proper error handling wherever possible.

One of the biggest benefits of JavaScript is that you can write and execute your code almost anywhere. You do not need a connection to an SAP instance as you do with ABAP to run your code. That is why, throughout this E-Bite, we encourage you to try absolutely everything you read. The best and quickest way to learn JavaScript is by constantly trying out the new concepts you read about.

In this section, we’ll get started with the important concepts to develop a contextual understanding of JavaScript. We’ll discuss compatibility, runtimes, preparation steps, and how to execute your first piece of JavaScript code in the browser and with Node.js. We’ll end with a look at how comments function with JavaScript.

## 1.1    ECMAScript and Browser Compatibility

ECMAScript is the formal standard of the JavaScript programming language and has been in use since 1997\. ECMAScript (ES) highlights the different releases of JavaScript and what features are included with each version. This is important because different browsers support these releases in certain browser versions. Some browsers don’t support certain versions at all, as is the case with Internet Explorer not supporting ES6 (ECMAScript 2015). Compare this to ABAP releases, where certain features are only available on later versions.

###### Note

You can see the full version history of ECMAScript at [https://en.wikipedia.org/wiki/ECMAScript](https://en.wikipedia.org/wiki/ECMAScript).

ES6 is one of the more well-known examples where new keywords like <samp class="listingcharacter">let</samp> and <samp class="listingcharacter">const</samp> were introduced (which we will cover in detail in [Section 2](#02_001.html_h2)). These are considered modern JavaScript keywords in comparison to the older <samp class="listingcharacter">var</samp> statement used to define variables. This E-Bite is all about modern JavaScript, so it is important to understand ECMAScript and to stay up to date on new features or standards as they are released.

## 1.2    Runtimes and Engines

The JavaScript code you write can be executed inside a web browser, on your local machine, or even on a server. Web browsers have their own runtime environments that let your JavaScript interact with the webpage’s Document Object Model (DOM), the browser itself (like using local or session storage), or external APIs (where you make a call to a server).

For a browser to use your JavaScript code, it must run its own JavaScript engine so it can parse your code and turn it into executable commands that your machine understands. For example, Chrome has the V8 JavaScript engine, Firefox has SpiderMonkey, and Microsoft Edge has Chakra.

Runtimes and engines are an important concept because your JavaScript code will need to run in more than one environment, and not all features are supported equally in every browser or browser version (see [Section 1.1](#01_001.html_h1.1)).

We’ll discuss how to run JavaScript with Node.js in [Section 1.5](#01_005.html_h1.5).

## 1.3    Preparation, Tooling, and IDEs

You can use any integrated development environment (IDE) you choose to write your JavaScript code. One of the more popular choices currently is Visual Studio (VS) Code from Microsoft, but many developers are already using Eclipse for their pure ABAP work (outside of Transaction SE38, that is!) and you can use it for JavaScript as well. The examples in this E-Bite are split into two broad categories:

*   Running JavaScript on a webpage using an index.html file. The JavaScript code either runs inside the index.html file or is referenced from an external JavaScript file (e.g., app.js).

*   Running a JavaScript file without an index.html file (webpage) using node.js.

We also recommend splitting each section into its own separate folder, as we will be making use of multiple index.html and app.js files in our examples and the folders will help organize your code.

From this point on (to keep continuity), we will be running our JavaScript examples exclusively in VS Code, as it includes IntelliSense, debugging, formatting, code navigation, refactorings, and many other advanced language features within a clean and user-friendly interface. You can find the installation file for VS Code at [http://s-prs.co/v535900](http://s-prs.co/v535900). We will be writing and executing our code with some key VS Code extensions, which you need to install from [http://s-prs.co/v535901](http://s-prs.co/v535901).

###### Note

For more information about VS Code, see [http://s-prs.co/v535902](http://s-prs.co/v535902).

To run our webpage example (using an index.html file), we will be making use of an extension called Live Server ([http://s-prs.co/v535903](http://s-prs.co/v535903)). With this extension, you will be able to preview changes to your code quickly and easily, much like activating and executing your ABAP code in Transaction SE38\. It will rerun your code every time you save, so you can view your changes in real time.

We also recommend an extension called Prettier – Code Formatter ([http://s-prs.co/v535904](http://s-prs.co/v535904)), which is just like using pretty print in Transaction SE38 to help format your code, and ESLint ([http://s-prs.co/v535905](http://s-prs.co/v535905)), which statically checks your code like the ABAP syntax check.

## 1.4    Executing JavaScript Code in the Browser

Before we write any JavaScript code in our IDE, we are going to try some code in the Google Chrome browser console. Open a browser window and press [F12]. If you are not on the tab already, look for the Console tab and click it. The browser console is where we can log information from our app, and we are going to use it to execute some JavaScript code. Type the following into the console and press [Enter]:

```
console.log("Hello World!") 
```

You should see “Hello World!” logged to the console, as shown in [Figure 1.1](#01_004.html_f1.1).

[![Chrome Console](bilderklein/klein01_001.png)](img-f1.1.html)

**Figure 1.1**     Chrome Console

Congratulations! You have just executed a line of JavaScript code in the browser. The <samp class="listingcharacter">console.log()</samp> statement is like the WRITE statement in ABAP, and is a great debugging tool when you are writing more complex logic and need to check that your variables are correct throughout your program. You will find more detail on debugging in [Section 14.2](#14_002.html_h14.2).

To run JavaScript on your webpage, it needs to be embedded using <samp class="listingcharacter"><script></samp> tags. These <samp class="listingcharacter"><script></samp> tags can hold actual JavaScript code like a simple function:

```
<script>function changeSomeText() {alert("Hi there!"}</script> 
```

You can also reference an external JavaScript file (e.g., app.js) that would hold all your JavaScript logic, which is a best practice, as follows:

```
<script src="app.js"></script> 
```

These <samp class="listingcharacter"><script></samp> tags can be placed within the <samp class="listingcharacter"><head></samp> or <samp class="listingcharacter"><body></samp> tags of your HTML page.

In our first example, we are going to add a JavaScript function directly in the <samp class="listingcharacter"><head></samp> tag of an HTML file. We are then going to trigger a standard HTML event <samp class="listingcharacter">onclick()</samp> (i.e., a button-click event) to run this function when we click the Try it button.

To begin, create a new folder, add a file called index.html, and copy the code snippet shown in [Listing 1.1](#01_004.html_l1.1) into it.

```
<!DOCTYPE html>
<html>
<head>
    <script>
        function changeSomeText() {
            document.getElementById("test").innerHTML = "Some new text appeared!";
        }
    </script>
</head>
<body>
    <div id="text-div">
        <h1>A normal everyday webpage</h1>
        <p id="test">Some old text.</p>
    </div>
    <div id="button-div">
        <button type="button" onclick="changeSomeText()">Try it</button>
    </div>
</body>
</html> 
```

**Listing 1.1**     JavaScript Function in the <head> Tag

Save your file and run your code, and you should see your HTML webpage displayed. Click the Try it button and, if all goes well, the text should change to Some new text appeared! as shown in [Figure 1.2](#01_004.html_f1.2). You have just created your first JavaScript function and triggered it from a standard HTML event.

Now, we are going to remove the <samp class="listingcharacter"><script></samp> tag (containing our JavaScript code) from our <samp class="listingcharacter"><head></samp> section and position it just before the closing <samp class="listingcharacter"></body></samp> tag of our HTML page, after our button. Refresh your HTML page and click the Try it button again. You should see the same text change as in [Listing 1.2](#01_004.html_l1.2).

[![JavaScript Function in the <head> Tag](bilderklein/klein01_002.png)](img-f1.2.html)

**Figure 1.2**     JavaScript Function in the <head> Tag

```
<!DOCTYPE html>
<html>
<body>
    <div id="text-div">
        <h1>A normal everyday webpage</h1>
        <p id="test">Some old text.</p>
    </div>
    <div id="button-div">
        <button type="button" onclick="changeSomeText()">Try it</button>
    </div>
    <script>
        function changeSomeText() {
            document.getElementById("test").innerHTML = "Some new text appeared!";
        }
    </script>
</body>
</html> 
```

**Listing 1.2**     JavaScript Function in the <body> Tag

The main difference between adding your script tags in the <samp class="listingcharacter"><body></samp> versus the <samp class="listingcharacter"><head></samp> section is that you improve page display speed; i.e., page elements load faster if the <samp class="listingcharacter"><script></samp> tag is at the bottom of the <samp class="listingcharacter"><body></samp> section, letting your page elements load first, followed by your <samp class="listingcharacter"><script></samp> tags, which can take longer to interpret.

Now, we are going to remove all our JavaScript from the HTML page and place it in an external file called app.js. The benefits of doing so include readability, maintainability, and reusability. You can reference the same JavaScript code from any HTML page and only need to write the code once, following the don’t repeat yourself (DRY) best practice.

Create a new folder and create the two files shown in [Listing 1.3](#01_004.html_l1.3) and [Listing 1.4](#01_004.html_l1.4) inside it, adding the relevant code to each one.

```
<!DOCTYPE html>
<html>
<head>
    <script src="app.js"></script>
</head>
<body>
    <div id="text-div">
        <h1>A normal everyday webpage</h1>
        <p id="test">Some old text.</p>
    </div>
    <div id="button-div">
        <button type="button" onclick="changeSomeText()">Try it</button>
    </div>
</body>
</html> 
```

**Listing 1.3**     index.html (Referencing External JavaScript File)

```
function changeSomeText() {
  document.getElementById("test").innerHTML = "Some new text appeared!";
} 
```

**Listing 1.4**     app.js (External JavaScript File)

Notice we have referenced the JavaScript file with just the filename <samp class="listingcharacter programmingelement">app.js</samp> because the file is in the same directory as our HTML file. This will not always be the case, so you will need to reference your external JavaScript file wherever it is in your app’s folder structure. See [https://www.w3schools.com/html/html_filepaths.asp](https://www.w3schools.com/html/html_filepaths.asp) for more information.

## 1.5    Executing JavaScript Code with Node.js

Node.js is an important JavaScript runtime built on Chrome’s V8 JavaScript engine that allows you to run your JavaScript code outside of a web browser, either on your local machine or an external server. Think of Node.js as just another place to run your JavaScript code without needing to create an entire webpage framework for the output.

To set up Node.js, download and install the version for your specific operating system (OS) from [https://nodejs.org/en/download/](https://nodejs.org/en/download/). Once installed, bring up the integrated terminal in VS Code via [Ctrl] + [`] and type “node”. Your window should change to look like [Figure 1.3](#01_005.html_f1.3). This means you have successfully installed Node.js and you can press [Ctrl] + [C] to exit to your normal terminal window.

[![node Command](bilderklein/klein01_003.png)](img-f1.3.html)

**Figure 1.3**     node Command

Now, we are going to run some JavaScript code using Node.js and log a string to the console. Create a JavaScript file called my-first-node-app.js, add the following code, and save the file:

```
console.log("Hello, this file was executed in Node!") 
```

We can then execute the file in the terminal section with the <samp class="listingcharacter">node</samp> command, followed by the location of the file relative to our current directory (for more help, see [https://nodejs.dev/learn/nodejs-file-paths](https://nodejs.dev/learn/nodejs-file-paths)). We are assuming we are already in the folder where the my-first-node-app.js file is located, so we run it like this:

```
node app.js 
```

You should then see the output <samp class="listingcharacter">Hello, this file was executed in Node!</samp> in the terminal window.

Congratulations! You used Node.js to run your JavaScript code on your local machine and viewed the output in a terminal window. We will follow this same process for many of the upcoming examples in this E-Bite, as it is a quick way to learn a concept and see the output.

## 1.6    Comments

Comments in your JavaScript code play the same helpful role that ABAP comments do. Just like in ABAP, JavaScript has single-line comments using <samp class="listingcharacter">//</samp>. For example:

```
// This is a comment 
```

You can use this to add comments about your code or comment a line of code out completely, as follows:

```
console.log("test123")    // This code writes text to the console
// Console.log("test456") 
```

You also have the option of multiline comments starting with <samp class="listingcharacter">/*</samp> and ending the comment with <samp class="listingcharacter">*/</samp>, as shown in [Listing 1.5](#01_006.html_l1.5).

```
/*
Some comments can
span multiple lines if
they need to
*/ 
```

**Listing 1.5**     Multiline Comment

In VS Code, for example, you can use the keyboard shortcut [Ctrl] + [/] to comment/uncomment selected lines of code.

# 2    Variables and Data Types

As with ABAP, JavaScript variables are there to store values that can be used throughout your program. As mentioned in section [Section 1](#01_001.html_h1), vanilla (standard) JavaScript is a loosely typed programming language, while ABAP in comparison is strongly typed. This means that you can define a variable in JavaScript with just a value and no type declaration, like an inline declaration in ABAP. However, in JavaScript, you can also declare a variable with no value and its type would remain undefined until you assigned a value to it. You can even reassign variables, so if a variable is of type <samp class="listingcharacter">number</samp>, you can change its type to <samp class="listingcharacter">string</samp> just by reassigning a new <samp class="listingcharacter">string</samp> type value to it.

This flexibility is great because it allows you to quickly build something, make changes, and execute ideas without adhering to the strict rules of something like the ABAP compiler. However, you must approach your variables with caution as you use them throughout your code; a function might rely on a variable being of a certain type, and since it’s easy for that variable type to change, that function is more likely to break for no apparent reason.

In this section, we’ll run through how to declare variables using old versus modern syntax, as well as what data types you can use. We’ll also look at accessing those variables in the context of global and local scope.

## 2.1    Variables

In ABAP, you use the <samp class="listingcharacter">DATA</samp> statement to define a variable, including its type and possibly a value as well, as follows:

```
DATA: lv_car TYPE string VALUE "Mercedes".
```

In JavaScript, you declare and assign values to your variables using the assignment operator (the <samp class="listingcharacter">=</samp> sign). You also have comparison operators that look remarkably similar; for example, <samp class="listingcharacter">==,</samp> which means “equal to.” We will look at comparison operators in more detail in [Section 3](#03_001.html_h3). Using the <samp class="listingcharacter">=</samp> sign in your variable declarations will look like [Listing 2.1](#02_001.html_l2.1).

```
var a = 10;        // Assign a numeric value to a
var b = 12;        // Assign a numeric value to b
var c = a + b;    // Assign the sum of a and b to c
console.log(a)
console.log(b)
console.log(c) 
```

**Listing 2.1**     Variable Declaration

The output is as follows:

```
10
12
22 
```

Notice how you can assign a number to a variable, as well as the sum of numbers or variables. Try renaming your variables to something more appropriate like our example in [Listing 2.2](#02_001.html_l2.2).

```
var applePrice = 10;            // Assign a numeric value to a
var bannanaPrice = 12;            // Assign a numeric value to a
var total = applePrice + bannanaPrice;    // Assign the sum of a and b to c
console.log(applePrice);
console.log(bananaPrice);
console.log(total); 
```

**Listing 2.2**     Renamed Variables

The output would be the same:

```
10
12
22 
```

All JavaScript variables must use unique names (known as identifiers), be as descriptive as possible, and follow these general rules:

*   Identifiers are case sensitive. <samp class="listingcharacter">A</samp> is different than <samp class="listingcharacter">a</samp>.

*   Identifiers must start with a letter.

*   Identifiers must not use reserved JavaScript keywords like <samp class="listingcharacter">var</samp> or <samp class="listingcharacter">function.</samp>

*   Identifiers can contain numbers, letters, dollar signs, and underscores.

*   Although not really a rule, you can decide if you want to use camel case or not.

Strings in JavaScript are assigned using quotation marks, while numbers are not. In the example in [Listing 2.3](#02_001.html_l2.3), notice how we can store either numbers or strings in our variables, as well as being able to chain variables together and log them to the console.

```
var height = 1.8;
var firstName = "John";
var lastName = "Smith";
console.log(firstName + " " + lastName + " is " + height + "m tall."); 
```

**Listing 2.3**     String and Number Variables

The output is as follows:

```
John Smith is 1.8m tall. 
```

Just like the previous example, try and use that same <samp class="listingcharacter">+</samp> sign to add some numbers together, but have one of the numbers in quotation marks like you would with a string, as shown in [Listing 2.4](#02_001.html_l2.4). The fact that the first number is in quotations means the rest of the numbers will be treated as strings, making the variable of type <samp class="listingcharacter">string</samp>.

```
var a = "9" + 1 + 7;
console.log(a);
console.log(typeof a) 
```

**Listing 2.4**     Variable Type Influence

The output is as follows:

```
917
string 
```

You can also declare empty variables (variables with no value), which in JavaScript means that this variable has a value of undefined, as shown in [Listing 2.5](#02_001.html_l2.5). In the next line, when you have assigned a value to the variable, if you try to log the variable to the console you will now see the new value.

```
var firstName;
console.log(firstName);
firstName = "John";
console.log(firstName); 
```

**Listing 2.5**     Undefined Variable

The output is as follows:

```
Undefined
John 
```

## 2.2    Data Types

In JavaScript, you have six data types known as “primitives.” A data type in JavaScript is considered primitive if it is not an object and has no methods that can be used to change it (the data types themselves are immutable).

This contrasts with JavaScript structural types, like arrays and objects, which are mutable and can be changed using object and array methods built into JavaScript itself (which we’ll discuss in more detail in [Section 5](#05_001.html_h5)). [Listing 2.6](#02_002.html_l2.6) shows a list of some of the data types (both primitive and structural) and how you could declare them.

```
var car // undefined (primitive type)
var weightKg = 10; // Number (primitive type
var dogsName = "Spot"; // String (primitive type)
var isTaskComplete = false; // Boolean (primitive type)
var numberArray = [1,2,3,4,5] // Object (structural type)
var object = {firstName:"John", 
lastName:"Smith"}; // Object (structural type) 
```

**Listing 2.6**     JavaScript Types

You can declare empty variables, where the value and type are both undefined, as follows:

```
var car; 
console.log(car); // undefined
console.log(typeof car); // undefined 
```

You can also declare a blank variable where the value is blank but the type is <samp class="listingcharacter">string</samp>, as follows:

```
var car = ""; 
console.log(car); // blank
console.log(typeof car); // string 
```

To make things more complex, you can take a variable like <samp class="listingcharacter">car</samp> and change its type in the same scope. This is why JavaScript is said to have dynamic types, and why you need to pay special attention to your variables. For example, [Listing 2.7](#02_002.html_l2.7) shows how we start with a <samp class="listingcharacter">car</samp> variable with type <samp class="listingcharacter">undefined</samp> and assign a string <samp class="listingcharacter">BMW</samp>, which changes the variable type to <samp class="listingcharacter">string</samp>. We then change the type twice more, from <samp class="listingcharacter">string</samp> to <samp class="listingcharacter">boolean</samp> and finally to <samp class="listingcharacter">number</samp>, just to assign a new value.

```
var car;
console.log(typeof car); // undefined
car = "BMW";
console.log(typeof car); // string
car = true;
console.log(typeof car); // boolean
car = 24;
console.log(typeof car); // number 
```

**Listing 2.7**     Dynamic Types

Another important concept regarding data types in JavaScript is how JavaScript evaluates expression from left to right, and the results can be different depending on what combination you use. This is in stark contrast to ABAP, where variables must be typed first and you will get a type error if you try to add a string to a number. In the following example, the number <samp class="listingcharacter">42</samp> will be treated as a string because the first part of the expression is the string <samp class="listingcharacter">"apple"</samp>:

```
var fruit = "apple" + 42;
console.log(fruit); // apple42 
```

If you then try adding two numbers together first, followed by the addition of a string as in the following example, you will find the numbers sum up correctly but <samp class="listingcharacter">"apple"</samp> is tagged on the end. So, it ran the calculation first and then continued to the addition of the string.

```
var fruit = 42 + 8 + "apple";
console.log(fruit); // 50apple 
```

As you have seen, JavaScript has a built-in operator called <samp class="listingcharacter">typeof</samp>, which you can use to check the data type of your variable. [Listing 2.8](#02_002.html_l2.8) shows how variable <samp class="listingcharacter">fruit1</samp> is type <samp class="listingcharacter">string</samp> when evaluating the expression from left to right, but following that same logic, variable <samp class="listingcharacter">fruit2</samp> is also type <samp class="listingcharacter">string</samp> even though we started out with the calculation on the left and added a string.

```
var fruit1 = "apple" + 42;
console.log(typeof fruit1); // string
var fruit2 = 42 + 8 + "apple";
console.log(typeof fruit2); // string 
```

**Listing 2.8**     typeof Operator

## 2.3    Scope of Global and Local Variables

In ABAP, we are familiar with the concept of global and local variables. In a simple report with a subroutine (<samp class="listingcharacter">FORM…ENDFORM</samp>), we can declare a global variable outside the subroutine, which both the program and subroutine can access. Consequently, we can also declare a local variable within the subroutine scope (inside the <samp class="listingcharacter">FORM…ENDFORM</samp>) where it is only accessible to the subroutine and not the rest of the program. In JavaScript, you also have global and local variables, but your program scope is also split into global scope and local scope. Variables declared in the global scope can be accessed from anywhere, but variables declared inside a function (local scope) can only be accessed inside their respective scopes (not from the global scope). Local scope can further be divided into function scope and block scope. We’ll walk through each in the following sections.

### Global Scope

In [Listing 2.9](#02_003.html_l2.9), we declare the variable <samp class="listingcharacter">car</samp> in the global scope and log this variable to the console within a function’s local scope. The function can access the <samp class="listingcharacter">car</samp> variable and log it to the console because the variable has been declared in the global scope.

```
var car = "BMW"; // Declared in the Global scope
function showCar() {
  console.log(car); // car is accessible in this function
}
showCar(); // BMW 
```

**Listing 2.9**     Global Scope

### Local Scope: Function Scope

Function scope is the scope inside the curly brackets <samp class="listingcharacter">{…}</samp> of a function (see [Section 4](#04_001.html_h4)); variables declared here are only accessible within the function itself. Following the same example in [Listing 2.10](#02_003.html_l2.10), we now declare our variable within the function scope. If we try to log the <samp class="listingcharacter">car</samp> variable outside the function, you will get a <samp class="listingcharacter">ReferenceError</samp>.

```
function showCar() {
  var car = "BMW"; // variable declared inside the function scope
  console.log(car); // car will be logged to the console
}
showCar(); // BMW
console.log(car); // ReferenceError: car2 is not defined 
```

**Listing 2.10**     Function Scope

### Local Scope: Block Scope

Block scope is the scope inside the <samp class="listingcharacter">{…}</samp> of JavaScript statements like <samp class="listingcharacter">switch</samp>, <samp class="listingcharacter">if</samp>, <samp class="listingcharacter">for</samp> loops, and <samp class="listingcharacter">while</samp> loops. The variables declared within the scope of these statements are also only accessible inside their respective statements’ block scope. However, this rule only applies to variables declared using modern JavaScript syntax, i.e., <samp class="listingcharacter">let</samp> and <samp class="listingcharacter">const</samp>. Watch how, in [Listing 2.11](#02_003.html_l2.11), a <samp class="listingcharacter">ReferenceError</samp> is triggered when trying to log <samp class="listingcharacter">car2</samp> to the console.

```
function test() {
  if (true) {
    var car1 = "BMW"; // old syntax - in function scope
    let car2 = "Audi"; // modern syntax - in block scope
  }
  console.log(car1); // BMW
  console.log(car2); // ReferenceError: car2 is not defined
}
test(); 
```

**Listing 2.11**     Block Scope inside the Function Scope

The reason why you cannot log <samp class="listingcharacter">car2</samp> is because it uses the modern syntax <samp class="listingcharacter">let</samp> and is locked into the block scope of the <samp class="listingcharacter">if</samp> statement, where even the function containing the <samp class="listingcharacter">if</samp> statement cannot access it. Since <samp class="listingcharacter">car1</samp> was declared using the older syntax, <samp class="listingcharacter">var</samp> can be accessed by the function, as it does not adhere to the <samp class="listingcharacter">if</samp> statement’s block scope.

## 2.4    Old Syntax versus Modern Syntax

Before ES6 (ECMAScript 2015), we only had the <samp class="listingcharacter">var</samp> keyword to declare variables in JavaScript. From ES6 onward, we have the <samp class="listingcharacter">let</samp> and <samp class="listingcharacter">const</samp> keywords, giving us more flexibility over <samp class="listingcharacter">var</samp>. These two new keywords are almost identical in nature, except <samp class="listingcharacter">let</samp> allows you to reassign a new value (like <samp class="listingcharacter">var</samp>), whereas <samp class="listingcharacter">const</samp> does not. They also allow us to declare variables that use block scope (see [Section 2.3](#02_003.html_h2.3)), whereas before ES6, we only had function scope and global scope.

We’ll walk through each keyword in the following sections.

### var

Variables using the <samp class="listingcharacter">var</samp> keyword can be changed as well as redeclared. This was one of the reasons <samp class="listingcharacter">let</samp> and <samp class="listingcharacter">const</samp> were introduced, giving us more control over our variables and making code less error prone, as we can now decide whether or not to restrict a variable. [Listing 2.12](#02_004.html_l2.12) shows how to both change and redeclare a variable using <samp class="listingcharacter">var</samp>. Here, the variable <samp class="listingcharacter">firstName</samp> is declared with value <samp class="listingcharacter">John</samp>, then its value is changed to <samp class="listingcharacter">Johnny</samp>, and finally redeclared as <samp class="listingcharacter">Fred</samp>.

```
var firstName = "John";
console.log(firstName); // John
firstName = "Johnny"; // Changing a variable
console.log(firstName); // Johnny
var firstName = "Fred"; // Delared a 2nd time
console.log(firstName); // Fred 
```

**Listing 2.12**     var Keyword

The output is as follows:

```
John
Johnny
Fred 
```

### let

Variables using the modern <samp class="listingcharacter">let</samp> keyword can be updated (reassigned) but not redeclared in the same scope, making it the popular successor to the <samp class="listingcharacter">var</samp> keyword. In [Listing 2.13](#02_004.html_l2.13), notice we can change the variable value when declared using <samp class="listingcharacter">let</samp>, changing <samp class="listingcharacter">John</samp> to <samp class="listingcharacter">Johnny</samp>.

```
let firstName = "John";
console.log(firstName); // John
firstName = "Johnny";
console.log(firstName); // Johnny 
```

**Listing 2.13**     let: Change Variable

In [Listing 2.14](#02_004.html_l2.14), if we try and reassign a variable using the <samp class="listingcharacter">let</samp> keyword in the same scope (e.g., redeclaring <samp class="listingcharacter">John</samp> as <samp class="listingcharacter">Fred</samp>), we get a <samp class="listingcharacter">SyntaxError</samp>.

```
let firstName = "John";
console.log(firstName);
let firstName = "Fred"; /* 
SyntaxError: Identifier 'firstName' has already been declared */ 
```

**Listing 2.14**     let: Reassign Variable

However, <samp class="listingcharacter">let</samp> variable identifiers can be declared again if they are outside of the same identifier’s block scope (see [Section 2.3](#02_003.html_h2.3)), as shown in [Listing 2.15](#02_004.html_l2.15).

```
let firstName = "John";
console.log(firstName); // John
if (true) {
  let firstName = "Johnny";
  console.log(firstName + " in block scope"); // Johnny in block scope
} 
```

**Listing 2.15**     let: Block Scope

### const

The <samp class="listingcharacter">const</samp> keyword is like <samp class="listingcharacter">let</samp> except you cannot change or reassign its value. The benefit of a variable that cannot be updated or redeclared is that it will not change throughout your program. In [Listing 2.16](#02_004.html_l2.16), we see immediately that if we try to change the variable <samp class="listingcharacter">firstName,</samp> we run into a <samp class="listingcharacter">TypeError</samp>.

```
const firstName = "John";
firstName = "Johnny"; // TypeError: Assignment to constant variable 
```

**Listing 2.16**     const: Changing Variable

In [Listing 2.17](#02_004.html_l2.17), we see that if we try to redeclare the <samp class="listingcharacter">firstName</samp> variable, we are presented with a <samp class="listingcharacter">SyntaxError</samp>.

```
const firstName = "John";
const firstName = "Johnny"; /* 
SyntaxError: Identifier 'firstName' has already been declared */ 
```

**Listing 2.17**     const: Redeclaring Variable

## 2.5    String and Number Methods

As in [Listing 2.8](#02_002.html_l2.8), where we use the <samp class="listingcharacter">typeof</samp> operator to find a variable type, you have built-in methods for strings and numbers that return information about the variable. When processing strings, you have a variety of methods to use. You can call methods that return the string length, as follows:

```
let alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
console.log(`String length is ${alphabet.length}`); // String length is 26 
```

You can call methods that give you the index of a word in a sentence, as follows:

```
let greetingStr = "Hello there friend!";
console.log(`There lies at index: ${greetingStr.indexOf("there")}`); /* There lies at index: 6 */ 
```

You also have methods that apply specifically to numbers that can, for example, reduce decimal points:

```
let num1 = 15.443256;
console.log(num1.toFixed(2)); // 15.44 
```

If required, you can convert your number to a string and vice versa, as shown in [Listing 2.18](#02_005.html_l2.18).

```
let num1 = 14.44;
console.log(typeof num1); // number
let numString = num1.toString(); // convert num1 to a string
console.log(typeof numString); //string
let num2 = Number(num1); // convert num1 back to a number
console.log(typeof num2); // number 
```

**Listing 2.18**     String and Number Methods

# 3    Operators and Loops

Now that we can declare variables in our code, we need to be able to work with those variables and use them in our program logic. In ABAP, most day-to-day requirements include arithmetic, value comparison, conditional statements, and loops to achieve a result. JavaScript also covers these areas, and the only real difference is the syntax. We’ll see these differences in action in the following sections.

## 3.1    Arithmetic Operators

As seen in [Section 2.1](#02_001.html_h2.1), you can do basic arithmetic in JavaScript such as summing two numbers or variables using the <samp class="listingcharacter">+</samp> operator, as shown in [Listing 3.1](#03_001.html_l3.1).

```
let a = 10; // Operand
let b = 15; // Operand
let c = a + b; // + is the operator that sums the numbers
console.log(c); // 25
let d = 10 + 15;
console.log(d); // 25 
```

**Listing 3.1**     Sum Operator

The previous arithmetic operation is split into the operator and operands. The operator is the <samp class="listingcharacter">+</samp> sign that sums the operands (<samp class="listingcharacter programmingelement">10</samp> and <samp class="listingcharacter programmingelement">15</samp>) to give you <samp class="listingcharacter programmingelement">25</samp>. You can also do the same with <samp class="listingcharacter">-</samp>, <samp class="listingcharacter">*</samp>, and <samp class="listingcharacter">/</samp> to subtract, multiply, and divide, respectively.

There is also the modulus operator <samp class="listingcharacter">%</samp>, which returns the remainder after a division calculation is performed, as shown in [Listing 3.2](#03_001.html_l3.2).

```
let a = 7;
let b = 2;
let c = a % b;
console.log(c); // 1 
```

**Listing 3.2**     Modulus (Remainder) Operator

Just like in mathematics, JavaScript arithmetic operations follow the same priority principle of multiplication (<samp class="listingcharacter">*)</samp> and division (<samp class="listingcharacter">/</samp>) being calculated first, taking priority over the <samp class="listingcharacter">+</samp> and <samp class="listingcharacter">-</samp> signs, which are calculated afterward. An example would be the following:

```
let sum = 10 + 5 * 3;
console.log(sum); // 25 
```

Using that same principle, you can also change this order by using <samp class="listingcharacter">( )</samp>, as follows:

```
let sum = (10 + 5) * 3;
console.log(sum); // 45 
```

In [Section 3.6](#03_006.html_h3.6), we will look at loops, where we can increment and decrement values using <samp class="listingcharacter">++</samp> or <samp class="listingcharacter">—-</samp> after a variable, as shown in [Listing 3.3](#03_001.html_l3.3).

```
let a = 10;
a++;
console.log(a); // 11
a--;
console.log(a); // 10 
```

**Listing 3.3**     Increment and Decrement Value

In [Section 2.1](#02_001.html_h2.1), we looked at the assignment operator (i.e., the <samp class="listingcharacter">=</samp> sign), which is used to assign a value to a variable. Now, we take it one step further in [Listing 3.4](#03_001.html_l3.4) with operators like <samp class="listingcharacter">+=</samp>, <samp class="listingcharacter">-=</samp>, <samp class="listingcharacter">*=</samp> and <samp class="listingcharacter">/=</samp>.

```
let a = 10;
let b = 2;
a += b;
console.log(a); // 12
a -= b;
console.log(a); // 10
a *= b;
console.log(a); // 20
a /= b;
console.log(a); // 10 
```

**Listing 3.4**     Arithmetic Assignment Operator

## 3.2    String Operators

String operators can be used to concatenate strings based on variables or hard-coded text to form longer strings. You saw this in [Listing 2.15](#02_004.html_l2.15), where we used the <samp class="listingcharacter">+</samp> operator to concatenate two strings. Another example is shown in [Listing 3.5](#03_002.html_l3.5), where three variables are concatenated with some hard-coded text and assigned to another variable, which we log to the console.

```
let firstName = "John";
let lastName = "Doe";
let age = 34;
let person = firstName + " " + lastName + " is " + age + " years old.";
console.log(person); // John Doe is 34 years old. 
```

**Listing 3.5**     String Concatenation Using +

You might find the variable concatenation in the previous example is long and convoluted. There is a more streamlined way to concatenate strings in JavaScript called template literals, like string templates in ABAP. They allow you to build your string between back quotes (<samp class="listingcharacter">’’</samp>), where spaces and other text are taken into consideration around variables referenced using <samp class="listingcharacter">${}</samp>. [Listing 3.6](#03_002.html_l3.6) shows how to reference the same three variables from [Listing 3.5](#03_002.html_l3.5), but arrange them in a more natural sentence-like structure instead of having to declare literal spaces between strings.

```
let firstName = "John";
let lastName = "Doe";
let age = 34;
let person = `${firstName} ${lastName} is ${age} years old.`;
console.log(person); // John Doe is 34 years old. 
```

**Listing 3.6**     Template Literals

## 3.3    Comparison Operators

ABAP comparison operators are similar in both syntax and function to JavaScript, allowing you to compare variables or values. In JavaScript, though, you evaluate the difference, and it can be either true or false depending on the result of the comparison, as shown in [Listing 3.7](#03_003.html_l3.7).

```
a = 20;
console.log(a != 21); // true
console.log(a < 20); // false
console.log(a <= 20); // true
console.log(a > 20); // false
console.log(a >= 20); // true 
```

**Listing 3.7**     Comparison Operators

The only real difference between ABAP and JavaScript are the equal to (<samp class="listingcharacter">=</samp>) and not equal to (<samp class="listingcharacter">!=</samp>) operators due to the dynamic typing of JavaScript. You need to extend your <samp class="listingcharacter">=</samp> or <samp class="listingcharacter">!=</samp> to include a comparison of the value and the type, as per [Table 3.1](#03_003.html_t3.1).

| Operator | Description |
| --- | --- |
| <samp class="listingcharacter">==</samp> | Only compares the actual value |
| <samp class="listingcharacter">===</samp> | Compares the value and the type |
| <samp class="listingcharacter">!=</samp> | Only compares the value |
| <samp class="listingcharacter">!==</samp> | Compares the value and the type |

**Table 3.1**     Comparison Operator Types

In [Listing 3.8](#03_003.html_l3.8), you see how if you compare variable <samp class="listingcharacter">b</samp>, which is <samp class="listingcharacter programmingelement">25</samp>, with a string <samp class="listingcharacter">25</samp> using the <samp class="listingcharacter">==</samp> operator, it will evaluate as <samp class="listingcharacter">true</samp> because it does not compare the type. When you use <samp class="listingcharacter">===</samp> with that same comparison, it evaluates as <samp class="listingcharacter">false</samp> because it takes the type into consideration (which does not match, i.e., <samp class="listingcharacter">number</samp> and <samp class="listingcharacter">string</samp>). The same principle applies for the <samp class="listingcharacter">!=</samp> operator as well.

```
b = 25;
console.log(b == 25); // true
console.log(b == 30); // false
console.log(b == "25"); // true because no type comparison
console.log(b === 25); // true
console.log(b === 30); // false
console.log(b === "25"); // false because of type comparison
console.log(b != 25); // false
console.log(b != 30); // true
console.log(b != "25"); // false because no type comparison
console.log(b !== 25); // false
console.log(b !== 30); // true
console.log(b !== "25"); // true because of type comparison 
```

**Listing 3.8**     Comparison Operator with Types and Values

## 3.4    Logical Operators

JavaScript also has the logical operators and (<samp class="listingcharacter">&&</samp>), or (<samp class="listingcharacter">||</samp>), and not (<samp class="listingcharacter">!</samp>), which can, for example, be used in conjunction with the comparison operators. In [Listing 3.9](#03_004.html_l3.9), we compare variables <samp class="listingcharacter">a</samp> and <samp class="listingcharacter">b</samp> with hard-coded numbers inside brackets. We use <samp class="listingcharacter">&&</samp> to say comparison 1 and comparison 2 must evaluate to <samp class="listingcharacter">true</samp> to be completely true. We use <samp class="listingcharacter">||</samp> where we only need one or the other to evaluate to <samp class="listingcharacter">true</samp> to be completely true. Finally, we use <samp class="listingcharacter">!</samp> when, if the comparison is not <samp class="listingcharacter">true</samp>, it evaluates to <samp class="listingcharacter">true</samp>.

```
let a = 10;
let b = 20;
console.log(a === 10 && b === 20);  // true
console.log(a === 20 && b === 10);  // false
console.log(a === 10 && b === 11);  // false
console.log(a === 10 || b === 20);  // true
console.log(a === 10 || b === 21);  // true
console.log(!(a === b));            // true 
```

**Listing 3.9**     Logical Operators

## 3.5    Conditional Operators

As in ABAP, you have the traditional conditional statements <samp class="listingcharacter">if</samp>, <samp class="listingcharacter">else</samp>, and <samp class="listingcharacter">else if</samp>. <samp class="listingcharacter">if</samp> and <samp class="listingcharacter">else if</samp> both run a comparison between two values and execute some code if that condition is met. The <samp class="listingcharacter">if</samp> statement is followed by the condition to evaluate in brackets and, if the condition is met (i.e., true), then the code in the curly brackets is executed. The <samp class="listingcharacter">else if</samp> statement works the same way and is triggered if the first <samp class="listingcharacter">if</samp> condition is not met and will check another condition. The <samp class="listingcharacter">else</samp> statement is inserted at the end of your conditional logic, either after <samp class="listingcharacter">if</samp> or <samp class="listingcharacter">else if</samp> depending on your scenario, and is triggered if all other statements before it are false.

If you run the code in [Listing 3.10](#03_005.html_l3.10) as is, the output “100 is definitely 100 or less” should result. If you change the value of variable <samp class="listingcharacter">a</samp> to 110, you should see “110 is simply not less than 100” as output. Finally, if you change variable <samp class="listingcharacter">a</samp> to a string like <samp class="listingcharacter">hello</samp>, then your <samp class="listingcharacter">else</samp> statement should be triggered and “hello is just not a number” should be logged to the console.

```
let a = 100;
if (a <= 100) {
  console.log(`${a} is definitely 100 or less`);
} else if (a > 100) {
  console.log(`${a} is simply not less than 100`);
} else {
  console.log(`${a} is just not a number`);
} 
```

**Listing 3.10**     Conditional Operators: if Statement

In ABAP, we can compress conditional logic like that seen in [Listing 3.10](#03_005.html_l3.10) into one concise line of code using the <samp class="listingcharacter">COND</samp> statement, as follows:

```
DATA(lv_num) = COND #( WHEN iv_num IS INITIAL THEN 0 ELSE iv_num ).
```

In JavaScript, we can replicate the <samp class="listingcharacter">COND</samp> statement using the ternary operator. It takes the first four lines of comparison logic we wrote in [Listing 3.10](#03_005.html_l3.10) (the <samp class="listingcharacter">if</samp> and <samp class="listingcharacter">else if</samp> part) and immediately makes the code more concise. This can be seen in [Listing 3.11](#03_005.html_l3.11), where we assign our <samp class="listingcharacter">output</samp> variable the result of the ternary logic. If <samp class="listingcharacter">a <= 100</samp> is true, return the value just after the <samp class="listingcharacter">?</samp>. If it is false, then return the value just after the <samp class="listingcharacter">:</samp>.

```
let a = 110;
let output =
  a <= 100
    ? `${a} is definitely less than 100`
    : `${a} is simply not less than 100`;
console.log(output); 
```

**Listing 3.11**     Ternary Operator

The ternary operator can also be chained, allowing you to completely encompass the logic from [Listing 3.10](#03_005.html_l3.10), as shown in [Listing 3.12](#03_005.html_l3.12).

```
let a = "hello";
let output =
  a <= 100
    ? `${a} is definitely less than 100`
    : a >= 100
    ? `${a} is simply not less than 100`
    : `${a} is just not a number`;
console.log(output); 
```

**Listing 3.12**     Ternary Operator Chained

The code in [Listing 3.12](#03_005.html_l3.12) does the same thing as [Listing 3.10](#03_005.html_l3.10), but the code is far more concise, although the syntax can be hard to read at first. To help with the syntax, remember anything written after the <samp class="listingcharacter">?</samp> is what runs if the condition evaluates to <samp class="listingcharacter">true</samp> and everything after the<samp class="listingcharacter">:</samp> runs if the previous statement evaluates to <samp class="listingcharacter">false</samp>, even if that is another comparison statement.

Another important conditional operator in ABAP is the <samp class="listingcharacter">SWITCH</samp> statement, which is a great way to avoid a large number of nested <samp class="listingcharacter">IF</samp> statements. The <samp class="listingcharacter">switch</samp> statement in JavaScript is again like its ABAP counterpart and, aside from a few syntactical differences, performs much the same way. You create a <samp class="listingcharacter">switch</samp> statement and add your expression to be evaluated in brackets, followed by your <samp class="listingcharacter">case</samp> statements with the code to be executed if the case condition is met. If a condition is met, you add a <samp class="listingcharacter">break</samp> statement to exit the <samp class="listingcharacter">switch</samp> statement after your code is executed. The <samp class="listingcharacter">default</samp> statement is added at the end to handle things if none of the <samp class="listingcharacter">case</samp> statements are met. [Listing 3.13](#03_005.html_l3.13) shows an example where we declare a <samp class="listingcharacter">company</samp> variable and use a <samp class="listingcharacter">switch</samp> statement to evaluate if its value matches any of the companies in the <samp class="listingcharacter">case</samp> statements. In this scenario, it matches the <samp class="listingcharacter">case "SAP":</samp> statement, so the <samp class="listingcharacter">"Something about SAP"</samp> text is logged to the console.

```
let company = "SAP";
switch (company) {
  case "Microsoft":
    console.log("Something about Microsoft");
    break;
  case "Google":
    console.log("Something about Google");
    break;
  case "SAP":
    console.log("Something about SAP");
    break;
  default:
    console.log("No company here :(");
} 
```

**Listing 3.13**     switch Statement

Run the code in [Listing 3.13](#03_005.html_l3.13) as is, and your output should be <samp class="listingcharacter">"Something about SAP"</samp> because that is the <samp class="listingcharacter">case</samp> condition matching our <samp class="listingcharacter">company</samp> variable. Try changing the <samp class="listingcharacter">company</samp> variable and trigger each of the other <samp class="listingcharacter">case</samp> statements, as well as the default.

## 3.6    Loops

In ABAP, we have unconditional loops using <samp class="listingcharacter">DO</samp>, conditional loops using <samp class="listingcharacter">WHILE</samp>, and the <samp class="listingcharacter">LOOP</samp> statement to loop through internal tables. In JavaScript, we have <samp class="listingcharacter">do</samp>, <samp class="listingcharacter">do…while</samp>, and <samp class="listingcharacter">while</samp> loops as in ABAP, but with the addition of a <samp class="listingcharacter">for</samp> loop instead of the ABAP <samp class="listingcharacter">LOOP</samp> statement. We’ll walk through each in the following sections.

### For Loop

The most common loop you will learn in JavaScript is the <samp class="listingcharacter">for</samp> loop, which might look a bit strange compared to <samp class="listingcharacter">LOOP AT</samp> in ABAP. The loop is controlled by the logic in the brackets and breaks down as follows:

*   <samp class="listingcharacter">let count = 0</samp>: Creating a variable to be used in the iteration.

*   <samp class="listingcharacter">count <= 10</samp>: Looping until the <samp class="listingcharacter">count</samp> variable hits ten or less.

*   <samp class="listingcharacter">count++</samp>: Tells the variable to add one to itself on every iteration. (<samp class="listingcharacter">count--</samp> counts down).

The complete syntax would look like we see in [Listing 3.14](#03_006.html_l3.14).

```
for (let count = 0; count <= 10; count++) {
  console.log(count);
} 
```

**Listing 3.14**     for Loop Syntax

The output should be a count from <samp class="listingcharacter">0...10</samp>, where we logged the <samp class="listingcharacter">count</samp> variable to the console so you can see how the iteration works. You can also count down from 10 by setting <samp class="listingcharacter">count</samp> to <samp class="listingcharacter programmingelement">10</samp>, the iteration to stop when <samp class="listingcharacter">count >= 0</samp>, and the count to increment down with <samp class="listingcharacter">count--</samp>.

### Do While

The <samp class="listingcharacter">do while</samp> loop works in a similar way to the <samp class="listingcharacter">for</samp> loop, but is arranged slightly differently. You execute your logic using the <samp class="listingcharacter">do</samp> statement and control your iterations using the <samp class="listingcharacter">while</samp> statement at the end, as shown in [Listing 3.15](#03_006.html_l3.15).

```
let count = 0;
do {
  console.log(count);
  count += 1;
} while (count <= 10); 
```

**Listing 3.15**     do while Statement

The output should mirror the <samp class="listingcharacter">for</samp> loop in [Listing 3.14](#03_006.html_l3.14), a count from <samp class="listingcharacter">0…10</samp>. Again, you can try reversing the count and logging the increments from <samp class="listingcharacter">10…0</samp> by changing the <samp class="listingcharacter">count</samp> variable to <samp class="listingcharacter programmingelement">10</samp>, swapping out the <samp class="listingcharacter">+=</samp> for <samp class="listingcharacter">-=</samp> and changing the <samp class="listingcharacter">while</samp> condition to <samp class="listingcharacter">(count >= 0)</samp>.

### While

The <samp class="listingcharacter">while</samp> statement works like the <samp class="listingcharacter">do while</samp> statement in [Listing 3.15](#03_006.html_l3.15), except you start with your <samp class="listingcharacter">while</samp> statement and execute your code (including the iteration control) below the statement itself, as shown in [Listing 3.16](#03_006.html_l3.16).

```
let count = 0;
while (count <= 10) {
  console.log(count);
  count++;
} 
```

**Listing 3.16**     while Statement

You should see the same count from <samp class="listingcharacter">0…10</samp> as with the other two loops’ output to the console. Try the count backward here as well by making the same changes as before: set <samp class="listingcharacter">count</samp> to <samp class="listingcharacter programmingelement">10</samp>, iterate down with <samp class="listingcharacter">count--</samp>, and stop the loop with <samp class="listingcharacter">count >= 0</samp>.

# 4    Functions

In ABAP, we are no stranger to functions or function modules with importing and exporting parameters, and in JavaScript, you have functions at your disposal as well. The syntax is a bit simpler in JavaScript, where a function can be declared in as little as one or two lines. They will become your main tool to encapsulate reusable logic in your application.

In the following sections, we’ll look at how to define a function with importing and returning parameters, including the new arrow function syntax. We will also look at variables within the global scope and address an important concept called closures.

## 4.1    Function Definition

JavaScript functions are defined using the <samp class="listingcharacter">function</samp> statement followed by the name of the function, the brackets <samp class="listingcharacter">()</samp> (for parameter definition), and the logic to be executed within the <samp class="listingcharacter">{}</samp>. [Listing 4.1](#04_001.html_l4.1) shows a simple function that logs a message to the console when executed.

```
// Defining the function
function mySimpleFunction() {
  console.log(`My simple function was invoked :)`);
}
mySimpleFunction(); // My simple function was invoked :) 
```

**Listing 4.1**     Standard Function

The output should be <samp class="listingcharacter">"My simple function was invoked :)"</samp> logged to the console. Try running this function yourself and see how easy it is to encapsulate logic in JavaScript.

As of ES6, you can also define JavaScript functions using the arrow function syntax as follows:

```
(params) => {logic} 
```

It looks quite different than the standard function definition in [Listing 4.1](#04_001.html_l4.1), but is a much more streamlined way to define functions. The syntax involves declaring a <samp class="listingcharacter">const</samp> variable (or function name) and assigning the function to it with the <samp class="listingcharacter">=</samp> sign. The function parameters are then defined with your brackets <samp class="listingcharacter">(params)</samp> followed by the arrow or <samp class="listingcharacter">=></samp> and then the <samp class="listingcharacter">{}</samp> that hold your logic to be executed, as shown in [Listing 4.2](#04_001.html_l4.2).

```
const mySimpleFunction = () => {
  console.log("My arrow function () => {} was invoked");
};
mySimpleFunction(); // My arrow function () => {} was invoked 
```

**Listing 4.2**     Arrow Function

The function logs text to the console when calling the newly created <samp class="listingcharacter">mySimpleFunction()</samp> function variable.

###### Important Note

Arrow functions are great, and you will use them a lot, but don’t discount classic functions just yet. Arrow functions are great for more simplistic logic, while classic functions still offer many complex features that arrow functions don’t, such as redefinition of the <samp class="listingcharacter">this</samp> keyword. The differences are beyond the scope of this E-Bite, but well worth your time to read about. In this E-Bite, we will use a combination of both function expressions, and we recommend you choose your syntax based on your scenario.

## 4.2    Parameters and the Return Statement

A JavaScript function can also have importing parameters, which can be used inside the function itself. You define your parameters in the brackets <samp class="listingcharacter">(param1)</samp> and inside your logic, you reference the parameter name <samp class="listingcharacter">param1</samp> and do something like log it to the console, as shown in [Listing 4.3](#04_002.html_l4.3).

```
const mySimpleFunction = (param1) => {
  if (param1) {
    console.log(param1);
  } else {
    console.log(`param1 is ${typeof param1}`);
  }
};
mySimpleFunction("Hello World!"); 
```

**Listing 4.3**     Function Parameters

In this example, we declare our function with an importing parameter <samp class="listingcharacter">param1</samp> and call that function, passing in the importing parameter <samp class="listingcharacter">"Hello World!"</samp>, which the function then logs to the console. Notice we have structured our logic inside an <samp class="listingcharacter">if</samp> statement. This is to highlight the dynamic typing of that <samp class="listingcharacter">param1</samp> parameter. If you call the function with no variable, a string will be logged to the console telling you <samp class="listingcharacter">param1</samp> is undefined.

As well as executing logic inside your function, you can also return variables to the caller using the <samp class="listingcharacter">return</samp> statement. [Listing 4.4](#04_002.html_l4.4) contains a function that calculates the sum of two parameters, a check to make sure the parameters are type <samp class="listingcharacter">number</samp>, and if so, returns the summed value. Notice how you can declare multiple parameters separated by a comma.

```
const mySumFunction = (param1, param2) => {
  if (typeof param1 === "number" && typeof param2 === "number") {
    return param1 + param2;
  } else {
    return "At least one of the parameters is not a number!";
  }
};
let sum = mySumFunction(100, 150);
console.log(sum); // 250 
```

**Listing 4.4**     Function Return Statement

Initially, we call this function with two number-type parameters (<samp class="listingcharacter programmingelement">100</samp>, <samp class="listingcharacter programmingelement">150</samp>) and we get a summed value of <samp class="listingcharacter programmingelement">250</samp> assigned to the variable <samp class="listingcharacter">sum</samp>, which is then logged to the console. The <samp class="listingcharacter">if</samp> statement checks that both importing parameters are indeed of type <samp class="listingcharacter">number</samp>, and if not, an appropriate message is returned. Try changing one of the parameters to a string, or only enter one of the two parameters for <samp class="listingcharacter">mySumFunction(100)</samp>, and your variable should be assigned a string that says, <samp class="listingcharacter">"At least one of the parameters is not a number!"</samp>, which is then logged to the console.

## 4.3    Global Scope and Closures

We looked at the function scope in [Section 2.3](#02_003.html_h2.3), which explained that we can access variables declared in the global scope (i.e., outside of the function) but variables declared inside a function are considered “private” to that function and are not accessible to the function caller.

However, the downside is global variables in JavaScript are accessible to any other function in the global scope, which can wreak havoc in your application. What we want is a way to create a global variable but lock down its scope so that only a certain function can access it. This is the same concept in ABAP classes with their <samp class="listingcharacter">PRIVATE SECTION</samp> declaration. Only the methods in that class can access those private variables, but those variables are declared outside the class methods themselves.

In JavaScript, this problem is solved using a concept called closures, which is essentially a function that wraps another function in a function scope so that when you call the parent function (which is like a wrapper), you create a parent function scope. Inside that parent function scope, you have another function that can access any variables within the parent wrapper.

Let’s walk through a simple example where we create a flexible calculator, as shown in [Listing 4.5](#04_003.html_l4.5). First, you define the <samp class="listingcharacter">flexiSumCalculator</samp> parent function as the scope (wrapper), with a parameter <samp class="listingcharacter">param1</samp> that is assigned to the private variable <samp class="listingcharacter">valueToAdd</samp>. Inside this wrapper, you define a return function <samp class="listingcharacter">calculator</samp> that returns the sum of the <samp class="listingcharacter">valueToAdd</samp> variable and the child function <samp class="listingcharacter">param2</samp> parameter.

So, you create a version of the calculator, e.g., <samp class="listingcharacter">flexiSumCalculator5</samp>, which will add 5 to any value you pass in. You do this by creating a <samp class="listingcharacter">const</samp> function variable of the <samp class="listingcharacter">flexiSumCalculator</samp> parent function. This function variable takes and stores <samp class="listingcharacter">param1</samp> as a global private variable for that version of the calculator, like an instance of a class in ABAP. You can then invoke that new <samp class="listingcharacter">flexiSumCalculator5()</samp> function and pass any value you want (as <samp class="listingcharacter">param2</samp>), and it will return <samp class="listingcharacter">param2</samp> plus 5.

```
// Parent function "scope" wrapper
const flexiSumCalculator = (param1) => {
  let valueToAdd = param1; // our new "private" variable
  // Function that returns the calculation
  return (caluclator = (param2) => {
    return (param2 += valueToAdd);
  });
};
const flexiSumCalculator5 = flexiSumCalculator(5); /* 
Invoking the new version with param2 */
console.log(flexiSumCalculator5(1)); // 6
console.log(flexiSumCalculator5(2)); // 7
console.log(flexiSumCalculator5(3)); // 8 
```

**Listing 4.5**     JavaScript Closures

So, when you create a version or instance of the calculator, you use <samp class="listingcharacter">param1</samp> to determine what the private variable will be. When you call this new function variable, you pass in a parameter, which is <samp class="listingcharacter">param2</samp>. The function variable can now be reused safely so when you run the above code, you get <samp class="listingcharacter programmingelement">6</samp>, <samp class="listingcharacter programmingelement">7</samp>, and <samp class="listingcharacter programmingelement">8</samp> logged to the console using the same function variable <samp class="listingcharacter">flexiSumCalculator5()</samp>.

# 5    Data Structures

In ABAP, we have the internal table and work areas that we use to read and manipulate data from our database tables before committing those changes to the database. In JavaScript, we have two key data structures that take the place of the ABAP internal table and work area: arrays and objects. There are many other data structures in JavaScript, but arrays, objects, and a combination of the two are the best starting point. These two data types are mutable (i.e., they can be changed), and so they have a set of standard JavaScript methods you can use to read and manipulate them. We’ll discuss both in the following sections.

## 5.1    Arrays and Array Methods

JavaScript arrays are like internal tables in ABAP and are designed to let you hold a table or list of values accessible through a single variable. The arrays themselves are defined by <samp class="listingcharacter">[…]</samp>, which contain a comma-separated list of items. In [Listing 5.1](#05_001.html_l5.1), we declare two arrays as variables, <samp class="listingcharacter">petArray</samp> and <samp class="listingcharacter">numberArray</samp>, respectively.

```
let petArray = ["Dog", "Cat", "Bird", "Fish", "Reptile"];
let numberArray = [1, 32, 63, 4, 75, 76, 347, 84];
console.log(petArray); // [ 'Dog', 'Cat', 'Bird', 'Fish', 'Reptile' ]
console.log(numberArray); // [ 1, 32, 63, 4, 75, 76, 347, 84 ] 
```

**Listing 5.1**     Simple Array Declaration

As in ABAP, each item in a JavaScript array has an assigned index (starting at 0) that you can use to access that value (i.e., read the array) using square bracket notation (<samp class="listingcharacter">[0]</samp>). In [Listing 5.2](#05_001.html_l5.2), we log a certain array value at a particular index (<samp class="listingcharacter">[0]</samp>and <samp class="listingcharacter">[1]</samp>, respectively) to the console from each of our arrays.

```
let petArray = ["Dog", "Cat", "Bird", "Fish", "Reptile"];
let numberArray = [1, 32, 63, 4, 75, 76, 347, 84];
console.log(petArray[0]); // Dog
console.log(numberArray[1]); // 32 
```

**Listing 5.2**     Find Values of an Array by Index

There are also a set of standard JavaScript methods that allow you to access and manipulate your arrays. Some of these methods accept parameters, while others also let you apply function logic and pass data like a value or a Boolean. There are many methods to choose from, so we will focus on a select few to give you an idea of how they work.

Let’s start off with sorting our array. In [Listing 5.3](#05_001.html_l5.3), we sort our <samp class="listingcharacter">petArray</samp> string values in alphabetical order using the <samp class="listingcharacter">sort()</samp> method, then call the <samp class="listingcharacter">reverse()</samp> method to reverse the order.

```
let petArray = ["Dog", "Cat", "Bird", "Fish", "Reptile"];
petArray.sort();
console.log(petArray);  // [ 'Bird', 'Cat', 'Dog', 'Fish', 'Reptile' ]
petArray.reverse();
console.log(petArray);  // [ 'Reptile', 'Fish', 'Dog', 'Cat', 'Bird' ] 
```

**Listing 5.3**     Arrays: Alphabetical Sort

Sorting numerically, on the other hand, is a more complex and uses the <samp class="listingcharacter">sort()</samp> method’s optional parameters and built-in sorting algorithm, as we see in [Listing 5.4](#05_001.html_l5.4).

```
let numberArray = [1, 32, 63, 4, 75, 76, 347, 84];
numberArray.sort((a, b) => a - b); // Sort ascending
console.log(numberArray); // [1, 4, 32,  63, 75, 76, 84, 347]
numberArray.sort((a, b) => b - a); // Sort descending
console.log(numberArray); // [ 347, 84, 76, 75, 63, 32, 4, 1] 
```

**Listing 5.4**     Arrays: Numeric Sort

We are calling the same <samp class="listingcharacter">sort()</samp> method from [Listing 5.3](#05_001.html_l5.3), except we’re sorting numbers this time, and for that, we need to use the built-in sorting algorithm, which takes two optional parameters (<samp class="listingcharacter">a</samp> = current value and <samp class="listingcharacter">b</samp> = next value in the array). The algorithm then iterates through the array values and calculates <samp class="listingcharacter">a – b</samp>. If the output is negative, it means <samp class="listingcharacter">b</samp> is greater than <samp class="listingcharacter">a</samp> and needs to stay in its current position, as the order is ascending. If the output is positive, it means <samp class="listingcharacter">b</samp> is smaller than <samp class="listingcharacter">a</samp> and therefore <samp class="listingcharacter">b</samp> needs to shift in front of <samp class="listingcharacter">a</samp>. This logic continues through the whole array until the correct ascending order is set. If you want the numbers to be in descending order, switch the logic around and instead run <samp class="listingcharacter">b – a</samp>.

After sorting your array, you might not remember the exact index of a particular value. JavaScript has a handy <samp class="listingcharacter">indexOf()</samp> method to find the index of a particular value in an array, as shown in [Listing 5.5](#05_001.html_l5.5) for the index of <samp class="listingcharacter">Fish</samp>.

```
let petArray = ["Bird", "Cat", "Dog", "Fish", "Reptile"];
let index = petArray.indexOf("Fish");
console.log(index); // 3 
```

**Listing 5.5**     indexOf()

Another useful method in JavaScript is the <samp class="listingcharacter">some()</samp> method. This allows you to scan an array to see if a certain value exists. In [Listing 5.6](#05_001.html_l5.6), we scan our <samp class="listingcharacter">petArray</samp> to see if the value <samp class="listingcharacter">Reptile</samp> exists. To do that, we create a new variable <samp class="listingcharacter">reptileExists</samp> and assign it to the return value from our <samp class="listingcharacter">petArray.some()</samp> method call. In that call, we pass in a parameter <samp class="listingcharacter">(element),</samp> which each value of the array is iterated through and passed to, like the <samp class="listingcharacter">sort()</samp> method discussed previously. We add a simple line of logic, <samp class="listingcharacter">element === "Reptile",</samp> inside the function. The function then iterates through all the array values until either all values don’t match (return <samp class="listingcharacter">false</samp>) or an item does match (return <samp class="listingcharacter">true</samp>), which we then log to the console.

```
let petArray = ["Bird", "Cat", "Dog", "Fish", "Reptile"];
let reptileExists = petArray.some((element) => element === "Reptile");
console.log(reptileExists); // true 
```

**Listing 5.6**     Array Method: some()

When changing data in our array, the first key point we need to understand is the array’s length, or how many items are we dealing with. In [Listing 5.7](#05_001.html_l5.7), we call <samp class="listingcharacter">petArray.length</samp>, which will return the length of the array (<samp class="listingcharacter">5</samp>, in our example).

```
let petArray = ["Dog", "Cat", "Bird", "Fish", "Reptile"];
console.log(petArray.length); // 5 
```

**Listing 5.7**     array.length Method

Now that we know how many items are in our array, let’s append an item to it using the <samp class="listingcharacter">push()</samp> method. In [Listing 5.8](#05_001.html_l5.8), we call <samp class="listingcharacter">petArray.push("Lion")</samp> and the string <samp class="listingcharacter">Lion</samp> will be added as the sixth item to our array at index <samp class="listingcharacter programmingelement">5</samp>. We use <samp class="listingcharacter">console.table()</samp> to log our array to the console in a tabular format, as well as log the array length before and after adding <samp class="listingcharacter">Lion</samp>.

```
let petArray = ["Dog", "Cat", "Bird", "Fish", "Reptile"];
console.log(petArray.length); // 5
petArray.push("Lion");
console.table(petArray);
console.log(petArray.length); // 6 
```

**Listing 5.8**     array.push Method

Let’s try to insert an item at the beginning of our array using the flexible <samp class="listingcharacter">splice()</samp> method. The <samp class="listingcharacter">splice()</samp> method syntax includes a few parameters and looks like [Listing 5.9](#05_001.html_l5.9).

```
myArray.splice(
"index where item is to be added", 
"how many items should be removed, can be 0 or none)", 
"the item(s) to be added"
). 
```

**Listing 5.9**     splice() Method Syntax

In [Listing 5.10](#05_001.html_l5.10), we apply this method to our <samp class="listingcharacter">petArray</samp> and add a <samp class="listingcharacter">Lion</samp> to the beginning of the array at index <samp class="listingcharacter programmingelement">0</samp>.

```
let petArray = ["Dog", "Cat", "Bird", "Fish", "Reptile"];
petArray.splice(0, 0, "Lion");
console.table(petArray); /* 
["Lion", "Dog", "Cat", "Bird", "Fish",// "Reptile"]; */ 
```

**Listing 5.10**     splice() Method: Add Item to an Array

The flexibility of the <samp class="listingcharacter">splice()</samp> method means you can either replace one item with another or remove it entirely. In [Listing 5.11](#05_001.html_l5.11), we remove <samp class="listingcharacter">Lion</samp> from our <samp class="listingcharacter">petArray</samp> because it is not really a suitable pet. After that, we remove <samp class="listingcharacter">Dog</samp> and replace it with two new items, <samp class="listingcharacter">Small Dog</samp> and <samp class="listingcharacter">Big Dog</samp>.

```
let petArray = ["Lion", "Dog", "Cat", "Bird", "Fish", "Reptile"];
petArray.splice(0, 1);
console.table(petArray); // ["Dog", "Cat", "Bird", "Fish", "Reptile"];
petArray.splice(0, 1, "Small Dog", "Big Dog");
console.table(petArray); /* 
["Small Dog", "Big Dog", "Cat", "Bird",// "Fish","Reptile"]; */ 
```

**Listing 5.11**     Array: splice() Method: Delete and Replace Items

###### Important Note

Notice that when we call <samp class="listingcharacter">splice()</samp> the second time, we pass in the same index (index <samp class="listingcharacter programmingelement">0</samp>) as the first <samp class="listingcharacter">splice(),</samp> even though <samp class="listingcharacter">Dog</samp> is at index <samp class="listingcharacter programmingelement">1</samp>. This is because when we execute the first <samp class="listingcharacter">splice()</samp> and remove <samp class="listingcharacter">Lion</samp> at index <samp class="listingcharacter programmingelement">0</samp>, the whole array updates and shifts <samp class="listingcharacter">Dog</samp> to where <samp class="listingcharacter">Lion</samp> was. This data mutation is something you should approach with caution. Data mutation is a critical concept in JavaScript due to its dynamic nature; the less things change in your logic, the less there is to keep track of or potentially break.

## 5.2    Objects and Object Methods

JavaScript objects are like structures in ABAP in that they are used to store more detailed information. They are made up of <samp class="listingcharacter">name:value</samp> pairs separated by a comma and held within <samp class="listingcharacter">{}</samp>. Think of a car; normally, you do not just have one property such as the <samp class="listingcharacter">make</samp>, but rather the <samp class="listingcharacter">make</samp>, <samp class="listingcharacter">model</samp>, <samp class="listingcharacter">topSpeed,</samp> and so on as follows:

```
let car = { make: "Mercedes", model: "S Class", topSpeed: 320 }; 
```

JavaScript arrays are like ABAP internal tables, and JavaScript objects are like work areas/structures that make up the records of an internal table. In [Listing 5.12](#05_002.html_l5.12), we take our car example further and create an array of different car objects and log that array of objects to the console. In [Listing 5.12](#05_002.html_l5.12), we see a table output with Mercedes, BMW, and Audi cars with some of their specs. Then, we log the <samp class="listingcharacter">car</samp> object at index <samp class="listingcharacter programmingelement">1</samp> using <samp class="listingcharacter">carArray[1].make</samp>.

```
let carArray = [
  {
    make: "Mercedes",
    model: "A Class AMG",
    colour: "Black",
    topSpeed: 168,
  },
  {
    make: "BMW",
    model: "M Series",
    colour: "White",
    topSpeed: 150,
  },
  {
    make: "Audi",
    model: "S4",
    colour: "Blue",
    topSpeed: 173,
  },
];
console.table(carArray);
console.log(carArray[1].make); // BMW 
```

**Listing 5.12**     Array of JavaScript Objects

# 6    JSON

JavaScript Object Notation (JSON) is an open-standard file format and not the same as a JavaScript object, although they might look similar. The purpose of JSON is to allow data to be sent back and forth as simple text between two points (e.g., a server and your app) that JavaScript, and most other programming languages including ABAP, can read and interpret. JavaScript has methods to convert JSON data to a JavaScript object and a JavaScript object into JSON data to be sent to a server.

Copy and paste the widely used OData test service ([http://s-prs.co/v535906](http://s-prs.co/v535906)) called Northwind into your browser, and you should see a JSON format response returned in the browser window, as shown in [Figure 6.1](#06_001.html_f6.1).

[![JSON Response](bilderklein/klein06_001.png)](img-f6.1.html)

**Figure 6.1**     JSON Response

In the following sections, we’ll walk through JSON syntax and methods, and discuss how it works with OData and SAPUI5.

## 6.1    JSON Syntax

JSON syntax is like JavaScript object syntax (see [Section 5.2](#05_002.html_h5.2)), where you have an object inside of <samp class="listingcharacter">{}</samp> that contains <samp class="listingcharacter">name:value</samp> pairs. Commas are used to separate data and names (or keys) must be written as strings within <samp class="listingcharacter">""</samp>, unlike JavaScript objects that can be written within single quotes. [Listing 6.1](#06_001.html_l6.1) shows our car example from the previous section written with JSON syntax.

```
{
  "make": "Mercedes",
  "model": "A Class AMG",
  "colour": "Black"
} 
```

**Listing 6.1**     JSON Object

That object itself can also be a value of a <samp class="listingcharacter">name:value</samp> pair, with <samp class="listingcharacter">myCar</samp> as the name and the car object as its value, as shown in [Listing 6.2](#06_001.html_l6.2).

```
{
  "myCar": {
    "make": "Mercedes",
    "model": "A Class AMG",
    "colour": "Black"
  }
} 
```

**Listing 6.2**     JSON name:value Pair with Object

You can also have multiple objects within an array, as we see in [Listing 6.3](#06_001.html_l6.3) (in this case, our <samp class="listingcharacter">Mercedes</samp>, <samp class="listingcharacter">BMW</samp>, and <samp class="listingcharacter">Audi</samp> example), which is a common format you will receive when working with SAP OData services. When you call an SAP OData service, you will likely receive a JSON format response with a list of items in an array, like a list of purchase orders.

```
{
  "myCars": [
    {
      "make": "Mercedes",
      "model": "A Class AMG",
      "colour": "Black"
    },
    {
      "Make": "BMW",
      "model": "M Series",
      "colour": "White"
    },
    {
      "make": "Audi",
      "model": "S4",
      "colour": "Blue"
    }
  ]
} 
```

**Listing 6.3**     JSON Object Array

## 6.2    JSON Methods

Note that even though JSON data and JavaScript objects are similar, you will need to convert the JSON data to work with it in your application. To do that, you will need to parse (change) the JSON string from your request into a JavaScript object using the standard JavaScript method <samp class="listingcharacter">JSON.parse()</samp>.

[Listing 6.4](#06_002.html_l6.4) shows some JSON data being parsed and assigned to the <samp class="listingcharacter">object</samp> variable. The <samp class="listingcharacter">object</samp> variable contains the parsed JSON data, which is now type <samp class="listingcharacter">object</samp>, that we can now work with in our code.

```
var object = JSON.parse(
  '{ "make": "Mercedes", "model": "A Class AMG", "colour": "Black", "trimOptions": ["Leather", "Cloth", "Alcantara"]}'
);
console.log(object);
console.log(typeof object); // object
console.log(object.make); // Mercedes
console.log(object.trimOptions[2]); // Alcantara 
```

**Listing 6.4**     JSON.parse()

To access the JSON data you have just parsed, use the same syntax for JavaScript objects from [Section 5.2](#05_002.html_h5.2). In [Listing 6.4](#06_002.html_l6.4), the output of <samp class="listingcharacter">make</samp> and <samp class="listingcharacter">trimOptions[2]</samp> will be <samp class="listingcharacter">Mercedes</samp> and <samp class="listingcharacter">Alcantara,</samp> respectively.

Once finished reading and manipulating our JSON data, we must convert it back to JSON before sending it to a server. This is done using a method called <samp class="listingcharacter">JSON.stringify()</samp>. In [Listing 6.5](#06_002.html_l6.5), we pass the <samp class="listingcharacter">jsObject</samp> variable into the <samp class="listingcharacter">JSON.Stringify()</samp> method and log the converted JSON string to the console. Notice we logged the <samp class="listingcharacter">jsObject</samp> variable type before and after it was converted to JSON format to show how it is converted from a JavaScript object back to JSON format, which is type <samp class="listingcharacter">string</samp>.

```
let jsObject = {
  make: "Mercedes",
  model: "A Class AMG",
  colour: "Black",
  trimOptions: ["Leather", "Cloth", "Alcantara"],
};
console.log(typeof jsObject); // object
console.log(JSON.stringify(jsObject));
console.log(typeof JSON.stringify(jsObject)); // string 
```

**Listing 6.5**     JSON.stringify()

## 6.3    OData and SAPUI5

SAPUI5 and OData are beyond the scope of this E-Bite, but if you are an ABAP professional who is moving into JavaScript, you will almost certainly encounter SAPUI5 and OData. It is important to know that SAPUI5 makes use of JSON data in a variety of ways and can load JSON data from either within the app (like test data) or from an outside source like SAP Gateway.

If you were, for example, creating test data for your application, you would store it in a file like test_data.json. This file would contain JSON-formatted data like that shown in [Listing 6.4](#06_002.html_l6.4), and you would load that JSON data into your application using an SAPUI5 framework method like this:

```
oModel.loadData("test_data.json") 
```

That will trigger a <samp class="listingcharacter">GET</samp> request, which will pull the data from that file and store it in the SAPUI5 model to be used in your application. We will cover this general type of data request in more detail in [Section 11](#11_001.html_h11) and [Section 12.7](#12_007.html_h12.7).

If you were using an SAP Gateway OData service, you would create an OData model with syntax that looks like this:

```
var oModel = new ODataModel("http://url.com/sap/opu/odata/IWBEP/GWSAMPLE_BASIC/?$format=json"); 
```

This would create an SAPUI5 OData model that you would use to pass data back and forth to your SAP system and display in your SAPUI5 views.

For now, just be aware that JSON is a data format you will often work with in JavaScript applications when requesting data from an outside source.

# 7    The Document Object Model (DOM)

The DOM is a treelike structure that represents the HTML elements on a webpage. The DOM is created by the browser when a webpage loads, allowing you to access all the HTML elements dynamically, including their Cascading Style Sheets (CSS) properties. The DOM is important because you will use it in conjunction with JavaScript to manipulate those HTML elements and to create dynamic webpages.

In this section, we’ll see how JavaScript interacts with the DOM through a practical example, and then learn how to traverse the DOM, use selector methods, and manipulate DOM elements.

## 7.1    DOM Example

Run the example shown previously in [Section 1.4](#01_004.html_h1.4), [Listing 1.3](#01_004.html_l1.3) and [Listing 1.4](#01_004.html_l1.4), and once you have your HTML page loaded in the browser, right-click Some old text, and in the context menu, click Inspect. You should see the Chrome DevTools window and, under the Elements tab, you should see your HTML element highlighted as shown in [Figure 7.1](#07_001.html_f7.1).

[![Basic HTML Webpage](bilderklein/klein07_001.png)](img-f7.1.html)

**Figure 7.1**     Basic HTML Webpage

Keep the Chrome DevTools window open and click the Try it button, and watch the text change in the Elements tab for that HTML element. This is a live view of your JavaScript code dynamically changing an HTML element using the DOM. You can manipulate the DOM directly from within the Elements tab by double-clicking that same text (between the <samp class="listingcharacter"><p></p></samp> tags), changing it, and pressing [Enter]. You should see the text on the webpage change to whatever you typed.

In our example, we interacted with an HTML element by selecting that element from the DOM and changing its value using this line of code:

```
document.getElementById("test").innerHTML = "Some new text appeared!"; 
```

Let’s break down this statement and look at what each part does:

*   <samp class="listingcharacter">document</samp>
    This is the “D” in DOM and is the global (root) document object that contains all the HTML elements.

*   <samp class="listingcharacter">.getElementById("test")</samp>
    This is the JavaScript method used to select the element in the DOM, which is the <samp class="listingcharacter"><p></samp> tag containing <samp class="listingcharacter programmingelement">"Some old text"</samp> with the <samp class="listingcharacter">id</samp> attribute <samp class="listingcharacter">test</samp>.

*   <samp class="listingcharacter">.innerHTML = "Some new text appeared!"</samp>
    This is the HTML property that sets the content of the HTML element (the bit between the <samp class="listingcharacter"><p>…</p></samp> tags) to <samp class="listingcharacter programmingelement">"Some new text appeared!"</samp>

## 7.2    Traversing the DOM

The DOM itself is just an object represented as an interconnected tree of nodes (HTML elements). You have a window object which represents the Browser tab, under which sits the document object node, which can be considered the root node of the actual webpage, with all your other nodes (HTML elements) sitting somewhere underneath it. If you look at the Elements tab in the Chrome DevTools window, you will see the node structure of our HTML page, as shown in [Figure 7.2](#07_002.html_f7.2).

[![DOM Node Structure](bilderklein/klein07_002.png)](img-f7.2.html)

**Figure 7.2**     DOM Node Structure

If you had to follow the full path to the <samp class="listingcharacter"><p></samp> tag containing our dynamic text, it would look roughly like this: Browser • document • <body> • <div id="text-div"> • <p id ="test">.

You can navigate around the DOM tree in Chrome DevTools by clicking the small arrows next to a node, which will open the next-level node(s) underneath it until you reach the lowest-level node.

When you traverse the DOM, you are navigating to whichever HTML element you are interested in so that you can read or manipulate it.

## 7.3    Selector Methods

In our previous example, we used the DOM method <samp class="listingcharacter">document.getElementById("test")</samp> to select an HTML element from the DOM based on its <samp class="listingcharacter">id</samp> attribute, which in this case was <samp class="listingcharacter">test</samp>. This is one of the JavaScript methods available as part of the Selectors API, which is part of the web APIs (more on this in [Section 13](#13_001.html_h13)). You have other methods you can use. One of the more popular ones is as follows:

```
document.querySelector("#test") 
```

This method finds the same <samp class="listingcharacter"><p></samp> element with <samp class="listingcharacter">"#test"</samp> referring to the <samp class="listingcharacter">id</samp> value <samp class="listingcharacter">test</samp>. Run this same method to find more than one element matching that <samp class="listingcharacter">id</samp> as follows:

```
document. querySelectorAll("#test") 
```

This method will return a list of all the elements that have the <samp class="listingcharacter">id</samp> of <samp class="listingcharacter">test</samp>.

You can also use Chrome DevTools to find the selector in the Elements tab by right-clicking an element and selecting Copy • Copy Selector, which you can then paste into your JavaScript selector method, as shown in [Figure 7.3](#07_003.html_f7.3).

[![Chrome Copy Selector](bilderklein/klein07_003.png)](img-f7.3.html)

**Figure 7.3**     Chrome Copy Selector

## 7.4    DOM Manipulation

You can use the DOM to change many different things on a webpage, from HTML element content text to element properties including CSS, even adding entirely new DOM elements. In our previous example, we changed the <samp class="listingcharacter">innerHTML</samp>, which is the content of the element, i.e., the text between the <samp class="listingcharacter"><p></p></samp> tags. In [Listing 7.1](#07_004.html_l7.1), we adjust the CSS of the text when it changes after the button click event using the <samp class="listingcharacter">style</samp> property after the new text is added.

```
function changeSomeText() {
  document.getElementById("test").innerHTML = "Some new text appeared!";
  document.getElementById("test").style.cssText =
    "fontWeight: bold; background-color: Chartreuse";
} 
```

**Listing 7.1**     DOM Manipulation: CSS

We can take DOM manipulation even further than just changing text or CSS properties and add completely new elements to the DOM. In [Listing 7.2](#07_004.html_l7.2), we create a function that adds a new <samp class="listingcharacter"><p></samp> tag to the <samp class="listingcharacter">div</samp> with an <samp class="listingcharacter">id</samp> of <samp class="listingcharacter">text-div</samp>.

```
function addSomeText() {
  const div = document.getElementById("text-div");
  const newText = document.createElement("p");
  newText.textContent = "Some brand new text here!";
  div.appendChild(newText);
} 
```

**Listing 7.2**     Adding New Element to the DOM

In this example, we first create a variable that holds our <samp class="listingcharacter">div</samp> where we want to place the new <samp class="listingcharacter"><p></samp> tag. We then call the method <samp class="listingcharacter">.createElement("p"),</samp> which creates a new <samp class="listingcharacter"><p></samp> element, and assign it to the variable <samp class="listingcharacter">newText</samp>. We add some text to the newly created <samp class="listingcharacter"><p></samp> element using <samp class="listingcharacter">.textContent</samp> and call <samp class="listingcharacter">.appenChild</samp> on our <samp class="listingcharacter">div</samp> variable to append the element as a child node.

This works both ways; you can follow similar logic to remove DOM elements as well. The function in [Listing 7.3](#07_004.html_l7.3) removes the <samp class="listingcharacter"><p></samp> element with an <samp class="listingcharacter">id</samp> of <samp class="listingcharacter">test</samp> from the DOM.

```
function removeSomeText() {
  const text = document.querySelector("#test");
  text.remove();
} 
```

**Listing 7.3**     Removing an Element from the DOM

Here, we create a variable <samp class="listingcharacter">text</samp> and assign it the <samp class="listingcharacter"><p></samp> element with an <samp class="listingcharacter">id</samp> of <samp class="listingcharacter">test</samp> using the <samp class="listingcharacter">.querySelector()</samp> method. We then call the <samp class="listingcharacter">.remove()</samp> method on that <samp class="listingcharacter">text</samp> variable to completely remove the element from the DOM.

# 8    HTML Events

Our example in the previous section uses the HTML <samp class="listingcharacter">onclick</samp> event (when a user clicks using their mouse) to trigger the JavaScript code that changes the text in the <samp class="listingcharacter"><p></p></samp> tag. There are many different types of HTML events, ranging from a mouse click to a key press to just hovering your mouse over a certain HTML element. You specify if you want to trigger these events within the properties of the element and specify the JavaScript code to be executed when this event is triggered.

We’ll discuss handling events in the following sections, as well as the most common events that are available.

## 8.1    Registering Events

In our example from [Section 7](#07_001.html_h7), we specified the <samp class="listingcharacter">onclick</samp> event in the <samp class="listingcharacter"><button></samp> tag, as follows:

```
<button type="button" onclick="changeSomeText()">Try it</button> 
```

The <samp class="listingcharacter">onclick</samp> event is specified as a property and the JavaScript function is specified after the equals sign with <samp class="listingcharacter">()</samp>, meaning it needs to be executed on this event. We can add another event, <samp class="listingcharacter">onmouseover()</samp>, to our example and change the <samp class="listingcharacter"><h1></samp> text when the mouse cursor hovers over it. Let’s adjust our <samp class="listingcharacter"><h1></samp> tag to include an <samp class="listingcharacter">id</samp> property and <samp class="listingcharacter">onmouseover</samp> event property:

```
<h1 id="header-text" onmouseover="onMouseHoverH1()">A normal everyday webpage</h1> 
```

We then add a new JavaScript function, <samp class="listingcharacter">onMouseHoverH1()</samp>, with the function code shown in [Listing 8.1](#08_001.html_l8.1) to modify the text and CSS when we hover over the text. The result will be the text You hovered over me didn’t you! appearing in red, as shown in [Figure 8.1](#08_001.html_f8.1).

```
function onMouseHoverH1() {
  let headerText = document.querySelector("#header-text");
  headerText.style.color = "red";
  headerText.innerHTML = "You hovered over me didn't you!";
} 
```

**Listing 8.1**     onmouseover Event Function

[![onmouseover Event](bilderklein/klein08_001.png)](img-f8.1.html)

**Figure 8.1**     onmouseover Event

Along with registering your events in the HTML DOM element properties themselves, you can also register an event directly in your JavaScript code without needing to specify the <samp class="listingcharacter">onclick</samp> property in your HTML. In [Listing 8.2](#08_001.html_l8.2), we use the <samp class="listingcharacter">window.onload</samp> event to register a <samp class="listingcharacter">"click"</samp> event on our button.

```
window.onload = (event) => {
  document.getElementById("btn1").addEventListener("click", changeSomeText);
}; 
```

**Listing 8.2**     Registering an HTML Event with JavaScript

In this example, the <samp class="listingcharacter">window.onload</samp> event only fires when the page has fully loaded, which needs to happen because we can only register an event to an HTML property when it’s loaded. Once the page is loaded, we use the <samp class="listingcharacter">.addEventListener</samp> method to register the <samp class="listingcharacter">"click"</samp> event (like the <samp class="listingcharacter">onclick</samp> HTML event property), followed by the function <samp class="listingcharacter">changeSomeText</samp>, which will be triggered when the event is fired.

## 8.2    Handling Complimenting Events

In our example from [Listing 8.1](#08_001.html_l8.1), notice how when you hover over the header text, the DOM manipulation occurs, but the text stays that way even when your mouse is no longer hovering over the header text. It is important to understand that when you change things in the DOM, you often need a counteracting event to balance things, like <samp class="listingcharacter">onmouseout</samp> in conjunction with <samp class="listingcharacter">onmouseover</samp>, to create the complete effect of moving your mouse on and off an element.

To do that, we adjust our HTML code once more and add the <samp class="listingcharacter">onmouseout</samp> property with a JavaScript function to return the text to what it was before. We add the <samp class="listingcharacter">onmouseout</samp> event property to the <samp class="listingcharacter"><h1></samp> tag as follows:

```
<h1 id="header-text" onmouseover="onMouseHoverH1()" onmouseout="onMouseOffH1()">A normal everyday webpage</h1> 
```

We add this with a JavaScript function like the one for <samp class="listingcharacter">onmouseover</samp>, as shown in [Listing 8.3](#08_002.html_l8.3), including the code to change the header text back. The result should be that the text changes when you hover over it and changes back when your mouse moves away again.

```
function onMouseOffH1() {
  let headerText = document.querySelector("#header-text");
  headerText.style.color = "";
  headerText.innerHTML = "A normal everyday webpage";
} 
```

**Listing 8.3**     onmouseout Event Function

## 8.3    Common HTML Events

Mouse events are common HTML events you will use regularly to make your webpage dynamic, but there are two other events worth noting you will come across quite often, as we’ll discuss in the following sections.

### onload

The <samp class="listingcharacter">onload</samp> HTML event fires when the page has finished loading and is a common requirement to execute JavaScript code that runs only when all webpage elements have loaded. Using our example from the previous section, we can add the <samp class="listingcharacter">onload</samp> event to our <samp class="listingcharacter"><body></samp> tag as follows:

```
<body onload="onPageLoad()"></body> 
```

We then add a new function from [Listing 8.4](#08_003.html_l8.4) to trigger an alert when our page has fully loaded.

```
function onPageLoad() {
  alert("Congratulations! The page has finished loading.")
} 
```

**Listing 8.4**     onload Event Function

### onchange

The <samp class="listingcharacter">onchange</samp> HTML event is triggered every time an HTML element changes; for example, as you type something into a form input, each new character you type will trigger the <samp class="listingcharacter">onchange</samp> event. To demonstrate, we add a form input to our HTML page and add the <samp class="listingcharacter">onchange</samp> event to it as follows:

```
Name:<input id="name-input" type="text" onchange="onInputChange()"> 
```

We add the function from [Listing 8.5](#08_003.html_l8.5) that will alert you whenever you type something new into the input and click out of it or press [Enter].

```
function onInputChange() {
  alert("Something changed in the input!");
} 
```

**Listing 8.5**     onchange Event Function

# 9    Asynchronous JavaScript

Up until this point, you have used JavaScript in a synchronous way without really knowing it. JavaScript is by nature a synchronous language, which means functions are executed in the order they were written, or more simply put, functions can only be executed one at a time. That point highlights one of the biggest downsides of standard JavaScript, i.e., each function must finish executing before the next one can start, causing what is known as blocking. Blocking can render your webpage slow and unresponsive. This is similar to when an ABAP program specifies <samp class="listingcharacter">COMMIT WORK AND WAIT</samp>, where the program has to wait for the result of that commit before continuing on.

This is where asynchronous JavaScript comes in. Asynchronous JavaScript is a way for you to get around the linear flow of standard JavaScript and add some flexibility to your code, so you can either wait for a function to finish executing or let it execute in the background and finish in its own time. This is similar to an ABAP program called <samp class="listingcharacter">COMMIT WORK</samp> where the program doesn’t wait around for the result of the commit. Note that this is an advanced JavaScript topic, but one worth being introduced to from the beginning. Asynchronous JavaScript is illustrated in [Listing 9.1](#09_001.html_l9.1) with the JavaScript <samp class="listingcharacter">setTimeout()</samp> function, which pauses the function execution for a few seconds. Notice how the function <samp class="listingcharacter">callExternalServer()</samp> does not hold up the <samp class="listingcharacter">doSomethingElse()</samp> function (even though it is executed before) and lets the rest of the program continue until it completes.

```
const doSomething = () => {
  console.log("Do something");
};
const callExternalServer = () => {
  setTimeout(() => {
    console.log("Call to external server complete");
  }, 3000);
};
const doSomethingElse = () => {
  console.log("Do something else");
};
doSomething();
callExternalServer();
doSomethingElse(); 
```

**Listing 9.1**     setTimeout() Function

In this section, we’ll look at the older JavaScript callbacks, the JavaScript promise, and finally the newer <samp class="listingcharacter">async</samp>/<samp class="listingcharacter">await</samp> syntax, which gives much more granular control over when our JavaScript logic executes.

## 9.1    Callbacks in JavaScript

Callbacks are one of the older coding strategies in JavaScript but you will see them often. They involve passing a function as a parameter to another function. The idea is that you create your first function that runs until completion and when it does, it calls another function, known as the callback. Think of it as sending someone a message and asking them to do something and “call you back” when they are done.

This allows for more granular control over when functions are executed and allows you to handle scenarios where one function relies on another to complete before it can start. A great way to illustrate this is with a calculator. In [Listing 9.2](#09_001.html_l9.2), we create a calculator we can pass some numbers into and when the calculation is done, we call another function that logs that result to the console.

```
const displayCalculatorResult = (result) => {
  console.log(result);
};

const calculatorWithCallback = (num1, num2, callback) => {
  let result = num1 + num2;
  // Calling our callback function
  callback(result);
};
calculatorWithCallback(1, 9, displayCalculatorResult); 
```

**Listing 9.2**     JavaScript Callback

Notice that we declared two functions, one to display the output and the other to calculate it. In our calculator function, we specified two number parameters and a third <samp class="listingcharacter">callback</samp> parameter, which is where we passed the display function. So, when we call the calculator function, the display function is only executed after the calculation has completed and logs the result to the console. The key here is that the display function only runs when the calculation is complete.

## 9.2    JavaScript Promise

The JavaScript promise is another advanced topic, but it is effectively just another way of writing a callback function with the added advantage of returning either a success or error and letting us decide what to do in each scenario. Promises are used for situations where you need to request data from outside your app and need to wait for that data to be returned before you start processing. We can simulate this using the <samp class="listingcharacter">setTimeout()</samp> function again, which will pause our promise execution and mimic a call to an external server.

The syntax for a promise is a bit complex, but it will make sense the more you use them. In [Listing 9.3](#09_002.html_l9.3), we declare a new function promise with <samp class="listingcharacter">resolve</samp> and <samp class="listingcharacter">reject</samp> parameters that we will use inside the function. We tell the function to return a <samp class="listingcharacter">resolve</samp> once the <samp class="listingcharacter">setTimeout</samp> function has completed after 5000 milliseconds (5 seconds).

```
const myFirstPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve("The server finally sent a response!");
    reject("An error occured :(");
  }, 5000);
});

myFirstPromise
  .then((data) => {
    // resolve part
    console.log(data);
  })
  .catch((error) => {
    // reject part
    console.log(error);
  }); 
```

**Listing 9.3**     JavaScript Promise

Notice how there is a five-second delay before the text is logged to the console. We call the <samp class="listingcharacter">myFirstPromise</samp> function and place the <samp class="listingcharacter">then()</samp> keyword after it, which holds the function to be executed when the promise function resolves. The <samp class="listingcharacter">resolve</samp> from the promise passes the text in the <samp class="listingcharacter">resolve</samp> brackets as a parameter to the <samp class="listingcharacter">then()</samp> part, which we import using the <samp class="listingcharacter">data</samp> parameter.

Also, notice that we have a <samp class="listingcharacter">reject()</samp>in there as well, but it was not executed. Normally, you would have some logic within the promise that would determine if the <samp class="listingcharacter">resolve</samp> were called or the <samp class="listingcharacter">reject</samp>. To trigger the <samp class="listingcharacter">reject</samp> in our example, we comment out the <samp class="listingcharacter">resolve()</samp> line and run the example again like before. You should now see the text <samp class="listingcharacter">"An error occurred :("</samp> logged to the console.

So, when using promises, just remember that promise <samp class="listingcharacter">resolve</samp> maps to the <samp class="listingcharacter">then()</samp> section and promise <samp class="listingcharacter">reject</samp> maps to the <samp class="listingcharacter">catch()</samp> section (like a <samp class="listingcharacter">TRY</samp>/<samp class="listingcharacter">CATCH</samp> block in ABAP). You can structure your success or fail logic around that.

## 9.3    Async and Await

The <samp class="listingcharacter">async</samp> and <samp class="listingcharacter">await</samp> keywords in JavaScript help make writing asynchronous code easier, compared to the previous promise syntax. The <samp class="listingcharacter">async</samp> keyword is used to transform a JavaScript function into a promise and replaces the <samp class="listingcharacter">new Promise</samp> syntax from [Listing 9.3](#09_002.html_l9.3). This then allows you to use the <samp class="listingcharacter">await</samp> keyword within the async function, which when placed in front of a normal function will wait for that function call to finish.

In [Listing 9.4](#09_003.html_l9.4), we compare a normal function versus what happens when you insert <samp class="listingcharacter">async</samp> before it. Notice how <samp class="listingcharacter">myFunction()</samp> returns the text, while <samp class="listingcharacter">myAsyncFunction()</samp> returns text wrapped in a promise because of the <samp class="listingcharacter">async</samp> keyword.

```
const myFunction = () => {
  return "A normal function";
};
console.log(myFunction()); // A normal function

const myAsyncFunction = async () => {
  return "A promise function"; // Promise { 'A promise function' }
};
console.log(myAsyncFunction()); 
```

**Listing 9.4**     async Function

Now that we know <samp class="listingcharacter">myAsyncFunction</samp> is a promise, we can rewrite our standard promise example from [Listing 9.3](#09_002.html_l9.3) using the <samp class="listingcharacter">async</samp> syntax, as shown in [Listing 9.5](#09_003.html_l9.5). We will also add two more calls to see how the flow works before and after the <samp class="listingcharacter">setTimeout</samp> function runs.

```
const myAsyncFunction = async () => {
  const myFirstPromise = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("The server finally sent a response!");
      //   reject("An error occured :(");
    }, 5000);
  });
  // Run this first
  console.log("Let's get started!");
  // Run this second but wait to finish (5 seconds)
  console.log(await myFirstPromise);
  // Run only when the function promise above has resolved
  console.log("I had to wait for the call above to finish");
};

myAsyncFunction(); 
```

**Listing 9.5**     async/await Function

In [Listing 9.5](#09_003.html_l9.5), we have the following text logged to the console:

<samp class="listingcharacter">Let’s get started!</samp> (Followed by a five-second pause.)
<samp class="listingcharacter">The server finally sent a response!</samp>
<samp class="listingcharacter">I had to wait for the call above to finish!</samp>

The <samp class="listingcharacter">async</samp> function acts as a wrapper for you to call other functions (including normal promises) within it, giving you better control over where one function might need to wait on another before executing. To see the benefit of the <samp class="listingcharacter">await</samp> keyword, remove it completely and see the following logged to the console:

<samp class="listingcharacter">Let’s get started!</samp> (no five-second pause).
<samp class="listingcharacter">Promise { <pending> }</samp>
<samp class="listingcharacter">I had to wait for the call above to finish!</samp>

You can clearly see where the promise (or any other function that takes time to execute) sits and how it has not been given a chance to finish before proceeding onto the next line of code, resulting in potential instability. Add the <samp class="listingcharacter">await</samp> keyword in and the correct order of events would be restored.

# 10    Classes

Most ABAP developers are familiar with the concept of a class in the realm of object-oriented programming. This section assumes you know at least the very basics of ABAP classes and the object-oriented programming paradigm, and illustrates how to recreate a class using JavaScript syntax.

Your JavaScript class acts as a blueprint for an object, and just like an ABAP class, you have the same building blocks to build that object blueprint, including attributes, methods, a constructor, static and dynamic attributes, and even inheritance.

## 10.1    Class Definition

Classes in JavaScript can be defined using either a class declaration or a class expression. A class expression can further be defined as named or unnamed. In [Listing 10.1](#10_001.html_l10.1), we declare our class with the <samp class="listingcharacter">class</samp> keyword followed by the name of our class, <samp class="listingcharacter">car</samp>.

```
class car {
  constructor(make, model) {
    (this.make = make);
  }
}
console.log(car.name); // car 
```

**Listing 10.1**     Class Declaration

In [Listing 10.2](#10_001.html_l10.2), we declare an unnamed class (no name after the <samp class="listingcharacter">class</samp> keyword) using a class expression that assigns a class to the variable <samp class="listingcharacter">myCarClass.</samp>

```
let myCarClass = class {
  constructor(make) {
    this.make = make;
  }
};
console.log(myCarClass.name); // myCarClass 
```

**Listing 10.2**     Class Expression (Unnamed)

In [Listing 10.3](#10_001.html_l10.3), we assign the same class from [Listing 10.2](#10_001.html_l10.2) to the <samp class="listingcharacter">myCarClass</samp> variable, but this time the class is named because we have included the class name <samp class="listingcharacter">car</samp> after the <samp class="listingcharacter">class</samp> keyword.

```
let myCarClass = class car {
  constructor(make) {
    this.make = make;
  }
};
console.log(myCarClass.name); // car 
```

**Listing 10.3**     Class Expression (Named)

Once the class is declared, we use it to instantiate an object by declaring a variable and using the <samp class="listingcharacter">new</samp> keyword, followed by the class name and any parameters needed for the constructor. In [Listing 10.4](#10_001.html_l10.4), we instantiate a new class object and assign it to the variable <samp class="listingcharacter">Mercedes</samp>.

```
class car {
  constructor(make) {
    this.make = make;
  }
}
let newCar = new car("Mercedes");
console.log(`${newCar.make}`); // Mercedes 
```

**Listing 10.4**     Class Object

In [Listing 10.4](#10_001.html_l10.4), we need to pass in the make of our new car object so that the class constructor can assign it as a property to the object itself using the <samp class="listingcharacter">this</samp> keyword. Once we have our new car object, we can call the properties of that object and, in this case, log them to the console.

## 10.2    Methods

Just like ABAP, we can add methods to our JavaScript class that allow us to interact with the instantiated objects. The syntax looks like a normal JavaScript function and includes the <samp class="listingcharacter">method_name</samp> followed by <samp class="listingcharacter">()</samp> holding the parameters and the actual logic within <samp class="listingcharacter">{}</samp>.

Using our example from [Listing 10.4](#10_001.html_l10.4), we add five new methods under the constructor in [Listing 10.5](#10_002.html_l10.5). They are starting and stopping the engine, increasing speed, applying the brakes, and logging our speed to the console. We also add our car’s speed as a new attribute to keep track of how fast we are going.

```
class car {
  constructor(make) {
    (this.make = make), (this.current_speed = 0);
  }
  start_engine() {
    console.log("Car started!");
    this.log_speed();
  }
  stop_engine() {
    console.log("Engine off.");
  }
  accelerate(kmh) {
    typeof kmh === "number"
      ? (this.current_speed += kmh)
      : console.error("parameter must be a number");
    this.log_speed();
  }
  brake() {
    this.current_speed = 0;
    this.log_speed();
  }
  log_speed() {
    console.log(`Speedometer: ${this.current_speed}`);
  }
}

let newCar = new car("Mercedes");
console.log(`${newCar.make}`); // Mercedes
newCar.start_engine();
newCar.accelerate(5);
newCar.accelerate(10);
newCar.accelerate(10);
newCar.brake();
newCar.stop_engine(); 
```

**Listing 10.5**     JavaScript Class Methods

Run the code from [Listing 10.5](#10_002.html_l10.5) and the output to the console will be as shown in [Listing 10.6](#10_002.html_l10.6).

```
Mercedes
Car started!  
Speedometer: 0
Speedometer: 5
Speedometer: 15
Speedometer: 25
Speedometer: 0
Engine off. 
```

**Listing 10.6**     Output from Listing 10.5

We were able to call the methods of our new object methods as defined in our <samp class="listingcharacter">car</samp> class in the same way we access the classes’ attributes (using the <samp class="listingcharacter">.</samp> notation), letting us control the car object and take it for a spin.

## 10.3    Static versus Dynamic Attributes and Methods

JavaScript class attributes and methods can be declared as static, as with ABAP. If you declare a static attribute or method in your JavaScript class, you can access it directly through the class without needing to instantiate an object. The drawback is you will not be able to access those same static attributes or methods from instances of that class.

To demonstrate this, we use our example in [Listing 10.5](#10_002.html_l10.5) and add a static attribute <samp class="listingcharacter">static_attribute</samp> and static method <samp class="listingcharacter">static_method()</samp>, calling them before we instantiate the object, as shown in [Listing 10.7](#10_003.html_l10.7).

```
class car {
  constructor(make) {
    (this.make = make), (this.current_speed = 0);
  }
  start_engine() {
    console.log("Car started!");
    this.log_speed();
  }
  stop_engine() {
    console.log("Engine off.");
  }
  accelerate(kmh) {
    typeof kmh === "number"
      ? (this.current_speed += kmh)
      : console.error("parameter must be a number");
    this.log_speed();
  }
  brake() {
    this.current_speed = 0;
    this.log_speed();
  }
  log_speed() {
    console.log(`Speedometer: ${this.current_speed}`);
  }
  static static_method() {
    return "Hello from a static class method";
  }
  static static_attribute = "A static attribute";
}

console.log(car.static_method());
console.log(car.static_attribute);
let newCar = new car("Mercedes");
console.log(`${newCar.make}`); // Mercedes
newCar.start_engine();
newCar.accelerate(5);
newCar.accelerate(10);
newCar.accelerate(10);
newCar.brake();
newCar.stop_engine(); 
```

**Listing 10.7**     Static Attributes and Methods

The output from [Listing 10.7](#10_003.html_l10.7) will look as shown in [Listing 10.8](#10_003.html_l10.8).

```
Hello from a static class method
A static attribute
Mercedes
Car started!
Speedometer: 0
Speedometer: 5
Speedometer: 15
Speedometer: 25
Speedometer: 0
Engine off. 
```

**Listing 10.8**     Output from Listing 10.7

Notice that we can access the static attribute and static method before we instantiate the class. If you call the static method or access the static attribute using the <samp class="listingcharacter">newCar</samp> object, you will get a <samp class="listingcharacter">TypeError</samp>.

## 10.4    Inheritance

Inheritance in JavaScript classes works in a similar way to ABAP classes and follows the same general object-oriented principle of a subclass inheriting (and extending) properties and methods of a superclass. The basic syntax involves the subclass definition with the addition of the <samp class="listingcharacter">extends</samp> keyword, followed by the name of the superclass you are inheriting from. From there, you can use the <samp class="listingcharacter">super</samp> method in the subclass constructor to pull in the attributes and methods from your superclass.

We continue our example in [Listing 10.7](#10_003.html_l10.7) and create a subclass that extends the <samp class="listingcharacter">car</samp> superclass, then use it to create a more specific class for a model of car. As shown in [Listing 10.9](#10_004.html_l10.9), we create a class called <samp class="listingcharacter">carModel</samp> that extends the <samp class="listingcharacter">car</samp> superclass using the <samp class="listingcharacter">extends</samp> keyword. Inside the <samp class="listingcharacter">carModel</samp> class <samp class="listingcharacter">constructor</samp>, we reference the superclass attributes and methods using the <samp class="listingcharacter">super</samp> keyword, making sure to pass in the <samp class="listingcharacter">(make)</samp> of the car, as the <samp class="listingcharacter">make</samp> attribute is assigned in the superclass, which the subclass then inherits. After that, the subclass extends the attributes of the superclass by adding its own attribute <samp class="listingcharacter">this.model</samp> in its own constructor.

```
class carModel extends car {
  constructor(make, model) {
    super(make);
    this.model = model;
  }
}

let newCarModel = new carModel("Mercedes", "S Class");
console.log(`${newCarModel.make} ${newCarModel.model}`); // mercedes S Class
newCarModel.start_engine();
newCarModel.accelerate(5);
newCarModel.accelerate(10);
newCarModel.accelerate(10);
newCarModel.brake();
newCarModel.stop_engine(); 
```

**Listing 10.9**     Class Inheritance

The output to the console from [Listing 10.9](#10_004.html_l10.9), including both superclass and subclass, is as shown in [Listing 10.10](#10_004.html_l10.10).

```
Hello from a static class method
A static attribute
Mercedes
Car started!
Speedometer: 0
Speedometer: 5
Speedometer: 15
Speedometer: 25
Speedometer: 0
Engine off.
Mercedes S Class
Car started!
Speedometer: 0
Speedometer: 5
Speedometer: 15
Speedometer: 25
Speedometer: 0
Engine off. 
```

**Listing 10.10**     Output from Listing 10.9

Notice that the <samp class="listingcharacter">newCarModel</samp> object, which is instantiated using the subclass <samp class="listingcharacter">carModel,</samp> was able to call methods from the superclass <samp class="listingcharacter">car</samp> while adding in (or extending) the class attributes to include the car-specific model.

# 11    AJAX

Asynchronous JavaScript and XML (AJAX) allows you to communicate with external webservers from within your webpage using HTTP methods like <samp class="listingcharacter">GET</samp> or <samp class="listingcharacter">POST</samp> and update the DOM based on the response. AJAX revolves around the browser’s built-in <samp class="listingcharacter">XMLHttpRequest</samp> object and the more modern Fetch API, which allows you to request data outside of your webpage. You could use AJAX to call the JSON data found in [Section 6](#06_001.html_h6) and you would receive the same JSON-formatted response.

As the name suggests, one of the benefits of AJAX is that it works asynchronously. That means when you use it to request data from a server and you do not know how long that data return will take, it will not hold up your webpage waiting for that requested data. This means your webpage can be updated in the background while still working, presenting a better user experience.

We’ll explore two key components of AJAX—the <samp class="listingcharacter">XMLHttpRequest</samp> object and the Fetch API—in the following sections.

## 11.1    XMLHttpRequest Object

The <samp class="listingcharacter">XMLHttpRequest</samp> object can be used to request data from resources located on an external server, depending on your server configuration. These calls are normally restricted to the same server address as the app because of a security concept called cross-origin resource sharing (CORS). For simplicity, we will assume that your local server does not allow CORS, so we will use the <samp class="listingcharacter">XMLHttpRequest</samp> object to request data from a local file stored in the same folder as our index.html and app.js files, as shown in [Listing 11.1](#11_001.html_l11.1) and [Listing 11.2](#11_001.html_l11.2).

```
<html>
<head>
    <script src="app.js"></script>
</head>
<body>
    <p id="text">Some text</p>
    <button onclick="sendRequest()">Get the data!</button>
</body>
</html> 
```

**Listing 11.1**     index.html

We run the webpage from [Listing 11.1](#11_001.html_l11.1) and see some text with a button underneath on the page. When we click the button, it triggers an HTML <samp class="listingcharacter">onclick</samp> event that executes the <samp class="listingcharacter">sendRequest</samp> function in [Listing 11.2](#11_001.html_l11.2).

```
const sendRequest = () => {
  let xhttp = new XMLHttpRequest();
  xhttp.open("GET", "test_data.json", true);
  xhttp.send();
  xhttp.onreadystatechange = function () {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("text").innerHTML = this.responseText;
    }
  };
}; 
```

**Listing 11.2**     app.js

Inside this function, we create a new <samp class="listingcharacter">XMLHttpRequest</samp> object called <samp class="listingcharacter">xhttp</samp> and use that object to structure our request. First, we call the <samp class="listingcharacter">.open</samp> method, pass in the type of request <samp class="listingcharacter">GET</samp> with the path to our local file test_data.json, and set the third parameter to <samp class="listingcharacter">true</samp>, which tells the call to run asynchronously. With the request set up, we call the <samp class="listingcharacter">.send()</samp> method to send the request. We then specify the <samp class="listingcharacter">.onreadystatechange()</samp> method, which listens for the response from the request. When it receives the response, it executes the function after the <samp class="listingcharacter">=</samp> sign. In that function, we check if the <samp class="listingcharacter">readyState</samp> is <samp class="listingcharacter programmingelement">4</samp> and the <samp class="listingcharacter">http</samp> status is <samp class="listingcharacter programmingelement">200</samp> (meaning the call was a success), and we change the <samp class="listingcharacter"><p></samp> tag <samp class="listingcharacter">innerHTML</samp> (with an <samp class="listingcharacter programmingelement">id</samp> of <samp class="listingcharacter">text</samp>) to the response text.

In [Listing 11.3](#11_001.html_l11.3), we have some <samp class="listingcharacter">car</samp> JSON data, which we now see on the webpage in place of <samp class="listingcharacter">Some text</samp>.

```
[
  {
    "make": "Mercedes",
    "model": "A Class",
    "Color": "White",
    "picture": "http://placehold.it/32x32",
    "topSpeed": 300
  }
] 
```

**Listing 11.3**     test_data.json

## 11.2    Modern Syntax: Fetch API

The good news is there is a much simpler way to request data in most modern browsers, the Fetch API. The Fetch API is wonderful because when we use it to call an API endpoint, it returns a JavaScript promise, which is much easier to work with. We can align our logic to the response depending on whether the promise resolves (success) or rejects (fails).

The basic syntax for a <samp class="listingcharacter">fetch</samp> request is illustrated in [Listing 11.4](#11_002.html_l11.4).

```
fetch("https://urlendpoint.com")
  .then("Success")
  .catch("Failure"); 
```

**Listing 11.4**     Fetch API Syntax

In [Listing 11.5](#11_002.html_l11.5), we use the Fetch API to call the same data from our local file test_data.json. We replace the <samp class="listingcharacter">sendRequest</samp> function in [Listing 11.2](#11_001.html_l11.2) with the function in [Listing 11.5](#11_002.html_l11.5) and replace the button <samp class="listingcharacter">onclick</samp> event function in [Listing 11.1](#11_001.html_l11.1) to call the new function in [Listing 11.5](#11_002.html_l11.5).

```
const sendFetchRequest = () => {
  fetch("test_data.json")
    .then((response) => response.json())
    .then((body) => {
      document.getElementById("text").innerHTML = body[0]["make"];
    })
    .catch((error) => {
      console.log(error);
    });
}; 
```

**Listing 11.5**     Fetch Request

We now see the text <samp class="listingcharacter">Mercedes</samp> replace <samp class="listingcharacter">Some text</samp> on the page. Inside the <samp class="listingcharacter">sendFetchRequest</samp> function, we call our <samp class="listingcharacter">fetch</samp> request and, in the brackets, we pass in the path to the local file test_data.json we want it to read. That <samp class="listingcharacter">fetch</samp> request returns a JavaScript promise and it resolves (is successful), hitting our first <samp class="listingcharacter">.then()</samp> statement. Inside that <samp class="listingcharacter">.then()</samp> statement, we create a function where we import our <samp class="listingcharacter">(response)</samp> as a parameter from the request and convert it to JSON format. When that formatting is complete, we hit our second <samp class="listingcharacter">.then()</samp> statement, where we take our JSON-formatted response and pick out the object at index <samp class="listingcharacter">[0]</samp>. The JSON data at index <samp class="listingcharacter">[0]</samp> has a <samp class="listingcharacter">name:value</samp> pair <samp class="listingcharacter">"make": "Mercedes"</samp>, and we access the value from it with the <samp class="listingcharacter">[make]</samp> JSON attribute and change our <samp class="listingcharacter"><p></samp> tag in [Listing 11.1](#11_001.html_l11.1) to that value <samp class="listingcharacter">Mercedes</samp>. We also have a <samp class="listingcharacter">.catch()</samp> statement to catch any promise rejections or errors that might come up during the request, logging those errors to the console.

# 12    jQuery: Your First JavaScript Library

JavaScript has grown in popularity due in no small part to its vast array of libraries and frameworks, including SAPUI5, that you can use to do almost anything. JavaScript libraries help us “do more with less” and abstract much of the complex logic you need to write in standard JavaScript with something more user friendly. One of the most popular libraries in the world is called jQuery ([https://jquery.com/](https://jquery.com/)), created by John Resig, and it has become a standard in JavaScript.

The exciting thing about a library like jQuery is it abstracts all the logic we used in the previous sections (see [Section 7](#07_001.html_h7) and [Section 11](#11_001.html_h11)) and makes it even easier to traverse and manipulate the DOM, handle HTML events, and work with AJAX. This makes it the perfect choice to start with when learning to work with JavaScript libraries.

In this section, we’ll import the jQuery library and walk through key jQuery logic, including using selectors, registering events, changing HTML and DOM elements and CSS, and making AJAX queries.

## 12.1    Importing a jQuery Library

The first thing we do is set up our environment and import the jQuery library so we can use it in our app.js file. External JavaScript libraries are imported in the same way as our app.js files from previous examples as they are just external file(s) containing JavaScript code. We follow the same logic shown previously in [Section 1.4](#01_004.html_h1.4), [Listing 1.3](#01_004.html_l1.3), where we declared a <samp class="listingcharacter"><script></samp> tag in our index.html file, which contained a reference to a .js file that contained the code.

There are two ways we could import or install jQuery. Either download the jQuery JavaScript code from [https://jquery.com/download/](https://jquery.com/download/) and add it to the project folder, or if we are using <samp class="listingcharacter">node</samp>, we can use <samp class="listingcharacter">npm</samp> (node package manager) to install it as a dependency. For simplicity, we add the file to our project folder just like with our app.js file, seeing as the jQuery code is just a JavaScript file anyway. We create a jquery-3.6.0.min.js file, matching the file name to the version you downloaded. At the time of writing, we downloaded this version: [https://code.jquery.com/jquery-3.6.0.min.js](https://code.jquery.com/jquery-3.6.0.min.js). We then copy all the code from the downloaded jQuery file into the jquery-3.6.0.min.js file, create our index.html file, and include a reference to the jQuery and app.js files respectively within <samp class="listingcharacter"><script></samp> tags, as shown in [Listing 12.1](#12_001.html_l12.1).

```
<!DOCTYPE html>
<html lang="en">
<head>
    <script src="jquery-3.6.0.min.js"></script>
    <script src="app.js"></script>
    <title>Document</title>
</head>
<body>
    <div>
        <h1 id="heading1">Let's try out some jQuery</h1>
        <p id="text1">jQuery is awesome!</p>
        <a id="link1" href="https://jquery.com/" target="_blank">jQuery.com</a>
    </div>
    <div style="padding-top: 5px; padding-bottom: 5px;">
        <button id="button1">Press me!</button>
    </div>
    <div id="form-div">
        <form id="form">
            <h4>Newsletter Signup</h4>
            <label for="email">Email</label><br>
            <input type="text" id="email" name="fname"><br>
        </form>
        <button id="form-button">Submit</button>
    </div>
    </div>
</body>
</html> 
```

**Listing 12.1**     index.html

Finally, create an app.js file and copy the initial code shown in [Listing 12.2](#12_001.html_l12.2) into it, which can now access the jQuery library.

```
$(document).ready(() => {
  alert("Document is loaded!");
}); 
```

**Listing 12.2**     app.js

We run our index.html page from [Listing 12.1](#12_001.html_l12.1), where we see that once our page has fully loaded, an alert saying Document is loaded! appears, as shown in [Figure 12.1](#12_001.html_f12.1). In [Listing 12.2](#12_001.html_l12.2), we call the <samp class="listingcharacter">$(document).ready()</samp> function, which is a jQuery wrapper that ensures any code within this function (in our case, the alert) is executed only when the webpage has finished loading.

[![Alert Triggered inside jQuery](bilderklein/klein12_001.png)](img-f12.1.html)

**Figure 12.1**     Alert Triggered inside jQuery

## 12.2    Using jQuery Selectors

In [Listing 12.2](#12_001.html_l12.2), notice the jQuery syntax is a bit different than standard JavaScript. The <samp class="listingcharacter">$</samp> sign followed by the brackets <samp class="listingcharacter">$(document)</samp> is called a jQuery selector and replaces the long method calls we used in previous sections, i.e., <samp class="listingcharacter">document.getElementById("text")</samp>. As before, we can select HTML DOM elements like our <samp class="listingcharacter"><p></samp> tags using the syntax <samp class="listingcharacter">$("p")</samp>. If you wanted to select an element by its <samp class="listingcharacter">id</samp>, you include a <samp class="listingcharacter">#</samp> symbol like this: <samp class="listingcharacter">$("#text1")</samp>.

We remove the <samp class="listingcharacter">alert</samp> from [Listing 12.2](#12_001.html_l12.2) and add the code from [Listing 12.3](#12_002.html_l12.3) inside the <samp class="listingcharacter">$(document).ready()</samp> function, where we will use our button to change the text in the <samp class="listingcharacter"><p></samp> tag.

```
$("#button1").click(() => {
    $("#text1").text("This text changed!");
  }); 
```

**Listing 12.3**     jQuery Button Event

There are many jQuery selectors to choose from and they are all there to help you easily traverse the DOM. There are too many to address in this E-Bite, but some worth noting include the following:

*   <samp class="listingcharacter">$(":button")</samp> selects all <samp class="listingcharacter"><button></samp> elements and can be applied to and other HTML elements.

*   <samp class="listingcharacter">$(p:first)</samp> and <samp class="listingcharacter">$(p:last)</samp> selects the first and last <samp class="listingcharacter"><p></samp> tags in the DOM, respectively.

*   <samp class="listingcharacter">$("p#text1")</samp> selects all <samp class="listingcharacter"><p></samp> tags with an <samp class="listingcharacter">id</samp> of <samp class="listingcharacter">text1</samp>.

*   <samp class="listingcharacter">$("*")</samp> selects all elements on the webpage.

## 12.3    Registering Events

In our example, notice that we inadvertently registered an HTML <samp class="listingcharacter">onclick</samp> event just by calling the jQuery <samp class="listingcharacter">.click()</samp> method. In jQuery, registering standard HTML events is a breeze, because you can register your event and the function it calls within your JavaScript file without needing to create a reference in your HTML file.

Let’s reimplement the example in [Section 8](#08_001.html_h8), where we registered the mouse hover logic that handles what happens when we hover over text with the mouse and then move off again. We add the code shown in [Listing 12.4](#12_003.html_l12.4) to our <samp class="listingcharacter">$(document).ready()</samp> function.

```
 $("#text1").on({
    mouseenter: function () {
      $(this).text("Hey! You hovered over me!");
    },
    mouseleave: function () {
      $(this).text("jQuery is awesome!");
    },
  }); 
```

**Listing 12.4**     mouseenter and mouseleave Events

We now see the text change when you hover over it and change back when you move your mouse away. Also, notice that we were able to register two events (<samp class="listingcharacter">mouseenter</samp> and <samp class="listingcharacter">mouseleave</samp>) events under one selector using the <samp class="listingcharacter">.on()</samp> statement. This makes the syntax more readable as both these events are normally linked with each other and should naturally be grouped together. Inside each event handler function, we have made use of the <samp class="listingcharacter">this</samp> keyword, which refers to the context of the <samp class="listingcharacter">#text1</samp> selector that wraps our two mouse hover events. You could also swap the (<samp class="listingcharacter">this</samp>) keyword for <samp class="listingcharacter">#text1</samp>.

## 12.4    Changing HTML Elements

To change the text of our HTML element in the previous section, we use the <samp class="listingcharacter">.text()</samp> statement. Inside the brackets, we put the new text we want to change to. This is just one of the many methods jQuery has to change almost anything in the DOM. We can append text rather than replace it entirely by taking <samp class="listingcharacter">$("#text1").text()</samp> and replacing the <samp class="listingcharacter">.text()</samp> method with either <samp class="listingcharacter">.append()</samp> or <samp class="listingcharacter">prepend()</samp>. When we click the Press Me! button, the text will be added (either at the beginning or the end, depending on the method) rather than replace the text already there. The following would place the text at the end:

```
$("#text1").append("This text changed!"); 
```

You can place the text at the beginning via the following:

```
$("#text1").prepend("This text changed!"); 
```

Let’s try another real-world example with the jQuery newsletter sign-up form on our page. The newsletter form DOM elements are all wrapped in a <samp class="listingcharacter">div</samp> with an <samp class="listingcharacter programmingelement">id</samp> of <samp class="listingcharacter">form</samp>. We want the user to sign up for the newsletter by entering their email in the input and clicking the Submit button. When they click Submit, we want the form to disappear as there’s no need for it after they have signed up. We add the code from [Listing 12.5](#12_004.html_l12.5) to our <samp class="listingcharacter">$(document).ready()</samp> function.

```
$("#form-button").click(() => {
    $("#form-div").hide("slow");
  }); 
```

**Listing 12.5**     jQuery .hide() form

When clicking Submit, your entire form <samp class="listingcharacter">div</samp> gently disappears. The great thing is that the nice-looking animated action is achieved in three easy-to-read lines of code. We select the form button using the jQuery selector and register our click event <samp class="listingcharacter">$("#form-button").click()</samp>. Inside our click event, we use another jQuery selector to select our entire <samp class="listingcharacter">div</samp> and hide it using the <samp class="listingcharacter">slow</samp> speed <samp class="listingcharacter">$("#form-div").hide("slow")</samp>. You can even specify the number of milliseconds the hide animation should take to complete with <samp class="listingcharacter">$("#form-div").hide(1000)</samp>.

## 12.5    Adding and Removing Elements from the DOM

Our jQuery <samp class="listingcharacter">.hide()</samp> and <samp class="listingcharacter">.show()</samp> example is great if you want to hide and show elements like form inputs based on user input while keeping an entire form intact. However, it may be more beneficial in some scenarios to completely remove the element from the webpage and replace it with a brand-new element. In our case, it might be better to completely remove the form <samp class="listingcharacter">div</samp> and replace it with a new <samp class="listingcharacter">div</samp> that contains text telling us the form submission was successful. To do that, we replace the function from [Listing 12.5](#12_004.html_l12.5) with the function in [Listing 12.6](#12_005.html_l12.6).

```
$("#form-button").click(() => {
    let confirmationText =
      "<div><p>Thank you, your email was submitted.</p></div>";
    $("#form-div").remove();
    $("div:last").append(confirmationText);
  }); 
```

**Listing 12.6**     jQuery: Adding and Removing Elements

We fill in our email address and after clicking Submit, our entire form <samp class="listingcharacter">div</samp> is removed and a new <samp class="listingcharacter"><div></samp> tag containing a <samp class="listingcharacter"><p></samp> tag is added. Notice how we have used the selector <samp class="listingcharacter">$("div:last")</samp> to find the last <samp class="listingcharacter">div</samp> on our webpage and used the <samp class="listingcharacter">.append()</samp> method to add the new <samp class="listingcharacter">div</samp> just after it. Again, in very few lines of code, we have found the element we want, removed it, and added another new element in a specific location in the DOM.

## 12.6    Changing CSS

jQuery also extends to changing CSS properties or even adding new ones. Manipulating CSS on a webpage based on user input is a common requirement and something jQuery handles very elegantly. To demonstrate this, let’s add some CSS changes to our <samp class="listingcharacter">mouseenter</samp> event from [Listing 12.4](#12_003.html_l12.4) to change the background color and font, as shown in [Listing 12.7](#12_006.html_l12.7). Notice how we can chain the jQuery statements together using the <samp class="listingcharacter">.</samp> notation.

```
$("#text1").on({
    mouseenter: function () {
      $(this)
        .text("Hey! You hovered over me!")
        .css("background-color", "DodgerBlue")
        .css("color", "white");
    },
    mouseleave: function () {
      $(this)
        .text("jQuery is awesome!")
        .css("background-color", "")
        .css("color", "");
    },
  }); 
```

**Listing 12.7**     jQuery CSS Methods

When hovering over our <samp class="listingcharacter">"jQuery is awesome!"</samp> text, we see the hover text background changes to blue and the font color changes to white, as in [Figure 12.2](#12_006.html_f12.2). jQuery method chaining is an especially useful way of changing multiple parts of an HTML element in one place.

[![jQuery Hover](bilderklein/klein12_002.png)](img-f12.2.html)

**Figure 12.2**     jQuery Hover

## 12.7    jQuery AJAX

We can use jQuery methods to make AJAX queries to external data, just like we did in [Section 11](#11_001.html_h11). jQuery abstracts much of the complexity of these queries and returns what we need to continue our logic. The jQuery syntax is illustrated in [Listing 12.8](#12_007.html_l12.8).

```
 $("some-button").click(() => {
    $.get("https://example.com", (data, status) => {
      // Some logic
    });
  }); 
```

**Listing 12.8**     jQuery AJAX Syntax

We have our regular jQuery selector and event <samp class="listingcharacter">$("some-button").click()</samp> inside, which we call our jQuery AJAX HTTP GET method <samp class="listingcharacter">$.get()</samp>, passing in the endpoint URL. We then specify a callback function <samp class="listingcharacter">(data, status) => {}</samp> with the parameters <samp class="listingcharacter">data</samp> being the data returned from the request and <samp class="listingcharacter">status</samp> being the HTTP response status (i.e., 200 if successful).

In our example, we add the code from [Listing 12.9](#12_007.html_l12.9) to the <samp class="listingcharacter">$("#form-button").click()</samp> method to call the data from our file test_data.json and display it in an alert as part of our email submission logic. We also make sure to copy the test_data.json file from [Section 11.1](#11_001.html_h11.1) into the current folder where the app.js file is located for this example.

```
$.get("test_data.json", (data, status) => {
      alert(`Congratulations! You've won a ${data[0]["make"]}!`);
    }); 
```

**Listing 12.9**     jQuery AJAX Example

We then enter our email in the form, click Submit, and we see an alert popup that says “Congratulations! You've won a Mercedes!” as shown in [Figure 12.3](#12_007.html_f12.3).

[![jQuery GET Call](bilderklein/klein12_003.png)](img-f12.3.html)

**Figure 12.3**     jQuery GET Call

This scenario is where jQuery really shines, because we were able to set up a click event, add and remove elements, call external data, use that data in an alert (doing so asynchronously), and all of this in no more than nine lines of code. You can imagine the power of jQuery in just about any scenario where you need your webpage to react to user input.

# 13    Web APIs

An API is a way for developers to interact with something complex in an easier way with easier syntax. APIs are a vast topic in JavaScript, so we are going to focus on an area of APIs called web APIs. Web APIs are nothing more than web-based interfaces that offer a set of ways (like methods) you can use to interact with things and request data that can be used in your app. Web APIs are a core feature of JavaScript development and allow you to leverage particularly useful tools that fall within another concept called browser APIs. Browser APIs are interfaces specific to the browser and allow us to interact with the device the browser is running on, and they form an interface that lets our JavaScript code securely access resources outside of our app. Some of the more common APIs used are browser history, geolocation, and browser storage.

In this section, we’ll explore how web APIs facilitate browser navigation, geolocation, and browser storage.

## 13.1    Browser Navigation and History

When people interact with your app, they are likely going to need to navigate from one page to another and, at some point, navigate to the page they came from. Your app needs to provide a stable way for this navigation between pages to happen. This is where the History API comes into play. You can use the browser’s window object to call either the location or history object to navigate a user from one page to another. Say we have two webpages, the first page being index.html as shown in [Listing 13.1](#13_001.html_l13.1), and the second page being detail.html as shown in [Listing 13.2](#13_001.html_l13.2). To navigate between them, you can use the JavaScript example shown in [Listing 13.3](#13_001.html_l13.3), where we set up two functions that use the <samp class="listingcharacter">window.location</samp> call to navigate to the detail.html page and the <samp class="listingcharacter">window.history</samp> call to navigate back in the browser’s history to the index.html page.

```
<!DOCTYPE html>
<head>
    <script src="app.js"></script>
    <title>Document</title>
</head>
<body>
    <h1>Home Page</h1>
    <button onclick="navigateToDetailPage()">Detail Page</button>
</body>
</html> 
```

**Listing 13.1**     index.html

```
<!DOCTYPE html>
<head>
    <script src="app.js"></script>
    <title>Document</title>
</head>
<body>
    <h1>Detail Page</h1>
    <button onclick="goBack()">Go Back!</button>
</body>
</html> 
```

**Listing 13.2**     detail.html

```
const navigateToDetailPage = () => {
  window.location = "detail.html";
};

const goBack = () => {
  window.history.back();
}; 
```

**Listing 13.3**     app.js

On our homepage, click Detail Page and navigate to our detail.html page using the <samp class="listingcharacter">navigateToDetailPage()</samp> function that uses the <samp class="listingcharacter">window</samp> object to change the <samp class="listingcharacter">.location</samp> to <samp class="listingcharacter">detail.html,</samp> which is then loaded into the browser, as shown in [Figure 13.1](#13_001.html_f13.1) and [Figure 13.2](#13_001.html_f13.2).

On the Detail Page, click Go back! and navigate to the index.html page. This is done using the same window object, but using the <samp class="listingcharacter">.history</samp> object instead on which we call the method <samp class="listingcharacter">.back()</samp>, which takes us to the previous page in our browser’s history, index.html.

[![Home Page](bilderklein/klein13_001.png)](img-f13.1.html)

**Figure 13.1**     Home Page

[![Detail Page](bilderklein/klein13_002.png)](img-f13.2.html)

**Figure 13.2**     Detail Page

## 13.2    Geolocation

Another popular API is the Geolocation API, which, as the name suggests, is used to find the location of the device the app is running on. The quickest way for your browser to find your location is by your IP or Wi-Fi signal, but when your app tries to get the user’s location, a small popup window will normally appear, asking the user to confirm if the browser can use geolocation for your app.

To use geolocation, we add the code from [Listing 13.4](#13_002.html_l13.4) into our app.js file from [Listing 13.3](#13_001.html_l13.3) and add a new button <samp class="listingcharacter"><button onclick=" alertLocation()">Show Location</button></samp> to our index.html page, shown previously in [Listing 13.1](#13_001.html_l13.1), to call the new function as shown in [Listing 13.4](#13_002.html_l13.4).

```
const alertLocation = () => {
  if ("geolocation" in navigator) {
    navigator.geolocation.getCurrentPosition((location) => {
      alert(
        `I am at ${location.coords.latitude} latitude by ${location.coords.longitude} longitude`
      );
    });
  } else {
    console.log("No geolocation available.");
  }
}; 
```

**Listing 13.4**     Geolocation API

Click Show Location and then click Allow when the browser geolocation permission popup appears, as shown in [Figure 13.3](#13_002.html_f13.3). We then see a JavaScript alert with your longitude and latitude as part of the text, which is a straightforward way to access the browser’s geolocation functionality and incorporate it into your JavaScript code.

[![Browser Geolocation Permission Alert](bilderklein/klein13_003.png)](img-f13.3.html)

**Figure 13.3**     Browser Geolocation Permission Alert

## 13.3    Browser Storage

Modern browsers like Chrome, Firefox, and Safari all have something called browser storage, where they store certain data when you visit a webpage. Depending on the type of browser storage used, the data might be kept or deleted after you close the webpage or browser window. There are many different reasons for storing data in the browser, from identification to security and even preference data.

Your browser storage options include local storage, which persists between sessions (when you close your webpage); session storage data that expires when you close the webpage; and cookies and database storage. For simplicity, we focus on using JavaScript to save some data to the browser’s local storage and view it when we refresh the page.

Before we continue, navigate to your browser’s developer console (we use Chrome in our example) and look for the Application tab, as shown in [Figure 13.4](#13_003.html_f13.4).

Under the Application tab, you will see a section called Storage. Under that, you will see Local Storage with your webpage underneath it, ready to store data and be used across sessions.

[![Chrome DevTools: Local Storage](bilderklein/klein13_004.png)](img-f13.4.html)

**Figure 13.4**     Chrome DevTools: Local Storage

Now, we add the code from [Listing 13.5](#13_003.html_l13.5) to our <samp class="listingcharacter">alertLocation()</samp> function (shown previously in [Listing 13.4](#13_002.html_l13.4)), below the <samp class="listingcharacter">alert()</samp>. When we click Show Location, we see the geolocation alert, and after clicking OK, we store the latitude data in our browser’s local storage as shown in [Listing 13.5](#13_003.html_l13.5).

```
if (!localStorage.getItem("latitude")) {
    localStorage.setItem("latitude", location.coords.latitude);
  } else {
    alert("Latitude is already stored on this browser.");
  } 
```

**Listing 13.5**     Browser Storage

Make sure the Application tab is open in Chrome DevTools as per [Figure 13.4](#13_003.html_f13.4), where there are currently no entries. With Chrome DevTools open, click Show Location and after clicking OK in the alert, you will see the latitude appear in the local storage, as shown under the Value column in [Figure 13.5](#13_003.html_f13.5).

[![Local Storage with Values](bilderklein/klein13_005.png)](img-f13.5.html)

**Figure 13.5**     Local Storage with Values

Refresh the page and see the latitude entry has persisted in the browser’s local storage. If we saved the latitude under session storage, the value would have been deleted after closing the browser window.

# 14    Debugging and Error Handling

Error handling in JavaScript plays a key role in development, and many techniques you use in your ABAP code can be directly translated to JavaScript, albeit with slightly different syntax. Due to JavaScript’s loose typing system, many errors will not be caught until runtime, so you should plan ahead for them.

When it comes to debugging, vanilla JavaScript does not have a tool like the much-loved ABAP debugger bundled with it. Your scenario and personal preference will dictate which tools you use. In our case, we make use of Chrome DevTools and the built-in debugger inside VS Code. There are many other debugging tools available, but these two are widely used and well documented. Alongside these tools, we also use the <samp class="listingcharacter">console.log()</samp> statement as part of your debugging strategy to log values to the console. This allows us to follow the output of our logic as the code executes to help spot any issues.

In the following sections, we’ll discuss some common types of errors and how they are viewed, before walking through the two key debugging tools and error handling in JavaScript.

## 14.1    Error Types and Views

There are many error types and scenarios, but they are beyond the scope of this E-Bite. Some of the more common errors you will come across include those shown in [Table 14.1](#14_001.html_t14.1).

| Error | Example |
| --- | --- |
| <samp class="listingcharacter">Uncaught TypeError: Cannot Read Property ’property-name’ of undefined</samp> | E.g., calling an attribute that is undefined. |
| <samp class="listingcharacter">ReferenceError: newaCr is not defined…</samp><samp class="listingcharacter">test-errors.js:9:16)</samp> | E.g., calling a method of an object that doesn’t exist yet. |
| <samp class="listingcharacter">Uncaught TypeError: Cannot set property ’innerHTML’ of null…</samp> | E.g., when your JavaScript code executes before the DOM is fully loaded and the element does not exist yet. |

**Table 14.1**     Some Common JavaScript Errors

Most of these errors will indicate where the error is coming from, including the file name and line number where the error occurred, as shown in [Listing 14.1](#14_001.html_l14.1).

```
console.log(`${newaCr.make}`);
               ^
ReferenceError: newaCr is not defined
    at Object.<anonymous> (C:\users\public\car.js:9:16) 
```

**Listing 14.1**     JavaScript Reference Error

The error in [Listing 14.1](#14_001.html_l14.1) happened at the <samp class="listingcharacter">console.log()</samp> statement, and occurred because the <samp class="listingcharacter">newaCr</samp> object is not defined (because of a typo). We see the file location <samp class="listingcharacter">C:\users\public\car.js</samp> with the line number and characters from the left, respectively, <samp class="listingcharacter">9:16 (C:\users\public\car.js:9:16),</samp> so we know exactly where the offending code is. If we are working in the browser, our errors are displayed in the browser’s console area (see [Figure 14.1](#14_001.html_f14.1)), and if we are working on a server-side Node.js app, for example, then in the terminal window (see [Figure 14.2](#14_001.html_f14.2)).

[![Errors in the Browser](bilderklein/klein14_001.png)](img-f14.1.html)

**Figure 14.1**     Errors in the Browser

[![Errors in VS Code Terminal](bilderklein/klein14_002.png)](img-f14.2.html)

**Figure 14.2**     Errors in VS Code Terminal

## 14.2    Debugging

The nature of JavaScript with its dynamic typing system means you will see many bugs that give you no indication of what has gone wrong, and you will need to place that important breakpoint in your code. In VS Code, you can place a breakpoint at the offending line of code, or you can use the using the <samp class="listingcharacter">debugger;</samp> statement, which is like the <samp class="listingcharacter">BREAK-POINT</samp> statement in ABAP. You can then hit these breakpoints using the built-in debugger in your IDE (VS Code, in our case) or hit your breakpoint in your browser’s developer tools panel (Chrome DevTools, in our case).

We’ll take a closer look at both tools in the following sections.

### Debugging with Chrome DevTools

Most major browsers have their own set of debugging tools, but we are introducing the concept using Chrome’s built-in debugging tools because they are among the best. To begin, we trigger our first JavaScript breakpoint using the <samp class="listingcharacter">debugger;</samp> statement and see what options we have in the browser. [Listing 14.2](#14_002.html_l14.2) shows a standard HTML page that references the JavaScript code in [Listing 14.3](#14_002.html_l14.3), which is where we’ll place our breakpoint. In [Listing 14.3](#14_002.html_l14.3), we placed a <samp class="listingcharacter">debugger;</samp> statement (our breakpoint) just before the <samp class="listingcharacter">alertText</samp> variable assignment.

```
<!DOCTYPE html>
<head>
    <title>Document</title>
    <script src="app.js"></script>
</head>

<body>
    <h1>Let’s do some debugging!</h1>
    <button id="button1" onclick="onButtonClick()">Press Me!</button>
</body>
</html> 
```

**Listing 14.2**     index.html

```
const onButtonClick = () => {
  debugger;
  let alertText = "Button clicked!";
  alert(alertText);
}; 
```

**Listing 14.3**     app.js

We run our webpage from [Listing 14.2](#14_002.html_l14.2), and when we click Press Me!, we do not trigger our breakpoint. That is because to trigger the breakpoint, we need to have Chrome DevTools open. Press [F12] or right-click and click Inspect in the context menu. Once the DevTools are open, refresh the page and click Press Me! again. Our browser screen dims, and we now see the code from our app.js file in the Sources tab and our <samp class="listingcharacter">debugger;</samp> statement highlighted with our code execution stopped at that breakpoint, as shown in [Figure 14.3](#14_002.html_f14.3).

Although the interface in [Figure 14.3](#14_002.html_f14.3) is a bit different, the process of debugging is much the same as ABAP. You see your code at the top right with a file explorer on the left showing your index.html and app.js files, with a few different sections underneath. You can see the Call Stack, which shows we are in the <samp class="listingcharacter">onButtonClick()</samp> function. You will also see the Scope section toward the right side, which holds our undefined <samp class="listingcharacter">alertText</samp> variable that we are now going to assign some text.

[![Chrome DevTools: Debugging](bilderklein/klein14_003.png)](img-f14.3.html)

**Figure 14.3**     Chrome DevTools: Debugging

Just like with the ABAP debugger, we can step through our code. Use the buttons toward the top middle of the browser or in Chrome DevTools above the Breakpoints section. Click the Step over next function button [F10] twice to step onto and over the <samp class="listingcharacter">alertText</samp> variable assignment, and watch how our local variable is assigned text in both the Scope section and the code view area in [Figure 14.4](#14_002.html_f14.4).

Before we continue, in [Figure 14.5](#14_002.html_f14.5), we change our <samp class="listingcharacter">alertText</samp> variable to I changed this text by double-clicking the Button Clicked! text in the Scope section, entering the new text, and pressing [Enter]. We then click the blue Resume script execution button [F8] to continue through our code where we see our alert with the updated text.

This is just the tip of the iceberg, and there is much more we can do when debugging in Chrome DevTools, going beyond code execution all the way to testing speed, performance, and even how well our app runs on other devices like mobile phones and tablets.

[![Chrome DevTools: Step Through Code](bilderklein/klein14_004.png)](img-f14.4.html)

**Figure 14.4**     Chrome DevTools: Step Through Code

[![Changing Variables](bilderklein/klein14_005.png)](img-f14.5.html)

**Figure 14.5**     Changing Variables

### Debugging in VS Code

You can also use your IDE to debug your code, and we are going to use the debugger in VS Code. This debugging tool more closely resembles the ABAP debugger, but the flow and interface are a bit different and may take some getting used to. The other benefit to debugging in VS Code is you can install many extensions to make things easier, including ones already available for pure ABAP. Let’s use Node.js to run the code from [Listing 14.4](#14_002.html_l14.4) and step through it using VS Code’s built-in debugger.

```
class car {
  constructor(make) {
    this.make = make;
  }
}

let newCar = new car("mercedes");
console.log(`${newCar.maek}`); 
```

**Listing 14.4**     fix-me.js

We run the code, and should see <samp class="listingcharacter">"Mercedes"</samp> logged to the console, but instead see <samp class="listingcharacter">undefined</samp> logged to the console. We place a breakpoint on our variable assignment and step through our code from there. Just like in the ABAP debugger, you can place a breakpoint by clicking in the left-hand column of the code editor, and we do the same at the line where we assign our <samp class="listingcharacter">newCar</samp> variable. We now see a red dot in [Figure 14.6](#14_002.html_f14.6), like in the ABAP debugger.

[![VS Code Breakpoint](bilderklein/klein14_006.png)](img-f14.6.html)

**Figure 14.6**     VS Code Breakpoint

Now that the breakpoint is set, click the Run and Debug button [Ctrl] + [Shift] + [D] in the left column of the VS Code window. Once we are in the debugging window, click the Run and Debug button and select Node.js as our environment from the dropdown. That runs our code and stops at the breakpoint we set. In our VS Code debugger window, we can see similar sections to Chrome DevTools. In [Figure 14.7](#14_002.html_f14.7), we have our VARIABLES, CALL STACK, and BREAKPOINTS sections on the left, and our code and DEBUG CONSOLE on the right.

[![VS Code Debugger](bilderklein/klein14_007.png)](img-f14.7.html)

**Figure 14.7**     VS Code Debugger

We step through our variable assignment by clicking the Step Over [F10] button once. At the bottom of the DEBUG CONSOLE, we type in <samp class="listingcharacter">newCar.make</samp> and see the output <samp class="listingcharacter">Mercedes</samp>, as shown in [Figure 14.8](#14_002.html_f14.8).

[![VS Code Debug Console: Variable Test](bilderklein/klein14_008.png)](img-f14.8.html)

**Figure 14.8**     VS Code Debug Console: Variable Test

This means our object is instantiating correctly, so the problem must lie in our <samp class="listingcharacter">console.log()</samp> statement. If we look closely, we see we misspelled the attribute as <samp class="listingcharacter">.maek</samp>. Run through the rest of the code execution by clicking the Continue [F5] button and correcting the error.

This is just a small part of what can be done using a built-in debugger like the one bundled with VS Code and, just like the ABAP debugger, it will become a tool you cannot live without.

## 14.3    Error Handling

In JavaScript, you can expect many unforeseen errors, and even though you have some great tools to debug your code, it is crucial that you implement proper error handling as well. As with all programming languages, proper error handling is key to building a stable and robust application.

Certain scenarios in ABAP can be handled by a simple <samp class="listingcharacter">IF</samp> statement if you know what errors to expect. However, there are scenarios where you need to play it safe with a <samp class="listingcharacter">TRY CATCH</samp> block. To introduce you to error handling in JavaScript, we replicate an ABAP <samp class="listingcharacter">TRY CATCH</samp> block and log a response to the console if we catch an error.

In [Listing 14.5](#14_003.html_l14.5), we wrap our corrected variable assignment shown previously in [Listing 14.4](#14_002.html_l14.4) in a <samp class="listingcharacter">try…catch</samp> statement:

```
try {
  let newCar = new car("Mercedes");
  console.log(`${newCar.make}`);
} catch {
  console.log("Something went wrong");
} 
```

**Listing 14.5**     fix-me.js: try…catch

We run the code and see <samp class="listingcharacter">Mercedes</samp> logged to the console. We then break our code by logging the car object name (with a typo) to the console, as follows:

```
console.log(`${newaCr.make}`); 
```

We run our app again and we see the text <samp class="listingcharacter">Something went wrong</samp> from our <samp class="listingcharacter">catch</samp> statement logged to the console, as there is no object called <samp class="listingcharacter">newaCr</samp>.

With this, we’ve concluded our discussion of debugging and error handling in JavaScript. You’re now ready to begin coding with JavaScript!

# 15    What’s Next?

You’ve mastered the JavaScript programming basics—now continue coding with SAP! Learn about the SAPUI5 user interface, explore cloud-native application development, or broaden your ABAP horizons and sharpen your code with clean coding tips. See where programming with SAP PRESS can take you!

![](bilderklein/klein1900.png)

###### Recommendation from Our Editors

Design, enhance, and deploy applications with SAPUI5: The Comprehensive Guide by Paul Modderman, Christiane Goebels, Denise Nepraunig, and Thilo Seidel! Get the know-how to develop MVC apps, use OData, create data bindings, debug and test code, and deploy apps. Learn the dos and don’ts of SAPUI5, whether you’re implementing CRUD or writing your own controls.

Visit www.sap-press.com/4987 to learn more about SAPUI5: The Comprehensive Guide!

In addition to this book, our editors picked a few other SAP PRESS publications that you might also be interested in. Check out the next page to learn more!

# More from SAP PRESS

| ![](bilderklein/klein1761.png) | ABAP to the FutureStay on the cutting edge of ABAP technology! See what’s new with the latest ABAP releases, including abapGit and transporting objects between systems, ABAP SQL, the RESTful ABAP programming model, and test tools for core data services, SAPUI5, and more. Take your ABAP coding to the next level!864 pages, 3^(rd) edition, pub. 02/2019 E-book: $69.99 &#124; Print: $79.95 &#124; Bundle: $89.99
www.sap-press.com/4751 |

| ![](bilderklein/klein1747.png) | SAP Cloud Platform: Cloud-Native DevelopmentLearn to build cloud applications from the ground up using SAP Cloud Platform! Explore the Neo and Cloud Foundry environments, pick your backend language, and create a frontend with SAPUI5, SAP Fiori, and more. Secure, test, and monitor your application before delivery and implementation.489 pages, pub. 12/2018 E-book: $69.99 &#124; Print: $79.95 &#124; Bundle: $89.99
www.sap-press.com/4713 |

| ![](bilderklein/klein2026.png) | Clean ABAP: A Style Guide for DevelopersAre you looking to clean up your code? This official companion to the Clean ABAP GitHub repository is brimming with best practices to help you write effective ABAP code. Dive into detailed code examples and explanations for using classes, methods, names, variables, internal tables, and more.351 pages, pub. 11/2020 E-book: $69.99 &#124; Print: $79.95 &#124; Bundle: $99.99
www.sap-press.com/5190 |

# Usage, Service, and Legal Notes

## Notes on Usage

This E-Bite is protected by copyright. By purchasing this E-Bite, you have agreed to accept and adhere to the copyrights. You are entitled to use this E-Bite for personal purposes. You may print and copy it, too, but also only for personal use. Sharing an electronic or printed copy with others, however, is not permitted, neither as a whole nor in parts. Of course, making them available on the internet or in a company network is illegal.

For detailed and legally binding usage conditions, please refer to the section [Legal Notes](#usage_service_notes.html_legal_notes).

This E-Bite copy contains a digital watermark, a signature that indicates which person may use this copy.

## Service Pages

The following sections contain notes on how you can contact us.

### Praise and Criticism

We hope that you enjoyed reading this E-Bite. If it met your expectations, please do recommend it. If you think there is room for improvement, please get in touch with the editor of the E-Bite: [Megan Fuerst](mailto:meganf@rheinwerk-publishing.com).

We welcome every suggestion for improvement but, of course, also any praise! You can also share your reading experience via Twitter, Facebook, or email.

### Technical Issues

If you experience technical issues with your e-book or e-book account at SAP PRESS, please feel free to contact our reader service: [support@rheinwerk-publishing.com](mailto:support@rheinwerk-publishing.com).

## Legal Notes

This section contains the detailed and legally binding usage conditions for this E-Bite.

### Copyright Note

This publication is protected by copyright in its entirety. All usage and exploitation rights are reserved by the author and Rheinwerk Publishing; in particular the right of reproduction and the right of distribution, be it in printed or electronic form.
© 2021 by Rheinwerk Publishing Inc., Boston (MA)

### Your Rights as a User

You are entitled to use this E-Bite for personal purposes only. In particular, you may print the E-Bite for personal use or copy it as long as you store this copy on a device that is solely and personally used by yourself. You are not entitled to any other usage or exploitation.

In particular, it is not permitted to forward electronic or printed copies to third parties. Furthermore, it is not permitted to distribute the E-Bite on the internet, in intranets, or in any other way or make it available to third parties. Any public exhibition, other publication, or any reproduction of the E-Bite beyond personal use are expressly prohibited. The aforementioned does not only apply to the E-Bite in its entirety but also to parts thereof (e.g., charts, pictures, tables, sections of text). Copyright notes, brands, and other legal reservations as well as the digital watermark may not be removed from the E-Bite.

### Digital Watermark

This E-Bite copy contains a digital watermark, a signature that indicates which person may use this copy. If you, dear reader, are not this person, you are violating the copyright. So please refrain from using this E-Bite and inform us about this violation. A brief email to [info@rheinwerk-publishing.com](mailto:info@rheinwerk-publishing.com) is sufficient. Thank you!

### Limitation of Liability

Regardless of the care that has been taken in creating texts, figures, and programs, neither the publisher nor the author, editor, or translator assume any legal responsibility or any liability for possible errors and their consequences.

# Imprint

This E-Bite is a publication many contributed to, specifically:

Editor   Megan Fuerst
Acquisitions Editor   Hareem Shafi
Copyeditor   Brandon Nolta
Cover Design   Graham Geary
   Icon made by Freepik from www.flaticon.com
Production E-Book   Graham Geary
Typesetting E-Book   III-satz, Husby (Germany)

ISBN 978-1-4932-2155-4

© 2021 by Rheinwerk Publishing Inc., Boston (MA)
1st edition 2021

All rights reserved. Neither this publication nor any part of it may be copied or reproduced in any form or by any means or translated into another language, without the prior consent of Rheinwerk Publishing, 2 Heritage Drive, Suite 305, Quincy, MA 02171.

Rheinwerk Publishing makes no warranties or representations with respect to the content hereof and specifically disclaims any implied warranties of merchantability or fitness for any particular purpose. Rheinwerk Publishing assumes no responsibility for any errors that may appear in this publication.

“Rheinwerk Publishing” and the Rheinwerk Publishing logo are registered trademarks of Rheinwerk Verlag GmbH, Bonn, Germany. SAP PRESS is an imprint of Rheinwerk Verlag GmbH and Rheinwerk Publishing, Inc.

All of the screenshots and graphics reproduced in this E-Bite are subject to copyright © SAP SE, Dietmar-Hopp-Allee 16, 69190 Walldorf, Germany.

SAP, ABAP, ASAP, Concur Hipmunk, Duet, Duet Enterprise, ExpenseIt, SAP ActiveAttention, SAP Adaptive Server Enterprise, SAP Advantage Database Server, SAP ArchiveLink, SAP Ariba, SAP Business ByDesign, SAP Business Explorer (SAP BEx), SAP BusinessObjects, SAP BusinessObjects Explorer, SAP BusinessObjects Web Intelligence, SAP Business One, SAP Business Workflow, SAP BW/4HANA, SAP C/4HANA, SAP Concur, SAP Crystal Reports, SAP EarlyWatch, SAP Fieldglass, SAP Fiori, SAP Global Trade Services (SAP GTS), SAP GoingLive, SAP HANA, SAP Jam, SAP Leonardo, SAP Lumira, SAP MaxDB, SAP NetWeaver, SAP PartnerEdge, SAPPHIRE NOW, SAP PowerBuilder, SAP PowerDesigner, SAP R/2, SAP R/3, SAP Replication Server, SAP Roambi, SAP S/4HANA, SAP S/4HANA Cloud, SAP SQL Anywhere, SAP Strategic Enterprise Management (SAP SEM), SAP SuccessFactors, SAP Vora, TripIt, and Qualtrics are registered or unregistered trademarks of SAP SE, Walldorf, Germany.

All other products mentioned in this E-Bite are registered or unregistered trademarks of their respective companies.