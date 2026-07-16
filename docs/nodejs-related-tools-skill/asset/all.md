![](cover.jpeg)

![](index-1_1.jpg)

![](index-2_1.png)

HisN

tor o

y de.js: Related Tools & Skills

Copyright © 2018 SitePoint Pty. Ltd.

Topics

Cover Design: Alex Walker

Tutorials

Off N

ers o

& t

D i

e c

als e of Rights

All rights reserved. No part of this book may be reproduced, stored in a retrieval system Hi o

ghrli tgrhatsnsmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical articles or reviews.

Settings

Su N

ppoo

rt tice of Liability

The author and publisher have made every effort to ensure the accuracy of the Sign Out

information herein. However, the information contained in this book is sold without warranty, either express or implied. Neither the authors and SitePoint Pty. Ltd., nor its dealers or distributors will be held liable for any damages to be caused either directly or indirectly by the instructions contained in this book, or by the software or hardware products described herein.

Trademark Notice

Rather than indicating every occurrence of a trademarked name as such, this book uses the names only in an editorial fashion and to the benefit of the trademark owner with no intention of infringement of the trademark.

Published by SitePoint Pty. Ltd.

48 Cambridge Street Collingwood

VIC Australia 3066

Web: www.sitepoint.com

Email: books@sitepoint.com

About SitePoint

SitePoint specializes in publishing fun, practical, and easytounderstand content for web professionals. Visit http://www.sitepoint.com/ to access our blogs, books, newsletters, articles, and community forums. You’ll find a stack of information on JavaScript, PHP, design, and more.

Playlists

HisP

tor ryeface

To W

pic h

s ile there have been quite a few attempts to get JavaScript working as a serverside language, Node.js (frequently just called Node) has been the first environment that's Tu g

toariin

al e

s d any traction. It's now used by companies such as Netflix, Uber and Paypal to power their web apps. Node allows for blazingly fast performance; thanks to its event Off lo

er o

s p

& m

Deaolsdel, common tasks like network connection and database I/O can be executed very quickly indeed.

Highlights

From a beginner's point of view, one of Node's obvious advantages is that it uses SetJtianvga

s Script, a ubiquitous language that many developers are comfortable with. If you can write JavaScript for the clientside, writing serverside applications with Node Su s

p h

poortuld not be too much of a stretch for you.

Sig Inn O tuhtis book, we'll take a look at a selection of the related tools and skills that will make you a much more productive Node developer.

Who Should Read This Book?

This book is for anyone who wants to start learning serverside development with Node.js. Familiarity with JavaScript is assumed, but we don't assume any previous backend development experience.

Conventions Used

CODE SAMPLES

Code in this book is displayed using a fixedwidth font, like so:

<h1>A Perfect Summer's Day</h1>

<p>It was a lovely day for

. a walk in the park.

The birds were singing and the kids were all back at school.</p>

Where existing code is required for context, rather than repeat all of it, ⋮ will be displayed:

function animate() {

⋮

new_variable = "Hello";

}

Some lines of code should be entered on one line, but we’ve had to wrap them because of page constraints. An ➥ indicates a line break that exists for formatting purposes only, and should be ignored:

