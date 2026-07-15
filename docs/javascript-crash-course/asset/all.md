![](cover.jpeg)

# JavaScript Crash Course : Go from "Zero" To "Hero" in 12 Easy Lessons

#### by Dr. Code

[http://www.EbooksByDr.Code.com](http://www.amazon.com/-/e/B00D3KXM7C)

Image on cover courtesy of metrue / FreeDigitalPhotos.net

**JavaScript Crash Course: Go From "Zero" To "Hero" In 12 Easy Lessons** Copyright © 2013 by Dr. Code

All rights reserved. No part of this book may be reproduced in any form without permission in writing from the author. Reviewers may quote brief passages in reviews.

## Disclaimer And FTC Notice

No part of this publication may be reproduced or transmitted in any form or by any means, mechanical or electronic, including photocopying and recording or by any information storage and retrieval system, or transmitted by email without permission in writing from the publisher.

While all attempts have been made to verify the information provided in this publication, neither the author nor the publisher assumes any responsibility for errors, omissions, or contrary interpretations of the subject matter herein.

This book is for entertainment purposes only. The views expressed are those of the author alone, and should not be taken as expert instruction or commands. The reader is responsible for his or her own actions.

Adherence to all applicable laws and regulations, including international, federal, state, and local governing professional licensing, business practices, advertising, and all other aspects of doing business in the US, Canada, or any other jurisdiction is the sole responsibility of the purchaser or reader.

Neither the author nor the publisher assumes any responsibility or liability whatsoever on the behalf of the purchaser or reader of these materials.

Any perceived slight of any individual or organization is purely unintentional.

I sometimes use affiliate links in the content. This means if you decide to make a purchase, I will get a sales commission. But that doesn't mean my opinion is for sale. Every affiliate link is to products that I've personally used and found useful. Please do your own research before making any purchases online.

### About This Book

This is the fourth in a series of books that helps people learn how to build a website with code. Being able to read and write code is becoming an increasingly important skill in today's technologically sophisticated world. Those who have this skill will have a significant advantage in the job market.

JavaScript is a computer language that enables a web page to interact with its users. This book provides an introduction to the JavaScript programming language, and is meant for the complete beginner. However, it is important that you know HTML and CSS before you learn JavaScript. This book assumes that you are familiar with both. If you are unfamiliar with HTML and CSS, my ebooks entitled ["HTML Crash Course: Go From Zero To Hero In 10 Easy Lessons"](http://www.amazon.com/dp/B00D0IUT8C) and ["CSS Crash Course: Introducing CSS In 10 Easy Lessons"](http://www.amazon.com/dp/B00FFD18EE) will get you up to speed quickly.

The simple fast-paced lessons in this book will have you creating interactive web pages in no time at all! This books offers you:

*   Short and Engaging Lessons
*   Lots of Visual Aids for Quick Comprehension
*   Hands-On Activities at the end of every lesson to help you understand and practice what was learned.

### More Kindle Ebooks By Dr. Code

["HTML Crash Course: Go From "Zero" To "Hero" In 10 Easy Lessons"](http://www.amazon.com/dp/B00D0IUT8C)

["CSS Crash Course: Introducing CSS In 10 Easy Lessons"](http://www.amazon.com/dp/B00FFD18EE)

["HTML & CSS: A Programmer's Quick Reference"](http://www.amazon.com/dp/B00CN02GI4)

["PHP Crash Course: Go From "Zero" To "Hero" In 12 Easy Lessons"](http://www.amazon.com/dp/B00ILXSJN8)

## Table of Contents

[Introduction](#part0000_split_003.html_one)

[Getting Started](#part0000_split_004.html_two)

[Lesson 1: The Script Tags](#part0000_split_005.html_three)

[Lesson 2: Hello World!](#part0000_split_006.html_four)

[Lesson 3: Comments And Variables](#part0000_split_007.html_five)

[Lesson 4: Doing Math In JavaScript](#part0000_split_008.html_six)

[Lesson 5: Functions](#part0000_split_009.html_seven)

[Lesson 6: Making Decisions And Conditional Statements](#part0000_split_010.html_eight)

[Lesson 7: Loops](#part0000_split_011.html_nine)

[Lesson 8: Arrays](#part0000_split_012.html_ten)

[Lesson 9: JavaScript Pop Up Boxes](#part0000_split_013.html_eleven)

[Lesson 10: Events And Event Handlers](#part0000_split_014.html_twelve)

[Lesson 11: An Introduction To Object Oriented Programming In JavaScript](#part0000_split_015.html_thirteen)

[Lesson 12: An Introduction To Form Validation](#part0000_split_016.html_fourteen)

## Introduction

### What is Javascript?

In this day and age, websites are interactive, not static like they used to be. This dynamic nature adds so much value to the internet because websites can interact with their users instead of simply displaying information. This interaction with the user is made possible by languages such as JavaScript. JavaScript is a programming language that enables a web page to respond to user input. For example, if a user skips over a required field in an online form, you can use JavaScript to display an error message directing the user to fill out the required information. This is part of what is called "form validation", and it is a major reason that people learn JavaScript. However, that is only one of the many cool things you can do with JavaScript!

JavaScript is a client-side scripting language, which means that it runs in a browser on the user's computer. JavaScript code can be inserted directly into HTML pages, and can be executed by all modern web browsers.

![pic of computer network](images/00001.jpeg)

**Figure 1\. A computer network** (Image courtesy of jscreationzs / freedigitalphotos.net)

NOTE: A server-side scripting language is executed on the computer of your web hosting service.

## Getting Started

All you need to start building your website is a notepad++ editor. I highly recommend notepad++, because it is such an awesome coding tool that is very simple to use and it works with many different programming languages. You can download this software for free at [www.notepad-plus-plus.org](http://notepad-plus-plus.org/download/v6.3.html). Once you get to this website, just click on the big green download button and install the software on your computer.

Next, open a new file and type the following code. Save this file as `"template.html"`. Make sure you type every character exactly as shown below, otherwise you could get an error when validating your webpage.

![template](images/00002.jpeg)

Now we're ready to get started!!!

## Lesson 1: The Script Tags

JavaScript code can be placed inside an HTML document or in an external file.

### Using The Script Tags Inside Your HTML Document

JavaScript code that is placed inside an HTML document must be placed between a pair of `<script></script>` tags to differentiate it from HTML and CSS code. The `<script></script>` tags may be placed in either the `<head>` or `<body>` section of an HTML document, or both. In fact, you can create as many pairs of `<script></script>` tags as you want or need. When in the `<head>` section, the `<script></script>` tags are positioned after the `<meta>` tag. When in the `<body>` section, they can be placed anywhere as long as they are between the `<body></body>` tags. However, in general, it is best to place as much of your JavaScript code as possible in the `<head>` section, because the `<head>` of the document is rendered before the `<body>`.

![html doc with script tags](images/00003.jpeg)

Because JavaScript is the most popular scripting language used today, you don't have to use the `type` attribute inside the opening `<script>` tag when creating a web page in HTML5\. However, in older versions of HTML, you must specify that you are placing JavaScript code inside the `<script></script>` tags, by using the `type` attribute with a value of `"text/javascript"`. This book assumes that you are using HTML5, so the script tags will not have the `type` attribute specified.

![script tags](images/00004.jpeg)

### Using An External JavaScript File

A more efficient way to add JavaScript code to your webpage is to use an external JavaScript source file. Using an external JavaScript file makes your code easier to read because your JavaScript code is separated from your HTML code. Another benefit is that you can effortlessly apply your JavaScript code to multiple webpages using this method.

You can call an external JavaScript file by using the `"src"` attribute in the opening `<script>` tag as follows: `<script src="filename.js">`. An external JavaScript file has a `".js"` extension, and contains only JavaScript statements. It is important to note that an external JavaScript source file does not contain a `<script>` element. The `<script>` element is located only within the HTML document that calls the JavaScript source file.

You can call an external JavaScript source file in either the `<head>` section or in the `<body>` section of your HTML document. However, when you call an external JavaScript file, any JavaScript statements in between the `<script></script>` tags will be ignored.

![how to use the source attribute](images/00005.jpeg)

## Lesson 2: Hello World!

JavaScript code is made up of statements. The purpose of a statement is to tell the browser what to do. A statement in JavaScript is comparable to a sentence in the English language, except each statement must end with a semicolon `(";")` instead of a period`(".")`.

Now we will learn our very first JavaScript statement, the `document.write();` statement. This statement enables you to write text on your web page, however, it does not include a line break. Any text that you want to write to your browser window should be enclosed in quotation marks ("") and placed between the parenthesis of the `document.write();` statement as follows: `document.write("text in here");`.

#### Now It's Your Turn To Practice:

We will now type our very first JavaScript statement which will print the words <samp class="calibre11">"Hello World!"</samp> on our web page. Open your `"template.html"` file and add the following code between the `<script></script>` tags in the body section of your HTML document:

![code for hello world example](images/00006.jpeg)

Save the file as "`hello.html`" and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00007.jpeg)

#### More Practice:

Now let's practice using an external JavaScript source file. Cut out the JavaScript code from between the `<script></script>` tags and paste them into a new file in your Notepad++ editor. Save the new file as "`myscript.js`". Your `"myscript.js"` file should look as follows:

![script](images/00008.jpeg)

NOTE: There are no `<script></script>` tags inside the external JavaScript source file.

Next, open your `"hello.html"` file in Notepad++ and add the `"src"` attribute to the opening `<script>` tag to link your JavaScript source file to your HTML document as follows:

![script tags](images/00009.jpeg)

Save your `"hello.html"` file and launch it in Chrome or the browser of your choice. Your browser window should look the same as before, displaying the message <samp class="calibre11">Hello World! I Love JavaScript!</samp>.

## Lesson 3: Comments And Variables

### Comments

Comments are used to make your JavaScript code more readable. You can use comments to explain your code so it is easier to understand. The computer will ignore any text within a comment, because they are meant to be read by humans, not computers.

There are two types of comments in JavaScript, single line comments and multi-line comments. Single line comments begin with a double forward slash `//`. Multi-line comments, on the other hand, begin with a forward slash and an asterisk `/*` and end with an asterisk and a forward slash `*/`. If you are using Notepad++, the comment text will automatically turn green when you use the comment symbols. An example of each type of comment is given below:

![code for comments example](images/00010.jpeg)

NOTE: Another way comments are commonly used is to temporarily disable your code for testing or debugging purposes. You can put the code you want to disable within a comment and the computer will ignore the code that is within the comment. This is called **commenting out code**.

### What Is A Variable?

A variable is a name that stands for a value. Variables can represent numbers, characters, boolean values, memory locations, and much more. The value of a variable can change. Variables play an important role in computer programming because they allow programs to be flexible. Using variables in your program enables it to process different sets of data each time the program is executed.

Each variable has a name and a data type. You can give your variable any name you like, but it must conform to some basic rules. These rules are slightly different in each programming language. However, it is always a good idea to give your variables a descriptive name that reminds you of the kind of value that will be stored in the variable. For example, if you want to store a user's name in a variable, you might want to call the variable `name`. The variable's data type tells the computer what type of value is stored in the variable. In other words, it can be a number, a string, a boolean, etc.

A constant is the opposite of a variable. A constant is a value that never changes. Constants are not used as frequently as variables because they lack flexibility.

### Naming Variables In JavaScript

In JavaScript, your variable name must consist of only letters, numbers, the "$" sign, and / or underscores. Variable names can not start with a number, so you can't name your variable `1car`, but you can name it `car1`. Variables are case-sensitive, so the variable `car1` is not the same as `Car1`. Finally, you can not use a reserved word as a variable name. A **reserved word** is a word that has special meaning in a programming language. Reserved words are also called **keywords**. Reserved words are always lowercase, and they appear as blue italicized text in Notepad++. The following is a list of reserved words in JavaScript:

### Reserved Words In JavaScript

![reserved words](images/00011.jpeg)

### The Basic Data Types

Variables can be of several data types, but the most basic data types are: numerical, string, boolean, and null. Numerical variables are variables whose value is a number. The number could be a whole number or a decimal, and it could be a positive or negative number. A string variable is simply a series of characters from the keyboard that are enclosed between quotation marks. A boolean variable is used to make decisions and its value is either `true` or `false`. The null variable is an empty variable, i.e. the variable has no value at all. It is different from zero, because zero is a value.

### Declaring Variables

Before you can use a variable in your program, you have to create it. The process of creating a variable is called **declaring a variable** in programming lingo. You can declare variables by using the variable name along with the `var` keyword. For example, if you want to create a variable called `fish`, you would use the statement `var fish;`. The `var` keyword is a reserved word in JavaScript and it is used to create variables.

If you wish, you can give the variable a beginning value at the same time that you create it. This is called **initializing a variable**. You can do this by using the assignment operator ( = ) to assign the variable a value. For example, the statement `var bull = true;`, creates a variable named `bull` and gives it a beginning value of `true`.

![example for declaring variables](images/00012.jpeg)

NOTE: JavaScript variables are dynamically typed. This means that the same variable can be used as a number, and then changed to a string or boolean type. In other words, a variable does not have a fixed type and can change types in JavaScript. So for example, your variable `tiger` is of a number type. However, you can change it to a boolean type by setting its value to `false` by using the assignment statement `tiger=false;`.

#### Now It's Your Turn To Practice:

Now we will practice creating variables and printing their values to a web page. We will also practice using comments in our JavaScript code. Open your `"template.html"` file and add the following code between the `<script></script>` tags:

![code for variables and comments example](images/00013.jpeg)

NOTE: You can place this code in either the `<head>` section or the `<body>` section of your HTML document. However, make sure the code goes between a pair of `<script></script>` tags.

Save the file as `"variables.html"` and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00014.jpeg)

## Lesson 4: Doing Math In JavaScript

### Operators And Operands

A computer instruction is made up of two basic parts: operators and operands. An **operator** is a character that represents an action. For example, the plus sign (+) is an arithmetic operator that represents addition. An **operand** is the part of a computer instruction that specifies the data that is to be operated on, or manipulated. So in the expression `x + 3`, `x` and `3` are the operands.

![pic of operator](images/00015.jpeg)

### The Assignment Operator

The **assignment operator** `( = )` is used to assign a value to a variable.

### The Arithmetic Operators

The most commonly used arithmetic operators are `( + )` for addition, `( - )` for subtraction, `( * )` for multiplication, `( / )` for division, and `( % )` for modulo reduction. Modulo reduction means that you are finding the remainder from integer division. So, for example, `7 % 3` (pronounced "seven modulo three") is 1, because the remainder when you divide 3 into 7 is 1\. All of these operators may be used with both numbers and variables.

However, the addition operator `( + )` can also be used with strings. When you add two strings together, it is called **concatenation**. The code below shows how to use the addition operator to add numbers, variables, and strings.

![arithmetic operator examples](images/00016.jpeg)

### Compound Assignment Operators

Compound assignment operators make coding easier by combining the arithmetic operators with the assignment operator. The compound assignment operators are `+=, -=, *=, and /=`. They are used as shorthand for basic arithmetic statements. For example, `sum += 10;` is short for `sum = sum + 10;`. In the same way, `num -= 2;` is short for `num = num - 2;`, and `num *= 2;` is short for `num = num * 2;`. Finally, as you might have guessed, `num /= 2;` is short for `num = num / 2;`.

### The Increment Operator

The **increment operator** is the symbol `( ++ )`. It is a shorthand for incrementing the value of a numeric variable by 1\. So the statement `num++;` is shorthand for `num = num + 1;`. You can use this operator before or after the variable name. For example, if you have a variable called `num` and you want to increment it by 1, you can either write `num++;` or `++num;`. Both of these statements will increment the value of the variable `num` by 1\. The only difference is when you want to use the value of the variable `num` in a calculation or print its value to the screen. So, for example, the statement `document.write(num++);` will print the value of the variable `num` to the screen and then it will add 1 to it. The code below will print the value <samp class="calibre11">6</samp> to the screen.

![increment example code](images/00017.jpeg)

However, if we change the code slightly and put the increment operator before the variable, the computer adds 1 to the value of the variable `num` first, and then print its value to the screen. So the result of the code below is that the value of 7 is printed to the screen.

![another increment example code](images/00018.jpeg)

### The Decrement Operator

The **decrement operator** is the symbol `( -- )`. It is used to decrease the value of a variable by 1\. So the statement `num--;` is shorthand for `num = num - 1;`. This operator is very similar to the increment operator except it subtracts 1 from the value of your variable.

#### Now It's Your Turn To Practice:

We will now practice using the assignment operators. Open your "`template.html`" file and type the following code between the `<script></script>` tags in the body section of your HTML document:

![code for span example](images/00019.jpeg)

NOTE: We can use HTML tags inside the `document.write();` statement to format text. HTML tags must be enclosed in quotation marks when used inside the `document.write();` statement. In the code above, we use the `<br>` tag to insert line breaks.

Save the file as `"assignment_operators.html"` and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00020.jpeg)

## Lesson 5: Functions

### What Is A Function?

Have you ever seen how workers in an auto factory use job specialization? One worker is responsible for welding the frame, another puts on the doors, while yet another puts in the glass windows, and so on, until you have a finished auto-mobile. The huge project of building a car is broken down into smaller tasks, and each worker specializes in doing one task. Similarly, we use functions to break down a big program into smaller manageable parts. Creating a complex program is similar to building a car. It is easier if you break down the job that you want your program to do into smaller tasks that can be easily tackled. A function is similar to the worker who uses job specialization to perform his task on the assembly line. A **function** is a named block of code that performs a particular task when called.

Another reason that functions are so awesome is that functions allow us to write a bit of code once, but we can use it over and over again, as many times as we want. That not only saves us lots of time and effort, but it also makes our code easier to read.

### Defining A Function

**Defining** a function means giving our function a name and writing a block of code for it so it can do something. We define a function by using the keyword `function` along with the name we want to give our function. We can name our function anything we like, but the first character must be a letter, and the rest of the name can include letters, numbers, or underscores. By convention, programmers use function names like `getUserName`, where the first word is not capitalized, and every word after the first starts with a capital letter. This naming convention is called **camel-caps notation**.

More often than not, our function will need some kind of information from outside the function to perform its task. This "outside information" that a function needs to do its job is called a **parameter**. A function might not take any parameters, or it could take one or more parameters, depending on what it is created to do. The parameters that a function needs are placed between a pair of parenthesis ( ), after the function name.

Finally, we must write a block of code for the function so it can do something. This block of code is called the **body** of the function, and it resides between a pair of curly braces { }. The body of the function is made up of one or more JavaScript statements.

The syntax for defining a function with no parameters is as follows. Since there are no parameters, the parenthesis after the function name are left empty.

![syntax of a function](images/00021.jpeg)

The syntax for defining a function with one parameter is as follows:

![syntax of a function with one parameter](images/00022.jpeg)

If the function requires more than one parameter, the parameters are separated by commas as follows:

![syntax of a function with one parameter](images/00023.jpeg)

NOTE: It is common practice to define functions and variables in the `<head>` section of the HTML document so that they are out of the way.

### Calling A Function

After you have defined your function, you can call it. When you call your function, you are asking it to do its job which you have defined it to do. If your function does not take any parameters, you can call your function with an empty pair of parenthesis. The syntax for calling a function with no parameters is as follows:

![syntax for calling a function](images/00024.gif)

If your function needs parameters, you must include the parameters in your function call. This is called **passing parameters** to your function. The syntax for calling a function with parameters is as follows:

![syntax for calling a function with parameters](images/00025.jpeg)

NOTE: When passing parameters, the names of the parameters don't have to be the same, but the order of the parameters matters. So the value of the first parameter in the function call will be given to the first parameter in the function definition, and so on.

#### Now It's Your Turn To Practice:

Open your "`template.html`" file and add the following code between the `<script></script>` tags in the body section of your HTML document:

![code for practicing functions example](images/00026.jpeg)

Save the file as "`functions.html`" and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00027.jpeg)

### Functions Calling Functions

You can also call a function from inside another function. All you have to do is place the function call in the body of another function. Let's look at an example to make things more clear.

#### More Practice:

Open your "`template.html`" file and add the following code between the `<script></script>` tags in the head section of your HTML document:

![code for functions example](images/00028.jpeg)

Save the file as `"functions2.html"` and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00029.jpeg)

### Global Vs. Local Variables

A variable's **scope** is the context in which it is defined. The scope of a variable can be either global or local. A **global** variable is declared outside of a function and is available to all parts of your program. A **local** variable, on the other hand, is declared inside a function and is only available within that function. The parameters inside the parenthesis of a function declaration are local variables.

### The Return Statement

Sometimes, you may want a function to return a value back to where the function call was made. The `return` statement allows you to return a value from a function. Let's look at an example to make things more clear.

#### More Practice:

Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for simple return example](images/00030.jpeg)

NOTE: The function call is inside the `document.write();` statement on line 16.

Save the file as `"return.html"` and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00031.jpeg)

NOTE: The function `avgNumbers` returns the value <samp class="calibre11">6.6666666666667</samp> to the `document.write();` statement where the function was called.

## Lesson 6: Making Decisions And Conditional Statements

Many times, you will come across a situation in which you need one block of code to run if a certain condition is true, and another block of code to run if another condition is true. We can use **conditional statements** to perform different actions based on various conditions. There are four different kinds of conditional statements that we can choose from:

*   the `if` statement
*   the `if...else` statement
*   the `if...else if...else` statement
*   and the `switch` statement

Let's take a closer look at each type of conditional statement.

### The If Statement

A simple `if` statement tests for a certain condition. If the condition is true, the code inside the `if` statement runs. However, if the condition is false, the code inside the `if` statement is ignored and the computer skips to the next line of code outside the curly braces { }. You can use a simple `if` statement if you want a block of code to run only if the specified condition is true. The syntax of the `if` statement is as follows:

![syntax for if statement](images/00032.jpeg)

### The If...Else Statement

If you want to execute a block of code if a certain condition is true, and another block of code if the condition is false, you can use an `if...else` statement. If the condition is true, the first block of code will run. However, if the conditions is false, the second block of code will run. The syntax of the `if...else` statement is as follows:

![syntax for if else statement](images/00033.jpeg)

### The Else-If Statement

Sometimes, it may be necessary to test for more than one condition. In such a case, you must use the `if...else if...else` statement. This type of conditional statement allows you to test for more than one condition. The first condition is always specified with the `if` statement. Any additional conditions are specified using `else...if` statements. Each `else if` statement allows you to specify another condition. You can specify as many conditions as you like, so you can have as many `else if` statements as you want. If none of the specified conditions are true, the block of code inside the `else` statement will run. The syntax for the `if...else if...else` statement is as follows:

![syntax for else if statement](images/00034.jpeg)

### Conditions And Comparison Operators

Comparison operators are used to compare two operands, and they are commonly used in conditional statements. Some commonly used comparison operators are listed below:

![some comparison operators](images/00035.jpeg)

A Boolean value of either `true` or `false` is returned after the two operands are compared. For example, the expression `5 == 5` will return a value of `true`, while the expression `5 != 5` will return a value of `false`.

The equal operator (==) will check if two operands are equal, however, the operands can be of different data types and still be equal. For example, the expression `5=="5"` will return a value of `true`, because the JavaScript interpreter will try to convert a string value to a number. However, if the string can not be converted to a number, the value of `false` is returned. So, the expression `5 == "five"` will return a value of `false` because the interpreter can not convert the string `"five"` to a number.

The strictly equal operator (===) is slightly different from the equal operator. It checks if two operands have the same value and are of the same data type. For example, the expression `5==="5"` will return a value of `false`, because one operand is of the number type, while the other is of the string type.

### Complex Conditions And Logical Operators

Sometimes you will want to test for more than one condition. In that case, you can create complex conditions consisting of 2 or more conditions using logical operators. There are three logical operators in JavaScript, and they are listed below:

![symbols for logical operators](images/00036.jpeg)

The AND operator (&&) returns a Boolean value of `true` only when all the operands have a value of `true`. The OR operator ( || ) returns a value of `true` when at least one of the operands has a value of `true`, otherwise it returns `false`. The NOT operator ( ! ) returns a value of `false` when the operand has a value of `true`, and it returns a value of `true` when the value of the operand is `false`. This information is summarized in the table below:

![summary of logical operators](images/00037.jpeg)

Let's look at some examples of how to create complex conditions using the logical operators. The expression `(5 < 30) && (6 == 8)`, will return a value of `false` because one of the operands has a value of `false`. However, the expression `(5 < 30) || (6 == 8)` will return `true` because one of the operands is `true`. And finally, the expression `!(6 == 8)` will return a value of `true` because the value of the operand is `false`.

#### Now It's Your Turn To Practice:

Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<body>` section of your HTML document:

![code for complex condition example](images/00038.jpeg)

Save the file as "`age.html`" and launch it in Chrome or the browser of your choice. Your browser window should display the message <samp class="calibre11">You are an adult who is not retired!</samp> Now, experiment by changing the value of the `age` variable to `2` and then to `70`. Your browser should display the message <samp class="calibre11">You are still a child!</samp> when the age is 2 and <samp class="calibre11">You are retired!</samp> when the age is 70.

### The Switch Statement

Finally, let's look at the last type of conditional statement, the `switch` statement. The `switch` statement can be very useful when you have one expression that needs to be evaluated, but many conditions and blocks of code that depend on the value of that expression. The `switch` statement works as follows:

1.  The expression, which is most often a variable, is evaluated once.
2.  Then the value of the expression is compared to a list of case values.
3.  If a match is found, the block of code associated with that case is executed.
4.  The `break;` statement allows you to exit the `switch` statement.
5.  If no match is found, the `default` block of code runs.

The following keywords are used in the `switch` statement: `switch, case, break`, and `default`. The syntax for the `switch` statement is as follows:

![syntax for switch statement](images/00039.jpeg)

NOTE: The blocks of code inside each case do not need to be enclosed in curly braces { }, so there should only be one pair of curly braces in the entire `switch` statement.

#### More Practice:

Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for switch example](images/00040.jpeg)

Save the file as "`grades.html`" and launch it in Chrome or the browser of your choice. Your browser window should display the message <samp class="calibre11">Congratulations! You got an A!</samp> Now, experiment by changing the value of the `grade` variable to `"B"` on line 9\. Save your document and launch it in your browser again. This time, you should see the message <samp class="calibre11">Great job! You worked hard!</samp> Continue testing all of the possible values for the `grade` variable and check that the correct block of code associated with each value of the `grade` variable runs.

## Lesson 7: Loops

### What Is A Loop?

A **loop** is a block of code that is executed repeatedly until a certain condition is met. There are two main types of loops: the `for` loop, and the `while` loop. Let's take a closer look at each one.

### The For Loop

The `for` loop is used to execute a block of code a number of times. A `for` loop begins with the `for` keyword followed by three statements that are enclosed in a pair of parenthesis ( ). The first statement is used to initialize the value of the counter variable and is executed before the loop begins. The second statement provides the condition for running the loop. The third statement is executed at the end of each loop and is used to update the value of the counter variable. The block of code that you want to repeat is enclosed inside curly braces { }. The syntax of the `for` loop is as follows:

![syntax for for loop](images/00041.jpeg)

Let's look at an example of a `for` loop to make things more clear. Statement 1 in the `for` loop below assigns the value of zero to the counter variable `x`. Statement 2 specifies the condition that as long as the counter variable `x` is less than 3, the `for` loop should run. Statement 3 runs after each run of the loop and increments the value of the counter variable `x` by 1\. So the end result of the `for` loop below is that the numbers 0, 1, and 2 are printed on separate lines to your browser window.

![example of for loop](images/00042.jpeg)

NOTE: You can also use the decrement operator ( -- ) in a `for` loop to count backwards. In such case, you should initialize your counter variable to a number other than zero if you want to deal with positive numbers.

The following table shows the values for the variable `x` in each run of the `for` loop and explains how each of the three statements helps in the decision making process of executing the `for` loop.

![the for loop in action](images/00043.jpeg)

After the `for` loop has run, your browser window should appear as follows:

![for loop screenshot](images/00044.jpeg)

### The While Loop

A `while` loop is another method you can use to repeatedly execute a block of code. The `while` loop begins with the `while` keyword followed by a condition enclosed within a pair of parenthesis ( ). A `while` loop continues running as long as the specified condition is true. The block of code to be repeated is enclosed within a pair of curly braces { }. The syntax for the while loop is shown below:

![syntax for while loop](images/00045.jpeg)

Now let's see the while loop in action. The while loop below will execute as long as the value of the variable `x` is less than or equal to 4\. It is very important that you put a statement inside the loop that will stop the while loop from executing, otherwise you will have an **infinite loop**. An infinite loop is a loop that never stops running, and it will cause your browser to crash. In this example, the statement `x++;` is very important because it provides a means for the loop to finish executing. Without this statement, you will have an infinite loop because the variable `x` will always have the value of 1, and 1 is always less than 4.

![example of while loop](images/00046.jpeg)

The table below shows the values of the variable `x` in each run of the `while` loop and explains the decision making process for executing the `while` loop.

![the while loop in action](images/00047.jpeg)

After the `while` loop runs, your browser window should look as follows:

![while loop screenshot](images/00048.jpeg)

### The Continue Statement

The `continue;` statement allows you to skip over one iteration of a loop. When the `continue;` statement is placed in a block of code, it tells the interpreter to skip the remaining block of code and immediately start the next iteration of the loop.

#### Now It's Your Turn To Practice:

Let's practice using the `continue;` statement. Suppose you want to print all the numbers from 1 and 10 except the numbers 7 and 9\. We will use the `continue;` statement to skip over the numbers 7 and 9\. Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<body>` section of your HTML document:

![example of continue statement](images/00049.jpeg)

Save the file as "`continue.html`" and launch it in Chrome or the browser of your choice. Your browser window should look as follows:

![screenshot of continue example](images/00050.jpeg)

NOTE: The numbers 7 and 9 are not printed to the screen.

### The Break Statement

Sometimes, you don't want to skip over one iteration of a loop, you just want to exit the loop entirely. The `break;` statement enables you to exit a loop early, breaking out of the enclosing curly braces { }.

#### More Practice:

Now, let's practice using the `break;` statement. Open your "`continue.html`" file and change the `continue;` statement to a `break;` statement as follows:

![example of break statement](images/00051.jpeg)

Save the file as "`break.html`" and launch it in Chrome or the browser of your choice. Your browser window should look as follows:

![screenshot](images/00052.jpeg)

NOTE: The numbers 1 through 6 are printed to the screen and then the loop is exited.

## Lesson 8: Arrays

### What Is An Array?

An array is used to store multiple values using a single variable name. For example, suppose you have a list of customer names. You could create a new variable for each customer as follows: `customer1 = "John Doe"; customer2 = "Mary Contrary"; customer3 = "Tom Tiger";`. However, if you wanted to loop through them to find a specific customer name, what would you do? The solution is to create a special data type that can store multiple values under a single name and enable you to access the values by referencing an index number. This special new data type is called an array. Referring back to our customer names example, you could create a `customer` array that has a list of names in it. You can access the names by using an index number as follows: `customer[0] = "John Doe"; customer[1] = "Mary Contrary"; customer[2] = "Tom Tiger";` .

### Creating And Populating An Array

Now that we have a general idea of what an array is, let's see how to create and populate an array. The syntax for creating an array in JavaScript is as follows:

![syntax for creating an array](images/00053.jpeg)

Once you have created an array, you will need to store values in it. This is called **populating the array**. To populate an array with values, you will need the name of the array, the index where you want to store a value, and the value that you want to store in the array. The syntax for populating an array is as follows:

![syntax for populating an array](images/00054.jpeg)

Now, let's look at some example code. The following code demonstrates how to create and populate the array from the previous discussion:

![example for creating an array](images/00055.jpeg)

### The Length Property Of An Array

The `length` property of an array is used to find out how many values are stored in an array. The syntax for using this property with an array is as follows:

![syntax for length property](images/00056.gif)

So, in our previous example, if we wanted to find the number of values stored in the `customer` array, we would use the code `customer.length`, which should return the number 3, since we have 3 values stored in our `customer` array.

#### Now It's Your Turn To Practice:

Now, let's practice looping through an array. Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for array example](images/00057.jpeg)

Save the file as "`arrays.html`" and launch it in Chrome or the browser of your choice. Your browser window should look as follows:

![screen shot](images/00058.jpeg)

### Methods Of Arrays

Methods are actions that can be performed on an array. There are many methods for arrays, but we will look at only a few of them so you can understand how to use them.

The `reverse()` method does not take any parameters and reverses the order of the array.

The `push()` method adds elements on to the end of the array. The parameters of this method are the items that you want to add to the array. Each item is separated with a comma. If the item that you want to add to the array is a string, it should also be enclosed in quotation marks.

The `sort()` method sorts the elements of your array in alphabetical order.

The `join()` method joins the elements of your array into a string object. If you use this method without any arguments, it will join the items in the list with a comma in between them but no space. If you want to separate the items in the array in a different way, you can use a parameter with the `join()` method. The value of the parameter will be the characters that you want to use to separate the items in the array. So, for example, `people.join(" ");` will separate the items in the list with a space instead of a comma, and `people.join(", ");` will separate the items with both a comma and a space.

#### More Practice:

Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for practicing array methods](images/00059.jpeg)

Save the file as "`methods.html`" and launch it in Chrome or the browser of your choice. Your browser window should look like this:

![screen shot](images/00060.jpeg)

## Lesson 9: JavaScript Pop Up Dialog Boxes

Pop up dialog boxes are used to communicate with and get information from the user. There are three kinds of pop up boxes in JavaScript: the alert box, the confirm box, and the prompt box. Let's take a look at how to use them.

### The Alert Box

The alert pop up box is used to display information to the user, and it is often used to display error messages. For example, if a user forgets to fill out a required field on a form, you could alert the user to fill out the required field. You can also use the alert dialog box to test your JavaScript code by using it to display the value of a variable at a certain stage of processing. The alert dialog box contains an `OK` button that when pressed confirms that the message has been seen by the user.

![pop up alert box](images/00061.jpeg)

The syntax for creating an alert dialog box is as follows:

![syntax for alert](images/00062.jpeg)

Or, you can use the following shorthand code:

![syntax for alert function](images/00063.jpeg)

We will practice using the alert pop up box in Lesson 10.

### The Confirm Box

The confirm pop up box is a little more complex than the alert pop up box. Instead of simply displaying a message, the confirm dialog box allows you to ask the user a question. The confirm pop up box displays two buttons at the bottom of the dialog box, `OK` and `Cancel`. When the user chooses the `OK` button, a value of true is returned, but when the user chooses the `Cancel` button, a value of false is returned. The confirm dialog box allows you to ask the user a yes or no question and continue processing based on the user's answer.

![pop up confirm box](images/00064.jpeg)

The syntax for creating a confirm dialog box is as follows:

![syntax for confirm function](images/00065.jpeg)

Or, you can use the following shorthand code:

![syntax for confirm function](images/00066.jpeg)

We will practice using the confirm pop up box in Lesson 12.

### The Prompt Box

The prompt pop up box enables you to ask your user a question and get information from your user in the form of a text string. The prompt dialog box returns the text string entered by the user when the `OK` button is selected, and it returns null when the `Cancel` button is selected.

![pop up prompt box](images/00067.jpeg)

The syntax for creating a prompt pop up box is as follows:

![syntax for prompt function](images/00068.jpeg)

Or, you can use the following shorthand code:

![syntax for prompt function](images/00069.jpeg)

#### Now It's Your Turn To Practice:

Let's practice using the `prompt` pop up dialog box to interact with the user. Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for practicing prompt method](images/00070.jpeg)

NOTE: In the code above, we use the variable `name` to store the value that the user types into the prompt dialog box.

Save the file as "`greetings.html`" and launch it in Chrome or the browser of your choice. Your browser window should display a prompt dialog box upon loading. Type your name in the field of the prompt dialog box and click on the <samp class="calibre11">OK</samp> button. Your browser window should appear as follows, but with the name that you entered:

![screen shot](images/00071.jpeg)

## Lesson 10: Events And Event Handlers

### What Is An Event?

The primary way that JavaScript code is used is to respond to events on a web page. An **event** is something that happens on a web page that can be detected by JavaScript, and that your code can respond to in some way. An event can be an action performed by a user, such as the user clicking his mouse on an HTML element. This is called the **click** event. An event can also be an action performed by the browser, such as the **load** event, which occurs when a web browser finishes loading a web page. Some of the more common events and their triggers are listed below:

![list of events](images/00072.jpeg)

### What Are Event Handlers?

JavaScript code that responds to a specific event is called an **event handler**. Event handlers are keywords that are responsible for executing JavaScript code when an event happens, such as when the user clicks on a button, moves his mouse over an HTML element, or submits a form, etc. If you add the prefix "on" to the event name, you get the name of the event handler. So, "`onclick`" is the event handler for the "click" event. Event handler names must be written in all lower case letters.

Event handlers are used as attributes inside the HTML element that initiates the event. The value of the event handler attribute is the JavaScript code that you want to run in response to the event. For example, suppose you want to create a really cool effect when a user moves his mouse over an image on your web page. You could use the code `<img onmouseover="JavaScript code" >` to add a mouseover event to the image element. The basic syntax of an event handler is:

![syntax for event handler](images/00073.jpeg)

You can add more than one JavaScript statement in an event handler. Just remember to enclose all of the statements within the quotation marks (" ") and end each statement with a semicolon (;) as follows:

![syntax ](images/00074.jpeg)

#### Now It's Your Turn To Practice:

Now let's practice using an event handler to respond to events on a webpage. We will use the `onclick` event handler to interact with the user. Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<body>` section of your HTML document:

![code for event handlers example](images/00075.jpeg)

NOTE: The message inside the alert function is enclosed in single quotes to differentiate it from the entire set of JavaScript code which is enclosed between double quotes.

Save the file as "`onclick.html`" and launch it in Chrome or the browser of your choice. When you click on the <samp class="calibre11">Touch Me!!</samp> button, your browser window should appear as follows:

![screen shot](images/00076.jpeg)

### Event Handlers And Functions

Now imagine if you wanted to add more than three statements inside an event handler attribute. Your code could get quite messy and hard to read. Therefore, if the JavaScript code that you have written to respond to an event is more than three statements, it may be easier to write a function and then simply call the function in the event handler attribute.

#### More Practice:

Let's practice using functions with event handlers. Open your "`onclick.html`" file and add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for functions example](images/00077.jpeg)

Next, use the `onclick` event handler to call your new function by using the following bit of code: `onclick="touchButton()"`. Your HTML document should appear as follows:

![code](images/00078.jpeg)

Save the file as "`onclick2.html`" and launch it in Chrome or the browser of your choice. Your browser window should appear as follows:

![screen shot](images/00079.jpeg)

### Choosing An Event Handler

Each HTML element has a specific set of event handlers that it can use. The table below summarizes which event handlers can be used with some commonly used HTML elements:

![list of event handlers](images/00080.jpeg)

#### More Practice:

Now let's practice using an event handler with a different HTML element. The `onload` event handler executes JavaScript code when your webpage is finished loading, and it is added to the opening `<body>` tag. Open your "`template.html`" file and add the following code between the `<script></script>` tags in the `<body>` section of your HTML document:

![onload example code](images/00081.jpeg)

NOTE: Once again, notice that the message inside the alert function is enclosed in single quotes to differentiate it from the entire set of JavaScript code which is enclosed between double quotes.

Save the file as "`onload.html`" and launch it in Chrome or the browser of your choice. Your browser window should appear as follows after loading:

![screen shot](images/00082.jpeg)

## Lesson 11: An Introduction To Object Oriented Programming In JavaScript

### What Is An Object?

Everything is an object in JavaScript. Strings, numbers, functions, arrays, booleans, forms, any HTML element on your webpage, the webpage itself, the browser window, etc, are all objects. An **object** is a special kind of data that has properties and methods.

### What Is A Property?

**Properties** are the values that are associated with an object. For example, suppose you have a variable called `myName` whose value is the string "Dr. Code". Then, the variable `myName` is an **instance of** the string object. All string objects have a `length` property that returns the number of characters in the string. Therefore, you can use the `length` property to find the number of characters in the variable `myName` using the following bit of code:

![example](images/00083.jpeg)

NOTE: The code `myName.length` will return the number `8` since the string "Dr. Code" has 8 characters, including the period and the space.

The syntax for accessing a property of an object is as follows:

![syntax](images/00084.jpeg)

### What Is A Method?

A **method** is an action that can be performed on an object. For example, all string objects have a `toUpperCase()` method that converts all the letters in a string to upper case letters. So, we can change all the letters in the variable `myName` to upper case letters by using the following bit of code:

![example](images/00085.jpeg)

NOTE: The code `myName.toUpperCase()` will return the string "DR. CODE".

The syntax for calling a method is as follows:

![syntax](images/00086.jpeg)

Now, let's look at some examples of objects that we have already used: the array object, the window object, and the document object.

### The Array Object

In Lesson 8, you were introduced to the array object. You learned how to use the `length` property to find out how many items were stored in an array. You also practiced using several methods of the array object: the `reverse()` method, the `push()` method, the `sort()` method, and the `join()` method.

### The Window Object

The **window object** is your browser window. It looks like this:

![window object](images/00087.jpeg)

In Lesson 9, you learned how to use three methods of the `window` object to create a dialog with your user: the `alert()` method, the `confirm()` method, and the `prompt()` method.

### The Document Object

The **document object** is the white space in your browser window that displays the actual web page. It looks like this:

![document object](images/00088.jpeg)

The `write()` method is used to write text on the `document` object. In Lesson 2, you learned how to use the `document.write()` method to write text on your web page.

### The getElementById Method

The document object has another very useful method, called the `getElementById()` method. The `getElementById()` method allows you to manipulate HTML elements on your webpage. This method not only enables you to change the content of an element based on user interaction, but it also allows you to change the CSS style rules associated with an element.

However, before you can manipulate an HTML element, you must use the `id` attribute to specify which element you want to manipulate. You can specify a unique name for an element as follows:

![syntax for adding id attribute](images/00089.jpeg)

Now that we have marked the HTML element that we want to manipulate with the `id` attribute, we can use the id name with the `getElementById()` method to access that particular HTML element as follows:

![syntax for getElementById](images/00090.jpeg)

There are several things that we can do to manipulate an HTML element. We can change the content of an element, we can change the attribute of an element, and we can change the style of an element.

### Changing The Content Of An HTML Element On The Fly

One thing we can do is set or change the content of the HTML element by using the `innerHTML` property as follows:

![syntax for using innerHTML property](images/00091.jpeg)

### Changing The Attribute Of An HTML Element On The Fly

You can also change the value of any attribute of the specified element using the following syntax:

![image element marked with id attribute](images/00092.jpeg)

### Changing The Style Of An HTML Element On The Fly

Finally, you can change the CSS style of an HTML element on the fly using the `getElementById()` method together with the `style` property. The syntax for changing a CSS style rule is as follows:

![syntax for changing CSS of an element](images/00093.jpeg)

NOTE: You can use this to change any CSS style rule.

#### Now It's Your Turn To Practice:

Let's practice changing the content and style of an HTML element on the fly. Open your `"template.html` file and add the following code between the `<body></body>` tags:

![HTML code for changing style](images/00094.jpeg)

Save this file as "`changeStyle.html`". Next, open your "`myscript.js`" file, and add the function `changeStyle()` as follows:

![javascript changeStyle function code](images/00095.jpeg)

Save both files and then launch the file "`changeStyle.html`" in Chrome or the browser of your choice. Your browser window should display the following:

![first screenshot](images/00096.jpeg)

Now click on the paragraph. Your browser window should appear as follows:

![second screenshot](images/00097.jpeg)

#### More Practice:

Now, let's practice changing an attribute of an HTML element on the fly. First, find two images and save the first image as "`image1.jpg`" and the second image as "`image2.jpg`". Make sure to save both images in the same folder as your "`template.html`" file. Next, open your "`template.html`" file and add the following `<img>` tag in the `<body>` section of your HTML document:

![code for changing attribute](images/00098.jpeg)

Next, we need to create the functions `changePic()` that will be called when the user mouses over the image, and the function `originalPic()` that will be called when the user moves his mouse away from the image. Add the following code between the `<script></script>` tags in the `<head>` section of your HTML document:

![code for changing attribute](images/00099.jpeg)

Save this file as "`changeImage.html`" and launch it in Chrome or the browser of your choice. Your browser window should display the picture that you saved as "`image1.jpg`". Try moving your mouse over the picture. The image should change to the picture that you saved as "`image2.jpg`". Now, move your mouse away from the image. The picture that you saved as "`image1.jpg`" should reappear.

### Creating Your Own Objects

The previous discussion was a sampling of some of the pre-defined objects available to you in JavaScript. In addition, however, JavaScript allows you to define and create your own objects. There are two ways that you can create your own objects in JavaScript:

1.  You can use a function to define an object and then create new instances of the object (Constructor Functions)
2.  You can define and create a direct instance of an object (Object Initializers)

### Creating Your Own Objects With Constructor Functions

You can use a **constructor function** to define your own objects in JavaScript. For example, suppose you wanted to create a person object with two properties, name and age. You could do this by creating a constructor function as follows:

![constructor function code](images/00100.jpeg)

NOTE: The keyword `"this"` is used as shorthand for referring to the current object.

Now that you have created a new `person` data type, you can create an instance of the `person` object as follows:

![code for creating an instance](images/00101.jpeg)

NOTE: The variables `Tim` and `Mary` are instances of the `person` object.

Now that you have created instances of your objects, you can use them as follows:

![using your objects](images/00102.jpeg)

The code above will result in the following text being written to your webpage:

![object screenshot](images/00103.jpeg)

NOTE: Use constructor functions when you have to make a bunch of variables.

### Creating Your Own Objects With Object Initializers

You can also use **object initializers** to define and create a direct instance of an object in one statement. Object initializers are often used when you have to make only one or two variables of the data type. If you have to make more variables, you should use the constructor function. The following is an example of how to create direct instances of an object with object initializers:

![object initializers](images/00104.jpeg)

Now we can use the variable names and the properties associated with them as follows:

![using your objects](images/00102.jpeg)

The code above will result in the following text being written to your webpage:

![object screenshot](images/00103.jpeg)

## Lesson 12: An Introduction To Form Validation

Now, let's put everything that we learned so far together and do some form validation. **Form validation** means making sure that the user fills in an online form correctly. The best way to learn is by doing, so let's get started and I'll explain on the way!

#### Now It's Your Turn To Practice:

First, we need a form. Open your `"template.html"` file and add the following `<form>` element between the `<body></body>` tags:

![HTML code for form](images/00105.jpeg)

Save the file as `"myform.html"` and launch it in Chrome or the browser of your choice. Your browser window should display the following:

![screenshot of form](images/00106.jpeg)

Now, let's use some JavaScript to make sure the user fills out the form correctly. First, add the following code to your opening `<form>` tag:

![form tag code](images/00107.jpeg)

Now, let's look at what we just added piece by piece.

### The Action Attribute

The `action` attribute of the `form` tag tells your browser where to send the form data when the user clicks on the <samp class="calibre11">Submit</samp> button. For simplicity and learning purposes, our form validation code will be located in the `<head>` section of our "`myform.html`" document, so we will send the data to the file `"myform.html"` for processing. However, when you have more complicated forms, you may want to send your form data to an external JavaScript source file for validation.

### The Method Attribute

The `method` attribute tells the browser how to send the form data. The two most commonly used methods are the `get` method and the `post` method. The `get` method attaches form data to the URL in name / value pairs. The `get` method should never be used when dealing with sensitive data because the data will be visible in the URL. Furthermore, if you have lengthy data to send, you should not use the `get` method because the length of the URL is limited to about 3000 characters. In instances when you have sensitive or lengthy data, you should use the `post` method, which has no restrictions on the length of the data, and is a more secure method since the data is not shown in the URL. However, for learning purposes, the `get` method is ideal since we will be able to see our submitted form data in the URL.

### The Onsubmit And Onreset Event Handlers

In our example, the `onsubmit` event handler calls the `confirmSubmit()` function when the user clicks on the <samp class="calibre11">Submit</samp> button of our form.

When the user clicks on the <samp class="calibre11">Reset</samp> button, all of the values that the user has entered in the form will be erased. In addition, you can use the `onreset` event handler to give the browser extra instructions on what to do when the <samp class="calibre11">Reset</samp> button is clicked. In our example, the `onreset` event handler calls the function `confirmReset()`.

### Accessing Form Data

Before we can check if the user filled out our form correctly, we must know how to access the data that was entered into the form by the user. The `document` object has a `forms[]` array that contains all the forms on a web page. Each form is contained within a pair of `<form></form>` tags, and you can have multiple forms on a web page. The forms are referenced according to their position on the web page. So the first `<form>` element on the web page is referred to as `forms[0]`, the second form element is `forms[1]`, and the third form element is `forms[2]`, and so on. However, most web pages do not contain more than one `<form>` element. If there are no forms on the web page, the `forms[]` array is empty. So, in our example, the code `document.forms[0]` will give us access to the form we created in the beginning of this lesson.

The `forms[]` array contains elements within the form, such as the `<input>` element, the `<select>` element, etc. that can be accessed. We can access the elements in a form by using the value of the `name` attribute of the element. For example, in the form that we created in the beginning of this lesson, we named the first `<input>` element "`myemail`" using the `name` attribute. We named the `<select>` element "`size`", and we named the set of radio buttons "`payment`". So, if we wanted to refer to the first `<input>` element that we created in our form, we would use the code `document.forms[0].myemail`.

Each element in a form is an object with properties and methods. One very useful property is the `value` property. The `value` property stores the data that the user enters into a `<form>` element. In the case of the email input field, the `value` property stores a string whose value is the text that the user enters into the email input field. So, if we want to access the email address that the user typed into the email address input field, we would use the code `document.forms[0].myemail.value`.

The `<select>` element is a little different from the email `<input>` element. The values of the `<select>` element are pre-defined. Recall the `<select>` element in our form at the beginning of this lesson:

![select element](images/00108.jpeg)

Notice that there is a `value` attribute inside each of the `<option>` tags. The `value` attribute equals the empty string (`""`) when the first `<option>` tag is selected. This means the user did not select any option from the drop down list. The text for the first option is usually reserved for writing instructions for the user, such as <samp class="calibre11">Select An Option</samp>. The `value` attribute equals "`small`" when the user selects the second option, it equals "`med`" when the user selects the third option, and so on. So, if we wanted to find out which option the user selected from the drop down list, we would use the code `document.forms[0].size.value`.

Recall that our form included a radio button element that let the user choose his method of payment, and that we named this set of radio buttons `payment` using the `name` attribute. Radio buttons and checkboxes are different from other `<input>` elements because the same name applies to a set of buttons. In order to distinguish between the buttons, we need to store the values of each button in an array called `payment[]`, where the first button's value is stored in `payment[0]`, the second button's value is stored in `payment[1]`, and the third button's value is stored in `payment[2]`. The value of each button is either `true` or `false`. It is `true` if the user selects the button, and `false` if the user does not select the button.

![radio buttons](images/00109.jpeg)

The `checked` property is only available to check boxes and radio buttons, and it returns the boolean value that tells whether a radio button or check box has been selected by the user. So, if we wanted to check if the user selected the <samp class="calibre11">Debit Card</samp> radio button in the <samp class="calibre11">Method Of Payment</samp> section of our form, we could use the following code: `document.forms[0].payment[1].checked`. If this bit of code returns a value of `true`, then the user has checked the <samp class="calibre11">Debit Card</samp> radio button.

### The confirmSubmit Function

The purpose of the `confirmSubmit()` function will be to validate our form data. You can name your function anything you like, but in our example, we named our function `confirmSubmit()`. Now that we've named our function, let's start building it!

### Checking If A Radio Button Has Been Selected

Now, let's start creating our `confirmSubmit()` function. Open your "`myform.html`" file and add the following code between the `<script></script>` tags in the `<head>` section:

![code for confirmSubmit function](images/00110.jpeg)

The purpose of the code above is to check if the user has selected a radio button in our form.

First, we assume that the user has not selected a radio button, so we set the value of a boolean variable called `paymentSelected` to `false`.

Next, we will check to see if any of the radio buttons have been selected using a `for` loop. Since there are 3 radio buttons on our form, we will set our counter variable to go through the loop 3 times. Each run of the loop checks for a value of `true`. If a value of `true` is found, that means the user checked a radio button, and we can change the value of our boolean variable `paymentSelected` to `true`, and break out of the loop. On the other hand, if none of the checked values has the value of `true` after the `for` loop has run, then the boolean variable `paymentSelected` will remain `false`, which means the user did not select a radio button.

The `if` statement after the `for` loop checks the value of the `paymentSelected` variable. If it's value is `false`, it sends an alert message to the user reminding him to select a radio button. Additionally, it sends back a return value of `false`, which tells the browser "Don't send the form data to the server".

The `else` statement is executed if the value of the `paymentSelected` variable is `true`. If the `paymentSelected` variable has a value of `true`, the function returns a value of `true`, which tells the browser "O.K. you can send the form data to the server".

### Checking If An Input Text Box Is Empty

Next, let's check if the user has filled in the email address section of our form. Add the following JavaScript code inside the `confirmSubmit()` function, after the `if` statement and before the `else` statement.

![code for checking email](images/00111.jpeg)

The purpose of this block of code is to check if the value of the email input text box is empty. A value of `""`, called the empty string, means that the user has not entered any text into the input text box. If the value of the input text box is the empty string, we will alert the user to enter a valid email address. In addition, we will send back a return value of `false`, which means the form data will not be submitted to the server. If the value of the input text box is not empty, the `else` statement will run, sending back a return value of `true`, thus enabling the form data to be submitted to the server.

### Checking If An Item In A Drop Down List Has Been Selected

Finally, we will check if the user has selected an item from the drop down list. Add the following code inside the `confirmSubmit()` function, after the `else if` statement and before the `else` statement.

![code for checking drop down list](images/00112.jpeg)

This block of code will check if the user has selected an item from the drop down list. The `else if` statement checks the value selected by the user in the drop down list. If the value is the empty string, that means the user did not select a size from the drop down list. In that case, the user is alerted to select a size and the function sends a return value of `false`, which means the form data will not be submitted to the server. If a value other than the empty string is detected by the `else if` statement, the `else` statement runs and the function sends a return value of `true`, enabling the form data to be sent to the server.

### The confirmReset Function

In our example, when the user clicks the <samp class="calibre11">Reset Form</samp> button, the function `confirmReset()` is called. So, let's create our `confirmReset()` function. Open your `"myform.html"` file again and add the `confirmReset()` function between the `<script></script>` tags in the `<head>` section, right after the `confirmSubmit()` function.

![code for confirmReset function](images/00113.jpeg)

The purpose of the code above is to send a pop up confirmation dialog box to ask the user if he is sure that he wants to reset the form before the form is reset. We create a boolean variable named `resetForm` to hold the response of the user. If the user presses the <samp class="calibre11">OK</samp> button, the value of `true` is stored in the variable `resetForm`, whereas if the user presses the <samp class="calibre11">Cancel</samp> button, a value of `false` is stored in the `resetForm` variable. The value of the `resetForm` variable is then returned by the function. When the value of `true` is returned, the form is reset, but when the value of `false` is returned, the form is not reset.

### Testing Our Form

Save your "`myform.html`" file and launch it in Chrome or the browser of you choice. Now, let's test out our form. First, fill out all of the fields on your form and click the <samp class="calibre11">Submit</samp> button. Your browser should display all the information you entered in name / value pairs in the URL box at the top of your browser window. The name portion of the name / value pair is the name that you gave to the form element using the `name` attribute when you created your form in HTML. The value portion is the information that the user entered in the form.

![screenshoot url after submitting form](images/00114.jpeg)

NOTE: The name / value pairs are separated from the URL by a "?" symbol, and each name / value pair is separated from each other by an "&" symbol.

Next, let's test our form by filling out every field except the email address field, and then clicking on the <samp class="calibre11">Submit</samp> button. Your browser window should display an alert box as follows:

![screenshoot of error submit form](images/00115.jpeg)

Fill out the form again, this time leaving out the <samp class="calibre11">Method Of Payment</samp> field. Click on the <samp class="calibre11">Submit</samp> button. You should get an error message that alerts you to select a method of payment.

Now, fill out the form again, but don't choose a size from the drop down list. Click on the <samp class="calibre11">Submit</samp> button. You should get an alert message telling you to choose a size.

Finally, fill out the form again, but this time click on the <samp class="calibre11">Reset Form</samp> button. A pop up confirmation box should appear asking you if you are sure that you want to reset the form.

* * *

## Congratulations!!!

You made it through your first 12 lessons in JavaScript. Now that you have the hang of things, you can make your website interactive and dynamic! You can definitely use all the skills you learned here along with your imagination to create something wonderful to share with the world. So what are you waiting for? Get started!!

## Thank You

Thank you for purchasing "JavaScript Crash Course". I hope this book helped you to learn JavaScript quickly and easily. As an independent author, I don't have a marketing department to provide exposure for my books. Therefore, if you found "JavaScript Crash Course" to be helpful to you, please spread the word by telling a few friends about this book or writing an Amazon review [http://www.drcode.com/jscrashcourse](http://www.amazon.com/dp/B00EVI5L92) .

**Thank You Again and Happy Coding,
Dr. Code**

**P.S.** Please help me to make my books better. If you notice any mistakes in my books, or if you have a suggestion to make my books better, please email me at drcode14@gmail.com.