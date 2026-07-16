![](Image00032.jpg)

LEARN JAVASCRIPT AND REACTJS BASICS:

FOR BEGINNERS

FAST AND EASY WAY TO LEARN CODING BASICS

JP TAM

[Javascript Tutorial](#text00003.html__Toc77969454)

[Javascript Example](#text00004.html__Toc77969455)

[Javascript comment](#text00005.html__Toc77969456)

[Javascript Variable](#text00006.html__Toc77969457)

[Javascript Data Types](#text00007.html__Toc77969458)

[Javascript Operators](#text00008.html__Toc77969459)

[Logical Operators](#text00008.html__Toc77969460)

[Javascript If Else](#text00009.html__Toc77969461)

[Javascript Switch Statement](#text00010.html__Toc77969462)

[Javascript loop](#text00011.html__Toc77969463)

[do while loop](#text00011.html__Toc77969464)

[JavaScript Function](#text00012.html__Toc77969465)

[Function with arguments](#text00012.html__Toc77969466)

[Javascript Object](#text00013.html__Toc77969467)

[Javascript array](#text00014.html__Toc77969468)

[ReactJS Introduction](#text00016.html__Toc77969469)

[React Environment Setup Step by Step](#text00017.html__Toc77969470)

[React JSX](#text00018.html__Toc77969471)

[React Components](#text00019.html__Toc77969472)

[Pros and Cons of ReactJS](#text00020.html__Toc77969473)

[Features of ReactJS](#text00021.html__Toc77969474)

[Comparison between React and Vue](#text00022.html__Toc77969475)

[ReactJS vs AngularJS](#text00023.html__Toc77969476)

[React Native vs ReactJS](#text00024.html__Toc77969477)

[React State](#text00025.html__Toc77969478)

[React Props](#text00026.html__Toc77969479)

[React Props Validation](#text00027.html__Toc77969480)

[React Component API](#text00028.html__Toc77969481)

[React Component Life-Cycle](#text00029.html__Toc77969482)

[React Constructors](#text00030.html__Toc77969483)

LEARN JAVASCRIPT BASICS:

FOR BEGINNERS

FAST AND EASY WAY TO LEARN CODING BASICS

JP TAM

Javascript Tutorial

This JavaScript lesson makes it simple for both beginners and experts to learn JavaScript.

What is JavaScript and how does it work?

JavaScript is a dynamic programming language for computers. It is a lightweight and cross-platform object-based scripting language.

With the aid of JavaScript, we can make our website more vibrant and engaging.

Brendan Eich, a Netscape employee, designed it in 1995.

It's a programming language that's used to make interactive websites. It's most commonly used for::

• Validation on the client's end.

• Its drop-down menus are dynamic.

• It shows the current date and time.

• Before transferring data to a server, validate user input in an HTML form.

• Create forms that respond to user input without requiring a connection to a server.

• Install new windows or frames and close them.

• Using popup windows and dialog boxes to display information.

(for example, an alert dialog box, a confirm dialog box, or a prompt dialog box)

• Create client-side programs that are small but complete.

• Clocks and other timepieces

• Game and app development for mobile devices.

Features of Javascript

• JavaScript is a scripting language that is based on objects.

• The language is case sensitive.

• It's light in weight.

• In JavaScript, every statement must be followed by a semicolon (;).

Advantages of Javascript

• JavaScript is a scripting language that is interpreted. There is no need for a compiler because there is no compilation process. JavaScript is interpreted by the browser as HTML tags.

• JavaScript is a simple programming language. It is very simple to learn for anyone. It's used to create dynamic and appealing websites.

• Because JavaScript is run on the client side, it lowers the load on the website server.

• It includes conditional checking, loops, and branching functionality that can be used in web pages.

• For the end user, JavaScript is relatively quick. They don't have to wait for the page to reload to see if they missed something.

• Web pages now have more functionality. To provide our site visitors with more functionality, we can use JavaScript to include drag-and-drop components and sliders.

JavaScript Example

<h2>Welcome to JavaScript</h2>    

<script>    

document.write("Hello JavaScript by TutorialandExample");    

</script>

Output

Welcome to JavaScript

Hello JavaScript by TutorialandExample

Javascript Example

<!DOCTYPE html>  

<html>  

<body>  

<h2>Welcome to JavaScript</h2>  

<script>  

document.write("Hello Friends");  

</script>  

</body>  

</html>

Output

Welcome to JavaScript

Hello Friends

JavaScript can be implemented by including JavaScript statements in the code.

<script>…</script>.

<!DOCTYPE html>  

<html>  

<body>  

<script type= "text/javascript">  

document.write("Hello World");  

</script>  

</body>  

</html>

Output

Hello World

In JavaScript, code may be written in three places.

1.  Between the <body>……</body> tag of HTML.
2.  Between the <head>……</head> tag of HTML.
3.  In .jsfile(external JavaScript).

As an illustration (code between the body tags)

In the example below, the body tag contains JavaScript code.

<!DOCTYPE html>  

<html>  

<body>  

<script type="text/javascript">  

alert("Hello world");  

</script>  

</body>  

</html>

Example2

(between the head tag, the code)

We'll create the function msg in the example below (). In JavaScript, you must write function in function name to define a function. To invoke a function, we must first create an event. We're using the one-click event to call the msg() function in this case.

<!DOCTYPE html>  

<html>  

<head>  

<script type="text/javascript">  

function msg(){  

alert("Hello world");  

}  

</script>  

</head>  

<body>  

<p>Welcome to Javascript</p>  

<form>  

<input type="button" value="click" onclick="msg()"/>  

</form>  

</body>  

</html

External JavaScript file

We can create a JavaScript file that we can include in HTML files.

Because a single JavaScript file may be used in multiple HTML pages, it allows for code reuse.

It improves the web page's performance.

The file must have a.js extension.

Example

<!DOCTYPE html>  

<html>  

<head>  

<script type="text/javascript" src="message.js"></script>  

</head>  

<body>  

<p>Hello world</p>  

<form>  

<input type="button" value="click" onclick="msg()"/>  

</form>  

</body>  

</html>

Javascript comment

Comments in JavaScript are used to describe the code. It's used to include code-related information, such as warnings or suggestions, so that end users can understand it.

JavaScript comments Types

1.  Single-line Comment
2.  Multi-line Comment

Single-line Comment

Double forward slashes (//) are used to express single-line comments. While the program is running, any text between the double forward slashes (//) and the end of the line will be ignored.

eg. Comment added - before the statement.

<!DOCTYPE html>  

<html>  

<body>  

<script>  

// single-line comment //  

document.write("hello world");  

</script>  

</body>  

</html>

eg. Comment added - after the statement.

<!DOCTYPE html>  

<html>  

<body>  

<script>  

var a=10; 

var b=20;  

var c=a+b; //It add values of a and b variable  

document.write(c); // print sum of 10 and 20  

</script>  

</body>  

</html>

Output

30

Multi-line comment

Single and multi-line comments can both be made with multi-line comments. Comments that span multiple lines begin with /* and conclude with */. JavaScript will ignore the text in between them.

/* Write comment here */

Example

<!DOCTYPE html>  

<html>  

<body>  

<script>  

/* It is multi-line comment.  

It will not be displayed */  

document.write ("Example of JavaScript multi line comment");  

</script>  

</body>  

</html>

Javascript Variable

Values (name=”Ram”) and expressions (Sum=x+y) are stored in variables.

We must first declare a variable before utilizing it. To declare a variable, we use the term var as follows:

var name;

There are 2 types of variables:

1.  Local Variable
2.  Global Variable

Local Variable – It's declared inside a function or a block.

Example

##### <script>  

##### functionabc(){  

##### var x=10; //local variable  

##### </script>

Global Variable - It has a global scope, meaning that it can be defined anywhere in JavaScript code.

Outside of the function, a variable is declared.

Example

<!DOCTYPE html>  

<html>  

<body>  

<script>  

var data =200; //global variable  

function a(){  

document.writeln(data);  

}  

function b(){  

document.writeln(data);  

}  

a();//calling javascript function  

b();  

</script>  

</body>  

</html>

In JavaScript, declaring a global variable within a function

To declare a JavaScript global variable inside a function, we must use the window object.

Example

##### window.value=90;

It can now be declared within any function and accessed from within any function.

Example

<!DOCTYPE html>  

<html>  

<body>  

<script>  

function a(){  

window.value=50; //declare global variable by use of window object  

}  

function b(){  

alert(window.value);//access global variable from other function  

}  

a();  

b();      

</script>  

</body>  

</html>

Javascript Data Types

It has a variety of data types to hold various types of values.

In Javascript, there are two sorts of data types.

1.  Primitive data types.
2.  Non-primitive data types.

Because JavaScript is a dynamic type language, we don't need to define the type of variable because the JavaScript engine uses it dynamically. The data type is specified using var in this case. It may store any type of value, including numbers, strings, and objects.

Example

##### var a=Ram; //String   

##### var b=20; //Number  

##### var x= {FirstName:''Ram'', lastName:''Doe''}; //Object

JavaScript - primitive data types

In JavaScript, there are five different types of primitive data types.

![](Image00000.jpg)

JavaScript non-primitive data types

There is 3 non-primitive data types are as follows:

![](Image00001.jpg)

Javascript Operators

Operators are symbols in JavaScript that are used to perform operations on operands. 3+2 equals 5 in simple terms. The operands here are 3 and 2, and the operator is +.

The JavaScript operators are as follows:

1.  Arithmetic Operators.
2.  Comparison (relational) Operators.
3.  Bitwise Operators.
4.  Logical Operators.
5.  Assignment Operators.
6.  Special Operators.

Arithmetic Operators

We employ arithmetic operations on the operands in arithmetic operators.

![](Image00002.jpg)

Comparison Operators

In the Comparison Operator, two operands A and B are compared.

![](Image00003.jpg)

Assignment operator

JavaScript support following - assign operators.

![](Image00004.jpg)

Bitwise Operators

JavaScript supports following - bitwise operators:

![](Image00005.jpg)

Logical Operators

Boolean values are commonly utilized with logical operators.

Following are the - logical operators-

![](Image00006.jpg)

Javascript If Else

A conditional statement in JavaScript is used to conduct different activities depending on the criteria.

In JavaScript, there are three types of statements.

1.  if Statement.
2.  if else Statement.
3.  if else if Statement.

if statement

If the condition is true or false, the if statement is used in JavaScript to run the function.

##### if (condition){ //   

#####     //content to be evaluated

##### }

![Image 1.jpg](Image00007.jpg)

Example:-

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=50;  

##### if(x>30){  

##### document.write("value of x is greater than 30");  

##### }  

##### </script >  

##### </body>  

##### </html>

output

Value of x is greater than 30

if else statement

If either condition is true or false, the if else statement is used.

Syntax

##### if(condition)  

##### {  

##### // set of statements  

##### }  

##### else  

##### {  

##### // set of statements  

##### }

![Image 2.jpg](Image00008.jpg)

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=20;  

##### if(x%2==0){  

##### document.write("x is even number");  

##### }  

##### else{  

##### document.write("a is odd number")  

##### }  

##### </script>  

##### </body>  

##### </html>

Output

X is even number

If else if

It merely looks at the content to see if the expression is true across many expressions. If otherwise if is a more complex version of the if else statement.

Syntax

##### If (condition1)  

##### {  

##### Statement(s) to be executed if condition 1 is true  

##### }  

##### else if (condition 2)  

##### {  

##### Statement(s) to be executed if condition 2 is true  

##### }  

##### else if (condition 3)  

##### {  

##### Statement(s) to be executed if condition 3 is true  

##### }  

##### else  

##### {     

##### Statement(s) to be executed if no condition is true  

##### }

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var x=50;  

##### if (x==10){  

##### document.write("x is equal to 10");  

##### }  

##### else if(x==50){  

##### document.write("x is equal to 50");  

##### }  

##### else if(x==30){  

##### document.write("x is equal to 30");  

##### }  

##### else{  

##### document.write("a is not equal to 10, 50 or 30");  

##### }     

##### </script>  

##### </body>  

##### </html>

Output

x is equal to 50

Javascript Switch Statement

In JavaScript, the switch statement is used to execute a single code under several conditions. It's the same as the else if statement, but it's easier to remember than the if..else..if statement.

![Image 3.jpg](Image00009.jpg)

Syntax

##### switch (expression)  

##### {  

##### case 1: statement(s)  

##### break;  

##### case 2: statement(s)  

##### break;  

##### â€¦..  

##### case n: statement(s)  

##### break;  

##### default: statements(s)  

##### }

NOTE:  In switch-case statements, the break statement is very important.

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var grade='B';  

##### var result;  

##### switch(grade){  

##### case 'A':  

##### result="A Grade";  

##### break;  

##### case 'B':  

##### result="B Grade";  

##### break;  

##### case 'C':  

##### result="C Grade";  

##### break;  

##### default:  

##### result="No Grade";  

##### }  

##### document.write(result);  

##### </script>  

##### </body>  

##### </html>

Output

B Grade

Javascript loop

Because the method of repeating forms a circle, repetition statements are referred to as loops. We use Loop statements to decrease the amount of lines in some cases. It's most commonly seen in Array.

In JavaScript, there are three different forms of loops.

1.  while loop
2.  for loop
3.  do-while loop

while loop

The code is performed in a while loop until the expression is true. If the number of iterations is unknown, it should be utilized.

![Image 4.jpg](Image00010.jpg)

Syntax

##### while (condition){  

##### statement(s) executed if expression is true  

##### }

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var i=1;  

##### while (i<=10)  

##### {  

##### document.write(i+ "<br/>");  

##### i++;  

##### }   

##### </script>  

##### </body>  

##### </html>

Output

1
2
3
4
5
6
7
8
9
10

For loop

It initialized the variable, checked the condition, and then incremented or decremented the value in the for loop.

It runs for a fixed amount of time.

![Image 5.jpg](Image00011.jpg)

Syntax

##### for (initialization; condition; increment)  

##### {  

##### code to be executed  

##### }

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### for (i=1; i<=12; i++)  

##### {  

##### document.write(i + "<br/>")  

##### }  

##### </script>  

##### </body>  

##### </html>

Output

1

2

3

4

5

6

7

8

9

10

11

12

do while loop

While a while loop executes items indefinitely, a do while loop executes code only once, regardless of whether the condition is true or false. We utilize do-while when we need to repeat the statement block at least once.

![Image 6.jpg](Image00012.jpg)

Syntax

##### do{  

##### code to be executed  

##### increment/decrement  

##### }  

##### while (condition);

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var i=11;  

##### do{  

##### document.write(i + "<br/>");   

##### i++;  

##### }while (i<=15);  

##### </script>  

##### </body>  

##### </html>

Output

11
12
13
14
15

JavaScript Function

The ability to define new functions within the Script>...../script> tag is an important feature of JavaScript. The function keyword is used to declare a function in JavaScript.

To reuse the code, we call the JavaScript method numerous times.

Advantages - JavaScript functions

1\. Code reusability: We use the same method several times to save time and code.

2\. Less coding: Our application is compressed as a result of this. When we conduct a routine task, we don't write a lot of code.

Syntax

##### function functionName(parameter or not)  

##### {  

##### statements  

##### }

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function msg()  

##### {  

##### alert("Hello! world");  

##### }  

##### </script>  

##### <input type="button" onclick="msg()" value="click here"/>  

##### </body>  

##### </html>

Output

Hello world!

Function with arguments

Call function by passing arguments.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function getcube(number)  

##### {  

##### alert(number* number* number);  

##### }  

##### </script>  

##### <form>  

##### <input type="button" value="click" onclick="getcube(3)"/>  

##### </form>  

##### </body>  

##### </html>

#### Output

27

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function getname()  

##### {  

##### name=prompt("Enter the Name");  

##### alert("Welcome Mr/Mrs " + name);  

##### }  

##### </script>  

##### </body>  

##### <form>  

##### <input type="button" value="Click" onclick="getname()"/>  

##### </form>  

##### </html>

Function with return value

Call function that - return value and - use it in program.

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### function getInfo()  

##### {  

##### return "Hello Raj! How are you?";  

##### }  

##### </script>  

##### <script>  

##### document.write(getInfo());  

##### </script>  

##### </body>  

##### </html>

Output

Hello Raj! How are you?

The Function() Constructor

A function statement isn't just for defining new functions; it may also be used to define functions dynamically using the Function() constructor and the new operator.

Syntax

##### <script>  

#####     var variablename = new Function(Arg1, Arg2...,  "Function Body" );   

##### </script>

Example

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script>  

##### var func = new Function("a", "b", "return a+b;");  

##### function secondFunction(){  

##### var result;  

##### result = func(50,50);  

##### document.write ( result );  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <p>Click button to call the function</p>  

##### <form>  

##### <input type="button" onclick="secondFunction()" value="Call Function">  

##### </form>  

##### <p>Use different parameters inside the function and try yourself...</p>  

##### </body>  

##### </html>

Function Literals

The concept of function literals, which is another way to construct functions, is introduced in JavaScript 1.2\. It's an expression that defines a function that doesn't have a name.

The syntax for a function literal is similar to that of a function statement, except that it is used as an expression rather than a statement, and there is no need for a function name.

Syntax

##### <script>  

##### var variablename = function (Argument List){  

#####           Function Body  

##### };    

##### </script>

Example

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script>  

##### var func = function(a,b){ return a+b };  

##### function secondFunction(){  

##### var result;  

##### result = func(10,20);  

##### document.write ( result );  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <p>Click the button to call the function</p>  

##### <form>  

##### <input type="button" onclick="secondFunction()" value="Call Function">  

##### </form>  

##### <p>Use different parameters inside the function and try yourself...</p>  

##### </body>  

##### </html>

Javascript Object

An object is a state-and-behavioral entity. JavaScript is a scripting language that focuses on objects. Although JavaScript is template-based rather than class-based, it allows us to create objects directly.

Syntax - to add property - to add object

##### objectName.objectProperty = propertyValue;

##### We use the  write()  method to document objects to write any content on the document.

##### Document.write("Hello world")

Example

#### The following example

###### shows how to - create an Object.

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <title>User-defined objects</title>  

##### <script type="text/javascript">  

##### var book = new Object();   // Object created  

##### book.subject = "5 points someone"; // Properties assign to the object  

##### book.author  = "ChetanBhagat";  

##### </script>  

##### </head>  

##### <body>  

##### <script type="text/javascript">  

##### document.write("Book Name is : " + book.subject + "<br>");  

##### document.write("Book Author is : " + book.author + "<br>");  

##### </script>  

##### </body>  

##### </html>

Output

Book Name is : 5 points someone
Book Author is : ChetanBhagat

Methods of an Object

Example

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <title>User-defined objects</title>  

##### <script type="text/javascript">// Define a function which will work as a method  

##### function addPrice(amount){  

##### this.price = amount;   

##### }  

##### function book(title, author){  

##### this.itle = title;  

##### this.author  = author;  

##### this.addPrice = addPrice; // Assign that method as property.  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <script type="text/javascript">  

##### varmyBook = new book("5 Points Someone", "ChetanBhagat");  

##### myBook.addPrice(150);  

##### document.write("Book Title is : " + myBook.title + "<br>");  

##### document.write("Book Author is : " + myBook.author + "<br>");  

##### document.write("Book Price is : " + myBook.price + "<br>");  

##### </script>  

##### </body>  

##### </html>

Output

Book Title is: 5 Points Someone

Book Author is :ChetanBhagat

Book Price is : 150

Javascript array

Arrays are used to represent a collection of elements in a single unit or memory region.

Every element that enters the array will be stored in the array with a unique index starting at zero. We can store data with the help of indexes.

In JavaScript, we must use the new keyword to declare an array. We use new Array to construct an array (n).

The number of slots in the array is denoted by n.

Syntax

myarray = new array(n);

NOTE:  We construct array objects with zero size whenever we build an array in JavaScript without specifying the size.

Example

##### <!DOCTYPE html>  

##### <html>  

##### <body>  

##### <script>  

##### var i;  

##### var emp = new Array();  

##### emp[0] = "Ajay";  

##### emp[1] = "Abhay";  

##### emp[2] = "Arun";  

##### emp[3] = "Shipra";  

##### for (i=0; i<emp.length; i++)  

##### {  

##### document.write(emp[i] + "<br>");  

##### }  

##### </script>  

##### </body>  

##### </html>

Output

Ajay
Abhay
Arun
Shipra

Example

##### <!DOCTYPE html>  

##### <html>  

##### <head>  

##### <script type="text/javascript">  

##### function array()  

##### {  

##### num = new Array(5)  

##### num[0] = 10  

##### num[1] = 20  

##### num[2] = 30  

##### num[3] = 40  

##### num[4] = 50  

##### sum = 0;  

##### for (i=0; i<num.length; i++)  

##### {  

##### sumsum = sum + num[i];  

##### }  

##### alert(sum)  

##### }  

##### </script>  

##### </head>  

##### <body>  

##### <input type="button" onclick="array()" value="click here">  

##### </body>  

##### </html>

Functions used in Array

![](Image00013.jpg)

LEARN REACTJS BASICS:

FOR BEGINNERS

FAST AND EASY WAY TO LEARN CODING BASICS

JP TAM

ReactJS Introduction

ReactJS Tutorial teaches you the fundamentals as well as some advanced ideas.

It is now the most important front-end library built by a Facebook software engineer named Jordan Walke.

It is built on a solid foundation and has a sizable community.

Facebook was the first to build and maintain it, and it has since been included into major products like as WhatsApp and Instagram.

In 2011, Facebook was the first to introduce React, but it wasn't until May 2013 that it was made public.

MVC (Model View Controller) architecture is now used by a large number of websites. The ‘V' in MVC stands for View, and React is the ‘V' in MVC.

There are various components that go into making a ReactJS application; these components are at the heart of all React apps.

When these components are combined with other parts, they allow for the creation of complex applications.

It fills the HTML DOM with data using virtual DOM. Because only the components of the DOM need to be changed rather than the entire DOM, virtual DOM is quick.

We'll need React components to build React applications, and these components will be organised inside the higher-level elements that determine the app's structure.

Let's look at an example of a form with buttons, labels, and input fields to see how it works.

Each element of the form is a React component, and the form itself is a higher-level component that defines the structure of the form.

After the updating of Virtual DOM, React determines the amendment that requires in the actual browser’s DOM.

Because of this, we have to write virtual components that React will turn into the real DOM instead of writing a React component directly into the DOM.

React Environment Setup Step by Step

React Environment Setup

This section will teach you how to set up an environment for developing ReactJS applications successfully:

Pre-Requisite for ReactJS

1.  NodeJS and NPM
2.  React and React DOM
3.  Webpack
4.  Babel

There are two ways - installing the ReactJS:

1.  Using npm command
2.  By using create-react-app

By using npm command

Step 1:  Install NodeJS. Go to https://nodejs.org

Step 2:  Click on downloads.

![Image 1.jpg](Image00014.jpg)

Step 3:  Install This Node.js

Step 4:  Use the following command to determine the version.

![Check the version by using commands](Image00015.jpg)

Step 5:  Now, in your preferred directory, create a root folder with the name you want.

![create a root folder in your desired directory](Image00016.jpg)

Step 6: Make a file called package.json. This file is necessary for module generation. Use the following command to make this file:

npm init –y

Step 7:  Using the npm command, instal React and associated DOM Packages:

npm install react react-dom –save  

Step 8:  Install Webpack

Webpack is primarily used for module packing, development, and automation of the production pipeline.

We must use the following command to instal Webpack.:

npm install webpack webpack-dev-server webpack-cli –save  

Webpack-dev-server is used during development, webpack is used to make production builds, and webpack-cli provides a set of instructions in the above command.

Step 9:  Install Babel.

Babel is a JavaScript compiler that allows you to convert one source code into another. Use the following command to instal Babel:

npm install babel-core babel-loader babel-preset-env babel-preset-react babel-webpack-plugin –save-dev  

Step 10:  Make a file. We need to add a few files to the project folder to finish the installation. The following are the files:

*   index.html
*   App.js
*   main.js
*   webpack.config.js
*   .babelrc

These files can be manually created or created using the command prompt. Use the command prompt to create files and type the following command:

type nul >  filename

Step 11:  Now,  Set Compiler, loader, and server for React Application

1.  Configure Webpack

To configure Webpack, add the following code to webpack.config.json. It changes the development server's port to 8080\. It is in charge of specifying the loaders for processing the file formats that your programme utilises, as well as installing any plugins that are required during development.

webpack.config.json

constpath=require('path');

constHtmlWebpackPlugin=require('html-webpack-plugin');

module.exports={

entry:'./main.js',

output:{

path:path.join(__dirname,'/bundle'),

filename:'index_bundle.js'

},

devServer:{

inline:true,

port:8080

},

module:{

rules:[

{

test:/\.jsx?$/,

exclude:/node_modules/,

use:{

loader:"babel-loader",

}

}

]

},

plugins:[

newHtmlWebpackPlugin({

template:'./index.html'

})

]

}

Now edit the package.json file and remove the lines “test” “echo ” Error: no test specified” && exit 1′′ from the “scripts” object, and replace them with the instructions start and build.

![Image 6.jpg](Image00017.jpg)

Remove the above-mentioned item and replace it with the following two:

1.  “start”: “webpack-dev-server –mode development –open –hot”,  
2.  “build”: “webpack –mode production”  

It is depicted in the figure below:

*   HTML webpack template for index.html

Using the HtmlWeb-packPlugin plugin, we need to create a custom template to generate index.html. It allows us to use a viewport tag to facilitate our app's mobile scaling.

In your index.html file, paste the following code.

index.html

<!DOCTYPEhtml>

<htmllang="en">

<head>

<metacharset="UTF-8">

<title>ReactApp</title>

</head>

<body>

<divid="app"></div>

<scriptsrc='index_bundle.js'></script>

</body>

</html>

*   App.jsx  and  main.js

This is the first react component and serves as the app's entrance point. Hello World will be rendered.

In your App.js file, paste the following code.

App.js

importReact,{Component}from'react';

classAppextendsComponent{

render(){

return(

<div>

<h1>HelloWorld</h1>

</div>

);

}

}

exportdefaultApp;

![Image 8.jpg](Image00018.jpg)

Now we must import and render this component to the root App element in order to see it in the browser.

main.js

importReactfrom'react';

importReactDOMfrom'react-dom';

importAppfrom'./App.js';

ReactDOM.render(<App/>,document.getElementById('app'));

*   Create .babelrc file

Add the following code to your  .babelrc  file.

.babelrc

{

"presets":[

"@babel/preset-env","@babel/preset-react"]

}

Now it's time to start the server. To start the server, type the following command in your command prompt, making sure it's in the same folder as the react files.

npm start

This command will display the port number, which will require a browser window to be opened. After you've opened it, you'll see the following:

![Image 9.jpg](Image00019.jpg)

![](Image00020.jpg)

![Image 10.jpg](Image00021.jpg)

The React Application's root directory contains a number of files and directories. The following are some examples:

1.  node_modules:  It includes React libraries as well as any additional third-party libraries that may be required.

2.  public:  It contains the application's public assets. It contains the index.html file, and React will mount the application on the div id=”root”></div> element by default.

3.  src:  There are multiple files in this folder, including App.css, App.js, App.test.js, index.css, index.js, and serviceWorker.js. The App.js file will be in charge of displaying the React output screen at all times.

4.  package-lock.json:  It generated automatically whenever the npm package alters either the package.json or the node modules tree. It isn't possible to publish it. It will be disregarded if it discovers a location other than the top-level package.

5.  package.json:  It contains information on the project's metadata. It gives npm information that allows it to identify the project's dependencies as well as the project itself.

6.  README.md:  It also includes the documentation for React topics.

React JSX

All React components, as we know, have a render function.

A React component's HTML output is specified by the Render function.

The JavaScript extension JSX allows you to write JavaScript code that appears like HTML. JSX is a react-specific HTML-like syntax that extends ECMAScript to allow HTML-like syntax to coexist alongside JavaScript/React programming.

Preprocessors (transpilers like Babel) employ this syntax to convert HTML-like syntax into standard JavaScript objects that a JavaScript engine can comprehend.

It allows you to put HTML/XML-like structures (e.g., DOM-like tree structures) in the same file as your JavaScript code, and then the preprocessor converts these expressions to actual JavaScript code. Like XML/HTML tags, JSX tags have a tag name, attributes, and children.

Why use JSX?

• It is faster than JavaScript because it optimises the code before it is translated to JavaScript.

• Rather than separating technologies by putting HTML and logic in different files, React uses components that include both.

• It is type-safe since most problems are discovered during compilation.

• It simplifies the process of creating templates.

Nested Elements in - JSX

If you want to use multiple elements, you must enclose them in a container element. The div is being utilised as a container element for three nested items.

App.JSX

import React, { Component } from 'react';

class App extends Component{

render(){

return(

<div>

<h1>Hello World !!</h1>

<h2>This is TutorialandExample</h2>

<p>Website with the best tutorials.</p>

</div>

)

}

}

export default App;

JSX Attributes

The characteristics of HTML elements in JSX are the same as in ordinary HTML. In JSX, attributes are named in camelcase rather than the conventional naming pattern of HTML, such as class in HTML becoming className in JSX. This is due to the fact that in JavaScript, the class keyword is a reserved keyword. In JSX, custom attributes can also be used. For custom attributes, we must use data-prefix.

The custom attribute data-customAttr is used as an attribute for the p> tag in the example below.

For example:

import React, { Component } from 'react';

class App extends Component{

render(){

return(

<div>

<h1>Hello World !!</h1>

<h2>This is TutorialandExample</h2>

<p data-customAttr = "hello">Website with the best tutorials.</p>  

</div>

);

}

}

export default App;

JavaScript Expressions

JavaScript expressions can be used inside of JSX. We'll need to wrap it with curly brackets {}.

The next example demonstrates this point more clearly.

Example:

import React, { Component } from 'react';

class App extends Component{

render(){

return(

<div>

<h1>{12+28}</h1>

<h1>Hello World !!</h1>

<h2>This is TutorialandExample</h2>

<p data-customAttr = {"hello"}>Website with the best tutorials.</p>

</div>

);

}

}

export default App;

We can't utilise if else statements in JSX; instead, we must use conditional (ternary) expressions. In the following example, the value of variable x equals 1, therefore the browser returns true; however, if we change this value to something other, the browser returns false.

For Example

import React, { Component } from 'react';

class App extends Component{

render(){

var x=1;

return(

<div>

<h1>{x == 1 ? 'True!' : 'False'}</h1>

<h2>This is TutorialandExample</h2>

<p data-customAttr = {"hello"}>Website with the best tutorials.</p>

</div>

);

}

}

export default App; 

JSX styling

Inline styles are recommended by React. CamelCase syntax is required to set inline styles. On particular items, React automatically appends px after the numeric value.

The styling in JSX is demonstrated in the following example:

For example:

import React, { Component } from 'react';

class App extends Component{

render(){

var newStyle = {

fontSize: 90,

fontFamily: 'Times New Roman',

color: '#789067'

}

return(  

<div>

<h1 style = {newStyle}>www.google.com</h1>

<h2>This is TutorialandExample</h2>

<p data-customAttr = {"hello"}>Website with the best tutorials.</p>

</div>

);

}

}

export default App;

JSX Comments

Curly braces must be used while composing comments. In JSX, comments start with /* and end with */, just like in JSX expressions. The example below demonstrates how to use comments in JSX.

For example:

import React, { Component } from 'react';

class App extends Component{

render(){

var newStyle = {fontSize: 90,

fontFamily: 'Times New Roman',

color: '#789067'

}  

return(

<div>

<h1 style = {newStyle}>www.google.com</h1>

<h2>This is TutorialandExample</h2>

<p data-customAttr = {"hello"}>Website with the best tutorials.</p>

{/* this is a comment of JSX*/

</div>

);

}

}

export default App;

React Components

To create a single-page application in the past, developers had to write thousands of lines of code.

It was quite difficult to make any changes to these applications because they follow the structure of traditional DOM.

If a mistake is discovered, it must be manually searched across the application and updated. To overcome this problem, a component-based strategy is used.

The entire application is separated into discrete logical groups of code, known as components, using this approach.

Components are the fundamental building blocks of a React application.

It simplifies the process of creating user interfaces.

Every component shares the same physical area but operates independently of one another, eventually merging into a parent component that will serve as the application's final user interface.

React components have their own structure, functions, and APIs.

They can be re-used depending on the situation.

The following are the two types of components in ReactJS:

1.  Functional Components (Stateless Components).
2.  Class Components (Stateful component).

Functional Components

Because they do not hold or maintain state, functional components are sometimes known as stateless components.

Functional components are a means of writing components that only have a render method and no state.

They are simple JavaScript functions that may or may not accept data as parameters.

We can also write a function that takes props (properties) as input and returns the displayed result.

The following is an example of stateless components:

Example

import React, { Component } from 'react'; 

class App extends React.Component { 

    render() { 

       return ( 

          <div> 

             <First/> 

             <Second/> 

          </div>   

       ); 

    } 

} 

class First extends React.Component { 

    render() { 

       return ( 

          <div>   

             <h1>Stateless Components</h1> 

          </div> 

       ); 

    } 

} 

class Second extends React.Component { 

    render() {   

       return ( 

          <div> 

             <h2>www.tutorialandexample.com</h2> 

             <p>This website has several tutorials.</p> 

          </div> 

       );   

    } 

}   

export default App;

Class Components

Because they retain or manage local state, class components are sometimes known as Stateful Components.

These components are more complicated than those that are stateless.

It necessitates extending React.

A class that extends the component and has a render function can be defined to build the Class.

The following is an example of a class component:.

Example:

In this example, we'll create a list of unordered components in which we'll dynamically append Name for each object in the data array. EcmaScript6 arrow syntax (=>) is used here, which is significantly cleaner than the old JavaScript syntax. It aids us in writing less lines of code for our elements. It comes in handy when we need to create a large number of item lists.

import React, { Component } from 'react'; 

class App extends React.Component { 

  constructor() { 

       super(); 

       this.state = { 

          data:  

          [ 

             {            

                "name":"Arun" 

             }, 

             {           

                "name":"Anup"            

             }, 

             {   

                "name":"Anil"         

             } 

          ] 

       } 

    } 

    render() { 

       return ( 

          <div> 

             <Name/> 

             <ul>           

                 {this.state.data.map((item) => <List data = {item} />)}          

             </ul>   

          </div> 

       ); 

    } 

} 

class Name extends React.Component { 

    render() {   

       return ( 

          <div> 

             <h1>Student Names</h1> 

          </div> 

       ); 

    } 

}   

class List extends React.Component { 

    render() { 

       return ( 

          <ul>           

             <li>{this.props.data.name}</li>  

          </ul> 

       );   

    } 

} 

export default App;

Pros and Cons of ReactJS

The following are some of the benefits and drawbacks of ReactJS:

Benefits of ReactJS

1.  Easy to - Learn and Use:

ReactJS is a simple to use and learn framework. It comes with a lot of documentation, training materials, and tutorials.

It is simple to comprehend for a developer with a JavaScript experience who can immediately begin developing web applications in a matter of days.

It is one of the JavaScript frameworks and is the V (view portion) in the MVC (Model-View-Controller) model.

We can't say ReactJS is feature-rich, but it does have the benefit of an open-source JavaScript user interface (UI) library, which aids in task execution.

2.  Creating Dynamic web - applications becomes easier:

Creating dynamic web apps using HTML strings was difficult due to the complicated coding necessary, but ReactJS has overcome this problem and made it simple.

It needs less coding and offers more features.

It makes use of the JSX (JavaScript) extension, which is a syntax that allows HTML quotes and HTML tag syntax to render certain subcomponents.

Machine-readable codes are also supported.

3.  Reusable Components:

The ReactJS web application is made up of several components, each with its own logic and controls.

These are in charge of producing a short, reusable HTML code that can be reused.

This reusable code makes it easier to design and maintain applications.

ReactJS uses a virtual DOM-based technique to fill the HTML DOM with data.

Because it simply alters the elements of particular DOMs rather than reloading it every time, the virtual DOM is quick.

4.  Performance Enhancement:

Because of Virtual DOM, ReactJS' speed has increased.

ReactJS is extremely fast.

ReactJS becomes significantly better than other frameworks as a result of this functionality.

There is a concept of managing virtual DOM behind this rationale.

The Document Object Model (DOM) is a cross-platform computer programming API for HTML, XML, and XHTML.

The DOM is exclusively contained within memory.

As a result, anytime we build a component, we don't write it to the DOM directly; instead, we write virtual components that transform into the DOM, resulting in smoother and faster performance.

5.  Handy Tools Support

ReactJS is also popular due to the availability of a useful collection of tools.

These technologies improve readability and make the developer's job easier.

These tools are Chrome and Firefox dev extensions that allow you to investigate the hierarchies of react components in the virtual DOM.

6.  Known to be - SEO friendly:

When it comes to SEO, there is a problem with standard frameworks.

Search engines have a hard time reading massive JavaScript apps in general. ReactJS solves this problem, making it easier for developers to navigate across numerous search engines.

That's why React.js apps may run on the server, with the virtual DOM rendering and returning a standard page to the browser.

7.  The benefit - of having - JavaScript library:

ReactJS provides a rich range of JavaScript libraries, which is why it is so popular among web developers.

The JavaScript library gives web developers more freedom to do things their own.

8.  Scope for - Code Testing

ReactJS applications are simple to start up.

It gives developers with the ability to swiftly test and debug their programmes using native tools.

Disadvantages of ReactJS

1.  High Pace development

It serves as both a benefit and a detriment.

It's a disadvantage since the environment changes so quickly that most developers don't want to have to relearn new ways of doing things on a frequent basis.

It might be difficult to keep up with all of these changes and constant updates.

They had to keep their abilities up to date and learn new ways of doing things on a regular basis.

2.  Poor Documentation

Another common drawback of continuously changing technologies is this.

Due to the rapid updating of react technologies, there is a lack of good documentation.

3.  View Part

Only the app's UI layers are handled by ReactJS.

As a result, other technologies must be chosen in order to provide a complete set of tooling for the project's development.

4.  JSX - as a barrier

ReactJS makes use of JSX, a syntax extension that allows HTML and JavaScript to be mixed together.

This strategy is advantageous, but some members of the development community, particularly new developers, regard JSX as a barrier.

Developers disagree about how difficult JSX is to learn.

Features of ReactJS

ReactJS is currently gaining popularity among developers as the greatest JavaScript framework. It's critical to the front-end ecosystem's success.

The following are some of the most important aspects of ReactJS:

*   JSX
*   Components
*   One-way data binding
*   Virtual DOM
*   Simplicity
*   Performance
*   Let’s elaborate on these features:

JSX

JavaScript XML is abbreviated as JSX. It's a JavaScript syntax that's been extended.

It has a syntax that is comparable to that of XML or HTML.

This syntax is converted into React Framework JavaScript Calls.

It improves ES6 to allow HTML-like text to coexist with JavaScript react code.

It is not required to use JSX in ReactJS, however it is recommended.

One-Way Data - Binding

ReactJS is built to follow the unidirectional data flow, often known as one-way Data Binding.

One-way data binding is beneficial since it allows for more control across the application.

When data flows in the opposite direction, additional characteristics are necessary.

It occurs because the components are assumed to be immutable, and the data contained within them is unchangeable.

Flux is a pattern that aids in data unidirectionality.

It gives the application additional flexibility, which leads to increased efficiency.

Virtual DOM

The virtual DOM is simply a replica of the real DOM. It's similar to one-way data binding.

Every time the web application is modified, the entire UI is re-rendered in virtual DOM representation.

The discrepancy between the new DOM (which is re-rendered) and the prior DOM's representation is then examined.

When it's done, real DOM modifies the items that have changed.

It reduces memory usage and speeds up the application.

Simplicity

As we all know, ReactJS makes use of JSX, which makes the application more user-friendly and the code more intelligible.

ReactJS uses a component-based approach, which allows the code to be reused.

It's simple to learn and utilise.

Components

ReactJS is composed of components, each of which has its own logic and controls.

The components are reusable, which makes code maintenance easier while working on large projects.

Performance

ReactJS is extremely fast. When compared to other frameworks, ReactJS benefits greatly from this functionality.

There is a concept of managing virtual DOM behind this rationale.

The Document Object Model (DOM) is a cross-platform computer programming API for HTML, XML, and XHTML.

The DOM is exclusively contained within memory.

As a result, anytime we build a component, we don't write it to the DOM directly; instead, we write virtual components that transform into the DOM, resulting in smoother and faster performance.

Comparison between React and Vue

Both React and Vue are well-known JavaScript libraries that are used to build hundreds of websites today.

Both React and Vue offer extremely powerful frameworks, each with their own set of advantages and disadvantages.

Which one you choose is determined by your business needs and use cases.

Both React and Vue have a lot of commonalities, such as component-based design, virtual DOM usage, props usage, debugging using Chrome Dev Tools, and so on.

Both of them differ from one another in the following ways:

![](Image00022.jpg)

![](Image00023.jpg)

![](Image00024.jpg)

ReactJS vs AngularJS

Difference between - ReactJS and AngularJS

AngularJS

AngularJS is an open source JavaScript framework that may be used to create a dynamic web application. It was created in 2009 by Misko Hovery and Adam Abrons, and it is presently maintained by Google. On March 11, 2019, AngularJS was updated to version 1.7.8\. It is mostly used to create single-page apps and leverages HTML and JavaScript attributes. The script> tag is used to incorporate it in an HTML page. It uses expressions to tie data to HTML and also extends HTML by using the directive to add built-in attributes.

Features of AngularJS

The following are some of the characteristics of AngularJS:

  1\. Data binding: AngularJS supports data binding in both directions. It's the data synchronisation between the model and display components that happens automatically.

  2\. POJO Model: The ‘Plain Old JavaScript Model,' which is employed by AngularJS, is       abbreviated as POJO. It provides both spontaneous and well-planned objects. It makes AngularJS self-contained and straightforward to utilise.

3.  MVC framework (Model View Controller): MVC is a software architecture paradigm that is used to create web applications. The functioning model of AngularJS is primarily built on MVC concepts. MVC in AngularJS has a dynamic, comfortable, and versatile architecture.
4.  Services: AngularJS comes with a number of built-in services, such as $http, which may be used to make an XMLHttpRequest.
5.  HTML for user interfaces: HTML is used to create user interfaces in AngularJS. AngularJS is a declarative language that uses shorter, easier-to-understand tags. It provides a slick, well-organized, and well-structured user interface.
6.  Dependency Injection: AngularJS features a dependency injection subsystem that simplifies the process of designing, understanding, and testing applications for developers.
7.  Google's Active Community: As we all know, Google maintains AngularJS, therefore in the event of a maintenance issue, there are numerous forums where questions can be answered.
8.  Routing: Routing is the system that allows you to move from one view to another. It's crucial for single-page apps, where everything is contained on a single page. Developers don't want to send visitors to a new page every time they click a menu item. The developer requires that the content be loaded on the same page as the URL is changed.

ReactJS

It is a critical front-end library created by a Facebook software engineer named Jordan Walke. Facebook was the first to create and maintain it, and it was later integrated into major products like as Whatsapp and Instagram. In 2011, Facebook was the first to introduce React, but it wasn't until May 2013 that it was made public.

ReactJS is an open-source JavaScript library for developing a single-page application's user interface. React is the ‘V,' which stands for View, according to MVC. There are various components that go into making a ReactJS app; these components comprise the heart of all React apps.

Features of ReactJS

*   JSX:  JavaScript XML is abbreviated as JSX. It's a JavaScript syntax that's been extended. It has a syntax that is comparable to that of XML or HTML. This syntax is converted into React Framework JavaScript Calls. It improves ES6 to allow HTML-like text to coexist with JavaScript react code. It is not required to use JSX in ReactJS, however it is recommended.

*   One-Way Data - Binding:  ReactJS is built to follow the unidirectional data flow, often known as one-way Data Binding. One-way data binding is beneficial since it allows for more control across the application. When data flows in the opposite direction, additional characteristics are necessary. It occurs because the components are assumed to be immutable, and the data contained within them is unchangeable. Flux is a pattern that aids in data unidirectionality. It gives the application additional flexibility, which leads to increased efficiency.

*   Virtual DOM:  The virtual DOM is simply a replica of the real DOM. It's similar to one-way data binding. Every time the web application is modified, the entire UI is re-rendered in virtual DOM representation. The discrepancy between the new DOM (which is re-rendered) and the prior DOM's representation is then examined. When it's finished, real DOM modifies the objects that have been altered. It reduces memory usage and speeds up the application.

*   Simplicity:  As we all know, ReactJS makes use of JSX, which makes the application more user-friendly and the code more intelligible. ReactJS uses a component-based approach, which allows the code to be reused. It's simple to learn and utilise.

*   Components:  ReactJS is composed of components, each of which has its own logic and controls. The components are reusable, which makes code maintenance easier while working on large projects.

*   Performance:  The performance of ReactJS is superb. When compared to other frameworks, ReactJS benefits greatly from this functionality. There is a concept of managing virtual DOM behind this rationale. The Document Object Model (DOM) is a cross-platform computer programming API for HTML, XML, and XHTML. The DOM is exclusively contained within memory. As a result, anytime we build a component, we don't write it to the DOM directly; instead, we write virtual components that transform into the DOM, resulting in smoother and faster performance.

Comparison Between - AngularJS v/s ReactJS

![](Image00025.jpg)

![](Image00026.jpg)

React Native vs ReactJS

Difference between - React Native - and ReactJS

React Native

React Native is an open-source JavaScript framework that may be used to create mobile apps for iOS, Android, and Windows.

It uses JavaScript to make a cross-platform mobile application.

React Native is similar to react, but instead of using web components as building blocks, it employs native components.

As a result, rather than using the browser, it is employed for mobile devices.

In 2013, it was also developed by Facebook for its well-known internal project Hackathon.

Facebook stated in March 2015 that React Native is open source and available on GitHub.

Advantages of - React Native

The following are some of the advantages of using React Native:

1.  Native Components:  If we need native functionality, we'll need to develop platform-specific code that hasn't been designed yet.

2.  Class Performance:  React Native's code is compiled into Native code, allowing it to run on both operating systems and perform the same functions.

3.  Cross-platform Usage:  It is compatible with both Android and iOS devices.

4.  JavaScript:  It is employed in the development of native mobile applications.

5.  Improving with time:  The best practises are always being developed by the community.

6.  Community:  It has a vast community that helps people get the answers they need.

7.  Uncertain Existence:  Because this framework was created by Facebook, its presence is unknown, as the company retains the rights to terminate the project at any time. It is unlikely to happen as the popularity of React Native grows.

Disadvantages - React Native

1.  Hard to learn : For a newcomer to the app development field, learning is difficult.

2.  Takes more time - in initialization:  Even for high-tech gadgets and devices, startup takes a long time.

3.  React Native - still new - immature:  React Native is still in beta and is only available for Android and iOS, which has a detrimental influence on mobile apps.

4.  Lacks the - security robustness:  React Native creates a security vulnerability. Experts advise against using React Native for developing banking and financial apps that demand a high level of confidentiality.

ReactJS

ReactJS is an open-source JavaScript library for developing a single-page application's user interface.

React is the ‘V,' which stands for View, according to MVC.

There are various components that go into making a ReactJS app; these components comprise the heart of all React apps.

When these components are combined with other parts, they allow for the creation of complex applications.

It is a critical front-end library created by a Facebook software engineer named Jordan Walke.

Facebook was the first to create and maintain it, and it was later integrated into major products like as Whatsapp and Instagram.

In 2011, Facebook was the first to introduce React, but it wasn't until May 2013 that it was made public.

Benefits of ReactJS

1.  Easy to - Learn and Use:

ReactJS is a simple to use and learn framework. It comes with a lot of documentation, training materials, and tutorials.

It is simple to comprehend for a developer with a JavaScript experience who can immediately begin developing web applications in a matter of days.

It is one of the JavaScript frameworks and is the V (view portion) in the MVC (Model-View-Controller) model.

We can't say ReactJS is feature-rich, but it does have the benefit of an open-source JavaScript user interface (UI) library, which aids in task execution.

2.  Creating Dynamic - web applications - becomes easier:

Creating dynamic web apps using HTML strings was difficult due to the complicated coding necessary, but ReactJS has overcome this problem and made it simple. It needs less coding and offers more features. It makes use of the JSX (JavaScript) extension, which is a syntax that allows HTML quotes and HTML tag syntax to render certain subcomponents. Machine-readable codes are also supported.

3.  Reusable Components:

The ReactJS web application is made up of several components, each with its own logic and controls.

These are in charge of producing a short, reusable HTML code that can be reused.

This reusable code makes it easier to design and maintain applications.

ReactJS uses a virtual DOM-based technique to fill the HTML DOM with data.

Because it simply alters the elements of particular DOMs rather than reloading it every time, the virtual DOM is quick.

4.  Performance Enhancement:

Because of Virtual DOM, ReactJS' speed has increased. ReactJS is extremely fast.

ReactJS becomes significantly better than other frameworks as a result of this functionality.

There is a concept of managing virtual DOM behind this rationale.

The Document Object Model (DOM) is a cross-platform computer programming API for HTML, XML, and XHTML.

The DOM is exclusively contained within memory.

As a result, anytime we build a component, we don't write it to the DOM directly; instead, we write virtual components that transform into the DOM, resulting in smoother and faster performance.

5.  Handy Tools Support

ReactJS is also popular due to the availability of a useful collection of tools.

These technologies improve readability and make the developer's job easier.

These tools are Chrome and Firefox dev extensions that allow you to investigate the hierarchies of react components in the virtual DOM.

6.  Known to be - SEO friendly:

When it comes to SEO, there is a problem with standard frameworks.

Search engines have a hard time reading massive JavaScript apps in general.

ReactJS solves this problem, making it easier for developers to navigate across numerous search engines.

That's why React.js apps may run on the server, with the virtual DOM rendering and returning a standard page to the browser.

7.  The benefit - JavaScript library:

ReactJS provides a rich range of JavaScript libraries, which is why it is so popular among web developers.

The JavaScript library gives web developers more freedom to do things their own.

8.  Scope - Code Testing

ReactJS applications are simple to start up. It gives the developer the ability to easily test and debug their code using native tools.

Disadvantages of ReactJS

1.  High Pace development

It serves as both a benefit and a detriment.

It's a disadvantage since the environment changes so quickly that most developers don't want to have to relearn new ways of doing things on a frequent basis.

It might be difficult to keep up with all of these changes and constant updates.

They must keep their abilities up to date and acquire new ways of doing things on a regular basis.

2.  Poor Documentation

Another common drawback of continuously changing technologies is this.

Due to the rapid updating of react technologies, there is a lack of good documentation.

3.  View Part

Only the app's UI layers are handled by ReactJS. As a result, other technologies must be chosen in order to provide a complete set of tooling for the project's development.

4.  JSX as barrier

ReactJS makes use of JSX, a syntax extension that allows HTML and JavaScript to be mixed together.

This strategy is advantageous, but some members of the development community, particularly new developers, regard JSX as a barrier. Developers disagree about how difficult JSX is to learn.

Difference - ReactJS - React Native

![](Image00027.jpg)

![](Image00028.jpg)

React State

The state is a changeable structure that holds data or information about the component.

A component's status can be altered over time. The status changes over time as a result of user interaction or system events.

Stateful components are components that have a state. It's an important part of the React component because it determines how it behaves and renders.

They're also in charge of making a component lively and engaging.

The goal of a state is to keep things as simple as possible.

The setState() method can be used to change the status, and calling it will cause the UI to update.

The local state or information is represented by a state.

It can be directly updated or accessed by the component or from within the component.

We must utilise the getInitialState() method to set an initial state before any interaction takes place.

For example, if we have five components that all require data or information from the state, we'll need to develop a container component to hold the state for them all.

Defining the State

We must first specify a default state of values for defining the component's initial state before we can define a state.

Add a class function Object() { [native code] } that uses this.state to assign an initial state.

The render() method can render the ‘this.state' attribute.

Example:

The following example demonstrates how to create a Stateful component using ES6 syntax:

import React, { Component } from 'react'; 

class App extends React.Component { 

constructor() {

super()

this.state = { displayBio: true }

}

render() {

const bio = this.state.displayBio ? ( 

<div>

<p><h3>This is tutorialexample website which provides you lot of tutorials.</h3></p>

</div>

) : nullreturn (

<div>

<h1> Hello World !!!!!!</h1>

{ bio }

</div>

)

}

}

export default App;

It is necessary to execute the super() method in the function Object() { [native code] } to set the state. This is due to the fact that this.state is uninitialized before the super() method is called.

Changing the State

The component's state can be updated by calling setState() and supplying a new state object as an argument. Now, in the aforementioned example, build a new method toggleDisplayBio() and bind this keyword to it; otherwise, it will not be accessible inside the toggleDisplayBio() method.

this.toggleDisplayBio=this.toggleDisplayBio.bind(this)

Example:

We're going to add a button to the render() method in the example below. The toggleDisplayBio() method is called when the button is pressed, and it displays the specified output.im

port React, { Component } from 'react'; 

class App extends React.Component {

constructor() {

super()

this.state = { displayBio: false }

console.log('Component this', this)

this.toggleDisplayBio = this.toggleDisplayBio.bind(this)

}

toggleDisplayBio(){

this.setState({displayBio: !this.state.displayBio});

}

render() {

return (

<div>

<h1>!! Hello World !!</h1>

{

this.state.displayBio ? (

<div>

<p><h4>This is tutoriaexample website that has a lot of tutorials. This website provides you a better source of learning.</h4></p>

<button onClick={this.toggleDisplayBio}> Show Less </button>

</div> (

<div>

<button onClick={this.toggleDisplayBio}> Read More </button>

</div>

)

}

</div>

)

}

}

export default App

React Props

The term "properties" is abbreviated as "prop." Because props are immutable, state and props are fundamentally different. Props are components that can only be read. It's the object that keeps track of a tag's attribute value, and it works similarly to HTML elements. It facilitates the transfer of data from one component to another. Props are comparable to function arguments in that they are supplied to the component in the same way that function arguments are passed to the function.

The props inside the component can't be changed. Within the components, we may add props, which are attributes. These properties are exposed as this.props in the component and are used to render dynamic data in our render method.

When you need immutable data in a component, add the reactDom.render() method to the ReactJS project's main.js file and utilise that file inside the component you need it in.

For example:

App.js

import React, { Component } from 'react';

class App extends React.Component {

render() {

return (

<div>

<h1> Hello { this.props.name } </h1>

<p> <h4> This is tutorialexample website which provides you lot of tutorials </h4></p>

</div>

);

}

}

export default App;

Main.js

import React from 'react';

import ReactDOM from 'react-dom';

import App from './App.js';

ReactDOM.render(<App name = "World" />, document.getElementById('app'));

Default Props

It is not required to include props in the reactDom.render() element at all times. Default props can also be set directly on the component function Object() { [native code] }. In the following example, it is well explained:

Example:

import React, { Component } from 'react';

class App extends React.Component {

render() {

return (

<div>

<h1>Hello World</h1>

<h2> Default Pros Example </h2>

<h3>Welcome to {this.props.name}</h3>

<p>tutorialexample provides you one of the best tutorials.</p>

</div>

);

}

}

App.defaultProps = {

name: "tutorialexample"

}

export default App;

Main.js

import React from 'react';

import ReactDOM from 'react-dom';

import App from './App.js';

ReactDOM.render(<App/>, document.getElementById('app'));

State and Props

In the app, both state and props can be merged. Props can be used to set the state in the parent component and then provide it to the child component.

For example:

App.js

import React, { Component } from 'react';

class App extends React.Component {

constructor(props) {

super(props);

this.state = {

name: "tutorialexample",

}

}

render() {  

return (

<div>

<Tutorial tutorialProp = {this.state.name}/>

</div>

);

}

}  

class Tutorial extends React.Component {

render() {

return (

<div>

<h1>State & Props Example</h1>

<h1>Welcome to {this.props.tutorialProp}</h1>

<p>tutorialexample provides you one of the best tutorials.</p>

</div>  

);

}

}

export default App;

Main.js

import React from 'react';

import ReactDOM from 'react-dom';

import App from './App.js';

ReactDOM.render(<App/>, document.getElementById('app'));

React Props Validation

Props are a good way to pass read-only attributes to react components, as we all know.

Proper use of the props is necessary in the component. If it is not utilised correctly, the component's behaviour may not be as expected.

As a result, props validation is critical for enhancing react components.

Props validation is a tool that aids developers in avoiding faults and problems in the future.

It improves the readability of the code.

PropTypes is a specific property used in React components that aids in bug detection by checking data types of values supplied by props, however it is not required to define components with PropTypes.

Validating Props

The react component's props are validated using App.propTypes.

When an invalid type passes any of the props, the JavaScript console will display warnings.

You'll configure the App.defaultProps after you've explained the validation rules.

Syntax:

class App extends React.Component {

render() {}

}

Component.propTypes = { /*Definition */};

Example:

There is an App component in this example that provides all of the props that we need. App.propTypes is used to validate the props in this case. You must include the line import PropTypes from ‘prop-types' in the App.js file to validate the props.

App.js

import React, { Component } from 'react';

import PropTypes from 'prop-types';

class App extends React.Component {

render() {

return (

<div>

<h1>ReactJS Props validation example</h1>

<table>

<tr>

<th>Type</th>

<th>Value</th>

<th>Validity</th>

</tr>

<tr>

<td>Boolean</td>

<td>{this.props.propBool ? "true" : "False"}</td>

<td>{this.props.propBool ? "true" : "False"}</td>

</tr>

<tr>

<td>Array</td>

<td>{this.props.propArray}</td>

<td>{this.props.propArray ? "true" : "False"}</td>

</tr>

<tr>

<td>Function</td>

<td>{this.props.propFunc(2)}</td>

<td>{this.props.propFunc(2) ? "true" : "False"}</td>

</tr>

<tr>

<td>Number</td>

<td>{this.props.propNumber}</td>

<td>{this.props.propNumber ? "true" : "False"}</td>

</tr>

<tr>

<td>String</td>

<td>{this.props.propString}</td>

<td>{this.props.propString ? "true" : "False"}</td>

</tr>

</table>

</div>

);

}

}

App.propTypes = {

propBool: PropTypes.bool.isRequired,

propArray: PropTypes.array.isRequired,

propFunc: PropTypes.func,

propNumber: PropTypes.number,

propString: PropTypes.string,

}

App.defaultProps = {

propBool: false,

propArray: [2,4,6],

propFunc: function(x){return x+5},

propNumber: 6-6,

propString: "Hello",

}

export default App;

Main.js

import React from 'react';

import ReactDOM from 'react-dom';

import App from './App.js';

ReactDOM.render(<App/>, document.getElementById('app'));

ReactJS Props Validators

![](Image00029.jpg)

![](Image00030.jpg)

![](Image00031.jpg)

React Component API

It's a really high-level API. It gives the application's code reusability while also making it absolutely unique. It can be used in a variety of ways to:

*   Creating Elements.
*   Transforming Elements.
*   Fragments.

We'll now go over the three most significant methods accessible in the React component API:

*   findDOMNode()
*   setState()
*   forceUpdate()

findDOMNode()

You must use ReactDOM to manipulate the DOM. The method findDOMNode() is used to locate DOM nodes. This approach assists us in locating or gaining access to the underlying DOM node.

Syntax:

ReactDOM.findDOMNode(component);

Example:

App.js

import React, { Component } from 'react';

import ReactDOM from 'react-dom';

class App extends React.Component {

constructor() {

super()

this.findDomNodeHandler1 = this.findDomNodeHandler1.bind(this);

this.findDomNodeHandler2 = this.findDomNodeHandler2.bind(this);

};

findDomNodeHandler1() {

var div1 = document.getElementById('One');

ReactDOM.findDOMNode(div1).style.color = 'red';

}

findDomNodeHandler2() {

var div2 = document.getElementById('Two');

ReactDOM.findDOMNode(div2).style.color = 'blue';

}

render() {

:return (

<div>

<center>

<h1>ReactJS Find DOM Node Example</h1>

<button onClick = {this.findDomNodeHandler1}>Button1</button>

<button onClick = {this.findDomNodeHandler2}>Button2</button>

<h3 id = "One">Red Color</h3>

<h3 id = "Two">Blue Color</h3>

</center>

</div>

)

}

}

export default App;

setState()

This method is used to update the component's state. Rather than altering the state instantaneously, it just modifies the existing state. It's the main technique for modifying the user interface (UI) in response to event handlers and server responses.

Syntax:

this.stateState(object newState[, function callback]);

Example:

App.js

import React, { Component } from 'react';

import PropTypes from 'prop-types';

class App extends React.Component {

constructor() {

super();

this.state = {

data: "!!!! Hello World !!!!"

}

this.updateSetState = this.updateSetState.bind(this);

}

updateSetState() {

this.setState({

data:"Welcome to tutorialexample"

});

}

render() {

return (

<div>

<center>

<h1>{this.state.data}</h1> <button onClick = {this.updateSetState}>SET STATE</button>

</center>

</div>  

)

}

}  

export default App

Main.js

import React from 'react';

import ReactDOM from 'react-dom';

import App from './App.js';

ReactDOM.render(<App/>, document.getElementById('app'));

forceUpdate()

This method allows the manually updating of the components.

Syntax:

Component.forceUpdate(callback);

Example:

App.js

import React, { Component } from 'react';

class App extends React.Component {

constructor() {

super()

this.forceUpdateState = this.forceUpdateState.bind(this);

}

forceUpdateState() {

this.forceUpdate();

};

render() {

return (

<div>

<center>

<h1>Example of Force Update method</h1>

<h2>Example to Generate Random Number</h2>

<h3>Random number: {Math.random()}</h3>

<button onClick = {this.forceUpdateState}>ForceUpdate</button>

</center>

</div>

);

}

}

export default App;

React Component Life-Cycle

Each component's construction process in ReactJS has multiple lifecycle functions. These methods are referred to as the component's lifespan. The component's life cycle is divided into four phases:

*   Initial Phase
*   Mounting Phase
*   Updating Phase
*   Unmounting Phase

Every stage of the lifecycle has its own set of methods. Let's go over each of these stages one by one:

Initial Phase

The birth step of a ReactJS component's lifecycle is referred to as this. The component's initial state and default props are included in this phase. These default properties are set in the function Object() { [native code] } of the component. This is a one-time step that involves the following methods:

*   getDefaultProps()

It's where you set the default value for this.props. It is called before the component is created.

*   getInitialState()

This.state's default value is specified with this.state.default.

Mounting Phase

In this phase, an instance of a component is created and added into the DOM. It entails the following procedures:

*   componentWillMount()

It is called just before a component is rendered into the DOM. If you call setState() within this method, the component will not be re-rendered.

*   componentDidMount()

It is called immediately after a component has been rendered and placed on the DOM. You can now query the DOM in any way you want.

*   render()

Every component has a definition for it. It's in charge of returning only one root HTML node element. You can produce a null or false value if you don't want to render anything.

Updating Phase

It's the next step in the lifecycle of a React component. We obtain fresh Props and change the State here. This phase also allows you to handle user interaction and provide communication with the component hierarchy. The primary goal of this phase is to ensure that the component is showing the most recent version.

This phase, unlike the Birth or Death phases, repeats itself over and over. It entails the following procedures:

*   componentWillReceiveProps()

When a component receives new props, this method is called. You must compare this if you expect the state to be updated in response to prop changes. next and props Props for using this to make the state transition. The setState() method is used to change the state of the system.

*   shouldComponentUpdate()

It is called anytime a component decides to make a DOM change or update. It allows you to control the component's behaviour as well as change it. When this function returns true, the component will be updated. The component will not update if this is not done.

*   componentWillUpdate()

It is called right before a component update occurs. By invoking this, you are not able to change the state of the component. The setState() method is used to change the state of the system. If the method shouldComponentUpdate() returns false, it will not be called.

*   render()

This.props and this.state are examined, and types such as React Elements, Arrays, and Fragments, Booleans or null, String, and Number are returned. If the function shouldComponentUpdate() returns false, the render() code will be run again to ensure that the component shows correctly.

*   componentDidUpdate()

It is called immediately after the component has been updated. This function allows you to put whatever code inside it that you wish to run when an update occurs. The initial render is not called with this method.

Unmounting Phase

The lifespan of a React component comes to an end with this phase. When the component's instance is killed and unmounted from the DOM, this function is called. Only one method is included in this phase, which is listed below:

*   componentWillUnmount()

Before a component is permanently deleted and unmounted, this procedure is called. It executes any cleanup actions that are required, such as invalidating timers, event listeners, cancelling network requests, and clearing up DOM elements. It will not be possible to remount the component instance once it has been unmounted.

Example

importReact,{Component}from'react';

classAppextendsReact.Component{

constructor(props){

super(props);

this.state={world:"World"};

this.changeState=this.changeState.bind(this)

}

render(){

return(

<center>

<div>

<h1>ExampleofReactJScomponentsLifecycle</h1>

<h3>Hello{this.state.world}</h3>

<buttononClick={this.changeState}>ClickHere!</button>

</div></center>

);

}

componentWillMount(){

console.log('ComponentWillMOUNT!')

}

componentDidMount(){

console.log('ComponentDidMOUNT!')

}

changeState(){

this.setState({world:"All!!-ItsanexampleofReactJScomponentLifecycle."});

}

componentWillReceiveProps(newProps){

console.log('ComponentWillRecieveProps!')

}

shouldComponentUpdate(newProps,newState){

returntrue;

}

componentWillUpdate(nextProps,nextState){

console.log('ComponentWillUPDATE!');

}

componentDidUpdate(prevProps,prevState){

console.log('ComponentDidUPDATE!')

}

componentWillUnmount(){

console.log('ComponentWillUNMOUNT!')

}

}

exportdefaultApp;

React Constructors

What is constructor?

The function Object() { [native code] } is a method that is used to initialise the state of a class object.

It is called automatically when an object in the class is created.

The function Object() { [native code] } notion is the same in React as well. A React component's function Object() { [native code] } is called before the component is mounted.

You must call the super(pros) function before any other line when writing a React component's function Object() { [native code] }. This.props will be undefined in the function Object() { [native code] } if super(pros) is not called, which might lead to errors.

Syntax

Constructor(props){

super(props);

}

The constructors are mostly used for two purposes in React:

1\. By assigning an object to this.state, it is utilised to initialise the component's local state.

2\. It's utilised to bind the event handler function that your component has.

It is not necessary to build a function Object() { [native code] } for a React component if you are not initialising the state or binding the methods for your React component.

The function Object() { [native code] } cannot call the setState() function directly (). If the component requires local state, you must assign the initial state using ‘this.state' in the function Object() { [native code] }. The lone function Object() { [native code] } assigns the initial state using this.state, while all other methods need the usage of the set.state() method.

Example:

The constructor's notion is demonstrated in the following example:

App.js

import React, { Component } from 'react';

class App extends Component {

constructor(props){

super(props);

this.state = {

data: 'Hello World'

}

this.handleEvent = this.handleEvent.bind(this);  

}

handleEvent(){

console.log(this.props);

}

render() {

return (

<div className="App">  

<center>

<h2>Example of React Constructor</h2>

<input type ="text" value={this.state.data}/>

<br/><br/>

<button onClick={this.handleEvent}>Please Click</button> </center>

</div>

);

}

}  

export default App;

Main.js

import React from 'react';

import ReactDOM from 'react-dom';

import App from './App.js';

ReactDOM.render(<App />, document.getElementById('app'));

Arrow Functions

It's a brand-new feature in the ES6 specification. It is not necessary to tie any event to ‘this' while using arrow functions, nor is it necessary to bind ‘this' inside the function Object() { [native code] }.

Example:

We used bind() in the previous example, but we don't need it now that we're utilising the arrow function. The following example shows how to use the program's arrow function.

importReact,{Component}from'react';

classAppextendsComponent{

constructor(props){

super(props);

this.state={

data:'HelloWorld'

}

this.handleEvent=this.handleEvent.bind(this);

}

handleEvent=()=>{

console.log(this.props);

}

render(){

return(

<divclassName="App">

<center>

<h2>ExampleofReactConstructor</h2>

<inputtype="text"value={this.state.data}/>

<br/><br/>

<buttononClick={this.handleEvent}>PleaseClick</button></center>

</div>

);

}

}

exportdefaultApp;