URL.open("http://www.sitepoint.com/responsiveweb

➥designrealusertesting/?responsive1");

You’ll notice that we’ve used certain layout styles throughout this book to signify different types of information. Look out for the following items.

TIPS, NOTES, AND WARNINGS

Hey, You!

Tips provide helpful little pointers.

Ahem, Excuse Me ...

Notes are useful asides that are related—but not critical—to the topic at hand. Think of them as extra tidbits of information.

Make Sure You Always ...

... pay attention to these important points.

Watch Out!

Warnings highlight any gotchas that are likely to trip you up along the way.

HisC

tor h

y apter 1: Unit Test Your JavaScript Using

To M

pics ocha and Chai

Tu B

torYia lJ

s ANI HARTIKAINEN

Have you ever made some changes to your code, and later found it caused something Offers & Deals

else to break?

Highlights

I'm sure most of us have. This is almost inevitable, especially when you have a larger amount of code. One thing depends on another, and then changing it breaks something Settings

else as a result.

Support

But what if that didn't happen? What if you had a way of knowing when something breaks as a result of some change? That would be pretty great. You could modify your Sign Out

code without having to worry about breaking anything, you'd have fewer bugs and you'd spend less time debugging.

That's where unit tests shine. They will *automatically* detect any problems in the code for you. Make a change, run your tests and if anything breaks, you'll immediately know what happened, where the problem is *and* what the correct behavior should be. This completely eliminates any guesswork!

In this article, I'll show you how to get started unit testing your JavaScript code. The examples and techniques shown in this article can be applied to both browserbased code and Node.js code.

The code for this tutorial is available from our GitHub repo.

What Is Unit Testing

W

h en yo u te st your c odeb, ase, you t ake a piece of code — t ypically a function — and verify it behaves correctly in a specific situation. Unit testing is a structured and automated way of doing this. As a result, the more tests you write, the bigger the benefit

you receive. You will also have a greater level of confidence in your codebase as you continue to develop it.

The core idea with unit testing is to test a function's behavior when giving it a certain set of inputs. You call a function with certain parameters, and check you got the correct result.

// Given 1 and 10 as inputs...

var result = Math.max(1, 10);

// ...we should receive 10 as the output

if(result !== 10) {

throw new Error('Failed');

}

In practice, tests can sometimes be more complex. For example, if your function makes an Ajax request, the test needs some more set up, but the same principle of "given certain inputs, we expect a specific outcome" still applies.

Setting up the Tools

For this article, we'll be using Mocha. It's easy to get started with, can be used for both browserbased testing and Node.js testing, and it plays nicely with other testing tools.

The easiest way to install Mocha is through npm (for which we also need to install Node.js). If you're unsure about how to install either npm or Node on your system, consult our tutorial: A Beginner's Guide to npm — the Node Package Manager With Node installed, open up a terminal or command line in your project's directory.

If you want to test code in the browser, run npm install mocha chai savedev If you want to test Node.js code, in addition to the above, run npm install g mocha

This installs the packages mocha and chai. Mocha is the library that allows us to run tests, and Chai contains some helpful functions that we'll use to verify our test results.

TESTING ON NODE.JS VS TESTING IN THE BROWSER

The examples that follow are designed to work if running the tests in a browser. If you

want to unit test your Node.js application, follow these steps.

For Node, you don't need the test runner file.

To include Chai, add var chai = require('chai'); at the top of the test file.

Run the tests using the mocha command, instead of opening a browser.

Setting up a Directory Structure

You should put your tests in a separate directory from your main code files. This makes it easier to structure them, for example if you want to add other types of tests in the future (such as integration tests or functional tests).

The most popular practice with JavaScript code is to have a directory called test/ in your project's root directory. Then, each test file is placed under test/someModuleTest.js. Optionally, you can also use directories inside test/, but I recommend keeping things simple — you can always change it later if necessary.

Setting up a Test Runner

In order to run our tests in a browser, we need to set up a simple HTML page to be our *test runner* page. The page loads Mocha, the testing libraries and our actual test files.

To run the tests, we'll simply open the runner in a browser.

If you're using Node.js, you can skip this step. Node.js unit tests can be run using the command mocha, assuming you've followed the recommended directory structure.

Below is the code we'll use for the test runner. I'll save this file as testrunner.html.

<!DOCTYPE html>

<html>

<head>

<title>Mocha Tests</title>

<link rel="stylesheet" href="node_modules/mocha/mocha.css">

</head>

<body>

<div id="mocha"></div>

<script src="node_modules/mocha/mocha.js"></script>

<script src="node_modules/chai/chai.js"></script>

<script>mocha.setup('bdd')</script>

<! load code you want to test here >

<! load your test files here >

<script>

mocha.run();

</script>

</body>

</html>

The important bits in the test runner are:

We load Mocha's CSS styles to give our test results nice formatting.

We create a div with the ID mocha. This is where the test results are inserted.

We load Mocha and Chai. They are located in subfolders of the node_modules folder since we installed them via npm.

By calling mocha.setup, we make Mocha's testing helpers available.

Then, we load the code we want to test and the test files. We don't have anything here just yet.

Last, we call mocha.run to run the tests. Make sure you call this *after* loading the source and test files.

The Basic Test Building Blocks

Now that we can run tests, let's start writing some.

We'll begin by creating a new file test/arrayTest.js. An individual test file such as this one is known as a *test case*. I'm calling it arrayTest.js because for this example, we'll be testing some basic array functionality.

Every test case file follows the same basic pattern. First, you have a describe block: describe('Array', function() {

// Further code for tests goes here

});

describe is used to group individual tests. The first parameter should indicate what we're testing — in this case, since we're going to test array functions, I've passed in the string 'Array'.

Secondly, inside the describe, we'll have it blocks:

describe('Array', function() {

it('should start empty', function() {

// Test implementation goes here

});

// We can have more its here

});

it is used to create the actual tests. The first parameter to it should provide a humanreadable description of the test. For example, we can read the above as "it should start empty", which is a good description of how arrays should behave. The code to implement the test is then written inside the function passed to it.

All Mocha tests are built from these same building blocks, and they follow this same basic pattern.

First, we use describe to say what we're testing for example, "describe how array should work".

Then, we use a number of it functions to create the individual tests each it should explain one specific behavior, such as "it should start empty" for our array case above.

Writing the Test Code

Now that we know how to structure the test case, let's jump into the fun part —

implementing the test.

Since we are testing that an array should start empty, we need to create an array and then ensure it's empty. The implementation for this test is quite simple: var assert = chai.assert;

describe('Array', function() {

it('should start empty', function() {

var arr = [];

assert.equal(arr.length, 0);

});

});

Note on the first line, we set up the assert variable. This is just so we don't need to keep typing chai.assert everywhere.

In the it function, we create an array and check its length. Although simple, this is a good example of how tests work.

First, you have something you're testing — this is called the *System Under Test* or *SUT*.

Then, if necessary, you do something with the SUT. In this test, we're not doing anything, since we're checking the array starts as empty.

The last thing in a test should be the validation — an *assertion* which checks the result.

Here, we are using assert.equal to do this. Most assertion functions take parameters in the same order: First the "actual" value, and then the "expected" value.

The *actual* value is the result from your test code, so in this case arr.length The *expected* value is what the result *should* be. Since an array should begin empty, the expected value in this test is 0

Chai also offers two different styles of writing assertions, but we're using assert to keep things simple for now. When you become more experienced with writing tests, you might want to use the expect assertions instead, as they provide some more flexibility.

Running the Test

In order to run this test, we need to add it to the test runner file we created earlier.

If you're using Node.js, you can skip this step, and use the command mocha to run the test. You'll see the test results in the terminal.

Otherwise, to add this test to the runner, simply add:

<script src="test/arrayTest.js"></script> Below:

<! load your test files here >

Once you've added the script, you can then load the test runner page in your browser of choice.

The Test Results

![](index-13_1.png)

![](index-13_2.png)

When you run your tests, the test results will look something like this: Note that what we entered into the describe and it functions show up in the output

— the tests are grouped under the description. Note that it's also possible to nest describe blocks to create further subgroupings.

Let's take a look at what a failing test looks like.

On the line in the test that says:

assert.equal(arr.length, 0);

Replace the number 0 with 1\. This makes the test fail, as the array's length no longer matches the expected value.

If you run the tests again, you'll see the failing test in red with a description of what went wrong.

One of the benefits of tests is that they help you find bugs quicker, however this error is not very helpful in that respect. We can fix it though.

Most of the assertion functions can also take an optional message parameter. This is the message that is displayed when the assertion fails. It's a good idea to use this parameter to make the error message easier to understand.

We can add a message to our assertion like so:

assert.equal(arr.length, 1, 'Array length was not 0');

If you rerun tests, the custom message will appear instead of the default.

Let's switch the assertion back to the way it was — replace 1 with 0, and run the tests again to make sure they pass.

Putting It Together

So far we've looked at fairly simple examples. Let's put what we've learned into practice and see how we would test a more realistic piece of code.

Here's a function which adds a CSS class to an element. This should go in a new file js/className.js.

function addClass(el, newClass) {

if(el.className.indexOf(newClass) === 1) {

el.className += newClass;

}

}

To make it a bit more interesting, I made it add a new class only when that class doesn't exist in an element's className property — who wants to see <div class="hello hello hello hello"> after all?

In the best case, we would write tests for this function *before* we write the code. But testdriven development is a complex topic, and for now we just want to focus on writing tests.

To get started, let's recall the basic idea behind unit tests: We give the function certain inputs and then verify the function behaves as expected. So what are the inputs and behaviors for this function?

Given an element and a class name:

if the element's className property does not contain the class name, it should be added.

if the element's className property does contain the class name, it should not be added.

Let's translate these cases into two tests. In the test directory, create a new file classNameTest.js and add the following:

describe('addClass', function() {

it('should add class to element');

it('should not add a class which already exists');

});

We changed the wording slightly to the "it should do X" form used with tests. This means that it reads a bit nicer, but is essentially still the same humanreadable form we listed above. It's usually not much more difficult than this to go from idea to test.

But wait, where are the test functions? Well, when we omit the second parameter to it, Mocha marks these tests as *pending* in the test results. This is a convenient way to set up a number of tests — kind of like a todo list of what you intend to write.

Let's continue by implementing the first test.

describe('addClass', function() {

it('should add class to element', function() {

var element = { className: '' };

addClass(element, 'testclass');

assert.equal(element.className, 'testclass');

});

it('should not add a class which already exists');

});

In this test, we create an element variable and pass it as a parameter to the addClass function, along with a string testclass (the new class to add). Then, we check the class is included in the value using an assertion.

Again, we went from our initial idea — given an element and a class name, it should be added into the class list — and translated it into code in a fairly straightforward manner.

Although this function is designed to work with DOM elements, we're using a plain JS

object here. Sometimes we can make use of JavaScript's dynamic nature in this fashion to simplify our tests. If we didn't do this, we would need to create an actual element and it would complicate our test code. As an additional benefit, since we don't use DOM, we can also run this test within Node.js if we so wish.

RUNNING THE TESTS IN THE BROWSER

To run the test in the browser, you'll need to add className.js and classNameTest.js to the runner:

<! load code you want to test here >

<script src="js/className.js"></script>

<! load your test files here >

<script src="test/classNameTest.js"></script> You should now see one test pass and another test show up as pending, as is demonstrated by the following CodePen. Note that the code differs slightly from the example in order to make the code work within the CodePen environment.

Live Code!

See the Pen Unit Testing with Mocha (1),

Next, let's implement the second test…

it('should not add a class which already exists', function() {

var element = { className: 'exists' };

addClass(element, 'exists');

var numClasses = element.className.split(' ').length;

assert.equal(numClasses, 1);

});

It's a good habit to run your tests often, so let's check what happens if we run the tests now. As expected, they should pass.

Here's another CodePen with the second test implemented.

Live Code!

See the Pen Unit Testing with Mocha (2),

But hang on! I actually tricked you a bit. There is a third behavior for this function which we haven't considered. There is also a bug in the function — a fairly serious one.

It's only a three line function but did you notice it?

Let's write one more test for the third behavior which exposes the bug as a bonus.

it('should append new class after existing one', function() {

var element = { className: 'exists' };

addClass(element, 'newclass');

var classes = element.className.split(' ');

assert.equal(classes[1], 'newclass');

});

This time the test fails. You can see it in action in the following CodePen. The problem here is simple: CSS class names in elements should be separated by a space. However, our current implementation of addClass doesn't add a space!

Live Code!

See the Pen Unit Testing with Mocha (3).

Let's fix the function and make the test pass.

function addClass(el, newClass) {

if(el.className.indexOf(newClass) !== 1) {

return;

}

if(el.className !== '') {

//ensure class names are separated by a space

newClass = ' ' + newClass;

}

el.className += newClass;

}

And here's a final CodePen with the fixed function and passing tests.

Live Code!

See the Pen Unit Testing with Mocha (4).

RUNNING THE TESTS ON NODE

In Node, things are only visible to other things in the same file. As className.js and classNameTest.js are in different files, we need to find a way to expose one to the other. The standard way to do this is through the use of module.exports. If you need a refresher, you can read all about that here: Understanding module.exports and exports in Node.js

The code essentially stays the same, but is structured slightly differently:

// className.js

module.exports = {

addClass: function(el, newClass) {

if(el.className.indexOf(newClass) !== 1) {

return;

}

if(el.className !== '') {

//ensure class names are separated by a space

newClass = ' ' + newClass;

}

el.className += newClass;

}

}

// classNameTest.js

var chai = require('chai');

var assert = chai.assert;

var className = require('../js/className.js');

var addClass = className.addClass;

// The rest of the file remains the same

![](index-19_1.png)

describe('addClass', function() {

...

});

And as you can see, the tests pass.

What's Next?

As you can see, testing does not have to be complicated or difficult. Just as with other aspects of writing JavaScript apps, you have some basic patterns which repeat. Once you get familiar with those, you can keep using them again and again.

But this is just scratching the surface. There's a lot more to learn about unit testing.

Testing more complex systems

How to deal with Ajax, databases, and other "external" things?

TestDriven Development

If you want to continue learning this and more, I've created a free JavaScript unit testing quickstart series. If you found this article useful, you should definitely check it out here.

Alternatively, if video is more your style, you might be interested in SitePoint Premium's course: TestDriven Development in Node.js.

HisC

tor h

y apter 2: An Introduction to Functional

To J

pic a

s vaScript

Tu B

torYia lM

s . DAVID GREEN

You’ve heard that JavaScript is a functional language, or at least that it’s capable of Offers & Deals

supporting functional programming. But what is functional programming? And for that matter, if you’re going to start comparing programming paradigms in general, how is a Highlights

functional approach different from the JavaScript that you’ve always written?

Settings

Well, the good news is that JavaScript isn’t picky when it comes to paradigms. You can mix your imperative, objectoriented, prototypal, and functional code as you see fit, and Support

still get the job done. But the bad news is what that means for your code. JavaScript can Sig s

n u

Op

u p

t ort a wide range of programming styles simultaneously within the same codebase, so it’s up to you to make the right choices for maintainability, readability, and performance.

Functional JavaScript doesn’t have to take over an entire project in order to add value.

Learning a little about the functional approach can help guide some of the decisions you make as you build your projects, regardless of the way you prefer to structure your code. Learning some functional patterns and techniques can put you well on your way to writing cleaner and more elegant JavaScript regardless of your preferred approach.

Imperative JavaScript

JavaScript first gained popularity as an inbrowser language, used primarily for adding simple hover and click effects to elements on a web page. For years, that’s most of what people knew about it, and that contributed to the bad reputation JavaScript earned early on.

As developers struggled to match the flexibility of JavaScript against the intricacy of the browser document object model (DOM), actual JavaScript code often looked something like this in the real world:

var result;

function getText() {

var someText = prompt("Give me something to capitalize");

capWords(someText);

alert(result.join(" "));

};

function capWords(input) {

var counter;

var inputArray = input.split(" ");

var transformed = "";

result = [];

for (counter = 0; counter < inputArray.length; counter++) {

transformed = [

inputArray[counter].charAt(0).toUpperCase(),

inputArray[counter].substring(1)

].join("");

result.push(transformed);

}

};

document.getElementById("main_button").onclick = getText;

So many things are going on in this little snippet of code. Variables are being defined on the global scope. Values are being passed around and modified by functions. DOM

methods are being mixed with native JavaScript. The function names are not very descriptive, and that’s due in part to the fact that the whole thing relies on a context that may or may not exist. But if you happened to run this in a browser inside an HTML

document that defined a <button id="main_button">, you might get prompted for some text to work with, and then see the an alert with first letter of each of the words in that text capitalized.

Imperative code like this is written to be read and executed from top to bottom (give or take a little variable hoisting). But there are some improvements we could make to clean it up and make it more readable by taking advantage of JavaScript’s objectoriented nature.

Object-Oriented JavaScript

After a few years, developers started to notice the problems with imperative coding in a shared environment like the browser. Global variables from one snippet of JavaScript clobbered global variables set by another. The order in which the code was called affected the results in ways that could be unpredictable, especially given the delays introduced by network connections and rendering times.

![](index-22_1.png)

![](index-22_2.png)

![](index-22_3.png)

![](index-22_4.png)

![](index-22_5.png)

![](index-22_6.png)

![](index-22_7.png)

![](index-22_8.png)

![](index-22_9.png)

![](index-22_10.png)

![](index-22_11.png)

![](index-22_12.png)

![](index-22_13.png)

![](index-22_14.png)

![](index-22_15.png)

![](index-22_16.png)

![](index-22_17.png)

![](index-22_18.png)

![](index-22_19.png)

![](index-22_20.png)

![](index-22_21.png)

![](index-22_22.png)

![](index-22_23.png)

![](index-22_24.png)

![](index-22_25.png)

![](index-22_26.png)

![](index-22_27.png)

![](index-22_28.png)

![](index-22_29.png)

![](index-22_30.png)

![](index-22_31.png)

![](index-22_32.png)

![](index-22_33.png)

![](index-22_34.png)

![](index-22_35.png)

![](index-22_36.png)

![](index-22_37.png)

![](index-22_38.png)

![](index-22_39.png)

![](index-22_40.png)

![](index-22_41.png)

![](index-22_42.png)

![](index-22_43.png)

![](index-22_44.png)

![](index-22_45.png)

![](index-22_46.png)

![](index-22_47.png)

![](index-22_48.png)

![](index-22_49.png)

![](index-22_50.png)

![](index-22_51.png)

![](index-22_52.png)

![](index-22_53.png)

![](index-22_54.png)

![](index-22_55.png)

![](index-22_56.png)

![](index-22_57.png)

![](index-22_58.png)

![](index-22_59.png)

![](index-22_60.png)

![](index-22_61.png)

![](index-22_62.png)

![](index-22_63.png)

![](index-22_64.png)

![](index-22_65.png)

![](index-22_66.png)

![](index-22_67.png)

![](index-22_68.png)

![](index-22_69.png)

![](index-22_70.png)

![](index-22_71.png)

![](index-22_72.png)

![](index-22_73.png)

![](index-22_74.png)

![](index-22_75.png)

![](index-22_76.png)

![](index-22_77.png)

![](index-22_78.png)

![](index-22_79.png)

![](index-22_80.png)

![](index-22_81.png)

![](index-22_82.png)

![](index-22_83.png)

![](index-22_84.png)

![](index-22_85.png)

![](index-22_86.png)

![](index-22_87.png)

![](index-22_88.png)

![](index-22_89.png)

![](index-22_90.png)

![](index-22_91.png)

![](index-22_92.png)

![](index-22_93.png)

![](index-22_94.png)

![](index-22_95.png)

![](index-22_96.png)

![](index-22_97.png)

![](index-22_98.png)

![](index-22_99.png)

![](index-22_100.png)

![](index-22_101.png)

![](index-22_102.png)

![](index-22_103.png)

![](index-22_104.png)

![](index-22_105.png)

![](index-22_106.png)

![](index-22_107.png)

![](index-22_108.png)

![](index-22_109.png)

![](index-22_110.png)

![](index-22_111.png)

![](index-22_112.png)

![](index-22_113.png)

![](index-22_114.png)

![](index-22_115.png)

![](index-22_116.png)

![](index-22_117.png)

![](index-22_118.png)

![](index-22_119.png)

![](index-22_120.png)

![](index-22_121.png)

![](index-22_122.png)

![](index-22_123.png)

![](index-22_124.png)

![](index-22_125.png)

![](index-22_126.png)

![](index-22_127.png)

![](index-22_128.png)

![](index-22_129.png)

![](index-22_130.png)

![](index-22_131.png)

![](index-22_132.png)

![](index-22_133.png)

![](index-22_134.png)

![](index-22_135.png)

![](index-22_136.png)

![](index-22_137.png)

![](index-22_138.png)

![](index-22_139.png)

![](index-22_140.png)

![](index-22_141.png)

![](index-22_142.png)

![](index-22_143.png)

![](index-22_144.png)

![](index-22_145.png)

![](index-22_146.png)

![](index-22_147.png)

![](index-22_148.png)

![](index-22_149.png)

![](index-22_150.png)

![](index-22_151.png)

![](index-22_152.png)

![](index-22_153.png)

![](index-22_154.png)

![](index-22_155.png)

![](index-22_156.png)

![](index-22_157.png)

![](index-22_158.png)

![](index-22_159.png)

![](index-22_160.png)

![](index-22_161.png)

![](index-22_162.png)

![](index-22_163.png)

![](index-22_164.png)

![](index-22_165.png)

![](index-22_166.png)

![](index-22_167.png)

![](index-22_168.png)

![](index-22_169.png)

![](index-22_170.png)

![](index-22_171.png)

![](index-22_172.png)

![](index-22_173.png)

![](index-22_174.png)

![](index-22_175.png)

![](index-22_176.png)

![](index-22_177.png)

![](index-22_178.png)

![](index-22_179.png)

![](index-22_180.png)

Eventually, some better practices emerged to help encapsulate JavaScript code and make it play better with the DOM. An updated variation of the same code above, written to an objectoriented standard, might look something like this: (function() {

"use strict";

var SomeText = function(text) {

this.text = text;

};

SomeText.prototype.capify = function(str) {

var firstLetter = str.charAt(0);

var remainder = str.substring(1);

return [firstLetter.toUpperCase(), remainder].join("");

};

SomeText.prototype.capifyWords = function() {

var result = [];

var textArray = this.text.split(" ");

for (var counter = 0; counter < textArray.length; counter++) {

result.push(this.capify(textArray[counter]));

}

return result.join(" ");

};

document.getElementById("main_button").addEventListener("click", function(e) {

var something = prompt("Give me something to capitalize");

var newText = new SomeText(something);

alert(newText.capifyWords());

});

}());

In this objectoriented version, the constructor function simulates a class to model the object we want. Methods live on the new object’s prototype to keep memory use low.

And all of the code is isolated in an anonymous immediatelyinvoked function expression so it doesn’t litter the global scope. There’s even a "use strict" directive to take advantage of the latest JavaScript engine, and the oldfashioned onclick method has been replaced with a shiny new addEventListener, because who uses IE8 or earlier anymore? A script like this would likely be inserted at the end of the

<body> element on an HTML document, to make sure all the DOM had been loaded before it was processed so the <button> it relies on would be available.

But despite all this reconfiguration, there are still many artifacts of the same imperative style that led us here. The methods in the constructor function rely on variables that are scoped to the parent object. There’s a looping construct for iterating across all the members of the array of strings. There’s a counter variable that serves no purpose

![](index-23_1.png)

![](index-23_2.png)

![](index-23_3.png)

![](index-23_4.png)

![](index-23_5.png)

![](index-23_6.png)

![](index-23_7.png)

![](index-23_8.png)

![](index-23_9.png)

![](index-23_10.png)

![](index-23_11.png)

![](index-23_12.png)

![](index-23_13.png)

![](index-23_14.png)

![](index-23_15.png)

![](index-23_16.png)

![](index-23_17.png)

![](index-23_18.png)

![](index-23_19.png)

![](index-23_20.png)

![](index-23_21.png)

![](index-23_22.png)

![](index-23_23.png)

![](index-23_24.png)

![](index-23_25.png)

![](index-23_26.png)

![](index-23_27.png)

![](index-23_28.png)

![](index-23_29.png)

![](index-23_30.png)

![](index-23_31.png)

![](index-23_32.png)

![](index-23_33.png)

![](index-23_34.png)

![](index-23_35.png)

![](index-23_36.png)

![](index-23_37.png)

![](index-23_38.png)

![](index-23_39.png)

![](index-23_40.png)

![](index-23_41.png)

![](index-23_42.png)

![](index-23_43.png)

![](index-23_44.png)

![](index-23_45.png)

![](index-23_46.png)

![](index-23_47.png)

![](index-23_48.png)

![](index-23_49.png)

![](index-23_50.png)

![](index-23_51.png)

![](index-23_52.png)

![](index-23_53.png)

![](index-23_54.png)

![](index-23_55.png)

![](index-23_56.png)

![](index-23_57.png)

![](index-23_58.png)

![](index-23_59.png)

![](index-23_60.png)

![](index-23_61.png)

![](index-23_62.png)

![](index-23_63.png)

![](index-23_64.png)

![](index-23_65.png)

![](index-23_66.png)

![](index-23_67.png)

![](index-23_68.png)

![](index-23_69.png)

![](index-23_70.png)

![](index-23_71.png)

![](index-23_72.png)

![](index-23_73.png)

![](index-23_74.png)

![](index-23_75.png)

![](index-23_76.png)

![](index-23_77.png)

![](index-23_78.png)

![](index-23_79.png)

![](index-23_80.png)

![](index-23_81.png)

![](index-23_82.png)

![](index-23_83.png)

![](index-23_84.png)

![](index-23_85.png)

![](index-23_86.png)

![](index-23_87.png)

![](index-23_88.png)

![](index-23_89.png)

![](index-23_90.png)

![](index-23_91.png)

![](index-23_92.png)

![](index-23_93.png)

![](index-23_94.png)

![](index-23_95.png)

![](index-23_96.png)

![](index-23_97.png)

![](index-23_98.png)

![](index-23_99.png)

![](index-23_100.png)

![](index-23_101.png)

![](index-23_102.png)

![](index-23_103.png)

![](index-23_104.png)

![](index-23_105.png)

![](index-23_106.png)

![](index-23_107.png)

![](index-23_108.png)

![](index-23_109.png)

![](index-23_110.png)

![](index-23_111.png)

![](index-23_112.png)

![](index-23_113.png)

![](index-23_114.png)

![](index-23_115.png)

![](index-23_116.png)

![](index-23_117.png)

![](index-23_118.png)

![](index-23_119.png)

![](index-23_120.png)

![](index-23_121.png)

![](index-23_122.png)

![](index-23_123.png)

![](index-23_124.png)

![](index-23_125.png)

![](index-23_126.png)

![](index-23_127.png)

![](index-23_128.png)

![](index-23_129.png)

![](index-23_130.png)

![](index-23_131.png)

![](index-23_132.png)

![](index-23_133.png)

![](index-23_134.png)

![](index-23_135.png)

![](index-23_136.png)

![](index-23_137.png)

![](index-23_138.png)

![](index-23_139.png)

![](index-23_140.png)

![](index-23_141.png)

![](index-23_142.png)

![](index-23_143.png)

![](index-23_144.png)

![](index-23_145.png)

![](index-23_146.png)

![](index-23_147.png)

![](index-23_148.png)

![](index-23_149.png)

![](index-23_150.png)

![](index-23_151.png)

![](index-23_152.png)

![](index-23_153.png)

![](index-23_154.png)

![](index-23_155.png)

![](index-23_156.png)

![](index-23_157.png)

![](index-23_158.png)

![](index-23_159.png)

![](index-23_160.png)

![](index-23_161.png)

![](index-23_162.png)

![](index-23_163.png)

![](index-23_164.png)

![](index-23_165.png)

![](index-23_166.png)

![](index-23_167.png)

![](index-23_168.png)

![](index-23_169.png)

![](index-23_170.png)

![](index-23_171.png)

![](index-23_172.png)

![](index-23_173.png)

![](index-23_174.png)

![](index-23_175.png)

![](index-23_176.png)

![](index-23_177.png)

![](index-23_178.png)

![](index-23_179.png)

![](index-23_180.png)

other than to increment the progress through the for loop. And there are methods that produce the side effect of modifying variables that exist outside of their own definitions.

All of this makes the code more brittle, less portable, and makes it harder to test the methods outside of this narrow context.

Functional JavaScript

The objectoriented approach is much cleaner and more modular than the imperative approach we started with, but let’s see if we can improve it by addressing some of the drawbacks we discussed. It would be great if we could find ways to take advantage of JavaScript’s builtin ability to treat functions as firstclass objects so that our code could be cleaner, more stable, and easier to repurpose.

(function() {

"use strict";

var capify = function(str) {

return [str.charAt(0).toUpperCase(), str.substring(1)].join("");

};

var processWords = function(fn, str) {

return str.split(" ").map(fn).join(" ");

};

document.getElementById("main_button").addEventListener("click", function(e) {

var something = prompt("Give me something to capitalize");

alert(processWords(capify, something));

});

}());

Did you notice how much shorter this version is? We’re only defining two functions: capify and processWords. Each of these functions is pure, meaning that they don’t rely on the state of the code they’re called from. The functions don’t create side effects that alter variables outside of themselves. There is one and only one result a function returns for any given set of arguments. Because of these improvements, the new functions are very easy to test, and could be snipped right out of this code and used elsewhere without any modifications.

There might have been one keyword in there that you wouldn’t recognize unless you’ve peeked at some functional code before. We took advantage of the new map method on Array to apply a function to each element of the temporary array we created when we split our string. Map is just one of a handful of convenience methods we were given when modern browsers and serverside JavaScript interpreters implemented the ECMAscript 5 standards. Just using map here, in place of a for loop, eliminated the

counter variable and helped make our code much cleaner and easier to read.

Start Thinking Functionally

You don’t have to abandon everything you know to take advantage of the functional paradigm. You can get started thinking about your JavaScript in a functional way by considering a few questions when you write your next program: Are my functions dependent on the context in which they are called, or are they pure and independent?

Can I write these functions in such a way that I could depend on them always returning the same result for a given input?

Am I sure that my functions don’t modify anything outside of themselves?

If I wanted to use these functions in another program, would I need to make changes to them?

This introduction barely scratches the surface of functional JavaScript, but I hope it whets your appetite to learn more.

**https://avxhm.se/blogs/hill0**

HisC

tor h

y apter 3: An Introduction to Gulp.js

Topics

BY CRAIG BUCKLER

Tu D

tore

iavlselopers spend precious little time coding. Even if we ignore irritating meetings, much of the job involves basic tasks which can sap your working Off d

eras y

& :Deals

Highlig g

htesnerating HTML from templates and content files compressing new and modified images

Settings

compiling Sass to CSS code

Supportremoving console and debugger statements from scripts Sign Ou ttranspiling ES6 to crossbrowser–compatible ES5 code code linting and validation

concatenating and minifying CSS and JavaScript files deploying files to development, staging and production servers.

Tasks must be repeated every time you make a change. You may start with good intentions, but the most infallible developer will forget to compress an image or two.

Over time, preproduction tasks become increasingly arduous and timeconsuming;

you'll dread the inevitable content and template changes. It's mindnumbing, repetitive work. Wouldn’t it be better to spend your time on more profitable jobs?

If so, you need a *task runner* or *build process*.

That Sounds Scarily Complicated!

Creating a build process will take time. It's more complex than performing each task manually, but over the long term, you’ll save hours of effort, reduce human error and save your sanity. Adopt a pragmatic approach:

Automate the most frustrating tasks first.

Try not to overcomplicate your build process. An hour or two is more than enough for the initial setup.

Choose task runner software and stick with it for a while. Don't switch to another option on a whim.

Some of the tools and concepts may be new to you, but take a deep breath and concentrate on one thing at a time.

Task Runners: the Options

Build tools such as GNU Make have been available for decades, but webspecific task runners are a relatively new phenomenon. The first to achieve critical mass was Grunt

— a Node.js task runner which used plugins controlled (originally) by a JSON

configuration file. Grunt was hugely successful, but there were a number of issues: 1\. Grunt required plugins for basic functionality such as file watching.

2\. Grunt plugins often performed multiple tasks, which made customisation more awkward.

3\. JSON configuration could become unwieldy for all but the most basic tasks.

4\. Tasks could run slowly because Grunt saved files between every processing step.

Many issues were addressed in later editions, but Gulp had already arrived and offered a number of improvements:

1\. Features such as file watching were built in.

2\. Gulp plugins were *(mostly)* designed to do a single job.

3\. Gulp used JavaScript configuration code that was less verbose, easier to read, simpler to modify, and provided better flexibility.

4\. Gulp was faster because it uses Node.js streams to pass data through a series of piped plugins. Files were only written at the end of the task.

Of course, Gulp itself isn't perfect, and new task runners such as Broccoli.js, Brunch and webpack have also been competing for developer attention. More recently, npm itself has been touted as a simpler option. All have their pros and cons, but Gulp remains the favorite and is currently used by more than 40% of web developers.

Gulp requires Node.js, but while some JavaScript knowledge is beneficial, developers

from all web programming faiths will find it useful.

What About Gulp 4?

This tutorial describes how to use Gulp 3 — the most recent release version at the time of writing. Gulp 4 has been in development for some time but remains a beta product.

It's possible to use or switch to Gulp 4, but I recommend sticking with version 3 until the final release.

Step 1: Install Node.js

Node.js can be downloaded for Windows, macOS and Linux from nodejs.org/download/. There are various options for installing from binaries, package managers and docker images, and full instructions are available.

For Windows Users

Node.js and Gulp run on Windows, but some plugins may not instal or run if they depend on native Linux binaries such as image compression libraries.

One option for Windows 10 users is the new bash commandline, which solves many issues.

Once installed, open a command prompt and enter: node v

This reveals the version number. You're about to make heavy use of npm — the Node.js package manager which is used to install modules. Examine its version number: npm v

For Linux Users

Node.js modules can be instal ed global y so they’re available throughout your system. However, most users wil not have permission to write to the

![](index-28_1.png)

![](index-28_2.png)

![](index-28_3.png)

![](index-28_4.png)

![](index-28_5.png)

![](index-28_6.png)

![](index-28_7.png)

![](index-28_8.png)

![](index-28_9.png)

![](index-28_10.png)

![](index-28_11.png)

![](index-28_12.png)

![](index-28_13.png)

![](index-28_14.png)

![](index-28_15.png)

![](index-28_16.png)

![](index-28_17.png)

![](index-28_18.png)

![](index-28_19.png)

![](index-28_20.png)

![](index-28_21.png)

![](index-28_22.png)

![](index-28_23.png)

![](index-28_24.png)

![](index-28_25.png)

![](index-28_26.png)

![](index-28_27.png)

![](index-28_28.png)

![](index-28_29.png)

![](index-28_30.png)

![](index-28_31.png)

![](index-28_32.png)

![](index-28_33.png)

![](index-28_34.png)

![](index-28_35.png)

![](index-28_36.png)

![](index-28_37.png)

![](index-28_38.png)

![](index-28_39.png)

![](index-28_40.png)

![](index-28_41.png)

![](index-28_42.png)

![](index-28_43.png)

![](index-28_44.png)

![](index-28_45.png)

![](index-28_46.png)

![](index-28_47.png)

![](index-28_48.png)

![](index-28_49.png)

![](index-28_50.png)

![](index-28_51.png)

![](index-28_52.png)

![](index-28_53.png)

![](index-28_54.png)

![](index-28_55.png)

![](index-28_56.png)

![](index-28_57.png)

![](index-28_58.png)

![](index-28_59.png)

![](index-28_60.png)

![](index-28_61.png)

![](index-28_62.png)

![](index-28_63.png)

![](index-28_64.png)

![](index-28_65.png)

![](index-28_66.png)

![](index-28_67.png)

![](index-28_68.png)

![](index-28_69.png)

![](index-28_70.png)

![](index-28_71.png)

![](index-28_72.png)

![](index-28_73.png)

![](index-28_74.png)

![](index-28_75.png)

![](index-28_76.png)

![](index-28_77.png)

![](index-28_78.png)

![](index-28_79.png)

![](index-28_80.png)

![](index-28_81.png)

![](index-28_82.png)

![](index-28_83.png)

![](index-28_84.png)

![](index-28_85.png)

![](index-28_86.png)

![](index-28_87.png)

![](index-28_88.png)

![](index-28_89.png)

![](index-28_90.png)

![](index-28_91.png)

![](index-28_92.png)

![](index-28_93.png)

![](index-28_94.png)

![](index-28_95.png)

![](index-28_96.png)

![](index-28_97.png)

![](index-28_98.png)

![](index-28_99.png)

![](index-28_100.png)

![](index-28_101.png)

![](index-28_102.png)

![](index-28_103.png)

![](index-28_104.png)

![](index-28_105.png)

![](index-28_106.png)

![](index-28_107.png)

![](index-28_108.png)

![](index-28_109.png)

![](index-28_110.png)

![](index-28_111.png)

![](index-28_112.png)

![](index-28_113.png)

![](index-28_114.png)

![](index-28_115.png)

![](index-28_116.png)

![](index-28_117.png)

![](index-28_118.png)

![](index-28_119.png)

![](index-28_120.png)

![](index-28_121.png)

![](index-28_122.png)

![](index-28_123.png)

![](index-28_124.png)

![](index-28_125.png)

![](index-28_126.png)

![](index-28_127.png)

![](index-28_128.png)

![](index-28_129.png)

![](index-28_130.png)

![](index-28_131.png)

![](index-28_132.png)

![](index-28_133.png)

![](index-28_134.png)

![](index-28_135.png)

![](index-28_136.png)

![](index-28_137.png)

![](index-28_138.png)

![](index-28_139.png)

![](index-28_140.png)

![](index-28_141.png)

![](index-28_142.png)

![](index-28_143.png)

![](index-28_144.png)

![](index-28_145.png)

![](index-28_146.png)

![](index-28_147.png)

![](index-28_148.png)

![](index-28_149.png)

![](index-28_150.png)

![](index-28_151.png)

![](index-28_152.png)

![](index-28_153.png)

![](index-28_154.png)

![](index-28_155.png)

![](index-28_156.png)

![](index-28_157.png)

![](index-28_158.png)

![](index-28_159.png)

![](index-28_160.png)

![](index-28_161.png)

![](index-28_162.png)

![](index-28_163.png)

![](index-28_164.png)

![](index-28_165.png)

![](index-28_166.png)

![](index-28_167.png)

![](index-28_168.png)

![](index-28_169.png)

![](index-28_170.png)

![](index-28_171.png)

![](index-28_172.png)

![](index-28_173.png)

![](index-28_174.png)

![](index-28_175.png)

![](index-28_176.png)

![](index-28_177.png)

![](index-28_178.png)

![](index-28_179.png)

![](index-28_180.png)

global directories unless npm commands are prefixed with sudo. There are a number of options to fix npm permissions and tools such as nvm can help, but I often change the default directory. For example, on Ubuntu/Debianbased platforms: cd ~

mkdir .node_modules_global

npm config set prefix=$HOME/.node_modules_global npm install npm g

Then add the fol owing line to the end of ~/.bashrc: export PATH="$HOME/.node_modules_global/bin:$PATH"

Final y, update with this:

source ~/.bashrc

Step 2: Install Gulp Globally

Install Gulp commandline interface globally so the gulp command can be run from any project folder:

npm install gulpcli g

Verify Gulp has installed with this:

gulp v

Step 3: Configure Your Project

For Node.js Projects

You can skip this step if you already have a package.json configuration file.

*Note for Node.js projects: you can skip this step if you already have a* package.json *configuration file.*

Presume you have a new or preexisting project in the folder project1. Navigate to this folder and initialize it with npm:

cd project1

npm init

You’ll be asked a series of questions. Enter a value or hit Return to accept defaults. A package.json file will be created on completion which stores your npm configuration settings.

Git Users

Node.js instal s modules to a node_modules folder. You should add this to your .gitignore file to ensure they’re not committed to your repository.

When deploying the project to another PC, you can run npm install to restore them.

For the remainder of this article, we'll presume your project folder contains the following subfolders:

src folder: preprocessed source files

This contains further subfolders:

html HTML source files and templates

images — the original uncompressed images

js — multiple preprocessed script files

scss — multiple preprocessed Sass .scss files

![](index-30_1.png)

![](index-30_2.png)

![](index-30_3.png)

![](index-30_4.png)

![](index-30_5.png)

![](index-30_6.png)

![](index-30_7.png)

![](index-30_8.png)

![](index-30_9.png)

![](index-30_10.png)

![](index-30_11.png)

![](index-30_12.png)

![](index-30_13.png)

![](index-30_14.png)

![](index-30_15.png)

![](index-30_16.png)

![](index-30_17.png)

![](index-30_18.png)

![](index-30_19.png)

![](index-30_20.png)

![](index-30_21.png)

![](index-30_22.png)

![](index-30_23.png)

![](index-30_24.png)

![](index-30_25.png)

![](index-30_26.png)

![](index-30_27.png)

![](index-30_28.png)

![](index-30_29.png)

![](index-30_30.png)

![](index-30_31.png)

![](index-30_32.png)

![](index-30_33.png)

![](index-30_34.png)

![](index-30_35.png)

![](index-30_36.png)

![](index-30_37.png)

![](index-30_38.png)

![](index-30_39.png)

![](index-30_40.png)

![](index-30_41.png)

![](index-30_42.png)

![](index-30_43.png)

![](index-30_44.png)

![](index-30_45.png)

![](index-30_46.png)

![](index-30_47.png)

![](index-30_48.png)

![](index-30_49.png)

![](index-30_50.png)

![](index-30_51.png)

![](index-30_52.png)

![](index-30_53.png)

![](index-30_54.png)

![](index-30_55.png)

![](index-30_56.png)

![](index-30_57.png)

![](index-30_58.png)

![](index-30_59.png)

![](index-30_60.png)

![](index-30_61.png)

![](index-30_62.png)

![](index-30_63.png)

![](index-30_64.png)

![](index-30_65.png)

![](index-30_66.png)

![](index-30_67.png)

![](index-30_68.png)

![](index-30_69.png)

![](index-30_70.png)

![](index-30_71.png)

![](index-30_72.png)

![](index-30_73.png)

![](index-30_74.png)

![](index-30_75.png)

![](index-30_76.png)

![](index-30_77.png)

![](index-30_78.png)

![](index-30_79.png)

![](index-30_80.png)

![](index-30_81.png)

![](index-30_82.png)

![](index-30_83.png)

![](index-30_84.png)

![](index-30_85.png)

![](index-30_86.png)

![](index-30_87.png)

![](index-30_88.png)

![](index-30_89.png)

![](index-30_90.png)

![](index-30_91.png)

![](index-30_92.png)

![](index-30_93.png)

![](index-30_94.png)

![](index-30_95.png)

![](index-30_96.png)

![](index-30_97.png)

![](index-30_98.png)

![](index-30_99.png)

![](index-30_100.png)

![](index-30_101.png)

![](index-30_102.png)

![](index-30_103.png)

![](index-30_104.png)

![](index-30_105.png)

![](index-30_106.png)

![](index-30_107.png)

![](index-30_108.png)

![](index-30_109.png)

![](index-30_110.png)

![](index-30_111.png)

![](index-30_112.png)

![](index-30_113.png)

![](index-30_114.png)

![](index-30_115.png)

![](index-30_116.png)

![](index-30_117.png)

![](index-30_118.png)

![](index-30_119.png)

![](index-30_120.png)

![](index-30_121.png)

![](index-30_122.png)

![](index-30_123.png)

![](index-30_124.png)

![](index-30_125.png)

![](index-30_126.png)

![](index-30_127.png)

![](index-30_128.png)

![](index-30_129.png)

![](index-30_130.png)

![](index-30_131.png)

![](index-30_132.png)

![](index-30_133.png)

![](index-30_134.png)

![](index-30_135.png)

![](index-30_136.png)

![](index-30_137.png)

![](index-30_138.png)

![](index-30_139.png)

![](index-30_140.png)

![](index-30_141.png)

![](index-30_142.png)

![](index-30_143.png)

![](index-30_144.png)

![](index-30_145.png)

![](index-30_146.png)

![](index-30_147.png)

![](index-30_148.png)

![](index-30_149.png)

![](index-30_150.png)

![](index-30_151.png)

![](index-30_152.png)

![](index-30_153.png)

![](index-30_154.png)

![](index-30_155.png)

![](index-30_156.png)

![](index-30_157.png)

![](index-30_158.png)

![](index-30_159.png)

![](index-30_160.png)

![](index-30_161.png)

![](index-30_162.png)

![](index-30_163.png)

![](index-30_164.png)

![](index-30_165.png)

![](index-30_166.png)

![](index-30_167.png)

![](index-30_168.png)

![](index-30_169.png)

![](index-30_170.png)

![](index-30_171.png)

![](index-30_172.png)

![](index-30_173.png)

![](index-30_174.png)

build folder: compiled/processed files

Gulp will create files and create subfolders as necessary: html — compiled static HTML files

images — compressed images

js — a single concatenated and minified JavaScript file css — a single compiled and minified CSS file

Your project will almost certainly be different but this structure is used for the examples below.

Following Along on Unix

Tip: If you're on a Unixbased system and you just want to fol ow along with the tutorial, you can recreate the folder structure with the fol owing command: mkdir p src/{html,images,js,scss} build/{html,images,js,css}

*Tip: If you're on a Unixbased system and you just want to follow along with the* *tutorial, you can recreate the folder structure with the following command:* mkdir p src/{html,images,js,scss} build/{html,images,js,css}

Step 4: Install Gulp Locally

You can now install Gulp in your project folder using the command: npm install gulp savedev

This installs Gulp as a development dependency and the "devDependencies" section of package.json is updated accordingly. We’ll presume Gulp and all plugins are

development dependencies for the remainder of this tutorial.

ALTERNATIVE DEPLOYMENT OPTIONS

Development dependencies are not installed when the NODE_ENV environment variable is set to production on your operating system. You would normally do this on your live server with the Mac/Linux command:

export NODE_ENV=production

Or on Windows:

set NODE_ENV=production

This tutorial presumes your assets will be compiled to the build folder and committed to your Git repository or uploaded directly to the server. However, it may be preferable to build assets on the live server if you want to change the way they are created. For example, HTML, CSS and JavaScript files are minified on production but not development environments. In that case, use the save option for Gulp and all plugins, i.e.

npm install gulp save

This sets Gulp as an application dependency in the "dependencies" section of package.json. It will be installed when you enter npm install and can be run wherever the project is deployed. You can remove the build folder from your repository since the files can be created on any platform when required.

Step 4: Create a Gulp Configuration File

Create a new gulpfile.js configuration file in the root of your project folder. Add some basic code to get started:

// Gulp.js configuration

var

// modules

gulp = require('gulp'),

// development mode?

devBuild = (process.env.NODE_ENV !== 'production'),

// folders

folder = {

src: 'src/',

build: 'build/'

}

;

This references the Gulp module, sets a devBuild variable to true when running in development (or nonproduction mode) and defines the source and build folder locations.

ES6

ES5compatible JavaScript code is provided in this tutorial. This wil work for al versions of Gulp and Node.js with or without the harmony flag. Most ES6 features are supported in Node 6 and above so feel free to use arrow functions, let, const, etc. if you're using a recent version.

gulpfile.js won't do anything yet because you need to …

Step 5: Create Gulp Tasks

On its own, Gulp does nothing. You must:

1\. install Gulp plugins, and

2\. write tasks which utilize those plugins to do something useful.

It's possible to write your own plugins but, since almost 3,000 are available, it's unlikely you'll ever need to. You can search using Gulp's own directory at gulpjs.com/plugins/, on npmjs.com, or search "gulp *something*" to harness the mighty power of Google.

Gulp provides three primary task methods:

gulp.task — defines a new task with a name, optional array of dependencies and a function.

gulp.src — sets the folder where source files are located.

gulp.dest — sets the destination folder where build files will be placed.

Any number of plugin calls are set with pipe between the .src and .dest.

IMAGE TASK

This is best demonstrated with an example, so let's create a basic task which compresses images and copies them to the appropriate build folder. Since this process could take time, we'll only compress new and modified files. Two plugins can help us: gulpnewer and gulpimagemin. Install them from the commandline: npm install gulpnewer gulpimagemin savedev

We can now reference both modules the top of gulpfile.js:

// Gulp.js configuration

var

// modules

gulp = require('gulp'),

newer = require('gulpnewer'),

imagemin = require('gulpimagemin'),

We can now define the image processing task itself as a function at the end of gulpfile.js:

// image processing

gulp.task('images', function() {

var out = folder.build + 'images/';

return gulp.src(folder.src + 'images/**/*')

.pipe(newer(out))

.pipe(imagemin({ optimizationLevel: 5 }))

.pipe(gulp.dest(out));

});

All tasks are syntactically similar. This code:

1\. Creates a new task named images.

2\. Defines a function with a return value which …

3\. Defines an out folder where build files will be located.

4\. Sets the Gulp src source folder. The /**/* ensures that images in subfolders are also processed.

5\. Pipes all files to the gulpnewer module. Source files that are newer than corresponding destination files are passed through. Everything else is removed.

6\. The remaining new or changed files are piped through gulpimagemin which sets an optional optimizationLevel argument.

7\. The compressed images are output to the Gulp dest folder set by out.

Save gulpfile.js and place a few images in your project's src/images folder before running the task from the command line:

gulp images

All images are compressed accordingly and you’ll see output such as: Using file gulpfile.js

Running 'imagemin'...

Finished 'imagemin' in 5.71 ms

gulpimagemin: image1.png (saved 48.7 kB)

gulpimagemin: image2.jpg (saved 36.2 kB)

gulpimagemin: image3.svg (saved 12.8 kB)

Try running gulp images again and nothing should happen because no newer images exist.

HTML TASK

We can now create a similar task which copies files from the source HTML folder. We can safely minify our HTML code to remove unnecessary whitespace and attributes using the gulphtmlclean plugin:

npm install gulphtmlclean savedev

This is then referenced at the top of gulpfile.js: var

// modules

gulp = require('gulp'),

newer = require('gulpnewer'),

imagemin = require('gulpimagemin'),

htmlclean = require('gulphtmlclean'),

We can now create an html task at the end of gulpfile.js:

// HTML processing

gulp.task('html', ['images'], function() {

var

out = folder.build + 'html/',

page = gulp.src(folder.src + 'html/**/*')

.pipe(newer(out));

// minify production code

if (!devBuild) {

page = page.pipe(htmlclean());

}

return page.pipe(gulp.dest(out));

});

This reuses gulpnewer and introduces a couple of concepts: 1\. The [images] argument states that our images task must be run before processing the HTML (the HTML is likely to reference images). Any number of dependent tasks can be listed in this array and all will complete before the task function runs.

2\. We only pipe the HTML through gulphtmlclean if NODE_ENV is set to production. Therefore, the HTML remains uncompressed during development which may be useful for debugging.

Save gulpfile.js and run gulp html from the command line. Both the html and images tasks will run.

JAVASCRIPT TASK

Too easy for you? Let's process all our JavaScript files by building a basic module bundler. It will:

1\. Ensure dependencies are loaded first using the gulpdeporder plugin. This analyses comments at the top of each script to ensure correct ordering. For example, //

requires: defaults.js lib.js.

2\. Concatenate all script files into a single main.js file using gulpconcat.

3\. Remove all console and debugging statements with gulpstripdebug and minimize code with gulpuglify. This step will only occur when running in production mode.

Install the plugins:

![](index-36_1.png)

![](index-36_2.png)

![](index-36_3.png)

![](index-36_4.png)

![](index-36_5.png)

![](index-36_6.png)

![](index-36_7.png)

![](index-36_8.png)

![](index-36_9.png)

![](index-36_10.png)

![](index-36_11.png)

![](index-36_12.png)

![](index-36_13.png)

![](index-36_14.png)

![](index-36_15.png)

![](index-36_16.png)

![](index-36_17.png)

![](index-36_18.png)

![](index-36_19.png)

![](index-36_20.png)

![](index-36_21.png)

![](index-36_22.png)

![](index-36_23.png)

![](index-36_24.png)

![](index-36_25.png)

![](index-36_26.png)

![](index-36_27.png)

![](index-36_28.png)

![](index-36_29.png)

![](index-36_30.png)

![](index-36_31.png)

![](index-36_32.png)

![](index-36_33.png)

![](index-36_34.png)

![](index-36_35.png)

![](index-36_36.png)

![](index-36_37.png)

![](index-36_38.png)

![](index-36_39.png)

![](index-36_40.png)

![](index-36_41.png)

![](index-36_42.png)

![](index-36_43.png)

![](index-36_44.png)

![](index-36_45.png)

![](index-36_46.png)

![](index-36_47.png)

![](index-36_48.png)

![](index-36_49.png)

![](index-36_50.png)

![](index-36_51.png)

![](index-36_52.png)

![](index-36_53.png)

![](index-36_54.png)

![](index-36_55.png)

![](index-36_56.png)

![](index-36_57.png)

![](index-36_58.png)

![](index-36_59.png)

![](index-36_60.png)

![](index-36_61.png)

![](index-36_62.png)

![](index-36_63.png)

![](index-36_64.png)

![](index-36_65.png)

![](index-36_66.png)

![](index-36_67.png)

![](index-36_68.png)

![](index-36_69.png)

![](index-36_70.png)

![](index-36_71.png)

![](index-36_72.png)

![](index-36_73.png)

![](index-36_74.png)

![](index-36_75.png)

![](index-36_76.png)

![](index-36_77.png)

![](index-36_78.png)

![](index-36_79.png)

![](index-36_80.png)

![](index-36_81.png)

![](index-36_82.png)

![](index-36_83.png)

![](index-36_84.png)

![](index-36_85.png)

![](index-36_86.png)

![](index-36_87.png)

![](index-36_88.png)

![](index-36_89.png)

![](index-36_90.png)

![](index-36_91.png)

![](index-36_92.png)

![](index-36_93.png)

![](index-36_94.png)

![](index-36_95.png)

![](index-36_96.png)

![](index-36_97.png)

![](index-36_98.png)

![](index-36_99.png)

![](index-36_100.png)

![](index-36_101.png)

![](index-36_102.png)

![](index-36_103.png)

![](index-36_104.png)

![](index-36_105.png)

![](index-36_106.png)

![](index-36_107.png)

![](index-36_108.png)

![](index-36_109.png)

![](index-36_110.png)

![](index-36_111.png)

![](index-36_112.png)

![](index-36_113.png)

![](index-36_114.png)

![](index-36_115.png)

![](index-36_116.png)

![](index-36_117.png)

![](index-36_118.png)

![](index-36_119.png)

![](index-36_120.png)

![](index-36_121.png)

![](index-36_122.png)

![](index-36_123.png)

![](index-36_124.png)

![](index-36_125.png)

![](index-36_126.png)

![](index-36_127.png)

![](index-36_128.png)

![](index-36_129.png)

![](index-36_130.png)

![](index-36_131.png)

![](index-36_132.png)

![](index-36_133.png)

![](index-36_134.png)

![](index-36_135.png)

![](index-36_136.png)

![](index-36_137.png)

![](index-36_138.png)

![](index-36_139.png)

![](index-36_140.png)

![](index-36_141.png)

![](index-36_142.png)

![](index-36_143.png)

![](index-36_144.png)

![](index-36_145.png)

![](index-36_146.png)

![](index-36_147.png)

![](index-36_148.png)

![](index-36_149.png)

![](index-36_150.png)

![](index-36_151.png)

![](index-36_152.png)

![](index-36_153.png)

![](index-36_154.png)

![](index-36_155.png)

![](index-36_156.png)

![](index-36_157.png)

![](index-36_158.png)

![](index-36_159.png)

![](index-36_160.png)

![](index-36_161.png)

![](index-36_162.png)

![](index-36_163.png)

![](index-36_164.png)

![](index-36_165.png)

![](index-36_166.png)

![](index-36_167.png)

![](index-36_168.png)

npm install gulpdeporder gulpconcat gulpstripdebug gulpuglify savedev Reference them at the top of gulpfile.js:

var

...

concat = require('gulpconcat'),

deporder = require('gulpdeporder'),

stripdebug = require('gulpstripdebug'),

uglify = require('gulpuglify'),

Then add a new js task:

// JavaScript processing

gulp.task('js', function() {

var jsbuild = gulp.src(folder.src + 'js/**/*')

.pipe(deporder())

.pipe(concat('main.js'));

if (!devBuild) {

jsbuild = jsbuild

.pipe(stripdebug())

.pipe(uglify());

}

return jsbuild.pipe(gulp.dest(folder.build + 'js/'));

});

Save then run gulp js to watch the magic happen!

CSS TASK

Finally, let’s create a CSS task which compiles Sass .scss files to a single .css file using gulpsass. This is a Gulp plugin for nodesass which binds to the superfast LibSass C/C++ port of the Sass engine *(you won't need to install Ruby)*. We'll presume your primary Sass file scss/main.scss is responsible for loading all partials.

Our task will also utilize the fabulous PostCSS via the gulppostcss plugin. PostCSS

requires its own set of plugins and we'll install these: postcssassets to manage assets. This allows us to use properties such as

![](index-37_1.png)

![](index-37_2.png)

![](index-37_3.png)

![](index-37_4.png)

![](index-37_5.png)

![](index-37_6.png)

![](index-37_7.png)

![](index-37_8.png)

![](index-37_9.png)

![](index-37_10.png)

![](index-37_11.png)

![](index-37_12.png)

![](index-37_13.png)

![](index-37_14.png)

![](index-37_15.png)

![](index-37_16.png)

![](index-37_17.png)

![](index-37_18.png)

![](index-37_19.png)

![](index-37_20.png)

![](index-37_21.png)

![](index-37_22.png)

![](index-37_23.png)

![](index-37_24.png)

![](index-37_25.png)

![](index-37_26.png)

![](index-37_27.png)

![](index-37_28.png)

![](index-37_29.png)

![](index-37_30.png)

![](index-37_31.png)

![](index-37_32.png)

![](index-37_33.png)

![](index-37_34.png)

![](index-37_35.png)

![](index-37_36.png)

![](index-37_37.png)

![](index-37_38.png)

![](index-37_39.png)

![](index-37_40.png)

![](index-37_41.png)

![](index-37_42.png)

![](index-37_43.png)

![](index-37_44.png)

![](index-37_45.png)

![](index-37_46.png)

![](index-37_47.png)

![](index-37_48.png)

![](index-37_49.png)

![](index-37_50.png)

![](index-37_51.png)

![](index-37_52.png)

![](index-37_53.png)

![](index-37_54.png)

![](index-37_55.png)

![](index-37_56.png)

![](index-37_57.png)

![](index-37_58.png)

![](index-37_59.png)

![](index-37_60.png)

![](index-37_61.png)

![](index-37_62.png)

![](index-37_63.png)

![](index-37_64.png)

![](index-37_65.png)

![](index-37_66.png)

![](index-37_67.png)

![](index-37_68.png)

![](index-37_69.png)

![](index-37_70.png)

![](index-37_71.png)

![](index-37_72.png)

![](index-37_73.png)

![](index-37_74.png)

![](index-37_75.png)

![](index-37_76.png)

![](index-37_77.png)

![](index-37_78.png)

![](index-37_79.png)

![](index-37_80.png)

![](index-37_81.png)

![](index-37_82.png)

![](index-37_83.png)

![](index-37_84.png)

![](index-37_85.png)

![](index-37_86.png)

![](index-37_87.png)

![](index-37_88.png)

![](index-37_89.png)

![](index-37_90.png)

![](index-37_91.png)

![](index-37_92.png)

![](index-37_93.png)

![](index-37_94.png)

![](index-37_95.png)

![](index-37_96.png)

![](index-37_97.png)

![](index-37_98.png)

![](index-37_99.png)

![](index-37_100.png)

![](index-37_101.png)

![](index-37_102.png)

![](index-37_103.png)

![](index-37_104.png)

![](index-37_105.png)

![](index-37_106.png)

![](index-37_107.png)

![](index-37_108.png)

![](index-37_109.png)

![](index-37_110.png)

![](index-37_111.png)

![](index-37_112.png)

![](index-37_113.png)

![](index-37_114.png)

![](index-37_115.png)

![](index-37_116.png)

![](index-37_117.png)

![](index-37_118.png)

![](index-37_119.png)

![](index-37_120.png)

![](index-37_121.png)

![](index-37_122.png)

![](index-37_123.png)

![](index-37_124.png)

![](index-37_125.png)

![](index-37_126.png)

![](index-37_127.png)

![](index-37_128.png)

![](index-37_129.png)

![](index-37_130.png)

![](index-37_131.png)

![](index-37_132.png)

![](index-37_133.png)

![](index-37_134.png)

![](index-37_135.png)

![](index-37_136.png)

![](index-37_137.png)

![](index-37_138.png)

![](index-37_139.png)

![](index-37_140.png)

![](index-37_141.png)

![](index-37_142.png)

![](index-37_143.png)

![](index-37_144.png)

![](index-37_145.png)

![](index-37_146.png)

![](index-37_147.png)

![](index-37_148.png)

![](index-37_149.png)

![](index-37_150.png)

![](index-37_151.png)

![](index-37_152.png)

![](index-37_153.png)

![](index-37_154.png)

![](index-37_155.png)

![](index-37_156.png)

![](index-37_157.png)

![](index-37_158.png)

![](index-37_159.png)

![](index-37_160.png)

![](index-37_161.png)

![](index-37_162.png)

![](index-37_163.png)

![](index-37_164.png)

![](index-37_165.png)

![](index-37_166.png)

![](index-37_167.png)

![](index-37_168.png)

![](index-37_169.png)

![](index-37_170.png)

![](index-37_171.png)

![](index-37_172.png)

![](index-37_173.png)

![](index-37_174.png)

background: resolve('image.png'); to resolve file paths or background: inline('image.png'); to inline dataencoded images.

autoprefixer to automatically add vendor prefixes to CSS properties.

cssmqpacker to pack multiple references to the same CSS media query into a single rule.

cssnano to minify the CSS code when running in production mode.

First, install all the modules:

npm install gulpsass gulppostcss postcssassets autoprefixer cssmqpacker cssnano savedev Then reference them at the top of gulpfile.js:

var

...

sass = require('gulpsass'),

postcss = require('gulppostcss'),

assets = require('postcssassets'),

autoprefixer = require('autoprefixer'),

mqpacker = require('cssmqpacker'),

cssnano = require('cssnano'),

We can now create a new css task at the end of gulpfile.js. Note the images task is set as a dependency because the postcssassets plugin can reference images during the build process. In addition, most plugins can be passed arguments (refer to their documentation for more information):

// CSS processing

gulp.task('css', ['images'], function() {

var postCssOpts = [

assets({ loadPaths: ['images/'] }),

autoprefixer({ browsers: ['last 2 versions', '> 2%'] }), mqpacker

];

if (!devBuild) {

postCssOpts.push(cssnano);

}

return gulp.src(folder.src + 'scss/main.scss')

.pipe(sass({

outputStyle: 'nested',

imagePath: 'images/',

precision: 3,

errLogToConsole: true

}))

.pipe(postcss(postCssOpts))

.pipe(gulp.dest(folder.build + 'css/'));

});

Save the file and run the task from the command line: gulp css

Step 6: Automate Tasks

We've been running one task at a time. We can run them all in one command by adding a new run task to gulpfile.js:

// run all tasks

gulp.task('run', ['html', 'css', 'js']);

Save and enter gulp run at the command line to execute all tasks. Note that I omitted the images task because it's already set as a dependency for the html and css tasks.

Is this still too much hard work? Gulp offers another method — gulp.watch — which can monitor your source files and run an appropriate task whenever a file is changed.

The method is passed a folder and a list of tasks to execute when a change occurs. Let's create a new watch task at the end of gulpfile.js:

// watch for changes

gulp.task('watch', function() {

// image changes

gulp.watch(folder.src + 'images/**/*', ['images']);

// html changes

gulp.watch(folder.src + 'html/**/*', ['html']);

// javascript changes

gulp.watch(folder.src + 'js/**/*', ['js']);

// css changes

gulp.watch(folder.src + 'scss/**/*', ['css']);

});

Rather than running gulp watch immediately, let's add a default task:

// default task

gulp.task('default', ['run', 'watch']);

Save gulpfile.js and enter gulp at the command line. Your images, HTML, CSS

and JavaScript will all be processed, then Gulp will remain active watching for updates and rerunning tasks as necessary. Hit Ctrl/Cmd + C to abort monitoring and return to the command line.

Step 7: Profit!

Other plugins you may find useful:

gulploadplugins ± load all Gulp plugin modules without require declarations gulppreprocess — a simple HTML and JavaScript preprocessor gulpless — the Less CSS preprocessor plugin

gulpstylus — the Stylus CSS preprocessor plugin gulpsequence — run a series of gulp tasks in a specific order gulpplumber — error handling which prevents Gulp stopping on failures gulpsize — displays file sizes and savings

gulpnodemon — uses nodemon to automatically restart Node.js applications when changes occur.

gulputil — utility functions including logging and color coding.

One useful method in gulputil is .noop() which passes data straight through without performing any action. This could be used for cleaner development/production processing code. For example:

var gutil = require('gulputil');

// HTML processing

gulp.task('html', ['images'], function() {

var out = folder.src + 'html/**/*';

return gulp.src(folder.src + 'html/**/*')

.pipe(newer(out))

.pipe(devBuild ? gutil.noop() : htmlclean())

.pipe(gulp.dest(out));

});

Gulp can also call other Node.js modules, and they don't necessarily need to be plugins.

For example:

browsersync — automatically reload assets or refresh your browser when changes occur

del — delete files and folders (perhaps clean your build folder at the start of every run).

Invest a little time and Gulp could save many hours of development frustration. The advantages:

plugins are plentiful

configuration using pipes is readable and easy to follow gulpfile.js can be adapted and reused in other projects your total page weight can be reduced to improve performance you can simplify your deployment.

Useful links:

Gulp home page

Gulp plugins

npm home page

Applying the processes above to a simple website reduced the total weight by more than 50%. You can test your own results using page weight analysis tools or a service such as New Relic, which provides a range of sophisticated application performance monitoring tools.

Gulp can revolutionize your workflow. I hope you found this tutorial useful and consider Gulp for your production process.

HisC

tor h

y apter 4: A Side-by-side Comparison of

To E

pic x

s press, Koa and Hapi.js

Tu B

torYia lO

s LAYINKA OMOLE

If you’re a Node.js developer, chances are you have, at some point, used Offers & Deals

Express.js to create your applications or APIs. Express.js is a very popular Node.js framework, and even has some other frameworks built on top of it Highlights

such as Sails.js, kraken.js, KeystoneJS and many others. However, amidst this popularity, a bunch of other frameworks have been gaining attention Settings

in the JavaScript world, such as Koa and hapi.

Support

In this article, we’ll examine Express.js, Koa and hapi.js — their similarities, differences Sig a

n n

O d

ut use cases.

Background

Let’s firstly introduce each of these frameworks separately.

EXPRESS.JS

Express.js is described as the standard server framework for Node.js. It was created by TJ Holowaychuk, acquired by StrongLoop in 2014, and is currently maintained by the Node.js Foundation incubator. With about 170+ million downloads in the last year, it’s currently beyond doubt that it’s the most popular Node.js framework.

KOA

Development began on Koa in late 2013 by the same guys at Express. It’s referred to as the future of Express. Koa is also described as a much more modern, modular and m

in

imal istic ve rsion of th e Express framework .

HAPI.JS

Hapi.js was developed by the team at Walmart Labs (led by Eran Hammer) after they tried Express and discovered that it didn’t work for their requirements. It was originally developed on top of Express, but as time went by, it grew into a fullfledged framework.

*Fun Fact: hapi is short for Http API server.*

Philosophy

Now that we have some background on the frameworks and how they were created, let’s compare each of them based on important concepts, such as their philosophy, routing, and so on.

Compatibility

Al code examples are in ES6 and make use of version 4 of Express.js, 2.4

of Koa, and 17 for hapi.js.

EXPRESS.JS

Express was built to be a simple, unopinionated web framework. From its GitHub README:

The Express philosophy is to provide small, robust tooling for HTTP servers, making it a great solution for single page applications, web sites, hybrids, or public HTTP APIs.

Express.js is minimal and doesn’t possess many features out of the box. It doesn’t force things like file structure, ORM or templating engine.

KOA

While Express.js is minimal, Koa can boast a much more minimalistic code footprint — 

around 2k LOC. Its aim is to allow developers be even more expressive. Like Express.js, it can easily be extended by using existing or custom plugins and middleware. It’s more futuristic in its approach, in that it relies heavily on the relatively new JavaScript features like generators and async/await.

HAPI.JS

Hapi.js focuses more on configuration and provides a lot more features out of the box

than Koa and Express.js. Eran Hammer, one of the creators of hapi, described the reason for building the framework properly in his blog post: hapi was created around the idea that configuration is better than code, that business logic must be isolated from the transport layer, and that native node constructs like buffers and stream should be supported as first class objects.

Starting a Server

Starting a server is one of the basic things we’d need to do in our projects. Let’s examine how it can be done in the different frameworks. We’ll start a server and listen on port 3000 in each example.

EXPRESS.JS

const express = require('express');

const app = express();

app.listen(3000, () => console.log('App is listening on port 3000!'));

Starting a server in Express.js is as simple as requiring the express package, initializing the express app to the app variable and calling the app.listen() method, which is just a wrapper around the native Node.js http.createServer() method.

KOA

Starting a server in Koa is quite similar to Express.js: const Koa = require('koa');

const app = new Koa();

app.listen(3000, () => console.log('App is listening on port 3000!'));

The app.listen() method in Koa is also a wrapper around the http.createServer() method.

HAPI.JS

Starting a server in hapi.js is quite a departure from what many of us may be used to from Express:

const Hapi = require('hapi');

const server = Hapi.server({

host: 'localhost',

port: 3000

});

async function start() {

try {

await server.start();

}

catch (err) {

console.log(err);

process.exit(1);

}

console.log('Server running at:', server.info.uri);

};

start();

In the code block above, first we require the hapi package, then instantiate a server with Hapi.server(), which has a single config object argument containing the host and port parameters. Then we start the server with the asynchronous server.start() function.

Unlike in Express.js and Koa, the server.start() function in hapi is not a wrapper around the native http.createServer() method. It instead implements its own custom logic.

The above code example is from the hapi.js website, and shows the importance the creators of hapi.js place on configuration and error handling.

Routing

Routing is another key aspect of modern web applications. Let’s define a /hello route for a simple Hello World app in each framework to have a feel of how routing works for them.

EXPRESS.JS

app.get('/hello', (req, res) => res.send('Hello World!'));

Creating routes in Express is as simple as calling the app object with the required HTTP method. The syntax is app.METHOD(PATH, HANDLER), where PATH is the path on the server and HANDLER is function which is called when the path is matched.

KOA

KOA

Koa doesn’t have its own router bundled with it, so we’ll have to use a router middleware to handle routing on Koa apps. Two common routing options are koaroute and koarouter. Here’s an example using koaroute: const route = require('koaroute');

app.use(route.get('/hello', ctx => {

ctx.body = 'Hello World!';

}));

We can see immediately that Koa needs each route to be defined as a middleware on the app. The ctx is a context object that contains Node’s request and response objects. ctx.body is a method in the response object and can be used to set the response body to either a string, Buffer, Stream, Object or null. The second parameter for the route method can be an async or generator function, so the use of callbacks in reduced.

HAPI.JS

server.route({

method: 'GET',

path:'/hello',

handler: function (request, h) {

return 'Hello world!';

}

});

The server.route() method in hapi takes a single config object with the following parameters: method, path and handler. You can see the documentation on routing in hapi here.

The request parameter in the handler function is an object which contains the user’s request details, while the h parameter is described as a response toolkit.

Middleware

One of the major concepts Node developers are used to is working with middleware.

Middleware functions are functions that sit in between requests and responses.

They have access to the request and response objects and can run the next middleware after they’re processed. Let’s take a look at how they’re defined in the

different frameworks by implementing a simple function that logs the time a request is made to the server.

EXPRESS.JS

app.use((req, res, next) => {

console.log(`Time: ${Date.now()}`);

next();

})

Registering middleware in Express.js is as simple as binding the middleware to the app object by using the app.use() function. You can read more on middleware in Express.js here.

Koa

app.use(async (ctx, next) => {

console.log(`Time: ${Date.now()}`);

await next();

});

Middleware registration in Koa is similar to Express.js. The major differences are that the context object (ctx) is used in place of the request and response objects in Express.js and Koa embraces the modern async/await paradigm for defining the middleware function.

HAPI.JS

server.ext('onRequest', (request, h) => {

console.log(`Time: ${Date.now()}`);

return h.continue;

});

In hapi.js there are certain extension points in the request lifecyle. The server.ext() method registers an extension function to be called at a certain point in the request life cycle. You can read more about it here. We make use of the onRequest extension point in the example above to register a middleware (or extension) function.

Usage

From the comparisons and code examples we’ve seen above, it’s clear that Express and Koa are the most similar, with hapi.js being the framework to deviate from the norm

that Node.js devs are used to. Hence hapi.js may not be the best choice when trying to build a quick and easy app, as it will take a bit of time to get used to.

In my opinion, Express is still a great choice when building small to mediumsized applications. It can become a bit complicated to manage for very large applications, as it doesn’t possess the modularity hapi.js has built into it, with support for custom plugins and its unique routing method. However, there’s been some speculation in recent times regarding the future of Express.js as TJ announced he’s no longer working on it and the reduced rate at which updates are shipped. Bit it’s pretty stable and willn’t be going away any time soon. It also has a large community of developers building various extensions and plugins for it.

Like Express.js, Koa is well suited for many simple Node.js projects. It only consists of the bare minimum (it has zero inbuilt middleware) and encourages developers to add what they need to it by building or making use of available external middleware. It makes use of modern JavaScript generator functions and async/await heavily, which makes it sort of futuristic in its approach. Its middleware cascading pattern is also great, as it makes implementing and understanding the flow of middleware in your applications very easy. Koa probably won’t be a great choice for you if you aren’t yet ready to embrace new shiny things like generator functions, or if you’re not willing to spend some time building out all the middleware you need. The community support for Koa is rapidly growing, as it has a good amount of external middleware already built for it (some by the core Koa team) for common tasks such as routing, logging and so on.

Hapi.js is the definite choice if you and your team prefer to spend more time configuring than actually coding out features. It was built to be modular and for large applications with large teams. It encourgages the microservice architecture, as various parts of your app can be built as plugins and registered in your server before starting it up. Hapi.js is backed by large companies such as Auth0 and Lob, so it has a pretty good future ahead of it and won’t be going away anytime soon. It’s also trusted by some big names, as seen on their community page.

Hapi.js has a whole lot more features out of the box than Koa and Express.js, such as support for authentication, caching, logging, validation and so on, which makes it feel more like a fullfledged framework. You can check out their tutorials page to get a good feel of the features they provide. There aren’t yet very many opensource projects and plugins built on and for hapi.js, so a lot of work might need to be done by developers using it if they plan to extend its core functionality.

Conclusion

Conclusion

All three frameworks are great choices when starting up new projects, but ultimately your choice will be based on the project requirements, your team members and the level of flexibility you’re looking for.

**https://avxhm.se/blogs/hill0**

HisC

tor h

y apter 5: An Introduction to Sails.js

Topics

BY AHMED BOUCHEFRA

Tu S

to a

ri i

allss.js is a Node.js MVC (model–view–controller) framework that follows the “convention over configuration” principle. It’s inspired by the popular Off R

er u

s b

& y

De o

al n

s Rails web framework, and allows you to quickly build REST APIs, singlepage apps and realtime (WebSocketsbased) apps. It makes Hi e

gh xlitge

ht n

s sive use of code generators that allow you to build your application with less writing of code—particularly of common code that can be Setotitnhgserwise scaffolded.

Su T

pphoert framework is built on top of Express.js, one of the most popular Node.js libraries, and Socket.io, a JavaScript library/engine for adding realtime, bidirectional, event

Sign Out

based communication to applications. At the time of writing, the official stable version of Sails.js is *0.12.14*, which is available from npm. Sails.js version 1.0 has not officially been released, but according to Sails.js creators, version 1.0 is already used in some production applications, and they even recommend using it when starting new projects.

Main Features

Sails.js has many great features:

it’s built on Express.js

it has realtime support with WebSockets

it takes a “convention over configuration” approach it has powerful code generation, thanks to Blueprints it’s database agnostic thanks to its powerful Waterline ORM/ODM

it supports multiple data stores in the same project it has good documentation.

There are currently a few important cons, such as: no support for JOIN query in Waterline

no support for SQL transactions until Sails v1.0 (in beta at the time of writing) until version 1.0, it still uses Express.js v3, which is EOL (end of life) development is very slow.

Sails.js vs Express.js

Software development is all about building abstractions. Sails.js is a highlevel abstraction layer on top of Express.js (which itself is an abstraction over Node’s HTTP

modules) that provides routing, middleware, file serving and so on. It also adds a powerful ORM/ODM, the MVC architectural pattern, and a powerful generator CLI (among other features).

You can build web applications using Node’s lowlevel HTTP service and other utility modules (such as the filesystem module) but it’s not recommended except for the sake of learning the Node.js platform. You can also take a step up and use Express.js, which is a popular, lightweight framework for building web apps.

You’ll have routing and other useful constructs for web apps, but you’ll need to take care of pretty much everything from configuration, file structure and code organization to working with databases.

Express doesn’t offer any builtin tool to help you with database access, so you’ll need to bring together the required technologies to build a complete web application. This is what’s called a stack. Web developers, using JavaScript, mostly use the popular MEAN

stack, which stands for MongoDB, ExpressJS, AngularJS and Node.js.

MongoDB is the preferred database system among Node/Express developers, but you can use any database you want. The most important point here is that Express doesn’t provide any builtin APIs when it comes to databases.

The Waterline ORM/ODM

One key feature of Sails.js is Waterline, a powerful ORM (object relational mapper) for SQLbased databases and ODM (object document mapper) for NoSQL documentbased databases. Waterline abstracts away all the complexities when working with databases and, most importantly, with Waterline you don’t have to make the decision of choosing

a database system when you’re just starting development. It also doesn’t intimidate you when your client hasn’t yet decided on the database technology to use.

You can start building you application without a single line of configuration. In fact, you don’t have to install a database system at all initially. Thanks to the builtin sailsdisk NeDBbased file database, you can transparently use the file system to store and retrieve data for testing your application functionality.

Once you’re ready and you have decided on the convenient database system you want to use for your project, you can then simply switch the database by installing the relevant adapter for your database system. Waterline has official adapters for popular relational database systems such as MySQL and PostgreSQL and the NoSQL databases, such as MongoDB and Redis, and the community has also built numerous adapters for the other popular database systems such as Oracle, MSSQL, DB2, SQLite, CouchDB and neo4j. In case when you can’t find an adapter for the database system you want to use, you can develop your own custom adapter.

Waterline abstracts away the differences between different database systems and allows you to have a normalized interface for your application to communicate with any supported database system. You don’t have to work with SQL or any lowlevel API (for NoSQL databases) but that doesn’t mean you can’t (at least for SQLbased databases and MongoDB).

There are situations when you need to write custom SQL, for example, for performance reasons, for working with complex database requirements, or for accessing databasespecific features. In this case, you can use the .query() method available only on the Waterline models that are configured to use SQL systems (you can find more information about query() from the docs).

Since different database systems have common and databasespecific features, the Waterline ORM/ODM can only be good for you as long as you only constrain yourself to use the common features. Also, if you use raw SQL or native MongoDB APIs, you’ll lose many of the features of Waterline, including the ability to switch between different databases.

Getting Started with Sails.js

Now that we’ve covered the basic concepts and features of Sails.js, let’s see how you can quickly get started using Sails.js to create new projects and lift them.

PREREQUISITES

![](index-52_1.jpg)

PREREQUISITES

Before you can use Sails.js, you need to have a development environment with Node.js (and npm) installed. You can install both of them by heading to the official Node.js website and downloading the right installer for your operating system.

Make sure, also, to install whatever database management system you want to use with Sails.js (either a relational or a NoSQL database). If you’re not interested by using a fullfledged database system, at this point, you can still work with Sails.js thanks to sailsdisk, which allows you to have a filebased database out of the box.

INSTALLING THE SAILS.JS CLI

After satisfying the working development requirements, you can head over to your terminal (Linux and macOS) or command prompt (Windows) and install the Sails.js Command Line Utility, globally, from npm:

sudo npm install sails g

If you want to install the latest *1.0* version to try the new features, you need to use the beta version:

npm install sails@beta g

You may or may not need *sudo* to install packages globally depending on your npm configuration.

SCAFFOLDING A SAILS.JS PROJECT

After installing the Sails.js CLI, you can go ahead and scaffold a new project with one command:

sails new sailsdemo

This will create a new folder for your project named sailsdemo on your current directory. You can also scaffold your project files inside an existing folder with this: sails new .

You can scaffold a new Sails.js project without a front end with this: sails new sailsdemo nofrontend

Find more information about the features of the CLI from the docs.

THE ANATOMY OF A SAILS.JS PROJECT

Here’s a screenshot of a project generated using the Sails.js CLI:

![](index-54_1.png)

A Sails.js project is a Node.js module with a package.json and a node_modules folder. You may also notice the presence of Gruntfile.js. Sails.js uses Grunt as a build tool for building frontend assets.

If you’re building an app for the browser, you’re in luck. Sails ships with Grunt — which means your entire frontend asset workflow is completely customizable, and comes with support for all of the great Grunt modules which are already out there. That includes support for Less, Sass, Stylus, CoffeeScript, JST, Jade, Handlebars, Dust, and many more. When you’re ready to go into production, your assets are minified and gzipped automatically. You can even compile your static assets and push them out to a CDN like CloudFront to make your app load even faster. (You can read more about these points on the Sails.js website.)

You can also use Gulp or Webpack as your build system instead of Grunt, with custom generators. See the sailsgeneratenewgulp and sailswebpack projects on GitHub.

For more community generators, see this documentation page on the Sails.js site.

The project contains many configuration files and folders. Most of them are self explanatory, but let’s go over the ones you’ll be working with most of the time:

api/controllers: this is the folder where controllers live. Controllers correspond to the *C* part in *MVC*. It’s where the business logic for your application exists.

api/models: the folder where models exist. Models correspond to the *M* part of *MVC* architecture. This is where you need to put classes or objects that map to your SQL/NoSQL data.

api/policies: this is the folder where you need to put policies for your application

api/responses: this folder contains server response logic such as functions to handle the 404 and 500 responses, etc.

api/services: this where your appwide services live. A service is a global class encapsulating common logic that can be used throughout many controllers.

./views: this folder contains templates used for displaying views. By default, this folder contains the *ejs* engine templates, but you can configure any Expresssupported engine such as EJS, Jade, Handlebars, Mustache and Underscore etc.

./config: this folder contains many configuration files that enable you to configure every detail of your application, such as CORS, CSRF protection, i18n, http, settings for models, views, logging and policies etc. One important file that you’ll frequently use is config/routes.js, where you can create your application routes and map them to actual actions in the controllers or to views directly.

./assets: this is the folder where you can place any static files (CSS, JavaScript and images etc.) for your application.

RUNNING YOUR SAILS.JS PROJECT

You can start the development server by running the following command from your project’s root:

sails lift

This will prompt you to choose a migration strategy, and then will launch the dev server.

![](index-56_1.png)

![](index-56_2.png)

You can then use your web browser to navigate to [http://localhost:1337/]

(http://localhost:1337/). If you’ve generated a Sails.js project with a front end (i.e without using the *nofrontend* option) you’ll see this home page: CREATING WATERLINE MODELS

![](index-57_1.png)

![](index-57_2.png)

![](index-57_3.png)

![](index-57_4.png)

![](index-57_5.png)

![](index-57_6.png)

![](index-57_7.png)

![](index-57_8.png)

![](index-57_9.png)

![](index-57_10.png)

![](index-57_11.png)

![](index-57_12.png)

![](index-57_13.png)

![](index-57_14.png)

![](index-57_15.png)

![](index-57_16.png)

![](index-57_17.png)

![](index-57_18.png)

![](index-57_19.png)

![](index-57_20.png)

![](index-57_21.png)

![](index-57_22.png)

![](index-57_23.png)

![](index-57_24.png)

![](index-57_25.png)

![](index-57_26.png)

![](index-57_27.png)

![](index-57_28.png)

![](index-57_29.png)

![](index-57_30.png)

![](index-57_31.png)

![](index-57_32.png)

![](index-57_33.png)

![](index-57_34.png)

![](index-57_35.png)

![](index-57_36.png)

![](index-57_37.png)

![](index-57_38.png)

![](index-57_39.png)

![](index-57_40.png)

![](index-57_41.png)

![](index-57_42.png)

![](index-57_43.png)

![](index-57_44.png)

![](index-57_45.png)

![](index-57_46.png)

![](index-57_47.png)

![](index-57_48.png)

![](index-57_49.png)

![](index-57_50.png)

![](index-57_51.png)

![](index-57_52.png)

![](index-57_53.png)

![](index-57_54.png)

![](index-57_55.png)

![](index-57_56.png)

![](index-57_57.png)

![](index-57_58.png)

![](index-57_59.png)

![](index-57_60.png)

![](index-57_61.png)

![](index-57_62.png)

![](index-57_63.png)

![](index-57_64.png)

![](index-57_65.png)

![](index-57_66.png)

![](index-57_67.png)

![](index-57_68.png)

![](index-57_69.png)

![](index-57_70.png)

![](index-57_71.png)

![](index-57_72.png)

![](index-57_73.png)

![](index-57_74.png)

![](index-57_75.png)

![](index-57_76.png)

![](index-57_77.png)

![](index-57_78.png)

![](index-57_79.png)

![](index-57_80.png)

![](index-57_81.png)

![](index-57_82.png)

![](index-57_83.png)

![](index-57_84.png)

![](index-57_85.png)

![](index-57_86.png)

![](index-57_87.png)

![](index-57_88.png)

![](index-57_89.png)

![](index-57_90.png)

![](index-57_91.png)

![](index-57_92.png)

![](index-57_93.png)

![](index-57_94.png)

![](index-57_95.png)

![](index-57_96.png)

![](index-57_97.png)

![](index-57_98.png)

![](index-57_99.png)

![](index-57_100.png)

![](index-57_101.png)

![](index-57_102.png)

![](index-57_103.png)

![](index-57_104.png)

![](index-57_105.png)

![](index-57_106.png)

![](index-57_107.png)

![](index-57_108.png)

![](index-57_109.png)

![](index-57_110.png)

![](index-57_111.png)

![](index-57_112.png)

![](index-57_113.png)

![](index-57_114.png)

![](index-57_115.png)

![](index-57_116.png)

![](index-57_117.png)

![](index-57_118.png)

![](index-57_119.png)

![](index-57_120.png)

![](index-57_121.png)

![](index-57_122.png)

![](index-57_123.png)

![](index-57_124.png)

![](index-57_125.png)

![](index-57_126.png)

![](index-57_127.png)

![](index-57_128.png)

![](index-57_129.png)

![](index-57_130.png)

![](index-57_131.png)

![](index-57_132.png)

![](index-57_133.png)

![](index-57_134.png)

![](index-57_135.png)

![](index-57_136.png)

![](index-57_137.png)

![](index-57_138.png)

![](index-57_139.png)

![](index-57_140.png)

![](index-57_141.png)

![](index-57_142.png)

![](index-57_143.png)

![](index-57_144.png)

![](index-57_145.png)

![](index-57_146.png)

![](index-57_147.png)

![](index-57_148.png)

![](index-57_149.png)

![](index-57_150.png)

![](index-57_151.png)

![](index-57_152.png)

![](index-57_153.png)

![](index-57_154.png)

![](index-57_155.png)

![](index-57_156.png)

![](index-57_157.png)

![](index-57_158.png)

![](index-57_159.png)

![](index-57_160.png)

![](index-57_161.png)

![](index-57_162.png)

![](index-57_163.png)

![](index-57_164.png)

![](index-57_165.png)

![](index-57_166.png)

![](index-57_167.png)

![](index-57_168.png)

![](index-57_169.png)

![](index-57_170.png)

![](index-57_171.png)

![](index-57_172.png)

![](index-57_173.png)

![](index-57_174.png)

![](index-57_175.png)

![](index-57_176.png)

![](index-57_177.png)

![](index-57_178.png)

![](index-57_179.png)

![](index-57_180.png)

A model is an abstraction, usually represented by an object or a class in a generalpurpose programming language, and it refers/maps either to an SQL table in a relational database or a document (or keyvalue pairs) in a NoSQL database.

You can create models using the Sails.js CLI:

sails generate model product

This will create a Product.js model in api/models with the following content:

/**

* Product.js

*

* @description :: TODO: You might write a short summary of how this model works and what it represents here.

* @docs :: http://sailsjs.org/documentation/concepts/modelsandorm/models

*/

module.exports = {

attributes: {

}

};

You can then augment your model with attributes. For example: module.exports = {

attributes: {

name: {

type: 'string',

defaultsTo: '',

required: 'true'

},

description: {

type: 'string',

defaultsTo: ''

},

quantity: {

type: 'integer'

},

user: { model: 'User' }

}

};

Notice how we can define the association (onetomany or belongsTo relationship) with the model *User*. You can see all supported associations and how to create them via this Sails.js associations page.

For more information about the available model attributes, see the Sails.js attributes page.

You can also add configurations per model or model settings by adding toplevel properties in the model definition, which will override the global models settings in config/models.js. You can override settings related to the model’s attributes, database connections etc.

For example, let’s specify a different datastore for the *product* model other than the global one used throughout the project:

module.exports = {

connection: 'mysqlcon'

attributes: { /*...*/}

}

This will instruct Sails.js to use a connection named *mysqlcon* to store this model data.

Make sure you add the *mysqlcon* connection to the *connections* object in config/connections.js:

module.exports.connections = {

// sailsdisk is installed by default.

localDiskDb: {

adapter: 'sailsdisk'

},

mysqlcon: {

adapter: 'sailsmysql',

host: 'YOUR_MYSQL_HOST',

user: 'YOUR_MYSQL_USER',

password: 'YOUR_MYSQL_PASSWORD',

database: 'YOUR_MYSQL_DB'

}

};

You also need to install the sailsmysql adapter from npm: npm install sailsmysql@forsails0.12

You can find the available model settings that you can specify from the Sails.js model

![](index-59_1.png)

![](index-59_2.png)

![](index-59_3.png)

![](index-59_4.png)

![](index-59_5.png)

![](index-59_6.png)

![](index-59_7.png)

![](index-59_8.png)

![](index-59_9.png)

![](index-59_10.png)

![](index-59_11.png)

![](index-59_12.png)

![](index-59_13.png)

![](index-59_14.png)

![](index-59_15.png)

![](index-59_16.png)

![](index-59_17.png)

![](index-59_18.png)

![](index-59_19.png)

![](index-59_20.png)

![](index-59_21.png)

![](index-59_22.png)

![](index-59_23.png)

![](index-59_24.png)

![](index-59_25.png)

![](index-59_26.png)

![](index-59_27.png)

![](index-59_28.png)

![](index-59_29.png)

![](index-59_30.png)

![](index-59_31.png)

![](index-59_32.png)

![](index-59_33.png)

![](index-59_34.png)

![](index-59_35.png)

![](index-59_36.png)

![](index-59_37.png)

![](index-59_38.png)

![](index-59_39.png)

![](index-59_40.png)

![](index-59_41.png)

![](index-59_42.png)

![](index-59_43.png)

![](index-59_44.png)

![](index-59_45.png)

![](index-59_46.png)

![](index-59_47.png)

![](index-59_48.png)

![](index-59_49.png)

![](index-59_50.png)

![](index-59_51.png)

![](index-59_52.png)

![](index-59_53.png)

![](index-59_54.png)

![](index-59_55.png)

![](index-59_56.png)

![](index-59_57.png)

![](index-59_58.png)

![](index-59_59.png)

![](index-59_60.png)

![](index-59_61.png)

![](index-59_62.png)

![](index-59_63.png)

![](index-59_64.png)

![](index-59_65.png)

![](index-59_66.png)

![](index-59_67.png)

![](index-59_68.png)

![](index-59_69.png)

![](index-59_70.png)

![](index-59_71.png)

![](index-59_72.png)

![](index-59_73.png)

![](index-59_74.png)

![](index-59_75.png)

![](index-59_76.png)

![](index-59_77.png)

![](index-59_78.png)

![](index-59_79.png)

![](index-59_80.png)

![](index-59_81.png)

![](index-59_82.png)

![](index-59_83.png)

![](index-59_84.png)

![](index-59_85.png)

![](index-59_86.png)

![](index-59_87.png)

![](index-59_88.png)

![](index-59_89.png)

![](index-59_90.png)

![](index-59_91.png)

![](index-59_92.png)

![](index-59_93.png)

![](index-59_94.png)

![](index-59_95.png)

![](index-59_96.png)

![](index-59_97.png)

![](index-59_98.png)

![](index-59_99.png)

![](index-59_100.png)

![](index-59_101.png)

![](index-59_102.png)

![](index-59_103.png)

![](index-59_104.png)

![](index-59_105.png)

![](index-59_106.png)

![](index-59_107.png)

![](index-59_108.png)

![](index-59_109.png)

![](index-59_110.png)

![](index-59_111.png)

![](index-59_112.png)

![](index-59_113.png)

![](index-59_114.png)

![](index-59_115.png)

![](index-59_116.png)

![](index-59_117.png)

![](index-59_118.png)

![](index-59_119.png)

![](index-59_120.png)

![](index-59_121.png)

![](index-59_122.png)

![](index-59_123.png)

![](index-59_124.png)

![](index-59_125.png)

![](index-59_126.png)

![](index-59_127.png)

![](index-59_128.png)

![](index-59_129.png)

![](index-59_130.png)

![](index-59_131.png)

![](index-59_132.png)

![](index-59_133.png)

![](index-59_134.png)

![](index-59_135.png)

![](index-59_136.png)

![](index-59_137.png)

![](index-59_138.png)

![](index-59_139.png)

![](index-59_140.png)

![](index-59_141.png)

![](index-59_142.png)

![](index-59_143.png)

![](index-59_144.png)

![](index-59_145.png)

![](index-59_146.png)

![](index-59_147.png)

![](index-59_148.png)

![](index-59_149.png)

![](index-59_150.png)

![](index-59_151.png)

![](index-59_152.png)

![](index-59_153.png)

![](index-59_154.png)

![](index-59_155.png)

![](index-59_156.png)

![](index-59_157.png)

![](index-59_158.png)

![](index-59_159.png)

![](index-59_160.png)

![](index-59_161.png)

![](index-59_162.png)

![](index-59_163.png)

![](index-59_164.png)

![](index-59_165.png)

![](index-59_166.png)

![](index-59_167.png)

![](index-59_168.png)

settings page.

SAILS.JS CONTROLLERS

Controllers hold your app’s business logic. They live in api/controllers and provide a layer which glues your app’s models and views. Controllers contain actions that are bound to routes and respond to HTTP requests from web/mobile clients.

A controller is a JavaScript object that contains methods called the *controller actions*, which take two parameters: a request and a response.

You can find more information about controllers on the Sails.js controllers page.

You can generate a controller using the Sails.js CLI: sails generate controller product

This command will generate a controller named

api/controllers/ProductController.js, with the following content:

/**

* ProductController

*

* @description :: Serverside logic for managing products

* @help :: See http://sailsjs.org/#!/documentation/concepts/Controllers

*/

module.exports = {

};

The code exports an empty JavaScript object where you can add new actions or override the default (automatically added) controller actions.

At this point, you can actually execute CRUD operations against your server without further adding any code. Since Sails.js follows convention over configuration, it wires your controllers to their corresponding routes and provides default actions for handling the common HTTP POST, GET, PUT and DELETE requests etc.

TESTING WITH POSTMAN

Using Postman, you can send POST, GET and other requests to test your API, so go

![](index-60_1.png)

![](index-60_2.png)

ahead and grab the Postman version for your operating system. Next, enter the product endpoint URL http://localhost:1337/product. Then choose the HTTP method to send — POST in this case, because we want to create a Product. Next, you need to provide data, so click on the *Body tab*, select the *Raw* option, then enter the following:

{

"name": "Product 1",

"description": "This is product 1",

"quantity": 100

}

Then hit the Send button.

You should pay attention to the returned status code: 200 OK means the product was successfully created.

You can then verify if products are created by sending a GET request:

![](index-61_1.png)

You can also update a product by its id by sending a PUT request: Finally, you can delete a product by its id by sending a DELETE request:

![](index-62_1.png)

For custom logic, you can also override these actions and implement your own.

When you create an API (i.e. a controller and a model) Sails.js automatically adds eight default actions, which are:

add to

create

destroy

find one

find where

populate where

remove from

update

Find where and find one, create, update and destroy are normal CRUD

actions that needs to be present in most APIs. The others are related to foreign records: add to: used to add a foreign record to another record collection (e.g a product to a user’s products).

populate where: used to populate and return foreign record(s) for the given association of another record. Read more information here.

remove from: used to remove a foreign record (e.g. a product) from one of a related record collection association (e.g. user’s products). See more information and examples here.

For customizing the behavior of the default actions, you can do either of these: Override the action in a specified controller. That is, create an action with the same name as one of these actions: find, findOne, create, update, destroy, populate, add or remove.

Override the default action for all controllers. You can do this by creating an api/blueprints folder, where you need to add files with lowercase names for a default action (e.g. find.js, findone.js, create.js, etc.). You can find more information about blueprints by checking the Sails.js Blueprint API docs.

ROUTING IN SAILS.JS

Routes allow you to map URLs to controllers or views. Just like the default actions, Sails.js automatically adds default routes for the default actions, allowing you to have an automatic API by just creating models and controllers.

You can also add custom routes for your custom actions or views. To add a route, open the config/routes.js file and add this:

module.exports.routes = {

'/products': {

view: 'products'

}

};

This maps /products to the template named *products* in views folder.

You can optionally add an HTTP verb to the URL. For example:

module.exports.routes = {

'get /': {

view: 'homepage'

}

};

You can also specify a controller action for a route. For example: module.exports.routes = {

'post /product': 'ProductController.create',

};

This tells Sails.js to call the *create* action of the *ProductController* controller when a client sends a POST request to the /product endpoint.

Conclusion

In this chapter, you were introduced to Sails.js. We looked at the basic concepts of Sails.js, and how to generate a new Sails.js project, and then created an API by just generating models, adding some attributes then generate controllers. Sails.js has other advanced concepts such as services, policies, blueprints and hooks. These you can further discover on your own, once you grasp and get familiar with the basic concepts in this introduction.

![](index-65_1.png)

![](index-65_2.png)

![](index-65_3.png)

![](index-65_4.png)

![](index-65_5.png)

![](index-65_6.png)

![](index-65_7.png)

![](index-65_8.png)

![](index-65_9.png)

![](index-65_10.png)

![](index-65_11.png)

![](index-65_12.png)

![](index-65_13.png)

![](index-65_14.png)

![](index-65_15.png)

![](index-65_16.png)

![](index-65_17.png)

![](index-65_18.png)

![](index-65_19.png)

![](index-65_20.png)

![](index-65_21.png)

![](index-65_22.png)

![](index-65_23.png)

![](index-65_24.png)

![](index-65_25.png)

![](index-65_26.png)

![](index-65_27.png)

![](index-65_28.png)

![](index-65_29.png)

![](index-65_30.png)

![](index-65_31.png)

![](index-65_32.png)

![](index-65_33.png)

![](index-65_34.png)

![](index-65_35.png)

![](index-65_36.png)

![](index-65_37.png)

![](index-65_38.png)

![](index-65_39.png)

![](index-65_40.png)

![](index-65_41.png)

![](index-65_42.png)

![](index-65_43.png)

![](index-65_44.png)

![](index-65_45.png)

![](index-65_46.png)

![](index-65_47.png)

![](index-65_48.png)

![](index-65_49.png)

![](index-65_50.png)

![](index-65_51.png)

![](index-65_52.png)

![](index-65_53.png)

![](index-65_54.png)

![](index-65_55.png)

![](index-65_56.png)

![](index-65_57.png)

![](index-65_58.png)

![](index-65_59.png)

![](index-65_60.png)

![](index-65_61.png)

![](index-65_62.png)

![](index-65_63.png)

![](index-65_64.png)

![](index-65_65.png)

![](index-65_66.png)

![](index-65_67.png)

![](index-65_68.png)

![](index-65_69.png)

![](index-65_70.png)

![](index-65_71.png)

![](index-65_72.png)

![](index-65_73.png)

![](index-65_74.png)

![](index-65_75.png)

![](index-65_76.png)

![](index-65_77.png)

![](index-65_78.png)

![](index-65_79.png)

![](index-65_80.png)

![](index-65_81.png)

![](index-65_82.png)

![](index-65_83.png)

![](index-65_84.png)

![](index-65_85.png)

![](index-65_86.png)

![](index-65_87.png)

![](index-65_88.png)

![](index-65_89.png)

![](index-65_90.png)

![](index-65_91.png)

![](index-65_92.png)

![](index-65_93.png)

![](index-65_94.png)

![](index-65_95.png)

![](index-65_96.png)

![](index-65_97.png)

![](index-65_98.png)

![](index-65_99.png)

![](index-65_100.png)

![](index-65_101.png)

![](index-65_102.png)

![](index-65_103.png)

![](index-65_104.png)

![](index-65_105.png)

![](index-65_106.png)

![](index-65_107.png)

![](index-65_108.png)

![](index-65_109.png)

![](index-65_110.png)

![](index-65_111.png)

![](index-65_112.png)

![](index-65_113.png)

![](index-65_114.png)

![](index-65_115.png)

![](index-65_116.png)

![](index-65_117.png)

![](index-65_118.png)

![](index-65_119.png)

![](index-65_120.png)

![](index-65_121.png)

![](index-65_122.png)

![](index-65_123.png)

![](index-65_124.png)

![](index-65_125.png)

![](index-65_126.png)

![](index-65_127.png)

![](index-65_128.png)

![](index-65_129.png)

![](index-65_130.png)

![](index-65_131.png)

![](index-65_132.png)

![](index-65_133.png)

![](index-65_134.png)

![](index-65_135.png)

![](index-65_136.png)

![](index-65_137.png)

![](index-65_138.png)

![](index-65_139.png)

![](index-65_140.png)

![](index-65_141.png)

![](index-65_142.png)

![](index-65_143.png)

![](index-65_144.png)

![](index-65_145.png)

![](index-65_146.png)

![](index-65_147.png)

![](index-65_148.png)

![](index-65_149.png)

![](index-65_150.png)

![](index-65_151.png)

![](index-65_152.png)

![](index-65_153.png)

![](index-65_154.png)

![](index-65_155.png)

![](index-65_156.png)

![](index-65_157.png)

![](index-65_158.png)

![](index-65_159.png)

![](index-65_160.png)

![](index-65_161.png)

![](index-65_162.png)

![](index-65_163.png)

![](index-65_164.png)

![](index-65_165.png)

![](index-65_166.png)

![](index-65_167.png)

![](index-65_168.png)

![](index-65_169.png)

![](index-65_170.png)

![](index-65_171.png)

![](index-65_172.png)

![](index-65_173.png)

![](index-65_174.png)

HisC

tor h

y apter 6: Building Apps and Services with

To t

pi h

cs e Hapi.js Framework

Tu B

torYia lM

s ARK BROWN

Hapi.js is described as “a rich framework for building applications and Offers & Deals

services”. Hapi’s smart defaults make it a breeze to create JSON APIs, and its modular design and plugin system allow you to easily extend or modify Highlights

its behavior.

Settings

The recent release of version 17.0 has fully embraced async and await, so you’ll be writing code that appears synchronous but is nonblocking *and* avoids callback hell.

Support

Winwin.

Sign Out

The Project

In this article, we’ll be building the following API for a typical blog from scratch:

# RESTful actions for fetching, creating, updating and deleting articles GET /articles articles#index

GET /articles/:id articles#show

POST /articles articles#create

PUT /articles/:id articles#update

DELETE /articles/:id articles#destroy

# Nested routes for creating and deleting comments POST /articles/:id/comments comments#create

DELETE /articles/:id/comments comments#destroy

# Authentication with JSON Web Tokens (JWT)

POST /authentications authentications#create T

he articl

e wil lcover:

Hapi’s core API: routing, request and response

models and persistence in a relational database routes and actions for Articles and Comments

testing a REST API with HTTPie

authentication with JWT and securing routes

validation

an HTML View and Layout for the root route /.

The Starting Point

Make sure you’ve got a recent version of Node.js installed; node v should return 8.9.0 or higher.

Download the starting code from here with git:

git clone https://github.com/markbrown4/hapiapi.git cd hapiapi

npm install

Open up package.json and you’ll see that the “start” script runs server.js with nodemon. This will take care of restarting the server for us when we change a file.

Run npm start and open http://localhost:3000/:

[{ "so": "hapi!" }]

Let’s look at the source:

// server.js

const Hapi = require('hapi')

// Configure the server instance

const server = Hapi.server({

host: 'localhost',

port: 3000

})

// Add routes

server.route({

method: 'GET',

path: '/',

handler: () =&gt; {

![](index-67_1.png)

![](index-67_2.png)

![](index-67_3.png)

![](index-67_4.png)

![](index-67_5.png)

![](index-67_6.png)

![](index-67_7.png)

![](index-67_8.png)

![](index-67_9.png)

![](index-67_10.png)

![](index-67_11.png)

![](index-67_12.png)

![](index-67_13.png)

![](index-67_14.png)

![](index-67_15.png)

![](index-67_16.png)

![](index-67_17.png)

![](index-67_18.png)

![](index-67_19.png)

![](index-67_20.png)

![](index-67_21.png)

![](index-67_22.png)

![](index-67_23.png)

![](index-67_24.png)

![](index-67_25.png)

![](index-67_26.png)

![](index-67_27.png)

![](index-67_28.png)

![](index-67_29.png)

![](index-67_30.png)

![](index-67_31.png)

![](index-67_32.png)

![](index-67_33.png)

![](index-67_34.png)

![](index-67_35.png)

![](index-67_36.png)

![](index-67_37.png)

![](index-67_38.png)

![](index-67_39.png)

![](index-67_40.png)

![](index-67_41.png)

![](index-67_42.png)

![](index-67_43.png)

![](index-67_44.png)

![](index-67_45.png)

![](index-67_46.png)

![](index-67_47.png)

![](index-67_48.png)

![](index-67_49.png)

![](index-67_50.png)

![](index-67_51.png)

![](index-67_52.png)

![](index-67_53.png)

![](index-67_54.png)

![](index-67_55.png)

![](index-67_56.png)

![](index-67_57.png)

![](index-67_58.png)

![](index-67_59.png)

![](index-67_60.png)

![](index-67_61.png)

![](index-67_62.png)

![](index-67_63.png)

![](index-67_64.png)

![](index-67_65.png)

![](index-67_66.png)

![](index-67_67.png)

![](index-67_68.png)

![](index-67_69.png)

![](index-67_70.png)

![](index-67_71.png)

![](index-67_72.png)

![](index-67_73.png)

![](index-67_74.png)

![](index-67_75.png)

![](index-67_76.png)

![](index-67_77.png)

![](index-67_78.png)

![](index-67_79.png)

![](index-67_80.png)

![](index-67_81.png)

![](index-67_82.png)

![](index-67_83.png)

![](index-67_84.png)

![](index-67_85.png)

![](index-67_86.png)

![](index-67_87.png)

![](index-67_88.png)

![](index-67_89.png)

![](index-67_90.png)

![](index-67_91.png)

![](index-67_92.png)

![](index-67_93.png)

![](index-67_94.png)

![](index-67_95.png)

![](index-67_96.png)

![](index-67_97.png)

![](index-67_98.png)

![](index-67_99.png)

![](index-67_100.png)

![](index-67_101.png)

![](index-67_102.png)

![](index-67_103.png)

![](index-67_104.png)

![](index-67_105.png)

![](index-67_106.png)

![](index-67_107.png)

![](index-67_108.png)

![](index-67_109.png)

![](index-67_110.png)

![](index-67_111.png)

![](index-67_112.png)

![](index-67_113.png)

![](index-67_114.png)

![](index-67_115.png)

![](index-67_116.png)

![](index-67_117.png)

![](index-67_118.png)

![](index-67_119.png)

![](index-67_120.png)

![](index-67_121.png)

![](index-67_122.png)

![](index-67_123.png)

![](index-67_124.png)

![](index-67_125.png)

![](index-67_126.png)

![](index-67_127.png)

![](index-67_128.png)

![](index-67_129.png)

![](index-67_130.png)

![](index-67_131.png)

![](index-67_132.png)

![](index-67_133.png)

![](index-67_134.png)

![](index-67_135.png)

![](index-67_136.png)

![](index-67_137.png)

![](index-67_138.png)

![](index-67_139.png)

![](index-67_140.png)

![](index-67_141.png)

![](index-67_142.png)

![](index-67_143.png)

![](index-67_144.png)

![](index-67_145.png)

![](index-67_146.png)

![](index-67_147.png)

![](index-67_148.png)

![](index-67_149.png)

![](index-67_150.png)

![](index-67_151.png)

![](index-67_152.png)

![](index-67_153.png)

![](index-67_154.png)

![](index-67_155.png)

![](index-67_156.png)

![](index-67_157.png)

![](index-67_158.png)

![](index-67_159.png)

![](index-67_160.png)

![](index-67_161.png)

![](index-67_162.png)

![](index-67_163.png)

![](index-67_164.png)

![](index-67_165.png)

![](index-67_166.png)

![](index-67_167.png)

![](index-67_168.png)

![](index-67_169.png)

![](index-67_170.png)

![](index-67_171.png)

![](index-67_172.png)

![](index-67_173.png)

![](index-67_174.png)

return [{ so: 'hapi!' }]

}

})

// Go!

server.start().then(() =&gt; {

console.log('Server running at:', server.info.uri)

}).catch(err =&gt; {

console.log(err)

process.exit(1)

})

The Route Handler

The route handler is the most interesting part of this code. Replace it with the code below, comment out the return lines one by one, and test the response in your browser.

server.route({

method: 'GET',

path: '/',

handler: () =&gt; {

// return [{ so: 'hapi!' }]

return 123

return `&lt;h1&gt;&lt;marquee&gt;HTML &lt;em&gt;rules!&lt;/em&gt;&lt;/marquee&gt;&lt;/h1&gt;`

return null

return new Error('Boom')

return Promise.resolve({ whoa: true })

return require('fs').createReadStream('index.html')

}

})

To send a response, you simply return a value and Hapi will send the appropriate body and headers.

An Object will respond with stringified JSON and ContentType: application/json

String values will be ContentType: text/html

You can also return a Promise or Stream.

The handler function is often made async for cleaner control flow with Promises: server.route({

method: 'GET',

path: '/',

handler: async () =&gt; {

let html = await Promise.resolve(`&lt;h1&gt;Google&lt;h1&gt;`) html = html.replace('Google', 'Hapi')

return html

}

})

It’s not *always* cleaner with async though. Sometimes returning a Promise is simpler: handler: () =&gt; {

return Promise.resolve(`&lt;h1&gt;Google&lt;h1&gt;`)

.then(html =&gt; html.replace('Google', 'Hapi'))

}

We’ll see better examples of how async helps us out when we start interacting with the database.

The Model Layer

Like the popular Express.js framework, Hapi is a minimal framework that doesn’t provide any recommendations for the Model layer or persistence. You can choose any database and ORM that you’d like, or none — it’s up to you. We’ll be using SQLite and the Sequelize ORM in this tutorial to provide a clean API for interacting with the database.

SQLite comes preinstalled on macOS and most Linux distributions. You can check if it’s installed with sqlite v. If not, you can find installation instructions at the SQLite website.

Sequelize works with many popular relational databases like Postgres or MySQL, so you’ll need to install both sequelize and the sqlite3 adapter: npm install save sequelize sqlite3

Let’s connect to our database and write our first table definition for articles:

// models.js

const path = require('path')

const Sequelize = require('sequelize')

![](index-69_1.png)

![](index-69_2.png)

![](index-69_3.png)

![](index-69_4.png)

![](index-69_5.png)

![](index-69_6.png)

![](index-69_7.png)

![](index-69_8.png)

![](index-69_9.png)

![](index-69_10.png)

![](index-69_11.png)

![](index-69_12.png)

![](index-69_13.png)

![](index-69_14.png)

![](index-69_15.png)

![](index-69_16.png)

![](index-69_17.png)

![](index-69_18.png)

![](index-69_19.png)

![](index-69_20.png)

![](index-69_21.png)

![](index-69_22.png)

![](index-69_23.png)

![](index-69_24.png)

![](index-69_25.png)

![](index-69_26.png)

![](index-69_27.png)

![](index-69_28.png)

![](index-69_29.png)

![](index-69_30.png)

![](index-69_31.png)

![](index-69_32.png)

![](index-69_33.png)

![](index-69_34.png)

![](index-69_35.png)

![](index-69_36.png)

![](index-69_37.png)

![](index-69_38.png)

![](index-69_39.png)

![](index-69_40.png)

![](index-69_41.png)

![](index-69_42.png)

![](index-69_43.png)

![](index-69_44.png)

![](index-69_45.png)

![](index-69_46.png)

![](index-69_47.png)

![](index-69_48.png)

![](index-69_49.png)

![](index-69_50.png)

![](index-69_51.png)

![](index-69_52.png)

![](index-69_53.png)

![](index-69_54.png)

![](index-69_55.png)

![](index-69_56.png)

![](index-69_57.png)

![](index-69_58.png)

![](index-69_59.png)

![](index-69_60.png)

![](index-69_61.png)

![](index-69_62.png)

![](index-69_63.png)

![](index-69_64.png)

![](index-69_65.png)

![](index-69_66.png)

![](index-69_67.png)

![](index-69_68.png)

![](index-69_69.png)

![](index-69_70.png)

![](index-69_71.png)

![](index-69_72.png)

![](index-69_73.png)

![](index-69_74.png)

![](index-69_75.png)

![](index-69_76.png)

![](index-69_77.png)

![](index-69_78.png)

![](index-69_79.png)

![](index-69_80.png)

![](index-69_81.png)

![](index-69_82.png)

![](index-69_83.png)

![](index-69_84.png)

![](index-69_85.png)

![](index-69_86.png)

![](index-69_87.png)

![](index-69_88.png)

![](index-69_89.png)

![](index-69_90.png)

![](index-69_91.png)

![](index-69_92.png)

![](index-69_93.png)

![](index-69_94.png)

![](index-69_95.png)

![](index-69_96.png)

![](index-69_97.png)

![](index-69_98.png)

![](index-69_99.png)

![](index-69_100.png)

![](index-69_101.png)

![](index-69_102.png)

![](index-69_103.png)

![](index-69_104.png)

![](index-69_105.png)

![](index-69_106.png)

![](index-69_107.png)

![](index-69_108.png)

![](index-69_109.png)

![](index-69_110.png)

![](index-69_111.png)

![](index-69_112.png)

![](index-69_113.png)

![](index-69_114.png)

![](index-69_115.png)

![](index-69_116.png)

![](index-69_117.png)

![](index-69_118.png)

![](index-69_119.png)

![](index-69_120.png)

![](index-69_121.png)

![](index-69_122.png)

![](index-69_123.png)

![](index-69_124.png)

![](index-69_125.png)

![](index-69_126.png)

![](index-69_127.png)

![](index-69_128.png)

![](index-69_129.png)

![](index-69_130.png)

![](index-69_131.png)

![](index-69_132.png)

![](index-69_133.png)

![](index-69_134.png)

![](index-69_135.png)

![](index-69_136.png)

![](index-69_137.png)

![](index-69_138.png)

![](index-69_139.png)

![](index-69_140.png)

![](index-69_141.png)

![](index-69_142.png)

![](index-69_143.png)

![](index-69_144.png)

![](index-69_145.png)

![](index-69_146.png)

![](index-69_147.png)

![](index-69_148.png)

![](index-69_149.png)

![](index-69_150.png)

![](index-69_151.png)

![](index-69_152.png)

![](index-69_153.png)

![](index-69_154.png)

![](index-69_155.png)

![](index-69_156.png)

![](index-69_157.png)

![](index-69_158.png)

![](index-69_159.png)

![](index-69_160.png)

![](index-69_161.png)

![](index-69_162.png)

![](index-69_163.png)

![](index-69_164.png)

![](index-69_165.png)

![](index-69_166.png)

![](index-69_167.png)

![](index-69_168.png)

![](index-69_169.png)

![](index-69_170.png)

![](index-69_171.png)

![](index-69_172.png)

![](index-69_173.png)

![](index-69_174.png)

![](index-69_175.png)

![](index-69_176.png)

![](index-69_177.png)

![](index-69_178.png)

![](index-69_179.png)

![](index-69_180.png)

![](index-69_181.png)

![](index-69_182.png)

![](index-69_183.png)

![](index-69_184.png)

![](index-69_185.png)

![](index-69_186.png)

![](index-69_187.png)

![](index-69_188.png)

![](index-69_189.png)

![](index-69_190.png)

![](index-69_191.png)

![](index-69_192.png)

![](index-69_193.png)

![](index-69_194.png)

![](index-69_195.png)

![](index-69_196.png)

![](index-69_197.png)

![](index-69_198.png)

![](index-69_199.png)

![](index-69_200.png)

![](index-69_201.png)

![](index-69_202.png)

![](index-69_203.png)

![](index-69_204.png)

![](index-69_205.png)

![](index-69_206.png)

![](index-69_207.png)

![](index-69_208.png)

![](index-69_209.png)

![](index-69_210.png)

![](index-69_211.png)

![](index-69_212.png)

![](index-69_213.png)

![](index-69_214.png)

![](index-69_215.png)

![](index-69_216.png)

![](index-69_217.png)

![](index-69_218.png)

![](index-69_219.png)

![](index-69_220.png)

![](index-69_221.png)

![](index-69_222.png)

![](index-69_223.png)

![](index-69_224.png)

![](index-69_225.png)

![](index-69_226.png)

![](index-69_227.png)

![](index-69_228.png)

![](index-69_229.png)

![](index-69_230.png)

![](index-69_231.png)

![](index-69_232.png)

![](index-69_233.png)

![](index-69_234.png)

![](index-69_235.png)

![](index-69_236.png)

![](index-69_237.png)

![](index-69_238.png)

![](index-69_239.png)

![](index-69_240.png)

![](index-69_241.png)

![](index-69_242.png)

![](index-69_243.png)

![](index-69_244.png)

![](index-69_245.png)

![](index-69_246.png)

![](index-69_247.png)

![](index-69_248.png)

![](index-69_249.png)

![](index-69_250.png)

![](index-69_251.png)

![](index-69_252.png)

![](index-69_253.png)

![](index-69_254.png)

![](index-69_255.png)

![](index-69_256.png)

![](index-69_257.png)

![](index-69_258.png)

![](index-69_259.png)

![](index-69_260.png)

![](index-69_261.png)

![](index-69_262.png)

![](index-69_263.png)

![](index-69_264.png)

![](index-69_265.png)

![](index-69_266.png)

![](index-69_267.png)

![](index-69_268.png)

![](index-69_269.png)

![](index-69_270.png)

![](index-69_271.png)

![](index-69_272.png)

![](index-69_273.png)

![](index-69_274.png)

![](index-69_275.png)

![](index-69_276.png)

![](index-69_277.png)

![](index-69_278.png)

![](index-69_279.png)

![](index-69_280.png)

![](index-69_281.png)

![](index-69_282.png)

![](index-69_283.png)

![](index-69_284.png)

![](index-69_285.png)

![](index-69_286.png)

![](index-69_287.png)

![](index-69_288.png)

![](index-69_289.png)

![](index-69_290.png)

![](index-69_291.png)

![](index-69_292.png)

![](index-69_293.png)

![](index-69_294.png)

![](index-69_295.png)

![](index-69_296.png)

![](index-69_297.png)

![](index-69_298.png)

![](index-69_299.png)

![](index-69_300.png)

![](index-69_301.png)

![](index-69_302.png)

![](index-69_303.png)

![](index-69_304.png)

![](index-69_305.png)

![](index-69_306.png)

![](index-69_307.png)

![](index-69_308.png)

![](index-69_309.png)

![](index-69_310.png)

![](index-69_311.png)

![](index-69_312.png)

![](index-69_313.png)

![](index-69_314.png)

![](index-69_315.png)

![](index-69_316.png)

![](index-69_317.png)

![](index-69_318.png)

![](index-69_319.png)

![](index-69_320.png)

![](index-69_321.png)

![](index-69_322.png)

![](index-69_323.png)

![](index-69_324.png)

![](index-69_325.png)

![](index-69_326.png)

![](index-69_327.png)

![](index-69_328.png)

![](index-69_329.png)

![](index-69_330.png)

![](index-69_331.png)

![](index-69_332.png)

![](index-69_333.png)

![](index-69_334.png)

![](index-69_335.png)

![](index-69_336.png)

// configure connection to db host, user, pass not required for SQLite const sequelize = new Sequelize(null, null, null, {

dialect: 'sqlite',

storage: path.join('tmp', 'db.sqlite') // SQLite persists its data directly to file

})

// Here we define our Article model with a title attribute of type string, and a body attribute of type text. By default, all tables get columns for id, createdAt, updatedAt as well.

const Article = sequelize.define('article', {

title: Sequelize.STRING,

body: Sequelize.TEXT

})

// Create table

Article.sync()

module.exports = {

Article

}

Let’s test out our new model by importing it and replacing our route handler with the following:

// server.js

const { Article } = require('./models')

server.route({

method: 'GET',

path: '/',

handler: () =&gt; {

// try commenting these lines out one at a time

return Article.findAll()

return Article.create({ title: 'Welcome to my blog', body: 'The happiest place on earth' }) return Article.findById(1)

return Article.update({ title: 'Learning Hapi', body: `JSON API's a breeze.` }, { where: { id: 1 } }) return Article.findAll()

return Article.destroy({ where: { id: 1 } })

return Article.findAll()

}

})

If you’re familiar with SQL or other ORM’s, the Sequelize API should be self explanatory, It’s built with Promises so it works great with Hapi’s async handlers too.

*Note: using* Article.sync() *to create the tables or* Article.sync({ force: true }) *to* drop *and create are fine for the purposes of this demo. If you’re wanting* *to use this in production you should check out sequelizecli and write Migrations for*

*any schema changes.*

Our RESTful Actions

Let’s build the following routes:

GET /articles fetch all articles

GET /articles/:id fetch article by id

POST /articles create article with `{ title, body }` params PUT /articles/:id update article with `{ title, body }` params DELETE /articles/:id delete article by id

Add a new file, routes.js, to separate the server config from the application logic:

// routes.js

const { Article } = require('./models')

exports.configureRoutes = (server) =&gt; {

// server.route accepts an object or an array

return server.route([{

method: 'GET',

path: '/articles',

handler: () =&gt; {

return Article.findAll()

}

}, {

method: 'GET',

// The curly braces are how we define params (variable path segments in the URL) path: '/articles/{id}',

handler: (request) =&gt; {

return Article.findById(request.params.id)

}

}, {

method: 'POST',

path: '/articles',

handler: (request) =&gt; {

const article = Article.build(request.payload.article) return article.save()

}

}, {

// method can be an array

method: ['PUT', 'PATCH'],

path: '/articles/{id}',

handler: async (request) =&gt; {

const article = await Article.findById(request.params.id) article.update(request.payload.article)

return article.save()

![](index-71_1.png)

![](index-71_2.png)

![](index-71_3.png)

![](index-71_4.png)

![](index-71_5.png)

![](index-71_6.png)

![](index-71_7.png)

![](index-71_8.png)

![](index-71_9.png)

![](index-71_10.png)

![](index-71_11.png)

![](index-71_12.png)

![](index-71_13.png)

![](index-71_14.png)

![](index-71_15.png)

![](index-71_16.png)

![](index-71_17.png)

![](index-71_18.png)

![](index-71_19.png)

![](index-71_20.png)

![](index-71_21.png)

![](index-71_22.png)

![](index-71_23.png)

![](index-71_24.png)

![](index-71_25.png)

![](index-71_26.png)

![](index-71_27.png)

![](index-71_28.png)

![](index-71_29.png)

![](index-71_30.png)

![](index-71_31.png)

![](index-71_32.png)

![](index-71_33.png)

![](index-71_34.png)

![](index-71_35.png)

![](index-71_36.png)

![](index-71_37.png)

![](index-71_38.png)

![](index-71_39.png)

![](index-71_40.png)

![](index-71_41.png)

![](index-71_42.png)

![](index-71_43.png)

![](index-71_44.png)

![](index-71_45.png)

![](index-71_46.png)

![](index-71_47.png)

![](index-71_48.png)

![](index-71_49.png)

![](index-71_50.png)

![](index-71_51.png)

![](index-71_52.png)

![](index-71_53.png)

![](index-71_54.png)

![](index-71_55.png)

![](index-71_56.png)

![](index-71_57.png)

![](index-71_58.png)

![](index-71_59.png)

![](index-71_60.png)

![](index-71_61.png)

![](index-71_62.png)

![](index-71_63.png)

![](index-71_64.png)

![](index-71_65.png)

![](index-71_66.png)

![](index-71_67.png)

![](index-71_68.png)

![](index-71_69.png)

![](index-71_70.png)

![](index-71_71.png)

![](index-71_72.png)

![](index-71_73.png)

![](index-71_74.png)

![](index-71_75.png)

![](index-71_76.png)

![](index-71_77.png)

![](index-71_78.png)

![](index-71_79.png)

![](index-71_80.png)

![](index-71_81.png)

![](index-71_82.png)

![](index-71_83.png)

![](index-71_84.png)

![](index-71_85.png)

![](index-71_86.png)

![](index-71_87.png)

![](index-71_88.png)

![](index-71_89.png)

![](index-71_90.png)

![](index-71_91.png)

![](index-71_92.png)

![](index-71_93.png)

![](index-71_94.png)

![](index-71_95.png)

![](index-71_96.png)

![](index-71_97.png)

![](index-71_98.png)

![](index-71_99.png)

![](index-71_100.png)

![](index-71_101.png)

![](index-71_102.png)

![](index-71_103.png)

![](index-71_104.png)

![](index-71_105.png)

![](index-71_106.png)

![](index-71_107.png)

![](index-71_108.png)

![](index-71_109.png)

![](index-71_110.png)

![](index-71_111.png)

![](index-71_112.png)

![](index-71_113.png)

![](index-71_114.png)

![](index-71_115.png)

![](index-71_116.png)

![](index-71_117.png)

![](index-71_118.png)

![](index-71_119.png)

![](index-71_120.png)

![](index-71_121.png)

![](index-71_122.png)

![](index-71_123.png)

![](index-71_124.png)

![](index-71_125.png)

![](index-71_126.png)

![](index-71_127.png)

![](index-71_128.png)

![](index-71_129.png)

![](index-71_130.png)

![](index-71_131.png)

![](index-71_132.png)

![](index-71_133.png)

![](index-71_134.png)

![](index-71_135.png)

![](index-71_136.png)

![](index-71_137.png)

![](index-71_138.png)

![](index-71_139.png)

![](index-71_140.png)

![](index-71_141.png)

![](index-71_142.png)

![](index-71_143.png)

![](index-71_144.png)

![](index-71_145.png)

![](index-71_146.png)

![](index-71_147.png)

![](index-71_148.png)

![](index-71_149.png)

![](index-71_150.png)

![](index-71_151.png)

![](index-71_152.png)

![](index-71_153.png)

![](index-71_154.png)

![](index-71_155.png)

![](index-71_156.png)

![](index-71_157.png)

![](index-71_158.png)

![](index-71_159.png)

![](index-71_160.png)

![](index-71_161.png)

![](index-71_162.png)

![](index-71_163.png)

![](index-71_164.png)

![](index-71_165.png)

![](index-71_166.png)

![](index-71_167.png)

![](index-71_168.png)

![](index-71_169.png)

![](index-71_170.png)

![](index-71_171.png)

![](index-71_172.png)

![](index-71_173.png)

![](index-71_174.png)

![](index-71_175.png)

![](index-71_176.png)

![](index-71_177.png)

![](index-71_178.png)

![](index-71_179.png)

![](index-71_180.png)

}

}, {

method: 'DELETE',

path: '/articles/{id}',

handler: async (request) =&gt; {

const article = await Article.findById(request.params.id) return article.destroy()

}

}])

}

Import and configure our routes before we start the server:

// server.js

const Hapi = require('hapi')

const { configureRoutes } = require('./routes')

const server = Hapi.server({

host: 'localhost',

port: 3000

})

// This function will allow us to easily extend it later const main = async () =&gt; {

await configureRoutes(server)

await server.start()

return server

}

main().then(server =&gt; {

console.log('Server running at:', server.info.uri)

}).catch(err =&gt; {

console.log(err)

process.exit(1)

})

Testing Our API Is as Easy as HTTPie

HTTPie is great little commandline HTTP client that works on all operating systems.

Follow the installation instructions in the documentation and then try hitting the API from the terminal:

http GET http://localhost:3000/articles

http POST http://localhost:3000/articles article:='{"title": "Welcome to my blog", "body": "The greatest place on earth"}'

http POST http://localhost:3000/articles article:='{"title": "Learning Hapi", "body": "JSON APIs a breeze."}'

![](index-72_1.png)

![](index-72_2.png)

![](index-72_3.png)

![](index-72_4.png)

![](index-72_5.png)

![](index-72_6.png)

![](index-72_7.png)

![](index-72_8.png)

![](index-72_9.png)

![](index-72_10.png)

![](index-72_11.png)

![](index-72_12.png)

![](index-72_13.png)

![](index-72_14.png)

![](index-72_15.png)

![](index-72_16.png)

![](index-72_17.png)

![](index-72_18.png)

![](index-72_19.png)

![](index-72_20.png)

![](index-72_21.png)

![](index-72_22.png)

![](index-72_23.png)

![](index-72_24.png)

![](index-72_25.png)

![](index-72_26.png)

![](index-72_27.png)

![](index-72_28.png)

![](index-72_29.png)

![](index-72_30.png)

![](index-72_31.png)

![](index-72_32.png)

![](index-72_33.png)

![](index-72_34.png)

![](index-72_35.png)

![](index-72_36.png)

![](index-72_37.png)

![](index-72_38.png)

![](index-72_39.png)

![](index-72_40.png)

![](index-72_41.png)

![](index-72_42.png)

![](index-72_43.png)

![](index-72_44.png)

![](index-72_45.png)

![](index-72_46.png)

![](index-72_47.png)

![](index-72_48.png)

![](index-72_49.png)

![](index-72_50.png)

![](index-72_51.png)

![](index-72_52.png)

![](index-72_53.png)

![](index-72_54.png)

![](index-72_55.png)

![](index-72_56.png)

![](index-72_57.png)

![](index-72_58.png)

![](index-72_59.png)

![](index-72_60.png)

![](index-72_61.png)

![](index-72_62.png)

![](index-72_63.png)

![](index-72_64.png)

![](index-72_65.png)

![](index-72_66.png)

![](index-72_67.png)

![](index-72_68.png)

![](index-72_69.png)

![](index-72_70.png)

![](index-72_71.png)

![](index-72_72.png)

![](index-72_73.png)

![](index-72_74.png)

![](index-72_75.png)

![](index-72_76.png)

![](index-72_77.png)

![](index-72_78.png)

![](index-72_79.png)

![](index-72_80.png)

![](index-72_81.png)

![](index-72_82.png)

![](index-72_83.png)

![](index-72_84.png)

![](index-72_85.png)

![](index-72_86.png)

![](index-72_87.png)

![](index-72_88.png)

![](index-72_89.png)

![](index-72_90.png)

![](index-72_91.png)

![](index-72_92.png)

![](index-72_93.png)

![](index-72_94.png)

![](index-72_95.png)

![](index-72_96.png)

![](index-72_97.png)

![](index-72_98.png)

![](index-72_99.png)

![](index-72_100.png)

![](index-72_101.png)

![](index-72_102.png)

![](index-72_103.png)

![](index-72_104.png)

![](index-72_105.png)

![](index-72_106.png)

![](index-72_107.png)

![](index-72_108.png)

![](index-72_109.png)

![](index-72_110.png)

![](index-72_111.png)

![](index-72_112.png)

![](index-72_113.png)

![](index-72_114.png)

![](index-72_115.png)

![](index-72_116.png)

![](index-72_117.png)

![](index-72_118.png)

![](index-72_119.png)

![](index-72_120.png)

![](index-72_121.png)

![](index-72_122.png)

![](index-72_123.png)

![](index-72_124.png)

![](index-72_125.png)

![](index-72_126.png)

![](index-72_127.png)

![](index-72_128.png)

![](index-72_129.png)

![](index-72_130.png)

![](index-72_131.png)

![](index-72_132.png)

![](index-72_133.png)

![](index-72_134.png)

![](index-72_135.png)

![](index-72_136.png)

![](index-72_137.png)

![](index-72_138.png)

![](index-72_139.png)

![](index-72_140.png)

![](index-72_141.png)

![](index-72_142.png)

![](index-72_143.png)

![](index-72_144.png)

![](index-72_145.png)

![](index-72_146.png)

![](index-72_147.png)

![](index-72_148.png)

![](index-72_149.png)

![](index-72_150.png)

![](index-72_151.png)

![](index-72_152.png)

![](index-72_153.png)

![](index-72_154.png)

![](index-72_155.png)

![](index-72_156.png)

![](index-72_157.png)

![](index-72_158.png)

![](index-72_159.png)

![](index-72_160.png)

![](index-72_161.png)

![](index-72_162.png)

![](index-72_163.png)

![](index-72_164.png)

![](index-72_165.png)

![](index-72_166.png)

![](index-72_167.png)

![](index-72_168.png)

http GET http://localhost:3000/articles

http GET http://localhost:3000/articles/2

http PUT http://localhost:3000/articles/2 article:='{"title": "True happiness, is an inner quality"}'

http GET http://localhost:3000/articles/2

http DELETE http://localhost:3000/articles/2

http GET http://localhost:3000/articles

Okay, everything seems to be working well. Let’s try a few more: http GET http://localhost:3000/articles/12345

http DELETE http://localhost:3000/articles/12345

*Yikes*! When we try to fetch an article that doesn’t exist, we get a 200 with an empty body and our destroy handler throws an Error which results in a 500\. This is happening because findById returns null by default when it can’t find a record. We want our API to respond with a 404 in both of these cases. There’s a few ways we can achieve this.

DEFENSIVELY CHECK FOR NULL VALUES AND RETURN AN ERROR

There’s a package called boom which helps create standard error response objects: npm install save boom

Import it and modify GET /articles/:id route:

// routes.js

const Boom = require('boom')

{

method: 'GET',

path: '/articles/{id}',

handler: async (request) =&gt; {

const article = await Article.findById(request.params.id) if (article === null) return Boom.notFound()

return article

}

}

EXTEND SEQUELIZE.MODEL TO THROW AN ERROR

Sequelize.Model is a reference to the prototype that all of our Models inherit from,

so we can easily add a new method find to findById and throw an error if it returns null:

// models.js

const Boom = require('boom')

Sequelize.Model.find = async function (...args) {

const obj = await this.findById(...args)

if (obj === null) throw Boom.notFound()

return obj

}

We can then revert the handler to its former glory and replace occurrences of findById with find:

{

method: 'GET',

path: '/articles/{id}',

handler: (request) =&gt; {

return Article.find(request.params.id)

}

}

http GET http://localhost:3000/articles/12345

http DELETE http://localhost:3000/articles/12345

*Boom*. We now get a 404 *Not Found* error whenever we try to fetch something from the database that doesn’t exist. We’ve replaced our custom error checks with an easytounderstand convention that keeps our code clean.

*Note: another popular tool for making requests to REST APIs is Postman. If you* *prefer a UI and ability to save common requests, this is a great option.*

Path Parameters

The routing in Hapi is a little different from other frameworks. The route is selected on the *specificity* of the path, so the order you define them in doesn’t matter.

/hello/{name} matches /hello/bob and passes 'bob' as the *name* param

/hello/{name?} — the ? makes name optional and matches both /hello and

/hello/bob

/hello/{name*2} — the * denotes multiple segments, matching

/hello/bob/marley by passing 'bob/marley' as the *name* param

/{args*} matches /any/route/imaginable and has the lowest specificity.

The Request Object

The request object that’s passed to the route handler has the following useful properties:

request.params — path params

request.query — query string params

request.payload — request body for JSON or form params request.state — cookies

request.headers

request.url

Adding a Second Model

Our second model will handle comments on articles. Here’s the complete file:

// models.js

const path = require('path')

const Sequelize = require('sequelize')

const Boom = require('boom')

Sequelize.Model.find = async function (...args) {

const obj = await this.findById(...args)

if (obj === null) throw Boom.notFound()

return obj

}

const sequelize = new Sequelize(null, null, null, {

dialect: 'sqlite',

storage: path.join('tmp', 'db.sqlite')

})

const Article = sequelize.define('article', {

title: Sequelize.STRING,

body: Sequelize.TEXT

})

![](index-75_1.png)

![](index-75_2.png)

![](index-75_3.png)

![](index-75_4.png)

![](index-75_5.png)

![](index-75_6.png)

![](index-75_7.png)

![](index-75_8.png)

![](index-75_9.png)

![](index-75_10.png)

![](index-75_11.png)

![](index-75_12.png)

![](index-75_13.png)

![](index-75_14.png)

![](index-75_15.png)

![](index-75_16.png)

![](index-75_17.png)

![](index-75_18.png)

![](index-75_19.png)

![](index-75_20.png)

![](index-75_21.png)

![](index-75_22.png)

![](index-75_23.png)

![](index-75_24.png)

![](index-75_25.png)

![](index-75_26.png)

![](index-75_27.png)

![](index-75_28.png)

![](index-75_29.png)

![](index-75_30.png)

![](index-75_31.png)

![](index-75_32.png)

![](index-75_33.png)

![](index-75_34.png)

![](index-75_35.png)

![](index-75_36.png)

![](index-75_37.png)

![](index-75_38.png)

![](index-75_39.png)

![](index-75_40.png)

![](index-75_41.png)

![](index-75_42.png)

![](index-75_43.png)

![](index-75_44.png)

![](index-75_45.png)

![](index-75_46.png)

![](index-75_47.png)

![](index-75_48.png)

![](index-75_49.png)

![](index-75_50.png)

![](index-75_51.png)

![](index-75_52.png)

![](index-75_53.png)

![](index-75_54.png)

![](index-75_55.png)

![](index-75_56.png)

![](index-75_57.png)

![](index-75_58.png)

![](index-75_59.png)

![](index-75_60.png)

![](index-75_61.png)

![](index-75_62.png)

![](index-75_63.png)

![](index-75_64.png)

![](index-75_65.png)

![](index-75_66.png)

![](index-75_67.png)

![](index-75_68.png)

![](index-75_69.png)

![](index-75_70.png)

![](index-75_71.png)

![](index-75_72.png)

![](index-75_73.png)

![](index-75_74.png)

![](index-75_75.png)

![](index-75_76.png)

![](index-75_77.png)

![](index-75_78.png)

![](index-75_79.png)

![](index-75_80.png)

![](index-75_81.png)

![](index-75_82.png)

![](index-75_83.png)

![](index-75_84.png)

![](index-75_85.png)

![](index-75_86.png)

![](index-75_87.png)

![](index-75_88.png)

![](index-75_89.png)

![](index-75_90.png)

![](index-75_91.png)

![](index-75_92.png)

![](index-75_93.png)

![](index-75_94.png)

![](index-75_95.png)

![](index-75_96.png)

![](index-75_97.png)

![](index-75_98.png)

![](index-75_99.png)

![](index-75_100.png)

![](index-75_101.png)

![](index-75_102.png)

![](index-75_103.png)

![](index-75_104.png)

![](index-75_105.png)

![](index-75_106.png)

![](index-75_107.png)

![](index-75_108.png)

![](index-75_109.png)

![](index-75_110.png)

![](index-75_111.png)

![](index-75_112.png)

![](index-75_113.png)

![](index-75_114.png)

![](index-75_115.png)

![](index-75_116.png)

![](index-75_117.png)

![](index-75_118.png)

![](index-75_119.png)

![](index-75_120.png)

![](index-75_121.png)

![](index-75_122.png)

![](index-75_123.png)

![](index-75_124.png)

![](index-75_125.png)

![](index-75_126.png)

![](index-75_127.png)

![](index-75_128.png)

![](index-75_129.png)

![](index-75_130.png)

![](index-75_131.png)

![](index-75_132.png)

![](index-75_133.png)

![](index-75_134.png)

![](index-75_135.png)

![](index-75_136.png)

![](index-75_137.png)

![](index-75_138.png)

![](index-75_139.png)

![](index-75_140.png)

![](index-75_141.png)

![](index-75_142.png)

![](index-75_143.png)

![](index-75_144.png)

![](index-75_145.png)

![](index-75_146.png)

![](index-75_147.png)

![](index-75_148.png)

![](index-75_149.png)

![](index-75_150.png)

![](index-75_151.png)

![](index-75_152.png)

![](index-75_153.png)

![](index-75_154.png)

![](index-75_155.png)

![](index-75_156.png)

![](index-75_157.png)

![](index-75_158.png)

![](index-75_159.png)

![](index-75_160.png)

![](index-75_161.png)

![](index-75_162.png)

![](index-75_163.png)

![](index-75_164.png)

![](index-75_165.png)

![](index-75_166.png)

![](index-75_167.png)

![](index-75_168.png)

![](index-75_169.png)

![](index-75_170.png)

![](index-75_171.png)

![](index-75_172.png)

![](index-75_173.png)

![](index-75_174.png)

const Comment = sequelize.define('comment', {

commenter: Sequelize.STRING,

body: Sequelize.TEXT

})

// These associations add an articleId foreign key to our comments table

// They add helpful methods like article.getComments() and article.createComment() Article.hasMany(Comment)

Comment.belongsTo(Article)

// Create tables

Article.sync()

Comment.sync()

module.exports = {

Article,

Comment

}

For creating and deleting comments we can add nested routes under the article’s path:

// routes.js

const { Article, Comment } = require('./models')

{

method: 'POST',

path: '/articles/{id}/comments',

handler: async (request) =&gt; {

const article = await Article.find(request.params.id) return article.createComment(request.payload.comment)

}

}, {

method: 'DELETE',

path: '/articles/{articleId}/comments/{id}',

handler: async (request) =&gt; {

const { id, articleId } = request.params

// You can pass options to findById as a second argument const comment = await Comment.find(id, { where: { articleId } }) return comment.destroy()

}

}

Lastly, we can extend GET /articles/:id to return both the article *and* its comments:

{

method: 'GET',

![](index-76_1.png)

![](index-76_2.png)

![](index-76_3.png)

![](index-76_4.png)

![](index-76_5.png)

![](index-76_6.png)

![](index-76_7.png)

![](index-76_8.png)

![](index-76_9.png)

![](index-76_10.png)

![](index-76_11.png)

![](index-76_12.png)

![](index-76_13.png)

![](index-76_14.png)

![](index-76_15.png)

![](index-76_16.png)

![](index-76_17.png)

![](index-76_18.png)

![](index-76_19.png)

![](index-76_20.png)

![](index-76_21.png)

![](index-76_22.png)

![](index-76_23.png)

![](index-76_24.png)

![](index-76_25.png)

![](index-76_26.png)

![](index-76_27.png)

![](index-76_28.png)

![](index-76_29.png)

![](index-76_30.png)

![](index-76_31.png)

![](index-76_32.png)

![](index-76_33.png)

![](index-76_34.png)

![](index-76_35.png)

![](index-76_36.png)

![](index-76_37.png)

![](index-76_38.png)

![](index-76_39.png)

![](index-76_40.png)

![](index-76_41.png)

![](index-76_42.png)

![](index-76_43.png)

![](index-76_44.png)

![](index-76_45.png)

![](index-76_46.png)

![](index-76_47.png)

![](index-76_48.png)

![](index-76_49.png)

![](index-76_50.png)

![](index-76_51.png)

![](index-76_52.png)

![](index-76_53.png)

![](index-76_54.png)

![](index-76_55.png)

![](index-76_56.png)

![](index-76_57.png)

![](index-76_58.png)

![](index-76_59.png)

![](index-76_60.png)

![](index-76_61.png)

![](index-76_62.png)

![](index-76_63.png)

![](index-76_64.png)

![](index-76_65.png)

![](index-76_66.png)

![](index-76_67.png)

![](index-76_68.png)

![](index-76_69.png)

![](index-76_70.png)

![](index-76_71.png)

![](index-76_72.png)

![](index-76_73.png)

![](index-76_74.png)

![](index-76_75.png)

![](index-76_76.png)

![](index-76_77.png)

![](index-76_78.png)

![](index-76_79.png)

![](index-76_80.png)

![](index-76_81.png)

![](index-76_82.png)

![](index-76_83.png)

![](index-76_84.png)

![](index-76_85.png)

![](index-76_86.png)

![](index-76_87.png)

![](index-76_88.png)

![](index-76_89.png)

![](index-76_90.png)

![](index-76_91.png)

![](index-76_92.png)

![](index-76_93.png)

![](index-76_94.png)

![](index-76_95.png)

![](index-76_96.png)

![](index-76_97.png)

![](index-76_98.png)

![](index-76_99.png)

![](index-76_100.png)

![](index-76_101.png)

![](index-76_102.png)

![](index-76_103.png)

![](index-76_104.png)

![](index-76_105.png)

![](index-76_106.png)

![](index-76_107.png)

![](index-76_108.png)

![](index-76_109.png)

![](index-76_110.png)

![](index-76_111.png)

![](index-76_112.png)

![](index-76_113.png)

![](index-76_114.png)

![](index-76_115.png)

![](index-76_116.png)

![](index-76_117.png)

![](index-76_118.png)

![](index-76_119.png)

![](index-76_120.png)

![](index-76_121.png)

![](index-76_122.png)

![](index-76_123.png)

![](index-76_124.png)

![](index-76_125.png)

![](index-76_126.png)

![](index-76_127.png)

![](index-76_128.png)

![](index-76_129.png)

![](index-76_130.png)

![](index-76_131.png)

![](index-76_132.png)

![](index-76_133.png)

![](index-76_134.png)

![](index-76_135.png)

![](index-76_136.png)

![](index-76_137.png)

![](index-76_138.png)

![](index-76_139.png)

![](index-76_140.png)

![](index-76_141.png)

![](index-76_142.png)

![](index-76_143.png)

![](index-76_144.png)

![](index-76_145.png)

![](index-76_146.png)

![](index-76_147.png)

![](index-76_148.png)

![](index-76_149.png)

![](index-76_150.png)

![](index-76_151.png)

![](index-76_152.png)

![](index-76_153.png)

![](index-76_154.png)

![](index-76_155.png)

![](index-76_156.png)

![](index-76_157.png)

![](index-76_158.png)

![](index-76_159.png)

![](index-76_160.png)

![](index-76_161.png)

![](index-76_162.png)

![](index-76_163.png)

![](index-76_164.png)

![](index-76_165.png)

![](index-76_166.png)

![](index-76_167.png)

![](index-76_168.png)

![](index-76_169.png)

![](index-76_170.png)

![](index-76_171.png)

![](index-76_172.png)

![](index-76_173.png)

![](index-76_174.png)

path: '/articles/{id}',

handler: async (request) =&gt; {

const article = await Article.find(request.params.id) const comments = await article.getComments()

return { ...article.get(), comments }

}

}

article here is the *Model* object; article.get() returns a plain object with the model’s values, on which we can use the spread operator to combine with our comments. Let’s test it out:

http POST http://localhost:3000/articles/3/comments comment:='{ "commenter": "mb4", "body": "Agreed, this blog rules!" }'

http POST http://localhost:3000/articles/3/comments comment:='{ "commenter": "Nigerian prince", "body": "You are the beneficiary of a Nigerian prince’s $4,000,000 fortune." }'

http GET http://localhost:3000/articles/3

http DELETE http://localhost:3000/articles/3/comments/2

http GET http://localhost:3000/articles/3

Our blog API is almost ready to ship to production, just needing a couple of finishing touches.

Authentication with JWT

JSON Web Tokens are a common authentication mechanism for APIs. There’s a plugin hapiauthjwt2 for setting it up, but it hasn’t yet been updated for Hapi 17.0, so we’ll need to install a fork for now:

npm install save salzhrani/hapiauthjwt2#v17

The code below registers the hapiauthjwt2 plugin and sets up a *strategy* named admin using the jwt *scheme*. If a valid JWT token is sent in a header, query string or cookie, it will call our validate function to verify that we’re happy to grant those credentials access:

// auth.js

const jwtPlugin = require('hapiauthjwt2').plugin

// This would be in an environment variable in production const JWT_KEY = 'NeverShareYourSecret'

var validate = function (credentials) {

// Run any checks here to confirm we want to grant these credentials access

![](index-77_1.png)

![](index-77_2.png)

![](index-77_3.png)

![](index-77_4.png)

![](index-77_5.png)

![](index-77_6.png)

![](index-77_7.png)

![](index-77_8.png)

![](index-77_9.png)

![](index-77_10.png)

![](index-77_11.png)

![](index-77_12.png)

![](index-77_13.png)

![](index-77_14.png)

![](index-77_15.png)

![](index-77_16.png)

![](index-77_17.png)

![](index-77_18.png)

![](index-77_19.png)

![](index-77_20.png)

![](index-77_21.png)

![](index-77_22.png)

![](index-77_23.png)

![](index-77_24.png)

![](index-77_25.png)

![](index-77_26.png)

![](index-77_27.png)

![](index-77_28.png)

![](index-77_29.png)

![](index-77_30.png)

![](index-77_31.png)

![](index-77_32.png)

![](index-77_33.png)

![](index-77_34.png)

![](index-77_35.png)

![](index-77_36.png)

![](index-77_37.png)

![](index-77_38.png)

![](index-77_39.png)

![](index-77_40.png)

![](index-77_41.png)

![](index-77_42.png)

![](index-77_43.png)

![](index-77_44.png)

![](index-77_45.png)

![](index-77_46.png)

![](index-77_47.png)

![](index-77_48.png)

![](index-77_49.png)

![](index-77_50.png)

![](index-77_51.png)

![](index-77_52.png)

![](index-77_53.png)

![](index-77_54.png)

![](index-77_55.png)

![](index-77_56.png)

![](index-77_57.png)

![](index-77_58.png)

![](index-77_59.png)

![](index-77_60.png)

![](index-77_61.png)

![](index-77_62.png)

![](index-77_63.png)

![](index-77_64.png)

![](index-77_65.png)

![](index-77_66.png)

![](index-77_67.png)

![](index-77_68.png)

![](index-77_69.png)

![](index-77_70.png)

![](index-77_71.png)

![](index-77_72.png)

![](index-77_73.png)

![](index-77_74.png)

![](index-77_75.png)

![](index-77_76.png)

![](index-77_77.png)

![](index-77_78.png)

![](index-77_79.png)

![](index-77_80.png)

![](index-77_81.png)

![](index-77_82.png)

![](index-77_83.png)

![](index-77_84.png)

![](index-77_85.png)

![](index-77_86.png)

![](index-77_87.png)

![](index-77_88.png)

![](index-77_89.png)

![](index-77_90.png)

![](index-77_91.png)

![](index-77_92.png)

![](index-77_93.png)

![](index-77_94.png)

![](index-77_95.png)

![](index-77_96.png)

![](index-77_97.png)

![](index-77_98.png)

![](index-77_99.png)

![](index-77_100.png)

![](index-77_101.png)

![](index-77_102.png)

![](index-77_103.png)

![](index-77_104.png)

![](index-77_105.png)

![](index-77_106.png)

![](index-77_107.png)

![](index-77_108.png)

![](index-77_109.png)

![](index-77_110.png)

![](index-77_111.png)

![](index-77_112.png)

![](index-77_113.png)

![](index-77_114.png)

![](index-77_115.png)

![](index-77_116.png)

![](index-77_117.png)

![](index-77_118.png)

![](index-77_119.png)

![](index-77_120.png)

![](index-77_121.png)

![](index-77_122.png)

![](index-77_123.png)

![](index-77_124.png)

![](index-77_125.png)

![](index-77_126.png)

![](index-77_127.png)

![](index-77_128.png)

![](index-77_129.png)

![](index-77_130.png)

![](index-77_131.png)

![](index-77_132.png)

![](index-77_133.png)

![](index-77_134.png)

![](index-77_135.png)

![](index-77_136.png)

![](index-77_137.png)

![](index-77_138.png)

![](index-77_139.png)

![](index-77_140.png)

![](index-77_141.png)

![](index-77_142.png)

![](index-77_143.png)

![](index-77_144.png)

![](index-77_145.png)

![](index-77_146.png)

![](index-77_147.png)

![](index-77_148.png)

![](index-77_149.png)

![](index-77_150.png)

![](index-77_151.png)

![](index-77_152.png)

![](index-77_153.png)

![](index-77_154.png)

![](index-77_155.png)

![](index-77_156.png)

![](index-77_157.png)

![](index-77_158.png)

![](index-77_159.png)

![](index-77_160.png)

![](index-77_161.png)

![](index-77_162.png)

![](index-77_163.png)

![](index-77_164.png)

![](index-77_165.png)

![](index-77_166.png)

![](index-77_167.png)

![](index-77_168.png)

![](index-77_169.png)

![](index-77_170.png)

![](index-77_171.png)

![](index-77_172.png)

![](index-77_173.png)

![](index-77_174.png)

![](index-77_175.png)

![](index-77_176.png)

![](index-77_177.png)

![](index-77_178.png)

![](index-77_179.png)

![](index-77_180.png)

![](index-77_181.png)

![](index-77_182.png)

![](index-77_183.png)

![](index-77_184.png)

![](index-77_185.png)

![](index-77_186.png)

![](index-77_187.png)

![](index-77_188.png)

![](index-77_189.png)

![](index-77_190.png)

![](index-77_191.png)

![](index-77_192.png)

![](index-77_193.png)

![](index-77_194.png)

![](index-77_195.png)

![](index-77_196.png)

![](index-77_197.png)

![](index-77_198.png)

![](index-77_199.png)

![](index-77_200.png)

![](index-77_201.png)

![](index-77_202.png)

![](index-77_203.png)

![](index-77_204.png)

![](index-77_205.png)

![](index-77_206.png)

![](index-77_207.png)

![](index-77_208.png)

![](index-77_209.png)

![](index-77_210.png)

![](index-77_211.png)

![](index-77_212.png)

![](index-77_213.png)

![](index-77_214.png)

![](index-77_215.png)

![](index-77_216.png)

![](index-77_217.png)

![](index-77_218.png)

![](index-77_219.png)

![](index-77_220.png)

![](index-77_221.png)

![](index-77_222.png)

![](index-77_223.png)

![](index-77_224.png)

![](index-77_225.png)

![](index-77_226.png)

![](index-77_227.png)

![](index-77_228.png)

![](index-77_229.png)

![](index-77_230.png)

![](index-77_231.png)

![](index-77_232.png)

![](index-77_233.png)

![](index-77_234.png)

![](index-77_235.png)

![](index-77_236.png)

![](index-77_237.png)

![](index-77_238.png)

![](index-77_239.png)

![](index-77_240.png)

![](index-77_241.png)

![](index-77_242.png)

![](index-77_243.png)

![](index-77_244.png)

![](index-77_245.png)

![](index-77_246.png)

![](index-77_247.png)

![](index-77_248.png)

![](index-77_249.png)

![](index-77_250.png)

![](index-77_251.png)

![](index-77_252.png)

![](index-77_253.png)

![](index-77_254.png)

![](index-77_255.png)

![](index-77_256.png)

![](index-77_257.png)

![](index-77_258.png)

![](index-77_259.png)

![](index-77_260.png)

![](index-77_261.png)

![](index-77_262.png)

![](index-77_263.png)

![](index-77_264.png)

![](index-77_265.png)

![](index-77_266.png)

![](index-77_267.png)

![](index-77_268.png)

![](index-77_269.png)

![](index-77_270.png)

![](index-77_271.png)

![](index-77_272.png)

![](index-77_273.png)

![](index-77_274.png)

![](index-77_275.png)

![](index-77_276.png)

![](index-77_277.png)

![](index-77_278.png)

![](index-77_279.png)

![](index-77_280.png)

![](index-77_281.png)

![](index-77_282.png)

![](index-77_283.png)

![](index-77_284.png)

![](index-77_285.png)

![](index-77_286.png)

![](index-77_287.png)

![](index-77_288.png)

![](index-77_289.png)

![](index-77_290.png)

![](index-77_291.png)

![](index-77_292.png)

![](index-77_293.png)

![](index-77_294.png)

![](index-77_295.png)

![](index-77_296.png)

![](index-77_297.png)

![](index-77_298.png)

![](index-77_299.png)

![](index-77_300.png)

![](index-77_301.png)

![](index-77_302.png)

![](index-77_303.png)

![](index-77_304.png)

![](index-77_305.png)

![](index-77_306.png)

![](index-77_307.png)

![](index-77_308.png)

![](index-77_309.png)

![](index-77_310.png)

![](index-77_311.png)

![](index-77_312.png)

![](index-77_313.png)

![](index-77_314.png)

![](index-77_315.png)

![](index-77_316.png)

![](index-77_317.png)

![](index-77_318.png)

![](index-77_319.png)

![](index-77_320.png)

![](index-77_321.png)

![](index-77_322.png)

![](index-77_323.png)

![](index-77_324.png)

![](index-77_325.png)

![](index-77_326.png)

![](index-77_327.png)

![](index-77_328.png)

![](index-77_329.png)

![](index-77_330.png)

![](index-77_331.png)

![](index-77_332.png)

![](index-77_333.png)

![](index-77_334.png)

![](index-77_335.png)

![](index-77_336.png)

![](index-77_337.png)

![](index-77_338.png)

![](index-77_339.png)

![](index-77_340.png)

![](index-77_341.png)

![](index-77_342.png)

return {

isValid: true,

credentials // request.auth.credentials

}

}

exports.configureAuth = async (server) =&gt; {

await server.register(jwtPlugin)

server.auth.strategy('admin', 'jwt', {

key: JWT_KEY,

validate,

verifyOptions: { algorithms: [ 'HS256' ] }

})

// Default all routes to require JWT and opt out for public routes server.auth.default('admin')

}

Next, import and configure our auth strategy before starting the server:

// server.js

const { configureAuth } = require('./auth')

const main = async () =&gt; {

await configureAuth(server)

await configureRoutes(server)

await server.start()

return server

}

Now all routes will require our admin auth strategy. Try these three: http GET localhost:3000/articles

http GET localhost:3000/articles Authorization:yep http GET localhost:3000/articles Authorization:eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6MSwibmFtZSI6IkFudGhvbnkgVmFsaWQgVXNlciIsImlhdCI6MTQyNTQ3MzUzNX0.KA68l60mjiC8EXaC2odnjFwdIDxE__iDu5RwLdN1F2A The last one should contain a valid token and return the articles from the database. To make a route public, we just need to add config: { auth: false } to the route object. For example:

{

method: 'GET',

path: '/articles',

handler: (request) =&gt; {

![](index-78_1.png)

![](index-78_2.png)

![](index-78_3.png)

![](index-78_4.png)

![](index-78_5.png)

![](index-78_6.png)

![](index-78_7.png)

![](index-78_8.png)

![](index-78_9.png)

![](index-78_10.png)

![](index-78_11.png)

![](index-78_12.png)

![](index-78_13.png)

![](index-78_14.png)

![](index-78_15.png)

![](index-78_16.png)

![](index-78_17.png)

![](index-78_18.png)

![](index-78_19.png)

![](index-78_20.png)

![](index-78_21.png)

![](index-78_22.png)

![](index-78_23.png)

![](index-78_24.png)

![](index-78_25.png)

![](index-78_26.png)

![](index-78_27.png)

![](index-78_28.png)

![](index-78_29.png)

![](index-78_30.png)

![](index-78_31.png)

![](index-78_32.png)

![](index-78_33.png)

![](index-78_34.png)

![](index-78_35.png)

![](index-78_36.png)

![](index-78_37.png)

![](index-78_38.png)

![](index-78_39.png)

![](index-78_40.png)

![](index-78_41.png)

![](index-78_42.png)

![](index-78_43.png)

![](index-78_44.png)

![](index-78_45.png)

![](index-78_46.png)

![](index-78_47.png)

![](index-78_48.png)

![](index-78_49.png)

![](index-78_50.png)

![](index-78_51.png)

![](index-78_52.png)

![](index-78_53.png)

![](index-78_54.png)

![](index-78_55.png)

![](index-78_56.png)

![](index-78_57.png)

![](index-78_58.png)

![](index-78_59.png)

![](index-78_60.png)

![](index-78_61.png)

![](index-78_62.png)

![](index-78_63.png)

![](index-78_64.png)

![](index-78_65.png)

![](index-78_66.png)

![](index-78_67.png)

![](index-78_68.png)

![](index-78_69.png)

![](index-78_70.png)

![](index-78_71.png)

![](index-78_72.png)

![](index-78_73.png)

![](index-78_74.png)

![](index-78_75.png)

![](index-78_76.png)

![](index-78_77.png)

![](index-78_78.png)

![](index-78_79.png)

![](index-78_80.png)

![](index-78_81.png)

![](index-78_82.png)

![](index-78_83.png)

![](index-78_84.png)

![](index-78_85.png)

![](index-78_86.png)

![](index-78_87.png)

![](index-78_88.png)

![](index-78_89.png)

![](index-78_90.png)

![](index-78_91.png)

![](index-78_92.png)

![](index-78_93.png)

![](index-78_94.png)

![](index-78_95.png)

![](index-78_96.png)

![](index-78_97.png)

![](index-78_98.png)

![](index-78_99.png)

![](index-78_100.png)

![](index-78_101.png)

![](index-78_102.png)

![](index-78_103.png)

![](index-78_104.png)

![](index-78_105.png)

![](index-78_106.png)

![](index-78_107.png)

![](index-78_108.png)

![](index-78_109.png)

![](index-78_110.png)

![](index-78_111.png)

![](index-78_112.png)

![](index-78_113.png)

![](index-78_114.png)

![](index-78_115.png)

![](index-78_116.png)

![](index-78_117.png)

![](index-78_118.png)

![](index-78_119.png)

![](index-78_120.png)

![](index-78_121.png)

![](index-78_122.png)

![](index-78_123.png)

![](index-78_124.png)

![](index-78_125.png)

![](index-78_126.png)

![](index-78_127.png)

![](index-78_128.png)

![](index-78_129.png)

![](index-78_130.png)

![](index-78_131.png)

![](index-78_132.png)

![](index-78_133.png)

![](index-78_134.png)

![](index-78_135.png)

![](index-78_136.png)

![](index-78_137.png)

![](index-78_138.png)

![](index-78_139.png)

![](index-78_140.png)

![](index-78_141.png)

![](index-78_142.png)

![](index-78_143.png)

![](index-78_144.png)

![](index-78_145.png)

![](index-78_146.png)

![](index-78_147.png)

![](index-78_148.png)

![](index-78_149.png)

![](index-78_150.png)

![](index-78_151.png)

![](index-78_152.png)

![](index-78_153.png)

![](index-78_154.png)

![](index-78_155.png)

![](index-78_156.png)

![](index-78_157.png)

![](index-78_158.png)

![](index-78_159.png)

![](index-78_160.png)

![](index-78_161.png)

![](index-78_162.png)

![](index-78_163.png)

![](index-78_164.png)

![](index-78_165.png)

![](index-78_166.png)

![](index-78_167.png)

![](index-78_168.png)

![](index-78_169.png)

![](index-78_170.png)

![](index-78_171.png)

![](index-78_172.png)

![](index-78_173.png)

![](index-78_174.png)

![](index-78_175.png)

![](index-78_176.png)

![](index-78_177.png)

![](index-78_178.png)

![](index-78_179.png)

![](index-78_180.png)

return Article.findAll()

},

config: { auth: false }

}

Make these three routes public so that anyone can read articles and post comments: GET /articles articles#index

GET /articles/:id articles#show

POST /articles/:id/comments comments#create

Generating a JWT

There’s a package named jsonwebtoken for signing and verifying JWT: npm install save jsonwebtoken

Our final route will take an email / password and generate a JWT. Let’s define our login function in auth.js to keep all auth logic in a single place:

// auth.js

const jwt = require('jsonwebtoken')

const Boom = require('boom')

exports.login = (email, password) =&gt; {

if (!(email === 'mb4@gmail.com' &amp;&amp; password === 'bears')) return Boom.notAcceptable() const credentials = { email }

const token = jwt.sign(credentials, JWT_KEY, { algorithm: 'HS256', expiresIn: '1h' }) return { token }

}

// routes.js

const { login } = require('./auth')

{

method: 'POST',

path: '/authentications',

handler: async (request) =&gt; {

const { email, password } = request.payload.login return login(email, password)

},

![](index-79_1.png)

![](index-79_2.png)

![](index-79_3.png)

![](index-79_4.png)

![](index-79_5.png)

![](index-79_6.png)

![](index-79_7.png)

![](index-79_8.png)

![](index-79_9.png)

![](index-79_10.png)

![](index-79_11.png)

![](index-79_12.png)

![](index-79_13.png)

![](index-79_14.png)

![](index-79_15.png)

![](index-79_16.png)

![](index-79_17.png)

![](index-79_18.png)

![](index-79_19.png)

![](index-79_20.png)

![](index-79_21.png)

![](index-79_22.png)

![](index-79_23.png)

![](index-79_24.png)

![](index-79_25.png)

![](index-79_26.png)

![](index-79_27.png)

![](index-79_28.png)

![](index-79_29.png)

![](index-79_30.png)

![](index-79_31.png)

![](index-79_32.png)

![](index-79_33.png)

![](index-79_34.png)

![](index-79_35.png)

![](index-79_36.png)

![](index-79_37.png)

![](index-79_38.png)

![](index-79_39.png)

![](index-79_40.png)

![](index-79_41.png)

![](index-79_42.png)

![](index-79_43.png)

![](index-79_44.png)

![](index-79_45.png)

![](index-79_46.png)

![](index-79_47.png)

![](index-79_48.png)

![](index-79_49.png)

![](index-79_50.png)

![](index-79_51.png)

![](index-79_52.png)

![](index-79_53.png)

![](index-79_54.png)

![](index-79_55.png)

![](index-79_56.png)

![](index-79_57.png)

![](index-79_58.png)

![](index-79_59.png)

![](index-79_60.png)

![](index-79_61.png)

![](index-79_62.png)

![](index-79_63.png)

![](index-79_64.png)

![](index-79_65.png)

![](index-79_66.png)

![](index-79_67.png)

![](index-79_68.png)

![](index-79_69.png)

![](index-79_70.png)

![](index-79_71.png)

![](index-79_72.png)

![](index-79_73.png)

![](index-79_74.png)

![](index-79_75.png)

![](index-79_76.png)

![](index-79_77.png)

![](index-79_78.png)

![](index-79_79.png)

![](index-79_80.png)

![](index-79_81.png)

![](index-79_82.png)

![](index-79_83.png)

![](index-79_84.png)

![](index-79_85.png)

![](index-79_86.png)

![](index-79_87.png)

![](index-79_88.png)

![](index-79_89.png)

![](index-79_90.png)

![](index-79_91.png)

![](index-79_92.png)

![](index-79_93.png)

![](index-79_94.png)

![](index-79_95.png)

![](index-79_96.png)

![](index-79_97.png)

![](index-79_98.png)

![](index-79_99.png)

![](index-79_100.png)

![](index-79_101.png)

![](index-79_102.png)

![](index-79_103.png)

![](index-79_104.png)

![](index-79_105.png)

![](index-79_106.png)

![](index-79_107.png)

![](index-79_108.png)

![](index-79_109.png)

![](index-79_110.png)

![](index-79_111.png)

![](index-79_112.png)

![](index-79_113.png)

![](index-79_114.png)

![](index-79_115.png)

![](index-79_116.png)

![](index-79_117.png)

![](index-79_118.png)

![](index-79_119.png)

![](index-79_120.png)

![](index-79_121.png)

![](index-79_122.png)

![](index-79_123.png)

![](index-79_124.png)

![](index-79_125.png)

![](index-79_126.png)

![](index-79_127.png)

![](index-79_128.png)

![](index-79_129.png)

![](index-79_130.png)

![](index-79_131.png)

![](index-79_132.png)

![](index-79_133.png)

![](index-79_134.png)

![](index-79_135.png)

![](index-79_136.png)

![](index-79_137.png)

![](index-79_138.png)

![](index-79_139.png)

![](index-79_140.png)

![](index-79_141.png)

![](index-79_142.png)

![](index-79_143.png)

![](index-79_144.png)

![](index-79_145.png)

![](index-79_146.png)

![](index-79_147.png)

![](index-79_148.png)

![](index-79_149.png)

![](index-79_150.png)

![](index-79_151.png)

![](index-79_152.png)

![](index-79_153.png)

![](index-79_154.png)

![](index-79_155.png)

![](index-79_156.png)

![](index-79_157.png)

![](index-79_158.png)

![](index-79_159.png)

![](index-79_160.png)

![](index-79_161.png)

![](index-79_162.png)

![](index-79_163.png)

![](index-79_164.png)

![](index-79_165.png)

![](index-79_166.png)

![](index-79_167.png)

![](index-79_168.png)

![](index-79_169.png)

![](index-79_170.png)

![](index-79_171.png)

![](index-79_172.png)

![](index-79_173.png)

![](index-79_174.png)

config: { auth: false }

}

http POST localhost:3000/authentications login:='{"email": "mb4@gmail.com", "password": "bears"}'

Try using the returned token in your requests to the secure routes!

Validation with joi

You can validate request params by adding config to the route object. The code below ensures that the submitted article has a body and title between three and ten characters in length. If a validation fails, Hapi will respond with a 400 error: const Joi = require('joi')

{

method: 'POST',

path: '/articles',

handler: (request) =&gt; {

const article = Article.build(request.payload.article) return article.save()

},

config: {

validate: {

payload: {

article: {

title: Joi.string().min(3).max(10),

body: Joi.string().required()

}

}

}

}

}

}

