![](Images/cover00136.jpeg)

LEARN JAVASCRIPT BASICS:

FOR BEGINNERS

AND

JAVASCRIPT WORKBOOK

FOR

EXAMS AND INTERVIEWS

FAST AND EASY WAY TO LEARN CODING BASICS

JP TAM

[Javascript Tutorial](#part0003.xhtml__Toc78463966)

[Javascript Example](#part0004.xhtml__Toc78463967)

[Javascript comment](#part0005.xhtml__Toc78463968)

[Javascript Variable](#part0006.xhtml__Toc78463969)

[Javascript Data Types](#part0007.xhtml__Toc78463970)

[Javascript Operators](#part0008.xhtml__Toc78463971)

[Logical Operators](#part0008.xhtml__Toc78463972)

[Javascript If Else](#part0009.xhtml__Toc78463973)

[Javascript Switch Statement](#part0010.xhtml__Toc78463974)

[Javascript loop](#part0011.xhtml__Toc78463975)

[do while loop](#part0011.xhtml__Toc78463976)

[JavaScript Function](#part0012.xhtml__Toc78463977)

[Function with arguments](#part0012.xhtml__Toc78463978)

[Javascript Object](#part0013.xhtml__Toc78463979)

[Javascript array](#part0014.xhtml__Toc78463980)

[JAVASCRIPT WORKBOOK](#part0016.xhtml__Toc78463981)

[Capitalize The First Letter](#part0016.xhtml__Toc78463982)

[Hours and minutes](#part0017.xhtml__Toc78463983)

[Count vowels](#part0018.xhtml__Toc78463984)

[Create a new string](#part0019.xhtml__Toc78463985)

[Concatenate two strings](#part0020.xhtml__Toc78463986)

[First not repeated character](#part0021.xhtml__Toc78463987)

[Find the longest word](#part0022.xhtml__Toc78463988)

[Counts the number of vowels](#part0023.xhtml__Toc78463989)

[Check a number is prime](#part0024.xhtml__Toc78463990)

[JavaScript: Get the data type](#part0025.xhtml__Toc78463991)

[Find the second lowest and second greatest](#part0026.xhtml__Toc78463992)

[Add two digits](#part0027.xhtml__Toc78463993)

[Leap Year Check](#part0028.xhtml__Toc78463994)

[Check given positive number](#part0029.xhtml__Toc78463995)

[string starts with 'Java' - Check](#part0030.xhtml__Toc78463996)

[Two given integer values - Check](#part0031.xhtml__Toc78463997)

[Find a value which is nearest to 100](#part0032.xhtml__Toc78463998)

[Positive number - Check](#part0033.xhtml__Toc78463999)

[String starts with 'Java' - Check](#part0034.xhtml__Toc78464000)

[Multiplication and division](#part0035.xhtml__Toc78464001)

[Convert temperatures](#part0036.xhtml__Toc78464002)

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

Local Variable– It's declared inside a function or a block.

Example

##### <script>  

##### functionabc(){  

##### var x=10; //local variable  

##### </script>

Global Variable- It has a global scope, meaning that it can be defined anywhere in JavaScript code.

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

![](Images/image00101.jpeg)

JavaScript non-primitive data types

There is 3 non-primitive data types are as follows:

![](Images/image00102.jpeg)

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

![](Images/image00103.jpeg)

Comparison Operators

In the Comparison Operator, two operands A and B are compared.

![](Images/image00104.jpeg)

Assignment operator

JavaScript support following - assign operators.

![](Images/image00105.jpeg)

Bitwise Operators

JavaScript supports following - bitwise operators:

![](Images/image00106.jpeg)

Logical Operators

Boolean values are commonly utilized with logical operators.

Following are the - logical operators-

![](Images/image00107.jpeg)

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

![Image 1.jpg](Images/image00108.jpeg)

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

![Image 2.jpg](Images/image00109.jpeg)

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

![Image 3.jpg](Images/image00110.jpeg)

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

NOTE: In switch-case statements, the break statement is very important.

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

![Image 4.jpg](Images/image00111.jpeg)

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

![Image 5.jpg](Images/image00112.jpeg)

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

![Image 6.jpg](Images/image00113.jpeg)

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

##### We use the write() method to document objects to write any content on the document.

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

NOTE: We construct array objects with zero size whenever we build an array in JavaScript without specifying the size.

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

![](Images/image00114.jpeg)

JAVASCRIPT

WORKBOOK

FOR

EXAMS AND INTERVIEWS

FAST AND EASY WAY TO

LEARN CODING BASICS

JP TAM

# JAVASCRIPT WORKBOOK

# Capitalize The First Letter

## Of Each Word

### Of A Given String

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00115.jpeg)

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function capital_letter(str)

##### {

#####     str = str.split(" ");

#####     for (var i = 0, x = str.length; i < x; i++) {

#####         str[i] = str[i][0].toUpperCase() + str[i].substr(1);

#####     }

#####     return str.join(" ");

##### }

### ![](Images/image00116.jpeg)

### OUTPUT

Output:

![](Images/image00117.jpeg)

# Hours and minutes

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00118.jpeg) 

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function time_convert(num)

##### {

#####   var hours = Math.floor(num / 60); 

#####   var minutes = num % 60;

#####   return hours + ":" + minutes;        

##### }

##### console.log(time_convert(71));

##### console.log(time_convert(450));

##### console.log(time_convert(1441));

### OUTPUT

1:11

7:30

24:1

# Count vowels

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to count the number of vowels in a given string.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function vowel_Count(str)

##### {

#####   return str.replace(/[^aeiou]/g, "").length;

##### }

##### console.log(vowel_Count("Python"));

##### console.log(vowel_Count("htmlresource.com"));

### Output:

1

5

#  Create a new string 

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

 ![](Images/image00119.jpeg)

</head>

<body>

</body>

</html>

### JAVASCRIPT CODE

function without_first_end(str) {

  return str.substring(1, str.length - 1);

}

console.log(without_first_end('JavaScript'));

console.log(without_first_end('JS'));

console.log(without_first_end('PHP'));

### Output:

avaScrip

H

# Concatenate two strings

## Except their first character

### HTML CODE

<!DOCTYPE html>

<html>

<head>

  <meta charset="utf-8">

  <meta name="viewport" content="width=device-width">

  <title>JavaScript program to concatenate two strings except their first character.</title>

</head>

<body>

</body>

</html>

### JAVASCRIPT CODE

function concatenate(str1, str2) {

  str1 = str1.substring(1, str1.length);

  str2 = str2.substring(1, str2.length);

  return str1 + str2;

}

console.log(concatenate("PHP","JS"));

console.log(concatenate("A","B"));

console.log(concatenate("AA","BB"));

### Output:

HPS

AB

# First not repeated character

## ![](Images/image00120.jpeg)

## HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <title>find the first not repeated character.</title>

##### </head>

##### <body>

##### </body>

##### </html>

## JAVASCRIPT CODE

function find_FirstNotRepeatedChar(str) {

  var arra1 = str.split('');

  var result = '';

  var ctr = 0;

  for (var x = 0; x < arra1.length; x++) {

    ctr = 0;

    for (var y = 0; y < arra1.length; y++)

    {

      if (arra1[x] === arra1[y]) {

        ctr+= 1;

      }

    }

    if (ctr < 2) {

      result = arra1[x];

      break;

    }

  }

  return result;

}

console.log(find_FirstNotRepeatedChar('abacddbec'));

### OUTPUT

e

# Find the longest word

## within a string

![](Images/image00121.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Find the longest word within a string</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function find_longest_word(str)

##### {

#####   var array1 = str.match(/\w[a-z]{0,}/gi);

#####   var result = array1[0];

#####   for(var x = 1 ; x < array1.length ; x++)

#####   {

#####     if(result.length < array1[x].length)

#####     {

#####     result = array1[x];

#####     }

#####   }

#####   return result;

##### }

##### console.log(find_longest_word('Web Development Tutorial'));

### OUTPUT

Development

# Counts the number of vowels

## within a string

### ![](Images/image00122.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Counts the number of vowels within a string</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function vowel_count(str1)

##### {

#####   var vowel_list = 'aeiouAEIOU';

#####   var vcount = 0;

#####   for(var x = 0; x < str1.length ; x++)

#####   {

#####     if (vowel_list.indexOf(str1[x]) !== -1)

#####     {

#####       vcount += 1;

#####     }

#####   }

#####   return vcount;

##### }

##### console.log(vowel_count("The quick brown fox"));

#### OUTPUT

5

# Check a number is prime

![](Images/image00123.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Check a number is prime or not</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function test_prime(n)

##### {

#####   if (n===1)

#####   {

#####     return false;

#####   }

#####   else if(n === 2)

#####   {

#####     return true;

#####   }else

#####   {

#####     for(var x = 2; x < n; x++)

#####     {

#####       if(n % x === 0)

#####       {

#####         return false;

#####       }

#####     }

#####     return true; 

#####   }

##### }

##### console.log(test_prime(37));

### OUTPUT

True

# JavaScript: Get the data type

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Detect JavaScript Data Types</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function detect_data_type(value)

##### {

##### var dtypes = [Function, RegExp, Number, String, Boolean, Object], x, len;

##### if (typeof value === "object" || typeof value === "function")

#####     {

#####      for (x = 0, len = dtypes.length; x < len; x++)

#####      {

#####             if (value instanceof dtypes[x])

#####             {

#####                 return dtypes[x];

#####             }

#####       }

#####     }

#####     return typeof value;

##### }

##### console.log(detect_data_type(12));

##### console.log(detect_data_type('w3resource'));

##### console.log(detect_data_type(false));

#### OUTPUT

number

string

Boolean

# Find the second lowest and second greatest

## numbers from an array

![](Images/image00124.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Find the second lowest and second greatest numbers from an array</title>

##### </head>

##### <body>

##### </body>

### JAVASCRIPT CODE

##### function Second_Greatest_Lowest(arr_num)

##### {

#####   arr_num.sort(function(x,y)

#####            {

#####            return x-y;

#####            });

#####   var uniqa = [arr_num[0]];

#####   var result = [];

#####   for(var j=1; j < arr_num.length; j++)

#####   {

#####     if(arr_num[j-1] !== arr_num[j])

#####     {

#####       uniqa.push(arr_num[j]);

#####     }

#####   }

#####     result.push(uniqa[1],uniqa[uniqa.length-2]);

#####   return result.join(',');

#####   }

##### console.log(Second_Greatest_Lowest([1,2,3,4,5]));

#### OUTPUT

2,4

# Add two digits

## Of a given positive integer

### Of length two

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to add two digits of a given positive integer of length two.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function add_two_digits(n)

#####    {

#####       return n % 10 + Math.floor(n / 10);

#####    }

##### console.log(add_two_digits(25))

##### console.log(add_two_digits(50))

### Output:

7

5

# Leap Year Check

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### <title>Find Leap Year</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function leapyear(year)

##### {

##### return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);

##### }

##### console.log(leapyear(2016));

##### console.log(leapyear(2000));

##### console.log(leapyear(1700));

##### console.log(leapyear(1800));

##### console.log(leapyear(100));

### OUTPUT

true

true

false

false

false

# Check given positive number

## ![](Images/image00125.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to check whether a given positive number is a multiple of 3 or a multiple of 7\. </title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function test37(x)

##### {

#####   if (x % 3 == 0 || x % 7 == 0)

#####   {

#####     return true;

#####   }

#####   else {

#####     return false;

#####   }

##### }

##### console.log(test37(12));

##### console.log(test37(14));

##### console.log(test37(10));

##### console.log(test37(11));

### Output:

true

true

false

false

# string starts with 'Java' - Check

## And false otherwise

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####   <title>JavaScript program to check whether a string starts with 'Java' and false otherwise.</title>

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function start_spec_str(str)

##### {

#####   if (str.length < 4)

#####   {

#####     return false;

#####   }

#####   front = str.substring(0, 4);

#####   if (front == 'Java')

#####   {

#####     return true;

#####   }

#####    else

#####    {

#####     return false;

#####   }

##### }

##### console.log(start_spec_str("JavaScript"));

##### console.log(start_spec_str("Java"));

##### console.log(start_spec_str("Python"));

### Output:

true

true

false

# Two given integer values - Check

### ![](Images/image00126.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00127.jpeg)

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function check_numbers(x, y)

#####   {

#####   if ((x >= 50 && x <= 99) || (y >= 50 && y <= 99))

#####   {

#####     return true;

#####   }

#####   else

#####   {

#####     return false;

#####   }

##### }

##### console.log(check_numbers(12, 101));

##### console.log(check_numbers(52, 80));

##### console.log(check_numbers(15, 99));

### OUTPUT

false

true

true

# Find a value which is nearest to 100

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00128.jpeg)

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function near_100(x, y) {

#####   if (x != y)

#####   {

#####   x1 = Math.abs(x - 100);

#####   y1 = Math.abs(y - 100);

#####   if (x1 < y1)

#####   {

#####     return x;

#####   }

#####   if (y1 < x1)

#####   {

#####     return y;

#####   }

#####   return 0;

#####   }

#####   else

#####     return false;

##### }

##### console.log(near_100(90, 89));

##### console.log(near_100(-90, -89));

##### console.log(near_100(90, 90));

### Output:

90

-89

false

# Positive number - Check

### ![](Images/image00129.jpeg)

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

#####  ![](Images/image00130.jpeg)

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function test37(x)

##### {

#####   if (x % 3 == 0 || x % 7 == 0)

#####   {

#####     return true;

#####   }

#####   else {

#####     return false;

#####   }

##### }

##### console.log(test37(12));

##### console.log(test37(14));

##### console.log(test37(10));

##### console.log(test37(11));

### Output:

true

true

false

false

# String starts with 'Java' - Check

## And false otherwise

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

#####   <meta charset="utf-8">

#####   <meta name="viewport" content="width=device-width">

##### ![](Images/image00131.jpeg) 

##### </head>

##### <body>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function start_spec_str(str)

##### {

#####   if (str.length < 4)

#####   {

#####     return false;

#####   }

#####   front = str.substring(0, 4);

#####   if (front == 'Java')

#####   {

#####     return true;

#####   }

#####    else

#####    {

#####     return false;

#####   }

##### }

##### console.log(start_spec_str("JavaScript"));

##### console.log(start_spec_str("Java"));

##### console.log(start_spec_str("Python"));

### Output:

true

true

false

# Multiplication and division

## of two numbers

### HTML CODE

##### <!DOCTYPE html>

##### <html>

##### <head>

##### <meta charset=utf-8 />

##### ![](Images/image00132.jpeg)

##### <style type="text/css">

##### body {margin: 30px;}

##### </style>

##### </head>

##### <body>

##### <form>

##### 1st Number : <input type="text" id="firstNumber" /><br>

##### 2nd Number: <input type="text" id="secondNumber" /><br>

##### <input type="button" onClick="multiplyBy()" Value="Multiply" />

##### <input type="button" onClick="divideBy()" Value="Divide" />

##### </form>

##### <p>The Result is : <br>

##### <span id = "result"></span>

##### </p>

##### </body>

##### </html>

### JAVASCRIPT CODE

##### function multiplyBy()

##### {

#####         num1 = document.getElementById("firstNumber").value;

#####         num2 = document.getElementById("secondNumber").value;

#####         document.getElementById("result").innerHTML = num1 * num2;

##### }

##### function divideBy()

##### {

#####         num1 = document.getElementById("firstNumber").value;

#####         num2 = document.getElementById("secondNumber").value;

##### document.getElementById("result").innerHTML = num1 / num2;

##### }

#### OUTPUT

![](Images/image00133.jpeg)

# Convert temperatures

### ![](Images/image00134.jpeg)

### HTML CODE

##### <!DOCTYPE html>

#####   <html>

#####   <head>

#####   <meta charset="utf-8">

#####   <title>Write a JavaScript program to convert temperatures to and from celsius, fahrenheit</title>

#####   </head>

#####   <body>

##### </body>

#####   </html>

### JAVASCRIPT CODE

##### function cToF(celsius)

##### {

#####   var cTemp = celsius;

#####   var cToFahr = cTemp * 9 / 5 + 32;

#####   var message = cTemp+'\xB0C is ' + cToFahr + ' \xB0F.';

#####     console.log(message);

##### }

##### function fToC(fahrenheit)

##### {

#####   var fTemp = fahrenheit;

#####   var fToCel = (fTemp - 32) * 5 / 9;

#####   var message = fTemp+'\xB0F is ' + fToCel + '\xB0C.';

#####     console.log(message);

##### }

##### cToF(60);

##### fToC(45);

### OUTPUT

![](Images/image00135.jpeg)