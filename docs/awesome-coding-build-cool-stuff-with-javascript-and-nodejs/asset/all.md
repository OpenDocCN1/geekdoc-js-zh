![](resources/title_page.jpg)

![Awesome Coding](resources/title_page.jpg)

## Awesome Coding

### Build Cool Stuff with JavaScript and Node.js

#### Engin Arslan

This book is for sale at [http://leanpub.com/awesomecoding](http://leanpub.com/awesomecoding)

This version was published on 2021-03-26

![publisher's logo](resources/leanpub-logo.png)

*   *   *   *   *

This is a [Leanpub](http://leanpub.com) book. Leanpub empowers authors and publishers with the Lean Publishing process. [Lean Publishing](http://leanpub.com/manifesto) is the act of publishing an in-progress ebook using lightweight tools and many iterations to get reader feedback, pivot until you have the right book and build traction once you do.

*   *   *   *   *

© 2021 Engin Arslan

## Table of Contents

## Guide

1.  [Begin Reading](#chap00.xhtml)

# 1 Preface

I have changed careers multiple times becoming a software developer. I studied Materials Engineering at the university, worked at a startup doing 3D modelling for games and then later became a Visual Effects Artist. Learning how to code and getting into software development was one of the best decisions I have ever made. It completely changed my life for the better.

As a software developer, I am now working in a financially rewarding field that is intellectually stimulating and can be performed from anywhere in the world. Being able to code can also feel extremely empowering. I know I have the skillset to build an application that billions of people in the world could use. Coding is a superpower in this digital economy. I believe it is also becoming a necessity. Many products and services are getting digitized, and there is greater demand for programmers than ever before.

I didn’t study computer science, and I wasn’t working in a field that required me to learn code before changing careers. Learning how to code wasn’t an obvious choice for me. I was working as a Visual Effects artist on movies and TV shows at the time. We used **3D** applications like **Maya** or **Houdini** to create digital scenes. Those applications were handling all the complexity involved in the process. In theory, that allowed us to focus on more creative aspects of the job. But in reality, our day-to-day job involved a lot of repetitive tasks that were very time-consuming. Luckily, these 3D applications exposed an **application** **programming interface** that we could use to control the application directly without relying on the user interface using a programming language called **Python**. I have started to experiment by writing short snippets of code that would automate small actions. The complexity of my programs grew over time. Not only was I able to automate my interactions with the software but also create solutions that were used by other artists in the company. Coding allowed my department to scale operations and deliver increasingly sophisticated graphics in a much more efficient way. I wrote programs that ended up getting used for TV shows and movies like **Vikings**, **The Strain**, **Silent Hill 2**, and **Pompeii**.

I started to enjoy programming more than my job, so I have decided to do this full-time. I only knew Python at the time, but the entry-level job market for Python software development didn’t seem great. I have decided to learn **JavaScript** and make it into **Web Development**. I spent more than a year without any guidance trying to learn web development in the evenings and weekends. I had no idea about what was important or not and how I should be investing my time. It was an incredibly frustrating experience.

I wrote this book so that you wouldn’t have the same difficulties I had while trying to learn how to code. With this book, I will teach you the essentials of programming with **JavaScript** and **Node.js** in a beginner-friendly way.

## Why Learn JavaScript?

There are a lot of programming languages out there. You might be wondering why you should be learning JavaScript. For one thing, JavaScript is one of the most widely used programming languages as it is built into every web browser. Almost all of the web pages and web applications you visit online use JavaScript to some degree.

The popularity of JavaScript has grown even more with the introduction of **Node.js** in 2009\. Node.js is a **programming environment** to run JavaScript outside of the browser. Previously JavaScript usage was limited to the web browser. With Node.js, JavaScript started to appear anywhere from web servers to desktop application development, wearables to robotics. This made JavaScript become one of the most prominent and flexible programming languages in the world.

JavaScript has a huge and vibrant community behind it due to its popularity. This means there is a lot of innovation and growth happening in the language. It also means that many people are out there to help you out if you ever get stuck with a problem. All these factors make JavaScript a great programming language to learn.

## What Will You Learn In This Book

This book will teach you the essentials of JavaScript from scratch. After establishing a foundation in JavaScript, you will learn about Node.js. All the while, you will be working on practical and interesting examples that involve data analysis, image manipulation, web scraping, command-line applications, natural language processing, and web APIs that get news, stock, and cryptocurrency data. After learning about the skills, tools, and technologies introduced in this book, you will also be able to build cool and interesting projects of your own using JavaScript and Node.js!

## Code Examples

The code samples from this book are available in a [GitHub repository](https://github.com/hibernationTheory/awesome-coding). You can download and run them on your own computer.

# I JavaScript Basics

# 2 Setting Up Your Development Environment

To start coding in **JavaScript**, we need an **environment** that can run the JavaScript code that we write. There are different kinds of environments we can use for executing JavaScript code. In this chapter, we will explore some of those options.

## Running JavaScript Inside the Developer Console

JavaScript is the programming language used for building web applications. That is why every browser is capable of running JavaScript code. We can even write JavaScript code inside the browser! If we are to launch the **Chrome** browser and then select `View > Developer > JavaScript console`, we can launch the **JavaScript console**. This interface allows us to write a single line of JavaScript at a time and execute it by pressing the **enter** key**.** We can try this by typing `console.log(2 + 2);` to the console and pressing **enter**. We would see the result of this calculation getting displayed. This is a neat feature but is not extremely useful for our purposes since the console only allows for a single line of code to be executed at a time.

![](resources/i_imgur_com---bOj2MKF.png)

All the other prominent browsers (like **Safari**, **Firefox**) also have a similar developer console that can run JavaScript code.

## Running JavaScript as Part of an HTML File

**HTML** is a formal language that describes how a document is structured. We can use HTML to describe the content of a web page. We can also use HTML files to load JavaScript files.

```
1 <h1>Hello World</h1>
2 <p>I am learning <strong>JavaScript</strong>!</p>
```

js-basics-01-setting-up/01.html

Here we have a code snippet written in the HTML language. HTML language consists of **tags** used to describe the **elements** of a document. Here we have an `h1` tag that represents the **main title** in a document. Then we have a `p` tag that describes a **paragraph**. Inside the `p` tag, we have a `strong` tag that indicates that the content it wraps is **important**. These tags help the web browser make sense of the document that we are providing.

HTML code is written inside HTML files. HTML files can also load JavaScript files to be executed by the browser.

Let’s first create an HTML file to be loaded by the web browser.

```
1 <!DOCTYPE html>
2 <html>
3   <body>
4     <h1>Hello World</h1>
5     <p>I am learning <strong>JavaScript</strong>!</p>
6   </body>
7 </html>
```

js-basics-01-setting-up/02.html

We have added more tags into this HTML code to make it a valid HTML document. We can now drag this file into a web browser or type the full file path into the address bar. The browser will open and render this file.

![](resources/i_imgur_com---z1Wk8C4.png)

We can use this HTML file to load JavaScript code as well. Let’s create a new file in the same directory as this HTML code with the name `main.js`. We can add these two lines of code inside the `main.js` file.

```
1 console.log("Hello World");
2 console.log(2 + 2);
```

js-basics-01-setting-up/main.js

Then, we will need to update our HTML file to load this JavaScript file.

```
1 <!DOCTYPE html>
2 <html>
3   <body>
4     <h1>Hello World</h1>
5     <p>I am learning <strong>JavaScript</strong>!</p>
6     <script src="main.js"></script>
7   </body>
8 </html>
```

js-basics-01-setting-up/03.html

We have added a new tag called `script`. We can use `script` tag to link to an external JavaScript file. It has an **attribute** called `src` that can be used to specify the file path of the file that we want to load. In this example, we need to ensure that the JavaScript file is in the same directory as the HTML file.

Let’s launch the JavaScript console after loading this file inside the browser. We would see the result of our JavaScript code is getting displayed in the console. This is a pretty reliable way of running JavaScript code on our computer.

## Running JavaScript Online

Since any browser can run JavaScript and HTML, many online editors help to do that in a very easy and practical way.

A couple of services that I use and like are [codepen.io](http://codepen.io), [jsbin.com](http://jsbin.com), and [codesandbox.io](http://codesandbox.io). There are many other services, but these three are the ones that I use the most. We can use all of them to write HTML and JS code inside the browser without creating any files on our computer. They are excellent environments for learning how to code and for prototyping ideas.

### Codepen

![](resources/i_imgur_com---dbnQvE9.png)

I love **Codepen** primarily because of the community aspect of it. It has tons of user-submitted content that shows you all the great things you can do using JavaScript, HTML, and CSS. It is both an amazing tool and a resource. If you go to their online code editor, there are sections that you can use to write HTML, JavaScript, and CSS. There is a white screen that will render your HTML. There is also a tab called **Console** that you can click to see the results of the JavaScript code that you execute.

### Jsbin

![](resources/i_imgur_com---8RPUgh5.png)

I use **Jsbin** very frequently because it is straightforward to get started. You just need to go to the URL, and you are immediately greeted with a coding editor. To prototype my JavaScript ideas, I select **JavaScript**, **Console**, and **Output** tabs in the menu. **JavaScript** is the field that you can use to write JavaScript code. **Console** displays the output of your code in real-time. You can use the **Clear** button to eliminate the errors that can accumulate as you write your code.

### Codesandbox

![](resources/i_imgur_com---Kt6ONuA.png)

**Codesandbox** has excellent features, and it is an incredible tool if you want to prototype a relatively complex idea. It has very advanced features that make it extremely capable as an online editor.

## Summary

There are several ways that we can start writing JavaScript. These are:

*   Writing it directly inside the browser.
*   Writing it inside a `.js` file and loading that file through an **HTML** file.
*   Using an online editor.

Of all these options, the first one is not very scalable since it only allows for a single line to be written at a time. We can instead write JavaScript files locally and load them in the browser with an HTML file. We can then use the **JavaScript console** inside the browser to see the code displayed from our JavaScript file.

The last option that we learned about is an **online editor**. Online editors are incredibly convenient because we don’t have to manage any files on our computers. We just visit a web page, and we are good to go. They are great environments for learning and experimentation.

While following this book, you can either use a local JavaScript file or use an online editor. They should both work for our purposes.

# 3 Basic Data Types and Variables

If we enter a number like `42` and execute that code in a JavaScript environment, we would see that it runs without any errors. That is a great sign. It means that we wrote something that the JavaScript language understands. The value that we have entered here is of type `number`. There are a couple of different **types** of values that JavaScript understands. Some of these are:

*   **numbers**
*   **strings**
*   and **boolean** values

In this section, we will learn about **numbers** and **strings**.

## Numbers

As we have seen before, a JavaScript code that only has a number inside would run without any errors. That is because numbers are a **native data type** in JavaScript. There are other native data types in JavaScript, such as **strings** and **booleans**. We will learn about them soon.

JavaScript programs execute from top to bottom unless we use a structure that would alter the program’s flow. This means that we can keep adding different numbers on different lines, and JavaScript would not complain when we execute this code.

```
1 42;
2 1;
3 2;
4 3;
```

It is good that we can write things in JavaScript that doesn’t make it complain (or crash and burn), but this is hardly impressive. Let’s do something that is slightly more useful, like displaying what we are putting in this file on the screen.

There is a programming structure called a **function** that packs a bunch of operations together for reusability. We will look into what functions are later on. For now, just know that there is a function called `console.log` that we can use to display values on the screen. It works like this:

```
1 console.log(42);
```

We write the name of the function and provide a value to it inside parentheses. The function displays that value to the screen when it runs. This particular code displays the number `42` on the screen.

```
1 console.log(1);
2 console.log(2);
3 console.log(3);
```

This program would display the number `1, 2, 3` on the screen on separate lines.

We can also write fractional numbers in JavaScript. Such as:

```
1 console.log(3.14);
```

These numbers are sometimes referred to as **floating-point numbers**.

### Operators

We can use mathematical operators to do calculations using numbers. Here are some of the operators that we can use:

*   `+`
*   `-`
*   `/`
*   `*`

Using these operators, we can perform mathematical operations between numbers.

```
1 console.log(10 + 20 - 5);
```

The above operation would display `25` to the screen.

Try to guess what would be the result of the following operation:

```
1 console.log(10 - 2 * 2);
```

If you have guessed `16`, you are making a common mistake. The math operators have different **precedence**. Multiplication and division happen before addition and subtraction. That’s why the result would actually be `6`. We would first have `2` multiplied by `2`, and then that result would get subtracted from `10`.

We can force a specific order of operations by using **parentheses** (`()`). The operation that is in the parentheses would happen before the others.

```
1 console.log((10 - 2) * 2);
```

This would result in `16` since we are forcing `10-2` to happen before multiplication with the usage of parentheses.

Let’s take a look at our next data type **strings**.

### Strings

If we wrote a text in the JavaScript console and tried to execute that code, we would likely get an error.

```
1 hello;
```

If we wanted to represent textual data in JavaScript, we need to define it as a `string`. A `string` is anything that is defined in between **quotation marks**. We can use single quotes (`'`) or double quotes (`"`) to define a string. The only restriction is that we need to finish the string with the type of quotation mark we have started with.

```
1 "hello";
2 "42";
```

**Consistency** is essential in programming. Even if you are doing something wrong, it would be easy to fix if you have been doing it consistently wrong. That is not to say choosing one kind of quotation mark is wrong over the other, but whatever your choice is, it should stay consistent throughout the codebase.

We might encounter a problem with single quotation mark usage if our text also contains a single quotation mark. If we don’t want that quotation mark to be interpreted as the end of the text, we can use a backslash character (`\`) in front of it.

```
1 'don\'t stop moving';
```

The backslash allows us to **escape** the common interpretation of the quotation mark.

We can use the addition math operator with strings as well. We can perform addition in between strings and other data types.

```
1 console.log("hello" + " " + "world");
```

This would display `"hello world"` on the screen. Notice, we have an empty string in the middle. The space character still counts as a string and provides the spacing we need in between two words.

We can also add a number and a string together.

```
1 console.log("hello" + 2);
```

JavaScript would convert the number to a string, in this case resulting in `hello2`. If we try to perform other operations between strings and numbers (like multiplication), we will get a `NaN` result, which means **not a number**. We would rarely want this value to occur in our program. A `NaN` would convert other values into `NaN` when used in math operations resulting in erroneous results to accumulate in the program.

## Variables

One of the most basic functionalities that we would want from a computer program is to store the results of our operations inside its **memory**. This is made possible by a programming structure called **variables**.

A variable is a name that points to a value inside the computer memory. We declare a variable name using one of the variable declaration keywords like `var`, `let`, `const` (more on this later) and **assign** a value to that variable. Here is an example:

```
1 const bigNumber = 999999;
```

From then on, the variable name is a reference to the value that is assigned to it. The `=` symbol assigns the **value** on the right-hand side to the **variable** name on the left-hand side. As a result, the below operation would display the number that is assigned to the variable.

```
1 console.log(bigNumber);
```

Variables are incredibly useful and essential since they allow us to reference our programs’ values at later stages. Here is an example of that:

```
 1 const piNumber = 3.14159;
 2 const radius = 5;
 3 
 4 const areaOfCircle = radius * piNumber * piNumber;
 5 const diameterOfCircle = 2 * radius;
 6 const circumferenceOfCircle = 2 * piNumber * radius;
 7 
 8 console.log(areaOfCircle);
 9 console.log(diameterOfCircle);
10 console.log(circumferenceOfCircle);
```

js-basics-02-basic-data-types/01.js

First of all, I am sorry to give you an example that makes such heavy use of math and geometry. Quite honestly, the day-to-day practice of programming can have very little to do with mathematics. It is simply not true that you need to be good at math to become a good programmer. Having said that, examples regarding mathematics are useful when most of what we know about programming has to do with numbers usage.

With that apology out of our way, we can see in this example how the usage of variables helps us when building programs. Since we have saved the values for the **pi number** and the **radius** inside variables, we could reference those values by just using their names. Here is what the same program would have looked like if it didn’t make use of variables.

```
1 const areaOfCircle = 5 * 3.14159 * 3.14159;
2 const diameterOfCircle = 2 * 5;
3 const circumferenceOfCircle = 2 * 3.14159 * 5;
4 
5 console.log(areaOfCircle);
6 console.log(diameterOfCircle);
7 console.log(circumferenceOfCircle);
```

js-basics-02-basic-data-types/02.js

This program looks shorter, but there are a couple of problems with it.

*   Code is not **DRY**
*   It uses **Magic Numbers**
*   There is no **Single Source of Truth**

Let’s take a look at what is meant by each of these issues.

### Code is not DRY

**DRY** in software engineering stands for **Don’t Repeat Yourself** and is an essential principle in programming. It means that we should not repetitively do the same things over and over again. Here we are typing the pi number and radius value over and over again across our program. If we needed to change the radius’s value, we would have to do it in multiple places. This kind of repetition exposes us to making mistakes. Every time we are typing the pi value, there is a chance that we can make a mistake and mistype it. Following the **DRY** principle and using a variable to store those values minimizes the risks of such problems.

### Usage of Magic Numbers

What do you think the number `5` represents in the above example? If you know geometry well, you might be able to guess that it is the value of the radius of a circle, but that still requires a mental effort. This is what we sometimes refer to as a **magic number** in programming. It does something and gets us to a result, but it is not entirely clear what it is or how it does that.

It is said that programs are read more than they are written. We should ensure that we create legible programs that are easy to read and do not hide nasty bugs inside. Giving meaningful variable names to values used in our programs ensures that our programs are easy to read and understand.

### No Single Source of Truth

In the program above, the value for the radius of the circle is spread throughout the code. There is no **single source** for that value. If we wanted to change that value, we would need to do it in multiple places. The **truth** or the knowledge of the value is **encoded** in multiple places. This can create ambiguity. Imagine there was a mistake in the program, and one line had a different value. How would we know which of the values is the correct one? We can’t be sure by looking at the program. Having a single source for that value would give us the confidence that the defined value is the correct one.

We are at the beginning of our programming journey, but these are essential software engineering fundamentals. A structure as simple as variables allows us to alleviate the above problems and write readable and maintainable programs.

### Choosing Variable Names

There are some rules and conventions regarding how we choose variable names. Here are some rules that we have to follow:

*   Variable names can’t start with a number, like `1myVariable`.
*   Variable names can’t contain a space, like `my variable`.
*   Variable names can’t contain a dash character (`-`), like `my-variable`.
*   Variable names can’t make use of **reserved** **words**, like `const`.

Of all these rules, the last one might look like it would be the hardest to follow. Reserved words in JavaScript are **keywords** that are part of the language. For example, the word `var` or `const` is reserved since it is a JavaScript keyword used to define a variable.

How could we know which variable names are reserved when we are just starting with programming? This is something that you would slowly get accustomed to as you learn more of the language. If we break this rule, our programs will fail to compile with an error that says `"SyntaxError: Unexpected token`.

Here are some conventions for choosing variable names. These are not hard rules but helpful and robust suggestions.

**Use Camel Casing or Underscores**

Use **camel casing** or **underscores** (`_`) when using a variable name that consists of multiple words to improve legibility.

*   Here is an example of a camel-case variable name: `myVariable`. Notice the first letter of the first word is lowercase. Any subsequent words start with an uppercase letter.
*   Here is an example of the usage of underscore: `my_variable`. In this case, all the words are lowercase but separated by an underscore.

Which of these methods we choose depends on the conventions of the codebase we are working on. In JavaScript, camel-case is generally the convention to go with, but there might be exceptions out there.

**Choose Meaningful Names**

We should use meaningful variable names to name variables. Imagine the following scenario:

```
1 const n = 3.14;
2 const r = 5;
3 
4 const a = r * n * n;
5 console.log(a);
```

This is a program that calculates the area of a circle with a radius value of `5`. Good luck understanding that by looking at the variable names. We should choose meaningful and explicit variable names when writing our programs. Notice how much better these lines of code read when we name everything more clearly.

```
1 const piNumber = 3.14159;
2 const radius = 5;
3 
4 const areaOfCircle = radius * piNumber * piNumber;
5 
6 console.log(areaOfCircle);
```

Notice that even `r` is not a good enough variable name. We need to be explicit enough to make our programs readable for others (and our future self!).

**Don’t Start With an Uppercase**

We shouldn’t start variable names with uppercase or so-called title case. We don’t do this:

```
1 const PiNumber = 3.14;
```

We might see names that have their first letter uppercase. This is reserved for some special use cases that we will learn about later. Don’t use title name variable names until then.

### Declaring Variables

So far, we have been declaring our variables using the `const` keyword.

```
1 const myVariable = 42;
```

For the longest time, JavaScript only had the `var` keyword for the declaration of variables. Later, two other variable declaration keywords, `let` and `const` got introduced. Here is the difference between each of them.

### var Keyword

When we declare a variable name using a `var` keyword, that variable name’s value can get reassigned. Like this:

```
1 var myVariable = 42;
2 myVariable = 7;
```

This proved to be problematic because it made it hard to keep track of the variable’s value throughout the program’s lifetime. That’s why we now have the `const` keyword to declare variables.

### const Keyword

```
1 const myVariable = 42;
```

When we declare a variable using the `const` keyword, we can’t reassign a different value to that variable. This ensures the value stays consistent throughout the lifetime of our program. It is a limitation, but it is one of those limitations that make our life as programmers easier. 95% of the time, I use the `const` keyword to declare my variables. But there are times that we need to reassign the value of the variable. That is when `let` keyword comes into play.

### let Keyword

`let` keyword is very similar to the `var` keyword in that it allows for a new value to be assigned to the variable declared using the `let` keyword.

```
1 let myVariable = 42;
2 myVariable = 7;
```

There are some different problems with the usage of the `var` keyword that we might not be able to appreciate with the current state of our knowledge. It is primarily regarding the variable’s **scope**, meaning where that variable is going to be accessible from. `let` keyword handles that scope issues for us as well. So with the introduction of the `let` keyword, I have completely stopped using the `var` keyword. `const` and `let` is going to be the only two keywords that we will be using moving forward. It is still important for us to know that the `var` keyword exists, but we would probably see it used less in modern codebases.

Let’s take a look at two more things before wrapping up this section.

## Semicolons

In JavaScript, we can signal the end of a statement using a semicolon (`;`) character. This symbol’s usage is not mandatory, but it helps the **JavaScript interpreter** in some edge cases. Even if we are working with a team that requires us to use semicolons in our code, these kinds of formatting issues are usually handled and automated by **code editors** nowadays. So semicolon usage is not something that we would have to worry about too much about since it can be automatically handled for us when using a code editor with correct configurations. It is one of those things that is good to know.

Moving forward, I will try to use semicolons in my code examples because I am old school like that.

## Comments

There are times that we might not want to have some of the things that we write in our programs to be executed. For example, we might want to leave a comment in our code that explains why we wrote a certain thing the way it is. This can be useful for whoever is going to read the code at a later time. And this might even include ourselves.

This is when comments are useful. It allows us to write things in our program that is not going to be executed by JavaScript.

Whenever we use the `//` operator before a line, JavaScript skips executing that line.

```
1 // This is a comment
2 // These lines would not be executed by JavaScript
```

## Summary

We are just starting our programming journey, but we have learned a lot in this chapter. We learned about some of the **data types** in JavaScript, like **numbers** and **strings**. We have also learned about the **math operators** and the **precedence** that these operators have. Then, we got introduced to **variables**. We looked into the rules and conventions that govern the naming of the variables. Additionally, we have learned about `let`, `const`, and `var` **keywords** used to declare variables. It was important for us to learn the `var` keyword, but we will mostly use `const` and `let` moving forward.

Another thing that was introduced in this chapter is the usage of **semicolons** at the end of lines. They are not mandatory in JavaScript but can be good to have.

We learned about **comments** as well. Comments are parts of our programs that are not executed and are generally there for instructional purposes.

Finally, we got introduced to three fundamental programming principles. Importance of **DRY**, having a **Single Source of Truth,** and avoiding **Magic Numbers**. These are very foundational principles in software development and are very useful to keep in mind.

# 4 Functions

In the previous section, we have learned about the `console.log` function. A **function** is a programming construct that combines different operations for purposes like reusability, convenience, etc.

In this section, we will learn more about functions. We will also learn about defining our functions. Functions are incredibly powerful programming structures that make building complex programs possible.

JavaScript and the environments that we use JavaScript in, such as **Web Browsers**, have many built-in functions that we can use. `console.log` is an example of such a function.

For the reasons that we will be learning about later, there is a `.` character in the name of this function.

To use a function, we need to **call** it **(**also know as **executing** a function**)**. If we were to type the name of the function and execute that code, nothing would happen.

```
1 console.log;
```

Calling a function requires us to place parenthesis next to it.

```
1 console.log();
```

When we execute this function, still nothing happens. That is because `console.log` function requires us to pass an **input** (or inputs) to it to work correctly. The input to a function is called an **argument**. We provide the arguments to a function inside the parentheses. Let’s call the `console.log` function with an argument.

```
1 console.log("hello");
```

We already know what `console.log` function does. It displays the given input to the screen. A function can take one or multiple arguments, depending on how it works. Multiple arguments to a function are separated by the comma (`,`) character. We can also pass multiple inputs to the `console.log` function. It would display each input on a separate line.

```
1 console.log("hello", "world");
```

Let’s take a look at some other built-in JavaScript functions.

## parseFloat Function

`parseFloat` is a built-in JavaScript function. It works with a single input and tries to convert it into a floating-point number (a fractional number). Here is how it works.

```
1 parseFloat("3.14");
```

This operation would convert the string `3.14` to a numeric `3.14`. We can ensure that is the case by making use of that value in operation.

```
1 const piNumberAsString = "3.14";
2 
3 console.log(piNumberAsString + 10);
4 console.log(parseFloat(piNumberAsString) + 10);
```

js-basics-03-functions/01.js

The first operation where we are using the pi number as a string would result in the value `3.1410` because when adding a string and a number, they simply get combined. It doesn’t work as a mathematical operation.

But the second operation where we are converting the pi number into a floating-point number would result in `13.14` because it is now a mathematical operation in between two numbers.

This example might have been hard to read because of the **nested functions** (function calls inside function calls) in the second operation.

```
1 const piNumberAsString = "3.14";
2 
3 console.log(parseFloat(piNumberAsString) + 10);
```

js-basics-03-functions/01_01.js

To make this example easier to read, we can save the `parseFloat` operation inside a variable and use that variable instead of calling `parseFloat` inside another function. Here is how to do that:

```
1 const piNumberAsString = "3.14";
2 const piNumber = parseFloat(piNumberAsString);
3 
4 console.log(piNumberAsString + 10);
5 console.log(piNumber + 10);
```

js-basics-03-functions/02.js

Now, this function would return the same result as before but is more readable. This was possible because the `parseFloat` function **returns** the result of its operation (more on **returning** later).

If we provided a value to the `parseFloat` function that can’t be converted into a floating-point number, it would return a `NaN`.

```
1 const result = parseFloat("hello");
2 console.log(result);
```

js-basics-03-functions/02_01.js

## parseInt Function

`parseInt` is a built-in JavaScript function that is very similar to `parseFloat`. It tries to convert the given value to an **integer** **number** (also known as **whole numbers**).

If we provided a value to the `parseInt` function that can’t be converted into an integer number, it would return a `NaN`.

```
1 const piNumberAsString = "3.14";
2 
3 console.log(parseInt(piNumberAsString)); // Would result in 3
```

js-basics-03-functions/02_02.js

In this example, `parseInt` function takes a **floating-point** number and converts it into an integer (`3` in this case).

## Thinking About Functions

We now know the three most important things to think about when using a function.

*   What a given function does.
*   What kind of inputs does it require (and how many)?
*   What kind of output does it have?

Having answers to these questions helps us be more confident when using a function.

Let’s answer these questions for the functions that we have learned about so far.

### console.log

*   **What does it do?** It displays the given inputs to the screen.
*   **What kind of inputs does it require?** It works with one or more inputs of any kind. The input can be a number or a string. It can be other data types that we haven’t learned about as well.
*   **What kind of output does it have?** It doesn’t have an output. We can verify this by trying to capture the output of the function inside a variable.

```
1 const result = console.log("hello world");
2 console.log(result);
```

We would see that the result is `undefined`. This means that the result simply does not exist.

### parseFloat

*   **What does it do?** It tries to convert the given input to a floating point number.
*   **What kind of inputs does it require?** It works with a single input. The input can be a number or a string.
*   **What kind of output does it have?** The output is a floating-point number if the given value is successfully converted. If not, this function would return a `NaN` value.

### parseInt

*   **What does it do?** It **tries** to convert the given input to an integer number (whole number).
*   **What kind of inputs does it require?** Unlike `parseFloat`, the `parseInt` function works with two inputs. The second input is optional, and we can ignore it for our learning purposes.
*   **What kind of output does it have?** The output is a whole number if the given value is successfully converted. If not, this function would return a `NaN` value.

We can think of functions as **black boxes**. It accepts one or more inputs and can have an output. But we don’t necessarily know what happens inside. Think of an **ATM (Automated Teller Machine)**. An ATM can take your bank card and your commands as an input, do something with those commands, and can have money and receipts as output. You don’t necessarily know what goes on inside an ATM machine either.

## Other JavaScript Functions

Here are few other JavaScript functions that are pretty useful.

### Math.abs

*   **What does it do?** Returns an **absolute** value for a given number. In mathematics, the absolute value of a number is the **positive** value for that number. It means that if we pass a negative number to this function, it will return the same number but without the negative sign in front of it.
*   **What kind of inputs does it require?** It works with a single argument that is a number.
*   **What kind of output does it have?** The output is a positive number of a given kind. It returns `NaN` if a non-numeric input is provided.

```
1 const value = -42;
2 const absoluteValue = Math.abs(value);
3 console.log(absoluteValue); // Would be `42`
```

js-basics-03-functions/02_03.js

### Math.random

*   **What does it do?** It returns a **“random”** (actually **pseudo-random**) number between `0` and `1` when it is called.
*   **What kind of inputs does it require?** It doesn’t require any inputs.
*   **What kind of output does it have?** The output is a floating-point number that is between `0` and `1`.

```
1 const randomNumber = Math.random();
2 console.log(randomNumber);
```

## Defining Functions

Using built-in functions would only take us so far. We would eventually want to define our own functions to be able to write more advanced programs. Let’s assume an operation that we would like to convert into a function, such as displaying `Hello World` to the screen.

```
1 console.log("Hello World");
```

We want to create a function with the name `hello`, which would execute this statement when called.

```
1 hello();
```

Here is how to do it. We declare a function by using the `function` keyword and coming up with a name for our function. In this case, we will call the function `hello`. We add parentheses next to the name and curly braces after that.

```
1 function hello() {}
```

This is now a function definition for a function named `hello`. When called, this function wouldn’t do anything because the function body, which is in between braces, is currently empty.

```
1 hello();
```

Inside the function definition braces, we should define the operations that we would like this function to perform. In this case, it would be placing the `console.log` statement in there.

```
1 function hello() {
2   console.log("Hello World");
3 }
```

This function would now display `Hello World` to the screen when called.

```
1 hello();
```

## Functions with Parameters

What if we wanted to create a function that would take user-provided input? For example, think of a function called `greet` that would display a greetings message customized for the given input. Where running this function below:

```
1 greet("John");
```

would display a message like `Welcome John`.

To be able to do this, we need to define a function that has parameters.

```
1 function greet(firstName) {}
```

Here we defined a function called `greet` that accepts a single parameter saved under a variable name `firstName`.

This means that when we call this function by providing an **input** (which is also called an **argument**). It would get that provided input and assign it to a variable called `firstName`. In more technical words, the argument that we pass to a function gets mapped to the **parameter** that is in the function definition.

```
1 greet("John");
```

We can verify this by making use of that argument inside our function. Let’s start by just using a `console.log` statement.

```
1 function greet(firstName) {
2   console.log(firstName);
3 }
```

Now, this function would display the given input to the screen, whatever that given input is.

```
1 greetings(42);
```

We want to display a welcome message by using this `greetings` function. This is how we would do it:

```
1 function greet(firstName) {
2   console.log("Welcome " + firstName);
3 }
```

This function would now display a welcome message customized for any given name.

```
1 greet("John");
2 greet("Jane");
3 greet("Humans");
```

The name of the parameter in our example is `firstName`. We could have chosen any name for this parameter, and the example still would have worked. It is an arbitrary name. The rules and conventions around choosing variable names apply to choosing parameter names and function names as well. We should always choose variable names that make sense.

Additionally, when naming functions, try to use a verb. A function usually describes an action, so it makes sense to name functions using verbs.

## Functions with Multiple Parameters

We can also define functions that have multiple parameters. Each parameter that we define should be separated with a comma (`,`).

```
1 function greet(firstName, lastName) {}
```

Here we defined a function called `greet` that takes two parameters: `firstName` and `lastName`.

Here is what such a function can look like:

```
1 function greet(firstName, lastName) {
2   console.log("Welcome " + firstName + " " + lastName);
3 }
```

This function now makes use of both of these parameters. We can pass two arguments to this function, separated by a comma.

```
1 greet("John", "Doe");
2 greet("Jane", "Doe");
```

We can define functions that accept as many arguments as we would like.

## Functions that Return a Value

Let’s create a function that would calculate the final price of a product given the discount amount.

If the product’s price is 100$, and it has a 20% discount, then its final price would be 80$. Our function should do this calculation for us.

```
1 getFinalPrice(100, 20);
```

Here is what the definition of that function would look like.

```
1 function getFinalPrice(initialPrice, discount) {
2   const finalPrice = initialPrice - (initialPrice * discount) / 100;
3   console.log(finalPrice);
4 }
5 
6 getFinalPrice(100, 20);
7 getFinalPrice(50, 20);
8 getFinalPrice(200, 60);
```

js-basics-03-functions/03.js

Let’s try to use this function to calculate the final price of a 100$ product that had a discount of 20% and then additional 30% over the already discounted price. We might be tempted to do something like this:

```
1 function getFinalPrice(initialPrice, discount) {
2   const finalPrice = initialPrice - (initialPrice * discount) / 100;
3   console.log(finalPrice);
4 }
5 
6 const priceAfterFirstDiscount = getFinalPrice(100, 20);
7 const finalPrice = getFinalPrice(priceAfterFirstDiscount, 30);
```

js-basics-03-functions/04.js

This code wouldn’t work. `getFinalPrice` function does a great job at calculating the discounted price of a product, but it just displays the resultant price as a result. It does not return the calculated value from the function. That is why the value of `priceAfterFirstDiscount` variable after this operation is `undefined`:

```
1 const priceAfterFirstDiscount = getFinalPrice(100, 20);
```

We need to ensure that this function returns the result of the calculations from inside the function to the outside context, where we call the function to assign that result to a variable. We can do this by using the `return` keyword.

```
1 function getFinalPrice(initialPrice, discount) {
2   const finalPrice = initialPrice - (initialPrice * discount) / 100;
3 
4   return finalPrice;
5 }
6 
7 const priceAfterFirstDiscount = getFinalPrice(100, 20);
8 const finalPrice = getFinalPrice(priceAfterFirstDiscount, 30);
9 console.log(finalPrice);
```

js-basics-03-functions/05.js

We have removed the `console.log` statement from inside the function. We are now using a `return` keyword to return the `finalPrice` from inside the function to the outside context.

`return` is a keyword that can only be used inside functions. It returns the value next to it from the function to the context that the function is called in.

Using the `return` keyword, we can now create a function that can do some calculations and return that value for further processing.

We now know quite a bit about functions. Let’s continue our learning by building two useful functions.

## A Real World Function Example

We can calculate a bunch of values regarding a circle given its **radius**.

The **diameter** of a circle is **two times its radius**.

The **circumference** of a circle is calculated using formula `2 * π * r`, where `π` is the pi number (`3.14`), and the `r` is the radius of a circle.

The **area** of a circle is calculated by the formula `π * r * r` where `π` is the pi number (`3.14`), and the `r` is the radius of a circle.

Let’s create a function that would calculate these three values for a given radius value and display them to the screen.

```
 1 function getCircleData(radius) {
 2   const piNumber = 3.14;
 3 
 4   const diameter = radius * 2;
 5   const circumference = diameter * piNumber;
 6   const area = piNumber * radius * radius;
 7 
 8   console.log("For the circle of radius: " + radius);
 9   console.log("Diameter is: " + diameter);
10   console.log("Circumference: " + circumference);
11   console.log("Area is: " + area);
12 }
```

js-basics-03-functions/06.js

Notice that this function doesn’t make use of the `return` keyword. It merely displays the results to the screen. What if we wanted to return these results from the function? If we tried to do so, we might find out that the `return` keyword only allows us to return one value from a function.

There are **data structures** in JavaScript we can use to store multiple values and return that one data structure from a function instead. We will learn about those later.

It is usually a better idea to create functions that only do one thing at a time. So this program would be better if it was written like this:

```
 1 function getDiameter(radius) {
 2   return radius * 2;
 3 }
 4 
 5 function getCircumference(radius) {
 6   const piNumber = 3.14;
 7   const diameter = getDiameter(radius);
 8 
 9   return diameter * piNumber;
10 }
11 
12 function getArea(radius) {
13   const piNumber = 3.14;
14 
15   return piNumber * radius * radius;
16 }
17 
18 function getCircleData(radius) {
19   const diameter = getDiameter(radius);
20   const circumference = getCircumference(radius);
21   const area = getArea(radius);
22 
23   console.log("For the circle of radius: " + radius);
24   console.log("Diameter is: " + diameter);
25   console.log("Circumference: " + circumference);
26   console.log("Area is: " + area);
27 
28   return diameter, circumference, area;
29 }
30 
31 const result = getCircleData(5);
32 console.log(result);
```

js-basics-03-functions/07.js

Our code turned out to be lengthier in this case, but we have now created a more robust program. It has a bunch of **single-purpose functions**. Having single-purpose functions make it easier to reason what is happening in our programs. If something is not working, we can just check to see what is happening in the function responsible for the calculation that is not working as expected.

Another benefit of having single-purpose functions is that we now have more primitive building blocks that we can utilize differently later. For example, we now have a function that is only responsible for calculating a circle area. It is potentially more usable in different contexts than a function that calculates the area and does a bunch of other things.

One potential improvement we can make to this function is creating a shared variable for the `piNumber`. In this example, both the `getCircumference` and the `getArea` function defined their own `piNumber`. This is not only wasteful, but it also breaks the **Single Source of Truth** principle. It is not like the pi number would change from one function to another, so we shouldn’t define it inside each function that uses it. Better to create a variable that we can reuse inside each function

```
 1 const piNumber = 3.14;
 2 
 3 function getDiameter(radius) {
 4   return radius * 2;
 5 }
 6 
 7 function getCircumference(radius) {
 8   const diameter = getDiameter(radius);
 9 
10   return diameter * piNumber;
11 }
12 
13 function getArea(radius) {
14   return piNumber * radius * radius;
15 }
16 
17 function getCircleData(radius) {
18   const diameter = getDiameter(radius);
19   const circumference = getCircumference(radius);
20   const area = getArea(radius);
21 
22   console.log("For the circle of radius: " + radius);
23   console.log("Diameter is: " + diameter);
24   console.log("Circumference: " + circumference);
25   console.log("Area is: " + area);
26 
27   return diameter, circumference, area;
28 }
29 
30 const result = getCircleData(5);
31 console.log(result);
```

js-basics-03-functions/08.js

Now, this is much better. There is one more learning to be had here, and that is regarding the **scope** of variables.

The variable `piNumber` is accessible from inside the `getArea` or `getCircumference` functions. Any variable declared outside the context of a function would be accessible from functions inside that context. This doesn’t work the other way around, though. A variable that is defined inside a function wouldn’t be accessible from outside that function. For example, the `diameter` variable declared inside the `getCircumference` function wouldn’t be accessible outside that function. Trying to do so would result in an error.

```
1 const piNumber = 3.14;
2 
3 function getCircumference(radius) {
4   const diameter = getDiameter(radius);
5 
6   return diameter * piNumber;
7 }
8 
9 console.log(diameter);
```

js-basics-03-functions/09.js

## Callback Functions and Anonymous Functions

A **callback function** is just a descriptive name for a function that gets passed into another function. The function that receives the callback function chooses when and how it wants to execute the function. Here is a straightforward example of a callback function.

```
 1 function someOperation() {
 2   console.log("this is a function that represents some operation");
 3 }
 4 
 5 function logStartAndEndForOperation(callbackFunction) {
 6   console.log("start of operation");
 7   callbackFunction();
 8   console.log("end of operation");
 9 }
10 
11 logStartAndEndForOperation(someOperation);
```

js-basics-03-functions/10.js

In this example, `someOperation` is a callback function in relation to `logStartAndEndForOperation` function since it is passed as an argument to that function. `logStartAndEndForOperation` function takes a callback function as an argument and determines how to call that given function.

There is a function called `setTimeout` in JavaScript. `setTimeout` takes a callback function and a value that specifies a millisecond amount. `setTimeout` executes the callback function after the given amount of milliseconds. Here is how it works.

```
1 function helloWorld() {
2   console.log("Hello World");
3 }
4 
5 const oneSecond = 1000; // one second is 1000ms
6 const threeSeconds = oneSecond * 3;
7 
8 setTimeout(helloWorld, threeSeconds);
```

js-basics-03-functions/13.js

In this example, `helloWorld` is a callback function. It is passed into `setTimeout` as an argument, and it gets called by the `setTimeout` after three seconds.

Callback functions are a frequently used pattern in JavaScript. We will see more usages of callback functions in the following chapters.

### Anonymous Functions

A concept that is closely related to callback functions is **anonymous functions**. An anonymous function is a function that is defined without specifying a name. We usually do this for defining functions that we won’t reuse in our program. It saves us from having to come up with a name for a function that is only going to be used once. In the above example, we could define the `someOperation` function as an anonymous function instead.

```
1 function logStartAndEndForOperation(callbackFunction) {
2   console.log("start of operation");
3   callbackFunction();
4   console.log("end of operation");
5 }
6 
7 logStartAndEndForOperation(function () {
8   console.log("this is a function that represents some operation");
9 });
```

js-basics-03-functions/11.js

We are now defining a function inside the parentheses of the `logStartAndEndForOperation` function. This function doesn’t have any name, so it is an anonymous function. We won’t be able to reuse it since we have no way of referring to it. Using anonymous functions as callback functions is a common pattern in JavaScript.

There is one more function concept that is closely related to callback functions and anonymous functions. That is the **arrow function expression**.

## Arrow Function Expression

**Arrow function expression** is a shorthand way of creating functions. We have previously seen how to create functions using the `function` keyword.

```
1 function myFunction() {}
```

Arrow function expression allows us to create a function without using the `function` keyword.

```
1 const myFunction = () => {};
```

This is an arrow function. Arrow functions don’t have a name, but we can save them inside a variable to assign a name to them. They really shine when we are working with anonymous functions since they are much shorter to write than function statements. Let’s rewrite the above example using arrow functions.

```
1 function logStartAndEndForOperation(callbackFunction) {
2   console.log("start of operation");
3   callbackFunction();
4   console.log("end of operation");
5 }
6 
7 logStartAndEndForOperation(() => {
8   console.log("this is a function that represents some operation");
9 });
```

js-basics-03-functions/12.js

The anonymous function was a bit easier to write using the arrow function. Arrow functions have some different properties than normal functions, but these differences are not very important for us at the moment. We can simply think of them as function expressions that are easier to write.

## Summary

In this chapter, we have learned about functions. Some functions are built-in to the JavaScript language (or part of the environment that JavaScript runs), such as `parseFloat,` `parseInt`, `Math.random`, `Math.abs`, and `console.log`.

When using functions, three essential things that we need to know about are what do they do, what kind of inputs do they require, and what kind of output do they have.

We have also learned about creating our own functions. We can define functions that have any number of **parameters**. Parameters of a function are defined inside parentheses and are separated by a comma. We can call functions by providing **arguments**, and those **arguments** get mapped to the **parameter** names that we have defined. We can use the `return` keyword to return a value from a function.

It is important to build functions that have a **single responsibility** and use verbs when naming functions since they represent actions.

Finally, three closely related function concepts are **callback functions**, **anonymous functions,** and **arrow function expression.** A **callback function** is simply a name given to a function passed as an argument to another function. `setTimeout` is an example of a JavaScript function that works with a callback function.

We can define functions without giving names to them. In which case, they are referred to as **anonymous functions**. **An arrow function expression** is a shorter way of defining functions and is suitable for declaring anonymous functions.

Functions are incredibly powerful programming structures that make building complicated applications possible. We will be using them a lot moving forward.

# 5 Comparison Operators and Conditionals

## Boolean Data Type

So far, we have learned two data types: **numbers** and **strings**. In this section, we will be learning about a new data type called **booleans.**

A boolean is a `true` or a `false` value. Here is an example of a boolean.

```
1 const x = true;
```

Here, the variable `x` has a value `true`, which is of type `boolean`.

Boolean values are generated as a result of using **comparison operators**.

## Comparison Operators

**Comparison operators** are operators that allow us to compare two values and generate a boolean value as a result. Here is a list of comparison operators:

*   `>` Bigger Than
*   `<` Smaller Than
*   `===` Equal
*   `>=` Bigger Than or Equal
*   `<=` Smaller Than or Equal
*   `!==` Not Equal

And here are some example usages of these Boolean operators:

```
1 console.log(10 > 3);
2 console.log(-10 < 0);
3 console.log("John" === "John");
4 console.log(10 >= 10);
5 console.log(10 <= 10);
6 console.log(42 !== 7);
```

js-basics-04-flow-control/01.js

All of these operations would result in a `true` value.

There is also the `!` operator that inverts the value of a boolean result.

```
1 const myVariable = true;
2 console.log(!myVariable); // false
```

In the above example, `!myVariable` would be equivalent to `false`. That is because using `!` in front of a boolean would invert the value of that boolean.

There are a couple of complexities that we need to be aware of regarding using comparison operators.

### Equality Operator vs. Strict Equality Operator

There are two kinds of equality operators in JavaScript. The **equality operator** (`==` or `!=`) and the **strict equality operator** (`===` or `!==`). We will almost always use the strict equality operator.

**Equality operator** can be misleading since it doesn’t check the type of values that we are comparing. When using the equality operator, these two completely different values would appear to be the same:

```
1 console.log(10 == "10"); // true
```

This is extremely misleading. The numeric value `10` and the string value `"10"` are nothing alike. We will not get this result if we are to use the strict equality operator.

```
1 console.log(10 === "10"); // false
```

You should avoid using the equality operator like a plague and use the strict equality operator at all times. I can’t remember the last time that I have used the equality operator. If we wanted to check to see if a number matches the string’s value, there are other ways of going about it, like converting that number to a string or converting the string to a number (by using the `parseInt` function that we have learned about).

### Comparing Fractional Numbers

In the example below, you might expect `x` and `y` to be equivalent. They are not.

```
1 const x = 0.1 + 0.2;
2 const y = 0.3;
3 const z = x === y;
4 console.log(z); // false
```

Computers use a **binary number** system to represent the values that we throw at them. Basically, everything is represented as a `0` or `1`. This results in some loss of precision when the computer stores the results of **fractional** number operations. This causes issues such as above, where `0.1 + 0.2` is not equivalent to `0.3`. This is a very common issue to be aware of when working with fractional numbers. There are a couple of workarounds for this issue. One is to check to see if two numbers are equivalent in the range of some threshold. Let’s say the threshold for our error tolerance is `0.01` for the example above, which means that the numbers can slightly differ from each other but not more than `0.01`. Here is how we would represent this idea in code.

```
1 const threshold = 0.01;
2 
3 const x = 0.1 + 0.2;
4 const y = 0.3;
5 const z = Math.abs(x - y) < threshold;
6 console.log(z);
```

`Math.abs` is a function that converts the given input to an absolute value (meaning converts the given numeric value to a positive value). In the above example, we say that if the difference between two values is smaller than a threshold of our choice, then we accept that these two values are equivalent. They are not equivalent if their difference is greater than the threshold.

Another way of doing comparisons using fractional numbers would be to convert them to string and then compare. We haven’t learned how to convert a value to a string yet, so we will not explore that option here.

## Logical Operators

**Logical operators** allow us to build **compound statements** using more than one boolean value.

Imagine I told you that you would be happy if you took care of your health **AND** your finances. This means that you need to take care of both your health **and** finances to be happy. If you didn’t do either one of them, it is not going to work out. This is the logic behind the **AND** (`&&`) operator in JavaScript. It returns `true` if both sides of the operation are `true`.

```
 1 let isTrue = true && true;
 2 console.log(isTrue); // true
 3 
 4 isTrue = 10 === 10 && 10 !== 11;
 5 console.log(isTrue); // true
 6 
 7 let isFalse = true && false;
 8 console.log(isFalse); // false
 9 
10 isFalse = false && true;
11 console.log(isFalse); // false
12 
13 isFalse = false && false;
14 console.log(isFalse); // false
```

js-basics-04-flow-control/02.js

As we can see in the above example, both sides of the AND operator need to be `true` for the resulting operation to be `true`.

Now let’s imagine I told you that you would be healthier if you improved your diet **OR** you started to exercise more. This means that you just need to do one of those things to see an improvement in your health. This is how the OR (`||`) operator works in JavaScript. It returns `true` as long as one of the values that we are comparing is `true`.

```
1 let isTrue = true || false;
2 console.log(isTrue); // true
3 
4 isTrue = false || true;
5 console.log(isTrue); // true
6 
7 let isFalse = false || false;
8 console.log(isFalse); // false
```

js-basics-04-flow-control/03.js

## Conditional Statements

Boolean values might seem a bit useless on their own. They are great when used in conjunction with **conditional statements**. A conditional statement executes only if the given condition is `true`. It is skipped if the condition evaluates to `false`. This is very different from what we have been learning so far. Previously, the programs that we wrote were executed from top to bottom in a linear fashion. Using conditional statements, we can alter the flow of our program. We can skip or execute a certain part based on a condition.

An `if` statement is an example of a conditional statement. Here is how it works.

```
1 const myVariable = true;
2 
3 if (myVariable) {
4   console.log("This gets displayed only if `myVariable` is `true`");
5 }
```

js-basics-04-flow-control/04.js

An `if` statement consists of the `if` keyword, **a condition** written inside the parentheses next to it, and **a body statement** that is written inside **curly braces**. If the condition inside the parenthesis evaluates to `true` then the statement that is inside the curly braces gets executed. If not, it doesn’t. Try changing the value of `myVariable` to `false` to see what happens.

We can append an `else` statement after the `if` statement.

```
1 const myVariable = true;
2 
3 if (myVariable) {
4   console.log("This gets displayed only if `myVariable` is `true`");
5 } else {
6   console.log("This gets displayed if the `myVariable` is NOT `true`");
7 }
```

js-basics-04-flow-control/05.js

The `else` block of the conditional statement gets executed if the `if` statement doesn’t. That is if the given condition evaluates to `false`. This is called an `if-else` statement.

This is basically (very basically, that is) how a login screen works.

```
1 const password = "1234";
2 
3 if (password === "1234") {
4   console.log("Welcome user");
5 } else {
6   console.log("Login failed");
7 }
```

js-basics-04-flow-control/06.js

Conditional statements allow us to write extremely flexible programs because we can adjust our program’s behavior based on some external input. Here, in this example, we are entering the value of the `password` ourselves, but there are more advanced ways to construct programs where we can capture the user input or fetch data into our program from other external sources.

## else if Statement

There is also a statement called `else if` that we can use alongside `if` statements. It allows us to handle multiple conditions.

Here is a program that displays the grade of a student given their test score.

```
 1 const score = 59;
 2 
 3 if (score >= 90) {
 4   console.log("A");
 5 } else if (80 <= score && score < 90) {
 6   console.log("B");
 7 } else if (70 <= score && score < 80) {
 8   console.log("C");
 9 } else if (60 <= score && score < 70) {
10   console.log("D");
11 } else {
12   console.log("F");
13 }
```

js-basics-04-flow-control/07.js

Since this functionality can be useful on multiple occasions, we might want to wrap it inside a function for reusability.

```
 1 function getGrade(score) {
 2   let grade;
 3 
 4   if (score >= 90) {
 5     grade = "A";
 6   } else if (80 <= score && score < 90) {
 7     grade = "B";
 8   } else if (70 <= score && score < 80) {
 9     grade = "C";
10   } else if (60 <= score && score < 70) {
11     grade = "D";
12   } else {
13     grade = "F";
14   }
15 
16   return grade;
17 }
18 
19 let grade;
20 grade = getGrade(59);
21 console.log(grade);
22 
23 grade = getGrade(71);
24 console.log(grade);
25 
26 grade = getGrade(100);
27 console.log(grade);
```

js-basics-04-flow-control/08.js

`if` and `if-else` statements allow us to write very capable programs. We can adjust this function to handle invalid values to make it much more robust.

```
 1 function getGrade(score) {
 2   if (score < 0 || score > 100) {
 3     console.log("You have entered an invalid value");
 4     return;
 5   }
 6 
 7   let grade;
 8 
 9   if (score >= 90) {
10     grade = "A";
11   } else if (80 <= score && score < 90) {
12     grade = "B";
13   } else if (70 <= score && score < 80) {
14     grade = "C";
15   } else if (60 <= score && score < 70) {
16     grade = "D";
17   } else {
18     grade = "F";
19   }
20 
21   return grade;
22 }
23 
24 let grade;
25 grade = getGrade(59);
26 console.log(grade);
27 
28 grade = getGrade(71);
29 console.log(grade);
30 
31 grade = getGrade(100);
32 console.log(grade);
33 
34 grade = getGrade(-10);
35 console.log(grade);
```

js-basics-04-flow-control/09.js

We have updated our function to display an error message and not to return a value when provided a `score` value below `0` or above `100`. When we use the `return` statement without any value, JavaScript implicitly returns a value called `undefined`. An `undefined` is a built-in JavaScript value that represents the absence of a value.

We get the value `undefined` if we initialize a variable but don’t assign a value. Or if a function doesn’t return a value just like in our example.

```
1 let x;
2 console.log(x); // undefined
```

There is another value called `null` that is similar to `undefined`. Whereas `undefined` represents an **implicit absence of a value**, `null` represents the **explicit absence of a value**.

It is like the difference between saying “I don’t know what the value is” (implicit) versus “there is no value here” (explicit).

```
1 const x = null;
```

Learning about `null` and `undefined` values provide a great segue for us to learn about **truthy** and **falsy** values.

## Truthy and Falsy Values

We have learned that there are two Boolean values, `true` and `false`. There are also other values in JavaScript that are not Boolean but are considered to be **like** `true` or `false` when evaluated in a Boolean context. Think of the number `0`. It is not a Boolean value. But if we were to use it in a conditional context it would evaluate as `false` because it is **falsy**. This means it is f**alse-like** but not precisely `false`.

```
1 const myVariable = 0;
2 
3 if (myVariable) {
4   console.log("This would NOT get displayed since `myVariable` is `0`");
5 }
```

Any non-zero number is **truthy**. They are **true-like** but not exactly `true`.

```
1 const myVariable = 42;
2 
3 if (myVariable) {
4   console.log("This would get displayed since `myVariable` is not zero");
5 }
```

`null`, `undefined`, `0`, empty string (`""`), and `NaN` are examples of falsy values. Everything else is a truthy value.

## Logical Operators Revisited

Previously we have learned about **logical operators** and their behavior. We have seen that the `&&` operator returns `true` if both of the values that it operates on are `true` or it returns `false`. This is actually only true when we are using Boolean values. But we would notice that logical operators work differently when we provide other kinds of values.

```
1 const x = 42 && "hello world";
2 console.log(x); // displays "hello world"
```

Here is what’s happening. There is this concept called **short-circuit evaluation**. An **AND** operation (an operation that uses `&&`) will short-circuit if the first (left-hand side) value is falsy. This means that it would simply evaluate to that value without looking at the rest of the operation. Otherwise, it would evaluate to the second (right-hand side) value.

An **OR** operation (an operation that uses `||`) will short-circuit if the first value is truthy. Otherwise, it would evaluate to the second value.

Previously I have explained as if these operators would always result in a `true` or a `false` value. That is not entirely correct. They evaluate to one of the values that are being operated on, and their behavior is determined by short-circuit evaluation.

## Summary

In this section, we have first learned about the Boolean data types of `true` and `false`. Then we have learned about comparison operators, which would result in Boolean values. We learned about some of the things that we need to be aware of when making comparisons. Like:

*   Making sure to use the **strict equality operator**.
*   Not directly comparing floating point numbers.

In addition to Boolean data types, we have also learned about two new values. These are `null` and `undefined`. They are used the signify an absence of a value.

We have the values `true` and `false`, but we have also values that are **truthy** and **falsy.** These are values that are not precisely Boolean but can be thought of as such.

We have then learned about **logical operators** and the concept of **short-circuit evaluation**.

The most important thing that we have learned about in this chapter is the **conditional statements**. Using `if`, `else`, and `if else` we can build programs that are much more capable than before.

# 6 Project: Creating an Email Template

When I was looking for a job at the beginning of my career, I have made a spreadsheet of all the companies and positions I wanted to apply to and created a cover letter template to send out to these companies. Unfortunately, I didn’t know programming at the time, so this had to be done manually.

Performing repetitive tasks like this is a perfect candidate for automation and hence programming. Let’s look at how we might tackle a task like this with what we know so far. We will also learn a couple of new tricks along the way.

## Creating a Body Template

We will start with a cover letter text that will serve as a template. We will simplify the example greatly so that we are not drowning in redundant details. Our text can be something like this:

```
1 Dear Sir/Madam,
2 
3 I am writing to apply for the <position> position advertised in the <company>.
4 
5 Thank you for your time and consideration. I look forward to speaking with you
6 about this employment opportunity.
7 
8 Best,
9 John Doe
```

js-basics-05-project-email-template/01.txt

Obviously, this is not a complete cover letter but should be suitable for our purposes. As you can see, we have placed `<position>` and `<company>` in angled brackets. This is to signal that these parts of the text are going to be represented by variables.

Let’s put this text into a string and store it inside a variable. So far, we have learned to wrap strings using the single (`'`) or double (`"`) quotation mark. If we tried to wrap this given text inside a quotation mark, we would notice that it doesn’t work. We can’t have a multiline string wrapped in quotation marks. We will need to have the entire text in a single line.

```
1 const template =
2   "Dear Sir/Madam, I am writing to apply for the <position> position advertised in t\
3 he <company>. Thank you for your time and consideration. I look forward to speaking \
4 with you about this employment opportunity.Best, John Doe";
5 
6 console.log(template);
```

js-basics-05-project-email-template/02.js

This text would be so much easier to read and manage if your code editor has a way to wrap text around. I use **VS Code**, and there is a way to activate word-wrap under `View > Toggle Word Wrap`.

When we execute this code, we will notice that it is nothing like how we would like it to display. We have lost all the line breaks. To add a line break to a single string, we need to use a **newline character** (`\n`). Let’s update our code with this.

```
1 const template =
2   "Dear Sir/Madam,\n\nI am writing to apply for the <position> position advertised i\
3 n the <company>.\n\nThank you for your time and consideration. I look forward to spe\
4 aking with you about this employment opportunity.\n\nBest,\nJohn Doe";
5 
6 console.log(template);
```

js-basics-05-project-email-template/03.js

We have updated the string to include the line breaks. Now, if we are to execute this code, we would notice it looks so much better. Let’s start making use of variables to be able to customize this template.

```
 1 const position = "Software Engineer";
 2 const company = "NASA";
 3 
 4 const template =
 5   "Dear Sir/Madam,\n\nI am writing to apply for the " +
 6   position +
 7   " position advertised in the " +
 8   company +
 9   ".\n\nThank you for your time and consideration. I look forward to speaking with y\
10 ou about this employment opportunity.\n\nBest,\nJohn Doe";
11 
12 console.log(template);
```

js-basics-05-project-email-template/04.js

This is starting to work, but there are still some improvements that we can apply. First of all, notice how hard it was to construct this string. We had to use the newline character (`\n`) all around. Injecting those variables using math operators wasn’t straightforward either. There is another way of creating strings that elegantly solves both of these problems.

## Template Literals

A **template literal** is a string constructed using the **backtick** character (```). There are a couple of advantages to using template literals. Let’s change our string to use backtick character to see how this works in action.

```
 1 const position = "Software Engineer";
 2 const company = "NASA";
 3 
 4 const template =
 5   `Dear Sir/Madam,\n\nI am writing to apply for the ` +
 6   position +
 7   ` position advertised in the ` +
 8   company +
 9   `.\n\nThank you for your time and consideration. I look forward to speaking with y\
10 ou about this employment opportunity.\n\nBest,\nJohn Doe`;
11 
12 console.log(template);
```

js-basics-05-project-email-template/05.js

Here we didn’t make any changes except for using backticks to construct the string instead of quotation marks. We can actually use **placeholders** inside template literals. We can place `${}` character inside a template literal, which would allow us to embed JavaScript code inside the curly braces. This means that we can get rid of the addition operator and directly embed variables inside the string defined by the template literal.

```
1 const position = "Software Engineer";
2 const company = "NASA";
3 
4 const template = `Dear Sir/Madam,\n\nI am writing to apply for the ${position} posit\
5 ion advertised in the ${company}.\n\nThank you for your time and consideration. I lo\
6 ok forward to speaking with you about this employment opportunity.\n\nBest,\nJohn Do\
7 e`;
8 
9 console.log(template);
```

js-basics-05-project-email-template/06.js

See how much more readable our code is right now. We don’t have those addition operators that break the flow of the code. It is so much easier to have strings that have variables inside when using template literals.

Template literals allow for multiline strings as well. So we can get rid of those newline (`\n`) characters too.

```
 1 const position = "Software Engineer";
 2 const company = "NASA";
 3 
 4 const template = `Dear Sir/Madam,
 5 
 6 I am writing to apply for the ${position} position advertised in the ${company}.
 7 
 8 Thank you for your time and consideration. I look forward to speaking with you about\
 9  this employment opportunity.
10 
11 Best,
12 John Doe`;
13 
14 console.log(template);
```

js-basics-05-project-email-template/07.js

Isn’t this amazing? Our code now looks just like what is intended with the output. This is what highly expressive code allows us to do. It removes the barriers between the code and the idea that it expresses. This looks so much better than our previous iterations.

It seems like template literals are amazing, isn’t it? You might be wondering if there could be a reason not to use them all the time. Honestly, I am not quite sure. One of the arguments against them could be that they were introduced somewhat recently to the JavaScript language. This means that not all environments might have support for it. There might also be performance implications to using template literals since they are much more overloaded than standard strings in terms of functionality. I am not too sure if it would make sense to worry about the performance argument. It would probably be negligible. Having said that, I have never worked on a codebase where template literals were the default way of writing strings. Maybe this will change in a few years.

Let’s wrap our code in a function to make it tidier.

```
 1 function createCoverLetter(position, company) {
 2   const template = `Dear Sir/Madam,
 3   
 4 I am writing to apply for the ${position} position advertised in the ${company}.
 5 
 6 Thank you for your time and consideration. I look forward to speaking with you about\
 7  this employment opportunity.
 8 
 9 Best,
10 John Doe`;
11 
12   console.log(template);
13   return template;
14 }
15 
16 let position = "Software Engineer";
17 let company = "NASA";
18 
19 createCoverLetter(position, company);
```

js-basics-05-project-email-template/08.js

Sometimes we have a name for the contact person at the company. If that is the case, we can replace the `Dear Sir/Madam,` text with something more personal. We can use a conditional statement since we would like this switch to occur only when the contact person data is available.

```
 1 function createCoverLetter(position, company, contactName) {
 2   let contact;
 3   if (contactName) {
 4     contact = contactName;
 5   } else {
 6     contact = "Sir/Madam";
 7   }
 8 
 9   const template = `Dear ${contact},
10     
11 I am writing to apply for the ${position} position advertised in the ${company}.
12 
13 Thank you for your time and consideration. I look forward to speaking with you about\
14  this employment opportunity.
15 
16 Best,
17 John Doe`;
18 
19   console.log(template);
20   return template;
21 }
22 
23 let position = "Software Engineer";
24 let company = "NASA";
25 let contact = "Jane Doe";
26 
27 createCoverLetter(position, company, contact);
```

js-basics-05-project-email-template/09.js

We have implemented a logic to check to see if there is any argument provided for `contactName`. If there is, we use that argument inside the template literal. If not, we use `Sir/Madam` instead.

Since writing a conditional that selects in between two values based on a given condition is so common, JavaScript has a shorthand way of writing those conditionals. It looks like this:

```
1 const x = someCondition ? "results in this value if true" : "this if false";
```

Here is how this would look like in the above example:

```
1 const contact = contactName ? contactName : "Sir/Madam";
```

This expression means that if the variable `contactName` is **truthy** we will use the value on the left-hand side of `:` symbol. If it is **falsy**, we will use the value on the right-hand side. `?` character in this context called a **ternary operator** since it takes 3 inputs.

We can make this expression even shorter by using logical operators.

```
1 const contact = contactName || "Sir/Madam";
```

This expression would short-circuit and evaluate to `contactName` if the `contactName` is **truthy**. Let’s update our code with this logic.

```
 1 function createCoverLetter(position, company, contactName) {
 2   const contact = contactName || "Sir/Madam";
 3 
 4   const template = `Dear ${contact},
 5       
 6 I am writing to apply for the ${position} position advertised in the ${company}.
 7 
 8 Thank you for your time and consideration. I look forward to speaking with you about\
 9  this employment opportunity.
10 
11 Best,
12 John Doe`;
13 
14   console.log(template);
15   return template;
16 }
17 
18 let position = "Software Engineer";
19 let company = "NASA";
20 let contact = "Jane Doe";
21 
22 createCoverLetter(position, company, contact);
```

js-basics-05-project-email-template/10.js

We would notice that if we don’t pass the `contact` argument inside the function, the body template will use the `Sir/Madam` text. There is a concept called **default parameters** that can be useful here. Basically, we can provide some default values for the parameters of a function so that they would use that value if the caller of the function does not provide an argument. It works like this.

```
 1 function createCoverLetter(position, company, contact = "Sir/Madam") {
 2   const template = `Dear ${contact},
 3         
 4 I am writing to apply for the ${position} position advertised in the ${company}.
 5 
 6 Thank you for your time and consideration. I look forward to speaking with you about\
 7  this employment opportunity.
 8 
 9 Best,
10 John Doe`;
11 
12   console.log(template);
13   return template;
14 }
15 
16 let position = "Software Engineer";
17 let company = "NASA";
18 let contact = "Jane Doe";
19 
20 createCoverLetter(position, company, contact);
```

js-basics-05-project-email-template/11.js

We can define a default parameter by using the assignment (`=`) operator. Here the `contact` parameter has a default value of `Sir/Madam`. If a value is not provided, then the function would use that value instead. This makes our code so much shorter.

Our program is currently in a pretty good spot. We can make it much more capable if we wanted to by introducing some extra logic based on the position we are applying to. For example, we can add a conditional logic that would add a paragraph to our cover letter if the position we are applying to is `Software Engineer` or a `Lawyer`.

```
 1 function createCoverLetter(position, company, contact = "Sir/Madam") {
 2   let details = "";
 3 
 4   if (position === "Software Engineer") {
 5     details = "\nI love software engineering. It is the best.\n";
 6   } else if (position === "Lawyer") {
 7     details = "\nI have always wanted to be a lawyer. It is my passion.\n";
 8   }
 9 
10   const template = `Dear ${contact},
11           
12 I am writing to apply for the ${position} position advertised in the ${company}.
13   ${details}
14 Thank you for your time and consideration. I look forward to speaking with you about\
15  this employment opportunity.
16   
17 Best,
18 John Doe`;
19 
20   console.log(template);
21   return template;
22 }
23 
24 let position = "Software Engineer";
25 let company = "NASA";
26 let contact = "Jane Doe";
27 
28 createCoverLetter(position, company, contact);
```

js-basics-05-project-email-template/12.js

## Summary

In this chapter, we have seen how programming can be applied to a practical problem. We are at the beginning of our journey, so things that we can do with our programming knowledge are relatively limited. But even then, we were able to create a function that has the potential to save us a lot of time.

In this chapter, we have also learned to create **template literals** by using the **backtick** character. Template literals are a way to construct strings that can embedded variables. We have also learned about the **ternary operators**. A ternary operator (`?`) is a shorthand way of writing conditions that has two outcomes.

Finally, we have learned about **default parameters** for functions which makes it easy to assign a default parameter to a function if the caller of the function does not provide a value.

# 7 JavaScript Objects

Up until this point, we have learned about data types such as **numbers**, **strings**, and **booleans**. We have also learned about a couple of different other built-in values like `undefined` and `null`. It is time to learn a new data type called **objects**.

An **object** in Javascript is a data type that helps to organize other data together. We can create an object by using **curly braces**.

```
1 const x = {};
```

This code above creates an empty object. We can now populate this object with values. A value is stored as a **property** of the object. Say, we want this object to have a **property** called `name` that will have the **value** `John`. Here is how we do that:

```
1 const x = {};
2 x.name = "John";
3 console.log(x);
```

This way of working with the properties on an object using a **dot** (`.`) is called **dot notation**.

If we are to `console.log` this object, we would see that it has a property called `name` that has the value `"John"`. Let’s add another property to this object called `lastName`.

```
1 x.lastName = "Doe";
```

As we can see, we can keep adding new properties and values to this object. This object that we are creating represents data about a person given it has properties called `name` and `lastName`. Since this object represents a person, we should probably find a better variable name than `x`. Let’s rewrite our example with a proper variable and property names.

```
1 const person = {
2   firstName: "John",
3   lastName: "Doe",
4 };
```

js-basics-06-objects/01.js

This rewrite is much better. As we can see in this example, we can also populate an object at **initialization**.

We can use the dot notation to access the values that are stored on objects. If we wanted to get the value of `firstName` on the `person` object. We can do this:

```
1 console.log(person.firstName);
```

And this would display the value of the `firstName` property.

We can use the dot notation to assign a different value to a property as well.

```
1 person.firstName = "Jane";
```

We can also have functions as properties on an object. Here is how to do it.

```
 1 function hello() {
 2   console.log("Hello");
 3 }
 4 
 5 const person = {
 6   firstName: "John",
 7   lastName: "Doe",
 8   sayHello: hello,
 9 };
10 
11 person.sayHello();
```

js-basics-06-objects/02.js

Alternatively we can define the function property at object initialization as well.

```
1 const person = {
2   firstName: "John",
3   lastName: "Doe",
4   sayHello: function hello() {
5     console.log("Hello");
6   },
7 };
8 
9 person.sayHello();
```

js-basics-06-objects/03.js

Function properties of objects are called **methods**. `sayHello` is a **method** of the `person` object. An **object** is made up of **properties** and **methods**.

Now that we have learned about objects and the dot notation, the dot symbol inside the `console.log` function should make more sense. `log` is a method of the `console` object. If we are to `console.log` the `console` object, we would see that it has many other methods.

```
1 console.log(console);
```

When defining object properties, we can use the **shorthand notation** if we have a variable with the same name as an object property. Here is how it works:

```
 1 const firstName = "John";
 2 const lastName = "Doe";
 3 
 4 const person = {
 5   firstName,
 6   lastName,
 7   sayHello: function hello() {
 8     console.log("Hello");
 9   },
10 };
11 
12 person.sayHello();
```

js-basics-06-objects/03_05.js

We have used the shorthand notation when defining the `firstName` and the `lastName`. We simply wrote the variable name, and the object accepted it as the value since it has the same name as the property name. This saves us some time when we are defining objects.

We can delete a property from an object by using the `delete` keyword.

```
1 delete person.lastName;
2 console.log(person);
```

An object can store any value, even other objects!

```
 1 const person = {
 2   firstName: "John",
 3   lastName: "Doe",
 4   sayHello: function hello() {
 5     console.log("Hello");
 6   },
 7   age: 42,
 8   isAlive: true,
 9   workInformation: {
10     companyName: "NASA",
11     position: "Software Engineer",
12   },
13   children: null,
14 };
15 
16 console.log(person);
```

js-basics-06-objects/03_01.js

We can also use square brackets (`[]`) to work with the properties and methods of objects. Here is how it works.

```
1 const person = {};
2 person["firstName"] = "John";
3 console.log(person["firstName"]);
```

js-basics-06-objects/03_02.js

The dot notation is easier to use but square brackets has some advantages over the dot notation.

Using square brackets, we can have numbers as property and method names. This is not possible to do while using dot notation.

```
1 const x = {};
2 x[42] = "Answer to everything";
3 console.log(x[42]);
```

js-basics-06-objects/03_03.js

Using square brackets we can also use variables as object keys.

```
1 const x = {};
2 const key = 42;
3 x[key] = "Answer to everything";
4 console.log(x[key]);
```

js-basics-06-objects/03_04.js

This is a very useful feature to have when we are **programmatically** creating an object.

## this Keyword

Let’s take a look at this example again, where calling the `sayHello` method on the person object displays the word `Hello` to the screen.

```
1 const person = {
2   firstName: "John",
3   lastName: "Doe",
4   sayHello: function hello() {
5     console.log("Hello");
6   },
7 };
8 
9 person.sayHello();
```

js-basics-06-objects/03.js

What if we wanted to have the `sayHello` method to make use of a stored value on the `person` object? For example, wouldn’t it be great if calling the `sayHello` method on this `person` object displayed `Hello, my name is John Doe` to the screen? We could try to solve this issue by **hardcoding** the `firstName` and `lastName` values inside the `sayHello` function.

```
 1 {
 2   const person = {
 3     firstName: "John",
 4     lastName: "Doe",
 5     sayHello: function hello() {
 6       console.log(`Hello, my name is John Doe`);
 7     },
 8   };
 9 
10   person.sayHello();
11 }
```

js-basics-06-objects/04.js

This wouldn’t work great since we might want to update the values for `firstName` or the `lastName` properties later, but then the `sayHello` wouldn’t get updated with this change.

```
1 person.firstName = "Jane";
2 person.sayHello(); // would display `Hello, my name is John Doe`
```

We can address this issue by making use of the `this` keyword. `this` keyword allows the object to refer to itself.

```
 1 const person = {
 2   firstName: "John",
 3   lastName: "Doe",
 4   sayHello: function hello() {
 5     console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
 6   },
 7 };
 8 
 9 person.sayHello();
10 
11 person.firstName = "Jane";
12 person.sayHello();
```

js-basics-06-objects/05.js

As we can see in this example, `this.firstName` refers to the `firstName` property that is on the `person` object.

We have been assigning a function with the name `hello` to the `sayHello` method, but that function does not actually have to have a name since it will be accessed through the method name. We could simply use an **anonymous function** in there.

```
 1 const person = {
 2   firstName: "John",
 3   lastName: "Doe",
 4   sayHello: function () {
 5     console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
 6   },
 7 };
 8 
 9 person.sayHello();
10 
11 person.firstName = "Jane";
12 person.sayHello();
```

js-basics-06-objects/05_01.js

But keep in mind that we shouldn’t use an **arrow function** when defining methods. Arrow functions have a different behavior around the `this` keyword, making them unsuitable to be used in this context. Take a look at the result we get when we use an arrow function instead of a normal function definition for the `sayHello` method.

```
 1 const person = {
 2   firstName: "John",
 3   lastName: "Doe",
 4   sayHello: () => {
 5     console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
 6   },
 7 };
 8 
 9 person.sayHello(); // Hello, my name is undefined undefined
10 
11 person.firstName = "Jane";
12 person.sayHello(); // Hello, my name is undefined undefined
```

js-basics-06-objects/05_02.js

`this` keyword does not refer to the object itself anymore when used inside an arrow function.

Objects help us with code organization. We now have an object representing a concept (a person) with all the properties and methods related to that object in a single spot. An alternative to this approach would have looked like this:

```
1 const firstName = "John";
2 const lastName = "Doe";
3 
4 function sayHello(firstName, lastName) {
5   console.log(`Hello, my name is ${firstName} ${lastName}`);
6 }
7 
8 sayHello(firstName, lastName);
```

js-basics-06-objects/06.js

This code does the same thing but it feels a bit less organized. `sayHello` function is clearly built to be used with a first name and a last name but it is not structurally tied to those concepts. Objects help us to resolve that issue.

## Passed by Value vs. Passed by Reference

An important concept about objects is regarding how they are stored in the computer memory.

All the data types that we have learned before this section are **passed by value**. This means that a new copy of the value is created when they are assigned into a variable.

```
1 let x = 42;
2 let y;
3 
4 y = x;
5 x = 7;
6 
7 console.log(x);
8 console.log(y);
```

js-basics-06-objects/07.js

What do you think will get displayed on the screen? If you have guessed `7` and `42`, you are correct.

Let’s take a look at a similar example with objects to see what happens in that case.

```
1 let x = { number: 42 };
2 let y;
3 
4 y = x;
5 x.number = 7;
6 
7 console.log(x);
8 console.log(y);
```

js-basics-06-objects/08.js

We would see that both `x` and `y` display the same value when we `console.log`.

Objects are **passed by reference**. When we assign the value of `x` to the variable `y`, we don’t create a new copy of `x`. `x` and `y` start referring to the same object in the computer memory. This is why the value of the variable `y` changes when we change the `number` property of `x`.

This is a critical behavior to keep in mind. Thinking that we are creating an entirely new copy of an object while we are just creating a reference is a common source of bugs.

There are cases when we might want to create a copy of an object. We can use the **spread** operator to do that. **Spread** operator (`...`) allows us to copy an object to a new value.

```
1 let x = { number: 42 };
2 let y;
3 
4 y = { ...x };
5 x.number = 7;
6 
7 console.log(x);
8 console.log(y);
```

js-basics-06-objects/09.js

We still need to be careful, though, because creating a copy using the spread operator would not create a copy of the deeper objects that might be nested in the object.

```
 1 const person = {
 2   firstName: "John",
 3   lastName: "Doe",
 4   sayHello: function hello() {
 5     console.log("Hello");
 6   },
 7   age: 42,
 8   isAlive: true,
 9   workInformation: {
10     companyName: "NASA",
11     position: "Software Engineer",
12   },
13   children: null,
14 };
15 
16 const anotherPerson = { ...person };
17 
18 anotherPerson.firstName = "Jane";
19 anotherPerson.workInformation.companyName = "SpaceX";
20 
21 console.log(person.firstName);
22 console.log(person.workInformation.companyName);
```

js-basics-06-objects/10.js

In this example, we have a `person` object. We are then creating a copy of the `person` object by using the spread operator. This copy has a different name and works at a different company. Then we are checking to see what happened with the original `person` data. The person’s `firstName` is still the same, but the `workInformation` had **mutated** when we changed it for `anotherPerson`. That is because the spread operation doesn’t create a **deep copy.** It only creates a **shallow copy**.

If we wanted to create a **deep copy** or a **deep clone** of a JavaScript object, then we might want to use external **programming libraries** created for that purpose. We will learn about programming libraries at a later time.

## Factory Functions, Constructor Functions, and Classes

In the previous examples, we have been creating an object to hold values that describe a person. Having data structures that represent some real or abstract concept is very common in programming. A financial application might have to represent the concept of money, a transaction, or a wallet. An e-commerce application can have representations for a cart, store, or product. An HR application might have to represent the concept of a person, just like we are doing here.

As we have seen in the example, we could easily create an object that holds the data representing a person. We had some issues when we wanted to create another object for a different person. If we wanted to create many instances of an object easily, we need to learn about **factory functions, constructor functions,** and **classes.** They are all different ways of creating an object template that can be used to create multiple instances of an object.

### Factory Functions

A **factory function** is essentially a function that **returns** an **object**. We can use such a function as a way to create multiple instances of an object. Here is an example:

```
 1 function getPerson(firstName, lastName) {
 2   return {
 3     firstName,
 4     lastName,
 5     sayHello: function () {
 6       console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
 7     },
 8   };
 9 }
10 
11 const personA = getPerson("John", "Doe");
12 const personB = getPerson("Jane", "Doe");
13 
14 personA.sayHello();
15 personB.sayHello();
```

js-basics-06-objects/11.js

Here, `getPerson` is a **factory function** since it allows us to create multiple instances of an object. There is nothing really special about a factory function. It is just a simple function that provides us with a way to create multiple instances of the same object.

There are some other methods for creating an object template. We won’t be using them in this book since factory functions are good enough for our use cases. However, it is still useful to learn about them since we might come across their usage when looking at different codebases. Those other methods are **constructor functions** and **classes.**

### Constructor Functions

A **constructor function** is a function that acts as a template for creating multiple instances of a same object. Let’s take a look at an example:

```
 1 function Person(firstName, lastName) {
 2   this.firstName = firstName;
 3   this.lastName = lastName;
 4   this.sayHello = function () {
 5     console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
 6   };
 7 }
 8 
 9 const personA = new Person("John", "Doe");
10 const personB = new Person("Jane", "Doe");
11 
12 personA.sayHello();
13 personB.sayHello();
```

js-basics-06-objects/12.js

In this example, `Person` is a **constructor function**. It defines a template for a person object. We then create instances of that object by calling this constructor function with the `new` keyword. A constructor function is just like a normal function but there are a couple of things that set it apart.

Constructor functions are defined with a **title case name** (`Person` instead of `person`). This is a hint that this function is a constructor function and should be called with the `new` keyword. If we don’t call a constructor function with the `new` keyword, `this` keyword won’t point to the object we have created. It simply won’t work as expected.

I have rarely had to define any constructor functions, but they are good to know because we might have to use constructor functions defined by others. We have to remember to call them with the `new` keyword.

### Classes

Another way of creating an object template in JavaScript is by using **classes**. A **class** is a special function that provides a different syntax for defining object templates. Here is how the above example can be written as a **class**.

```
 1 class Person {
 2   constructor(firstName, lastName) {
 3     this.firstName = firstName;
 4     this.lastName = lastName;
 5   }
 6 
 7   sayHello = function () {
 8     console.log(`Hello, my name is ${this.firstName} ${this.lastName}`);
 9   };
10 }
11 
12 const personA = new Person("John", "Doe");
13 const personB = new Person("Jane", "Doe");
14 
15 personA.sayHello();
16 personB.sayHello();
```

js-basics-06-objects/13.js

Unlike constructor functions**,** classes are a pretty common concept that exists in many other programming languages. JavaScript initially didn’t have any support for classes. It was added to the language at a later stage. The classes in JavaScript and other languages have some fundamental differences, but we won’t spend too much time with either classes or with constructor functions so that discussion is beyond the concerns of this book.

## Summary

An **object** is a data type that allows us to organize other data together. Objects have **properties** and **methods**. We can think of properties as defining a **value** on the object, whereas methods define the object’s **behaviors**. We can use the **dot notation** or the **square bracket notation** when working with objects. Using **dot notation** makes it easier to type but doesn’t work when we want to use numbers or variables as property or method names.

We can use the `this` keyword to refer to the object itself. Remember **not** to use **arrow functions** when defining methods since they don’t work well with the `this` keyword.

One fundamental concept to be aware of when working with objects is how they are passed around. Objects are **passed by reference,** whereas other data types that we have seen so far, like numbers or strings, are **passed by value**. This has implications on assigning objects to variables. If we want to create a new copy of an object when assigning it to a variable, we should be using the **spread operator**. It is important to remember that the spread operator only creates a **shallow copy** of the object.

Finally, we have looked into creating an object template that we can use to create multiple objects (**object instances**) easily. We have learned about **factory functions, constructor functions,** and **classes** used for this purpose.

# 8 Arrays

It is a common requirement in programming languages to have a data structure that will be a container for other kinds of data. This is what **arrays** allow us to do. They are a container and collection of data. We can create arrays by using square brackets (`[]`). We can either create an empty array and populate it afterward or create it pre-populated with values. Here are some array examples:

```
 1 const emptyArray = [];
 2 const myFavoriteFood = ["pizza", "sushi", "steak"];
 3 const myFavoriteNumbers = [3, 7, 19, 42];
 4 const myFavoritePeople = [
 5   {
 6     name: "John Doe",
 7   },
 8   { name: "Jane Doe" },
 9 ];
10 const myFavoriteRandomThings = [42, "pizza", myFavoritePeople];
```

js-basics-07-arrays/01.js

As we can see in the examples, an **array** can have any number of values, and they can be of any type. We separate different values in an array by using commas (`,`).

Arrays are **ordered** collection of data. This means that the position of the items in an array is stored and retained. We can access the items in an array by using the **square bracket notation** and a number that points to the position (**index**) of the item we are accessing.

```
1 const myFavoriteFood = ["pizza", "sushi", "steak"];
2 console.log(myFavoriteFood[1]);
```

js-basics-07-arrays/02.js

Which item do you think the above example is going to display? You might intuitively guess that it is going to be `pizza`, but that is not correct. It would display `sushi`. Arrays are **zero-indexed**. The first position of an array is at index `0`.

```
1 const myFavoriteFood = ["pizza", "sushi", "steak"];
2 
3 console.log(myFavoriteFood[0] === "pizza");
4 console.log(myFavoriteFood[1] === "sushi");
5 console.log(myFavoriteFood[2] === "steak");
6 console.log(myFavoriteFood[3] === undefined);
```

js-basics-07-arrays/03.js

We would get an `undefined` value if we try to access an index of an array that doesn’t exist.

Using the **square bracket notation** we can also assign a new value to the given index of an array.

```
1 const myFavoriteFood = ["pizza", "sushi", "steak"];
2 
3 console.log(myFavoriteFood[0] === "pizza");
4 console.log(myFavoriteFood[1] === "sushi");
5 console.log(myFavoriteFood[2] === "steak");
6 
7 myFavoriteFood[0] = "tacos";
8 
9 console.log(myFavoriteFood);
```

js-basics-07-arrays/04.js

## Arrays are Objects

Arrays are a **subset** of JavaScript **objects**. They have object-like behavior but are specialized to deal with collections of data.

Since arrays are objects, they have built-in methods and properties that we can use. If we wanted to add new items to an array, we would use the `push` method.

```
1 const myFavoriteFood = ["pizza", "sushi", "steak"];
2 
3 myFavoriteFood.push("tacos");
4 
5 console.log(myFavoriteFood);
```

js-basics-07-arrays/05.js

`push` allows us to add new values to the end of an array. There is also a `pop` method that allows us to remove an item from the end of an array.

```
1 const myFavoriteFood = ["pizza", "sushi", "steak"];
2 
3 myFavoriteFood.pop();
4 
5 console.log(myFavoriteFood);
```

js-basics-07-arrays/06.js

We frequently need to know how many items an array contains. We can use the `length` property of an array to get that information.

```
1 const myFavoriteFood = ["pizza", "sushi", "steak"];
2 
3 console.log(myFavoriteFood.length);
```

js-basics-07-arrays/07.js

Arrays have other methods and properties. We will learn about those other methods and properties when we actually need them.

## Passed by Value vs Passed by Reference

We previously learned the difference between how different data types are passed around inside the program. Strings, numbers, and boolean values are **passed by value**. That means a new copy of them is created when they are assigned to a new variable.

```
1 const num = 42;
2 const newNum = num; // a copy of num gets created
```

This is not the case with **objects**. This is not the case with arrays either since arrays are a subset of objects too. Both objects and hence arrays are **passed by reference**.

```
1 let x = [42];
2 let y;
3 
4 y = x;
5 x.push(7);
6 
7 console.log(x);
8 console.log(y);
```

js-basics-07-arrays/08.js

In this example, `x` and `y` would end up having the same values. The workaround for this issue is similar to how it is for objects. We need to use the **spread** operator (`...`) to create a copy of the array when assigning it to a different variable.

```
1 let x = [42];
2 let y;
3 
4 y = [...x];
5 x.push(7);
6 
7 console.log(x);
8 console.log(y);
```

js-basics-07-arrays/09.js

Remember, just like in objects, the spread operator when used for arrays creates a **shallow** copy.

## Strings as Collections

Arrays are collections of data. Strings are similar to arrays in the sense that they are collections of individual characters. This means that we can also use some of the array methods on strings as well.

```
1 const name = "John Doe";
2 
3 const firstLetter = name[0];
4 console.log(firstLetter);
5 
6 const nameLength = name.length;
7 console.log(nameLength);
```

js-basics-07-arrays/10.js

However, we **can’t** assign a new value to a character of a string. This operation below would not work on strings.

```
1 const name = "John Doe";
2 
3 name[0] = "B";
4 
5 console.log(name);
```

js-basics-07-arrays/11.js

This is because strings are **immutable**. We can’t change a string after it is created. If we want to update a string, we need to create a new copy of it. But we can change objects or arrays after we create them.

## Example: Building a Password Validator

Let’s bring everything that we have learned in this chapter together. We will write a password validator to check to see if a given string is suitable to be used as a password. The password requirements we are going to have is going be as follows:

*   Longer than 8 characters.
*   Shorter than 12 characters.
*   It needs to end with the character `Z`.

If the password is valid it should return `true`. If not, it should return `false`.

Clearly, these are some absurd requirements, but they will work well for our learning purposes. Let’s start by creating the skeleton for our function.

```
1 function passwordValidator(password) {}
2 
3 const myPassword = "";
4 console.log(passwordValidator(myPassword));
```

js-basics-07-arrays/12.js

We are getting `undefined` when we execute this function since we are not **returning** anything from it yet.

Before we implement the first function, we will write a statement regarding our expectations from this function. We want it so that any password that is shorter than 8 characters is going to result in a `false` value, or else it would result in a `true` value.

```
1 function passwordValidator(password) {}
2 
3 let myPassword = "1234"; // shorter than 8 characters
4 let result = passwordValidator(myPassword) === false;
5 console.log(result);
6 
7 myPassword = "1234567Z"; // 8 characters.
8 result = passwordValidator(myPassword) === true;
9 console.log(result);
```

js-basics-07-arrays/13.js

In short, we want both of the `console.log` statements in this code to display `true` after we are done implementing the first requirement. Let’s do that.

```
 1 function passwordValidator(password) {
 2   if (password.length < 8) {
 3     return false;
 4   }
 5 
 6   return true;
 7 }
 8 
 9 let myPassword = "1234"; // shorter than 8 characters
10 let result = passwordValidator(myPassword) === false;
11 console.log(result);
12 
13 myPassword = "1234567Z"; // 8 characters.
14 result = passwordValidator(myPassword) === true;
15 console.log(result);
```

js-basics-07-arrays/14.js

We can verify that our code is working since both of the `console.log` statements are displaying true.

Let’s continue with a similar workflow, where we first write down what we expect to see and then implement the code that is going to satisfy that expectation.

```
 1 function passwordValidator(password) {
 2   if (password.length < 8) {
 3     return false;
 4   }
 5 
 6   return true;
 7 }
 8 
 9 let myPassword = "1234"; // shorter than 8 characters
10 let result = passwordValidator(myPassword) === false;
11 console.log(result);
12 
13 myPassword = "1234567Z"; // 8 characters.
14 result = passwordValidator(myPassword) === true;
15 console.log(result);
16 
17 myPassword = "1234567890101"; // longer than 12 characters
18 result = passwordValidator(myPassword) === false;
19 console.log(result);
```

js-basics-07-arrays/15.js

The last condition should display `true` after we implement the second requirement.

```
 1 function passwordValidator(password) {
 2   if (password.length < 8) {
 3     return false;
 4   }
 5 
 6   if (password.length > 12) {
 7     return false;
 8   }
 9 
10   return true;
11 }
12 
13 let myPassword = "1234"; // shorter than 8 characters
14 let result = passwordValidator(myPassword) === false;
15 console.log(result);
16 
17 myPassword = "1234567Z"; // 8 characters.
18 result = passwordValidator(myPassword) === true;
19 console.log(result);
20 
21 myPassword = "1234567890101"; // longer than 12 characters
22 result = passwordValidator(myPassword) === false;
23 console.log(result);
```

js-basics-07-arrays/16.js

Let’s implement the last requirement by following the same methodology. First, we will write down a statement about the expectation from the implementation.

```
 1 function passwordValidator(password) {
 2   if (password.length < 8) {
 3     return false;
 4   }
 5 
 6   if (password.length > 12) {
 7     return false;
 8   }
 9 
10   return true;
11 }
12 
13 let myPassword = "1234"; // shorter than 8 characters
14 let result = passwordValidator(myPassword) === false;
15 console.log(result);
16 
17 myPassword = "1234567Z"; // 8 characters.
18 result = passwordValidator(myPassword) === true;
19 console.log(result);
20 
21 myPassword = "1234567890101"; // longer than 12 characters
22 result = passwordValidator(myPassword) === false;
23 console.log(result);
24 
25 myPassword = "123456789"; // does not have the 'Z' character at the end.
26 result = passwordValidator(myPassword) === false;
27 console.log(result);
```

js-basics-07-arrays/17.js

And then we will handle the implementation of the requirement.

```
 1 function passwordValidator(password) {
 2   const passwordLength = password.length;
 3 
 4   if (passwordLength < 8) {
 5     return false;
 6   }
 7 
 8   if (passwordLength > 12) {
 9     return false;
10   }
11 
12   const lastCharacterIndex = passwordLength - 1;
13   const lastCharacter = password[lastCharacterIndex];
14 
15   if (lastCharacter !== "Z") {
16     return false;
17   }
18 
19   return true;
20 }
21 
22 let myPassword = "1234"; // shorter than 8 characters
23 let result = passwordValidator(myPassword) === false;
24 console.log(result);
25 
26 myPassword = "1234567Z"; // 8 characters.
27 result = passwordValidator(myPassword) === true;
28 console.log(result);
29 
30 myPassword = "1234567890101"; // longer than 12 characters
31 result = passwordValidator(myPassword) === false;
32 console.log(result);
33 
34 myPassword = "123456789"; // does not have the 'Z' character at the end.
35 result = passwordValidator(myPassword) === false;
36 console.log(result);
```

js-basics-07-arrays/18.js

We first created a variable called `passwordLength` to hold the password’s length since it is being used in multiple places. Then, we are getting the index for the string’s last character by subtracting one from this value. If a string is `8` characters long, then the last character would be index `7` since positions are **zero-indexed**.

```
1 const lastCharacterIndex = passwordLength - 1;
```

This operation gives us the last index position, and we can use this value to get the last character. We can then check to see if the last character is of the desired value. If so, we return `true` if not, and we return `false`.

We could have certainly written this code without having to write all those assertions about expected values. But then, we would still need to test the code against some password values to see if it works as expected. This way of working, where we first assert what we expect and then write the feature that would satisfy that assertion, is an example of **Test-Driven Development.** It is a commonly used software development methodology that results in code that is well tested and less susceptible to bugs.

## Summary

In this chapter, we have learned about **arrays**. Arrays are ordered collections of data. We can use them to store other types of data, including other arrays. Arrays are a subset of **objects**. They have methods that we can use to manipulate the array, like `push` or `pop`, and properties such as `length`. Since arrays are objects, they are also passed by **reference,** so we should be careful when creating copies of arrays. We have also learned that **strings** are similar to arrays because they are also collections of items (characters).

We have also seen a simple example of **Test-Driven Development (TDD)**. TDD is a programming methodology that is very frequently used in software development to develop applications that are less susceptible to bugs.

# 9 Loops

One of the things that computer programs really excel at is repetition. We can easily write a program that would make a computer perform a given operation hundreds or billions of times with a change of a single number. This is one of the things that makes programming so powerful. Once we have an operation that successfully works on one value, it is fairly easy to scale that operation to work on thousands or even millions of values. A **loop** is a programming structure that allows us to perform these kinds of repeating, iterative operations. There are a bunch of ways to write loops. Newer ways of creating loops have been introduced to JavaScript with the language’s development over the years. One of the most foundational ways of creating a loop is by using a `while` loop.

## while Loop

A `while` loop is a loop that works indefinitely as long as the condition that enables the loop is satisfied. Here is an example of a `while` loop. Beware that this is an infinite loop. It would run continuously until we somehow terminate the program.

```
1 let x = 0;
2 
3 while (x < 10) {
4   console.log("This is an infinite loop.");
5 }
```

js-basics-08-loops/01.js

We start with the keyword `while`. We then write a condition next to the `while` keyword inside the parenthesis. This loop will run **while** this condition is `true`. We then write the logic that we want to execute inside the loop by using **curly brackets**. In this example, `x` is always going to be smaller than `10`. This means that the loop will always run. This is an infinite loop.

Infinite loops have their uses, but we usually want to have loops that execute a limited amount of times. We can achieve this using a `while` loop as well. We just need to ensure that the condition that makes the loop run evaluates to `false` after a while.

Here is an example of a `while` loop that runs 10 times.

```
1 let x = 0;
2 
3 while (x < 10) {
4   console.log(x);
5   x = x + 1;
6 }
```

js-basics-08-loops/02.js

What is different with this loop is that the value of `x` does not stay the same. We increase the value of `x` by `1` every time this loop runs. `x = x + 1` means, take the current value of `x`, add `1` to it and assign the new value to be the current value of `x`.

Note that we are using the `let` keyword when declaring the variable `x` since if we were to use `const`, we wouldn’t be able to assign a new value to `x`.

## Example: Writing a Countdown Function Using a While Loop

Let’s create a function that would countdown from 10 to 1\. At the end of the countdown, it should display a given text value.

```
1 countdown("Launch!");
2 // Counts down from 10 to 1\. Then displays "Launch!" to the screen.
3 // 10
4 // 9
5 // ...
6 // Launch!
```

Let’s also make it so that the countdown value would be adjustable. If there is no second argument provided, it should countdown from 10. But a second argument can be passed to customize this value to be anything we want (as long as the given value is above 1).

```
1 countdown("Launch!", 3);
2 // Counts down from 3 to 1\. Then displays "Launch!" to the screen.
3 // 3
4 // 2
5 // 1
6 // Launch!
```

We should start by writing the skeleton for our function.

```
1 function countdown(message, startingNumber = 10) {}
2 
3 countdown("Launch!");
```

js-basics-08-loops/03.js

We will create a `while` loop inside the `countdown` function and make it start from the `startingNumber`. The loop should continue while the `startingNumber` is bigger than `0`.

```
1 function countdown(message, startingNumber = 10) {
2   while (startingNumber > 0) {
3     console.log(startingNumber);
4     startingNumber = startingNumber - 1;
5   }
6 }
7 
8 countdown("Launch!");
```

js-basics-08-loops/04.js

With each iteration of the loop, we are subtracting `1` from the `startingNumber`. When the `startingNumber` reaches `0`, the loop will stop working.

The final thing that we need to do here is to make use of the `message` variable. And let’s test it by passing a different `startingNumber`.

```
 1 function countdown(message, startingNumber = 10) {
 2   while (startingNumber > 0) {
 3     console.log(startingNumber);
 4     startingNumber = startingNumber - 1;
 5   }
 6 
 7   console.log(message);
 8 }
 9 
10 countdown("Launch!", 15);
```

js-basics-08-loops/05.js

We also need to ensure that the user is passing a starting number that is above `1`.

```
 1 function countdown(message, startingNumber = 10) {
 2   if (startingNumber <= 1) {
 3     console.log("Please enter a number bigger than 1.");
 4     return;
 5   }
 6 
 7   while (startingNumber > 0) {
 8     console.log(startingNumber);
 9     startingNumber = startingNumber - 1;
10   }
11 
12   console.log(message);
13 }
14 
15 countdown("Launch!", 0);
```

js-basics-08-loops/06.js

Here we have added a check to see if the `startingNumber` is above 1\. If it is not we are displaying an error message and **returning** from the function.

## for Loop

Since it is very common to write loops that only execute for a given amount of time, JavaScript has a dedicated structure for it. It is called a `for` loop. Here is how to build a `for` loop.

```
1 for (let counter = 0; counter < 10; counter = counter + 1) {
2   console.log("This for a for loop");
3 }
```

js-basics-08-loops/07.js

A `for` loop has five parts:

*   The `for` keyword.
*   There is a parenthesis next to the `for` keyword. Inside there, the first section is for the initialization of a **loop variable**. We named this variable to be `counter` in this example, but it can be anything we want.
*   The second section of the parenthesis is the **loop condition**. The loop will run as long as this condition is `true`.
*   The third section of the parenthesis is the **loop variable incrementation**. Here we adjust the **loop variable’s value** so that the **loop condition** can be satisfied at some point (assuming we are **not** trying to write an infinite loop).
*   The last part of a `for` loop is the body statement. This is what gets executed as part of the loop.

## Example: Writing a Countdown Function Using a for Loop

Let’s rewrite our previous example using a `for` loop.

```
 1 function countdown(message, startingNumber = 10) {
 2   if (startingNumber <= 1) {
 3     console.log("Please enter a number bigger than 1.");
 4     return;
 5   }
 6 
 7   for (
 8     let countdownNumber = startingNumber;
 9     countdownNumber > 0;
10     countdownNumber = countdownNumber - 1
11   ) {
12     console.log(countdownNumber);
13   }
14 
15   console.log(message);
16 }
17 
18 countdown("Launch!", 5);
```

js-basics-08-loops/08.js

`for` loop collects every expression needed for managing a loop in one place (inside the parenthesis next to the `for` keyword). This makes it a bit easier to write and manage a `for` loop. When writing a `while` loop, there is a risk of forgetting to increment the **loop variable** and create an unintentional infinite loop. The structure of the `for` loop minimizes that risk.

It is worth mentioning that the variable name chosen for `for` loops are usually much shorter for legibility. Conventionally, the letter `i` is used as a **loop variable** name. We can update our example to reflect that convention.

```
 1 function countdown(message, startingNumber = 10) {
 2   if (startingNumber <= 1) {
 3     console.log("Please enter a number bigger than 1.");
 4     return;
 5   }
 6 
 7   for (let i = startingNumber; i > 0; i = i - 1) {
 8     console.log(i);
 9   }
10 
11   console.log(message);
12 }
13 
14 countdown("Launch!", 5);
```

js-basics-08-loops/09.js

## Looping Over Collections

As we have learned earlier **arrays** and **strings** are collection-like data types. We can loop over these collections using a `while` loop or a `for` loop.

Let’s write a function that would display every item of a given array on a separate line.

```
1 function displayItems(collection) {
2   for (let i = 0; i < collection.length; i = i + 1) {
3     console.log(collection[i]);
4   }
5 }
6 
7 const myFavoriteFood = ["pizza", "sushi", "tacos"];
8 displayItems(myFavoriteFood);
```

js-basics-08-loops/10.js

We wrote a `for` loop here that starts a loop from number `0` up until the given collection’s length, which is equal to `3` in this case. This means that the **loop variable** will be assigned the values `0`, `1`, and `2` throughout this loop’s execution. We can use these values as **indices** of items of the given collection.

There are built-in array methods that allow us to iterate over a given array since it is such a common operation to perform.

Two of those methods are `forEach` and `map`.

## forEach Method

The array’s `forEach` method executes a given **callback function** for every item in the array.

```
1 const myFavoriteFood = ["pizza", "sushi", "tacos"];
2 
3 myFavoriteFood.forEach(function (item, index, arr) {
4   console.log(item);
5   console.log(index);
6   console.log(arr);
7 });
```

js-basics-08-loops/11.js

The `forEach` method takes a callback function and provides it with three arguments.

*   The first argument is the **current item** in the iteration.
*   The second argument is the **index** of the current item.
*   The third item is the **array** that we are iterating over.

Using `forEach` displaying every item in a given array becomes extremely easy.

```
1 const myFavoriteFood = ["pizza", "sushi", "tacos"];
2 
3 myFavoriteFood.forEach(function (item) {
4   console.log(item);
5 });
```

js-basics-08-loops/12.js

It is common to use the shorthand function definition syntax (**arrow function**) when defining inline functions. It reduces the amount of code that we need to write. Let’s refactor our example to use an arrow function.

```
1 const myFavoriteFood = ["pizza", "sushi", "tacos"];
2 
3 myFavoriteFood.forEach((item) => {
4   console.log(item);
5 });
```

js-basics-08-loops/13.js

## Example: Multiplier Function

Let’s write a function called **multiplier** that gets an array of numbers. It should multiply every item in the array with a given value (or with `2` if a value is not provided). Then it should return a **new** array with the updated values. It should look like this:

```
1 const arr = [1, 2, 3, 4, 5];
2 const newArr = multiplier(arr, 3);
3 
4 console.log(arr); // [1, 2, 3, 4, 5];
5 console.log(newArr); // [3, 6, 9, 12, 15];
```

js-basics-08-loops/14.js

We are displaying the value of both the given array (`arr`) and the `newArr` to ensure that our function does not change, **mutate,** the original array. As a general rule, functions should not **mutate** the given values but return a new value whenever possible.

Let’s see how to tackle this example both with a `for` loop and using the `forEach` method.

This is how we would implement this function using a `for` loop.

```
 1 function multiplier(arr, multiplierNum = 2) {
 2   const result = [];
 3 
 4   for (let i = 0; i < arr.length; i = i + 1) {
 5     const currentItem = arr[i];
 6     const newItem = currentItem * multiplierNum;
 7     result.push(newItem);
 8   }
 9 
10   return result;
11 }
12 
13 const arr = [1, 2, 3, 4, 5];
14 const newArr = multiplier(arr, 3);
15 
16 console.log(arr); // [1, 2, 3, 4, 5];
17 console.log(newArr); // [3, 6, 9, 12, 15];
```

js-basics-08-loops/15.js

We are creating an empty array called `result` inside the function body to store the results of our multiplication operation. Then we are creating a `for` loop to iterate over the items of an array. We multiply each item with the given `multiplierNum` value and then `push` this new value into the `result` array. We return the `result` array after the loop is complete.

Same functionality implemented with `forEach` method would look like this.

```
 1 function multiplier(arr, multiplierNum = 2) {
 2   const result = [];
 3 
 4   arr.forEach((item) => {
 5     const newItem = item * multiplierNum;
 6     result.push(newItem);
 7   });
 8 
 9   return result;
10 }
11 
12 const arr = [1, 2, 3, 4, 5];
13 const newArr = multiplier(arr, 3);
14 
15 console.log(arr); // [1, 2, 3, 4, 5];
16 console.log(newArr); // [3, 6, 9, 12, 15];
```

js-basics-08-loops/16.js

It is a very common operation to iterate over arrays and alter the items’ values to create a new array. Arrays have a method called `map` that makes these kinds of operations much easier.

## map Method

A `map` method is similar to a `forEach` method. We pass a callback function to a `map` method that gets executed on every item.

```
1 const myFavoriteFood = ["pizza", "sushi", "tacos"];
2 
3 myFavoriteFood.map((item) => {
4   console.log(item);
5 });
```

js-basics-08-loops/17.js

As we can see, it looks very similar to the `forEach` method. The arguments that the callback function takes are also the same as the `forEach` method. The difference is that the `map` method results in a new array with the items we return from the callback function.

```
1 const myFavoriteFood = ["pizza", "sushi", "tacos"];
2 
3 const myNewFavoriteFood = myFavoriteFood.map((item) => {
4   return "ice cream";
5 });
6 
7 console.log(myFavoriteFood); // ["pizza", "sushi", "tacos"];
8 console.log(myNewFavoriteFood); // ["ice cream", "ice cream", "ice cream"];
```

js-basics-08-loops/18.js

Using the `map` method, we are able to construct a new array consisting of whatever we `return` from the callback function.

Writing a `multiplier` function is so much easier when using the `map` method.

```
 1 function multiplier(arr, multiplierNum = 2) {
 2   return arr.map((item) => {
 3     return item * multiplierNum;
 4   });
 5 }
 6 
 7 const arr = [1, 2, 3, 4, 5];
 8 const newArr = multiplier(arr, 3);
 9 
10 console.log(arr); // [1, 2, 3, 4, 5];
11 console.log(newArr); // [3, 6, 9, 12, 15];
```

js-basics-08-loops/19.js

Probably, we wouldn’t even write a separate `multiplier` function since the `map` method makes it so easy to this operation on the array.

```
1 const arr = [1, 2, 3, 4, 5];
2 const newArr = arr.map((item) => item * 3);
3 
4 console.log(arr); // [1, 2, 3, 4, 5];
5 console.log(newArr); // [3, 6, 9, 12, 15];
```

js-basics-08-loops/20.js

## filter Method

It is a common requirement to go through the items of an array to see if they satisfy a certain condition. For example, imagine having to write a function that would iterate over an array and return all those items that are longer than 4 characters.

```
1 function checkLength(arr) {}
2 
3 const arr = ["pizza", "taco", "egg", "sushi", "ice cream"];
4 const newArr = checkLength(arr);
5 console.log(newArr); // ["pizza", "sushi", "ice cream"];
```

js-basics-08-loops/21.js

We would need to use a `loop` or the `forEach` method to implement this function with our knowledge. `map` wouldn’t be applicable here since `map` returns **something** for each item in an array. Here we don’t want to return **anything** if the item is shorter or equal to 4 characters in length.

```
 1 function checkLength(arr) {
 2   const result = arr.map((item) => {
 3     if (item.length > 4) {
 4       return item;
 5     }
 6   });
 7 
 8   return result;
 9 }
10 
11 const arr = ["pizza", "taco", "egg", "sushi", "ice cream"];
12 const newArr = checkLength(arr);
13 console.log(newArr); // ["pizza", undefined, undefined, "sushi", "ice cream"]
```

js-basics-08-loops/22.js

Here is what the implementation would look like using a `forEach` method.

```
 1 function checkLength(arr) {
 2   const result = [];
 3 
 4   arr.forEach((item) => {
 5     if (item.length > 4) {
 6       result.push(item);
 7     }
 8   });
 9 
10   return result;
11 }
12 
13 const arr = ["pizza", "taco", "egg", "sushi", "ice cream"];
14 const newArr = checkLength(arr);
15 console.log(newArr); // ["pizza", "sushi", "ice cream"]
```

js-basics-08-loops/23.js

This function achieves what we are trying to do, but there is a better way of doing this. It is by using the `filter` method.

```
 1 function checkLength(arr) {
 2   return arr.filter((item) => {
 3     if (item.length > 4) {
 4       return true;
 5     }
 6 
 7     return false;
 8   });
 9 }
10 
11 const arr = ["pizza", "taco", "egg", "sushi", "ice cream"];
12 const newArr = checkLength(arr);
13 console.log(newArr); // ["pizza", "sushi", "ice cream"]
```

js-basics-08-loops/24.js

The `filter` method takes a callback function that gets provided with the same arguments as `forEach` or the `map` method. The `filter` method iterates over every item and returns a new array that consists of items where the callback function for the item returns `true`. The item will not be included in the final array if the callback function is to return a `false` or a **falsy** value (like `undefined`).

## Summary

In this chapter, we have learned about **loops**. A **loop** is a programming structure that allows us to perform repetitive operations easily. There are a bunch of ways to write loops. We have learned about the `while` and `for` loops. We can use these structures to loop over arrays or write loops that work indefinitely (**infinite loops**).

When working with collections like **arrays** or **strings**, we frequently need to perform operations on every item of that collection.

*   Given an array of names, we might want to find a person with a specific name.
*   Given an array of numbers, we might want to operate on every number (maybe calculate the square root of all of them.), etc.

This operation of going through every item in a collection is called **iteration**. We can use `while` or `for` loops to iterate over arrays, but some array methods are better suited to this task. These are `forEach` and `map` methods.

A `forEach` method allows us to iterate over each item of an array and execute a **callback function** on those items. The `map` method is structurally similar to the `forEach` method, but it returns a new array consisting of the values returned from the callback function.

We have also learned about the `filter` method that is also structurally similar to `forEach` and `map` methods. The `filter` is similar to the `map` method in that it also returns a new array. We can use the `filter` method to eliminate the items in an array that we don’t need.

# 10 Project: Password Validator

Previously we have implemented a simple password validator, but we now have much more knowledge to implement a full-featured version. There are some new requirements that we would like this password validator to enforce.

The given password should:

*   be minimum of 8, maximum of 12 characters.
*   can not start or end with a space character.
*   should at least include 2 special characters (can be `!@#$%^&*`)
*   can not have 2 characters repeated in a row
*   needs to have at least 2 numbers

These password requirements might sound ridiculous, but there are actually websites out there with similar or even more restrictive requirements. This link has many examples for unreasonable password restrictions that can be found in the wild: [https://github.com/dumb-password-rules/dumb-password-rules](https://github.com/dumb-password-rules/dumb-password-rules).

We are going to create a function called `passwordValidator` that is going to validate the given password. It will return `true` if the given password is valid, `false` if not.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   // returns true if is a valid password
 9   // otherwise returns false
10 }
```

js-basics-09-project-password-validator/00.js

We have previously seen what **test-driven development (TDD)** looks like. In **TDD,** we would first write a test or an assertion about the functionality we will implement. Then, we would write the functionality that will get verified by the test.

Here we are not going to follow TDD methodology, but we will still do something similar. We will have an **array** of invalid passwords. Our password validator is expected to validate all of these passwords correctly. In this case, it should return `false` for each of these invalid passwords.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   // returns true if is a valid password
 9   // otherwise returns false
10 }
11 
12 const disallowedPasswords = [
13   "1234567", // too few characters
14   "123456789101112", // too many characters
15   "12345678 ", // has space at the end
16   " 12345678", // has space at the beginning
17   "12345678", // does not include 2 special chars
18   "12345678!", // does not include 2 special chars
19   "123456778!@", // repeating char 7
20   "12345678!!@", // repeating char !
21   "abcdefgh!@", // does not have numbers
22   "abcdefgh!@1", // does not have enough numbers
23 ];
24 
25 disallowedPasswords.forEach((password) => {
26   const isSuccessfullyValidated = passwordValidator(password) === false;
27   if (!isSuccessfullyValidated) {
28     console.log(`validation failed for ${password}`);
29   }
30 });
```

js-basics-09-project-password-validator/01.js

`disallowedPasswords` is an array that contains a bunch of passwords that are not valid according to our requirements. We are looping through each of these passwords by using the `forEach` method and feed them into the `passwordValidator` function. We expect the result to be `false`. If the result is not `false`, we log a message to the screen that says the `validation failed` for the given password.

We expect to get less of this message as we implement the features of this password validator.

## Minimum 8, Maximum 12 Characters

We have previously worked on an example that also had similar password length requirements. We can validate the length of the password quickly by using **comparison operators**.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   if (password.length < 8) {
 9     return false;
10   }
11 
12   if (password.length > 12) {
13     return false;
14   }
15 }
16 
17 const disallowedPasswords = [
18   "1234567", // too few characters
19   "123456789101112", // too many characters
20   "12345678 ", // has space at the end
21   " 12345678", // has space at the beginning
22   "12345678", // does not include 2 special chars
23   "12345678!", // does not include 2 special chars
24   "123456778!@", // repeating char 7
25   "12345678!!@", // repeating char !
26   "abcdefgh!@", // does not have numbers
27   "abcdefgh!@1", // does not have enough numbers
28 ];
29 
30 disallowedPasswords.forEach((password) => {
31   const isSuccessfullyValidated = passwordValidator(password) === false;
32 
33   if (!isSuccessfullyValidated) {
34     console.log(`validation failed for ${password}`);
35   }
36 });
```

js-basics-09-project-password-validator/02.js

We should now be getting fewer validation errors. It is hard to tell how many of our passwords are passing the validation, though. Let’s implement some code to be able to identify that.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   if (password.length < 8) {
 9     return false;
10   }
11 
12   if (password.length > 12) {
13     return false;
14   }
15 }
16 
17 const disallowedPasswords = [
18   "1234567", // too few characters
19   "123456789101112", // too many characters
20   "12345678 ", // has space at the end
21   " 12345678", // has space at the beginning
22   "12345678", // does not include 2 special chars
23   "12345678!", // does not include 2 special chars
24   "123456778!@", // repeating char 7
25   "12345678!!@", // repeating char !
26   "abcdefgh!@", // does not have numbers
27   "abcdefgh!@1", // does not have enough numbers
28 ];
29 
30 const results = disallowedPasswords.map((password) => {
31   const isSuccessfullyValidated = passwordValidator(password) === false;
32 
33   if (!isSuccessfullyValidated) {
34     console.log(`validation failed for ${password}`);
35     return false;
36   }
37 
38   return true;
39 });
40 
41 const finalResults = results.filter((result) => result);
42 console.log(
43   `total success is ${finalResults.length} out of ${disallowedPasswords.length}`
44 );
```

js-basics-09-project-password-validator/03.js

We are now looping through the `disallowedPasswords` array with a `map` method and save the result in a `results` array. This will create an array that consists of `true` or `false` values. We are then filtering this array to get rid of the `false` values.

```
1 const finalResults = results.filter((result) => result);
```

js-basics-09-project-password-validator/03.js

The `filter` method on arrays allows us to create an array with only the specified values. What gets included in the resulting array is determined by what we return from the filter method’s callback function. An item gets included in the resulting array if what we return is `true` or **truthy**. It is not included if it is `false` or **falsy**.

We display the `length` of the `finalResults` array to show how many passwords can be successfully validated at the moment.

## No Space at the Start or at the End

We don’t want to allow passwords that have a space character at the beginning or the end. We will enforce this restriction by grabbing the first and the last character and checking to see if it is equivalent to the space character.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   const length = password.length;
 9 
10   if (length < 8) {
11     return false;
12   }
13 
14   if (length > 12) {
15     return false;
16   }
17 
18   const firstChar = password[0];
19   const lastChar = password[length - 1];
20   const spaceChar = " ";
21 
22   if (firstChar === spaceChar || lastChar === spaceChar) {
23     return false;
24   }
25 }
```

js-basics-09-project-password-validator/04.js

I have omitted the part where we are checking against the `disallowedPasswords` array to focus on the `passwordValidator` function. This is the logic that we have implemented inside the function to check for the space character.

```
1 const firstChar = password[0];
2 const lastChar = password[length - 1];
3 const spaceChar = " ";
4 
5 if (firstChar === spaceChar || lastChar === spaceChar) {
6   return false;
7 }
```

js-basics-09-project-password-validator/04.js

If the first or the last character is equivalent to `" "` (space character), we are returning `false`. We don’t return `true` just yet because we can’t be sure if the password is valid. There are other checks that we need to perform before we can return `true`.

## Includes at Least Two Special Characters

Our requirements define the following characters as **special characters.**

```
1 const specialChars = ["!", "@", "#", "$", "%", "^", "&", "*"];
```

We would like to make sure that the given password has at least two special characters in it.

To check for that requirement, we will loop through every character of the given password for every special character we have and check to see if there is a match. We will count the number of matches. If the count is less than `2`, we will return `false`.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   const length = password.length;
 9 
10   if (length < 8) {
11     return false;
12   }
13 
14   if (length > 12) {
15     return false;
16   }
17 
18   const firstChar = password[0];
19   const lastChar = password[length - 1];
20   const spaceChar = " ";
21 
22   if (firstChar === spaceChar || lastChar === spaceChar) {
23     return false;
24   }
25 
26   const specialChars = ["!", "@", "#", "$", "%", "^", "&", "*"];
27   let specialCharMatchCount = 0;
28 
29   specialChars.forEach((char) => {
30     for (let i = 0; i < length; i = i + 1) {
31       const currentChar = password[i];
32       if (currentChar === char) {
33         specialCharMatchCount = specialCharMatchCount + 1;
34       }
35     }
36   });
37 
38   if (specialCharMatchCount < 2) {
39     return false;
40   }
41 }
```

js-basics-09-project-password-validator/05.js

Here we have an array of special characters called `specialChars`. We also have a variable called `specialCharMatchCount` which will keep the count of the special characters that we encounter in the password. We then loop through every character inside the `specialChars` array. Inside the loop, we have another loop that goes through every character of the given password. If the password’s current character matches the current special character, we increment the `specialCharMatchCount` value by `1`. We return `false` if the value is less than `2` at the end of the iteration.

```
 1 const specialChars = ["!", "@", "#", "$", "%", "^", "&", "*"];
 2 let specialCharMatchCount = 0;
 3 
 4 specialChars.forEach((char) => {
 5   for (let i = 0; i < length; i = i + 1) {
 6     const currentChar = password[i];
 7     if (currentChar === char) {
 8       specialCharMatchCount = specialCharMatchCount + 1;
 9     }
10   }
11 });
12 
13 if (specialCharMatchCount < 2) {
14   return false;
15 }
```

js-basics-09-project-password-validator/05.js

## No Repeating Characters

We would also like to check if there are any repeating characters inside a given password. To do that, we will construct a `for` loop to get the current character of the password and the previous character. The function should return `false` if the current character is equivalent to the previous character.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   const length = password.length;
 9 
10   if (length < 8) {
11     return false;
12   }
13 
14   if (length > 12) {
15     return false;
16   }
17 
18   const firstChar = password[0];
19   const lastChar = password[length - 1];
20   const spaceChar = " ";
21 
22   if (firstChar === spaceChar || lastChar === spaceChar) {
23     return false;
24   }
25 
26   const specialChars = ["!", "@", "#", "$", "%", "^", "&", "*"];
27   let specialCharMatchCount = 0;
28 
29   specialChars.forEach((char) => {
30     for (let i = 0; i < length; i = i + 1) {
31       const currentChar = password[i];
32       if (currentChar === char) {
33         specialCharMatchCount = specialCharMatchCount + 1;
34       }
35     }
36   });
37 
38   if (specialCharMatchCount < 2) {
39     return false;
40   }
41 
42   for (let i = 0; i < length; i = i + 1) {
43     const currentChar = password[i];
44     const previousChar = password[i - 1];
45     if (currentChar === previousChar) {
46       return false;
47     }
48   }
49 }
```

js-basics-09-project-password-validator/06.js

This is the part of the function where we are checking for repeating characters.

```
1 for (let i = 0; i < length; i = i + 1) {
2   const currentChar = password[i];
3   const previousChar = password[i - 1];
4   if (currentChar === previousChar) {
5     return false;
6   }
7 }
```

js-basics-09-project-password-validator/06.js

We are getting the previous character by using the loop index, which is the `i` variable. This check might look weird when we are first starting the loop since `i-1` will return `-1`. `password[-1]` returns `undefined`. `undefined` wouldn’t be equivalent to the `password[0]`, so our logic works.

## Includes at Least Two Numbers

The final requirement we will implement is to check if the given password has at least two numbers. This will be similar to the check that we have performed to count the special characters in the password. We will create an array with all the numbers and a variable that keeps the count of the numbers we encounter in the password.

```
 1 // min 8, max 12 chars
 2 // no space at the start or end
 3 // should at least include 2 special chars of: !@#$%^&*
 4 // no repeating chars
 5 // need to have at least 2 numbers
 6 
 7 function passwordValidator(password) {
 8   const length = password.length;
 9 
10   if (length < 8) {
11     return false;
12   }
13 
14   if (length > 12) {
15     return false;
16   }
17 
18   const firstChar = password[0];
19   const lastChar = password[length - 1];
20   const spaceChar = " ";
21 
22   if (firstChar === spaceChar || lastChar === spaceChar) {
23     return false;
24   }
25 
26   const specialChars = ["!", "@", "#", "$", "%", "^", "&", "*"];
27   let specialCharMatchCount = 0;
28 
29   specialChars.forEach((char) => {
30     for (let i = 0; i < length; i = i + 1) {
31       const currentChar = password[i];
32       if (currentChar === char) {
33         specialCharMatchCount = specialCharMatchCount + 1;
34       }
35     }
36   });
37 
38   if (specialCharMatchCount < 2) {
39     return false;
40   }
41 
42   for (let i = 0; i < length; i = i + 1) {
43     const currentChar = password[i];
44     const previousChar = password[i - 1];
45     if (currentChar === previousChar) {
46       return false;
47     }
48   }
49 
50   const numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
51   let numberCount = 0;
52 
53   numbers.forEach((number) => {
54     const numberStr = number.toString();
55     for (let i = 0; i < length; i = i + 1) {
56       const currentChar = password[i];
57       if (currentChar === numberStr) {
58         numberCount = numberCount + 1;
59       }
60     }
61   });
62 
63   if (numberCount < 2) {
64     return false;
65   }
66 
67   return true;
68 }
```

js-basics-09-project-password-validator/07.js

We have created an array called `numbers` with all the number characters and a variable called `numberCount` that keeps the count for the number occurrences inside the given password. We loop through each number and convert the current number to a string using the `toString` method. Then we loop through the password for every number to check if the password’s characters match the current number. If there is a match, we increment the `numberCount` variable by `1`.

```
 1 const numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
 2 let numberCount = 0;
 3 
 4 numbers.forEach((number) => {
 5   const numberStr = number.toString();
 6   for (let i = 0; i < length; i = i + 1) {
 7     const currentChar = password[i];
 8     if (currentChar === numberStr) {
 9       numberCount = numberCount + 1;
10     }
11   }
12 });
13 
14 if (numberCount < 2) {
15   return false;
16 }
```

js-basics-09-project-password-validator/07.js

We have successfully implemented all the requirements we had for this password validator! But there is a lot of room for improvement in this function. Let’s improve our code to be more readable and maintainable.

## Refactoring Code

**Refactoring** is a technique for restructuring a code without changing its external behavior. The purpose of refactoring is usually to improve the quality of the code. As a result of refactoring, code might become easier to read, faster to execute, more resilient to errors, etc.

One of the first things that we should do in this function is to move the check for individual requirements inside their own separate functions. This will allow us to group related functionality and tidy up the `passwordValidator` function. Once we are done, the `passwordValidator` function would become so much more readable.

```
 1 // min 8, max 12 chars
  2 // no space at the start or end
  3 // should at least include 2 special chars of: !@#$%^&*
  4 // no repeating chars
  5 // need to have at least 2 numbers
  6 
  7 function checkLength(password, min, max) {
  8   const length = password.length;
  9 
 10   if (length < min) {
 11     return false;
 12   }
 13 
 14   if (length > max) {
 15     return false;
 16   }
 17 
 18   return true;
 19 }
 20 
 21 function checkIfSpaceAtEitherEnd(password) {
 22   const length = password.length;
 23 
 24   const firstChar = password[0];
 25   const lastChar = password[length - 1];
 26   const spaceChar = " ";
 27 
 28   if (firstChar === spaceChar || lastChar === spaceChar) {
 29     return false;
 30   }
 31 
 32   return true;
 33 }
 34 
 35 function hasValidAmoutOfSpecialCharacters(password) {
 36   const length = password.length;
 37   const specialChars = ["!", "@", "#", "$", "%", "^", "&", "*"];
 38   let specialCharMatchCount = 0;
 39 
 40   specialChars.forEach((char) => {
 41     for (let i = 0; i < length; i = i + 1) {
 42       const currentChar = password[i];
 43       if (currentChar === char) {
 44         specialCharMatchCount = specialCharMatchCount + 1;
 45       }
 46     }
 47   });
 48 
 49   if (specialCharMatchCount < 2) {
 50     return false;
 51   }
 52 
 53   return true;
 54 }
 55 
 56 function hasRepetition(password) {
 57   for (let i = 0; i < length; i = i + 1) {
 58     const currentChar = password[i];
 59     const previousChar = password[i - 1];
 60     if (currentChar === previousChar) {
 61       return false;
 62     }
 63   }
 64 
 65   return true;
 66 }
 67 
 68 function hasValidAmountOfNumbers(password) {
 69   const numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];
 70   let numberCount = 0;
 71 
 72   numbers.forEach((number) => {
 73     const numberStr = number.toString();
 74     for (let i = 0; i < length; i = i + 1) {
 75       const currentChar = password[i];
 76       if (currentChar === numberStr) {
 77         numberCount = numberCount + 1;
 78       }
 79     }
 80   });
 81 
 82   if (numberCount < 2) {
 83     return false;
 84   }
 85 
 86   return true;
 87 }
 88 
 89 function passwordValidator(password) {
 90   const minAllowedLength = 8;
 91   const maxAllowedLength = 12;
 92 
 93   if (!checkLength(password, minAllowedLength, maxAllowedLength)) {
 94     return false;
 95   }
 96 
 97   if (checkIfSpaceAtEitherEnd(password)) {
 98     return false;
 99   }
100 
101   if (!hasValidAmoutOfSpecialCharacters(password)) {
102     return false;
103   }
104 
105   if (hasRepetition(password)) {
106     return false;
107   }
108 
109   if (!hasValidAmountOfNumbers(password)) {
110     return false;
111   }
112 
113   return true;
114 }
```

js-basics-09-project-password-validator/08.js

We have created individual functions for the validation of each requirement. The code might look slightly longer right now, but the `passwordValidator` is so much more readable. In fact, to read this code is almost like reading in English. Each variable and a function has an obvious name and purpose.

If we are to check the function against `disallowedPasswords`, we should still see that it works as expected. We don’t have a very firm test structure in place, but even the very little we have is proving useful in ensuring that our refactor didn’t break anything.

## Summary

In this chapter, we have built a full-featured password validator that can enforce a lot of arbitrary restrictions. We have used what we have learned in previous chapters, like **loops** and **conditional statements,** and built a **function** that we could potentially use in a software application. We have also learned what **refactoring** is and applied it to make our code a lot more legible and maintainable.

# 11 Programming Libraries

Until this point, we have either been using functions bundled into JavaScript like `console.log`, `parseInt`, `Math.random`, or functions that we have created ourselves. However, it would be extremely time-consuming to create every functionality needed when building a software application. This is why we have **programming libraries (or packages)**, code that is previously written for a specific purpose that is packaged and shared for reusability.

Imagine trying to build a first-person shooter game. If we had to write every piece of functionality we need by ourselves, we would have to write a lot of code to handle the 3D graphics. That means a lot of complex mathematical operations would need to be implemented in code. We would have to spend weeks or even months developing the foundational pieces before doing anything unique to our game. Luckily, creating and displaying 3D graphics on the computer is a solved problem. Many other smart people out there had to work on similar issues, and some of them choose to share their solutions to these problems in the form of **programming libraries**.

That is why getting started with programming is so much easier nowadays than it was before. We can simply install a library that would do the most complex tasks for us so that we can focus on building things that will be unique to our application.

There are libraries out there that would allow us to build 3D graphics, data visualizations, e-commerce solutions, and even artificial intelligence applications. Building a software application is mostly about figuring out how to use these libraries and bring them together in ways that are unique to what it is that we are trying to build.

JavaScript is one of the most popular programming languages in the world. As a result, it has a vibrant ecosystem of libraries that is created by its community. The great news is that the vast majority of these packages are free to use.

One way of discovering JavaScript libraries is using **npm**. **npm** is a **package manager** and a **package registry** for JavaScript. A **package manager** essentially keeps track of what libraries we have installed for our project. As a **package registry**, we can use **npm** to discover packages using their website’s search functionality.

I also use Google to search for a package that will fit my specific needs. As mentioned in the example above, if I needed a 3D graphics library, I would search for `3d graphics library JavaScript` and see what comes up.

When choosing a library to use in our project, we would check to see if it does what we are looking for, if it has many users and a community behind it, and actively maintained. We might have additional requirements like ease of use, popularity, etc.

This chapter will introduce you to a couple of useful and interesting programming libraries that are available in JavaScript.

## Loading Libraries

To use a library in our JavaScript code, we need the HTML file to load that library before our code is loaded.

Assuming this is the setup we have for loading a JavaScript file:

```
1 <!DOCTYPE html>
2 <html>
3   <body>
4     <h1>Hello World</h1>
5     <p>I am learning <strong>JavaScript</strong>!</p>
6     <script src="main.js"></script>
7   </body>
8 </html>
```

js-basics-10-programming-libraries/01.html

We would have to load the libraries before we load the `main.js` since `main.js` will depend on these libraries to work.

```
1 <!DOCTYPE html>
2 <html>
3   <body>
4     <h1>Hello World</h1>
5     <p>I am learning <strong>JavaScript</strong>!</p>
6     <script src="path/to/library"></script>
7     <script src="main.js"></script>
8   </body>
9 </html>
```

js-basics-10-programming-libraries/02.html

Where `"path/to/library"` would be the **file path** or the **URL** that points to the library we want to load. We can download the library to our local drive and use it from there, or there are **CDN’s** **(Convent Delivery Network)** that hosts these libraries online. We can use [www.cdnjs.com](http://www.cdnjs.com) to see if they host the library that we want to use.

## Library Examples

Here are some libraries that are interesting and useful.

### Day.js

![](resources/i_imgur_com---gYKoSTb.png)

**[Day.js](https://day.js.org/)** is a library that makes working with dates easier in JavaScript. Working with time in programming languages is usually much harder than people realize. There are different time zones; there are daylight savings, there can be different amounts of days in February each year, there are leap years, leap days, etc. All of these considerations make it incredibly hard to build a robust program that will handle each of these edge cases easily. Luckily, there are a bunch of programming libraries that make working with time easier. Day.js is one such library.

To start using it we reference it in an HTML file using a `script` tag.

```
 1 <!DOCTYPE html>
 2 <html>
 3 <body>
 4   <h1>Hello World</h1>
 5   <p>I am learning <strong>JavaScript</strong>!</p>
 6 	<script src="https://cdnjs.cloudflare.com/ajax/libs/humanize-duration/3.25.1/humani\
 7 ze-duration.min.js"></script>
 8   <script src="main.js"></script>
 9 </body>
10 </html>
```

js-basics-10-programming-libraries/03/index.html

And then we can start using the library in our `main.js` file.

```
1 const now = dayjs();
2 const currentDate = now.format();
3 console.log(currentDate);
```

js-basics-10-programming-libraries/03/main.js

Calling `dayjs()` gives us an object that represents the current time. In this example, we are saving this object inside a variable called `now`. To display this object’s current value, we can call a method called `format` that would display the value in an internationally accepted format. It would look something like this:

```
1 2021-02-06T16:00:31+01:00
```

This default display format is not easy to understand for a casual user. Luckily we can have this value formatted differently by passing a formatting string to the `format` method.

```
1 const now = dayjs();
2 const currentDate = now.format("DD/MM/YYYY");
3 console.log(currentDate);
```

js-basics-10-programming-libraries/04/main.js

`DD/MM/YYYY` is a formatting string that instructs the `format` method to display the date in a `Day/Month/Year` format. It is a very common thing to use a formatting string when working with date libraries. You can determine what kind of formatting values are accepted by the `format` method by visiting this link: [https://day.js.org/docs/en/display/format](https://day.js.org/docs/en/display/format).

Using a date library makes it easy to calculate different dates. Let’s look at an example of that.

```
1 const now = dayjs();
2 const currentDate = now.format("DD/MM/YYYY");
3 console.log(currentDate);
4 
5 const targetDate = now.add(999, "day");
6 const targetDateFormatted = targetDate.format("DD/MM/YYYY");
7 console.log(targetDateFormatted);
```

js-basics-10-programming-libraries/05/main.js

Here we are using the `add` method to calculate what the date would be after `999` days from the current date.

You might have heard about the **10,000 hours** rule. It is a theory popularized by **Malcolm Gladwell** in his book, **Outliers**. It states that to master any discipline, you need to commit to working on it for at least ten thousand hours. This principle has long been debunked, but it would still be interesting to use it in our code. Let’s assume we want to master a skillset, and we want to commit 3 hours per day, every day, to our practice. When would we master this skill if we were to start studying now?

```
1 const hoursNeededForMastery = 10000;
2 const practiceAmountPerDay = 3;
3 const daysNeededForMastery = hoursNeededForMastery / practiceAmountPerDay;
4 
5 const now = dayjs();
6 const targetDate = now.add(daysNeededForMastery, "day");
7 const targetDateFormatted = targetDate.format("DD/MM/YYYY");
8 console.log(`You should be able to achieve mastery by ${targetDateFormatted}`);
```

js-basics-10-programming-libraries/06/main.js

We find out how many days are needed for mastery by dividing `10000` by the amount of practice we would like to have per day. Then we are using the `add` method to add the number of days to the current date to see the date we would achieve mastery. We can create a function with this logic to make it reusable.

```
 1 function getDateForMastery(practiceAmountPerDay) {
 2   const hoursNeededForMastery = 10000;
 3   const daysNeededForMastery = hoursNeededForMastery / practiceAmountPerDay;
 4 
 5   const now = dayjs();
 6   const targetDate = now.add(daysNeededForMastery, "day");
 7   const targetDateFormatted = targetDate.format("DD/MM/YYYY");
 8   console.log(
 9     `You should be able to achieve mastery by ${targetDateFormatted} when working ${\
10 practiceAmountPerDay} hours per day.`
11   );
12 }
13 
14 getDateForMastery(1);
15 getDateForMastery(3);
16 getDateForMastery(5);
17 getDateForMastery(8);
```

js-basics-10-programming-libraries/07/main.js

According to these calculations, practicing 1 hour per day vs. 8 hours per day makes a difference of 24 years.

`Day.js` has tons of other methods that we can use. Find more about it at [`https://day.js.org/en/`](https://day.js.org/en/).

### Humanize Duration

![](resources/i_imgur_com---Gsqr7Qy.png)

Programming languages generally store time in **milliseconds**. This is good for precision but not great for readability. **[Humanize Duration](https://github.com/EvanHahn/HumanizeDuration.js)** is a library that takes a time value in milliseconds and converts it into a human-readable format.

To start using this library we reference it in a HTML file using a `script` tag.

```
 1 <!DOCTYPE html>
 2 <html>
 3   <body>
 4     <h1>Hello World</h1>
 5     <p>I am learning <strong>JavaScript</strong>!</p>
 6     <script src="https://cdnjs.cloudflare.com/ajax/libs/humanize-duration/3.25.1/hum\
 7 anize-duration.min.js"></script>
 8     <script src="main.js"></script>
 9   </body>
10 </html>
```

js-basics-10-programming-libraries/08/index.html

And then we can start using it inside our JS file.

```
1 const durationInMs = 3000;
2 const durationInText = humanizeDuration(durationInMs);
3 console.log(durationInText); // 3 seconds
```

js-basics-10-programming-libraries/08/main.js

`humanizeDuration` is a function that this library exports. It takes a value in milliseconds and converts it into a human-readable format. It also takes a second optional argument that we can use to adjust various aspects of the values it returns.

```
1 const durationInMs = 1000000;
2 const durationInText = humanizeDuration(durationInMs, {
3   units: ["d"],
4 });
5 console.log(durationInText); // 0.011574074074074073 days
```

js-basics-10-programming-libraries/09/main.js

In this example, we pass a `d` value to the `units` array to display the resulting value in **days**. We could have also passed different values to get results in days, weeks, months, etc. You can check out the library documentation at [https://www.npmjs.com/package/humanize-duration](https://www.npmjs.com/package/humanize-duration) to determine what other options are available for us to use. One thing that is really impressive about this library is how it works with different languages as well. We can provide a **language code** to the function, and it would output the result in the given language.

```
1 const durationInMs = 3000000000;
2 const durationInGermanText = humanizeDuration(durationInMs, {
3   language: "de",
4 });
5 console.log(durationInGermanText); // 1 Monat, 4 Tage, 6 Stunden, 50 Minuten
```

js-basics-10-programming-libraries/10/main.js

### franc

![](resources/i_imgur_com---fmoCEEi.png)

**[franc](https://github.com/wooorm/franc)** is a programming library that detects the language of a given text. Generally speaking, language detection is a task that is better tackled by machine learning if accuracy is a concern. But such a solution might require a lot of processing power, the involvement of additional steps such as model training, or usage of an external service if using a 3rd party solution.

**franc** relies on a statistical approach to detect languages so that it can work even on a browser. To start using it, we should reference it inside our HTML file.

```
 1 <!DOCTYPE html>
 2 <html>
 3 <body>
 4   <h1>Hello World</h1>
 5   <p>I am learning <strong>JavaScript</strong>!</p>
 6 	<script src="https://github.com/wooorm/franc/releases/download/3.0.0/franc-min.js">\
 7 </script>
 8   <script src="main.js"></script>
 9 </body>
10 </html>
```

js-basics-10-programming-libraries/11/index.html

**franc** has 3 different packages, `franc-min`, `franc`, and `franc-all`. They respectively support 82, 187, and 406 languages. In this example, we are using `franc-min`, which supports 82 languages with 8 million or more speakers.

Using **franc** is fairly simple. We pass a string to the `franc` function and it returns a result for the language code for the detected language of the text.

```
1 const languageCode = franc(
2   "Ein Differenzstrommessgerät überwacht den Differenzstrom in elektrischen Anlagen.\
3  Dieser Strom errechnet sich aus der Summe der Ströme aller Leiter außer dem Schutzl\
4 eiter (PE), die in die Anlage führen. Differenzströme können beispielsweise als Folg\
5 e von Isolationsfehlern auftreten."
6 );
7 console.log(languageCode); // deu
```

js-basics-10-programming-libraries/11/main.js

Here, we are passing a German block of text from Wikipedia to the `franc` function, and it returns the language code `deu`, which is the `ISO 639-2 Language Code` for German.

Under the hood, **franc** assigns a probability to possible language matches and returns the result with the highest probability. If we would like to see what probabilities it assigns to the result, we could use the `all` method.

```
1 const languageCodes = franc.all(
2   "Şefkat sözlüklerde “acıyarak ve/veya koruyarak sevme, sevecenlik” olarak tanımlan\
3 ır."
4 );
5 console.log(languageCodes);
```

js-basics-10-programming-libraries/12/main.js

We are now passing a Turkish text into the `franc.all` function. It returns an array of results since we are using the `all` method. Here is what the results look like:

```
 1 /*
 2 [
 3   [
 4     "tur",
 5     1
 6   ],
 7   [
 8     "uzn",
 9     0.7268835616438356
10   ],
11   [
12     "mad",
13     0.707298801369863
14   ],
15   [
16     "jav",
17     0.6907106164383562
18   ],
19 ...
20 */
```

Calling `all` returns an array of arrays. Each array has a language code as the first item and the probability value for a match with that language code as the second item. A probability of `1` means a certainty, so there is no need to look further than the first item. But there might be cases where **franc** might not have such certainty. In that case, it might make sense to consider other options that have a high probability of a match.

**franc** works best when given long sentences. Its confidence and the values for probabilities can decrease when working on shorter texts.

You can learn more about this library at this link: [https://github.com/wooorm/franc](https://github.com/wooorm/franc)

## Summary

In this chapter, we have learned about **programming libraries** and what makes them so useful. When building applications, it is normal to use 10s or even hundreds of such libraries. These libraries can also be using other libraries. This means that we might end up using thousands of libraries when building even a relatively simple application! **npm** is the package/library registry that we can use to discover these libraries.

We have also learned about a couple of different libraries to illustrate how programming libraries can be used and how they can be useful.

# 12 Project: Data Analysis

I have worked on many projects in my career where I needed to work with datasets. Usually, you are given a big dump of data, and you are expected to modify it to work for your purposes. Working with such data using programming is a great way to exercise our coding skills.

In this chapter, we will take a look at a dataset of thousands of data points and pose questions to this data. We will seek answers to our questions using our programming skills.

We will programmatically generate the data with a library called **faker**. **faker** is a JavaScript library that allows us to generate massive amounts of fake data like names, addresses, or numbers.

Generating fake data in a programming context is useful primarily for testing purposes. Programmers sometimes need large amounts of data to be able to test their applications. A library like **faker** can be used to effortlessly create realistic but fake data that wouldn’t compromise any user information.

To start using **faker** in our project, we need to start referencing it. There are a couple of ways of going about it. We can download a local copy of it and serve it from our computer. We can also link up to an online version of the library. We will go with the second way of doing it since it is easier.

To use the library, we will place this `script` tag inside your `html` document.

```
1 <script src="https://cdnjs.cloudflare.com/ajax/libs/Faker/3.1.0/faker.min.js">
```

You can place this tag inside the `head` tag. If you are working locally, you would also be linking to your **JavaScript** file from this HTML file. In that case, make sure to load **faker** before you load your own script. This is required since we will use **faker** in the script we will be writing.

```
 1 <!DOCTYPE html>
 2 <html>
 3   <head>
 4     <meta charset="utf-8" />
 5     <meta name="viewport" content="width=device-width" />
 6     <title>My document</title>
 7     <script src="https://cdnjs.cloudflare.com/ajax/libs/Faker/3.1.0/faker.min.js"></\
 8 script>
 9     <script src="main.js"></script>
10   </head>
11   <body></body>
12 </html>
```

js-basics-11-data-analysis/01/index.html

We can focus on JavaScript now that we have the HTML setup ready.

## Using Faker

`faker` has a bunch of categories that it can generate data in. Examples of these categories are `address`, `commerce`, `finance`, and `name`. Each category has a bunch of methods that generate a specific kind of **fake** data in that category. For example, `name` category has these methods:

*   `firstName`
*   `lastName`
*   `jobTitle`
*   `gender`

Here are some methods from the `address` category:

*   `country`
*   `countryCode`
*   `state`
*   `streetName`

You can learn more about the other methods available on their Github page: [https://github.com/marak/Faker.js/](https://github.com/marak/Faker.js/)

The structure of a `faker` function call is like this:

```
1 faker.name.firstName();
```

The above line would generate a fake first name every time it is called. If we wanted to get a fake `streetName`, we would do:

```
1 faker.address.streetName();
```

In our example, a datapoint will have the following information:

*   first name
*   last name
*   email
*   country
*   and if a student or not.

Let’s create a single datapoint and save it inside a JavaScript object.

```
 1 const firstName = faker.name.firstName();
 2 const lastName = faker.name.lastName();
 3 const email = faker.internet.email();
 4 const country = faker.address.country();
 5 const isStudent = faker.random.boolean();
 6 
 7 const personalInformation = {
 8   firstName,
 9   lastName,
10   email,
11   country,
12   isStudent,
13 };
14 
15 console.log(personalInformation);
```

js-basics-11-data-analysis/01/main.js

The methods that we haven’t talked about before are `internet.email`, and `random.boolean`. `email` should be self-explanatory. `random.boolean` is simply a method that returns a random value of `true` or `false`. We are storing the resulting value using the variable `isStudent`. We then create a JavaScript **object** called `personalInformation` that holds all this data.

JavaScript has this feature where if a property uses the same **key** and **value,** then we don’t have to specify them separately. So instead of doing this:

```
1 const personalInformation = { firstName: firstName };
```

We can do this:

```
1 const personalInformation = { firstName };
```

Notice that every time this function executes, it returns a different value. The results that are returned from faker are not only fake but also **random** as well. This can be problematic, and we will address this issue soon but let’s first create a function that will wrap and return this data.

```
 1 function getRandomPersonData() {
 2   const firstName = faker.name.firstName();
 3   const lastName = faker.name.lastName();
 4   const email = faker.internet.email();
 5   const country = faker.address.country();
 6   const isStudent = faker.random.boolean();
 7 
 8   const personalInformation = {
 9     firstName,
10     lastName,
11     email,
12     country,
13     isStudent,
14   };
15 
16   return personalInformation;
17 }
18 
19 const randomPersonData = getRandomPersonData();
20 console.log(randomPersonData);
```

js-basics-11-data-analysis/02/main.js

We have now created a function called `getRandomPersonData` that will return random and fake personal information when called. Let’s write some logic that would call this function multiple times.

```
 1 function getRandomPersonData() {
 2   const firstName = faker.name.firstName();
 3   const lastName = faker.name.lastName();
 4   const email = faker.internet.email();
 5   const country = faker.address.country();
 6   const isStudent = faker.random.boolean();
 7 
 8   const personalInformation = {
 9     firstName,
10     lastName,
11     email,
12     country,
13     isStudent,
14   };
15 
16   return personalInformation;
17 }
18 
19 const amount = 10;
20 for (let i = 0; i < amount; i = i + 1) {
21   const randomPersonData = getRandomPersonData();
22   console.log(randomPersonData);
23 }
```

js-basics-11-data-analysis/03/main.js

We have created a `for` loop that loops `10` times. Every time the loop runs, we are getting a new person’s data logged to the screen.

This is great, we now have the logic in place that can generate any number of fake data for us.

As mentioned before, the data that faker generates is not only fake but random as well. This might not be desirable in certain cases. In our example, we want to generate a dataset that remains the same every time we run our program. Not only that, we would like to create a dataset that would be the same regardless of who creates it. This way, you can follow this example much easier.

Computer-generated data is never truly random. That is because computers are **deterministic** machines. They are designed so that given the exact input, they would always produce the same output. They use mathematical tricks to generate values that look random but are not in reality. This is called **pseudo-randomness**.

There is this concept of **seed** in computer-generated randomness. Basically, it is the non-random value that generates the **pseudorandom** values. Given the same seed, we would always get the same “**random”** values.

To set a seed we can call the `seed` function like this:

```
1 faker.seed(1);
```

This means that our random values are now generated by using the seed value of `1`. If you are to make use of the same seed value, you will get the same result every time you run your program.

```
 1 faker.seed(1);
 2 
 3 function getRandomPersonData() {
 4   const firstName = faker.name.firstName();
 5   const lastName = faker.name.lastName();
 6   const email = faker.internet.email();
 7   const country = faker.address.country();
 8   const isStudent = faker.random.boolean();
 9 
10   const personalInformation = {
11     firstName,
12     lastName,
13     email,
14     country,
15     isStudent,
16   };
17 
18   return personalInformation;
19 }
20 
21 const amount = 10;
22 for (let i = 0; i < amount; i = i + 1) {
23   const randomPersonData = getRandomPersonData();
24   console.log(randomPersonData);
25 }
```

js-basics-11-data-analysis/04/main.js

Let’s now create a function that will wrap the `for` loop logic. We will call this function `createDataset`. It will get an `amount` argument and will use it to generate that many data items. It will store those items in an array and return that array.

```
 1 function createDataset(amount) {
 2   const dataset = [];
 3 
 4   for (let i = 0; i < amount; i = i + 1) {
 5     const randomPersonData = getRandomPersonData();
 6     dataset.push(randomPersonData);
 7   }
 8 
 9   return dataset;
10 }
11 
12 const dataset = createDataset(10000);
13 console.log(dataset);
```

js-basics-11-data-analysis/05/main.js

Now that we have this function, it is trivial to create a dataset with however many data points we want. Here we are creating a dataset of `10000` data points.

The fun part starts now that we have this data. Here are the questions that we will try to answer with this data:

*   How many students are there in this dataset and what is their percentage?
*   Which email providers exists in this dataset?
    *   Create an array that consists of every unique email provider’s name, like `google.com`, `yahoo.com`, etc.
*   How many users there are for each email provider?
*   Which user has the longest email address and what is that address?
*   Which user has the shortest email address what is that address?
*   Which country has the most users in this dataset?
*   Which country has the least users?

Let’s get started!

## How Many Students Are There?

Our first task is to find out the number of students in this dataset and their percentage. Moving on, instead of displaying the entire function, I will just include the part that we are actively developing.

We can count the number of students by using a `for` loop.

```
 1 // How many students are there?
 2 let numStudents = 0;
 3 for (let i = 0; i < dataset.length; i = i + 1) {
 4   const currentItem = dataset[i];
 5   const isStudent = currentItem.isStudent;
 6   if (isStudent) {
 7     numStudents = numStudents + 1;
 8   }
 9 }
10 
11 console.log(numStudents);
12 console.log((numStudents / dataset.length) * 100);
```

js-basics-11-data-analysis/06/main.js

The number of students divided by the dataset length multiplied by `100` gives us the percentage of students.

There are couple of small optimization we can do.

1.  We can put everything in a function that calculates this student data and returns it to us.
2.  We can use the **object** **destructuring** pattern to unpack the property values from the `currentItem`.

```
 1 // How many students are there?
 2 function getStudentsData(dataset) {
 3   let numStudents = 0;
 4   for (let i = 0; i < dataset.length; i = i + 1) {
 5     const currentItem = dataset[i];
 6     const { isStudent } = currentItem;
 7     if (isStudent) {
 8       numStudents = numStudents + 1;
 9     }
10   }
11 
12   return {
13     amount: numStudents,
14     percentage: (numStudents / dataset.length) * 100,
15   };
16 }
17 
18 const studentsData = getStudentsData(dataset);
19 console.log(studentsData);
```

js-basics-11-data-analysis/06_01/main.js

We have used the `for` loop here since it is a very generic purpose loop but a `filter` method can help us write less code.

```
 1 // How many students are there?
 2 function getStudentsData(dataset) {
 3   const students = dataset.filter((item) => {
 4     return item.isStudent;
 5   });
 6 
 7   const numStudents = students.length;
 8 
 9   return {
10     amount: numStudents,
11     percentage: (numStudents / dataset.length) * 100,
12   };
13 }
14 
15 const studentsData = getStudentsData(dataset);
16 console.log(studentsData);
```

js-basics-11-data-analysis/06_02/main.js

We are using the `filter` method to create an array of `students`. `filter` would create an array only with those items that return `true` when the `item.isStudent` is called. Then finding the number of students becomes a simple matter of looking at the `length` of this array. This results in code that is much more expressive and easier to read.

## Which Email Providers Exist?

Our second task is to find out which email providers exist in the dataset. To answer this question, we first need to extract the email provider given the email address.

For this purpose, we will assume anything that comes after the `@` symbol in an email is the email provider. We will write a `for` loop that goes through every character in a given string. The loop will locate the `@` symbol, and it would record what comes after this symbol.

Here is what that logic looks like:

```
 1 // Which email providers exists in this dataset?
 2 const data = dataset[0];
 3 const email = data.email;
 4 const emailLength = email.length;
 5 
 6 let atSymbolFound = false;
 7 let emailProvider = "";
 8 
 9 for (let i = 0; i < emailLength; i = i + 1) {
10   const currentCharacter = email[i];
11   if (atSymbolFound) {
12     emailProvider = emailProvider + currentCharacter;
13   }
14 
15   if (currentCharacter === "@") {
16     atSymbolFound = true;
17   }
18 }
19 
20 console.log(emailProvider);
```

js-basics-11-data-analysis/07/main.js

Inside the `for` loop, we are getting the current character of the email address. And then, we are checking to see if the `currentCharacter` is equivalent to the `@` symbol. If so, we are setting a variable called `atSymbolFound` to be `true`. We have another conditional logic inside the loop that checks to see if the variable `atSymbolFound` is `true`. If so, it starts constructing a string called `emailProvider` that would store the email provider’s name.

This logic works but we can make it simpler. Here is one way of improving it.

```
 1 const data = dataset[0];
 2 const email = data.email;
 3 const emailLength = email.length;
 4 
 5 let atSymbolIndex;
 6 let emailProvider;
 7 
 8 for (let i = 0; i < emailLength; i = i + 1) {
 9   const currentCharacter = email[i];
10 
11   if (currentCharacter === "@") {
12     atSymbolIndex = i;
13     break;
14   }
15 }
16 
17 if (atSymbolIndex !== undefined) {
18   emailProvider = email.slice(atSymbolIndex + 1, emailLength);
19 }
20 
21 console.log(emailProvider);
```

js-basics-11-data-analysis/07_01/main.js

Our previous logic was creating a string one character at a time.

```
1 emailProvider = emailProvider + currentCharacter;
```

In this new approach, we are only using the `for` loop to find the location of the `@` character. We are then using the `slice` method with the `atSymbolIndex` on the string object to get the part of the string that is relevant to us.

Notice the usage of the `break` keyword inside the `for` loop. `break` allows us to exit the loop early. We don’t need to keep looping once we found what we are looking for.

`slice` is a method that allows us to get a subsection of a string or an array. It accepts two inputs. An index to start slicing from and an index to slice up to. Using the `atSymbolIndex` allows us to get the part of the email address that is of interest to us.

We can optimize this code further.

```
 1 // Which email providers exists in this dataset?
 2 const data = dataset[0];
 3 const email = data.email;
 4 const emailLength = email.length;
 5 let emailProvider;
 6 
 7 const atSymbolIndex = email.indexOf("@");
 8 if (atSymbolIndex > -1) {
 9   emailProvider = email.slice(atSymbolIndex + 1, emailLength);
10 }
11 
12 console.log(emailProvider);
```

js-basics-11-data-analysis/07_02/main.js

There is a string and an array method called `indexOf`. It returns the index of the given item. It returns `-1` if the item is not found. Using this method, we can make our code much shorter.

We are going to remove the `if` statement that guards us from not having a `@` symbol. We will just trust `faker` to provide us with valid email addresses.

```
1 // Which email providers exists in this dataset?
2 const data = dataset[0];
3 const email = data.email;
4 
5 const atSymbolIndex = email.indexOf("@");
6 const emailProvider = email.slice(atSymbolIndex + 1, email.length);
7 
8 console.log(emailProvider);
```

js-basics-11-data-analysis/07_03/main.js

This is perfect. Notice how much shorter our code now is. Let’s put it inside a function.

```
 1 // Which email providers exists in this dataset?
 2 function getEmailProvider(email) {
 3   const atSymbolIndex = email.indexOf("@");
 4   const emailProvider = email.slice(atSymbolIndex + 1, email.length);
 5 
 6   return emailProvider;
 7 }
 8 
 9 const data = dataset[0];
10 const email = data.email;
11 const emailProvider = getEmailProvider(email);
12 console.log(emailProvider);
```

js-basics-11-data-analysis/07_04/main.js

We have now created a function called `getEmailProvider` and calling that function on the first datapoint of our dataset. Let’s now run this function over our entire dataset.

```
 1 // Which email providers exists in this dataset?
 2 function getEmailProvider(email) {
 3   const atSymbolIndex = email.indexOf("@");
 4   const emailProvider = email.slice(atSymbolIndex + 1, email.length);
 5 
 6   return emailProvider;
 7 }
 8 
 9 function getEmailProviders(dataset) {
10   const uniqueEmailProviders = [];
11 
12   dataset.forEach((data) => {
13     const email = data.email;
14     const emailProvider = getEmailProvider(email);
15     if (!uniqueEmailProviders.includes(emailProvider)) {
16       uniqueEmailProviders.push(emailProvider);
17     }
18   });
19 
20   return uniqueEmailProviders;
21 }
22 
23 const allUniqueEmailProviders = getEmailProviders(dataset);
24 console.log(allUniqueEmailProviders);
25 console.log(allUniqueEmailProviders.length);
```

js-basics-11-data-analysis/07_05/main.js

We have created a function called `getEmailProviders` that goes through each data point of the dataset using the `forEach` method. There is an initially empty array called `uniqueEmailProviders` in this function. As we are going through the dataset, we extract the email provider from the current data point. Then, we check to see if that email provider already exists inside `uniqueEmailProviders` array by using the `includes` method.

`includes` is a pretty simple method. It takes an item and checks to see if that item exists on the array. If it does, it returns `true` else, it returns `false`. We push the current item into the `uniqueEmailProviders` if the item does not already exist there.

After running this script we should get the following result.

```
1 ["hotmail.com", "yahoo.com", "gmail.com"];
```

Turns out there are only three unique email providers in this dataset.

## How Many Users There Are for Each Email Provider?

In this section, we will try to find out how many users there are for each email provider. Additionally, we will check to see the number of users they have as a percentage of the total. To be able to do so, we will reuse the `getEmailProvider` function that we created earlier.

```
 1 // How many users there are for each email provider?
 2 function getEmailProvider(email) {
 3   const atSymbolIndex = email.indexOf("@");
 4   const emailProvider = email.slice(atSymbolIndex + 1, email.length);
 5 
 6   return emailProvider;
 7 }
 8 
 9 function analyzeEmailProviders(dataset) {
10   const emailProviderData = {};
11 
12   dataset.forEach((item) => {
13     const email = item.email;
14     const emailProvider = getEmailProvider(email);
15 
16     if (!emailProviderData[emailProvider]) {
17       emailProviderData[emailProvider] = 0;
18     }
19   });
20 
21   return emailProviderData;
22 }
23 
24 const emailProviderAnalysis = analyzeEmailProviders(dataset);
25 console.log(emailProviderAnalysis);
```

js-basics-11-data-analysis/08/main.js

Here we have created a new function called `analyzeEmailProviders` to collect the user numbers for each email provider. We are gathering that data inside the `emailProviderData` object. This object is initially empty. We then go through the items of the `dataset` and find out the email provider for each item. We then check to see if that `emailProvider` exists on the `emailProviderData` object as a key. If it doesn’t exist, we create that key on the object and assign `0` to it. We then increment this number each time we find a user for an email provider.

## Which User Has the Longest Email Address?

Now we will find out which user has the longest email address. We will also see what that email address is. For this purpose, we need to go through every item in the list to find out what the longest email address is.

```
 1 // Which user has the longest email address and what is that address?
 2 function findTheLongestEmailAddress(dataset) {
 3   dataset.forEach((item) => {
 4     const emailAddress = item.email;
 5     console.log(emailAddress);
 6   });
 7 }
 8 
 9 const longestEmailAddress = findTheLongestEmailAddress(dataset);
10 console.log(longestEmailAddress);
```

js-basics-11-data-analysis/09/main.js

We start by creating a function called `findTheLongestEmailAddress`. We pass the entire dataset into this function and loop through every item in that dataset. This loop will form the basis of our logic. As we are looping, we should record the length and the value of the current email address. If the next email address is longer in length, we should override our record with the most current one.

If we keep doing this, the longest email address would be whatever our record is at the end of the loop.

```
 1 // Which user has the longest email address and what is that address?
 2 function findTheLongestEmailAddress(dataset) {
 3   let length = 0;
 4   let email;
 5 
 6   dataset.forEach((item) => {
 7     const emailAddress = item.email;
 8     const emailLength = emailAddress.length;
 9 
10     if (emailLength > length) {
11       length = emailLength;
12       email = emailAddress;
13     }
14   });
15 
16   return {
17     length,
18     email,
19   };
20 }
21 
22 const longestEmailAddress = findTheLongestEmailAddress(dataset);
23 console.log(longestEmailAddress);
```

js-basics-11-data-analysis/09_01/main.js

We initialize a `length` variable with a value of `0`. We have an `if` statement inside the `forEach` loop that checks whether the current email length is longer than the previously recorded `length` (which is 0, to begin with). If so, it updates the length and records the current email address under the variable name `email`.

We return an object with the `length` and `email` properties once we exit the loop.

## Which User Has the Shortest Email Address?

In this section, we will find out which user has the shortest email address and the value of that address. In the previous example, we had an initially recorded length of `0`, and every time an email address was longer than this length, we made a record of it. We could do a similar thing here as well. We can start with a ridiculously high length value for an email address, such as 1000, and every time the email address length is shorter than that value, we could make a record of it.

```
 1 // Which user has the shortest email address and what is that address?
 2 function findTheShortestEmailAddress(dataset) {
 3   let length = 1000;
 4   let email;
 5 
 6   dataset.forEach((item) => {
 7     const emailAddress = item.email;
 8     const emailLength = emailAddress.length;
 9 
10     if (emailLength < length) {
11       length = emailLength;
12       email = emailAddress;
13     }
14   });
15 
16   return {
17     length,
18     email,
19   };
20 }
21 
22 const shortestEmailAddress = findTheShortestEmailAddress(dataset);
23 console.log(shortestEmailAddress);
```

js-basics-11-data-analysis/10/main.js

This function was relatively easy to create. We just had to change the `length` value to something large and change the `>` operator in the conditional block to the `<` operator.

```
1 if (emailLength < length) {
```

Having said that, this solution feels **hacky** and unreliable. We are relying on an arbitrary number, `1000`, to find the result. We know from experience that the email addresses are not that long, but it feels not as reliable since the solution is based on observation. A better way to go about it would be to derive the initial length from the dataset.

```
 1 // Which user has the shortest email address and what is that address?
 2 function findTheShortestEmailAddress(dataset) {
 3   let length = dataset[0].email.length;
 4   let email;
 5 
 6   dataset.forEach((item) => {
 7     const emailAddress = item.email;
 8     const emailLength = emailAddress.length;
 9 
10     if (emailLength < length) {
11       length = emailLength;
12       email = emailAddress;
13     }
14   });
15 
16   return {
17     length,
18     email,
19   };
20 }
21 
22 const shortestEmailAddress = findTheShortestEmailAddress(dataset);
23 console.log(shortestEmailAddress);
```

js-basics-11-data-analysis/10_01/main.js

We are now initializing the `length` variable with the first item’s email address length in the dataset. This way, the number is much more grounded in reality and less arbitrary. The solution feels less **hacky**. Hacky solutions are not necessarily bad. They are frequently a way to get the job done in a much easier way. But this comes at a cost. We might end up writing programs that are hard to understand and maintain if we are frequently looking to cut corners.

## Which Country Has the Most Users?

Finding out which country has the most users will be similar to finding out the number of users each email provider has. We will first have to loop through every item in the dataset and determine which country they are from. We will keep track of the count in an object that has a key for each country in the list.

```
 1 // Which country has the most users?
 2 function getCountryData(dataset) {
 3   const countryData = {};
 4 
 5   dataset.forEach((item) => {
 6     const country = item.country;
 7 
 8     if (!countryData[country]) {
 9       countryData[country] = 0;
10     }
11 
12     countryData[country] = countryData[country] + 1;
13   });
14 
15   return countryData;
16 }
17 
18 const countryData = getCountryData(dataset);
19 console.log(countryData);
```

js-basics-11-data-analysis/11/main.js

This is pretty much the same logic that we had used when we were trying to count the users per email provider. But we are not done yet. This function gives us the number of users per country, but we need to find out which country has the most users in the dataset.

Let’s create another function called `analyzeCountryData` to find out which country has the most users.

```
 1 // Which country has the most users?
 2 function getCountryData(dataset) {
 3   const countryData = {};
 4 
 5   dataset.forEach((item) => {
 6     const country = item.country;
 7 
 8     if (!countryData[country]) {
 9       countryData[country] = 0;
10     }
11 
12     countryData[country] = countryData[country] + 1;
13   });
14 
15   return countryData;
16 }
17 
18 function analyzeCountryData(countryData) {
19   Object.keys(countryData).forEach((country) => {
20     const userCount = countryData[country];
21     console.log(`${country} has ${userCount} users`);
22   });
23 }
24 
25 const countryData = getCountryData(dataset);
26 const analyzedCountryData = analyzeCountryData(countryData);
27 console.log(analyzedCountryData);
```

js-basics-11-data-analysis/11_01/main.js

We have now created a function called `analyzeCountryData` that goes through every country and displays a text about the number of users there.

We can iterate through an object’s properties with the help of a function called `Object.keys`. `Object.keys` return an `array` that consists of the keys of the given object. We are then able to iterate through those keys with the use of the `forEach` method.

Next, we need to find the country with the most users. The logic for that operation will be similar to what we did to find out the user with the longest email address.

```
 1 // Which country has the most users?
 2 function getCountryData(dataset) {
 3   const countryData = {};
 4 
 5   dataset.forEach((item) => {
 6     const country = item.country;
 7 
 8     if (!countryData[country]) {
 9       countryData[country] = 0;
10     }
11 
12     countryData[country] = countryData[country] + 1;
13   });
14 
15   return countryData;
16 }
17 
18 function analyzeCountryData(countryData) {
19   let users = 0;
20   let countryName;
21 
22   Object.keys(countryData).forEach((country) => {
23     const userCount = countryData[country];
24     if (userCount > users) {
25       users = userCount;
26       countryName = country;
27     }
28   });
29 
30   return {
31     users,
32     country: countryName,
33   };
34 }
35 
36 const countryData = getCountryData(dataset);
37 const analyzedCountryData = analyzeCountryData(countryData);
38 console.log(analyzedCountryData);
```

js-basics-11-data-analysis/11_02/main.js

We have created two new variables called `users` and `countryName`. `users` have a value of `0`. Every time we find a country with more users than `0`, we update this value with the new amount of users and the `countryName` with the country that has that users. It is pretty much the same logic that we have used in finding out the longest email address. The `Northern Mariana Islands` is the country with the most users, which is `58` users.

## Summary

In this chapter, we have learned about the **faker** library, which allows us to generate massive amounts of fake data. The data that faker generates is not only fake but also random. We get a different result every time we run faker functions. This is sometimes not desirable. But computer-generated random data is not truly random. It is only **pseudo-random**. We can ensure that we get the same data each time using a **seed** function and a specific input to that function.

We have also learned many new JavaScript features. `break` is a keyword that allows us to exit a loop early. `slice` is a collection method that allows us to get a subsection of a string or an array. `indexOf` is another collection method that returns the index of the given item in that collection. `includes` is a method that checks to see if a given item exists or not in the collection.

We have used the data that we have generated to find answers to the questions we had about the data. Working with datasets that are like this is a very common task in computer programming.

# II Getting Started with Node.js

# 13 Introduction to Node.js

For the longest time, JavaScript has solely been the language of the web browser. That made it incredibly useful for building the **front-end** (user-facing side) of the websites, but that was the scope of its usage. When building web applications, developers frequently need to work outside of the browser to use file systems or databases. This required the developers to use different programming languages such as **Python**, **Ruby**, or **PHP** to achieve these tasks. This resulted in a fragmented developer experience where they had to jump in between many different technologies to develop web applications.

This has all changed with the introduction of **Node.js** in 2009\. Node.js is a programming environment to run JavaScript outside of the browser. In other words, it is a JavaScript **runtime**. Using Node.js, we can interact with the file system and do other kinds of things that were previously not possible to do with JavaScript. With the introduction of Node.s, JavaScript started to appear anywhere from web servers to desktop application development, wearables to robotics. A single developer that only knows JavaScript (alongside **HTML** and **CSS**) could suddenly develop an entire web application by themselves.

With Node.js, JavaScript became one of the most widely-used and flexible programming languages in the world.

In the rest of the book, we will explore some of the awesome things we can do with JavaScript in Node.js.

## Installing Node.js

There are a couple of ways of installing Node.js. One obvious way is to go to the official website at [https://nodejs.org/en/download/releases/](https://nodejs.org/en/download/releases/) and grab the installer for your operating system. We will be using version `14.15.5` for this book.

![](resources/i_imgur_com---60GROCw.png)

Installing Node.js like this is an acceptable way of doing it, but it presents some issues. Node.js has multiple versions available for download. Imagine having built a project using the current version of Node.js. Several months later, we want to start working on a new project, and we would like to use the latest version of Node.js that has fresh new features. If we are to update our Node.js, the old project might stop working if it is somehow not compatible with the new version.

This is not something that you might have to worry about as a beginner, but it is a real challenge for professional developers. **NVM** (**Node Version Manager**) is a package that solves this problem. You can find the installation instructions for it here: [https://github.com/nvm-sh/nvm](https://github.com/nvm-sh/nvm).

Feel free to choose whichever installation method you are more comfortable with. The problem that I have described above likely won’t be relevant to you if you are just beginning your programming journey.

## Using the Terminal

We will have to use the **terminal** (also known as the **command-line interface**) to run Node.js programs. The terminal is a way to interact with the computer using text commands. It is also the interface that you see when watching programmers hack security networks in Hollywood films. How you launch and work with the terminal varies with the operating system that you use. **Linux**, **macOS**, and **Windows** operating systems all have terminal access. I wrote this book on an Apple that uses a macOS operating system, so the terminal commands that I show might sometimes be specific to that operating system.

We can run the following command in the terminal to ensure that Node.js is installed properly on our system.

```
1 node -v
```

This command should display the version of Node.js that you have installed.

## Using a Code Editor

A **code editor** is basically a text editor that is specialized in writing code. It has features such as syntax and error highlighting, advanced search-replace and edit functionality, and extensibility using plugins. Code editors are incredibly useful when developing software. In theory, we can write our code in a plain text file and save it as a `.js` file, but using a code editor can help us become so much more efficient.

Just like how there are a lot of text editors out there, there are also a lot of code editors. **Sublime** and **Visual Studio Code** (**VS Code**) are some of the popular code editors. I am using Visual Studio Code, and I couldn’t be happier. I have also used Sublime in the past. It is not as feature-rich as VS Code, but it is still a great choice if you are just starting out.

![](resources/i_imgur_com---v9ozWZ9.png)

## Our First Node.js Program

Let’s write our first Node.js program. Create a folder in the operating system. We can create this folder either through the graphical interface of our operating system or using the terminal. The way to create a folder in the macOS terminal is by running the following command.

```
1 mkdir learning-nodejs
```

This command will create a folder called `learning-nodejs`. Then go into this folder. We can do so by running `cd learning-nodejs`.

Inside this folder, we will create a JavaScript file. We can create a file by using the terminal by running the `touch` command. Running `touch main.js` would create a file called `main.js` inside this folder.

At this point, we can launch this file using a **code editor** (We can use the UI for that).

```
1 console.log("Hello World");
```

We will `console.log` the string `"Hello World"` in this file to ensure everything is working. Let’s execute this file using Node.js inside the terminal by running `node main.js`

```
1 node main.js
```

We should see `Hello World` getting displayed on the terminal.

Congrats! You have written your first Node.js program!

## Summary

In this chapter, we have learned about Node.js, the runtime that allows us to run JavaScript outside of the web browser. Node.js unlocked a lot of new application domains for JavaScript and helped the language to proliferate. It is one of the biggest reasons why JavaScript is so prominent today.

Additionally, we have learned about installing Node.js. We have also learned about using the terminal (or the command line) on our computer and the benefits of using an editor for coding.

After all that setup, we have finally created our first Node.js program!

# 14 Modules

Everything that we have learned about using JavaScript also applies to using the language in the Node.js runtime. The primary difference that using JavaScript in Node.js makes is the access that it provides to the filesystem. Using Node.js, we can read and write from the filesystem, have access to the computer internals, and natively source other JavaScript files in our code.

A JavaScript file that we can source (**import**) in another file is called a **module**. Previously, we had to use an **HTML file** to load JavaScript files into the web browser environment. This is not the same as loading a file into another file. When we load multiple JavaScript files using HTML, we are loading them into a global context. This can create a mess because the variables defined in one file can clash with those in other files. It can be hard to know what is available in the context and what isn’t.

Imagine you are going out. You put your belongings into a bag. Whenever you need something, you know you need to reach into the bag to take it out. The bag creates a separation between the environment that you are in and your belongings. The outside world doesn’t know what is in the bag. This is an analogy for using modules. You are specifically taking out (**importing**) things from the bag to use them.

The HTML version of this example would be that your belongings are automatically in your surroundings wherever you go. They are all out there for everyone to see. You know they should be there, but there is no guarantee that nothing will happen to them. It is also messy. There is no separation between what belongs to you and what doesn’t.

We can use modules in Node.js to organize our code better. It also creates an abstraction just like functions do. We don’t know what is happening inside the module when we import it. We just need to know how to use the functionality that it exposes. A module, just like a function, hides its internals and exposes an interface for us to use instead.

## Using Modules in Node.js

A **module** is basically a JavaScript file that we can **import** into another JavaScript file. Node.js comes with a lot of **built-in modules**. A **built-in module** is a module that comes with the Node.js installation. There are also **third-party modules**. A third-party module is a module that other people create and publish online. These would be the **libraries** and **packages** that we have learned about earlier. Additionally, we can create our own modules.

### **Built-in Modules**

Node.js has built-in modules that enable us to do things like building a server, interfacing with the filesystem, or using cryptographic functions. We can **import** a module into a Node.js file by using the `require` function. We pass the module’s name to the `require` function when importing a built-in or a third-party module (also known as a **library**). For example, Node.js has a built-in module called `path`. Here is how we would import it.

```
1 const path = require("path");
```

`path` is a built-in module that has a bunch of methods related to file path operations. One of the methods it has is called `extname`. The `extname` method returns the **file extension** for the given file name.

```
1 const path = require("path");
2 
3 const fileName = "document.txt";
4 const fileExtension = path.extname(fileName);
5 console.log(fileExtension);
```

nodejs-02-modules/01.js

If we are to run this code, we will see that the `extname` method is returning `.txt`, which happens to be the file extension of the file name that we have provided. We will be using other built-in modules in the later chapters.

### **User Created Modules**

It is also possible to create our own modules. This helps us to organize our code better. Let’s create a file called `math.js` and define a bunch of math-related functions in there.

```
 1 function add(numbers) {
 2   let total = 0;
 3   numbers.forEach((number) => {
 4     total = total + number;
 5   });
 6 
 7   return total;
 8 }
 9 
10 function multiply(numbers) {
11   let total = 1;
12   numbers.forEach((number) => {
13     total = total * number;
14   });
15 
16   return total;
17 }
18 
19 function average(numbers) {
20   const total = add(numbers);
21   return total / numbers.length;
22 }
```

nodejs-02-modules/02.js

Here we have a couple of functions that operate on an array of numbers. As the name implies, the `add` function adds all those numbers together. `multiply` function multiplies them. The `average` function calculates the average value for them.

Now let’s create another file called `main.js`. We will have an array of numbers in this file.

```
1 const numbers = [1, 3, 5, 7, 9];
```

nodejs-02-modules/03.js

We want to add these numbers together. We have already defined a function that we can use for this purpose in another file (`math.js` file). We should **import** that file to have access to the functions it contains.

First, we **export** the `add` function from the `math.js` to use it inside the `main.js` file. We will add the following statement to the end of `math.js` to export the `add` function.

```
1 module.exports = add;
```

nodejs-02-modules/04/math.js

This statement makes this file export the `add` function. `math.js` file has now become a **module**. We can import it from other files. We will use the `require` function inside the `main.js` file to import `math.js`. Here is how to do that:

```
1 const add = require("./math");
2 
3 const numbers = [1, 3, 5, 7, 9];
4 
5 const total = add(numbers);
6 console.log(total);
```

nodejs-02-modules/04/main.js

We can import built-in modules and 3rd party modules by simply providing their name. But we need to provide a **relative file path** when importing the modules that we define. `./` signifies the current directory. If the `math.js` file were inside a directory called `misc`, then the `require` statement would have looked like this:

```
1 const add = require("./misc/math");
```

If the `math` file was inside the parent directory, then we could access it by using `..`.

```
1 const add = require("../math");
```

In our example, `require` function is instructed to look for the `math.js` file inside the current directory. Notice how we don’t have to provide the file extension to the `require` function. It already assumes that we are passing a JavaScript file to it.

We are currently exporting only one function from the `math` module. But `math` module has other useful functions as well. If we wanted to export multiple functions from a module, we would pass an object to the `module.exports` property.

```
1 module.exports = {
2   add: add,
3   multiply: multiply,
4   average: average,
5 };
```

nodejs-02-modules/05/math.js

Here we have an object where the **property names** (the **keys**) define the export names. And the corresponding values are the functions that we are exporting.

Since the property name and the function names match, we could write this in a shorter form.

```
1 module.exports = {
2   add,
3   multiply,
4   average,
5 };
```

nodejs-02-modules/06/math.js

Let’s import these values inside `main.js`.

```
 1 const math = require("./math");
 2 
 3 const add = math.add;
 4 const multiply = math.multiply;
 5 const average = math.average;
 6 
 7 const numbers = [1, 3, 5, 7, 9];
 8 
 9 const total = add(numbers);
10 const mult = multiply(numbers);
11 const avg = average(numbers);
12 
13 console.log(total, mult, avg);
```

nodejs-02-modules/05/main.js

As we can see, whatever we assign to the `module.exports` get returned from the `require` function. Here the `require` function is returning an object that has all those functions that we have exported. We can use the **object destructuring** syntax here to extract the object values easier.

```
 1 const math = require("./math");
 2 
 3 const { add, multiply, average } = math;
 4 
 5 const numbers = [1, 3, 5, 7, 9];
 6 
 7 const total = add(numbers);
 8 const mult = multiply(numbers);
 9 const avg = average(numbers);
10 
11 console.log(total, mult, avg);
```

nodejs-02-modules/06/main.js

Here the **object destructuring** syntax allows us to unpack the values of the `math` object easier.

```
1 const { add, multiply, average } = math;
```

**Object destructuring** is not an essential feature of the language but makes our code a bit more concise. Features like this are called **syntactic sugar**. They don’t change the functionality but make the language easier to read and write by making it more expressive. They make the language “sweeter” for us to use.

Using modules we were able to organize our code much better. `math.js` contains all the generic mathematical operation functions and the `main.js` uses that module to perform specific calculation.

## Summary

Modules are one of the primary things that set using JavaScript in Node.js apart from using it in the browser. We can use modules in Node.js to organize our code better.

In this chapter, we have learned about how to use built-in modules in Node.js by using the built-in `path` module. Node.js has a bunch of other modules that we will be learning more about later. We have also learned about building our own modules.

**Object destructuring** and the concept of syntactic sugar are two other things that we have learned about. They are not essential to know about but useful bits of knowledge.

# 15 Third-Party Modules and Libraries

We have learned about programming libraries before. **Programming libraries (or packages)** are **modules** that are previously written for a specific purpose that is packaged and shared for reusability.

We have also learned about **npm**. **npm** is a **package manager** and a **package registry** for JavaScript. **npm** stands for **Node Package Manage**r. It was originally developed for managing Node.js packages.

Npm gets installed on our system when we install Node.js**.** Run the following command in the terminal to make sure it is installed and working as expected:

```
1 npm -v
```

This should display the npm version that is installed.

We can use npm to install packages to our system easily. We have previously used the `faker` package in the browser. `faker` is a package that also runs on Node.js. Let’s install it using npm to start using it in our Node.js programs.

First, create a folder that will host the files that we will create in this chapter. We can think of this folder as our project folder. `mkdir` is the terminal command in macOS that creates a folder. `cd` is the command that allows us to navigate to the given folder path.

```
1 mkdir project-faker
2 cd project-faker
```

Next, we can install `faker` in this folder.

```
1 npm install faker@5.1.0
```

This installs version `5.1.0` of the `faker` library. We could also just run `npm install faker` and that would install whatever the latest version is. Here we are installing a specific version so that the examples in the book would still work as expected if anything changes with this package in the future.

Let’s create a file called `main.js`. We can also create files in the terminal. The command to do so in macOS is `touch`.

```
1 touch main.js
```

We can import `faker` in there and start using it.

```
 1 const faker = require("faker");
 2 
 3 function getPersonData() {
 4   const firstName = faker.name.firstName();
 5   const lastName = faker.name.lastName();
 6 
 7   const personalInformation = {
 8     firstName,
 9     lastName,
10   };
11 
12   return personalInformation;
13 }
14 
15 const person = getPersonData();
16 console.log(person);
```

nodejs-03-third-party-modules/01/main.js

The code is pretty much the same as what we had in the browser, except for the import step that is using the `require` function.

When we run the `npm install faker` command, the `faker` library got installed into a `./node_modules` folder. `node_modules` folder contains the packages that are installed for our project. We can think of these packages as the **dependencies** of the project. Our project **depends** on version `5.1.0` of the `faker` library to run properly.

If we wanted to share our project with someone else, we could send them our file alongside the `node_modules` folder, and they would have everything that they need to run our code. This would be highly inefficient, though. `node_modules` can have thousands of files in it and can be hundreds of megabytes in size. Thankfully, npm has a solution to help us keep track of the dependencies that our project relies on. We don’t have to send the **node_modules** folder to anyone if we wanted to share our project. We only need to share a list of dependencies for our project. npm can use this list to recreate the dependencies of the project. We can achieve this by using a file called `package.json`.

## Using package.json

**JSON** is a file format that is generally used to store human-readable data. It is commonly used with JavaScript, but it is language-independent. A lot of other programming languages also rely on it to store and transfer data.

`package.json` is a file that we can use to keep a list of the installed packages for our project. npm relies on the `package.json` file to determine the dependencies that are needed for running a project.

We could create a `package.json` file by running the `npm init` command.

Let’s run the `npm init` command in our projects folder. We will get asked a bunch of questions that will customize this file for our project. We can press enter to fill those fields with their default values.

Alternatively we can run `npm init -y` to create a `package.json` file with default values. This will skip the customization step. It is okay since we can always do this later.

Once we have the `package.json` file in place, we will rerun the faker installation, but this time with the `--save` **flag**. A **flag** is just a modifier for a terminal line command. Here `--save` flag will make this installation get logged in the `package.json` file.

```
1 npm install --save faker@5.1.0
```

Take a look at the `package.json` file. It should now have an entry for the installed package under the `dependencies` field.

```
1 "dependencies": {
2   "faker": "^5.1.0"
3 }
```

nodejs-03-third-party-modules/02/package.json

Notice that there is now a new file called `package-lock.json` in the current folder. This file keeps track of the **exact** version of a package that is installed for our project. The version number `^5.1.0` is just an approximation of the version that is required by the project. The **caret symbo**l (`^`) signals that minor version updates to this package are also acceptable. Even though we have specified to require version `5.1.0`, we might have received version `5.1.2`. In theory, as long as the first number between the versions is the same, then those two versions should be quite similar, so this usually doesn’t pose a problem. This versioning convention where the order of the numbers designates if the update is major or minor is called **semantic versioning**. We won’t delve too much into it here.

We now have a `package.json` file that keeps track of the dependencies of the project. We should always install packages using the `--save` flag. This will ensure that the packages get tracked in the `package.json` file. There is also the `--save-dev` flag but we don’t have to worry about it for the time being.

If we now wanted to transfer this project to somewhere else, we can go ahead and delete the `./node_modules` folder. Calling `npm install` in a folder where there is a `package.json` file will re-install every dependency required by this project. `package.json` and `package-lock.json` ensure the reproducibility of our project setup.

## Summary

In this chapter, we have revisited the concepts of **programming libraries** (**packages**) and **npm**. Npm is short for **Node Module Manager**. It allows us to install packages from the **npm registry**. It also helps us manage our project’s dependencies by keeping a list of the installed packages. It achieves this with the help of a file called `package.json`. We create a `package.json` file by running `npm init` command. Running `npm init` with the `--y` flag allows us to skip the customization step.

When we install a package using the `--save` flag, that installation gets recorded inside the `package.json` file. When we install a package using the `--save` flag, another file called `package-lock.json` gets created. This is a file that keeps track of the **exact versions** of the packages that are installed. The version that we have specified and the version that gets installed can sometimes differ. This divergence doesn’t cause a problem as long as the version change is not a major one. **Semantic versioning** helps us to understand if the difference between the two versions is minor or major.

The installed dependencies are stored inside a `./node_modules` folder. This folder gets recreated every time we run the `npm install` command.

# 16 **Project: Writing a Command-Line Tool**

We have been using the `console` object and the `console.log` function since we started to learn JavaScript. `console.log` could very well be one of the most used functions in JavaScript. Having said that, `console` is actually not a native part of the JavaScript language. It is an **object** that is provided by web browsers and Node.js. Node.js provides other **global objects** and **variables** that are similar to `console`. `__dirname` is one such **built-in global variable**. It is available in every Node.js program, and it stores the value of the current file path.

```
1 console.log(__dirname);
```

nodejs-04-project-command-line-tool/01.js

Another useful global object in Node.js is `process`. The `process` object is a global that provides information about the current Node.js process. We are interested in the `argv` method of the `process` object. The `argv` method captures the arguments that are passed into a Node.js program from the command-line when it is launched.

Let’s create a new folder for our project and create a new file inside that folder.

```
1 mkdir project-command-line-tool
2 touch main.js
```

We will display the value of the `process.argv` inside that new file.

```
1 console.log(process.argv);
```

nodejs-04-project-command-line-tool/02.js

This code displays an array of two items when executed using Node.js. The first item is the path for the Node.js installation and the second one is the path for the currently executed file.

The `process.argv` function starts getting interesting when we pass additional arguments to the file we are calling.

```
1 node main.js firstName=John lastName=Doe
```

`process.argv` captures the additional arguments we pass into this file from the terminal. We can use these arguments inside our file to customize our program’s behavior with the user input. That allows us to create flexible C**ommand-Line applications**. Command-Line applications (**CLI’s** in short) are programs that are controlled through the terminal.

## Building a Number Guessing Game

In this project, we will build a CLI game that generates a random number in the desired range of numbers and prompts the user to guess the number. The game should end when the user correctly guesses the number or fails to do so after a fixed number of attempts.

We can use the `Math.random` function to create a number in between 0 (inclusive) and 1 (exclusive). If we want to use 10 numbers for our game, we can multiply the result of `Math.random()` with `10`.

```
1 const randomNumber = Math.random();
2 const scaledRandomNumber = randomNumber * 10;
3 console.log(scaledRandomNumber);
```

nodejs-04-project-command-line-tool/03.js

These generated numbers are currently impossible to guess. We need to convert them into whole numbers. The result of a `Math.random` operation can be `0` but can not be `1`. We will round up the resulting numbers (using `Math.ceil` function) so that they will be in between `0` and `10`. We don’t want to have a `0` value in our game though. So if the result is ever `0` we will return `1`.

```
1 const randomNumber = Math.random() + 0.1;
2 let scaledRandomNumber = Math.ceil(randomNumber * 10);
3 if (scaledRandomNumber === 0) {
4   scaledRandomNumber = 1;
5 }
6 console.log(scaledRandomNumber);
```

nodejs-04-project-command-line-tool/04.js

We should put this random number generating logic into a function.

```
 1 function getRandomNumber(upperLimit = 10) {
 2   const randomNumber = Math.random() + 0.1;
 3   let scaledRandomNumber = Math.ceil(randomNumber * upperLimit);
 4   if (scaledRandomNumber === 0) {
 5     scaledRandomNumber = 1;
 6   }
 7 
 8   return scaledRandomNumber;
 9 }
10 
11 function main() {
12   const randomNumber = getRandomNumber();
13   console.log(randomNumber);
14 }
15 
16 main();
```

nodejs-04-project-command-line-tool/05.js

## Getting the Command Line Arguments

Let’s make it so that the `upperLimit` value of the `getRandomNumber` can be controlled from outside this program. We will make use of `process.argv` to capture user input from the terminal and pass that input to the `getRandomNumber` function. Let’s create a function called `getCommandLineInputs`.

```
1 function getCommandLineArguments() {
2   const arguments = process.argv.slice(2, process.argv.length);
3   return arguments;
4 }
```

nodejs-04-project-command-line-tool/06.js

`process.argv` is an array. We are not interested in the first two values of this array. Here we are using the `slice` method to capture the array items starting from the index position `2` up until the length of the array. This will give us the arguments passed into the Node.js file when it is called in the terminal.

Let’s make it so that if the user passes an argument that has the name of `upperLimit`, our program will extract the value of that argument.

```
 1 function getProcessedArguments() {
 2   const userArguments = getCommandLineArguments();
 3   const processedArguments = {};
 4 
 5   userArguments.forEach((arg) => {
 6     const argArray = arg.split("=");
 7     const [argKey, argValue] = argArray;
 8 
 9     if (argValue) {
10       processedArguments[argKey] = argValue;
11     }
12   });
13 
14   return processedArguments;
15 }
```

nodejs-04-project-command-line-tool/07.js

We created a function called `getProcessedArguments`. `getProcessedArguments` uses the `getCommandLineArguments` function to get the user-provided arguments. It goes through each argument in the `userArguments` array. It uses the `split` method to create an array from the current item. The `split` method creates an array from a string by splitting the string whenever there is a match to the given input. Here are some examples of how it works:

```
 1 const name = "John Doe";
 2 const email = "john.doe@gmail.com";
 3 const city = "Vancouver";
 4 const favoriteNumbers = "1,3,7,19,42";
 5 const date = "2/2/2222";
 6 
 7 const nameArr = name.split(" ");
 8 const nameArr2 = name.split(".");
 9 const emailArr = email.split("@");
10 const cityArr = city.split("");
11 const favoriteNumbersArr = favoriteNumbers.split(",");
12 const dateArr = date.split("/");
13 
14 console.log(nameArr); // [ 'John', 'Doe' ]
15 console.log(nameArr2); // [ 'John Doe' ]
16 console.log(emailArr); // [ 'john.doe', 'gmail.com' ]
17 console.log(cityArr); // [ 'V', 'a', 'n', 'c', 'o', 'u', 'v', 'e', 'r' ]
18 console.log(favoriteNumbersArr); // [ '1', '3', '7', '19', '42' ]
19 console.log(dateArr); // [ '2', '2', '2222' ]
```

nodejs-04-project-command-line-tool/08.js

Calling `"2/2/2222".split("/")` creates an array from the string where there is a new item whenever there is a match to the given input, `/` in the case.

`"John Doe".split(".")` results in an array with a single item because the `"."` character doesn’t appear in the string. There is no split to be done.

When we call `split` with an empty string (a string that has no characters in it `""`) it splits every character.

In our code, we are using the `arg.split("=");` to split the given argument if it has a `=` in it. There won’t be any split if no character matches the `=` symbol. We are then using **array destructuring** to get the first and the second items of the resulting array.

```
1 const argArray = arg.split("=");
2 const [argKey, argValue] = argArray;
```

nodejs-04-project-command-line-tool/07.js

**Array destructruring** is another **syntactic sugar** just like **object destructuring**. It is a shorthand way of doing this:

```
1 const argKey = argArray[0];
2 const argValue = argValue[1];
```

We then check to see if the `argValue` exists. If it does, we save it under the `argKey` name in the initially empty `processedArguments` object.

```
 1 function getProcessedArguments() {
 2   const userArguments = getCommandLineArguments();
 3   const processedArguments = {};
 4 
 5   userArguments.forEach((arg) => {
 6     const argArray = arg.split("=");
 7     const [argKey, argValue] = argArray;
 8 
 9     if (argValue) {
10       processedArguments[argKey] = argValue;
11     }
12   });
13 
14   return processedArguments;
15 }
```

nodejs-04-project-command-line-tool/07.js

This is what full code looks like:

```
 1 function getProcessedArguments() {
 2   const userArguments = getCommandLineArguments();
 3   const processedArguments = {};
 4 
 5   userArguments.forEach((arg) => {
 6     const argArray = arg.split("=");
 7     const [argKey, argValue] = argArray;
 8 
 9     if (argValue) {
10       processedArguments[argKey] = argValue;
11     }
12   });
13 
14   return processedArguments;
15 }
16 
17 function getCommandLineArguments() {
18   const arguments = process.argv.slice(2, process.argv.length);
19   return arguments;
20 }
21 
22 const processedArguments = getProcessedArguments();
23 console.log(processedArguments);
```

nodejs-04-project-command-line-tool/07.js

Let’s call this file with below arguments.

```
1 node 07.js amount=10 upperLimit=20 attempts 3
```

The result would be equivalent to `{ amount: '10', upperLimit: '20' }`. Our program ignores the arguments that don’t have a `=` character in them.

We can have all this logic for processing arguments inside our main file, but it would be much better if they were in a different file for organizational purposes. This is where **modules** are incredibly beneficial. Let’s create a file called `arguments.js` and export these functions from there.

```
 1 function getProcessedArguments() {
 2   const userArguments = getCommandLineArguments();
 3 
 4   const processedArguments = {};
 5 
 6   userArguments.forEach((arg) => {
 7     const argArray = arg.split("=");
 8     const [argKey, argValue] = argArray;
 9 
10     if (argValue) {
11       processedArguments[argKey] = argValue;
12     }
13   });
14 
15   return processedArguments;
16 }
17 
18 function getCommandLineArguments() {
19   const arguments = process.argv.slice(2, process.argv.length);
20   return arguments;
21 }
22 
23 module.exports = {
24   getProcessedArguments,
25 };
```

nodejs-04-project-command-line-tool/09/arguments.js

We are now exporting the `getProcessedArguments` from this file. We can do the same thing for our random number generating function. Let’s create a module called `random.js` and export the `getRandomNumber` function from there. We will update the `getRandomNumber` function to ensure the `upperLimit` value is a **number** by calling the `parseInt` function. This will be useful when we start passing the command-line arguments, that are strings, into this function.

```
 1 function getRandomNumber(upperLimit = 10) {
 2   const randomNumber = Math.random() + 0.1;
 3   let scaledRandomNumber = Math.ceil(randomNumber * parseInt(upperLimit));
 4   if (scaledRandomNumber === 0) {
 5     scaledRandomNumber = 1;
 6   }
 7 
 8   return scaledRandomNumber;
 9 }
10 
11 module.exports = {
12   getRandomNumber,
13 };
```

nodejs-04-project-command-line-tool/09/random.js

Let’s import these functions into our main file.

```
 1 const { getProcessedArguments } = require("./arguments");
 2 const { getRandomNumber } = require("./random");
 3 
 4 function main() {
 5   const arguments = getProcessedArguments();
 6   const upperLimit = arguments.upperLimit;
 7 
 8   const randomNumber = getRandomNumber(upperLimit);
 9   console.log(randomNumber);
10 }
11 
12 main();
```

nodejs-04-project-command-line-tool/09/main.js

We are getting all the arguments that are passed into the file by calling `getProcessedArguments`. We are then getting the `upperLimit` property and then pass it into the `getRandomNumber` function. Now we can set the random number range from the command line when we execute this file!

```
1 node main.js upperLimit=1000
```

Number range would be equivalent to `10` if we don’t set the `upperLimit` argument.

## Capturing the User Input

Now that we can generate a random number in the desired range, we should interactively get the user input. We will ask the user to provide a number, and we will check to see if the provided number matches the generated random number.

We will be using a third-party library called `readline-sync` for interactively getting the user input.

We need to create a `package.json` file before installing any external libraries. Run `npm init -y` to create a `package.json` file.

```
1 npm init -y
```

Now that the `package.json` is created, install the `readline-sync` library by running the below command.

```
1 npm install --save readline-sync@1.4.10
```

Let’s import this library into our main file and start using it.

```
 1 const readlineSync = require("readline-sync");
 2 const { getProcessedArguments } = require("./arguments");
 3 const { getRandomNumber } = require("./random");
 4 
 5 function main() {
 6   const arguments = getProcessedArguments();
 7   const upperLimit = arguments.upperLimit;
 8 
 9   const randomNumber = getRandomNumber(upperLimit);
10   let userNumber = readlineSync.question("Guess the number! ");
11   userNumber = parseInt(userNumber);
12 
13   const success = userNumber === randomNumber;
14   if (success) {
15     console.log("Success. You won!");
16   } else {
17     console.log(
18       `Nope! You have guessed ${userNumber}.
19 The generated number was ${randomNumber}.`
20     );
21   }
22 }
23 
24 main();
```

nodejs-04-project-command-line-tool/10/main.js

We are importing the library on the first line.

```
1 const readlineSync = require("readline-sync");
```

nodejs-04-project-command-line-tool/10/main.js

We are then using the library’s `question` method to display a message to the user and capture their command-line input.

```
1 let userNumber = readlineSync.question("Guess the number! ");
```

nodejs-04-project-command-line-tool/10/main.js

The `question` method allows us to capture the command line input and store it inside the `userNumber` variable. We are then converting this variable into a `number` by using the `parseInt` function.

```
1 let userNumber = readlineSync.question("Guess the number! ");
2 userNumber = parseInt(userNumber);
```

nodejs-04-project-command-line-tool/10/main.js

We are then checking to see if the provided number matches the generated number. We display a message according to the result.

```
1 const success = userNumber === randomNumber;
2 if (success) {
3   console.log("Success. You won!");
4 } else {
5   console.log(
6     `Nope! You have guessed ${userNumber}.
7 The generated number was ${randomNumber}.`
8   );
9 }
```

nodejs-04-project-command-line-tool/10/main.js

This is the core logic of our game. The only thing that remains to be implemented is to create a game loop so that the user can take multiple guesses.

## Creating the Game Loop

Notice how Node.js programs we wrote so far just exit after they complete. This is a pretty common behavior in command-line applications. There are a lot of applications that don’t behave this way, though. When using an application with a graphical interface, the application generally doesn’t terminate unless we close it. The same applies to computer games as well. This is because they are running in a loop that doesn’t terminate unless we explicitly quit (or there is a critical error). We can achieve similar behavior in our application by using a `while` loop.

```
 1 const readlineSync = require("readline-sync");
 2 const { getProcessedArguments } = require("./arguments");
 3 const { getRandomNumber } = require("./random");
 4 
 5 function main() {
 6   const arguments = getProcessedArguments();
 7   const upperLimit = arguments.upperLimit;
 8 
 9   const randomNumber = getRandomNumber(upperLimit);
10 
11   const rounds = 3;
12   let currentRound = 1;
13   while (currentRound <= rounds) {
14     let userNumber = readlineSync.question("Guess the number! ");
15     userNumber = parseInt(userNumber);
16 
17     const success = userNumber === randomNumber;
18     if (success) {
19       console.log("Success. You won!");
20       return;
21     } else {
22       console.log(`Nope!`);
23     }
24 
25     currentRound = currentRound + 1;
26   }
27 
28   console.log(`Nope! The generated number was ${randomNumber}.`);
29 }
30 
31 main();
```

nodejs-04-project-command-line-tool/11/main.js

We have created a variable called `rounds` that define the number of rounds allowed in the game. We also have a variable called `currentRound` that defines the current round. We then created a `while` **loop** that runs while the `currentRound` number is less **than or equal** to the `rounds` value. At the end of every loop, we iterate the `currentRound` by `1`. If the user ever guesses the correct number, we display a `success` message, and we **return** from the function to terminate the loop early.

```
 1 const rounds = 3;
 2 let currentRound = 1;
 3 while (currentRound <= rounds) {
 4   let userNumber = readlineSync.question("Guess the number! ");
 5   userNumber = parseInt(userNumber);
 6 
 7   const success = userNumber === randomNumber;
 8   if (success) {
 9     console.log("Success. You won!");
10     return;
11   } else {
12     console.log(`Nope!`);
13   }
14 
15   currentRound = currentRound + 1;
16 }
```

nodejs-04-project-command-line-tool/11/main.js

That’s pretty much it! One other thing we can do is to accept user input for the `rounds` value as well.

```
 1 const readlineSync = require("readline-sync");
 2 const { getProcessedArguments } = require("./arguments");
 3 const { getRandomNumber } = require("./random");
 4 
 5 function main() {
 6   const arguments = getProcessedArguments();
 7   const upperLimit = arguments.upperLimit;
 8   const rounds = arguments.rounds || 3;
 9 
10   const randomNumber = getRandomNumber(upperLimit);
11 
12   let currentRound = 1;
13   while (currentRound <= rounds) {
14     let userNumber = readlineSync.question("Guess the number! ");
15     userNumber = parseInt(userNumber);
16 
17     const success = userNumber === randomNumber;
18     if (success) {
19       console.log("Success. You won!");
20       return;
21     } else {
22       console.log(`Nope!`);
23     }
24 
25     currentRound = currentRound + 1;
26   }
27 
28   console.log(`Nope! The generated number was ${randomNumber}.`);
29 }
30 
31 main();
```

nodejs-04-project-command-line-tool/12/main.js

We have added the line `const rounds = arguments.rounds || 3` that allows the user set the number of rounds from the command line. If the received value is empty, the `rounds` gets the default value of `3`.

Our program is finished, but we could keep improving it. For example, the program would break if the user were to provide non-numerical values as command-line arguments. We could add some logic to handle those invalid values. We could also add more features like hinting at the user if they are getting close to the result or moving away from it.

## Summary

In this chapter, we have learned about the built-in globals in the Node.js runtime. We have focused on `process.argv` method that provides us the command-line arguments passed into a Node.js program. Using these arguments allows us to write **Command-Line Applications**.

We have used the `Math.random` function to create random numbers. `Math.ceil` function allowed us to convert these generated numbers into whole numbers. We have also used the `slice` methods of arrays to get the desired items from the `argv` array. The `split` method of strings helps us to generate arrays from strings.

We have also learned about **Array destructruring** which is another **syntactic sugar** just like **object destructuring**.

We have installed a third-party library called `readline-sync` to be able to capture the user input from the terminal interactively.

Finally, we have created a game loop using the while structure. The loop runs for the number of rounds that are defined or until the user finds the right answer.

# III Interacting with the File System in Node.js

# 17 Working with Folders

One of the most common and practical operations that you could perform while working with JavaScript in Node.js is interacting with files and folders on your file system. Think of actions such as creating a folder (directory), creating a file, and reading a file.

There are two ways of interacting with the operating system when using Node.js.

*   One of them is synchronously.
*   And the other one is asynchronously.

We will start by looking at how things work synchronously and then see the difference between these two modes down the line.

## Performing Folder Operations

### Create a Folder if it Does Not Exist

Let’s start by looking at how to perform certain folder operations in Node.js.

We will begin by manually creating a new folder for our project and, inside that folder, create a file called `main.js`.

```
1 mkdir filesystem
2 cd filesystem
3 touch main.js
```

You could perform these operations using the file explorer of your system, but here they are being done through the terminal. By the end of this introduction, you will be able to manipulate the file system programmatically using JavaScript!

Let’s dive into the `main.js` file that we have created. We will first learn how to create a folder programmatically. We will import the `fs` module, which contains a bunch of functions for file system operations. We will call the `mkdirSync` function from the `fs` module to create a folder at the given path. As the `Sync` suffix suggests, this function **makes** a folder **synchronously**.

```
1 const fs = require("fs");
2 
3 const folderPath = "myFolder";
4 
5 fs.mkdirSync(folderPath);
```

filesystem-01-working-with-folders/01.js

We can run the code in this file by typing `node main.js` in the terminal. If you didn’t get any messages in the terminal, it means that the code has been successfully executed. You should be able to see the newly created folder.

We will notice that if we tried to rerun this code, it would fail with an error because the folder that we are trying to create already exists on the same path.

Let’s add some code to check to see if the folder exists first. We will be using the `existsSync` function to do that. `existsSync` function checks to see if a file or a folder exists on the given path.

```
1 const fs = require("fs");
2 
3 const folderPath = "myFolder";
4 
5 const folderExists = fs.existsSync(folderPath);
6 console.log(folderExists);
```

filesystem-01-working-with-folders/02.js

Let’s run this program now. It logs the value `true` if the folder exists and `false` if not.

Using this knowledge, we can update our code to create the folder only if it exists using an `if-else` statement.

```
 1 const fs = require("fs");
 2 
 3 const folderPath = "myFolder";
 4 
 5 const folderExists = fs.existsSync(folderPath);
 6 if (!folderExists) {
 7   fs.mkdirSync(folderPath);
 8 } else {
 9   console.log("Folder exists");
10 }
```

filesystem-01-working-with-folders/03.js

Notice how we are making use of variable names that are very easy to understand. Also, notice how we use a positive variable name instead of a negative one as in `folderExists` and not `folderDoesNotExist`. When naming variables, we generally want to avoid using negative names, as negating a negative name can make it hard to understand. Check this example here:

```
1 if (!folderExists)
```

It is easier to understand that we are negating the `folderExists` variable to imply that the folder does not exist. But if the variable name was like this:

```
1 if (!folderDoesNotExist)
```

It becomes harder to think of this variable name when it is negated due to the double negative.

### Create a Folder Relative to the Destination File Path

Let’s wrap the current functionality we have inside a `createFolder` function.

```
 1 const fs = require("fs");
 2 
 3 const targetPath = "myFolder";
 4 
 5 const createFolder = (folderPath) => {
 6   const folderExists = fs.existsSync(folderPath);
 7   if (!folderExists) {
 8     fs.mkdirSync(folderPath);
 9     return true;
10   } else {
11     console.log("Folder exists");
12   }
13 
14   return false;
15 };
16 
17 createFolder(targetPath);
```

filesystem-01-working-with-folders/04.js

Whenever we call the `createFolder` function, we would either create a folder or not, depending on if a folder with the given name already exists at the destination that we are trying to create the folder.

The reason to return `true` or `false` from this function is to know if the function is completed successfully or not. We can safely assume that the function ended up creating a folder if it returns a `true` value. Returning a boolean value like this is not something essential to do but can be useful at times.

If we are to go into the `myFolder` directory and try to run the script from here using a relative path, we will notice that the script creates a folder in the folder that we ran the script from.

```
1 cd myFolder
2 
3 node ../main.js
```

This behavior might not be desirable. We might want the script to create a folder at the same spot every time that it runs. To ensure that, we can use the `__dirname` global variable available to every Node.js program.

Let’s first see the value of `__dirname` by logging it in the console.

```
1 console.log(__dirname);
```

As we can see by executing this line of code in our file, the `__dirname` variable is logging the folder that the script is in regardless of where we run the code from.

Let’s make use of this variable in our code.

```
 1 const fs = require("fs");
 2 
 3 const folderName = "myFolder";
 4 const targetPath = `${__dirname}/${folderName}`;
 5 
 6 const createFolder = (folderPath) => {
 7   console.log(`Creating a folder at: ${folderPath}`);
 8 
 9   const folderExists = fs.existsSync(folderPath);
10   if (!folderExists) {
11     fs.mkdirSync(folderPath);
12     console.log("Success!");
13     return true;
14   } else {
15     console.log("Folder already exists");
16   }
17 
18   return false;
19 };
20 
21 createFolder(targetPath);
```

filesystem-01-working-with-folders/05.js

Using the `__dirname` variable, our code is now creating a folder in the same directory as the source script every time it runs.

Notice how we are constructing the folder in the previous example by using **template literals**.

```
1 const targetPath = `${__dirname}/${folderName}`;
```

filesystem-01-working-with-folders/05.js

We could have used the addition operator to construct a string, but template literals are more readable as they don’t break the text flow. The same result using the addition operator would have looked like this:

```
1 const TARGET_PATH = __dirname + "/" + FOLDER_NAME;
```

This is not too hard to read in this example, but it can quickly get unwieldy for longer strings.

There is a slight problem with constructing folders in this manner. Different operating systems (like Windows or Mac) might have that slash symbol pointing to backward or forwards, so our code when using a forward slash might fail in other operating systems.

A function called `join` that lives under the `path` module can help with **normalizing** the constructed path for us. Normalizing in this context means it would construct a path that would work regardless of the operating system. Using the `join` function, we could construct the same path by doing this:

```
1 const path = require("path");
2 const TARGET_PATH = path.join(__dirname, FOLDER_NAME);
```

This is the final code that makes use of the `path.join` function.

```
 1 const fs = require("fs");
 2 const path = require("path");
 3 
 4 const folderName = "myFolder";
 5 const targetPath = path.join(__dirname, folderName);
 6 
 7 const createFolder = (folderPath) => {
 8   console.log(`Creating a folder at: ${folderPath}`);
 9 
10   const folderExists = fs.existsSync(folderPath);
11   if (!folderExists) {
12     fs.mkdirSync(folderPath);
13     console.log("Success!");
14     return true;
15   } else {
16     console.log("Folder already exists");
17   }
18 
19   return false;
20 };
21 
22 createFolder(targetPath);
```

filesystem-01-working-with-folders/06.js

This function is at a pretty good spot right now. Programmatically creating a single folder might not look like a big deal, given we had to write a bunch of lines of code to achieve this. You might be thinking that doing all this manually could have been much easier. The great thing about doing things programmatically is that once you have created a function like this, there is not much difference in executing it once to create a single folder versus executing it to create thousands of folders. That’s the beauty of programming. It gives you a ton of leverage.

Let’s adjust our code a little bit to create as many folders as we would like.

### Create Multiple Folders

```
 1 const fs = require("fs");
 2 const path = require("path");
 3 
 4 const createFolder = (folderPath) => {
 5   console.log(`Creating a folder at: ${folderPath}`);
 6 
 7   const folderExists = fs.existsSync(folderPath);
 8   if (!folderExists) {
 9     fs.mkdirSync(folderPath);
10     console.log("Success!");
11     return true;
12   } else {
13     console.log("Folder already exists");
14   }
15 
16   return false;
17 };
18 
19 const main = () => {
20   const parentFolderName = "myFolder";
21   const parentFolderPath = path.join(__dirname, parentFolderName);
22 
23   const childFolderPrefix = "subFolder_";
24   const childFolderAmount = 10;
25 
26   createFolder(parentFolderPath);
27   for (let i = 0; i < childFolderAmount; i++) {
28     const childFolderPath = path.join(
29       __dirname,
30       parentFolderName,
31       `${childFolderPrefix}${i}`
32     );
33     createFolder(childFolderPath);
34   }
35 };
36 
37 main();
```

filesystem-01-working-with-folders/07.js

We first call the `createFolder` function to create a parent folder containing all the other child folders. And then, we call the `createFolder` function again inside a `for` loop to create the child folders (still using the `parentFolderName` while constructing the path) where the amount of child folders is determined by the `childFolderAmount` variable.

```
 1 const childFolderPrefix = "subFolder_";
 2 const childFolderAmount = 10;
 3 
 4 createFolder(parentFolderPath);
 5 for (let i = 0; i < childFolderAmount; i++) {
 6   const childFolderPath = path.join(
 7     __dirname,
 8     parentFolderName,
 9     `${childFolderPrefix}${i}`
10   );
11   createFolder(childFolderPath);
12 }
```

filesystem-01-working-with-folders/07.js

We can make small improvements to this code. One thing that comes to mind is that extracting the `createFolder` function from this file into a module. Given how useful the `createFolder` function is, it might make sense to extract it into a separate file to access it from other files if we ever wanted to. This is entirely redundant for our current purposes, but it is a good practice for our learning.

The benefit of extracting the `createFolder` function to its file is that we can completely ignore the implementation details of this function going forward. We can assume it works as intended and not worry about the inner workings of it. It will help declutter our code and make it easier to read and understand.

Let’s create a file called `utilities.js` and place the `createFolder` function in there.

```
 1 const fs = require("fs");
 2 
 3 const createFolder = (folderPath) => {
 4   console.log(`Creating a folder at: ${folderPath}`);
 5 
 6   const folderExists = fs.existsSync(folderPath);
 7   if (!folderExists) {
 8     fs.mkdirSync(folderPath);
 9     console.log("Success!");
10     return true;
11   } else {
12     console.log("Folder already exists");
13   }
14 
15   return false;
16 };
17 
18 module.exports = {
19   createFolder,
20 };
```

filesystem-01-working-with-folders/utilities.js

Notice how we are using the `module.exports` syntax to export the `createFolder` function. This is the pattern to use whenever we are exporting content from a file.

We will import this function in our `main.js` file.

```
 1 const path = require("path");
 2 const { createFolder } = require("./utilities");
 3 
 4 const main = () => {
 5   const parentFolderName = "myFolder";
 6   const parentFolderPath = path.join(__dirname, parentFolderName);
 7 
 8   const childFolderPrefix = "subFolder_";
 9   const childFolderAmount = 10;
10 
11   createFolder(parentFolderPath);
12   for (let i = 0; i < childFolderAmount; i++) {
13     const childFolderPath = path.join(
14       __dirname,
15       parentFolderName,
16       `${childFolderPrefix}${i}`
17     );
18     createFolder(childFolderPath);
19   }
20 };
21 
22 main();
```

filesystem-01-working-with-folders/08.js

Notice the `main.js` looks much smaller now that we are using a module to contain a piece of functionality that can exist separately in a different file. Using modules will make our code easier to read and maintain.

Let’s write another useful script before wrapping up this section. What if we wanted to create folders based on some predefined names? Say we wanted to create a folder called `project` and inside that folder have some subfolders called `assets`, `output`, and `plugins`. Our current script only creates folders with the given prefix. Here is what our script could look like if we wanted to accommodate custom file names:

```
 1 const path = require("path");
 2 const { createFolder } = require("./utilities");
 3 
 4 const main = () => {
 5   const parentFolderName = "project";
 6   const subFolderNames = ["assets", "output", "plugins"];
 7 
 8   const parentFolderPath = path.join(__dirname, parentFolderName);
 9   createFolder(parentFolderPath);
10 
11   subFolderNames.forEach((folderName) => {
12     const folderPath = path.join(__dirname, parentFolderName, folderName);
13     createFolder(folderPath);
14   });
15 };
16 
17 main();
```

filesystem-01-working-with-folders/09.js

Of course, we could also create another function that performs this functionality of creating a folder and subfolders for us if we wanted to take this a step further.

## Summary

We learned about how to work with folders **synchronously** using Node.js. We have used the `fs.existsSync` and `fs.mkdirSync` functions to check if a folder exists and create the folder if it doesn’t. We have also learned about some useful things to keep in mind when programming, such as:

*   Refraining from using negative variable names
*   Using modules to encapsulate functionality.

Avoiding negative variable names would help us write programs that are easier to read and maintain. Using modules to abstract away and encapsulate functionality is one of the most important principles that we can follow when building software.

We have also used loops to create as many folders as we would like and create folders from a given array of names. Once we have a loop that creates a single folder, we can scale that loop to create thousands of folders. This is a great example to the scalability of computer programs.

# 18 Reading and Writing Files

We can use Node.js to create/write files and read data from them.

When we write data to a file, the file ends up getting created if it doesn’t already exist. That’s why we are using the words **writing** and **creating** interchangeably. We will first be using the `writeFileSync` function to write data to a file in a synchronous way.

```
1 const fs = require("fs");
2 
3 const filePath = "temp.txt";
4 const fileData = "hello world";
5 
6 fs.writeFileSync(filePath, fileData);
```

filesystem-02-reading-and-writing-files/01.js

When we run this program, we create a file called `temp.txt` with the content `hello world`. Notice that rerunning this program doesn’t result in any errors. We end up overwriting the content of the previous file.

Let’s now look into reading files. For this purpose, we will be using the `readFileSync` function.

```
1 const fs = require("fs");
2 
3 const filePath = "temp.txt";
4 
5 const data = fs.readFileSync(filePath);
6 console.log(data);
```

filesystem-02-reading-and-writing-files/02.js

This program would read the contents of the `temp.txt`, assuming that a file with that name exists in the current folder. The result that we are getting from this operation is not in the form that we might have expected. We are receiving something called a `Buffer` that looks like this:

```
1 <Buffer 68 65 6c 6c 6f 20 77 6f 72 6c 64>
```

To get the result of this operation as a string of text instead of a string of a `Buffer`, we need to specify an encoding value of `utf8` to the `readFileSync` function. Encoding value defines how we want the content of this file to be interpreted. We are working with a text file, so the `utf8` encoding value helps us to interpret the content as such.

```
1 const fs = require("fs");
2 
3 const filePath = "temp.txt";
4 
5 const data = fs.readFileSync(filePath, "utf8");
6 console.log(data);
```

filesystem-02-reading-and-writing-files/03.js

Now we are getting the content of the file as a string of text. This function would throw an error if the file we are trying to read from didn’t exist. We could first check to see if the file exists just like we did when working with folders, but a better way of doing it is just trying to do the operation anyway and **catch** the error if it happens. We can achieve this by using a JavaScript structure called **try…catch**.

## Error Handling in JavaScript

**try…catch** is a built-in JavaScript structure much like **if-else** that allows us to **handle** an error if it happens.

To explore how this works, let’s first examine how to **throw** an error in JavaScript. We could do so by using the `throw` statement.

```
1 throw "42";
```

`throw` statement throws an error with the given value. In this case, the error we throw will have the value of the string `42`.

There is a built-in JavaScript object called `Error` object that we can use to define our errors. This code below creates an `Error` object with the given string as the error message.

```
1 const message = "This is the error message";
2 const error = new Error(message);
3 console.log(error.message);
4 
5 throw error;
6 
7 console.log("End of Program");
```

filesystem-02-reading-and-writing-files/04.js

As we can see, we can access the string value that we pass into the `Error` object during the creation through the `Error` object’s `message` property. This value can be seen on the screen when the error is thrown.

Note that the rest of the program does not get executed after an error is encountered. The program exits immediately if there is an **unhandled** error. We can **handle** errors using the **try…catch** structure.

Let’s see how **try…catch** works now that we know how to create error conditions deliberately.

```
1 const genericError = new Error("Something went wrong");
2 
3 try {
4   throw genericError;
5 } catch (errorObj) {
6   console.log(errorObj);
7 }
8 
9 console.log("End of program");
```

filesystem-02-reading-and-writing-files/05.js

Here in this example, we are defining a generic error and deliberately throwing that error inside the `try` block of the **try…catch** structure. The `catch` block that comes after the `try` receives the `error` object and lets us do whatever we would like to do with it. Here we have chosen to handle the error by **console.logging** it instead of **throwing** that error. This way, we can see that an error has happened but not let it take our program down. We can verify that the program continues to function until the end since we see the final `console.log` message displayed on the screen.

Let’s use **try…catch** statements to update our previous code.

## Reading Files with Error Handling

Previously we had this program read the contents of a file, but it would crash if the target file didn’t exist.

```
1 const fs = require("fs");
2 
3 const filePath = "temp.txt";
4 
5 const data = fs.readFileSync(filePath, "utf8");
6 console.log(data);
```

filesystem-02-reading-and-writing-files/03.js

Let’s update our code so that we can handle the error that gets thrown if the file does not exist.

```
 1 const fs = require("fs");
 2 
 3 const readFileSync = (filePath) => {
 4   try {
 5     const data = fs.readFileSync(filePath, "utf8");
 6     return data;
 7   } catch (err) {
 8     console.log("Something went wrong");
 9     console.log(err);
10   }
11 
12   return null;
13 };
14 
15 const main = () => {
16   const filePath = "temp.txt";
17   const data = readFileSync(filePath);
18   console.log("Data contained in the file is:");
19   console.log(data);
20 };
21 
22 main();
```

filesystem-02-reading-and-writing-files/06.js

First, we are wrapping the `readFile` functionality inside a function to make it a bit more readable and reusable. Then inside this function, we are using the **try…catch** block. We return the content of a target file if we can read that file without any errors. In case there are any errors, we return a `null` value from this function.

```
 1 const readFileSync = (filePath) => {
 2   try {
 3     const data = fs.readFileSync(filePath, "utf8");
 4     return data;
 5   } catch (err) {
 6     console.log("Something went wrong");
 7     console.log(err);
 8   }
 9 
10   return null;
11 };
```

filesystem-02-reading-and-writing-files/06.js

We are then creating a function called `main` to contain the main body of operations that we will be executing. Inside the `main` function, we are making use of this `readFile` function to read the file’s contents at the given path. We then log the contents to the screen with a descriptive text at the beginning.

Error handling is an essential aspect of writing resilient programs. **try…catch** is a powerful structure in JavaScript that allows us to handle errors in ways that suits our purposes. When we are writing a program, sometimes we want to throw an error and cause a crash since we might be operating in an environment that doesn’t tolerate any errors. For example, if we have a program that handles business transactions, it might be better to stop the program from executing than to have it work with faulty values. But in other cases, we might want to ignore errors and continue with the execution. **try…catch** allows us to have control over what to do when an error happens.

## Summary

We have just learned about how to read and write files in Node.js synchronously. We have also learned about the **try…catch** statement that allows us to handle errors. When not handled, errors would make our programs crash but using the **try…catch** statement, we can choose to handle those errors in any way we want.

# 19 Working Asynchronously

The `Sync` suffix included in the functions such as `fs.existsSync` and `fs.mkdirSync` indicates that these functions are **synchronous (sync)** and they have **asynchronous (async)** versions. **Synchronous** operation is an operation where we have to wait for it to finish before the next operation can start. This is pretty much how a lot of things we have seen so far are working. For example, when we performed an operation on one line and wanted to `console.log` the result of that operation on the next one, the process waits for the first operation to finish. That is how we are able to display the result of the operation on the next line.

```
1 const result = 10 + 10;
2 console.log(result);
```

There are cases when this linear order of operations is not desirable. Sometimes we might want to execute a statement but not care about the results immediately after. This is especially relevant when working with processes that take a longer time to perform. **Input** and **output** operations such as creating, reading, or writing files and folders are usually of this nature. They tend to take much longer compared to operations that happen in the system memory or CPU. We might not want to block the system from doing any further operations by synchronously performing the slow processes. This is why we have asynchronous versions of these potentially costly operations. When we execute an asynchronous function, the program doesn’t wait around for that operation’s result but continues to execute the following lines.

In Node.js, there are two ways to perform async operations. One of them is using **callback functions,** and the other one is using **Promises**.

Let’s look at how we asynchronously perform file system operations using **callback functions**.

## Creating a folder asynchronously

Let’s asynchronously create a folder.

```
1 const fs = require("fs");
2 
3 const folderPath = "myFolder";
4 
5 const callback = (err) => {
6   console.log(err);
7 };
8 
9 fs.mkdir(folderPath, callback);
```

filesystem-03-working-async/01.js

Here we are using the `mkdir` function instead of the `mkdirSync` function to create the folder in an async way. `mkdir` function takes two arguments. The first one is the relative path for the desired folder, and the second argument is a callback function.

A callback function is just a descriptive name for a function that gets passed into another function. The function that receives the callback function chooses when it wants to execute the function. Here is a straightforward example of a callback function.

```
 1 const someOperation = () => {
 2   console.log("this is a function that represents some operation");
 3 };
 4 
 5 const logStartAndEndForOperation = (callbackFunction) => {
 6   console.log("start of operation");
 7   callbackFunction();
 8   console.log("end of operation");
 9 };
10 
11 logStartAndEndForOperation(someOperation);
```

filesystem-03-working-async/02.js

In this example, `someOperation` is a callback function in relation to `logStartAndEndForOperation` function since it is passed as an argument to that function. `logStartAndEndForOperation` function takes a callback function as an argument and determines when to call that given function.

`mkdir` function also takes a callback function as an argument and calls that function when the directory creation operation is finished. `mkdir` function calls the callback function with a single argument, which is the error object with information about the errors that might have occurred during the directory creation. If there are no errors, then it would call the callback function with a `null`. Here is an example to illustrate calling the callback function with an argument.

```
 1 const someOperation = () => {
 2   console.log("this is a function that represents some operation");
 3 };
 4 
 5 const logStartAndEndForOperation = (callbackFunction) => {
 6   const importantValue = 42;
 7   console.log("start of operation");
 8   callbackFunction(importantValue);
 9   console.log("end of operation");
10 };
11 
12 logStartAndEndForOperation(someOperation);
```

filesystem-03-working-async/03.js

I have adjusted the previous example slightly to call the callback function with a numeric value of `42`.

Note that the `someOperation` function doesn’t actually expect any arguments in our example, but that doesn’t mean we can’t pass arguments to it. It is just that the function wouldn’t be using those arguments.

Going back to the `mkdir` function, the error object that gets passed into the callback function carries information about what went wrong during the process. Receiving an error object instead of a `null` value means that the folder didn’t get created for some reason.

```
 1 const fs = require("fs");
 2 
 3 const folderPath = "myFolder";
 4 
 5 const callback = (err) => {
 6   if (err) {
 7     if (err.code === "EEXIST") {
 8       console.log("Folder already exists");
 9     } else {
10       console.log("Something went wrong");
11     }
12   } else {
13     console.log("Success!");
14   }
15 };
16 
17 fs.mkdir(folderPath, callback);
```

filesystem-03-working-async/04.js

If we `console.log` the error object to the screen, we would see that it would be `null` if the directory is created successfully. But it would be an object with some properties if there is an error condition like the same directory name already existing. One of these properties is the `code` property that has a code for the error reason. For the case where the directory already exists, the `code` would be equivalent to `EEXIST`. We can use this code to `console.log` a message that informs the user that the folder already exists. If there is an error object, but the code is different, we can simply `console.log` a generic error message that communicates something went wrong for a simple error handling mechanism. If there are no errors, we can assume that the folder is successfully created and displaying a success message.

In this example, we don’t need to check to see if the folder exists anymore since we would get an error anyway if it does and handle the situation accordingly.

When using callback functions, error handling is a bit different than compared to working synchronously. In a synchronous scenario, we would be using **try…catch** statements to handle errors. In callback functions, we are using the error object that we receive to handle the errors.

How do we know if this function is asynchronous? We can verify that by placing a `console.log` statement right after the `mkdir` call. We would notice that the `console.log` statement gets executed before the callback function. This is because the input-output operations such as creating a folder take much longer to complete than merely logging a value to the screen.

```
 1 const fs = require("fs");
 2 
 3 const folderPath = "myFolder";
 4 
 5 const callback = (err) => {
 6   if (err) {
 7     if (err.code === "EEXIST") {
 8       console.log("Folder already exists");
 9     } else {
10       console.log("Something went wrong");
11     }
12   } else {
13     console.log("Success!");
14   }
15 };
16 
17 fs.mkdir(folderPath, callback);
18 console.log("End of program");
```

filesystem-03-working-async/05.js

We might see callback functions not separately declared as we did here but defined inline where they are being passed into the function. That might make sense given that this is not a function that we are planning on reusing but want to pass as an argument to another function call. Having an inline callback function would look something like this:

```
 1 const fs = require("fs");
 2 
 3 const folderPath = "myFolder";
 4 
 5 fs.mkdir(folderPath, (err) => {
 6   if (err) {
 7     if (err.code === "EEXIST") {
 8       console.log("Folder already exists");
 9     } else {
10       console.log("Something went wrong");
11     }
12   } else {
13     console.log("Success!");
14   }
15 });
16 
17 console.log("End of program");
```

filesystem-03-working-async/06.js

It is not an incident that the first argument for the callback function for `mkdir` is the `err` object. That is a pretty well-established convention in Node.js. Let’s take a look at other asynchronous functions to understand the callback function arguments a bit better.

## Reading and Writing files in Node.js

To be able to write to a file asynchronously, we will be using the `writeFile` function. Here is how we do it:

```
 1 const fs = require("fs");
 2 
 3 const filePath = "temp.txt";
 4 const fileData = "hello world";
 5 
 6 fs.writeFile(filePath, fileData, (err) => {
 7   if (err) {
 8     console.log(err);
 9   }
10 });
```

filesystem-03-working-async/07.js

We are using the async version of `writeFile`. Sync version for the same functions exists under the name `writeFileSync`.

This code creates a file called `temp.txt` in the folder where we call the script from and writes the data `hello world` into that file. If we were to execute this script again, it would work without throwing an error, unlike the `mkdir` function. It doesn’t complain when the target file already exists; it just overwrites it with new data. And just like we learned before, the first argument for the callback function is the error object.

Let’s look at how to read files.

```
 1 const fs = require("fs");
 2 
 3 const filePath = "temp.txt";
 4 
 5 fs.readFile(filePath, "utf8", (err, data) => {
 6   if (err) {
 7     console.log(err);
 8   } else {
 9     console.log(data);
10   }
11 });
```

filesystem-03-working-async/08.js

This code will read the content of the `temp.txt` file granted that it exists. We would receive an error message with the error code `ENOENT` in case the file does not exist. We can update our code to handle that error message.

```
 1 const fs = require("fs");
 2 
 3 const filePath = "temp.txt";
 4 
 5 fs.readFile(filePath, "utf8", (err, data) => {
 6   if (err) {
 7     if (err.code === "ENOENT") {
 8       console.log("File does not exist");
 9     } else {
10       console.log("Something went wrong");
11     }
12   } else {
13     console.log(data);
14   }
15 });
```

filesystem-03-working-async/09.js

What if we wanted to get the content of the file that we read and pass it to another function for further processing? Doing so was very straightforward when we were working with synchronous functions. Here is what that would look like if the function is synchronous.

```
1 const fs = require("fs");
2 
3 const filePath = "temp.txt";
4 
5 const data = fs.readFileSync(filePath, "utf8");
6 console.log(data);
```

filesystem-03-working-async/10.js

This would not be possible to do when working with asynchronous functions. We can’t just execute an async function and expect to capture the result with a variable assignment since the result of that execution doesn’t become available until later. We need to do any further processing on the result inside the callback function.

Say we have a function that prints out some statistical information about the given string, like the string’s length and the number of words in it.

```
 1 const fs = require("fs");
 2 
 3 const getTextData = (text) => {
 4   const numChars = text.length;
 5   const numWords = text.split(" ").length;
 6 
 7   console.log(`Given text has ${numChars} characters and ${numWords} words.`);
 8 };
 9 
10 const main = () => {
11   const filePath = "temp.txt";
12 
13   fs.readFile(filePath, "utf8", (err, data) => {
14     if (err) {
15       console.log("Something went wrong");
16       console.log(err);
17       return;
18     } else {
19       getTextData(data);
20     }
21   });
22 };
23 
24 main();
```

filesystem-03-working-async/11.js

As we can see, if we wanted to operate on the results of `readFile` function, we would have to do that from inside the callback function of `readFile`.

```
1 fs.readFile(filePath, "utf8", (err, data) => {
2   if (err) {
3     console.log("Something went wrong");
4     console.log(err);
5     return;
6   } else {
7     getTextData(data);
8   }
9 });
```

filesystem-03-working-async/11.js

## Choosing in Between Synchronous and Asynchronous Functions

Now that we know how to work with synchronous and asynchronous functions you wonder how to choose between two methods. As you might have noticed, synchronous functions are much easier to work with since it results in a linear code that runs from top-to-bottom. In comparison, asynchronous functions require more lines of code to write and are more complicated due to their non-linear nature.

Having said that, there are substantial performance benefits for using asynchronous operations. It makes sense to use synchronous functions if the performance is not a consideration. Otherwise, asynchronous functions are the way to go.

We have only seen using callback functions for asynchronous operations. There are also **Promises** and **async/await** to handle asynchronous operations that we will be exploring later.

## Summary

In this section, we have learned about the difference between synchronous and asynchronous operations. We have used asynchronous file system operations such as `fs.mkdir`, `fs.writeFile`, `fs.readFile`.

We have also learned how to choose in between synchronous and asynchronous operations. If performance is a concern, we should choose to work with asynchronous operations; otherwise, synchronous operations are also fine.

# IV Image Processing in Node.js

# 20 Image Processing in Node.js using Jimp

In this chapter, we will look into using JavaScript and Node.js for image processing. We will take an input image and then perform operations on this image such as resizing, color manipulation, applying effects, and adding text on top of it. Performing these operations using Node.js might not seem impressive, given we could easily do these things (and much more) using a graphics editor like **Photoshop**. But the power of performing these operations programmatically comes from the fact that once we have a program that works for a single image, we can easily extend it to work on thousands of images. The operations we perform becomes infinitely scalable and repeatable.

What is image processing used for? Given we have an image, we might want to:

*   Add some effects to it (like make it grayscale or sepia).
*   Perform color manipulation to make images look better (like adjust the contrast, brightness, etc.)
*   Crop the images we have to a specific size based on our requirements.
*   Add branding or watermark to those images.

We will be using a third-party library for doing image processing in Node.js. There are a bunch of libraries on Node.js that can help us with this task. The one that we will be using is called **jimp**. **jimp** stands for **JavaScript Image Manipulation Program**.

jimp is a library that is written entirely in JavaScript. This means that it doesn’t have any external dependencies. Sometimes graphics processing libraries can have sophisticated dependencies that might not work on every platform. For example, there are image manipulation libraries out there that wouldn’t work on the Windows platform. This is not the case with jimp. More information about this library is available at this link: [https://github.com/oliver-moran/jimp](https://github.com/oliver-moran/jimp)

Let’s get started by creating a new folder. Inside this folder, we will create a file called `main.js` to write our JavaScript code.

```
1 mkdir image-manipulation
2 cd image-manipulation
3 touch main.js
```

We will also create a `package.json` file by calling `npm init -y`.

```
1 npm init -y
```

Now that we have a `package.json` installed in our project folder, we can install the `jimp` package by running:

```
1 npm install --save jimp
```

`--save` flag ensures that the package that we are installing gets saved in the `package.json` file. `package.json` will have a list of all the required packages (aka **dependencies**) to run this project.

We will also need an image file to manipulate. We can use Google images to find a **jpg** image that we would like to work on and saved this image into the project folder under the name `source.jpg`

Now we can start using this library. Let’s jump into the `main.js` file.

```
 1 const Jimp = require("jimp");
 2 
 3 const sourceFilePath = "./source.jpg";
 4 const targetFilePath = "./source_updated.jpg";
 5 
 6 Jimp.read(sourceFilePath, (err, image) => {
 7   if (err) {
 8     console.log("Something went wrong");
 9     throw err;
10   }
11 
12   image
13     .resize(512, 512)
14     .greyscale()
15     .write(targetFilePath, (err) => {
16       if (err) {
17         console.log("Something went wrong");
18         throw err;
19       }
20 
21       console.log("Successfully completed");
22     });
23 });
```

image-01-image-processing/01.js

Here we are importing the jimp library under the name `Jimp`. We are then declaring two variables for path names. One of them is the path for the source image, and the other one is the destination path that we would like to save the modified image.

```
1 const Jimp = require("jimp");
2 
3 const sourceFilePath = "./source.jpg";
4 const targetFilePath = "./source_updated.jpg";
```

image-01-image-processing/01.js

As we can see, `Jimp` has a method called `read` that helps us read in the image file as an image object. Here, the callback function receives the error object as the first argument and the resultant data as the second argument. This is similar to how the other callback functions work in Node.js.

```
1 if (err) {
2   console.log("Something went wrong");
3   throw err;
4 }
```

image-01-image-processing/01.js

We are checking to see if there is an error using the `if` statement. If there is an error, we are logging a message that says `Something went wrong`. If not, we start operating on the `image` object. This object has a bunch of methods that we can use to manipulate the image file.

Digital images are made up of **pixels**. We can think of a pixel as a square that has a single color. When a grid of pixels comes together, they form an image. The size of an image is defined by the number of pixels used for the width and the height.

We are calling the `resize` method of the image with the arguments of `512, 512`. The first argument defines how many pixels we want the image’s width to be, and the second one is for the height of the image.

```
1 image.resize(512, 512);
```

image-01-image-processing/01.js

We are then calling the `greyscale` method on the object to turn the image black and white. Afterward, we are calling the `write` method to write out the manipulated image to the file system. We can pass a **callback** to this function to display a message after the image is successfully saved onto the disk.

```
 1 image
 2   .resize(512, 512)
 3   .greyscale()
 4   .write(targetFilePath, (err) => {
 5     if (err) {
 6       console.log("Something went wrong");
 7       throw err;
 8     }
 9 
10     console.log("Successfully completed");
11   });
```

image-01-image-processing/01.js

As you can see, the jimp library is fairly straightforward to use. We will use this library to illustrate a potential problem with the callback functions. Let’s look at a more complicated example to see this issue.

## Callback Hell

jimp has another useful method called `loadFont`. As the name suggests, `loadFont` allows us to load a font file. The font file needs to have the file extension of `.fnt`. We can then use this font file to place text onto the image file using the `print` method.

We can either use a custom font with a `.fnt` extension to load into the program or use the fonts included with this library. For our purposes, loading in the default font file would be much more comfortable. We could use this constant variable that is part of the library to load a white **sans-serif** font that is `64px` size.

```
1 Jimp.FONT_SANS_64_WHITE;
```

image-01-image-processing/02.js

We can pass this variable to the `loadFont` method to load the corresponding font.

```
1 Jimp.loadFont(Jimp.FONT_SANS_64_WHITE, (err, font) => {
2 }
```

image-01-image-processing/02.js

And then, we can use the loaded font inside the `print` method.

```
 1 const Jimp = require("jimp");
 2 
 3 const sourceFilePath = "./source.jpg";
 4 const targetFilePath = "./source_updated.jpg";
 5 
 6 Jimp.read(sourceFilePath, (err, image) => {
 7   if (err) {
 8     console.log("Something went wrong");
 9     throw err;
10   }
11 
12   Jimp.loadFont(Jimp.FONT_SANS_64_WHITE, (err, font) => {
13     if (err) {
14       console.log("Something went wrong");
15       throw err;
16     }
17 
18     image
19       .resize(512, 512)
20       .greyscale()
21       .print(font, 10, 10, "Image Title")
22       .write(targetFilePath, (err) => {
23         if (err) {
24           console.log("Something went wrong");
25           throw err;
26         }
27 
28         console.log("Successfully completed.");
29       });
30   });
31 });
```

image-01-image-processing/02.js

We are loading the font file using the `loadFont` method and then using it inside the `print` method. The `print` method takes four arguments. The `font` object, the **x-axis** and **y-axis** location of the font, and the text to be printed using that font. The **x-axis** location is determined using the distance in pixels from the left side of the image. The **y-axis** location is determined using the distance in pixels from the top of the image. We are placing a text that reads `Image Title` 10 pixels away from the top-left corner.

Here is the problem that you might have started to notice regarding our code. We keep indenting our code with each new **async** operation. This creates a deeply nested structure in our code that can affect the code’s legibility and maintainability. This problem is called **Callback Hell**, where the program keeps getting nested with each callback.

There are asynchronous structures other than callback functions that we can use to help us tackle this problem and write more readable code.

## Callbacks vs. Promises

Here is what an asynchronous operation that works with **callback functions** would look like:

```
1 someAsyncOperation((err, data) => {
2   if (err) {
3     throw err;
4   }
5 
6   someOtherAsyncOperation(data);
7 });
```

Using functions that are based on **Promises**, we can write asynchronous code that would look like this:

```
1 someAsyncOperation()
2   .then(someOtherAsyncOperation)
3   .catch((err) => throw err);
```

A **Promise** is a JavaScript object that represents the **state** and **value** of an asynchronous operation. When an asynchronous operation that returns a Promise executes, it would return a **Promise** with a **pending state**. A pending Promise is a Promise that will **resolve** (or get **rejected**) once the underlying async operation is complete. Here is how we can create a Promise object if we were creating it from scratch:

```
1 new Promise((resolve, reject) => {});
```

For the most part, we won’t be creating Promise objects ourselves but work with asynchronous functions that return a Promise.

A Promise object has a method called `then` that accepts a callback function called with the result of the operation once it is complete. A Promise object also has a `catch` method that we can use to handle possible errors.

Let’s illustrate the difference between **Promises** and **callback functions** by looking at the `setTimeout` function.

`setTimeout` is a JavaScript function that takes a duration value in milliseconds and a callback function, and it executes the callback function after the given duration value has elapsed. It looks like this:

```
1 const duration = 1000;
2 setTimeout(() => {
3   console.log("this will get displayed after one second");
4 }, duration);
```

Consider this contrived example below. We are creating a function called `delayForOneSecond` that will wait 1 second (1000ms) before calling the callback function that prints out the message `"hello"`.

```
 1 function sayHello() {
 2   console.log("hello");
 3 }
 4 
 5 function delayForOneSecond(cb) {
 6   const duration = 1000;
 7   setTimeout(cb, duration);
 8 }
 9 
10 delayForOneSecond(sayHello);
```

image-01-image-processing/03.js

If for some reason, we wanted to have a three-second delay before displaying the message, we would adjust our code to look like this:

```
 1 function sayHello() {
 2   console.log("hello");
 3 }
 4 
 5 function delayForOneSecond(cb) {
 6   const duration = 1000;
 7   setTimeout(cb, duration);
 8 }
 9 
10 delayForOneSecond(() => {
11   delayForOneSecond(() => {
12     delayForOneSecond(() => {
13       sayHello();
14     });
15   });
16 });
```

image-01-image-processing/04.js

Now we can see the pyramid shape emerging due to callback functions which is not desirable.

If `delayForOneSecond` function returned a `Promise` we could write the above program like this.

```
1 delayForOneSecond()
2   .then(delayForOneSecond)
3   .then(delayForOneSecond)
4   .then(sayHello);
```

Now we don’t have a deep nesting and a pyramid shape (also known as **Callback Hell**). The code looks linear.

Here is how we can update the `delayForOneSecond` function for it to return a `Promise` object.

```
 1 function sayHello() {
 2   console.log("hello");
 3 }
 4 
 5 function delayForOneSecond(cb) {
 6   const duration = 1000;
 7 
 8   return new Promise((resolve) => {
 9     setTimeout(() => {
10       if (cb) {
11         cb();
12       }
13       resolve();
14     }, duration);
15   });
16 }
17 
18 delayForOneSecond()
19   .then(delayForOneSecond)
20   .then(delayForOneSecond)
21   .then(sayHello);
```

image-01-image-processing/05.js

Promises allow us to write async programs that are much more manageable and readable since they don’t result in deeply nested structures that callback functions can cause.

Now that we know a little more about Promises, we can go back to our image manipulation example to put that knowledge into use.

## Using Jimp with Promises

It turns out we can use jimp with Promises as well. The library is designed so that if we don’t pass a callback argument, then the functions would return a Promise.

```
 1 const Jimp = require("jimp");
 2 
 3 const sourceFilePath = "./source.jpg";
 4 const targetFilePath = "./source_updated.jpg";
 5 
 6 let image;
 7 
 8 Jimp.read(sourceFilePath)
 9   .then((_image) => {
10     image = _image;
11 
12     return Jimp.loadFont(Jimp.FONT_SANS_64_WHITE);
13   })
14   .then((font) => {
15     return image
16       .resize(512, 512)
17       .greyscale()
18       .print(font, 10, 10, "Image Title")
19       .write(targetFilePath);
20   })
21   .then(() => {
22     console.log("Successfully completed");
23   })
24   .catch((err) => {
25     console.log(err);
26     throw err;
27   });
```

image-01-image-processing/06.js

Notice we are not getting a deeply nested structure anymore. Promises solve the problem of **Callback Hell** for us. The only thing that is worth noting here is the usage of the `image` variable. We are initially declaring an empty `image` variable. We are initializing this variable but not assigning any value to it yet. We are then using this variable to store the `image` object we receive from reading the image file.

```
1 let image;
2 
3 Jimp.read(sourceFilePath).then((_image) => {
4   image = _image;
5 
6   return Jimp.loadFont(Jimp.FONT_SANS_64_WHITE);
7 });
```

image-01-image-processing/06.js

We declare this variable outside of the Promise chain because we want that variable to be accessible from every step of the Promise method chain.

## Summary

jimp is a convenient Node.js library that allows us to do all kinds of image manipulation tasks. It has many functions that allow us to perform common image manipulation operations such as cropping, color adjustments, blurring, etc.

jimp has support for both callback functions and Promises. Callback functions are the most primitive way of handling asynchronous operations. It gets the job done but can cause readability issues in our code since we have to nest a lot of callback functions together when we perform a lot of asynchronous operations. Thankfully JavaScript introduced a new programming structure called Promise to handle this issue.

A Promise is a JavaScript object that allows us to write asynchronous operations in a much more readable and manageable way. We have learned how to create Promises from scratch and using jimp with Promises.

# V Web Scraping

# 21 Automate the Web Using Puppeteer

We can programmatically interact with websites by using JavaScript. Automating our interactions with the web by using programming enables us to build tools that can periodically check online stores for changes in product price, fill forms for us, take screenshots or download files with a single command.

There are many libraries in the JavaScript ecosystem that would allow us to control a browser programmatically. The package that we will be using for this purpose is called **[Puppeteer](https://github.com/puppeteer/puppeteer)**. It is a well-maintained library that is developed by the teams at Google.

Puppeteer allows us to control a Chrome (or a Chromium) browser programmatically. When we control a browser without any graphical **UI (user interface)**, it is said to be running in a **headless** mode.

Before learning all about Puppeteer, I would like to introduce an **asynchronous** programming structure called **async-await**. We have previously learned how **callback functions** and **Promises** work. **async-await** is an asynchronous programming structure that got introduced into JavaScript after **Promises**. It makes working with asynchronous code a lot easier. In fact, using **async-await**, we can write code that almost reads like synchronous code. Using **async-await** makes working with Puppeteer much easier.

## async-await

To illustrate how the **async-await** feature in JavaScript works, we will use a function that returns a `Promise`.

```
 1 function delayForOneSecond(cb) {
 2   const duration = 1000;
 3 
 4   return new Promise((resolve) => {
 5     setTimeout(() => {
 6       if (cb) {
 7         cb();
 8       }
 9       resolve();
10     }, duration);
11   });
12 }
```

puppeteer-01-automate/01.js

Here, we have `delayForOneSecond` that takes a **callback function**,`cb`, as an argument. It immediately returns a new `Promise` that executes a `setTimeout` function with a `1000ms` delay. The Promise resolves after one second (which is equivalent to 1000ms) and executes the callback function if one is given.

Using this function, we can write a program that would display the message `hello` on the screen after 3 seconds.

```
 1 function sayHello() {
 2   console.log("hello");
 3 }
 4 
 5 function delayForOneSecond(cb) {
 6   const duration = 1000;
 7 
 8   return new Promise((resolve) => {
 9     setTimeout(() => {
10       if (cb) {
11         cb();
12       }
13       resolve();
14     }, duration);
15   });
16 }
17 
18 delayForOneSecond()
19   .then(delayForOneSecond)
20   .then(delayForOneSecond)
21   .then(sayHello);
```

puppeteer-01-automate/02.js

We have a chain of `then` statements that allows us to execute one `Promise` after another.

```
1 delayForOneSecond()
2   .then(delayForOneSecond)
3   .then(delayForOneSecond)
4   .then(sayHello);
```

puppeteer-01-automate/02.js

Let’s rewrite this program using **async-await**.

```
 1 function sayHello() {
 2   console.log("hello");
 3 }
 4 
 5 function delayForOneSecond(cb) {
 6   const duration = 1000;
 7 
 8   return new Promise((resolve) => {
 9     setTimeout(() => {
10       if (cb) {
11         cb();
12       }
13       resolve();
14     }, duration);
15   });
16 }
17 
18 async function main() {
19   await delayForOneSecond();
20   await delayForOneSecond();
21   await delayForOneSecond();
22   sayHello();
23 }
24 
25 main();
```

puppeteer-01-automate/03.js

We didn’t have to change anything about the function definition for `delayForOneSecond` to make use of the **async-await** construct. How the **async-await** structure works is as follows.

First, we need a function body that will contain the asynchronous functions that we want to execute. In this example, it is the `main` function. Secondly, we place the keyword `async` in front of that function definition. Doing so allows us to make use of the `await` keyword inside that function. Now that we did this, we can now use the `await` keyword in front of the functions that return a Promise.

```
1 async function main() {
2   await delayForOneSecond();
3   await delayForOneSecond();
4   await delayForOneSecond();
5   sayHello();
6 }
```

puppeteer-01-automate/03.js

As we can see in the example, what `await` keyword allows us to do is wait until the `Promise` resolves before executing the next line. Doing so allows us to write code that reads from top to bottom, just like any other synchronous code. Don’t let this trick you into thinking our code just became synchronous, though. It is still asynchronous; it is just that the asynchronous code inside the `async` function body is behaving as if it is synchronous.

Let’s place a `console.log` statement after the `main` function to probe the behavior of **async-await**.

```
 1 function sayHello() {
 2   console.log("hello");
 3 }
 4 
 5 function delayForOneSecond(cb) {
 6   const duration = 1000;
 7 
 8   return new Promise((resolve) => {
 9     setTimeout(() => {
10       if (cb) {
11         cb();
12       }
13       resolve();
14     }, duration);
15   });
16 }
17 
18 async function main() {
19   await delayForOneSecond();
20   await delayForOneSecond();
21   await delayForOneSecond();
22   sayHello();
23 }
24 
25 main();
26 console.log("Start of the program");
```

puppeteer-01-automate/04.js

Running this code, we would notice that the text, `Start of the program`, is getting displayed before the text, `hello`. The `console.log` statement that displays `Start of the program` is synchronous, so it gets executed immediately, but there is still some delay till we get the message `hello`. The program only **awaits** for the asynchronous code to be executed inside the `async` function block, but outside of that function, our program’s flow is still synchronous.

Let’s take a look at the Puppeteer library now that we know how to use **async-await**.

## Getting Started with Puppeteer

Let’s install Puppeteer to start working with it. We will begin with creating a new folder for our project and running the `npm init` command in that folder to create a `package.json` file in there.

Now that we have the `package.json` file created. We can install the puppeteer library by running this command:

```
1 npm install --save puppeteer@3.0.4
```

This installation might take a while since it downloads a version of the **Chromium** browser compatible with this library.

After downloading the file we can create a file called `main.js` and start coding inside it.

Here is an example of a Puppeteer program that programmatically launches a **headless** browser to visit a website and then takes a screenshot of that site to save it onto the computer.

```
 1 const puppeteer = require("puppeteer");
 2 
 3 async function main() {
 4   const browser = await puppeteer.launch();
 5   const page = await browser.newPage();
 6   await page.goto("https://example.com");
 7   const filePath = "example.png";
 8   await page.screenshot({ path: filePath });
 9 
10   await browser.close();
11 }
12 
13 main();
```

puppeteer-01-automate/05.js

We start our code by importing the `puppeteer` library. After that, we define an `async` function called `main` and then call it at the end of our program. The main logic of our program resides inside the `main` function.

Inside the function body, we first launch a browser **instance** by calling `puppeteer.launch()`. Whenever we launch a browser, we should remember to close it to not to cause any **memory leaks** from our program. A **memory leak** means the program that is not working is still consuming resources of the system. We close the browser by calling `browser.close()`.

We launch a new page inside that browser by calling `browser.newPage()`. We then visit the `[example.com](http://example.com)` domain inside that page by using the `page.goto` method. We take a screenshot of the page by using the `page.screenshot` method and save that screenshot into the same folder that we have called the program from. We then ensure that we are closing the browser and exit the program.

I just want to quickly illustrate what the same program would have looked like if it was written by using `Promises`.

```
 1 const puppeteer = require("puppeteer");
 2 
 3 function main() {
 4   let browser;
 5   let page;
 6 
 7   puppeteer
 8     .launch()
 9     .then((_browser) => {
10       browser = _browser;
11       return browser.newPage();
12     })
13     .then((_page) => {
14       page = _page;
15       return page.goto("https://example.com");
16     })
17     .then(() => {
18       const filePath = "example.png";
19       return page.screenshot({ path: filePath });
20     })
21     .then(() => {
22       browser.close();
23     });
24 }
25 
26 main();
```

puppeteer-01-automate/06.js

As we can see, the code looks lengthier and more complex in this example. Another big problem is that we are creating `browser` and `page` objects during our code’s flow, and these objects need to be accessed throughout our program. This results in an issue where we need to save these objects inside a variable to access them throughout the program’s flow, making our code harder to read. It might not look that bad with a simple example, but it can quickly get ugly if the program were to be more complex.

Given that we create variables like `browser` and `page` that need to be accessed globally during the lifetime of a Puppeteer program, using the **await-async** pattern is proving to be very useful.

## Summary

We can programmatically browse the web by using a **headless browser**. A **headless browser** is a browser that doesn’t have a **graphical user interface** and is controlled by programming. We have learned about a headless browser called **Puppeteer** that is developed by teams at Google. We have looked at a simple Puppeteer example that allows us to visit a web page and take a screenshot there.

We have also learned about the **async-await** structure**. async-await** is a programming structure that makes working with asynchronous code much easier. Puppeteer is much easier to use with an **async-await** structure since there are many global variables that we would like to access throughout the lifetime of a program.

# 22 Programming Inside the Browser

Web browsers like Chrome, Firefox, or Safari have ways to execute JavaScript code inside the current website’s context. For example, if we go to any website like [`https://en.wikipedia.org/`](https://en.wikipedia.org/) and launch the development console (View > Developer > JavaScript console in Chrome). In this console, if we are to type `console.log(document.title)` and execute this command, we would see that it displays the `title` of the current page that we are at. There are a bunch of built-in functions and variables that we can access in this context. The `document` object is one of them. Here is another example of using the `document` object. We can use `console.log(document.URL)`, and it would display the URL of the current page.

We need to know a little more about how web pages are developed if we wanted to do more interesting things in the context of a browser using **Puppeteer**. Let’s take a quick look at three technologies that bring websites to life. A website is a combination of three languages. **HTML**, **CSS** and **JavaScript**.

## HTML (Hypertext Markup Language)

HTML is the computer language that allows us to define the structure and the layout of a website. Note that HTML is not a programming language but a **markup language**. A markup language doesn’t have the programming structures like conditional or looping statements necessary to represent complex logic.

Here is what a website that just displays the title `Page Title` and the sentence `Hello World` might look like behind the hood.

```
 1 <!DOCTYPE html>
 2 
 3 <html lang="en">
 4   <head>
 5     <title>The HTML5 Herald</title>
 6   </head>
 7 
 8   <body>
 9     <h1>Page Title</h1>
10     <p>Hello World</p>
11   </body>
12 </html>
```

We can see the structure for any website for ourselves. Go to a website like [`https://en.wikipedia.org/`](https://en.wikipedia.org/) and then display the source (`View > Developer > View Source in Chrome`) for that page. We can alternatively inspect the individual HTML elements that make up the website using the development console in Chrome (`View > Developer > Inspect Elements`).

Let’s go through what each part of that above HTML code means.

```
1 <!DOCTYPE html>
```

This is a declaration for the browser to state that the text file transmitted to the browser is an HTML file. The browser knows to interpret the incoming document as HTML once it sees this declaration at the top. This line is not part of the HTML language, but it is there for the browsers to correctly interpret the HTML document file.

HTML language is made up of **HTML elements**. HTML elements are a bunch of tags that allow us to create a document that websites can interpret. The examples of some HTML elements that are being used in the above example are `html`, `head`, `title`, `body`, `h1`, and `p`.

Notice how these elements are written. There are an opening and a closing **tag** for each element, and the name of the element is written in brackets. The opening tag has the name of the element and any additional properties. For example, the opening tag for the `html` element is `<html lang="en">`, and it has a property called `lang` that takes the value `en`. What that property does is not really important for our discussion. The closing tag for this element is written with a `/` character like `</html>`.

```
1 <html lang="en"></html>
```

The `html` element is the root element of an HTML document and encompasses all the other elements.

```
1 <head></head>
```

The `head` element contains metadata about the document that is interpreted by the browser. In this case, we are using the `title` element to declare the document’s title inside this section. The title information for a website gets displayed on the browser tab.

```
1 <title>The HTML5 Herald</title>
```

The variable `document.title` returns the text that is contained inside this element.

The `body` element contains the content of an HTML document. Here we would add all the other content that can be displayed on the website.

```
1 <body></body>
```

Inside the `body` element we have two other elements. `h1` and `p`.

```
1 <h1>Page Title</h1>
```

An `h1` denotes a **heading** in an HTML document. There are 5 other heading elements: `h2`, `h3`, `h4`, `h5`, and `h6`. They are of decreasing prominence. Meaning `h1` should be the document’s primary heading, and we should only have one `h1` per page. `h2` should be hierarchically under `h1` and is a subheading, etc. Some browsers would render a text larger when they see it inside the `h1` element. That can be useful, but we don’t actually rely on browsers for the styling or our HTML documents. We use the **CSS** language for that. We will learn about that soon.

```
1 <p>Hello World</p>
```

Lastly, we have a `p` element. `p` stands for **paragraph**, and it is used to contain textual content in an HTML document.

There are many other HTML elements. This is only a short introduction for us to gain a contextual understanding of HTML.

We need to have a basic understanding of an HTML structure to do more with our Puppeteer knowledge. Puppeteer allows us to automate our interactions with the websites. When we are programmatically working with a website, we need to understand the underlying language that makes it work.

Let’s take a quick look into **CSS** and then use that knowledge to automate our interactions with the web.

## CSS (Cascading Stylesheets)

As mentioned before, HTML is a markup language. It controls the display of the data by providing us with elements that help with the layout and structure. **CSS** is the **styling language** of the web. It helps us to define a style and apply that style to HTML elements. We can write CSS statements inside separate `.css` files or the HTML document. In this section, we won’t be learning about writing CSS statements but will develop a conceptual understanding of the technology to use the language for our purposes.

Here is a CSS declaration that would set the color of a text of an HTML element to `red`.

```
1 color: red;
```

When we write CSS declarations, we need to associate the declaration with an HTML element. Here is what a CSS declaration inside a **CSS** file might look like.

```
1 h1 {
2   color: red;
3 }
```

What this declaration would do is that it would select all the `h1` elements inside an HTML document and change their color to `red`. In this CSS code, the `h1` is said to be a `CSS selector`. It helps us select all `h1` elements.

This is great, but sometimes we might want to be a little bit more targeted with how we style HTML elements. This is where `class` names and `id`’s come into play.

## Classes and ID’s

Previously, we have seen that we could define properties on HTML elements. The `html` element in our example had a property called `lang` with a value of `en`. There are a bunch of different properties that we can define on HTML elements. Two of those properties that are important for our discussion are `class` and `id` properties.

Here is a `p` element that has a `class` property defined with the value `red-text`.

```
1 <p class="red-text">Hello World</p>
```

We can also add an `id` property to this same `p` element.

```
1 <p class="red-text" id="super-unique-id">Hello World</p>
```

The values for `class` and `id` are arbitrary. We could have called them anything we want. Some naming rules apply, though!

Having these properties allow us to target these HTML elements from our CSS declarations. Imagine having an HTML document with a bunch of `p` elements with only some of those elements having a `red-text` class. If we wanted to target only those elements that have that class name, we could write a CSS declaration that looks like this:

```
1 .red-text {
2   color: red;
3 }
```

The `.` symbol in front of the property name is a **selector** for **class names**. It selects all those elements that have the class name `red-text`.

If We wanted to target an element with a specific ID, this is how we would write that selector:

```
1 #super-unique-id {
2   color: red;
3 }
```

`#` symbol is a **selector** for **ids**.

You might be wondering about the difference between the `id` and the `class` property. There can be multiple elements in a CSS document that has the same `class` property. `class` property is great for applying common styles to multiple elements. Unlike `class` property, the value of an `id` property needs to be unique inside an HTML document. We can’t have more than one element that has the `id` value.

CSS is an incredibly powerful language that allows us to create amazing websites. There is a lot to be learned about CSS, but here we are only covering what is necessary for our purposes.

## Using JavaScript inside the Browser

Here is why all this information is useful. There is a method on `document` object called `querySelector` that allows us to save a reference to an HTML on the web page. For example, calling `document.querySelector('h1')` would allow us to get a reference to the `h1` element. We can then call the `innerText` method on the `h1` element to get the element’s text content. Here is what that code looks like:

```
1 const h1Element = document.querySelector("h1");
2 const h1Content = h1Element.innerText;
3 console.log(h1Content);
```

If we were to execute this code on our previous example, it would display `Page Title` to the screen.

The argument that we pass inside the `querySelector` is a **CSS selector**! The JavaScript `querySelector` method returns the **first** element that matches that CSS selector.

If we wanted to get all the elements that match the CSS selector, we could use the `querySelectorAll` method. It returns an **array** of all the objects that match. Here is what the usage of that method on the above example would look like:

```
1 const h1Elements = document.querySelectorAll("h1");
2 const h1Element = h1Elements[0];
3 const h1Content = h1Element.innerText;
4 console.log(h1Content);
```

We can now start looking at some practical examples using Puppeteer now that we know how everything works together.

## Summary

In this chapter, we have learned about executing JavaScript code inside a web page context. The `document` object available inside the browser has methods that we can use to gather information about the web page we are visiting.

We have also learned some basics about **HTML** and **CSS. HTML** and **CSS** are two other languages that make up a website. HTML defines the layout and structure of a web document, and CSS applies styles to it.

The `document` object has two methods called `querySelector` and `querySelectorAll` that allow us to use CSS selectors to fetch information about particular HTML elements on a webpage. We will make use of these functions as we are writing Puppeteer programs.

# 23 Project: Get Random Wikipedia Articles

In this chapter, we will build a program that will fetch a random Wikipedia article every time it runs.

Let’s look at how we would manually perform such a task to understand how we would automate it. In this case, we need to visit the website for Wikipedia ([https://en.wikipedia.org](https://en.wikipedia.org/wiki/Gong_Naiying)) and click on the link named `Random Article` to take us to a random article page. On each article page, there is a title and an introductory paragraph.

We will need to follow the same steps with our **Puppeteer** program. We will visit the **URL** for random results and fetch the **HTML** elements with the title and the description. We would then need to display these results on the screen.

The URL for the `Random Article` page is [`https://en.wikipedia.org/wiki/Special:Random`](https://en.wikipedia.org/wiki/Special:Random). We can get this value by right-clicking on this link and selecting `Copy Link Address`. We will start by writing a program that will visit this URL and take a screenshot.

```
 1 const puppeteer = require("puppeteer");
 2 
 3 async function main() {
 4   const browser = await puppeteer.launch();
 5 
 6   const page = await browser.newPage();
 7   const urlPath = "https://en.wikipedia.org/wiki/Special:Random";
 8   await page.goto(urlPath);
 9   const filePath = "example.png";
10   await page.screenshot({ path: filePath });
11 
12   await browser.close();
13 }
14 
15 main();
```

puppeteer-03-project-wiki/01.js

Everytime we run this program we are capturing a new screenshot from the visited URL.

We can inspect the HTML structure of an article page in a Chrome browser by clicking `View > Developer > Inspect Elements`. We would see that the title of the article is defined inside an `h1` tag. This means that we can get the title data by running the code below inside the developer console when we are on an article page.

```
1 const title = document.querySelector("h1");
2 const titleText = title.innerText;
```

puppeteer-03-project-wiki/02.js

We can use Puppeteer to execute this code in the context of a webpage. We can use the `page.evaluate` function for this purpose. `page.evaluate` takes a callback function as an argument that gets evaluated in the current web page context. What we return from this callback function can be used in the Puppeteer application.

```
 1 const puppeteer = require("puppeteer");
 2 
 3 async function main() {
 4   const browser = await puppeteer.launch();
 5 
 6   const page = await browser.newPage();
 7   const urlPath = "https://en.wikipedia.org/wiki/Special:Random";
 8   await page.goto(urlPath);
 9   const filePath = "example.png";
10   await page.screenshot({ path: filePath });
11 
12   const title = await page.evaluate(() => {
13     const title = document.querySelector("h1");
14     const titleText = title.innerText;
15 
16     return titleText;
17   });
18 
19   console.log(title);
20 
21   await browser.close();
22 }
23 
24 main();
```

puppeteer-03-project-wiki/03.js

Here we are capturing the value of the `h1` tag in the **webpage context** and returning that value to the **Puppeteer context**.

```
1 const title = await page.evaluate(() => {
2   const title = document.querySelector("h1");
3   const titleText = title.innerText;
4 
5   return titleText;
6 });
```

puppeteer-03-project-wiki/03.js

`page.evaluate` can be a little unintuitive since its callback function can’t refer to any value in the Puppeteer context. For example, we can’t do something like the following example when using the `page.evaluate` function:

```
1 const selector = "h1";
2 const title = await page.evaluate(() => {
3   const title = document.querySelector(selector);
4   const titleText = title.innerText;
5 
6   return titleText;
7 });
8 
9 console.log(title);
```

puppeteer-03-project-wiki/04.js

This program would throw an error. The `selector` variable doesn’t exist inside the webpage context, so we can’t refer to it from there. If we wanted to pass data to the webpage context, we could do so by providing it as an argument to the `page.evaluate` and its callback function.

```
1 const selector = "h1";
2 const title = await page.evaluate((selector) => {
3   const title = document.querySelector(selector);
4   const titleText = title.innerText;
5 
6   return titleText;
7 }, selector);
8 
9 console.log(title);
```

puppeteer-03-project-wiki/05.js

In this example, we are passing the `selector` variable as the second argument to the `page.evaluate` function as well as an argument to the callback function.

In our program, let’s get the first paragraph of the article as well. Looking at the HTML structure, it seems like the `p` element we are looking for is inside an element with the **class** value `mw-parser-output`. That element, in turn, is inside the element with the id value `mw-content-text`. We can select all `p` elements inside that container with this **CSS** **selector**: `#mw-content-text .mw-parser-output p`.

```
 1 const [title, description] = await page.evaluate(() => {
 2   const title = document.querySelector("h1");
 3   const titleText = title.innerText;
 4 
 5   const description = document.querySelector(
 6     "#mw-content-text .mw-parser-output p"
 7   );
 8   const descriptionText = description.innerText;
 9 
10   return [titleText, descriptionText];
11 });
```

puppeteer-03-project-wiki/06.js

We are now getting both the **title** and the first **paragraph** from the article page. We are returning them to the Puppeteer context as an **array**. We are using **array destructuring** to unpack these values. Let’s also get the **URL** of the current page by using the `window.location.href` variable.

```
 1 const [title, description, url] = await page.evaluate(() => {
 2   const title = document.querySelector("h1");
 3   const titleText = title.innerText;
 4 
 5   const description = document.querySelector(
 6     "#mw-content-text .mw-parser-output p"
 7   );
 8   const descriptionText = description.innerText;
 9 
10   const url = window.location.href;
11 
12   return [titleText, descriptionText, url];
13 });
```

puppeteer-03-project-wiki/07.js

This is looking pretty great. We can format these values that we are capturing using a **template literal** and display them on the screen using `console.log`.

```
 1 const puppeteer = require("puppeteer");
 2 
 3 async function main() {
 4   const browser = await puppeteer.launch();
 5 
 6   const page = await browser.newPage();
 7   const urlPath = "https://en.wikipedia.org/wiki/Special:Random";
 8   await page.goto(urlPath);
 9   const filePath = "example.png";
10   await page.screenshot({ path: filePath });
11 
12   const [title, description, url] = await page.evaluate(() => {
13     const title = document.querySelector("h1");
14     const titleText = title.innerText;
15 
16     const description = document.querySelector(
17       "#mw-content-text .mw-parser-output p"
18     );
19     const descriptionText = description.innerText;
20 
21     const url = window.location.href;
22 
23     return [titleText, descriptionText, url];
24   });
25 
26   console.log(`
27 Title: ${title}
28 Description: ${description}
29 Read More at: ${url}
30 `);
31 
32   await browser.close();
33 }
34 
35 main();
```

puppeteer-03-project-wiki/07.js

This code works great so far, but I am noticing that the description text is sometimes empty. Looking at the article page, this seems to happen when the first `p` element has a class called `mw-empty-elt`. Let’s update our code to check to see if the first element’s class name is equivalent to `mw-empty-elt`. If so, we would use the second `p` element instead. We can use the `document.querySelectorAll` function to get an array of all HTML elements that match the given CSS selector.

```
 1 const puppeteer = require("puppeteer");
 2 
 3 async function main() {
 4   const browser = await puppeteer.launch();
 5 
 6   const page = await browser.newPage();
 7   const urlPath = "https://en.wikipedia.org/wiki/Special:Random";
 8   await page.goto(urlPath);
 9   const filePath = "example.png";
10   await page.screenshot({ path: filePath });
11 
12   const [title, description, url] = await page.evaluate(() => {
13     const title = document.querySelector("h1");
14     const titleText = title.innerText;
15 
16     let descriptionParagraph;
17     const descriptionParagraphs = document.querySelectorAll(
18       "#mw-content-text .mw-parser-output p"
19     );
20     const firstDescriptionParagraph = descriptionParagraphs[0];
21     if (firstDescriptionParagraph.className === "mw-empty-elt") {
22       descriptionParagraph = descriptionParagraphs[1];
23     } else {
24       descriptionParagraph = descriptionParagraphs[0];
25     }
26 
27     const descriptionText = descriptionParagraph.innerText;
28 
29     const url = window.location.href;
30 
31     return [titleText, descriptionText, url];
32   });
33 
34   console.log(`
35 Title: ${title}
36 Description: ${description}
37 Read More at: ${url}
38 `);
39 
40   await browser.close();
41 }
42 
43 main();
```

puppeteer-03-project-wiki/08.js

This program is now in a pretty good spot! We have added the logic to choose the second paragraph if the first one has the class name `mw-empty-elt`.

```
 1 let descriptionParagraph;
 2 const descriptionParagraphs = document.querySelectorAll(
 3   "#mw-content-text .mw-parser-output p"
 4 );
 5 const firstDescriptionParagraph = descriptionParagraphs[0];
 6 if (firstDescriptionParagraph.className === "mw-empty-elt") {
 7   descriptionParagraph = descriptionParagraphs[1];
 8 } else {
 9   descriptionParagraph = descriptionParagraphs[0];
10 }
11 
12 const descriptionText = descriptionParagraph.innerText;
```

puppeteer-03-project-wiki/08.js

## Things to Keep in Mind with Headless Browsers

We have previously talked about the leverage we achieve when we perform things programmatically. If we have a program that can access a single website, it can then be a simple matter to scale it to access thousands of websites.

This can be problematic when interacting with the web. If we were to load thousands of pages from a single domain in a short amount of time, it could potentially overwhelm the servers hosting those pages. It can even be interpreted as an attack on the website. Our IP can temporarily get blocked from accessing their resources or even get banned. We need to be mindful when using websites programmatically. We might want to add artificial delays in between our operations to slow our program down. We also need to be careful about what data we can access programmatically. Some websites try to prevent programmatic access to protect their data.

**Web scraping** is the act of using programs like Puppeteer to access and harvest data from websites programmatically. There can be legal implications for web scraping, so you should do your own research before engaging in such an action.

Web scraping is not the only way to access data on a webpage. There are many web applications out there that expose an **API** to connect developers with their resources. An API is an **Application Programming Interface** that we can use to interface with a resource programmatically. Using APIs, developers can build applications on top of popular services such as **Twitter**, **Facebook**, **Google,** or **Spotify**. We will learn more about APIs in the next chapter.

## Summary

In this chapter, we have built a simple Puppeteer program that visits Wikipedia to display data from a random article. We have learned about the `page.evaluate` function that allows us to evaluate code in the context of the visited web page. We have also used **CSS Selectors** to be able to get data for the desired HTML elements in a webpage. Other than that, we have used functions and properties such as `document.querySelector`, `document.querySelectorAll` and `window.location.href` to be able to get the data we are after from a web page.

Finally, we have learned about some of the things that we need to be mindful of when accessing a resource on the internet.

# VI APIs

# 24 Working With APIs

An **API** is short for **Application Programming Interface**. APIs define how applications talk to each other. We have been writing programs that use APIs all along the way. For example, we have interacted with the built-in **fs** library, **Puppeteer**, or **jimp** through their API. When we use these libraries in our programs, our programs use the **interface** that these libraries define without knowing whatever might be going inside that library.

An API abstracts away the underlying system’s complexity and exposes a simplified interface for the user to interact with.

We can think of a car as a complex system. It has internal combustion or an electric engine. Both of which are made up of thousands of smaller components. There is a bunch of other parts of a car that makes it work. But as a driver of the car, all we use (for the most part) is the interface exposed to us.

That interface consists of the wheel, gas and brake pedals, and a shift. This simplified interface allows us to operate this complex system easily. When driving a car, we only worry about the higher-level concerns. We don’t want to think about what is happening in the engine while driving a car. We want to make sure we are safely transporting ourselves from one point to another. Roads can be dangerous, and the last thing we would want to do is think about a car’s inner workings while driving.

There are times where we might need to deal with the internals of the car. Suppose we want to do things with our car that is not intended by the manufacturer, like modify the engine to increase performance or efficiency. Or we might need to fix some issues. That is when we might want to take a look under the hood.

This is very similar to what happens when we are programming. When using the `fs` module to create folders in Node.js, we don’t really want to know what Node.js is doing internally to create those folders. We just want to call a function and get the result. Unless we had particular needs or performance concerns, we wouldn’t look under the hood of a Node.js function. What is exposed through the API should be enough for our needs.

Of all the APIs that are available, the most interesting ones to use are the **APIs** for **Web Services (Web API** in short).

Unlike programming libraries, a web API is an interface to an external service, to a service that doesn’t live on our computer. We connect to a web API through the **World Wide Web**. We can query government data, use powerful machine learning models or programmatically interact with services such as Google, Twitter, Spotify, or Reddit using web APIs. In a way, a web API grants superpowers to our programs.

## Communicating with Web APIs

We need to be able to communicate over the internet to be able to use web APIs. Node.js has built-in libraries as well as third-party libraries that enable us to do that. We will be using a third-party library called `node-fetch` for this purpose. Let’s create a new folder for this chapter and create a `package.json` file in there. Then, we will install `node-fetch`.

```
1 mkdir project-learning-webapis
2 cd project-learning-webapis
3 npm init -y
4 npm install --save node-fetch@2.6.1
```

Let’s also create a file called `main.js`. We can do so by running `touch main.js`. We will start using `node-fetch` inside this file.

```
 1 const fetch = require("node-fetch");
 2 
 3 async function main() {
 4   const url = "https://en.wikipedia.org/wiki/Main_Page";
 5 
 6   const response = await fetch(url);
 7   const body = await response.text();
 8 
 9   console.log(body);
10 }
11 
12 main();
```

apis-01-working-with-apis/01.js

Using the `fetch` function allows us to make an **HTTP** **request**. **HTTP** is the name of the **communication protocol** that is used by the **World Wide Web**. Sending **requests** and receiving **responses** is how web browsers communicate with web pages and the `fetch` function allows us to do that programmatically.

`fetch` is an **asynchronous** function. It sends a **request** to the given **URL (website address)** and **returns** a `response` object as a result. Here, we are sending a request to a resource that is an **HTML** file. We can see the plain text version of this HTML data by calling the `response.text` function.

Not every resource on the web is an HTML file. Some URLs can return other forms of data, such as **JSON** as well.

```
 1 const fetch = require("node-fetch");
 2 
 3 async function main() {
 4   const url = "https://api.github.com/users/github";
 5 
 6   const response = await fetch(url);
 7   console.log(response);
 8   const data = await response.json();
 9 
10   console.log(data);
11   console.log(data.name);
12 }
13 
14 main();
```

apis-01-working-with-apis/02.js

Here we are sending a **request** to a URL that returns **JSON** data. Calling `response.json` parses this data as JSON and returns a **JavaScript object.** Here we are console logging the `name` property of the `data` object.

We will be using the `fetch` function to communicate with web APIs.

## Using Web APIs

There is a lot of web APIs out there. Most of your favorite online websites likely offer APIs to allow other applications to communicate with their services. Companies build APIs for their services for many reasons, like allowing developers to innovate on top of their platform, monetize the data they possess or provide convenience to their users.

We can use the **Google Maps API** to build map-based applications. **Instagram API** would allow us to post on their platform programmatically. We can send SMS messages from our programs using the **Twilio API**.

A lot of APIs might require us to get **authenticated** to start using them. In the authentication process, we register to the API platform as an application developer to get **API** **Keys**. An API key (or a secret) is a private key that identifies our application to the API platform.

APIs can have limitations over how many requests we can perform in a given time frame. They might offer free or paid tiers that have different kinds of limitations. Platforms can incentivize developers to discover their APIs by offering a free tier. They can also make money by offering a paid tier to larger businesses with more demanding needs from these APIs. A free tier is generally enough for personal projects, but if you are looking to build a web application that will serve other users, you might have to pay for the API access.

## About Web Browser APIs and Web Service APIs

The term **Web API** is sometimes used to refer to the API that is exposed by web browsers. Previously we have used the `document.querySelector` function to be able to get data about the elements on a web page. That is an example of a Web Browser API. Web Browsers also have a `fetch` function similar to the `fetch` function we have learned in this chapter. Node.js doesn’t have that function built-in (it is not part of its API), so we had to install it as a third-party package.

## Summary

In this chapter, we have learned what an **API (Application Programming Interface)** is. We can think of APIs as simply an interface of a program. An API abstracts away the underlying system’s complexity and exposes a simplified interface for the user to interact with. APIs for web services (**Web APIs**) provide exciting possibilities since they make it possible for us to use their advanced capabilities programmatically.

We can use a library like `node-fetch` to interact with Web APIs. Using a `fetch` function, we can send a **request** to a web address (**URL)** and get a **response**. APIs are supposed to be consumed programmatically, so they would usually return a **JSON** response.

We might need to get authenticated on the API provider’s platform to use an API, and we might also need to pay depending on our usage. Every service will have different features and limitations, so it is important to check with the documentation before using these APIs.

# 25 Project: Stock and Crypto Market API

**Alpha Vantage** ([https://www.alphavantage.co/](https://www.alphavantage.co/)) is an API with a free tier for getting stock and crypto market data. You have to get an API key to use their services. Just follow this link to do so: [https://www.alphavantage.co/support/#api-key](https://www.alphavantage.co/support/#api-key). At the time of this writing, the free tier limits are 5 API calls per minute and 500 API calls per day. Admittedly, these are not very permissive limits but should be good for our learning purposes.

![](resources/i_imgur_com---pJr7PU7.png)

Let’s initiate a new project by creating a folder with `main.js` and `package.json` files in it. We will also install the `node-fetch` library.

```
1 mkdir project-alpha-vantage
2 cd project-alpha-vantage
3 npm init -y
4 npm install --save node-fetch@2.6.1
```

Just like when using a programming library, we need to check the documentation with an API service to understand all the available functionality. Looking at Alpha Vantage’s documentation will show us the full scope of the things we can do with this API.

## Finding the Stock Symbol for a Company

One of this API’s functionalities is to find the **stock symbol** (**stock ticker**) for a given company name. A stock symbol is a unique identifier for a company that is on the stock market. We will need to know the stock symbol of a company to look up information about it. We can use the **Search Endpoint (**[https://www.alphavantage.co/documentation/#symbolsearch](https://www.alphavantage.co/documentation/#symbolsearch)) on Alpha Vantage to get the stock symbol. We need to provide a couple of arguments to this **API endpoint** to use it. An **endpoint** is basically a point of contact with the API. Since this a web API, the point of contact lives on a web address (**URL**).

```
1 https://www.alphavantage.co/query?function=SYMBOL_SEARCH&keywords=tesco&apikey=demo
```

Whatever comes after the `?` in this URL are the arguments that are passed to this endpoint. We can think of them as being similar to arguments passed into a **CLI** Node program to modify its behavior. We will pass the `SYMBOL_SEARCH` value into the `function` parameter to indicate we want to use the **Search Endpoint.** We will pass a **search keyword** to the `keywords` parameter. And we need to pass our **API key** to the `apikey` parameter.

```
 1 const fetch = require("node-fetch");
 2 const { API_KEY } = require("./config");
 3 
 4 async function getSymbol(companyName) {
 5   const endpointUrl = `https://www.alphavantage.co/query?function=SYMBOL_SEARCH&keyw\
 6 ords=${companyName}&apikey=${API_KEY}`;
 7   const response = await fetch(endpointUrl);
 8   const data = await response.json();
 9 
10   console.log(data);
11 }
12 
13 async function main() {
14   const companyName = "tesla";
15   await getSymbol(companyName);
16 }
17 
18 main();
```

apis-03-project-news-api/01/main.js

I have created a `config.js` file for this example to store the API key. Here, we are importing the `API_KEY` from that file. Remember that API keys are like passwords, so we should keep them safe and secure. The config file looks something like this.

```
1 const API_KEY = "YOUR_API_KEY_HERE";
2 
3 module.exports = {
4   API_KEY,
5 };
```

apis-03-project-news-api/01/config.js

We are also importing the `node-fetch` module. We have created a function called `getSymbol` that has the URL for the Search Endpoint as a **template literal**. We use the `companyName` argument and the API key to populate the values of this template literal.

```
1 async function getSymbol(companyName) {
2   const endpointUrl = `https://www.alphavantage.co/query?function=SYMBOL_SEARCH&keyw\
3 ords=${companyName}&apikey=${API_KEY}`;
4   const response = await fetch(endpointUrl);
5   const data = await response.json();
6 
7   console.log(data);
8 }
```

apis-03-project-news-api/01/main.js

This endpoint returns an object with a property called `bestMatches` that has an array for all the matches that the keyword we have provided has generated. This array’s items are objects that have a property called `9\. matchScore` that displays a confidence score for the match. The higher the confidence, the more likely is a positive match.

Unfortunately, the first match I am getting on my end for using `tesla` as the search keyword is not what I want at all.

```
 1 {
 2   bestMatches: [
 3     {
 4       '1\. symbol': 'TL0.DEX',
 5       '2\. name': 'Tesla',
 6       '3\. type': 'Equity',
 7       '4\. region': 'XETRA',
 8       '5\. marketOpen': '08:00',
 9       '6\. marketClose': '20:00',
10       '7\. timezone': 'UTC+01',
11       '8\. currency': 'EUR',
12       '9\. matchScore': '1.0000'
13     },
14 		...
15 ]
```

It seems like the endpoint is prioritizing the results from the European markets. I guess this might be because I am currently located in Germany. I wasn’t able to find a way to modify this behavior. I don’t use the European markets to trade stocks, so I would prefer to get the `United States` region’s result.

We will update the logic to return the result from the `United States` region with the highest match score. The function will return a `null` if there is no such match.

```
 1 const fetch = require("node-fetch");
 2 const { API_KEY } = require("./config");
 3 
 4 function filterSymbolSearchResults(searchResults) {
 5   const matches = searchResults.bestMatches;
 6   const matchesFromUS = matches.filter((symbolData) => {
 7     if (symbolData["4\. region"] === "United States") {
 8       return true;
 9     }
10   });
11 
12   const match = (matchesFromUS[0] && matchesFromUS[0]["1\. symbol"]) || null;
13 
14   return match;
15 }
16 
17 async function getSymbol(companyName) {
18   const endpointUrl = `https://www.alphavantage.co/query?function=SYMBOL_SEARCH&keyw\
19 ords=${companyName}&apikey=${API_KEY}`;
20   const response = await fetch(endpointUrl);
21   const data = await response.json();
22 
23   return filterSymbolSearchResults(data);
24 }
25 
26 async function main() {
27   const companyName = "tesla";
28   const symbol = await getSymbol(companyName);
29   console.log(symbol);
30 }
31 
32 main();
```

apis-03-project-news-api/02/main.js

`filterSymbolSearchResults` function parses the search results to return the `symbol` property of the first object that is from the `United States` region. It returns `null` if no such object exists.

```
 1 function filterSymbolSearchResults(searchResults) {
 2   const matches = searchResults.bestMatches;
 3   const matchesFromUS = matches.filter((symbolData) => {
 4     if (symbolData["4\. region"] === "United States") {
 5       return true;
 6     }
 7   });
 8 
 9   const match = (matchesFromUS[0] && matchesFromUS[0]["1\. symbol"]) || null;
10 
11   return match;
12 }
```

apis-03-project-news-api/02/main.js

Notice how we are using square brackets to access these property names because they have a number, a dot, and a space character in them. These characters prohibit us from using the **dot notation** to access these properties.

We now have a function that returns the symbol for a given company name. Let’s tidy up our program a bit by moving the `getSymbol` function into a file called `stocks.js`. We will be using this file as a module to contain and export the reusable functions we create.

```
 1 const fetch = require("node-fetch");
 2 const { API_KEY } = require("./config");
 3 
 4 function filterSymbolSearchResults(searchResults) {
 5   const matches = searchResults.bestMatches;
 6   const matchesFromUS = matches.filter((symbolData) => {
 7     if (symbolData["4\. region"] === "United States") {
 8       return true;
 9     }
10   });
11 
12   const match = (matchesFromUS[0] && matchesFromUS[0]["1\. symbol"]) || null;
13 
14   return match;
15 }
16 
17 async function getSymbol(companyName) {
18   const endpointUrl = `https://www.alphavantage.co/query?function=SYMBOL_SEARCH&keyw\
19 ords=${companyName}&apikey=${API_KEY}`;
20   const response = await fetch(endpointUrl);
21   const data = await response.json();
22 
23   return filterSymbolSearchResults(data);
24 }
25 
26 module.exports = {
27   getSymbol,
28 };
```

apis-03-project-news-api/03/stocks.js

We will only export the `getSymbol` function from this module for now. `filterSymbolSearchResults` does not need to be exported since it is only used by the `getSymbol`. The outside world doesn’t need to know about the `filterSymbolSearchResults` function. It is essentially an **implementation detail** of the `getSymbol` function.

Our main file is looking much lighter now.

```
1 const { getSymbol } = require("./stocks");
2 
3 async function main() {
4   const companyName = "tesla";
5   const symbol = await getSymbol(companyName);
6   console.log(symbol);
7 }
8 
9 main();
```

apis-03-project-news-api/03/main.js

This might be a good opportunity to make this program accept **command-line arguments.**

```
 1 const { getSymbol } = require("./stocks");
 2 
 3 function getCommandLineArgument() {
 4   const argument = process.argv[2];
 5 
 6   return argument;
 7 }
 8 
 9 async function main() {
10   const companyName = getCommandLineArgument();
11   if (!companyName) {
12     console.log("Please provide a company name to continue.");
13     return;
14   }
15   const symbol = await getSymbol(companyName);
16   console.log(symbol);
17 }
18 
19 main();
```

apis-03-project-news-api/04/main.js

We have created a function called `getCommandLineArgument` that basically returns the first argument passed into this Node.js file. We have also added a logic that will terminate the program if no argument is provided.

Now we can call this function with any company name, and it should return the stock ticker for that company.

```
1 node main.js apple
```

Running this command returns the symbol `APLE`. That is actually incredibly inaccurate. `APLE` is the ticker symbol for **Apple Hospitality REIT Inc,** which is most likely not what we were thinking of when we type `apple`. This is not an acceptable performance from a search service, but it will have to do for our learning purposes. After all, we are using this API for free. We get the expected result when we pass `"apple inc"` as an argument.

```
1 node main.js "apple inc"
```

## Getting the Price Data for a Stock

Alpha Vantage has another endpoint called the **Quote Endpoint** that returns the end-of-day stock price data for a given symbol. Let’s start consuming this endpoint in our program.

```
 1 const fetch = require("node-fetch");
 2 const { API_KEY } = require("./config");
 3 
 4 async function getStockQuote(symbol) {
 5   const endpointUrl = `https://www.alphavantage.co/query?function=GLOBAL_QUOTE&symbo\
 6 l=${symbol}&apikey=${API_KEY}`;
 7   const response = await fetch(endpointUrl);
 8   const data = await response.json();
 9 
10   return data;
11 }
12 
13 async function getStockPrice(symbol) {
14   const data = await getStockQuote(symbol);
15 
16   return data["Global Quote"]["05\. price"];
17 }
```

apis-03-project-news-api/05/main.js

We have created a function called `getStockQuote` that gets the quote data (full price data) for a stock symbol. We have also created a function called `getStockPrice` that uses `getStockData` to return the price data that we are interested in.

Now we can export and use the `getStockPrice` function in our main file to get the stock price for a given company name.

```
 1 const { getSymbol, getStockPrice } = require("./stocks");
 2 
 3 function getCommandLineArgument() {
 4   const argument = process.argv[2];
 5 
 6   return argument;
 7 }
 8 
 9 async function main() {
10   const companyName = getCommandLineArgument();
11   if (!companyName) {
12     console.log("Please provide a company name to continue.");
13     return;
14   }
15   const symbol = await getSymbol(companyName);
16   const price = await getStockPrice(symbol);
17 
18   console.log(`The current price for ${symbol} is $${price}`);
19 }
20 
21 main();
```

apis-03-project-news-api/05/main.js

We have updated the `main` function to get the stock symbol for a given company name and then get its stock price. After that, we display a message that shows the stock symbol and the price together.

## Getting Company Financials

Alpha Vantage has an endpoint called **Company Overview** that provides a lot of useful financial metrics for a given stock symbol. You can check the endpoint yourself to see what kind of data is available there. In this example, we will make use of the `52WeekHigh` value. `52WeekHigh` is the highest price that this stock had in a year. We will update our program to tell us how far the current price is from the `52WeekHigh` percentage-wise.

**Company Overview** **Endpoint** URL has similar parameters to the **Quote Endpoint**. It has `function`, `symbol` and `apikey` as parameters.

```
1 async function getCompanyOverview(symbol) {
2   const endpointUrl = `https://www.alphavantage.co/query?function=OVERVIEW&symbol=${\
3 symbol}&apikey=${API_KEY}`;
4   const response = await fetch(endpointUrl);
5   const data = await response.json();
6 
7   return data;
8 }
```

apis-03-project-news-api/06/stocks.js

We will export the `getCompanyOverview` function and use it in our main file.

```
 1 const { getSymbol, getStockPrice, getCompanyOverview } = require("./stocks");
 2 
 3 function getCommandLineArgument() {
 4   const argument = process.argv[2];
 5 
 6   return argument;
 7 }
 8 
 9 async function main() {
10   const companyName = getCommandLineArgument();
11   if (!companyName) {
12     console.log("Please provide a company name to continue.");
13     return;
14   }
15   const symbol = await getSymbol(companyName);
16   const price = parseFloat(await getStockPrice(symbol));
17   const companyData = await getCompanyOverview(symbol);
18 
19   const fiftyTwoWeekHigh = parseFloat(companyData["52WeekHigh"]);
20 
21   const percentageDiffFrom52WeekHigh =
22     ((fiftyTwoWeekHigh - price) * 100) / price;
23 
24   console.log(`The current price for ${symbol} is $${price}.
25 It is ${percentageDiffFrom52WeekHigh}% below ${fiftyTwoWeekHigh}.`);
26 }
27 
28 main();
```

apis-03-project-news-api/06/main.js

We are using the `getCompanyOverview` function to get the company overview. We are then using the `52WeekHigh` to calculate the percentage difference of the current stock price to this stock’s highest price in the past year.

```
1 const companyData = await getCompanyOverview(symbol);
2 
3 const fiftyTwoWeekHigh = parseFloat(companyData["52WeekHigh"]);
4 
5 const percentageDiffFrom52WeekHigh = ((fiftyTwoWeekHigh - price) * 100) / price;
```

apis-03-project-news-api/06/main.js

The assumption here is that if the stock was at that price at one point, it could reach that price again sometime in the future. Getting the percentage difference gives us an idea about the stock’s percentage upside - what could be the highest value that this stock attain. Of course, this is a very coarse estimation but is still useful to see.

## Getting the Price in Bitcoin

The last thing we will do here is to use Alpha Vantage to get some cryptocurrency-related data. We will use the **Currency Exchange Endpoint** to get the exchange rate of Bitcoin (**BTC**) to American Dollar (**USD**) and then use that exchange rate to calculate the stock price in BTC.

**Currency Exchange Endpoint** URL has `from_currency`, `to_currency`, and `apikey` as parameters.

We will first add a function that will get the exchange rate for any given currency pair.

```
1 async function getExchangeRate(from, to) {
2   const endpointUrl = `https://www.alphavantage.co/query?function=CURRENCY_EXCHANGE_\
3 RATE&from_currency=${from}&to_currency=${to}&apikey=${API_KEY}`;
4   const response = await fetch(endpointUrl);
5   const data = await response.json();
6 
7   return data["Realtime Currency Exchange Rate"]["5\. Exchange Rate"];
8 }
```

apis-02-project-stock-api/07/stocks.js

We are looking for the value under the `["5\. Exchange Rate"]` key of the `Realtime Currency Exchange Rate` field of the returned object.

We are then going to add another function called `getValueInBitcoin` that would get a USD value and calculate the corresponding BTC value by making use of the exchange rate data using the `getExchangeRate` function.

```
1 async function getValueInBitcoin(usdValue) {
2   const btcToUSDExchangeRate = await getExchangeRate("BTC", "USD");
3   const valueInBtc = usdValue / parseFloat(btcToUSDExchangeRate);
4 
5   return valueInBtc;
6 }
```

apis-02-project-stock-api/07/stocks.js

We are dividing the `usdValue` with the BTC to USD exchange value to calculate a USD price in Bitcoins. We will import this file inside the main file and use it to calculate the `priceInBTC`.

```
1 const priceInBTC = await getValueInBitcoin(price);
```

apis-02-project-stock-api/07/main.js

This is what the final code looks like:

```
 1 const {
 2   getSymbol,
 3   getStockPrice,
 4   getCompanyOverview,
 5   getValueInBitcoin,
 6 } = require("./stocks");
 7 
 8 function getCommandLineArgument() {
 9   const argument = process.argv[2];
10 
11   return argument;
12 }
13 
14 async function main() {
15   const companyName = getCommandLineArgument();
16   if (!companyName) {
17     console.log("Please provide a company name to continue.");
18     return;
19   }
20   const symbol = await getSymbol(companyName);
21   const price = parseFloat(await getStockPrice(symbol));
22   const priceInBTC = await getValueInBitcoin(price);
23 
24   const companyData = await getCompanyOverview(symbol);
25 
26   const fiftyTwoWeekHigh = parseFloat(companyData["52WeekHigh"]);
27 
28   const percentageDiffFrom52WeekHigh =
29     ((fiftyTwoWeekHigh - price) * 100) / price;
30 
31   console.log(`The current price for ${symbol} is $${price}.
32 It is ${percentageDiffFrom52WeekHigh}% below ${fiftyTwoWeekHigh}.
33 It is worth ${priceInBTC} in Bitcoin.
34 `);
35 }
36 
37 main();
```

apis-02-project-stock-api/07/main.js

Alpha Vantage has tons of other endpoints, including data on the Forex markets. The free tier call limits can be a bit restricting, but they can be good enough for personal usage.

## Summary

In this chapter, we have looked at the Alpha Vantage API to understand how to leverage APIs in our projects. Alpha Vantage is a simple to use API for getting stock, cryptocurrency, and foreign exchange data. When using an API, it is essential to read their documentation to get a sense of the available functionality. We have consumed the Alpha Vantage API by making HTTP calls to an endpoint by providing our API key and other necessary arguments.

The free tier of Alpha Vantage allows for rather limited usage. Once you start using APIs more frequently, you might be able to find other options that are better suited for your use cases.

# 26 Project: News API

**News API** ([https://newsapi.org/](https://newsapi.org/)), as the name suggests, is an **API** for getting news data. It is free to use for developers with certain limitations. You can find more information on this at their pricing page: [https://newsapi.org/pricing](https://newsapi.org/pricing).

![](resources/i_imgur_com---q5XlpcZ.png)

## Using NewsAPI with a Client Library

To start using this API, we have to register and get an API key. Once we have the key, we can either use the **URL endpoints** or the **unofficial** **client library** to consume the API. A **client library** is just a wrapper around the API in different programming languages to make it easier to use. It is a convenient abstraction around making **HTTP requests** to the URL endpoints. An **unofficial** **client library** is a library that is **not** published by the API developers. This means that it might not always be up-to-date with the underlying API. In this case, the unofficial library is linked on the News API pages, so we can trust it to be fairly reliable.

The Node.js client library for News API is available at [https://github.com/bzarras/newsapi](https://github.com/bzarras/newsapi). Let’s create a folder for this project and install the client library.

```
1 mkdir project-news-api
2 cd project-news-api
3 npm init -y
4 npm install --save newsapi@2.4.1
```

We will first create a `config.js` file that will export the API key.

```
1 const API_KEY = "YOUR_API_KEY";
2 
3 module.exports = {
4   API_KEY,
5 };
```

Example Config File

We will also create a `main.js` file. We will import this `API_KEY` variable inside the `main.js` file alongside the `newsapi` library.

```
1 const NewsAPI = require("newsapi");
2 const { API_KEY } = require("./config");
3 
4 const newsapi = new NewsAPI(API_KEY);
5 console.log(newsapi);
```

apis-03-project-news-api/01/main.js

We are **console logging** the `newsapi` variable to ensure everything is loaded properly. **newsapi** is a **Promise-based** library. This means that we can use `async-await` to work with it.

```
 1 const NewsAPI = require("newsapi");
 2 const { API_KEY } = require("./config");
 3 
 4 const newsapi = new NewsAPI(API_KEY);
 5 
 6 async function main() {
 7   const response = await newsapi.v2.everything({
 8     q: "covid",
 9     language: "en",
10   });
11 
12   console.log(response.articles);
13 }
14 
15 main();
```

apis-03-project-news-api/02/main.js

We are using the `v2.everything` method to get every news for the given query (`covid` in this case) and the given language. This query would return the results for the current date. We can also specify a date range. The free tier allows us to get a maximum of 100 results from up to one month ago. We will enter a date range to the `from` and `to` fields. In this example, the dates are based on when I wrote this chapter, so you might need to update it with newer dates.

```
 1 const NewsAPI = require("newsapi");
 2 const { API_KEY } = require("./config");
 3 
 4 const newsapi = new NewsAPI(API_KEY);
 5 
 6 async function main() {
 7   const response = await newsapi.v2.everything({
 8     q: "covid",
 9     language: "en",
10     from: "2021-02-02",
11     to: "2021-03-02",
12     pageSize: 100,
13   });
14 
15   console.log(response.articles);
16 }
17 
18 main();
```

apis-03-project-news-api/03/main.js

## Adding Day.js

We can improve this code in a couple of ways. The dates for the `from` and `to` ranges are currently hardcoded. We can use a date formatting library to handle the dates programmatically. We will be using **Day.js** for this purpose. Let’s install it.

```
1 npm install --save dayjs@1.10.4
```

We can use **Day.js** to easily get formatted dates and calculating time ranges.

```
 1 const NewsAPI = require("newsapi");
 2 const { API_KEY } = require("./config");
 3 const dayjs = require("dayjs");
 4 
 5 const newsapi = new NewsAPI(API_KEY);
 6 
 7 async function main() {
 8   const now = dayjs();
 9   const dateFormat = "YYYY-MM-DD";
10 
11   const today = now.format(dateFormat);
12   const monthAgo = now.subtract(1, "month").format(dateFormat);
13 
14   const response = await newsapi.v2.everything({
15     q: "covid",
16     language: "en",
17     from: monthAgo,
18     to: today,
19     pageSize: 100,
20   });
21 
22   console.log(response.articles);
23 }
24 
25 main();
```

apis-03-project-news-api/04/main.js

We are using the `dayjs` function to get the current time and the `.format` method to format it to use in the **newsapi**. We are also using the `subtract` method to calculate what the date was a month ago.

```
1 const now = dayjs();
2 const dateFormat = "YYYY-MM-DD";
3 
4 const today = now.format(dateFormat);
5 const monthAgo = now.subtract(1, "month").format(dateFormat);
```

apis-03-project-news-api/04/main.js

## Performing Sentiment Analysis

We will also perform a **sentiment analysis** of the news articles. Sentiment analysis is the classification of emotions within text data using **natural language processing** (**NLP**) techniques. There are various ways of performing sentiment analysis, and some of those involve using **machine-learning (ML)** and **artificial intelligence (AI).** We can consume ML and AI APIs from our application to do natural-language processing, but there are also Node.js libraries that we can use.

In this example, we will be using a library called **sentiment** to do sentiment analysis. Let’s install it using the following command.

```
1 npm install --save sentiment@5.0.2
```

When we pass a text into the `sentiment.analyze` function, it **tokenizes** the string and assigns a positive or negative score to each token. We can think of **tokens** as the words that make up the text. The resulting object returned from the `analyze` function has four fields that are relevant for us. `score`, `comparative`, `negative`, and `positive`.

`score` field tells us the sentiment score for the text. `comparative` is the sentiment score as well, but it is **normalized** for the length of the text. A longer sentence will have more words, which means there is more chance that it will have a higher (or lower) score in total. By normalizing the text, we divide the score by the text length, which allows us to compare different sentences without worrying about the variance in text length.

`negative` is an array that holds the tokens (words) that have a negative meaning. `positive` array is for the words that have a positive meaning.

Let’s use this library with a sentence like `I love coding in JavaScript`.

```
1 const Sentiment = require("sentiment");
2 const sentiment = new Sentiment();
3 
4 const analysis = sentiment.analyze("I love coding in JavaScript");
5 console.log(analysis); // score: 3, comparative: 0.6, positive: ['love'], negative: \
6 []
```

apis-03-project-news-api/05/main.js

In this example, the sentiment score is above 0, which means the sentiment is positive. The positive sentiment is calculated based on the presence of the word `love`.

We will do sentiment analysis based on the news titles for the given time period. We will add up the sentiment in all news articles to see if it is positive or negative in aggregate. We will also check to see what words contribute to the resulting sentiment.

```
 1 const NewsAPI = require("newsapi");
 2 const { API_KEY } = require("./config");
 3 const dayjs = require("dayjs");
 4 const Sentiment = require("sentiment");
 5 
 6 const newsapi = new NewsAPI(API_KEY);
 7 const sentiment = new Sentiment();
 8 
 9 async function main() {
10   const now = dayjs();
11   const dateFormat = "YYYY-MM-DD";
12 
13   const today = now.format(dateFormat);
14   const monthAgo = now.subtract(1, "month").format(dateFormat);
15 
16   const response = await newsapi.v2.everything({
17     q: "covid",
18     language: "en",
19     from: monthAgo,
20     to: today,
21     pageSize: 100,
22   });
23 
24   const articles = response.articles.map((article) => {
25     return article.title;
26   });
27 
28   console.log(articles);
29   console.log(sentiment.analyze(articles[0]));
30 }
31 
32 main();
```

apis-03-project-news-api/06/main.js

Here, we are creating an array called `articles` that only consists of the news titles. We will be feeding each title to sentiment analysis to calculate a sentiment score.

```
1 const articles = response.articles.map((article) => {
2   return article.title;
3 });
4 
5 console.log(articles);
6 console.log(sentiment.analyze(articles[0]));
```

apis-03-project-news-api/06/main.js

In the example above, we only calculate the first item’s sentiment to see if everything is working. Once we ensure everything is working as expected, we can analyze the sentiment for all of the articles.

```
 1 const NewsAPI = require("newsapi");
 2 const { API_KEY } = require("./config");
 3 const dayjs = require("dayjs");
 4 const Sentiment = require("sentiment");
 5 
 6 const newsapi = new NewsAPI(API_KEY);
 7 const sentiment = new Sentiment();
 8 
 9 async function main() {
10   const now = dayjs();
11   const dateFormat = "YYYY-MM-DD";
12 
13   const today = now.format(dateFormat);
14   const monthAgo = now.subtract(1, "month").format(dateFormat);
15 
16   const response = await newsapi.v2.everything({
17     q: "covid",
18     language: "en",
19     from: monthAgo,
20     to: today,
21     pageSize: 100,
22   });
23 
24   const articles = response.articles.map((article) => {
25     return article.title;
26   });
27 
28   let totalSentiment = 0;
29   let positiveWords = [];
30   let negativeWords = [];
31 
32   articles.forEach((article) => {
33     const sentimentData = sentiment.analyze(article);
34     const sentimentScore = sentimentData.comparative;
35     positiveWords = [...positiveWords, ...sentimentData.positive];
36     negativeWords = [...negativeWords, ...sentimentData.negative];
37 
38     totalSentiment = totalSentiment + sentimentScore;
39   });
40 
41   if (totalSentiment < 0) {
42     console.log(
43       `Sentiment is negative with score of ${totalSentiment}. Words that describe th\
44 e sentiment are: ${negativeWords.join(
45         ", "
46       )}...`
47     );
48   } else {
49     console.log(
50       `Sentiment is positive with score of ${totalSentiment}. Words that describe th\
51 e sentiment are: ${positiveWords.join(
52         ", "
53       )}...`
54     );
55   }
56 }
57 
58 main();
```

apis-03-project-news-api/07/main.js

Here we have created 3 new variables, `totalSentiment`, `positiveWords`, and `negativeWords`. We go through every article and calculate the sentiment score. We add the resulting `comparative` score into the `totalSentiment` variable and add the words contributing to that sentiment score into the `positiveWords` and `negativeWords` array.

```
 1 let totalSentiment = 0;
 2 let positiveWords = [];
 3 let negativeWords = [];
 4 
 5 articles.forEach((article) => {
 6   const sentimentData = sentiment.analyze(article);
 7   const sentimentScore = sentimentData.comparative;
 8   positiveWords = [...positiveWords, ...sentimentData.positive];
 9   negativeWords = [...negativeWords, ...sentimentData.negative];
10 
11   totalSentiment = totalSentiment + sentimentScore;
12 });
```

apis-03-project-news-api/07/main.js

We then check to see if the `totalSentiment` is negative or positive. We display a different message for both of those options.

```
 1 if (totalSentiment < 0) {
 2   console.log(
 3     `Sentiment is negative with score of ${totalSentiment}. Words that describe the \
 4 sentiment are: ${negativeWords.join(
 5       ", "
 6     )}...`
 7   );
 8 } else {
 9   console.log(
10     `Sentiment is positive with score of ${totalSentiment}. Words that describe the \
11 sentiment are: ${positiveWords.join(
12       ", "
13     )}...`
14   );
15 }
```

apis-03-project-news-api/07/main.js

Currently, the query that we use for the news articles is **hardcoded**. Let’s make it so that we can pass an argument to this function from the command-line.

Just like in the previous chapter, we will create a function called `getCommandLineArgument` that will get the extra argument that is passed into this program from the command-line.

```
1 function getCommandLineArgument() {
2   const argument = process.argv[2];
3 
4   return argument;
5 }
```

apis-03-project-news-api/08/main.js

We are then going to use this function to get the query that is passed into our program. We will terminate the program if no query is provided.

```
 1 const query = getCommandLineArgument();
 2 if (!query) {
 3   console.log("Please provide a search query to continue.");
 4   return;
 5 }
 6 
 7 const response = await newsapi.v2.everything({
 8   q: query,
 9   language: "en",
10   from: monthAgo,
11   to: today,
12   pageSize: 100,
13 });
```

apis-02-project-stock-api/08/main.js

And that should be it! We can now run this program to search the news for any word and understand the sentiment around it. We can even combine this program with the previous program that we have wrote to get the sentiment and the financial information around any company that trades in the stock market!

Here is what the final code looks like:

```
 1 const NewsAPI = require("newsapi");
 2 const { API_KEY } = require("./config");
 3 const dayjs = require("dayjs");
 4 const Sentiment = require("sentiment");
 5 
 6 const newsapi = new NewsAPI(API_KEY);
 7 const sentiment = new Sentiment();
 8 
 9 function getCommandLineArgument() {
10   const argument = process.argv[2];
11 
12   return argument;
13 }
14 
15 async function main() {
16   const now = dayjs();
17   const dateFormat = "YYYY-MM-DD";
18 
19   const today = now.format(dateFormat);
20   const monthAgo = now.subtract(1, "month").format(dateFormat);
21 
22   const query = getCommandLineArgument();
23   if (!query) {
24     console.log("Please provide a search query to continue.");
25     return;
26   }
27 
28   const response = await newsapi.v2.everything({
29     q: query,
30     language: "en",
31     from: monthAgo,
32     to: today,
33     pageSize: 100,
34   });
35 
36   const articles = response.articles.map((article) => {
37     return article.title;
38   });
39 
40   let totalSentiment = 0;
41   let positiveWords = [];
42   let negativeWords = [];
43 
44   articles.forEach((article) => {
45     const sentimentData = sentiment.analyze(article);
46     const sentimentScore = sentimentData.comparative;
47     positiveWords = [...positiveWords, ...sentimentData.positive];
48     negativeWords = [...negativeWords, ...sentimentData.negative];
49 
50     totalSentiment = totalSentiment + sentimentScore;
51   });
52 
53   if (totalSentiment < 0) {
54     console.log(
55       `Sentiment is negative with score of ${totalSentiment}. Words that describe th\
56 e sentiment are: ${negativeWords.join(
57         ", "
58       )}...`
59     );
60   } else {
61     console.log(
62       `Sentiment is positive with score of ${totalSentiment}. Words that describe th\
63 e sentiment are: ${positiveWords.join(
64         ", "
65       )}...`
66     );
67   }
68 }
69 
70 main();
```

apis-03-project-news-api/08/main.js

## Summary

In this chapter, we have used the **News API** to get the news data for a given keyword. We could again have used the `node-fetch` library to interface with the API, but News API provides an **unofficial client library** for Node.js, which is slightly easier to use. A **client library** is just an abstraction for communicating with the API using **HTTP**.

We have also used a couple of other libraries in this program. We have used the **Day.js** library to make working with dates easier. We have also used a library called **sentiment** to perform **sentiment analysis** for the news articles from the **News API.** This helped us build a program that can analyze the world’s sentiment in a given date range and compare it to the sentiment in other times. We can also use this to see if the sentiment is improving or degrading over time.

# 27 Closing Words

My purpose for writing this book was to teach you programming from scratch by providing cool and practical exercises along the way. I hope you enjoyed it.

If you find any issues or have suggestions or comments on improving the book, I would love to hear them. Please drop me a line at awesomecodingco@gmail.com.

Feel free to connect with me on [Twitter](https://twitter.com/inspiratory) and [Linkedin](https://www.linkedin.com/in/enginarslan/). You can learn more about my other works on my [website](http://www.enginarslan.com/).

Thanks a lot for reading!

Engin Arslan