In addition to payload, you can also add validations to path, query and headers.

Learn more about validation in the docs.

Who Is Consuming this API?

We could serve a singlepage app from /. We’ve already seen — at the start of the tutorial — one example of how to serve an HTML file with streams. There are much

better ways of working with Views and Layouts in Hapi, though. See Serving Static Content and Views and Layouts for more on how to render dynamic views:

{

method: 'GET',

path: '/',

handler: () =&gt; {

return require('fs').createReadStream('index.html')

},

config: { auth: false }

}

If the front end and API are on the same domain, you’ll have no problems making requests: client > hapiapi.

If you’re serving the front end from a *different* domain and want to make requests to the API directly from the client, you’ll need to enable CORS. This is super easy in Hapi: const server = Hapi.server({

host: 'localhost',

port: 3000,

routes: {

cors: {

credentials: true

// See options at https://hapijs.com/api/17.0.0#routeoptionscors

}

}

})

You could also create a *new* application in between the two. If you go down this route, you won’t need to bother with CORS, as the client will only be making requests to the frontend app, and it can then make requests to the API on the server without any crossdomain restrictions: client > hapifrontend > hapiapi.

Whether that front end is another Hapi application, or Next, or Nuxt … I’ll leave that for you to decide!

**https://avxhm.se/blogs/hill0**

HisC

tor h

y apter 7: Create New Express.js Apps in

To M

pics inutes with Express Generator

Tu B

torYia lP

s AUL SAUVE

Express.js is a Node.js web framework that has gained immense popularity Offers & Deals

due to its simplicity. It has easytouse routing and simple support for view engines, putting it far ahead of the basic Node HTTP server.

Highlights

However, starting a new Express application requires a certain amount of boilerplate Settings

code: starting a new server instance, configuring a view engine, setting up error handling.

Support

Although there are various starter projects and boilerplates available, Express has its Sign Out

own commandline tool that makes it easy to start new apps, called the expressgenerator.

What is Express?

Express has a lot of features built in, and a lot more features you can get from other packages that integrate seamlessly, but there are three main things it does for you out of the box:

1\. Routing. This is how */home* */blog* and */about* all give you different pages. Express makes it easy for you to modularize this code by allowing you to put different routes in different files.

2\. Middleware. If you’re new to the term, basically middleware is “software glue”. It accesses requests before your routes get them, allowing them to handle hardtodo stuff like cookie parsing, file uploads, errors, and more.

3\. Views. Views are how HTML pages are rendered with custom content. You pass in the data you want to be rendered and Express will render it with your given view engine.

Getting Started

Getting Started

Starting a new project with the Express generator is as simple as running a few commands:

npm install expressgenerator g

This installs the Express generator as a global package, allowing you to run the express command in your terminal:

express myapp

This creates a new Express project called myapp which is then placed inside of the myapp directory.

cd myapp

If you’re unfamiliar with terminal commands, this one puts you inside of the myapp directory.

npm install

npm is the default Node.js package manager. Running npm install installs all dependencies for the project. By default, the expressgenerator includes several packages that are commonly used with an Express server.

OPTIONS

The generator CLI takes half a dozen arguments, but the two most useful ones are the following:

v ejs|hbs|hjs|jade|pug|twig|vash. This lets you select a view engine to install.

The default is jade. Although this still works, it has been deprecated in favor of pug.

c less|stylus|compass|sass. By default, the generator creates a very basic CSS

file for you, but selecting a CSS engine will configure your new app with middleware to compile any of the above options.

Now that we’ve got our project set up and dependencies installed, we can start the new server by running the following:

npm start

Then browse to http://localhost:3000 in your browser.

Application Structure

The generated Express application starts off with four folders.

BIN

The bin folder contains the executable file that starts your app. It starts the server (on port 3000, if no alternative is supplied) and sets up some basic error handling. You don’t really need to worry about this file because npm start will run it for you.

PUBLIC

The public folder is one of the important ones:

*everything*

in this folder is accessible

to people connecting to your application. In this folder, you’ll put JavaScript, CSS, images, and other assets that people need when they connect to your website.

ROUTES

The routes folder is where you'll put your router files. The generator creates two files, index.js and users.js, which serve as examples of how to separate out your application's route configuration.

Usually, here you’ll have a different file for each major route on your website. So you might have files called blog.js, home.js, and/or about.js in this folder.

VIEWS

The views folder is where you have the files used by your templating engine. The generator will configure Express to look in here for a matching view when you call the render method.

Outside of these folders, there’s one file that you should know well.

app.js

The app.js file is special because it sets up your Express application and glues all of the different parts together. Let’s walk through what it does. Here’s how the file starts: var express = require('express');

var path = require('path');

var favicon = require('servefavicon');

var logger = require('morgan');

var cookieParser = require('cookieparser');

var bodyParser = require('bodyparser');

These first six lines of the file are requires. If you’re new to Node, be sure to read Understanding module.exports and exports in Node.js.

var routes = require('./routes/index');

var users = require('./routes/users');

The next two lines of code are requiring the different route files that the Express generator sets up by default: routes and users.

var app = express();

After that, we create a new app by calling express(). The app variable contains all of the settings and routes for your application. This object glues together your application.

app.set('views', path.join(__dirname, 'views'));

app.set('view engine', 'jade');

Once the app instance is created, the templating engine is set up for rendering views.

This is where you’d change the path to your view files if you wanted.

After this, you’ll see Express being configured to use middleware. The generator installs several common pieces of middleware that you're likely to use in a web application.

//app.use(favicon(path.join(__dirname, 'public', 'favicon.ico')));

app.use(logger('dev'));

app.use(bodyParser.json());

app.use(bodyParser.urlencoded({ extended: false }));

app.use(cookieParser());

app.use(express.static(path.join(__dirname, 'public')));

favicon. This one is pretty selfexplanatory: it just serves your favicon.ico out

of your public directory.

logger. When you run your app, you might notice that all the routes that are requested are logged to console. If you want to disable this, you can just comment out this middleware.

bodyParser. You might notice that there are two lines for parsing the body of incoming HTTP requests. The first line handles when JSON is sent via POST

request and it puts this data in request.body. The second line parses query string data in the URL (e.g. /profile?id=5) and puts this in request.query.

cookieParser. This takes all the cookies the client sends and puts them in request.cookies. It also allows you to modify them before sending them back to the client, by changing response.cookies.

express.static. This middleware serves static assets from your public folder. If you wanted to rename or move the public folder, you can change the path here.

Next up is the routing:

app.use('/', routes);

app.use('/users', users);

Here the example route files that were required are attached to our app. If you need to add additional routes, you’d do it here.

All the code after this is used for error handling. You usually won’t have to modify this code unless you want to change the way Express handles errors. By default, it’s set up to show the error that occurred in the route when you’re in development mode.

A Useful Tool

Hopefully you now have a clear idea of how the expressgenerator tool can save you time writing repetitive boilerplate when starting new Expressbased projects.

By providing a sensible default file structure, and installing and wiring up commonly needed middleware, the generator creates a solid foundation for new applications with just a couple of commands.

HisC

tor h

y apter 8: An Introduction to MongoDB

Topics

BY MANJUNATH M

Tu M

torio

aln

s goDB is an opensource, documentoriented, NoSQL database program. If you’ve been involved with the traditional, relational databases Off feo

rs r

& lo

De n

al g

s , the idea of a documentoriented, NoSQL database might indeed sound peculiar. “How can a database not have tables?”, you might wonder.

Hi T

ghlhigihst stutorial introduces you to some of the basic concepts of MongoDB and should help you get started even if you have very limited experience with a Setdtiantgsabase management system.

Support

What’s MongoDB?

Sign Out

Here’s what the official documentation has to say about MongoDB.

MongoDB is an opensource database developed by MongoDB Inc. that’s scalable and flexible. MongoDB stores data in JSONlike documents that can vary in structure.

Obviously, MongoDB is a database system. But why do we need another database option when the existing solutions are inexpensive and successful? A relational database system like MySQL or Oracle has tables, and each table has a number of rows and columns. MongoDB, being a documentoriented database system, doesn’t have them. Instead, it has a JSONlike document structure that is flexible and easy to work with. Here’s an example of what a MongoDB document looks like:

{

"_id": ObjectId(3da252d3902a),

"type": "Article",

"title": "MongoDB Tutorial Part One",

"description": "First document",

"author": "Manjunath",

"content": "This is an..."

}

{

"_id": ObjectId(8da21ea3902a),

"type": "Article",

"title": "MongoDB Tutorial Part Two",

"description": "Second document",

"author": "Manjunath",

"content": "In the second..."

}

A document in a NoSQL database corresponds to a row in an SQL database. A group of documents together is known as a collection, which is roughly synonymous with a table in a relational database. For an indepth overview of both NoSQL and SQL

databases and their differences, we have that covered in the SQL vs NoSQL tutorial.

Apart from being a NoSQL database, MongoDB has a few qualities of its own. I’ve listed some of its key features below:

it’s easy to install and set up

it uses a BSON (a JSONlike format) to store data it’s easy to map the document objects to your application code it claims to be highly scalable and available, and includes support for outofthebox replication

it supports MapReduce operations for condensing a large volume of data into useful aggregated results

it’s free and open source.

MongoDB appears to overcome the limitations of the ageold relational databases and NoSQL databases. If you aren’t yet convinced about why it’s useful, check out our article on Choosing Between NoSQL and SQL.

Let’s go ahead and install MongoDB.

Installing MongoDB

Installing MongoDB is easy and it doesn’t require much configuration or setup.

MongoDB is supported by all major platforms and distributions, and you can check out their documentation if you’re in doubt.

I’ve covered the instructions for installing MongoDB on macOS below. For Linux, MongoDB recommends installing the software with the help of your distribution’s

package manager. If you’re on Windows, it’s as easy as downloading the latest release from from the MongoDB website and running the interactive installer.

Installing MongoDB on macOS using Homebrew

Homebrew is a package manager for macOS, and this tutorial assumes you’ve already installed Homebrew on your machine.

1\. Open the terminal application and run

$ brew update

1\. Once brew is updated, install the mongodb package as follows $ brew install mongodb

1\. Create a data directory so that the mongod process will be able to write data. By default, the directory is /data/db:

$ mkdir p /data/db

2\. Make sure your user account has permission to read and write data into that directory:

$ sudo chown R ìd un` /data/db

&gt; # Enter your password

3\. Initiate the mongo server. Run the mongod command to start the server.

4\. Start the Mongo shell. Open up another terminal window and run mongo. The mongo shell will attempt to connect to the mongo daemon that we initiated earlier.

Once you’re successfully connected, you can use the shell as a playground to safely run all your commands.

5\. Exit the Mongo shell by running quit() and the mongo daemon by pressing control + C.

Now that we have the mongo daemon up and running, let’s get acquainted with the MongoDB basics.

Basic Database Operations

Enter the Mongo shell if you haven’t already:

[mj@localhost ~]$ mongo

MongoDB shell version v3.6.1

connecting to: mongodb://127.0.0.1:27017

MongoDB server version: 3.6.1

connecting to: test

You can see my version of MongoDB shell when you log in. By default, you’re connected to a test database. You can verify the name of the current database by running db:

&gt; db

test

That’s awesome, but what if we want a new database? To create a database, MongoDB

has a use DATABASE_NAME command:

&gt;use exampledb

switched to db exampledb

To display all the existing databases, try show dbs:

&gt; show dbs

local 0.078GB

prototype 0.078GB

test 0.078GB

The exampledb isn’t in the list because we need to insert at least one document into the database. To insert a document, you can do

db.COLLECTION_NAME.insertOne({"key":"value"}). Here’s an example:

&gt; db.users.insertOne({'name':'Bob'})

{

"acknowledged" : true,

"insertedId" : ObjectId("5a52c53b223039ee9c2daaec")

}

MongoDB automatically creates a new users collection and inserts a document with the keyvalue pair 'name':'Bob'. The ObjectId returned is the id of document inserted. MongoDB creates a unique ObjectId for each document on creation and it becomes the default value of the _id field:

&gt;show dbs

exampledb 0.078GB

local 0.078GB

prototype 0.078GB

test 0.078GB

Similarly, you can confirm that the collection was created using the show collections command:

&gt; show collections

users

We’ve created a database, added a collection named users and inserted a document into it. Now let’s try dropping it. To drop an existing database, use the dropDatabase() command as exemplified below:

&gt;db.dropDatabase()

{ "ok" : 1 }

show dbs confirms that the database was indeed dropped.

> show dbs

local 0.078GB

prototype 0.078GB

test 0.078GB

For more database operations, see MongoDB reference page on Database Commands.

MongoDB CRUD Operations

As you might already know, the CRUD acronym stands for Create, Read, Update, and Delete. These are the four basic database operations that you can’t avoid while building

an application. For instance, any modern application will have the ability to create a new user, read the user data, update the user information and, if needed, delete the user account. Let’s accomplish this at the database level using MongoDB.

CREATE OPERATION

Creation is the same as inserting a document into a collection. In the previous section, we had inserted a single document using the db.collection.insertOne() syntax.

There’s another method called db.collection.insertMany() that lets you insert multiple documents at once. Here’s the syntax:

&gt; db.COLLECTION_NAME.insertMany(

[ &lt;document 1&gt; , &lt;document 2&gt;, ... ]

)

Let’s create a users collection and populate it with some actual users:

&gt; db.users.insertMany([

{ "name": "Tom","age":33, "email": "tom@example.com" },

{ "name":"Bob", "age":35, "email":"bob@example.com" },

{ "name": "Kate", "age": 27, "email": "kate@example.com" },

{ "name": "Watson", "age":15, "email":"watson@example.com"}

])

{

"acknowledged" : true,

"insertedIds" : [

ObjectId("5a52cb2451dd8b08d5a22cf5"),

ObjectId("5a52cb2451dd8b08d5a22cf6"),

ObjectId("5a52cb2451dd8b08d5a22cf7"),

ObjectId("5a52cb2451dd8b08d5a22cf8")

]

}

The insertMany method accepts an array of objects and, in return, we get an array of ObjectIds.

READ OPERATION

Read operation is used to retrieve a document or multiple documents from a collection.

The syntax for the read operation is as follows:

&gt; db.collection.find(query, projection)

![](index-92_1.png)

![](index-92_2.png)

![](index-92_3.png)

![](index-92_4.png)

![](index-92_5.png)

![](index-92_6.png)

![](index-92_7.png)

![](index-92_8.png)

![](index-92_9.png)

![](index-92_10.png)

![](index-92_11.png)

![](index-92_12.png)

![](index-92_13.png)

![](index-92_14.png)

![](index-92_15.png)

![](index-92_16.png)

![](index-92_17.png)

![](index-92_18.png)

![](index-92_19.png)

![](index-92_20.png)

![](index-92_21.png)

![](index-92_22.png)

![](index-92_23.png)

![](index-92_24.png)

![](index-92_25.png)

![](index-92_26.png)

![](index-92_27.png)

![](index-92_28.png)

![](index-92_29.png)

![](index-92_30.png)

![](index-92_31.png)

![](index-92_32.png)

![](index-92_33.png)

![](index-92_34.png)

![](index-92_35.png)

![](index-92_36.png)

![](index-92_37.png)

![](index-92_38.png)

![](index-92_39.png)

![](index-92_40.png)

![](index-92_41.png)

![](index-92_42.png)

![](index-92_43.png)

![](index-92_44.png)

![](index-92_45.png)

![](index-92_46.png)

![](index-92_47.png)

![](index-92_48.png)

![](index-92_49.png)

![](index-92_50.png)

![](index-92_51.png)

![](index-92_52.png)

![](index-92_53.png)

![](index-92_54.png)

![](index-92_55.png)

![](index-92_56.png)

![](index-92_57.png)

![](index-92_58.png)

![](index-92_59.png)

![](index-92_60.png)

![](index-92_61.png)

![](index-92_62.png)

![](index-92_63.png)

![](index-92_64.png)

![](index-92_65.png)

![](index-92_66.png)

![](index-92_67.png)

![](index-92_68.png)

![](index-92_69.png)

![](index-92_70.png)

![](index-92_71.png)

![](index-92_72.png)

![](index-92_73.png)

![](index-92_74.png)

![](index-92_75.png)

![](index-92_76.png)

![](index-92_77.png)

![](index-92_78.png)

![](index-92_79.png)

![](index-92_80.png)

![](index-92_81.png)

![](index-92_82.png)

![](index-92_83.png)

![](index-92_84.png)

![](index-92_85.png)

![](index-92_86.png)

![](index-92_87.png)

![](index-92_88.png)

![](index-92_89.png)

![](index-92_90.png)

![](index-92_91.png)

![](index-92_92.png)

![](index-92_93.png)

![](index-92_94.png)

![](index-92_95.png)

![](index-92_96.png)

![](index-92_97.png)

![](index-92_98.png)

![](index-92_99.png)

![](index-92_100.png)

![](index-92_101.png)

![](index-92_102.png)

![](index-92_103.png)

![](index-92_104.png)

![](index-92_105.png)

![](index-92_106.png)

![](index-92_107.png)

![](index-92_108.png)

![](index-92_109.png)

![](index-92_110.png)

![](index-92_111.png)

![](index-92_112.png)

![](index-92_113.png)

![](index-92_114.png)

![](index-92_115.png)

![](index-92_116.png)

![](index-92_117.png)

![](index-92_118.png)

![](index-92_119.png)

![](index-92_120.png)

![](index-92_121.png)

![](index-92_122.png)

![](index-92_123.png)

![](index-92_124.png)

![](index-92_125.png)

![](index-92_126.png)

![](index-92_127.png)

![](index-92_128.png)

![](index-92_129.png)

![](index-92_130.png)

![](index-92_131.png)

![](index-92_132.png)

![](index-92_133.png)

![](index-92_134.png)

![](index-92_135.png)

![](index-92_136.png)

![](index-92_137.png)

![](index-92_138.png)

![](index-92_139.png)

![](index-92_140.png)

![](index-92_141.png)

![](index-92_142.png)

![](index-92_143.png)

![](index-92_144.png)

![](index-92_145.png)

![](index-92_146.png)

![](index-92_147.png)

![](index-92_148.png)

![](index-92_149.png)

![](index-92_150.png)

![](index-92_151.png)

![](index-92_152.png)

![](index-92_153.png)

![](index-92_154.png)

![](index-92_155.png)

![](index-92_156.png)

![](index-92_157.png)

![](index-92_158.png)

![](index-92_159.png)

![](index-92_160.png)

![](index-92_161.png)

![](index-92_162.png)

![](index-92_163.png)

![](index-92_164.png)

![](index-92_165.png)

![](index-92_166.png)

![](index-92_167.png)

![](index-92_168.png)

![](index-92_169.png)

![](index-92_170.png)

![](index-92_171.png)

![](index-92_172.png)

![](index-92_173.png)

![](index-92_174.png)

To retrieve all user documents, you can do this:

&gt; db.users.find().pretty()

{

"_id" : ObjectId("5a52cb2451dd8b08d5a22cf5"),

"name" : "Tom",

"age" : 33,

"email" : "tom@example.com"

}

{

"_id" : ObjectId("5a52cb2451dd8b08d5a22cf6"),

"name" : "Bob",

"age" : 35,

"email" : "bob@example.com"

}

{

"_id" : ObjectId("5a52cb2451dd8b08d5a22cf7"),

"name" : "Kate",

"age" : 27,

"email" : "kate@example.com"

}

{

"_id" : ObjectId("5a52cb2451dd8b08d5a22cf8"),

"name" : "Watson",

"age" : 15,

"email" : "watson@example.com"

}

This corresponds to the SELECT * FROM USERS query from an SQL database.

The pretty method is a cursor method, and there are many others too. You can chain these methods to modify your query and the documents that are returned by the query.

What if you need to filter queries and return a subset of the collection? Say, find all users who are below 30\. You can modify the query like this:

&gt; db.users.find({ "age": { $lt: 30 } })

{ "_id" : ObjectId("5a52cb2451dd8b08d5a22cf7"), "name" : "Kate", "age" : 27, "email" : "kate@example.com" }

{ "_id" : ObjectId("5a52cb2451dd8b08d5a22cf8"), "name" : "Watson", "age" : 15, "email" : "watson@example.com" }

$lt is a query filter operator that selects documents whose age field value is less than 30\. There are many comparison and logical query filters available, and you see the entire list in the Query Selector documentation.

UPDATE OPERATION

The update operation modifies the document in a collection. Similar to the create operation, MongoDB offers two methods for updating a document. They are: 1. db.collection.updateMany(filter, update, options) 2. db.collection.updateMany(filter, update, options).

If you need to add an extra field, say registration, to all the existing documents in a collection, you can do something like this:

&gt; db.users.updateMany({}, {$set: { 'registration': 'incomplete'}})

{ "acknowledged" : true, "matchedCount" : 4, "modifiedCount" : 4 }

The first argument is an empty object because we want to update all documents in the collection. The $set is an update operator that sets the value of a field with the specified value. You can verify that the extra field was added using db.users.find().

To update the value of documents that match certain criteria, updateMany() accepts a filter object as the first argument. For instance, you might want to overwrite the value of registration to complete for all users who are aged 18+. Here is what you can do:

&gt; db.users.updateMany(

{'age':{ $gt: 18} },

{$set: { 'registration': 'complete'}

})

{ "acknowledged" : true, "matchedCount" : 3, "modifiedCount" : 3 }

To update the registration details of a single user, you can do this:

&gt; db.users.updateOne(

{'email': 'watson@example.com' },

{$set: { 'registration': 'complete'}

})

{ "acknowledged" : true, "matchedCount" : 1, "modifiedCount" : 1 }

DELETE OPERATION

Delete operation removes a document from the collection. To delete a document, you can use the db.collection.deleteOne(filter, options) method, and to

delete multiple documents, you can use the db.collection.deleteMany(filter, options) method.

To delete documents based on certain criteria, you can use the filter operators that we used for the read and update operation:

db.users.deleteMany( { status: { $in: [ "dormant", "inactive" ] } } )

{ "acknowledged" : true, "deletedCount" : 1 }

This deletes all documents with a status of “dormant” or “inactive”.

That’s it.

An Overview of MongoDB Drivers

For an application to communicate with the mongodbserver, you have to use a clientside library called a driver. The driver sits on top of the database server and lets you interact with the database using the driver API. MongoDB has official and thirdparty drivers for all popular languages and environments.

In this tutorial, we’re going to look at our options for drivers for Node.js. Some drivers add lots of good features, like like schema support and validation of business logic, and you can choose the one that matches your style. The popular drivers for Node.js include the native MongoDB driver and Mongoose. I’ll briefly discuss their features here.

MONGODB NODE.JS DRIVER

This is the official MongoDB driver for Node.js. The driver can interact with the database using either promises or callbacks, and also supports the ES6 async/await functions. The example below demonstrates connecting the driver to the server: const MongoClient = require('mongodb').MongoClient;

const assert = require('assert');

// Connection URL

const url = 'mongodb://localhost:27017/exampledb';

// Database Name

const dbName = 'exampledb';

(async function() {

let client;

try {

// Attempts to connect to the server

client = await MongoClient.connect(url);

console.log("Successfully connected to the server.");

const db = client.db(dbName);

} catch (err) {

//Log errors to console

console.log(err.stack);

}

if (client) {

client.close();

}

})();

The MongoClient.connect returns a promise, and any error is caught by the try …

catch block. You’ll be implementing the CRUD actions inside the try … catch block, and the API for that is similar to what we’ve covered in this tutorial. You can read more about it in the official documentation page.

MONGOOSE DRIVER

Another popular Node.js driver for MongoDB is Mongoose. Mongoose is built on top of the official MongoDB driver. Back when Mongoose was released, it had tons of features that the native MongoDB driver didn’t have. One prominent feature was the ability to define a schema structure that would get mapped onto the database’s collection.

However, the latest versions of MongoDB have adopted some of these features in the form of JSON schema and schema validation.

Apart from schema, other fancy features of Mongoose include Models, Validators and middlewares, the populate method, plugins and so on. You can read more about these in the Mongoose docs. Here’s an example to demonstrate mongoose.connect() for connecting to the database:

var mongoose = require('mongoose');

// Connection URL

const url = 'mongodb://localhost:27017/exampledb';

mongoose.connect(url);

var db = mongoose.connection;

db.on('error',

console.error.bind(console, 'connection error:'));

db.once('open', function() {

// we're connected!

});

Conclusion

MongoDB is a popular NoSQL database solution that suits modern development requirements. In this tutorial, we’ve covered the basics of MongoDB, the Mongo shell and some of the popular drivers available. We’ve also explored the common database operations and CRUD actions within the Mongo shell. Now it’s time for you to head out and try what we’ve covered here and more. If you want to learn more, I recommend creating a REST API with MongoDB and Node to acquaint yourself with the common database operations and methods.

# Document Outline

*   [Chapter 1](#index_split_000.html_p7)
*   [Chapter 2](#index_split_000.html_p20)
*   [Chapter 3](#index_split_000.html_p25)
*   [Chapter 4](#index_split_000.html_p41)
*   [Chapter 5](#index_split_000.html_p49)
*   [Chapter 6](#index_split_000.html_p65)
*   [Chapter 7](#index_split_001.html_p81)
*   [Chapter 8](#index_split_001.html_p86)